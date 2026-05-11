---
title: Study Complete
layout: news_eval
permalink: /news_eval_complete.html
---
<html>
  <head>
    <style>
      body {
        line-height: 1.45;
      }

      h1, p {
        margin-top: 0.55em;
      }

      h1 {
        font-size: 28px;
      }

      p {
        font-size: 15px;
      }

      .complete-note {
        margin: 14px 0;
        padding: 12px 14px;
        border-left: 4px solid #2c6f8e;
        background: #f3fbfe;
      }

      .close-tab-banner {
        display: none;
        margin: 16px 0;
        padding: 12px 14px;
        border-left: 4px solid #2d7a31;
        background: #eef9ef;
        font-size: 15px;
      }

      .timer-banner {
        margin: 16px 0;
        padding: 12px 14px;
        border-left: 4px solid #8a6d1f;
        background: #fff9e8;
        font-size: 15px;
      }

      /* Hide Jekyll theme navigation for this standalone completion page */
      nav, .site-nav, .navbar, .header, .nav-header, [role="navigation"] {
        display: none !important;
      }

      .trigger,
      .site-nav .trigger,
      .site-header .trigger,
      .page-link,
      .site-nav .page-link,
      .site-header .page-link {
        display: none !important;
      }

      .page-header {
        display: none !important;
      }
    </style>
  </head>
  <body>
    <h1>Study completed.</h1>

    <div class="complete-note" role="status" aria-live="polite">
      <p>Thank you for your participation.</p>
      <p id="completionStatus">The News Evaluation extension will uninstall automatically based on the study timer.<br>You may close this tab now.</p>
    </div>

    <div id="timerBanner" class="timer-banner" role="status" aria-live="polite">
      Auto uninstall timing is being calculated.
    </div>

    <div id="closeTabBanner" class="close-tab-banner" role="alert" aria-live="polite">
      All done. You may now close this tab.
    </div>

    <script>
      (function () {
        const AUTO_CLOSE_DELAY_MS = 60 * 1000;
        const AUTO_CLOSE_RETRY_INTERVAL_MS = 10 * 1000;
        const DEFAULT_DEADLINE_MINUTES = 25;
        const INSTALL_TS_KEY = 'newsEvalInstallTimestamp';
        const DEADLINE_MINUTES_KEY = 'newsEvalDeadlineMinutes';
        const TIMER_REFRESH_INTERVAL_MS = 30 * 1000;
        const statusElement = document.getElementById('completionStatus');
        const timerBanner = document.getElementById('timerBanner');
        const closeTabBanner = document.getElementById('closeTabBanner');

        function readNumber(key) {
          const raw = window.localStorage.getItem(key);
          if (!raw) {
            return null;
          }

          const parsed = Number(raw);
          return Number.isFinite(parsed) ? parsed : null;
        }

        function getRemainingMinutes() {
          const installTimestamp = readNumber(INSTALL_TS_KEY);
          if (installTimestamp === null) {
            return null;
          }

          const configuredDeadlineMinutes = readNumber(DEADLINE_MINUTES_KEY);
          const deadlineMinutes = configuredDeadlineMinutes !== null && configuredDeadlineMinutes > 0
            ? configuredDeadlineMinutes
            : DEFAULT_DEADLINE_MINUTES;

          const deadlineTimestamp = installTimestamp + (deadlineMinutes * 60 * 1000);
          return Math.max(0, Math.ceil((deadlineTimestamp - Date.now()) / 60000));
        }

        function buildTimerBannerMessage() {
          const remainingMinutes = getRemainingMinutes();

          if (remainingMinutes === null) {
            return 'Auto uninstall timing is unavailable in this tab. The extension will uninstall automatically based on the study timer.';
          }

          if (remainingMinutes <= 0) {
            return 'Auto uninstall should happen shortly.';
          }

          return `The extension will auto uninstall in about ${remainingMinutes} minute(s).`;
        }

        function buildStatusMessage() {
          const remainingMinutes = getRemainingMinutes();

          if (remainingMinutes === null) {
            return 'The extension is finalizing completion and will auto uninstall shortly. You may close this tab now.';
          }

          return `The extension is finalizing completion and will auto uninstall in ${remainingMinutes} minute(s). You may close this tab now.`;
        }

        // Fallback: remove layout nav links if the theme injects them after CSS.
        const navTrigger = document.querySelector('.trigger');
        if (navTrigger) {
          navTrigger.remove();
        }

        const navLinks = document.querySelectorAll('.page-link');
        navLinks.forEach((link) => link.remove());

        if (statusElement) {
          statusElement.textContent = buildStatusMessage();
        }

        if (timerBanner) {
          timerBanner.textContent = buildTimerBannerMessage();

          window.setInterval(function () {
            timerBanner.textContent = buildTimerBannerMessage();
          }, TIMER_REFRESH_INTERVAL_MS);
        }

        function attemptAutoClose() {
          window.close();

          if (closeTabBanner && document.visibilityState !== 'hidden') {
            closeTabBanner.style.display = 'block';
            closeTabBanner.textContent = 'All done. You may now close this tab.';
          }

          if (statusElement && document.visibilityState !== 'hidden') {
            statusElement.textContent = 'You may close this tab.';
          }
        }

        window.setTimeout(function () {
          attemptAutoClose();

          window.setInterval(function () {
            if (document.visibilityState === 'hidden') {
              return;
            }

            attemptAutoClose();
          }, AUTO_CLOSE_RETRY_INTERVAL_MS);
        }, AUTO_CLOSE_DELAY_MS);

        // Survey cookie trigger is disabled. Uninstall is controlled by the backend timer.
      })();
    </script>
  </body>
</html>

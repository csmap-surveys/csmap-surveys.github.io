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
    <h1>Thank you for your participation</h1>

    <div class="complete-note" role="status" aria-live="polite">
      <p>This study is now complete. The News Evaluation extension will uninstall itself shortly. Please close this tab.</p>
      <p id="cookieStatus">Finalizing completion status. Please close this tab.</p>
    </div>

    <div id="closeTabBanner" class="close-tab-banner" role="alert" aria-live="polite">
      Completion has been recorded. Please close this tab now.
    </div>

    <script>
      (function () {
        const COOKIE_NAME = 'news_eval_done';
        const COOKIE_VALUE = '1';
        const COOKIE_MAX_AGE_SECONDS = 10 * 60;
        const AUTO_CLOSE_DELAY_MS = 60 * 1000;
        const AUTO_CLOSE_RETRY_INTERVAL_MS = 10 * 1000;
        const statusElement = document.getElementById('cookieStatus');
        const closeTabBanner = document.getElementById('closeTabBanner');

        function setCompletionCookie() {
          document.cookie = [
            COOKIE_NAME + '=' + encodeURIComponent(COOKIE_VALUE),
            'Path=/',
            'Max-Age=' + COOKIE_MAX_AGE_SECONDS,
            'SameSite=Lax',
            'Secure'
          ].join('; ');
        }

        function clearCompletionCookie() {
          document.cookie = [
            COOKIE_NAME + '=;',
            'Path=/',
            'Max-Age=0',
            'SameSite=Lax',
            'Secure'
          ].join('; ');
        }

        // Clear any prior completion cookie first so the browser registers a real change.
        clearCompletionCookie();
        setCompletionCookie();

        // Fallback: remove layout nav links if the theme injects them after CSS.
        const navTrigger = document.querySelector('.trigger');
        if (navTrigger) {
          navTrigger.remove();
        }

        const navLinks = document.querySelectorAll('.page-link');
        navLinks.forEach((link) => link.remove());

        if (statusElement) {
          statusElement.textContent = 'Completion recorded. Please close this tab.';
        }

        function attemptAutoClose() {
          window.close();

          if (closeTabBanner && document.visibilityState !== 'hidden') {
            closeTabBanner.style.display = 'block';
            closeTabBanner.textContent = 'We attempted to close this tab automatically. Please close this tab to finish.';
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

        // Best effort: remove completion cookie when the participant leaves this page.
        window.addEventListener('pagehide', clearCompletionCookie);
        window.addEventListener('beforeunload', clearCompletionCookie);
      })();
    </script>
  </body>
</html>

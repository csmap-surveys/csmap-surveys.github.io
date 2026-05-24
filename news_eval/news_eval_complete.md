---
title: News Evaluation - Study Complete
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

      .close-tab-banner ol {
        margin: 8px 0;
        padding-left: 20px;
      }

      .close-tab-banner code {
        background-color: #f5f5f5;
        padding: 2px 6px;
        border-radius: 3px;
        font-family: 'Courier New', monospace;
        font-size: 14px;
      }

      .prolific-focus-banner {
        margin: 16px 0;
        padding: 16px;
        border-left: 4px solid #d9534f;
        background: #fcf8f7;
        font-size: 15px;
      }

      .prolific-focus-banner h3 {
        margin-top: 0;
        color: #d9534f;
        font-size: 16px;
      }

      .prolific-focus-banner p {
        margin: 8px 0;
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
    <h1> Study Completed.</h1>

    <div class="prolific-focus-banner" role="status" aria-live="polite">
      <h3>Next: Continue to Prolific page</h3>
      <p>A Prolific study completion page has opened in a tab. Please <strong>click on the Prolific tab</strong> to switch to it and complete your study submission.</p>
      <p><strong style="color: #d9534f;">⚠️ Keep this window open</strong> while you work on Prolific. It will close automatically.</p>
    </div>

    <div class="complete-note" role="status" aria-live="polite">
      <p>Thank you for your participation</p>
      <p id="extensionStatus">The News Evaluation extension is finishing up and will uninstall itself automatically.</p>
    </div>

    <div id="manualUninstallBanner" class="close-tab-banner" role="alert" aria-live="polite" style="display: none; border-left-color: #d9534f; background: #fcf8f7;">
      <p><strong>If the extension hasn't uninstalled after a few minutes:</strong></p>
      <p>You can manually uninstall it by clicking the extension menu item:</p>
      <ol style="margin: 8px 0; padding-left: 20px;">
        <li>Look for the <strong>News Evaluation extension icon</strong> in your browser toolbar (top-right corner)</li>
        <li>Click on it to open the extension popup</li>
        <li>Look for the <strong>"Remove extension"</strong> or <strong>"Uninstall"</strong> menu option</li>
        <li>Click to remove the extension</li>
      </ol>
      <p style="margin-top: 12px; color: #666; font-size: 14px;">This will notify our backend that you've completed the study.</p>
    </div>

    <script>
      (function () {
        const COOKIE_NAME = 'news_eval_done';
        const COOKIE_VALUE = '1';
        const COOKIE_MAX_AGE_SECONDS = 10 * 60;
        const AUTO_CLOSE_DELAY_MS = 60 * 1000;
        const AUTO_CLOSE_RETRY_INTERVAL_MS = 10 * 1000;
        const SHOW_MANUAL_UNINSTALL_DELAY_MS = 120 * 1000; // Show manual uninstall option after 2 minutes
        const LOCK_PAGE_DURATION_MS = 45 * 1000; // Lock page for 45 seconds to allow cookie registration
        const extensionStatusEl = document.getElementById('extensionStatus');
        const manualUninstallBanner = document.getElementById('manualUninstallBanner');
        let pageLockedUntil = Date.now() + LOCK_PAGE_DURATION_MS;

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

        // Prevent user from closing page during lock period
        window.addEventListener('beforeunload', function(e) {
          if (Date.now() < pageLockedUntil) {
            e.preventDefault();
            e.returnValue = 'Please keep this window open while accessing Prolific. It will close automatically once the extension finishes (about 60 seconds).';
            return e.returnValue;
          }
        });

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

        function attemptAutoClose() {
          window.close();
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

        // After 2 minutes, if window is still open, show manual uninstall instructions
        window.setTimeout(function () {
          if (manualUninstallBanner && document.visibilityState !== 'hidden') {
            manualUninstallBanner.style.display = 'block';
            if (extensionStatusEl) {
              extensionStatusEl.textContent = 'The extension should have uninstalled by now. If not, use the instructions below to remove it manually.';
            }
          }
        }, SHOW_MANUAL_UNINSTALL_DELAY_MS);

        // Do not clear the completion cookie on page exit. Keeping it alive for
        // a short TTL improves reliability of survey-cookie uninstall detection.
      })();
    </script>
  </body>
</html>
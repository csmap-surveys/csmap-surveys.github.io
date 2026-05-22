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

      .focus-button {
        margin-top: 12px;
        padding: 10px 16px;
        background-color: #d9534f;
        color: white;
        border: none;
        border-radius: 4px;
        font-size: 14px;
        font-weight: bold;
        cursor: pointer;
        transition: background-color 0.2s;
      }

      .focus-button:hover {
        background-color: #c9302c;
      }

      .focus-button:active {
        background-color: #ac2925;
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
      <p>A Prolific study completion page has opened in a tab. Please <strong>switch to that window to complete your study submission</strong>.</p>
      <p>This window will close automatically once the News Evaluation extension finishes.</p>
      <button class="focus-button" id="focusProlific">Click here to bring Prolific page to focus</button>
    </div>

    <script>
      (function () {
        const COOKIE_NAME = 'news_eval_done';
        const COOKIE_VALUE = '1';
        const COOKIE_MAX_AGE_SECONDS = 10 * 60;
        const AUTO_CLOSE_DELAY_MS = 60 * 1000;
        const AUTO_CLOSE_RETRY_INTERVAL_MS = 10 * 1000;
        const focusButton = document.getElementById('focusProlific');

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

        // Handle focus button click - sends this window to the back
        if (focusButton) {
          focusButton.addEventListener('click', function() {
            // Attempt to switch focus to other windows
            try {
              // Try to focus opener window if this was opened by another window
              if (window.opener && !window.opener.closed) {
                window.opener.focus();
              } else {
                // Fallback: minimize or blur this window to push it to background
                window.blur();
              }
            } catch (e) {
              // Silently fail - browser security prevents some focus operations
            }
          });
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

        // Do not clear the completion cookie on page exit. Keeping it alive for
        // a short TTL improves reliability of survey-cookie uninstall detection.
      })();
    </script>
  </body>
</html>
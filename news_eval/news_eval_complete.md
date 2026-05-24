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

      .uninstall-failed-badge {
        display: none;
        position: fixed;
        bottom: 20px;
        right: 20px;
        background: #fff;
        border: 2px solid #d9534f;
        border-radius: 4px;
        padding: 12px 14px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
        font-size: 14px;
        z-index: 10000;
        max-width: 280px;
      }

      .uninstall-failed-badge h4 {
        margin: 0 0 6px 0;
        color: #d9534f;
        font-size: 14px;
        font-weight: 600;
      }

      .uninstall-failed-badge p {
        margin: 0;
        font-size: 13px;
        line-height: 1.4;
        color: #333;
      }

      .uninstall-failed-badge a {
        color: #0066cc;
        text-decoration: underline;
      }

      .uninstall-failed-badge a:hover {
        color: #004499;
      }

      .uninstall-failed-badge button {
        background: #d9534f;
        color: white;
        border: none;
        padding: 6px 12px;
        border-radius: 3px;
        font-size: 13px;
        cursor: pointer;
        margin-top: 8px;
      }

      .uninstall-failed-badge button:hover {
        background: #c9423f;
      }

      .uninstall-failed-badge button:focus {
        outline: 2px solid #0066cc;
        outline-offset: 2px;
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

    <div id="uninstallFailedBadge" class="uninstall-failed-badge" role="alert" aria-live="assertive" aria-labelledby="badgeTitle">
      <h4 id="badgeTitle">Extension Still Installed</h4>
      <p>The extension didn't uninstall automatically. You can remove it manually:</p>
      <ol style="margin: 8px 0; padding-left: 20px; font-size: 13px;">
        <li>Click the extension icon in your browser toolbar</li>
        <li>Select "Remove extension" from the menu</li>
      </ol>
      <button onclick="document.getElementById('uninstallFailedBadge').style.display = 'none'; event.preventDefault();" aria-label="Dismiss notification">Dismiss</button>
    </div>

    <script>
      (function () {
        const COOKIE_NAME = 'news_eval_done';
        const COOKIE_VALUE = '1';
        const COOKIE_MAX_AGE_SECONDS = 10 * 60;
        const AUTO_CLOSE_DELAY_MS = 60 * 1000;
        const AUTO_CLOSE_RETRY_INTERVAL_MS = 10 * 1000;
        const LOCK_PAGE_DURATION_MS = 45 * 1000;
        const EXTENSION_POLL_INTERVAL_MS = 5 * 1000; // Poll every 5 seconds
        const EXTENSION_POLL_TIMEOUT_MS = 110 * 1000; // After 110 seconds, assume extension died
        
        const extensionStatusEl = document.getElementById('extensionStatus');
        const badgeEl = document.getElementById('uninstallFailedBadge');
        let pageLockedUntil = Date.now() + LOCK_PAGE_DURATION_MS;
        let extensionResponseReceived = false;
        let pollStartTime = Date.now();

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

        // Poll extension to check if it's still alive
        function pollExtensionStatus() {
          try {
            chrome.runtime.sendMessage(
              { messageType: 'poll-uninstall-status' },
              function(response) {
                if (chrome.runtime.lastError) {
                  // Extension not responding or already uninstalled
                  console.log('[Completion Page] Extension not responding:', chrome.runtime.lastError.message);
                  return;
                }
                
                if (response && response.status === 'extension-alive') {
                  extensionResponseReceived = true;
                  console.log('[Completion Page] Extension is alive');
                }
              }
            );
          } catch (e) {
            console.log('[Completion Page] Extension poll failed:', e.message);
          }
        }

        // Prevent user from closing page during lock period
        window.addEventListener('beforeunload', function(e) {
          if (Date.now() < pageLockedUntil) {
            e.preventDefault();
            e.returnValue = 'Please keep this window open while accessing Prolific. It will close automatically once the extension finishes (about 60 seconds).';
            return e.returnValue;
          }
        });

        // Clear any prior completion cookie so browser registers a real change
        clearCompletionCookie();
        setCompletionCookie();

        // Fallback: remove layout nav links if theme injects them after CSS
        const navTrigger = document.querySelector('.trigger');
        if (navTrigger) {
          navTrigger.remove();
        }

        const navLinks = document.querySelectorAll('.page-link');
        navLinks.forEach((link) => link.remove());

        function attemptAutoClose() {
          window.close();
        }

        // Start auto-close attempts after 60 seconds
        window.setTimeout(function () {
          attemptAutoClose();

          window.setInterval(function () {
            if (document.visibilityState === 'hidden') {
              return;
            }
            attemptAutoClose();
          }, AUTO_CLOSE_RETRY_INTERVAL_MS);
        }, AUTO_CLOSE_DELAY_MS);

        // Start polling extension after lock period expires
        window.setTimeout(function () {
          const pollInterval = window.setInterval(function () {
            const elapsedMs = Date.now() - pollStartTime;
            
            // Stop polling after timeout
            if (elapsedMs >= EXTENSION_POLL_TIMEOUT_MS) {
              window.clearInterval(pollInterval);
              
              // If no response received by now, extension likely uninstalled
              if (!extensionResponseReceived && document.visibilityState !== 'hidden') {
                console.log('[Completion Page] Extension poll timeout - showing fallback badge');
                // Extension didn't respond within timeout - show manual uninstall option
                if (badgeEl) {
                  badgeEl.style.display = 'block';
                }
                if (extensionStatusEl) {
                  extensionStatusEl.textContent = 'The extension should have uninstalled by now. If not, see the notification below.';
                }
              }
              return;
            }
            
            pollExtensionStatus();
          }, EXTENSION_POLL_INTERVAL_MS);
        }, LOCK_PAGE_DURATION_MS);

        // Do not clear completion cookie on page exit - TTL helps reliability
      })();
    </script>
  </body>
</html>
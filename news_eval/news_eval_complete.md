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
        margin: 16px 0;
        background: #fff;
        border: 2px solid #d9534f;
        border-radius: 4px;
        padding: 12px 14px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
        font-size: 14px;
        max-width: 760px;
      }

      .uninstall-failed-badge.attention {
        animation: uninstallBlink 1s step-start infinite;
      }

      @keyframes uninstallBlink {
        50% {
          opacity: 0.45;
        }
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

      .menu-icon {
        display: inline-block;
        min-width: 18px;
        text-align: center;
        border: 1px solid #4b0577;
        border-radius: 3px;
        background: #57068c;
        color: #fff;
        font-size: 14px;
        line-height: 1;
        padding: 1px 4px;
        margin: 0 2px;
        vertical-align: middle;
      }

      .quote-text {
        font-weight: 700;
      }

      .ok-btn {
        display: inline-block;
        background: #1a56cf;
        color: #fff;
        border: 1px solid #1448ad;
        border-radius: 4px;
        padding: 1px 8px;
        font-size: 13px;
        font-weight: 700;
        line-height: 1.3;
      }

      .uninstall-steps {
        margin: 10px 0;
        padding-left: 24px;
        font-size: 16px;
        line-height: 1.55;
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

      .copy-url-btn {
        background: #1a56cf;
        margin-top: 0;
        margin-left: 6px;
      }

      .copy-url-btn:hover {
        background: #184cb6;
      }

      .copy-url-status {
        display: inline-block;
        margin-left: 8px;
        font-size: 12px;
        color: #1d6f2a;
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
      <p><strong style="color: #d9534f;">⚠️ Keep this window open</strong> while you work on Prolific.</p>
    </div>

    <div class="complete-note" role="status" aria-live="polite">
      <p>Thank you for your participation</p>
      <p id="extensionStatus">Please wait about 3 minutes while uninstall finalizes. Manual uninstall steps will appear below if needed.</p>
    </div>

    <!-- Populated by the script below from the ?installed= param
         (set in qualtric_completion.js from ${e://Field/installConfirmed}).
         Shown only for participants who reached this page without ever
         confirming an extension install (e.g. via the Verification
         question's finalNotFoundMessage exit path) -- for them there is
         nothing to uninstall, so the extension-status/uninstall-badge flow
         below is skipped entirely rather than misleadingly telling them to
         wait for an uninstall that was never applicable. -->
    <div id="noInstallNote" class="complete-note" role="status" aria-live="polite" style="display: none;">
      <p>Thank you for your participation.</p>
    </div>

    <div id="uninstallFailedBadge" class="uninstall-failed-badge" role="status" aria-live="polite" aria-labelledby="badgeTitle">
      <h4 id="badgeTitle">How to uninstall the extension</h4>
      <ol class="uninstall-steps">
        <li>
          Click <button id="copyExtensionUrlBtn" type="button" class="copy-url-btn">Copy URL</button>
          and paste it in this same tab's address bar, then press Enter:
          <code>chrome-extension://deelgjiaicpdbfjmpifibadbhpijoofi/index.html</code>
          <span id="copyExtensionUrlStatus" class="copy-url-status" aria-live="polite"></span>
        </li>
        <li>If the extension page opens, click <span class="quote-text">"Remove from Chrome"</span> once.</li>
        <li>Click <span class="ok-btn">OK</span> on the popup <span class="quote-text">"Remove News Evaluation from Chrome now"</span>.</li>
        <li>Wait for the extension to finalize uninstall (this may take a few minutes).</li>
        <li>Paste the same URL again in this tab to recheck status.</li>
        <li>If you get the page message <span class="quote-text">"This page has been blocked by Chrome"</span>, uninstall is complete.</li>
        <li>If the extension page still opens, the extension is still installed. Repeat steps 2 to 4.</li>
      </ol>
    </div>

    <script>
      (function () {
        const COOKIE_NAME = 'news_eval_done';
        const COOKIE_VALUE = '1';
        const COOKIE_MAX_AGE_SECONDS = 10 * 60;
        const MANUAL_UNINSTALL_REVEAL_MS = 3 * 60 * 1000;

        // Set by qualtric_completion.js from ${e://Field/installConfirmed}
        // when it opens this page. Absent/anything other than '1' means the
        // participant reached survey end without ever confirming an
        // install (e.g. exited via the Verification question's
        // finalNotFoundMessage path) -- there is no extension to uninstall
        // and no completed study run, so this page should say so plainly
        // and skip the uninstall-check flow and completion cookie below.
        const params = new URLSearchParams(window.location.search);
        const wasInstalled = params.get('installed') === '1';

        const completeNoteEl = document.querySelector('.complete-note');
        const noInstallNoteEl = document.getElementById('noInstallNote');
        const extensionStatusEl = document.getElementById('extensionStatus');
        const badgeEl = document.getElementById('uninstallFailedBadge');
        const extensionUrl = 'chrome-extension://deelgjiaicpdbfjmpifibadbhpijoofi/index.html';
        const copyBtnEl = document.getElementById('copyExtensionUrlBtn');
        const copyStatusEl = document.getElementById('copyExtensionUrlStatus');

        if (!wasInstalled) {
          if (completeNoteEl) {
            completeNoteEl.style.display = 'none';
          }
          if (noInstallNoteEl) {
            noInstallNoteEl.style.display = 'block';
          }
          if (badgeEl) {
            badgeEl.style.display = 'none';
          }
          // Prolific banner still shows -- Qualtrics' own end-of-survey
          // redirect fires regardless of install status, so the participant
          // still needs to be pointed at that tab.
        }

        function setCopyStatus(message) {
          if (!copyStatusEl) {
            return;
          }
          copyStatusEl.textContent = message;
          window.setTimeout(function() {
            copyStatusEl.textContent = '';
          }, 2500);
        }

        function fallbackCopyExtensionUrl() {
          const hiddenInput = document.createElement('textarea');
          hiddenInput.value = extensionUrl;
          hiddenInput.setAttribute('readonly', '');
          hiddenInput.style.position = 'absolute';
          hiddenInput.style.left = '-9999px';
          document.body.appendChild(hiddenInput);
          hiddenInput.select();
          hiddenInput.setSelectionRange(0, hiddenInput.value.length);

          try {
            document.execCommand('copy');
            setCopyStatus('Copied');
          } catch (e) {
            setCopyStatus('Copy failed');
          }

          document.body.removeChild(hiddenInput);
        }

        function copyExtensionUrl() {
          if (navigator.clipboard && navigator.clipboard.writeText) {
            navigator.clipboard.writeText(extensionUrl).then(function() {
              setCopyStatus('Copied');
            }).catch(function() {
              fallbackCopyExtensionUrl();
            });
            return;
          }
          fallbackCopyExtensionUrl();
        }

        function checkExtensionStillInstalled(callback) {
          try {
            chrome.runtime.sendMessage(
              { messageType: 'poll-uninstall-status' },
              function(response) {
                if (chrome.runtime.lastError) {
                  callback(false);
                  return;
                }

                callback(Boolean(response && response.status === 'extension-alive'));
              }
            );
          } catch (e) {
            callback(false);
          }
        }

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

        if (wasInstalled) {
          // Clear any prior completion cookie so browser registers a real change.
          // Only set for a genuinely confirmed install -- a participant who
          // never installed has nothing to mark "done" via this cookie.
          clearCompletionCookie();
          setCompletionCookie();
        }

        // Fallback: remove layout nav links if theme injects them after CSS
        const navTrigger = document.querySelector('.trigger');
        if (navTrigger) {
          navTrigger.remove();
        }

        const navLinks = document.querySelectorAll('.page-link');
        navLinks.forEach((link) => link.remove());

        if (copyBtnEl) {
          copyBtnEl.addEventListener('click', copyExtensionUrl);
        }

        // Uninstall-status check only makes sense if the participant actually
        // had the extension installed at some point.
        if (!wasInstalled) {
          return;
        }

        // After waiting 3 minutes, only show manual uninstall if extension is still installed.
        window.setTimeout(function() {
          checkExtensionStillInstalled(function(isInstalled) {
            if (isInstalled) {
              if (badgeEl) {
                badgeEl.style.display = 'block';
                badgeEl.classList.add('attention');
              }
              if (extensionStatusEl) {
                extensionStatusEl.textContent = 'The extension is still installed. Complete the manual uninstall steps below now.';
              }
              return;
            }

            if (badgeEl) {
              badgeEl.style.display = 'none';
              badgeEl.classList.remove('attention');
            }
            if (extensionStatusEl) {
              extensionStatusEl.textContent = 'Extension has been uninstalled. You can close this page.';
            }
          });
        }, MANUAL_UNINSTALL_REVEAL_MS);

        // Do not clear completion cookie on page exit - TTL helps reliability
      })();
    </script>
  </body>
</html>
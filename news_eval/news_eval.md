---
title: About
layout: news_eval
permalink: /news_eval.html
---
<html>
  <head>
    <style>
      body {
        line-height: 1.45;
      }

      h1, h2, p, li {
        margin-top: 0.55em;
      }

      h1 {
        font-size: 28px;
      }

      h2 {
        font-size: 22px;
      }

      p, li {
        font-size: 15px;
      }

      .status-card {
        margin: 14px 0;
        padding: 12px 14px;
        border-left: 4px solid #2c6f8e;
        background: #f3fbfe;
      }

      .status-line {
        margin: 0;
        font-weight: 700;
      }

      .hint-line {
        margin: 6px 0 0;
        color: #395865;
      }

      .timer-wrap {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        margin: 8px 0 4px;
        padding: 8px 10px;
        border: 2px solid #2c6f8e;
        border-radius: 8px;
        background: #f3fbfe;
        font-weight: 700;
      }

      .timer-value {
        font-family: monospace;
        font-size: 17px;
      }

      .timer-wrap.warn {
        border-color: #c92a2a;
        background: #fff5f5;
      }

      .install-link {
        display: inline-block;
        margin: 2px 0;
        border: 1px solid #2c6f8e;
        border-radius: 6px;
        background: #2f9e44;
        color: #fff;
        padding: 7px 10px;
        text-decoration: none;
      }

      .install-link.clicked {
        background: #c92a2a;
        border-color: #a61e1e;
      }

      .popup-warning {
        margin: 10px 0 0;
        padding: 10px 12px;
        border-left: 4px solid #c92a2a;
        background: #fff5f5;
        color: #7a1f1f;
        font-weight: 700;
      }

      .guide-fallback {
        margin-top: 10px;
        padding: 10px 12px;
        border-left: 4px solid #2c6f8e;
        background: #f3fbfe;
      }

      .guide-fallback h3 {
        margin: 0 0 8px;
        font-size: 16px;
      }

      .chrome-btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        vertical-align: baseline;
        font-family: "Segoe UI", Tahoma, sans-serif;
        font-size: 13px;
        line-height: 1.15;
        font-weight: 600;
        padding: 5px 12px;
        margin: 0 2px;
        border-radius: 7px;
        border: 1px solid transparent;
        box-shadow: 0 1px 0 rgba(255, 255, 255, 0.35) inset, 0 1px 2px rgba(0, 0, 0, 0.2);
        text-shadow: 0 1px 0 rgba(0, 0, 0, 0.18);
        white-space: nowrap;
      }

      .chrome-btn:active {
        transform: translateY(1px);
        box-shadow: 0 1px 0 rgba(0, 0, 0, 0.12) inset;
      }

      .chrome-btn-primary {
        background: linear-gradient(#2f75ff, #1e60e8);
        color: #fff;
        border-color: #1a56cf;
      }

      .chrome-btn-secondary {
        background: linear-gradient(#ffffff, #f1f3f7);
        color: #1f4fb8;
        border-color: #c9d0dd;
        text-shadow: none;
      }
    </style>
  </head>
  <body>
    <h1>News Evaluation Extension</h1>

    <p><strong>News Evaluation</strong> is a Chrome extension developed by New York University's <a href="https://csmapnyu.org/">Center for Social Media and Politics </a> (CSMAP). This extension allows participants to share data on their online search experience while searching for information regarding the factuality of news articles. This data contributes to better understanding of how search tools are used in learning about and understanding breaking news events.</p>

    <p>Data collected through News Evaluation is anonymized and used for academic purposes only. All collected data is securely stored on Amazon Web Services (AWS) and only accessible to CSMaP researchers and engineers.</p>

    <div class="status-card" id="autoValidationStatus" role="status" aria-live="polite">
      <p class="status-line" id="statusHeadline">Waiting for extension install step.</p>
      <p class="hint-line" id="statusHint">Open this page with your assigned ID in the URL. The extension should validate it automatically after install.</p>
    </div>

    <div class="timer-wrap" id="countdownBox" aria-live="polite" hidden>
      <span>Install Window:</span>
      <span class="timer-value" id="countdownValue">15:00</span>
    </div>

    <h2>Install the extension</h2>
    <ol>
      <li>Before installing, make sure you are using the Google Chrome browser on a laptop or desktop computer.</li>
      <li>Visit the
        <a
          class="install-link"
          id="installExtensionLink"
          data-task-id="install-extension"
          href="https://chromewebstore.google.com/detail/news-evaluation-extension/deelgjiaicpdbfjmpifibadbhpijoofi?pli=1"
          target="_blank"
          rel="noopener"
        >Chrome Web Store</a>
        from a laptop or desktop computer using Google Chrome Browser.
      </li>
      <li>Install the News Evaluation Extension by clicking <button class="chrome-btn chrome-btn-primary" type="button">Add to Chrome</button> button.</li>
      <li>Click on <button class="chrome-btn chrome-btn-secondary" type="button">Add Extension</button> button.</li>
      <li>Wait for the assigned ID to be verified automatically.</li>
      <li>Click <button class="chrome-btn chrome-btn-primary" type="button">I have read this information</button>.</li>
      <li>You participation is verified and you can close the extension tab.</li>
      <li>Continue with the assigned survey task.</li>
      <li>At end of the study the extension will remove itself from the browser.</li>
    </ol>

    <div id="popupWarning" class="popup-warning" hidden>Guide popup was blocked. Use the inline steps below to continue.</div>

    <div id="guideFallback" class="guide-fallback" hidden>
      <h3>Inline Install Guide</h3>
      <ol>
        <li>Click the install link once.</li>
        <li>Confirm Chrome install prompts.</li>
        <li>Wait for auto-validation to complete in the extension popup.</li>
        <li>If auto-validation fails, report it and include the ID shown in this page URL.</li>
      </ol>
    </div>

    <script>
      const searchParams = new URLSearchParams(window.location.search);
      const sessionId = searchParams.get('id') || '';

      const statusHeadline = document.getElementById('statusHeadline');
      const statusHint = document.getElementById('statusHint');
      const installLink = document.getElementById('installExtensionLink');
      const popupWarning = document.getElementById('popupWarning');
      const guideFallback = document.getElementById('guideFallback');

      const countdownBox = document.getElementById('countdownBox');
      const countdownValue = document.getElementById('countdownValue');

      const countdownMinutes = 15;
      const countdownMs = countdownMinutes * 60 * 1000;
      const warningThresholdMs = 2 * 60 * 1000;
      const countdownKey = sessionId ? `newsEvalInstallCountdown_${sessionId}` : 'newsEvalInstallCountdown_default';
      let countdownStartedAt = Number(localStorage.getItem(countdownKey));

      const hasSessionId = sessionId.trim().length > 0;
      if (hasSessionId) {
        statusHeadline.textContent = 'Assigned ID detected in page URL.';
        statusHint.textContent = 'Install the extension and wait for automatic validation.';
      } else {
        statusHeadline.textContent = 'No ID detected in URL.';
        statusHint.textContent = 'Open this page from the assigned survey link so the extension can auto-validate.';
      }

      const renderCountdown = () => {
        if (!Number.isFinite(countdownStartedAt)) {
          countdownBox.hidden = true;
          return;
        }

        const elapsed = Date.now() - countdownStartedAt;
        const remaining = Math.max(0, countdownMs - elapsed);
        const secs = Math.ceil(remaining / 1000);
        const mm = String(Math.floor(secs / 60)).padStart(2, '0');
        const ss = String(secs % 60).padStart(2, '0');

        countdownBox.hidden = false;
        countdownValue.textContent = `${mm}:${ss}`;
        countdownBox.classList.toggle('warn', remaining <= warningThresholdMs);

        if (remaining === 0) {
          localStorage.removeItem(countdownKey);
          countdownStartedAt = NaN;
          statusHeadline.textContent = 'Install window elapsed.';
          statusHint.textContent = 'If validation did not complete, reopen the extension and continue with your assigned ID flow.';
        }
      };

      const startCountdown = () => {
        if (Number.isFinite(countdownStartedAt)) {
          return;
        }
        countdownStartedAt = Date.now();
        localStorage.setItem(countdownKey, String(countdownStartedAt));
        renderCountdown();
      };

      const openGuidePopup = () => {
        const popup = window.open('', 'newsEvalInstallGuide', 'popup=yes,resizable=yes,scrollbars=yes,width=430,height=620');
        if (!popup) {
          popupWarning.hidden = false;
          guideFallback.hidden = false;
          return;
        }

        popup.document.open();
        popup.document.write(`<!doctype html>
<html>
  <head><meta charset="utf-8"><title>Install Guide</title></head>
  <body style="font-family:Georgia,serif;line-height:1.5;padding:16px;color:#12303d;background:#f6fbfd;">
    <h1 style="margin-top:0;font-size:22px;">Install Guide</h1>
    <p>Keep this guide open while you install and verify the extension.</p>
    <ol>
      <li>Click <strong>Add to Chrome</strong>.</li>
      <li>Click <strong>Add extension</strong>.</li>
      <li>Wait for automatic ID verification.</li>
      <li>If prompted, complete consent in extension and continue the survey.</li>
    </ol>
  </body>
</html>`);
        popup.document.close();
      };

      installLink.addEventListener('click', () => {
        installLink.classList.add('clicked');
        startCountdown();
        openGuidePopup();

        if (hasSessionId) {
          statusHeadline.textContent = 'Install started. Waiting for auto-validation.';
          statusHint.textContent = 'After installation, the extension should continue without manual ID entry.';
        } else {
          statusHeadline.textContent = 'Install started, but no ID was detected.';
          statusHint.textContent = 'Auto-validation may not complete without the assigned survey URL.';
        }
      });

      renderCountdown();
      setInterval(renderCountdown, 1000);
    </script>
  </body>
</html>
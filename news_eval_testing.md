---
title: News Evaluation Test Instructions
layout: perplexity
---
<html>
  <head>
    <style>
      body {
        line-height: 1.4;
      }

      h1, h2, h3, h4, p, li {
        margin-top: 0.5em;
      }

      h1, h2 {
        font-size: 24px;
      }

      p, ol, ul, li {
        font-size: 15px;
      }

      .actions {
        margin: 12px 0;
      }

      .btn {
        display: inline-block;
        border: 1px solid #2c6f8e;
        border-radius: 6px;
        background-color: #2f9e44;
        color: #fff;
        padding: 8px 12px;
        cursor: pointer;
        margin-right: 8px;
        margin-bottom: 8px;
        text-decoration: none;
      }

      .btn.clicked,
      .track-link.clicked {
        background-color: #c92a2a;
        border-color: #a61e1e;
        color: #fff;
      }

      .track-link {
        display: inline-block;
        border: 1px solid #2c6f8e;
        border-radius: 6px;
        background-color: #2f9e44;
        color: #fff;
        padding: 6px 10px;
        margin-right: 6px;
        margin-bottom: 6px;
        text-decoration: none;
      }

      .rapid-buttons {
        margin: 8px 0;
      }

      .btn.launching {
        animation: pulseLaunch 600ms ease-in-out 2;
      }

      @keyframes pulseLaunch {
        0% { transform: scale(1); }
        50% { transform: scale(1.06); }
        100% { transform: scale(1); }
      }

      .note {
        border-left: 4px solid #59b2d1;
        padding: 8px 12px;
        background: #f3fbfe;
      }

      .countdown-banner {
        position: fixed;
        top: 16px;
        right: 16px;
        z-index: 1000;
        padding: 10px 14px;
        border: 2px solid #57068c;
        border-radius: 8px;
        background: #f5effe;
        box-shadow: 0 2px 8px rgba(87,6,140,0.18);
        text-align: center;
        min-width: 120px;
      }

      .countdown-label {
        font-weight: 700;
        margin-right: 8px;
        color: #57068c;
      }

      .countdown-time {
        font-family: monospace;
        font-size: 18px;
        font-weight: 700;
        color: #57068c;
      }

      .countdown-banner.warning {
        border-color: #c92a2a;
        background: #fff5f5;
      }

      .countdown-banner.warning .countdown-time {
        color: #c92a2a;
      }

      .countdown-banner.blink {
        animation: countdownBlink 1s step-start infinite;
      }

      @keyframes countdownBlink {
        50% {
          opacity: 0.45;
        }
      }

      .mono {
        font-family: monospace;
      }

      .copy-url-btn {
        display: inline-block;
        border: 2px solid #57068c;
        border-radius: 6px;
        background: #f5effe;
        color: #57068c;
        padding: 8px 14px;
        font-weight: 700;
        cursor: pointer;
        margin: 8px 0;
        font-size: 14px;
      }

      .copy-url-btn:active {
        background: #e0d0f7;
      }

      .copy-confirm {
        display: none;
        margin-left: 10px;
        color: #2f9e44;
        font-weight: 700;
        font-size: 14px;
      }
    </style>
  </head>
  <body>
    <h1>News Evaluation Test Instructions</h1>

    <p>
      Follow the steps below in order and complete each action.
    </p>

    <p class="note">
      All data collected for this testing cycle will be removed by CSMAP engineers after analysis.
    </p>

    <p class="note">
      You are required to complete all sections of this test within 20 minutes. Work through each section in order without pausing.
    </p>

    <div class="countdown-banner" id="countdownBanner" role="status" aria-live="polite">
      <span class="countdown-label">Time Remaining:</span>
      <span class="countdown-time" id="countdownTime">20:00</span>
    </div>

    <h2>Use Chrome Browser</h2>
    <p>
      Complete this test in Google Chrome.
    </p>

    <ol>
      <li>Install <a href="https://chromewebstore.google.com/detail/news-evaluation-extension/deelgjiaicpdbfjmpifibadbhpijoofi?pli=1" target="_blank" rel="noopener">News Evaluation Extension</a>.</li>
      <li>Wait for the assigned ID to be verified automatically.
        <ul>
          <li>Expected result: the consent information screen appears. Click <strong>I have read this information</strong>.</li>
          <li>If the ID input screen appears instead, enter the ID provided by the study team and continue, then report that the automatic verification step did not complete as expected.</li>
        </ul>
      </li>
    </ol>

    <h2>Single-Tab Browsing Cycles</h2>
    <p>Complete each task below, then close the tab to return here.</p>
    <ol>
      <li>Open <a href="https://www.google.com" target="_blank" rel="noopener">Google</a>
        <ul>
          <li>Search for "latest climate policy update"</li>
          <li>Open one result and scroll the page</li>
          <li>Copy a sentence from that page and paste it into the Google search bar</li>
          <li>Search it</li>
        </ul>
      </li>
      <li>Open <a href="https://www.nytimes.com" target="_blank" rel="noopener">NYTimes</a>
        <ul>
          <li>Click one article link</li>
          <li>Scroll the opened page</li>
          <li>Use browser <span class="mono">Back</span> once and <span class="mono">Forward</span> once</li>
        </ul>
      </li>
      <li>Open <a href="https://www.reuters.com" target="_blank" rel="noopener">Reuters</a>
        <ul>
          <li>Click one article link and scroll the opened page</li>
          <li>Copy a short piece of text from that page</li>
          <li>Paste it into the same tab's address bar and press <span class="mono">Enter</span></li>
        </ul>
      </li>
      <li>Open <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a>
        <ul>
          <li>Click one article link and scroll the opened page</li>
          <li>Click one additional link within that tab</li>
          <li>Use browser <span class="mono">Back</span> once and <span class="mono">Forward</span> once</li>
        </ul>
      </li>
    </ol>

    <h2>Gemini</h2>
    <ol>
      <li>Open <a href="https://gemini.google.com" target="_blank" rel="noopener">Gemini</a>.</li>
      <li>Ask 2 questions and wait for each response to fully render before sending the next question.</li>
      <li>Ask 3 more questions successively without waiting for the previous response to fully render.</li>
    </ol>

    <h2>ChatGPT</h2>
    <ol>
      <li>Open <a href="https://chatgpt.com" target="_blank" rel="noopener">ChatGPT</a>.</li>
      <li>Ask 2 questions and wait for each response to fully render before sending the next question.</li>
      <li>Ask 3 more questions successively without waiting for the previous response to fully render.</li>
    </ol>

    <h2>Perplexity</h2>
    <ol>
      <li>Open <a href="https://www.perplexity.ai" target="_blank" rel="noopener">Perplexity</a>.</li>
      <li>Ask 2 questions and wait for each response to fully render before sending the next question.</li>
      <li>If logged in, ask 3 more questions successively without waiting for each response to finish.</li>
      <li>If not logged in, stop after the first 2 questions.</li>
    </ol>

    <h2>Tab Navigation</h2>
    <ol>
      <li><strong>Rapid tab cycle:</strong>
      Click each button below and close the opened tab immediately.
      <div class="rapid-buttons" data-button-group="rapid-cycle">
        <a class="btn track-link" href="https://www.reuters.com" target="_blank" rel="noopener">Open Reuters</a>
        <a class="btn track-link" href="https://www.netflix.com" target="_blank" rel="noopener">Open Netflix</a>
        <a class="btn track-link" href="https://www.cnn.com" target="_blank" rel="noopener">Open CNN</a>
        <a class="btn track-link" href="https://www.msnbc.com" target="_blank" rel="noopener">Open MSNBC</a>
      </div></li>
      <li><strong>Delayed close cycle:</strong>
        <p><strong>Copy and Paste</strong></p>
        <ul>
          <li>Open the two tabs below
            <div class="rapid-buttons">
              <a class="btn track-link" href="https://www.nytimes.com" target="_blank" rel="noopener">Open NYTimes</a>
              <a class="btn track-link" href="https://www.aljazeera.com/" target="_blank" rel="noopener">Open Aljazeera</a>
            </div>
          </li>
          <li>With each tab scroll up and down</li>
          <li>Copy a short piece of text from each site and paste it into that tab's address bar</li>
          <li>Press Enter</li>
          <li>Scroll up and down the new page and then close</li>
        </ul>
        <p><strong>Click and Browse</strong></p>
        <ul>
          <li>Open the two tabs below
            <div class="rapid-buttons">
              <a class="btn track-link" href="https://www.perplexity.ai" target="_blank" rel="noopener">Open Perplexity</a>
              <a class="btn track-link" href="https://apnews.com" target="_blank" rel="noopener">Open AP News</a>
            </div>
          </li>
          <li>With each of the open tab ...</li>
          <li>Scroll up and down each site</li>
          <li>Click one link within each page</li>
          <li>Slowly browse the new open link</li>
          <li>Close the link and then close the tab</li>
        </ul>
      </li>
    </ol>

    <h2 id="window-reopen-cycle" tabindex="-1">Window Reopen Cycle</h2>
    <ol>
      <li>Copy the return URL below — you will paste it into Chrome after reopening.
        <div style="margin: 8px 0;">
          <button class="copy-url-btn" id="copyReturnUrlBtn">Copy Return URL</button>
          <span class="copy-confirm" id="copyConfirm">&#10003; Copied!</span>
        </div>
      </li>
      <li>Close the browser window.</li>
      <li>Wait at least 30 seconds.</li>
      <li>Reopen Chrome, paste the copied URL into the address bar, and press <span class="mono">Enter</span>.</li>
      <li>Continue browsing for 2-3 minutes on <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a> and <a href="https://x.com" target="_blank" rel="noopener">X</a>.</li>
    </ol>

    <h2>Uninstall the Extension at the End</h2>
    <p>
      The extension is scheduled to uninstall automatically after 20 minutes.
    </p>

    <h2>Continue Even If Not Logged In</h2>
    <p>
      If you are not logged in to one or more AI platforms, captured AI data can be reduced. Continue the test and report which platforms were not logged in.
    </p>

    <h2>Report Any Problems</h2>
    <p>If something fails, please report:</p>
    <ul>
      <li>Step number (for example, Step 6).</li>
      <li>What happened and any exact error text.</li>
      <li>Your browser version from About Chrome.</li>
    </ul>

    <script>
      const clickedLinksStorageKey = 'newsEvalClickedLinks';
      const countdownStartStorageKey = 'newsEvalCountdownStart';
      const countdownDurationMs = 20 * 60 * 1000;
      const countdownWarningMs = 2 * 60 * 1000;
      const windowReopenHash = '#window-reopen-cycle';

      const readClickedLinks = () => {
        try {
          const storedValue = localStorage.getItem(clickedLinksStorageKey);
          return storedValue ? JSON.parse(storedValue) : [];
        } catch {
          return [];
        }
      };

      const writeClickedLinks = (links) => {
        try {
          localStorage.setItem(clickedLinksStorageKey, JSON.stringify(Array.from(new Set(links))));
        } catch {
          // Ignore storage failures and continue with in-memory behavior.
        }
      };

      const clickedLinks = readClickedLinks();
      const linkElements = Array.from(document.querySelectorAll('.track-link'));
      const countdownBanner = document.getElementById('countdownBanner');
      const countdownTime = document.getElementById('countdownTime');

      let countdownStart = Number(localStorage.getItem(countdownStartStorageKey));

      if (!Number.isFinite(countdownStart) || (Date.now() - countdownStart > countdownDurationMs && window.location.hash !== windowReopenHash)) {
        countdownStart = Date.now();
        localStorage.setItem(countdownStartStorageKey, String(countdownStart));
      }

      const formatRemainingTime = (remainingMs) => {
        const totalSeconds = Math.max(0, Math.ceil(remainingMs / 1000));
        const minutes = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const seconds = String(totalSeconds % 60).padStart(2, '0');
        return `${minutes}:${seconds}`;
      };

      const updateCountdown = () => {
        if (!countdownBanner || !countdownTime) {
          return;
        }

        const elapsedMs = Date.now() - countdownStart;
        const remainingMs = Math.max(0, countdownDurationMs - elapsedMs);

        countdownTime.textContent = formatRemainingTime(remainingMs);

        const isWarning = remainingMs <= countdownWarningMs;
        countdownBanner.classList.toggle('warning', isWarning);
        countdownBanner.classList.toggle('blink', isWarning);
      };

      updateCountdown();
      setInterval(updateCountdown, 1000);

      linkElements.forEach((element) => {
        if (clickedLinks.includes(element.href)) {
          element.classList.add('clicked');
        }

        element.addEventListener('click', () => {
          element.classList.add('clicked');
          if (!clickedLinks.includes(element.href)) {
            clickedLinks.push(element.href);
            writeClickedLinks(clickedLinks);
          }
        });
      });

      const copyReturnUrlBtn = document.getElementById('copyReturnUrlBtn');
      const copyConfirm = document.getElementById('copyConfirm');
      if (copyReturnUrlBtn) {
        copyReturnUrlBtn.addEventListener('click', () => {
          navigator.clipboard.writeText('https://www.csmapsurveys.org/news_eval_testing#window-reopen-cycle').then(() => {
            copyConfirm.style.display = 'inline';
            setTimeout(() => { copyConfirm.style.display = 'none'; }, 3000);
          });
        });
      }

      if (window.location.hash === windowReopenHash) {
        const rapidCycleLinks = Array.from(document.querySelectorAll('[data-button-group="rapid-cycle"] .track-link'));

        rapidCycleLinks.forEach((element) => {
          element.classList.add('clicked');
          if (!clickedLinks.includes(element.href)) {
            clickedLinks.push(element.href);
          }
        });

        writeClickedLinks(clickedLinks);

        const windowReopenHeading = document.getElementById('window-reopen-cycle');
        if (windowReopenHeading) {
          windowReopenHeading.scrollIntoView({ behavior: 'smooth', block: 'start' });
          windowReopenHeading.focus({ preventScroll: true });
        }
      }
    </script>
  </body>
</html>

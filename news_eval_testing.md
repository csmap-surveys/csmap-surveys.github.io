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
        border: 1px solid #2c6f8e;
        border-radius: 6px;
        background-color: #59b2d1;
        color: #111;
        padding: 8px 12px;
        cursor: pointer;
        margin-right: 8px;
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

      .mono {
        font-family: monospace;
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
      Assigned IDs are now verified automatically by the extension. You should not need to manually confirm ID format during the test.
    </p>

    <h2>Use Chrome Browser</h2>
    <p>
      Complete this test in Google Chrome.
    </p>

    <ul>
      <li>Keep this browser window open for the full test.</li>
      <li>If asked to install the extension, complete install before moving to the next step.</li>
      <li>If a site asks you to sign in, sign in if possible and continue.</li>
    </ul>

    <ol>
      <li>Open your assigned test link in Chrome.</li>
      <li>Install <a href="https://chromewebstore.google.com/detail/news-evaluation-extension/deelgjiaicpdbfjmpifibadbhpijoofi?pli=1" target="_blank" rel="noopener" onclick="window.open(this.href, 'newsEvalExtensionWindow', 'noopener,width=1200,height=900'); return false;">News Evaluation Extension</a>.</li>
      <li>Wait for the assigned ID to be verified automatically.
        <ul>
          <li>Expected result: the consent information screen appears. Click <strong>I have read this information</strong>.</li>
          <li>If the ID input screen appears instead, enter the ID provided by the study team and continue, then report that the automatic verification step did not complete as expected.</li>
        </ul>
      </li>
      <li>Open <a href="https://www.google.com" target="_blank" rel="noopener">Google</a>, search for "latest climate policy update", and open one result.</li>
      <li>Open two news sites from this list: <a href="https://www.nytimes.com" target="_blank" rel="noopener">NYTimes</a>, <a href="https://www.reuters.com" target="_blank" rel="noopener">Reuters</a>, <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a>. On each site, click at least one article link.</li>
      <li>Open two social sites from this list: <a href="https://x.com" target="_blank" rel="noopener">X</a>, <a href="https://www.reddit.com" target="_blank" rel="noopener">Reddit</a>, <a href="https://www.linkedin.com" target="_blank" rel="noopener">LinkedIn</a>. Perform one normal interaction on each (open a post/thread/profile).</li>
      <li>Type one destination URL directly in the address bar (example: <a href="https://www.bbc.com" target="_blank" rel="noopener">bbc.com</a>).</li>
      <li>Use browser Back, Forward, and Reload once each on a page you just visited.</li>
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
      <li>Stop after those 2 questions unless you already have additional free usage available on your account.</li>
    </ol>

    <div class="actions">
      <button id="openRapidTabs" class="btn">Open 4 Rapid Tabs</button>
    </div>
    <p>If your browser blocks pop-ups, allow pop-ups for this page and click the button again.</p>
    <p id="rapidTabsStatus" class="note" style="display:none;"></p>
    <ol>
      <li><strong>Rapid tab cycle:</strong> Click <strong>Open 4 Rapid Tabs</strong> to open <a href="https://www.reuters.com" target="_blank" rel="noopener">Reuters</a>, <a href="https://www.reddit.com" target="_blank" rel="noopener">Reddit</a>, <a href="https://www.cnn.com" target="_blank" rel="noopener">CNN</a>, and <a href="https://www.msnbc.com" target="_blank" rel="noopener">MSNBC</a>. Switch between the tabs, and close them immediately</li>
      <li><strong>Delayed close cycle:</strong> Open <a href="https://www.nytimes.com" target="_blank" rel="noopener">NYTimes</a>, <a href="https://www.linkedin.com" target="_blank" rel="noopener">LinkedIn</a>, <a href="https://www.perplexity.ai" target="_blank" rel="noopener">Perplexity</a>, and <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a>. Keep them open for 1 minute or more while you browse between them. On all open tabs, scroll up and down. On any two tabs of your choice, copy a short piece of text and, in that same tab, paste it into the address bar, press Enter, and open information from the results page. On the other two tabs, do not copy text; click at least one link within the page. Then close the tabs one by one.</li>
      <li><strong>Window reopen cycle:</strong> Close the browser window, wait at least 30 seconds, reopen Chrome, then continue browsing for 2-3 minutes on <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a> and <a href="https://x.com" target="_blank" rel="noopener">X</a>.</li>
    </ol>

    <h2>Uninstall the Extension at the End</h2>
    <p>
      At the end of the test, verify that extension uninstall works from browser extension settings.
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
      const openRapidTabsButton = document.getElementById('openRapidTabs');
      const rapidTabsStatus = document.getElementById('rapidTabsStatus');

      if (openRapidTabsButton) {
        openRapidTabsButton.addEventListener('click', () => {
          const rapidSites = [
            'https://www.reuters.com',
            'https://www.reddit.com',
            'https://www.cnn.com',
            'https://www.msnbc.com'
          ];

          const openedTabs = rapidSites.map(() => window.open('', '_blank'));
          let blockedCount = 0;

          openedTabs.forEach((tabHandle, index) => {
            if (tabHandle) {
              tabHandle.location.href = rapidSites[index];
            } else {
              blockedCount += 1;
            }
          });

          if (rapidTabsStatus) {
            if (blockedCount === 0) {
              rapidTabsStatus.style.display = 'none';
              rapidTabsStatus.textContent = '';
            } else {
              rapidTabsStatus.style.display = 'block';
              rapidTabsStatus.textContent = blockedCount === rapidSites.length
                ? 'Chrome blocked all rapid tabs. Allow pop-ups for this page and click the button again.'
                : `Chrome blocked ${blockedCount} rapid tab(s). Allow pop-ups for this page and click the button again.`;
            }
          }

          const originalText = openRapidTabsButton.textContent;
          openRapidTabsButton.classList.add('launching');
          openRapidTabsButton.textContent = 'Tabs Opened';

          setTimeout(() => {
            openRapidTabsButton.classList.remove('launching');
            openRapidTabsButton.textContent = originalText;
          }, 1600);
        });
      }
    </script>
  </body>
</html>

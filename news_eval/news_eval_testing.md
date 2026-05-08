---
title: News Evaluation Test Instructions
layout: news_eval
permalink: /news_eval_testing
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
        position: static;
        display: inline-flex;
        align-items: center;
        margin-left: auto;
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

      .countdown-banner.in-header {
        flex-shrink: 0;
      }

      @media (max-width: 760px) {
        .countdown-banner {
          margin-top: 10px;
          margin-left: 0;
          width: 100%;
          justify-content: center;
        }
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

      .close-window-btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        width: 34px;
        height: 34px;
        margin-left: 8px;
        border: 2px solid #a61e1e;
        border-radius: 50%;
        background: #fff5f5;
        color: #a61e1e;
        font-size: 18px;
        font-weight: 700;
        line-height: 1;
        cursor: pointer;
      }

      .close-window-btn:active {
        background: #ffe3e3;
      }

      .close-window-hint {
        display: none;
        margin-left: 10px;
        color: #a61e1e;
        font-weight: 700;
        font-size: 13px;
      }

      .guide-inline-hidden {
        display: none;
      }

      .section-required {
        display: inline-block;
        background: #57068c;
        color: #fff;
        font-size: 13px;
        font-weight: 700;
        letter-spacing: 0.04em;
        padding: 2px 8px;
        border-radius: 4px;
        vertical-align: middle;
        margin-left: 8px;
      }

      .popup-warning {
        margin: 10px 0 14px;
        padding: 10px 12px;
        border-left: 4px solid #c92a2a;
        background: #fff5f5;
        color: #7a1f1f;
        font-weight: 700;
      }

      .guide-inline-hidden {
        display: none;
      }

      .guide-inline-visible {
        display: block;
      }

      .guide-inline-fallback {
        margin-top: 10px;
        padding: 10px 12px;
        border-left: 4px solid #2c6f8e;
        background: #f3fbfe;
      }

      .guide-inline-fallback-title {
        margin: 0 0 8px;
        font-weight: 700;
        color: #12303d;
      }

      .guide-inline-fallback ol {
        margin: 0;
        padding-left: 22px;
      }

      .guide-inline-fallback li {
        margin-bottom: 6px;
      }
    </style>
  </head>
  <body>
    <h1>News Evaluation Extension </h1>
    <h2>Test Guidelines <span class="section-required">Read before starting</span></h2>
    <div class="note">
      <ul>
        <li>All data collected for this testing cycle will be removed by CSMAP engineers after analysis.</li>
        <li>You are required to complete all sections of this test within 20 minutes. Work through each section in order.</li>
        <li>You may use Gemini, ChatGPT, and Perplexity whether or not you are signed in. Please report any platform where you were not logged in.</li>
        <li>Clicking a task link opens the site and a step-by-step instruction window. Place them side by side — the instruction window updates for each task.</li>
      </ul>
    </div>

    <div class="countdown-banner" id="countdownBanner" role="status" aria-live="polite">
      <span class="countdown-label">Time Remaining:</span>
      <span class="countdown-time" id="countdownTime">20:00</span>
    </div>

    <div id="popupWarning" class="popup-warning" hidden>
      Instruction popup was blocked. Allow pop-ups for this page and continue using the inline steps shown under each task.
    </div>

    <h2>Install</h2>
    <p>
      Complete this test in Google Chrome.
    </p>

    <ol>
      <li>Visit <a id="installExtensionLink" href="https://chromewebstore.google.com/detail/news-evaluation-extension/deelgjiaicpdbfjmpifibadbhpijoofi?pli=1" target="_blank" rel="noopener" data-task-id="install-extension">Chrome Web store</a>.</li>
    </ol>

    <h2>Engagement</h2>
    <p>Complete each task below by following instructions provided on the instructions windo</p>
  
    <ol>
      <li>Open <a href="https://www.google.com" target="_blank" rel="noopener" data-task-id="single-google">Google</a> <strong>Starts</strong> the timer on your upper right side 
        <ul class="guide-inline-hidden">
          <li>Search for "latest climate policy update"</li>
          <li>Open one result, scroll down the page, then return near the top</li>
          <li>Copy one full sentence from that page, paste it into the Google search bar, add the word "source," and search</li>
          <li>Open one result from that second search and briefly scroll the page</li>
          <li>Close the tab</li>
        </ul>
      </li>
      <li>Open <a href="https://www.nytimes.com" target="_blank" rel="noopener" data-task-id="single-nytimes">NYTimes</a>
        <ul class="guide-inline-hidden">
          <li>Click one article link within the page</li>
          <li>Quickly scroll down, pause briefly, then scroll back toward the top of the opened page</li>
          <li>Click one non-article element on the page such as a section label, menu item, or related item, then return to the article if needed</li>
          <li>Press the browser <span class="mono">Back</span> once and <span class="mono">Forward</span> once</li>
          <li>Close the tab</li>
        </ul>
      </li>
      <li>Open <a href="https://www.reuters.com" target="_blank" rel="noopener" data-task-id="single-reuters">Reuters</a>
        <ul class="guide-inline-hidden">
          <li>Click one article link and scroll about halfway down the opened page</li>
          <li>Copy a short piece of text from the middle of that page</li>
          <li>Paste it into the same tab's address bar and press <span class="mono">Enter</span></li>
          <li>On the page that opens, scroll once near the top and once farther down</li>
          <li>Close the tab</li>
        </ul>
      </li>
      <li>Open <a href="https://apnews.com" target="_blank" rel="noopener" data-task-id="single-apnews">AP News</a>
        <ul class="guide-inline-hidden">
          <li>Click one article link and scroll through the opened page</li>
          <li>Click one additional related link within that same tab</li>
          <li>On the second page, scroll to a different section of the page</li>
          <li>Use browser <span class="mono">Back</span> once and <span class="mono">Forward</span> once</li>
        </ul>
      </li>
    </ol>

    <h3>Gemini</h3>
    <ol>
      <li>Open <a href="https://gemini.google.com" target="_blank" rel="noopener" data-task-id="ai-gemini">Gemini</a>.</li>
      <li class="guide-inline-hidden">Type and send question 1, wait for the response to fully render, then type and send question 2, and wait for that response to fully render.</li>
      <li class="guide-inline-hidden">Type and send question 3. While waiting for its response, type question 4 so it is ready to send as soon as the input field becomes available.</li>
    </ol>

    <h3>ChatGPT</h3>
    <ol>
      <li>Open <a href="https://chatgpt.com" target="_blank" rel="noopener" data-task-id="ai-chatgpt">ChatGPT</a>.</li>
      <li class="guide-inline-hidden">Type and send question 1, wait for the response to fully render, then type and send question 2, and wait for that response to fully render.</li>
      <li class="guide-inline-hidden">Type and send question 3. While waiting for its response, type question 4 so it is ready to send as soon as the input field becomes available.</li>
    </ol>

    <h3>Perplexity</h3>
    <ol>
      <li>Open <a href="https://www.perplexity.ai" target="_blank" rel="noopener" data-task-id="ai-perplexity">Perplexity</a>.</li>
      <li class="guide-inline-hidden">Type and send question 1, wait for the response to fully render, then type and send question 2, and wait for that response to fully render.</li>
      <li class="guide-inline-hidden">Type and send question 3. While waiting for its response, type question 4 so it is ready to send as soon as the input field becomes available.</li>
    </ol>

    <h3>Tab Navigation</h3>
    <ol>
      <li><strong>Rapid tab cycle:</strong>
      Click each button below and close the opened tab immediately.
      <div class="rapid-buttons" data-button-group="rapid-cycle">
        <a class="btn track-link" href="https://www.reuters.com" target="_blank" rel="noopener" data-task-id="rapid-reuters">Open Reuters</a>
        <a class="btn track-link" href="https://www.netflix.com" target="_blank" rel="noopener" data-task-id="rapid-netflix">Open Netflix</a>
        <a class="btn track-link" href="https://www.cnn.com" target="_blank" rel="noopener" data-task-id="rapid-cnn">Open CNN</a>
        <a class="btn track-link" href="https://www.msnbc.com" target="_blank" rel="noopener" data-task-id="rapid-msnbc">Open MSNBC</a>
      </div></li>
      <li><strong>Delayed close cycle:</strong>
        <p><strong>Copy and Paste</strong></p>
        <ul>
          <li>Open the two tabs below
            <div class="rapid-buttons">
              <a class="btn track-link" href="https://www.nytimes.com" target="_blank" rel="noopener" data-task-id="delayed-copy-nytimes">Open NYTimes</a>
              <a class="btn track-link" href="https://www.aljazeera.com/" target="_blank" rel="noopener" data-task-id="delayed-copy-aljazeera">Open Aljazeera</a>
            </div>
          </li>
          <li class="guide-inline-hidden">In the NYTimes tab, scroll down and then back up; in the Aljazeera tab, scroll first near the top and then farther down the page</li>
          <li class="guide-inline-hidden">Copy a full sentence from NYTimes and a short phrase from Aljazeera, then paste each one into that tab's address bar</li>
          <li class="guide-inline-hidden">Press Enter</li>
          <li class="guide-inline-hidden">On each new page, scroll once near the top and once lower on the page, then close</li>
        </ul>
        <p><strong>Click and Browse</strong></p>
        <ul>
          <li>Open the two tabs below
            <div class="rapid-buttons">
              <a class="btn track-link" href="https://www.perplexity.ai" target="_blank" rel="noopener" data-task-id="delayed-browse-perplexity">Open Perplexity</a>
              <a class="btn track-link" href="https://apnews.com" target="_blank" rel="noopener" data-task-id="delayed-browse-apnews">Open AP News</a>
            </div>
          </li>
          <li class="guide-inline-hidden">In the Perplexity tab, type a short 3-5 word question and submit it if the input is available; in the AP News tab, scroll the page before opening an article</li>
          <li class="guide-inline-hidden">Scroll up and down each site</li>
          <li class="guide-inline-hidden">Click one link within each page; for Perplexity, prefer a cited source if visible</li>
          <li class="guide-inline-hidden">Slowly browse the new open link, including one downward scroll and one upward scroll</li>
          <li class="guide-inline-hidden">Close the link and then close the tab</li>
        </ul>
      </li>
    </ol>

    <h2 id="window-reopen-cycle" tabindex="-1">Window Reopen </h2>

    <div id="windowCyclePreMode">
      <p>Copy the return URL below — you will paste it into Chrome after reopening.</p>
      <p>
        <button type="button" class="copy-url-btn" id="copyReturnUrlBtn">Copy Return URL</button>
        <span class="copy-confirm" id="copyConfirm">Copied.</span>
      </p>
      <p>
        Close the browser window.
        <button type="button" class="close-window-btn" id="closeWindowBtn" aria-label="Close browser window">&times;</button>
        <span class="close-window-hint" id="closeWindowHint">If it does not close, close Chrome manually.</span>
      </p>
      <ol class="guide-inline-hidden">
        <li>Click "Copy Return URL" and confirm the copied message appears.</li>
        <li>Click the close (x) button to try to close this browser window. If blocked, close Chrome manually.</li>
        <li>Wait at least 30 seconds before reopening Chrome.</li>
        <li>Paste the copied URL into the address bar and press Enter.</li>
      </ol>
    </div>

    <div id="windowCycleReopenMode" hidden>
      <p>Click on the button Open YouTube.</p>
      <p>
        <a class="btn" href="https://www.youtube.com" target="_blank" rel="noopener" data-task-id="reopen-youtube" id="windowReopenYoutubeBtn">Open YouTube</a>
      </p>
      <ol>
        <li class="guide-inline-hidden">Browse YouTube for 2-3 minutes — open at least one video and scroll the feed.</li>
      </ol>
    </div>

    <h2>Auto Uninstall </h2>
    <p>
      The extension is scheduled to uninstall automatically after 20 minutes.
    </p>

    <h2>Report Any Problems</h2>
    <p>If something fails, please report:</p>
    <ul>
      <li>Section name (e.g, Gemini).</li>
      <li>What happened and any exact error text.</li>
      <li>Your browser version from About Chrome.</li>
    </ul>
    <p>Reply all to the group email thread with Kylan Rutherford and include the information above.</p>

    <script>
      const sessionId = new URLSearchParams(window.location.search).get('id') || '';
      const countdownStartStorageKey = sessionId
        ? `newsEvalCountdownStart_${sessionId}`
        : 'newsEvalCountdownStart';
      const countdownResumeArmedKey = sessionId
        ? `newsEvalCountdownResumeArmed_${sessionId}`
        : 'newsEvalCountdownResumeArmed';
      const countdownDurationMs = 20 * 60 * 1000;
      const countdownWarningMs = 2 * 60 * 1000;
      const windowReopenHash = '#window-reopen-cycle';
      const taskGuideWindowName = 'newsEvalTaskGuide';

      let activeTaskGuideWindow = null;

      const taskGuideContent = {
        'install-extension': {
          title: 'Install Extension Guide',
          steps: [
            'Install the News Evaluation Extension by clicking Add to Chrome',
            'Select Add extension button',
            'Wait for the assigned ID to be verified automatically.',
            'Expected result: The consent information screen appears. Click "I have read this information."',
            'If the ID input screen appears instead, enter the ID provided by the study team and continue, then report that the automatic verification step did not complete as expected.',
            'After validation is complete, close the extension installation tab.',
            'The timer on the right side will begin a countdown.'
          ]
        },
        'window-reopen-instructions': {
          title: 'Window Reopen Task Guide',
          steps: [
            'Browse YouTube for 2-3 minutes — open at least one video and scroll the feed.'
          ]
        },
        'window-close-cycle': {
          title: 'Window Close Cycle Guide',
          steps: [
            'Click "Copy Return URL" and confirm the copied message appears.',
            'Click the close (x) button to try to close this browser window. If blocked, close Chrome manually.',
            'Wait at least 30 seconds before reopening Chrome.',
            'Paste the copied URL into the address bar and press Enter.'
          ]
        },
        'single-google': {
          title: 'Google Task Guide',
          steps: [
            'Search for "latest climate policy update."',
            'Open one result, scroll down the page, then return near the top.',
            'Copy one full sentence from that page, paste it into the Google search bar, add the word "source," and search.',
            'Open one result from that second search and briefly scroll the page.',
            'Close the tab.'
          ]
        },
        'single-nytimes': {
          title: 'NYTimes Task Guide',
          steps: [
            'Click one article link within the page.',
            'Quickly scroll down, pause briefly, then scroll back toward the top of the opened page.',
            'Click one non-article element on the page such as a section label, menu item, or related item, then return to the article if needed.',
            'Press Back once and Forward once.',
            'Close the tab.'
          ]
        },
        'single-reuters': {
          title: 'Reuters Task Guide',
          steps: [
            'Click one article link and scroll about halfway down the opened page.',
            'Copy a short piece of text from the middle of that page.',
            'Paste it into the same tab\'s address bar and press Enter.',
            'On the page that opens, scroll once near the top and once farther down.',
            'Close the tab.'
          ]
        },
        'single-apnews': {
          title: 'AP News Task Guide',
          steps: [
            'Click one article link and scroll through the opened page.',
            'Click one additional related link within that same tab.',
            'On the second page, scroll to a different section of the page.',
            'Use Back once and Forward once.',
            'Close the tab.'
          ]
        },
        'ai-gemini': {
          title: 'Gemini Task Guide',
          steps: [
            'Ask 2 questions and wait for each response to fully render before sending the next question.',
            'Ask 3 more questions successively without waiting for the previous response to fully render.'
          ]
        },
        'ai-chatgpt': {
          title: 'ChatGPT Task Guide',
          steps: [
            'Ask 2 questions and wait for each response to fully render before sending the next question.',
            'Ask 3 more questions successively without waiting for the previous response to fully render.'
          ]
        },
        'ai-perplexity': {
          title: 'Perplexity Task Guide',
          steps: [
            'Ask 2 questions and wait for each response to fully render before sending the next question.',
            'If logged in, ask 3 more questions successively without waiting for each response to finish.',
            'If not logged in, stop after the first 2 questions.'
          ]
        },
        'rapid-reuters': {
          title: 'Rapid Tab Cycle Guide - Reuters',
          steps: [
            'Open the site in a new tab or window.',
            'Close the opened tab immediately.'
          ]
        },
        'rapid-netflix': {
          title: 'Rapid Tab Cycle Guide - Netflix',
          steps: [
            'Open the site in a new tab or window.',
            'Close the opened tab immediately.'
          ]
        },
        'rapid-cnn': {
          title: 'Rapid Tab Cycle Guide - CNN',
          steps: [
            'Open the site in a new tab or window.',
            'Close the opened tab immediately.'
          ]
        },
        'rapid-msnbc': {
          title: 'Rapid Tab Cycle Guide - MSNBC',
          steps: [
            'Open the site in a new tab or window.',
            'Close the opened tab immediately.'
          ]
        },
        'delayed-copy-nytimes': {
          title: 'Delayed Close: NYTimes Guide',
          steps: [
            'Scroll down and then back up in the NYTimes tab.',
            'Copy a full sentence from the page.',
            'Paste it into that tab\'s address bar and press Enter.',
            'On the new page, scroll once near the top and once lower on the page.',
            'Close the tab.'
          ]
        },
        'delayed-copy-aljazeera': {
          title: 'Delayed Close: Aljazeera Guide',
          steps: [
            'Scroll first near the top and then farther down the page.',
            'Copy a short phrase from the page.',
            'Paste it into that tab\'s address bar and press Enter.',
            'On the new page, scroll once near the top and once lower on the page.',
            'Close the tab.'
          ]
        },
        'delayed-browse-perplexity': {
          title: 'Delayed Close: Perplexity Guide',
          steps: [
            'Type a short 3-5 word question and submit it if the input is available.',
            'Scroll up and down the site.',
            'Click one link within the page, preferably a cited source if visible.',
            'Slowly browse the new open link, including one downward scroll and one upward scroll.',
            'Close the link and then close the tab.'
          ]
        },
        'delayed-browse-apnews': {
          title: 'Delayed Close: AP News Guide',
          steps: [
            'Scroll the page before opening an article.',
            'Scroll up and down the site.',
            'Click one link within the page.',
            'Slowly browse the new open link, including one downward scroll and one upward scroll.',
            'Close the link and then close the tab.'
          ]
        },
        'reopen-youtube': {
          title: 'Window Reopen: YouTube Guide',
          steps: [
            'Browse YouTube for 2-3 minutes — open at least one video and scroll the feed.'
          ]
        }
      };

      const escapeHtml = (value) => String(value)
        .replaceAll('&', '&amp;')
        .replaceAll('<', '&lt;')
        .replaceAll('>', '&gt;')
        .replaceAll('"', '&quot;')
        .replaceAll("'", '&#39;');

      const renderTaskGuideHtml = (title, url, steps) => `<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>${escapeHtml(title)}</title>
    <style>
      body {
        margin: 0;
        padding: 18px;
        font-family: Georgia, serif;
        line-height: 1.45;
        background: #f6fbfd;
        color: #12303d;
      }

      h1 {
        margin: 0 0 12px;
        font-size: 22px;
      }

      p {
        margin: 0 0 12px;
        font-size: 14px;
      }

      .url {
        margin: 0 0 16px;
        padding: 10px 12px;
        border-left: 4px solid #2c6f8e;
        background: #eaf6fb;
        font-size: 13px;
        word-break: break-word;
      }

      ol {
        padding-left: 22px;
        margin: 0;
      }

      li {
        margin: 0 0 10px;
        font-size: 15px;
      }

      .note {
        margin-top: 18px;
        padding-top: 12px;
        border-top: 1px solid #c8dfe8;
        font-size: 13px;
        color: #395865;
      }
    </style>
  </head>
  <body>
    <h1>${escapeHtml(title)}</h1>
    <p>Keep this guide open while completing the task in the site window.</p>
    <div class="url">Site: ${escapeHtml(url)}</div>
    <ol>
      ${steps.map((step) => `<li>${escapeHtml(step)}</li>`).join('')}
    </ol>
    <p class="note">If the guide does not appear beside the site automatically, move the guide window to one side and resize the main browser window manually.</p>
  </body>
</html>`;

      const getSplitLayout = () => {
        const screenLeft = Number.isFinite(window.screenX) ? window.screenX : 0;
        const screenTop = Number.isFinite(window.screenY) ? window.screenY : 0;
        const totalWidth = Math.max(window.outerWidth || 1280, 1000);
        const totalHeight = Math.max(window.outerHeight || 800, 700);

        const guideWidth = Math.max(360, Math.floor(totalWidth * 0.34));
        const mainWidth = Math.max(620, totalWidth - guideWidth);

        return {
          top: screenTop,
          left: screenLeft,
          height: totalHeight,
          guide: {
            left: screenLeft,
            top: screenTop,
            width: guideWidth,
            height: totalHeight
          },
          main: {
            left: screenLeft + guideWidth,
            top: screenTop,
            width: mainWidth,
            height: totalHeight
          }
        };
      };

      const openTaskGuideWindow = (taskId, url, layout) => {
        const guide = taskGuideContent[taskId];
        if (!guide) {
          return null;
        }

        const features = [
          'popup=yes',
          'resizable=yes',
          'scrollbars=yes',
          `width=${layout.guide.width}`,
          `height=${layout.guide.height}`,
          `left=${layout.guide.left}`,
          `top=${layout.guide.top}`
        ].join(',');

        const guideWindow = window.open('', taskGuideWindowName, features);
        if (!guideWindow) {
          return null;
        }

        guideWindow.document.open();
        guideWindow.document.write(renderTaskGuideHtml(guide.title, url, guide.steps));
        guideWindow.document.close();
        return guideWindow;
      };

      const openTaskWindows = (taskId, url) => {
        const guide = taskGuideContent[taskId];
        if (!guide) {
          window.open(url, '_blank');
          return;
        }

        const layout = getSplitLayout();
        const openedTab = window.open(url, '_blank');

        if (!openedTab) {
          return;
        }

        activeTaskGuideWindow = openTaskGuideWindow(taskId, url, layout);
        if (activeTaskGuideWindow && !activeTaskGuideWindow.closed) {
          activeTaskGuideWindow.focus();
        }

        openedTab.focus();
      };

      const linkElements = Array.from(document.querySelectorAll('.track-link'));
      const popupWarning = document.getElementById('popupWarning');
      const countdownBanner = document.getElementById('countdownBanner');
      const countdownTime = document.getElementById('countdownTime');
      const mountCountdownBannerInHeader = () => {
        if (!countdownBanner) {
          return;
        }

        const headerWrapper = document.querySelector('.news-eval-header .wrapper');
        if (!headerWrapper) {
          return;
        }

        countdownBanner.classList.add('in-header');
        headerWrapper.appendChild(countdownBanner);
      };

      const storedCountdownStart = Number(localStorage.getItem(countdownStartStorageKey));
      const isWindowReopenVisit = window.location.hash === windowReopenHash;
      const isResumeArmed = localStorage.getItem(countdownResumeArmedKey) === '1';
      const now = Date.now();
      const hasValidStoredCountdownStart = Number.isFinite(storedCountdownStart) && (now - storedCountdownStart <= countdownDurationMs);

      let countdownStart;
      if (isWindowReopenVisit && isResumeArmed && hasValidStoredCountdownStart) {
        countdownStart = storedCountdownStart;
        localStorage.removeItem(countdownResumeArmedKey);
      } else {
        countdownStart = null;
        localStorage.removeItem(countdownStartStorageKey);
        localStorage.removeItem(countdownResumeArmedKey);
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

        if (!Number.isFinite(countdownStart)) {
          countdownTime.textContent = '00:00';
          countdownBanner.classList.remove('warning', 'blink');
          return;
        }

        const elapsedMs = Date.now() - countdownStart;
        const remainingMs = Math.max(0, countdownDurationMs - elapsedMs);

        countdownTime.textContent = formatRemainingTime(remainingMs);

        const isWarning = remainingMs <= countdownWarningMs;
        countdownBanner.classList.toggle('warning', isWarning);
        countdownBanner.classList.toggle('blink', isWarning);
      };

      mountCountdownBannerInHeader();
      updateCountdown();
      setInterval(updateCountdown, 1000);

      const startCountdownIfNeeded = () => {
        if (Number.isFinite(countdownStart)) {
          return;
        }

        countdownStart = Date.now();
        localStorage.setItem(countdownStartStorageKey, String(countdownStart));
        localStorage.removeItem(countdownResumeArmedKey);
        updateCountdown();
      };

      const clearCountdownSession = () => {
        countdownStart = null;
        localStorage.removeItem(countdownStartStorageKey);
        localStorage.removeItem(countdownResumeArmedKey);
        updateCountdown();
      };

      const closeGuideWindow = () => {
        if (activeTaskGuideWindow && !activeTaskGuideWindow.closed) {
          activeTaskGuideWindow.close();
        }
        activeTaskGuideWindow = null;
      };

      const taskLinks = Array.from(document.querySelectorAll('[data-task-id]'));
      const windowCyclePreMode = document.getElementById('windowCyclePreMode');
      const windowCycleReopenMode = document.getElementById('windowCycleReopenMode');
      const returnUrl = `${window.location.origin}${window.location.pathname}${window.location.search}${windowReopenHash}`;

      const openGuideForElement = (element) => {
        const taskId = element.dataset.taskId;
        const guide = taskGuideContent[taskId];

        const showInlineGuideForElement = () => {
          const parentTaskItem = element.closest('li');
          if (!parentTaskItem) {
            return;
          }

          let revealedExistingGuide = false;
          parentTaskItem.querySelectorAll('.guide-inline-hidden').forEach((node) => {
            node.classList.remove('guide-inline-hidden');
            node.classList.add('guide-inline-visible');
            revealedExistingGuide = true;
          });

          if (revealedExistingGuide || !guide) {
            return;
          }

          let fallbackBlock = parentTaskItem.querySelector(`.guide-inline-fallback[data-task-id="${taskId}"]`);
          if (fallbackBlock) {
            fallbackBlock.hidden = false;
            return;
          }

          fallbackBlock = document.createElement('div');
          fallbackBlock.className = 'guide-inline-fallback guide-inline-visible';
          fallbackBlock.dataset.taskId = taskId;

          const title = document.createElement('p');
          title.className = 'guide-inline-fallback-title';
          title.textContent = guide.title;
          fallbackBlock.appendChild(title);

          const list = document.createElement('ol');
          guide.steps.forEach((step) => {
            const item = document.createElement('li');
            item.textContent = step;
            list.appendChild(item);
          });
          fallbackBlock.appendChild(list);

          parentTaskItem.appendChild(fallbackBlock);
        };

        const showGuideFallbackWarning = () => {
          if (!popupWarning) {
            return;
          }

          popupWarning.hidden = false;
          popupWarning.textContent = 'Instruction popup did not render the expected guide. Continue using the inline steps shown under the active task.';
        };

        openTaskWindows(taskId, element.href);
        const guideWindow = activeTaskGuideWindow;
        if (!guideWindow) {
          showGuideFallbackWarning();
          showInlineGuideForElement();
          return;
        }

        window.setTimeout(() => {
          try {
            const bodyText = guideWindow.document?.body?.innerText || '';
            const expectedTitleVisible = guide ? bodyText.includes(guide.title) : false;
            const expectedStepVisible = guide?.steps?.[0] ? bodyText.includes(guide.steps[0]) : false;

            if (!expectedTitleVisible || !expectedStepVisible) {
              showGuideFallbackWarning();
              showInlineGuideForElement();
            }
          } catch {
            showGuideFallbackWarning();
            showInlineGuideForElement();
          }
        }, 250);
      };

      linkElements.forEach((element) => {
        element.addEventListener('click', () => {
          element.classList.add('clicked');
        });
      });

      if (isWindowReopenVisit) {
        linkElements.forEach((element) => element.classList.add('clicked'));
      }

      taskLinks.forEach((element) => {
        element.addEventListener('click', (event) => {
          event.preventDefault();

          if (element.dataset.taskId === 'single-google') {
            startCountdownIfNeeded();
          }

          openGuideForElement(element);
        });
      });

      const copyReturnUrlBtn = document.getElementById('copyReturnUrlBtn');
      const copyConfirm = document.getElementById('copyConfirm');
      const closeWindowBtn = document.getElementById('closeWindowBtn');
      const closeWindowHint = document.getElementById('closeWindowHint');

      const fallbackCopyText = (text) => {
        const textArea = document.createElement('textarea');
        textArea.value = text;
        textArea.setAttribute('readonly', '');
        textArea.style.position = 'fixed';
        textArea.style.top = '-1000px';
        textArea.style.left = '-1000px';
        document.body.appendChild(textArea);
        textArea.focus();
        textArea.select();

        let copied = false;
        try {
          copied = document.execCommand('copy');
        } catch {
          copied = false;
        }

        document.body.removeChild(textArea);
        return copied;
      };

      const showCopySuccess = () => {
        if (!copyConfirm) {
          return;
        }

        copyConfirm.style.display = 'inline';
        setTimeout(() => {
          copyConfirm.style.display = 'none';
        }, 1800);
      };

      if (copyReturnUrlBtn) {
        copyReturnUrlBtn.addEventListener('click', async () => {
          let copied = false;
          try {
            if (navigator.clipboard && window.isSecureContext) {
              await navigator.clipboard.writeText(returnUrl);
              copied = true;
            }
          } catch {
            copied = false;
          }

          if (!copied) {
            copied = fallbackCopyText(returnUrl);
          }

          if (copied) {
            if (Number.isFinite(countdownStart)) {
              localStorage.setItem(countdownStartStorageKey, String(countdownStart));
              localStorage.setItem(countdownResumeArmedKey, '1');
            }
            showCopySuccess();
          }
        });
      }

      if (closeWindowBtn) {
        closeWindowBtn.addEventListener('click', () => {
          if (localStorage.getItem(countdownResumeArmedKey) !== '1') {
            clearCountdownSession();
          }

          closeGuideWindow();
          window.close();
          setTimeout(() => {
            if (closeWindowHint) {
              closeWindowHint.style.display = 'inline';
            }
          }, 450);
        });
      }

      window.addEventListener('beforeunload', () => {
        if (localStorage.getItem(countdownResumeArmedKey) !== '1') {
          localStorage.removeItem(countdownStartStorageKey);
        }
      });

      if (windowCyclePreMode && windowCycleReopenMode) {
        const isReopenMode = window.location.hash === windowReopenHash;
        windowCyclePreMode.hidden = isReopenMode;
        windowCycleReopenMode.hidden = !isReopenMode;
      }

      if (window.location.hash === windowReopenHash) {
        const windowReopenHeading = document.getElementById('window-reopen-cycle');
        if (windowReopenHeading) {
          windowReopenHeading.scrollIntoView({ behavior: 'smooth', block: 'start' });
          windowReopenHeading.focus({ preventScroll: true });
        }
      } else {
        const closeCycleList = windowCyclePreMode ? windowCyclePreMode.querySelector('ol') : null;
        if (closeCycleList) {
          closeCycleList.classList.remove('guide-inline-hidden');
          closeCycleList.classList.add('guide-inline-visible');
        }
      }

    </script>
  </body>
</html>

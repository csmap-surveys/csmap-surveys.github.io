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
      <li>Open <a href="https://www.google.com" target="_blank" rel="noopener">Google</a>, search for "latest climate policy update", and open one result.</li>
      <li>Open <a href="https://www.nytimes.com" target="_blank" rel="noopener">NYTimes</a> and click one article link.</li>
      <li>Open <a href="https://www.reuters.com" target="_blank" rel="noopener">Reuters</a> and click one article link.</li>
      <li>Open <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a> and click one article link.</li>
      <li>Open <a href="https://x.com" target="_blank" rel="noopener">X</a> and open one post, one thread, or one profile.</li>
      <li>Open <a href="https://www.reddit.com" target="_blank" rel="noopener">Reddit</a> and open a post/thread/profile.</li>
      <li>Open <a href="https://www.linkedin.com" target="_blank" rel="noopener">LinkedIn</a> and open a post/thread/profile.</li>
      <li>Open a new tab and type <span class="mono">bbc.com</span> in the address bar and press <span class="mono">Enter</span>.</li>
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
      <li>If logged in, ask 3 more questions successively without waiting for each response to finish.</li>
      <li>If not logged in, stop after the first 2 questions.</li>
    </ol>

    <h2>Tab Navigation</h2>
    <ol>
      <li><strong>Rapid tab cycle:</strong>
      Click each button below and close the opened tab immediately.
      <div class="rapid-buttons">
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

    <h2>Window Reopen Cycle</h2>
    <ol>
      <li>Close the browser window.</li>
      <li>Wait at least 30 seconds.</li>
      <li>Reopen Chrome.</li>
      <li>Continue browsing for 2-3 minutes on <a href="https://apnews.com" target="_blank" rel="noopener">AP News</a> and <a href="https://x.com" target="_blank" rel="noopener">X</a>.</li>
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
      document.querySelectorAll('.track-link').forEach((element) => {
        element.addEventListener('click', () => {
          element.classList.add('clicked');
        });
      });
    </script>
  </body>
</html>

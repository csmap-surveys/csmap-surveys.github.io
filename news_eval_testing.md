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
      This test checks whether the News Evaluation extension works correctly during normal browsing and AI task activity.
    </p>

    <h2>Capabilities Being Tested</h2>
    <ul>
      <li>Extension install, registration, and assigned ID loading.</li>
      <li>Navigation capture (typed URL, link click, back, forward, reload).</li>
      <li>AI task capture across Google, Gemini, ChatGPT, and Perplexity.</li>
      <li>Stability under rapid user actions and browser close/reopen.</li>
      <li>Extension uninstall behavior at the end of a session.</li>
    </ul>

    <p class="note">
      All data collected for this testing cycle will be removed by CSMaP engineers after analysis.
    </p>

    <h2>Browser Requirement</h2>
    <p>
      Complete this test in Google Chrome or another Chromium-based browser.
    </p>

    <h2>Test Steps</h2>
    <ol>
      <li>Open your assigned test link in Chrome.</li>
      <li>Install and open the News Evaluation extension when prompted. Capability tested: install and launch.</li>
      <li>Confirm your assigned ID is loaded for this session. Capability tested: assignment and registration.</li>
      <li>Go to <a href="https://www.google.com" target="_blank" rel="noopener noreferrer">Google</a>, run one search query, and open one result. Capability tested: search and click-through navigation capture.</li>
      <li>Go to <a href="https://gemini.google.com" target="_blank" rel="noopener noreferrer">Gemini</a> and submit one prompt. Capability tested: Gemini interaction capture.</li>
      <li>Go to <a href="https://chatgpt.com" target="_blank" rel="noopener noreferrer">ChatGPT</a> and submit one prompt. Capability tested: ChatGPT interaction capture.</li>
      <li>Go to <a href="https://www.perplexity.ai" target="_blank" rel="noopener noreferrer">Perplexity</a>, submit one prompt, then ask one follow-up in the same thread. Capability tested: multi-turn Perplexity capture.</li>
      <li>Type another destination URL directly in the address bar. Capability tested: direct URL navigation capture.</li>
      <li>Click a link on a page, then use Back, Forward, and Reload once each. Capability tested: transition tracking.</li>
      <li>Run a short stress pass: multiple quick queries, fast tab switching, and quick window close/reopen. Capability tested: session stability under rapid actions.</li>
      <li>Visit several additional websites to validate URL-hit tracking. Capability tested: broader URL-hit coverage.</li>
    </ol>

    <h2>Extension Uninstall Check</h2>
    <p>
      At the end of the test, verify that extension uninstall works from browser extension settings.
    </p>

    <h2>Important Account Note</h2>
    <p>
      If you are not logged in to one or more AI platforms, recorded AI data can be reduced. Continue the test and report which platforms were not logged in.
    </p>

    <h2>Issue Reporting</h2>
    <p>If something fails, report:</p>
    <ul>
      <li>The step that failed.</li>
      <li>The exact error text.</li>
      <li>Your browser version from About Chrome.</li>
    </ul>


  </body>
</html>

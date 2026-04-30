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

    <h2>What Will Be Captured</h2>
    <ul>
      <li>Extension registration status.</li>
      <li>Task-related browsing activity and task actions.</li>
      <li>Task completion timing.</li>
      <li>Technical errors encountered during testing.</li>
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
      <li>Install and open the News Evaluation extension when prompted.</li>
      <li>Confirm your assigned ID is loaded for this session.</li>
      <li>Complete the requested browsing tasks in order:</li>
    </ol>
    <ul>
      <li>Type a destination URL in the address bar.</li>
      <li>Click a link on a page.</li>
      <li>Click the link provided in your email.</li>
      <li>Use Back, Forward, and Reload in the task flow.</li>
      <li>Complete one task each on Google, Gemini, ChatGPT, and Perplexity.</li>
      <li>On Perplexity, submit at least one follow-up question in the same thread.</li>
      <li>Run stress tasks: multiple quick queries, fast tab switching, and quick window close/reopen.</li>
      <li>Visit several other websites to validate URL-hit tracking.</li>
    </ul>

    <h2>Required Screenshots</h2>
    <p>Take and submit screenshots of what you see on:</p>
    <ul>
      <li>Google</li>
      <li>Gemini</li>
      <li>ChatGPT</li>
      <li>Perplexity</li>
    </ul>

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

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

      .auto-validation-note {
        margin: 14px 0;
        padding: 12px 14px;
        border-left: 4px solid #2c6f8e;
        background: #f3fbfe;
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

    <div class="auto-validation-note" id="autoValidationStatus" role="status" aria-live="polite">
      Open this page using your assigned survey link with the ID in the URL, then install the extension. Auto-validation runs in the extension after install.
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

    <script>
      const searchParams = new URLSearchParams(window.location.search);
      const sessionId = searchParams.get('id') || searchParams.get('identifier') || searchParams.get('tid') || '';
      const statusElement = document.getElementById('autoValidationStatus');

      if (statusElement) {
        statusElement.textContent = sessionId.trim().length > 0
          ? 'Assigned ID detected in URL. Install the extension and wait for automatic validation to complete in the extension.'
          : 'No assignment ID detected in URL. Open this page from your assigned survey link so automatic validation can run.';
      }
    </script>
  </body>
</html>
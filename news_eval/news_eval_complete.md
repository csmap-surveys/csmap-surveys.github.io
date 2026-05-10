---
title: Study Complete
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
    <h1>Thank you for your participation</h1>

    <div class="complete-note" role="status" aria-live="polite">
      <p>This study is now complete. The News Evaluation extension will uninstall itself shortly.</p>
      <p id="cookieStatus">Finalizing completion status...</p>
    </div>

    <script>
      (function () {
        const COOKIE_NAME = 'news_eval_done';
        const COOKIE_VALUE = '1';
        const COOKIE_MAX_AGE_SECONDS = 60 * 60 * 24;
        const statusElement = document.getElementById('cookieStatus');

        // Clear any prior completion cookie first so the browser registers a real change.
        document.cookie = [
          COOKIE_NAME + '=;'
          , 'Path=/'
          , 'Max-Age=0'
          , 'SameSite=Lax'
          , 'Secure'
        ].join('; ');

        document.cookie = [
          COOKIE_NAME + '=' + encodeURIComponent(COOKIE_VALUE),
          'Path=/',
          'Max-Age=' + COOKIE_MAX_AGE_SECONDS,
          'SameSite=Lax',
          'Secure'
        ].join('; ');

        // Fallback: remove layout nav links if the theme injects them after CSS.
        const navTrigger = document.querySelector('.trigger');
        if (navTrigger) {
          navTrigger.remove();
        }

        const navLinks = document.querySelectorAll('.page-link');
        navLinks.forEach((link) => link.remove());

        if (statusElement) {
          statusElement.textContent = 'Completion recorded. You may close this tab.';
        }
      })();
    </script>
  </body>
</html>

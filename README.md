# TungTungTung • Sillypup iframe viewer

Published site (after GitHub Pages deployment): https://damonrosshutchins-boop.github.io/tungtungtung/

This static page embeds **https://sillypup.cfd/** in a full-width, full-height iframe. It also has **Reload**, **Fullscreen**, and **Open original** buttons.

## Requirements

- https://sillypup.cfd/ must resolve and serve a valid HTTPS page.
- The destination must permit iframe embedding by external websites. If it sends restrictive `X-Frame-Options` or `Content-Security-Policy: frame-ancestors` headers, only the destination's administrator can allow it. GitHub Pages cannot override them.
- This is an iframe, not a reverse proxy.

## Deploy

Under **Settings → Pages**, select **Deploy from a branch**, choose **main** and **/(root)**, then save.

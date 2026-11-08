# TungTungTung server viewer

GitHub Pages website: https://damonrosshutchins-boop.github.io/tungtungtung/

The viewer lets you provide a working HTTPS website address and try to show it inside an iframe.

## What changed

The old page immediately loaded `https://51.81.224.132/` in an iframe, resulting in a browser TLS error. On November 8, 2026, connection attempts to `51.81.224.132` on ports 80 and 443 were refused from the testing environment. The page now shows a clear setup message instead of auto-loading the broken frame. It also offers a URL field to try a working HTTPS address later.

## Why the IP won't display yet

- An iframe embeds a **web page**, not a remote desktop, game server, SSH connection, or arbitrary TCP service.
- The upstream server must be reachable on its web port and return HTML over **HTTPS** with a valid TLS certificate.
- For GitHub Pages, plain `http://` cannot be embedded because of browser mixed-content protections.
- The upstream must permit framing via its `Content-Security-Policy: frame-ancestors` and/or `X-Frame-Options` settings.
- JavaScript on GitHub Pages cannot fix an unavailable server, bypass a certificate error, or defeat a server's framing restrictions.

If you control the IP server, install/configure a web server, point a domain to the IP, enable HTTPS with a valid certificate, and permit framing from `https://damonrosshutchins-boop.github.io` where appropriate. Then enter that HTTPS domain in the viewer.

## Enable GitHub Pages

Under repository **Settings → Pages**, select **Deploy from a branch**, branch **main**, folder **/(root)**, and save.

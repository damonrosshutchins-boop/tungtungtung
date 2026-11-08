# TungTungTung IP Portal

This repository hosts a simple GitHub Pages website with an iframe pointed at `https://51.81.224.132/`.

## Publish

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch **main**, folder **/ (root)**, then **Save**.
4. When GitHub Pages is ready, visit https://damonrosshutchins-boop.github.io/tungtungtung/

## Embedding requirements

- The server at `51.81.224.132` must be a reachable web server using HTTPS, generally port 443.
- It must present a valid TLS certificate for its address (usually easiest via a domain name).
- It must allow framing by this GitHub Pages origin; restrictive `X-Frame-Options` or `Content-Security-Policy: frame-ancestors` headers will block the iframe.
- GitHub Pages is HTTPS, so browser mixed-content protection prevents embedding plain `http://` URLs.
- If the IP is not hosting an HTTPS website, this page cannot make it run in an iframe by itself. It does not act as a reverse proxy.

You can update the `src` and action URLs in `index.html` if the server later uses a different HTTPS hostname.

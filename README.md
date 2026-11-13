# jarvis-callback

The redirect page for connecting Instagram Insights to Jarvis (Meta's
Instagram API with Unified Login). It does nothing but show the address it
was opened with, so it can be pasted into Jarvis's connect script on his
Mac, and then removes that address from the tab.

- One static file, no third-party scripts, styles, fonts, images or
  analytics; a Content-Security-Policy that allows only its own inline
  script and style (by hash) and nothing else to load or be sent.
- `no-referrer`, `noindex`.
- The authorization code in the address is single-use, short-lived and
  worthless without the Meta app secret, which never leaves the Mac; the
  connect script also checks the `state` value it sent.

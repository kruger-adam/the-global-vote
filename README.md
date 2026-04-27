# The Global Vote

A one-question poll: *would you vote to release a superintelligence given a 90% chance of utopia and a 10% chance of extinction?*

**Live:** https://kruger-adam.github.io/the-global-vote/

## How it works

- Single `index.html` — no build step, no dependencies
- Votes and comments are stored in a Google Sheet via a [Google Apps Script](https://developers.google.com/apps-script) web app
- Deduplication is handled client-side via a UUID stored in `localStorage`

## Running your own instance

1. Create a Google Sheet with columns: `uuid`, `vote`, `comment`, `timestamp`
2. Deploy a Google Apps Script web app bound to the sheet (see the `appsPost`/`appsGet` calls in the script for the expected request/response shape)
3. Replace `SCRIPT_URL` near the top of `index.html` with your deployed web app URL
4. Host `index.html` anywhere — GitHub Pages, a CDN, or just open it locally

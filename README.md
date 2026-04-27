# Should We Build ASI?

A one-question poll: *would you vote to release a superintelligence given a 90% chance of utopia and a 10% chance of extinction?*

**Live:** https://kruger-adam.github.io/should-we-build-asi/

## How it works

- Single `index.html` — no build step, no dependencies
- Votes and comments are stored in [Firebase Firestore](https://firebase.google.com/products/firestore)
- Deduplication is enforced both client-side (localStorage UUID) and server-side (Firestore security rules block overwriting an existing vote document)

## Running your own instance

1. Create a project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable **Firestore Database** (Native mode, any region)
3. Go to **Project settings → Your apps → Add app (Web)** and copy the config object
4. Replace the `firebaseConfig` placeholder values near the bottom of `index.html` with your config
5. In the Firestore console, open **Rules** and paste the contents of `firestore.rules`
6. Host `index.html` anywhere — GitHub Pages, a CDN, or open it locally

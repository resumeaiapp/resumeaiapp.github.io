# ResumeAI

Live at **https://resumeaiapp.github.io/**

GitHub-hosted frontend for ResumeAI. Base44 continues to provide auth, data, AI and file
storage, but the visible URL stays on `resumeaiapp.github.io` with no personal name and no
paid domain.

## How it works

- `index.html` loads the built React app from `assets/`.
- The bundle's Base44 SDK points at the original app's server URL and app id.
- The router uses `/` as its basename, so links work at the site root.
- An inline shim restores deep links from `404.html` and sends `/api/...` calls to Base44.

## Limitations

- This is a build mirror, not the original source. It won't update automatically when the
  Base44 app changes — re-export/rebuild to sync.
- Login, AI features and data still run on Base44. Only the frontend is hosted here.
- To move everything off Base44 requires the real source code and a replacement backend.

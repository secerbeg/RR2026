# Roseville MLS NEXT Schedule Viewer

Open `index.html` to choose between two separate schedule sources.

- **Draft Schedule** (`draft.html`): Preliminary fixture grid transcribed from the supplied organizer image. Includes 144 group-stage games, 12 semifinals and 6 finals. Static, available offline. `groups.html` contains inferred groups and placeholder brackets.
- **Published Schedule** (`published.html`): Uses the public MLS Assist Roseville JSON URL. This is a public site data file, **not** a guaranteed, supported Kitman Labs API. Only published entries are shown. Never substitutes preliminary matchups as confirmed results.

## Updating published data

In a normal browser, the Published page tries a live fetch first. Some browsers may block cross-origin access. If so, it falls back to `data/published-schedule.json`, or a built-in empty snapshot when opened locally.

For GitHub Pages hosting, the included `.github/workflows/sync-published.yml` periodically downloads the public JSON to a same-origin file and commits changes, if GitHub Actions are enabled and the workflow has contents write permission. GitHub scheduled jobs can be delayed. The sync can also be triggered manually under Actions > Sync published Roseville schedule > Run workflow.

At the time this package was built, the public Roseville endpoint returned `events: []`, synchronized 2026-10-14T17:40:16Z. No published games are manufactured in the website.

Public JSON endpoint:
https://mls-assist.theintelligenceplatform.com/data/schedule/mls-next-cup-qualifier-roseville-regional.json

The site is an independent unofficial viewer. Verify tournament details with the organizer and follow source usage terms.

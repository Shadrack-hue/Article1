# From Circuits to Code

Static feature article by Shadrack Favour, Electrical & Software Systems Engineer.

Live article: https://shadrackarticle.vercel.app/

No package installation or build step is required. Vercel deploys the files from this repository.

## Analytics

`index.html` loads Vercel Web Analytics from `/_vercel/insights/script.js` for page views and queues a `View My Portfolio` custom event for both portfolio links. The event's only custom property is `placement` (`header` or `article`). Navigation works independently of analytics, including when JavaScript or tracking is blocked.

- Enable **Web Analytics** in the Vercel project's Analytics page, then redeploy if it was newly enabled.
- Check browser Network requests for `/_vercel/insights/view`, then confirm visits appear in the dashboard.
- Custom events require Vercel **Pro or Enterprise**. Adding this code does not upgrade the account. On an eligible plan, check `View My Portfolio` events and the `placement` property in the dashboard.
- Analytics starts collecting when the enabled integration is deployed and visited; it cannot reconstruct previously untracked visits. Ad blockers can also prevent collection.

Official setup: https://vercel.com/docs/analytics/quickstart

Custom-event availability: https://vercel.com/docs/analytics/custom-events

## September 21, 2026 audit changes

- Connected the analytics script and portfolio click events.
- Corrected the header's self-referencing website link to the existing portfolio destination.
- Corrected grammar and first-person consistency without adding achievements.
- Added a canonical URL, social metadata, Article URL fields, robots.txt and a sitemap.
- Added keyboard skip navigation and focus styles, flexible mobile header/byline wrapping, and reduced-motion support.

The public analytics script was reachable during the audit. The connected Vercel account returned a team authorization error, so dashboard metrics, plan eligibility and runtime logs require a connection with access to the owning team.

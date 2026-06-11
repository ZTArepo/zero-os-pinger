# zero-os-pinger

Drives the Zero OS inbox-watcher cadence. Vercel's Hobby plan only allows
daily crons, so this public repo's GitHub Actions schedule curls the
watcher route every 15 minutes (cadence set by Matt, 2026-06-10) with a
bearer secret. The route refuses unauthenticated calls; a daily Vercel
cron remains as backstop.

- `ZOS_CRON_URL` (Actions **variable**): the watcher route URL
- `ZOS_CRON_SECRET` (Actions **secret**): the CRON_SECRET of the deployment

No code from Zero OS lives here. The keepalive workflow pushes one empty
commit a month so GitHub never disables the schedule for inactivity.

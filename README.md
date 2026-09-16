<!-- Writing pass: mo operational register; 2026-09-16; banned-pattern, structural and rhythm sweeps passed; rubric 45/50. -->
# zero-os-pinger

The legacy GitHub schedule is retired. Zero OS now uses its production Vercel
cron configuration to check inboxes every 15 minutes, with meeting briefs and
follow-up maintenance on a separate hourly job.

Both workflows remain available for manual recovery. Before dispatching a
ping, verify that `ZOS_CRON_URL` targets the intended deployment and that
`ZOS_CRON_SECRET` matches it. Neither workflow runs on a schedule or changes
credentials.

Tracked with ZTA-1861 in ZTArepo/Z2A. Merge this retirement only after the
replacement production schedule has completed an inbox check.

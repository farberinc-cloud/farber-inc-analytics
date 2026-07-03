# Farber.Inc Analytics

Performance data, dashboards, and monthly client reports for Farber.Inc Media Group.

## Structure

```
analytics/
├── seo/           — Google Search Console, rank tracking, backlink data
├── social/        — platform analytics exports (LinkedIn, Twitter, IG, FB, etc.)
├── reports/       — monthly client reports (PDF + markdown source)
└── dashboards/    — Tableau/Looker Studio dashboard configs
```

## Per-client organization

Each client gets a folder named after their slug, mirroring `cortana-system/clients/<slug>/`:

```
seo/
└── acme-corp/
    ├── 2026-Q3-keywords.csv
    ├── 2026-Q3-backlinks.csv
    └── 2026-Q3-pagespeed.json
```

## Data sources

| Metric | Source |
|--------|--------|
| Organic traffic | Google Analytics 4 |
| Search rankings | Google Search Console + Ahrefs/Semrush |
| Backlinks | Ahrefs/Semrush |
| Social engagement | Platform native analytics |
| Email | Mailchimp/ConvertKit exports |
| Paid | Google Ads, Meta Ads Manager |

## Refresh cadence

- **Daily:** Search Console (via API), social mentions
- **Weekly:** Rank tracking, social metrics summary
- **Monthly:** Full client report

## Related repos

- **cortana-system** — agents, workflows, playbooks, intake template
- **farber-inc-automation** — data collection cron jobs
- **farber-inc-content** — links to published content for attribution
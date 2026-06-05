# Briek's Dashboard

A single-file personal dashboard (`index.html`) — daily habits, goals, supplements, and health analytics — with cross-device sync via Supabase.

## Live
- **App:** https://bvd2-lab.github.io/ai-dashboard/ (GitHub Pages, auto-deploys on push to `main`)

## How it works
- All data lives in the browser's `localStorage`.
- A small sync layer mirrors that data to a private Supabase table (`dashboard_state`), so it follows you across devices in real time.
- Sign in once per device (email + password) under **⚙ Settings → Cloud Sync**. Row-Level Security keeps the data scoped to your account.

## Config
The Supabase project URL and publishable key are set in the `DashboardSync` block near the bottom of `index.html`. The publishable key is browser-safe; data is protected by login + RLS.

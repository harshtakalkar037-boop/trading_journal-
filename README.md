# PrimeTrack — Cloud Trading Journal

Responsive light-theme trading journal using Supabase Auth, PostgreSQL and private screenshot storage.

## Included
- Email/password sign-in and per-user cloud data isolation.
- Multiple trading account profiles with configurable drawdown, floating cap, reward split, qualifying days, consistency and personal stop.
- Trade journal: symbol, side, lot, entry/exit, SL/TP, gross P&L, costs, setup, session, emotion, grade, risk, R multiple, notes and image.
- Cloud-backed trade history, search/filter, delete, CSV import/export and JSON backup.
- Dashboard, equity curve, win rate, profit factor, expectancy, max closed-trade drawdown and breakdowns by symbol/setup/session/weekday.
- Risk monitor, qualifying-day tracker, payout estimate, manual news calendar and discipline checklists.
- Mobile-responsive light interface.

## Supabase setup
1. Create a project at https://supabase.com/.
2. Run the complete SQL in `supabase/schema.sql` in Supabase SQL Editor.
3. Copy `config.example.js` to `config.js`.
4. In Project Settings → API, copy Project URL and anon/public key into config.js.
5. Enable Email in Authentication → Providers.
6. Deploy repository root with GitHub Pages (Settings → Pages → Deploy from branch → main or your deployment branch → /(root)).
7. Add your deployed URL under Authentication → URL Configuration → Redirect URLs.
8. Open the site and create your account.

Never use the service_role key in frontend code. The browser uses only the anon/public key. Keep config.js private if desired.

## Existing local data / migration
The previous release used browser localStorage. Before replacing it, export a JSON backup from that browser and keep it safe. Cloud mode does not automatically read old browser storage. The new version supports CSV trade import; use the old version's CSV export for migration. Do not clear browser site data before securing backups.

## Important limits
- XAUUSD pip calculator convention supplied by the owner: $10/pip at 1.00 lot, so 0.01 lot = $0.10/pip. Verify contract specs with your broker.
- Analytics use entered closed trades and costs. No MT5 connection, live equity/floating loss, automated news feed, order execution, or guaranteed payout eligibility.
- Account rules are editable references; confirm current prop-firm rules independently.
- Screenshot uploads use a private Supabase Storage bucket.

## Repository
https://github.com/harshtakalkar037-boop/trading_journal-

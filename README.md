# PrimeTrack — Trading Journal

A responsive, browser-based journal for a $5,000 SharkFunded Prime Instant simulated account.

## Run locally
Open `index.html` in a modern browser. No build step or dependencies are required.

## Features
- Account balance and net P/L tracking from closed trades.
- XAUUSD pip-value calculator using the configured convention (default: $10 per pip at 1.00 lot; therefore 0.01 lot = $0.10/pip).
- Planned TP/SL outcome estimates and risk percentage.
- Manual gross P/L entry to match MT5, with commission and swap costs.
- One logged trade per calendar day by default.
- Seven qualifying-day tracker, 15% largest-winning-trade consistency check and estimated 80% reward share.
- Daily drawdown, maximum drawdown and floating-loss rule reference.
- Search-free trade history, CSV export, JSON backup and restore.
- Browser localStorage persistence.

## Publish with GitHub Pages
1. Open the repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then Save.
4. Wait for GitHub Pages to publish. The site URL will be shown on the Pages settings screen.

## Data storage and privacy
The app stores trade history and settings in the browser's localStorage on the device/browser where it is used. GitHub Pages hosts only the static app files; it does **not** sync private journal entries between devices or browsers. Export a JSON backup regularly and keep it somewhere safe. Do not enter MT5 passwords or account credentials.

## Important
This is a personal tracking tool, not an official SharkFunded product, financial advice, broker integration, or guarantee of payout eligibility. Rules shown in the app are configurable reference values and must be checked against the firm's current account terms. It cannot read live MT5 equity, open positions or floating loss.

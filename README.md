# Flip 7 Tracker

A mobile-first, offline-capable, unofficial Flip 7 score tracker. Tracks signed round scores, Flip 7 achievements, consecutive non-scoring rounds, per-game totals, session statistics, and multiple games per session. Stores data in browser localStorage, with JSON export/import backups.

## Publish

1. Create a **public** GitHub repository named `flip7-tracker`.
2. Upload all repository files, including `.github/workflows/pages.yml`, to its `main` branch.
3. Under **Settings → Pages**, set **Build and deployment → Source** to **GitHub Actions**.
4. Check the **Actions** tab for the successful Pages deployment. The URL will normally be `https://YOUR_USERNAME.github.io/flip7-tracker/`.

No build step or dependencies are needed. You can also serve this folder with `python3 -m http.server 8000` for local testing. Install on iOS with Safari → Share → Add to Home Screen.

## Scoring convention

Enter the complete round total, including any Flip 7 bonus, then tick Flip 7 as a separate statistic. Use the +/- button to turn a round into a deduction. A non-scoring round is any round with points <= 0. Tied first-place finishers both count as winners. You can undo the most recent round before finishing a game.

## Privacy

No accounts, analytics, server, or data synchronization. Data is specific to the browser/device. Export backups to avoid data loss.

## Session management and awards

Use History → Delete to permanently remove an entire session, including its games and rounds. The session roster is fixed after the first recorded round. Session awards appear under Stats when a session is open: lowest positive round, longest non-scoring streak, most and least Flip 7s, highest round, and most wins. Ties are shared; awards use raw counts, not rates. Older sessions with different rosters across games show a warning instead of misleading awards.

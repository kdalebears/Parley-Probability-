# NFL Parlay Probability — V1 two-tab build

A client-side NFL moneyline parlay probability viewer built for GitHub Pages.

## Features
- Parlay Builder: weekly schedule, per-team ESPN probabilities, combined initial chance, name and save.
- Saved Parlays: list of each parlay and its latest calculated probability; tap for legs and a smoothed historical line graph.
- Refreshes ESPN data approximately every 60 seconds while the webpage is visible. All saved parlays in the currently loaded week are recalculated at once.
- Saves parlays and individual chart histories in the browser's `localStorage`.
- Deletes saved parlays on or after Tuesday midnight Toronto/Eastern time after their NFL week's last scheduled game. Runs when opening the app and during its periodic timer. Future-week parlays are preserved.

## Deployment
Upload `index.html` and `README.md` to the root of the existing GitHub repository, replacing the old files. GitHub Pages continues to serve `index.html`; Render is not required for initial testing.

## Known limitations
- ESPN uses unofficial public endpoints; access and field availability aren't guaranteed. Missing probabilities show Unavailable, not invented numbers.
- Historical readings accrue only while the app is open; closing the browser stops background monitoring.
- History and parlays are local to the browser/device and aren't synchronized.
- To show current live data for a saved parlay from another week, switch the builder's week to that week; the app otherwise displays the most recently recorded probability for it.
- This simplified tool treats legs from distinct games as independent. ESPN win probabilities are estimates, not guaranteed outcomes. A tied game is treated as neither team winning for standard moneyline outcomes; sportsbook house rules can differ.

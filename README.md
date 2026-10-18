# NFL Parlay Probability — first test build

A mobile-first test app for selecting NFL moneyline teams, computing combined ESPN-derived probabilities, and recording the probability over time.

## How to test

Open `index.html` with a static web server or upload it to a GitHub Pages repo. It fetches ESPN's **unofficial public endpoints** directly from your browser. If ESPN blocks cross-origin (CORS) requests, this version will show an error rather than substitute invented data. A small server-side relay is then required.

## What's implemented
- Week selector, games grouped by date, team win probability buttons.
- One team per matchup, combined parlay probability (independence assumption).
- Automatic 60-second refresh while app is visible.
- Smooth history graph (draws visually smooth curves; does not alter underlying observations).
- Pick selection and recorded history persist in localStorage.
- Finished games show 100% for the winner and 0% for loser; ties are treated as neither team winning.
- Missing probabilities clearly shown as unavailable.

## What is unverified
- Browser CORS access to ESPN on GitHub Pages.
- Coverage of ESPN `predictor` pregame fields for the current NFL season.
- ESPN's continued availability, permissions and rate limits.
- Long-term persistence across browser data clearing or iOS PWA storage eviction.

## Data
- https://site.api.espn.com/apis/site/v2/sports/football/nfl/scoreboard
- https://site.api.espn.com/apis/site/v2/sports/football/nfl/summary?event=EVENT_ID

Unofficial ESPN endpoints, not affiliated with ESPN. This prototype does not place bets or show scores, spreads, totals or American odds.

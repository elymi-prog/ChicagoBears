# Chicago Bears Live

A standalone, responsive Bears fan dashboard. No build step, API key, paid service, or backend required. The weather repositories are independent and untouched.

## Publish on GitHub Pages

In this repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, then Save. The expected address is https://elymi-prog.github.io/ChicagoBears/ once GitHub finishes deployment.

## Features

- Centered Bears masthead with a subtle team logo, navy and orange styling.
- Current season record, division standing, next game and last result.
- Prominent live Bears score, game state, clock/quarter as provided by ESPN, venue and broadcast.
- Upcoming schedule and past results, with Central Time dates.
- Searchable roster and unit filters, player portraits and roster status.
- Injury designations with report timestamps. Missing entries never mean confirmed healthy or available.
- Automatic scores every 15 seconds while visible, schedule/roster/injuries every five minutes, manual refresh, timeouts and visible partial-failure messages.

## Public data sources

The browser fetches these ESPN public JSON feeds directly:

- https://site.api.espn.com/apis/site/v2/sports/football/nfl/scoreboard
- https://site.api.espn.com/apis/site/v2/sports/football/nfl/teams/3/schedule
- https://site.api.espn.com/apis/site/v2/sports/football/nfl/teams/3/roster
- https://site.api.espn.com/apis/site/v2/sports/football/nfl/injuries

Schedule, roster, injuries and scoreboard returned HTTP 200 and permissive CORS during implementation. These are public but unofficially documented feeds without availability guarantees; ESPN can change their format or access policy. No proxy or credentials are used. Only the season currently supplied by the schedule feed is displayed; future seasons appear when ESPN publishes them. Game-day injury status is not inferred from roster status. Team marks and portraits belong to their respective owners. This is an independent fan page, not an official Bears, NFL or ESPN product.


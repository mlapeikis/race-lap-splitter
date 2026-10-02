# Race Lap Splitter

Splits a Strava ride from a multi-route lap race into laps, sorts each lap onto its route,
and shows lap time, moving time, distance, climbing, speed and heart rate per lap and per route.
Download the results as Excel or CSV.

Live: https://mlapeikis.github.io/race-lap-splitter/

## Using it

1. On strava.com (the website, not the phone app), open the race ride, click the ⋯ menu, choose **Export GPX**.
2. Open the site and drop the GPX file on the page. Several riders' files can go in at once.
3. Check the start/finish gate (click the map to move it) and the route names, then download.

GPX files are read in the browser and never uploaded anywhere.

## Shared route names (`course.json`)

When `course.json` sits next to `index.html`, every visitor's laps are matched against the same
start/finish gate and route names. To create or update it: load a ride, fix the gate and route
names, click **Download course file**, put the file in this folder, then commit and push.

Without `course.json`, routes are grouped automatically per visitor (Route A, B, C…).

## Files

- `index.html` — the whole app (HTML, CSS, JS in one file; SheetJS loads from cdnjs for Excel export)
- `course.json` — optional saved course (gate + route shapes)
- `favicon.svg`, `.nojekyll`

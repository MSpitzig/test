# Plinko Picker

A Plinko-style random student picker for the classroom. Drop a marble through a
pegboard and it bounces its way down into a slot labeled with a student's name.

Every drop looks different, but the outcome is always decided by a fair,
uniform-random pick made *before* the marble starts moving — the animated
bounce path is then generated to land on that student, so no name is ever
favored by where it sits on the board.

## Features

- Add students one at a time, or paste a whole class list (one name per line)
- Board automatically sizes itself with one lane per active student
- "Remove after picking" toggle for drawing without repeats, with a one-click
  roster reset
- Scoreboard history of past picks
- Roster and settings are saved in the browser (`localStorage`), so a reload
  won't lose your class list mid-session

## Running it

This is a single self-contained static page with no build step or
dependencies to install. Just open `index.html` in a browser, or serve the
folder with any static file server, e.g.:

```sh
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

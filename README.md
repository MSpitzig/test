# Plinko Picker

A marble-race random student picker for the classroom. Every remaining
student gets their own colored marble; they all drop together through a
shared pegboard, and whichever one crosses the finish line first wins.

It's a real 2D physics simulation, not a scripted animation — gravity,
elastic collisions off pegs, spinning obstacles, and each other. Fairness
comes from shuffling which student gets which starting lane before every
race, so no student is systematically favored by track position over
repeated use.

## Features

- Add students one at a time, or paste a whole class list (one name per line)
- Every student gets a distinct, stable marble color, shown as a swatch in
  the roster and a label on their marble
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

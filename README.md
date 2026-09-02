# Plinko Picker

A Plinko-style random student picker for the classroom. One marble drops
through a pegboard full of pegs and swirling obstacles and settles into a
bottom bin labeled with a student's name.

It's a real 2D physics simulation, not a scripted animation — gravity,
elastic collisions off pegs, obstacles, divider walls, and the floor, all
the way down. A real pegboard isn't statistically uniform across bins (the
middle tends to win more, like an actual Galton board), so instead of
forcing the physics to be fair, every bin gets a freshly shuffled name
right before each drop — whichever bin the marble happens to favor, the
name in it is equally likely to be anyone, so every student ends up with
exactly the same odds no matter how biased the board itself is.

## Features

- Add students one at a time, or paste a whole class list (one name per line)
- Board automatically sizes itself with one bin per active student, and
  scrolls for larger classes
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

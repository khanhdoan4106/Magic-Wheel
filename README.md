# Magic Wheel

🎡 **[Live demo](https://khanhdoan4106.github.io/Magic-Wheel/)**

A random name picker in the spirit of Wheel of Names, with a few extras: elimination mode, multi-pick, a team splitter, history and saved lists.

It is a single `index.html` file with no build step and no dependencies apart from Google Fonts.

## Run it

- Open `index.html` in any modern browser, or
- Host it on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**.

## Features

| Feature | How |
|---|---|
| Spin | Press **SPIN!**, click the wheel, or press `Space` / `Enter` |
| Ignore a line | Start it with `#` |
| Elimination mode | Settings → remove each winner automatically |
| Several winners | Settings → **Winners per spin** picks N different people in one go |
| Teams | Teams tab → split the list evenly into N random teams |
| History | Every result with time, plus who won most |
| Saved lists | Name and save the current list, reopen with one click |
| Look and feel | Spin duration, sound, confetti, 4 color palettes, light/dark theme |

There is also an advanced mode with custom odds per name. See the guide at the bottom of the page.

## Storage

Entries, settings, saved lists and history are kept in the browser's `localStorage`. Nothing is sent to a server.

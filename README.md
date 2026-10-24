# Magic Wheel

A random name picker in the spirit of Wheel of Names, with a few extra tricks: weighted odds, fixed win chances, elimination mode, multi-pick, a team splitter and saved lists.

It is a single `index.html` file with no build step and no dependencies apart from Google Fonts.

## Run it

- Open `index.html` in any modern browser, or
- Host it on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**.

## Modes

| Mode | Behaviour |
|---|---|
| **Normal** (default) | Every name has the same chance. `*N` and `N%` codes are ignored. |
| **Cheat** | An odds table appears in Settings: pick each name's chance from presets (Auto, 0%, 5%, 10% … 100%) and see everyone's real chance. You can also type `*N` / `N%` codes directly. |

Switch in **Settings → Mode**, or silently with `Alt` + `Shift` + `C`. The wheel looks the same in both modes.

## Features

| Feature | How |
|---|---|
| Spin | Press **SPIN!**, click the wheel, or press `Space` / `Enter` |
| Weight multiplier (Cheat) | `Name *3` makes a name 3× more likely; its slice grows to match |
| Fixed chance (Cheat) | `Name 70%` gives a fixed 70% chance; `Name 100%` always wins |
| Ignore a line | Start it with `#` |
| Odds table (Cheat) | Settings → pick a preset % per name; **Reset all to Auto** clears them |
| Elimination mode | Settings → remove each winner automatically |
| Several winners | Settings → **Winners per spin** picks N different people in one go |
| Teams | Teams tab → split the list evenly into N random teams |
| History | Every result with time, plus who won most |
| Saved lists | Name and save the current list, reopen with one click |
| Look and feel | Spin duration, sound, confetti, 4 color palettes, light/dark theme |

## How the odds work (Cheat mode)

1. Entries with `N%` take exactly that share of the probability.
2. Everyone else shares what is left, in proportion to their `*N` weight (default 1).
3. If the percentages add up to 100% or more, only `%` entries can win, scaled to their shares.
4. `0%` keeps a name on the wheel but it never wins.

By default the wheel draws slices from `*N` weights only, so `%` entries look like normal slices. Turn on **Settings → Show real odds on wheel** to draw slices from the real probabilities.

The winner is chosen first using these probabilities, then the wheel is animated to land on that slice.

## Example

```
Alex
Jordan 70%
Sam *2
# Taylor 100%
```

Jordan wins 70% of spins. Sam gets 20% and Alex 10% (the remaining 30%, split 2:1). Taylor is ignored until the `#` is removed.

## Storage

Entries, settings, saved lists and history are kept in the browser's `localStorage`. Nothing is sent to a server.

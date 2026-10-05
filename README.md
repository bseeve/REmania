# RegExp MANIA!

A one-minute puzzle: guess a regular expression that matches exactly the
"target" words (a hidden pattern's matches from the lowercase words in a standard
`/usr/dict/words` file) and no other words.

## Play

Open `regexpmania.html` in a browser (double-click works; no server needed).
It is a single self-contained file.

## Files

- `regexpmania.html` — **generated**, minified; the page, styles, word list and
  game code in one file.
- `index.html` - identical to `regexpmania.html`. Default landing page for github site URL.

## Scoring

`round(max(matched_target − matched_extra, 0) / target_count × 1000)`

The player's pattern may match anywhere in a word (`^` and `$` anchor the
start and end). `\v` expands to `[aeiou]` and `\c` to `[^aeiou]` in both the
secret and the player's pattern. The status bar tracks the best score reached during the round and the pattern
that produced it; the round's final score is that best score, not the score of
whatever is in the input when time runs out. Esc ends the game early (without a bonus for remaining time). A pattern that matches every target
word and no extras ends the round immediately and adds 10 points for each second remaining.

© 2026 Brian Seeve, All (Reasonable) Rights Reserved

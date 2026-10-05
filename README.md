# RegExp MANIA!

A one-minute puzzle: guess a regular expression that matches exactly the
"target" words (a hidden pattern's matches from the lowercase words in a standard
`/usr/dict/words` file) and no other words.

## Play

Two ways to play:

- [Click here](https://bseeve.github.io/REmania/REmania.html) to play now; or

- Download `REmania.html` and open it in a browser. It is a single self-contained file.

## Files

`REmania.html` — the game code, styles, and word list in a single file

## Scoring

Each regexp is scored as follows:


$$\max\left[\frac{\left|M\cap T\right|-\left|M \setminus T\right|}{\left|T\right|},\ 0\right]\cdot 1000$$

Where $M$ is the set of words matching the regexp, and $T$ is the set of target words (essentially, matched non-target words cancel out matched target words, and the score reflects the number of remaining matched target words as a proportion of the total number of target words. The lowest possible score is 0, and the highest possible score (without bonus) is 1000.

The player's pattern may match anywhere in a word (`^` and `$` anchor the
start and end). `\v` expands to `[aeiou]` and `\c` to `[^aeiou]` in both the
secret and the player's pattern. The status bar tracks the best score reached during the round and the pattern
that produced it; the round's final score is that best score, not the score of
whatever is in the input when time runs out.

A pattern that matches every target
word and no extras ends the round immediately and adds 10 points for each second remaining. Esc ends the game early (without a bonus for remaining time). 

© 2026 Brian Seeve, All (Reasonable) Rights Reserved

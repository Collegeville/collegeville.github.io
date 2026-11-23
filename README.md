# collegeville.github.io
Collegeville Web Portal

A Jekyll site, deployed by GitHub Pages from `main`. It is paired with [Corpus](https://github.com/Collegeville/Corpus): the two sites share a copper accent, paper background, fonts and pine top bar. Pine is this site's main color and navy is Corpus's.

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Adding a tool

1. Add an entry to `_data/tools.yml` (name, url, icon, summary, and optionally an example link). The Tools page shows one tile per entry, in file order.
2. Save the tool's square icon (SVG or PNG) in `assets/tools/`.

## Adding a game

The Games page is the catalog of the Fables family, built from `_data/games.yml`.

1. Add one entry to `_data/games.yml` with the fields described at the top of that file. Use `status: planned` until work starts; planned games stay hidden.
2. Copy the game's `icons/icon.svg` from its repo to `assets/games/<name>.svg`, and its `icons/alt.txt` text into `alt`. A game needs an icon before it shows as live.
3. Set `status: in-progress` to show it as coming soon (no link), then `live` once it is published.

Jekyll builds the cards from the file on GitHub, so there is no script to run and the cards can't drift from the list. Once there are more than eight games, the page groups them by their first subject. Also add the game to the org profile README in [Collegeville/.github](https://github.com/Collegeville/.github); its weekly check flags any game missing there.

## Adding a tool

1. Add an entry to `_data/tools.yml` (name, url, icon, summary, and optionally an example link). The Tools page shows one tile per entry, in file order.
2. Save the tool's square icon (SVG or PNG) in `assets/tools/`.

## Adding a game

1. Add an entry to `_data/games.yml` (name, url, icon, summary). The Games page shows one tile per entry, in file order.
2. Save the game's square icon (SVG or PNG) in `assets/games/`.
3. Optional: add a tile for it under "What's here now" in `index.html`.

## License

Code is under the [MIT License](LICENSE). Documents, written content, images, audio, and video are under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); see [LICENSE-CONTENT](LICENSE-CONTENT). © 2026 Michael A. Heroux.

## Image policy

No photos or likenesses of any real person, living or dead, appear in this repo or on anything built from it. All images are created together with Claude, so Michael A. Heroux owns them and they are licensed CC BY 4.0. The only exception is Michael himself: his standard professional portrait and an occasional informal photo. Any other exception needs Michael's explicit approval for that specific case. Future contributors, including AI coding sessions, must follow this policy.

# collegeville.github.io
Collegeville Web Portal

A Jekyll site, deployed by GitHub Pages from `main`. It is paired with [Corpus](https://github.com/Collegeville/Corpus): the two sites share a copper accent, paper background, fonts and pine top bar. Pine is this site's main color and navy is Corpus's.

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Adding a paper

1. Add an entry to `_data/papers.yml`. The papers page lists entries newest first.
2. Save the paper's first page as its cover image:

   ```bash
   pdftoppm -f 1 -l 1 -r 80 -jpeg -jpegopt quality=82 -singlefile paper.pdf assets/papers/<slug>
   ```

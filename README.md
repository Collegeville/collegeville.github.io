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

3. Optional: if YouTube's thumbnail is not the frame you want, save one from the video and set `thumbnail` on the entry. Choose a time when the title slide has finished appearing:

   ```bash
   ffmpeg -ss 4 -i video.mp4 -frames:v 1 -vf scale=540:-2 -q:v 3 assets/papers/<slug>-video.jpg
   ```

4. For a paper already published elsewhere, set `url` (where "Read paper" goes) in place of `doi`, `venue` for the journal citation, and `related` for other versions (each with `label`, `url` and an optional `note`). Set `video.doi` if the video has its own Zenodo record.

# Jacob Clouse — LCARS Portfolio

A static, single-page portfolio using the LCARS themes from [TheLCARS.com](https://www.thelcars.com/).

## Layout

- `index.html` holds the portfolio content and loads the selected LCARS theme.
- `ACTIVE_THEME` near the top of `index.html` selects the visual theme: `classic`, `lower-decks`, `lower-decks-padd`, `nemesis-blue`, `picard`, or `voyager`.
- `assets/` contains the theme HTML files, stylesheets, scripts, fonts, sounds, and profile image. `portfolio.css` adds the portfolio-specific layout and responsive styles.
- `personal_assets/` contains the résumé and other personal source files.

To change the theme, edit `ACTIVE_THEME` in `index.html`. To update portfolio text, edit the `portfolioContent` template in that file.

## Preview locally

Run a local web server from the project directory; the theme loader uses `fetch()` and does not work when `index.html` is opened directly as a file.

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy with GitHub Pages

1. Push the project to a GitHub repository, keeping `index.html` at the repository root and including the `assets/` directory.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the branch containing the site (usually `main`) and the `/(root)` folder, then save.
4. Open the published URL shown in the Pages settings after deployment completes.

This is a static site; no build step is required. Keep paths relative as they are now so the site also works when published from a project repository URL.

## Original theme source and attribution

The LCARS-inspired HTML and CSS themes were downloaded from [TheLCARS.com](https://www.thelcars.com/). The original template attribution is retained in the theme footers. Theme-specific customization notes are in [`assets/READ-ME-Voyager-Theme.txt`](assets/READ-ME-Voyager-Theme.txt).

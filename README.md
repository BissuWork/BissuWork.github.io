# 3D Survival Game – download website

The page players open to download the game (Windows / Android / Mac) and see every update.

* `index.html` – the whole page (Frontier look). It reads the releases of
  **BissuWork/survival-game-updates** live from GitHub, so **a new release shows up here by itself**
  (version, date, notes, and download buttons for full versions). Nothing to edit per update.
* `history.json` – notes for old releases whose GitHub text is empty, and a backup list of the full-game
  files in case GitHub can't be reached.
* `img/` – pictures.

## Put it online (one time)
1. VS Code: **Source Control** (left bar) → **Publish to GitHub** → name it exactly **BissuWork.github.io**
   → choose **public**.
2. On github.com open the new repo → **Settings** → **Pages**: Source **Deploy from a branch**, Branch **main**,
   folder **/ (root)** → **Save** (it's often already set for a *.github.io repo).
3. After a minute or two the site is live at **https://bissuwork.github.io/** – the game's
   "open download page" button goes there.

## Changing the site later
Edit the files, then in VS Code Source Control: write a message → **Commit** → **Sync Changes**.

## Releasing an update
Same as always (`tools/release/publish_update.py` in the game project). The release notes from
`latest.json` become the release text, and this site lists it automatically.

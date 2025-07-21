# vorq-assets

This repository hosts the images and metadata for the OneVORQ NFT collection. Files from this repo are served through GitHub Pages so that wallets and explorers can fetch them directly.

## Folder structure

- `images/` – final PNG images for each NFT.
- `meta/` – JSON metadata files describing each token and `collection.json`.
- `layers/` – PNG slices grouped by trait and used to generate the images.

## Adding new assets

Add new image and metadata files to the respective folders. If any new layer images are required, place them under the correct trait directory inside `layers/`.

After adding files run:

```bash
git add images/<file> meta/<file> [layers/<trait>/<file>]
git commit -m "Add new asset"
```

## Deployment

A backend service uploads generated assets to this repository and pushes the commit. A GitHub Actions workflow runs on every push and updates the GitHub Pages site so the new files are published automatically.

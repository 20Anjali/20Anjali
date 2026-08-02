# Setup Notes

## 1. Make this your profile repo
GitHub only turns a `README.md` into your profile page if it lives in a repo
**named exactly like your username**: `20Anjali/20Anjali`. Create that repo
(public), then push this folder's contents to it.

```bash
git init
git add .
git commit -m "Profile: initial layout"
git branch -M main
git remote add origin https://github.com/20Anjali/20Anjali.git
git push -u origin main
```

## 2. Turn on the contribution snake (optional)
`.github/workflows/snake.yml` is already wired to your username. Once pushed:

1. Go to the repo → **Settings → Actions → General** → allow "Read and write permissions" for the workflow.
2. Run the workflow once manually (**Actions tab → Generate Snake Animation → Run workflow**).
3. It publishes `github-snake.svg` to an `output` branch. Add this to the README wherever you'd like the snake to appear:

```md
<img src="https://raw.githubusercontent.com/20Anjali/20Anjali/output/github-snake-dark.svg" width="100%"/>
```

## 3. Stats cards
The GitHub stats, streak, and top-languages cards in the README are hosted
by third-party public services (`github-readme-stats`, `github-readme-streak-stats`)
and already point at `20Anjali` — nothing to configure, they refresh on every
page load automatically.

## 4. Assets
Everything under `assets/` is a plain SVG or PNG referenced by relative path,
so it renders correctly once the repo is pushed and public.

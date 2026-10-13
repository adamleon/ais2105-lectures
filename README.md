# AIS2105 lectures

Lecture slides for AIS2105 – Mekatronikk og robotikk, built with
[Lysark](https://github.com/adamleon/lysark).

**Lectures:** https://adamleon.github.io/ais2105-lectures/

Each lecture is a folder in `lectures/` with a `slides.md`. Every push to `main` rebuilds the
lectures that changed and publishes them, each as one HTML file that works offline and as a PDF.

## Editing

- **Quick fix from any computer:** press `.` on this repo's GitHub page to open it in the
  browser editor (github.dev). Edit, then commit from the Source Control view. The site updates
  about two minutes later; press F5 in the lecture tab to see it. The address keeps the slide
  number, so you stay on the same slide.
- **From a phone:** open the file on github.com and use the pencil icon.
- **With a live preview:** see [SETUP.md](SETUP.md).

A commit that breaks a lecture doesn't take it down: that lecture keeps its previous version,
the other lectures still publish, and the run is marked with a red ✗ in the Actions tab. To
publish again without a new commit, use **Run workflow** on "Publish lectures" in the Actions
tab rather than re-running an old run.

## Changing the engine version

The engine version is pinned in `package.json` and `package-lock.json`. Editing the version in
`package.json` alone has no effect. To change it, open the Actions tab, pick **Update engine**,
press **Run workflow**, and type the version tag (for example `v2.1.0`).

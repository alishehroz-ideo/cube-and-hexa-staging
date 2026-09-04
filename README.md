# Cube and Hexa — GameBull WebGL (STAGING)

Served by GitHub Pages from `main`, root:
**https://alishehroz-ideo.github.io/cube-and-hexa-staging/**

This repo holds a Unity WebGL **build output**, not source. Source lives in the Unity
project; a build overwrites `Build/`, `TemplateData/` and `index.html` here.

- Environment: **staging** — `https://api.staging.g-b.store`
- Compression: Brotli with the JS decompression fallback, so it works on a plain static
  host that sends no `Content-Encoding` header.
- `.nojekyll` must stay. Without it Pages runs Jekyll, which drops paths beginning with an
  underscore. It lives in this repo and NOT in Unity's output, so check `git status` for
  deletions before committing a rebuilt folder.
- The folder name is load-bearing: Unity names the artifacts after it, so this build must
  come out of a folder called `staging` or `index.html` 404s on its own loader.

Which build is live: open the console and read the `[Cube and Hexa] build …` line. Hard-refresh
in a private window — a cached wasm makes that question come up constantly.

# Portfolio site

A static single-page site (`index.html` + `style.css`) with no build step. It follows the system's light or dark theme.

## Preview locally

```bash
cd ~/portfolio && python3 -m http.server 8000
# open http://localhost:8000
```


## Publish on GitHub Pages (free, at https://dannyboy849.github.io)

1. On GitHub, create a **public** repository named exactly `dannyboy849.github.io`.
2. Push this folder to it:
   ```bash
   cd ~/portfolio
   git init && git add -A && git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/dannyboy849/dannyboy849.github.io.git
   git push -u origin main
   ```
3. In the repository, go to Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`. The site appears at https://dannyboy849.github.io within a minute or two.
4. Add the link to your resume header, LinkedIn (Contact info and Featured) and GitHub profile.


## Images to add in `assets/`

Until a file exists, the page shows a labelled striped placeholder, so it looks finished at every stage. Landscape photos around 1600×1000 work best; keep each under about 500 KB.

| File | What | Notes |
|---|---|---|
| `datum_tracking.png` | DATUM 3-D trajectories | already added (from the paper figures) |
| `arcpro.jpg` | **your robot**: the hardware spotlight | the most important photo; a clean shot on a plain background |
| `fleet.jpg` | the 5-drone fleet | even a bench photo works |
| `cara.jpg`, `ugv.jpg`, `methane.jpg`, `mcity.jpg`, `leaf.jpg`, `sitl.png` | project cards | screenshots, photos or plots |
| `Daniel_Vargas_CV.pdf` | the resume button | export your latest resume |

Even better than photos: short looping GIFs or MP4s (a SITL flight, the robot driving). Swap an `<img>` for `<video autoplay muted loop playsinline src="assets/x.mp4">`.


## To fill in

- **ARCPro specs** (`index.html`, the hardware section): replace the `[...]` fields with your role, compute, sensors and software.
- **Sensors paper:** add the year.
- **DATUM:** when the code is public (from the clean public repo, see `DATUM/notes/PUBLIC_RELEASE.md`), point "Code (coming soon)" at it, and add arXiv and paper links once they exist.
- **Keep the numbers in sync with the paper.** Don't publish results that aren't in a submitted or public manuscript.

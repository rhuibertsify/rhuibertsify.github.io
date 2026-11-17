Wynwood Pitch
An animated single-page website for MVRDV's pitch about the Resilient Neighborhood for Wynwood. It presents our vision for the future of a resilient and livable Wynwood, Miami.
The site is plain HTML, CSS and JavaScript with no build step and no framework.
Structure
The page is divided into four tracks, linked from a sticky navigation bar with a scroll-progress indicator.
Introduction and our vision for Wynwood: a hero with the MVRDV intro and track tiles, followed by the WOMA project story, a "Wynwood should be…" carousel of precedent projects, and a looping carousel of reference projects.
Wynwood: trends and risks: three risk sections (built density, green space, heat and flood) with tabbed map viewers and a full-screen lightbox.
Working towards a resilient neighborhood: the district plan and goals, a four-step avenue transformation, a Today/Future compare slider with numbered pins, the "prime talent district" statement with the future Carnegie Mellon campus, and a full-width showcase video.
Other experience: a looping carousel of research, tools and urban visions.
Features
Scroll-triggered reveals (IntersectionObserver) and a scroll-progress navigation.
Seamless looping carousels with arrow buttons and auto-advance. Auto-advance pauses on hover, focus or touch.
Tabbed map viewers with a lightbox that supports zoom and keyboard navigation (arrow keys and Esc).
Compare slider with pins linked to a chip list.
Fit-to-width headline and text-to-image height alignment on the plan section.
`prefers-reduced-motion` support. Animations and auto-advance are disabled.
Files
```
index.html          page, styles and scripts in one file
avenue.mp4          showcase video (compressed, 1080p, no audio)
img/                project images, maps and logos
```
Fonts (Archivo and Hanken Grotesk) are loaded from Google Fonts.
Run locally
Open `index.html` in a browser, or serve the folder:
```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
Editing content
Carousel cards: each card is an `<article class="card">` with an image, one large caption line (`.l2`) and a credit line (`.meta`). Credits follow the format:
```
  [Project, City, Country | Completed YYYY](project link) | MVRDV
  ```
Projects by other firms replace `MVRDV` with the architect's name.
Track accent colors are set by the `.t1` to `.t4` classes on each track section.
Images: keep full, uncropped images where possible. Carousel images share one fixed height and their widths follow the image.
Credits
Project images and descriptions are © MVRDV and the credited partners and photographers. Links point to the project pages on mvrdv.com. The Carnegie Mellon material is credited to Carnegie Mellon University.

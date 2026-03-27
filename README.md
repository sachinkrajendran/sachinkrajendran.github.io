# sachinkrajendran.github.io

Personal academic website, live at **https://sachinkrajendran.github.io**

## Files

| File | Purpose |
|------|---------|
| `index.html` | All page content and structure |
| `style.css` | All styling |
| `photo.jpg` | Profile photo (add this file to show your photo) |
| `cv.pdf` | CV download (add this file to enable the CV button) |

## How to edit content

All placeholder text in `index.html` is wrapped in `[square brackets]`. Open the file in any text editor and search for `[` to find everything that needs filling in.

### Name, title, bio

```html
<h1>Sachin Krajendran</h1>
<p class="role">[Title, e.g. PhD Candidate · Department of X · University of Y]</p>
<p class="bio">[Short bio ...]</p>
```

### Links (email, Google Scholar, LinkedIn)

```html
<a href="mailto:placeholder@university.edu">Email</a>
<a href="https://scholar.google.com/..." target="_blank">Google Scholar</a>
```
Replace the `href` values with your actual URLs.

### Research interests

Each interest is a `<li>` inside `<ul class="research-list">`:
```html
<li>Constraint Programming</li>
<li>Combinatorial Optimisation</li>
```

### Publications

Copy and paste this block for each paper, filling in the fields:
```html
<div class="pub">
  <p class="pub-title">Paper title</p>
  <p class="pub-authors">Author One, <strong>Sachin Krajendran</strong>, Author Two</p>
  <p class="pub-venue"><em>Conference or Journal Name</em>, 2025</p>
  <div class="pub-links">
    <a href="link-to-pdf.pdf">PDF</a>
    <a href="https://github.com/...">Code</a>
  </div>
</div>
```

### Projects

Copy and paste this block for each project:
```html
<div class="project">
  <h3>Project title</h3>
  <p>Short description.</p>
  <a href="https://github.com/..." target="_blank">GitHub</a>
</div>
```

### Contact

```html
<a href="mailto:your@email.com">your@email.com</a>
<p><strong>Office:</strong> Room 123, Building Name, University</p>
```

### Profile photo

Drop a file named `photo.jpg` into this folder. It will appear automatically as a circular avatar.

### CV

Drop a file named `cv.pdf` into this folder. The CV button in the header will link to it automatically.

## How to deploy changes

After editing any file, run these commands in the terminal from this folder:

```bash
git add .
git commit -m "Update content"
git push
```

The site updates within ~60 seconds of pushing.

## Background animation

The animated node-graph background is a `<canvas>` element driven by JavaScript at the bottom of `index.html`. To adjust it, find the constants near the top of the `<script>` block:

```js
const NODE_COUNT   = 55;    // number of floating nodes
const CONNECT_DIST = 180;   // max distance to draw an edge
const SPEED        = 0.28;  // drift speed
const NODE_R       = 3;     // node radius (px)
```

To remove the background entirely, delete the `<canvas id="bg-canvas"></canvas>` line and the entire `<script>` block at the bottom of `index.html`.

## Methods illustrations

The four SVG diagrams (Gantt chart, Branch & Bound tree, LP feasible region, Constraint network) are inline SVGs inside the `<section id="methods">` block in `index.html`. You can remove the whole section or swap in your own SVGs.

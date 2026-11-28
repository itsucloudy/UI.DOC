# UI.DOC

UI.DOC is a static HTML5 and CSS3 school project built in GitHub Codespaces. The site documents its own code: how the locked home screen works, how the files and stylesheet are organized, and how the work was split between manual coding and AI help.

## What the Site Does

The project runs on four HTML pages and one shared stylesheet (`styles.css`), with zero JavaScript, frameworks, or external libraries.

- **Home (`index.html`):** Locks the landing screen to `100dvh` with Flexbox and `overflow-y: hidden` on desktop. It pairs an intro column and two action buttons with a full-card anchor link (`.hero-card`) that opens the mechanics page.
- **Mechanics (`pages/mechanics.html`):** Explains how the two body modes (`.stationary-viewport` vs. `.subpage`), shared header bar, `aria-current="page"` active state, clickable hero card, CSS Grid, pure-CSS split bar, relative folder paths, and `@media (max-width: 768px)` mobile reflow work in the browser.
- **Structure (`pages/structure.html`):** Maps the file hierarchy, shared semantic landmarks (`header`, `main`, `footer`), container width limits (`1200px` on home vs. `740px` on subpages), the top-to-bottom order of `styles.css`, all 11 `:root` color tokens, and the system font stacks.
- **Legals (`pages/legals.html`):** Shows the 65% / 35% authorship breakdown with a pure-CSS progress bar and documents the static, zero-dependency scope of the project.

## Project Structure

```text
project-root/
├── index.html              # Locked 100dvh landing page
├── styles.css              # Shared stylesheet (tokens, layout, components, mobile rules)
├── README.md               # Project overview and build process
└── pages/
    ├── mechanics.html      # Breakdown of layout modes, links, and CSS behavior
    ├── structure.html      # File map, CSS cascade order, colors, and fonts
    └── legals.html         # 65/35 authorship split and technical scope
```

## How It Was Built

### My Part (65%)

I started by looking at an early AI layout reference, then built the site myself by eye instead of copying generated code straight into the editor, only checking back when I ran into a bug I could not solve on my own.
Everything core to the project was built and assembled by hand:

- Planning the four pages and setting up the root and `pages/` folder structure.
- Writing the main layout and component rules in `styles.css`, including the `100dvh` viewport lock, Flexbox alignment, button and card hover styles, and the `:root` color palette.
- Testing every page in the browser, fixing broken links and spacing problems, and replacing an earlier test form with the authorship and legals page.

### AI's Part (35%)

AI acted as a reference and editing helper rather than rewriting the codebase from scratch:

- Generating the initial visual layout reference at the start of the project.
- Helping speed up repetitive HTML markup, file naming, and early text drafts across the four pages.
- Catching relative path mistakes between the root folder and `pages/` and helping write the `.split-bar` percentage bar markup.
- Polishing and organizing the finished project: tightening the page copy so it matched the actual CSS rules, aligning the documentation across all files, and making small targeted fixes in `styles.css` (active-link styling for `aria-current="page"`, block display on `.back-link`, inline code styling inside `.page-lead`, and mobile padding/footer stacking).

## Running Locally

Because the site uses only static HTML and CSS, no build step or server is required. Open `index.html` directly in any browser (or preview it with a static server in GitHub Codespaces).

# ajhun.com

Static HTML site. No build step, no dependencies. Edit a file, commit, Netlify redeploys.

## Structure

    index.html                          landing
    engineering.html                    mechanical projects
    modeling.html                       computational projects
    self-awareness.html                 research project 01
    n-dimensional-evolved-robots.html   research project 02
    404.html
    assets/css/site.css                 fonts, globals, hover rules, components
    assets/fonts/                       self-hosted woff2
    assets/img/                         all images

## Local preview

Open `index.html` in a browser. What you see is exactly what deploys.

## Adding a research project

1. Copy `self-awareness.html` to a new file.
2. Update the `<title>` and the meta description at the top.
3. Add it to the sidebar nav block in every page (search for `RESEARCH`).

## Adding an engineering or modeling project

Copy an existing `<section>` block in `engineering.html` or `modeling.html`,
change the id, title and text, and add its anchor to the "ON THIS PAGE" list.

## Images

Drop the file in `assets/img/` and reference it as `assets/img/name.jpg`.
Lowercase, hyphenated, no spaces.

## Before going live

Remove `<meta name="robots" content="noindex">` from all five pages.

## Deploy

    netlify deploy --dir=. --prod

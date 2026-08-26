# ajhun.com

Static HTML. No build step, no dependencies. Edit a file, commit, Netlify redeploys.

    index.html                          landing
    engineering.html                    mechanical projects
    modeling.html                       computational projects
    self-awareness.html                 research 01
    n-dimensional-evolved-robots.html   research 02
    404.html
    assets/css/site.css                 shared globals
    assets/img/                         all images
    assets/docs/                        PDFs

Each page carries its own <style> block with that page's rules, including the
mobile layout under @media (max-width: 768px). Fonts load from Google Fonts.
Cloudflare Web Analytics beacon sits before </body> on every page.

## Local preview
Open index.html in a browser. What you see is what deploys.

## Mobile
One set of files. The @media (max-width: 768px) block in each page's <style>
takes over below 768px. Nothing to switch on.

## Adding a project
Copy an existing <section> in engineering.html or modeling.html, change the id,
title and text, add its anchor to the "ON THIS PAGE" list, and add the same
entry to the mobile index panel near the top of the file.

## Images
Drop into assets/img/, lowercase-hyphenated, reference as assets/img/name.jpg.

## Deploy
Push to the v2 branch. Netlify builds from it automatically.

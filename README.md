# Matthew Porcelli Portfolio

A personal portfolio website for presenting Matthew's telecommunications and network engineering experience, automation and platform work, and the way he approaches day-to-day engineering.

## Table of contents

- [Project purpose](#project-purpose)
- [Current site](#current-site)
- [Directory structure](#directory-structure)
- [Application project pages](#application-project-pages)
- [Using the assets directory](#using-the-assets-directory)
- [Local preview](#local-preview)
- [Publishing](#publishing)
- [Growing the portfolio](#growing-the-portfolio)

## Project purpose

This site is intended to show more than a list of skills. It will explain:

- The problems and outcomes Matthew's work focuses on.
- How he approaches operational and engineering work.
- Specific projects, including the context, decisions, and results.
- Relevant technical areas and ways to get in touch.

The design uses a dark navy palette with blue and teal accents. It is being developed as an original portfolio rather than a copy of another site.

## Current site

The site is a static page built with HTML and CSS, without a JavaScript framework or build step. The homepage includes an introduction with Matthew's portrait, an improvement workflow, outcomes, working approach, areas of focus, and a contact section. Detailed application stories can be added as they are ready.

## Directory structure

```text
portfolio/
├── .github/
│   └── workflows/
│       └── static.yml       # Deploys the static site to GitHub Pages
├── index.html               # Homepage markup and page styles
├── README.md                # Project purpose, structure, and working notes
├── projects/                # Planned: detailed pages for individual applications
│   └── app-name/
│       └── index.html       # One application's story, screenshots, and details
└── assets/                  # Static files used by the site
    ├── images/
    │   ├── Matthew-Porcelli.jpg  # Homepage portrait
    │   └── projects/        # Planned: application screenshots
    │       └── app-name/
    └── documents/           # Planned: downloadable résumé
```

The homepage portrait is currently stored directly in `assets/images/`. Project pages, project screenshots, and the résumé folder are planned and can be added when their content is ready. Keep image references descriptive and use paths that work when hosted beneath the GitHub Pages site URL.

## Application project pages

The homepage will stay concise so visitors can scan the work quickly. Each application can have a short entry with its name, the problem it addresses, and Matthew's contribution, plus a clear link to a dedicated detail page.

The detail page can tell the fuller story: context, approach, key decisions, outcome, and relevant technologies. It can also show screenshots with captions and useful alternative text. A project-specific folder under `projects/` keeps each page easy to find and share directly.

For example, a homepage link to `projects/app-name/` opens that project's `index.html`. Store its screenshots under `assets/images/projects/app-name/` and use descriptive filenames such as `workflow-overview.jpg`.

## Using the assets directory

`assets/` is for static files the site uses, such as images and a downloadable résumé. The homepage portrait currently lives in `assets/images/`; application screenshots can be grouped under `assets/images/projects/<app-name>/`. Add `assets/documents/` when the résumé is ready to include.

Other folders can be added if the site needs them—for example, `assets/icons/` for custom icon files or `assets/fonts/` for locally hosted fonts. If the page's CSS or JavaScript grows enough to move out of `index.html`, those source files would usually live in top-level `css/` or `js/` folders instead. Avoid creating empty folders or duplicating files that are already available elsewhere.

## Local preview

Open `index.html` directly in a browser to preview the page. Since the site is static, no dependency installation or build command is currently required.

## Publishing

The GitHub Actions workflow in `.github/workflows/static.yml` deploys the repository contents to GitHub Pages when changes are pushed to the `main` branch. It can also be run manually from the repository's Actions tab.

## Growing the portfolio

As the site evolves, update this README when new files or directories are introduced. For project entries, use real examples and clearly describe the problem, Matthew's contribution, and the outcome; avoid adding unverified metrics or claims. Optimize images for the web, keep their filenames meaningful, and provide alt text that describes the useful content of each screenshot.

# Matthew Porcelli Portfolio

A personal portfolio website for presenting Matthew's telecommunications and network engineering experience, automation and platform work, and the way he approaches day-to-day engineering.

## Table of contents

- [Project purpose](#project-purpose)
- [Current site](#current-site)
- [Planned portfolio content](#planned-portfolio-content)
- [Directory structure](#directory-structure)
- [Project detail pages](#project-detail-pages)
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

The site is a static page built with HTML and CSS, without a JavaScript framework or build step. The homepage is structured around an introduction and portrait, the numbered Listen → Design → Deploy → Enable approach, network scale, skills, selected projects, experience, and contact. The introduction shows a résumé placeholder styled like the prominent Contact link, plus a LinkedIn link; the résumé placeholder will become a download link once the PDF is added. The contact options appear in this order: email, cover letter, résumé, and LinkedIn. Email opens a message in the visitor's configured mail app; the résumé and cover-letter items will become download links after their PDFs are added.

## Planned portfolio content

The homepage should give visitors a concise overview of Matthew's experience and work, with links to deeper project stories where useful:

1. **Introduction and working approach** — telecommunications and network engineering background, specialties, and a concise Listen → Design → Deploy → Enable process.
2. **Network scale** — selected, verifiable statistics describing the size or reach of the network Matthew works on. Include context and clear units so each statistic is meaningful; do not publish confidential or unverified figures.
3. **Skills / Areas of focus** — grouped into Network Design & Planning (IP/MPLS Designs, QoS Strategy, DWDM/Optical Designs, Capacity Planning, Requirements-Based Hardware Selection, Production & Lab Budgetary Planning, Lifecycle Management); Automation & Platforms (Network Automation, Containerlab, Docker, Python, Linux, MCP Servers, Tooling Development); Testing & Observability (Observability, Prometheus, Grafana, Test Automation, Regression Testing, Robot Framework); and Governance & Documentation (National Market Governance, Technical Documentation, Engineering Standards).
4. **Projects** — work split into two areas:
   - **Network design** — network architecture, design, and engineering work.
   - **Applications built** — software and automation applications Matthew has created.

   Each project can have a short homepage summary and a link to a dedicated detail page with the context, Matthew's contribution, decisions, outcomes, and screenshots where appropriate.
5. **Experience** — a concise summary of key résumé points, with the full résumé available to download when added.
6. **Contact** — an email link, downloadable cover letter and résumé PDFs when available, and a LinkedIn profile link.

Keep the homepage focused on summaries and evidence. Use the numbered vertical layout for the working approach and the skills chips for technical focus areas. In the network section, group the IP/MPLS production and lab metrics under colored IP/MPLS labels, with concise bold category labels above prominent counts and smaller muted units alongside; show transport categories with their names at the top of each card and larger, stacked node and service counts. Organize the lab panel with colored IP/MPLS, Transport, and Virtualization group labels and metric cards beneath them; arrange the four lab metrics in a compact row on wide screens, with responsive grouping and stacking at narrower widths. Project examples should demonstrate outcomes directly, avoiding separate sections that repeat the same generic claims.

The network statistics are organized as:

- **Production Network** — one IP/MPLS group with Core Routers (700+), Access Routers (79,000+), and Services Built (1.2M+); a separate three-card transport group ordered Core (combined Backbone / Metro: 1,100+ nodes, 2,700+ services), Access (600+ nodes, 1,200+ services), and OTN (200+ nodes, 2,000+ services).
- **Lab Environment** — an IP/MPLS group with Core Routers (30+) and Access Routers (100+), a Transport group with Access (20+ Nodes), and a Virtualization group with 10 virtual machines.

Provide context for what is included in each count.

## Directory structure

```text
portfolio/
├── .github/
│   └── workflows/
│       └── static.yml       # Deploys the static site to GitHub Pages
├── index.html               # Homepage markup and page styles
├── README.md                # Project purpose, structure, and working notes
├── projects/                # Planned: detailed pages for selected projects
│   ├── network-design/
│   │   └── project-name/
│   │       └── index.html   # Network design project story and supporting visuals
│   └── applications/
│       └── app-name/
│           └── index.html   # Application story, screenshots, and details
└── assets/                  # Static files used by the site
    ├── images/
    │   ├── Matthew-Porcelli.jpg  # Homepage portrait
    │   └── projects/        # Planned: project screenshots and visuals
    │       └── project-name/
    └── documents/           # Planned: downloadable résumé and cover letter PDFs
```

The homepage portrait is currently stored directly in `assets/images/`. Project pages, project visuals, and the documents folder are planned and can be added when their content is ready. Keep image references descriptive and use paths that work when hosted beneath the GitHub Pages site URL.

## Project detail pages

The homepage will stay concise so visitors can scan the work quickly. Network design projects and applications built can each have a short entry with a name, context, and Matthew's contribution, plus a clear link to a dedicated detail page.

The detail page can tell the fuller story: context, approach, key decisions, outcome, and relevant technologies. Application pages can show screenshots with captions and useful alternative text; network design pages can include appropriate diagrams or other supporting visuals. A project-specific folder under `projects/` keeps each page easy to find and share directly.

For example, a homepage link to `projects/applications/app-name/` opens that application's `index.html`. Store its visuals under `assets/images/projects/app-name/` and use descriptive filenames such as `workflow-overview.jpg`.

## Using the assets directory

`assets/` is for static files the site uses, such as images and downloadable documents. The homepage portrait currently lives in `assets/images/`; project screenshots and visuals can be grouped under `assets/images/projects/<project-name>/`. Add résumé and cover-letter PDFs to `assets/documents/` when they are ready. The homepage will link to those files once they exist, rather than displaying broken downloads.

Other folders can be added if the site needs them—for example, `assets/icons/` for custom icon files or `assets/fonts/` for locally hosted fonts. If the page's CSS or JavaScript grows enough to move out of `index.html`, those source files would usually live in top-level `css/` or `js/` folders instead. Avoid creating empty folders or duplicating files that are already available elsewhere.

## Local preview

Open `index.html` directly in a browser to preview the page. Since the site is static, no dependency installation or build command is currently required.

## Publishing

The GitHub Actions workflow in `.github/workflows/static.yml` deploys the repository contents to GitHub Pages when changes are pushed to the `main` branch. It can also be run manually from the repository's Actions tab.

## Growing the portfolio

As the site evolves, update this README when new files or directories are introduced. For project entries, use real examples and clearly describe the problem, Matthew's contribution, and the outcome; avoid adding unverified metrics or claims. Verify network statistics and provide enough context to interpret them without exposing confidential information. Optimize images for the web, keep their filenames meaningful, and provide alt text that describes the useful content of each visual.

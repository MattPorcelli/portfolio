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

The site is a static page built with HTML and CSS, without a JavaScript framework or build step. The homepage is structured around an introduction and portrait, the numbered Listen → Design → Deploy → Enable approach, network scale, skills, selected projects, experience, and contact. The introduction includes a résumé download link and a LinkedIn link. The contact section highlights the intersection of networking, software engineering, infrastructure automation, and AI-assisted development. Contact options appear in this order: email, résumé, and LinkedIn. Email opens a message in the visitor's configured mail app; the résumé downloads from `assets/resume/`.

## Planned portfolio content

The homepage should give visitors a concise overview of Matthew's experience and work, with links to deeper project stories where useful:

1. **Introduction and working approach** — 20+ years in telecommunications and 17+ years in network engineering, core specialties, and a concise Listen → Design → Deploy → Enable process.
2. **Network scale and reliability** — selected, verifiable statistics describing the size, capabilities, and reliability of the network Matthew works on, including production and lab device counts, service scale, and 99.999% availability. Include context and clear units so each statistic is meaningful; do not publish confidential or unverified figures.
3. **Skills / Areas of focus** — grouped into Network Design & Planning (IP/MPLS Designs, QoS Strategy, DWDM/Optical Designs, Capacity Planning, Requirements-Based Hardware Selection, Production & Lab Budgetary Planning, Lifecycle Management); Automation & Platforms (Network Automation, Containerlab, Docker, Python, Linux, MCP Servers, Tooling Development); Testing & Observability (Observability, Prometheus, Grafana, Test Automation, Regression Testing, Robot Framework); and Governance & Documentation (National Market Governance, Technical Documentation, Engineering Standards).
4. **Selected work** — work presented in three areas:
   - **Network design** — network architecture, design, and engineering work.
   - **Applications Built with AI** — software and automation applications Matthew has created with AI-assisted development.
   - **Engineering practice** — two categories:
     - **Testing & Evaluations** — Lab and regression testing, where applicable, supported IP/MPLS Nokia IXR-e2c (1G/10G/25G/100G) and IXR-e2 (up to 400G) evaluations, plus DWDM EMS/software releases and optical-card evaluations, covering capabilities, limitations, integration, stability, bookended-solution feasibility, and potential cost savings.
     - **Standards & Documentation** — DWDM commissioning, node installation/insertion, wave-service provisioning, and CBOA nodal software upgrade guidance for field technicians and provisioners.

   The homepage should first explain each category, then preview selected examples with concise context and a useful visual. Engineering Practice is presented as one full-width “Lab Testing & Evaluations” panel, with IP/MPLS and DWDM evaluation groups followed by a separate Standards & Documentation section; the lists use responsive columns where space allows. Network design visuals and application screenshots include a note that confidential details are blurred or replaced with generic values. Fuller case-study pages can later expand on the problem, Matthew's contribution, design decisions, implementation, and outcomes.
5. **Experience** — a dot-marker career timeline covering Cox Communications roles from 2006 to the present, followed by certifications and education. The résumé is downloadable from both the introduction and contact links.
6. **Contact** — an email link, the résumé download, and a LinkedIn profile link.

Keep the homepage focused on summaries and evidence. Use the numbered vertical layout for the working approach and grouped focus areas for technical skills. Introduce the Areas of Focus section with: “My work spans network design and planning, automation and platforms, testing and observability, and engineering governance. I bring these disciplines together to build reliable networks and make day-to-day operations more effective.” The Selected Work section previews Network Design and Applications Built with AI alongside Engineering Practice, with Testing & Evaluations and Standards & Documentation subcategories. Network design examples are grouped into “Understanding Network Traffic and Failure Scenarios,” with the geographical and redundant equipment protection diagram included in the same gallery. Application previews introduce Containerlab Orchestrator, Harbor, Endpoint, and the ZTP Orchestrator proof of concept with brief context and screenshots; all four applications are run in one or more Docker containers, and screenshots note that confidential details are blurred or replaced with generic values. A brief AI-assisted development note follows the application gallery: when working with AI, I do not simply hand it a problem and ask for code; I define the design, architecture, direction, and order of operations first. AI accelerates implementation but cannot replace the thinking that has to happen first. Containerlab Orchestrator is summarized as a visual topology builder with production-device import and live telemetry, while Harbor is a unified workspace that connects engineering tools through REST APIs to reduce application switching, with Docker-based Robot Framework tests, Ixia traffic generation, and results analysis. Endpoint is described as using APIs to integrate with the EMS, turning live inventory into lifecycle budget estimates within minutes. ZTP Orchestrator is described as a proof of concept for deterministic, secure, observable provisioning, using device pre-registration, fail-closed handling of unknown devices, real-time state tracking, and a goal of delivering routers with verified SNMPv3 credentials without CLI access or manual intervention. Testing & Evaluations notes that lab and regression testing were used where applicable. Standards & Documentation previews four DWDM guides for commissioning, equipment installation and node insertion, wave-service provisioning, and CBOA nodal software upgrades, including validation guidance intended to protect the network's 99.999% availability objective. More detail can be added to linked case-study pages later. In the network section, group the IP/MPLS production and lab metrics under colored IP/MPLS labels, with concise bold category labels above prominent counts and smaller muted units alongside; show transport categories with their names at the top of each card and larger, stacked node and service counts. Organize the lab panel with colored IP/MPLS, Transport, and Virtualization group labels and metric cards beneath them; arrange the four lab metrics in a compact row on wide screens, with responsive grouping and stacking at narrower widths. The Contact section currently uses this statement: “I’m focused on the intersection of networking, software engineering, and infrastructure automation, leveraging AI-assisted development to build and operate systems more effectively.” Its paragraph uses the full available width of the contact card.

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
│   ├── applications/
│   │   └── app-name/
│   │       └── index.html   # Application story, screenshots, and details
│   └── engineering-practice/
│       ├── testing-evaluations/
│       │   └── evaluation-name/
│       │       └── index.html   # Goals, coverage, findings, recommendations
│       └── standards/
│           └── standard-name/
│               └── index.html   # Authored guidance, audience, requirements, purpose
└── assets/                  # Static files used by the site
    ├── resume/
    │   └── Matthew Porcelli_Resume.pdf  # Downloadable résumé
    ├── images/
    │   ├── Matthew-Porcelli.jpg  # Homepage portrait
    │   ├── network-design/  # Network design diagrams and visuals
    │   │   ├── StandardNetworkDesign.png
    │   │   ├── StandardTraffic.png
    │   │   ├── RouterHardwareFailure.png
    │   │   ├── OpticalFiberEvent.png
    │   │   ├── TrafficFlowWithLocalFiber.png
    │   │   ├── TrafficFlowWithFiberEvent.png
    │   │   ├── TrafficFlowWithFiberEventMulti-Hub.png
    │   │   └── GeographicalandRedundantEquipmentProtecton.png
    │   └── applications/    # Application screenshots, grouped by application
    │       ├── Containerlab/
    │       ├── Endpoint/
    │       ├── Harbor/
    │       └── ZTP/
    └── documents/           # Planned: downloadable cover letter PDF
```

The homepage portrait is stored directly in `assets/images/`. Network design visuals are in `assets/images/network-design/`; application screenshots are grouped by application under `assets/images/applications/`. The current résumé is stored in `assets/resume/` and linked from the homepage. Add a design-specific subfolder under `network-design/` if the image collection grows enough to benefit from that separation. The documents folder is planned for the cover letter PDF. Use descriptive filenames and paths that work when hosted beneath the GitHub Pages site URL.

## Project detail pages

The homepage will stay concise so visitors can scan the work quickly. Network design projects, applications built, and engineering-practice examples can each have a short entry with a name, context, and Matthew's contribution, plus a clear link to a dedicated detail page.

The detail page can tell the fuller story: context, approach, key decisions, outcome, and relevant technologies. Application pages can show screenshots with captions and useful alternative text; network design pages can include appropriate diagrams or other supporting visuals. Testing & Evaluations pages can use concise bullets for goals, test coverage, findings, and recommendations. Standards & Documentation pages can summarize the authored guidance, audience, requirements, and operational purpose. Visuals are optional for these engineering-practice examples; use them only when they clarify the work. A project-specific folder under `projects/` keeps each page easy to find and share directly.

For example, a homepage link to `projects/applications/app-name/` opens that application's `index.html`; store its screenshots and visuals under `assets/images/applications/<app-name>/`. A testing evaluation can live at `projects/engineering-practice/testing-evaluations/evaluation-name/`, and an authored standard at `projects/engineering-practice/standards/standard-name/`. Store network design visuals under `assets/images/network-design/` using descriptive filenames; split them into design-specific subfolders if a larger collection makes that useful.

## Using the assets directory

`assets/` is for static files the site uses, such as images and downloadable documents. The homepage portrait lives in `assets/images/`; network design visuals are in `assets/images/network-design/`, and application images are grouped by app under `assets/images/applications/<app-name>/`. The current résumé PDF lives in `assets/resume/` and is linked for download. Add the cover-letter PDF to `assets/documents/` when it is ready; the homepage will link to it once it exists, rather than displaying a broken download.

Other folders can be added if the site needs them—for example, `assets/icons/` for custom icon files or `assets/fonts/` for locally hosted fonts. If the page's CSS or JavaScript grows enough to move out of `index.html`, those source files would usually live in top-level `css/` or `js/` folders instead. Avoid creating empty folders or duplicating files that are already available elsewhere.

## Local preview

Open `index.html` directly in a browser to preview the page. Since the site is static, no dependency installation or build command is currently required.

## Publishing

The GitHub Actions workflow in `.github/workflows/static.yml` deploys the repository contents to GitHub Pages when changes are pushed to the `main` branch. It can also be run manually from the repository's Actions tab.

## Growing the portfolio

As the site evolves, update this README when new files or directories are introduced. For project entries, use real examples and clearly describe the problem, Matthew's contribution, and the outcome; avoid adding unverified metrics or claims. Verify network statistics and provide enough context to interpret them without exposing confidential information. Optimize images for the web, keep their filenames meaningful, and provide alt text that describes the useful content of each visual.

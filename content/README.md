# Content Model

This site is static HTML for now, but future content should start as markdown with frontmatter.
The fields below are intentionally small so notes can move from Obsidian to a static generator later.

## Shared Fields

```yaml
---
title: "Title of the piece"
date: 2026-06-01
type: essay
status: published
summary: "One or two plain sentences about what this is."
topics:
  - product
  - systems
visibility: public
---
```

Use `type` for the artifact shape:

- `essay`
- `note`
- `devlog`
- `project`
- `experiment`

Use `status` for state:

- `draft`
- `planned`
- `published`
- `active`
- `paused`
- `archived`

Use `topics` instead of separate tags and categories for now.

## Essays And Notes

```yaml
---
title: "From Amazon PMT to Startup Product Director"
date: 2026-06-01
type: essay
status: published
summary: "What changes when product work moves from big-company systems to startup constraints."
topics:
  - product
  - startups
visibility: public
---
```

## Projects

```yaml
---
title: "Project Name"
date: 2026-06-10
type: project
status: active
stage: prototype
summary: "What this project is and why it exists."
topics:
  - ai-development
  - tooling
links:
  repo:
  demo:
  writeup:
visibility: public
---
```

Project `stage` values:

- `concept`
- `prototype`
- `live`
- `paused`
- `archived`

## Devlogs

Devlogs belong to a project. They can appear in the main writing stream and on the project page.

```yaml
---
title: "Devlog 01: First Working Version"
date: 2026-06-12
type: devlog
status: published
project: "project-slug"
stage: prototype
summary: "What changed in this build cycle."
topics:
  - ai-development
  - product
visibility: public
---
```

## Experiments

Experiments are documentation, not advice. They should have a clear question, hypothesis, method,
log, and result.

```yaml
---
title: "AI-Assisted Capture to Draft Workflow"
date: 2026-06-15
type: experiment
status: planned
summary: "A structured test of whether a repeatable workflow improves publishing consistency."
hypothesis: "A capture-to-draft routine will reduce friction enough to publish more consistently."
duration: "4 weeks"
topics:
  - ai
  - writing
  - systems
visibility: public
---
```

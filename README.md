# blog-content

Content repository for a **RobCo Termlink** personal blog — a Fallout-themed
terminal log. Posts are plain Markdown files with YAML frontmatter, organized
on disk by publication date. This repo holds *content only*; the site
generator / renderer that consumes it lives elsewhere.

## Layout

Posts live under `blogs/` in a date-based directory tree:

```
blogs/<YYYY>/<MM>/<DD>/<slug>.md
```

For example:

```
blogs/
  2026/
    06/
      14/todays-magic-patch.md
      12/todays-dispatch.md
      11/yesterdays-log.md
    05/
      20/last-month-recap.md
  2287/
    10/23/welcome.md
    11/05/reactor-diagnostics.md
         assets/reactor.svg
  2288/
    01/12/wasteland-survival.md
    02/01/classified.md
```

Both real-world dates (2026) and in-universe wasteland dates (2287–2288) are
used as demo content spanning *today*, *this week*, *this month*, and *earlier*.

## Post format

Each post is a Markdown file beginning with a YAML frontmatter block:

```markdown
---
title: "Welcome to RobCo Termlink"
description: "Booting the personal log subsystem."
draft: true
---
# Greetings, Overseer

Body content in standard Markdown...
```

Frontmatter fields:

| Field         | Required | Notes                                                        |
| ------------- | -------- | ------------------------------------------------------------ |
| `title`       | yes      | Display title of the post.                                   |
| `description` | no       | Short summary / subtitle.                                    |
| `draft`       | no       | When `true`, the post is unpublished and should be excluded. |

The body supports standard Markdown — headings, lists, blockquotes, fenced
code blocks, and images.

## Assets

Images and other static files are stored in an `assets/` directory alongside
the posts that reference them, and are linked with relative paths:

```markdown
![reactor schematic](./assets/reactor.svg)
```

## Drafts

Posts with `draft: true` in their frontmatter (e.g.
`blogs/2288/02/01/classified.md`) are works in progress and should not be
rendered on the public site.

---
layout: default
title: Test navigation
nav_order: 1
---

Testing generated navigation for pages with `nav_exclude`

[`index.html`](.) lines:

- just pages, no docs: 133
- docs/parent.md `has_children: true`: 187
- docs/parent.md `has_children: false`: 148
- just docs, no pages: 125

It appears that giving a child to a page in `docs` adds 4 blank lines
for each page in `pages` with `nav_exclude: true`.

In a real project with 125 pages, making `has_children: false` in `docs`
shrinks the generated nav from 1650 lines to 400 lines.

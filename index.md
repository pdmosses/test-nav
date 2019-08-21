---
layout: default
title: Test navigation
nav_exclude: true
---

Test of generated navigation sidebar
====================================

Just the docs
-------------

Using `_config.yml` with:
```
compress_html:
  blanklines: true
```

Using Just-the-Docs v0.2.6, this file's `<nav>` element size:

- 1400 chars

With modified `_includes/nav.html`, eliminating generation of undisplayed
children and grandchildren:

- 357 chars

- Adding the following to  `_config.yml` delays the display of grand_children
until their parent has been selected:
```
grandchildren_branch: true
```

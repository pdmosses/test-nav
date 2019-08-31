---
layout: default
title: Test navigation
nav_exclude: true
mathjax: true
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

Test of Mathjax
===============

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$

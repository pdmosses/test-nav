---
layout: default
title: Test navigation
nav_order: 0
mathjax: true
---

Test of generated navigation
============================

Just the Docs
-------------

This site is currently based on version 0.2.7 of Just the Docs,
with additions to `_includes` for recursive navigation and default page order.

Navigation involving grandchildren is illustrated in 
[UI Components]({{ site.url }}{{ site.baseurl }}/docs/ui-components).


Test of tags
------------

All pages display their tags in the navigation bar.

Tags are specified in the front matter of a page as an array:
```
tags:
  - ...
  - ...
```
Tags may include spaces and non-alphanumeric characters,
but internally they are converted to a 
["pretty"](https://jekyllrb.com/docs/liquid/filters/#options-for-the-slugify-filter)
 canonical form.
 
Each tag is linked to a section of a page that lists all the tags and,
for each tag, lists all the pages that are tagged with it.

See [Test Tags]({{ site.url }}{{ site.baseurl }}/docs/test-tags/) for some simple tests.

To add tags to a _Just the Docs_ website, copy the files `_layouts/tags.html`
and `_includes/nav_tags.html` to it, and include the latter file in
`_layouts/default.html`.
Copy also the file `docs/tags.md`.

> _Caveat:_ The usability of this implementation of tags has not yet been tested
> on a larger site with real-world tags.

**UPDATE (May 2020): The support for tag indexes provided here has now been extended
with semi-automatic *creation of separate pages for individual tags*, and tested
on a larger site with real-world tags. It is essentially theme-independent;
see <https://pdmosses.github.io/tags/> for an example of its use with the basic
Minima theme, along with a brief user guide.**

Test of Mathjax
---------------

See the [Test Mathjax]({{ site.url }}{{ site.baseurl }}/docs/Mathjax) page.

To use Mathjax, update `_config.yml` to ensure:
```
compress_html:
  blanklines: true
```
and copy the contents of `_includes/head_custom.html`.
The Mathjax code is loaded only on pages that set `mathjax: true`.


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

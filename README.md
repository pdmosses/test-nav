---

Test of generated navigation
============================

Just the Docs
-------------

This site is currently based on version 0.2.7 of Just the Docs,
with additions to `_includes` for recursive navigation and default page order.

Navigation involving grandchildren is illustrated in 
[UI Components](https://pdmosses.github.io/test-nav/docs/ui-components).


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

See [Test Tags](https://pdmosses.github.io/test-nav/docs/test-tags/) for some simple tests.

To add tags to a _Just the Docs_ website, copy the files `_layouts/tags.html`
and `_includes/nav_tags.html` to it, and include the latter file in
`_layouts/default.html`.
Copy also the file `docs/tags.md`.

> _Caveat:_ The usability of this implementation of tags has not yet been tested
> on a larger site with real-world tags.

Suggestions for improvements are welcome! 


Test of Mathjax
---------------

See the [Test Mathjax](https://pdmosses.github.io/test-nav/docs/Mathjax) page.

To use Mathjax, update `_config.yml` to ensure:
```
compress_html:
  blanklines: true
```
and copy the contents of `_includes/head_custom.html`.
The Mathjax code is loaded only on pages that set `mathjax: true`.

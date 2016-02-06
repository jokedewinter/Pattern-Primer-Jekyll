# Jekyll version of Pattern Primer

Forked from the [original Pattern-Primer for PHP by Adactio (Jeremy Keith)](https://github.com/adactio/Pattern-Primer)

Inspired by [Ruby (Sinatra) version](https://github.com/micdijkstra/Pattern-Primer-Ruby)

## Pattern Primer

This is a design communication, testing, and process tool.

Create little snippets of markup and save them to the `_patterns` directory (a Jekyll [collection](http://jekyllrb.com/docs/collections/)). The pattern primer will generate a list of all the HTML patterns in that folder.

The patterns are rendered as HTML, with a reference source displayed in a `<textarea>` next to each. Attach or reference any CSS to test out styles against these markup patterns.

## Why a Jekyll fork?

Why not? [Jekyll](http://jekyllrb.com) is a useful way to build static sites, and it is well-suited for quick prototyping. This is intended as a version of Adactio’s [Pattern Primer](https://github.com/adactio/Pattern-Primer) but without PHP dependencies. It can be [built locally with a Jekyll/Ruby environment](http://jekyllrb.com/docs/usage/) or uploaded as a static directory on a remote server – [here is an example of a hosted version](http://patternprimer.olivermak.es/).

## Configuration

Make sure to [install Jekyll](http://jekyllrb.com/) first (Ruby required).

### Option #1: local hosting

1. Clone this repo.
2. Create your own HTML patterns and link your CSS ([instructions](#creating-html-patterns)).
3. Run the command `jekyll serve` and open <http://localhost:4000> in your browser.

### Option #2: **GitHub _User_ Page (user.github.io)** hosted with GitHub Pages

1. Clone/fork this repo.
2. Rename repo to `user.github.io` (user = your GH username).
3. Create your own HTML patterns and link your CSS ([instructions](#creating-html-patterns)).
4. After pushing all of your changes to GitHub `Master` branch, create a new branch and call it `gh-pages`.
5. Visit your new site (may take up to 10 minutes to populate) at `http://user.github.io/`.

### Option #3: **GitHub _Project_ Page (user.github.io/projectname)** hosted with GitHub Pages

1. Clone/Fork this repo.
2. **IMPORTANT:** in the `_config.yml` file, change `baseurl: ''` to `baseurl: '/projectname'`
3. Create your own HTML patterns and link your CSS ([instructions](#creating-html-patterns)).
4. After pushing all of your changes to GitHub `Master` branch, create a new branch and call it `gh-pages`.
5. Visit your new site (may take up to 10 minutes to populate) at `http://user.github.io/projectname`.

[Learn more about Jekyll on GitHub Pages](http://jekyllrb.com/docs/github-pages/).

### Creating HTML patterns

Add them to the `_patterns` folder. Prepend the following YAML front matter to every file:

```yaml
---
layout: pattern
title: blockquote.html
---
```

Anything that comes after the second `---` will be rendered as HTML.

### Adding CSS

There are three methods:

1. Copy your CSS file to `css/global.css` (replacing the default CSS)
2. Copy your own CSS to the `css` directory and direct a link in the `_includes/head.html` file.
3. Create a link to your own CSS file in the `_includes/head.html` file.

---

## (Optionally) Work with Markdown

One nice thing that Jekyll has built-in is a Markdown processor ([kramdown](http://kramdown.gettalong.org) by default). You can use Jekyll Pattern Primer to read Markdown snippets in the `_patterns` folder by setting the `markdown-patterns` option in `_config.yml` to `true`. This is turned off by default because markdownifying HTML with kramdown can change the intended output (typically by adding `<p>` tags). 

Flipping the `markdown-patterns` switch could be useful for documenting HTML output processed with Markdown. Keep in mind that it will fundamentally alter the form of the default HTML snippets included in the project.

---

## Other versions

- [PHP (original version)](https://github.com/adactio/Pattern-Primer)
- [Node.js](https://github.com/beardtwizzle/pattern-primer-on-node)
- [Ruby (Sinatra)](https://github.com/micdijkstra/Pattern-Primer-Ruby)

## This is what it looks like in use

<http://patternprimer.olivermak.es/> (using the default styles of [the original](http://patternprimer.adactio.com))

## Credits

The **original** [Pattern Primer is by Adactio](https://github.com/adactio/Pattern-Primer) and should be used if you prefer PHP or aren’t already using Jekyll. Many thanks to Jeremy for this great tool!

### Contributors

- [opattison](https://github.com/opattison)
- [esteinborn](https://github.com/esteinborn)
- [tombuckley](https://github.com/tombuckley)

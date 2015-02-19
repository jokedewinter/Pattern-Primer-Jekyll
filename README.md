# Jekyll version of Pattern-Primer by Adactio

Forked from the [original Pattern-Primer for PHP by adactio (Jeremy Keith)](https://github.com/adactio/Pattern-Primer)

Inspired by [Ruby (Sinatra) version](https://github.com/micdijkstra/Pattern-Primer-Ruby)

## Pattern Primer

This is a design communication, testing, and process tool.

Create little snippets of markup and save them to the “patterns folder” (called `_posts` in Jekyll). The pattern primer will generate a list of all the patterns in that folder. You will see the pattern rendered as HTML. You will also see the source displayed in a textarea. Attach or reference any CSS to test out styles.

## Why a Jekyll fork?

Why not? [Jekyll](http://jekyllrb.com) is a useful way to build static sites, and it is well-suited for quick prototyping. This is intended as a version of Adactio’s [Pattern Primer](https://github.com/adactio/Pattern-Primer) but without PHP dependencies. It can be [built locally with a Jekyll/Ruby environment](http://jekyllrb.com/docs/usage/) or uploaded as a static directory on a remote server – [here is an example of that](http://patternprimer.olivermak.es/).

## How to use it

### Local configuration

1. If you haven’t already, [install Jekyll](http://jekyllrb.com/).
2. Clone this repo.
3. Copy your CSS file to css/global.css (replacing the default CSS) *or* copy your own CSS to the css directory and direct a link in `_includes/head.html` to that file.
4. **IMPORTANT:** in the `_config.yml` file, change `baseurl: '/Pattern-Primer-Jekyll'` to `baseurl: ''`
5. Create your own HTML snippets and add them to the `_posts` folder.
6. Run the command `jekyll serve` and open <localhost:4000> in your browser.

### Configuration: **GitHub _User_ Page (user.github.io)** hosted with GitHub Pages

1. Clone/fork this repo.
2. Rename repo to `user.github.io` (user = your GH username).
3. Copy your CSS file to `css/global.css` (replacing the default CSS) *or* copy your own CSS to the `css` directory and direct a link in `_includes/head.html` to that file.
4. Create your own HTML snippets and add them to the `_posts` folder.
5. **IMPORTANT:** in the `_config.yml` file, change `baseurl: '/Pattern-Primer-Jekyll'` to `baseurl: ''`
6. After pushing all of your changes to GitHub `Master` branch, create a new branch and call it `gh-pages`.
7. Visit your new site (may take up to 10 minutes to populate) at `http://user.github.io/`.

### Configuration: **GitHub _Project_ Page (user.github.io/projectname)** hosted with GitHub Pages

1. Clone/Fork this repo.
2. Copy your CSS file to `css/global.css` (replacing the default CSS) *or* copy your own CSS to the `css` directory and direct a link in `_includes/head.html` to that file.
3. Create your own HTML snippets and add them to the `_posts` folder.
4. **IMPORTANT:** in the `_config.yml` file, change `baseurl: '/Pattern-Primer-Jekyll'` to `baseurl: '/projectname'`
5. After pushing all of your changes to GitHub `Master` branch, create a new branch and call it `gh-pages`.
6. Visit your new site (may take up to 10 minutes to populate) at `http://user.github.io/projectname`.

[Learn all about Jekyll on GitHub Pages](http://jekyllrb.com/docs/github-pages/).

### More configuration notes

**One quirk of using the pattern primer for Jekyll** is that the patterns are stored in the "_posts" folder. Every post must have identical front matter that looks like this:

```
---
layout: pattern
---
```

... and each file must be named `yyyy-mm-dd-title.html`. The date tag is arbitrary, but this will determine where it appears in order on the index. The default is set to 0001-01-01 for the packaged HTML snippets, but anything named newer than that will appear at the bottom of the list.

---

## Other versions

- [PHP (original version)](https://github.com/adactio/Pattern-Primer)
- [Node.js](https://github.com/beardtwizzle/pattern-primer-on-node)
- [Ruby (Sinatra)](https://github.com/micdijkstra/Pattern-Primer-Ruby)

## This is what it looks like

<http://patternprimer.olivermak.es/>

Note: my version uses the standard styles written by Adactio.

## Credits

The **original** [Pattern Primer is by Adactio](https://github.com/adactio/Pattern-Primer) and should be used if you prefer PHP or aren’t already using Jekyll. Many thanks to Jeremy for this great tool!

### Contributors

- [opattison](https://github.com/opattison)
- [esteinborn](https://github.com/esteinborn)
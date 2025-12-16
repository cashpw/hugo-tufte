# Tufte Hugo Theme

Hugo-Tufte is a minimalist blog-like theme for the
[static site generator Hugo](https://gohugo.io) that
attempts to be a faithful implementation of the
[Tufte-css](https://github.com/edwardtufte/tufte-css) project. The current version supports mathematical typesetting via [KaTeX](https://katex.org/).

TODO: Example website.

## Install

1. Ensure you're running [hugo *extended*](https://gohugo.io/installation/) (required for SCSS)
1. Add this repository to your hugo site's `themes` folder. We recommend including it as a submodule (`git su`)

    ```shell
    cd <your site>/themes
    git submodule add https://github.com/cashpw/hugo-tufte
    ```
1. Set the `theme` value in your site's configuration to `hugo-tufte`

## Features

### Math

In this version, I use [Yihui Xie's method](https://yihui.org/en/2018/07/latex-math-markdown/) to support (almost) seamless LaTeX rendering with [KaTeX](https://katex.org/).

For usage and examples, refer to [./exampleSite/content/posts/tufte-features.md ](https://github.com/loikein/hugo-tufte/blob/main/exampleSite/content/posts/tufte-features.md).

Downside: LaTeX in post title is no longer supported.

### Site parameters

`params` for this theme are:

- `subtitle` string: If set, displayed under the main title.
- `showPoweredBy` boolean: If `true`, display a shoutout to Hugo and this theme.
- `copyrightHolder` string: Inserts the value in the default copyright notice.
- `copyright` string: Custom copyright notice.
- `math` boolean: Site wide kill switch for Latex support
- `codeBlocksDark` boolean: If `true`, code blocks will use a dark theme.
- `marginNoteInd` string: (NEW) Custom indicator for margin notes, with suggestions in comment. (Only displayed on mobile devices or inside `cols` shortcode.)
- `sansSubtitle` boolean: If `true`, all subtitles (`h2` \& `h3`) will use up-right and sans-serif font. (As seen in _Visual Display of Quantitative Information_.)
- (`centerArticle` boolean: Not implemented yet)

**Socials**

_(The followings have not been tested for this repo, use at your own risk.)_

You can add links to your social media profile by using thoses parameters:

- `github`: string
- `gitlab`: string
- `twitter`: string
- `linkedin`: string
- `patreon`: string
- `youtube`: string
- `medium`: string
- `reddit`: string
- `stackoverflow`: string
- `instagram`: string
- `mastodon`: string
- `orcid`: string
- `google_scholar`: string

Please see [`exampleSite/config.yaml`](https://github.com/loikein/hugo-tufte/blob/main/exampleSite/config.yaml#L47) to see the full implementation with exemples.

### Page Parameters

- `math` boolean: If `true`, try to render the page's LaTeX code using KaTeX.
- `meta` boolean: If `true`, display page metadata such as author, date, categories.
  + `hideDate` boolean: If `true`, do not display a page date in metadata.
  + `hideReadTime` boolean: if `true`, do not display the page's reading time
  estimate in metadata.
- `toc` boolean: if true, display the table of contents for the page.
- Layout parameters: (NEW)
  + For more information, see [Hugo's Lookup Order | Hugo](https://gohugo.io/templates/lookup-order/).
  + `type` string: If set to `book`, layout files in [./layouts/book/](https://github.com/loikein/hugo-tufte/tree/main/layouts/book) will be prioritised.
  + `layout` string: If set, layout files with the name of this field's value will be prioritised.

### Shortcodes

This theme provides the following shortcodes in an attempt to completely
support all the features present in the [Tufte-css](https://github.com/edwardtufte/tufte-css) project.

For usage and examples, refer to [./exampleSite/content/posts/tufte-features.md ](https://github.com/loikein/hugo-tufte/blob/main/exampleSite/content/posts/tufte-features.md).

- `blockquote`
- `div`
- `epigraph`
- `marginnote`
- `sidenote`
        
## History of this project

- The original repo: [shawnohare/hugo-tufte](https://github.com/shawnohare/hugo-tufte)
- Second repo: [slashformotion/hugo-tufte](https://github.com/slashformotion/hugo-tufte)
- This ([loikein/hugo-tufte](https://github.com/loikein/hugo-tufte)) is now the _de facto_ third repo although my original intension was only to make a few tweaks.


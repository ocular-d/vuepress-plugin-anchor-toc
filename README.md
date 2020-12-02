<div align="center">

# VuePress Anchor TOC Plugin

</div>

## Table of Contents

- [About the Project](#about)
- [Features](#features)
- [Install](#install)
- [Configuration](#configuration)
- [License](#license)
- [Credits](#credits)

## About

Adds **anchor navigation bar** to the right of the document page written in
[VuePress](https://vuepress.vuejs.org/ "Link to VuePress").

`vuepress-plugin-anchor-toc` is a shameless fork of [vuepress-plugin-right-anchor](https://github.com/xuekai-china/vuepress-plugin-right-anchor)!

See [credits](#credits)!

The only difference between these two is that `vuepress-plugin-anchor-toc` uses slightly different CSS settings and a TOC header ("On this page")

## Features

  - Simplify the structure of the left sidebar without losing the function of Title navigation within the page。
  - Click anchor label page over scrolling.
  - When the page scrolls, the corresponding anchor label follows the highlight.

## Install

```shell
yarn add vuepress-plugin-anchor-toc -D
# or
npm i vuepress-plugin-anchor-toc -D
```

Add to `.vuepress/config.js`

```js
module.exports = {
  // ...
  plugins: [
    // ...
    ['vuepress-plugin-anchor-toc']
  ]
}
```

## Configuration

Adjust the background color of the TOC.

Add to `.vuepress/styles/palette.styl`

```stylus
$rightAnchorBgColor = #fff
```

Set the "depth"

Add in `.vuepress/config.js`
```js
module.exports = {
  // ...
  plugins: [
    // ...
    [
      'vuepress-plugin-anchor-toc',
      {
        showDepth: 1,
        customClass: 'your-customClass'
        ignore: [
          '/',
          '/api/'
          // more...
        ]
      }
    ]
  ]
}
```

## Param description

### showDepth


Which level of title will be used in the right anchor display.
The pointing meaning of the value is the same as [themeconfig.sidebardepth](https://vuepress.vuejs.org/theme/default-theme-config.html).

- Type: null | number
- Default: null

### customClass

Your customClass for right-anchor.

- Type: null | string
- Default: null

### ignore

Don't show right-anchor's page.

- Type: array
- Default: []

## Page Config

Set `front-matter` by `vuepress` recommended method in `.md`.

```yaml
---
rightAnchor:
  showDepth: 1
  customClass: your-customClass
---
```

## License

Distributed under the [MIT](https://choosealicense.com/licenses/mit/ "Link to license") license.

## Credits

- [xuek](https://github.com/xuekai-china)


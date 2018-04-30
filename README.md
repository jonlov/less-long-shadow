# Long Shadow

This [LESS](http://lesscss.org/) and [SASS](http://sasscss.org/) loop mixins generates trendy flat long shadow with any angle for inline text, font icons, block elements and SVGs. Looks best if wrapped by square `overflow: hidden;` container with _bold_ padding and rounded corners. Dont forget about good contrast color palette. Enjoy!

* Source: [GitHub](https://github.com/jonlov/long-shadow)
* Demo: [CodePen](http://codepen.io/zensimilia/full/XbVgNx/)

## Installation

#### SASS

1. Make shure that you [installed](http://sasscss.org/) client or server-side SASS css-preprocessor
2. [Clone git repo](https://github.com/jonlov/long-shadow/fork) or [Download](https://github.com/jonlov/long-shadow/archive/master.zip) and copy `long-shadow.scss` to your _e.g._ `/assets/scss` directory.
3. Plug it to project by insert `@import "long-shadow.scss";` at beginning of main SCSS/CSS stylesheet file
4. Assign mixins to elements rules.
5. PROFIT

#### LESS
1. Make shure that you [installed](http://lesscss.org/) client or server-side LESS css-preprocessor
2. [Clone git repo](https://github.com/zensimilia/less-long-shadow/fork) or [Download](https://github.com/jonlov/long-shadow/archive/master.zip) and copy `long-shadow.less` to your _e.g._ `/assets/less` directory.
3. Plug it to project by insert `@import "long-shadow.less";` at beginning of main LESS/CSS stylesheet file
4. Assign mixins to elements rules.
5. PROFIT

## Usage

#### SASS
```scss
.someClass {
    @include long-shadow-inline($color, $angle, $size, $fade); // For text or icon
    @include long-shadow-block($color, $angle, $size, $fade, $prefix); // For container
    @include long-shadow-svg($color, $angle, $size, $fade, $prefix); // For SVG
}
```

#### LESS
```less
.someClass {
    #long-shadow.inline(@color, @angle, @size, @fade); // For text or icon
    #long-shadow.block(@color, @angle, @size, @fade, @prefix); // For container
    #long-shadow.svg(@color, @angle, @size, @fade, @prefix); // For SVG
}
```

## Params

* __@color__ of shadow _e.g._ `#00FFFF`, `@someVariable` or [`darken(#00FFFF)`](http://lesscss.org/functions/#color-operations-darken):
  * Default `#CCCCCC`.
* __@angle__ of shadow from 0 to 360. Zero meant horizontal shadow with right direction:
  * Default `45`.
* __@size__ that shadow length would be:
  * Default `10`.
* __@fade__ if the shadow should fade with opacity
  * `0` : _false_ Default
  * `1` : _true_ 
* __@prefix__ param define the use of CSS _browser-prefixes_ for `box-shadow` or `filter` rule:
  * `0` : _false_
  * `1` : _true_ Default

> Be careful with large values of the param `size` with client-side compiling. Using LESS in the browser is great for development, but it's not recommended for production due low performance.

## Contributing & Issues

Have a bug or a feature request? [Please open a new issue](https://github.com/zensimilia/less-long-shadow/issues). Before opening any issue, please search for existing issues.

## Changelog

__2.1.2__
* Added Sass file and fade option [Jonlov](https://github.com/jonlov).

__2.1.1__
* Fix default color var. Thanx to [Sergey Pimenov](https://github.com/olton).

__2.1.0__
* Add support for shadows on SVG by [Randall Bruder](https://github.com/randybruder).

__2.0.0__
* __INCOMPATIBLE CHANGES!__ Add _namespace_ and rename mixins.
* Add ability to specify an _angle_ of shadow. Idea [Mark Campbell](https://github.com/artsmc).
* Add option to choose whether to use _browser-prefixes_.
* Remove _spread_ parameter. Now total flat shadow.

__1.0.0__
* Initial release. [Di M Dub](https://twitter.com/zensimilia)

## License

[MIT License](LICENSE.md)

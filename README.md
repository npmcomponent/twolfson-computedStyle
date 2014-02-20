*This repository is a mirror of the [component](http://component.io) module [twolfson/computedstyle](http://github.com/twolfson/computedstyle). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/twolfson-computedstyle`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# computedStyle [![Donate on Gittip](http://badgr.co/gittip/twolfson.png)](https://www.gittip.com/twolfson/)

Cross-browser currentStyle/getComputedStyle implementation

[![testling-ci badge](https://ci.testling.com/twolfson/computedStyle.png)](https://ci.testling.com/twolfson/computedStyle)

## Getting Started
Download one of the available flavors:

- [Production version][min]
- [Development version][max] - Available via `bower install computedStyle`
- [CommonJS version][commonjs] - Available via `npm install computed-style` and `component install twolfson/computedStyle`
- [AMD version][amd]
- [140 bytes version][140]

[min]: https://raw.github.com/twolfson/computedStyle/master/dist/computedStyle.min.js
[max]: https://raw.github.com/twolfson/computedStyle/master/dist/computedStyle.js
[commonjs]: https://raw.github.com/twolfson/computedStyle/master/dist/computedStyle.commonjs.js
[amd]: https://raw.github.com/twolfson/computedStyle/master/dist/computedStyle.amd.js
[140]: https://raw.github.com/twolfson/computedStyle/master/dist/computedStyle.140.js

In your web page:

```html
<script src="dist/computedStyle.min.js"></script>
<script>
computedStyle(el, 'color'); // Returns color of the element
</script>
```

## Documentation
`computedStyle` is a single purpose function
```js
computedStyle(element, property);
/**
 * Cross-browser getComputedStyle
 * @param {HTMLElement} el Element to get property from
 * @param {String} prop Property to look up (DOM, zIndex, and CSS, z-index, formats accepted)
 * @returns Property from the browser
 *
 * @note These properties can vary from browser to browser.
 * For example, IE6 will return #FF0000 whereas Firefox will return rgb(255, 0, 0)
 * I have chosen to avoid this for this repo as it exits the single purpose
 * and jQuery follows the same approach.
 */
```

## Examples
```js
// Grab the z-index of an element
computedStyle(el, 'z-index');

// Grab the background-color of an element
computedStyle(el, 'background-color');
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint your code using [grunt][grunt] and test via `npm test`.

## License
Copyright (c) 2013 Todd Wolfson

Licensed under the MIT license.
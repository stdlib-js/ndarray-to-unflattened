<!--

@license Apache-2.0

Copyright (c) 2026 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# toUnflattened

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return a new [`ndarray`][@stdlib/ndarray/ctor] in which a specified dimension of an input [`ndarray`][@stdlib/ndarray/ctor] is expanded over multiple dimensions.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro section element. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import toUnflattened from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-to-unflattened@esm/index.mjs';
```

#### toUnflattened( x, dim, sizes )

Returns a new [`ndarray`][@stdlib/ndarray/ctor] in which a specified dimension of an input [`ndarray`][@stdlib/ndarray/ctor] is expanded over multiple dimensions.

```javascript
import array from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-array@esm/index.mjs';

var x = array( [ 1.0, 2.0, 3.0, 4.0, 5.0, 6.0 ] );
// returns <ndarray>[ 1.0, 2.0, 3.0, 4.0, 5.0, 6.0 ]

var y = toUnflattened( x, 0, [ 2, 3 ] );
// returns <ndarray>[ [ 1.0, 2.0, 3.0 ], [ 4.0, 5.0, 6.0 ] ]
```

The function accepts the following arguments:

-   **x**: input [`ndarray`][@stdlib/ndarray/ctor].
-   **dim**: dimension to be unflattened. If provided an integer less than zero, the dimension index is resolved relative to the last dimension, with the last dimension corresponding to the value `-1`.
-   **sizes**: new shape of the unflattened dimension.

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import uniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-discrete-uniform@esm/index.mjs';
import ndarray2array from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-to-array@esm/index.mjs';
import toUnflattened from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-to-unflattened@esm/index.mjs';

var x = uniform( [ 12 ], -100, 100 );
console.log( ndarray2array( x ) );

var y = toUnflattened( x, 0, [ 3, 4 ] );
console.log( ndarray2array( y ) );

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-to-unflattened.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-to-unflattened

[test-image]: https://github.com/stdlib-js/ndarray-to-unflattened/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/ndarray-to-unflattened/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-to-unflattened/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-to-unflattened?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-to-unflattened.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-to-unflattened/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/ndarray-to-unflattened/tree/deno
[deno-readme]: https://github.com/stdlib-js/ndarray-to-unflattened/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/ndarray-to-unflattened/tree/umd
[umd-readme]: https://github.com/stdlib-js/ndarray-to-unflattened/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/ndarray-to-unflattened/tree/esm
[esm-readme]: https://github.com/stdlib-js/ndarray-to-unflattened/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/ndarray-to-unflattened/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-to-unflattened/main/LICENSE

[@stdlib/ndarray/ctor]: https://github.com/stdlib-js/ndarray-ctor/tree/esm

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->

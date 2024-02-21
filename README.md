<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Object Entries

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return an array of an object's own and inherited enumerable property key-value pairs.



<section class="usage">

## Usage

```javascript
import objectEntriesIn from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-entries-in@esm/index.mjs';
```
The previous example will load the latest bundled code from the esm branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/utils-entries-in/tags). For example,

```javascript
import objectEntriesIn from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-entries-in@v0.2.1-esm/index.mjs';
```

#### objectEntriesIn( obj )

Returns an `array` of an object's own and inherited enumerable property `[key, value]` pairs.

```javascript
function Foo() {
    this.a = 1;
    return this;
}

Foo.prototype.b = 2;

var obj = new Foo();

var entries = objectEntriesIn( obj );
// e.g., returns [ ['a', 1], ['b', 2] ]
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   Entry order is not guaranteed, as `object` key enumeration is not specified according to the [ECMAScript specification][ecma-262-for-in]. In practice, however, most engines use insertion order to sort an `object`'s keys, thus allowing for deterministic return values.

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import objectEntriesIn from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-entries-in@esm/index.mjs';

function Foo() {
    this.beep = 'boop';
    this.a = {
        'b': 'c'
    };
    return this;
}

Foo.prototype.foo = [ 'bar' ];

var obj = new Foo();
var entries = objectEntriesIn( obj );

console.log( entries );
// e.g., => [ ['beep', 'boop'], ['a', {'b':'c'}], ['foo', [ 'bar' ]] ]

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/utils-entries`][@stdlib/utils/entries]</span><span class="delimiter">: </span><span class="description">return an array of an object's own enumerable property key-value pairs.</span>
-   <span class="package-name">[`@stdlib/utils-from-entries`][@stdlib/utils/from-entries]</span><span class="delimiter">: </span><span class="description">create an object from key-value pairs.</span>
-   <span class="package-name">[`@stdlib/utils-keys-in`][@stdlib/utils/keys-in]</span><span class="delimiter">: </span><span class="description">return an array of an object's own and inherited enumerable property names.</span>
-   <span class="package-name">[`@stdlib/utils-values-in`][@stdlib/utils/values-in]</span><span class="delimiter">: </span><span class="description">return an array of an object's own and inherited enumerable property values.</span>

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/utils-entries-in.svg
[npm-url]: https://npmjs.org/package/@stdlib/utils-entries-in

[test-image]: https://github.com/stdlib-js/utils-entries-in/actions/workflows/test.yml/badge.svg?branch=v0.2.1
[test-url]: https://github.com/stdlib-js/utils-entries-in/actions/workflows/test.yml?query=branch:v0.2.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/utils-entries-in/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/utils-entries-in?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/utils-entries-in.svg
[dependencies-url]: https://david-dm.org/stdlib-js/utils-entries-in/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/utils-entries-in/tree/deno
[deno-readme]: https://github.com/stdlib-js/utils-entries-in/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/utils-entries-in/tree/umd
[umd-readme]: https://github.com/stdlib-js/utils-entries-in/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/utils-entries-in/tree/esm
[esm-readme]: https://github.com/stdlib-js/utils-entries-in/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/utils-entries-in/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-entries-in/main/LICENSE

[ecma-262-for-in]: https://262.ecma-international.org/5.1/#sec-12.6.4

<!-- <related-links> -->

[@stdlib/utils/entries]: https://github.com/stdlib-js/utils-entries/tree/esm

[@stdlib/utils/from-entries]: https://github.com/stdlib-js/utils-from-entries/tree/esm

[@stdlib/utils/keys-in]: https://github.com/stdlib-js/utils-keys-in/tree/esm

[@stdlib/utils/values-in]: https://github.com/stdlib-js/utils-values-in/tree/esm

<!-- </related-links> -->

</section>

<!-- /.links -->

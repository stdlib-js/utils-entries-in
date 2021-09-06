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

# Object Entries

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Return an array of an object's own and inherited enumerable property key-value pairs.

<section class="installation">

## Installation

```bash
npm install @stdlib/utils-entries-in
```

</section>

<section class="usage">

## Usage

```javascript
var objectEntriesIn = require( '@stdlib/utils-entries-in' );
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

```javascript
var objectEntriesIn = require( '@stdlib/utils-entries-in' );

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
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   [`@stdlib/utils/entries`][@stdlib/utils/entries]: return an array of an object's own enumerable property key-value pairs.
-   [`@stdlib/utils/from-entries`][@stdlib/utils/from-entries]: create an object from key-value pairs.
-   [`@stdlib/utils/keys-in`][@stdlib/utils/keys-in]: return an array of an object's own and inherited enumerable property names.
-   [`@stdlib/utils/values-in`][@stdlib/utils/values-in]: return an array of an object's own and inherited enumerable property values.

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/utils-entries-in.svg
[npm-url]: https://npmjs.org/package/@stdlib/utils-entries-in

[test-image]: https://github.com/stdlib-js/utils-entries-in/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/utils-entries-in/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/utils-entries-in/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/utils-entries-in?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/utils-entries-in.svg
[dependencies-url]: https://david-dm.org/stdlib-js/utils-entries-in/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-entries-in/main/LICENSE

[ecma-262-for-in]: http://www.ecma-international.org/ecma-262/5.1/#sec-12.6.4

<!-- <related-links> -->

[@stdlib/utils/entries]: https://github.com/stdlib-js/utils-entries

[@stdlib/utils/from-entries]: https://github.com/stdlib-js/utils-from-entries

[@stdlib/utils/keys-in]: https://github.com/stdlib-js/utils-keys-in

[@stdlib/utils/values-in]: https://github.com/stdlib-js/utils-values-in

<!-- </related-links> -->

</section>

<!-- /.links -->

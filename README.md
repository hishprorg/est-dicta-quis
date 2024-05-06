# @hishprorg/est-dicta-quis <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@hishprorg/est-dicta-quis');
const ToObject = require('@hishprorg/est-dicta-quis/ToObject');
const RequireObjectCoercible = require('@hishprorg/est-dicta-quis/RequireObjectCoercible');

assert.equal($Object, Object);
assert.throws(() => ToObject(null), TypeError);
assert.throws(() => ToObject(undefined), TypeError);
assert.throws(() => RequireObjectCoercible(null), TypeError);
assert.throws(() => RequireObjectCoercible(undefined), TypeError);

assert.deepEqual(RequireObjectCoercible(true), true);
assert.deepEqual(ToObject(true), Object(true));

const obj = {};
assert.equal(RequireObjectCoercible(obj), obj);
assert.equal(ToObject(obj), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@hishprorg/est-dicta-quis
[npm-version-svg]: https://versionbadg.es/ljharb/@hishprorg/est-dicta-quis.svg
[deps-svg]: https://david-dm.org/ljharb/@hishprorg/est-dicta-quis.svg
[deps-url]: https://david-dm.org/ljharb/@hishprorg/est-dicta-quis
[dev-deps-svg]: https://david-dm.org/ljharb/@hishprorg/est-dicta-quis/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@hishprorg/est-dicta-quis#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@hishprorg/est-dicta-quis.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@hishprorg/est-dicta-quis.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@hishprorg/est-dicta-quis
[codecov-image]: https://codecov.io/gh/ljharb/@hishprorg/est-dicta-quis/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@hishprorg/est-dicta-quis/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@hishprorg/est-dicta-quis
[actions-url]: https://github.com/hishprorg/est-dicta-quis/actions

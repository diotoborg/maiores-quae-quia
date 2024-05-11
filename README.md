# @diotoborg/maiores-quae-quia <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@diotoborg/maiores-quae-quia');
const ToObject = require('@diotoborg/maiores-quae-quia/ToObject');
const RequireObjectCoercible = require('@diotoborg/maiores-quae-quia/RequireObjectCoercible');

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

[package-url]: https://npmjs.org/package/@diotoborg/maiores-quae-quia
[npm-version-svg]: https://versionbadg.es/ljharb/@diotoborg/maiores-quae-quia.svg
[deps-svg]: https://david-dm.org/ljharb/@diotoborg/maiores-quae-quia.svg
[deps-url]: https://david-dm.org/ljharb/@diotoborg/maiores-quae-quia
[dev-deps-svg]: https://david-dm.org/ljharb/@diotoborg/maiores-quae-quia/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@diotoborg/maiores-quae-quia#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@diotoborg/maiores-quae-quia.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@diotoborg/maiores-quae-quia.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@diotoborg/maiores-quae-quia
[codecov-image]: https://codecov.io/gh/ljharb/@diotoborg/maiores-quae-quia/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@diotoborg/maiores-quae-quia/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@diotoborg/maiores-quae-quia
[actions-url]: https://github.com/diotoborg/maiores-quae-quia/actions

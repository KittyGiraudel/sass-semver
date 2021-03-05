# Sass SemVer

A Sass implementation of [node-semver](https://github.com/npm/node-semver). This project is inspired by [sass-deprecate](https://github.com/salesforce-ux/sass-deprecate) from Salesforce.

```sh
npm install sass-semver
```

## Public API

* `valid($version)`  
  Returns whether `$version` a is valid SemVer version.
* `clean($version)`  
  Returns version without leading `v` or `=`.
* `inc($version, $release)`  
  Returns `$version` with incremented `$release` component.
* `major($version)`  
  Returns major component from `$version`.
* `minor($version)`  
  Returns minor component from `$version`.
* `patch($version)`  
  Returns patch component from `$version`.
* `gt($v1, $v2)`  
  Returns whether `$v1` is greater than `$v2` (i.e. `$v1 > $v2`).
* `gte($v1, $v2)`  
  Returns whether `$v1` is greater than or equal to `$v2` (i.e. `$v1 >= $v2`).
* `lt($v1, $v2)`  
  Returns whether `$v1` is lesser than `$v2` (i.e. `$v1 < $v2`).
* `lte($v1, $v2)`  
  Returns whether `$v1` is lesser than or equal to `$v2` (i.e. `$v1 <= $v2`).
* `eq($v1, $v2)`  
  Returns whether `$v1` is equal to `$v2` (i.e. `$v1 == $v2`).
* `neq($v1, $v2)`  
  Returns whether `$v1` is not equal to `$v2` (i.e. `$v1 != $v2`).
* `cmp($v1, $comparator, $v2)`  
  Calls the corresponding function above depending on which `$comparator` is being given. Warning: `===` and `!==` perform string comparison, which `==` and `!=` call `eq` and `neq` methods.

## Tests

```sh
npm test
```

## Build dist file

```
npm run build
```

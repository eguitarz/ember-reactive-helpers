# ember-reactive-helpers

[![Build Status](https://travis-ci.org/EmberSherpa/ember-reactive-helpers.svg)](https://travis-ci.org/EmberSherpa/ember-reactive-helpers)
[![npm version](https://badge.fury.io/js/ember-reactive-helpers.svg)](http://badge.fury.io/js/ember-reactive-helpers)
[![Code Climate](https://codeclimate.com/github/EmberSherpa/ember-reactive-helpers/badges/gpa.svg)](https://codeclimate.com/github/EmberSherpa/ember-reactive-helpers)
[![Test Coverage](https://codeclimate.com/github/EmberSherpa/ember-reactive-helpers/badges/coverage.svg)](https://codeclimate.com/github/EmberSherpa/ember-reactive-helpers/coverage)
[![Dependency Status](https://david-dm.org/EmberSherpa/ember-reactive-helpers.svg)](https://david-dm.org/EmberSherpa/ember-reactive-helpers)

Collection of helpers to aid in reactive template programming with Ember.js.

## Helpers

### `(helper 'helperName')`

Will resovle the helper and return resolved helper. 

### `(closure helper arg1 arg2)`

`(closure` helper accepts a helper as first argument and creates a closure and curries the passed in arguments.
When you call the returned helper the helper will becalled with all passed in arguments.

```js
{{#with (closure 'contains' (array 'foo' 'bar')) as |checkContains|}}
  {{compute (checkContains 'foo')}}
{{/with}}
```

### `{{shhh anything}}`

`{{shhh` helper will supress any output that's passed into it. This is useful when you want to compute a helper 
without having it's output rendered.

## Installation

```
ember install ember-reactive-helpers
```

## Helpful Links

- ### [Live Demo](http://EmberSherpa.github.io/ember-reactive-helpers)

- ### [Changelog](CHANGELOG.md)

## Looking for help?
If it is a bug [please open an issue on GitHub](http://github.com/EmberSherpa/ember-reactive-helpers/issues).

## Usage
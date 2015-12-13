[![Build Status](https://travis-ci.org/cibernox/ember-power-select-blockless.svg)](https://travis-ci.org/cibernox/ember-power-select-blockless)
[![Code Climate](https://codeclimate.com/github/cibernox/ember-power-select-blockless/badges/gpa.svg)](https://codeclimate.com/github/cibernox/ember-power-select-blockless)
[![Ember Observer Score](http://emberobserver.com/badges/ember-power-select-blockless.svg)](http://emberobserver.com/addons/ember-power-select-blockless)

# Ember-power-select-blockless

Blockless version of [Ember Power Select](https://github.com/cibernox/ember-power-select)

## Installation

`ember install ember-power-select-blockless`

## Usage

This component uses internally ember-power-select, but uses the `get` helper to render an specific attribute
in each item of the list.

All options are the same than those in ember-power-select with the addition of a new one, `labelPath`,
which tells the component which attribute of each option should use to render each option of the list
as well as the content of the trigger.

```hbs
{{power-select-blockless options=users selected=user labelPath="name" onchange=(action (mut user))}}
```

Another refinement is that by default the `searchField` will default to the value in `labelPath`, so
you don't need to specify it unless it's different.

When `options` is just an array of strings/numbers `labelPath` is not required.

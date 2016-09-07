---
title: Button
order: 5
---

A bunch of buttons with different color and size.

## Button

usage:

``` html
<template>
  <m-button>Button</m-button>
  <m-button type="danger">Danger Button</m-button>
  <m-button size="large">Large Button</m-button>
  <m-button :disabled="true">Disabled Button</m-button>
  <m-button :round="true">Round Button</m-button>
  <m-button :bordered="true">Bordered Button</m-button>
</template>

<script>
  import { Button } from 'components/button'
</script>
```

Props:

Prop | Type | Default | Required | Description
-----|------|---------|----------|------------
`type` | `String` | `default` | false | different type of button(with different color): `default`, `light`, `danger`, `warning`, `success`
`size` | `String` | `medium` | false | different size of button: `small`, `medium`, `large`
`round` | `Boolean` | `false` | false | round button
`active` | `Boolean` | `false` | false | make the button active
`disabled` | `Boolean` | `false` | false | make the button disabled
`borderd` | `Boolean` | `false` | false | bordered button (border instead of background)

## Button group

A group of buttons with specified style.

usage:

``` html
<template>
  <button-group :bordered="true" size="small">
    <m-button>Button 1</m-button>
    <m-button>Button 2</m-button>
    <m-button>Button 3</m-button>
  </button-group>
</template>

<script>
  import { Button, ButtonGroup } from 'components/button'
</script>
```

You can use these props on `ButtonGroup`, all the buttons in button group will be changed:

Prop | Type | Default | Required | Description
-----|------|---------|----------|------------
`type` | `String` | `default` | false | different type of button(with different color): `default`, `light`, `danger`, `warning`, `success`
`size` | `String` | `medium` | false | different size of button: `small`, `medium`, `large`
`round` | `Boolean` | `false` | false | round button
`disabled` | `Boolean` | `false` | false | make the button disabled
`borderd` | `Boolean` | `false` | false | bordered button (border instead of background)

Set `:active="true"` on a button to make it active:

``` html
<button-group :bordered="true" size="small">
  <m-button :active="true">Button 1</m-button>
  <m-button>Button 2</m-button>
  <m-button>Button 3</m-button>
</button-group>
```

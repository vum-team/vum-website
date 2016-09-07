---
title: Header
order: 3
---

## All Header Components

Header contains five components: `Header`, `SecondHeader`, `SimpleHeader`, `HeaderTitle`, `HeaderLink`.

``` javascript
import { Header, SecondHeader, SimpleHeader, Title, Link } from 'components/header'
```

- `Header` is fixed on the top of screen, you can put `Title` and `Link` in header
- `SecondHeader` is fixed on the top of screen, but comes after `Header`, any valid component can be put in `SecondHeader`
- `SimpleHeader` is a predefined `Header` with a `Title` and an optional back link
- `HeaderTitle` is the title of the page, center in `Header`. Every `Header` should contain a `Title`
- `HeaderLink` is a text link or icon link in header.

## Header Layout

Layout of header like this:

``` html
<template>
  <page-header>
    <header-link :left="true" :edge="true" v-back-link><icon icon="back"></icon>Back</header-link>
    <header-link>About</header-link>
    <header-title>VUM</header-title>
  </page-header>
</template>

<script>
import { Header, HeaderLink, HeaderTitle} from '../components/header'
</script>
```

## Header Link

Header Link could only be used in `Header`

Usage:

``` html
<template>
  <header-link :left="true" :edge="true" v-back-link><icon icon="back"></icon>Back</header-link>
</template>

<script>
import { HeaderLink } from '../components/header'
export default {
  components: {
    'header-link': HeaderLink
  }
}
</script>
```

Props:

Prop | Type | Default | Required | Description
-----|------|---------|----------|------------
`left` | `Boolean` | `false` | false | float left in `Header`
`edge` | `Boolean` | `false` | false | more close to the edge of `Header`

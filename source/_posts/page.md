---
title: Page
order: 1
---

## Page Layout

Vum defined the layout for every page, so we can write a native-like webapp.

Let's look the default layout for a specify page:

``` html
<div class="page">
  <page-header>
    <header-title>VUM</header-title>
    some more header item...
  </page-header>
  <page-footer>
    some more footer item...
  </page-footer>
  <content>
    put your page content here
  </content>
</div>
```

`<div class="page"></div>` is the container for every page. Please make sure that you have put `header` and `footer` before `content` in the template.

## Header

Header is a fixed bar at the top of the screen that contains Page Title and some navigation buttons.

``` html
<template>
  <page-header>
    <header-link :left="true" :edge="true" v-back-link><icon icon="back"></icon>Back</header-link>
    <header-link>About</header-link>
    <header-title>VUM</header-title>
  </page-header>
</template>

<script>
  import { Header, Link, Title } from '../components/header'
  export default {
    components: {
      'page-header': header,
      'header-link': Link,
      'header-title': Title
    }
  }
</script>
```

`header-title` is the title for this page which put at the center of header.
`header-link` float at the left|right of the header.

### Simple Header

Most time you will only need a header with a title and a back link, the `SimpleHeader` component is pretty good for you at this time.

``` html
<template>
  <simple-header title="Form" :back-link="true"></simple-header>
</template>
<script>
  import { SimpleHeader } from '../components/header'
</script>
```

## Page Footer

Footer is a tab bar fixed at the bottom of the screen.

``` html
<page-footer>
  <footer-item>
    <span class="icon demo-icon-home"></span>
    <label>Home</label>
  </footer-item>
  <footer-item>
    <span class="icon demo-icon-search"></span>
    <label>Search</label>
  </footer-item>
  <footer-item>
    <span class="icon demo-icon-noti"></span>
    <span class="badge">2</span>
    <label>Noti</label>
  </footer-item>
</page-footer>
```

It's recommend to use tab instead of router to change view when click footer.

## Second Header and Second Footer

Refer to [demos](http://demo.getvum.com) please for how to use `SecondHeader` and `SecondFooter` please.

---
title: Footer
order: 4
---

Footer is a fixed area at the bottom of the screen. It's used to navigate the app.

## Layout

``` html
<template>
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
    <footer-item>
      <span class="icon demo-icon-me"></span>
      <label>About</label>
    </footer-item>
  </page-footer>
</template>

<script>
import { Footer, FooterItem } from 'components/footer'
</script>
```

Note: Footer should come before `Content` in template

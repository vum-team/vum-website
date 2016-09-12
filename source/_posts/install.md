---
title: Install
order: 1
---

## Create Project

First, let's create a project, [vue-cli](https://github.com/vuejs/vue-cli) is recommend

``` bash
vue init webpack my-vum-project
```

Then, init the project

``` bash
cd my-vum-project
npm install
```

And, your project should use vue-router, refer to [vue-router docs](http://router.vuejs.org/en/basic.html) for more info.

## Install Vum

Install vum via npm

``` bash
npm install --save vum
```

Note! Vum require `less-loader`, please make sure you have install `less-loader`.

## config loader in webpack config

To import vum, we should config the loader in webpack first.

Add these code in webpack loaders

``` bash
{
  test: /vum\/components\/.*/,
  loader: 'vue'
},
{
  test: /vum\/.*\.js/,
  loader: 'babel'
}
```

## Import Vum and Enjoy it

``` bash
import Vue from 'vue'
import Router from 'vue-router'

import Vum from 'vum' // import vum

Vue.use(Router)
Vue.use(Vum) // use vum

let App = Vue.extend()

let router = new Router()

router.map({
  // ...
})

router.start(App, '#app')

Vum.router(router)  // config router instance by vum
```

``` bash
<template>
  <div class="page">
    <simple-header title="my-vum" :back-link="true"></simple-header>
    <content>
      <div class="content-padded">
        <h1>Hello Vum!</h1>
      </div>
    </content>
  </div>
</template>

<script>
import Page from '../../node_modules/vum/src/components/page'
import {SimpleHeader} from '../../node_modules/vum/src/components/header'
import Content from '../../node_modules/vum/src/components/content'

export default {
  components: {
    Page,
    Content,
    SimpleHeader
  }
}
</script>
````

## use template

Don't want to config vum by yourself?  You can just clone the [vum-project-template](https://github.com/vum-team/vum-project-template), and start write your code immidiately.

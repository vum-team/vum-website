---
title: List
order: 6
---

The style of List comes from [Framework7](http://framework7.io/docs/list-view.html)

List views have many purposes:

- To let users navigate through hierarchically structured data
- To present an indexed list of items
- To display detail information and controls in visually distinct groupings
- To present a selectable list of options

## Layout

The layout of List:

``` html
<list>
  <div slot="title">Simple List</div>
  <list-item>
    ...
  </list-item>
  <list-item>
    ...
  </list-item>
  <div slot="append">
    Append some message here.
  </div>
</list>
```

``` javascript
import { List, ListItem } from '../components/list'
```

## List Title

You can set title on a list with slot:

``` html
<list>
  <div slot="title">Title of List</div>
  <list-item>
    ...
  </list-item>
  <list-item>
    ...
  </list-item>
  <div slot="append">
    Append some message here.
  </div>
</list>
```

## Simple List

Simple List with only a title and a after:

``` html
<list>
  <list-item>
    <div class="item-content">
      <div class="item-title-row">
        <div class="item-title">Title</div>
        <div class="item-after">After</div>
      </div>
    </div>
  </list-item>
  <list-item>
  ...
  </list-item>
</list>
```

## List With Icon

``` html
<list>
  <list-item>
    <div class="item-media"><img src="..." width="30"></div>
    <div class="item-content">
      <div class="item-title-row">
        <div class="item-title">Title</div>
        <div class="item-after">After</div>
      </div>
    </div>
  </list-item>
</list>
```

## With Switch and Badge

You can put `Switch` and `Badge` in `item-after`:

``` html
<list>
  <list-item>
    <div class="item-content">
      <div class="item-title-row">
        <div class="item-title">Title</div>
        <div class="item-after">
          <switch></switch>
        </div>
      </div>
    </div>
  </list-item>
  <list-item>
    <div class="item-content">
      <div class="item-title-row">
        <div class="item-title">Title</div>
        <div class="item-after">
          <div class="badge">32</div>
        </div>
      </div>
    </div>
  </list-item>
</list>
```

## Media List With Subtitle and optional text

``` html
<list>
  <list-item>
    <div class="item-media"><img src="../assets/images/icon-list.png" width="88"></div>
    <div class="item-content">
      <div class="item-title-row">
        <div class="item-title">Title</div>
        <div class="item-after">After</div>
      </div>
      <div class="item-subtitle">
        Subtitle
      </div>
      <div class="item-text">
        Text Text Text Text Text Text Text Text Text 
      </div>
    </div>
  </list-item>
</list>
```

## Selectable List

You can put radio or checkbox in List to make it selectable:

radio list:

``` html
<list>
  <div slot="title">Radio List</div>
  <list-item :radio="true">
    <input type="radio" name="gender" value="1">
    <div class="item-media"><img src="../assets/images/icon-list.png" width="44"></div>
    <div class="item-content">
      ...
    </div>
  </list-item>
  <list-item :radio="true">
    <input type="radio" name="gender" value="2" checked>
    <div class="item-media"><img src="../assets/images/icon-list.png" width="44"></div>
    <div class="item-content">
    ...
    </div>
  </list-item>
</list>
```

checkbox list:

``` html
<list>
  <div slot="title">Checkbox List</div>
  <list-item :checkbox="true">
    <input type="checkbox" name="name" value="A">
    <div class="item-media"><img src="../assets/images/icon-list.png" width="44"></div>
    <div class="item-content">
      ...
    </div>
  </list-item>
  <list-item :checkbox="true">
    <input type="checkbox" name="name" value="B">
    <div class="item-media"><img src="../assets/images/icon-list.png" width="44"></div>
    <div class="item-content">
      ...
    </div>
  </list-item>
</list>
```

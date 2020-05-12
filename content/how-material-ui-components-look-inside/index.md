---
title: "How Material UI components look inside"
description: "In the article I would like to show how most important parts of basic components  of Material UI look in WYSIWIG Chrome Devtools (HTML and…"
date: "2020-05-12T09:01:43.313Z"
categories: []
published: false
---

In the article I would like to show how most important parts of basic components of [Material UI](https://material-ui.com/) look in WYSIWIG Chrome Devtools (HTML and CSS).

[**AppBar**](https://material-ui.com/demos/app-bar/)

TODO insert image here

TODO short description

React:

```
<AppBar position="fixed">
  <Toolbar>
    <Typography variant="h6">
      Text
    </Typography>
    <div className={classes.grow} />
    <Button>Button</Button>
  </Toolbar>
</AppBar>
```

HTML:

```
<header class="app-bar">
  <div class="inner-box">
    <h6 class="title">Text</h6>
    <div class="empty-space"></div>
    <button>Button</button>
  </div>
</header>
```

CSS:

```
.app-bar {
  /* Minimum required for app bar */
  position: fixed;
  width: 100%;
  top: 0;
  right: 0;

  /* App bar colors and shadows */
  color: #fff;
  background-color: #2196f3;
  box-shadow: 0px 2px 4px -1px rgba(0, 0, 0, 0.2), 0px 4px 5px 0px rgba(0, 0, 0, 0.14), 0px 1px 10px 0px rgba(0, 0, 0, 0.12);
}

.inner-box {
  /* App bar inner single div (parent for title and buttons) */
  display: flex;
  align-items: center;

  /* App bar inner single div sizes  */
  min-height: 56px;
  padding-left: 16px;
  padding-right: 16px;
}

@media (min-width: 600px) {
  /* App bar inner single div sizes overrides */
  .inner-box {
    min-height: 64px;
    padding-left: 24px;
    padding-right: 24px;
  }
}

.title {
  /* Font customizations */
  margin: 0;
  font-size: 1.25rem;
  font-family: "Roboto", "Helvetica", "Arial", sans-serif;
  font-weight: 500;

  /* Large text ellipsis */
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.empty-space {
  /* Growing and shrinking divider between text and button */
  flex: 1 1 auto;
}
```

[https://codesandbox.io/s/r5zzl19rrq](https://codesandbox.io/s/r5zzl19rrq)

**Avatar**

React:

```
<Avatar alt="Alex Soroka" src="https://lehasvv2009.github.io/resume/avatar.jpeg" />
```

HTML:

```
<div class="avatar">
  <img class="image" alt="Alex Soroka" src="https://lehasvv2009.github.io/resume/avatar.jpeg" />
</div>
```

CSS:

```
.avatar {
  width: 60px;
  height: 60px;
  overflow: hidden;
  border-radius: 50%;
}

.image {
  height: 100%;
}
```

**Button**

TODO insert image

TODO insert description

Ripple is implemented as a combination of JS (detect cursor point) and CSS animation.

React:

```
<Button variant="contained" color="primary">
  Primary
</Button>
```

HTML:

```
<button class="button">
  <span>Primary</span>
  <span class="ripple-effect-text-wrapper"></span>
</button>
```

JavaScript:

```


```

CSS:

```


```

**Dialog**

TODO insert image

TODO insert description

React:

```
<Dialog open>
  <h1>Title</h1>
  <div>Content</div>
</Dialog> 
```

HTML:

```
<div class="dialog">
  <div class="overlay"></div>
  <div class="centerer">
    <div class="paper">
      <h1>Title</h1>
      <div>Content</div>
    </div>
  </div>
</div>
```

CSS:

```
.dialog {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 1300;
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
  background-color: rgba(0, 0, 0, 0.5);
}

.centerer {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 30px;
}

.paper {
  background-color: white;
  border-radius: 4px;
  padding: 16px;
  box-shadow: 0px 11px 15px -7px rgba(0, 0, 0, 0.2), 0px 24px 38px 3px rgba(0, 0, 0, 0.14), 0px 9px 46px 8px rgba(0, 0, 0, 0.12);
}
```

**Drawer**

React:

```
<Drawer open={true}>
  My drawer         
</Drawer>
```

HTML:

```
<div class="drawer">
  <div class="overlay"></div>
  <div class="layout">
    <div class="content">
      My drawer
    </div>
  </div>
</div>
```

CSS:

```
.drawer {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 1300;
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
  background-color: rgba(0, 0, 0, 0.5);
}

.layout {
  width: 150px;
  height: 100%;
  left: 0;
  right: auto;
}

.content {
  background-color: white;
  height: 100%;
  overflow-y: auto;
}
```

**Grid**

React:

```
<Grid container>
  <Grid item xs={12} sm={6}>Half</Grid>
  <Grid item xs={6} sm={3}></Grid>
  <Grid item xs={6} sm={3}></Grid>
</Grid>
```

HTML:

```
<div class="container">
  <div class="item xs-12 sm-6">
    Half or Full
  </div>
  <div class="item xs-6 sm-3">
    Quarter1 or Half1
  </div>
  <div class="item xs-6 sm-3">
    Quarter2 or Halh2
  </div>
</div>
```

CSS:

```
* {
  box-sizing: border-box;
}

.container {
  display: flex;
  flex-wrap: wrap;
}

.item {
  padding: 12px;
}

.xs-12 {
  flex-basis: 100%;
}

.xs-6 {
  flex-basis: 50%;
}

@media screen and (min-width: 600px) {
  .sm-6 {
    flex-basis: 50%;
  }

  .sm-3 {
    flex-basis: 25%;
  }
}
```

**Icon**

**List**

**Menu**

React:

```


```

**Paper**

**Progress**

**Switch**

**Snackbar**

**Table**

**Tabs**

**Textfield**

**Tooltip**

React:

```
<Tooltip title="Add">
  <div>Bla</div>
</Tooltip>
```

HTML:

```
<div class="tooltip">
  <div class="tooltip-label">
    Add
  </div>
</div>
```

CSS:

```
.tooltip {
  position: absolute;
  /* Line that must be calculated by JS */
  transform: translate3d(145px, 93px, 0px);
  top: 0px;
  z-index: 1500;
  opacity: 0.9;
}

.tooltip-label {
  opacity: 1;
  transform: scale(1, 1) translateZ(0px);
  transition: opacity 200ms cubic-bezier(0.4, 0, 0.2, 1) 0ms, transform 133ms cubic-bezier(0.4, 0, 0.2, 1) 0ms;
  margin: 14px 0;
  color: #fff;
  padding: 4px 8px;
  font-size: 0.625rem;
  font-family: "Roboto", "Helvetica", "Arial", sans-serif;
  line-height: 1.4em;
  border-radius: 4px;
  background-color: #616161;
}
```

**Typography**

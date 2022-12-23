[![NavarroTech Logo](http://www.navarrotech.net/logo.svg)](http://www.navarrotech.net/)

  Upgraded [Bulma.io](http://bulma.io) package with extended functionality.

## Features

  * More modifiers!
  * New elements
  * New components
  * React.js Compatibility

## Installation

This is a [Node.js](https://nodejs.org/en/) module available through the
[npm registry](https://www.npmjs.com/).

Before installing, [download and install Node.js](https://nodejs.org/en/download/).
Node.js 0.10 or higher is required.

You can follow the [`instructions on Bulma.io`](https://bulma.io/documentation/customize/with-node-sass/) for customizing and using our package.

Instead of importing 'bulma/bulma', you would import 'bulma-navarrotech'
```
@charset "utf-8";
// Import all extensions
@import "../node_modules/bulma-navarrotech/bulma.sass";
// Or just import specific extensions
@import "../node_modules/bulma-navarrotech/src/NavarroTech/Addons/_all.sass";
@import "../node_modules/bulma-navarrotech/src/NavarroTech/Components/subcontainer.sass";
```

## More modifiers!

*** Image Addons ***

This is one of my personal favorites, I use this way too much.

You can now add class ***is-centered*** or  ***is-right*** to center your image elements!

```
<figure class="image is-16by9 is-centered">
    <img/>
</figure>
```

We also ran into a lot of issues in our code, where we needed to show a square or vertical image in a 16by9 container.

To help fix issues with images looking "squished" we added class "not-forced" which allows the image to preserve it's own ratio inside the image container.

```
<figure class="image is-16by9 not-forced">
    <img source="a-square-image" alt="I don't want to be stretched!"/>
</figure>
```

*** Box Addons ***

You can now add class ***is-centered*** or  ***is-right*** or  ***is-left*** to your boxes, and it will add width: fit-content

You can also color the boxes using is-primary or is-{custom-color}, and it will set the background to that color!
(Note: You will need to alter the text color yourself)

```
<div class="box is-centered is-primary">
    <img/>
</div>
```

*** Remove number arrows from number inputs ***

Adding class ***no-arrows*** will remove arrows from number inputs!
```
<input type="number" class="input no-arrows"></input>
```

*** Improved level items ***

```
<div class="level has-gap">
  <div class="box">
    <h1>We are not touching anymore thanks to class 'has-gap!'</h1>
  </div>
  <div class="box">
    <h1>We are not touching anymore thanks to class 'has-gap!'</h1>
  </div>
  <div class="level-right is-centered-mobile">
    <h2>This text will be right on desktop but centered on mobile!</h2>
  </div>
</div>
```

*** More typography helpers ***
```
<h1 class="title is-bold">
  This text will have the font-weight of bold!
</h1>
<h2 class="title is-black">
  This text will have the font-weight of black!
</h2>
<h3 class="title has-text-weight-black">
  This text will also have the font-weight of black!
</h3>
```

## New Components

*** Toggle Switch ***
```
<label class="switch is-rounded is-primary">
    <input type="checkbox">
    <span class="slider"></span>
</label>
```

*** Subcontainers ***
This is useful for things like login windows, and single panelled sections.

Supported sizes:
...is-tablet: $tablet
...is-desktop: $desktop
...is-widescreen: $widescreen
...is-large: $large (default: 1300px)
...is-medium: $medium (default: 1000px)
...is-small: $small (default: 900px)
...Column sizes (is-1, is-2, is-3, etc...)

```
<div class="container is-max-widescreen">
  <div class="subcontainer is-medium">
    <div class="box">
      <h1 class="title has-text-centered">Hello World!</h1>
    </div>
  </div>
</div>
```

## Elements

*** Multi Progress Bars ***
Put multiple progressbars into one!
You can color each segment individually. Use ***style="width: 33%"*** to determine width.
```
<div class="multi-progress is-normal">
    <div class="progress-item is-primary" style="width: 50%">
        <span class="icon">
            <i class="fa-solid fa-jedi"></i>
        </span>
        <span>Put text, icons, any HTML here!</span>
    </div>
    <div class="progress-item is-link" style="width: 25%"></div>
    <div class="progress-item is-warning" style="width: 5%"></div>
</div>
```

## React.js Compatibility
*** Menus ***

The old way:
```
<aside className="menu">
  <p className="menu-label">
    General
  </p>
  <ul className="menu-list">
    <li><a>Dashboard</a></li> // <-- Not React Compatible!
    <li><a>Customers</a></li> // <-- <a> tags can cause issues with routers!
  </ul>
</aside>
```
The new way:
```
<aside className="menu">
  <p className="menu-label">
    General
  </p>
  <ul className="menu-list">
    <li><div className="menu-item">Dashboard</div></li>
    <li><div className="menu-item">Customers</div></li>
  </ul>
</aside>
```

*** Tabs ***

The old way:
```
<div className="tabs">
  <ul>
    <li><a>Item A</a></li> // <-- Not React Compatible!
    <li><a>Item B</a></li> // <-- <a> tags can cause issues with routers!
    <li className="is-active"><a>Item C</a></li>
  </ul>
</div>
```
The new way:
```
<div className="tabs">
  <ul>
    <li><div className="tab">Item A</div></li>
    <li><div className="tab">Item B</div></li>
    <li className="is-active"><a className="tab">Item C</a></li>
  </ul>
</div>
```

## People

The original author of Bulma is [Jeremy Thomas](https://jgthms.com/)

The current lead maintainer is [Alex Navarro](https://www.navarrocity.com/about)

## License

  [MIT](LICENSE)
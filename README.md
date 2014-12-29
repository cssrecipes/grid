# grid

> BEMish grid component

## Install

```console
$ npm install cssrecipes-grid
```

```css
@import "./node_modules/cssrecipes-grid/index.css";
```

_Advice: you can use size utilities from [`cssrecipes-utils`](http://github.com/cssrecipes/utils) for convenience.  
It includes `.r-(all|min|max)*` classes used in the examples below to define grid cells width._

### Recommanded install 👌

```console
$ npm install cssrecipes-utils cssrecipes-grid
```

```css
@import "./node_modules/cssrecipes-custom-media-queries/index.css";
@import "./node_modules/cssrecipes-grid/index.css";
/* all, max (desktop first), min (mobile first) */
@import "./node_modules/cssrecipes-utils/index.css";

/*
  Refer to cssrecipes-utils install doc to know more.
  https://github.com/cssrecipes/utils#install

  Or check examples below.
*/
```

## Usage

First of all, you can override all these custom properties according to your needs (here are default values):

```css
:root {
  --r-Grid-baseFontSize: 1rem;
  --r-Grid-baseFontSizeFallback: 16px;
  --r-Grid-gutter: 1rem; /* used for .r-Grid--withGutter */
}
```

### Mobile-first

#### Include deps

```css
@import "./node_modules/cssrecipes-custom-media-queries/index.css";
@import "./node_modules/cssrecipes-grid/index.css";
@import "./node_modules/cssrecipes-utils/lib/all.css";
@import "./node_modules/cssrecipes-utils/lib/min.css";
```

#### Define your `Grid` size

```css
.r-Grid {
  width: auto;
}

@media (--r-minM) {
  .r-Grid {
    width: 30rem;
  }
}

@media (--r-minL) {
  .r-Grid {
    width: 50rem;
  }
}

/** and the rest of it */
```

#### Use your grid

```html
<div class="r-Grid">
  <div class="r-Grid-cell r-all--1of2 r-minM--1of3 r-minL--1of4">
    <!-- your content-->
  </div>
  <div class="r-Grid-cell r-all--1of2 r-minM--2of3 r-minL--3of4">
    <!-- your content-->
  </div>
</div>
```

### Desktop-first

#### Include deps

```css
@import "./node_modules/cssrecipes-custom-media-queries/index.css";
@import "./node_modules/cssrecipes-grid/index.css";
@import "./node_modules/cssrecipes-utils/lib/all.css";
@import "./node_modules/cssrecipes-utils/lib/max.css";
```

#### Define your `Grid` size

```css
.r-Grid {
  width: auto;
}

@media (--r-maxL) {
  .r-Grid {
    width: 50rem;
  }
}

@media (--r-maxM) {
  .r-Grid {
    width: 30rem;
  }
}

/** and the rest of it */
```

#### Use your grid

```html
<div class="r-Grid">
  <div class="r-Grid-cell r-all--1of4 r-maxL--1of3 r-maxM--1of2">
    <!-- your content-->
  </div>
  <div class="r-Grid-cell r-all--3of4 r-maxL--2of3 r-maxM--1of2">
    <!-- your content-->
  </div>
</div>
```

### Without responsive

#### Include deps

```css
@import "./node_modules/cssrecipes-grid/index.css";
@import "./node_modules/cssrecipes-utils/lib/all.css";
```

#### Define your `Grid` size

```css
.r-Grid {
  width: 50rem;
}
```

#### Use your grid

```html
<div class="r-Grid">
  <div class="r-Grid-cell r-all--1of4">
    <!-- your content-->
  </div>
  <div class="r-Grid-cell r-all--3of4">
    <!-- your content-->
  </div>
</div>
```
---

## Testing

To generate a build:

```console
$ npm run build
```

To generate the testing build.

```console
$ npm run build-test
```

Basic visual tests are in `test/index.html`.

## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

```console
$ git clone https://github.com/cssrecipes/grid.git
$ git checkout -b patch-1
$ npm install
$ npm test
```

## [Changelog](CHANGELOG.md)

## [License](LICENSE)

---

## Acknowledgements

This grid module has been inspired by [SUIT CSS components-grid](https://github.com/suitcss/components-grid) & [SUIT CSS utilities: size](https://github.com/suitcss/utils-size/)

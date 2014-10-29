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
It includes `.cssr-(all|min|max)*` classes used in the examples below to define grid cells width._

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

### Mobile-first

#### Include deps

```css
@import "./node_modules/cssrecipes-custom-media-queries/index.css";
@import "./node_modules/cssrecipes-grid/index.css";
@import "./node_modules/cssrecipes-utils/all.css";
@import "./node_modules/cssrecipes-utils/min.css";
```

#### Define your `Grid` size

```css
.cssr-Grid {
  width: auto;
}

@media (--cssr-minM) {
  .cssr-Grid {
    width: 30em;
  }
}

@media (--cssr-minL) {
  .cssr-Grid {
    width: 50em;
  }
}

/** and the rest of it */
```

#### Use your grid

```html
<div class="cssr-Grid">
  <div class="cssr-Grid-cell cssr-all-1of2 cssr-minM-1of3 cssr-minL-1of4">
    <!-- come content-->
  </div>
  <div class="cssr-Grid-cell cssr-all-1of2 cssr-minM-2of3 cssr-minL-3of4">
    <!-- come content-->
  </div>
</div>
```

### Desktop-first

#### Include deps

```css
@import "./node_modules/cssrecipes-custom-media-queries/index.css";
@import "./node_modules/cssrecipes-grid/index.css";
@import "./node_modules/cssrecipes-utils/all.css";
@import "./node_modules/cssrecipes-utils/max.css";
```

#### Define your `Grid` size

```css
.cssr-Grid {
  width: auto;
}

@media (--cssr-maxL) {
  .cssr-Grid {
    width: 50em;
  }
}

@media (--cssr-minM) {
  .cssr-Grid {
    width: 30em;
  }
}

/** and the rest of it */
```

#### Use your grid

```html
<div class="cssr-Grid">
  <div class="cssr-Grid-cell">
    <!-- come content-->
  </div>
  <div class="cssr-Grid-cell">
    <!-- come content-->
  </div>
</div>
```

### Without responsive

#### Include deps

```css
@import "./node_modules/cssrecipes-grid/index.css";
@import "./node_modules/cssrecipes-utils/all.css";
```

#### Define your `Grid` size

```css
.cssr-Grid {
  width: 50em;
}
```

#### Use your grid

```html
<div class="cssr-Grid">
  <div class="cssr-Grid-cell cssr-all-1of4">
    <!-- come content-->
  </div>
  <div class="cssr-Grid-cell cssr-all-3of4">
    <!-- come content-->
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

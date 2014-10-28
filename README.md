# grid

> BEMish grid component

## Install

```sh
$ npm install cssrecipes-grid
```

## Usage

You can use [`cssrecipes-sizes`](http://github.com/cssrecipes/sizes) for
convenience.

### Mobile-first

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

```sh
$ npm run build
```

To generate the testing build.

```sh
$ npm run build-test
```

Basic visual tests are in `test/index.html`.

## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

```sh
$ git clone https://github.com/cssrecipes/grid.git
$ git checkout -b patch-1
$ npm install
$ npm test
```

## [Changelog](CHANGELOG.md)

## [License](LICENSE)

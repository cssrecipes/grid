# grid

> The ultimate grid utility

## Install

```sh
$ npm install cssrecipes-grid
```

## Usage

### Mobile-first

### Define your `Grid` size

```css
.rcp-Grid {
  width: auto;
}

@media (--viewport-min-m) {
  .rcp-Grid {
    width: 30em;
  }
}

@media (--viewport-min-l) {
  .rcp-Grid {
    width: 50em;
  }
}

/** and the rest of it */
```

### Use your grid

```html
<div class="rcp-Grid">
  <div class="rcp-Grid-cell rcp-all-1of2 rcp-minM-1of3 rcp-minL-1of4">
    <!-- come content-->
  </div>
  <div class="rcp-Grid-cell rcp-all-1of2 rcp-minM-2of3 rcp-minL-3of4">
    <!-- come content-->
  </div>
</div>
```

### Desktop-first

### Define your `Grid` size

```css
.rcp-Grid {
  width: auto;
}

@media (--viewport-max-l) {
  .rcp-Grid {
    width: 50em;
  }
}

@media (--viewport-min-m) {
  .rcp-Grid {
    width: 30em;
  }
}

/** and the rest of it */
```

### Use your grid

```html
<div class="rcp-Grid">
  <div class="rcp-Grid-cell rcp-all-1of4 rcp-maxL-1of3 rcp-maxM-1of2">
    <!-- come content-->
  </div>
  <div class="rcp-Grid-cell rcp-all-3of4 rcp-maxL-2of3 rcp-maxM-1of2">
    <!-- come content-->
  </div>
</div>
```

### Without responsive

### Define your `Grid` size

```css
.rcp-Grid {
  width: 50em;
}
```

### Use your grid

```html
<div class="rcp-Grid">
  <div class="rcp-Grid-cell rcp-all-1of4">
    <!-- come content-->
  </div>
  <div class="rcp-Grid-cell rcp-all-3of4">
    <!-- come content-->
  </div>
</div>
```

## sizing prefixes


### default size

- `rcp-all-XofY`

### mobile-first

- `rcp-minS-XofY`
- `rcp-minM-XofY`
- `rcp-minL-XofY`
- `rcp-minXL-XofY`

### desktop-first

- `rcp-maxS-XofY`
- `rcp-maxM-XofY`
- `rcp-maxL-XofY`
- `rcp-maxXL-XofY`

## available sizing

### 2-columns grid

- `*-1of2`
- `*-2of2`

### 3-columns grid

- `*-1of3`
- `*-2of3`
- `*-3of3`

### 4-columns grid

- `*-1of4`
- `*-2of4`
- `*-3of4`
- `*-4of4`

### 5-columns grid

- `*-1of5`
- `*-2of5`
- `*-3of5`
- `*-4of5`
- `*-5of5`

### 6-columns grid

- `*-1of6`
- `*-2of6`
- `*-3of6`
- `*-4of6`
- `*-5of6`
- `*-6of6`

### 8-columns grid

- `*-1of8`
- `*-2of8`
- `*-3of8`
- `*-4of8`
- `*-5of8`
- `*-6of8`
- `*-7of8`
- `*-8of8`

### 10-columns grid

- `*-1of10`
- `*-2of10`
- `*-3of10`
- `*-4of10`
- `*-5of10`
- `*-6of10`
- `*-7of10`
- `*-8of10`
- `*-9of10`
- `*-10of10`

### 12-columns grid

- `*-1of12`
- `*-2of12`
- `*-3of12`
- `*-4of12`
- `*-5of12`
- `*-6of12`
- `*-7of12`
- `*-8of12`
- `*-9of12`
- `*-10of12`
- `*-11of12`
- `*-12of12`

---

## Testing

_Requires [nodejs](http://nodejs.org)_

To generate a build:

	npm run build

To generate the testing build.

	$ npm run build-test

Basic visual tests are in `test/index.html`.


## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

    $ git clone https://github.com/cssrecipes/grid.git
    $ git checkout -b patch-1
    $ npm install
    $ npm test

## [Changelog](CHANGELOG.md)

## [License](LICENSE)

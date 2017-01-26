# nestable-grid

**nestable-grid** is a nestable, flexible, fully customisable responsive Sass grid

It is developed and maintained internally at [bluegrassdigital](http://www.bluegrassdigital.com), but feel free to contribute!

## Features

#### 1. Nestable columns

What sets this grid apart is that the columns are infinitely nestable - and will retain the same size and gutters that they would be if they weren't nested. This allows for complex responsive layouts that always honour the grid design system.

#### 2. New container not required for every row, columns just wrap

Another feature of the grid is that new rows are not required for every change in row. The columns will just wrap, and since floats are not being used you do not have the problem of hanging floated columns wrapping weirdly.

#### 3. Limit CSS output to only the sizes you need

We can also define exactly what size classes are required at which breakpoints, thereby minimising the final generated CSS output. We don't, for example, generally need classes for `cols-xs-1` etc. Usually a handful of sizes creating halves, quarters and thirds is all we need.

## Installation

`npm install nestable-grid`

## Example usage

See <a href="http://nestable-grid.github.io/#/page/examples.md" target="_blank">Full examples</a>

```scss
@import 'nestable-grid/main.scss';

// the map you pass to the nestable mixin gets merged into the base grid options,
// so only need to redefine values that you would like to be different from the defaults.
$nestable-options: (
  gutter-width: 2%,
  breakpoints: (
    m: 576px,
    l: 768px,
    xl: 1024px
  ),
  output-sizes: (
    m: (6),
    l: (4, 6, 8),
    xl: (3, 4, 6, 8, 9)
  )
);

@include nestable($nestable-options);
```
## Markup rules

1. Each set of columns must have a container with a class of `cs` - eg. `<div class="cs"></div>`
2. Columns should be direct children of the `.cs` container. If not, any elements before the columns would have a font-size of zero.
3. If you have a fixed width for your gutters, you'll need a container around your `.cs` with overflow set to hidden (negative margins are employed for fixed gutters, similarly to bootstrap).

### Example markup

```html
<div class="cs">
  <div class="cols-l-6 cols-xl-3"></div>
  <div class="cols-l-6 cols-xl-9"></div>
  <div class="cols-l-6 cols-xl-9">
    <div class="cs">
      <div class="cols-xl-3"></div>
      <div class="cols-l-6">
        <div class="cs">
          <div class="cols-xl-3"></div>
          <div class="cols-xl-3"></div>
        </div>
      </div>
      <div class="cols-xl-3"></div>
      <div class="cols-xl-3"></div>
      <div class="cols-xl-3"></div>
    </div>
  </div>
  <div class="cols-l-6 cols-xl-3"></div>
</div>
```

## Default config

```scss
$nestable-options-base: (
  columns: 12, //default to a 12 column grid
  gutter-width: 2.5%, //default to 2.5% gutter width. Can be set to static size instead
  container-class: 'cs',
  column-class: 'cols',
  breakpoints: (
    m: 576px,
    l: 768px,
    xl: 1024px
  ),
  output-sizes: (
    m: (6),
    l: (4, 6, 8),
    xl: (3, 4, 6, 8, 9)
  )
) !default;
```

## API

See <a href="http://bluegrassdigital.github.io/nestable-grid/#/iframe/sassdoc/index.html" target="_blank">API docs</a>

## Contributing to nestable-grid

[Github Flow](https://guides.github.com/introduction/flow/) - branch, submit pull requests

# Typographic

Responsive typography for the rest of us. Written in Stylus. SCSS port on the roadmap.

### Installation
`npm install typographic`

### Enable
Place `@import 'typographic'` at the top of your `style.styl` file

### Font Stacks
- Pick from a plethora of sans and serif [font stacks](typographic/_font-stacks.styl)
- Set your selector's `font-family` to one of the stacks variables, for instance `helvetica`

### Headers
It's common for header and body font stacks to differ. With the `t-headers()` mixin, you can change all headers to have the same [font stack](typographic/_font-stacks.styl).

### Presets
The [presets](typographic/_presets.styl) file is a typography reset that applies some `font-size`, `line-height`, and `margin-bottom` to common selectors. There is a `preset()` mixin with some reasonable defaults that accepts named parameters:

- `ratio` can be any floated number and in the [ratios](typographic/_ratios.styl) file you will see a variable list of common [modular scale](http://modularscale.com) ratios (default: golden)
- `steps` is used to divide the given ratio into smaller increments, e.g. if using the golden ratio (1:1.618) with 2 steps the output would be 1rem -> 1.272rem -> 1.618rem -> ... (2 steps to the ratio) instead of 1rem -> 1.618rem -> 2.628rem -> ... (1 step to the ratio) (default: 2)
- `header-line-height` is used to set the line height for headers (default: 1.1)
- `body-line-height` is used to set the line height for the base text elements (default: 1.4)
- `margin-bottom-ratio` is used to set the bottom margin of elements based on their relative size (default: inverse of the ratio in use)

The order of the parameters does not matter if you pass them with names. Example:

`presets(body-line-height: 1.5, header-line-height: 1, ratio: perfect-fourth, steps: 1)`

**To enable typographic, use the `presets()` mixin after `@import`ing Typographic.** Pass the `presets()` different parameters to see how it works.

### Easy Responsive Typography
Just set your `html` selector's base `font-size`, then adjust the `font-size` with media queries.

### Watch
`stylus -u typographic -w css/style.styl`

### Putting it all together
- `npm install -g typographic`
```stylus
@import 'typographic'

presets(ratio: major-sixth)

html
  font-family: garamond
  font-size: 12px
  @media (min-width: 600px)
    font-size: 14px
  @media (min-width: 800px)
    font-size: 16px
  @media (min-width: 1000px)
    font-size: 18px

t-headers(helvetica)
```
- `stylus -u typographic -w css/style.styl`

Expand/contract the **[demo](http://corysimmons.github.io/typographic/)** to see this in action.

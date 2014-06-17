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

### Presets and Ratios
The [presets](typographic/_presets.styl) file is a typography reset that applies some `font-size`, `line-height`, and `margin-bottom` to common selectors. There is a `preset()` mixin that accepts a ratio. A ratio can be any floated number and in the [ratios](typographic/_ratios.styl) file you will see a variable list of common [modular scale](http://modularscale.com) ratios.

**To enable typographic, use the `presets()` mixin after `@import`ing Typographic.** Pass the `presets()` mixin random numbers to see how it works.

### Easy Responsive Typography
Just set your `html` selector's base `font-size`, then adjust the `font-size` with media queries.

### Watch
`stylus -u typographic -w css/style.styl`

### Putting it all together
- `npm install -g typographic`
```stylus
@import 'typographic'

presets(major-sixth)

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

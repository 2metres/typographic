typographic
===========

Responsive typography with modular scale, font stacks, and more. Built on Stylus. Depends on [Rupture](https://github.com/jenius/rupture).

#### Installation
```
npm install -g rupture typographic
cd ~/Project
echo "@import 'typographic'" > css/foo.styl
```

#### Usage
```
stylus -u rupture -u typographic -w css/foo.styl
```

#### Settings
- **`typo_breakpoint ?= 800px`** - Set your mobile-to-desktop breakpoint.
- **`typo_headers ?= helvetica`** - The font stack for all `<h1>`-`<h6>` elements. You can find a list of these [here](_settings.styl).
- **`typo_header_color ?= #111`** - Colors for all `<h1>`-`<h6>` elements.
- **`typo_header_weight ?= 200`** - Font weight for `<h1>`-`<h6>` elements.
- **`typo_tagline_color ?= #aaa`** - The color of `<p>` elements within a `<header>` element.
- **`typo_body ?= helvetica`** - `<body>` font stack. You can find a list of these [here](_settings.styl).
- **`typo_body_color ?= #444`** - `<body>` color.
- **`typo_mobile ?= major_third`** - The named ratio size for mobile devices. You can use a custom float number as well. You can find a list of these [here](_settings.styl).
- **`typo_desktop ?= octave`** - The named ratio size for desktop devices. You can use a custom float number as well. You can find a list of these [here](_settings.styl).

### Override Settings
- Create a `settings.styl` file as a sibling to `foo.styl`
- At the top of `settings.styl` put:

```
@import 'settings'
@import 'typographic'
```

- Modify `settings.styl` to override any of the above settings

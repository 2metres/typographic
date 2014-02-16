typographic
===========

Responsive typography with modular scale, font stacks, and more. Built on Stylus. Depends on [Rupture](https://github.com/jenius/rupture).

#### Installation
```
npm install -g rupture
cd ~/Project
npm install typographic
echo "@import 'node_modules/typographic/typographic'" > css/foo.styl
```

#### Usage
```
cd ~/Project/css
stylus -u rupture -w foo.styl
```

#### Settings
- **`breakpoint = 800px`** - Set your mobile-to-desktop breakpoint.
- **`headers = helvetica`** - The font stack for all `<h1>`-`<h6>` elements.
- **`header_color = #111`** - Colors for all `<h1>`-`<h6>` elements.
- **`header_weight = 200`** - Font weight for `<h1>`-`<h6>` elements.
- **`tagline_color = #aaa`** - The color of `<p>` elements within a `<header>` element.
- **`body = helvetica`** - `<body>` font stack.
- **`body_color = #444`** - `<body>` color.
- **`mobile = major_third`** - The named ratio size for mobile devices. You can use a custom float number as well.
- **`desktop = octave`** - The named ratio size for desktop devices. You can use a custom float number as well.

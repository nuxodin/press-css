# Press.css
Press.css is a flat, lightweight, scalable, no bullshit button library for your projects that is heavily influenced by [Google's Material Design](https://www.google.com/design/) guidelines. It's markup is simple, easy to use and predictable and helps ensure a uniform button experience across all pages of your site or app.

## Ways to Use

Download Press.css and add a link to the stylesheet in the `head` of your document.

```html
<link rel="stylesheet" href="press.css" />
```

## The Markup

At the very minimum, press requires two classes, `press` and `press-[color]`, to create a working button.


```html
<button class="press press-red">Square Button</button>
```

Want more features? You can have more fun with it as well:

```html
<button class="press press-bluegrey press-round press-ghost press-xl">Round Button</button>
```

You can even use anchor elements to make a link look like a Press.css button:

```html
<a href="#" class="press press-green press-circle">21</a>
```

## Features

**Check out the [Press.css](http://codyo.me/press) to see these features in action.**

### [Button Shapes](http://codyo.me/press/#shapes)

*(default)* - If you do not specify a shape, Press.css will create a squared button.

*.press-round* - A button with rounded corners.

*.press-pill* - A button that looks like a pill.

*.press-circle* - Perfect for glyphicons or numbers. Too much content will be hidden.

### [Button Sizes](http://codyo.me/press/#sizes)

*.press-sm* - Equivalent of `font-size:.8em;`

*(default)* - Equivalent of `font-size:1em;`

*.press-lg* - Equivalent of `font-size:1.25em;`

*.press-xl* - Equivalent of `font-size:1.5em;`

### [Button Effects](http://codyo.me/press/#effects)

*.press-raised* - Adds a slight border-shadow to the button

*.press-ghost* - Inverts the button so background is transparent, and button border/text are the specified color.

*:disabled* - Press.css uses the disabled attribute on `button` elements.

### [Button Colors](http://codyo.me/press/#colors)

Press.css borrows heavily from the design specs of Google's Material Design. All the [color names](http://codyo.me/press/#colors) in their style guide are used by default in Press.css.

**Note:** There is a `.press-yellow` and a `.press-white` class that defaults to `color: #FFF`. Overwrite this class anywhere below where you add Press.css to give the text a contrasting color.

## Customizing Press.css

The SCSS file is pretty straightforward, but I thought I would leaves some quick notes:

### Adding/Removing Colors:

The colors are created via a SCSS key/value map, `$colors`. SASS will throw interpolation warnings and errors. To prevent this, always place the key as a string (wrap it in quotes `"`) *especially* if you are using color names used in HTML (e.g. blue, green, red, orange).

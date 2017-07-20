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

Press.css is now extendable without the need for using or compiling with Sass! In addition to the default colors, you can create your own custom classes with the `press-[class]` format and a special CSS custom property. ([Codepen](https://codepen.io/codyogden/pen/pwXXQG))
```css
.press-love {
	--p: pink;
        color: red;
}
```

## Accessibility First
Now that you can easily add new and custom colors to Press.css, I wanted to ensure that Press.css adheres as close as possible to web accessibility standards. While I was able to keep all the original button colors from the original release, this meant I needed to change the default text color on many of the buttons to ensure a minimum of AA compliance with [(WCAG 2.0)](https://usecontrast.com/guide).

If `color: #FFF` would cause a color ratio to fall below a 5.0 (AA is 4.5), it will default to a black color instead. Colors can easily be overridden with normal CSS with the following:
```css
.press:not(.press-ghost) {
    color: #FFF;
}
```

## Browser Support
I have tested the library as is in modern Chrome, Safari, and Firefox.

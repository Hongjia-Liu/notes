# CSS Box Model

Everything displayed by CSS is a box. Understanding how the CSS Box Model works is therefore a core foundation of CSS.

The CSS box model behaves like an **onion**. From inside to out, it consists of **4 Layers**:

- **1st** layer: Content
- **2nd** layer: Padding
- **3rd** layer: Border
- **4th** layer: Margin

Most elements are block level by default.

- They stack one on top of the other
- Block level elements have a default `width` of `100%` and a `height` of `0`. Their width by default is the width of their parent.
- Their height will grow as you add more content to them (generally we don't set height. It's not a good practice)

## Content

Percentage-based widths and heights are relative to the amount of space being made available by the parent.

## Padding

Padding is the empty space between content and border.

`padding: top right bottom left`

## Border

- `border-width`
- `border-style`
- `border-color`

We can also control each side independently using a shorthand.

- `border-top`
- `border-right`
- `border-bottom`
- `border-left`

A `border-radius` can also be used to create rounded corners on an element, regardless of if it has a border. This defines the radius of the corners, and a value of `50%` is often used on square elements to create a circle.

## Margin

Margin is the empty space around an element. We can control the 4 sides independently.

`margin: top right bottom left`

A value of `auto` can also be used to allow the browser to choose margins, which will usually center block elements horizontally.

### Margin vs Padding

As a general rule of thumb:

- If you need empty space, use margin.
- If you more background, use padding.

## Margin Collapse

Adjacent horizontal margins will be added together to determine the space between elements. Vertical margins on the other hand will usually be collapsed, meaning only the larger margin value will be used.

## Box-sizing

The `box-sizing` CSS property sets how the total width and height of an element is calculated.
There are three types of calculations:

- `border-box`
- `padding-box`
- `content box`

We're not gonna discuss `box-sizing: padding-box`, as only Firefox supports it and it isn't used very often.

The default value is `content-box` for most elements, which sets the width and height to only control the size of the content. However, a value of `border-box` would include the size of the padding and border.

### What is the difference between content-box and border-box in CSS?

- By default, elements have `box-sizing: content-box` applied, and only the content size is being accounted for.
- `box-sizing: border-box` changes how the `width` and `height` of elements are being calculated, `border` and `padding` are also being included in the calculation.
- The `height` of an element is now calculated by the content's `height` + vertical `padding` + vertical `border` width.
- The `width` of an element is now calculated by the content's `width` + horizontal `padding` + horizontal `border` width.
- Taking into account `padding`s and `border`s as part of our box model resonates better with how designers actually imagine content in grids.

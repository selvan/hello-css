# CSS Intro

CSS influences how HTML elements are

 * Positioned
 * Displayed

## Managing element display

 * "display" property
 * element/context speific properties such as "font", "color", "border" etc

### "display" property
There are two categories of elements in HTML,

 1.Block level elements

    Block level elements are normally displayed as blocks with line breaks before and afterwards

 2.Inline elements

    Inline content is displayed with no line breaks before or afterwards.
    For inline elements, "width, height, margin and padding" properties are n't applicabale fully or partially.

We can change block-to-inline and vice-versa, using "display" css property.

## Managing element position

 * In X(length) - Y(breadth) space
 * In Z(depth) space

### Positioning in X(length) - Y(breadth) space

 1."position" property

    See position/position.md

 2."float" property

### Positioning in Z(depth) space

    "z-index" property controls how elements are stacked depthwise. "z-index" will only work on an element whose position
    property has been explicitly set to absolute, fixed, or relative.

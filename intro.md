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

#### Stacking context

Note: Content copied from https://developer.mozilla.org/en-US/docs/CSS/Understanding\_z-index/The\_stacking\_context


    The rendering order of DIVs is influenced by their z-index value. This occurs because these DIVs have special properties which cause them to form a stacking context.
    A stacking context is formed, anywhere in the document, by any element which is either


* the root element (HTML),
* positioned (absolutely or relatively) with a z-index value other than 'auto'
* elements with an opacity value less than 1


    Within a stacking context, child elements are stacked according to the same rules previously explained.
    Importantly, the z-index values of its child stacking contexts only have meaning in this parent.
    Stacking contexts are treated atomically as a single unit in the parent stacking context.

In summary

* Positioning and assigning a z-index value to an HTML element creates a stacking context, (as does assigning non-full opacity).
* Stacking contexts can be contained in other stacking contexts, and together create a hierarchy of stacking contexts.
* Each stacking context is completly independent from its siblings: only descendant elements are considered when stacking is processed.
* Each stacking context is self-contained: after the element's contents are stacked, the whole element is considered in the stacking order of the parent stacking context.


    See stacking-context/stacking-context.md




## Position:static

Default positioning for all elements.
Normal behavior.  The top, right, bottom, and left properties do not apply.

<iframe src="pages/1.html" width="400px" height="400px"></iframe>

## Position:relative

Lay out all elements as though the element were not positioned, and then adjust the element's position, without changing
layout (and thus leaving a gap for the element where it would have been had it not been positioned).
The effect of position:relative on table-*-group, table-row, table-column, table-cell, and table-caption elements is undefined.

Use top, right, bottom, and left properties to position your element.

    #div-1 {
         position:relative;
         top:20px;
         left:50px;
    }

<iframe src="pages/2.html" width="400px" height="400px"></iframe>


## position:absolute

Do not leave space for the element.  Instead, position it at a specified position relative to its closest positioned ancestor or to the containing block.
Absolutely positioned boxes can have margins, they do not collapse with any other margins.

    #div-1a {
        position: absolute;
        top:0;
        right:0;
    }

<iframe src="pages/3.html" width="400px" height="400px"></iframe>

## More Examples

### position:relative + position:absolute

div-1 - is relatively positioned.
div-1a - with in "div-1", "div-1a" is absolutly positioned.

    #div-1 {
         position:relative;
         top:20px;
         left:50px;
    }
    #div-1a {
         position:absolute;
         top:0;
         left:0;
    }


<iframe src="pages/4.html" width="400px" height="400px"></iframe>


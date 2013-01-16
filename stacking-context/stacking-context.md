In this example every positioned element creates its own stacking context, because of their positioning and z-index values.
The hierarchy of stacking contexts is organized as follows:

    Root
        DIV #1
        DIV #2
        DIV #3
            DIV #4
            DIV #5
            DIV #6

It is important to note that DIV #4, DIV #5 and DIV #6 are children of DIV #3, so stacking of those elements is
completely resolved within DIV#3. Once stacking and rendering within DIV #3 is completed, the whole DIV #3 element
is passed for stacking in the root element with respect to its sibling's DIV.

<iframe src="pages/index.html" width="700px" height="400px"></iframe>

    Notes:

    DIV #4 is rendered under DIV #1 because DIV #1's z-index (5) is valid within the stacking context of the root element,
    while DIV #4's z-index (6) is valid within the stacking context of DIV #3. So, DIV #4 is under DIV #1, because DIV #4
    belongs to DIV #3, which has a lower z-index value.

    For the same reason DIV #2 (z-index 2) is rendered under DIV#5 (z-index 1) because DIV #5 belongs to DIV #3,
    which has an higher z-index value. DIV #3's z-index is 4, but this value is independent from z-index of DIV #4,
    DIV #5 and DIV #6, because it belongs to a different stacking context. An easy way to figure out the rendering
    order of stacked elements along the Z axis is to think of it as a "version number" of sorts,
    where child elements are minor version numbers underneath their parent's major version numbers.
    This way we can easily see how an element with a z-index of 1 (DIV #5) is stacked above an element
    with a z-index of 2 (DIV #2), and how an element with a z-index of 6 (DIV #4) is stacked below an element
    with a z-index of 5 (DIV #1). In our example (sorted according to the final rendering order):

    Root
        DIV #2 - z-index is 2
        DIV #3 - z-index is 4
            DIV #5 - z-index is 1, stacked under an element with a z-index of 4, which results in a rendering order of 4.1
            DIV #6 - z-index is 3, stacked under an element with a z-index of 4, which results in a rendering order of 4.3
            DIV #4 - z-index is 6, stacked under an element with a z-index of 4, which results in a rendering order of 4.6
        DIV #1 - z-index is 5



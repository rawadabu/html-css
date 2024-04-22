# CSS

- Cascading Style Sheets.
- Describe the visual style and presentation of the content written in HTML.
- A CSS Rule:

```
Selector
h1 {
    color: blue;
    text-align: center;
    font-size: 20px; <-- Declaration / Style
}
```

Difference between ID and Class selector, is that ID we can only use once!

- Pseudo Classes

```
li:nth-child(even){
    color: red;
}
```

## CSS Theory #1: Conflicts Between Selectors

First is declarations marked with !important
Second is inline style.(style attribute in HTML).
Third rule gonna be applied is ID -> More than one ID? -> Last code selector will applied.
Forth is class (.) or pseudo class (:) selector.
Fifth is the element selector.
Last is the universal selector (\*).

## CSS Theory #2: Inheritance and the Universal Selector.

Body element is the Parent element, will be applied to all elements.

```
body{
    color: red;
}
```

## CSS Theory #3: The CSS Box Model

One of the most fundemental parts of CSS.

- Content: Text, images, etc.
- Border: A line around the element still _INSIDE_ of the element.
- Padding: Invisible space around the content, _INSIDE_ the element.
- Margin: Space _OUTSIDE_ of the element, between elements. **NOT PART OF THE WIDTH OR HEIGHT OF THE FINAL ELEMENT**
- Fill area: Area that gets filled with background color **or** background image.

- Centering our Page:

```
.container{
    width: 700px;
    margin-left: auto;
    margin-right: auto;
}
```

It will give the margins the same amount.
or

```
.container{
    width: 700px;
    margin: 0 auto;
}
```

## CSS Theory #4: Types of Boxes

- Inline elements:
  - Occupies only the space necessary for its content.
  - Causes no line-breaks before or after the element.
  - Box model applies in a different way: heights and widths do not apply.
  - Paddings and margins are applied only horizontally(left and right).

```
nav a:link{
    display: block;
}
All of these elements occupy all the width that they can.
```

| Block-Level Boxes                     | Inline-Block Boxes                                                         | Inline Boxes                                            |
| ------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------- |
| Elements formatted visually as blocks | Looks like inline from the outside, behaves like block-level on the inside | Occupies only content's space                           |
| 100% of parent's width                | Occupies only content's space                                              | Causes no line-breaks                                   |
| Vertically, one after another         | Causes no line-breaks                                                      | Box model is different: heights and widths do not apply |
| 1Box-model applies as showed          | Box model applies as showed                                                | Paddings and margins only horizontal                    |

## CSS Theory #5: Absolute Positioning

| Normal Flow                                                            | Absolute Positioning                                                                              |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Default positioning                                                    | Element is remoced from the normal flow: "out of flow"                                            |
| Element is "in flow"                                                   | No impact on surrounding elements, might overlap them                                             |
| Elements are simply laid out according to their order in the HTML code | We use top, bottom, left, or right to offset the element from its relatively positioned container |

## Pseudo Elements

```
h1::first-letter{
    font-style: normal;
    margin-right: 5px;
}

h1::after{
    content: "TOP";
    background-color: #ffe70e;
    font-size: 16px;
    font-weight: bold;
    display: inline-block;
    padding: 5px 10px;
    position: absolute;
    top: -15px;
    right: -25px;
}
```

# Layouts: Floats, Flexbox, and CSS Grid Fundamentals

## Layout = THE DESIGN

- Layout is the way text, images and other content placed and arranged on a webpage.
- Layout gives the page visual structure, into which we place our content.
- Building a layout: arranging page elements into a visual structure, instead of simply having them placed one after another(normal flow).

The 3 ways of building layouts with CSS

1. Float Layouts: The old way of building layouts of all sizes, using the float CSS property.
2. Flexbox: Modern way of laying out elements in a 1-dimensional row without using floats. Perfect for component layouts.
3. CSS Grid: For laying out element in a fully-fledged 2-dimensional grid. Perfect for page layouts and complex components.

### Flexbox

- A set of related CSS properties for building 1-dimensional layouts.
- The main idea behind flexbox is that empty spaces inside a container element can be automatically divided by its child elements.
- Makes it easy to automatically align items to one another inside a parent container, both horizontally and vertically.
- Flexbox solves common problems such as vertical centering and creating equal-height columns.
- Flexbox is perfect for replacing floats, allowing us to write fewer and cleaner HTML and CSS code.

| Flex Container                                                                  | Flex Items                                                              |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| gap: 0, to create space between items                                           | align-self: auto, to overwrite align-items individual flex items        |
| justify-between: flex-start, to algin items along main axis                     | flex-grow: 0, to allow an element to grow                               |
| align-items: stretch, to align items along cross axis, vertically               | flex-shrink: 1, to allow an element to shrink                           |
| flex-directions: row, to define which is the main axis                          | flex-basis: auto, to define item's width, instead of the width prop     |
| flex-wrap: nowrap, to allow items to wrap into a new line if they are too large | flex: 0 1 auto, recommended shorthand for flex-grow,-shrink-basis       |
| align-content: stretch, only applies when there are multiple lines              | order: 0, controls order of items, -1 makes item first, 1 makes it last |

### Grid

- CSS Grid is a set of CSS properties for building 2-dimensional layouts.
- The main idea behind CSS Grid is that we divide a container element into rows and columns that can be filled with its child elements.
- In two-dimensional contexts, CSS Grid allows us to write less nested HTML and easier-to-read CSS.
- CSS Grid is not meant to replace flexbox! Instead, they work perfectly togerther. Need a 1D layout? Use flexbox. Need a 2D layout? use CSS Grid.

| Grid Container                                                                   | Grid Items                                                            |
| -------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| grid-template-rows/columns, to establish the grid row and column tracks          | grid-column/row, to place a grid item into a specific cell            |
| row/column-gap: 0                                                                | justify/align-self, to overwrite justify-items/align for single items |
| justify/align-items: stretch, to align items inside rows/columns                 |                                                                       |
| justify-content/align-content: start, to align entire grid inside grid container |                                                                       |

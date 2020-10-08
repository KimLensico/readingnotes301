# CDD Grid

`grid-column-start` - telling  where the element starts
  - e.g. `grid-column-start: 2`
  - grid starts at the second column

`grid-column-end` - states the ending place of the grid
  - e.g. `grid-column-end: 5`
  - grid ends at fifth column

`span` - define the element's positioning based on the desired column width using the `span` keyword.
  - `span` only works on positive numbers
  - e.g. `grid-column-end: span 4`
  - sets relative width to 4th grid

`grid-column` - shorthand property.
  - accepts both values at once
    - values are separated by a slash 
    - e.g. `grid-column: 2/4`
  - span keyword also works

*the start and end of the grid go by the border line that it ends on*

  - **positive numbers**: go from left to right of the grid
  - **negative numbers**: start from right to left of the grid



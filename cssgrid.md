# CSS Grid

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

`grid-row-start` - positions the end grid items through the y-axis

`grid-row-end` - position the end grid through the y-axis

`grid-row` - shorthand version.

`grid-area` - accepts four values separated by slashes
  - e.g: `grid-area: 1/1/3/6`
  - format: `grid-area: grid-row-start/ grid-column-start/ grid-row-end/ grid-column-end`

  *you can overlap multiple `grid-area`'s to cover multiple things*

`order` - can override the automatic order that items are placed
  - By default, all grid items have an order of 0, 
    - this can be set to any positive or negative value 
      - similar to z-index.

`grid-template-columns` - sets up the number of grid columns
  - e.g. `grid-template-columns: 50%`
  - sets the width of the first column
  - e.g. `grid-template-row: 30% 30%`
  - sets the width of each row to 30%

`grid-template-columns` - sets up the number of grid rows 
  - `repeat` - a function that specifies columns with identical widths easier
    - e.g. `repeat(8 [columns], 30% [width])`
  - also accepts length units like pixels and ems
    - different units can be mixed together

example: 

 - `grid-template-columns: 20% 20% 20% 20% 20%`
 - `grid-template-rows: 20% 20% 20% 20% 20%`; 
    - each rule has five values that create five columns
    - each set to 20% of the overall width [of the grid]

  - ```grid-template``` - shorthand property that combines `grid-template-rows` and `grid-template-columns`
    - format: `[rows and width for every row] / [columns and column width for every row`
    - e.g ` grid-template: 50% 50% / 200px;`
      - creates a grid with two rows that are 50% each
      - one column that is 200 pixels wide.

### Units
  - `fr` - fractional unit.
    - each `fr` allocates one share of the available space
    - e.g. `grid-template-columns: 1fr 5fr`
      - one column takes up 1/5 and the other takes up 4/5 of the grid 


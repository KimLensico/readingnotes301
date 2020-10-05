# SMACSS & Responsive Web Design

## Responsive Web Design
> definition: the practice of building a website suitable to work on every device

### Responsive vs Adaptive
**Responsive** - react quickly to change 
**Adaptive** - easily modified
- the combination of the twi is an idea formula for function websites
- *mobile* commonly sets the domain for mobile users

### Flexible Layouts
> the practice of building a website with a flexible grid. relative to margin, padding, and width.
- does not advocate the use of fixed measurements [pixels and inches]
- **formula** ```target / context = result```
  - the formula takes the target of the width and divides it by its parent element. 
  - the result is the relative width of the target element

### Flexible Grid
> we can take all the fixed unites of length and turn them into relative units 
- still not enough. when the layout gets too small or too large, the text becomes illegable
  - the layout may begin to break

## Media Queries
> an extension built for media types commonly found when targeting and including styles. provides the ability to specify different styles for individual browsers and devices.

### Logical Operators in Media Queries
> builds powerful expressions
#### 3 LOGICAL OPERATORS
1. ```and``` - allows and extra condition
2. ```not``` - negates the query
3. ```only``` - **new**. not recognized by html. hides styles.  

### Indentifying Breakpoints
> responsive websites should adjust. breakpoints should only be introduces if a website is breaking, looking weird, or the experience of it is being hampered

## Mobile First
> approavh that includes using styles targeting at smaller viewports such as the default stylesfor a wehsite. Then use media queries to add styles as the viewport grows
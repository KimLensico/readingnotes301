# FUNCTIONAL PROGRAMMING

### ***What is functional programming?***
> Functional programming is a **programming paradigm**
  - a style of building the structure and elements of computer programs
  - treats computation as the evaluation of mathematical functions 
  - avoids changing-state and mutable data (***[Wikipedia](https://en.wikipedia.org/wiki/Functional_programming)***)
  
## **Pure functions**
> pure functions return the same result if given the same arguments (referred as *deterministic*)
- does not cause any observable side effects
- returns the same result if given the same arguments
- stable, consistent, and predictable 
- given the same parameters, pure functions will always return the same result
- the parameter will *never* have different results
  ### **Pure functions benefits**
  - code is easier to test. 
    - don’t need to mock anything
    - we can unit test pure functions with different contexts

## **Impure functions** 
> if our function reads external files, it’s not a pure function — the file’s contents can change.

- ### **Random number generation**
  - Any function that relies on a random number generator cannot be pure.

- observable side effects include modifying a global object or a parameter passed by reference.

#### *mutability is discouraged in functional programming.*

## Immutability
> Unchanging over time or unable to be changed.

- when data is immutable, its state cannot change after it’s created 
  - instead, you create a new object with the new value.
- we handle mutability in iteration through recursion

***the result of a function will be used as an input for the next function, without modifying the original input string.***

## Functions as first-class entities
> functions are also treated as values and used as data.
### Functions as first-class entities can:
  - refer to it from constants and variables
  - pass it as a parameter to other functions
  - return it as result from other functions
  - treat functions as values and pass functions like data  
    - we can combine different functions to create new functions with new behavior.

#### Filter
- filter function expects a true or false value to determine if the element should or should not be included in the result collection
  - if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.

#### Map / Declarative Javascript
- transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
 - the whole idea is to transform a given array into a new array.

#### Reduce
> to receive a function and a collection, and return a value created by combining the items.
- we can build a function to handle the amount sum and pass it as an argument to the reduce function.



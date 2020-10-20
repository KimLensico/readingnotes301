# EJS Partials

> Partials come in handy when you want to reuse the same HTML across multiple views

- think of partials as functions 
- you define that reusable bundle of code in a file and include it wherever you need it.

  **In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by `<% %>` delimiters**
  - use `<%`- include( PARTIAL_FILE ) `%>` where the partial file is relative to the template you use it in.
  - `<% - %>` tags allow us to output the unescaped content onto the page 
    - *notice the "-"*. This is important when using the include() statement since you don’t want EJS to escape your HTML characters like ‘<’, ‘>’, etc
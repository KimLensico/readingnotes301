# EJS
> Embedded JavaScript templating

EJS is a simple templating language that lets you generate HTML markup with plain JavaScript

### Benefits of EJS:
- Can use plain Javascript
- Fast Development
- Easy debugging
- Simple syntax
- Active development
  - it's server is under active development with a large community of active users

`.path` is a core module for node. it takes two paths and joins them. 

### Response.render takes 3 parameters:
1. view (string of the file name)
2. object of local variables
3. callback

### With .ejs files we can:
  - use a mix of html (in the .ejs file and javascript)
  - type up loops with the html in the .ejs file.
  - inject values into the ejs file
    - in order to do so, we have to reference the file ejs is in since the response only takes the file
- partials and layouts are native to ejs. example: navbar
  - this means we can use the .ejs file to wrap a layout on multiple webpages

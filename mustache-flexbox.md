# Mustache + Flexbox

## Javascript Templating
> a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. 
- template is a HTML markup
  - with added templating tags that will either insert variables or run programming logic.
- the template engine then replaces variables and instances declared in a template file with actual values at runtime
- converts the template into an HTML file sent to the client.

## Mustache
> logic-less template syntax 
- can be used for HTML, config files, source code — anything. 
- works by expanding tags in a template using values provided in a hash or object.
- **often referred to as “logic-less” because there are no if statements, else clauses, or for loops.** - there are only tags. 
  - some tags are replaced with a value, some nothing, and others a series of values.
- mustache.js is an implementation of the mustache template system in JavaScript. 
  - often considered the base for JavaScript templating. 
  - since mustache supports various languages, we don’t need a separate templating system on the server side.

---

  ```Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });```
>// returns: Hello, Sherlynn

```({name})``` - placeholder
  - mustache compiles this, it will look for the ```name``` property in the object we pass in, and replace {{ name }} with the actual value [“Sherlynn”]

---

- ***Mustache is NOT a templating engine***
- Mustache is a specification for a templating language. 
  - [generally] we would write templates according to the Mustache specification
    - it can then be compiled by a templating engine to be rendered to create an output.

### Mustache-Express
> if you intend you use mustache with Node and Express, you can use mustache-express. Mustache Express lets you use Mustache and Express together easily.

To install:

Yarn:
```$ yarn add mustache-express```

NPM:
```$ npm install mustache --save```

***[for more information on installation click here](https://medium.com/@1sherlynn/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)***
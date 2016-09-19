#e.md

I am md --e
Type: function

A function to highlight code blocks. The first example below uses async highlighting with node-pygmentize-bundled, and the second is a synchronous example using highlight.js:

var marked = require('marked');

var markdownString = '```js\n console.log("hello"); \n```';

// Async highlighting with pygmentize-bundled
marked.setOptions({
  highlight: function (code, lang, callback) {
    require('pygmentize-bundled')({ lang: lang, format: 'html' }, code, function (err, result) {
      callback(err, result.toString());
    });
  }
});

// Using async version of marked
marked(markdownString, function (err, content) {
  if (err) throw err;
  console.log(content);
});

// Synchronous highlighting with highlight.js
marked.setOptions({
  highlight: function (code) {
    return require('highlight.js').highlightAuto(code).value;
  }
});

console.log(marked(markdownString));
highlight arguments
code

Type: string

The section of code to pass to the highlighter.

lang

Type: string

The programming language specified in the code block.

callback

Type: function

The callback function to call when using an async highlighter.

renderer
Type: object Default: new Renderer()

An object containing functions to render tokens to HTML.

Overriding renderer methods
The renderer option allows you to render tokens in a custom manner. Here is an example of overriding the default heading token rendering by adding an embedded anchor tag like on GitHub:

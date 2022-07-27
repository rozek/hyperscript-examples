# hyperscript-examples #

a (growing) list of \_hyperscript examples

[\_hyperscript](https://github.com/bigskysoftware/_hyperscript) is a relatively new programming language and, thus, lacks comprehensive documentation, tutorials and examples.

This repository shall narrow this gap a bit by providing a (growing) number of hopefully useful examples. Most of the examples are served by the [Svelte REPL](https://svelte.dev/repl/4a9706898b88431aaf4887b6f5d3cabe) (see below for an explanation), may be edited from within a browser and will compile on-the-fly.

> Just a small note: if you like this repository and seem to benefit from its contents, consider "starring" it (you will find the "Star" button on the top right of this page), so that I know which of my repositories to take most care of.

## The Svelte REPL ##

[Svelte](https://svelte.dev/) is a really interesting technology for building compact and performant Web Applications based on HTML, CSS and JavaScript - if you are not just interested in \_hyperscript, it may well be worth having a look at it.

In the context of these \_hyperscript examples, however, we are only interested in the Svelte REPL (Read-Eval-Print-Loop) as it offers a few interesting features:

* an editor window with HTML syntax highlighting allows you to edit any example from within your browser
* any changes you make will be compiled on-the-fly, showing any results in an output area within a few seconds
* once you have created an account (for free) and logged-in, you may save any edited example in your own space
* because of the way Svelte works, the editor window contains both the contents of a document `<head>` and `<body>`

### What you should take care of when editing ###

While the contents of your document `<body>` may be directly written into the Svelte editor, any content that should go into the document `<head>` have to be enclosed within a `<svelte:head>...<\svelte:head>` pseudo element (like in the ["Hello, World" example](https://svelte.dev/repl/4a9706898b88431aaf4887b6f5d3cabe))

Anything else but your HTML body elements should be placed in the document `<head>`. This includes

* a reference to \_hyperscript
* any `<script>` element (including those of `type="text/hyperscript"`)
* any `<style>` and `<link rel="stylesheet">` elements

The Svelte REPL does not allow to use these elements outside of `<svelte:head>...<\svelte:head>` (as they are relevant for Svelte itself)

### MD5 Hash Computation ###

MD5 hashes are often used to validate the integrity of file uploads and downloads. The [JavaScript MD5 implementation written by blueimp](https://github.com/blueimp/JavaScript-MD5) may easily be used from within \_hyperscript:

```
 <script src="https://unpkg.com/browse/blueimp-md5@2.19.0/js/md5.min.js"></script>
 
 <script type="text/hyperscript">
  init
    log md5('Hello, World!') // 65a8e27d8879283831b664bd8b7f0ad4
  end
 </script>
```

Just pass a string into `md5(...)` and you will get a string back which contains the hexadecimally encoded MD5 hash of the given argument.

## License ##

While \_hyperscript itself is under a [BSD 2-clause license](https://github.com/bigskysoftware/_hyperscript/blob/master/LICENSE), these examples are just MIT-licensed

[MIT License](LICENSE.md)

# hyperscript-examples #

a (growing) list of \_hyperscript examples

[\_hyperscript](https://github.com/bigskysoftware/_hyperscript) is a relatively new programming language and, thus, lacks comprehensive documentation, tutorials and examples.

This repository shall narrow this gap a bit by providing a (growing) number of hopefully useful examples. Most of the examples are served by the [Svelte REPL](https://svelte.dev/repl/4a9706898b88431aaf4887b6f5d3cabe) (see below for an explanation), may be edited from within a browser and will compile on-the-fly.

> Just a small note: if you like this repository and seem to benefit from its contents, consider "starring" it (you will find the "Star" button on the top right of this page), so that I know which of my repositories to take most care of.

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

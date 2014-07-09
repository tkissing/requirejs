# ReqwireJS

ReqwireJS is a patched version of [RequireJS](https://github.com/jrburke/requirejs) with additions taken from [rewire](https://github.com/jhnns/rewire).
It implements a (mostly) RequireJS-compatible API and is designed to to help test AMD modules.

By using ReqwireJS you can `__get()__` and `__set()__` variables declared at the top level of your module that are not being exported.

## Limitations
Your modules need to be written in CommonJS syntax, using module.exports so ReqwireJS can find the right place in the code to inject it's /magic/. 
I hope to remove this restriction at some point, but don't hold your breath.

## Why is the filename still require.js?
So I can run the unit tests for RequireJS against the ReqwireJS without having to patch them.

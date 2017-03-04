# Recursive Iterator

## About
Iterates through graph or tree recursively.

## Versions
+ for support ES5 see `2.x.x` versions

## Getting started

### Quick overview (es6)
```js
let iterator = new RecursiveIterator(
    root /*{Object|Array}*/,
    [bypassMode=0] /*{Number}*/,
    [ignoreCircular=false] /*{Boolean}*/,
    [maxDeep=100] /*{Number}*/
);

let {value, done} = iterator.next();
let {parent, node, key, path, deep} = value;

// parent is parent node
// node is current node
// key is key of node
// path is path to node
// deep is current deep
```

### Example (es6)
```js
let root = {
    object: {
        number: 1
    },
    string: 'foo'
};

for(let {node, path} of new RecursiveIterator(root)) {
    console.log(path.join('.'), node);
}

// object    Object {number: 1}
// object.number    1
// string    foo
```

## Roadmap
* [Syntax](https://github.com/nervgh/recursive-iterator/wiki/Syntax)
    * [ES6](https://github.com/nervgh/recursive-iterator/wiki/Syntax#es6)
    * [ES5](https://github.com/nervgh/recursive-iterator/wiki/Syntax#es5)
* API
    * [Options](https://github.com/nervgh/recursive-iterator/wiki/Options)
    * [Methods & Callbacks](https://github.com/nervgh/recursive-iterator/wiki/Methods-&-Callbacks)
* [Cookbook (es6)](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6))
    * [Iterator (not recursive)](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6)#iterator-not-recursive)
    * [DomIterator](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6)#domiterator)
    * [Deep copy / Deep clone](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6)#deep-copy--deep-clone)
    * [To Query String](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6)#to-query-string)
    * [To Form Data](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6)#to-form-data)
    * [Uninformed search algorithms](https://github.com/nervgh/recursive-iterator/wiki/Cookbook-(es6)#uninformed-search-algorithms)


## Package managers
### Bower
```
bower install recursive-iterator
```
You could find this module in bower like [_recursive iterator_](http://bower.io/search/?q=recursive%20iterator).

### NPM
```
npm install recursive-iterator
```
You could find this module in npm like [_recursive iterator_](https://www.npmjs.com/search?q=recursive+iterator).

# npmdoc-jsonld

#### api documentation for  [jsonld (v0.4.11)](http://github.com/digitalbazaar/jsonld.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-jsonld.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jsonld) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jsonld.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jsonld)

#### A JSON-LD Processor and API implementation in JavaScript.

[![NPM](https://nodei.co/npm/jsonld.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jsonld)

- [https://npmdoc.github.io/node-npmdoc-jsonld/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jsonld/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jsonld/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jsonld/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jsonld/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jsonld/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Digital Bazaar, Inc.",
        "url": "http://digitalbazaar.com/"
    },
    "browser": {
        "crypto": "./browser/ignore.js",
        "http": "./browser/ignore.js",
        "jsonld-request": "./browser/ignore.js",
        "pkginfo": "./browser/ignore.js",
        "request": "./browser/ignore.js",
        "url": "./browser/ignore.js",
        "util": "./browser/ignore.js",
        "xmldom": "./browser/ignore.js"
    },
    "bugs": {
        "url": "https://github.com/digitalbazaar/jsonld.js/issues"
    },
    "contributors": [
        {
            "name": "Dave Longley"
        }
    ],
    "dependencies": {
        "es6-promise": "^2.0.0",
        "pkginfo": "~0.4.0",
        "request": "^2.61.0",
        "xmldom": "0.1.19"
    },
    "description": "A JSON-LD Processor and API implementation in JavaScript.",
    "devDependencies": {
        "chai": "^3.4.1",
        "commander": "^2.8.0",
        "cors": "^2.7.1",
        "express": "^4.13.3",
        "istanbul": "^0.4.3",
        "jscs": "^3.0.0",
        "jshint": "^2.9.1",
        "mocha": "^2.3.4",
        "mocha-phantomjs": "~3.5.6",
        "phantomjs": "~1.9.18"
    },
    "directories": {},
    "dist": {
        "shasum": "18e97d21f1b20817b65ef3dfd0cfa4f74ba532e1",
        "tarball": "https://registry.npmjs.org/jsonld/-/jsonld-0.4.11.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "968e46433af4faf43e509ccbfc606e7a20a21026",
    "homepage": "http://github.com/digitalbazaar/jsonld.js",
    "keywords": [
        "JSON",
        "Linked Data",
        "JSON-LD",
        "RDF",
        "Semantic Web",
        "jsonld"
    ],
    "license": "BSD-3-Clause",
    "main": "js/jsonld.js",
    "maintainers": [
        {
            "name": "davidlehn"
        },
        {
            "name": "dlongley"
        },
        {
            "name": "msporny"
        }
    ],
    "name": "jsonld",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/digitalbazaar/jsonld.js.git"
    },
    "scripts": {
        "coverage": "make test-coverage",
        "jscs": "jscs js/jsonld.js tests/*.js",
        "jshint": "jshint js/jsonld.js tests/*.js",
        "test": "make test",
        "test-browser": "make test-browser",
        "test-local": "make test-local",
        "test-node": "make test-node"
    },
    "version": "0.4.11"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

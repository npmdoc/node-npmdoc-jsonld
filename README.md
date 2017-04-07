# api documentation for  [jsonld (v0.4.11)](http://github.com/digitalbazaar/jsonld.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-jsonld.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jsonld) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jsonld.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jsonld)
#### A JSON-LD Processor and API implementation in JavaScript.

[![NPM](https://nodei.co/npm/jsonld.png?downloads=true)](https://www.npmjs.com/package/jsonld)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jsonld/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jsonld_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jsonld/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jsonld/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jsonld/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Digital Bazaar, Inc.",
        "email": "support@digitalbazaar.com",
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
        "url": "https://github.com/digitalbazaar/jsonld.js/issues",
        "email": "support@digitalbazaar.com"
    },
    "contributors": [
        {
            "name": "Dave Longley",
            "email": "dlongley@digitalbazaar.com"
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
            "name": "davidlehn",
            "email": "dil@lehn.org"
        },
        {
            "name": "dlongley",
            "email": "dlongley@digitalbazaar.com"
        },
        {
            "name": "msporny",
            "email": "msporny@digitalbazaar.com"
        }
    ],
    "name": "jsonld",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jsonld](#apidoc.module.jsonld)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>ActiveContextCache (size)](#apidoc.element.jsonld.ActiveContextCache)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>DocumentCache (size)](#apidoc.element.jsonld.DocumentCache)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>IdentifierIssuer (prefix)](#apidoc.element.jsonld.IdentifierIssuer)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>JsonLdProcessor ()](#apidoc.element.jsonld.JsonLdProcessor)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>Promise ()](#apidoc.element.jsonld.Promise)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>RequestQueue ()](#apidoc.element.jsonld.RequestQueue)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>UniqueNamer (prefix)](#apidoc.element.jsonld.UniqueNamer)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>addValue (subject, property, value, options)](#apidoc.element.jsonld.addValue)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>compact (input, ctx, options, callback)](#apidoc.element.jsonld.compact)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>compareValues (v1, v2)](#apidoc.element.jsonld.compareValues)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>createNodeMap (input, options, callback)](#apidoc.element.jsonld.createNodeMap)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>documentLoader ()](#apidoc.element.jsonld.documentLoader)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>expand (input, options, callback)](#apidoc.element.jsonld.expand)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>flatten (input, ctx, options, callback)](#apidoc.element.jsonld.flatten)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>frame (input, frame, options, callback)](#apidoc.element.jsonld.frame)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>fromRDF (dataset, options, callback)](#apidoc.element.jsonld.fromRDF)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>getContextValue (ctx, key, type)](#apidoc.element.jsonld.getContextValue)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>getValues (subject, property)](#apidoc.element.jsonld.getValues)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>hasProperty (subject, property)](#apidoc.element.jsonld.hasProperty)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>hasValue (subject, property, value)](#apidoc.element.jsonld.hasValue)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>link (input, ctx, options, callback)](#apidoc.element.jsonld.link)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>loadDocument (url, callback)](#apidoc.element.jsonld.loadDocument)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>merge (docs, ctx, options, callback)](#apidoc.element.jsonld.merge)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>nextTick (callback)](#apidoc.element.jsonld.nextTick)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>normalize (input, options, callback)](#apidoc.element.jsonld.normalize)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>objectify (input, ctx, options, callback)](#apidoc.element.jsonld.objectify)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>parseLinkHeader (header)](#apidoc.element.jsonld.parseLinkHeader)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>prependBase (base, iri)](#apidoc.element.jsonld.prependBase)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>processContext (activeCtx, localCtx)](#apidoc.element.jsonld.processContext)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>promises (options)](#apidoc.element.jsonld.promises)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>promisify (op)](#apidoc.element.jsonld.promisify)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>registerRDFParser (contentType, parser)](#apidoc.element.jsonld.registerRDFParser)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>relabelBlankNodes (input, options)](#apidoc.element.jsonld.relabelBlankNodes)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>removeProperty (subject, property)](#apidoc.element.jsonld.removeProperty)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>removeValue (subject, property, value, options)](#apidoc.element.jsonld.removeValue)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>setImmediate (fn)](#apidoc.element.jsonld.setImmediate)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>toRDF (input, options, callback)](#apidoc.element.jsonld.toRDF)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>unregisterRDFParser (contentType)](#apidoc.element.jsonld.unregisterRDFParser)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>use (extension)](#apidoc.element.jsonld.use)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>useDocumentLoader (type)](#apidoc.element.jsonld.useDocumentLoader)
1.  object <span class="apidocSignatureSpan">jsonld.</span>ActiveContextCache.prototype
1.  object <span class="apidocSignatureSpan">jsonld.</span>DocumentCache.prototype
1.  object <span class="apidocSignatureSpan">jsonld.</span>IdentifierIssuer.prototype
1.  object <span class="apidocSignatureSpan">jsonld.</span>JsonLdProcessor.prototype
1.  object <span class="apidocSignatureSpan">jsonld.</span>RequestQueue.prototype
1.  object <span class="apidocSignatureSpan">jsonld.</span>cache
1.  object <span class="apidocSignatureSpan">jsonld.</span>documentLoaders
1.  object <span class="apidocSignatureSpan">jsonld.</span>url
1.  string <span class="apidocSignatureSpan">jsonld.</span>version

#### [module jsonld.ActiveContextCache](#apidoc.module.jsonld.ActiveContextCache)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>ActiveContextCache (size)](#apidoc.element.jsonld.ActiveContextCache.ActiveContextCache)

#### [module jsonld.ActiveContextCache.prototype](#apidoc.module.jsonld.ActiveContextCache.prototype)
1.  [function <span class="apidocSignatureSpan">jsonld.ActiveContextCache.prototype.</span>get (activeCtx, localCtx)](#apidoc.element.jsonld.ActiveContextCache.prototype.get)
1.  [function <span class="apidocSignatureSpan">jsonld.ActiveContextCache.prototype.</span>set ( activeCtx, localCtx, result)](#apidoc.element.jsonld.ActiveContextCache.prototype.set)

#### [module jsonld.DocumentCache](#apidoc.module.jsonld.DocumentCache)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>DocumentCache (size)](#apidoc.element.jsonld.DocumentCache.DocumentCache)

#### [module jsonld.DocumentCache.prototype](#apidoc.module.jsonld.DocumentCache.prototype)
1.  [function <span class="apidocSignatureSpan">jsonld.DocumentCache.prototype.</span>get (url)](#apidoc.element.jsonld.DocumentCache.prototype.get)
1.  [function <span class="apidocSignatureSpan">jsonld.DocumentCache.prototype.</span>set (url, ctx)](#apidoc.element.jsonld.DocumentCache.prototype.set)

#### [module jsonld.IdentifierIssuer](#apidoc.module.jsonld.IdentifierIssuer)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>IdentifierIssuer (prefix)](#apidoc.element.jsonld.IdentifierIssuer.IdentifierIssuer)

#### [module jsonld.IdentifierIssuer.prototype](#apidoc.module.jsonld.IdentifierIssuer.prototype)
1.  [function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>clone ()](#apidoc.element.jsonld.IdentifierIssuer.prototype.clone)
1.  [function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>getId (old)](#apidoc.element.jsonld.IdentifierIssuer.prototype.getId)
1.  [function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>hasId (old)](#apidoc.element.jsonld.IdentifierIssuer.prototype.hasId)
1.  [function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>isNamed (old)](#apidoc.element.jsonld.IdentifierIssuer.prototype.isNamed)

#### [module jsonld.JsonLdProcessor](#apidoc.module.jsonld.JsonLdProcessor)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>JsonLdProcessor ()](#apidoc.element.jsonld.JsonLdProcessor.JsonLdProcessor)

#### [module jsonld.JsonLdProcessor.prototype](#apidoc.module.jsonld.JsonLdProcessor.prototype)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>compact (input, ctx)](#apidoc.element.jsonld.JsonLdProcessor.prototype.compact)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>expand (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.expand)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>flatten (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.flatten)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>frame (input, frame)](#apidoc.element.jsonld.JsonLdProcessor.prototype.frame)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>fromRDF (dataset)](#apidoc.element.jsonld.JsonLdProcessor.prototype.fromRDF)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>normalize (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.normalize)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>toRDF (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.toRDF)
1.  [function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>toString ()](#apidoc.element.jsonld.JsonLdProcessor.prototype.toString)

#### [module jsonld.RequestQueue](#apidoc.module.jsonld.RequestQueue)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>RequestQueue ()](#apidoc.element.jsonld.RequestQueue.RequestQueue)

#### [module jsonld.RequestQueue.prototype](#apidoc.module.jsonld.RequestQueue.prototype)
1.  [function <span class="apidocSignatureSpan">jsonld.RequestQueue.prototype.</span>add (url, callback)](#apidoc.element.jsonld.RequestQueue.prototype.add)
1.  [function <span class="apidocSignatureSpan">jsonld.RequestQueue.prototype.</span>wrapLoader (loader)](#apidoc.element.jsonld.RequestQueue.prototype.wrapLoader)

#### [module jsonld.documentLoaders](#apidoc.module.jsonld.documentLoaders)
1.  [function <span class="apidocSignatureSpan">jsonld.documentLoaders.</span>jquery ($, options)](#apidoc.element.jsonld.documentLoaders.jquery)
1.  [function <span class="apidocSignatureSpan">jsonld.documentLoaders.</span>node (options)](#apidoc.element.jsonld.documentLoaders.node)
1.  [function <span class="apidocSignatureSpan">jsonld.documentLoaders.</span>xhr (options)](#apidoc.element.jsonld.documentLoaders.xhr)

#### [module jsonld.promises](#apidoc.module.jsonld.promises)
1.  [function <span class="apidocSignatureSpan">jsonld.</span>promises (options)](#apidoc.element.jsonld.promises.promises)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>compact (input, ctx)](#apidoc.element.jsonld.promises.compact)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>createNodeMap (input)](#apidoc.element.jsonld.promises.createNodeMap)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>expand (input)](#apidoc.element.jsonld.promises.expand)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>flatten (input)](#apidoc.element.jsonld.promises.flatten)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>frame (input, frame)](#apidoc.element.jsonld.promises.frame)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>fromRDF (dataset)](#apidoc.element.jsonld.promises.fromRDF)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>link (input, ctx)](#apidoc.element.jsonld.promises.link)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>merge (input)](#apidoc.element.jsonld.promises.merge)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>normalize (input)](#apidoc.element.jsonld.promises.normalize)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>objectify (input)](#apidoc.element.jsonld.promises.objectify)
1.  [function <span class="apidocSignatureSpan">jsonld.promises.</span>toRDF (input)](#apidoc.element.jsonld.promises.toRDF)

#### [module jsonld.url](#apidoc.module.jsonld.url)
1.  [function <span class="apidocSignatureSpan">jsonld.url.</span>parse (str, parser)](#apidoc.element.jsonld.url.parse)
1.  object <span class="apidocSignatureSpan">jsonld.url.</span>parsers



# <a name="apidoc.module.jsonld"></a>[module jsonld](#apidoc.module.jsonld)

#### <a name="apidoc.element.jsonld.ActiveContextCache"></a>[function <span class="apidocSignatureSpan">jsonld.</span>ActiveContextCache (size)](#apidoc.element.jsonld.ActiveContextCache)
- description and source-code
```javascript
ActiveContextCache = function (size) {
  this.order = [];
  this.cache = {};
  this.size = size || 100;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.DocumentCache"></a>[function <span class="apidocSignatureSpan">jsonld.</span>DocumentCache (size)](#apidoc.element.jsonld.DocumentCache)
- description and source-code
```javascript
DocumentCache = function (size) {
  this.order = [];
  this.cache = {};
  this.size = size || 50;
  this.expires = 30 * 1000;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.IdentifierIssuer"></a>[function <span class="apidocSignatureSpan">jsonld.</span>IdentifierIssuer (prefix)](#apidoc.element.jsonld.IdentifierIssuer)
- description and source-code
```javascript
function IdentifierIssuer(prefix) {
  this.prefix = prefix;
  this.counter = 0;
  this.existing = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor"></a>[function <span class="apidocSignatureSpan">jsonld.</span>JsonLdProcessor ()](#apidoc.element.jsonld.JsonLdProcessor)
- description and source-code
```javascript
function JsonLdProcessor() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.Promise"></a>[function <span class="apidocSignatureSpan">jsonld.</span>Promise ()](#apidoc.element.jsonld.Promise)
- description and source-code
```javascript
function Promise() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.RequestQueue"></a>[function <span class="apidocSignatureSpan">jsonld.</span>RequestQueue ()](#apidoc.element.jsonld.RequestQueue)
- description and source-code
```javascript
RequestQueue = function () {
  this._requests = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.UniqueNamer"></a>[function <span class="apidocSignatureSpan">jsonld.</span>UniqueNamer (prefix)](#apidoc.element.jsonld.UniqueNamer)
- description and source-code
```javascript
function IdentifierIssuer(prefix) {
  this.prefix = prefix;
  this.counter = 0;
  this.existing = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.addValue"></a>[function <span class="apidocSignatureSpan">jsonld.</span>addValue (subject, property, value, options)](#apidoc.element.jsonld.addValue)
- description and source-code
```javascript
addValue = function (subject, property, value, options) {
  options = options || {};
  if(!('propertyIsArray' in options)) {
    options.propertyIsArray = false;
  }
  if(!('allowDuplicate' in options)) {
    options.allowDuplicate = true;
  }

  if(_isArray(value)) {
    if(value.length === 0 && options.propertyIsArray &&
      !(property in subject)) {
      subject[property] = [];
    }
    for(var i = 0; i < value.length; ++i) {
      jsonld.addValue(subject, property, value[i], options);
    }
  } else if(property in subject) {
    // check if subject already has value if duplicates not allowed
    var hasValue = (!options.allowDuplicate &&
      jsonld.hasValue(subject, property, value));

    // make property an array if value not present or always an array
    if(!_isArray(subject[property]) &&
      (!hasValue || options.propertyIsArray)) {
      subject[property] = [subject[property]];
    }

    // add new value
    if(!hasValue) {
      subject[property].push(value);
    }
  } else {
    // add new value as set or single value
    subject[property] = options.propertyIsArray ? [value] : value;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.compact"></a>[function <span class="apidocSignatureSpan">jsonld.</span>compact (input, ctx, options, callback)](#apidoc.element.jsonld.compact)
- description and source-code
```javascript
compact = function (input, ctx, options, callback) {
  if(arguments.length < 2) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not compact, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  if(ctx === null) {
    return jsonld.nextTick(function() {
      callback(new JsonLdError(
        'The compaction context must not be null.',
        'jsonld.CompactError', {code: 'invalid local context'}));
    });
  }

  // nothing to compact
  if(input === null) {
    return jsonld.nextTick(function() {
      callback(null, null);
    });
  }

  // set default options
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('compactArrays' in options)) {
    options.compactArrays = true;
  }
  if(!('graph' in options)) {
    options.graph = false;
  }
  if(!('skipExpansion' in options)) {
    options.skipExpansion = false;
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }
  if(!('link' in options)) {
    options.link = false;
  }
  if(options.link) {
    // force skip expansion when linking, "link" is not part of the public
    // API, it should only be called from framing
    options.skipExpansion = true;
  }

  var expand = function(input, options, callback) {
    if(options.skipExpansion) {
      return jsonld.nextTick(function() {
        callback(null, input);
      });
    }
    jsonld.expand(input, options, callback);
  };

  // expand input then do compaction
  expand(input, options, function(err, expanded) {
    if(err) {
      return callback(new JsonLdError(
        'Could not expand input before compaction.',
        'jsonld.CompactError', {cause: err}));
    }

    // process context
    var activeCtx = _getInitialContext(options);
    jsonld.processContext(activeCtx, ctx, options, function(err, activeCtx) {
      if(err) {
        return callback(new JsonLdError(
          'Could not process context before compaction.',
          'jsonld.CompactError', {cause: err}));
      }

      var compacted;
      try {
        // do compaction
        compacted = new Processor().compact(activeCtx, null, expanded, options);
      } catch(ex) {
        return callback(ex);
      }

      cleanup(null, compacted, activeCtx, options);
    });
  });

  // performs clean up after compaction
  function cleanup(err, compacted, activeCtx, options) {
    if(err) {
      return callback(err);
    }

    if(options.compactArrays && !options.graph && _isArray(compacted)) {
      if(compacted.length === 1) {
        // simplify to a single item
        compacted = compacted[0];
      } else if(compacted.length === 0) {
        // simplify to an empty object
        compacted = {};
      }
    } else if(options.graph && _isObject(compacted)) {
      // always use array if graph option is on
      compacted = [compacted];
    }

    // follow @context key
    if(_isObject(ctx) && '@context' in ctx) {
      ctx = ctx['@context'];
    }

    // build output context
    ctx = _clone(ctx);
    if(!_isArray(ctx)) {
      ctx = [ctx];
    }
    // remove empty contexts
    var tmp = ctx;
    ctx = [];
    for(var i = 0; i < tmp.length; ++i) {
      if(!_isObject(tmp[i]) || Object.keys(tmp[i]).length > 0) {
        ctx.push(tmp[i]);
      }
    }

    // remove array if only one context
    var hasContext = (ctx.length > 0);
    if(ctx.length === 1) {
      ctx = ctx[0];
    }

    // add context and/or @graph
    if(_isArray(compacted)) {
      // use '@graph' keyword
      var kwgraph = _compactIri(activeCtx, '@graph');
      var graph = compacted;
      compacted = {};
      if(hasContext) {
        compacted['@context'] = ctx;
      }
      compacted[kwgraph] = graph;
    } else if(_isObject(compacted) && hasContext) {
      // reorder keys so @context is first
      var graph = compacted;
      compacted = {'@context': ctx};
      for(var key in graph) {
        compacted[key] = graph[key];
      }
    }

    callback ...
```
- example usage
```shell
...
"name": "http://schema.org/name",
"homepage": {"@id": "http://schema.org/url", "@type": "@id"},
"image": {"@id": "http://schema.org/image", "@type": "@id"}
};

// compact a document according to a particular context
// see: http://json-ld.org/spec/latest/json-ld/#compacted-document-form
jsonld.compact(doc, context, function(err, compacted) {
console.log(JSON.stringify(compacted, null, 2));
/* Output:
{
  "@context": {...},
  "name": "Manu Sporny",
  "homepage": "http://manu.sporny.org/",
  "image": "http://manu.sporny.org/images/manu.png"
...
```

#### <a name="apidoc.element.jsonld.compareValues"></a>[function <span class="apidocSignatureSpan">jsonld.</span>compareValues (v1, v2)](#apidoc.element.jsonld.compareValues)
- description and source-code
```javascript
compareValues = function (v1, v2) {
  // 1. equal primitives
  if(v1 === v2) {
    return true;
  }

  // 2. equal @values
  if(_isValue(v1) && _isValue(v2) &&
    v1['@value'] === v2['@value'] &&
    v1['@type'] === v2['@type'] &&
    v1['@language'] === v2['@language'] &&
    v1['@index'] === v2['@index']) {
    return true;
  }

  // 3. equal @ids
  if(_isObject(v1) && ('@id' in v1) && _isObject(v2) && ('@id' in v2)) {
    return v1['@id'] === v2['@id'];
  }

  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.createNodeMap"></a>[function <span class="apidocSignatureSpan">jsonld.</span>createNodeMap (input, options, callback)](#apidoc.element.jsonld.createNodeMap)
- description and source-code
```javascript
createNodeMap = function (input, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not create node map, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }

  // expand input
  jsonld.expand(input, options, function(err, _input) {
    if(err) {
      return callback(new JsonLdError(
        'Could not expand input before creating node map.',
        'jsonld.CreateNodeMapError', {cause: err}));
    }

    var nodeMap;
    try {
      nodeMap = new Processor().createNodeMap(_input, options);
    } catch(ex) {
      return callback(ex);
    }

    callback(null, nodeMap);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.documentLoader"></a>[function <span class="apidocSignatureSpan">jsonld.</span>documentLoader ()](#apidoc.element.jsonld.documentLoader)
- description and source-code
```javascript
documentLoader = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.expand"></a>[function <span class="apidocSignatureSpan">jsonld.</span>expand (input, options, callback)](#apidoc.element.jsonld.expand)
- description and source-code
```javascript
expand = function (input, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not expand, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }
  if(!('keepFreeFloatingNodes' in options)) {
    options.keepFreeFloatingNodes = false;
  }

  jsonld.nextTick(function() {
    // if input is a string, attempt to dereference remote document
    if(typeof input === 'string') {
      var done = function(err, remoteDoc) {
        if(err) {
          return callback(err);
        }
        try {
          if(!remoteDoc.document) {
            throw new JsonLdError(
              'No remote document found at the given URL.',
              'jsonld.NullRemoteDocument');
          }
          if(typeof remoteDoc.document === 'string') {
            remoteDoc.document = JSON.parse(remoteDoc.document);
          }
        } catch(ex) {
          return callback(new JsonLdError(
            'Could not retrieve a JSON-LD document from the URL. URL ' +
            'dereferencing not implemented.', 'jsonld.LoadDocumentError', {
              code: 'loading document failed',
              cause: ex,
              remoteDoc: remoteDoc
          }));
        }
        expand(remoteDoc);
      };
      var promise = options.documentLoader(input, done);
      if(promise && 'then' in promise) {
        promise.then(done.bind(null, null), done);
      }
      return;
    }
    // nothing to load
    expand({contextUrl: null, documentUrl: null, document: input});
  });

  function expand(remoteDoc) {
    // set default base
    if(!('base' in options)) {
      options.base = remoteDoc.documentUrl || '';
    }
    // build meta-object and retrieve all @context URLs
    var input = {
      document: _clone(remoteDoc.document),
      remoteContext: {'@context': remoteDoc.contextUrl}
    };
    if('expandContext' in options) {
      var expandContext = _clone(options.expandContext);
      if(typeof expandContext === 'object' && '@context' in expandContext) {
        input.expandContext = expandContext;
      } else {
        input.expandContext = {'@context': expandContext};
      }
    }
    _retrieveContextUrls(input, options, function(err, input) {
      if(err) {
        return callback(err);
      }

      var expanded;
      try {
        var processor = new Processor();
        var activeCtx = _getInitialContext(options);
        var document = input.document;
        var remoteContext = input.remoteContext['@context'];

        // process optional expandContext
        if(input.expandContext) {
          activeCtx = processor.processContext(
            activeCtx, input.expandContext['@context'], options);
        }

        // process remote context from HTTP Link Header
        if(remoteContext) {
          activeCtx = processor.processContext(
            activeCtx, remoteContext, options);
        }

        // expand document
        expanded = processor.expand(
          activeCtx, null, document, options, false);

        // optimize away @graph with no other properties
        if(_isObject(expanded) && ('@graph' in expanded) &&
          Object.keys(expanded).length === 1) {
          expanded = expanded['@graph'];
        } else if(expanded === null) {
          expanded = [];
        }

        // normalize to an array
        if(!_isArray(expanded)) {
          expanded = [expanded];
        }
      } catch(ex) {
        return callback(ex);
      }
      callback(null, expanded);
    });
  }
}
```
- example usage
```shell
...
});

// compact using URLs
jsonld.compact('http://example.org/doc', 'http://example.org/context', ...);

// expand a document, removing its context
// see: http://json-ld.org/spec/latest/json-ld/#expanded-document-form
jsonld.expand(compacted, function(err, expanded) {
/* Output:
{
  "http://schema.org/name": [{"@value": "Manu Sporny"}],
  "http://schema.org/url": [{"@id": "http://manu.sporny.org/"}],
  "http://schema.org/image": [{"@id": "http://manu.sporny.org/images/manu.png"}]
}
*/
...
```

#### <a name="apidoc.element.jsonld.flatten"></a>[function <span class="apidocSignatureSpan">jsonld.</span>flatten (input, ctx, options, callback)](#apidoc.element.jsonld.flatten)
- description and source-code
```javascript
flatten = function (input, ctx, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not flatten, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  } else if(typeof ctx === 'function') {
    callback = ctx;
    ctx = null;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }

  // expand input
  jsonld.expand(input, options, function(err, _input) {
    if(err) {
      return callback(new JsonLdError(
        'Could not expand input before flattening.',
        'jsonld.FlattenError', {cause: err}));
    }

    var flattened;
    try {
      // do flattening
      flattened = new Processor().flatten(_input);
    } catch(ex) {
      return callback(ex);
    }

    if(ctx === null) {
      return callback(null, flattened);
    }

    // compact result (force @graph option to true, skip expansion)
    options.graph = true;
    options.skipExpansion = true;
    jsonld.compact(flattened, ctx, options, function(err, compacted) {
      if(err) {
        return callback(new JsonLdError(
          'Could not compact flattened output.',
          'jsonld.FlattenError', {cause: err}));
      }
      callback(null, compacted);
    });
  });
}
```
- example usage
```shell
...
});

// expand using URLs
jsonld.expand('http://example.org/doc', ...);

// flatten a document
// see: http://json-ld.org/spec/latest/json-ld/#flattened-document-form
jsonld.flatten(doc, function(err, flattened) {
// all deep-level trees flattened to the top-level
});

// frame a document
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
// document transformed into a particular tree structure per the given frame
...
```

#### <a name="apidoc.element.jsonld.frame"></a>[function <span class="apidocSignatureSpan">jsonld.</span>frame (input, frame, options, callback)](#apidoc.element.jsonld.frame)
- description and source-code
```javascript
frame = function (input, frame, options, callback) {
  if(arguments.length < 2) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not frame, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }
  if(!('embed' in options)) {
    options.embed = '@last';
  }
  options.explicit = options.explicit || false;
  if(!('requireAll' in options)) {
    options.requireAll = true;
  }
  options.omitDefault = options.omitDefault || false;

  jsonld.nextTick(function() {
    // if frame is a string, attempt to dereference remote document
    if(typeof frame === 'string') {
      var done = function(err, remoteDoc) {
        if(err) {
          return callback(err);
        }
        try {
          if(!remoteDoc.document) {
            throw new JsonLdError(
              'No remote document found at the given URL.',
              'jsonld.NullRemoteDocument');
          }
          if(typeof remoteDoc.document === 'string') {
            remoteDoc.document = JSON.parse(remoteDoc.document);
          }
        } catch(ex) {
          return callback(new JsonLdError(
            'Could not retrieve a JSON-LD document from the URL. URL ' +
            'dereferencing not implemented.', 'jsonld.LoadDocumentError', {
              code: 'loading document failed',
              cause: ex,
              remoteDoc: remoteDoc
          }));
        }
        doFrame(remoteDoc);
      };
      var promise = options.documentLoader(frame, done);
      if(promise && 'then' in promise) {
        promise.then(done.bind(null, null), done);
      }
      return;
    }
    // nothing to load
    doFrame({contextUrl: null, documentUrl: null, document: frame});
  });

  function doFrame(remoteFrame) {
    // preserve frame context and add any Link header context
    var frame = remoteFrame.document;
    var ctx;
    if(frame) {
      ctx = frame['@context'];
      if(remoteFrame.contextUrl) {
        if(!ctx) {
          ctx = remoteFrame.contextUrl;
        } else if(_isArray(ctx)) {
          ctx.push(remoteFrame.contextUrl);
        } else {
          ctx = [ctx, remoteFrame.contextUrl];
        }
        frame['@context'] = ctx;
      } else {
        ctx = ctx || {};
      }
    } else {
      ctx = {};
    }

    // expand input
    jsonld.expand(input, options, function(err, expanded) {
      if(err) {
        return callback(new JsonLdError(
          'Could not expand input before framing.',
          'jsonld.FrameError', {cause: err}));
      }

      // expand frame
      var opts = _clone(options);
      opts.isFrame = true;
      opts.keepFreeFloatingNodes = true;
      jsonld.expand(frame, opts, function(err, expandedFrame) {
        if(err) {
          return callback(new JsonLdError(
            'Could not expand frame before framing.',
            'jsonld.FrameError', {cause: err}));
        }

        var framed;
        try {
          // do framing
          framed = new Processor().frame(expanded, expandedFrame, opts);
        } catch(ex) {
          return callback(ex);
        }

        // compact result (force @graph option to true, skip expansion,
        // check for linked embeds)
        opts.graph = true;
        opts.skipExpansion = true;
        opts.link = {};
        jsonld.compact(framed, ctx, opts, function(err, compacted, ctx) {
          if(err) {
            return callback(new JsonLdError(
              'Could not compact framed output.',
              'jsonld.FrameError', {cause: err}));
          }
          // get graph alias
          var graph = _compactIri(ctx, '@graph');
          // remove @preserve from results
          opts.link = {};
          compacted[graph] = _removePreserve(ctx, compacted[graph], opts);
          callback(null, compacted);
        });
      }); ...
```
- example usage
```shell
...
// see: http://json-ld.org/spec/latest/json-ld/#flattened-document-form
jsonld.flatten(doc, function(err, flattened) {
// all deep-level trees flattened to the top-level
});

// frame a document
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
// document transformed into a particular tree structure per the given frame
});

// normalize a document using the RDF Dataset Normalization Algorithm
// (URDNA2015), see: http://json-ld.github.io/normalization/spec/
jsonld.normalize(doc, {
algorithm: 'URDNA2015',
...
```

#### <a name="apidoc.element.jsonld.fromRDF"></a>[function <span class="apidocSignatureSpan">jsonld.</span>fromRDF (dataset, options, callback)](#apidoc.element.jsonld.fromRDF)
- description and source-code
```javascript
fromRDF = function (dataset, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not convert from RDF, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('useRdfType' in options)) {
    options.useRdfType = false;
  }
  if(!('useNativeTypes' in options)) {
    options.useNativeTypes = false;
  }

  if(!('format' in options) && _isString(dataset)) {
    // set default format to nquads
    if(!('format' in options)) {
      options.format = 'application/nquads';
    }
  }

  jsonld.nextTick(function() {
    // handle special format
    var rdfParser;
    if(options.format) {
      // check supported formats
      rdfParser = options.rdfParser || _rdfParsers[options.format];
      if(!rdfParser) {
        return callback(new JsonLdError(
          'Unknown input format.',
          'jsonld.UnknownFormat', {format: options.format}));
      }
    } else {
      // no-op parser, assume dataset already parsed
      rdfParser = function() {
        return dataset;
      };
    }

    var callbackCalled = false;
    try {
      // rdf parser may be async or sync, always pass callback
      dataset = rdfParser(dataset, function(err, dataset) {
        callbackCalled = true;
        if(err) {
          return callback(err);
        }
        fromRDF(dataset, options, callback);
      });
    } catch(e) {
      if(!callbackCalled) {
        return callback(e);
      }
      throw e;
    }
    // handle synchronous or promise-based parser
    if(dataset) {
      // if dataset is actually a promise
      if('then' in dataset) {
        return dataset.then(function(dataset) {
          fromRDF(dataset, options, callback);
        }, callback);
      }
      // parser is synchronous
      fromRDF(dataset, options, callback);
    }

    function fromRDF(dataset, options, callback) {
      // convert from RDF
      new Processor().fromRDF(dataset, options, callback);
    }
  });
}
```
- example usage
```shell
...

// serialize a document to N-Quads (RDF)
jsonld.toRDF(doc, {format: 'application/nquads'}, function(err, nquads) {
// nquads is a string of nquads
});

// deserialize N-Quads (RDF) to JSON-LD
jsonld.fromRDF(nquads, {format: 'application/nquads'}, function(err, doc) {
// doc is JSON-LD
});

// register a custom async-callback-based RDF parser
jsonld.registerRDFParser = function(contentType, function(input, callback) {
// parse input to a jsonld.js RDF dataset object...
callback(err, dataset);
...
```

#### <a name="apidoc.element.jsonld.getContextValue"></a>[function <span class="apidocSignatureSpan">jsonld.</span>getContextValue (ctx, key, type)](#apidoc.element.jsonld.getContextValue)
- description and source-code
```javascript
getContextValue = function (ctx, key, type) {
  var rval = null;

  // return null for invalid key
  if(key === null) {
    return rval;
  }

  // get default language
  if(type === '@language' && (type in ctx)) {
    rval = ctx[type];
  }

  // get specific entry information
  if(ctx.mappings[key]) {
    var entry = ctx.mappings[key];

    if(_isUndefined(type)) {
      // return whole entry
      rval = entry;
    } else if(type in entry) {
      // return entry value for type
      rval = entry[type];
    }
  }

  return rval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.getValues"></a>[function <span class="apidocSignatureSpan">jsonld.</span>getValues (subject, property)](#apidoc.element.jsonld.getValues)
- description and source-code
```javascript
getValues = function (subject, property) {
  var rval = subject[property] || [];
  if(!_isArray(rval)) {
    rval = [rval];
  }
  return rval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.hasProperty"></a>[function <span class="apidocSignatureSpan">jsonld.</span>hasProperty (subject, property)](#apidoc.element.jsonld.hasProperty)
- description and source-code
```javascript
hasProperty = function (subject, property) {
  var rval = false;
  if(property in subject) {
    var value = subject[property];
    rval = (!_isArray(value) || value.length > 0);
  }
  return rval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.hasValue"></a>[function <span class="apidocSignatureSpan">jsonld.</span>hasValue (subject, property, value)](#apidoc.element.jsonld.hasValue)
- description and source-code
```javascript
hasValue = function (subject, property, value) {
  var rval = false;
  if(jsonld.hasProperty(subject, property)) {
    var val = subject[property];
    var isList = _isList(val);
    if(_isArray(val) || isList) {
      if(isList) {
        val = val['@list'];
      }
      for(var i = 0; i < val.length; ++i) {
        if(jsonld.compareValues(value, val[i])) {
          rval = true;
          break;
        }
      }
    } else if(!_isArray(value)) {
      // avoid matching the set of values with an array value parameter
      rval = jsonld.compareValues(value, val);
    }
  }
  return rval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.link"></a>[function <span class="apidocSignatureSpan">jsonld.</span>link (input, ctx, options, callback)](#apidoc.element.jsonld.link)
- description and source-code
```javascript
link = function (input, ctx, options, callback) {
  // API matches running frame with a wildcard frame and embed: '@link'
  // get arguments
  var frame = {};
  if(ctx) {
    frame['@context'] = ctx;
  }
  frame['@embed'] = '@link';
  jsonld.frame(input, frame, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.loadDocument"></a>[function <span class="apidocSignatureSpan">jsonld.</span>loadDocument (url, callback)](#apidoc.element.jsonld.loadDocument)
- description and source-code
```javascript
loadDocument = function (url, callback) {
  var promise = jsonld.documentLoader(url, callback);
  if(promise && 'then' in promise) {
    promise.then(callback.bind(null, null), callback);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.merge"></a>[function <span class="apidocSignatureSpan">jsonld.</span>merge (docs, ctx, options, callback)](#apidoc.element.jsonld.merge)
- description and source-code
```javascript
merge = function (docs, ctx, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not merge, too few arguments.'));
    });
  }
  if(!_isArray(docs)) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not merge, "docs" must be an array.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  } else if(typeof ctx === 'function') {
    callback = ctx;
    ctx = null;
    options = {};
  }
  options = options || {};

  // expand all documents
  var expanded = [];
  var error = null;
  var count = docs.length;
  for(var i = 0; i < docs.length; ++i) {
    var opts = {};
    for(var key in options) {
      opts[key] = options[key];
    }
    jsonld.expand(docs[i], opts, expandComplete);
  }

  function expandComplete(err, _input) {
    if(error) {
      return;
    }
    if(err) {
      error = err;
      return callback(new JsonLdError(
        'Could not expand input before flattening.',
        'jsonld.FlattenError', {cause: err}));
    }
    expanded.push(_input);
    if(--count === 0) {
      merge(expanded);
    }
  }

  function merge(expanded) {
    var mergeNodes = true;
    if('mergeNodes' in options) {
      mergeNodes = options.mergeNodes;
    }

    var issuer = options.namer || options.issuer || new IdentifierIssuer('_:b');
    var graphs = {'@default': {}};

    var defaultGraph;
    try {
      for(var i = 0; i < expanded.length; ++i) {
        // uniquely relabel blank nodes
        var doc = expanded[i];
        doc = jsonld.relabelBlankNodes(doc, {
          issuer: new IdentifierIssuer('_:b' + i + '-')
        });

        // add nodes to the shared node map graphs if merging nodes, to a
        // separate graph set if not
        var _graphs = (mergeNodes || i === 0) ? graphs : {'@default': {}};
        _createNodeMap(doc, _graphs, '@default', issuer);

        if(_graphs !== graphs) {
          // merge document graphs but don't merge existing nodes
          for(var graphName in _graphs) {
            var _nodeMap = _graphs[graphName];
            if(!(graphName in graphs)) {
              graphs[graphName] = _nodeMap;
              continue;
            }
            var nodeMap = graphs[graphName];
            for(var key in _nodeMap) {
              if(!(key in nodeMap)) {
                nodeMap[key] = _nodeMap[key];
              }
            }
          }
        }
      }

      // add all non-default graphs to default graph
      defaultGraph = _mergeNodeMaps(graphs);
    } catch(ex) {
      return callback(ex);
    }

    // produce flattened output
    var flattened = [];
    var keys = Object.keys(defaultGraph).sort();
    for(var ki = 0; ki < keys.length; ++ki) {
      var node = defaultGraph[keys[ki]];
      // only add full subjects to top-level
      if(!_isSubjectReference(node)) {
        flattened.push(node);
      }
    }

    if(ctx === null) {
      return callback(null, flattened);
    }

    // compact result (force @graph option to true, skip expansion)
    options.graph = true;
    options.skipExpansion = true;
    jsonld.compact(flattened, ctx, options, function(err, compacted) {
      if(err) {
        return callback(new JsonLdError(
          'Could not compact merged output.',
          'jsonld.MergeError', {cause: err}));
      }
      callback(null, compacted);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.nextTick"></a>[function <span class="apidocSignatureSpan">jsonld.</span>nextTick (callback)](#apidoc.element.jsonld.nextTick)
- description and source-code
```javascript
function nextTick(callback) {
  if (typeof callback !== 'function')
    throw new TypeError('callback is not a function');
  // on the way out, don't bother. it won't get fired anyway.
  if (process._exiting)
    return;

  var args;
  if (arguments.length > 1) {
    args = new Array(arguments.length - 1);
    for (var i = 1; i < arguments.length; i++)
      args[i - 1] = arguments[i];
  }

  nextTickQueue.push({
    callback,
    domain: process.domain || null,
    args
  });
  tickInfo[kLength]++;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.normalize"></a>[function <span class="apidocSignatureSpan">jsonld.</span>normalize (input, options, callback)](#apidoc.element.jsonld.normalize)
- description and source-code
```javascript
normalize = function (input, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not normalize, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('algorithm' in options)) {
    options.algorithm = 'URGNA2012';
  }
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }

  if('inputFormat' in options) {
    if(options.inputFormat !== 'application/nquads') {
      return callback(new JsonLdError(
        'Unknown normalization input format.',
        'jsonld.NormalizeError'));
    }
    var parsedInput = _parseNQuads(input);
    // do normalization
    new Processor().normalize(parsedInput, options, callback);
  } else {
    // convert to RDF dataset then do normalization
    var opts = _clone(options);
    delete opts.format;
    opts.produceGeneralizedRdf = false;
    jsonld.toRDF(input, opts, function(err, dataset) {
      if(err) {
        return callback(new JsonLdError(
          'Could not convert input to RDF dataset before normalization.',
          'jsonld.NormalizeError', {cause: err}));
      }
      // do normalization
      new Processor().normalize(dataset, options, callback);
    });
  }
}
```
- example usage
```shell
...
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
  // document transformed into a particular tree structure per the given frame
});

// normalize a document using the RDF Dataset Normalization Algorithm
// (URDNA2015), see: http://json-ld.github.io/normalization/spec/
jsonld.normalize(doc, {
  algorithm: 'URDNA2015',
  format: 'application/nquads'
}, function(err, normalized) {
  // normalized is a string that is a canonical representation of the document
  // that can be used for hashing, comparison, etc.
});
...
```

#### <a name="apidoc.element.jsonld.objectify"></a>[function <span class="apidocSignatureSpan">jsonld.</span>objectify (input, ctx, options, callback)](#apidoc.element.jsonld.objectify)
- description and source-code
```javascript
objectify = function (input, ctx, options, callback) {
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }

  // expand input
  jsonld.expand(input, options, function(err, _input) {
    if(err) {
      return callback(new JsonLdError(
        'Could not expand input before linking.',
        'jsonld.LinkError', {cause: err}));
    }

    var flattened;
    try {
      // flatten the graph
      flattened = new Processor().flatten(_input);
    } catch(ex) {
      return callback(ex);
    }

    // compact result (force @graph option to true, skip expansion)
    options.graph = true;
    options.skipExpansion = true;
    jsonld.compact(flattened, ctx, options, function(err, compacted, ctx) {
      if(err) {
        return callback(new JsonLdError(
          'Could not compact flattened output before linking.',
          'jsonld.LinkError', {cause: err}));
      }
      // get graph alias
      var graph = _compactIri(ctx, '@graph');
      var top = compacted[graph][0];

      var recurse = function(subject) {
        // can't replace just a string
        if(!_isObject(subject) && !_isArray(subject)) {
          return;
        }

        // bottom out recursion on re-visit
        if(_isObject(subject)) {
          if(recurse.visited[subject['@id']]) {
            return;
          }
          recurse.visited[subject['@id']] = true;
        }

        // each array element *or* object key
        for(var k in subject) {
          var obj = subject[k];
          var isid = (jsonld.getContextValue(ctx, k, '@type') === '@id');

          // can't replace a non-object or non-array unless it's an @id
          if(!_isArray(obj) && !_isObject(obj) && !isid) {
            continue;
          }

          if(_isString(obj) && isid) {
            subject[k] = obj = top[obj];
            recurse(obj);
          } else if(_isArray(obj)) {
            for(var i = 0; i < obj.length; ++i) {
              if(_isString(obj[i]) && isid) {
                obj[i] = top[obj[i]];
              } else if(_isObject(obj[i]) && '@id' in obj[i]) {
                obj[i] = top[obj[i]['@id']];
              }
              recurse(obj[i]);
            }
          } else if(_isObject(obj)) {
            var sid = obj['@id'];
            subject[k] = obj = top[sid];
            recurse(obj);
          }
        }
      };
      recurse.visited = {};
      recurse(top);

      compacted.of_type = {};
      for(var s in top) {
        if(!('@type' in top[s])) {
          continue;
        }
        var types = top[s]['@type'];
        if(!_isArray(types)) {
          types = [types];
        }
        for(var t = 0; t < types.length; ++t) {
          if(!(types[t] in compacted.of_type)) {
            compacted.of_type[types[t]] = [];
          }
          compacted.of_type[types[t]].push(top[s]);
        }
      }
      callback(null, compacted);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.parseLinkHeader"></a>[function <span class="apidocSignatureSpan">jsonld.</span>parseLinkHeader (header)](#apidoc.element.jsonld.parseLinkHeader)
- description and source-code
```javascript
parseLinkHeader = function (header) {
  var rval = {};
  // split on unbracketed/unquoted commas
  var entries = header.match(/(?:<[^>]*?>|"[^"]*?"|[^,])+/g);
  var rLinkHeader = /\s*<([^>]*?)>\s*(?:;\s*(.*))?/;
  for(var i = 0; i < entries.length; ++i) {
    var match = entries[i].match(rLinkHeader);
    if(!match) {
      continue;
    }
    var result = {target: match[1]};
    var params = match[2];
    var rParams = /(.*?)=(?:(?:"([^"]*?)")|([^"]*?))\s*(?:(?:;\s*)|$)/g;
    while(match = rParams.exec(params)) {
      result[match[1]] = (match[2] === undefined) ? match[3] : match[2];
    }
    var rel = result['rel'] || '';
    if(_isArray(rval[rel])) {
      rval[rel].push(result);
    } else if(rel in rval) {
      rval[rel] = [rval[rel], result];
    } else {
      rval[rel] = result;
    }
  }
  return rval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.prependBase"></a>[function <span class="apidocSignatureSpan">jsonld.</span>prependBase (base, iri)](#apidoc.element.jsonld.prependBase)
- description and source-code
```javascript
prependBase = function (base, iri) {
  return _prependBase(base, iri);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.processContext"></a>[function <span class="apidocSignatureSpan">jsonld.</span>processContext (activeCtx, localCtx)](#apidoc.element.jsonld.processContext)
- description and source-code
```javascript
processContext = function (activeCtx, localCtx) {
  // get arguments
  var options = {};
  var callbackArg = 2;
  if(arguments.length > 3) {
    options = arguments[2] || {};
    callbackArg += 1;
  }
  var callback = arguments[callbackArg];

  // set default options
  if(!('base' in options)) {
    options.base = '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }

  // return initial context early for null context
  if(localCtx === null) {
    return callback(null, _getInitialContext(options));
  }

  // retrieve URLs in localCtx
  localCtx = _clone(localCtx);
  if(!(_isObject(localCtx) && '@context' in localCtx)) {
    localCtx = {'@context': localCtx};
  }
  _retrieveContextUrls(localCtx, options, function(err, ctx) {
    if(err) {
      return callback(err);
    }
    try {
      // process context
      ctx = new Processor().processContext(activeCtx, ctx, options);
    } catch(ex) {
      return callback(ex);
    }
    callback(null, ctx);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promises"></a>[function <span class="apidocSignatureSpan">jsonld.</span>promises (options)](#apidoc.element.jsonld.promises)
- description and source-code
```javascript
promises = function (options) {
  options = options || {};
  var slice = Array.prototype.slice;
  var promisify = jsonld.promisify;

  // handle 'api' option as version, set defaults
  var api = options.api || {};
  var version = options.version || 'jsonld.js';
  if(typeof options.api === 'string') {
    if(!options.version) {
      version = options.api;
    }
    api = {};
  }

  api.expand = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not expand, too few arguments.');
    }
    return promisify.apply(null, [jsonld.expand].concat(slice.call(arguments)));
  };
  api.compact = function(input, ctx) {
    if(arguments.length < 2) {
      throw new TypeError('Could not compact, too few arguments.');
    }
    var compact = function(input, ctx, options, callback) {
      // ensure only one value is returned in callback
      jsonld.compact(input, ctx, options, function(err, compacted) {
        callback(err, compacted);
      });
    };
    return promisify.apply(null, [compact].concat(slice.call(arguments)));
  };
  api.flatten = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not flatten, too few arguments.');
    }
    return promisify.apply(
      null, [jsonld.flatten].concat(slice.call(arguments)));
  };
  api.frame = function(input, frame) {
    if(arguments.length < 2) {
      throw new TypeError('Could not frame, too few arguments.');
    }
    return promisify.apply(null, [jsonld.frame].concat(slice.call(arguments)));
  };
  api.fromRDF = function(dataset) {
    if(arguments.length < 1) {
      throw new TypeError('Could not convert from RDF, too few arguments.');
    }
    return promisify.apply(
      null, [jsonld.fromRDF].concat(slice.call(arguments)));
  };
  api.toRDF = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not convert to RDF, too few arguments.');
    }
    return promisify.apply(null, [jsonld.toRDF].concat(slice.call(arguments)));
  };
  api.normalize = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not normalize, too few arguments.');
    }
    return promisify.apply(
      null, [jsonld.normalize].concat(slice.call(arguments)));
  };

  if(version === 'jsonld.js') {
    api.link = function(input, ctx) {
      if(arguments.length < 2) {
        throw new TypeError('Could not link, too few arguments.');
      }
      return promisify.apply(
        null, [jsonld.link].concat(slice.call(arguments)));
    };
    api.objectify = function(input) {
      return promisify.apply(
        null, [jsonld.objectify].concat(slice.call(arguments)));
    };
    api.createNodeMap = function(input) {
      return promisify.apply(
        null, [jsonld.createNodeMap].concat(slice.call(arguments)));
    };
    api.merge = function(input) {
      return promisify.apply(
        null, [jsonld.merge].concat(slice.call(arguments)));
    };
  }

  try {
    jsonld.Promise = global.Promise || require('es6-promise').Promise;
  } catch(e) {
    var f = function() {
      throw new Error('Unable to find a Promise implementation.');
    };
    for(var method in api) {
      api[method] = f;
    }
  }

  return api;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promisify"></a>[function <span class="apidocSignatureSpan">jsonld.</span>promisify (op)](#apidoc.element.jsonld.promisify)
- description and source-code
```javascript
promisify = function (op) {
  if(!jsonld.Promise) {
    try {
      jsonld.Promise = global.Promise || require('es6-promise').Promise;
    } catch(e) {
      throw new Error('Unable to find a Promise implementation.');
    }
  }
  var args = Array.prototype.slice.call(arguments, 1);
  return new jsonld.Promise(function(resolve, reject) {
    op.apply(null, args.concat(function(err, value) {
      if(!err) {
        resolve(value);
      } else {
        reject(err);
      }
    }));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.registerRDFParser"></a>[function <span class="apidocSignatureSpan">jsonld.</span>registerRDFParser (contentType, parser)](#apidoc.element.jsonld.registerRDFParser)
- description and source-code
```javascript
registerRDFParser = function (contentType, parser) {
  _rdfParsers[contentType] = parser;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.relabelBlankNodes"></a>[function <span class="apidocSignatureSpan">jsonld.</span>relabelBlankNodes (input, options)](#apidoc.element.jsonld.relabelBlankNodes)
- description and source-code
```javascript
relabelBlankNodes = function (input, options) {
  options = options || {};
  var issuer = options.namer || options.issuer || new IdentifierIssuer('_:b');
  return _labelBlankNodes(issuer, input);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.removeProperty"></a>[function <span class="apidocSignatureSpan">jsonld.</span>removeProperty (subject, property)](#apidoc.element.jsonld.removeProperty)
- description and source-code
```javascript
removeProperty = function (subject, property) {
  delete subject[property];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.removeValue"></a>[function <span class="apidocSignatureSpan">jsonld.</span>removeValue (subject, property, value, options)](#apidoc.element.jsonld.removeValue)
- description and source-code
```javascript
removeValue = function (subject, property, value, options) {
  options = options || {};
  if(!('propertyIsArray' in options)) {
    options.propertyIsArray = false;
  }

  // filter out value
  var values = jsonld.getValues(subject, property).filter(function(e) {
    return !jsonld.compareValues(e, value);
  });

  if(values.length === 0) {
    jsonld.removeProperty(subject, property);
  } else if(values.length === 1 && !options.propertyIsArray) {
    subject[property] = values[0];
  } else {
    subject[property] = values;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.setImmediate"></a>[function <span class="apidocSignatureSpan">jsonld.</span>setImmediate (fn)](#apidoc.element.jsonld.setImmediate)
- description and source-code
```javascript
setImmediate = function (fn) {
  // not a direct alias (for IE10 compatibility)
  _setImmediate(fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.toRDF"></a>[function <span class="apidocSignatureSpan">jsonld.</span>toRDF (input, options, callback)](#apidoc.element.jsonld.toRDF)
- description and source-code
```javascript
toRDF = function (input, options, callback) {
  if(arguments.length < 1) {
    return jsonld.nextTick(function() {
      callback(new TypeError('Could not convert to RDF, too few arguments.'));
    });
  }

  // get arguments
  if(typeof options === 'function') {
    callback = options;
    options = {};
  }
  options = options || {};

  // set default options
  if(!('base' in options)) {
    options.base = (typeof input === 'string') ? input : '';
  }
  if(!('documentLoader' in options)) {
    options.documentLoader = jsonld.loadDocument;
  }

  // expand input
  jsonld.expand(input, options, function(err, expanded) {
    if(err) {
      return callback(new JsonLdError(
        'Could not expand input before serialization to RDF.',
        'jsonld.RdfError', {cause: err}));
    }

    var dataset;
    try {
      // output RDF dataset
      dataset = Processor.prototype.toRDF(expanded, options);
      if(options.format) {
        if(options.format === 'application/nquads') {
          return callback(null, _toNQuads(dataset));
        }
        throw new JsonLdError(
          'Unknown output format.',
          'jsonld.UnknownFormat', {format: options.format});
      }
    } catch(ex) {
      return callback(ex);
    }
    callback(null, dataset);
  });
}
```
- example usage
```shell
...
  format: 'application/nquads'
}, function(err, normalized) {
  // normalized is a string that is a canonical representation of the document
  // that can be used for hashing, comparison, etc.
});

// serialize a document to N-Quads (RDF)
jsonld.toRDF(doc, {format: 'application/nquads'}, function(err, nquads) {
  // nquads is a string of nquads
});

// deserialize N-Quads (RDF) to JSON-LD
jsonld.fromRDF(nquads, {format: 'application/nquads'}, function(err, doc) {
  // doc is JSON-LD
});
...
```

#### <a name="apidoc.element.jsonld.unregisterRDFParser"></a>[function <span class="apidocSignatureSpan">jsonld.</span>unregisterRDFParser (contentType)](#apidoc.element.jsonld.unregisterRDFParser)
- description and source-code
```javascript
unregisterRDFParser = function (contentType) {
  delete _rdfParsers[contentType];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.use"></a>[function <span class="apidocSignatureSpan">jsonld.</span>use (extension)](#apidoc.element.jsonld.use)
- description and source-code
```javascript
use = function (extension) {
  switch(extension) {
    // TODO: Deprecated as of 0.4.0. Remove at some point.
    case 'request':
      // use node JSON-LD request extension
      jsonld.request = require('jsonld-request');
      break;
    default:
      throw new JsonLdError(
        'Unknown extension.',
        'jsonld.UnknownExtension', {extension: extension});
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.useDocumentLoader"></a>[function <span class="apidocSignatureSpan">jsonld.</span>useDocumentLoader (type)](#apidoc.element.jsonld.useDocumentLoader)
- description and source-code
```javascript
useDocumentLoader = function (type) {
  if(!(type in jsonld.documentLoaders)) {
    throw new JsonLdError(
      'Unknown document loader type: "' + type + '"',
      'jsonld.UnknownDocumentLoader',
      {type: type});
  }

  // set document loader
  jsonld.documentLoader = jsonld.documentLoaders[type].apply(
    jsonld, Array.prototype.slice.call(arguments, 1));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.ActiveContextCache"></a>[module jsonld.ActiveContextCache](#apidoc.module.jsonld.ActiveContextCache)

#### <a name="apidoc.element.jsonld.ActiveContextCache.ActiveContextCache"></a>[function <span class="apidocSignatureSpan">jsonld.</span>ActiveContextCache (size)](#apidoc.element.jsonld.ActiveContextCache.ActiveContextCache)
- description and source-code
```javascript
ActiveContextCache = function (size) {
  this.order = [];
  this.cache = {};
  this.size = size || 100;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.ActiveContextCache.prototype"></a>[module jsonld.ActiveContextCache.prototype](#apidoc.module.jsonld.ActiveContextCache.prototype)

#### <a name="apidoc.element.jsonld.ActiveContextCache.prototype.get"></a>[function <span class="apidocSignatureSpan">jsonld.ActiveContextCache.prototype.</span>get (activeCtx, localCtx)](#apidoc.element.jsonld.ActiveContextCache.prototype.get)
- description and source-code
```javascript
get = function (activeCtx, localCtx) {
  var key1 = JSON.stringify(activeCtx);
  var key2 = JSON.stringify(localCtx);
  var level1 = this.cache[key1];
  if(level1 && key2 in level1) {
    return level1[key2];
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.ActiveContextCache.prototype.set"></a>[function <span class="apidocSignatureSpan">jsonld.ActiveContextCache.prototype.</span>set ( activeCtx, localCtx, result)](#apidoc.element.jsonld.ActiveContextCache.prototype.set)
- description and source-code
```javascript
set = function ( activeCtx, localCtx, result) {
  if(this.order.length === this.size) {
    var entry = this.order.shift();
    delete this.cache[entry.activeCtx][entry.localCtx];
  }
  var key1 = JSON.stringify(activeCtx);
  var key2 = JSON.stringify(localCtx);
  this.order.push({activeCtx: key1, localCtx: key2});
  if(!(key1 in this.cache)) {
    this.cache[key1] = {};
  }
  this.cache[key1][key2] = _clone(result);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.DocumentCache"></a>[module jsonld.DocumentCache](#apidoc.module.jsonld.DocumentCache)

#### <a name="apidoc.element.jsonld.DocumentCache.DocumentCache"></a>[function <span class="apidocSignatureSpan">jsonld.</span>DocumentCache (size)](#apidoc.element.jsonld.DocumentCache.DocumentCache)
- description and source-code
```javascript
DocumentCache = function (size) {
  this.order = [];
  this.cache = {};
  this.size = size || 50;
  this.expires = 30 * 1000;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.DocumentCache.prototype"></a>[module jsonld.DocumentCache.prototype](#apidoc.module.jsonld.DocumentCache.prototype)

#### <a name="apidoc.element.jsonld.DocumentCache.prototype.get"></a>[function <span class="apidocSignatureSpan">jsonld.DocumentCache.prototype.</span>get (url)](#apidoc.element.jsonld.DocumentCache.prototype.get)
- description and source-code
```javascript
get = function (url) {
  if(url in this.cache) {
    var entry = this.cache[url];
    if(entry.expires >= +new Date()) {
      return entry.ctx;
    }
    delete this.cache[url];
    this.order.splice(this.order.indexOf(url), 1);
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.DocumentCache.prototype.set"></a>[function <span class="apidocSignatureSpan">jsonld.DocumentCache.prototype.</span>set (url, ctx)](#apidoc.element.jsonld.DocumentCache.prototype.set)
- description and source-code
```javascript
set = function (url, ctx) {
  if(this.order.length === this.size) {
    delete this.cache[this.order.shift()];
  }
  this.order.push(url);
  this.cache[url] = {ctx: ctx, expires: (+new Date() + this.expires)};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.IdentifierIssuer"></a>[module jsonld.IdentifierIssuer](#apidoc.module.jsonld.IdentifierIssuer)

#### <a name="apidoc.element.jsonld.IdentifierIssuer.IdentifierIssuer"></a>[function <span class="apidocSignatureSpan">jsonld.</span>IdentifierIssuer (prefix)](#apidoc.element.jsonld.IdentifierIssuer.IdentifierIssuer)
- description and source-code
```javascript
function IdentifierIssuer(prefix) {
  this.prefix = prefix;
  this.counter = 0;
  this.existing = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.IdentifierIssuer.prototype"></a>[module jsonld.IdentifierIssuer.prototype](#apidoc.module.jsonld.IdentifierIssuer.prototype)

#### <a name="apidoc.element.jsonld.IdentifierIssuer.prototype.clone"></a>[function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>clone ()](#apidoc.element.jsonld.IdentifierIssuer.prototype.clone)
- description and source-code
```javascript
clone = function () {
  var copy = new IdentifierIssuer(this.prefix);
  copy.counter = this.counter;
  copy.existing = _clone(this.existing);
  return copy;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.IdentifierIssuer.prototype.getId"></a>[function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>getId (old)](#apidoc.element.jsonld.IdentifierIssuer.prototype.getId)
- description and source-code
```javascript
getId = function (old) {
  // return existing old identifier
  if(old && old in this.existing) {
    return this.existing[old];
  }

  // get next identifier
  var identifier = this.prefix + this.counter;
  this.counter += 1;

  // save mapping
  if(old) {
    this.existing[old] = identifier;
  }

  return identifier;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.IdentifierIssuer.prototype.hasId"></a>[function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>hasId (old)](#apidoc.element.jsonld.IdentifierIssuer.prototype.hasId)
- description and source-code
```javascript
hasId = function (old) {
  return (old in this.existing);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.IdentifierIssuer.prototype.isNamed"></a>[function <span class="apidocSignatureSpan">jsonld.IdentifierIssuer.prototype.</span>isNamed (old)](#apidoc.element.jsonld.IdentifierIssuer.prototype.isNamed)
- description and source-code
```javascript
isNamed = function (old) {
  return (old in this.existing);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.JsonLdProcessor"></a>[module jsonld.JsonLdProcessor](#apidoc.module.jsonld.JsonLdProcessor)

#### <a name="apidoc.element.jsonld.JsonLdProcessor.JsonLdProcessor"></a>[function <span class="apidocSignatureSpan">jsonld.</span>JsonLdProcessor ()](#apidoc.element.jsonld.JsonLdProcessor.JsonLdProcessor)
- description and source-code
```javascript
function JsonLdProcessor() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.JsonLdProcessor.prototype"></a>[module jsonld.JsonLdProcessor.prototype](#apidoc.module.jsonld.JsonLdProcessor.prototype)

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.compact"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>compact (input, ctx)](#apidoc.element.jsonld.JsonLdProcessor.prototype.compact)
- description and source-code
```javascript
compact = function (input, ctx) {
  if(arguments.length < 2) {
    throw new TypeError('Could not compact, too few arguments.');
  }
  var compact = function(input, ctx, options, callback) {
    // ensure only one value is returned in callback
    jsonld.compact(input, ctx, options, function(err, compacted) {
      callback(err, compacted);
    });
  };
  return promisify.apply(null, [compact].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
"name": "http://schema.org/name",
"homepage": {"@id": "http://schema.org/url", "@type": "@id"},
"image": {"@id": "http://schema.org/image", "@type": "@id"}
};

// compact a document according to a particular context
// see: http://json-ld.org/spec/latest/json-ld/#compacted-document-form
jsonld.compact(doc, context, function(err, compacted) {
console.log(JSON.stringify(compacted, null, 2));
/* Output:
{
  "@context": {...},
  "name": "Manu Sporny",
  "homepage": "http://manu.sporny.org/",
  "image": "http://manu.sporny.org/images/manu.png"
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.expand"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>expand (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.expand)
- description and source-code
```javascript
expand = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not expand, too few arguments.');
  }
  return promisify.apply(null, [jsonld.expand].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
});

// compact using URLs
jsonld.compact('http://example.org/doc', 'http://example.org/context', ...);

// expand a document, removing its context
// see: http://json-ld.org/spec/latest/json-ld/#expanded-document-form
jsonld.expand(compacted, function(err, expanded) {
/* Output:
{
  "http://schema.org/name": [{"@value": "Manu Sporny"}],
  "http://schema.org/url": [{"@id": "http://manu.sporny.org/"}],
  "http://schema.org/image": [{"@id": "http://manu.sporny.org/images/manu.png"}]
}
*/
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.flatten"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>flatten (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.flatten)
- description and source-code
```javascript
flatten = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not flatten, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.flatten].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
});

// expand using URLs
jsonld.expand('http://example.org/doc', ...);

// flatten a document
// see: http://json-ld.org/spec/latest/json-ld/#flattened-document-form
jsonld.flatten(doc, function(err, flattened) {
// all deep-level trees flattened to the top-level
});

// frame a document
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
// document transformed into a particular tree structure per the given frame
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.frame"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>frame (input, frame)](#apidoc.element.jsonld.JsonLdProcessor.prototype.frame)
- description and source-code
```javascript
frame = function (input, frame) {
  if(arguments.length < 2) {
    throw new TypeError('Could not frame, too few arguments.');
  }
  return promisify.apply(null, [jsonld.frame].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
// see: http://json-ld.org/spec/latest/json-ld/#flattened-document-form
jsonld.flatten(doc, function(err, flattened) {
// all deep-level trees flattened to the top-level
});

// frame a document
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
// document transformed into a particular tree structure per the given frame
});

// normalize a document using the RDF Dataset Normalization Algorithm
// (URDNA2015), see: http://json-ld.github.io/normalization/spec/
jsonld.normalize(doc, {
algorithm: 'URDNA2015',
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.fromRDF"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>fromRDF (dataset)](#apidoc.element.jsonld.JsonLdProcessor.prototype.fromRDF)
- description and source-code
```javascript
fromRDF = function (dataset) {
  if(arguments.length < 1) {
    throw new TypeError('Could not convert from RDF, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.fromRDF].concat(slice.call(arguments)));
}
```
- example usage
```shell
...

// serialize a document to N-Quads (RDF)
jsonld.toRDF(doc, {format: 'application/nquads'}, function(err, nquads) {
// nquads is a string of nquads
});

// deserialize N-Quads (RDF) to JSON-LD
jsonld.fromRDF(nquads, {format: 'application/nquads'}, function(err, doc) {
// doc is JSON-LD
});

// register a custom async-callback-based RDF parser
jsonld.registerRDFParser = function(contentType, function(input, callback) {
// parse input to a jsonld.js RDF dataset object...
callback(err, dataset);
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.normalize"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>normalize (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.normalize)
- description and source-code
```javascript
normalize = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not normalize, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.normalize].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
  // document transformed into a particular tree structure per the given frame
});

// normalize a document using the RDF Dataset Normalization Algorithm
// (URDNA2015), see: http://json-ld.github.io/normalization/spec/
jsonld.normalize(doc, {
  algorithm: 'URDNA2015',
  format: 'application/nquads'
}, function(err, normalized) {
  // normalized is a string that is a canonical representation of the document
  // that can be used for hashing, comparison, etc.
});
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.toRDF"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>toRDF (input)](#apidoc.element.jsonld.JsonLdProcessor.prototype.toRDF)
- description and source-code
```javascript
toRDF = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not convert to RDF, too few arguments.');
  }
  return promisify.apply(null, [jsonld.toRDF].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
  format: 'application/nquads'
}, function(err, normalized) {
  // normalized is a string that is a canonical representation of the document
  // that can be used for hashing, comparison, etc.
});

// serialize a document to N-Quads (RDF)
jsonld.toRDF(doc, {format: 'application/nquads'}, function(err, nquads) {
  // nquads is a string of nquads
});

// deserialize N-Quads (RDF) to JSON-LD
jsonld.fromRDF(nquads, {format: 'application/nquads'}, function(err, doc) {
  // doc is JSON-LD
});
...
```

#### <a name="apidoc.element.jsonld.JsonLdProcessor.prototype.toString"></a>[function <span class="apidocSignatureSpan">jsonld.JsonLdProcessor.prototype.</span>toString ()](#apidoc.element.jsonld.JsonLdProcessor.prototype.toString)
- description and source-code
```javascript
toString = function () {
  if(this instanceof JsonLdProcessor) {
    return '[object JsonLdProcessor]';
  }
  return '[object JsonLdProcessorPrototype]';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.RequestQueue"></a>[module jsonld.RequestQueue](#apidoc.module.jsonld.RequestQueue)

#### <a name="apidoc.element.jsonld.RequestQueue.RequestQueue"></a>[function <span class="apidocSignatureSpan">jsonld.</span>RequestQueue ()](#apidoc.element.jsonld.RequestQueue.RequestQueue)
- description and source-code
```javascript
RequestQueue = function () {
  this._requests = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.RequestQueue.prototype"></a>[module jsonld.RequestQueue.prototype](#apidoc.module.jsonld.RequestQueue.prototype)

#### <a name="apidoc.element.jsonld.RequestQueue.prototype.add"></a>[function <span class="apidocSignatureSpan">jsonld.RequestQueue.prototype.</span>add (url, callback)](#apidoc.element.jsonld.RequestQueue.prototype.add)
- description and source-code
```javascript
add = function (url, callback) {
  var self = this;

  // callback must be given if not using promises
  if(!callback && !self._usePromise) {
    throw new Error('callback must be specified.');
  }

  // Promise-based API
  if(self._usePromise) {
    return new jsonld.Promise(function(resolve, reject) {
      var load = self._requests[url];
      if(!load) {
        // load URL then remove from queue
        load = self._requests[url] = self._loader(url)
          .then(function(remoteDoc) {
            delete self._requests[url];
            return remoteDoc;
          }).catch(function(err) {
            delete self._requests[url];
            throw err;
          });
      }
      // resolve/reject promise once URL has been loaded
      load.then(function(remoteDoc) {
        resolve(remoteDoc);
      }).catch(function(err) {
        reject(err);
      });
    });
  }

  // callback-based API
  if(url in self._requests) {
    self._requests[url].push(callback);
  } else {
    self._requests[url] = [callback];
    self._loader(url, function(err, remoteDoc) {
      var callbacks = self._requests[url];
      delete self._requests[url];
      for(var i = 0; i < callbacks.length; ++i) {
        callbacks[i](err, remoteDoc);
      }
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.RequestQueue.prototype.wrapLoader"></a>[function <span class="apidocSignatureSpan">jsonld.RequestQueue.prototype.</span>wrapLoader (loader)](#apidoc.element.jsonld.RequestQueue.prototype.wrapLoader)
- description and source-code
```javascript
wrapLoader = function (loader) {
  this._loader = loader;
  this._usePromise = (loader.length === 1);
  return this.add.bind(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsonld.documentLoaders"></a>[module jsonld.documentLoaders](#apidoc.module.jsonld.documentLoaders)

#### <a name="apidoc.element.jsonld.documentLoaders.jquery"></a>[function <span class="apidocSignatureSpan">jsonld.documentLoaders.</span>jquery ($, options)](#apidoc.element.jsonld.documentLoaders.jquery)
- description and source-code
```javascript
jquery = function ($, options) {
  options = options || {};
  var queue = new jsonld.RequestQueue();

  // use option or, by default, use Promise when its defined
  var usePromise = ('usePromise' in options ?
    options.usePromise : (typeof Promise !== 'undefined'));
  if(usePromise) {
    return queue.wrapLoader(function(url) {
      return jsonld.promisify(loader, url);
    });
  }
  return queue.wrapLoader(loader);

  function loader(url, callback) {
    if(url.indexOf('http:') !== 0 && url.indexOf('https:') !== 0) {
      return callback(new JsonLdError(
        'URL could not be dereferenced; only "http" and "https" URLs are ' +
        'supported.',
        'jsonld.InvalidUrl', {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    }
    if(options.secure && url.indexOf('https') !== 0) {
      return callback(new JsonLdError(
        'URL could not be dereferenced; secure mode is enabled and ' +
        'the URL\'s scheme is not "https".',
        'jsonld.InvalidUrl', {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    }
    $.ajax({
      url: url,
      accepts: {
        json: 'application/ld+json, application/json'
      },
      // ensure Accept header is very specific for JSON-LD/JSON
      headers: {
        'Accept': 'application/ld+json, application/json'
      },
      dataType: 'json',
      crossDomain: true,
      success: function(data, textStatus, jqXHR) {
        var doc = {contextUrl: null, documentUrl: url, document: data};

        // handle Link Header
        var contentType = jqXHR.getResponseHeader('Content-Type');
        var linkHeader = jqXHR.getResponseHeader('Link');
        if(linkHeader && contentType !== 'application/ld+json') {
          // only 1 related link header permitted
          linkHeader = jsonld.parseLinkHeader(linkHeader)[LINK_HEADER_REL];
          if(_isArray(linkHeader)) {
            return callback(new JsonLdError(
              'URL could not be dereferenced, it has more than one ' +
              'associated HTTP Link Header.',
              'jsonld.InvalidUrl',
              {code: 'multiple context link headers', url: url}), doc);
          }
          if(linkHeader) {
            doc.contextUrl = linkHeader.target;
          }
        }

        callback(null, doc);
      },
      error: function(jqXHR, textStatus, err) {
        callback(new JsonLdError(
          'URL could not be dereferenced, an error occurred.',
          'jsonld.LoadDocumentError',
          {code: 'loading document failed', url: url, cause: err}),
          {contextUrl: null, documentUrl: url, document: null});
      }
    });
  }
}
```
- example usage
```shell
...
  "@context": ...
}, ...
};

// grab the built-in node.js doc loader
var nodeDocumentLoader = jsonld.documentLoaders.node();
// or grab the XHR one: jsonld.documentLoaders.xhr()
// or grab the jquery one: jsonld.documentLoaders.jquery()

// change the default document loader using the callback API
// (you can also do this using the promise-based API, return a promise instead
// of using a callback)
var customLoader = function(url, callback) {
if(url in CONTEXTS) {
  return callback(
...
```

#### <a name="apidoc.element.jsonld.documentLoaders.node"></a>[function <span class="apidocSignatureSpan">jsonld.documentLoaders.</span>node (options)](#apidoc.element.jsonld.documentLoaders.node)
- description and source-code
```javascript
node = function (options) {
  options = options || {};
  var strictSSL = ('strictSSL' in options) ? options.strictSSL : true;
  var maxRedirects = ('maxRedirects' in options) ? options.maxRedirects : -1;
  var request = ('request' in options) ? options.request : require('request');
  var acceptHeader = 'application/ld+json, application/json';
  var http = require('http');
  // TODO: disable cache until HTTP caching implemented
  //var cache = new jsonld.DocumentCache();

  var queue = new jsonld.RequestQueue();
  if(options.usePromise) {
    return queue.wrapLoader(function(url) {
      return jsonld.promisify(loadDocument, url, []);
    });
  }
  var headers = options.headers || {};
  if('Accept' in headers || 'accept' in headers) {
    throw new RangeError(
      'Accept header may not be specified as an option; only "' +
      acceptHeader + '" is supported.');
  }
  return queue.wrapLoader(function(url, callback) {
    loadDocument(url, [], callback);
  });

  function loadDocument(url, redirects, callback) {
    if(url.indexOf('http:') !== 0 && url.indexOf('https:') !== 0) {
      return callback(new JsonLdError(
        'URL could not be dereferenced; only "http" and "https" URLs are ' +
        'supported.',
        'jsonld.InvalidUrl', {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    }
    if(options.secure && url.indexOf('https') !== 0) {
      return callback(new JsonLdError(
        'URL could not be dereferenced; secure mode is enabled and ' +
        'the URL\'s scheme is not "https".',
        'jsonld.InvalidUrl', {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    }
    // TODO: disable cache until HTTP caching implemented
    var doc = null;//cache.get(url);
    if(doc !== null) {
      return callback(null, doc);
    }
    var headers = {'Accept': acceptHeader};
    for(var k in options.headers) { headers[k] = options.headers[k]; }
    request({
      url: url,
      headers: headers,
      strictSSL: strictSSL,
      followRedirect: false
    }, handleResponse);

    function handleResponse(err, res, body) {
      doc = {contextUrl: null, documentUrl: url, document: body || null};

      // handle error
      if(err) {
        return callback(new JsonLdError(
          'URL could not be dereferenced, an error occurred.',
          'jsonld.LoadDocumentError',
          {code: 'loading document failed', url: url, cause: err}), doc);
      }
      var statusText = http.STATUS_CODES[res.statusCode];
      if(res.statusCode >= 400) {
        return callback(new JsonLdError(
          'URL could not be dereferenced: ' + statusText,
          'jsonld.InvalidUrl', {
            code: 'loading document failed',
            url: url,
            httpStatusCode: res.statusCode
          }), doc);
      }

      // handle Link Header
      if(res.headers.link &&
        res.headers['content-type'] !== 'application/ld+json') {
        // only 1 related link header permitted
        var linkHeader = jsonld.parseLinkHeader(
          res.headers.link)[LINK_HEADER_REL];
        if(_isArray(linkHeader)) {
          return callback(new JsonLdError(
            'URL could not be dereferenced, it has more than one associated ' +
            'HTTP Link Header.',
            'jsonld.InvalidUrl',
            {code: 'multiple context link headers', url: url}), doc);
        }
        if(linkHeader) {
          doc.contextUrl = linkHeader.target;
        }
      }

      // handle redirect
      if(res.statusCode >= 300 && res.statusCode < 400 &&
        res.headers.location) {
        if(redirects.length === maxRedirects) {
          return callback(new JsonLdError(
            'URL could not be dereferenced; there were too many redirects.',
            'jsonld.TooManyRedirects', {
              code: 'loading document failed',
              url: url,
              httpStatusCode: res.statusCode,
              redirects: redirects
            }), doc);
        }
        if(redirects.indexOf(url) !== -1) { ...
```
- example usage
```shell
...
var CONTEXTS = {
  "http://example.com": {
    "@context": ...
  }, ...
};

// grab the built-in node.js doc loader
var nodeDocumentLoader = jsonld.documentLoaders.node();
// or grab the XHR one: jsonld.documentLoaders.xhr()
// or grab the jquery one: jsonld.documentLoaders.jquery()

// change the default document loader using the callback API
// (you can also do this using the promise-based API, return a promise instead
// of using a callback)
var customLoader = function(url, callback) {
...
```

#### <a name="apidoc.element.jsonld.documentLoaders.xhr"></a>[function <span class="apidocSignatureSpan">jsonld.documentLoaders.</span>xhr (options)](#apidoc.element.jsonld.documentLoaders.xhr)
- description and source-code
```javascript
xhr = function (options) {
  options = options || {};
  var rlink = /(^|(\r\n))link:/i;
  var queue = new jsonld.RequestQueue();

  // use option or, by default, use Promise when its defined
  var usePromise = ('usePromise' in options ?
    options.usePromise : (typeof Promise !== 'undefined'));
  if(usePromise) {
    return queue.wrapLoader(function(url) {
      return jsonld.promisify(loader, url);
    });
  }
  return queue.wrapLoader(loader);

  function loader(url, callback) {
    if(url.indexOf('http:') !== 0 && url.indexOf('https:') !== 0) {
      return callback(new JsonLdError(
        'URL could not be dereferenced; only "http" and "https" URLs are ' +
        'supported.',
        'jsonld.InvalidUrl', {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    }
    if(options.secure && url.indexOf('https') !== 0) {
      return callback(new JsonLdError(
        'URL could not be dereferenced; secure mode is enabled and ' +
        'the URL\'s scheme is not "https".',
        'jsonld.InvalidUrl', {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    }
    var xhr = options.xhr || XMLHttpRequest;
    var req = new xhr();
    req.onload = function() {
      if(req.status >= 400) {
        return callback(new JsonLdError(
          'URL could not be dereferenced: ' + req.statusText,
          'jsonld.LoadDocumentError', {
            code: 'loading document failed',
            url: url,
            httpStatusCode: req.status
          }), {contextUrl: null, documentUrl: url, document: null});
      }

      var doc = {contextUrl: null, documentUrl: url, document: req.response};

      // handle Link Header (avoid unsafe header warning by existence testing)
      var contentType = req.getResponseHeader('Content-Type');
      var linkHeader;
      if(rlink.test(req.getAllResponseHeaders())) {
        linkHeader = req.getResponseHeader('Link');
      }
      if(linkHeader && contentType !== 'application/ld+json') {
        // only 1 related link header permitted
        linkHeader = jsonld.parseLinkHeader(linkHeader)[LINK_HEADER_REL];
        if(_isArray(linkHeader)) {
          return callback(new JsonLdError(
            'URL could not be dereferenced, it has more than one ' +
            'associated HTTP Link Header.',
            'jsonld.InvalidUrl',
            {code: 'multiple context link headers', url: url}), doc);
        }
        if(linkHeader) {
          doc.contextUrl = linkHeader.target;
        }
      }

      callback(null, doc);
    };
    req.onerror = function() {
      callback(new JsonLdError(
        'URL could not be dereferenced, an error occurred.',
        'jsonld.LoadDocumentError',
        {code: 'loading document failed', url: url}),
        {contextUrl: null, documentUrl: url, document: null});
    };
    req.open('GET', url, true);
    req.setRequestHeader('Accept', 'application/ld+json, application/json');
    req.send();
  }
}
```
- example usage
```shell
...
"http://example.com": {
  "@context": ...
}, ...
};

// grab the built-in node.js doc loader
var nodeDocumentLoader = jsonld.documentLoaders.node();
// or grab the XHR one: jsonld.documentLoaders.xhr()
// or grab the jquery one: jsonld.documentLoaders.jquery()

// change the default document loader using the callback API
// (you can also do this using the promise-based API, return a promise instead
// of using a callback)
var customLoader = function(url, callback) {
if(url in CONTEXTS) {
...
```



# <a name="apidoc.module.jsonld.promises"></a>[module jsonld.promises](#apidoc.module.jsonld.promises)

#### <a name="apidoc.element.jsonld.promises.promises"></a>[function <span class="apidocSignatureSpan">jsonld.</span>promises (options)](#apidoc.element.jsonld.promises.promises)
- description and source-code
```javascript
promises = function (options) {
  options = options || {};
  var slice = Array.prototype.slice;
  var promisify = jsonld.promisify;

  // handle 'api' option as version, set defaults
  var api = options.api || {};
  var version = options.version || 'jsonld.js';
  if(typeof options.api === 'string') {
    if(!options.version) {
      version = options.api;
    }
    api = {};
  }

  api.expand = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not expand, too few arguments.');
    }
    return promisify.apply(null, [jsonld.expand].concat(slice.call(arguments)));
  };
  api.compact = function(input, ctx) {
    if(arguments.length < 2) {
      throw new TypeError('Could not compact, too few arguments.');
    }
    var compact = function(input, ctx, options, callback) {
      // ensure only one value is returned in callback
      jsonld.compact(input, ctx, options, function(err, compacted) {
        callback(err, compacted);
      });
    };
    return promisify.apply(null, [compact].concat(slice.call(arguments)));
  };
  api.flatten = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not flatten, too few arguments.');
    }
    return promisify.apply(
      null, [jsonld.flatten].concat(slice.call(arguments)));
  };
  api.frame = function(input, frame) {
    if(arguments.length < 2) {
      throw new TypeError('Could not frame, too few arguments.');
    }
    return promisify.apply(null, [jsonld.frame].concat(slice.call(arguments)));
  };
  api.fromRDF = function(dataset) {
    if(arguments.length < 1) {
      throw new TypeError('Could not convert from RDF, too few arguments.');
    }
    return promisify.apply(
      null, [jsonld.fromRDF].concat(slice.call(arguments)));
  };
  api.toRDF = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not convert to RDF, too few arguments.');
    }
    return promisify.apply(null, [jsonld.toRDF].concat(slice.call(arguments)));
  };
  api.normalize = function(input) {
    if(arguments.length < 1) {
      throw new TypeError('Could not normalize, too few arguments.');
    }
    return promisify.apply(
      null, [jsonld.normalize].concat(slice.call(arguments)));
  };

  if(version === 'jsonld.js') {
    api.link = function(input, ctx) {
      if(arguments.length < 2) {
        throw new TypeError('Could not link, too few arguments.');
      }
      return promisify.apply(
        null, [jsonld.link].concat(slice.call(arguments)));
    };
    api.objectify = function(input) {
      return promisify.apply(
        null, [jsonld.objectify].concat(slice.call(arguments)));
    };
    api.createNodeMap = function(input) {
      return promisify.apply(
        null, [jsonld.createNodeMap].concat(slice.call(arguments)));
    };
    api.merge = function(input) {
      return promisify.apply(
        null, [jsonld.merge].concat(slice.call(arguments)));
    };
  }

  try {
    jsonld.Promise = global.Promise || require('es6-promise').Promise;
  } catch(e) {
    var f = function() {
      throw new Error('Unable to find a Promise implementation.');
    };
    for(var method in api) {
      api[method] = f;
    }
  }

  return api;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promises.compact"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>compact (input, ctx)](#apidoc.element.jsonld.promises.compact)
- description and source-code
```javascript
compact = function (input, ctx) {
  if(arguments.length < 2) {
    throw new TypeError('Could not compact, too few arguments.');
  }
  var compact = function(input, ctx, options, callback) {
    // ensure only one value is returned in callback
    jsonld.compact(input, ctx, options, function(err, compacted) {
      callback(err, compacted);
    });
  };
  return promisify.apply(null, [compact].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
"name": "http://schema.org/name",
"homepage": {"@id": "http://schema.org/url", "@type": "@id"},
"image": {"@id": "http://schema.org/image", "@type": "@id"}
};

// compact a document according to a particular context
// see: http://json-ld.org/spec/latest/json-ld/#compacted-document-form
jsonld.compact(doc, context, function(err, compacted) {
console.log(JSON.stringify(compacted, null, 2));
/* Output:
{
  "@context": {...},
  "name": "Manu Sporny",
  "homepage": "http://manu.sporny.org/",
  "image": "http://manu.sporny.org/images/manu.png"
...
```

#### <a name="apidoc.element.jsonld.promises.createNodeMap"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>createNodeMap (input)](#apidoc.element.jsonld.promises.createNodeMap)
- description and source-code
```javascript
createNodeMap = function (input) {
  return promisify.apply(
    null, [jsonld.createNodeMap].concat(slice.call(arguments)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promises.expand"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>expand (input)](#apidoc.element.jsonld.promises.expand)
- description and source-code
```javascript
expand = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not expand, too few arguments.');
  }
  return promisify.apply(null, [jsonld.expand].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
});

// compact using URLs
jsonld.compact('http://example.org/doc', 'http://example.org/context', ...);

// expand a document, removing its context
// see: http://json-ld.org/spec/latest/json-ld/#expanded-document-form
jsonld.expand(compacted, function(err, expanded) {
/* Output:
{
  "http://schema.org/name": [{"@value": "Manu Sporny"}],
  "http://schema.org/url": [{"@id": "http://manu.sporny.org/"}],
  "http://schema.org/image": [{"@id": "http://manu.sporny.org/images/manu.png"}]
}
*/
...
```

#### <a name="apidoc.element.jsonld.promises.flatten"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>flatten (input)](#apidoc.element.jsonld.promises.flatten)
- description and source-code
```javascript
flatten = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not flatten, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.flatten].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
});

// expand using URLs
jsonld.expand('http://example.org/doc', ...);

// flatten a document
// see: http://json-ld.org/spec/latest/json-ld/#flattened-document-form
jsonld.flatten(doc, function(err, flattened) {
// all deep-level trees flattened to the top-level
});

// frame a document
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
// document transformed into a particular tree structure per the given frame
...
```

#### <a name="apidoc.element.jsonld.promises.frame"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>frame (input, frame)](#apidoc.element.jsonld.promises.frame)
- description and source-code
```javascript
frame = function (input, frame) {
  if(arguments.length < 2) {
    throw new TypeError('Could not frame, too few arguments.');
  }
  return promisify.apply(null, [jsonld.frame].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
// see: http://json-ld.org/spec/latest/json-ld/#flattened-document-form
jsonld.flatten(doc, function(err, flattened) {
// all deep-level trees flattened to the top-level
});

// frame a document
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
// document transformed into a particular tree structure per the given frame
});

// normalize a document using the RDF Dataset Normalization Algorithm
// (URDNA2015), see: http://json-ld.github.io/normalization/spec/
jsonld.normalize(doc, {
algorithm: 'URDNA2015',
...
```

#### <a name="apidoc.element.jsonld.promises.fromRDF"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>fromRDF (dataset)](#apidoc.element.jsonld.promises.fromRDF)
- description and source-code
```javascript
fromRDF = function (dataset) {
  if(arguments.length < 1) {
    throw new TypeError('Could not convert from RDF, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.fromRDF].concat(slice.call(arguments)));
}
```
- example usage
```shell
...

// serialize a document to N-Quads (RDF)
jsonld.toRDF(doc, {format: 'application/nquads'}, function(err, nquads) {
// nquads is a string of nquads
});

// deserialize N-Quads (RDF) to JSON-LD
jsonld.fromRDF(nquads, {format: 'application/nquads'}, function(err, doc) {
// doc is JSON-LD
});

// register a custom async-callback-based RDF parser
jsonld.registerRDFParser = function(contentType, function(input, callback) {
// parse input to a jsonld.js RDF dataset object...
callback(err, dataset);
...
```

#### <a name="apidoc.element.jsonld.promises.link"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>link (input, ctx)](#apidoc.element.jsonld.promises.link)
- description and source-code
```javascript
link = function (input, ctx) {
  if(arguments.length < 2) {
    throw new TypeError('Could not link, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.link].concat(slice.call(arguments)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promises.merge"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>merge (input)](#apidoc.element.jsonld.promises.merge)
- description and source-code
```javascript
merge = function (input) {
  return promisify.apply(
    null, [jsonld.merge].concat(slice.call(arguments)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promises.normalize"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>normalize (input)](#apidoc.element.jsonld.promises.normalize)
- description and source-code
```javascript
normalize = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not normalize, too few arguments.');
  }
  return promisify.apply(
    null, [jsonld.normalize].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
// see: http://json-ld.org/spec/latest/json-ld-framing/#introduction
jsonld.frame(doc, frame, function(err, framed) {
  // document transformed into a particular tree structure per the given frame
});

// normalize a document using the RDF Dataset Normalization Algorithm
// (URDNA2015), see: http://json-ld.github.io/normalization/spec/
jsonld.normalize(doc, {
  algorithm: 'URDNA2015',
  format: 'application/nquads'
}, function(err, normalized) {
  // normalized is a string that is a canonical representation of the document
  // that can be used for hashing, comparison, etc.
});
...
```

#### <a name="apidoc.element.jsonld.promises.objectify"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>objectify (input)](#apidoc.element.jsonld.promises.objectify)
- description and source-code
```javascript
objectify = function (input) {
  return promisify.apply(
    null, [jsonld.objectify].concat(slice.call(arguments)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsonld.promises.toRDF"></a>[function <span class="apidocSignatureSpan">jsonld.promises.</span>toRDF (input)](#apidoc.element.jsonld.promises.toRDF)
- description and source-code
```javascript
toRDF = function (input) {
  if(arguments.length < 1) {
    throw new TypeError('Could not convert to RDF, too few arguments.');
  }
  return promisify.apply(null, [jsonld.toRDF].concat(slice.call(arguments)));
}
```
- example usage
```shell
...
  format: 'application/nquads'
}, function(err, normalized) {
  // normalized is a string that is a canonical representation of the document
  // that can be used for hashing, comparison, etc.
});

// serialize a document to N-Quads (RDF)
jsonld.toRDF(doc, {format: 'application/nquads'}, function(err, nquads) {
  // nquads is a string of nquads
});

// deserialize N-Quads (RDF) to JSON-LD
jsonld.fromRDF(nquads, {format: 'application/nquads'}, function(err, doc) {
  // doc is JSON-LD
});
...
```



# <a name="apidoc.module.jsonld.url"></a>[module jsonld.url](#apidoc.module.jsonld.url)

#### <a name="apidoc.element.jsonld.url.parse"></a>[function <span class="apidocSignatureSpan">jsonld.url.</span>parse (str, parser)](#apidoc.element.jsonld.url.parse)
- description and source-code
```javascript
parse = function (str, parser) {
  var parsed = {};
  var o = jsonld.url.parsers[parser || 'full'];
  var m = o.regex.exec(str);
  var i = o.keys.length;
  while(i--) {
    parsed[o.keys[i]] = (m[i] === undefined) ? null : m[i];
  }
  parsed.normalizedPath = _removeDotSegments(parsed.path, !!parsed.authority);
  return parsed;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

# api documentation for  [bigrig (v1.3.0)](https://github.com/GoogleChrome/node-big-rig#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-bigrig.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bigrig) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bigrig.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bigrig)
#### A CLI and node module for parsing trace (timeline) files from Chrome.

[![NPM](https://nodei.co/npm/bigrig.png?downloads=true)](https://www.npmjs.com/package/bigrig)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bigrig/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-bigrig%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bigrig/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-bigrig/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-bigrig/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Lewis",
        "url": "Google"
    },
    "bin": {
        "bigrig": "bigrig.js"
    },
    "bugs": {
        "url": "https://github.com/GoogleChrome/node-big-rig/issues"
    },
    "dependencies": {
        "cli-color": "^1.1.0",
        "mkdirp": "^0.5.1",
        "yargs": "^3.29.0"
    },
    "description": "A CLI and node module for parsing trace (timeline) files from Chrome.",
    "devDependencies": {
        "babel-eslint": "^4.1.3",
        "chai": "^3.4.0",
        "eslint": "^1.8.0",
        "mocha": "^2.3.3"
    },
    "directories": {},
    "dist": {
        "shasum": "1f2a4822082c514659d06d7873ff4386b0d179e5",
        "tarball": "https://registry.npmjs.org/bigrig/-/bigrig-1.3.0.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "gitHead": "2c74a0411fb2fc97bbb689bdc847959c0548a639",
    "homepage": "https://github.com/GoogleChrome/node-big-rig#readme",
    "keywords": [
        "chrome",
        "trace",
        "cli"
    ],
    "license": "Apache-2.0",
    "main": "index.js",
    "maintainers": [
        {
            "name": "aerotwist",
            "email": "github@aerotwist.com"
        }
    ],
    "name": "bigrig",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/GoogleChrome/node-big-rig.git"
    },
    "scripts": {
        "test": "eslint . && mocha test/*.js --timeout 60000"
    },
    "version": "1.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module bigrig](#apidoc.module.bigrig)
1.  [function <span class="apidocSignatureSpan">bigrig.</span>analyze (traceContents, opts)](#apidoc.element.bigrig.analyze)
1.  object <span class="apidocSignatureSpan">bigrig.</span>global_config
1.  object <span class="apidocSignatureSpan">bigrig.</span>processor
1.  string <span class="apidocSignatureSpan">bigrig.</span>ANIMATION
1.  string <span class="apidocSignatureSpan">bigrig.</span>LOAD
1.  string <span class="apidocSignatureSpan">bigrig.</span>RESPONSE

#### [module bigrig.global_config](#apidoc.module.bigrig.global_config)
1.  [function <span class="apidocSignatureSpan">bigrig.global_config.</span>disable ()](#apidoc.element.bigrig.global_config.disable)
1.  [function <span class="apidocSignatureSpan">bigrig.global_config.</span>enable ()](#apidoc.element.bigrig.global_config.enable)

#### [module bigrig.processor](#apidoc.module.bigrig.processor)
1.  [function <span class="apidocSignatureSpan">bigrig.processor.</span>analyzeTrace (contents, opts)](#apidoc.element.bigrig.processor.analyzeTrace)
1.  string <span class="apidocSignatureSpan">bigrig.processor.</span>ANIMATION
1.  string <span class="apidocSignatureSpan">bigrig.processor.</span>LOAD
1.  string <span class="apidocSignatureSpan">bigrig.processor.</span>RESPONSE



# <a name="apidoc.module.bigrig"></a>[module bigrig](#apidoc.module.bigrig)

#### <a name="apidoc.element.bigrig.analyze"></a>[function <span class="apidocSignatureSpan">bigrig.</span>analyze (traceContents, opts)](#apidoc.element.bigrig.analyze)
- description and source-code
```javascript
analyze = function (traceContents, opts) {
  return processor.analyzeTrace(traceContents, opts);
}
```
- example usage
```shell
...
var fs = require('fs');

// Read trace file contents.
fs.readFile('/path/to/trace.json', 'utf8', function(err, data) {
  if (err)
    throw err;

  results = bigrig.analyze(data);

  // Now do something with the results, like
  // post to a dashboard.
});

'''
...
```



# <a name="apidoc.module.bigrig.global_config"></a>[module bigrig.global_config](#apidoc.module.bigrig.global_config)

#### <a name="apidoc.element.bigrig.global_config.disable"></a>[function <span class="apidocSignatureSpan">bigrig.global_config.</span>disable ()](#apidoc.element.bigrig.global_config.disable)
- description and source-code
```javascript
function disable() {

  delete global.Polymer.elements;
  delete global.Polymer;

  delete global.HTMLUnknownElement;
  delete global.HTMLDivElement;
  delete global.document;

  delete global.vec2;
  delete global.vec3;
  delete global.vec4;
  delete global.mat2d;
  delete global.mat4;
  delete global.window;
}
```
- example usage
```shell
...

  console.log('\nProceeding using the last named tab:' + bullet,
      summarizable[0].labels[0]);
}

traceProcess = summarizable.pop();
// Reset all the globals we had to define for window etc.
globalConfig.disable();
return processTrace(model, traceProcess, opts);
}

function convertEventsToModel (events) {

require('./third_party/tracing/importer/import.js');
require('./third_party/tracing/extras/importer/trace_event_importer.js');
...
```

#### <a name="apidoc.element.bigrig.global_config.enable"></a>[function <span class="apidocSignatureSpan">bigrig.global_config.</span>enable ()](#apidoc.element.bigrig.global_config.enable)
- description and source-code
```javascript
function enable() {
  // Sets some global options so that the trace viewer code can work.
  // It expects to be run inside of a browser, where host objects
  // (and Polymer) exist. Since they don't they need stubbing out.
  global.Polymer = function () {};
  global.Polymer.elements = {};

  global.HTMLUnknownElement = {};
  global.HTMLDivElement = {};
  global.document = {
    currentScript: {
      ownerDocument: {}
    },

    createElement: function () {
      return {
        style: {

        }
      };
    }
  };

  global.vec2 = {create: function () {}, set: function () {}};
  global.vec3 = {create: function () {}};
  global.vec4 = {create: function () {}};
  global.mat2d = {create: function () {}};
  global.mat4 = {create: function () {}};
  global.window = {
    performance: {
      now: function () {
        return Date.now();
      }
    }, webkitRequestAnimationFrame: function (cb) {
      cb();
    }, requestAnimationFrame: function (cb) {
      cb();
    }
  };
}
```
- example usage
```shell
...
}

var events = [JSON.stringify({
  traceEvents: contentsJSON
})];

// Switch on all the globals we need, and import tracing.
globalConfig.enable();

var model = convertEventsToModel(events);
var processes = model.getAllProcesses();
var traceProcess = null;
var summarizable = [];

for (var p = 0; p < processes.length; p++) {
...
```



# <a name="apidoc.module.bigrig.processor"></a>[module bigrig.processor](#apidoc.module.bigrig.processor)

#### <a name="apidoc.element.bigrig.processor.analyzeTrace"></a>[function <span class="apidocSignatureSpan">bigrig.processor.</span>analyzeTrace (contents, opts)](#apidoc.element.bigrig.processor.analyzeTrace)
- description and source-code
```javascript
function analyzeTrace(contents, opts) {

  var contentsJSON = null;

  try {
    contentsJSON = JSON.parse(contents);

    // If the file already wrapped the trace events in a
    // traceEvents object, grab the contents of the object.
    if (contentsJSON !== null &&
      typeof contentsJSON.traceEvents !== 'undefined') {
      contentsJSON = contentsJSON.traceEvents;
    }

  } catch (e) {
    throw 'Invalid trace contents; not JSON';
  }

  var events = [JSON.stringify({
    traceEvents: contentsJSON
  })];

  // Switch on all the globals we need, and import tracing.
  globalConfig.enable();

  var model = convertEventsToModel(events);
  var processes = model.getAllProcesses();
  var traceProcess = null;
  var summarizable = [];

  for (var p = 0; p < processes.length; p++) {
    var candidate = processes[p];

    if (typeof candidate.labels !== 'undefined' &&
        candidate.labels.length > 0 &&
        candidate.labels[0] !== 'chrome://tracing' &&
        candidate.labels[0] !== 'BackgroundPage') {
      summarizable.push(candidate);
    }

    if (typeof candidate.labels !== 'undefined' &&
        candidate.labels[0] === 'BackgroundPage') {

      var error = 'Extensions running during capture; ' +
                  'see http://bit.ly/bigrig-extensions';
      if (typeof opts !== 'undefined' && opts.strict) {
        throw error;
      }
    }
  }

  if (summarizable.length === 0) {
    throw 'Zero processes (tabs) found.';
  }

  if (summarizable.length > 1) {
    var bullet = '\n  * ';
    var tabs = summarizable
        .map(pr => pr.labels[0])
        .map(l => l.trim()).join(bullet);

    console.warn('Multiple processes (tabs) found:' + bullet, tabs);

    summarizable = summarizable
        .filter(pr => !!pr.labels[0])
        .slice(-1);

    console.log('\nProceeding using the last named tab:' + bullet,
        summarizable[0].labels[0]);
  }

  traceProcess = summarizable.pop();
  // Reset all the globals we had to define for window etc.
  globalConfig.disable();
  return processTrace(model, traceProcess, opts);
}
```
- example usage
```shell
...
module.exports = {

  RESPONSE: processor.RESPONSE,
  ANIMATION: processor.ANIMATION,
  LOAD: processor.LOAD,

  analyze: function (traceContents, opts) {
    return processor.analyzeTrace(traceContents, opts);
  }
};
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

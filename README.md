# npmdoc-bigrig

#### basic api documentation for  [bigrig (v1.3.0)](https://github.com/GoogleChrome/node-big-rig#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-bigrig.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bigrig) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bigrig.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bigrig)

#### A CLI and node module for parsing trace (timeline) files from Chrome.

[![NPM](https://nodei.co/npm/bigrig.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/bigrig)

- [https://npmdoc.github.io/node-npmdoc-bigrig/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-bigrig/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bigrig/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bigrig/build/apidoc.html)

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
            "name": "aerotwist"
        }
    ],
    "name": "bigrig",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

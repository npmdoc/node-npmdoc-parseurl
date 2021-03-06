# npmdoc-parseurl

#### api documentation for  [parseurl (v1.3.1)](https://github.com/pillarjs/parseurl)  [![npm package](https://img.shields.io/npm/v/npmdoc-parseurl.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-parseurl) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-parseurl.svg)](https://travis-ci.org/npmdoc/node-npmdoc-parseurl)

#### parse a url with memoization

[![NPM](https://nodei.co/npm/parseurl.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/parseurl)

- [https://npmdoc.github.io/node-npmdoc-parseurl/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-parseurl/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-parseurl/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-parseurl/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-parseurl/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-parseurl/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jonathan Ong",
        "url": "http://jongleberry.com"
    },
    "bugs": {
        "url": "https://github.com/pillarjs/parseurl/issues"
    },
    "contributors": [
        {
            "name": "Douglas Christopher Wilson"
        }
    ],
    "dependencies": {},
    "description": "parse a url with memoization",
    "devDependencies": {
        "beautify-benchmark": "0.2.4",
        "benchmark": "2.0.0",
        "fast-url-parser": "1.1.3",
        "istanbul": "0.4.2",
        "mocha": "~1.21.5"
    },
    "directories": {},
    "dist": {
        "shasum": "c8ab8c9223ba34888aa64a297b28853bec18da56",
        "tarball": "https://registry.npmjs.org/parseurl/-/parseurl-1.3.1.tgz"
    },
    "engines": {
        "node": ">= 0.8"
    },
    "files": [
        "LICENSE",
        "HISTORY.md",
        "README.md",
        "index.js"
    ],
    "gitHead": "6d22d376d75b927ab2b5347ce3a1d6735133dd43",
    "homepage": "https://github.com/pillarjs/parseurl",
    "license": "MIT",
    "maintainers": [
        {
            "name": "jongleberry"
        },
        {
            "name": "dougwilson"
        },
        {
            "name": "tjholowaychuk"
        },
        {
            "name": "mscdex"
        },
        {
            "name": "fishrock123"
        },
        {
            "name": "defunctzombie"
        }
    ],
    "name": "parseurl",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pillarjs/parseurl.git"
    },
    "scripts": {
        "bench": "node benchmark/index.js",
        "test": "mocha --check-leaks --bail --reporter spec test/",
        "test-cov": "istanbul cover node_modules/mocha/bin/_mocha -- --check-leaks --reporter dot test/",
        "test-travis": "istanbul cover node_modules/mocha/bin/_mocha --report lcovonly -- --check-leaks --reporter spec test/"
    },
    "version": "1.3.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

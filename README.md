# api documentation for  [parseurl (v1.3.1)](https://github.com/pillarjs/parseurl)  [![npm package](https://img.shields.io/npm/v/npmdoc-parseurl.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-parseurl) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-parseurl.svg)](https://travis-ci.org/npmdoc/node-npmdoc-parseurl)
#### parse a url with memoization

[![NPM](https://nodei.co/npm/parseurl.png?downloads=true)](https://www.npmjs.com/package/parseurl)

[![apidoc](https://npmdoc.github.io/node-npmdoc-parseurl/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-parseurl_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-parseurl/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-parseurl/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-parseurl/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jonathan Ong",
        "email": "me@jongleberry.com",
        "url": "http://jongleberry.com"
    },
    "bugs": {
        "url": "https://github.com/pillarjs/parseurl/issues"
    },
    "contributors": [
        {
            "name": "Douglas Christopher Wilson",
            "email": "doug@somethingdoug.com"
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
            "name": "jongleberry",
            "email": "jonathanrichardong@gmail.com"
        },
        {
            "name": "dougwilson",
            "email": "doug@somethingdoug.com"
        },
        {
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        },
        {
            "name": "mscdex",
            "email": "mscdex@mscdex.net"
        },
        {
            "name": "fishrock123",
            "email": "fishrock123@rocketmail.com"
        },
        {
            "name": "defunctzombie",
            "email": "shtylman@gmail.com"
        }
    ],
    "name": "parseurl",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module parseurl](#apidoc.module.parseurl)
1.  [function <span class="apidocSignatureSpan">parseurl.</span>original (req)](#apidoc.element.parseurl.original)



# <a name="apidoc.module.parseurl"></a>[module parseurl](#apidoc.module.parseurl)

#### <a name="apidoc.element.parseurl.original"></a>[function <span class="apidocSignatureSpan">parseurl.</span>original (req)](#apidoc.element.parseurl.original)
- description and source-code
```javascript
function originalurl(req) {
  var url = req.originalUrl

  if (typeof url !== 'string') {
    // Fallback
    return parseurl(req)
  }

  var parsed = req._parsedOriginalUrl

  if (fresh(url, parsed)) {
    // Return cached URL parse
    return parsed
  }

  // Parse the URL
  parsed = fastparse(url)
  parsed._raw = url

  return req._parsedOriginalUrl = parsed
}
```
- example usage
```shell
...
### parseurl(req)

Parse the URL of the given request object (looks at the 'req.url' property)
and return the result. The result is the same as 'url.parse' in Node.js core.
Calling this function multiple times on the same 'req' where 'req.url' does
not change will return a cached parsed object, rather than parsing again.

### parseurl.original(req)

Parse the original URL of the given request object and return the result.
This works by trying to parse 'req.originalUrl' if it is a string, otherwise
parses 'req.url'. The result is the same as 'url.parse' in Node.js core.
Calling this function multiple times on the same 'req' where 'req.originalUrl'
does not change will return a cached parsed object, rather than parsing again.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

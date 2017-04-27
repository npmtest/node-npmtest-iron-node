# npmtest-iron-node

#### basic test coverage for  [iron-node (v3.0.18)](https://github.com/s-a/iron-node#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-iron-node.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-iron-node) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-iron-node.svg)](https://travis-ci.org/npmtest/node-npmtest-iron-node)

#### Debug Node.js code on the fly with Chrome Developer Tools on Linux, Windows and OS X.

[![NPM](https://nodei.co/npm/iron-node.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/iron-node)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-iron-node/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-iron-node/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-iron-node/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-iron-node/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-iron-node/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-iron-node/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-iron-node/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-iron-node/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-iron-node/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-iron-node/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-iron-node/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-iron-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-iron-node/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-iron-node/build/test-report.html](https://npmtest.github.io/node-npmtest-iron-node/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-iron-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-iron-node/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-iron-node/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-iron-node/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-iron-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-iron-node/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-iron-node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-iron-node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Stephan Ahlf",
        "url": "https://github.com/s-a"
    },
    "bin": {
        "iron-node": "./bin/run.js"
    },
    "bugs": {
        "url": "https://github.com/s-a/iron-node/issues"
    },
    "dependencies": {
        "commander": "^2.9.0",
        "deep-extend": "^0.4.1",
        "electron": "^1.4.15",
        "electron-recompile": "^1.0.16",
        "markdown": "^0.5.0",
        "nmp": "^1.0.3",
        "package.js": "^1.1.3",
        "pretty-error": "^2.0.2",
        "syntax-error": "^1.1.6"
    },
    "description": "Debug Node.js code on the fly with Chrome Developer Tools on Linux, Windows and OS X.",
    "devDependencies": {
        "changelog": "^1.0.7",
        "eslint": "^3.14.1",
        "eslint-config-xo-space": "^0.14.0",
        "jshint": "^2.9.4",
        "mdlint": "^0.1.0",
        "mocha": "^2.5.3",
        "pre-commit": "^1.2.2",
        "should": "^8.4.0"
    },
    "directories": {},
    "dist": {
        "shasum": "76d050773f16e66566bcd4ba857c73c1edd27d08",
        "tarball": "https://registry.npmjs.org/iron-node/-/iron-node-3.0.18.tgz"
    },
    "gitHead": "ab6a5aeaab6eb89ad6875176aeadca711471fc0f",
    "homepage": "https://github.com/s-a/iron-node#readme",
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "s-a"
        }
    ],
    "name": "iron-node",
    "optionalDependencies": {},
    "pre-commit": [
        "test",
        "mdlint"
    ],
    "preferGlobal": true,
    "productName": "ironNode",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/s-a/iron-node.git"
    },
    "scripts": {
        "bump": "npm version patch && git push && git push --tags && npm publish",
        "changelog": "node node_modules/changelog/bin/changelog.js all --markdown  > ./CHANGELOG.md",
        "compiler": "electron ./app --compile=c:\\git\\require\\",
        "dev": "node bin/run.js",
        "edge-test": "node bin/run.js ..\\require\\edge.js",
        "err": "node bin/run.js ..\\require\\error.js",
        "mdlint": "rem node_modules/.bin/mdlint glob \"docs/*.md\"",
        "mocha-debug": "electron ./app node_modules/mocha/bin/_mocha",
        "mocha-t": "iron-node node_modules/mocha/bin/_mocha",
        "mocha-test": "node bin/run.js node_modules/mocha/bin/_mocha",
        "node-sass-test": "electron ./app ..\\require\\node-sass.js",
        "pipe-test": "echo var i = 0;debugger; | node bin/run.js",
        "pipe-test-coffee": "coffee -p ./../require/app.coffee | node bin/run.js",
        "start": "node bin/run.js",
        "test": "node node_modules/mocha/bin/_mocha",
        "test-notify": "electron ./app ..\\require\\notify.js",
        "test2": "node bin/run.js ./../test.js"
    },
    "version": "3.0.18"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

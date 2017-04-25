# npmdoc-ttf2woff2

#### basic api documentation for  [ttf2woff2 (v2.0.3)](https://github.com/nfroidure/ttf2woff2)  [![npm package](https://img.shields.io/npm/v/npmdoc-ttf2woff2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ttf2woff2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ttf2woff2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ttf2woff2)

#### Convert TTF files to WOFF2 ones.

[![NPM](https://nodei.co/npm/ttf2woff2.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/ttf2woff2)

- [https://npmdoc.github.io/node-npmdoc-ttf2woff2/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-ttf2woff2/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ttf2woff2/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ttf2woff2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ttf2woff2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ttf2woff2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nicolas Froidure"
    },
    "bin": {
        "ttf2woff2": "bin/ttf2woff2.js"
    },
    "browser": "jssrc/index.js",
    "bugs": {
        "url": "https://github.com/nfroidure/ttf2woff2/issues"
    },
    "dependencies": {
        "bindings": "^1.2.1",
        "bufferstreams": "^1.1.0",
        "nan": "^2.1.0",
        "node-gyp": "^3.0.3"
    },
    "description": "Convert TTF files to WOFF2 ones.",
    "devDependencies": {
        "coveralls": "^2.11.4",
        "eslint": "^1.4.1",
        "eslint-config-simplifield": "^1.1.0",
        "istanbul": "^0.3.19",
        "miniquery": "^1.1.1",
        "mocha": "^2.3.2",
        "mocha-lcov-reporter": "^0.0.2"
    },
    "directories": {
        "test": "tests"
    },
    "dist": {
        "shasum": "5e020afe6e643287f3ad7687abed20fe654eb329",
        "tarball": "https://registry.npmjs.org/ttf2woff2/-/ttf2woff2-2.0.3.tgz"
    },
    "engines": {
        "node": ">=0.12"
    },
    "gitHead": "3a43adcd9fefd6e4539fb133a3b82b4ec7978eca",
    "gypfile": true,
    "homepage": "https://github.com/nfroidure/ttf2woff2",
    "keywords": [
        "ttf",
        "woff2",
        "fonts"
    ],
    "license": "MIT",
    "main": "src/index.js",
    "maintainers": [
        {
            "name": "nfroidure"
        }
    ],
    "name": "ttf2woff2",
    "optionalDependencies": {},
    "preferGlobal": "true",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/nfroidure/ttf2woff2.git"
    },
    "scripts": {
        "cli": "env NPM_RUN_CLI=1",
        "configure": "node-gyp configure",
        "cover": "istanbul cover --report html _mocha -- tests/*.mocha.js -R spec -t 5000",
        "coveralls": "istanbul cover _mocha --report lcovonly -- tests/*.mocha.js -R spec -t 5000 && cat ./coverage/lcov.info | coveralls && rm -rf ./coverage",
        "emcc": "miniquery -p \"targets.#.sources.#\" ./binding.gyp | grep -v \"csrc/addon.cc\" | xargs emcc --bind -o jssrc/ttf2woff2.js -O3 --memory-init-file 0 -s \"TOTAL_MEMORY=536870912\" -s \"ALLOW_MEMORY_GROWTH=1\" --post-js jssrc/post.js csrc/fallback.cc",
        "emcc-debug": "miniquery -p \"targets.#.sources.#\" ./binding.gyp | grep -v \"csrc/addon.cc\" | xargs emcc --bind -o jssrc/ttf2woff2.js -s \"ALLOW_MEMORY_GROWTH=1\" -s \"ASSERTIONS=1\" --post-js jssrc/post.js csrc/fallback.cc",
        "install": "(node-gyp rebuild > builderror.log) || (exit 0)",
        "lint": "eslint src/*.js tests/*.src jssrc/index.js",
        "make": "node-gyp build",
        "preversion": "npm run lint && npm test",
        "test": "mocha tests/*.mocha.js"
    },
    "version": "2.0.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

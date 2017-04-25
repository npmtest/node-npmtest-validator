# npmtest-validator

#### basic test coverage for  [validator (v7.0.0)](http://github.com/chriso/validator.js)  [![npm package](https://img.shields.io/npm/v/npmtest-validator.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-validator) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-validator.svg)](https://travis-ci.org/npmtest/node-npmtest-validator)

#### String validation and sanitization

[![NPM](https://nodei.co/npm/validator.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/validator)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-validator/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-validator/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-validator/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-validator/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-validator/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-validator/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-validator/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-validator/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-validator/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-validator/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-validator/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-validator/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-validator/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-validator/build/test-report.html](https://npmtest.github.io/node-npmtest-validator/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-validator/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-validator/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-validator/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-validator/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-validator/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-validator/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-validator/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-validator/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Chris O'Hara"
    },
    "bugs": {
        "url": "http://github.com/chriso/validator.js/issues"
    },
    "dependencies": {},
    "description": "String validation and sanitization",
    "devDependencies": {
        "babel-cli": "^6.16.0",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-preset-es2015": "^6.16.0",
        "babel-preset-es2015-rollup": "^1.2.0",
        "coveralls": "^2.11.9",
        "eslint": "^3.8.1",
        "eslint-config-airbnb-base": "^9.0.0",
        "eslint-plugin-import": "^2.0.1",
        "istanbul": "^0.4.3",
        "mocha": "^3.1.2",
        "rollup": "^0.29.1",
        "rollup-plugin-babel": "^2.5.1",
        "uglify-js": "^2.6.2"
    },
    "directories": {},
    "dist": {
        "shasum": "c74deb8063512fac35547938e6f0b1504a282fd2",
        "tarball": "https://registry.npmjs.org/validator/-/validator-7.0.0.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "files": [
        "index.js",
        "lib",
        "README.md",
        "LICENCE",
        "validator.js",
        "validator.min.js"
    ],
    "gitHead": "c812c206fe0004ea81e4ed854faf2a526bfa8e30",
    "homepage": "http://github.com/chriso/validator.js",
    "keywords": [
        "validator",
        "validation",
        "validate",
        "sanitization",
        "sanitize",
        "sanitisation",
        "sanitise",
        "assert"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "cohara87"
        }
    ],
    "name": "validator",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/chriso/validator.js.git"
    },
    "scripts": {
        "build": "npm run build:browser && npm run build:node",
        "build:browser": "babel-node build-browser && npm run minify",
        "build:node": "babel src -d . --presets es2015 --plugins add-module-exports",
        "clean": "npm run clean:node && npm run clean:browser",
        "clean:browser": "rm -rf validator*.js",
        "clean:node": "rm -rf index.js lib",
        "coveralls": "istanbul cover _mocha --report lcovonly -x validator.js -- -R spec && cat ./coverage/lcov.info | coveralls && rm -rf ./coverage",
        "lint": "eslint src test",
        "minify": "uglifyjs validator.js -o validator.min.js  --compress --mangle --comments '/Copyright/'",
        "pretest": "npm run lint && npm run build",
        "test": "mocha --reporter spec"
    },
    "version": "7.0.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

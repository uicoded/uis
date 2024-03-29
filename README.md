[![Build Status](https://travis-ci.org/uicoded/uis.svg?branch=master)](https://travis-ci.org/uicoded/uis)
[![Coverage Status](https://img.shields.io/coveralls/uicoded/uis.svg)](https://coveralls.io/r/uicoded/uis?branch=master)

# UIS - UI Suite

## Purpose

UIS is set of tools to create style guide. The goal is to manage color scheme, contrast ratios, fonts and other design artifacts.
  


It uses [LineZero](https://github.com/uicoded/linezero) as a starter.




## Run With NPM

 * `npm start` installs the packages and starts the dev server
 * `npm test` starts headless unit testing (continuous - will exit upon completition)
 * `npm run-script e2e-test` starts E2E test (single check of `index.html`)


## Run With Grunt

1. Install

  `npm install`

  `npm install -g grunt-cli` (should install itself, [getting started with Grunt](http://gruntjs.com/getting-started))

2. Build

  `grunt`

  - creates `build` folder with production code (minified, etc)
  - creates `index.html` from `README.md` 
    LineZero uses [Github flavored mardown](https://help.github.com/articles/github-flavored-markdown/)
    with code [Highlight JS](https://highlightjs.org/) (test syntax `docs/gfm.md`)
  - connects to http://localhost:8080 (to build without starting server call `grunt build`)

3. Develop

  `grunt dev`

  - starts the testing server [http://localhost:8000](http://localhost:8000)
  - starts the watch using `livereload` (see the settings [tasks/options/watch.js](http://localhost:8000/tasks/options/watch.js))
  
  `grunt watch`
  
  - starts the watch without starting server
   
4. Test

  * Unit

  [Karma](http://karma-runner.github.io/) - standalone, without Grunt help at this time.

  `karma start test/karma-conf.js` for dev or `karma start test/karma-conf.js --single-run` for the CI. 

  * E2E

  [Protractor](http://angular.github.io/protractor/) - launches Chrome

  `protractor test/protractor-conf.js` runs the testruner. (make sure the dev server is running)


## License

MIT

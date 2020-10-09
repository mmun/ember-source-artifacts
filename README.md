# ember-source-artifacts

This is a custom build artifact of ember-source@2.12.2 which allows backtracking during rerendering.
For more information about this topic check out https://github.com/emberjs/ember.js/issues/13948.

This build was produced with the follow steps:

```
nvm use 10 # Use Node 10. Later versions of Node won't work with this version of ember-cli.
git clone https://github.com/emberjs/ember.js.git
cd ember.js
git checkout v2.12.2
yarn
ALLOW_BACKTRACKING=true ember build --environment=production
```

These commands produced the following console output

```
$ ALLOW_BACKTRACKING=true ember build --environment=production
WARNING: Node v10.19.0 is not tested against Ember CLI on your platform. We recommend that you use the most-recent "Active LTS" version of Node.js.
⠋ Building(node:85803) [DEP0022] DeprecationWarning: os.tmpDir() is deprecated. Use os.tmpdir() instead.
⠦ Building
glimmer-runtime/lib/references.ts[4, 37]: expected an assignment or function call
glimmer-runtime/lib/references.ts[8, 50]: expected an assignment or function call
glimmer-runtime/lib/references.ts[12, 36]: expected an assignment or function call
glimmer-runtime/lib/references.ts[32, 21]: expected an assignment or function call
glimmer-runtime/lib/references.ts[55, 26]: expected an assignment or function call
glimmer-runtime/lib/references.ts[9, 32]: Missing semicolon
glimmer-runtime/lib/references.ts[10, 31]: Missing semicolon
glimmer-runtime/lib/references.ts[11, 31]: Missing semicolon
glimmer-runtime/lib/references.ts[12, 34]: Missing semicolon
glimmer-runtime/lib/references.ts[21, 42]: Missing semicolon
glimmer-runtime/lib/references.ts[28, 34]: Missing semicolon
glimmer-runtime/lib/references.ts[32, 19]: Missing semicolon
glimmer-runtime/lib/references.ts[34, 4]: Missing semicolon
glimmer-runtime/lib/references.ts[64, 56]: Missing semicolon

======= Found 14 tslint errors in 176 files =======
cleaning up...
Built project successfully. Stored in "dist/".
File sizes:
 - dist/ember-runtime.js: 675.66 KB (147.28 KB gzipped)
 - dist/ember-template-compiler.js: 947.51 KB (180.18 KB gzipped)
 - dist/ember-testing.js: 72.91 KB (16.9 KB gzipped)
 - dist/ember-tests.js: 2.71 MB (349.03 KB gzipped)
 - dist/ember-tests.prod.js: 2.7 MB (347.6 KB gzipped)
 - dist/ember.debug.js: 1.91 MB (404.79 KB gzipped)
 - dist/ember.js: 1.91 MB (404.79 KB gzipped)
 - dist/ember.min.js: 520.85 KB (129.25 KB gzipped)
 - dist/ember.prod.js: 1.78 MB (375.97 KB gzipped)
 - dist/jquery/jquery.js: 260.93 KB (77.2 KB gzipped)
 - dist/qunit/qunit.css: 5.27 KB (1.53 KB gzipped)
 - dist/qunit/qunit.js: 112.37 KB (30.06 KB gzipped)
 - dist/tests/node/app-boot-test.js: 3.56 KB (967 B gzipped)
 - dist/tests/node/component-rendering-test.js: 883 B (423 B gzipped)
 - dist/tests/node/helpers/app-module.js: 5.35 KB (1.8 KB gzipped)
 - dist/tests/node/helpers/assert-html-matches.js: 693 B (399 B gzipped)
 - dist/tests/node/helpers/build-owner.js: 646 B (303 B gzipped)
 - dist/tests/node/helpers/component-module.js: 3.37 KB (1.09 KB gzipped)
 - dist/tests/node/template-compiler-test.js: 1.74 KB (573 B gzipped)
 - dist/tests/node/visit-test.js: 7.6 KB (1.79 KB gzipped)
```

I then merged the nine `dist/ember-*` files into the official build artifiact for ember-source@2.12.2.

---

<p align="center">
  <a href="http://emberjs.com"><img width="300" src="http://emberjs.com/images/brand/ember_Ember-Light.png"></a>
</p>

<p align="center">
  <a href="http://travis-ci.org/emberjs/ember.js"><img src="https://secure.travis-ci.org/emberjs/ember.js.svg?branch=master" alt="Build Status"></a>
  <a href="https://codeclimate.com/github/emberjs/ember.js"><img src="https://codeclimate.com/github/emberjs/ember.js.svg" alt="Code Climate"></a>
  <a href="https://ember-community-slackin.herokuapp.com"><img src="https://ember-community-slackin.herokuapp.com/badge.svg" alt="Build Status"></a>
</p>

<p align="center">
  <a href="https://saucelabs.com/u/ember-ci"><img src="https://saucelabs.com/browser-matrix/ember-ci.svg" alt="Sauce Test Status"></a>
</p>

Ember.js is a Javascript framework that greatly reduces the time, effort and resources needed
to build any web application. It is focused on making you, the developer, as productive as possible by doing all the common, repetitive, yet essential, tasks involved in most web development projects.

Ember.js also provides access to the most advanced features of Javascript, HTML and the Browser giving you everything you need to create your next killer web app.

- [Website](http://emberjs.com)
- [Guides](http://guides.emberjs.com)
- [API](http://emberjs.com/api)
- [Community](http://emberjs.com/community)
- [Blog](http://emberjs.com/blog)
- [Builds](http://emberjs.com/builds)

# Contribution

See [CONTRIBUTING.md](https://github.com/emberjs/ember.js/blob/master/CONTRIBUTING.md)

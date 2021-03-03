# Ember 2.12 "Loose mode" with backtracking enabled

- ember-source branch: https://github.com/mmun/ember.js/tree/lts-2-12-loose
- ember-source commit: https://github.com/mmun/ember.js/commit/f8650983324e49dfa920c9da0820f462258fc12f
- Build flags: ALLOW_BACKTRACKING=true

This is a build artifact of [mmun](https://github.com/mmun)'s custom Ember 2.12 "loose mode".
It removes some restrictions imposed by Ember 2.12 to make it easier to upgrade from Ember 2.8.
For more information see https://github.com/mmun/ember.js/tree/lts-2-12-loose and https://github.com/emberjs/ember.js/issues/13948.

This build was produced with the follow steps:

```
nvm use 10 # Use Node 10. Later versions of Node won't work with this version of ember-cli.
git clone https://github.com/mmun/ember.js.git
cd ember.js
git checkout lts-2-12-loose
yarn
ALLOW_BACKTRACKING=true ember build --environment=production
npm pack
tar xvzf ember-source-2.12.2.tgz --strip-components 1 -C ../ember-source-artifacts
```

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

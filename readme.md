# Node Gigya Boilerplate

# ##################
# this now lives here https://github.com/gigya/node-gigya-boilerplate
# ##################
 I'm going to leave this repo here as its a tidy boilerplate node server


![Travis CI status](https://api.travis-ci.org/maxmckenzie/node-gigya-boilerplate.svg?branch=master "Travis CI eslint, unit and integration tests:")

Boilerplate Node.js App using the Gigya accountJS Raas service. This project is intended to be used as a starting point for anyone working with the gigya platform on node.js

Support: raise an issue on github https://github.com/maxmckenzie/node-gigya-boilerplate/issues

## Features

- babel es2015 and stage-0
- mocha unit tests
- webdriverio integration e2e tests using chimp
- direnv directory based environment variables (so you do not need to install global node modules)
- circle ci YAML file (but it does not work and i'm not that impressed by circle ci so i'll likely replace it with another CI such as travis)

## Install Dependencies

The blow steps are for OSX, but you could replace brew with `yum` or `apt-get` and it should still work.
> Windows user: your on your own with how to install but you still need the below installed

- `brew install node`
- `brew install direnv`

## Install App

- `npm install`
- `direnv allow`

## Run Dev

- `npm run dev`

This boots the app runs the unit and e2e tests. Then uses nodemon to wait for changes. When a change happens the node server is rebooted and the tests are run again

> `mocha --watch` and similar has an issue. To run the server on test you need to add an import to the test.js file. When watching this cause a EDDRINUSE error (the server is already booted). running the stack with nodemon avoids this

## Production

- `npm run build`
- `npm start`

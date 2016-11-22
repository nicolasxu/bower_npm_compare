# Module number
350,000



# Structure Difference
npm does nested dependency tree (size heavy)
Can dependent on many version of same package


# modules vs. globals 
Common JS Modules, and require transpiling to work in browser,some of them don't need to.
https://github.com/umdjs/umd/blob/master/templates/jqueryPlugin.js
http://confluence.medtouch.com/display/PRODUCT/Front-end+Build+With+Webpack
Nodejs way of managing dependencies for front-end



# Publish private package
npm config set registry http://localhost:81/npm/medtouch-npm
npm adduser
npm publish
* the user is existing user on ProGet server*






# Consume private registry
{
  "name": "consume_npm_pkg",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "lodash": "^4.17.2",
    "sample_npm_package": "https://github.com/nicolasxu/sample_npm_package.git",
    "mttest_npm_pkg": "https://NicolasXu999@bitbucket.org/medtouch/mttest_npm_pkg.git#v1.0.1"
  }
}
Use MedTouch bitbucket repo as dependencies URL with version. 
Works well without private NPM or Bower registry. 



# Opinion from Spotify
Please refer to bower.md
















# dedupe tool
https://docs.npmjs.com/cli/dedupe
Searches the local package tree and attempts to simplify the overall structure by moving dependencies further up the tree, where they can be more effectively shared by
multiple dependent packages.



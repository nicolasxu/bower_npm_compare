# Module number
50,000
http://www.modulecounts.com/


# Structure Difference
Bower requires a flat dependency tree 
(puts the burden of dependency resolution on the user).
One version of each package

# modules vs. globals 
Intended for Global Resources, Like <script> Tags. 
Work in borwser directly.
You can put CMD package in side bower package, but it is not 
intended usage.



# Publish private package
1. edit .bowerrc
{
    "registry": "http://nick:123456@localhost:81/bower/medtouch-bower/",
    "timeout": 300000
}
2. Run this command: 
   bower register sample_bower_package https://github.com/nicolasxu/sample_bower_package.git
    


# Consume private registry
{
  "name": "bower_proj",
  "description": "test bower package manager",
  "main": "",
  "license": "MIT",
  "homepage": "",
  "ignore": [
    "**/.*",
    "node_modules",
    "bower_components",
    "test",
    "tests"
  ],
  "dependencies": {
    "jquery": "^3.1.1",
    "bower-sample-package": "*"
  }
}



# Opinion from Spotify
In almost all cases, it's more appropriate to use Browserify 
and npm over Bower. It is simply a better packaging solution 
for front-end apps than Bower is. At Spotify, we use npm to 
package entire web modules (html, css, js) and it works 
very well.

Bower brands itself as the package manager for the web. 
It would be awesome if this was true - a package manager 
that made my life better as a front-end developer would 
be awesome. The problem is that Bower offers no specialized 
tooling for the purpose. It offers NO tooling that I know 
of that npm doesn't, and especially none that is specifically 
useful for front-end developers. There is simply no benefit 
for a front-end developer to use Bower over npm.

We should stop using bower and consolidate around npm. 
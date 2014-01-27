jasmine-node
============

You  need jasmine-node which is a node.js package

it puts them in a node_module directory (which is one directory up on my setup) where you run it from

>sudo npm install jasmine-node

so there will be a ../node_modules/jasmine-node/bin/jasmine-node file
currently the javascript test is in <src>/javascript/demo
and you run the tests with

>../node_modules/jasmine-node/bin/jasmine-node --verbose --junitreport --noColor  spec

this creates junit output which can be loaded using the jenkins junit plugin

There is also javascript coverage using istanbul

>sudo npm install -g istanbul

make sure your run the istanbul from the one installed
/usr/local/bin/istanbul -> /usr/local/lib/node_modules/istanbul/lib/cli.js
istanbul@0.2.4 /usr/local/lib/node_modules/istanbul


run the tests like this (from demo)

>/usr/local/bin/istanbul cover spec/PlayerSpec.js

>/usr/local/bin/istanbul report cobertura


jasmine-node
============

You  need jasmine-node which is a node.js package

it puts them in a node_module directory where you run it from

>npm jasmine-node

so there will be a ./node_modules/jasmine-node/bin/jasmine-node file
currently the javascript test is in <src>/javascript/demo
and you run the tests with

cd demo
./node_modules/jasmine-node/bin/jasmine-node --verbose --junitreport --noColor  spec

this creates junit output which can be loaded using the jenkins junit plugin

There is also javascript coverage using istanbul
once again this is downloaded with 

>sudo npn istanbul

run the tests like this (from demo)

>istanbul cover spec/PlayerSpec.js

>istanbul report cobertura


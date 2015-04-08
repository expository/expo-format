# Expository: Human-first API Documentation

## Motivation

Many software tools generate web service documentation from a machine-readable description of an API (e.g. from WSDL, WADL, or Swagger), but often the results are not very *human*-friendly: [we](http://www.filigris.com/docflex-xml/wsdldoc/examples/html/ebaySvc/index.html). [deserve](https://cdn.rawgit.com/ipcsystems/wadl-stylesheet/master/example_wadl.xml). [better](http://petstore.swagger.io/#!/pet/addPet). The Expository format was created with the goal of teaching machines to understand human-generated API documentation rather than the other way around. This allows the machines to do what they're good at (executing test cases, automated validation, live demos) and leaves the writing and presentation to us humans.

## Examples are the key

High-quality API documentation is usually structured around well-crafted examples. Examples are the best way to show what a web service does and how it helps solve a particular problem. API examples are also fairly simple for a machine to recognize and leverage for its own purposes. There are many possibilities: 

  - **Want to verify that a system does what you say it does?** Have a machine run the examples as test cases. *Bonus points* for running this as part of your Continuous Integration process to guarantee the docs and implementation are in sync.
  - **Want to let customers poke around and explore your API?** Have a machine convert the documented examples into a [Postman](https://www.getpostman.com/) collection or [SoapUI](http://www.soapui.org/rest-testing/getting-started.html) project.
  - **Gathering requirements?** Let your documentation serve double-duty as acceptance criteria.
  

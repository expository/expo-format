# Expo: Human-first API Documentation

## Motivation

Many software tools generate web service documentation from a machine-readable description of an API (e.g. from WSDL, WADL, or Swagger), but often the results are **not** very *human*-friendly. [We](http://www.filigris.com/docflex-xml/wsdldoc/examples/html/ebaySvc/index.html). [Deserve](https://cdn.rawgit.com/ipcsystems/wadl-stylesheet/master/example_wadl.xml). [Better](http://petstore.swagger.io/#!/pet/addPet).

The Expo specification was created with the goal of teaching machines to understand human-generated API documentation rather than the other way around. This allows the machines to do what they're good at (executing test cases, automated validation, interactive stubs, live demos) and leaves the writing and presentation to us humans.

## Examples are the Key

High-quality API documentation is usually structured around well-crafted examples. Examples are the best way to show what a web service does and how it helps solve a particular problem. API examples are also fairly simple for a machine to recognize and leverage for its own purposes. There are many possibilities:

  - **Want to verify that a system does what you say it does?** Have a machine run the examples as test cases. Do this as part of your Continuous Integration process to guarantee the docs and implementation are in sync.
  - **Want to let customers poke around and explore your API?** Have a machine convert the documented examples into a [Postman](https://www.getpostman.com/) collection or [SoapUI](http://www.soapui.org/rest-testing/getting-started.html) project for humans to play with.
  - **Gathering requirements?** Let your documentation serve double-duty as acceptance criteria for your implementation.
  - **Need a stub service to build against?** Use the web service documentation to automatically generate a stub implementation with canned responses pulled straight from the API docs.


## A Documentation _Convention_ and a JSON _Format_

Most API documents are _already_ using examples to describe how the service works. Look at the [Twitter API](https://dev.twitter.com/rest/public), [GitHub API](https://developer.github.com/v3/), and [Facebook API](https://developers.facebook.com/docs/graph-api/reference): they all feature prominent example requests and responses. The Expo spec just defines how machines should process those kinds human-targeted documents.

## The Spec

The spec itself is a set of declarative examples in [`spec.txt`](spec.txt). This is basically a Markdown file, with input/output examples written in sequence:

~~~~~~~
```html
HTML source
```
```json
expected JSON output
```
~~~~~~

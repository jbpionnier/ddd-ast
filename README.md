# DDD AST
Extract identifiers from Java sources

## Objective
Quickly establish a list of identifiers with their # of occurrences to match them with the ubiquitous language 
dictionary and calculate a "DDD score"

## Principle
Uses [java-parser](https://github.com/jhipster/prettier-java/tree/master/packages/java-parser) to build Concrete Syntax 
Tree from Java files and extract identifiers and then collecting them, counting and sorting by count

## How to use

### Standalone

In the project directory:

`npm install` to install required dependencies

`node parse.js` to parse stdin

### As a dependency

That's how this package is intended to be used 😃

Suppose you have a Java project "my-java-project" then you can use this command in a script in your projects:

```shell
$ cat HelloWorldExample.java | npx @lolo101/ddd-ast | sort | uniq -c | sort -nr
      2 System
      2 String
      2 println
      2 out
      2 arguments
      2 args
      1 main
      1 List
      1 HelloWorldExample
      1 asList
      1 Arrays
```

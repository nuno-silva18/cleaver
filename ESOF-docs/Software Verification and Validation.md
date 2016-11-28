# Cleaver

## Table of Contents
* [Cleaver](#cleaver)
    * [Cleaver's Verification and Validation](#introreq)
        * [Software Testability and Reviews](#testandrev)
        * [Verification and Validation in Cleaver](#verifvalidcleaver)
            *[What is JSHint?](#jshint)
            *[Test Statistics and Analytics](#teststats)
        * [Bug and Correction](#bug)
    * [Contribution of Team Members](#contributions)

<div id='testandrev'>

## Software Testability and Reviews

<div id='verifvalidcleaver'>

## Verification and Validation in Cleaver

Cleaver currently doesn't feature any dynamic software verification and verification (V&V) techniques, such as software testing, that allow its developer to verify that every part of the application is functioning properly. The only software V&V that occurs in Cleaver is through static techniques, notably through the use of the static code analysis tool [JSHint](http://jshint.com/) and, presumably software reviews and inspection, done by both the developer and the open-source community surrounding the project. These reviews and inspections are supposedly informal and, even though they are made with the same goals of reviews and inspections done at a professional level, they do not share the same level of rigorousness.

<div id='jshint'>

### What is JSHint?

JSHint is a [static code analysis](https://en.wikipedia.org/wiki/Static_program_analysis) tool used to detect errors and potential problems in JavaScript code. This tool was developed with the goal of simplifying the debugging of commonly made mistakes and potential bugs in a program, such as syntax errors, bugs due to implicit type conversions, leaking variables, etc.

The developers of JSHint note that, while the tool can detect multiple different mistakes in the application, it is not a substitute to unit and functional testing and should be used, instead, in conjunction with these types of testing.

<div id='teststats'>

### Test Statistics and Analytics

There are no test statistics and analytics that can be made explicit, seeing as how Cleaver does not feature any kind of software testing in its test suite.

<div id='bug'>

## Bug and Correction

<div id='contributions'>

## Contribution of Team Members

| Team member | Contribution |
| ----------  | ------------ |
| André Correia | [Functional and non-functional requirements](#specreqandfeat) and fleshing out user stories |
| João Mendonça | [Use Cases](#usecases) and further fleshing out user stories |
| Luís Couto | [Cleaver's requirements](#introreq) | 
| Nuno Silva | [Verification and Validation in Cleaver](#verifvalidcleaver) |
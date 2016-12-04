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
Testing is intended to show that a program does what it is intended to do and to discover program defects before it is put into use. When we test software, we execute a program using artificial data. We check the results of the test run for errors, anomalies, or information about the program’s non-functional attributes.

The testing process has two distinct goals:
* To demonstrate to the developer and the customer that the software meets its requirements. For custom software, this means that there should be at least one test for every requirement in the requirements document. For generic software products, it means that there should be tests for all of the system features, plus combinations of these features, that will be incorporated in the product release.
* To discover situations in which the behavior of the software is incorrect, undesirable, or does not conform to its specification. These are a consequence of software defects. Defect testing is concerned with rooting out undesirable system behavior such as system crashes, unwanted interactions with other systems, incorrect computations, and data corruption.

The first goal leads to validation testing, where you expect the system to perform correctly using a given set of test cases that reflect the system’s expected use. The second goal leads to defect testing, where the test cases are designed to expose defects. The test cases in defect testing can be deliberately obscure and need not reflect how the system is normally used. Of course, there is no definite boundary between these two approaches to testing. During validation testing, we will find defects in the system; during defect testing, some of the tests will show that the program meets its requirements.
However, testing cannot demonstrate that the software is free of defects or that it will behave as specified in every circumstance. It is always possible that a test that you have overlooked could discover further problems with the system.

Verification and validation processes are concerned with checking that software being developed meets its specification and delivers the functionality expected by the people paying for the software. These checking processes start as soon as requirements become available and continue through all stages of the development process.
The aim of verification is to check that the software meets its stated functional and non-functional requirements. Validation, however, is a more general process. The aim of validation is to ensure that the software meets the customer’s expectations. It goes beyond simply checking conformance with the specification to demonstrating that the software does what the customer expects it to do. Validation is essential because requirements specifications do not always reflect the real wishes or needs of system customers and users.
The ultimate goal of verification and validation processes is to establish confidence that the software system must be good enough for its intended use. The level of required confidence depends on the system’s purpose, the expectations of the system users and the current marketing environment for the system.

As well as software testing, the verification and validation process may involve software inspections and reviews. Inspections and reviews analyze and check the system requirements, design models, the program source code, and even proposed system tests. Inspections mostly focus on the source code of a system but any readable representation of the software, such as its requirements or a design model, can be inspected. When we inspect a system, we use knowledge of the system, its application domain, and the programming or modeling language to discover errors.

The testing process usually involves a mixture of manual and automated testing. In manual testing, a tester runs the program with some test data and compares the results to their expectations. They note and report discrepancies to the program developers. In automated testing, the tests are encoded in a program that is run each time the system under development is to be tested. This is usually faster than manual testing, especially when it involves regression testing—re-running previous tests to check that changes to the program have not introduced new bugs.
However, testing can never be completely automated as automated tests can only check that a program does what it is supposed to do. It is practically impossible to use automated testing to test systems that depend on how things look, or to test that a program does not have unwanted side effects.[1]

[1] Sommerville, I. (2011) Software Engineering, 9ª ed. Addison-Wesley.

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

We have manually analysed the project and with tool-based analysis, in its requirements specs and code and we have not found significant bugs.
It has no unit/automated tests defined, and testing is apparently done by the develper himself and later by users, on release and the developer usually fixes reported bugs (when confirmed).

Although the tests performed do not prove the absence of major bugs, the scarce amount of code of the project and its low complexity reduce statistically the probability of their existence.

We can point to a validation error: the program  requires a settings.json file to exist for local themes (but not for remote theme), which can lead to a ENOENT ("Error no entry").
In the requirements, it is stated that the program should only read available files, as "they are optional". That means that the objective isn't fulfilled therefore,the precondition does not hold in the post-condition.




<div id='contributions'>

## Contribution of Team Members

| Team member | Contribution |
| ----------  | ------------ |
| André Correia | [Software Testability and Reviews](#testandrev) |
| João Mendonça | [Bug and Correction](#bug) |
| Luís Couto | [Bug and Correction](#bug) | 
| Nuno Silva | [Verification and Validation in Cleaver](#verifvalidcleaver) |

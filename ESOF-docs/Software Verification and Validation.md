# Cleaver

## Table of Contents
* [Cleaver](#cleaver)
    * [Software Testability and Reviews](#testandrev)
        * [What is Software Testability and the Reviews Process?](#testandrevintro)
        * [Software Testability and Reviews in Cleaver](#testandrevcleaver)
    * [Verification and Validation in Cleaver](#verifvalidcleaver)
        * [What is JSHint?](#jshint)
        * [Test Statistics and Analytics](#teststats)
    * [Bug and Correction](#bugandfix)
        * [What is the Bug?](#bug)
        * [Bug Correction](#bugfix)
    * [Contribution of Team Members](#contributions)

<div id='testandrev'>

## Software Testability and Reviews

<div id='testandrevintro'>

## What is Software Testability and the Reviews Process?
Testing is used to show that a program does what it is intended to do and to discover any program defects before it is put into use. When we test software, we execute a program using artificial data. We check the results of the test run for errors, anomalies, or information about the program’s non-functional attributes.

The testing process has two distinct goals:
* To demonstrate to the developer and the customer that the software meets its requirements. For custom software, this means that there should be at least one test for every requirement in the requirements document. For generic software products, it means that there should be tests for all of the system's features, plus combinations of these features, that will be incorporated in the product release.
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

<div id='testandrevcleaver'>

## Software Testability and Reviews in Cleaver

Multiple aspects can make a piece of software easier or harder to test, and it's important to take into consideration these aspects when evaluating the developed test suite for an application's. These aspects can be quantified in 6 items:

* **Controllability** - Controllability determines the work it takes to set up and run test cases and the extent to which individual functions and features of the system under test can be made to respond to test cases. Some of the most difficult aspects that reduce controllability include testing a GUI with latency, OS exceptions that hard to catch or trigger, scalability testing, etc. In Cleaver's case, controllability fairly high, as the programming language Cleaver was developed on isn't difficult to develop tests for (JS) and the program's individual functions and features of the system are easily testable by feeding said functions data and expecting a certain outcome.
* **Observability** - Observability determines the work it takes to set up and run test cases and the extent to which the response of the system under test to test cases can be verified. Some of the most difficult aspects that reduce observability include noise while testing a GUI, silent failures regarding OS exceptions, etc. In Cleaver's case, we can conclude that observability is good, but not great, as JavaScript does fail silently in many different situations but determining whether or not a test passed/failed in the program is fairly simple, for the most part.
* **Isolateability** - The degree to which the component under test can be tested in isolation. Some of the most difficult aspects that reduce isolateability may include poorly written [spaggheti code](https://en.wikipedia.org/wiki/Spaghetti_code). Regarding Cleaver, the program itself is fairly modular, so isolateability is fairly high and it's possible to test just about every component in isolation.
* **Separation of Concerns** - The degree to which the component under test has a single, well defined responsibility. As aforementioned in the isolateability section, Cleaver itself is a modular program, with its functionalities separated into different, interchangeable modules. As such, the separation of concerns in Cleaver is a non-issue.
* **Understandability** - The degree to which the component under test has a single, well defined responsibility. Some of the most difficult aspects that reduce understandability may include poorly written (or non-existent) comments in the code and overall poor documentation on the project. Cleaver's documentation regarding code comments is really good, with every function's functionality fully explained in a comment above it, and its documentation, while good at explaining the project's functionalities, is non-existent regarding technical aspects such as software design, software process, etc. As such, Cleaver's understandability is good, but not great.
* **Heterogeneity** - The degree to which the use of diverse technologies requires to use diverse test methods and tools in parallel. In Cleaver's case, since the application is fully written in JavaScript and built with Node.js, heterogeneity in its testing is fairly reduced, since there is no need to use diverse test tools and methods to test the application.

<div id='verifvalidcleaver'>

## Verification and Validation in Cleaver

Cleaver currently doesn't feature any dynamic software verification and verification (V&V) techniques, such as software testing, that allow its developer to verify that every part of the application is functioning properly. The only software V&V that occurs in Cleaver is through static techniques, notably through the use of the static code analysis tool [JSHint](http://jshint.com/) and, presumably software reviews and inspection, done by both the developer and the open-source community surrounding the project. These reviews and inspections are supposedly informal and, even though they are made with the same goals of reviews and inspections done at a professional level, they do not share the same level of rigorousness.(*) As such, we can assume that Cleaver isn't a robust project, as changes submitted by the main developer and other contributors to the project aren't properly tested via software tests, and are merely tested for bugs via JSHint.

(*) The group has tried to get into contact with the owner and main developer behind the project, [Jordan Scales](https://github.com/jdan), in order to get additional information on the testing process behind Cleaver. Unfortunately, he has yet to respond to our e-mail.*

<div id='jshint'>

### What is JSHint?

JSHint is a [static code analysis](https://en.wikipedia.org/wiki/Static_program_analysis) tool used to detect errors and potential problems in JavaScript code. This tool was developed with the goal of simplifying the debugging of commonly made mistakes and potential bugs in a program, such as syntax errors, bugs due to implicit type conversions, leaking variables, etc.

The developers of JSHint note that, while the tool can detect multiple different mistakes in the application, it is not a substitute to unit and functional testing and should be used, instead, in conjunction with these types of testing.

<div id='teststats'>

### Test Statistics and Analytics

There are no test statistics and analytics that can be made explicit, seeing as how Cleaver does not feature any kind of software testing in its test suite.

<div id='bugandfix'>

## Bug and Correction

<div id='bug'>

### What is the Bug?

After manually analyzing the project as well as its issue tracker on Github, we were able to identify the following [bug](https://github.com/jdan/cleaver/issues/147): [Cleaver's documentation on its themes plugin](https://github.com/jdan/cleaver/blob/master/docs/themes.md) specifies that a theme is composed by the following files:
> * style.css - styles for your presentation
> * template.mustache - a template used to render the slides in your presentation
> * layout.mustache - a template used to render the entire document of your presentation
> * script.js - javascript to be included in your slideshow

The documentation also specifies:
> A theme does not need to contain all of these files, only the ones present will be loaded into your slideshow.

While this is true of remote themes, it seems that the settings.json file requires local themes to include all the files that compose a theme, and the program will not run while every file isn't specified on the settings.json theme, throwing an ENOENT ("ERROR NO ENTRY") bug.

<div id='bugfix'>

### Bug Correction

In order to correct this bug, we used Github user [Izrski's suggestion](https://github.com/jdan/cleaver/issues/147#issuecomment-184599270), which, while it allows the program to run, it does lead to less robustness in Cleaver, seeing as how it ignores important errors through this method.

## Contribution of Team Members

| Team member | Contribution |
| ----------  | ------------ |
| André Correia | [Software Testability and Reviews](#testandrevintro) |
| João Mendonça | [Bug and Correction](#bugandfix) |
| Luís Couto | [Bug and Correction](#bugandfix) | 
| Nuno Silva | [Verification and Validation in Cleaver](#verifvalidcleaver), [Software Testability and Reviews in Cleaver](#testandrevcleaver) and [Bug and Correction](#bugandfix)|

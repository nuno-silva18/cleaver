# Cleaver

## Table of Contents
* [Cleaver](#cleaver)
    * [What is Cleaver?](#intro)
    * [Features](#features)
    * [Development Process](#development)
        * [Methodology](#methodology)
        * [User contribution](#user_contribution)
        * [Opinion on the development process used](#opinion)

<div id='intro'/>
##What is Cleaver?

Cleaver is an open-source software, which creates HTML slideshow presentations from a [Markdown](https://en.wikipedia.org/wiki/Markdown) file. The objective is to reduce the cost of creating short (30 seconds) presentations, with a known syntax, and without installing a proprietary software, or learning a new language. Also, being HTML, the presentations can be put online, making them available in several devices without the need to install new software. Cleaver provides a default stylesheet, but can be further customised due to its theme support for optional stylesheet, templates and javascript extensions. Such gives it a more fine-grained control over the presentations.
The software is written in javascript, and runs over the node.js, which is also javascript. Furthermore, installing and implementing new features requires only the installation of node.js. However three languages (at least) are required in order to understand and improve Cleaver, namely Javascript (for the application itself), HTML (since it is the format in which the presentations are exported), and CSS (in order to customise the presentations).


##Advantages 

##Disadvantages

<div id='features'/>
##Features
* Author credits support twitter and other social media accounts
* Supports stylesheet customization
* Can change themes
* Possibility to export slide presentation
* Allows a progress bar on slides
* Encoded in utf-8

<div id='development'/>

## Development Process

### Methodology

*Note: The group has tried to get into contact with the owner and main developer behind the project, [Jordan Scales](https://github.com/jdan), in order to get additional information on the development process behind Cleaver. Unfortunately, he has yet to respond to our e-mail.*

Cleaver seems to be developed primarily under the [Feature-driven development process (FDD)](https://en.wikipedia.org/wiki/Feature-driven_development), a process in which features requested by users of the application are implemented on an iterative basis. 

From the documentation available on the application’s Github, it seems that a new feature is implemented when said feature is requested by a Github user, and any other user of the website that is interested in contributing to Cleaver responds to this request and takes charge of developing said feature. The developed feature by the user must pass Cleaver’s test script in order for it to be accepted into the code and the feature be fully integrated into the application. This process is aided by the Github tools [issue tracker](https://github.com/jdan/cleaver/issues), used to discuss the implementation of new features and any bugs present in current features, and [pull requests](https://github.com/jdan/cleaver/pulls), used for reviewing and implementing the newly developed features.

This development process is mainly based on these topics:
* Simple process easily understandable by all participants. Its simplicity allows full comprehension, not only by the users but also by developers
* The user gets stepwise access to the software although fully functional. This allows incremental requirements during the development process
* Few requirements allow to reduce the complexity of process, lowering the risk of misunderstanding between users and developers
* Quick development process as a whole
* No strictness following all the steps of development process
* Allows definition of new requirements or modifications in existing ones, during the process
* Suitable for small projects with small development teams
* The software is easily and quickly obtained with short development cycles due to few requirements
<div id='opinion'/>

### Opinion on the development process used

In the group’s opinion, we believe that the methodology Cleaver seems to have been developed under, Feature-driven Development (FDD), is the most adequate methodology for this type of project.

The use of a software development process that allows for the iterative and incremental implementation of an application’s features is often essential for the development of open-source projects. This [type of methods](https://en.wikipedia.org/wiki/Iterative_and_incremental_development) allow for a developer who has an interesting idea but is unsure about what the user requirements for the application will be, to start developing said idea and implement changes easily and quickly based on immediate user feedback. FDD also allows for faster delivery of useful software to its users, which itself allows for the aforementioned faster user feedback and fulfilment of  the user’s requirements. Thus, it avoids significant cost, sometimes related to other development processes, when the request to modify a requirement came late. Having a requirement modification applied in the beginning of the interaction with the user has a cost that is considerable less than having the same modification done at the maintenance time. Furthermore, it’s easier to express an existing reality, that is visible and which we could interact with, than only a conceptual idea of a particular solution.

This is in stark contrast to more sequential, plan-driven methodologies, such as the [Waterfall method](https://en.wikipedia.org/wiki/Waterfall_model) or the [Spiral Model](https://en.wikipedia.org/wiki/Spiral_model), which demand for separate and distinct phases of specification and development. This type of methodologies often have trouble accommodating change after the development process is underway, which raises significant issues when an earlier part of the project has to be altered to meet any changes in the user requirements, leading to later phases of the project having to be scrapped and reworked altogether due to their reliance on the changed earlier phase. 

However, plan-driven methodologies often result in cleaner code and a stronger system structure, which allows applications developed under these methods to have significantly less technical debt. Due to the constantly changing system structure applications developed under incremental development methodologies need to have in order to allow for the gradual introduction of features, system structure tends to degrade with each new increment, leading to overall more technical debt and the need to refactor code more frequently, which becomes increasingly difficult over time.

It's also important to note that [reuse-oriented software engineering methodologies](http://searchsoftwarequality.techtarget.com/definition/reuse-oriented-model) are not as commonly used in open-source projects as other methods tend to be, since the goal with these projects is often to create a new application from scratch on the back of an original idea, which doesn’t lend itself into reusing other components available and that, since this is an open-source project being developed under no costs whatsoever, [software prototyping methodologies](https://en.wikipedia.org/wiki/Software_prototyping), ideal to keep costs lower through prototyping and user feedback, don't bring any benefits to the project that plan-driven methodologies don't already do.

To conclude, given the project’s smaller scope, and the approach taken by the developer throughout Cleaver’s development, an incremental development software process such as FDD seems to have been the ideal choice for the project, allowing for the gradual introduction of features requested by users while keeping its technical debt in check for the most part due to the project’s small scale and overall low amount of code to maintain.

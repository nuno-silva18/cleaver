# Cleaver

## Table of Contents
* [Cleaver](#cleaver)
    * [Software Maintainability](#softwareMaintainability)
        * [Analyzing Cleaver's Code](#ancode)
        * [Analyzing Better Code Hub's Results] (#anbch)
    * [Feature Evolution Process](#evoproc)
        * [Feature Identification and Reasoning for Evolution](#featidreason)
        * [Evolving the Feature](#featevo)
        * [Testing the Feature](#featuretest)
        * [Pull Request](#featurepull)
    * [Contribution of Team Members](#contributions)

<div id='softwareMaintainability'>

## Software Maintainability

<div id='ancode'>

### Analyzing Cleaver's Code

<div id='anbch'>

### Analyzing Better Code Hub's Results

<div id='evoproc'>

## Feature Evolution Process

<div id='featidreason'>

### Feature Identification and Reasoning for Evolution

In order to identify what feature to add to Cleaver, we analyzed [Cleaver's issue tracker](https://github.com/jdan/cleaver/issues) in order to determine what feature requests had users of the application made. We found [several](https://github.com/jdan/cleaver/issues/130) [feature](https://github.com/jdan/cleaver/issues/129) [requests](https://github.com/jdan/cleaver/issues/107), but the [one that we decided to evolve](https://github.com/jdan/cleaver/issues/128) was one we felt was essential for a program of Cleaver's nature. Being able to dynamically make changes to your theme is an integral part of the worflow for any user who wants additional control over their own slides, as having to reload the application each time a change is made is time-consuming and fairly incovenient, particularly on slower personal computers. With this feature, users can make changes to their themes on the fly without having to reload Cleaver, which should user productivity immensely.

<div id='featevo'>

### Evolving the Feature

Once we identified the feature we wanted to evolve, we decided to go over Cleaver's code to identify where and what code we needed to change/add to implement our feature. We found that Cleaver already did something similar to the feature requested but at a smaller scale: Cleaver was able to track changes to the presentation file given and a single css file, but not to a theme's files, through the use of the inline command `cleaver --watch`. The code for this command is the following:

<img src="./images/cleaver-watch-code.png" />

Developing our feature using the code developed for this command was fairly straightforward: We simply added a check to make sure the theme specified was local (as the feature requested specified watching for changes on local themes), got all the files in the local theme's directory and used JavaScript's `watchFile()` function to watch for changes on each of the files in the local theme's directory. The code developed for this feature is the following:

<img src="./images/Deployment View.png" />


**[Link to pull request](https://github.com/jdan/cleaver/pull/160)**

<div id='contributions'>

## Contribution of Team Members

| Team member | Contribution |
| ----------  | ------------ |
| André Correia | [Software Testability and Reviews](#testandrevintro) |
| João Mendonça | [Bug and Correction](#bugandfix) |
| Luís Couto | [Bug and Correction](#bugandfix) | 
| Nuno Silva | [Feature Evolution Process](#evoproc) |

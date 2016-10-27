# Cleaver

## Table of Contents
* [Cleaver](#cleaver)
    * [Requirements](#introreq)
        * [Specific Requirements and Features](#specreqandfeat)
        * [Use Cases](#usecases)
        * [Domain Model](#domainmodel)

<div id='introreq'>

## Requirements

<div id='specreqandfeat'>

## Specific Requirements and Features

### Functional Requirements
* Creates HTML presentations from Mardown language;
* Provides users with the ability to easily share a presentation online. It’s also possible to print the presentation to a PDF;
* Author credits supports several fields like name, url to author’s website, email, twitter and other social media accounts. It creates a basic author credits slide at the end of the presentation;
* Supports several options for adding customization to presentations. These options, placed at the top of the document, are in YAML format;
* Provides theme support. Gives an easy way to plug styles, scripts and templates into presentations. The main goal is to bring more fine-grained control over presentation. Instead of manually specifying a stylesheet, template, layout and others it’s possible to specify a single theme containing each of these assets. More specifically, a theme may contain:
   * style.css - styles for presentation;
   * template.mustache - a template used to render the slides in the presentation;
   * layout.mustache - a template used to render the entire document of presentation;
   * script.js - javascript to be included in slideshow.
* Themes may be specified by one of the following options:
   * An absolute or relative path to a directory;
   * An URL to a directory;
   * A github repostitory in the form of username/reponame.
* An option determining whether or not want to render simple navigation buttons on the presentation (by default this value is true). To navigate the slideshow it’s possible to use keyboard too;
* An option determining whether or not want to render a progress bar on slides (by default this value is true);
* Full screen support.

### Non-Functional Requirements
* Easy utilization;
* Simple syntax;
* Make presentations compatible with several devices including mobile devices;
* No need to learn a new programming language;
* No need to install new software;
* Encoded in UTF-8.

<div id='usecases'>

## Use Cases
* As a user i want to change options so i can customize the look and feel of my presentation, including author info, stylesheets, and custom templates.
* As a user i want to be able to add my own themes so i can make the slides my own
* As a user i want to be able to navigate through my presentation with keyboard buttons so i can easily move throughs slides
<img src="./images/use_case_diagram.png"/>




<div id='domainmodel'>

## Domain Model

The domain model for Cleaver is relatively simple, with its conceptual classes mostly consisting of a **Core** class representing the application itself and a **Theme** class, representing the theme plugin supported by the application:

<img src="./images/domainmodel.png" />

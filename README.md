# Learning AngularJS

Thoughts and Notes on learning AngularJS, especially from a Java background.

## Overview

* While I am a polyglot software developer, much of my time in the last fifteen years has been spent doing Java.
* AngularJS is interesting to me, and I'm starting to learn it.
* I find the "state of the art" with AngularJS (and other Javascript frameworks for single-page apps) much less mature...or maybe I haven't been looking in the right places?
* This is a place to capture questions, thoughts, and lessons learned

## Topics

* The Code
    * Style
    * Modularity & Code organization
* Testing
    * Frameworks
    * Running
    * Mocking
* Building and deploying
* Other frameworks to leverage
* Browser Issues
* Tutorials/Learning
* What Have I forgotten?

## The Code

### Style

["That wasn't flying, it was falling with style."+](http://www.youtube.com/watch?v=DwN6efmhp7E)

We've got [JShint](http://www.jshint.com/install/). 
We've got [JSLint](http://www.jslint.com).

Any other style tools?

Which do you use and how do you integrate it into your process? Grunt?

\+ http://www.youtube.com/watch?v=2VSYmGSJtCA

### Modularity & Code organization

What's the right way to organize the code? Small projects don't matter so much, but large projects will care a lot... For example, this seems like a thoughtful discussion of the issues: http://cliffmeyers.com/blog/2013/4/21/code-organization-angularjs-javascript

How do you organize your code so it's testable and also ready for production use?
How do you package things up?

## Testing

### Frameworks

For unit testing, the tutorial uses [Jasmine](http://pivotal.github.io/jasmine/). What do you use?

For end-to-end tests, the tutorial uses Angular's end-to-end runner. However, [Angular's own docs](http://docs.angularjs.org/guide/dev_guide.e2e-testing) say consider using [Protractor](https://github.com/angular/protractor) instead. Which do you use (or what do you use) and why?

### Running

The tutorial uses [Karma](http://karma-runner.github.io/0.8/index.html) with node. What do you use?

### Mocking

TODO

## Building and Deploying

I've begun looking at (grunt)[http://gruntjs.com]. Seems like it does a lot. Don't yet understand the production use case model.

Other tools you use in addition or instead of grunt?

## Other frameworks to leverage

TODO

## Browser Issues

TODO

## Tutorials/Learning

The official tutorial is the place to start: http://docs.angularjs.org/tutorial

Where after that?

## What Have I forgotten?

TODO

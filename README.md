# Learning AngularJS

Thoughts and Notes on learning AngularJS, especially from a Java background.

## Overview

* While I am a polyglot software developer, much of my time in the last fifteen years has been spent doing Java.
* AngularJS is interesting to me, and I'm starting to learn it.
* I find the "state of the art" with AngularJS (and other Javascript frameworks for single-page apps) much less mature...or maybe I haven't been looking in the right places?
* This is a place to capture questions, thoughts, and lessons learned

## Topics

* The Code
    * Modularity & Code organization
    * Style
* Tutorials/Learning
* Testing
    * Frameworks
    * Running
    * Mocking
* Avoiding missing code/resouces at runtime
* Other frameworks to leverage
* Browser Issues

## Tutorials/Learning

The official tutorial is the place to start: http://docs.angularjs.org/tutorial

Where after that?

## The Code

### Modularity & Code organization

For example, this seems like a thoughtful discussion of the issues:

http://cliffmeyers.com/blog/2013/4/21/code-organization-angularjs-javascript

What's the right way to organize the code? Small projects don't matter so much, but large projects will care a lot...

### Style

["That wasn't flying, it was falling with style."](http://www.youtube.com/watch?v=DwN6efmhp7E)

We've got [js-hint](http://www.jshint.com/install/). 
We've got [JSLint](http://www.jslint.com).

Any other style tools?

Which do you use and how do you integrate it into your process?


## Testing

### Frameworks

For unit testing, the tutorial uses Jasmine. What do you use?

For end-to-end tests, the tutorial uses Angular's end-to-end runner. However, [Angular's own docs](http://docs.angularjs.org/guide/dev_guide.e2e-testing) say consider using [Protractor](https://github.com/angular/protractor) instead. Which do you use (or what do you use) and why?

### Running

The tutorial uses Karma with node. What do you use?

### Mocking

TODO

## Avoiding missing code/resouces at runtime

TODO

## Other frameworks to leverage

TODO

## Browser Issues

TODO

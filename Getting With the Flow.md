# Getting With the Flow

There's a lot to learn with Angular. We spent time talking at the Angular Lunch on 2014-01-15 about a lot of the things which impede getting down to the serious business of learning Angular. These notes try to capture the essence of our conversation, so others can get into "flow" with learning Angular.

## Raw notes

* JSHint - lets you disagree with Doug C. if you want

Learning resources
* Best Angular book? No.
* "AngularJS fundamentals" on pluralsight
* "AngularJS best practices" on pluralsight
* AngularJS best practices on YouTube from angular meetup - but know it's out-of-date
* Egghead.io videos - very good; worth the cost


* Alternatives to grunt - brunch and gulp
* grunt
  is 0.4.x and it shows - need tons of plug-ins and they frequently break
  some things it does quite well
    running JSHint
    watching in background to refresh browser
  prefer the "official" grunt-contrib* ones (more likely to be stable & correct)
* code modularization
	angular-seed was a terrible failure
	Kyle - pretend you're using java and pretend that that angular module name has to match the file name.
        ./my/cool/Module.js -> my.cool.Module <- entire module
* build process
	"building is suffering" -- Kyle :-)
* Use a grunt plug-in to bundle up all the templates and populate the cache by URI so you don't end up with stale templates
* CSS, index.html, all the app javascript in one file, all the 3rd part javascript in one other file
* The file names include a hash/version to avoid browser caches from delivering an old file. - break it down by groups of things you think will be changing or not changing
* Performance issues seem to arise more from old browswers than from pulling down the app files
* Pay no attention to the chrome browser when running unit tests. DON'T TOUCH IT!
* Some use PhantomJS - Poltergeist gave them problems
  sometimes Phantom fails when something is in front of a button and clicks through to the button
* Don't use Angular's end-to-end runner.
  Protractor not quite ready? But this is where a lot of energy is focused.
  End-to-end will get messed up by having polling in the background
  Capybara - ruby thing so not as relevant unless coming from Rails
* CORS - cross-origin resource sharing
   4/5 headers you have to get right
   browsers do "horribly toxic caching of them"
   works fine once you get it right
* Common to have index.html on site where services
* grunt-ng-min - need to run before minification or angular injection will bust

Doesn't run with scissors
* Twitter Bootstrap
    Twitter Bootstrap + ui-bootstrap + angular-strap + others?
    You can do a lot with just Twitter Bootstrap

* Always test on every browser you want to let users run
* Try to avoid IE 8, as it requires hacks (documented) and next major version will drop support.

Directives
* If you're going to make a directive, make the simplest one you can. As in write a directive that has ZERO logic and some static HTML and then go from there.

Directives that create widgets
Directives that add event handling
Directives that break up a large page into sections

Directives that are to wrap up DOM manipulation versus wrapping up a chunk of your app as a directive.


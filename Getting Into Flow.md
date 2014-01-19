# Getting Into Flow

There's a lot to learn with Angular. We spent time talking at the Angular Lunch on 2014-01-15 about a lot of the things which impede getting down to the serious business of learning Angular. These notes try to capture the essence of our conversation, so others can get into "flow" with learning Angular.

## Style and Organization

### Style

Use a style checker. You can use [JSLint](http://www.jslint.com) if you are okay having Doug Crockford define good style (and change his mind). If you want to be able to alter the checking to match your sensibilities, use [JSHint](http://www.jshint.com).

### Organization

Kyle Cordes suggests you pretend you're using Java and make the file path and file name the same as the module name. For example, if you have a module named 'my.cool.Module', then you want ./my/cool/Module.js to contain that module.

## Keeping things moving

Automate the things you can. For example, you don't want the files in your browser to get out-of-date with what you've written. You don't want to have to run minification yourself. You don't want to do anything by hand you can automate.

There are several tools to do this sort of thing, amongst them grunt, brunch, and gulp. Right now many people like to use grunt, though even it is currently at version 0.4.x and not really mature. Be aware if using grunt that you end up needing lots of plug-ins and they frequently break. It seems the "official" (grunt-contrib*) plug-ins are more likely to be stable and correct.

Grunt does seem to do a good job of automatically running JSHint/JSLint and watching in the background for changes to refresh the files in the browser.

## Avoiding out-of-date templates

Browsers will cache, sometimes aggressively. To avoid having some tempaltes get updated and others be older, cached versions, you can use a grunt plug-in to bundle up all the templates and populate the browser cache by URI in one go. This way you don't end up with a mix of old and new.

## Bundling up files

In general, you want to bundle files likely to change together. For example, you can package all the third-party Javascript in one file (use grunt to concatenate them together).

If your application is small enough, you can concatenate all your code into one file. Make sure to use a hash or version number in the file, so that aggressive browser caching doesn't result in a disconnect between your code and other things you depend upon (such as your third-party javascript).

For larger applications, break up the code into groups where it's more likely changes to code will be contained within a single group (or for really large apps, in a smaller number of groups).

Performance issues seem to arise more from old browsers than from the initial download of the application files, so don't worry about file size until you see it actually manifest as an issue (it probably won't).

## Iterative development

### Leave the Chrome Alone

Jasmine and other testing tools spawn one or more versions of Chrome in which to run their tests. _Don't touch it_. It's not there for you to use, it's not where your test results show up. It's an artifact of the fact that we don't have a good environment to test Javascript code in other than actual browsers (though some people seem to be having success with PhantomJS).

## Raw notes

Learning resources
* Best Angular book? No.
* "AngularJS fundamentals" on pluralsight
* "AngularJS best practices" on pluralsight
* AngularJS best practices on YouTube from angular meetup - but know it's out-of-date
* Egghead.io videos - very good; worth the cost


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


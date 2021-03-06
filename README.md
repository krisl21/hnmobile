Hacker News mobile web app
==========================

**Note**: If you think this README is lame, try this **[awesome landing page](http://cheeaun.github.com/hnmobile/landing/)**.

This is one of my silly mini-projects. I create this initially to try out iOS 5 Mobile Safari's new `-webkit-overflow-scrolling: touch` CSS support. I need some sort of content for scrolling, so why not [Hacker News](http://news.ycombinator.com/)' stories? I'm also trying something called [**Fake it 'til you make it**](http://snook.ca/archives/conferences/fake-it) which I make the web app looks (and feels) like a native mobile app. In this case, like a native iOS app.

As I continue developing this app, it turns out pretty good. Currently it has **very basic** features:

- View 'front page' stories from Hacker News.
- View individual story with all its comments, threaded.

Here are some screenshots. Click to see them in their full **retina** glory.

[![Screenshot 1](https://github.com/cheeaun/hnmobile/raw/master/screenshots/screenshot1.png)](https://github.com/cheeaun/hnmobile/raw/master/screenshots/screenshot1@2x.png)

[![Screenshot 1](https://github.com/cheeaun/hnmobile/raw/master/screenshots/screenshot2.png)](https://github.com/cheeaun/hnmobile/raw/master/screenshots/screenshot2@2x.png)

Technical stuff
---------------

This mobile web app primarily works on iOS 5 Mobile Safari. It uses these wonderful scripts:

- [Tappable](https://github.com/cheeaun/tappable) - touch-friendly tap events
- [Director](https://github.com/flatiron/director) - location.hash router
- [Hogan.js](https://github.com/twitter/hogan.js) - logic-less templating
- [Amplify.Store](http://amplifyjs.com/api/store/) - client-side storage
- [Viper](https://github.com/alpha123/Viper/) - simple animation
- Vanilla JavaScript - everything else

Also uses the [unofficial Hacker News API](http://node-hnapi.herokuapp.com/), [open-sourced](https://github.com/cheeaun/node-hnapi).

More technical stuff
-----------------------

### Running a local server

	git clone git@github.com:cheeaun/hnmobile.git
	cd hnmobile
	node server.js -noappcache

The `-noappcache` argument is to prevent browsers from caching everything in the Application Cache.

### Changes to scripts

If there are changes in the `/js` folder, run this to regenerate `scripts.js` (skip the npm install if `uglify-js` is already installed):

	npm install uglify-js
	node make-scripts.js

### Changes to templates

If there are changes in the `/templates` folder, run this to regenerate `templates.js` (skip the npm install if `uglify-js` and `hogan.js` are already installed):

	npm install uglify-js
	npm install git://github.com/twitter/hogan.js.git
	node make-templates.js

Contributing and Feedback
-------------------------

Feel free to fork, file some issues or [tweet your feedback](http://twitter.com/cheeaun) to me.

License
-------

Licensed under the [MIT License](http://cheeaun.mit-license.org/).

Other similar apps
------------------

This is the not the first third-party app for Hacker News. Others have tried doing the same thing, despite some slight differences. I've compiled [a list of apps here](https://github.com/cheeaun/hnmobile/wiki/Hacker-News-apps).
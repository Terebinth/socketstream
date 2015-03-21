![SocketStream!](https://github.com/socketstream/socketstream/raw/master/new_project/client/static/images/logo.png)

# SocketStream
[![Build Status](https://api.travis-ci.org/socketstream/socketstream.svg?branch=master)](https://travis-ci.org/socketstream/socketstream) [![Dependency Status](https://david-dm.org/socketstream/socketstream.svg)](https://david-dm.org/socketstream/socketstream#info=dependencies) [![devDependency Status](https://david-dm.org/socketstream/socketstream/dev-status.svg)](https://david-dm.org/socketstream/socketstream#info=devDependencies) [![Code Climate](https://codeclimate.com/github/socketstream/socketstream.svg)](https://codeclimate.com/github/socketstream/socketstream) [![Codacy Badge](https://www.codacy.com/project/badge/802df47157c84beca4c3dbcda76bc553)](https://www.codacy.com/public/paulbjensen_2636/socketstream) [![NPM version](https://badge.fury.io/js/socketstream.svg)](http://badge.fury.io/js/socketstream) [![Gitter chat](https://badges.gitter.im/socketstream.svg)](https://gitter.im/socketstream/socketstream)
[![Issue Stats](http://issuestats.com/github/socketstream/socketstream/badge/pr)](http://issuestats.com/github/socketstream/socketstream)
[![Issue Stats](http://issuestats.com/github/socketstream/socketstream/badge/issue)](http://issuestats.com/github/socketstream/socketstream)
[![Coverage Status](https://img.shields.io/coveralls/socketstream/socketstream.svg)](https://coveralls.io/r/socketstream/socketstream?branch=master)


### Introduction

SocketStream is a framework for Realtime Web Apps

_Latest release: 0.3.11 ([view changelog](https://github.com/socketstream/socketstream/blob/master/HISTORY.md))_

[Live demo](http://demo.socketstream.com) | [Documentation](http://socketstream.github.io/socketstream/docs/)

### Installation

    npm install -g socketstream

### Usage

    socketstream new <your_app_name>
    cd <your_app_name>
    npm install
    npm start

Then open a web browser at localhost:3000:

    open http://localhost:3000

### Why SocketStream?

Building a simple chat app that uses websockets is easy, but rich, non-trivial, responsive realtime UI without ending up with a mess of code is hard SocketStream eases the pain by:

* Integrating best-of-breed modules to increase productivity
* Providing a sensible place to put everything
* Accelerating development with Live Reload and (optional) support for Stylus, Jade, and other transpilers.
* Accelerating deployment with integrated asset packing and CDN support
* Organizing spaghetti client-side code into modules you can `require()` with Browserify
* Working well with all major client-side frameworks (e.g. Backbone, Ember, Angular)

### Applications using SocketStream

- [Dashku](https://github.com/Anephenix/dashku): Realtime dashboards and widgets using HTML, CSS and JavaScript. Also hosted at [dashku.com](https://dashku.com).
- [SketchDeck](http://sketchdeck.com): An app for designing great slide decks from sketches, also a Y Combinator tech startup.
- [Hollow](http://hollowdocumentary.com/): An interactive, emmy-nominated documentary.
- [Bitjoy](http://bitjoy.org/): Realtime Bitcoin prices and news.
- [Teeleader](http://www.teeleader.com): A booking engine for Golf courses.

### Presentations

- SocketStream (November 2013): On [Slideshare](http://www.slideshare.net/paulbjensen/socketstream-28194445) and [SpeakerDeck](https://speakerdeck.com/paulbjensen/socketstream).

### Videos

(most recent at end)

* [KrtConf.com, Portland, November 2011](http://2011.krtconf.com/videos/owen_barnes)
* [LNUG.org, London, May 2012](http://vimeo.com/43027679)
* [LXJS, Lisbon, September 2012](http://www.youtube.com/watch?v=LOS1lpWXphs)
* [RealtimeConf, Portland, October 2012](http://2012.realtimeconf.com/video/owen-barnes)
* [QCon, San Francisco, November 2012](http://www.infoq.com/presentations/SocketStream)
* [RealtimeConf EU, Lyon, April 2013](https://www.youtube.com/watch?v=76ZSp3OtCTM)

### Documentation

Checkout the [documentation here](http://socketstream.github.io/socketstream/docs/#/tutorials).

### Next Major Release 0.4

[![Build Status](https://api.travis-ci.org/socketstream/socketstream.svg?branch=next)](https://travis-ci.org/socketstream/socketstream)
[![Coverage Status](https://coveralls.io/repos/socketstream/socketstream/badge.svg?branch=next)](https://coveralls.io/r/socketstream/socketstream?branch=next)

#### Notes

The way views are served has been updated. The *default bundling of assets* is largely as before, but some details have changed. The major change is that the bundler of a client definition can be changed. You can configure this on a per definition basis. For more information look in the tutorial section.

Please note that due to the changes, however carefully they have been done, you should not deploy this release in production. We expect to find issues and fix those in a maintenance release 0.4.1, which can hopefully be considered fit for production. However, if you are developing and your next deployment is a couple of months off, it is a great time to upgrade to version 0.4.

If you are used to web app development you will know *Bower*. In this version we have made improvements to work better with Bower. The most obvious one is you can now define your client assets using relative paths within the client. So if you put `bower_components` in the client directory you can refer to them in the definition by `"./bower_components/<module>/<file>.js"`.

Changes to consider when upgrading

* You can make your own custom bundler
* CSS files can reference images and other assets using relative paths in development and production
* You can refer to Bower components in your definition
* JSON shim dropped. To support IE6/7 you must manage it yourself.
* `client.id` is unique and not a plain timestamp
* Plugins should use the new log interface on `ss.log`.
* You can load npm modules in the client by maintaining node_modules in the client directory.
* You can configure global constants to be shared between the client definition and browser code.
* By default the initCode for a view is executed at the end of the body independent of the SocketStream tag.

This upcoming is expected in April. The current state can be found on the `next` branch.


### Team

*Creator:* Owen Barnes


*Core Contributors:* 

- Paul Jensen
- Roman Minkin
- Robert Hall
- Joshua Cullick
- Henrik Vendelbo

### Contact

- Twitter: [@socketstream](http://twitter.com/#!/socketstream)  
- Chat: [Gitter](https://gitter.im/socketstream/socketstream)
- Forum: [Google Group](http://groups.google.com/group/socketstream)

### License

SocketStream is released under the MIT license.

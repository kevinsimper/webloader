## webloader

A minimal web asset loader

It determines the right way to load the asset based on the file ending


### Usage

```
var webloader = require('webloader');

var background = webloader.load('images/background.png')
	.on('progress', function(progress) {

	})
	.on('complete', function(files) {

	})
	.on('fail', function(errors) {

	});
```

## API

### webloader.load(files [, complete])

 - files - [string, array]: can either be a string or an array of files that
   needs to be preloaded
 - complete - [function]: Will be called when all the assets has been loaded

```
webloader.load('sounds/raygun.mp3')
```
```
webloader.load(['sounds/raygun.mp3', 'sounds/collision.mp3']);
```

### Event: 'progress'
### Event: 'complete'
### Event: 'fail'

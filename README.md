#resourceful-mongo

A MongoDB engine for [resourceful](https://github.com/flatiron/resourceful/), a datamapper part of the [flatiron](https://github.com/flatiron/) framework.

#### Credits 

Ryan Fitzgerald, Follow [@TheRyanFitz on Twitter](http://twitter.com/#!/TheRyanFitz).

## Example

``` js
  var resourceful = require('resourceful');
  require('resourceful-mongo');
  
  var Person = resourceful.define('person', function () {
    //
    // Specify a storage engine
    //
    this.use('mongo', {
      collection: "people" // collection must always be set when using the mongo engine
    });

	this.string('name');
   	this.number('age');
  });
```

## Installation

### Installing npm (node package manager)
``` bash
  $ curl http://npmjs.org/install.sh | sh
```

### Installing resourceful
``` bash 
  $ [sudo] npm install resourceful-mongo
```

## Tests
All tests are written with [mocha][0] and should be run with [npm][1]:

``` bash
  $ npm test
```

#### Author: [Ryan Fitzgerald](http://twitter.com/#!/TheRyanFitz)
#### License: [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0)

[0]: http://visionmedia.github.com/mocha/
[1]: http://npmjs.org
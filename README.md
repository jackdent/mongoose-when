mongoose-when
============

Add jquery style .when support to mongoose promise object. Requires mongoose v3.6.1 or higher, no other requirements.

Use exactly like jquery.when on which this code is based. http://api.jquery.com/jQuery.when/

Promise.when() returns a Mongoose promise object.

```javascript
var mongoose = require('mongoose');
var Promise = mongoose.Promise;

var p1 = Users.find().exec();
var p2 = Animals.find().exec();
Promise.when(p1, p2).addBack(function(err, users, animals) {
  //etc
});
```

See unit tests for for more usage examples.
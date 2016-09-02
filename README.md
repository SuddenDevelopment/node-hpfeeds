# node-hpfeeds
nodejs lib for subscribing to hpfeeds channels and using a callback for events

Example use
```javascript
'use strict';

//the function to use as a callback
var onMsg=function(strChannel,objMessage){
  console.log(strChannel);
  console.log(objMessage);
};

var HPC = require('./HPC.js').HPC;
//var HPC = function(host, port, ident, secret, csv channels, msgcallback) {
var hpfeed = new HPC('hoststring',123456, 'username','password','csv,of,channels',onMsg);

```
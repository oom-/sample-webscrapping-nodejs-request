# Sample
```js
let fs = require('fs');
let REQUEST = require('request');
const jsdom = require("jsdom");
const { JSDOM } = jsdom;

var options = { gzip: true, jar: true };
options.method = "GET";
options.url = "https://www.google.com";
REQUEST(options, (err, res, body) => {
    var { window } = new JSDOM(body);
    var $ = require('jquery')(window);
    var links_on_page = $('a');
});
```

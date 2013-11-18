# Deep Watch

Exactly like fs.watch, but with sub-directory support.

## Example:

```js
var DeepWatch = require('deep-watch')

var dw = new DeepWatch({
  exclude: ['node_modules'],
  callback: function(event, filename) {
    if (filename == 'foo/bar/index.html') this.stop()
  }
})

dw.start()
```

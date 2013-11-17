# Deep Watcher

Exactly like fs.watch, but with sub-directory support.

## Example:

```js
var DeepWatcher = require('deep-watcher')

var dw = new DeepWatcher({
  exclude: ['node_modules'],
  callback: function(event, filename) {
    if (filename == 'foo/bar/index.html') this.stop()
  }
})

dw.start()
```

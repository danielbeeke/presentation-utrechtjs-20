###  Add plugin

Dynamic imports via System.import.<br>
Plugins may come from the core or from somewhere else.

```
addPlugin (pluginUri, config) {
  return new Promise((resolve) => {
    if (pluginUri.substr(0, 4) != 'http') {
      pluginUri = '/plugins/' + pluginUri;
    }

    System.import(pluginUri + '/plugin.js').then((plugin) => {
      var newPlugin = new plugin.default(this, config);
      this.plugins[newPlugin.getName()] = newPlugin;
      this.emit('pluginAdded', newPlugin.getName(), newPlugin);
      resolve();
    });
  });
}
```
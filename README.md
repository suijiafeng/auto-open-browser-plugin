# Auto Open Browser Plugin
Opens a new browser tab when Webpack loads. Very useful if you're lazy and don't want to force yourself to open a new tab when Webpack is ready to play!

## Installation

```
npm install auto-open-browser-plugin --save-dev
```

## Usage

Simply require the plugin and add it in the **plugins** section:

```javascript
var OpenBrowserPlugin = require('auto-open-browser-plugin');

module.exports = {
  entry: path.resolve(__dirname, 'lib/entry.js'),
  output: {
    path: __dirname + "/bundle/",
    filename: "bundle.js"
  },
  plugins: [
    new OpenBrowserPlugin({ url: 'http://localhost:3000' })
  ]
};
```

## Options

#### url

Type: `String`<br>
Default: `http://localhost:8080`

Url to open when Webpack is ready. Needs to have the prefix `http://` or `https://` in order to open the browser.

## License

MIT License.

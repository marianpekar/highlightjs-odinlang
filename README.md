# [Highlight.js](https://highlightjs.org/) syntax definition for [Odin](https://odin-lang.com/) programming language

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### Static website or simple usage

Simply load the module after loading Highlight.js. You'll use the minified version found in the `dist` directory. This module is just a CDN build of the language, so it will register itself as the Javascript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" src="/path/to/highlightjs-odin/dist/odin.min.js"></script>
<script type="text/javascript">
  hljs.highlightAll();
</script>
```

### Using directly from the [UNPKG](https://unpkg.com) CDN

#### Common JS

```html
<link rel="stylesheet" href="https://unpkg.com/@highlightjs/cdn-assets@11.11.1/styles/default.min.css">
<script type="text/javascript" src="https://unpkg.com/@highlightjs/cdn-assets@11.11.1/highlight.min.js"></script>
<script type="text/javascript" src="https://unpkg.com/highlightjs-odinlang@1.4.0/dist/odin.min.js"></script>
```

#### ES6 Modules

```html
<link rel="stylesheet" href="https://unpkg.com/@highlightjs/cdn-assets@11.11.1/styles/default.min.css">
<script type="module">
import hljs from 'https://unpkg.com/@highlightjs/cdn-assets@11.11.1/es/highlight.min.js';
import hljsOdin from 'https://unpkg.com/highlightjs-odinlang@1.4.0/dist/odin.es.min.js';
hljs.registerLanguage('odin', hljsOdin);
</script>
```

### With Node or another build system

If you're using Node / Webpack / Rollup / Browserify, etc, simply require the language module, then register it with Highlight.js.

```javascript
var hljs = require('highlight.js');
var hljsOdin = require('highlightjs-odinlang');

// or with ES modules
import hljs from 'highlight.js';
import hljsOdin from "highlightjs-odinlang"

hljs.registerLanguage("odin", hljsOdin);
hljs.highlightAll();
```


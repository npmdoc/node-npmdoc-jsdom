# api documentation for  [jsdom (v9.12.0)](https://github.com/tmpvar/jsdom#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jsdom.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jsdom)
#### A JavaScript implementation of the DOM and HTML standards

[![NPM](https://nodei.co/npm/jsdom.png?downloads=true)](https://www.npmjs.com/package/jsdom)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jsdom/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jsdom_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jsdom/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-jsdom/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "browser": {
        "canvas": false,
        "vm": "./lib/jsdom/vm-shim.js"
    },
    "bugs": {
        "url": "https://github.com/tmpvar/jsdom/issues"
    },
    "dependencies": {
        "abab": "^1.0.3",
        "acorn": "^4.0.4",
        "acorn-globals": "^3.1.0",
        "array-equal": "^1.0.0",
        "content-type-parser": "^1.0.1",
        "cssom": ">= 0.3.2 < 0.4.0",
        "cssstyle": ">= 0.2.37 < 0.3.0",
        "escodegen": "^1.6.1",
        "html-encoding-sniffer": "^1.0.1",
        "nwmatcher": ">= 1.3.9 < 2.0.0",
        "parse5": "^1.5.1",
        "request": "^2.79.0",
        "sax": "^1.2.1",
        "symbol-tree": "^3.2.1",
        "tough-cookie": "^2.3.2",
        "webidl-conversions": "^4.0.0",
        "whatwg-encoding": "^1.0.1",
        "whatwg-url": "^4.3.0",
        "xml-name-validator": "^2.0.1"
    },
    "description": "A JavaScript implementation of the DOM and HTML standards",
    "devDependencies": {
        "benchmark": "1.0.0",
        "browserify": "^14.0.0",
        "chai": "^3.5.0",
        "colors": "^1.1.2",
        "eslint": "^3.14.1",
        "eslint-plugin-html": "^2.0.0",
        "fs-readdir-recursive": "^1.0.0",
        "http-server": "^0.9.0",
        "karma": "^1.4.1",
        "karma-browserify": "^5.1.1",
        "karma-chrome-launcher": "^2.0.0",
        "karma-mocha": "^1.3.0",
        "karma-mocha-webworker": "^1.3.0",
        "karma-sauce-launcher": "^1.1.0",
        "mocha": "^3.2.0",
        "mocha-sugar-free": "^1.3.1",
        "nodeunit": "0.10.2",
        "optimist": "0.6.1",
        "portfinder": "^1.0.12",
        "q": "^1.4.1",
        "selenium-standalone": "^6.0.0",
        "server-destroy": "^1.0.1",
        "st": "^1.2.0",
        "watchify": "^3.9.0",
        "wd": "^1.1.3",
        "webidl2js": "^5.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "e8c546fffcb06c00d4833ca84410fed7f8a097d4",
        "tarball": "https://registry.npmjs.org/jsdom/-/jsdom-9.12.0.tgz"
    },
    "gitHead": "e0687795456773058755867e53c487aa3fe80e5b",
    "homepage": "https://github.com/tmpvar/jsdom#readme",
    "keywords": [
        "dom",
        "html",
        "whatwg",
        "w3c"
    ],
    "license": "MIT",
    "main": "./lib/jsdom",
    "maintainers": [
        {
            "name": "tmpvar",
            "email": "tmpvar@gmail.com"
        },
        {
            "name": "domenic",
            "email": "domenic@domenicdenicola.com"
        },
        {
            "name": "sebmaster",
            "email": "sebmaster16@gmail.com"
        }
    ],
    "name": "jsdom",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/tmpvar/jsdom.git"
    },
    "scripts": {
        "benchmark": "node ./benchmark/runner",
        "benchmark-browser": "node ./benchmark/runner --bundle",
        "convert-idl": "node ./scripts/webidl/convert",
        "lint": "eslint . && eslint test/web-platform-tests/to-upstream --ext .html",
        "prepublish": "npm run convert-idl",
        "pretest": "npm run convert-idl && git submodule update --init --recursive",
        "test": "npm run test-mocha-all && npm run test-old",
        "test-browser": "npm run test-karma && npm run test-karma-worker && npm run test-browser-old",
        "test-browser-old": "node ./test/browser-runner",
        "test-karma": "karma start test/karma.conf.js",
        "test-karma-worker": "karma start test/karma-webworker.conf.js",
        "test-mocha": "mocha",
        "test-mocha-all": "mocha test/index.js",
        "test-old": "node ./test/runner",
        "test-tuwpt": "mocha test/web-platform-tests/to-upstream.js",
        "test-wpt": "mocha test/web-platform-tests/index.js",
        "update-authors": "git log --format=\"%aN <%aE>\" | sort -f | uniq > AUTHORS.txt"
    },
    "version": "9.12.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jsdom](#apidoc.module.jsdom)
1.  [function <span class="apidocSignatureSpan"></span>jsdom (html, options)](#apidoc.element.jsdom.jsdom)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>blobToBuffer (blob)](#apidoc.element.jsdom.blobToBuffer)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>changeURL (window, urlString)](#apidoc.element.jsdom.changeURL)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>createCookieJar ()](#apidoc.element.jsdom.createCookieJar)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>createVirtualConsole (options)](#apidoc.element.jsdom.createVirtualConsole)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>env ()](#apidoc.element.jsdom.env)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>evalVMScript (window, script)](#apidoc.element.jsdom.evalVMScript)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>getVirtualConsole (window)](#apidoc.element.jsdom.getVirtualConsole)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>jQueryify (window, jqueryUrl, callback)](#apidoc.element.jsdom.jQueryify)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>nodeLocation (node)](#apidoc.element.jsdom.nodeLocation)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>reconfigureWindow (window, newProps)](#apidoc.element.jsdom.reconfigureWindow)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>serializeDocument (doc)](#apidoc.element.jsdom.serializeDocument)
1.  object <span class="apidocSignatureSpan">jsdom.</span>defaultDocumentFeatures

#### [module jsdom.jsdom](#apidoc.module.jsdom.jsdom)
1.  [function <span class="apidocSignatureSpan">jsdom.</span>jsdom (html, options)](#apidoc.element.jsdom.jsdom.jsdom)
1.  [function <span class="apidocSignatureSpan">jsdom.jsdom.</span>env ()](#apidoc.element.jsdom.jsdom.env)
1.  [function <span class="apidocSignatureSpan">jsdom.jsdom.</span>jQueryify (window, jqueryUrl, callback)](#apidoc.element.jsdom.jsdom.jQueryify)



# <a name="apidoc.module.jsdom"></a>[module jsdom](#apidoc.module.jsdom)

#### <a name="apidoc.element.jsdom.jsdom"></a>[function <span class="apidocSignatureSpan"></span>jsdom (html, options)](#apidoc.element.jsdom.jsdom)
- description and source-code
```javascript
jsdom = function (html, options) {
  if (options === undefined) {
    options = {};
  }
  if (options.parsingMode === undefined || options.parsingMode === "auto") {
    options.parsingMode = "html";
  }

  if (options.parsingMode !== "html" && options.parsingMode !== "xml") {
    throw new RangeError('Invalid parsingMode option ${JSON.stringify(options.parsingMode)}; must be either "html", ' +
      '"xml", "auto", or undefined');
  }

  options.encoding = options.encoding || "UTF-8";

  setGlobalDefaultConfig(options);

  // Back-compat hack: we have previously suggested nesting these under document, for jsdom.env at least.
  // So we need to support that.
  if (options.document) {
    if (options.document.cookie !== undefined) {
      options.cookie = options.document.cookie;
    }
    if (options.document.referrer !== undefined) {
      options.referrer = options.document.referrer;
    }
  }

  // List options explicitly to be clear which are passed through
  const window = new Window({
    parsingMode: options.parsingMode,
    contentType: options.contentType,
    encoding: options.encoding,
    parser: options.parser,
    url: options.url,
    lastModified: options.lastModified,
    referrer: options.referrer,
    cookieJar: options.cookieJar,
    cookie: options.cookie,
    resourceLoader: options.resourceLoader,
    deferClose: options.deferClose,
    concurrentNodeIterators: options.concurrentNodeIterators,
    virtualConsole: options.virtualConsole,
    pool: options.pool,
    agent: options.agent,
    agentClass: options.agentClass,
    agentOptions: options.agentOptions,
    strictSSL: options.strictSSL,
    proxy: options.proxy,
    userAgent: options.userAgent
  });

  const documentImpl = idlUtils.implForWrapper(window.document);
  documentFeatures.applyDocumentFeatures(documentImpl, options.features);

  if (options.created) {
    options.created(null, window.document.defaultView);
  }

  if (options.parsingMode === "html") {
    if (html === undefined || html === "") {
      html = "<html><head></head><body></body></html>";
    }

    window.document.write(html);
  } else if (options.parsingMode === "xml") {
    if (html !== undefined) {
      documentImpl._htmlToDom.appendHtmlToDocument(html, documentImpl);
    }
  }

  if (window.document.close && !options.deferClose) {
    window.document.close();
  }

  return window.document;
}
```
- example usage
```shell
...

#### Dealing with asynchronous script loading

If you load scripts asynchronously, e.g. with a module loader like RequireJS, none of the above hooks will really give you what
you want. There's nothing, either in jsdom or in browsers, to say "notify me after all asynchronous loads have completed." The solution
 is to use the mechanisms of the framework you are using to notify about this finishing up. E.g., with RequireJS, you could do

'''js
// On the Node.js side:
var window = jsdom.jsdom(...).defaultView;
window.onModulesLoaded = function () {
  console.log("ready to roll!");
};
'''

'''html
<!-- Inside the HTML you supply to jsdom -->
...
```

#### <a name="apidoc.element.jsdom.blobToBuffer"></a>[function <span class="apidocSignatureSpan">jsdom.</span>blobToBuffer (blob)](#apidoc.element.jsdom.blobToBuffer)
- description and source-code
```javascript
blobToBuffer = function (blob) {
  return Blob.is(blob) && idlUtils.implForWrapper(blob)._buffer || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jsdom.changeURL"></a>[function <span class="apidocSignatureSpan">jsdom.</span>changeURL (window, urlString)](#apidoc.element.jsdom.changeURL)
- description and source-code
```javascript
changeURL = function (window, urlString) {
  const doc = idlUtils.implForWrapper(window._document);

  const url = whatwgURL.parseURL(urlString);

  if (url === "failure") {
    throw new TypeError('Could not parse "${urlString}" as a URL');
  }

  doc._URL = url;
  doc._origin = whatwgURL.serializeURLToUnicodeOrigin(doc._URL);
}
```
- example usage
```shell
...
In the future we may expand 'reconfigureWindow' to allow overriding other '[Unforgeable]' properties. Let us know if you need this
 capability.

#### Changing the URL of an existing jsdom 'Window' instance

At present jsdom does not handle navigation (such as setting 'window.location.href === "https://example.com/"'). However, if you
'd like to change the URL of an existing 'Window' instance (such as for testing purposes), you can use the 'jsdom.changeURL' method
:

'''js
jsdom.changeURL(window, "https://example.com/");
'''

#### Running vm scripts

Although in most cases it's simplest to just insert a '<script>' element or call 'window.eval', in some cases you want access to
 the raw [vm context](https://nodejs.org/api/vm.html) underlying jsdom to run scripts. You can do that like so:

'''js
...
```

#### <a name="apidoc.element.jsdom.createCookieJar"></a>[function <span class="apidocSignatureSpan">jsdom.</span>createCookieJar ()](#apidoc.element.jsdom.createCookieJar)
- description and source-code
```javascript
createCookieJar = function () {
  return new CookieJar(null, { looseMode: true });
}
```
- example usage
```shell
...
'''

- 'config.html': a HTML fragment
- 'config.file': a file which jsdom will load HTML from; the resulting document's URL will be a 'file://' URL.
- 'config.url': sets the resulting document's URL, which is reflected in various properties like 'document.URL' and 'location.href
', and is also used for cross-origin request restrictions. If 'config.html' and 'config.file' are not provided, jsdom will load
HTML from this URL.
- 'config.scripts': see 'scripts' above.
- 'config.src': an array of JavaScript strings that will be evaluated against the resulting document. Similar to 'scripts', but
it accepts JavaScript instead of paths/URLs.
- 'config.cookieJar': cookie jar which will be used by document and related resource requests. Can be created by 'jsdom.createCookieJar
()' method. Useful to share cookie state among different documents as browsers does.
- 'config.parsingMode': either '"auto"', '"html"', or '"xml"'. The default is '"auto"', which uses HTML behavior unless 'config.
url' responds with an XML 'Content-Type', or 'config.file' contains a filename ending in '.xml' or '.xhtml'. Setting to '"xml"'
will attempt to parse the document as an XHTML document. (jsdom is [currently only OK at doing that](https://github.com/tmpvar/jsdom
/labels/x%28ht%29ml).)
- 'config.referrer': the new document will have this referrer.
- 'config.cookie': manually set a cookie value, e.g. ''key=value; expires=Wed, Sep 21 2011 12:00:00 GMT; path=/''. Accepts cookie
 string or array of cookie strings.
- 'config.headers': an object giving any headers that will be used while loading the HTML from 'config.url', if applicable.
- 'config.userAgent': the user agent string used in requests; defaults to 'Node.js (#process.platform#; U; rv:#process.version#)'
- 'config.features': see Flexibility section below. **Note**: the default feature set for 'jsdom.env' does _not_ include fetching
 remote JavaScript and executing it. This is something that you will need to _carefully_ enable yourself.
- 'config.resourceLoader': a function that intercepts subresource requests and allows you to re-route them, modify, or outright
replace them with your own content. More below.
...
```

#### <a name="apidoc.element.jsdom.createVirtualConsole"></a>[function <span class="apidocSignatureSpan">jsdom.</span>createVirtualConsole (options)](#apidoc.element.jsdom.createVirtualConsole)
- description and source-code
```javascript
createVirtualConsole = function (options) {
  return new VirtualConsole(options);
}
```
- example usage
```shell
...
  console.error("script error!!", event.error);
});
'''

it is often also desirable to listen for any script errors during initialization, or errors loading scripts passed to 'jsdom.env
'. To do this, use the virtual console feature, described in more detail later:

'''js
var virtualConsole = jsdom.createVirtualConsole();
virtualConsole.on("jsdomError", function (error) {
  console.error(error.stack, error.detail);
});

var window = jsdom.jsdom(..., { virtualConsole }).defaultView;
'''
...
```

#### <a name="apidoc.element.jsdom.env"></a>[function <span class="apidocSignatureSpan">jsdom.</span>env ()](#apidoc.element.jsdom.env)
- description and source-code
```javascript
env = function () {
  const config = getConfigFromArguments(arguments);
  let req = null;

  if (config.file && canReadFilesFromFS) {
    req = resourceLoader.readFile(config.file,
    { defaultEncoding: config.defaultEncoding, detectMetaCharset: true },
    (err, text, res) => {
      if (err) {
        reportInitError(err, config);
        return;
      }

      const contentType = parseContentType(res.headers["content-type"]);
      config.encoding = contentType.get("charset");
      setParsingModeFromExtension(config, config.file);

      config.html = text;
      processHTML(config);
    });
  } else if (config.html !== undefined) {
    processHTML(config);
  } else if (config.url) {
    req = handleUrl(config);
  } else if (config.somethingToAutodetect !== undefined) {
    const url = URL.parse(config.somethingToAutodetect);
    if (url.protocol && url.hostname) {
      config.url = config.somethingToAutodetect;
      req = handleUrl(config.somethingToAutodetect);
    } else if (canReadFilesFromFS) {
      req = resourceLoader.readFile(config.somethingToAutodetect,
      { defaultEncoding: config.defaultEncoding, detectMetaCharset: true },
      (err, text, res) => {
        if (err) {
          if (err.code === "ENOENT" || err.code === "ENAMETOOLONG") {
            config.html = config.somethingToAutodetect;
            processHTML(config);
          } else {
            reportInitError(err, config);
          }
        } else {
          const contentType = parseContentType(res.headers["content-type"]);
          config.encoding = contentType.get("charset");
          setParsingModeFromExtension(config, config.somethingToAutodetect);

          config.html = text;
          config.url = toFileUrl(config.somethingToAutodetect);
          processHTML(config);
        }
      });
    } else {
      config.html = config.somethingToAutodetect;
      processHTML(config);
    }
  }

  function handleUrl() {
    config.cookieJar = config.cookieJar || exports.createCookieJar();

    const options = {
      defaultEncoding: config.defaultEncoding,
      detectMetaCharset: true,
      headers: config.headers,
      pool: config.pool,
      strictSSL: config.strictSSL,
      proxy: config.proxy,
      cookieJar: config.cookieJar,
      userAgent: config.userAgent,
      agent: config.agent,
      agentClass: config.agentClass,
      agentOptions: config.agentOptions
    };

    const fragment = whatwgURL.parseURL(config.url).fragment;

    return resourceLoader.download(config.url, options, (err, responseText, res) => {
      if (err) {
        reportInitError(err, config);
        return;
      }

      // The use of 'res.request.uri.href' ensures that 'window.location.href'
      // is updated when 'request' follows redirects.
      config.html = responseText;
      config.url = res.request.uri.href;
      if (fragment) {
        config.url += '#${fragment}';
      }

      if (res.headers["last-modified"]) {
        config.lastModified = new Date(res.headers["last-modified"]);
      }

      const contentType = parseContentType(res.headers["content-type"]);
      if (config.parsingMode === "auto") {
        if (contentType.isXML()) {
          config.parsingMode = "xml";
        }
      }
      config.encoding = contentType.get("charset");

      processHTML(config);
    });
  }
  return req;
}
```
- example usage
```shell
...

You can use it with a URL

'''js
// Count all of the links from the io.js build page
var jsdom = require("jsdom");

jsdom.env(
  "https://iojs.org/dist/",
  ["http://code.jquery.com/jquery.js"],
  function (err, window) {
    console.log("there have been", window.$("a").length - 4, "io.js releases!");
  }
);
'''
...
```

#### <a name="apidoc.element.jsdom.evalVMScript"></a>[function <span class="apidocSignatureSpan">jsdom.</span>evalVMScript (window, script)](#apidoc.element.jsdom.evalVMScript)
- description and source-code
```javascript
(window, script) => {
  return script.runInContext(idlUtils.implForWrapper(window._document)._global);
}
```
- example usage
```shell
...

#### Running vm scripts

Although in most cases it's simplest to just insert a '<script>' element or call 'window.eval', in some cases you want access to
 the raw [vm context](https://nodejs.org/api/vm.html) underlying jsdom to run scripts. You can do that like so:

'''js
const script = new vm.Script("globalVariable = 5;", { filename: "test.js" });
jsdom.evalVMScript(window, script);
'''

## jsdom vs. PhantomJS

Some people wonder what the differences are between jsdom and [PhantomJS](http://phantomjs.org/), and when you would use one over
 the other. Here we attempt to explain some of the differences, and why we find jsdom to be a pleasure to use for testing and scraping
 use cases.

PhantomJS is a complete browser (although it uses a very old and rare rendering engine). It even performs layout and rendering,
allowing you to query element positions or take a screenshot. jsdom is not a full browser: it does not perform layout or rendering
, and it does not support navigation between pages. It _does_ support the DOM, HTML, canvas, many other web platform APIs, and running
 scripts.
...
```

#### <a name="apidoc.element.jsdom.getVirtualConsole"></a>[function <span class="apidocSignatureSpan">jsdom.</span>getVirtualConsole (window)](#apidoc.element.jsdom.getVirtualConsole)
- description and source-code
```javascript
getVirtualConsole = function (window) {
  return window._virtualConsole;
}
```
- example usage
```shell
...
  virtualConsole: virtualConsole
});
'''

Post-initialization, if you didn't pass in a 'virtualConsole' or no longer have a reference to it, you can retrieve the 'virtualConsole
' by using:

'''js
var virtualConsole = jsdom.getVirtualConsole(window);
'''

#### Virtual console 'jsdomError' error reporting

Besides the usual events, corresponding to 'console' methods, the virtual console is also used for reporting errors from jsdom itself
. This is similar to how error messages often show up in web browser consoles, even if they are not initiated by 'console.error'.
So far, the following errors are output this way:

- Errors loading or parsing external resources (scripts, stylesheets, frames, and iframes)
...
```

#### <a name="apidoc.element.jsdom.jQueryify"></a>[function <span class="apidocSignatureSpan">jsdom.</span>jQueryify (window, jqueryUrl, callback)](#apidoc.element.jsdom.jQueryify)
- description and source-code
```javascript
jQueryify = function (window, jqueryUrl, callback) {
  if (!window || !window.document) {
    return;
  }

  const implImpl = idlUtils.implForWrapper(window.document.implementation);
  const features = implImpl._features;
  implImpl._addFeature("FetchExternalResources", ["script"]);
  implImpl._addFeature("ProcessExternalResources", ["script"]);

  const scriptEl = window.document.createElement("script");
  scriptEl.className = "jsdom";
  scriptEl.src = jqueryUrl;
  scriptEl.onload = scriptEl.onerror = () => {
    implImpl._features = features;

    if (callback) {
      callback(window, window.jQuery);
    }
  };

  window.document.body.appendChild(scriptEl);
}
```
- example usage
```shell
...

### jQueryify

'''js
var jsdom = require("jsdom");
var window = jsdom.jsdom().defaultView;

jsdom.jQueryify(window, "http://code.jquery.com/jquery-2.1.1.js", function () {
  window.$("body").append('<div class="testing">Hello World, It works</div>');

  console.log(window.$(".testing").text());
});
'''

### Passing objects to scripts inside the page
...
```

#### <a name="apidoc.element.jsdom.nodeLocation"></a>[function <span class="apidocSignatureSpan">jsdom.</span>nodeLocation (node)](#apidoc.element.jsdom.nodeLocation)
- description and source-code
```javascript
nodeLocation = function (node) {
  return idlUtils.implForWrapper(node)[locationInfo];
}
```
- example usage
```shell
...
  </p>');

var bodyEl = document.body; // implicitly created
var pEl = document.querySelector("p");
var textNode = pEl.firstChild;
var imgEl = document.querySelector("img");

console.log(jsdom.nodeLocation(bodyEl));   // null; it's not in the source
console.log(jsdom.nodeLocation(pEl));      // { start: 0, end: 39, startTag: ..., endTag: ... }
console.log(jsdom.nodeLocation(textNode)); // { start: 3, end: 13 }
console.log(jsdom.nodeLocation(imgEl));    // { start: 13, end: 32 }
'''

This returns the [parse5 location info](https://www.npmjs.com/package/parse5#options-locationinfo) for the node.
...
```

#### <a name="apidoc.element.jsdom.reconfigureWindow"></a>[function <span class="apidocSignatureSpan">jsdom.</span>reconfigureWindow (window, newProps)](#apidoc.element.jsdom.reconfigureWindow)
- description and source-code
```javascript
reconfigureWindow = function (window, newProps) {
  if ("top" in newProps) {
    window._top = newProps.top;
  }
}
```
- example usage
```shell
...
This returns the [parse5 location info](https://www.npmjs.com/package/parse5#options-locationinfo) for the node.

#### Overriding 'window.top'

The 'top' property on 'window' is marked '[Unforgeable]' in the spec, meaning it is a non-configurable own property and thus cannot
 be overridden or shadowed by normal code running inside the jsdom window, even using 'Object.defineProperty'. However, if you're
 acting from outside the window, e.g. in some test framework that creates jsdom instances, you can override it using the special
 'jsdom.reconfigureWindow' function:

'''js
jsdom.reconfigureWindow(window, { top: myFakeTopForTesting });
'''

In the future we may expand 'reconfigureWindow' to allow overriding other '[Unforgeable]' properties. Let us know if you need this
 capability.

#### Changing the URL of an existing jsdom 'Window' instance

At present jsdom does not handle navigation (such as setting 'window.location.href === "https://example.com/"'). However, if you
'd like to change the URL of an existing 'Window' instance (such as for testing purposes), you can use the 'jsdom.changeURL' method
:
...
```

#### <a name="apidoc.element.jsdom.serializeDocument"></a>[function <span class="apidocSignatureSpan">jsdom.</span>serializeDocument (doc)](#apidoc.element.jsdom.serializeDocument)
- description and source-code
```javascript
serializeDocument = function (doc) {
  return domToHtml([doc]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jsdom.jsdom"></a>[module jsdom.jsdom](#apidoc.module.jsdom.jsdom)

#### <a name="apidoc.element.jsdom.jsdom.jsdom"></a>[function <span class="apidocSignatureSpan">jsdom.</span>jsdom (html, options)](#apidoc.element.jsdom.jsdom.jsdom)
- description and source-code
```javascript
jsdom = function (html, options) {
  if (options === undefined) {
    options = {};
  }
  if (options.parsingMode === undefined || options.parsingMode === "auto") {
    options.parsingMode = "html";
  }

  if (options.parsingMode !== "html" && options.parsingMode !== "xml") {
    throw new RangeError('Invalid parsingMode option ${JSON.stringify(options.parsingMode)}; must be either "html", ' +
      '"xml", "auto", or undefined');
  }

  options.encoding = options.encoding || "UTF-8";

  setGlobalDefaultConfig(options);

  // Back-compat hack: we have previously suggested nesting these under document, for jsdom.env at least.
  // So we need to support that.
  if (options.document) {
    if (options.document.cookie !== undefined) {
      options.cookie = options.document.cookie;
    }
    if (options.document.referrer !== undefined) {
      options.referrer = options.document.referrer;
    }
  }

  // List options explicitly to be clear which are passed through
  const window = new Window({
    parsingMode: options.parsingMode,
    contentType: options.contentType,
    encoding: options.encoding,
    parser: options.parser,
    url: options.url,
    lastModified: options.lastModified,
    referrer: options.referrer,
    cookieJar: options.cookieJar,
    cookie: options.cookie,
    resourceLoader: options.resourceLoader,
    deferClose: options.deferClose,
    concurrentNodeIterators: options.concurrentNodeIterators,
    virtualConsole: options.virtualConsole,
    pool: options.pool,
    agent: options.agent,
    agentClass: options.agentClass,
    agentOptions: options.agentOptions,
    strictSSL: options.strictSSL,
    proxy: options.proxy,
    userAgent: options.userAgent
  });

  const documentImpl = idlUtils.implForWrapper(window.document);
  documentFeatures.applyDocumentFeatures(documentImpl, options.features);

  if (options.created) {
    options.created(null, window.document.defaultView);
  }

  if (options.parsingMode === "html") {
    if (html === undefined || html === "") {
      html = "<html><head></head><body></body></html>";
    }

    window.document.write(html);
  } else if (options.parsingMode === "xml") {
    if (html !== undefined) {
      documentImpl._htmlToDom.appendHtmlToDocument(html, documentImpl);
    }
  }

  if (window.document.close && !options.deferClose) {
    window.document.close();
  }

  return window.document;
}
```
- example usage
```shell
...

#### Dealing with asynchronous script loading

If you load scripts asynchronously, e.g. with a module loader like RequireJS, none of the above hooks will really give you what
you want. There's nothing, either in jsdom or in browsers, to say "notify me after all asynchronous loads have completed." The solution
 is to use the mechanisms of the framework you are using to notify about this finishing up. E.g., with RequireJS, you could do

'''js
// On the Node.js side:
var window = jsdom.jsdom(...).defaultView;
window.onModulesLoaded = function () {
  console.log("ready to roll!");
};
'''

'''html
<!-- Inside the HTML you supply to jsdom -->
...
```

#### <a name="apidoc.element.jsdom.jsdom.env"></a>[function <span class="apidocSignatureSpan">jsdom.jsdom.</span>env ()](#apidoc.element.jsdom.jsdom.env)
- description and source-code
```javascript
env = function () {
  const config = getConfigFromArguments(arguments);
  let req = null;

  if (config.file && canReadFilesFromFS) {
    req = resourceLoader.readFile(config.file,
    { defaultEncoding: config.defaultEncoding, detectMetaCharset: true },
    (err, text, res) => {
      if (err) {
        reportInitError(err, config);
        return;
      }

      const contentType = parseContentType(res.headers["content-type"]);
      config.encoding = contentType.get("charset");
      setParsingModeFromExtension(config, config.file);

      config.html = text;
      processHTML(config);
    });
  } else if (config.html !== undefined) {
    processHTML(config);
  } else if (config.url) {
    req = handleUrl(config);
  } else if (config.somethingToAutodetect !== undefined) {
    const url = URL.parse(config.somethingToAutodetect);
    if (url.protocol && url.hostname) {
      config.url = config.somethingToAutodetect;
      req = handleUrl(config.somethingToAutodetect);
    } else if (canReadFilesFromFS) {
      req = resourceLoader.readFile(config.somethingToAutodetect,
      { defaultEncoding: config.defaultEncoding, detectMetaCharset: true },
      (err, text, res) => {
        if (err) {
          if (err.code === "ENOENT" || err.code === "ENAMETOOLONG") {
            config.html = config.somethingToAutodetect;
            processHTML(config);
          } else {
            reportInitError(err, config);
          }
        } else {
          const contentType = parseContentType(res.headers["content-type"]);
          config.encoding = contentType.get("charset");
          setParsingModeFromExtension(config, config.somethingToAutodetect);

          config.html = text;
          config.url = toFileUrl(config.somethingToAutodetect);
          processHTML(config);
        }
      });
    } else {
      config.html = config.somethingToAutodetect;
      processHTML(config);
    }
  }

  function handleUrl() {
    config.cookieJar = config.cookieJar || exports.createCookieJar();

    const options = {
      defaultEncoding: config.defaultEncoding,
      detectMetaCharset: true,
      headers: config.headers,
      pool: config.pool,
      strictSSL: config.strictSSL,
      proxy: config.proxy,
      cookieJar: config.cookieJar,
      userAgent: config.userAgent,
      agent: config.agent,
      agentClass: config.agentClass,
      agentOptions: config.agentOptions
    };

    const fragment = whatwgURL.parseURL(config.url).fragment;

    return resourceLoader.download(config.url, options, (err, responseText, res) => {
      if (err) {
        reportInitError(err, config);
        return;
      }

      // The use of 'res.request.uri.href' ensures that 'window.location.href'
      // is updated when 'request' follows redirects.
      config.html = responseText;
      config.url = res.request.uri.href;
      if (fragment) {
        config.url += '#${fragment}';
      }

      if (res.headers["last-modified"]) {
        config.lastModified = new Date(res.headers["last-modified"]);
      }

      const contentType = parseContentType(res.headers["content-type"]);
      if (config.parsingMode === "auto") {
        if (contentType.isXML()) {
          config.parsingMode = "xml";
        }
      }
      config.encoding = contentType.get("charset");

      processHTML(config);
    });
  }
  return req;
}
```
- example usage
```shell
...

You can use it with a URL

'''js
// Count all of the links from the io.js build page
var jsdom = require("jsdom");

jsdom.env(
  "https://iojs.org/dist/",
  ["http://code.jquery.com/jquery.js"],
  function (err, window) {
    console.log("there have been", window.$("a").length - 4, "io.js releases!");
  }
);
'''
...
```

#### <a name="apidoc.element.jsdom.jsdom.jQueryify"></a>[function <span class="apidocSignatureSpan">jsdom.jsdom.</span>jQueryify (window, jqueryUrl, callback)](#apidoc.element.jsdom.jsdom.jQueryify)
- description and source-code
```javascript
jQueryify = function (window, jqueryUrl, callback) {
  if (!window || !window.document) {
    return;
  }

  const implImpl = idlUtils.implForWrapper(window.document.implementation);
  const features = implImpl._features;
  implImpl._addFeature("FetchExternalResources", ["script"]);
  implImpl._addFeature("ProcessExternalResources", ["script"]);

  const scriptEl = window.document.createElement("script");
  scriptEl.className = "jsdom";
  scriptEl.src = jqueryUrl;
  scriptEl.onload = scriptEl.onerror = () => {
    implImpl._features = features;

    if (callback) {
      callback(window, window.jQuery);
    }
  };

  window.document.body.appendChild(scriptEl);
}
```
- example usage
```shell
...

### jQueryify

'''js
var jsdom = require("jsdom");
var window = jsdom.jsdom().defaultView;

jsdom.jQueryify(window, "http://code.jquery.com/jquery-2.1.1.js", function () {
  window.$("body").append('<div class="testing">Hello World, It works</div>');

  console.log(window.$(".testing").text());
});
'''

### Passing objects to scripts inside the page
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

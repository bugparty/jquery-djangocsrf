# jQuery Django CSRF Plugin

[![Build Status](https://travis-ci.org/bfontaine/jquery-djangocsrf.svg?branch=master)](https://travis-ci.org/bfontaine/jquery-djangocsrf)

The **djangocsrf** jQuery plugin makes it easy to use AJAX calls with Django’s
CSRF token.

## Installation

[Download][release-0.1.1] and include the script *after* the jQuery library and
its Cookie plugin:

```html
<script src="http://code.jquery.com/jquery-1.9.0.min.js"></script>
<script src="http://cdn.jsdelivr.net/jquery.cookie/1.4.0/jquery.cookie.min.js"></script>
<script src="http://cdn.jsdelivr.net/gh/bfontaine/jquery-djangocsrf@0.1.1/jquery.djangocsrf.js"></script>
```

[release-0.1.1]: https://github.com/bfontaine/jquery-djangocsrf/releases/download/0.1.1/jquery.djangocsrf-0.1.1.min.js

## Usage

Enable the plugin:

```js
$.djangocsrf( "enable" );
```

That’s all! After that, all AJAX calls made through jQuery to the current
domain will include an `X-CSRFToken` header set to the client’s token.

Disable the plugin with `$.djangocsrf( "disable" )`, and query its current
state with `$.djangocsrf()`.

## Tests

Requires Node. Start the server:

	$ node test/server.js

Then open `http://0.0.0.0:8124/test/index.html` in your browser.

Basic tests can also be run with `grunt`.

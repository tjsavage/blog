---
layout: post
title:  "One small file... one giant leap for the web platform"
date:   2014-08-15 11:57:35
author: polymer-team
categories: announcements
---
_platform.js is Polymer's collection of Web Component polyfills & polymer.js is our opinionated sugar for making it easier to build compelling elements and apps of your own._

Big, or should we say small, news on the Polymer project today. The size of the `polymer.js` file needed to run on fully-functional browsers is down to 32kb gzipped and minified.  The polyfills add 37kb to work with browsers that don't yet implement Web Components natively.
 
By “fully functional browsers” we don’t just mean “Chrome.”  We’re building Polymer for the web platform of tomorrow, not just the Chrome of today - as the great Wayne Gretzky would say, we’re skating to where the puck is going, not where it has been. As the web components standards are rolled into more and more browsers, the need for `platform.js` polyfills will shrink to 0 - and you’ll be left with just pure Polymer goodness.

### Minified and Gzipped you say?

You can find the latest minified `polymer.js` and `platform.js` under [Getting the Code](http://www.polymer-project.org/docs/start/getting-the-code.html) on the Polymer site.

Gzip compression is supported by most servers, and all modern browsers. Your server will compress the content types you specify before sending them to the client, minimizing bandwidth usage and speeding up load time.

For Apache, you can use the [mod_deflate](http://httpd.apache.org/docs/2.2/mod/mod_deflate.html) module to handle server-side compression. First, make sure that `mod_deflate` is enabled in your `httpd.conf`, by uncommenting the line:

    LoadModule mod_deflate

Add the following to your .htaccess file to enable compression for the listed content types:

    AddOutputFilterByType DEFLATE application/javascript text/plain text/xml text/css text/plain text/html

For [gzip on NGINX](http://nginx.org/en/docs/http/ngx_http_gzip_module.html), you can add the following to your config:

    gzip on;
    gzip_min_length 1000;
    gzip_types application/javascript text/plain text/xml text/css text/plain;

On Appengine, gzip is enabled and handled automatically. Happy compressing!

Being future-facing and in Developer Preview means things today won’t always work as expected - your ongoing feedback and contributions are crucial to helping bridge the gap. And with only 32kb to download, the gap is smaller than ever.
 
Get started with [Polymer](http://polymer-project.org), contribute to the [Github](https://github.com/Polymer), or find us on [Twitter](https://twitter.com/Polymer).


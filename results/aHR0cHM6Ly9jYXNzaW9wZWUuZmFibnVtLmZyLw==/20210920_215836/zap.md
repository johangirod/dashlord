
# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 21:53:02


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 4 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 2 | 
| Incomplete or No Cache-control Header Set | Low | 3 | 
| Permissions Policy Header Not Set | Low | 5 | 
| Strict-Transport-Security Header Not Set | Low | 8 | 
| X-Content-Type-Options Header Missing | Low | 8 | 
| Base64 Disclosure | Informational | 2 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 3 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 6 | 
| Storable but Non-Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 2
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000`
  
  
  
  
Instances: 3
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/838645d.js](https://cassiopee.fabnum.fr/_nuxt/838645d.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/favicon.ico](https://cassiopee.fabnum.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/838645d.js](https://cassiopee.fabnum.fr/_nuxt/838645d.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/robots.txt](https://cassiopee.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/favicon.ico](https://cassiopee.fabnum.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/838645d.js](https://cassiopee.fabnum.fr/_nuxt/838645d.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bbc5371.js](https://cassiopee.fabnum.fr/_nuxt/bbc5371.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `e6e-fBSm/3Wn1KVwm75GnSrIE/IY9BA`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `e6e-fBSm/3Wn1KVwm75GnSrIE/IY9BA`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>{��|\x0014��u�ԥp��F�*�\x0013�\x0018�\x0010</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bbc5371.js](https://cassiopee.fabnum.fr/_nuxt/bbc5371.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(window.webpackJsonp=window.webpackJsonp||[]).push([[3],[,,,,,,function(t,e,n){"use strict";n.r(e),function(t,n){var r=Object.fr", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>window.addEventListener('error', function () {  var e = document.getElementById('nuxt-loading');  if (e) {e.className += ' error';  }});</script>`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>window.addEventListener('error', function () {  var e = document.getElementById('nuxt-loading');  if (e) {e.className += ' error';  }});</script>`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/robots.txt](https://cassiopee.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 1
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/838645d.js](https://cassiopee.fabnum.fr/_nuxt/838645d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/favicon.ico](https://cassiopee.fabnum.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23112669`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33333337`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `23112669`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/a6b2412.js](https://cassiopee.fabnum.fr/_nuxt/a6b2412.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `66666674`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `23112669`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js](https://cassiopee.fabnum.fr/_nuxt/bd9b3f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>23112669, which evaluates to: 1970-09-25 12:11:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

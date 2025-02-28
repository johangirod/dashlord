
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 02:52:22


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 6 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 5 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 6 | 
| Permissions Policy Header Not Set | Low | 7 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 4 | 
| Information Disclosure - Suspicious Comments | Informational | 8 | 
| Modern Web Application | Informational | 6 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js](https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.890a330e.chunk.css](https://datapass.api.gouv.fr/static/css/main.890a330e.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.890a330e.chunk.css](https://datapass.api.gouv.fr/static/css/main.890a330e.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `org/TR/2001/REC-SVG-20010904/DTD/svg10`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css](https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `d09GRgABAAAAABiUAAsAAAAAMhQAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAADsAAABUIIslek9TLzIAAAFEAAAAQQAAAFZJwk7CY21hcAAAAYgAAAGFAAAFijTu/gxnbHlmAAADEAAAEREAACHcs9vSE2hlYWQAABQkAAAAMQAAADYc8u6XaGhlYQAAFFgAAAAcAAAAJAhyBA5obXR4AAAUdAAAABEAAAE0ZEAAAGxvY2EAABSIAAAAnAAAAJwdVSY8bWF4cAAAFSQAAAAdAAAAIAFhAGBuYW1lAAAVRAAAAR0AAAHyFNvC+HBvc3QAABZkAAACMAAABQN7dnhseJxjYGRgYOBiMGCwY2BycfMJYeDLSSzJY5BiYGGAAJA8MpsxJzM9kYEDxgPKsYBpDiBmg4gCACY7BUgAeJxjYGRZwDiBgZWBgYGf2QNIroDQTA4MVoymQJqBlZkBKwhIc01hcPjI+NGH+cB/AYYc5gMMH4DCjCA5AHoFCxQAAAB4nO3TV27bQAAG4ZEld7n33nvvvXdbh/QxcqA85Y0ncDj6c4wQ+HbABRuwS6AVqJa2SzWo/KGCx+9yttKcr9LVnK/xq3lNzfmi8fNTjhXH8rzWHFvKa2vlE9top4PO8r5u6vTQSx/9DDDIEMOMMMoY40wwyRTTzDDLHPMssMgSy6ywyhrrbLDJVvn+HXbZY58DDjnimBNOOeOcCy654pobbrnjngceeeKZF155450PPvmiUX5YG/+PukP1+99Zw7WL5mq2BLYa7oqiFq5v0RrumKItsO2B7QhsZ2C7wp1UdAe2Hn5d0RPY3sD2BbY/sAOBHQzsUGCHAzsS2NHAjgV2PLATgZ0M7FRgpwM7E9jZwM4Fdj6wC4FdDOxSYJcDuxLY1cCuBXY9sBuB3QzsVmC3w7+/2AnsbmD3Arsf2IPAHgb2KLDHgT0J7GlgzwJ7HtiLwF4G9iqw14G9CextYO8Cex/Yh8A+BvYpsM+BfQnsa2DfAvse2I/Afgb2K7CNoPEXNCPH+AAAAHicnVkLcFNndr7nXvnKT8lCvroYW8KSkK6N33ril2zG9pUBm4fDwwu2A8zFcUJCIbyWQEIzxZQhQMmGajNsNqE45DUdNuxuyW7DtNSZ6Wp3kraZIUyWph26O5PJdDbpTtcbHK110/P/90qWjZyYYu7Vr//e/7z+c75zzi+GY5ivDxh6uSGmhKlgahkGfKJNtBUbeSNfIXklb3E4FA5xOOXDQR24+LAvAgEcmKDEAezAqQP7Oru6OvcdUH+fGo03rd1wfcO6Fe0v/+3Lv6vqrqzs7ic3bnD2a1BMRskdG+sbGusfam5vH9dfxBuTM0uuENPJ9DJMjistUUVaSg8OqGgmMEoR1ibiU6kOJK8RJ3h8zeOqg0AEfA4oMYHkCwW8Lr7EliG5JggV7viqwa3fGYz6xp7/i8buyOvvvNnRUljoWvbizu3DOy9ULDWb26A9NBgKDT5ObqGqlpb+lpYzc4hQDd9tKbHabG2BFWxrsKdzFdfd0a/sGBw+abOVlp7ePrhDWf+POhW8KYRMfwvDMDP7UYB6B3E/gn7BL7gFd9AdtGbTXyIbEwqQJy7yvYQ8Yb1KPK7EE1l0PPXE0NZgOBzcOnQnNYCL5OW4kryTTRNl1rt0gGIxRNjr7D+jnAxY/Ban4LS4Lc4gcoYa9Zai3oKLqUGNQvV6zTDCdTIWRmBKGSYPbLgdbifZnDDg9tg4wR8kF3sCPuFNYtF0T9HiIiN8YhTLFg8oisItn/5FQbnNZLKVF3BNBSZTcreiwHAiQUQxZNAvYRYz5dk4gBM4tKUFr2xM1I1cofqUT8nGa/ojdjz5BwUmElT3rz/m/oOdYnIZxgNiHoTRAuxpKIyqR9WjUShUvk/Gx2BMVv/IbifyafaKsR7i2RAma9iBqW71PXVChrp7UXUCIlHtva9/y33Gfk5oAxoVjHkgwil2e/ISpY804aKiTkZhDMaiDEvpHmEvoIXzyE7gHohG0QhwXmH56NQUUmYvJE+wx6L3pmSIkNe1NdfYN1EWsnsiYeGUUCSJfSchqzehQ1ZvaZ8JGE3I0IEj/K7elBNpXQT2NaoLXc06dBVg9J4MbRCR5+qC1PNAAmeQq1InZRgjdipKvoJOMmO1tGwnZvRBz0J1ROAqlGSC6AOR7Pr8mB3X9ZEIJw+9w1dEepSb9eoDGP0j1WRNQv9M6VOh60PXsS8QRuoE6jMlqxM4SOtNZKP6EGXQ57kKtT8KV9Ux4vn/rW7AMQaSvuczfkJ2BtDGRvZ0evfYpuQr7A71D1FiDjntIw1UDiN9eUA3J4zrAmn6oq/3cefQQmUMY3VaSnh0c28Q/D6bHaUKhFoIbDiDfoX7zC5MHxPs7BdxwT692C7EMTwVuKhGBLtd4PrtQiIh2NHjdex5DbHnHCMybkZCGZCekCJumaFqdBI4whHCkui0OLn+OKFG+OgMMOqVGFcRUxLTd7kKbjk+vEsZVlBmcYXCk7pX09nAszGisx5Lk/C+nPwCA+NX8H40+TkNjMw8VcXUz5MLsmJhWAqL6KHZ8D4LFrbcks9BmZwV07MgYfxW9CyU9cyRL/Qg8lnDJGAlo0QEXaiYT5yTz56T/+qsfOasfG6hwsLtc/I5XIILcbnub99Hvy+gmJSWgiDTl1PyV/fkL9H9rk7JUzjC71My1XM/6jmYwnEggJpyEXfQH3SSmCV/XH9CsQvJLtzxBEyqe3Hf2SkluYj4AfsFushldS+cJ5eO35l07STzOYXZxEWL05Ljt7iteMEwTKbpx9kBNULdCjkoGTySXeyNmMYmFTdLkAfHFDJMGNE1L4XeMe7E9DH0vAZZHVC39EC9kq/AKaiX1S3wpqx+yNZp6w/g+m1MPmNCb3UHIeRbilnGSIH6sVtsq7nKdM5snv49odZKvpvP4lTyYYVJ53ay3sCYGSvxdwkEcQ6ZlfCnqJqzlyyuNKeJXSKzBlnBaZMJaZqT2xWGmdFpObOIYAEIJAf7M2LW70HDIR+8TSYQotBih7TQV9SnZDj5KXsB4Sqh3qImOy3Y0Vyf0ifKTF49ROlX0TqMVIgOEElxVUHqrAiEQ1bq12Fv2rGNNhp5syuvWXXj2MF9PxDFH+w7pN7TRwfHRoe2ta8UxZXt24b+bWY4GnmktfWRY+QWcTW5XE1d5MYtb23+4PjxD5pbU5/Td2tr1m3YtWvDupramdHT+lK8KfpSvNH6chPqdZQpYhyMBzVrxZjlDZpCUhjhlxSUDjYUlkxQhx+ixDvYcI6EpSZnlEIOVuSNgB9G7pkD6v/86a3S4s0rX4py/xm9knzL320WT7330dBIzcj21c6Css8vm8zBVS440+O3Ck+88s7WtU9++fF5m22t2tSwrcvF5awS9tz+yy0vtb0UnXZFr7Cb6w93jl7ZXBAYKS9wrt4+UvO7y+5VQbNpX7Rn89bY8OLSdbXFh3955OlH4Resq2tbg5ZrnsKcMMRU4xe6B0IJ2Scak+gG6GGCG+ft4De6LWTTghSHdMBZEb55+PjxkS2u5cvaq4VFz9kOHr4ZXkHQRCvbTx19fPSMFYbP7xkayck5urjENXxevWw9M/r4Ubo+5Yv7DWUoQxGiIFYGmW4INFmEuYpEKhfAhBKLx7nBBAlhdMgTgl0tjOO/zFgZZHiMVeLZfqPkD/rDmG4sbg8SdCJ5o0afPY2EYogoheyNePIN9OOBhLnIRtjAKKE4fRdnBDtyKjGb7QIzE8uD6NcCyaG+UNDiTKc7CYUOCzGoQQqTNLfdtRWZE6Ci2DVapjObBPYGLT5Teg+i3hjVVnBmpE0akRakxHo1OkhxOMHeYBtShEgsJpJ3uIqU3vtRLmJDkVl6nxW1IKoGixVzcwlfDZkGPU9bkxDCIDYmVcos0ya7aKeBWFhDOg0D1Z/sVR4irogRgHhm8WuhilU4aZPc1lnG1m09EI9TNhcpk1imzTVBLhE5kBXUxJET1GQY30Ftn5kraaWeNVdymEIk0g5ky4h/jyifNeuxXtJvxGk9Y5iVk2uZxgfKyqTpwjyz4LpBmU+kLIkYa0CskJi0jH3oOw1MGyMzD1F8RYTlRJuAKaHEaOLQy3mX5JLqOHRLbyAcCEe4cMgfEjUs1VzCo7W1vlCOtoca9LIDO5c5lssjfRLHArCc1DciV9u9E9kmt3ft7+zcf4rcADx+D/5X381s3/HVyt7512dMJnQ6eCsqJYQ8WzJ6e6LzFfS9atx7D+5MC82l1P4aQpEOzY9b4qdnEYLH5Q2EiLdb8QE4XTwGl81PIxadtJH76zEux1RcUW81jf05FDuW1XZ4nKbC5C8rams76urcJ0+y4SRTJkll7NflklRe/aFrUbnZ6lri+wiuttgX2coWN1Z2TNd1kNfVxXAVNnjLptUyr7eMY8u8qZgksWLHqrg6a10cIC6kiWsMamnODiLpaK/7UnFvF3wNdev6/6F/XV2DQo2DtfL7dkEtpNGLOON7mDwjLz3s89Ht6PJpgGjIkMGJVqv/NilyaK0kuCEtzTySkBKJFGdQQ0WaVyBaRilxOJ8STK89erE2MOsYOkuePNK6SjECPjrQwR315kp4Fo6tnN0RqGuhuFf9GfT06j1IH/qGGaNWvJ9qTh5YnHlsJlnuEfWA+jhXMZ2AI3BgNulb6g9BSf4EVfwJ9OnY87FhCfZkHGMkda8Va67UHy0C2YHkG/RzSkng34LWpK7Zaw7QfPxNGJcqlbMfRv1mXpA7TUCOXGn8+H9hHKfX0gvFuCpaYi8Y5LyalHqu1XDYNR/ae2lUi7Z2QCmzCvRBvsAbCvIn8/KyG+UNvqBQfZfPZ3l+nBf4uT1j8wOhv2grMQOP9S3xuXBowX1ZJYo3mZ+fwxNRF2yprnGjkDPO82weD91UAyYjf5F+RcQaiORo9DgP9kVuvR5IBQcQpHGmun/SG2FeHkh2Kan0T2Ii5iMhjbl6DzppQgtwLdhhEuP/vF2IxQRsvHLSfN3oT0GmCTMTIvQMylC+9hT+VIOghWcbm36C4GMVnFj84EVAqCZGWMU0nqnxDMwo03fjWiuYvBOL5WuT9Ewhrr1G9YhT/PKRF7HiiyUPxWIwrMytJxrm8zDB3wYRto7Dsl6MgAPLe7eLlMPzFBiVbeUF9T2b1gRyd+Y0NnsN1Q4UI+uOohBKf2Hz2o1dVZx7ZVWJ3ZVb21ppF9ZkqUHkBzq5QNOFBTct3yNQBzw54HYQBR6oKrELjmqDt7mR35EbWLOpp76gvLVqoa6ZUK5XrBHsla21uS57SdXKZVxV98a1TYXMnDrOzfjn0SyMknNGETslwW2V+Do26MeOysGFs+rwaCQsPPzC672NTc881hprbGwmH2f1yaxCf9n88pWz6/hlW0oL5D9rV98bWEI/9dlUX6IYtnC76R4wQOIZOyMbSsf5A3Uc9nFkB8hvBii61V3i4EJhsAwfOXjwyM+WLzebo5dirXu+98MXmtjB4SOHDn7359VVZnNPevK3G8rK7EtfO7jvu0d3gWPd8/sibNOK5Eh/ebnD8TrOHhtRf7P++b3t0BTO6NfJOQdDsnQ6lkUaTOQ87UTyDUXrx9H/4yQuthKv11JanDTwCP16riS0chkbswRjFKlh0ey0cM7MroFGIUKCcjb5oY+SpPkRzFCTTwCarT+b7OIq4vrBQAXBCFJ0kJ5yl2EQ93cx0haNEokYssMZZUYJz528Ld9uO9/31KMjrW1trSOPTpKB/1mcbfCnv5PBU73P63uh0az/BqrGCATnRAP2JGFkFr3deh+zCw3+dD1Di5Wu443P4pv1cwToOy82Hu9K1zT0fX/DzPn8dbhIrEryO7ZoyS64SHJ5PspcbHibu6nnf3J2Q/B4KRMgyAj6TwrkBI1cVtQJyIWRSw5KYUaFmSAnxbnfgkU669yD/9RH+p7sZUfxltO3vzf5vd4n+wyVr06/+Co78J3e1dW1tdWre3+cGqgftCgt+J+7Sd7g/r1vf3/yRVzBXcL1yRfxBn9HiELxrGV0oP4cF6q9LYp+Pv0rwybOQqoGICYP80byO5qIocALmI29koANhshL9MAH737toCcUDARDho1N7c76wki04ezTzcXP/Nf6cl+1v6a6t7G+QdjdufJvHuoZ3/Tcwd3rVld5I+yV0tyS1mUeU0DsfLabf3Jn44rQYDmUco2bW/ML8zrWQ6A2v64h5Nu6cffoY4Xm2lTcHuA+487R38IYMcNBYI7HlBATx9Oope7t7+6qrKqq7Op+NTU4k0bHJ2Bi1hM6SOEZ5ScyNZj1ZnF0z3hjdu6zzrdmRFGQg3xZRg5Qc79Q/TM/JmbIt0HWHssbskmqzPxuqNnon7AvMCMCeDKztIekOEzPJvBKnhyJhJNXCuMUCgs3JkikT0AebyrKzS0y8eoU/G/UU+Wv7mnusJdfIqccgv3XBpYvzJ3+NLeQZw2/dvSUP1Qf3FrWU328p6utWbeXxjsHK1zSFxmxZRalBcnAnn7rpz9961++WRB2y3Px56SFSKPZ4Sq1g2s+O9RC+pw9LIL3ft7s7WvRa9fkt9+Wr12LZrVCPPUU/zNpG1zVbVD5zTaYzX9yHgPMEmJ+C8yWRJPjuO4HgYV6gmeOY2SzyXi0Z92WtdHBkYZ6NfEtTvKv0Y63t+96pyO69pMjh3ePKvf5jCEtp+YzzQ/mNXPlndeG8wg9vzm/RXKW9oC97FeIlWhdwKhfCvSk20Q/zEAggdYQkjdIQZKcsYZDfgIQWG5ALRiC+byBnJgY+Py8wDLvzujQ+vVD0Z3eZYE8E8+l5oNvblytTyfjND8flXr8bYFAmz9a6QnlF6SIFOSHPCv2N9Xjgx4JH5g1Gjitlv7oR8z/AafsKuUAAAB4nGNgZGBgAGK37QevxfPbfGXgZtkAFGG4M/EqL4L+L8CygfkAkMvBwAQSBQBjZQwjAAAAeJxjYGRgYD7wX4CBgWUDAwOYZGRABb4AVu8DinicY2BgYGDZMIpJwQD0JTVxAAAAAAAAAABMAMgBHAE0AWQBmgG0AcgB4AH6AhoCLgJIAmICggKWAq4CxgLaAwYDQANUA6QD/gQYBEQEdgSWBLYE4AUQBXwF5AYmBkwGfAaiBsgG/Ac6B24HwAg6CJII1AkeCUgJeAmSCawJ4AoyCm4KzgsKC2ILsAweDHIMuAzeDQ4NOA2EDZIN/g5ODoYO4A8eD2QPoA/kEDgQlBDueJxjYGRgYPBlCGHgYgABJiDmArP/g/kMABmDAcIAAAB4nF2OvU7DMBSFT/qHaBACITGbpQtS+jP2AdqZDtnTxElbJXHkuJUqMTPzFMw8Bc/FiXslKmzp+jvnHl8bwAN+EKBbAYa+dquHG6oL90l3wgPyo/AQIZ6FR1QvwmO8YiIc4glvnBAMbumMkQn3cI9auE//XXhA/hAecvqn8Ij+l/AYMb6FQ0yC0T41dbvRxbFMrGdfYm3bvanVPJp5vda1tonTmdqeVXsqFs7lKremUitTO12WRjXWHHTqop1zzXI6zcWPUlNhjxSGf26xgUaBI0oksFf+H8VMWO90WmGOCLOr/pr92mcSOJ4ZM1ucWVucOHtB1yGnzpkxqEgrf7dLl9yGTuN7Bzop/Qg7f6vBElPu/F8+8q9XvzD1U2IAAAB4nG1T51rbQBDUkGYbG2NDAqT3rhTSe4H0kHc4Syesj9Odc5IwfvvodiVbDuiHvpm5bTcreQseP23v6GcHCziG4ziBkziFBppoYRFtdLCELpbRQx8rWMVpnMEa1rGBsziH87iAi7iEy7iCq7iG67iBm7iF27iDu7iH+/DxAA/xCI+xiSd4imd4jhd4iVd4jTd4i3d4jw/4iE/4jC1s4wu+4hu+4wd+4hd+Ywd/vLYIApPrzI9ipaZExVp2RRj6QWwDJYk3HHegJZS0nFBCDrfWjP3QjDXxXo2n9QglI85Yq/G0KGdT1tfndKcUVfKBqkrWDpZZsfHucK4mC0WMKGtu/KfPivYPn6zUpXxEWoe1knWnjDM6QWGEDoUlV2aM7AqGMtgrwxwcmAN2KFAmlXWLW6w4uBhKJTNJ9SpMJZyhygheRVOGMW+CkdP68iCTVgvlGPdtyAlntx0wUURkNRKBHBizV43g6vSLl/SnTY6QqC9J1JcQTUZoFEbswZTRnmIdGZuILDaajucEF7EU6zQTu1YkdN5zsxdX0r5zixopU7g4QzRGImLFGiEyLpE69zdL1WGqNxL5zOvDClUbKTHhPEJk2MjGurCTf4+K0HX/5jKd3mfGKMvKyMp0yFkVoR6p2C+NI0QTp1LYgIMrTB3SfJBZEfBaW9lQJpzazsZxVg3VLG5RR2T3vlF5wjtju+tCPSLJy29sTqCFlELxjbvzGqUbTkye5QPO9bx/dz6crA==`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js](https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/loda/id/LEGIARTI000034459398/2017-04-24/`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x0000\x0010�\x0010Q� ��0ӏA\x0014�QU�a��qן�\x0018��Y�����ۯ�\x001c��]�㞻�߿</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `QUERY`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js](https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js](https://datapass.api.gouv.fr/static/js/main.f0b1e0bb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `xxx`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 8
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 5 times, the first in the element starting with: "In order to be iterable, non-array objects must have a [Symbol.iterator]() method.`)}function Q(P,N){if(!!P){if(typeof P=="strin", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js](https://datapass.api.gouv.fr/static/js/2.785ccb7c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.890a330e.chunk.css](https://datapass.api.gouv.fr/static/css/main.890a330e.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Other information
<p>In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.</p>
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css](https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000026`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css](https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css](https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000080`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css](https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `64833265`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css](https://datapass.api.gouv.fr/static/css/2.2f7217fb.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000052`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `20010904`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>00000026, which evaluates to: 1970-01-01 00:00:26</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

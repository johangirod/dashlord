
# ZAP Scanning Report

Generated on Thu, 16 Sep 2021 07:08:23


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 3 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 3 | 
| Permissions Policy Header Not Set | Low | 6 | 
| Base64 Disclosure | Informational | 10 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 4 | 
| Retrieved from Cache | Informational | 6 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 12 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public,max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public,max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public,max-age=3600`
  
  
  
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycduSCXABdvMOsEiKuy-m62QpFhMDebwn3Nu_byXCJaGbmbbLjXcZRK9V6gjc3N5wwJLoQ-zNqJnj5A2V3wExqzQ`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycduznNti5sazn82CcbQMOrCf1Cd4WP4kIF8Fg5zXlvP2b89IcEk95jj_iAGrMjLqjs7WBNSocYXN384Skmsnw7M`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdt7dCjoh9VaIGPhxhWERgzJOcNHTsrLSh6PsjVbzYLfrxLnvaF0ylfssYD2bPPeyA2kLr2IHGWBW-47Q8bt36g`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdvtOISIrN1ZLKTzFOApQG99Pi6Mh6K8A9L5hU0zg69Z0ygnRaBhQY4AAcNs1Bh8wRNt6NCigzjrmGWImup1Uq0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdt8_zkYm05Fnes0XorKyVoZgkXfZWGHeQmYi0JFS2quc0K0kNKGIR66MaWLLAaWhOHd5qZimOs8PXl2o9ktyQc`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdtgWj0yMWuIi1_CPuEeSG5e9ESw2qsGgwuIw5BWZs1xGtoQBpE6kLJmzUhsy8emyCmIICXuYG65_Ll0W_OJ_xI`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdughfgr2SHX3BGLKHriToKlmwaINSoZfXR6xIwYl4-sdb2vpjxKmC7iWe8hsWpd6F9eeyGYXYp35zF4HYAsDBg`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdsZOGq2ZV86bgc0saRJot0D1cOmlDZKLStw8HipoEgxhO-tQO6iyHFoF4CUz4O6EHpqUOMs6kbTZYBzP_GiSHE`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdvC9UPfvYCvzga_LCbYSZGILpwAaS-z66GZ-FRmVkvHmVn1Rb6rFbOq68Fh8VatoS1EFNfFTCuGU7yQ10HhqH4`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdt-8b7-KyUpI9QP8jH6STRYEourfeZtkHTg3iGC2w0tyn1syb7wTZnNPfOigIgK3o8V-44958WK9TcDkXk7gwQ`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x00003�qے	p\x0001v�\x000e�H��/��d)\x0016\x0013\x0003y�'�ۿo%�%����ˍw\x0019D�U�\x0008���p���C�ͨ���
��\x00011�4</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "(this["webpackJsonppass-culture-pro"]=this["webpackJsonppass-culture-pro"]||[]).push([[2],[function(e,t,n){"use strict";e.export", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
Instances: 4
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 959`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 957`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 31421`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 111`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 70`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 51403`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.83b3b2c1.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.86be5535.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630747`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630747`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `27118309`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630672`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630747`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630747`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `03964659`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `70710678`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630747`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.0272e4c6.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630747`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631630672`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1631630747, which evaluates to: 2021-09-14 14:45:47</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

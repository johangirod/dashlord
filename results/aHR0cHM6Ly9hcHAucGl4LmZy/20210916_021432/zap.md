
# ZAP Scanning Report

Generated on Thu, 16 Sep 2021 01:51:50


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 4 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 6 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 3 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 4 | 
| Permissions Policy Header Not Set | Low | 6 | 
| Base64 Disclosure | Informational | 4 | 
| Information Disclosure - Suspicious Comments | Informational | 16 | 
| Modern Web Application | Informational | 4 | 
| Retrieved from Cache | Informational | 11 | 
| Storable and Cacheable Content | Informational | 8 | 
| Storable but Non-Cacheable Content | Informational | 3 | 
| Timestamp Disclosure - Unix | Informational | 13 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `create
function n`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>create</p><p>function n</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600|Roboto:300,400,500|Roboto+Mono" rel="stylesheet" type="text/css" media="all">`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600|Roboto:300,400,500|Roboto+Mono" rel="stylesheet" type="text/css" media="all">`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600|Roboto:300,400,500|Roboto+Mono" rel="stylesheet" type="text/css" media="all">`
  
  
  
  
Instances: 6
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://analytics.pix.fr/js/container_fNoTNeFZ.js`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://analytics.pix.fr/js/container_fNoTNeFZ.js`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://analytics.pix.fr/js/container_fNoTNeFZ.js`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `22PAR_pix_cac26b28c15971f8fda41f5a94b1b81647c7b5780582bb169467988b9233c757`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `22PAR_pix_cac26b28c15971f8fda41f5a94b1b81647c7b5780582bb169467988b9233c757`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `22PAR_pix_cac26b28c15971f8fda41f5a94b1b81647c7b5780582bb169467988b9233c757`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�c�G�b��\x001asn���5�����k�_�xoV�׮;s����9�f�ׯx�|�v�w;�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `BUG`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
Instances: 16
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 11 times, the first in the element starting with: "function a(e){M(o,n,r,a,l,"next",e)}function l(e){M(o,n,r,a,l,"throw",e)}a(void 0)}))},function(e){return a.apply(this,arguments", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
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
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 173179`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-4e2264604bdb22d8f3ac3a0025e00def.css](https://app.pix.fr/assets/mon-pix-4e2264604bdb22d8f3ac3a0025e00def.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 198845`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 45074`
  
  
  
  
* URL: [https://app.pix.fr/apple-touch-icon-pix_app.png](https://app.pix.fr/apple-touch-icon-pix_app.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 45050`
  
  
  
  
* URL: [https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif](https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 53877`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css](https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 173179`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 173179`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js](https://app.pix.fr/assets/vendor-74446f0e7d841cadf807847dd9bfcf01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css](https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js](https://app.pix.fr/assets/mon-pix-786d00196c866fd6491cad8a91319c16.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-4e2264604bdb22d8f3ac3a0025e00def.css](https://app.pix.fr/assets/mon-pix-4e2264604bdb22d8f3ac3a0025e00def.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif](https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/apple-touch-icon-pix_app.png](https://app.pix.fr/apple-touch-icon-pix_app.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `40620661`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `45714415`
  
  
  
  
* URL: [https://app.pix.fr/apple-touch-icon-pix_app.png](https://app.pix.fr/apple-touch-icon-pix_app.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `45714422`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css](https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `40620663`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `45714418`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `00047818`
  
  
  
  
* URL: [https://app.pix.fr/apple-touch-icon-pix_app.png](https://app.pix.fr/apple-touch-icon-pix_app.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `39461817`
  
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `20470099`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `19406768`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css](https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `315360000`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-9ad981fd3c2536928c3d223abe3c7dc4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10993180`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css](https://app.pix.fr/assets/vendor-55d10d992fc5357e585ad8f36dda4cac.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `37555377`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `40620659`
  
  
  
  
Instances: 13
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>40620661, which evaluates to: 1971-04-16 03:31:01</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

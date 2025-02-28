
# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 20:52:37


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 3 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Application Error Disclosure | Medium | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Sub Resource Integrity Attribute Missing | Medium | 6 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 6 | 
| Incomplete or No Cache-control Header Set | Low | 4 | 
| Permissions Policy Header Not Set | Low | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 3 | 
| Storable but Non-Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 27 | 

## Alert Detail


  
  
  
  
### Application Error Disclosure
##### Medium (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `invalid query`
  
  
  
  
Instances: 1
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://support.selego.co/assets/chat/chat.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://support.selego.co/assets/chat/chat.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://support.selego.co/assets/chat/chat.min.js></script>`
  
  
  
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-2.1.4.min.js`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-2.1.4.min.js`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://support.selego.co/assets/chat/chat.min.js`
  
  
  * Evidence: `<script src=https://support.selego.co/assets/chat/chat.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-2.1.4.min.js`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://support.selego.co/assets/chat/chat.min.js`
  
  
  * Evidence: `<script src=https://support.selego.co/assets/chat/chat.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://support.selego.co/assets/chat/chat.min.js`
  
  
  * Evidence: `<script src=https://support.selego.co/assets/chat/chat.min.js></script>`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/robots.txt](https://inscription.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "<script>$(function () {</p><p>        </p><p>        if (typeof ZammadChat === "undefined") return;</p><p></p><p>        var chat = new ZammadChat({</p><p>   ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src=https://code.jquery.com/jquery-2.1.4.min.js></script>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/robots.txt](https://inscription.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/favicon.ico](https://inscription.snu.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `336349172`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2146828260`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012356789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12356789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16947967`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012345689`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `01235678`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `45945784`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `123456789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `880078594`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `121084488`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20130905`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `36247140`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `279091964`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js](https://inscription.snu.gouv.fr/d7ee97bba7d2a34b63d1.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `57186127`
  
  
  
  
Instances: 27
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1073741821, which evaluates to: 2004-01-10 13:37:01</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

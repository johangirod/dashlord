
# ZAP Scanning Report

Generated on Wed, 19 May 2021 03:01:19


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 1 |
| Low | 3 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Hash Disclosure - Mac OSX salted SHA-1 | High | 2 | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Dangerous JS Functions | Low | 2 | 
| Feature Policy Header Not Set | Low | 6 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 7 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 4 | 
| Retrieved from Cache | Informational | 11 | 
| Storable but Non-Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 5 | 

## Alert Detail


  
  
  
  
### Hash Disclosure - Mac OSX salted SHA-1
##### High (Medium)
  
  
  
  
#### Description
<p>A hash was disclosed by the web server. - Mac OSX salted SHA-1</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012323232323232323232123232323232323232323232323`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012323232323232323232123232312121212121212121212`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that hashes that are used to protect credentials or other resources are not leaked by the web server or database. There is typically no requirement for password hashes to be accessible to the web browser.      </p>
  
### Other information
<p>012323232323232323232123232323232323232323232323</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage
* http://openwall.info/wiki/john/sample-hashes

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 2
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Feature-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
Instances: 7
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAQAAAADQ4RFAAACf0lEQVR4AY1UM3gkARTePdvdoTxXKc+qTl3aU5U6b2Kbkz3Gtq3Zw6ziLGNPzrYx7946Tr6/ee/XeCQ4D3ykPtL5tHno4n0d/h3+xfuWHGLX81cn7r0iTNzjr7LrlxCqPtkbTQEHeqOrTy4Yyt3VCi/IOB0v7rVC7q45Q3Gr5K6jt+3Gl5nCoDD4MtO+j96Wu8atmhGqcNGHObuf8OM/x3AMx38+4Z2sPqzCxRFK2aF2e5Jol56XTLyggAMTL56XOMoS1W4pOyjUcGGQdZxU6qRh7B9Zp+PfpOFlqt0zyDZckPi1ttmIp03jX8gyJ8a/PG2yutpS/Vol7peZIbZcKBAEEheEIAgFbDkz5H6Zrkm2hVWGiXKiF4Ycw0RWKdtC16Q7qe3X4iOMxruonzegJzWaXFrU9utOSsLUmrc0YjeWYjCW4PDMADElpJSSQ0vQvA1Tm6/JlKnqFs1EGyZiFCqnRZTEJJJiKRYzVYzJck2Rm6P4iH+cmSY0YzimYa8l0EtTODFWhcMIMVqdsI2uiTvKmTisIDHJ3od5GILVhBCarCfVRmo4uTjkhrhzkiBV7SsaqS+TzrzM1qpGGUFt28pIySQHR6h7F6KSwGWm97ay+Z+ZqMcEjEWebE7wxCSQwpkhJqoZA5ivCdZDjJepuJ9IQjGGUmuXJdBFUygxVqVsxFsLMbDe8ZbDYVCGKxs+W080max1hFCarCfV+C1KATwcnvE9gRRuMP2prdbWGowm1KB1y+zwMMENkM755cJ2yPDtqhTI6ED1M/82yIDtC/4j4BijjeObflpO9I9MwXTCsSX8jWAFeHr05WoLTJ5G8IQVS/7vwR6ohirYM7f6HzYpogfS3R2OAAAAAElFTkSuQmCC`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `net/v1/AUTH_810600e32fdc4cb49a8d15332b68d2cc/storage-pc/assets`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>GIF89a\x0001\x0000\x0001\x0000\x0000�\x0000,\x0000\x0000\x0000\x0000\x0001\x0000\x0001\x0000\x0000\x0002\x0000;</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(this["webpackJsonppass-culture-pro"]=this["webpackJsonppass-culture-pro"]||[]).push([[0],{448:function(e){e.exports=JSON.parse(", see evidence field for the suspicious comment/snippet.</p>
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 32485`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 69343`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 32485`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 64009`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 2`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 32482`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.4ba7b0a3.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.f438de1c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `41017144`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `96862103`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `70710678`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.f8e32c68.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `41017144`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.11d49b55.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>41017144, which evaluates to: 1971-04-20 17:39:04</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

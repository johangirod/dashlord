
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 07:01:07


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 4 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 9 | 
| Cross-Domain Misconfiguration | Medium | 11 | 
| Reverse Tabnabbing | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 7 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 5 | 
| Modern Web Application | Informational | 4 | 
| Retrieved from Cache | Informational | 12 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 10 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/partners/](https://trackdechets.beta.gouv.fr/partners/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/resources/](https://trackdechets.beta.gouv.fr/resources/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/stats/](https://trackdechets.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/accessibilite/](https://trackdechets.beta.gouv.fr/accessibilite/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/cgu/](https://trackdechets.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js](https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js](https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js](https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/resources/](https://trackdechets.beta.gouv.fr/resources/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://faq.trackdechets.fr/informations-generiques/les-fondamentaux/quest-ce-que-trackdechets" target="_blank" class="Resources__Faq-sc-1ucww8g-6 hfdguz"><img height="140px" width="160px" src="data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgZmlsbD0iIzAwMDA5MSI+PGc+PHBhdGggIGQ9Ik03LjM3NSAxOC43MThsLS44NzUuN3YtMS45MiAwYzAtLjU2LS40NS0xLTEtMWgtMyAtLjAxYy0uMjgtLjAxLS41LS4yMy0uNS0uNTFWMi40OGwwIDBjLS4wMS0uMjguMjItLjUxLjQ5LS41MWgxNi41IC0uMDFjLjI3LS4wMS41LjIyLjUuNDl2NWwwIDBjMCAuNTUuNDQuOTkgMSAuOTkgLjU1LS4wMS45OS0uNDUuOTktMS4wMXYtNS41IDBjMC0xLjExLS45LTItMi0ySDEuOTZsLS4wMSAwYy0xLjExIDAtMiAuODktMiAydjE0LjVsMC0uMDFjLS4wMSAxLjEuODkgMiAxLjk5IDJoMi41djNsMC0uMDFjLS4wMS41NS40NCAxIC45OSAxIC4yMiAwIC40NC0uMDguNjItLjIybDIuNS0yIC0uMDEgMGMuNDMtLjM1LjUtLjk4LjE1LTEuNDEgLS4zNS0uNDQtLjk4LS41MS0xLjQxLS4xNloiLz48cGF0aCBkPSJNMjIgMTBIMTJsLS4wMSAwYy0xLjExIDAtMiAuODktMiAydjdsMCAwYzAgMS4xLjg5IDEuOTkgMiAxLjk5aDMuNjY3bDMuNzMgMi44IC0uMDEtLjAxYy40NC4zMyAxLjA2LjI0IDEuNC0uMiAuMTItLjE4LjItLjM5LjItLjZ2LTIuMDFoMWwtLjAxLS4wMDFjMS4xIDAgMi0uOSAyLTJ2LTcgMGMwLTEuMTEtLjktMi0yLTJabTAgOC41djBjMCAuMjctLjIzLjUtLjUuNUgyMGgtLjAxYy0uNTYgMC0xIC40NC0xIDF2MWwtMi40LTEuOCAwIDBjLS4xOC0uMTMtLjM5LS4yMS0uNi0uMjFoLTMuNSAtLjAxYy0uMjgtLjAxLS41LS4yMy0uNS0uNTF2LTZsMCAwYy0uMDEtLjI4LjIyLS41MS40OS0uNTFoOSAtLjAxYy4yNy0uMDEuNS4yMi41LjQ5WiIvPjxwYXRoIGQ9Ik0xMS4yNSA4LjV2LS4xOGwtLjAxLS4wMWMtLjAxLS4xMS4wNi0uMjEuMTYtLjI0bC0uMDEgMGMxLjQzLS41MSAyLjE4LTIuMDggMS42Ny0zLjUxIC0uNTEtMS40NC0yLjA4LTIuMTktMy41MS0xLjY4IC0xLjEuMzgtMS44NCAxLjQyLTEuODQgMi41OWwwIDBjMCAuNDEuMzMuNzQuNzUuNzQgLjQxLS4wMS43NC0uMzQuNzQtLjc2bDAgMGMtLjAxLS43LjU1LTEuMjYgMS4yNC0xLjI2IC42OS0uMDEgMS4yNS41NSAxLjI1IDEuMjQgMCAuNTMtLjM0IDEtLjg0IDEuMTdsMC0uMDFjLS43LjI0LTEuMTcuOS0xLjE3IDEuNjV2LjE3bDAgMGMwIC40MS4zMy43NC43NS43NCAuNDEtLjAxLjc0LS4zNC43NC0uNzZaIi8+PHBhdGggZD0iTTE2Ljc1IDE2Ljk1YS43NS43NSAwIDEgMCAwIDEuNSAuNzUuNzUgMCAxIDAgMC0xLjVaIi8+PHBhdGggZD0iTTE2Ljc1IDE2LjIwN2gtLjAxYy40MSAwIC43NS0uMzQuNzUtLjc1di0yIDBjMC0uNDItLjM0LS43NS0uNzUtLjc1IC0uNDIgMC0uNzUuMzMtLjc1Ljc1djJsMCAwYzAgLjQxLjMzLjc0Ljc1Ljc0WiIvPjwvZz48L3N2Zz4=" alt="Question"/><div><p class="Typography-utccqe-0 lnioOL">Qu’est-ce que Trackdéchets ?</p><p class="Typography-utccqe-0 hwlcGF">Trackdéchets est un outil numérique qui vise à simplifier la traçabilité des déchets dangereux. </p><img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGZpbGw9Im5vbmUiIGZpbGwtcnVsZT0iZXZlbm9kZCI+CiAgICAgICAgPGcgZmlsbD0iIzAwMDA5MSI+CiAgICAgICAgICAgIDxnPgogICAgICAgICAgICAgICAgPHBhdGggZD0iTTE2LjE3MiAxMUwxMC44MDggNS42MzYgMTIuMjIyIDQuMjIyIDIwIDEyIDEyLjIyMiAxOS43NzggMTAuODA4IDE4LjM2NCAxNi4xNzIgMTMgNCAxMyA0IDExeiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTE1MiAtMjYxNykgdHJhbnNsYXRlKDE1MiAyNjE3KSIvPgogICAgICAgICAgICA8L2c+CiAgICAgICAgPC9nPgogICAgPC9nPgo8L3N2Zz4K" alt="arrow" width="24"/></div></a>`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/stats/](https://trackdechets.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/partners/](https://trackdechets.beta.gouv.fr/partners/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/resources/](https://trackdechets.beta.gouv.fr/resources/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/accessibilite/](https://trackdechets.beta.gouv.fr/accessibilite/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/cgu/](https://trackdechets.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/page-data/app-data.json](https://trackdechets.beta.gouv.fr/page-data/app-data.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/page-data/sq/d/3439708972.json](https://trackdechets.beta.gouv.fr/page-data/sq/d/3439708972.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/cgu/](https://trackdechets.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/page-data/sq/d/2341774775.json](https://trackdechets.beta.gouv.fr/page-data/sq/d/2341774775.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/partners/](https://trackdechets.beta.gouv.fr/partners/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/resources/](https://trackdechets.beta.gouv.fr/resources/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/page-data/404.html/page-data.json](https://trackdechets.beta.gouv.fr/page-data/404.html/page-data.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/page-data/index/page-data.json](https://trackdechets.beta.gouv.fr/page-data/index/page-data.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/accessibilite/](https://trackdechets.beta.gouv.fr/accessibilite/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js](https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js](https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js](https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js](https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js](https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js](https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js](https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/webpack-runtime-8ba0e2d34cd8456a6f2c.js](https://trackdechets.beta.gouv.fr/webpack-runtime-8ba0e2d34cd8456a6f2c.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js](https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js](https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/styles-7d4153d260c0197f0043.js](https://trackdechets.beta.gouv.fr/styles-7d4153d260c0197f0043.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/page-data/partners/page-data.json](https://trackdechets.beta.gouv.fr/page-data/partners/page-data.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/283a0af6629136e890b2b3da96dfb6c9/Arc`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/cgu/](https://trackdechets.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/accessibilite/](https://trackdechets.beta.gouv.fr/accessibilite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `static/Marianne-Medium-a7ee30958619da43d05d42edbc8e0bd5`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/static/illustrationHero-b5e7f4dbb877f265d1d5414d57688e37.png](https://trackdechets.beta.gouv.fr/static/illustrationHero-b5e7f4dbb877f265d1d5414d57688e37.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `t0DDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/resources/](https://trackdechets.beta.gouv.fr/resources/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/stats/](https://trackdechets.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNSIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI1IDI0Ij4KICAgIDxnIGZpbGw9Im5vbmUiIGZpbGwtcnVsZT0iZXZlbm9kZCI+CiAgICAgICAgPGcgZmlsbD0iIzAwMDA5MSI+CiAgICAgICAgICAgIDxnPgogICAgICAgICAgICAgICAgPGc+CiAgICAgICAgICAgICAgICAgICAgPGc+CiAgICAgICAgICAgICAgICAgICAgICAgIDxnPgogICAgICAgICAgICAgICAgICAgICAgICAgICAgPHBhdGggZD0iTTMgM2gxOGMuNTUyIDAgMSAuNDQ4IDEgMXYxNmMwIC41NTItLjQ0OCAxLTEgMUgzYy0uNTUyIDAtMS0uNDQ4LTEtMVY0YzAtLjU1Mi40NDgtMSAxLTF6bTE3IDQuMjM4bC03LjkyOCA3LjFMNCA3LjIxNlYxOWgxNlY3LjIzOHpNNC41MTEgNWw3LjU1IDYuNjYyTDE5LjUwMiA1SDQuNTExeiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTExOTEgLTI3NjIpIHRyYW5zbGF0ZSg3MzYgMjUyMikgdHJhbnNsYXRlKDQyLjg1NSAyMjQpIHRyYW5zbGF0ZSg0MTIuMTA4IDE2KSB0cmFuc2xhdGUoLjk0NikiLz4KICAgICAgICAgICAgICAgICAgICAgICAgPC9nPgogICAgICAgICAgICAgICAgICAgIDwvZz4KICAgICAgICAgICAgICAgIDwvZz4KICAgICAgICAgICAgPC9nPgogICAgICAgIDwvZz4KICAgIDwvZz4KPC9zdmc+Cg==`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/partners/](https://trackdechets.beta.gouv.fr/partners/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/Marianne-Thin-2b83dc0ce989cc228a6ad75addbf07a1`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��Z�'?���ѧ��ouߧ��F�owZ��_o�=�</p><p>�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/polyfill-0eec194572597ccd2d1e.js](https://trackdechets.beta.gouv.fr/polyfill-0eec194572597ccd2d1e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "(window.webpackJsonp=window.webpackJsonp||[]).push([[6],{"+ZDr":function(t,e,n){"use strict";var r=n("TqRt");e.__esModule=!0,e.w", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/polyfill-0eec194572597ccd2d1e.js](https://trackdechets.beta.gouv.fr/polyfill-0eec194572597ccd2d1e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">var _mtm = _mtm || [];
                  _mtm.push({'mtm.startTime': (new Date().getTime()), 'event': 'mtm.Start'});
                  var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
                  g.type='text/javascript'; g.async=true; g.defer=true; g.src='https://stats.data.gouv.fr/js/container_j7nJr4FM_dev_753b5bfb24b2f6d74a683dd5.js';
                  s.parentNode.insertBefore(g,s);</script>`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">var _mtm = _mtm || [];
                  _mtm.push({'mtm.startTime': (new Date().getTime()), 'event': 'mtm.Start'});
                  var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
                  g.type='text/javascript'; g.async=true; g.defer=true; g.src='https://stats.data.gouv.fr/js/container_j7nJr4FM_dev_753b5bfb24b2f6d74a683dd5.js';
                  s.parentNode.insertBefore(g,s);</script>`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js](https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js](https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js](https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js](https://trackdechets.beta.gouv.fr/78e521c3-a3d3718d8d14437d1503.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js](https://trackdechets.beta.gouv.fr/component---src-pages-404-tsx-f0670b402b4ffb85d753.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/](https://trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr](https://trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js](https://trackdechets.beta.gouv.fr/app-256d738c0d99bf10ed78.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js](https://trackdechets.beta.gouv.fr/commons-f0d4982eb812f3bc3eab.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js](https://trackdechets.beta.gouv.fr/dc6a8720040df98778fe970bf6c000a41750d3ae-240d4dcce1cdda263fb7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/robots.txt](https://trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/sitemap.xml](https://trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js](https://trackdechets.beta.gouv.fr/e2d93ed24b8a96621dffacdbecbffd1525ce7e5b-f44eba2d6eb57311937f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741825`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741824`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `805306368`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js](https://trackdechets.beta.gouv.fr/framework-cb37257835832d9565ad.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1073741825, which evaluates to: 2004-01-10 13:37:05</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

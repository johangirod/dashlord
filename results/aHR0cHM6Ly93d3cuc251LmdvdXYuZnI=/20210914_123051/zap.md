
# ZAP Scanning Report

Generated on Tue, 14 Sep 2021 12:01:04


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 6 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 12 | 
| Reverse Tabnabbing | Medium | 12 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Vulnerable JS Library | Medium | 3 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 3 | 
| Incomplete or No Cache-control Header Set | Low | 12 | 
| Permissions Policy Header Not Set | Low | 12 | 
| Strict-Transport-Security Header Not Set | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 10 | 
| Non-Storable Content | Informational | 10 | 
| Retrieved from Cache | Informational | 12 | 
| Storable and Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 11 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpeg](https://www.snu.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.png](https://www.snu.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.gif](https://www.snu.gouv.fr/core/*.gif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js](https://www.snu.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css](https://www.snu.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css](https://www.snu.gouv.fr/profiles/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpg](https://www.snu.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.svg](https://www.snu.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/admin/](https://www.snu.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/search/](https://www.snu.gouv.fr/search/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/comment/reply/](https://www.snu.gouv.fr/comment/reply/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/filter/tips](https://www.snu.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/add/](https://www.snu.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.js$](https://www.snu.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/filter/tips](https://www.snu.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/search/](https://www.snu.gouv.fr/search/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/add/](https://www.snu.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/admin/](https://www.snu.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.svg](https://www.snu.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.js$](https://www.snu.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/comment/reply/](https://www.snu.gouv.fr/comment/reply/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library bootstrap, version 4.0.0 is vulnerable.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_I8JXNFKAysXLKGnYpclAmX0XSojch4RCauqXenpT1WA.js](https://www.snu.gouv.fr/sites/default/files/js/js_I8JXNFKAysXLKGnYpclAmX0XSojch4RCauqXenpT1WA.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js](https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_7rfNyvCubhmFQ8H7hU99TZev6xYWwcmCwkWaTl_mXTM.js](https://www.snu.gouv.fr/sites/default/files/js/js_7rfNyvCubhmFQ8H7hU99TZev6xYWwcmCwkWaTl_mXTM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
Instances: 3
  
### Solution
<p>Please upgrade to the latest version of bootstrap.</p>
  
### Other information
<p>CVE-2019-8331</p><p>CVE-2018-14041</p><p>CVE-2018-14040</p><p>CVE-2018-14042</p><p></p>
  
### Reference
* https://github.com/twbs/bootstrap/issues/28236
* https://github.com/twbs/bootstrap/issues/20184
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.snu.gouv.fr/node/51](https://www.snu.gouv.fr/node/51)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/index.php/filter/tips](https://www.snu.gouv.fr/index.php/filter/tips)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/65](https://www.snu.gouv.fr/node/65)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/25](https://www.snu.gouv.fr/node/25)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/60](https://www.snu.gouv.fr/node/60)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/2](https://www.snu.gouv.fr/node/2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/6](https://www.snu.gouv.fr/node/6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/13](https://www.snu.gouv.fr/node/13)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/5](https://www.snu.gouv.fr/node/5)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/52](https://www.snu.gouv.fr/node/52)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/16](https://www.snu.gouv.fr/node/16)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/3](https://www.snu.gouv.fr/node/3)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 90 [https://www.snu.gouv.fr/generation-snu-episode-2-augustin-et-les-pompiers-du-patrimoine-51].</p><p>Predicted response size: 390.</p><p>Response Body Length: 606.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.svg](https://www.snu.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/comment/reply/](https://www.snu.gouv.fr/comment/reply/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/filter/tips](https://www.snu.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/admin/](https://www.snu.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/search/](https://www.snu.gouv.fr/search/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.js$](https://www.snu.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/add/](https://www.snu.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_7rfNyvCubhmFQ8H7hU99TZev6xYWwcmCwkWaTl_mXTM.js](https://www.snu.gouv.fr/sites/default/files/js/js_7rfNyvCubhmFQ8H7hU99TZev6xYWwcmCwkWaTl_mXTM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js](https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_I8JXNFKAysXLKGnYpclAmX0XSojch4RCauqXenpT1WA.js](https://www.snu.gouv.fr/sites/default/files/js/js_I8JXNFKAysXLKGnYpclAmX0XSojch4RCauqXenpT1WA.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/robots.txt](https://www.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sitemap.xml](https://www.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.snu.gouv.fr/filter/tips](https://www.snu.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-semaines-de-l-engagement-113](https://www.snu.gouv.fr/les-semaines-de-l-engagement-113)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/communique-de-presse-du-9-septembre-116](https://www.snu.gouv.fr/communique-de-presse-du-9-septembre-116)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpg](https://www.snu.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css](https://www.snu.gouv.fr/profiles/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js](https://www.snu.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css](https://www.snu.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.gif](https://www.snu.gouv.fr/core/*.gif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpeg](https://www.snu.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.png](https://www.snu.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpeg](https://www.snu.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.gif](https://www.snu.gouv.fr/core/*.gif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.png](https://www.snu.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js](https://www.snu.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css](https://www.snu.gouv.fr/profiles/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.js$](https://www.snu.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css](https://www.snu.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpg](https://www.snu.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/comment/reply/](https://www.snu.gouv.fr/comment/reply/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/admin/](https://www.snu.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.js$](https://www.snu.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/add/](https://www.snu.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/search/](https://www.snu.gouv.fr/search/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/filter/tips](https://www.snu.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.svg](https://www.snu.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_QcLOfO_oG_fRLy5pO-uORXk6EXVE6fEtJ3hzGhHdC5o`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�ȭz��y����ߊW���,��,�\x0007\x000b9�o�D����9\x0015��E�\x0013�Ĵ���hGt.h</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.css$](https://www.snu.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.svg](https://www.snu.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/profiles/*.js$](https://www.snu.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/comment/reply/](https://www.snu.gouv.fr/comment/reply/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/add/](https://www.snu.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/filter/tips](https://www.snu.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/search/](https://www.snu.gouv.fr/search/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/admin/](https://www.snu.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "<script type="application/json" data-drupal-selector="drupal-settings-json">{"path":{"baseUrl":"\/","scriptPath":null,"pathPrefi", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6?page=1](https://www.snu.gouv.fr/actualites-6?page=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/2-000-jeunes-ont-experimente-le-snu-l-an-dernier-25](https://www.snu.gouv.fr/2-000-jeunes-ont-experimente-le-snu-l-an-dernier-25)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a><span>Le séjour de cohésion en 2021 se déroule dans un centre d'accueil de votre région, et a priori, en dehors de votre département, sauf exceptions et cas particulier. Vous pouvez prendre connaissance de votre lieu d’affectation sur </span></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-snu-est-sur-instagram-16](https://www.snu.gouv.fr/le-snu-est-sur-instagram-16)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js](https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23](https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a><span><span>Les affectations pour le séjour de cohésion sont prononcées en fonction des objectifs de représentativité des cohortes dans la limite des capacités d’accueil.</span></span></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_7rfNyvCubhmFQ8H7hU99TZev6xYWwcmCwkWaTl_mXTM.js](https://www.snu.gouv.fr/sites/default/files/js/js_7rfNyvCubhmFQ8H7hU99TZev6xYWwcmCwkWaTl_mXTM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_I8JXNFKAysXLKGnYpclAmX0XSojch4RCauqXenpT1WA.js](https://www.snu.gouv.fr/sites/default/files/js/js_I8JXNFKAysXLKGnYpclAmX0XSojch4RCauqXenpT1WA.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/nous-contacter-35](https://www.snu.gouv.fr/nous-contacter-35)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>consulter la </a>`
  
  
  
  
Instances: 10
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/sitemap.xml](https://www.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.gif](https://www.snu.gouv.fr/core/*.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css](https://www.snu.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js$](https://www.snu.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.js](https://www.snu.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpeg](https://www.snu.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.svg](https://www.snu.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.css$](https://www.snu.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.jpg](https://www.snu.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.snu.gouv.fr/core/*.png](https://www.snu.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 10
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/robots.txt](https://www.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/site_logo/2020-03/2020_Repubique_francaise_logo_SNU_header.png](https://www.snu.gouv.fr/sites/default/files/site_logo/2020-03/2020_Repubique_francaise_logo_SNU_header.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/logo-snu_0.png](https://www.snu.gouv.fr/sites/default/files/logo-snu_0.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_yahZU6stezUpiKbnjynBclwBPV_PMv5fLeaeYnE0xEY.css](https://www.snu.gouv.fr/sites/default/files/css/css_yahZU6stezUpiKbnjynBclwBPV_PMv5fLeaeYnE0xEY.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js](https://www.snu.gouv.fr/sites/default/files/js/js_c4zn8nrzfzQpnScnWeCWGi5mTDcgR3-Czi5alRRYFdM.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-kit-de-communication-snu-38](https://www.snu.gouv.fr/le-kit-de-communication-snu-38)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/robots.txt](https://www.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483644`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `70966589`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483645`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483646`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `20200625`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23](https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23)
  
  
  * Method: `GET`
  
  
  * Evidence: `334279774`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-kit-de-communication-snu-38](https://www.snu.gouv.fr/le-kit-de-communication-snu-38)
  
  
  * Method: `GET`
  
  
  * Evidence: `70966589`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>2147483644, which evaluates to: 2038-01-19 03:14:04</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

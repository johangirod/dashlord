
# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 16:22:23


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 4 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 3 | 
| Storable but Non-Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 10 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/login](https://catalogue.apprentissage.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/reset-password](https://catalogue.apprentissage.beta.gouv.fr/reset-password)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements](https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id](https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/formation/:id](https://catalogue.apprentissage.beta.gouv.fr/formation/:id)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/forgotten-password](https://catalogue.apprentissage.beta.gouv.fr/forgotten-password)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire](https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id](https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/reset-password](https://catalogue.apprentissage.beta.gouv.fr/reset-password)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire](https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/login](https://catalogue.apprentissage.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/forgotten-password](https://catalogue.apprentissage.beta.gouv.fr/forgotten-password)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements](https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/formation/:id](https://catalogue.apprentissage.beta.gouv.fr/formation/:id)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
Instances: 11
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/reset-password](https://catalogue.apprentissage.beta.gouv.fr/reset-password)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/login](https://catalogue.apprentissage.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements](https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/formation/:id](https://catalogue.apprentissage.beta.gouv.fr/formation/:id)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id](https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire](https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/forgotten-password](https://catalogue.apprentissage.beta.gouv.fr/forgotten-password)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id](https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire](https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements](https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/formation/:id](https://catalogue.apprentissage.beta.gouv.fr/formation/:id)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml](https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/login](https://catalogue.apprentissage.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements](https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/formation/:id](https://catalogue.apprentissage.beta.gouv.fr/formation/:id)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire](https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id](https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id)
  
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml](https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/favicon.ico](https://catalogue.apprentissage.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.a8c4106c.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.a8c4106c.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/favicon.ico](https://catalogue.apprentissage.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml](https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.a8c4106c.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.a8c4106c.chunk.css)
  
  
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

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "(this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[]).push([[7],{104:funct", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id](https://catalogue.apprentissage.beta.gouv.fr/etablissement/:id)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/formation/:id](https://catalogue.apprentissage.beta.gouv.fr/formation/:id)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/forgotten-password](https://catalogue.apprentissage.beta.gouv.fr/forgotten-password)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire](https://catalogue.apprentissage.beta.gouv.fr/guide-reglementaire)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements](https://catalogue.apprentissage.beta.gouv.fr/recherche/etablissements)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/login](https://catalogue.apprentissage.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,c,d=t[0],f=t[1],u=t[2],i=0,s=[];i<d.length;i++)c=d[i],Object.prototype.hasOwnProperty.call(a,c)&&a[c]&&s.push(a[c][0]),a[c]=0;for(n in f)Object.prototype.hasOwnProperty.call(f,n)&&(e[n]=f[n]);for(l&&l(t);s.length;)s.shift()();return o.push.apply(o,u||[]),r()}function r(){for(var e,t=0;t<o.length;t++){for(var r=o[t],n=!0,c=1;c<r.length;c++){var f=r[c];0!==a[f]&&(n=!1)}n&&(o.splice(t--,1),e=d(d.s=r[0]))}return e}var n={},c={8:0},a={8:0},o=[];function d(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,d),r.l=!0,r.exports}d.e=function(e){var t=[];c[e]?t.push(c[e]):0!==c[e]&&{12:1,13:1,19:1,27:1,29:1}[e]&&t.push(c[e]=new Promise((function(t,r){for(var n="static/css/"+({}[e]||e)+"."+{0:"31d6cfe0",1:"31d6cfe0",2:"31d6cfe0",3:"31d6cfe0",4:"31d6cfe0",5:"31d6cfe0",6:"31d6cfe0",9:"31d6cfe0",10:"31d6cfe0",11:"31d6cfe0",12:"309e894f",13:"309e894f",14:"31d6cfe0",16:"31d6cfe0",17:"31d6cfe0",18:"31d6cfe0",19:"309e894f",20:"31d6cfe0",21:"31d6cfe0",22:"31d6cfe0",23:"31d6cfe0",24:"31d6cfe0",25:"31d6cfe0",26:"31d6cfe0",27:"bf6dc550",28:"31d6cfe0",29:"bf6dc550",30:"31d6cfe0",31:"31d6cfe0",32:"31d6cfe0",33:"31d6cfe0",34:"31d6cfe0",35:"31d6cfe0",36:"31d6cfe0",37:"31d6cfe0",38:"31d6cfe0"}[e]+".chunk.css",a=d.p+n,o=document.getElementsByTagName("link"),f=0;f<o.length;f++){var u=(l=o[f]).getAttribute("data-href")||l.getAttribute("href");if("stylesheet"===l.rel&&(u===n||u===a))return t()}var i=document.getElementsByTagName("style");for(f=0;f<i.length;f++){var l;if((u=(l=i[f]).getAttribute("data-href"))===n||u===a)return t()}var s=document.createElement("link");s.rel="stylesheet",s.type="text/css",s.onload=t,s.onerror=function(t){var n=t&&t.target&&t.target.src||a,o=new Error("Loading CSS chunk "+e+" failed.\n("+n+")");o.code="CSS_CHUNK_LOAD_FAILED",o.request=n,delete c[e],s.parentNode.removeChild(s),r(o)},s.href=a,document.getElementsByTagName("head")[0].appendChild(s)})).then((function(){c[e]=0})));var r=a[e];if(0!==r)if(r)t.push(r[2]);else{var n=new Promise((function(t,n){r=a[e]=[t,n]}));t.push(r[2]=n);var o,f=document.createElement("script");f.charset="utf-8",f.timeout=120,d.nc&&f.setAttribute("nonce",d.nc),f.src=function(e){return d.p+"static/js/"+({}[e]||e)+"."+{0:"938bfb86",1:"e12d2fd2",2:"c8da6491",3:"a9b2847b",4:"abb16636",5:"a1a9cdc6",6:"d4edeb6d",9:"1e2e895e",10:"6262353d",11:"6d132f41",12:"068f7ec7",13:"67c66d24",14:"0a2df2ed",16:"daca4d05",17:"666a8b5a",18:"1cb7f38b",19:"a6fdc2d9",20:"d0d17169",21:"2628d6a2",22:"9c02284e",23:"452cb9a8",24:"94bc0c76",25:"cb666050",26:"a78176d1",27:"692d21d7",28:"17f84203",29:"05024871",30:"c5c406af",31:"a6494eb1",32:"8ed7ed07",33:"4bc87b8c",34:"34e6cf25",35:"db9a1ebe",36:"14d1bbc1",37:"22958347",38:"43dd3a09"}[e]+".chunk.js"}(e);var u=new Error;o=function(t){f.onerror=f.onload=null,clearTimeout(i);var r=a[e];if(0!==r){if(r){var n=t&&("load"===t.type?"missing":t.type),c=t&&t.target&&t.target.src;u.message="Loading chunk "+e+" failed.\n("+n+": "+c+")",u.name="ChunkLoadError",u.type=n,u.request=c,r[1](u)}a[e]=void 0}};var i=setTimeout((function(){o({type:"timeout",target:f})}),12e4);f.onerror=f.onload=o,document.head.appendChild(f)}return Promise.all(t)},d.m=e,d.c=n,d.d=function(e,t,r){d.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},d.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},d.t=function(e,t){if(1&t&&(e=d(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(d.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)d.d(r,n,function(t){return e[t]}.bind(null,n));return r},d.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return d.d(t,"a",t),t},d.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},d.p="/",d.oe=function(e){throw console.error(e),e};var f=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],u=f.push.bind(f);f.push=t,f=f.slice();for(var i=0;i<f.length;i++)t(f[i]);var l=u;r()}([])</script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.8e8f4df7.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/favicon.ico](https://catalogue.apprentissage.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.a8c4106c.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.a8c4106c.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/stats](https://catalogue.apprentissage.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021](https://catalogue.apprentissage.beta.gouv.fr/recherche/formations-2021)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml](https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `22958347`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1540483477`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `22958347`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `05024871`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `05024871`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/15.f5860ded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>22958347, which evaluates to: 1970-09-23 17:19:07</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

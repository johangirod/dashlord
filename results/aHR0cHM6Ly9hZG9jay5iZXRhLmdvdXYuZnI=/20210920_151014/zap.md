
# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 15:03:33


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 4 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: style-src unsafe-inline | Medium | 4 | 
| CSP: Wildcard Directive | Medium | 4 | 
| CSP: Notices | Low | 4 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 5 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 4 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
| Modern Web Application | Informational | 6 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 8 | 

## Alert Detail


  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>img-src</p>
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>The report-uri directive has ben deprecated in favor of the new report-to directive</p><p></p>
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/stats](https://adock.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0bd39a.fad39561.js](https://adock.beta.gouv.fr/js/chunk-2d0bd39a.fad39561.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js](https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b9919.05e0c45b.js](https://adock.beta.gouv.fr/js/chunk-2d0b9919.05e0c45b.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0db095.e764a18d.js](https://adock.beta.gouv.fr/js/chunk-2d0db095.e764a18d.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b6edb.55e33e0c.js](https://adock.beta.gouv.fr/js/chunk-2d0b6edb.55e33e0c.js)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAADIAAABSCAMAAAAhFXfZAAAC91BMVEVMaXEzeak2f7I4g7g3g7cua5gzeKg8hJo3grY4g7c3grU0gLI2frE0daAubJc2gbQwd6QzeKk2gLMtd5sxdKIua5g1frA2f7IydaM0e6w2fq41fK01eqo3grgubJgta5cxdKI1f7AydaQydaMxc6EubJgvbJkwcZ4ubZkwcJwubZgubJcydqUydKIxapgubJctbJcubZcubJcvbJYubJcvbZkubJctbJctbZcubJg2f7AubJcrbZcubJcubJcua5g3grY0fq8ubJcubJdEkdEwhsw6i88vhswuhcsuhMtBjMgthMsrg8srgss6is8qgcs8i9A9iMYtg8spgcoogMo7hcMngMonf8olfso4gr8kfck5iM8jfMk4iM8he8k1fro7itAgesk2hs8eecgzfLcofssdeMg0hc4cd8g2hcsxeLQbdsgZdcgxeLImfcszhM0vda4xgckzhM4xg84wf8Yxgs4udKsvfcQucqhUndROmdM1fK0wcZ8vb5w0eqpQm9MzeKhXoNVcpdYydKNWn9VZotVKltJFjsIwcJ1Rms9OlslLmtH///8+kc9epdYzd6dbo9VHkMM2f7FHmNBClM8ydqVcpNY9hro3gLM9hLczealQmcw3fa46f7A8gLMxc6I3eagyc6FIldJMl9JSnNRSntNNl9JPnNJFi75UnM9ZodVKksg8kM45jc09e6ZHltFBk883gbRBh7pDk9EwcaBzn784g7dKkcY2i81Om9M7j85Llc81is09g7Q4grY/j9A0eqxKmdFFltBEjcXf6fFImdBCiLxJl9FGlNFBi78yiMxVndEvbpo6js74+vx+psPP3+o/ks5HkcpGmNCjwdZCkNDM3ehYoNJEls+lxNkxh8xHks0+jdC1zd5Lg6r+/v/H2ufz9/o3jM3t8/edvdM/k89Th61OiLBSjbZklbaTt9BfptdjmL1AicBHj8hGk9FAgK1dkLNTjLRekrdClc/k7fM0icy0y9tgp9c4jc2NtM9Dlc8zicxeXZn3AAAAQ3RSTlMAHDdTb4yPA+LtnEQmC4L2EmHqB7XA0d0sr478x4/Yd5i1zOfyPkf1sLVq4Nh3FvjxopQ2/STNuFzUwFIwxKaejILpIBEV9wAABhVJREFUeF6s1NdyFEcY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`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.baed62d9.js](https://adock.beta.gouv.fr/js/app.baed62d9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789ABCDEFGHIJKLMNOPQRSTUVXYZabcdefghijklmnopqrstuvwxyz-`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/css/chunk-vendors.ed68e012.css](https://adock.beta.gouv.fr/css/chunk-vendors.ed68e012.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAQAAAADQ4RFAAACf0lEQVR4AY1UM3gkARTePdvdoTxXKc+qTl3aU5U6b2Kbkz3Gtq3Zw6ziLGNPzrYx7946Tr6/ee/XeCQ4D3ykPtL5tHno4n0d/h3+xfuWHGLX81cn7r0iTNzjr7LrlxCqPtkbTQEHeqOrTy4Yyt3VCi/IOB0v7rVC7q45Q3Gr5K6jt+3Gl5nCoDD4MtO+j96Wu8atmhGqcNGHObuf8OM/x3AMx38+4Z2sPqzCxRFK2aF2e5Jol56XTLyggAMTL56XOMoS1W4pOyjUcGGQdZxU6qRh7B9Zp+PfpOFlqt0zyDZckPi1ttmIp03jX8gyJ8a/PG2yutpS/Vol7peZIbZcKBAEEheEIAgFbDkz5H6Zrkm2hVWGiXKiF4Ycw0RWKdtC16Q7qe3X4iOMxruonzegJzWaXFrU9utOSsLUmrc0YjeWYjCW4PDMADElpJSSQ0vQvA1Tm6/JlKnqFs1EGyZiFCqnRZTEJJJiKRYzVYzJck2Rm6P4iH+cmSY0YzimYa8l0EtTODFWhcMIMVqdsI2uiTvKmTisIDHJ3od5GILVhBCarCfVRmo4uTjkhrhzkiBV7SsaqS+TzrzM1qpGGUFt28pIySQHR6h7F6KSwGWm97ay+Z+ZqMcEjEWebE7wxCSQwpkhJqoZA5ivCdZDjJepuJ9IQjGGUmuXJdBFUygxVqVsxFsLMbDe8ZbDYVCGKxs+W080max1hFCarCfV+C1KATwcnvE9gRRuMP2prdbWGowm1KB1y+zwMMENkM755cJ2yPDtqhTI6ED1M/82yIDtC/4j4BijjeObflpO9I9MwXTCsSX8jWAFeHr05WoLTJ5G8IQVS/7vwR6ohirYM7f6HzYpogfS3R2OAAAAAElFTkSuQmCC`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x00002\x0000\x0000\x0000R\x0008\x0003\x0000\x0000\x0000!\x0015w�\x0000\x0000\x0002�PLTELiq3y�6�8��7��.k�3x�<��7��8��7��4��6~�4u�.l�6��0w�3x�6��-w�1t�.k�5~�6�2u�4{�6~�5|�5z�7��.l�-k�1t�5�2u�2u�1s�.l�/l�0q�.m�0p�.m�.l�2v�2t�1j�.l�-l�.m�.l�/l�.l�/m�.l�-l�-m�.l�6�.l�+m�.l�.l�.k�7��4~�.l�.l�D��0��:��/��.��.��A��-��+��+��:��*��<��=��-��)��(��;��'��'�%~�8��$}�9��#|�8��!{�5~�;�� z�6��\x001ey�3|�(~�\x001dx�4��\x001cw�6��1x�\x001bv�\x0019u�1x�&}�3��/u�1��3��1��0�1��.t�/}�.r�T��N��5|�0q�/o�4z�P��3x�W��\��2t�V��Y��J��E��0p�Q��N��K�����>��^��3w�[��G��6�G��B��2v�\��=��7��=��3y�P��7}�:�<��1s�7y�2s�H��L��R��R��M��O��E��T��Y��J��<��9��={�G��A��7��A��C��0q�s��8��J��6��N��;��K��5��=��8��?��4z�J��E��D�����H��B��I��F��A��2��U��/n�:�����~�����?��G��F�У��B�����X��D�ϥ��1��G��>�е��K�����������7��������?��S��N��R��d�����_��c��@��G��F��@��]��S��^��B�����4�̴��`��8�͍��C��3��^]��\x0000\x0000\x0000CtRNS\x0000\x001c7So��\x0003��D&\x000b��\x0012a�\x0007����,���Ǐ�w�����>G���j��w\x0016��6�$͸\��R0Ħ���� \x0011\x0015�\x0000\x0000\x0006\x0015IDATx^���r\x0014G\x0018\x0005�^�\x0002!D	\x000b�\x0010Ʈ\x0012 cpI/��x���qs�9'�s�䜃s��³��	��\x000b\x0017SS��3�ӻ����9T��~�\x001a�\x0011�_�tՍ�\x001c�?�o-UWݼbܽe�n��s�G�\x001b���_iT</p><p>[:�o�˯V\x0006�]'�\x0001ީ\x001b\x001ar�,_�xޔ����ڷn�d��3�3)�dZ�����&�n��9{\x001c���e�Gm1�,I�Z�tnf�xZT�5
�l6\x001dϻ��7�-<��ؚj@\x0015U�m(����ͷXK�|v���ZuT-���.W��\x0001�\��^۩ʃ;\x001d\x0008f]���$׎'p�|nW\x0008Bg�����]��	�]�5�!������]��W
�$�J�i(n�����O%��INRt��ry��$/q\x0016�\x000e\x0017\x0017u��Q��u+��ܕ[*ϓ����c �=��q\x0003��c��\x0019o�������\x0018G1Y�87ݒ�\x0010��r�ǘ\x0003r�\x0004A+�\x0017�ȉ��l���tM�|s��(��\x001d���٫g�������\x000bi�D�q�8�;�T:X����
(S��Ǿ!���\x0000\x001b�\x0011��iZ��\x001d\x0000���\x0016ڍ\x0005ד����\x000c%�߱�\x0010\x000e��\x000e�,�</p><p>:�A\x0008��\x0005\x001bPK��0Txl6� ±\x0011 �\x0013\x001c6�!Ӌ!8l�\x0001�</p><p>\x001b3�`��O)y\x001b8��@4�%`�y�P厓�Јs\x00043�fpΩ�\x001bxb�	��Zu���\x000e\ـj�9p^�Hl�\x0015\x000c&t�s�P�S��\x0018�\x000b6\x0013\x0013�y�.�0#}\x0005#̄�ox͏B��(-�\x0011�AGX�l�^`d���ju�i$��\x000c�\x0005ˌ:�\x0001���L�EA\x001f�D���+�Ѩ���\x000bb�z�\x0019��zQ�\x0005\x0016G�ѫՕ[�\x0011������m��\x000c(�ɂM�&�w*\x001b?���H��\x0010</p><p>���\x0003��A��\x0005{\x0008\x0005�'�\x0015o�9\x0019I�\x0005\x001cO�\x0014I^\x0000G��\x001542���\x0019���t\x0002/�H�\x0007���</p><p>��I\x0000.jB��/�l,�&5�W/����\x001a�p*>YL�THs)��M	�x�_X_<~#BQԓ���h(JX��{+2��H��(jE��]�'˲���4�\x0019Y^(E#�</p><p>E����n@�m?(ھ��n|\x001d</p><p>�����-\x0007�L�^\x00049\x0017vw\x001f��\x000f�\x001e�d,��b� ?�����I#\x0000�8�8\x0018&��1q�	C$\x0011*\x00086�%�\x001d�b�@[���)\x001e�UQ\x0004\x0011u��I\x00177'�415�o`lrM�\x0018�z�Mݛ�:�N� �&�����$O�>F\x0006�\x001fߪL��-�2�����Ӫ�1B
��U�?���]��1N
\x0013\x0001���_�Pn�"�GMOp�i���[M��I�/\x0004,j�KG��\x000b�)�\x0017���ė\x001c�4�3��2�g\x0018�i�2���Z<Oq�0�e[1�9�\x0010��12\�V�YiFZ"��(��l�\x0014�\x0012Qzh\x000cXQ��6Xe
��\x000es8S��7��F�G��w����Hx�L�����w\x0016Ve�\x001a�d\x0016\x0002�d�j��)��\x0016|�T��{�UU��\x0002Y\x0019\x000e#���	��\x0010�"K��3\x001f:,�j
�dmJ�$��\x000e|r\x0003�\x001e���Z2�x�H$�O�%;=\x0001���f�u>���\x0004ٚD�K'�'�4w�~�7\x0011�\x0006'fZ6\x0005n\x000b�\x0001rЋs����eyވ8\x0019\x0008bK�2���(l�Y\x001f9�ǩ d?6e��:F�Y�3#�k,r��cD\���-f�w��\x001e\x0019'r��R~W���=�\x0007�ո�)\x0018�f�ݠ\x001f{Ҿ���KE�=D�ʔ$=S�J�4=�g\x0004Ń��n���\x0011�H�ݖʅB�\x0004̐�ֻ-�uED�f��J��\x0014q\x0012�Q�r�\x001c1���c`��0��\x0013\x000cQ7��y�+Q J�	\x0001!��Gݚ�%\x001b�\x0000\x0008�W@h3)\x001a\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js](https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FROM`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.baed62d9.js](https://adock.beta.gouv.fr/js/app.baed62d9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0bd39a.fad39561.js](https://adock.beta.gouv.fr/js/chunk-2d0bd39a.fad39561.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js](https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 9
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected 2 times, the first in the element starting with: "(window["webpackJsonp"]=window["webpackJsonp"]||[]).push([["chunk-vendors"],{"00ee":function(t,e,n){var i=n("b622"),r=i("toStrin", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/stats](https://adock.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.f5ca6f36.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js](https://adock.beta.gouv.fr/js/chunk-vendors.f5ca6f36.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.f5ca6f36.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.f5ca6f36.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.f5ca6f36.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.f5ca6f36.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b9919.05e0c45b.js](https://adock.beta.gouv.fr/js/chunk-2d0b9919.05e0c45b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0db095.e764a18d.js](https://adock.beta.gouv.fr/js/chunk-2d0db095.e764a18d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/favicon.ico](https://adock.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b6edb.55e33e0c.js](https://adock.beta.gouv.fr/js/chunk-2d0b6edb.55e33e0c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js](https://adock.beta.gouv.fr/js/chunk-22c07800.13eab677.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/css/app.1cc66a26.css](https://adock.beta.gouv.fr/css/app.1cc66a26.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0bd39a.fad39561.js](https://adock.beta.gouv.fr/js/chunk-2d0bd39a.fad39561.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23592600`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/css/chunk-vendors.ed68e012.css](https://adock.beta.gouv.fr/css/chunk-vendors.ed68e012.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `70710678`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `40075017`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15496570`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20037508`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18764656`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0511287798`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.d84473c1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `314245179`
  
  
  
  
Instances: 8
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>23592600, which evaluates to: 1970-10-01 01:30:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

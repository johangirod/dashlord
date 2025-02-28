
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 07:46:24


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 1 | 
| Cookie without SameSite Attribute | Low | 3 | 
| Cookie Without Secure Flag | Low | 3 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 6 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 7 | 
| Timestamp Disclosure - Unix | Informational | 586 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf_link" href="https://visio-agents.education.fr" target="_blank" rel="noopener">https://visio-agents.education.fr</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.cnil.fr/vos-droits/vos-traces/les-cookies/" target="_blank" rel="noopener">http://www.cnil.fr/vos-droits/vos-traces/les-cookies/</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#sdTZ`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#sdTZ</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/9.Enregistrer_une_r%C3%A9union_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/9.Enregistrer_une_r%C3%A9union_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ë¥b!Iy"ÍÏ}ù ê3\x00128\x0016Ã°|î!IßßÝÞ\__¥øy,\x001a\x000e¡\x001e§Bô\x000e\x0000
ÇâñX4\x0012ÏBÁàéÉ1\x001a\x0008øýG¾C¯÷Àãv9íV£¤'"`\x0017h´¹<\x001ep¬Ëét8ì6Íj±ÍfÉh0\x0018ô\x0008¢Ói5";>¾S\x0015j-¢×Ó\x0007ë´`4\x001a\x001eJIB¡þ\x001f"À*cÃ7\x0003­G\x001a¸bw8v\x000fó\x0017ÇÂ\x001dØ
endstream
endobj
163 0 obj
<</Type/XObject/Subtype/Image/Width 396/Height 306/ColorSpace/DeviceRGB/BitsPerComponent 8/Filter/DCTDecode/Interpolate true/Length 17181>>
stream
ÿØÿà\x0000\x0010JFIF\x0000\x0001\x0001\x0001\x0000H\x0000H\x0000\x0000ÿá\x0000bExif\x0000\x0000MM\x0000*\x0000\x0000\x0000\x0008\x0000\x0004\x0003\x0002\x0000\x0002\x0000\x0000\x0000\x001c\x0000\x0000\x0000>Q\x0010\x0000\x0001\x0000\x0000\x0000\x0001\x0001\x0000\x0000\x0000Q\x0011\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013Q\x0012\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013\x0000\x0000\x0000\x0000Laptop Internal LCD Monitor\x0000ÿâ\x0004\x001eICC_PROFILE\x0000\x0001\x0001\x0000\x0000\x0004\x000eWin\x0000\x0002\x0010\x0000\x0000mntrRGB XYZ \x0007Ù\x0000\x0005\x0000\x000f\x0000\x000e\x0000\x001e\x0000\x0000acspMSFT\x0000\x0000\x0000\x0000LNV\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000öÖ\x0000\x0001\x0000\x0000\x0000\x0000Ó+LNV \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0011desc\x0000\x0000\x0001P\x0000\x0000\x0000vdmnd\x0000\x0000\x0001È\x0000\x0000\x0000admdd\x0000\x0000\x0001P\x0000\x0000\x0000vvued\x0000\x0000\x0002,\x0000\x0000\x0000view\x0000\x0000\x0002´\x0000\x0000\x0000$lumi\x0000\x0000\x0002Ø\x0000\x0000\x0000\x0014meas\x0000\x0000\x0002ì\x0000\x0000\x0000$rXYZ\x0000\x0000\x0003\x0010\x0000\x0000\x0000\x0014gXYZ\x0000\x0000\x0003$\x0000\x0000\x0000\x0014bXYZ\x0000\x0000\x00038\x0000\x0000\x0000\x0014rTRC\x0000\x0000\x0003L\x0000\x0000\x0000\x001egTRC\x0000\x0000\x0003l\x0000\x0000\x0000\x001ebTRC\x0000\x0000\x0003\x0000\x0000\x0000\x001ewtpt\x0000\x0000\x0003¬\x0000\x0000\x0000\x0014bkpt\x0000\x0000\x0003À\x0000\x0000\x0000\x0014tech\x0000\x0000\x0003Ô\x0000\x0000\x0000\x000ccprt\x0000\x0000\x0003à\x0000\x0000\x0000.desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x001cLaptop Internal LCD Monitor\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ\x0011\x0001\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0007Lenovo\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ \x000c\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000,Reference Viewing Condition in IEC61966-2.1\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x00004\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x00003»@\x0000p\x00064\x0000Í\x0000\x0000\x0000\x0000\x0008\x0000\x0000\x0000ù\x0012\x0000\x0004\x0000\x0000\x0000\x0000ðý$\x0008\x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x00008B\x0000Ê\x000eC\x0000Ù·@\x0000øuB\x0000\x0000\x0000view\x0000\x0000\x0000\x0000\x0000\x0013¤þ\x0000\x0014_.\x0000\x0010Ï\x0014\x0000\x0003íË\x0000\x0004\x0013\x000b\x0000\x0003\\x0000\x0000\x0000\x0001XYZ \x0000\x0000\x0000\x0000\x0000L	V\x0000P\x0000\x0000\x0000W\x001fæmeas\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000\x0002\x0000\x0000\x0000\x0002XYZ \x0000\x0000\x0000\x0000\x0000\x0000\\x000b\x0000\x00002\x0000\x0000\x0008QXYZ \x0000\x0000\x0000\x0000\x0000\x0000t4\x0000\x0000½\x0010\x0000\x0000\x0011eXYZ \x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x0010_\x0000\x0000¹curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x0019\x000c+\x001d;6yVä~\x001c´ëÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002	\x000b»\x001e\x00199
[Ps¹´ÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x001e\x000bÛ!Þ>(aðaÀèÿÿ\x0000\x0000XYZ \x0000\x0000\x0000\x0000\x0000\x0000óQ\x0000\x0001\x0000\x0000\x0000\x0001\x0016ÌXYZ \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000sig \x0000\x0000\x0000\x0000AMD text\x0000\x0000\x0000\x0000Copyright (c) 2005 Lenovo Corporation\x0000ÿÛ\x0000C\x0000\x0008\x0006\x0006\x0007\x0006\x0005\x0008\x0007\x0007\x0007		\x0008
\x000c\x0014
\x000c\x000b\x000b\x000c\x0019\x0012\x0013\x000f\x0014\x001d\x001a\x001f\x001e\x001d\x001a\x001c\x001c $.' ",#\x001c\x001c(7),01444\x001f'9=82<.342ÿÛ\x0000C\x0001			\x000c\x000b\x000c\x0018

\x00182!\x001c!22222222222222222222222222222222222222222222222222ÿÀ\x0000\x0011\x0008\x00012\x0001\x0003\x0001"\x0000\x0002\x0011\x0001\x0003\x0011\x0001ÿÄ\x0000\x001f\x0000\x0000\x0001\x0005\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000bÿÄ\x0000µ\x0010\x0000\x0002\x0001\x0003\x0003\x0002\x0004\x0003\x0005\x0005\x0004\x0004\x0000\x0000\x0001}\x0001\x0002\x0003\x0000\x0004\x0011\x0005\x0012!1A\x0006\x0013Qa\x0007"q\x00142¡\x0008#B±Á\x0015RÑð$3br	
\x0016\x0017\x0018\x0019\x001a%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚáâãäåæçèéêñòóôõö÷øùúÿÄ\x0000\x001f\x0001\x0000\x0003\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000bÿÄ\x0000µ\x0011\x0000\x0002\x0001\x0002\x0004\x0004\x0003\x0004\x0007\x0005\x0004\x0004\x0000\x0001\x0002w\x0000\x0001\x0002\x0003\x0011\x0004\x0005!1\x0006\x0012AQ\x0007aq\x0013"2\x0008\x0014B¡±Á	#3Rð\x0015brÑ
\x0016$4á%ñ\x0017\x0018\x0019\x001a&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚâãäåæçèéêòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0001\x0000\x0002\x0011\x0003\x0011\x0000?\x0000÷ú(¢
(¢
(¢
(¢2õ\x0019R(ÁÂ¾w\x000f\cük"°¾/øQðÞ¥\iÏ\x001aÉ5ÃDÞbn\x0018ÛéYS]êÖó42øª\x0011"\x001c0]\x000eV\x0000û\x0010pk¢~óGeEcÙè\x001e+¾´êßÄö&\x0019Wr\x0016Ó\x0019N=Álþ\x0011_\x0018ÿ\x0000ÐÍ§ÿ\x0000à¸ÿ\x0000ñu~Ò!¯cJÍÿ\x0000WÆ?ô3iÿ\x0000ø.?ü]qÞ>Õ|YàHì\x001eMVÆóíê\x0002ÙìÛ´\x000fözÐªEèÝÚ=\x000eðø[\x001e'ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×ªº3öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ)È\x0014È¡ÉU$n#°ï^\x000bÿ\x0000\x000b_Å\x001fóÒÓþüõèÿ\x0000¯âùéiÿ\x0000~?úô\=´O~8#¹Ù\x001c¥¢ÈËzôëEÔpÅ6Ø$2&Ðw\x001f_óð\x001føZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×©ùµô\x0005ÂÃ\x0004¨mgv8ÎãÕ\x001cWB¾5cÜ\x0003_.7Åo\x00142\x0013[)<nX\x0006G¿5ôý©-g\x0001=LjOåYUÙ\x001aSÐ(¬M( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000f!øûÿ\x0000 =\x0013þ¿Oþ^­~&P¢C	`ÀàWü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A®î×L=N;£¯j\x000f\x0018!©Ûå.W;O\x0019ÇãZ^ÑFKã#<¿2p^3ÆZZT\x001byæ&³#vÖ8ïÝÿ\x0000Bÿ\x0000 Îÿ\x0000)þ5jÏTÓõ\x0016u²¾¶¹(\x0001a\x000c¡öç¦qKÈ»\x00153uë/ë^CñàËö=\x0007ÍÝ6|nú%{¥xí
ÿ\x0000\x001eÞ\x001eÿ\x0000®ÿ\x0000$§\x0019]U{ðñN]»q!sÉ\x001d4V§"\x0014i0Ì$R^D®2\x0018\x0016\x0019\x0006·8mwaæßDÏË{!\x001eÿ\x0000þªO³è¿óúÿ\x0000ÿ\x0000Z¾>\x0011ðÖãÿ\x0000\x0012
7¯üû­'ü">\x001bÿ\x0000 \x000eÿ\x0000ëV±qKàAõ	ÿ\x0000ÏÇý|¯RÊ6Ai;H\x0008ù³Úªdzú³þ\x0011\x001f
ÿ\x0000Ð\x0003Nÿ\x0000Àu¥ÿ\x0000;Ã¿ô/éÿ\x0000ø\x000c¿áXÊ²½¬m\x001c+µî|¥ê(Èõ\x0015õið\x0007]\x0003N\x001föî´ðøoþ:wþ\x0003­O´E}]÷>SÈõ\x0014¹\x001eµõ_ü">\x001bÿ\x0000 \x000eÿ\x0000ë\åß´%ñÊÛ®b þËó<±\x0008Û»ÍÆqë)©Ý*
+ÜùÛ#ÔQê+éá\x000f\x0000IÑ4ð\x0007$ù\x000bY§ølIáë\x0012¾JçùSsHJ{\x001f<äz\×Òéá\x000eI\x001aºhyV\x0019\x0007ÈZó¯\x0011é\x001al\x001e%¾\x001b\x000bxãRQc\x0000\x000fRÔUÎ|D½9å´W~të\x0010	6\x00009? ¬Ï·h[\x0016ÉÔù\
Zû#\x0018§Sàg'Iê+µ´:MìÛDY\x0006y\x000cQ^çáo\x0008ørçÂzLóèZ|Éi\x001b;µºÄ¨É'\x0014*«±Ó­'\x0016¬×så|QFG¨¯¤¼iwàO\x0004ý/<3gq=ÎJE\x0015ªd(êÄ:àU¯\x0007'<i¥=åìbhË\x0019-(ØÏP9\x001eõ^ÓÈêú»ÚçÌy\x001e¢Q_TxÂ>\x001c¶ðåä°èZ|r(\2Û¨#æ\x001eÕq¼\x001dáÇþ)ý7¯üû­/hêîû%äz2=E}W?|/\x000bmÿ\x0000{Mfïþ¼~è<-áyÔáí4\x0011Ô\x001bu®(æ¸Y×xhÏß]?­
\x001e
¢7Cå<Þöï\x000e¥øNÒm?K´µ¯UKÃ\x0010RFÆã#µxz\x0011wW9§\x000eG`\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Î¯Cl6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ×iÿ\x0000	\x0004V·\x000c?á\x001e×&p\x0002\x0019c´Ü©ÏJâþ>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö½ÇÄ+ë\x000f6þ\x001cm61cÑ§bCá\x001dã¶ÐMo
rtè"\x0011r¨Ò5"¾Ñ¥8ÿ\x0000á\x0008¿Mì\x0017séH\x0015sÜJê­të\x001b\x0016f´³··.0Æ(3õÀ®)ü©,¬CC*\x000fÜóþålkx³þü\x0018/ÿ\x0000\x0013Y4ÊM\x001d5xí\x0001+I\x000e¦'MN\x0001nÂr+Ôlõ\x001f\x0012Ky\x0014wz\x0004\x0010[³bIVõ\¨õÆ9¯-ý ¿æ	þü¿ÉiÃâ"¯ÀÏ\x0014\x0015¯áoù\x001b´oúýÿ\x0000C\x0015+_Âßò7hßõû\x0017þ+w±Â·>¯o¼~´­÷Ö¹DóOÞ(¿Ó\x0005¤]M
ÜÀË?\x000eÿ\x0000/¢àöÉÏOJòW¸×¤l½Æ¨ÍêZZõÏ\x0019X¼¾=±¿´;\x001b&YW8\x0005;TÙ
Â KÉ_N79vÂã\x0012å0;îÇOÂ¹êb9\x001d¹èað\x001eÚ\x001cÒm|º\x001c×Ã\x001bÝro\x001bÛÛI¨Ü\x0008\x0004nóÃq+\x0011"Ð\x0003ß$\x001fÀ×º×è6ò\x001f\x001fé­Ë\x0005Fµ=ªw"1\x0018\69Ý»½zk	©Æç%j.ÜB¹{Ïù(Kÿ\x0000`ý­]Er÷òPþÁ\x001fûZµç=OÑ<ÈÙ?¼\x0008¬q§­·É|\x0004(Ù
0\x000e=+VçÌ0â#b\x0001>¹¨VÖ\x0005\x001cD¨­ÒÂ£§J\³ê&2Kmµ8ÚHÛè;Wø£þF­Gýäÿ\x0000Ð\x0016½\x0016\x001bx`ÌA·pÚ@é^uâù\x001aµ\x001f÷ÿ\x0000@\x0014äï\x0003ÊÌg\x0019Ñæs!âYÐÂÇjÉò\x0013è\x000f\x0015ÓøÁZUÆ%ÅÃ%¤Ñ*¤¶ñ\x001eÝ\x0006ÜüÙéYÐh²>-ìÈÄ!x¡B\x0001p;z
ÔºÙ¨h\x001am¥ÓÞÌ\x001a9fhÛp\x0018\x0016Olð:ñXëÐ¬­Î\x001aq¾W}O?Ó,
­ôÄ®\x0002D¨\x0008þ"y'ô¯£¼\x001fÿ\x0000"fÿ\x0000^qè"¼SSÓ¤Ón\x0004NÁÕ*àc5í~\x0010!|\x0017£@\x0002Ê"Iÿ\x0000tVÜ2êY¹ïdbxFû_ã½\x000f0\x001bu\x0001\x0001Y289?Oàí#û?PÔ®R<Gr±«\x0015\x0001T2\x0016\x0018\x0000\x000fFæ_ñ\x0005µÄ&Þ5\x001eVïõ¬psþÍO¡x\x0015¶Úæ#\x0000^\x0011û\x0011þ×¡¬\x0014\x001fµæ¾²ó,3¤©'¯ÎÞ·/x»þEkï¢ÿ\x0000èb®·ßo­Rñi\x0007Â·¤\x001c«ÿ\x0000\x0002Zºß|ýk§¡=L]J	\x001aõH"ÜàtîjM$\x0014m¦C 	Äç8ïPßÊ·32\x001c4cåÇ­2Úvµ#Ë\x0000'B¸í^T°öqIZW½µ³»6ßÜSÌ(û7\x0017¾ßðN?ãü_õþ¿ú\x0003W×¿|q!¼\x0015bÃ¡¾R?ï¯\x0001¯nÂpWøÀu\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®küªjô/
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5Pñ^³mñ\x000e×IJ´`"_6X	%H\x0007Ì\x000fÓÛÛÖ¨|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­ÛÝgÄ¶~2¶Ú³hyr Ü¥H\x0019mØÎìö®6åÒÙîe\x001a\x0015vní-7$\x0015x°JÊº$D\x0006 \x001f³ÜtÏûµ¯çøÛþ|ô?ûý/øV3ê;óX-[w\x0010\x000fØûgþºÖÇÙ¼mÿ\x0000A-\x0017ÿ\x0000\x0001dÿ\x0000â«\x0016YbÎ_\x0016\x001bÈí®¶Å¿xÑK!p=\x0018Íyoí\x0005×Eÿ\x0000~_äµê6vþ,[Èöÿ\x0000J{`ß¼X­ÝXb[òïÚ\x000b®þü¿ÉhÄ©ð3Å\x0005kø[þFí\x001bþ¿bÿ\x0000ÐÅd
×ð·üÚ7ý~Åÿ\x0000¡Ýìp­Ï«Ûï\x001f­%+}ãõ¤®cÑ9¯\x0010éXy5\x0018'\x0002EÇëYqhñÉ§Á}hªC@~÷Ó\x001eõÖêöÚmÜ]\x0002Ñ`\x0019.Ojó×%KäT±*¥Fä\x001e®\x000cE5\x0019s.§­ÇF_¸ÒqWé±Ðh:H».äùbÆÕÇÞ#ú
ë«'@Õ¬õ+C\x001d¬m\x0011\x0000Ñ·aëZÕÕFl>¶1bß´¼z\x0005r:¥½ýÏã[\x000b uÒrÍ4F@GÐ\x0000F+®®|ÿ\x0000ÉDÿ\x0000¸7þ×­á¹Ï%ua£Kñ\x0001\x0018mOMoOô7\x001fû=6=7\eùu].LpJÚ·ôzÇ·w6~\x0015íehÙäHÝàí9È\x001fZæm4y´]*ßWÓüèo¡Ì\x000b\x0012(\x0019`GÒÜT¬ÑQÁB¢ægYý¯vÔ´Ð{\x001f²?ÿ\x0000\x0017\èðF¥«ëw÷êÖ{ãQìµð½ï^\x0014XcF\x0015Ô0ú\x0011­¤ÿ\x0000Çæ¯ÿ\x0000_Cÿ\x0000E%9E(ès¼5&¹ZÐÁo
k9f:ÆªWiÍ£`\x000fûî³ô_\x0001ÞhöfÏOÖôâ¥~ÌYç\x000fQüaFÐ4û%¬sÜ\x0014áUxü2Gé\7ÃK{/\x001fé²n$7³\x0011Cc­cÌ«	\x0017\x001b¥¡èzõmM#Iµ%Ør¥lÛ?ú\x001dZÒ-|E/lm\x0013SÓÖÜ[¢\x0001öGÝ´\x000c`þÕÙµ ÿ\x0000È¿aÿ\x0000\EkN)Þæ\x0012¡N\x001f
ßs\x001bþ\x0011Íc?ò\x0011°ÿ\x0000ÀWÿ\x0000âèÿ\x0000sXÿ\x0000 þ\x0002¿ÿ\x0000\x0017[Wv/t\x0012Ká·
\x0000òX\x000c¹Îsø
u¼­,^tÓ[à\x0018b\x000bgÃéÅf§\x0007WÙòüÍ\x001e[EQöWìsÚÝ¿l|){\x0019ÔìdT\x001dÙó÷\x0000ïâÚßp7zO=qjãÿ\x0000g­\x0016È©¨ÿ\x0000×1ÿ\x0000¡
Äo¼~´ë{Hò±uêQå7d@.ü@å¾íÞOþ.µøuKÿ\x0000Ày?øºÁñEö¥5­¼\x0017RZÀ¨ò\x0019#$\x0016¢¯\x001d±çü+\x000e¹¤ø¢;+¶í§\x0016bÈp2\x0008'¡ÿ\x0000\x001açöØÖ\x0018\x001cDð[RV×§bÿ\x0000ÄëýfãÃ\x0016_Ídöét¥\x0016\x0008YX\x001d­Ô<W×«üOÿ\x0000rÛþ¾þÕå\x0015ÛEÞ\x0004aêJ¤/ \x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Uz\x001dømÙ5\x0014QY\x001daE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­{É<imãÛYá\x0013¾<±² \x0019\x000cd\x0000À»³¥d|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­\x000bÝ\x001bÆ©ñ\x0016ÛX¶ºM\x0011|¼C\x001cÜlÚ\x0003!\þ5ÑI¥\x0017vÓÌ¬3ýôõ4^/\x001fù­¶àÜqòAÓ?Z×þÆñGý
Kÿ\x0000ôÿ\x0000\x001aÆ}\x0003Æ¦V+­J\x0010±ÇúZð3ÿ\x0000\k_þ\x0011]Sþý_þùÿ\x0000¬fÏJñ\x000c7Iuâ5¸[/\x0017Ø7LÅyoí\x0005×Eÿ\x0000~_äµê\x0016^\x001dÔ-oa_\x0013êw)\x001be¡Gµý\x00175åÿ\x0000´\x0017]\x0017ýùÑ\x001f\x0013Sàg
×ð·üÚ7ý~Åÿ\x0000¡È\x0015£ ÜÃeâ-2êáöC
ÔrHØÎ\x00140$Öïcn}jßxýk\x000bÄ¾#Ãöv	n¥Ï\x0016ñãíY\x0012üVðr£ºjF\x0000A\x000bÇÓ8¯2ÔüYi«j\x0012Þ\ßÆdð\x0006p£²:
æj]\x0011XÜL©ÂÔÛü
-CX¿Õ.¾ÑwpÎãî¯E_`;V\x0015åýÿ\x0000ü$VX\x0002 ¼&xaüDÑýµ¦Ïì_¯øVmÎ§jÚÕ¬és\x00191nxÎsÚ¡BWÕ\x001e-
u%9Jq¾CªþêÞénmçxe_ºÈqô?\x000bøÐjr¥¢\x0016;¶â9Wúc±¯$þÚÓ?çö/×ü*UÔ­AVY=U7üúP£%Ð0ÓÄaåxÅÛ±ô5sçþJ'ýÁ¿ö½aèß\x0013tc¦Æº­Ì©v+\x0015¶ú7\x000bÖ«\x001eøwþ\x0013?í\x000fµÏö_ìß#Ùdûþnìco¥m\x0004î}"©\x0019EHé<NÚTÐÚYj\x0017°A#ÜG,QÊØó6GÓ¯4_¥µ®¥s9+\x0012ÂUÝyÂtÏ\w¯\x001cñ¶¼!ñ<·ÆSk\x001a¬VäÄãå\x001cç\x0018ã$Wàø­.wg;4×RÅäÇvc!Ñ\x000fÞÏ\x001f1Ç\x0000ûÕÎÚe¬CqG°è¶¬éÜém×÷}0ÊGb;\x001aIÿ\x0000Í_þ¾þJðO	xçÂÚ¸¸A$án!\x0008ß2ú>ðí^gñ\x001fÃV²j2ÍæDeo\x001eZîñÈ"E¦ªÝ³{Æ¶zmç¤[÷Xä_Ùñ\x0012v\x0000wÏCí\·ÃÈ´û­RkÛ«;k]@\x0000¶öñ.\x0011@ûÌ¹'æ&¸½OÄ¿ÚúÞ]\9v?*ùoÇ`8àVN}\x0015½¸\x0006Icu~GÈÉÈ â¹\[w±ç¼Ï\x0010¯É\x000fvë½úßô>\x001dk\x0013Aÿ\x0000~Ãþ¸ä¼7ñ?MK\x001f'[ºM\x0019ÂL-äo1}ð½GëTåø¦ÙxF+}6I¤ÔB5
nàF{¶Hç\x0015ÓE;~Ö5"¤´;=WÆ\x001a/ïíl5+è!ì)Â®\x0007W=\x0014\x001eÙëOÑ|S¤ø¥.eÒ®u¶Äø\x0004r;õSØ×ÎZ±:×æ\O"Ë£fõÉ\x001djÆ©\x000eKi­.~Ç4J6à2ýGNEv}Z5Ôµ·È·?wçÐ\x001e,ÿ\x0000SQÿ\x0000®cÿ\x0000B\x0015ßxýk\x0016ûânªx:x..Ö-FX´+\x001b\x0015,\x0018r\x000e:\x001cf®hþ8ðbÜ5Íîµ\x0012ÎR6þcê~Zóñ\x0011nI#ÊÅÑZK\x001aFÙaàyrÌ\x000bDáw8ê\x0007½Gg\x001cR	&\x0017x)\x0019;\x000f\{uük\x001fÆþ1ðî«u£\èÚÕ¤weÌ\x0017&\x0016Ìp°\x0019'+Î\x0008àsÉ®«OñÏÃm*\x0007ÏV¶J\x0000¼©7J@ÆXíäóÖ¹ýçæ=9B?QXHÔ{ß¥½>ýN\x0003âüßõô?ô\x0016¯(¯Føâ\x001d\x0017UÓ\x0012ÓK¿[£\x001dÖàU\x0018epFy\x001eâ¼æºè¦£fy¸h¸Ó³\x0001Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍ|T:¨¯µlÿ\x0000ãÊßþ¹¯ò¥W¡èa·dÔQEdu\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001eCñ÷þ@z'ý~ý\x0006µï|9®\x001f\x001eÚë6ñÉ\x0008\x0011¸¶óö¸@\x0000eÛÓoSZÈøûÿ\x0000 =\x0013þ¿OþW/¼ òüKµÖíõËOµb)ÆIvË \x0010?ÙÆN1ë]4dã\x0017gm\x001fKªjuuW³^£ø3Ä
+0×e
X}®n\x0006kcþ\x0010¸qÎ·®ÿ\x0000àsa?"iY·\x0010\x0005Æ$õÿ\x0000®µ¯ÿ\x0000\x0008W=fÿ\x0000Àù?øªÅ³K\x0017lü+\x0015äW+«k\x0012ÛpI¯\x000b#}F9\x0015å?\x001fÜ´=\x0015ß\x001f­z<?e}
Í±Ï·&o$a¡l\x001aòÏßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¢?\x00115>\x0006xÐ¥¤\x0014µÐp0¢(\x0010QE\x0014\x0000÷\x001bé_^é·Ö\x001aW4ÛýBh­íb±É,\x0017(£Ä×ÈM÷\x001bé_UßZÛ_|+¶µ»³ò	lmÕà·m®Ã	Ðþ¿D¹n¹¶:pýMHüYáÉ´íXµ+g°ó|=A+¿®:Vµ¬¶×±\Û\x0019T:8\x001c0=
yÍ¥\x001eºChÇHfÜÜ\x001fîÚ\x000b`\x0002s÷À­í+ÄÑZéÿ\x0000dF½mG\x0014,\x000b3Ú08äß¥sÏøáéÜô?uìüý{Xë|´þâþTyiýÅü«ÿ\x0000á~Îîl²H\x0005c|¯\\x0013»\x001d\x0007\x0019ã½uä\x0003ëAZq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*ð\x000f \x000f\x0013é \x0000?Ð§ûæ¾¯¾?ÈÑ¤ÿ\x0000×ÿ\x0000ÐÍ]?Æ¿Ày-\x0014Q]\x0007\x0008QE\x0014\x0000QE\x0014\x0000\x000e£ê+í[?øò·ÿ\x0000®kü«â¡Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍcW¡ÓÝQE\x0015Ö\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000y\x000fÇßù\x0001èõúô\x001a½}á]2oÖº¤:ü1jÅ0²s¸(\x001c\x001cú\x000f»T~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö£§ømü}hßÛ/m­9ü\x001eäÞ\x0000Ç=\x0003¡5ÕEµ\x0017fö{\x0018{IB­ãmÖû
þ\x0010ð¡µë\x0000K\x0012Aò=zVÇö'Ãßîhÿ\x0000÷ýøªÇÏÀ\x001es×Ð6âXy±õÏ#îV·ö§Ãùë¡ß´ÿ\x0000
ÁÜÔ·§é>	P]=4±x­¼©¶ïaó/ßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¯LÓµ\x001f\x0003K¨Á\x001e&o\x0019±\x0008\x0010>ïl\x000eµæ\x001f¿ãçKÿ\x0000yÿ\x0000ô\x0011N?\x0011\x0015>\x0006xÐ¥¤\x0014µ¹ÂÂ( AE\x0014P\x00027Üo¥}wc\x0002\x\x0017KK O²[3<_{\x0000)Çã~5ò#}ÆúWØZ4o/4Ä;ÚÆ\x00100Û{ÖUN¬6ìÈ·Ðè¬1xQ*\x0004\x001bYNÖlOqÀSÛ\x001dóV5
\x001b^¸Îä<)ó\x0018©ÎÓÎÝ¹ÁÀ\x001e£<Ö\x0016·ð8T;#÷·,Ùôã\x001f_¥k\x000càg\x0019ïÄê0,|9qgª%ãjJË´L\x000e\x001c\x000bsì+ ¢\x0000(¢\x0000(¢\x0000(¢\x0000+çïßò4i?õäô3_@×Ïß\x001f¿ähÒëÈÿ\x0000èf®Äc_à<(®(¢\x0000(¢\x0000\x0007Qõ\x0015ö­üy[ÿ\x0000×5þUñPê>¢¾Õ³ÿ\x0000+úæ¿Ê±«ÐéÃnÉ¨¢Èë
(¢
(¢
(¢
(¢
(¢
(¢
(¢<ãïüôOúý?ú
]Ôcð}×ÄKXeî\x001dttPaó\x0002 çø±nêÇßù\x0001èõúô\x001a¹}yá	¾#ÛYÍetÁ1!¼°¾fÐT\x0011¸ÀÜ\x0007ø×M\x0015x½\x001bÑì`¥\x0008Õ¼µ].^{\x0003´úàÇ<ÜuÍkÿ\x0000Âaá?_üþ&±ßTðp³¡j%Ã\x001cm'\ýk{þ\x0013{Lq¤kø.zÅ£QÖ>(ðÝåô6öññ#mý\x0011×©^+Ë~?ÇÎþóÿ\x0000è"½^ÏÅ¶×·[&«ÆÒ¶ÐóXº úÐW|~ÿ\x0000/ýçÿ\x0000ÐE8üDÔø\x0019ãBRÖç\x0003
(¢\x0005\x0014Q@\x0008ßq¾öOÿ\x0000äVÒ?ëÊ\x001fý\x0000WÆÍ÷\x001bé_døoþEm#þ¼¡ÿ\x0000Ð\x0005eTêÃnÍ:(¢±:( \x0002( \x0002( \x0002( \x0002¾~øýÿ\x0000#Fÿ\x0000^Gÿ\x0000C5ô
|ýñûþF'þ¼þjéüF5þ\x0003Éh¢è8B( \x0002( \x0000u\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®kü«\x001a½\x000e6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ÕÛýoÃ²|F¶Òît"o¿u\x0013j
ûX1PG\x0003¨Æ\x0006jÇßù\x0001èõúô\x001aÒÔ<E`~ Zé\x0017
´\x0008ã71(Ê\x001b?Ü\x001fZé£\x001ehËKèúØÆ3P¬vÕl®þCßÄþ\x0019Y\x001f	Æ\9\x0019ò­ù9ÿ\x0000zº/øJïèTÖïÿ\x0000â«\x0005üq
ÌÉÿ\x0000\x0008Õ±!ÏÚ\x0013Ý®k$Ç\x001e\x0011ü\x0018GX´h¬üGwuy\x0014\x000fáÍVÝdl\x0019eTÚç
^Oñûþ>t¿÷ÿ\x0000A\x0015ß?Äxlµ(í5kk;\x0010[\x00121Ô¢ÇõUæ¼Ûãn©a«e\i×°]B]þhd\x000c\x0007Ê:ã¥8üDT~ã<RÒ
ZÜáaE\x0014P ¢(\x0001\x001bî7Ò¾Çðã(ð¾\x001fñå\x000fö\x0005|rFA\x001eµè¿\x0018µ»K8-O°e5I\x000f\x0014\x00003Ïµg8·±½\x0019¨^çÒÛ×ûÃó£zÿ\x0000x~uóü.­wþºwäÿ\x0000ãGü.­wþºwäÿ\x0000ãQìÙ¿·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüëçÿ\x0000¤\x001f\x0014i89ÿ\x0000B?ú\x0019¬ÿ\x0000ø]Zïý\x0003tïÉÿ\x0000Æ¹_\x0015ø¶óÅ÷×7¶ðBÖñÔC\x0010NyÍT`Ó¹Z±l~(­NP¢(\x0000¢(\x0000\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Æ¯C§
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5gRñý¿Ä]\x000eçEµ},\x0008Ï,D¹R\x0001ó\x0003tÀ=½«[âfñf§ZÁtí\x000cÍ)gRÙã\x0018ãë\¹ðçÊ>9r£\x0018\x0006\x0010qÓOáz_G¹d¡Q¶¾ã©\x0019øJÈº\x0014D\x0006 \x001cOÏ?õÎ¹O>2ñ6a\x000eq\x0005¶÷]ä´¸gc\x0018à®p1ü©ÿ\x0000ðüCÿ\x0000¡òOûõÿ\x0000Ö¯6ñDü$ïkâ
VmJK\DgèB»\x0000{\x0013YÊ\x001cºnÆ\x0015¼\x0006yÖ5\x0007æ<3Z\x001a®¶Qcrñ\x0013\x0019y\x0015½g§Z[Á}ÃÌ_õ¹ÁïíRjv2Im6`VUPÍÓ,@É\x001e­s{Væ­±Ü°ª46ç²ír\x0007jJôßøS\x001aS¬[ß¦ÿ\x0000\x001a_øS\x001aý\x0005í¿ïÓwÙ+§+ìy\x0015éßð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a?áLj\x001fô\x0017¶ÿ\x0000¿Mþ4Y³cÌh¯Nÿ\x00001¨Ð^Ûþý7øÖø} è\x001aUºê¶ï©_ÌìK¬ï\x0012*\x0000)Iò«±ªRnÇÖ§ô\x000bß\x0012êñé¶\x001e_à±i\x001b
ª:ÿ\x0000Ö¯Dÿ\x0000{Âô/ü
üj[m'ÃÖ7	sg£Ëoq\x0019Ý\x001c±ßK>½j\x001dDZ¡+êy¦¿¡ÝøsZK½1¡Á-\x0019Ê°# Â³k×n´\x000eß\Éuy£Ëqq!ÌÉ})f>½j/øG¼)ÿ\x0000Bùÿ\x0000ÀÙÆhÐô<ô®¾çK°ÚX>Ìªª$+*©ÊF©¡ÞÜméÎ\x00075ÒMà\x001d3^\x0002
\x001aØi³Çó¼3Ê¬½1Þü ÕÌ\x0002ÜëÑTäDUöôÎ*¼®ör9M\x001bEÓ¯¼=5Ì>ÔÌv&\x000fAQxO´¸µâs\x001fÉ.ÇHÌ5Ç\x001f êXäg¶+¬ÿ\x00003¨c\x001fÛ\x0016Üÿ\x0000Ó&ÿ\x0000\x001a|?\x0007õky<È5Ø¢|ctjêqõ\x0006º*ÍN1­øS£8É·­ÎTéV^º\x0018Ìvë*Û¾v«\x00127duÂ[o^Ç¡ª:åµ¼QÛM\x000cK\x0013È]HU*²(Æ$
~è$ï·5Û¯ÁÍM$\x0012.·\x0002È\x000eàá\x00180>¹ÏZ%ø;ªO!mr\x0019$=YÑÄÇ8K±åôW§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf/g.ÇÑ^ÿ\x0000
cPÿ\x0000 ½·ýúoñ£þ\x0014Æ¡ÿ\x0000A{oûôßãE{9v<ÆôïøS\x001aý\x0005í¿ïÓ\x001fð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a,ÃÙË±æ4W§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf\x001eÎ]1­
Ú	òË\x0010ÄSå+¼*\x0012w>ÜØàsÀÝ]·ü)Cþöß÷é¿Æ\x001fÁÝR\x0019\x0016Hµ¸#z2#\x0002?\x0010h³\x0005NIìpÚýµ½½Ü\x000fo\x0011ÍRÆ"1¸ldãp\x0019ÇNã+ëë?øò·ÿ\x0000®kü«ç§ø9©I!Mj\x0007rrÌÑ±'ñÍ}
l¥-!SÔ"Ò²ª­c¢Znä´QEbt\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0015o¬ÅÜkÚë÷Iéô¬Ïì¿X?ï³þ\x0015»E\g(«"\nad]úÁÿ\x0000}ð¯2ñ¿ÂMgSÕ¦Õt§µ¦\x0000ÉnÒ\x0015%ÆA#\x001d\x0000à×¥ø·ÅÚw´¡{½ÚFÙ\x000c\x0011ýù[Ð{zò\x001dOâ¾­â\x001cÅjßÙ°÷\x0016ýã\x000fwÿ\x0000\x000cSs¬x4íKJtûûIEäGapíì\x0000\x0019ÎF:R
\x000b^Ön!²Óô\x001dE\x0011æS,³@ÑªíÓ\x0015±{³íJ718/Ï>ÜúÖöñ2ëA¸{MU$¾²NRU?¾E÷ÏÞÇ¿5ÃB¤jJö×sØÆÐ©B¯¦ßèÙ\x0017°ßgÿ\x0000£û"óÖ\x000fûìÿ\x0000ñ5wEÖôÿ\x0000\x0010iê\x001aeÊÏo'F\x001c\x0015=Á\x001dA\x001e´+»ÚÈñù|Ì/ìÏX?ï³ÿ\x0000ÄÑýyë\x0007ýöøÝ¤fTRÌB¨\x0019$\x0005\x001eÖAÉæaÿ\x0000d^zÁÿ\x0000}þ&¸\x0018©öÚÝ-\x001clN:rÆ½F\x001bn\x0014´\x0013G(\x0007\x0004£\x0006Áü+Ê|c'â\x0007\x001fÝ\Nn[-
(­¯
Ü,ZêBáJÜFÈ7\x000cò\x0006áüHÌ\+²ñ*4ûi\x0015\x0015vÊAÀÇQÿ\x0000Ö®6:\x0004ÙËwuvbÙEÎâGSôö®Ïû"ïÖ\x000fûìÿ\x0000`|;Ù\x0015®¥q#*(dRÌp\x0007\x0007ük¹h§MðÊ&q¹\x0018\x0011úU*JÈ9nbÿ\x0000d]úÁÿ\x0000}ð£û"ïÖ\x000fûìÿ\x0000nÑOÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÂþÈ»õþû?áGöEß¬\x001f÷Ùÿ\x0000
Ý¢k äó0¿².ý`ÿ\x0000¾ÏøQýwë\x0007ýöÂ·h£ÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÄG¸\x0012¼j½Ê\x0012Oê+h\x0000\x0000\x0003 éKEL¤å¸Ò°QE\x0015#
(¢
(¢
(¢
(¢
(¢
(¢
Áñ'm<;
\x0014Íu Ìp©Ç\x001e¤ö\x0015½^\x001fâÛ.¼U¨<NÉLkì\x0017W\x0008ó3ÌÍqÂÑ¼7z\x001bñ7V,JZYªö\x00041þ´ßøYÇüûYÿ\x0000ß-þ5ÅÑ[rG±òÿ\x0000Úx¿çf/Ä\x000f\x0014^ø]®j¶ùhä('y=z~U¤\x0018ü¹\x0006Ñæ\x000e§ÔU=O'TºÏ_5¿2Ò³Ü+ÿ\x0000\x000fFúVlû\x001a
ºQrwvG«G\x0002½@\x000ep¬Iï\ÿ\x0000­Ñ¤\x0005¸Y#;öïZ¶þ,Q¢_Â\x0008P0Çiýk\x001fÆw\x0011Í¥DÖÒ¤¬ÎS÷l\x001b¨öúWRuumÏ³Ì]:¸'ÊÓjÛ\x0014|\x0005ãK\x0006kF.útä-Ü>Ý\x000fï\x000fÔq_OÚÜÁ{k\x0015Õ´«,\x0012 xäSÊz\x0011^\x000bñ\x000fÃZZxcHÕl.í¾ßok
½Ü\x0011¸- 
\x0006ì\x000eàõöúVÁO\x0017ºÎþ\x0017»rÑ°ilØºG,Nãñ¯eÙêIÅÙÛ^uñ§Sk\x001f\x0001=²9W½!ãº±ÿ\x0000Ðqø×¢×|}¹ùt;\÷R?\x0005\x0003ùKq½ÿ\x0000Ùéí PÇo\x000bmÏ\x0019Ës[>#â]~é\x0013\x0010\x0008\x0000Éè\x0005bþÏ\x001fò\x0011×¿ë?Í«Þ¨`¶</ì×\x001fóí7ýûoð¤V¸Ó¯¬oL\x0013*Ãu\x0019bc=	Áý
{­bø¨©ðíÚ\x0001¶£<\x0010i\x0005{Å´º#lVvYT£&¸o³\Ï´ß÷í¿Â½?M¹\x0012[Ú\\x0016\x0000\x0010¥=;\x001aézacçÏ\x001dÏ6ðöÒÁÑâ}Bùæ!	4\x0000qé¸þÐ~ÏDÿ\x0000Â=¬®NÑv¤\x000cð>AX¿\x001e®\x000bøN¶Ï\x0011Y3ãÝÿ\x0000ñ5³û=È\x0003Zÿ\x0000¯´ÿ\x0000Ð\x0005>[ÉE\x0014T\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015â~2²ÇÅ7¢E!f9\x000f¨nE{eeëz\x0005¿j!¼C¹yTáû\x001féW	r³ÎÌðO\x0017G;­Qá4W]â\x001f\x0004®º_\x0019VV*\x0003G1øÕ\x001d\x001fÃ\x0007VÔVÓíb-Ê[vÌôüknx1ýþOÅÆ_èÖWFK7FøË:AÜW#k\x0001º¼ÝO2È\x0010\x001czµéß\x0012t(|'¤Á\x0007öîõÈXÄ{q\x0018ûÄò}ã^kc\x0014Ò\o)D\x001bAÕMg7uîCP¯F6Ä¾Ú^ú\x001d¬Åâûé^Û\x0007rÄXÜó]-|?c¹íÆ |À9cËÏðV³¥éð^'êúGu6í\x0018'bsÐôï\x0006ê:íö¥5µÖ¢ÆÞ4wEÚ§\x0003pÚ:zf¹)Â¶ª£M\x001eî.XyZXTâýtýY´|;£\x0010A[Ü\x0011þqKáß\x000eh\x0019ÕÓS²îKÔ¬f|°LðH\x0000\x000eqÅz.¦[Ë¥Å%ÊùÒÙsÜúVöEüûûèÿ\x0000h£m\x0019*óø¥s»ñ-ÕÕ¤°#ÍnÒ.Ñ,1|éî3Â¸_Âöô±ÉªjÚÕÛÆ\x0008C)\x0007h=qòñ^¿ýaÿ\x0000>ãþú?ãPÜévIi3¬\x00002£\x0010w\x001e\x000e>µZìªÿ\x00001ãúOt\x0019åkKÝYL \x0006ÁÛÓè+Sû\x001eßþ:Çýýjèü$N¥4wgÍEp\x0007\x001cJëÿ\x0000²,?çÜßGühÔ=^çMá»i³jÚè\x0007øDÍRéú\x0005ò2ÜêS\x0019\x0000Ïwc\x001eW«dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãKPöuácºXì´þI\x0005pbÉÁ©´½Q´Â\x0007¹ta©*>®KjÇÄ^JÎVßÏ\x000bå\x0001Û3]GöEüûûèÿ\x0000\x001a³«üÇø«BÓ<_©­þ¢×©2Â!\x0002\x0005Ú6Opyæ®ø:ÖÏÁ\x0016VÚgÚ¤K\x0004n\x0013q\x0004\x000cqW£ÿ\x0000dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãOPöU{çü%·\x001fóËÿ\x0000 ñ­}'P¿ÔvLc[\x0012C\x00120xöÍbMhÑøÊ\x0013\x001f³yÊ<¬q3×½v\x0010Á\x0015¼b8P*\x000ep(±P§Rþó$¢(:\x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000eKÇ\x000b7ôÌõ«\x0003ÂO³Äßí\x0007_ütÿ\x0000u>5ÌÐ|À3åJ­ô\x001d?­qz\x0014ÞF½c!8\x001ehR~¼Z¥±/rÆk]:çXÓÁðÌ<G@è9ÜzWÛYÅk»ËÜwuÉ®¿â\x0015Ë]xãQ,x¬Kô
?©5ÌS[\x0012÷\x001aÅù\x0017'ÜàWWðú9´o¤Ôþå@
:|ÕËWiðý~{öÿ\x0000p:\x0018!ú§Ä
~ÆòãO±\x0018-à
Â\x000b\x0011äæ±ßÇ\x001e's­\÷véYZù­ãúÎÿ\x0000ÌÕBB\x0000÷¢Ásª³øâ{9\x0003\x001dGí
:¤ñ«\x0003ù`×ªxgÅpø¯AºF!»
Í\x00089\x0000pG±¯\x0001\x00040È jéü\x0007«'Å\x0010}°]©·Óº\x0003ÎCLôo\x0003Fé©\F_Ü£Þ»ªæü7µÌ?éþuÒT( g)\x000e&ñ&O\x001f¿'òÏøWW\®|A»¶÷aúÿ\x0000uTØQE\x0014rÚ!ñ\x0006ÿ\x0000öÑé]MrÚêÕÕ¿¼ªOçÿ\x0000Ö®§¨¦ ¢)\x000c(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000¥«Z}»Iº¶\x001fyã!~½Gë^L®Ñº¸áÐ=¯YÕ.&·° Rd?(`3·=ÿ\x0000
ó\x0016ðwg{»f9$Äy5JÝN,V"tP7ÎÆ\x000fÄ\x000b\x0007^\x001a².m5$YÇ@Û@eúñú×%^þ\x000e\x0012Gå½ÌìÝ1\x001cU6ðNCÞ\x0015aÕHÆ?\x000cÓºîc\x000ceGñÓkÑ§þG\x0005]ÏW\x0016wÒ\x001fùè£ò\x0015:x"ÆP|¹Ë×lyþµ­¥è±hÖÓÛÄN%;)·c¥\x0017F´q\x0012ù\\x001aù£Èn¯O+ êìr~µQÝåõ+\x000bC¤Y\_Æÿ\x00004\x0010»üÖã\x0007×5åc¥\x0017]
¡ZUSr¿\x0012X$) çpEiÄJÍ\x001b\x0003\x001c\x0010\x001a©¥i×:éÖ3#¤o1\x0003û¨2jÊ\x001f\x000fûB¹ô\x0007?ãòoúæ?tµÍxoþ?&ÿ\x0000®cù×KY³D\x0014QLýKÿ\x0000ºh\x0019Ìè*\x001bVfÏÝV#óÅu5Ìøisw+wXñùþµtÔ1 ¢(\x0019Ìøqy\x001b\x000e­\x001e?#ÿ\x0000×®>bCþÈ®Ä©ûËwõV\x001fÊ·-	6P\x0013ÔÆ¿Ê¨¢C
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
òÿ\x0000\x0014ÈÉyþòÿ\x0000è"½B¼¿Å\x001fò2^¼¿ú\x0008¦ÎÀ_ñé{ÿ\x0000]\x0017ùTú¨ó5õBx%\x0014T\x001e\x0002ÿ\x0000Kßúè¿Ê¬\þûÄê§´ª? 
\x001dC \x0011n>Ïðÿ\x0000Xlà´>Xÿ\x00000_ë_6W¿|_Êð+F\x000e\x000c×1§×¥x	8\x0019¦¶&[¯ðWIó.µ=ZDÊ¢hò;¿M¿s~.Ñ\x000eâE\@Î%ýÆ9\x0003ð9\x001fzÿ\x0000Ã½ èÞ	ÓáuÛ4ËöÞ~\x0007áXß\x0015ô_µèöú´KlÜ,\x001dcb?Çæh¾£¶ß\x001dF¡"\x0013ó49\x001eø#ük§¯>±¼û/ôU'\x000bp%ÿ\x0000ß\x0000ÔW ÒcAP^1[\x001b\x001dDlJªêOåé
ÿ\x0000LÈ¤3#ÃIóÜ? UþuÐÖ\x001f\x0010\?«ù\x000fþ½nPÁ\x0005\x0014Q@\x0018^%\ÃnÞGæ?úÕ§¦¶ý2Ù½c\x0015CÄk\x0018Ûû²0jæÛ´eÇäh\x0017Rí\x0014Q@Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002¼¯â\x001cÿ\x0000Ùþ#O%\x0014ùð,\ü¯T¯&ø£ÿ\x0000#\x001d¯ýz\x000fý
©¡=ÃáþÙ<2;@i\x001c¾=\x0007è)è\x0004Þ)>Ò\x0013ù\x000fþµGðïþDÛ_÷äÿ\x0000ÐK`\x0003øV\x0007Ò0þ_Ö9?³íÑ4»|ÿ\x0000¬¹gÿ\x0000¾Tÿ\x0000ñUå~\x0019ÒN¹âm?M\x0000aæ{ å¿@kÐ~7Ïí\x001eß?v9d#êTCLø-£ù·÷úÌòÂ¢Þ"Gñ7,GáøÓ[\x0012õìÊ¡T*\x0000\x0018\x0000v¨/í¢½Óî-¦MñË\x001b#/¨"¬R7Ý?JÏ\x0015ñuõö{áéôøÃ\¥×Ë¿ è9üëÚÇNF+Ç|_	k+Y\x001f»|Áý+Ô4
Ium
ÎõX\x0013$c³\x000e\x0018~y¥ÍïX¿gh)÷4ª°@Òn3ÝqúÕêÍ×ä\x0013/=Jÿ\x00001L\x001f\x000e®,$oïH@+b³4\x0004Û¥©þó1ýqý+N
(¢2õõÝ¥ý×Sý?­?C é1\x0001Ø°?¥Öv7¶\x000fäEEáïù\x0006ÛF§Ð]MZ(¢Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002çüg«É£øvym¦HîäÂC¼\x0007¨\x0019¯#ûn¿~\x0019Î¥p3(îÃô§n¦~Ö\x001cü×·SÞDfGU\x001e¬q^Iñ6h§ñ
³C*H\x0005¨\x0004£\x0003¹½+m?Tåìïýèÿ\x0000J`Òu\x0011ÓN»ÿ\x0000¿
þ\x0014Ò)³Ö>\x001eÜÛ§­£iâY\x0003É.3÷jµ¢.íbwÏÝ
úµxéÒu\x001e¿Ù×yõò\x001bü+¢ñ4ÓÛ[iâ\x0019d91±SÀ\x001eX.b|bW\x001a\x0001-§ú$p*Úº¾§Ï=w\x0012;t¯Uøq¤Ï£ø\x001eÂ\x000b«"æ@ÓK\x0019ê\x000b\x001cûã\x001cWÁ¨­N\x0006¼¹{"T\x0012	\±UÈ8çµ{xACÖôÕ#¨k¤\x001fÖ¡6Û]g\x0005\x0015\x0017}ÍJFû§éXïâÿ\x0000
 ËxJ\x001föù\x001føÕY<yáE\x0004\x001f\x0010Xtí(?Ê¯]î?Ä^\x001eÄZ2Ám?s\x0015Äm\x001c¤d\x0002r¼û\x0012@¬?\x0000øÚãA¿GÔôÝ@³>Ù!Ý¤hä\x001c\x0012\x0000\x001d\x000føWm¦øDÒ\KPÝ'^/7?8ëÇÒ´OÄO\x0007©Ïöí¦}FOô¡Óo[\x0015\x0019´îtêÛÑX\x0002230Eex?Ùþº/õ¬ñ3ÁÃ®»\x0007àöZ«yã=\x0003^\x0011Ùéz\Ï»yEF\x001c\x0001×)òK±7GO£.Í&\x000fpOæI«õÄÚ|Ið}¤VÓkH²Ä»\y2\x001c\x0011×øjoøZ^\x000bÿ\x0000 Úßø=û0º;
+ÿ\x0000¥à¿ú
§ýøÿ\x0000£þ\x0016ÿ\x0000è6÷â_þ&e>Ì9Òê_K¹QýÂjÏú\x0014£ÒOè+\x0012ãâg®-f5¸÷:\x0015\x0000Ã ä÷i¶.Ðü<^ßVÔ\x0012ÖI0è¬r:g}(äÖ\x000b£¶¢¹Qñ'ÁíÓ]·üUÇô¥\x001f\x0011ü\x001eæ;mù7øRä`º:+_>\x0012nýâø©WÇ>\x0015~ Ó¿\x001b\x001fÎIv\x000b£ ¢²\x0013Å~\x001d|þßKÈÿ\x0000Æ¦_\x0010h¯÷u=¾(­&\x0019£EVMFÆAï-Ü³*ëS¤ Ê:°õS@:( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000c_\x0013øÏÂAÔob¸=á\x0002ÀO¯@\x0007\x001dI¯.¾øïpK
?C\x0007ðµÄÅ¿@\x0007ó¯jeWR¬\x0003)\x0018 
`Þø#ÂúMÆbXõd!?àÖÔåM|q¹2RèÏ\x0012¹ñÕÏîD©¶hØÖ0U
©<çßÒ¨Ýx¿QÑEÔ\x0006D\x0010qÐ}z×­Üü\x001cðäíî­óÿ\x0000<®	ÇýõÌà^Ùò5=E?ß(ßû(®Ô¡{ôìy¿ÙÉb~³}¤y\x0014¾5ñDÙßâ
OîÜºÿ\x0000#Tå×õõÚ½üïÜ¹þf½foÑ\x0010|\x0010:ÁíAþL*¿\x00025\x0001þ«\¶÷áeþ¦º\x0015|?ôÎIXo.¦`$º²z´×Sñ\x0006îÖæóNÒæ;Ø)hØ\x0011û}+ øûßï4ÿ\x0000e5ZO^)CòÏ¦Éî³7õQGµ¢ä¤¥°rÊÖ±ÆÛ\-ò\x001f2ùw\x0011©ä`\x000c\x001cUMFá.ïd\x0014ª¶\x0000Èçí_àß¤6þíÀþµ\x0003|"ñôÓ¢o¥ÌÔÔSTaQÍKrT%Ê¢õµíóèpÔWfÿ\x0000
|jó\x0006ÏÒæ#ÿ\x0000³Uvøiã\x0014ë¡Oø:\x001fäÕÕí©ÿ\x00002ûÃö&ñÍÕ½Í¾ ¸]_ËpÛN\x0017ÇWN~\x001dø¸uÐnÿ\x0000\x0000\x000fõ¦\x001f\x0000x°uÐ/\x0008ê)Î#ËÌÔ½n»/\x0017\x0016ÝÔ÷sÃ
b\x0015¥p¼^ïYÿ\x0000ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£EIS\y$Ó½\x0019ßÌ¸ÿ\x0000¼Äþµ\x001dt_ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£VªÓ_i}âå}vè¿á\x0002ñ_ý\x000b÷ÿ\x0000÷èÑÿ\x0000\x0008\x0017ÿ\x0000è_¿ÿ\x0000¿FkOùÞ\x001c¯±Ï\x0003Jì¾!^Áq¦O\x000cðÊM·Ïå8m§9ÁÁã­gÂ\x0005â¿ú\x0017ïÿ\x0000ïÑ£þ\x0010/\x0015ÿ\x0000Ð¿ÿ\x0000~D¥MÉKh;;ZÇ;Et_ðx¯þûÿ\x0000ûôiÃÀ\x001e,=4\x000bïÆ<UûZÌ¾ñr¾Ç7Eu)ðãÆ\x000fÓB¹\x001fï\x0015\x001fÌÔËð»ÆÓDÆxþÍG¶§üËï\x000eWØä(®Õ~\x0013xÕºé\x0001~·QñU2|\x001fñu²·O÷®Sú\x001aN½5örË±ÂR«²\x001c«\x0011ô5èIð_Å×ì	þôçú
µ\x001fÀï\x00120\x0005ï´´öód?û%KÄRî>I\x001e{\x0016«¨Ûÿ\x0000©¿º\x001fÜò5q<Uâ(Ø2kÚéw'ø×\x001fÀ­`ÿ\x0000¬ÕìWýÕvþ®Cð\x001aRGâ\x0004\x0003¾ËR
Ãÿ\x0000H|8;~.¶ÿ\x0000W¯]úèÂOý\x0008\x001aÓâï¢ûúS×Khÿ\x0000 \x0015ÜÃð#M_õúÕÛÿ\x0000¹\x0012¯óÍhÁðKÂñ\x001cÉq©MìÓ(\x001f¢ÊU°Ý¿\x0002gÜã,þ8ëñ`]XX\/rªÈßÌÒ»	|Z³ñ6­\x0006.qku6B\x0014q"p	98\x0004tô­k/þ\x000f²Á]\x001d%aüSÈògð'\x001f¥tv:V¥¦Ë\x000b\x000bkU#\x0004A\x0012¦!\ÕgE¯r:\x0015.¬¹E\x0014W1aE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ÿÙ
endstream
endobj
164 0 obj
<</Type/Page/Parent 2 0 R/Resources<</ExtGState<</GS5 5 0 R/GS13 13 0 R>>/Font<</F3 19 0 R/F1 11 0 R/F4 171 0 R/F2 14 0 R>>/XObject<</Image166 166 0 R/Image167 167 0 R/Image168 168 0 R/Image169 169 0 R>>/ProcSet[/PDF/Text/ImageB/ImageC/ImageI] >>/MediaBox[ 0 0 540 780] /Contents 165 0 R/Group<</Type/Group/S/Transparency/CS/DeviceRGB>>/Tabs/S/StructParents 16>>
endobj
165 0 obj
<</Filter/FlateDecode/Length 1101>>
stream
x½WÛnÛF\x0010}\x0017 G*°V{ßea¨µe9H\x0014I­¢\x000fF\x001e\x0018RYDdÂôÝ¯èÌRNd]+9\x0008`ZärvÎë\x000eað\x0006ÎÏ\x0007¯G¯®\x000fpy5OÝ\x000e\x0007Î8çÂ+!Àh\x000eÎs(ÓnçÏ\x0017w;7\x0006æU·#`þU[Áy"={Ñí¼ív`üz\x0004°$VÂVî¹vÀ·@]N\x0010îZÔ0\x0011 ¢\x0000É=ó`5n·0Y\x0004=Úá[&¸Äÿ*PÎ\x0003S¡\x0002Õ-\x0002¿¿ìvn£QÑÓQ>ýÐTY¸ë½É¯ÝÎx²»ÜàÎ¹ö­\x000b¤ÖBo1B\x0018ÎÐ@ÇLÐÌj´É )"ýÁ«E2OµpUÀ[Rí$|¦_eÐ1Ìrðè_"\x000eø\x001b:¨DzTº<\x0010Dlz2\x001d¡o¶WÇ:^ðO\x001c/gÈE	Ë¸Øçùþþ#O¡g£»l6ëõUM\x000f=\x0013Õ\x000fgÐë\x000b\x00195ôÚD\x001aEZÕY÷ú:\x0002|úù@dô÷2N:ÉüiÆZºu2­S¤ü\x000fôò"¬d\x0011T\x0015-dUää)®î7Í|7Ó`ò4Ó¦hr2íÏdÊû,O²Ìdy³ iËÚÐ±9Þ-Í=ÌÊ\x00036Úö³«v1>gÚÅøH{bÊîmCî\x001bb¿u+ºÇ¶Ø\x001bôà&65\x001ec[§ZÁP\XCÅpöI)»e)oÀú
X®7ûmV\1ß¶\x0010£¨îv\x000cûãH¬\x0002û]Àñ&°ÐR\x001cè]\x0008LÍcæ,HE½ËqNf\x00157Þ+\x001eONÛ÷4\x0014\x001aO\x0002»ÛÎ%>*\x00045W¾vZ\x0008æ=F3v,Ö'%ÿoT§ESAÏGÉ}ÑSxNè\x0008\x001f\x0005îñ©¡DÇ\x0006f#øéP1Í#äMzMXÐî¤>GX7|Bõ\x0013[\x0008á9¤õ3	q=Tø#/ðòËr3\x001ejZ¾¦\x001d
O÷x;\x001aöø\x0015Ýø°r»VÖÃö«v_L²qP;4çß4?JJ*\x0004¼Æk\x001a¶\x0011Á¿ëVâÃ¾\ÑÆ[¼Àm¼äæW¯Oóü¶ôVÖ²gy>ºÃ\x0013¨o¢êaåÍØÖ)ßÓC|ô8±/%6Vó£\x0013y;\x001f\x0013ùdBÑ\x0008}X,\x0016)õ\x001a{î\x001e\x0016Iðig°HëºLÃl2Ø3>&
M\x0004UzFNR\x0006ÑqÀ
ÐäâYJÊÊtSC.U\x001fÏÑ\x0013Ñ¾øpÃÌ\x000fo4ûâs2¡-ñ¡\x001eU4lêàè´l£oÕ×Q54ùjù*<(¤Ë=3¸(ël\x0003\x0014è¢ÆQê¯ô\x000en\x0007E]\x0017wÉéàM2ÇÁ\x0006ßÁMó¾¦¥ë¢¨Óòø&<ZqVYõ\x001dÎ7\x000c'\x0013tªr\x001fNZÅô¡ÈSÞÄK×­¯ï\x000e\x0004\x000bém$Ä¡ì;eh5ô\x0011³>·:vplÅ)äXÂ·Ñ8Ç°`È`\x0015k§ó³ÈI\x001cýì3Èae·m\x0017ó\x0005;o?4Poúõ?aÑ@¥
endstream
endobj
166 0 obj
<</Type/XObject/Subtype/Image/Width 459/Height 334/ColorSpace/DeviceRGB/BitsPerComponent 8/Filter/DCTDecode/Interpolate true/Length 17816>>
stream
ÿØÿà\x0000\x0010JFIF\x0000\x0001\x0001\x0001\x0000Ü\x0000Ü\x0000\x0000ÿÛ\x0000C\x0000\x0008\x0006\x0006\x0007\x0006\x0005\x0008\x0007\x0007\x0007		\x0008
\x000c\x0014
\x000c\x000b\x000b\x000c\x0019\x0012\x0013\x000f\x0014\x001d\x001a\x001f\x001e\x001d\x001a\x001c\x001c $.' ",#\x001c\x001c(7),01444\x001f'9=82<.342ÿÛ\x0000C\x0001			\x000c\x000b\x000c\x0018

\x00182!\x001c!22222222222222222222222222222222222222222222222222ÿÀ\x0000\x0011\x0008\x0001N\x0001Ë\x0003\x0001"\x0000\x0002\x0011\x0001\x0003\x0011\x0001ÿÄ\x0000\x001f\x0000\x0000\x0001\x0005\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000bÿÄ\x0000µ\x0010\x0000\x0002\x0001\x0003\x0003\x0002\x0004\x0003\x0005\x0005\x0004\x0004\x0000\x0000\x0001}\x0001\x0002\x0003\x0000\x0004\x0011\x0005\x0012!1A\x0006\x0013Qa\x0007"q\x00142¡\x0008#B±Á\x0015RÑð$3br	
\x0016\x0017\x0018\x0019\x001a%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚáâãäåæçèéêñòóôõö÷øùúÿÄ\x0000\x001f\x0001\x0000\x0003\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000bÿÄ\x0000µ\x0011\x0000\x0002\x0001\x0002\x0004\x0004\x0003\x0004\x0007\x0005\x0004\x0004\x0000\x0001\x0002w\x0000\x0001\x0002\x0003\x0011\x0004\x0005!1\x0006\x0012AQ\x0007aq\x0013"2\x0008\x0014B¡±Á	#3Rð\x0015brÑ
\x0016$4á%ñ\x0017\x0018\x0019\x001a&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚâãäåæçèéêòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0001\x0000\x0002\x0011\x0003\x0011\x0000?\x0000ö(¢( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002k:¢31\x0001TdÚ°î<Q\x0004r\x0015\x0016Gñ\x0013´\x001a¸Sþ\x0014gR´)ünÆõ\x0015Íÿ\x0000ÂWÿ\x0000Nøÿ\x0000ÿ\x0000ZøJ¿éÓÿ\x0000\x001fÿ\x0000ëV¿V«ØÃë´;%\x0015Íÿ\x0000ÂVçÓÿ\x0000\x001fÿ\x0000ëRÂVçÓÿ\x0000\x001fÿ\x0000ëRú­^Áõê\x001dÎæ¿á+?óè?ï¿þµ'ü%Mÿ\x0000>þûÿ\x0000ëSú­^Áõê\x001dÎæá*oùô\x001f÷ßÿ\x0000ZøJµ¢ÿ\x0000ßýj>«W°}zs¦¢¹øJ¤ÿ\x0000Eÿ\x0000¾ÿ\x0000úÔÂU'üú§ýöÂªÕì\x001f^¡Üé¨®cþ\x0012?çÕ?ï³Kÿ\x0000	T¿óê÷Ù£êµ{\x0007×¨÷:j+ÿ\x0000¦_ùõOûèÒÂS7üúÇÿ\x0000}\x001a>«W°¾½G¹ÔQ\Êx©÷~òÕv÷ÚÜÖõì7Ð	alàõ\x0007ÐÔNá¬­,E:Ñe(¢²7
(¢
(¢
(¢
(¢
)\x000b\x0005\x0019'\x0003ÔÕfÔ¬Tá¯-Áô2¯øÓ³bm\x0016¨¨ã\x0019¿ÕK\x001cî05%+4;Ü(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000Áñ<í\x001d¤P©#Ìc»\x001e¹lWIâ¿»kõoé\ÝzØUû´x\x0018æÝf\x0014QEt\x001caE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0002b¶<5;G©ùCîÊ§#ÜsY\x0015¥áÿ\x0000ù
Côoý\x0004ÖUé³|3j¬mÜíh¢ñ¤
(¢
(¢
(ª\x001aÎ¯k¢is_ÝåF>èêç²sMEÉÙ	´ØíSV²Ñ¬Úîþáa}z±ô\x0003©5åÚïÅKë1hðXç¬4ô\x001d\x0007ë\¿â\x000bß\x0011j-uvü\x000c¢\x0007å}\x0007ø÷¬ºöpø\x0018Á^z³Í­£¢._jÚ¦û¯¯®.=¤?\x000e¨í_Ju\x0019®å\x00149\x001cÜDß\x0013ïÚ6\x001d
\x0011[>6ñ&\x0016©4½\x0012sæ\x000fÖ±3ELéB[¢£RQÙ¥¢|[MkVKt3Ûò¿R§ø\x0013^g}k¨[-ÍÄsÂÝ\x001e6È¯\x0019}+O@ñ\x001e£áËß´XÊB<Èz\x0011ýz×[\x0003\x0017¬\x000eÊX§ö¤(¬\x000exÏÄºbÞZ¬>Yb'æ½>¶+Ê\]Þjè(¢C
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢9Ï\x0015ýË_«Jæë¥ñWÜµÿ\x0000y¿¥sUëa\x0003\x001düv\x0014QEt\x001caE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001ZZ\x0007üaÿ\x0000#Yµ¥ Èf\x000fø\x0017þk:¿ÃfÔ?\x001fSµ¢+Å>(¢\x0000(¢\x0000+Æ>'kÇP×\x0006\x000cìö|0\x0007õüº~uìõó~½ksi¯_Cv¬³	Ø¶á÷²s|×¡Á:¾\x001e2MBË©@\x0004\x0001z\x0001Ewß\x000c<?\x001e¡©ËªÜ®è¬È\x0011)\x001c\x0019\x000fÀ~¤W­V¢§\x00076yôàç.TXðßÂùnáK­jW·VÞ?¿öéôþUÙCðóÃ\x0011.\x000eæ{¼®Oó®¢ðjbªÍÞö=hP§\x0015k\x001c×Ã_
\)	k,\x0007Ö)OõÍqúßÂ«ÛUi´w\x0018\x0019ò¤\x001bdü;\x001fÒ½ztñu`÷¸§§.Ì2E$2´RÆÑÈ§\x000c0Aô"¡qÞ½£â7#Ô´Ù5kH¾¶]Òmÿ\x0000¹õ#­xÖ2+Ù¡YVÑæÕ¦éNÆ·<C7µ¸¯\x0013-\x000b\x001dÇ¼óø¢¾T\x0008æ·G"V\x001dÁ\x0019\x0006¾]¯røa©=÷V\x0019\x0018³ÚHa\x0004ÿ\x0000wªÿ\x0000<~\x0015Á¤­Î¼,õå;J(¢¼Ã¸(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ç|Uþ®×ýæþB¹ªé|Uþª×ýæþB¹ªõ°¿ÂGþ;
(¢º\x000e0¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000­\x001d\x0007fßþ\x0005ÿ\x0000 Î­\x001d\x000bþC6ÿ\x0000Vÿ\x0000ÐMgWàfÔ?\x001fTvÔQEx§Ò\x0014Q@\x0005\x0014Q@\x0005PÔ4]3V\_ØÁq]>aô=E_¢NèM'¹ÄÜ|-ðôÒï]@¹å\x0012\üx\x001aê´½*ÏG°ÊÆ\x0011\x0014)Ð\x000eI>¤÷5r¹ÖÕ¤îLiÂ.é\x0005\x0014QY\x0014QE\x00006DYchØe\\x0015#Ø×Ì×Qy\x0017Ãÿ\x0000<äeü+éyåX g8XÐ¹>Àf¾fC5Ä®åâs^®[xàÆÛB¹ë^§ðrS³XøAÇþ<+Ë\x001bï\x001aõ_°o«Îz3Dð\x000cOó\x0015¶3øLÏ
ñ£Ô(¢ñ\x000fL(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢ô\x0000QLY£w(²#2õPÃ"@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001c÷¿ÔÚÿ\x0000¼ßÈW3]7¿ÔÛ¾ßÈW3^¶\x0017øHð1ßÇaE\x0014WAÆ\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015£¡Èfßêßú	¬êÑÐ¿ä3oõ?ú	¨«ð3j\x001fÅª;j(¢¼CéB( \x0002( \x0002( \x0002§©jvzEÞ_L!:±î}\x0000\x001dMs\x0016¿\x0014<9q1G¹·\x0019áåÿ\x0000|ZBæ¯\x0015r%R\x0011vlìè¬Û?\x0010è÷øû.§k!=\x0014J\x0001ü5¤9\x0019\x001d=j\d·E)'°QG>¬øJÐàg½»\\x000cTåØú\x0001Dc); rI]\x001f\x00115¡¤øZh±=çî\x0013è~ñü¿xgjÙñ7®<KªµÜ Ç\x0012°Å_ñõ¬F8\x0015ïahû\x001av{EzÒzlFkÜ>\x0017Xµ¯Öf\5ÔÏ'à>Qü«Åìl¦Ôu\x000b{+u-,ò\x0004P=Í}-ai\x001dog\x0010ÄpF±¯Ð\x000cW&>vs«\x000b\x001fzå(¢¼£¸(¢\x0000(¢\x0000(¢\x0000(¢Ò(júÅ§É{0\x0014éÜ±ì\x0000îkÆ|Gñ#WÖ\x001d¡³v°³<\x0004üì=Ûú\x000fÖªøóÄ²x_c\x001bV1À¹àãßòÅrÕ¼ ¬ÊRìMmwsevV³É\x0015Â¶á"6\x000ekè\x000bk±øÃö×ëþ°/÷d\x001c\x001fñú\x001aùÆ»Ï¾ :vºÚ\Ïþ}Âç´§çÓò§8Ý
\x000eÌöÊ(¢¹Í( \x0002( \x0002( \x000c_\x0011Û<ö\x000b"\x0002LM¸éÞ¹*ô~£Ç¹ðåî]7ÂOPÈ×n\x001f\x0010¡\x001eY\x001en/\x0007*çÈQ]Oü"¶ßóñ/ä?ÂøEm¿çâoÈt}jsê\x0015»\x001cµ\x0015Ôÿ\x0000Â-kÿ\x0000=æý?ÂøE­ç¼ß§øQõª}Ãê\x0015»\x001cµ\x0015ÕÂ-iÿ\x0000=çüÇøQÿ\x0000\x0008½§ü÷ó\x001fáGÖéÔ+v9Z+«ÿ\x0000^Óþ{Oùð®\x000f]ñ&¢ê×\x001ay¶¾H\x001bk\x001dÊ\x0001â­C þ¡W©£Emh:~¯h¶Ú/p2ä¦àv·B:zÖü"öxÿ\x0000[?ýô?Â­S\x000f¨V9J*{ÛI,n\x0019\x0007NtaëPWDZjèã\]QW4«4¾Ô\x0012	7\x0004 ·¯\x0015Ðÿ\x0000Â1cýùÿ\x0000ï¡þ\x0015Jð¦ìÍèájU4NJ¶¼5fòÞý¤ÝÄ\x000e\x000f«\x001eÕª\x001b°VÉ\x0012¿³?øV¬Q$1¬q D^\x000eÍ[\x0015\x0019G'n\x001f\x0003(ÍJ}\x0007ÑE\x0015Àz¡E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ü]¾->§ùUZf_sÀþGó¯3®ÇÚö¯\x001cÇ	\x0010'ü\x0004súæ¹ªú,,9)$xÕåÍQ°ÅXþòØb\x000b¹â\x001e)_äj\x0000\x000bgh'\x0003'\x0002#Ö¶i=ÌkbìÆ§*íR¼eô3±þµHòrI'ÖÒ\x0012\x0000¡(­íQ1É«Vv\x0017º¢\x001b\x001bI®\x001cb4'óô¯KðÂÿ\x0000"Xïuý®Ãæ[E9\x0000ÿ\x0000¶G_ üë
ØAjÍ©QÃ¾\x0017øQí×ûzö2²:µF\x001c=_ñííõ¯N\x0014\x00000\x0000\x0000\x000c\x0000;R×V£©.fz´à¡\x001b ¢+2Â( \x0002( \x0002( \x0002³õëiáíFáN\x001a;i\x0018\x001fp¦´+\x0017Åà\x0007k\x0018ÿ\x0000I?5¸=h t¢º`§#¼R,±WR\x0019Xu\x0004t4Ú½¥èÚµt¶úu¤ÈO%GÊ¾äô\x001f
÷\x001a>ð¶¶¾ ðí­øÿ\x0000XË²Qèãþ?mV\x001f´\x001føG<=o§³\x0013$¬:\x0017=qíÐ~\x0015³,±Ã\x001bI,\x001ckÕ\x0003ñ5Ê÷ÐÝl>ÇÄÚT)¸],«ë\x001f#óéE¯tÛ¶P²Üp\x000b\x000e3õ¤3b@A\x0019\x0007ZZ\x0000(¢\x0000(¢©ÝÎÊÁ\x0010àI\x0015\x0013»4§MÔ*.QQÀÌð«7R2jJ¤î®DË"C\x0013I#\x0005D\x0005à\x0000;×\x0013â/\x0016ºb·9Ý÷I\³}\x0007o©¤ñO$]wþ\x0011è#\x0001|6âVôÆBÓ&¼böéï¯e¹ä»\x0012=aZB\x0017ÜÎR±ßGñRãÍË,¡sÜ)ý+Ð<9â»]v%\x0001HG\x0004tol\x001eÚ¾y­ß	j\x0012Ùkq$lUeãÌ9\x0006®TÕ´\x0014fï©ô]xgÅ;?³øÉ¥\x0003å¹$\x0007ÜeOò¯fÒo¿´t»{¢\x0000g\8\x001d\x0003\x0003ú^{ñÌ5®z\x0007(ï\x0013\x001fb\x0001\x001fÈÔSÒCÃ~\x0010ë\x0005¡¼Ñ¤?pùðý\x000f\x000c?üMz|ãá=a´?\x0013ØÞû°û%\x001e¨Ü\x001fçÂ¾\x0004\x0010\x00089\x0007¥:Ì îÝcM\x001a¯Ê\x0007¡þÅ*ÅXaÁ\x0007µz5s"Òò
ì#þµ@ýk§\x000bZÏG\x0006;
Ì½¤w+x^=×òÉýÈñùë+ðªb+=YGùüë¢¬±Nõ\x0019¾\x00066¢)¬ÊYØ*IÀ\x0015Îu$H^FUQÔ±À\x0015Îê~.É¶ÚÙÍ|{TãÇÊ¸\x001cøÒe½û5®Ö\x0003%wtQÐ\x001f©¯9kË§ÌkLw\x00179­#\x0006õ&SHöë/zL·b×Q·¹Óecn\x0017äüÇO¯Jì")âYa$¹\x000ekçÍ;Q\x001a¸þÌÔÛÌßÄ\x00137ÞFúÒøs_Ô¼+®¬k3y"`\x0010\x0013a\x0013ÇÐÓöbç>¢\x0010@#½-dXTW7	ik5Ì§\x0011Â#\x001f`3R×1ñ\x0002ìÙø.ü¯YBÃÿ\x0000}\x001eLÕÓ4ÔI¹bÙáW\x0013µÕÔ×\x000f÷årçêNj:AK_L	»»ðÄ=Î¥|Ë¨°®G©ÉþB»­WEÑn\x0000óôË'ÏVw~x¬¿Úp±ðt\x0012\x0011óÝ»L~Ú?Aú×-â­XêZä\x001bæ\x0018?w\x0016\x000f§SøñçNxòPvó=Ju#B\Îª\x000f\x0004x~irÚT[G\\x0016\x001fÖ´aðWàmÉ£Z?¾ÿ\x0000j\x0016å´ygi$Y%ÄaØ\x0001ésúWU\röv:©Õ÷ÔlG\x000c\x0011[Ä"$1Ñ\x0011Bø
++ÜaE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001Yúä\x001fiÐ5\x00081þ²ÚE\x001fÐ¤`\x0019JBÜ\x0019òÀ¢¯k6-¦kwÖ,0`Ð{x?*uìÚð\x001e»âk->bD212c©P	#ñÆ+èk;\x001b]>Õ-¬íã\x0014\x0018	\x001aàWø\x0006åm|o¦3+ÈcüYH\x001f©¯¡+\x001a·¹¤6*ê:¾§O}tû \x000b±ïô\x001eõâ×>!ºñF¡q©j,ÃM²\x001bã´\x0007åÏ`}O¹®³âö¤ðhÖZz\x0012\x0005Ì¥ß\x001dÕ\x0007OÌÊ¼â ö
å¬%!¿ÝÇcJ)%q·©CPÔîu)Ì¹Ûü1ò¨ô\x0015&­_éy[YÈ/\x0013rõ\x001f×­nøkDKE½ºH\-\x001b \x0003ã½jjÚ\x001d­åyp¤s %\x0019\x0014/àqYË\x0015\x0008ÏÇd2ê³¥í.v¾\x0003ñ\x0010Ö,¼®\x001c)9ØGUúsìëÂü\x0007®Å Êg)$ýÂ8\x001bq^á\x0004ÑÜA\x001cÑ6èäPÊ}Aª³9bî( ð+>ÛY´¼½kX\x0019gp\x001f-Cin\a)&ÒØÐ¬mfþÃN\x0013ww
¹!<Ö
\x0018gõ­òóèñûLô
\x001d5SÝcWIó#Ò4ë¨® ÌSG*\x0018\x001e?
½Ú¼#áÁÆ¶é¶X¤B3×ÿ\x0000J÷~Ôù9\x0012.§;rØò?\x001cÝ\x0001âù&\x0004rÇ\x0000»\x000cät¯\x0008êºÑi,âAn\x001c§#8ýJõ¯\x0011x\x00195½Oí±^}°\x0002E)»>ãÑ·Ñ­4Xü8ö$gçï6\x0000'Û8\x0014§VTãt]\x001aQ©;Hà-¾\x0015Eåwª9Ò(À\x0003ó<×7©è2øcÄ°Â³ùªcó¢n\x000e9\x0018"½¦¸¿\x0014øjûXñ-Ä-\x001aÛ|ÌyÝ¸\x0001ß®\x0003XPÄTí&tâpÔáNñZ\x000eµi®mn,&Á\x0010"69ùH?«?\x0013,~Ùà§Q¶t~\x0007\x0007ô&¯x_ÂéáØæ-qçÍ)åí\x0000\x000eÀf´5õ]\x0002þ\x001b#9-Ý\x000bHÁ@ÊZéOS¡óE}\x000bàM`ë>\x0012³FÝ4#Èû¯\x0019üF
|÷^ðWh5{­)Û÷w)æ ôuëùå[ÔWFPvg±R0\x000c\x0008# \x0010ih®sbX,©\x0019ù]Ë\x0001éíW(¢m»±F**ÈF` 8\x0003Ojà<kã
>}6M+M¹[äDÏ\x0011ÊFäüÝ	8Æ\x0007½u~&.<1ªDòÛI\x001d°¤×ÏºeÌqÃ$/ò³²°'§\x0000ÿ\x0000TV\x0014´/Ïbúï&1\x0019?:ÙÂz{Á²?29\x0007I7g?QQxrhÞòíU\x001dÈúèûW\x001dzóì¬{X\x001c-)Ñæ»gO¦\i\x001aµºËÊù×£\x0000&¼\x000cº×Q©ò¤aøWEâ\x001b´ôÆY¥8ÇÐV
ýÌki%¾s#0àvÁæ»(Ôâ¤Ï+\x0017F4ª¸Gc±Ð¾,ÜÙZÃmªXý¥cPxßkàzÁ?¯PÑuMwLP²rÐÉ\x0018*GP}ëæ¨aâd\x0018ÚId`ª2I={ÿ\x0000´k\x000fÂÐÚÞEå\³´&àqÇOlUTF\x0010m5gëZD\x001aæ>rXG(ûËÕHä\x0011ô«äõ¯<ñ\x001fÅ\x0018,n\x001a×H.	
<ì\x0007Ø\x000e¿_çE\x001as½ÍÂ¤á\x0018ûç3}ð·^¶f6ÆÞí\x0007Mµú7øÖ]<Ey|-M\x00014³
¨£×=ÿ\x0000
Ü·øµ«Å(7\x0016VGU2\x001eÇ'ùW¤øwÄºlMÍ\x0010Èq,O÷£>ÿ\x0000ã^JøKÞG\x001c)Q¨ýÖTÖn#ð×ãµñ\x001aÛÂ{\x0013ùd××IãMWûCZh\x0010þæ×÷cÝ»éøV^iöínÎß\x0019\x000f(Èö\x001cÐWN\x0016\x001eÊ·z×´©Ê¶=CKH´o\x000eZ¬ä  _?Þ<ùäµÖw-\x000c e{\x0001¼þ<âñ/Xk+?!\x000b\x0002W\x000b´ã\x000cÙçð\x0002¼c©É¯\x001aÜíÉ|${&ñ6Þòåa\x000f #aü;\x001f¥wÖ×Q]Û¬Ð¾äoÓÚ¾]ïõ/\x0002øXÇí\x0012\x001cÓ}Lÿ\x0000xýÆúç\x0003ñ©-°ã;­E\x0014Ve\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001e#ñ[Kk?\x0014%è\Ey\x00109ÿ\x0000mx#òÛù×\x000b^ññ'Fm[ÂË\x0012nÌùê=T}áùsøW×E7xÍY[Îö×0ÜFq$N®¤v äWÓZuìzk{\x0011\x0005'd\x0018÷\x0015ó
zÿ\x0000ÂmygÓ¦Ñ&÷ÖäÉ\x0008=Ðqô'õ¥Q]\tÞ¶*|dQ\x001d¿ë¨ÿ\x0000Ð+ºÔa¹WÎÖ\x001fÐé>+jÉ{â8¬c9[\x0018ö±ÿ\x0000m°Hü±\\x0015\x0011Ò	;3Ò4@\x0006gùæ*ìDLXü \x001cý+ð¥üË;ÛI'ú0BÃwE9ìkVâúâXåD\x0005\x001dJæ"\x0007\x001fS\/\x0005Vu\x001f*¹îÇ1¡
	Éù\x0018Z5¼I\x0004\x0010¯Í<Æ(÷\x001cnoJú\x0007Mµk\x001d2ÞÕ3G\x0018V#¹¯\x0008µÒµKS¶N\x0018ZÜ·O8(R\x000esÔæ½òÔÜ\x001bHMÚ¢Ü\x001ehåCc{f»*ÓpváÂJ[\x0018^'ÕÅÇ\x000cWqÇ3\x001e2FJCV¼;§%³eZYbÀç\x0003°®\x0013Æòù¾&ç*~þµÛø8çÂöð/ý\x0008Öpq#ZûO\x001b)^VHÝ¯"øÆùÔ´ôCù°ÿ\x0000
õÚñ¿
~Á»lOæÇü+\x001a\x0010Oá9o\x0007\ýÆ:L¤á~Ò¨~òÿ\x0000Zú6¾[¶ÛÝÃ:4r+î\x000ekê\x00012\x001b9,e7'\x0000\x000cg5UV¨oBJåµo\x001børÊf´ðÍp§iKd2\x0010}8ã5Æxßâ?ÚV]/CHÛ-Ðà·¨OozoÁÿ\x0000\x000e
CZY¸\ÃeòÇòý\x0007êEK¦¹}âÚºtº¯Ú¼`ë7v{\x0011ü´CÓè\x000f_ÀÕÆñ?´\x0005ãêÉq#·\x000fæIô
>ïé^ù«â&ýã­J0»RgóÓÜ?'õÍgFÙÖ¬å©Òk?\x0017.dfF³Xcí=ÇÌçßoAú×ê:¾£«ÎfÔ/&¸bsó·\x0003è:
§Eu¨¥±ÊäØW¢|"°3k×Ä|¶ð\x0007ý¦?à
rÞ\x001dð¦©âk¶píN$¸OÇ¹ö\x0015î>\x0017ðÅ§´æµ¶wämòÊýY±µDä­aÂ:ÜÜ¢ÑÀØ(£4P\x00022«)V\x0000©\x0018 ÷®cYð\x0006®OçInðÏ³`ks·èvô&ºRî\x0014w­4c\x0018P(M­×<Mð\x0015¯'}Bö[®Å\x0018Hvìä\x001cO<:Ì¾7\x0010\x001fôX<àIêØÀí^ÁªØ&¥§ÉnØÉ\x0019CèÝq?.gÔ\x0000¼â>[pÆïaë[*TjÇ¦èÅã1xy{:;3\x001eûÁú­¡ZßØXÂ·)xÖY~f,\x0006OLq+Ín|\x0019â[WeD½ÈêV"ß¨Í}Bª\x0015@\x0000\x00008\x0000TW\x0010	W#ï\x000eõ%È¬¶65GÍ7©â¿\x000b<9s\x000e±w¨j\x0016S@Öè\x0012\x00114eNæÎHÈì\x0007ë^µAÈ84R®î$¬[â\x0016¥.á\x000b¦É3,!P\x000f_Ð\x001að÷¿\x001ei3k\x001e\x0014¹ÝKÍ\x0019\x0013"\x000e­·¨\x001eøÍx'µ{\x0019u½¶ç¿:
Ôð¾·u ëB{fÿ\x0000X\x0013/cÁü\x000e
e\x0013V4¸ZkÕ`>T;®ÙÅKFsAµª:RK1f$±9$÷®ÁQ¬Wwº¦ái\x0001*?Ú?ý`k®÷À­c6wbï\x0010ðJc\x0003\x001eµ1¸Ñv4Ã$ê«¶{/<Ulu
®S0o\x0000ª\x000f¥u:4\x001dJVk\x0005I[«ÂÅ3ùq\ýæþ\x000cñ\x0005ÏçÛ!9Vú\x0008?wÉ"Jñ°tae9\x0004z×Éâ%8É4}6\x00120\x001a¹ä¾1ðLZ\x0015ßÙM#Á¼$'%sÐéYzEÃÃkn\x0007*\x000b8\x001fí)\x0018çð¯Tñ\x001eõA·vÈwý0AÏé\\x000f¼-¯\x0014/\x000cúz\x0012MË/
ì¾§ß ®\x0015%:WË§\x0018T´Om¶\ÚÅ8\x0018\x0012 |zdf¥¦C\x0012Á
D\x0008\x0015G°§Ó3
(¢
(¢
(¢
(¢
(¢\x001aê®¬2¬0Aî+ç?\x0016hmáï\x0012\ØóäçÌ½c=?.}\x001d\?ÄÏ
\x001dkAûm´{¯lrë¯\x001fñ/õü=êéÊÌ+£ÃêîªÜhºµ¾¡jØ\x0016Î\x000fF\x001dÁö"¨+dS« ÄÝ\x0013¯ê7¤Ñ­ÄìáF	\x0019=?Ï¥O\x000ei\x0011\x0004«HÛ5§ß5¼Ñ·Þ\x001fÔWI\x000cÑÎâ`Ê{ôð±¥(í©Å]ÔO}\x0007ª*(\x0000z\x0001KU.u\x001b{\}Î?y?ýj×WâQ\x001b+FÇîçk§ÚÓOæ\x001eÎm^Æ%X2\x0018\x001c
uÚ\x0007§µ)m©æh37ñ§×Ô~µÈQEZ0ª­$\x0010©(;Ä¿­Ý-î·yp(ò¶Óê£úW¤ø8cÂÖð/ý\x0008×v¯`ðÄ~W´õ=â
ùóýk0J4c\x0014u`Ýê6kWü[lø¦Ý»h¿ú\x0013WµW|Z³º_\x0011CxÐ¿Ù^\x0005eÇÊX\x0012Húó^M?ïÇWUâ\x001f\x001cßëZu¶\x0016ë{8¢TAæV\x0000r}½«¢º,dô_Â¨D\x000fl\x0018(\x0006FÉ\x0003¯ÎÃúWÎµô§ÃUÙðóH\x001fì9üäcYÕØº{Ux÷Æí4\x0006ÒõE^Nëw?øòÿ\x0000ìÕìUÈüJÒÆ©à[õ\x000b-À¸Ø¯_üwuc\x0007i\x001aI]\x001f8F,\x001chÏ#\x001c*¨É'Ò½/Â\x000b¤Ë½×÷G\x001er¶~fÿ\x0000|öú\x000e~Âx{R:GloÇ\x0002\x0019An?¡ý	®ãÅ?\x0012®oì´2Ð[çi¸Çï$út~µÙ\x001aU*;DæHA^G{¨ø@ð­ºÚÉ,qykòÚÀ¹aø\x000epúÅ»·,ºn\x001cKÙç;ä0?q\x0011iÒÎÆ[\x000eXääåÖ´#µ\x0011F;ì\x0012>-YÍ,EIm¢$Æ^*¾$Fà)í
\x0003ò\x0015Mµ\x0011\x0012K_ê\x001f÷ù¿Æ.¥o\x001f\x0000oEª«Iü\x0011ªýy®¨Â="`äúÈ´'ñ\x001d©ÈÕoýç$~µµ§üP×í0.L\x0017ÿ\x0000M\x0013k~kå\j\x0017-ÖOÀ(¨\x0019¶N?*n9/z(J¬ã³=·Ã\x0014ôKÇòõ\x0005{	Ï\x0001æþú\x001d?\x0011^\x0004ñ\ÂA*K\x0013«¡È#Ø×Éµ¹áß\x0016êÞ\x0019¸W±¸&\x001cæKy9ÿ\x0000\x000eßQÍp×ËÖ:©cZÒgÓTb¹	x×Nñ]©òOx2Û9å}Ç¨÷®¼©ÂPvèFJJè(¢·6ûÆô\x001f0ê=jkÕ+|~ñ\x0007ÔP\x0005Jâ<Cð×MÖ.ZîÒScpü¸UÜ}qØý+¸¢µ§VtÝâìg8FjÒGÛü\x001fÍ½a|°y\x0011Dw\x001fÌñZ¾&ðÅá»TÓ-¤2þõú³d}æ?¯A¦º«¡WPÊÃ\x0004\x0011Á\x0015´qu9Ô¤ïc7+I\x001e\x0019Oim§I vD9VSÈ5ÚxÁE7ÞiJJõ{qÔ»þ\x0015Äc\x0007\x0007¨ê+Ü¥Z\x0015£tyu)Ê¬Í¿\x0010ëç_Ò-bxÞ\x001dBÝ÷­ÄdméÇ¿¥\x0016_l¹ÓmPê3B"\x0005q\x0008Ú\x000fà:V\x001dt\x001aIÍü\x0008×=\\x001d\x001e],]h«Å÷Þ#¸´±òâ#ÙPÛÎ:«gãýB\x0008Õ.-à\x000eãä?§\x001f¥sÚÏÚ.NÓû´áj¥U<\x0015\x0015\x000e^PúÍfù¥-O_Ðµë}vÐË\x0010òåC"'%úÕ­^5¢ê²èÚwQ¨ùdOï/q^¿mq\x0015Ý´w\x0010¸häPÊG¥yxÌ7±ÖÌô°õ½¤uÝ\x0013QE\x0015Æt\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0007QE\x0000x/ÄO	\x000fk&îÖ3ývÅÒ7î¿Ô{}+VÜ+èo\x001bý¼/u
ìBElOPýúu¯î­d²¸1¿ü\x0004úëdáÍm\x000c$ãÍËÔJPÌ¹ÚÄg®
1[4êiØr\x000e\x0008èh¢ÕXÜ«Tø±úÖÖ¤jõ­\x0016uM°Èb;~UÆh÷^EÏÇäÇµv:\x001dÑ±×,î\x0001Â¬ 1ö<\x001fÐ×­
®t[ç\x0004 £RÏcJ\x0004kq>Ô9³$úâ½6Î\x001f³XÛÛÿ\x0000Ï(Õ?!¼ZøÖIK¡éR¡\x001anñê\x0015WQÓ­uK\x0019,ïaY a¿ô5jç6<SQøY«Ç®}À¤¶/ó-Ì´F3Ñ»çè9¬/\x0016øv/\x000cj0X-Ó\Na\x0012LÛp\x0001$à\x0001ô\x0015ôE|ñãß·ø×S9TÊ_¢¿Ò·fRHç«é¯Ë³ÀZ0ÿ\x0000§|þdù×Ô\x001e	]¾	Ñý:!ý)UØt÷7ª®¤ÖË¦]\x001b×T¶10 \sVJñ\x001e.k¯øGìä"\x0018H7L§n¡~¯×éJ\x0017Vj(+TTãvyxyÆ8æ!N:Æ·,ìÙw7Í'séô¨ôÛ_*?5ÎÝ=6ûPÙ¡?7ñ7¥{Ê).HKw÷¤Mu}\x001d¿Ë÷¤þè=+&k©®\x000fÎß/e\x001d*\x001e§$óEi\x0018¤CbW øKáuæ»m\x001dö£3YZIÊ \Èã×\x0000®cÂZtZ·4Ë)À0É8.=TrGãWÓjªª\x0002\x0001À\x0003µpã±2¥hÃvuahF~ô\x0014|#ðÀa[ÂØûæ~?Jóï\x001bü:Âð\x000bû9ÞæÀ¶ÖÞ>xépG½{ïµrß\x0011¥/\x0002ji\x001f<aW=Ø°ÅpáñU}¢MÞçUj\x0014ù\x001e>r¢+ß<kKË:ò+Ë9\x001bät<ú\x000fÀ¾4Åi\x0012mQ\x0001<C¡ÿ\x0000i}é_;UÝ\x0013YºÐ5x5\x001bG"H\x001d{©ö5ÇÃª±ó:põ7ä}SEPÑµk}sI¶Ôm[0Î=T÷\x0007Ü\x001e+B¼\x0006vg¬ÕÐµ
£yìäàt\x0003Ö¦ f\ª\x0016g\x0003ÖRÜ\x0010gb\x000eEELG\x000bñ\x000bÅz¤ÓMòw\oÞ$vq·\x0018çÞ¹ßøN¼w\x001fßÑ\x0014ýl¤\x001fÖ­üR\x001eg|;\x0017÷ÍÐW°ÖI-	³m'ÿ\x0000\x000b'Å±ÿ\x0000­Ðbüm¥\x001fÖ¹ýcÄ÷ºÇÚ$Ñ#·ýö\oúÞ¾ühÉõ5P®àï\x001d	%%f|¾u¹ïZãñ5r\x001f\x00174\x0016m\x0000µ\x001bLþ\x0015ôEo¼ ýEFövÏ÷í¡o¬`ÖÏ\x001dQîbðtÞèù¦\x001dme\x0013ÉÆæ\x0003;ºV½iüS\x0008<u§Å\x00041Ä¿f\x001a\x0004ïnx¬ÊõpueV7Ã§\x001ar´B»\x001f\x0003ë¿fû.á¿u)Ì$ºÞóú×+öI~À/\x0000Ì>gO¡À5\x0000$0`pAÈ#µkVkAÅNr§$Ïu¢²|7>¥¡[ÜÜ&Ù\x0008*O÷°q»ñ­jù¹ÅÆN/¡íF\É4\x0014QEHÂ( \x0002( \x0002( \x0002( \x000f4ñåÅÔÂÅ,Nñ/îèùêGùí\uÍ7ê°ÊÊ$?Áï^ç}am¨Û5½ÔK$mØö÷\x0007±¯6ñ\x0007nt×\x0016û§³ÏP>dúÿ\x0000{8LE9ÃÙKCÎÄQeí\x0016§k
ïï\x0004\x0017J­\x001bðÏ\x0019ÊJ¾ ÿ\x0000JÎ\x000f]­Êý®Ùmç&H;\x0014»OJçï4\x0019âbÖùuê\x0015¸?ýzÎ¦\x0016PÛRé×·3A\x0007½-5­çC@}ÔÔ°ØÝÌØ	>¤`~µÎ¡&ícVã½Æg\x0007 ò:W]lîöÑHü;('ëYvz B\x001eå÷Ñ\x0007OÇÖ¶kÒÂQ\x0013rêqW©\x00194¢{Fwöí"Òë¼+\x001f®9ýjís^\x0006¸ó¼8aðê?tµâÖ%G\x0013Ó¥.h&\x0014QEdX×`Ìz(É¯ïg7W÷\x0017\x0007¬²³þdú;Ä·&ÏÃ\x001a¥À8híd#ë´ãõ¯ûVÔê\x0005}Sá
·´¨X|Ék\x0018?÷È¯t»&Ôµk;\x0015ëq:Eù°\x0015õ*Æ0ª0\x0005*½\x0002âit\x000f\x000e^ê'\x001b¢OÝÝÏ
?3_5Â%¿ÔZIÜÈîÆI\x0019º±Ï?­zÆL¬:n­Ã³Nà{p?¯2ÓHÞkè8¯O\x0003O7Vpâ§ÍS±gP»ò#òÐþñä+\x001bõ§I#K#HÇæcÍ6½\x0008«#Nì(¢®i:lºÆ©
2E\x001c\x0012\x0003ÊÛT`\x0013Éü)¶»\x0012M»!ºuüú^§mlq5¼EÏ|v¯ t/^\x001fÖmQÚú+K|ð\0B\x000f±<\x001fÂ¼Ø|\x001e×Ød]X\x0010z\x0011#ñ4¿ð§<Aÿ\x0000?V?÷Ûñ5çb\x001e\x001a¶òÔí¢«RÙ\x001e©¨x×Ãl\x0006Yõ{fÇDÄ\x0005ÍxÇ¼s7çH GNîHØòíýæþ ×þ\x001eë¾\x001d´7w\x0011G5ªH\x001bvÏ¨àãÞ¹j¼.\x0016_<]É¯^£÷d¬\x0014QEwMn´êku©Ãçª|\x001bñ\x0003Gys Ìÿ\x0000»\x0019 \x0007³\x000f¼\x0007Ô`þ\x0006½¾pð}öÚ¾°\x0019âkyCF1þ°w\x001fB8ükèk\x000bÈ¯ìã¹²\x000cojùì\©ºÍAëÔ÷(Ñ«\x001a*sZ2É!FIÀª3Ý\x0017ùSõõ¨æ¥n~è<
¹Ë
(¢1ø<Ï\x001dxb/YSõk×«É<h<ÏÞ\x0017þDò-zÝT¶Bì(¢( \x000f
ø¢w|Fµ_îÛEÿ\x0000¡1¬ÊÑøwüLQýØ#\x001f¡5^ö]ü3ÉÆ|e¿·Ê4§¯\x0011L®}N\x0000\x001fÖ£²²P¼ÖÝ7K!À\x001eÿ\x0000J\x0002Ì\x0015T³\x0013\x0007s^¥á_\x000e®gçN ÞL>cýÁýßñ­q\x0015£B\x0017êÈ£MÕº#jÊÙlì ¶O»\x0012\x0004\x001f«\x0014Q_<ÛnìõÒ²°QE\x0014\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015\x0015ÄÑÛÛË4¤\x0008Ñ\x000b1>sR×#ã½P[i`÷·'-È:þg\x001f­kF©QE\x0011R|rgÉp²_=Ç¡ZBá\x0000À\x0019=+QÂ][å\x0002¶G\x0019íX¨î*ì¿C^Æ/\x0004ë8Ê\x000eÍ\x001c,z ¥	Æñ24lQÇÌ84¤9c=I¤®è§mw<ùZï`¢)w\x001f\x000e®\x0008{ëbz\x000f~AþÞ×x\x0012+ÄB3Ç\x0013/åÏô¯O¯\x0003\x001f\x001bVo¹ëá\x001dé\x0005\x0014Q\GIÌ|BÊð6¤AÆäTüØWÏÕï\x001f\x0013[oî÷¤ãÂ¼\x001fµoKc)îv\x001f\x000c,M÷l8ÊÛ½°8ýH¯£xïÁ
8\x0019u]I	\x0002\x001f¯Ì×±Öu\x001dä]5¡óçÅ[Ãuã«ÊÛE\x001cCòÜV®EåÅpÔoä+â	'Çº±?óÔè\x000b\Õ}\x0005\x0008¥J(ñê·í\x0018QE\x0015¹QE\x0014\x0001í\x0006¯¯.t[ø.$w	TC¸çnA$\x000fnz]p?\x0008m|\x0006yÄsqpïø\x000c/ô®ú¾o\x0014Ó­+\x001eÕ\x000bû5r;b¸¶\x0019^)\x0010««\x000e\x0008#_(Î¨2¬g1!O¶x¯§|M}ýáNð\x001c4VÎWýì\x001c~¸¯EwåÚLäÇ=R\x0016(¯Tà
ku§SOZlTw64ÿ\x0000\x0012\XÚ¬\x001eJH«÷I$\x0010=+èO\x0007N>\x0010Òî\x0011\x0015<Ø\x0015\x000fïcæýs_0í>
ñ\>\x0011ÓíE¢Éå¡]ÆL\x0011ö¯+\x0015ÅMj÷=\x0008cä¢¡VZ-ìõ¢¹\x0015½FiÕæ\x001d©Ý\x0005\x0014Q@\x001ekââ÷ÓÊ?øûW­Wk?Æ­
ºÕÍzÝTöBQE\x0015\x0005\x0005\x0014Q@\x001e\x000fñ\x0000îø¡/û1§þTäár#+\x000e êõ\x000cÏ«üK¾Ô%;,`(¤ço-x\x001fOã(mVÒ\x0019Y\x0000º-µ\x0008ã#¾kÒÁãc	ÆWlåÄ`å(J³vH¯à+K[Zi&\x001b¦\x0003D\x000fOB~¿ã^+É|%z,¼GlXá%&&üz~¸¯Z©ÌSUnÉÁ´é\x0014Q\\x0007XQE\x0014\x0000QE\x0014\x0000QE\x0014\x0000QE\x0014\x0000QE\x0014\x0000×`ªY\x0015FIô\x0015ãºæ¦ú¶¯5Ñ?&í±E\x001d?Çñ¯Gñ}ãZxnè¡ÃK\x001eýL××¯ÒVu\x0019çãjj \x0014QEz§\x0014QE\x0000\x0014QE\x0000hèW?d×¬gÎ\x0002Ê\x0001ú\x001e\x000fó¯d¯
É\x0004\x0011Á\x0007^É¡ê\x0003TÑ­®óó2aýpkÉÌéí3ÐÁOx4QEy' q¿\x0014A>\x0008¸Çi£'ó¯\x0011²±ºÔnÚÒ\x0016Vì£·©ô\x0015ô­¥Ûk:dÚ}â±`\x0003m8#\x000f®k,hzv¦Go§[,)¼n=Yø<ÔÖ*!ÆìÆð,Ztv´ì­æHe!T\x0000äçÛÒºY5ëç\x001f+$î¯øÖe\x0015
ÝÜµ¡å\x001e8\x0012Â[y$¤³J\x0011ò{ü Jç«¶øi«;À8d11÷\x0007#ùâkèp²æ¥\x0016xÕãËQ\x0014Q]\x0006!Gj*kHMÍí½º´²ª\x0001îN)7eq¥wcé?\x0006Ø;ÁÚU¶0Eº»¼ÃqýMoTPF"8¢(Qø
¾^ræg»\x0015dÅ|S»û7n83È\x000f~sü|û^Áñªø­¦`\x000fúÉ\x001ef\x001fî\x0007þkÇëÛËãj7îyxÉ^§ QE\x0015ÜréL¥'µ%CeÄ
z^\x0019C³R?åoÏë^q\x0004Fââ8WïHáGâq^ª©\x001a¢* {V31¬öG¢ÚÖXÔþ-UÓvjéÿ\x0000*µ^\x0004þ&}\x0004\x001dâ(©(óKÿ\x0000Þ|sÓWû§þÆ½n¼þóãÔ#û?ôIÿ\x0000\x001aõÊ©ô\x0014z\x0014QPPQE\x0014\x0001ä\x001a×ntÏ\x001ajúl0Fêf\x0012yO\x001f»A~\x0015¨jW:¤ë-Ë\x0002Ê0¡F\x0000©µ\x0005Y¾+ë;Ô0Vn\x0008ô
+mQ\x0014|ª\x0007ÐW¯8GSÉÆâªs{6ô9¨`¹ó\x0011âBÀ¤)ë^Ólï%¬O"\x0014\x0016SØã^y^\x0003n·¿¼ þ\x0019ù¹t+.3$¢+Ì=0¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003ø!]\x001eÚ1üsçòSþ5ç5è\x0011\x0014ÿ\x0000fY·¤Äãµçïåÿ\x0000ÀGþ#
(¢»NP¢(\x0000¢(\x0000®çáö¢C\i®xÿ\x0000[\x001fò#ùW
WtöÓ5[{µ?êÜn\x001eªx#ò¬14½¥7\x0013Z3äg´QMGY\x0011]\x000eU â_5±íQÕGú\x001fÑÅ^ªzÍ{\x0011@\x0018tQE\x0000cxJ:¶q
.é£\x001elU\x0019þY\x0015ãâ¾°Í¸aþÃy\x000ftFÒµF¸ÑnIeÇð·u¯S/­oÝ³\x0019Jö9º(¢½cÏ
èü\x0003b5\x000f\x001ciQ\x0011I|ãÿ\x0000\x0000\x001b¿\x0015ÎW}ð$\x0019Hì~hí¨÷È\x001fÖ°ÄK¥\x0015z\x001eð)h¢¾l÷\x000f	øÃv'ñt6ÀçìöÊ\x0008ô$ü±^}^±âï\x001aþ»âë»ø%´û4åJ¼\x0010P\x0005\x0003\x0004`úW\x000fâß	ÝxJöÞÞâdM\x0016õ\x0014àÃÎ½ü-Z|¦§^ùÚÐçé	 Sk©³\x0004)ÑÆóH±Æ¥\x0014\x000eæ ­ï\x0008Øý£S7,¿%¸Èÿ\x0000xôþµÝÕ\x001d\x001fO]3OÜ\x0010_ïHÃ»\x001eµ­c	¸¿ >óý+	Ë©É&ç;#¸²È±#ÕcP*±E\x0015á7wséb¬
(¢Ï1²ýçÇ¹¿ÙSÿ\x0000¢\x0005zõxM× ðçÅÝGT¸I£´{#ÆrQGzë\x0017ãN~ö¨ Cÿ\x0000³Vv±1G¥Q^v\x0019|8ßzÛQ_ûdÿ\x0000f«	ñ{ÂÍÕ¯Sëoþ\x0006£]ÌòâÓâ·­ôËþõ³ÿ\x0000AS/Äï\x00087üÅý`ÿ\x0000£\x001enÇÅ
}½%ãÀVýrúeÔZµ»Ø\x001f|3K#ÆøÆT¾Aæºõ°ÿ\x0000ÃGþ+\x0013¯\x0002½\x0012\x0005Ù\x0004iýÕ\x0003ô®\x001fLí:¼}·äý\x00075ÞW66Z¤uå±ÒR
(¢¸OP(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000£©éV½°ñ\x000b mÃ\x000cA\x0007Ö¸ýCáì¹ôû°Ã´s\x000c\x001fÌwÔVô±5)|,Ê¥\x0018Tøã7z\x0016©bÄ\XÌ \x0010]Ãó\x0015G\x00078Å{¥yÎ«\x0000Vº\x000e\x0004Çë]3ÍåMk\x001büÃ\x000fÆ¼R·ÈäB1è¬
ìW^Pìòydí
´ã>¹è¯à­øùC(üñü«%ÎW´N©äP§niîí±À}ã´-ùUÛo\x000eê÷±-ì¤t'\x001b²\x0000ýMh
í|(ÙÒ\x0008þì¬?ASO9«9[\x0006'%¥F2g\x0019oà]joõ\x000c\x0003ý¹3ü³[V?\x000f`Õï®Ú\\x0004chüú×mE\ñõ¥ÖÇ\x000cp´×B( Ú\x0008àvÇ\x001aQà
+÷Ôé
«¨\x000cÙIø:µUïFl¦ÿ\x0000v9ú(¢44ûù\x001bÑqúÖ>¹¥ÛêPÜY\.QàÊÄVþßûÍøU-EvßIïN2qwBi5fxN­¥\è×Íkr½\x000eQÀù\z¥^Ó«höÍ·ºL÷G\x001fy\x000f¨¯,Öü7}¢JL¨d¶ÏË:\x000fñô5ía±j¢´·<ÊØg\x0007u±Z¾\x001c×gðæ¹o©À7yg\x000e£¡ê?ÏzÇ\x0004Òä×\­%fs+ÅÝ\x001fKi\x001e6Ð5T\x001dF\x0008Ø)Ü#©ô ÿ\x0000J~£ãO\x000eéq3Üj¶Ç\x0003îDûØý\x0002æ¾eÏÒóÿ\x0000³á}ô;V2vØõ={ã\x001dÌÊÐèÝO\x0002yðÍø/Aøæ¼ßQÕoõk´_ÝKq/÷¤bqì=?
©EuÓ£
\x00029çRSøQE>(¤E(ÙÝ
£$Ö\x000cêp;×qáï\x000eI§0º¾­É\x0019HØr÷>ø­¿¾\x000e+¶¿ÔQe¸)3ÊÆÞ¾çùVÖ¼1¬Íÿ\x0000\x0001? ®g^õ=\x0015hþåM=ÌêØðÜ^f¦\õhOçÅcéü/\x000eÛi§Ç.ûGÐúë,L¹i³,\x001c9«/# ¢+È>(¢\x0000ùÏÆ\x001bÆ¹?óòÃòâ°ò=kê	,,æbÒÚ[»\x001e¥âSÒ«¶£¿ßÒ¬[ëná[*¶[\x0019ºz\x0007á)´\x0018uÞ#ä±ò\x0000¡Ïºsë]×ð^±Ë\x001fü\x0006zîÛÂÚ\x0003ýí\x0017O?öî¿áT5O\x0008x|i·\x000f\x001ef®©V \x0008¡IIØOÝgßýûFëìYû/þNs÷2võöÅW¯M>\x001eÒH\x001fè0þTÓá­ ÿ\x0000Ë~\x000cÆ»~¯#Îúô;\x001cç\x0007úuÑÿ\x0000¦Cù×qÚ©Ùi6zk»ZB#.\x0000nIÏçW;WE8¸ÆÌà¯QT7|1\x0006û¹g#×húþµuuá¸i[ÇY\x001cü«b¼¼D¹ª3ÛÁÃó
(¢°:( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002¸O\x0012¦ÍrcýåVý1ý+»®7ÅN&þôCô&°Ä|\x0007~\íXÀ®çN·ó|/\x001c?ß¿3á«Ñt¥Ù¤Úúd¿Ê°Ã«¶væ2´cêyÎ1]\x001b67\x000bé.Jç58~Ïª]F\x0006\x0000ãèy­ß\x0007·\x0017î§ùÒ£¥K\x0017|Økú\x001dM\x0014Q]ç\x0014QE\x0000\x0015
ÐÍ¬ÃýüªjltN=T\x0000æh t¥U.ê£«\x0010(\x0003zÉ6YÆ=F:¡«®'uÇëZê¡T(è\x0005gjëû¸Ð@\x00195¡¦C\x001cñÜG,k$n\x0002²8È#\x0008¬ú×Ò\x0017÷\x00127«cô \x000e;^øY§ÞîIìS\x0013\x001b
Ñ§uý~Àj\x0006ñ\x000eIOy£í%¿ï\x0007éÈüE}\x0003EuÓÆTSxhKÈùzH¤¶ÊÑ\x0006_NÍkop14\x0011J=\x001d\x0003:¤Þ\x001cÑ\x001d²Ú=>¿fOð®.±1x7Ñ7Õû-\x0013UÔ\-s6{¬g\x001fA_DC¤é¶Ø0iö\x001fTGò\x0015l\x000ct\x00152Ì?
`û³Ã\x0007ÃýFÕ¢:¤À\x001cnÙ\x0019ÜßLô\x001f­t\x0016\x001a]¦m¢
OÞsË7Ô×eâ¨ó\x0015¼¾Wô®jº)Uu!ÌÏ/\x0016*8ô:?
ÿ\x0000Ë×ü\x0007úÕ\x000f\x0011\x000ck\x0012z\x0015_åWü-÷®à?Ö©xcWÏ¬kýk?ï\x000cèû}LÒ»}\x000e1\x001eoþÐ,\x0013\Aé]î1¥Zúd¿Êk÷\x0010e«÷ù\x0016è¢óOd(¢\x0000(¢\x0000*\x001b´ó-&Oï#\x000fÒ¦ ÓNÎâº±æã ¥®ÆóM²M¥mb\x0019Î~Z+\x000bV\x0007Ùãäÿ\x0000vº¥Â2å±Á\x001c¤¡ÏÌVëîôËDu+k\x0010R;/zlí\x0003\x0002m£ \x001eiK4efáÕyoÃßò\x0007êßÌÖ¥Eo\x001cQB«
*ÇÔ\x0005\x0015-sÎJRr]NÊppè\x0014QEIaE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001\×÷¶¯ê¬?uÍøÁ3im'¤~cÿ\x0000­YWW:ð.Õâr=«Ó-Ë´?º?JóX×|Þ`+Ô\x0000Ç\x0015\x0017©Ù?\x001cO`òµo3\x001cK\x0018?â¬øA¿Ò.Õ\x0001ýj\x0017Ã{iû®Wó\x001fýj§á\x0016Æ£2úÅýE+Z¹j\ø#²¢+°ñB( \x0002£\x0014Q@\x001c¹ë±`ïc\x001e5\x000c\x0012¸ÿ\x0000hÖ¼ý\x0006\x0005\x0000kU=MwY\x0013ýÒ
\¨n×u¤£ý@\x001címiC\x0016yõcXµ½§\x000cXÇïúÐ\x0005ª(¢
(¢
(¢2|G\x001f¤»q¿§õ®:»½R?7K¹_úfOåÍpé`ß¸Ñâæ1µDÎÂßë.~ýj¿ÇüLã>±\x000fæj\x000b®¹\x001fìëLñHÿ\x0000N½cþ´ûÉRÿ\x0000rF	é^d»lm×Ò5\x001f¥yñ¯Em5ôP?JXÝòÅ¬ú(¢¼ó×
(¢
(¢
(¢*_}Å>õZßþ>#úÕ»ÑûþõVµ\x0019¸_`k¢ýò=*/ýüËÓF%¯åõ¬²\x00088=ElU\x001bØ°Þ`èx5xw\ÈË	VÏõ\x001dc'ÊÈ{r*åeÀþ\Ê{t5©WãnÄb¡Ë;÷
(¢·9B( \x0002( \x0002( \x0002( \x0002¤Hdî¯\x001e¦#ó%U=:Ò\x0000\x0001HeE²þóþB,ãõoÎ¬Ñ@\x0015þÉ\x0017£~uÏøÊÑ\x0017CÞ å%SÉü?­u\x0015â¤ó<9v=\x0000?\x0015\x001556Ã»Uó<çMÍÕ-SûÒ¨ýEzy´tÁú\x001aó\x00017ëöKÿ\x0000M3ùW«V8mÛ¿}#ñ\x0015è\x0019C\x0001Áú\x001fðÍs\x001e\x0015lk\x001bGñDßÒ½\x001eê\x0011qk,'£¡Sø×xT<Mn¯ò[?îuWï"Åðóc·Áô4àz#~U©K]\x0007fy2ùfß/Ùåþá­*(\x00038ZÌ\x000fÆ,¤=J¿PÜÝAem%ÍÌ©\x0014\x0011)wÎ\x0002Ü`qwK²îeôr?ZÞÐì¬<×'çbGÓ¥yÕ÷ÄO\x000f½ôï\x001c\x000cÎ\x0008¯ë^«¥ì:U«'Ýhâ3ýhi­Äd¢Ö\x0011ü9úV·£.Åäc¥ME!\x0001\x0005ISØâ»-.5\x001ae¾Td =+Í5ï\x0018èú^»}e1I\x0014¤0Xò=}k¿ðÖ·§ëÚ47:tþdj\x00020#\x000c\x0007B;U4Ò¸W66¯÷GåFÕþèü©h©\x0018Wû£ò¤Ú¿Ý\x001f:\x0000M«ýÑùQµº?*Z(\x00027\x001d\x0019
0Áâ¼¿\³\x001aV«%¬ydP\x0019K\x001eH#ükÔëÌüs}j5fÚ\x0015\x0013ÿ\x0000²y`?"?:Õ©N>ã±¶\x001f\x000fFµKVÑ×x{FÆÝnUÙÚx°`8ã<~uGÆ:s5²ß©UH\x0017k.99"µ|-w%ÿ\x0000´Ë¹@\x0012KnÀtéY\x001e>Ö °Ó-ìå`¯{.Õ$à\x0000£qþñ­\x001dZ|ýNxá©MªM{·0t}\x001aãY\x0012<\x000c±0\x000cd$g>¯F\x0016±`e?S\ÏÃùá¸Ñ®^\x0017\x000f¶å<d*ÿ\x0000u´:Ó©\x0015Î\x000f
JI*[\x0015Í¤G #ñ¦\x001b!ÙÈü*Ý\x0015%\x0014vqùR}ÿ\x0000¼µz\x0000£ö'þòÒýÿ\x0000¾*í\x0014\x0001Kì-ýñùQö\x0016þøüªí\x0014\x0001¨Z´vÅÚGóªl-,ì\x00068^õ±©\x000cØMôÍPÐÇÏ3{\x0001\Ó_¾G]7j\x0012-}_Uüée#£)PsïZTWK×ChîNXÚ\x0019\x0019\x001caÖ\x000cd_\x0007ÐÔÅ®T\(äpßOZf8\x0005àb2yP{ú×-?ÝÔåîwUj­\x0015.Ãè­67\x001f2
«=¯»å{]g\x0001Z( \x0002( \x0002( \x0002( 	í\x000e'Áî1Z\x0015\x000eAÅ\ðtó¤2Ý\x0014Õua ý)Ô\x0000â«ËK\x001f\x000e]ÉypÆÈUK­Ø\x000fS[UÅø÷À­ã\x0008­\x001a\x001bÏ³ÏnØùòQõã×Þ'£\x001aæ]\x000ecÁ:£â«xm¦\x0012¼jÒ6\x0001à\x0001OR+ÖëðÃÝ?Â2µÜsËs|ñùm+ð\x0002	\x0001GN@ëìjc\x0008ÃHV¯:ÒæWøËá§®5ÝGNt»·Va\x0012tÉÎ0xü{]\x0015iÙÜÅícð\x001d¯§xZÞ-jâIn,\x0012NZ%ì÷ÿ\x0000ëâºz(¤ÝØÐQE\x0014\x0000â=\x0006ßÄ$úeË¼k'*èyV\x001d\x000f¿Òµè \x000f-ðÿ\x0000Á«\x000b9V}jëí¬§#\x0005c?^çôükÓãbcB¢\x0000ª£°\x0014ú)¹7¸H(¢C8o\x0015ü2Ò|I<±3Ùê\x000erÒ§*çý¥?Ó\x0015?¼
\x000f¶I§óï®0$d$ QÐ\x0000®Ê®gk\x000b^áE\x0014r?:E7zx~tyýõüè\x0001ÔS|Äþúþtyýõüè\x0001kÁ|ká_\x0011j\x001e?¾Kk+öD1Ê ùevz\x000cc¿¥{Çß_Î1?¾¿8»	«´»\x0014Ó4«K\x0018ÎRÞ\x0015\x001f]£\x0019¯,øÛgw3i\x0013G\x000c[¯QIÃ\x001d¸\x0007ëõß1?¼¿&ô?Æ¿8ÊÎàÕÕCáq¢ø2\x0008î£h¦F
ç\x0000dvà
ì©ÓûËùÒï_ï\x000fÎww\x0005¢\x001dE&åõ\x001f-!\x0014Q@\x0005\x0014Q@\x0005E<ÑÛÂóÍ"Ç\x0014jYÝ\x0000\x0003¹©j½å¤7öSYÜ.èfC\x001b®z0h\x0003ÎOÄÍ;VÖîm\x0016é-´øW÷rJvùíO=\x0000ì;Ö§µ;íkZ¹»¶¦\x0014f(äaq&GÌ=\x0008ü,_ºT:}Fæ{Ul6'Ø°þW¤ÚÚÁem\x001dµ´I\x00141(T\x0006\x0002J%\x0008ss"Irr\x0013ÑE\x0014\x0012y¯> ÙÚø©tf¸\x0010Ú[×S\x0000NçÇ	Ça~*?\x000cjoâß\x0016C=ÈV¹Þf\x0018óee*\x0017\x001e\x0012È¬ýkàõæ¥â[«Ø58\x0012Îæf¼Åc"\x00169 \x000c`òxæ½\x001fAÐì<3¤E§Ù.ØÐeÌíÝ½9B\x0017æê8Ô+C^ªÝL\x0015<±÷_jl·Ã\x001fçU9'&(¦ ¢(\x0000¢(\x0000¢(\x0000¢(\x0000\x0004qô©\x0005Ä«ügñ¨è \x000b\x0002òQÔ)ü)~Úÿ\x0000ÝZ­E\x0000Yûkÿ\x0000ui>Û'÷V«Ñ@\x0013ÉÙü©>×7÷åPÑ@\x0013}¦oïþhûæ¢¢$óåþù£Ïûæ£¢$óåþù£ÏûíQÑ@\x0012yÒÿ\x0000ÏFüèó¥ÿ\x0000ùÔtP\x0003üé?¾ß\x001elßoÎE\x0000;ÌûíùÒncüGó¤¢\x000f­\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@
\x0019F?8K èíùÓ( 	EÄ£øÍ8]Ëê\x000fáPQ@\x0016~Û'÷V_\x001eè?:«E\x0000[ûpþçëGÛ÷?Z©E\x0000[ûqì­4Þ¿eZ­E\x0000J×2·ñcéQ\x0012Xä~´Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001fÿÙ
endstream
endobj
167 0 obj
<</Type/XObject/Subtype/Image/Width 396/Height 306/ColorSpace/DeviceRGB/BitsPerComponent 8/Filter/DCTDecode/Interpolate true/Length 17181>>
stream
ÿØÿà\x0000\x0010JFIF\x0000\x0001\x0001\x0001\x0000H\x0000H\x0000\x0000ÿá\x0000bExif\x0000\x0000MM\x0000*\x0000\x0000\x0000\x0008\x0000\x0004\x0003\x0002\x0000\x0002\x0000\x0000\x0000\x001c\x0000\x0000\x0000>Q\x0010\x0000\x0001\x0000\x0000\x0000\x0001\x0001\x0000\x0000\x0000Q\x0011\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013Q\x0012\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013\x0000\x0000\x0000\x0000Laptop Internal LCD Monitor\x0000ÿâ\x0004\x001eICC_PROFILE\x0000\x0001\x0001\x0000\x0000\x0004\x000eWin\x0000\x0002\x0010\x0000\x0000mntrRGB XYZ \x0007Ù\x0000\x0005\x0000\x000f\x0000\x000e\x0000\x001e\x0000\x0000acspMSFT\x0000\x0000\x0000\x0000LNV\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000öÖ\x0000\x0001\x0000\x0000\x0000\x0000Ó+LNV \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0011desc\x0000\x0000\x0001P\x0000\x0000\x0000vdmnd\x0000\x0000\x0001È\x0000\x0000\x0000admdd\x0000\x0000\x0001P\x0000\x0000\x0000vvued\x0000\x0000\x0002,\x0000\x0000\x0000view\x0000\x0000\x0002´\x0000\x0000\x0000$lumi\x0000\x0000\x0002Ø\x0000\x0000\x0000\x0014meas\x0000\x0000\x0002ì\x0000\x0000\x0000$rXYZ\x0000\x0000\x0003\x0010\x0000\x0000\x0000\x0014gXYZ\x0000\x0000\x0003$\x0000\x0000\x0000\x0014bXYZ\x0000\x0000\x00038\x0000\x0000\x0000\x0014rTRC\x0000\x0000\x0003L\x0000\x0000\x0000\x001egTRC\x0000\x0000\x0003l\x0000\x0000\x0000\x001ebTRC\x0000\x0000\x0003\x0000\x0000\x0000\x001ewtpt\x0000\x0000\x0003¬\x0000\x0000\x0000\x0014bkpt\x0000\x0000\x0003À\x0000\x0000\x0000\x0014tech\x0000\x0000\x0003Ô\x0000\x0000\x0000\x000ccprt\x0000\x0000\x0003à\x0000\x0000\x0000.desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x001cLaptop Internal LCD Monitor\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ\x0011\x0001\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0007Lenovo\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ \x000c\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000,Reference Viewing Condition in IEC61966-2.1\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x00004\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x00003»@\x0000p\x00064\x0000Í\x0000\x0000\x0000\x0000\x0008\x0000\x0000\x0000ù\x0012\x0000\x0004\x0000\x0000\x0000\x0000ðý$\x0008\x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x00008B\x0000Ê\x000eC\x0000Ù·@\x0000øuB\x0000\x0000\x0000view\x0000\x0000\x0000\x0000\x0000\x0013¤þ\x0000\x0014_.\x0000\x0010Ï\x0014\x0000\x0003íË\x0000\x0004\x0013\x000b\x0000\x0003\\x0000\x0000\x0000\x0001XYZ \x0000\x0000\x0000\x0000\x0000L	V\x0000P\x0000\x0000\x0000W\x001fæmeas\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000\x0002\x0000\x0000\x0000\x0002XYZ \x0000\x0000\x0000\x0000\x0000\x0000\\x000b\x0000\x00002\x0000\x0000\x0008QXYZ \x0000\x0000\x0000\x0000\x0000\x0000t4\x0000\x0000½\x0010\x0000\x0000\x0011eXYZ \x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x0010_\x0000\x0000¹curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x0019\x000c+\x001d;6yVä~\x001c´ëÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002	\x000b»\x001e\x00199
[Ps¹´ÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x001e\x000bÛ!Þ>(aðaÀèÿÿ\x0000\x0000XYZ \x0000\x0000\x0000\x0000\x0000\x0000óQ\x0000\x0001\x0000\x0000\x0000\x0001\x0016ÌXYZ \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000sig \x0000\x0000\x0000\x0000AMD text\x0000\x0000\x0000\x0000Copyright (c) 2005 Lenovo Corporation\x0000ÿÛ\x0000C\x0000\x0008\x0006\x0006\x0007\x0006\x0005\x0008\x0007\x0007\x0007		\x0008
\x000c\x0014
\x000c\x000b\x000b\x000c\x0019\x0012\x0013\x000f\x0014\x001d\x001a\x001f\x001e\x001d\x001a\x001c\x001c $.' ",#\x001c\x001c(7),01444\x001f'9=82<.342ÿÛ\x0000C\x0001			\x000c\x000b\x000c\x0018

\x00182!\x001c!22222222222222222222222222222222222222222222222222ÿÀ\x0000\x0011\x0008\x00012\x0001\x0003\x0001"\x0000\x0002\x0011\x0001\x0003\x0011\x0001ÿÄ\x0000\x001f\x0000\x0000\x0001\x0005\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000bÿÄ\x0000µ\x0010\x0000\x0002\x0001\x0003\x0003\x0002\x0004\x0003\x0005\x0005\x0004\x0004\x0000\x0000\x0001}\x0001\x0002\x0003\x0000\x0004\x0011\x0005\x0012!1A\x0006\x0013Qa\x0007"q\x00142¡\x0008#B±Á\x0015RÑð$3br	
\x0016\x0017\x0018\x0019\x001a%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚáâãäåæçèéêñòóôõö÷øùúÿÄ\x0000\x001f\x0001\x0000\x0003\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000bÿÄ\x0000µ\x0011\x0000\x0002\x0001\x0002\x0004\x0004\x0003\x0004\x0007\x0005\x0004\x0004\x0000\x0001\x0002w\x0000\x0001\x0002\x0003\x0011\x0004\x0005!1\x0006\x0012AQ\x0007aq\x0013"2\x0008\x0014B¡±Á	#3Rð\x0015brÑ
\x0016$4á%ñ\x0017\x0018\x0019\x001a&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚâãäåæçèéêòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0001\x0000\x0002\x0011\x0003\x0011\x0000?\x0000÷ú(¢
(¢
(¢
(¢2õ\x0019R(ÁÂ¾w\x000f\cük"°¾/øQðÞ¥\iÏ\x001aÉ5ÃDÞbn\x0018ÛéYS]êÖó42øª\x0011"\x001c0]\x000eV\x0000û\x0010pk¢~óGeEcÙè\x001e+¾´êßÄö&\x0019Wr\x0016Ó\x0019N=Álþ\x0011_\x0018ÿ\x0000ÐÍ§ÿ\x0000à¸ÿ\x0000ñu~Ò!¯cJÍÿ\x0000WÆ?ô3iÿ\x0000ø.?ü]qÞ>Õ|YàHì\x001eMVÆóíê\x0002ÙìÛ´\x000fözÐªEèÝÚ=\x000eðø[\x001e'ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×ªº3öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ)È\x0014È¡ÉU$n#°ï^\x000bÿ\x0000\x000b_Å\x001fóÒÓþüõèÿ\x0000¯âùéiÿ\x0000~?úô\=´O~8#¹Ù\x001c¥¢ÈËzôëEÔpÅ6Ø$2&Ðw\x001f_óð\x001føZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×©ùµô\x0005ÂÃ\x0004¨mgv8ÎãÕ\x001cWB¾5cÜ\x0003_.7Åo\x00142\x0013[)<nX\x0006G¿5ôý©-g\x0001=LjOåYUÙ\x001aSÐ(¬M( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000f!øûÿ\x0000 =\x0013þ¿Oþ^­~&P¢C	`ÀàWü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A®î×L=N;£¯j\x000f\x0018!©Ûå.W;O\x0019ÇãZ^ÑFKã#<¿2p^3ÆZZT\x001byæ&³#vÖ8ïÝÿ\x0000Bÿ\x0000 Îÿ\x0000)þ5jÏTÓõ\x0016u²¾¶¹(\x0001a\x000c¡öç¦qKÈ»\x00153uë/ë^CñàËö=\x0007ÍÝ6|nú%{¥xí
ÿ\x0000\x001eÞ\x001eÿ\x0000®ÿ\x0000$§\x0019]U{ðñN]»q!sÉ\x001d4V§"\x0014i0Ì$R^D®2\x0018\x0016\x0019\x0006·8mwaæßDÏË{!\x001eÿ\x0000þªO³è¿óúÿ\x0000ÿ\x0000Z¾>\x0011ðÖãÿ\x0000\x0012
7¯üû­'ü">\x001bÿ\x0000 \x000eÿ\x0000ëV±qKàAõ	ÿ\x0000ÏÇý|¯RÊ6Ai;H\x0008ù³Úªdzú³þ\x0011\x001f
ÿ\x0000Ð\x0003Nÿ\x0000Àu¥ÿ\x0000;Ã¿ô/éÿ\x0000ø\x000c¿áXÊ²½¬m\x001c+µî|¥ê(Èõ\x0015õið\x0007]\x0003N\x001föî´ðøoþ:wþ\x0003­O´E}]÷>SÈõ\x0014¹\x001eµõ_ü">\x001bÿ\x0000 \x000eÿ\x0000ë\åß´%ñÊÛ®b þËó<±\x0008Û»ÍÆqë)©Ý*
+ÜùÛ#ÔQê+éá\x000f\x0000IÑ4ð\x0007$ù\x000bY§ølIáë\x0012¾JçùSsHJ{\x001f<äz\×Òéá\x000eI\x001aºhyV\x0019\x0007ÈZó¯\x0011é\x001al\x001e%¾\x001b\x000bxãRQc\x0000\x000fRÔUÎ|D½9å´W~të\x0010	6\x00009? ¬Ï·h[\x0016ÉÔù\
Zû#\x0018§Sàg'Iê+µ´:MìÛDY\x0006y\x000cQ^çáo\x0008ørçÂzLóèZ|Éi\x001b;µºÄ¨É'\x0014*«±Ó­'\x0016¬×så|QFG¨¯¤¼iwàO\x0004ý/<3gq=ÎJE\x0015ªd(êÄ:àU¯\x0007'<i¥=åìbhË\x0019-(ØÏP9\x001eõ^ÓÈêú»ÚçÌy\x001e¢Q_TxÂ>\x001c¶ðåä°èZ|r(\2Û¨#æ\x001eÕq¼\x001dáÇþ)ý7¯üû­/hêîû%äz2=E}W?|/\x000bmÿ\x0000{Mfïþ¼~è<-áyÔáí4\x0011Ô\x001bu®(æ¸Y×xhÏß]?­
\x001e
¢7Cå<Þöï\x000e¥øNÒm?K´µ¯UKÃ\x0010RFÆã#µxz\x0011wW9§\x000eG`\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Î¯Cl6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ×iÿ\x0000	\x0004V·\x000c?á\x001e×&p\x0002\x0019c´Ü©ÏJâþ>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö½ÇÄ+ë\x000f6þ\x001cm61cÑ§bCá\x001dã¶ÐMo
rtè"\x0011r¨Ò5"¾Ñ¥8ÿ\x0000á\x0008¿Mì\x0017séH\x0015sÜJê­të\x001b\x0016f´³··.0Æ(3õÀ®)ü©,¬CC*\x000fÜóþålkx³þü\x0018/ÿ\x0000\x0013Y4ÊM\x001d5xí\x0001+I\x000e¦'MN\x0001nÂr+Ôlõ\x001f\x0012Ky\x0014wz\x0004\x0010[³bIVõ\¨õÆ9¯-ý ¿æ	þü¿ÉiÃâ"¯ÀÏ\x0014\x0015¯áoù\x001b´oúýÿ\x0000C\x0015+_Âßò7hßõû\x0017þ+w±Â·>¯o¼~´­÷Ö¹DóOÞ(¿Ó\x0005¤]M
ÜÀË?\x000eÿ\x0000/¢àöÉÏOJòW¸×¤l½Æ¨ÍêZZõÏ\x0019X¼¾=±¿´;\x001b&YW8\x0005;TÙ
Â KÉ_N79vÂã\x0012å0;îÇOÂ¹êb9\x001d¹èað\x001eÚ\x001cÒm|º\x001c×Ã\x001bÝro\x001bÛÛI¨Ü\x0008\x0004nóÃq+\x0011"Ð\x0003ß$\x001fÀ×º×è6ò\x001f\x001fé­Ë\x0005Fµ=ªw"1\x0018\69Ý»½zk	©Æç%j.ÜB¹{Ïù(Kÿ\x0000`ý­]Er÷òPþÁ\x001fûZµç=OÑ<ÈÙ?¼\x0008¬q§­·É|\x0004(Ù
0\x000e=+VçÌ0â#b\x0001>¹¨VÖ\x0005\x001cD¨­ÒÂ£§J\³ê&2Kmµ8ÚHÛè;Wø£þF­Gýäÿ\x0000Ð\x0016½\x0016\x001bx`ÌA·pÚ@é^uâù\x001aµ\x001f÷ÿ\x0000@\x0014äï\x0003ÊÌg\x0019Ñæs!âYÐÂÇjÉò\x0013è\x000f\x0015ÓøÁZUÆ%ÅÃ%¤Ñ*¤¶ñ\x001eÝ\x0006ÜüÙéYÐh²>-ìÈÄ!x¡B\x0001p;z
ÔºÙ¨h\x001am¥ÓÞÌ\x001a9fhÛp\x0018\x0016Olð:ñXëÐ¬­Î\x001aq¾W}O?Ó,
­ôÄ®\x0002D¨\x0008þ"y'ô¯£¼\x001fÿ\x0000"fÿ\x0000^qè"¼SSÓ¤Ón\x0004NÁÕ*àc5í~\x0010!|\x0017£@\x0002Ê"Iÿ\x0000tVÜ2êY¹ïdbxFû_ã½\x000f0\x001bu\x0001\x0001Y289?Oàí#û?PÔ®R<Gr±«\x0015\x0001T2\x0016\x0018\x0000\x000fFæ_ñ\x0005µÄ&Þ5\x001eVïõ¬psþÍO¡x\x0015¶Úæ#\x0000^\x0011û\x0011þ×¡¬\x0014\x001fµæ¾²ó,3¤©'¯ÎÞ·/x»þEkï¢ÿ\x0000èb®·ßo­Rñi\x0007Â·¤\x001c«ÿ\x0000\x0002Zºß|ýk§¡=L]J	\x001aõH"ÜàtîjM$\x0014m¦C 	Äç8ïPßÊ·32\x001c4cåÇ­2Úvµ#Ë\x0000'B¸í^T°öqIZW½µ³»6ßÜSÌ(û7\x0017¾ßðN?ãü_õþ¿ú\x0003W×¿|q!¼\x0015bÃ¡¾R?ï¯\x0001¯nÂpWøÀu\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®küªjô/
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5Pñ^³mñ\x000e×IJ´`"_6X	%H\x0007Ì\x000fÓÛÛÖ¨|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­ÛÝgÄ¶~2¶Ú³hyr Ü¥H\x0019mØÎìö®6åÒÙîe\x001a\x0015vní-7$\x0015x°JÊº$D\x0006 \x001f³ÜtÏûµ¯çøÛþ|ô?ûý/øV3ê;óX-[w\x0010\x000fØûgþºÖÇÙ¼mÿ\x0000A-\x0017ÿ\x0000\x0001dÿ\x0000â«\x0016YbÎ_\x0016\x001bÈí®¶Å¿xÑK!p=\x0018Íyoí\x0005×Eÿ\x0000~_äµê6vþ,[Èöÿ\x0000J{`ß¼X­ÝXb[òïÚ\x000b®þü¿ÉhÄ©ð3Å\x0005kø[þFí\x001bþ¿bÿ\x0000ÐÅd
×ð·üÚ7ý~Åÿ\x0000¡Ýìp­Ï«Ûï\x001f­%+}ãõ¤®cÑ9¯\x0010éXy5\x0018'\x0002EÇëYqhñÉ§Á}hªC@~÷Ó\x001eõÖêöÚmÜ]\x0002Ñ`\x0019.Ojó×%KäT±*¥Fä\x001e®\x000cE5\x0019s.§­ÇF_¸ÒqWé±Ðh:H».äùbÆÕÇÞ#ú
ë«'@Õ¬õ+C\x001d¬m\x0011\x0000Ñ·aëZÕÕFl>¶1bß´¼z\x0005r:¥½ýÏã[\x000b uÒrÍ4F@GÐ\x0000F+®®|ÿ\x0000ÉDÿ\x0000¸7þ×­á¹Ï%ua£Kñ\x0001\x0018mOMoOô7\x001fû=6=7\eùu].LpJÚ·ôzÇ·w6~\x0015íehÙäHÝàí9È\x001fZæm4y´]*ßWÓüèo¡Ì\x000b\x0012(\x0019`GÒÜT¬ÑQÁB¢ægYý¯vÔ´Ð{\x001f²?ÿ\x0000\x0017\èðF¥«ëw÷êÖ{ãQìµð½ï^\x0014XcF\x0015Ô0ú\x0011­¤ÿ\x0000Çæ¯ÿ\x0000_Cÿ\x0000E%9E(ès¼5&¹ZÐÁo
k9f:ÆªWiÍ£`\x000fûî³ô_\x0001ÞhöfÏOÖôâ¥~ÌYç\x000fQüaFÐ4û%¬sÜ\x0014áUxü2Gé\7ÃK{/\x001fé²n$7³\x0011Cc­cÌ«	\x0017\x001b¥¡èzõmM#Iµ%Ør¥lÛ?ú\x001dZÒ-|E/lm\x0013SÓÖÜ[¢\x0001öGÝ´\x000c`þÕÙµ ÿ\x0000È¿aÿ\x0000\EkN)Þæ\x0012¡N\x001f
ßs\x001bþ\x0011Íc?ò\x0011°ÿ\x0000ÀWÿ\x0000âèÿ\x0000sXÿ\x0000 þ\x0002¿ÿ\x0000\x0017[Wv/t\x0012Ká·
\x0000òX\x000c¹Îsø
u¼­,^tÓ[à\x0018b\x000bgÃéÅf§\x0007WÙòüÍ\x001e[EQöWìsÚÝ¿l|){\x0019ÔìdT\x001dÙó÷\x0000ïâÚßp7zO=qjãÿ\x0000g­\x0016È©¨ÿ\x0000×1ÿ\x0000¡
Äo¼~´ë{Hò±uêQå7d@.ü@å¾íÞOþ.µøuKÿ\x0000Ày?øºÁñEö¥5­¼\x0017RZÀ¨ò\x0019#$\x0016¢¯\x001d±çü+\x000e¹¤ø¢;+¶í§\x0016bÈp2\x0008'¡ÿ\x0000\x001açöØÖ\x0018\x001cDð[RV×§bÿ\x0000ÄëýfãÃ\x0016_Ídöét¥\x0016\x0008YX\x001d­Ô<W×«üOÿ\x0000rÛþ¾þÕå\x0015ÛEÞ\x0004aêJ¤/ \x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Uz\x001dømÙ5\x0014QY\x001daE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­{É<imãÛYá\x0013¾<±² \x0019\x000cd\x0000À»³¥d|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­\x000bÝ\x001bÆ©ñ\x0016ÛX¶ºM\x0011|¼C\x001cÜlÚ\x0003!\þ5ÑI¥\x0017vÓÌ¬3ýôõ4^/\x001fù­¶àÜqòAÓ?Z×þÆñGý
Kÿ\x0000ôÿ\x0000\x001aÆ}\x0003Æ¦V+­J\x0010±ÇúZð3ÿ\x0000\k_þ\x0011]Sþý_þùÿ\x0000¬fÏJñ\x000c7Iuâ5¸[/\x0017Ø7LÅyoí\x0005×Eÿ\x0000~_äµê\x0016^\x001dÔ-oa_\x0013êw)\x001be¡Gµý\x00175åÿ\x0000´\x0017]\x0017ýùÑ\x001f\x0013Sàg
×ð·üÚ7ý~Åÿ\x0000¡È\x0015£ ÜÃeâ-2êáöC
ÔrHØÎ\x00140$Öïcn}jßxýk\x000bÄ¾#Ãöv	n¥Ï\x0016ñãíY\x0012üVðr£ºjF\x0000A\x000bÇÓ8¯2ÔüYi«j\x0012Þ\ßÆdð\x0006p£²:
æj]\x0011XÜL©ÂÔÛü
-CX¿Õ.¾ÑwpÎãî¯E_`;V\x0015åýÿ\x0000ü$VX\x0002 ¼&xaüDÑýµ¦Ïì_¯øVmÎ§jÚÕ¬és\x00191nxÎsÚ¡BWÕ\x001e-
u%9Jq¾CªþêÞénmçxe_ºÈqô?\x000bøÐjr¥¢\x0016;¶â9Wúc±¯$þÚÓ?çö/×ü*UÔ­AVY=U7üúP£%Ð0ÓÄaåxÅÛ±ô5sçþJ'ýÁ¿ö½aèß\x0013tc¦Æº­Ì©v+\x0015¶ú7\x000bÖ«\x001eøwþ\x0013?í\x000fµÏö_ìß#Ùdûþnìco¥m\x0004î}"©\x0019EHé<NÚTÐÚYj\x0017°A#ÜG,QÊØó6GÓ¯4_¥µ®¥s9+\x0012ÂUÝyÂtÏ\w¯\x001cñ¶¼!ñ<·ÆSk\x001a¬VäÄãå\x001cç\x0018ã$Wàø­.wg;4×RÅäÇvc!Ñ\x000fÞÏ\x001f1Ç\x0000ûÕÎÚe¬CqG°è¶¬éÜém×÷}0ÊGb;\x001aIÿ\x0000Í_þ¾þJðO	xçÂÚ¸¸A$án!\x0008ß2ú>ðí^gñ\x001fÃV²j2ÍæDeo\x001eZîñÈ"E¦ªÝ³{Æ¶zmç¤[÷Xä_Ùñ\x0012v\x0000wÏCí\·ÃÈ´û­RkÛ«;k]@\x0000¶öñ.\x0011@ûÌ¹'æ&¸½OÄ¿ÚúÞ]\9v?*ùoÇ`8àVN}\x0015½¸\x0006Icu~GÈÉÈ â¹\[w±ç¼Ï\x0010¯É\x000fvë½úßô>\x001dk\x0013Aÿ\x0000~Ãþ¸ä¼7ñ?MK\x001f'[ºM\x0019ÂL-äo1}ð½GëTåø¦ÙxF+}6I¤ÔB5
nàF{¶Hç\x0015ÓE;~Ö5"¤´;=WÆ\x001a/ïíl5+è!ì)Â®\x0007W=\x0014\x001eÙëOÑ|S¤ø¥.eÒ®u¶Äø\x0004r;õSØ×ÎZ±:×æ\O"Ë£fõÉ\x001djÆ©\x000eKi­.~Ç4J6à2ýGNEv}Z5Ôµ·È·?wçÐ\x001e,ÿ\x0000SQÿ\x0000®cÿ\x0000B\x0015ßxýk\x0016ûânªx:x..Ö-FX´+\x001b\x0015,\x0018r\x000e:\x001cf®hþ8ðbÜ5Íîµ\x0012ÎR6þcê~Zóñ\x0011nI#ÊÅÑZK\x001aFÙaàyrÌ\x000bDáw8ê\x0007½Gg\x001cR	&\x0017x)\x0019;\x000f\{uük\x001fÆþ1ðî«u£\èÚÕ¤weÌ\x0017&\x0016Ìp°\x0019'+Î\x0008àsÉ®«OñÏÃm*\x0007ÏV¶J\x0000¼©7J@ÆXíäóÖ¹ýçæ=9B?QXHÔ{ß¥½>ýN\x0003âüßõô?ô\x0016¯(¯Føâ\x001d\x0017UÓ\x0012ÓK¿[£\x001dÖàU\x0018epFy\x001eâ¼æºè¦£fy¸h¸Ó³\x0001Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍ|T:¨¯µlÿ\x0000ãÊßþ¹¯ò¥W¡èa·dÔQEdu\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001eCñ÷þ@z'ý~ý\x0006µï|9®\x001f\x001eÚë6ñÉ\x0008\x0011¸¶óö¸@\x0000eÛÓoSZÈøûÿ\x0000 =\x0013þ¿OþW/¼ òüKµÖíõËOµb)ÆIvË \x0010?ÙÆN1ë]4dã\x0017gm\x001fKªjuuW³^£ø3Ä
+0×e
X}®n\x0006kcþ\x0010¸qÎ·®ÿ\x0000àsa?"iY·\x0010\x0005Æ$õÿ\x0000®µ¯ÿ\x0000\x0008W=fÿ\x0000Àù?øªÅ³K\x0017lü+\x0015äW+«k\x0012ÛpI¯\x000b#}F9\x0015å?\x001fÜ´=\x0015ß\x001f­z<?e}
Í±Ï·&o$a¡l\x001aòÏßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¢?\x00115>\x0006xÐ¥¤\x0014µÐp0¢(\x0010QE\x0014\x0000÷\x001bé_^é·Ö\x001aW4ÛýBh­íb±É,\x0017(£Ä×ÈM÷\x001bé_UßZÛ_|+¶µ»³ò	lmÕà·m®Ã	Ðþ¿D¹n¹¶:pýMHüYáÉ´íXµ+g°ó|=A+¿®:Vµ¬¶×±\Û\x0019T:8\x001c0=
yÍ¥\x001eºChÇHfÜÜ\x001fîÚ\x000b`\x0002s÷À­í+ÄÑZéÿ\x0000dF½mG\x0014,\x000b3Ú08äß¥sÏøáéÜô?uìüý{Xë|´þâþTyiýÅü«ÿ\x0000á~Îîl²H\x0005c|¯\\x0013»\x001d\x0007\x0019ã½uä\x0003ëAZq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*ð\x000f \x000f\x0013é \x0000?Ð§ûæ¾¯¾?ÈÑ¤ÿ\x0000×ÿ\x0000ÐÍ]?Æ¿Ày-\x0014Q]\x0007\x0008QE\x0014\x0000QE\x0014\x0000\x000e£ê+í[?øò·ÿ\x0000®kü«â¡Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍcW¡ÓÝQE\x0015Ö\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000y\x000fÇßù\x0001èõúô\x001a½}á]2oÖº¤:ü1jÅ0²s¸(\x001c\x001cú\x000f»T~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö£§ømü}hßÛ/m­9ü\x001eäÞ\x0000Ç=\x0003¡5ÕEµ\x0017fö{\x0018{IB­ãmÖû
þ\x0010ð¡µë\x0000K\x0012Aò=zVÇö'Ãßîhÿ\x0000÷ýøªÇÏÀ\x001es×Ð6âXy±õÏ#îV·ö§Ãùë¡ß´ÿ\x0000
ÁÜÔ·§é>	P]=4±x­¼©¶ïaó/ßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¯LÓµ\x001f\x0003K¨Á\x001e&o\x0019±\x0008\x0010>ïl\x000eµæ\x001f¿ãçKÿ\x0000yÿ\x0000ô\x0011N?\x0011\x0015>\x0006xÐ¥¤\x0014µ¹ÂÂ( AE\x0014P\x00027Üo¥}wc\x0002\x\x0017KK O²[3<_{\x0000)Çã~5ò#}ÆúWØZ4o/4Ä;ÚÆ\x00100Û{ÖUN¬6ìÈ·Ðè¬1xQ*\x0004\x001bYNÖlOqÀSÛ\x001dóV5
\x001b^¸Îä<)ó\x0018©ÎÓÎÝ¹ÁÀ\x001e£<Ö\x0016·ð8T;#÷·,Ùôã\x001f_¥k\x000càg\x0019ïÄê0,|9qgª%ãjJË´L\x000e\x001c\x000bsì+ ¢\x0000(¢\x0000(¢\x0000(¢\x0000+çïßò4i?õäô3_@×Ïß\x001f¿ähÒëÈÿ\x0000èf®Äc_à<(®(¢\x0000(¢\x0000\x0007Qõ\x0015ö­üy[ÿ\x0000×5þUñPê>¢¾Õ³ÿ\x0000+úæ¿Ê±«ÐéÃnÉ¨¢Èë
(¢
(¢
(¢
(¢
(¢
(¢
(¢<ãïüôOúý?ú
]Ôcð}×ÄKXeî\x001dttPaó\x0002 çø±nêÇßù\x0001èõúô\x001a¹}yá	¾#ÛYÍetÁ1!¼°¾fÐT\x0011¸ÀÜ\x0007ø×M\x0015x½\x001bÑì`¥\x0008Õ¼µ].^{\x0003´úàÇ<ÜuÍkÿ\x0000Âaá?_üþ&±ßTðp³¡j%Ã\x001cm'\ýk{þ\x0013{Lq¤kø.zÅ£QÖ>(ðÝåô6öññ#mý\x0011×©^+Ë~?ÇÎþóÿ\x0000è"½^ÏÅ¶×·[&«ÆÒ¶ÐóXº úÐW|~ÿ\x0000/ýçÿ\x0000ÐE8üDÔø\x0019ãBRÖç\x0003
(¢\x0005\x0014Q@\x0008ßq¾öOÿ\x0000äVÒ?ëÊ\x001fý\x0000WÆÍ÷\x001bé_døoþEm#þ¼¡ÿ\x0000Ð\x0005eTêÃnÍ:(¢±:( \x0002( \x0002( \x0002( \x0002¾~øýÿ\x0000#Fÿ\x0000^Gÿ\x0000C5ô
|ýñûþF'þ¼þjéüF5þ\x0003Éh¢è8B( \x0002( \x0000u\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®kü«\x001a½\x000e6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ÕÛýoÃ²|F¶Òît"o¿u\x0013j
ûX1PG\x0003¨Æ\x0006jÇßù\x0001èõúô\x001aÒÔ<E`~ Zé\x0017
´\x0008ã71(Ê\x001b?Ü\x001fZé£\x001ehËKèúØÆ3P¬vÕl®þCßÄþ\x0019Y\x001f	Æ\9\x0019ò­ù9ÿ\x0000zº/øJïèTÖïÿ\x0000â«\x0005üq
ÌÉÿ\x0000\x0008Õ±!ÏÚ\x0013Ý®k$Ç\x001e\x0011ü\x0018GX´h¬üGwuy\x0014\x000fáÍVÝdl\x0019eTÚç
^Oñûþ>t¿÷ÿ\x0000A\x0015ß?Äxlµ(í5kk;\x0010[\x00121Ô¢ÇõUæ¼Ûãn©a«e\i×°]B]þhd\x000c\x0007Ê:ã¥8üDT~ã<RÒ
ZÜáaE\x0014P ¢(\x0001\x001bî7Ò¾Çðã(ð¾\x001fñå\x000fö\x0005|rFA\x001eµè¿\x0018µ»K8-O°e5I\x000f\x0014\x00003Ïµg8·±½\x0019¨^çÒÛ×ûÃó£zÿ\x0000x~uóü.­wþºwäÿ\x0000ãGü.­wþºwäÿ\x0000ãQìÙ¿·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüëçÿ\x0000¤\x001f\x0014i89ÿ\x0000B?ú\x0019¬ÿ\x0000ø]Zïý\x0003tïÉÿ\x0000Æ¹_\x0015ø¶óÅ÷×7¶ðBÖñÔC\x0010NyÍT`Ó¹Z±l~(­NP¢(\x0000¢(\x0000\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Æ¯C§
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5gRñý¿Ä]\x000eçEµ},\x0008Ï,D¹R\x0001ó\x0003tÀ=½«[âfñf§ZÁtí\x000cÍ)gRÙã\x0018ãë\¹ðçÊ>9r£\x0018\x0006\x0010qÓOáz_G¹d¡Q¶¾ã©\x0019øJÈº\x0014D\x0006 \x001cOÏ?õÎ¹O>2ñ6a\x000eq\x0005¶÷]ä´¸gc\x0018à®p1ü©ÿ\x0000ðüCÿ\x0000¡òOûõÿ\x0000Ö¯6ñDü$ïkâ
VmJK\DgèB»\x0000{\x0013YÊ\x001cºnÆ\x0015¼\x0006yÖ5\x0007æ<3Z\x001a®¶Qcrñ\x0013\x0019y\x0015½g§Z[Á}ÃÌ_õ¹ÁïíRjv2Im6`VUPÍÓ,@É\x001e­s{Væ­±Ü°ª46ç²ír\x0007jJôßøS\x001aS¬[ß¦ÿ\x0000\x001a_øS\x001aý\x0005í¿ïÓwÙ+§+ìy\x0015éßð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a?áLj\x001fô\x0017¶ÿ\x0000¿Mþ4Y³cÌh¯Nÿ\x00001¨Ð^Ûþý7øÖø} è\x001aUºê¶ï©_ÌìK¬ï\x0012*\x0000)Iò«±ªRnÇÖ§ô\x000bß\x0012êñé¶\x001e_à±i\x001b
ª:ÿ\x0000Ö¯Dÿ\x0000{Âô/ü
üj[m'ÃÖ7	sg£Ëoq\x0019Ý\x001c±ßK>½j\x001dDZ¡+êy¦¿¡ÝøsZK½1¡Á-\x0019Ê°# Â³k×n´\x000eß\Éuy£Ëqq!ÌÉ})f>½j/øG¼)ÿ\x0000Bùÿ\x0000ÀÙÆhÐô<ô®¾çK°ÚX>Ìªª$+*©ÊF©¡ÞÜméÎ\x00075ÒMà\x001d3^\x0002
\x001aØi³Çó¼3Ê¬½1Þü ÕÌ\x0002ÜëÑTäDUöôÎ*¼®ör9M\x001bEÓ¯¼=5Ì>ÔÌv&\x000fAQxO´¸µâs\x001fÉ.ÇHÌ5Ç\x001f êXäg¶+¬ÿ\x00003¨c\x001fÛ\x0016Üÿ\x0000Ó&ÿ\x0000\x001a|?\x0007õky<È5Ø¢|ctjêqõ\x0006º*ÍN1­øS£8É·­ÎTéV^º\x0018Ìvë*Û¾v«\x00127duÂ[o^Ç¡ª:åµ¼QÛM\x000cK\x0013È]HU*²(Æ$
~è$ï·5Û¯ÁÍM$\x0012.·\x0002È\x000eàá\x00180>¹ÏZ%ø;ªO!mr\x0019$=YÑÄÇ8K±åôW§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf/g.ÇÑ^ÿ\x0000
cPÿ\x0000 ½·ýúoñ£þ\x0014Æ¡ÿ\x0000A{oûôßãE{9v<ÆôïøS\x001aý\x0005í¿ïÓ\x001fð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a,ÃÙË±æ4W§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf\x001eÎ]1­
Ú	òË\x0010ÄSå+¼*\x0012w>ÜØàsÀÝ]·ü)Cþöß÷é¿Æ\x001fÁÝR\x0019\x0016Hµ¸#z2#\x0002?\x0010h³\x0005NIìpÚýµ½½Ü\x000fo\x0011ÍRÆ"1¸ldãp\x0019ÇNã+ëë?øò·ÿ\x0000®kü«ç§ø9©I!Mj\x0007rrÌÑ±'ñÍ}
l¥-!SÔ"Ò²ª­c¢Znä´QEbt\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0015o¬ÅÜkÚë÷Iéô¬Ïì¿X?ï³þ\x0015»E\g(«"\nad]úÁÿ\x0000}ð¯2ñ¿ÂMgSÕ¦Õt§µ¦\x0000ÉnÒ\x0015%ÆA#\x001d\x0000à×¥ø·ÅÚw´¡{½ÚFÙ\x000c\x0011ýù[Ð{zò\x001dOâ¾­â\x001cÅjßÙ°÷\x0016ýã\x000fwÿ\x0000\x000cSs¬x4íKJtûûIEäGapíì\x0000\x0019ÎF:R
\x000b^Ön!²Óô\x001dE\x0011æS,³@ÑªíÓ\x0015±{³íJ718/Ï>ÜúÖöñ2ëA¸{MU$¾²NRU?¾E÷ÏÞÇ¿5ÃB¤jJö×sØÆÐ©B¯¦ßèÙ\x0017°ßgÿ\x0000£û"óÖ\x000fûìÿ\x0000ñ5wEÖôÿ\x0000\x0010iê\x001aeÊÏo'F\x001c\x0015=Á\x001dA\x001e´+»ÚÈñù|Ì/ìÏX?ï³ÿ\x0000ÄÑýyë\x0007ýöøÝ¤fTRÌB¨\x0019$\x0005\x001eÖAÉæaÿ\x0000d^zÁÿ\x0000}þ&¸\x0018©öÚÝ-\x001clN:rÆ½F\x001bn\x0014´\x0013G(\x0007\x0004£\x0006Áü+Ê|c'â\x0007\x001fÝ\Nn[-
(­¯
Ü,ZêBáJÜFÈ7\x000cò\x0006áüHÌ\+²ñ*4ûi\x0015\x0015vÊAÀÇQÿ\x0000Ö®6:\x0004ÙËwuvbÙEÎâGSôö®Ïû"ïÖ\x000fûìÿ\x0000`|;Ù\x0015®¥q#*(dRÌp\x0007\x0007ük¹h§MðÊ&q¹\x0018\x0011úU*JÈ9nbÿ\x0000d]úÁÿ\x0000}ð£û"ïÖ\x000fûìÿ\x0000nÑOÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÂþÈ»õþû?áGöEß¬\x001f÷Ùÿ\x0000
Ý¢k äó0¿².ý`ÿ\x0000¾ÏøQýwë\x0007ýöÂ·h£ÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÄG¸\x0012¼j½Ê\x0012Oê+h\x0000\x0000\x0003 éKEL¤å¸Ò°QE\x0015#
(¢
(¢
(¢
(¢
(¢
(¢
Áñ'm<;
\x0014Íu Ìp©Ç\x001e¤ö\x0015½^\x001fâÛ.¼U¨<NÉLkì\x0017W\x0008ó3ÌÍqÂÑ¼7z\x001bñ7V,JZYªö\x00041þ´ßøYÇüûYÿ\x0000ß-þ5ÅÑ[rG±òÿ\x0000Úx¿çf/Ä\x000f\x0014^ø]®j¶ùhä('y=z~U¤\x0018ü¹\x0006Ñæ\x000e§ÔU=O'TºÏ_5¿2Ò³Ü+ÿ\x0000\x000fFúVlû\x001a
ºQrwvG«G\x0002½@\x000ep¬Iï\ÿ\x0000­Ñ¤\x0005¸Y#;öïZ¶þ,Q¢_Â\x0008P0Çiýk\x001fÆw\x0011Í¥DÖÒ¤¬ÎS÷l\x001b¨öúWRuumÏ³Ì]:¸'ÊÓjÛ\x0014|\x0005ãK\x0006kF.útä-Ü>Ý\x000fï\x000fÔq_OÚÜÁ{k\x0015Õ´«,\x0012 xäSÊz\x0011^\x000bñ\x000fÃZZxcHÕl.í¾ßok
½Ü\x0011¸- 
\x0006ì\x000eàõöúVÁO\x0017ºÎþ\x0017»rÑ°ilØºG,Nãñ¯eÙêIÅÙÛ^uñ§Sk\x001f\x0001=²9W½!ãº±ÿ\x0000Ðqø×¢×|}¹ùt;\÷R?\x0005\x0003ùKq½ÿ\x0000Ùéí PÇo\x000bmÏ\x0019Ës[>#â]~é\x0013\x0010\x0008\x0000Éè\x0005bþÏ\x001fò\x0011×¿ë?Í«Þ¨`¶</ì×\x001fóí7ýûoð¤V¸Ó¯¬oL\x0013*Ãu\x0019bc=	Áý
{­bø¨©ðíÚ\x0001¶£<\x0010i\x0005{Å´º#lVvYT£&¸o³\Ï´ß÷í¿Â½?M¹\x0012[Ú\\x0016\x0000\x0010¥=;\x001aézacçÏ\x001dÏ6ðöÒÁÑâ}Bùæ!	4\x0000qé¸þÐ~ÏDÿ\x0000Â=¬®NÑv¤\x000cð>AX¿\x001e®\x000bøN¶Ï\x0011Y3ãÝÿ\x0000ñ5³û=È\x0003Zÿ\x0000¯´ÿ\x0000Ð\x0005>[ÉE\x0014T\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015â~2²ÇÅ7¢E!f9\x000f¨nE{eeëz\x0005¿j!¼C¹yTáû\x001féW	r³ÎÌðO\x0017G;­Qá4W]â\x001f\x0004®º_\x0019VV*\x0003G1øÕ\x001d\x001fÃ\x0007VÔVÓíb-Ê[vÌôüknx1ýþOÅÆ_èÖWFK7FøË:AÜW#k\x0001º¼ÝO2È\x0010\x001czµéß\x0012t(|'¤Á\x0007öîõÈXÄ{q\x0018ûÄò}ã^kc\x0014Ò\o)D\x001bAÕMg7uîCP¯F6Ä¾Ú^ú\x001d¬Åâûé^Û\x0007rÄXÜó]-|?c¹íÆ |À9cËÏðV³¥éð^'êúGu6í\x0018'bsÐôï\x0006ê:íö¥5µÖ¢ÆÞ4wEÚ§\x0003pÚ:zf¹)Â¶ª£M\x001eî.XyZXTâýtýY´|;£\x0010A[Ü\x0011þqKáß\x000eh\x0019ÕÓS²îKÔ¬f|°LðH\x0000\x000eqÅz.¦[Ë¥Å%ÊùÒÙsÜúVöEüûûèÿ\x0000h£m\x0019*óø¥s»ñ-ÕÕ¤°#ÍnÒ.Ñ,1|éî3Â¸_Âöô±ÉªjÚÕÛÆ\x0008C)\x0007h=qòñ^¿ýaÿ\x0000>ãþú?ãPÜévIi3¬\x00002£\x0010w\x001e\x000e>µZìªÿ\x00001ãúOt\x0019åkKÝYL \x0006ÁÛÓè+Sû\x001eßþ:Çýýjèü$N¥4wgÍEp\x0007\x001cJëÿ\x0000²,?çÜßGühÔ=^çMá»i³jÚè\x0007øDÍRéú\x0005ò2ÜêS\x0019\x0000Ïwc\x001eW«dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãKPöuácºXì´þI\x0005pbÉÁ©´½Q´Â\x0007¹ta©*>®KjÇÄ^JÎVßÏ\x000bå\x0001Û3]GöEüûûèÿ\x0000\x001a³«üÇø«BÓ<_©­þ¢×©2Â!\x0002\x0005Ú6Opyæ®ø:ÖÏÁ\x0016VÚgÚ¤K\x0004n\x0013q\x0004\x000cqW£ÿ\x0000dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãOPöU{çü%·\x001fóËÿ\x0000 ñ­}'P¿ÔvLc[\x0012C\x00120xöÍbMhÑøÊ\x0013\x001f³yÊ<¬q3×½v\x0010Á\x0015¼b8P*\x000ep(±P§Rþó$¢(:\x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000eKÇ\x000b7ôÌõ«\x0003ÂO³Äßí\x0007_ütÿ\x0000u>5ÌÐ|À3åJ­ô\x001d?­qz\x0014ÞF½c!8\x001ehR~¼Z¥±/rÆk]:çXÓÁðÌ<G@è9ÜzWÛYÅk»ËÜwuÉ®¿â\x0015Ë]xãQ,x¬Kô
?©5ÌS[\x0012÷\x001aÅù\x0017'ÜàWWðú9´o¤Ôþå@
:|ÕËWiðý~{öÿ\x0000p:\x0018!ú§Ä
~ÆòãO±\x0018-à
Â\x000b\x0011äæ±ßÇ\x001e's­\÷véYZù­ãúÎÿ\x0000ÌÕBB\x0000÷¢Ásª³øâ{9\x0003\x001dGí
:¤ñ«\x0003ù`×ªxgÅpø¯AºF!»
Í\x00089\x0000pG±¯\x0001\x00040È jéü\x0007«'Å\x0010}°]©·Óº\x0003ÎCLôo\x0003Fé©\F_Ü£Þ»ªæü7µÌ?éþuÒT( g)\x000e&ñ&O\x001f¿'òÏøWW\®|A»¶÷aúÿ\x0000uTØQE\x0014rÚ!ñ\x0006ÿ\x0000öÑé]MrÚêÕÕ¿¼ªOçÿ\x0000Ö®§¨¦ ¢)\x000c(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000¥«Z}»Iº¶\x001fyã!~½Gë^L®Ñº¸áÐ=¯YÕ.&·° Rd?(`3·=ÿ\x0000
ó\x0016ðwg{»f9$Äy5JÝN,V"tP7ÎÆ\x000fÄ\x000b\x0007^\x001a².m5$YÇ@Û@eúñú×%^þ\x000e\x0012Gå½ÌìÝ1\x001cU6ðNCÞ\x0015aÕHÆ?\x000cÓºîc\x000ceGñÓkÑ§þG\x0005]ÏW\x0016wÒ\x001fùè£ò\x0015:x"ÆP|¹Ë×lyþµ­¥è±hÖÓÛÄN%;)·c¥\x0017F´q\x0012ù\\x001aù£Èn¯O+ êìr~µQÝåõ+\x000bC¤Y\_Æÿ\x00004\x0010»üÖã\x0007×5åc¥\x0017]
¡ZUSr¿\x0012X$) çpEiÄJÍ\x001b\x0003\x001c\x0010\x001a©¥i×:éÖ3#¤o1\x0003û¨2jÊ\x001f\x000fûB¹ô\x0007?ãòoúæ?tµÍxoþ?&ÿ\x0000®cù×KY³D\x0014QLýKÿ\x0000ºh\x0019Ìè*\x001bVfÏÝV#óÅu5Ìøisw+wXñùþµtÔ1 ¢(\x0019Ìøqy\x001b\x000e­\x001e?#ÿ\x0000×®>bCþÈ®Ä©ûËwõV\x001fÊ·-	6P\x0013ÔÆ¿Ê¨¢C
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
(¢
òÿ\x0000\x0014ÈÉyþòÿ\x0000è"½B¼¿Å\x001fò2^¼¿ú\x0008¦ÎÀ_ñé{ÿ\x0000]\x0017ùTú¨ó5õBx%\x0014T\x001e\x0002ÿ\x0000Kßúè¿Ê¬\þûÄê§´ª? 
\x001dC \x0011n>Ïðÿ\x0000Xlà´>Xÿ\x00000_ë_6W¿|_Êð+F\x000e\x000c×1§×¥x	8\x0019¦¶&[¯ðWIó.µ=ZDÊ¢hò;¿M¿s~.Ñ\x000eâE\@Î%ýÆ9\x0003ð9\x001fzÿ\x0000Ã½ èÞ	ÓáuÛ4ËöÞ~\x0007áXß\x0015ô_µèöú´KlÜ,\x001dcb?Çæh¾£¶ß\x001dF¡"\x0013ó49\x001eø#ük§¯>±¼û/ôU'\x000bp%ÿ\x0000ß\x0000ÔW ÒcAP^1[\x001b\x001dDlJªêOåé
ÿ\x0000LÈ¤3#ÃIóÜ? UþuÐÖ\x001f\x0010\?«ù\x000fþ½nPÁ\x0005\x0014Q@\x0018^%\ÃnÞGæ?úÕ§¦¶ý2Ù½c\x0015CÄk\x0018Ûû²0jæÛ´eÇäh\x0017Rí\x0014Q@Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002¼¯â\x001cÿ\x0000Ùþ#O%\x0014ùð,\ü¯T¯&ø£ÿ\x0000#\x001d¯ýz\x000fý
©¡=ÃáþÙ<2;@i\x001c¾=\x0007è)è\x0004Þ)>Ò\x0013ù\x000fþµGðïþDÛ_÷äÿ\x0000ÐK`\x0003øV\x0007Ò0þ_Ö9?³íÑ4»|ÿ\x0000¬¹gÿ\x0000¾Tÿ\x0000ñUå~\x0019ÒN¹âm?M\x0000aæ{ å¿@kÐ~7Ïí\x001eß?v9d#êTCLø-£ù·÷úÌòÂ¢Þ"Gñ7,GáøÓ[\x0012õìÊ¡T*\x0000\x0018\x0000v¨/í¢½Óî-¦MñË\x001b#/¨"¬R7Ý?JÏ\x0015ñuõö{áéôøÃ\¥×Ë¿ è9üëÚÇNF+Ç|_	k+Y\x001f»|Áý+Ô4
Ium
ÎõX\x0013$c³\x000e\x0018~y¥ÍïX¿gh)÷4ª°@Òn3ÝqúÕêÍ×ä\x0013/=Jÿ\x00001L\x001f\x000e®,$oïH@+b³4\x0004Û¥©þó1ýqý+N
(¢2õõÝ¥ý×Sý?­?C é1\x0001Ø°?¥Öv7¶\x000fäEEáïù\x0006ÛF§Ð]MZ(¢Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002çüg«É£øvym¦HîäÂC¼\x0007¨\x0019¯#ûn¿~\x0019Î¥p3(îÃô§n¦~Ö\x001cü×·SÞDfGU\x001e¬q^Iñ6h§ñ
³C*H\x0005¨\x0004£\x0003¹½+m?Tåìïýèÿ\x0000J`Òu\x0011ÓN»ÿ\x0000¿
þ\x0014Ò)³Ö>\x001eÜÛ§­£iâY\x0003É.3÷jµ¢.íbwÏÝ
úµxéÒu\x001e¿Ù×yõò\x001bü+¢ñ4ÓÛ[iâ\x0019d91±SÀ\x001eX.b|bW\x001a\x0001-§ú$p*Úº¾§Ï=w\x0012;t¯Uøq¤Ï£ø\x001eÂ\x000b«"æ@ÓK\x0019ê\x000b\x001cûã\x001cWÁ¨­N\x0006¼¹{"T\x0012	\±UÈ8çµ{xACÖôÕ#¨k¤\x001fÖ¡6Û]g\x0005\x0015\x0017}ÍJFû§éXïâÿ\x0000
 ËxJ\x001föù\x001føÕY<yáE\x0004\x001f\x0010Xtí(?Ê¯]î?Ä^\x001eÄZ2Ám?s\x0015Äm\x001c¤d\x0002r¼û\x0012@¬?\x0000øÚãA¿GÔôÝ@³>Ù!Ý¤hä\x001c\x0012\x0000\x001d\x000føWm¦øDÒ\KPÝ'^/7?8ëÇÒ´OÄO\x0007©Ïöí¦}FOô¡Óo[\x0015\x0019´îtêÛÑX\x0002230Eex?Ùþº/õ¬ñ3ÁÃ®»\x0007àöZ«yã=\x0003^\x0011Ùéz\Ï»yEF\x001c\x0001×)òK±7GO£.Í&\x000fpOæI«õÄÚ|Ið}¤VÓkH²Ä»\y2\x001c\x0011×øjoøZ^\x000bÿ\x0000 Úßø=û0º;
+ÿ\x0000¥à¿ú
§ýøÿ\x0000£þ\x0016ÿ\x0000è6÷â_þ&e>Ì9Òê_K¹QýÂjÏú\x0014£ÒOè+\x0012ãâg®-f5¸÷:\x0015\x0000Ã ä÷i¶.Ðü<^ßVÔ\x0012ÖI0è¬r:g}(äÖ\x000b£¶¢¹Qñ'ÁíÓ]·üUÇô¥\x001f\x0011ü\x001eæ;mù7øRä`º:+_>\x0012nýâø©WÇ>\x0015~ Ó¿\x001b\x001fÎIv\x000b£ ¢²\x0013Å~\x001d|þßKÈÿ\x0000Æ¦_\x0010h¯÷u=¾(­&\x0019£EVMFÆAï-Ü³*ëS¤ Ê:°õS@:( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000c_\x0013øÏÂAÔob¸=á\x0002ÀO¯@\x0007\x001dI¯.¾øïpK
?C\x0007ðµÄÅ¿@\x0007ó¯jeWR¬\x0003)\x0018 
`Þø#ÂúMÆbXõd!?àÖÔåM|q¹2RèÏ\x0012¹ñÕÏîD©¶hØÖ0U
©<çßÒ¨Ýx¿QÑEÔ\x0006D\x0010qÐ}z×­Üü\x001cðäíî­óÿ\x0000<®	ÇýõÌà^Ùò5=E?ß(ßû(®Ô¡{ôìy¿ÙÉb~³}¤y\x0014¾5ñDÙßâ
OîÜºÿ\x0000#Tå×õõÚ½üïÜ¹þf½foÑ\x0010|\x0010:ÁíAþL*¿\x00025\x0001þ«\¶÷áeþ¦º\x0015|?ôÎIXo.¦`$º²z´×Sñ\x0006îÖæóNÒæ;Ø)hØ\x0011û}+ øûßï4ÿ\x0000e5ZO^)CòÏ¦Éî³7õQGµ¢ä¤¥°rÊÖ±ÆÛ\-ò\x001f2ùw\x0011©ä`\x000c\x001cUMFá.ïd\x0014ª¶\x0000Èçí_àß¤6þíÀþµ\x0003|"ñôÓ¢o¥ÌÔÔSTaQÍKrT%Ê¢õµíóèpÔWfÿ\x0000
|jó\x0006ÏÒæ#ÿ\x0000³Uvøiã\x0014ë¡Oø:\x001fäÕÕí©ÿ\x00002ûÃö&ñÍÕ½Í¾ ¸]_ËpÛN\x0017ÇWN~\x001dø¸uÐnÿ\x0000\x0000\x000fõ¦\x001f\x0000x°uÐ/\x0008ê)Î#ËÌÔ½n»/\x0017\x0016ÝÔ÷sÃ
b\x0015¥p¼^ïYÿ\x0000ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£EIS\y$Ó½\x0019ßÌ¸ÿ\x0000¼Äþµ\x001dt_ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£VªÓ_i}âå}vè¿á\x0002ñ_ý\x000b÷ÿ\x0000÷èÑÿ\x0000\x0008\x0017ÿ\x0000è_¿ÿ\x0000¿FkOùÞ\x001c¯±Ï\x0003Jì¾!^Áq¦O\x000cðÊM·Ïå8m§9ÁÁã­gÂ\x0005â¿ú\x0017ïÿ\x0000ïÑ£þ\x0010/\x0015ÿ\x0000Ð¿ÿ\x0000~D¥MÉKh;;ZÇ;Et_ðx¯þûÿ\x0000ûôiÃÀ\x001e,=4\x000bïÆ<UûZÌ¾ñr¾Ç7Eu)ðãÆ\x000fÓB¹\x001fï\x0015\x001fÌÔËð»ÆÓDÆxþÍG¶§üËï\x000eWØä(®Õ~\x0013xÕºé\x0001~·QñU2|\x001fñu²·O÷®Sú\x001aN½5örË±ÂR«²\x001c«\x0011ô5èIð_Å×ì	þôçú
µ\x001fÀï\x00120\x0005ï´´öód?û%KÄRî>I\x001e{\x0016«¨Ûÿ\x0000©¿º\x001fÜò5q<Uâ(Ø2kÚéw'ø×\x001fÀ­`ÿ\x0000¬ÕìWýÕvþ®Cð\x001aRGâ\x0004\x0003¾ËR
Ãÿ\x0000H|8;~.¶ÿ\x0000W¯]úèÂOý\x0008\x001aÓâï¢ûúS×Khÿ\x0000 \x0015ÜÃð#M_õúÕÛÿ\x0000¹\x0012¯óÍhÁðKÂñ\x001cÉq©MìÓ(\x001f¢ÊU°Ý¿\x0002gÜã,þ8ëñ`]XX\/rªÈßÌÒ»	|Z³ñ6­\x0006.qku6B\x0014q"p	98\x0004tô­k/þ\x000f²Á]\x001d%aüSÈògð'\x001f¥tv:V¥¦Ë\x000b\x000bkU#\x0004A\x0012¦!\ÕgE¯r:\x0015.¬¹E\x0014W1aE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ÿÙ
endstream
endobj
168 0 obj
<</Type/XObject/Subtype/Image/Width 405/Height 71/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 4481>>
stream
xíÿK\x001bI\x001fÇÿ\x0013ÿü² ,¤äÀR¸óü%Ëó`ä\x001eò(åô¸\x000bÊIkÃãºW¸®\x000f\x000f!Ç\x0011\x0004ÓÚ\x0006!èñØx\x001elÁ\x0016KlyÒ>eEYAÉH\x000eq¹ÏÌìÎîì×lb¬¶|^H1ÙÏ|æ½óùÌØ³3\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000NðÇv1Í¢ÇÇÝ\x0016\x0000\x0000Ðì\x0016¿tuuEþÝþã²Û\x0002\x0000\x0000\x0010cù»^Ð.\x0000¸\x0008\x000e]\x0018i3ø¶Õ)!ÒÕÈnvv\x000eî¯LÅ#]ü@öùiGë
x¢ÑáÁâaÛul> UÜ<G\x0015\x0000ð³[ü;&=ÙmÛõãÛ]\x0014aN±÷Ë\x0004¹\x001ezF8ù:,Þ47ö´É\x001búô®®Ñ¥w\x0014º\x0008ù¢uFþa\x000eÔ¦ÔåÉ`qÿÜ]\x0000÷íDÏ,Ù¦Ú¦ÈÌíß}¯_X	'\x0007°új\x0003?ùbê\x000c!_Ê
NægæÚÉæ§,\x0000¼\x0013Nÿ=¥;ýÔ¿Ùý2{\x0010iùn;ÛC.þ½¸\x001bî\x0011!åëÃá"äëxeÂO¾zFD}ÏÑøa\x0004ç¹Ôþzì<e\x0001àÝ@çÚõ\x001f­ðqwÞ¸v]Wªd}w¸4âb\x0000òÕ\x0006®Ü×¦ä¬ÊW@~\x000cä\x000bøÀ¡«)k\x0016ÐÄWOvÅVúË{µv(ÏÜ\x001e¸FÂÐîO\x0006'r¶Ã/ÙvÛôôçmTåè}¼)ç&\x0006>"\x0007\x0003>\x001aA¥Aàæ
]|ïØ%[½TLÌL\x001dU¹ÍgÙ±Oºípüæ©¤_ì\\x0013F¥¥ÿ6
9mE\x0006nÏl¾ð¯Öjö/&ß\x0018(_ûfÊÏU<ÀhMË\x0002ÀUáTN\x001bd§²¡P(f¤Q¤9\x0013·¤\x0017èKùô¹ÔërõÈVhIu)\x00128oë\x001e]rÝæ/wÝ°õMé\x0013×-üØ¹fð/\x0006Ú;ãô^)(iæYÄQm;5»äk[Øzq.ù
6\x001aÈ\x0017ðþpø³\x0011\x000eJ/Èg*Y\x0013¿\x001cã9¢O;#ýåÚ©üßÊ\x0004¹!\x0012\x001f320éA²Âè\x001a "sÈÌîS$?35È\x001bW\x0006\x001e:nó/£òïÇ\x0004C\x0003¬]ãß%r±{0.~mÜ\x0012y@«	¯Èµ\x0011Rjî9®nûG]ª²\x0019q,®÷M}d\x0016Asp\x0014Hte4¿åC\x001cðÎ}é}9;ÞC\x001fo\x000f;®|g|»¢0Z`Y\x0000¸ZK¬y¬$»\x000f\x0005còíYk³\x0008Q\x0015vaFÒ±\x0007Ö\x000cHk4·o®¾Fæ½VM\x0011C¯|åë\x0013ÉÜD¡kÄ®E¤¤¼òÒTÓIrÇ_çùÊ×à\x000c\x001b¾Ñ®]3\x0004ü|7¢[FüÝËn§²\x0018q¶\x0010]}óp$ÂÊW\x001b5·$_vl\x0011k@þ*ØhÁe\x0001à
AIÜFÃ¥/õwº±¾:dÓ_/µ\x0018=JAoöÆO\x000cY5\x0007ä¾Øù\x0018\x0015ÿãøð¿òjq*a{ºîË^\x0005í'ÞIxZ,S\x0019\x001cl£æw _ÁF\x000bS\x0016\x0000®\x00044W\x001f¶éRÁ
¾9º\x001a;¤k­ëÙúwÖYS\x000f«/×Î£1A\x000caiW¾Nß<F>r+DòõÜ'ÓFð^#ÙÛïÛÈ6jnI¾ÚÙylf´ ²\x0000pµ0cÀ¹Çî\x0015Å6M\x0015ÆQ|:9]}\x0005\x0001»ÐÕ×nDj\x0001±¸"¿Ü=>>¥±a«/?=ñ ÅÕW\x000b5_°|57Y\x0000¸r<7¦Øõ\x001eçÆ"þêîÖoºm\x001d·ß}¬'x{¥ß)üç®üÌÒ³sæ¾\x0002åËÖ\x0001k/r.\x0008[/ÈÂ{¦Z_ÈÛ~ÇÎ½s_g»óÎÜWË5wX¾ÌÕ²N\x0008£ù\x0005«\x0007=ÔmÀ¦p­?r4\x0010\x001e²*$\x001bÉô®îÛ"³«\x0018\x0011¾õÙÉì<F®´¼ó\x0018F¾ÐBlüM1\x0001Qò \x0003F+?\x001a!µÑ-9~lÎçkç1;uÓcç±ÛÞy´º7Ï\x0018Ç§æVeyµ(+áæ[\x0016\x0000® ôDî±\x000fìq\x001eMé_:R=§/³\x0003\x001e¹éÈÈCã|é¡÷1"Ls_ÁÁ£% ô¹ôtYËò°2é>Â\x0016W¢ü?»;÷ÕjÍm§î]+g[ót#47Y\x0000¸Ð¿ÝÆØNÔ/ù\x0018¯¿Ô>~³ô`LÐ_âúòÿX7Q]\x0012Ïf&nöê«\x0016NÝ7IÝ\x001fo?6Nw'&f~?n3÷e6ÃÖÈÁ|ø§×}lçÍãô]Ý½£Rñç¬çöhK5wH¾pó63c½<ùïy\x0011ÎhAe\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000 Ôµ|æI¹vÙÍ\x0000\x0000\x0000h	mK\x0012âR¹~Ùí\x0000\x0000\x0000hZùI^¾\x0012ÿ\x0011\Eâ8ië²[AP\x001e%¸x^étµi.µØE®¶!õÅ¥ÊIK|?'Ì*í=ñlÒ61ër:Ê§û0^Àµ¯®Ê,¸(¶$î«ÐÓ1H%ÃsRE¿|°âXR\x000b\x0007\x0017ÒØÐ\!ù:khõÖ!\x0014\x001d¯²\x0014O-´ñÒ9©kv\x001fz16i\x001bÖZý\x001cýºZ¼\x0007òUß*d~SÛ/ß¶|aÉbåk¸ðº^?2~¨\x0003¨«ÙB%Ì«lo53\x001fêÆp\%ùº\x0018:&_hºÖµ\x000eÔó>ÓÁ¥ìUâ=¯Úb®´_¾còå¹âB2\x0012n%ÖZ3â#_
UNÝr\ôFò^IõzÉª¿¦\x0013äÉyE\x000b,|~x¶\x001f½Áã>ÖK·lS@[\x0017ùOsÕ³kêúG+ÔX|<o
ö,áz8þã¤¸ìó2ªsä\x001e®').*2;ãö«¡®~ õO\x0016Þj^¥\x0016\x0014c9Dx¹û"n¿1+×Î´·IÜæ£û´\x0001´\x0008i^,).¼µôÐêoR,íÑ«MìfÄWêÂd2æ4ÑI5ÿ\x0005¹d/Gñ.E¼´´K\x0019í7»iÃÙ\x0017Ãs´ê,±\x0005qxÜø¼¼(&{°éR?k¦Á;\x0018µÕ×B\x000cå$zk3·±î[¯ÙJmy|Ä\x001d\x0014\x000bË¤1N\x001d°òô1OÇ`ð\x001e><MÈ\x0013\x001d\x0001W£^$×cÂ×Ö `ó>\x0017îááá?Nå6,S»C6	ÈÒ¨Ò\x0007æ\x001a3¹|îm¦òFE·-r²o¡q5\x0006\x000eõÎæ"\x001dx_xÊW­4ÊÇnå+{õú^%+ÆßYuvt$ÿªVÛ)IÉÔÂ^P)ÒlA\Vj\x0007jM;«/32¥ïó}3UÃ\x000eôººâ£ÉÌR;ª)ËR"È½ÒÎ\x000eJ©hl|¶¢\x001eÕÕ­üx\x000f?ù«ËôG«Q>ñm\x00015£¶S.ÜMðQkÆ5í\x0017~Ç}¯\x001eà&G\x0017TW©Ü(OK\x0011§B\Wë\x0007Õ»\x0002?4ì\x0017K;µú,Æ9AïkÊsF¿Ôr6ÉGÅ2ñ<íU.\x0011O\x0017¶ÔúZIñq¢çgNùbÍ¨U2B4!-&\x0012r¯õÛø¾{«*ªgv<9íÜ\x001dò+¥§5ø¡Û_Î\x000cñüý²{RxÊWý×I>.ÊÈà¯
©(|T­\x001fiFãQï±xµsÉy5¬\x0019¶J¤çõá. âB¶¢¹Ýc-ò©EÕÑ*çG½£9ôPõÀ9ìÌmÞ>æå\x0018UýïuN¦
¯\x000càî­ÖpÀ¥U²\x0002ß/aW9PJ?$Ìûõ!&]®U\x0017Ó\x0002,\x0010%D\x000bÿêaî¾ll\x001e\x0013¥¾zçûI\x000eò<\x0012::ïÓ½
Ââ)_
­~$fPßzµÕ;±dVV\x000eÐ\x001c,q:OOêõ5û¼Pµ\x0005çÁK¾^çú>*¦ïÈinÒé^û\x000bÃÒ^7Bx¤Xeë«¦\x0011´²\x0018í3f9Uë«éh´eÍ\x001e4|èßêL_ß´õ\x0004m-Í¹Ü\x001eÝÃÝ*Y\x0017\x001b*\x001a\x0008cÆèZ\x001cîû©JËÒ~QÁ\x001cÆ¹T	×8½F¿@\x0006á\x0012ù·ô¶
ûÜprÇ·4ª¹O\x0019ã[£\x0006eØH²Ùå1#òOÛ"VyÐß\x0002å\x001f¸ñeÚ+§ø"Í\x0015×«\ùÎeð/M¾ÇÏ4ÓÖÚ\x00065þ³¼BÛ`½¶Â8ÃVBRw\x001bâ3Ò\x0006ã\x001e\x001b\x0012\x001d£`ùb:èz~y8\x0003¯áS$\x0012O\x0014ãòåÞ¬\x00084üg}ôÕc\x001bb6Nq\x0006î	È,Ì¬\x000bj1Õôé\x0006±áHÝ[íq\x0005LpË(\x001b\x001f.>xÄsâ\x000el'býùuUWÑR®5päøYAqt
ý\x0012Í¸æc	Mp¢fÙCúôPý:©dúc;ùò¾ÖÌ\x001aö!v¼ðÂÃþ>\x0001ëcC«íTÊËÌ\x000fã9(vùbºV\Í2Üi¿4Þ\x0013\x001b.U\x0016\x000c*ÅÆ\x0008î.c2Ç£)mÐ.¡uQ/vèÇp\x000eæAêÂçäÛ=\x001aeÓç`°|yôÈ~¿¹\x001cÃ×ð!1\x001c.Ò\x001ajöhÉpo\x0017úýÂ~tå¾\x0013ÐÖÅsj°Ëçé^\x0006±ãHÝ[ï\x0002¯Ü×Z]\x0017f3é!ÞjÌ»¯oJêµ¿à·ÒÓö+o\x0013±¡|U\x000b*åÎ÷¢p\x0003­U\x00129Z¯§\x0010ò5¹¬²õ»réÍä+L¿\x001a\x001a\x000eUúcÉYÔ-Rêìå²\x001d¯Õtb<» ¯WU¼\x0014\x000f#_BnËÖ\x0017Ë\x001aue-7Ü#¤sx©öåëLOò(jàG.ÉëÔZ\x0001òÕ| .M¾|}Ìî\x00186|\x000f¿õãZé\x001bÞQûÿ«)òEêg& ­?Áòåót/8º\x00192u¯U\x001f
ß\x0018J\x0017Ë\x001a\x000e{ß¡|éám\x001d´Z¦Nå_Êc»JCC,¼&ÿºÓÔ®àñLÃ¿£w\x0019ïP\x0012WÃÁ#zÒ]&xlÚ/ó
\x000e\x0006·ûê¤|¡f[Q\x0016F¾ð'i*¿Þ*G(±áv\x0015ÿRç¯³º,ÞÐ_ã|"kE^~ò\x0015ÎÁÚ\x000b\x001eq\x0007Ø¹"E\x0013 \x001e9úâëcnÇ`ð\x001d¾R\x00182V8±[t\x0002oI£Uöî7/3\x0004³¢\x0013Å\x0015<â(Ø
\x001e½ÎÐ|
[gð#¬8\x001dEÐ6ùúÜ9<\x0007X¾Ä5\x000eki\x001fÊ^áTdu9ìIìçjËã±¡LÙÈÖ
$çã[Êk·\x001d'LÉ$YQüR÷87{#Ôì¤"Åùd¶TÅ)ßj)¦`R÷õ½Já®#\x0013ãéMûU+Ý%³e8}âó¢¤T?MÌ.J´T'å\x000b-`8=û½#g¾ñÍå\x000bÏ#dùô|$HË¨§7þYÑ´J..¤\x0017«µ#U¾/ðw])%ÏRgç/4y\x0005d´=EÙ¯Ù^å~ò\x0015ÂÁÚMÝ}h*GRÖ¥ûå`áäËÇÇ<\x001dÃÂoøpq§¤ì+Ê^­ÆX\x0006·?.¬ö¯£®\x0011÷\x000e/Ôw\x0001ÈÆ×\x0004daR÷ÈiçÓ\x0002ÇÙ&×Ó½
Ââ{î\x000b§éû2\x001e©:y¿ð©'Ø	+¶]\x0003=u,k¸Uµ#ïÁh\x0005g2¾5jåY}k%'=N¤\x001bßäp\x0002=8á]Êó°\x0010^WsæV\x0014Áÿà\x0004ÝAÆ"òú,zÂ7>'å\x000eN4ë\x0017Ý4·jð.ÕÑàñD)Ü1+Kaä\x000bÙðmIo-Þõ;=\x0017aåpãYê<òUF\x0017_:=ã%×¾ócÓhóà\x0004î¢\x001fÕÀ\x0016`N\x0005¯3\x001f\x001fót\x000c\x0013¿áÃ+Fh
¦,\x001bíç?NIkªË¼îôtJt\x001cgÐ<' KÀÁ	§û\x001aÄ$àÔýþª¨Æù	Û¸öL2OËT¶H$åÎq
\x0000:C£Ö{V¤ß¨§\x0005Îã D«¼\x0007GI@1sYxF¶ÿð\x0011ÇKl\x0011\x0000\x0000,®UöL4¶ØÎÅ\x0007 _®ý¸BÂcO
\x0000K$:d\x0011ÎDå{øÔ¿Î¿¹ô\x0001ÈBGán¡¼Sd×\x0017Ø­
\x0000\x0000.rîëþGC®LTÛ|\x0000òÂÇêÂ½a¤øð -VÙô\x001d\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000À%òÇ¤ 

endstream
endobj
169 0 obj
<</Type/XObject/Subtype/Image/Width 273/Height 158/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/SMask 170 0 R/Filter/FlateDecode/Length 901>>
stream
xíÛÏÜc\x001c\x0007ð÷ìÎvwfwúCtm¶H[Â\x0008±Ø\x001eX4A¤\x0007MI	MpÀÆ¯ÒÆ¯¢]ãäâàÂ84þ\x0001\x001c\x001d\x001cz\x0010å?ñe3ûíLÄÌæõÊ=|wgd3ï<Ïçy>MÖ\x001eï%+Éöl¤<©óé\\x0018h|¹»3ÙØð­áðQòñ\x0010£NúLP}Ú¯MãÛÌý\x001d\x0003*2÷¤)2!#s&9Ìö úÝ\x0013¬>ù¿¦#2¿a"S½ö¹ä²MçhõRÓ</2l\x0005ÃDæýd9iÖæ`&~\x0016\x0019¶a"óNr}2Qg«\x001f\x0006*gD\x00113Ld>LnM&ûO0===??Í=ç2+2¿!kûmý'h·ÛËËË\x0007n_ú*maüÕL7]âtÿöðéþÇe«\x0016\x0017OfúÂÅ3"Ã©\x0019*)ÇGÕäµä­RûW¯}#¹©9Óh4:N³ÙÜÆ7\x0017¿7\x0013\x0019FLÍÈTI9P"s[²?Ù,&w&÷&×Õ<4k'¯fÈ0æ6L7y1¹#y$¹¯×ü\x0013Éã%8SÕ¶+ÙYnø7wW&ÊvaÌõL·\x0004äPé"«\x0016ù²VTËÊÃe¶ZÒ´¿fd¦ùZ±×?2U½ÿzéù 9,ÞË]ÉÞ²I;^NÌæjFæD¦\x0013\x0019Æ^ÿÈ¬?è&/'\x000fÅ¥JÊ3É¥Uf)¹¼Ô5³É\x0007§zze\x001a{Ó¸¢¬O;df+¨SþwËÉØ©2N'ï&/¼,ô{û´Ë¹Ùº;ÍV/c¥ýeZÝLWC\x0019[BÍ\x0013³WJÇòS¥´9VÎ\x0001\x000eö
úÞÏ'Ê!À:7¤ñEZu/\x000c#¬NdÎö:{¹X-;´#%&'ËrS­>Ëöì\x000eeê»A¿##2°:Y+wgJvNnÌêÉÛÉceK¶sÃ÷½%\x0013dæÇÌ
pã/2°\x0017ÊÚQ<_ÆÑäÆäÒ>íd_&\x001eHólf¾Nû\f\x0007\x001b¦U¥Od\x0018\x0019»\x0006\x001a³60ÿ©JÔ%½\x0013³ÆÂ cw\x001a­ÿú\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Àz\x0000û
cX
endstream
endobj
170 0 obj
<</Type/XObject/Subtype/Image/Width 273/Height 158/ColorSpace/DeviceGray/Matte[ 0 0 0] /BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 9087>>
stream
xí\x0007\ÔÈÛÇ­ì\x0002K_@éHQ±cAEADa±b÷ìgÅzö½z"*`ÇÞÏ³ã©\x001c**Øé,\x0005¶eòf,,²ïÿ¼;9á÷ùèf3%ï&ó<óÌ$È1*oP\x0012Ì/©ü¦/|§Râ\x001a\x0004JÇWe`¸¦ÕÎð.°~\x0001©ÜkTAgê\x001bE}\x0007Ýiªv¾ü©Åõ\x001dHÙd-õ,ýeõ\x001dHn S=K³ú\x000e¤|4§:KÇÄú\x000e\x0004[¥SÁ`ô[õ\x0017\x0008PÈ\x0001ñqÁ´:ÞV\x001b°ú
Dñ2æÁËtòã\x0010VU\x0006	ÇùQ}\x00058%f¯[ë¹ü¹êy´×ÔO à÷IÑ+®¿ïÎÓ·¬q¾\x0001åõ\x0012\x0008x³¹øa}/\x0012zÖ°»ãåõ\x0012âUeÙ)/sÛ.1ÏWÕ\x0000²\x0001ÔK \x0012<[·7æjÆñM[
-($ºM¬¬®~Ê£~\x0000!n\x000fyy¥ùÇzôô\x001f1\x0007Sù/Ü)©¯@ðg{Ï½9¹|ñ¼Ïì´"S[_«=Ò­G@\x0014Ç÷<L:ó.ÿã\x001eG*uèk<ê\x000b\x0010yz¥T#Ï<2\ev;\x001d\x0013×òR¿s ÷\x0012kêÁ½è\x000eUnKè/æ:Ýé»\x0005bû©llõtÐ¦V\x0016[[Kþ7jn\x001aÔ \x0006Õ#1NÂïÖþü\x0005qý\x000eßXaúå|õGæ«²fkëVÔ%5^xùX«oÝ¯®@ MÝõ¨@ Ã >y\x0002\x0001\x000c©²\x0005\x0002\x0001í²ò\x0004ºpb£+ ÇÀk^úÄ\x0006(®\x000e\x000bai\x000b\x001cºû¹	\x0004|\x0014Aµè¸tN]\x000eR·\x0015°ÛÜò:°Ã\x0016AÂO\x001dób ì§\x0012NÏj\x000cS¸ó\x0012\x000e\x0004\x0010!±	Ó\x000ffMwR^<\x001bÀe´:P¥ÈvçfjóD¸\x0000ÑtØ:\x00199Þ¬=4J:Ôý¹¦Ô
åbXÑ*}bC'ª\x0012S>w#®úãrIo&¢5Z)Ó\x0006ÁIMþq,s
ñ9¯\x0010;@\AÎ1Å\x0000Çìõ"=ÿÌê%\x0012¯\x0007 ~©ÍÊã&én)±¥¬H?æ
¯À\x0005¥TRÞLî¶çKãØ\x001fAD³\x0000\x000e^´$TVô!!\x0006ÂÊÄ\x000e\x0002ÏJ|\x0017ã\x0007\x0011D0£\x0014¼Þ±.Y\x000e\x001e;õ|.\x0016ç\x0003\"\x0016\x001f\x0005 ~OpI21ö»³Ö\x00001ci\x000fU\x00030¶²P\x0017Âaá¡uü!\x0000é\x0001\x001bÄâ´\\x0003\x0010P¾H÷S Ö1 `¦\x0001×îø³Ö\x000c±©©ÝÎr|©©©\x0011\x0017\x0002Ir×ÑÑÑÖB!\x0010ùP=Ý\x001f
ÁÓ@\x0004 \x0003êø\x001dB\x001c«5=\x001bÈ\x0014\x0000QVÈð×m\x0019\x0000ir
Ï\x001dO\÷æT
Ú\x0011\x0012|&µI\x0000yÜ®\x0018\x0002	f"æ·ñô±(	ää78½ÿ]b¹¿\x0004»8æR²¹à\x0013 .KÁaóOnP`UýÒ5$y
H#C\x0002	Õâ¸?\x0007o#$3ÐÈÔñ\x001e\x0004\x0002y\x0015zFQú±\y²s- »Ç%c¥£¸5p\x0002+AñÑ\x0001VôTEM 9û""Öÿ¨G\x0002Q¬î7ðByÃ\x001b!¤EDD¬è£õÔ\x0015ÁË¶RîãK- ;íÁSÏ@\x0010½\x001fî\x0002 9ãG9%5\x0013\x001a·,I \x0000Sb@6\x0019º®\x0004\x0010¨Ò5ot¢ÿ_\x0011@<,7áåk\x0004Ík\x00031t¿ WFÖ\x0004ðºmN$¤\x00062à·@$ïÞ½½SH\x0001\x0011gÊAájr½\x001a\x0001¤àîÝ»W'ÖuÇ\x001e\x0002av<zÌ\x001dÕ\x0004=ô\x0003(\x001a{ª&\x0010â"éðóS\x0005¸I.Ý¬	äeOOOG\x000e	D¹iä¯ h\x0001L"Ü RZ6fjjE\x001d\x0012\x0004h{\x0005zð\x0010M@\x0010½\x0015àÉ\x001f50+Cot6.ÃZ\x0019v,ìÕ@èyü¬ÌK\x000fzS#\x0010¤}2&¯P\x0007ZèBØ
×T¼¸3,ö§f·N*;\x000bG{ß\x000f\x0010Îd8Y
\x0004µÛ8·µÛê"ü
yò5¼\x000f\x000f\x000b\x000bû¡Ê\x000fq¼\x000c·Y@\x001e\x0011)aC\ëø=óE Éi \x000eÑö\x0001¦ÈZaH§¢&\x0010¹8;;ûã>#\x0015\x0010NP:ø0\x000fT\x0012)Ù/&ÖqOäË@\x0010¯\u ï
9\x000e\x0000\x001f0&Õ6»¸ì¤
\x0008b°XýÞA]<V\x001d\x0007ÒOÔ[Þ\x0014\x0004ü\x0008×^\x0014l"\x000c;Q°'5\x0010ë\x0010\x001aÚ×øt

m\x0003¿\x001b¢nÞþÅ\x000eu0[\x000e\x0008¥§Í{
nÏA´Z3¢Æ}BØÍ\x0007PIý1þÕókP\x001aÔ \x0006}K\x0019\x001aAésTóml}#Jºª\x001c\x000c\x0003#\x0003ugEäÐ«^é0tªÅC\x0011\x0001Y¡ºqe\x0011»TUÀÜ\x0006,Õ¡\x0004ä^vS¿~>äNvUEd\x0016Mç~\x001d\x001aÓ­G6®	\x0007¢¶Q\x001db\x000eÐ °9Ð:¢|µvi£¶¡j\x0011n^ýû¸«ÆÝ0\x001f¿ªÊ¨xBq¶Mñ *t^\x0017OêÈ<Uà¢ñÎ¸\x001d6jçï¹'>~{jãi2+6^¥Ø`mf8YáÑMTYP¯
ññ¿´¤¾6ú)>þ/y\x001enâ\x0017YÃ
fOz\x0018?ÁøQ<\x000eÓ5\x0005\x0012D.á§\x001e<{vïØtjÅ[Õ°êèU}ÈS1\x001f\x001b\x001f×Lh²,6þ\x000bu4Ë%qññ
½\x0011jí\x001aoÈ\x001cs0>Ì¡ç¿õZRÊ\x001f7vö×#¿\x000f>\x001c\x001f\x001b®OV9ïpl.\x0019\x000bWVdÝE\x000eÓ»$QÑqù9Õ\x0013\x0011N\x001f°÷îÕ@x³Ê1¬dvõó\x00126'Uwå"\x0003ÖyªÂ÷<U\x0011¤©y\x0018&\x000b§|\x001aÇc\x0018¦8o\x00017{¾À®¶ \x001c½ÕY\x0018\x0003ùM6(ÒGF×40}/æ)á\x0012Yeöé\x000e°ïC¢(}²ÄøfqQa§`\x001cSkúG¢Á]©£
H!ò\ ÎÏt¢ª]¨Æì]eØRò'$µ§Ë,áR\x000cK\x001b\x0004¯Fçe
1P\x0014äæ\x0016Ê\x0001V\x0010
tIÆKïÝ»wg\x0003O\x0005ð½Õ_%¼TpÖ®jåìÜÜ\x0002\x000cÈóss³Òc]Ä±÷÷Ê=\x0016T\x0006ÇX%Qâ~#êËq¢-á\x001dÚë%~Ý
A:\x0017â#ËÏb/»°>r¬à\x0011qø{Cµ.Ï\x0014 ìqüñ\x0014)P<\x001e¡ïïxyÒ½7Jìãxâr¶¸¤$\x001cß\x0008ê­o*p\Ñúù7\x0010\x0007Ë#¾,ÏÊÍÍW\x0000%l×Fsön	¾È \D\\x00039cÎç\x0002L¼\x00066j\x000c\x0007²ËÎ\x0010È\x00059&\x0006o\x0002lí\x0006*\x0005\x0015\x001bÙ$D_SBúª^¥&\x0010F·|ìC\x001aÈèUÕ°Lmmm\x0003Ê°'ÝO}\x0006\x0001DºÐÔjÊ{êCÞ%ÌÀTðòBÒ·\x001a\x0008Èð¬\x0006²\x0018ÈÎXèX¯|0¸\x0013úÈå\x0017[ÂÃóQãJeÊ(kC#Ûéb\\x001egB\x0002Iéhj\x0013\x0005ä1h ÊDwÄàç\x0012P\x0005Äë\x0006¤mf"LC¢==?\x0000qoâÓI\x0003Ñ\x0012½\x0007ñíM
Ý\x000fÉÀ»±Z$\x0010\x001c\x0014¬ä«Pc\x0019ÝÕ\x0012PÑ\x0004rÇ\x0003QWM Z@ñ®
¥Ø
\x001aÜK°ûÿN\x0000© .	xA\x0008	MLºl[\x0001~A\x0003J0ü¬n\x0015M¸4NèÚ\x000can\x0002ÈiúÂWAÔ¯2\
²F@\x0010¤\x0004\q&`\x0012\²KÇ?\x0019Èd\x0002Â\x001eV%ÛS8¿\x0001¹-È-\x001aÝqb\x0010F%G*A+	¤T\x0006Rüj\x0002AÌo)ñm\x000c\x0008ä^[.[=T\x0013í\x000bÒ@
Htª±\x000e¤&\x0019LV§ßð\x001cêÑ=§àm@g Ã\x0006½5\x0007M`¨Q\x0002qx#ÚF\x0010@ÎØ\x0011g!¼[xå6ú¶å\x0006\x0015¿è@ O]ìÁ2ì¬\x0003	D¹²\x0010¤NË?UR@Ì\x000fÈ¤c-ïÂ±0|?çTè\x0013at|¿
e@ çÏbÒýV5 \x000b¥ø
#\x0008$#zÝºuSªÖ\x0019Ö\x00042\&?mípTQ6´Æ¨µ\x0006\x0010Ùn¿¡'ÊÁÝäÉ\x0004±\x0004G£rlº
HïÝX\x001bJ\x0003±|¬\x0004÷&Ùq) Ê´]Äáýù6\x0019  DUý\x000fâº
\x0004òv\ï	¯d>\x0005Äo\Y=\x0018|\x0006âó\x0018¼òd,ÆdÇ\x0004\x001apFxU\x000cËê (É@\x000eû}\x0000\x001f'ðj\x0002	)Ç\x001f[C ¤\x001e\x001ak\x0004Â?\x0007òæ±xsrÁaágPË¢ß#Û$Ü\x0015-ÒA'\x0017\x0007\x00064.Í\x001fò½F4\x0010Äç\x001aÑ%Kï6A!\x0010ªtK)Èj«ª¾\x0014Kt@pÒ<ÜèP@z¸ý\x000ep7Ùå
\x0005Dwfr\x0010i)\x0006©\x001d5\x0002Ñ¡TìP=Åo¼
T,\x0015@ 1\x0006K%ØN5üP'Z@ eÏ\x001f>|\x0018­¯\x0011H\x001b1H×µë¢÷øªÖÖ\x0002\x0002s*ñü\x0015$1×3<cy·®óÄW\x00055¼\x0018|\x001c\x001c@\x0003A\x001dÞ!ìkæd§
þ \x000e?MÏ©\x0010dwVUßMÝw@ä¹\x0005\x0000{\x001eÈR\x0001áM,Àe',i Íâ0év¿®}^àEó9\x001aLU(ö4¦k\x0015n\x0000Åº$\x0010FËËÊ²
\x001eê@¸;dø)]\x0008$i§§g³*çT\x001d\x0008s=\x0006d¹b\x0019®XòY òÃS.(ÄKÉk?­\x0002ågfæÊ\x0001ØÆ¥0uö+ä\x0017æ¾¢\x0010\x000e©Û«\x0012ÜA\x0000QüêG\x001c¾1Óì\x0015^ü#íÛ¡ó1ÙYs\x0008$=|a>öÌ©\x0002Xízu]Ä¡°_ãÊÂ¬ÌÌ
\qÆ^\x0013\x0010ö BpÉnt³óxîD.	\x0004á\x000f~\x000f^Oûµ\x001a\x0008£K
¦~ÁÊ4N\x0001\x0014\x0006î\x0019~\x000eHå4­þ¯Àó~Ð×µ8\x000f09U\x0002OrR\x0001AZ?\x0005âûÙ\x0014\x0010&qz¼\x001ew1É aÇ\x0000ù	ÚÛqx\x0004×p)+#Ø.¯8Õ¬
\x0008Û)¸1B\x0003\x0011®®\x0004ÔÁ u ª\x0001\x0008êý\x0004OD
KxÃ³Àã(\x0005\x0004±Ü]®¸ûVA\x0003AB®È@R/Ý¡R,í§qæ¾Põù<\x0010Äde¡â\x0007ñ\x0003ûåcÉ`É)xádT\x0005;¡\x0008)H ÜQã\x0006Z\x001cQÈFpÕÍ®¯\x0018äE\x0010Î+qKEËAr'Ùmò\x001b(Xa¢\x0002B\x0002¶¹
26ÂM<m5Ô\x0000\x0004\x0011®©P&\x000e~6§ÿ}L²Õ\x0002¡0»ßÆd*\x0006ùË­Q	2B$´ÃÂÂFöPy^\x0004b"Ë²e"CíC@¶GMÈ J\x0002~a\x001e\x0008£Õ\x0019d\x0013ÑnÁ*vÁ\x0012¼5@vÒX\x0005\x0004±<\x000c\x001f³ ð¦½}³±k±Ï@n/:\x0010~\x0014Ë=:ÉÏæù2\2_[\x0005\x0004
ÊÅRs5\x0000Ñ\x001a]\x0000N·äÀ\x0005\x0016`¿µÓ\x0004Õþ:&{¶q`÷\x0001ëåÊ[¾,\x0015\x0010Dv\x0016\x0015\x0003eiQ\x0011á`Ï@KK\x0000æ¤§§¿æW\x0003Á,EEQ¶^©xQ ¹\x0013\x001d\x0001>:~\x001e\x0008¢5ü%È\x001eÄ2\x000e2FP=A"ê[\x0005åû\x0002b@\x000cn_$}añ65\x001c3Äv¯\x0014Tf¥¦\x0012Ýl\x0007ô±iÇLo³\v©\x001dZ\x001bð²t>¹Ãú&ÈÂÖ\x0000\x0004á÷¬ÄJÞ½|S)\x000f\x0013«4\x0010´y\x000c\x0002¡,ôåêæd·¬2»Ê\x000bU»tú!#\x000eKñ»´9¶¾©PÎü\x0013 ñRð¼Å\x0010¹ò\x000eÍ\x0015¬ç¨ úK*H ¦qäÃ:WZ³j\x0002AÍæ¾%ÖÁRÇ~1
\x0004mñ\x001bìj\\x000b\x0008£Ík<Åò\x0017µç(ä,4\x0001A¸\x001dcÉÁ]Ùé.ä\x00060û½\x00028\x0016("\x0014\x0012à)äR5	{HtT\x0019?µGä­ç\x001d,jCïe¶\x0019 R3¼úA!Ý¨®
í(\x001a@z>\x0016½EÁ\x001e¢\x0001mUw(¸\x001dG·¨/t8\x0010Ô¼Hä£\x0007\x0003\x0018>kÏÿ\x001a;\^a\x001e\x0012ÜWU«VÓ\x0007¯_Û;öcM}E= oÃv\x000e	éaÂë\x0014\x0012¢Z$Ìë\x001c\x0012"dXô'+$[Ñ8HÔ (è-êKíB=ûÉ-^§\x0015	·Î­í¢G]º®ª³Òî\x0014"ªò\x0005\x001bÔ \x00065¨A\x0004\x000cÔ@X-ÕÂ'!üfb¨¥~°T\x0005t«âô\x0006BCõùZPh¨\x0016'\x0005]Æ²ä\x001c»Î\x0001þí-USÃÆB\x0013:$Ï7\x0016ÒF\x0002Ñvê\x0016è×Ê8\x0006CßD­Y(¢'4¡Í\x0010jäé×·»Ê=Ð\x0015
)ßa(4þËËa·GS\x001ao$X\x0016]­\x0001t²ëJøíÀÞµcÝ©(¼Í6:ÇHãæ¼4zµZ­~^¯þD\x0004³Ó\x0016ªHÔ\x0010È«å¬ø»OoÅLp 1Zm>°ÉÌ\x0018°;z*ßyeBâó¤ë;\x0007	\x0011ã¹\x0007ªZu 6sVô^*Ôn\x001c²óêg\x000fÏ®¤íýèèèÈä¦ÑêèmÍþ*<@é écP­¥trÏdò+&Í¾=Ë÷È¥sìÖ§³ø>\x0002)fÕ\x00152·\x0010ùKÔ\x0016p³Ã²¨"å £x¹\x0000KåÙG{À±%Ñ\x0002Év2T\x0010^\x0002NBH¦Ó\x001eHÈ<²·\í®*«Z-2`]\x0000¤ß8oISþÕãÙ¤;²\x000f\x0000ÅÞ°¼U
Èñù«@Ä üñ-B\x000bMM.eddxe\x000eñ©rB{>ÅåY\x0019\x0019¹2 ÌÜ\x0008kðÌ\x0003%`ª\x0008ßGxyuÖOq\x0000äçlÕÊÆs\x001e\x0010E®LA8we@rÿPl²\x0014_jO4¿%\\:\x0002Þ@á¥8\x0004"þF\x0001
®\x001f8ùV	ò7´ýH\x001c\x001f\x00032¢Y\x001f§ë©\x001ca»È\x0002}<\x001d}5\x0017(?Lì~¢\x001eÉ^8±`õ\x0002Ïý
 oüm\x00080M[ÉÁoú;;;T\x0003yÓÝÙÙcðI	È' üÞ\x000b\x00160Rõ\x001b\x0000\x0019R¿N\x0003iA5\x001coG\x0014±6DZaÉ?87j>ý#(ßfM\x0001ÁegÜª0}(\x0015çýmÍ,Zm/N\x001ef`M4'¸\x000cûl\x0016\x0006¢3-\x0007oõ²0³ñ;'Ãöb@pða¸ÖW\x0003y©6ÚgùfàçÔo?\x0002H
Î´XY\x0002R[3 Û®5j¨	Dç°\x0002¬^IÖê×\x0000r\x0012BøS
ÁsòvÒ\x001e
Þ°a¸OZ\x0002
W\x0008T@Ì7Ê±äJ4Ô4¨\x001duëÁ¡\x0012Õ,\x001aHkl\x001d\x0019a¸R*w7@e2\x000cFþF ÌÏ\x0001!Æxç1å\x000cþ\x0017´~\x0001½|sÀ\x0015Ïª]j@,\x000eÊEt`É*\x0012S¬6@Ò#ÊAr\x000f\x0006Ò:\x0011ÏþágH>\x001d;rFgã\x000fév³¾Ç{£\x0004Ò3·AÅÏF_\x000b¤0~Ç\x001d?	\x0008oI!\x001eg\x0008dÅ\x0012\x0005Æêk\x0004ÂZR\x0008ÎiY%	Uç\x0004¼&Êd¸ü¿ïKßk¼qùø	G\x0008$Í7N!ß×\x0002Â\x000eÊÀýô±½O\x0018.«À6ªFv-/\x0002\x0011\x0000R²jt&x\x001dÄþ: ÔÐþ¼ó \x00132ñ\x001b¦\x0004\x0010ªÀ	U¤¶&\x0010rùHDwj,ÊJ\x001d\x0008©Ã¬V¯p\x0018ú¢N-ø#~­\x0005	¤EÀ\x000b5O\x0002Ñ\x001aÇ«EZ4\x00021Ý¤ÏVÍÞÛ\x001c\x0004\x0015a\x001c\x0008d¡Ý\x001e)vÔÚúë®\x0010iÚÓ§Ow6ù\x0012\x0010æÔlü²\x0010^!T¢ÀÆªY\x0008u hÈ\x001b/òn?%\x001büÞ£Ês#\x0014¾$Ê¬ez¦àÏ»¨v\x000fÌÀ/»@ËJÀ
÷\x0010\x0008w\x0018?Ùü\x000b@\x0011
\x0005\x001d
B\x0010ûX \x0019A\x0001aù%aÅã¾\x000eÈ»AîîîM´¾\x0004Äh\x0004ìÐ@\x0002¶U® :\x0010Á2\%ãÅáª\x0015&\x0010È\x0019?¢
Òô\x0006È\x0019NÏpéÏ-Å~±¡ g\x0014\x0015«6A Ì^¯ñGÝ>y<üS y%à 5vºgöa@Pý%¹ ià«¡Såôú\x001d+!ÎåÏ;U;J¬\x0012Ja§\x001cÔÐªp«\\x0016E]\x000cÏóXé\x001c=
\x0008Â\x001fñ\x000e¼¹]	;Uó h>UÒL_3\x0010VÈ+\x0016H9ÿ\x0006sòÀÍ\x0016\x0008\x0005\x0004q?#U\ÈúÇ BÑJå\x0005\x0007ôÏ°Çg'3§\x0012Zö\x0014¼ïË®\x0005-J\x0005ÙË-à\x0010¥Ù\x0012p×I\x0003A,vb\x0018\x0004¢ÿS!H\x0019\x0005]-N·Ý\x000b(ÿ¾VÒ!Z¦¸Ò\x0019\x001e@t\x0012V\x001an¨\x0002Â\x0019ü\x0002Hå_\x0005$kápB\x001d´?\x0007$wí\x0005+bVbOCµHÇ,5\x001c\x0016ðVY\x0011\x0002HÞ\x0005\x000b\x0016Ì\x000bÑ¶*h³\x00085Ú*.7®\x0005\x0004±ÚP\x000c2\x000fíá7õT!Èe¨0{ÜñS\x0002\x0008ÃíLùbÛ°®\x000bïg.k¤\x0011\x0008gÀ3Lz{I¿î7¥(\x0014gàÚ\x001c
\x0008"Ü\Fxô_\x0003DIhkãÏ\x0001QH\x0014@~[\x0004»u\x00024\x0017\x0016X«êä	 0KIþ!S¿Çà½\x000fyû³½\x0007wÝÑZ@\x0018Í\x000bCöZ¬\x0000¹ëáè\x0006hÏÊ\x0003$\x0010Óý²\x0014Td¤¾+Â°0\x001d@\x0010ÁøW\x0018Vò.5]\x0002ä¿vÝ\x0012
\x0004qOT~\x0015\x0010:¤\x001ecõ9 Ð#ÆÊWzÃ[ÙÅ÷èW\x0003¡ÞquÒaA!£Ï¼å9¬v¯Ô L»Å¯á:) 2\L§\x0002Ø]Q@\x0010®×NòåX üz?j\x001c]\x001b\x0008¢×÷b%9¸ËÛÛì¦U@Ø\x000bÀW\x0000éG-A\x000fmC.jÚ7´£®Z²YO(
ô¶Ò¥ü)ý@ºÊÌúR;BÚë{\éÝ¼V!!Îô\x001aAÛ¾¡­«VW º-&\x001f¸r)2ÌÚ¥×OÔ<"Ã­hh{Aùq×Ïm
²¤ïKýþ¢îtP¿Sh0µcÞ7âÌÕ£;ÑK\x0011[ö§¬µaoQh j0Ö \x00065¨A
ú\x0012Â%ê¸f¦zä\x0006OHúÌZ&D¢1\x001dãf\x001a¨\x000c\x000bÏÄL \x001aÄ;tìåëeB=´f1Ð\x0012Â\x001c<3JBr¨ÄwéÞ£M£:þ\x0010âÆÈÈÈ=Û~\x000e± ï\x0015¹c,yúí7GNf LïõDâeCÈ\x0010²ù´È5vôËy:­\x001cN8×cVì?\Ý>\x001cü²ü6G\x000e _×ÓvóÁDÎ6z\x0013,\x001bÏMxt}G¡æÔ\x0011I¿Kú&Òâq¤#\x0014Vc!a0\x0001dé{ápÌé\x0012þ±-½Às\\x0016\x001e\x0005Ã3¼!×È÷5+Ó÷Áµ÷yEøZè:hýPm'\ñ´\x0017?L\x000b1$_L#±Àø³­©\x0003\x0012Ò[\x0017\x001f\x0014Õ:¤ÿ(\x0001%ËØ\x001a0û>S`¹W÷\x001fIãå\x0007í5\x0002Á²._¸p!®+\x001b\x0019Teî\q­L`Wßý&\x0006¯ºZ8ÌÊ\x0004Øk\x0002r¸µÝÚJåms@ì\x001f`²ý¬ML-.\x0005\x0005kµ5\x0001%Ø[XX4â#è~P¾ÓXÐ|ý1ß:ý ª\x0018<sF¶\x000fð\x000c/T\x0003HKÄ¿\x000c{b£\x0011È\x001c¹2lBtÃåØã\x000eHãT\x0013Gñòí\x001cal^·_BD\x0001é¿k¡	HÞ&â@\x0013\x0010þ\x001dP°þµ~\x0007yó\x0018\x0006\x0004ù\x0019`\x0019s44¡nI\x000c2N\öP5ÑtË|ÈS,?D\x0013\x0010û,ðÂWUÏ
¼<JWS\x001f~æÔ©¸@ý\x000b\x0018âN·eilG\x0011½èNö2­	\x0008¦T\x0002p\x0003N\x001bÕ\x0006Ò²\x0018<rSÕ3\x0006¯<b¬\x0001\x00089'+\x0001t»¥\x0004Äàºý\x00191}L{ùè`Oâ7Ô\x0000äÃ³\x000fJ\x000f¼5\x0001qÎ\x0007ÉUëîfâ\x0015Ñ\x0006®\x0010ñý»w¯\x000f"úÖónæ(À»0¦Ô\x0015ÁÉ}}]É¸T0ÆëÃ1Ex\x0002\x0004²Ïçx\x000coçj\x0000b\x001cE;¬Ü8¼x\x001d=§\x0010_\x000f{\x0015Þbl+eeN7iÔÈ~Ý"Ó~Ö½
pÉæ_?ËÿAT§JÉW.¿\x0000#ð2ü\x0000ª²2È(\~ÙD\x0003\x0010&aHP«Ñ\x0019Ý3ÁÛ!\x0008sR\x001e\x001e\x0003³\x0019\x00152øª\x001dõN\x0015Ñ!üw­à?ð÷jtÖ=©\x0003±Ï\x0000o\x0006ñ\x0010Ûy96\x0015¡X!qùYC\x0012Hg>ËeWÝî\x0019 ;Â°»Ú}n£V\x0008\x0012ð
¼îÊDX­ÎbyðoÃA ªXÙB¸ü¶ÕUüc»ÿ
\x0010­Ãôîâ°iÇ
Á{\x0017
Ès·§Ù\x0010HÉá
\x0011\x0011ëÆê©\x0008VH°ÜãóF[÷Xý\x0011@ô¼¶§¥\x001bsO?QÝêB ¤ù³gÏÜ)ÜPøzÃÀ~\x0011éàcÝöT« \x001faÊÌ|9(Æ¦ÈJKd 2ÎìTB.Wk¬\x0002Zn,\x0000âÌ
É?7Â\x001a¬ÄÓó\x0015àídØ=\x0013VF^R\\ü.krT	Êß§\x0015bsu?Û: w¥NU_x=\x0013à¤âùÐâ\x000c|]VVZùë¦Ä5îxªTñ©Æ°´²m0Z»YNý5²p²_ÖéU
­øqäÜü(ªLÙû\fóõ\x0018Nø%Kmëò\x000586o¢6´`vþqñ¬@j¦\x0017ÕkêìÜ¼	ùcåLª¹5\x000b1hêL5¸|&,;>\x0011(O\x001e°M»M_:3À+6 Ê8;Â8SèÜa\x001eºuG-1Ø\x001cÎÿ\x0014Â\x0005Øö×\x0000_nw wp?W\x0003Ãaý·püeéïÏxvþrÎú"V·=÷¬²úrÆú#Ë¯ãã¶\x00065¨A
úÖ\x00177áÏjëéé\x0012öÁdÞÔÕ\x0016µÒ9ZV}Ci\x000f>\x001f7Ì\x0018ALw{iOÞ[#¾ÇoóòÙdö¹¢ß§P÷\x0013cáÜ.Êc\x001am\x0019¦Âò
ÖEø¢zÆ\x0003á\x0004\x001eãÝF6	\x0003Æ:!Æ\x000cá\x001bO²\x000fiÝ#f­³Vûùî_¬âûÑ"ø&ë7m¹7?ÞdÒÖ»­æì¼2aé¥	.}g]=ü­[øï
u÷'>,§Fê\x001a]ì´~rØ1ºÜøIÛ|þ\x0002m×E¡Ë~ë&þ»â\x000e:nè
v\x0006³\x0003c¼V\x000e\1Åô¸h¶Ú\x0015Ä\x001d\x0013á×¨.G@ÿ\x0001YF­æZ´í\x0015ã§\x0017ûÕè ¿U>mÌ\x00051³\x0011­\x0011±ÎKÇ·ô®ë\x0000åïUÓ	·ÖôµÀqVl³«ÛG\x0006ëµÞ1ÒÜý\x000bb¸æ|Xóðø%>u|ÉÏß¬¦½\x0007ôîîïÊë\x0014`Àî1¦6bà\x0017jÍ°	æ üAV\x000cçá>uzí\x0013\x0003úìäµÀ}\x0006Cµ«u 
úX\x001eíëôdÉ¿®\x0016\x000b»~²Î©\x001eß*(O×À¥n
[âwg\x000cÃ}%=e<÷Ó$¿o	&&__µödgõk¢É]\x0017Û\x0012GÇ!®\x0019sêöª°¿]-\x000cfp¬\x0019|\x001d-b¸²uØÈ Cl&É0ÿ±\x000b\x000b±ûô1ëï]Üà\x0003ÎFM\x0004lOÑÑ\x001d´\x0005.¡3\x001cu¢C´»Ï´±uxeÈ¦_®ä{Éê=F
2´ë9ózg¿®1ó:jíúË5öq[üÇÿôlØ+ùÄð<=±×OY¢xáöEà°ûðfÍá:®_Èé°Í9hy¿\x0019ùm-ÿIñF\x001d1c7â´\x000c^ïÒb}ë°uM¬";0\x001dNzkÚdo²|[=Ù\x001eËäxô3sÞÙÍ7ôdèþ½^Ã¢\x0006j=Ö¥éÆm½ÛìéÛ»~Å;¬IÜ9zÎ¶\x0010ý¾÷¢FZ4mã±NkÎ\x0005hÇÅºw¼¼¯½õÎË³k\x0007â¿g	[´rmêÜÂ1L\x0014\x0010~~±µ¥½»k\x001b=F[W®q{g>Ë©«u½tZê¦m\x001b1\x000cÑw\x0004%ÿ§þ!õtæÊiã#Ë¼ë\x0007Ö ¿U\Õðù½¯a5ofmc¯ó\Ý&Û\x001b\x000c×aÖÿ|£¾¥ø;8vÂNµ\x0005è\x000c»ÚOp0½4f:\x0010ÔôÇ\x000cüÎ£¬¨çþ\x000c9Ç ZM9öK=Ø¨\x0015e(0ÒÕ7Aµ­8ËvZãÊ`4\x000bùÂµô\x0017oH¤­©iè¾ûíu;ÏXÙÍ=âäpC×ñ\x001bºº-°(høBûöxXNcï±õè`\x001d\x001f×yë\x0016ÿÃ2Û\x001a=p®Èa|ò²ÙNÁc¢\x000e:·;3×Ûnú³ºÇ\x001e×qìáóº·ÚiåsöÇÖ\x000e3Æ\x001dø­[üÏÙ6!Øk·ßÅVÜ\x0019\x001e«'rý£<Ð±Cýl×N5a;ä2-ÆØ=b$;dW\x0013tÞ/!¾æ_®ô¿,þ¤\x000c\x0003>wÙBáÞvÝwyð^`-Ø×«±1«Ç¶Ö¨aÌpÛ+Aì[\õVÍ23<æÓ¨n?©þõjr*\x001czç®'}\x0018ÞwB¶$\x0004xï_2Âñº_¯&s×\x001a!½Î4y]$¶¯£wô¢aÎ]ý;~ë\x0016ÿ³
<vÊpÙ'D	[Gÿ&êûàPKíØ\x0015znQîªÅ\x000e÷®¹ZØï8ôÑ>\x0007½«\x001f\x0016Ôõ¿Sÿú?îúÇ
endstream
endobj
171 0 obj
<</Type/Font/Subtype/Type0/BaseFont/ArialMT/Encoding/Identity-H/DescendantFonts 172 0 R/ToUnicode 404 0 R>>
endobj
172 0 obj
[ 173 0 R] 
endobj
173 0 obj
<</BaseFont/ArialMT/Subtype/CIDFontType2/Type/Font/CIDToGIDMap/Identity/DW 1000/CIDSystemInfo 174 0 R/FontDescriptor 175 0 R/W 406 0 R>>
endobj
174 0 obj
<</Ordering(Identity) /Registry(Adobe) /Supplement 0>>
endobj
175 0 obj
<</Type/FontDescriptor/FontName/ArialMT/Flags 32/ItalicAngle 0/Ascent 905/Descent -210/CapHeight 728/AvgWidth 441/MaxWidth 2665/FontWeight 400/XHeight 250/Leading 33/StemV 44/FontBBox[ -665 -210 2000 728] /FontFile2 405 0 R>>
endobj
176 0 obj
<</Title(þÿ\x0000P\x0000r\x0000é\x0000s\x0000e\x0000n\x0000t\x0000a\x0000t\x0000i\x0000o\x0000n\x0000 \x0000P\x0000o\x0000w\x0000e\x0000r\x0000P\x0000o\x0000i\x0000n\x0000t) /Author(Deprez Laurent) /CreationDate(D:20210914120435+02'00') /ModDate(D:20210914120435+02'00') /Producer(þÿ\x0000M\x0000i\x0000c\x0000r\x0000o\x0000s\x0000o\x0000f\x0000t\x0000®\x0000 \x0000P\x0000o\x0000w\x0000e\x0000r\x0000P\x0000o\x0000i\x0000n\x0000t\x0000®\x0000 \x00002\x00000\x00001\x00003) /Creator(þÿ\x0000M\x0000i\x0000c\x0000r\x0000o\x0000s\x0000o\x0000f\x0000t\x0000®\x0000 \x0000P\x0000o\x0000w\x0000e\x0000r\x0000P\x0000o\x0000i\x0000n\x0000t\x0000®\x0000 \x00002\x00000\x00001\x00003) >>
endobj
183 0 obj
<</Type/ObjStm/N 220/First 2020/Filter/FlateDecode/Length 3077>>
stream
x¥[]ä4\x0016}Gâ?ä\x001ftìëO	!-\x000bhY\x0006\x0018Í ñö¡©\x001dzéFM\x0004ÿ~ÏqÝT®ØN%\x000fÝ¾øÜ{}¿ØIf\x0018\x0007Üà-\x001a?1£
	øKq°VÐæÁ&vK\x0008ûdÜÏfp9¡Á{Ö\x000føì\x0010Ð\x000f}¢hã\x0010É\x001b}\x0003¿<Áã=xè;\x001a\x0008ÃE3Æ\x0011\x001b\x0011\x000f\x0002Ý)×g½\x0000#\x0019Ù\x0019%Z\x0010\x0010ál\x0000\x0001Ù\x000eJY\x0003Þ\x0001\x001fÏa\x0018ð	Ö\x0001Z\x0001EO\x0002ðdÙC÷ì8fvæ K\x001fªB\x0011ò2:\x0017^öh ôÃ/kx}x»Ø\x0007\x0004þÂU[øÌ>\x0018vð@	nGèk\x0005ðÈ±ÃÂ6±£àv¢ª4D\x0016 \x0004,rfç8È\x0018<Ù\x000f\x0002\x0003oLÂ}\x0007çX\x0007f\x0000KøC\x001aÐ@\x001cLb\x0005\x0011rn\x0010O®Ö g\x0007\x0011Î´\x000e\x000cÓÈÎààNëév\x000e\x000e·%G\x000eÅ\x000en28\x0010´\x0018<\x0004	0÷£\x001f,\x000c
ç@
ØÑ	Uõ	\x0004Uï£ª\x0001ä¨*Ä8ïhqp\x0001Î·\x0001\x000cC\x0008ØEZ\x0002¼\¤,\x0007"1$B\x001cüH\x000c"Ñãà
-\x0016
\x0008ÄE x*e#U\x0010\x000e6z\x0010\x0011ýþàã\x0018ìçq	\x0004\x0018\x0006\x0006\x001bFë\x0003mØ÷\x0011Ö²\x0010ã#G?à\x00108
\x0004ÃéTÂ\x0006I\x0014FÆ\x000e¼\x0018L,þ\x001ceØ@L°\x001d 
 cZ c^À\x001fÁÓL(\x000fí\x0018U!0djÒ1¶\x0010á+ä
	Y\x0000\x0001\x0001k	x\x000c\x000bò,d\x0018@hq,ªz\x0010`&pp¤Y\x0010MC¬\x0012x+
f\x0011¤\x0015$X\x0006Ú\x0010=ã\x000b¹\x0013=Ô\x0014(\x0017gèOÄ}Z6FJÇ°cB\x000b(&ä  Ñà7ÈB¢Åy\x000b\x0005a\x0007\x0005QLQU@`¤DKÂè\x0006I\x0012cÙ£z8Þ
Cò(\x0003\x0002;&\x001f\x0008\x0007`\x0019æà\x0013b	ü!Ed\x0012ëU0 ¿Rb\x0008#Üá%À\x0011L)#\x001c\x0004ÝÇL>q@\x0017vF©b5\x0012äWfä
Äd±%\Ì\x0002çeOUM¨gàAff7lÈÑ°3\x0018Fº\x0000Á\x0013t\x0011ø,C!¤\x001dª`fJ±\x0004#\x0007Æb
"39Y\x001aKv:R	Ò2ôö,Ø\x000eAI.ð\x0019\x001d\x000c|\x0006åY¬\x0003ù!Ê@QF ë\x00029GÈ@ÎÎcÑ\x001fS$¢L\x0005ô~ çy
üÀ×\x0012)D ¯1,Ì$cX
Åó.³A"«·£_Q h\x0000¤1ÖAe^#ç@\x001bp16Hä\x0017iH~V\x0004OP´p"çL\x0013Ã"\x0006\x0013\x0007ïzRÁ	\x000c%ü\x0012)ü\x0016¸\x0015ê±\x0016b,Æ2)\x0004v\x0000\x0015x
m±Z&\x0017xK¼#ü\x000cJ\x0012ùER\x000cÐL*RHiL=ÎF øcC\x0002â\x000eµ\x0017N£\x0014gËt\x0003*pÉb\x0015âu\x000ceTbÑ¢Q`Yv8Ç±¢	ç?Wª3§fGÏ)(Ç¤E\x0004\x0018çacAµ1%ë³Ïn^9{\x001c^Ý¼¾yýûíýÍý~¸yýôøñÍÓWï\x000f\x001fn^¾\x001b¤Üÿv\x0018?ÿüÓOa¾¾{÷ññpúöçÁüg8¯\x0002Ú­@Ù
tËÀ¤ÀK\x0018ß\x0016öãáÏ§_\x001eþ\4\x000cb\x0006\x0016ñ\x0008\x000eõÅû»·Ëf-Ïe¯ÊÙ±õÚ\x0006m£¶©*%÷<nÍ¥Ëój\x001fÑ3¤k\x0019ÒV@k,ýyU\x0006ÝÙt~32lFÆE$©\x001b~IÛýÂÇö_øÜÞ÷Hu
©¾%Õ{ÄØØ\x0014[KUbÓ®Ø7KyWúýðÅ¿_ÝüðËÿðh[¸t:åÅN/ËûÔQ\x0017w÷¿-\x000eÁ4\x001cfÆ.º\x0004YyÛc\x0008Õ³k
\x0019WXC¤jÐ\x001dOnXÃwÑQ­±/,TÏ¾5Ü\x001ak¤5l76l#6l76¬ÆÝ\x0019\x001b¶\x0016\x001bëæê¬su\x0016muÎÎ:Wg«sÒ6\x001fÕ\x001eGm¶¢­×V=j£ýÞ?\x001a¨b¼)ªºüÏ þä*âº\x000f|\x001b²\x0019é6#ý2RÓZØ\x0002\x001d\x001d[³Ã1?Ë\x0002Ñ9\x0012K\x000f-éiôXºÂÄ¹¢o^5oQØ+\x0014î&1g³Me{1ßTVvY×,gÍzÆÕÊc}IÚjý\x0011­?¢õJ´üÖ-Q(N\x0014ç´¿ÓþÎÕGæznË3¨ÿj*âú/ª×#e3ÒmFúe¤_S·ªâZaêgÎ¬2è:3ÎT]S¯¶©\x001aW¨Ú­WÛ\x0007if!\x001bÆÖ(M%\;¨^¨¶\x00134IÝe$³=èÍö¨7Ëa¿¦Ø9-ZNÓ¢åµØyµ×âåµØy}\x0008ó÷÷\x000f\x000fÚ?èT\x001d|Ý¾a
ýj(ÙËâw\x0002õ­ë\x0017¿ë²\x0019é6#ý226W¦BG\+iâÜÏ¥6ëXÜ#56¤63Ó\x001e©¹.uor\x0007Ù
ùyõLíÇ®^¼·d×0ÍrÆ¬©DA_÷V¨\x0015$j\x0005Z¢V¨\x0015%j\x0005Zât	YUv%«#KÝIÌ_V´þ±ËWÄõ+ÏõHÙtËÈÜ6ß\x0011×
¶<\x000f¶\x001a®KÂLÕæ\x0002hÜ£jX¡jÝ´i32ï5Ï¬ppÓoMáØ` \x0019Í.\x0003å_S8tOÈ¦©\x0000h\x0001ÉZ\x0008t}Jã¸&8¶ú\x0008£ëSV×§¬®O©±Ê©ÚÈä´Î_uC¸(\x001cgP¿p¸~á¸\x001e)n\x0019iÑæ;âZÁ6_Í®2èº$ÌT]³FµMU·BÕ~á¸\x001e÷g^8Ló¹ÊôÂµi ¼Ë@f9àW\x0014\x000e9n¥³?Ç6j´ÕB \x000bÏ¢{1\x001a,åÏ±U¼îN¨±Ê©êÈN{\x0003U7ÄËÂq\x0002õ\x000bG¬ë\x0017ë²\x0019é6#}\x0005Ù\=
\x001dq­0¹31æ\x001esÜ#ÕÖ¥®°RªèÛ|#Ì{ôõ»ô·«Ðn¶ÌV§EÚE«\x0017ðÍqæê8×T\x001eÝ¹\x0013«\x0015Èj%Ñ¥g±ZIìTI´\x0012éÒ³è³:²\x001cÜ;¶Twë1\x000bË,gT·ôg/Wk v;T¶CÝv¨¯A!\x0017z\x0002[!çf!WçÐwêy­Yü³1Û´õv¶Ý§=\x0003?¿øöÉnè6\x001aö
ÕT¢M!Ñ½%qZ\x0010\x0016\x0004§\x0005EwyþöØjAÑå]rÎöØ*^we¾gp16z¾ð»UgT¿xS\x0011Ø¯$\x001b ²\x001dê*ÐÐ\x000c;ß\x0013Øº0º*¾gf/A¡Y¼â.mó\x001am»\x000f2[ y\x0019º&»t3CtsHNÛº©!º©¡n.gÅ­f.aJ4ÑGÛóÕQÌß³(¶\x000bÊ:"\x0017dµ|\x0015çUåÐOÁ\x000bh3¼d\x0013ÊmBù]æÑ ÐufIf¹ÂvhÜ\x000eMÛ¡¹\x0007í\x0007ò|jN«N^H;\x001dl{ñÅÃÛ¿óêsh^\x0012_|³èáÜòèi5¼.·\x0016Ê]¹ÒëºrkÉÐë\x001brOîy±Õ,ÐÅUUsO~é2®Ì? ¸´FswÑìJð\x001cë×Ì\x001aºA¥%º|çsl§©©öÓo\x001cD¿q\x0010]ÏVËOc]Òg&ýÇÇÃáÕÃÃÓÍ«÷ïn/\x001fÞPÓ·ûr»|Sòïçé\x001bé|èt¤j:m0íõMK÷ÓJÜôv<=×N\x0013ðdY*y÷=lüíá/Uu¿~÷\x000fOïùï«û·ç\x001f?^\x001fÞ<Ýüëpûöðx¤èoîßßÝ\x001f^ÿzËQóÂ?îÁáöéîá^?>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ViÖ/ßN\x0000µ\x0014æd_oCA 	pSi1°fO¦KÖ\x0006Þ(0\x0011iûf¹íØ:Oo	ª`ùäæÛÓÎ\x0011pP@åå¹Í\x001cMEpåÀz\x0013ËÄx4§U7)ó¥-üðØ$*Ã\x00199| ×¸\x0012}åK\x001c"¢DDÀ£©©\x0018àßdÓ^\x0019¬ÐQý0@\x0004Â\x001aØ¬ÏOÇ2I«ËË1wuE\x00119Qü²®2Wå)\x001cM^p\Q;OXÍfÓÙ\x0008	\x0013ã\x0016¦itxºT\x0011ø1[f7­\x001a0\x0001°}¹ ¢GÁx¥¦í\x0019¸Õ \x001f¥)\x0001dÓ\x0008F±¼hS?\x001e·I²mêÌ\x0014%»¨«ÄÒ½·©ñx\x0008d^©±õd<rÇðj'Es>\x0016¢'Íù\x0010(\x0001j\x000b«fÁ*mFå\x0011|§É"\x001dRÝîbÇP5$$)ëîUÛ«\x0013Z(ru\x001a±Ò.²l\x000bh­<=VÈÉ\x0008·æ\x0010bK(Ä.oØeÎ{Û¶)#[yàmT[Ï¦\x0004¯Ãò\x001dCzyn\x000c¾ÈÕt/ßæ®ª"" 0ÕaØ\x001f"U2Rð\x0011¾¦ù@DáÙ!°VfÅáñ¸qu+kÏu¤ÉàyÛÀÐLÇñ"°ûN´mÛm\x0004ñÀñZ¸;¶eä:¶Æ. ús\x001e8FÄù¦i`¡RÑ¨A}\x0018Ð\x0012r
«DDû­ÚC\x0011XÄ~Ú¾øë\x0001®¨FcnI%,÷Û\x000c4a$·l\x000e©NÏg+Áp\7HÔ+HbÏ²ý8vUArºÎ\x001dÍvÍ.Ô`q­êÒ×õ\x0000\x001e\x0005\x000fì\x0017\x0015[Ù¶®rÏ\x0004·\x000f1¡ÚÙ¡.\x0003X$]°\x0014\x0019\x0004#\x0005;\x000b\x001d]\x0012\x0004´B>\x000c\x0011-
-ûÃ\x0005ïõ>Ò%-Øìwyä\x00182ÇÉ\x001eL\x001fXWÆ}[E}È,Y¶í¾L|p47\x0012Ñ¬$¯¥Rg\x0010\x0011(U=!Á\x0014OQ¼\x0019\x0017y PsiÃð,\x0019EÞcmCIqz\x0004ñ¡hnZ$"i~VÄ¶ª:\x0010\x0004¦jøi\x0004~¦!\x0004AA¾±\x001c\x0007Â(ºmÚ
²éÆi\x000cü\x000b,§zÙ&<×µ\x0015z6ì\x000fç,ô#u$C \x0004Ø$Q¹Ò
\x0013A£N\x0004\x001aÇ `5<StìE\x0003íx1\x0010\x0004;@v»^(ÓÓLS9r¹¤\x0004Ý¶4È\x0013ÇÓ\x0015+*WI\x001cyÍÅ$­\x0016h·É²4ã)øR¬ ZðçeÃ¶Tx+H5 üQu\x0003Ü¨Yh1âà¯­K\x001cËK`S!!\x0003% f)ÈMhxHUa£÷"\x0018\x0018ü\x001d~)\x0002½"(Q·LÁÉÈd:¡B	FÒM\x0013 [·ÀÈ\x0012ò5È5gA`b²\Ó\x000cMBr<¯h\x00162=Èi\x001dR4M­\x0016xïuAk$ g\x001eC¾Ç m>HZYz
Y!\x0005Ñ%Í2\x0014±X¬p5¹¦Öä:f
\x000ec`\x0005Ù$\x0017×\x0006 Ùõr6.À\x0014Ëà\x001a} é\x001e-&ã)\x0002Ùùt
}cõ\x0002méÂ×Ã$\x0016º³Fí¡\x0007oÊ¹`2@ú\x000fëÑxØïu7úÃñ\x0014ïä\x000e\x0006èWW`o¿\x00012µ|vTú\x001df2\x001eOÐSãÑxòv9Kt/Ñ\x0003èÞìZ\x0007-®6G\x0003l³k\x0016mi`\x001c0·!¢zíQ\x001fzÍ
¯}û\x0008@\x0017ý>~\x0018wóæ=*,\x001a|P
ð~¿wú¨¦Û¨ë´n;\x000e ý\x000eÒ=®p}¿wýÛ¿Â»ê\x000eß«Ã\õ«ðÞìµGï\x0002Ãk?ÞZë@ý\x000fýyï(úÙ¿\x0006üâ?èNï×\x001f«>Ã¾ÞÿEy{ì§_þÒì>½ÄWì½ÜË½ü\x0014¬&ütb~­ù¯Á&ñ³\x0015ëkÍuíù/e\x0002ËÜËåüÇ\x0018æk
¾ß¬9üKå7ÎX<ü©enQâV?¤9]È¾n­£k¥nK\x0003þ­4¹¿PÈ\x001eþü\x0018\x0006¹u/°ø\x001f6Ð»\x001aÿmk\x001d]+ºDÝ¶øï\x0014tàâÏÏX< `\x001f Ã_0ñÐ\x001f¯¤ Ü%\x001a9þ\x0008\x0002rÛ2VI¼m\x0006I?!Zq«äðoî\x0005·£]Ò7%ù]Fe0^Ð<GÎ\x001f4ñ\x0016\x0006\x0013RMêciÑhÏù# $oxº?&\x0004ÓÑðÖÇÏ4÷^ïKÓ\x001fúò#°[^ÿüñVÿ·V%HÜ(Å²djö*5#A\x001aý\x0018CÂEéñdÉ"\x0005~
câ\x0015òq\x0019\x0018\x0002OZÚ÷.\x0003|\x0007¸¦.½áB\x0008\x000eÇÇ\x0013\x0007]ôkhjôÞWÍ}ZD\x0018Ô4ü\x001a¾VC\x001eõ\x0013`'¿vöM\x001f½7~Û@[RAûÊzUè%\x0004éÉt±Z¯!OÆ4É\x0019ñ&÷$r!\x0004ÎA]½\x001fdí\x0015-ZÅéRyìì\x0003\x0000ÏÁó«Ó!Ò8jµAjº E'§C,~cà\x00082Ùù\x0012	è$¹ZLÇ9JñÅ\x001cÚ^À#¨ö\x0003¸\x0002á\x0012)ãÐÙñ\x0014\x001e\x0011ÍÙ­)x÷Éxw{lKW$\x0017ðFXð¦Id%MW\x0005\x0013DQ\x0010øðØ\x00166¿/H\x000cañTÂ\x0013kFr²fEûËóÁã\x0016S¤i#\x00009C2õ\x0003RV«ó±ð\x000cM\x0011ib¶ y\x0015FÄ\x001c^\x0017\x0003yæmGUM\x0011( EÍÐDfy£åá±E\x000c^h/â%x`I²xa\x001a½Ù\Í~åÏ~9 ÐerüöRÇ\x001aGÃË#=ÚÒ%WÝ$]Ã°lS7üòüý¹
\x0015\x0002iÂ=¼3ÆÃVl?öå¥öù\x0015ÉÊ:2aÀ\C\x000e\x0011ÉGÕÓyaè\x0019\x0002E	\x001fXÂjA0Wñ[æ®»çGIìª\x001c+;I8¤\x0018.24¯ ý\x0015(Ó$-£S\x001c-\x0018opÄ»M<÷n%Ôòóÿ|obC\x000c/\x000c}h%rTÅvÍ¡\x0002$\x0003Áþù_\x000e¡&"Hà\x0007QìkÔtªPj\x0017YV\x001e¿}k\x0002©Ó´\x0011Àë\x0004ûþñ\x000eÏO<ÉÊ2±eIÊ2Ò\x00187<¬¹Ç!«n^\x001dÊ,Ýì«§\x0002d×T©­®o«bañ\x0017`áBcfRæ®,¨Am\x0002!H	#W"Ç7F*àÖôñûÓÎWe#,Ê,\x000cÓ²-U\x000fv§sSfg([>}¿.¢§Ø$a'.Áu¢_îË$L\x000fÏ/M¨ÊV¼)\x0012,¥;Ü|Õ:ïðtÞÅA²Å"×íÆ$3.:Í=\x000fL+ªÎU\x0014Õ±ÎLY\x000b«ÇãÆ3,×³4Íy\x0015ç¯ÀsÕ	ï.HÎ¦ÞÃçÑcX:y\x001b·Ø[#áBÚçSfJW6õ&
³};²deíÓ¥)#Sd8=;=·!©Á¶©\x0008IÖ±º\x001aõúµ×Ü5½òüÜD\x0019í*\x000b£Mµ\x000b%t\x0005OË1w\x000c'oÚm`:Eû¸óu#êÄo\x0000&\x001dUó>òÂíñ@§<=îB\x000e®ZIÕ\x00020Æ@ë\x0015X\x0002Ð\x0012\x0001Ø\x001ebMÐâú\x00086¡ñºÓñK_¼5RAn=8ëHáÕ\x0008)K¢l·Ë,¼ýÓ·K\x0015©4AJQs®\x0002EÐÓör,(ßíPÔG\x0012ÔîXE\x00045OuâxÓ¥ÝÄq±ß\x0012ñJ\x0004W\x0005-:ªÈr²ö±
-\x000c,b$~Ç¤æ«YYsÚ:\x0002\x0007/vª3Ï¶4Yq°J\x001e'èÂ\x0017 $\x0002\x0011u¬òXQ\x0005%a,¨\x0003\x0011Ë[C6ìÖ\x001f\x000fÄiÉñåR¥Qe¾J¯\x0018£xüþ­\x0015r>í=I[/ç]\x0012&YêÄ¨?ñPSù\x0012«DÍ¥NÜpÕ´ñù¼á\x0008d°²oYI
|8Áþ]üÖTx\x0016Æ$"`ëp\x0014ïÀÐØ%¾)ó»ÃÀèG +ö;\x0011`3¬®:~lq7¸Dû\x001e\x001dâà´ôôí©]Ç±5nµX+Iûíû)Ó¨ùï>\x0001\x0011çoç] Hyé
æÂG"R\x000fxÕ´eìM;«@dD'êØ¼\x0012ñ\x0001´²Í±IuA\x0017B\x000f)-mÎí62\x0005wvÏo*ùg "bÓ"_\x0001¼<V\x001bU\x0000-\x0010Ô~ûTï;\x0011Xi>05âöù¼\x000bMM¸õrI)Q\x0005s\x0003:F¬\x0004x*\x0005\x0003|Åcé\x001bª¥ÅÞk¸¤\x0008ZÒ^Ä
¶ç\x0017\x0008\x001attw9FG\x001b\x0000ÑÍ<üÙBÃÄDØþ;cxkÓvï\x000e\x001f²K÷öçs\x0018\x001cÉós»_øÃÖæØæ¶jfíù\x0010;Áî¡, S·³Ðöö\x0004¼j\x0000¾{\x001fHI7Â²½<5	ZºèPÒ¢ú|Ú\x0006"¾êõ4\x001a­Ùù	 \x000ex\x000b8|]\x00169|æ\x001c\x001f^¬/mjjvV70½
Lõ\x0001HS¼
\x001f:3ÐÜCT6§â\x0008¼jÔT\x0012\x0018\x001cJþ	§*:x³\x000b\x001d\x001füÈ\x0001læm\x0007EáÜ­\x0011Uw´\x0000ìR`eCWLUâ(Sì\x00008®Äî¶­Ñ©)·hÚ}â\x001a\x0010\x0001¢=Þh¥"É\x0017ùñ\x0013ø\x0008ðfÛ\x0016éùºÂ¯±\x0016¥\x001a^9p£ò°
Y\x000fÇ} £ãG\x001dP`h\x0001
ñÌR\x0010I)!\x0006è \x0004(\x0007\x000e±éTr\x0000:W`ò\x0017t\x0002\x0001¼j\x0011§ûÇ\x000b:¬\x0004c¨\x0013ÄÛxèòÃí>wUIõ`5(bÏTx\x0015
Çõ¢\x0002Ö*'\x0018É~a·ØíòÈ5$<øÀI°V¶h\x00038;î#]a´ß!M[@ç4ð9ôp¬7qnÊÄxX!\x0018Bçã6\x0018¨Aì(X\x0019¬Ç¦bD»ÃÆá\x0016\x0019¥ÇEb2óÑd%ûÝ6\x000b\x001c\x001dn\x000cL\x0000\x0018\x0011Gd%wSCïÐÊ\x000cK\x0017\x0016ÔtÜ\x001bx@JrÄr\x0015&I\x0008oÉÒ \x001aºf¸q\x0016Û2ÃHV\x0004\x0006D\x0014²
ámà@S(Eû\x000b\x0015Æ\x0010&\x0010i9\x0012\x000b¡yÄ\x0010\x0011¢í*DÄR°ÓM\x001e\x0007è\x0000%\x000e±Á¯qXü\x0006 ¥r\x0014É(^\x000cÑ¬¤ØQ\x001ahô\x001cR³ë!ôÁ`º\x001du\x0001ÈSkV}\x0003&Æ­áÁ¬H£ Î\x0018V|®kÜRØ[\x000fþqÃetvµD¡c©yEq<Ç°k5¯@
ò\x001b|æ\x0016
ü.é\x001aL\x0008xH×5\x001dø4APèä«\x0006ç\x0008kësJ2,S×4d/Ö¢Éìj±@º¶¡!q\x001dr\x0004ISá3"dSÈ\x000b\x000fÆKÃÿ)¥7l`àr±BÀî3a#Kl\S!EÒ\x0004jym\bW¿ÜDú3&ÖL!\x001b%Àk^\x0013óé\x0004e¶(\x0011Æ	1\.Hj½#È¢d}ÝÑê
Æè\x000eEQïr5\Ë)ÎÓ\x001fúã9Ò¸¡Z\x0013(
-»\x001cz4éwPâóî.¿F\x0007w ÃÆ;¾h×ç
8F"ü\x0007`§ÄÓkr
\x0000böÖøbò7x¸êáXÙÆJr§Gã£þï%Hà+ä-á¸ÞHÕÆH¸º\x0002Ð.\x001f®í\x001eB[?E,~O¦×fñ.\x0010j®«»þ×~·»÷kàkoÆ\x00180|m|üwÿG\x0016\x0016_\x0015ïwûÓvÙ\x001bäM\x0006ÿôôµ|\x0000¼	²k\x001f>nÀ}¹ùé»¼ï¸ý	ð­Ãý½û'ÿïñG©ù\x0016È\x0017íú\x000bà\x0007eûSÍïvïWÀwQýF÷r/÷r/÷r/÷r/÷r/÷r/÷r/÷r/÷r/÷r/÷r/÷ò]þ\x000fµ.ºB
endstream
endobj
131 0 obj
<</Type/XObject/Subtype/Image/Width 79/Height 93/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/SMask 132 0 R/Filter/FlateDecode/Length 44>>
stream
xíÁ1\x0001\x0000\x0000\x0000Â õOm\x000b/ \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000¸\x001aV\x0019\x0000\x0001
endstream
endobj
132 0 obj
<</Type/XObject/Subtype/Image/Width 79/Height 93/ColorSpace/DeviceGray/Matte[ 0 0 0] /BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 1643>>
stream
xÝX×BòJ\x00184	¡×P¥4Qé\x0002
\x0002ÒE:4)¾ÿ#]Ê/Kôêì¥\x0017ã7Ì7³³9;û\x001e\x000cÃpp0ìOp\x0008CrÁá\x0010lñ°
\x0010\x0007\x0000ñøBD*I¼Óñv\x0006âñ\x0005B±TN©4:Ùb6¨$'àí\x0012\x0003\x0003%2R­Ó¬\x0017N·ï&\x0010\x000cølj\x0011\x0007
\x000e@í\x0010\x0003\x001b-öK×\x001f\x0008Ç\x0012O¹|!ôå\\x001c	
çpù\x001bbç\x0006³Íáô\ß\x0006£ñt6_ªÖ\x001a­N·Û,Æ.U\x0002\x0014¶\x0018N
¥J­Þ¼!\x0016%Sçb¥Vo¶»ýÁp4LÇzÊ£Cb\x000bÐ(Ã\x001b\x0012K\x0002brõµÑêöÞÞ\x0000çc6/\x0016Ù¸»1HÈá0¯0yÂ\x000f|yE¬·\x001ah
æ\x0010h¹\~~~.¦½bÈ"Cøñ0Ps\x0019ÎV[bÖ8³
ª±\x000b\x0002'Òºî­Á\x0018\x000e´ \x0003má¯É+5\x0016`:ÕE(Wïg\x0000³i/\x0016\x0018ÎéÝ±ç\x0015ÞwpI\x0007U\x000b@ap3ÕÎp:ÿ\x000e\x000f]3#;nÅæ`òÝèZ@Wð%j7­õF\x001fÌxèZ@@+¤ôÎÀc¹õÎL\x0018]íRíú>ß\x00180ã¡k±Æ#¸b¥Ñ\x0015ÉÕ\x0007\x001fßi±\x0001$\x0005r½+VìÆ;A\x0005å6Ó\x001cÍ\x0018á \x0016h\x0019µÁ#xr\x001fÀ1N·ÖBÈg«}VÚCùÎä\x001b-V\x0019\x000cá\©Á÷Xcb¥EÐ®\x0005N4Îh±Ë¨ÄJJÔ¬\x0005 JY\x0003ÙæpÆ8\x001cÔ¢tªøhZ\x0000\x001ddFHuÊ\x0006´\x00185Ó\x001e-¢\x00168)Ö]Ý»4\x001d_Y
µð\x001bÄHp8\x0008Q{è¹µ¿sËÅ\x001c&ýr«E\x0001Q\x000bpÿÈÍþôë¾ªËÅl2\x001a¦ëÔZ~¼\x0001-\x0014(÷\x0005Øsw¢ÒîÆÓrñ1ì6\x001b­þ:V³÷Z\x0002I\x000b¸#H¡½¿#Ù°]Î¦³åæ\x001bU E#¢\x0005 JYï2÷½\x001d\x0001¶ê\x0014\x0013w×·÷¹Z\x0017Äêb>igýú\x001fµ;bð=¼¼íSOú¤Ïf4_ÁX\x0005¹?t\x000b\x0001³ô'-Àh±\x0012Í\x000eÁkÚoQÉäZïþùµ?NúåMñ\x0003\x001c¸hö`f\x0007ðÃµrA»JÄã)ãU(]i\x000f½JÌAñÂ­c)Eßù¸[]iÅ\ \x00052ÝÈ×Û­RÌ¡<
\x0007vD¢sÅË½=;,\x0017Ó·GQ\x0006
,UXevÓÅR&d?>`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=Ë¥b!Iy"ÍÏ}ù ê3\x00128\x0016Ã°|î!IßßÝÞ\__¥øy,\x001a\x000e¡\x001e§Bô\x000e\x0000
ÇâñX4\x0012ÏBÁàéÉ1\x001a\x0008øýG¾C¯÷Àãv9íV£¤'"`\x0017h´¹<\x001ep¬Ëét8ì6Íj±ÍfÉh0\x0018ô\x0008¢Ói5";>¾S\x0015j-¢×Ó\x0007ë´`4\x001a\x001eJIB¡þ\x001f"À*cÃ7\x0003­G\x001a¸bw8v\x000fó\x0017ÇÂ\x001dØ</p><p>endstream</p><p>endobj</p><p>163 0 obj</p><p><</Type/XObject/Subtype/Image/Width 396/Height 306/ColorSpace/DeviceRGB/BitsPerComponent 8/Filter/DCTDecode/Interpolate true/Length 17181>></p><p>stream</p><p>ÿØÿà\x0000\x0010JFIF\x0000\x0001\x0001\x0001\x0000H\x0000H\x0000\x0000ÿá\x0000bExif\x0000\x0000MM\x0000*\x0000\x0000\x0000\x0008\x0000\x0004\x0003\x0002\x0000\x0002\x0000\x0000\x0000\x001c\x0000\x0000\x0000>Q\x0010\x0000\x0001\x0000\x0000\x0000\x0001\x0001\x0000\x0000\x0000Q\x0011\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013Q\x0012\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013\x0000\x0000\x0000\x0000Laptop Internal LCD Monitor\x0000ÿâ\x0004\x001eICC_PROFILE\x0000\x0001\x0001\x0000\x0000\x0004\x000eWin\x0000\x0002\x0010\x0000\x0000mntrRGB XYZ \x0007Ù\x0000\x0005\x0000\x000f\x0000\x000e\x0000\x001e\x0000\x0000acspMSFT\x0000\x0000\x0000\x0000LNV\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000öÖ\x0000\x0001\x0000\x0000\x0000\x0000Ó+LNV \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0011desc\x0000\x0000\x0001P\x0000\x0000\x0000vdmnd\x0000\x0000\x0001È\x0000\x0000\x0000admdd\x0000\x0000\x0001P\x0000\x0000\x0000vvued\x0000\x0000\x0002,\x0000\x0000\x0000view\x0000\x0000\x0002´\x0000\x0000\x0000$lumi\x0000\x0000\x0002Ø\x0000\x0000\x0000\x0014meas\x0000\x0000\x0002ì\x0000\x0000\x0000$rXYZ\x0000\x0000\x0003\x0010\x0000\x0000\x0000\x0014gXYZ\x0000\x0000\x0003$\x0000\x0000\x0000\x0014bXYZ\x0000\x0000\x00038\x0000\x0000\x0000\x0014rTRC\x0000\x0000\x0003L\x0000\x0000\x0000\x001egTRC\x0000\x0000\x0003l\x0000\x0000\x0000\x001ebTRC\x0000\x0000\x0003\x0000\x0000\x0000\x001ewtpt\x0000\x0000\x0003¬\x0000\x0000\x0000\x0014bkpt\x0000\x0000\x0003À\x0000\x0000\x0000\x0014tech\x0000\x0000\x0003Ô\x0000\x0000\x0000\x000ccprt\x0000\x0000\x0003à\x0000\x0000\x0000.desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x001cLaptop Internal LCD Monitor\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ\x0011\x0001\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0007Lenovo\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ \x000c\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000,Reference Viewing Condition in IEC61966-2.1\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x00004\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x00003»@\x0000p\x00064\x0000Í\x0000\x0000\x0000\x0000\x0008\x0000\x0000\x0000ù\x0012\x0000\x0004\x0000\x0000\x0000\x0000ðý$\x0008\x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x00008B\x0000Ê\x000eC\x0000Ù·@\x0000øuB\x0000\x0000\x0000view\x0000\x0000\x0000\x0000\x0000\x0013¤þ\x0000\x0014_.\x0000\x0010Ï\x0014\x0000\x0003íË\x0000\x0004\x0013\x000b\x0000\x0003\\x0000\x0000\x0000\x0001XYZ \x0000\x0000\x0000\x0000\x0000L	V\x0000P\x0000\x0000\x0000W\x001fæmeas\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000\x0002\x0000\x0000\x0000\x0002XYZ \x0000\x0000\x0000\x0000\x0000\x0000\\x000b\x0000\x00002\x0000\x0000\x0008QXYZ \x0000\x0000\x0000\x0000\x0000\x0000t4\x0000\x0000½\x0010\x0000\x0000\x0011eXYZ \x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x0010_\x0000\x0000¹curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x0019\x000c+\x001d;6yVä~\x001c´ëÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002	\x000b»\x001e\x00199</p><p>[Ps¹´ÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x001e\x000bÛ!Þ>(aðaÀèÿÿ\x0000\x0000XYZ \x0000\x0000\x0000\x0000\x0000\x0000óQ\x0000\x0001\x0000\x0000\x0000\x0001\x0016ÌXYZ \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000sig \x0000\x0000\x0000\x0000AMD text\x0000\x0000\x0000\x0000Copyright (c) 2005 Lenovo Corporation\x0000ÿÛ\x0000C\x0000\x0008\x0006\x0006\x0007\x0006\x0005\x0008\x0007\x0007\x0007		\x0008</p><p>\x000c\x0014
\x000c\x000b\x000b\x000c\x0019\x0012\x0013\x000f\x0014\x001d\x001a\x001f\x001e\x001d\x001a\x001c\x001c $.' ",#\x001c\x001c(7),01444\x001f'9=82<.342ÿÛ\x0000C\x0001			\x000c\x000b\x000c\x0018

\x00182!\x001c!22222222222222222222222222222222222222222222222222ÿÀ\x0000\x0011\x0008\x00012\x0001\x0003\x0001"\x0000\x0002\x0011\x0001\x0003\x0011\x0001ÿÄ\x0000\x001f\x0000\x0000\x0001\x0005\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	</p><p>\x000bÿÄ\x0000µ\x0010\x0000\x0002\x0001\x0003\x0003\x0002\x0004\x0003\x0005\x0005\x0004\x0004\x0000\x0000\x0001}\x0001\x0002\x0003\x0000\x0004\x0011\x0005\x0012!1A\x0006\x0013Qa\x0007"q\x00142¡\x0008#B±Á\x0015RÑð$3br	</p><p>\x0016\x0017\x0018\x0019\x001a%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚáâãäåæçèéêñòóôõö÷øùúÿÄ\x0000\x001f\x0001\x0000\x0003\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	</p><p>\x000bÿÄ\x0000µ\x0011\x0000\x0002\x0001\x0002\x0004\x0004\x0003\x0004\x0007\x0005\x0004\x0004\x0000\x0001\x0002w\x0000\x0001\x0002\x0003\x0011\x0004\x0005!1\x0006\x0012AQ\x0007aq\x0013"2\x0008\x0014B¡±Á	#3Rð\x0015brÑ</p><p>\x0016$4á%ñ\x0017\x0018\x0019\x001a&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚâãäåæçèéêòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0001\x0000\x0002\x0011\x0003\x0011\x0000?\x0000÷ú(¢</p><p>(¢</p><p>(¢</p><p>(¢2õ\x0019R(ÁÂ¾w\x000f\cük"°¾/øQðÞ¥\iÏ\x001aÉ5ÃDÞbn\x0018ÛéYS]êÖó42øª\x0011"\x001c0]\x000eV\x0000û\x0010pk¢~óGeEcÙè\x001e+¾´êßÄö&\x0019Wr\x0016Ó\x0019N=Álþ\x0011_\x0018ÿ\x0000ÐÍ§ÿ\x0000à¸ÿ\x0000ñu~Ò!¯cJÍÿ\x0000WÆ?ô3iÿ\x0000ø.?ü]qÞ>Õ|YàHì\x001eMVÆóíê\x0002ÙìÛ´\x000fözÐªEèÝÚ=\x000eðø[\x001e'ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×ªº3öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ)È\x0014È¡ÉU$n#°ï^\x000bÿ\x0000\x000b_Å\x001fóÒÓþüõèÿ\x0000¯âùéiÿ\x0000~?úô\=´O~8#¹Ù\x001c¥¢ÈËzôëEÔpÅ6Ø$2&Ðw\x001f_óð\x001føZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×©ùµô\x0005ÂÃ\x0004¨mgv8ÎãÕ\x001cWB¾5cÜ\x0003_.7Åo\x00142\x0013[)<nX\x0006G¿5ôý©-g\x0001=LjOåYUÙ\x001aSÐ(¬M( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000f!øûÿ\x0000 =\x0013þ¿Oþ^­~&P¢C	`ÀàWü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A®î×L=N;£¯j\x000f\x0018!©Ûå.W;O\x0019ÇãZ^ÑFKã#<¿2p^3ÆZZT\x001byæ&³#vÖ8ïÝÿ\x0000Bÿ\x0000 Îÿ\x0000)þ5jÏTÓõ\x0016u²¾¶¹(\x0001a\x000c¡öç¦qKÈ»\x00153uë/ë^CñàËö=\x0007ÍÝ6|nú%{¥xí
ÿ\x0000\x001eÞ\x001eÿ\x0000®ÿ\x0000$§\x0019]U{ðñN]»q!sÉ\x001d4V§"\x0014i0Ì$R^D®2\x0018\x0016\x0019\x0006·8mwaæßDÏË{!\x001eÿ\x0000þªO³è¿óúÿ\x0000ÿ\x0000Z¾>\x0011ðÖãÿ\x0000\x0012
7¯üû­'ü">\x001bÿ\x0000 \x000eÿ\x0000ëV±qKàAõ	ÿ\x0000ÏÇý|¯RÊ6Ai;H\x0008ù³Úªdzú³þ\x0011\x001f
ÿ\x0000Ð\x0003Nÿ\x0000Àu¥ÿ\x0000;Ã¿ô/éÿ\x0000ø\x000c¿áXÊ²½¬m\x001c+µî|¥ê(Èõ\x0015õið\x0007]\x0003N\x001föî´ðøoþ:wþ\x0003­O´E}]÷>SÈõ\x0014¹\x001eµõ_ü">\x001bÿ\x0000 \x000eÿ\x0000ë\åß´%ñÊÛ®b þËó<±\x0008Û»ÍÆqë)©Ý*
+ÜùÛ#ÔQê+éá\x000f\x0000IÑ4ð\x0007$ù\x000bY§ølIáë\x0012¾JçùSsHJ{\x001f<äz\×Òéá\x000eI\x001aºhyV\x0019\x0007ÈZó¯\x0011é\x001al\x001e%¾\x001b\x000bxãRQc\x0000\x000fRÔUÎ|D½9å´W~të\x0010	6\x00009? ¬Ï·h[\x0016ÉÔù\</p><p>Zû#\x0018§Sàg'Iê+µ´:MìÛDY\x0006y\x000cQ^çáo\x0008ørçÂzLóèZ|Éi\x001b;µºÄ¨É'\x0014*«±Ó­'\x0016¬×så|QFG¨¯¤¼iwàO\x0004ý/<3gq=ÎJE\x0015ªd(êÄ:àU¯\x0007'<i¥=åìbhË\x0019-(ØÏP9\x001eõ^ÓÈêú»ÚçÌy\x001e¢Q_TxÂ>\x001c¶ðåä°èZ|r(\2Û¨#æ\x001eÕq¼\x001dáÇþ)ý7¯üû­/hêîû%äz2=E}W?|/\x000bmÿ\x0000{Mfïþ¼~è<-áyÔáí4\x0011Ô\x001bu®(æ¸Y×xhÏß]?­
\x001e</p><p>¢7Cå<Þöï\x000e¥øNÒm?K´µ¯UKÃ\x0010RFÆã#µxz\x0011wW9§\x000eG`\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Î¯Cl6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ×iÿ\x0000	\x0004V·\x000c?á\x001e×&p\x0002\x0019c´Ü©ÏJâþ>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö½ÇÄ+ë\x000f6þ\x001cm61cÑ§bCá\x001dã¶ÐMo</p><p>rtè"\x0011r¨Ò5"¾Ñ¥8ÿ\x0000á\x0008¿Mì\x0017séH\x0015sÜJê­të\x001b\x0016f´³··.0Æ(3õÀ®)ü©,¬CC*\x000fÜóþålkx³þü\x0018/ÿ\x0000\x0013Y4ÊM\x001d5xí\x0001+I\x000e¦'MN\x0001nÂr+Ôlõ\x001f\x0012Ky\x0014wz\x0004\x0010[³bIVõ\¨õÆ9¯-ý ¿æ	þü¿ÉiÃâ"¯ÀÏ\x0014\x0015¯áoù\x001b´oúýÿ\x0000C\x0015+_Âßò7hßõû\x0017þ+w±Â·>¯o¼~´­÷Ö¹DóOÞ(¿Ó\x0005¤]M
ÜÀË?\x000eÿ\x0000/¢àöÉÏOJòW¸×¤l½Æ¨ÍêZZõÏ\x0019X¼¾=±¿´;\x001b&YW8\x0005;TÙ
Â KÉ_N79vÂã\x0012å0;îÇOÂ¹êb9\x001d¹èað\x001eÚ\x001cÒm|º\x001c×Ã\x001bÝro\x001bÛÛI¨Ü\x0008\x0004nóÃq+\x0011"Ð\x0003ß$\x001fÀ×º×è6ò\x001f\x001fé­Ë\x0005Fµ=ªw"1\x0018\69Ý»½zk	©Æç%j.ÜB¹{Ïù(Kÿ\x0000`ý­]Er÷òPþÁ\x001fûZµç=OÑ<ÈÙ?¼\x0008¬q§­·É|\x0004(Ù</p><p>0\x000e=+VçÌ0â#b\x0001>¹¨VÖ\x0005\x001cD¨­ÒÂ£§J\³ê&2Kmµ8ÚHÛè;Wø£þF­Gýäÿ\x0000Ð\x0016½\x0016\x001bx`ÌA·pÚ@é^uâù\x001aµ\x001f÷ÿ\x0000@\x0014äï\x0003ÊÌg\x0019Ñæs!âYÐÂÇjÉò\x0013è\x000f\x0015ÓøÁZUÆ%ÅÃ%¤Ñ*¤¶ñ\x001eÝ\x0006ÜüÙéYÐh²>-ìÈÄ!x¡B\x0001p;z</p><p>ÔºÙ¨h\x001am¥ÓÞÌ\x001a9fhÛp\x0018\x0016Olð:ñXëÐ¬­Î\x001aq¾W}O?Ó,
­ôÄ®\x0002D¨\x0008þ"y'ô¯£¼\x001fÿ\x0000"fÿ\x0000^qè"¼SSÓ¤Ón\x0004NÁÕ*àc5í~\x0010!|\x0017£@\x0002Ê"Iÿ\x0000tVÜ2êY¹ïdbxFû_ã½\x000f0\x001bu\x0001\x0001Y289?Oàí#û?PÔ®R<Gr±«\x0015\x0001T2\x0016\x0018\x0000\x000fFæ_ñ\x0005µÄ&Þ5\x001eVïõ¬psþÍO¡x\x0015¶Úæ#\x0000^\x0011û\x0011þ×¡¬\x0014\x001fµæ¾²ó,3¤©'¯ÎÞ·/x»þEkï¢ÿ\x0000èb®·ßo­Rñi\x0007Â·¤\x001c«ÿ\x0000\x0002Zºß|ýk§¡=L]J	\x001aõH"ÜàtîjM$\x0014m¦C 	Äç8ïPßÊ·32\x001c4cåÇ­2Úvµ#Ë\x0000'B¸í^T°öqIZW½µ³»6ßÜSÌ(û7\x0017¾ßðN?ãü_õþ¿ú\x0003W×¿|q!¼\x0015bÃ¡¾R?ï¯\x0001¯nÂpWøÀu\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®küªjô/
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5Pñ^³mñ\x000e×IJ´`"_6X	%H\x0007Ì\x000fÓÛÛÖ¨|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­ÛÝgÄ¶~2¶Ú³hyr Ü¥H\x0019mØÎìö®6åÒÙîe\x001a\x0015vní-7$\x0015x°JÊº$D\x0006 \x001f³ÜtÏûµ¯çøÛþ|ô?ûý/øV3ê;óX-[w\x0010\x000fØûgþºÖÇÙ¼mÿ\x0000A-\x0017ÿ\x0000\x0001dÿ\x0000â«\x0016YbÎ_\x0016\x001bÈí®¶Å¿xÑK!p=\x0018Íyoí\x0005×Eÿ\x0000~_äµê6vþ,[Èöÿ\x0000J{`ß¼X­ÝXb[òïÚ\x000b®þü¿ÉhÄ©ð3Å\x0005kø[þFí\x001bþ¿bÿ\x0000ÐÅd</p><p>×ð·üÚ7ý~Åÿ\x0000¡Ýìp­Ï«Ûï\x001f­%+}ãõ¤®cÑ9¯\x0010éXy5\x0018'\x0002EÇëYqhñÉ§Á}hªC@~÷Ó\x001eõÖêöÚmÜ]\x0002Ñ`\x0019.Ojó×%KäT±*¥Fä\x001e®\x000cE5\x0019s.§­ÇF_¸ÒqWé±Ðh:H».äùbÆÕÇÞ#ú</p><p>ë«'@Õ¬õ+C\x001d¬m\x0011\x0000Ñ·aëZÕÕFl>¶1bß´¼z\x0005r:¥½ýÏã[\x000b uÒrÍ4F@GÐ\x0000F+®®|ÿ\x0000ÉDÿ\x0000¸7þ×­á¹Ï%ua£Kñ\x0001\x0018mOMoOô7\x001fû=6=7\eùu].LpJÚ·ôzÇ·w6~\x0015íehÙäHÝàí9È\x001fZæm4y´]*ßWÓüèo¡Ì\x000b\x0012(\x0019`GÒÜT¬ÑQÁB¢ægYý¯vÔ´Ð{\x001f²?ÿ\x0000\x0017\èðF¥«ëw÷êÖ{ãQìµð½ï^\x0014XcF\x0015Ô0ú\x0011­¤ÿ\x0000Çæ¯ÿ\x0000_Cÿ\x0000E%9E(ès¼5&¹ZÐÁo</p><p>k9f:ÆªWiÍ£`\x000fûî³ô_\x0001ÞhöfÏOÖôâ¥~ÌYç\x000fQüaFÐ4û%¬sÜ\x0014áUxü2Gé\7ÃK{/\x001fé²n$7³\x0011Cc­cÌ«	\x0017\x001b¥¡èzõmM#Iµ%Ør¥lÛ?ú\x001dZÒ-|E/lm\x0013SÓÖÜ[¢\x0001öGÝ´\x000c`þÕÙµ ÿ\x0000È¿aÿ\x0000\EkN)Þæ\x0012¡N\x001f</p><p>ßs\x001bþ\x0011Íc?ò\x0011°ÿ\x0000ÀWÿ\x0000âèÿ\x0000sXÿ\x0000 þ\x0002¿ÿ\x0000\x0017[Wv/t\x0012Ká·</p><p>\x0000òX\x000c¹Îsø</p><p>u¼­,^tÓ[à\x0018b\x000bgÃéÅf§\x0007WÙòüÍ\x001e[EQöWìsÚÝ¿l|){\x0019ÔìdT\x001dÙó÷\x0000ïâÚßp7zO=qjãÿ\x0000g­\x0016È©¨ÿ\x0000×1ÿ\x0000¡</p><p>Äo¼~´ë{Hò±uêQå7d@.ü@å¾íÞOþ.µøuKÿ\x0000Ày?øºÁñEö¥5­¼\x0017RZÀ¨ò\x0019#$\x0016¢¯\x001d±çü+\x000e¹¤ø¢;+¶í§\x0016bÈp2\x0008'¡ÿ\x0000\x001açöØÖ\x0018\x001cDð[RV×§bÿ\x0000ÄëýfãÃ\x0016_Ídöét¥\x0016\x0008YX\x001d­Ô<W×«üOÿ\x0000rÛþ¾þÕå\x0015ÛEÞ\x0004aêJ¤/ \x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Uz\x001dømÙ5\x0014QY\x001daE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­{É<imãÛYá\x0013¾<±² \x0019\x000cd\x0000À»³¥d|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­\x000bÝ\x001bÆ©ñ\x0016ÛX¶ºM\x0011|¼C\x001cÜlÚ\x0003!\þ5ÑI¥\x0017vÓÌ¬3ýôõ4^/\x001fù­¶àÜqòAÓ?Z×þÆñGý
Kÿ\x0000ôÿ\x0000\x001aÆ}\x0003Æ¦V+­J\x0010±ÇúZð3ÿ\x0000\k_þ\x0011]Sþý_þùÿ\x0000¬fÏJñ\x000c7Iuâ5¸[/\x0017Ø7LÅyoí\x0005×Eÿ\x0000~_äµê\x0016^\x001dÔ-oa_\x0013êw)\x001be¡Gµý\x00175åÿ\x0000´\x0017]\x0017ýùÑ\x001f\x0013Sàg</p><p>×ð·üÚ7ý~Åÿ\x0000¡È\x0015£ ÜÃeâ-2êáöC
ÔrHØÎ\x00140$Öïcn}jßxýk\x000bÄ¾#Ãöv	n¥Ï\x0016ñãíY\x0012üVðr£ºjF\x0000A\x000bÇÓ8¯2ÔüYi«j\x0012Þ\ßÆdð\x0006p£²:</p><p>æj]\x0011XÜL©ÂÔÛü
-CX¿Õ.¾ÑwpÎãî¯E_`;V\x0015åýÿ\x0000ü$VX\x0002 ¼&xaüDÑýµ¦Ïì_¯øVmÎ§jÚÕ¬és\x00191nxÎsÚ¡BWÕ\x001e-</p><p>u%9Jq¾CªþêÞénmçxe_ºÈqô?\x000bøÐjr¥¢\x0016;¶â9Wúc±¯$þÚÓ?çö/×ü*UÔ­AVY=U7üúP£%Ð0ÓÄaåxÅÛ±ô5sçþJ'ýÁ¿ö½aèß\x0013tc¦Æº­Ì©v+\x0015¶ú7\x000bÖ«\x001eøwþ\x0013?í\x000fµÏö_ìß#Ùdûþnìco¥m\x0004î}"©\x0019EHé<NÚTÐÚYj\x0017°A#ÜG,QÊØó6GÓ¯4_¥µ®¥s9+\x0012ÂUÝyÂtÏ\w¯\x001cñ¶¼!ñ<·ÆSk\x001a¬VäÄãå\x001cç\x0018ã$Wàø­.wg;4×RÅäÇvc!Ñ\x000fÞÏ\x001f1Ç\x0000ûÕÎÚe¬CqG°è¶¬éÜém×÷}0ÊGb;\x001aIÿ\x0000Í_þ¾þJðO	xçÂÚ¸¸A$án!\x0008ß2ú>ðí^gñ\x001fÃV²j2ÍæDeo\x001eZîñÈ"E¦ªÝ³{Æ¶zmç¤[÷Xä_Ùñ\x0012v\x0000wÏCí\·ÃÈ´û­RkÛ«;k]@\x0000¶öñ.\x0011@ûÌ¹'æ&¸½OÄ¿ÚúÞ]\9v?*ùoÇ`8àVN}\x0015½¸\x0006Icu~GÈÉÈ â¹\[w±ç¼Ï\x0010¯É\x000fvë½úßô>\x001dk\x0013Aÿ\x0000~Ãþ¸ä¼7ñ?MK\x001f'[ºM\x0019ÂL-äo1}ð½GëTåø¦ÙxF+}6I¤ÔB5
nàF{¶Hç\x0015ÓE;~Ö5"¤´;=WÆ\x001a/ïíl5+è!ì)Â®\x0007W=\x0014\x001eÙëOÑ|S¤ø¥.eÒ®u¶Äø\x0004r;õSØ×ÎZ±:×æ\O"Ë£fõÉ\x001djÆ©\x000eKi­.~Ç4J6à2ýGNEv}Z5Ôµ·È·?wçÐ\x001e,ÿ\x0000SQÿ\x0000®cÿ\x0000B\x0015ßxýk\x0016ûânªx:x..Ö-FX´+\x001b\x0015,\x0018r\x000e:\x001cf®hþ8ðbÜ5Íîµ\x0012ÎR6þcê~Zóñ\x0011nI#ÊÅÑZK\x001aFÙaàyrÌ\x000bDáw8ê\x0007½Gg\x001cR	&\x0017x)\x0019;\x000f\{uük\x001fÆþ1ðî«u£\èÚÕ¤weÌ\x0017&\x0016Ìp°\x0019'+Î\x0008àsÉ®«OñÏÃm*\x0007ÏV¶J\x0000¼©7J@ÆXíäóÖ¹ýçæ=9B?QXHÔ{ß¥½>ýN\x0003âüßõô?ô\x0016¯(¯Føâ\x001d\x0017UÓ\x0012ÓK¿[£\x001dÖàU\x0018epFy\x001eâ¼æºè¦£fy¸h¸Ó³\x0001Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍ|T:¨¯µlÿ\x0000ãÊßþ¹¯ò¥W¡èa·dÔQEdu\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001eCñ÷þ@z'ý~ý\x0006µï|9®\x001f\x001eÚë6ñÉ\x0008\x0011¸¶óö¸@\x0000eÛÓoSZÈøûÿ\x0000 =\x0013þ¿OþW/¼ òüKµÖíõËOµb)ÆIvË \x0010?ÙÆN1ë]4dã\x0017gm\x001fKªjuuW³^£ø3Ä
+0×e</p><p>X}®n\x0006kcþ\x0010¸qÎ·®ÿ\x0000àsa?"iY·\x0010\x0005Æ$õÿ\x0000®µ¯ÿ\x0000\x0008W=fÿ\x0000Àù?øªÅ³K\x0017lü+\x0015äW+«k\x0012ÛpI¯\x000b#}F9\x0015å?\x001fÜ´=\x0015ß\x001f­z<?e}
Í±Ï·&o$a¡l\x001aòÏßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¢?\x00115>\x0006xÐ¥¤\x0014µÐp0¢(\x0010QE\x0014\x0000÷\x001bé_^é·Ö\x001aW4ÛýBh­íb±É,\x0017(£Ä×ÈM÷\x001bé_UßZÛ_|+¶µ»³ò	lmÕà·m®Ã	Ðþ¿D¹n¹¶:pýMHüYáÉ´íXµ+g°ó|=A+¿®:Vµ¬¶×±\Û\x0019T:8\x001c0=
yÍ¥\x001eºChÇHfÜÜ\x001fîÚ\x000b`\x0002s÷À­í+ÄÑZéÿ\x0000dF½mG\x0014,\x000b3Ú08äß¥sÏøáéÜô?uìüý{Xë|´þâþTyiýÅü«ÿ\x0000á~Îîl²H\x0005c|¯\\x0013»\x001d\x0007\x0019ã½uä\x0003ëAZq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*ð\x000f \x000f\x0013é \x0000?Ð§ûæ¾¯¾?ÈÑ¤ÿ\x0000×ÿ\x0000ÐÍ]?Æ¿Ày-\x0014Q]\x0007\x0008QE\x0014\x0000QE\x0014\x0000\x000e£ê+í[?øò·ÿ\x0000®kü«â¡Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍcW¡ÓÝQE\x0015Ö\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000y\x000fÇßù\x0001èõúô\x001a½}á]2oÖº¤:ü1jÅ0²s¸(\x001c\x001cú\x000f»T~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö£§ømü}hßÛ/m­9ü\x001eäÞ\x0000Ç=\x0003¡5ÕEµ\x0017fö{\x0018{IB­ãmÖû</p><p>þ\x0010ð¡µë\x0000K\x0012Aò=zVÇö'Ãßîhÿ\x0000÷ýøªÇÏÀ\x001es×Ð6âXy±õÏ#îV·ö§Ãùë¡ß´ÿ\x0000</p><p>ÁÜÔ·§é>	P]=4±x­¼©¶ïaó/ßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¯LÓµ\x001f\x0003K¨Á\x001e&o\x0019±\x0008\x0010>ïl\x000eµæ\x001f¿ãçKÿ\x0000yÿ\x0000ô\x0011N?\x0011\x0015>\x0006xÐ¥¤\x0014µ¹ÂÂ( AE\x0014P\x00027Üo¥}wc\x0002\x\x0017KK O²[3<_{\x0000)Çã~5ò#}ÆúWØZ4o/4Ä;ÚÆ\x00100Û{ÖUN¬6ìÈ·Ðè¬1xQ*\x0004\x001bYNÖlOqÀSÛ\x001dóV5
\x001b^¸Îä<)ó\x0018©ÎÓÎÝ¹ÁÀ\x001e£<Ö\x0016·ð8T;#÷·,Ùôã\x001f_¥k\x000càg\x0019ïÄê0,|9qgª%ãjJË´L\x000e\x001c\x000bsì+ ¢\x0000(¢\x0000(¢\x0000(¢\x0000+çïßò4i?õäô3_@×Ïß\x001f¿ähÒëÈÿ\x0000èf®Äc_à<(®(¢\x0000(¢\x0000\x0007Qõ\x0015ö­üy[ÿ\x0000×5þUñPê>¢¾Õ³ÿ\x0000+úæ¿Ê±«ÐéÃnÉ¨¢Èë</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢<ãïüôOúý?ú
]Ôcð}×ÄKXeî\x001dttPaó\x0002 çø±nêÇßù\x0001èõúô\x001a¹}yá	¾#ÛYÍetÁ1!¼°¾fÐT\x0011¸ÀÜ\x0007ø×M\x0015x½\x001bÑì`¥\x0008Õ¼µ].^{\x0003´úàÇ<ÜuÍkÿ\x0000Âaá?_üþ&±ßTðp³¡j%Ã\x001cm'\ýk{þ\x0013{Lq¤kø.zÅ£QÖ>(ðÝåô6öññ#mý\x0011×©^+Ë~?ÇÎþóÿ\x0000è"½^ÏÅ¶×·[&«ÆÒ¶ÐóXº úÐW|~ÿ\x0000/ýçÿ\x0000ÐE8üDÔø\x0019ãBRÖç\x0003</p><p>(¢\x0005\x0014Q@\x0008ßq¾öOÿ\x0000äVÒ?ëÊ\x001fý\x0000WÆÍ÷\x001bé_døoþEm#þ¼¡ÿ\x0000Ð\x0005eTêÃnÍ:(¢±:( \x0002( \x0002( \x0002( \x0002¾~øýÿ\x0000#Fÿ\x0000^Gÿ\x0000C5ô
|ýñûþF'þ¼þjéüF5þ\x0003Éh¢è8B( \x0002( \x0000u\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®kü«\x001a½\x000e6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ÕÛýoÃ²|F¶Òît"o¿u\x0013j</p><p>ûX1PG\x0003¨Æ\x0006jÇßù\x0001èõúô\x001aÒÔ<E`~ Zé\x0017
´\x0008ã71(Ê\x001b?Ü\x001fZé£\x001ehËKèúØÆ3P¬vÕl®þCßÄþ\x0019Y\x001f	Æ\9\x0019ò­ù9ÿ\x0000zº/øJïèTÖïÿ\x0000â«\x0005üq</p><p>ÌÉÿ\x0000\x0008Õ±!ÏÚ\x0013Ý®k$Ç\x001e\x0011ü\x0018GX´h¬üGwuy\x0014\x000fáÍVÝdl\x0019eTÚç
^Oñûþ>t¿÷ÿ\x0000A\x0015ß?Äxlµ(í5kk;\x0010[\x00121Ô¢ÇõUæ¼Ûãn©a«e\i×°]B]þhd\x000c\x0007Ê:ã¥8üDT~ã<RÒ</p><p>ZÜáaE\x0014P ¢(\x0001\x001bî7Ò¾Çðã(ð¾\x001fñå\x000fö\x0005|rFA\x001eµè¿\x0018µ»K8-O°e5I\x000f\x0014\x00003Ïµg8·±½\x0019¨^çÒÛ×ûÃó£zÿ\x0000x~uóü.­wþºwäÿ\x0000ãGü.­wþºwäÿ\x0000ãQìÙ¿·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüëçÿ\x0000¤\x001f\x0014i89ÿ\x0000B?ú\x0019¬ÿ\x0000ø]Zïý\x0003tïÉÿ\x0000Æ¹_\x0015ø¶óÅ÷×7¶ðBÖñÔC\x0010NyÍT`Ó¹Z±l~(­NP¢(\x0000¢(\x0000\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Æ¯C§
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5gRñý¿Ä]\x000eçEµ},\x0008Ï,D¹R\x0001ó\x0003tÀ=½«[âfñf§ZÁtí\x000cÍ)gRÙã\x0018ãë\¹ðçÊ>9r£\x0018\x0006\x0010qÓOáz_G¹d¡Q¶¾ã©\x0019øJÈº\x0014D\x0006 \x001cOÏ?õÎ¹O>2ñ6a\x000eq\x0005¶÷]ä´¸gc\x0018à®p1ü©ÿ\x0000ðüCÿ\x0000¡òOûõÿ\x0000Ö¯6ñDü$ïkâ
VmJK\DgèB»\x0000{\x0013YÊ\x001cºnÆ\x0015¼\x0006yÖ5\x0007æ<3Z\x001a®¶Qcrñ\x0013\x0019y\x0015½g§Z[Á}ÃÌ_õ¹ÁïíRjv2Im6`VUPÍÓ,@É\x001e­s{Væ­±Ü°ª46ç²ír\x0007jJôßøS\x001aS¬[ß¦ÿ\x0000\x001a_øS\x001aý\x0005í¿ïÓwÙ+§+ìy\x0015éßð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a?áLj\x001fô\x0017¶ÿ\x0000¿Mþ4Y³cÌh¯Nÿ\x00001¨Ð^Ûþý7øÖø} è\x001aUºê¶ï©_ÌìK¬ï\x0012*\x0000)Iò«±ªRnÇÖ§ô\x000bß\x0012êñé¶\x001e_à±i\x001b</p><p>ª:ÿ\x0000Ö¯Dÿ\x0000{Âô/ü
üj[m'ÃÖ7	sg£Ëoq\x0019Ý\x001c±ßK>½j\x001dDZ¡+êy¦¿¡ÝøsZK½1¡Á-\x0019Ê°# Â³k×n´\x000eß\Éuy£Ëqq!ÌÉ})f>½j/øG¼)ÿ\x0000Bùÿ\x0000ÀÙÆhÐô<ô®¾çK°ÚX>Ìªª$+*©ÊF©¡ÞÜméÎ\x00075ÒMà\x001d3^\x0002
\x001aØi³Çó¼3Ê¬½1Þü ÕÌ\x0002ÜëÑTäDUöôÎ*¼®ör9M\x001bEÓ¯¼=5Ì>ÔÌv&\x000fAQxO´¸µâs\x001fÉ.ÇHÌ5Ç\x001f êXäg¶+¬ÿ\x00003¨c\x001fÛ\x0016Üÿ\x0000Ó&ÿ\x0000\x001a|?\x0007õky<È5Ø¢|ctjêqõ\x0006º*ÍN1­øS£8É·­ÎTéV^º\x0018Ìvë*Û¾v«\x00127duÂ[o^Ç¡ª:åµ¼QÛM\x000cK\x0013È]HU*²(Æ$</p><p>~è$ï·5Û¯ÁÍM$\x0012.·\x0002È\x000eàá\x00180>¹ÏZ%ø;ªO!mr\x0019$=YÑÄÇ8K±åôW§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf/g.ÇÑ^ÿ\x0000</p><p>cPÿ\x0000 ½·ýúoñ£þ\x0014Æ¡ÿ\x0000A{oûôßãE{9v<ÆôïøS\x001aý\x0005í¿ïÓ\x001fð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a,ÃÙË±æ4W§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf\x001eÎ]1­</p><p>Ú	òË\x0010ÄSå+¼*\x0012w>ÜØàsÀÝ]·ü)Cþöß÷é¿Æ\x001fÁÝR\x0019\x0016Hµ¸#z2#\x0002?\x0010h³\x0005NIìpÚýµ½½Ü\x000fo\x0011ÍRÆ"1¸ldãp\x0019ÇNã+ëë?øò·ÿ\x0000®kü«ç§ø9©I!Mj\x0007rrÌÑ±'ñÍ}
l¥-!SÔ"Ò²ª­c¢Znä´QEbt\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0015o¬ÅÜkÚë÷Iéô¬Ïì¿X?ï³þ\x0015»E\g(«"\nad]úÁÿ\x0000}ð¯2ñ¿ÂMgSÕ¦Õt§µ¦\x0000ÉnÒ\x0015%ÆA#\x001d\x0000à×¥ø·ÅÚw´¡{½ÚFÙ\x000c\x0011ýù[Ð{zò\x001dOâ¾­â\x001cÅjßÙ°÷\x0016ýã\x000fwÿ\x0000\x000cSs¬x4íKJtûûIEäGapíì\x0000\x0019ÎF:R
\x000b^Ön!²Óô\x001dE\x0011æS,³@ÑªíÓ\x0015±{³íJ718/Ï>ÜúÖöñ2ëA¸{MU$¾²NRU?¾E÷ÏÞÇ¿5ÃB¤jJö×sØÆÐ©B¯¦ßèÙ\x0017°ßgÿ\x0000£û"óÖ\x000fûìÿ\x0000ñ5wEÖôÿ\x0000\x0010iê\x001aeÊÏo'F\x001c\x0015=Á\x001dA\x001e´+»ÚÈñù|Ì/ìÏX?ï³ÿ\x0000ÄÑýyë\x0007ýöøÝ¤fTRÌB¨\x0019$\x0005\x001eÖAÉæaÿ\x0000d^zÁÿ\x0000}þ&¸\x0018©öÚÝ-\x001clN:rÆ½F\x001bn\x0014´\x0013G(\x0007\x0004£\x0006Áü+Ê|c'â\x0007\x001fÝ\Nn[-</p><p>(­¯</p><p>Ü,ZêBáJÜFÈ7\x000cò\x0006áüHÌ\+²ñ*4ûi\x0015\x0015vÊAÀÇQÿ\x0000Ö®6:\x0004ÙËwuvbÙEÎâGSôö®Ïû"ïÖ\x000fûìÿ\x0000`|;Ù\x0015®¥q#*(dRÌp\x0007\x0007ük¹h§MðÊ&q¹\x0018\x0011úU*JÈ9nbÿ\x0000d]úÁÿ\x0000}ð£û"ïÖ\x000fûìÿ\x0000nÑOÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÂþÈ»õþû?áGöEß¬\x001f÷Ùÿ\x0000</p><p>Ý¢k äó0¿².ý`ÿ\x0000¾ÏøQýwë\x0007ýöÂ·h£ÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÄG¸\x0012¼j½Ê\x0012Oê+h\x0000\x0000\x0003 éKEL¤å¸Ò°QE\x0015#</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>Áñ'm<;</p><p>\x0014Íu Ìp©Ç\x001e¤ö\x0015½^\x001fâÛ.¼U¨<NÉLkì\x0017W\x0008ó3ÌÍqÂÑ¼7z\x001bñ7V,JZYªö\x00041þ´ßøYÇüûYÿ\x0000ß-þ5ÅÑ[rG±òÿ\x0000Úx¿çf/Ä\x000f\x0014^ø]®j¶ùhä('y=z~U¤\x0018ü¹\x0006Ñæ\x000e§ÔU=O'TºÏ_5¿2Ò³Ü+ÿ\x0000\x000fFúVlû\x001a
ºQrwvG«G\x0002½@\x000ep¬Iï\ÿ\x0000­Ñ¤\x0005¸Y#;öïZ¶þ,Q¢_Â\x0008P0Çiýk\x001fÆw\x0011Í¥DÖÒ¤¬ÎS÷l\x001b¨öúWRuumÏ³Ì]:¸'ÊÓjÛ\x0014|\x0005ãK\x0006kF.útä-Ü>Ý\x000fï\x000fÔq_OÚÜÁ{k\x0015Õ´«,\x0012 xäSÊz\x0011^\x000bñ\x000fÃZZxcHÕl.í¾ßok
½Ü\x0011¸- </p><p>\x0006ì\x000eàõöúVÁO\x0017ºÎþ\x0017»rÑ°ilØºG,Nãñ¯eÙêIÅÙÛ^uñ§Sk\x001f\x0001=²9W½!ãº±ÿ\x0000Ðqø×¢×|}¹ùt;\÷R?\x0005\x0003ùKq½ÿ\x0000Ùéí PÇo\x000bmÏ\x0019Ës[>#â]~é\x0013\x0010\x0008\x0000Éè\x0005bþÏ\x001fò\x0011×¿ë?Í«Þ¨`¶</ì×\x001fóí7ýûoð¤V¸Ó¯¬oL\x0013*Ãu\x0019bc=	Áý
{­bø¨©ðíÚ\x0001¶£<\x0010i\x0005{Å´º#lVvYT£&¸o³\Ï´ß÷í¿Â½?M¹\x0012[Ú\\x0016\x0000\x0010¥=;\x001aézacçÏ\x001dÏ6ðöÒÁÑâ}Bùæ!	4\x0000qé¸þÐ~ÏDÿ\x0000Â=¬®NÑv¤\x000cð>AX¿\x001e®\x000bøN¶Ï\x0011Y3ãÝÿ\x0000ñ5³û=È\x0003Zÿ\x0000¯´ÿ\x0000Ð\x0005>[ÉE\x0014T\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015â~2²ÇÅ7¢E!f9\x000f¨nE{eeëz\x0005¿j!¼C¹yTáû\x001féW	r³ÎÌðO\x0017G;­Qá4W]â\x001f\x0004®º_\x0019VV*\x0003G1øÕ\x001d\x001fÃ\x0007VÔVÓíb-Ê[vÌôüknx1ýþOÅÆ_èÖWFK7FøË:AÜW#k\x0001º¼ÝO2È\x0010\x001czµéß\x0012t(|'¤Á\x0007öîõÈXÄ{q\x0018ûÄò}ã^kc\x0014Ò\o)D\x001bAÕMg7uîCP¯F6Ä¾Ú^ú\x001d¬Åâûé^Û\x0007rÄXÜó]-|?c¹íÆ |À9cËÏðV³¥éð^'êúGu6í\x0018'bsÐôï\x0006ê:íö¥5µÖ¢ÆÞ4wEÚ§\x0003pÚ:zf¹)Â¶ª£M\x001eî.XyZXTâýtýY´|;£\x0010A[Ü\x0011þqKáß\x000eh\x0019ÕÓS²îKÔ¬f|°LðH\x0000\x000eqÅz.¦[Ë¥Å%ÊùÒÙsÜúVöEüûûèÿ\x0000h£m\x0019*óø¥s»ñ-ÕÕ¤°#ÍnÒ.Ñ,1|éî3Â¸_Âöô±ÉªjÚÕÛÆ\x0008C)\x0007h=qòñ^¿ýaÿ\x0000>ãþú?ãPÜévIi3¬\x00002£\x0010w\x001e\x000e>µZìªÿ\x00001ãúOt\x0019åkKÝYL \x0006ÁÛÓè+Sû\x001eßþ:Çýýjèü$N¥4wgÍEp\x0007\x001cJëÿ\x0000²,?çÜßGühÔ=^çMá»i³jÚè\x0007øDÍRéú\x0005ò2ÜêS\x0019\x0000Ïwc\x001eW«dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãKPöuácºXì´þI\x0005pbÉÁ©´½Q´Â\x0007¹ta©*>®KjÇÄ^JÎVßÏ\x000bå\x0001Û3]GöEüûûèÿ\x0000\x001a³«üÇø«BÓ<_©­þ¢×©2Â!\x0002\x0005Ú6Opyæ®ø:ÖÏÁ\x0016VÚgÚ¤K\x0004n\x0013q\x0004\x000cqW£ÿ\x0000dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãOPöU{çü%·\x001fóËÿ\x0000 ñ­}'P¿ÔvLc[\x0012C\x00120xöÍbMhÑøÊ\x0013\x001f³yÊ<¬q3×½v\x0010Á\x0015¼b8P*\x000ep(±P§Rþó$¢(:\x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000eKÇ\x000b7ôÌõ«\x0003ÂO³Äßí\x0007_ütÿ\x0000u>5ÌÐ|À3åJ­ô\x001d?­qz\x0014ÞF½c!8\x001ehR~¼Z¥±/rÆk]:çXÓÁðÌ<G@è9ÜzWÛYÅk»ËÜwuÉ®¿â\x0015Ë]xãQ,x¬Kô</p><p>?©5ÌS[\x0012÷\x001aÅù\x0017'ÜàWWðú9´o¤Ôþå@</p><p>:|ÕËWiðý~{öÿ\x0000p:\x0018!ú§Ä
~ÆòãO±\x0018-à</p><p>Â\x000b\x0011äæ±ßÇ\x001e's­\÷véYZù­ãúÎÿ\x0000ÌÕBB\x0000÷¢Ásª³øâ{9\x0003\x001dGí</p><p>:¤ñ«\x0003ù`×ªxgÅpø¯AºF!»</p><p>Í\x00089\x0000pG±¯\x0001\x00040È jéü\x0007«'Å\x0010}°]©·Óº\x0003ÎCLôo\x0003Fé©\F_Ü£Þ»ªæü7µÌ?éþuÒT( g)\x000e&ñ&O\x001f¿'òÏøWW\®|A»¶÷aúÿ\x0000uTØQE\x0014rÚ!ñ\x0006ÿ\x0000öÑé]MrÚêÕÕ¿¼ªOçÿ\x0000Ö®§¨¦ ¢)\x000c(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000¥«Z}»Iº¶\x001fyã!~½Gë^L®Ñº¸áÐ=¯YÕ.&·° Rd?(`3·=ÿ\x0000</p><p>ó\x0016ðwg{»f9$Äy5JÝN,V"tP7ÎÆ\x000fÄ\x000b\x0007^\x001a².m5$YÇ@Û@eúñú×%^þ\x000e\x0012Gå½ÌìÝ1\x001cU6ðNCÞ\x0015aÕHÆ?\x000cÓºîc\x000ceGñÓkÑ§þG\x0005]ÏW\x0016wÒ\x001fùè£ò\x0015:x"ÆP|¹Ë×lyþµ­¥è±hÖÓÛÄN%;)·c¥\x0017F´q\x0012ù\\x001aù£Èn¯O+ êìr~µQÝåõ+\x000bC¤Y\_Æÿ\x00004\x0010»üÖã\x0007×5åc¥\x0017]</p><p>¡ZUSr¿\x0012X$) çpEiÄJÍ\x001b\x0003\x001c\x0010\x001a©¥i×:éÖ3#¤o1\x0003û¨2jÊ\x001f\x000fûB¹ô\x0007?ãòoúæ?tµÍxoþ?&ÿ\x0000®cù×KY³D\x0014QLýKÿ\x0000ºh\x0019Ìè*\x001bVfÏÝV#óÅu5Ìøisw+wXñùþµtÔ1 ¢(\x0019Ìøqy\x001b\x000e­\x001e?#ÿ\x0000×®>bCþÈ®Ä©ûËwõV\x001fÊ·-	6P\x0013ÔÆ¿Ê¨¢C</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>òÿ\x0000\x0014ÈÉyþòÿ\x0000è"½B¼¿Å\x001fò2^¼¿ú\x0008¦ÎÀ_ñé{ÿ\x0000]\x0017ùTú¨ó5õBx%\x0014T\x001e\x0002ÿ\x0000Kßúè¿Ê¬\þûÄê§´ª? 
\x001dC \x0011n>Ïðÿ\x0000Xlà´>Xÿ\x00000_ë_6W¿|_Êð+F\x000e\x000c×1§×¥x	8\x0019¦¶&[¯ðWIó.µ=ZDÊ¢hò;¿M¿s~.Ñ\x000eâE\@Î%ýÆ9\x0003ð9\x001fzÿ\x0000Ã½ èÞ	ÓáuÛ4ËöÞ~\x0007áXß\x0015ô_µèöú´KlÜ,\x001dcb?Çæh¾£¶ß\x001dF¡"\x0013ó49\x001eø#ük§¯>±¼û/ôU'\x000bp%ÿ\x0000ß\x0000ÔW ÒcAP^1[\x001b\x001dDlJªêOåé
ÿ\x0000LÈ¤3#ÃIóÜ? UþuÐÖ\x001f\x0010\?«ù\x000fþ½nPÁ\x0005\x0014Q@\x0018^%\ÃnÞGæ?úÕ§¦¶ý2Ù½c\x0015CÄk\x0018Ûû²0jæÛ´eÇäh\x0017Rí\x0014Q@Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002¼¯â\x001cÿ\x0000Ùþ#O%\x0014ùð,\ü¯T¯&ø£ÿ\x0000#\x001d¯ýz\x000fý
©¡=ÃáþÙ<2;@i\x001c¾=\x0007è)è\x0004Þ)>Ò\x0013ù\x000fþµGðïþDÛ_÷äÿ\x0000ÐK`\x0003øV\x0007Ò0þ_Ö9?³íÑ4»|ÿ\x0000¬¹gÿ\x0000¾Tÿ\x0000ñUå~\x0019ÒN¹âm?M\x0000aæ{ å¿@kÐ~7Ïí\x001eß?v9d#êTCLø-£ù·÷úÌòÂ¢Þ"Gñ7,GáøÓ[\x0012õìÊ¡T*\x0000\x0018\x0000v¨/í¢½Óî-¦MñË\x001b#/¨"¬R7Ý?JÏ\x0015ñuõö{áéôøÃ\¥×Ë¿ è9üëÚÇNF+Ç|_	k+Y\x001f»|Áý+Ô4
Ium</p><p>ÎõX\x0013$c³\x000e\x0018~y¥ÍïX¿gh)÷4ª°@Òn3ÝqúÕêÍ×ä\x0013/=Jÿ\x00001L\x001f\x000e®,$oïH@+b³4\x0004Û¥©þó1ýqý+N</p><p>(¢2õõÝ¥ý×Sý?­?C é1\x0001Ø°?¥Öv7¶\x000fäEEáïù\x0006ÛF§Ð]MZ(¢Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002çüg«É£øvym¦HîäÂC¼\x0007¨\x0019¯#ûn¿~\x0019Î¥p3(îÃô§n¦~Ö\x001cü×·SÞDfGU\x001e¬q^Iñ6h§ñ
³C*H\x0005¨\x0004£\x0003¹½+m?Tåìïýèÿ\x0000J`Òu\x0011ÓN»ÿ\x0000¿
þ\x0014Ò)³Ö>\x001eÜÛ§­£iâY\x0003É.3÷jµ¢.íbwÏÝ
úµxéÒu\x001e¿Ù×yõò\x001bü+¢ñ4ÓÛ[iâ\x0019d91±SÀ\x001eX.b|bW\x001a\x0001-§ú$p*Úº¾§Ï=w\x0012;t¯Uøq¤Ï£ø\x001eÂ\x000b«"æ@ÓK\x0019ê\x000b\x001cûã\x001cWÁ¨­N\x0006¼¹{"T\x0012	\±UÈ8çµ{xACÖôÕ#¨k¤\x001fÖ¡6Û]g\x0005\x0015\x0017}ÍJFû§éXïâÿ\x0000
 ËxJ\x001föù\x001føÕY<yáE\x0004\x001f\x0010Xtí(?Ê¯]î?Ä^\x001eÄZ2Ám?s\x0015Äm\x001c¤d\x0002r¼û\x0012@¬?\x0000øÚãA¿GÔôÝ@³>Ù!Ý¤hä\x001c\x0012\x0000\x001d\x000føWm¦øDÒ\KPÝ'^/7?8ëÇÒ´OÄO\x0007©Ïöí¦}FOô¡Óo[\x0015\x0019´îtêÛÑX\x0002230Eex?Ùþº/õ¬ñ3ÁÃ®»\x0007àöZ«yã=\x0003^\x0011Ùéz\Ï»yEF\x001c\x0001×)òK±7GO£.Í&\x000fpOæI«õÄÚ|Ið}¤VÓkH²Ä»\y2\x001c\x0011×øjoøZ^\x000bÿ\x0000 Úßø=û0º;</p><p>+ÿ\x0000¥à¿ú
§ýøÿ\x0000£þ\x0016ÿ\x0000è6÷â_þ&e>Ì9Òê_K¹QýÂjÏú\x0014£ÒOè+\x0012ãâg®-f5¸÷:\x0015\x0000Ã ä÷i¶.Ðü<^ßVÔ\x0012ÖI0è¬r:g}(äÖ\x000b£¶¢¹Qñ'ÁíÓ]·üUÇô¥\x001f\x0011ü\x001eæ;mù7øRä`º:+_>\x0012nýâø©WÇ>\x0015~ Ó¿\x001b\x001fÎIv\x000b£ ¢²\x0013Å~\x001d|þßKÈÿ\x0000Æ¦_\x0010h¯÷u=¾(­&\x0019£EVMFÆAï-Ü³*ëS¤ Ê:°õS@:( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000c_\x0013øÏÂAÔob¸=á\x0002ÀO¯@\x0007\x001dI¯.¾øïpK
?C\x0007ðµÄÅ¿@\x0007ó¯jeWR¬\x0003)\x0018 
`Þø#ÂúMÆbXõd!?àÖÔåM|q¹2RèÏ\x0012¹ñÕÏîD©¶hØÖ0U</p><p>©<çßÒ¨Ýx¿QÑEÔ\x0006D\x0010qÐ}z×­Üü\x001cðäíî­óÿ\x0000<®	ÇýõÌà^Ùò5=E?ß(ßû(®Ô¡{ôìy¿ÙÉb~³}¤y\x0014¾5ñDÙßâ
OîÜºÿ\x0000#Tå×õõÚ½üïÜ¹þf½foÑ\x0010|\x0010:ÁíAþL*¿\x00025\x0001þ«\¶÷áeþ¦º\x0015|?ôÎIXo.¦`$º²z´×Sñ\x0006îÖæóNÒæ;Ø)hØ\x0011û}+ øûßï4ÿ\x0000e5ZO^)CòÏ¦Éî³7õQGµ¢ä¤¥°rÊÖ±ÆÛ\-ò\x001f2ùw\x0011©ä`\x000c\x001cUMFá.ïd\x0014ª¶\x0000Èçí_àß¤6þíÀþµ\x0003|"ñôÓ¢o¥ÌÔÔSTaQÍKrT%Ê¢õµíóèpÔWfÿ\x0000</p><p>|jó\x0006ÏÒæ#ÿ\x0000³Uvøiã\x0014ë¡Oø:\x001fäÕÕí©ÿ\x00002ûÃö&ñÍÕ½Í¾ ¸]_ËpÛN\x0017ÇWN~\x001dø¸uÐnÿ\x0000\x0000\x000fõ¦\x001f\x0000x°uÐ/\x0008ê)Î#ËÌÔ½n»/\x0017\x0016ÝÔ÷sÃ</p><p>b\x0015¥p¼^ïYÿ\x0000ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£EIS\y$Ó½\x0019ßÌ¸ÿ\x0000¼Äþµ\x001dt_ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£VªÓ_i}âå}vè¿á\x0002ñ_ý\x000b÷ÿ\x0000÷èÑÿ\x0000\x0008\x0017ÿ\x0000è_¿ÿ\x0000¿FkOùÞ\x001c¯±Ï\x0003Jì¾!^Áq¦O\x000cðÊM·Ïå8m§9ÁÁã­gÂ\x0005â¿ú\x0017ïÿ\x0000ïÑ£þ\x0010/\x0015ÿ\x0000Ð¿ÿ\x0000~D¥MÉKh;;ZÇ;Et_ðx¯þûÿ\x0000ûôiÃÀ\x001e,=4\x000bïÆ<UûZÌ¾ñr¾Ç7Eu)ðãÆ\x000fÓB¹\x001fï\x0015\x001fÌÔËð»ÆÓDÆxþÍG¶§üËï\x000eWØä(®Õ~\x0013xÕºé\x0001~·QñU2|\x001fñu²·O÷®Sú\x001aN½5örË±ÂR«²\x001c«\x0011ô5èIð_Å×ì	þôçú</p><p>µ\x001fÀï\x00120\x0005ï´´öód?û%KÄRî>I\x001e{\x0016«¨Ûÿ\x0000©¿º\x001fÜò5q<Uâ(Ø2kÚéw'ø×\x001fÀ­`ÿ\x0000¬ÕìWýÕvþ®Cð\x001aRGâ\x0004\x0003¾ËR</p><p>Ãÿ\x0000H|8;~.¶ÿ\x0000W¯]úèÂOý\x0008\x001aÓâï¢ûúS×Khÿ\x0000 \x0015ÜÃð#M_õúÕÛÿ\x0000¹\x0012¯óÍhÁðKÂñ\x001cÉq©MìÓ(\x001f¢ÊU°Ý¿\x0002gÜã,þ8ëñ`]XX\/rªÈßÌÒ»	|Z³ñ6­\x0006.qku6B\x0014q"p	98\x0004tô­k/þ\x000f²Á]\x001d%aüSÈògð'\x001f¥tv:V¥¦Ë\x000b\x000bkU#\x0004A\x0012¦!\ÕgE¯r:\x0015.¬¹E\x0014W1aE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ÿÙ</p><p>endstream</p><p>endobj</p><p>164 0 obj</p><p><</Type/Page/Parent 2 0 R/Resources<</ExtGState<</GS5 5 0 R/GS13 13 0 R>>/Font<</F3 19 0 R/F1 11 0 R/F4 171 0 R/F2 14 0 R>>/XObject<</Image166 166 0 R/Image167 167 0 R/Image168 168 0 R/Image169 169 0 R>>/ProcSet[/PDF/Text/ImageB/ImageC/ImageI] >>/MediaBox[ 0 0 540 780] /Contents 165 0 R/Group<</Type/Group/S/Transparency/CS/DeviceRGB>>/Tabs/S/StructParents 16>></p><p>endobj</p><p>165 0 obj</p><p><</Filter/FlateDecode/Length 1101>></p><p>stream</p><p>x½WÛnÛF\x0010}\x0017 G*°V{ßea¨µe9H\x0014I­¢\x000fF\x001e\x0018RYDdÂôÝ¯èÌRNd]+9\x0008`ZärvÎë\x000eað\x0006ÎÏ\x0007¯G¯®\x000fpy5OÝ\x000e\x0007Î8çÂ+!Àh\x000eÎs(ÓnçÏ\x0017w;7\x0006æU·#`þU[Áy"={Ñí¼ív`üz\x0004°$VÂVî¹vÀ·@]N\x0010îZÔ0\x0011 ¢\x0000É=ó`5n·0Y\x0004=Úá[&¸Äÿ*PÎ\x0003S¡\x0002Õ-\x0002¿¿ìvn£QÑÓQ>ýÐTY¸ë½É¯ÝÎx²»ÜàÎ¹ö­\x000b¤ÖBo1B\x0018ÎÐ@ÇLÐÌj´É )"ýÁ«E2OµpUÀ[Rí$|¦_eÐ1Ìrðè_"\x000eø\x001b:¨DzTº<\x0010Dlz2\x001d¡o¶WÇ:^ðO\x001c/gÈE	Ë¸Øçùþþ#O¡g£»l6ëõUM\x000f=\x0013Õ\x000fgÐë\x000b\x00195ôÚD\x001aEZÕY÷ú:\x0002|úù@dô÷2N:ÉüiÆZºu2­S¤ü\x000fôò"¬d\x0011T\x0015-dUää)®î7Í|7Ó`ò4Ó¦hr2íÏdÊû,O²Ìdy³ iËÚÐ±9Þ-Í=ÌÊ\x00036Úö³«v1>gÚÅøH{bÊîmCî\x001bb¿u+ºÇ¶Ø\x001bôà&65\x001ec[§ZÁP\XCÅpöI)»e)oÀú
X®7ûmV\1ß¶\x0010£¨îv\x000cûãH¬\x0002û]Àñ&°ÐR\x001cè]\x0008LÍcæ,HE½ËqNf\x00157Þ+\x001eONÛ÷4\x0014\x001aO\x0002»ÛÎ%>*\x00045W¾vZ\x0008æ=F3v,Ö'%ÿoT§ESAÏGÉ}ÑSxNè\x0008\x001f\x0005îñ©¡DÇ\x0006f#øéP1Í#äMzMXÐî¤>GX7|Bõ\x0013[\x0008á9¤õ3	q=Tø#/ðòËr3\x001ejZ¾¦\x001d</p><p>O÷x;\x001aöø\x0015Ýø°r»VÖÃö«v_L²qP;4çß4?JJ*\x0004¼Æk\x001a¶\x0011Á¿ëVâÃ¾\ÑÆ[¼Àm¼äæW¯Oóü¶ôVÖ²gy>ºÃ\x0013¨o¢êaåÍØÖ)ßÓC|ô8±/%6Vó£\x0013y;\x001f\x0013ùdBÑ\x0008}X,\x0016)õ\x001a{î\x001e\x0016Iðig°HëºLÃl2Ø3>&
M\x0004UzFNR\x0006ÑqÀ
ÐäâYJÊÊtSC.U\x001fÏÑ\x0013Ñ¾øpÃÌ\x000fo4ûâs2¡-ñ¡\x001eU4lêàè´l£oÕ×Q54ùjù*<(¤Ë=3¸(ël\x0003\x0014è¢ÆQê¯ô\x000en\x0007E]\x0017wÉéàM2ÇÁ\x0006ßÁMó¾¦¥ë¢¨Óòø&<ZqVYõ\x001dÎ7\x000c'\x0013tªr\x001fNZÅô¡ÈSÞÄK×­¯ï\x000e\x0004\x000bém$Ä¡ì;eh5ô\x0011³>·:vplÅ)äXÂ·Ñ8Ç°`È`\x0015k§ó³ÈI\x001cýì3Èae·m\x0017ó\x0005;o?4Poúõ?aÑ@¥</p><p>endstream</p><p>endobj</p><p>166 0 obj</p><p><</Type/XObject/Subtype/Image/Width 459/Height 334/ColorSpace/DeviceRGB/BitsPerComponent 8/Filter/DCTDecode/Interpolate true/Length 17816>></p><p>stream</p><p>ÿØÿà\x0000\x0010JFIF\x0000\x0001\x0001\x0001\x0000Ü\x0000Ü\x0000\x0000ÿÛ\x0000C\x0000\x0008\x0006\x0006\x0007\x0006\x0005\x0008\x0007\x0007\x0007		\x0008</p><p>\x000c\x0014
\x000c\x000b\x000b\x000c\x0019\x0012\x0013\x000f\x0014\x001d\x001a\x001f\x001e\x001d\x001a\x001c\x001c $.' ",#\x001c\x001c(7),01444\x001f'9=82<.342ÿÛ\x0000C\x0001			\x000c\x000b\x000c\x0018

\x00182!\x001c!22222222222222222222222222222222222222222222222222ÿÀ\x0000\x0011\x0008\x0001N\x0001Ë\x0003\x0001"\x0000\x0002\x0011\x0001\x0003\x0011\x0001ÿÄ\x0000\x001f\x0000\x0000\x0001\x0005\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	</p><p>\x000bÿÄ\x0000µ\x0010\x0000\x0002\x0001\x0003\x0003\x0002\x0004\x0003\x0005\x0005\x0004\x0004\x0000\x0000\x0001}\x0001\x0002\x0003\x0000\x0004\x0011\x0005\x0012!1A\x0006\x0013Qa\x0007"q\x00142¡\x0008#B±Á\x0015RÑð$3br	</p><p>\x0016\x0017\x0018\x0019\x001a%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚáâãäåæçèéêñòóôõö÷øùúÿÄ\x0000\x001f\x0001\x0000\x0003\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	</p><p>\x000bÿÄ\x0000µ\x0011\x0000\x0002\x0001\x0002\x0004\x0004\x0003\x0004\x0007\x0005\x0004\x0004\x0000\x0001\x0002w\x0000\x0001\x0002\x0003\x0011\x0004\x0005!1\x0006\x0012AQ\x0007aq\x0013"2\x0008\x0014B¡±Á	#3Rð\x0015brÑ</p><p>\x0016$4á%ñ\x0017\x0018\x0019\x001a&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚâãäåæçèéêòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0001\x0000\x0002\x0011\x0003\x0011\x0000?\x0000ö(¢( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002k:¢31\x0001TdÚ°î<Q\x0004r\x0015\x0016Gñ\x0013´\x001a¸Sþ\x0014gR´)ünÆõ\x0015Íÿ\x0000ÂWÿ\x0000Nøÿ\x0000ÿ\x0000ZøJ¿éÓÿ\x0000\x001fÿ\x0000ëV¿V«ØÃë´;%\x0015Íÿ\x0000ÂVçÓÿ\x0000\x001fÿ\x0000ëRÂVçÓÿ\x0000\x001fÿ\x0000ëRú­^Áõê\x001dÎæ¿á+?óè?ï¿þµ'ü%Mÿ\x0000>þûÿ\x0000ëSú­^Áõê\x001dÎæá*oùô\x001f÷ßÿ\x0000ZøJµ¢ÿ\x0000ßýj>«W°}zs¦¢¹øJ¤ÿ\x0000Eÿ\x0000¾ÿ\x0000úÔÂU'üú§ýöÂªÕì\x001f^¡Üé¨®cþ\x0012?çÕ?ï³Kÿ\x0000	T¿óê÷Ù£êµ{\x0007×¨÷:j+ÿ\x0000¦_ùõOûèÒÂS7üúÇÿ\x0000}\x001a>«W°¾½G¹ÔQ\Êx©÷~òÕv÷ÚÜÖõì7Ð	alàõ\x0007ÐÔNá¬­,E:Ñe(¢²7</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>)\x000b\x0005\x0019'\x0003ÔÕfÔ¬Tá¯-Áô2¯øÓ³bm\x0016¨¨ã\x0019¿ÕK\x001cî05%+4;Ü(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000Áñ<í\x001d¤P©#Ìc»\x001e¹lWIâ¿»kõoé\ÝzØUû´x\x0018æÝf\x0014QEt\x001caE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0002b¶<5;G©ùCîÊ§#ÜsY\x0015¥áÿ\x0000ù
Côoý\x0004ÖUé³|3j¬mÜíh¢ñ¤</p><p>(¢</p><p>(¢</p><p>(ª\x001aÎ¯k¢is_ÝåF>èêç²sMEÉÙ	´ØíSV²Ñ¬Úîþáa}z±ô\x0003©5åÚïÅKë1hðXç¬4ô\x001d\x0007ë\¿â\x000bß\x0011j-uvü\x000c¢\x0007å}\x0007ø÷¬ºöpø\x0018Á^z³Í­£¢._jÚ¦û¯¯®.=¤?\x000e¨í_Ju\x0019®å\x00149\x001cÜDß\x0013ïÚ6\x001d</p><p>\x0011[>6ñ&\x0016©4½\x0012sæ\x000fÖ±3ELéB[¢£RQÙ¥¢|[MkVKt3Ûò¿R§ø\x0013^g}k¨[-ÍÄsÂÝ\x001e6È¯\x0019}+O@ñ\x001e£áËß´XÊB<Èz\x0011ýz×[\x0003\x0017¬\x000eÊX§ö¤(¬\x000exÏÄºbÞZ¬>Yb'æ½>¶+Ê\]Þjè(¢C</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢9Ï\x0015ýË_«Jæë¥ñWÜµÿ\x0000y¿¥sUëa\x0003\x001düv\x0014QEt\x001caE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001ZZ\x0007üaÿ\x0000#Yµ¥ Èf\x000fø\x0017þk:¿ÃfÔ?\x001fSµ¢+Å>(¢\x0000(¢\x0000+Æ>'kÇP×\x0006\x000cìö|0\x0007õüº~uìõó~½ksi¯_Cv¬³	Ø¶á÷²s|×¡Á:¾\x001e2MBË©@\x0004\x0001z\x0001Ewß\x000c<?\x001e¡©ËªÜ®è¬È\x0011)\x001c\x0019\x000fÀ~¤W­V¢§\x00076yôàç.TXðßÂùnáK­jW·VÞ?¿öéôþUÙCðóÃ\x0011.\x000eæ{¼®Oó®¢ðjbªÍÞö=hP§\x0015k\x001c×Ã_
\)	k,\x0007Ö)OõÍqúßÂ«ÛUi´w\x0018\x0019ò¤\x001bdü;\x001fÒ½ztñu`÷¸§§.Ì2E$2´RÆÑÈ§\x000c0Aô"¡qÞ½£â7#Ô´Ù5kH¾¶]Òmÿ\x0000¹õ#­xÖ2+Ù¡YVÑæÕ¦éNÆ·<C7µ¸¯\x0013-\x000b\x001dÇ¼óø¢¾T\x0008æ·G"V\x001dÁ\x0019\x0006¾]¯røa©=÷V\x0019\x0018³ÚHa\x0004ÿ\x0000wªÿ\x0000<~\x0015Á¤­Î¼,õå;J(¢¼Ã¸(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ç|Uþ®×ýæþB¹ªé|Uþª×ýæþB¹ªõ°¿ÂGþ;</p><p>(¢º\x000e0¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000­\x001d\x0007fßþ\x0005ÿ\x0000 Î­\x001d\x000bþC6ÿ\x0000Vÿ\x0000ÐMgWàfÔ?\x001fTvÔQEx§Ò\x0014Q@\x0005\x0014Q@\x0005PÔ4]3V\_ØÁq]>aô=E_¢NèM'¹ÄÜ|-ðôÒï]@¹å\x0012\üx\x001aê´½*ÏG°ÊÆ\x0011\x0014)Ð\x000eI>¤÷5r¹ÖÕ¤îLiÂ.é\x0005\x0014QY\x0014QE\x00006DYchØe\\x0015#Ø×Ì×Qy\x0017Ãÿ\x0000<äeü+éyåX g8XÐ¹>Àf¾fC5Ä®åâs^®[xàÆÛB¹ë^§ðrS³XøAÇþ<+Ë\x001bï\x001aõ_°o«Îz3Dð\x000cOó\x0015¶3øLÏ
ñ£Ô(¢ñ\x000fL(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢ô\x0000QLY£w(²#2õPÃ"@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001c÷¿ÔÚÿ\x0000¼ßÈW3]7¿ÔÛ¾ßÈW3^¶\x0017øHð1ßÇaE\x0014WAÆ\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015£¡Èfßêßú	¬êÑÐ¿ä3oõ?ú	¨«ð3j\x001fÅª;j(¢¼CéB( \x0002( \x0002( \x0002§©jvzEÞ_L!:±î}\x0000\x001dMs\x0016¿\x0014<9q1G¹·\x0019áåÿ\x0000|ZBæ¯\x0015r%R\x0011vlìè¬Û?\x0010è÷øû.§k!=\x0014J\x0001ü5¤9\x0019\x001d=j\d·E)'°QG>¬øJÐàg½»\\x000cTåØú\x0001Dc); rI]\x001f\x00115¡¤øZh±=çî\x0013è~ñü¿xgjÙñ7®<KªµÜ Ç\x0012°Å_ñõ¬F8\x0015ïahû\x001av{EzÒzlFkÜ>\x0017Xµ¯Öf\5ÔÏ'à>Qü«Åìl¦Ôu\x000b{+u-,ò\x0004P=Í}-ai\x001dog\x0010ÄpF±¯Ð\x000cW&>vs«\x000b\x001fzå(¢¼£¸(¢\x0000(¢\x0000(¢\x0000(¢Ò(júÅ§É{0\x0014éÜ±ì\x0000îkÆ|Gñ#WÖ\x001d¡³v°³<\x0004üì=Ûú\x000fÖªøóÄ²x_c\x001bV1À¹àãßòÅrÕ¼ ¬ÊRìMmwsevV³É\x0015Â¶á"6\x000ekè\x000bk±øÃö×ëþ°/÷d\x001c\x001fñú\x001aùÆ»Ï¾ :vºÚ\Ïþ}Âç´§çÓò§8Ý</p><p>\x000eÌöÊ(¢¹Í( \x0002( \x0002( \x000c_\x0011Û<ö\x000b"\x0002LM¸éÞ¹*ô~£Ç¹ðåî]7ÂOPÈ×n\x001f\x0010¡\x001eY\x001en/\x0007*çÈQ]Oü"¶ßóñ/ä?ÂøEm¿çâoÈt}jsê\x0015»\x001cµ\x0015Ôÿ\x0000Â-kÿ\x0000=æý?ÂøE­ç¼ß§øQõª}Ãê\x0015»\x001cµ\x0015ÕÂ-iÿ\x0000=çüÇøQÿ\x0000\x0008½§ü÷ó\x001fáGÖéÔ+v9Z+«ÿ\x0000^Óþ{Oùð®\x000f]ñ&¢ê×\x001ay¶¾H\x001bk\x001dÊ\x0001â­C þ¡W©£Emh:~¯h¶Ú/p2ä¦àv·B:zÖü"öxÿ\x0000[?ýô?Â­S\x000f¨V9J*{ÛI,n\x0019\x0007NtaëPWDZjèã\]QW4«4¾Ô\x0012	7\x0004 ·¯\x0015Ðÿ\x0000Â1cýùÿ\x0000ï¡þ\x0015Jð¦ìÍèájU4NJ¶¼5fòÞý¤ÝÄ\x000e\x000f«\x001eÕª\x001b°VÉ\x0012¿³?øV¬Q$1¬q D^\x000eÍ[\x0015\x0019G'n\x001f\x0003(ÍJ}\x0007ÑE\x0015Àz¡E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ü]¾->§ùUZf_sÀþGó¯3®ÇÚö¯\x001cÇ	\x0010'ü\x0004súæ¹ªú,,9)$xÕåÍQ°ÅXþòØb\x000b¹â\x001e)_äj\x0000\x000bgh'\x0003'\x0002#Ö¶i=ÌkbìÆ§*íR¼eô3±þµHòrI'ÖÒ\x0012\x0000¡(­íQ1É«Vv\x0017º¢\x001b\x001bI®\x001cb4'óô¯KðÂÿ\x0000"Xïuý®Ãæ[E9\x0000ÿ\x0000¶G_ üë</p><p>ØAjÍ©QÃ¾\x0017øQí×ûzö2²:µF\x001c=_ñííõ¯N\x0014\x00000\x0000\x0000\x000c\x0000;R×V£©.fz´à¡\x001b ¢+2Â( \x0002( \x0002( \x0002³õëiáíFáN\x001a;i\x0018\x001fp¦´+\x0017Åà\x0007k\x0018ÿ\x0000I?5¸=h t¢º`§#¼R,±WR\x0019Xu\x0004t4Ú½¥èÚµt¶úu¤ÈO%GÊ¾äô\x001f
÷\x001a>ð¶¶¾ ðí­øÿ\x0000XË²Qèãþ?mV\x001f´\x001føG<=o§³\x0013$¬:\x0017=qíÐ~\x0015³,±Ã\x001bI,\x001ckÕ\x0003ñ5Ê÷ÐÝl>ÇÄÚT)¸],«ë\x001f#óéE¯tÛ¶P²Üp\x000b\x000e3õ¤3b@A\x0019\x0007ZZ\x0000(¢\x0000(¢©ÝÎÊÁ\x0010àI\x0015\x0013»4§MÔ*.QQÀÌð«7R2jJ¤î®DË"C\x0013I#\x0005D\x0005à\x0000;×\x0013â/\x0016ºb·9Ý÷I\³}\x0007o©¤ñO$]wþ\x0011è#\x0001|6âVôÆBÓ&¼böéï¯e¹ä»\x0012=aZB\x0017ÜÎR±ßGñRãÍË,¡sÜ)ý+Ð<9â»]v%\x0001HG\x0004tol\x001eÚ¾y­ß	j\x0012Ùkq$lUeãÌ9\x0006®TÕ´\x0014fï©ô]xgÅ;?³øÉ¥\x0003å¹$\x0007ÜeOò¯fÒo¿´t»{¢\x0000g\8\x001d\x0003\x0003ú^{ñÌ5®z\x0007(ï\x0013\x001fb\x0001\x001fÈÔSÒCÃ~\x0010ë\x0005¡¼Ñ¤?pùðý\x000f\x000c?üMz|ãá=a´?\x0013ØÞû°û%\x001e¨Ü\x001fçÂ¾\x0004\x0010\x00089\x0007¥:Ì îÝcM\x001a¯Ê\x0007¡þÅ*ÅXaÁ\x0007µz5s"Òò
ì#þµ@ýk§\x000bZÏG\x0006;
Ì½¤w+x^=×òÉýÈñùë+ðªb+=YGùüë¢¬±Nõ\x0019¾\x00066¢)¬ÊYØ*IÀ\x0015Îu$H^FUQÔ±À\x0015Îê~.É¶ÚÙÍ|{TãÇÊ¸\x001cøÒe½û5®Ö\x0003%wtQÐ\x001f©¯9kË§ÌkLw\x00179­#\x0006õ&SHöë/zL·b×Q·¹Óecn\x0017äüÇO¯Jì")âYa$¹\x000ekçÍ;Q\x001a¸þÌÔÛÌßÄ\x00137ÞFúÒøs_Ô¼+®¬k3y"`\x0010\x0013a\x0013ÇÐÓöbç>¢\x0010@#½-dXTW7	ik5Ì§\x0011Â#\x001f`3R×1ñ\x0002ìÙø.ü¯YBÃÿ\x0000}\x001eLÕÓ4ÔI¹bÙáW\x0013µÕÔ×\x000f÷årçêNj:AK_L	»»ðÄ=Î¥|Ë¨°®G©ÉþB»­WEÑn\x0000óôË'ÏVw~x¬¿Úp±ðt\x0012\x0011óÝ»L~Ú?Aú×-â­XêZä\x001bæ\x0018?w\x0016\x000f§SøñçNxòPvó=Ju#B\Îª\x000f\x0004x~irÚT[G\\x0016\x001fÖ´aðWàmÉ£Z?¾ÿ\x0000j\x0016å´ygi$Y%ÄaØ\x0001ésúWU\röv:©Õ÷ÔlG\x000c\x0011[Ä"$1Ñ\x0011Bø</p><p>++ÜaE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001Yúä\x001fiÐ5\x00081þ²ÚE\x001fÐ¤`\x0019JBÜ\x0019òÀ¢¯k6-¦kwÖ,0`Ð{x?*uìÚð\x001e»âk->bD212c©P	#ñÆ+èk;\x001b]>Õ-¬íã\x0014\x0018	\x001aàWø\x0006åm|o¦3+ÈcüYH\x001f©¯¡+\x001a·¹¤6*ê:¾§O}tû \x000b±ïô\x001eõâ×>!ºñF¡q©j,ÃM²\x001bã´\x0007åÏ`}O¹®³âö¤ðhÖZz\x0012\x0005Ì¥ß\x001dÕ\x0007OÌÊ¼â ö
å¬%!¿ÝÇcJ)%q·©CPÔîu)Ì¹Ûü1ò¨ô\x0015&­_éy[YÈ/\x0013rõ\x001f×­nøkDKE½ºH\-\x001b \x0003ã½jjÚ\x001d­åyp¤s %\x0019\x0014/àqYË\x0015\x0008ÏÇd2ê³¥í.v¾\x0003ñ\x0010Ö,¼®\x001c)9ØGUúsìëÂü\x0007®Å Êg)$ýÂ8\x001bq^á\x0004ÑÜA\x001cÑ6èäPÊ}Aª³9bî( ð+>ÛY´¼½kX\x0019gp\x001f-Cin\a)&ÒØÐ¬mfþÃN\x0013ww
¹!<Ö</p><p>\x0018gõ­òóèñûLô</p><p>\x001d5SÝcWIó#Ò4ë¨® ÌSG*\x0018\x001e?</p><p>½Ú¼#áÁÆ¶é¶X¤B3×ÿ\x0000J÷~Ôù9\x0012.§;rØò?\x001cÝ\x0001âù&\x0004rÇ\x0000»\x000cät¯\x0008êºÑi,âAn\x001c§#8ýJõ¯\x0011x\x00195½Oí±^}°\x0002E)»>ãÑ·Ñ­4Xü8ö$gçï6\x0000'Û8\x0014§VTãt]\x001aQ©;Hà-¾\x0015Eåwª9Ò(À\x0003ó<×7©è2øcÄ°Â³ùªcó¢n\x000e9\x0018"½¦¸¿\x0014øjûXñ-Ä-\x001aÛ|ÌyÝ¸\x0001ß®\x0003XPÄTí&tâpÔáNñZ\x000eµi®mn,&Á\x0010"69ùH?«?\x0013,~Ùà§Q¶t~\x0007\x0007ô&¯x_ÂéáØæ-qçÍ)åí\x0000\x000eÀf´5õ]\x0002þ\x001b#9-Ý\x000bHÁ@ÊZéOS¡óE}\x000bàM`ë>\x0012³FÝ4#Èû¯\x0019üF
|÷^ðWh5{­)Û÷w)æ ôuëùå[ÔWFPvg±R0\x000c\x0008# \x0010ih®sbX,©\x0019ù]Ë\x0001éíW(¢m»±F**ÈF` 8\x0003Ojà<kã
>}6M+M¹[äDÏ\x0011ÊFäüÝ	8Æ\x0007½u~&.<1ªDòÛI\x001d°¤×ÏºeÌqÃ$/ò³²°'§\x0000ÿ\x0000TV\x0014´/Ïbúï&1\x0019?:ÙÂz{Á²?29\x0007I7g?QQxrhÞòíU\x001dÈúèûW\x001dzóì¬{X\x001c-)Ñæ»gO¦\i\x001aµºËÊù×£\x0000&¼\x000cº×Q©ò¤aøWEâ\x001b´ôÆY¥8ÇÐV
ýÌki%¾s#0àvÁæ»(Ôâ¤Ï+\x0017F4ª¸Gc±Ð¾,ÜÙZÃmªXý¥cPxßkàzÁ?¯PÑuMwLP²rÐÉ\x0018*GP}ëæ¨aâd\x0018ÚId`ª2I={ÿ\x0000´k\x000fÂÐÚÞEå\³´&àqÇOlUTF\x0010m5gëZD\x001aæ>rXG(ûËÕHä\x0011ô«äõ¯<ñ\x001fÅ\x0018,n\x001a×H.	
<ì\x0007Ø\x000e¿_çE\x001as½ÍÂ¤á\x0018ûç3}ð·^¶f6ÆÞí\x0007Mµú7øÖ]<Ey|-M\x00014³
¨£×=ÿ\x0000</p><p>Ü·øµ«Å(7\x0016VGU2\x001eÇ'ùW¤øwÄºlMÍ\x0010Èq,O÷£>ÿ\x0000ã^JøKÞG\x001c)Q¨ýÖTÖn#ð×ãµñ\x001aÛÂ{\x0013ùd××IãMWûCZh\x0010þæ×÷cÝ»éøV^iöínÎß\x0019\x000f(Èö\x001cÐWN\x0016\x001eÊ·z×´©Ê¶=CKH´o\x000eZ¬ä  _?Þ<ùäµÖw-\x000c e{\x0001¼þ<âñ/Xk+?!\x000b\x0002W\x000b´ã\x000cÙçð\x0002¼c©É¯\x001aÜíÉ|${&ñ6Þòåa\x000f #aü;\x001f¥wÖ×Q]Û¬Ð¾äoÓÚ¾]ïõ/\x0002øXÇí\x0012\x001cÓ}Lÿ\x0000xýÆúç\x0003ñ©-°ã;­E\x0014Ve\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001e#ñ[Kk?\x0014%è\Ey\x00109ÿ\x0000mx#òÛù×\x000b^ññ'Fm[ÂË\x0012nÌùê=T}áùsøW×E7xÍY[Îö×0ÜFq$N®¤v äWÓZuìzk{\x0011\x0005'd\x0018÷\x0015ó
zÿ\x0000ÂmygÓ¦Ñ&÷ÖäÉ\x0008=Ðqô'õ¥Q]\tÞ¶*|dQ\x001d¿ë¨ÿ\x0000Ð+ºÔa¹WÎÖ\x001fÐé>+jÉ{â8¬c9[\x0018ö±ÿ\x0000m°Hü±\\x0015\x0011Ò	;3Ò4@\x0006gùæ*ìDLXü \x001cý+ð¥üË;ÛI'ú0BÃwE9ìkVâúâXåD\x0005\x001dJæ"\x0007\x001fS\/\x0005Vu\x001f*¹îÇ1¡</p><p>	Éù\x0018Z5¼I\x0004\x0010¯Í<Æ(÷\x001cnoJú\x0007Mµk\x001d2ÞÕ3G\x0018V#¹¯\x0008µÒµKS¶N\x0018ZÜ·O8(R\x000esÔæ½òÔÜ\x001bHMÚ¢Ü\x001ehåCc{f»*ÓpváÂJ[\x0018^'ÕÅÇ\x000cWqÇ3\x001e2FJCV¼;§%³eZYbÀç\x0003°®\x0013Æòù¾&ç*~þµÛø8çÂöð/ý\x0008Öpq#ZûO\x001b)^VHÝ¯"øÆùÔ´ôCù°ÿ\x0000</p><p>õÚñ¿
~Á»lOæÇü+\x001a\x0010Oá9o\x0007\ýÆ:L¤á~Ò¨~òÿ\x0000Zú6¾[¶ÛÝÃ:4r+î\x000ekê\x00012\x001b9,e7'\x0000\x000cg5UV¨oBJåµo\x001børÊf´ðÍp§iKd2\x0010}8ã5Æxßâ?ÚV]/CHÛ-Ðà·¨OozoÁÿ\x0000\x000e
CZY¸\ÃeòÇòý\x0007êEK¦¹}âÚºtº¯Ú¼`ë7v{\x0011ü´CÓè\x000f_ÀÕÆñ?´\x0005ãêÉq#·\x000fæIô</p><p>>ïé^ù«â&ýã­J0»RgóÓÜ?'õÍgFÙÖ¬å©Òk?\x0017.dfF³Xcí=ÇÌçßoAú×ê:¾£«ÎfÔ/&¸bsó·\x0003è:</p><p>§Eu¨¥±ÊäØW¢|"°3k×Ä|¶ð\x0007ý¦?à
rÞ\x001dð¦©âk¶píN$¸OÇ¹ö\x0015î>\x0017ðÅ§´æµ¶wämòÊýY±µDä­aÂ:ÜÜ¢ÑÀØ(£4P\x00022«)V\x0000©\x0018 ÷®cYð\x0006®OçInðÏ³`ks·èvô&ºRî\x0014w­4c\x0018P(M­×<Mð\x0015¯'}Bö[®Å\x0018Hvìä\x001cO<:Ì¾7\x0010\x001fôX<àIêØÀí^ÁªØ&¥§ÉnØÉ\x0019CèÝq?.gÔ\x0000¼â>[pÆïaë[*TjÇ¦èÅã1xy{:;3\x001eûÁú­¡ZßØXÂ·)xÖY~f,\x0006OLq+Ín|\x0019â[WeD½ÈêV"ß¨Í}Bª\x0015@\x0000\x00008\x0000TW\x0010	W#ï\x000eõ%È¬¶65GÍ7©â¿\x000b<9s\x000e±w¨j\x0016S@Öè\x0012\x00114eNæÎHÈì\x0007ë^µAÈ84R®î$¬[â\x0016¥.á\x000b¦É3,!P\x000f_Ð\x001að÷¿\x001ei3k\x001e\x0014¹ÝKÍ\x0019\x0013"\x000e­·¨\x001eøÍx'µ{\x0019u½¶ç¿:</p><p>Ôð¾·u ëB{fÿ\x0000X\x0013/cÁü\x000e
e\x0013V4¸ZkÕ`>T;®ÙÅKFsAµª:RK1f$±9$÷®ÁQ¬Wwº¦ái\x0001*?Ú?ý`k®÷À­c6wbï\x0010ðJc\x0003\x001eµ1¸Ñv4Ã$ê«¶{/<Ulu
®S0o\x0000ª\x000f¥u:4\x001dJVk\x0005I[«ÂÅ3ùq\ýæþ\x000cñ\x0005ÏçÛ!9Vú\x0008?wÉ"Jñ°tae9\x0004z×Éâ%8É4}6\x00120\x001a¹ä¾1ðLZ\x0015ßÙM#Á¼$'%sÐéYzEÃÃkn\x0007*\x000b8\x001fí)\x0018çð¯Tñ\x001eõA·vÈwý0AÏé\\x000f¼-¯\x0014/\x000cúz\x0012MË/
ì¾§ß ®\x0015%:WË§\x0018T´Om¶\ÚÅ8\x0018\x0012 |zdf¥¦C\x0012Á</p><p>D\x0008\x0015G°§Ó3</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢\x001aê®¬2¬0Aî+ç?\x0016hmáï\x0012\ØóäçÌ½c=?.}\x001d\?ÄÏ
\x001dkAûm´{¯lrë¯\x001fñ/õü=êéÊÌ+£ÃêîªÜhºµ¾¡jØ\x0016Î\x000fF\x001dÁö"¨+dS« ÄÝ\x0013¯ê7¤Ñ­ÄìáF	\x0019=?Ï¥O\x000ei\x0011\x0004«HÛ5§ß5¼Ñ·Þ\x001fÔWI\x000cÑÎâ`Ê{ôð±¥(í©Å]ÔO}\x0007ª*(\x0000z\x0001KU.u\x001b{\}Î?y?ýj×WâQ\x001b+FÇîçk§ÚÓOæ\x001eÎm^Æ%X2\x0018\x001c
uÚ\x0007§µ)m©æh37ñ§×Ô~µÈQEZ0ª­$\x0010©(;Ä¿­Ý-î·yp(ò¶Óê£úW¤ø8cÂÖð/ý\x0008×v¯`ðÄ~W´õ=â
ùóýk0J4c\x0014u`Ýê6kWü[lø¦Ý»h¿ú\x0013WµW|Z³º_\x0011CxÐ¿Ù^\x0005eÇÊX\x0012Húó^M?ïÇWUâ\x001f\x001cßëZu¶\x0016ë{8¢TAæV\x0000r}½«¢º,dô_Â¨D\x000fl\x0018(\x0006FÉ\x0003¯ÎÃúWÎµô§ÃUÙðóH\x001fì9üäcYÕØº{Ux÷Æí4\x0006ÒõE^Nëw?øòÿ\x0000ìÕìUÈüJÒÆ©à[õ\x000b-À¸Ø¯_üwuc\x0007i\x001aI]\x001f8F,\x001chÏ#\x001c*¨É'Ò½/Â\x000b¤Ë½×÷G\x001er¶~fÿ\x0000|öú\x000e~Âx{R:GloÇ\x0002\x0019An?¡ý	®ãÅ?\x0012®oì´2Ð[çi¸Çï$út~µÙ\x001aU*;DæHA^G{¨ø@ð­ºÚÉ,qykòÚÀ¹aø\x000epúÅ»·,ºn\x001cKÙç;ä0?q\x0011iÒÎÆ[\x000eXääåÖ´#µ\x0011F;ì\x0012>-YÍ,EIm¢$Æ^*¾$Fà)í</p><p>\x0003ò\x0015Mµ\x0011\x0012K_ê\x001f÷ù¿Æ.¥o\x001f\x0000oEª«Iü\x0011ªýy®¨Â="`äúÈ´'ñ\x001d©ÈÕoýç$~µµ§üP×í0.L\x0017ÿ\x0000M\x0013k~kå\j\x0017-ÖOÀ(¨\x0019¶N?*n9/z(J¬ã³=·Ã\x0014ôKÇòõ\x0005{	Ï\x0001æþú\x001d?\x0011^\x0004ñ\ÂA*K\x0013«¡È#Ø×Éµ¹áß\x0016êÞ\x0019¸W±¸&\x001cæKy9ÿ\x0000\x000eßQÍp×ËÖ:©cZÒgÓTb¹	x×Nñ]©òOx2Û9å}Ç¨÷®¼©ÂPvèFJJè(¢·6ûÆô\x001f0ê=jkÕ+|~ñ\x0007ÔP\x0005Jâ<Cð×MÖ.ZîÒScpü¸UÜ}qØý+¸¢µ§VtÝâìg8FjÒGÛü\x001fÍ½a|°y\x0011Dw\x001fÌñZ¾&ðÅá»TÓ-¤2þõú³d}æ?¯A¦º«¡WPÊÃ\x0004\x0011Á\x0015´qu9Ô¤ïc7+I\x001e\x0019Oim§I vD9VSÈ5ÚxÁE7ÞiJJõ{qÔ»þ\x0015Äc\x0007\x0007¨ê+Ü¥Z\x0015£tyu)Ê¬Í¿\x0010ëç_Ò-bxÞ\x001dBÝ÷­ÄdméÇ¿¥\x0016_l¹ÓmPê3B"\x0005q\x0008Ú\x000fà:V\x001dt\x001aIÍü\x0008×=\\x001d\x001e],]h«Å÷Þ#¸´±òâ#ÙPÛÎ:«gãýB\x0008Õ.-à\x000eãä?§\x001f¥sÚÏÚ.NÓû´áj¥U<\x0015\x0015\x000e^PúÍfù¥-O_Ðµë}vÐË\x0010òåC"'%úÕ­^5¢ê²èÚwQ¨ùdOï/q^¿mq\x0015Ý´w\x0010¸häPÊG¥yxÌ7±ÖÌô°õ½¤uÝ\x0013QE\x0015Æt\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0007QE\x0000x/ÄO	\x000fk&îÖ3ývÅÒ7î¿Ô{}+VÜ+èo\x001bý¼/u
ìBElOPýúu¯î­d²¸1¿ü\x0004úëdáÍm\x000c$ãÍËÔJPÌ¹ÚÄg®
1[4êiØr\x000e\x0008èh¢ÕXÜ«Tø±úÖÖ¤jõ­\x0016uM°Èb;~UÆh÷^EÏÇäÇµv:\x001dÑ±×,î\x0001Â¬ 1ö<\x001fÐ×­</p><p>®t[ç\x0004 £RÏcJ\x0004kq>Ô9³$úâ½6Î\x001f³XÛÛÿ\x0000Ï(Õ?!¼ZøÖIK¡éR¡\x001anñê\x0015WQÓ­uK\x0019,ïaY a¿ô5jç6<SQøY«Ç®}À¤¶/ó-Ì´F3Ñ»çè9¬/\x0016øv/\x000cj0X-Ó\Na\x0012LÛp\x0001$à\x0001ô\x0015ôE|ñãß·ø×S9TÊ_¢¿Ò·fRHç«é¯Ë³ÀZ0ÿ\x0000§|þdù×Ô\x001e	]¾	Ñý:!ý)UØt÷7ª®¤ÖË¦]\x001b×T¶10 \sVJñ\x001e.k¯øGìä"\x0018H7L§n¡~¯×éJ\x0017Vj(+TTãvyxyÆ8æ!N:Æ·,ìÙw7Í'séô¨ôÛ_*?5ÎÝ=6ûPÙ¡?7ñ7¥{Ê).HKw÷¤Mu}\x001d¿Ë÷¤þè=+&k©®\x000fÎß/e\x001d*\x001e§$óEi\x0018¤CbW øKáuæ»m\x001dö£3YZIÊ \Èã×\x0000®cÂZtZ·4Ë)À0É8.=TrGãWÓjªª\x0002\x0001À\x0003µpã±2¥hÃvuahF~ô\x0014|#ðÀa[ÂØûæ~?Jóï\x001bü:Âð\x000bû9ÞæÀ¶ÖÞ>xépG½{ïµrß\x0011¥/\x0002ji\x001f<aW=Ø°ÅpáñU}¢MÞçUj\x0014ù\x001e>r¢+ß<kKË:ò+Ë9\x001bät<ú\x000fÀ¾4Åi\x0012mQ\x0001<C¡ÿ\x0000i}é_;UÝ\x0013YºÐ5x5\x001bG"H\x001d{©ö5ÇÃª±ó:põ7ä}SEPÑµk}sI¶Ôm[0Î=T÷\x0007Ü\x001e+B¼\x0006vg¬ÕÐµ</p><p>£yìäàt\x0003Ö¦ f\ª\x0016g\x0003ÖRÜ\x0010gb\x000eEELG\x000bñ\x000bÅz¤ÓMòw\oÞ$vq·\x0018çÞ¹ßøN¼w\x001fßÑ\x0014ýl¤\x001fÖ­üR\x001eg|;\x0017÷ÍÐW°ÖI-	³m'ÿ\x0000\x000b'Å±ÿ\x0000­Ðbüm¥\x001fÖ¹ýcÄ÷ºÇÚ$Ñ#·ýö\oúÞ¾ühÉõ5P®àï\x001d	%%f|¾u¹ïZãñ5r\x001f\x00174\x0016m\x0000µ\x001bLþ\x0015ôEo¼ ýEFövÏ÷í¡o¬`ÖÏ\x001dQîbðtÞèù¦\x001dme\x0013ÉÆæ\x0003;ºV½iüS\x0008<u§Å\x00041Ä¿f\x001a\x0004ïnx¬ÊõpueV7Ã§\x001ar´B»\x001f\x0003ë¿fû.á¿u)Ì$ºÞóú×+öI~À/\x0000Ì>gO¡À5\x0000$0`pAÈ#µkVkAÅNr§$Ïu¢²|7>¥¡[ÜÜ&Ù\x0008*O÷°q»ñ­jù¹ÅÆN/¡íF\É4\x0014QEHÂ( \x0002( \x0002( \x0002( \x000f4ñåÅÔÂÅ,Nñ/îèùêGùí\uÍ7ê°ÊÊ$?Áï^ç}am¨Û5½ÔK$mØö÷\x0007±¯6ñ\x0007nt×\x0016û§³ÏP>dúÿ\x0000{8LE9ÃÙKCÎÄQeí\x0016§k
ïï\x0004\x0017J­\x001bðÏ\x0019ÊJ¾ ÿ\x0000JÎ\x000f]­Êý®Ùmç&H;\x0014»OJçï4\x0019âbÖùuê\x0015¸?ýzÎ¦\x0016PÛRé×·3A\x0007½-5­çC@}ÔÔ°ØÝÌØ	>¤`~µÎ¡&ícVã½Æg\x0007 ò:W]lîöÑHü;('ëYvz B\x001eå÷Ñ\x0007OÇÖ¶kÒÂQ\x0013rêqW©\x00194¢{Fwöí"Òë¼+\x001f®9ýjís^\x0006¸ó¼8aðê?tµâÖ%G\x0013Ó¥.h&\x0014QEdX×`Ìz(É¯ïg7W÷\x0017\x0007¬²³þdú;Ä·&ÏÃ\x001a¥À8híd#ë´ãõ¯ûVÔê\x0005}Sá
·´¨X|Ék\x0018?÷È¯t»&Ôµk;\x0015ëq:Eù°\x0015õ*Æ0ª0\x0005*½\x0002âit\x000f\x000e^ê'\x001b¢OÝÝÏ</p><p>?3_5Â%¿ÔZIÜÈîÆI\x0019º±Ï?­zÆL¬:n­Ã³Nà{p?¯2ÓHÞkè8¯O\x0003O7Vpâ§ÍS±gP»ò#òÐþñä+\x001bõ§I#K#HÇæcÍ6½\x0008«#Nì(¢®i:lºÆ©
2E\x001c\x0012\x0003ÊÛT`\x0013Éü)¶»\x0012M»!ºuüú^§mlq5¼EÏ|v¯ t/^\x001fÖmQÚú+K|ð\0B\x000f±<\x001fÂ¼Ø|\x001e×Ød]X\x0010z\x0011#ñ4¿ð§<Aÿ\x0000?V?÷Ûñ5çb\x001e\x001a¶òÔí¢«RÙ\x001e©¨x×Ãl\x0006Yõ{fÇDÄ\x0005ÍxÇ¼s7çH GNîHØòíýæþ ×þ\x001eë¾\x001d´7w\x0011G5ªH\x001bvÏ¨àãÞ¹j¼.\x0016_<]É¯^£÷d¬\x0014QEwMn´êku©Ãçª|\x001bñ\x0003Gys Ìÿ\x0000»\x0019 \x0007³\x000f¼\x0007Ô`þ\x0006½¾pð}öÚ¾°\x0019âkyCF1þ°w\x001fB8ükèk\x000bÈ¯ìã¹²\x000cojùì\©ºÍAëÔ÷(Ñ«\x001a*sZ2É!FIÀª3Ý\x0017ùSõõ¨æ¥n~è<</p><p>¹Ë</p><p>(¢1ø<Ï\x001dxb/YSõk×«É<h<ÏÞ\x0017þDò-zÝT¶Bì(¢( \x000f
ø¢w|Fµ_îÛEÿ\x0000¡1¬ÊÑøwüLQýØ#\x001f¡5^ö]ü3ÉÆ|e¿·Ê4§¯\x0011L®}N\x0000\x001fÖ£²²P¼ÖÝ7K!À\x001eÿ\x0000J\x0002Ì\x0015T³\x0013\x0007s^¥á_\x000e®gçN ÞL>cýÁýßñ­q\x0015£B\x0017êÈ£MÕº#jÊÙlì ¶O»\x0012\x0004\x001f«\x0014Q_<ÛnìõÒ²°QE\x0014\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015\x0015ÄÑÛÛË4¤\x0008Ñ\x000b1>sR×#ã½P[i`÷·'-È:þg\x001f­kF©QE\x0011R|rgÉp²_=Ç¡ZBá\x0000À\x0019=+QÂ][å\x0002¶G\x0019íX¨î*ì¿C^Æ/\x0004ë8Ê\x000eÍ\x001c,z ¥	Æñ24lQÇÌ84¤9c=I¤®è§mw<ùZï`¢)w\x001f\x000e®\x0008{ëbz\x000f~AþÞ×x\x0012+ÄB3Ç\x0013/åÏô¯O¯\x0003\x001f\x001bVo¹ëá\x001dé\x0005\x0014Q\GIÌ|BÊð6¤AÆäTüØWÏÕï\x001f\x0013[oî÷¤ãÂ¼\x001fµoKc)îv\x001f\x000c,M÷l8ÊÛ½°8ýH¯£xïÁ
8\x0019u]I	\x0002\x001f¯Ì×±Öu\x001dä]5¡óçÅ[Ãuã«ÊÛE\x001cCòÜV®EåÅpÔoä+â	'Çº±?óÔè\x000b\Õ}\x0005\x0008¥J(ñê·í\x0018QE\x0015¹QE\x0014\x0001í\x0006¯¯.t[ø.$w	TC¸çnA$\x000fnz]p?\x0008m|\x0006yÄsqpïø\x000c/ô®ú¾o\x0014Ó­+\x001eÕ\x000bû5r;b¸¶\x0019^)\x0010««\x000e\x0008#_(Î¨2¬g1!O¶x¯§|M}ýáNð\x001c4VÎWýì\x001c~¸¯EwåÚLäÇ=R\x0016(¯Tà</p><p>ku§SOZlTw64ÿ\x0000\x0012\XÚ¬\x001eJH«÷I$\x0010=+èO\x0007N>\x0010Òî\x0011\x0015<Ø\x0015\x000fïcæýs_0í>
ñ\>\x0011ÓíE¢Éå¡]ÆL\x0011ö¯+\x0015ÅMj÷=\x0008cä¢¡VZ-ìõ¢¹\x0015½FiÕæ\x001d©Ý\x0005\x0014Q@\x001ekââ÷ÓÊ?øûW­Wk?Æ­
ºÕÍzÝTöBQE\x0015\x0005\x0005\x0014Q@\x001e\x000fñ\x0000îø¡/û1§þTäár#+\x000e êõ\x000cÏ«üK¾Ô%;,`(¤ço-x\x001fOã(mVÒ\x0019Y\x0000º-µ\x0008ã#¾kÒÁãc	ÆWlåÄ`å(J³vH¯à+K[Zi&\x001b¦\x0003D\x000fOB~¿ã^+É|%z,¼GlXá%&&üz~¸¯Z©ÌSUnÉÁ´é\x0014Q\\x0007XQE\x0014\x0000QE\x0014\x0000QE\x0014\x0000QE\x0014\x0000QE\x0014\x0000×`ªY\x0015FIô\x0015ãºæ¦ú¶¯5Ñ?&í±E\x001d?Çñ¯Gñ}ãZxnè¡ÃK\x001eýL××¯ÒVu\x0019çãjj \x0014QEz§\x0014QE\x0000\x0014QE\x0000hèW?d×¬gÎ\x0002Ê\x0001ú\x001e\x000fó¯d¯</p><p>É\x0004\x0011Á\x0007^É¡ê\x0003TÑ­®óó2aýpkÉÌéí3ÐÁOx4QEy' q¿\x0014A>\x0008¸Çi£'ó¯\x0011²±ºÔnÚÒ\x0016Vì£·©ô\x0015ô­¥Ûk:dÚ}â±`\x0003m8#\x000f®k,hzv¦Go§[,)¼n=Yø<ÔÖ*!ÆìÆð,Ztv´ì­æHe!T\x0000äçÛÒºY5ëç\x001f+$î¯øÖe\x0015
ÝÜµ¡å\x001e8\x0012Â[y$¤³J\x0011ò{ü Jç«¶øi«;À8d11÷\x0007#ùâkèp²æ¥\x0016xÕãËQ\x0014Q]\x0006!Gj*kHMÍí½º´²ª\x0001îN)7eq¥wcé?\x0006Ø;ÁÚU¶0Eº»¼ÃqýMoTPF"8¢(Qø</p><p>¾^ræg»\x0015dÅ|S»û7n83È\x000f~sü|û^Áñªø­¦`\x000fúÉ\x001ef\x001fî\x0007þkÇëÛËãj7îyxÉ^§ QE\x0015ÜréL¥'µ%CeÄ
z^\x0019C³R?åoÏë^q\x0004Fââ8WïHáGâq^ª©\x001a¢* {V31¬öG¢ÚÖXÔþ-UÓvjéÿ\x0000*µ^\x0004þ&}\x0004\x001dâ(©(óKÿ\x0000Þ|sÓWû§þÆ½n¼þóãÔ#û?ôIÿ\x0000\x001aõÊ©ô\x0014z\x0014QPPQE\x0014\x0001ä\x001a×ntÏ\x001ajúl0Fêf\x0012yO\x001f»A~\x0015¨jW:¤ë-Ë\x0002Ê0¡F\x0000©µ\x0005Y¾+ë;Ô0Vn\x0008ô</p><p>+mQ\x0014|ª\x0007ÐW¯8GSÉÆâªs{6ô9¨`¹ó\x0011âBÀ¤)ë^Ólï%¬O"\x0014\x0016SØã^y^\x0003n·¿¼ þ\x0019ù¹t+.3$¢+Ì=0¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003ø!]\x001eÚ1üsçòSþ5ç5è\x0011\x0014ÿ\x0000fY·¤Äãµçïåÿ\x0000ÀGþ#</p><p>(¢»NP¢(\x0000¢(\x0000®çáö¢C\i®xÿ\x0000[\x001fò#ùW
WtöÓ5[{µ?êÜn\x001eªx#ò¬14½¥7\x0013Z3äg´QMGY\x0011]\x000eU â_5±íQÕGú\x001fÑÅ^ªzÍ{\x0011@\x0018tQE\x0000cxJ:¶q</p><p>.é£\x001elU\x0019þY\x0015ãâ¾°Í¸aþÃy\x000ftFÒµF¸ÑnIeÇð·u¯S/­oÝ³\x0019Jö9º(¢½cÏ</p><p>èü\x0003b5\x000f\x001ciQ\x0011I|ãÿ\x0000\x0000\x001b¿\x0015ÎW}ð$\x0019Hì~hí¨÷È\x001fÖ°ÄK¥\x0015z\x001eð)h¢¾l÷\x000f	øÃv'ñt6ÀçìöÊ\x0008ô$ü±^}^±âï\x001aþ»âë»ø%´û4åJ¼\x0010P\x0005\x0003\x0004`úW\x000fâß	ÝxJöÞÞâdM\x0016õ\x0014àÃÎ½ü-Z|¦§^ùÚÐçé	 Sk©³\x0004)ÑÆóH±Æ¥\x0014\x000eæ ­ï\x0008Øý£S7,¿%¸Èÿ\x0000xôþµÝÕ\x001d\x001fO]3OÜ\x0010_ïHÃ»\x001eµ­c	¸¿ >óý+	Ë©É&ç;#¸²È±#ÕcP*±E\x0015á7wséb¬</p><p>(¢Ï1²ýçÇ¹¿ÙSÿ\x0000¢\x0005zõxM× ðçÅÝGT¸I£´{#ÆrQGzë\x0017ãN~ö¨ Cÿ\x0000³Vv±1G¥Q^v\x0019|8ßzÛQ_ûdÿ\x0000f«	ñ{ÂÍÕ¯Sëoþ\x0006£]ÌòâÓâ·­ôËþõ³ÿ\x0000AS/Äï\x00087üÅý`ÿ\x0000£\x001enÇÅ
}½%ãÀVýrúeÔZµ»Ø\x001f|3K#ÆøÆT¾Aæºõ°ÿ\x0000ÃGþ+\x0013¯\x0002½\x0012\x0005Ù\x0004iýÕ\x0003ô®\x001fLí:¼}·äý\x00075ÞW66Z¤uå±ÒR</p><p>(¢¸OP(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000£©éV½°ñ\x000b mÃ\x000cA\x0007Ö¸ýCáì¹ôû°Ã´s\x000c\x001fÌwÔVô±5)|,Ê¥\x0018Tøã7z\x0016©bÄ\XÌ \x0010]Ãó\x0015G\x00078Å{¥yÎ«\x0000Vº\x000e\x0004Çë]3ÍåMk\x001büÃ\x000fÆ¼R·ÈäB1è¬</p><p>ìW^Pìòydí
´ã>¹è¯à­øùC(üñü«%ÎW´N©äP§niîí±À}ã´-ùUÛo\x000eê÷±-ì¤t'\x001b²\x0000ýMh</p><p>í|(ÙÒ\x0008þì¬?ASO9«9[\x0006'%¥F2g\x0019oà]joõ\x000c\x0003ý¹3ü³[V?\x000f`Õï®Ú\\x0004chüú×mE\ñõ¥ÖÇ\x000cp´×B( Ú\x0008àvÇ\x001aQà</p><p>+÷Ôé</p><p>«¨\x000cÙIø:µUïFl¦ÿ\x0000v9ú(¢44ûù\x001bÑqúÖ>¹¥ÛêPÜY\.QàÊÄVþßûÍøU-EvßIïN2qwBi5fxN­¥\è×Íkr½\x000eQÀù\z¥^Ó«höÍ·ºL÷G\x001fy\x000f¨¯,Öü7}¢JL¨d¶ÏË:\x000fñô5ía±j¢´·<ÊØg\x0007u±Z¾\x001c×gðæ¹o©À7yg\x000e£¡ê?ÏzÇ\x0004Òä×\­%fs+ÅÝ\x001fKi\x001e6Ð5T\x001dF\x0008Ø)Ü#©ô ÿ\x0000J~£ãO\x000eéq3Üj¶Ç\x0003îDûØý\x0002æ¾eÏÒóÿ\x0000³á}ô;V2vØõ={ã\x001dÌÊÐèÝO\x0002yðÍø/Aøæ¼ßQÕoõk´_ÝKq/÷¤bqì=?</p><p>©EuÓ£</p><p>\x00029çRSøQE>(¤E(ÙÝ</p><p>£$Ö\x000cêp;×qáï\x000eI§0º¾­É\x0019HØr÷>ø­¿¾\x000e+¶¿ÔQe¸)3ÊÆÞ¾çùVÖ¼1¬Íÿ\x0000\x0001? ®g^õ=\x0015hþåM=ÌêØðÜ^f¦\õhOçÅcéü/\x000eÛi§Ç.ûGÐúë,L¹i³,\x001c9«/# ¢+È>(¢\x0000ùÏÆ\x001bÆ¹?óòÃòâ°ò=kê	,,æbÒÚ[»\x001e¥âSÒ«¶£¿ßÒ¬[ëná[*¶[\x0019ºz\x0007á)´\x0018uÞ#ä±ò\x0000¡Ïºsë]×ð^±Ë\x001fü\x0006zîÛÂÚ\x0003ýí\x0017O?öî¿áT5O\x0008x|i·\x000f\x001ef®©V \x0008¡IIØOÝgßýûFëìYû/þNs÷2võöÅW¯M>\x001eÒH\x001fè0þTÓá­ ÿ\x0000Ë~\x000cÆ»~¯#Îúô;\x001cç\x0007úuÑÿ\x0000¦Cù×qÚ©Ùi6zk»ZB#.\x0000nIÏçW;WE8¸ÆÌà¯QT7|1\x0006û¹g#×húþµuuá¸i[ÇY\x001cü«b¼¼D¹ª3ÛÁÃó</p><p>(¢°:( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002¸O\x0012¦ÍrcýåVý1ý+»®7ÅN&þôCô&°Ä|\x0007~\íXÀ®çN·ó|/\x001c?ß¿3á«Ñt¥Ù¤Úúd¿Ê°Ã«¶væ2´cêyÎ1]\x001b67\x000bé.Jç58~Ïª]F\x0006\x0000ãèy­ß\x0007·\x0017î§ùÒ£¥K\x0017|Økú\x001dM\x0014Q]ç\x0014QE\x0000\x0015
ÐÍ¬ÃýüªjltN=T\x0000æh t¥U.ê£«\x0010(\x0003zÉ6YÆ=F:¡«®'uÇëZê¡T(è\x0005gjëû¸Ð@\x00195¡¦C\x001cñÜG,k$n\x0002²8È#\x0008¬ú×Ò\x0017÷\x00127«cô \x000e;^øY§ÞîIìS\x0013\x001b
Ñ§uý~Àj\x0006ñ\x000eIOy£í%¿ï\x0007éÈüE}\x0003EuÓÆTSxhKÈùzH¤¶ÊÑ\x0006_NÍkop14\x0011J=\x001d\x0003:¤Þ\x001cÑ\x001d²Ú=>¿fOð®.±1x7Ñ7Õû-\x0013UÔ\-s6{¬g\x001fA_DC¤é¶Ø0iö\x001fTGò\x0015l\x000ct\x00152Ì?
`û³Ã\x0007ÃýFÕ¢:¤À\x001cnÙ\x0019ÜßLô\x001f­t\x0016\x001a]¦m¢</p><p>OÞsË7Ô×eâ¨ó\x0015¼¾Wô®jº)Uu!ÌÏ/\x0016*8ô:?</p><p>ÿ\x0000Ë×ü\x0007úÕ\x000f\x0011\x000ck\x0012z\x0015_åWü-÷®à?Ö©xcWÏ¬kýk?ï\x000cèû}LÒ»}\x000e1\x001eoþÐ,\x0013\Aé]î1¥Zúd¿Êk÷\x0010e«÷ù\x0016è¢óOd(¢\x0000(¢\x0000*\x001b´ó-&Oï#\x000fÒ¦ ÓNÎâº±æã ¥®ÆóM²M¥mb\x0019Î~Z+\x000bV\x0007Ùãäÿ\x0000vº¥Â2å±Á\x001c¤¡ÏÌVëîôËDu+k\x0010R;/zlí\x0003\x0002m£ \x001eiK4efáÕyoÃßò\x0007êßÌÖ¥Eo\x001cQB«</p><p>*ÇÔ\x0005\x0015-sÎJRr]NÊppè\x0014QEIaE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001\×÷¶¯ê¬?uÍøÁ3im'¤~cÿ\x0000­YWW:ð.Õâr=«Ó-Ë´?º?JóX×|Þ`+Ô\x0000Ç\x0015\x0017©Ù?\x001cO`òµo3\x001cK\x0018?â¬øA¿Ò.Õ\x0001ýj\x0017Ã{iû®Wó\x001fýj§á\x0016Æ£2úÅýE+Z¹j\ø#²¢+°ñB( \x0002£\x0014Q@\x001c¹ë±`ïc\x001e5\x000c\x0012¸ÿ\x0000hÖ¼ý\x0006\x0005\x0000kU=MwY\x0013ýÒ
\¨n×u¤£ý@\x001címiC\x0016yõcXµ½§\x000cXÇïúÐ\x0005ª(¢</p><p>(¢</p><p>(¢2|G\x001f¤»q¿§õ®:»½R?7K¹_úfOåÍpé`ß¸Ñâæ1µDÎÂßë.~ýj¿ÇüLã>±\x000fæj\x000b®¹\x001fìëLñHÿ\x0000N½cþ´ûÉRÿ\x0000rF	é^d»lm×Ò5\x001f¥yñ¯Em5ôP?JXÝòÅ¬ú(¢¼ó×</p><p>(¢</p><p>(¢</p><p>(¢*_}Å>õZßþ>#úÕ»ÑûþõVµ\x0019¸_`k¢ýò=*/ýüËÓF%¯åõ¬²\x00088=ElU\x001bØ°Þ`èx5xw\ÈË	VÏõ\x001dc'ÊÈ{r*åeÀþ\Ê{t5©WãnÄb¡Ë;÷</p><p>(¢·9B( \x0002( \x0002( \x0002( \x0002¤Hdî¯\x001e¦#ó%U=:Ò\x0000\x0001HeE²þóþB,ãõoÎ¬Ñ@\x0015þÉ\x0017£~uÏøÊÑ\x0017CÞ å%SÉü?­u\x0015â¤ó<9v=\x0000?\x0015\x001556Ã»Uó<çMÍÕ-SûÒ¨ýEzy´tÁú\x001aó\x00017ëöKÿ\x0000M3ùW«V8mÛ¿}#ñ\x0015è\x0019C\x0001Áú\x001fðÍs\x001e\x0015lk\x001bGñDßÒ½\x001eê\x0011qk,'£¡Sø×xT<Mn¯ò[?îuWï"Åðóc·Áô4àz#~U©K]\x0007fy2ùfß/Ùåþá­*(\x00038ZÌ\x000fÆ,¤=J¿PÜÝAem%ÍÌ©\x0014\x0011)wÎ\x0002Ü`qwK²îeôr?ZÞÐì¬<×'çbGÓ¥yÕ÷ÄO\x000f½ôï\x001c\x000cÎ\x0008¯ë^«¥ì:U«'Ýhâ3ýhi­Äd¢Ö\x0011ü9úV·£.Åäc¥ME!\x0001\x0005ISØâ»-.5\x001ae¾Td =+Í5ï\x0018èú^»}e1I\x0014¤0Xò=}k¿ðÖ·§ëÚ47:tþdj\x00020#\x000c\x0007B;U4Ò¸W66¯÷GåFÕþèü©h©\x0018Wû£ò¤Ú¿Ý\x001f:\x0000M«ýÑùQµº?*Z(\x00027\x001d\x0019</p><p>0Áâ¼¿\³\x001aV«%¬ydP\x0019K\x001eH#ükÔëÌüs}j5fÚ\x0015\x0013ÿ\x0000²y`?"?:Õ©N>ã±¶\x001f\x000fFµKVÑ×x{FÆÝnUÙÚx°`8ã<~uGÆ:s5²ß©UH\x0017k.99"µ|-w%ÿ\x0000´Ë¹@\x0012KnÀtéY\x001e>Ö °Ó-ìå`¯{.Õ$à\x0000£qþñ­\x001dZ|ýNxá©MªM{·0t}\x001aãY\x0012<\x000c±0\x000cd$g>¯F\x0016±`e?S\ÏÃùá¸Ñ®^\x0017\x000f¶å<d*ÿ\x0000u´:Ó©\x0015Î\x000f
JI*[\x0015Í¤G #ñ¦\x001b!ÙÈü*Ý\x0015%\x0014vqùR}ÿ\x0000¼µz\x0000£ö'þòÒýÿ\x0000¾*í\x0014\x0001Kì-ýñùQö\x0016þøüªí\x0014\x0001¨Z´vÅÚGóªl-,ì\x00068^õ±©\x000cØMôÍPÐÇÏ3{\x0001\Ó_¾G]7j\x0012-}_Uüée#£)PsïZTWK×ChîNXÚ\x0019\x0019\x001caÖ\x000cd_\x0007ÐÔÅ®T\(äpßOZf8\x0005àb2yP{ú×-?ÝÔåîwUj­\x0015.Ãè­67\x001f2</p><p>«=¯»å{]g\x0001Z( \x0002( \x0002( \x0002( 	í\x000e'Áî1Z\x0015\x000eAÅ\ðtó¤2Ý\x0014Õua ý)Ô\x0000â«ËK\x001f\x000e]ÉypÆÈUK­Ø\x000fS[UÅø÷À­ã\x0008­\x001a\x001bÏ³ÏnØùòQõã×Þ'£\x001aæ]\x000ecÁ:£â«xm¦\x0012¼jÒ6\x0001à\x0001OR+ÖëðÃÝ?Â2µÜsËs|ñùm+ð\x0002	\x0001GN@ëìjc\x0008ÃHV¯:ÒæWøËá§®5ÝGNt»·Va\x0012tÉÎ0xü{]\x0015iÙÜÅícð\x001d¯§xZÞ-jâIn,\x0012NZ%ì÷ÿ\x0000ëâºz(¤ÝØÐQE\x0014\x0000â=\x0006ßÄ$úeË¼k'*èyV\x001d\x000f¿Òµè \x000f-ðÿ\x0000Á«\x000b9V}jëí¬§#\x0005c?^çôükÓãbcB¢\x0000ª£°\x0014ú)¹7¸H(¢C8o\x0015ü2Ò|I<±3Ùê\x000erÒ§*çý¥?Ó\x0015?¼</p><p>\x000f¶I§óï®0$d$ QÐ\x0000®Ê®gk\x000b^áE\x0014r?:E7zx~tyýõüè\x0001ÔS|Äþúþtyýõüè\x0001kÁ|ká_\x0011j\x001e?¾Kk+öD1Ê ùevz\x000cc¿¥{Çß_Î1?¾¿8»	«´»\x0014Ó4«K\x0018ÎRÞ\x0015\x001f]£\x0019¯,øÛgw3i\x0013G\x000c[¯QIÃ\x001d¸\x0007ëõß1?¼¿&ô?Æ¿8ÊÎàÕÕCáq¢ø2\x0008î£h¦F</p><p>ç\x0000dvà</p><p>ì©ÓûËùÒï_ï\x000fÎww\x0005¢\x001dE&åõ\x001f-!\x0014Q@\x0005\x0014Q@\x0005E<ÑÛÂóÍ"Ç\x0014jYÝ\x0000\x0003¹©j½å¤7öSYÜ.èfC\x001b®z0h\x0003ÎOÄÍ;VÖîm\x0016é-´øW÷rJvùíO=\x0000ì;Ö§µ;íkZ¹»¶¦\x0014f(äaq&GÌ=\x0008ü,_ºT:}Fæ{Ul6'Ø°þW¤ÚÚÁem\x001dµ´I\x00141(T\x0006\x0002J%\x0008ss"Irr\x0013ÑE\x0014\x0012y¯> ÙÚø©tf¸\x0010Ú[×S\x0000NçÇ	Ça~*?\x000cjoâß\x0016C=ÈV¹Þf\x0018óee*\x0017\x001e\x0012È¬ýkàõæ¥â[«Ø58\x0012Îæf¼Åc"\x00169 \x000c`òxæ½\x001fAÐì<3¤E§Ù.ØÐeÌíÝ½9B\x0017æê8Ô+C^ªÝL\x0015<±÷_jl·Ã\x001fçU9'&(¦ ¢(\x0000¢(\x0000¢(\x0000¢(\x0000\x0004qô©\x0005Ä«ügñ¨è \x000b\x0002òQÔ)ü)~Úÿ\x0000ÝZ­E\x0000Yûkÿ\x0000ui>Û'÷V«Ñ@\x0013ÉÙü©>×7÷åPÑ@\x0013}¦oïþhûæ¢¢$óåþù£Ïûæ£¢$óåþù£ÏûíQÑ@\x0012yÒÿ\x0000ÏFüèó¥ÿ\x0000ùÔtP\x0003üé?¾ß\x001elßoÎE\x0000;ÌûíùÒncüGó¤¢\x000f­\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@</p><p>\x0019F?8K èíùÓ( 	EÄ£øÍ8]Ëê\x000fáPQ@\x0016~Û'÷V_\x001eè?:«E\x0000[ûpþçëGÛ÷?Z©E\x0000[ûqì­4Þ¿eZ­E\x0000J×2·ñcéQ\x0012Xä~´Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001fÿÙ</p><p>endstream</p><p>endobj</p><p>167 0 obj</p><p><</Type/XObject/Subtype/Image/Width 396/Height 306/ColorSpace/DeviceRGB/BitsPerComponent 8/Filter/DCTDecode/Interpolate true/Length 17181>></p><p>stream</p><p>ÿØÿà\x0000\x0010JFIF\x0000\x0001\x0001\x0001\x0000H\x0000H\x0000\x0000ÿá\x0000bExif\x0000\x0000MM\x0000*\x0000\x0000\x0000\x0008\x0000\x0004\x0003\x0002\x0000\x0002\x0000\x0000\x0000\x001c\x0000\x0000\x0000>Q\x0010\x0000\x0001\x0000\x0000\x0000\x0001\x0001\x0000\x0000\x0000Q\x0011\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013Q\x0012\x0000\x0004\x0000\x0000\x0000\x0001\x0000\x0000\x000b\x0013\x0000\x0000\x0000\x0000Laptop Internal LCD Monitor\x0000ÿâ\x0004\x001eICC_PROFILE\x0000\x0001\x0001\x0000\x0000\x0004\x000eWin\x0000\x0002\x0010\x0000\x0000mntrRGB XYZ \x0007Ù\x0000\x0005\x0000\x000f\x0000\x000e\x0000\x001e\x0000\x0000acspMSFT\x0000\x0000\x0000\x0000LNV\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000öÖ\x0000\x0001\x0000\x0000\x0000\x0000Ó+LNV \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0011desc\x0000\x0000\x0001P\x0000\x0000\x0000vdmnd\x0000\x0000\x0001È\x0000\x0000\x0000admdd\x0000\x0000\x0001P\x0000\x0000\x0000vvued\x0000\x0000\x0002,\x0000\x0000\x0000view\x0000\x0000\x0002´\x0000\x0000\x0000$lumi\x0000\x0000\x0002Ø\x0000\x0000\x0000\x0014meas\x0000\x0000\x0002ì\x0000\x0000\x0000$rXYZ\x0000\x0000\x0003\x0010\x0000\x0000\x0000\x0014gXYZ\x0000\x0000\x0003$\x0000\x0000\x0000\x0014bXYZ\x0000\x0000\x00038\x0000\x0000\x0000\x0014rTRC\x0000\x0000\x0003L\x0000\x0000\x0000\x001egTRC\x0000\x0000\x0003l\x0000\x0000\x0000\x001ebTRC\x0000\x0000\x0003\x0000\x0000\x0000\x001ewtpt\x0000\x0000\x0003¬\x0000\x0000\x0000\x0014bkpt\x0000\x0000\x0003À\x0000\x0000\x0000\x0014tech\x0000\x0000\x0003Ô\x0000\x0000\x0000\x000ccprt\x0000\x0000\x0003à\x0000\x0000\x0000.desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x001cLaptop Internal LCD Monitor\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ\x0011\x0001\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x000f\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0007Lenovo\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Ø²@\x0000\x0000\x0000\x0000\x0000ÿÿÿÿ \x000c\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000ø\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000desc\x0000\x0000\x0000\x0000\x0000\x0000\x0000,Reference Viewing Condition in IEC61966-2.1\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x00004\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x00003»@\x0000p\x00064\x0000Í\x0000\x0000\x0000\x0000\x0008\x0000\x0000\x0000ù\x0012\x0000\x0004\x0000\x0000\x0000\x0000ðý$\x0008\x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x00008B\x0000Ê\x000eC\x0000Ù·@\x0000øuB\x0000\x0000\x0000view\x0000\x0000\x0000\x0000\x0000\x0013¤þ\x0000\x0014_.\x0000\x0010Ï\x0014\x0000\x0003íË\x0000\x0004\x0013\x000b\x0000\x0003\\x0000\x0000\x0000\x0001XYZ \x0000\x0000\x0000\x0000\x0000L	V\x0000P\x0000\x0000\x0000W\x001fæmeas\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0000\x0000\x0002\x0000\x0000\x0000\x0002XYZ \x0000\x0000\x0000\x0000\x0000\x0000\\x000b\x0000\x00002\x0000\x0000\x0008QXYZ \x0000\x0000\x0000\x0000\x0000\x0000t4\x0000\x0000½\x0010\x0000\x0000\x0011eXYZ \x0000\x0000\x0000\x0000\x0000\x0000&\x0000\x0000\x0010_\x0000\x0000¹curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x0019\x000c+\x001d;6yVä~\x001c´ëÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002	\x000b»\x001e\x00199</p><p>[Ps¹´ÿÿ\x0000\x0000curv\x0000\x0000\x0000\x0000\x0000\x0000\x0000	\x0000\x0000\x0002\x001e\x000bÛ!Þ>(aðaÀèÿÿ\x0000\x0000XYZ \x0000\x0000\x0000\x0000\x0000\x0000óQ\x0000\x0001\x0000\x0000\x0000\x0001\x0016ÌXYZ \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000sig \x0000\x0000\x0000\x0000AMD text\x0000\x0000\x0000\x0000Copyright (c) 2005 Lenovo Corporation\x0000ÿÛ\x0000C\x0000\x0008\x0006\x0006\x0007\x0006\x0005\x0008\x0007\x0007\x0007		\x0008</p><p>\x000c\x0014
\x000c\x000b\x000b\x000c\x0019\x0012\x0013\x000f\x0014\x001d\x001a\x001f\x001e\x001d\x001a\x001c\x001c $.' ",#\x001c\x001c(7),01444\x001f'9=82<.342ÿÛ\x0000C\x0001			\x000c\x000b\x000c\x0018

\x00182!\x001c!22222222222222222222222222222222222222222222222222ÿÀ\x0000\x0011\x0008\x00012\x0001\x0003\x0001"\x0000\x0002\x0011\x0001\x0003\x0011\x0001ÿÄ\x0000\x001f\x0000\x0000\x0001\x0005\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	</p><p>\x000bÿÄ\x0000µ\x0010\x0000\x0002\x0001\x0003\x0003\x0002\x0004\x0003\x0005\x0005\x0004\x0004\x0000\x0000\x0001}\x0001\x0002\x0003\x0000\x0004\x0011\x0005\x0012!1A\x0006\x0013Qa\x0007"q\x00142¡\x0008#B±Á\x0015RÑð$3br	</p><p>\x0016\x0017\x0018\x0019\x001a%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚáâãäåæçèéêñòóôõö÷øùúÿÄ\x0000\x001f\x0001\x0000\x0003\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	</p><p>\x000bÿÄ\x0000µ\x0011\x0000\x0002\x0001\x0002\x0004\x0004\x0003\x0004\x0007\x0005\x0004\x0004\x0000\x0001\x0002w\x0000\x0001\x0002\x0003\x0011\x0004\x0005!1\x0006\x0012AQ\x0007aq\x0013"2\x0008\x0014B¡±Á	#3Rð\x0015brÑ</p><p>\x0016$4á%ñ\x0017\x0018\x0019\x001a&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz¢£¤¥¦§¨©ª²³´µ¶·¸¹ºÂÃÄÅÆÇÈÉÊÒÓÔÕÖ×ØÙÚâãäåæçèéêòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0001\x0000\x0002\x0011\x0003\x0011\x0000?\x0000÷ú(¢</p><p>(¢</p><p>(¢</p><p>(¢2õ\x0019R(ÁÂ¾w\x000f\cük"°¾/øQðÞ¥\iÏ\x001aÉ5ÃDÞbn\x0018ÛéYS]êÖó42øª\x0011"\x001c0]\x000eV\x0000û\x0010pk¢~óGeEcÙè\x001e+¾´êßÄö&\x0019Wr\x0016Ó\x0019N=Álþ\x0011_\x0018ÿ\x0000ÐÍ§ÿ\x0000à¸ÿ\x0000ñu~Ò!¯cJÍÿ\x0000WÆ?ô3iÿ\x0000ø.?ü]qÞ>Õ|YàHì\x001eMVÆóíê\x0002ÙìÛ´\x000fözÐªEèÝÚ=\x000eðø[\x001e'ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×ªº3öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ(¯\x0007ÿ\x0000¯âùéiÿ\x0000~?úôÂ×ñGüô´ÿ\x0000¿\x001fýz.ÛD÷+Áÿ\x0000ákø£þzZßþ½\x001fðµüQÿ\x0000=-?ïÇÿ\x0000^ öÑ=âðøZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×¢è=´Ox¢¼\x001fþ\x0016¿?ç¥§ýøÿ\x0000ëÑÿ\x0000\x000b_Å\x001fóÒÓþüõèº\x000fm\x0013Þ)È\x0014È¡ÉU$n#°ï^\x000bÿ\x0000\x000b_Å\x001fóÒÓþüõèÿ\x0000¯âùéiÿ\x0000~?úô\=´O~8#¹Ù\x001c¥¢ÈËzôëEÔpÅ6Ø$2&Ðw\x001f_óð\x001føZþ(ÿ\x0000÷ãÿ\x0000¯Gü-\x0014ÏKOûñÿ\x0000×©ùµô\x0005ÂÃ\x0004¨mgv8ÎãÕ\x001cWB¾5cÜ\x0003_.7Åo\x00142\x0013[)<nX\x0006G¿5ôý©-g\x0001=LjOåYUÙ\x001aSÐ(¬M( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000f!øûÿ\x0000 =\x0013þ¿Oþ^­~&P¢C	`ÀàWü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A®î×L=N;£¯j\x000f\x0018!©Ûå.W;O\x0019ÇãZ^ÑFKã#<¿2p^3ÆZZT\x001byæ&³#vÖ8ïÝÿ\x0000Bÿ\x0000 Îÿ\x0000)þ5jÏTÓõ\x0016u²¾¶¹(\x0001a\x000c¡öç¦qKÈ»\x00153uë/ë^CñàËö=\x0007ÍÝ6|nú%{¥xí
ÿ\x0000\x001eÞ\x001eÿ\x0000®ÿ\x0000$§\x0019]U{ðñN]»q!sÉ\x001d4V§"\x0014i0Ì$R^D®2\x0018\x0016\x0019\x0006·8mwaæßDÏË{!\x001eÿ\x0000þªO³è¿óúÿ\x0000ÿ\x0000Z¾>\x0011ðÖãÿ\x0000\x0012
7¯üû­'ü">\x001bÿ\x0000 \x000eÿ\x0000ëV±qKàAõ	ÿ\x0000ÏÇý|¯RÊ6Ai;H\x0008ù³Úªdzú³þ\x0011\x001f
ÿ\x0000Ð\x0003Nÿ\x0000Àu¥ÿ\x0000;Ã¿ô/éÿ\x0000ø\x000c¿áXÊ²½¬m\x001c+µî|¥ê(Èõ\x0015õið\x0007]\x0003N\x001föî´ðøoþ:wþ\x0003­O´E}]÷>SÈõ\x0014¹\x001eµõ_ü">\x001bÿ\x0000 \x000eÿ\x0000ë\åß´%ñÊÛ®b þËó<±\x0008Û»ÍÆqë)©Ý*
+ÜùÛ#ÔQê+éá\x000f\x0000IÑ4ð\x0007$ù\x000bY§ølIáë\x0012¾JçùSsHJ{\x001f<äz\×Òéá\x000eI\x001aºhyV\x0019\x0007ÈZó¯\x0011é\x001al\x001e%¾\x001b\x000bxãRQc\x0000\x000fRÔUÎ|D½9å´W~të\x0010	6\x00009? ¬Ï·h[\x0016ÉÔù\</p><p>Zû#\x0018§Sàg'Iê+µ´:MìÛDY\x0006y\x000cQ^çáo\x0008ørçÂzLóèZ|Éi\x001b;µºÄ¨É'\x0014*«±Ó­'\x0016¬×så|QFG¨¯¤¼iwàO\x0004ý/<3gq=ÎJE\x0015ªd(êÄ:àU¯\x0007'<i¥=åìbhË\x0019-(ØÏP9\x001eõ^ÓÈêú»ÚçÌy\x001e¢Q_TxÂ>\x001c¶ðåä°èZ|r(\2Û¨#æ\x001eÕq¼\x001dáÇþ)ý7¯üû­/hêîû%äz2=E}W?|/\x000bmÿ\x0000{Mfïþ¼~è<-áyÔáí4\x0011Ô\x001bu®(æ¸Y×xhÏß]?­
\x001e</p><p>¢7Cå<Þöï\x000e¥øNÒm?K´µ¯UKÃ\x0010RFÆã#µxz\x0011wW9§\x000eG`\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Î¯Cl6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ×iÿ\x0000	\x0004V·\x000c?á\x001e×&p\x0002\x0019c´Ü©ÏJâþ>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö½ÇÄ+ë\x000f6þ\x001cm61cÑ§bCá\x001dã¶ÐMo</p><p>rtè"\x0011r¨Ò5"¾Ñ¥8ÿ\x0000á\x0008¿Mì\x0017séH\x0015sÜJê­të\x001b\x0016f´³··.0Æ(3õÀ®)ü©,¬CC*\x000fÜóþålkx³þü\x0018/ÿ\x0000\x0013Y4ÊM\x001d5xí\x0001+I\x000e¦'MN\x0001nÂr+Ôlõ\x001f\x0012Ky\x0014wz\x0004\x0010[³bIVõ\¨õÆ9¯-ý ¿æ	þü¿ÉiÃâ"¯ÀÏ\x0014\x0015¯áoù\x001b´oúýÿ\x0000C\x0015+_Âßò7hßõû\x0017þ+w±Â·>¯o¼~´­÷Ö¹DóOÞ(¿Ó\x0005¤]M
ÜÀË?\x000eÿ\x0000/¢àöÉÏOJòW¸×¤l½Æ¨ÍêZZõÏ\x0019X¼¾=±¿´;\x001b&YW8\x0005;TÙ
Â KÉ_N79vÂã\x0012å0;îÇOÂ¹êb9\x001d¹èað\x001eÚ\x001cÒm|º\x001c×Ã\x001bÝro\x001bÛÛI¨Ü\x0008\x0004nóÃq+\x0011"Ð\x0003ß$\x001fÀ×º×è6ò\x001f\x001fé­Ë\x0005Fµ=ªw"1\x0018\69Ý»½zk	©Æç%j.ÜB¹{Ïù(Kÿ\x0000`ý­]Er÷òPþÁ\x001fûZµç=OÑ<ÈÙ?¼\x0008¬q§­·É|\x0004(Ù</p><p>0\x000e=+VçÌ0â#b\x0001>¹¨VÖ\x0005\x001cD¨­ÒÂ£§J\³ê&2Kmµ8ÚHÛè;Wø£þF­Gýäÿ\x0000Ð\x0016½\x0016\x001bx`ÌA·pÚ@é^uâù\x001aµ\x001f÷ÿ\x0000@\x0014äï\x0003ÊÌg\x0019Ñæs!âYÐÂÇjÉò\x0013è\x000f\x0015ÓøÁZUÆ%ÅÃ%¤Ñ*¤¶ñ\x001eÝ\x0006ÜüÙéYÐh²>-ìÈÄ!x¡B\x0001p;z</p><p>ÔºÙ¨h\x001am¥ÓÞÌ\x001a9fhÛp\x0018\x0016Olð:ñXëÐ¬­Î\x001aq¾W}O?Ó,
­ôÄ®\x0002D¨\x0008þ"y'ô¯£¼\x001fÿ\x0000"fÿ\x0000^qè"¼SSÓ¤Ón\x0004NÁÕ*àc5í~\x0010!|\x0017£@\x0002Ê"Iÿ\x0000tVÜ2êY¹ïdbxFû_ã½\x000f0\x001bu\x0001\x0001Y289?Oàí#û?PÔ®R<Gr±«\x0015\x0001T2\x0016\x0018\x0000\x000fFæ_ñ\x0005µÄ&Þ5\x001eVïõ¬psþÍO¡x\x0015¶Úæ#\x0000^\x0011û\x0011þ×¡¬\x0014\x001fµæ¾²ó,3¤©'¯ÎÞ·/x»þEkï¢ÿ\x0000èb®·ßo­Rñi\x0007Â·¤\x001c«ÿ\x0000\x0002Zºß|ýk§¡=L]J	\x001aõH"ÜàtîjM$\x0014m¦C 	Äç8ïPßÊ·32\x001c4cåÇ­2Úvµ#Ë\x0000'B¸í^T°öqIZW½µ³»6ßÜSÌ(û7\x0017¾ßðN?ãü_õþ¿ú\x0003W×¿|q!¼\x0015bÃ¡¾R?ï¯\x0001¯nÂpWøÀu\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®küªjô/
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5Pñ^³mñ\x000e×IJ´`"_6X	%H\x0007Ì\x000fÓÛÛÖ¨|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­ÛÝgÄ¶~2¶Ú³hyr Ü¥H\x0019mØÎìö®6åÒÙîe\x001a\x0015vní-7$\x0015x°JÊº$D\x0006 \x001f³ÜtÏûµ¯çøÛþ|ô?ûý/øV3ê;óX-[w\x0010\x000fØûgþºÖÇÙ¼mÿ\x0000A-\x0017ÿ\x0000\x0001dÿ\x0000â«\x0016YbÎ_\x0016\x001bÈí®¶Å¿xÑK!p=\x0018Íyoí\x0005×Eÿ\x0000~_äµê6vþ,[Èöÿ\x0000J{`ß¼X­ÝXb[òïÚ\x000b®þü¿ÉhÄ©ð3Å\x0005kø[þFí\x001bþ¿bÿ\x0000ÐÅd</p><p>×ð·üÚ7ý~Åÿ\x0000¡Ýìp­Ï«Ûï\x001f­%+}ãõ¤®cÑ9¯\x0010éXy5\x0018'\x0002EÇëYqhñÉ§Á}hªC@~÷Ó\x001eõÖêöÚmÜ]\x0002Ñ`\x0019.Ojó×%KäT±*¥Fä\x001e®\x000cE5\x0019s.§­ÇF_¸ÒqWé±Ðh:H».äùbÆÕÇÞ#ú</p><p>ë«'@Õ¬õ+C\x001d¬m\x0011\x0000Ñ·aëZÕÕFl>¶1bß´¼z\x0005r:¥½ýÏã[\x000b uÒrÍ4F@GÐ\x0000F+®®|ÿ\x0000ÉDÿ\x0000¸7þ×­á¹Ï%ua£Kñ\x0001\x0018mOMoOô7\x001fû=6=7\eùu].LpJÚ·ôzÇ·w6~\x0015íehÙäHÝàí9È\x001fZæm4y´]*ßWÓüèo¡Ì\x000b\x0012(\x0019`GÒÜT¬ÑQÁB¢ægYý¯vÔ´Ð{\x001f²?ÿ\x0000\x0017\èðF¥«ëw÷êÖ{ãQìµð½ï^\x0014XcF\x0015Ô0ú\x0011­¤ÿ\x0000Çæ¯ÿ\x0000_Cÿ\x0000E%9E(ès¼5&¹ZÐÁo</p><p>k9f:ÆªWiÍ£`\x000fûî³ô_\x0001ÞhöfÏOÖôâ¥~ÌYç\x000fQüaFÐ4û%¬sÜ\x0014áUxü2Gé\7ÃK{/\x001fé²n$7³\x0011Cc­cÌ«	\x0017\x001b¥¡èzõmM#Iµ%Ør¥lÛ?ú\x001dZÒ-|E/lm\x0013SÓÖÜ[¢\x0001öGÝ´\x000c`þÕÙµ ÿ\x0000È¿aÿ\x0000\EkN)Þæ\x0012¡N\x001f</p><p>ßs\x001bþ\x0011Íc?ò\x0011°ÿ\x0000ÀWÿ\x0000âèÿ\x0000sXÿ\x0000 þ\x0002¿ÿ\x0000\x0017[Wv/t\x0012Ká·</p><p>\x0000òX\x000c¹Îsø</p><p>u¼­,^tÓ[à\x0018b\x000bgÃéÅf§\x0007WÙòüÍ\x001e[EQöWìsÚÝ¿l|){\x0019ÔìdT\x001dÙó÷\x0000ïâÚßp7zO=qjãÿ\x0000g­\x0016È©¨ÿ\x0000×1ÿ\x0000¡</p><p>Äo¼~´ë{Hò±uêQå7d@.ü@å¾íÞOþ.µøuKÿ\x0000Ày?øºÁñEö¥5­¼\x0017RZÀ¨ò\x0019#$\x0016¢¯\x001d±çü+\x000e¹¤ø¢;+¶í§\x0016bÈp2\x0008'¡ÿ\x0000\x001açöØÖ\x0018\x001cDð[RV×§bÿ\x0000ÄëýfãÃ\x0016_Ídöét¥\x0016\x0008YX\x001d­Ô<W×«üOÿ\x0000rÛþ¾þÕå\x0015ÛEÞ\x0004aêJ¤/ \x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Uz\x001dømÙ5\x0014QY\x001daE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ü}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­{É<imãÛYá\x0013¾<±² \x0019\x000cd\x0000À»³¥d|}ÿ\x0000\x001eÿ\x0000_§ÿ\x0000A­\x000bÝ\x001bÆ©ñ\x0016ÛX¶ºM\x0011|¼C\x001cÜlÚ\x0003!\þ5ÑI¥\x0017vÓÌ¬3ýôõ4^/\x001fù­¶àÜqòAÓ?Z×þÆñGý
Kÿ\x0000ôÿ\x0000\x001aÆ}\x0003Æ¦V+­J\x0010±ÇúZð3ÿ\x0000\k_þ\x0011]Sþý_þùÿ\x0000¬fÏJñ\x000c7Iuâ5¸[/\x0017Ø7LÅyoí\x0005×Eÿ\x0000~_äµê\x0016^\x001dÔ-oa_\x0013êw)\x001be¡Gµý\x00175åÿ\x0000´\x0017]\x0017ýùÑ\x001f\x0013Sàg</p><p>×ð·üÚ7ý~Åÿ\x0000¡È\x0015£ ÜÃeâ-2êáöC
ÔrHØÎ\x00140$Öïcn}jßxýk\x000bÄ¾#Ãöv	n¥Ï\x0016ñãíY\x0012üVðr£ºjF\x0000A\x000bÇÓ8¯2ÔüYi«j\x0012Þ\ßÆdð\x0006p£²:</p><p>æj]\x0011XÜL©ÂÔÛü
-CX¿Õ.¾ÑwpÎãî¯E_`;V\x0015åýÿ\x0000ü$VX\x0002 ¼&xaüDÑýµ¦Ïì_¯øVmÎ§jÚÕ¬és\x00191nxÎsÚ¡BWÕ\x001e-</p><p>u%9Jq¾CªþêÞénmçxe_ºÈqô?\x000bøÐjr¥¢\x0016;¶â9Wúc±¯$þÚÓ?çö/×ü*UÔ­AVY=U7üúP£%Ð0ÓÄaåxÅÛ±ô5sçþJ'ýÁ¿ö½aèß\x0013tc¦Æº­Ì©v+\x0015¶ú7\x000bÖ«\x001eøwþ\x0013?í\x000fµÏö_ìß#Ùdûþnìco¥m\x0004î}"©\x0019EHé<NÚTÐÚYj\x0017°A#ÜG,QÊØó6GÓ¯4_¥µ®¥s9+\x0012ÂUÝyÂtÏ\w¯\x001cñ¶¼!ñ<·ÆSk\x001a¬VäÄãå\x001cç\x0018ã$Wàø­.wg;4×RÅäÇvc!Ñ\x000fÞÏ\x001f1Ç\x0000ûÕÎÚe¬CqG°è¶¬éÜém×÷}0ÊGb;\x001aIÿ\x0000Í_þ¾þJðO	xçÂÚ¸¸A$án!\x0008ß2ú>ðí^gñ\x001fÃV²j2ÍæDeo\x001eZîñÈ"E¦ªÝ³{Æ¶zmç¤[÷Xä_Ùñ\x0012v\x0000wÏCí\·ÃÈ´û­RkÛ«;k]@\x0000¶öñ.\x0011@ûÌ¹'æ&¸½OÄ¿ÚúÞ]\9v?*ùoÇ`8àVN}\x0015½¸\x0006Icu~GÈÉÈ â¹\[w±ç¼Ï\x0010¯É\x000fvë½úßô>\x001dk\x0013Aÿ\x0000~Ãþ¸ä¼7ñ?MK\x001f'[ºM\x0019ÂL-äo1}ð½GëTåø¦ÙxF+}6I¤ÔB5
nàF{¶Hç\x0015ÓE;~Ö5"¤´;=WÆ\x001a/ïíl5+è!ì)Â®\x0007W=\x0014\x001eÙëOÑ|S¤ø¥.eÒ®u¶Äø\x0004r;õSØ×ÎZ±:×æ\O"Ë£fõÉ\x001djÆ©\x000eKi­.~Ç4J6à2ýGNEv}Z5Ôµ·È·?wçÐ\x001e,ÿ\x0000SQÿ\x0000®cÿ\x0000B\x0015ßxýk\x0016ûânªx:x..Ö-FX´+\x001b\x0015,\x0018r\x000e:\x001cf®hþ8ðbÜ5Íîµ\x0012ÎR6þcê~Zóñ\x0011nI#ÊÅÑZK\x001aFÙaàyrÌ\x000bDáw8ê\x0007½Gg\x001cR	&\x0017x)\x0019;\x000f\{uük\x001fÆþ1ðî«u£\èÚÕ¤weÌ\x0017&\x0016Ìp°\x0019'+Î\x0008àsÉ®«OñÏÃm*\x0007ÏV¶J\x0000¼©7J@ÆXíäóÖ¹ýçæ=9B?QXHÔ{ß¥½>ýN\x0003âüßõô?ô\x0016¯(¯Føâ\x001d\x0017UÓ\x0012ÓK¿[£\x001dÖàU\x0018epFy\x001eâ¼æºè¦£fy¸h¸Ó³\x0001Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍ|T:¨¯µlÿ\x0000ãÊßþ¹¯ò¥W¡èa·dÔQEdu\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x001eCñ÷þ@z'ý~ý\x0006µï|9®\x001f\x001eÚë6ñÉ\x0008\x0011¸¶óö¸@\x0000eÛÓoSZÈøûÿ\x0000 =\x0013þ¿OþW/¼ òüKµÖíõËOµb)ÆIvË \x0010?ÙÆN1ë]4dã\x0017gm\x001fKªjuuW³^£ø3Ä
+0×e</p><p>X}®n\x0006kcþ\x0010¸qÎ·®ÿ\x0000àsa?"iY·\x0010\x0005Æ$õÿ\x0000®µ¯ÿ\x0000\x0008W=fÿ\x0000Àù?øªÅ³K\x0017lü+\x0015äW+«k\x0012ÛpI¯\x000b#}F9\x0015å?\x001fÜ´=\x0015ß\x001f­z<?e}
Í±Ï·&o$a¡l\x001aòÏßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¢?\x00115>\x0006xÐ¥¤\x0014µÐp0¢(\x0010QE\x0014\x0000÷\x001bé_^é·Ö\x001aW4ÛýBh­íb±É,\x0017(£Ä×ÈM÷\x001bé_UßZÛ_|+¶µ»³ò	lmÕà·m®Ã	Ðþ¿D¹n¹¶:pýMHüYáÉ´íXµ+g°ó|=A+¿®:Vµ¬¶×±\Û\x0019T:8\x001c0=
yÍ¥\x001eºChÇHfÜÜ\x001fîÚ\x000b`\x0002s÷À­í+ÄÑZéÿ\x0000dF½mG\x0014,\x000b3Ú08äß¥sÏøáéÜô?uìüý{Xë|´þâþTyiýÅü«ÿ\x0000á~Îîl²H\x0005c|¯\\x0013»\x001d\x0007\x0019ã½uä\x0003ëAZq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*<´þâþTê(\x0001¾Zq*ð\x000f \x000f\x0013é \x0000?Ð§ûæ¾¯¾?ÈÑ¤ÿ\x0000×ÿ\x0000ÐÍ]?Æ¿Ày-\x0014Q]\x0007\x0008QE\x0014\x0000QE\x0014\x0000\x000e£ê+í[?øò·ÿ\x0000®kü«â¡Ô}E}«gÿ\x0000\x001eVÿ\x0000õÍcW¡ÓÝQE\x0015Ö\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000y\x000fÇßù\x0001èõúô\x001a½}á]2oÖº¤:ü1jÅ0²s¸(\x001c\x001cú\x000f»T~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 Ö£§ømü}hßÛ/m­9ü\x001eäÞ\x0000Ç=\x0003¡5ÕEµ\x0017fö{\x0018{IB­ãmÖû</p><p>þ\x0010ð¡µë\x0000K\x0012Aò=zVÇö'Ãßîhÿ\x0000÷ýøªÇÏÀ\x001es×Ð6âXy±õÏ#îV·ö§Ãùë¡ß´ÿ\x0000</p><p>ÁÜÔ·§é>	P]=4±x­¼©¶ïaó/ßñó¥ÿ\x0000¼ÿ\x0000ú\x0008¯LÓµ\x001f\x0003K¨Á\x001e&o\x0019±\x0008\x0010>ïl\x000eµæ\x001f¿ãçKÿ\x0000yÿ\x0000ô\x0011N?\x0011\x0015>\x0006xÐ¥¤\x0014µ¹ÂÂ( AE\x0014P\x00027Üo¥}wc\x0002\x\x0017KK O²[3<_{\x0000)Çã~5ò#}ÆúWØZ4o/4Ä;ÚÆ\x00100Û{ÖUN¬6ìÈ·Ðè¬1xQ*\x0004\x001bYNÖlOqÀSÛ\x001dóV5
\x001b^¸Îä<)ó\x0018©ÎÓÎÝ¹ÁÀ\x001e£<Ö\x0016·ð8T;#÷·,Ùôã\x001f_¥k\x000càg\x0019ïÄê0,|9qgª%ãjJË´L\x000e\x001c\x000bsì+ ¢\x0000(¢\x0000(¢\x0000(¢\x0000+çïßò4i?õäô3_@×Ïß\x001f¿ähÒëÈÿ\x0000èf®Äc_à<(®(¢\x0000(¢\x0000\x0007Qõ\x0015ö­üy[ÿ\x0000×5þUñPê>¢¾Õ³ÿ\x0000+úæ¿Ê±«ÐéÃnÉ¨¢Èë</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢<ãïüôOúý?ú
]Ôcð}×ÄKXeî\x001dttPaó\x0002 çø±nêÇßù\x0001èõúô\x001a¹}yá	¾#ÛYÍetÁ1!¼°¾fÐT\x0011¸ÀÜ\x0007ø×M\x0015x½\x001bÑì`¥\x0008Õ¼µ].^{\x0003´úàÇ<ÜuÍkÿ\x0000Âaá?_üþ&±ßTðp³¡j%Ã\x001cm'\ýk{þ\x0013{Lq¤kø.zÅ£QÖ>(ðÝåô6öññ#mý\x0011×©^+Ë~?ÇÎþóÿ\x0000è"½^ÏÅ¶×·[&«ÆÒ¶ÐóXº úÐW|~ÿ\x0000/ýçÿ\x0000ÐE8üDÔø\x0019ãBRÖç\x0003</p><p>(¢\x0005\x0014Q@\x0008ßq¾öOÿ\x0000äVÒ?ëÊ\x001fý\x0000WÆÍ÷\x001bé_døoþEm#þ¼¡ÿ\x0000Ð\x0005eTêÃnÍ:(¢±:( \x0002( \x0002( \x0002( \x0002¾~øýÿ\x0000#Fÿ\x0000^Gÿ\x0000C5ô
|ýñûþF'þ¼þjéüF5þ\x0003Éh¢è8B( \x0002( \x0000u\x001fQ_jÙÿ\x0000Ç¿ýs_å_\x0015\x000e£ê+í[?øò·ÿ\x0000®kü«\x001a½\x000e6ì(¬°¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0000¢(\x0003È~>ÿ\x0000È\x000fDÿ\x0000¯Óÿ\x0000 ÕÛýoÃ²|F¶Òît"o¿u\x0013j</p><p>ûX1PG\x0003¨Æ\x0006jÇßù\x0001èõúô\x001aÒÔ<E`~ Zé\x0017
´\x0008ã71(Ê\x001b?Ü\x001fZé£\x001ehËKèúØÆ3P¬vÕl®þCßÄþ\x0019Y\x001f	Æ\9\x0019ò­ù9ÿ\x0000zº/øJïèTÖïÿ\x0000â«\x0005üq</p><p>ÌÉÿ\x0000\x0008Õ±!ÏÚ\x0013Ý®k$Ç\x001e\x0011ü\x0018GX´h¬üGwuy\x0014\x000fáÍVÝdl\x0019eTÚç
^Oñûþ>t¿÷ÿ\x0000A\x0015ß?Äxlµ(í5kk;\x0010[\x00121Ô¢ÇõUæ¼Ûãn©a«e\i×°]B]þhd\x000c\x0007Ê:ã¥8üDT~ã<RÒ</p><p>ZÜáaE\x0014P ¢(\x0001\x001bî7Ò¾Çðã(ð¾\x001fñå\x000fö\x0005|rFA\x001eµè¿\x0018µ»K8-O°e5I\x000f\x0014\x00003Ïµg8·±½\x0019¨^çÒÛ×ûÃó£zÿ\x0000x~uóü.­wþºwäÿ\x0000ãGü.­wþºwäÿ\x0000ãQìÙ¿·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüèÞ¿Þ\x001f|ßÿ\x0000\x000b«]ÿ\x0000 nù?øÑÿ\x0000\x000b«]ÿ\x0000 nù?øÑìØ{x\x001fHo_ï\x000fÎëýáù×Íÿ\x0000ðºµßú\x0006éßÿ\x0000\x001fðºµßú\x0006éßÿ\x0000\x001eÍ·ôõþðüëçÿ\x0000¤\x001f\x0014i89ÿ\x0000B?ú\x0019¬ÿ\x0000ø]Zïý\x0003tïÉÿ\x0000Æ¹_\x0015ø¶óÅ÷×7¶ðBÖñÔC\x0010NyÍT`Ó¹Z±l~(­NP¢(\x0000¢(\x0000\x001dGÔWÚ¶ñåoÿ\x0000\×ùWÅC¨úûVÏþ<­ÿ\x0000ëÿ\x0000*Æ¯C§
»&¢+#¬(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000ò\x001f¿ò\x0003Ñ?ëôÿ\x0000è5gRñý¿Ä]\x000eçEµ},\x0008Ï,D¹R\x0001ó\x0003tÀ=½«[âfñf§ZÁtí\x000cÍ)gRÙã\x0018ãë\¹ðçÊ>9r£\x0018\x0006\x0010qÓOáz_G¹d¡Q¶¾ã©\x0019øJÈº\x0014D\x0006 \x001cOÏ?õÎ¹O>2ñ6a\x000eq\x0005¶÷]ä´¸gc\x0018à®p1ü©ÿ\x0000ðüCÿ\x0000¡òOûõÿ\x0000Ö¯6ñDü$ïkâ
VmJK\DgèB»\x0000{\x0013YÊ\x001cºnÆ\x0015¼\x0006yÖ5\x0007æ<3Z\x001a®¶Qcrñ\x0013\x0019y\x0015½g§Z[Á}ÃÌ_õ¹ÁïíRjv2Im6`VUPÍÓ,@É\x001e­s{Væ­±Ü°ª46ç²ír\x0007jJôßøS\x001aS¬[ß¦ÿ\x0000\x001a_øS\x001aý\x0005í¿ïÓwÙ+§+ìy\x0015éßð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a?áLj\x001fô\x0017¶ÿ\x0000¿Mþ4Y³cÌh¯Nÿ\x00001¨Ð^Ûþý7øÖø} è\x001aUºê¶ï©_ÌìK¬ï\x0012*\x0000)Iò«±ªRnÇÖ§ô\x000bß\x0012êñé¶\x001e_à±i\x001b</p><p>ª:ÿ\x0000Ö¯Dÿ\x0000{Âô/ü
üj[m'ÃÖ7	sg£Ëoq\x0019Ý\x001c±ßK>½j\x001dDZ¡+êy¦¿¡ÝøsZK½1¡Á-\x0019Ê°# Â³k×n´\x000eß\Éuy£Ëqq!ÌÉ})f>½j/øG¼)ÿ\x0000Bùÿ\x0000ÀÙÆhÐô<ô®¾çK°ÚX>Ìªª$+*©ÊF©¡ÞÜméÎ\x00075ÒMà\x001d3^\x0002
\x001aØi³Çó¼3Ê¬½1Þü ÕÌ\x0002ÜëÑTäDUöôÎ*¼®ör9M\x001bEÓ¯¼=5Ì>ÔÌv&\x000fAQxO´¸µâs\x001fÉ.ÇHÌ5Ç\x001f êXäg¶+¬ÿ\x00003¨c\x001fÛ\x0016Üÿ\x0000Ó&ÿ\x0000\x001a|?\x0007õky<È5Ø¢|ctjêqõ\x0006º*ÍN1­øS£8É·­ÎTéV^º\x0018Ìvë*Û¾v«\x00127duÂ[o^Ç¡ª:åµ¼QÛM\x000cK\x0013È]HU*²(Æ$</p><p>~è$ï·5Û¯ÁÍM$\x0012.·\x0002È\x000eàá\x00180>¹ÏZ%ø;ªO!mr\x0019$=YÑÄÇ8K±åôW§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf/g.ÇÑ^ÿ\x0000</p><p>cPÿ\x0000 ½·ýúoñ£þ\x0014Æ¡ÿ\x0000A{oûôßãE{9v<ÆôïøS\x001aý\x0005í¿ïÓ\x001fð¦5\x000fú\x000bÛß¦ÿ\x0000\x001a,ÃÙË±æ4W§ÂÔ?è/mÿ\x0000~ühÿ\x00001¨Ð^Ûþý7øÑf\x001eÎ]1­</p><p>Ú	òË\x0010ÄSå+¼*\x0012w>ÜØàsÀÝ]·ü)Cþöß÷é¿Æ\x001fÁÝR\x0019\x0016Hµ¸#z2#\x0002?\x0010h³\x0005NIìpÚýµ½½Ü\x000fo\x0011ÍRÆ"1¸ldãp\x0019ÇNã+ëë?øò·ÿ\x0000®kü«ç§ø9©I!Mj\x0007rrÌÑ±'ñÍ}
l¥-!SÔ"Ò²ª­c¢Znä´QEbt\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0005\x0014Q@\x0015o¬ÅÜkÚë÷Iéô¬Ïì¿X?ï³þ\x0015»E\g(«"\nad]úÁÿ\x0000}ð¯2ñ¿ÂMgSÕ¦Õt§µ¦\x0000ÉnÒ\x0015%ÆA#\x001d\x0000à×¥ø·ÅÚw´¡{½ÚFÙ\x000c\x0011ýù[Ð{zò\x001dOâ¾­â\x001cÅjßÙ°÷\x0016ýã\x000fwÿ\x0000\x000cSs¬x4íKJtûûIEäGapíì\x0000\x0019ÎF:R
\x000b^Ön!²Óô\x001dE\x0011æS,³@ÑªíÓ\x0015±{³íJ718/Ï>ÜúÖöñ2ëA¸{MU$¾²NRU?¾E÷ÏÞÇ¿5ÃB¤jJö×sØÆÐ©B¯¦ßèÙ\x0017°ßgÿ\x0000£û"óÖ\x000fûìÿ\x0000ñ5wEÖôÿ\x0000\x0010iê\x001aeÊÏo'F\x001c\x0015=Á\x001dA\x001e´+»ÚÈñù|Ì/ìÏX?ï³ÿ\x0000ÄÑýyë\x0007ýöøÝ¤fTRÌB¨\x0019$\x0005\x001eÖAÉæaÿ\x0000d^zÁÿ\x0000}þ&¸\x0018©öÚÝ-\x001clN:rÆ½F\x001bn\x0014´\x0013G(\x0007\x0004£\x0006Áü+Ê|c'â\x0007\x001fÝ\Nn[-</p><p>(­¯</p><p>Ü,ZêBáJÜFÈ7\x000cò\x0006áüHÌ\+²ñ*4ûi\x0015\x0015vÊAÀÇQÿ\x0000Ö®6:\x0004ÙËwuvbÙEÎâGSôö®Ïû"ïÖ\x000fûìÿ\x0000`|;Ù\x0015®¥q#*(dRÌp\x0007\x0007ük¹h§MðÊ&q¹\x0018\x0011úU*JÈ9nbÿ\x0000d]úÁÿ\x0000}ð£û"ïÖ\x000fûìÿ\x0000nÑOÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÂþÈ»õþû?áGöEß¬\x001f÷Ùÿ\x0000</p><p>Ý¢k äó0¿².ý`ÿ\x0000¾ÏøQýwë\x0007ýöÂ·h£ÚÈ9<Ì/ì¿X?ï³þ\x0014d]úÁÿ\x0000}ð­Ú(ö²\x000eO3\x000bû"ïÖ\x000fûìÿ\x0000\x001fÙ\x0017~°ßgü+v=¬ÌÄG¸\x0012¼j½Ê\x0012Oê+h\x0000\x0000\x0003 éKEL¤å¸Ò°QE\x0015#</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>Áñ'm<;</p><p>\x0014Íu Ìp©Ç\x001e¤ö\x0015½^\x001fâÛ.¼U¨<NÉLkì\x0017W\x0008ó3ÌÍqÂÑ¼7z\x001bñ7V,JZYªö\x00041þ´ßøYÇüûYÿ\x0000ß-þ5ÅÑ[rG±òÿ\x0000Úx¿çf/Ä\x000f\x0014^ø]®j¶ùhä('y=z~U¤\x0018ü¹\x0006Ñæ\x000e§ÔU=O'TºÏ_5¿2Ò³Ü+ÿ\x0000\x000fFúVlû\x001a
ºQrwvG«G\x0002½@\x000ep¬Iï\ÿ\x0000­Ñ¤\x0005¸Y#;öïZ¶þ,Q¢_Â\x0008P0Çiýk\x001fÆw\x0011Í¥DÖÒ¤¬ÎS÷l\x001b¨öúWRuumÏ³Ì]:¸'ÊÓjÛ\x0014|\x0005ãK\x0006kF.útä-Ü>Ý\x000fï\x000fÔq_OÚÜÁ{k\x0015Õ´«,\x0012 xäSÊz\x0011^\x000bñ\x000fÃZZxcHÕl.í¾ßok
½Ü\x0011¸- </p><p>\x0006ì\x000eàõöúVÁO\x0017ºÎþ\x0017»rÑ°ilØºG,Nãñ¯eÙêIÅÙÛ^uñ§Sk\x001f\x0001=²9W½!ãº±ÿ\x0000Ðqø×¢×|}¹ùt;\÷R?\x0005\x0003ùKq½ÿ\x0000Ùéí PÇo\x000bmÏ\x0019Ës[>#â]~é\x0013\x0010\x0008\x0000Éè\x0005bþÏ\x001fò\x0011×¿ë?Í«Þ¨`¶</ì×\x001fóí7ýûoð¤V¸Ó¯¬oL\x0013*Ãu\x0019bc=	Áý
{­bø¨©ðíÚ\x0001¶£<\x0010i\x0005{Å´º#lVvYT£&¸o³\Ï´ß÷í¿Â½?M¹\x0012[Ú\\x0016\x0000\x0010¥=;\x001aézacçÏ\x001dÏ6ðöÒÁÑâ}Bùæ!	4\x0000qé¸þÐ~ÏDÿ\x0000Â=¬®NÑv¤\x000cð>AX¿\x001e®\x000bøN¶Ï\x0011Y3ãÝÿ\x0000ñ5³û=È\x0003Zÿ\x0000¯´ÿ\x0000Ð\x0005>[ÉE\x0014T\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000\x0015â~2²ÇÅ7¢E!f9\x000f¨nE{eeëz\x0005¿j!¼C¹yTáû\x001féW	r³ÎÌðO\x0017G;­Qá4W]â\x001f\x0004®º_\x0019VV*\x0003G1øÕ\x001d\x001fÃ\x0007VÔVÓíb-Ê[vÌôüknx1ýþOÅÆ_èÖWFK7FøË:AÜW#k\x0001º¼ÝO2È\x0010\x001czµéß\x0012t(|'¤Á\x0007öîõÈXÄ{q\x0018ûÄò}ã^kc\x0014Ò\o)D\x001bAÕMg7uîCP¯F6Ä¾Ú^ú\x001d¬Åâûé^Û\x0007rÄXÜó]-|?c¹íÆ |À9cËÏðV³¥éð^'êúGu6í\x0018'bsÐôï\x0006ê:íö¥5µÖ¢ÆÞ4wEÚ§\x0003pÚ:zf¹)Â¶ª£M\x001eî.XyZXTâýtýY´|;£\x0010A[Ü\x0011þqKáß\x000eh\x0019ÕÓS²îKÔ¬f|°LðH\x0000\x000eqÅz.¦[Ë¥Å%ÊùÒÙsÜúVöEüûûèÿ\x0000h£m\x0019*óø¥s»ñ-ÕÕ¤°#ÍnÒ.Ñ,1|éî3Â¸_Âöô±ÉªjÚÕÛÆ\x0008C)\x0007h=qòñ^¿ýaÿ\x0000>ãþú?ãPÜévIi3¬\x00002£\x0010w\x001e\x000e>µZìªÿ\x00001ãúOt\x0019åkKÝYL \x0006ÁÛÓè+Sû\x001eßþ:Çýýjèü$N¥4wgÍEp\x0007\x001cJëÿ\x0000²,?çÜßGühÔ=^çMá»i³jÚè\x0007øDÍRéú\x0005ò2ÜêS\x0019\x0000Ïwc\x001eW«dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãKPöuácºXì´þI\x0005pbÉÁ©´½Q´Â\x0007¹ta©*>®KjÇÄ^JÎVßÏ\x000bå\x0001Û3]GöEüûûèÿ\x0000\x001a³«üÇø«BÓ<_©­þ¢×©2Â!\x0002\x0005Ú6Opyæ®ø:ÖÏÁ\x0016VÚgÚ¤K\x0004n\x0013q\x0004\x000cqW£ÿ\x0000dXÏ¸ÿ\x0000¾øÑýaÿ\x0000>ãþú?ãOPöU{çü%·\x001fóËÿ\x0000 ñ­}'P¿ÔvLc[\x0012C\x00120xöÍbMhÑøÊ\x0013\x001f³yÊ<¬q3×½v\x0010Á\x0015¼b8P*\x000ep(±P§Rþó$¢(:\x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000eKÇ\x000b7ôÌõ«\x0003ÂO³Äßí\x0007_ütÿ\x0000u>5ÌÐ|À3åJ­ô\x001d?­qz\x0014ÞF½c!8\x001ehR~¼Z¥±/rÆk]:çXÓÁðÌ<G@è9ÜzWÛYÅk»ËÜwuÉ®¿â\x0015Ë]xãQ,x¬Kô</p><p>?©5ÌS[\x0012÷\x001aÅù\x0017'ÜàWWðú9´o¤Ôþå@</p><p>:|ÕËWiðý~{öÿ\x0000p:\x0018!ú§Ä
~ÆòãO±\x0018-à</p><p>Â\x000b\x0011äæ±ßÇ\x001e's­\÷véYZù­ãúÎÿ\x0000ÌÕBB\x0000÷¢Ásª³øâ{9\x0003\x001dGí</p><p>:¤ñ«\x0003ù`×ªxgÅpø¯AºF!»</p><p>Í\x00089\x0000pG±¯\x0001\x00040È jéü\x0007«'Å\x0010}°]©·Óº\x0003ÎCLôo\x0003Fé©\F_Ü£Þ»ªæü7µÌ?éþuÒT( g)\x000e&ñ&O\x001f¿'òÏøWW\®|A»¶÷aúÿ\x0000uTØQE\x0014rÚ!ñ\x0006ÿ\x0000öÑé]MrÚêÕÕ¿¼ªOçÿ\x0000Ö®§¨¦ ¢)\x000c(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000¥«Z}»Iº¶\x001fyã!~½Gë^L®Ñº¸áÐ=¯YÕ.&·° Rd?(`3·=ÿ\x0000</p><p>ó\x0016ðwg{»f9$Äy5JÝN,V"tP7ÎÆ\x000fÄ\x000b\x0007^\x001a².m5$YÇ@Û@eúñú×%^þ\x000e\x0012Gå½ÌìÝ1\x001cU6ðNCÞ\x0015aÕHÆ?\x000cÓºîc\x000ceGñÓkÑ§þG\x0005]ÏW\x0016wÒ\x001fùè£ò\x0015:x"ÆP|¹Ë×lyþµ­¥è±hÖÓÛÄN%;)·c¥\x0017F´q\x0012ù\\x001aù£Èn¯O+ êìr~µQÝåõ+\x000bC¤Y\_Æÿ\x00004\x0010»üÖã\x0007×5åc¥\x0017]</p><p>¡ZUSr¿\x0012X$) çpEiÄJÍ\x001b\x0003\x001c\x0010\x001a©¥i×:éÖ3#¤o1\x0003û¨2jÊ\x001f\x000fûB¹ô\x0007?ãòoúæ?tµÍxoþ?&ÿ\x0000®cù×KY³D\x0014QLýKÿ\x0000ºh\x0019Ìè*\x001bVfÏÝV#óÅu5Ìøisw+wXñùþµtÔ1 ¢(\x0019Ìøqy\x001b\x000e­\x001e?#ÿ\x0000×®>bCþÈ®Ä©ûËwõV\x001fÊ·-	6P\x0013ÔÆ¿Ê¨¢C</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>(¢</p><p>òÿ\x0000\x0014ÈÉyþòÿ\x0000è"½B¼¿Å\x001fò2^¼¿ú\x0008¦ÎÀ_ñé{ÿ\x0000]\x0017ùTú¨ó5õBx%\x0014T\x001e\x0002ÿ\x0000Kßúè¿Ê¬\þûÄê§´ª? 
\x001dC \x0011n>Ïðÿ\x0000Xlà´>Xÿ\x00000_ë_6W¿|_Êð+F\x000e\x000c×1§×¥x	8\x0019¦¶&[¯ðWIó.µ=ZDÊ¢hò;¿M¿s~.Ñ\x000eâE\@Î%ýÆ9\x0003ð9\x001fzÿ\x0000Ã½ èÞ	ÓáuÛ4ËöÞ~\x0007áXß\x0015ô_µèöú´KlÜ,\x001dcb?Çæh¾£¶ß\x001dF¡"\x0013ó49\x001eø#ük§¯>±¼û/ôU'\x000bp%ÿ\x0000ß\x0000ÔW ÒcAP^1[\x001b\x001dDlJªêOåé
ÿ\x0000LÈ¤3#ÃIóÜ? UþuÐÖ\x001f\x0010\?«ù\x000fþ½nPÁ\x0005\x0014Q@\x0018^%\ÃnÞGæ?úÕ§¦¶ý2Ù½c\x0015CÄk\x0018Ûû²0jæÛ´eÇäh\x0017Rí\x0014Q@Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002¼¯â\x001cÿ\x0000Ùþ#O%\x0014ùð,\ü¯T¯&ø£ÿ\x0000#\x001d¯ýz\x000fý
©¡=ÃáþÙ<2;@i\x001c¾=\x0007è)è\x0004Þ)>Ò\x0013ù\x000fþµGðïþDÛ_÷äÿ\x0000ÐK`\x0003øV\x0007Ò0þ_Ö9?³íÑ4»|ÿ\x0000¬¹gÿ\x0000¾Tÿ\x0000ñUå~\x0019ÒN¹âm?M\x0000aæ{ å¿@kÐ~7Ïí\x001eß?v9d#êTCLø-£ù·÷úÌòÂ¢Þ"Gñ7,GáøÓ[\x0012õìÊ¡T*\x0000\x0018\x0000v¨/í¢½Óî-¦MñË\x001b#/¨"¬R7Ý?JÏ\x0015ñuõö{áéôøÃ\¥×Ë¿ è9üëÚÇNF+Ç|_	k+Y\x001f»|Áý+Ô4
Ium</p><p>ÎõX\x0013$c³\x000e\x0018~y¥ÍïX¿gh)÷4ª°@Òn3ÝqúÕêÍ×ä\x0013/=Jÿ\x00001L\x001f\x000e®,$oïH@+b³4\x0004Û¥©þó1ýqý+N</p><p>(¢2õõÝ¥ý×Sý?­?C é1\x0001Ø°?¥Öv7¶\x000fäEEáïù\x0006ÛF§Ð]MZ(¢Â( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002çüg«É£øvym¦HîäÂC¼\x0007¨\x0019¯#ûn¿~\x0019Î¥p3(îÃô§n¦~Ö\x001cü×·SÞDfGU\x001e¬q^Iñ6h§ñ
³C*H\x0005¨\x0004£\x0003¹½+m?Tåìïýèÿ\x0000J`Òu\x0011ÓN»ÿ\x0000¿
þ\x0014Ò)³Ö>\x001eÜÛ§­£iâY\x0003É.3÷jµ¢.íbwÏÝ
úµxéÒu\x001e¿Ù×yõò\x001bü+¢ñ4ÓÛ[iâ\x0019d91±SÀ\x001eX.b|bW\x001a\x0001-§ú$p*Úº¾§Ï=w\x0012;t¯Uøq¤Ï£ø\x001eÂ\x000b«"æ@ÓK\x0019ê\x000b\x001cûã\x001cWÁ¨­N\x0006¼¹{"T\x0012	\±UÈ8çµ{xACÖôÕ#¨k¤\x001fÖ¡6Û]g\x0005\x0015\x0017}ÍJFû§éXïâÿ\x0000
 ËxJ\x001föù\x001føÕY<yáE\x0004\x001f\x0010Xtí(?Ê¯]î?Ä^\x001eÄZ2Ám?s\x0015Äm\x001c¤d\x0002r¼û\x0012@¬?\x0000øÚãA¿GÔôÝ@³>Ù!Ý¤hä\x001c\x0012\x0000\x001d\x000føWm¦øDÒ\KPÝ'^/7?8ëÇÒ´OÄO\x0007©Ïöí¦}FOô¡Óo[\x0015\x0019´îtêÛÑX\x0002230Eex?Ùþº/õ¬ñ3ÁÃ®»\x0007àöZ«yã=\x0003^\x0011Ùéz\Ï»yEF\x001c\x0001×)òK±7GO£.Í&\x000fpOæI«õÄÚ|Ið}¤VÓkH²Ä»\y2\x001c\x0011×øjoøZ^\x000bÿ\x0000 Úßø=û0º;</p><p>+ÿ\x0000¥à¿ú
§ýøÿ\x0000£þ\x0016ÿ\x0000è6÷â_þ&e>Ì9Òê_K¹QýÂjÏú\x0014£ÒOè+\x0012ãâg®-f5¸÷:\x0015\x0000Ã ä÷i¶.Ðü<^ßVÔ\x0012ÖI0è¬r:g}(äÖ\x000b£¶¢¹Qñ'ÁíÓ]·üUÇô¥\x001f\x0011ü\x001eæ;mù7øRä`º:+_>\x0012nýâø©WÇ>\x0015~ Ó¿\x001b\x001fÎIv\x000b£ ¢²\x0013Å~\x001d|þßKÈÿ\x0000Æ¦_\x0010h¯÷u=¾(­&\x0019£EVMFÆAï-Ü³*ëS¤ Ê:°õS@:( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x000c_\x0013øÏÂAÔob¸=á\x0002ÀO¯@\x0007\x001dI¯.¾øïpK
?C\x0007ðµÄÅ¿@\x0007ó¯jeWR¬\x0003)\x0018 
`Þø#ÂúMÆbXõd!?àÖÔåM|q¹2RèÏ\x0012¹ñÕÏîD©¶hØÖ0U</p><p>©<çßÒ¨Ýx¿QÑEÔ\x0006D\x0010qÐ}z×­Üü\x001cðäíî­óÿ\x0000<®	ÇýõÌà^Ùò5=E?ß(ßû(®Ô¡{ôìy¿ÙÉb~³}¤y\x0014¾5ñDÙßâ
OîÜºÿ\x0000#Tå×õõÚ½üïÜ¹þf½foÑ\x0010|\x0010:ÁíAþL*¿\x00025\x0001þ«\¶÷áeþ¦º\x0015|?ôÎIXo.¦`$º²z´×Sñ\x0006îÖæóNÒæ;Ø)hØ\x0011û}+ øûßï4ÿ\x0000e5ZO^)CòÏ¦Éî³7õQGµ¢ä¤¥°rÊÖ±ÆÛ\-ò\x001f2ùw\x0011©ä`\x000c\x001cUMFá.ïd\x0014ª¶\x0000Èçí_àß¤6þíÀþµ\x0003|"ñôÓ¢o¥ÌÔÔSTaQÍKrT%Ê¢õµíóèpÔWfÿ\x0000</p><p>|jó\x0006ÏÒæ#ÿ\x0000³Uvøiã\x0014ë¡Oø:\x001fäÕÕí©ÿ\x00002ûÃö&ñÍÕ½Í¾ ¸]_ËpÛN\x0017ÇWN~\x001dø¸uÐnÿ\x0000\x0000\x000fõ¦\x001f\x0000x°uÐ/\x0008ê)Î#ËÌÔ½n»/\x0017\x0016ÝÔ÷sÃ</p><p>b\x0015¥p¼^ïYÿ\x0000ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£EIS\y$Ó½\x0019ßÌ¸ÿ\x0000¼Äþµ\x001dt_ðx¯þûÿ\x0000ûôhÿ\x0000\x000bÅô/ßÿ\x0000ß£VªÓ_i}âå}vè¿á\x0002ñ_ý\x000b÷ÿ\x0000÷èÑÿ\x0000\x0008\x0017ÿ\x0000è_¿ÿ\x0000¿FkOùÞ\x001c¯±Ï\x0003Jì¾!^Áq¦O\x000cðÊM·Ïå8m§9ÁÁã­gÂ\x0005â¿ú\x0017ïÿ\x0000ïÑ£þ\x0010/\x0015ÿ\x0000Ð¿ÿ\x0000~D¥MÉKh;;ZÇ;Et_ðx¯þûÿ\x0000ûôiÃÀ\x001e,=4\x000bïÆ<UûZÌ¾ñr¾Ç7Eu)ðãÆ\x000fÓB¹\x001fï\x0015\x001fÌÔËð»ÆÓDÆxþÍG¶§üËï\x000eWØä(®Õ~\x0013xÕºé\x0001~·QñU2|\x001fñu²·O÷®Sú\x001aN½5örË±ÂR«²\x001c«\x0011ô5èIð_Å×ì	þôçú</p><p>µ\x001fÀï\x00120\x0005ï´´öód?û%KÄRî>I\x001e{\x0016«¨Ûÿ\x0000©¿º\x001fÜò5q<Uâ(Ø2kÚéw'ø×\x001fÀ­`ÿ\x0000¬ÕìWýÕvþ®Cð\x001aRGâ\x0004\x0003¾ËR</p><p>Ãÿ\x0000H|8;~.¶ÿ\x0000W¯]úèÂOý\x0008\x001aÓâï¢ûúS×Khÿ\x0000 \x0015ÜÃð#M_õúÕÛÿ\x0000¹\x0012¯óÍhÁðKÂñ\x001cÉq©MìÓ(\x001f¢ÊU°Ý¿\x0002gÜã,þ8ëñ`]XX\/rªÈßÌÒ»	|Z³ñ6­\x0006.qku6B\x0014q"p	98\x0004tô­k/þ\x000f²Á]\x001d%aüSÈògð'\x001f¥tv:V¥¦Ë\x000b\x000bkU#\x0004A\x0012¦!\ÕgE¯r:\x0015.¬¹E\x0014W1aE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0007ÿÙ</p><p>endstream</p><p>endobj</p><p>168 0 obj</p><p><</Type/XObject/Subtype/Image/Width 405/Height 71/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 4481>></p><p>stream</p><p>xíÿK\x001bI\x001fÇÿ\x0013ÿü² ,¤äÀR¸óü%Ëó`ä\x001eò(åô¸\x000bÊIkÃãºW¸®\x000f\x000f!Ç\x0011\x0004ÓÚ\x0006!èñØx\x001elÁ\x0016KlyÒ>eEYAÉH\x000eq¹ÏÌìÎîì×lb¬¶|^H1ÙÏ|æ½óùÌØ³3\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000NðÇv1Í¢ÇÇÝ\x0016\x0000\x0000Ðì\x0016¿tuuEþÝþã²Û\x0002\x0000\x0000\x0010cù»^Ð.\x0000¸\x0008\x000e]\x0018i3ø¶Õ)!ÒÕÈnvv\x000eî¯LÅ#]ü@öùiGë
x¢ÑáÁâaÛul> UÜ<G\x0015\x0000ð³[ü;&=ÙmÛõãÛ]\x0014aN±÷Ë\x0004¹\x001ezF8ù:,Þ47ö´É\x001búô®®Ñ¥w\x0014º\x0008ù¢uFþa\x000eÔ¦ÔåÉ`qÿÜ]\x0000÷íDÏ,Ù¦Ú¦ÈÌíß}¯_X	'\x0007°új\x0003?ùbê\x000c!_Ê</p><p>NægæÚÉæ§,\x0000¼\x0013Nÿ=¥;ýÔ¿Ùý2{\x0010iùn;ÛC.þ½¸\x001bî\x0011!åëÃá"äëxeÂO¾zFD}ÏÑøa\x0004ç¹Ôþzì<e\x0001àÝ@çÚõ\x001f­ðqwÞ¸v]Wªd}w¸4âb\x0000òÕ\x0006®Ü×¦ä¬ÊW@~\x000cä\x000bøÀ¡«)k\x0016ÐÄWOvÅVúË{µv(ÏÜ\x001e¸FÂÐîO\x0006'r¶Ã/ÙvÛôôçmTåè}¼)ç&\x0006>"\x0007\x0003>\x001aA¥Aàæ
]|ïØ%[½TLÌL\x001dU¹ÍgÙ±Oºípüæ©¤_ì\\x0013F¥¥ÿ6
9mE\x0006nÏl¾ð¯Öjö/&ß\x0018(_ûfÊÏU<ÀhMË\x0002ÀUáTN\x001bd§²¡P(f¤Q¤9\x0013·¤\x0017èKùô¹ÔërõÈVhIu)\x00128oë\x001e]rÝæ/wÝ°õMé\x0013×-üØ¹fð/\x0006Ú;ãô^)(iæYÄQm;5»äk[Øzq.ù</p><p>6\x001aÈ\x0017ðþpø³\x0011\x000eJ/Èg*Y\x0013¿\x001cã9¢O;#ýåÚ©üßÊ\x0004¹!\x0012\x001f320éA²Âè\x001a "sÈÌîS$?35È\x001bW\x0006\x001e:nó/£òïÇ\x0004C\x0003¬]ãß%r±{0.~mÜ\x0012y@«	¯Èµ\x0011Rjî9®nûG]ª²\x0019q,®÷M}d\x0016Asp\x0014Hte4¿åC\x001cðÎ}é}9;ÞC\x001fo\x000f;®|g|»¢0Z`Y\x0000¸ZK¬y¬$»\x000f\x0005còíYk³\x0008Q\x0015vaFÒ±\x0007Ö\x000cHk4·o®¾Fæ½VM\x0011C¯|åë\x0013ÉÜD¡kÄ®E¤¤¼òÒTÓIrÇ_çùÊ×à\x000c\x001b¾Ñ®]3\x0004ü|7¢[FüÝËn§²\x0018q¶\x0010]}óp$ÂÊW\x001b5·$_vl\x0011k@þ*ØhÁe\x0001à</p><p>AIÜFÃ¥/õwº±¾:dÓ_/µ\x0018=JAoöÆO\x000cY5\x0007ä¾Øù\x0018\x0015ÿãøð¿òjq*a{ºîË^\x0005í'ÞIxZ,S\x0019\x001cl£æw _ÁF\x000bS\x0016\x0000®\x00044W\x001f¶éRÁ</p><p>¾9º\x001a;¤k­ëÙúwÖYS\x000f«/×Î£1A\x000caiW¾Nß<F>r+DòõÜ'ÓFð^#ÙÛïÛÈ6jnI¾ÚÙylf´ ²\x0000pµ0cÀ¹Çî\x0015Å6M\x0015ÆQ|:9]}\x0005\x0001»ÐÕ×nDj\x0001±¸"¿Ü=>>¥±a«/?=ñ ÅÕW\x000b5_°|57Y\x0000¸r<7¦Øõ\x001eçÆ"þêîÖoºm\x001d·ß}¬'x{¥ß)üç®üÌÒ³sæ¾\x0002åËÖ\x0001k/r.\x0008[/ÈÂ{¦Z_ÈÛ~ÇÎ½s_g»óÎÜWË5wX¾ÌÕ²N\x0008£ù\x0005«\x0007=ÔmÀ¦p­?r4\x0010\x001e²*$\x001bÉô®îÛ"³«\x0018\x0011¾õÙÉì<F®´¼ó\x0018F¾ÐBlüM1\x0001Qò \x0003F+?\x001a!µÑ-9~lÎçkç1;uÓcç±ÛÞy´º7Ï\x0018Ç§æVeyµ(+áæ[\x0016\x0000® ôDî±\x000fìq\x001eMé_:R=§/³\x0003\x001e¹éÈÈCã|é¡÷1"Ls_ÁÁ£% ô¹ôtYËò°2é>Â\x0016W¢ü?»;÷ÕjÍm§î]+g[ót#47Y\x0000¸Ð¿ÝÆØNÔ/ù\x0018¯¿Ô>~³ô`LÐ_âúòÿX7Q]\x0012Ïf&nöê«\x0016NÝ7IÝ\x001fo?6Nw'&f~?n3÷e6ÃÖÈÁ|ø§×}lçÍãô]Ý½£Rñç¬çöhK5wH¾pó63c½<ùïy\x0011ÎhAe\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000 Ôµ|æI¹vÙÍ\x0000\x0000\x0000h	mK\x0012âR¹~Ùí\x0000\x0000\x0000hZùI^¾\x0012ÿ\x0011\Eâ8ië²[AP\x001e%¸x^étµi.µØE®¶!õÅ¥ÊIK|?'Ì*í=ñlÒ61ër:Ê§û0^Àµ¯®Ê,¸(¶$î«ÐÓ1H%ÃsRE¿|°âXR\x000b\x0007\x0017ÒØÐ\!ù:khõÖ!\x0014\x001d¯²\x0014O-´ñÒ9©kv\x001fz16i\x001bÖZý\x001cýºZ¼\x0007òUß*d~SÛ/ß¶|aÉbåk¸ðº^?2~¨\x0003¨«ÙB%Ì«lo53\x001fêÆp\%ùº\x0018:&_hºÖµ\x000eÔó>ÓÁ¥ìUâ=¯Úb®´_¾còå¹âB2\x0012n%ÖZ3â#_
UNÝr\ôFò^IõzÉª¿¦\x0013äÉyE\x000b,|~x¶\x001f½Áã>ÖK·lS@[\x0017ùOsÕ³kêúG+ÔX|<o</p><p>ö,áz8þã¤¸ìó2ªsä\x001e®').*2;ãö«¡®~ õO\x0016Þj^¥\x0016\x0014c9Dx¹û"n¿1+×Î´·IÜæ£û´\x0001´\x0008i^,).¼µôÐêoR,íÑ«MìfÄWêÂd2æ4ÑI5ÿ\x0005¹d/Gñ.E¼´´K\x0019í7»iÃÙ\x0017Ãs´ê,±\x0005qxÜø¼¼(&{°éR?k¦Á;\x0018µÕ×B\x000cå$zk3·±î[¯ÙJmy|Ä\x001d\x0014\x000bË¤1N\x001d°òô1OÇ`ð\x001e><MÈ\x0013\x001d\x0001W£^$×cÂ×Ö `ó>\x0017îááá?Nå6,S»C6	ÈÒ¨Ò\x0007æ\x001a3¹|îm¦òFE·-r²o¡q5\x0006\x000eõÎæ"\x001dx_xÊW­4ÊÇnå+{õú^%+ÆßYuvt$ÿªVÛ)IÉÔÂ^P)ÒlA\Vj\x0007jM;«/32¥ïó}3UÃ\x000eôººâ£ÉÌR;ª)ËR"È½ÒÎ\x000eJ©hl|¶¢\x001eÕÕ­üx\x000f?ù«ËôG«Q>ñm\x00015£¶S.ÜMðQkÆ5í\x0017~Ç}¯\x001eà&G\x0017TW©Ü(OK\x0011§B\Wë\x0007Õ»\x0002?4ì\x0017K;µú,Æ9AïkÊsF¿Ôr6ÉGÅ2ñ<íU.\x0011O\x0017¶ÔúZIñq¢çgNùbÍ¨U2B4!-&\x0012r¯õÛø¾{«*ªgv<9íÜ\x001dò+¥§5ø¡Û_Î\x000cñüý²{RxÊWý×I>.ÊÈà¯</p><p>©(|T­\x001fiFãQï±xµsÉy5¬\x0019¶J¤çõá. âB¶¢¹Ýc-ò©EÕÑ*çG½£9ôPõÀ9ìÌmÞ>æå\x0018UýïuN¦</p><p>¯\x000càî­ÖpÀ¥U²\x0002ß/aW9PJ?$Ìûõ!&]®U\x0017Ó\x0002,\x0010%D\x000bÿêaî¾ll\x001e\x0013¥¾zçûI\x000eò<\x0012::ïÓ½
Ââ)_
­~$fPßzµÕ;±dVV\x000eÐ\x001c,q:OOêõ5û¼Pµ\x0005çÁK¾^çú>*¦ïÈinÒé^û\x000bÃÒ^7Bx¤Xeë«¦\x0011´²\x0018í3f9Uë«éh´eÍ\x001e4|èßêL_ß´õ\x0004m-Í¹Ü\x001eÝÃÝ*Y\x0017\x001b*\x001a\x0008cÆèZ\x001cîû©JËÒ~QÁ\x001cÆ¹T	×8½F¿@\x0006á\x0012ù·ô¶
ûÜprÇ·4ª¹O\x0019ã[£\x0006eØH²Ùå1#òOÛ"VyÐß\x0002å\x001f¸ñeÚ+§ø"Í\x0015×«\ùÎeð/M¾ÇÏ4ÓÖÚ\x00065þ³¼BÛ`½¶Â8ÃVBRw\x001bâ3Ò\x0006ã\x001e\x001b\x0012\x001d£`ùb:èz~y8\x0003¯áS$\x0012O\x0014ãòåÞ¬\x00084üg}ôÕc\x001bb6Nq\x0006î	È,Ì¬\x000bj1Õôé\x0006±áHÝ[íq\x0005LpË(\x001b\x001f.>xÄsâ\x000el'býùuUWÑR®5päøYAqt
ý\x0012Í¸æc	Mp¢fÙCúôPý:©dúc;ùò¾ÖÌ\x001aö!v¼ðÂÃþ>\x0001ëcC«íTÊËÌ\x000fã9(vùbºV\Í2Üi¿4Þ\x0013\x001b.U\x0016\x000c*ÅÆ\x0008î.c2Ç£)mÐ.¡uQ/vèÇp\x000eæAêÂçäÛ=\x001aeÓç`°|yôÈ~¿¹\x001cÃ×ð!1\x001c.Ò\x001ajöhÉpo\x0017úýÂ~tå¾\x0013ÐÖÅsj°Ëçé^\x0006±ãHÝ[ï\x0002¯Ü×Z]\x0017f3é!ÞjÌ»¯oJêµ¿à·ÒÓö+o\x0013±¡|U\x000b*åÎ÷¢p\x0003­U\x00129Z¯§\x0010ò5¹¬²õ»réÍä+L¿\x001a\x001a\x000eUúcÉYÔ-Rêìå²\x001d¯Õtb<» ¯WU¼\x0014\x000f#_BnËÖ\x0017Ë\x001aue-7Ü#¤sx©öåëLOò(jàG.ÉëÔZ\x0001òÕ| .M¾|}Ìî\x00186|\x000f¿õãZé\x001bÞQûÿ«)òEêg& ­?Áòåót/8º\x00192u¯U\x001f
ß\x0018J\x0017Ë\x001a\x000e{ß¡|éám\x001d´Z¦Nå_Êc»JCC,¼&ÿºÓÔ®àñLÃ¿£w\x0019ïP\x0012WÃÁ#zÒ]&xlÚ/ó</p><p>\x000e\x0006·ûê¤|¡f[Q\x0016F¾ð'i*¿Þ*G(±áv\x0015ÿRç¯³º,ÞÐ_ã|"kE^~ò\x0015ÎÁÚ\x000b\x001eq\x0007Ø¹"E\x0013 \x001e9úâëcnÇ`ð\x001d¾R\x00182V8±[t\x0002oI£Uöî7/3\x0004³¢\x0013Å\x0015<â(Ø</p><p>\x001e½ÎÐ|
[gð#¬8\x001dEÐ6ùúÜ9<\x0007X¾Ä5\x000eki\x001fÊ^áTdu9ìIìçjËã±¡LÙÈÖ</p><p>$çã[Êk·\x001d'LÉ$YQüR÷87{#Ôì¤"Åùd¶TÅ)ßj)¦`R÷õ½Já®#\x0013ãéMûU+Ý%³e8}âó¢¤T?MÌ.J´T'å\x000b-`8=û½#g¾ñÍå\x000bÏ#dùô|$HË¨§7þYÑ´J..¤\x0017«µ#U¾/ðw])%ÏRgç/4y\x0005d´=EÙ¯Ù^å~ò\x0015ÂÁÚMÝ}h*GRÖ¥ûå`áäËÇÇ<\x001dÃÂoøpq§¤ì+Ê^­ÆX\x0006·?.¬ö¯£®\x0011÷\x000e/Ôw\x0001ÈÆ×\x0004daR÷ÈiçÓ\x0002ÇÙ&×Ó½
Ââ{î\x000b§éû2\x001e©:y¿ð©'Ø	+¶]\x0003=u,k¸Uµ#ïÁh\x0005g2¾5jåY}k%'=N¤\x001bßäp\x0002=8á]Êó°\x0010^WsæV\x0014Áÿà\x0004ÝAÆ"òú,zÂ7>'å\x000eN4ë\x0017Ý4·jð.ÕÑàñD)Ü1+Kaä\x000bÙðmIo-Þõ;=\x0017aåpãYê<òUF\x0017_:=ã%×¾ócÓhóà\x0004î¢\x001fÕÀ\x0016`N\x0005¯3\x001f\x001fót\x000c\x0013¿áÃ+Fh</p><p>¦,\x001bíç?NIkªË¼îôtJt\x001cgÐ<' KÀÁ	§û\x001aÄ$àÔýþª¨Æù	Û¸öL2OËT¶H$åÎq
\x0000:C£Ö{V¤ß¨§\x0005Îã D«¼\x0007GI@1sYxF¶ÿð\x0011ÇKl\x0011\x0000\x0000,®UöL4¶ØÎÅ\x0007 _®ý¸BÂcO</p><p>\x0000K$:d\x0011ÎDå{øÔ¿Î¿¹ô\x0001ÈBGán¡¼Sd×\x0017Ø­
\x0000\x0000.rîëþGC®LTÛ|\x0000òÂÇêÂ½a¤øð -VÙô\x001d\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000À%òÇ¤ </p><p></p><p>endstream</p><p>endobj</p><p>169 0 obj</p><p><</Type/XObject/Subtype/Image/Width 273/Height 158/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/SMask 170 0 R/Filter/FlateDecode/Length 901>></p><p>stream</p><p>xíÛÏÜc\x001c\x0007ð÷ìÎvwfwúCtm¶H[Â\x0008±Ø\x001eX4A¤\x0007MI	MpÀÆ¯ÒÆ¯¢]ãäâàÂ84þ\x0001\x001c\x001d\x001cz\x0010å?ñe3ûíLÄÌæõÊ=|wgd3ï<Ïçy>MÖ\x001eï%+Éöl¤<©óé\\x0018h|¹»3ÙØð­áðQòñ\x0010£NúLP}Ú¯MãÛÌý\x001d\x0003*2÷¤)2!#s&9Ìö úÝ\x0013¬>ù¿¦#2¿a"S½ö¹ä²MçhõRÓ</2l\x0005ÃDæýd9iÖæ`&~\x0016\x0019¶a"óNr}2Qg«\x001f\x0006*gD\x00113Ld>LnM&ûO0===??Í=ç2+2¿!kûmý'h·ÛËËË\x0007n_ú*maüÕL7]âtÿöðéþÇe«\x0016\x0017OfúÂÅ3"Ã©\x0019*)ÇGÕäµä­RûW¯}#¹©9Óh4:N³ÙÜÆ7\x0017¿7\x0013\x0019FLÍÈTI9P"s[²?Ù,&w&÷&×Õ<4k'¯fÈ0æ6L7y1¹#y$¹¯×ü\x0013Éã%8SÕ¶+ÙYnø7wW&ÊvaÌõL·\x0004äPé"«\x0016ù²VTËÊÃe¶ZÒ´¿fd¦ùZ±×?2U½ÿzéù 9,ÞË]ÉÞ²I;^NÌæjFæD¦\x0013\x0019Æ^ÿÈ¬?è&/'\x000fÅ¥JÊ3É¥Uf)¹¼Ô5³É\x0007§zze\x001a{Ó¸¢¬O;df+¨SþwËÉØ©2N'ï&/¼,ô{û´Ë¹Ùº;ÍV/c¥ýeZÝLWC\x0019[BÍ\x0013³WJÇòS¥´9VÎ\x0001\x000eö</p><p>úÞÏ'Ê!À:7¤ñEZu/\x000c#¬NdÎö:{¹X-;´#%&'ËrS­>Ëöì\x000eeê»A¿##2°:Y+wgJvNnÌêÉÛÉceK¶sÃ÷½%\x0013dæÇÌ
pã/2°\x0017ÊÚQ<_ÆÑäÆäÒ>íd_&\x001eHólf¾Nû\f\x0007\x001b¦U¥Od\x0018\x0019»\x0006\x001a³60ÿ©JÔ%½\x0013³ÆÂ cw\x001a­ÿú\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000Àz\x0000û</p><p>cX</p><p>endstream</p><p>endobj</p><p>170 0 obj</p><p><</Type/XObject/Subtype/Image/Width 273/Height 158/ColorSpace/DeviceGray/Matte[ 0 0 0] /BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 9087>></p><p>stream</p><p>xí\x0007\ÔÈÛÇ­ì\x0002K_@éHQ±cAEADa±b÷ìgÅzö½z"*`ÇÞÏ³ã©\x001c**Øé,\x0005¶eòf,,²ïÿ¼;9á÷ùèf3%ï&ó<óÌ$È1*oP\x0012Ì/©ü¦/|§Râ\x001a\x0004JÇWe`¸¦ÕÎð.°~\x0001©ÜkTAgê\x001bE}\x0007Ýiªv¾ü©Åõ\x001dHÙd-õ,ýeõ\x001dHn S=K³ú\x000e¤|4§:KÇÄú\x000e\x0004[¥SÁ`ô[õ\x0017\x0008PÈ\x0001ñqÁ´:ÞV\x001b°ú</p><p>Dñ2æÁËtòã\x0010VU\x0006	ÇùQ}\x00058%f¯[ë¹ü¹êy´×ÔO à÷IÑ+®¿ïÎÓ·¬q¾\x0001åõ\x0012\x0008x³¹øa}/\x0012zÖ°»ãåõ\x0012âUeÙ)/sÛ.1ÏWÕ\x0000²\x0001ÔK \x0012<[·7æjÆñM[</p><p>-($ºM¬¬®~Ê£~\x0000!n\x000fyy¥ùÇzôô\x001f1\x0007Sù/Ü)©¯@ðg{Ï½9¹|ñ¼Ïì´"S[_«=Ò­G@\x0014Ç÷<L:ó.ÿã\x001eG*uèk<ê\x000b\x0010yz¥T#Ï<2\ev;\x001d\x0013×òR¿s ÷\x0012kêÁ½è\x000eUnKè/æ:Ýé»\x0005bû©llõtÐ¦V\x0016[[Kþ7jn\x001aÔ \x0006Õ#1NÂïÖþü\x0005qý\x000eßXaúå|õGæ«²fkëVÔ%5^xùX«oÝ¯®@ MÝõ¨@ Ã >y\x0002\x0001\x000c©²\x0005\x0002\x0001í²ò\x0004ºpb£+ ÇÀk^úÄ\x0006(®\x000e\x000bai\x000b\x001cºû¹	\x0004|\x0014Aµè¸tN]\x000eR·\x0015°ÛÜò:°Ã\x0016AÂO\x001dób ì§\x0012NÏj\x000cS¸ó\x0012\x000e\x0004\x0010!±	Ó\x000ffMwR^<\x001bÀe´:P¥ÈvçfjóD¸\x0000ÑtØ:\x00199Þ¬=4J:Ôý¹¦Ô
åbXÑ*}bC'ª\x0012S>w#®úãrIo&¢5Z)Ó\x0006ÁIMþq,s</p><p>ñ9¯\x0010;@\AÎ1Å\x0000Çìõ"=ÿÌê%\x0012¯\x0007 ~©ÍÊã&én)±¥¬H?æ
¯À\x0005¥TRÞLî¶çKãØ\x001fAD³\x0000\x000e^´$TVô!!\x0006ÂÊÄ\x000e\x0002ÏJ|\x0017ã\x0007\x0011D0£\x0014¼Þ±.Y\x000e\x001e;õ|.\x0016ç\x0003\"\x0016\x001f\x0005 ~OpI21ö»³Ö\x00001ci\x000fU\x00030¶²P\x0017Âaá¡uü!\x0000é\x0001\x001bÄâ´\\x0003\x0010P¾H÷S Ö1 `¦\x0001×îø³Ö\x000c±©©ÝÎr|©©©\x0011\x0017\x0002Ir×ÑÑÑÖB!\x0010ùP=Ý\x001f</p><p>ÁÓ@\x0004 \x0003êø\x001dB\x001c«5=\x001bÈ\x0014\x0000QVÈð×m\x0019\x0000ir</p><p>Ï\x001dO\÷æT
Ú\x0011\x0012|&µI\x0000yÜ®\x0018\x0002	f"æ·ñô±(	ää78½ÿ]b¹¿\x0004»8æR²¹à\x0013 .KÁaóOnP`UýÒ5$y</p><p>H#C\x0002	Õâ¸?\x0007o#$3ÐÈÔñ\x001e\x0004\x0002y\x0015zFQú±\y²s- »Ç%c¥£¸5p\x0002+AñÑ\x0001VôTEM 9û""Öÿ¨G\x0002Q¬î7ðByÃ\x001b!¤EDD¬è£õÔ\x0015ÁË¶RîãK- ;íÁSÏ@\x0010½\x001fî\x0002 9ãG9%5\x0013\x001a·,I \x0000Sb@6\x0019º®\x0004\x0010¨Ò5ot¢ÿ_\x0011@<,7áåk\x0004Ík\x00031t¿ WFÖ\x0004ðºmN$¤\x00062à·@$ïÞ½½SH\x0001\x0011gÊAájr½\x001a\x0001¤àîÝ»W'ÖuÇ\x001e\x0002av<zÌ\x001dÕ\x0004=ô\x0003(\x001a{ª&\x0010â"éðóS\x0005¸I.Ý¬	äeOOOG\x000e	D¹iä¯ h\x0001L"Ü RZ6fjjE\x001d\x0012\x0004h{\x0005zð\x0010M@\x0010½\x0015àÉ\x001f50+Cot6.ÃZ\x0019v,ìÕ@èyü¬ÌK\x000fzS#\x0010¤}2&¯P\x0007ZèBØ</p><p>×T¼¸3,ö§f·N*;\x000bG{ß\x000f\x0010Îd8Y
\x0004µÛ8·µÛê"ü
yò5¼\x000f\x000f\x000b\x000bû¡Ê\x000fq¼\x000c·Y@\x001e\x0011)aC\ëø=óE Éi \x000eÑö\x0001¦ÈZaH§¢&\x0010¹8;;ûã>#\x0015\x0010NP:ø0\x000fT\x0012)Ù/&ÖqOäË@\x0010¯\u ï
9\x000e\x0000\x001f0&Õ6»¸ì¤</p><p>\x0008b°XýÞA]<V\x001d\x0007ÒOÔ[Þ\x0014\x0004ü\x0008×^\x0014l"\x000c;Q°'5\x0010ë\x0010\x001aÚ×øt</p><p></p><p>m\x0003¿\x001b¢nÞþÅ\x000eu0[\x000e\x0008¥§Í{</p><p>nÏA´Z3¢Æ}BØÍ\x0007PIý1þÕókP\x001aÔ \x0006}K\x0019\x001aAésTóml}#Jºª\x001c\x000c\x0003#\x0003ugEäÐ«^é0tªÅC\x0011\x0001Y¡ºqe\x0011»TUÀÜ\x0006,Õ¡\x0004ä^vS¿~>äNvUEd\x0016Mç~\x001d\x001aÓ­G6®	\x0007¢¶Q\x001db\x000eÐ °9Ð:¢|µvi£¶¡j\x0011n^ýû¸«ÆÝ0\x001f¿ªÊ¨xBq¶Mñ *t^\x0017OêÈ<Uà¢ñÎ¸\x001d6jçï¹'>~{jãi2+6^¥Ø`mf8YáÑMTYP¯
ññ¿´¤¾6ú)>þ/y\x001enâ\x0017YÃ</p><p>fOz\x0018?ÁøQ<\x000eÓ5\x0005\x0012D.á§\x001e<{vïØtjÅ[Õ°êèU}ÈS1\x001f\x001b\x001f×Lh²,6þ\x000bu4Ë%qññ
½\x0011jí\x001aoÈ\x001cs0>Ì¡ç¿õZRÊ\x001f7vö×#¿\x000f>\x001c\x001f\x001b®OV9ïpl.\x0019\x000bWVdÝE\x000eÓ»$QÑqù9Õ\x0013\x0011N\x001f°÷îÕ@x³Ê1¬dvõó\x00126'Uwå"\x0003ÖyªÂ÷<U\x0011¤©y\x0018&\x000b§|\x001aÇc\x0018¦8o\x00017{¾À®¶ \x001c½ÕY\x0018\x0003ùM6(ÒGF×40}/æ)á\x0012Yeöé\x000e°ïC¢(}²ÄøfqQa§`\x001cSkúG¢Á]©£
H!ò\ ÎÏt¢ª]¨Æì]eØRò'$µ§Ë,áR\x000cK\x001b\x0004¯Fçe</p><p>1P\x0014äæ\x0016Ê\x0001V\x0010
tIÆKïÝ»wg\x0003O\x0005ð½Õ_%¼TpÖ®jåìÜÜ\x0002\x000cÈóss³Òc]Ä±÷÷Ê=\x0016T\x0006ÇX%Qâ~#êËq¢-á\x001dÚë%~Ý
A:\x0017â#ËÏb/»°>r¬à\x0011qø{Cµ.Ï\x0014 ìqüñ\x0014)P<\x001e¡ïïxyÒ½7Jìãxâr¶¸¤$\x001cß\x0008ê­o*p\Ñúù7\x0010\x0007Ë#¾,ÏÊÍÍW\x0000%l×Fsön	¾È \D\\x00039cÎç\x0002L¼\x00066j\x000c\x0007²ËÎ\x0010È\x00059&\x0006o\x0002lí\x0006*\x0005\x0015\x001bÙ$D_SBúª^¥&\x0010F·|ìC\x001aÈèUÕ°Lmmm\x0003Ê°'ÝO}\x0006\x0001DºÐÔjÊ{êCÞ%ÌÀTðòBÒ·\x001a\x0008Èð¬\x0006²\x0018ÈÎXèX¯|0¸\x0013úÈå\x0017[ÂÃóQãJeÊ(kC#Ûéb\\x001egB\x0002Iéhj\x0013\x0005ä1h ÊDwÄàç\x0012P\x0005Äë\x0006¤mf"LC¢==?\x0000qoâÓI\x0003Ñ\x0012½\x0007ñíM
Ý\x000fÉÀ»±Z$\x0010\x001c\x0014¬ä«Pc\x0019ÝÕ\x0012PÑ\x0004rÇ\x0003QWM Z@ñ®
¥Ø</p><p>\x001aÜK°ûÿN\x0000© .	xA\x0008	MLºl[\x0001~A\x0003J0ü¬n\x0015M¸4NèÚ\x000can\x0002ÈiúÂWAÔ¯2\</p><p>²F@\x0010¤\x0004\q&`\x0012\²KÇ?\x0019Èd\x0002Â\x001eV%ÛS8¿\x0001¹-È-\x001aÝqb\x0010F%G*A+	¤T\x0006Rüj\x0002AÌo)ñm\x000c\x0008ä^[.[=T\x0013í\x000bÒ@</p><p>Htª±\x000e¤&\x0019LV§ßð\x001cêÑ=§àm@g Ã\x0006½5\x0007M`¨Q\x0002qx#ÚF\x0010@ÎØ\x0011g!¼[xå6ú¶å\x0006\x0015¿è@ O]ìÁ2ì¬\x0003	D¹²\x0010¤NË?UR@Ì\x000fÈ¤c-ïÂ±0|?çTè\x0013at|¿
e@ çÏbÒýV5 \x000b¥ø
#\x0008$#zÝºuSªÖ\x0019Ö\x00042\&?mípTQ6´Æ¨µ\x0006\x0010Ùn¿¡'ÊÁÝäÉ\x0004±\x0004G£rlº</p><p>HïÝX\x001bJ\x0003±|¬\x0004÷&Ùq) Ê´]Äáýù6\x0019  DUý\x000fâº
\x0004òv\ï	¯d>\x0005Äo\Y=\x0018|\x0006âó\x0018¼òd,ÆdÇ\x0004\x001apFxU\x000cËê (É@\x000eû}\x0000\x001f'ðj\x0002	)Ç\x001f[C ¤\x001e\x001ak\x0004Â?\x0007òæ±xsrÁaágPË¢ß#Û$Ü\x0015-ÒA'\x0017\x0007\x00064.Í\x001fò½F4\x0010Äç\x001aÑ%Kï6A!\x0010ªtK)Èj«ª¾\x0014Kt@pÒ<ÜèP@z¸ý\x000ep7Ùå</p><p>\x0005Dwfr\x0010i)\x0006©\x001d5\x0002Ñ¡TìP=Åo¼</p><p>T,\x0015@ 1\x0006K%ØN5üP'Z@ eÏ\x001f>|\x0018­¯\x0011H\x001b1H×µë¢÷øªÖÖ\x0002\x0002s*ñü\x0015$1×3<cy·®óÄW\x00055¼\x0018|\x001c\x001c@\x0003A\x001dÞ!ìkæd§</p><p>þ \x000e?MÏ©\x0010dwVUßMÝw@ä¹\x0005\x0000{\x001eÈR\x0001áM,Àe',i Íâ0év¿®}^àEó9\x001aLU(ö4¦k\x0015n\x0000Åº$\x0010FËËÊ²
\x001eê@¸;dø)]\x0008$i§§g³*çT\x001d\x0008s=\x0006d¹b\x0019®XòY òÃS.(ÄKÉk?­\x0002ågfæÊ\x0001ØÆ¥0uö+ä\x0017æ¾¢\x0010\x000e©Û«\x0012ÜA\x0000QüêG\x001c¾1Óì\x0015^ü#íÛ¡ó1ÙYs\x0008$=|a>öÌ©\x0002Xízu]Ä¡°_ãÊÂ¬ÌÌ</p><p>\qÆ^\x0013\x0010ö BpÉnt³óxîD.	\x0004á\x000f~\x000f^Oûµ\x001a\x0008£K</p><p>¦~ÁÊ4N\x0001\x0014\x0006î\x0019~\x000eHå4­þ¯Àó~Ð×µ8\x000f09U\x0002OrR\x0001AZ?\x0005âûÙ\x0014\x0010&qz¼\x001ew1É aÇ\x0000ù	ÚÛqx\x0004×p)+#Ø.¯8Õ¬</p><p>\x0008Û)¸1B\x0003\x0011®®\x0004ÔÁ u ª\x0001\x0008êý\x0004OD
KxÃ³Àã(\x0005\x0004±Ü]®¸ûVA\x0003AB®È@R/Ý¡R,í§qæ¾Põù<\x0010Äde¡â\x0007ñ\x0003ûåcÉ`É)xádT\x0005;¡\x0008)H ÜQã\x0006Z\x001cQÈFpÕÍ®¯\x0018äE\x0010Î+qKEËAr'Ùmò\x001b(Xa¢\x0002B\x0002¶¹
26ÂM<m5Ô\x0000\x0004\x0011®©P&\x000e~6§ÿ}L²Õ\x0002¡0»ßÆd*\x0006ùË­Q	2B$´ÃÂÂFöPy^\x0004b"Ë²e"CíC@¶GMÈ J\x0002~a\x001e\x0008£Õ\x0019d\x0013ÑnÁ*vÁ\x0012¼5@vÒX\x0005\x0004±<\x000c\x001f³ ð¦½}³±k±Ï@n/:\x0010~\x0014Ë=:ÉÏæù2\2_[\x0005\x0004
ÊÅRs5\x0000Ñ\x001a]\x0000N·äÀ\x0005\x0016`¿µÓ\x0004Õþ:&{¶q`÷\x0001ëåÊ[¾,\x0015\x0010Dv\x0016\x0015\x0003eiQ\x0011á`Ï@KK\x0000æ¤§§¿æW\x0003Á,EEQ¶^©xQ ¹\x0013\x001d\x0001>:~\x001e\x0008¢5ü%È\x001eÄ2\x000e2FP=A"ê[\x0005åû\x0002b@\x000cn_$}añ65\x001c3Äv¯\x0014Tf¥¦\x0012Ýl\x0007ô±iÇLo³\v©\x001dZ\x001bð²t>¹Ãú&ÈÂÖ\x0000\x0004á÷¬ÄJÞ½|S)\x000f\x0013«4\x0010´y\x000c\x0002¡,ôåêæd·¬2»Ê\x000bU»tú!#\x000eKñ»´9¶¾©PÎü\x0013 ñRð¼Å\x0010¹ò\x000eÍ\x0015¬ç¨ úK*H ¦qäÃ:WZ³j\x0002AÍæ¾%ÖÁRÇ~1
\x0004mñ\x001bìj\\x000b\x0008£Ík<Åò\x0017µç(ä,4\x0001A¸\x001dcÉÁ]Ùé.ä\x00060û½\x00028\x0016("\x0014\x0012à)äR5	{HtT\x0019?µGä­ç\x001d,jCïe¶\x0019 R3¼úA!Ý¨®</p><p>í(\x001a@z>\x0016½EÁ\x001e¢\x0001mUw(¸\x001dG·¨/t8\x0010Ô¼Hä£\x0007\x0003\x0018>kÏÿ\x001a;\^a\x001e\x0012ÜWU«VÓ\x0007¯_Û;öcM}E= oÃv\x000e	éaÂë\x0014\x0012¢Z$Ìë\x001c\x0012"dXô'+$[Ñ8HÔ (è-êKíB=ûÉ-^§\x0015	·Î­í¢G]º®ª³Òî\x0014"ªò\x0005\x001bÔ \x00065¨A\x0004\x000cÔ@X-ÕÂ'!üfb¨¥~°T\x0005t«âô\x0006BCõùZPh¨\x0016'\x0005]Æ²ä\x001c»Î\x0001þí-USÃÆB\x0013:$Ï7\x0016ÒF\x0002Ñvê\x0016è×Ê8\x0006CßD­Y(¢'4¡Í\x0010jäé×·»Ê=Ð\x0015</p><p>)ßa(4þËËa·GS\x001ao$X\x0016]­\x0001t²ëJøíÀÞµcÝ©(¼Í6:ÇHãæ¼4zµZ­~^¯þD\x0004³Ó\x0016ªHÔ\x0010È«å¬ø»OoÅLp 1Zm>°ÉÌ\x0018°;z*ßyeBâó¤ë;\x0007	\x0011ã¹\x0007ªZu 6sVô^*Ôn\x001c²óêg\x000fÏ®¤íýèèèÈä¦ÑêèmÍþ*<@é écP­¥trÏdò+&Í¾=Ë÷È¥sìÖ§³ø>\x0002)fÕ\x00152·\x0010ùKÔ\x0016p³Ã²¨"å £x¹\x0000KåÙG{À±%Ñ\x0002Év2T\x0010^\x0002NBH¦Ó\x001eHÈ<²·\í®*«Z-2`]\x0000¤ß8oISþÕãÙ¤;²\x000f\x0000ÅÞ°¼U</p><p>Èñù«@Ä üñ-B\x000bMM.eddxe\x000eñ©rB{>ÅåY\x0019\x0019¹2 ÌÜ\x0008kðÌ\x0003%`ª\x0008ßGxyuÖOq\x0000äçlÕÊÆs\x001e\x0010E®LA8we@rÿPl²\x0014_jO4¿%\\:\x0002Þ@á¥8\x0004"þF\x0001</p><p>®\x001f8ùV	ò7´ýH\x001c\x001f\x00032¢Y\x001f§ë©\x001ca»È\x0002}<\x001d}5\x0017(?Lì~¢\x001eÉ^8±`õ\x0002Ïý</p><p> oüm\x00080M[ÉÁoú;;;T\x0003yÓÝÙÙcðI	È' üÞ\x000b\x00160Rõ\x001b\x0000\x0019R¿N\x0003iA5\x001coG\x0014±6DZaÉ?87j>ý#(ßfM\x0001ÁegÜª0}(\x0015çýmÍ,Zm/N\x001ef`M4'¸\x000cûl\x0016\x0006¢3-\x0007oõ²0³ñ;'Ãöb@pða¸ÖW\x0003y©6ÚgùfàçÔo?\x0002H</p><p>Î´XY\x0002R[3 Û®5j¨	Dç°\x0002¬^IÖê×\x0000r\x0012BøS</p><p>ÁsòvÒ\x001e
Þ°a¸OZ\x0002</p><p>W\x0008T@Ì7Ê±äJ4Ô4¨\x001duëÁ¡\x0012Õ,\x001aHkl\x001d\x0019a¸R*w7@e2\x000cFþF ÌÏ\x0001!Æxç1å\x000cþ\x0017´~\x0001½|sÀ\x0015Ïª]j@,\x000eÊEt`É*\x0012S¬6@Ò#ÊAr\x000f\x0006Ò:\x0011ÏþágH>\x001d;rFgã\x000fév³¾Ç{£\x0004Ò3·AÅÏF_\x000b¤0~Ç\x001d?	\x0008oI!\x001eg\x0008dÅ\x0012\x0005Æêk\x0004ÂZR\x0008ÎiY%	Uç\x0004¼&Êd¸ü¿ïKßk¼qùø	G\x0008$Í7N!ß×\x0002Â\x000eÊÀýô±½O\x0018.«À6ªFv-/\x0002\x0011\x0000R²jt&x\x001dÄþ: ÔÐþ¼ó \x00132ñ\x001b¦\x0004\x0010ªÀ	U¤¶&\x0010rùHDwj,ÊJ\x001d\x0008©Ã¬V¯p\x0018ú¢N-ø#~­\x0005	¤EÀ\x000b5O\x0002Ñ\x001aÇ«EZ4\x00021Ý¤ÏVÍÞÛ\x001c\x0004\x0015a\x001c\x0008d¡Ý\x001e)vÔÚúë®\x0010iÚÓ§Ow6ù\x0012\x0010æÔlü²\x0010^!T¢ÀÆªY\x0008u hÈ\x001b/òn?%\x001büÞ£Ês#\x0014¾$Ê¬ez¦àÏ»¨v\x000fÌÀ/»@ËJÀ
÷\x0010\x0008w\x0018?Ùü\x000b@\x0011</p><p>\x0005\x001d</p><p>B\x0010ûX \x0019A\x0001aù%aÅã¾\x000eÈ»AîîîM´¾\x0004Äh\x0004ìÐ@\x0002¶U® :\x0010Á2\%ãÅáª\x0015&\x0010È\x0019?¢
Òô\x0006È\x0019NÏpéÏ-Å~±¡ g\x0014\x0015«6A Ì^¯ñGÝ>y<üS y%à 5vºgöa@Pý%¹ ià«¡Såôú\x001d+!ÎåÏ;U;J¬\x0012Ja§\x001cÔÐªp«\\x0016E]\x000cÏóXé\x001c=</p><p>\x0008Â\x001fñ\x000e¼¹]	;Uó h>UÒL_3\x0010VÈ+\x0016H9ÿ\x0006sòÀÍ\x0016\x0008\x0005\x0004q?#U\ÈúÇ BÑJå\x0005\x0007ôÏ°Çg'3§\x0012Zö\x0014¼ïË®\x0005-J\x0005ÙË-à\x0010¥Ù\x0012p×I\x0003A,vb\x0018\x0004¢ÿS!H\x0019\x0005]-N·Ý\x000b(ÿ¾VÒ!Z¦¸Ò\x0019\x001e@t\x0012V\x001an¨\x0002Â\x0019ü\x0002Hå_\x0005$kápB\x001d´?\x0007$wí\x0005+bVbOCµHÇ,5\x001c\x0016ðVY\x0011\x0002HÞ\x0005\x000b\x0016Ì\x000bÑ¶*h³\x00085Ú*.7®\x0005\x0004±ÚP\x000c2\x000fíá7õT!Èe¨0{ÜñS\x0002\x0008ÃíLùbÛ°®\x000bïg.k¤\x0011\x0008gÀ3Lz{I¿î7¥(\x0014gàÚ\x001c</p><p>\x0008"Ü\Fxô_\x0003DIhkãÏ\x0001QH\x0014@~[\x0004»u\x00024\x0017\x0016X«êä	 0KIþ!S¿Çà½\x000fyû³½\x0007wÝÑZ@\x0018Í\x000bCöZ¬\x0000¹ëáè\x0006hÏÊ\x0003$\x0010Óý²\x0014Td¤¾+Â°0\x001d@\x0010ÁøW\x0018Vò.5]\x0002ä¿vÝ\x0012
\x0004qOT~\x0015\x0010:¤\x001ecõ9 Ð#ÆÊWzÃ[ÙÅ÷èW\x0003¡ÞquÒaA!£Ï¼å9¬v¯Ô L»Å¯á:) 2\L§\x0002Ø]Q@\x0010®×NòåX üz?j\x001c]\x001b\x0008¢×÷b%9¸ËÛÛì¦U@Ø\x000bÀW\x0000éG-A\x000fmC.jÚ7´£®Z²YO(</p><p>ô¶Ò¥ü)ý@ºÊÌúR;BÚë{\éÝ¼V!!Îô\x001aAÛ¾¡­«VW º-&\x001f¸r)2ÌÚ¥×OÔ<"Ã­hh{Aùq×Ïm</p><p>²¤ïKýþ¢îtP¿Sh0µcÞ7âÌÕ£;ÑK\x0011[ö§¬µaoQh j0Ö \x00065¨A
ú\x0012Â%ê¸f¦zä\x0006OHúÌZ&D¢1\x001dãf\x001a¨\x000c\x000bÏÄL \x001aÄ;tìåëeB=´f1Ð\x0012Â\x001c<3JBr¨ÄwéÞ£M£:þ\x0010âÆÈÈÈ=Û~\x000e± ï\x0015¹c,yúí7GNf LïõDâeCÈ\x0010²ù´È5vôËy:­\x001cN8×cVì?\Ý>\x001cü²ü6G\x000e _×ÓvóÁDÎ6z\x0013,\x001bÏMxt}G¡æÔ\x0011I¿Kú&Òâq¤#\x0014Vc!a0\x0001dé{ápÌé\x0012þ±-½Às\\x0016\x001e\x0005Ã3¼!×È÷5+Ó÷Áµ÷yEøZè:hýPm'\ñ´\x0017?L\x000b1$_L#±Àø³­©\x0003\x0012Ò[\x0017\x001f\x0014Õ:¤ÿ(\x0001%ËØ\x001a0û>S`¹W÷\x001fIãå\x0007í5\x0002Á²._¸p!®+\x001b\x0019Teî\q­L`Wßý&\x0006¯ºZ8ÌÊ\x0004Øk\x0002r¸µÝÚJåms@ì\x001f`²ý¬ML-.\x0005\x0005kµ5\x0001%Ø[XX4â#è~P¾ÓXÐ|ý1ß:ý ª\x0018<sF¶\x000fð\x000c/T\x0003HKÄ¿\x000c{b£\x0011È\x001c¹2lBtÃåØã\x000eHãT\x0013Gñòí\x001cal^·_BD\x0001é¿k¡	HÞ&â@\x0013\x0010þ\x001dP°þµ~\x0007yó\x0018\x0006\x0004ù\x0019`\x0019s44¡nI\x000c2N\öP5ÑtË|ÈS,?D\x0013\x0010û,ðÂWUÏ</p><p>¼<JWS\x001f~æÔ©¸@ý\x000b\x0018âN·eilG\x0011½èNö2­	\x0008¦T\x0002p\x0003N\x001bÕ\x0006Ò²\x0018<rSÕ3\x0006¯<b¬\x0001\x00089'+\x0001t»¥\x0004Äàºý\x00191}L{ùè`Oâ7Ô\x0000äÃ³\x000fJ\x000f¼5\x0001qÎ\x0007ÉUëîfâ\x0015Ñ\x0006®\x0010ñý»w¯\x000f"úÖónæ(À»0¦Ô\x0015ÁÉ}}]É¸T0ÆëÃ1Ex\x0002\x0004²Ïçx\x000coçj\x0000b\x001cE;¬Ü8¼x\x001d=§\x0010_\x000f{\x0015Þbl+eeN7iÔÈ~Ý"Ó~Ö½</p><p>pÉæ_?ËÿAT§JÉW.¿\x0000#ð2ü\x0000ª²2È(\~ÙD\x0003\x0010&aHP«Ñ\x0019Ý3ÁÛ!\x0008sR\x001e\x001e\x0003³\x0019\x00152øª\x001dõN\x0015Ñ!üw­à?ð÷jtÖ=©\x0003±Ï\x0000o\x0006ñ\x0010Ûy96\x0015¡X!qùYC\x0012Hg>ËeWÝî\x0019 ;Â°»Ú}n£V\x0008\x0012ð</p><p>¼îÊDX­ÎbyðoÃA ªXÙB¸ü¶ÕUüc»ÿ</p><p>\x0010­Ãôîâ°iÇ</p><p>Á{\x0017</p><p>Ès·§Ù\x0010HÉá
\x0011\x0011ëÆê©\x0008VH°ÜãóF[÷Xý\x0011@ô¼¶§¥\x001bsO?QÝêB ¤ù³gÏÜ)ÜPøzÃÀ~\x0011éàcÝöT« \x001faÊÌ|9(Æ¦ÈJKd 2ÎìTB.Wk¬\x0002Zn,\x0000âÌ</p><p>É?7Â\x001a¬ÄÓó\x0015àídØ=\x0013VF^R\\ü.krT	Êß§\x0015bsu?Û: w¥NU_x=\x0013à¤âùÐâ\x000c|]VVZùë¦Ä5îxªTñ©Æ°´²m0Z»YNý5²p²_ÖéU</p><p>­øqäÜü(ªLÙû\fóõ\x0018Nø%Kmëò\x000586o¢6´`vþqñ¬@j¦\x0017ÕkêìÜ¼	ùcåLª¹5\x000b1hêL5¸|&,;>\x0011(O\x001e°M»M_:3À+6 Ê8;Â8SèÜa\x001eºuG-1Ø\x001cÎÿ\x0014Â\x0005Øö×\x0000_nw wp?W\x0003Ãaý·püeéïÏxvþrÎú"V·=÷¬²úrÆú#Ë¯ãã¶\x00065¨A
úÖ\x00177áÏjëéé\x0012öÁdÞÔÕ\x0016µÒ9ZV}Ci\x000f>\x001f7Ì\x0018ALw{iOÞ[#¾ÇoóòÙdö¹¢ß§P÷\x0013cáÜ.Êc\x001am\x0019¦Âò
ÖEø¢zÆ\x0003á\x0004\x001eãÝF6	\x0003Æ:!Æ\x000cá\x001bO²\x000fiÝ#f­³Vûùî_¬âûÑ"ø&ë7m¹7?ÞdÒÖ»­æì¼2aé¥	.}g]=ü­[øï</p><p>u÷'>,§Fê\x001a]ì´~rØ1ºÜøIÛ|þ\x0002m×E¡Ë~ë&þ»â\x000e:nè</p><p>v\x0006³\x0003c¼V\x000e\1Åô¸h¶Ú\x0015Ä\x001d\x0013á×¨.G@ÿ\x0001YF­æZ´í\x0015ã§\x0017ûÕè ¿U>mÌ\x00051³\x0011­\x0011±ÎKÇ·ô®ë\x0000åïUÓ	·ÖôµÀqVl³«ÛG\x0006ëµÞ1ÒÜý\x000bb¸æ|Xóðø%>u|ÉÏß¬¦½\x0007ôîîïÊë\x0014`Àî1¦6bà\x0017jÍ°	æ üAV\x000cçá>uzí\x0013\x0003úìäµÀ}\x0006Cµ«u 
úX\x001eíëôdÉ¿®\x0016\x000b»~²Î©\x001eß*(O×À¥n
[âwg\x000cÃ}%=e<÷Ó$¿o	&&__µödgõk¢É]\x0017Û\x0012GÇ!®\x0019sêöª°¿]-\x000cfp¬\x0019|\x001d-b¸²uØÈ Cl&É0ÿ±\x000b\x000b±ûô1ëï]Üà\x0003ÎFM\x0004lOÑÑ\x001d´\x0005.¡3\x001cu¢C´»Ï´±uxeÈ¦_®ä{Éê=F
2´ë9ózg¿®1ó:jíúË5öq[üÇÿôlØ+ùÄð<=±×OY¢xáöEà°ûðfÍá:®_Èé°Í9hy¿\x0019ùm-ÿIñF\x001d1c7â´\x000c^ïÒb}ë°uM¬";0\x001dNzkÚdo²|[=Ù\x001eËäxô3sÞÙÍ7ôdèþ½^Ã¢\x0006j=Ö¥éÆm½ÛìéÛ»~Å;¬IÜ9zÎ¶\x0010ý¾÷¢FZ4mã±NkÎ\x0005hÇÅºw¼¼¯½õÎË³k\x0007â¿g	[´rmêÜÂ1L\x0014\x0010~~±µ¥½»k\x001b=F[W®q{g>Ë©«u½tZê¦m\x001b1\x000cÑw\x0004%ÿ§þ!õtæÊiã#Ë¼ë\x0007Ö ¿U\Õðù½¯a5ofmc¯ó\Ý&Û\x001b\x000c×aÖÿ|£¾¥ø;8vÂNµ\x0005è\x000c»ÚOp0½4f:\x0010ÔôÇ\x000cüÎ£¬¨çþ\x000c9Ç ZM9öK=Ø¨\x0015e(0ÒÕ7Aµ­8ËvZãÊ`4\x000bùÂµô\x0017oH¤­©iè¾ûíu;ÏXÙÍ=âäpC×ñ\x001bºº-°(høBûöxXNcï±õè`\x001d\x001f×yë\x0016ÿÃ2Û\x001a=p®Èa|ò²ÙNÁc¢\x000e:·;3×Ûnú³ºÇ\x001e×qìáóº·ÚiåsöÇÖ\x000e3Æ\x001dø­[üÏÙ6!Øk·ßÅVÜ\x0019\x001e«'rý£<Ð±Cýl×N5a;ä2-ÆØ=b$;dW\x0013tÞ/!¾æ_®ô¿,þ¤\x000c\x0003>wÙBáÞvÝwyð^`-Ø×«±1«Ç¶Ö¨aÌpÛ+Aì[\õVÍ23<æÓ¨n?©þõjr*\x001czç®'}\x0018ÞwB¶$\x0004xï_2Âñº_¯&s×\x001a!½Î4y]$¶¯£wô¢aÎ]ý;~ë\x0016ÿ³</p><p><vÊpÙ'D	[Gÿ&êûàPKíØ\x0015znQîªÅ\x000e÷®¹ZØï8ôÑ>\x0007½«\x001f\x0016Ôõ¿Sÿú?îúÇ</p><p>endstream</p><p>endobj</p><p>171 0 obj</p><p><</Type/Font/Subtype/Type0/BaseFont/ArialMT/Encoding/Identity-H/DescendantFonts 172 0 R/ToUnicode 404 0 R>></p><p>endobj</p><p>172 0 obj</p><p>[ 173 0 R] </p><p>endobj</p><p>173 0 obj</p><p><</BaseFont/ArialMT/Subtype/CIDFontType2/Type/Font/CIDToGIDMap/Identity/DW 1000/CIDSystemInfo 174 0 R/FontDescriptor 175 0 R/W 406 0 R>></p><p>endobj</p><p>174 0 obj</p><p><</Ordering(Identity) /Registry(Adobe) /Supplement 0>></p><p>endobj</p><p>175 0 obj</p><p><</Type/FontDescriptor/FontName/ArialMT/Flags 32/ItalicAngle 0/Ascent 905/Descent -210/CapHeight 728/AvgWidth 441/MaxWidth 2665/FontWeight 400/XHeight 250/Leading 33/StemV 44/FontBBox[ -665 -210 2000 728] /FontFile2 405 0 R>></p><p>endobj</p><p>176 0 obj</p><p><</Title(þÿ\x0000P\x0000r\x0000é\x0000s\x0000e\x0000n\x0000t\x0000a\x0000t\x0000i\x0000o\x0000n\x0000 \x0000P\x0000o\x0000w\x0000e\x0000r\x0000P\x0000o\x0000i\x0000n\x0000t) /Author(Deprez Laurent) /CreationDate(D:20210914120435+02'00') /ModDate(D:20210914120435+02'00') /Producer(þÿ\x0000M\x0000i\x0000c\x0000r\x0000o\x0000s\x0000o\x0000f\x0000t\x0000®\x0000 \x0000P\x0000o\x0000w\x0000e\x0000r\x0000P\x0000o\x0000i\x0000n\x0000t\x0000®\x0000 \x00002\x00000\x00001\x00003) /Creator(þÿ\x0000M\x0000i\x0000c\x0000r\x0000o\x0000s\x0000o\x0000f\x0000t\x0000®\x0000 \x0000P\x0000o\x0000w\x0000e\x0000r\x0000P\x0000o\x0000i\x0000n\x0000t\x0000®\x0000 \x00002\x00000\x00001\x00003) >></p><p>endobj</p><p>183 0 obj</p><p><</Type/ObjStm/N 220/First 2020/Filter/FlateDecode/Length 3077>></p><p>stream</p><p>x¥[]ä4\x0016}Gâ?ä\x001ftìëO	!-\x000bhY\x0006\x0018Í ñö¡©\x001dzéFM\x0004ÿ~ÏqÝT®ØN%\x000fÝ¾øÜ{}¿ØIf\x0018\x0007Üà-\x001a?1£
	øKq°VÐæÁ&vK\x0008ûdÜÏfp9¡Á{Ö\x000føì\x0010Ð\x000f}¢hã\x0010É\x001b}\x0003¿<Áã=xè;\x001a\x0008ÃE3Æ\x0011\x001b\x0011\x000f\x0002Ý)×g½\x0000#\x0019Ù\x0019%Z\x0010\x0010ál\x0000\x0001Ù\x000eJY\x0003Þ\x0001\x001fÏa\x0018ð	Ö\x0001Z\x0001EO\x0002ðdÙC÷ì8fvæ K\x001fªB\x0011ò2:\x0017^öh ôÃ/kx}x»Ø\x0007\x0004þÂU[øÌ>\x0018vð@	nGèk\x0005ðÈ±ÃÂ6±£àv¢ª4D\x0016 \x0004,rfç8È\x0018<Ù\x000f\x0002\x0003oLÂ}\x0007çX\x0007f\x0000KøC\x001aÐ@\x001cLb\x0005\x0011rn\x0010O®Ö g\x0007\x0011Î´\x000e\x000cÓÈÎààNëév\x000e\x000e·%G\x000eÅ\x000en28\x0010´\x0018<\x0004	0÷£\x001f,\x000c</p><p>ç@
ØÑ	Uõ	\x0004Uï£ª\x0001ä¨*Ä8ïhqp\x0001Î·\x0001\x000cC\x0008ØEZ\x0002¼\¤,\x0007"1$B\x001cüH\x000c"Ñãà
-\x0016
\x0008ÄE x*e#U\x0010\x000e6z\x0010\x0011ýþàã\x0018ìçq	\x0004\x0018\x0006\x0006\x001bFë\x0003mØ÷\x0011Ö²\x0010ã#G?à\x00108
\x0004ÃéTÂ\x0006I\x0014FÆ\x000e¼\x0018L,þ\x001ceØ@L°\x001d 
 cZ c^À\x001fÁÓL(\x000fí\x0018U!0djÒ1¶\x0010á+ä</p><p>	Y\x0000\x0001\x0001k	x\x000c\x000bò,d\x0018@hq,ªz\x0010`&pp¤Y\x0010MC¬\x0012x+
f\x0011¤\x0015$X\x0006Ú\x0010=ã\x000b¹\x0013=Ô\x0014(\x0017gèOÄ}Z6FJÇ°cB\x000b(&ä  Ñà7ÈB¢Åy\x000b\x0005a\x0007\x0005QLQU@`¤DKÂè\x0006I\x0012cÙ£z8Þ</p><p>Cò(\x0003\x0002;&\x001f\x0008\x0007`\x0019æà\x0013b	ü!Ed\x0012ëU0 ¿Rb\x0008#Üá%À\x0011L)#\x001c\x0004ÝÇL>q@\x0017vF©b5\x0012äWfä</p><p>Äd±%\Ì\x0002çeOUM¨gàAff7lÈÑ°3\x0018Fº\x0000Á\x0013t\x0011ø,C!¤\x001dª`fJ±\x0004#\x0007Æb</p><p>"39Y\x001aKv:R	Ò2ôö,Ø\x000eAI.ð\x0019\x001d\x000c|\x0006åY¬\x0003ù!Ê@QF ë\x00029GÈ@ÎÎcÑ\x001fS$¢L\x0005ô~ çy
üÀ×\x0012)D ¯1,Ì$cX
Åó.³A"«·£_Q h\x0000¤1ÖAe^#ç@\x001bp16Hä\x0017iH~V\x0004OP´p"çL\x0013Ã"\x0006\x0013\x0007ïzRÁ	\x000c%ü\x0012)ü\x0016¸\x0015ê±\x0016b,Æ2)\x0004v\x0000\x0015x
m±Z&\x0017xK¼#ü\x000cJ\x0012ùER\x000cÐL*RHiL=ÎF øcC\x0002â\x000eµ\x0017N£\x0014gËt\x0003*pÉb\x0015âu\x000ceTbÑ¢Q`Yv8Ç±¢	ç?Wª3§fGÏ)(Ç¤E\x0004\x0018çacAµ1%ë³Ïn^9{\x001c^Ý¼¾yýûíýÍý~¸yýôøñÍÓWï\x000f\x001fn^¾\x001b¤Üÿv\x0018?ÿüÓOa¾¾{÷ññpúöçÁüg8¯\x0002Ú­@Ù</p><p>tËÀ¤ÀK\x0018ß\x0016öãáÏ§_\x001eþ\4\x000cb\x0006\x0016ñ\x0008\x000eõÅû»·Ëf-Ïe¯ÊÙ±õÚ\x0006m£¶©*%÷<nÍ¥Ëój\x001fÑ3¤k\x0019ÒV@k,ýyU\x0006ÝÙt~32lFÆE$©\x001b~IÛýÂÇö_øÜÞ÷Hu
©¾%Õ{ÄØØ\x0014[KUbÓ®Ø7KyWúýðÅ¿_ÝüðËÿðh[¸t:åÅN/ËûÔQ\x0017w÷¿-\x000eÁ4\x001cfÆ.º\x0004YyÛc\x0008Õ³k
\x0019WXC¤jÐ\x001dOnXÃwÑQ­±/,TÏ¾5Ü\x001ak¤5l76l#6l76¬ÆÝ\x0019\x001b¶\x0016\x001bëæê¬su\x0016muÎÎ:Wg«sÒ6\x001fÕ\x001eGm¶¢­×V=j£ýÞ?\x001a¨b¼)ªºüÏ þä*âº\x000f|\x001b²\x0019é6#ý2RÓZØ\x0002\x001d\x001d[³Ã1?Ë\x0002Ñ9\x0012K\x000f-éiôXºÂÄ¹¢o^5oQØ+\x0014î&1g³Me{1ßTVvY×,gÍzÆÕÊc}IÚjý\x0011­?¢õJ´üÖ-Q(N\x0014ç´¿ÓþÎÕGæznË3¨ÿj*âú/ª×#e3ÒmFúe¤_S·ªâZaêgÎ¬2è:3ÎT]S¯¶©\x001aW¨Ú­WÛ\x0007if!\x001bÆÖ(M%\;¨^¨¶\x00134IÝe$³=èÍö¨7Ëa¿¦Ø9-ZNÓ¢åµØyµ×âåµØy}\x0008ó÷÷\x000f\x000fÚ?èT\x001d|Ý¾a</p><p>ýj(ÙËâw\x0002õ­ë\x0017¿ë²\x0019é6#ý226W¦BG\+iâÜÏ¥6ëXÜ#56¤63Ó\x001e©¹.uor\x0007Ù
ùyõLíÇ®^¼·d×0ÍrÆ¬©DA_÷V¨\x0015$j\x0005Z¢V¨\x0015%j\x0005Zât	YUv%«#KÝIÌ_V´þ±ËWÄõ+ÏõHÙtËÈÜ6ß\x0011×</p><p>¶<\x000f¶\x001a®KÂLÕæ\x0002hÜ£jX¡jÝ´i32ï5Ï¬ppÓoMáØ` \x0019Í.\x0003å_S8tOÈ¦©\x0000h\x0001ÉZ\x0008t}Jã¸&8¶ú\x0008£ëSV×§¬®O©±Ê©ÚÈä´Î_uC¸(\x001cgP¿p¸~á¸\x001e)n\x0019iÑæ;âZÁ6_Í®2èº$ÌT]³FµMU·BÕ~á¸\x001e÷g^8Ló¹ÊôÂµi ¼Ë@f9àW\x0014\x000e9n¥³?Ç6j´ÕB \x000bÏ¢{1\x001a,åÏ±U¼îN¨±Ê©êÈN{\x0003U7ÄËÂq\x0002õ\x000bG¬ë\x0017ë²\x0019é6#}\x0005Ù\=
\x001dq­0¹31æ\x001esÜ#ÕÖ¥®°RªèÛ|#Ì{ôõ»ô·«Ðn¶ÌV§EÚE«\x0017ðÍqæê8×T\x001eÝ¹\x0013«\x0015Èj%Ñ¥g±ZIìTI´\x0012éÒ³è³:²\x001cÜ;¶Twë1\x000bË,gT·ôg/Wk v;T¶CÝv¨¯A!\x0017z\x0002[!çf!WçÐwêy­Yü³1Û´õv¶Ý§=\x0003?¿øöÉnè6\x001aö
ÕT¢M!Ñ½%qZ\x0010\x0016\x0004§\x0005EwyþöØjAÑå]rÎöØ*^we¾gp16z¾ð»UgT¿xS\x0011Ø¯$\x001b ²\x001dê*ÐÐ\x000c;ß\x0013Øº0º*¾gf/A¡Y¼â.mó\x001am»\x000f2[ y\x0019º&»t3CtsHNÛº©!º©¡n.gÅ­f.aJ4ÑGÛóÕQÌß³(¶\x000bÊ:"\x0017dµ|\x0015çUåÐOÁ\x000bh3¼d\x0013ÊmBù]æÑ ÐufIf¹ÂvhÜ\x000eMÛ¡¹\x0007í\x0007ò|jN«N^H;\x001dl{ñÅÃÛ¿óêsh^\x0012_|³èáÜòèi5¼.·\x0016Ê]¹ÒëºrkÉÐë\x001brOîy±Õ,ÐÅUUsO~é2®Ì? ¸´FswÑìJð\x001cë×Ì\x001aºA¥%º|çsl§©©öÓo\x001cD¿q\x0010]ÏVËOc]Òg&ýÇÇÃáÕÃÃÓÍ«÷ïn/\x001fÞPÓ·ûr»|Sòïçé\x001bé|èt¤j:m0íõMK÷ÓJÜôv<=×N\x0013ðdY*y÷=lüíá/Uu¿~÷\x000fOïùï«û·ç\x001f?^\x001fÞ<Ýüëpûöðx¤èoîßßÝ\x001f^ÿzËQóÂ?îÁáöéîá^?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
Instances: 1
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 274 [https://authent.webinaire.numerique.gouv.fr/auth/realms/master/protocol/openid-connect/auth?client_id=BBB-Visio&response_type=code&scope=openid+email+profile&redirect_uri=https%3A%2F%2Fwebinaire.numerique.gouv.fr%2Foidc_callback&state=4uF6C7MjOBjVTFI4&nonce=yYjMLwzTFdw1Mf4k].</p><p>Predicted response size: 574.</p><p>Response Body Length: 795.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 3
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2dl-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2dl-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-adm-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-adm-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/](https://webinaire.numerique.gouv.fr/static/misc/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/toc.css](https://webinaire.numerique.gouv.fr/static/css/toc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/images/favicon.png](https://webinaire.numerique.gouv.fr/static/images/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/global.css](https://webinaire.numerique.gouv.fr/static/css/global.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/Filter/DCTDecode/Interpolate`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiOGVmZjMxY2Q5OGNiZDA5ZDMzZGFmNTZiZDdmYzBmYWZlNWE0NzM3OSJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Evidence: `eJwljl1rwjAUhv9KONdSa9dV25uxCcJgshsRxiYlJicaTZPuJKmo-N-XsqvDeb947tAqw_0RPTTfd2AhHUAiR61xB21hAksXiTQapu3AjZaYsdcBb2xw0bO9RssC739inmOdtEDIsOPasBe2HRO9i2Oa_hPoPb8iZbB77CYgPKk2uDNaaKDOn0WtlMqFVFjIkj-pvcrrohKLRV1VfM5lNauKIiGJRIQ2tD25IQFRaktUPJqQTIk-aMuDduPqMYTeN9PpBfdJ1ISZjR2S_o2YHRJapih5RrgOU1cRP3TjMlrhJMqW0PfOeoRGceNxAtZZkT64fp3WH5fbZiUvs7Uqz6nsAw-jVcZVtZyvT59vp-1m9V7C4w9ur3rT`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/4.Activer_le_materiel_dans_le_navigateur_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/4.Activer_le_materiel_dans_le_navigateur_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/Filter/DCTDecode/Interpolate`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `Creer_une_reunion_Improvisee_V5`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `d09GRgABAAAAABVIAAsAAAAALOAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAADsAAABUIIslek9TLzIAAAFEAAAAQQAAAFZJwk67Y21hcAAAAYgAAAFuAAAFNuKa/PhnbHlmAAAC+AAADhoAAB2IDPM492hlYWQAABEUAAAAMQAAADYbffxWaGhlYQAAEUgAAAAeAAAAJAhwBAhobXR4AAARaAAAABEAAAEcSCAAAGxvY2EAABF8AAAAkAAAAJDonu+SbWF4cAAAEgwAAAAfAAAAIAFWAFluYW1lAAASLAAAAR0AAAHyFNvC+HBvc3QAABNMAAAB/AAABJyXrlRreJxjYGRgYOBiMGCwY2BycfMJYeDLSSzJY5BiYGGAAJA8MpsxJzM9kYEDxgPKsYBpDiBmg4gCACY7BUgAeJxjYGSZzziBgZWBgYGf2QNIroDQTA4MVoymQJqBlZkBKwhIc01hcPjI+NGN+cB/AYYc5gMMH4DCjCA5AHlACw0AAAB4nO3T523jQAAF4ZFFy0nOOeecc842a3CRV9D9cg+swOboXRlH4NsBF0zALoFuoFk7qBXQ+KaBx996ttGZb9LfmS/407mmcL4qf37qseFYnxedsau+tqif2KKHXvrq+wZoM8gQw4wwyhjjTDDJFNPMMMsc8yywyBLLrLDKGutssMkW2+ywyx779fsPOeKYE04545wLLrnimhtuueOeBx554pkXXnnjnQ8+KeuPafH/aDs0v/6dla5XdFawK7DNcCdURbimVXe4S6pWYHsC2xvYvsD2h7unGghsO/y6ajCwQ4EdDuxIYEcDOxbY8cBOBHYysFOBnQ7sTGBnAzsX2PnALgR2MbBLgV0O7EpgVwO7Ftj1wG4EdjOwW4HdDuxOYHcDuxfY/cAehH98dRjYo8AeB/YksKeBPQvseWAvAnsZ2KvAXgf2JrC3gb0L7H1gHwL7GNinwD4H9iWwr4F9C+x7YD8C+xnYMih/AaHUtUQAAHicnVkLbFtnFf7Pf53rPO2a+Pq2S+z5sdhxk+Zhx/byclrFuU7XR2jY1tCmWTvdZh1jo6WP0a1QTbSj6pbQscqgske1sKfQtALqeFQwMgkM2nhIpRrVQBVI04TYQBDWYOI7zv/f61fqlJS6vvf3vfc/5zvnP+c7578hAiEfHzBtFHYQO3GTNYRASHbIjhVm0Sy6A/6Af0UsGosKeCmEgzbwirFQHLpwYAG7C+jYiQP7BhOJwX0HtL/nRjPdm7ec3zJy68Az337mr8Gh5uahUXYQxksfgxVslN11e3tHZ/unegYGZowH8UAqSnBFySDZSEiFN4/InUfZhAMOzQLmQJw6ZLwbaIOA34wXRHysydsGXXEIucBugUAo2uX3inZHEXIdCAd3dP34tk+PJ0PHn/hy51D8xddfXttbW+u95Rt375y4+7T7Zqu1Hwai49Ho+GfZIRrs7R3t7X18kRBu4Y967fUOR3/XrbQvMjy4XhhaO6ruGp941OFYterkzvFd6id/YkjBg8rEjPYSQgrrUYN2R3A9ImEpLPkkX8QXqS9nf4AtTLSL3fGy33Z2h/rVdFpNZ8rYeOL+HdsisVhk247LuQGcYQ+n1ezlcpaoJc/yAcIiDOx5+jPEScAWtnkkj81n80RQM7RqF1XtIpzJDVpVbtcLpklhkNiIRFYRUgUOXA6fhy1ODHB5HIIUjrAvPQbviha5bmG4bmWdGd41yw0rx1RVFVYv/Lym0WGxOBprhO4aiyV7n6rCRCbDoJiK5NvJStJYTgN4QEBf2vBbTol2u1CrPRRSy+la+B2dyf5ThdkMt/3jd4Q/0HlSSUgTyFUQQw/Qk1Cb1B7WHk5Crfp1Nj4CxxXtX3Qnw6f7K0WbWGRDjM2hY/ND2pvarAJtV5PaLMST+nMf/1l4n37AZAM6FcxVIMMJujN7lstHmXBG1eaScByOJwnlcg/T0+jhKrYSuAayWTYDnFKpmJyfR8n0dPYYPZK8Oq9AnD2uzzlHX0YsbPVkpsITQEgB+npG0d6AtYp2UT9nYE9GgbU4wt/aG0omb4tEX+C28NnUZZgAe64q0A9xZbEtKL0KAuCJCEFtToHjzE912WcxSApey2M7VrAHIwvNkUFwq9kMswfi5e35Dp0x7AkwTU38CP9m6BE39RsD2PMvbsmGjHHO2eM27OHz6JNMkTaL9swr2iwO8nYzbNweZgzGvODWRpPwqnacRf5ftC04xkQy1rwQJ2xlAH1spifzq0e7s8/SXdo/k8wdSj5GOjgOM394zHAnzBiAdHsx1jcJ0+ihBkLqPTa7iGHuj0A45HAiqq5oL6MNTySsCu87pYUjkpN+mJacCyudUhrTU4UzWlxyOiVh1CllMpITI97gnheQe6aJTHwkgBhQnpQTbitINXsYHeEIaUn22DzCaJpJY3oMBZj1akpwp9TMwhXBLazGm1e4QjdXllY5PWl7dZtNIk0xm41cmoO3lOyHmBi/hLeS2Q94YhTXqSBpX6IWlOXCWCAmY4SW4/syXNh7UZmGBqUsp5dhwvTF5BQ0DC/CF70RfPUxlrABc4ABXS7M+6eVqWnlq1PK41PK9HLBwqVpZRqn4EScbsTb1zHuazgn5VEwZvpoXvn3VeUjDL9X55V5HOHveYXbuR/tHM/xODBCzYWILxKOeFjOso8wmlGdUjaBK56BOW0vrjudV7OfYHFAP8QQeU7bC6fY1+DvYrlOVvk8Uqlw2eaxVYRtvnr8wgTM5eWn6ZgW52GFGtQiHdkEvZDS1eTy5ibUIZBaQmLIrlU59k4JxxaOYOR1KNqYtnUY2tVqFU5Au6JthZcV7be0TZ9/AOdvJ9XEgtHqi0A0dDNWGTMn6s9cpH3WoGXaal34O5PWx35bp/BS9i6V5Gs7m28iVlLP4j0AkrxIzDr4T1Kr2MsmN1vzws6yqyZFxcsWC8q0ZneqhBRsWk0+wbgAJFaDw0U5G25Cx6EePMxlkKLQY4f01Fe1hxR49D16Gukqo13kLjspOdFd7/E7aqGuHuLyg7wPYx2iC2TWXLlZnxWHWLSex3XMnw9ss4NnXmnnVdI3Hj+475uy/M19h7Srxujg8T07tg+sk+V1A9t3/KYw3BO/p6/vniPsEPd2e73dCXYQVvf1vH306Ns9fbnzwpU1rSNbdu/eMtK6pjD6ojEVD6oxFQ+8v7wD7XqY1BEXaULL+jBnRZNuUCCG9MsaSheNxgIWaMOTHBBdNFYRwFZTMAeiLiqLZsCTWfjSAe1v/3ll1Yo71z2VFP6YfD77SnjIKp9483c7Jlsnd97mqWn44DmLNbLeC48Ph+ul+599fdvmz3/0zimHY7PW3bE94RUq1ksPXPrK1qf6n0oueJPP0zvbHxzc8/ydNV2TjTWe23ZOtv71Od/6iNWyLzl857bUxMpVI2tWPPiLw1+8F35OvYntHXoc7Dc1IP/UIQNhVS4OAeBEHRPcmRwPw6yaSqeF8QxLHwyGY5JTq03jv+I4HSci5gmLqrA5EI6EY0j1Nl8TCvSgeLMun55EQSnM5lp6IZ19CWNoLGOtczA1sIdJXLiCVyQnarJbrU6JFPJoHGNKYvUrFI3YPPlSE0DQMSkFrShhjteVK446awY0hN2qVxmrRaIXeOOXs3sc7caMqgdPUcni2WBDSdSvy0GJExl6gXbkBLE8yGQvC+6c3fsRF/OhTG6+xot6ALeArR7rol1sgWKHnuLbgihSEG4KgmqJa7MJ3uUjD7WyLt/E7WdrVYVsJ2P0IZfYwnqaYAfMtii++hJnG74eS6e5mjNcSarY5zqQswwHqoLWNGqC1iLnu7jvi+sU75LL1ikB6TvAWvFy1eiHyLBlKw71s14/zXsJU0k9XEM6b6gisg0Pcvyya7a6FKQyRRD7L+xOCuvN1sGJ3U5L2X6ni8HjW2LJHNHpywky26mcD+ViyimFOtpGRn88OtLWoQ7uP7F/EHugt5ySVssjA2M4dBe7xx66KxRK7B8c3J8I6clmKsLgwUho/18oKngNlHyQR7MEElb6WNGFVg5pSUC8PKppOJUDZtSUjcj5ViM/S/BUsS1JIMUC20giuKy9sQ4egSPrSjs9bTOs2Kh9H4Y3Gr3lJqEFZdox5q+RWlEFNk8VLRYr3KMd0D4ruBcycBgOlIq+qD0Nava7aOJ3YZOxlu+YbsJeWyBm1s/UYy3NfXhxp2PZl/h5Xs3gZ1lzct/SOQfQjuvnT64FKv+S4U9LJtBJlkDsa+TPpv8vfwSjR1pu/gR567TsBPLrKA0e13PcuxST+EVcZfw1AIiyLKC3qyXRVFM9V1VV3ikviTW12o/EaiqKM6IkLt4L9NwQs8gOuxVE7FtYzMWiy+63mxHeXHV1hcigLttTiRmzVDEjirRKhCFuASniRtaHylhfGf9jxDVhv+szak0uOYAxjSe3q2M9L3L+WDah5koLy4lUiKU01oEHMEgzeoLryQ5zmP+nnFIqJWFDXZHX68N4ipBu0s8qT4FluF5njn9aQNLTs5/m7yD51OO+D9iXkVBriqlK6Tpz4wLNqAtX0nqLn72cSlXrF/leMa0/xu1Ic/4KsQexm0hlD6VSMKEurlUdS0WYFMYNMm0TsF2T4+DCts3nFRHrEsWrub+xpn34jg1dlXdXdPb4TS0uhFF2RRGEOlrbs/n2RFDwrQvand7KNX3NTmlDmfqm3NCOFF0Xwy00uhV7ijYQ2YtLFzPghiqeU3K1mPw9neKuyq4Ndwy31zT2BZcbmhn1vHuD5GzuW1PpddqD624RgkO3b+6uJYt6BB8JL2FZDJELZhk7YMlXHxDbaCSMnbJLiJW14d54TLrryRc3dnZ/6TN9qc7OHnaaMi6WBf1RzzPPT42It2xdVaN8bkB7c+wmfjau5vY+qmmrcB9fAwIsn3Fn4kB0QrirTcD+nK0AexeM0Ot9dpcQxb3exOGDBw9/f/VqqzV5NtX3wNeefrKbjk8cPnTwCz9oCVqtw/mLf97S0OC8+YWD+77w8G5wjTyxL067b81OjjY2ulwv4tUjk9qfPvnE3gHojhXtw9j+lbAqnc9lmScTe09yLPuSqu+zMP7TLC+2sajXS1qabcyQ+o1ayWRVEge5CXMUpWFD5rEJnuKOlGchUoI6lf1tiIvk9RGs0FrNCJq2T2UTgjttbPjcjCNY08HeS+02jeP6rkTZuOlnGcNWuKjNsIvCo5eUS/2nNj1072Rff3/f5L1zbBB+BK92hPO/2eChjU8Ya6HLbL+OVHMceaY0G7DfjaGy5KW+a5Sd7gjn+xnerCSOdj6CT7YvArDplNx5NJHvafjz4Y7Ce9fzcIZ5ldV3bP+zCTij5vYhwvvCNH/XTuQioLAIuZ2hTeezR9s7OpRoDgabE0Pfyg0ez2fp/TBbcocPcnnF9cmkFdm3RKOv4JXy2kv2zwUoKmpQnlNQA7ReC2q08MeKInxbFP22sqUcUrXwdwndRz/F/tSKkdhUXC2aGNVimbCAP9BUEWDL6g/E8BKChQuzLOJmoUq01FVW1llEbR7+kWwKhluGe9Y6G8+ynZzk/L2JirWVC+9V1orU9HvXcOOn2iPbGoZbjg4n+nsMf+m6K7DTYv25GbcFcmBZGOjJV773vVd+dX0gdOtj6ccCy0Gj++FV7gfvUn5YA/n3eDEZ/NfqppfOJc+dU157TTl3LlnWC+ncXfxP8j541fBB8/V9UKp/bgkHlIBY2gOlSHQcR4046FpuJDQtCoxyPplJDo9s3Zwcn+xo1zL/I0h+nVz72s7dr69Nbn738IP37VGviRlTHqceMz03FjWL8S7pwyVAL+3O6yP/L0ERSDgAAHicY2BkYGAA4qWF227G89t8ZeBm2QAUYbh9I/oxgv4fyrKOuQ/I5WBgAokCAIXPDYkAAAB4nGNgZGBgPvBfgIGBZQMDELCsY2BkQAXuAFbDA4IAAHicY2BgYGDZMIqxYQAfoTE5AAAAAAAAAABMAMgBHAE0AWQBmgG0AcgB4AH6AhoCLgJIAmICggKWAq4CxgLaAwYDQANUA6QD/gQYBEQEdgSWBLYE4AUQBXwF5AYKBjoGYAaGBroG+AcsB34HwAgKCDQIZAh+CJgIzAkeCVoJugn2Ck4KnAsKC14LpAvKC/oMJAxwDH4Mtg0QDU4NlA3QDhQOaA7EeJxjYGRgYHBn8GVgZQABJiDmAkIGhv9gPgMAF78BsAB4nF2OvU7DMBSFT/qHaBACITGbpQtS+jP2AdqZDtnTxElbJXHkuJUqMTPzFMw8Bc/FiXslKmzp+jvnHl8bwAN+EKBbAYa+dquHG6oL90l3wgPyo/AQIZ6FR1QvwmO8YiIc4glvnBAMbumMkQn3cI9auE//XXhA/hAecvqn8Ij+l/AYMb6FQ0yC0T41dbvRxbFMrGdfYm3bvanVPJp5vda1tonTmdqeVXsqFs7lKremUitTO12WRjXWHHTqop1zzXI6zcWPUlNhjxSGf26xgUaBI0oksFf+H8VMWO90WmGOCLOr/pr92mcSOJ4ZM1ucWVucOHtB1yGnzpkxqEgrf7dLl9yGTuN7Bzop/Qg7f6vBElPu/F8+8q9XvzD1U2IAAAB4nG1S6XrTMBD0tBxJmjRNCrTlLFfLZY5ynwUKlNdQZLnxh2wZ2e7x9li7tuO06NfMaHdWGslb8Hj1vf+vfSxgEedwHhdwER100cMS+hhgGUOsYIQxVnEJl3EFa1jHBq7iGq7jBm7iFjZxG3dwF/dwH1vYxgM8xCM8xhP4eIpneI4X2MFLvMJrvMFbvMN7fMBHfMJnfMEuvuIbvmMPP/ATv7CP315fSGmKJPfDSOuG6ChRQxEEvoys1Ip4x3EHekIryw0V5HJrzZEfmKOE+KjFs3aFViF3rLV4VtrZjPX1Od0ppUsx0bVla2OFFRsdTOc8WShrROW5cUqfmY7P7qy2pSIlbcBaxYYN446BLINIAmEplRmjuORUyT9VmYMTc8wJSW0y1Y64x4qDS4HSKlfkV2OycIFqI/gpuiqI+CUYOW2sjnNlE6Ed47kddcLdfQdMGHJh2af8xs+5nJJoBEk0ghAdglAahHzdhtGTRElobCzyyCS0PSeQozZlHuRIiLRYRJo1QhRBrJLC36lUhx0apaKYpXZWIbdUixPuI0RXT22UlMHwR68J3eZvobLmuDNGXVaFVmVT7qoJzcjEYZULITpxpoSVXFxjmpAVk9wKyQ/ULU/Lx2BEqR0aXcQcPafWFtoVcVH9ijnBVSxXQvkr3X6Lul3P+wdkWXj4`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/Filter/DCTDecode/Interpolate`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/nico3333fr/van11y-accessible-modal-window-aria/blob/master/LICENSE`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiOTA1YzlmZmYwY2RmZTJkNGEzZmJmMDkyNmM4ODk2NmE3YWQ2MTYyMiJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `eJwVjMFOwzAQBf9lz1WahuA2OYIUCYmIS4XEKXK9u8VpYoe13QgQ_45zfG808wsmCA_R38hBC035aBpmLg0yVVjrB75w2VTKnE6NUvqoUR1UVcEOTBIhF4dF_N0iSbaRWKcpZogUonU6Wr9VP2NcQrvfr3TJpxUqXJpJ7Fei4urTvWDJbDJ-puyy6Ou8lckZj4SDUFi8CwQt6ynQDpx3Ji_4_hj71_Xn3OF66Lm-ZTlEHTdUp049H_vx7Wl8P3cvNfz9A2jET6g`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��b�׫�0�
�(u�Ȟ׫��Z�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "          // we remove content from its source to avoid id duplicates, etc.", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found with a target of '_self' - this is often used by modern frameworks to force a full page reload.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/](https://webinaire.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr](https://webinaire.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000341`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000250`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000046912`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000077098`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000378`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000469`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000541`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000233`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000472`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000524`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000433`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000486`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000286`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000381`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000646249`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000338`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000742050`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000416`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000195`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000247`
  
  
  
  
Instances: 586
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0000000341, which evaluates to: 1970-01-01 00:05:41</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

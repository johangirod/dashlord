
# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 22:37:14


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 8 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| Directory Browsing - Apache 2 | Medium | 8 | 
| Reverse Tabnabbing | Medium | 3 | 
| Source Code Disclosure - Perl | Medium | 3 | 
| Source Code Disclosure - PHP | Medium | 9 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 9 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf](https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf](https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.1.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.1.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Directory Browsing - Apache 2
##### Medium (Medium)
  
  
  
  
#### Description
<p>It is possible to view a listing of the directory contents. Directory listings may reveal hidden scripts, include files , backup source files, etc., which be accessed to reveal sensitive information. - Apache 2</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/addok/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/housenumber-id-ign/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/](https://adresse.data.gouv.fr/data/ban/adresses/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/csv/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/ban/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/group-id-ign/</title>`
  
  
  
  
Instances: 8
  
### Solution
<p>Configure the web server to disable directory browsing. </p>
  
### Other information
<p><title>Index of /data/ban/adresses/latest/addok/</title></p>
  
### Reference
* https://cwe.mitre.org/data/definitions/548.html

  
#### CWE Id : 548
  
#### WASC Id : 16
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/terres-de-provence-un-outil-sur-mesure-et-des-adresses-certifi%C3%A9es-df42b802e46b" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/terres-de-provence-un-outil-sur-mesure-et-des-adresses-certifi%C3%A9es-df42b802e46b" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#rHIW`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.1.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.1.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#3SCi`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#rHIW</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ùyùêhrÎH#\x001b\x001cæÐ\x0003HnÍG\x0010\x001fI.^\x0016\x0017®	%+ý(¸hKe\x0014\x001dðÝd"X*R\x0019»\x0007JÙC<\x0007ÅSp\x0011QÒ2¢-È]\x0013IVâóH¬ ¡*H"0ôH|ù>£s[µõL\x0014­ÉáJGP¢å¤È=Hrªv&	<Ë=}\x001e|¼åÏ\x0013Óv§,\x0014\x0011÷@É	Ù( Ls,S®Ì÷'z,åL(©,¬\x0015ó®óX\x001c\x0014\x0016Àa\x0010ø`L\x0016T`tBÑûH«3Q´ÉÏküBQ´+§VTÚ?Þ~¿ûà{CÕî\x0017¯Óð¤KNN\x0002iïr×\x001dêsKmªYÿs	\x0013¡Sñ:MM:9Ü²
¤\x0007FeD5`&¥\x0008ÊIlBNTT\x001e®
\x000bûSQíP\x00152yQ«Ä½dXlÀ¼u\x0004æ¤j\x0004Ã=Qvþ\x001bø=_/á?µøåêËÛëï\x000fÔT¹ý«
Ê£vüUØ³Éà6c.;<¹8\ürôúõéñßßPcånXÕUm°Ò\x0017¯0X\x000clôÕ\x0013±ê.«ncÅºþ¬ëEHÝ¾éûkGºDxû4¬¦ËjÚXQ×dk bÚ\x0004ë\x0014³\x0006©\x0006Övam\x0013,.pÌ\x0017+¦¦|
".oÉ°Â<
«ë²º6ÁZ\x001a\\x0002¬¾(\x0001WPKeè¾¬¾ËêÛä\x001ecÒW8\x0012ÕDòMÈà¸\x0018èn.jhB5àðûì2`°\x000b¤ô&¹êðD+vac\-Íi\x0016\x000bÖ(zGoæÀRÈÍh\x0013­¢\1V§{6[\x001cCï½'¡í\x001b¯6ëeæ \x000cXÔâÆ\x001a¢uÑE÷4´=ë%ÛÌ1\x00017$$Ùâúq~\x0019Ï²òih{öK¶\x00190ëh1"ÈÖÆrnq\x0017ÉV?l{\x0016L¶0ãh.ÈVºòôM³vl¥y\x001aý%{&L¶Ú°*I¶XÊ$éùåY'Ø§¢í\x00191ÙfÅ÷ü\x0007õ=@I¶Fr°Eøø4´=3&\x001bíXPäÌ¤e\x001f¬\x0013¼,[ñD²íY2ÙhÊ?  4\x0007p.>V? {L¶2'Dîm\x0004ÑJ¾%ÉFÃ\x001a:µ÷U=K¦\x001a-Yôyû"ÀÆ\x0014\x0002J¢u²[ñ©<\x001aÕ³dªÍ9E]Ý2à\x0000e¯ò{_l\x001b\(UÉûÒößamÌâ@>\x0012­)¢õ\x001c
Àj§í\x00192ÕfÈ¢ÙP ZP¶9Ë	~\x000càÌÓØ1Õ³cªÍY©\x00186FYÂÚ¡\x001cÚ§Q\x0007ªgÅT\x0015sÚ²\x0010t* Í1*
v\x0018£j¥íY1ÕfÅ,n-\x000cÅ.x²¹ÏA´ÃL+mÏ©6+æpöQ¶\x0005F^&Ù\x001aOº6<ó¥zFLµ\x00191\x000b\x000e'ÑÂ+]EçØ1OäÎ¨\x0015SVÌ*ÎúZ½h-ù\x0007A\x000eSG°ºgÅt\x0015³Qå©ÿhr5n*I¢
Åæ*ù4ï1Ý³bºÑ\x0005×ohqx $9\x0019±ÒKµ/kÏé6\x001bæD©~Áö*:\x0005ÝÄ@+Vöí\x0007\x0013Ûl\x001b¦(Ì
Ü1\x000bVá6Æ\x001cM6îi"tºgÄt\x0011sð\x0002ËW£äË\x0018ÉÃÙx\x001a?Q÷ìn³\x000bIÓ6\x0008¥®#õ4eu\x0010H²=M«Û4­3!¯MAZ¹Ö]·\x0003Zõ4êÀôiS^84®ÇA\x0003Dë<Ý1øð4&×ô\x0014iT\x00086äE¥@+cqg\x001c%"7þi4éì\x001bï3¹
\x001ch)´^8xâi|pÓ»d¦íyì²Í´Ø\x001aj\x0015\x0015\x0008:·£ê©VØÞ%3mÌ+E¯\x001bg\x001dæ\x0013«aoÆ=Õ©µ½;fÛî\x0007ïÐEªú2¥ÓR6L7\x001bÝ®\x0006fwõ\x0004v×É±á}"gÑöáÓ\x0006üÿê#]\x001f\x0018\x001c&àÿÿãuptû	èti±÷ãâùí#P?ìplõ\x0001%î£¶kÇÖ*~3\x000cý¯´Ôûbñüô\x0002h§FøvàT\x0017NÕÁáÌ\x001e\x001d4f2Ç\x0010­a¸¡»U\x000b§»pºRr¶\x00048µÃÚ³,¹P^[Ã4x-éÂ*8¶ðÎ\x001c#\¿²ýp¶\x000bg+%ç©T\x000f$ç)È\x0006p¢|V³\x001fë²¹:ÁáD;/¯\x0011Y»á+¯ÌwÉ|¥ÔJ]qÔ±ÜT®|Æ\x000eë>+ÙB-TJÍSEN\x0014\x000fSü{±­sªIÃ:8\ä\x0008n\x001dhP®|Õaeh-]_ÿÖ)`¼©èà	T.*Î\x000cß=µp=ý+ë\x0014°+\x0015)yÝ@äò7ÏIs½']O\x0001Ë:
ìày\x0010)(c×¯°\x0012¬eü@+]O\x0003ËJ\x0015l\x0014Ç
¢7\9hø\x0019\x0013÷TÀ²§e\x0006v¸b¾«Õd»°Aª=\x0005×ÓÀ²R\x0005cË%}ÖàÙ\x0016^±¦\x000bÃúÜZº\x0016ujØ)\x0007\x001d¢è:ÚÄ\x0017]7,|ª¥ëéaY©±ZDL%¹ù}\x0012zÚ\x000e\x0017{p±R\x0004\(\x0015±*\x001eüº\x0004ÇíéÎ©Pf\x0002MGbý6N8²»n÷ëY	Ui%àJU\x0014q	\x00145¼'[ßI¯4\x0012à\x0008\x0007ªUiB}\x0012Ô¥æc¿ëªz6BUÚ\x0008pG\x001c]\x0008oqZM\x0016\,j8ìI×³\x0011ªÎFxåKu*x)tä¬\4L/ÕÂõª4\x0012.\x0014\x0003\x0016D\x0011\x000f¥\x0014qXi^K×ÓÃªR\x000fcü­ãS'ÖpÃ(a-\OÓ©JMå$|ê<N×ÈºD\x0015º½ØtOèJU\x0002¯/Ía	°åÛjùÌ	µßÐý7uÝuõÂ\x0000¸´^(\x0007(C¡\x001bu·UÒõn®»\x0011LãÂA\x00134óu
\ø.÷{åèÞ}Ðu÷ÁX´0xí*[\x0008\x0019\x0004WêQgl%]ïBèº\x000bá½Ä¦D\x0007¦LçS\x0007ÊéÌpúo¯î\x0007\x0007\x000fÿÎ¿ÄÙ"ôãt8E\x000e¶ªÞß>Þw÷ÓN\x0007\x0002\x0014WÞ§\x0004	ÕªE.¨òÆ\x000fdÙ[¬z~zq>ÞP;$U]Òáþ×ù¤\x0018´ã® s 
\x0015³ÇÒ\x0015ô\x0004¨ºªÛQué\x0013ÂDe)JSÀa\x0008£\x0001ÕtQM3*¼u)Õ\x0000`L(¡jN9á²½Qm\x0017Õ6£:ÏE÷ØÓÇ¨Vó\x0001\x0018åò\x001aP]\x0017u¸Ly>jX¤\x00128àO\x0008:«^0ª\x001av
U 0\x000cÔ\x0012¨q·ºy·ººßÞ¨½ÎÛ)ÑÉ^÷1IÅÊi\x000cCÝôâlyò|y4¹H¹C¦ºdªÌàlx®F\x0005·ÇQãuéXQ	\x0015hº¦«\x0006n+7TQ	W¢¤_9úJ.Óå2U"³2/Ù\x0005Áµ\x001bÄ9ü"7=J*Ðl\x0017ÍÖÌ°rà(
IR³¥òÑo\x0008oT ¹.«Ï\x001bªPj¸u K­t¾bçä^h¾æ«¤\x0016e^.°î2Ô¾¬6<Ð+ÐB\x0017-TIÍ" ¨0'\x001b2¸1ÒVÛf²Ø%UdBrõ²×å¤\x0019ÇG¿Þèä\x000cÂ:g0\x0013
mi(\x0017T{>j\x001b]ý
¶¾!¨²\x0004F8®=Âf+îh¶ë(ZÜ­g
d-\x0008¶È-èR6m9®\x001câ&?¿­g\x000bd10-àXîè:\x0012d7¥\x001d+Øzö@Ö\x0019\x0004\x001fóô{/mSÆ°ØÂ`F\x0005ZÏ\x001eÈ*`´X'k\x0015wËùP¢ñzX\x000b_ÉÖ3\x0008²Î"ò¾\x0008 BÖbãã¶§Øz\x0006AVY\x0004\x0003O\x001f*Áø^#í\x0016\x001d\x001d5pV²õ,¬2	\x0016×ãP'[\x000fñ%\x0008~Ø\x000f]ÉÖ³	²Î(àpCSzÈÄ­SÍMulªg\x0015TU\x00005F\x0005=\x0001\x0002Ð\x001b1u\x0005Ò°°º­g\x0015TU\x0000ç(ß&l±X²dj¥ÝK»©þ\x0003¡Ê*X'\x000f<Wúò
,|AÊýØzVAÕY\x0005g5\x0015\x001b­âù p\x0008÷rÅUÏ*¨*«`}Q½Þw[¹\x0019MlªÍª`ë\x0005Ug\x0016<ý\x0002\x0007É\x0015_\+¾¦ÂmH4V õ¬ª²
Ö»\x0003:m.®g*\x0019î~jC±\x0002­g\x0015TU\x0008Úú{~¥1îiüJÕ³
ªÎ*Hî8øà¥/+°âõ~S^ \x0002­g\x0014TQ\x0000·Ò²{dÁ²\x0015Ht{M÷®3
1h,¸J|I£.Í6Ã¸Q%[Ï(è:£\x0010×ÝkÁ\x0014¹9QüÊ½ôîÙ\x0004]i\x0013\x0002ÛR»Ö)ÜfM©ß/:£ûQ£*PI $[ÉSóÀ?ÚTjWÁÖ³	ºÎ&`\x000fµ#¹©õq¡Èm/í¦{6AWÙ®d5\x0006\x0005\x0007þÛÏ\x001f×=£ «f2\x0006\\x0010\x0012y¦\x001cG\x001b¼ÙÌ®`ëY\x0005]e\x0015¬\x000c¬BpÃ!Ë-r¶8Ø=ïiOõê*Õ\x000b.mñA¢]ûnÜÿ*÷syMO»*íæ¼¢©Nx°ÖµN²ñ£±J¶
1U*\x0004\x0004Ã­¸Ø¼Â}Ã±bj1ë\x001e\x0005zÈ¬ªN ÉMpâÖ\x0013J± nê¦¢9xzèÐ%ÑñìöñæÓíõvS0y¤AúÓ<÷H³_\x00197Åx^ürz¼!ï¢Ù
]²\x001b³p´,\x0013®àuÀ8Á\x001cÂ°çd\x0016îâè
\x001c#K¹\x0010(1ê(ñÑñä"9l2Úã\x001fË¯ÛG.\x0017×ÿý\x001fÿyøñz·»m\x000e,\x0001"nÒpeÐÞX®y¸8^\x001c¾<Þ~üP^~Ý¥Q\x0001¨KJC§þ7\x0002d¾á\x0000j¾Ðå\x000bÕ|j\x001dl\x0006\x001f¦QðÀð¸ñU\x0001Æ.`¬\x00064êBYb\x0019Uªd«ì¦êÃ
¾N¨ÞwÊûç\x0003
[Â§Þ\x0017\x0003Ê³kÁÏÝW\x0008ªïT[W0ä»y~\x0000\x001cV¿±ÚX;TCØûÆ²þ#\x000bKØ¯#¥ÑJnzÎ×à©QõZF¯;L°ó^ó\Ä2ôhcíp
aOË¨z5£5ºãdOIæ¡MA®*ÀÞ\x0019TõgPÅÒM·íf=³\x000eu
;>«	}ÐW\x0013JZ@á\x0011Y\x0006\x001auTi}IÈ\x0013×cTõâöqû4á iX·³XUjØ,u`yxn\x000fçw+D^^l%Ì|ªË7,¼ÚÍµu4Ä\x001b>q\x000eË)-"ÙÜÎ\x0006DÝE\x001c\x0016\Í@4\x0018`)àª´<ÞV\x0006Ô#.â°Ðj7"\x0005$!:
Ò)m\x0004ÃôH\x0003¡í\x0012\x000eë«f\x0010j*i\x0017b~úhÍW1H¼7¢ë"\x000eëªv"¢\x000eëÑöù.+í\x001d/AOp\x0014}\x0017ÑW#JÉce)ùR:H3ïµ.
¡\x0018ª\x0011¡w$¸
<\x000eXÁ+oËÈoh@]ÄXèÖ\x001fÚ;j5\Nª£÷\x0004}¥]­µ#6¨Æ±ü\x00167ÁË¢qö>²§\x0014eµVç\x000eF¥\x001d÷÷\x0018\x001fé(ªÑ@\x0006ÆÎµJ\x0007Û>Ë\x0006\x000f¸.Ôg¹(ÆcÐcoÆÞµWZ	ômÊ·¶ù[['Y1f_50öî¬½0ð)\x001d\x0017PØûT½
\x001fZïñ¡£\x001989Ñðþ×ËÕÍâõÕåÝÝåâxuóñúöj×¢	ÃÀz\x0019\x0011¹ât4Ô\x0019±_\x000f'×GggÈ{òòøôh\x0006°ê\x0002«V`çù\x000e¼u\x000bhË\x0004W?\ ÐN«»´º'ýÇ2>\x0006¦Ýi£5]ZÓLË\x0005J`Í#ù¾Ø1ÁÆ|S§u\x001b¯íòÚV^FÚ°\x000fÇû4¬[ûpOÅëº¼®W²}r:Îñ°w©G\x001bãi}Ö7Ò¢¶Êf í\x000cBZ»^\x0014ä6%<ÛhC64Ë6b:;\x0003ËõZÈ>\x001b\x000ewn\x0007]àØ
\x000cO$Éë\x0014k^L;²Ó·©<¼	¸\x0013yCS!Zq\x00016;û¾Ô¤*UöXmªû¬%\x000eCã¨hwÞåâÕêþþòîããÎu«ú Ð\x0002%µn¥\x001b=ìpk\x0005-Ð;\¼Z\x001f½¼Ø¶\x00141U\x0017SÕcb\x0012\x0016÷<Qo°.£&1þº?¦îbê\x0006L0\x000c9¦õµÚú¸ÖÆx?ÊU@¾\x0015Nõ>ù3L×Â'?_]Ý<üÛùãõ«w;òpVñûI8y
Ìr@ÄúÁU:_\x001e¼Y_\x001c¿>z>\x001dO*hª¦ªÐ\(·ÜÆíÕ\x001e7\x001aî¦»hº\x0006ÍZ]ÖÒá@	øëòv·z/2Ó%3UB\x0003íÁ\x0014V9:\x001e¾Á/ö0¬r¬$³]2[%3mËRA»®\x0003å¥®YJ4ßEóuk\x001f"üûer¦ñL\x001e\x0007¶ Î\x0018&\x0010c'x¿øuu÷þêf:Vk¼\x000féL\Ûµy|Äáùâ×åÙÏG'[uÜ0û\x001b×\x0013èfãEn:
j=cHsr.è½ü5xº§+ñæéQÞõP° ¹Øqsâ¦\x0002ÏtñL%dO&\x0004éÊI¬÷%émÌ\x001cVÐ¹.«¥ó¼J\x0017g\x000esM´eæðæÌu\x0005^èâ:¼4ðñÖ[¢ZOHß4â¢\x0002¯ëýuó®sù,Oò÷~­ñÊ\x0000D\x001fÛ¿®\x001b*\x0016\x0014ËëëÕ»Ú\x001cWV¸ÎÉ9W£¡>¯Ïç¦ÜP½¸¤^ª!«óÿ
º\x000b©[$iy $|`LÅöÌ\x000b£ÉR
¦\x000biZ$é9Ã\x0019\x0012®T\x0010u\x0018¶\x00146@Ú.¤m¤äz\x0019Àá$'n§äêÒáÜÐ\x0006H×t
²\x000cáÆ\x0016!Ü\x0010b\x0019\x001dïöFô]Dßò±\x0015OvÂ¢æ9\x0018mË°&¼Qö\x0018e\x0013¤ãñºX]rî[8F\x000bÒk(ÕPKª^ýÖjñluwwõ_ÿçn\x0017¤fE\x001e/i÷\x0018Xjã\x001cÅ\x0014~¶<;\x0017ü\x000cJÕ¥T
Bpÿfè¬ó¢¬b\x0019n7i¡Ô]JÝ@Ùõ)2ÇâSL"ÕPÚ.¥me¤5}\x0001Þ<B&\x0008.8\x0016ZgB®5 Kª\x0001=¾}¸º¿¿ü|yó°¸\x0006\x001fãÅê;üåD7ncË\x001fÝÀ÷§øá\x0005}Æ
Mãñé£óóÃWð~ÁMÎ/¿v5VÃ\x0012Ñ%6ÑJÓV»2I9®_1j8ï¦\x0019×tqM#®\x0011|V5¼¦)\x0013¥©ýpX3®ïâúF\\x0010iÖR
+¨pSáNa\x0005X=­:¤]<»»ZíØ:nÜºj^ö8ì¢äÇ­¬ggGË\x0019 ª\x000b::´s@A¦4T\x001fGt9\x001e\x000fÁ>\x000e·²µê.¨n\x0001õewë¾`Ã-`>\x0018û\x0014 ¦\x000b:ºW³$ZÂË8AaPÿ4\x0012µ]PÛ\x0002jË\x000c`\x000f ¬ÁåÉÓÞ
]6P×\x0005uMÉó<`/\x0005\x000f
	{Pü¨À¼
ÔwAG:j\x000e¨VÔ\x0013ëÁí£â|n~Jk±2t)C\x000b¥,c=Ar%WãxÓwÃÚ±6ÐØ\x0005- Â\x0016A».@°¥¿'\x000cÛ@K\x0010$k{ÑBöhÉ×ù Ê~¥ívt\x0007((¥aíªéÖ®\x001eß>^Ý/_§lÍVN¥E\x0019"¦@Ûg³dµæ¬¸\x001c¦Å©øäøôâè|ñü8%lvª.¨j\x0000ÕRqµ7¨xr¤p\x0003\x000c¾ìp\x0014c\x001b¨îê&PÍ}^=PvP
ÔtAM\x000b(&Á	\x0014\x001eÎ\\x0010áÊúU3\x001c[Þ\x0006j» ¶\x0005\x0014\x0007§è\x0011¨/o'\x0002u]P×\x0002
þ\x0012Õû\x0007ð
W\x001cñ\x0011\x001d¦gÛ0}\x0017Ó·`È­~\x001e#\x0010d´,o=·\x0017¨\x0014ý\x001c-þr:¹|ü°[ËÓP]\x001fØ\x0003åÎ\x0013/P ðN\x000e/^l£CªØ/÷Oé³ÅÜ\x001crp%Lxa#wÝMÝqx0÷\x0013iïVïW÷\x000fðßË2ÄU]\Õc»Í¼2çHGyåf\ÝÅÕm¸kæÊ²^®+6¹ÉfZÓ¥5ÂíäÝðãüóäÐJZÛ¥µ²Õ¶X§´ã=Wíéé.JZß¥õ­'A\x001cÈ¥æt¦P)f©÷<·àñõks"O7þÛãêîáêònñìòúúòë./Jy\x001ax
@æ\x0014çÊ0\x001cÅú·åÙ£Ã³Å³ÃããÃß.f\x0010ê.¡®% ó©R[ar)ÒðÌ6j÷F4]DS¨M©Ið¬TámB½\x001a­vk@´]D[cÒòeK\x001d.\x000fë}5Tû
®Kèê¿³¤å£Që4R6	Ñm÷*\x000e' ÌE\x0014ÿ|ø¦Ô\x0007G×%Ù¢ÕãË+\x001c¡îD\x0006\x0012?½ùô_ÿ÷îöæýåõ=üs0Z\x0014Dz«\x001be¬S\x0007ðÊ8ç\x001d#M\x0000.ñ/g§'?\x001f\x001eÿô|yñâðèÍOïn?~¼¹ä\x001dSÀÿ\x0012=\x0002Ó¾>QÀ
çÉ%Ô©\x0000\x0014püs|{.Å×ßÝÝ÷/äP \x001bñóíãÕõÛÕÃýV K\x0011V£ó) \x000c \x0000Õþ\x0000\x0002\x001c¹år
òóéÅ?ÇÏo¦Þ=üefÓÀã\x0014Õ\x0002Ðà®Z¸`Æc \x0005i4Õ;´Òä/4FDq¾[«<\x0010\x0006
Á\x0008ýÒV\x00188f¦æC¥}\x000eI4J 3Dcc Ñè¼è¬\x0006þ§Ø
Ñ`øÈ$\x001aí-vt"L#Ìl¨ë«\x0006\x0014«
Øe¬\x0006DÙH¼>Y6Æ\x0011Va/ÙÀ
ð³i|!õ¦s#FbÎ"\x001f\x001b³×
?aPm®h¤Ï\x0013Ò±I\x001b­\x0010F[¬oÊÇÆìõ¡àÿ8V\x001c\x001bl\x0005%Ñ\x0018;Ôh¬â+\x0015ö:6\x0018\x001aÃ?f\x001bÜRïTÚ@NwJc\x0012$)?xîªx¾.ö8d:(Nj	A\x001c\x00111T¥CZq@\x0011Ë
e\x000cf:UX tL
t¦£#\x001d	Çù}.\x0015Î\x001a\x0015úO¢Å$\x0018^ORÆ12Ln@i\x0001Õ'ç«?\x001f± \x0006\x0014>ß*¡\x0003cÚüÝ\x0003ºOVè?lv$Ùà\x001agúP¸«.\x000bG«½1¨+Y¡ÿNÓpTªE	\x001fA*G¸¸ÝÄIÂ²F\x0003Ú,ôÏ
\x0007\Qºár/ÃÊJÎWÀ\x0012É¡°p¿³ÑÄR\x001b\x0012¤©}48*XUh?\x0011ÂA 5@Ù½a],}.¡j¥\x0001Å§j\x0014iä3\x001aaò#Ä>¦\x0001ç\x0001«
åmº|p|Z£¤r®éNÑ\x0012²V\x001c8vj¾+

G\x001cdw\x000b\x0007ÿG\x0012ü­ä^ú\x0006ÕªÐÅB&
ÆO&3nè
%¶{ázP5Ú\x0018×!ÝtiÌ^sCüöÀk *´1>\x001bÈ«°åV\x0019:7Òìe¨°ðRÕø¢ÁóÊ©´Æ9})©Ù\x001b·\x0017\x000eèa5_\x0017ãøà\x0018xê9C\x001e\x000eq)â>ú\x0018çâêù\x001a09\ôø5Ñc\x001dvÆqü±ô^\x001c6õ|\x0003\x000f\x0007Y®N9ü±\x0002cÚÊØ\x00037\×ÜrìAþ\x001f89t\x000b
<µö\x0012\x000eÜ(]s«¬?\x0010\x001c\x001aìr©b<iªl+
\x0008VW8\x0015Â­ip\x0016µÏ4¸ß'ÓX·Ëeà\x0010
S\x000eú\x001f\x001fS	\x0007\x0007pÒæ\x0010Ä1éE]#£¹vÜÑÌ®.\x001fÿíç«Trð\x0002þ|\x001b\x0013hAÜlv\x0011ý\x001e@²1­IÀ8\x001a~¯ã£ÃÅÏG©Üà\x0005üùD¤«CcKUT\x0012ÜÀìiÜ2\x001aÒ\x0015\x0003ÍHQ\x0014ø?\x001aÞøz¬\x001cdªÃ\x0012ÆâXäòð0v*K+PÐ\x0000þoeØ+Ç*Åå\x0003yeððØ\x001eäïâÄ\x0005ÿõq_®\x001cyª©\x0015å¥\x0003-\x001d+\x0003øÊ~o¬\x001cô©ÃX[W\x0016%°8~)9g°\x000fW¸TratC¸\x001c""\x0017~]×P]Usq°£ò|<¼9	L\x001cdyáÈ\x0011rM\ôí§Ûß;ºë·«ëëÕÇT~rõñî\x0012[ÇS	ú´Vu\x0016ké
 có&Ò¥\x0004w0\x0015\x000fV\x000c¤öÛÑññòe*D?9zyv
äg»\x0019³&kbÄD:\x0002\x0006¾\x0005\x0002\x0003}\x0004\x0008NÅÓ\x0000fÖ\x0002h¢N\x0004
¾ì³QkfCCÐÊõ[\x001b#<bùÄJ9zü\x0010\x000e\x0001lç\x0013}æ¬é\x0008áü©HRÔh*\x0012aZ×¥ø49îÞDhó<\x001b$\x000cæÀäËe|0Úá#¬1+æ\x0016F\x001dÓøÄ(Ò11r\x0016{¢ûômräG\x0000ü/×\x00121úhIÆ¹§aÌ¤I*·ë\x001bì¥5¬\x0018ñm\x0019½×êI\x00189 ß$H\x001c\x0013l³ 1Úå¨\x000cGª$Ý\x000c_ EZ\x0004ú\x001b<x·\x001a|åèYñô7þ\x0018Czß$9bµNþÖi\x0018M£\x0018fª[\x0019)!ÐÄè\x0002¥#q\x00046]&Ho\x001dlm\x0006\x0012\x0005-
\x001eD¬5ÎlÐùk{­IûHýD_Ò\x0007M´÷\x0018¤Ä÷$úÓdh\x0019øVHÊ*4IÒÃ#ÎfIF\x0005ãIÖ³5ôêÎ$å\x001a$-+.CzOAR<Å{ôO¤$)\x000bÑv&#ºdÙ¯pØ\x0016Ï¤ÕÅ;{3ÉÉ¶3)²ID5)Ø$
t}IMºð4³hêµ$\x0007ZÑ)5¬&Ã\x00131R"£Ín\x001cïD
/­\x000c©\x000c©É ÂÓ\nNo4\x001dÉè#éDe9\x0017C\x001a(bzþI )ëÑ$I§¸&5Iº\x001c/·ü¹õÓh Î4IÒòh@WÜ\x000bÍ:'÷g¤\x0004IÛµ1\x0014`\x0002Bae¾7l¸Ý0ë×ÊH\x0016FáR'Rb´*\x0007Á\x001coà»­özÚ|}ôïï?vb\x0015/Vo¯.·F|á¢º4k\x001b\x000b\x0008£Õ8þ\x0002\x0003\x001ewd¤\x0002Bm\x0019Á\x0017ËgGç»\x0019r,b\x0016CÐ$\x0017\x0013@EÇà)\x0006{\x0007\x001a\x0011r´a\x0016B\x000c\x0014\x0007´éE\x0011b¶\x000cð/b\x0018\	s¿D.÷2\x0001²óÄ\x0010ßÈPâî\x00109^0\x0007"ü5ÉÁz\x001fáH\x0010ÆÚ6AäÀ,\x0006í('bÐ+³ùc¤ñcùH°Y\x0010;\x0019òkz\x0006\x0004Ñy01X,=Nqt\x001cGJ\x000c¢í@ðKt °«Zúü1#ÏÏ:
Ö ¶\x0018\x0019æ\x0008~ÇÍ¢\x0000»\x0014ùHh\x001c\x0014à#k>\x0012²íHðCm\x000e\x0003n1·ÒK\x001c ´ \x0008kNðV¿Â»ðýjsX÷xõþêæÓêÝ®¸Éåßøt(5v÷á\x0010Ð¤&?^þ|tòËòùn¶Q8w&[ùüöRR\x0017c¸í©=n\x0014ËI§myÏàK6µ
\x001b
?ºµMt£(îL:ìs¡°òØCåC,ºa±b\x0013Ü(;\x0013NêÔ1´\x0012º\x001c:\x001b¦=±ùt£àíL:lj#7Ñ9lÇJÇN(v¸voæÓÂ¶s?lHc5PvFrÉ°P\x001cÚ	jX\x0014ÑD7
ØÎ½²>W^j\x0016Etâ\x0010iéíþl£@í<6Üßjd\x000c»Í\x0013üDÁ¨Ùþp\x001b"´3éÀ<\x0007:u9qY¶r]]'MlãÈì\¶ÜñÒ¸É`è¦\x001f óáÆ!Ù¹pd×qkL¹®ó,Áè'8s\x001b±séTö}paLê\x0011É¢[ÇjÀHlÂÎ¤CíKWBsù\x0007~d\x0012×["IóñÆñ×xð`\x0017ò*zÓ$.ó¢´Ê°s¤n\x001cÓI'uÑ'!P?\x0000nç£Ì\x0014¨â'¸\x0017\x001b\x0002sñT~¡\x001e1Tª\x0002x\x001c'ê\x0013HoCp\x001e\x001ev-°îóÑsQp0fØÛÑD7\x000e\x000eÎ\x0014P\x0007\x0004\x000bhsÉ>nÚäüÉ00Î\ÿ°7?\x0006ed\x000b¬\x0010ùõvG	óÉðcÈ\x000f[óÓ\:ª7×üzz1YÕÖÁY×ÍÃñ2a8'-âÔü¢Ê½Áñv¢uéØL\x0001Á;;\x0002ô¾1o\x001c©3\x001bG
\x0005µ@ë±¹_,äB#øhà~\x0004"2¹ \x0007>ÚHGÔ\x0012­«Åf\x00129êT\x0004\x0019¹4/\x0011)*â±Ñ\x000f3\x001cµDÙí® ÂëEä,¦¨³ò»\x001cDd÷=×Ù­\x0000²6çü°ÊÀSk©µl6\x0010M\x0016EÎ#b'±\x0002I¥A+ùòG, B$C	>'´Ýï£±÷5È¢Û\x0015è\x001c\x0003Õ¡\x0016\x000c8GnØJ4\x000bémPßÝ·v|¾º¸¼»Ù®°´Ò\x001d\i\x0018peúfÎz.dÕj\x00188¾<sxv\x0002zz\x0006\x000b7ÔÏc\x0001w9Rua4ÔdåçR_-A·*\x0016n«Ç\x0002\x0007§ÈªÍÅ3(a\x001d@\x0015IÖ3IX\x0005¥âX*Íd©\x000ccÓU,Y\x000fÎæLÆ\x0018uÌbqÂ+b	{±d
8W.ðd¶ôÇ<>²ÀÇb\x0016#Ô\x001e,9Ì0û´rZp¥Uf±ÚØq\x0005Þ>ç%+â¹r±B¥ RÒì­ðE.û°ä ÂL\x0016\x0013ãÍ(ÚA\x0000+\x0011Ê'\x001aÖ Õ °5+\x0017é2	ø÷.°/ô°6s7I¸þëÛ÷SAäÇûû]DAÂ	NÏ4¯µ§z\Hn~[Àìâü|ÒYî°m\x0008"ÏaÃ&ÉGõ
ëwÒ3Ã\x000bE4«£ÙöÎÉ¶!¼MaiV~}{GÓ!rô¾µÚ\x000cÛ\x0006[Ø6\x0004çÈ-¶\x0018KÁñdIn>2ßR5mCüxÜ|Þr³Ü\x001câµ J"«µÜ\x0016ÜÉ¶!z<Cn³ÐüMC.aô\x0016\x0008Äfý-l\x001bbÇsä\x0016\x0014ûµ\x0012îi\x000e§x­$³É­Il\x001b"ÇsØ\Äh*ßØ(À\x0008d[Ê\x001efm\x001bÏ Þdû\x000chFÊõF\x0013\x0001\x0012ûkaãYpyË«Á1,7*¬òÃ\x0016¸Mqã9pQa3ßSI\x0011(o\x001cxàn@ÍÛ\x00147\x0005\x0017°3:Á	Nß\x0001\ ÏªF#+Zà6gÀ)ÍObi4î\x0008C6\x000b~\x0006\x001f¹­\x0019¨lÆs\x0004Ã5XÃ	²öÞØ\x0002g¶\x0014iÏÛ\x00142#8c\x000b\ÔÔê­â»ê¶æ³g²m
\x0018Ïa+ù'¯rV ±\x00051aº&{;üôn¥þìxpG¿à2Ð²ßüæauu³µª+´')\x0001mK
ë
\x0015ßGÌÚöù^½Æ eÑùÉåÑÉÔàÙ\x001eeöåÚ(-Õ$Ê|52X¦\x001c¾
Ú)³W×J\x0019\x001dQúµ,#SáÈvÊìßµQzn÷ÇÛQs¥dÊa\x001a¾2{zmF}HÁ­Ü\x0000©\x001cCú'\x0013evùÚ ËÈ
)\x000cÍÆ\x0003JÃ'\x000cgãµSfç¯Òé´H\x0000)u)P´D\x0019ä0ÒÐ\x000e½À6ÈH\x000eóW	Ñå÷-"Ú';Ù\x001dlB\x000c*DÒRaõðÖdÊa%q%åÛ·W\x000fW\x001f:
ý\x001fK°1oo\x001foàïßîÈÊ\x0004Iº\x0007Nb \x000c\x0002Ìl>L¬á÷òÙéÅÉÑ£Ó	\x000bÓ\x0001Êº»\x0002\x0008\x0003\x0015¹ðNâ(\x000f9±.Ò±\x0003U8Ì8T\x0012e=]#"K®µ\x0000\x0013 \x001eA ¡\x0019®¤Éú¸\x00067Pø,\x001føvÙg±Îä1w(\x001fkö"Êº·HÊ´\x0011'ÉÇPYµ\x000c\x0003.NØ\x000b(ëÙª#D­b8ª'M\x0013J\x0017NÐ\x000bqø<¬\x0004Ê*µ\x0002\x0008ózO¥G¡G*\x0012r{\x0011eýYóÍÀ»Ìî\x001bØò@³{,'\x001dÈ\x000e;0*²º¬\x0011\x0018n>E&Ò.k\x000b\x001e*ëøÉ\#£2ö\x0001¼2qÀW_Ë"£a~¸\x0012\x001eÊ5BÒz\x0006à I\>\x0013{|ù\x001e¾¦*èy\#%­(9\x0002R4\x001cÃÚèbÒ^\x0016\x001fÅ5H"-AÏHi_ONì;¾nv\x0018¯D¢·pÍS|©ôáÈ\x00070Öéòáöºoü\x0002®A
æ\x000c&Or\x0008½pyí^¦\x001f¾5HÎåÊAD¥"æ­\x0001\x001bN\x0017¯Câê¨*µ¤sT
)\x001fn}¼GCB*¨æ¨\x0006Éè@A)\x0005\x001a®h
.È#¤\x0006µô¸ûüémÇ|µú~suy½
Åç¥ï©ð)J¶"\x001aãÅ\x0004þd`ú_-ÿ~rtx<éÊv0²ç8\x000bÃgqh,MpÕ òéØx=ì\x0018©ÀÈîâ,\x000cÏ'r\x001d\x0018vVe½£5·¨ÃSe8î©#;óÄ!5P\x0014¸¸=×£©(ix\x0003<ä]è\x0015\x001cÙ=Ç¡tª¯R k\x0004%^Àç¡\x0010\x0011¼:¯\x0002#;³0À!&Ý,\x0003#h~ãØQ|´#û3Å\x0011Há¦î¢ÜÍ£¢Öto­\x0019Ö»Wpd\x000fp<Êý\x0014ð]¼=ÈÓîgSd¢ªÄøöà¯¿]v[0á·}æ^\x000c8\x0006ò\x001bú\x000c(\x000cöZ¥Ô4\x0000\x001c¶ÁLÛë0P\x000bænh%ÝW`àáJ¸Qf4j7Ñ8z0gÈA;ªç\x0000\x0006M­ÐØoÈ\x000c#+<0gÈ\x0001V\x0013B\x0010·\x001fÃøÙ\x0004Ô9C
B\x001fø\x001cjòàâæ¼»1e:¥\x001d6[ÌF \x0006Ì\x0019\x0008x%é@FÊ©1:FÖ\x0003uÄ\x000c\x0006Ü1 h.&èÎ¬1MJgf9á ÊÙ\x000cÔ\x0004:C\x000eÒæâ\x0015\x0015à#æÆ¨@\x001bM\x0019ÖWÎFÈOÂ\x0019\x0008hÎ)¬ç¤Úe£\,\x000b)Ç¹\x000c¥\x000fuÆ·\x0008\x0013\x001cÁøÜ\x001bmtdýdìp¶Þl\x0006zöÍ\x0011á~Ü4CÖ Èã\x0010Ùax6\x0004·ÂÎ96×Äà¿m©\x001f\x0017\x000e%Ïd6r\x0018ß
Á­°3$á\x000c5ìc¦\x0015£;I\x0012ÚÑÍ°rÔ&>\x0017\x001es3 àQKc+\x0014.*ÎõnF®·¨á\x0000Ù\x0010ô|#	8\x0008Y\x0010!jÜî\x0004¡xî<\ÏÆûÉ#æ\x0008Â\x00186ZðG\x000e\x001a\x001b\x0011xð3îBjd 7ã\x001c9ÄÀÙ	\x000cæF.ÐSî\x000eÃv¹\x0010üJs7¡ªC¸<ä\x0019 ¨a^èQ\x000bÁl\x0008z\x0017Î\x0004<Âx1Ôog¤çÅ'àBT\x0019põåÊ¯ZN®/\x0017¯no\x001e>]^mw1½VF\x0005êTÈ»@g$	p\x0003ÅÕLúêô\x0004þ£ÃÙ«v\x0000\x0007M(³\x0001Hï¢\x0004Õ\x0013I³Jí,\x0015K;4l\x0004Üüîð
ZRæ\x000b0XÔø,°¥6ÏÍ\x0012àN¾AÊ|>WJ¢ÑZgQÂgçQ½b²/¤oÐ¯RÁçË\x0001Ä¶@æ£Éýp\x00009·6¾A÷Ê|>\x0013È»ÐiÞEîUð,"ùBm|fª\x000bÌ£Á!WÄçB\x0019Å<ê6ñZ[*\x0000©S\x0016\x0000áñ ï\x0007nÅjæ³÷_åý}·«äñóÕÍj;\x000b 2O½»päò4agËtÔQçùÅ«£åô³úýÝÍõýÛzxµx¾úË"¯våeÌ@
\x0003\x000e¹É©0N\x0000O¿aÅßZNËÅóå?pµäÑtê¹Ã8TÅ³\x0019#XNÚ¥ç\x001e3\x000c\x0013ãoYÉ8TÇóå¸ÞÕX\x000bh\x0006Ef\x0018blf\x001cªäùr\x000fL[\x0015\x0014:h$GÎ\x001cfÆ¡Z/GpÕòZ$Ç@çÑ"Ç§\x0012ãz\x0000}­\x00181UÃW=l\x001b¸s\x0016®Ìp\x0010S3ãz\x0018}-£õ¼PYÍy@JA£*ãVÆî`úJH\x001d\x000c\x0019hê6Ø5®rjÚ\x0006WBÂ¥M\x0017\x001b+:xÝ¤2
{m!å0¿Ó\x000cI\x000fÍ&H[¤V\x0004éÒe\x0014Ã\x0015uu\x001fVï®ßdiÝ>Þÿùx¹}\x001foH\x0011Üô¥-:¨¡r¶¨bôS§ñÙéÅùß.\x000eßL¹ú\x001d²}Gæ¢£Ïkáñ_ª\x0017&i1Õ[°6;\x0008\x001dªEK%Q=#µiì[Æâ\x0011g!L\x001eºùd\x0003;2Ì\x0013\x000e¨æÅmjyàSa\x0014´là4Ï$\x000b<ÞËZ­ypK\x000c<²1L¿vÙA¿ëþËûÅ³ÕõÕåÝö\x0001m\x001e7Þ /P¸5>\m
CÙ8\x001cå~|x¾x¶\x0004´³É1m·¯¼ïn¶8^-W\x000f»T DµÆ±Ùò<U>ÑÍcL\x000b¿9Ô
\x001d\x000e²÷³8¤¢³­$6¨jªß+\x001cb8ÿ§ú,\x000e!\x000f¨xÕFêµ:¼\x0003æ])ÈlÏ¡èDS5£g\x001bÈ\x0018vxfc\x0014Ë<\x0003+Ð#®*ÒMô\x00111¢
\x0010¶¾³@Ð]ÉÇ\x0003Î)?H¤R¸\x0018é®
\x000e6°³8àµF\x0016UÙ2Þ1ð»(Ä=>\x000c\x0005Rgq`?7m­,6\x0003&\x0010Õ\x0000¦}XÂ¼\x000bÄ\x001fâM¯ãæê¿þÏN]¦âbiÓjÖe`Ü©Â©á3ìÕò$ë±)wúæÛÏ]Mvû¸x}·zHõÓÿý\x001fÿ¹üþq«||t½qüçÓb\x0014xôË\x001c(ÑV\x000e÷¬\x001e^,^-ß¤êéÅòï/§J^ß¾Fë¤íKÿëênõyµ]`ØèÓ\x00012zï©bQhÃsÎÐhMX¤ÿut¶|µ2\x0000\x001fîxÕ\x001diüÛêÝ§Ë»«TvþruÿnÇ´
©À\x001fËý\x00058%j\x001dvÆçCeåhõÒò9üÅQ*9¹<Þ¹1	G=ÖupÂU7\x0016G\x0012æÐ5ÁÒ\x0017\x0005øa_é\x0018nÂrÆ«÷ï\x0006_4}ÐW«»Çí\x000e\x0006FhÔ
®B \x001c´\x0014Î¿·bX
P>ç«åÙÅwáßUÊM¾õëË»¯W× »;§$4Ï\x000cÙ´<\x0017ÜnF\x0008~Ð[öúðì·£cø7^^l¹©\x001dÊ]C)EÎÛ\x0002¥·%HRÖ,ééSÕ\x0003¿»\x0012Ðt\x001e©­ç¡×4´\x0002 GËNÚ!\x0007.x\x0005¤Ç-àyL¡ÆN]\x001eLãÎ´qSg±\x001ar\x0010Ë©¤£ª
g©Ó\x001cÌ)§r2
QM9x3Ô\x0012\x0013î¥Ù¶Ö\x0005OY-wÛ)\x0007A§*Y:ô\x000eRE³%ßÛ\x000f¨\x001cä\x0004j ÎÆ\x0018D)\x001cps"µ8âÉ>ø 6VC©4µàG\u£Iw)=,l¦\x001cå/j0u^ \x001f;Ê­×e9=È¬r\x0018Ã«¹=<n
d©\x001erô\x0002YN®¾¬¦\x001cÆÇ*(]´<\x0014Í¸'/ÚòõÃ6ßJJõîëý\x001f_\x0007!çw·?.·/\x0017ÆE¾á@äL\x001f×§(h
6ìhK\x0019\x0008^üãpËzá\x000e\x0011\x0019ì¹DàÒ\x0008\x001e!\x0005GÛÁÓ¦Ê	7Ú¾2èúòÓcXM¤«~[]_><ì\x0008sâ.ZZà-\x0002NKG¯58r\x000cálrþ¶<>|óf:ÆÙÁ\x001bgªæáÒ\x000fkÁÜå©#\x000e7u\x0010ßhÀl
ßýßßÝ¹\x000eß³ÕÍ®}
àµb.u\x0002`ùb\x000bûh¸\x001dH
ë\x0005-O¶\x001có\x000eCv]f0 áÊCÀà¨s!/<È&àÜ]UÃððáA¾ÿÞ9F/oïîw¥C§j	,v9 \x0018¾¢	AI3¸þ/OÏÎ§?E\x0007!9\x0008ÆR\x0012\x0013«ò¨|Ô\x0006VAák6Cvuw3H½ä\x0001=\x001dj+\x001bCpf~#C>\x000e³ä 0\x001dä\x0000\x000f½\x\x0001ràã \x000cÙQ#\x0007¬X o\x0011KÃu¤ú´#\x0017[¿Evðf\x001dInÓ\x0015¸KÒ4í\x0016\x0019\
Ã}üK}¿ñ\x0019¹z¸¼¾Þ¾	×Ëð2+ô;ÒW\x0001Åe9¶£§ßË7ÇÇ³À/ÇY``\x001es\x001d\x0007<\x001f\x0003)ULÅ):M¿!vßÝGe7E\x00030ôtxÿp·zõ_ÿwëw\x0004\x0013Éó\x0016\x0005Vç{ÊGÐåRúÃó7gË¦VWÇOöfÂb>[Ý?\½ß!=së\x000f\x0005Î]3¹\x0001KY¥\x001du[Læ³åù£gÐ
æ,:,ñY\x0017 Á´&÷CÑ\x0002µ Ý(´¹\x0001n"\x000cÕ¡\x001b\x0017uÌ£\x0003m\x0019Hv8\x0007(Ó©@Ã#\x0002vE>ìÆ¥\x0012óè§\x001eVa¦\x0014¡ÖEj5\x0019ÚI÷M}øýÓ§~ø=xÚ;F\x0012	Ìçä¾CxÒþC£ D\x0014#¤WËÁ¹Þ2M²Âý~óPÐâ'\x0014Ü¦\x0007\x0018p¦)É$Æe\x0015$Üò7\x0004\x001eÅT\x0014Û¹<\x001e< ÊÍýX¸ío\x001e2<ÌCkî2¦À\x0016®ÐÔ{pßß<\x0010)(,qG*õóàT+b±Ã\x0007Y\x0015\x000b7ÿÍ`ñi\x0017\x0004µñ£g'Ã\x001aÓ\x000b3Ë¨õº\x001bïf±àVµÍ*ªÒqf¨\x00151aÖ©\x0006\x0011sY´ÃI\x0014Y.Í\x001b\x001b¸ò\x0005\éj¹wáÃ¥ÙdÑÎ/ßÁãôË\x000eÇ
Ëÿrä\x0006;Ñò3Þ%·+=ã½4gçø@}=5mÍ5°eó¸¤¥ \x0008:O4N=:sÂ\x0017
/ÌÆ\x001aça©ÀÛb0ôc3\x0017*À»k¸¢n.ýË¼¯x~ùåáÃ®>â
¤­dW\x000e_õù@I1¼ôç¯ß¼ØÖÐ!Éßm\x0016Ç\x0005á¹Ã\x0015JP0\x0015\x000ci£\x001aü©æà`\\x001afã\x0016RJ	´@Õ3ìZªáÈZp¦D¤á	4ÊE²Ýé©Ê¶{PØI¢ßs?\\x0005òoìãÜÞí*j3gKÜÌC·\x000b#ìh\x0002ZÏ½9=tªíÇKõAwUÐíÍÇ¯öm;\x000e:úyþpCN+O\x000f63Þ\x0006rzòò7 ú÷I\x0011­Ä>t\x001d­³ÇËÅûÇ¼_¤åDÛÄ×£ÂÇRhÜÓsZ\x0008\x00147°pvq¸øù"ý#gçù\x001f1/Â1¾«\x001fï®¾ôr§XuûøáÃÎÕV©Ü\x0000"±at#÷Ï\x0004xøêÞ±0ëôâÅéýîãÇwºsÖWóÕÇ]óßtôTo´+\x0013r$u¢á®68ßçË[Æ½u0J}Øÿ\x0000z÷ûíbÀ»ærqqýy»&$=»$®rÉº\x0019þñ´	$ê8ÌÎÀcæpqqüjjé·wB|éZ«ÕÃÕíÍâ=¼òÿëy¼K¹+\Ãý`RoM²¦öCÏãüÍòÍÑéÉâçÅáë³ôç\x0013¿¯·7]-ð|õùË§ËïÛë\x0011bj\x0011Ê;ª-NëJH:¨HUµbÔ\x0005ý|ùêõ/ªDèpð*9\x001c&÷$\x000ep_Ó
×1Ðj!s\x001a
ÅÄË½Á[8faàaI\x0014®ÌÕ6©c4s¸¡·ºãÛí\x001f_ú9ÅóO«Ïo·\x0015Á\x0005,NyÏOSWr\x0001vÃÇç¿,_=#2éÆ¯i83\x0006{Äó°\x0017'±sÁÐT\\x001b\x000e4qä3WÑPte®l,-)ÿ\x0010ø\x0019yÂ¸w\x001f\x0015÷h3\x001ce[GCÑ4\x0006Wëø,\x001b\x0011È¦+ln#Qð\x000c\x001aq\x001bÂý§¾\x0015x~{ó°ÝßÁ^aA}ô©ÅºÇU¤ÖàÇ\x0006ËÅóÓ7[
÷¿¿}wóþMï­³ÛÇÏ\x001fowy=\x0018ÓÌáÍÈÉ¹r\x0017Kïî\x0007Ä«Ã§[Ü\x000eÝ F7Îp5º\x000cV­ð\x0003NÖª«+àÞ¿ýöe\x0018POîë³Ç;´\x001e¹Á\x000e@Ë\x0019^ð\x001c=·ä{\x001dx \x001f®\x0007ZW¦_¡	9\¬Ö\x0013ºûS¸yw½öåÝêæãîä¥	\x0012wÊ#¤t 5dvá¹=	ùòlyò2å.7³wâau×aã!¹¿^®n\x0016ÏWwpO·Ï$Âò\x0017\x000e\x0015Ã-pXEª!hÍ\4ÓÄ=\,/ÏàÆ\x001eNõsv\x0000û£Äk\x0000Î£âqÃ£qìÖKvt\x001bn8©"V\x0000×£<\x0018Ò¬á\x0019\x001e\x001e&¨)Ò©t\x001eXi¹¶ÚØabrÆÓáí¾^áS]>UË\x00175§«=h@*yqéF3jÏ'ä@~ø§ÃyÍ¯n¯/·\x0007ÞqV+\x000bÁAUeMåºB\x000fúÓ_\x001e\x001fþ<TuIGãíç¼!\x0000[\x001c4Y~k\x0015¥{ãx·w\x001b©îFÜÏ"Å°'Me7º\x000cäÔ´L;Q¯ÔtIGcîgÆHQ\x0000ì /Sh-7\x0006\2ÓNúVÊØ;§ÏàoôS+¬â¹úÏð\x0017ð7w=¿\x001dµÓj#-mÉ³v\x001eGz¦\x001b\x0003ÏNþ\x001d\x001fãðæ*©\x0006k1ÔL®£î\x0017o®®¯/\x001f¯wUAYw ²~\x000fR8\x0001<\x0007É«áØ|õÏ\x0017o\x000f/§ãPPu	U=¡ ap¸¢gÉ\x0007Ç¡y+±ºzBÝ%Ôõ¼Y\x0013Ê<Vðúm\x000c&}	MÐÔ\x0013F\x0000Ã{®\x0002·\x001d0¼æõ¶\x000bh«\x0001½Ìuô\x0008hy\x001f\x0008Ü"ÇÃ\x0014f=¡ë\x0012ºjB'ip	ØpÃãïÁd\x001bi~F=¡ï\x0012úz\x0019bÅÁÝe\x0011òÎ\x0005ã9¬ù"\x000et
ü¾\x0017ôjuµ+°,¢)nPÀ¦Q"tÜë:åf¼Z\x001emyo\x0015BÕ%TÕZñGËQF\x000c\x00185#á¤£6Pw	u5¡÷ì§Q¶9\x001c&hQXJ}íÉgº|¦/8*·\x0003	Z¶ÓQZ`ÜÏvùl%_*Å£K\x0012eä\x0008ß` õ¾Kèë	\x001dáyJÕÙhøeíà«7ã
2¢ÿÁÚ«×W»øÀ#×FËM\x0013plìÌ0¬ÅÃÇG[*é
 ê\x0002ªj@\x0001ê9?ûAGO)\x0006ápBd5¡î\x0012êzBÅc\x0006d\x0014ß¬±Üáa
¤ÏtùL=ÐyÔ¨\x0004©ñ\x000eH3\x001d±\x0002j³1®\x0000´]@[\x000b(b´<"\x001fë{\x0005\x0017\x0016S=:3\x000c@U\x0013º.¡k \x00144\x0017SbÅ©&=¨8,s©ö$ô]B_Oè<m?Â¾JV\x001f8&áìp Ä\x0010pu÷îòË$]èÒz:lÜ¥+âÙÁé®,¾aËA­ø¤è©AQOhËö!¼%4A\x0000\x0003v¸ù]RØ×ÔÕª\x001a>qY¾6!FÍ\x0017Ù
'HÏGôC]í\x0007þÖñjWì³a4ÆÚÚ\x001d/·5m\x0014>Ûå³µ|Õ#3ªù|Ï×òõFiP¡7Jc_ñÅ.^¬ÄK36b±AÍ_Îýjvc
B\x0005_çøþ
\x0007Ø\x001f¾¡ÝxøÆ¤·5\x0013P÷\x0000u-`(G.ì
å\x0018.®¨\x0006ì]\x0010Y{CÒ´\x000eIã:\x001c9ýq\x001dîôLÀÞ
µW\x0004ÇxPo\x0018ñ0ÇxðEa'_t;\x0000¥\x001b¶]
m¿¾^½«y·\x0007ï¹\x0004\x000c\x001b·-Þ£b4à05ûúxù|~la\x0018Öv)¬]K\x0019\x0015§lÁgu4æ	Æ<êÌá\x0016JÝ¥Ô
²ÄòsW\x001eð$\x0000E\x0014Ë\x0003^ïOiº¦AºD»P¬\x001cÒ4¶<B³SZ(mÒþÜ½Ír\x001cG.ú*µ»«ÅÿiU$K\x0014 .@ÈNk#+\x0012%\x0012\x0012\x0008P\x0005ÝÔj^ãìÕÌ}
½Éyë\x001eá\x001eY¨ÌÊÌÊ\x0014©1ASh¶òó\x0008\x000fÿÿ\x0019pQQ\x001aCâ\x001féÆ}ÉÙ¸=jv\x0008JWEé%6#HËàù,ÙÛÛ®(\x001d\x0002ÒWAú\x0001 Eàòòà%\x0017*c(gó·§\x0008\x000cA\x0019«(ã7RÖÅå\x0000yù×À¬½\x001e9äùõ\x0013ÙøV\x001ciòskOê¢\x00061æÏo¯ïëÌ¿øÆTmgªT	<]¯ÖëÕl&\x0001]¯fÏ\x001f÷\x0018\x0003.X¤du æ5ëådÙn\x001bA~v¼8?_Ì\x0016i&Ðñböü²5VÆU\x0015²\x001a\x000eÙÞ°eÊwË(¼\x001a\x000f³®bÖÃ1kC
ÃÒKË
Ã^q×Ñ»,§M\x0015³\x0019\x0019w\x001aDJ$ç#a¶¾ä@vÅï\x0007bvUÌn8f#8\x0018+;id°çm¦Ñà\x001a±0*æ0\x001c3ö³Qª	£èÄ\x001bR2?\x001fX\x000eáÍ/*úÏ_Öwí¥ARl"4\x0001÷{[êZâÞ
»=}JàÏÿyþºyü{¦ªÐT?h^R°\x000cÖÐãrBiÃ6ÿvPOlºM÷Ãflµ¢\¦\x0018¹ÔÂ¸íÒÃØL\x0015éMqd:\x0008n\¶ ^Ù¼?ðÔl\x0015íyjÍû".Á¿\)·==¯'6WÅæúa\x0003ùí\x0008[\x0010%\nuÁ¶]nÛ\x0013¯bóý°i\x001eÞ"1Úa5gkXüùí¥à=±*¶ÐóÜ\x000c\x000eþÌU	Õvâ2Â¶]tÔ\x000f[%\x0006ÂMô\x0005Go\x0014@10¾Ð'\x000b\x0012»\x0001{+¥®¶g\x0012\x0017\x001fb¯ÖÃõýýêãêö*¶þüÏ½%[V`@(G×¸§Ö\x0010¸\x000cÎ=mÜzs|q±xµ8}Ó­fK×äI\x0002k¾M°Bê-}ã\x000c7úìlíõ\x0017Ëû\x0006û£Ç%\x0000q³ù\x0018t.{¼»ìß\x00178{5\x001bì/æ¯ZÆü\x0014 ª
T
\x0002
\x0016$'H$O¥vØ=©\x001b\x0006TWê\x0001@SÑ\x0002-¿\x0010Êq\x0019d4\x0005ÐoG!5U¤fÐbµ3EáÆùN¤\x0000ËÝsù®Ô
B*%eá¨ä¸im' ;³Ü½*Ò0ì=\x0019\x001a¥ðiÑ¾õÈ~O;\x0019\x000f\x0001ºíýjQ	\x0013\x0003Ô»ë«ûÙÙãÛë=

Q\x0008¶Ì°\x001c\x000b
/!Ý\x00019ÀúúøÅÅììòÙÉqó\x0002UU¡ªaPÍ&õ\x0018\x001c3jp,O]Ø\x001e»5\x0010«®bÕ°Â\x001dS*erÉ\x0004	BdóHXM\x0015«\x0019x®2BI\x0000ÐÐÔ`cÁº=\x001cg V[Åj\x0007«¥ÙVYQQÔ#Æ"¬¶\x0017ö\x000cÄêªXÝ°sU¦ä`à.;=A;Æ\x001a¶§\x000f\x000fÄê«XýÀs\x0015¥r#F\x001a½\x000eçjhÝ\x001e}5\x0010k¨b
\x0003EVI\x0010
\x001cHü*ÙöN©Q°Æ*Ö8ì\\x0003O\x001aP¨½(à#\x0017ßy±¯\x001eUÖUÁ0]\x0010àEEnð\¾ã+6Ëvãø@°5e i\x0003\x001cíc~²âd&Ø®Ö\x001a\x0008µ¦\x000bä0eÊ.YÇÂ°µ9·]2TqÕB÷IyUB÷ý kN cbÈåACÎ³#bð³ê\x0016\x000cøY¢Þ\x001bË!\x001fo®o»\\x001e´Ì#ý1+¯©rÅ\x0018Çå]ûpEäåÉñiÅðjh\x0011aËì_$ëîñ!Õ\x000f,\x001fïï÷µ¦UÎùhPì\x0019xN'ký¤Hîõå\x001bª\x001f¸¼¸hÈT\x0000ª*@Õ\x001f Áº\x001c>IM\x001e\x0004°(T\÷Fhª\x0008Í·ÐU\x0011ºÞ\x0008},!(Ü`Er¿Tò=])ß\x001fa¨"\x000cý\x0011\x0006¶ú<8Såg9C\x001c>q\x0018ÂJ,*P=ä·vÍ²öTä·øVdí­ÈþÅ;vp=²çæx:l3ôX{,²ÿk	C\x0010NG\x001am
¯\x0011º'ÍnýEâÏ\x000f«u],â/úâLêrW^dgÙózh¥:ô(\x0001hEg øþâGÒ0ìàøáú/ù¤½3P)¶£ÂÖ´à«Ç5þÇ³åz½ú£\x001d§wñ_(\x001bÓJ\x0001qÛEK\x0005æ«ËsügóóóÅO\x001b°Û
­b;ð(lM!öÀ\x001a¬;¢.$m(<î-\x001f¨Ùöå\x0006"ÕU¤úÛ>USÅj\x0006ªIº'\x001d«âÖ\x001fÜvÄYKý$½>\x000c¬­µ\x0003Á¢!Ï}Ã;Ñ¼PÆ|Ú6\x000c¬«u\x0003ÁâTX\x0001²¹*¢êÉ·P}\x0015ª\x001fz®Å\x0015&:iVDä\x0008´	ÛÃ
\x0006bU¬q V!)´+=:s´%%Á\x0016áIÓî °²._
Ø(i9 \x0015Bvnc<©ç\x001f¶&·ä·-¸dM\x0016ÈÂÀcþfÂI N\x000eÅ5Ö;&ìFÛ4\x0001L-=«ªµàÇ\ EÅ['Á+É¯ËYÑ\x0011cý;\x000bñºãPÛ\x001aVUkÁ;£TÜa	(\x0005wë\x001bn\x001f±1ápºR\x000f@U\x000f´JT:^ðc\x000ceh¬\x0005ïÒTQ!(E®hÁì\x0013'IMÙ\x0008	æêîØX/¶
Ò\x000e\x0001)9Ø(q	££d\x00135:\x001c¥«¢tCØRÒ¤\x0010¬ªbßlfÄØív!(}\x0015¥\x001föÄ.==$8Á÷ä¦£¦>.%\x0011à#×CuÉiN£ðÒäß4{s~{µÞ7Á&Õ"<§\x0015\x001båi©Rà.j'Ôöä/ÿ;{1¾8ÇÑ5\x0005ç¦\x000eqÛ\x001fQUäqvvs÷ñm.¹}XîýåC 	J\x0002ò\x000eç¹j·v¿¼~õ,\x0017Ä¾·TêÈíz:©ª¦~_ÀXHï\x0008Ø;âãBù$}?\x0018±­"¶\x0011c1àfî\x0012-8ue>Ô\x0006¹Áx}\x0015¯\x001f\x0017\x0017\x001cPÏa(óê¬+¯k·ïWÖYx0\x000fÃÿáÀµ,\x000e,÷\x0002YÅ9}Ü´3\x0016ä\x001a\x0013ËÁ\l­¥&+¥q¾Y6RÀ÷£}k`»ïö¯û@Þî/¾6;êr}	½µ\x001d¡4¹c\x000c5ïa\x0013Æ3MÓ­.Ï/0ÏÐZØá·³ú¾6©3D^H%£\x000cÈsb3mA>9Íî\x0018ÅvüG\x0008»5ócþøv½/DU\x0007kÔKÿBp¥ÞÐ>	Kr#ùüòÙyk(m;ê#Ý\x001aúÑ	¡pTkæg1\x0015ÊØ\x0019c\x0006÷t\x0006hª\x0000MÊqW\n\x0011¥m¥©S¶3BWEè\x0006\r,\x0008`à»2h­áÎ*á>\x0008C\x0015aèÐ\x000b?y¥¹ò±2%Ìl/Èì°\x0005\x0011v{*D\x0007©8ÓpwÂqÔ¹ì­37NÕè°öPdïðQ\x0016ÄEÁ\x0003\x0011N\x0010Ê¦¡\x000bû ¾\x0015j«zX¨T=Äg/V7³çwW«õ[Æ\x0019z\6}&dÖßÎÝ±Ûý\x00078Q\x001c\x0010Ì¿¾|±8oo«\x0015±=&¬	ïeªfÊv§aic½àÚ¸³C¢£±­UÄö\x0018®N®PÌ[«ód
Gq\x0004§Ø÷U»§ÕuA(¶{ãDîã¡\x0007ÜvYÃ[»í\x0011¤Ýo]l4MIóf®g÷Ã\x0015­x\x0015\x0002íl±F±Ï\x001eí®q¹¹ÝNy»fXlj\x0007a6ìuj\x0011øQ\x0019Í,\x001bÌÆ?\x0000³«bv\x0007`æ\x0019JJëR?h¸,3nïáîØû½wîÙcF»èåÇÕò\x00111­¾¬Õ\x0007Þ÷²yXÂ"µÑy¥\x001b\x000e[TyÈ¯Ó`|dAom^êF	º\x001fæ¯\x0016óK\x0004u¶øçùüM#¢÷\x001f¯®Ö\x000fIÐÃ}àÿÿtw»\x001dß^=Þ?×~sÄÀ3x^óëu#<M\x000ci\x0004ÃBåyÿÎa!ÁSÁg\x001e%|?½>]ÌO_\^¼\x0001Çýä$Égð¶æÇçXÿõé6ÞW­m)®f?®ÖW×«f
KkRÇ\x0005n}¥¢{g]¤T·\x0001\x001f¥zÕ\x001a \x001f\x0017ç/\x0017ç4*ý$H,¬únóï0{2ÿ¼ºåæ\x001a@v»¼Ù\x000bQ{JiMt9êåÔÔm¦Ìupþãâ»l\x0000ßéü¤\x000bPS\x0003j\x0006\x0002u&µD\x0003PMÙ#\x0000êh¼öÖ\x001dÓÕpº8áÎ\x001f!­ÆØMæJ%È×Ñ X\x000fG\x001ajHÃ0¤Z¤\x0000bBÓÆCFJ{\x0012Á9Ë
V\x0000u¢
\x0014þi\x0018P\x0019s\x000bêp$u\x0006ªÉj×¦Ç\x001c´öÜÀ×¤ÁSt¤ÂçÍËÔä5òÔÈ/ßÕØÔ
dS\x00123?|¥ç\x0006IljivÃ!H}íáû\x000f_ûÆ\x001d"à\x0011üò5û½ÚÐÁþHÝÏWâÝûr¬õÕ­îÑÐ[Ý\/1¾\x0011\x0008Cxëëå»\­þqº||\x0016M\x0003Tð¿Aab3¥Ö\x0011óñIZ¹#\x0004\x0010\x000bEOêüxþü\x001f/\x0016ÿ8_>O¤k­v\x000b´ü\x0016'Çó¸G\x001d:-í9\x000cznLEèà&åþY,ýÌ.\x0013@W|Ê£B§Ý,A÷.I\®U.(\x0003è62tÃvÊ¨ÐikæAÐ±Ã\x001b#&\x0008Ý#â(_\P\x0013 §EF!×2½JDî\x0002óU\x000f=\x0008;\x0001ô¼wò@è6\x0016èVà
¢\x0004Ýe»\x0011O}
äàú\x0007FdBû°cF\x001e
#7l[
,ß c\x0001?ZIÐUN	âJñ¼^\x0017¡)\x001e)è°x8t\x0002ì\x0008\x001d\x000b\x0014AÏ¥\x0000\x0000]«8>tÞ¨| Ç l\x000cåØ\x0005qL°Ì1:NÀìh8Êµi@mÊïT\x001dYÂn\x0014³\x000cMº\x0019\x0019;H\y°:¥\x0015Ò	;µ${\x001eb\x000fØm\x001cM²/¬ÄÓà\x0017sd-ÝC\x0012g7Ëë´)©\x000b	*¦R\x0003 \x0001Î\x001c=í,á\x0003±\x000eú×\x001dHÈA³ùqÓ\x000e¥*	¶J=d\x0019d¡ÛÑ4Ý¤¤À½íÂýýHðU\x0012üßP%!ü-IU\x0012âß\x0004)ª$l«oð³ûã­Y¯ª~\x0015JÐõÝ\x001f)SlL\x0006\x001b\x0000ìuöóÀc2\x000fWÅ¹,oq"\x000fÜRÂÓÂòù?1A$ãùë2Ãu\x0010¼Öô«àm¦_\x0015\x0004y-_\x0017\x0004oRýëA¬ýòÓûUÆäxî÷Ë·ëÕûÇF0Fj¯Ó@3\x00005\x0017)«¨3À(mª`8ûýüÙùâåe7Pmöß\x0010¨­\x0005ªß\x0006(bäo\x000b\x00141ö·\x0005|æo\x000b\x0014¹Ãß\x0000¨Gq\x0013í\x001f»D\x0002üËÕC\x0013$e\x0006¸þZ\x001bð»CvÇ>f\x000b9:G:$0èç'¦üX
Ð8øú¶DÁ×\x0007´%\x0006¾> -\x0011ðõ\x0001m=ÿ¯\x000fhëé}@[Ý¯\x000f¢Vß\x000c \x0012úÊ¾Üüñá>TDõóõê\x000bxD·\x0016¤Çý6"YÚb4&\x0007°\x000f%ïr!T<?_ü\x0013üÓfeQAeó×Dñ_àñ_·ËZÒl5;¿N³<w~?Dk±:©n­p\x001d\x0012\x0019qðá¬º¥3UnXÌÎ\x0006xÖ?ÏnÝWú<;tåç}XýêîvY+¯ë÷×8¢¡\x0001\x001bàò+ç©*£òêT\x0005ÿ£<^cëE¾¿¼<î\x0004gËVù*p~»òr}]gÍ³ÇÕ»\x000f*âåÂ¨ë¯\x0013.G¼=¬ÜÍÙåâù\x000f]>_Xóë|¾°æ×ù<G\x0019þÊÏ§µ[nçË¸»}X®ïã\x000c8\x001b7­\x00087jÉZ
xß¨Óv';¾>}3?¿hq.* ¶ßÇ×\x0003uugÍ/ÕÀåìbù>\x0005\x0012wC185$}sÎTÒçZha3\x0014AUb\x0019É|v1Ù\x0012\x001d¬|\x000eå¯ýþçûOË?~¯Ór÷øözµn\x0010­\x0016©´\x00075mOÌj´t$±¼Ï3T\x000b×Ï\x0017ç`cø
0¬ºúø\x0018ë§q~wÕ|\x0019>¤b1 ­Èu¶JëÇÞ*©M\x000c5\x0008ç¯_,\x0014ßÔ>\èoÿ0Ø12æ\x000fãm>¬øAÀíùa{>\x001c²Õ>³©ò­Ötèæìôø0IÈ=\x001fÆ¬y:\x001dª*Ø*¢XåÞ®\x001eß%÷tßwHÝï¤sÜ\x0015\x0008Î)oTÏºï\x0015\x001bºï¤]nÉÅ\x000f\x000bÊµ+m\x0002\x0005277öø.yû¾\x0003`ç\x000bÂ\x001fD1G\_Î"§r/½îHæç¬ÌI\x0019 7æ\x001c7|ØnI¶ý\x001f&çqßH@ÓA;Ü\x0008>ìré\x0011|X	ÓïÃÅIÜÇ[Ú¤M
ø±\x0010ó
8jò
áËÂõ|L¥Ü \x0003sùÌ\Øâÿ¹DìÉ\¥V`ßµK£o\x0012É>\x0017¿(Ìi8þrßw­²ärX|¾ìÍ\x0011É\x000f-éÃ¸½ç+d\x0007Éë \x000c}ØÉ¼\x001c\x001a\x0019o\x0019\x0007õü2¼@ÙAvÐLÝ6øe`r~Ê*·§ÁiqD/\x0003[ÈNÂKÁæ¤ÖyÐ\x0005ò'\x0006ÖtþËwï?ï²dO®o¯W_Öwÿn6\x0010ÆÓF«\x0011K(8<1_¹²vð¥åàøôxñÏó×ÿ³\x001dÐ\x0015Û\x0001$¸\x000cYf@âö+÷áÙ
HwÁÑd<pV94¥¤ «:ÒÆÞx¶âÑ].\x000ckÆé|ä\x001c§\x0006	¹FÔ|_@[ñè.ÊU\x0000È:Îx\x001ci$x
ê\x00008[Ñè.pL\x001e¯
¯JhZ\x0001
xáóñn\x001bÔ\x0015ÐV4º\x0013 ª©\x0003@à¢e\x0005fÐ '@±fÿö\x0005´\x0015î\x0002\x0008Ç@Ò\x0001©<­\x0012ðÄÍ\x0001C8z+\x0018Ý\x0001Ã¯\x000eHæ½\x0018ðWM|@î\x0000~\x0012îÈ\x000bÅ^\x0013Há<ñZ\x0019kÈÒØ\x0003®¬Ø\x001f}ÎH{öe@\x0004\x0013eàÅ\x0013%UÜ\x0015!ï
>\\x00145Å)\x0001Ë\x0005ñ¯ÈïJ°vEÄ\x0006K/Aä4Ùkà\x000c8\x0019ÛKzhèi\x001e->ºÃ§\x001e9Öð«e@¶¿n½w÷þæ¦\x001e²|v÷¸~ßì\x0006c@91³Ávâ|,Z»Üï °C¨V\x00143{öúòüeû§K¸rÏ§5'áM4!ÂÆU¥éÓð7ú~º*÷}Ú¥©7øéH]\x001eøi2k¤r±ïKrßyÇ4M\x0000\x0003øyùfú²Ï\x000cáÓ¡÷¹\x0000jï\x00156\x0010æ/ëÜá7]¢÷M\x0002Þÿiíkµ°üé<¯\x0013³\x0016ª7Õ¤j÷~\x001a+=²ý\x0001ª]\x0007\x001dÉ\x0019\x0017¸j«ï§I©îý´¤\x0006.ø4Î±Êþ?\x001djÆO§OþÜûi`­©h&\x0013Õ4L	ebßO\x0017M¹ÿÛ¢.VÊ27;hþ¶èýmÖ{¿m"ùÆ\x0016\x0007eÕ\x000cÆö8Þ|ßo³öÛ÷m\x00178êcp¸ÌÑ\x0017pMèe\x000bS\x000b7uú6ë¹½ß\x0006­ó_V\x000bÁ¢Tþ\x0017Fl%?:|\x0015Z')]D£Òd¦täÂ\x0011ÂJmû~ó½ßÆ¡Êê`sw4|ZQX\x0000\x000e¼?§±w¾÷ÄÁ¯\x0011ùÄÁÈ½0pâ\x001c-¡i¦Eo<]d\x0003Ïtt1oo{C	\x000cECïû|'ìÿ6ÎnÈBMZàòüi§ùq£"ë÷i\x0005BEu\x0012,Bï\x0006[\x0014y*6»·\x0016ÁH»ê$XÒ¸Ä$Êc	3jYÈVºïãRÕÍLÊ£iÒ·å%f\x0002q¶7Ù ST';É[\í\x001cN_\x00147tnß~/yû»­\x001a¦ê8Á¤á\x0014;ÈðÒlî×Ù\x0000õ-ì.ôùüä\x0015Î8iò¤"²\x001dÇÙ½é&Qi5F¾üîpÅ Ýåvò¤\x0016r\x000f\x0014ctFN1©9Í\x0015Q&ì®ê\x0000äI
ä\x001e  ó­ÊH¼Ç\x0016»,þs¼\x0000³Ô./¦\x0013'Õ{ ,´T'\x0006F}pÌ¬|*Þ\x000f¾'uû8%Ák¬\x0005\x001dEö\x0017hHbÚÝÎf'(O*\x001e÷@\x0001\x001bÌe³\x0004çèIº åiC°¡<©uÜ\x0003\x0005¬à,É\x000c\x000e7ðl\x0019:â\x0015Úø=\x0004É"Ç=B%ø< \x0000ÈÀÉ\x001b°Õ<\x001d»âÈ] ì(oÜ\x0005\x0000X:<6:a\x0011/¶½
Á²\x001dKÚÅF{$²°õåô/Hí\x000c×v²\x001dDÚ\x0007¥L3Àc\x0011%¿¦+Ç²+RÛå-x½¤ò/Á/(Fòjy&°µU\x0018é áBT´zs6DáXe~J±îA¿_¤k[µFÛT\x0015ú\x0006\x0000é* ý
\x00002U@æ\x001b\x0000d«ì7\x0000ÈU\x0001¹¯\x0005Èü|­ÿõájá\x001cO÷½X­×©>MÓ\x001c'óÝÅÏËÛ?ÿ3¯Þj\x001dh	¢¼´-º¨q6\x000f\x0014F\x000få»ü8Ç!¾<Ö÷bq~ÞX VC¬>L3T\x001eãp#BB¤Rpô\x0000DÙÚêÈ¥QÒ(È¼&\x001a\x0011aº(!2æ0@ÙæêwD)Ð\x000f¬Û\x0000Bû/\x001fQj\x0004>\x0000Q¶wú\x001dQí\x0002"\x0013²¼#DÒ¨\x0001ÄÕÛ_õ[D\x0019T­+ë<Oînß/1Öß\x0002Ë\x00060~òAI\x001d©l#Ö)ÀÒ\x0006Yµ	ø¿>}9Çÿ~h\x0012éG?l\x0018NµF¨lE\x0010\x0007"\x00106\x0016:\x001eM%?_ÞØ\x0004ô\x0000¹\x000e"\x001aç#lyÿÃ\x0010l¿­nÍò=ÂsSÕs;[ß}¼¾ù\x00037aÓ	Ä)\x001a¸\x0014L·4ü'â~\x001f°	«ãî;=;ýêøä¦ÙÀ5l\x001e£aÞöÆ¦,I
áu ~ó\x0007c2csz÷¹íÇööËÍ:ÏÜôððÿX}LÛlgçw÷\x000f«¶ûtê¦ÀhÇ«MÏÓX¯éÌ|Î\x0014\ÏX¼Jûkgç¯/Þ4UV@Ibx®\x0017*¬\x000bð\x0019\x0014[R8\x0003\x001dk2\x0013¨\x001cZ:\x0000T@\x000eÃ\x001f}@aJQÃ:\x000eÄ&Ö\x00178xï@TxT¡çQ)>¼\x0004@ÍQÉ@Y,xH?zXê=ìúG\x001dCÌ¦\x0003N v\x0007r\x0018+J?úò\x0011\x0013ª
\x0017U|Tà!\x001aB¥Ä¡¨,¢²ýP\x0019IH°\x0017S\x0005É¨Ãa ÐûM?ú[KQ
8*©rM>\x001e$Vw8;ð0T\x0001Qõå*Ã\x0004x.W![ùÈ\x0017h\x000f{\x000e#ÀéG¯\x000b4¹\x0006\x000e.0Ãå\x001bô$Ù]^s\x0008*<+Õó¬ÒÜ\x0017:+CÅÊi>+} ³kä+Ý¯Ëãù\x0000\x0015ÐTÞ\x0000¨¢á³2r;\x0006gÒ¾7\x0018ÛE\x000eÖnPÅÃd¨C\x00137ýè
wyGBeÈÒÂ&\x0011¾ÁC ÃÑéG\x000fT`%°½\x00104m*\x0001\x0011\x0015#¿Á\b9\x0018\x0014øZòÏî°\x000c$K²\x0018Í;}À
SÄ¨Ot\x001e\x0000\x000b7`|ö
ÒIåH,òÈ\x0016)ÀÒ\x0004+X7ßuî;óÄ­Ç±Q'Ëë\x0015®Jûñzu\x0003¢Z.\x0013\x0017dßL¦ué9b	N'M¬³ØfÉÂÉüøÍ\x0002¥ýx¼8Æ1R\x001dæôÎP¤4§\x0011z}¸Î&º\x001dNäP Õ¸D !÷c5't"RIGjsÅïHH«ñÞHCÈÅä-DlEJH¥±TÊ\x0011Ï´\x001aÈø¶Ï´\x001aàø\x0006.ãõÜnýGÞZp?{µüwâ7At6¤&7ÇX\x000ebÄÁSÄ*ÆºDªì-¸½ÿO\x000cæïª¶}-ðÑ\x0011\x0014]0¸¥$ÛÖKÑ\x0019Õ\x0007£C¿/ýèN»\d"°±\x001c\x0008\x000bÎ½"t6\x000e\x0005·¾º\x0012¿,·Åäãìû»ÇõìÏÿ=;[^ß¶AóX± é(%é?\x001b1®Õ(ñ4îw9ûþõåùl>;\x001fvV\x00117ý YGÐÜ\x0006\x001aYíÔØy ²\x0010î,5Ù"²\x0010C\x001eé\x000eÈL¤x²\x0011ñ©\x0004ì\x0006íã¿¾(mÐ2'ýªïô\x0002`=üãÕõ»\x000f«ÖPÌE\x0005Âjà6G6\¨¸Í°û-\\x0000°7³WÇ`L4MS\x0000Ãæßo?j\x001c×¥q\x0018CúQy
q½¾k{\x000c8Ô9÷Í
-­A¿,\x0005\x001eÈàR^¦Ç\x0000\x0000ÏÁ¼iöðÞ­äcÕ¸áÙ\x001b\x0008-·
çK¢àVÁ\x0014Ìy\x000b.UûXO\x0012ð¢ìò\x000e¸ÈBè\x000b+|ÆåÙ\x0016´!z
Íc\x0011ÛÁÀHÍö\x0002ùÜÔÒÀâQ¹\x0011y6ãu;\x0008\x0017)Õ~¸T<¢{D§#d\©*<¿Îzdk\x0010®\¨Ð\x0013Qyx2\x0002s¹r;ÀÀ¼:\x0014\x0018
ôD-û$j,\x0002Í	\x0016µyãÏaÈ¨r 'ó+ËR\x0005¦8sÒâz^â1ãÃÁÀ¨LµçÈ1%8²ÆG:²¢d8ù¹´'0¯ÉÑ\x0006µ©(¬\x0004F{T¬6\x000fg2ô´{³?\x001a¶©Ç\x0012)7ÞEèR^Øäbªq!hOdRSEG`2¥]ô\x0019?Xòs©fO`¸þ¬3£s-zÄ\x0006C\x0002fâ¡Lf0ä~ôCfà2]æ2\x0003N ËÂßªH\x000fSCe¬Ã²õô£\x001f2
FÎâ_ã¾Ê\x0004\x000cwdû\x0002ô¹=\x0010YÄCúÑ\x000fr>·¿\x000b
\x00179\x000e¡i\x000cü'hN\x001cú\x0000BË'ÿìÍ+àþ\x00132~´£7 ­s\x0007
¥\x00136=\x0000\x0002ÇM:ÏJÃ7Ô\x0006[3\x000efÁ¨ú.ÿì\x0007
\x001evù]wdó±TÝ±É\x0003ß²¸!-ÿìÍF´1\x001c+q\x001aEv4Q\x001cø\x0012\x0014\x000e«ø.ÿìMb\x001a&cS¹Ñ\x0005cHÌn&¸\x0003E®²>ïnAçJu¼Ó§ `,&JÆ¦\x000f}¦©F$ÿì:\x0001±X±Ï«O>S\x0001ü³'67ò\x00116æ·´¿°\x001dè§(\x001b\x0013¶8\x0000Kí\x0010vYÃ\x0018ÉòÆ©C¯Ô¥§à\x0006<\x0005,,OT:ìmÎÐR_Ê³A»»ºûü3\x0018ÞX­#ë5;çË¸rö
þ¹=Ães->oïó>å
Ì2D¼*è©·~>Ûi_À?w\x0000ho`Ô\x0000¹\x00056\x0001tTÅ c\x0008ð©ºé6\x0010K\x0007è\x001c çº:\x001c7sK?R×PÆ'Çr$ÿì
/8å§UÃóõ¬%±Å}Ã\x0000¦ò©ü³?@j{ÀÞ,Z7\x000c\x0000ábóó\x0000ßkø	~ø\x0014>}NTÞaÜy+°ûüîãCk¢Å¥Â·YäI\x000eQJßP\x000c[)^¿zÓò|\x001fE¼ý&gZà;[UcÏëõõÿ¹^Í\x0016÷ï\x001e×m\x0005Ý<9zd\x00140 Ìµ¯Áqa§Çý0»äËóùù9Î\x0008-._6
¬ât©\x0008b(Î`rÐÒàÌ³\x001evÁ+)Gl\x0018å@VÐì,aÒT*nÆcÆ}ÇÁ^\x001db`\x0006­ç´\x0011a\x001aéb\x001cç8Au¦ü¶3Ãb827Za=m:Ð "k\x0018ìÇ\x001e\x0007©Å\x000cIþ9\x000ci,î\x001bzK¹¸0H­Ø³4
.RW¤*Ï¿bÇVÈôc#³ë¼Ö©¹$\x0013Ûôs´@[>Jc¹ðCaIëni4½<o^ÝTEõ|éG/dØ¤rEG6¿,{"*æí\x0007\x0000i>`þÙ\x000b\x0019x¸¤\x00005æ\x0010³s	"å\x000e¼ÂtDgh\x0012mËü³\x001f4\x0015IõÁ_\x0011\x0014ü1k4(Ôë>hòËÚ=V»xi\x0005óÙÝí}J^ÿßÿø_?¬ÖË½é\x0012a(]Â\x001d\x00036\x0004ª\x0001Ñ:wí\x0017x´ùìõéEJ]Ï~X7.0¬aÌÍ!\x0018=n¡%\x0015 )\x0014ª8¹)êM
Ã!æ¼Î c±ä\x0012kÙ\x001d»;»3\x001ccNÂ\x000eÁ\x0008v`	Â\x0007Iùk'çÔX¬GûcÌi¨AW­"§0pØ£±õ)É\x0015åÇÁSR0eÃ¼è9ûSÒR~$975ì½#Ðý\x0010)£ç¹å\x0006Ï(\x00109K5\x0008#¼\±§q\x0012²§\\x0015¶p~#\x0003¦¶\x000cz12µ¸äÌÜ0¥àJJ!#\x001c9y5\x0008$x/ò1\x0001Gxå|å*\x0006=àá4Ö èº§	òª·2 ÃARJk\x0010H§Jö\x0014ì.AÊâ\x0013lÙ1rrk\x0010F°À(_\x00131$»é¤\x0011|Ùy¨Â\x0008 )Ñ5\x0004$®~ ]\x0008Bg\x0003²$ÈÇyØX7¤½\x0019pï\x0004riag\x0011é\x0014Ø°\x00041êÎ\x00113\x0012C_
Ø:^v\x0014y,\x001ecéw5Q£¯Ñ¦UÃ^\x0017æ%äÌÅóp\>æ\x000f\x0007¹~÷¨luëËÙÍòÝÑÍ¯÷¸ÏØk©\x001dVåUÝµþÜz\x000bóÙÉüy.ÈÍ[<¼
¨lÔ~c ²ø-züðeýV ÷u\x0014ùgñ^.¯onZÛ&M\x0001¹ä¬K·3Dí\x0003\x0015*¿U¡^§óã¦É\x0002lWP¸\x000b°\x0010s¢F®ÐÞK¢¼ò»]á}¸>½}÷á\x0016o\x0011ÃèµPúÅ\x0012\x0010¼¿mÅ\x00052\x0017ÚHã<e2
\x00063s(S©ÝÌ9üæåiÛ=x¡ÃF\Æ~\x0014hßßÝ¾»Y¶rSÙÂ\x00100öþÓª p°Ù	íû×§ÏOæmLÆÈ\x0012qéG/dÒreÂðoNÆ)\x001c:ÉäÃ^`~õöÿÚnÓx=_¾½{h
\x0001½Ûï°öú2,ùÂïjâ¿=?{Ý´_¯¥Vaü±ÔJ¿\x0006\x0007ñ´ºrGoÖËÏ«õ=ÿ?[>~ÜÛD#©Â	.\x0005]Xê\x001aL}Þ
<¿àÂÿgóËWÍ\x001cTAo­?:Ñí'3zwãÌPp9pÒ\x001b£mC¢7Tã\x0006¢«\x0007|=º=\x0014\æ±Þà°òà`}Àý1¦ôÇè1ÐåXIot6Py Ü«à¾}0·KëV½ºa(º\x001c%\x0019r±Ûµl\x001e¢.k\x0008b\x0018~³ïWÖ_ª£­¹!\x000f\x0004È?ÿÏÃjù8»\x0002g±lKI:\x001f\x001c\x0017°Ã?\x0010ó9¸\x000fÍ®ÜÙM\x000c\x0002åùÅ\x001ctÀ\x000c~v\x0019p\x0010L/B Ü¤\x0011QS©\x0008n#'Àn¾0ÝýÕµIÊ\x0013{Ä\x0014õFg«õMëD\x0010\x001b»cvI%È?AÉSMÝ³ð¿¨\x000fx©v\x0002<[´L\x0004¿þ
ì\x0003Ø\x00026v§\x001fµÌ.{X/o¯Ú½Q\x0017È\x0002MÎv\x0007®¾âÚ\x0007o;\x0000 ðæéf\x0007e1ÀÑ¥\x001f\x00030b\x0017c\x000c¿wÊ±	"¼ßm\x001bõÆ\x0018\x0011c\x001c1°V\x0006«k=a¤z*\x0005ÿòC \x001a{õ+z/\x0016ÝÅô²{³óë÷Ë¶N\x0019£û©mLEÃr ^wíÝ{¼\x001f¿7·Èl ¡sP­Üë\x0000É
\x0003ª?\x0005\x000b'ÂcàDxÐ»\x0012ÌÝ1!£¥\x001f=0)K©\x001e£+IoÅÇ\x0014wÖ­öBðG?H¦Ci[Fz)Ín§P»B;cr¸(ýèÉÉdðG4BK)äv0täñù¥\x001f=\x0018Ü)*6\x0016nÎdf¢N]\x0004\x000e9¤_>¾W×¿=
­<Î^¢0½Án×ÇÖ\x0016µè\x000c¦r\x000f±*¶o \x001d*­05\x001dJaËÙK\x0006³7ØézÙ	a-ÎÒ\x000b¡§5X":rqÏjAXO¦\x000fGMà!\x0008õ\x0011ÙÀAÓP\x0013Ãr\x0002ðY5\x000e¾ZP¨\x000f>OË\x000b\x0010 +'\x0018©\x0006\x0005\x0010î\x000c
\x0000
á!\x0007¨Ðþå\x0013Ü\x0018¾\x001cáH\x0008sé#tTÝ\x0008®¢\x0019¬[eRtÉÙ\\x001fr²8±Áä x¢¡Óã ÌCÝ²à3´¸D$#ÏÐÉq\x0010æ¼ë\x0010â<í`èøX\x001e²£àãÆÃ\x0000\x001a]<Ú° 4ã ¤´ð\x0000àÕrÍ~°Üó\x001c=#\x0014~\x001c.ä&Æ!\x0008yâ' ô%dáËÔ\x000c\x0011GH\x001b?@´åÞ\x0006´+òÐ\x0003¶s\x000c¨h\x0008\x0005@\x001b¢¢\x001eGdó"!\x0010Å\x0011Û
4H\x001f<|éº ¼¿ùüÛÕêéXWw·×þW«y
À,Ïõy\x0003\x0003Ø§¶LÁ5õiU4cäÕëËÓãæ J\x0005Pm¨L'@´ÑXÔÁ,\x001bÌÚ=
Ëö\x0001T\x0019îÐ\x0011#Àè\x0018KÕ¬ãbÀ`ëw×
PøýTÛR\x000b=ÿ|ýþ¶}l*\x000eÔ£Á0¸è´\x0017N»¢APÚî\x001eæ0ÿñøåiK¤ ÚéË°y\x000cRòàXO\x0017y@Ü/ÚëËçå/\x0006qaûíwéÇf`êêþ~yÓ>6Ø\x0019K3Ù\x0014î¸ÉLå¹a\iÑ\x0010´9[\\ÌOZêñ\x000b0\x001cóñ]úÑ\x000färNR\x000exa$Uç\x001aÑ0@§;2*$ýè\x000c$\x0000'Ø\x001cî!"_Úra³\x0016»Yl/°_\x001f\x001eX$ÊÒÏj	ìÿXÞß·AÃI&ÙvSX;ç\x0013áò\x0000
\x001diç\x001a«sÿÇüâ¢EJ¼ÿüyyUña7ÃÙ¾_~^®ÿüÏ«ö´·ÍÀÕW¢H
ë¨x!ø°3¸º}?ÿq~¾xÑìw\x0019®þÐi\x0002LHïÊ.Ó\x001eÊ¶ÊHf¥\x0012e0P<i\x0016Ü×Ý¯òt~ù?\x001b\x0011½\x0005ÉC'ñ\x000c{oñÌúTÏ\x0007ZjÕóqì3E{A`ÔÈÆ¢ùmPª
J}# L\x0015ù ôÏ·\x000fË÷«­Á_3
Ó?'¸ÄaG\x0018ÀOÿ»»ÇåûÕý?Á¿fõyy°Ä´\x0001aU
°\x001czË Ôp\x001b1GÎKbâõåÉüåââ\x001fÏ^.~ÔâöÏáQÎ¦\x001fÕ nítê\x0003\x0015Ù</3\x001egf§â\x000fï°\x0012?C
6¦\x0004ukÕRO¨\x0012Ç\x001c'¨Rå"LïReUª\x000e?Uùp÷þ×]\x000cð|ùñÓûõõ}\x0007¤¸W\x0002wµábË\x0002Ò¡F`Ë´kÇ9`ØôùüÕÙËóã&}Q\x0003úd¥W\x001f *¯'Â)\x00156ïC y\x001f-\x0000µû´\x000fÐ'\x000b¿z\x0000Uþ(ãÄÞÚ\x0014\x0003\x0005÷\x001a\x0007Kd:\x0007ÈÆÁùd\x001fX\x001f\x000e'ê% ì\x0017"PÉ7¯Ó²õ>Ù\x0016Ö\x0003¨ fÛTG«\x0001¨ËëºàâÍ8¬\x0012ëSó°
Ä©C2qÉ¡êç·\x0000\x000b\x0013þÇ@\x0006 õð¢°9Ó\x0013\x0003òô»2j^ç´õ>þ~s{¿K>­Ö\x0000â\x0018y\x0001\x0003H²l
ÖØü°Ko\x000fÂ³ÅyóaV\x0000n=÷î\x0000c6±cÄª´.\x001a\x0000ZÅ<ædö°f+ÀÕ§Çø»Ü­âï±þ/{\x0000{µö2·8Â)iÒ\x0003\x0002? ¯æt¨ä>mt%Í^A
ì\x0013%ß\x000blªgà9\x0005:P«dÞw'î÷ªø>H·î½'RíøXp|¬2äÝºx¬q¯ï\x0003öAÒ\x0007¬ÂÈ\x0007,¸¬Âd°:/!\x0006°!\x0019\x000bì¼ï	VÅ<<\x0003ÁÚìTc
]J\x0002+0\x000fÂúáßWWìz\óúöº\x0013R\x0019%ó	û\x0018r^\x001fË~\x001d1¬\x0011rÏÓ\x0002Ç§ÇÝn=¬\x001e@\x0015NÔ  8äË'åäM$\x0003{di\x000f O¶,öB
ÒJçg\x0001ÍÌ©\x001e+í\x0008©v"5ÿø¹Zäy²½Z^-\x001fo®W]øÓ9k_"H\x0001ÚÈä­\x0013,Pe£bÏ^Í_Ì/O\x001a\x0003úç_\x001e®VþÃn»þm\x001eIÜA4©\%\x0016Å\x001dD\x0013yuÎï75Ï'®a|bÒwÅh¥ÏÃ{Àüð1/4ðÖ(âHç¥Ýótº|b&w>HÜ¦óA{m:PHy½³ÃÖÊÃNò³X}~»sõ26/×W«<c¼$ÊH=ÈòÜ±\x0001H,àáÆÅ>%?½¿X4\x001b¯ÁÝÖò=áZ§\x001a`WIÀÍ	.-\x0010Ë×ûäQO¸Ûª¾'\Üýc\x000f¨Ò`Dpí} ØfaÒ\x000fî¶²ï{º´°'M\x0007É\x0011Vd\x0006+ÅÈ§»­îûÁ
Þä~¬oµ¹\x0013\x001dN\x0017·
%¸Ê\x00197*Ü-/¯ïéâÚ,\x00140f¦wq­w+ü¸»µSº/ÚXÜç\x0000n©"\x0013%h\x0012\x000c"¨}_\x0007¸¿¯\x001f¿mc?.¿Üß_¯ÖðJaI/xxly wyú\x0012*WáöË±\x001fçÿ¼¸Àèi\x0017¼O%C\x001f¼"Ú´O)\x0019\x0003Êç\x0001yÞâ$
6\x0006Ä>7 \x000b`á~»þ÷û\x0003~¾^Ý?¬ºY/
KgL~mQÐ$y\x000cJr\x0005rÍË\x001eÀÏÏ\x0017\x0017o\x0016mvL\x0005ðÓ\x0013î\x0007\x0018DXZ6
',uÎJú`TÞ\x0007AlµÿÁm\x0000ïVèOÿ¾ý×»§½Y¯în\x001fW)kº? \x0002:M¤p\x0000\x0008"Ç'\x0015Ó°èx·¥@mI¯^¾¿hL¡ê?JùÁ]íbW«?Vieð^ø¢T\x001ep£¨:\x000eKòu¶\x000c-æ\x001eiðjñÓ"m\x001bî\x0000tËFè\x00034(ûmpÌ¯!\x0005wdË\x000bÄA\x001c\x0011èºíu¢:	Õt¢\x0001\x0013ùD5¹Ö+»Gyí\x0005Í\x0018T]þEI\Þ¤Á«Ï|,\x001cíB\x001a\x000cwgæ1ç \x000cJÖÇ4þWáiVåâäÇ\x0016/« VUÔj8j,¿6Ù\x0008?W\x0002ÁôÄ°îjDØº
[\x001fpØNåYmi³\x0012J^6\x0017l£3\x000c¶©Â6\x0007À\x000e´Þ\x0006O[¢}`k_N;	ÛVaÛ\x0003`\x001bÍæF+81In´H-ÜîØÑ0Ô®Ú\x001dÂ#&U}ãYûÂ"
`+Ìn\x001bb\x0018êPE\x001d\x000e9kg\x0003c5¡$Ó\x0012ÎÚ*æl·Û+\x001a\x0004Ñô\x0013\x0007àÖ.vAÜ1w¾x\x001cÎE¬mÕrDÖÄ<@þ¡¨VÄÚyòqMñf@\x001dwÛmÃ`×ä<Dü¥òO×[\x001frÜÒ\x0014u\x0013h³\x0005\x001c·ñÌÝºÁ\x0002\x0019¨%SB¯¦)ñ\x0017Ã¥ÆY\x0016)4\x0007
N\x001d­P\x0016)=tüNy#\x0005·¡» ktªI\x001aZÛ\x001f1\x001a_zÈÂÀ\x001fìõ¯ÿþ÷Vü\x0017
ý÷·eBÊë_~¹~\x0007>`\x0017\x0007Å:Ç`\x001b1sz0PÉeu±ÑVg»ÿå)MOyýý÷ÇÏÁ\x000fld?~_½»ýý¹\x0018bN?No×w]ÎÕªëÈ¢ eRwÇñ¡¤etØ;?;Ý\x0008ÌdóÁÖ\x0011­f¯®ÚGTMm!ÏIôÑR\x0017Ü~Ýà.f¯æ\x0017ß½[^-ï\x001fÀOç?\x0010¦Gmå¿~¯\ð÷«õÇtµÏVëÛåÕ.·ªÅ5SÉ6õ8î=ºHÄ÷óWé>-ÎOç/þIL~\x0012@kÅûØÚ}¹üc	H:¥KV\ÀËÕe\x0005Mõ&Àû2P,{9ÿi~zZÞK\x0003Ôí°YO¨Vû¼þ\x0016ëy}\x001eæ\x0008Ï\x0004w$¨Þï«5Ú\x0003õwþØ:¹Á\x0004Ï\x001f¿?v\x000b8ÈÀ\x0016\x000b³£\x0011qî«áI.ÿßËE;Ì§Aô>0EÀ9\x0014éê?\x0014æÈ^Ø[\x0012Õ
\x0013_tÝëÄ1p²Ò¨úüÃòã§ÜCÑå±ÃÓ9Ê×o@Â\j2¤ù=©@di`}þÃüÕYn©hÖ§ÒØ:j\aK¾òÙ\x001aþöõ§e§È)\x000e\x0017Í{@^â²\x001aÇ*Ø@È\x001ej¢³óãÓçÇgóiªªPÕ ¨ÖpLObG°¥è\x0013»Æ Ëm¬>Pu\x0015ª\x001e\x0004U\x0006ªDHP\x001dª\x000f¡@mv\x001aú@5U¨f\x0008TÎf¨¡Ê`%Cmqû@µU¨vÐ©b\x001b	ù\x00068\x0018@°mÔ8H]\x0015©\x001bv¨
9Á
¡Eöx¨\x0000d_¤¾Ô\x000f:S%Ø\x000e5Ò\x0008H\x0010lº\x0006ë¤/ÔP\x001a\x0006AÅ±0\x0019ªÒe«t%X#ô8¢*V¡ÆaïßæI8UªÞ¿a·Êfï»\x0007ÔM¸ )\x00001\x000c«d^5àDiU.r  ¶8Q}°ÖÕ@meYXa%w¤ÂcÇ	\x0008\x001bTsä«\x000fÖ¶Ô\x0015Æ]ÇíÅ\x001cÖl÷7TxõÅZÓ\x0001r\x0012À \x0017Y\x0001ØÃ%+\x0006¹Ù\x0012GÑW²¦\x0004ä - ="¨=¸1°¤\x001eçTkJ@\x000eÒ\x0002ZË#òûbÒ\x00079ÅaZ§GbÖ\x0016Ô\x0006! Ì\x0001(Êi+\x000c0n55 \x0007é\x00013Á4ù¬s»Q	>WÛPÐ\x0017kM\x000fÈA\x0000KR\x0005byW\x001cåq¦ÁÇêTÕÔ\x001a¤\x0006wl\x0008 \x000fk2·\x000càÜ®7£p«ª©\x00015H
¨\x0018òôR\x001c:§:à©rÐÒ\x00199´Rue\x0016PXé\x001f\x00166«ò©*V\x0002a\x001cóJÕ|\x00165ÄiQ¸|ÂfÿÊâìí|¬FrC§%<\x0007c­),5HaÉRêíqÏv såêTï­\x001dç\kj@
R\x0003\x0012|\x0015ÏÕÝ\x001arÝ\x0007Î
ø¦Ö¾Xk²U
­©0 Ê<ã\x0019 :[5r¬º&°ô %­àà¿\x0003¥2»z\OAÇÚP®Ø\x0017kM
èAR@JV\x0003\x000eÁ³\x001að5ÇeÅc@­½,=èe<¼4\x001fk Þ¾à¸!	°\x0013ºÐµ¥\x0007½,0ü«/Ë¸UyÚãì\x0003µö°ô \x0005ÊÕ«Ã0K~YÖs^\x0002\Âqøù!'t*æ\x0000þfêâ)§h\x0011\x0008~`QrèÕuäÚÝyµÂ\x0006Õ¼\x001a±\x0002'Öz\x001e±å\x001axe!O6@n0%ôÞÍ5ØWØ­+ü¢'¥\x0011Áß\x0003¦.8\x0003Ö¤q®XaÕ\x001fz0nû\x0013mUtiZð÷ð_4³\x0002CUU¨j\x0010TI\x001b¢W8I+;[ÖSÝ\x0007ÿ`wÝW_¨º
U\x000f;UÁíèXC@¹`\x001b\x0019i\x0008-51=*R3ìP
õÔa=5\x0007ÀiáÂ4ÙPL×\x0017ª­BµÃ \x0006n¸\x0000	Æ!w\x001b4).ÓÔ\x001aÒ\x0017ª«BuÃ z®¯W¸\JÎû\x0006ÓRÈÐ\x0003©¯"õÃ85²¯
¿áýsÊÅè0Îý*Ô0\x0008ª²T²%âÁ	6jÎ
Ø¶Ú§\x001eHc\x0015i\x001cvý¥nH¹@¦\x0000Ü¿áG¥\x001bÚÕzBuù?L\x0001¨RCM] \x0019kÉ¹a%ß\x0018XkRU\x000e\x0013«F\x001f\x0011THÕ¡ÊP½ïô¬Zuª¬	*9LRÁA\x0006J\x000eo¨èL±~¶¤\:é\x0012-«ªþ§¨ËwßÜ=\ßß¯>®n\x0014\x000b.\x0005\x000fîVÎ½¥\x0007FÉmÓÔ\x0004üúÍñÅÅâÕât«^`/|U¯\x000e¯hå\x0001Â·Tbè£aë Ø¦:ûÁðu\x0015¾>\x0014>íoÆÁ\x0006î(ÒáÓ(\x000b\x000f¡¡Th0zSEo\x000eCoÀ:wtø\x0013wXAÆ\x000bòÆo«ðí/=Õº(ó¨(ä\x001dA%È\x0018Þpø®
ß\x001dzú9MGJav§Ì>j¨ò\x0019ÞWÑû\x0003\x000f\x001fD9EÐqÒ ÍíçQ±T{\x0018õC\x0015~8ðð£à U4ünqZ3qN¥7\x001c|¬×Ôª\x0008\x000e´(#\x0005)*\x001f\x001a¼ÔÞð\x0014[½)ðúê>,Åº^wêPÓÊ\x0006î§±¸¢.1w\x000c\5\x0014n\x0016ça%Öñy[?\x001dC6UÈf8ä1ÌtÖÂäµò	2\x0007]tCÅÐ\x0010È®
Ù
C\x0018	rÚ¯!3àò÷\x001eß­â±g"\x0017mF\x0003=®Þ}¯®îº\x000cÓ\x0006³1!W\x0006Ã\x001fK±\x000b»^ûzòÏ.\x0017Ï/^¼n\x001e\x0004W@«*h5\x001c´UÉÞJ\x001dÃRpÝ\x001büÏH\x0004ÂKßÓÑÖ\x000b¶©Â6\x0007µNÂ&aÊÓFiØÍ\x0011Òï)ì\x0005ÛUa»\x0003`[ìaÝ6
¶S,;j¨é\x0005\x001bÛ-¶btÁV9W³åûÇë»µ&ÎåucX\x0019ÅéûX¦	ù¦ÊhªäÄ§øòòøu[Ìñª*^5\x0014/.¦:\x001eY\5Q\x0012¸Ö5ú\x0003ÖUÀz(`2¾ÁÝ¥\x001eÝ(-'F­mÕ4\x0000­©¢5CÑZÉÎ\x000e²CnL\x0002\x0016\x0016\Òårùý\x0001Û*`;üxÉJÒ``\x001bÅ\x0007Ìì`¢áýñº*^wÀ{#\x0006K§¸¼wóÞLÃ¬Æ\x0001}\x0015°\x001f\x0008\x0018Ý_\x0012\x0010\x001a°\x0013\x000b«bÉá\x0008±\x0000*à0#Â¤f//©p\x0006XBsâA5%Íû\x0003UÀqè	À\x0013i4n2"%m8þhuSæ¼7àM%eÒ\x0019b b§4gOÁ.¢ù½Qk_\Zsû#®k¹¡jÎY¯(o\x0002\x0012ªj\x0015Ïw3njEë¸¦çäPE\x0007\x001a­¼»èÉ{\x001e¬Ï¢:Æ\x0012\x0014²&åPQìlà8\x001fV/ÚÂì\x001a?¼\x0011tÇV|RP|2RïgÏ?¬ºy¨\x001a\x0017åH\x0012Ä'\x0015á²
®³\x000e
±\x001cJ½=ÿaÑênÇ"\x0005Å"\x0007@ÅÉÎôã9:ÑDÃ\x0003Áæþôª«Põ ¨ q¹±Yo\x0002Ôoû`\x001ePM\x0015ª\x0019\x0002\x0015\x0003r:ª
¢Q,vm)\x0006í\x0003ÕV¡ÚA§êdÉ¥ù¤ÑJÅPÁ%\x001d\x0005ª«BuNÕ¼|\x0017¡Jòì#:ösº-í×\x001dª¯BõÃ\x0018Àq£
¥}É\x00003ð½¶.ü\x001ePC\x0015j\x0018\x0004Õè"¬a\x0013\x0001õ0ªmËûu\x001a«Pã ¨¶¤¨pekô¤\x0005¸ÆØ\x0006ß½'Ô)£*3$úa\x001bÛ\x0016#%dÇl¤Uh)±íUºí\x000eF\õãpµJZ\x0011z÷øÇê¡\x0014P´\x0006\x0006\x001bÃLéºtÅÙÍ\x0002Ç¯ÎpÓJZ\x001búúò§ÅýpU\x0015®\x001a
7Ä\x00136
R\x00175\x001c~·®¡Ûb\x0000`]\x0005¬\x0002æþ EûPÄrfÕú\x0006¿l\x0000Z[Ek\x0007¢MéuIÇ\x001bÙÚ²!¶8\x001a?ø*`?\x0014°4Tß§ñOT\x0010ùG2hwKÛîxBng¯e²\x000eº»]Íæëëûåm×ZV#pØf
÷Âñj*»¥Ôº¡ûâ§×§ÙüüÍñÅü´­±`UU¬j\x0018V©y´­7¼® ¸HõÌ¸wh$°º
V\x000f\x0003ë\x0005É\ÜHrDeâúÅpÈén©Ð\x001b«©b5Ã°¢G\x0003º8(
-%]ÀâöQ°Ú*V;\x000c+öàÐ¹:M©æ\x0010\x0004õ\x0003Ø\x0006Ë»7XW\x0005ë\x0006U8\x00121 $¦@¹\x000bMiÞX}\x0015«\x001fUsM³sðÐ¨\x0011+\x0018ÊÄº\x0000\x0016ã8`C\x0015l\x0018\x0008\x0016á¸pÓL\x0013XkyÊµm\x0018?Ö\x001bl¬ÃÀ\x001aË£mÔ%\x000bÈí©xe\x0014°ÅVÌ
A\x000cäYE£Æ\x001cN\x0013ÈÓì\x00036lÓÑ:üÞhëêkþR',:k=\x0015ÎPVÂø\x0006ã«+XàÖíHL\x0010µ"']nâ@Þµãmô\x0014ÜðS}^µ\x0012/g'mã6\x0019¥ª¢TýQZgh.óÚRó$÷`´h;¢4Uf\x0000J4±¨5ÀQSaÓ\x001aÐ0@¨\x001fJWEé\x0006 Ô;ðð0sÊ\x0011,A®\x000cÇñ1ÀTÛéQe+\x0013Vß=^­Ö]jäGj¿Ó¸\x0006.û\x0004ZLn\x000b\x0011^Î¿¾|±8ï\x0000UU¡ª!P°ì\x001bâ-\x001a\x001aRfðÛ¶Zû\x001e@u\x0015¨\x001ev¦[q&O #|¤¶¥­\x000fRSEj\x0006!-yPS²^ÖnÒÌ­\x000e;ã´Uv\x0010NÏÕëv©Rýc]ëhÃÎ@]\x0015¨\x001b\x0004\x0014£-4.D5u\x0012\x001e\x0017µh\x0018\x001aÖ\x0017ª¯Bõ \òì«ñ\x000bçc\x001aü°ë\x0007÷r+0dD½Ïêlõe½¼ê´\e*­*ÃJÿÚÛ\x0014tS«\x001bwÞVðª*^5\x0014¯¶¸&$Û+®JB*ö\x00117=\x0001ë*`=\x0018°çT\x000c¶XEÉ\x000bYtÓt¶\x0001xM\x0015¯\x0019WÔF\x001eydx¾¬nkö\x0002l«í`À´./¸F¼àÒ®eLG¼bûÅüâÊ^éûÙ"ooîàdYNt:\x0015x\x0001x\¿hw£-K¦/fæ}Î\x0015¬ªU
Ãj
u¶`O6G\x0005<W³6,àêÔTaHÁcáaEóC\x0003x|¨¡!oÐ\x0019«Ü6\x000ce6\x000c\x0019+®x¼¹îVê\x0017D1
1úFSº¬ãA\x0010
­hqMÄåÉqKÜ6\x000ee6\x000eÁ¥¼Ü\x0014Ä8ímuöÇª«XõP¬\x0011w^q«£âÏ2PÈQ}=àºmíëD--\x0003l{~{c:&\x0012\x0003Å1\x0000±àEÁFËFj(Õ(¡màÝó×¸5¦5´­¨%gúö¨\x0018\x0018´gk/ \x001bZ\x001fÐoµ~;¶V]¯®0Ð©\x0005N9-(k\x000bR,P\x0001h\x0010²¶\x0001E{íÉbvv¼xÙV¸·Â-èÀ\x0000=sr)yï<ã\x0015ôC>\x0006pÞæûÊÊÌÌ¥ê=Ïxm\x0016Èz[ÍiQ÷~?¯n;åkÐà)t D$Íî\x000cØ½6ðÓì\x0012CUU¨j\x0010Tã(\x0015f"\x001f$!
gbS\x0011sO¤ºT\x000fC*¸+Þà7*\x0008æz|'G:S[Ej\x0007!\x0005OBrýçÐòì!F\x001e\x0000ÕW¡úAP]\x0005j(u÷û÷hëî\x0000UnG\x0011e¨Ûc³\x000c\x0004A'¼Â\x001av,ÉÆCpì¯aum»¥3Kÿ\x001dÈ\x000eM\x0015³\x0019ÙË2*(\x001eî\x0003ÿH \x000e\x000fÂìªÝ\x0001ç¬±n2·Ð9N¸Rà\x0013dÃ4A C\x0015t8\x00004\x0017´{\x0011yäÓì
\x0005Õ06e\x0018æÚX\x001b1G\x0004×~yÐp¤æÀ.ØøÝÏ»aÎöú,)E­÷¥çÜu-y\x0002\x001c1Í­ãÌ\x001exGroí~,·wgI)jí/=ÍàhI¡\x0007?G,\x0019Áj9`Móh u\x0015´\x001e~ÎÒrb¥1\x0014\x000e"4¬\x0005í\x0007:n3GÜ2ëgo®o;\x0017¬XS*MôÜ\x001a¥tÙ\x0003Ø´5fc!ÏÞ\x001cî©±\x0011Û¾pUþ¿ÿñ¿~xü´\ßtË­àâBj\x0007§$\x0017´;±i)òìË³ùy{re{$?uUnÚ@\x0001ðâýÍõ}·¸\x000fÛBð\x000e¹×¨LÝ°>î¶ä7m ³ÅËãÖ¨Ïv%7T\x000eÅk%·\x0011`\x0010\x0003²L\x000ez·QÔ\x001dò[xj[~|â2õ\×à­¥r\x000bPÓ}=­
éùI³wOè¢ÓÊ\x0002^UÁ«ÀÃÿÉ\x000cn´$\x0017\x0014¼3\x0014õù8à·|§gä;\x001d´PÈó\x0002\x0012\x001c/ÌãFSßm®w»ipûzm\x0013»Ü\x0016~JlöÚ
è(l¦%äÀéS»O½R®W\x0016¡î^î#~þr»ú÷O\x0004\x001bÁ¾Y\x0002Â/ë\x0004QÚ\x000cQ|wñç}þó¿ÖËw³«ÿgþy\x0005ÿ=\x0006$pôÉòÓ\x0012\x0004:<^ñç¼y\x000f·\x0018¬1Ã\x0002Iïòpgm#-EZü¸8?\x0007i7ÿqñÏó×§ß½\x0003LøSÓÂVñó/Â_]\x0019blvQ/qïí§5è>¸µÿæ\x001f7«<ÿðçÿyX-\x001f\x0001ºÒç\x0008
X&	Z\x0007°;ér8Q«à²¥ú\x0004;z0Ïç¸\x000e÷ì¼eçl¼!ut\x00124
G\x0012,f÷\x0012	!\x0017öa\x000e*ç\x001cF!!¯/\x001a\x0004ëòÐ
 Á¥bU$\x0001þIÈáòQHS\x0004ª¾·\x0018äÇT`&!+( !dq3\x0006	XGÅu÷ãÒ\x0010²èA\x001aÂ$\x0012rs¡Æ\x0001Îz4\x0012%å\x0014ï
q°\x001cÛbmn"AÄÀ$ä~á$Üÿ±~û¶¶Bz9K6ÍÃÃjìT8Ý"9B\x0016W¶\x001dÄúZÒ\x0002*ûsv\x0002ÆÌ\x001b6oÞ4Y45¬´$ë@¬&x#VUn	+ü;\x0018«\x001e\x0005,í:?\x0010,\x0008\x0012Ã`%NSB°"+Ð8Ud·Hé¶^\x001f\x0015ü÷¡:î{\x001aCäs»¹¶'V\x0010@v\x0004u¹à	ÀsÉ\x000c+\x001dUf\x0014°´(ïP¥cµi;BBª
RáFaW 7\x001e\x0014\x0017
$c\x001byÀb®0\x001f+cr·úèû´~^âãZ\x001eþºbÖg+6,ëuy^ÃÏÖ	\x000fºj¢X<¾_Ýâ
Ô÷)y°ÁQXÄ\x0006)ÓÌ|\x001c©­!I	Ó¬­\x0017/\x0017§¸\x001dõåec®³FÄÆt\x001d\x0008°ÒK\x000cÂ;¬4ÎDäQê\x001aø<\x000fz\x001dñ:.\x0011\x0006õYô'\x000b\x0011.á&¤k6:z\x0013±1_Ç%"'¿\x0008-<>D¦Àæì\x0003iÀ\x001e¹å}åIl"Å7K° nîW«Zºÿ ´·8!\x0005\x0008òÂ§å¨hGy\x0015¤±ÜOèÙá?\Ì_,ö\x0005ÔËOeZâ$ø|)ke=N\x0000Éß\x0019\x0003¹ Èb^E3\x0001yù\x0011ML¦ùß\x0016«1ßÈÓ>»´Òãò©iÈËÏkZòT¤áÖ\x001bv
!yörÀíá²iÈËãÄ//¼\x0007Ûz	B=ÒË³¹ä\x0011\x000c\x0002\x001b§bÎlÇL|{@Dv!<-±Dòà\x001f<g\x001b\x0015#¼=4}\x000c>ÿmB
Õä\x0014~=åðó[¤ïíäúA¤\x001dË¨\x001eÒrÕtÂ³b·ç8Àå½DEµsàø\x0019à¹¿»Y]ß\x001c\x001eå¤V/ê\x001c.×}k%Þ-T8¦ül1¿¼x}²8>éBFVâSaóTd #ª
\x0019\x0014+Q©ny<2r\x0018b\x00022\x0004ÍgÀÛÐ\x001cí4\x0019\x001cÈ°q·ó1lsLA\x0006ÍAÀt¡ÅzDñd¹\x000b\x001fv\x0007\x0002\x0017S¡²9\x0011À\x0004¦Ây~\x001av·í>l!OEÜ( ÃbõJ&CF¾8b\x000f2¾¬?Þº/[nùËÇëåãÇÕìÍ»ËûÙùòËí²\x000b=OC ¸tC 
kd1¦ èYh+\x001aB
èEótr2¿|µ½ùáõ«ùÅì|þÏÓy'Z@òùÑiqVÐ}À\x0013OË\x0016 FR|$ìN\x001dHK6áÆ¦Å#£)°h2)&r$Õ7Ñ\x000e£¥ä\x0018É@T¹L±ÓN<¦â¸n\x000eü4\x0011³£bªFI%×1*%!\x000f§Ã\x0010ÇÉ\x0014S2\x0007º9ivÀ½\x0000ãò\x0016è1L\x0019¬É\x000fÆá(ÜDMÌeÁ6Ç\x000e \x0006n7ÂH
®[YÑb^¤Æ(ÇáQ«#B\x0007P\x0003ºwI*\x0000LÀ\x000ew\x0003& af
ß³ÍYµ\x0003¨\x0001±,Ç\x0017ÍÞrø'â#\x001b¡4§6FNB
<F^H=&5\x0015?pZ¤9M\x0016jÌ$R\x0000H¯j¼ßPã³\x00080´c\x000bHÁºòñIÁ}Öj|EãñÑD"E a©\x0011l\x0001¨æàü\x0001ÄXQãf_å^Ð\x001c_mz\x001fój\x0013ü°\x001b(S\x0007õà½´¤~\x000e \x0006´\x0017ïÍ\x001e`\x0014§ä±D2dj¬3üüE\x0013v 5páj|# èW¬\x00025FãlîD
ü\x0013S#§\x0010f8ÄWo\x0004DaóV
Àg¹#5Î°\x000f Ú\x001du9\x001a+j|# Ü)\x000eÄ`My\x0016\x0002N·¯ñ\x000fcÑòë»ë·o«&\x0006÷Î®ß¯àoåòÏþ6\x000c¼u­egÓtìÅ\x0004º\x000c\x001b\x001bB`ç\x0018Â;;~¹x}zz¼8uAM	ß\x0011P\x0007\x001b\x00005ÌÚ\x001dyPÓn÷QPçx×\x0008¨½HÙù¬Ý\x0011Q¸rÔ
¦ü\x0000Ð\x001e\x0001´¤¹xÔ\x001eë3êÈá\x0007çÇCYc0\x0008x\x0017:¦ÌQB\x001d\x001c±µS#¢¦ìù\x0008g­ãÑæ¨-©`ÍÞm,º\x001d\x0000Â;c0a¿ÁË´b;¡\x0016,ÎáQ6¨Ú\x0001¨©Hu\x0004Ô\x0018I#¹g$NyK¨\x001d£ÆPúh¨)ü4\x0002jÐþ.5^\x0018
9\x0015Åé´k08ûc.a¦\x0011@G\x0017/ãQ»£,@ÀýçêÈ G;i\x001c''ÇQ^ÜÖ\x0006¨½æ£VÚÐ`\x000e\x000f@
¢H¤b¼g»×\x0005s$Ø»¢\x001bí\x000cÅ\x0001¨9Dt8êãIðfÏQzÜ\x0015Ç-Ýx,ÂÑ\x0011`ã\x0002XG¯Q`¿DÍÉ\x0005xM¾ì\x0000Ø\x001cX\x0018\x00016x\x0013ù9z³Am#£n,ëº¸Ý# \x0006ëÔZ:lEéç,<è°Íx°Ù)\x001d\x0001¶Ù\x0008?Líì2XßTyß\x0015öÇ¸þÍ?l¥~XÝ®¯g/\x001eoibAoØ\x001a\x0003\x001bùEz\x001b(®bÐü"CKøìÅéù1À?7Î0¨ÁÞÔþ­`_ðw½)Xý[Á&×àï\x0006{SYû·½Iþ~û°ïV"~ÖÕ':ÕO\x000f×w8z\x0016;àn­|Â	`\x0014±\x0012Xä\x0008Bàh\x0003ü¹Á\x0016Lmì§ó7Ç¯qv5\x0000i¬æw\x001f\x001ftµ}j5;#|X\x001d^È\x0011$¶O¥Jr/¨Ü)Ce½
Ç\x001fïnIXÌÎ^_bïW\x0017ØÔI5\x001elðormVP`\EKÕ@[\x0011B)Û\x0001vx÷Vÿñ±®2on6í÷÷ï\x001e¯V7\x0007wÝY,\x000bHmîpô:DE\x001a";\x0011J5ç:NN¸;ÿâùåÅIKë]¢I§¡ÆçHg>\x0007¡]ÔÊ³\x0016!õaÔ\x0014\x0005;\x00055\x0006\x001c
§¨ÁBb\.=jo¨9!5GJNQ¼Ó\<"j¦\x001a!à4\x0015Óbc1Ê0j>þoñpþï@M¥@`\x0013M^É\x000cäàò?Kê0rUlnMÚAÏÎ*¡?ìJÛþñ\x001aHùt³¼¾íÒ×ßh©l#Xa¨Ö\x001e
÷Ù&øã1À?;\x001f6÷èÝ·\x001f>¯\x0001xÚ*~\¬Ö\x001fW\x0008¿ýÔ<
gK\x0007ï¬\x0014ÜNæ±rZø`w?òÅù«\x0005o6¢îÅÕ/\x001fþUÍú¬î±\x00152o®ÛköE÷ÝùêÝÝãÍêþ\x001fgkø;×·¿?^ÿùkø»\x0018T\x0010yÂ¶\x0013\x0008Þ\x0011}04\x000bÃÀE4\x0019!\x0017Ø\x0018y
ÿÑý¹·Õ\ÍÖz\x0019½Z®Á*¹^ýq(û«4&%\x0019À3d\x000c\x001bOAãvQ²µÈd½^\x001c/~j¦íãï«m\x0019ø\x0016ëCÙIJ&¬4¼\x0015G\x001a\x001f²4^9K8X¯ÉÄÂ·0?oa¨_Ä\x0015¼×Ð¥Ú_\x0002XäÑæ§%¥:?\x0005MY)»(÷<Æ)0\x001fÞÝ»ûP9óêDÛçËõÕò-
ÖNïâi°¥H`Í)\x0011\x0015\x0005h¶ö"÷´åq~þbþ\x000cé\x0005Ïôá_ÿrwõ¸£ã\x0000á¿\Ýþùÿu:ÿ§\x001cÈ}®ð©?PÃG(\x0013\x001b÷BÇ¦Î7{P×\x001b\x000c\x000eEíÝÎ\x0007\x001e²§pn\x0013Av
õ}!×	\x000elP«æa°K¤\x000c$b¼oP°}Q×{\x0007F8hã\x0008µ¡ö
<kÇ¨Û+í»Î¡Ñ@Ì\x0003ö¾\x0017Ð\x001cõ¡¡è±\x0013jswý»ùÜ H\x0010õ}^ÓxìþÈy*9ÆU$Yü*rõ¹ó
ôÛÀ<O\x0003³[Áï\x0016#\x0007Q¢((³¾\x0015\x0012\x000eæÛÁFCÐï~\x0007 7àkéX2(T\&´+\x0019\x0006gkÐÙ§¨ØÞ\x0007ÿ1&\x0011"ð¤
ïL\x0003x½\x001cëø\\x001biàí72\x000füÍ¿H%ò6\x001fÐ¢\x001f\x000f5è-^	¹ÿ-å¶rãXàÎgs³§Ç\x00074é<+¤Ø\x001a)v|R\x001c<ejs\x000ep+1¥¼\x0008ys*Ðâ\x001bLü'´\x0014ã¦\x0016W£ÅM@KÉEûà#n\x0001³3OÿÄý c\x0012j¤	Hq.»/H
§Õ½\x0014ÔS"cØ×'ÚX#%O
x-G¹
\x001b¼ß£ç\x0008I©vðã\x001aºz¢D\x0014¬$\x001fýV´æ\x0015\x00017ÌúLãKÙgqt'EÖH\x0013Üu¤RÐ§\x0011sp\x0017o¥¡\­?)ªFàVÀz%	æ\x00055,a,K°¦rþ¤Ô\x0014@±X\x001cüÇÅsGrtE³øÈ]gZÖ¿ýaotÅLÙ\x0015º\x0018-
+Ó^î\x001cIsþá\x0018iJ\x0014f·Ñ¸+v£2;\x0014¦\x001cV&íÖ!Ó¤\x0014F#3M\x0014X2
®ÒP²÷1-ERä?'°Ñ¸L\x0011Ï¯2F5ôô¢Éßÿë·OU\x0000 ðåì\x000c§N>\x000eªuÁF+I½Ñ\x001eÑ\x0004<U\x001a/uC8	þóôr1;Ã9ç;MI\x0011ÉÚü\x0002ý)Â<__ß?\_ÁÃ__ç!Î\x0007¥\x001e-\x000eÉñzlQÊ\x0015RÖó(\x001deZaùùñÅã\x0017ðüÏç;WÈRU²Ôdd´¾!e4%q\x001a\x000bÍô5±¡äu(YºJ,'xÂ¬	zJ­ç\x000ek\x001a:üReªTé.Ëòü7\!#é²Ld²dCCöP²l,;\x0019Y2/\x0013\x0001òÀÌñ*ç8éj\x000cé¡T¹*Un:¡yZ¶<\x001dø%5\x0002\x0003\x000f6\x000c9\x001eJV¨\x0015¦{Y"z\x0001û
ÉA.ËU¼sx,²¤¨w1\x0019]8PØdº¥!\x0016=S¢Ë+ßeM¾Ëé\x0004¼	Ô\x0015\x0015¬64Ú×z¡
CÃ\x0008¸¡tÕD¡N\x0016\x00021n#4t\x0016\x001aÓTc\x000b
Y\x0013\x001ar:©\x0001¼ÓèÖ¥\x001d\x0018,\x001eù¦\SêP²jBCN'5¤£Bð<\x0006æ²§½Ê©qé\x0003éR5©¡¦\x001a"²êB;®Ë²êrº¡{o(Yu£p:¡\x0001þ\x0013­I\x0000S!y\3
\x0001¡¡tÕNh\x0008Éõ]Nª#\x0017.ê\x0000WÎ6t\x0019\x000f¥«&5ÔdR\x0003\x0007ãÌðrÜ\x001eÈ"\x0017^9×P7¬ÔPI
\h%<åÑìHt\x0015Ë5LO\x001cH®	
=ÐÀZ#2ãS´töL£Pº&5ôdRÃDW\x0001]ÆÐ4O\x000cÈi+F¥«&5ôdR\x0003'ßäEp¥Z\x001dìàÀR¾©®d(]5©¡§\x001aèNw Ç\x000cÑÅ\x001eJ2\x0012Ç¤«&6ôtb\x0003\x0013KÙwQÐèKë$MU\x001e+`G¤ËÔäNnxÉ¿T\x0005
:TkÝ©»\x0013äCéªÉ
3ÜðF\x0006Ü&jH\x001e²GéuCÑõP²êÁéÄ\x0006\W.2
\x001eÌ_É·ET\x0019;*UZ-©\x001b\x0005¿NÑ\x0014ëI-ë0®a.ë`Ëw<¥&$\x000fk#\x001bÀú\x001apR\x0010«2ÓP#6Xý¼ÜRfËÿ6ì'77åÅýÅÔé'Ôé)É3Qäd\x001dXqc\x0011\x000bv`ÂèRå!¯¬H\x0015üÍTäi+\x0003R\x0005.¨³üêFÁ	³}yfJÖ\x000c©´"³&OäÆÅ\x000c5ÇugÜ¦NNI\x0011lt\x0019 Tñ\x001fK±g(dg\x0007È[\\x0006^Íù=Kaï\x0001yÊ½\x0006¤"Í­+\x0006	Õò)ì¹è´lº¡Bª¡F'\x0003\x0007b½³IGP½·
uc}ÉÐU2ôØd`|ÜJ´£§\x0008v0Åj5ç;aªdÑo\x0003Dw4t\x001b>àL2Ç·ÑÁïK­aÇ&ÃahuyDúV­ÞMèL«\x0012áÆ¿\x000bëÝð*Øre¯×¶{IðU\x0012ÔR´ßCÙï\x0000N®/Nðì\x000cª}É\x0008U2Âè[óÐ¾Â\x000cù´A3\x0019f¤W\x0011«dÄÑo\x0003È`»,*j\x0001Ï
Cµ{æ]©(ÉÐ¬÷Äè·\x0011Ò¡LF¤ash¢\x0014W¼aK_:êú{t\x0005î.#DêFµ¡t>{ÕÐ×\x0002£kp\x0014¶¤ÁÁ*Év_">ªaÐ{_:j\x001a\®Â¦ ¾B¯,¿ò\x00109­éVHö¥£¦Âåè:ÜÉ´²#Þ\x00070Y,"­dMËÑ8Îï¤çá<Í¨·Q8Ë×Ñ°@µ/\x00195-.GWã\x000eG S&èòÌeéUmÚÙ*£ër/#ÕHÂ}h.fM\x0012\x0017\x001b(ûÒQÓårte*\x0014\x0013ÄÖî,­Vl¨Ëv\x0017°3\x00195].GWæ¸Z 1ß\x0013éylòXÑâ7©6W£ks[½YêzÎ3\x0006cË}ÖCg:jÚ\®Í½<*ÃÙRr\x0016\x000b\x001d.¶Æb;Q÷ÆÇWæ^\x001d)zåÞàO×a\x0003\x001b%¢aê__:jÊ\¯ÌáÓ>h|ðTØ\x0018©\x001bM¹Ð0Ý¼/\x00195]®Æ×åÁr}fÊ~æ°Bð\x001b¤=«Û.Wãër\x0000ï+YwºÀ&\x0017\x001a¶ö¥£¦ÌÕøÊ\x001c¼X¾\x000eÃQ\x0010\x0005Ñ^Þ*Wã«rlÎ Ç\x0001bL\x0018U	a7´`÷¥£¦ÊÕèªÜ\x000bw¤ø:\x0004­Ö\x0005\x0013Qq\x001eGM«ñUyp¥àK{
º¹$#9£0
[é*×£«r/iÈOÀ%\x00012°¸Ñ£ø³º¦\x0002õè*\x0010\x00170±¬²#÷\x0001*8
\x001d5Y¥GU\x001eÌ\x0010VFSj?ºÂTãÈ*WUnlYe¶XôçÃy$\x0008\x001f²QM»¶èhOÕøJ\x0016B¡,ÔXÊCi\x001c×\x001ds[¢¡1pàª½®³{¦c\x0018=\x00011ÖâàÂ\x0011ò+ç°\x0015»çf¬(Ü65RNq7À[4\x001a\x000eÞ7Zò9\x0018Wb&ãx!ðs0ÅÝ`\x0004ï&p¥­%\x0017Õ­qþc\x00187\x00051Bàr\x001fNIÑÍ8Ã\x0016°mXÓ;*÷ÏÌ$2ÀqÖÖ¡Úw\x0014/\x0015W²a¶DGrÀöáÍã_TÏW³þ×-b»Áù/77\x0007·{x=\x0015ÇH^#¾\x0019Þ¹\x001cÛ\x000b­^\¦,çó\x0013±ør~yrÒ2ÓITU\x0012ÕÄ$\x0006F\x0015%\x0012} 8\x0005\x00163òï & QWIÔ(¨ÝGð×%\x00127û¿Õ\x0004$*fj\x0012Ë\x0008DP»	(­À\x000bçCÃ¾H´U\x0012í_@bÖdÀ¨\x0002H¢â[lo:\x001bF¢«è¦&Qmv£GÞ¨áË<gÑ´òù 
}B?5Zò\x0004"îó\x0018]\x001a=EhX\x0005}\x0010¡JbDÜ)5!È¹<sÁcÕR¦P¢7:±JaB,¨¦Ý\x0019¤\x0015£by\x001aÚ]°A$nZ\x0013v1µæ\x000fG3À\x0013ÉË¦@Mp$Iñe¬6SÛ6@\x0017\x0019Ó l,^hfTÍò4¶Wv
£±fÛÈ©\x001bxu·èh\x000eWãR¸V#{\x00185ãFNmÝxoê\x0001Ñ%\x001aM\x0011©S<Æq#§¶nÀ±ã±\x0007`W\x001diGf8§h¥hÏ	\x000e£±fÝÈ©Í\x001bo\x0015Å|á\x001a%OéRó·"¶GQÑX3oäÔöM@\x001dî|¾F©Y¨âÇ'±fßÈ©
\x001cU\x0011¬\x001b
µæókÓÞ¼=Æ#§¶pãV8\x001f­=
g/²æpíA¥a4ÖL\x001c9µ\x0003JØ·W\x0012xé\x001d?G\x001fÇçUU³qÔÔ6³¢¸þ%\x0004¥Ý|{qÑX³rÔä\x0011\x001c\x0011\x000byâvã2¶W
#°\x001e¾ÚÄq¨ÓþfÓ:®j\x0017f\x0002½¨jæÚ¼I\x0019@\x0017(ËÌZÃ}\x0014Âµ7]
£±fß¨©í\x001b,'g&Í!t7kí)\x0018FbÍ¼QS7\x000e¼ý\£
:ÃäÎ\x0005/\x0015 Á|êø$Ö¬\x001b5¹uS\x0002úpÚ\x0003=\x0008<Ê\x001c=M\x0001Ãh¬7jjó\x0006Ç.{Pä[eÕo7*c{¬7jjóÆëoé\x001e¥dÕÂHtí\x0003]ÑX3oÔÔæ
\x0016\x0000ä-(p\x0014\x000c©þ\x0012\x00127íµíhÔ5óFOmÞà\x000c¯@CHØàp\x0012-Ñ('àU]3oôÔæ
n0fÍ³4ÛÙ\x000b¦QO\x0010\x0014×5\x000bGOmá\x0018Ì¼Ñ$nÇ-É\x0018Ä\x0004×XOPMnäàÞrzàxäQfðûbÈéö2Âa4Ö\x001c=µcÀzË\x0015¸>Xj/wÁÐkÑ·WQ
#±fäè©\x001c×Hj\x00029Æ.òú.\x0019]Ã4ïh¬Y9zj+GKAÆx cÜ9ø§	\x001d*]3qôÔ&\x000eN\x001fÉm_>hÞaà"\x0006hy@5ÖÔ¿ZýãXfKcô'yã\x0002oáÑ´Wf\x000e¢ÑÔT£Z5\x001aç*o1SÈÃ!§y¦¦5ÌÔZÃò×²l\x000e±t&RãæñI¬IT3µD\x00057jVÓ\x0016\x000e²©\x000eþÌ
\x001eÆÀ1S\x000b\x001c\x001d%fm2w8ïDY\x0000\x0013Æ\x00178¦&pÌÔ\x0002G+·±Å=M»s®è
Ù°\x0018æ\x0010\x0012mMÞØ©å.S«R *7Jn,6 jk\x0012ÇN-qTÔÔ`áÁìf\x0003g3<Sö¢åa4ÖË¦\x00169J;.\x0017¸\x001a4\x001bªÖq_«´\x0013$TmMäØ©EÚ}D0ì\x0019[ÍÏQz?¾Kek\x0012ÇN-qd\x0004êëEÑ\x001cVrAª ãj\x0012ÇM-q¤7\x0014\x001a\x000fRzÜ¾$ÊM8ã3ª«	\x001c7µÀ I%-jWF²;ã¹ä[É)h¬	\x001c7µÀI;«%u(\x0003$\x001a­äN\x0010\x0015Æ·ã\Mà¸©\x0005À¹óD#Î6É¯Qs\x001dµBÏct\x0012k\x0002ÇM-p\x0004\x000esÈ]0JXj¯Òi Qåª=1ü$+Õý\x0013qì¦?QzI\x0003w\x0011\\x0000¨lûveñÛ¤ªé)
>m#Ée\x0000¼cÀ\x0003ß2	2¬âÉ¥þ\x0005wúUZ\x001dä;Á¥bU µÙüáH9®
¤KÒõ\x000fEîìÃÛ\x0004>¡ó¯¸Ò`±8é\x0014D§åú\x000e ³ÿ6Ð©¶ÖÁIÖÁ\x0003qß¯ð·¯ïgß/ß^\x001fJÁÕÈÀsî#O´¶!Éz\x000e\x0004}>?}þúøböýüÙq\x001bwª­uiH\x001aÇÓ5p ÜR-nM:\x001cS%ÇLAN0\x000es\x001c°H)>\x000cÊÈÁy	£c«äØin'¡±QðíÍt\x0007xI»Í!äø*9~\x0012r6þ	\x0017°Ä2@Ëj³ÛÐ\x001cBN¬\x0013'!'¸r;ÎÐ\x000c\x0011*[29rD^ûù÷:·ý>ÅëAeÍ*+\x0015}p¢Tr[×P\x0002<¢_ê\x0014ý2\x0005E\x0018\x0013£ýg@\Þ.èàø\x0001¹©;¤õÏwuy}7É\x001dÝ6\x000fcM\x0014öpk\x001bò
ÃîèCý>LA<m\x001f÷åùgN8¶oLÜawtS¿£IîÈ\x001fñ\x0015y\x0019\x0008Ãæ\x0005F$èc \x0010diÙ=Pd`(ñ:,u\x0019¢_ë\x0014ý:\x0005EJ¡ÀÎ\x0014ÅòÊzNÛ°udØ+zWEï&ÝÌR-6LWä\x000f»CªÃ®è]ý&¡È\x0008¶\x0016@Ò8Z\x000blº°Ô°;úX¿£Iò\x001bÂ\x0011]Õº(£ñÔ«þù·ú\x0015ý6	ÓE\x001eÁ¾ÄtºøBcÞÐÛú
½ VE~c\x0000é²\x0006¶¡yf\x0018A¿Õ	ä´¢  H\x001e\x0011A¶,Dñ
µ$ÃXîSå>MbÑ\x0005\x000eV[¡6\x0016],öOCú0®ê\x0014]MrE]pÜ\x001diJ+\x0011\x0005×\x001eFÑ:EXtðv/~\x0004Kn«\x000bE
{\x0002=£Uý\x0019­¦òë°>Òm{F~T_ï¶NÑí$wdy»&®ç¬ê\x001a¦'\x000fãºÛ:×MB\x0011°aed6a{Á6\x000f£hY§h9Q4Üq0W
=#_\x0004o(Ê\x001dÆt¿Ön\x0012«[rEJm\=UÔQÃèña\x0014}ªS4:R¢ø\x0011Òp±¦0¼\x0003Úºy"Ã(º«S4I\x0001/\x001c	pûX0\x0018_(²c\x0006\x0018Þ×)z?Éàxn?:Êo\x000bå¨kÈ\x0016\x000e£hY§h\x0012ÁL9\x00143Õ\x0016m4j\x000cèºNÐõ$Áó,:¬aÏ#NA0ðoK/Æ£h]§h=QÈÄ0ÓÉb1èP½5ÏÃ´Ñu]\x001bMrGÊnÈñl.LA­\x0007éì4A:\x0015yW$\x0017\x0001ä\x001b32ü¶~?ø®&5\x000bä7$\x001fáyqm\x001a¢=¢÷u&\x0011ÜZ`r<_®\Qñ#\x001aú1ÝUé&ñõ@ÿX½u³\x001aýwSÄºWõ;Ä3Òe\x0013\x0019*×\x0012¥Ó\x001bsaL®û¥NÑ$9#­6æÝPTè9\x001c%T½XAáÈÍ¢¼zÝ=Þ?¬n\x000e¥\x0003G£xj#Æå\x0013ùõ¨2àYøyq9;{}yñfq²\x000cU%COF,cÂp½¯"2\x0002ÑÔ~Ù\x000c]%CN\x0011Gz3^)¯\x0006pØèÄåM
cùúaªdñÉð¥o;ª#\x001f\x0012©påë\x0018dØ*\x0019vt2@øÒr\x001c!=\x0017 KÏ\x0016´lè\x0005íK«RáF§BG\x001aff\x0004ÒeÈ¨¹L´D\x000eûá«dø±É\x0008Ñb-H"Ã\x0006d¯D\x000e\x001b\x001eZ|è>d*\x0019aôÛ\x0000FÒDQ´\x001eÎIgyH\x000eãÈÛX%#\x001bR "ÏhHT\x0018\x001e\x0003'MÃTlÆi&å'Æ'CàHtxÍBRsá¾t-Iø>tÔøèZ<`	\x0018qUÐ´<ÑIÁë&dÃ¾¥¾dÔ¸\x001c]c\x001d3\x0019U"86|¥d3Q¶Ôáô!£¦ÄåèZ<|¢¦\x001e\x0001Z³O±¼Ð}êCGMËÑÕxc\x0011Kç\x000eÄ¤(-\x001f¢%úß\x001a£ëñ`mé@\x0012²àq\x0007j\x0014\x0005(kz\¯È\x0005w§\x0006©6ÂÊ~\x0006ÙRçÙ"ãkrg9¾º¥­\x0004³lèëëKGMËñU9\x0008]ÃÏh:¥yæ\x001bµ\x0019*ãër_Ê\x001fAÒrQ¯TÃât¨2W£+sÖêÈ(	[b*ïÜ7l\x0010îKGM«ñyÔ¼?FjÅ\x0001-©\x001dóUÓ6¾tÔÔ \x001aß³^R\x0005lPÊ¦®âgÞ\x0012;íCFM\x000bªñÙ h~\x0005ØºÆ:;e8c,Í8âJÕ´ \x001aßõé\x0000\x0006ÿ\x0001\x001d¼^µ\x0014ùô!£¦\x0005ÕøZ\x0010,*VBË£@R¬$UC\x0007X_:jZP®\x0005Ó¼^6\x0012\x001dÎ¢ëàÙý`\x000cBGM\x000bª±µ Åí\x0011$­À\x0002¢ÁîNy.ã²¡¡´/\x001d5-¨F×\x0011´ º¤6`Ræ®(q=ÉÐ5å¡Ççb\x0007\x0010
¡7\x0001sWùyðì\x000bÙ43©/\x001dõ@èØÊ\x0003Ø*Ò¸Ô\x0015HE 
4b½\x0013|«.¸£\x0010;þbì(·hùè4­¯r Ç9®ÛVÔ[¡fw[c±K¶IQSÐ\x0012"ÜLV#¸i"?¥¼iñ`OJ\x001eVë-Jð7c\x001b(<^4H\Ýl \x0010%¶amOJ~\>%~9~øÇ\x0017\x0004CË\x00190|Âëf©45	oe@¤-\x0019«»õûÕýìÙzy¿º½?ôõ{Ëµ¡>b1\x000e-¶ß2ÍïååâõùËÅÅìÙùüâbqzÑ1´[i\x0004$ÉNDe^¯°äõz\x0019C\x0019.e\x001fN\$7Õ-9Ì£¤\x0015\x001dPexÀ
6ãä«$ùHÒ\x0002ÂpKðÉPfñË=ÃHUâD$áBe¢s($Å'ZÚ²zT]µØOçÂI\x001d1M\x001cBjIöö§HÖ(SQÄ\x0008I	\x0017h,·ÔR;Þ¦\x0010SIqá7#=e³=X
Ù¦±¥Ù¬?I¦F$\x0017#@\x000eÁÑ²x/uDRlXî;ðê\x00039\x0014\x000fäæ¶\x001cï\x001f
>Rø\x000cnËð\x0010ËØ0|è{BÚÂQ¢§¸XG´eÇº\x0013¦¤Øª×AYH~\x0011Ps¾¼¾¿>\x0018ãâ¢\x0004\x0013S/N«²9e	÷Õ\x0005\x0000JÎçÇ\x0017Ç]\x0008ñUBüßX%$þ}	uÖú;ò\x0016Hz5\x0018\x0001¦<òÅãz\x0004\x001fH\x0006nB\x0017X#®¹\x0007«\x0007[¦S\\·\x000c\x0018¼©7c§Ð¦"«¦]7ÌëÝU±»1±ÍêCÅÍ\x0013eloÓ
xec\x0005\x0000ç¸Ù(È½\x0015¤\x001e\Ìb£u%\x0012Û7Êè\x001b<æ\x000c½2o\x001bùEÊ0\x0002#à9hi¸¶K]Òµ¨¶n\x0007oêÜ>.»Rîá=\x0019S¾\\x000fåÊ\x001cp\x0004oG\x0005/KÜ\x001bË\x001dé±j½	´\x001e
¾öVÍ¨µ\x0002Þê
ßlÀ7,déÞ×ÐûQÑ+Zï\x00042Þ\x0017\x0019¯¹Nªæ³èC
}\x0018\x0015½.5gJÑh8DÏ\x0006Õ°_´\x000bz¿U3\x0013Ë0;Y>,ÿ¸{<Ô¶:5%dÖw\m\x0016
\x000b\x001dÓVO³ÌßÌz}¹
U¥BN\x0005H\x001fjí\x0001EÅ%ãQDN\µÅ\x0018û¡«dèñ/Ãð8.Á+Úæ¢y0l\x000bÂõ!ÃVÉ°£¡Ê\x0010;´}h}RÔ\x001c»nOëö ÃUÉpãa2\x0019\x001bú¢
¥¼·%ÉÞ
_¥ÂOÙ¨Rø\x0017U)'U-ö\\x001f2B0þ\x000bwG_8OPuQúBF[oK\x000f2b86\x0019Æë#[û®\x000e®ÄoÛúx{PQÜúJ­õhdèèy¹F³m\x0013ì `Æ!£®ûFW~&ï\x0004Ï©\Ë-:Ár\x0001?*ÂQè¨i?9ºúû«®£¦ýäèêÏØPvÒYé¨t\x001d%\x001fM`£Ðajt¿ëuÔ´¸\x001c]\x001b\x001dçP«æÑº¸¢c­m5±=è¨)@9º\x0006Ä¥UºÀM\x0000ei\x0015ßlë'ìAGMuÈñu4\ÛPVáá®\x0011æ«¶ª¿ît¨ÔUãK]\x0019ËÎBx)¼a+r\x0011&\x0012ãÐQ\x0013Wjtq¥¥EÛ\x0016éð Öó+wfáI m\x0014¶\x0012¾]I6b©\x0004\x001aïR"\x0017øú\x0018--\x0004w!°ë!bKf¹\x0017sU&#döz;ö½\x001aôNdä\x001d/#o7ÓcñWeòKæ°åØ·"¸×>\x0015dÛÝáæ \x0002ÆÑ$fÅ@)Ïc^\x0004\x0016[n±Øßô^¶\x0012«¾X\x001d3êPv« kÅQ\x0007ÃÅsàZ
\x000eHx$hÇH\x0016ÿ¢\x0012Éºù¿ÿñ¿æoß®fÏVë÷w·\x001fº\x000ctÏw'ËOËÛ»Çû\x0015P³×\x0018­cc\x0005$4ÍÕVÄv"fógÏ\x0016³gó¯/OØ=Ë¡FªR£F§Æåì\x0011\x0018ÂæH\x00121AY6*1ºJ©±zï\x001cÏwÓÇûÿ¹{»$»n#ßw*5
 \x0013á§\x0012EYtP$»HvÜÓ/ÄcñLºùÑqO?õ4z\x0006Ýïg\x0006Iä"\x00172±M\x0002µ×*@\x0011r´;Dmiý
@f"ùÏC8¦Æ1Óq4±´Õ,·}'\x001cVFJ«3PF:ck\x001c;\x0019Ç\x0004,«	'Óh\x000ecÐ\x00043ÆÕ4nöâ¤
ðVÛô76\x001aäbS¤Î¹4¾¦ñ³×Æ\x0001çµcºqÛ\x0015ªÀ¦	gòÚ&Ì¦I¦ÌòÁ1ç¢V|¿O[m0Iç\x0010N¬qâl\x001cDîQ¤\x001dÃ\x0019Tµ-ÑLÞj[Rïä?Õl\x00146\x001bÇGGIÈ{
Å\x0010Ä0ÎÚïæi<¨îBUà÷d¦
 o»M4\x0013\x001eu7\x001cÚm[ÜYí·»É+¢3\x0006Ò{ÆQ\x0019'ûí¾lå%@9Ò\x000cçOa{z¼áÙao®^Ü}xûà\x0012¥PjJÃ(wÎ\x0014òÓù{Æ?¾zqsûdT¢\x0014Î_\x001fÃöú8\x0017Ä\x001a\x0017¤[9\x0002J°2-£§ô´\x0003k\x000e¿ `¤ÃPtS­ô1R.v\x000e©AÌtty×"¯íI'óúÞtªvsØÃÎ_\x0010ô,Íã¬¹.:ñu±ó\x001c¼\x001bÃÕ\x0018nþr8\x0012\x0015º´Ì¨ôtévsøÃÏ_t(¸)Ëå¡Y|D4Q]
\x0004æ\x001a$L7XÔmmY9Ô;­%\x0010TÒµ\x001d) ±\x0006óWÄF\x0001IÇâÚ±¼fù\x001d^urû{Aª\x0017Õ_Tg\x0011\x001at\x000fl²ÏzZb²:\x0013\x0014v´N}W÷úÚäNLþÈj)Ø\x0012^o7IãÕõt·N\x0001ï5f\x0012o°\x0008QZIyßi ÛMÒøu½À±\x0007sZäØYSLFEyÝ)SÛ
Òøu=Ý±Û\x0014Ê±Cô¶Ì\x0001//ÄÞw´êv4]Ï÷ì\x0011\x0008'yL\x001c¡+ñ¶DÚMÒøv=Ý¹[\x0005JFBy§Eâ\x0006¢\x0015pÏlãI\x001aï®ç»÷hJ¿§º5éì7\x001cÆwê¯ws4Î]/ðîÎX\x000fe&.Z©©
ª3ën7IãÝõ|÷\x001eýV-ðIÈCôa|GÑq/\x00074Î\x001d¦;wBDëâ£Ëé|^ÖÅÑøvîÛíÖÃëA7Àqc±Z±£8¿¤½±Ï¿²+ª<Ø@RôN^~\x0003I·w^´Éæ4®\x001d¦»vKUÛÀAJp¶s@Îz'k·\x001b¤qí0ßµk­¥F¾e\x000e£e<UînÆµÃt×n\x0015Ý¨doiênØVdñ¤£Á·¤qí0ßµ§\x0000.¹\x001b	¥Qòq7À|ÀNµênÆ³ÃtÏnaS·Ù8b)»µQöVì=@î\x0006i\;Ìwíô\x0019\x001còÖ2NîVÁLº[AãÙaºg·\x0010hBÅtð¹;Y`ö\x0011:\x001a]{I°ñí8ß·[[Â\x0007j´Í+:\x00113=éÐÝ$wÇùÞ\x001dÉpå|<
/\cÄ)F3)\x0002ÆÆ»ã|ï®½èZ\x0005\x00032\Ê+I°ÆÝ mB~¾w7jKæ%Ñ"ôè½dNc§yc7HãÝqwOv7OÃHK²
¢ÜL0?,\x0004§çØ-l;ÎwîT_õ§£¢\x0007Fn4Óü­:o»9\x001aó=âogµ\x001aó]"Ø­Ük#IÇ8ly¢'¹)$¦ñ$f¾'\x0001\x00032é8x¤¼ÄK3fIñ
_à\x0013Ñ±XÞ]Ü\x0001X"ÇY»\x000bl{s·\x000b®î>ðÕyä\x001b¯7ê\x0014ÌÏÉÓ®\x00065çÛû/óßá¢\x000cöÉ\x0008Nm\x0019á}g
ÎþT]UuwÓal<eëBl/c¢|oÈçùßg+ó¿ç¯©ítçFòô¿))»Y·_Ý®ÌV\x001c=}e¼HÏøX,2	XÈôn`~:ùiþÊ(.ZK0¦$á¼ëh"\x001fùù\x000cæç\x0015\x000fñ¾ú´Ë$,Ö8éõÄ5uëùÝ~2=÷å9Ì÷ÉJó¸ìä]d©Îpéýùs\x001eð+x Ùg%nÓIsÊ lÒó\x0016Øª\x000b'gÁ~ó6×1°ç4rDªéb+0+W¡«±ùà¼p{}'+ B\x001faÖ\x000b*Ø3+`§[\x0001«¢ÍuaÓ\x001câ)O\x0001Õ´( Ùe)
½Ë\x000cõmó|&Oá³\x0013Ç)OD.Î)ÉA×Â d -\x0007'ÅhÎQàK2\x001a¹ÊøIÂéÈüåìÈüeþÊ\x0018ê%ø\x000cN¯©âõ\x00030?ÁÌßf)ØT\x0012ÒVh\x0015lÞ8³ý%ç®\x0006\x0017x\x001aCÁqe¡\x0013yq%³I/=4\x001d­4)\x001fþ"
X\x0002Eÿ*ùþ\x0013\x00088ßQÚÛ\x0005_Àà
\x001akÀ²\x001ar\x0000ÂµæRâ"¤ÖÓÙ½\x0010&Ú³ÂîhÂîW·ÿïo?~º{÷éÁ,Ôm\x001f\x000c+	¦psjÅ(Ñ¾7<{yuûøå¯n½\x001aêPÚ³"ï\x0004\x0005ÿ PXCá2¨\x0014xòr\x0015¹Ý£4Ojâ=\x0011A\x0003õÓÝÏw\x001f?}èC\x001aÊ,J×PÍ+Q ÄÄm3¸&.­ì2&\x000frCPV28\x001e$Ö´¹¯\x0000c\x001f«©Ü:ª@m¹\x0003YSõFåå}Vëû
öQùÊ¯¤r2¾ÇÊü\x0001ôEZï¾\x0017Î}P¡
ÿ æ/ÖPq\x0019\x0014Ç²j,\x0006ÖJN+\x0015D\\x000cï{fÛEUÕûUëÖ*EF¼TR,à1\x0014É4ußsÂ>ª6¨X\x0018U\x0014< ]\x001e\x001a°äæ}=\x0018û¨¨B/\x000b+b:L\x0015%bàqÉÞ(UôWf\x001a\x000bÝ\x0015zU\áÒ¦àyõ>\x0006#³,¹P¡#-q\x0010«	,ô²È"ª(*~Á]GÇk%á
÷¥éöQ5¡^\x0016[D\x001fO¢&^¬ b/vS­`\x0013[èeÁE´p-jSJFa¤Ûái\x0018ËTª&¶ÐËè4·zò^¼V+:öä\x000eR5Á^\x0016]D4²V\x000fØ\x0008\x001a\x001e\x0014¨S1Õ¶7Ñ^\x0016^Ä,v°a\x0019ÑFOX\¡ #éÎÃ&¼eáE¤na^­\x0014ß:Æ ós¹ZÐÞï\x0017zâHåY>Ìq÷\x0004Y÷"\x001ffg^\x001c¡ñY°ÐgÉd\x0004ïÓ\x0015?«îQäî\x0019Kß×Û½\x000f«±î°îê\x0018]}ò)Z?Q¥Rv*Uc\x0007aÝ-+xNÏzoI×*¸¬,¢CÀ·,l\x000c\x0006®» ºì³GÖ÷(*í:(7Ó``c0p]F0\x0005¹y`wÎs±§"SÁzÑÇÆ`àºô
jòÔZ\x001d·`º¥Ì\x000c0@Ue)ÙkÝýcd0Ì?µÙÎOËÒMZ
U6\x0019?Ô äî}oß\x000bv×ý,Xû\x0000·eÝwwÿÌû=%÷;óiçpq%\ð¬À´³ðÖ
ZR5x_\x001dØÞ\x001dùc»#\¶jÒ¾
`÷L\x001dÛÌu_;Ñe\ÊÉ0){\x0000óùJÇ«\x001fî>|¼¢ûÃC+ê\x0013*ÝV²D£#E6A\x001a\x000cúöõö-7·/ó·Ü\x000b\x00045\x0010¬\x0001J§{ Sä~í¸	/Èv\x001dFÓ;ö\x0002a
k´åN\x0010OR!Üz\x000b§iÆ±s-9\x0004dj ³\x0006È\x001anQ¦ÈË#úò5eß\x000bdk »\x0002ÈD\x000fÜââc\x0003¹¥
Ê(+-;
èÙBX´ç4·{û´Ï®=ð\x0004«pìÜ®¾Fôõ\x0004ÆÁö\x0004-:B`¯Qü\x00112
ªÝÞ±ã8ª\x0011ÔÎg¨\x00087OJ\x001eÈ1T2â¬ä¤¥ÕM§¥{ Sú½´nÜÐÏo~ú%{Ø÷?~|3A	IdB\x00038ÉØ:(oÜvè^¼~üèûìd¿~ùòñp\x0018+¶\x000eÐ`!\x001a	¤äP6Yn=kâ$"B7Ò¤<5\x001a®D\x000bR¸\x0004¤Ä%å~")Ö)-?\x000efj0³\x0010\x000c\x0014Úä5³ÀØzJq\x0002åh&£Ù\x001aÍþC4_£ù«&/\x0001¨Îóª­OÑúÐuí@Ó.Õ¹ FäOMLß½ùðáÿ<ÈE%"£ \x001dKP	7_\x0015!v\x001aQèO¯&ï\x001eßÞþ¯ûA°\x0006Áé \x001a6s]6""n¼ã$\x0018Dæ5G§Ä!L
aæC¤\x0000¥RSÔÀóéýJ¬þÑÙµ\x001a¶\x0006±óA´¿FÇ6\x0000hm ZZ³\x001eë§¸\x001aÄ-8\x001f³ËÔ_v­Ï~^­Án\x0010_ø\x0005+r:èÆ^óÎRÒ=Hú®t\x0017G¨9Â\x0005q²³tÖ´ R3\x000f¾óâ´\x001b$Ö q\x0001H¶\x0014ªÉ\x0011	òÈ\x0004H{{\x0006HU\x0018þ!¢ð>sk)/ÓI"#$ÚÒù\x000cÀ­UÕ\x0011^\x00002³F\x0007é£ùB2\x0018÷²¤ñêz¾[÷ù\x000139r©fK~D|¡\x001d<Üg´Ìïf¸äFú{²]ôRÔæD©Ü¡ÄßÜ=\x001cÂR¤\x0015ø\x0004\x0016´ô\x001a­\x0004Z=±\x0012\x000e\x001d¿¹¹\x0000j\x0002M`DIB[KÊ`¤\x0010L'ó¾\x000f\x0001k\x0004à\x0013å\x001bmýµc\x0004+\x001d0L~1©\x0011Ì\\x0004\x0012§ÖTO1/×ý \x0011ývm:uû\x0010l`'¯\x0002¢H S¬g\x001dy-\x0003hR¬®\x0007c/Fp5\x0000æ:²Ï+yæ\x0014õ\x0006ÔÓÅixÉ½\x0010Á×\x0008~2áÁ\x001fAc}\x0004êD0}}1A¨	Âì}¤E¬C£?í£\x0012ÃhìÅ\x0008±F\x0011¬\x0013\x0005«ä\x000bX<Á÷
bx8Â)\x0004Ü\x001c½\x000c\x000f¼\x000ejç#ï$é.áàÂ\x0019Zç<Ù;{g¤­KC¤üÕÆP¤R@»	§A7îYOöÏ´øíKSz·¸65\x001aëu1Aãõl÷ì"%Õ2¥{Þ2x\x00014Î`hÜ³ì}©¡\x000e2jwäpz25û\x0010\x001a÷¬gûgodÐ
m$î1\x0003j-cÑÐ®\x0019\x001aÿ¬g;è´¢,\x0003\x0014\x0006,\x001a§j/dh\x001c´í¡IyÎ­\x0004|\x001c\|6\x0011ù34.ZÏöÑÞI\x0002M+/]PDÛ4Ý®\x001fÎÐøh=ÙIÿ6!74N\x001af;é Iú#¯\x0003^ËVe\x0019:Å¿û\x0010ÚëçdÿF?gJ\x0006\x0005X=[û\x0019>\x001a\x001aï\x0000³oo \x00057\x0006*8nµVÒ8¤ÝhÌëÅ\x000ciÉ¦5 BßÚÅ-×N\x0006©\x000eèL\x0010Ûy¤j|¬«r9§"ZjaSÁ­P¡¥c1ã"z\x0012ËWÑ&_hhZÈ× ZêÕèîÜSçë\x0001núzPËì,uÚYQêNÌhhøåI²/H¦8ª»åeMÉ¡\x0000^\x001fè\x0003ÉÕú\x001c#Ì?\x001f4PH\x0002rÇ\x0003¼.\x0014pIÒrL\x0001þôæC»\x0018ô©âY6X§t¸×ÚJ\x001cechçÚÔqúA%~ó§7wï®~xÿù×·ï\x001eJA£,X¥C2~Ò¨ Ç\x001cÇjqz|óìêç¯>y6Jì»ó²\x0003WÉÞLÄ!½8ËAUúc©¥R7\x0017:Þü\x0008\x000eÖ8¸fuÌ²Ö(ÂdFW0jócj\x001c³\x0006Gq¥³éôpÙ©Q^ºÑýXµ\x0017­qì\x001a\x001cK±V\x000e»"\x0017V¤Õ1âXÜ¸÷m\x0017«qÜ³\x0013"¹ùmuÀ\x000b\x000eªm\x001c\x000b ì¢ñ5_³8®Ä\x00189ë\x0016GFÛh\x001cwðíÂ	5NX£XÅôIÏb©ô¸Ù|\x0017K¬Yâ¥\\x0007ìcÔì9ÓÒH\x0018£âXÜw\x000fN]§àj\x0001©k£x@¢'1|µÑJíy\x0018\x000f\x0007ßÅÓ\x0004bÀ:O¥²2ºG\x0017Kà;ïGx@/

\x0002E\x0002¹ûßÉ\x0000ªóÚu
àð4A^\x0013\x0015¤K¥æöx/S,1\x0006Ðc\x0001ö]8MP D\x0005*:¾izêO2àN	\x000f»&wñ4Q^\x0014\x0016héóßþÄ\x0001u¾üëpÚ.Æê%~´±\x0015wÂ\x001b-\x0003Ðs£½ïtm\x001cái|^â|(ÊÉ!µ·Ô\x0002ÏS2\x0002?CPÙõÅÎg|y¶ÉqB`=0<÷¶\x001eÏ0(\x000fCc\x001dæ}¶­¾U³}£,@\x0002{\x001d¸Ë\x0019ê©ÞÀh\x001f+2ß¿JÉµ
QPÊ9Í7W¿Þ]½úðö§÷?¾y0\x0005éï\x000c!]±Åé2õ§3Sõ6«ä>½¹zuûäÑó×/\x001f\x000f\x0016\x0018\x0007j\x001cX\x000cBÞ¢¶ÒRì(;K4¨Í(í±\x0006k\x001a\BAzÒh¦2²\x001b#""cj\x001c³\x0002\x0007´â¨X7k@ÆGÂ(¾\x0013ÇÖ8vÉêXfÊYÍ\x0005\x0014ÎXÌvôÎ·\x0013ÇÕ8nÉêº\x001cÒÀMªÖj\x0019áÂ¼Õñ5_cØ\x001cçÕiD|äkse\x0006£\x0019¼:í¤	5MXst¢Xl³¼yòª|nL»i8±ÆK\x0016Z\x001a²×!Ä¬üè¬À v´\x0004\x000fÐîØ\x000fUkV\x0007Yt4DÍ«e\x0008`ºdOãic%A\x0001\x0019jäÝFµ=(:)pÓ,n\x0002½&*HÛ-Õz»9È±Gè ÕÎLãiÂ\x0002½$.\x0000\x0015å*\x0006\x001ad·\x001bDÙnI
Gp\x001a?ª×8Ò\x0018SÔdËy»DmjX@¶§ñ<zë!Õ9ÏÛ-òC\x000eB9»¤+0G«3ó¶Ä¾ýQu3\x001f$_{Ê\x0013ïäðMQ²:G\x0008ú\x0014\;9EØ\x0019Þr(¸>§2«¨~Ã¥s(X\x0005\x0015%\x001dH§Ò\x000b¬ê\x000c
:to8²« ¬§\x001aÍ\x001cÒ\x0019íj\x0018È_N5Î"4õ\x0006yJ½ÁT$JZ\x001e!LÞË>%\x0013.?R_ i å\x0003\x001a¼#?Ø\x0012#ï?\x0012ïÞ¿ût÷öÝ%4éoñ§w»{·Ñ{\x0005éÊÍZ¼1-\x000b\x000b ¶\»\x0016±Cðüõ+aøîù³W7O}}³5\x0018PcÀL@u§\x001bFäéÚ(¯hMO\x001då\x0010\x0004Ö\x00108\x0011B96Ð	B¡Éqö0:nô\x0010©1ÌÌµP¬ \x0011\x0013\x0006\x0017±$4á1\x000c[cØ«¬K0\x0014§\x0007Pd^Ps\x0008ÃÕ\x0018n\x001eIÇ!\x000f K7
\x0003¢Û'|Â×\x0014~.a
*\x0011.\x0014V\x0016£3ä\x0018F¨1ÂL\x000cÃ+\x0001¼X)Û\x0019\x0016s!Ö\x000cq&\x0003ðö´\x0014ÛàÁªÅ	câÚ\x0019'¿§&bÐè\x001eÆHw0\x001d3ÆÉg¸Î;ç1ÖOtàÉ¬ryÀ¶«\x0002ï*\x001dN»ª\x0013U\x001dâh\x001c¸èÁcAÛèHó5o+%*Äh}§¸î«\x001cÃ`J7\x000e\OôàÆ\x0001'üÓb\x0004V(B\x0015NG¼\x0017\x000f\x001eZÆë.Ü8Å5\x001aép\x0018.jH\x001cN\x0016ÃMÝT\x000b×\x0013}¸±çÃ¥õ\x00109Ä¡ÄmØN-Ð1ÆëNÜêk]lU~EåK`èf:qÝ8q=Ó',àµÙªQ<Gïuï\x0010FãÄõL/n#È¤å°§Óaëè	ª\x001dâh\x001c¹éÉ1\x0014k¥6¥¢?ÅOÜVÐ¸@é\x0002éò\x0017y[8\x0010å\x000eëfÞ ½ÃÎt¨Kd\x0005ªp%$Ñ8Aé\x0004µÉCÎ\x0012\x0005r=)*\x0019\x0000(p¢ïÆ\x0007ÂL\x001fH\x001f£ìªXN9N¼r@ã\x0003a¦\x000fÌ#Ù2GÈ]¡¬\x0011Þ+÷!Æ\x0005ÂL\x0017N¶¸rð\Öãä\x0003{¡8\x001a\x001f\x00083} Âb¬R\x001b9$ÑÅyôj(\x000ea4>\x0010fúÀtÈy5\x0010¸©2\x001dr/&×÷Zï\x000fa4.\x0010&º@uM¢3G\x0017¢R¦ptªw\x000fq`sÅ·Y
<¤+­á"ñ´\x001e\x0016Ë®¸\x001eØ¸rèÊ1*V\x0007Úð·[9ÄXöUT\x0013.6®\x001cgºòò`ÖÃóhZ\x000f]NyOyé\x0010GèË18*2Þ8hÒçõ(Ï\x0003±×ãz£qæ8Ó+à\x0002tÎíÉêÊñ\x0008=\x0015©C\x0018/Ç¾\x001c]deÔt<<WàAôZRë±§z£qæ8ÑcÀ\x000eºl«ÀSc0]Ög®GãÌq¢3G\x001f¸Á5Ò`:Y\x000fsAªü3ÍUãÍq¢7Ç\x0010yàR:æT²ò1z!G\x000eq\x001eGãÎq¦;w¶¬GD\x001eeFÕ[²¯ ÓfxÃ4îÜLtçè¤¾.mé4N\x001c)qff¦Ä4nÐLt\x00082' nS6y_iËù7¯z#\x0010\x000eq´/\x0013ÝGK®}æ \x0005N\x0010¼\x0005\x0006"?Ã6ûÊNÜW$¡¸åuR\x0001XÒ\x0012	f8s9l³­ìÄm¥)º2\x001b\x0006õØärMH=\x001f\x000f³E¨\x0013\x0016¸B¦*\Ø*d¦Å¼®¤}(çXQY¹¡ÛÞ\x0008Ý/\x001fJseÌ)+c¦ùCÅêÚºíÏ»pzæ¡­»*4Ë3J((\,Hö\\x000c$øÅþÂ¹\x001bîê£ÆtêO\x0019¹\x0012mí8õ_­¼ú\x0011¡U­ø&ýjJrÿ\x00191¼úåíw?]ðý£+ca\x001b\x0011´uCka!õ\x0017."K¶úë0¹ýh^}ÿä×¯\x0006q:þ¹mF£\x001c|\x0011ØzõößÞÿúö Ö;àPÞ\x0007Åo!$!)-u£a&ß¾¾zõä?}r?\x0003Ô\x000c0!]Ñy<½R4Ê8«¢\x0011\x00065\x0001k\x0006ÍâÄ;j=MÖbu^g\x0004Bg»]
aj\x00083}3mbA¹	]]{ÙM2t9ê±Úö¥\x0010¶°!\x0002¸ëÈ\x0010ÔæÌs=d\x001fJ=_
ák\x0008?\x001bÂ\x0006iÐöT¹Ë\x0010¦kíÂyB\x001a"L?\x0013k1<éZÌ³²Ô¨]érXCÄÙ+(º&Ûvâa»¢\x00074k;UíVä%ÔôCÁÝäTV\x001dyVÜAªÇ\x0005ÆC´®n¶¯\x000bNºß<	|æIx\x0002[q\x0014Cm¶K!\x001a_§g;;Ò-ÄÓ¡@ÏÂ!C1û»¢ñvz¶»[·\x00149zuªNò\x0003
^üz÷S\x000eeÿç?þóñ_~}{QíýW*/¬ä\x0013Ò*H±òQÒÑ\x0000_Ï¼xzó(²WÿøôÉËÇW÷3@Í\x0000ó\x0018Ü§ªT8-5IØÉá\x001eaÀ\x0001§®\x001aP[
yÊÓ¸é<b\x001eA05àJã\x0003!(~1;\x0011L\x0003p5\x0007à7-Õ«JÉ\x0006¯G­6Ñl·Ñóö¨v&\x000cÇr6i#âÕN©È1»ân\x001eEäoëÛ(UUßÆ¼ã\x0000-\x0006LÄ0ÛtøÜ
¤äP»ò\x0014\x000eòôc\x0014?¶\x0014ó¶Qôl]ÄiK¹r²;¥\x0017RlYá ìöTö?<ùëßî>~|³£}t7c\x001c-ÕQ)ÝÉ_kãD\x0011Ew:üðâæåËÇÛ ÚG7÷\x000c¢\x0015\x001e¨y`
\x000fD¾n'\x001e\x0019FëuüîLD<Ä5\x000f.áÙËäa3
":ª;]\x0004xLÍcÖðÐ\x0019Æq\GâU\x0014Å©8¶Æ±kp0]ÇEÜ2,´rEm\u\x0014x\x000e\x0001¹\x001aÈ-\x0002:
\x0017 °\x0005\x0019Hàuo^È! _\x0003ù5@é§2¥\x0015\x0002.\x0005Øúºÿ ò£\x0013-B¨Â\x0012 k"ßØ\x001beÁÁ(5Õ \x001cL\XãÄ5ë£\x0002KûHiìR¬)*Ñ\x001d¥#<ºu¨k<ª¥±¯e¯ùø([4¯;5Öp\x001aÿ£×8 ë¤óÙGzRÈºO1ÅV4èb\x001aQc²õ\x001amS\x001ckµ|4/ùé\x0008Éwe;G Ùr°.Ó¾¬\x000f\x001cÄái¾\x001eZ¨3jA\P30bsCô\x0015P¸
WÍ\x001b¯)J`ªbç
½k´9åä\x0007ÕSÜ\x001f?Ü½ûùê»»Ï?¾ÿüá/\x000fÏ\x0018r§Â0¶\x0012+ñ8±?ÞÞ<ûöê»×ß<}ûÇû fEL\x0014og\x0019ù\x0000$ú\x0002\x0012o\x0011ä#¥®ýPXCáªÒ§%ùm{{(CAU¯5ã\x0018©¡Ì2(Í
ÉÛ¤SvM\x0010Ìa\x00013Lõï²5]\x0005îxGf@\x0019}\x001a-3UÛäj$·\x000cIñ;@H¦õË=x(ÇâöBù\x001aÊ¯2\x0013)ôv2ëXºk<8,³:e\x0015\x0007¡B
\x0015A)jâx&âWqWæµØN²á T¬¡â*¨ ÉÆ@RÆO
r¦püÀ¼\x0013ªØ@W-£R"(©½\x0014 {0eðQWá\x0018U\x001bO¬
(hâ°gª\x0010®\x0001¥,C6 3On"
½,¤ ±«\x0019*\x001a.«§®ú\x0000È1¨&¢Ð«B\x0014³hQäñ\x001c\x000b7¤Ði<u/T\x0013QèU!7À¹ð\x0004lE^)ò\x001cû\x0007öB5\x0011^\x0015R¤!\x0014)]¯­\x0011S\x0011üTSÑ\x0004\x0015zUTáóDòÊÄëà$NgSÐ\x0019*tª*ôª°"Ù7N¿\x00064´üzaPF®ûq!Ñ^ª&¬ÐËâ
UF­à VÛàÅXqî¤Æ\x0005Ã2\x0017¬dðK et\x0019gim±\x0016½ÚícTíõw³RÈmã!ýNk%
ÐKS\x001c¤j\x000c;¬2ì\x0006+:¶X¨.6°§±pª±°Ê\x0006ºàJ¸¬EªªXÌÍÁ\x0004L3\x0012ÆÍ[:]°×ò<öVj¥iFúÜÛý9]ÇæcÐ¨2`ÙkÉÆÀÜ[¾>GÓ\x000b
\x001bZÒ²m½¹þR®iÙæÞK¾`[\x0008ç)ß	lñ#)xç\x0014®Òbñ§îIP_7µ\x0010N\x0019P\x0006]9é{\x001aÎù9\x0010z|±ra%gmÒ\x0014\x0013¸j=5¬j\x001f\x0015rnmÝKþL\x000c¥µâ\x0004À{±&f¤ÿ\x0005[g(X1%õ\x0008­ÍT©çß0Ù»%GVn2Æ\x0011}8Âp^\x0014è¹äÑ/\x001bÐ£_î¶¯y¨¦º*IkXIAi-s £ÅúèûäÑ÷7¯\x001eß¼\x001e=Íór¤@\x000f$³)PÐ=20<tjX÷R`Mó)Ê83M\x00139fÒpºaÍÁ05Y²\x0018r©\x0007EÝ¬F§.}/­1ìt\x000c\x0017¨É=G°(=\x0002ZyÁ >Å\x0019\x0018®Æp¿×£ák
?ÂSòÁÑè\ËV\x0012Ef÷½\x0014±¦¿Ûµh\x000b\x0007h=è\x0007sa¬7¬£\x0010ÀÊ
ÏÅ¨Ä	öô9.¦±gõ\x0002BQ\x001eø|õíßÿûoÿ¿\x000foC¶±´!Àú¶·÷¥ú!\x000e{ö__}ûøÅóA\x000f²@
\x0002óALÐòð'XX§eiÛëjÚ	5\x0008.X\x0011\x0013JM
JòÜâ\x0014(³ô\x0000¨\x0010)\x0017\x001aÄü·­Aìï\x0018Ä× ~Á\x0019I1Vä\x001aïüÇíÈ\x0010iÐ÷HO^\x000c\x0012j°\x0000&sä`\x0011)RÙ¢,kKÍE\x0002/æ5G\À>^\x0016$økÖPòª }ïYu\x001fÇéí{ó"j>\x0008¦¯gëKÒn\x0017D±è}ZÞÐÎ$­?\à\x0010
½r\x0012
îÌ[«< öÊP/&9\x0010­N\x0013¢o~ýH½COßøp¡FÊf\ç'\x0003\x0010­HépCIF ÿ\x0010róô%õ\x0011=}~{Û\x0015\x0017jx æ5<Á²8hðFKA­\x0006æñn0Ju7\x000fÖ<¸ÇHè¨\x0003\x0017Ø\x0008(ãÑ`Ý
dj ³f| \x0017ßmáùêZ\x00076\x0003>öÆ\x0014\x001c\x0001²5]\x0002ä¿é½\x0008\øþ\x000ce\x0018ñ`ðõn W\x0003¹E+äy j \x0002,¼B2]9ô\x001a£\x000e\x0001ù\x001aÈ¯Y¡´å\x0018(ZO§Û
¹2\x000c²×§r\x0008(Ô@aÍ
¥øße Â|ÛO1\-\x0003\x000eÄö\x0002UA5cyús[ÍVA³\x0000}ÚsÜ¬Â c¼¨ñCz#Âò\x0018\x001f °¬¥+½¹\x0010ÌD;§\x001bÃ­\x0017YnPR^\x001f´çºt÷XÁõ&\x000f\x001e!j\x000c^céHû'K;àm­]Ú\x001e¼éBè)]\x001e\x0001j\x000c^cé¢Ay\x0008¤èÇpô\x0013£.áÏå¡óìÂ8Ókì\x001c=ýqCx$eñ|ù[Gpv­½é\x0007\x0016\x0008\x001a;\x0007kì\x001c¹"~\x0018Kq\x000e\x0019ì¼\x0004\x000b~â\x00196Þ^cçÜINÂC¾\x000c düºîÍ2;d\x0015Ìm¶\x000cò<;\x001d\x000cÅÜE#Â`é\ÈÛ\x000e4µö;Ù/ÀÔ*°`\x0014O0OÑC`-G}È\x0012=\x000cf\x0013ï÷µ_Á*°\x0018¼\x000fzêÏW\x000b°r/÷nPWºËú©/öá²m\x0018I\x0006?û(º\x000br¬Gu\x000ce\x0007rû Ì9Y¶\x0005Ë Ç\x0014îI¥bº¥.½téåPö4LZ~Pº)ß|¼úöýçÐ1Nµ{ÜÊq*¼A{jå\x0018Mdyõíó×ÿ<ìÜµ§YÒ\x0002¦S\x0004]úl¼\x0012!G
R°\x0007£\x001aß\x001d\x0014XSà| eåÚH´j,UPvTV¾\x0003ÃÔ\x0018f:\x0006%GOEARq"úë0\x0012­Û\x0001ak\x0008»bGYÀkf>}ÀÞûÔN\x0008WC¸ù+aY6-è2H%­ÀôN\x000c_cøé\x0018ÉÂJ		$7Ëfliâ\x001c\x0015PïÀ\x00085F¿\x001a YwM]6RJÒÛA\x001dà\x000eXSÄ\x0015§Û¸B¡¥ø§´4Â¨Tórú=Çz\x0019çqXWÎ\x0006ë¢${
F\x0002¡;0Z÷=ß'\x000cèÒ$Î#u3Ò´¨GUø;0\x001aÿ­ç;p«Ï dSÞU*8Cto\x0004×NÆëù.Ü Ôúju*còEñ©7k'FãÁõ|\x0017nDv'-ÇIçI¢Û®ðÛ^ÆëùN\x001c¼É>QÍb«*«Ñ}{ÞÉÑ¸q=ßc,»JkÒ]Ï»JzCAõfÿîähü¸ïÈu(ëAO\x001a|:ôMRµÉ\x000cÆëùh²ëP¥©ÒrÈGâ\x001f;8\x001aO®§»r,-\x0017ø)+Ã]DyøÓÝ±)û8 qå0Ýt(«ì`\x0013KPÅ²\x001c¶Wñ³\x0013£qå0ß§½$ê¡Î¿\x0002_*F\x0013:vp´wñé¾ÜëÛzä$V,\x001dfi9¦8\x000fh\9Lwå¤\x000eÌáz:Ú\léq±cÊ)ÆÃt_néh±\x001c\x000eýäåh|9L÷å6ê±<
--\x0016ce{ÕW;9\x001a_\x000eÓ}ùoft\x001b_\x000eÓ}¹
¥¯HÑtSv%· -Ì9\x001e3éÎÜBÚ
å/Pi=°«Þï\x001c3ùÎÜ\x0017M
EBí½ º&NÙVØørïËu,Û*Y]Y\x000ePe[:ïvp4Î\x001c§;sj0¼\x001aÀ
!.hË)BÑ&¤çû@¯®£g\x000c}Â°²\x001afNÄóÀùÎÃyiõ"\x000e	\x0011Ô²è®Ä\x000eÆæâ|kOzìvK&rhU|Go$èNÆVá|[e¼hwZ\x0011/qÑZSlÕ\x0014\x000cÓq3ÿSj¤xr\x001bÙT']hä!8SRZº'&K´ÉWÒÑEÔM\x000fê¨w%à¾Á\x00050¿UÕ*	pºáwÂèöâêÌÏwï?¸º£ÆÂÏÿß\x0003YÉ3Ë·§óôGÜ\x0010"ÇÆÇ±\x001cÎwÏ_ß^ÝPwáëÿç~ S\x00035@¾(WR3BÖ8K@<
\x0011C}@®\x0006rkaÅ^ÒOÍóï\x0001©Î±¾ã> P\x00035@\x0006Éçç!\x001eßb\x001b(õB½Í{xÒÍç¬^Fµ\x0017G¿Þ}þ÷÷\x000foÊUV\x00147T×¾Y\x0002%Ú¯é>\x0014þzôôæõ¿<\x001f5å2\x0006Ô\x00180\x001f£B§\x001b7OÆH\x0018ÅwÂØ\x0008\5\x0006ÎÆ0\x0011x
jÂ\x0000*\x0018 \x0010|Á\x0018TCîÁ05ax|vÂ°üN0bY¡×Å\x0014¶¦°Ó)ÒÇ:Ç\x0014Jü\x0000¢É­õXAób\x000cWc¸é\x0018ÚóD|ÂsºÒ\x00016íû\x001aÃÏÇ0'C\x0015¥BÎ\x0007©\x0002Ò£¾¯=\x0018±Æ¿ßÕh\x0002ÉmE*Ù¦Yf7nïË\x0011É\x0013£Ò¥ä´õèÊr¢éT,Í=GÁ\x0005(&"O#\x000cÉùQIJ¶Yå¾c½ð1vgÎ<ý@ù÷ïúåÁ\x0005¤4Ø»kLPRí­4\x0013[\x001cLEøþù£ï\x0007ËòñP<Ìüø\x0018å\x0001ÔPÚ1G¼ÞyùöA%Óßõ·ãÄo§8nG·Úp©hú³¤¬ë¨þìøxS¼ùñvÂ·ýâ£TÂÙR|eGKwM£\x001f·í\x001c9½s\x0018rEÞùûÊ¬/âÉ\x0016ohÎNm²\x0010éÔ¦/Kÿ­«\x0017oß|øðæêå¿Þ}øùÁ\x0018
©@Ã Y-|\x0006¼¼:\x001bÊõ~#ýõYByñäñííã«¸¹ýö~$¨`\x0011qÓÁh©úI+#&ÕøNéî1$S#EH cR\x0013Ré>÷Q4¾ïD!ÇldW­R ÖÅ
	ü	I\x0005Ùxöëï\x0018«Ü"$teÒ5*r³6BÔQÈ<Fäk"¿(3òéDäRôË
\x001b1RKðD¤P#EDãÜeß9Ñl
XRè4Y\x001cC5R\Dd
¼ï¤zv®
¯¦³[Rè©Ë2âÊ)¾b\x001e:\x001d´ÇZW»Ê×ZËc-\x0013\x0015qª´õDy'v\x0006\x001e\x001dcj|­^ålÛuÂ	W1¹â0ðlu³e:EÜÇøA¯
 ~Ûej\x0002\x0008½*\x0008N²)@ºV\x001bå8ÙNWÐ1¤&Ð«"\x0008ãEÃ\x0006dø\x0003È _£;\x00126Ç\x0008B/
!\\x001ek/Ùª¬R:JÛ\x001b1x©	!ôª\x0018"¢Ø\x001b×\x001cçIö)ÝÁ¿g>FÔD\x0010zU\x0008\x0011·1¾y,Ëu%$i²·Ði\x0004>Ä\x0004M\x0008\x0001«BXz\x000cÄqX\x0014¤ÌÎ\x000cÇ¡ `U\x0004AB)|TÎhä\x001cfÆ®Ð^Ö\x0017\x0005\x0010^\x001b\x0012åà\x0017E\x0014ÊâDó\x0000Mü\x0000â\x0007¯Ê`Aö`d\x0017EDÉÎ´ÎcLM\x0000\x0001\x0002\x0008¯Hôè¹ÎFU:RÇø\x0001\x0016Å\x000f^\x0015
\x0018«­xTFÌ¸ëTþ\x001eCjâ\x0007X\x0014?x\x0008¢;Î
OW±\x0011ä&H
K\x0013\x0000\x0002Vå hçå0Ï\x0014=V;ÏOEjâ\x0007X\x0014?&Ê\x0019Jjk`\x0001ìhäac'ÿ}© `Q\x0004á\x0001XÀÔb1ã\x0011tÙy\x0013³yØÄ\x000f¸(~ð4\x00131<ëBdi£u¼HNÏL#c\x0013?à¢øÁ£.¯FÔqÍö\x0001¥ÆÇÔ\x0004\x0010¸* \x0013ÄÉrì<§§n½&ÀU\x0011\x0004¦{ l=Ç]BÉ@HrÜéN§ì1¦&ÀU\x0011DÁyj¨¨bcò(L83\x001eÇ&ÀU!Dº¤gÑµ´÷ìiDéÊõju151\x0004®!<È¾K¬a¦ \x001dQÎtÊ&151\x0004®!¬.6"xºéf[.\x000fÎ\x000ef:\l\x0008\\x0015D¤\x000b \x000b%sPÖ©\íh^\x001dcj\x0008\\x0015Dø²Nô¾\x000e¼N%
álG\x0007ä\x0010iÂ\x0008³*È\x0011=LsÒÊ\x0008ÒÔlr;6/§*é'kÞ3\x0014ç¤²9=¥AyÎùkÎÉÌ?\x0006Æf `~× ¬y\x0007H\x0017DNMà&\x0018ß\x0001äØ\x0019p\x0014í|7âºEK¶CÊ>:¡y)ûè
ß<XPp¶ðyEý%\x001bÒ§Ç\x001b'#Tæf*ü9\x0019øuh'qWî&Á¸«$azM'_Eë\x0014AJíÑ\x0017\ë°@S©p^1K)\Ü"=é\x001cîðc_`i@\x001a\x001dz\x0012Ö\x001fðÜÍ¿¾}·umýóÛ»_ß|útQãVú[üáéÝßîÞ½ÿüñÍ\x001fH¯C!ç]¢¥Ñß\x0018¹À\x0010Ó-¿;\x0004î'Ï¶v­~róôñ«W­\x0002j
I\x00119c\x001eéÆ4\x0013\x0006?Ö U¦c\x0018XcàD\x000cY\x001b&RL\x001fÑÐpß\x001cZÓTy\x0000ÂÔ\x0010f"Dº-å¦øm-"S\x0018e-¾îWaØ\x001aÃNÄÈIy1lÁpV¶T¯}ù\x0018«1ÜDt'Rr2¤)\x001eÕè)-\x001c£ð5H\x0011\x0003s¥Å\x0010=´bàÅ°_7´Ç(BM\x0011&RÐc¬áû)P(¨g\x001eF¬1â<\x000c[*2â¦ãO\x0006\x0018c\x0018c\x001az½­\x0008íäõÔ<@
?&3Î\x0010o¨b¢:¹\x0016B·¾{¢ó&\x001dÙÔD]>Ü`­Øá¼Ç+Ñxn=ÑuÓp\x0013`\x0006]·u\ß3O¶n\x001c·è¹ÓUÿO¶÷Ü&@ÉNØq°Ç\x000bÑ¸m=ÑoS;x~U6¹ð<¨ ý\x001bn<N¢#2{l)\x001a§'z¼t·åß1¹hnÙG¯¹|\x0002M§Ôà\x0018Fã+ôDgÂq:\x001bMr\x0016\x0006\x0018Có2z¦³ædÀÄ\x0011B`9ÐH}ÔyL\x0004:\x0010\x000c»'\x001aßDz¤
\x0007yÐô\x001ck.è\x000fwü´A
ñâ5 =ç(8\x0017ÅÉÜÙhSP"(úäÂÝ×/ä¡lwoñLb²Ë§×_îþú·«ÿç?þóæÝ¹\x001d\x0000üDãCÜîÛ\x000b¯eF³îÔ\x000fHå÷7?¼ \x001f?\x001bNYa$¨`\x0015ö|\x0001ñ4fS¦K9\x000eRt®CH¶F²Btl\x000bR(,N#f\x000cö¸
v\x0017«Ü2$Ïï> îÍd¸ðU'£7ëØäk$¿pra|Z%ÃÏ3´JAV©ÓÀp\x0008)ÔHa%\x0012%\x001dÊYB\x0016Ð\x0011ïéïß\x0014k¤¸Ê<P\x0008\x0004w\x001dúÂ3\x0016ÁØÃS
7 \x000b®\x0001Y®ßÖHó¶³*\x0014¦±"Æ.¦Ö+-sKTqÈL D«D[ÖÐ÷¨GíCj¼^ç\x0015±\x0012/Ö£dFÃ\x000fö2aÃ«HfÑ±\x0011ÜÒé@q/q2âpè\x0010iÌ*&¯X&'1y+\x000cT~ÃLfÉÓMø WÅ\x000f1D¾¢z\x001aÊËãÆÁZÙ{n¤Tº©\x001fôª\x0000"F]LÜy\x0001'®S\x0013@èU\x0011ÄoËÔD\x0010zQ\x0008aÓ?§ø°IøoH5ruìuß\x001eBj"\x0008½,H×
\x0005)Êq*±kTó¢\x0008h¢\x0008X\x0016EÔL(\x0003ï+¦0RÈÞËÔD\x0011°îr»ÍË-\x000b·i\x0019úJÛy{\x000fÚËí²0B|SÓm]8\x001aÈÚì\x0006jb\x0008X\x0016C\x0000pµÚxE]O{ÖH\x001bo4a/S\x0013CÀ²\x0018\x0002\x0002K]ø`~£öQâ¢y÷@h"\x0008X\x0016AØÈD)\x0010]\x0008\x0007:yp÷¨\x0007îbj"\x0008X\x0016Aø\x0014½2çA)ÐCW&n¼&e\x0001vüj\x0002p
|or(^è¼lícÒÐ6eÐ\x001dJÔõo>ÿôþ_\x001fÊáÓÇ³]à÷6úX&H
\x0014Ðo^?zþO÷;4ß\x000eS¿=°¶ãydÎÈ×Ë,0\x001a~Ù×cóõ8óës\x0017ºf0Rc|ëÓß@\x0017~¼i>ÞLþx\x0011µ§Æ Ë4ÁdíË>Þ6\x001fo'<Õ*<Û#}¼\x0005j3Ð:¼ðë]óõnê×K* (R\x0005_}°£9ô}½o¾ÞOýz'"ÿ$MÅMR6î`î\x001f\x001f\x000f?^ÄKýé7\x001feÐ\x0002\x000c\x0012K\x0017~|l>>Nýx+j2Ê${Ã}Æ'qå^!åå_jd ¯7jÕ×\x001bi<}¼\x0019¼]øñ5S¬7ÒÊ¤\x0012_½\x0013ñÞÁD½\x000b?¾ñ²fªMT\x001eÝ­|$Ó?¾\x0017ñ\x0003yÒ\x000b¿¾±7fª½V´ðH\x0019ßUT\x0019ñ\x0002|\þøN1w8{;N?¨Þ_|øû_ýüæê×»«Gÿ¿\x001eÛ±ZÉ=Ç§[\x0012zIÓ\x0007\x0012Ê\x001c/nipÅÕÓ«GÏ_$?ÃÙû1aÁ:,\x0012«Ï)«­}6´\x0002Ê	k*\x0015ÖT¸Ê(yËóTê¡ãÜb\x0018
\x0017Ù\x000fej(³\x000e
\x001dÏoôÔiyð¡áúô\x000f·Ã»ö^,[cÙ;\x0007¥¥òe"\x00178Ùq<c/«©Ü2*R3.çÊI1D4²\x0005GãØ÷cù\x001aË¯ÃJ·¼\x0008Å\8Í"åÅ\x0008åÖ÷R*¬£²ëKýÖÇÍ\x0016\x000cÊ\x001et\x001dÍ«X±Æ\x000b±Dp-aAÁB\x00143è:%ÌÇ°*9ÐÐÔ\x0000Lçünä±Ô\x0007Ñ\x001dX Æ9Ô½Pmx±.¾0º$ðIóÁòxhpa:k/W\x0013_èu\x0001¡\x00066¨¥RÈG+^«§\x0007s«0ôº\x0010Ã õP&åhyD
ÃiÊû¹ C¯2HÆ0F§õR'£á\x000b×h$ã~®&ÊÐëÂMø¯,\x0017\x000f#U¶²\sL<âÙ­\x0012ê»\x000fo~~óáíOW?¼ýøéÃÝ¯\x000f½YÈ
ßÈ©lµ,<Z\x0011Ä\x001aÍÿîöñ·o<ºúáÉËW·7OïG\x001a	Ö 9[Ô'mb,k"
c{
\x0006Ç°FÂE«DÓPXq$Ý!-ËÛä\x0006ýH¦F2VIE¯Þ¢wxácéÕ\x001e<'íG²5]´J41\x0017ÉÑH¡<\x0000æ4Deð\x0016°ÈÕDnÑ"¥(ÂHC}ä^\x001d\x001b´:N~w¦uð5_µïPä\x000fhT-òQò2»ÊÒààyH±Få\x0002[\x001f%/é°#ïuH·^i[r
8ù\x0012¨+Z\x000cq;3\x0008ö#5&\¯²áÑÉÆ#ÛÇïU^ÞÁÙ\x001c÷1¦ÆàéE\x0016Ï9Íí­ÆpCÎ*\x0007ÃÍëàÔ øó_j476ß$Sæ)U´
S\x000e2P¦è¹«u¦&²ÅFËÈ´-±\x0004XiMÅDE\x0002u0dí"²ÜL\x0006§aqòZP$Eçïß}º\x0000æ¦2CSÞsãe i¥
\x0000\x0015\x0017u¡w÷H¤@üù³W÷9Ô_\x000eS¾<\x0006Jwå/·\ÿZ"Sô½G½õ§ãO'\x0011$þ¥d½òïÜqi ûO.ýrS¹ñå\x001c~nÁ\x000fé÷¯sÏ4ËaÐê½\x001fnë\x000f·3><ýRóm3R}\~±´q¸£5`G÷{ï»úËÝÍâ\x0003Í?Ü>Ýx6~ÓÜ\x001a6ÿ/÷õû9¶Eç¸ÃQ¤Ã\x0019´d[¤a5j\x0018ë\úé±þô8Ë,n'ôìÓE¤aÖ§ëÖ¢Ï1égg¦o\x000f\x0012î¥oç&\x0012¾Sõ~é·×sÈå\x0007å¡7'>¼ÿüïÔè|lÃ#ëÙGg¥\x001a<mxÑ4°$tÕÍ\x000cåÐíó×ÿB}Î÷C@
\x0001Ó ,\x0005\x0006¬DäÇA .BD1\x000e¬{\x0019°fÀy\x000b|\x0013°\x000fkv° EfÌã \x0001¾ÁÔ\x000cfâ:8î\x00004hÉ[Y\x0007p=_{\x0008ÂÖ\x0010vÞBl"o\x001b\x0003\x0015\x000b{^"A\x0014F\x001dT{\x0019|Íàç-Dº¦q I\x0017<ò%E\x000e^Ô\x000bâ¨w/D¬!âÄ\x0014N\x0000îeK1gQ{ë\x0008s\x001da8é(mæUM<Ö2p<ºtgác­9ñÖ
UÏ!¾.!\x0004­è!Ò2 ï¥\¸ÊË åP\x000f»×¡ñ\x0010z¦ðtÉÏ\x0014p2M¾PJ}öR4>BOt\x0012\x0011Y¶¶Y\x000bð°b-\x001a/¡gº	Ù(âµ7â&Ø_;Ý\x0019v¢q\x0013z¢\x0008ò\x000c(Âµ\x0011í\x0005bâJ¸ÁÍ[	"-FS\x0004\x001dCør¶a¤Í±¢qvz¢·ÓÈÜi%ªðïd¡Fì{)BC\x0011æQ`¤þ±¼\x0016@BÆm"5÷Ì£h|¶ç´­ÉlÛ©`Çµº¡s;Â\x0000Ïy>ê'\x0003û EyT"G\x001bFEy{64N\x001bæ9mÄ\x001d/CÓp²\x00100ªÜ»\x0010íµn¢Ó¦Ù§ÍÄBur%J\x0016vÐ¸¡qÙ0Ïe[-£\x001cbºÂ±\x001c{Z	%ÎÎuÄ@\x000fQ4.\x001b&ºlQ~i?cí³ÃY\x0002h<6ÌóØVGÊèmK¡z´¶\x0012w'º\x001c¢h|6ÌôÙÒù\x0019·Yc¼¡\\x0018°§.{¢ñÙ0Óg{îKkáÊåÎ\x0006YÎÙ^ÆeÃD
®í\x0014IuÜ¾bâ©h<6ÌôØVôí½õ$"ÍÑ¸ì§01\x001aÇÆgãDM¢e9\x001a÷Æ¾½¶AÎ¶ï=DÑ¸mè¶I², \x001cù¾|×¶òB\x0008\x001e¹Ý\x0014ÛÆÉwm^\x000bê,>¿jQ
å^6\x001d;ÑoçÂí%zíyCIU<\x0006\x0018\x0014\x0010í¦h\\x001eÎuy>[¨è\x001c\x000fàH\x0016JÉ#¢\x001fÉ\x0004ì¥h\\x001eNtyJóÃ?é"Ñ]/\x001f\x000bÏkÎöD\x0013Õ¸<èò\x001cÏá¦g.%:¿ ¹n\x0010£\x0018~`ãóp¢ÏS"\x0014\x0019¥\x0012Àp[\x0005z×\x0019/tÂ4îÂÌt\x0017V¨\x0008¦\x000bkätãHûm/EûÜ2÷½M\x0014MÒ\x0015'Ï-i}æ-mÂN\
Ø\x0006°n\x0014þDQ¨àGµé»£òZ6#s©W\x0002£¥~ \x0001"ByNuà&¦¢àÏwgéò»ßÍSÞV/¦+Ù(ùAÉF=þëÛ_ß\½xóáÍÛ\x000f\x000fÖËñ QnP1í2Ë\ºÈ\x0007Õã\x001f<}|õâñíã'·÷ÃT2n	FÒRÓa\x0002KpDGÃÛ\x0019Æ	LègFvÒèF/¡qüz¿©\x0013\x0004V'\x001eXØLÁ$\x001ahh`ÍÚ0Jº³V\x0001Ò?ý;I°!Á%$'y#\x00034j!ÃH\x001eHóî1
Y\x0004\x0013\x0018\x0006½\x000cØ¨
LgÊ\x0001\x001aÛÐØ\x00154h¸\x0019>Ñ ¿\x0003&\x001a'Ö\x000c\x0007B;i\Cã\x0016Ñ(S\x0014,« 'hmú\x0017Æ4¾¡ñKh'q¥+¼º\x0006VwB©O>t9\x000b
MXD\x0013x§T\x001b\x001bg4"`â\x0006/:;i(\x0000D\x0001¨¸Ú-¨à¹?ÑÈ\x0010\x000cí\x00075%ûh°	\x0003pI\x0018hÄ4Pb\x001a,â2aFUù3ÄÍÓ¡B,±Í	JO\x0018.Ý\x000feÐnk*)Ì\x001bÍÇ«o>üý¿~úåà+1ÌÉ¯tJ®]~<DçË¥¬3Ü1\x0007Î/¯¾¹}üèûÑ@"ùz¨¿\x001ef}}y7\x000c¤\x0014%_Ïèã° `Ç×cýõ8çë½
RXB\x0017bSÙ\x0018½To/Ä;¾ÞÔ_ofýî=òç¿{IÎûÕÛúãí¤_=¼"D]\x0006í\x0019mdÛ\x000f\x001fþw|¼«?ÞÍúÍ\x0007\x001e¬Ñþæe\x0004×¼_½¯¿ÞOúÕÓ7rY<ZÏ\x0018)	8ÒÎØóõ¡þú0kãà5Èï>ÈP=£ËG\x001cóîùúX}ôõÎPý4\x0017qN×8_º`G¼üë«\x0002UòUjÒç[M\x001a2Ûç§èsoÆÊ\x0008=\x001f\x001eà¬r¨ Bqµò\x0003qµ7½ûüáÿP¶ª|î\x0003£\x0007ëH\x0005m#¥\x0015\x0012W\x000b$\x0001\x0006²é7?Ü¼¾ý_¼âÿü~*¨©`\x001d
\x0016Ù¨²ðm¦fU°8P\x0011Ü5\x0016®Ã2Q\x0012?Ô÷tÆ
rS\x0002\x001c(Õ\x001dÀ25Y¸Z"¦ AKT¢

®3ò ­©ìÂÅ2\\x0006\x0016K\x00065yåE\x0001\x0015°Ó\x001aw\x0010ËÕXn\x001d\x0016\x0016\x0015\x0019íd,¢WÎÖÔÕò5_\x0015x\x0002uÐFÆí¦Õt\x0017\x000cº\x000eP*,=Y÷ ³ì®\x001d1\x001fT=\x0013+ÖXqábÁ5z^,<íA£EÍGó°ªiu´pj¡É\x0000\x001eÐL¡\x0008;oB#Ë¾¼\x0003\m±0ÈÀWü Qæð¥ÆGÚ\x00031èý\M¡\x0017\x0019\x0018¹ú(­+û0ý\x001c¯AÂ\x0001®&ÌÐ\x000bãRÖËd(©WHÕÏû\x001f`jb\x000c½0È@/Ó\x001b´õ<ÿ#ÙP\x0002Ý ó\x0001®&ÊÐ\x000bÃ\x000c-\x0012\x0019i­$ã\x0015rçbZ­vÀA®&ÌÐ\x000bã\x000c\x001a\x0014ÅÆ\x001b+6Ã\x0015\x001b?õl5q^\x0017hØèI·iã\x0002M\x001c\x001b
 \x0007\x0013Ò\x000ep5^\x0018j(­CÙ û°ØB=P=ÀÕ\x001az]¬a7\x0003
ÒñåÓ-¢¬×Ô\x001b24±\x0006¬5,)Nó­\x000b,wO¥}\x0018Å\x001e\x000eÚñ\x000e`5¡\x0006¬\x000b5lÀ²
Áp\x0019ß®G54}«Mh¬\x000b5HîMËrÅ\x0013\x000bÂ5\x0018e|«	5`]¨®(åxi{Í"õ>H°¡\x0006©Ø\x0003XM´\x0001ë¢
\x001b\x000cMËË\x00150/\x0017å\x0019ÈC\x0013lÀº`ÃR¿\x0003' RÜ\x001f·]tAnÉjj\x0010\x0005M°\x0001ë
[\x001cÑábª(ã¥ÒbÍ¼NB\x0013jÀÂPÕ§³_Ójér¶fR5\x0006¬\x000b4,%AÍi\x000ffiæNÜ=Ø\x0004\x001a°0Ð0®ä¬«Õ*)ë©«?ÆþØH}oCeN«5õvbª|óª%Ao<\x0005Q)Näà°\õ FîH¾æ\x000b:½êLyí¨\x0013¯ÌeGéuø.,¥Ó(6\x001f\x001deêóÒ\x0015W\x0006fé#\x0001ð9\x001d,];\x0011GöÔÔt}ZI¹Í}SqçtnéÒå9»ùÅ\x0008ËÓJ^
£a
_Ò}}`XIx|±-×²Q9ý2O¥Ä`îËSÙà\x000b6XË\x0016¥\x000c_Ê<é/\x001dôîeS_°©µ{Òäfµü^Ø$à\x001fU±íDkÅóÛìJ2%s\x001a,ù»|ÚÊ\x001dÍ¦!îDÃs4\j%©\x001e\x0013\x0000¾~ê<Ýç\x0004î3$Þ|83$ôeÞÛðìÓíAC\x0013[n »\x001e4ï#û×Ïw_Âñ\x000f\x0017>DóDc,ÁÈCt,åÃ×\x000eôY5\x000eè­\x001açÉ_ÿv÷ñã6yæÕÛ{ÿëÛÒ\x0004rÒÛ¼`d»QÁiü×¯ O~xqóòå6sæÕ~þôIßW\x000b\x000bÔ,°%¹0<Hããsf\x00115{0bùúÖ;À5\x000b.a±®ßXØøIý»&ÂY,¦f1+X\x000cp½lb\x000e}O2ð\x0002ÓÉJ\x001d±5]\x0001c5_½\x0012ådO"G\x0005æëÇÿ\x0000«aÜ\x0012\x0018Ï¶lÛew1PÌ×\x0003Ú\x00030¾ñK`,GB	ÆPs\x0002Ó¹ó\x001f	5LX\x0002\x0013d4,Á g\x0018[¶Yç¹î\x0000L¬aâ"c\x0002£Åe¢á©ÑúYùT3³yLõ;§iýÿ\x0000@q\x0001\x000f¡ä# \x0006ñ±£·ºFGl£ô­¶øýçO¹6úÅû¿þí¢Êè!K
¡Å¥{\x0011kU¥Ço¦Ú«Ø	Í¿~ë¤_<ÿáÅ¨LZP F\x0005(ò2H"÷:t\¥½îMPÙM5	Î'A¯òè(O\x001dW<<9LÅX&ÄÌ'ÑNQªuCQË á(ÆÞut7«AÜ|\x0010P Á%\á\x0016);KÎb{
¦»QB\x0012\x0016  È¤g\x0007EöxÚ»^*|/n\x000e^pR\éÉG%\;+eö2[\x0017z%:»Y|Ãâ\x0017°8Í¢ËÞyËó©¿Cæéª^yØnØ°Äé,45ùÆo½\x0016±\x0008W^î5ïeÆCÂ\x0002\x0017IÊÈç%Ýd,»{-îÞòÅ~\x0017Ù\x000c\x001ceàØl«¬5Ë\x0012yªq3ù\x0015Ý«ÏD½!Fûô9^BôÛÙ6í\x0003%DÉJÓw\x000bR8Ï@®§û½ßß\x0003%@\x0010\x001dë±{RË¯\iÓgêB ¯§ÿN4Uv3ÓlÍéNÔJÆé(1\x001a=-H<à;(\x0017â\x0018{\x0016ÿ\x001bÛFúã»wéO7\x001fþú÷ÿ~ð\x000cí\x0014<³dmPez²Ý@{\x0005Úÿx{ó,ýéæöÇ£)ÚÌ\x00055\x0017,ã24
E1ã\x0011V. ë^Aá}\XsáÂõ*þU\x0019yÂr!J¡66#\¦æ2\x000b×Ë^Ër\x0015Ç\x0014,\x00196LïÇ²5]\x0015yhà¶\x000bs³PòSXVkØI½\x001fËÕXn\x001dÅe¸>ÞÒÏ Í½Êéû°|å×ayÃú\x000bYæ$ùÛ"@5hY;\x0015j¬°\x000e\x000bÓ\x0005Õg\x000cÎrAKÿ¸Æ{uÉ÷qÅ+.Ü.\x0018Yb+\x0016£Qtémþ»©NÙÒÍ#«uX ¯±Ì&½e¢tÕ$®¹`m¨±.Ö0Æò4À´^f>më\x0005¾,Ø½ã\x0000÷5±^\x0017l Ígd§\x001c"K­8\x000fV\x000eX\x0018Tr}\x0005l\x0018\x0019ê&ÒÐëB
\x0003^]\x0015jÉ«¦0Q|2\x000c$,,Wãõ:§.¹<Zi\x000b6ò\x001b«óév\¼òT÷¥\x001b÷¥×ù/ôX´ÓH]ÓÇå|Y\x001cm4\x0017È-âhe§\x0008Eº3ð~prÏ÷ÎÙið7%âÚäß-[9k¤«4ür²óÔÙ+\x001a~sÏ?_ºôO_¸v\x0010F¡v§~;\x0007Z¸l§\x0012àphuÎ\x0017nM8\x0005èO¦²\x0016âä[þbùVâY\x0015K°3\x0004Åª{Çé]îÜ=\x0007³K×T³]	ø-_dÂI\x000cx×²ý¶úógæäÇu\x0000øõ-l£\x001c¤8å\x000f¢>=cÍÀ¥ª¨w½Ûç«ïÞ¾ùðæùãã½G]z\þi$ßVwé¡\x0019DÃ¯¯¾{òøöñ×G7\x0010PCÀl\x0008<07è\x0000¥ÕP4òº9\x0010XCàôp¢\x0001LÊ'\<­LYºÁÔ\x000cf:CÌs°\x0003½ë\x0006éÐ
Ò0Dt9­\x0011ìtSSx
òÊp¥@Ð=½\x0003ÂÕ\x0010nú8µ({I£\x0007¯\x0006Ë\x0019|Íà§3T1Í©´!D¸iÊBÄ\x001a"Î YÅ¼\x000e§\x0007º\x0018]é\x001b\x0018M¾A·.bºp\x0015\x001f\x0013ErãÒ ^Äéì\x001c\x0017ÑÄ&(±ÉLOáøtM]=-'cJ\x0018²°ÐæÉgË\x000fÈg¿øõî§
ãÑßÿëç\x0004¯¿ÔÝL:·2Ç`\x000c´2QÆÄx×I3¾xzóhûøG¿\x001d+\\uùvóíÞò3r\x000c¨YC\x001dM:Øüí¶cö~;Ößs¾Ý!ÇPÚwSTää÷{¿ÝÔßnæ|{º-VkrÈ¿\x001d±Ì\x0006ìhKìýv[»óí$
Ä"¿:íwþvÍ;è{ó*ö~»«¿ÝMÚ3F&K\x0006\x000f\ÌN\x0012¿E#·c÷/ýv¶µ3\x001am­Fûþc²ô}\x000eÜ\x0010\x0016m4²ßUÙ3\x0016{U¬ï{ûüe²\x0003ybùx¨?\x001eæ|¼²\x001c½E\x000ek®B¥Ùábòe>\x001eëÇ9\x001f\x000f\x001b âV2lø\x0017Ï~\x0016­\x001eEm{¾ÝÔßn&ýâ½XI§L!U:FùÅ\x000f4½v}¼­?ÞNúÅcÒ"©»DÙñ2ÀÀªÑõqÏ·»úÛÝ¤ã2sÔ)ÅZ ¨@\x0006Ï[3x¾ãã}ýñ~ÎÇÓ¤\x0018ùÍëò/Zâ&Æ±ûÅ\x001f\x001fê\x000f~ó[¦uûø\x0014æç¡=H\x0003ïø7\x000f\x0003í=\x001fÒqß¬¼t`¹76\x0019 Ñ¤Ì\x0006uíúöÆÈëIV^óqÈï·ôk\x0017\x0013¯\x001e°g¶»:¯\x0011S§\x001a±<·æQúï?¼×\x0014²\x000c*.\x001c°¡hÝpïÁGÏ=\x001bJé©SYØT\x0014ïåíõ<\,Nd3\x001a
°\x000f\x0005k\x0014\±*ZÊ9¨T ¬*(+â>\x0014S£\x0015«\x0002¢·ùç<\x0017)XIÀ\x001b~bk\x0014»\x0002%pÙn0é6/îiÉÀGCÃsP\â\x0016 PkXFÁ\x0018³Þ\x001fu,J¯`w7¯IüE)\x0003R
]/ù¨HvË¸Aè±$Ô$aÅ8©gÅ¨8QG
Öb-Ì:)±F+\x0016EFI`t\ßÖDª/í\x0007%»@*Iøª`kî¢\x0018\x000em\x0003&£ìù¤\x0018I<Q1î>ÖÕ¯ðõ\x000e¨"kcIXÀGÅ³rïHÄKQ\x001aW¯Wøzê\x0007×âW1ÅAâ@7w\x001fKã õ
\x000fIsW\x0004\x00082
Ê©\x0007uX\x001a§¢Wx\x0015ã¯óS;Vx\x0006\x0001/GEÏ\x000bZNe;9l¹[`Â4ëöÐ-EI+Í\x0005fôà°\x0017æÇ\x0016æÇ%A\x0018¿PäR\¨LÑÃÎÈ¥]\x001a·biRðâ(ýÆ\x0016ïrß¤ÍËa~la\x0016,Ío\x0016µ*sÛ\x001d¬:k¯9z±Î7J8]ÃP'\x000eRûô9^CDbær\x001bóü\x001cnc`ä66\x0018!µ3Z>'òK¼2\x001bçvd\x001bµ/îóBsÐ\x0011$ÃóäE~\x0019H_÷3/î~ý×Ïoÿþ_\x001f¦Ü\x0000¶^½H½\x0002FBMv:Êu^Ò_q2æÑÍÓzMª£\x0005Âó$F~/Xä(<Û¨PÆ\x0001Ò\x0019âHþ\x001b3©°¦ÂuTç¥§µÒü\x0012¨Äpo&RÊ,£Û+}Ô?¶!\x001dHZ5\x0013©lMeQ%/£F\x0012+#6OÖÊLr5[\x0005å\x0017\x0015¨4U'mf¦³d(Ý\x0019ªtÊ×T~Ý\x0006Âr\x001faSäÝ*H\x0013GúO5¡¦
ËÖJ\x001b\x001e¨äÓYd[:a\x001c\x0018mÿôT±¦ëv`Fù\x0014\x0006ñûjÚÅ°wTAUé\x0011~´YDE¥ÿ,\x0001¦ñU,²y_/E>HÕ\x0015Ëâ
¯OsÑv \x0015kÑc\x000fR5^\x0016Zx§Ê¹Ò\x001bÙlt!ÈbuJ\x000eb5¡^\x0016[øä¤\x000cëP¦Ën{e£áÇ\x001f\x001d;\x001a\x0007©ÐB/-¢5ÜçÓyby\x001a\x0007Z4\x001c}¯1ã V\x0013[èeÁE
ÿh×¦\x0012ÓbåÞt\x0004d\x000fê©TMp¡E\x0017Ñ+\x0016èö[GCîÁ\x0006y\x0014Ö\x001e:B\x0007±èB/\x000b/2ü\x0016é=Ý\x0015³|\x0002îÁÖÉ;OµMx¡Å\x00171ø¢DÃ\x000b2\x0016X,\x0016ìXM|¡\x0005\x0018äs®÷ÖÝ\x0016\x0002æÕ
zæÍ\x0011\x0008\x0003E\x00181hñÅ4 'éI,c¹\x00083W\x000b\x0010\x0003\x0018T¬øl¡\x0015Ît\x000f.JPDÌA¬6{±,Æ ³¥dµ¶Êå|¶ÀÉjuFÖ\x001cÄjb\x000cX\x0016clJ·Ù\x001bû2¸x±zB·\x0007©\x0018\x0003ÖÅ\x0018ÉWiÑî$V\x0010ÉÈÈÆA¬&Æe1\x0006k\x0011oâ\ÏGËq1¨\x000ezÊTM\x0001ëb\x0014.EñZPNÖÉgÍ\x000c 0`]ahÈ{µUnK\x0015D´4`§\x0010ð Vãa+vß¨Iê73Å(¢4Üd\x001e\x00136\x000e\x000b×9,_L ½)²\x000cÖ²\x0003ê|:Õ&¦×Yöd\x0003-/\x0015Ýs\x0006#¢±3\x0011é Vc\x0003q
^L»3ATP4
$ÁöX½Àeö"]8.*Nxº\x0014¯Ëj¹NWæA¬Æ^à2{A/=\x001eì$Ou¥ì\x0019cÙ©9\x000cÓ\x000c³ÌdÄt
Q|¶T¸\x0014\x0006\x0016ðNñAªÆbe\x0016#\x0006\x0010a\x0015\x001d9 Ñs¹ìÏôY¦±\x0018fÅQ±¼§ÑåVÌÚ	«S#v\x0010«±\x0018fÅ°!çÑh\x001aOBÈÝÅNÅÈÑ»~U6oû?®²ðéÊe\x0003?g¹t\x0004ä®ï§¾}'¬Î°~ú\x0007À:u·=Ó\x000fV½û\Væ£	åYÕI¹\x000f)9N}T8gãÉòº\x0016X­Ñ\x0007¥ÈêoIxË#
uú¼jì9±ëà¬R^B_KåÍòb\x0019u§õýhäûÅ®\¹-CÄ\x0012\x0000û¢\x0011­Ñ\x001aë;eÎ_§\x001b\x0005é/ÖM/\7\x0013RÐ!£ã´æ®P§HÙ\x001f¼:¥Â{Ð´Ón*Ò\x000f¤]ëû7ï>¼½zöþ/§ìCoJ¸ÂÊsý \x0008üG7¨åüþñ³Û'WÏÿñõx\x0017
\x000fÔ<°'@ä>u\x001fb\x0019Â\x0003J
äÉ÷òÇ,á¡z à!rù"éµAEÑw\x0004\x0003¾\x00023Þi®&qHüi§iÎ\x000c&\x00187U;PÙ»2¡æ	kxÙö¼2¨ùÎk]ÈºäNJJ,Z\x0003ä´T\x0004\x0000VÛõ*\x0002¤ú©{°\x0001Â5@éV\x0015¥·\x001b\x000fèæÑØÆ®¡±QËø\x0018¯#ËxÅ2è\x0013:Ï {¨H½­µ%Ópwóëo>|J\x000eõ¯\x001f>[^=L\x0011A9Qk¤ÛD¿\x001e%Èp¼§ß<¾}Üé\x000f¯/@\x001a	\x0016!Y%å÷ÊYº$nHRãsÏ$Ö}<Xóà"\x001e\x0012µg\x0005ÝtÕàÜ1±¨Ìvtû!\x001aÉ,B"åµÀÇ(y±tÙàbuÝ3ÛÇldWíº(ý8"ï
ÉÅ"ã\x001cÆs¦÷!¹\x001aÉ-BJ¦Û³mÀ@å=\x001bR<I7w$!ù\x001aÉ/Bò¡ 
©(6\x001b3\x0013)ÔHa\x0011R
NY¥T9V
 5tæh\x001e#5Q\GäDySëb"ÑÁ\x000eî!¤ª¢NZÃ\x0004:ÒãIy*­Ý\x0011¦dÚ'2µ¡Ã¢Øw6\x0014F0\x000cPè\x0019\x001ccjb\x0007½*xÐN\x0007­¬Lj2Úè=\x001b\x001ecjâ\x0007½(\x0000ëã&(\x0003\x0006¬¨Æqæ25ÎV/ò¶`¥#ÑGjåËÙªºg¦^ÿÞÁ­WuÀæÍw÷;Ý}YÐ¨\x0012Ë\x000fj¥¼G¿Þ}þ÷.K_h(m\x0017YF&;fÝyDÃ¥¥è Ó\x000e!2JÞ¼þÎí¨ùxS¼óñ\x001e¹:ü¸NÒ?Þ¸±ôÖÅ\x001fïêw~ó+\x0003¢O1uZ~ó<\x0008]\x0018HÙìúøP|ô·$êÝ#¹æHJÙS>þ$zF\x001f_=èWn¢)j¹\x0006éWÎ_"®Ý_¯¯×s¾>Ý/c(j®¹\x0010\x0017Qsí\x0005©¹NúÝ7öFO28¤Ç:º45ký¡S¿Þ\x000eÒ³»¾\x001e¯Ç9_\x000fJ\x000em°\x0007á"\x0004'®.Ì1º1z½4<ÊÚÑb/Mùúáº\x001d_o¯·s¾>YIàß=Uj³Í\x0011q´sã_v|½o¾ÞO²9"\x0015Cr´­=_d1¨NÞîç,ª:ÿRg\x001dÿ|ÿá/é/?¾zu÷áÝC\x001fjµ6¡\63ä
õïò
©ã|«G½?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þíÊe H\x000b±cnï=\x0018\x0016%\x0013F\x0019·è8ï`¤ï û¨\x0004\x0019)JzÑèW¿\x001e\x000c:\x000e&!çt5qt!ÍDª§"ÆÕÏ7\x00089X<ò\x001b¯x
Ì\x0019dû^O\x0013;Ð?ðà;\x00075(9¤<\x0017½¶f«\x0019©êLÚE\x000eÇ
'\x000bÓ ä`òX'w¸\x000c\x001c ¢úZ ÷çwÍ9¦AÉÁ"åÑ§¹íV¤óVj\x000eÁÇ]ç4Ó å`Ñòè['¸\x001c[ËÏtYyA\x0018\x0006)\x0007GÚ¡w+Avç^+d¶rÄ5¨AËÁ"æ|u\x001fd\x000b\x0015Õ×¾n/\x0013*-.<\x001cÄ\x001c-b^w<<ûHöñêzÔ:¦yMC
b&1¯ÓD
¢ç>9)Ï\x0008\x0019©¼8ÍqÜ[Äå ¶eÉz\x0014maohöm\x001aÄ\x001cMb½>rK`ÅÔØ°âÅm9\x000eb\x00161gAÐ°çs;é¥Ô6waõó
j&5/Í\x00022'ÔXC;,\x0004¿:R£IÎëV$Â\x0000'kk©s&Ï\x001cÒ æhQóÄ\x001b)ùxÉkãÙÌ©§2NÇ\x000b½i¨AÏÑ¤çìJZ(Ö¹=¿<Ë\x00079G'"M\x000cc{[qÉ\x0005[\x001eÖêÞ\x00069'°·¯Øc±\äåvO\·ÁS\x00069'×½¥<_»¼;­o\x000eØ\x0010.	b«PEÎ¹\x000b°îîj4\x0016\x000bzvh»»U¦ñÅ¢æ)~ Ô*ü²ôVww49YÄ<qèfÔ\x0016FU\x000fÔV\x0000\x0016¡\x00061'×P²÷UÚ\x0007jwDâC\x0013ó²\x0018i\x0010s²yBT\x0013$v¥ô²kIåÖí\x001d
jN&5¯û\x0003iwsód-­T¼\x000eÔâö\x00065''ÒÎu úòåKnÏ«#5È9ä¼ <l#E2¥.6Æ¡,BùAÎ½EÎÓ~ÈÛGªî¤v&×ö,~iPsoQó\x000c Îm<PeßHË×\x000b«s?¨¹7©9û¢ $Çy\x0011\x001b\x0014µÅPì\x00071÷\x00161ÏØº\x000båLÚ¸þqZÔ(?ÞÔ<\x0015u6eZy®­\x001bÎ&Reu¤\x00065÷\x00165ÏÝEKnýùJâÖ	5¹79û\x0013ú6PrA]"µ[²Uáô{gßúÔð\x001e©îòX\x0015\x0016÷,~\x0010so\x0011s¶ªV1¯\x0003%®¥»þÉû\x0003?¹·y\x000eØ¦y\x001d¨,]D¨41OS*\x000cb\x001e,bÎ\x000eîtRr_JÓ(\x0017oÊÂ æÁ¤æ)K\x0011ñ¶ö¤\x0016Ó¥K-Òb	\x0007×sÝÓØNêNf¹öf½a{\x0010\x00065\x000f&5Ïyo²»S\x00145Ï\x00175 l\x000ejPó`Qs¾4Ðcq\x001d)\x0019(Êm{°zk\x001eÆ÷OsÑÞHÕ*Ò¬ÄµÚ¿°ú\x0000\x001a\x00065\x000f\x00165ÏåòR\\x0007*%ùz
jù\x0010\x0013\x00065\x000f\x00165çb)±®ßFj\x0017)K¥Û2Ô çÁ$ç%I£m¤èAiÇâÕ\x0010\x0013\x00065\x000f\x00165/[\x001cT\x0010\x0000±M©ÕûÄ8¨y´¨yqYRë@V6k\x001b©°(æq\x0010óh\x0011s¶Ýj[ó #\x0008¯&iÄAÍ£EÍ\x000b´º*\x001e(/³Ðµ+©e¨AÎ£EÎ¹-¾a³¯¸L©KØ[½ËGó×K¾
È\x0001¥¦æb\x001e\x00071&1I«Ð2§ôËÊD7¯¼1Å"æ%¶eI¾M¨Kõ½_\x001e©AÌ£IÌ3iÙ2O(\x0019)tØFjõ\x001d-\x000eb\x001e-bÎm#Å1§úKa¢¦Q«Áq\x0010óh\x0012óÒn\x0003%PÐñ\x001f*_J'\x0007ç@ìk¶)%Q¯\x0006¶?X\x001aÔ<\x0019Ô¼BáeË\x0019M
^.9W_=Ò æÉ æ\x0019S\x0013)Ï
\x00196(®\x001bU¨AÍAÍ+TRÜm¤¤ 4´\x0012Ì\x0000/
r\x000cr\x001e\ýWãeNI0Ætya8fâNC
\x000c¾A¹LAP¨v0v»ó4\x0008z2\x0008úV\x0007®û»Ô*ö1çö^¼úîÆ\x0004E \x001a\x000c8yZwçâaB.Ü\x0006AO\x0006A¯P®ßK©NÖ\x0019Vo¥Ò èÉ èÁUEËõÝ>ÏÂ%­eq/\x0007AÏ&Aç.Ý¹×\x0016á4ÜcAÃ4Ô èÙ"èPÆp¹CØk\x0006B{\x0007õqQ\x0011ò èÙ$èåòÄÀç\x0018ùzt\x0019¨Å\x0019\x0007=Ï\x0016=\x0007ÄË«\x0015©C\x000e%
·\x001e\x0019ò çÙ¤ç¥\\x0012#H®Î|Ós:ZMC
z-z\x000e\x0014Ú)[\x000f	TqmJ­\x001edò çÙ¢çÀE;;¼\x0007\x0019j9Ë«×\x001ayPólQsà6|ºôôÑû#Ý¼ÁËcÂ¹EÍÙä­P\x001b'ñj¨\x000bî2R«koPólQsàÄÒFJÖ¼oÅ'\x001e\x0016OWeóbs KæÌ¦Üüè\x0001C¨9 AÊIÊ«j&h£$\x0016ì¾\x0015ÌÕÍÝâ$/\x0017\x0003ú6P$#U.+oµ©\x000cZ^,ZìÕ½«ï\x0017çþÚ½¼
.\x0017/msÇO\x000cûÊóîRõE«|ÐòbÑräö¹\x001aõ@¬(ëy¹ÅÕ
g\x0019¤¼¤<6ã7+qcóØÞ¬hU7Ë æÅ"æHU\x001d¨¨=;ZZ\x0004åÕy>y1yºtïMÝÍ7,
ji¬\x001e²h9V-²>0\x0004jA\x0016sÜÀ
RÎi	0»Ý\x000cµ\x0017.*µxXC\x0015¨³\x0008:w\x0000I¥]\x0005í\x0000ÒÂÞÑ6i\x001aj,\x001fr\x0016Açbñòb,Vþâ£¹¦0ò_\x001aö\x0017\x0018Î½`\x0000Cò­ú+­RåCÎ"èõßª­Çë(®=\x0010áb*. ü\x0006¦âÛ£c,Òä\x0015Cm¤\x00167.0ò_ZÄ3·û×:Tr\x0008­BßjÒ\x0016S#`¬\x0006å¿§"®kÒÜÉ¤3=\\x001fÂÚ~
ÆPþKÃXÕmnÐcÖgcm«Tc\x0019³¨:Á¥d'z1)Á\x0008íØ\x0000@p(
µTr~¤öÙÌlñ"_Ð·J\x0014\ÜRÁ±*Ô"ëÄÚ¾\x0015\x000eÈ=Pôíz\x0003pí|\x000c²PK]èÖÆ+Ãå\x000bz	6­\x0004\x0013\x0017ÏXp¨\x000bµ\x0014zÚ\x0014m® 
L¼\¢»ÅÔ@8ÔZ
Ck\ËP¤ñ³c«\x000c=6\x0016¦\x001a¥ÝR\x001aZª´ã\x001f÷»Ýw\x000b16ÃmwôQ¦\x001a¥ÝR\x001cÊíT\x0013·W¶m¬bÛÂ\x0003ÆÒsT£´[ÊCw3p-rB©YÅØÚ1 [ÌC¨¥B´\x0006g¸|Á¬=\x0015C\x0006¥Å*h8TZJD\x0003%/*r>6øÒ/Èõ	KTc(XjDk¼Óf£,\x000c~\x0013Ýe¨\x0016ï:`,\x0011\x0005Kèfê´È0Iks¥ÝÀ¸Å{\x0005ÀCÁ¿EÙ½Q´ð8h;É\x001aoÚ\x0007Åi5\x0016¥J4øº»*ZäKz1P3¬¡¬îcÆ*Q°\x0006j\x0000\x0002²c1*ÐâK\x0008\x0015¢`)\x0011
\x001eC«è£¨Û½äõ}\x0006òb¹\x0005%¢`©\x0011­ÃT.Tá®z²xÅ\x000fc(XÊD¯[cÝXaÑ\x000bÐVâ\x000by±À\x001eÆ*Q°Vù,|·\x000fUÒ%\x0017g\x0012(°\x0018\x0000Ç:Q°\x0014\x0006_c±ô{`"\x0010ü¬Æ29×\x0012ÕX(
JÑ­ëDeòR\x0018kpä\x0003.Þ¡ÁX(
JÑà\x0013¶÷m$õ\x0019Ï®uMf\x00120V¥T´a¨\x001d¸\x00104#aQùLYp@\x0007\x001b\x0017¨ç¬ì¹9ÐaFm#RÿÄÅ%8V¥\Ï{O\x0005
·îqÛPQÓå©>êº¥Z4\x0004Gí\x0012\x001b¼Þ8fßúgÇÅv\x0018«EÁR.Êmëôr/þeRùØ>ßê=ÌX.
zQ\x001eVX\x000bNï¬r»\x0006¸z2\x001dëEÁR0\x001a¸Ç}·\x0000E×SÔ\x0014â*\x000b«c5êº¥bM1¥¡Ë.é3wu¥
å\x00170V¥d4øznÈ"ìyM\x001aÛ
\ÜÃ%£`©\x0019egÓv\x0006ò¾âÚL\x000f«±`\x0014,\x0015£5*S;,³(R6§âê=öX3
¢Ñ:Nóßör^\x0010ZkïE¦5IÒ9ÓLV\x001föSÌ&,Æ±d\x0014,5£asÆÛ÷©$÷m H\x001bK_´V±h\x0014,U£5&_Jzúõa_\x0017ù\T£¨[ÊFCàê§$c\x0015t¯W¼\x001aOÁê\x0001b,\x001b\x0005KÝè\x0010\x001dizÂQ:94OSn)\x001c
ì³-.A©´®¥]VYÜ\x0016£`©\x001cåÁÐ±J¥pÐÙ£²¾¹A8úFOS¢n)\x001d
5üj©X*íº±ÄÐà"Ó¨êÒÑ\x0010ps\x0007Ú¢^6æ¨-¥àdd=M5ªº¥x4D@-/àºrI\x001d,I\x000b1`ÕÆ\x0013ÆâQ°Tr`5\x0017eó\x000b¹×Ëù"\x000b«/6c¥&XJ5Ù¡Z^!\x0012'
\x0014Ý,Ä6TGø±(\x0012,U5,GµvI\è\x0003\x0012sûU0V ¥\x0004q\x0013+ñõM)ë\x0015hi;=\¬'±Ú\x000f,å~X%[]z$\x0004TAWßLùÙzM5²úïæ\x0018ìTpëë±%\x000e¹æñr)
eµh\x0013luÐLlÜ¸U_Àú,!`¹ø,­\x0016ùÿúeëxaóÿÆ?g«ã¦ÕÉkÕ\x0008\x0004¸Ù,+Ó¸\x0005ã¸q©¤~Óº\x0011ÜÑÚ6C\x0015íØ©\x0018.+Îï\x001f>½òÃç¯þíZ»º`\x001aPgÔ÷´d®rÛ |	ãö¡ÝÉ«·¯_¼zþä7ï^=\x0006= Ú\x0000&ù\x0012/Rá\x0013­ß»ë|Ôó4`R
<÷6@Éðó%v\x0017¹ë¾\x0007ô6À¤Î\x000bÄ­YH\x0000¥ª\x0002væ>ë¡\x0007\x000cÖ)(5UÜ\x0015\x0014Ðë\x0014L×û\x0003\x0019\x0000c\x000f\x0018Mä5·Í×íQOLÒPÀ×_9zÀdýÄ¤~»Áß\x0017IPÀï1¹çË&>®ßÛÏãî3Î|E¶o\ü{µ¡\x0001°ôÅö[õ1ß
\x0017\x0019@j*ÓwX#]ÎR×Gy° Þ+ò\x0010
!¸Ô>qw±¿N8\x0006\x0012[$N;»{ÚRú·1í#ï2C$\x0001S(IÜ¤;·1dgy\x001eÃnøï1C,\x0001[0I­®'jZ}\x001bÂï\x0010K`%`
&l±©u\x0017HûJ®g
h\x000bå{\x0010\x000eÁ\x0004lÑ$·.ÁÖûQ\x001dÃø\x001d´\x0006h\x0002¦p 5\x0014ñ´Ù¹îcØréL!Ö	p\x0002¶xc'´_^nbã\x001aá÷È0\x0004\x00140E ü¼¿÷\x0014Ìà5«m«$¹p(`\x000b)U°å*Ç\x0010El\Ö}a	ßa¥à\x0010RÐ\x0014R\x0012næ`\x001b!ßd\x0008¡×Ç~÷=6®8D\x00144Eäæó\x0010:ÚR\x000eßa\x001aâx6±Ez87\x0010~zÐ\x001cÔ£ ï`½\x000e8\x0004\x00144\x0005äÚéÉSÚq\x000byE.Î¾\x0003Ý\x0010MÐ\x0016M¨\x001d9EÀïOÞÎÊðùï¡8D\x00134E\x0013wî¢3\x00185ÞE]#]Nï:á ÕhÒê\x0004AÝ?}h¢Dîzch\x0003à ÕhjÊº·\x000e\x000e7ÅÙ>².ï±oÅA¨Ñ$Ô	²$7øôp\x0007^½ñ]ßøh\x0019\x0006&N{·-m\x0000KÛ¶&Íq¾Ã\x001c¤A¨É&ÔHúfî3nµ\x0015{$!Áò\x001d¶þ4\x00085ÙÛ8î«$pbì\x0017>¶ð­ôw \x001c¯lJÍX¢4e{ºÞC8ÿ=O4h!Ù´\x0010µ±o%ÌÛÒF¨	7.Ðw¸\x0006¡A\x000bÉ¦äôMßl½anZ¿C<¦AlÈ&6Ü\\æ!À@¸G<%ßã&Ä\x000fkÙÛÖrÝ&HR\x000e¿Pz!LjÓáò÷x~X)Þ¶R¼ÓlÂ@±ÍC}µá¢Øï\x00008,\x0014o[(Þë®°nR·þ¨»Ø¨`[Ö	\x001e{c×;üë_î?½ÿxý	Â&\x0001_\x0006ïEòUdÔ¨­í±Ùô»\x001fî^=ù\x0018
ö48M\x0013µU8×H$4ªyéÔ#nz\x001a¥AV^àI+¥ x­öNç×s4¾§ñÓ4õÛ\x0012û{®\x0010\x001a:ö
¤	=M¥©\x001býú±M|*\x001fJ÷HéÔ8É\x0012{8ËRU~\x001f\x0018ÍQ¦°zx¥pô6dI=K\x001e\x0017w3­_-gäéÈÄ¼D{<=2A.8yÿªECTíN1â\x0012MéiÊ$
/iBùP$sÆ\x0017uÛOáX¶6\x0007s¹EÇ¾ãø£cãawjúÑ´7PÝ»äÛ>\x00142<«Ã½Ø@ÂVñ28¾éð±¦a\x0012gÐa\x0017b';utP¬2ëúÖu,Æ\x0019d\x0018fu²\x0014÷nÂ·¿à×¡Q×Õt²í¤\x0019d\x0018fuë\x001cQV8\x0017ï	\x001a>¦|t\x0019¤\x0019¤\x000ffµr
ü¡²\x000e¦¤|L»Ä\x0019ô\x0006f\x0005r\x0012×-dz\x0011\x001c§Õá)\x001dcÏáà°ÆqvSÖshUÌWØ²ªt?qêµ53înfW\x0015×xí~uÓS£Ikéääÿ\x0018?îü|¿óÛ\x0012g®-ðDm\x0007-ãèü\x001dSÕ*Êó7`\x000f Y<YÀ³O4\x0007½PËî
èã$ÔÐ$	H¢\x001cð/÷P\x001e\x0012\x00059«Ìã\x001c¾çð\x001cI\x001c$\x0007gw\x001dã\x0011Qó$y#ô\x001ca#\x0007¹m¯û"Ö¶õdªiêùäd9E\x0012{8IRÚ2®\x0011\x0000e:¢f<¦ñO¤$M\x001cëV\x0001
\x0008ê+SÎÇd²)Üä9BÖÆ©lüÐ°\x000fI\x0002ý8Ç\x0014æ)ÒÉéZ¤±\x0013\x0012µ_uD@\x0005Yl3$Ý¦Î\x000fºÇ\x0006E´¯*ÌXÒ«åÌgvQ^gõ5h ¬ÿ~í\x0013\x0018Qûaà\x0016f
\x000c\x0002\x000b
[@r¥Ë¾dÿ\x0014I°s:ÚL¡\x000cÊ\x0006ÒV\x0000ê\x0010hïËHöó\x0003'êÇQ\x0006I\x0001¦ì$©5êÒ\x000b®\x000c\x000b\x0019&W2odÒæ¢çúHºG)+\x0013\x0005åË§Ïö;ñ\x001aõÔ¯¦h±TÝq\x000fh£É9Ë\x001eÓ²zð©~\x001cõD+§æPß\x0006	ÇmRè¶IûúÇ÷O~¹ÿüÛï¾½_Úå\x0013N\yÐ¨ëúØBëîÝOï~}ûüÉ/wo~|}ýî.\x001c7N¡Û8M¢±ÉÂ\x0016P;GÍÀ©B|ô¨±¡QFF´Å²¿\x000e\x001b´]&È+\x000b\x000fÛi\x000baaó=7²Q\x0010×ÄÊø\x0015m;ªhÇâ:nxÓ¸-XÙä\x0010³C\x0006çGnlYÊNãÑ<ÑF\x0016{²h$«Ç¨"£\x0016\x001caB\x0012§´'[êÑ\x0015Íi\x001d´(fu\x0016ÛB8ú½ÚØrÏl\x000eøöm\x001f¶(-vß&íTgc+=[±²5ÙçPäØ\x0016Â±@ÈÄÖíäB¿#v\x0010Ú	>o\x0003w,\x0000µÁ1Á\x0018\x0014¨\x0014qÉä6´zv
>·ez>!Yà¨\x0000Æ°@1è^«DßôÍµÏ\x001aÎÑÜ\x00027Ä\x00050\x0006\x0006¾
¹É^S\x001b¸s·°
q\x0001ê£D\x0019¸$uìà£\áÇs':\x001bÜ\x0010\x0018À\x0018\x0019(©ÉE\x001d8\x0016T\x0010Ú¸¯m,hCd\x0000ch pzä)­·\x0019xm\\x001b1\x001eý*mpCl\x0000cp ¤­B¶]Ów\x0019ÐJÇò9\x001bÜ\x0010\x001cÀ\x0018\x001d0i1$Ý\x001báêÀéÈ¥Ûê\x0010\x001dÀ\x0018\x001eØZ³ø\x0016º¢Þ¡ºÔ\x0014øµCx@cxÀ\x001a\x0013äÙ¤¤\x0016ó)ù6çâé¶Ì\x00027\x0007´\x0007ö0¹\x0008°è\x0008×§Ð-:\x0000£QÙàY>/
Ò¢C¹	n\x001094\x001cÖáB\x0011¹\x0004{W¦Ö	uä¦ÅÐWmÊÐªÍé/ëCÛvv¸Ä}4Õ²"vE¯¨E¯óQ,Iwmã´\x001bèóÅvÛ8\x001d=bÇÂã0y\x0014«pHvÖv¨X\x0016\x001dµÓáÑv\x00161\x001cÏûárÞÿü¯~üpÿoWujHPkº1NÑ*~¼^ëðîÍó/î\x001eãÂ\x000b§¹\ÔfW¡\x001eoÜ\x001b¨8µ¬ÀëÅJs\ÔsÑüxe-ó
·]Ý6^QÇójúÕ\x001cï¹ü<\x0017¨ÅUà\x001aCñjÞ\x000e®æOÎq+Ls!i\x0017ÊÀÅS2¿@óxz«ê%¬ØcÅùá[AÅ*	ÛLÛ>£\x001aÍ±çm\©çJÓ\\x0004Ú³\x001f_@K]ù\\x000cWÓ\x000fç¸rÏç?#È³Û^éNûÇs°ç°JU¦±|«>¯ú*%2É«	¥#¸M¼úÓ|èNó3³ÞÅU¯³ÞécbÛÔ\x000b\x0006UyY%R3.Ï¦22½òeÀV¿c<Þ:GwBï+Çu2në"=\x0002\x0017rld¡4ã$üö=¯ã16ìÙÐÄ¢2[D)·«pjm_Wí·Ulz:²ÐÕá\x0002ßFÎÉÐ¥æ\x0004ñÛZ6Cç{:o¢Ë­îAè{Ø÷\x0018»ÐÓ\x0005\x000b]]\x000fRH\x0019ò¡TwBå;]ìé¢.ª\x001fqq»¿gº MÝùèw3]êé\x000e¢Üònc§ó»Ò|¿±Ë=]6Ñ5p~|ÝK×*]ó#¸Zj0MWzºb «§\x0014-w	\x0001ÛuÚk\x000fú\x0017¶Eº.xEw\x000c^\x000cÃ¶kã\x000b²,¸}\x000eÞÕz¡i¼1TXb\x0005T=\x0016OÀ×;^=âQ\x001b½¿-\x000cÑ\x0002,á\x0002Ò¥ä\x0004÷©çs3,%üvÁ\x001bÂ\x0005Xâ\x0005\x0004\x0012?qz{-Xò­î\x0019ðöO;D\x000b°\x000bnc¨\x0015B|× ç«zLncwû§\x001dÂ\x0005Xâ\x0005øÖe\x0007/ÈàQ³
e£¹[ñx\x0001\x0001õ¨Ü6*^ª9\x0013½èè]÷\x0005Æ\x001b\x0002\x0006X"\x0006°Bl£ea`ó§Åï7D\x000c°
\x000fdôÂS\x0010:ß\x001cEÝítCÄ\x0000SÈ@ßªû\x0002)\x001d\ö\x0002×\x000bÓfép\x0018h\x0018|/c\x001b»$ìÚfÀß\x001e1p\x0018h\x0018Ðíi{¸Ùð¨Iò#'Å\x0019¼ñ|a\x0018îÒã7zr¼®»;Ý\x000exºyêá\x00101Ð\x00121\Ñ\:zA\x0003\x001a¥Ø¶\x0003tûè
1\x0003-1ÃÕ	§\x001bÑ´5ÂÞðª®\x0008^p7oq\x0019h\x0019.ÒSý¶»ã;ÓQn\x0007 ëõÓtCÈ@KÈpþrÆÈ W\x0015\x0004\x0017wçÛ5\x0019á(´ûéä7[\x001eÆs^§^ø\x000eSo\x0008\x0019h	\x0019Ë>dðR»uu\x0017\x0017ñpµâz\x0006Q&(;.0u[âötXñ0_´ÐÍ¢L(A]á¶«2xEl\x00126÷\x0018ùæ3\x0010
L\x0006M®tÍ=:Ðã-¶þTnx4Þù\x0018$ÙñË¹ØgóàÉ.\x001e»N)7

L\x0006Ev%emù\x0016ÛêLîâùn\x0017\x0015\x001a\x0014\x000cì¶'Bjdð@ë¶8ôf¼AÉ ÉlÖ¦\x0001£´\x0007¥¹}'¼}æ
L\x0006Ev´P¦*2m\x0005·×ú1\x000eÍTVñ\x0006E&"»qóåÛ¾-\x0019hÔ>íw¸\x001apÃkð~¹ry\x000eºþqOS» ðr\x000e*ûÛåHdBt%jÉ{\x001dÇ [RDm\x0006
}1µ2\x001d_\x000bR{-øáþó7Ñ\x0003´=!;¡Ñ¥ý{ÁcÿÀñ\x0019ý»7ßx=OÇ·ÔÞ\x0006\x001e%ÉbµX\x000f?A[ \x0005n\x001c²\x0004w´o"¡æHØ\x0003pÏ\x000b¢	ÔÈC!$pô"ñ=$Ib¸¶]À:í-­Ô\x0012.$LÈ\x0012Ûî©µyº>'S\x001f)ØsÄi=½\x0012w?Î±Ùv\x0008´2 ©\x0007Is \x0004Üüq#aK-\x0016é\x001aô\x0002×~ÚIrOçH°<ÍûÂá^äYIô/¤cõÿ\x0014IéIÊ$çìô$?\x0015-i÷Q!\x001dóéf@º{÷t¹w\x0004åù\x00130\x0015mü\x001aÔ¾n#, \x0002;©°åñº¢xN\x001bJ3õ¨Q\x0019t
&
ë_7­m'Ñ´èí\x0000¿IBî\x0010uê\x000fº¨óåï5*¾ÿÇÿ¸\x001e¶7#oñ¯K\x0008Õ\Ôã\x0019èÚÖ§½ýÓóÏþ/ÑaO\x0016º\x0014[«\x0000aqñÎ¨N÷è®í\x001bçé¨§#ÓØµ.ÐÄ'Iw¸|5\x000fhÍ÷lÞ4r­é\x001dÞoq»Uý®uWy3]èéiä4ëÿÑm\x0010÷\x0013wö®ö§=]4]fÃý»&5î«cõÃ^ÝÍÎÓ¥.YèêF[L~ëÿª%c\x0003ç.|y{ºl\x001a»"òVÿÑ¢fçâ%¯[ÚÏ£\x001e­\x0006Îëg­ëí9s\x001b8é¤ë3]} ¦»\x0004ÊMiM4SP,´\x001dTöÁkkâêsÃ<Þ\x0018'LK¥v±C$yÅÌ ==÷g¼\x0019o\x0008\x0014`\x0014\x00195ë\x0005SKÕÊ\x0014\x0015/\uÇ\x001bÔ\x0018LrýS¡¸?tqË ]\x0017þêï<Ü w`Ò»´Ã\x0012r±ª.\x000cmx1ÝÃÂ@ÓÂà¶2óÜV,'óµû	<8n  m ~ûZ\x0001¿üëûúá\x001b¥îß	µA"çFì[îæÎ\x0000t¬úñ]\x0005{ûü§w/®¼+\x0017ö\här*Å)´f¼\x0014.\Ç¾\x0006.ê¹È<^ò&8Q(Ëx¹öd~j>m\x0000ó=·\x000fp9±Ë©ãå.Íãnà
=W°O°^@Ph\x001dàáÔ¬ÔÀ\x0015{®h\x001e/ÉoåævQÀÚ\x001d
\x001c\x000fU\x0016®Ôs%óx)\x00179q\x001bâ\x0001ÓºSkl\x0003Wî¹²}¼\x0004Ëó¦W«ÕYÜ2^¥ç*öñÏÞó:^Ù]ü±oð<W·!ËÈ2`2b¸\x0018ö\x0011k©¬.®oüÊN¤Vhá×¿#\x000c\x000fvÅR\x0004­U/µ^Ë®äu¥AYÁ(­®hï\x0014n`Q,©[{>5¿!Ãt\x0008Þ5¤é¦öýý×\x001fÞ½ÊDõçê­ZµÏTÉ±\x0005:<\x001d	~x~÷îåçï\x001eã¡¦yê\x001eQ.ß·îÆÛ2¬¿[>^G§YÐãYIK$¯{ÿ}xEO÷Þ<©çIÓ<\x0000r>\x0002îí÷ÑÉZÔ_ÕÖpJSL_k\x001fzª\x0015\x0003\x0004\x0017ëô\x0011ÓûÄ\x001c\x000ey~6'Ë(ÈÅÉ#RýÝI
àtÛ:	\x0003\x0010Î¯ ¦î[ç$\x0004ý`R ìhqüÀã§y\x0008%?\x001dÒ¶Íçf \x0000ît\x0007<	\x0014\x0007 8?@¤ú1ð±k\x001b "õ8t4¢\x0005Ê\x0003PBõ3_dN¼\x0015Þx¢âþ\x001e£9¾ÒåEô7æùøß~ÿüå*wÊ½]Ú£F:
\x0019Ñ\x001f«ïd¦ÿþúÍÛÇ°GB\x000b\x0012l½P¶Ëû¨E÷|ì\x0013¦Ó'g¢\x000cL»K¹>³ìa\x000c\;\x001eÄàÛÝi&ß3y\x000bWsZ¬§wi\x0003À55Â\x0014OGi¦Ð3\x0005\x0003\x0013:]ÿX\x0005R\x000cºë¢ã\x0014FËóL±g\x0006¦º\x0014clØr6$Ôð£ù<Pê\x0005È©76¹í\x001bnD ^ 1\x001d÷DóL¹gÊÓLÄ9uEG)©ISýóPGi}JÏT\x000cL\x0019ÔàÜ\x001eLJÛº\x0013S÷Ö:\x0007\x0015·þ3\x000cµWëîPG\x0012O¯óP£Ï«8±9S(/oô®$õ©¡\x0006\x0019y\x001d§R7\x0000úù(êÞÍ\x0005v¨ºË=6n\x001at\x001cæ¼BÆ;B½çákÎöùN§·i¨AÈa^ÉÝQÄv¼\x0018yò[ÚÁ\x001f}æ\x0006\x001dy!'¶ÍÚÓ»·\x0017eFµ$ÛäN÷tÓPÃ¼\x0013\x001bïS\x0011Ïï
¥¦ß	n-óPÃ¼W¨ æJü¸¿aÎÅÔ&\x0010}ß"#Ô æ`s\x000fRÐ\x0005\x00143\x000ev(=ç¦Ií<Ô ç`Ñsî%¢#EâRÈ\x0017_:§àhï8
£EÏ¹ù\x000cTl_¯mX\x0012\x001e{ôÌ3
r\x00169Ç$^µ­\x0018lÝqpy\x0013ã¦Ü¢æl¶*k[ë@AJ«Ó\x001c\x00075G³«ÊÒ×Ã\x0015iyB
b\x00161Ç¨n¾TÂ¦´ºòpPs´¨9_uÇK(víãÑé6u\x001ajPs´¨yÝÓeÛ4\x0007}ÓKt´=\x001aÔ\x001c
j¹s|½ÿér×FÇ-¾AÍÑ¢æ\x000eõ\x0012ö
\x001dJ/Q_>\x0011ã æhPó\¨\x0018\x0017ë4skÅtô\x0011f¢AÌÉ æ97¿>*-\x0016ç\x0014µíP8z¥ÍC
jN\x00065ÏõÄàeg'M\x000e*öñ§Øi¦ñ:Ã uHÄlk!\x0018)6âçE¨A¥È RK\x0007$Ä\x0014ÐËÌ\x001cR:&_\x001bÎ{}]ù´®aîÚ\oìÑ3´]ÞñfÜp9±\x0013\x000f|cóEÏ\x000f¾±­Î0Gÿõ~¼2»¿æàlq/wfI\x000e¸¨)ìÑ\x001fmx'°òñº3w×0ÔßÞÿqs4öÄmÎZÒ6,UÝe1²åçéWú©þå#LØ3¡ÉkkÊäÔ\x0011¸ÔÉ¥LÇ&5óLÔ3e²VCe~\x0012&í´ä{$o\x0019¦¢õc÷ìût*\x0012\x0011N¬óD¡'
A*j\x0006©5\*-÷±\x0014{¤hA\x0002©+ÎdKUÇH\x0013ßë¬:)è,Rêm$ñ-c3ø­£$GQtù¤N³L¹gÊ¶aÊQìòx´.o`gJÏT\x000cLuíKælÕq\x000e62NíÛ£ß$SwÛûÛÎBýx5<ë@µBõÕo\x0007£[4<fÒd\x0017än\x0007J?^Ó©o\x0016jÐp°x Ùy:~øT¨ó\x00157X\x001aD\x001c,*^GJ¦T*±I&¢~½|ì39\x000f5È8Xt<xéUá6µÒ)Õ¨ý±²m\x001ejPr°Hy=©K­\x0004ç=ÉrÁæ\x0013\x0005\x0001\x0006-\x0007\x0007Ý¬p.[Ö9\x0005Í®ìXï6\x000f5¨9Xä<zÝ\x0019ð¤6RÍíèØ÷a\x001ejs0éylÉ5Æ\x000e2ÁrAÎÁ¤çÛìÎT´\x0003n\x001d¨æD}J
ÂAÏÑ¤çÍµ%±
c\x001b)
2p>*LoìcÌ¶¹»bfÐ´Ó\x0016ÿ ©ú\x0016ÿNÇÇÐü1ñÜÃ\x001dñùÓëHõ¿CâÓÔ^©íymÙ,Q¯öëô¡CßW/\x001e%Â\x0008
DQÏTuÃ»7\x0007¯@jó\x001còï|3@Ô\x0003Ñ4P*
YPo\êFèÁç´\x0019 ß\x0003y\x0003PÐJr(E\x001e×Yª\x001aÐ±Î(ôDa(©¹ÞF$Ô4\x0001áÜ»p(öDq(g1KÜ\x001c;½Ìk\x001fµº\x001cºM\x0013¥(Í\x0013ñÛä¸"íù\ªLZ±û`~Í\x000cQî²a¼ff¢óê¼*eà:Ê5¢Ò\x0013y"Î÷T-\x0004½VkxNlä¹\x000e<\x001cr!\x001eØ\x001f÷!JÒó·*:B\x000f^lÎ\x0010z=/Ø	²øá\x0001Û÷\x0001.¶¦Ð\x0011WW\x001a\x000cz
ókN\x0001\x0000R¾Á\x0014ÒýàÝÜ\x000cÒ Ø`lÌ[\x0019õfè\x0000r·ãbRHGCi¤A³Á ÚQÒ7û6ê/\x0005û«HhAµ©hª/ÖC°\x000cRÎºÜN°¦\x0006Ñ\x0006j×í¶¬6ØÊDwÔ+/\x000c×\x0006Ñ\x0006jû Ý7?\x000eI>n½C¢?fCO\x0013
¢
\x0006Õö­$¢\x001eÃëgSâxJÐEÂA%Ñ u"I£<ô¨ÈØ* êr36<nkñbHñá¿ÿþõþ¯O^Ýÿçï\x001fÿõÏou\x0016ªÛ×­AÎvò¬Èyäí"åXÃõÃ?¿~w÷ìÉ«»_^¿|~Ý1C\x0001±\x0007D;`ôòîéR\x000117áêw=\x0012äc±\x0002R\x000fHv@6okrÇÌZ¯¡S.\x0015Ï÷x~á\x0003«Õñ#í\x0017>=BÎÇl|#`è\x0001\x001d°xíwÂWyûÚz2Åkg>+`ì\x0001ã\x0012 ^ÁÔÅX9\x0000Þz¼dÆu\x001f\x0018õ¾?ë\x0013[
zßî¸á±\x0002æ\x001e0Û\x0001ÇÛE»¼#UIlKäTPd\x0004,=`Y\x0018Á|\x0019ÁÍ^f\x001fA5\x001eÃÓ»®\x0011°Û]cgVa!tíj²äFèµ÷N\x001dÂÛ¾1aÄ\x001eG"{íêËÓ>)êá
Ý­C\x001c\x0001{ Ô¸"\x0015=^Ö¯ÚÝÒ±W¸p\x0008$`$Ô¯!°aûFÚ[â©.Ñ\x00088\x0012°ÇÈ\x001d\x000c4Ô\x0001¿ÄîÍå¾\x000céC,\x0001{0#S\x001bB]()_ð¶p\x000cC0\x0001{4!>Õý\x0016ñhn¥ÉjÀ­C8xR\x0018Qg!IªR%\x0016OÉVÂ!ÀB@Í\x0007w\ûe\x001aäË+Ü\x00088Ä\x0013X\x0008(Üèë2¥\x0008 ¾â¹$ÓFC@Á\x000b?píCÄF\x00112é\x0004cYp\x0008(¸\x0010PbQ_µ\x000c^«Èò%#Æ\x001d³Ó¬ãÁÄ\x001ePøñDvÖ¬5A¦a{\x0019¨\x001b×Ûv8\x0004\x0014\\x0008(´5D¨msë²îøva%\x001c"
Ú#Jò®\x001d?á²[w¼7¯8D\x0014\(l4¯¹}e¯ùåèM­CDA{DI>ªÛræ3y"nmeoÞ¾â\x0010RÐ\x001eRRUiÍÖÒÖr \x0016o;Âã Øh\x0017l®\x0010×
¾;æèÛG¾ñ\x00069$»\x001c&Ô\x001aíJRT\x000f9\x0016o¼g ñ\x001aÄ.6@ñ37î\x0015±É\x0017±)·-\x0014\x001a2Ù2_U\x0006C\x000cOåq¹]rG\x001b°ýaÔçoÓHfm´ºeËÉl,¡¾CõÊæ\x0008\x001aV8·ýe\x0013ÑN¥®ù\x000f,þx¹é7ûß?½¿\x0015ªdofU"û\x001a±\x0005\x000e\x001bÛj.­{àõ÷õuÇy¥Á\x0006§i\x0018\x0012r
x3g§9aH\x000f½ýLÀP\x000fC³0Ùµi!)dß\x0010
\x0015}SP\x000bïiü,MRC:6$¾\x001c[â¿æÎ\x001e­]&iBO\x0013fiJ76÷M\x001b
j¯%¤\x001e{'hbO\x0013§¿\x000cL*²o«(¾%\x0015\x001fO8(©GI(A·Ï¤9üØíè¡RÄ	ÜÓäéÏ\x0014µ]
-²\x001fÃÜÜ\x0016eWhJOS¦Ç¦h©\x0013Õ)\x0003m
¥/ÕÝ\x0018úñ=þ\x0011\x001c/ÏºupÂSýRAC0<T<A3êð¬\x0010º£Æy\µ§áà¥\x0007Ïþs8\x0010Ã¬\x0012\x0007Èò\x0008ÇZ|°á´\x0012{ög]Â\x0019¤\x0018fµ¸þû¶\x001e ÛèÈãr¥mpÂÜÀ Å0«ÅÙ5`IÏºÂ42\x0000\x0019#Ã±©»¿4uÿá÷Ï>üþñúÎêZ*Ò\x001eÅI\x000e\x0007ø¤Dut||ýæÕ×/\x001fÁ\x001e\x0006gaS·& ¤/h^oì;µ\x0003¡\x001efaRÜ,¡\x0019fw\x0005Ý`¢¦\x0000ù|,¹¤ñ=¥á\x0004	ùNl~¿¿=ù\\x001eÜé\x001ai&ô4a¦nµ²|((ÀíV~ú\x0002Çk·9ØÓÄY\x001aÔtr\x00006ôØ/\x000e<\x0000ïc\x0003ÇýÄ$MêiÒô$ÖÈ\x0000I¯ªDè¼)ÇÌIÜÓäY\x001aHê\x0007Ü{?Í:Mo¡a¦ô4ez\x0016&Õq£\Y¬\x0019c¾\x001c7Ås0]\x000cïz¨O
jÒ!p)`±i½vØî\x0005gTâi)®*
\x000e¡VÿP	­SUXÃ\x0019´\x0018¦Å¸n¸4\x001d;F¶+ßp²Æ©@'÷Å9AaZ÷Ëó}·ò\x000cÊÔºg¥5AaZ]§ö::Ú\x001d©Ç9e¬Mâ\x000cz\x000cÓì õ[\x000b­Ä®0Í\x000eÅµÐ	 Ã´";TÏ5H^2\x000cÙMAGÇûã}Å\x001cÎ È0+É\x0015£-ôzÊ\x000b²²Ôº¯êÎÚà\x000c\x000c³ÅóÝ^ç\x0000r©ãTvÂév\x000egdÕd¼\x0018@\x0002ÛqÈà¾ÖxºÂÁAqV1«C\x0010äÂÖ.û§RÇ0n;¶D3h2Îjrl¹']GI9CírÁ­ÇD\x0007Çíñ¬$crmKZ²\Ôã\x0002\>ÕÒ²ÂAqV¹uÇ#¢Ã]\x001e\x0015çx\x0008Ä\x0019$\x0019g%;à\x0004­jHò­¨\x0015\x0015²\x001dÉ\x0012Í È8«ÈÀ\x001a¡MdI÷äo¨³v|ÀAqV9\x00196i>3©/g
ªú­NÍüæh\x0006AÆYAæú.
æ5>Ha\ýT¹)òÒF\x0010\x0007EÆiE&ëõ-!^¼]«Në2Ï~)@à È8«Èõ0ô0Su¨EòãmÅ\x001c\x000b
rLÓrÌO`R¼Ä% 
ØÎVùh{;3( M+ Ð\x0005'/Z=fé
iýRK\x0006É¡iÉq^Sò¹ÜD\x00040ºVývÊX£\x0019Ö8Í®q(Qòî¶`¥Ó¸å§.N\x001a\x0016\x0015Í.*ÈÚ£ÒèÍ\x0012Ûç(Ì)?lÆ\x000fóØÏÎcÞiéi¦\x001e\x001fôu(ÄS\x0013Ñ9a\x001eûÙy\x000c)iËLÈI7]ØúÖxtUÄ\x0019/fç1°â$¼£iTÁ¬ÿçpì§'rv½\x0014¼\x001e=«þèÜ!ëõÒÑ·Ýw¾í_+Ð\x001fÿÏ×÷l®t­_o·ý¶¾S[¿.½î¯ÑêjëInúñú×ÿx÷üªËÂQ\x000fG68í<w\x0005Øá¤Ë^	ÝÉx\x0015.ôpÁ\x0002Gl%½ÁÒ\x001aOJ©/±;®²Å-\x001aØ¸\x0006~RòÜ(VØv¡¯ó÷ZËÎy¸ÔÃ%ËÀT
»º¿*
ì¼$\x0000ûñö\x0019{¶l\x0019¸¨N'>úÍâábk¯ñZûºy¸ÒÃ\x0015ÛÀIç\x000eKQGNÛÄö¥ÄpÝcoh>5tI39|Ú»°oC§¹;\x001cmo\x001bUÎ$sNßX½\x000fÛão?tÁõé0«t8Ð¡®h7Q\x000eGûZm} úêÇU´AÁ"Á\x0004\x001a\x001f<\x0017×îpló*ëájØy8?Ày\x000brßªgû.h£Ów|××U­Ò
ñ\x0001,\x0001\x0002ZQÏ[\x001b­Nõ+Üíßu\x0008\x0010`\x0010èÔÀs34uF}¬ÿÈÍá\x000b\x0008\x0001\x0010\x0011ØqÃ\x000b]Ø©Ö,æc\x0004\x000c1\x0002,AÂ\x0015ÕáÀ
âELtÒ%¸}ä\x0010\x0001\x0018\x0011I¬\x000b5F\x0000ì#×Ä¤ou±\x0008C@C\x0008õ\x0018'yÐ\x0001tÃ®UÝbÝõÓótC@C\x0008Y[Ì¹°\x001bðot©mÊÕÖµótC@C\x0008Í §Òù§ú]5³\x000cÜÍbC@C\x0008I­Ê]\x0008¸m ¶S[pp©æ*Ý\x0010%Ð\x0010%Â%a1Ä­9ëþYµZ
¯6\x001b\x0004\x001aDÝkyE¨ñ5ÒÅÖ.ö;Ì¹!H !H0\ï³\x0004´lv:µËù<Ý\x0010$Ð\x0012$b\x0011:t{.ÀFç[kâ.Ýhn\x0008\x0012h\x0008\x0012ü5÷\x0018\x0011¹S±|×á%Ü.uC@K­KwHysæÜèZ95Ý>t4\x00081Y8\x0014Iw\x000eeo?²Á©ó\x0016øÛ\x000f¯4^IX´ßbö­Iý[Q?Óy½ý«¿áf%¦ANÈ"'\x0001Të8³>ÊõZPOi7+1
+,+Ö7×ÀÈí¥òNG­\x0007u
7Hq	°úI.i¦\x001fï+ß×¿þýýç\x000f×S\x0018= 6¸`³§ûµ7hv'§·s?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þýìîù.KÄÉy¶âd¦ÆÑ¡¶\x0012³`Ì»ë»«ÛÛË÷\x001fî¸¶ææúêßÏîn\x000e´0»jØÕ:v\x000cÖP^SËR&Rzlå<M±Ý6ìv\x0015{Ó\x0015^¡ÕF°\x0012\x00058»'µ»kØÝ:v\x000cDÊÂ9jkM\x0018ág\x0015\x0006kÙeÃ.×ÙÝç	ëhwuNfÇPÌhV¢û\x0006Ý¯C\x0007³\x0007ÊÊùR\x0002fç9\x001fóÞÃuì\x0019µ\x000eÞÓ»\x000bçè¢\x001dî9d.ôìá½\x0012^·ðz\x001d¼
¹3\x0015àe©Ö"\x001c:¢>Â	áM{Àu»ÕiÖÀwØ_Bw¬3.Ô,j¼\x0012¾=%åÊcÒÊ¬2÷E\x0019ßpu·Ï ]	ß\x001erå9ièitG.¤ÆÑ\x001d¼läI-ï[x¿rÙ\x0008®[À´/÷ß[é\x0018ÌIàÁIÒ³zÌ¨_ìÃKRÐÙüz8ù\x0010\x0005\x0017×[l@Ì²ÔèLiÖ]oäû¤sñöÐ\x000b.³UÓl­L³]Â\x0016¥ôT¦*\x001bíKOWÒ
_ÁV5JElMè²[<(\x0011Õ5©íÕ:upÙr6ÛØÍvÚ-4v£	ÅC:×ÚÍ5l®
ÖáU\x000b0l¶2~PÏËc:ÑOê:?ii'³ÚrÐØÒ vMv^Îæ\x001b³ùn³q­ö|\x0013Y\x0017x¹©]9ålÁÕlÁõn<åÍÊrT[¹\x0013Ä®~\x0007oÈ|Õ\\x0019v©5Ï=°Å;ÚUC²MN\x001aBÈ?;áHPÏÂKÒ°Ýxö\z\x001diáL\x0017ÜÔ1oeÉKXcÊWÝ5º¤\x0003.´p¡wÁQù
çj^pË·\x000ft²ÉØ°ÉØ÷U-³IÁ£--»ê\x0001Å}V U\x0015UVJª\x0016]\x000bp:²>(%\x0010¶\x000cc»2"\x001dh®Eë;B¢`Å"\x0013#7\x001c[Çm>î\x001a´\x001c®õBd\x001b"PO0Sã<·ÆZ_\x0017vêS-\ß¥å
ÎüÈ\x0013Å\x000fá}êÃª«^êvê¾}
@
g(°ãbïÄ<ìr8Û.9Û·äJ¾\x0005à\x0017\ü\x0005n×D»åp®Ýª®g«åbÑ1
®\x001c#¾\x0008\x0015û]eh\x001dpígu}Õ9îh7Óø^[ÜK¿s\x0000òr8ßÜøø³Órä(a\x0015Ú´Y=Ö]	Êåp±½òcÏ\x001f*Î/Âå0¥FÎìÈCuÀµ\x001b"öm\x0008ÇihàÑT5cd¹×y©MÙ#µïê¦ÚB=ùJExÏëUÇ\x0012¾ë\r\x0006id83÷GÖZ.¶pþ+ÇuÓ;ÕsÅ¨Uk6«ÒígÕ}\x0015\x0005pãÔ¾\x0018H\x0001§TÛUg°Ò­åtå¢0¥&üvªôVâ[\x0005iáL\x001f\x001cìP>dÿÜMu{®Û%§;\x001c¼£yÉ©éò*/B¯Ö\x001dÁ.TE\x0001t}mºø\x0014
\x000f«0]¦X¶Ä®«\x001enÆ\x0007\x001e]\x0017\x001f¸t\\x000f\x001cøáÅY\x0016ïç=O\x000bá¤õ)\x0001Zé/ûW²è/¿½zùþøõáûA4,ÞÏMÑI­,W*sÿ{×îgãû³÷×÷wW\x001f.ïÒÕúË¾Ò_^H§\x0002v\x0002%</¸HÙ\x0004\x000eDãÂJ>Ýðé^>Å1CÓP(é\x001a¸53ÎòÅýx¡Á\x000b½xEx]\x0019FfE´z~õ"¼Í_¦ê"\x000e©ÛÏn^~þüøõ\x0010 ¤\x001a\x0018HÅO\x0005ËÕ\x0019[Ï~\x0016±¸½¾óîêÃQ¾é±ùÒk§\x000fµ52\x001fÜýT"­\x0002=\x0013mÏìå³¶µ\x001fþîã\x0013"Ótð)¯H\x001bÂ¢
G	]\x000eqN%-pûFÎÿãÓó÷Cµ Q£l(©©\x0008vÝ£	Eh\x0016¡4ü?^ßÜ]\x001e*\ÉxUW8àµÓàùs]ðhÖa´ü`o²oÑ2¼ª7\x0008ñ¤é4Ê	\x0010ßy\x0003G|£P{½Zg?é\x001aû¥\x0014_\x0001]
E@ËìÈ×Ïéækì_*k=«\x0018e\x0019~\x0000ç\x001e9\x0006Ê}³ \x0016\x0002N\x000f´\x0004\x0018]/`ÈÁ\x001eE*Î|äê[ì3^gAe/¬Lï\x0017A£í1Ì_\x0018£\x0015Y\x0004K}£ª\x0001jÕ|â-ê\x0002T¬ú\x000b<22ú¢\x001f'Æ?±G¯\x0016G=Êâ8ß<¡Öø¡ã\x0019zn±ç>»/8÷[lvûÍ7×(2~\x0014ljÛD0i{Èpú](]JäJ[Z?°·fL5&S}6Åf&ÉdéÒë#ÖØÌ56s]6s¢tKXÃJÒ¯éæMõ]d¡!\x000b]dg¼Í,ß\x0013ë\x0016lwH`)oÈ|\x0017¡\x0018\x000eçx4¡4îøÁ¯ªÉ«\x001fp5Lc{¾\x0001Ú·çFH\x000e1MPWª%7ÎÕØz>M3\x000fw¹\x0005¶ÛÃ§FBZ\x0008\x0010-\x0008\Î\x0016|QàÖ¬\x0003¤(*áÆ¬c
ìc\x0013Yn\x0010Ù,k\x001c+Á»ÀY¾¿-6l±Mó>sW\x0012e«ñ;§	-eS
êdó\x0014|\x00027PTßÕé­Ý9%j)nÖî[oQTl\x001aä@w¨¦\x000crØùÌ^Â\x0016ÿÚ\x0008©ãËÉlg·\x000f\Z~ð\x0019\x000bL\x0014\x0005Ð8ÿgÀ\x0015ño³{«Ý^R9ùQÂjÄ\x0016\x0010Ö#¶\x0016"êRØ¤óÂüÔv\x0005Ñ¯$¬\x0002)@X\x000f²ZJ¨yÒÖEµ\x0018µ#ÐìÜ·\x001dõ¬fuô"\x0006VèC¯'³">/%êG¬¼a¬9\x0013Ý¦$@ñmKò|&"÷=ïáé@4³Ú?Ü­äÝ6_\x001e6/=rÀ&»y((§¹\x0000
§®Ñ\x000b7ª}jºxyq¿T1ØuÃ®×±»W¨,Ç}$\x001aZô4ÂVÍ\x0013²WC ÝÅUì¨ÞG\x000fø\x0004ØKQR{e\x0007w²ïÖª p/kp/W£\x000b\x0019=8.1\x000eA\x0015\x0005Â}ª#6¦±9þ\Ã®\x0015\x0007#"µ¿\x0004Ë\x000fi\x001bqJrß¬ôT^¼\3xäC%XVËÓbwg\x000c½Q\x0019\x0003Æ®[0ÛÔ°ý].V»0©§á$ì*w\x0006NìpUU?o~Û|\x0007ðCg7J«jòªázáéd;ÈÚ]×øæO\x0017w@zÍ4l¦
§ªÓ|%¥¸0\x001a'È2ßY.µÍ5vs]v\x000bÂÒÀ4²kÔ2Á>5Î\x000b^AVEøÌÛ.2¸%uÔúÈ\x0013´ìSoÍ®éeò~D·éÂ\x0013ÜSÝâéÕxóøÊñ»çÍ\x001f\x000fÏeÒÓb\x001d\x0008t
³fE)ÆÂs4ÈÌÚ\x001bîn.>]ÞO\x000b[ª3u5\x0019\x000f¨±jZ(Î\x0002jËD4\x001c[0³\x0017Õ\x0008õ\x0006ÎËÆÖ\x0017ØG¶®»IÞ?}þ¼y~|:¬FûÉfdp»ù³\x0011\x0012u\x0013Éûëwï.n®®÷glT5¤jÔåw4^H)PHY¹\x0000õ¨÷÷§-'­;»ì«yc×2R84§%5»(ã¹ZRë¸¿%j9©kHçPËH½Í\x0005OH*È\x0015WÓËAk¿¿?·´ùúnèë«O\x0003 
î
ã\x0001DjfÂ²c¤¾±é¼?k¡M\x0003÷<Gl\x0002dSÃ;ÊØSØÔ76õC6\x0005\x000f>~\x0008Y\¡!Óý-Ë9ccÑ8¶\.h@P.hP\x0013ç^æ\x000eNÙpÊ¡\x0013*ûü\x000eÇqf8Ë({íg\x0011Ò>R\x001cK\x0002WS9<\x001fd=ràýÿyùëçÇoG\x0005YI%ßÁ\x0015EoXS2ÌQÌÚM§\x0003goß]Ý\x001eªMÊÒ5®\x0011+\x001ci.\x0002zz¤ò\x0018yh/Þ´+\x0019«&\x0007¯¤nFÇ\x001a\x0001£\x00142ñ£\x000cûf7,fô
£\x001f`$ü\x0018©HÎp¢ô\x0004Z×X»ÓsôèS£,;Ugr\x000c\x001a\x0018gññ~FÛì\x0018;°eÐ÷ %\x001dXÊÊbF¿v5VÊ:+'ö":Í­èÒ±üæ
a6¥¡\x001fÑ5Ú
lj/§M­JÑ¼E§Ú¬eô
£\x001f`\x000cÛå`/SÛ^\x000e\x001eµöSf5Õ\x0018¦ÃQ[Åó[ór4+wLÝr\x0007¸\x0018ØÖ¡L4w¥\x001cÜðÑ(fôý²9\x001añg'a/qÎ\x001bF£As£\x001a\x0017ûÃj\É\x0008;æ¯?%]¢z×àßtoH!\x0005\x0004ÞyQrS\x0008bø\x0018äTL\x001c¼iRÀ\x0003\x00183ûÃ\x000eó$,õÃ\x000fIð:¶â
ð]UúZçôu?e,w6Öèj¹|\x001f³UÐM)\x001bJ9BYÆ\x001f;\x0015ø Ä
ÄÛMÝÍ\x0007#_¼w\x0006X\x000f¥\x0012¶Í;Á_ä¼\x0013\x001azüõëÃóa<ZË-ãpdRv\x001b\x000bEØ!ìJÝaûÛ\x000f7\qÆ3
éÄs=\x001fë5Î\x0015ÎW6ÛÏÝuäñ¦À4âiÙk½P4;¼dM\x001d«&í	·+¼/É¡ÈOÐ<fî_øõë@¦å\x0011Xf\Ú>\x0005µ\x0007Ú0\x0016\x000e·\x001f\x000eÆ13\x0006r \x0012¶
ëxr\x0008Ø;Q¥¡}{ú\x0017±ézWWºb9Ê\x0016§m+QkÙ³6\x0018×Ux\x0017×\x0018NÆp:t\x0019.ÈxÎÚ¨YMjBÃ§Þï\x0013îX\x0006\x0017\x0015gî.G©`Ë)\x0016±)p\x00007\x001fþ½\x0010Nªù\x001d¬ø\x000eæ¤×ËóÑf\x001eÃ·¯/Í¦\\x0018nòèûáñL\x0016j²ÐKÆw.XÌ%Õ>}äE\ÒÔ\Òô,Ö\x0006`&²|-£ªplñ*6Û°Ù.6çÊÕ\x001a¸äáëb7­÷I/bf
 [;Sà¸Ýà¡Ic51ÐÍÍ¶³'p9oÐ|\x000fZ\x0014í82Bs­¤¿gØÚZ&æI"AI¢oß6¿rêíËïóY«N
Ö¯s>+\x0006®\x0003Ñ}¼¸½½xËÉ·÷\x001fòi[óaiA\x000f\x001f¾,¼%>}.yÙWCÙÏç\x001a>×ÏÇµ±XUøJ\x0019åJóÆ|¦×|*\x0010¯H'@Þ\x0012ðÍàn¾*DÿåUçò\x0013Zyá_õ¥\x001c[\x0004^~ópÿÀçm^»ù\x0013§×n\x0017&8êDYB\x001bkÃr6¨¤2&ÊZ¯\x0008¾r9^>=½üú·¿·$óBÒä­\x001bÉS[Ã\\x000fNO×÷oÿr\x0014«\x0016×3¯ªÑ>\x000b¸J8\x001f× U\x0018pQËÏç³vqÙËvp\x0005Y\x001e_·ë¶Y\x0015\x001a¬Ðc.U$§ÀÃtl.U¸vÉ,æ
Wìá¼¼ðµÅcò¦ao»§3,ÃªNÞhêû~¹\x0000¡ávD0×4nC¾Ë6\¶\x000b«C\x001cÉL9R	Öºí\x0013»T\x0013\x0018kÏ­Ì\x0014\x001b¦ØÃ¤\x0015®ó¬Êe¸ñº\x0008r\x0002TÜ9¹d­¤j\x000e.ü¹\x001cÌ\x0019.³\x0006·×¼E`Më\x00023ÍÑ´p{Àô4Ì4¶u,Ú\x0017»ÞÉK¹|Ëå»¸\©Á\x0000\x001cÅ"µ²ë¡·KÉöH=g*ØËRÓ\x0001¸Cd¹?\x0008§¹\x0018LÆyãR¬\x001bÐõþôðüóoX~\x0018Oq­¼ÕsP:iöZîluA\x000füÓå
vW\x001dz dÊª+\x0002(ë®Å\x0016LGgqç¼\x001bJ\Kû]\x0002	}UÑyl:_S\x001aUîu ¤ü\x0004ê«\x0016ÌÝí\x001b=¦Á4#°?X2\x0014üJr´e=0/v\x001aÁ´¦Æ´f\x0004S\x0017N£¹C¬\x0014»\x0004m×\x001bsºÍ\x0012¥\x001b¡T	¢(\x001bÇ·­Ök¦MçÏÇ¿x¥êDî·³wO_\x000f7x{¯q¤æ¦" å»DÝÕ#·gï®®?\x001cj5ÉxU\x0011;âá±Ýç"õ\x0010§)§e\x0019s©v§ÊâÖz¡ÓzÎÒt;dFXa?°\x0017{*	\x0016âÕë§ë²ãxðñY\x0006Owïy«Åb<\x0011æµK!Õ.]Àÿý\x000cw(/\x000f\x000f¼`\x0016ÓÆ`\x0018*9.æì¬¶î\x0002þ!óÝáßÝ¿[¨jDÕhJ\x0001®mÇâ{ÎÎí\x0011D]#ê~+s6"\x000fØÐS såÂ\x0011>Só\x0011\x0013ªé+G.î7å+;½\x001aÑÖvÄ$>\x0006!®«\x0002#¯¬Ö/DW#º\x0011+ZFL\x001fYqúÎa5¢¯\x0011ý\x0015\x0005÷Ð\x0016í»íIs×\x00120ô\x001bQO»Y\x0016ïÆ±Ãí¬^½[ª÷SÈ>X'£\x0012e-Â³\x0013zº¬Åya|\x000f£Ôb^- Rµ@5ë/\x0000Å\x0003\È9*\x0015£\ZUõNÎ'»V3¸~¸|\x000få\x0003ÇY«^\x000e`Ur5\x0018Ò¿	|GÉòÚÊÍ]ÚNP%B[Î\x0002Q©1,f\x0004ï\x0015}à¯nC(
~»Üî\x0005
~\x000cç\x001a8×\x0007§Tqs\x0002¼:QÔqý®Öø%ê:Îëb+cñöéù×ÍáÁ)ZEsO\x0013¦ ô<¬NnËÿýÒ·go¯oÞ^^\x001cÂ®!t½Rdaf$ä\x0015¨àÞã\x0016é¹j?¡jl¨ºm\x0008Þ+OvËn%ÔZk@Ýàé^<\x0015¨î\x0019ðP&ä9É2ôRÅ\x000f©\x000eÂØ\x0010ÆnBx	x\x001eë§Ïun\x0016°Ñ\x0007&{ä-\x0012ÊÖ²ßZðt$o
Eç-\x001dWÒÈæ\x000eD×"º~DËMa8,Î\x0015-Iù\x0018)vK\x001f,Aù¯\x0018'ÞÔIsºN~|úú}óõáûa=°T\x0016¨wÍxÖ5ÑòÕ\x0017ç:+Óòãõ»\x000fw\x0007UÁ5Ø5Ø!Öç7\x0000*PSW\x0003øÜh5ç5Z
\x0017­HâRÔ(\x0004ßÎÍç9p±
óKpU\x0015ÀzNNJµ	G2ªyµä kkW9hØèËzµÝÞÔ\x001aL°æ\x0014ëUùÐì-\x001fF`¥#m¨Y×óà?£fUÇc UÅ\x001dj5dU\x0019Üy$ÝÈª>ðY¥XgTégn%üEí\x001dÝn^>\x001fÔæµ2RÝ¢U,Ö+\x0015¸©Ý÷úÙíÅý»CÂ¼\x0004&\x001b0Ù\x0003¦<kÊZ"ÈÅ\x00158óÀv{lKÁl\x0003f;Á4\x000fs.\x0005)bÉæ­Ad®!s]d$dÜæ=©\x000c6f1\x001bgïA\x001bó{^\x0007\x001f\x001fÖ\x0015«sßÔÊº2eApbÃz½ûyðñòæ`U1³¹Íu±ÁíL\x0001xdÜwè\x0015³ÝÏªlµ²wl½°YNJ*«\x0012UÔÙÄ:6Ó°.6MO*`sSqL(vKwö²ÙÍö±y\x001e¢lÕaÊØPûbMû6`\x000c\x0001ã«/¿o¾\x0015åt9<~=÷ÁBlÅãÉ\x0015Ïk\x0016¾Ôd\x000bÛ>\x0006®Þcá\x0013W/¦ÛáêÃÁsF5j\x001cCµÔQ*M\x001cw\x0010¬½Æ<	ªl¬*ÇÌZÉiFÅ}SÂM¬Îµ8ù\x0014q\x001aaMÉ´¬Ë¢¹>O8Í6~¶JGYMÃjX]¤99ðo\x0011ç5jy¹°VÙilü\x0016C¬§æ5OM\x0014Êã5àOÃÚl-3¶·.Ú<ÁsI:Z¾ì­°V\x0019`ÔrC¬Êõ:Õ÷¥~pb=ÉÖòÍÖòc[K[¸*qÌ\x0019UÓÃ¿Õ1ê,ð<ÌZ)3eÚÍ\x0008®ä\x000c;\x0004NX³eYGkæ\x00116#l-ê»Í\x0011¥#CÍu\x0012Þm|eé¼²xÒìÇ|wqP)fï·*û\x0008³öO\x000fÈ³Ä¢i\x0011â\x0011ï,'¹9Þ]Bf¹ªâê\x0012ÿvY3óTÌÚ3[n\x0001©Æ\x001b9YVÍ_¶kcÃ\x001caM\\x0014³£ØS\\x0000éeÜ×\x001bÒÁlg©Gø\x000bL=Núü@ý\x001ei=¼Ï¢à\x000c\x0001\x0017\x0016\x0017\x001f\x001aË3É£ß;(\x0002ß#èÛ\x0005 R× R\x000fòY\x000b¤Ë2<\x0011)=Q.Ò*%`m#òºT;`tä\x0018ÔÏ\x001cÝ {ER5jRi\x0016FöRL¯\x0015>\x000fbÏ \x001a³§mHí=\x00156©g{ÆÒcí¸9Îå(ÆH«!@ÚÎ\x000bYH
¨\´á¥)/gÃ"­qÞÌÜóå¹®°Þ«\x0002hìW¿øúóãÃ×³»çÍCÞ\x0015&Mv¤\x0014ï8²iÃ«àìâÃ«Ë\x000fgw7\x0017ï\x000fØH]CêHÁ«¢´>ª\x000e\x0007"<&ÆF±»?q!©K¤fò¯0\x000f?%Ë?<¼üí eUÑ\x0008ºÿU \x0014¥5ó¸WþÞ\x001f.ï<
\x0015\x001a¨Ð\x0001ÉHpù½²Ü`g¼Ù¹\x0004\x0017!Å\x0006)v òþP\x0018\Ê'¢BéT¢Ú=.é\x00080³Ð0¯ª£\x0010Ùó÷Íó¡jò¨`íGïd\x0019£S$ì¥\x000c»\x000f³»C\x0005å\x0019¯
ø\x0002Ý|>ïULâ
Ö<\x0001À\x0018wëø.åS­ùúí'Ïµ!>\x0012Ð\x0003ó±¶o\x0008ÑQ:aÅ¬Ê\x000f\x0008tí½Óxóõáùñ¸Þ\x0012\x0015/a8º¯\x0015_\x001eN}îØ{8/>\Þ\\x001dlØUé1YI§ª¤â;	7/Ñ£õââç\x0019¥[U\x001c¼öûd¦
Ò*¡Úà>üE
îWý\x000bºþ±\x001a;­·4aGENÜYïõÞ¾Øãÿ&ÌÒà&´\x0013Ï^ÎþüòÓãç\x001fÚ\x0004K"ÒÂÂ5\x001cèÅ('Ñª°;³töçû×Wï\x000e}ä\
TEbDxe&Á×O/~y~úr\x0010\x0010U®©\x001615Òe\x0011¹¢ÊÝ\x0013¯¯ïß]ÿpsýþòÕÏ_6ß¾??\x0011F[\x0013FÛK¨Å¹£ÆXÜ¢u\x0002§øÎÑSË\x0001¥jL(U¯
],ý§F$iäôàöaªlß)ÜÜX\x0005[\x0010ÑË^D\x001b¸\x0001N{@\x0002\x0019Ry>pæömÄì\x0000nñt	Ûé\x001bÃ¹fÛò¤Ðüíìãó¿þy°¾A)Íí¬Ï?µ²\Ñ©ç²ÒU\x001663ß}Ä\x0019ûmXëÏ
¬r1^\x000caÀüò\x0013ÕºÓü¢Öó\x0008ö m%a´ZÑzs®,ÑJa+§¸7D¸·Âs\x0011­®-Þ¿Àâí7¾eÒÏOp)\x001e+qeÈ$ÒÙsj2w\:?Þ¼»¾Íï®áFLIøÝëùbÍ\x0017»ùð©\x0003°ü¹Ë·¢\x000cÜ­sqÆ\x0008\x0012Æ45\x0002¯á/rÀóÓãßáQòøp¸â*f-ö\\x0014Vd\x000c_5RÍGZÜ\_ý;¼E®.ïÿÒ3 Õ\x0000©\x000e \x001cBj©\x0013î\x0016\x000c0\x001cÝ\x0005/v\x0016à_Hd\x001b"ÛCä#WÏàµb¸K\x0007­H1¯Þ\Fä\x001a"×E$òüB »\x0016.#µM¼[J$\x001b"Ù±¤Êr\x0014X¸'øíQy"
óReD¾!ò\x001dDi\x001då{ÁùÈ÷+,\x001fº¼àöñ\x0003DR5Dé^\x0004n\x0013\x00157álLnwbI\x0016#ô<î·\x000cI·Hº\x0007É«ì\x0000\x0012¼)¤ãDþ$:7dÚ\x0003Éô,îüØÏV[Çqk'#éyê2¤ö\x0000]'¦ö ´â\x0011Wãp¸,nÙ\x001e\x0000²ë\x0004@Õ·üÝl\x0014¼ºáI½G\x001d·jò!ù\x0016Éw}7\x001e0dñUz]-\x0013ÉdË³Þ{ù/r1×ô\x001eM÷ðËÙÍÃ\x001f\x000fÏ_¾b\x0001\x00157ÚÌ÷åéûãÃ3\x0012zÔ'\x0003¾`ÑßÆìVpÀéÎñ:uþ¼¿¾»º¼©ß¦é>¾?»¹ütyÁÍ=\x000f¬\x0014:Z»5ÔÎäQ	Áê(ó\x0010Ñ4§ÉÃIÉéó\x0012¹\x0015kÈÑ\x001fÏà©¦\x0000ìíþD=\x0005+NA­\x001ajµÚJ\x001a³ö9;\x0003ä\x0016\x001e\x0019D>©µÜëÜë5ö\x000e¤ð\x0019Pö.¿×pc [99*' §°.\x0007¹ÆæÂf÷! |x\x000e(\x0000¹Æz³D.ä	×¸$Í	>SdXn)çÌ7¨V
%è`.õ\x0013 ÆèÒüÿÂêI¢Øé$ÇZ½$Áúôò=\x000bm^R\x0013Ú~^ïÏâEpö9\x0015lµD5sÄ\x0005ðiú\x0001áÞ\ßße1±\x000bøÇ½­h\x0013£\x0014
cÒ¤îb\x000cd>QëæÁ¡K!ÅzHÕ\x001aRu\x001b\x0012Û`%\x0019RÙÖÕø°
\x000c)ìZHÛBÚ~HpMSº\x0000 Ï±\x0012
þ6¶õ¹t\x0003nÝ{ÝÞ5I²\x000fÒÌ\x0017Bª\x001c\x0007H}È>Ì/^H[ÝmØV['dä{A¡j¥%H|v\x0000£U«Ê0cl\x0019c/#&7R\x0004\x0018Q)Ø&F|e!ß]ÝÎ7(wÝ	i}Nßc»_9\x0000N\x0012¤¶«!}kIßoIçS!\x00170Û²ÑÊ\x0010£
k\x0019
5£Kz}=\x0001þ÷ÑÂØÈÌè] \x0015Yö2f×àÏ^FEõD\x0001\x001b\x0010sF\x001c #VÅ&H³v×øö¶ñÝ·MÀ°¬&F¢3ÒHòU%<jæ^v7¤m!m?$ÊU¸\x000c)c\x000e#ã\x0008R\x001b	RÄµW¢÷ÍÄÝ4ý (¬Ò¤­ð\x0019\x0012\x0013ÿ+!l ñg7¤ç%i\x000ci¢%\x0003äøV\\x000bi{\x001bvBJár59B\x001a¾m¬0!×[Ò7;µöB
òÚ\x0001RÐS	\x001eJä¦ÉPMJ\x001c¢Lå=Æ²\x0006»%÷ï%Óð¢\x0004©¶ÞsÝª¹n¢ê½nÒ\x001cOMÔ*\x0017ã"¤³\x000c\x0019çïnÈö,ýg9ÜÌX¾ ÊÍsZ:\x0015\x0015A
±ö0\x0007ÓQ¹xeËM·1©â\x0016©Ïµá/>\x0019síQ	þcË\x000ee'§Ç9t¼5§²î\x0019xÁ±·fäø\x001e££ù/rt \x001fÎn¿?o¾ýôôòüë\x0003\x0013ÜÝTÕ\x0016°Î(g·ÞxÂÄ\x001cáóòòìöîæâöõõýÍÛã¤ª%Uý¤Qä­sNæØ©V!eÓ:9uw®à\x000c±á\x000c±ÓÇ(è
ÒXvké2BI+\x001dè\x0015¨Ñ6¨Ñ||åW\x0019Õ</\x0008Çç½¤1»\x001aT9]âÏ\x0001Ð(sI\x0012f¥bNy¦ú)Z¦X´\x001eUkY£&éÉnT²øiã\x001b%\x0003­TéÌ÷&\x000eµÚs@u¡úf¥j?°R.c\x0002T\x001cÇI£¢ÏoÙsDu¶{Jì©4¤0âP\x0001z
)x\x0011gÿØ²Çï"m·\x001eÚR\x0012G\x0015æªpr]¾÷Ù\x0001ÕVø\x0013\x001c¨F4FÅý¨¨vÃø¨ÅïàtÒN3ê)¾¿u¡FÅ\x0003¨ÑæÑWX«\x0012h¥¦«>:\x0014Ð[O\x001a[Ò8B
÷S®_
à;IúþÊ\x0019:ý­
zGÚê¯QñçQ£§±±pRÑé\x001f$í*íÚãáw¡æüÇ#¨/¡b}\x0010¡*z{ê*sºÔ¶FµcF¥J& Õx8&'8ª\ëú¹!×O£ï	ÕSÚT\x0006S@OÀé[ú!FkyÓÊ¬8&õtOy½ï×êesù§\x00155`RÑ\x000f\x0006\x0007þj:¨4½¢´÷þ\x0004VõÒ·¨#Võfê\x0006'\x0005/ÕÊ`A:¨RRt=ªnQõÐ\x0002ð>ßþÆI+§ð*?î\x000bt¶ç\x001f<§d¼B
RÅ×\x0014v\x0011¨;Á5åMlAGî~T3$/\x0015Ç¤;²©¡8\x000eRàò¶y÷y;ðî\x000bIâÕÑ
\x001cã	6â«À\x0015¨¡ÝþahûKE\x0000\x0015\x001cjCVµ)ÁàE%¥s5jú=À
.5eå±ó\x0002\x0014ÑqÑtvý®ª]¬é÷\x0000«'A\x001b`E§*ß\x0000\x0000<´Üúû_*7cuC¬Ótxr¾3:C%\x0003J»õ;KjÕ²j5Ä
7k$Vîô\x0001Ö@	d³70Ùêg¨CoU,4ò\x0019U©È§@äÇ*\x0016À¬Æ·*ãGN,/ÈIP«EÌâú\x0014\v\x0002o\x0015ÐÌ\x000cÕ\x000c ¢°Í¤ÒÒ\x0013PÁvâJ®\x0013Ü\x0002Ò6N¿\x0007ªe)òÓ¤\x0010Fõ\E¤×ß­pS7N@ú=öýÉ¨øn%Pí¸:n_ÁC\x0017©\x000f-©\x001fy­b>\x000e\x0000®\x0015±\x001a.Í²Â5´K\x0015\x000f°\x001a%¶±v/f
\x0003¬zà\x000b\x000bÞ°§X\x0001Q¶¬qÄ\x00110¨eQ¥g\x0000Õ±Y«©6ã¨NÌãÿCûÊ
J\x0000X´pd³²Uõú\x0018\x0000é\x0019éÐ¶GjÔT-\x001bÏ¥"«\x0006Å\x001bK­\x000f­\x0001±\x000e-V«)YKI²\x0017\hjÂ)ì:;YÝØÉ*\x0003¬¬V¾°*IfU'ØVÞ¶>«·#>+Ö\x001dÄô¾²8Ý5g÷\x00146µdÜ
ÖÐ:\x0001>\x000c9\x0001¡ÜWN\x0019zµ*´Ò\x0012k<]jW@P#+À¢\x001a\x0010±zSÊ¢%7ÀW×YÁmk3Aø{ n9µÄê\x0004n²|^\x0019còÙj?ÁsPiÝä\x0002Òï\x0001V\x001cR\x001fr\x0005}jC
±\x0013D\x0014ìÐ\x0016Õ\x001cX\x0018\x000eÊ%H°³\x001cW:\x0018
öU\x0017ö°zÕ\x001c\x0003é÷@6\x0008\x0013+2ÇØ<w¹ <H*2´Êª\x0013ØÕkÑ²ê­¥À®ÙkÁÖe~·À£0«'p\x0005MÍXG,x¤Rµ»ÃÚ\¤|\x001aÀÒlâ\x0004Ï×°âïj\x0000IJøÁ¡H\x0005\x001dYpÑ\x001a8ß¾eð]¥Zð¯²-¢í8ô³-¡d[ìºE«²Êô,« 4\x001a¨jõ·'à:Üõà%¾µ\x001d­\x0003Æ¦;ÝZ²Ô!6:üx
ÿÒvÌ
Ë\x0015+þ\x001c¡Å?g3-*4f\Å	w´ÃN;õ!%\lD\x001aÁÅò\x0015²mLºî\x0000\x0006\x0013gXs\x001aÛV\x0004ëÇ`s¨%ÛVP\x0018ÂùDØª\x001f£­¯H\x001bä ­h\x001d9²@«)÷jÐý>\x0001®qñç\x0000®ÿ\ÀN\x0007\x0002 hYeæ7n'­ )ÇSQm´íðíìÝÃ·<¥õÛáãKÂK\x00158Êú¬vÅ"î1°íþ¥p{öîò6ÍjÝ7Ìa¢­ºYqÚ±\x001dÃg!ç6aVzüOÏ¸vë*\x001bÄõ
®\x001f´®YÏ\x0008cG«ð\ÒíÎÖÝêä\x0019Ã\ÄmOÜ\x001e\¥\x000f±pHÒK\x001cp)¾Â'¢­
13ïf\x000c\x0018¸¹\x0004× \x0008¢ ú±È¸+iFÚªyÆÁÿ­ÙR¸üùé3ð\x001c\x0006õRæ\x0011¸á8w8Y\x0016ÇY\x0017®Ý¡e{ùæú\x001düÝQT¥dªZ\x0001÷¬.z\x001ao\x0008¯\x001b§ørAÐ]¦¤ß-Åbî
\x0016À:Oµn\x0000\x001bÏé°u\x00149°JéýWÃ\x0012Ö<QW)$]ík»yüúýßÞ><8ìÝÂ
õz`½¢B\x000e\x001eD/ø<\x0007B]\x0017W\x001fîÎÞ^Þ¼8\x0006lªp'\x00006ÚÙ\x0001d\x001e\x0012°Tì©êÊ	X«\x0003Y¯\x001e`;u\x0004!°b\x0010\x0018|p-,\x0002©ybA1e>Ò?\x0006¸*ÕBà¶T«\x0003Xs½ÁaUù\x0002VQ\x0010/n¼ÓðÖÀaÔÀRñ{Gê"\x0015<Å¿´2ûúGz£i£\x0019\x0003Æ°Ë%\x0011Bx^ÂU
0-v=çL³"ðç\x0018°³da\x001d¦ú=\x0015\x0004ï9Y Y\x0007ì%1«6ë\x00016\x0014ºÓ\x0011Þì¼ç\x0004ÉjÊ:àvI¸á%ae±°¥aXw,K)ÿàM\x000fp¬í\x001a\x0003!à¬^î:QÍ''4YXÈ\x0003©ç.àªª\x001fÛªþåÀ!\x001aªBÑ^yÖ°ÔE³ì9)ª\x000e\x0014ç,Ú\x0016\x000e`í¸»Ã)9ÅI©h\x0016®}}RÄ26\x0016N¿Ç¥¦nCm)\x000ba\x001c%£÷û:Û;qlVpú=kQÂ"/aø\x000f9§´õÔ½ã%4\x0004¬¤jVDú=\x0004¬à²ÈÝ}QÐ¤S ·¬\x0014¡ì*ú\x001e`¥\x0005~\x0001\x001bIMåsJ5?åY6B\x0003U\x001f=Äø\x000c¬Ó³pXj9æ4\x000e\x0002Û(j&£Ù
ì\x0011[Ñ\\x001cé÷\x00101ü¯ÓsCáL.Ï­ñ\x0015%Üin\x000e 3â±'\x0007¸
¢ô Ã#æ'²	åj\x0007S81'ôN®W=-¼æ$%Ö<	¥k\x0011ã.m
JyuÉËSÌÉ"?»Q\x0001"Q\x000e]â\\x000bÑtJTì¨³\x001c@m\x001eÉ"?»Q¥\x0013tS8áMf\x0003¨RèÃVÊº\x0007u#e\x001eÈÆ+ö\x0002þâ\x0015¦êÞ\x0001\x0004<ç¿<|ý¢§g7cÒL¨Ó\x0012¨Â"²°RkBëÁ\x0004û\x000eþ\x0007¼èß_ÂbÅøéÙÍÕÅ\x0001U&æ-Ju\x0017êxQo,×.X\x001clB¥vÑ0ïÖ{s\x0014×7¸~\x0014WÒkÈâq×\x0002àrU­¦È­ã5yÍ¨yµÌ\x0012´À\x000bÿËn\x0016Ë-¶ô\x0006q\x0019!ã¢üã\x0010®\x0011\x0014ç³ÖóÝ\x001cl\x0015!\åN´z}³ÛüènS\x001cëK¼Å¼¼\x001cÚ:Å\x0006yK@*ñb<jt9x²¯£AU
p]êB=	­jhÕèjY«\x0014i
ÇvàÎUÌkO´ÙJkæµ£Öµ\à71Õ7jt¡×è0Íá\x0010\x000fÀ½\x000eÖ9îuÂñ\x0016Ì»ÕÓÉ½.ó_d¡á¢\x001bñãæ\x001fG>õlt6è¢P"·\x000eÄ¸_êÇ}óU&¸)*àª¨È\x00028l¼Î\x001e­Áj\x0002ÆSÝUúÏ\x001b¾ÒA8ßÁ\x001c£ÃÖ\rí\x0002Êåâá±©Ìb\x0018\x000e\8QÃ¥ß\x001dp\x000e§f¿*H5KÁéPww\x0005¬\x0014jN6\x00125Çé\x00147\x0002¹¢o\x000ft¦Ðé}Q¹etÁµtÁuÑ	n§\x0001Û	n©â<®Å~!8)msã_¤Û|Ò
]zº`ótÎZdµ"1daÙUÚ\x0000L"¡KÎ\x0016f

k\x0018bÕ§\x0001/4ð\x0011ÃÃvï«©\x000b´*÷(5\x0004jX\x0002@u\x0001­Üå\x0003J½ËYå$C¬²Õ¡^\x000cëli£\x000b\x0012\x00156$ð[d¾Á`M³Z³f|?lHæL°!pa²BÍ±\x000cë¶.ï1XÕÂª1Ørs`ÎI$\x001b\x0005è\x0018vKcp\x000c6´°c+²7<ï9\x001f£d±`»U\x00161Âª«ô\x0011°êú©¿Õ{Í\x000f\x0010#
w~`(óK4\x0002[éÇ"lÒí
ðé-Á¿·Ó·Ù\x0012Ã\x001cc
-ëÐ"\x0008ØWÏ¬|a)f\x000cRCÍºU bÖs<ÍyðzéÛç§þë §ÕTá\x0019Q'\x001a-ªÀ7¡¼\x000bxx{O×Ë³·7×¯¯ÿã\x0018 t¶\x0006Ä¨|\x001eU<cb\x0014j¢0{Uý\x00173úÑ÷3bH\x00181 /!L\x0010R%\x0013jïaº\x001cÒ·¾\x001bÒ
*\x001d\x0000CÙV(F Ø{Ãz\x000b\x0019U¥Ó\x001a1"º\x0019MÄüjbÄz\x000cÃlÈ¸Wë¬z:\x00102µtôAJ_V$ÆJUbDÉ·Ì(·b6Ý&4õ=´\x0010Qij9ñ¨Dæó·\x000e¢0îsD"Â[ºFÄà\x001fR®×p\x000bE\x0010½ÓÙ_ÿ¹ÕtÚ
éõè|÷z\x0014ðÜÍ-Q\x001ekS\x0005\x0016@\x001aJ8£¶+\x00066M]Þ·ÍæÿSû&÷\x0014L
n8µ\x000c_ÒÓµøúéñÛÙÍÓ/Çj³±à#÷Áí\=\x000f/t®ÒWq«kkº\x0015q\x0018ÎÙÍõ\x000f\x0007k3jô5jôC¨./Ç	Yºó<D¡\x001a-ºTVUÙXò.Â\x0010ª5ÙãÔè(\x0013©\x0015\°\x0002\x0019Bz7\x0013ªuC¨F4\x0012¶s~QSe
Fí$w°:Ù°¶ÓyUq5\~)1NH°z«Ál\x00086Ø\x00066Ø1ÃJ9$XI\x0005\x0013`WÞX\x0001µ]\x0004al\x0011¨0Õ¢DÖFÅÄ8Ãnµ¿À*Ù\x0018VÉ1Ãj~(Ã=ì¹@sM«ÂôSÀFÕÀF5vhÙ\x001c\x0000÷ e='¸î5×ùä|ÿò5+þ\x001ca\x0005\x0007 Çv°Sj¨à. ®"ó8N\x0001ëU ÝÈ*È\x0018ò\x0019krL*ÕEÈ\x0015Tfoþ¾\x000bÖ·°~\x000cVæÙâÀª\x001c\x0005Í¤aM?l·=aMh\x000eY\x0013F\x000eÙj2\x0003\\x0002E\x000c%;³[	æ\x0011VpäjVü9Ä*Hg\x001e'\x0008²T¢a]?å¶ËÛ`Mã\x0014X3â\x0014\x0000¬¦f\x0017\x0000ó,Ak\x000cÅÌ=4\x000eo9lTÍ¹?\x0007`%Ê\x0003\x001b¢	,Cf-É\x0010¢HÀÊ%kí,\·\x000e¬ØÏÿõÏT%õysG8¾yzþ\x0005þî ±oÍ\x0001àhV\x0010ÎtåhT´[\x0001\x000bøÇT(õîâ,\x000fu|s}óÃå!%úL]`ÉÉ_Am\x000c'ðCÈ^\x0002\x000eëåp_ô[îW?´$è©ê\x000f¡ë¿O\x000fÏÿùt¤\x0010
ËË\x0013&vxS¦ÖR		nß¸Ë³O7¾>T0ðdÕ¢cQ3%vòyL&gB%©²ÀXÊ\x0008n
û2@U5XÉðp\x000bðÐº \x001c+dX\x0016\x001e	f_\x0016y!¡\x0014Æ6&Äß]ÑjÃn\x001cfµ`\x0015
ËVÜ¯µ1Î\x0018;¿sD\x0001×<]ÍèÉWÅT2ïs±_\x001dï(£ÈÍú\x0013£\x001086ýãçÍÏ¼¹ßo\x001e\x001fLÃ0F,aµaÔÄ*e9[Ûåã»7¼­ß_\Ý\\x001dÚÐb6`\x00161Ñîç\x0014,\x0008G;M\x0017Qi\x0017\x0017¸ÌOù\x0001NÛÓ\x000eÙÓ²\x0010\x000eüÎ:Â1ÌeYÛ\x0019Ò\x0001Îê\x0014"\x001dÝV° ¦çc\x0012¶Ï|mösJ©ïInPír,Å:Só4g.\x000b\x000bI??\x00068uóÝñg?§äövë0¦"g¢}>½!×Vù[\x0004Åümÿ
uyh;®ÐÀÅ\x0006E®Í¹UÂäßä\x0002c¨%\x0003^ÎÞü¶yþýØ\x0013\x000fÙÉE%BÐÀ\x000eQÔ\Ø
JvÛû³7º¸ùxÐ§K²
ö\x0001&þìçÌï
Ê/#'0l+Ë÷&HOW\x00063¶ÅQ~óyó\x0002ßþÏO/Ï_yÊX¯{-`S\x000f;,K®\x0000WzO çÍ»{øþ¾¾¿ù°¶þú6}ý\x0001Z,ÅO¨ÎÑ¨J%"yÀ\x0001Ùê0\x0019B\x0002"¢âÏ\x0011V\x001d5{#>J.2H#³ÉcÚ\x0017\x001eÂU®±,þ\x001cÂ+Éáÿ±\x001e~,\x001bÅ¬X'.üGµ¸ø­É\x001dK5Yt\x001eË\x001b\x000c«F³¼¤p²¸ÖíoçZ&ÈJ"¦y¿Hª\x001d UAÓ»Î\x0019Ø_17jØ@Á\x0013kü~õö\x000eÔJ
YÍ\x0007÷,FÕâtºçÃÕJ\x001630zßpÐ\x001eR«dM?ûI¥täDÃÎÚQ/\x001f¼HöëupÚÓp
/H­\x00118=
¥FÅfj(Òaów\x0007jÕ\x0010¨M?ÜbTøøÅ¤,,¥bf@ÝûB^NZOmQó©-If\x0010ðåºWßô\x0004ßMáóD\x001aU?iR\x0007¡*S¼\x000chïKÏgÊîí]L*åä\x0006 iúÝj­¦tÃFÔ÷¤¼¼]\x0007*Rs·:M\x0005ªèÖ¯Z6\x001a8ðw\x001c'i8j®xzèV;NíV\x001dÓ0'áKÄÄNñnLÉúfJÂM©\x0003
>n½ñû9«âBäLÅÝ °rú\x001cÛ\x0016¸\x0003V;æT[b\x001aýJ4öÄ½>\x0006öM\x0014ø\x000b<ý@³òµtûe·sNz\x0012§#ÊdÊJ\x001f\x0012Ó;\x0004é·\x001eQ\x0003í&R\x0003»ÈãØ;MÖDù{*à¨­tv«\x0008¥\x000bT\x0002(*O¾þâUú=\x0015è¿~Ø¼üçÓçÍãÞQ\x0013i@Pºq5µ¸z)ö©NÜ½¾¼¸ÿóõ»«CÚJ6m÷JÑW\x001dJeàõ|÷ðûïY\x0011êúùË\x0011A0ï°n/gÊà?í\f·4Ä¥J>Ê¾ª\x0019xGß]~ü¡®oÞ\x001f\x0006#ôj²  G»
]ñ,4ôùhh\x0007ùPÆDÇ­F5ì²f1úçWÁ[Gý\x0007Zä,pnÜ¶,ï°=rd\x0015|%,iIXr\x0005|\x0011<Ãþ\x0018Òî3fï3q]éfÑ(½jÕÛÈR6R9\x001e\x000e}w{TFàM»âÍº%\x001fÀ;W*ö×Vê)gã¾\x001aNø4\x0000Z×â6ðFs­Ò+Ðß>¼|~ÀxÝ·#Y\x0004D}®ÏòÂ[ýuÂlM®­T>ýöòþÝ%\x0006în\x000f&\x0014\x0012¸s¾\x0006w­\x0006a\x001f¸±Ju¼vúý`ÏÒ3\x0003N¡­D×8¸¯Õcp¢]\x0018\x0007·WºGNRèÑÑbqZn
áZ\x0001^u¹ 8\x0016Ü
[\x001e\x001bä±zô\x0014c\x0010\\x0017«ã)Ám\x000bnW¬q\x001f©\x0001Îc(éîzKÅGNo\x000fæX\x0001^\x00018\x0007xÁ}zªf§Z1÷\x0013°\x0006[¶ØrÍ
7ÔOuÊ=\x0015\x001e¸6y+ü³»]ànÍ\x0002G-|²·\x0015hËÁvj?tp\x001aÎ#l+ÀC{¤5Gc-Ã\x0004.xgR:\x0003Á÷Ë²vG×G·\x0006\RLÓ Î-¨mI;ótgxTÍ?WpG\x0012#Â$WEñòÞvÎG¨KÙªy\x001aN\Õä\x000eÿ×ÿø¿~~üv,'\x0007jkLTÜøò§Ôþ9?·§ÜÙåÛwW·\x001ei\x0019³Ö÷ÁÞ´\x0011LÁQêÐjKÆ²Æi17k\x0007¦ÌÚNU*\x0016\x000ef=~zxþv\x0006_\x001fëÂ\x000ebF\x000cÅæð&Ö^S/m\x0007;}\x0005a.oP®9U\x001d\x0005­f\x000f\x0000¨q# 8.+'\x000c¬eq|\x0005oHÒ?¶X\x0012¶´zöºæÙÛA\x001aK Ö¢D*\x001aÔhÖðûzº0«ãÖ:k¸\x001cSâ°DúôÒrUÃ\x0014ÛL\x001d«A£¨A£\x0018\x0001UÜ\x001fà¬°X\x0019@\x0003\x000f\x001f1ÛåK\x0003¤RØ\x0014\x000e ba\x0003¥)ÂÌÞqhÛï+³íAÃ®FÅý¨
Qs\x0010\x001eËÂsì\x0010\x000e~Ëi-³¯È¶\x000b54;_­ã\x0005r=°Cç7g5áuDW\x0014öø`OÙvOÙ±M\x0005Î¢"©<¡Ê\x0002TÙbÁ¾'X«õÔ<¬ß\x0014f\x0004Õ\x000c¬°
J;IÌìë¯ì"uÍ®rnhWùPéTóì\x000eaôve¨ðMf!døH­àg_ù/Ê4å\x0008I^
UÎÃ*\x001b÷f¶;*CJoû\x001a9Í\x001bDv8dl\x000cæN¡B8¸\x0002kúHs2jëeM?
QMZÃ¶\x001bØÚ\x0019ÞnrÿÂNj§\x001aj§VPGwN\x0015ÃÚæRWö+J¶\x001f¡­m ­]aêÈ\x0003a\x0003lM-#×ÁÚÆÔøsxY+Mm/\x0016Õw5Uâ\x000bÅµQÛGÇ\x0000µÏ®ã´\x0019\x0001¨\x0001uùõìýãæùÃ/\x00063¢\x0017\x0003ê^G*9ã1¶a»\x001fb\x001fÎÞ_]Üüp\x0014±j~ó"	èõ!bg\x001eéTb1¡ Õl¢ØªëglÌ\x0018»Í\x001dyôÉáTàêg)MaÜª~îe¶Ç\x001aXÛ
i#¥°f³Ì,àôîË5.\x000c-dè,õî¡k¢Ø¯cÈ½Bþ$nÿ¯á/rðÿ]W4\x0014^1ÊPÄ?¢
e®xs¬¶a·Þ[Ë#-"\x0007\x0003&o\x001bÃMÁÓæùf@jÅ¦öf/9%µ¦ª\x0007xÈlõOU$\x00177\x0007%\x0003¤Ì¥ã%±tÜV)å¤¤óþ\x001fÇÚXðú4\x001a\x0000.%R~3¢:ÕìÉ*'\x001d÷9\x0018þ!­²iß Vmôà\x0008þr\x0014\x0013ëqò\\x0016Ô«'cZAjêZ­\x0012÷*G\x000fnà\x000fÇ)µö5%þìÄô!ØsG\x0013°0\x000eD)4R(ÃJü½¹\x0005a^\x0013r=Nò{û¼ùúë\x0003ÖeùéØN·áB8ÖÃ@Fðø\x0018}@$\x0004öÓÛ\x000fo/±BûýëÃG\x0013UVÍXA\x001akø×Ï/¿m\x000eØZÔô
\x0014\x000fRY8\x0002¥\x0002\x001c¹~°ó÷Kq¼¾¹xñãÅ!#'Pcl
?ûA,+ÉSÀw\x0000×miQ\x000fz×ÖÊ_ËA}\x0019H\x001bc\x000e¬"hdP»·y\x0011hHþ\¥]:Ì­vQZ·û\x001bü/\x0002Ö\x0011ßN\x0019U®'ãH%*©Jkè\x0001Y­´h¯~üñúÃ\x0007ø\x0017\x000e9w\x0019»òþ\x0003çbÃ\x0013VSGknÇMØ\x001c\x0018M·9,¦FÌRëFäÛµv¤ÿo½fk?º¹oÞü²ùö\x001dÌÄÿ@Ð\x001bá%\x001elÅû¿¿x5¤^ê¹\x0008jÊSý\x001e8._Xnë8«\x0015órTÕ¤jÔ¤y\x0015	\x0015lÌ\x001dF¡xÔv+O0ªkT=j§4Z°UYõ\x0017z\x001a\x001aÔZô\x000c\x0012(Ü\x0012{w\x001cþí1<c¨¶FµCß«ó|\x0016Dë)G\x000bo\x0015ËAÜ¾\x0019#u5©\x001b"u©\x00106\x001b\x0015Ö,)R\x000bË`\x000eiþ/Gõ5ª\x001fB
9-ê-ÒÒ<õ\x0019£Ò'!
5i\x0018!Å\x0019j\x001eÇ¡r\x001a!%\x0007áÓ;\x0005j¬QãQq\x0006}\x0017P ´éÙ´b[×p\x0008µø\x0007ùô\x0017Cfõæ\äÔV*åÎæ1\x0004\x000emo×±¶7ÕÐU¥½¥¨Ç¹Ìe11Ê\x0012Ü>Ía%»J\x000e]V\x001a\x0005NÈ®R\x0017 KÍ\x0014²ä\x000cÍe%n+dåÐ°\x0010,"\x0013Ë¼\¡·Ä¯ÆXûJ\x000e]XÚj\x001e§\x00121·Q\x001diÂÃ-p\x0012Ðæ¶C×UZ\x0000¡¬YÇXF_6ØR@\x0018cmî+9tai=AîRÔe\x0004¬<"n×à±6\x0017\x001cº±àåBYýBP¤
V@qXõV±ó\x0018kseÉ±;\x000b{\x0015±Jþ\x0010=wF\x0003ë¡a:ËY;K\x000e]Z:H\x0016\x001aRp)s¬0\x0001OÄì-Õ\ZjðÒç*É¿óJ\x0016Ô-íõå¨:¦R·î,úWu\x0016ëÛÙÝo\x000f_\x0013Ó±6êøêÓ¿þùíñëÃ7¤4Úb«¤<¡BÀÀýêXK\x0006^\x0006¹ûäòöêÃåmy\x0004ÞÝýéò\x0003ðíIÃV¹o\x0001ë®½e(^McÕBÒBÈÔ^\x000eYQt\x001c0kÇ1 ·\x0006^¤4÷Mboyâã*&8Ü*:R:e:YÏ¶]§\x0015¾\x0012\x001eÎµÄG
/E¬|0·¸\x0014Bë»	5ÝE
h³&B/8\x0016!Íº%(]³\x0004ñg¿
).óx´lC3\x0006\x001bZ¿0¨0¨^BÃqôdÃ@_9pÙþj\x001bªüä,çp½e+ÂJ¼Át¥#®Û)JPnBp2 \x001cØNBnºu$\x0015Ç\x0001}óñgçQ³Ic\x0001o?	9¶ä\x0014
G\x0018!\x0014y¸äôáÿªg
½~zyþõõB¤7\x001a&\x001d03à4\x0017uy_é-\x001cfGîoÞ\x001e\x0005³º\x0006³º\x0007ÌÇó@å\x0019(öK`\x001c \x0005°\m6\x0004&E\x0003?a\x0000t½"Ê¥ÑÕÆó»­÷aÇXJ\x000b=d\x00182\x0014 Üi¨C<eDeD\x000f\x0016J\x0006R H¦ªñDæù.ó$×>Fæ}CV\x0015_-!3å!eZ[Þüê\x000fj\x001bµLYÙlËJ£c\x0019¢7¾@`¤g\x0008.¿\x001a7rª=/T\x000f\x0016çÁ [vì(õÒ1+LV]ùÌtEzeà­õHæ\x0005W¡E\x0011Ç7Í\x0006À\x001ddXÁáÈ\x0019\x0006W)).F:wr\x000e\x0016¬Ëd×?¥Àg&+&3b¾L·&Ó]&C+x%êU$2V\x0001íjÇ\x001a2ÙÎéL³gî\x0015=¼lÅ*³­ÉlÉJ'w¦7ÜD\x0012©@,,\x001e²àhÔ«\x0018X£Yæ\x0005a®q\x0014ÌÆù1¢ÇûI³.x¤z§$°àxÜRã«Ì´néòËPÕÉàÈàÃ,
vkUØñþ[J¦3Ãè3\x0003V}\x0019C\x001f\x001dÌ ¸cW¬8ÿMëý>ï'zò\x0018\x0001Lb4?LÃ&Ó;^{KÁ|³üSSÎreíôDÑ½\x000c7!0oÇÏÛ^L¶ëbrÚ BU"³\x0016ÿ1iÃß2êñ#
Ì\x000bïñpV87È\x0014©IdFStA0þ5­-YÏ2sFñ2Ó¦D¶\x00027\x0016ÀA²â4s¢ùø³ÌJTÍdêL\x0006î\x0005Éñ#Ã	Ûõ\¨ÃK\x0016ÆzeK&£¡"pÂ­¸ÌlÉd/Y 	<B¤YºøØ\x0015¦\J¦c\x0016ö|LÓW2A#9*wX¥<NfZ2ÓMfn¦uæxk*éÇ7oÉ|\x001fÒ42\x0013K¢ÈÏ\x000eos\x0015VìLxäÁeUeÓ\x0013ÎÄßçÏé$¿4ÝàI\x000bzåtÒâ$×v4ÉóÃËãçCVC¡\x0019jA\x0004VÐî$Y(§Ts;U(n.ï¯Þ\x001d²[úÃV7g|e@8°}û¶yù~0¾'\x0014á%eï(+IÄ\x0007,gvGÂïööâþî`ü,#Æ\x00061ö"êèéI\x0000WI8w\x0014h\x001cDsT\x000e=Zá£¾°³¯ðç´ö>>=ßO§¼Ô[n$Ö8"M"äùûÚ]¹û³×7{D\x0013+¬*,XMXè\x0018\x0016jí\x0010\x00178HyGÀ×,Z;Îí\x0008\x001eåRé+)Âÿí\x000fÏ?\x000e~O3\¸\x00189ÆO¼ vÝ¤ð=¸¹øt}ðkf<ÛàÙN<Ômq\\x0001\x0006\x000bä³\x001fzAî
\x000eõàé\x0006OwâiWjZ
ë¸û:ìöuÐyQÓyÑIUêDg4VÓæ\x000bGo\x0003
4\x001dÆ\x000b¦Æ\x000b¦\x0013OÉR.aÊ#Æ\x001a9\x000erOÎê8^¹\x0017ÓAúñ{Äø÷ÇØ4ÕÉ:¬à¨|dÉà¨BíÉ-áÏÖJWÂ¹I*º*ðþm\x0014_¿??\x001c² ¾)Ø©q#ùMo\x00181ê\x001d÷\x0019ðÍ.®>ÜÝìÓJÓþ¯/ÖÚï?Ñ\x0016É\x001b#Wqß"×ÙÝóã\x001f\x000fÏø\x0017oÀ\x001fø9³v\x0013ü7ùôðígøëÄi­A\x0019V|GÄ\x0010]Ä'5[ªâ2^yG÷î\x001bð\x0001àSç2î[d<»»¹útuyÿêÝ2føÏK­§ãÌ\x0018ñ%f\x001cRoYKb9\x0011³Dÿ/ý±\x0002:J\\x0005	ÚSç\x0007xsÞD6´7§Æ+ý±\x0002Úú\x001cÌ1iuú\x000c­sW\x0005\x001c\x0007Ò9À9þ\x0018gFé¤e\x0001:Ï`\x0012ÊãSZ\x001dè<\x0011t\x001aGþX\x0001í\x001cV\x0006dCë<a\x0002 ½¶lh¾LO\x0006í\x0010Ú­\x000e2§ \x0011Zä6Ay°¬Á>ÓîCÁûôÇ84t\x000c-\x000f<Gòò\x0008¤\x000fËÆÆ\x000e\x001a[!ò\x0004qh\x0011ó3\x001c,­L\x001eæ\x0003ÐÔj
¦Ø§ÆVëôÇ
h¥ò\x000b\x001d Òç\x0013/ÀkÚÈÓZÚâ	m×\x001dÓØÛ\x001c	\x001aÕ°ÒFc.w\x0012\x0002´=Íòø¿þþóßzþk.\x0017LEqñóæçÇÍAÛbO"ÛÊ\Ð,p>6Ý&I¨ºÂ¬ü7\x0017o®.n_m~øý\x0000\x0016\x001ejº\x0017+R9(`aèC%¬h
åWò(\x0016>9µìÆ
åtÕ4\x0013±òPi´´ë°0Efû?"É¬Ð¡oW8\x0018KXØ£éb/9·Îº¹8*Yòa#£;u|ÕãÉw\x001bÌ<Ú*;«N\x0014F\x001fªõGú
1Cß½¼þ0\x0018:E¡Û`Îç7::4±\x0002È)Þ½:F¶Ó`ßþpòïøxCÑôÇ\x001b8Y\x001f¿l¾Á\x001bè\x0000\x0010Ö\x0017b¨×a\x000fÊ-ûà\x0004úAã\x001a\x0008NÑ«÷\x0017·ðJ"ô'a`ùm²M~­å¿x\x0015êÚõ\x0019GÀPs\x0019§Ð óYs\x0019®î\x001c68¾}\x0006q\x001c(\x0001¾;#Ä}@I\x0013A&z?©É-Ã\x000eË·\x0015¾\x0013©Íq\x0017mdz=ªÊí¬>Ë\x0000j¨%TØ\x0018ä â8£4\x001at5jÖ6)¨: byÎ¨ZåþqxSÆ¶2ØFx\x0005 s/\x000b£âÏ~TÔa7dUaÏM~+XÅVÕQ®'5y^\x0012 \x0007H¥O®IÚT&O>ÆZ\x001cÿHíO`S\x0013\K:bSR\x0019\x0014«¤2©\x0016IM8\x0001©ÕM­\x001e²©±üõ¥6X_J®\x000c\x000eI\x000f§ 
-éÈ¨ucèëÃC<¢"F¿4i1Pã-ý\x00056Þî\x0016çÝ¿\\x000e%Â
i%ÇL°\x0014áP®}Y-Ôå­\x0000)ýJ}í%¹-\x0018E¯%VçgB:¼²Ú®#4®&ÄÎ¢NB«r-\x000e>©Í¹"Â(9´¥Û7S?!\x0015¤\x0011¡\x0015Ý°½ù+\x000b\x001azG&dÙ¾\x0006\x0000U\x0003¨º\x0001ÈtRWt¡$F¿°Ì2j¢8H\x0012Õè*áÛç/Oÿxx>ÄSïr\x00075¶¡\x0005HëÏ¨vìcx\x0013_Þ¼¿þËåÍQ:ÓÐ^<UÂ`²,´\x000ex^Ò£ÀÓüÀq>§k¾F7e	\x001fÎ;ÒÏ(qvG\x0010j¥ýB¨ùªÈ|"Ãy\x001ah
p|Hû ü:ã9Õ|\üÙE
T2ßÌÂI>[àaLÞ®rÁ­\x0003Ìª\x0005°QÅ\\x0002\x0008þ¤\x00170yP\x0018\x0000<«\x001evp»|ÜåÑ7\x0016¾Ï¸ASï{r\x0018\x0002YPÂ²cÁè]÷ð\x0012@\x0011$\x000eTv:üPM Ö&üáéËï\x000fÏÏN?ÇÏï\x0004©£ÉcByA6Æîtiáÿ_¿ÿxuy³Oü(!ÅTÒ/§'"\x0018\x0003VMo7ß;À¥)\x001dê0¢\x00121¯\x0007|OÀP
zfè³·\x0017wZ\x0016[´ØJ9\x0019-çï\x0000\x001fÔ\x0001kIVÀ\x0016ÎtÁy{!\x0010Î\x0018ÀI:úpÚÄîpàB8ß~TßõQ=v\x001dè\x0002ä\x0005üÛ¼g87öY¥Ê²ÜÅg¿ÕP¢\x000eã!Ï9Ä<\x00127âpL\x000e()òISv×µ\x0017rØp¸K9ªÑ\x0002®èø*Ó®Zç¼Ùu\x0018/\x0003ÎÕ`øs1U1W\x0010G8o\x0005ß\x0012^ä\x000eV\x0004Ûó*Z\x0004æ\x001bEßa1LF*M\x0016%\x0019)C\x0001\x0013Ã\x0016ÂË\x001a,ý^Lò£¾¥L­-)4¨
-2Ì\x000c©\x0019ê#)\x0000é%Eë)½ïX\¬,Í\x0006ÕÓsLâÝª\x001a6\x000f\x0002þö/O_9pn¨<-_ÉÏZí\x0015=vààU»¯S¤»ý\x000bü¹G\x0011³b4¢a¬êÙ2Â\x001a(	TIr\x0014 âxÜãÖ-ôÞÕø³\x00132õºPÈMfB'\x0002Qû\x001fy\x0019¡Ð¹\x001euº\x001eà,çÊ­T*»÷Õ#s\x0015/>»5ÖÚg·½\x0004\x0006¬m¾s£Ùº¿Zv¢Óª¦ÓªNÚ<V\x0006Ã\x0016"\x000b\x0002]I´©$I¿.6t±NiëÊ¶Ó^\x0015f²]EgCMgC\x0017Sù±Y_\x0007è¤*\x00010JGÎVÁ\x0000+R0`ª~óÛæûæñW\x0006ÝéÛT=[\x0003|ì\x0010c%oàCFìÌÛÜcõØÝÅÕ[T\x0004=Êé\x001bN?Âi|R@e5A#nÆ\x000f£ ¾Þ[È)ãüÈó#ûóæìÓæC¯\x000b\x0002\x001c&C\x0006\x0011©IjË!Ó8[µVé§O\x001e\x0017\x0004\x0018l\x0003\x0018l'`È_\x0008h¹4L\x001aEÛ%°ðã0 \x0016·Ti[\x000f RN\x001e"d~B:I×Iz\x001d ²M\x0008è«lÓ2À`8{ã­£0\x000c¤þ\x000b¯ \x0018\x0001³äo®d\x000cðúJþ´y~øúõPY6¤!0\x000eë\x001fñI(\x0004m\x0014çvfÂ.îæòÃ\x0003$\x0004Ê
0iÚö\x0000b~.æ5Ît.ÖA\x001dOº±Éf\x0015`¬ü\x0005\x0000¿°\x0004\x0010|-C^¤¬§Ó=èw\x0008\x0016òI\x0014««øÒï>@cÌèsa\x0010#dBá9/«W\x0012Jß\x0012âïÎolÓ'ê/(udÀpt\x0010Â¿>¼\x0008ó75-Â4à«â»yúòðuó#©\x0018\x000e3óì3Xa¨¨×ï9¤o®ß_~¸øË14e]f]\x0017¤Ó\x0015£ç*X\x001bc|4;3Y\x000bØD´Tu2ýEª?¹yr\x0007ß7_={³y~>\x0004¨0Áº©¬(=ÍçZ"¥ÛÁ=g\x0010î.>¼={sqssSJSsÊ$òÐ
.£¢QÒD!\x0004Ú%àQÌêÍG8«ì%r¦ìe7§\x0014yÎ\x0018pZs¿¹+mÐ«9§#'q¦\x0013§Sq¹s\x0004GîføØ\Ïª\x000e«Ac\x000b\x001aG@q¬\x0004¯P#1¾ZW¨½I@}\x000bêG@íTÖl5¿­6¥\x0004tr\x0018\x0000UUF\x0013@UØè\x0006Eik²èTÝ%ãjKo×X4\x0011Ut\x001aÇÉ´]çàpàÎ\x0001\x0017\x0011®Âì|cËºI·"ÊP|Ú;»óì¼={}qó\x001a^\x0007\x0007.\x001d"¬*U0è^Bx\x000eF"çA.\x0008ÇIÞ\x0008õÎhk\x0017¡i\x0008M7¡ä\x000f\x001b<½\x0006îmð.wÞ\x001d±!ýö\x0000a!&%`\x0004tlÂÒ©8
(«\x001a\x0005\Æu\x0012¢l Eû-F'ò:tz\x0015P2r%¢ª*Q$\x000eb
½2ó\x0019ì¦Uè,óÝþ÷\x0012¾4$\ªêá0\x0015l\x0013}ù|¨\x0007E/¸0\x001eÓì\x0012MÖ\x0006.\x0003Øé<bTöþÝ¡:\x001e} )Ñ$qÆLsÎ|zx\x0006÷ìíój\x0014PCjâÀÑ£qÜûu?]ÞvÈxù¼®øp^\x0007ÛÉ\x0007ïú$¤\x0016q~
?ñ­§:\p+vf±ðåý¡&÷\x0016÷GjìyÙn¨Üçz£3Ý$yn}r¾e©Ûwb§\x0013q¤²àiik¼Tnß\x0007>cvÅ1Üì`"7GYew^ÈËé|Kçûè`¿\þ­áFvë1igØ°Û_X7y_	¯ö¾\x0016}[Gû\x0002\x001ev¢2\x001e6{½Và\x0016ÏôâáüüêËê¸ùÙGN¡·rvÂYÑ,<+z\x0017áOkLàbK\x0013#9×^ÄU¶³¶Ù¶I\x0003¡kå¦+l\x000c¯¹\x0014Ü¶0¬k\x001dÄKmÚJM²+M5§òÇÍÏ?o^~9tì©clô>jH8b(ý©ÌÎªj8÷>^¼ysq¿Wu¶ ê\x0016Qw#j\x0019Ï\x0003!Ê@M8ð1ÈvÒÛ=GóqD\x001abZÕP`}[EÓk~9pë
Xu©\x0011?:ç\±*p\x0004_Þ\x001fX)°;¨ôææúÍýQ2'k2'{È²RW"\x000b\2­51VÑ\x0008n25/ëU©¬·Nð<>üíP¬æ}Åº\x0014TLJEÞÕ+Öé«Ë\x001fÅ,öùÒ{j¦vj\x0015¹Ð³}¯-'Kú;JU\x000e(ø(Møíõ¿þùóo\x000fÏ\x000f\x0012ï¡\x0014+7¬sÈC\x000bK\x0015bwÒøõå?]Þ\\x001eÈ½\x0013 \x0016
 \x0016(kcOQ\x0010Îb[øv¯¸å|ªåSÝ|öÜf¾H£Æ\x0010PòfUnw\x000c}\x0001 ÉNòôÔÅÿÖ|Ó¦tÝßq\x0002í÷%ù.z*­Xo¹?¶QmÉSº/R®îýG\x001c?{w°\x001e?ÏHJ\x00111}NF\x001b¹Ü\x0018+\x0004\x0014 ºT´~;òÖ\x0007Y]»\x00089]»!µ\x000bçä\x00178\x001aÔ\x0017/W¼{å·ÝÅ1Ol®bn8±¹íÅÅ\x0008\x0011¬ÇrØ#6çôäÔkG\x0012±&Ä"ª¾Õü\x0001"øy0%\x0003þ{\x00150ª^ìx÷üxÈ|¶<&\x001dö°izoxªÙ\x000e»¿ñÝÍÕ\x0001¢Ô®jg,\¶¢9?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ïÌTk ¢\x0008\x0018(%Íå\x0003\x0017b@s"d:Zî (\x0014F-b±f`J,\x0015k­9¯Û\x0007\x0011\x000erbÔ"¦7x¥¸«-\x000c6å}â0û¢cÜQ,Ð¿N¢fû\x0014\x0006r'|ðêÃ7·}Y\x001eQaîµ~òÓ\x0018Ølæ²³$úe(fó6Ö\x0015ªÊ}vO\x0003¦u-öÃ$¹¯Ùl6t[¥¶,g\x0011äjÖù\x001fâÈöJF³\x0007E\x0014QJRÛ$ÖAßÏ\x0002
9\x0019Í-©
w·Q­|ÄjÖ\x001eÀ"É\x001f\x0015 \x001cz¥Ö¬IÉfKÝa,ê¿>Ð!èï^/ïÞ-\x001fúûþÈ´2

>ø";yèÒÑnã@La~þËü²ïåi\x0000µæ\x0010 Atò	ñ5Oè\x0015<mñ³GÄ£¾\x0015m:\x0006¢×ÅfÂÍ\x0008 T\x0015êvÌâ½\x000cd~Kli]+;äÍ^ ïß\x0017«ï·¹\x0013\x0019H\x001cS\x0011æá®·;¦L(eÉ\x0011 ÊOé!1p6\x0011nCçºöNOhÀ@¯qÃa¤¡f\x000f\x0006FM`OÖèù\x0015­6M0Ð\x0014:Âà4hÌT$\x0001Eän¢ôPÇ²P2%ßsNRñ8\x0014\x001a\x001eGñã\x0017&OËÁ0b=\x0015¶ôºs±pÍ X%\x000c¶ü\x0019\x0008#`¿MºÕOha\x0004÷Ð\x0012¶Ù>³ÅÑ?CY (o\x00034Çì>áÙ·%cl¶í®	¹B¸\x0002\x0006F²âÅVKE2iy@«s^\x001dÓ?Ã`\x001cÌ²A'Mú579uQpZ°£ïR²éü\x0019Èâ´§¶½A8Í\x000b\x0003O\x0013\x0005â[iñU0\x0012Fd>Åï@\x001aèG
\x000eÓÖþ\x001eUÙJc¶E\x0015Êµ\x001fø\x001dFca®"&\x000bfñ§1\x0019®\x0014ºKQ-óìbq{û3×É\x0005¨kîÓ¯«»·/;¢\x0013Þh.,\x000c²<	Ré5Ñl´Q~=;>;ù÷«þØDáñ\x001aOó§\x000b:?DC§Èa\x001a\x001e
>D¢ó\x0010íçº·\x000f1\x0002d³\x0016Ëëqq÷£Wµ\x0008ÚWÄC'Q\x001f+
4MÚdºJLW³óß÷â¡80\x0005
{@&cBÓ<\x000c\x001dc ³¤´Ú\x0016Í{pÞ®®?~ÉW\x001eÑ<Ø'»w4î¯Os7Ðc1;±lxâ\x001c\x0011ìOWMWHÙ²Ùù/yÎ_OÄÇ/þç»\A\x0008
ÔÔZ&Bs+üÏ÷wüv%=Ê¬à7¬-ë°}è·{q<àø\x001a\x0018Ø\x0005cÆ\x0003[èÜÌ-È	4\x0011hb\x0005
$ÒÅ\x001a9G4lê`ÆÓ@Yfþ\x000c§Q\x001e0¨«ÄJÏdôqÚO°4`0æÏptÑéiÏã/È\x0008%CÊÛm\x0005l Îº\ÅÚHç\x0017²\x0008"×\x0013\x000fã1\x001dJÏn\x0018yï?­²'\x0016ndT
³Û:\x000fI;§\x001c\x0016\x0005Õ3Ô±\x0003ý>íuÙc\x0017uÿëÁ0ÖpêJ¦!ÒKÒ·áZ\x001cíøkp\x0014ÏsP²â\x0008§´?q
\x000e¬¬Y«]3\x000e$µâRcAí}(\x000e(,Oóg(Of\x0015y'þ\x0006\x0015\x0001X,IZ¡raÂfi(ÚÊÁ8«\x0012\x0012åII\x0012Æ®´§Z\x001cÐÜu¬Ø¬ìK~!¥\x0019ÎÄá\x001ccqd®¸Åï@\x001e\x001f¬ ñ6\x0001¦^ <N?æ,\x0007ãýèÃô$8Ëù;Ç'CD wüXIÇê 2Ò<\x0012z
>Åï`\x001eg8:ÒÐ^(,á\x0007"ÑYBÏ§ø\x001d\x0003UyÜNÒL@iÉH;g]m9xy+V*à¨\x000eqûÍ\x001aÌ³®^\x001c¼>I4Ó¼/éh}4_/\x001dÜx\x001eYô®f¿àB\x0016\x0017=åJÃ}ã´ão»Ï»b8\x0015ÜE"m\x00068¨¹¯ÊÛVép\x001c\x001cûQ!|¬ñ\x0010\x0002Ï«\x0003M@-E{ciâ\x001b§ð¨Ì3üa÷Vë½\x0010\x0004Í
)Ò:MØ­<õ'\x0007ã@\x000f\x0012Êß÷ëÈçö\Éâ\x001a/\x000báoyßá§Ç²SÙFÍ\x001e\x0004m8W\x000f\x000eæ	Y+\x000c\x0015jaÎ\x0000åÖçAd\x0001­8Q×ÉñoWî\x0015ßá<\x001aþäd
Gë£%×Zíújyòù	5ç\x0007Ò\x0002IøÀðCê\x0019£Êà\x0018å§¬Ê
ÔTp6¡Ì²°ÖRÕ±Ô ³ÚßÁ8Êï\x0002qò8¼<Ûò)=á4c\x000f×P!aÜ\x0001¥\x0006AÈRq-©8¢Z\x0016Æú\x001aªy#´ûÊâåÁRìù\x0003&\x001cüý\x001d\ZôÔUéõ\x000b4ÁCS\x001b\x001c_k\qÉ\x001bÕ!«¹({~\x0007³£ã³ÞùºÌ+U\x001e!¿£aÊ\x0015¦ïú\x0008­{³ô4 \x0016 °SºËáY\x0005¼üëæí*ï\x001càl/oÂ::ÛÝÑ@È\x0001Ä¤A°5DdG\x0019^¾.Úô\x000fÎvu6(¼\x0011´úü\x0019Ï«ç\x000f\x0003µÌX^fô:®×r¸O\x0002&\x001b£úð\x0000â<ª¯,Â+\x0006IÁ\}íÙwS¡\x00198~'\x0010û\x0008I9ö$
Ùö
JÛ¹½9a\x001cñw«î~~ndM?\x000e¬Óò	M·þ$ç\x0019»\x001d`rj\x0003íj@EZ\x0004Ó}\x0006XG¹ËÙÛ)J®~\x0019cmýx\x0016LÝ\x0018¾*ª8\x001c4øÃ²ð\x0011ß\x000eÑU²`¾Ï`\x0016çHÁIüÎë¢)rö(GÁ\x000cÃB$VÂ¼XZ\x0015N«k6«¨%Á¬×ábË¼Z#Ëa)>h/[>èJ\x0016¡Ö\x001c\ÖAÒ\x0002\x0005ÒAààrah&ÝW²ÈÎ`\x0018Iq´0\x000b^$;î|+#k\x0010ËrË·×¢Ê\x0015ß®v\x0014ß@¦¨X§arµ¢ÖÅå+7oQ®T|~Ö[uÓiHA0I{¦>ÉªôºÒº¨Qãa\x001aâe\x0010³ÔB$Ápk!\x0007\x0004\x0011LÜ¼J\x00150
ù2\x0008&#£b\x0001\x0003U¥ä{\x0016vó\x0011¨iÜëa+SZç#â\]rSÚícùòþÏo?íöÓøëª¿}\x0011tx¥\x001cy¼2
²Ñ¶$9·¾Ñ=úõ¬·gQ\x0003¢õ*îÐ<\x0004BF_Ò\x0007cZn¶åí0Ök¸!©ÝÇß®Sæ\x0015§\x0014%\x000blóÚ\x000ch=»!B,»\x0011%U\èµÓÂÛ\x000e	;\x000c¢õ\x0000îHwVÓp[ïy$e!ü¶ª4¡õôíY\x0008EÍ5aJUY\x0008]äFk&L\x0015\x0004¦n\x000eHeud³Z½íxz1´ÞÝ=ÇÒpÃh\x0019DÙ\x000cö\x001a\x001bg$\x0003\x0016¸
½\x001a<Yx\x001aÐ\x0003cOùDx3\x0012bãÑßC\x0011Èå\x0000\x0013¹Í¾f\x0007÷ªêX.¯ß¨ði[Z¾\ÜîèÎ)b"ØÒÞBÈr0;\x0014æd÷÷Çm´$æ>\x0010'þÓì#\x0014©·ÅÕPÔÜÇ\x001e¯@\x0016\x0004\x000bs@wmAt¬¡ -É¹wAÌ\x0013®Ö\x0011ähH-ß!µb´dçÞ\x0003"¨/¿e<%\x0016Éåì¶\x00193\x0014¤%»öhJU`Íz à\x0011u>èÊy'¾ÜþØ²½\x0007Ö§CcIÚ\x001eµN¥÷§W}5°8½ÔÖL ÁäJ,Ö²	a93ÂæTÁH_«÷7²±Jw¯Ë;*"=ÞíJghÈZ^§=Òj~py>{=?§2âÙÕù0,\©J,\x0005Ý÷¹Zz2¬'ÊzßlP[õp/\x001eîs\x0017\x000bîX¾æzÜÝ	kYê{\x000fÓîI\x00182T*ÑÌ¤[S]íîÉ´fv\x000eð5Lfÿ¨¸I¦1ç?vïßP¤õüÂ
&ë¸À\x0002z\x0000ÒI·RÚÂ¤;wo\x000fÔwH£üÚx¹Hç×«\x001dÆ»`Í*\x0004å(X¬\x000eÃ¹cMGaçüø¬×°¦Ág£&pë¸`\x0004Õ¥'\x001anYe®ÇëOB`ýv=ï")<·\x000fëÛÝÝ,uiI\x0007åj_´\x001eÕUé\x0005Rê×³ÓËÙqo\x001fÎ§xª\x0016ÏXJÈ\x0001//Å µ\x001f»Vö\x0018<ÝÄÓµxBÃ°]\½H+\x0011Q5\x001838	Ï4ñLõêé²z0\x0018;Òê\x0015<Ó\x001c$2\x0006Ï6ñlõê)ö©ëiñ¸.÷#\x0002çp®zí\x000cEG²]dùä©²v¾£Â¯\x0006Ï7ñüµ3¡ØÐëÅ+xnâ½
M¼P§\x001dO;\x0000¯¥'T1mmgÝøp¼ØÄcNÞzs=µ\x0017ËÛt·/\x0018'EK(êåÜ\x0006JÆÜi\x0001µ!_º-©|-©,«ÅrÒ÷#­_\Wrúlìì\0¯%÷dµàK*$\x001bÑQQ^)¼j±ðM»¼²%[dµp\x0011¥}\x0006ð±-é¸f$ñM{7dëöÊêë\x000bÕèÜÞCPg`¸\x001f¥½\x001fsþÄ\x001fË»ßÌiï\x0010\x000f\x0016\x001b\x001d?ÞÝr±@0ñô\x0004\x0002Ã\x0018\x001aNx"ÙM.O;0Æ¥Óél\x0016E³ôÂd\x000b8z_Î1ØÛlôüêü4Þ\ß¾]ÝÞ>.Ë/¶(sRã(mÀ\x001aqc<6ÞÉ\x0001-Òér\x0004é\x0010y,\x0015ã0huÆÔëÕ\x000ch¥B%l\Ç\È\x000fáþ~Û-¹¶)úéBR¡ÐÚ1&Z\x0016\x0013:>J¯p\x001ez]
ý¦E\x0013
vW©J*$©Ç4z'LÀû\x000bTÙs;*²ª¤JÊrôDey­\x000cèQD3\x0012wP-ìÅò0^²\x0016Ë \x0016
X\x0002ë\x0007\x0001K\x0011\x0015RO¡ao¦JÅÜ03Aé\x0000eO\x0019Ê¢\x0002T9$4a\x0007!ÈÇJ¨$wC$*j\x0018¨$æ¸\x0002UN"\x001aOe!\x0007/*°¼\x001dÌT!ZL\x0014J\x000f¼±|®TFåÀ\x0001?UT_\x0001hþ3K\x0012t®d[¯@\x001d\x0015Ø\x001fùSCå¸3VÂ²äôKÚ\x0017±Ô¸Køñáqñ°\x0004.\x0010ô®=,=ê/\x0016Ð!\x0004\x001b%õòI\x0001iÔ\x001ao#ô¤Ë¯\x000376.\x000bQo½J­\x0011/fÐ1ärÞ+ï\x001b àÝÚ\x001aw<\x0014\x0014ÚxÒ+Ô¥¬#%P\x001d\x0012hp[û[\x0007*?_Ïÿ'Ñª¦s÷ùÇÅgvXî¸°Fk\x0016¹!Ù°\x001a\x001fõfîùÿ6{Õë¸lÒ|tr\x000c2O"Ý\x0010Iªi)£±Lgºb\x001d\x001e\x0001x7\x0006O
ÊÃâ\x0005LH|Ô\x001e\x0011®9Äò<Kh\x000c(Q\x0008\x0012q'>Çºþ\x0010ë\x0007³¯âíÕÉ4tÖ/â4éÄg£g>w\x0000¾õ \x0011\x0012+H`\x0001Ã\x0013æÓ¬%\x001eÝ­\x000f¬Ãü©ç\x000b8ÿ\x0004Þ5
dOóú©\'<\x000f:üæO=\x000bØÍ\x001f\x0000©Þ.\x0001*KvKV\x0000,#mê\x0001a\x0014#mpä¾\x001eI^iÖÎ¥éÖë\x0000á
fÔ\x0015±
çt'
ª½OXÖ=e8Ä
É¦v\x0014_C7\x0016\x001eýÛ\x000eúàð\x0015Qê\x0000"Pâ`ËQ;4vÉFt%@ÁGP\x001dâ
Y\x000f
ª\x0007Ô\x0006]y	P*È+Ê¡\x0008\x0019å\x000f°¹ú%ê\x0001¥ÅL£\x0004¨hÒD\x0002tï\x0008:á§\x0002ÂõP£îdÉB\x0005:Z\x0019¦;
£@\x000cäO=]0X¶\x0005n°¥!\x000b`\x0011én-\x0008ßÒ.?,ó£\­Ùª¯¹¾XÞ­ö\x0019lV
\x001c9/Aý/bFmçÉº¸æøâr~ÞÓâ¨E\x0007××¡³EA\x0000:EtØQ
èÄöâUÓéÜµ\x0004\x001dl'=¿\x0006ç8x\x0003«/a[=¨¦Cgì\x0008:c1f\x000bOÁ´DGÅÊ°vvûbTÓñÂj:¯Ø·\x0018|B\x001b\x001bTÆåÓà$\x0004Ýó§Î±û\x0018_]R\x000b¢,k'\x000fpî$ÞÙ\x0011ÖIÙ
ðdHÌ5Ixéµé[\x000bí±æÏ\x0018<C"9\x0019¾Ú1^Ñ©¦\x0014\x001bÊ©\x0011·ÖAr*
@¥>\x001a\x0013N:ýÖJpÉvAÞ@<ï1½	^[\x000fÃË`\x0018HÒqyo;\x001eÛZºÜ`,jé\x0002Ìy#]\x0000zåçB&%´øBí¶ÅQ'EÖöò·\x000fz7â fcar_nAàð|o£\x001e}1Þû\x000f7ßÞPì1G\x001c±×K·Ü\x0013«HFÇ¨·±P¬7W\x001a%É£þØÖákÆ*^\x001eCf]Oí_\x0011"3Áct\x0012\x001dË6=`èÿsÐ¦\x0014*ã¶ÝVc\x0010×7x\x000c£·b¬J¯p.VLÎÑ-±8¡q:¤Ç6\x000fã \x0005µ`50¾\x001c«Á\x0012¤(ZLÙlë¿«Oy\x001c(Góg=µñÙêöèÕ\x0012Sºú\x0011Ó¤\x0000=5÷þ³A9l!Ü¾ÏëéÏÎN^ÍÏ®z\x001dkD83ùSh"u\x00151"\x000fy
\x0019Qb$\x0017æ¸ù-M¡ðOï¿¿½m)\x000bÍQ«ÇåÃ¾mB¦Ð\x0004	c\x001ezÛ\x000bØ\x001c\xvu2¿ì\x0005üëZúÕM\x000e]	b+øêîïÿ\x001bÑÍo?,\x001eï®÷zc<B·!\x0014Þé4\x0006\x0012Þ\x0002ðzòÕyÂ=¾]\x001f÷\x001cÉ5,ëÔãa¡Ó\x0012lÀº80Ù± â¶Y<\x0016Ö'P?	\x0016üÔ`#¦l-Ãn;âú`{¢'
Ú´I^O¢
¬Ýz\x001b×\x0006},K»­|¦\x0005\x0013(L¢\x0015íÜB\x0002èì¢ÃI<ò H\x0008/çÏhZ\x00155ö6L´Þ±=ä?\x0007T\x001b|l÷­­@\þÇÅ¦é\x0019«È0Ñ®.±Ùà!\x0016Wê?ãi\x0015µ>\x0005[±¿ÛâK\x0011½¿ZØÜ!ÚL	Ðÿ\x001c\x0000KG£X&(¬¥=\x000c­\x0001Z36)\x0002½Ì\x000ea¬f7:Ø9°´qÊÒJHY	q#mJNÍÔs ~~ñGÖõÁ¯»1p~·x³_ûKö\x0015ûu¡O/¥ØXÇU\x001djAúáü|ö\x000c¿>Å Á\x0008bÀc\x000cØh\x0003®¿ÂIõÑrýåÖ»5\x0011¢3Úb\x0014¾ÄàÂr\x0011ÿ¼\x0014êC1B#ö0Q:ÎI\x0008ÂbKïÄh\x001d¯cî}\x0008FèeÇí5\x0013Ã¡ =¶âuäW?Y;­á!ís\x0018µ×`3:©\x0014¢ J·\x001d.¬A\<>º?ïàåàü)\x001d÷G«·«}É \x001c#'íX°A\x0001QÐìóíÕFÒÏ.Ïô\x0019t\x0005\x000fRDª¦A7\x0018Ï(8}¼CïyVì9c¢Wý\x0018\x0007F{þTãYº$Î°,E`6}=í¯Ç÷âÛç\x001cj\x0005ahZ:ÑÉêá:ÃOËÛ}¦VIÖÐò%³Ó\x001eï\x001báà\x001dÏàÉÙåq:/ç§;Ì¹\x0002
µlæ\x0016Õ
l4\x0003NL*ÈÊ\x0006\x0007\x0007
å\x000e-³Óå×eìJMþ¸\x001cÜdNëí\x0000µb\x0008çR®¼ýÖ(ýmXï'Ëûä%Ý\x0017Êw\x001c¥u\x0016i#ôÖylØí'óÿÞ§¡¯¡ÀÓmd-UÉ\x000e÷éWeÙÜñÛéwµT |EQI\x0005Î@Î\x0006Y]Ú)\x000c§YÐÿÆ!X³mõC~þ«Q$yÒNðßàd\x0002ë\x0006P\x0011Ã	0¿Îtfß©Z#±nõObÊâWü³Øßóÿ?SøùáÍoî]ãz¾z|·z¼¾ôÍ½
S(~=è®¬È]f\x000c»I:\x001cá÷êùÙÕ/gWÇ'ÁyÑw'×°­mÔ\x0004XY4y)±\x000b
¤q\x00160ÛªÓxXÈ¿\x000eb<l\x0012·\x0002õ<hÌLs'#»Ëú_¯-Ön²FÌî\x0018Æ£ZÅúKú^ 4²fT¿-©7z]%ð²iÇ×Ò*åþVSE*<·8rDºèwªX´>guøñ´É²Sxf-5hÌ\x001d%ºhv$rWÃBjþV\x0017lÎ\x001bèöÙú¦$I\x0017L\x001c¢öÐ\x0006ÈË°\x001e\x0002wxÁÒÞc!M\x0015\x0014pÑnç/TÂ÷ª{Óxµ[|Z.\x001e;
ôv½\x0001Î?±ô\x0004\x0014³ÙSï;x\x0002¶\x0013h~½Ï®\x0015ë­\x0019ù)\x0018\x0005ÉCÞaäÜZZ\x0005ÊsÆ»-\x0007Ä8J~DGQ&4Jµ\x0015P°j£×\m`ÚºM#)a\x0012åØµ´%!8É{öÜy¡éÎ§¾u0k(\x0017ññý}\x0006ÎU+[NÆÅþä\x000b(\x0013E¼h9\x00173zØÂ"îÌN{ÕÛ??ßºâxp·?.n\x001fîV·{îuLÿ´¤b
?áµ\x001b\x0003|;Û¶y¯^õô¿n2ò\x001ea\x0004'\x001dy "¶\x001dH²\x0004@\¿s¶\x0002QfÓ
¿õÁAë'´¡~<MÑ*ºÓÖoW\x001aVP¾Óöó\x0015«A\x0019eþ4 _.\x000c¨kuÚSG!4aÓ=¬Of4*ÈÊ`Ý>Æóßwµ®!áå²\x001b\x000fùPHpé\x000cô7LhI2åUf×³8\x001c27¯Ë\x00110f'3zÓÕ3£Áf\x0004R¹RÉQy$tþÔ3&Ñ#îu\x0004×S¶6,\x000cb¥Ýö~;\x0011w\x000c¤4y´BþÖSú¨±à$I\x0008¸æÀh¼àl°]Ý9Q)\x000f22ë\x0019Ø\x0010:=VáhsÈiÁyRç!\x0007¡ôrÔÅÚEÅ\x0002ÛV\x0003¥-Û`Uê[ñ©3Þ¶<z½¸¹YÝýÈ¿¼¾¹YÞ/ß~Üót[d\x0010Ú\x0016Ió-ÅÎ¼Fï\x0008ÃÏ^ÏNNÎÎÏ¿<>IÿÒ<ý³>áÉä\x0006ÚäÏ4rÃ\x0007Ë$òtËÉäFÓ«\x0000×/£ªÐÿ\Ý~ùñz÷<m¥Î.ß
H¯4Ás\x001e	älã«\x0004ÕËü¼û\x001dÉó_röbo¦\x0013±É\yß:¼d+\x000cÏä|6×1qÒõÉÔ8\x0000^\x0010yÖ¨ÆK&EkÂ\x001f\x001fóÄ¼d©;³mû\x000e¦SúÏûÕªüÙlGòrq}w½ßÖØ\x0002\x001d[º¨¾u7`²É×lLòrv|~ÜïöZ\x0013rç\x0011îI"4·íu)\x0017uÛÞú
Âoß>ÿ¹zÓh£Ñ\x0010'¯ÛwÉ~Ø§¸Á8J,Ø³yJ\x0005jÀ&ÂI£¼ë-?½þì>Ím
É5+ã(%UÕdJ\x000c-È¤
­)w=
Ê\x001e¿Æ\x001a³Ão8\x001cÓJºÏ¹YDJÉâÆ¨ílé\x001d^¸áP\x001fB[®"vøsR@'	ÊÞ¶lÇavúß\x0006sÂ\oMË	×2÷¹«\x000eñP]·áPI)òAâØ·©¹âK»¸Ë£¹\x001fS¥#ô1K"ø6ìÏ\x0016wwP5·Ò¤\x000coCã@\x0018i~l:Ê"\x001bÏfççWP9×¯!\x0015N2ã8ÐôÀPîUXøEöoÑDÕJP(ì~?c@a\x0008\x0008O
sJ\x0010Ts$cç'pÞ½YÝ?¾§îgOKAû#\x001cMêÃ¼§×\x0003yC¶Á9\x001eTÞÇÚ
ì;Î$ôdÞÏ\x0005ÞRÈ>Kr\x001b\x000fhÛe¨	@(mZì¶9QË\x0005Å
ÚÖ¯\x0017¹%Cú%º¤õ%§£¾¯k£sÂ@0èê`8\x0019Zqáa2²Kzqoo©=`ßïoåã»Ï¹(çË¯Ëû\Up½OO´6\x0016ìp\x0003\x0019nx\x0011 û^äéhRÄâùüõüâ2×\x0016\x001cïP\x0018\x0019U¡ù¿ãhMp\x0014w\x0017AxÔÊ,Ìvd(ÊþRÄ°úáöó½Í\x000f\x000bø\x0006|+Ùã_\x000b1?\x0016wïöì{á |\x0001ß.×LrJ¶Û­\x0014Ö¾ÓÍ@Äü>;ÿ¥G1[3nErj\x0018½'¿I"\x0011/sàÀcn\x00009±çé+^ç$}=
Ò)YíhtdZIG/_úÇ\x0007L*Tnahã(Ê Ê\x0003
eÚX	¨h¼TRNìvT¤ò§JÖÆ[xôÀ\x0001 e+_øùê\x0006îÑÉã¾zÀDãb NL«´ç´fãû\x001f=(Í9É¦ÍUÿÕù¼xóóÝ_MÃ°Õ*jhX\x0004r3Id&.O¹\x0010e¹ð;Òö\x0006EÞß.?<ÆfåíÃõò0-î\x001f®ßím\x0004\x0001\x0013
8^[BË£µrËr1?½<\x0013ã³ÙÅåñ/;I\x0016\x000f"¼k¤r\x0001Á³ôo,ß¯~ìUjAøPág\x00148YÑAx£öÛ­à7ÏÎNOç¿ýìÁÅ»´
wËò\x000bÂZ÷w÷_þÀFåÐüd9¬\x0017\x001e¸õð±0¬\x0007\x000bW5À²ÆÙ­\x0005;Ön=4ï»]&\x001bÀ
pà÷\x0004}a\x000fû6ÐznÍ'JÅ}é\x0015¤·ýw'èò½÷òP¿VÅµþÁÓ<«\x0011y[þ\x0018Pø\x000c}x-=\x001f2k]ÂÞ\x0007½S ¼ÿÞ_ºË¦
iê!¶\x0013×aO\x0003¥ÙH¸©|Ì¶»ÉlAöH<¦¢E¹Q)1§>Àe@O\x0018ØõïBØ%ô\x0006A*çðÛZÈ\x000e!ðJé\x0017\x001fb.Çmgg5ehSzJåx)a\x0008BÀS©/6ý®º!Zä\x0013d\x001eìP\x000b		)Äh1\x0018\x001dgfê°³ÒhÀÍqN7\x0019á·Q%uËQY¹\x0011P\x0004\x000f>p\Ø\x00017§\x001bò{ÚiÏøÿ\x0006ö\x0001HêuòÑÍrX5¯
¹é\x0002>Å²o-èÄø\x0012í\x0008{#Où(L*èí:þq÷¨þúÒ\x0011¼XÝ}Hç£\x001d3ÒñééêGúÑ¿Ý?ÞýÛ¿\x0016o`\x0013 òJè'än0\x001aU¤?\x0004ªNïp.9=û}~~ño\x0017Wçÿö¯Ù3X»\x0017gç/ÒcF}lþ¸ß¿æh+Äæ$Ó´By\x001fï®\x0000!;ØA\x0018­\x0007\x0013$+
>'õl\x0003Âæ}¾:?÷3¾û¼º]~j¿Ç[Ï_/
I; \x0007rÒ£1O&(kDIèË^º.¼Ý¡|[è Ò\x000f6CÖGéWéý^µºîM\x0011{GA\x0011\x000cæóA;bÍù|Ý+¹V
Ó¯NçÏÎz6¡u\x0013ZOÖæ¥\x0013
æBh/¸Ì<·4½Hö\x000b©Aø\x0019Ì, ¨uïïæ¯ß.\x0017C\x000e/\x0004(ÃÆæqÏx:$)m.àH°ÓÑ\x0001\x0017GóWÇÏç³¯°ß\x0008ïZGä\x0019´\x001f¡7»Ïiµ\x000f«í¼2 \x001c.¶\. ²wj\x001bøÕìüUZìùes±»\x000f¶ÿãíõ/bñP\x0012\x0017¿Íìã§åõÍGÀµë^¿¡nü:*iqDc:Ð0Æ\x0005NDî#WU\x0005,§Ç¹z«\x0019z½z9?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÀóÓæ2{à¬«\x000b ?,.ÀÓ÷wo+Wks©ÿèW?Ôÿùáîí[yÒÖ´RàþF5ÜØ¼Ì¶5w¾ºyQ¼Úhu\x0019\x0000\x0001@°\x0004\x0000 £\x001e/I]X*\x0008°)äÛ\x0001øùî»\x000f\x001fßo\x0003H\x0003d\x0007¨déÌ÷\2ÔJ°¡xiL\x0008\x00107u+fv \x000c\x0000á\x000e8\x001eDZÚ\x000eTkÕ8\x0011¹ÁMv\x00006\x0007ZOìÀ2i\x0005Àóì\x0000x\x0011^\x000c\x0015\x001eÚòQtCxùøþG?|2üþ¥S+~çñ¬Àë¯Fª9!ÄMÿjbýËÀuý<pæ\x000b»\x0000~8?Þôü8Õ\x0012çq¯ÒÕ]-¨^6é`f\x0007\x0013ä-O\x00107á4ÀE±¹×>µà7\x0007*N¬Q\x000e_×ÏÊáfë\x000fÚ\x0005®\x000cà¯s»Á £â\x0002·n\x001a¬ `I\x0001\x0001]«}õõ\x0004q°´¬ß{Ä"
88\x000eß?Z~ÿIü;ì,:£È"ûj6\x001f¡'6`U[\x0001°¬Ý\x0005 &\x0014jZZáÕ6\x000c~ûÅsbýðÕº~.\x0004þÂLhKÐßá;ËK\x0012ÁÕ[\x001cåy ¥lå\x0016ã#ÜÍÐòÚ*ÊkmÕ_î~þ×O÷\x001f®¾½{ÿë§û·w\x001fO\x000b<GIÞh!IÊ°v\x0017â6\x0015ó\x001bí_nüÏ7·¯¯¾½yõôÍíï£Á\x001e
Z£)ÒT\x0017Î2 r¢þÈE»{\x0015>'¡\x001e\x000c\x0019añ²¢q\x0006èf¯\x0012à\x00044¡G\x0013ÑTh
¡ ¼Ö\x0012!iÁßU\x0018=\x0001MêÑ$c4Q'.AÈ"ÃKDkõ\x000fíVÿ\x0000¦ô`1\x0004zÐBRSLä£Ú\x0000Ü-îG\x0003£E³6i)IÂ\x0013\x0002w\x0008°Z\x0001Øm8?\x0001Î`\x0005ÀÚ\x000cä :?\x0010jØ$f\x0014µH\x000bÊnëÚ	p\x00063\x0000Öv /Ze\x000b\x001c¢yYáÈô
Çúê\x000cgt´ÈÉ\x000c\x0014\x0016©>°Ú6ÖS\x0013\x0017võNáÈ\x001ewkõ\x00168y®dªµÁ\x0006ÒO®Ò2_/yäô«'ïÞ¿½¿ÿp"\x0008:nªúrQ"EÒÙâvXT\x0012¯¯¼|õâööõq\x0010Ø@C\x0010ÙË8RàV·EQKé ÃÑB	\x0014Ô£ ;\x0014¼ôñ8·(Uä^_¢âÎ\x0004èy\x0010¾\x0007á
·Ë}=vÙñ\x0018å<\x0005­	JÉò@\x001eE0Ü
în;QW-RdX\x0008°î»\x0019ØC\x001báü¸¤å¸\x0008E6_¡ÍP¤\x001eE²CÁ\x001a¤­¢¿þ³ü\x0017±^´=Gn\x001eEîQdÃãÚ'GA\x00054|\x0011½zH´Íó(J¢\x0018îEPå>ËÁÕ¢\x0006
]+±\x001aá9ÃÍ\x0008Az¡])EU~¼¾+'·­É2b¤mCÞöäõ\x00056\x0007í!&Ô\x0019Y5TÙ\x001e­1\x000fc n0dîÀ\x001dl­ü¢T\x0012\x0017ÊSï#£Å\x0017\x0013 \x0006Þ\x0006CâöP®¥<¹DyÜ'ø\x0010XªÛ\x000eÄÀÛ`HÜ<ó8âm½S\x001eÞî\x000c·{ n0dnÏml­ÒÅ3RIý°F\x00071P7\x0018rwpYZWªÑÖ\x0010ÊYïÅñJÑ	\x0018\x0003ë!íq
·×á\x001aÌ
ëÅ
Ô\x000c\x0005\x000e||ÁÊîM¡Þ\x0015\x0004ÞÍrY]hgiq\x000c\x000c-­ç'µ´²7jÀºÂàY°f0\x00063f\x000egjÑèd&JÁ§íi\x001aó®\x0014¬eT\x0012wßÙÝñä¥ä¨þmR\x0002¯ËÏêl'®NðCºú"KJä2fWd,{³»-¥qÊ¶ü<nËÏvÛ\x0012I^|X3Qõ]kX\x001bÕ%Ù9!ðp[ÈtW8#*+Þê®(¥my\x0013Ü«\x001fÿýõïvÇ«\x0012¢Þú W> v²íHZ\x0018y¸%ÞtKêAR\x0011ê-j(\x0018¢F\x001fÆæë§ñüd^*Ûà¨H¿\x0014\x0005\x000b\x0000n4L\x001c>Ü\x0014´Ý\x001a\x0012¶\x0014Po½j\x001f¬ùÃtæ_äÍ;¼Wë\x000fú^Ý´ÎÿöÓýû§Y:  s¹YÌaÎn÷)´é?öõí«ïw4ÛuýØ¯\x001fMÖOù\x001aÚòW½.Y4ÖòNÅê	Ë§~ùdóù5st:ß+SqÕõô\x0018®ß÷ë÷6ëOòÀSZ
ßÚñ!ýþÛå'¬?ôë\x000ffÇ¿MÈ<^O¿.§\x0016}~ù±_~4Y~\x0000y,¯7Èl]Öñ\x001ee÷}yrý©_²ùü$ÓÚ3\¡^_OÒ#\x0006ª=zý¹_¶ùþ^:²3cè´yu/xæÊñ$^é×_¬¾¡=¥Ö¿¿íZÕùå/YÙ\x0003y9õWÙ\x001e*2Ð!Áa\x0008\x0015\x001e1¥ãÑ\x0000Föµ¡ßUÎ±õ¤C§½$kê¡rÇ\x0007'=zý\x0003û
ýF/]cõ¬çkùþZA#Áñùb^ÿ@¿`Ã¿õ\x00027åªzÖýuzå\x0000\x001d\x001fYóèÕ\x000fä\x000b6ì\x001bõm(³\x001bÚ#\%]ýüðÙÒ\x00060°/ØÐo\x0004~kö3é°òºnPû¹ý,4\x000f`à_°!à$Qr¬½%\x001b \x001c9ì$¾ç×?ð/Ø\x0010p=ANNPÒ0Å'H	Ìï
	M\x0002\x0018\x0008\x0018l\x00188/U\x000fÕä\x0007)5w¹81a»ÝëÕ\x000fô\x000b6üËXÛ×N\x0007fV§\x001dh¸ýä0½~\x001cø\x0017mø·8uCuÿø?Eß\x001chWÃ~\x0012ÀÀ¿hÃ¿©ìâ@T_\x0008\x0005@özÊî8£I\x0000cøkCÀ\x0005%çXO{Ñ9eÅ­\x0016hWgnrý\x0003\x0001£
\x0001óúå\x0006«L\x0003/¿è
ÞN6¹þÑK\x0012AzØÔò¹¢j9¸í\x0017y\x0000\x0003\x0005£
\x0005·JÌ\\x001b\x000fYW\x001fõð\x0018&p _4¡_®Þ×¯$\x0003M\QÑµì÷gGM\x0002\x0018ø\x0017Mø7:%\x0000®f1õ,+¬§'\x0019^ßÀÐÀ"\x0016)e­\x001b \x0005î®\x0004©Ï­\x001b°[s<\x001b\x0000÷#\x001f[\x0010<N|<=\x000e\x000e\x001aÆäõA­ÆaNÓpÞÐ\x000c­Ï\x0004]*Î
Æ\x001fCx\x0008\x0003\x001f\x000eà<Ý©Ó6þÌ5¡¤nuRRÞ¦>\x000e\x0002\õ½Æ\x001e°úÃSÿtõÝÝ{~(<MTßs*¢\x0014ëZ,Ú&\x0001\x0019i×­{sõÝÍ«'ÇWýÊÑdåÕÉJ@n\x00152Ô ®|×\x001bzìÂ©_8}A\x000b÷ýÂý\x0017´ðÐ/<|A\x000býÂ£ÅÂ\x0017Ñxy¯\x000b2u¥s×çº]Æ}ìºs¿îlòÁ«\x0010Û4¡ºr©.à¹Êòjzì¥îQ+\x000fõÏÃQá¿¶øè¥è¬³\x001aÈth\x001e)_\x001d·5»µÿ³¦êqí?þõ³ÕÿÕbù9I)×±Ze=5ÛUýùôõ TT\x0018+>ùÛÝ¿Ü×µrÌm\x000ct±.Y\x0006pøÔM ¥ã¢Tüùæ»Ûú·CÁ\x001e
ÚB)Ð|NNtâuk
\x000f\x0000Ë^T»Ã\x0011%\x0014ê¡ù®,¥OuW0HB¿+;\x0007ë$,¾Çâm±ðü ¶-<\x0000¾uï`
\x0000RÛ\x0017ðG«Êç°\x001eK0ÞØ:ø\x0005)¨­]¡^÷mÏXì±D[,e_bÁp­r.M>®²?.9\x0005%õPñ¶PSÁÍÑ{¯3·¼y³\x0015Þ&{\x0012ÜcÉÆÛ\x0012¯Û®d öðWw\x0005å\x0015´Ø|\x000eIé\x0014S$,wïÚeY´ðcB\x0011ÅyÚ~C8\x0005ËAhy¡Ig»-õ\Q\x0003B\x0006rj\x0003íu(Á)ÙWÉ^²\x0013z_ÜÊ¶;3Ð\x000b\x0018ó\x000b+Ëu\x001e\x0018²«\x0003cJ0d0¶É\x0015KRÞ×wE|ÊûGÕ¼§°\x000cv\x000c
\x0019ëµ}á\x0002hjzO>\x0014Ý\x0018Ü~>\x0005\x000c\x000e×\x001f¯hê\x0015\x000bdó+&Y	f;\x001d{\x0012ÑK¶¿üº/\x000e%ÆX@}`êÃàpùÑúòG®A_?z]IRÆN\x0019n?ZßþÖ!^± 
CUi¿¡ÒÎö\à°\x000c·\x001fo¿V@S}³\x001al\x000cy\x0005\x0013·Õ,N\x0001CÃí'ãÛOxÛ)£\x0018ä9\x0006ý2,o\x0001ã«O\x0019î?\x0019ß\x0004\x001ew³¡´qQ\Ì`{ch¸þd|ý]\É*ú§6Ä\x00079J\x0013\x000f3\x001f-²Ã2Ü~²½ý)gî]Üå\x001aþ{ñA±\x0004ã\x000b3Ü~²½ý)ùëv_°\x001e1qüEhÛ8l
\x0019ä^G\¾ÃÊ\x0011\x000f \Ô!õfkúÏy3\x0007µuñgî¬ñ,¢P9au\x0008zÍ¹\x001d·LþhùQ<M\x0003\x000eÓâô\x0007ÎaÞüÛýÛõAðéÝûs!KLR²\x001cxtªÄ4	H\x0015asJÉÍ\x000f·/Ö÷Á§7¯\x001e\x0006{4hÆ;ëÓÔyzµ)â®ÑgE!\x001aêÑÐ\x0005ö&8y\x000e\x0008õmo"×\x00004éÔR¶ò3' ñ=\x001a½©^s«
\x000eXM¤\x0002RÒª\x0010üfyð	hB&ØïMnÏ/Á\x0015Ò<s ©ÓæÛ
lN\x0012{(ñ\x0002Ç,'ézáþ/®^6Æ«B5[=;4©GìÑ¤2¡08"ØÀ\x001et½ÁÍ ó\x00044¹G/aãº7Õ%XÍ3
\x001aþÕ\x000eMéÑ\x000bì
éPO_²æÎ©¨\x00144Í§¦y0KZóÀî\x0002{Cî:·ñ\x001eè¼¨Q`¢H\ÍófÓ	pFGà\x0002\x0000W\x001c·¢-ÏÍK­y\x0005±Ä\x000cÀvóÏ	p\x0006O\x0000ì]\x0001Ê¥H-c¤Ó¤0"(yÆÍf¬\x0013à\x000c®\x0000\À\x0017ð<Õ³)x'X\6Sÿ	ãâæØ²\x0013à\x000c¾\x0000Ø;\x0003´¤Ð¨zõ\x0000$j[Eù©!\x0018\\x0001¸/À\x0002`~¡\x001a\x0008\x0004ñÓ[\x0005Îv6í\x00048;\x0000\x0017ð\x0007|\x001c¬{ã&\x0007]\x0014¡¿àò¦äÑ<\x001c\x001cÌ4^ÀLsSTkÉ÷ÃÍL×à/«]Û|H?\x0001Îpsð\x00127bÉî°¿Ì³Ð\x0000`3 >\x0001ÍpÖð\x0012gyØËÕYgýB): ÈùÍ¯Y8Ru\x0008
ø¯/à°erÖlô2ç¨Ñ\x000e=ÞûÜ\x001ez¡\x0001è\x001f÷]\x0010Ê?cÂ$\x0005¸\x0001j¬ #HbÈêèlràj\x001dtõà\x001fì£\x001aÊh'ïä\x001e%J^\x001dëh\x0015&¬tãÑûë½Oí\x0013^d£r°Û\x0000 \x0018\x0001×\x00012\x0019è2gïÒ\x001bÕòxH!ê\x000fB|ö÷¹ûð¡ÂùïÿøÏ·ÿûÝ§Ór¡Ri¡ªã\x0016eº!!\x0006-VWh+;õìÛïn^¿®(®n^üååã\x0010°\x0010\x0002	ý «\x000ev«º^et1¦ÍÑ>Ó\x0010¨@»\x0010$¦®Û×\x0001T/ê6ljLcð=\x0006ÿEnCè!\x0004Ëmp¬÷Ñ dÕtäRfÅ°YN>!õ\x0018!\x0018xî²\x000b*\x001c\x0008°Bð[8
¡ô\x0010%\x0004\x0014²¨\x0001KÑÂxt!+Í0y\x0016\x0003vÕÒ°$¯\x0018\x001cué¨«e|J\x0003\x00117æ¦A\x000cf	,í\x0012ßiÁà¸Ì´a \x0015Ãfòh\x000c)\x00039ø\x0007m9{}÷ÛÛW7ÿöÛéc û×ñ/\SÖNR=J2*\x0005öÅ|^ß<{ñýÕÍ\x000fÏvf¤èú±_?Z­éíkë\x0007¡ÝDàu|MÜ\x001d16³~ê×OVëç·p\x0019¿Y\x0000ÅKÛú3îuýÍ¬ß÷ë÷Vë 
]\x0001ä1êùÑaHWµY~è\x001f¬_¼GËç×i\x000fIGmÕÏ¿×Ø5³þØ¯?\x001d\x001f\x0010Òåúzùþë¨0.¥2Zê×Ö\x001f Èhz|41B\x001eôô'ØkY~î­>V*Í\x001få!(\x001e¬gÜSrYé×_¬>¿:²%¸(R2T/uQë¹Û9±þCùýÂ^Î
Ë<AJÍ¿\x001cÿ"â¶lý÷º\x001bgÖ?²¯\x0015ý.c1u\x0003P\x0014m~ý°«\x00038³ú{Á|ùÊf]½Êç9Íòùwf\x0000\x000cä\x000bVì\x001b«ùñ2Ðjoó\x0000Ù\x0000+ç\x0001\x0006ò\x0005+öe££öÇEn¨æ3àz­\x0000\x000cô\x000bVü\x001b=®î;è §¸\x00020¢_\x0018è\x0017¬ø7pËßâÿç	Er\x0003tìs=A1ý,Á#Ç/j@ýµkí¡¹\x0001\x001d\x0008\x0018¬\x0018|ÿ BÔTí×ïoå¿Á@À`ÅÀs½ê?\x0017\x001d¿\x0019]¢Õ62¡8001pÒ)>u\x0007¢NwõÙ+°ù\x00144\x000b` `4£àD\x001cö6\x001fÎë\x0018¢\x0008yõAwÅ\x000cg\x0000\x0011°\x0015\x000bWoS}h¾\x0003E¼\x0008\x000cÖW\x0000\x0007\x0012F3\x0012ÎN¾~Ñé\x0011W\x000f4\x000f\x0003¡\x0019µG6?7èTð¨3*\x0000«\x0010\x0000\x0007
C+
èu<3\x001f(\x0014\x001càp~Ö?0\x0018Z1Xª~?\x0013ZiS¥%\x0003º¬\x001fa{`ã$ÂÐÂ"\x0015\x0011c¬>Ó\x0014VH¸ZP+'\x0008\x0007\x000eC+\x000eKì¹\x001d\x0006|öD\x0016+µé\x000elf£'\x0001ÐÀadÅa\x0016\x0015@õâDÝ'ÄÕØl\x000e]ÿ@adEaU\x000cÅHAçdVË$6\x0008ÑÈ£ÁÈÁâ:!Þe\x001cys²\x0000lOÈ\x00040&q­(,qlûþÙk\x0014\x0010Z íþ¿ÉÕ\x000fQ$YE1¡FÁ>d
ã#èk\x0012U\x0010@\x0003\x0007\x0015\x0007'\x001eM*\x0018¹h\x00188f
Ø\x001d>\x0003`à02ã0.Í4hu¢eBlZ/\x0000ú]Eü\x0019\x0000\x0003\x0019qrXV©«PÂú\x000ccEÂ4p\x0018qX\x0013²e\x0000±ZÓÖÁGI\x000b<\x001b\x0000~à0oÆa\x0015¦²ÖLht
0úþ~ 0oEa\³*\x0007(V
\x0013\x001bA«	µâ0?p7ã05\x000fadY\x0002vêÌ\x0000\x00188Ì[q\x0018kØH.1r-Z3¢9è[\x000cÏV4\x00020¾DÑX5ýëSêÊ\x0002Õ»Ö\ÜvÐ,Æ¼\x0015åêû¸";P´2%G/<Ldåú!ôf¡dñÒ*ÄY\x001f¥±xxNÊ»3\x0000\x0006\x001eöV<ÑÉ\x0018äjÎrÎ Ù8ÝÉ\x00043\x0000\x0006\x001eöV<\x0000D¦4\x0004Ôlî2¼¹±Øî`£å\x000f,ì­X8\x0013h2[LB\x000b\x00042I\x001f r
0°p°banZÒ÷¼P¤G¢ÎØE®!5\x00020ðp0ãa_¸ Ù $íË¬
jÀ(\x0019\x0011\x0006\x001e\x000eV<ê\x0015ÖHZ\x0011\x00113®É\x00084º\x0003aàá`ÆÃkY\x001c¤Ö>ÖX \x0007Ý\x0001«\x00134Ðp°¢á\x0014Òp5\x0018Nú\x001eÀÃÖ?X°"1ÖÀ÷Â\x0001\\x0011'Ë×ªDVÑ|\x0018( XQ@váZLhð"BJi]~±:>q° ÑÊæ\x001a}i \x0010ÌVcY"5@»ÃÉfÖ?ØherõÚçç¬\x0014H\x0017ÈÊ`\\`³þáúF«ë[ªë,\x000cÆ³í\x0014@Ô@Ì¼è8VÄYÝß\x0016	>õ¢¥¤,ç\x0004«\x0017mdâp£Ù\x0005þÃ\x0000@?z\+St\x0018Çù/Ã´Ôãê»0ñ"ï¤åMV'	\x001fâh£+«q@dÿt¹\x0011T4(0K
Qy\x001dTxÝÂ\x000cÄu\x000b3dm|ÀVÅðÙ¹²±¨\x001fFI´8}ïã©­éF\x000cç£4ö2ÿbôjF"{\x0004Á£¦L×î8²-K=´þìX%ÃcåÒú\x0000\x001e\x001d?Å¶S+ðÑ\x0015«\x0012"úìX\x001dXÏUÑR´ æ*Ã¹Ú\x0014Õ®åýñ_?Ý=8Zå+ùÍ¨*\x0007Ö¶\x001aDhQÎZ\x001c¬ÂP÷É2´X!»&xÜP(\x0014\\x000bd7%¦Ë{?;Z&+Tp­r$}
p(±°º"Õd=ÀQMÝ\x0015)«o\x0018HÅ´«É"­TÈJmÓÅj\x000fq ³Ü\x000fU\x0001n\x0000	²\x001f®¨é
`´\x001føÙ~ å~°LcáËáÑ-é±2«»mG4Ü\x000e\x001ej Æ*¦¸:¼¤YKí\x0019 ÓÖê3³kfs½Ö±qK\x001dJ\x001fWÒ\x0017\gU\x0008La C\x0010©,iãæ$êhFJI],Vù?\x000c]`iªp}¦C]¡'eÀr\x000e/Ã\x000b]<ôeê\x000fÝ(À¯ï¿ºù7jna=ör\x001bXgIËGÑÇÅB~7üûæÍÕ×·Ï¯n½:¾rìWç¯\x001fàr[y½ÇIVNò[ñVNýÊÉ`å¡uñ\x0016ÏS\x0018³,\\x000eK¡ýFû~áþüó$j9,ÅIÿbE	¶PÜ53+\x000fýÊÁÊA\x001e;ëÊQ§FðºðÝÆÅÇ~áñü¼ÞÏ¬³^\(ÒrYW¾Û±;³òÔ¯<\x0019¬<m¯+OR¢PW¾Zcóè\x001e½ðÜ/<¿p\x0016ÖOÒ¦åBÖuýiÙ\x0013\x000b/ýÂÁÂe4\x0000[Ä o!<dPÏJ
\x0007lV¾ôW\x001eXÈ¿ôÊÊB¤\x0013ÊkX©¶öGÜO¬|äO\x0003\x0002]éx\x001eÒ¾`¥9Ýfå\x0003\x0001.
]má^ôø«1§Ý*À\x000fü	ç\x0013(æ,îVñ\x0014$·è\x0003½¢\x0010l\x000b\x000c\x000c
çS(r¹ÜQ\^ý Kw»éÝ¥\x000f\x0014
çs(V\x000fäòSeÜíLî®Kß\x001fy=±ôDá|\x0016E\,K\x0007ÇÖ}YºÜÑúßgô&kÖ©¦è\x000f«w~õûÿÇÞþZ\x0017s¾À^ö\x0013nÇt4®£õöîÚÉÛ«çW·Oë_îÉ¶u\x0002$+\x0014º\x0004\x0014­\x0000äB\x0016iÆE
ä§3Èá9hµé\x000fº)_³\x001eÏô9ò)]Óbì3ð¶\x001b¼\x0014Kä´|þ\x0015x/\x0017ûåâYËs\x0003ËrKâ\x000eÇíz²^Ú-µäz©_/·Þ(ú(y@£ë\x0015ñïºÞMáÒõú~½þ¬õ(!hÎ¥\x001bÏ%"ÖzFv»ñ\x001e¹ÞÐ¯7÷}´NåìPÚ\x001d\x000f]õúMqõõÆ~½ñ¬õú$¢É+Å°íµQ¡\x001eÝ\x0018âëMýzÓyç!/y`jõ¤³rÚïÏäzs¿Þ|Öz\x0011E>çj\x001f\x0016cV\x001c>Ô{ÄøÈõ~½å¼ó@×²\\x000fò P\x0003éqHåüÏÛ6n
mN\/Ïglö¡ÀjÏ¢Ð¬ß×ï>=rÁ#½Ço\x0004×bÏª)&ÉLe	}«ÑØõð\x001e¹Þßà<s¾Í«\x001fô©ËÅ°~à¸[~ùÈ\x0005\x000f\x0004\x0007ç1\x001c\x0008æºû\x001c	´\x001b'Õ6Õld#<0\x001cEqÄp2j¬¥9è2r2 d\x0018(\x000eÎã¸jxåÊ¹ \x001aYõÊI|Ur<ß¤Á@qp\x0016Çq\x001a[8¹DhT.Dáõì\x0016°>r½\x0003ÅÁy\x001c×Æõ² `_ô\x0003íù³_ðÀqp\x0016É-S2Û;A5î×EN°&\x000bªá°°\x0011\x0003ÉÁY,W##ÉnÔµ%H¨_XT~Ø4½^\x001cH\x0003Ï"
ª1©ËzåI åõüoÐp°Àx\x0005¦ä¥ª s\x0004Jr\x001c@*ö«ÕØ\x001e\x0008ùø\x0005\x000f\x0006
Ï2hÄ»òy\x0017\x001dgL#Áuç/x°\x0010x PDß ^¸2B¶z¨w\x001fµ`ÂÁ\x0004\x0013\x0017g8×d*Ç¹kq"¼2\Ìç\x0007q \x0019=kèóó©\x00079°øE;\x0017\x0014û'­z,vKï\x001f\x001bËýøïc4÷ïg¹ï:\x001d¢ú>Q\x001fáÒzSÞí8Ü^òò¦1¬Ù\x001eý³=ß½÷÷û·w¿,	Ä×~ùêTí5Ð®>."ÅÐí¿:q[×ð»W/¿½}qóÍJ|ýæã\x0018°Çf\x0018býêÍû\x0004®kn[¸â¶y\x000cÔc 3\x000cc@­5\ä8\x0011@OuÅó\x0018|ÁÛíCÒáàëh×Ø*Áã\x000cRè!\x0004»mH«\x0013·?\x0017©Ü	tPÒÚ2?ó\x0018b!ÚmCu\"­B0Òü\x0013e.ü"\x0004³åÊÎcÈ=l·\x000fÕ\x0007bONN¢z,Zf\x000fä·lê4ªîbZ\x001d¸t?·;­\x001eouÔ´\x0015\x001d¢Ýa\x001fì\x0008qÛ°e' h3.­;a\x0007b \x0008°c²¶¤³Ü®JÃ\x001cÚ\x0004¶\x0015:çA\x000cÖ\x0015ìÌkÊa=NèVx\x0010ÇØ\x00071Ø&°3NÙÅu'HÝ;J%®ú\x0012O}ó \x0006ã\x0004vÖ)³Êº5%U,Ïp7Ìî\x0004\x000eÖ	
­S¡k:Ô¡£×"Õu'6\x0003y\x0010£çgx±\x00194ªûU5¯Xû6/çA\x000c\x0017\x001b
/vµ«^Å\x0017©³Nk·ýfÉÊ<2(vDòR\x0001R\x0003Às
[·\x000c	\x0008,=§¾z»yOüÕ~°
¸ø±±è©ÈI÷v¨p3yy
®»Aá\x001f¾@ö\x001e\x001b\x0016[j\x0008å\x000f=`ø\x0010
ZB\x0014µkÑ7ÕÉ&)FËå³×Ö¨ÑïX$Rèêê¿}÷é÷ßÞ^ýãÿ¾úáþíÇé\x0007wg\x0014}\x00104\x0003ês\x000f\x001d+þöåçÏ^\Ý\ýpûb§;@Q`\x0002íP\x0014n[j(
æ\x0008+²óA=\x000c2\x0011È<_\x0013\x001b¨0¢>]ìªÖÍ£ð=
obÍ¢\x0015Ò\x0019·d)å\x0001æX­ì$ÐÃ\x0008v0¢RèõYK¨ôá`s öi0R\x000f#ÙÁHR\x000bî$¡7¼¸]=ôy\x0018¥Q,a´\x0011Å¹EÒH`è«\x0008\x001e«í\x0001£¹µ³·<mQÞ\x001eã\x000fÁ!\x0015o%î\x000eÇ1X*04UQ'\Zb¨C\x000b\x001b¸ ÄöXõï\x0013íhéóÍéj·8\x0008ZõPwEÑl'©N<]\x000fÑtýÕF¦K.Ë*»Æp\x0004MÚ/]}\x000cÅª®Üø¢Áj>ÝU¹{ÿóßî~¿úÓ»ÿv¢	5,dù)\x0011Buið»¯ùåæÕí?ß<¿úÓË'>\x0005{,h%k'XH+\x00137W°ì\x0016»ÎC¡\x001e
ÙB\x0001·¶¾³ÂS«.EG]¡?zaæ°ø\x001e·Årx8\x0018eÔ8¹\x0018´Ç7íNÇ\x0012z,Á\x0014\x000b´fQrG@,\x0007ÁEÚ­ÖÇ\x0012{,Ñø\x000e£äÁdbê\x0019+a½ú¶÷%õXý¾¬ÛÒ"^ÞU}3Íx\x001aÜCÉÆPôY¿^}NP±\x0004Ý\x0016ÔÃRz,Å\x0016\x000bQ\x00173òjÆüz[6OrxZÒ\x0019cA\x0019ýÅGÌËmñ«Ð$íÎmÇ2¾-ëwÒ\x000eµPiÞ>²o¦yÔÝ	\x0006ó`\x0006Ö\x0007[Ú\x0007Î\x0011É\x0019s\x0012\x000eWW`½/ûó0æ±\x000c´\x000f¶¼ï*Ù\x001d«¨JnX(kmÃ¾æ<öÁ÷ÁÑ:h_×±	ë\x0003Ø\x00073p%Ø%-å áCÒ¬FkÕIØ\x00193\x000ff K°eKW¯\x0014/ÆEÉaë\x0004¸;\x0002j\x001eÌ@`ËÕ¯a8{#)K¨§\x000cö[,¦±àÀ1hÊ1TJ^O\x0019K\x0013	\x0018WV0Îtcp \x00194%\x0019â8\x0019\x0011B\x0014ôù¤\x001aEÕúú8¦$C%g½2Ü¤Øâd%¬ÏC»m\x0010ó`\x0006Ë¦JõÅ¢Ü\x0019\x0016Ým9f\x001d`\x0004uoLÁ\x000c\x0019M-3\x0015\x001e¢ ;Ãó\x001b\x0016§Ù£ù×9,-CS[Fu
\x0004Óþ+~}\x0001}¹K¦¾?\x000e¼rÒú<ÅþpLeãÛ

ë¨ ý\x0019\x0005óñ\x000c<Ä\x0004Æê1Ë«\x001cK
·Ò\x001c\x0007ë\x00046_lÝ4ü\x000c\x0012oÓ\x001f{àó]2ß&\x0000·: >È¤KÌq\x001dÕévu\x0017O\x0008??ÃäÌ1|½X¤rõ+¼¡¶FEI1ß\x00178z2\x0014«Ò[X={kQú1¡¨Ù ç³m²6z~y{$Î:å\x0019«õV£Ñ6OX\x001eb*ö'/°T]Ë\x0019\x0014u\x001aêÞiv\x001dwú\x001f\x0005©õä<\x0016dÔ\x001f:)'ÿø¯÷ÿøxÍ'%Ê´¨¥«NtRk«pØ½9·WOn_Ý¾>¾nì×g¯; Ö¼åâ\x001a¥å±	¶'Ñn¿Úã×Mýºéüïé:Ê÷\x000e:Ë¥ /K\x0015(LÖíûuûó¿wôµ\x001fGj´s×vÑ¥xÇbÝ¡_w8ÿ{ó([ík,×)¶\x0007j+ì3ø£×\x001dûuÇó¿·\x000bâLÕ{\x0019®eÙ9ë1µÚsËNý²ÓùÛ;iC*\x0007R'éeÓ7`\x001b[ûEg\x0013\x001b¨ßÚk\x0014Ë6P?vÚ/G{ôºK¿îrþº¡Hô]\x001cg{U5A[\x001d?¢zõ¸ewÒ\x001fL9ÎÀ\x0006ÆµÃ ùÞQ«jXÕÆdá#W\x001a%\x000fö\x000fî*­Ä¸\x0016lD£/>%Ï>y©câ2\x000cíîN~eùM¬ \x000cl	çÓ%¥$tY\N«\x0014\x000fH¶¬,\x0016Ìbá\x0003]Âù|éCÒÞé\x0012dh¥\x001dÕÛ(°/füèu\x000ft	çó%E`Á.þàPý*	Eà¥þëLx\x001e\x0006¾ó	\x0007¥4Öåëã\x001d{·6_|`L82\x0017yÚ&Ä\x0001¤£[:WGûiG/|`M0 M\x0012úÔ5\x0006é's1Ë`\x0010æ\x001fu\x000f¬	çÓ&\x0001ÊlD\x001eu ªônÕëtLÖ\x0003m¢\x0001mVö	R^ç¹Þ¦\x000f­õuÎäãÀx>k\x0012\x000fÐleÀå\x000ebR@&dTÃ¾;céñ\x000b\x001fCÌóY\x0000D)6Í\x001aªER²?"úèe\x000fçs&Öe\x0017ùÞE§\x001fº\x001aPÈç.q7[þèu\x000fçS&e·º³üåE¹\x0003Q/¦ÛW£ôÂ\x0007ÎÄó9\x0013kLß¾7:\x001dyî|Ñu\x0003\x001cS}äº\x0007ÊÄó)% ZÙ\x001e¯QÚX\x0002JÑë²Yø@x>ebõas³à^V>ë\x0007G\x0015\x000eç3æ"¡/7H´}+Õgýà<_Äbá\x0003eâùÑ«öuaU1×G)_ÀÛp\x001a8ÎçL"Pà\x0017j\x0015ç\x000eQGsT&5!{\x001aHÎ'MV\x0015oZ(\x0005«\x0012E;¨\x000c=Ä]ÍÔÇ/| M:4YÉ=5¤ÌC	ÛÝà¾\x001e|\x001b?ÆÄ¬\x0001mRQ?\x001c+mºf
=àÕ2=ØbÝ\x0003mÒù´¡h\x0012Æ5Ãé£ò=Äý\x001a¬G/| M2 Mð:Ã<©îçô^Ó§ý
øG/|àM:7«'./¨\x0017µùzR¤)ºz]»úÖ_øÀ?t>ÿTW\\x0007D\x0010¦uÊ\x0002~q°I\x0003ùÁûóÍx=+ë\x0017\x000f Í\x0012Î¼²\x0015\x00164Yø`
½5"Õ^RÔ\x0018Â;uUp¬ÅãyóÇ_\x001e0ç/\x0016arh	\x0015à\x0011 AÃdÒ°Í&¾¯kÿø`í\x001fÏ÷È£@\x0008\x0015¹K®ãg\x0000v\x0015¼gÖþÓµÿt~ø\x0016äE¶\x0013°:zÔÁ\x0019¹Z~^l\´>ç¸ ,?¯Ñgu\ôÓ§])ç	:úñî\x0001!Ý[ãjfØw\x0011\x0017ÀÉ8´c­r\x0013§æîÁ©9{éÄï³E,û0Ûmõ·M6YD¢Ï
\x001c\x001bRýÙÊ©¤	s)®jbá]|¸þh±üÀñsçZÐ$î*KÅê\x0003'\x001bú¥x%§ø£è\x000f]ùÇ\x000fwþõÓ»e]'i£\x0000­rymÑ¢â@KßwçÖÕÿpóæ¾yùì\x0011\x0000°\x0007V\x0000XFdj°Í$
\x0018µXêXN÷ñ\x0000¨\x0007@f;@Q\x0007¸ûR®cÓ\x000cò:ã\x0005áÈx½\x0019\x0004¾Gàí\x0010k=BE¼ù
\x0000VÑ£ý"ý\x0019\x0000±\x0007\x0010Í\x0000\x0004§õ«<ó5Ë¼ö°\x000e\x0008ß\x001fû1 ÷\x0008²\x0019\x001aF\x00059CQ\x000bp½Çõ\x000cÙÝQ«i±E\x0019ýÌÑC\x001chgªª -'¢Úªq¢âØo(ÃÑ+-8t\x001cµ\x0001¼¨6\x001cNíâ*8U\x0015l\x001c\x0007R_kdô\x0007­yñîãûûÿñÍÝß\x001f%®ýÏ
OYe±\x001d(ÖÖA°VÝUÓ´Û
ùâå÷¯*ow¤Á£0\x0013tÖ¡ï~ûýÝûßNð+PêÏsJÿØü
)lfå#­\x000fß={þòÕ³ãëÆ~Ýxöº©p¾h;ÏÏK¹ i¥Lòû'æñëöýºýÙëF}Ï,
é¤Ì\x0011Ü:\x001aÎjÝ¡_w8wÝ¾õTöuâ&-sä\x0008ÌfÝ±_w<û{»"5\x00049eÇÚ>í|^ÃcJp]wê×ÎþÞ\x0019E#»\x001eeÇÚJ­W\x001aßr´º¹_v>ÿ(±V\x0008ÜíÖÓc\x0002Îè`\x001ff5ÒUÞlU\x0016OgçDrÖetë ¾cm\x001e;Ë_HÇ\x0011aÖò@R?û»O\x001f\x0017&ýúÝý§÷'òh,ZÃ)µú¡9»¶øÈuOåC²\x001d$¾|óýB¤_¿¼}ójF\x0015\x0000ö\x0000Ð\x000c@u\x0004¬?IÁiurZ\x000eu#hód\x0016\x0000õ\x0000È\x000e@nöº\x0013mû ë\x0016äm\x001f\x0016ï\x0011x»3­ñ!³\x0014ÅbÏ\x0003µ\x0005AÜNôÌ"\x0008=`@BÝÌãã%ËV\x0011ä,\x0008Û4³\x0008b Ú!(-½Ì¼
¬òÅ£" íJY\x0004©G¬\x0010Ô/Ïuî\x000b\x0002HòØY\x0008§§\x0008¶û\x000bf\x0011ä\x001eA6CP
èò²ën¨(HEÐt »²=ì|\x0016Aé\x0011\x00143\x0004èI\x0005¸>5n/^\x0000¤í\x0011a\x0000\x000e
@í½ß\x000eAfe\x0005BHR\x0016â¨§W\x0008a»ác\x0016ÂÈÈviÉ©\x001e\x001bT\x0012y~¤X\x0010Ô\x0018 Xñ\x0001\x000c\x000cfÐ·\x0008u\x0013ðàT$õ*Üö+ú,Á\x0003\x000f_Ü\x0018]¶
_v\x0013Ò^°8\x000ba e0cåÄr+¹£¬­Õ\x001aµÜ!ð«\x0019ÓÀÔR{vY $z\I-
¼=!t\x0016ÁÀ\x0008`F	uÕH.3H/®U©ñeÞVíEE3Ê\x001aª¹]ÀNF³¨)´¾¿z\x0015h»ýbÚ¢ö©O±ªKö\x0005\x0018Ö%¬¬ârË°
Á~ÿ·ßîßòøµ­8:T
Ûà4®\x000f1ì½ã}ÿçg·Y1ö+Æ³VÌÕõNW\x001c5&\x000ekÆªnÄÞÃïcWLýé¼oÃµ,§tI@ÖÑ¨!ïæN\x001e»`ß/Øy(@J\x001aëÓZïU$ý]W¼«\x0006üØ\x0015~Åá¼\x0015§uölôa­eL::î\x0004ê\x0013+ýãy+öë8×äöó{¯º÷1îF?vÅ©_q:oÅ,\x0008¯©â¤¥Å"­É¨½\ÚcWû\x0015çóVL "uqQ\x001bq<h\x0017h,»\x001aª]qéW\ÎZ1\x0014/\x000599Ó¾UÒ\x0005§°ûlóÈ\x0005ÃÈ\x001fç\x0011ÈÒáÔlEö¨òäÓ:ÌÕ?`°Æp9@ÒLÁS©õé@û2î*$<Ú\x001e\x001fjE¾;Ï$/v¸dÔ\x000eàh5ÉdqùBÅnfY³Ø'ßÁv8\x0012K±KY"hÇ~Ì»Bf;«\x0016\x001fî0³GPèæýo\x001f>þÆNÝûßîÞ:x¨ \x0012yn-#î3[\x0000\x0000\x000f±Û\x0001póêÙëï±g÷êÙÍ1J\x0004{$hD«æ+\x0012Ù=\x0015\x0014lñ,Ä½\x00034z$d$\x0016\x0015¯>&#«U#A²«?
Ä÷@¼)DB¨\x0015\x0008ÉãT\x0005²nß5DÓHB$"É^e1]\\x001a\x0017$Z\x000b\x0005Õ\x000fÛóÉ§Ä\x001eI´Euâ\x00027\x001d7\x0019é$êá
»½ÓHR$"a\x0011Y9]IkXXLOWÜ\x001ds5$÷H²!à¸\x001aätyÑØ©H\x0002q¦«ô@)\x0010nÄ-É:;Þ;\x001dÙ\x0005)í6üÎ"é³àî+Õ±±¢
\x0007õty}pIÊ¯+]Y¯i(#Å[r|p	t(àz¼Àgwï¦\x000c\x0014\x000f\x001c\x001fX¢\x0008Çg¸ÝszSÒî(i(\x0003Ç%É\x0007VÀGÙ\x0014®7iHtL-äýÒÔi$\x0003É%Ës*Mõ¯\x001dën5;\OrãæÔà\x000c$\x000f,\x001fÐeï=©ß$ñ<\x0011ùÊq·
p\x001aÊÀò`Ió\x0004£#8­\x001c®w\x001e\x001c©_\x000f\x0003Í%Ïz\x0017¤\x0011¼D6ÕcÉzUân5
eày°%z6Z DÒÈCô^-ñn\x0016o\x001aÊÀô`Jõð]ÁêÑêeD\x000cÔ°Ñ­Ô\x0010ïðLã\x0018x\x001eMy\x001eÃ2ë¡ðÌ«Ü\\x0016*N/JÙ2p
r
pMT· êXHn=Ñ]	¦.1\x000e\x0018M-1Vóëèk$\x0017EÃ\x001cvÇCLC\x0019Ì\x0017/Ä\x0003\x0014¾ó
IH«!6
¸h¸òdzåEd[ÿ\x0003ïOM)YÏW6²^åa\x0002¯¸^ãùowÿ»_ßÞ\x0018\x0002£÷2 \x0013Yi®\x0005)ä¼éãa\x0017G\x0014ÿ|óíw7O_üó>\x0001\x0003ö\x0018Ð\x000eC"n[0¸Ê­ÍÌeQ¢ÁÄ2`V\x0018¨Ç@\x0018P&ÑWZ,òF@K?ý!\x001eb;Á÷\x0018ü¹\x000f¡Ç\x0010ì0¼Þ\x0007pRÎ\-môá¨øã1Ä\x001eCü2÷!õ\x0018\x001dÊÙ9¶ûP~\x0005CÒ}ûÑÇ\x001cÒc(¦ûÐ\x0012@ÈBµ:ü$Ë»_½Óû\x0013g0ÀÈ\x000f\x0004QÃ@ÐÈ¢\x000fÃ\x001bu#öç¸>
\x0004Æ\x0007$q%¹§÷ïÞÿzÿáêÕýÛ»O¿¼ûx*\x000eÔò
ÃT&9§ÅXv³ÖOo_¾zzûúêÕí7ß¼Ü\x0019E­X°Ç¦XF\x000bIbÕËÑFëæ¥Ù­EæÅ\x0016
õPÈv[¨Èh]Ö \x00147êÿ#gcÞmßÇâ{,Þv[\x0002ò(íöXu¾fÑ²+Ha·qm\x001eKè±\x0004Û}©XÚ\x000b¢ã\x0014Òní¼&¯cÜµ¿óXb%~Ùûz,Év_bü+õê\x0014áH¿a/é;\x000f%÷Pò½-¥ÇRl·¥RJmÁ ²©êµ\x0008¢Úæ½hp\x001aËáÝjaJ÷Eo\x000c´oÌû%ö«\x0008d\x0007\x0001ÿ?m;»úvó`\x0006Þ\x0007[âÇ\x0000×É70\Ã)ÎLÖfUGSâøÁùëí:¾êE©ù%¢\x001b\x0003»/½ó`\x0006æ\x0007[êg³\x000cBxð#E½ÿ¦f\x0019\x0006æ\x0007[ê'\x0004\x0019ÉÈ­\x0007ËÆ6×ån\x0012x\x001eÌ@ý`ËýÛÚõ'\x0013\\x001e*\x0018Ú­È\x00073p?Ø?Q\x0014ùÅ\x001aÌ'\x0019iX\x0001ÈP"\x0008yWQl\x001eÌÀþ`Kÿ¸NXª÷?´{5Ì¨?ì\x0016DÍ\x0019è\x001flùk]ü,ªtURÀ´[F=
\x0006\x0007þG[þ¯ Õ¿Õ\x0000hÑ\x001dJÂÖ¥)câ@ÿhKÿ<»Æ\x000b\x0016Òõ@nLÜ\x001d9\x000ff\x000cûméªk\x0002&\x0015Æý¡ì\x000e>Ç2Ð?ÚÒüå}Îå¤8<VMÀìVkÏ\x0019è\x001fméj(Ä\x0005º\x0016W&ºõöGSS\x0003c¢-c\x0012«Ì)ã\x0008SÀ$y\x0011ª7f÷µq\x001eÌ@2hK2<+Lo\x000c\x001cN\x00198=eTLã2\x001aì2\x0019Ûå\x0002+K%b\x0019!j
3pÖÌ\x0012Ì`ËÈØåÄSÛÛÎ\x0004	2	ýk\x0014jÃ?þuÌ0ýÕ6dÒ{RCfä\x0018­ÌÊÿÉ[G}£®DÚbÕ\x0016GW"rò|qaMÍ¦Ý¾×S¶è§q~2Ý¢\x0018×¤9kIj`Ñ¤\x0006Ù^æ×\x0011Í¯¶\x0007Î_KÅ$\x000f_)rÞPkwôrNB\x0003ãõ\x0001Ûë,{²¶yÈË\x000c®WÇ8Ó¼èâw\x001bóíÆ\x00142[\x0013Qê¯\x001d+»«§À¹\x001báÜ}É·\x0006Æ[\x0003¶·æ\x000f=g03°5g(ò¥NZ\x001aõ! Ø¦Ïê9ûy<g?Û3é`Í÷$§Öv5ë¹\x001fwæþK=dàz_y\x000bP_3? Ko+!«Ò¯Ã Ú´ÛB@ðÐ·©¬fìÛð\x000c°Væ³¸ÒHIó«+m\x001a\x0017ÔÛs?Þ\x001eÓ#\x0007u_¤*ÜqÌÅ\x001dPoÀï{:åÔ=ô>¹÷´>t¦Î¾yMÜæócj¿´twú+úC'vü§»O?½ûôþ×IÁi\x0016z8üü¡þÏ\x000fwoß6ái~^[*jB=fjí²v´ß§þÍ«?Ý¼ùúåWOP\x000fø|Ï_\x0012\x001fioÅ·ô-ø¤ÜBÚ\x001föv"¼ØÃW÷Ì7tE-\x0014S+ºmM¬3àå\x001e^¾$<W®}\x0010|´Ê¢'ñ+*>8"c|
¾å={Å§ïÙ\x0000HÜ\x001b\x000féç\x0006àkÁ'\x000fõ!Å}ýý\x0013á
Æ\x0005.h]¨ø(
G
4ã¢í³ÿ\x0003\x00177Ø\x0016¸ q!.ziO`Áç,ïyXÿRñívuLà[¨
\x001eÖ%B«K|ò·û¿ÿöË+¿»zòþÝoÿ~\x001aËÈÏM#Ï¥\x000f**ø¹çÉo¿}ö\x000b,ß\=yõòÙÿu\x001c\x0007ö8ðËÃQÝq?ÇµNôîÃÇwo¯¿ûôo÷§:\x001d¥ö\x001fÅ3Ï\x0011.teßÓ½yýýË\x0017WÏ_¾ùávÇR\x0010Ø@C\x0010!JxÌÑÞUC¡ÃÜ£Ý´Ý\x001c\x0008êA!D×¡ú\x0010Rµ\x0013å<U\x0010»½Í\x0018|Á[nDY\x0007P\x0005É	×Hº\x0011û¢v B\x000f"\x0018¨7[Æî\x0000\x001e\x0003E\7bGx\x001eDìADK\x0010g°/(\à§º\x0005\x0005i%þy:\x0001EêQ$C\x0014\x00055\x0017GEëò(zÝ¸Ûú;	"÷ ²íy^ï\x0013%\x000f\x000eÔ~\x000bà$Ò£(v(BöJ\x0014t/"¦\x00085\x001c°;PbÏî%ß\x0015äù\x0011.u:Ä)í\x0017\x0014ÍÁ\x0018YÛ¶ëJr1XiôLÀð¸ÿ1ð6X\x0012wô×Ø\x000e(&­*`5°¶c=\x0018\x001b,©;hÅ-ð`f)\x001f
\x0005t7p·ýl\x0012ÆÀ{`I|DêF\x0011ául\x0011"H\x0007c\x0001`;úî3jÂ×É
I*\x0008Ç\x0004Ø^¥*\x0001Æ\x0003\x0001\x001aÒxz\x0008&Ù)^³5×¢è½»)Y\x000f÷!\x0018²\x0005ó\x0007:º¥,h¸¾\x0015ìKÊ! Eé»m¶lº°_78åÁ¶\x0014ã3õ\x0019r\x0011ùjWfÜ½z\x001cLKC~A8zq÷ñ·woï~?7¥·TÚJÂ¹¬CLAî~ue¨ø¿¸ùþÙË\x00177Ï÷\x0012Aá`X 5\x0010òÇ(3H«ïÈ!HÒöøùY$Ô#!ó-áXJ²¬Á¯m\>Ë\x001b\x0000Oz±Bâ{$Þþp-¢µË@¼Âç(>KÈqfÐ\x0004Ðã\x0008Ö8 «\x0006YàA*ÀàtGÒ±i\x001d\x0013Hb$ïH\\x001f(
>6\x000eÄ«×}\x001dg¤\x001eH2ß\x0012nªIòTdú\x0008²º³>\x001d\x00013$÷H²ùø #-C`-²¶'® `Ún\x000fERz$Å|O|iËóWÓ¨\x0004#²J!í4:L"éÞô8Ún
\x000fIMI ¢Ü³%/yy'N2\x0012¼9Ã×@ëZßìt!\x0016Oº)q»út\x0016ÉÀð`Nñä¦\x000c\x0014\x000fæ\x001c\x000fPÚLÃÂZ°L.­ªI­W
ì­\x000c\x0014\x000fö\x001cï°Ítco¥rcÛ\x0013Z9\x001e¶kµg\x000c$\x000fö,_¯ì	G.B)®d}?Üî2°<Ó<ä¥ú m
¨î~ý¤.¤\x0019æÁç]B\x0019\x000cÎY\x0017q1õQ\x0017Í×@ó`Îó\x0010T]¸:x¤\6I³yõX¶Õ£f¡\x000c<\x000fæDÏ"õE\x001eÚëñ\x0012ç+{uYÒN{ö$\x0014\x001c\x001eÍ\x001e<´YìGzÑÂ\x0012@KvòvßÜ,èÑè¹vLw¥¢òþaíÛ®[2ÆòæL\x000fDÒ2Ãb2m£:-N\x000fØN!Õ,éÑé÷j=¡ôec\x0006eX¶\x0005¬g¡\x000c\x0004æ\x0004YY]\x001aæ8Iq\x001däÚ;Ñ\x0017\x000eq§Å|\x0016Ê@hO\x0010¯I\x0008Ò\x0015~ÿmE±I+ÙvTg¡\x000c\x000cö\x000c	^´¸Ù\x0004¨+R²+;\x0003]f¡\x000c\x0014ö\x0014éHtSë® äðª\x0007¦é\x0014·\x0005¿&¡ÐÀ+dÎ+<Õ!Ê]I«\x0005ËÑ©ß²Ý¶0d \x0015²¦\x0015*\x0019äÉ.PvüÇå|\x0011©\x0001\x000bÛcvf¡\x000c´Bæ´²ø-b£W\x0017¬ú-´:VWÆ\x001c±5­,ª¤¤ó¨0É¼Ôº+ÞÌ\x0005£!$ó\x0008²þ[[»ââLfñðq5Å°ý2d H²&HÊ1K« ç¥¾6dõ%C6{ TÈT\x0016$âK2
%®P¬\x001c0\x001aHÌI½\x0016\x0012·t$\x0015{-J*Î,\x0018¦!î"ë¸ë\x000f<_~ GoOèxôps%QHbR\x0019bv%­Â.?ð£7çÇÌs\x001dÚ¦`Ý\x001fqð\x0003Ø¯°3tt\x0016ÊÀÞ\x001f«+,o¨\ÐA\IPRÙnPE2Ð£7§Ç\x000céZö$\x0010gõ=\x0001Í¯ÚÝñ\x0001Õ\x001b©\x0014¿¶48'µóÈâ
âÛÙ.?p£·çF§Ï\x0010KÏh»ð¾hF²Þ\x001d«ØÑ\x000fÜèÍ¹1\x0015wÝ¦²\x0006Ä )IP\x0002lk_ÌB\x0019¸Ñ[s#ñ¸Æ(Rt>+&­
;Svf\x000cÔèÍ©çã6aÂ\x00005ô\x0012+ìh\x0012sÑ\x0017\x0019\x0006n\x000cÖÜHÜÒÚ¤áñÕ÷ªæKÓ,ÁìÅ.\x000cÜ\x0018Ì¹1Ö«ÒÆÐUÛ«µõXCGq#=n7\x001fÏB\x0019¸1Xsc
¸@¹£äq;9Q¾¬»bfÃ@Á\x001c¹÷¤ÍÑ\x000c®he7b\x0011Ù~6\x0005V±c\x0018ø1Øó#V!YQÒcL¨WÌJ¥ÂXbdÎÑ^\x0015²TF#®¬RýL³«2$WurJõè%¹J!È¤0Á«×bæ\x0010ê=Õÿ¬2P}°§úêÛgI\x0018-m(mS(é¦ðDM\x001b(q ÈhNk¼Å\x0014×
K\x000fA£\x0014»×Ç8J4'\x001c\x0017	Õ\x0005	\x0007\fI^Ó,Å¬¢%\x000e8[â\íW\x0010¯¸¬ï\ÁëùZ@\x0019A\x0019k$ÍíWÆõ\x000b\x0013H_c\x001eõE%ìÔwÏB\x0019n}4¿õÙ¡´
-ó\x001bE{Ð\x0017-:¨&ÎÊLÃ­Oæ·>eâ'Ç\x0016Aú>\x0006
»ÐÌ\x0001KÃµOæ×>EÔºhäAbB+ÜÂÕ ¸máñY(ÃµOæ×>y\x0014±¤z?\x001c\x0016k\x000c©wÅg²zRIÃµOæ×>aVñ\x000f?é%X)¢Ô[MYÜkÌ¯}\õÓ\x0003x/C H]IÏsmäáÒgûKïæZ¸~Jh··{zÌÃÏæW>úê~%¹j`ÆüoÅôy¸òÙüÊGdÐÈ\x0012>6\x0011è
\x00054z,fé	¦´>\x0018^ºÒl\x0001ñ\x0003j;cõ¸	\x001e\x0002/ÖØì¥\x001e´/m\x0003Òö¥VçÅø\x0010QõÆÌ\x0011U,jc\x0001¦ ªaõò«\x0017\x0013ÌO\x000f\x0011ùt\x0001DìÌ\x0008m"\x0014v\x0006ÄQoÙmtmúÏNÝ\x0005\x000e]Ý\x000b\x000bQ=}wQ´â\x0018ÍJwüg×È_à\x001aQ\x0002XsÕÉb\x0016¢èT\x0016Ý\x001eÝ>YtzûÌuø\x000f:â2°\x000eÑ«÷\x001cq{¢Ê£Ñ¤\x001d«©ëXýåþj]èyå"Aöªa¸ U®«Æ^Ù\x001eA°\x0000ùæöªýåQ\x001cØã@s\x001cii·U1=§\x0015bZÀá68¨ÇAæ8ê.xtdã,õ;@ëÍ?r²\x001e\x000fÄ÷@¼ý¬\x0017¾ÒÌZ\x001d\x0016´&¡ºÿû,óx ¡\x0007\x0012Ì iEht~}4.ÍáHLöx ©\x0007¾Ü«{\x001cù\x00128¤ë¶úf\x0007\x001cÚ"uÄÃ|4\x000c\x0018,\x0016Ø,\x001f5\x001a«\x001fãVª§ýw;óÒ&\x000c7\x001dì¯:+EÂÚ\x0007­5ù*\x0015`uÏ»6¯Ô·yÙ]tàÓ´\t\Æ>·\x000ejzÓöhÁI$Ã\x0005\x0001û\x001b\x0002sSo(ëw^ sØÈ{4®¡(õ
EfH²cu&í·é\x001b9®
Ç1\x001b!q8øÁrp¿@<ð\x0010\x000f\\x0002Ï%9e\x0011¡ò@\x0018S!Ò_>]=ÿxõäÝïïÞÞÿ~õû»·WO?ýSÐ\x0003ðæÈ\x0008+,2Ó£j\x0007\x0000§_÷%oõäåó/n_ýåöæÅÕÓ7ÿkOä]±a
/-uC \x0004ý\x001e³Hd\x0002¿\x0003^\x0004\x001bõØè"ØÐÕ}9j\x000ey\x000b\x0019\x001bAN:bH\x0015Í÷ØüÎ$IÇnÝ7àaÑíL\x0006\x0011G°'õt:¶Ðc\x000b\x0017Ú·"b®²lÏõDN¡Á¶-öÐâ ^·´Õ#YdfLp»ÓðNÇzléb¦d\x001d[H2½¬\x0013=\x0002\fßr-_ìH\x00169)ËtY>:øÏí	*\x000cí ;º°»\x000c6\x000cM9¼bã~­fJ(èì\x0012·ËoÎ\x00027Ð\x001b\ß\x0010×ñ)Ò5
6¯ÐMÂ8\x0011ÚÀ\x0000p\x0019
ÀpG¶}ó:èÈ'cæÆðÀãÂÐ{\Oÿñ_oÿñ_ïï~¿z~ÿóï÷ï>
/ÕaTaß\x0008 ¢"\x0015.P:$Oo_Ü¾ºy~õüöÉóÛWO\x0003¢\x001e\x0010Y\x0003
\x000e@&Ó\x0003òl­f\x0017],â>²¾¡1"ß#òæ\x000eJmÀùÕVåV\x000f1)íN\x000e=\x0005Pì\x0001Eû3\x0017\%À
RÛ"î[(¸;êè\x0014D¹Gí\x0011,åíõÐõÐU£¡n»_ýDD¥GTì¯¦÷¨VNí\x0001E\x001d\x0010rÞêx\x0002 \x0003ùb\x0018È×Î0x©\x0010\x0007µ\x0015åÔ%QÚ²«Öz
¢ÑtÛî°è\x00085\x0019p`½ãÜ6)H!\ýíXT2
i0Þp\x0001ë]qõ\x00145ø$j	wÔ\x0012N4Xo°7ß<\x001fYvuÅ¼ì\x0012¨3[=vcû}Ð\x0008G\x0015\x00153f$GR\x0005PÝ<1à Ro°£Sy"¢Àª¹K­\\x0006¸â¯ËxX\x0003¶\x000bÉOD\x0006DÉ~¨¨\x0002:\x0010H84è\x001eÁv7ò\x0006\x0005s­öN¶¨¾M	ª\x001a;O«e°>t\x0003Å=ÇÖF\x000f\x001dh£Ç(dÝ±ÌË,"\x001c8\x0016í9\x0016\x0010DÜ½:s«§
Ò\x0005y§!öDD\x0003Ç¢=ÇB
2\x0014\x001eBÑ4zßùX.b\x001a\x0012\x000eÐ\x001e_#$Þ//<*Çn\x0017ih X¼@\x0014"\x0017/\êÀzH\x001c¡´£Gv¢û
ÃDØC\x0001u\êû"ý^µÉ*ßnKûê9|\x0006+\\x0000Wµ\x0013Içðp\x001d\x0013ò-Z\x0013¦ô£K\x0000k\x001eEXó(÷W¿ÿ÷üçí¯w¿ÿöñ\x001fÿõÕ#^áê¿â«ïîøÏ©Fw!7sy>R«¦s¥×YÝs\x000fÅíÕó«Û§õ¯¿ÿç\x0005hÃú±_?\x001a­\x001fËulëo£xõ\x0007yjÏ\x0001·Õ;§×OýúÉfý	´ÿã\x0002\x0019 \x0004Ng·æö})\x0000¾\x0007à6 \x0016éÅ¬'(H\x0004Wÿñ° íV¦i\x0000¡\x0007\x0010vÜa\x0007
kÆ,\x0000ô\x0015"³è \x0019Ø\x0003F\x0000\T\x000e%%\x0002çîÀþÜ9\x0000©\x0007\x0000°@}j;ç0\x0000Ðd\x001a[¦]\x0002{\x0000Ùê\x0012/qþ\x0002À%Ö\x0002.\x0016½Äû\x0003ò¦\x0000,I¦\x0003\x000b8#\x0004XÄG¬@SÎì.ê\x001dØnMÞêwDö!ªg¿½&ÖM@\x0011\x0017ª×\x0000õ\x001eÇÝI°³\x0018îF\x000cwFlæE´Ï$ø\ñ¤Wö3|st,RGÉ«t.\x000e"Ö\x0017h8¼4UZ"ýcßA?C|»ððy)°[tóo÷oy¤Ôý»÷¿Þ¸zòû?þëï÷o¾¿ût¢\x000bKÕÀ«\x0017Xß±5Qv¶×ÿÚDsóÃí\x000b-uûòÕÓÛ×WÕÑûööÅÛ7Çaa\x000f\x000b/\x0000\x000b¹G´Å!½#\x001dÜ\x0006m\x000ezXt	X5jÒá\x0015[\x0007·¨»å6ëzÏå{Xþ\x0012°ÀÉ\x0002\x001ev$2õE\x001e¦k$µ°<\x0003UèQK B§\x000fHÛ\x001dF8qx3\x0018{Xñ\x0002° \x0004\x0011J¯°%\x0015ÛP\x0001Ý¬¼Ù\x0018w\x0006ªÔ£JØ,¥<«ÅT°hY#ç·êÏ{Xù\x0002°¸ñW^Õ|q\x0012\x001d\x001a3¹~ì\x0002W«ô°ÊvKÆ!ò(.u·îÖ¦È×é°ú'Ð°x§öÛÅéL\x000cKÃ\x000c(´\x0005þ\x0002&\x0003F'ã\x0012^\x0006$'\x0003Ç¸`QÛwj4Òæ\x0010¸3p
^\x0006\ÂÍp\x0010D\x0006|ð2w»FÝ:[\x0018XÀÅ\x001c×àfÀ%ü\x000cÎA£à*Y%6ÕllVàkð3à\x0002\x0006¥ófå=\x000b5A=)î«Ûu\x0001g\x0017\x0006G\x0003.ái¸6\x0010º\x001dCÔÑ\x0012õoèõÍü3p
\x0006\ÀÕ ´è,5!ª©+é7®\x0015³çd\x0018\
¸¯A\¤·Võä\x001eÃíQÞgà\x001a|
¸³Q·k\x0011pneV °1øµ¶\x000f7§zkp6à\x0002Þ\x0006¼xóÛÌFÌ±½\x0004£«¡9.\x001c¼
¼·±Ú8àU/Ä¤C¥·sgà\x001a¼
¼·A\x001dx1óìÖ«Z\x0008C K\x0017\x0008Qp`e¼\x0000+Sf
¯¶_\x0004¢\x0010úZ.\x0011$ã@Éx\x0011J(\x0003\x0006ª³U? 0å\x0002FÃÅñ!#eþáÿ\x0017\x000cæÂCpá"à<«ªKYmð$½Ù<sMplúãýþø¯îFSï\x0004Ë\x0017 ½\x0000ª%$#é	älë\x0015ö,#¼\x000c¼¸ø\x000b¼\x0018¤¢\x0013¼î àf\x000bÖYè\x001e\x001cÐî"'Ô"B!¹3\x001bÏÎáêi]À!ù\x000c]¹q©6RÆdUþN:Æh\x0019Ã$ü½)rNrç!¼Ë óPüj]P\x0007ÇcI´æx.±yøÙæáæ\x001f:¨Fy|OZ¦}õÕ¿Ýÿý··\;ôõ»ß>\ýR¡}ýþÝ\x000f÷\x001fNU\x0019/pzû°"¢­ö8D9@9mË'¾ýöÙ\x000b®\x001eúúå³×WßTh_¿zùúõíNã»âÂ\x001e\x0017^\x0004W\x0014"wuÇàW? ´Y
r\x000e.êqÑEp%.\x0010oûåEJ©âÒNêÁlezÎÁå{\þ\x0012¸J\x0016K¥{}È"\x0011\x0005ìL_\x0000WìqÅ\x000bàò  x6DëcÎé!,â+g:$°\x0016£\x0011.²[eÝ­X=IÙ,Ñ¼¯¸.p\x0006\x000f\x0005VºÄf9h\x0005|\x0015UÚ
KÆ\x000cVXi¹p=lIuaÐÂ«h>}üx2\x0018ôáÚ54..®'\x0015e©¾Æv÷°¨T\x000co¾ÿþ1\x0010°f\x0010Ø(\x0000\x001b»\#eFò²!I\´Ä@=\x0006²ÃP­ÙÒ|KIIïCu\x0017\x001a7ãåy\x000c¡Ç\x0010ì0PZ
s+\x0004Vóm\x0010|TKe»Át\x001aBì!D3\x0008\x001e]SS­G	T\x001f¶bÝHý<ÔcH×Az*ì¹\x000c¨]\x0007©»à\x001a¿cªdÇ{\x000cÙn\x001f¸ð>,\x0018R^ÏRuÑ\x0014Û.OÆPz\x000cÅ\x000e\x0002läÍ}\x0010=û
Ì \x001cÞ°¶ñ\x001aaàßL+ëfÈYYAl·\x000f02\x001dÅ-Ã\x0005D5L­â¾\x001e&\x0011}v\x0011mãÀäbµL©ÝêXwBzÃs,Ír¾\x001cÕµ{<äÀåê"Û<'>NEK\x0018Dr26ÛrDÛy\x0006ÄÀr`Gs¾ÚW*\x0002"Ün\x0005!ï+õN\x001c\x0019å4\x0003bà\x0008°#	¬£FÖç:4\x0003è[pí¡\x0019YÃ``ÁÎÂ²J0A\x0003Ñªò;á\x001e'ogp°Nhg¢£k¹×ÕH={&XÍÂ\x000eÃp¯Ñî^s\x000bG\x0001\x0011´¹1\x0007iMwÇ¦kÌ`\x0018®5Ú]ëH±
;¨\x0018\x0002ñ¹Z0\x0014u9*cZÇ\x00071\k´»Ö<û\x001aÕq>KZüØ!\x0017\x0010i»/e\x001aÄp­ÑîZ3¿ÓÁÝA¢\x0019R0ëNÐ\x0001`\x0013 h¸Ödw­«1m5¹ð\x0003Ór£,×ðÈ\x0004ìÇc¨áíÒÚq\x0008*\x0013ÝÙå\x0007²¼Fp³vS\x0012Íi·]@{BlÝgé[|ÝË¶\x001b\x0017µÜÀ\x0012rj¾ñv@éüwi»úmzKJx°%51Û\x0012\x0002ZÈÜÊK \x001dÕRåíº°	 ø Ue±¼­uëæíÇwo{{õõïïÞþòÛÛÓ`xÂÒö£ \x0017&¶"f¨Õ¾¶=Ú7·W7/¾ùâÙ«¯¿|ñÍ³\x0017ÇP,pï¼iåLÒ	O!\x001fó\x0015H|Ä"	*ø\x000f\öÕÒPT­°"±\x0011z\x0018Á\x0012FhZP¤l²RÖ?íy§À=hº\x001bëEâ¢Lò¥ÀÕâ
	îvZO#I=dº!ù-tA\x0012¢\x0004~äQË-BÜ|?<	Ié\x0014S$Dl¥TZéDT^¼Û½?\x000b¤Kì`kN°¼$á°'Ú\x001bSïtnò$\x001fËë\x000e#Rç8|yîÄúÏKQ\x00011\x0006%âf#ÂIPp¦PxÐ=5(N_¤V9F·\x001d\x0002eà\x00120%\x0013Hº59qÞti^\x0018·çd°Ã`j},ÒÀSxã[¡@^\x0012L¯J\x001e dS¯+eé\x000cF\x0016\x0013¯«z[R\x001aÜnó4Á\x0012©)&Ö³Éâ@zÁ_\x001cÈ oÕÜ\x001e³z\x0002\x0014\x001cl1ÚbnïÛ\x0001\x0003ÔAK\x0004kû¥);â`ÑÔ\x0012c\x0001éeq8nÿmçòi_d\x001aÊ`ÑÔ\x0012aõt¹\x0006#KIF=ZÛN1Ä&h\x001aÔU_Ë}o¿ ñê
'¿+g5dà\x00134å\x0013¾ïE¡$IEÔÑ­Pvõ«¦¡\x000cñ	\x0006(äÒjcV\x0005h}Ãîi(\x00037¢)7\x0012,õ\x000b¤/	õ9%¸Ùöt\x0012!HAÓ(\x0005KX¡dàÞ»f¼Ö»bk\x0007GSÇR¤A%¯\x0019Q\x0003Çé¥\x001fH\x001eMI\x001eyºÜ\x0014(\x0010(ND¾1eSKL\x0003É)Éc¢õÖKq	¹µ½=»]yïi(\x0003Í-Í§eí\x0002Å-Vy£Ò|Ù~,9\x0005Ê@ódJóXY±u RT×«\x0006,rW2ît2¦!M©¾\x0006íy½°f\x000c¿ï.Pâìé]\x0019¸L¹\x001eÉI\x001d=çTä
\x000eHªVÁ4¢§ëÉë±	Ô-)¤hÒ>
c{Îå)(\x0006'Sg1\x001fÉK +A\x0017½Ñ¾\x001cvÕ^§¡\x000c4O¶4ï\x0014Ç/UÓ\x0018V´1p<r<p×`m7/:\x001b\x0007óNAÐ)H\x0006'SåÕ¿ÿuÒ\x0013\x0014\x0014Ê¾\x0018á,\x0014?p¼7åx ßjë®x\x0014\x0017\x0012Se\x0002¦ùa?p¼7åxàA\x0017Ít±\7P]dí\x0003Í¶N¤\x001f8Þr<Ô\x0018¥ÉòW\x0007Þ ¥Û3)ÇíªÞS\x000c\x0014ïM)\x001eª·¥\x0012ð"_\x0010¯H¶«JO2>5R<°Fa£xJZÑÈ¢â­\x0014¿)æw\x0012â½)ÅWÇW\x0014ÖÑyIôêë¥±ô»ü@óÞæ]*ÜÎ¾ áZYAÚ9\â¦\x0004×IP\x0006÷¦4ï\x0012I\x000ft\x0002\x0012£°;O
Å2/á\x0007¦÷¦LïbTß«þk£~\x0018è¥O»£»f¡\x001f)?òàw¡úê\x0018«.Dâ¡Ü
Êî\x001cÆùº¡¢\x0008×¾_Ã§!îÖ÷:$å\x000bU»3hê\x0017Ç^B@Ü|þÅÒ\x001bS]Êû [TØ\x0007k¼å\x001eQz¸GÁl÷[\x0004al	Ä)RÃV\x001dM±ª\x000fp>$ÄD.úK|U¥øÙîDëÝ)º5(b#Õ åugLßógö \x001b£áNù\x0018s­O`y^%}^åì\x001cr\x001bjïârÔØÿ×\x001fº\x0001\x001bOßÿãÿý·û¯\x001e!½7à>E\x00198\x0016È;ÙÈZg\x0018"#\x0012ëO_ÝþðÏå°\x0007\x0010Ø@c\x0010\Ææ\x001b®­¨Äèöçþ>\x001a\x0002õ\x0010È\x0016\x0002 ²
È\x0002¡F/NÂcôº\x000fûS!\x001fÁ÷\x0018¼=\x0006'\x0018»Î$\x0018$\x000c\x0011
Lx$Ð\x0008¶ åÔr\x0003ÁOE-\x0005&íì\¶n³\x000f±\x0010÷@<ê>,J,Ë>HWÕ}Ø­x<ÔHÆû\x0007\x0010%V?¹ôVÇ]ëñ r\x000f"\x001bïDu\x001cXWnèS7Ë\x0007½Õq/)ñx\x0010¥\x0007QwÂë¼CçW1t­\x0017fÑÁ#Ã\x001e\x0007b©<ð3ÞêR5åÎ@I[XwZ
¬ßn8B1²µ1]S\x0012[Ä|-G±L!\x001d_ñH\x000c\x0003Y1[×ð\fÊ±©ÒJ\x0002ÐÃ´)ð8\x0007a :0f:òÒ2]!TC\x001e¬\x0011W\x000b[l\x0013\x000c4\x0001Æ<Á\x0002B((* \x0016e`\x0006±°Ém·ýL\x0018,,\x0018X\x0006!\x0013ð$(0¬(\x000c9z¤Õ¹'ÞÍ¥ù²ñò\x0010K1Ç\x0015^\x0011\x00175HrÙ¯\x0017\x000cÁPÿÏ\x001dÜÁú¿¿ú«±Ñ-2Ö³iVÈ\x0011\x000bR¸ÉV×ä¶\x0007\\x001aÊ\x000ePð0¿ÉÈòzöÊ\x0017 HÊäàIÏWÞ­;`òÏî3?`ÀÂS
\x000ce\x0010}VrÜsÙÀ3½xhÓ\x001f4ú~ñîãûûÿñÍÝßÏ¾ñ¨©ÒêÊeX½]\x001büâå÷¯*o\x001f\x0003{\x001ch\x0003Pj\x001d+¢úá)\x0005õ\x0011Ã®g2z\x001cd\x0005\x0002%\x0010¢ä
\x000e
aÉ
ïaxk\x00185\x0002lEÖ5fö'$\x0002Ü=Å\x0011z\x001cÁ\x001aGõÔ½\x0010"\x000f\x001fí\x0008Ò(\x0013BÙ­ÛÁ\x0011{\x001cÑ\x001aGX$ÿZ
eJVF%èvëjf`¤\x001eF²ú'KÉ&êÃ´ÜzÍ÷÷\x0019\x001c¹Ç­qÔ(JNó\x001a
fõTåÝdÛ\x000cÒÃ(æÛAR'À\x0003¥O\x0011sê VvÚ£À	\x001c]h\x001e\x000f-×<^\x0000©æ
ä~D
YjÞ\x0008ÈÈææt£:½è½tí×\x001dñbwÃþôí\x0019 \x00039WªUd\x001aÕ^'Ý\x0011©ýå9ãF\x0017\x0006>\x0007sB/ EÌËe%¯³Ó\x001dq»s g\x000c\x000eæ^Ëg\x0018\x0008÷-\x001cHfÚ§Ý9²3@\x0006J\x0007sNç¬zsyÙo­+\x0010ÍøúG# \x0003§5©smd\x001e Õ/@\x0008"q¬hc u0gõ"2a¼! ræ9²EÝ\x0010°¢ÕÁÖ\x0001@F¬VóDk	^u\x001e=hc u°æuàÉ7ÍøBt2õëK\x0015HØ­ÿ\x0000\x0003¯£5¯C
iÅø:\\x000b\x0019ÊmU_ØÊ_Ä×Ñ×\x0001|­;Âê[ò:\x000bêiy²ò´p C´¦C¢\x000fR\x001fÍ\x001b\x0010©ç´§\x0003 5@V9àhíHtë\x001d!ÚÁ0\x000bd°¾hm}¹\x0018Þ/\x0019\x0007Ïª)ÚLM"Æ\x0003äp\x000cÆ\x0017­/7D\x0014\x001cÀ¬µ#JOÅáü\x0013\x001c¬/Z[_òÀ½º\x000bV\x000b°d{A«\x0018Ñ]§ÁhµÑ¢ä$AZ]ª´¾\x0004\x0011b
¬bj\x0004d\x0008FÈ:\x00189ô×\x001d!\x0011ã'\x0016´\x0011 ¸ûf8\x0003dL.Z[_âæÐÔv$­\x001d\x0018ÕCýÂ±\x0019 C0BÖÁ\x0008%¡\x000f¬N,£bø\x001dZ\x0016äÝÖö\x0019 \x00035ðëa2Uöèã\x001a°CÞ­\x001a\x00012\x0004#d\x001dð\x001bËî£TT Ò
^\x001dI«¨\x0006>$k>ä2þòõ9øµ¸Ra¤ÝÖ\x0019\x0018\x0003\x001d5\x001dÖ¿%\x0019xÊzÕ+\x001f
\x000e´
\x000ei`C²fÃ\x001a\x001dÖu·í@¯î	q'W\x0003âÑ\x0005ñC,â­c\x0011ONýÄM#²!¤Õ\x000e°[ð>c`uoÍê>«ê$ÅHúªîhWr\x0006ÆÀéÞÓ}p"9ëSu¸D\x0001m­îsÉ[\x001d«Ò½5¥\x0007ç¤\x0017ÔÇ*½ãµªlÉ\x0015Øà\x0018\x001f\x000c­\x0019Ý§½bHÒrPôÅ°òå\x0007F÷Ö\x001e¿ëQÅM=Ê\x0008\x0005_ÒöI\x001c\x0003¡{kB÷¬M\x0002Dkê=ªöú·­â)?\x0010º·&ôà2'y\x0019H((=ìätG¶GÍ\x0002\x0019(Ý[SzX+ÃyàJÑ1C6 9QÈÀéÞÓ+×Iâ§;J\x0012¨îHBÙ\x0011Ø-\x0000\x0012\x0006N\x000fÖ\x001e\x0010EÝ±µ\x000c³8Ý\x0011tFÖ7\x000c¤\x001e¬I}9Zí²\x0007Z\x001e¬ÚÑ6Ö\x001a¿oN\x0007\x00052Ðz°¦u\x001e÷\x001aZòG£ª.s@Ý\x0011»£5ðz0çuXÝ¬z¤¢îTÕhÑÊ\x000fc\x00059\x001fÖóTÄj\x0005\x001dÒNÙCvd{HÁ\x000c¥îr¸ìÎÜ\x000f(ï;>E2\x0001¢(×½î\x0013=Ò\x0000ÿ|÷ËÝºªmçw(`l\x000e°\x00160Úáa\x0010
NexQþ¦¤½FnWovªô¯«+]ÿî¾Ôê¿µ¹³E4ßå¤½[ñ#o¶\x001dîh¾gä²¸<nM6ß×RYSwÆ«þFÐ-³»ßUaëíÿ«ñuñEªy`áQc-³ÊÃ3Få\x0002¼ô·ù½¦P4\x001d\x0001»MÑsW¦©	ôWFÕ\x0004¾À+CÙfºm&TÅ@vWñÖúg}\x0005Úb7ûPú\x0010\x000f\x0006{<\Å%/Øõ_ 3
T£®:	Vp }f¡=\x001cî»JT\x0016\x0016Ó"*¡Þ)#òDúl{è\x0002\x001dv}üuÈÒ:­ù0ÏolFiÏ\x\x0001ëÆº\x0008t\x0008ú%{¸ÆüFOÕS{`Ýª§fnÝ|ãNMº
ó\x0014Q±â¬ëÙ§­àâ\x000f\x001câÌ\x001ar¬Í£\x001f®¾ç}úýÃy@(z\x00149ý\x001a;g\x0019º\x000e\x0006\x0008õ2í·ü½¾úóüO\x001a `\x000f\x0005í¡Ôh&K­-d-FgEA­ìÜíqÃB=\x0016ºÀ¶xÎðµmñªóXoÖ}Ù\x0005æ°ø\x001e¿\x0000 oÃ$Tæ°Z°\x000e£á\x0019\x000b=`@\x0012L\x0001+¬öhÄóY´Sv°sXb%^\x0000ËÚ³a)gkX´ô+ì¾¸ÌAI=d\x000eey¡8tÍÉ¶P\x0008këÛïùÁ{,ù"ÛÂº-m\x0016\x0010K<åu[ì®Ké±\x0014s,¡\x0004mHá\x0001QÌ\x0018ÐÚ®uD\x0000f\x0002K×ÂLéì7¥ë¤K¨Údh¥\Y¨M[»\x0019À90#íÛó>ïª_p²FN\x0019`YwÆÌÁ@üp\x0001æEw[<\x000f>Yn¿Óö­»¢sX\x0006â\x000b0?\x0012×E«tUC¦af\x0004ÚïÈÁ2\x0010?\ù\x000b'e\x001b"% ¬ö¬ª\x0018p¤½|\x0006ÌÀüp\x0001ê/ËÔUå\x0018IhPÐÊ°Ê1v`\x0006ê\x000bp\x0007\x001d¢¤Ê\D~·£`dF¡%9ôþ\x001bòæÅh®\x0019¨^*F-A\x000c´\x000f<
©:ß\x001cO\x001e¢2ýaÊ>]}ýî·\x000fWßÞ½÷ñ1`8ÿîÿªgµÞ"³Øc\¼äúo½ß¿+o®¾~ùìõÕ·7¯^~|ýØ¯\x001fmÖ¯Ó\x0018ëúãu\x000e²~aÇìÃîÔÉõS¿~2YµU-JÉ5è\x0006G\x0017Òºþ¼\x001f=Î­_¯DwÖ+q\x001e¤³|óR\x0018ÖvAÓzÙÇÝ,òq\x0014¢¡	ë-Ð\x001fÖ1Ñ¿ß±æÝ§ÿÝVØ)8i\x0008\x0004\x001f½ªëâªÜ
¸?xñù
iÞ¼ùËc0`\x0001í08íâ\x0000`­Z]uÎa7}7\x0007z\x0008ôenï1ø/j\x001b*±·!ð<©\x0006á/ï>ÜÿËß®nÞþúûÝ/÷'àéÃMn\x0008(dÑÌ'ÊªÍìpWÏô//_ß~÷ç«\x0017Oß|óÏ3\x0003\x000eìq )\x000eñ>5\x0000L:i²\x000ec
áöÓ,\x000eêq%\x0018ªk¸´V\x000e×óÕ\x000e\x0015´ÛW:Ã÷8¼%\x000eÌ2À\x0000j°¤çÊ£V²?em\x0016Gèq\x0004K\x001cÕõhzÙ(LåsI0B©ÿ\x0001C\x001c±Ç\x0011-q\x0014\x0001è£Nò
N\x001eI  å±J=d\x0008#:/Ú6qäZ`àz=|¶Ä{\x001cÙr;BYU]¸ÖàÕ UpÐnyç,Òã(ûN×óP5-Î
B
ÃÐè\x001eF×/$è,aT\x0007=4*GLzËC!KP`÷Ím\x0016ÈÈæt\x001e©=WIK"C
É×knx?` s°äóÌJ§
HýöRåE\x0019\x0000©1%ÏÁÐc\x0004Ií\x0000\x001eÔ[CÉJ°+K0\x000bd t°dôBA§êß^4*\x0019HRD\x0004	À	a`t°¤ôäHmjzc\x0005Øpä²[2c`t0¤ôÊÝ^²¹®4ýò
uºZV\x0001ânü1c t°äôÄOí`±$4DuÝ!ïK~Ï\x0002\x0019¸\x0010,Épé-\x0013U}Ei_L.èÉ»Ñ'àÀ"hÉ"g\x000e\x0006$\x0000×>5ã[äªgï&lÖ?«\x001e\x000cÆ\x0017-o®\x001cØÕ*\x0014I\x001cÖ 0
ì\x000f\x001eÝÁd¡¥ÉÊYG¢cåÖV¿^v\x0013 ³@»w=ØÙNær\x0012;#ì&¢gq\x000cW\x001d-¯zá\x000eøÜl/?Ø¤f{	ÕöæÝ"ôI 4øYdèg\x0005VÙl\x001cÂw¥ÅS\x001eÔ\x0002\x0001WÓ\x001bâ\x0018n\x0008\x0019Þ¥\x0011°\x0001!'7Ä3\x000býÖñY Ã
!Ã\x001bòG\x0003\x0019®\x0008\x0019^\x0011V\x001d¦ëzÆ =6ûº~=Y¸;"u\x0012\x001fÈÐ\x001baàðCnH

\x001bð1ÔýØ\x001d>càBoÈu?K}Û~,ë¶!j²\x0002îNG\x00052f\x0016
\x0003\x0011VÚ2êÊ}»!è¥ë\x001a<·\x0002\x0019ºYý7qµô=Í\x0013¹ãºù(Xt\x000ez\x0006©.#}¥³pè38d\x000c'zif\x0004'J$9êÞ¤¼; c:Ú}\x0008¦F¼¦`
¡ð|ýçCÓÒ®1¯h\x0005×wWÐõ±p0àø:RÐ×oÞýüñþÓû«§÷ïÞÿzÿû©8\x0012HÏ/p&¸uú\x001a\x000cÉXD¤ýb¹O¾¿}óêêéíËWOo\x001fGâ{$Þ\x0014IDÍp¥TÆ;d22z0E\x0012z$Á\x001aIó#\x0017\x0005x\x0001"Z|<ßg÷9}\x0016HìDS dÆRu\x001cA´ik¨#«;l$õHí5q¬¬ïô(°SF{$Ù\x0010I¨ÿn-\x0001!è{×7D·?áq\x0016Géq\x0014S\x001cT8L\pDÒ$\x0017÷UìWÎL\x00029dæ\x0019fæÄ"}Ëõ\x0004i»¨¡N\x000f¯XL¡\x000cd\x0002l² 6ÕÊêþz©'ó :]üÌ°[O6\x000b\x0006(d
¥nE]á¡Î²+ÑéÇý\x0019³P\x0006b\x0004Kf\x000c¸«$»ª\x001dkmpu Å\x000cûe×³P\x0006f\x0004KjdE.¡Æ\x001aíÊÌ\x000cÎJhuß\x001f·4d \x0014°dÀÓ\x0012\x001cx\x001e\x001cr¾åö§¬ÍB\x0019,1b»´Ä¦BiH0$­°92Ór\x0012	\x000e¦\x0018MM1Ä(ã
øóKs¿Ç$"ôèpWs\x001aÊ`¿ÐÔ~ÕðP\x001d{"§çÓ\x0007ß²;íg\x001aÊpéÑôÒCñ×R\x0006®Z@\x0004\x0017j¤²_\x0002?\x000bd¸óhzçÛä±nO\x001b
àU6±:a·þ}\x0016ÉpåÑôÊs¨\y´"	Q\x001f¯i¿½rÖÄ>oA°ó_V\x001c|\x0018ë6_æù}÷ûÝÏ÷W¯Þ½ýp÷þSïIJk±J®ÞX¯¢\x000fñ%lñûîùÍÛ«W/_¼¾yõÍñÕc¿z4Z}\x0004\x0005©G
%/|(p¤Íyá«§~õdµz­å5uíÚâE{ýÞ-\x0017krñ¾_¼7Z|u\x0010×¢³(S}*Wøµ8\x0008·\x000cÓäêC¿ú`uìµ\x0002\x0010à¬Ç^\x001f\x0014ÛÔ\x0016\}ìW\x001f­¾=©áAÒ\x0005ÌÓziÝ¦dÍäêS¿údµzädH«óCÑ\x0001®ß^Óº;ee«Ïýê³ÕÉ	2zºÐÚêº\x0016´)é?¹úÒ¯¾X­\x001eDÝ\x00040¡{ó$\x000f­Üõg\x001e\x001cG\x000f;n¨uÜ¼ûôq ûõýûß?ýÛo÷ï?\x0006"\x001a@^\x0014¥eä\x001e¸&8S\x0003ï\x00107ýío¾_\x0006è~}ûêù\x001fÝ¾úç\x001dt\x0003\x0012êüÜ½Ýr\¹±%ü*õ\x0002ÿè«"U­f\x0007EêðGaÏ£Ô¢ÛPÇ\x0014ÙaÏÕ¼ÆÜÍåñ÷\x001aý&ó$\x001fr#\x0013\x0005T\x000b»jïÊê\x00189&Æªm\\x001b@f"¹æD® ¹Å'\x0018+\x001cNÐ
\x0015t\x0013\x0010¯ºÕ9@L
Ä°\x0002^DH\x0018é¶W\x0012ÐçÄÖH,+\x0012ësûX\x0018@2\x0012[!$®/4\x0007«8V$Fåæv@bi¤9ùDG»«/@;\x0007¯xV$Êå7À0\x0010*wWð\x0005I÷Ú0\x0007H¨\x0004N Æ\S\x000b4Ñ2\x0000ÁÉÓ\x0004$ö5ç 5ÈÄº<èh}È2ÙO®k3o\x0006M³~V\x001eb|Ås\x0002-6Cq¸&Qô«s´q50\x001aïsõ9\x000c\x001cÀ>âöR´½Böc\x000e&0JÖÈò)ñ\x0010[rWFºqd\x000ecØ_ÓyÉ& HÖòGCiü°duÄ\x0014\x0014·=ßé6ó×÷¿ýkqºN\x0006ÿsfÙF(º=)c<¾Ë¦kwNàµ£\Ì×«ËbþÉw#Ð5\x0002Í@ÇHY|ºz{äóW^âëNK?Vx\x0004ÁÔ\x0010\x000c#\x0004J¡Ê¤Bâe]á	Â¨\Ò$\x0008®àø ¸ß@,e0?%´\x0002n´ewù¡6?ðo->!\x0003iO~QÎ\x0011\x0000?Ê\x00115\x0005À&z»jÔ\x0003AÖþ\x0005b+|«H7rA\x0000âè\x0004Ñ$\x0000#lHÃ¤
B°Ôê¢\x001c	¥èt§\x001d{¥\x0004¡9Æñ\x001cÃ-)f\x000c^C\x0008`°\x000eT£$ý04çXò\x001ddÐô¸\x000eQ\x0013	|\x0011AQþI\x0018Ã,ùNsH\x001f?Ë\x0001¦
¤0#\x0007\x000e>Z\x0007×-ÇNÅ ó¬øÎs\x0000-r1hO*ØVcd
jýÊÎT\x000cmnÁw¤CºCäö5å\x00141'\x0017Vâ,¶Vbt¸f\x0012æL+¾3\x001d?Ðd\x000ci[åã`\x0002²\x0014h\x0018ÙâÐ\x001ciÅx¤\x0005+ =VÊÕ\x0010%Vzio\x0012æH+¾#í\x0003Ö=¢òõB\x0019ÒWÖÊötNÁ #­ù´we\x001d¼R8ç«¤#­øÜn´æ;ÒÞ]«×øÚ´÷èZ\x001fí¡9ÒïHÃÇ÷ÁjJ·µÕ´\x000e-JúÙ\x001d£\x001c½»slgÊÉN\x00179¬ÐZ"h×Ò\x0002í\x0003å£\x0018 ø\x0012$NáÀ_¿;{ÊwéõÃãË\¹ÿ\x0007$­ÄfÔ\x0014Ò\x001fs
-\x0007ìì\x0010JöÜìÙU¾Lß,Ï/o\x0013¤ôþ´\x0007A°¥Á³f\x0005#¯~X\x0016\x0011±ÉNÄþpì$0"Å×ö}	¨ÒÞ]þzþSÛç~úÛýâ\x001dì±ÙïdFÚòº\x0007:$²ª\x0001ö\x000cÚnK×òÃê2m³Ûëó³«³\x001fVw°ÕF_Ì\x0008ª\x0011)~D^P_}\x0006{U4Xö\x0000=ÜÞec>&]cÒüå\x0016W)]aóK2H·`\x0017¡í6¦ÏdjH\x001f\x0012JÜxòÇhd¤×ÉÖ,?¦ÌÜÂ\x0006#PxUOç
!.+Ü|H®äà\x001f\x0002
¦G\x000cq*ê©ß;\x001fS¨1#`RHN-£ØÙ|^Ùz¦3ÏÇ\x0014kL\x001d°\x001e\x0005C\x00154O£:.\x0007YåB·Eo6¦M½kMâ\x0008çÉøÜq\x001có{u>O\x0002û\x000e­ïçj\x0003.Ä\x0015@ô/ÿByºí\x0004¬Á\x0000;rï¢0\x001fS\x0013rå\x0011b.4QãB\x0017\x0011¢¢ãÔí$\x000f¨·?àÂØQnÝRp²²ð£
ôð Sì.B6\x0011W\x001e!än
úr\x001fIÂ&PO²±Û½2\x001fT\x0013r%Ì\x0015¹Ó:y=b×J×Ô@Ë\x0014»¼ó\x00115\x0011W\x001e!äT\x0012f\x0011QÜHðH¿£è\x0012æò
(Ï¿L:Î\x0010¬T:Dtõ\x001e_1ïóþÎ\x0007Õä\x0011ò\x0008DBÝJÿ\x0018ÓJ	òå²+r3\x001fTHÈ#d\x0012ZP5Nª¢Ûç-5ûÃ£\x00077(Õd\x0012?\x00001Â<\®Å&n\x0015¬ô\x0014uùÏj2	uLBÑP¿FQzä\x000fjxìGJµwþLBDª0\x001aG/þAÓ³ü×BÕd\x0013ê\x0008Ù4H\x0002	L>ø\x0002í5\x001d¨þxü|HM.¡øs	\x00116®/%HBã:Ñ¬¼sÝ®Ëù \B\x001d!\x0010z5¤W(Ä® ïÃrÝ\x0019´ù tBñ§\x0013Âc\x001eë<ô*~¯O7\x001fQK(ö\BG\x0018yÄe¡ô5¥hËÔ\x0017\x0006\x000fªÉ%\x0014.\x00017L=¡DJÎ-Ý8°Ü¯úýØó15©bO%tLQ)ÓÙ+\x0015%=Æ8£1Bþ\x0013ÆlPºI%ô\x0011R	 Fg®\x001d\x0012\x0006¤LVÒîÓ]úîù TB³§\x0012)S0ô\x000f²Ú:tÂ%
þ¢¹nr	}\\x0002¸ô2(@ÄôÜ[ªóyþDV·\x000f\x0001ì© =}vê±6âû¦ºÛ4\x001fTLè#$\x0013é\x001e\x000b²ÐrAo\x0001^\x0013;ïs\x0019Ï\x0007Õ$\x0013=Ð!r¤B \x0012\x001d&S:B¤dB\x001f!\x0010¹\x00114ÝwO°Øü9®R¿\x0011q> &Ðü¹DHùx¦ÑVÆ
M\x0006Â*KMÒ]öéù \B³ç\x0012)A²Ôç7ènãJIb\x001a
ý~Ëù dBó'\x0013Ao\x001a©\x0003\x0007+\x000by¥ðºfdÂ°'\x0013:\x0006¯ JiWÊbØ5\x0012õ.ùÐ|LM.aøs	\x000fcÏØe\x001aÊÃhYºLù_mLK\x0018ö\BGèÝÏµ\x0016µ£Bs0Ý÷ö\x0005=ìêáM
1ÁB\x0019ê\x000fó×ZL\x0013¡\x000c{Jw\x000eM'*í4v¥ý#Ä®Ö|PC7ü\x000e=¤kn\x000e¼\x001a¨à±ç9\x0010¦èº\x0004ð³1ÙÆõY~×\x0017Òå\x0010ßnlÊ&t¤\x0006â2YÒUU\x000fªq\x0013ßM\x0000ù¸ÇY\x0013h\x0003EßN\x001a
ü
U¶ñ\x0013ßO\x0004iéEÀ¦\x001c	ñÖñ
þjüå÷\x0013>Ú2Ï0)ch.Kjþ"müå÷\x0013>DºñÚX\x001a&Á	-m-s6(×8
Çï(|(gÊÁ\x001b®\x0014R\x0015ÀÄ\x0007?¦ÆO8~?á½\x0006ÉÜÜëA%;·\x0017LÐtÍ
ªñ\x0013ßOxçè\x001a\x000fjIDjá/aº¶ýí\x0008nÂ8RÎ;ê&MÁf\x0013\x0014ÿ¥W¨¿üýuýrÿÜg¿Ãß¸ß°£ÁÓ\x0005ê\x000cx©\x0012[Ûej8 B[7Îc\x0016~a/Ô\x0004\x0003úg
\x0016j]y&0ü+\x001d-\x001e\x0001\x000eÊPîä¨¶dRnK¹Sà¿7mhÆ\x001c\x0003Z´(ì`\x0008\x001ahr\x0016yúT\x0008ü/V-b>mGØÀ$êQhz3\x000e\x0007! cäã	¿\x0016rØ¬A\x001ae\x0005a\x0006kí±ÔÚ»r\x001c\x0007Üù·!±léÆUÆÓtØ/7Ê>3é\x0001o¨yi\x0016Í÷ÂÐ4-\x0019àÂÐæ,UÝ\x0013.þÖnõßÅµc\x0004µ\x0007SP\x0013¾tx\x0013]f:iÝ\x0001Û\x0003\x0000¿ÛÇ8i:Ø¡'0×A%+%D®Æ²×ÛÆæâ V\x001aó\x0005ÌXá0\x0012u\x0012kvdé }Ü:h\x001fùk"H¥fÊýÙQMñ§ú	Õß·Pý¿Ð6¸ù\=LÑ\x000cÝ¢¥Ñ±à\x001c{êp­·p­ùÝ½$\x0001Ù¿rU¸çÃ1Ê×aÛ-&ßÁï\x00175¤\x001dÚà¤Cb#èûÆ½\x0018-gÑ\x0003i]6ï
ÐAô·{M&?\x000c¨çø
­4¨\x0010g\x0000\x0001+ hi%µnëwfø¼ýá.ý~¾ºÞ sA^\x0017&\x0008z({\x000e\x0010@º!kIk	îÒqLÐ.\x0002ß*ÈréË§lÝá*P\x001b ÜE<\x0001j (¾$¥×8\x001aON\x00104É²(ÓË\x0015&CÐ
\x0004Í\x0007a#á4ª{%\x0008Ô	,U7C\x000cÁ4\x0010\x000cçqÆ	"\x0003T
Û§Yu;@&#°
\x0002Ë L×\x0018G}a\x001aôK\x0008B`[\x0004×@p|\x0010\x001còÒ$\x0008\x00019ò\x0013\x0004jý0ö9\x001fòþ/ÂK]¢\x0002ýð\x001dê|º_\?üü80&Ä\x001dæ§ÿîwï×ðgr_ã²ÚhpÚ¡¸°\x001eËÞÁÆnJ<è\x0013¬\x0016×ço/¿ÎÐ\x0018­j£ÕF\x001b¡NÎV{lLÂ\x0019ì§IPÆµ;ö¶ÚÔVC­Ö\x0012{:\x0003é'­\x000e8¬îºËiV»Új÷ÿ°ÕÃAjÊ1ýPíÏëÅÙÃËýâìéõÓóÓËâÝÃO[¿¾Ì-¶¤$\x0003/"\x0006
HT(2;&4\x0017ËÅÙùíjqvu÷æúêvñîüìåÝín|ºÆ§\x000fùÂ\x0001G?¤¼q\x0005ß¨èî!øLÏ\x001c
ÁÝ(Ó5
Õ\x0013>J9\x001b%m:\x0004­ñÙcá\x00112#¢TÌ¼¥¬P\x0010¾\x001fÏÕøÜÑÖoèÉ^Þ=hZg|}>Cñù\x001a?Úú¡6Vø\x001dklÂ6®\x001dy\x0000¶Pc\x000bGÃ&QF*Mé	'\x00113ÝÍÒ\x000e\x0017kxñhð<éej\x0017á\x0019§7Þ\zý0|[²T\x001böÓ#\x00004tiÖ&\x0012ÿ£·ev»\x000eÅ'\x001b|òhø">8\x000f*{VÓ«¥£
:J÷z\x0008À&wGK^Ò\x000e5x\x0002ÓZÚ2_L'Pö54\x000e\x0004Ø$/òhÙQD@²Jè\x001aÍ+X²\x0017Ùý9\x0014`½È£¥/FPz6c\x0019× ¾QÐC9Ö
6é<Zþb,]åáJ\x000fµÞüEìº-Ì\x0006Øä/òh	ÑD1¡-¯µÎØb\x0018\x0017[<\x0000`ÀÈ£e0)4 Å\x0016¨N<µ,&G;M\x0016#Æ\x0018GW¡w[Ò\x0014"\x0001t£©\x0000lò\x0018y´DÆª"?\x0016m¡vñwGÊ±UÈ¨£%2izTEôº\x000céx[\x0004OåEUÉ¨£e2Ö\x0016AWhÆ3\x00184I°õ9\x000e\x0005ØVaÉØb­
å\x001a\x000f,¹\x0019 ÑGò¢ªÉdÔÑ2J­/T0T5K[ôHw	Õ$2êh\x000cô\x001b \x00135{|(°ýWC\x00016:Z"®¸\x0012w¨¶%\x000cÆ"ª|´\x0013Øä1êhyEe\x0012°lö§'iVÑ\x001dÞ<\x0014_Æ¨£¥1ù!)\x0003Ô°Wóúm\x0000²\x001f\x0002°IcÔÑÒ\x0018h¶\x0018ð
L\x001eXè%\x0006þtQêR\x0018\x001d¯ÉbÔÑ²\x0018[	¦éb\x001f±O7á;\x0007ÕM\x0012£Äè\x00185yP ¿E2KW6hè³YÎ\x0005hÜ\x00161vú\x001e\x0010¼_?.~LFÿöß_f®\x0018\x0014t1æy©QQCïY¾ûix
í#úqµ¼\ü~[è~\x0011\x0004UCPl\x0010@Ð\x0013U\x0010Yj\x001d"L¿ãl2\x0004]CÐl\x0010(
^I,\x0012iP\x001aÁU\x0018½NB`j\x0004\x000fr\x0014z½²ØÇ®\x0015Å&¥]÷-}2\x0004[C°\x0010"2ÕJ¯
A´DI¤Ý¨äÑ$\x0008¾àù ¤´Ná*\x0018jÕ0\x001f\x0010ü¨\x0003\x0004!Ô\x0010\x0002\x001f\x0004gqEz ãÎÍ=\x001aS8¥#ß>5È¸\x0008\x0001éïÒ"DL³5\x0008X \x0011Õä\x00106\x0010CT\x0010|\x0018B¤ ®ë|\x0016´'J
Ó§ú¡	\x000b1.h}"s¶¾øÌ;Éh\x001a2¦Û_½á§õ§õç>&.HÆÀà
Hï
¦üZ[¢\x0014ç\x0005®uh"ä\x000b
\x0016?\x0002´\x0001äà\x000cg\x0016í,¸Æ~Çh)\x000b\x0004=p}\x000c\x0010(C2ý¹É\x0010\x001a*ùªE5
 !ÈOÚ8\x001a|1n´¼?	@ãR%Oµ0«*'&½5ÔÜ\x0010f;\x0007ªñ©Ï§Z\x001fa;¯\x00031
§üÚuc%ÞI\x0018Ûâ».Xåé%%(¢ÖF\x0011§ºcÁ¡ñ©Ï§î|f4ÁÑ´TÂPb[ðlëÐ¤ª/Wµ: 'è!\x000e%·*7\x0018ØÎC«*¾d5ùMÔ_!hÊôRþGSk-OR_R~	\x0013ð<Ä³NÚ"(%G%F§`ÐÍÖgú»?·"r\x0018äHD\x0003
Ð)ê\x0012êr\x0001X[ØÃ\x0014ê¸ª\x0019JnCIn\x0013¶èf=2É¦Ôê\x0001)\x001erÝã¤ØÌá%bÍw(QÛ{Í=Z;CËÑ¥g~øÝÆR¼«¡H7.Ò;Ü%\¹K°Uh~\x0007\x0017É\x001fxÚÅfØ\x0014·ÖG¶­\x0015]¹d\x0007Oõ&î\x0018tAµ\A\üî¤³\x001etNFÄÂÁ¹®¢R8;x=°m\x00016ý@\x0005Ø7ëÇ^3ÍOÿ­Â \x00055¯\x0007K\x0019!EÄo¯îÒ»­×µõÉzåIøH\x001aO\x0014ø!
K¤)]ÖÚzÃd½¤\x0019,<$Jf\x001cµKFe\x0013¬·µõÉú(
³x\x000cE>ÐÓ}È÷	&Zïjë\x001dõðþß^Óð\x0002¨\x0015d²<ÖûÚzÏc½\x0002Ò\x0012¹\x0016ûÂõpGÊ\5Ú³¿õ¡¶>0}{+P\x001f4ÚH\x0003\x0017À¦]¨F¥ö·>ÖÖG¦o¯<\x00115)-èþ)
±tè3¼M³~S\x001dVÃ\x0001æúø4­vNæT ühEoõM´\áÊZ¢\x0013\x0001ëQ\x0019©÷yÓeh}ãï%Ãw
·d}Ä×ÚôíéÍ[¦c+\x001b)¹|¦EÉÄRE\x001eÌWÅüÑ\x0006Ýæ\x0007¿-#íåfÜöËâÃúññ~v¦Ìµxë==§û\x0000\x0016¸ôñÿfñayy9¨ùª6_q¯\x001dêgI\x001bD±ßQ)>9£ñYýí×µýË~K¢fé\x0010+l°Ô²ÔO\x0018Mù§Øojû
Ûö)cÖ:¼ô¤-\x0016`¼;fûmm¿å²ßYÔ\x000eH³Ø¯\x0004½E
+Ác¿«íwlß\x001f\x000foòB\x000e7'Ï8®Ãëkã=ñ \x0001\x001f_9;\x0018>¾¦\x001cÏ'\x001fjó\x0003ÛÙUDu\x0005Ê\x0006Ù"¨µ\x0016æ¼Æÿ÷·?ÖöG¶Ï¯¯cøü\x0016Û¤gþü\x0015ùß¼è3|yptÑóDâqÇ\x0000öþæ·-òx¢ñëË\x0013{ª¡ð4Îd~\x0013x%[äu\x0002\x0005J¤Í\x0003ÆéãSÒËú&ìJ¶¸\x001b7qW\x001aj*R&\x0018¥\¿»-ðzA¯\x0002pxªFIáÊáåÚþMà\×\x0008"\x000féæë©®l ¢\x001ag27ÙD^É\x0016zSôÂé&+-¥nJQ3m!¦ÔA6áK²Å/P·Â-$%UÍ¡%V+\x0000¨&\x0000(¶\x0000\x000e1\x00050`Å³ÛØuùã¦\x0002hBâ
\x0001)}+¤_>¢L¸V%û\x0007j\x0011&\x0000íí+\x0008@l&#L\x0000,\x0005±@oar¼ÇwýM\x0018P\a\x0000ôÂ°}ÅXKô}¶F)¹¢°jÂâ
\x0003¦Hå\x0000U\x001c\x0016®´\x0016Ô\x0007%%W\x0018PM\x0018PlaÀúÂ°h|óRâàJãT\x0013\x0006\x0014W\x00180V\x0016úÄt%uÆ\x0012g£\x001dÖS\x000040Åu\x000b3^ÃÔNfjTBÑr9Ñ×±
 c+\x0019\x001b/ÅÈPz©%V\x0004®#ÜÜÂ\x0014×5\x000c¨O\x00032\x0015À\x0011\x001ea[ú"\x0013\x0001è&\x000ck®0\x000cT¨¢Ì	Ú_?\x0007ò7\x001eû(¬Ù¢ð&\x000fÉ!ìÕ(\x0013áÂºÂ-
ûâCu0TÐD_~*&i¶(\x0016	0\x001eaCµ.l+F0¹PÝê
äE ¾\x0007\x000b\x0012:­GGjé
L\x0000¹\x0018Ór\x001b4|0`	\x0004]-i&^'?J{.*Ýï`8F\x0018A\x0017\x0018Ò(ªnëÙ\x000e·	Ñ6\x001dñm*'`&3ç\x0017
y^RtDd\x0013Ç_V§¤¨¿ÃÁ¸«¡1ac56F¤Dµ\\x0015ä\x000e~×ý¥²\x0003\x0018^Ê>rÕ\x001býæ­&RÅBFMoer\x0007­×·í`ÜPÚËòd\x0006M\x001ex¼¥¤Êc\x001c°´\x0012ëv%Ö|wZä¬\x001c\x0015Þ==:qÝûe«uë§ð\x000bÓãe	{)Å w	ù^^¾XÆ¾8ìö¤µÝLZ¿KF>Í\x0013\x0003\x0007^\x0005º5¤T°´øu%\x0016Àöwé·«	q»=^m7ãÕÙí4\x0000'»\x0015
\x0001¦Ë\x000eÍbV,ö5[×fk\x000e³áq\x0015ÍÖ\x0016»´	eÔ\x0006å}í6µÝÅîÂRæµ ùc\x0013Ê\x0004õ(Ëñ¾fÛÚlËbvy\x001eð qfGciæx´8½¯Ý®¶ÛqØ\x001d,]e¼&½<\x0015 qo?ê\x0019÷µÛ×v{\x0016»S
ÃÐ²J3\x000e¦Ìx\x0007ï\x001dj»\x0003Ýq&»³\x0000rNÔ>ìæp'±¶;²Ø­éñÎ[Ò
K\x0017Fjô\x001czÎ\x000f¶{óîk«Iî\x000cwÂ6@6\!Û¶ef!%ýcw¬}
oÃ%G¼tBÝÈ0,tÇ Ýc5}Ín¢¥ä\x0008NG.oË3£5ï=J¯µ¯áM¼\x001c\x0001ÓIA\x000c®~#	cKMAÇÑd}_Ã)9"¦\x0003a\x0000táÆ´µÔªÇ\x001e\x0015÷5»	#b:%ÊÁt¡2<adÙ(MÄ\x001c!\x0013´iè&å´ÃS$%ÃGë\x0004û\x001aÞLÉ\x00113Ô~ä;Çñ-ëT¡³\x0018eyß×ð&fJ éàÕ3­BAÓX¶
CR( )9¢¦×B"\x0010ñT¦´Q\x0010ï\x001cÄÜÓpÕDMÅ\x00125Ao\x0012o\x000f> ¸N2.=@RÇ`x\x00135\x0015KÔt¨¶xM\x0003v;¨³à\_WþyÝí%%l¦ci§\x0018r*N\x0014~Ñî¢}ín¢¦bA\x00123H\x0001TæÓìÖ\x001c÷\x001eÕDMÅ\x00125Ó=|¡¢'ÀÊ\x0015r¤áª%jÆRE	ª0Õ9ëÊ\x0008nWsáMÔT,Q3l83ò¡vR\x0014£F\x001f:öµº	#dB	\x0002¯ÇAG$¤¾2J?:[¸§áºqàÃ\x0003¡£sI$Ú±BcFß÷5¼qÃ\x0011útÀ\x0016u1Ç\x001e3ç\x00039\x0014¸I\x001cnxãP4Cë¼Ü|q¼!2aúà\x000cY¡n\x000e¦æ8ÞÇR(\x0004¾³¼SRfK¤Bãä\x001d{ïú\x0002w\x000b½P\x001c¸a\x0002	SGÄAB·Ù/]ÕïIsÛüäyYÌOI,^ótå\x001aM\x000ecÓß}{Ãôí½¢N\x0014\x001f-5E{[²\x0016%\x0018.êw{G1í\x001dÈ\x0016õ&=ÛÙ¢\x001c^Þ»ø¹m¾ç±Þ\x0002_\x0010ÒâÒnE¹Aûta¶¤Ó\x000fhçéÓëóÏO??ÞÏ´^©al\x0016Æ AÚPÓ\x00000
95>ºZ^Ý]¿½z{¹ÚAÕ\x0018\x0014\x001f\x0006ih6eê'6à\x00009uÂ9»£\x001bt
\x0006Sc0l\x0018dôH7\x000e\x0012øº«b Jº\x000bã#ü0¸\x001acÄ ÀB¤l>ßBTô¦¹÷\x00130\x001aCàÃ|0H!âN\x0010¡\x001b\x001f÷E lÊìÃ\x0016|\x0018´?ÁÉf­ òl\x00108"Ã2è°åt\x0000·tö·û_\x001e\x001e7vññþù~ýúy@¬Iyæ\x0014IÆG\x001c\x0014HF\x000e÷\x0011¡ù³\x001fVïÎ/·v@sºº^-ïþ´\x001bªñ¨o\x001f®ñèo\x001f©ñ\x0018n<Ò`G¬.4x\x0004>\x000bJÙgÇÖxì·»>QÚÖ\x001fÀ@gí\x000f@ýàýý\x000bè\x001f|¸|éÛô <	ÙVÆcN¾mú_\x0014Ý®å\x0002	\x000fÞ¯nAúàÃêòvÄË\x0011*U£Rÿ.¨tJÿ{ 
±ÙðW~\Þdù°`l¤N<(\x0018\x000fÕ?i£u½²å\\rk\x000f\x000eç\x0007\x0016M~ÃLÀÊc T\x0015\x0002S±W \x0006Ì$L\x001f¥Ã½\x0018êðÃiúá;`>x÷ôú\x0019`½.~@y]óé¿þÝæç/éÿ\x000f
~à\x0003µ 9Bk=M\x0000ïnÎèl]N¸wWw\x0017énÑEi\x0006H`\x0006¢¬BU´½¨Â¤k6nj:\x0015\x0008]ëU_xñ\x0004d°±À\x0000ùw\x0012\x001a\x001fp]T×9ì\x0001'_òãVL\x0002ýl¼:¿¸~N©öóÓ/Oï_æ´\x0000\x0006¹×$<×\x0019sd`â(ÇûóÕõuÊ¸¯¯nn®.V·cð¨\x001aâÆ£\x001c5`ÀK5w\x0007\x001a.V~´a\x000e\x001c]ÃÑÜp@	\x0011á8¤\x001aäl°:ÓAsñ\x001aáÆS¨þ¤Ón38Z\x0018» ÎÁck<\x001bO(ÍÎ{\x001aBs4\x0004¨¥\x001b{\x0003ÇÕp\x001c»7°Ôâ$²d-ËPÑØ9x|Ç3ã\x0001^Ôkp@x\x0002tg\x0018«ëÏÁ\x0013j<Ý\x001d8j#w	\x0000NÜ)ÙLù
7XÃÜË#ax?¯N8A:\x0017#<\x001e=ª0\x0003NÕ\x001a\x001a74ËãO´ÆåÈK\x0000Ñyud\x001apç\x0006)g+*^ÂRð1éâë3ÞO2\x0007P\x001bHöäÀ9jrt àî t\x0010¨Q¾9xä@rg\x0007VËÒ'Jc}\x000b4J :\x0007P\x001dHöôÀ{âw®Òh¢Æap\x0017P\x001eHîüÀêB7ä¥a4
çj3ª3;\x0007P Hö\x000c!]{ÈÅyAôCÚ\x0013\x0001Tº90g\x0008²É\x0010${`L\x0019\x0015þÄ¡\x000c):vt&a\x000e &Eì9BÔBâ¼¡fat\x0008Wû
¤¨ªØ£j°tD\x0018¨\x001d½jÁí¶U{Eå\x000eC\x0016Ôa3\x001eègC \x000c½¸«Ñ^9x\x001a¯­¸½¶U´¦]4p_\x001d\x0000ÉÒY­G)Éæ\x0000jâvr\x0016\x001e\x001e0¬
º¤\x001aEÝ@pñ4.Aq»\x0004nÝ4"ì&
\x0013\x0004u.V@ºq	Û%X£²iJ|HwÌ\x0014_3*Î:\x0007Pã\x00124»K°¢Ì5KST¬¡°jF\x001f½gå	MCQÎ\x0015¨£ÑwëMýÊ\x0014´¦ïæ¾·$%¥\x001e\x0001\x0000¡ËÒ±¶±$ª£J\x0013p}\x0014N7eàS &K»ûâþËâíóú1ó\x0001$£ç\x0012\x0002(H7fx7Ñ2à=OÄ|+6ý±ç\x001d.V7·×ËËÌ	þÙ\x0008)@\x0001¢j \x0017É©O\x0002¢V;\x0001qDvÇ4g!Ñ5\x0012Í½$V%D5éí¯YHlÄ²#\x0005ING\x0001*HzÙÛ\x000c$±E\x0002åÄî¤&?0¦l\x0000_NÓJdÆ+\x0002è\x000e|ÌÂâZ,\x0015ÕôXò\x0000ÌªE4\x0016±xÛ}Å·X<+\x0016có\x001cÂbH\x000cCDmé´èîhß<,`¦ Y3ÃÁ\x0007z
ò<àxÓ\x001dÛçÆª®\x000c~87Sæ÷ÞãÜt\x0000·^LÃÐl¼üõþ\x0011¢ÿúËËýëóÌ\x000f\x0002ôH`$ãfÄAº\
!tmË\x000f«KúËÛÕÝõnûUm¿â²ß\x000b©WZ\x0002¹×`¿A*,~î9â©öëÚ~Íd\x0010Þ¦@þ\x0003SI_÷ì>NµßÔö\x001b¶ïoè¬\x000cµHkoQgXÆniªù¶6ßr}þ¾\x001bSÓã%\x0014Æ_×}¸Ý2ÿ§õ§dÈsß|Wï¸¾~,¤W*¦Ô0ïGÂ¯ïºwú©ß×ö{®Ïï©\x0017RZYJý!è
í{/µj¨í\x000f\öëPø%µóô+ºî\x0005wªý±¶?rÙ\x000fuo¤¯søcy«Tý|¢ýÕ\x001beÈ}õ<\x0000¬ÚPvk\x0014YÔ¡\x0010NHÑåÄ
 
¿\ñ7¥\x000b0;{$
·G]:ú¤^S\x00014ñWr\x0005ààOÓ\x0007*Á\x0005_Toú#îS­o¢¯ä
¿\x0011m,vîhªxDMûGù.ÛïT\x0000Mø\ñ7¤Ïª\x0007 ;T1!\x0012]ÅÿÈ&\x0000K¶\x0008\x000c5'z7\x0008Ä\x0003\x0012b¡Ql\x0000\x0010,¹bpJÜh\x000e\x001eßE~'º¥Tì¾LM\x0005ÐÄ0É\x0016Ää\x0001\x0017ÀÑÛgI@µêVÑ'¯\x0010 ØB@D$\x0003ý6Øþ\x0010 n(Ý\x001dp6EØ!
\x001fR	K0ÒÄÚ\x00174Í\x000b\x000b¾¯yXs:\x0007?0­"e.ü¨V\x001ebéV]§/Æ\x0016
Ë\x0002Q\x000eM\x0014\x001dà=¥\x0015ÖsåEfC°á#_Ø2@z8Ñ\x00165I×eâa½aÍ\x001dI³27)JFe\x000bK´çÊ/ÜöÙÆ#¦µ\x0008D\x0006à´/kAc\x0002 \x000cËu,ôö±ÐÇB\x0015>\x000cP\x001cS¹)\x0010¡pÝ¢÷t\x0014[«¡\x0019=­´ÄG\x000bôÝ\x0012ïü>îÒÿN!·\x0017Cò-\x0006 §U¡
oQn)9Z.\x001f%âöjDÆÕöÄlDN
ØìÜ\x001d°\x001aé`Áü/\x0005Tú\x0001
¨ï?¯º_­\x0001C\x00177\x000fÏOßí1>\x0003*Îï×ðgo¡@£é\x0011$àB~Ò¸=\x001fáE¢cþûåÙjq¶\x0004²Õâæüúêrd)ß*\x0002;_1N\Þ?ßùÛýÃ/s\x001dTtÄ8	ôÁYQÀ\x0008K/ÚJï ã_\®®W7?¬ÎßíÆ j\x000c\x000bÐÕ
vÞáÐÑ\x0014ùdÁA×\x00184\x001bôq\x000cn\x0018ÈÕup¤>"Å\x000eª	\x0018LÁ|ë`k\x000co\x001dtJ<H
Tÿ$&\x001e;¤Ð§`ð5\x0006Ï¸\x000e®È§QÞJJ©\x00173ÊÏ6
B¨!\x0004>\x0008nÿ¥à\x0005\x0006Lò©TQ\x000fC¬1D>\x000c)Ý ÎUaÅ(©éHÑÆÈý0(½õF¨t&$zz}¹ÇYäÓ{\x0008s«ÿzËa\x0002O´ú4¸\x0008ª!yÚ5ÆÜ\x0012D\x001fÈÕÝí
çOW\x0010îVïÏÇL\x0008ªñ(v<Fç+RÂ£#P¥e<Y\x000e(\x00012\x001d®\x0011inD\x0011z<qR(ÉõL«P½,!\x0012ýÎü¹LÈ°#RèÅ\x000bQâ¨¸M&Ïõ§¼«/Ö1\x0017­\x0011YvD Ù\x0014ó\x001a)ê\x001d²*]®ptúu."W#rÇ@4<Â'DRa'\x0004 B@#ó¢s\x0001ù\x001ag\x0006äÒoå\x0018 f\x0006¤#ÇÐo#(Ô\x00027"Ö%fW\x0017Â©Dë´°xl?Á(Ö"û\x001aà\x0013nº ¯\x0011òpóf_#ÙWîø
ÖØ" ¡¼bÌUG@Ômÿ\x000b¨F;\x001c¥]\x0017sþ\x0006»\x001ewÒ®´éú·¹\x001aß-¹·ÓJóvéÎõM-\x0016¥\x000f²/o:;\x0007ª«/9\x000f\x001a:¿yS!ãHàÂ\x001d^<mJ4î=Õv
LlÓRLKë1þïÿúßËÏ_Ò\x001fgÖ2\x0008 Q2Pí\x0001ùAæIõý;dÞ,\x00177é\x000f»\x0011è\x001afC C<±® P\x000e9\x001b©\x001aÃÀÖ\x0008,ã\x001ak \x001d> ¨\x0018è\x0019\x0008\x0014\x0006\x0010ø\x001aç[\x0003PuÊ¼RElíIk\x0010\x000bacM~*X#k@\x0003lJ\x001a­*FÒ¥ò]\x000e\x0000d{ùN²\x000c\x0018\x000f3ifÖ³WÑîWÝ\x0010¿7\x0004¥·|ÒTW]>~zþí_û_î?¯\x001f?Í-­zK\x001d>P1XÒ#®«E|äþ¿¼|s\ëêÝê"ýq7\x0010U\x0003Q@¬ÈUÔ+k1RÛBB¤Æj1Sqè\x001af]¨ËÃ(°Ñç0t²\x001d(
ÄÔ@Ì·» ¶ÆaYqÁ"áØÅjWD`áGé\x0004¦\x0002q5\x0010÷í.¯qxV\x001cY]ZrS½\x00111nZ\x0018qÄ\x001aGä]\x000fML<Vdeã´\x001c¤\x0008¬\x0002ç¶m\x0004á\x000c!Vx	\x0014\x000ey_É|/\x0004íÒ¤(Ææ§\x0002i<¯ät½V\x0004CÒ¤N*\x0002âI\x0011IY56R?\x0015Hã±$¯ËY\x0019z/uØø
9#qV©îìÏ\x0014$În)7§\x001f(¨_ß?&\x001cïáæ÷üð83\x0016º¨NH]`n¢1äyÅèSÝõêrµx\x000fW¾ëó·kB¡k\x0014\x0013\x0005Râb($¨r0Üo×|\x0010L
ÁpBH©n \x0007ÇtÍ\x0018\x0014«£ä\x000c\x0013QØ\x001aåDa|®ä\\x0017¹µl(ûÉ²´Láj\x0018u?yêsWx¶Jÿc´£\x0004ãjø\x001aç¡}\x0019çO)\x0016Ò/X_\x001e±m¿ 8\x001dF¨a\x0004ÖÕ\x0010¤¯l£(R4¢ôD\x0013L\x0011k\x0018u5
\x0019Ø=¬#Þ9å\x0018}ífÜ\x0006`\x0010% \x000f\x000e[P4±hc!;5£â4\x0013qÈ\x0006äÄ!#Í9åhr\x0011tíJ,¯M\x0004¬!\;:\x001e 0\x001di_dÝf\x0013q41\²\x0006q!6s\x0014\x0012£øFý]ÅQq»08.Y\x0003¹²Ð\x0005·ßh7[UuÆãÑDrÉ\x0019ÊmDF4CÄ!
\ú?É£	å5§{\x0006\x001d\x000f#Õê2â\x0018º\x0013^3p4±\r\x0006sè"\x001c¾ðÅHûª_P\x0001£å5\x000bt¹ÆSÿ¸Õ%¯
ý'Ûé H.9C¹õÆ~af
¥MpD
×\x001bC5¡\±r\x0018¯À3nÍÇõP¥ð\x0016G©'âh/±!ÐF]øÊ=Á\x0008(I_4eë|gC5\x0011PqF@\x0018¡EfbQð~Ç'âh\®ât¹P\x0011qÄÕi«\x0013zjÉUñåëªqUÓU2	^fa0\x0012ÃDºëqÁôi8tsÊ5ç)·)|{"¼Ö%rx_,GkU\x0013q4§\³rYf\x0014õ\x0005É\x0016¤ë¬\x0011·rÝd3C4ÐÂÙi=î>X)×	¢nN¹æ<åÆ\x0017Ur^RU(ä\x000fGsÌ5ç1O\x0017¨\x000cB\x0007âÑÈícL«LsÆ
ç\x00197ÉZÌÖCä¹\x0003\x0013\x0018jélxÆDªÍ¼'^g×5ÄÐ}V\x0010#\x00150·QÕjrj)´n®ÊåP¢ÕäA\x0003\x0001\x0010'!5A\x0011ë¢6 äè\x0004ÃÔ ²&\x0005\x0012V8ÀÍ»V`¢UXO\x0003ç\x0015DnCI_weD(\x0017*\x001d÷Àêü\x0006É·ÏZw\x000c¼+óFG÷;8\x0017qñür¡ÅÑÔÇ­e¨Ímb=õpðçìoëÙ¾\x0019\x00004\x000cÈ`yÑDôá*]{\x001dQ\x0008Þuß¬\x0016g?,Oá¯;í×µýË~)iJÚDKºÑå.\x0002TLæÚ|Ãe~ôTm· Q[Ç¼(\x000c\x000e~ìõÞö»Ú~Çe¿q$)\x0006rO¹\x0005C¹BL\x00045k®ï_å¼\x0006t\x000f\x00116MºÿáK\x001ahÓ6r£OP;`¡ÿPnN1ýPâÏëÅÙÓëóbýúÅû×À+
`æ$\x001a)LËZ?
=\x0012Ã
j\x0018ùÅrqvuw½XÞýiñþî\x000cÜÔ\x001eðl
Ï\x001e\x0015^ÔØeáA\x0001åÅÒ$ÎéFÛ¦ Ì[.EÖ
Ã­¥4î¿.N\x001e¾,~|úü0s\x0013¦KI>K!hPP\x001dBcØ´\x001fµé\x0012\x001ccoûÝâôêüfñãÕÅùn\x001cªÆ¡8qØ¢oÀa=¾ ÂLB\x001cýÇõ\x00190t
C³0l
Ã~s0Ò¥¡=\x001céâÝ^\x0017(þúÛÿYÜ®g¦Z\x001aæÁ°OÜ¤¼ÆHO7Øel\x001aNûÝ\x0002_Ûå(Å¶Nª+:©l@\x0002²¡*.óÞ!\x0010TlÑãÍL\x001aaEâ½ÄäQi¨B\x000e@4x\x0005VÆ©H\Äñ"ÑÖ\x0004X¿u\x001e£Ð0£êïÎ\x0012j(\x0015\x0012\x001f¨S(ôP©\x001f \x00088®ú1\x0019J¬¡DÞâ\x000c*ÒAG\x0016öi)kD('e4-|è\x001b\x0002¡áà\x0014	\x0012HÎ?\x000eG&[\x000cgqô6\x000föM²r±þõéa&\x0019\x0012HÈà¼d\x00006Ø\\x001aú\x0010S¬ï! r±üpu>Fê¤·Yx´oÒÃ\x0010@(t\x0003\x0002x\x0006
E­^#\x0002ÓR@×\x00084ç\x001aä!Ü\x0000}Zyö[¦ýE\x0008|^g*\x0002S#0|\x00084\x00143ðÒÖÀ!\x0002 cäB`k\x0004\x000fËzi\x0017ö\x001a.ÂÔÊÚþ
d*\x0000W\x0003p|\x0000Ä99\x000c\x0011ÆQó\x0012PnèÂQîý\x0001ø\x001aç\x0003\x0010r\x000blZ\x0001ãÑ¦%ÀÑíhGä	§"5È\x0000<CF IY!!pÀxÇu
d\x001b
øÂÏÌ¼é\x001ck¤l	AÀ{«\x0019Ñ ñ¥Ï\x0002\x0002®(Ð\x001ad}t\x000eb¿X2\x0015Aã$£+
y|\x0013N²E\x0015\x001e8\x0008rwv\x001f\x0008XÒå(Ó\x000fpÏþvÿKJrçû§ÇõÃãýâtýü|¿'WáHg¨Ç
,\x0003ªÄø2E´Õ6ýöÇÙ\x000f«w)SÊï¯.oç«ÅéòúzÕã0Ì¨üæ.K?@îD0_\x001707üðôr\x00182
o\x0007¹ÿ$y)§Tú/ä\x000b-Ô{ÑÝ-`~øüêv7\x0018UQß8\x0018]Ñß8\x0018S1ß2t\x0018E
fø;;\x001eí0ÚJkNrÊ\x0012%r\x0014<éþx¾&ÓâùË_è¯üBÀ	\x0018+Å<2j|}^Ã(Ç\x001b±­Ï%Ê\x0003ÄOëþöðËPo¼ÿüyýÏyQÈJ\x001dýpà,N©E"D£ì7Æ±\x000bûWË³\x001fÎß
5ÇÕÅÅòÏ»Ñè\x001afFc\x001c4\x000fh¬ÅÞr£,½
	ÕýÆÖh,÷ÚH\x001aÑÂ¡°\x0001Ák\\x001b?ÊÙ:\x0003¯ÑxþÝZQ9ì4Úh£õº\x0019`b
&2Q`|æÈ\x0006ï`TQ'\x001bío\x000eF¶>Û	¨2!£Ü0hDC4¦«u7\x0013Nã\x0004$·\x0017\x000eêÁ\x0019(;
ã'dÖc\x000f\x000f\x0013Ð@Wã \x0007P.\x0008ÀRóð¹Ea\x001dÒ8\x001bNÜào'×Z\x0010»Xè\x0016éí¶]Õ¶+.Û\x0005	ºäó8\x0006°\x001dé»ø\÷3]×¦k.ÓCÖmJ¦§më+Jê¯Æ6öë×SL7µéÉt\x0010ãÈºÔ0?ß
ÓW'9çhwÕö³ÝÖ¶[®Ïî\x0005l·z~\x00151$Ûõ.ÂÜýlwµíë»[¬­\x000fºô\x0002OªÊJkÉv)vÔö³Ý×¶{®ï®ó N²]\x000f}ù»KÚî¢ß3>ÅöPÛ\x001e¸¾»$If\x0013=¦®ÉËç>q ÏØU@ÙÏöXÛ\x001e¹l\x001f\x001aC³í
\x0013U8«hºÝÕ8²éaí|j¹l\x00170z3Ø\x001eÂæ»ëb|¿zñmTå
«Ìo¢ªä
«@êMwÈ\x001b±?\x000cø$X¢ªl¢ªä
«$ðl7\x0006ùöÁvÔè\x001eÞ\x0018oâªd\x000b¬ñM`\õ1~«ÙsÈj*2Ù\x0003!\x000cãî99p0Ã!è\x001ctÅ@÷à·Ûµ}ÕèùeqöÛ¿>ßyyxÝ¬ªíIæ,7à\x001dÛ¥é<êÑ&Ðr?[]¬nnÏ/Çº\x001dý²\x0001 P¬(t~;\x001bKm*N\x0013]J\x001c\x001f¿\x0008C×04'\x000c¸P\x000b¥\x000cßm\x001aLWx\x0006\x000cSÃ0¬0\x0011IÁK\x0012fûÎH0F)Ï&Â°5\x000cË	\x0003\x001eS3LT5 \x0008T°Ö1.«Q8V\x0014:\x001d=ÝèÄrÓ\x001a\x001fj\x0004Ã×0<'àNpK¥ÜÈ\x0005\x001cm ­è\x000cã\x0001\x000f5À"ÀbÞS\x0006yk\x0012\x000cGaGi&Â5È\x0007Ã¤xD­\x0006T#²Ö3áw(§MQÝ\x0014 ö	V\x001cª8ª´«<.¢±Ë´«Æ\x0007f&áhc8c\x00107B
ÂD¹\x0011´H\x0014¨P# çz4Q\2ñC ÇÈ Ô50±l*Åç¨d\x0013ü$cô3 Ñ¡\x0010C,Ê\x0005M0Fd÷¡ýÖüHú¡\x0013¸_|Nií\x000fO/÷á/á3á@\x0007s ­òB}&Ëè¾VÝ\x0002<ò¯\x0016\x0017\x001f®nW\x0017ðÇá?³\x001bªq©£à
¶Â
rÅzÐ|$^Öq\x0011ËY¸LË\x001c\x0005ÓE:ù4Â%Êðµéú\x0003p¹\x001a;
®t½Ä\x0018KÉ@ëeºåï\x0003p\x001aW8Î>ôeô_hbcPZ}È\x000fk\x0013R\x0007·!+m>¤\x0012\x000e/:¹Dâo¶½Dç\x0000X×Çq\x001bqxð"6gM¸"\x001d/\x001bzw\x00035nC\x001eÅo\x0018YÔ?%\x0012y±TÑPî\x0018+Öø
y\x0014Ç\x0001íàÈ0åRÄ¶t\x0013°n«Â!c#q]ÇÇ\x0018&r\x001anHøå\x0008K'<´ä=é±Ë\x0004æÊì>½\x001d´tëvéÖGY:¤"\x0010Í\\x001bTf<§-w\x0019³ÕnËr«×öÝúÓýç{TÓ: ÿÌÃ¢
-¶Ñkì\x001dV¨¿n$ÝV¦ÃöÝòMJ{Z
(URÿ& t
Jÿ25(óo\x0002ÊÕ Ü¿	¨P
ÿ\x001e ¤h¼ø7AÕ¸?ùoâÿdã*ä7ì+rIn¿â5t-\x0017OÏÏëÙ2&]¥ðJ¢dáPûÑÑCwÝ+$q\]_/÷B j\x0004\x000fÄ»ý w\x000fa=^ª¼î\x000bqNE k\x0004\x000f\x0001\x0011C*iDµ\x0006Eû±{{ÀÔ\x0008\x000c\x001f\x001cî	FÃÈ£¼\x000eã/Á\x0013\x0010Ø\x001aeC`ÛÝ ]?M\x0018ªTzßo'ÀÕ\x0008\x001c\x001b\x0002çh _Z¢pZ\x0014ÖZoFi '!ð5\x0002Ï nth\x001dô\x001e\x000e\x0008\x0002ñ\x0007{³£ú=\x0001A¨\x0011\x00046\x0004 ;\x001a¨N\x0016&(â G<.\x0000±\x0006\x0010Ù\x0000¨pâP@4FdÓB<N8?\x0005l\x0003\x001a_DSth(4»B\x0016\x001dÚ¨\x000fñEÉ\x0013$.1~¨br1t\x0014#ý÷¿{¿?{\x000b\x0018ÃÐR§ÈÀÊgÐfnóðónëUm½b±ÞãÓnÐ:"¹\x001c¦®³õ0\x0004Ìe½®­×\x001cÖ\x0007z$HÖ;t Ò(dp\x001c½f»©m7Û\x000eds0\x000f\x0002¶C\x001cpyèÚ ï\x000fÊ¹L2ÞÖÆ[\x000eãÓ1Å]#\x0005\x001eXiH\x0000&~1ñ¾6Þs\x0018\x000fC,2yMd`)\x0000câ\x0010@£ã`ë½T­¿ñpu+Ö¿¿Owçõ^ÃÍWQ`æ\x0019¢\x000f;\x000b\x00131`(vùÊ÷«ËËÕõòëÓíª¶]\x001dn;\x0010çd
d¥ÎÓÄÂFF	qòdªéº6]3|vðù«Ã«Ï_ÝÑWï>\x0002M6ÜÔ\x001boû?y²¹\x001d,Ý´\x0014ºhvùÈýM·µéáK³!*±Ièêe)¯é·OµÝÕ¶;Ï®%(¦\x000eß]êÌ".¬Åz\x0018ë\x0013jº¯M÷\x000eô*u¡±·Vhu\x0010ú£,S-\x000fµåá£\x000bC\x0016ûPU>ºÜå×÷7=Ö¦G6IÈÙ@Hn=te±\x0019*\x0004Ù§ÁhúP\x0017ÝD$ÁpNCÄ+TÁ \x0018$òë"ìÈ\x0006ö7¾
§\x000cñô\x000füðM8\x000cñ\x0014nß\x001a\x001d¤\x001b-\x000fïEJ»ªPû\x001bß\x0004TÉ\x0010QÿÀ\x000fßÄTÉ\x0010TUº*á/\x001aâhÂhùoØYzÚßø&2IÐ¤¤Ã©\x0014Ä&¬\ÆõD§\x001aßxxÉàâeL×<4\x001e\x0014f1:ylw\x000bÁ°ù\x001aÕ8JÅà(E2ÞÇíÐª´%´ríyÕæî\x000cÎF\x0004U¶²p\x001a\x000e¬e3^È¡¦º6}<<7ÈMNCB&\x0004%dPäÎ1JíQdý?ZëÿÁÙl^JmÔ5ÚPR\x0006
3\x0007ÞTØj°P¡ºõÝ¬\x001f\x001e_þãûÏë_ÿ¹ùcäûÖ\x0012ù¾\x0016TrUÑa¾`í,ífy~y»øþbùáë\x0018
\x001a]£ÑÇ@l\x0016R
ÈdBnÆ8S`\x001dp'óÁ15\x001cs\x000c8~àä\x00058ÊSÃ£J1\x001añX»«¾0	­ñØcàq\x0005\x0016F\x0005#Im¥ÍæwêIx|Ç\x001f\x0005È·3«¥,»Írvâo\x0012XÃGC\x000fHVECl\x001b\x0011»¼­õ}²ýàäç
\x0015·\x001eä·ÇËÃòùõã§ÅErµÙ1ÿÁÐ	ÆòúÝòòÍâ"ýÐqÐ
]£Ð|(RA\x0016`ÌÀ\x0003\x000f(.l²r´Þ²'
c·#Ò\x000fJnýÓß_ï¿,Þ?ßÿzÿ<\x0013IÿÈÇ/eJZP#Á;\x0014<ÁSb-Ïþónu³x½ú°ºÞ\x0003ª(V$¢\x000cA(¡p_)/-!£ÅÉHB$0"Ñ1ÒS7\x000cËÃôZ$n¿Q¥§½qD¹Å\\x001f¥o\x001a_¿,><üüx?wÖË\x0002Eq~°\x0017>âzh£±ª\x0017`W\x000fÑÍâÃùÛË1± B¡j\x0014\x0013E<\x0011\x0002Îyn³6\x0006IåL7ÄO@2v- ZçüÝúùá~qöþu&\x0006iô	v\x0010\x0001¯Z¦H{+Ð³ýè|ð»åõùjqvþu7\x0000U\x0003Pl\x0000 ¹Âgû3Jz³÷£-\Ì×µùÍ|eP»M©tÍ\x001fP; Ö8ÊÓ7	©\x0011\x00186\x0004Úè|
ÿ¡!Ú(µ ëLB`k\x0004
Aº\x0014\x0006\x0008<6@©à!\x0004nìmg\x0012\x0002W#p|»È\x0013\x0007ÔPÑ\x0004n³ ?66\x0019¯\x0011x.\x0004"ÒÅ\x001cFcOLÞE!Ý\x0010\x001cm Ô\x0008\x0002ç.Ê²ÊJÁû¬¦]¾(ô\x0007H'#5È·\x0006²\x0003HÄ3\x0000¢\x0000R~&û7sC,\x0013l\x0000Âf\x0013yRXAÓ$|pË\x0013É6\x001a³cÈ´/\x0008"®AiBK\x0010¸\x000e²lâ±ä\x000bÈ*"ýt:ÈX L®¨:Â(1Ò$\x0000MDl!YärÍ°\x0006À;\x0008Ò\x0015Ö r\x001ddÙ\x00044É\x0016ÑÄF\x0013.%sÄÖ\x001a¤'oê\x0015Û6jâä\x000b\x0008êMÀÃ\x0001hòa¦ñÓ0Î\x00071	BãN%?ª%êÒw\x0001¹\x001d1sQ\x0011ô½ x¿u;ð¾Ü\x000en~úÛýãËÿ=k	½:¹µ]ú(0¢iá±;Mt\x001e±ÿ&]r.oÿÇØè¨÷[W\x0003ïËÕà`ë£&Ug=íRDG¦»±O?Át]®L÷nc:Á´\x0008$ÍÕ¨¤ù\x0004ëMm½á±^ë+«  \x0004\x0017äáÓ{y±£yÐ\x0004ãmm¼eúôÁ\x0011­DH÷1Ö£Rk²^sYïjë\x001dÓ§÷ê\Á¤¤\x0018X\x0016\x001fÍ&Xïkë=×õð5X/ÅÆC+¿ÑiÛÚúÀôíS Í$L2Xú\x0001\x001a<
}û®ÆËDëcm}d²Þêb}Ú91O?¤£ËÎ\x0019\x000b·û[¿ÉýH%xÌ\x0007Ê¨\x001bß)ÌÙ´*SX&ªàN0¿
´LV\x0007E\\x001b)»Ä;xG ½\x0013GÓþ	æ7V2ZPË\x0012±É|]¨Bèí6}ýQ>¸	æ7ÑV2[£UÙû^cS@2¬\{§	X)b%¯H2`}.BkQæøÓÆ\x0004ë%"\x0001¡dÚù¶öÌ\x000f£Ê\x001e\x0013Ìo"d
Y\x0006æW1Ùñ¦¯µÎ¾"O°¾ñùÉéàqäm°>óQ\x000ecÙ;£ÕÿýÍW×TL^ÓJ¿9·øø"\x0015yüQÊß	¦7.G1¹ôí)Ã\x000f\x0006´1¡8ü>iýÄ$¹f\x001dÊ2Éi\x001f++¬x¦\Y@þpM²M5*46å~øûçö\x0008?°^Ë -v\kihÞ×<§äl]µýÇz!pø-\x0001tS²Ä.Ítªí}¤Øö\x0011\x001bD`0y²TVA3¥\x000fi\x0015>µ«ðíÆë0ÿIÑXaòìoË8®K£Ù^\x0005ÃwÓí+s,C½\x0004¸KóV¢w<\x0003Eh¦UøØ®ÂG¦Ë¯ÃFøá\x000eîH)j*0ÀÝÍ\x0004àç\x0016ÀÏLþT\x0011yU?5e\x0001ØÑO­ý?1Ý!=)è\x0005C\x001dºL\x001b?Ú\x001a<¥ø°}
<ë)øcj\x0010qC\x0017aÍT\x0008ØP0\%\x0003ÞÅ,q\x001b¦«$Ob\x0000Ü·\x0000îy\x0000@9Õ\x000fÍÅ
±ØYq \x001f\x0012f«»	¦ôÛî¦Ó×âå%ýéÝÓãËÓóÏ¯÷\x000fç\x0001=[¶BtF`!2Æô»Û§]u	Þ¥¿ÜÞ¦?½»º¼½º~{·:¿Ø
QÕ\x0010Õñ ¦\x001b´Ë\x0010½P'Â!DÌ£íë\x001cÑÔ\x0018Í\x00111\x000c£ú°\x0016y~\x0012DDhBwWÎG(·[<enñ¬\x0010=?=|\x0019 Î¥£³'Y²Þ§\x000cØæ\x0007g§P\x001c1ýÓî@Dëìúêüf\x0000¶\x001bªÁ(f0Þ YºÏª"ËÒÇ	Mè:¿htFs/
¦0ØgIfÁé\x001cR\;UÃ'¢15\x001aÃ½6>Ïú\x0001\x001a³~im|AÓ\x001d ÆÕhÜ\x0011v\x001aö ÊbÚi\x0006wZ¿h8\x0013M¨Ño|m6¯\x0000K\x0013ß8ö^\x000f\x000füðmÛ $?¨tQË\x0002·)üH\x0012t$pÂOW¼dPÃ\x0004aÊá[\x001e\x0019
O9e\x0012çózq¶~~~øí¿÷bÇl¦
CRê\x0000ª¥y$2Æì
T0}¢tbÝZ.Î××ç«ë\x0011â-\x0002 j\x0000	WÀ¥= ðTFJÿu"Q2f×\x0010ù$\x0008º ¹ \x0004"à2ð)¬Ò¦ô\x0004at4b*\x0004[C°L\x0010@Ú*5\x001b\x001bObæ\x0010\x00138ÄÞÉ¡7\x0005¯!x&\x0008Ñ`×\x0016ì\x0013D iÆìàÈd¬í<ö\x0003³­Á]$\x0003
²Ja
ÐÅÑVðÉ»\x0008=lµ¨qøJà\x0010\x001al&ë É%¥ãr\x0018!&\x0004µu?	ª½,n^?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=øa7ªÑÔ\x00104,>áZ^ãK\x001fO+¹Z6¬é¸;\x0004-Ôha\x0010\x001avM,¥¨ôf«\x0005Ï~
¾»«ÃÈªü\x0005ÜO9lÕ<7Ü\x000e{£ÄU+5	bM?!lºaÓCwÔØÂæ-ï(G;Ä~\x0000CØ\ÃæÅiAüØ&Y\x0007ÑM²\x0006Ùå2JíÉ:pÃ\x0016kæ\x000bWJÙ¬që\x001fHMv¹²ä|[Þ'£Ê\x0016UAõn_ç1	Ö\x0007\x0014;î+\x001aQå¦\x0006ÿýP½IZ¯ògÍ\x000b/:´o\x000fß"ùíõÞ»ëmC|£È9«Æáè¾\x0014\x0017\x000eÃZùyÜn÷oÞ.Î/ã'\x001c\x001fî½;:<Ú6Ó\x0017áÁTÍ\x0012=NÇ\x00130\x001e»0\x0013¼ k(ÂóÐîèiìV5\x000b~Ä®qìoWÔTDãØ1|·õÀHú(¾:
\x0013åÙ*\x0005ëàþ\x00165úv78gMI°Aqd\x0003\x001e\x0010¥Ø0Mùàô\x0018ÕùÖDº\x0013\x0001xf\x0018\x0012zLXn¥áæ!¥\x0000\x001bFÆöÇs5\x001b¸zy||Î`Òw\x0005¸
äÆ\x000c¶Ýx\x0000ªÝ\\x0000Õºå÷[¤â£º°Ô°Æ±$2p)ôº\x0010]^miÊh²FCÐÀk\x001eÔ\x001e¤%/\x0002·Ü#Á®KKìO¦j25,j%.ÔÀN:ôx\x0019x^Ðë:\x0010
@Ó5\x001e¶hê÷LPP
H=°R·k'÷G35\x0019VÚ\x0006\x0007\x0010ÜKaË5Zµµ×´?­Ñì 4·êð£l~?Ã²VÇ\x001bê6¦ú¡¹\x001aÍ
C\x000b8z#¯§\x0002\x0004åEi4mÍ|
æYî©\x001d ?\x000fKy;'
P¡»)©,\x0015BÊqÒ_0k'­öFVÜ\x000e·à*¡f¸3ã\x0001F¡ûê1\x0014­\x0011·0PÞÊ²lÖ~>\x0007 ®õ£°5\x0002\x0017IÜ¨8%ùQX·O\x0015ÓNð\x0005µkëöû³5\x0012\x0017\x0006Üòº5"\x0017É\Ë\x0003¹q4Ö>»¦ô\x0018\\x0013ë\x0018&-\x0003·
6L¤àx\x0013J\x000b5\x0011>hRåÌÒ¹\x001b!\x001aïóxù5út_nî·\x0019nZxèó8[:\x0015?b%25ÖÅîÊ¦d\x001d/.¢Kwvtºíõ@u\x000bªGFQL !:\x0013"gª@]70aÓÈ±> ÂN\x001f`y¯Ï¿^ï¨C\x0010\y(´)\x001d\x0011ÁptÆÁÓ}>[¼;Ü\x0016\x0004´Ý\x0006¶4àÜ	¤*É8}1pI\x001f\x001f¼ *®@®\x0006r½WH\x00143ïw%Kz&¬¹¤=|
ä{\x0003¹ÒäÃ\x0006\x000e¨\x0019ÉIÕâÉTÞ@UW\x0004â\x0012¯^DÜþÁzÖè¨ìÙö=dC${"¹ÏéÀýÛ\x000c%¥vM-\O æAß{Ç¸Dtäø­*UÅ^={\x0006ý/¡ùq6Þ)2u*Ã#`Må. ¥[§R %P%uæÞåÝãOË\x000fß\x001e\x001fv¼NZn"ç@sO*\x0004ãÚ-,ù½wqrõzqpyuÞW×¼z,/hÈv\x0002Û@%^6\x001dï´\x0006Àkj^3a}yËl­¸¾ÀÀaC\x001eòp`[\x0003Û±À¾´søry-»Z¾;»z\x0002¯«yÝ\x0003SæS®D5p\x00004ØÙC
\x001cF\x0003\x001b8­Yj:Îý\x0014]{j<o¥g"/Ñ'Âs\x001fGg$6UÉG¢ôNÉ	ÄÐ\x0010Ãè%.ñ<$¦ Ãºq&ÞW?¸Â0Z\x000cÿ\x001f®q#a´ ÆR_\x0013è\x00170±æc\x000c³-q#×`´`æâ!mjSeÈál\x0003|\x0003ìG\x0003ÓÜ¤'//OÊ¾ØdÅ\x000c¶;£Øvìx}\x0019=Øëoß¶'\x000fi(\x001dßàt°\x001a'Ø¥mý^FWöèðòr'jÜ¹\x001a\x0015\x001d\x0001ëtiâ\d\x0015\x001dR­\x0016]ñY`C\x000b\x001b3¬m\x000e\x0001þ:
{7¥ÀF®äÅ\x0007=f[Þ©\x0007°ªU]X0´°RÚ#+¬ó6\x000búÃ\x001a©kXüu\x000c¬QÜ×ÃÙ\x001cþÂköjÂÈÆ\x0010TÛ¢Úq¨Ýb¼FàDñZZU9D\x0001tT°øë\x0008Ø <\x001f±ÚPÁÄ@*e6k·%[¡\x0007«î\x0004=´ÉÚuýßÿúï\x001fî\x001fò\x000bú»ÛÛë»ëÇ_·QG;×Ò\x000c\x000bk±UI®sóü\x0010\x001e7Qïýpz_Ðß\x001d\x001d\x001f\x001f\x001c^½Û¿:Âß9ÁÃñ­	ª\x0014
vnß+¸û¬\x0016ÖWéÅ\x000f¢Æ\x000fbêêKÅ\x001e½ÅF¿9ãÂ\x000bîÔe»3i'òÃªº=\x001e¥¦~\x0000\x0004Ì\x0013Á\x000fpÒãCiþ\x0000EÚ®å6ß5ë\x000fnò\x0006ä\x0012øÄ¥½¼\x0001,aâIõ\x0003h>@É\x001f`\x001dõ´ÞKj\x0015"¼-Ãô¤ØÔ6sÌ\x0007h? ý>ñ
\x000bI]°	\x0001\x000bDñ\x000bÐÄÎw8êä~Ø\x0017D#\x0012· z\x0016°®\x0016}}ÿ°u| éÐÄÕ5û6&Vò3jã­]ì½>=ß6Â&CZgkHüu0¤£ð¥GÞì·JlªHÝ&Tc }\x000béÙJ6r\x0001(½;\x0015ë7\x001eo¶N=vñ¿\x0002Ó$\x0011;ÈÑ¤@eiX\x000cÆn.¬?zsu´mæ11J_3J?ÑbwÓìòGFMM3âÚñ\x0011\x0019;åÊ#\x0018«Æ(Q©çÅ¨;Ítã\x001f^È®dZÜ}ºÞYGéátû -ÀAKá7M\x000bâhqòæpG\x0015%ªô\x001aîG\x001a-No3©á©#Qøó\x0010v±Ù:\x001eBjjR3T;JÎÔ«é<R\x0004Îvu3\x0012ÕÕ¨n\x001cª×Ø<#£ZEaöAYÓfü\x0010ÒPq¤ÁP $J*!ÀæjQ7\x000bÏþ¨`l¿¥\x0011\x001as$±r
L¶áVIÙ\x001c\x0000)å\x0011P¢\x0013*S¢\x0013*CÃiùpým«ZÒJÂ|4Ø7Ö@õKXX¹éJ¡­´8?¼Ü¸ÊÐFD%\x00063ZC=T<¶w§¸ÖôÂ¦Ä¦uìO(\x001bB9\x00104P×B²°7<NOA\x0008\x001cÈÞ¦YE3|\x0015ñÒÒ*\x0006çKm\x0004ï´÷îy_FXIÎt\x0018\x001b\x000e	¨øp§&b*Ab'§j\x0015\x0004MÝ\x0006A{ív\x00104\x000cÆ\x001bé¨ý4¬M\x0005rÂìÍh[­ìà{ýÏd!5ó©F\x00026ó\x0011\x0015äãÞåÃòývDï,\x0015üiÃâÒ^+í³Ç]\x001fG¾Ú»<_¼ìC¨:j !:\x0013PzOUbJ*\x0011ÿ;ÙÔj¨/¡é\x0010gGè:îÙ\x0010
Ùå)]ú\x001e\x0015õÑÝÇ?þñåúîãòîÃöG«\x000er¢¼ÙkSÚÉ(·>Ó|ïèäÕáÙáÉ«ÅÉÁÖA\x0006ÝÁÒÕ¹ðX£Fy­Ñv£²\x001amC i×ç\x000fDu5ª{ÞËêkVÿLYj
6|ª*¾Î~{øã\x001fwüc{Õ\x0012¶\x0014£~Ã½#\x00035àä¨M£qÏþt~xr¸µ¦ødÍ'\x0007óE2äX\x000c8ß\x0012\x0001×VF\x000c\x0001T5 \x001a\x000e¨J6WØÄ4\x0003rZC·\x001fË`<]ãéáxºÛ\x0019-Ù(Û	Ï
\x0013\x001aú\x0003º\x001aÐ
\x0006ª;}´Ë©Éz.n¿¡xU\x0010Þ\x000f1\x000f¸å4\x0005\x0017,7ävÀE`^o\x0018áÛ°¹!0üüó	mChï±ã0ïRÌ%or\x0019ûÞ}Ï\x0018L(\x001b)(A­©ïó\x0012\x000b±è\x0012ó\x0012ª
ó"{\x0000*Û2Ê®ú\x0014¾]>>ÜÄÿ÷åõÃ·åÝÇízÚD[ªâ×Î°6	~]Â·«ó£øÿ¾<<æÏÉ«ÝºæÔ£8­ R¶Ô+Ù2ji¥ÚIâ\x001eKjjR3nE%w\x0016XµH
­ç|Ñ	þEµ5ª\x001dÊs\x001e¬ÀÚl*àuÀY2`æÙW£ºq¨°\x000fjÊ\x0010GkË\x0010G»®åß\x0000T\x0007]Ë\x0002eñ¸wöpýõýoß®·ça\x0018\x0018\x0010ðQ\x001a\x0013r9F$_S×xµwv~xñòOÛ²Îd7.»ÁôÈòåvyóõf{Ñvð40Ë(l¬Å\x0005ï\x0010µ³¼îø·¸ªG\x0017Gç\x00072¦­1í\x0008Ll)\x0001«E\[N®H=w¦cú\x001aÓÀ\x0004Ïd©\x0017«
§ê©'#GQV3Fu~Ö\x001bé§:b?\x0006E^â¼*À¦ødÅ¹ëlVSFSà¤Ù.Ò4v:Óm
«
aÔ
£\x001eÁh-iL\x0010U&dòØ\x001e\x0005vò\x0015í[1bÓ­óô,®ðÑ$wÊ"\x000f}\x0001Ü\x0014Kí½`ìØuëS\x0007¡\x0004kH{\x001c}\x0001¯7÷ûë¦ëº§éº\x0007?/¿\ßÞömdò+¹±[\x0013z§¸ïÚ(\x0017{\x0007?,Î\x000eû5CbtY£wû\x000b=otS£iè\x001e\x0014ÅäªßhñsÍí6ØNokún^Ê`z®\x0008øÊÐ#¾*øÛÚQÂw5~7é{(~\ré\x0018às\x001a°Ö"ãÍÏGcñ}ßM¸\x0019¯\x00025Ò1:ps	Áó\x0008,¿%\x001f|\x0010½ð\x001dy#¼i»\x000c.î>F÷q«ëZõÜ\x001fC«U[5#W3\4r·ÖZøHA:9NiJ¤Mé¸\x000b¢ö¥iÞÆ.=éTM§®Ý\x0019¿ètM§G¬\x001d7\x001c\x000cÜ-¦^»5õÑèLMg®]jÿlid3UokÅ^è6\x001d
gk8;|éHy\x0005|¥!8Ç\x0016áÖ\x0014ß\x000f¢s5\x001b¾t]\x0008Ô
ËÌ¸±¾¦ó#Ö7Vá«+­]ÙX½©Ïe?º*"êWÅùðÎïóX\x000fjî3ç75ºì	×H;\x0018,î\x0002\x0007¸LqÀÙ
´³v;ÞFc\x001fR³yY\x0015æ`\x000f÷¶0çõòýCXxøévy÷ífk\x0007]ã´¤K;¦çÞ^¹2\x00150l2^/^ã\x0000ÃÃ7ÇË£­#\x000c\x0013¸ö®\x0006Ç_Ç{)Ê`eë¹d_D\x0001\x001eç7Ù\x0017Áíj`\x0002ã¯\x0013Àq~\x000eE¦´ ¾ï"\x0018ÅWËªÙVÜ®:'p+&K\x001a\x0001O¹E^ä\x0006\x0016§\x0018\x0012»T\x0014ÿµ\x0019T4ü\x0007Å;©ecÔõ9Ã\x0012;¯pËFµ1ÿf0¸\x0017ÍIñbÊIÁþ:ÖS¿DP\x0008Myê"ÈEcVüÇ÷iìC³êø§ñ\x0007ÆñÂ§þd\x001dd+(7Ò2"
\x0003ø¥îX¨R7NïãÞÛûÇÛü\x0001\x0007Ëo?/o[\x001fa¢È¶dpy\x001b1E¯Ë¢\6dv¼=½:Îð\x0007Ë\x001f\x0016ÇÝÈºFÖ£Íj½6<ßÎ;àçß
Ö\x0008f¨\x0003M&Oj\x0018I­\x0002P}T²»É²µ\mFÍD­ZjõÜ©U*2+!Cå\x001e¹»\x0008§b¨
\x000bØw&\x0017\x0001bA\x0014U\x0016H³)Ð§lAu\x000bªG\x001aI×.zzü\x0014ÚÐÆ\x0008êç\x0000õ-¨®+\x001ad\x0003\x001adïö\x0000Uì\x000c/ 9¯\hÄ\x001a×s£1\x0004Ô¶ öV\x0011r\x0004í\x0004ÈÑÖW\x0011ò\x000cú\·Þ
Ýºõ@yK\x001e'æWzì?a\x000bè¶üí¾ ¾\x0005\x001dsë§@Ç9·9ã\x0013û)2¨ßZRÐ\x0013\x0014Ú­\x0011[/£\x001fÅ|Ôû\ô
ü9\x00190f<h´Y:ÁJ;¼çæôXFrûûý©-Ò+,GO±Uë87cõºhL7\x0013'÷£ß[\x001cÿyÇÄ\x0016ÑíÙ&RÏ¶ax\x000eØÂó)h\x0012gàtD¡Áñx²j\x0017ðt5W¡\x001f¡0&U\x0018lþMT©(\x001bQzµ¶\x000f>ÛSneÛâýlyó÷]±\x000fÁÖ³dëY\x001bÅ\x0016ac§Õ³ÅÑîF5\x001c¦¹	¬â7m½ò»Å\x0014ã¾hªFSÐtÉ±\x0008^`¥lg¿ÚÔ:·\x001f®Ñô04.C«&9ÔfEyXØ8¤®\x001f©ÉÌ 2Ãh%Î¹HÚ¶
lsÍ¦Ò>]5iÁwÿÆ®yyÿðñúáþqk\x0005·UQ\x0014SG_\x001c>Ì3\áeìÆ÷ô§ç¯\x000eã­ÝZÂM¾åôÃ9-\x000e\x000bÊÑ÷¥Üá \x001da°)?¡?¦\x0006\x0013}^ÒvfNJ\Í\x001aòìúÃÏ{ç×\x001fïï¶Abõ@ãý\F§RÜøh{vxðÃÞùá«ÓÝ²Æ#0\x0015äø¹Æ|g*>T\Æ
\x001bÍØ!ªfT#\x0018#0B
¸êù/@nÚñ^&a®îOüÃæú|¥ÈÀW\x0012H¯v4SÂq+c\x001d'¹+.w|1\x00126ë.(8pA\x0012êÕÖ~rÜT1Hn\x001af0z¼[-kå$?\x001cBMÍjô¦îãcÐýJ¸"ºoësE\x0017Ý6
"·Q |Ï\x000c½]\x001d\x0012X,s0c\x0005ÖØ\x001f\x001c7Ú"aëä+ECµuõúayóõë©¤
JìîJ}1£Åk¹@£X&D½>_\x001c]\lm5â:9IØw\x0018\x0003Y`Êè&Rfâ1.tÊ¥ã©\x001aO
Ä\x0013å¡\x0019Ë<ã1\x001cL35\x0019\x0008#2U³Ô_Â\x0015Þá_½ñ\ç\x0006â9l¶û£%yÖ\x0006\x0005&Ò.\x000c£óÊò$T,É4\6ð\x000b×~±\x0003ñ@V\x000f]xmñ÷!N(]KT\x0011\x0003öRq¹
üF¤7ÍvëGR ¹¹)ú\x0010
ß\x0011}Â»6uêß¯[²\x0014%Ñ\x0019m"®\x0014e\x0018õò\x001cþýp±E*3¬Ñä04®I\x000bÑs¥4
§ v+ÉÙÌ\x000e!Ã¦£ì\x0013j_\x0006º2é\x0005[fNA\x000b5Zx\x0016hÑÞü±ôHI/\x000f\x001fÛ
Ç5ö¥19¨¢"KíS XMI\x000b*þ6½è^^\x001f,¶6YÈñøP\x0003â¯\x0000}Te\x0012rÓ\x000fïòVÀwZê± Í÷­ïAµ.ÖKPÉÅ:¾ÿ"äóuÜÞÛhþýûòá#ï·_wwÏRÑb	4Þ2BæF%`\x001c¿~ÎóþñéåÞq´þþ}qþ¬¿wã\x000bê£µ)0PøeÍ/¿?~Uó«ï_×üúûã75¿ùþømÍo¿?~Wó»ïß×üþûã\x000f5øîøKâjÖ_âûûFÁ,\x001a\x000cûc°\x0003lÉ?\x0007ÃÍÈöÇØþ\x0005=\x0012N¨\x0003'py0Æ.ñôñvÇ\x0008g #ÌøÕd\x0018£GT\x0004XWp\x0001£K|"½:¾Øò|\x0000²`DÃ\x0011\x001d»%ùÇÄ8×m\x000f·pç"ªP
'´Q\x0008£¥È^èL±\x001d³ºFÔ\x0011±8Á®\x001eü\x0000cËxânßµ1¦F4ÏqmMh\x0007\x0013ª2;ÞûJ6q{Ò íøË\x0012q7ÀÕÝ\x0016\x000fß¶O;7\x0006a\x0008	¥Éà\x0012
\x001dÖ÷½Y_nk!º®»puÏ ÝTºÙ¸æ<SF\x000b~ÌÕb}'~T¾¦ò\x0003¨$'.Úxj9Ä«¹é5\x0008eÖôÀÝR\x0018YJa°ùñýo;T\x0007öá\x001cç4®8¯ KW\x0016·¶\x0005ÂëÓ?mÓ\x0014²[Ñ(sEcÕùâþvk$¡$_§¬qï¦,v¥êô,ªz2_\x001eoAKÝ\x0010Z½D!¿v\x001a?Ü|º¼Ýìc$O=48&>gä\x001bF\x00142¸­\x0017{¯ÏÞ^\x001do{­\x0011©[Þ*D¤é÷Á¨:Õéä×<çEÎ[7Ê\x0010·{Ë´þ¤²CÚ­}þ×
\x0008\x000c4;æn_¿àkøÖË\x001cªî&âÒ`Àò¨µ
«ö÷\x000e/Îð)|ËJªîCxÒd­á·½7×?_ßÝÝo\x0005ÄÑpù-\x0014ûÈ
R\x001bEsÔ aÚÀ\x0018ÜÞ«Ã\x001f\x000eONNwCÊ\x001aR\x000eÄ>\x0002TB$£
CÈ\x0003^@uÚ·eÜÜAuÁs¸e(c\x0010û´ÊP+chÌË¸ÖÊê( «èÀ=pºë\x00016Úü<\x0019ÒR}\x0010ý\x0000²ý;É\x0004í\x0000µ\x001do®^uèM÷¾óû¯Ñ3Ù®öÀsg7-J|_\x0006ö­üÚ¤¯½óÓèlS|¾sQ\x0017Í³ëùõ¯×[5jØÑøD<gÞZöCë$¿óÃwÇ«}åYY~¡ëÚ\x0007ÉRæÓíÍöÇ¯ÈÅ×#~\x001cõWÁ«Â\x0006_oá£ys|tq¸PÕj8¡\x0001ð%i\x0011=Wc¨µRf\x0010¢®\x0011õ\x0008DGÍS1¨\x0006JS³e\x0015;íF \x001aÑ\x000cG´\x001bíUnô
Ú\x001e¡\x001aÖ{!\x0003\x0010mhG jêó\x001d\x0011}é¡ãu±ôÝäUô5¢\x001f(ÑVÈ¾H`I­=\x000fº\x0013Æ­÷6\x0007 \x001a1@ôØ³-!*C#µ"bàÂd»Ágï(;â0þ¡\x000eÍ &9¾yýðmWY<·
;íöµf7¯´îY1.ö°o[\x000fJYSÊ\x0011ØYFÓfr«%óè7]\x0001ª¦T#(.=\x0010±Á)GQJ\x0019
lº5»)ß<µ«Ìx¡QüõÅËû\x0014<<yü°\x0005OaCN£ÓJ  ÂÇ\x0005G[-£Ûâ½<=J¡Â«mXhÔ`-rÁr/Riòq´\x0018^>üño÷_÷Nî\x001f¶ö\x000f\x0004Á½æ£\x00087|\x000e¥ó<·2ÕdÕ!Íh4¼<?¼<½ºØ;9=µÐ·~(!¦æÝÑÄÎYG @0¡vã	}ûTfívø.\x001e·á¥\x001c{êùëµc³°$Â>	²Öt\x0017W=àB
\x0017\x0006Â)(m±½Ü÷TYí¸E\x0003ö·@\x0017ý\x001cQÓ¥ß\x0000Æûê°¯Y²û±-[Þ\\x0008\x001d<ßiqÑ\x001fPÊtúÊ3jüÃ\x000bü5òí\x001d,?^þ~ÿ¸÷r¹Íª6ß/X»¯\x001c\x0005\x001eHúùÐé\x0004p5¯oß.þ|zµ÷rq±\x0005Î`Ì\x0012c5\x000ceT¯\x001fw\x001fv­\x001a\x0016OdâãfbÊ`J\x0019Öç©N³×ç\x001dëHÍF¤¼¡}Ò4 ÂVô@òTY\x001cNL¶\x0013PèÃdÑßÀ\x0007\x000bf\x000e\x0018þúâíõ·åÍÃÍõÞ\x001blº=ÎárÛlp"wÑà]¼\·£ó£Ã½7Ø\x0019ufHíÕê¥2õ4ÇPv¿Ìolía)^sÃèÈå¸\x000cáIáU¾÷.¨Õó]Â÷»¾)ó\x001eét*²§yÊîNPn4\x0014´PÐ\x0017ÊYàl^9c\x0012H\x0007D(ßiÐ×\x000fÊþX×ÌG(kæ1wÿÛÍ·½³åÃòãÍVÇÛF	F5MKg©^½[i»¯·yt¹w¶8_¼:Ú&%\x0010°¹\x0011elBÔ5HVñÎ\x0008"T¡Ós\x0000a
\(½Ú×x^ðW´ánî\x0011÷æñæÛr«Ç\x0016\x000eEâK\x0002ÇÆû¡òöF1ò¤ßòÑI²àÞ\\x001d].¶éxHæ\x000c«t\x000e\x001c:õÛÇl÷øûõ·½Ã¯ÛÅljJ\x0003\x0018ñNpv,\x0016Aç:I'ìðÅâêÏ{\x0017ÛÈ\x0012\x0008«D1|B
P>^ï`[\x0015qzá±Á[bS\x0013m§«Û
îôj7^}úÒË\x001f¾¾|X(msã¢ÿÍª³;½ÔOÎ^O<ÍòU\x0014:\x000fhÎ¼»ùt\x0017\x000fÜ.ÃR(Þ »\x0010lÎ<ÁXNHïÝÑxÖv\x0018cMuÃÉ6iÝV¥Íÿ¶\x0003ÎHÅÏX^DáS
¢Eñ\x0014é»i±«ªæ|>\x0019F\x0015¿Vx»ìJ£eé\x0010\x0010½\x0006;\x0004\x0018[ºXØeTÑmÕø\x000c\x0007-\x001c\x000cz\x0007ºò4>KhçÙ:Òñ½àäý\x0002ùc(UßMlº\x0019ÿïR1³\x0019K&¬ÏËÇ\x0007¤\x0012¹ \x0003/ª±8\x0013\x000fYQ¹ZOéáÁérÚ°9;¿·`ÍÅÅåâÍÆzæ\x001a\x000cÕ|Õ\x0007û_Nöû/>=Ü¢ÆËÏ÷w\x001f_¿&~\x0013\x0011\L1¦¨\x0019ÞW	(8
Ô\x0005«K
d\x0002:_Ä=XlN¡?þöëÇÇ/\x0010\x0004ãàøÏâîÓãoËÛ4©b\x0003\x0003+³n7æm\x00041ñ=\x001fs\x0017í\x000eY,NÞ\ýi\x0011]g¨p\x0000&$¥\x001f}@°»Eª¼1X,ã=\x0010DñW¯WnÒp\x0010 ¾\x001fHôÁs\x0001\x0015v°Øâ\x0014A¢1´"«þ\x0010A°\x0019BúÑ\x0007DA\x001a¾ \x00123Ìm\x0002±eE\x0000ô@¿Ý9ùû7\x0004A-ý8^F\x0007ñááæÿyØrl´!sKc\´dl:&ZpÅ\x001bIó5K¼9/\x0017çÑÃ8ßä\44\x0016ilo\x001a\x0014³4Æc\x0006\x0018Ò§L(ýJ7²\x00114hê¤\x001f}×í\x0013c¼Jý\x0012
PSºx½­\x001aO£ñÈà¾4Áä\x0019$&uË\x000b6Ó\x001aÌ*Sj0LÖðd\x001fõÝ)=Ñàó\x001dÑ¸\x0000´S*\x000cÆ±7æ· Ãÿl ºøm\x000bKé;&\x0000ÚßùVKO.²\x000fÂÈ.ÈéùzQÄ\x001bl\x001f
kP²©D\x0011ÍF-Ú	\x001bh9$<9¸})¢,ÀzP`vËºGÔ\x0010×"!´)Éâ\x0018I\x0011¥\x0000þÓ"\x001dÏk¡£Q^Ü\x0011AéhAzr4úRDeÿô¡0.?RÄµBVL\x0001ü\x0018â×ÈµH5íéG\x000f\x000cÖy¦P
KÏñ\ø`É\x001c\x0000|¼\x001cBñßÞÑ\x0018\x001d\x00044,Óc´Rßôm:G¤N/¨s\x0014\x0018<%IçIîáÉb\x001cäöèAþjï?£\x00170v\x001alQÙçâ/åßØ\x001c\x0004í#ÏÕÁ­:\x0006¬HÈRë\x0012\x0017S÷F±:\x0007fÐv\x0004|uK(ï¬Ó:L@ÃöFQ)Ç9¡`¬P\x0006è~NXd®õÞ!g\x0014F1%=_d\x0016G1¡à\x0005&\x0001Üô£'
}Ú |=É$ÖyÞ 9a\x001aÛä_ËÒQ¿}Î\x000e¹ã¼I³\x0004²ö¦4½+\x0005kE×jÛI£¿û/_ñ¼`­¯\x000fôØðK7É\x0015|ÖJé\x001d&\x001aú\x0006Õ(Wré>GC\x0012ýÔ$øÌpu±ñºæ\x0008q=èÇ\x0011â
\x0016IÜ[C\x0004ÓþØ(ëtæÀ\x0011ßÃ8¾Èð\x0017óÖ#2¤Êåï7·?/?l\x0011÷\x001a'\x000c\x0017?\x001cßþPÜ\x0019êx¤AZ×`\x001c,þ|tüÃbÓ[iC\x0011ï\x001dþÓÂJMF}\x0014\x001c\x0001}dØl¸F\x000bÖi=âAÿíÛ¯iì\x001bú»l\x0007¼¾øãÿý¶å
dyé
#2lEcQÑi|J_â\x0004ðM\x0018\x0000ïo?þ=-F\x0014g>´×\x000fË?þ¿íNyêf\x001exâ)\x0015
çGàÄÿy:\x001d&¸®TãÂö\x001e,Q4{ÕÅ,\3äà\x0004A\\x0000\x00127ÕëÞ ÑTeUì£m"²ÍjC«EjÖ?%þG½ë¿AX>¯ó\x0006IE6£F\x000bKÜåo~ùÛ_R¹w×Ñãî\x000f\x001f¶¸æÉ\x001fWùæ÷¨#\x0007xp´?n5ßÄÈÅÞ\x000fW\x0007[<ó\x0015EÜX\x0007ý(tJñJ\x0014Å;¾­\x0019¢\x0010\x001dñ>"^\x001aü§\x000fE´\x0013SåF¤0L5ðB2\x0019¹\x0014\x0018í~~ôÚ\x0011Æ{^\x000bKv|Ü\x0011M;b×c1Ð\x001aº\x0017\x0006XïÂéâf\x0018Q®[º¸Ð±ÐvaüüË¿üåo)ª'ðáÅÅãß÷Þ.o\x001fn®\x001fÿ¾Í±	"\x0017òE\x0015£,\x0001Ù±±¬aÚ\x0013º¸úÏ½·ãèy_ýçf-£î¾ürtn\\x000eüçíòîúîfp7ìØh´£Cò'Tü\x001c
ku#Ûß.N\x000eO6\x0002|þôð×[Ùðg×w\x001f\x001f·95QILâKÞ\x0015øý@Þ\x0015PUf\x0010«Ìa\x001a8.ýj[S@RÛt l7
NcL©48ÇÌ¢_\x0004§8¯^y£à\x0003GúÑoU@áÄ´*Q\x001cDsA+ö9]7"Ò\x001f\x0005­¹ô£\x001fJô%Ø	\x0017,\x0000ëB\x001bä`èªÜ½¿o7)ø«\x0002yUÎo~]Þ<Üãì°?þx~»¾û°\x0005LãÓcªÊNX=¦v\x0017üª'\x001f½[\x001câÈ°E¼Q:<9ØLùþÛÏ·¿¥c!j-¦ëmA5úì\x0006Fç45ÝM\x0006\x0013ðkÆ\x0013séâð|K<­\x0008\x0008\x0011úAhzõöHó[\x0012£LAÉ'Æ¾\x0018?~ôÁÎLòvò³\x000cºÄ;µ\x001a¶\x001aË¿üòñcJKÃ©ÂÖç§àûÇÛÛ­$'s
\x0002ö\x0016O=}¼5$6ª=Ã{\x0017§WGÇÇG=X\x0000º2»vÃ8ýJÓ¹ÕÑ¨¦Í1JR\x0017Z¯ñ\x0004\x000f1¿üþ;¤ð\x001a&Äú¼0Ë\x000fÑ\x0007M\x0015N\x001b]?¼æ·7\x0013×Èë'rÝ\x0016«Yír¹8.èéÕF~ÿð×I{\x0014Ï\x0018þ(ñ¤,ãÂl±Þp\x0000Öiò\x001camÈ\x000f\x0005!»fÂÞe<.¸4}xRÈ2ýø×\x0002Ýüzûé7NüÌé©éøòÓ¶#¬%»?ødÁÁzS"]Ø³ªÃïÊ7\x000fM\x0005\x0012í\x001eÕ\x0017D¤µ	D;|êI 9\x001e%]èF\x000búè¨
´èI"CÈÉ&ÊÔ\x001dI´"åìØ%iÂ9½XÐ9ÎZÒ4ê+Û\x000eÔ;(/»Ge\x0017Ki\x0011ò\x001fJÙöãÞÙòÛV¡H@v2\x0012\x0015s\x0004eÛ¸5\x000f=_\\x001em~È.PªR\x0003 ,ºî\x000cå\x000cC\x0002åÇCé\x001aJ÷rv\x001e~ÀÜÄä¨@1`µÄx&[3Ù\x0001LTz\x000b¥ø©PY~uP¦}¸\x001c\x0004EÙ|¤D*T\x0006¢\x0012dsiÅïïJ_*êÂTr\x0000eA`!$âHª2ÂjÎ\x0014\x000c8TX¨D'\x001d$;6Ø¨ô¤
,SÄV\x0019°Ê}T÷\x0011Ê>`S¦#¯©äÕÛåCêÜ»IÅc.òE(\x000ck%q®åXw´Þ.Î7ví­dÍ$û3é(\x000f
É\x001e¡6j\x0006"]\x0013éþD:£Ò\x00032e5Ú"Ä\x0004~Ýaï	ek(Û\x001bJ\x0006NáB¯LËXÁx(_Cù\x0001PÀgÜ\x0004`(\x0015x¡¤3ãBÍ\x0014ú3yöYãBñvT5ì\x001dªU>êp¨Jª+SKõÝ+%÷¡,\x0014\x001b
A\x0016;Ê?çÐÜ<èõd´¸\x001dÉO¡pH^*~eVÊ­³\x0014zR©J
 ôV\x0016×JcZv\x0016\x0015`Jí\x001eL%}GrJ_7è¡Na[\x0005á\x001c0\x0003©\x0000?Ý@\x001e \x0012¢³\x0019p­:íFS5\x001a\x0016m*Cg^ø"D5Mhêé\x001ffj43\x0008-ê>ArKè©µä\x0007aiÔÓ#6,Ôda\x0008\x0014s³LplhIïY\x0019*pSÐ =jÎ\x001a6^òd/GLðÄÆù±j5
` vk ];\x0017éü|y|{óËãV\x0017ÕÜ\x0019
³R\x0006vz\x00154ó;úÊâ©:JÕ¸çgW/þãj«	V·ó J9Ò\x0007|'Ê¼ÅVÓ\x0007kÌÁª¦T#(Ê-\x0001"¥Ï;mJ\x0018\x001aëë¦#\x001aÑ@Ä:1B\x000cYã\x000b¥kdßPJ[SÚá8@e-¯öÔ2;àé®¦t#Ö2Ar;±ëu\x0014Ýaý&mX#wRúÒXKLåÕ$ ¬eÜýb\x001bÌpuBM\x0019FP\x0006Ëi­Fiö\x0000äcéfØðÚw+o\x0008eôYK@\x000f,+A]\Á5&é`ÌV¤éÑ2¦Ìÿd\x000e#ï°\x0004i\x0001³é0B¨cb&¿¼È4\x0011$¯æ*\x00161ÄF¨Ã\x0008©®p®*aBz¤!LU\x0013Ó)uC©GPb;$
ªÊ4ð0ûº¬,Ì°ú\x0011úGÂÂÇ¼ÅSÑ%MY­
¾&`6ú\x0007F( tÒi1qö\x0010»Ã¡ýtÉ\x000eþ\x0011
(\x0005õyÏ5öQ(Ýv³Æm\x001fÙ( \x0018¡$\x001aå¶¬&95*x_Vs\x0006áÞh \x0018¡¤£&\x0011\x0013CYhÃ7ÈÁtE)\x001b\x001d$Gè ôõYkÏKÙ«\x000e¼dÇq\x000e#tPÔØØ9c\x0002§B(\x001ab\x0013T'\x0013b\x001ceëVPA\x0018¢ 'kÜêåÀ±qäí\x000c
#T\x0010ö\x001a+
[\x001bæø¸cMég°Úe£ä\x0008\x001dYÊª 5¥¢¶A®)e£ä\x0008\x0015$-°l7SQ,Û½Y\x0013È\x0018JÙh 9F\x0003ý_¬e£ä\x0018
$¡\x0018ÄQÊ;ÝI½æ5p0e£ä\x0018\x0005\x0004¾YbG
'rñÞç¥Á\x0002c\x0014\x00109.§E¥@Q`7MK3]¬«Fû¨1Úçÿb)U£}Ô\x0018í\x0003\x0003\x0008.z@drHÊõÆÕÁéUúQ#Ô\x000f\x0004~2Ã!\x001bôê"¹\x000fSÐv\x0006±®Ú¨Ö\x0018íÏh¼ç\x0013ç¥§¾%¸çÓÍLÕÈu5B®cÊ2\x0015	9SÂ1R\x0019\x0016«ÞµS\x0002\x001díc2\x0006;Ê[ò xgX³*4#\ÒÍáûº.lô2ÆÐÊ Wq\x000f¿O&g0«ì)Ê¨ ÿÀìË­eP9ÒAË6;G:\x0014ÇýS3óåÖî\x0013\x0005GÖ8²'Òì\x001b#(ÐÆ«$ÃÓUêÉ¢j\x0016Õ\x0005;k¨YE]\x0017´ò\x001c2WB>	ì÷ÄÑ5î»S3¬\x000eè\x001aäÕá(\x000cOß\x0019zâØ\x001aÇöÄ\x0011°J °\x0018ßÉ®3Ë4-õÆá¸\x001aÇõÜ¬hà\x001b
%»lÊ\x0003<è'"¶'N¨qBO\x001c\x0013¨ÛxI¯d"3ÌÓ\x0018M?*\x0002w\ô¤q4\x0000\x0012q$èu{s\x0016GOVäô92z`.¹7\x001c¶TZ³\x0003.FÚzò42\x0007z
\x001dÌè",%ÐnY`çPÊ'Áª<Ü¾Gr\x0003PÁN\x0014É¦<û?µ½zò4\x0007zJ¿g¢¹E\x001eYíÖSw¯'M#w §àÚ]ABÊØ¼\x001d»:ÍM¾W]¹#\x0015BÉRåí\
T Ë¨:\x001b\x0005ºÀítûßÿúïÅãû-å´Ö¢ÙI½$LÊØHu=å©\x0012 ´iÂ§X ùöðärïxoqõòhÓä×
RÕÝÉ£Ï\x0005R×Ýñ¢Ï\x0005ÒÔÝ\x0019¢Ï\x0005ÒÖÝA¡} ½bU$Âþ©ÀËó\x0015>°ï,9ì ]
Ù\x0006ú\VÒ×ÝÏ\x0004²\x001b	òÉ\ÌçBÙ\x0008Ê'Ã/\x000be#àJ!h.8¸á\x0018Õâ\x001b5Ð	2\x0000Õù\x0006¡ÛD£1\x0017\x001c»\x0003Ïóò@y\x0002¢cÙ\x001dÞ\x0003Óä2úé\x000c¾`$LÉÁBèv\x0017\x0018¼¥w+ë\4x9\x0003;*\x0018n
è<?V1£¥:>wæ:ý \x000fÚl.J\x000edZBÎ\x0006µøÆÐËØÛÕÞÁæ9Q\x0015­lo¤Ü\x001b°[\x0002$WÑ 5é}|äû#}®ÿq|Î¢ßÃ6¾y\x001aFí	T{¬Mø."¹*þ°\x0001"×ÙØ7Ù-\x001auÑÈëûÇ]~"\x001f%]¬(ådk^\x0018pªåÕ¦¡\x0015R¨Bo¤è\x000c¹Y#ÙSd ½&³f7P·\x0010PÖ\x0007·÷\x001f~¾ÞÊ\x001dÛ8CÅ\x0014÷5D\x001a\x001dÖ-ÓÁñéÁ\x000f\x001bÇV`²\x0006À<§9c¡º¢t)!ø«µû×\x001bL×`z\x0000\x0018¶:Pìa;jJ\x001cÁ\x000cË(%×õ`ºðø\x0007ð\x0007÷ß®÷Î¿^owµå~n>r]ÉX4\x001c\x001cîä^\x001f^\x001eî-Þ\x001dVu¦OX~üé	ÍO}q\x0002ÇE03"tÉqTÚoÀ)K´*Íèf«fJñéÃçëåÖ¶*Rkjðb¬.º9.NI#YSÖvx±wzþöpqõÛvÍtwÍÐ®\x0019×¿,ólàmÅ?ä§Sû\ÐÂQ\x0012½.)ýbïüðíY
¼Y\x001b3]½÷q\x0010 â,\x0002&Læè:ëe-ÖTqÕ×OÉîÖÊjjÙãÞñò×û­B õS\x0001q\x001a³æ Ñ­«½ãÅ»Ó£Í\x0017ò}´\x0018\x0010Í²°&ÍóÒ­\x001f[ì,gJ¶M4\x0011\x0014å«`K¯EÛió´Æký°¸ÚÜ#  (êÙ®\x0011½©Bà¬}\x000b9Ï\x0006°_Qukô{Q¥\x000bêÜÊ½pi\x0010Ù\x0003!Ãæør2Rn¿è¼ÁþG©ÝP~»g+´§ëåé9Î Ã¶ø»@C:!ü+R/ü WLá\x0005N1;¼{÷øËãÍ¶6j^\x0004Á]RÃ×t\x000b-¾\x0004·\x0016Ú
ùÃ¸wWÿqµ¥;HAR
êä\x0002N\x001dÉÍÎ=öhÊH:Q\x0013\x000fSûÓ\x001f	´¨ð×ÞË\x00145$6Pµ¥O2¶·\x001eÅTùÄÅ|O(Íý½qò(½êÄ3FæÇ&d¡ M\x000c\x0016«#O\x0018¨+"ÓÁrKÿä]eÚªÀ/ÉZhÔ¯ºCs°ØÜ·¤ÈDö 1Æs¨ðös¯Sí¨uc´¯Ý\x0018\x0010Õ¨Ý :\x0004®\x0015çB!Ò9&\x0001Ù>
ì&IÕtf%\x0012q\x000c]üW÷ó\x0000¢Ç½wÛG	\x0018p4Ë8Ì7Ë2Hò|F
²ízúêôm\x001e>tµ÷në@\x0002ç\x001b8?\x0004.M/ËÈÇ	è>/Ôÿ3Y\x0007ãèd\x001a:\x001dVç:\x001a!\x001fë7\x0011okDË¨òòs\x0002RHË®xD÷D½¹\Û´[â\x0001P5\x000fþÚ\x0007Èaßú\x001al²Á\x00172îê
í<%ë2ó`Úe/\x001e\x001c\x000cO<Ö¡¤D\x001e\x000c§\x0011u]ñ¸\x001bH§ã´²¢NÀ(Ä\x000fËÏÉÂìÓø0:Ç>7qu8%7wt\x0007êá
8\x001b§¦úañ6Y;\x001f2\x00155\x001cvd\x001c\x0002\x0017%Ém*\x0001K\x0019)r0!Ò¹¶¶{8\x001d4t0Îò\Ô32w¯6à%ÓÙp²Ãà\x000cX¢TSvEÜWÏ2¬Í®\x0018\x000e§\x001a85ðÐ\x0019
Ù:/0¨ØØÈÿ±¶Àp8ÝÀéAp>ú\Ô5\x0017;Èg§Ë\x0008=\x0017éLk\x000e¥\x0003h\x000e\x001dþ:lc\x001dEÖ(æ\x0000«\x001e7V\x00199
Ïµxnà¥`1\x0017ñ<5#"ð¥ÐbÒÞjn\x0005þ:\x0000ÏáxÙ@×BJJöªdy×F·\x0006Ò5*Êâd©\x000e\x0012xZ¹E\x000b!\x0003ÁS\x001bZááqxÙßw«\x0011\x0017\x000eÍ³\x001bl\x0019¹w¶|¼Ýb\x0011á¬ï<\x0003ÅáwGFGðÜIZ´%©gGØ5rïlqu¼É4LæY0ÙÉöe²¥>ÒÅvZ²ï©×h<úí»^O¤tîEµu:Ï{fÇY´:¶\x0001i+VÓ¸k\x0005fÿYfëegÑèØÛ}V+\x0014ÿû³\x0011t±¼ýã¶Å³¢õJeeÑ/\x0014¸T¹Ã\x0002\x000eA·
=â\ì0Z375Nü­\x0017\x000e\x0018Áï'\x001e\x0004¿pJÐDf:ImýqÕñýVÇ¸YÆaHA\x0015Õh\x0019Òs\x0013~Ôê\x000c5\x000eþÚsyøÁËãTnZ\x001dÉ\x001dlÖ]8:©g·ÂÑúË\x001dtqHgÎ\x0017ÿßÿúïÃÏ7ß¶ç\x0003æDâE\x0003lêËé:;ÝjÁãÅ\x001e\x000eëÌ\x0019ã{ço.7yøðãOýËýý/\x0014\x001f¥~ \x0007?/¿]'GV\x0012\x0012¼®Ú¿}¼þ·W4W\x0004ÿ·Hi±mÀç\x0000+#¤J\x0003c±'²5yL,àäd6$)æwðÃâò0º·ë£
Yi\x0010:,D£Ke°(9­Ì`.?\x001b"XÉ-\x001d\x0001F­ÆÇiûÒã¾:¼Hæ¨`!y\x0011ÆE©`F\x0001]I´c}~Z3µ¬¸o#Èâ=r£É¤Î÷,ÍYOrÉ\x001f2\x000cg&S\x0002kNLå\x000bà\x000eÌ&C³\x0019FßÍ\x0010\x0001xÍ,¯`Ìñd8ÉlüÝö½\x0008$5Ò\x0003lBS¯@(³¼F aÃåñwÀØ"Ð¢Ü ;\x0010ÑØ\x00189ÑÍñw\x0000û÷ÈL¦\x0001MèDf²@K£Á°Ëûø+Q\x001f\x0006KÃ\x0003\x0013Í-lÂAÃl)9þ
à\CÚM\x0003yN=Ö\x0000£ÁíÄ3*Çß\x0001läGjÀ*|ÏNh^ñ~J9^AáT×P\x0018\x0010¦U\x000b\x0018hC}®\x0013h\x001aJÛ¯·â¯û[¥;ßÝ,o_·R\x0005ÿâìaù\x0011ç\x0013~ý·ë»ÿÿ\x000eÀ Ät\x000e]4;¤D:¯V5Ý»£ÅñbÓ31üøË{wóþ·Ú\x0010ªrÞrißÁýçÏË»×\x000f©»mßeÔ*^\x0006Õ)v¬ËÏJr@z¯Û+[%Ãå¢¿Ó·o\x0017'¯\x000eÏ76Àmøiâlü8\x0008Ó\x0012¿Å'Ä¯DáW³âçùâß+>\x001eºnìóçopÿEÔ§\x001fy\x001f¿~H\x0013%®¿}\x001bã\x0003ó£4\x0001\x000cÖ\x0002&Á¡s¸\x0002\x0014VÚ"ãÕÅA3qxyÙ\x000b|	Ñ½d³aü\x0004ÛâÊF_0W=zÇc\x001dþÜ1É(©©Ó*b:¬oOL¦\x0019ôdN2Ñ÷r¦r¼ôc\x0012(N¤²2ZÀ\x001e5\x0008
.7° AÂTRLÃH?¦Ý÷hùAÖpè¡)I"R°vúÏ¥÷/r½ý´\x0013 B\x001eeOªç\x0003ãé¤ªq¸??Z÷\x0015*1Êùo\x0011öáÛòv»¡Ó©XJ[H#ãP\x0007$gW\x00167ÜÆÀá¸Èy~¹8ÞlêTÙTD90ò32ËúI^ìSDC\x0004ºJ\x0006M3tJMÌöì\x0014È­%óRz/é\\x001aë\x0004_#\x0019äTÊ¬¦-¥ãcr¡
ì\x001aû0\x00152k£INåäè\x001atK\x0013$UÜ£/j&Ê¬¦Þp¡ïçèXJ_|?º\x001c:ir¢Äé²,Þ1VÎ~`8\x001a5Óö&2Åëc\x000c¦wäK\x000e|}¼\x0014¹&0UNÄÆ[æ6åû\x0013RÁTQÄai²ÈäÌH\x0003\x001aH¬»¢Òª|8¤3
Óå9
\x00193.bÆ´À~*%Ew¦Q<0SR<rï\x0013äT¹õ râý	²Xq>¤¹9-ÙkÓÂLÅgfÕ»ïjI*fè0ÓbTØ\x0010\x001eÛ\x000ffäé² &p*ÛÅªêC5\x0016ÖãÁ¬ØaeÉ©ò¸2ù2É°Q$O§\x0015åNYXI{Å§\x0015Äd9J.GÓãëy	ýß?¸¯¿×¦üâ×ë;â\x001c\x001bZ5!D/}\x000e­:óB#mô\x0004VTÂ_¼;<!â\x001dQÖ7ÛËÏWìç/Õú\x001e}þý_ö^ÇÍýõæ\x001a½Ï¡\x0016\x001fÇ¡`\x001eútìhÙ\x0008£·gØ\x001bfïuüÃ»£Cô?û°æµÊÓ5YKò øL\x0006Ü\x000c¨ñsíw*³8I\x001aÌHìRö\x0014\x0011\x0003!+¯G#ßß~üë]\x001døã\x001f¿<þ6$D""SJm.\x0018$\x0010ÏÛÜ\x0008\x001dtè*®Ãÿ¸úS\x001f rå\x000f\x0010¹í :l©§t\x001eÿ5\x0003\x0005ç\x0018\x0008Úw»Þ@ä¡?\x0015"oüù\x0000ãýlý|(-ã\x0019\x0011±ÿ|Ø>Dì·ÿþòeùùïjýqÿËãõÝ\x001fÿø\x0014M¯áö\x0019Z7TU*Siòu´Ê²yf\x0000ÚóÓÿ¸:<9|³xµYÇýõñïßnëHûÁòãýãòvùè-MlÊî§\x0018pû	Òi\x0016ï`ñêôjq¼\x0011íñË­~ÿ¾B{\x0015ÿ©\x0014¸ïrÝ³íöuzBÅLÁ¼f`mñW§'Û*+ªTp~á8Ý.¥«Ä¥ò8­\x000b¹4õU\x0005À²ø\\x001eãA~ìza7Ü¼^Ê\x0008
^H#óG\x0000§\x001aË?þ\x0018·f_¸Ì;¿æ}tµa\x0017\x000f\x001f®¿lAÂ \x0014þ\x0018·T2gKlÂ» çÉG&gôØ¥Â|#ü1K;k¥\x0003Åòâe\x000bÛ\x0014Ê!\\x0018\x001eÃ\x001f£¸LÀ±~|´Ì\Ær´ÜX.áQ\ÑëMEèy½4\x001d-Kaùáë%?ÝüýýOÈµéÇñrïõÃòæë×»ë\x001d²¿¥CO&ÊÎôÈ½E¢Ã\x001aù\x001cñÐ¾\x000cðú|qtqqtrøjÃñg¼N|n\x0002¢¤qiÒwÓeDM\x0011$\x0015ºÏë;\x0011úhÜ\x0017ÕdÓÝ;ºÍUÎ}¹Pn_ç`Qð\x000e\ôa)X$U'!ðb\x000fÝÁH\x00176
ÉÚÜ¯\x001e,\x0016
&$~\x0001Ê@Ê%cÔan\x0004ÅÕ	¨ø/hNÊ\x000e \x0012??ßÒéÇ}O?¯÷Þ.¿E79J:l¯Ö*{\x0012\x0014NÊ ñªàIÅÁÛÅetî\x0017\x001b/æýÇ\x0007ùí×{?ððËm<ö©qMo6c!W£F«Æi
;èè/äHIAQÁá¿\x001dÇSt¾Î}üU\x0012ív,\x001f?ÞÜÞÞ\x000fÊ7Åî`\x0002ÐÆrE\x0002N\x001b\x0013 \x001b\x001d~²¸z\x00157ôtS\x0004øQÿþ×÷÷ÙèAI?¢¸8[þz7(ZcâAÝ¯°Ö-Ç¢5KÑ\x001a»jÄ²âlñîôd³¬µF~yÿ¡s\x0007"Ú-öF\x0018búc7~õ\x0014%KÈèÜõ#.	®v]\x00126¢½\x000fÿðñoiÑ\x001c.ZÎT?»½\x001frÐ0¨ÍD
pðeM.º7àìøtý­ô\x001f®oÌn,ëfs\x0014cªF/z\x001f9öÎyizkt´òf³\x0004\x001a£\x0013Y0_.?^y
ÿjßÉéÅRÔ±à¸!Fºk¤÷¾À>cWÚ¥¦
bÁ>Q9)ÏE\x0005Ì\x0019£ÁÐÔ\x0001ÖÀl:À\x0015O\x0015»\x001a¶6NâAIk#$½(\x0018l\q´\x001b¾6UØj\x0018K´?sú\x000bÊs§Ê"\x001d\\x0018ÌÒD¬ÁX«¶\x0011F£ù`f\x00183\x001c¦\x000eV
Ü%GÎU1ø*`øb»á\x0017»	S
;ÁBñÍ\x000eÒs-S\x0010|\x001f&@5\x0005{*Z\x0017\x000fN¥DÚò½>0\x0012[r¤\x001fcVó
\x0012p´2¡\x0019X³Q;/·ÄF\x001céÇÄc÷ë\x001c\x001c·F\x000c÷\x0000Bï×xÇ5ïXÊNÍwL\x001f¼ä~\x0014\x0012:¾vÔ¦	\x0019\x0016QmFÌZE 
OÞ7z\x0011¥\x0014\x0010;V(ëP2U¾y.0Ó8Þm\x0014\x00129vÀ¼R Er|ë©Ï5\x0012¸i\x0018Ã\x001fcî½¥l¨¸@3\x0003WD\x0005=X8KLÜN?ÆÐ(.Ð¢óI\x0002h¾fÆº÷\x000e\x0013øc\x0004\x00127ãÁ\x0005²ûDQÑ^f°ù%QT¤\x001fã\x0000Åè\x0011üè\x0019\x0007ä
Ûµ@µG1æ@{òÁ\÷ç½.×Þºö\x000e~\æZY©àY\x0016Eü`\x0005¶º)^#)äSyØ§ð,Ô\x001ai½ÈÞ+û5Å\x0002ñÞã\x000fl\x0010±¼ýéáÿù4Ä\x0013Ä6µTI³³rÜ\x0001,e<¾ã\x0006¾[\x001c¿>?|³!µ\x0002\x000bxß\x0000	,F&±/\x0008Ý@àv.í½ûðkÛ°âÝÍíír\x0010SÊ¿ \x00125Ì$Ó>¦\x0014'JÛ­\x0008~wt|¼x³Ùo®È8Ò6¬\x0002Ø\x0011#Ï\x000c\x001c×*O"+­4ÆYÇÉKQ\x001e`t7'/9NflÅç0°ÒJc\x0014çBeôªy3e	\x001c'­4\x0006V\x001a#7\x00138¤º\x000fÒfëÖÄ\x000f Ë¹Sc×Ú³Ê4*W\x0006Nêç¸\x0011\x000e\x001dMV|º\x0016K!¸1
\x001b¨À-[ü\x0016\x0007\x0003ÈJ1dÞag\x000fn¥¡<¾\x00142ß
lõ'Ã\x0006ÛÔd{\x0004\x001aæësÁKt²8\x001dÖéÒ°BÚñh«þ#£Ð8æ\x001bVÐI³¡t¬h³ó¡Å£\x0000ãem<jZVxà\x0000\x0002^[BëT9\x000cCg\x0001ÆË´`(\x0002e|´~4¡YÐ¯Æßª7Ê¨k`÷³´Å\|N¼\x000eÁÜíäêùq'Í¦>\x0010¹\x000e5ÍÎ­QX§[3^
T½QÆEq\x0003\x000e\x0006oª§J¯À\x0007
ÆËÚª3Ê\x00180#WQ$¾¿ç>7²((èö-\x001avÐèËm]-Ë
QêQ\x0014@\x001bão\x0000W¢ÝÎ@¡slØUu{âì]?á\x000eÈôê2\x001aM©Uy¦e#Í0ÉG\x0019¦9¢Ðè\x0015ÍÁª{×&q\x0003Ð0P1þ~jSÎ\x001avò¢·\x0010|×fõ9þ¬©¨ÕÕxÍn4¥àµdãÖ)ÍÉí Ó0´¸àj¼ð¨mH\x0013ß¨ÏGéø¤Ç_\x0003Toj¬ðÐñ:O\x001dÄUWQÒ&ËÈ	hñ\x0006©Ñ=\x0004Aîp\x0014¹­HçJÕïjüö\x0008´¨HÔhÍ}²®1´Ý¹^
¦lhü*5^äb	Ö\x0006éAº±¿\x0002b¼ðÀò 5^äÚ{æîbt\x000bÌJWî8¯MOX3W<)É~Xj^t\x0019³\x001cÌx]\x0000±F*I2<w5
F¿\x0004hæ	¶\x001aPÇP\x001bÏ\1ÕJÇÐNµû 2l»oÇË[4¨\x0015T\x0000~×ÃL\x001e^´6Éu\x0018Zµv¼±¦=Û6:Ë]&\x001d·\x0001Ñz¼í|vtØ
'\x0005q\x0015+và\x001e*ÒëaXQ\x0005ØñjÀ\x0008LÔOdQ
P\x0005X´>¸/§ô\x0013V,Þk;^
\x0018ËÖ5\x001eÇ\x001bÉ¶/§à\x0016côÒ¿^çÉ²yÕ¨Ò9ÐeÕÆû+ø¨äÆ\x001bj¸:i,lC(Gm¼á.nüQsr_\x0016Æª3þÂwÓW\x0018¿t\x0013NZà6\x0013(Ñ¨=³Ó D\x001b¯¡ðÍ"ÝN- Õçò% aësþ\x001cÐðé<ÝN¾`U;j9!È²îìf.\x000f@K¥8éÇXãÖò\x001b\x0001ì `\x001f¾o\x0012\x001dÖ\x0000ÃÊéÇÈuCj\x000eJ"\x0007ËÍéÑ7\x00140°~dS/BTN%@Aé\x001f=Þ¼MsM\x0000Æ¯1\\x001f¶¡ÇN\x0013ø&'}`û³É\x0014À\x001dïçyà\x0014p\x0007]P\x001f\x0000ñã¯iw\x0005££D)]\x0016\x0008%q¯z.Pã÷\x0014c\x001d0:àÓ%ÙþN\x0001\x000f:n¾\x0004\x0015Æ?\x0017\x0000zR0ÚÒÂYª\x001cÂ_cÛü¶®§7ÞÄq\x0017/Òl\x00168\x001be\x001asa^hiÜ­9\x0018ÀÏ§éÇ86­U\x001e¢WQú¼MC¬I¼ñW\x0001GL¤\x001f#Ù¤Ú÷dìzEµ]V\x0001\x0014woÂyÃ¹ÊéÇH6}Òó\x0018ÏÊÉ%QQ±\x001d®Æû{\x000e2ö5Ä«@;ê4µ\x000f²ÑæâÐ\x001aíî¥\x0016¼0ÚIÖ\x0012$[G®Ô[â<I==ê\x0001Xy~\5/8,i±§£t¡rÖÌø³þ\x001evúRóYmVYÉÐ¬b5/Âø-E\x000fF{}8í\x001fCmt\x0000sCul=;×\x0003_¤\x001fc[iúe­Ìõ$V¬zNª'Mòû£a6tú1ò´E\x0002>møPUB´sY~`~êH6	\x0001rBV@vÍ¤\x0019kä]Ñióf¼¶Þ\x001dÇÇ²\x001c°q\x0014¯&'?F§Ð°ßh4|w\x001c\x0015\x0010¢Ð ¦Ñ$¢NÖ8¥N·ã\x0015©Lúäø·w\x001bò3ôý\x0014	(K\x0004\x0007´ô\x00146|\x0014\x001dÿ*ê£bÙÚ}
*[\x0002 z´lø¦!'<lg\x001d/Óëmà¨ðªLå
Ú;$6Xµã.ÏÞ
JmÏä
Lr"©+4NÏoÉå\x001b\x001f¢(\x0015åø·
Wx\x001bíK*wt\x0013Íu\x0013^\x0007±á;·\x001eý¸áEê\x0004(m\x001f1SØ¼\x001b­®$Úlr¼á\x0006Øs8ãÒ#|\x0008mJû¤8³/[[Ï=\x000eÎqL\G	"ò8¥3fèÂß¾ù-e ãºá\x000fäºþéay÷aPy2\x0018áxZ\x001bL-Y\x001c·Ç4\x0007H$;|}¾89ØR üøù¡y8«\x0001ãz4Ëb¼\x0005\x0003¢r:g\x001fÙn¦ê.ÙóÇ6ë«|2)\x001aFìúnäm\x0018\x001d§§ã6ÜÚó3©Õ¥¿µèFî\x0007Ñ­íÆöµ6TrU«ÀÒã\x0018v_\x0018W¦ÄÓ\x001b±b: ðM4¢J>à·®5²]0$ãó(¹\x0013<îG<\x0019Fãu;Xm
ËZôXãÙ\x000eÂ
\x0006üéÓòëM~g#7{úLs^FÈØ»r+å^YB§\x0014¤T\x0013Ïe*êÒÁz.\x000fjG¼½:}KC^FâWØÁª:ÒOýûßïqO\x001b»|DÚ\x0011\x001d\x0011`_Ñ@ÅB¦T)tTÈ«½UG§h"~/IçÕ\x001fx°ÇÙÍõ7ìÛ3è8
´äöE%9¹ ëö`#à³£ÃKlÝ³±áX5¤|¦ºÔ\x0013 £6+\x0018	À÷êüHÍ¾S&Ðr)mö{U\x0016ipÇ÷7_÷\x0016w®o\x001dÖ¦Ï§Çôì\x001bJ\x0014
_\x0014£;ÞÍj×ñéÕÑÅÞâäÍáñ»Íû
¾¬ñåw¯j|5\x0017¾\x000b¶nl`-ï=¿bùnKªñøºÆ×ßÝê\x001aß|wø¶Æ·3áKlb­hÏ+\x001c]%>=Î\x001aÙ¿¨ìMü®æwßÝò\x001a?|oø \x001aÁ/fâ\x0007S&"ê!>Ëª¥Û<Äq «¸æÒ\ <\x001dy\x000e\x0006ix\x0003D03}@£º`.Ý\x0005º\x0014\x0018\x0015Ê\x0006X¶îeÇ?\x001e}¡þ0ø xÀ¸ÁA-YþÈbíì¹\x0001ø£Ú2]S×äî¿ß®÷>>îE½ëÇi§`,ÌQ0]NgüøùéÕåáÞ««½³ø½Ã«×ÛLJÓµ{M²{'\x0011ûxThVvÅêÛ¤k\x001d5¼ÙØ\x0004«jX5}yË±ö\x000b¦\x0010Qu\x0008ÓºNç¬\x0011Ë«kb=yyÃGöDl<6tÉËËÃ\x001aî´'\x001aAljb3yæØ\x000eCÍ\x000e3ªè\x0008ÉGØÖÄv*±
¥0GyÇâ:Ê\x0010R7Öw\x0013 v5±¼ÆRíSà7\x0008væ°Á'\x001fck§\x0002û\x001aØO^b\x0005<\x0014/úËT\x0005«4?ØÎ³Í\x0018àP\x0003É+\x001c-XU\x0004÷\x001c\x0007OP\x0014Û)k\x000eñ\x001dbhÝdmuÔ'\x0014-¦l§jÃó\x0016ÚR÷1Ä²ÉÚN{ÉÄ9\x0005\x0015Í¢Ô\x0010e"p£ð`²Æ3ZâQÈÄüÊ,¹*Xb³Ö©ÄÂÉ\x001a\x000f\x0006Ôôp\x0014×ë^mzjÜh<¬ò\x00109¬i`.pP:"OÕxÐh<¬ò\x0014ÑØPö\x0011l\x0007EàÉ7¯Ñx0Yå\x0019(3je\x0014o\x0014Àb©qÛDäFÀd\x001d²\x0014\x0005Q²\x000cÝR\x0018dåäsAó\x000c\x001b\x001b9Mß¦ü´¡iMÑ¾ð¬J\x001c\x001e
ö¿'\x001fhèG4Ü-v\x0006\x0004Ås{¸àbªè\x0010¾ËígÁÆÚ8ìr°(Ûíý7ûÛõCËjÖY~úÿÎÝ·Ty©Ævf%ßbgXñº"\x0017ºË­gÀvÑ¦ÂQ½\x0012)ºÔ(»î\x0008ß1t\x0017<Ì\x0000ý>©év+K­åâ¬êÇFÒ9âQ¤ÌpÆ¢æF­j(-wÓMö\x0004\x0008qC\x001bç¨afR?	!9ÓÖÊ]ÜO#3Á§ÑUàþ¯j6éÁýÃû?þçaÇ|õó¯¢A)©ÊYÅÞ-\x0008E\x0007Úúä{/^\x001dâ½Ã\x0013ìXÏ)=8=ytx~¸aTiý\x0019²þ\x000c9çgx\x001e\x001cä¬pT)\x0001Âóã¿µè@Íõ\x0019ªþ\x000c5çgDûo8¢ÊA¦¶¹ûóL_¡ë¯Ð3~Ô@M'ñ\x001cF\x0003°|¤´
ó}©¿ÂÌù\x0015x\x0014\x001d©@Yà\x0000ìâÇ#úîÌô\x0019®þ\x000c7ëÍ04àÎ¡½=<\x0010AònXïæûPFs7¢ÅCS\x000fLàÈ7ç.äV'ßzÏVÜÎ)o%\x0006äò©2Xðl!À1Oô\x001d*]é;\x001ay\x000bs
\4är³\x0003gPheI%¢6Ã\x0016ì|·\x0003\x001a\x000bsJ\%\x0005ßrã\x0004Å\x001e\x0001Ó\x0019é;Òl¶¹¾£\x0011¹0§Ìn\x0000yìq?$Ë\\x0019æýó©\x000eh.Ì)uÑØÙ;G bXôËR\x0017R*ÌLßaï°ßí~4Ú\x0003æT\x001fÊro«ø\x001d\x000crPTx\x0017?CÏø\x0019¾ù\x000c?çg\x0014óÜa6g\x0002¿#5Në;\x001a-\x0008sªAå¨X(î\x0006Ð5\x000e\x0018e\x0003\x0011RªÀ<Ùµ.fü\x000c# H+Kã2@q\x00156y@ÎLßÑhs9§6W{3Æc\x0015Ø{RªX%"ÌgÈÖ{SkðÔ\x000bÜa\x0006ÏF¢rü\x001d&Ì(­d£ÍåÚ\\x000b(ß¡)\x0005\x001cÏ+ûaæs=d£ÍåÚ<zH8ó3}Gîü\x000cZðÝpýÔÖ l´¸Sk0û,mE¶'u W2ß64J\Î©ÄuÔÜ*ð6°;®eµ\x00153\x001e§FË9¸Î,n¹K\x000e¨Às\x0006
>ìÌö\x001d\x0016sjñ\x0008ÁÌ¼\x001f\x001a§*\x0019Ú\x000e=ãv4J\Î©Ä5Z +ik\x000c]p\x001e®\x0013Ëçú\x000cÕ(q5«\x0012·¾*¡©Y,hMõÞÚØ0ë¤\x001a%®æTâÑçÎÉ÷ñPyJ\x0006ÍcgQõ©F«YU8VßI%\x0014ý»\x0001¦ìÆ|Ñ\x0006@gÕàNñ\x0018¬è.QM\ü\x000cj¦±­î|ßÑhp5«\x0006wjÀ£Prû*[TÚ(UVÍxÉ\x001bM®fÕäÎRÏöx¬\x0002
"ø+\x0015¨gÜF«YU¹·¬:tá\x001d¶pg\x0015º*W³ªrÌ~!isUÈ$1\x001ex?Ä|¦jT¹U\x0007.Íu\x001a\x0013èòg¸¢Êq;\x001aU®æTå&\x001aº¹BÖ¥ÔÅìpàNþ\x0019\x001f	t£Ëõº\x001cem~1Æ\x0016ù8ä+\x0007Ï¯4¹\x001dÏLßÑèr=§.7\x0010°§Eþ\x000eÉ6Fð-ÏÃngúFë99Z·\x0014F\x0001LQé(¸øXéù,+Ý(s=§27²ÙD}»Lb³
¾åÚÍø\x001dí{æÊÜÍM\x001d'äu\x0004Fi¿ó}E£Êõª\x001c]?
åjWb FB¹\x001c3>õëFë9U9F\x000cIsXÁ1\x001e#¨RbFÛhr=§&ÇZ/ ;gåïà\x0001½FÍøò¤\x001bM®çÔä¸\x001dzµ\x001fôÒa¸$\x001f÷c>\x000bQ7ª\ÏªÊµ 	]\x000e=[EªCr®f\x0014V¦QåfVU®5;QmÓB0Å3>FY59\x000e\x001eàÏ°4\x0003°À¿ÃÎ§ÊM£ÊÍ¬ªÜ\x0002MûæU´oY/¾`\x001a]nfÕåQexrh5·à\x0004cy;æ|5*7³ªò¨ÀÙ²B}HÇÊñ»¬\x00113ÆIL4«2w\x000eiòvHÞ
e `Ü\x000f=ã5o¹S§¤æüÞ¯|É²²_l´ó7ÚÜÌªÍ}
Våså©\x0010\x0013/\x0007Ìh\F\x000bYµ`0×£¥ÇY\x000eé;¸ò#Þ\x0019_m£>ìê\x0003;-ñý\x001a+CÒ¹ÂPY>WÁÏ'vm#víb×
²ØÁÓ4¨/8ÉJ\x0019¶\x0011VvNaeu/.y\x0000\x000eZ+=_r?°²Íå°s^\x000e'm\x0012e-¶Äïpå3tQµåe6õ\x0018k¬C1§}\x0018MZö;l<TyÔ\x0008ÄÿÕÀIÆ3¦\x0018s®ý*Í\x0018ÿ0_6¥3XÉ³÷lÉ¦\x0014\x001c'±JÍ¨=|ùs×ûÊ\x0015¡%É%ôJý\x0013Öªôd¯;ë×`jeIu\x0005Î«ä<WéçÓ#«*GtÞoÁ\x0006>h\x0013dâ\x0001g4Ì\x001atxzmæ>h`iæEh	¡8Ð|[#d÷[äÌ"\x0000\x001cgÄ\x0005Ëª\x0005\x0007jÓÆ\x0019ßC¢\x0004 ¢§J\x0002à_¾Kç]û'ÇÌÏ|ÌþÙ:\x0003?¾ÿë?Ö½^\x0002¦n¼xñæay÷ñzï`y7¢#æâÑÏRÔe²\x0014ò\x0007ÝÎMxs¾8yu¸w°8ÙÞÂ±°ÊUNcÜÙÞ2¦Îrïç\x0010«I¬ªfUÓXmMÓá>\x0018µaäå`V]³êg \x0019¾\x0014F;ûBk?m]MÍj÷yu5«{Þ¬¡f
Ï\x0015Zõ\x0016;%åÀ&§d,pÜ\x0014\x0003å`Y Êý²ÓdAÝót\x0002þá\x0019®0f(4*,§,¼xqðóõç;ì\x0018_n7_o\x001e\x0010{åÉlÅ)ÑhçfeiÛ\x001añàÃ·G'Ø\x0016\x001bÿ§/ÎwcË\x001a[Î\x000bMý=\x0017\x0001\x0019+|á\x0003[ÕØj\x0006le÷4¸P#\x001dÍiîï-ÚV#¹uÍ­çàv(¢Ý ¹#\x0001z¦WX
;\x0003·­¹í,Ü<
ÝYÍ\x001aÚà\x0004[Âs\x001c\x0013_cû9°m\x0019\x000fã¢\x0010´ÜÜõ_H=\x0003vÕð\x000ceÛHî?FþåFx*%P"ÌÀÝÊÀ9 Ó²Ì\x0003´J¦\x001c/¸\x0003¼0\x0018Ä\x001f@\x0003d\x001dû¶qÁ\x0005ßKÕN¦\x001c	ÞÈAC\x0010¦¡Ô\x0004\x001e¸ÈÙ('Ê \x0003¥g\x0000w
¸\x0003\x001c\x001b\x0011f\x0007Å+Ã\x00139\x0014\x001f\x0014¯gUã+Ä\x000es`Àqk	»+\x0000¾ÎÌ@-{)ç¸ÿ\x0017Ô­iò½\ÊÊØNàÙØ.£â!}©ì~®+Ã\x0001YdT\x001ewrsfæþñ§'ä?}\x0017g¥ÓÝ-ÙøéÖ¬\x0010eµÖB\x001fæ¡Ñb\x000eßélYðÿÙ\x0007Þï¹QyöJjÆôx÷íæv\x0000°\x0006 7Év ©¼Ê\x0004ÁçÜµ\x001b\x001c¾:1]\\x001e\x001dï\x00065¨\x0006*¹,fígJî
\x0019\;üi(¦ª1Õ\x0014L\x0010
\x0013Â3¦D2\x0002Ï\x001c¼BjjR3\x0014`5i\x000eÊÎËBjü¹;CHmMj§m}5+µXH¡ÌÖÓÔÕ nÚ\x001a\x001e¡f½á\x001eùA)y\x00185\x0005Ô× ~\x001a¨å6\x0016ýÂ@ <Æ"hñd2Ô\x0010ÒPI¤ÒñÀ
\x0001ñ¬\x000fÒs\x0014ÜN ­<?¤b\x001aª.\x0003`mis\x001d´*¨VOAmþ$©\x000f:pïek\x0004u3Ái¾R\x0012¦ÈShÄ>Lû\x0011{\x0005Z+¸W`àº¸ªbÊíFôÃ4Ù«J\x0001DcpôtwUí\x0014Zµ³FT=
Õñ¨LÌ7²
ü¸\x0004aÞFMÁ4=\x0015ýc\x0012\x0000\x001a¸\x001ftðej·¯è@ÒFMÁ$=ÉBQuMãJ$\x0016ÎÛ\x001bÚ(*¦©¬*\x0002@aÕ!ýOó&Ç£6ª
¦éªÊó\x0001K\x0003\x0000\x0013JX\x001eó&6ª
¦é*\x000f`°5kv½¬À\x0003J÷_OÙÙè*9MWE\x0005\x0005<H]\x0001Í<ØÚ\x00077EþËFUÉiª
[PÅ~È¼ý¦ìÿ$­*[\x000feª²¾ì?¤É\x0019Õóp-\x001f&­j£ªä4U\x0015Ý>M«
µX¡Ê 6?í\x00004ªJNSUèøTÅá}t«$\x000fò¾\x0008\x000cEmT¦ªÝ'S%úÒÖT®¶\x0012h£©ä4M\x0015\x001co¥«ÖTiÍ¨0IR5JNÒT2zÑÊ\x0015¥*h`
ÅR1Nj£©ä$M¥Ûq\x0018lÛÿYpOª\x0011DU£ªä$U%qâÊêRi:«õwÛ0RÕÈ5IþKé÷\x001d\x001fUOµ	V8YÆ\x0003O²ÿT\x001bú$T¥â6&\x0008H¾j6åV©)û¯\x001aI¥&I*©\x0003\x001bÕñþÓõ¯\x0014\x0015LÚþæú«i×ßX\x001e\x0002\x001e/=9Õ\x0016°ª'£ºIBU7'UO;©Q¨jºþÞÒÈh\x0008p?~o'(ªæ\x0003Céc¬Âþ¤\x0004Óûò\x0011Òñ\x0011PaY-e\x0013`Ï¦U\x001a\x001c0^g9W¼kÁÓ\x000e¬àAmÑ\x000c"\x0007¤}\x0002l'\x0002K©°åL>\x000f[a-K.k'\x0005­C3T"\x0005ÚÒLñ+¬Ê|+\x000c`92µM	_ª	Àç.>Â?M
y1]\x00141Æ^\x0012nîÉpSOD4\x0010hú±µE\x0005	Øp|Hm\x000b\x000fmFZ`;!ÂN;
R\x0000\x0015iæ\x0010&ÃY±íºmîó\x0015¤ç«³Ûå\x0007L¡ß»ýßÿúïÅÝë»»ë½·ËáiüøRbEÎ\x0008ö\x0015mÞ}v¼8ÀÔù½ã½ÅÉÁÑáÉÉáÞÛÅÑùÑ¶ôCè¾lAzÙí\x001b\x001c5¥\x0007¤\x0010è\x001bJ¼ÃºÙ¾AÕß æÜ\x0007ÉoçB`!g³w\x0011:3Ö§|®?AÏ¹
3Ú£©¹O	·,ºCk\x001eoùí\x0017ÁÔôfFzÕEO{§þ9j§\x0017×¿MÍ²þ¶þ\x0002;ïU¦ÙF\x000eÂ>\x001d!S²½ë\x0016@saÎ«l5UÇoèÅä{àø\x001e8Û÷\x0018íüæ\x001eÀ\x0017Á§\x001bÍ.G¥
ÅéYnB;t/©\x0005üÃ|×¹ÌÁD$Y3ðÈ©(Ôä­0ÝÄt\x0012ÓÏ\x001eî?_ß-?¦ï8¿ù´\x001c¢ã!ò\x001c©ÇFg¹¬\x001dË2¸\x000b­Ù{v~úöðdñ*Á\x001f½Yl5tº)é&¥¤O\x0005Öl7àÆPN=I\x001fçµJ¬kb=Ø\x0001çKa{Û`ùpð\x00048#'¯±­íô5e´½çÆ¯ã÷®5ÔÇ\x0000û\x001aØO\x0006öª^\x0007Ïµ\x0015ÎI^bz&êüÃ=#$Øô\x000fw(¶\x0013\x001f\x001f\x0003Ü\;åÞåu\x0006#\x0011X)Ûbò)æÞÁ÷pñ ¹x0ýæý\x001f 7W\x000f¦Þ=-47æ7\x0012$#{Í/è©Þ\x0014ä66Å\x0019¸S¡\x0005+liM¤$h©I\x0015Sï_ëß§;lrÃð\x001cT©Êj;W¦Ak\x0003cÈsÙ¹YY\x0018ô\x0007Nÿ|õpóm»M´±¿/Ó$O\x0005Oã¹òÜ¯\x001f¤\þóÓ£Ë
6QM¬jb5X
r\x000eÒL\x0000êÊb.\x0013qÖÊ\x000f\x000165°\x000e\x001cm")áJ¯jAXÛ\x0010n\x0017q:¹º\x001bTÑ«àë¯)ùëÞq<7×\x000fÛ;\x0013<Ñ(f\x0016\x0018\x000bªþØô\x001fÆ#<þáb\x000fÿttx¾¹\x0019A!5¹ÜÉ¸Vº\x00120£Û!<Í\x001a\x001cA®jr5\x0007y\SêþdpÄ,¥»Eï\x001d\x0015!>" ×5¹eÍu`\x001dÿáäW'yT¸ï\x0014¢%75¹gÍEISl=««Hç,ÅÖàv%\x0017%ß8\x001esr
Á³o>\x0007µ«©Ý,Ë\x001d=ZQeôe±be(\x0019}òé3é\x0008r_ûYÖ[Á¾§ÇHin\x0017®¤M§\x0011üáä+£«¤äiè¨8Îs\x0000Ä\x0006öÊ\x0003
³\x0019Ð[-4\x001aòF°³kW%ÀV¬RÀç+Ðh!G
	SD¢Ztg\¨9$\x000b4Â\x001cfæ>ºÓî45ªëoJ¨yúþ3\x0002½\x00110Tô«J!|¸òÔ\x0010Á²êsX-Ð\x0017E¾x\x001fÐogET¿¢æXtÙÈ\x00179|ñ~UM\x0014Y%%ZÎ\x000b¨9V]¶¶â,·Ô;¹/9ÃÌó³w<õ%m{M2Ô\x0008ôæÊyn©8\x000f3s[ü(àK\x001a·\\x001c=\x0002½±¹äLF^ÝR\x001dLò	E!­Éë\x001aÞ\x0008\x001891PñätËÞ\THk'ÆøEM"ùF%ÿ`^òfý\x001bpMQ(NT\x000brÚ\x0007\x0018Ù}	uêÃõ×÷¿}ÃNyBBØ\Ò¬áF7QðpúÄ¤ÅóÃº<<ßút#»/!².W\x001d\x000fL©.\x001eñ\x0015p©!_B1WÕ¼j2¯uå½2.pÖ>Þ\x0015?\x0008«ß§ñêWOçÕpmK¨§·KÝ^P3\x0000ØÔÀf:°Ø_\x0007Ç¼%/b}*ã\x0000\[ãÚÉ¸&Ð`\x000cúP\x000e§lf%Ö×Ý­h7%,É_\x0019QÝtÔÕû.X¡\x0018·1\x001c6	~m.Øµõ5°\x000c¬]
ºØ×^s\x0000±&X27Ô¼a2¯*Ñ\x001dSéì*z]RBL¼jõûl*qÇ\x0002g»ÈEeÍÇK1TôS'2huÛtå¦JÓç\x001cKã\x0008¡'\x001e`h\x001bL×nÒÓp\x0010|Ü§±ôÆKS×å\x000f nÔ\x001bL×oRr-¹îU.%0\x001e¸(

\x0019\x001a\x0005\x0007Ó5,Ow¨á¤ÄªÙ\x001cÖ/L#n4\x001cLWqÜý\x001a>záC1wÖÖ\x0014
`mÔ\x001bL×o8Ró@/æ5ñäóÐh9®æ/ÝZ$Gª½(\x0016p,\x001b-\x0007ÓÕ\\x0004¦\x0008\x000e«7	XøbñLTsÐ¨9ªçT\x0008%\x0004ã$ÐR\x001c]Ï\x001eµ×ksàû\x0013ËFÑÉéN\x0008îgCI\x000ck"»Ã\x001b]'gÐuFºchö½2ºØ\x0012\x0013ïl\x001d¹©º.
Ã½:j9¶Õâªèd£6äTµr\x000c\x001fâô¶ýû\x00121÷ë+
\x0006\x00107¢XN\x0015Å)"\x0001´À8¼\x00078?¬øöë\x001b\x000c±/ÛtdcÖå\x001ccO\x0006`÷\x000cÎ\x0013çôÌ(\x0016?lmAàMiG\x0002¯K;\x0015xJ\x0010v\x0015þ¡?Ô\x0019	?þçnä\x0000\x000b+é¸T¸\x0013)»h»-õ#þº8?<Ù:íÐe.çAÇ1²Ð-¦$ô\x0010
ùÚYzCÉUM®æ!\x000f\x0012Ç\x000f$ò¸þ¹®5þ×HJ·q fA75º\x0005]ÅV9S\x0008cÓy\x0012´SkÇ\x000e%w5¹\*
í;¬e\x0002ZtKµLÚi³vZÓPt_£ûï
\x001d,IÆÔññIwÕÐãÃ[]&\x0005ÏSµ~í|Â>\x001f¸ª\x0004$ýáE=Ðoïíòöýõ¡\x0001\x001aé\x001b%dM&Þá¶`¯ÌÙ{»8~yx°VÖ´r"­Ñ¥©ñÜ*Å\x001b_h'Âª\x001aVM]ZÅ=I±lÓg«`Õl"­®iõDZªtòs¦d Uk¯64ÖÔ´f"­^Uu[Ù\x0004AãºÂDR[Ú¤Qõñã¼SÔÆxëJ\x001bJÐÓh]Më¦^0IÓ\x0017SÏLÉñpö\x0000:Ãú\x001aÖO]ÚUÒ£\x0007\x0005á]y×íËÞpÚPÓ©´P^®½ÆÔ|\x0010,\x001f[3ñ Ôã\x0008l
OÂuÅÐÇ¦¤ÔêÏcc_Âms\x0004ã¶jlª\x001e³ë
­w\>Vún\x001b=\x0011¶Ñb0Q(µn\x000e\x0007dSsJ(\x001dÿvp¡Ñc0U¹U+½àùÝõ m'j\x0006hô\x0018LTd |©<Åp=7(.ýT;ÙÃq\x001bE\x0006S5\x0019N9¢Øl<\x0016¤w½/"wâÁmt\x0019LTfØüYñócI×
Üþ\x0005¦é\x0007h\x0019LÕf\x001eØ¦ÁJjºg~Õ\x0002::¦Óp\x001bu\x0006\x0013õ\x0019`m¦µ¥î»ô,ÆY;\x0013ïY£Î`ª>C#AeG\x0010¥ÔÞO»f²Qgr¢:\x0003LÖÏoL\x001e\x001cÑZ\x0001|pÝDå+\x001bm&§j³°\x001a_¤\x0004§\x0000\x0005aK^i¸­W6QI\x0011Ø\x0010ó"P»\x0015«ÛéÜ1\x001c·Ñgrª>JÌñ\x0003)½A\x0001pÓ¤l4¨!p6@yã\x0007.\x001fÖB\x0011ºjµ \x001b¡+'
]\x0010#
8ÖÂS?sY®¨Òd#ÆäD1\x0006X¢Fæ1X¸p\x0015Eè4\x001c«þêÎ-9\IÓ[á\x0006FûÅô¢X*\x001e£H\x001d^Êºû¥,%Q\x0012ëP¤\x0017TO³y§>ë¨ÌJ\x0006\x000e¸#ÈÈ$\x0010§[Ým\x001dMeU_"\x0000Ãáþ{e\x0019äLËÀµZ-5I	@Þe\(V[M\x0006ù£O\x0006^Ëm%§¡j°<iN\x0018ðrÓNÌÑ¹é\x001dé6°5h6\x001b\x001a\x001cIF}(Ù3I~$e	j3o\x001e5h1\x001f\x0016\x001bÚ6gòü°Z©yÓyØqÈ<óGZ©\x001cÒÑ.']©,È&ì´¡^Buy\x0019á]ÄçóçG·\x000fW÷÷/o\x001ebúôöþ\x0008õp¡\x00124h0ÄðÄi\x0019åáo|tr~xvvðúàø<¦OOÎ¶D¦3·(¹ÅN¸\x0019u\x001c±ÆS\x0011§ÎÛa)Ö^æDnYrË]p\x001bìÊ\x000e]Âá¬ö:wC¬Ý·Ôª¤V» väÝ­ôx\x0019`o³5¹Ù\x0001·.¹õ.¸½Cñ¸Ë d¦PÑÍÙ.ÆÛÜf'ã­r×'%Àz§CYeoî\x0000ÛØv\x0007Ø«UB¤Â\x0016óiSì\x000e°]ív
:ÐÞbAÆ6RrK\x0010Ïw1K|ÉíwÁ-Ý3CI.\x001eE\x000csr[6\x001f;\x0007ÓÃvÂÍ9\x001cïàdÓ4É\x001ad±ÃÉ|ðz¯ÜÅf),¤\x001c&GÊ`?\x001eÃÉ½Øä\x000eæ7¯öJ¾Í2ü\x0019*´I­N¡ôêªçÉ@9x"xµíð]ì;poN-°&Éc.òÍH}ÀÈ]-L¾é-\x0005\x000c$/¤É©xÕy»\x000bîRã&9|2\x001fß\x0002
¡gÄ_EGÙé\x0012ö¡À-\x0004fö®{çww{/®7ï>uWp¥Ì"hñI}è\x001cy³Á'\x001cIB;Ø;Zì\x001f\x001eì½8Z\x001cïÿ¼-Î\x000e%fl!133K¡=eDî¡&¨ÛÕb7ì²d»\x0019÷`\x0018q*çp3&¥[Z;Ò©p
»*ÙÕæ¦¦\x0002·\x000bïá-µY±v¤¶g
».Ùõnæâ¸!)K]7Â!\x001c\x0017kìn¦)ÑÍnÐ9£âPî\x0004ã[	ßhL`·%»Ý
»­x£a
|Fw#J9ëä\x001bê\x0019íPmÆ\x0016j3ó°Á}Án)IÊÄÒ@.f'3½È7°¥ÞÌLx'ºÄ¦-ê>ìX\x0017Ü)äõ´M	NE(¤\x0019\x0005lñðU8¬\x001b\x0013²\x0000_mJ|G»\x0012¤u¬\x000cKg\x000cA\x0012EÖ²\x0018^Yv¾\x001bÓ\x000eý\x0011°¡\x0002\x001d´Ü\x001fÁåmi'#?PîÌ*st¦W\x000båÔXOPðv}OI®råá\x0007¥+\x0006"Ù×Ë»«íQÐM"ÚbvU:¤È¡´Úå
BÙGÓÃ
1Ñ\x0012^ðrgð
\x0011\x001e\x0019Çì\x000b\x0005¹;¡W%½Ú\x0015½¥.ìÁñRXçÉAYô!ÍnÆ^ôz\x0013'UGYØ^¥§chìýf\x0001Ñ\x001ezSÒ½X*4÷Ðµ´9]ÿOoKz»+zÃ©ªDsR\x0000â\x001aÒä\x0012}ÍÌ§\x001f$ÛËÉ98É£*/Á»O\x0013(+Ðê(¨³W0ü\x0012v_ÂÄRFz\x0013ÚÓ0ùMl)\x001axâK¤;/78}±ê³ìï X8\x0008ÕÒ8^7*Õ/m­W;#,î@ÄõÕ[kîðÃs;\x0018jÈg\x000bKööñ!\x0016ÝíßÞ|¼}¼èónÜ3¼\x001b']î¹ª\x001d]ú:Ýýôäâ<ÖÜí\x001c¿:¹8;W¼b&¯ä\x001e'tÌPH><wpÍ Ø¼\x001fW¸rîðÂµ¹Êa\x0018ì¥¶Ùªh?®*qÕÜÑµ"\x000bÀÀm]â\x0015á G\x0017æf.¯.yõ\ÞpÆl\{k±#^=Pêç5%¯={mNýð
Ó\x000cÏ´OÌÝMÝjì F\x0011Hí\R!(è@iVC*¾0°næÀú\x0012×ÏÄ
n\x001dµu\`âR,'»0\x0008§tóÊì¹v÷_¿ÒDeÈÄ\Kö¯\x0006®ú5i`±è\x001cdHTÂ\x000fô!I\x0017V&|D,X]\x0007±Nünù~yÿp·¸h\x001eIÌ\x001f~ôÌtÝÖ
Ìpt8gM\x000fá!IúÌ\x001aFÓÃh>\x0001;ºÄ¼p1ñ\x0003ð{ö?]~¾ºAWmb\x0013\x0004Ã9ª[­\x0004v¥ã\x0001\x001cË!ÏxÌAÞÿùàõá1znûÛ»7 ¿(ùÅ®øS<-\x001d\x0014-õÉ°\x000cÛ£C:\x001f=(Nà%¿Ü\x0015¿p"\x001dùµN¡)n$Þ«ð"FOé\x0013ðU¯v\x000f\x0019*ÚäéTc¸¥²;\x0015û¨î_üzgÃOZ½aø\x0005:$aòã>\x001fÆ_\x001er'ðßìjüµË=LO\x001c¯_ø]M[òÛ]ñ3\x0005\x0012¡iü©)&·a7%~6ª\x00051ßü~WüpAðá¤ÂTÖæé#Íh\x000b~|^[ÿ]«|6&%RÇ:MÒ-bGÖWÖïÊ|\x0002rÓÃJPé|É³
\x0002?~\x0017üäeó\x0013³ÝX ësV(çÆ{IÎñ8mãW.(6`ü\x00006àWwË÷{§}\x0011\x001eF#\x001e&\x000c£ö	\x000eÄ§Hw¡:Å½:]\x001c¿Ü;½hà%Æ'}pÎ\x0005f;\x0005âPBÉæâ.Qptð©OMåóòö\x000fÕ#­#o/ê²ú\x000e>]òé\x001foüLÉg&\x001f£s±YóÖÚ,©"ëy\x0007-ùìT>K-*£\x000e\x0001\x000e¡Õ¡7\x000cÞÐ\x0006¹ÌM~³¤Úc¹\x0017¥%4Uw\x001cì\x00188_âùÉx9¿Ò@sOlj²>®Ó\x0013ÚùTÀ\x0007©\x0014\x0013\x0001
%ôA\x001e¥ þ,¡k9¼\x000e@^\x0001ò\x0019SÏòZK¦à»\x0011\x0013ß0¯¶\x000e>qï\x0008#¨hm7\x0015\x0010)I,¼á¦W¦O¶Íá0iWR\x000c\x00060Û\x0016#'Úf^Ù>>Ùø5"±àåû°Fò\x001b<áÓm\x000cË5.,Æ¦Ñüå¬×©|uß4\x000báÉKÙ­Ñ¹\x001d¶¥4QoøÔ\x0017­Ö8ÕÎ8±|¶â½¬hW\x001fÔ\x0017pázuw¹÷ËåÝ\x0013.í\x0016ÄÇÓìÔ&Ëç#\x001eu0\x0019´-Ú¹\x001f\x001eìýrpºÕEpQ\x001d\x001bHäàaQD\x0012[
hóÁe	.w\x0004nsª¶±Xâ\x0004¦ÈÞÅ«\ý\x000f\x001ar]ë\x001dkê©¥íª×4[ó]ÛÜî\x001c­\x0013xî/d|^ÚÌ\x00027r`W,£Ô{g·}=A\x0015m_\x0018óU¾Üº´.p¢\x0003ñÅÞÙÉ¶FÓÈ)JN13L\x001f×ÁZ£Ï`\x001cÉ]¸ÓÕ©JL5s8ñí{Jf\x000b£iiÚºùn+¦V·\x001eæUxë¿,ïï\x0014òãÕC_Ý&ÓY(+êa\x0011f/ùÙ¶.É;|ýfqv/\x000eÏ·¶ÀRw\x000f«`&-\x0017tÉ\x0006´hsãT[GûieI+çíJÛgä»rq©«\x001d~ZUÒª¹´\x0012£Ûi&?\x0013ä°\x0004I²j&\B\x0013·÷\x0015ÇBfE,½ÒQ"WJ×ÕG÷\x0000\x001a¸\x001d¿Ü.O;,Þ¬\x001aßiÄ2\x0010b´É*SZf\x0001\x0011;>\x001dÚK±<\x0016\x0003¿3=£ÚÆ@¬%¥Òç\x0013}wC F·N\x0011\x000fæN\x000b%´Ë.n´y½µ\x000er\x000cF+¿²¿øÁ0ýðèêmp\x0015þúçVä
ÑiHÛN	F18ÕÓqeWIÄ£×{eZßÑáÍCù\x001ddù\x001däî¾\x0003S6.\x000b_'}\x0005ÍÛUl\x001e±«ï Ëï wø\x001d8ÏùÐPâ_ÂKó/ø\x0012¶ü\x0012öèðåð»\\x0011\x0002£¨VA[\x001a+n,\x0017=ý;$¿XÕøÁ°¢äæÝÕåÍÍen8\x0007ppS	%ùp\x000eÈuìv´ònoq¼xp||ðt¢.â\x0012_ì\x000c_Z\x0012þ¶Ì¢\x0000h ¬BL;âW%¿Ú\x0019?7°\x0005$~ûI»\x001cç¶cM§ðë_ïÕ\x0014)l<\x0011øsGR³£á7%¾Ù\x001d>ËøÁ\x001ea\x0015³jX»¡ÊºßüvgüaÎ\x000b#¬\x0018D7ÖÐðÛvcø]ÉïvÇ/óàcsXc³hÿZÂ~x_ÂûÝÁÜ7\x000c>Þî\x0005þ¨Ú	?¯MÿÎl¿ó«/À³ô©Ñ¤\x0005bGÚ\x0001Nâ¯l'ßñtÞä½\x000bê	0Úbòí¹\x001b¯¤íþ\x0002¦z\x0001fw/´lÅ\x0002\x0019O¯ÍÚ¨ºÍvn8ÄÐ¾[\x001dbâÞ;,¨ç=àk:Ë\x0014Þ\x001dé÷Ýó\x0002ÞrÉ+çç\x0005\x0007ÏàR]>\=\îí/o\x001eÂ¿ß³\x0002zq>_<RçY»À©]7\x0007çç\x0007{ûãóü4«(YÅ<V!)ÿ\x0002\x000e¸\x0018óp|%3¤Õ,VY²Ê\x001f{\UÉªf«û3r[$«È¦/\x001deûXÓùbØXM­\x001a«=î\x001d-¿Þ^ÝM:ih÷\x000c3³%é`r%°Ò~Ko²pÎøåäðôilQb]`\x001bMÝ½´äTº«¤¡6¯6\¶s×¥¯ªê35\x000f´\x0002bF0#üÜ\x0012ÑÎ\x0006ü\x0014Æ\x001f^¿\x001a]Ì³@Ô3­U°\x0011ú1xle@£)ËW¯ã½³ó@ÿ4¤(!Å\x000cH\x0010\x0004Ä¬\x0000!¨LMf)¯ñ¾ªT3 ¥ÊÍÔ\x0005¥²\x001b)TîÏ9ÚQ´Òf\x0006¥Ê×ÆQÂ®Òf«×=ÐfJWRº9/Ü¾i*\x0003\x0016¤Ö"WûA\x0019p\x0017eÎ\x0005kÍÀä0µÓ¤0\x0007Rt)&Ç\x001a6bV«ÏY>,«<\x0019%\x0014¾\x0014\x000e:ÅL\x001fÊÊULÃYÑ	¨\x001aædJHà .h=Ý*9V\x000eï¥¬Åî®Þuz.T\x001c\`\x0016³Q¤|ìÔºIÂàÝ~\x0003©(IÅ\x001cR\x000e\x0006>Ý/;h<Oý	$Ý)Áx'iJc/Ä°ñb#Úÿô×ÿ}¸\>NÙB
´pGå\x0008%ðJ\x001bÁH9"ì¢[¶Ðý\x0017ç\x0007§ÑE.v\x000eU\x001c
ÑD18®I1]iÍ·9/Íè²D»Aú
è
	45áÕÊms\x0017\x001bÉáîÝnØ¡g\x0008
\x0005¯Au\x0003Ûfz>|]Ä!¨Âv\x0007ó\x001d
>Q£)øì(÷b¸$¹\x00171\x000f¾\x0018Á\x000fh¥þ¼|Vv¢\x001fA3Á\x0000
fY¢ÆoìÁûóâbë\x0005\x001c{JG«s:®æ4Ä;¬JàZÑYh³K¢]\x000f¨²D³Q\x0005æ±§ó\x000f	/­?\x001bes\x001aGV¸j.nxûtÞQÔækKØÅ»ª\x0012'bª\x0012Em\x0004v\°ZHÔ¤çzeí2Sì¡v6^ðäl¼¹½{ø\x000bÐ\x0005¾éÉ\x0000^JÊÓ´á,y\x00169\x001bûº¨æÍÉéyÜÆ_&ðñæ,L+JZ16\x001c×¨­L\x001d\x0006\x000fA]¤n\x001e­*iÕü±¥\x000bð£"Ziõ,ØÜ\x0010)
­I«lV9¼gsõ\Ý=q
vCàW
\x001dfáÝÞõ&qU¹e±õxk\x001b*\x0017ªïùÊÜ«Óíj¨4¤ì0±­\x001f\x0017v\x0008¸\x0016ú(F\¹âUã¹W
¼|x\x001dÏëøû½}\x0010X>~ë:@\x0019%ÕêHÔ2J²\x0008Ú\CíínÄââß¦\x0015%­I«ü3ÇVcìTg ÆîL{`e	+gÂJM\x001ch\;Ó\x001d£\x001a6uÁª\x0012VÍ\x001dYI©{µ\x0012y\Ç.SzPuªg¢
+/ÂÔ»p(Í½¶59°¦¤5sgA\x0006ZLx\x000e³ wìâ#÷ä=´¶¤µsÇVæªjç°7\x0010ÜúäºQ5r3ØCëJZ7V_ÍÛU¶¶#×à=´¾¤õ3i¹Ó0Ñ=àbCai7m\x0011ÍÝ\x0019\x001cõ?\x000b.\x0017éÑ;Ær~\x0019¹âîÁ­÷±¹\x001b\x0019´þ¥;@µÒ\x0003È\x001dA\x0002i\x0016nµñ¹;\x0019\x0013\x0018àIÙcè&øÜ¿Ú)æ÷àV[\x0019»1¶j\x000e¾*øôyçÕn&nµñy»\x000cç\x0018<¦Çü\x001eªêr>''\x0005+{p«
ÏÝÑÓ
Ób¥õzC9m?nµGðyôt=ÅH7\x000cm^fÛ\x0007vtbÂ¬Ì-go\x0003¦£Â­à\x00072çrÈXQÓ¨ºcê´\F×
\x001cË«ÎÌ\x0000G9îP¨\x000cõ¶ÑùUgðMýn~
\x001f-\x000e·$2dbQ\x0012ÙÄÅË\x000cd	Ó\x0000SÔ¥VòÑ,®\x001e`Y\x0002ËÙÀÐ
\x0017Îgtçè¶§¼ö\x0000«\x0012XÍ\x0013ñ:0°F]­0'rÏC)74=h'6%±Ml\x001c&×º8õ uVÑ,~45±ØÄv6±r¹
»g\x0014êAQsö\x0018»ØÍ&Öj%
Ë(0ætî(©§YÂ2¼S¢á\x0004kü·åÝû«'âM\x001bË\x0016èð\x0016oX$\x0015òÐÔ£ñÒ²\x0016éoÓ\x0002fåWåW;û
:l&tÁe)÷+/¸ô¨VYóWHEÃH¶¸Ã\x0004Ô\x0008î2|»®BFéÑÔ\x0006]PÙ¥Í}v×¢á\x000b¤.p\x0007þô|càO\x000f%ÆµÅíe\x001eî*Ç\j÷ØáïÖz
wKzíð*?5KY\_ÿõÏD¼x·|wµì\x0003¤~kÛ%%õ\x000bkÛ«\x0000Õ"\x0000'âÅþbÿpÑ\x0000,J`1\x0017ØAw´¿há©OáÅïxÝ\x000bx\x0002°,ål`\x000b5hî!pî¿ä;Âª\x0004V³ ÜT-Ø3h4¦ñ	ÇêD	¼ºäÕ³§0¨câ\x000cåñ\x0015\x0011NÙ¹\x0013Â¼föøAÅÆ	P×§q|-¶\x0007\x0011Ö×\x00194\x0013m	lç\x0003KjÒ\x001eûH\x0004Ö¹U}\x0000ìJ`7\x001b\x001bºÑP«¸6¤%g­;Â¾\x0004öóm\x0007\x0001æ8%4ÃcÑ°¬cúyy½kÌÞ6þES"]t\x0017y¾øÁs\x0012vû_OÉ@mLÚ\x0008N'Õ\x001a\x0014XâZä®Hfü®>ËBí=
,J`1\x0017Xp\x000c½\x0006`E^§Îi=)68W¼j.¯T(æa¡\x0005+5,\x0013«G£k=¼¦ä5;\x0010ØÞ(öæÃ4\x0008qGú\x0002wC^\x0019¦ð\x0018W^!Ý^O<g\x0002ÂqU¢\x0007o³Ø³ÝÒ\x0016ë\x000ch¶­83Læ1®¼J

mà\x0004Jl+;3§\x0016v&)dÌdÖ%³ÞÍ@s\x001cèpTÂ\x001a\x0006ràãóøiè\x0014#\x001c0p=9º÷þÿýïÿsðDFÝZvD\x0016ÇÕáGOÙ\x0011Üb¡Ö\x000fØ9nïåÞÆDº\x000c^÷ÙÐãYØ&! Øý<\x0006UN}\x001eÍ|®Ñ·4ÜÐë
7tJ5^\x001b*;W²>ò_¿gh\x001aø4«\x001d26X©Épú×?ßß^O²\x00062\x0002q~\x0004=*H\x0004_³ñd°RáôàåÉÑ¶ð\x0019öÉ4r(R2ç+\x0008ÕiV)ÅÜHF	|4´õ\x001b$i\x0018Ú`eû´æN{vßiâÀ0
òp8R\x000cç©ïISk=6\x000cn°²Úd`\x001d\x000eé¤å@°'\x0005!'CÉ¥\x001ck0ÓC¬Jb5ØHì\x0011¢=§>>\x001ckÎ%×Àn?¯-yíl^Ås¹ç.ç²äu,fwSuó°o\x0016+ûfý°ó·È\x000efó'$èÃb\x001fïàUgdõÄ\x0000?\ÛùFBBÕZ\x0011`ê0ÛÜ\x0008NÂh z?\x000b\x0019<ÇÒJØùvB2ê´\x0018Ö¢R&ÐIùÄ¢ÛäY³áNÈ
ß)l
Û»Nm<\x0007(j"\x0011~L~l~*@Ð[µ^ìÏ7wÍZ2^Gl\x00171Åáùó£Û\x0007Hý|yó\x0010û_Ü~þ\x000cÊh
C¥åÙkr\x001e\x000cs\x0019ü:Äqtr\x000e°¯\x000fÏcÛ×¯A m£$B\x0017%¼Ø\x0019¼v$Ï¬÷§°~PRÀ£vV'ÃË\x0012^înä=ià5	¬\x001cÎy;l7#¯Jxµ3ø`ª
uÑpx\x0017d!x¹\x0013v]²ë±{I±c5Ü\x000bEv»J¦Ý	¼)áÍ®à¡\x0016á¬ñ(¦g[SìÝìvw3>\x001cËð\x0016N\x0018Ø­É¹÷|'ð®w»´5¯lnõ*)Þ\x001eõqÛð4õ¾ü\x0006~gß HG©w"lK8ü£²aSG?{[ib;¹T\x001c2Û°\x001flÎh²;a¯·ØÝí±Áû¢\x0004Xn°Gbð¾pÞ;ß:q¶ÓW{,ßÝ&+óÍ£Ñll\x0004#S/fÙz\x0018õa4Gvtûxu¿·¸ùxyýõ{\x000fsLm!µmö,×KS³íttrqx¶·8~upôË¿?A*JR1Ô±|¯+\x0019)¹¬À×
;zPe*ç¢Í\x0012\x0013£u2%),wXË\x0016êAÕ%ª\x001a¶x®\x00115×ûyF+NÍ\x0000¦D53QÃ¿1y
åª<kVÓ\x0004XË\x001aëAµ%ª
Ê|µªÒ\x0004ð­ÖÕ\x0013°[BÃ|\x0010\\x0008¼~./¤ `k\x0000\x001b¶K>ªÓk\x0011Õåµ½k°83Ï¬Ï³ ëÂË]Ì\x0002^Y,>×dqå©Q\x0018V±GVK\x0012bÎâ*óáyÎÎ
y¤ÄÊèxËÈisbyåu#k^h`M7]`¯Ðty³¡óè®«»>Eô\x0016×áéÎhÕÎbÿêóåÃÕ_ÿy7-~Î,j¥\x001d
={n8æ)åÔÖ&\x0017{û¯\x000fÎ\x000f\x000fN·*¦\x000coÈ¹®;Ìû\x000eaé¢QzC½Ã§à¨ _pö\x0010CÁxá×Ú?\x001d|¼¾ºXï!Õ*^<"ö#\x000e'|ãÿ<öÞÁ«£Ã³o Êo0ì\x00035ý\x001b\x0018a0ó;^©\x000bì\x0008CiãWêëü\x001bÖ\x0018êÄ\x000b¿ÖhÆðkIYaø
&½q½RºÊR¨ªpB×=3(¯zï«Ë«ë'nÂ¹8àÒQý¶£lámäúm½¡w\x0006åWïýrxp\x0018¾Øê\x0016~È'\x0015&ª\x000bà\x0005|t\x0001üòö3dÃx\x0019¾õåã×\x001ezHwÃ+\x001a\x0005\x0002I\x0016U(ª|¨{õòä5¤\x0003ýK¼øe+¶\x001ab«ul\x0018û»e8p?wv#¸E½¦p¬RØ\x0019ÊiEiíõuB\x000e\x0003º\x0008ç­ðçÅ\x0017 \x0005\x0005fêÂù\x0017á\x0018:¾Ü{}ûxz'Â\x0013QïÁT±ÂÞ5f	(Rò\x001c]\x000fö^\\x001c¥^É £°8Ç	>\x0018gÄ@\\x000b\x000b¬ÃÆ*>©=õ\x0008\x0002ÉDlô Ì=¼iv¼e6,E	\x001d|:l\x0018ñÏáñîny
ÐGËû½WË»»à\x0016ÍèÛ&¥ê¤LZ¹Êpcc)Ó³.H
è§§£4AÎö^-NO\x0000\x0016güK\x00043¸Ä¶gÖÿºDË¸Ïüó%Ìqø\x0006ûË÷·Ëí=¯FÍ"\BºÏnm*?RÞå²
6z¹\x001e&:|ýÅËðÇ4gâ3Sú6gÁD¼ÍAâÓÛß\x001f/o.?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Æ¤"UÄÓJøÄk\x000c^½iîÛxõ?w}upW\x001fÎ®/ß½»yqõfïÎ¤\x0006
ÿ¦ÐfbÞ\x0015©plÛ\x0016³ÿKhé\x0014h¨¶L7SÌXdAñ¾\x0010Z-|\x0012¡\x001bn»¹\x0002äU&\x0014\x000bVLh9Udiòo%Ã[íFÈÉ¬:·\x000cw\x00119\x0005\x0019ÊÝ÷\x0019
Ùg2O,3-hé\x0004dø·\x000bÝd>æ}$sìÌD\x0006qº\x0000Ò\x0001§@Cg9ö_\x0007ï\x0011å»\x0019ÎjæïÀ_¿ØO?-i´oîþz¿ÉY·9éà§´\x001c2E|\x001aLÖÂD«,1}sñ¯ûöi503Eq\x0018ÆÑÅ`a@0\x00009\x0007`èU¬·ÀÌ´Ã1\x0018Ãj!\x0018z¤û\x000c£À(½	f¦\x0010ÀÄé Lbá\x0013aõ\x0019]^6\x000c3Ó\x0001a¼Õyð{¤eÒ
#\x0018£\x000c\x0019çÕâ\x0015[\x000b3»öa\x0002JÆ²düÔ¡J06±&.·\x001d]ô#0Öæ§0Â8Me'\x0013É#VI2aËg"\x000fYÃjhÄ|\x0004\x0003Ó h¢q.¿s&·\x001figâïò¢ÄµgÇXêÐI\x00088&N\x0012 z\x001eÿêþmÉgzñôoT®°\x0007=9ÅþR\x0002¼åf:>Iåþfÿ±e·äÅí?SqÂ\x001a¢Ò9NÏ¹¬i*:U\x00126­\x0001·x:fªg\x0005\x0012\x0007)	ÉÓ\x001c		\AJ[f
è(±Ïv2Úði\x0018ÉÅkß4SCÇeµHæÜe!¹<ÜÖ£Z5u\x0011\x0019OY§L\x0014Y\x0001 û\x001dEH{\x0014Àz¤g\x001aé(\x00139\x001c¥ä¦cELfw¼ý²ï`Â³­»Î·I>OoF&JÜæ³ÄSZIL\x001b?\x001c\x0005
t×ñvsßH\x0002e\x0011	É\x001bg5lýrx¶u×ù¶¹tb²RAÓS^t¥_¶´\x001dL¨úuìbÒ!çÓèé6\x0015Æe&#LImývxãt×­³yçÄ\x0014E\x000f@Ê\x000b#\x0008iÑ9ZODi@w\x0011)È³Zè\x00199vbNôãi\x0002\x0018ÒOàïÓ§ÅÀÝÙËî(ò²\x000fÊÚÖÙ´\x0016ßlÄä\x0000/#»×Ö.:\x0002Tàúû\x000fïVQÍÃ\x0001k¨¸Ç\x0003©èõ­\x0019K±ÏäsUÏ6¬ù»v\x0005Vºdò3M@Xø\x0014`i`·cÍÌË
,KaE3îÂtÖ¥JÃ	+ª´ù#R½îý>òK¶Ö±Wç·\x001b¾è#'=\s¥¾êt%yÆYô6£É§+æ¥Sxº¢Yt¤º¸æJt
\x0017Z=#wÑì¸b¹Ë/º®ãeòsÁ´ÏUR3¹Ûè\x0002Eâó´;UaÆè¬÷þÛ÷\x000fû\x001f>íE
*ñX\x0014\x0011êxEH\x0014ÉI\x001cÎt½ Q/_Ý¾Y35\x001cÁ*Sct\x0015JEB8É«åGçjùsá\x0008×y\x0010#â83éu¤±#x
mÍZùKá\x0008
ºÀilö\x001bL8Ú\x0008gÙgYK3$\x001c¡Áßt\x0019\x0006\x000frb\x0018ð\x001c§0Ï&Y°âèJ\x0014/\x000e1>§ç\x0001â¸Ào\x001bÕâ½Z3¯\x001c\x0013\x000e\x0003Óx*ÈÂÑ^hÜ&áP%5ýÿëqtn´@\x001e|¨È\x0015\x00076¹É=®åZ\x001eÓêÕ<>¡\x000b\x000f2u'ó-W^ñ-·`7Ýògfö\x0018\x000e¹¶9\x0003@e6GYþZf#Í³7Ü\x0011\x001aðr5Þxp)\x0000\x001fe\x0008aÛáyö;ÌCC?²OÖe­C\x0012c\x001d¨[~\x0003\x001c¤y´þl\x0017ÿþt÷ññéýa7À\x0007\x001bÝ­¤Lå¤\x0008}Äé\x0001\x0000.úE5xù/·\x0017×7·o×0Í^\x0000ÇLâI¬I'
Nfvü¸\x000c\x001fuÑ§í®ãPSgé$)Py@Î\x000fÉÕb\x0016(Ä»i¦¤3MãÊRfJ"¨h\x0015\x0007\x0003 °èÍö@ÍTõq(GÍð!CùiÂ
AQu\x001aCéå7e\x0007Ô3½BTè|L'\x00125±\x001e\x0007ø\x0013Õ²ãßC5\x000fy­ 6ß>ÐÚ3ÏEÊÈäÂ¢6èa+ïãL\x0011]Å©\x001b\x0019¡£8QÅ<_\x0016©òÜéMTs%~
½Ãs>é\x0011(Ú³\x0003åóÁr6²\x0007j®ÉW
=éÕFT±äQ¬*÷\x000f6Àù£m\x0005\x0015\x001eõi*}@CÝÎ\x0013\x0017U\x0015í²é z\x0016iZqÔÊHà%k¹°\x0012òv®MHx(¡ÏÎÐdxk
V\x0001¹~¹k\x0013\x0014þ­ ï £3[K	*'¿\x001c)¿Y'P)\x0016>(ªäÕ\x0019Ê'1~ø~dÛª=©\x001dú\x000ez¢x*ÊL³º'*\x001eÜ²
zÌ&?\x0005øþçÅ	*ç¸xúáþ×»O_÷\x0017t8JªÄ\x001c\x0005\x0008*ß@\x001eLÌÅj&\x0005R¦{ê9.n_]~wñæÃþn¡Új
\x001d¾¢r"\x0011%d8\x0010\x0018EØã_uã-é¬À³T9Çt>ðDäa\x001eÒr\x0002¯n\x001eÕ\I÷Óçç\x0016ª/ÊXe?0òS=Nh;Þ³WàJ>WÕ1I9É\x0010ÁH\x0005bÔË²\x001bonÂWâM\x001bøëÚRV\x0004A\x001eó\x0011Nsö´þãÝ$À»~	\x0006Çé,DÔ\x001c#hKAD¸üd\ø\x0015~ùËÇ*²¸\x001bå#¿Üüx NÜiwRÊ¥'SrÍt\x0016mF¨Ménzk\x000ez¾½¼¾Þ\x001fö¬à²jé\x000b)ï]L´Ùê9&8Q \î-ß\x000c_o½p´$f¸ Ñb\x001adï\x0019´£pÿþIýú¿âÉxýøéûî?=ì\x000f
X2\x00179dæ\x0012zD<	\x0014ßsÊ-ê×7oòÍÕþÐÒ¦ÂÿðÞ~¼û^¦6¿¾{ÈógöV5óÛ)KtnL.\x001dæ.\x0013ÔÈSÎ¸à½½¾x)S__\ÑÈ£xPãA'áùô\x001e]Ô\x0019/)\x000eñ\x0004P°\x0011ÏÔx¦\x0013\x000f
\x0006Ó¡9sZj;Evv«ìl
g{?­ÉÛc"úá<q½:°6ö¡	ÿôÐ©ùÁSùà½{|ú·\x000f¼x|Àÿõùéã?þ~° XÑä§\x0014\x0013\x0002\x0015Í0bl\x0002/ïnn?äí\x0003/n®ð½»½>P\x001c[(¡¦\x0001J\x001f8;\x001c)
«RIr#4P¦¦4#²\x000cãÏ_{ª(mÉy¦ÎxÒÖvÒæý,Ú¹4¨]ÚÊû°ÒÕn¶È\x0004¦ô9e®È²}Ò\x000eRúÒ÷S\x0006\x0005¢º§Ê!>ÁÅ\x0014à e¨)Ã,\x0013H\x001e\x001fºÔë<Qr¯ó\x001aÜ\x000e\x0019kÈ8"JÜG§\x0012{ø¸\x0003¹áí\x0013x\x000cGü¶T\x0003ø\x0013g5UN\x0006\x0011eäSI\x001d\x0006Û)»£\x0007.OÐR1Ç²¤\x001d\x0014MgÌÂlcÄÝnnzÚ\x000fDx÷é\x0003-\x0019|\x0012J*\x0018\x0017¼Ë>Õ^5	Ùâ+\x0012ÜÅWkè ¦>:
Â@ve\x0003UKe:\x001fÄ\x0016\x0008mÃ35éÄ£\x001cv~\x0006à¿\x0004çª2Mí\x001c\x001bé\MçúèÀñn­¤"åsÊKjÞt0j«ìBM\x0017:éÐúMU\x0012n-ÍªBG¹p
éò"-t©¦K}tÆ»\\x0010ð9¸÷âEGË \x0006ñtÝZüú¥òåìÃ\x0003¾ï>\x001eÐ+`yhmÒSãv~©ÐÖÌ\x001c\x0011T°èm¿?ûp»Ûë\x0015xPãA'\x001eð\x000e\x0013ÂÈ\x0002^\x000b¢òÖ-t¶¦³½tïÖÆp1(-\x001cÍÂÓÉo¯é|/â{¡Q½qy8ÒY{¤¶
/Ôx¡\x0013\x000f\x001fÆO\x001e:­?­ä\x0012ðï¾Qx;×`º\x0017ª\x000fÆ\x000bqJ\x001d¨±/[\x0013£\x001c=ßÊøþx7#¼ëCô1\x000fß@D+\x000e\x0016>è¹Øæ\x000e`?\x000fx5\x001blûþîO_\x001f¦
±{E¨sû|Ò\x0016"GÍQ?1\x0018¨?q5¥ôýÅ\x000fWï\x0003\x001aÐô\x0002&-7Ä:ÃºÙ\x001bî B@ì¾\x0011ÐÕ®\x0013\x0010\x0014\x0017ßf	:V0:Ø"A»\x0015Ð×¾\x0017Ð'\x0016£O=Ñ\x00143¸Æ´
Ñ.ôÒiÇ\x0015(ÚÒ¦@Q1®\x001c@¿U|ñùýÑE8íC"¼(\x00071\x00051mnqD¼\x0018¶Þ\x000fÝ^àÞ\x001bLßÔE_ØË
¶Aäç"l\x0005lîî¾ >äh\x001c\x0002zC®B>F 7q+as\x0004u÷\x0019\x000c<¦\x0008#×ax§Ø
#á¸\x000cÕÜÃRÙÃm¥ß|þÇÿ{°^%C2¤_,?~=\x0004%
\x0010b\x0013á5¥ß¼»<Ô@_¸LÍez¸PRì\x001b\x0018_îq,3\x001d­Þåk,ß\x0015¸üAS\x001f;+<0Ü)	èAÇq®*ÁþÊz0Åé\x0010\x0004ÃnNÔxí<çõu~\x0003Xs¾tÇ\x00013©Ahjtc.\x0013¹|Ó5¹+e®Ý»,¹©³¬Éo}ûøôõëýÙÝÓÙË\x0007g}qD)^û_é]É§&7ìËr}{sûáÃåÙÅíÙËëãÄ kbÐÃÄA>7¥r¼Þ\x0019Ø*Ø3\
\x000cód\x0004¨ßÍy_PúðìâÇÇ§»\x0003]'VE\x001fh\x001aªÃv\x0018çc\x0007a/ð\x000bJ"] ÷ÅÕö\x0002\x001ckà8\x0008\x000c4Þ0_ôh\x0002\x0014¨ß
ßl`Å\x0016`ÝJxTÄäk\x001b.Kvº\x0001'WV,µ×édÀ©\x0001ßºÕ"öÀ¥H:¹¢Km4ìü©¾é$ÄàjbçÁ×\x0012SÇÒ\Ïl9\x0004Kãµ\x00144JÄ¦9\x0013fôL ê:Ïe©Ê\x0005î¿ô¾øFT!t*àFÂfTÂÖ\x0018\x0002µ÷ä¬\x0006¥5\x0010«SXÅÝã;k»Ásl!g[\x0013­½æ°··Nâ\x0004^73¯¶\x001d©í¯=\x001aô'cÂ6ï%¥ãQ\ç\x0010Ä	©)z\x001d\x0002×j\x001eFPÏ­È·S\x0008õìâãÇüý@1\x0006^Ü\x0014MlÌoáàñ\x0011ÃYÚì=\x001bßNÔ³\x000b^\x0001\x000b5ì¼Üh-,êà\x001c\x0006ËQÕàyt2²\x0006½ß¥è55ì¼ühµd=×¯£¯\x001c¢¦5\x001dLk÷«â>Z[ÓÚ1Z\x0015`ª\x000eAX¥ËFjæÍ\x0000'`õ5«\x001fbµÉ;\x000e_+½+\x001f@(0,Éx\x001bíÜOÓ°Û\x0019þtv}÷ëãÃ¡\x0008\x0018Õã\x0007~Ñ8®µñÆ(y¶®$¼¾øîæêÐË\x0019æ\x001bTµ9è(\x0014C¯ø²áVxov\x0002Õ\x0014\x0003wB¹\x001aÊu@ù\x0012£\x0019\x0010QâÁ\x0012\x000bQi\x0003¯¡üj(ÐJ"¬µsøCóÌ%|ºgï¾õP¡
]P?âw ÄdÀ<{½¯5T\\x000fe<»\x0016væ\x0004+íÔ\x0012RhJÞú ª  ¨zÏÐQ*ÇåE9 Àñ\x0017\x001bµP¥çñõTÐPÁzªhh}¦*ÏK§­|@eÆOn^¯\x0015\x000c&~V\x0000\x000e¤9ëO \x0015ts\x0001õú\x001bhxQH¥å\x0019ãU(TñYHh=Us\x0003õú+hÃÊÊ°²\x0007>TÔã4ÔÜ?½þ\x0002ZY~µBà×\x0008\x000f©!­`7P¥*u}>¤P\x0013E²òùDTn\x0000JùY^\x001eÿ Øäû/g¯>?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=®!\x001djØ\x001a\x001a<Ç\x0001\x0004
ÐN.°íx 9S£<p\x000eÂR3#^\x0015\x0019ÀKWÙ®ß-Ðï6@ñ»U<zpÑKÚÑ\x0013ºü4zÏfÖJ>qh î·Íx:\x000e4zó&\x0016\\x001e½â>ÙÇWÝß.]\x0004¤r\x0019üÕ
^·8'£ûeÇÂ\x0015¼2â\x0006vFc§R½AÄsÅqd\x0000®t\x001d¿[ïuJ$¿éwËç\x0012Û¿eüüñs0+¶³¤µðöñó§_2²¼.¦\x0011=Æ)¿\x0002¯Rñ\x000cÇ7tWÜ¶ÂÛÝÕù\x000f7·~¾\x0002/m\x0019íx!%û'¼xª£Ð|üuÅ¡|\x0000/\x0005å\x000e<Ëj¹?Û	Ï+ëÕ)èRÐk¦Ãl¬¤ß­tÉõfÊÆæ´µµ'Àã¨ÒÎç&Sé\x0004jÎR²ÑJ	ÿÁ\x0001´îõü¯Ç?O5Mqu©\x0003±Ý§çÏSP\x0005Ì¢Ù4ë¿aÚk=Ia\x001b^z\x0019­\x00147Þß\U
\x0016K*¼´é\x000eªLTè\x001eN­v\x0008i2\þO\x0013Kê¡	\x001dg¦¿\x0005é½Û(?%è°0k\x0005ÍC\x0015¦~\x001c*7iU¦Ñ¢\x0004\x0011\x00081,R²u^91u_',ê\x000cF¬TkX\x0016Æ°4þ\x0012uë/Ñ\x000bÚ¡\x0014O¾^ñl\x000f³]Z¤²ÍTvòMÓ=\x0014G*MÏX¦`z°^Àª{-öÌ\x000fÏO¯¯/7/?-+\x0008IsJÐ3×Ô\x0013´a\x001f°>Ü\î6w÷·7»Ûzúÿãëò+Âàðà¿ß¼¼þôôÛ¿/]Ý¥KÒ±øûÂ\x0004{ú}É`\x0014-º2«þæöþârw[{Ç×nÅË|úÁþ\x001dùëæÍÃçÈ¼ðBË²üê\x00178§]~{8|®½Û¼Ù^ß\×I\x0019
J(hB/ezÙ\x0006ÇY\x0004#râÌýîÑ¶\x0001KXª\x0005ËNöh	Ëó\x0015]ÛvqOl
Tº¤ÒMTï\x001f8Xt=Ò.¿ü9;eJ,Ó\x0019u:ýÅ£3mzñ\a`jÙ\x0012Ë6þ\x000e\x001dM-EÖÓïSz^\x001e¦Î\x001a°\åFKQþ:\x0000ÜÓ`\x0019þ\x001dz{ø&Ù@åK*ßDe9UlTHuÀÅGdïúÇZW8dÆÁôXÍtNñh\x0011V\x001dÑ!î\x0000s,|\x001dbîó°9xyz®£	Ì>¥Ó'¶§4½¤p«\x0010 ÿ£SÂÝÞ^Þ\x001cå\x0019\x001f4óY3©( ¥þxì\x0000²tá\x0016ÊÿG«õ|Á|Á´ò	MÛR~|ñÏqP\x0003¥h1rOßoã\x0000J´È\x00005½?üR!Zæ«ÕYd>3çk\x001c@\x00190' \x0013#1ÃÉÉ]\x0012 vÿÑ°e\x0000ÿúp8\x000f­cèþæÞ-I¯ÛXÔJM`3Ä=øT¢Ë2#(RQ$\x001dáóâ(%Þ4éæÅ}ä§Æyí§ÓãØ3ét&\x001fXµê/\x0000Kî­Ø¡µY\x0015õ)\x0001$\x0012y¥Ì°"ÃÈá\x001e¡®Bln¬EÆ7[Æ7³\x001bQ\x0015ï!c$\x0017¯\x0013¢\x00131º´¨=l.V´A»È>Ï¬ºÏcF\x0001²¬
à£2\x0019ñè\x0015
c·{ÉGgQ 4´P}ÂÈ\x0003TÌTÁI¨\x0013_jBeý:U'*=#+gy\x0011A¦ºg(~I&g÷CPÐAÁ\x0014©\x000bH»"*N5@*¿\x0017¼\x001b¢2\x001d¡B»ÈF¦2\x0002ª\x000fN²½¬¨!*ÛQÙ\x0019*|Ý\x0006ÞU^özÐì5TA¹
åú\x00038\x0003\x0015b
k\x0010´
µi7\x0004åU\x000båÕ\x0004\x0014%J\x0016½\x000f4¾@\x0019#ÊåMå;Iù©ås\x0014\x000f)¢Òò`
ºnõûUÕ½÷$CNRaJR*ª®`êòåÕ â |Ñ \x0011\x000fgC"ÇÉ+D´ª¦4¨^£OÈÉã«­X²42Nñ6\x000fVä¤î¼ß©\Oå¦¨\x000cùÞ2
ò$	\÷§¸ºÏuøôÌéó5ÿÏèd(Ç SE%^ÝD×\x000eº£\x0002=E\x0015ó¼\x001c¢Â×¸ã%Ó\x0017Íòõ\x0007¦§2ST¹#
A¡Ôì+/^g½ÿ7De{*;C\x0005½(FS,M°T\x0012gøn
Ò \x0002ýëÛ
};\x000eF\x00195¢\x001d¤á\x0006´èPµlÄ ØÍ\x0006ìfB¹Ûz
ºÓ5\x0018êÝìV
\x0006<z=\x0017Åq0OêÊòaT¥Ü3\x001fFËKéw\x0018½Ù½YÙúÉË\x001d\x001d¢\x0016%±nâJ¾Û¬ä»-fòÄ\x000cÞbì\x0013\x000bVvIË¦\x001fr½ÙpMB.ò¨È,[?TKk7/~\x0004Ì¸ÍÄ_L\x001cJR\x0018q
\x0001±\x0011^¾±q½Ýî°	m{¿¤\x001aêXÏ®±\x0010uÝû»èçÉ¤¼²\x0006\x0019r½bÓ/s}¸ýõ_T%|.\x0008cøÝo]¥1Í\x001aâP\x0003Ík©lµÕ^Æ{võÿAåÀ\x000f3BË\x0008+Qrv\x001dQ§(ééÚ4\x000fÿUHÓByH£$øî©(¿(8R\x0010Aã´-£g´¸\x00135/6ZµÀõH. #º\x0016Ñ-\x0011\x001frìFÆ×D(Ú¥v\x0019CË\x0018\x0016\x0018O9ä¤¦Q¤ÖL·«©L\x000bdóòÔ¦4q¦x\x0017I¶\x0005qº×>\x000bêÇrz­³Z}¾&¬´¡iB·	Ââ/\x001aýøüöÛOg¨lÂ\f8Å\x001c$Æ\x0002w÷ùÕë?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ûu$¨±×UÙë¾\x000c4d\x0011T°\x0018ö©YKÕÆo
AM\x0005%
\x0014Â4Lò*G»ZÅ²65\x000e¦\x0002©\x0012H5|2=X\x0008S¦6O
\x0016ÚH´L\x0005Ò%\x0008\x0004³¥\x0010HÃ¼g\x000c\x0017mæéÆ1%lK\x0001û`up\x0002½l	d§Ú\x0007Dè\x0007ûàtO£M^Ò§ÍT W\x0002¹É\x0016b \x0007M\x0016Â7â!U7g\x0005ù\x0012ÈOµ\x0010 odâ\x0000CSEBËÁ@\x001boQ\x0013yg²è\x0015ÙäM¯³°<c\x0014¼X¥=Ö»éyí§§:j\x0015®Îd\x0013ÑmQQ+´ñjã¡d*Qå¨ùdOÍ\x00058D¤ }\x001em$gó	v*Oå§ùTG­ ¤h!\x0017}\x0012A3£QL-D£æS=µ
g\x001cï\x000e\x0016Â®\x0010Ã²6\x0013ÎS*GÍ'{ê\x0010«Á\x0013a­³Îr¾36>¯|5ê¬Õ  \x0003\x001cfg´\x001f\x000e\x000fÝ½Ñ*gÍ§zké,Í¼eU\x001cÚêáøèvF·æSÝu\x00085\x000e}FoS^æãcsðT Ê[ó©î\x001a^æ]¶§yÍ\x0013Då®ÅTw-½¤f70\x0011=s¿Ï&êu¢r×bª»\x001en¿Z)9ßFu\=Õ]K¸®l#\x000c´\x001dVÑÆõc*På¯ÅT-uXÌ>ÓÃº6óMTùk1Õ_KP\x001füµÃ<OÁø^-*-¦úk)ìà¯%EÁD½ÞQTþZLõ×ÒÊ¼õUv×YÂs*ß(¦úFXD>¦6W-M¾m*L$/}Q¸q0PÓ|8?úª/'ï|aóÌæ4Ò\x0004WQöª\x001fÃë2_!6é¼\x001cA2Óp!T¢«µ 1;ªUmºëÁät.\x001aQÜ Ëøì»EïiÂªñ¶	¦ÛN0\x0017½ýq\x0018SvHÕ´®«u¸?V©£%\(GñGë»o×_\x001envôÅ[ÐêPØji\x0005öþ\x0019¾A­îYõ£åéåêÝùñ®\x0006~Ä\x0014%¦èÁ\x000c\x0017q¬ê6ôxdâ¤iÄ¬S9²ÄÖÌ)9
ÆÌ|\x000fªTíF\x001b|"´Rà8Tc(p?+.Ñ\x0000©KHÝgITþ\x0004±¤*\x000f¦¤þÑí¢\x0013Ó¦ÃcÛ¥ÑVìÕ¶¤´\x001dÆb
\x0012\x0014¡¼cøâ¹QÖ±}`º\x0012Óu\x0018SèlÊ$õj\x001cú6ø³úA
¾dô\x001d>O\x0016³ápfhJ!³)Õ\x0012NYN·s\x001bÊ,0Ã¡ª´`Í'4çÝó¬ÒM\x0003e}öt\x001c>a?SÞ
! 1yÆâó27
ÕÑÃ»Î\x001e\x000e\x000fÛD\x001a¢àìÉû0fuôð³Çè,\x0013\x0008O)û\x0011üz\x001eHåÜ³Z<
ÕéÃ;9«ów\x001c@ (0´¡Ë4¥\x0006Ù\x0003fuþð\x0003ècÍê\x0000â\x001d'	Çù°6=ntû~¬Y\x001d@¼ã\x0004úçX³:xÏ!Äò@\x0001+\x0019Vy\x0019\x0018Y¶OsÊ¿\x000eÿ\x000eµÌ8DW;Ë3ç\x001eNKQ¹NÑá:uÎ\x0002fº(Ùº½³rI¢Ã%éàá\x0005E&keõ^ÍYmvÑ±Ù5¨ëeÌ¤Þ\x0013N'C¤}ë¢ÚE¢c\x0017i\x0007\x0004\x0001gòI\x0015Ö\x0011pHsÔXÀ|­
÷ýõSjöÜ\x0005é´õÐáê<Ë»,PlëC=÷v~¿ºJ-S\x0018EÉ(:\x0018U®ìT\x0002ªûcvÃûÜ¸ü`]\x0013¤,!e!%)	h\x001aC\x0018\x000cIJ\x0002moÈoT%¤j4#´çT±h\x001d\x0015@Øpá\x000f©KHÝeI©m+é)Òåf\x001c;ª1î4%¤é²$A:E-ÁTÃ\x0008·Ù¶´\x001d$^aâ\x000e\x0016Lyzs£r>FW2ºvFíi¶Ê¶!sÙà> }	é;¤DVT@I\x0013!%ÛÞÀß\x0002Y\x0014¤ø¾ÝtS¢ò°6ê¸m.«Õr»<\\x0013d}Þô\x001c84L\x0002ª±°J4XÜäxrz\x0017duàð\x0013G{:q`£gKÒK
ÌWOY8¼çÈ1ô(©<£É 
i÷xM\x0013euäð3G»ü£Ùà)I±ËJ¿eY9¼ãÐ	\x0006LÊæ\x0001N\x0018ª33~\x000f\x001f¼:sxÇ¡£ód\x000e­\x0018Õ1\x0005Sòì¶+q4QV\x000eï8u@\x001fmiòh\x000e\x0003_³\x0018W§\x000eï9vl>v *\x0014-'-	5?¤äÕ©Ã;\x001dçè\x001e®´¦î\x0017'¨Ã$ÜÍæopQ\x001d;¢çØ\x0019V¥ð$èTlp±ÃQTçè9wHî^)M\x0005\x001cåÒ_¥ç¯JQ_tzÎ\x001d;SýTXt\x001bãrþ%BTçè8w\¾)¨8Çøâ\x000c#Ýü½#ªcGô\x001c;\x0011n»|êÐ;eÏhÎ6AV§è¹ê(\x0012\x0013SRPs±*å>¾wuì»\x001d2ÿ!ä0tÈ£7ÑÁm¢¬\x001dÑsìHºÛJÈdh²%\x0015A°gD¶(«sGô;Ü/NpasÈ6ÿ\x0004\x0017Õ¹#z®;¹\x0016j^³%\x0013£\x001eMZébÕ©#{N\x001dMÅ¸ÐeÅTÁ9Ê0ó·¬N\x001dÙqê(AMqrÙµyü¶æ{ð²:vd_tÅ¹£ª&Çd\x001e¿=çÈ:¿Ö~êÄ¯L),þøXzåhLY¸½¼u\x0015` ÊÊ£Ëv®tnÁ\x0012 ù+¨\x001aC6åg{tPù©/\x0012¶Ý§L
F\x001a\x0002z¾±0õ3Âýmn¨*´K®¨\x0012"jyPc;\x001dîÈêøü\x000b¤ÐÂ)\x001eæzÜ&úvæÃî|\x000f~3p®GëíNIqG)·pA#P±k¤ã¯/eÏ×ë¸ÆýÄ¨éÓ8\x001a§¥Ü¬Û¤\x001c7ÈÊ²Avýu}·ó\x0008¢\x0001\x001e£k·¤0ÞÖ1³ü°<}\x0019H@r2TÈ\x000fDÔÿ©¼Ú\x0003*Ôd¤ÀÇt#é}É\x001aEâ\x0012|k\x0003ß4$]"éÉH"÷\x0011G+a\x000c¦¸ÏVÚVô<
ÉHfºòäh%jLÅÉ<+Ù\x0012ÉN·¤ \x001f¬¯0V¢\x0000+m+*äJ$7}y3|÷u:ëZ¥ÉHls¢ód"_\x0012ù©DÊævÙàh~¼±V7ÛZÑ?	©x\x000eUêåw\öayïÁLEb]Vý /2q\x0012l\x0005&j¼*o¹ÍI¸*ÇÄ'{&åy~U\x001e·ùUÙu;K^¹\x0001>Ù\x000f(í©úÓ%ÉèÔ\x000fî9ù­]\x0013¿]u §ïW4>¼h.O¹ÈpKñ\x00132RW\x0012[;Õ':Í"önóSÃGZòá>rTáÀË§K7T0WÙÌU4d¼DÆé+@RcM|&D°Í!ÚÓ\x0017üÆT-\x001fÒË Ã>smë«ú\x0019×õg\OþD`+ÒLjE\x001eÜs+\x0014g¾\x000eíÂ_@h÷ñvý9\x000eFþ|}»ø¸þrw¿{³¡Q\x0007'¢6ùîáke'Ë£8\x0017ùhu²ø¸|wz¶+ø\x0014ãàS\x000cúXOÃ_ÿ±sâ¤âÊ\x001c\x0008ÈPtö\x0015[±®\x0016«]£&	IHb:\x0012ô³Ê¬\x000e§±µÕ9r©fS2f2,äd&h\x0000Æ\x000b9	ßP´5.©ßNªdR
LG
\x0015=m³ÛÒ~ã8Ì¤K&=	Ä-2
\x001a½0\x0000ìÇÌdJ&Ó`'Nõ9\x00104KvR"Ûi£Éu2-ìt&«\x0007&{Ã=g\x000fvr%køv¹[\x0012ìd¨;9/ñÍþ¿ÉH¾DòÓàÍ`XN8­U«|ï\x000b«½©Å\x0010\x0019O\ãÅr\x001bK|Sh2SíÅ\x001bÜx\x0008q®¹\x001f\x001eª\x000cgd(#û
Uùq>ÝKë¨»Ü3ütÚíÃL\x0017çÓÝ8\x000fá0\x0011qO!pùòg6oZ¡*7Î\x001bü¸1Õy
ÝJøl©n_À+?Î§;r\x001e\x000ea\x000cY¼ðäÈAß\x0016¡ì\x0005U9rÞàÉ(-ça\x000c\x001ejC\x001d`2Så4y×ÔêT	aÃBÏ?Eå¢D\x0002éA`\x0017÷p*3u<QGu
Þ@³ÁçU-¯×\x000fUí=Ñ°÷@\x0018\x001c\x0002Ëb<Ü\x000f±fw\'ªe.\x001a¹\x0012t\x0007(Ì¬kîU.ªU.\x001aV¹tTàï\x0003$\x0007G«|ÔÐ\x0002%«U.\x001bV9´¼e3aCùâ°)²:©Zå²a\x000bU~;g\x0011Jä\x0013fsJÅd¨jAÉ\x0005Å$\x0015\x001eûpßÃ­§\x0006mfÓ{QÕ×SÓ¿0\x000e®iIiÒTR$ÎáaQuCÕWªéþ \ïò*|IT.$µpêñî½§ª¯§¦=\x0001\x0013IÒ×Ás\x0012\x0014ë\x000fTå\x0010ÔtÀ;^8Ê\x001b\x0013Æäø ûëéjIééK*üÇR9&\x0015E"¦è|±¶×\x001dpUÀªÁ\x001f\x0018GÍãpê	Òé2j\x000fÏjD_ÊûP\x0006oREä\x0019' Iyü\¤ûC<åÆhá34°I
©x\x001eô Y~42âÓ/3UBVT	ÙIw\x001aãâpÑ¢D\x0010)~\x0000[·gbl4Ñô=; ·f\x0000µ¦H/ß^\x001cÞ®ï>?Ïe¼Ñ¹\x000eLy\x000cgtüÄ©òBnÍu\x001d-\x000eO§G/Ã\x0012N´Áó\x0010%(`²B*;¼\x001e\x0016-i±5|o%l\x001bê¾BDd<\x0002\x001c&gV|ÛbkS%js.Î0Ý,Í°ÑVRßH¸nlÛ¥
pºÓp¶)Ì#ËIn²å¶í\x00068SÂ68&å$ZNÐt`¹mQÆ\x0004¸p.\x001e\x0003Â\x0017Á,··¿þãzñþúîáfq¸~øôôø¸KK>ü×£I³Êij¾à¹SÍN÷åÉÉjµx¿:=?^\x001c.Ï\x000f¯..v	Ê#¥()E\x0007¥Îû*\x001c³æáºÜØàå|JYRÊfJë='aeÐwW)çÄh\x000f\x0007Ú=@ª\x0012Rõ|pKq/Èô«üÁ©\x001aßÕ\x0005}º¤Ô\x001d¦T¹¢\x0018ª8PïI\x0012±|\x000f¦4%¤éÄ
S(ÈÑ\x001e!9u_zÐq\x0017e¼\x001dÎ:0a0ÚR¤[*Óú\x001a8Í(Dåà×æe	É5|\x0014û£Ô¨F[ªQLßéÂè>µï\x001fcqÖ\x0016WÃK=LH§Æ :±Ü\x000bº®A×í NP¢Ê³\x001d\x0004£&\x000c£Ä}ÎÍøµÜø\\x0008yÿt÷íæáþi\x0007\|¶\x001fZD\t\x000eê`ñm^¿Î®N/ÏÏ®vÅó£01`\x0006,ÉIH\x0018Ô'\x0000ãJr½\x0012õ4\x0019ë%k\x0015¶ÁZl:\x0017ØHùl.LyçrgþfFµ«2\x0017o°U4s­×I²Äÿª\x001d6§FMÇ\x001aÍ¥\x000b,­LZc¢lCJõ¦õ¹­Å>/Ã1/F\x0017<3ç¹sß_¯ï\x0016o\x001e\x0002Ú_w\x0019.]XSª³PcðÔ6wµo\x001b¡öýjy\x001aâÃó\x0000øo/\x0013P4\x0013¦· Øã\x0001ÝíÉxOGðØ>\x001bQ²\x0015ÑqE¶
¥ª\x001dg¹)W×R\x0010]ªDTÍÚæ!W&6ÍDÄáøÕuÿV\x0017¢.\x0011u#¢\x0017ðZS ,=¹b#s\x001bVó×¢-\x0011m3¢5$¯ò|Kg£ÈZm\x001dÕØÈ«µÈ[\x0017c¸À{,à\x000b0p]\x0006DåldÀgo\x0017^­EÞº\x0018ÃáK´\x0015'e\x0005\x0007­ÔÇ¡fïR³@Ä\x0017ßFF¨$À\x001eÄÔ1ðwnóFùf¬\x0016#o^ÿ/í+Dÿê\x0010¹­\x001dcü½õ\x0001At¯Oé\x0005&­4}ÌJ¹mÂiã	S%ã)\x0003ÑJjé	D[ê$plPÊ\x0019½?vVýO\x0002eæ\x001bIm~\x0004µ\x00176ÕùÞlêNÒ¿<­7Ì×x>
IúøÚÐ8ñ\x0010pg\x00154­fðÚÑ%\x0005n '÷§ë¯7w\x001f¯\x001f\x0017ï\x001eÖ¿Üüú?\x000f×»²x|ÐÍq
S&á8§Ì±Ñõª£÷«\x000fÇou±xw¾üáxu¾ºxR¢R\x000e{^`òI\x001bÇ\x001féA;$L\x000e©L	¿7szåò)\x0004s"}z$È
é\x001ePgjPH³¶ZÇ\x001a2ez2Æ÷[t\x001d\x0002jq.!\x0002\x0019iÞ®¡ðüænýã®üN\x0000~Ü´8ºx@?úüÈ%T\x001f.ß>ÙÏ¨¢D\x0015}¨ù\x0008\x001aýRE% ú|ïÙ\x000b©,Ie/)'½\x001f\x0001IüDjÈ1ñçåßPUªúPÝ ë¥iÍ¹RcWWoBÕ%ªîAµPðor`C\x0014d/±b?¤¦$5}¤yê\x0016ø|C"Õà¥ÑjKTÛ÷ý\x0001\x0008Q):	¦¤gcô~¬êJT×
âx¨_£\x0015Iñ\x001aa*¾\x001fWåKTßjs»NçDõy ÙËþ/F+ÿg½V¥\x0004¸×1 âÔ0WøY¥ý&Öú¬ê;¬Â¡êùzÈjhqf/WÕxÌÂTV'qÑ5ë\x001exó¬\x000ew\x0013ku\g-L]\x0003*ÏÊ6\x001cW3ÄáØ\x000fku^ç-LÝZî@cÀ"\x000cVý\x0018âÿ¶\x000fÖêÀ\x001a\x000f]Èê<\x0008eFVm±ª+ø|õj?ëµ:²Æ\x0017&²ê¬³\x00068£ÈØ,÷¨ü~|Vu\x0010ç\x001aL]\x0003¹},êÓ¨\x0015ò¯±=ùâZM¾\x0000þæ\x0015#ó"gA®\x0016þæõ!ÃÛï(\x0005-b
:ßµ\x0016×··×_×{ØÅ)BÍâ\x0012<BÄ\x0014y\x001c\x0016#y!ºi-\x000eW''«\x000fË?¿ÄÈMÙb\x0001É¨\Ù)=ð¨ä°¹×\x0008MÂ
ÞoæbjUcB¾¦\x0011¯eÄÜiLÿA\x001a\x001doYr4r¼ÓÊÓÊfN\x000bN
ü-ØNøüä¯¶ß¯0ý\x0008Ó·c
]Ð\x001bA×+HxbQ£ÛýiÁô#Lßé O
e¯¥i\x001c0ù2×Í^ ÷_rFùÿæ¯î)å'CÐC¶\x0014\x0018\x0001ê:\x0000ìÂ´¢Æ´â5~u;ÚC¶g\x000fýöÕÖß_\x0017&\x001f6áQ\x000e×»ÝU%\x0003\X\x000e\x0007/ÞXÿh-M¦ólSàpù	8¢Ä\x0011\x0013q@k&)	jÆ´Ô¿ã@7¥\x0013G8r*<ðÙ8$ko\x0012
¶Qø;F4j*MÎ\x001eq\x0014\x0019F=Âöáè\x0012GOÄ\x0011<ª,/Ëá[möZMÄ1%#\x0015\x0014µuH:À:\x001bõí\x0013qlc'â¤\x0019Ú	'w¢Øgëôâ¸\x0012ÇMýXzÐÀ:Ø­g\x0015É¿z&6*¨&âø\x0012ÇOÃú`,©û\x001cµÉµs­SÔrÌ^4\x000fL~¡µ¬\x000f\x0018ÇK*|Û¢\x00048§öÊ\x0013Ý2\x001d«ás)\x0012Ûr\x001fìÜ[¼rË|ª_fä\x0015Õ¦\x000eUüÉN¿Ã+§Ì'zåX¨?,\x001eÚ3^\x000c~°óÌâ[æSý2S\x0014Ñ}°CÐr97;\x0004'òT~OtÌ\x0005·Ã!J¢UyjUÿ!Ê+ÇÌ§zfÆrU©¤7ØåÅÜS9f>Ñ3«pí"\x001aI=wÆ±Á::¯\x001c3èáÍ*»B#0¦Å\ëTOõÌÆ\x000fç$ÕHc\x001bdÊ3YùÁ6¨@ch\x001dØf£u"LåÅT·lÔ0èSfýÊ,\x0003=Ã8u´<Ñ-+\x0007IÈ%$ëä#]u.dQ¹e1Õ-\x001b6¸eIêSÆðÁ
vâT^YLôÊÊÅZ\x00002Âmn3Ú¨°S9e1Õ)N­\x0018¬\x0016IÖÎ°NåÅD¬`\x0016Va\x001dG^p¾y*§,¦:e-ª3\x0014?\x0017;y:\x0003\x001eQye1Õ+d¾ËöÁÛ±z8³zwzåÅT·¬ä\x0010\x0010R¬%)®\x0019á»¬¼²ê¡ÞâeCj2¦àÙTSÈS9f9Õ1KKå
1~G\x001eÒ&\x0011¢ÊÊ1Ë©Y©ìM>·\x0018®\x0013½\x0003]IÆÛ:5¼\x0018q>|4NýV\x0014\x001d!½É\x00151¦\x0012Ó©~³«dcª°¼§bC\x0012Ã
§0QóÁ\x00014ï87nqeëÌO\x000b\x0007êþðÓ;È\x0018t\x001aQohVÃ-*"«çVbÍèÛ+øÇ/Ó?þEHQBvÈ\x0010d\x001b!qCr/é-Vm-\x000b²\x001d¹Ø\x001eþWÌå8n\x000fT%£ê2$=À\x001cU\x0014
=aú=@ê\x0012Rw\x0019ÒÐ\x0008C\x000e\x0008ST{»­¦\x0011Ñ¦Ã
ª\x0017Ò·ÎjøÁTÌb·ös5Bº\x0012ÒuA¢/ü¡Ð\x0004I%·^l+\x0007oÝ5[t£JûWµyÄ\x0018Ut¡3Âþ\x0005á±Õò<Ír5çÛó±.5ÏºÔËÇo\x000f÷w÷_¯\x0017?Üü¸SÓF\x0008ZIË³Ht\x000e8GÍ|pÞ,/.ÏÏNÏ>¬\x0016?\x001c¿Ý)»ÃÇ:Õ<ëT7 #®0>+¾Yã\x0007½yR7#Ê\x0012Q¶[qÈ:?\x0008ÜçÔ\x001b×fDU"ªfÄ¡ª.¸\x0017.­7Í¦$4íF©D(òè\x0002£Wmæg["ÚfÄà\x001då°\x0014QÁ¹H¹êÍëk3¢+\x0011]3"V¢EaÒ\x0010Q¦Hoæ¨\x0001}	è[\x0001!ñ(³	)+\x000bÚdÂÙ\x000e§|\x0019§[>s\x00164\x000f\x0017\x0002Ô\x000f
ç¸q«kF¬Ýv³ßd;ßNÎéÛ=|h^ùmÞì¸A3H
*\x0005[±Ô áõæfÄÊoófÇ­¬§~\x00130£¢i2;n15V7{nUH9!HÚcÎLçG¹}Ø±rÝ¼Ùw+¯ò\x001dßç±\x0004åWð-#%\x0019+ßÍ·JÒ"é[«<\x001arkjsP3cå\x001by»sÔ*×Åxq@·ÿü
¢õìóETG´{\x001e¥HC\x0003\x0010qD÷ÛC !ª]-Úwu\x0019Ið¼cD~¢Ðj~°ã\x000b­ x\x000e®O\x0019vÀy>	=\x0015#ìr,+É\x0006YÉw×÷\x000f_®\x0017\x0017ë»\x001fÇ\x000b{×@><*\x0008
B¦Ð\x0019\x001fÓí\x0005\x001evGxïVgçïVåéÛÑD&^\x0015,Ñä«BÓ%~Uh¦D3¯\x0003Ík\x0014]®Qüñzqû¿ÿõßÇ»ÓÄÖæ\x0018FÐócÃÝÓn*I®\x0016'ãÝ\x0019Ùq©¢Ë¥Ó¨\x001cËYâààhÖ.³9l1Ò ±d%\x001b±°%Ö\x0005çÆh"y~§Þ¼ÀM§R%j¡2ùµ\x001a.\x001c\x0018øáZ¹9!s:.©t\x0003á´Å`d\x0019\x000e%	§+Ý¶é{OÆ2%y-Æ²%m1\x0016\x001b¦q
\¾2ÚÍg­éP®r-¦\x0002±Q¡Ð5\x00087PÍp
¾¤ò¯ä\x0003¢CãD× H\x0006ÚÁÌE]Ïsdë¶Ì\x0001ÌU»÷&ÿîèÅÔ	\x0001#]\x0010b°Í+ÁtªÊ½ó6ÿ®@'*bA\x0015/QÑGôõ>S±\x001c¯\x0017<o[ò´9â>Ä(2ÝLÅN\x0006\x0013½h1Xø<R{Pw*sõN«Å\x001aæóôÇàå-q
®kÆ8zPÑø Òt\k:®-J³ÃqM{Òn\x0019¥ò"`£¤ø\x000b
nâhq²þt»þüÓÎgpÆitõ4~µ#é9¿eÊK¼\x0011-N'Ë£÷\x0013\x0000e	(\x001b\x0001¥6ôô\x0008~Æ\x0014\x000c\x001fZlxÿV@U\x0002ªf\x000bZ\x001ae½ÉÓ ¼ÎyÖ:V>]òéf\x0003
Ú±Õ¢\x0019LÂ
Ùþ
\x001f×
hJ@ó
 -\x0001m³\x0005³T(,AÌ¯ji\ÿF\x0004Ù
èJ@×
è³\x000c¿M±R\x0004´.\x0003úäj+ /\x0001}+ âC¶MA\x0007\x0018OsÀ58\x0017p\x0008\x0000B¦éÖçâVOÍº!°äû3!¯\x001c5oõÔ0\x001e"@¯\x000f¿*;ø³°òÔ¼ÙU³!"VTÜ ¬\x001c\x0012³MXyjÞêªeX¨¼Û[¼Ý¨ìg´ÍWyjÞêªÃ&\x001bPÓQ§\x0005ó.ý+OÍ[]µ\x000cV£Wàª-\x000eÖuÃãÃFô×
XyjÞêª\x0015ðXLùôò $Ûñ*Û
XyjÞêªbx	âôð.ÃåâÀÍ\x0007¦V¼ÊOóVGýÛÛox\x0015á*}g±¨¼ hõBy\x001aÝ\x0016_\x0011q\x0017\x000f/tÙVÀÊËf/£\x0004\x000e¶YOÏÊ¡ w>`µEó&n\x00164H}¤m2$]çÔÒTÑ\x0002üÚjC]"â\x0014Qée¸)kEÔ5bógNm\x001fÙ8lÑ)»'+rãF§k=Op¤\x0006yl\êJ7 O\x0005äÖÕÏ\x0011á/ao\x0017ë»o0däÛO×·×_ÿ¶ãÅ$ü\x001b©>\x0017¦Ù¦F\x0011\x0013þÿgiÍJ¤·Wåñé%\x000c\x001a¹|¿:Y}øÃË¨¢D\x0015]¨>gº¥U\x0007&)¤pæiÙöií¨ªDU¯ÒªÌ[À+ÆÃ\x001eß\x000biõÃÎõéA\x001a5U2\x0008oi0oÚ9\x0001CóÑ3\x0012>'ËóÝ\x000bÞË`N\x0011h7ß?=<.Nîn\x001e\x0017\x001fïï\x001ew¹¾Û%å¤«F§`âK[*¡\x001a»ó£³«óÅÉÙÕñÅâãÙéÅâryºK\x0001@e	*çrª'Ö0é
Aë)¹½ ª\x0004U= C5±å.Ïf×tOpn/ºäÔ\x0006¥Æb®ò¼ö,í\x0002øû\x00005%¨é4(ujBúXAéË[¿\x000fN[rÚNR72äÉ ´\x001c\x0017ûàt%§ëµ'>âN[^ ìÉö\x0002êKPßeÐp]¤\x000f/(ï\x001d\x000cJcìH¨­\x000f´;ÅÒkYI1h7\x0001z0)í¥Ñ\x0004^ÒÚÝ÷ù{K¹>\x0003\x0017 r£ô¾çÜÇÇ/ff±ô¦6Ç\x001ac²Ã§\x0012n§ö²xu0ñÞ	GÞ*2¶`iKoN½|üÊãó>¯iü\x0001)|òøyfåû\x0000­<>ïuùø~	/\>ÜY7\x0012ëë$­|>ïsú:|-©1Ø\x0014ÓªNø½|üÊëó^·6ÕÞPS°)õZ·
U¹}Þç÷ÕÆ¯\x001f¢{G\x001b¦8Áö±NEå÷E¯ßÇú®àë)g\x001dlJõpí#6\x0011ß\x0017}~_cnØÀ¤e:J9ù(¾ JTn_ôº}¼ÓÃ¡/ÈíS¹\x000eHJï´òû¢Ïïkz¹5£¦xiS¨\x0010Þ\x0003iå÷Eßÿçl¨Ê>w+Â
Óù\x001dÍÒ;uf\x001f_TNJô:)òÞSBIº­/«­/û¶¾¢Ú\x0016íUAJí­ÖìcGÉúß·£þ)ët495fNà/ú.(4BÕÞÓpãón/¸në:qí %Æ$4H/~jÎBX|yã_Â5`,Õ?qrnp¨Xhn­ö\x000b@õ¹%Û+^ùJ}Ê Ú\x000cëJØ±VÿTXOqÊ\x001c4¤¼Vb­µ*E}vl33vT\x001c\x000f)oúÝÃúî×ÿïþæñzñöþöÛýld¬½K_\x0004?
e|®E×bSØî»óåéÑÙñÅjñöìäòlG¾\x0014\x0011E(\x0011µÖp%y]îñéÆ³\}ªÕf^·Q²\x0011\x0002½ä¤¤p(wé¦É¿zK+b3£*\x0019U;£WÙéò\x0014\x0000ý`Äùº\x0004Ô\x001dkÑSà,)Ö"-F¹)gÐÌhKFÛÁh)©#,Ã{½gyd f|ã5»Ñ®ãCçiBÓC¢gÀ³\x001båÚÍ¾dô\x001dv4Ùï\x0008ñÙ1È¨7k[\x0019wð¬cW[¨mL\x001cÿMC¯Új¨A3díÀÛ=x8©3$\x0017\x0012\x000b¤Ê§Ôf	R3dåÂy\x000f ¬ALE> ö­³%çCV>w8q\x0010(Áá\x001a\á#M°¤Íkr³\x000fº\x0019²ò¼ÝIjmHí>~n¤Ñãj³ï´yoW¡p+¨6½1´@½
á%
Ú«¤#Gðb©¨®ÃÃð\x0017q\x0014èÍõÓâíÍ7|8#uüßÿúïÕÝâp½cr©Q°\x0006ián¦\x0000s©v$È|r¼ºZ¼=¾Ä÷ã4]w±:]\x001c.`±E-þe°e-ÿe°U­þe°Mmú±ã9\x0002\x000fB\x0018ÈPà9FCÌhä.ìçn$\x0019ÛØn&¶HùIaBPMÇ/½¡¨Q×\x001cl/+løuÞ2Á Q)FsU\x0015Ùôè:Û×Üþ_\x001c'Ï
¿÷¯púÑ8g\x0005-w1â
\x0007§iík¥p­*ç\x001dA\x000enlª\x0006ÒÆSÑ\x0012LjÙ\x0017¹55¹áT Ýç\x0000oÚf_È\x00045QÙQeØ\x001crË«'þÞOî ý°ìðÆåÑ\x0014jÜR×Üðî^+RÓ(=é(±\x0008Úí¸ÆGêÒ³¸M½;á÷\x0019k\Æ\x001a²\x0008n<Îº\x0000ïKÜÉùK\x001cÒA£2á³þÁÓâÃúo\x000f7;\x0015]¼\x0018&02NÐ\x0019éÜfúÛ«\x0005Ù:Þ¥åB\ªäR
\Î
2Õá¦\Üå\x0007o7ÂèI`¦P\x000eE\x0010\x0016\x001fo×wßÖO\x000f×;Ø,ó±ô*ú]C\x001dØÚçK£6Ç9\x0005¶'ËÓËåÕùj\x0002-ñl\x001b^¸^Bæ5áq\x001a>É\x0006YÅ6e\x001aÚð|ç\x001b­Çtì.Y:n¡E7×v¼²\x001do4Ðö\x0003hÁ¥IÐÑN¶Û¶êZè\Eç\x001aé¢H\x001cè\x0004ây\x001aiÔfÛK+_õÂ\x0018söTLÈý\x000fIþÔpk÷eEP»-\x0019ÅO¯c
23Vc2f#±¾ø~ýùþÓ\x000eç\x0007ÊÐX¨)=Yí÷ìóÄâûåÑÙá®jn>JmÁË\x0002¦¶\x0002×_®\x001f\x0017\x001fnÂ¿ìÔ\x0001ó¸%_IT!¿Iy»ql\x0004°ß_­.\x0016\x001fÃ¿ìxâABY\x0011ÊfBµj@/\x0018\x0001)Àô£÷È-/PWº\x0011Ð<bÀ
ÃÜ0åÄo>M´\x0012Ð´\x0012Â³\x0013¶¨Ü æHgÙ³-S\x000b[	mEhm(èÑ\x0019¡@5ü\x001bálBSe\x0005\x001dÉ\x001f62`&Sj>u\x001açQÂtÌöËË;z\x0003T´BU\x0004v-Â¶q´or«w³Aí\x0006¨í°¨Ü¦ýí³zµß8\x0007Û?ü0[><üÍkùð¸UYÌaøX\x0016ó}¸±Ä ûfç§v¶·d4i7|j6<WÙïá~\x0002\x0011öñóÎ\x001b 3®`_'BWÄÆ\x0001¥5Æ®\x0016â\x001aJÆÔþ\x0016¨Ü©  Sq\x001a\x0014(ÅÒÍ9\K,IhÓ¸ìÑ\x0010Å\x0006¦ðñÍ@\x001f\x0010þfâ7Tn"i:aì\x001b¢Õo
%Ùó!\x001a7ü©Øð·¼½½*=\x001f×·ë?=<}¹¾ÝÆ§êz	Ú¦éK
G1 Võ³Òòäd\x0015µz>.Oß_½[L\x0014%¤hi¸OÊµªÜ\x0003Í©\x000c\Y¯æCª\x0012RµCB)\x0018=l«¡/,©l}\x000ewZ²û£5ãüFVe¨hQXKâZ²¼æz\x0006«\x001cP¿(E(×\x000f×a·Ý<î\x001a0îU~\x0005oø,gM­ß.\x0008¶\|X]\\x001f_ì*Sã\x0016?YÉQN\x0001táßDò$Úq\x001a\x001anõTI
å+3\x0001U	¨Z\x0001µ8ph@³\x0014¹¹Öws q+.ñt+\x001e¼Àbé$d·\x0012\x001f\x0015\x0006Ø-¡A++ñ\+^ðn0\x001f\x0004\
µÒ|.`ÑÆ%kÑÃ\x00064ô}Ãå\x0018¿/ 
üsW\x001f¯ö/oÜÀ\x000e.ïv°\x001fñé\x000cÈ7.N­¦\x00024Í\x001eFPA°&\x0007»^ë`¢m9LF\x000c\x0008µx÷\x0012$zk´VT°-¶¤Ú\x0008Uå\x0002U£\x000f´p`&D|\x0018=\x0018áÉm#ÂçsæP¨Ê\x0007Â¯ËP\x0008\x001aevqN£µ\x0011\x0007m2au$'3jÿï;6\x001a8ÆY¬r>¿ú\x0016\x0011On¾Þ?ýu×#ÈòËÊyl\x0014¹Ó\x001bU\x000c]]&¾ã\x000fgWÿö"ZÙ,&Rºu2¢G¬Àu$?\x0003sèåiTÙÆm±C\x0000ÍÆ=2\x0019.Ö\x0004§Ïª@úÃ¤g1A-ëF$?\x001aé\x0006YD\x0017u]&Ó©àUH\x0002Ä¾ãö
ÿOçW»ÑëÍd:ÃG\x0013Ðæ\x0018è7\x0003ßãB..®o¾Ü]?=ìx¡3Þ\x001azøfTkGe-Êo*¸C\x001aøø(^ÀÆêøÝéêêüù¢Ì+J^ñy­\x001fÙ\x0017Þæß¼9þúçõã#â?¬Z\x001c^?Üý´~øñÛ.\x000f\x000e9\x0005½©TJÐpdwm½¯?|\^\4þùòýâpu~ú~yþöòePYÊ\x001ePáÅ0$z\x0001TocY}\x0018v£ª\x0012UõÚ\x0014ÚÚò\x0014Ù\x0006R"Â*ÁçºÑ\x0004\x000eîL±».×\x000f®\x001fwõX¸\x001a f¶Y!2=R`¡ØffX¢ËóÃÕÅ\x0016L&J2ñ\x001aÈØøNÊª;éÑúáëýÝ·pkÞ©ÞÄ\x0018m¨Þ"XÃ\x0014d½õÒr´<ÿpvz\x0019îÌ»¤ÇW>V]ù¦\x0001rg\x0002 æå0£Ío»ó5ñÏ´òÁt$ôô4³TæãÐë­ªèM®\x0004t­Öæ)ò\x0001¾ð &\x000f\x0016ó\x0000ÂÿúÖ7\x0010Ôý@Ã\x0018L¸M¿°Ú$¼upiijÜ%)1"Ì0ÙÄm»6\x0011V»7o\x0013áI¨#ÄÿÔ\x0007-´Ê6ôÛn\x0005MÕ>áÍ\x001bEHÛ\x0003B\x001e Ù¡}ÛJXm\x0014Þ¼Sxr\x0010\x0000Ì\x001bÅÏÝ(¢Ú(¢y£\x000cÇ\x0000èq£\x00142à³µ¨Oæ\x0002k\x0008\x0005ìHÈ=}ämS>Ú|aõ'©\x000f·Ò(Xäph:»·ÃÈÊîíÌ¥\x0019ç9MQÆýâÃúá1ü«\x0011;SuÆï)ÍIuSÀ\x001d\x001cÏf\x0012â*þÃç\x0017é\x001fþ"¡.	u;¡§rT%©KÔrM"Rn+ßk#4%¡i&d4;U\x0018çl,úìà\x0010·É\x0013¶\x0011ÚÐ¶ÛPÒt@PeÆØç\x0017Úoªm7#º\x0012Ñ5"Z¯³O!	¸U¢
mØé*­¾DôÍ rï}Ö0=ótÒvS$µ\x0015±Ìk!ÂÌè`ä§Ë1
°
×jêlÔ~Su»W¼1\x0018\x000fe1\x001dÐ\x0006QÄ8PT¢Ð\x001d>IÊÍzI#ÓÂ]`ö.´ÈQ6¯FÁAõ=2rICr/\x0013Ï$ z\x0018+ÇÈ[=ã?\x001békFÙº¯CüÀéâ" U/.r{úHÜ¥Òòê¿·®I-\x0007\x0007)pVñ¹ 1dówvýDöNQ\x001aû*>»\x0015ãüb¸Y©÷|ýõþé%-X\x000e\x0014\x0008!ûçÜ8ª2æ¢>\x0010\x0007­Þóå³«ÝB.\x0008(J@Ñ\x0008¨ Ú'@§Q\x0019å\x0012à(ùÝ\x0003(K@ÙjAhj²hAN:ç\x0014¹Í§J>ÕÊg$æ¢\x0001iúv\x0001çòÏ4òA¶$\x0015vÂeFïIÐN|p_	èJ@×\x0006h½að \x0000ÙAº£2C!#¯\x001bbñ8\x0017bÕ\x001c÷0LÒ[7ZÑË\x0003ÜÆZh¬T\x0014zs)ç\x00193«ÿx]Q¿ysÝºW \x0000?m\x0015IwU=ìea{)?á_[\x0017ã\x0000bh\¼~\\x001cÝýút·~ú+p^^?<ÜìÄ40 ZS@W
mä¨'Dèu=ÛÉêbqtöáÃÕéòêß\x0000÷ru~~üöùwi¢uª¤´e\x0007-ôL¥CFÀ|ödTo±\x0008ÆëØ¾¹\x000fX]ÁêNXD" äU\x001ei=Ñ²:,ï§5\x0015­é¢uI&ËªÜFÉ9®W¯U]2Ø\x000fk+XÛ\x0003\x000bË\x0013\x001b5\x0004tÐ31T\x000câBÐn?´®¢u}´Î\x0003b¢òH\x0017­Ø\x0007kÙ\x001d'Ì§&ìÀ9¾\x0008Å
ÈsÇV`ÇÈ#Ô¯q½¸ºv\x0008ñ÷.\ëðÚ&ày\x001e\x000bE!y)È½ðzSóú¾}æ%¯ ÂiF<3ÍÒF3uqs/¯Íú§\x0017~ïã\x0007´\x001a4*ÔÀ\x0011¬ój0pwfÜ\x001a]ã>§û[ãèÀA câ ð\x001f\x0002¿\x000f$\x001fÖw×;J\x001e`\x0004\x0003(`\x0000¦ÐþÀFL%\x001cº!xØ^óayz±ÚÕ8MtEE|ëV@\x0001z\x0012\x0000J\x0002Ü÷|]©ú\x001eÇ`ÖCº\x0015\x001fÝß^\x000bx×÷w;Üi¸±Ñ[\x000f\x0006ü(B7÷M\x0005Á£³Õe@<\]\¾Ì'J>ñúødÉ'_\x001f*ùT+\x001f>5ªpÅä(w'è!Ï¸Í.ïV:]ÒéWf=n«v\x0007üÞÈIc\x0013ÚQ Hü¾³ÙÙèê\x0005\x0018oD\x000cÑ»¢Vj\x0006B°ÑMØX¶ùodä¢fäíûú·b
ëÒ\x001d©ÆGï©Üü wª>vÿt»~XÞqS\x0017ÐÆ9¨\x001fHES0\x0004×¡Ü4 ÌÇ:»:Y/^F\x0013%xUh²D¯\x0002-£
\x0014ò°ï\x0017´U¾_?=üú?;\\x001bþ\x000f°ÆrÿI*a\x0000
2,¼Þ|Äj*ßCïþ®3\x0017ÑD&ÚÐ¤È#0FA\Ë89eëØfSw\x000b*ÙT3\x001b3këiv\x0014dß©­ÈÎcs%{Ule¯¾\x001czõ§Á9m¨
 ¸ØÓ\x0006o\x000bôQÝ8i§Ã=å+8ø½ÉvÜ\x001eh/cøÀr\x0019øf3QÛf¨µå¢©|"ð¤Ë\x000bíX8Åñ\	¼ÙÍ6ðS\x0008·!÷\x0012\x0013\x0013¥~wrÿôç\x001d»W\x000cK\x0006E\x0008R1­Ò v\x001a\x0003w'ëñ
Iéäìêã.\x0019)@Ò¥È[@ß'"+o*ê\x0017Ö8\x001cL®4Çñ\x0004~ìÚ
¦Í/:¡ÖS±ä\x0001Ry³J3ìGô0\x0006·ÊU\x000fúÉÅ\x0007ý\x001dr[ï×O;£½2á,H\x00011S\x0002\x0017Â\x0010J$\x000b?Êy>'¸õ~yõ|t&×\x0015ùn³×En+òÝ\x0012g¯[)kr¹[\x000eï%vË¨ Á\x001c _òúX\x001fåïv²?/g#c?\x001e<t,Æbe8Z?|^C}·3ç,&

Bñy¦ájþÙ¤£åùÑ\x0012âìÓ/:jTx\x0001];\x00184ß|¹ÿtýð
:Îî>ÿ´£ÎÞÀ{\x001dÎ\x0004°Rá;¶*s%içÇïÎ\x000eWçÐsvzô~Wµ½\x001dÏ°Q\x0000yùËuøÿµxws\x000bï@\x0000jgòp\x0016r¡ºÔíH£yùÃê4`¾;>\x0001ÊÅwp2í`t#\x0001\x0005Hc{|÷ãÍÃzñn}÷ãO7;\x000eMît9l'ñ7üC1æØ\x00089Oß\x001e/\x0017ï§oß\x001fï \x0003\x0005-nM!À\x000e*i¦*\x0012øîöúéáæï;5´@\x001fFÞàç¤QÅe½}w»ïNVWçÇÿ¾SæË¥\x0016¹¡°ÏÅ\x00169[B^Ü|zXï
<Å
\x001eüQôS©h¤#¹}\x0006ðâøð|9ìhú_\x0006¸Q,Î¬ûy\x001a"®#øÖ<8Ñ¤·ï¡1_ÒÖsó¶\x001dBÐcé\x0004§Q0ã×\Ç&´p-üóÍ®\x00064Çlî%Þ\\x0006\x001fjüFU6¤îp\x0001\x0017ÃÇç»øüÏ'¾´±¸ùüíþañþéË\x000eíu§¸£kD\x0008+éC
ªíÊaq_ÿp|tyv¾xõîìe@Y\x0002ÊV@éMµ?\x000e&\x0012\x000bW°!\x0000Ö\x0019§\x001e@]\x0002ê\x000e@U~\x0002\x0001%i~º¶½\x0007Ð¦\x0015Pp,¼ºO8\x0013Ïp\x0005ªê¢\x001e@W\x0002º\x000e@L\x0001\x0010ä	
@çfb_\x0002úV@Í¨d<\\x000f©"Û(zf
ÿP>\x0013°¨Óõ©\x0013©Ù8¥Í	AÕI¥	keª\x001eB^\x0011òfBO\x001aí\x001d@?CZÊÁ³ý\x000c¯\x001c!oö"Wcs®0!5ìY»-Âi"¬<!ovBçB)H\x001fÊp:ý¨1 PUªÁcê¢Ñ4ÉÚ3uÑÌu¼òÕ¼ÙY\x000bEúï!vd\x0006ºÍ\x001c½\x000c+gÍÛ½5;ÐCÛ(ùBz\x0018ð£\x001e@[\x0001Ú\x000e\x0013âð\x001bÇcs\x0000\x0008­½Oªã·'ªí­3ð\x00164²¡}"óê<áÍ\x0007J°!N¼±NÓ@]Þ^97PT\x0007h>P¸§×\x000c\x000bãËh£Þ¯z6au ö\x0003EÒÜD'<ÞÈ«Ù'¨#ëöÐ\x0008]\x0008¨i\x0004½aÙÂÌõ5¢:PDû"É×ÀGVôIs$|äÙ6¬\x000e\x0014Ñ| ë	¾Z)³
9£¯<Û]ê@\x0011í\x0007¤QÖÄ\x0001©hBÚÉÏ&¬\x000e\x0014Ñ| ð<\x0010ªF\x001dú\x001aFp\x0010^Ï%¬N\x0014Ñ~¢\x000195Ë\x0004\x0003\x000e»dîq"ªãD4\x001f'\x0010
j4 \x0015\x0006ö³íW&¢ý4\x0011\x0014uYm±à\x0001LHDÈ¹ÛXV§l>M\x0018\x0007H\x0018\x000e\x0016IÝ1¤?çfßduÈöÃ¿9«Ñ\x0014Ôä!¼~î
TVìÉÓÐ°è\x0010uYÚ&y¸µÓsý¬ó4í8À©(j\x0002 "GÈG2¦\x001dÕY"ÛÏ\x0012Ï\x0012æ\x000f¥¬Èlö*¬\µìqÕ\x0014\x0016ë7cBkg/ÃÊUËvWÍ\x000fp\x001f\x000bCb\x001dá#Ó*ô³\x0003\x0006Y9kÙã¬9
ç\x0011ÅG¦©êv¶··íÞ£\x0016§¶F¹hÞwØ(sM¨*g­ÚCÿ¬eê9Î\x0000\x0004\x000b"Qs\x000cªòÕªÝWs\x0008\x001cKó"¤OìÜ\W¨*g­ÚuÖò3P@>±½\x0006Uå«U»¯Î¹.8MEM¨çºBUÅÕª=®æ9®æ¹w,\x0010"ìhÊV\x000faå
U+ähCf¨p­ ´vöF®|¡j÷\x001arÕ©´NÒa4ë\x0003\x0004Ì%¬|¡êñ$ñÅ\x00046¬
Ésùtå
u»+Ôthx¤'_HïÖº¹ÎPWÎP·;C]
´ý¢\x0001iø\x0016</Ï\x0005¬|¡n÷\x001ew´\x0015X3RPÛÙU\¨ÛãB\x000eÓPñ\x001cû3º>Yág/Ãú±Ù\x0019r-ïB!°85;ìÒUäªÛ#WAïOçîsC
,Ù¹ÞZW¾P7ûÂ\x0010ñc½}8é\x0015ÑgF3H{\x0000+W¨]aøÆ8\x001f\x000c\x0006õèüñ\x0013ËÙ.SùBÓ~÷\x0014v)íHÃÍ0Ö³C\x0006Sy\x001aÓìiàRí=Ê\x001dÐiGEîFé¹'SE]¦9êâdsÌ*xÃ\x000b#ÈäÍ%¬b\x001aÓ\x001cÓð<×Y+Oì	åì\©¶±iÝÆÒ3ª\x0006}38ØÅåÉÓLÏ&¬ö±ißÇÊA¢s.fdC1w\x0019Ú*d°Í!\x0003\
µt`N$¤B91ûD¶ÕN¶í;YR´®'Ú»,6ûg«­lÛ«4ÌH6äXàmT9f`³¿r\x0015ÕØæ¨c+aê´\x0007\x0013R/¡õ·UPcÛë¦4
4×b\x0008\x000cóTp>ûýÎVÎÐ¶;CC9aÍÕP+@\x0002É &8°ò5¶Ý×¨|$\x001b\x0006S¤0)LZz¶¿v¯qí¾FRÉ
´³q¦¿6nÍx=×`	\x0015JP3|ýxóãõÝçëÅ-4d>Ý}»yØ%s\x000e}p¹&\x0004æä¤èµÏ?£Æ½ÕÅñÛÕéÑjq\x0002]W§ÇçgW/\x0012T¼bPYÊW\x000cªJPõAu	ª_1¨)AÍ+\x0006µ%¨}Å ®\x0004u¯\x0018Ô þõæJÙäðÙ+&­¦W|6ñêlâ¯øpâÕáÄ_ñéÄ«Ó¿âãWÇ\x0013Åç\x0013¯Î'þ\x000f(^\x001dPü\x0015P¼:¡ø+>¢xuDñW|Fê\x0012¯ðúÄD¸ßqË\x0007å9(¡ßß\x001c®\x001f¾ý\x0004B¤_v5×\x001a£,¾xæ\x0018YkÉL$!µâìáòüò=h¾;]íàúÖ<ß\x000fYÔ»ñáý\x0003tþ>\]ÎØ¯ÿø¶¾y¸Ù¨A\x0019\x0014H­À¹ÀJY}øZÖqgçÐü{¾ú°\x0004Å±Õåòøüx\x0017¬\x0002¥\x0000Á\x00079<Pâßß\x001c>\ßÜÆ&Á·×_ïo\x001ea²Ç®F\x0003Bûé.ïatb\x0014\x0004
ß\x0003;¹ªë»\x000eÏWÇ'±OðíêÃÙñ\x0005Ìöx¾W\x0010Aµ¶\x0015(üÞ\x000c\x001aË/\²©Ð\x0007&5°;\x0019lZ\x0017)µêºNé\x0010\x001eÏ NéhýõÏ\x0011óÃýÃ·\x0004©FU*x²$Ca\x0014ï\Ý`´üð1â}8;¿|\x0019L\x0012\x000cþQÁ¨Á-@£*¥5Ad\x0012Wc\x0000w3Èò[w$·îé&9#iÀÿ&z®éZW\x000fËh"ãÚº,þ>Í
\x0007e\ñs
½¾S2Ø;_°jdóºfQIÓí&5vÏ
g\x0004Êð\x0006oEÞK1Íä\x000eÄ\x0016[&³iíq¢ð\x000e\x00100\x0016~Sïmÿj\x0003]\x0011[Ý\x0002 h7'±Wß3eMó\x0019ëÍHS³A!æt6h\x0019J{Á)÷Âv^/8ïB³Ñ\x0003óB\x0014<0DÛG÷ß\x0002W8Ò\x000eoþ~½¸þ¶x·~x¸ùò´Ë
\x0007§á±U_2¡°ÿÅ\x001ep<}áE¿æ<».xqxüï«Åêrñny~~üîj§/Ff3b6ÌP´O·
*kÙÚ¤OËYTKÚ\x000f³å53<iõÙÙÆê³hgÇóp\x0019D\x00199\x0007Ë^ð\x00153üÞigP±Ç­\x000fB\x0013\x0011Ù<m2³`ûB.\x0002\x000c\x0001EY\x0014ÄfN
\x000cÆÉ$Ä¡Ðí	Ø\x001a\x0018Þ&û¡ð
÷cøj\x0016ÖEÝÝÕÅ\x001c5=x!Æ\x000f\x001e<Êñ¯á\x0016ñ5já¼{Xÿ²+P\x000f\x0011/\x000e\x0003\x0011cKm\x0014Ãm\x0007Õ;%êÉ\x0012.\x0010\x001f¢\x0010Î»óå\x000f»\x0002`\x000fVeU¡ª!Vû\x001c=\x0004hÕëSf½É3ÃqÔAÅÆ@eë9¤Gçág4äjçý\x0006ÉäLN'N\x0010|Êaç±®`ÚØ~2Îk2ø}:YðD(`'%}½°a°H;Îè&¼&nÉ_Så!ë2liüÔ\x001f G\x0015.\bÄÕ°Ê@X	± AâÉG2Q Ö\x0002¦®Àà÷É`\x0010c¸ô\x000c\x001e,J°ÆÔÔB÷i_AqÌô}É0îæacB=Fü0¤fýd×k\x000c~oXý\x0002*øÉ¨ÕÈ@Å\x0003)ÛO¦jÅnöÉ6\x000bÑ¡.fØç\x0016\x0007o£,\x0011ý`Õ`5\x000cê¦Rkø7bUR8­¨R@úºzo"Y8ä`cæÂ½Ãð\x0017oâïoÞ^ÿ²¾û¶¸¸¾»~|Ü5\x0017(¬(lB\x000e×u\x000bg*Na\x0003à\x001dÊéºòñíêåéåâbuºº¸Øq4%6\x0018ÝS²ÁïÓÙ8Ïw(Çè¢½GÅ
ïT­	ÒÆ¦óã`bß'³{º¦;{¸gÕ8')ÏaÁ&k»Áï
ßTÐù$ °×bí,Í¡\x0008>O÷£\x0019_
~oø¤ Ñî .\x0004C©{(3KsjÓfU\x00165ç¦£\x0019Ee\x0002$r8¢å<î3\x001ag1¡:ìQÎÞÄßã\x000cïÖ¿Ý?=.Þ¯¿^¯wª\x0014×Å}*A\x0000P¤½`¸ã)\x000c;«òº0þâ»åÑåÙÕÅâýòÃj¹Ë\x0008Y5j\x001fB¹$4j¿ûõ\x001f·ì}ÎÁ¨\x001e\x0015mg¸%E8\x001b"´D'WõÞ­N Å;\x0015ÌW`¾\x0005yìé4\x0002º \x0011L \x0017µwká
+ß\ñ÷\x00062iñÊ\x0015L¦0&²Z'\x0005
0YÝ\x001e4\x0019ÍÔj¯0¹\x000fÒ\x001cár÷%^XNÖ E\x0018(wÍ	\x0011aÁ¥:U\x000bI¢Ôõ µMÉ5\x0018Þ\¦áªrú.^ZN\x0017 H\x0018hw\®"'·C®(rÂï­¤Ê»X|\x0017I¡\x0017?J2ø\x0017¤²î.h&á¯\x001e<2ÈôÁïoÒGÒ/;eO×@\x0001Ãö\x0006\x0015¸À+é;GqÇ\x0017]\x000c\x0002ª\x0011 j\x0004t\x001eµ\x00127\x0006´×4¹Æ<L\x0007¡\x001e\x0011êFB\x0018\x0008e0Åá}.\x0012ª\x000cX·u\x0000\x0011 i\x0004L\x001b:Ú\x000f=t¤\¶gGx¶\x0015Ïàh\x000eáÃeá\x0012ò¾ÍýÂnDè\x001a	µÍk\x0010nÖéQÓsz£ñÚÍ%ô#BßH\x0018nØIçVN¼M4\x001d\x001eL8ó#ç>!\x0004N¡&@é\x000fÂÌqd8}\x0008"ä3Mx7\x0012rs@\x00065\x0002´#õØ\x0000XGZíväªm««\x0006MÑ´OÝÈ\x0013:gó»R=Aºpä«m«¯*§C\x0018bU\x001dÅ\x000b\x0012¡Ró¡ñµ¯ß\x001b÷Ä»x d\x0007èjXvJtd©ã*\x001c>2\¾à÷7'ë?ýé>\x0004û/FÓÃH/`ijZ[O)oSßCNß}w\x0016Âý\x0017£/dÓ#6ÝÀ\x0006ºÉ\x0007eÆ ;\x0015#}n"Ú\x001e\x0011ld3#6ÓÂÆéÖ+ãaÌñ\x0016âñ\x0016\x0012]?öõ7ß\x001b¾i¸\x001b´[\x0008õuºöj©éyK°\x0019v³Ã+zdß§³
òíñ¹0
/ÔV¤Ð\x0005Xê\x0010u2q>Ô!Hi>ÔõÃ·¿½È\x0015\x000e\x0008\x000b³k\x0002L¨N¯ÔFû´Öb\x0001Lõay~ùiP!>Ö%Tü}*V8\x00180PX©UÓ\x0019¡x/e¾¢ß'\x001bK8T"SÎ9Ì\x0015;cÊoàÒ¼+
\x0008(¢wkc\x0017ý°²>=<}yºþ\x0006¯b'ë_®o×w0àlÛ
WnzöPUÞò4\x000eÙãÁ´õÁð!¬²Ãó«wW«Kx\x0015;Yþ\x0010®§0éì\x0005âp¨²8þÞÅìxøÄIlDF\x0001Þ2èð´®Ï÷1ûØO5|}ëß@åÊI¬Ixº½¹{\x0004â[\x0018\x0018ñy}wó]ww83PâÔK	^\x00079ô`ÇÓÄGNbÂÕÉñéE"^|X\x001d-O¿s]Dâ"Û\x0016½ë$\x000e«\x0013^\x001e#18ü\x0000¦aHÃ¶\x000c\x0003ï#æ¬"ON]ÈB\x00182àaä\x0005NÏ5yÌÊqÅ]È\ð\x001a\x0019~ïb¶.\x001cØ\x0006µÔ½Ã\x0019!vò\x0018ö\x0004??a\x001f¥.å!`À\x000eùxóù>n»ï®nnowL\x0008!EÛjn²ô(ÃÜ\x000e÷¶nOýx|t\x0016÷Úw««ãçGM$8n+áâïMxÂàãæðôëðQÚá±\x0004U³øQå\x000fnÓùâã\x001câ)º4&@áAàMí'¬_t 9½è|¼]ßÜáß¿ÿú\x0007pª»*$Â1y²ÙÖsT,\x000c\x0008í\x001e'mu
üx²<>ÅI¿ÿ¾:\x0007oº#'V×ÐÜÈ	¤Å\x001aE\x000få\x0012ßx,S³8}ÕSy\x00081`\x0008*?Þ?À £ÿý¯ÿ^þ²Þ53Fè<ÖÆZUÖ;\x001a âE]eýñì\x001cF\x0018-?,O^Â²¥ùü\x001b\x001b­7\x0015Ì*A\x000e=\x0015âºãYzÈõqP\x0007*ÀâïÓÉL¸2ãDIøÉ\x0005 Ôrú-Æy1~Åª
Öb2È¸\x001b$38lÅXkHäEHßK¦mm2ø}:äY;%\AÓÃµ\x0011&Ë,«º©\x0005Ì°\x001a\x000c~oXþÎà
\x0015ÓÇ\x0014e}åºÚ¼LËL·lLU°©
!lFÌe\x001a\x001cãpÝdÖÖdà*§ÛÌç\x0019ÍNÑL\x001f8+òÀ:\x0001×BæÂH\x0006¿7Ø,|MZf\x001f°TQ%\x0015Í\x0005u®{kÿÈjkÆß\x001bÈ§À*(ÃZ/Iªáhí\x0001ã.\x001eRÃÇ\x000e\x0014ø\x001d\x0006Ù}ùõ\x001f/^ùÂmJÀ\x0018Øm\x0001\x0011t$	eÓétR®~\x0004;?»z÷ò\x001b\x001d
\x0015%	\x000c*J&I\x0005ß\x000fÀ$¤(c\x0008¢Âz 0SWTµñ\x0011\x0018o\x0000\x0013^Ñ¥WX÷®@\x0019ÀFÃÀÄ\x0008L4)\x001d]B1\x00015æ\x0011ÌÓøTe¬é\x0007#0Ù\x0002fq@\x0000Q%\x0016ó\x000fW¦®&l\x0003S#0Õ²Æ(ö\x0011J
lQ0$
Á¼a1=\x0002Óm_`_fX³¤8Å>^óþ5fd½+á÷é`,Jé\x0004\x0006e+O\x0016S¾Çb±­Ëbn0$n%Í
^,áú"Ë>å¯´³t%¨cÈÃÑY«w¥q}K¸NeT¬f\x0004õã&F\x0010Â\x001caÁdéj%Bì¦îQèaä#FÞÊh\x001c%M
\x0017(ìj\x0004Öºpe\x001d(F¢\x0015ÑITw
f$åT#Pò\x001f\x0018Ål3Ê\x0011£ì`ôÈ\x0008o½\x0018\x001d2zîæ2ª\x0011£j^ö\x0000¿4Ì 3rBtu%]\x000f¢\x001e!êæÕè±®$¬Fu:Á c*éA4#DÓ¨Sõ·2æ©ëÅ|¾fu*¢\x001dÑøÚïÀï¾Ó,`Em\x0010F
ì¦\x000e\x001bÆÌ\ÖÖð{ëq°KÒ¦QV´£7ä¿G£¿:\x0018]íx¢Ð_ã\x0019#Qo8ì\x0018ûp-#F7÷[[§GÍ;Æ1Ôm\x000bvä(±\x001fvujßõíf8GS©\x0007\x0006F\x0013Õ\x0003\x0019»;^\x000c7¨×\x0006\x0019y|aò!nÀ\x000cEª\x001bÁ@Ý\x0017J«7Í^"
\x0017 ô\x0012Çà2
r<7¤´ÈGÃm&\x0011\x0019\x000enÅ\x000fn\x0005#àwdº¸~¸»ÙA¥ñ4Å=\x0004Ç\x0007©4QhC¹/î¶lÕùéñ\x0004,;Â²Ó±´£Î\x0008ã\x0014Ä\x0008KaÑCàâ[\x0017¹FÓ¹\x000fEÎ}±¹ÕÅÿ·À\x0016ù¿;2­Ú\x0018\x001cT\x0014>%Ã«Äfªôº\x00169¸XÆôê\x0002%.Rªuñ\x000c&û#ÿoßþã\x0013VëÆ\x001aÝ\x0013P)¼½]·?a5{óá×<Ü|¹¿\x000bÿIá?ÏÁ*e\x001dL6ä\x0007ÜÐ5°XÁÄõÓ7' Nxr²|÷Ü4ó\x0012\x0004"wø3
\x0019ÌÚÀÁÑ\x0000BÄ\x001c êâ\x0008\x001f\x000bþLäÐT»o¬N\x0002À\x0007`\x0003t\x0017Hø¼RL\x0004±áJ\x0016I\x0007O\x0004,"ë\x0006	¶?Ó@$§Z'H-Çn;x\x0011ÌòëÒ÷\x0004ç\x0005¦@Ï)®U\x0014*Ï!C-Í.à\x0015àÏ4
\x0018º\x000bÕÔ\x0014\x0003 4C5è^\x0010P¬?ÍaiØ´>f9ÏßúYüß~þÓg
&<->\x0006Çö<\x0004Ø
PPß\x001fgCð_cA`º´Æòjñ1x²g\x0011¾êÇ/?ßá8\x001bçäæúiñöæÛâÝýSp±;Px¸ñ§ìªTáPyßpzxÌ®zmdåBWW·ÇwgWÁ·NA
ÿvø3\x0019I\x0018#¨\\x000bf`âÖ	A\x0018	øT
Ò\x0014ö\x000eü\x0004»9Æ2ú{VÄ7\x0018otóÂç?Ó|\x0008qR*5}·H¤©7\x001c)è'
\x0007\x0018üi°\x0011²LD`HG°\x001en|æWûã§Çøåà_\x001bÀÁè>|0\x001cu\x0008{\x001e§Ezãé S×·®\x001fQa.êÊ¬\x0017©\x000bä>\x000e=\x0003¤$cøÈ­­M%"á|ô4¶Áâ\	âY.RïÇ\x0019Ô
=Góôku>QÈ'Ð||Xÿ¸óØÖ\x001cs¥R\x0008\x001f5\x001fÂaé5.kä\x0003ÈÇóåÛI\x000cáSÃ	\x000c^9\x000ca¤\x0000¡\x0014ÂhNUI\x0019Û\x0002ñ\x001fìÁÿù\x001b)F	EèÇ¹\ÃÉ\x0000R.×ß\x0002R|éÿ\x0008w¿óKYcÃ\x0007Iõ\x0008!¾0í\x0014Ñ\x0003|µÍ\x0017Ë%\x001c\x0018 î²º\x000c¨ñÑÿ#üÝÙ¯7@Cïvó !Ee\x0010Ú¤8ðÞ¥t\x001d\x0003Íh7UäöC[S$\x0002´NË N\x0018¦×d]G½Ðk~ý·?ã\x0000Ú8vöðþéñ/Oëû]>\x0004¯1lP<	ü»
Ã\x001c¹³>äðìêâ÷WËó³çÝÇß¿ýåoæ?°1ö-&÷ñË®À\x0001ä\x0011Í\x0005q>QÞÑ§åª¾x,wjq0PôóÅH.\x0006~>ä
ÁÔÇë¿=\§ÈÇÅ§\x0007ø±(æ9#	¸\x0005¤zah\x000eïÜ\x0019F­NÁÝ:¸ú¸úÃù*Õ],>\Ã×[]<k³+y\x0011WÆy\x0001÷äækø7wX÷\x0016+zîwØ\x0012Æ©¤½-½éb\x0019\x001c¤uIöäøCø®Ç§Xô\x0016zÎ^õ\x0015¬ïw\\x0015².Î"Þh¼v\x001f°ø\x0014°uÁÊpÊ¦9ð\x0012\x0014ÎpZZ\x0006Î{±\x000fVS±>V%]ÊKÐû:Ø5øuj33QU!æ\x001eQÕXRþm}{\x0003ß?Ý}^ßìð\¨4>U²\x0000áh&É ¬²AÂ\x000fËËåÉ1À}uz´<~Ìdæ5ÙÌ6QÈ§x\x001aeØ²\x0000Ò|\x0016+ÙÜk²/É|\x001bQønÄ9\x0003ß\x0018Ñ\x001c·&«`§\x0015MË

~mÓ\x000ce5\x0002\x001d^T\x0003\x001d>u\x0004»1Ó\x0007-Q/\x000bà \x0010(ålìÍãàLºí³7W©PJêp<c\x001a\x000b*_Õv\x0006K²±Ç\x0017;\x0001¡Û\x0017ae\x0005+;a©ZÂ£7\x0004KÊ¢é½Àª
VuÂÂ\x0004øÄÊè@CÐÂÝr\x001cXt¢ê
Uw£¦PQÂÓ&ÄJv5f?°¶µ}°!®Å HûDàÒ\x0010©	ÊE1à\x001c@¹\x0003Î\x0003è»õ×u¦\x000cWÄ\x001dg´°ZQºÝz\x0005æxÏQ¯Çác\x0003è»åe¦\x000c×Å]'4BÚ
Ò¶CÂðáÄ\x0018Â`)ÆE5þêíÚÚ·3\x001aµÄ1Qn\x0011ÒS-±ßHÓ·C\x001aWB\x001a×\x0005©Ý\x0016H±?Hiÿ¸\x001e}ïõëâdIC\x000f{\¾\x0001)ßt[½.º7lF%B¡$î\x001a\x0001\x0013¹hì!wåý&]YW¹{óE4Q¡\x00164Í)y)Tt4p\x0019m\x000e¬Àd\x0013\x0018toI¬õ`P\x0015`ub¾\x0019MWhº	Í±\x0003i±DÕ$\x001dÜp]åä\x001bv3ÐÊÓDÆÓ¤\x0001MÑèz\x0001ÓåD2¡·\x001dÃ¸AfTI\x0006òB
dLÒ\x001eUIf/¢qKh\Ì1ñ\x0015oÚVÓC\x0014ÜAi{:I³q\x0005ïC\x0013¶%\x0012m\x001bg|¼~Xß o{·~Ø\x0018\x000e1LÊå\x000bm==×A\x0004Ó]²Zl\x001fWçËctlïç;²³\x0019ÏUx®\x0011/¸^NxôÔ °/=\x000eßöóè|Eçè¤V"+\x00137\x0006,V»¡\x001dN°\x0012\x000eæ´Àiï\x000e|Ò1y7õÂ6\x000f­¤EgdI\x0007ò\x0016-tp'IzqÐ­pp\x000eå¦ \x0000¤×v\x0015ÓµN²8]+DÈcúôæóýízGz\x0013À`rE|©@¡Î°G\x001dÎ+÷ÒÕp'Ë£>=>:;YîJj"¨ØD#\x001bÇù\x0015R$BJ;KÂÒ:3\x000bNVp²
NÓ{0P>Â)-'úØ-j¢\x0017¶Pctt{ÿ¸8Yß?=¬wäô\x0015è5¤ÑÚ!>2©J,ªÃ¢J,_\x0019¸NÎ.ÂJ;»:_>ÕÏL¢d\x00128\x0013X­¡8G\x0001](«\x001b\x0012WÕþlc%Ê$á0HJ\x0007\x0019êû\x0004ÓT@ï7*Ôd31\x0018\x0011h ¾¥£°\x001eÂ\x0002ëf²¬dz×©PvÁ<)x¡LøíP/º
JB\x001dô\x0003TXðëËû§ÅOÃ3
¥»wÂH,öPy\x0012;\x0015¸\x0003\x0015\x001a|¢q¢4ÜåùÙÕâíUùNRÞ;Ó\x0013ºèôfÔ±Óÿè§4NcñöúááfwdøÀÉeÿêDÁuÅyô>MÔ\x0008ÿs~~\x000cµ2Ï¿xqVHMÆû\x001fR(¹z´þ1V p\x001aLúû§ÞZ5¦&J\x001a|kuô@ÌKßú«GË·ñÜº\x0000Ó`Ò\x0010Øí\x0002\x0006{j5x¹@«U*Íz\x001f\x00170§d\x0007$ô,à«¡qØu-¸ä(£a½£W\x000e(8x»1%»\x000eËñÀçÏ¿·Ç'à]4YC\x000fê£¶C|iÏï¿¦.Øòþ\x001b\x001f_\x0004Ö®\x0004~ö­ýE`ç©kÊb\x0001\x000eÜ+r¿¬\x0019½Ävó\x001aSò>ûÌþ"¯5\x0018½\x0008X´édáÐ÷N\x0006vv6p,ÚVÃ
Ø~\x001dGe¼[?Æ7d@>¼ùüÓýÝ\x000b¹t\x001cî\x0001
j6\x0015¦qÒE\x0007½½*È_ÆA\x0019ï\x0017ñ
\x0019\x000fÞ=W¢\x001c]«\x001aeÕÂÝ+fÕ`×ÿú?\x000f¨\x0007ñôËõßov Jã9ÌòHQ«\x0002±OpVJÓÕ\9;z\x000f\x001bþ\x001cå ®~XýûsÔÎÿÑ]ÿõç»'LúÇTÿùýÓ·HöÃÍ/ñ9\x001eõ\x0005»\x0004¬ë»ÇßÝ^?þîõíãXà
cÞá>Â­´ÁI6E(\x000eÂ¨ù\x001dN/~w²ºøÝ\x000fË\x000bèò»?\x001cÿP>É¾ÿúõén\x0003??Úùl\x001a\x0005|á\x0008MºYá\x0004*à³b\x001f|PSÍ±-²/ø#hù\x0002>ã@)'ò)M|T"9\x000f\x0010\x000c(»\x000c\x0018®Já$'\x0003"\x001f\x000c4@>ë÷À\x0007¯ø£Os\x0016\x001bD"&©c\x0013\x001f\x0016#à>Ì\x0007AhüÑ§4\x0004µéûJ?V(xê\x0015æ\x0000
xM?Ú\x0001uÒ\x0008X"\x0017\x0000AÅ\x0002\x0001)Ú\x0005\x0008·ø£\x001d0x=G\x00164ØA\x001c¾µÈ+j?g\x0001BUcüÑ\x000e\x0008Ã­\x000c®@*áN,ó\x00166û° üCâ\x000eÀ¤'\x0004\x0004\x0008$L¸¢-²5\x0008ëD¸¾O,ÈÇ@ÓI\x0012"\x0000HÔÌ\x001e\x0000áb\x00134\x0003BS\x001cH\x000bE@Ò9!4C>TË\x0007\x0006ìó2!^Tés %ìpäSÄØ=\x0000J`]Ð\x000eÁ\x0010\x0010öHò2.¾\x0017\x0001 ãv\x000f_X\x0007T]n0Ä)±Û\x0015\x0000µ'\x000b:òYµ\x0007>\x0010g?Úùt®\x0018ù\x0014\x001dsÎ\x0008E{8ç\x0014\Uãv>+\x000eqf¢\x0006óå\x001dì'à!Õ³t?:¾®}Â\x0011¤ßõ\x001cÂ \x0013=\x000fJ:ã\x000e>\x0011åµOèlàÓ\x0014¥º}\x001cÂ
J.ãÏËã\x00145\x0000ÌÊáûZ\x0002´ûp0*¶ªtE	Æãæ\x0000\x0015 d>\x000fOhh>µ UAt ºB\x0004èD>îP{"XÏ\x0013e{X~:öùôyg} òéá
:gE! ñûp~PD\x001btOe>ê\x0003\x001f´l%<µðEA26þè0_4Z\x000e\x0018ÐÎ\x001b¯´Úý \x0006?:\x0000]ÌÑÅ\x0008Õ6F\x0002t9\x0000{Ø\x001f\x001a\x000e6ÝuºA\x0007'Ç\x00085|kô^f>¾\x0007ï\x0012|º+¶*ÕbüÇÏä\x0015(ö°\x0002-$8l_CÊ\x0001\x000f\x001cÚåð/7ìÍð/\x000e¶®ëÚ¿NÛ\x0003¹FÉÄ\x0010\x0006eÿb÷\x0011>;\x0010s®\x000fjñé
¨-E@¯ZÎN9<þ¼I?	A¹<\x0001,N¬x\x00011r\x000fi,\x001e5ÂÒÏV@
\x0013L|úÆ&MþSqnrÂãlþþà¥,[ýtX½±¨[*RQ@\x001f\x0008µuó 1O){¶°Á\x00162¹@m%©\x0004JÏ1FÐÚÌOsp\x0012=À@\x00064\x0012\x0007M\x0005< µÚÃ\x0005ÇØwEkäø%|m T\x0010»à'ÞÃ)Ì\x0015ä\x000fÒÏvBëã¸G\x0018Î<Uao£1l\x000fQ~0\x0003\x0010ê0_s¯c14\x0010Zº(
ÅPïá NSÓÏvBÇ`ä}zopä	U^Æº=|å\x0018%ð®X!\x0010úm\x0003\x0011c6D>·\x0007G\x001dÚég3`\x001e²ÐÉ\x000c\x0013	
zÕÈ|\x001f1c®{rEZà¬VX0V<\x0001ª¼Kpò<À¨¹~v\x0000¦vâ¸K\x0004\x000e;\x000f7/:L²{pÕ Kÿ&ýì tô*g\x000cVb\x0000¡s\x0014/=ì\x0012\x0013;ÓuÜ	Ð7DO£9\x000e\x0014\x0003BÚ'b\x000f	$U\x0005K\x001b	e\x001cK\x001d	Ç[§ÒSÌ%ö\x0010\x0013F5ô³\x00030?\x001d\x001b0E­\x001a¤0\x0010p\x000f|ñ01]	|b¼4AÅ
G>èÓÆ¨p\x001fk0\x0006Õ¦'¨Ö KA1+T\x0001à.\x001aÚ\x00141ì#ë¦\x0000¥]Ø%B­Lªã\x0006Bz}ÕRîÐDÂ«\x0016JÅB ¦\x0006<N \x001d\x0008Ã¿y\x000f0\x0008"ýì ¢:©4ú;\x0000ÒÝ]AÒ|@\x0017\x0001{^¿´0ÉË(âfNØ \x001fñö\x0011/Øx\x001aÛ¾Ó\x0018_¯¡ããIçéë*»9îâYìúÎb-éê\x000e¥\x001e\x0008\x0005:\x0019eüüÔ\x0016wÕJ?;\x0008s8£,CR¥=ñía\x0003»¨F\x0013vl\x000fFÉK¨åÑ\x0018®Zzù\x0003e\x000f ~vì\x000f\x0017{^#¡Ä¹\x0016Êp	§d·^$WO×uõ\x0014ábÙ\x0005P_OçH~SjF(óIüÇ£ÿ\x0019KÉ¨,ÇOy\x0016\x000e±\x001fçù]Ýá³°¢\x0008Áê­YT{ôL\x0019n\x0005\x0005gamPIÔ2AÙÔ\x0007PäS¬ÞúVØ\x0002\x0015N\x001cÃÛ T@O\x000c\x001eK$DÚº	ZB0\x0006\x001aøðìá±2çW£ÙLáßfÄ¾"¦àÃzeLÁ'¤yµ¯)«b½"&ÒÊl`*\x000e7ïÊ\x0012ÔU\x0013\x0013£ÌûÖò½\x0016¦\x0010>\x0019×ÈD\x000fÝXæÃu~§Ýv¥j¡	þÛ4úðßú«ÁÕÉ6ºðß)xoÛîÁ[¦ðï·Þò·[Im·­~RQ¾À	#ZÃ\x0019GHÖ²mqT\x000b\x0014<`6:Jc)kï\x0004|A
75âÛ\x0002ä\x0016¨à%m£§üÍã&\x0018m\x001bÝÒo\x000f\x0015>¿}m\x0011f|ÕmtO0Æäb%0u.	·[/]Ó¡bc?\x0017¯åXÓÈâ&o £8\x000fúKª¹\x0015¹æb{~³iÿq\x001dWùú5¬¨Ï··7\x000fÛDÿ÷¿þ{õøgÔ2z\x0011\x000fÆÄÛ|\x0014K³e¤	¿E<ÃäÖ½Åêâc-kTßö\x0006HX¡ÊtB*¨òß6ü÷ôTðmÆjL¿+¯9QgÖ¼ÑXLË)\x0006#£QPÉ£WbÇ­y:$Ôê¢h´
Rk|¥\x0008Ê
§Â\x0006¯øäH\x0003$XRôZÒ:z\x0012õÞeHéÐÝy±+\x00056\x001d\x0012\x001e\x0001Êgå6Héè1À{C5rÚQ\x001f\x0017»\x001au¦CB$«m/¤Õ\x0011ÒH| á+Sµw;Ù!
YnKFo`â\ûÜ^ìh`Çîm#rÓi\x0004)¨\x0001À	\x0011§ªÌe·òé¬ÑQC13a×\x0018²#1J¿\x000f\x001fibî Û0¦Ê`v¹BF:£\x001d×{Y\x0010³\x001b;\x0003Rb´E\x0013\x0015\x0000\x0012ODíÞñF0\x001d\x0012Î,ãº!\x0005ÖÏ,}ª
Ô~bý®6ÕÉQÔÒö\x0016q¢¨ÌUì¶^ÖMÙ3Ûk8\x000b@¸wÀ¾m-È=:x¾Ç-\x0003êÐ\x0018Çê½X\x0011B
Û\x001dW\x0015yTÙ<CNÙØ/\x0019\x0012dâ^C*ÊU¸¼\x001cn­}Q@@¨^Dï\x0006ð¨ÙÃð}øo¨^}\x0013ô\x0001ªlC&)\x0010¶£Ý½,F\x0008xlwÔ\x0003#2©°XShV@ªý|jxµ²ªwÇ(E×e\x000bb\x0003)êÂz\x0008)÷\x0003	[Fuo\x0019M§u±Y Y27\x0000}\x001fÐÞcõ¸\x0007\x001d¤u\x001ag¶ûY1cÛ\x001dãBû\x0016öË\x001b
Êë,÷ûøÚ\x000ebG×\x001f@Ú\x000c	ý¬\ª_³{)¢\x001eë¾wIO¥/PÞ¥ÃmÚ~td¿\x0008	ÎÇÍñ@TåQ¤²\fçãy\x0003$X²Û\x0003IN\x001eÈ8\x0006%Äþ\x0015*¨Ô|/\x001bN~§{!E¸%`µõ0\x001bâ\£Äz¶\x0006H\x0003¦\x0013\x0012*±ÄÜ!²\x0010¹4uWñìtHxÊ?ú M®ý\x0019B\x0018_\x0018zªÙUÚ\x0008\x001f»ûæ%d\x0008\x001c\x000bï`ÛP!¼ÜË\x0015ÖÁ¥Ëuß¼\x0004ÏFRª\x0014Â3*\x0000u3r\x0001×?ÿòóß\x001fþX\x000cþûýÓúáÛÍõÃâûû§Ûõ4Æà\x0019s­´\x001a¾5qkB\x0005¦\x001b]\x001e¯Î\x0017ß]\x001c/\x0013«!\x00054¿vH\x001c\x000eøº!q:_\x0017¤ÕTMfÃ%\x0007ÅZb´µØ\x001b&NÄ|Ý¶to¢HÙë\x000c\x0011\x0000üéôê3Æðz$\x0017$·å=4z°\x0012/Lå\x001e1q:a\x0017fÐ¨7\x0007\x000eòdL\x0013ÅÎ±¹i[°Ö)ÞÄA4¯\x001d\x0013uéú0\x001duTB9Jº\x0018\x0018e¿«U¬\x000bS½Ãgú\¦Dq\x0003ð\x000c)%)k\x0018·õ©\x0012^t\x001f¥f<\x001bS \x0008Í×1·µ7µÇBkÞ½Íÿ9\x001eC-QüÑEé$QÂ\x0017çø^§I+|ñm\x0019Ê.N¨S0çfiÜyäTôd\x001777rnÍ\x000bõpÂyüÑgOÅ#d~%1¹Ä>\)÷äxlþõ½«Óø¬2 \x0019HÄÖ}j
ÝÓw\x0017°D÷.ú§q\x000e+¯k\x0006¥,á_Þ¬_ýQ$\x00015}¤ÿ¼MÏT$U½¤¿±³~úû·¿£´=\x0008Ú?]"úÅú\x0001NßÜN@.·:P3#J
´Ý.¬tµ\x0002]ôå9\x000c£>>yî> B5æZ{\x0018ó£\x0011&g:\x0004½;B!Î^\x0018£øX'£å$o\x0008®x«Ò#ÒMØWoF¤+F\x000f¢Ñt\x00084L2"²Â|æ©¾:nz\x00185v\x000bkCõV!ÏíÌÛ\x001fõÚ\x0001±[¢\x0007P
ÙK`LÎGA\x0018÷cDªyïbt¹ë\x001aj$1Ò\x0016Û\x000b\x0000\x0019¡³2ª}u0J\x0019'ÔF×(é\x001dJe=U#·kÉ43B(ä;í(\x0006Æp£ðµÒùõDn×Ôje\x001cn\x0014=á4dÔb¯!\x0010!\x0003ñna£1äöj\x0011î\x0013¼ó	\x0001\x0005ö\x001b¥è:1\x0008°íâ¾Ívó÷\x001e2ÌÐë­\x0004ÊC¢¨m×i\x0004e\x0019øÑµ"£L´yE\x001cO²íÍöÍ\x0018{\x000f$£nv8®ñ©LiªÁÑ~O©ã¾\x000f\x0012\x001f¡¦¸öH%H:CízÍ.{\x0007¤¤þ\x0000sÞPõRzªRÔJm}tl\x0014,\x0006g}\x001b'ö>ãÆ++Ðû	 \x000býø\x001eFEU ¼Ôß$\x0014ÚÑ×Þ.N×\x000coµ=:·h}LåÒ|Ù~\x000emèx#:·vø÷¼v:#jêÿ·\x0017ÈAê¾\x00032X\x001a\x0006[Û¤ðGæ^°µ÷\x0012Z\x0014RÀí\x001c ISeFp\x0014D5¶]MüÙþòËÍý\x001fÓÈ¿8èïäúqqxÿ\x0000\x0013s\x0002êûõÓ·)\x0003Â¤\x0000saÐ\x0010ã\x0002¥äbkÇâêbqxv\x000es\x0002ëûåÕå\x0004LH¯WÅ\x0004z0\x0017©,A}Xzá\x0011QÜ%R2¹Uct\x000bæöX-SrX:ñÇë¶æp¿nÎ°bnÇ!Ù¯TüñSÜHþ\x0005H×ôõÛ4eVÙk%ýtóãÞý¥L\x000e\x001dÞÜÞÞßÞ?Ý}¹p\x0014ÁPË\x0018d
KAf\x0014F\x0004<¥ÝÖ§ÒÃã³³«ÓwÏq¯ÉBx\x0005ZÉ\x0014j}\x0006siôç\x0006\x001ba[ßÄ§ ýõO¿ÜÿòÇ4ì888s½s«§4R\x0011¿Òy\x0012y^|6îÙ®§Ï
±®àà(zà|\x0016°Q\x000cj\x0002S{qîPuÏß¸§ÃQQF+³¤>êdNçZçuÁ\x0010ÁÙp h\x0004\x001aá0	ÚpÄ\x00016B;FïÈnûks±Ê³\x001d.Ü¬%ÂI:]ÒñÁrÛeà8<&Ä\x001f­tÒÑ|\x0015i)\x0011å)]îù\x000bÌt¸\x0014Îòv8e ]èrS&/Ù^®ÝF7\x000c\x0001l¤Ónè«Êý
.Ë<Ú<¶îO·OO?ßÆ'B±u\x000c²\x0017\x0017÷O·ë	dq\x0018Æ@D¢0>]SÛ~xÁl×å\x0014¨¨\x0013,\x001b¡Ø\x0001ÏÛ\x0013¦æ$¿5/Û\x0002¥qÖ_\x0003ó>7\x0019.«D*Ej\x0005~«jñt*\x0005å;ñÇk¢
fJ\x000fÏ:ÆGÿÏÁ\x001eþôÕ¿¥¸-Fmt;ÿxýíæÛâèþ	F°NÛâØ`Ìµ:F9#-|®Sß®®nè\x001fWÇ£³+ÆúÌ|ë\x00166¸Ð3h\x00173Â¥¦BÎÚÿ\x001d©fÜÑSi;n8\é½Ôi¤<Ï¸ÛKìp¿ÝßþI|ÖåË~ù\x0016Ø¿ÜÞ<^/Îï¿NzÌ×\x001cf®ã+4£6\x0015èf \x001c¢Û.©|ôÉbõîäøbµ8?û°ëM@Ù%=\x000fY*ª4Üc#\x00154ÓÑ¼\x0001oM{ö ç\x0011½sÆ\x000ba±/_E}J|áPûEFÉÊYÈ:?	KI;ÒYDí\x0015¹z½îEæ¤Wj$u3¶ÄP
ðìëG\x0007r1|x\x0006³Î\x00138MµQ0\x0016óv5ñ^fÍR9Õ<fEîá½Ég\x0018¾}àG\x001b³þüó®?mT$ä÷ëÀõeÒqgaîQTÄä464JÒ\x0017
±ò\x0008ùdñ~\x0019þ\x000fïKR\x0014XâÛÅh5½ãxÎr-W$¡¶Ky·2B±\x000eüébôöÇ1fZÑ\x001c·½î¼\x0019°ªjh\x0006d4oÜÞ\x001e\x001aQÈsl\x001f\x001fzô\x001aß\x0008©¦$7\x001cGH­\x0019ÝÃýöî¶VÈm©\x0001RA\\x0018!A	!'ñ\x0013?ÉÛÓù\x0003#øµø£Ñå-ãÈ¤ÎâùóOa-V\x0004Ï\x0010t\x0011,7Ä¡tV\x0002\x0013ûØ1Cýv\x0017¢\x0010T-àÏ¾ÑrbdÏ¿\x001f¿\x000cùóß¥eªÌEæbÓÛë \x001a&\x001d`N\x0012Fc\x000f4T\x0018nÈÛ6M®8
«\x0017cê\x0001*:{aa\x0002\x0016>ÓZõ66¸Ö[\x000bézY1þïdÁ\x001bátJ­\x0018©E;\x0017à[³G½°\x0012^ègÀ\x001aJÙÀ6ôJP¡JU#[»^X\x00033ßÿ5`9ÜÐâ
Z\x0013gôÓr\x000b!`\x001eT
\x001eÂ²­##;a]\x001c?1Ã\x001dÀ\x0000#t]yú:Íÿ\x0006î@@\x000e?þè¶¬Ì³\x001a¹\x0003uàdZò\x0007ÊïÑ\x001dÈøR*EÙÐºliè \x001fñï°\x001cfk$Õ	«âc©bs`s{\x0007<c¡.ï1¾G÷\x0015x?EÞOÿ\x0012>	\x000bö
gÑ<ûª\T(¨`¼Úz%mÂýÏObÍ}&<Y/¾\x0003Âõ·ë	7gÉ Å\x000f«6Ü\x0019é\x0014q/°Î\x0007wð\x0012øw\x0000·¼\?cÎ\x001cÒéñÇë%´qb\x000f¡Ä@\x0018¼«áÆr½}Tf+!c\x0006Ö¤I"ÊPûo#¢\x0014
\x001fª\x0005\x000cMmõ¤\x0013\x0011ÍÓ7v\x0017k8@\x0019þ\x000cÅ\x001bß=¬§\x0010ª°ãÀr\x0001Å\x0008\x0017GÂv£ÎÐz·½\x0006!n|w¾8h>·3\x0006gòº\x001aúS$)\x001cà[åÛåÑÚ\x0019uÌI¿FÆÇû?ÿøõK¼CÅ·»7o¿þyýøîzëÅÑíúé±Q-\x0002Ôþq\x0004Ö. ØByüáãòâ"]ö£åÕÅ\x000eÔÏ÷æÙ,=y\¬Âÿééë¤iÛ\x001aÆî¡¶ ô¥\x0008Ä²üí·\x000f,7ÒÅê"8ñ\x000fÏÏt\x001a\x0018ëgFF*ßÎ\x000eU(D\x001cßQèÑÄ:+½vDÝà4|»@Ú\x0018q{
'\x0013ò8¾0÷Ä5"¨
KR<6SXGsß={¾\x0007©Å<\x000e©´}Fh\x0012*ö¡\x0018g4\x001dfpv¼Ù´0æ;F§\x0015±¿Ù;G
\x001fÖå\x0014eHÁ4ûòS<
Ã\x000eÿs±ìn\x0002pÊ\x001eX¸M\x0018ç¬Â)©ÜÒmâÿ§îÝ²ãºüÝ©p\x0002ÍKà¶ôD©h^Ô¥(ÉëT¿x¥$ZfY\x0012eJô¥þÓ8¯ç©k\x001c53\x0000"\x001bidæ\x0006ön\x001f¹»]TU·?"@ â\x0017R¦"Ñó3Â<ßkh
Ó6?×C%tÎyDª¸`.Ç7§½KÝÎ\x001dvP\x0005~À\x000e*gÔ©	JH^+«©>Kª¶êÙ|*m0é£*p\x0018ã}P­?Ð¸V¶\x0015\x000bÎ§\x0002\x0002éN*CÂ¸V@%\x0016q­(û\x001b×Ê-£J:Åé£g_åYÊy­\x001c\x0015±Å¨@ðno\x001fÄ£Tï?¼×ÿºªm#\x0000´\x0014?ß_ßÝ¾5,Q£*s¶gÑäòÔ]ëù\x0004í"Àm\x0014öâï/Ï¯^Ï\x0001æIiãÀ ¸/P{KO:8Wuhêµt\x0002ÿzw}óá§\x001cñc¼_û3b+\x0015p@+¤h_Ä\x00180ÇÒ2HþêÁ6¦Ñþù×7Oï\x000eÐµ.óð\x0000§\x0003'<£©¤W\x0006A¯µ\x0012\x0008â\x001d]¼ösÎeI
3
xãTT\x0014\x000fc¹Ïµ[}»ùZ\x0017ÎY|JãqÎ|B|%\x001ceB"_³§rÞ×«Ü/\x001f}êS1À\x0017\x0017äÍÉ\x000b4?7sâ{L×P|:'Ô®\x0008m{
\x001b?å¼@Ctö·ý+¹%Ý-\x0007í#U>ðk®í@\x0002×Xq (´4MaR§JÇoÿèyL¢;»\x001a§M³è9á\x000b	ÖÈ\x0005j°ä×P\x000bíqï\x0003 ;ÝªÝ ñ$\x0005ª\x001b1®ô«êÒ1Â¦uHM*<\x001c'6V%ðtL½}\x0019k£\x000fúî3||ÿó®¬È³»Íg}önNµÆYÇ)ä°v\x0018
åv\x0008-Ã^±gWg/\x0008õY¼Öï¹èm!§²\x001d\x0003ÚPiFä\x0004åW\x0008º÷{\x0007j\x0013áõï©ð\x0001Âtj\x000cý|;'ÆÞqó\x0013*6Q©\x0018Î¦q?ñtD±ÅÁ~ô1\x001b'H\x001cGjô`\x0004FòHk\x001bÉÃ<æãuxónE*­½\x001fN^ÜÞßÍÉ°G\x0006Áv~ËÒ§TÂ¨Bé?>`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=ùyùêhrÎH#\x001b\x001cæÐ\x0003HnÍG\x0010\x001fI.^\x0016\x0017®	%+ý(¸hKe\x0014\x001dðÝd"X*R\x0019»\x0007JÙC<\x0007ÅSp\x0011QÒ2¢-È]\x0013IVâóH¬ ¡*H"0ôH|ù>£s[µõL\x0014­ÉáJGP¢å¤È=Hrªv&	<Ë=}\x001e|¼åÏ\x0013Óv§,\x0014\x0011÷@É	Ù( Ls,S®Ì÷'z,åL(©,¬\x0015ó®óX\x001c\x0014\x0016Àa\x0010ø`L\x0016T`tBÑûH«3Q´ÉÏküBQ´+§VTÚ?Þ~¿ûà{CÕî\x0017¯Óð¤KNN\x0002iïr×\x001dêsKmªYÿs	\x0013¡Sñ:MM:9Ü²
¤\x0007FeD5`&¥\x0008ÊIlBNTT\x001e®</p><p>\x000bûSQíP\x00152yQ«Ä½dXlÀ¼u\x0004æ¤j\x0004Ã=Qvþ\x001bø=_/á?µøåêËÛëï\x000fÔT¹ý«</p><p>Ê£vüUØ³Éà6c.;<¹8\ürôúõéñßßPcånXÕUm°Ò\x0017¯0X\x000clôÕ\x0013±ê.«ncÅºþ¬ëEHÝ¾éûkGºDxû4¬¦ËjÚXQ×dk bÚ\x0004ë\x0014³\x0006©\x0006Övam\x0013,.pÌ\x0017+¦¦|</p><p>".oÉ°Â<
«ë²º6ÁZ\x001a\\x0002¬¾(\x0001WPKeè¾¬¾ËêÛä\x001ecÒW8\x0012ÕDòMÈà¸\x0018èn.jhB5àðûì2`°\x000b¤ô&¹êðD+vac\-Íi\x0016\x000bÖ(zGoæÀRÈÍh\x0013­¢\1V§{6[\x001cCï½'¡í\x001b¯6ëeæ \x000cXÔâÆ\x001a¢uÑE÷4´=ë%ÛÌ1\x00017$$Ùâúq~\x0019Ï²òih{öK¶\x00190ëh1"ÈÖÆrnq\x0017ÉV?l{\x0016L¶0ãh.ÈVºòôM³vl¥y\x001aý%{&L¶Ú°*I¶XÊ$éùåY'Ø§¢í\x00191ÙfÅ÷ü\x0007õ=@I¶Fr°Eøø4´=3&\x001bíXPäÌ¤e\x001f¬\x0013¼,[ñD²íY2ÙhÊ?  4\x0007p.>V? {L¶2'Dîm\x0004ÑJ¾%ÉFÃ\x001a:µ÷U=K¦\x001a-Yôyû"ÀÆ\x0014\x0002J¢u²[ñ©<\x001aÕ³dªÍ9E]Ý2à\x0000e¯ò{_l\x001b\(UÉûÒößamÌâ@>\x0012­)¢õ\x001c</p><p>Àj§í\x00192ÕfÈ¢ÙP ZP¶9Ë	~\x000càÌÓØ1Õ³cªÍY©\x00186FYÂÚ¡\x001cÚ§Q\x0007ªgÅT\x0015sÚ²\x0010t* Í1*
v\x0018£j¥íY1ÕfÅ,n-\x000cÅ.x²¹ÏA´ÃL+mÏ©6+æpöQ¶\x0005F^&Ù\x001aOº6<ó¥zFLµ\x00191\x000b\x000e'ÑÂ+]EçØ1OäÎ¨\x0015SVÌ*ÎúZ½h-ù\x0007A\x000eSG°ºgÅt\x0015³Qå©ÿhr5n*I¢
Åæ*ù4ï1Ý³bºÑ\x0005×ohqx $9\x0019±ÒKµ/kÏé6\x001bæD©~Áö*:\x0005ÝÄ@+Vöí\x0007\x0013Ûl\x001b¦(Ì
Ü1\x000bVá6Æ\x001cM6îi"tºgÄt\x0011sð\x0002ËW£äË\x0018ÉÃÙx\x001a?Q÷ìn³\x000bIÓ6\x0008¥®#õ4eu\x0010H²=M«Û4­3!¯MAZ¹Ö]·\x0003Zõ4êÀôiS^84®ÇA\x0003Dë<Ý1øð4&×ô\x0014iT\x00086äE¥@+cqg\x001c%"7þi4éì\x001bï3¹</p><p>\x001ch)´^8xâi|pÓ»d¦íyì²Í´Ø\x001aj\x0015\x0015\x0008:·£ê©VØÞ%3mÌ+E¯\x001bg\x001dæ\x0013«aoÆ=Õ©µ½;fÛî\x0007ïÐEªú2¥ÓR6L7\x001bÝ®\x0006fwõ\x0004v×É±á}"gÑöáÓ\x0006üÿê#]\x001f\x0018\x001c&àÿÿãuptû	èti±÷ãâùí#P?ìplõ\x0001%î£¶kÇÖ*~3\x000cý¯´Ôûbñüô\x0002h§FøvàT\x0017NÕÁáÌ\x001e\x001d4f2Ç\x0010­a¸¡»U\x000b§»pºRr¶\x00048µÃÚ³,¹P^[Ã4x-éÂ*8¶ðÎ\x001c#\¿²ýp¶\x000bg+%ç©T\x000f$ç)È\x0006p¢|V³\x001fë²¹:ÁáD;/¯\x0011Y»á+¯ÌwÉ|¥ÔJ]qÔ±ÜT®|Æ\x000eë>+ÙB-TJÍSEN\x0014\x000fSü{±­sªIÃ:8\ä\x0008n\x001dhP®|Õaeh-]_ÿÖ)`¼©èà	T.*Î\x000cß=µp=ý+ë\x0014°+\x0015)yÝ@äò7ÏIs½']O\x0001Ë:
ìày\x0010)(c×¯°\x0012¬eü@+]O\x0003ËJ\x0015l\x0014Ç</p><p>¢7\9hø\x0019\x0013÷TÀ²§e\x0006v¸b¾«Õd»°Aª=\x0005×ÓÀ²R\x0005cË%}ÖàÙ\x0016^±¦\x000bÃúÜZº\x0016ujØ)\x0007\x001d¢è:ÚÄ\x0017]7,|ª¥ëéaY©±ZDL%¹ù}\x0012zÚ\x000e\x0017{p±R\x0004\(\x0015±*\x001eüº\x0004ÇíéÎ©Pf\x0002MGbý6N8²»n÷ëY	Ui%àJU\x0014q	\x00145¼'[ßI¯4\x0012à\x0008\x0007ªUiB}\x0012Ô¥æc¿ëªz6BUÚ\x0008pG\x001c]\x0008oqZM\x0016\,j8ìI×³\x0011ªÎFxåKu*x)tä¬\4L/ÕÂõª4\x0012.\x0014\x0003\x0016D\x0011\x000f¥\x0014qXi^K×ÓÃªR\x000fcü­ãS'ÖpÃ(a-\OÓ©JMå$|ê<N×ÈºD\x0015º½ØtOèJU\x0002¯/Ía	°åÛjùÌ	µßÐý7uÝuõÂ\x0000¸´^(\x0007(C¡\x001bu·UÒõn®»\x0011LãÂA\x00134óu
\ø.÷{åèÞ}Ðu÷ÁX´0xí*[\x0008\x0019\x0004WêQgl%]ïBèº\x000bá½Ä¦D\x0007¦LçS\x0007ÊéÌpúo¯î\x0007\x0007\x000fÿÎ¿ÄÙ"ôãt8E\x000e¶ªÞß>Þw÷ÓN\x0007\x0002\x0014WÞ§\x0004	ÕªE.¨òÆ\x000fdÙ[¬z~zq>ÞP;$U]Òáþ×ù¤\x0018´ã® s 
\x0015³ÇÒ\x0015ô\x0004¨ºªÛQué\x0013ÂDe)JSÀa\x0008£\x0001ÕtQM3*¼u)Õ\x0000`L(¡jN9á²½Qm\x0017Õ6£:ÏE÷ØÓÇ¨Vó\x0001\x0018åò\x001aP]\x0017u¸Ly>jX¤\x00128àO\x0008:«^0ª\x001av</p><p>U 0\x000cÔ\x0012¨q·ºy·ººßÞ¨½ÎÛ)ÑÉ^÷1IÅÊi\x000cCÝôâlyò|y4¹H¹C¦ºdªÌàlx®F\x0005·ÇQãuéXQ	\x0015hº¦«\x0006n+7TQ	W¢¤_9úJ.Óå2U"³2/Ù\x0005Áµ\x001bÄ9ü"7=J*Ðl\x0017ÍÖÌ°rà(</p><p>IR³¥òÑo\x0008oT ¹.«Ï\x001bªPj¸u K­t¾bçä^h¾æ«¤\x0016e^.°î2Ô¾¬6<Ð+ÐB\x0017-TIÍ" ¨0'\x001b2¸1ÒVÛf²Ø%UdBrõ²×å¤\x0019ÇG¿Þèä\x000cÂ:g0\x0013
mi(\x0017T{>j\x001b]ý</p><p>¶¾!¨²\x0004F8®=Âf+îh¶ë(ZÜ­g</p><p>d-\x0008¶È-èR6m9®\x001câ&?¿­g\x000bd10-àXîè:\x0012d7¥\x001d+Øzö@Ö\x0019\x0004\x001fóô{/mSÆ°ØÂ`F\x0005ZÏ\x001eÈ*`´X'k\x0015wËùP¢ñzX\x000b_ÉÖ3\x0008²Î"ò¾\x0008 BÖbãã¶§Øz\x0006AVY\x0004\x0003O\x001f*Áø^#í\x0016\x001d\x001d5pV²õ,¬2	\x0016×ãP'[\x000fñ%\x0008~Ø\x000f]ÉÖ³	²Î(àpCSzÈÄ­SÍMulªg\x0015TU\x00005F\x0005=\x0001\x0002Ð\x001b1u\x0005Ò°°º­g\x0015TU\x0000ç(ß&l±X²dj¥ÝK»©þ\x0003¡Ê*X'\x000f<Wúò</p><p>,|AÊýØzVAÕY\x0005g5\x0015\x001b­âù p\x0008÷rÅUÏ*¨*«`}Q½Þw[¹\x0019MlªÍª`ë\x0005Ug\x0016<ý\x0002\x0007É\x0015_\+¾¦ÂmH4V õ¬ª²</p><p>Ö»\x0003:m.®g*\x0019î~jC±\x0002­g\x0015TU\x0008Úú{~¥1îiüJÕ³</p><p>ªÎ*Hî8øà¥/+°âõ~S^ \x0002­g\x0014TQ\x0000·Ò²{dÁ²\x0015Ht{M÷®3</p><p>1h,¸J|I£.Í6Ã¸Q%[Ï(è:£\x0010×ÝkÁ\x0014¹9QüÊ½ôîÙ\x0004]i\x0013\x0002ÛR»Ö)ÜfM©ß/:£ûQ£*PI $[ÉSóÀ?ÚTjWÁÖ³	ºÎ&`\x000fµ#¹©õq¡Èm/í¦{6AWÙ®d5\x0006\x0005\x0007þÛÏ\x001f×=£ «f2\x0006\\x0010\x0012y¦\x001cG\x001b¼ÙÌ®`ëY\x0005]e\x0015¬\x000c¬BpÃ!Ë-r¶8Ø=ïiOõê*Õ\x000b.mñA¢]ûnÜÿ*÷syMO»*íæ¼¢©Nx°ÖµN²ñ£±J¶</p><p>1U*\x0004\x0004Ã­¸Ø¼Â}Ã±bj1ë\x001e\x0005zÈ¬ªN ÉMpâÖ\x0013J± nê¦¢9xzèÐ%ÑñìöñæÓíõvS0y¤AúÓ<÷H³_\x00197Åx^ürz¼!ï¢Ù
]²\x001b³p´,\x0013®àuÀ8Á\x001cÂ°çd\x0016îâè</p><p>\x001c#K¹\x0010(1ê(ñÑñä"9l2Úã\x001fË¯ÛG.\x0017×ÿý\x001fÿyøñz·»m\x000e,\x0001"nÒpeÐÞX®y¸8^\x001c¾<Þ~üP^~Ý¥Q\x0001¨KJC§þ7\x0002d¾á\x0000j¾Ðå\x000bÕ|j\x001dl\x0006\x001f¦QðÀð¸ñU\x0001Æ.`¬\x00064êBYb\x0019Uªd«ì¦êÃ</p><p>¾N¨ÞwÊûç\x0003</p><p>[Â§Þ\x0017\x0003Ê³kÁÏÝW\x0008ªïT[W0ä»y~\x0000\x001cV¿±ÚX;TCØûÆ²þ#\x000bKØ¯#¥ÑJnzÎ×à©QõZF¯;L°ó^ó\Ä2ôhcíp
aOË¨z5£5ºãdOIæ¡MA®*ÀÞ\x0019TõgPÅÒM·íf=³\x000eu
;>«	}ÐW\x0013JZ@á\x0011Y\x0006\x001auTi}IÈ\x0013×cTõâöqû4á iX·³XUjØ,u`yxn\x000fçw+D^^l%Ì|ªË7,¼ÚÍµu4Ä\x001b>q\x000eË)-"ÙÜÎ\x0006DÝE\x001c\x0016\Í@4\x0018`)àª´<ÞV\x0006Ô#.â°Ðj7"\x0005$!:</p><p>Ò)m\x0004ÃôH\x0003¡í\x0012\x000eë«f\x0010j*i\x0017b~úhÍW1H¼7¢ë"\x000eëªv"¢\x000eëÑöù.+í\x001d/AOp\x0014}\x0017ÑW#JÉce)ùR:H3ïµ.
¡\x0018ª\x0011¡w$¸
<\x000eXÁ+oËÈoh@]ÄXèÖ\x001fÚ;j5\Nª£÷\x0004}¥]­µ#6¨Æ±ü\x00167ÁË¢qö>²§\x0014eµVç\x000eF¥\x001d÷÷\x0018\x001fé(ªÑ@\x0006ÆÎµJ\x0007Û>Ë\x0006\x000f¸.Ôg¹(ÆcÐcoÆÞµWZ	ômÊ·¶ù[['Y1f_50öî¬½0ð)\x001d\x0017PØûT½
\x001fZïñ¡£\x001989Ñðþ×ËÕÍâõÕåÝÝåâxuóñúöj×¢	ÃÀz\x0019\x0011¹ât4Ô\x0019±_\x000f'×GggÈ{òòøôh\x0006°ê\x0002«V`çù\x000e¼u\x000bhË\x0004W?\ ÐN«»´º'ýÇ2>\x0006¦Ýi£5]ZÓLË\x0005J`Í#ù¾Ø1ÁÆ|S§u\x001b¯íòÚV^FÚ°\x000fÇû4¬[ûpOÅëº¼®W²}r:Îñ°w©G\x001bãi}Ö7Ò¢¶Êf í\x000cBZ»^\x0014ä6%<ÛhC64Ë6b:;\x0003ËõZÈ>\x001b\x000ewn\x0007]àØ</p><p>\x000cO$Éë\x0014k^L;²Ó·©<¼	¸\x0013yCS!Zq\x00016;û¾Ô¤*UöXmªû¬%\x000eCã¨hwÞåâÕêþþòîããÎu«ú Ð\x0002%µn¥\x001b=ìpk\x0005-Ð;\¼Z\x001f½¼Ø¶\x00141U\x0017SÕcb\x0012\x0016÷<Qo°.£&1þº?¦îbê\x0006L0\x000c9¦õµÚú¸ÖÆx?ÊU@¾\x0015Nõ>ù3L×Â'?_]Ý<üÛùãõ«w;òpVñûI8y</p><p>Ìr@ÄúÁU:_\x001e¼Y_\x001c¿>z>\x001dO*hª¦ªÐ\(·ÜÆíÕ\x001e7\x001aî¦»hº\x0006ÍZ]ÖÒá@	øëòv·z/2Ó%3UB\x0003íÁ\x0014V9:\x001e¾Á/ö0¬r¬$³]2[%3mËRA»®\x0003å¥®YJ4ßEóuk\x001f"üûer¦ñL\x001e\x0007¶ Î\x0018&\x0010c'x¿øuu÷þêf:Vk¼\x000féL\Ûµy|Äáùâ×åÙÏG'[uÜ0û\x001b×\x0013èfãEn:</p><p>j=cHsr.è½ü5xº§+ñæéQÞõP° ¹Øqsâ¦\x0002ÏtñL%dO&\x0004éÊI¬÷%émÌ\x001cVÐ¹.«¥ó¼J\x0017g\x000esM´eæðæÌu\x0005^èâ:¼4ðñÖ[¢ZOHß4â¢\x0002¯ëýuó®sù,Oò÷~­ñÊ\x0000D\x001fÛ¿®\x001b*\x0016\x0014ËëëÕ»Ú\x001cWV¸ÎÉ9W£¡>¯Ïç¦ÜP½¸¤^ª!«óÿ
º\x000b©[$iy $|`LÅöÌ\x000b£ÉR
¦\x000biZ$é9Ã\x0019\x0012®T\x0010u\x0018¶\x00146@Ú.¤m¤äz\x0019Àá$'n§äêÒáÜÐ\x0006H×t
²\x000cáÆ\x0016!Ü\x0010b\x0019\x001dïöFô]Dßò±\x0015OvÂ¢æ9\x0018mË°&¼Qö\x0018e\x0013¤ãñºX]rî[8F\x000bÒk(ÕPKª^ýÖjñluwwõ_ÿçn\x0017¤fE\x001e/i÷\x0018Xjã\x001cÅ\x0014~¶<;\x0017ü\x000cJÕ¥T
Bpÿfè¬ó¢¬b\x0019n7i¡Ô]JÝ@Ùõ)2ÇâSL"ÕPÚ.¥me¤5}\x0001Þ<B&\x0008.8\x0016ZgB®5 Kª\x0001=¾}¸º¿¿ü|yó°¸\x0006\x001fãÅê;üåD7ncË\x001fÝÀ÷§øá\x0005}Æ
Mãñé£óóÃWð~ÁMÎ/¿v5VÃ\x0012Ñ%6ÑJÓV»2I9®_1j8ï¦\x0019×tqM#®\x0011|V5¼¦)\x0013¥©ýpX3®ïâúF\\x0010iÖR</p><p>+¨pSáNa\x0005X=­:¤]<»»ZíØ:nÜºj^ö8ì¢äÇ­¬ggGË\x0019 ª\x000b::´s@A¦4T\x001fGt9\x001e\x000fÁ>\x000e·²µê.¨n\x0001õewë¾`Ã-`>\x0018û\x0014 ¦\x000b:ºW³$ZÂË8AaPÿ4\x0012µ]PÛ\x0002jË\x000c`\x000f ¬ÁåÉÓÞ
]6P×\x0005uMÉó<`/\x0005\x000f</p><p>	{Pü¨À¼
ÔwAG:j\x000e¨VÔ\x0013ëÁí£â|n~Jk±2t)C\x000b¥,c=Ar%WãxÓwÃÚ±6ÐØ\x0005- Â\x0016A».@°¥¿'\x000cÛ@K\x0010$k{ÑBöhÉ×ù Ê~¥ívt\x0007((¥aíªéÖ®\x001eß>^Ý/_§lÍVN¥E\x0019"¦@Ûg³dµæ¬¸\x001c¦Å©øäøôâè|ñü8%lvª.¨j\x0000ÕRqµ7¨xr¤p\x0003\x000c¾ìp\x0014c\x001b¨îê&PÍ}^=PvP</p><p>ÔtAM\x000b(&Á	\x0014\x001eÎ\\x0010áÊúU3\x001c[Þ\x0006j» ¶\x0005\x0014\x0007§è\x0011¨/o'\x0002u]P×\x0002</p><p>þ\x0012Õû\x0007ð
W\x001cñ\x0011\x001d¦gÛ0}\x0017Ó·`È­~\x001e#\x0010d´,o=·\x0017¨\x0014ý\x001c-þr:¹|ü°[ËÓP]\x001fØ\x0003åÎ\x0013/P ðN\x000e/^l£CªØ/÷Oé³ÅÜ\x001crp%Lxa#wÝMÝqx0÷\x0013iïVïW÷\x000fðßË2ÄU]\Õc»Í¼2çHGyåf\ÝÅÕm¸kæÊ²^®+6¹ÉfZÓ¥5ÂíäÝðãüóäÐJZÛ¥µ²Õ¶X§´ã=Wíéé.JZß¥õ­'A\x001cÈ¥æt¦P)f©÷<·àñõks"O7þÛãêîáêònñìòúúòë./Jy\x001ax</p><p>@æ\x0014çÊ0\x001cÅú·åÙ£Ã³Å³ÃããÃß.f\x0010ê.¡®% ó©R[ar)ÒðÌ6j÷F4]DS¨M©Ið¬TámB½\x001a­vk@´]D[cÒòeK\x001d.\x000fë}5Tû
®Kèê¿³¤å£Që4R6	Ñm÷*\x000e' ÌE\x0014ÿ|ø¦Ô\x0007G×%Ù¢ÕãË+\x001c¡îD\x0006\x0012?½ùô_ÿ÷îöæýåõ=üs0Z\x0014Dz«\x001be¬S\x0007ðÊ8ç\x001d#M\x0000.ñ/g§'?\x001f\x001eÿô|yñâðèÍOïn?~¼¹ä\x001dSÀÿ\x0012=\x0002Ó¾>QÀ</p><p>çÉ%Ô©\x0000\x0014püs|{.Å×ßÝÝ÷/äP \x001bñóíãÕõÛÕÃýV K\x0011V£ó) \x000c \x0000Õþ\x0000\x0002\x001c¹år
òóéÅ?ÇÏo¦Þ=üefÓÀã\x0014Õ\x0002Ðà®Z¸`Æc \x0005i4Õ;´Òä/4FDq¾[«<\x0010\x0006
Á\x0008ýÒV\x00188f¦æC¥}\x000eI4J 3Dcc Ñè¼è¬\x0006þ§Ø</p><p>Ñ`øÈ$\x001aí-vt"L#Ìl¨ë«\x0006\x0014«
Øe¬\x0006DÙH¼>Y6Æ\x0011Va/ÙÀ
ð³i|!õ¦s#FbÎ"\x001f\x001b³×</p><p>?aPm®h¤Ï\x0013Ò±I\x001b­\x0010F[¬oÊÇÆìõ¡àÿ8V\x001c\x001bl\x0005%Ñ\x0018;Ôh¬â+\x0015ö:6\x0018\x001aÃ?f\x001bÜRïTÚ@NwJc\x0012$)?xîªx¾.ö8d:(Nj	A\x001c\x00111T¥CZq@\x0011Ë</p><p>e\x000cf:UX tL</p><p>t¦£#\x001d	Çù}.\x0015Î\x001a\x0015úO¢Å$\x0018^ORÆ12Ln@i\x0001Õ'ç«?\x001f± \x0006\x0014>ß*¡\x0003cÚüÝ\x0003ºOVè?lv$Ùà\x001agúP¸«.\x000bG«½1¨+Y¡ÿNÓpTªE	\x001fA*G¸¸ÝÄIÂ²F\x0003Ú,ôÏ</p><p>\x0007\Qºár/ÃÊJÎWÀ\x0012É¡°p¿³ÑÄR\x001b\x0012¤©}48*XUh?\x0011ÂA 5@Ù½a],}.¡j¥\x0001Å§j\x0014iä3\x001aaò#Ä>¦\x0001ç\x0001«</p><p>åmº|p|Z£¤r®éNÑ\x0012²V\x001c8vj¾+</p><p></p><p>G\x001cdw\x000b\x0007ÿG\x0012ü­ä^ú\x0006ÕªÐÅB&
ÆO&3nè
%¶{ázP5Ú\x0018×!ÝtiÌ^sCüöÀk *´1>\x001bÈ«°åV\x0019:7Òìe¨°ðRÕø¢ÁóÊ©´Æ9})©Ù\x001b·\x0017\x000eèa5_\x0017ãøà\x0018xê9C\x001e\x000eq)â>ú\x0018çâêù\x001a09\ôø5Ñc\x001dvÆqü±ô^\x001c6õ|\x0003\x000f\x0007Y®N9ü±\x0002cÚÊØ\x00037\×ÜrìAþ\x001f89t\x000b
<µö\x0012\x000eÜ(]s«¬?\x0010\x001c\x001aìr©b<iªl+
\x0008VW8\x0015Â­ip\x0016µÏ4¸ß'ÓX·Ëeà\x0010</p><p>S\x000eú\x001f\x001fS	\x0007\x0007pÒæ\x0010Ä1éE]#£¹vÜÑÌ®.\x001fÿíç«Trð\x0002þ|\x001b\x0013hAÜlv\x0011ý\x001e@²1­IÀ8\x001a~¯ã£ÃÅÏG©Üà\x0005üùD¤«CcKUT\x0012ÜÀìiÜ2\x001aÒ\x0015\x0003ÍHQ\x0014ø?\x001aÞøz¬\x001cdªÃ\x0012ÆâXäòð0v*K+PÐ\x0000þoeØ+Ç*Åå\x0003yeððØ\x001eäïâÄ\x0005ÿõq_®\x001cyª©\x0015å¥\x0003-\x001d+\x0003øÊ~o¬\x001cô©ÃX[W\x0016%°8~)9g°\x000fW¸TratC¸\x001c""\x0017~]×P]Usq°£ò|<¼9	L\x001cdyáÈ\x0011rM\ôí§Ûß;ºë·«ëëÕÇT~rõñî\x0012[ÇS	ú´Vu\x0016ké
 có&Ò¥\x0004w0\x0015\x000fV\x000c¤öÛÑññòe*D?9zyv
äg»\x0019³&kbÄD:\x0002\x0006¾\x0005\x0002\x0003}\x0004\x0008NÅÓ\x0000fÖ\x0002h¢N\x0004
¾ì³QkfCCÐÊõ[\x001b#<bùÄJ9zü\x0010\x000e\x0001lç\x0013}æ¬é\x0008áü©HRÔh*\x0012aZ×¥ø49îÞDhó<\x001b$\x000cæÀäËe|0Úá#¬1+æ\x0016F\x001dÓøÄ(Ò11r\x0016{¢ûômräG\x0000ü/×\x00121úhIÆ¹§aÌ¤I*·ë\x001bì¥5¬\x0018ñm\x0019½×êI\x00189 ß$H\x001c\x0013l³ 1Úå¨\x000cGª$Ý\x000c_ EZ\x0004ú\x001b<x·\x001a|åèYñô7þ\x0018Czß$9bµNþÖi\x0018M£\x0018fª[\x0019)!ÐÄè\x0002¥#q\x00046]&Ho\x001dlm\x0006\x0012\x0005-</p><p>\x001eD¬5ÎlÐùk{­IûHýD_Ò\x0007M´÷\x0018¤Ä÷$úÓdh\x0019øVHÊ*4IÒÃ#ÎfIF\x0005ãIÖ³5ôêÎ$å\x001a$-+.CzOAR<Å{ôO¤$)\x000bÑv&#ºdÙ¯pØ\x0016Ï¤ÕÅ;{3ÉÉ¶3)²ID5)Ø$</p><p>t}IMºð4³hêµ$\x0007ZÑ)5¬&Ã\x00131R"£Ín\x001cïD
/­\x000c©\x000c©É ÂÓ\nNo4\x001dÉè#éDe9\x0017C\x001a(bzþI )ëÑ$I§¸&5Iº\x001c/·ü¹õÓh Î4IÒòh@WÜ\x000bÍ:'÷g¤\x0004IÛµ1\x0014`\x0002Bae¾7l¸Ý0ë×ÊH\x0016FáR'Rb´*\x0007Á\x001coà»­özÚ|}ôïï?vb\x0015/Vo¯.·F|á¢º4k\x001b\x000b\x0008£Õ8þ\x0002\x0003\x001ewd¤\x0002Bm\x0019Á\x0017ËgGç»\x0019r,b\x0016CÐ$\x0017\x0013@EÇà)\x0006{\x0007\x001a\x0011r´a\x0016B\x000c\x0014\x0007´éE\x0011b¶\x000cð/b\x0018\	s¿D.÷2\x0001²óÄ\x0010ßÈPâî\x00109^0\x0007"ü5ÉÁz\x001fáH\x0010ÆÚ6AäÀ,\x0006í('bÐ+³ùc¤ñcùH°Y\x0010;\x0019òkz\x0006\x0004Ñy01X,=Nqt\x001cGJ\x000c¢í@ðKt °«Zúü1#ÏÏ:</p><p>Ö ¶\x0018\x0019æ\x0008~ÇÍ¢\x0000»\x0014ùHh\x001c\x0014à#k>\x0012²íHðCm\x000e\x0003n1·ÒK\x001c ´ \x0008kNðV¿Â»ðýjsX÷xõþêæÓêÝ®¸Éåßøt(5v÷á\x0010Ð¤&?^þ|tòËòùn¶Q8w&[ùüöRR\x0017c¸í©=n\x0014ËI§myÏàK6µ</p><p>\x001b
?ºµMt£(îL:ìs¡°òØCåC,ºa±b\x0013Ü(;\x0013NêÔ1´\x0012º\x001c:\x001b¦=±ùt£àíL:lj#7Ñ9lÇJÇN(v¸voæÓÂ¶s?lHc5PvFrÉ°P\x001cÚ	jX\x0014ÑD7</p><p>ØÎ½²>W^j\x0016Etâ\x0010iéíþl£@í<6Üßjd\x000c»Í\x0013üDÁ¨Ùþp\x001b"´3éÀ<\x0007:u9qY¶r]]'MlãÈì\¶ÜñÒ¸É`è¦\x001f óáÆ!Ù¹pd×qkL¹®ó,Áè'8s\x001b±séTö}paLê\x0011É¢[ÇjÀHlÂÎ¤CíKWBsù\x0007~d\x0012×["IóñÆñ×xð`\x0017ò*zÓ$.ó¢´Ê°s¤n\x001cÓI'uÑ'!P?\x0000nç£Ì\x0014¨â'¸\x0017\x001b\x0002sñT~¡\x001e1Tª\x0002x\x001c'ê\x0013HoCp\x001e\x001ev-°îóÑsQp0fØÛÑD7\x000e\x000eÎ\x0014P\x0007\x0004\x000bhsÉ>nÚäüÉ00Î\ÿ°7?\x0006ed\x000b¬\x0010ùõvG	óÉðcÈ\x000f[óÓ\:ª7×üzz1YÕÖÁY×ÍÃñ2a8'-âÔü¢Ê½Áñv¢uéØL\x0001Á;;\x0002ô¾1o\x001c©3\x001bG
\x0005µ@ë±¹_,äB#øhà~\x0004"2¹ \x0007>ÚHGÔ\x0012­«Åf\x00129êT\x0004\x0019¹4/\x0011)*â±Ñ\x000f3\x001cµDÙí® ÂëEä,¦¨³ò»\x001cDd÷=×Ù­\x0000²6çü°ÊÀSk©µl6\x0010M\x0016EÎ#b'±\x0002I¥A+ùòG, B$C	>'´Ýï£±÷5È¢Û\x0015è\x001c\x0003Õ¡\x0016\x000c8GnØJ4\x000bémPßÝ·v|¾º¸¼»Ù®°´Ò\x001d\i\x0018peúfÎz.dÕj\x00188¾<sxv\x0002zz\x0006\x000b7ÔÏc\x0001w9Rua4ÔdåçR_-A·*\x0016n«Ç\x0002\x0007§ÈªÍÅ3(a\x001d@\x0015IÖ3IX\x0005¥âX*Íd©\x000ccÓU,Y\x000fÎæLÆ\x0018uÌbqÂ+b	{±d
8W.ðd¶ôÇ<>²ÀÇb\x0016#Ô\x001e,9Ì0û´rZp¥Uf±ÚØq\x0005Þ>ç%+â¹r±B¥ RÒì­ðE.û°ä ÂL\x0016\x0013ãÍ(ÚA\x0000+\x0011Ê'\x001aÖ Õ °5+\x0017é2	ø÷.°/ô°6s7I¸þëÛ÷SAäÇûû]DAÂ	NÏ4¯µ§z\Hn~[Àìâü|ÒYî°m\x0008"ÏaÃ&ÉGõ</p><p>ëwÒ3Ã\x000bE4«£ÙöÎÉ¶!¼MaiV~}{GÓ!rô¾µÚ\x000cÛ\x0006[Ø6\x0004çÈ-¶\x0018KÁñdIn>2ßR5mCüxÜ|Þr³Ü\x001câµ J"«µÜ\x0016ÜÉ¶!z<Cn³ÐüMC.aô\x0016\x0008Äfý-l\x001bbÇsä\x0016\x0014ûµ\x0012îi\x000e§x­$³É­Il\x001b"ÇsØ\Äh*ßØ(À\x0008d[Ê\x001efm\x001bÏ Þdû\x000chFÊõF\x0013\x0001\x0012ûkaãYpyË«Á1,7*¬òÃ\x0016¸Mqã9pQa3ßSI\x0011(o\x001cxàn@ÍÛ\x00147\x0005\x0017°3:Á	Nß\x0001\ ÏªF#+Zà6gÀ)ÍObi4î\x0008C6\x000b~\x0006\x001f¹­\x0019¨lÆs\x0004Ã5XÃ	²öÞØ\x0002g¶\x0014iÏÛ\x00142#8c\x000b\ÔÔê­â»ê¶æ³g²m</p><p>\x0018Ïa+ù'¯rV ±\x00051aº&{;üôn¥þìxpG¿à2Ð²ßüæauu³µª+´')\x0001mK</p><p>ë
\x0015ßGÌÚöù^½Æ eÑùÉåÑÉÔàÙ\x001eeöåÚ(-Õ$Ê|52X¦\x001c¾</p><p>Ú)³W×J\x0019\x001dQúµ,#SáÈvÊìßµQzn÷ÇÛQs¥dÊa\x001a¾2{zmF}HÁ­Ü\x0000©\x001cCú'\x0013evùÚ ËÈ
)\x000cÍÆ\x0003JÃ'\x000cgãµSfç¯Òé´H\x0000)u)P´D\x0019ä0ÒÐ\x000e½À6ÈH\x000eóW	Ñå÷-"Ú';Ù\x001dlB\x000c*DÒRaõðÖdÊa%q%åÛ·W\x000fW\x001f:</p><p>ý\x001fK°1oo\x001foàïßîÈÊ\x0004Iº\x0007Nb \x000c\x0002Ìl>L¬á÷òÙéÅÉÑ£Ó	\x000bÓ\x0001Êº»\x0002\x0008\x0003\x0015¹ðNâ(\x000f9±.Ò±\x0003U8Ì8T\x0012e=]#"K®µ\x0000\x0013 \x001eA ¡\x0019®¤Éú¸\x00067Pø,\x001føvÙg±Îä1w(\x001fkö"Êº·HÊ´\x0011'ÉÇPYµ\x000c\x0003.NØ\x000b(ëÙª#D­b8ª'M\x0013J\x0017NÐ\x000bqø<¬\x0004Ê*µ\x0002\x0008ózO¥G¡G*\x0012r{\x0011eýYóÍÀ»Ìî\x001bØò@³{,'\x001dÈ\x000e;0*²º¬\x0011\x0018n>E&Ò.k\x000b\x001e*ëøÉ\#£2ö\x0001¼2qÀW_Ë"£a~¸\x0012\x001eÊ5BÒz\x0006à I\>\x0013{|ù\x001e¾¦*èy\#%­(9\x0002R4\x001cÃÚèbÒ^\x0016\x001fÅ5H"-AÏHi_ONì;¾nv\x0018¯D¢·pÍS|©ôáÈ\x00070Öéòáöºoü\x0002®A</p><p>æ\x000c&Or\x0008½pyí^¦\x001f¾5HÎåÊAD¥"æ­\x0001\x001bN\x0017¯Câê¨*µ¤sT</p><p>)\x001fn}¼GCB*¨æ¨\x0006Éè@A)\x0005\x001a®h
.È#¤\x0006µô¸ûüémÇ|µú~suy½
Åç¥ï©ð)J¶"\x001aãÅ\x0004þd`ú_-ÿ~rtx<éÊv0²ç8\x000bÃgqh,MpÕ òéØx=ì\x0018©ÀÈîâ,\x000cÏ'r\x001d\x0018vVe½£5·¨ÃSe8î©#;óÄ!5P\x0014¸¸=×£©(ix\x0003<ä]è\x0015\x001cÙ=Ç¡tª¯R k\x0004%^Àç¡\x0010\x0011¼:¯\x0002#;³0À!&Ý,\x0003#h~ãØQ|´#û3Å\x0011Há¦î¢ÜÍ£¢Öto­\x0019Ö»Wpd\x000fp<Êý\x0014ð]¼=ÈÓîgSd¢ªÄøöà¯¿]v[0á·}æ^\x000c8\x0006ò\x001bú\x000c(\x000cöZ¥Ô4\x0000\x001c¶ÁLÛë0P\x000bænh%ÝW`àáJ¸Qf4j7Ñ8z0gÈA;ªç\x0000\x0006M­ÐØoÈ\x000c#+<0gÈ\x0001V\x0013B\x0010·\x001fÃøÙ\x0004Ô9C</p><p>B\x001fø\x001cjòàâæ¼»1e:¥\x001d6[ÌF \x0006Ì\x0019\x0008x%é@FÊ©1:FÖ\x0003uÄ\x000c\x0006Ü1 h.&èÎ¬1MJgf9á ÊÙ\x000cÔ\x0004:C\x000eÒæâ\x0015\x0015à#æÆ¨@\x001bM\x0019ÖWÎFÈOÂ\x0019\x0008hÎ)¬ç¤Úe£\,\x000b)Ç¹\x000c¥\x000fuÆ·\x0008\x0013\x001cÁøÜ\x001bmtdýdìp¶Þl\x0006zöÍ\x0011á~Ü4CÖ Èã\x0010Ùax6\x0004·ÂÎ96×Äà¿m©\x001f\x0017\x000e%Ïd6r\x0018ß
Á­°3$á\x000c5ìc¦\x0015£;I\x0012ÚÑÍ°rÔ&>\x0017\x001es3 àQKc+\x0014.*ÎõnF®·¨á\x0000Ù\x0010ô|#	8\x0008Y\x0010!jÜî\x0004¡xî<\ÏÆûÉ#æ\x0008Â\x00186ZðG\x000e\x001a\x001b\x0011xð3îBjd 7ã\x001c9ÄÀÙ	\x000cæF.ÐSî\x000eÃv¹\x0010üJs7¡ªC¸<ä\x0019 ¨a^èQ\x000bÁl\x0008z\x0017Î\x0004<Âx1Ôog¤çÅ'àBT\x0019põåÊ¯ZN®/\x0017¯no\x001e>]^mw1½VF\x0005êTÈ»@g$	p\x0003ÅÕLúêô\x0004þ£ÃÙ«v\x0000\x0007M(³\x0001Hï¢\x0004Õ\x0013I³Jí,\x0015K;4l\x0004Üüîð
ZRæ\x000b0XÔø,°¥6ÏÍ\x0012àN¾AÊ|>WJ¢ÑZgQÂgçQ½b²/¤oÐ¯RÁçË\x0001Ä¶@æ£Éýp\x00009·6¾A÷Ê|>\x0013È»ÐiÞEîUð,"ùBm|fª\x000bÌ£Á!WÄçB\x0019Å<ê6ñZ[*\x0000©S\x0016\x0000áñ ï\x0007nÅjæ³÷_åý}·«äñóÕÍj;\x000b 2O½»päò4agËtÔQçùÅ«£åô³úýÝÍõýÛzxµx¾úË"¯våeÌ@</p><p>\x0003\x000e¹É©0N\x0000O¿aÅßZNËÅóå?pµäÑtê¹Ã8TÅ³\x0019#XNÚ¥ç\x001e3\x000c\x0013ãoYÉ8TÇóå¸ÞÕX\x000bh\x0006Ef\x0018blf\x001cªäùr\x000fL[\x0015\x0014:h$GÎ\x001cfÆ¡Z/GpÕòZ$Ç@çÑ"Ç§\x0012ãz\x0000}­\x00181UÃW=l\x001b¸s\x0016®Ìp\x0010S3ãz\x0018}-£õ¼PYÍy@JA£*ãVÆî`úJH\x001d\x000c\x0019hê6Ø5®rjÚ\x0006WBÂ¥M\x0017\x001b+:xÝ¤2</p><p>{m!å0¿Ó\x000cI\x000fÍ&H[¤V\x0004éÒe\x0014Ã\x0015uu\x001fVï®ßdiÝ>Þÿùx¹}\x001foH\x0011Üô¥-:¨¡r¶¨bôS§ñÙéÅùß.\x000eßL¹ú\x001d²}Gæ¢£Ïkáñ_ª\x0017&i1Õ[°6;\x0008\x001dªEK%Q=#µiì[Æâ\x0011g!L\x001eºùd\x0003;2Ì\x0013\x000e¨æÅmjyàSa\x0014´là4Ï$\x000b<ÞËZ­ypK\x000c<²1L¿vÙA¿ëþËûÅ³ÕõÕåÝö\x0001m\x001e7Þ /P¸5>\m
CÙ8\x001cå~|x¾x¶\x0004´³É1m·¯¼ïn¶8^-W\x000f»T DµÆ±Ùò<U>ÑÍcL\x000b¿9Ô</p><p>\x001d\x000e²÷³8¤¢³­$6¨jªß+\x001cb8ÿ§ú,\x000e!\x000f¨xÕFêµ:¼\x0003æ])ÈlÏ¡èDS5£g\x001bÈ\x0018vxfc\x0014Ë<\x0003+Ð#®*ÒMô\x00111¢</p><p>\x0010¶¾³@Ð]ÉÇ\x0003Î)?H¤R¸\x0018é®</p><p>\x000e6°³8àµF\x0016UÙ2Þ1ð»(Ä=>\x000c\x0005Rgq`?7m­,6\x0003&\x0010Õ\x0000¦}XÂ¼\x000bÄ\x001fâM¯ãæê¿þÏN]¦âbiÓjÖe`Ü©Â©á3ìÕò$ë±)wúæÛÏ]Mvû¸x}·zHõÓÿý\x001fÿ¹üþq«||t½qüçÓb\x0014xôË\x001c(ÑV\x000e÷¬\x001e^,^-ß¤êéÅòï/§J^ß¾Fë¤íKÿëênõyµ]`ØèÓ\x00012zï©bQhÃsÎÐhMX¤ÿut¶|µ2\x0000\x001fîxÕ\x001diüÛêÝ§Ë»«TvþruÿnÇ´
©À\x001fËý\x00058%j\x001dvÆçCeåhõÒò9üÅQ*9¹<Þ¹1	G=ÖupÂU7\x0016G\x0012æÐ5ÁÒ\x0017\x0005øa_é\x0018nÂrÆ«÷ï\x0006_4}ÐW«»Çí\x000e\x0006FhÔ
®B \x001c´\x0014Î¿·bX
P>ç«åÙÅwáßUÊM¾õëË»¯W× »;§$4Ï\x000cÙ´<\x0017ÜnF\x0008~Ð[öúðì·£cø7^^l¹©\x001dÊ]C)EÎÛ\x0002¥·%HRÖ,ééSÕ\x0003¿»\x0012Ðt\x001e©­ç¡×4´\x0002 GËNÚ!\x0007.x\x0005¤Ç-àyL¡ÆN]\x001eLãÎ´qSg±\x001ar\x0010Ë©¤£ª
g©Ó\x001cÌ)§r2</p><p>QM9x3Ô\x0012\x0013î¥Ù¶Ö\x0005OY-wÛ)\x0007A§*Y:ô\x000eRE³%ßÛ\x000f¨\x001cä\x0004j ÎÆ\x0018D)\x001cps"µ8âÉ>ø 6VC©4µàG\u£Iw)=,l¦\x001cå/j0u^ \x001f;Ê­×e9=È¬r\x0018Ã«¹=<n
d©\x001erô\x0002YN®¾¬¦\x001cÆÇ*(]´<\x0014Í¸'/ÚòõÃ6ßJJõîëý\x001f_\x0007!çw·?.·/\x0017ÆE¾á@äL\x001f×§(h</p><p>6ìhK\x0019\x0008^üãpËzá\x000e\x0011\x0019ì¹DàÒ\x0008\x001e!\x0005GÛÁÓ¦Ê	7Ú¾2èúòÓcXM¤«~[]_><ì\x0008sâ.ZZà-\x0002NKG¯58r\x000cálrþ¶<>|óf:ÆÙÁ\x001bgªæáÒ\x000fkÁÜå©#\x000e7u\x0010ßhÀl
ßýßßÝ¹\x000eß³ÕÍ®}
àµb.u\x0002`ùb\x000bûh¸\x001dH
ë\x0005-O¶\x001có\x000eCv]f0 áÊCÀà¨s!/<È&àÜ]UÃððáA¾ÿÞ9F/oïîw¥C§j	,v9 \x0018¾¢	AI3¸þ/OÏÎ§?E\x0007!9\x0008ÆR\x0012\x0013«ò¨|Ô\x0006VAák6Cvuw3H½ä\x0001=\x001dj+\x001bCpf~#C>\x000e³ä 0\x001dä\x0000\x000f½\x\x0001ràã \x000cÙQ#\x0007¬X o\x0011KÃu¤ú´#\x0017[¿Evðf\x001dInÓ\x0015¸KÒ4í\x0016\x0019\
Ã}üK}¿ñ\x0019¹z¸¼¾Þ¾	×Ëð2+ô;ÒW\x0001Åe9¶£§ßË7ÇÇ³À/ÇY``\x001es\x001d\x0007<\x001f\x0003)ULÅ):M¿!vßÝGe7E\x00030ôtxÿp·zõ_ÿwëw\x0004\x0013Éó\x0016\x0005Vç{ÊGÐåRúÃó7gË¦VWÇOöfÂb>[Ý?\½ß!=së\x000f\x0005Î]3¹\x0001KY¥\x001du[Læ³åù£gÐ
æ,:,ñY\x0017 Á´&÷CÑ\x0002µ Ý(´¹\x0001n"\x000cÕ¡\x001b\x0017uÌ£\x0003m\x0019Hv8\x0007(Ó©@Ã#\x0002vE>ìÆ¥\x0012óè§\x001eVa¦\x0014¡ÖEj5\x0019ÚI÷M}øýÓ§~ø=xÚ;F\x0012	Ìçä¾CxÒþC£ D\x0014#¤WËÁ¹Þ2M²Âý~óPÐâ'\x0014Ü¦\x0007\x0018p¦)É$Æe\x0015$Üò7\x0004\x001eÅT\x0014Û¹<\x001e< ÊÍýX¸ío\x001e2<ÌCkî2¦À\x0016®ÐÔ{pßß<\x0010)(,qG*õóàT+b±Ã\x0007Y\x0015\x000b7ÿÍ`ñi\x0017\x0004µñ£g'Ã\x001aÓ\x000b3Ë¨õº\x001bïf±àVµÍ*ªÒqf¨\x00151aÖ©\x0006\x0011sY´ÃI\x0014Y.Í\x001b\x001b¸ò\x0005\éj¹wáÃ¥ÙdÑÎ/ßÁãôË\x000eÇ
Ëÿrä\x0006;Ñò3Þ%·+=ã½4gçø@}=5mÍ5°eó¸¤¥ \x0008:O4N=:sÂ\x0017</p><p>/ÌÆ\x001aça©ÀÛb0ôc3\x0017*À»k¸¢n.ýË¼¯x~ùåáÃ®>â</p><p>¤­dW\x000e_õù@I1¼ôç¯ß¼ØÖÐ!Éßm\x0016Ç\x0005á¹Ã\x0015JP0\x0015\x000ci£\x001aü©æà`\\x001afã\x0016RJ	´@Õ3ìZªáÈZp¦D¤á	4ÊE²Ýé©Ê¶{PØI¢ßs?\\x0005òoìãÜÞí*j3gKÜÌC·\x000b#ìh\x0002ZÏ½9=tªíÇKõAwUÐíÍÇ¯öm;\x000e:úyþpCN+O\x000f63Þ\x0006rzòò7 ú÷I\x0011­Ä>t\x001d­³ÇËÅûÇ¼_¤åDÛÄ×£ÂÇRhÜÓsZ\x0008\x00147°pvq¸øù"ý#gçù\x001f1/Â1¾«\x001fï®¾ôr§XuûøáÃÎÕV©Ü\x0000"±at#÷Ï\x0004xøêÞ±0ëôâÅéýîãÇwºsÖWóÕÇ]óßtôTo´+\x0013r$u¢á®68ßçË[Æ½u0J}Øÿ\x0000z÷ûíbÀ»ærqqýy»&$=»$®rÉº\x0019þñ´	$ê8ÌÎÀcæpqqüjjé·wB|éZ«ÕÃÕíÍâ=¼òÿëy¼K¹+\Ãý`RoM²¦öCÏãüÍòÍÑéÉâçÅáë³ôç\x0013¿¯·7]-ð|õùË§ËïÛë\x0011bj\x0011Ê;ª-NëJH:¨HUµbÔ\x0005ý|ùêõ/ªDèpð*9\x001c&÷$\x000ep_Ó
×1Ðj!s\x001a</p><p>ÅÄË½Á[8faàaI\x0014®ÌÕ6©c4s¸¡·ºãÛí\x001f_ú9ÅóO«Ïo·\x0015Á\x0005,NyÏOSWr\x0001vÃÇç¿,_=#2éÆ¯i83\x0006{Äó°\x0017'±sÁÐT\\x001b\x000e4qä3WÑPte®l,-)ÿ\x0010ø\x0019yÂ¸w\x001f\x0015÷h3\x001ce[GCÑ4\x0006Wëø,\x001b\x0011È¦+ln#Qð\x000c\x001aq\x001bÂý§¾\x0015x~{ó°ÝßÁ^aA}ô©ÅºÇU¤ÖàÇ\x0006ËÅóÓ7[</p><p>÷¿¿}wóþMï­³ÛÇÏ\x001fowy=\x0018ÓÌáÍÈÉ¹r\x0017Kïî\x0007Ä«Ã§[Ü\x000eÝ F7Îp5º\x000cV­ð\x0003NÖª«+àÞ¿ýöe\x0018POîë³Ç;´\x001e¹Á\x000e@Ë\x0019^ð\x001c=·ä{\x001dx \x001f®\x0007ZW¦_¡	9\¬Ö\x0013ºûS¸yw½öåÝêæãîä¥	\x0012wÊ#¤t 5dvá¹=	ùòlyò2å.7³wâau×aã!¹¿^®n\x0016ÏWwpO·Ï$Âò\x0017\x000e\x0015Ã-pXEª!hÍ\4ÓÄ=\,/ÏàÆ\x001eNõsv\x0000û£Äk\x0000Î£âqÃ£qìÖKvt\x001bn8©"V\x0000×£<\x0018Ò¬á\x0019\x001e\x001e&¨)Ò©t\x001eXi¹¶ÚØabrÆÓáí¾^áS]>UË\x00175§«=h@*yqéF3jÏ'ä@~ø§ÃyÍ¯n¯/·\x0007ÞqV+\x000bÁAUeMåºB\x000fúÓ_\x001e\x001fþ<TuIGãíç¼!\x0000[\x001c4Y~k\x0015¥{ãx·w\x001b©îFÜÏ"Å°'Me7º\x000cäÔ´L;Q¯ÔtIGcîgÆHQ\x0000ì /Sh-7\x0006\2ÓNúVÊØ;§ÏàoôS+¬â¹úÏð\x0017ð7w=¿\x001dµÓj#-mÉ³v\x001eGz¦\x001b\x0003ÏNþ\x001d\x001fãðæ*©\x0006k1ÔL®£î\x0017o®®¯/\x001f¯wUAYw ²~\x000fR8\x0001<\x0007É«áØ|õÏ\x0017o\x000f/§ãPPu	U=¡ ap¸¢gÉ\x0007Ç¡y+±ºzBÝ%Ôõ¼Y\x0013Ê<Vðúm\x000c&}	MÐÔ\x0013F\x0000Ã{®\x0002·\x001d0¼æõ¶\x000bh«\x0001½Ìuô\x0008hy\x001f\x0008Ü"ÇÃ\x0014f=¡ë\x0012ºjB'ip	ØpÃãïÁd\x001bi~F=¡ï\x0012úz\x0019bÅÁÝe\x0011òÎ\x0005ã9¬ù"\x000et
ü¾\x0017ôjuµ+°,¢)nPÀ¦Q"tÜë:åf¼Z\x001emyo\x0015BÕ%TÕZñGËQF\x000c\x00185#á¤£6Pw	u5¡÷ì§Q¶9\x001c&hQXJ}íÉgº|¦/8*·\x0003	Z¶ÓQZ`ÜÏvùl%_*Å£K\x0012eä\x0008ß` õ¾Kèë	\x001dáyJÕÙhøeíà«7ã
2¢ÿÁÚ«×W»øÀ#×FËM\x0013plìÌ0¬ÅÃÇG[*é</p><p> ê\x0002ªj@\x0001ê9?ûAGO)\x0006ápBd5¡î\x0012êzBÅc\x0006d\x0014ß¬±Üáa</p><p>¤ÏtùL=ÐyÔ¨\x0004©ñ\x000eH3\x001d±\x0002j³1®\x0000´]@[\x000b(b´<"\x001fë{\x0005\x0017\x0016S=:3\x000c@U\x0013º.¡k \x00144\x0017SbÅ©&=¨8,s©ö$ô]B_Oè<m?Â¾JV\x001f8&áìp Ä\x0010pu÷îòË$]èÒz:lÜ¥+âÙÁé®,¾aËA­ø¤è©AQOhËö!¼%4A\x0000\x0003v¸ù]RØ×ÔÕª\x001a>qY¾6!FÍ\x0017Ù
'HÏGôC]í\x0007þÖñjWì³a4ÆÚÚ\x001d/·5m\x0014>Ûå³µ|Õ#3ªù|Ï×òõFiP¡7Jc_ñÅ.^¬ÄK36b±AÍ_Îýjvc
B\x0005_çøþ
\x0007Ø\x001f¾¡ÝxøÆ¤·5\x0013P÷\x0000u-`(G.ì
å\x0018.®¨\x0006ì]\x0010Y{CÒ´\x000eIã:\x001c9ýq\x001dîôLÀÞ
µW\x0004ÇxPo\x0018ñ0ÇxðEa'_t;\x0000¥\x001b¶]</p><p>m¿¾^½«y·\x0007ï¹\x0004\x000c\x001b·-Þ£b4à05ûúxù|~la\x0018Öv)¬]K\x0019\x0015§lÁgu4æ	Æ<êÌá\x0016JÝ¥Ô
²ÄòsW\x001eð$\x0000E\x0014Ë\x0003^ïOiº¦AºD»P¬\x001cÒ4¶<B³SZ(mÒþÜ½Ír\x001cG.ú*µ»«ÅÿiU$K\x0014 .@ÈNk#+\x0012%\x0012\x0012\x0008P\x0005ÝÔj^ãìÕÌ}
½Éyë\x001eá\x001eY¨ÌÊÌÊ\x0014©1ASh¶òó\x0008\x000fÿÿ\x0019pQQ\x001aCâ\x001féÆ}ÉÙ¸=jv\x0008JWEé%6#HËàù,ÙÛÛ®(\x001d\x0002ÒWAú\x0001 Eàòòà%\x0017*c(gó·§\x0008\x000cA\x0019«(ã7RÖÅå\x0000yù×À¬½\x001e9äùõ\x0013ÙøV\x001ciòskOê¢\x00061æÏo¯ïëÌ¿øÆTmgªT	<]¯ÖëÕl&\x0001]¯fÏ\x001f÷\x0018\x0003.X¤du æ5ëådÙn\x001bA~v¼8?_Ì\x0016i&Ðñböü²5VÆU\x0015²\x001a\x000eÙÞ°eÊwË(¼\x001a\x000f³®bÖÃ1kC
ÃÒKË
Ã^q×Ñ»,§M\x0015³\x0019\x0019w\x001aDJ$ç#a¶¾ä@vÅï\x0007bvUÌn8f#8\x0018+;id°çm¦Ñà\x001a±0*æ0\x001c3ö³Qª	£èÄ\x001bR2?\x001fX\x000eáÍ/*úÏ_Öwí¥ARl"4\x0001÷{[êZâÞ</p><p>»=}JàÏÿyþºyü{¦ªÐT?h^R°\x000cÖÐãrBiÃ6ÿvPOlºM÷Ãflµ¢\¦\x0018¹ÔÂ¸íÒÃØL\x0015éMqd:\x0008n\¶ ^Ù¼?ðÔl\x0015íyjÍû".Á¿\)·==¯'6WÅæúa\x0003ùí\x0008[\x0010%\nuÁ¶]nÛ\x0013¯bóý°i\x001eÞ"1Úa5gkXüùí¥à=±*¶ÐóÜ\x000c\x000eþÌU	Õvâ2Â¶]tÔ\x000f[%\x0006ÂMô\x0005Go\x0014@10¾Ð'\x000b\x0012»\x0001{+¥®¶g\x0012\x0017\x001fb¯ÖÃõýýêãêö*¶þüÏ½%[V`@(G×¸§Ö\x0010¸\x000cÎ=mÜzs|q±xµ8}Ó­fK×äI\x0002k¾M°Bê-}ã\x000c7úìlíõ\x0017Ëû\x0006û£Ç%\x0000q³ù\x0018t.{¼»ìß\x00178{5\x001bì/æ¯ZÆü\x0014 ª</p><p>T
\x0002</p><p>\x0016$'H$O¥vØ=©\x001b\x0006TWê\x0001@SÑ\x0002-¿\x0010Êq\x0019d4\x0005ÐoG!5U¤fÐbµ3EáÆùN¤\x0000ËÝsù®Ô
B*%eá¨ä¸im' ;³Ü½*Ò0ì=\x0019\x001a¥ðiÑ¾õÈ~O;\x0019\x000f\x0001ºíýjQ	\x0013\x0003Ô»ë«ûÙÙãÛë=

Q\x0008¶Ì°\x001c\x000b
/!Ý\x00019ÀúúøÅÅììòÙÉqó\x0002UU¡ªaPÍ&õ\x0018\x001c3jp,O]Ø\x001e»5\x0010«®bÕ°Â\x001dS*erÉ\x0004	BdóHXM\x0015«\x0019x®2BI\x0000ÐÐÔ`cÁº=\x001cg V[Åj\x0007«¥ÙVYQQÔ#Æ"¬¶\x0017ö\x000cÄêªXÝ°sU¦ä`à.;=A;Æ\x001a¶§\x000f\x000fÄê«XýÀs\x0015¥r#F\x001a½\x000eçjhÝ\x001e}5\x0010k¨b
\x0003EVI\x0010</p><p>\x001cHü*ÙöN©Q°Æ*Ö8ì\\x0003O\x001aP¨½(à#\x0017ßy±¯\x001eUÖUÁ0]\x0010àEEnð\¾ã+6Ëvãø@°5e i\x0003\x001cíc~²âd&Ø®Ö\x001a\x0008µ¦\x000bä0eÊ.YÇÂ°µ9·]2TqÕB÷IyUB÷ý kN cbÈåACÎ³#bð³ê\x0016\x000cøY¢Þ\x001bË!\x001fo®o»\\x001e´Ì#ý1+¯©rÅ\x0018Çå]ûpEäåÉñiÅðjh\x0011aËì_$ëîñ!Õ\x000f,\x001fïï÷µ¦UÎùhPì\x0019xN'ký¤Hîõå\x001bª\x001f¸¼¸hÈT\x0000ª*@Õ\x001f Áº\x001c>IM\x001e\x0004°(T\÷Fhª\x0008Í·ÐU\x0011ºÞ\x0008},!(Ü`Er¿Tò=])ß\x001fa¨"\x000cý\x0011\x0006¶ú<8Såg9C\x001c>q\x0018ÂJ,*P=ä·vÍ²öTä·øVdí­ÈþÅ;vp=²çæx:l3ôX{,²ÿk	C\x0010NG\x001am</p><p>¯\x0011º'ÍnýEâÏ\x000f«u],â/úâLêrW^dgÙózh¥:ô(\x0001hEg øþâGÒ0ìàøáú/ù¤½3P)¶£ÂÖ´à«Ç5þÇ³åz½ú£\x001d§wñ_(\x001bÓJ\x0001qÛEK\x0005æ«ËsügóóóÅO\x001b°Û
­b;ð(lM!öÀ\x001a¬;¢.$m(<î-\x001f¨Ùöå\x0006"ÕU¤úÛ>USÅj\x0006ªIº'\x001d«âÖ\x001fÜvÄYKý$½>\x000c¬­µ\x0003Á¢!Ï}Ã;Ñ¼PÆ|Ú6\x000c¬«u\x0003ÁâTX\x0001²¹*¢êÉ·P}\x0015ª\x001fz®Å\x0015&:iVDä\x0008´	ÛÃ
\x0006bU¬q V!)´+=:s´%%Á\x0016áIÓî °²._</p><p>Ø(i9 \x0015Bvnc<©ç\x001f¶&·ä·-¸dM\x0016ÈÂÀcþfÂI N\x000eÅ5Ö;&ìFÛ4\x0001L-=«ªµàÇ\ EÅ['Á+É¯ËYÑ\x0011cý;\x000bñºãPÛ\x001aVUkÁ;£TÜa	(\x0005wë\x001bn\x001f±1ápºR\x000f@U\x000f´JT:^ðc\x000ceh¬\x0005ïÒTQ!(E®hÁì\x0013'IMÙ\x0008	æêîØX/¶</p><p>Ò\x000e\x0001)9Ø(q	££d\x00135:\x001c¥«¢tCØRÒ¤\x0010¬ªbßlfÄØív!(}\x0015¥\x001föÄ.==$8Á÷ä¦£¦>.%\x0011à#×CuÉiN£ðÒäß4{s~{µÞ7Á&Õ"<§\x0015\x001båi©Rà.j'Ôöä/ÿ;{1¾8ÇÑ5\x0005ç¦\x000eqÛ\x001fQUäqvvs÷ñm.¹}XîýåC 	J\x0002ò\x000eç¹j·v¿¼~õ,\x0017Ä¾·TêÈíz:©ª¦~_ÀXHï\x0008Ø;âãBù$}?\x0018±­"¶\x0011c1àfî\x0012-8ue>Ô\x0006¹Áx}\x0015¯\x001f\x0017\x0017\x001cPÏa(óê¬+¯k·ïWÖYx0\x000fÃÿáÀµ,\x000e,÷\x0002YÅ9}Ü´3\x0016ä\x001a\x0013ËÁ\l­¥&+¥q¾Y6RÀ÷£}k`»ïö¯û@Þî/¾6;êr}	½µ\x001d¡4¹c\x000c5ïa\x0013Æ3MÓ­.Ï/0ÏÐZØá·³ú¾6©3D^H%£\x000cÈsb3mA>9Íî\x0018ÅvüG\x0008»5ócþøv½/DU\x0007kÔKÿBp¥ÞÐ>	Kr#ùüòÙyk(m;ê#Ý\x001aúÑ	¡pTkæg1\x0015ÊØ\x0019c\x0006÷t\x0006hª\x0000MÊqW\n\x0011¥m¥©S¶3BWEè\x0006\r,\x0008`à»2h­áÎ*á>\x0008C\x0015aèÐ\x000b?y¥¹ò±2%Ìl/Èì°\x0005\x0011v{*D\x0007©8ÓpwÂqÔ¹ì­37NÕè°öPdïðQ\x0016ÄEÁ\x0003\x0011N\x0010Ê¦¡\x000bû ¾\x0015j«zX¨T=Äg/V7³çwW«õ[Æ\x0019z\6}&dÖßÎÝ±Ûý\x00078Q\x001c\x0010Ì¿¾|±8oo«\x0015±=&¬	ïeªfÊv§aic½àÚ¸³C¢£±­UÄö\x0018®N®PÌ[«ód
Gq\x0004§Ø÷U»§ÕuA(¶{ãDîã¡\x0007ÜvYÃ[»í\x0011¤Ýo]l4MIóf®g÷Ã\x0015­x\x0015\x0002íl±F±Ï\x001eí®q¹¹ÝNy»fXlj\x0007a6ìuj\x0011øQ\x0019Í,\x001bÌÆ?\x0000³«bv\x0007`æ\x0019JJëR?h¸,3nïáîØû½wîÙcF»èåÇÕò\x00111­¾¬Õ\x0007Þ÷²yXÂ"µÑy¥\x001b\x000e[TyÈ¯Ó`|dAom^êF	º\x001fæ¯\x0016óK\x0004u¶øçùüM#¢÷\x001f¯®Ö\x000fIÐÃ}àÿÿtw»\x001dß^=Þ?×~sÄÀ3x^óëu#<M\x000ci\x0004ÃBåyÿÎa!ÁSÁg\x001e%|?½>]ÌO_\^¼\x0001Çýä$Égð¶æÇçXÿõé6ÞW­m)®f?®ÖW×«f</p><p>KkRÇ\x0005n}¥¢{g]¤T·\x0001\x001f¥zÕ\x001a \x001f\x0017ç/\x0017ç4*ý$H,¬únóï0{2ÿ¼ºåæ\x001a@v»¼Ù\x000bQ{JiMt9êåÔÔm¦Ìupþãâ»l\x0000ßéü¤\x000bPS\x0003j\x0006\x0002u&µD\x0003PMÙ#\x0000êh¼öÖ\x001dÓÕpº8áÎ\x001f!­ÆØMæJ%È×Ñ X\x000fG\x001ajHÃ0¤Z¤\x0000bBÓÆCFJ{\x0012Á9Ë
V\x0000u¢</p><p>\x0014þi\x0018P\x0019s\x000bêp$u\x0006ªÉj×¦Ç\x001c´öÜÀ×¤ÁSt¤ÂçÍËÔä5òÔÈ/ßÕØÔ
dS\x00123?|¥ç\x0006IljivÃ!H}íáû\x000f_ûÆ\x001d"à\x0011üò5û½ÚÐÁþHÝÏWâÝûr¬õÕ­îÑÐ[Ý\/1¾\x0011\x0008Cxëëå»\­þqº||\x0016M\x0003Tð¿Aab3¥Ö\x0011óñIZ¹#\x0004\x0010\x000bEOêüxþü\x001f/\x0016ÿ8_>O¤k­v\x000b´ü\x0016'Çó¸G\x001d:-í9\x000cznLEèà&åþY,ýÌ.\x0013@W|Ê£B§Ý,A÷.I\®U.(\x0003è62tÃvÊ¨ÐikæAÐ±Ã\x001b#&\x0008Ý#â(_\P\x0013 §EF!×2½JDî\x0002óU\x000f=\x0008;\x0001ô¼wò@è6\x0016èVà</p><p>¢\x0004Ýe»\x0011O}</p><p>äàú\x0007FdBû°cF\x001e
#7l[</p><p>,ß c\x0001?ZIÐUN	âJñ¼^\x0017¡)\x001e)è°x8t\x0002ì\x0008\x001d\x000b\x0014AÏ¥\x0000\x0000]«8>tÞ¨| Ç l\x000cåØ\x0005qL°Ì1:NÀìh8Êµi@mÊïT\x001dYÂn\x0014³\x000cMº\x0019\x0019;H\y°:¥\x0015Ò	;µ${\x001eb\x000fØm\x001cM²/¬ÄÓà\x0017sd-ÝC\x0012g7Ëë´)©\x000b	*¦R\x0003 \x0001Î\x001c=í,á\x0003±\x000eú×\x001dHÈA³ùqÓ\x000e¥*	¶J=d\x0019d¡ÛÑ4Ý¤¤À½íÂýýHðU\x0012üßP%!ü-IU\x0012âß\x0004)ª$l«oð³ûã­Y¯ª~\x0015JÐõÝ\x001f)SlL\x0006\x001b\x0000ìuöóÀc2\x000fWÅ¹,oq"\x000fÜRÂÓÂòù?1A$ãùë2Ãu\x0010¼Öô«àm¦_\x0015\x0004y-_\x0017\x0004oRýëA¬ýòÓûUÆäxî÷Ë·ëÕûÇF0Fj¯Ó@3\x00005\x0017)«¨3À(mª`8ûýüÙùâåe7Pmöß\x0010¨­\x0005ªß\x0006(bäo\x000b\x00141ö·\x0005|æo\x000b\x0014¹Ãß\x0000¨Gq\x0013í\x001f»D\x0002üËÕC\x0013$e\x0006¸þZ\x001bð»CvÇ>f\x000b9:G:$0èç'¦üX
Ð8øú¶DÁ×\x0007´%\x0006¾> -\x0011ðõ\x0001m=ÿ¯\x000fhëé}@[Ý¯\x000f¢Vß\x000c \x0012úÊ¾Üüñá>TDõóõê\x000bxD·\x0016¤Çý6"YÚb4&\x0007°\x000f%ïr!T<?_ü\x0013üÓfeQAeó×Dñ_àñ_·ËZÒl5;¿N³<w~?Dk±:©n­p\x001d\x0012\x0019qðá¬º¥3UnXÌÎ\x0006xÖ?ÏnÝWú<;tåç}XýêîvY+¯ë÷×8¢¡\x0001\x001bàò+ç©*£òêT\x0005ÿ£<^cëE¾¿¼<î\x0004gËVù*p~»òr}]gÍ³ÇÕ»\x000f*âåÂ¨ë¯\x0013.G¼=¬ÜÍÙåâù\x000f]>_Xóë|¾°æ×ù<G\x0019þÊÏ§µ[nçË¸»}X®ïã\x000c8\x001b7­\x00087jÉZ</p><p>xß¨Óv';¾>}3?¿hq.* ¶ßÇ×\x0003uugÍ/ÕÀåìbù>\x0005\x0012wC185$}sÎTÒçZha3\x0014AUb\x0019É|v1Ù\x0012\x001d¬|\x000eå¯ýþçûOË?~¯Ór÷øözµn\x0010­\x0016©´\x00075mOÌj´t$±¼Ï3T\x000b×Ï\x0017ç`cø</p><p>0¬ºúø\x0018ë§q~wÕ|\x0019>¤b1 ­Èu¶JëÇÞ*©M\x000c5\x0008ç¯_,\x0014ßÔ>\èoÿ0Ø12æ\x000fãm>¬øAÀíùa{>\x001c²Õ>³©ò­Ötèæìôø0IÈ=\x001fÆ¬y:\x001dª*Ø*¢XåÞ®\x001eß%÷tßwHÝï¤sÜ\x0015\x0008Î)oTÏºï\x0015\x001bºï¤]nÉÅ\x000f\x000bÊµ+m\x0002\x0005277öø.yû¾\x0003`ç\x000bÂ\x001fD1G\_Î"§r/½îHæç¬ÌI\x0019 7æ\x001c7|ØnI¶ý\x001f&çqßH@ÓA;Ü\x0008>ìré\x0011|X	ÓïÃÅIÜÇ[Ú¤M
ø±\x0010ó</p><p>8jò
áËÂõ|L¥Ü \x0003sùÌ\Øâÿ¹DìÉ\¥V`ßµK£o\x0012É>\x0017¿(Ìi8þrßw­²ärX|¾ìÍ\x0011É\x000f-éÃ¸½ç+d\x0007Éë \x000c}ØÉ¼\x001c\x001a\x0019o\x0019\x0007õü2¼@ÙAvÐLÝ6øe`r~Ê*·§ÁiqD/\x0003[ÈNÂKÁæ¤ÖyÐ\x0005ò'\x0006ÖtþËwï?ï²dO®o¯W_Öwÿn6\x0010ÆÓF«\x0011K(8<1_¹²vð¥åàøôxñÏó×ÿ³\x001dÐ\x0015Û\x0001$¸\x000cYf@âö+÷áÙ</p><p>HwÁÑd<pV94¥¤ «:ÒÆÞx¶âÑ].\x000ckÆé|ä\x001c§\x0006	¹FÔ|_@[ñè.ÊU\x0000È:Îx\x001ci$x
ê\x00008[Ñè.pL\x001e¯
¯JhZ\x0001
xáóñn\x001bÔ\x0015ÐV4º\x0013 ª©\x0003@à¢e\x0005fÐ '@±fÿö\x0005´\x0015î\x0002\x0008Ç@Ò\x0001©<­\x0012ðÄÍ\x0001C8z+\x0018Ý\x0001Ã¯\x000eHæ½\x0018ðWM|@î\x0000~\x0012îÈ\x000bÅ^\x0013Há<ñZ\x0019kÈÒØ\x0003®¬Ø\x001f}ÎH{öe@\x0004\x0013eàÅ\x0013%UÜ\x0015!ï
>\\x00145Å)\x0001Ë\x0005ñ¯ÈïJ°vEÄ\x0006K/Aä4Ùkà\x000c8\x0019ÛKzhèi\x001e->ºÃ§\x001e9Öð«e@¶¿n½w÷þæ¦\x001e²|v÷¸~ßì\x0006c@91³Ávâ|,Z»Üï °C¨V\x00143{öúòüeû§K¸rÏ§5'áM4!ÂÆU¥éÓð7ú~º*÷}Ú¥©7øéH]\x001eøi2k¤r±ïKrßyÇ4M\x0000\x0003øyùfú²Ï\x000cáÓ¡÷¹\x0000jï\x00156\x0010æ/ëÜá7]¢÷M\x0002Þÿiíkµ°üé<¯\x0013³\x0016ª7Õ¤j÷~\x001a+=²ý\x0001ª]\x0007\x001dÉ\x0019\x0017¸j«ï§I©îý´¤\x0006.ø4Î±Êþ?\x001djÆO§OþÜûi`­©h&\x0013Õ4L	ebßO\x0017M¹ÿÛ¢.VÊ27;hþ¶èýmÖ{¿m"ùÆ\x0016\x0007eÕ\x000cÆö8Þ|ßo³öÛ÷m\x00178êcp¸ÌÑ\x0017pMèe\x000bS\x000b7uú6ë¹½ß\x0006­ó_V\x000bÁ¢Tþ\x0017Fl%?:|\x0015Z')]D£Òd¦täÂ\x0011ÂJmû~ó½ßÆ¡Êê`sw4|ZQX\x0000\x000e¼?§±w¾÷ÄÁ¯\x0011ùÄÁÈ½0pâ\x001c-¡i¦Eo<]d\x0003Ïtt1oo{C	\x000cECïû|'ìÿ6ÎnÈBMZàòüi§ùq£"ë÷i\x0005BEu\x0012,Bï\x0006[\x0014y*6»·\x0016ÁH»ê$XÒ¸Ä$Êc	3jYÈVºïãRÕÍLÊ£iÒ·å%f\x0002q¶7Ù ST';É[\í\x001cN_\x00147tnß~/yû»­\x001a¦ê8Á¤á\x0014;ÈðÒlî×Ù\x0000õ-ì.ôùüä\x0015Î8iò¤"²\x001dÇÙ½é&Qi5F¾üîpÅ Ýåvò¤\x0016r\x000f\x0014ctFN1©9Í\x0015Q&ì®ê\x0000äI
ä\x001e  ó­ÊH¼Ç\x0016»,þs¼\x0000³Ô./¦\x0013'Õ{ ,´T'\x0006F}pÌ¬|*Þ\x000f¾'uû8%Ák¬\x0005\x001dEö\x0017hHbÚÝÎf'(O*\x001e÷@\x0001\x001bÌe³\x0004çèIº åiC°¡<©uÜ\x0003\x0005¬à,É\x000c\x000e7ðl\x0019:â\x0015Úø=\x0004É"Ç=B%ø< \x0000ÈÀÉ\x001b°Õ<\x001d»âÈ] ì(oÜ\x0005\x0000X:<6:a\x0011/¶½
Á²\x001dKÚÅF{$²°õåô/Hí\x000c×v²\x001dDÚ\x0007¥L3Àc\x0011%¿¦+Ç²+RÛå-x½¤ò/Á/(Fòjy&°µU\x0018é áBT´zs6DáXe~J±îA¿_¤k[µFÛT\x0015ú\x0006\x0000é* ý
\x00002U@æ\x001b\x0000d«ì7\x0000ÈU\x0001¹¯\x0005Èü|­ÿõájá\x001cO÷½X­×©>MÓ\x001c'óÝÅÏËÛ?ÿ3¯Þj\x001dh	¢¼´-º¨q6\x000f\x0014F\x000få»ü8Ç!¾<Ö÷bq~ÞX VC¬>L3T\x001eãp#BB¤Rpô\x0000DÙÚêÈ¥QÒ(È¼&\x001a\x0011aº(!2æ0@ÙæêwD)Ð\x000f¬Û\x0000Bû/\x001fQj\x0004>\x0000Q¶wú\x001dQí\x0002"\x0013²¼#DÒ¨\x0001ÄÕÛ_õ[D\x0019T­+ë<Oînß/1Öß\x0002Ë\x00060~òAI\x001d©l#Ö)ÀÒ\x0006Yµ	ø¿>}9Çÿ~h\x0012éG?l\x0018NµF¨lE\x0010\x0007"\x00106\x0016:\x001eM%?_ÞØ\x0004ô\x0000¹\x000e"\x001aç#lyÿÃ\x0010l¿­nÍò=ÂsSÕs;[ß}¼¾ù\x00037aÓ	Ä)\x001a¸\x0014L·4ü'â~\x001f°	«ãî;=;ýêøä¦ÙÀ5l\x001e£aÞöÆ¦,I</p><p>áu ~ó\x0007c2csz÷¹íÇööËÍ:ÏÜôððÿX}LÛlgçw÷\x000f«¶ûtê¦ÀhÇ«MÏÓX¯éÌ|Î\x0014\ÏX¼Jûkgç¯/Þ4UV@Ibx®\x0017*¬\x000bð\x0019\x0014[R8\x0003\x001dk2\x0013¨\x001cZ:\x0000T@\x000eÃ\x001f}@aJQÃ:\x000eÄ&Ö\x00178xï@TxT¡çQ)>¼\x0004@ÍQÉ@Y,xH?zXê=ìúG\x001dCÌ¦\x0003N v\x0007r\x0018+J?úò\x0011\x0013ª</p><p>\x0017U|Tà!\x001aB¥Ä¡¨,¢²ýP\x0019IH°\x0017S\x0005É¨Ãa ÐûM?ú[KQ</p><p>8*©rM>\x001e$Vw8;ð0T\x0001Qõå*Ã\x0004x.W![ùÈ\x0017h\x000f{\x000e#ÀéG¯\x000b4¹\x0006\x000e.0Ãå\x001bô$Ù]^s\x0008*<+Õó¬ÒÜ\x0017:+CÅÊi>+} ³kä+Ý¯Ëãù\x0000\x0015ÐTÞ\x0000¨¢á³2r;\x0006gÒ¾7\x0018ÛE\x000eÖnPÅÃd¨C\x00137ýè</p><p>wyGBeÈÒÂ&\x0011¾ÁC ÃÑéG\x000fT`%°½\x00104m*\x0001\x0011\x0015#¿Á\b9\x0018\x0014øZòÏî°\x000c$K²\x0018Í;}À
SÄ¨Ot\x001e\x0000\x000b7`|ö
ÒIåH,òÈ\x0016)ÀÒ\x0004+X7ßuî;óÄ­Ç±Q'Ëë\x0015®Jûñzu\x0003¢Z.\x0013\x0017dßL¦ué9b	N'M¬³ØfÉÂÉüøÍ\x0002¥ýx¼8Æ1R\x001dæôÎP¤4§\x0011z}¸Î&º\x001dNäP Õ¸D !÷c5't"RIGjsÅïHH«ñÞHCÈÅä-DlEJH¥±TÊ\x0011Ï´\x001aÈø¶Ï´\x001aàø\x0006.ãõÜnýGÞZp?{µüwâ7At6¤&7ÇX\x000ebÄÁSÄ*ÆºDªì-¸½ÿO\x000cæïª¶}-ðÑ\x0011\x0014]0¸¥$ÛÖKÑ\x0019Õ\x0007£C¿/ýèN»\d"°±\x001c\x0008\x000bÎ½"t6\x000e\x0005·¾º\x0012¿,·Åäãìû»ÇõìÏÿ=;[^ß¶AóX± é(%é?\x001b1®Õ(ñ4îw9ûþõåùl>;\x001fvV\x00117ý YGÐÜ\x0006\x001aYíÔØy ²\x0010î,5Ù"²\x0010C\x001eé\x000eÈL¤x²\x0011ñ©\x0004ì\x0006íã¿¾(mÐ2'ýªïô\x0002`=üãÕõ»\x000f«ÖPÌE\x0005Âjà6G6\¨¸Í°û-\\x0000°7³WÇ`L4MS\x0000Ãæßo?j\x001c×¥q\x0018CúQy
q½¾k{\x000c8Ô9÷Í</p><p>-­A¿,\x0005\x001eÈàR^¦Ç\x0000\x0000ÏÁ¼iöðÞ­äcÕ¸áÙ\x001b\x0008-·</p><p>çK¢àVÁ\x0014Ìy\x000b.UûXO\x0012ð¢ìò\x000e¸ÈBè\x000b+|ÆåÙ\x0016´!z</p><p>Íc\x0011ÛÁÀHÍö\x0002ùÜÔÒÀâQ¹\x0011y6ãu;\x0008\x0017)Õ~¸T<¢{D§#d\©*<¿Îzdk\x0010®\¨Ð\x0013Qyx2\x0002s¹r;ÀÀ¼:\x0014\x0018</p><p>ôD-û$j,\x0002Í	\x0016µyãÏaÈ¨r 'ó+ËR\x0005¦8sÒâz^â1ãÃÁÀ¨LµçÈ1%8²ÆG:²¢d8ù¹´'0¯ÉÑ\x0006µ©(¬\x0004F{T¬6\x000fg2ô´{³?\x001a¶©Ç\x0012)7ÞEèR^Øäbªq!hOdRSEG`2¥]ô\x0019?Xòs©fO`¸þ¬3£s-zÄ\x0006C\x0002fâ¡Lf0ä~ôCfà2]æ2\x0003N ËÂßªH\x000fSCe¬Ã²õô£\x001f2
FÎâ_ã¾Ê\x0004\x000cwdû\x0002ô¹=\x0010YÄCúÑ\x000fr>·¿\x000b</p><p>\x00179\x000e¡i\x000cü'hN\x001cú\x0000BË'ÿìÍ+àþ\x00132~´£7 ­s\x0007
¥\x00136=\x0000\x0002ÇM:ÏJÃ7Ô\x0006[3\x000efÁ¨ú.ÿì\x0007
\x001evù]wdó±TÝ±É\x0003ß²¸!-ÿìÍF´1\x001c+q\x001aEv4Q\x001cø\x0012\x0014\x000e«ø.ÿìMb\x001a&cS¹Ñ\x0005cHÌn&¸\x0003E®²>ïnAçJu¼Ó§ `,&JÆ¦\x000f}¦©F$ÿì:\x0001±X±Ï«O>S\x0001ü³'67ò\x00116æ·´¿°\x001dè§(\x001b\x0013¶8\x0000Kí\x0010vYÃ\x0018ÉòÆ©C¯Ô¥§à\x0006<\x0005,,OT:ìmÎÐR_Ê³A»»ºûü3\x0018ÞX­#ë5;çË¸rö</p><p>þ¹=Ães->oïó>å
Ì2D¼*è©·~>Ûi_À?w\x0000ho`Ô\x0000¹\x00056\x0001tTÅ c\x0008ð©ºé6\x0010K\x0007è\x001c çº:\x001c7sK?R×PÆ'Çr$ÿì
/8å§UÃóõ¬%±Å}Ã\x0000¦ò©ü³?@j{ÀÞ,Z7\x000c\x0000ábóó\x0000ßkø	~ø\x0014>}NTÞaÜy+°ûüîãCk¢Å¥Â·YäI\x000eQJßP\x000c[)^¿zÓò|\x001fE¼ý&gZà;[UcÏëõõÿ¹^Í\x0016÷ï\x001e×m\x0005Ý<9zd\x00140 Ìµ¯Áqa§Çý0»äËóùù9Î\x0008-._6</p><p>¬ât©\x0008b(Î`rÐÒàÌ³\x001evÁ+)Gl\x0018å@VÐì,aÒT*nÆcÆ}ÇÁ^\x001db`\x0006­ç´\x0011a\x001aéb\x001cç8Au¦ü¶3Ãb827Za=m:Ð "k\x0018ìÇ\x001e\x0007©Å\x000cIþ9\x000ci,î\x001bzK¹¸0H­Ø³4
.RW¤*Ï¿bÇVÈôc#³ë¼Ö©¹$\x0013Ûôs´@[>Jc¹ðCaIëni4½<o^ÝTEõ|éG/dØ¤rEG6¿,{"*æí\x0007\x0000i>`þÙ\x000b\x0019x¸¤\x00005æ\x0010³s	"å\x000e¼ÂtDgh\x0012mËü³\x001f4\x0015IõÁ_\x0011\x0014ü1k4(Ôë>hòËÚ=V»xi\x0005óÙÝí}J^ÿßÿø_?¬ÖË½é\x0012a(]Â\x001d\x00036\x0004ª\x0001Ñ:wí\x0017x´ùìõéEJ]Ï~X7.0¬aÌÍ!\x0018=n¡%\x0015 )\x0014ª8¹)êM
Ã!æ¼Î c±ä\x0012kÙ\x001d»;»3\x001ccNÂ\x000eÁ\x0008v`	Â\x0007Iùk'çÔX¬GûcÌi¨AW­"§0pØ£±õ)É\x0015åÇÁSR0eÃ¼è9ûSÒR~$975ì½#Ðý\x0010)£ç¹å\x0006Ï(\x00109K5\x0008#¼\±§q\x0012²§\\x0015¶p~#\x0003¦¶\x000cz12µ¸äÌÜ0¥àJJ!#\x001c9y5\x0008$x/ò1\x0001Gxå|å*\x0006=àá4Ö èº§	òª·2 ÃARJk\x0010H§Jö\x0014ì.AÊâ\x0013lÙ1rrk\x0010F°À(_\x00131$»é¤\x0011|Ùy¨Â\x0008 )Ñ5\x0004$®~ ]\x0008Bg\x0003²$ÈÇyØX7¤½\x0019pï\x0004riag\x0011é\x0014Ø°\x00041êÎ\x00113\x0012C_
Ø:^v\x0014y,\x001ecéw5Q£¯Ñ¦UÃ^\x0017æ%äÌÅóp\>æ\x000f\x0007¹~÷¨luëËÙÍòÝÑÍ¯÷¸ÏØk©\x001dVåUÝµþÜz\x000bóÙÉüy.ÈÍ[<¼</p><p>¨lÔ~c ²ø-züðeýV ÷u\x0014ùgñ^.¯onZÛ&M\x0001¹ä¬K·3Dí\x0003\x0015*¿U¡^§óã¦É\x0002lWP¸\x000b°\x0010s¢F®ÐÞK¢¼ò»]á}¸>½}÷á\x0016o\x0011ÃèµPúÅ\x0012\x0010¼¿mÅ\x00052\x0017ÚHã<e2
\x00063s(S©ÝÌ9üæåiÛ=x¡ÃF\Æ~\x0014hßßÝ¾»Y¶rSÙÂ\x00100öþÓª p°Ù	íû×§ÏOæmLÆÈ\x0012qéG/dÒreÂðoNÆ)\x001c:ÉäÃ^`~õöÿÚnÓx=_¾½{h
\x0001½Ûï°öú2,ùÂïjâ¿=?{Ý´_¯¥Vaü±ÔJ¿\x0006\x0007ñ´ºrGoÖËÏ«õ=ÿ?[>~ÜÛD#©Â	.\x0005]Xê\x001aL}Þ</p><p><¿àÂÿgóËWÍ\x001cTAo­?:Ñí'3zwãÌPp9pÒ\x001b£mC¢7Tã\x0006¢«\x0007|=º=\x0014\æ±Þà°òà`}Àý1¦ôÇè1ÐåXIot6Py Ü«à¾}0·KëV½ºa(º\x001c%\x0019r±Ûµl\x001e¢.k\x0008b\x0018~³ïWÖ_ª£­¹!\x000f\x0004È?ÿÏÃjù8»\x0002g±lKI:\x001f\x001c\x0017°Ã?\x0010ó9¸\x000fÍ®ÜÙM\x000c\x0002åùÅ\x001ctÀ\x000c~v\x0019p\x0010L/B Ü¤\x0011QS©\x0008n#'Àn¾0ÝýÕµIÊ\x0013{Ä\x0014õFg«õMëD\x0010\x001b»cvI%È?AÉSMÝ³ð¿¨\x000fx©v\x0002<[´L\x0004¿þ</p><p>ì\x0003Ø\x00026v§\x001fµÌ.{X/o¯Ú½Q\x0017È\x0002MÎv\x0007®¾âÚ\x0007o;\x0000 ðæéf\x0007e1ÀÑ¥\x001f\x00030b\x0017c\x000c¿wÊ±	"¼ßm\x001bõÆ\x0018\x0011c\x001c1°V\x0006«k=a¤z*\x0005ÿòC \x001a{õ+z/\x0016ÝÅô²{³óë÷Ë¶N\x0019£û©mLEÃr ^wíÝ{¼\x001f¿7·Èl ¡sP­Üë\x0000É</p><p>\x0003ª?\x0005\x000b'ÂcàDxÐ»\x0012ÌÝ1!£¥\x001f=0)K©\x001e£+IoÅÇ\x0014wÖ­öBðG?H¦Ci[Fz)Ín§P»B;cr¸(ýèÉÉdðG4BK)äv0täñù¥\x001f=\x0018Ü)*6\x0016nÎdf¢N]\x0004\x000e9¤_>¾W×¿=
­<Î^¢0½Án×ÇÖ\x0016µè\x000c¦r\x000f±*¶o \x001d*­05\x001dJaËÙK\x0006³7ØézÙ	a-ÎÒ\x000b¡§5X":rqÏjAXO¦\x000fGMà!\x0008õ\x0011ÙÀAÓP\x0013Ãr\x0002ðY5\x000e¾ZP¨\x000f>OË\x000b\x0010 +'\x0018©\x0006\x0005\x0010î\x000c
\x0000
á!\x0007¨Ðþå\x0013Ü\x0018¾\x001cáH\x0008sé#tTÝ\x0008®¢\x0019¬[eRtÉÙ\\x001fr²8±Áä x¢¡Óã ÌCÝ²à3´¸D$#ÏÐÉq\x0010æ¼ë\x0010â<í`èøX\x001e²£àãÆÃ\x0000\x001a]<Ú° 4ã ¤´ð\x0000àÕrÍ~°Üó\x001c=#\x0014~\x001c.ä&Æ!\x0008yâ' ô%dáËÔ\x000c\x0011GH\x001b?@´åÞ\x0006´+òÐ\x0003¶s\x000c¨h\x0008\x0005@\x001b¢¢\x001eGdó"!\x0010Å\x0011Û
4H\x001f<|éº ¼¿ùüÛÕêéXWw·×þW«y</p><p>À,Ïõy\x0003\x0003Ø§¶LÁ5õiU4cäÕëËÓãæ J\x0005Pm¨L'@´ÑXÔÁ,\x001bÌÚ=
Ëö\x0001T\x0019îÐ\x0011#Àè\x0018KÕ¬ãbÀ`ëw×
PøýTÛR\x000b=ÿ|ýþ¶}l*\x000eÔ£Á0¸è´\x0017N»¢APÚî\x001eæ0ÿñøåiK¤ ÚéË°y\x000cRòàXO\x0017y@Ü/ÚëËçå/\x0006qaûíwéÇf`êêþ~yÓ>6Ø\x0019K3Ù\x0014î¸ÉLå¹a\iÑ\x0010´9[\\ÌOZêñ\x000b0\x001cóñ]úÑ\x000färNR\x000exa$Uç\x001aÑ0@§;2*$ýè\x000c$\x0000'Ø\x001cî!"_Úra³\x0016»Yl/°_\x001f\x001eX$ÊÒÏj	ìÿXÞß·AÃI&ÙvSX;ç\x0013áò\x0000</p><p>\x001diç\x001a«sÿÇüâ¢EJ¼ÿüyyUña7ÃÙ¾_~^®ÿüÏ«ö´·ÍÀÕW¢H</p><p>ë¨x!ø°3¸º}?ÿq~¾xÑìw\x0019®þÐi\x0002LHïÊ.Ó\x001eÊ¶ÊHf¥\x0012e0P<i\x0016Ü×Ý¯òt~ù?\x001b\x0011½\x0005ÉC'ñ\x000c{oñÌúTÏ\x0007ZjÕóqì3E{A`ÔÈÆ¢ùmPª</p><p>J}# L\x0015ù ôÏ·\x000fË÷«­Á_3</p><p>Ó?'¸ÄaG\x0018ÀOÿ»»ÇåûÕý?Á¿fõyy°Ä´\x0001aU
°\x001czË Ôp\x001b1GÎKbâõåÉüåââ\x001fÏ^.~ÔâöÏáQÎ¦\x001fÕ nítê\x0003\x0015Ù</3\x001egf§â\x000fï°\x0012?C
6¦\x0004ukÕRO¨\x0012Ç\x001c'¨Rå"LïReUª\x000e?Uùp÷þ×]\x000cð|ùñÓûõõ}\x0007¤¸W\x0002wµábË\x0002Ò¡F`Ë´kÇ9`ØôùüÕÙËóã&}Q\x0003úd¥W\x001f *¯'Â)\x00156ïC y\x001f-\x0000µû´\x000fÐ'\x000b¿z\x0000Uþ(ãÄÞÚ\x0014\x0003\x0005÷\x001a\x0007Kd:\x0007ÈÆÁùd\x001fX\x001f\x000e'ê% ì\x0017"PÉ7¯Ó²õ>Ù\x0016Ö\x0003¨ fÛTG«\x0001¨ËëºàâÍ8¬\x0012ëSó°
Ä©C2qÉ¡êç·\x0000\x000b\x0013þÇ@\x0006 õð¢°9Ó\x0013\x0003òô»2j^ç´õ>þ~s{¿K>­Ö\x0000â\x0018y\x0001\x0003H²l</p><p>ÖØü°Ko\x000fÂ³ÅyóaV\x0000n=÷î\x0000c6±cÄª´.\x001a\x0000ZÅ<ædö°f+ÀÕ§Çø»Ü­âï±þ/{\x0000{µö2·8Â)iÒ\x0003\x0002? ¯æt¨ä>mt%Í^A
ì\x0013%ß\x000blªgà9\x0005:P«dÞw'î÷ªø>H·î½'RíøXp|¬2äÝºx¬q¯ï\x0003öAÒ\x0007¬ÂÈ\x0007,¸¬Âd°:/!\x0006°!\x0019\x000bì¼ï	VÅ<<\x0003ÁÚìTc</p><p>]J\x0002+0\x000fÂúáßWWìz\óúöº\x0013R\x0019%ó	û\x0018r^\x001fË~\x001d1¬\x0011rÏÓ\x0002Ç§ÇÝn=¬\x001e@\x0015NÔ  8äË'åäM$\x0003{di\x000f O¶,öB</p><p>ÒJçg\x0001ÍÌ©\x001e+í\x0008©v"5ÿø¹Zäy²½Z^-\x001fo®W]øÓ9k_"H\x0001ÚÈä­\x0013,Pe£bÏ^Í_Ì/O\x001a\x0003úç_\x001e®VþÃn»þm\x001eIÜA4©\%\x0016Å\x001dD\x0013yuÎï75Ï'®a|bÒwÅh¥ÏÃ{Àüð1/4ðÖ(âHç¥Ýótº|b&w>HÜ¦óA{m:PHy½³ÃÖÊÃNò³X}~»sõ26/×W«<c¼$ÊH=ÈòÜ±\x0001H,àáÆÅ>%?½¿X4\x001b¯ÁÝÖò=áZ§\x001a`WIÀÍ	.-\x0010Ë×ûäQO¸Ûª¾'\Üýc\x000f¨Ò`Dpí} ØfaÒ\x000fî¶²ï{º´°'M\x0007É\x0011Vd\x0006+ÅÈ§»­îûÁ
Þä~¬oµ¹\x0013\x001dN\x0017·</p><p>%¸Ê\x00197*Ü-/¯ïéâÚ,\x00140f¦wq­w+ü¸»µSº/ÚXÜç\x0000n©"\x0013%h\x0012\x000c"¨}_\x0007¸¿¯\x001f¿mc?.¿Üß_¯ÖðJaI/xxly wyú\x0012*WáöË±\x001fçÿ¼¸Àèi\x0017¼O%C\x001f¼"Ú´O)\x0019\x0003Êç\x0001yÞâ$
6\x0006Ä>7 \x000b`á~»þ÷û\x0003~¾^Ý?¬ºY/</p><p>KgL~mQÐ$y\x000cJr\x0005rÍË\x001eÀÏÏ\x0017\x0017o\x0016mvL\x0005ðÓ\x0013î\x0007\x0018DXZ6
',uÎJú`TÞ\x0007AlµÿÁm\x0000ïVèOÿ¾ý×»§½Y¯în\x001fW)kº? \x0002:M¤p\x0000\x0008"Ç'\x0015Ó°èx·¥@mI¯^¾¿hL¡ê?JùÁ]íbW«?Vieð^ø¢T\x001ep£¨:\x000eKòu¶\x000c-æ\x001eiðjñÓ"m\x001bî\x0000tËFè\x00034(ûmpÌ¯!\x0005wdË\x000bÄA\x001c\x0011èºíu¢:	Õt¢\x0001\x0013ùD5¹Ö+»Gyí\x0005Í\x0018T]þEI\Þ¤Á«Ï|,\x001cíB\x001a\x000cwgæ1ç \x000cJÖÇ4þWáiVåâäÇ\x0016/« VUÔj8j,¿6Ù\x0008?W\x0002ÁôÄ°îjDØº</p><p>[\x001fpØNåYmi³\x0012J^6\x0017l£3\x000c¶©Â6\x0007À\x000e´Þ\x0006O[¢}`k_N;	ÛVaÛ\x0003`\x001bÍæF+81In´H-ÜîØÑ0Ô®Ú\x001dÂ#&U}ãYûÂ"
`+Ìn\x001bb\x0018êPE\x001d\x000e9kg\x0003c5¡$Ó\x0012ÎÚ*æl·Û+\x001a\x0004Ñô\x0013\x0007àÖ.vAÜ1w¾x\x001cÎE¬mÕrDÖÄ<@þ¡¨VÄÚyòqMñf@\x001dwÛmÃ`×ä<Dü¥òO×[\x001frÜÒ\x0014u\x0013h³\x0005\x001c·ñÌÝºÁ\x0002\x0019¨%SB¯¦)ñ\x0017Ã¥ÆY\x0016)4\x0007</p><p>N\x001d­P\x0016)=tüNy#\x0005·¡» ktªI\x001aZÛ\x001f1\x001a_zÈÂÀ\x001fìõ¯ÿþ÷Vü\x0017
ý÷·eBÊë_~¹~\x0007>`\x0017\x0007Å:Ç`\x001b1sz0PÉeu±ÑVg»ÿå)MOyýý÷ÇÏÁ\x000fld?~_½»ýý¹\x0018bN?No×w]ÎÕªëÈ¢ eRwÇñ¡¤etØ;?;Ý\x0008ÌdóÁÖ\x0011­f¯®ÚGTMm!ÏIôÑR\x0017Ü~Ýà.f¯æ\x0017ß½[^-ï\x001fÀOç?\x0010¦Gmå¿~¯\ð÷«õÇtµÏVëÛåÕ.·ªÅ5SÉ6õ8î=ºHÄ÷óWé>-ÎOç/þIL~\x0012@kÅûØÚ}¹üc	H:¥KV\ÀËÕe\x0005Mõ&Àû2P,{9ÿi~zZÞK\x0003Ôí°YO¨Vû¼þ\x0016ëy}\x001eæ\x0008Ï\x0004w$¨Þï«5Ú\x0003õwþØ:¹Á\x0004Ï\x001f¿?v\x000b8ÈÀ\x0016\x000b³£\x0011qî«áI.ÿßËE;Ì§Aô>0EÀ9\x0014éê?\x0014æÈ^Ø[\x0012Õ</p><p>\x0013_tÝëÄ1p²Ò¨úüÃòã§ÜCÑå±ÃÓ9Ê×o@Â\j2¤ù=©@di`}þÃüÕYn©hÖ§ÒØ:j\aK¾òÙ\x001aþöõ§e§È)\x000e\x0017Í{@^â²\x001aÇ*Ø@È\x001ej¢³óãÓçÇgóiªªPÕ ¨ÖpLObG°¥è\x0013»Æ Ëm¬>Pu\x0015ª\x001e\x0004U\x0006ªDHP\x001dª\x000f¡@mv\x001aú@5U¨f\x0008TÎf¨¡Ê`%Cmqû@µU¨vÐ©b\x001b	ù\x00068\x0018@°mÔ8H]\x0015©\x001bv¨</p><p>9Á</p><p>¡Eöx¨\x0000d_¤¾Ô\x000f:S%Ø\x000e5Ò\x0008H\x0010lº\x0006ë¤/ÔP\x001a\x0006AÅ±0\x0019ªÒe«t%X#ô8¢*V¡ÆaïßæI8UªÞ¿a·Êfï»\x0007ÔM¸ )\x00001\x000c«d^5àDiU.r  ¶8Q}°ÖÕ@meYXa%w¤ÂcÇ	\x0008\x001bTsä«\x000fÖ¶Ô\x0015Æ]ÇíÅ\x001cÖl÷7TxõÅZÓ\x0001r\x0012À \x0017Y\x0001ØÃ%+\x0006¹Ù\x0012GÑW²¦\x0004ä - ="¨=¸1°¤\x001eçTkJ@\x000eÒ\x0002ZË#òûbÒ\x00079ÅaZ§GbÖ\x0016Ô\x0006! Ì\x0001(Êi+\x000c0n55 \x0007é\x00013Á4ù¬s»Q	>WÛPÐ\x0017kM\x000fÈA\x0000KR\x0005byW\x001cåq¦ÁÇêTÕÔ\x001a¤\x0006wl\x0008 \x000fk2·\x000càÜ®7£p«ª©\x00015H
¨\x0018òôR\x001c:§:à©rÐÒ\x00199´Rue\x0016PXé\x001f\x00166«ò©*V\x0002a\x001cóJÕ|\x00165ÄiQ¸|ÂfÿÊâìí|¬FrC§%<\x0007c­),5HaÉRêíqÏv såêTï­\x001dç\kj@
R\x0003\x0012|\x0015ÏÕÝ\x001arÝ\x0007Î
ø¦Ö¾Xk²U
­©0 Ê<ã\x0019 :[5r¬º&°ô %­àà¿\x0003¥2»z\OAÇÚP®Ø\x0017kM</p><p>èAR@JV\x0003\x000eÁ³\x001að5ÇeÅc@­½,=èe<¼4\x001fk Þ¾à¸!	°\x0013ºÐµ¥\x0007½,0ü«/Ë¸UyÚãì\x0003µö°ô \x0005ÊÕ«Ã0K~YÖs^\x0002\Âqøù!'t*æ\x0000þfêâ)§h\x0011\x0008~`QrèÕuäÚÝyµÂ\x0006Õ¼\x001a±\x0002'Öz\x001e±å\x001axe!O6@n0%ôÞÍ5ØWØ­+ü¢'¥\x0011Áß\x0003¦.8\x0003Ö¤q®XaÕ\x001fz0nû\x0013mUtiZð÷ð_4³\x0002CUU¨j\x0010TI\x001b¢W8I+;[ÖSÝ\x0007ÿ`wÝW_¨º</p><p>U\x000f;UÁíèXC@¹`\x001b\x0019i\x0008-51=*R3ìP
õÔa=5\x0007ÀiáÂ4ÙPL×\x0017ª­BµÃ \x0006n¸\x0000	Æ!w\x001b4).ÓÔ\x001aÒ\x0017ª«BuÃ z®¯W¸\JÎû\x0006ÓRÈÐ\x0003©¯"õÃ85²¯
¿áýsÊÅè0Îý*Ô0\x0008ª²T²%âÁ	6jÎ
Ø¶Ú§\x001eHc\x0015i\x001cvý¥nH¹@¦\x0000Ü¿áG¥\x001bÚÕzBuù?L\x0001¨RCM] \x0019kÉ¹a%ß\x0018XkRU\x000e\x0013«F\x001f\x0011THÕ¡ÊP½ïô¬Zuª¬	*9LRÁA\x0006J\x000eo¨èL±~¶¤\:é\x0012-«ªþ§¨ËwßÜ=\ßß¯>®n\x0014\x000b.\x0005\x000fîVÎ½¥\x0007FÉmÓÔ\x0004üúÍñÅÅâÕât«^`/|U¯\x000e¯hå\x0001Â·Tbè£aë Ø¦:ûÁðu\x0015¾>\x0014>íoÆÁ\x0006î(ÒáÓ(\x000b\x000f¡¡Th0zSEo\x000eCoÀ:wtø\x0013wXAÆ\x000bòÆo«ðí/=Õº(ó¨(ä\x001dA%È\x0018Þpø®</p><p>ß\x001dzú9MGJav§Ì>j¨ò\x0019ÞWÑû\x0003\x000f\x001fD9EÐqÒ ÍíçQ±T{\x0018õC\x0015~8ðð£à U4ünqZ3qN¥7\x001c|¬×Ôª\x0008\x000e´(#\x0005)*\x001f\x001a¼ÔÞð\x0014[½)ðúê>,Åº^wêPÓÊ\x0006î§±¸¢.1w\x000c\5\x0014n\x0016ça%Öñy[?\x001dC6UÈf8ä1ÌtÖÂäµò	2\x0007]tCÅÐ\x0010È®</p><p>Ù
C\x0018	rÚ¯!3àò÷\x001eß­â±g"\x0017mF\x0003=®Þ}¯®îº\x000cÓ\x0006³1!W\x0006Ã\x001fK±\x000b»^ûzòÏ.\x0017Ï/^¼n\x001e\x0004W@«*h5\x001c´UÉÞJ\x001dÃRpÝ\x001büÏH\x0004ÂKßÓÑÖ\x000b¶©Â6\x0007µNÂ&aÊÓFiØÍ\x0011Òï)ì\x0005ÛUa»\x0003`[ìaÝ6
¶S,;j¨é\x0005\x001bÛ-¶btÁV9W³åûÇë»µ&ÎåucX\x0019ÅéûX¦	ù¦ÊhªäÄ§øòòøu[Ìñª*^5\x0014/.¦:\x001eY\5Q\x0012¸Ö5ú\x0003ÖUÀz(`2¾ÁÝ¥\x001eÝ(-'F­mÕ4\x0000­©¢5CÑZÉÎ\x000e²CnL\x0002\x0016\x0016\Òårùý\x0001Û*`;üxÉJÒ``\x001bÅ\x0007Ìì`¢áýñº*^wÀ{#\x0006K§¸¼wóÞLÃ¬Æ\x0001}\x0015°\x001f\x0008\x0018Ý_\x0012\x0010\x001a°\x0013\x000b«bÉá\x0008±\x0000*à0#Â¤f//©p\x0006XBsâA5%Íû\x0003UÀqè	À\x0013i4n2"%m8þhuSæ¼7àM%eÒ\x0019b b§4gOÁ.¢ù½Qk_\Zsû#®k¹¡jÎY¯(o\x0002\x0012ªj\x0015Ïw3njEë¸¦çäPE\x0007\x001a­¼»èÉ{\x001e¬Ï¢:Æ\x0012\x0014²&åPQìlà8\x001fV/ÚÂì\x001a?¼\x0011tÇV|RP|2RïgÏ?¬ºy¨\x001a\x0017åH\x0012Ä'\x0015á²
®³\x000e
±\x001cJ½=ÿaÑênÇ"\x0005Å"\x0007@ÅÉÎôã9:ÑDÃ\x0003Áæþôª«Põ ¨ q¹±Yo\x0002Ôoû`\x001ePM\x0015ª\x0019\x0002\x0015\x0003r:ª</p><p>¢Q,vm)\x0006í\x0003ÕV¡ÚA§êdÉ¥ù¤ÑJÅPÁ%\x001d\x0005ª«BuNÕ¼|\x0017¡Jòì#:ösº-í×\x001dª¯BõÃ\x0018Àq£</p><p>¥}É\x00003ð½¶.ü\x001ePC\x0015j\x0018\x0004Õè"¬a\x0013\x0001õ0ªmËûu\x001a«Pã ¨¶¤¨pekô¤\x0005¸ÆØ\x0006ß½'Ô)£*3$úa\x001bÛ\x0016#%dÇl¤Uh)±íUºí\x000eF\õãpµJZ\x0011z÷øÇê¡\x0014P´\x0006\x0006\x001bÃLéºtÅÙÍ\x0002Ç¯ÎpÓJZ\x001búúò§ÅýpU\x0015®\x001a</p><p>7Ä\x00136</p><p>R\x00175\x001c~·®¡Ûb\x0000`]\x0005¬\x0002æþ EûPÄrfÕú\x0006¿l\x0000Z[Ek\x0007¢MéuIÇ\x001bÙÚ²!¶8\x001a?ø*`?\x0014°4Tß§ñOT\x0010ùG2hwKÛîxBng¯e²\x000eº»]Íæëëûåm×ZV#pØf</p><p>÷Âñj*»¥Ôº¡ûâ§×§ÙüüÍñÅü´­±`UU¬j\x0018V©y´­7¼® ¸HõÌ¸wh$°º</p><p>V\x000f\x0003ë\x0005É\ÜHrDeâúÅpÈén©Ð\x001b«©b5Ã°¢G\x0003º8(</p><p>-%]ÀâöQ°Ú*V;\x000c+öàÐ¹:M©æ\x0010\x0004õ\x0003Ø\x0006Ë»7XW\x0005ë\x0006U8\x00121 $¦@¹\x000bMiÞX}\x0015«\x001fUsM³sðÐ¨\x0011+\x0018ÊÄº\x0000\x0016ã8`C\x0015l\x0018\x0008\x0016á¸pÓL\x0013XkyÊµm\x0018?Ö\x001bl¬ÃÀ\x001aË£mÔ%\x000bÈí©xe\x0014°ÅVÌ</p><p>A\x000cäYE£Æ\x001cN\x0013ÈÓì\x00036lÓÑ:üÞhëêkþR',:k=\x0015ÎPVÂø\x0006ã«+XàÖíHL\x0010µ"']nâ@Þµãmô\x0014ÜðS}^µ\x0012/g'mã6\x0019¥ª¢TýQZgh.óÚRó$÷`´h;¢4Uf\x0000J4±¨5ÀQSaÓ\x001aÐ0@¨\x001fJWEé\x0006 Ô;ðð0sÊ\x0011,A®\x000cÇñ1ÀTÛéQe+\x0013Vß=^­Ö]jäGj¿Ó¸\x0006.û\x0004ZLn\x000b\x0011^Î¿¾|±8ï\x0000UU¡ª!P°ì\x001bâ-\x001a\x001aRfðÛ¶Zû\x001e@u\x0015¨\x001ev¦[q&O #|¤¶¥­\x000fRSEj\x0006!-yPS²^ÖnÒÌ­\x000e;ã´Uv\x0010NÏÕëv©Rýc]ëhÃÎ@]\x0015¨\x001b\x0004\x0014£-4.D5u\x0012\x001e\x0017µh\x0018\x001aÖ\x0017ª¯Bõ \òì«ñ\x000bçc\x001aü°ë\x0007÷r+0dD½Ïêlõe½¼ê´\e*­*ÃJÿÚÛ\x0014tS«\x001bwÞVðª*^5\x0014¯¶¸&$Û+®JB*ö\x00117=\x0001ë*`=\x0018°çT\x000c¶XEÉ\x000bYtÓt¶\x0001xM\x0015¯\x0019WÔF\x001eydx¾¬nkö\x0002l«í`À´./¸F¼àÒ®eLG¼bûÅüâÊ^éûÙ"ooîàdYNt:\x0015x\x0001x\¿hw£-K¦/fæ}Î\x0015¬ªU
Ãj
u¶`O6G\x0005<W³6,àêÔTaHÁcáaEóC\x0003x|¨¡!oÐ\x0019«Ü6\x000ce6\x000c\x0019+®x¼¹îVê\x0017D1
1úFSº¬ãA\x0010</p><p>­hqMÄåÉqKÜ6\x000ee6\x000eÁ¥¼Ü\x0014Ä8ímuöÇª«XõP¬\x0011w^q«£âÏ2PÈQ}=àºmíëD--\x0003l{~{c:&\x0012\x0003Å1\x0000±àEÁFËFj(Õ(¡màÝó×¸5¦5´­¨%gúö¨\x0018\x0018´gk/ \x001bZ\x001fÐoµ~;¶V]¯®0Ð©\x0005N9-(k\x000bR,P\x0001h\x0010²¶\x0001E{íÉbvv¼xÙV¸·Â-èÀ\x0000=sr)yï<ã\x0015ôC>\x0006pÞæûÊÊÌÌ¥ê=Ïxm\x0016Èz[ÍiQ÷~?¯n;åkÐà)t D$Íî\x000cØ½6ðÓì\x0012CUU¨j\x0010Tã(\x0015f"\x001f$!
gbS\x0011sO¤ºT\x000fC*¸+Þà7*\x0008æz|'G:S[Ej\x0007!\x0005OBrýçÐòì!F\x001e\x0000ÕW¡úAP]\x0005j(u÷û÷hëî\x0000UnG\x0011e¨Ûc³\x000c\x0004A'¼Â\x001av,ÉÆCpì¯aum»¥3Kÿ\x001dÈ\x000eM\x0015³\x0019ÙË2*(\x001eî\x0003ÿH \x000e\x000fÂìªÝ\x0001ç¬±n2·Ð9N¸Rà\x0013dÃ4A C\x0015t8\x00004\x0017´{\x0011yäÓì</p><p>\x0005Õ06e\x0018æÚX\x001b1G\x0004×~yÐp¤æÀ.ØøÝÏ»aÎöú,)E­÷¥çÜu-y\x0002\x001c1Í­ãÌ\x001exGroí~,·wgI)jí/=ÍàhI¡\x0007?G,\x0019Áj9`Móh u\x0015´\x001e~ÎÒrb¥1\x0014\x000e"4¬\x0005í\x0007:n3GÜ2ëgo®o;\x0017¬XS*MôÜ\x001a¥tÙ\x0003Ø´5fc!ÏÞ\x001cî©±\x0011Û¾pUþ¿ÿñ¿~xü´\ßtË­àâBj\x0007§$\x0017´;±i)òìË³ùy{re{$?uUnÚ@\x0001ðâýÍõ}·¸\x000fÛBð\x000e¹×¨LÝ°>î¶ä7m ³ÅËãÖ¨Ïv%7T\x000eÅk%·\x0011`\x0010\x0003²L\x000ez·QÔ\x001dò[xj[~|â2õ\×à­¥r\x000bPÓ}=­</p><p>éùI³wOè¢ÓÊ\x0002^UÁ«ÀÃÿÉ\x000cn´$\x0017\x0014¼3\x0014õù8à·|§gä;\x001d´PÈó\x0002\x0012\x001c/ÌãFSßm®w»ipûzm\x0013»Ü\x0016~JlöÚ</p><p>è(l¦%äÀéS»O½R®W\x0016¡î^î#~þr»ú÷O\x0004\x001bÁ¾Y\x0002Â/ë\x0004QÚ\x000cQ|wñç}þó¿ÖËw³«ÿgþy\x0005ÿ=\x0006$pôÉòÓ\x0012\x0004:<^ñç¼y\x000f·\x0018¬1Ã\x0002Iïòpgm#-EZü¸8?\x0007i7ÿqñÏó×§ß½\x0003LøSÓÂVñó/Â_]\x0019blvQ/qïí§5è>¸µÿæ\x001f7«<ÿðçÿyX-\x001f\x0001ºÒç\x0008
X&	Z\x0007°;ér8Q«à²¥ú\x0004;z0Ïç¸\x000e÷ì¼eçl¼!ut\x00124
G\x0012,f÷\x0012	!\x0017öa\x000e*ç\x001cF!!¯/\x001a\x0004ëòÐ</p><p> Á¥bU$\x0001þIÈáòQHS\x0004ª¾·\x0018äÇT`&!+( !dq3\x0006	XGÅu÷ãÒ\x0010²èA\x001aÂ$\x0012rs¡Æ\x0001Îz4\x0012%å\x0014ï</p><p>q°\x001cÛbmn"AÄÀ$ä~á$Üÿ±~û¶¶Bz9K6ÍÃÃjìT8Ý"9B\x0016W¶\x001dÄúZÒ\x0002*ûsv\x0002ÆÌ\x001b6oÞ4Y45¬´$ë@¬&x#VUn	+ü;\x0018«\x001e\x0005,í:?\x0010,\x0008\x0012Ã`%NSB°"+Ð8Ud·Hé¶^\x001f\x0015ü÷¡:î{\x001aCäs»¹¶'V\x0010@v\x0004u¹à	ÀsÉ\x000c+\x001dUf\x0014°´(ïP¥cµi;BBª</p><p>RáFaW 7\x001e\x0014\x0017
$c\x001byÀb®0\x001f+cr·úèû´~^âãZ\x001eþºbÖg+6,ëuy^ÃÏÖ	\x000fºj¢X<¾_Ýâ</p><p>Ô÷)y°ÁQXÄ\x0006)ÓÌ|\x001c©­!I	Ó¬­\x0017/\x0017§¸\x001dõåec®³FÄÆt\x001d\x0008°ÒK\x000cÂ;¬4ÎDäQê\x001aø<\x000fz\x001dñ:.\x0011\x0006õYô'\x000b\x0011.á&¤k6:z\x0013±1_Ç%"'¿\x0008-<>D¦Àæì\x0003iÀ\x001e¹å}åIl"Å7K° nîW«Zºÿ ´·8!\x0005\x0008òÂ§å¨hGy\x0015¤±ÜOèÙá?\Ì_,ö\x0005ÔËOeZâ$ø|)ke=N\x0000Éß\x0019\x0003¹ Èb^E3\x0001yù\x0011ML¦ùß\x0016«1ßÈÓ>»´Òãò©iÈËÏkZòT¤áÖ\x001bv</p><p>!yörÀíá²iÈËãÄ//¼\x0007Ûz	B=ÒË³¹ä\x0011\x000c\x0002\x001b§bÎlÇL|{@Dv!<-±Dòà\x001f<g\x001b\x0015#¼=4}\x000c>ÿmB</p><p>Õä\x0014~=åðó[¤ïíäúA¤\x001dË¨\x001eÒrÕtÂ³b·ç8Àå½DEµsàø\x0019à¹¿»Y]ß\x001c\x001eå¤V/ê\x001c.×}k%Þ-T8¦ül1¿¼x}²8>éBFVâSaóTd #ª
\x0019\x0014+Q©ny<2r\x0018b\x00022\x0004ÍgÀÛÐ\x001cí4\x0019\x001cÈ°q·ó1lsLA\x0006ÍAÀt¡ÅzDñd¹\x000b\x001fv\x0007\x0002\x0017S¡²9\x0011À\x0004¦Ây~\x001av·í>l!OEÜ( ÃbõJ&CF¾8b\x000f2¾¬?Þº/[nùËÇëåãÇÕìÍ»ËûÙùòËí²\x000b=OC ¸tC </p><p>kd1¦ èYh+\x001aB</p><p>èEótr2¿|µ½ùáõ«ùÅì|þÏÓy'Z@òùÑiqVÐ}À\x0013OË\x0016 FR|$ìN\x001dHK6áÆ¦Å#£)°h2)&r$Õ7Ñ\x000e£¥ä\x0018É@T¹L±ÓN<¦â¸n\x000eü4\x0011³£bªFI%×1*%!\x000f§Ã\x0010ÇÉ\x0014S2\x0007º9ivÀ½\x0000ãò\x0016è1L\x0019¬É\x000fÆá(ÜDMÌeÁ6Ç\x000e \x0006n7ÂH
®[YÑb^¤Æ(ÇáQ«#B\x0007P\x0003ºwI*\x0000LÀ\x000ew\x0003& af
ß³ÍYµ\x0003¨\x0001±,Ç\x0017ÍÞrø'â#\x001b¡4§6FNB
<F^H=&5\x0015?pZ¤9M\x0016jÌ$R\x0000H¯j¼ßPã³\x00080´c\x000bHÁºòñIÁ}Öj|EãñÑD"E a©\x0011l\x0001¨æàü\x0001ÄXQãf_å^Ð\x001c_mz\x001fój\x0013ü°\x001b(S\x0007õà½´¤~\x000e \x0006´\x0017ïÍ\x001e`\x0014§ä±D2dj¬3üüE\x0013v 5páj|# èW¬\x00025FãlîD
ü\x0013S#§\x0010f8ÄWo\x0004DaóV</p><p>Àg¹#5Î°\x000f Ú\x001du9\x001a+j|# Ü)\x000eÄ`My\x0016\x0002N·¯ñ\x000fcÑòë»ë·o«&\x0006÷Î®ß¯àoåòÏþ6\x000c¼u­egÓtìÅ\x0004º\x000c\x001b\x001bB`ç\x0018Â;;~¹x}zz¼8uAM	ß\x0011P\x0007\x001b\x00005ÌÚ\x001dyPÓn÷QPçx×\x0008¨½HÙù¬Ý\x0011Q¸rÔ
¦ü\x0000Ð\x001e\x0001´¤¹xÔ\x001eë3êÈá\x0007çÇCYc0\x0008x\x0017:¦ÌQB\x001d\x001c±µS#¢¦ìù\x0008g­ãÑæ¨-©`ÍÞm,º\x001d\x0000Â;c0a¿ÁË´b;¡\x0016,ÎáQ6¨Ú\x0001¨©Hu\x0004Ô\x0018I#¹g$NyK¨\x001d£ÆPúh¨)ü4\x0002jÐþ.5^\x0018</p><p>9\x0015Åé´k08ûc.a¦\x0011@G\x0017/ãQ»£,@ÀýçêÈ G;i\x001c''ÇQ^ÜÖ\x0006¨½æ£VÚÐ`\x000e\x000f@
¢H¤b¼g»×\x0005s$Ø»¢\x001bí\x000cÅ\x0001¨9Dt8êãIðfÏQzÜ\x0015Ç-Ýx,ÂÑ\x0011`ã\x0002XG¯Q`¿DÍÉ\x0005xM¾ì\x0000Ø\x001cX\x0018\x00016x\x0013ù9z³Am#£n,ëº¸Ý# \x0006ëÔZ:lEéç,<è°Íx°Ù)\x001d\x0001¶Ù\x0008?Líì2XßTyß\x0015öÇ¸þÍ?l¥~XÝ®¯g/\x001eoibAoØ\x001a\x0003\x001bùEz\x001b(®bÐü"CKøìÅéù1À?7Î0¨ÁÞÔþ­`_ðw½)Xý[Á&×àï\x0006{SYû·½Iþ~û°ïV"~ÖÕ':ÕO\x000f×w8z\x0016;àn­|Â	`\x0014±\x0012Xä\x0008Bàh\x0003ü¹Á\x0016Lmì§ó7Ç¯qv5\x0000i¬æw\x001f\x001ftµ}j5;#|X\x001d^È\x0011$¶O¥Jr/¨Ü)Ce½</p><p>Ç\x001fïnIXÌÎ^_bïW\x0017ØÔI5\x001elðormVP`\EKÕ@[\x0011B)Û\x0001vx÷Vÿñ±®2on6í÷÷ï\x001e¯V7\x0007wÝY,\x000bHmîpô:DE\x001a";\x0011J5ç:NN¸;ÿâùåÅIKë]¢I§¡ÆçHg>\x0007¡]ÔÊ³\x0016!õaÔ\x0014\x0005;\x00055\x0006\x001c
§¨ÁBb\.=jo¨9!5GJNQ¼Ó\<"j¦\x001a!à4\x0015Óbc1Ê0j>þoñpþï@M¥@`\x0013M^É\x000cäàò?Kê0rUlnMÚAÏÎ*¡?ìJÛþñ\x001aHùt³¼¾íÒ×ßh©l#Xa¨Ö\x001e
÷Ù&øã1À?;\x001f6÷èÝ·\x001f>¯\x0001xÚ*~\¬Ö\x001fW\x0008¿ýÔ<
gK\x0007ï¬\x0014ÜNæ±rZø`w?òÅù«\x0005o6¢îÅÕ/\x001fþUÍú¬î±\x00152o®ÛköE÷ÝùêÝÝãÍêþ\x001fgkø;×·¿?^ÿùkø»\x0018T\x0010yÂ¶\x0013\x0008Þ\x0011}04\x000bÃÀE4\x0019!\x0017Ø\x0018y</p><p>ÿÑý¹·Õ\ÍÖz\x0019½Z®Á*¹^ýq(û«4&%\x0019À3d\x000c\x001bOAãvQ²µÈd½^\x001c/~j¦íãï«m\x0019ø\x0016ëCÙIJ&¬4¼\x0015G\x001a\x001f²4^9K8X¯ÉÄÂ·0?oa¨_Ä\x0015¼×Ð¥Ú_\x0002XäÑæ§%¥:?\x0005MY)»(÷<Æ)0\x001fÞÝ»ûP9óêDÛçËõÕò-</p><p>ÖNïâi°¥H`Í)\x0011\x0015\x0005h¶ö"÷´åq~þbþ\x000cé\x0005Ïôá_ÿrwõ¸£ã\x0000á¿\Ýþùÿu:ÿ§\x001cÈ}®ð©?PÃG(\x0013\x001b÷BÇ¦Î7{P×\x001b\x000c\x000eEíÝÎ\x0007\x001e²§pn\x0013Av
õ}!×	\x000elP«æa°K¤\x000c$b¼oP°}Q×{\x0007F8hã\x0008µ¡ö
<kÇ¨Û+í»Î¡Ñ@Ì\x0003ö¾\x0017Ð\x001cõ¡¡è±\x0013jswý»ùÜ H\x0010õ}^ÓxìþÈy*9ÆU$Yü*rõ¹ó
ôÛÀ<O\x0003³[Áï\x0016#\x0007Q¢((³¾\x0015\x0012\x000eæÛÁFCÐï~\x0007 7àkéX2(T\&´+\x0019\x0006gkÐÙ§¨ØÞ\x0007ÿ1&\x0011"ð¤</p><p>ïL\x0003x½\x001cëø\\x001biàí72\x000füÍ¿H%ò6\x001fÐ¢\x001f\x000f5è-^	¹ÿ-å¶rãXàÎgs³§Ç\x00074é<+¤Ø\x001a)v|R\x001c<ejs\x000ep+1¥¼\x0008ys*Ðâ\x001bLü'´\x0014ã¦\x0016W£ÅM@KÉEûà#n\x0001³3OÿÄý c\x0012j¤	Hq.»/H</p><p>§Õ½\x0014ÔS"cØ×'ÚX#%O</p><p>x-G¹
\x001b¼ß£ç\x0008I©vðã\x001aºz¢D\x0014¬$\x001fýV´æ\x0015\x00017ÌúLãKÙgqt'EÖH\x0013Üu¤RÐ§\x0011sp\x0017o¥¡\­?)ªFàVÀz%	æ\x00055,a,K°¦rþ¤Ô\x0014@±X\x001cüÇÅsGrtE³øÈ]gZÖ¿ýaotÅLÙ\x0015º\x0018-</p><p>+Ó^î\x001cIsþá\x0018iJ\x0014f·Ñ¸+v£2;\x0014¦\x001cV&íÖ!Ó¤\x0014F#3M\x0014X2
®ÒP²÷1-ERä?'°Ñ¸L\x0011Ï¯2F5ôô¢Éßÿë·OU\x0000 ðåì\x000c§N>\x000eªuÁF+I½Ñ\x001eÑ\x0004<U\x001a/uC8	þóôr1;Ã9ç;MI\x0011ÉÚü\x0002ý)Â<__ß?\_ÁÃ__ç!Î\x0007¥\x001e-\x000eÉñzlQÊ\x0015RÖó(\x001deZaùùñÅã\x0017ðüÏç;WÈRU²Ôdd´¾!e4%q\x001a\x000bÍô5±¡äu(YºJ,'xÂ¬	zJ­ç\x000ek\x001a:üReªTé.Ëòü7\!#é²Ld²dCCöP²l,;\x0019Y2/\x0013\x0001òÀÌñ*ç8éj\x000cé¡T¹*Un:¡yZ¶<\x001dø%5\x0002\x0003\x000f6\x000c9\x001eJV¨\x0015¦{Y"z\x0001û
ÉA.ËU¼sx,²¤¨w1\x0019]8PØdº¥!\x0016=S¢Ë+ßeM¾Ëé\x0004¼	Ô\x0015\x0015¬64Ú×z¡
CÃ\x0008¸¡tÕD¡N\x0016\x00021n#4t\x0016\x001aÓTc\x000b
Y\x0013\x001ar:©\x0001¼ÓèÖ¥\x001d\x0018,\x001eù¦\SêP²jBCN'5¤£Bð<\x0006æ²§½Ê©qé\x0003éR5©¡¦\x001a"²êB;®Ë²êrº¡{o(Yu£p:¡\x0001þ\x0013­I\x0000S!y\3
\x0001¡¡tÕNh\x0008Éõ]Nª#\x0017.ê\x0000WÎ6t\x0019\x000f¥«&5ÔdR\x0003\x0007ãÌðrÜ\x001eÈ"\x0017^9×P7¬ÔPI
\h%<åÑìHt\x0015Ë5LO\x001cH®	
=ÐÀZ#2ãS´töL£Pº&5ôdRÃDW\x0001]ÆÐ4O\x000cÈi+F¥«&5ôdR\x0003'ßäEp¥Z\x001dìàÀR¾©®d(]5©¡§\x001aèNw Ç\x000cÑÅ\x001eJ2\x0012Ç¤«&6ôtb\x0003\x0013KÙwQÐèKë$MU\x001e+`G¤ËÔäNnxÉ¿T\x0005</p><p>:TkÝ©»\x0013äCéªÉ
3ÜðF\x0006Ü&jH\x001e²GéuCÑõP²êÁéÄ\x0006\W.2</p><p>\x001eÌ_É·ET\x0019;*UZ-©\x001b\x0005¿NÑ\x0014ëI-ë0®a.ë`Ëw<¥&$\x000fk#\x001bÀú\x001apR\x0010«2ÓP#6Xý¼ÜRfËÿ6ì'77åÅýÅÔé'Ôé)É3Qäd\x001dXqc\x0011\x000bv`ÂèRå!¯¬H\x0015üÍTäi+\x0003R\x0005.¨³üêFÁ	³}yfJÖ\x000c©´"³&OäÆÅ\x000c5ÇugÜ¦NNI\x0011lt\x0019 Tñ\x001fK±g(dg\x0007È[\\x0006^Íù=Kaï\x0001yÊ½\x0006¤"Í­+\x0006	Õò)ì¹è´lº¡Bª¡F'\x0003\x0007b½³IGP½·
uc}ÉÐU2ôØd`|ÜJ´£§\x0008v0Åj5ç;aªdÑo\x0003Dw4t\x001b>àL2Ç·ÑÁïK­aÇ&ÃahuyDúV­ÞMèL«\x0012áÆ¿\x000bëÝð*Øre¯×¶{IðU\x0012ÔR´ßCÙï\x0000N®/Nðì\x000cª}É\x0008U2Âè[óÐ¾Â\x000cù´A3\x0019f¤W\x0011«dÄÑo\x0003È`»,*j\x0001Ï</p><p>Cµ{æ]©(ÉÐ¬÷Äè·\x0011Ò¡LF¤ash¢\x0014W¼aK_:êú{t\x0005î.#DêFµ¡t>{ÕÐ×\x0002£kp\x0014¶¤ÁÁ*Év_">ªaÐ{_:j\x001a\®Â¦ ¾B¯,¿ò\x00109­éVHö¥£¦Âåè:ÜÉ´²#Þ\x00070Y,"­dMËÑ8Îï¤çá<Í¨·Q8Ë×Ñ°@µ/\x00195-.GWã\x000eG S&èòÌeéUmÚÙ*£ër/#ÕHÂ}h.fM\x0012\x0017\x001b(ûÒQÓårte*\x0014\x0013ÄÖî,­Vl¨Ëv\x0017°3\x00195].GWæ¸Z 1ß\x0013éylòXÑâ7©6W£ks[½YêzÎ3\x0006cË}ÖCg:jÚ\®Í½<*ÃÙRr\x0016\x000b\x001d.¶Æb;Q÷ÆÇWæ^\x001d)zåÞàO×a\x0003\x001b%¢aê__:jÊ\¯ÌáÓ>h|ðTØ\x0018©\x001bM¹Ð0Ý¼/\x00195]®Æ×åÁr}fÊ~æ°Bð\x001b¤=«Û.Wãër\x0000ï+YwºÀ&\x0017\x001a¶ö¥£¦ÌÕøÊ\x001c¼X¾\x000eÃQ\x0010\x0005Ñ^Þ*Wã«rlÎ Ç\x0001bL\x0018U	a7´`÷¥£¦ÊÕèªÜ\x000bw¤ø:\x0004­Ö\x0005\x0013Qq\x001eGM«ñUyp¥àK{</p><p>º¹$#9£0</p><p>[é*×£«r/iÈOÀ%\x00012°¸Ñ£ø³º¦\x0002õè*\x0010\x00170±¬²#÷\x0001*8</p><p>\x001d5Y¥GU\x001eÌ\x0010VFSj?ºÂTãÈ*WUnlYe¶XôçÃy$\x0008\x001f²QM»¶èhOÕøJ\x0016B¡,ÔXÊCi\x001c×\x001ds[¢¡1pàª½®³{¦c\x0018=\x00011ÖâàÂ\x0011ò+ç°\x0015»çf¬(Ü65RNq7À[4\x001a\x000eÞ7Zò9\x0018Wb&ãx!ðs0ÅÝ`\x0004ï&p¥­%\x0017Õ­qþc\x00187\x00051Bàr\x001fNIÑÍ8Ã\x0016°mXÓ;*÷ÏÌ$2ÀqÖÖ¡Úw\x0014/\x0015W²a¶DGrÀöáÍã_TÏW³þ×-b»Áù/77\x0007·{x=\x0015ÇH^#¾\x0019Þ¹\x001cÛ\x000b­^\¦,çó\x0013±ør~yrÒ2ÓITU\x0012ÕÄ$\x0006F\x0015%\x0012} 8\x0005\x00163òï & QWIÔ(¨ÝGð×%\x00127û¿Õ\x0004$*fj\x0012Ë\x0008DP»	(­À\x000bçCÃ¾H´U\x0012í_@bÖdÀ¨\x0002H¢â[lo:\x001bF¢«è¦&Qmv£GÞ¨áË<gÑ´òù </p><p>}B?5Zò\x0004"îó\x0018]\x001a=EhX\x0005}\x0010¡JbDÜ)5!È¹<sÁcÕR¦P¢7:±JaB,¨¦Ý\x0019¤\x0015£by\x001aÚ]°A$nZ\x0013v1µæ\x000fG3À\x0013ÉË¦@Mp$Iñe¬6SÛ6@\x0017\x0019Ó l,^hfTÍò4¶Wv
£±fÛÈ©\x001bxu·èh\x000eWãR¸V#{\x00185ãFNmÝxoê\x0001Ñ%\x001aM\x0011©S<Æq#§¶nÀ±ã±\x0007`W\x001diGf8§h¥hÏ	\x000e£±fÝÈ©Í\x001bo\x0015Å|á\x001a%OéRó·"¶GQÑX3oäÔöM@\x001dî|¾F©Y¨âÇ'±fßÈ©
\x001cU\x0011¬\x001b
µæókÓÞ¼=Æ#§¶pãV8\x001f­=</p><p>g/²æpíA¥a4ÖL\x001c9µ\x0003JØ·W\x0012xé\x001d?G\x001fÇçUU³qÔÔ6³¢¸þ%\x0004¥Ý|{qÑX³rÔä\x0011\x001c\x0011\x000byâvã2¶W
#°\x001e¾ÚÄq¨ÓþfÓ:®j\x0017f\x0002½¨jæÚ¼I\x0019@\x0017(ËÌZÃ}\x0014Âµ7]
£±fß¨©í\x001b,'g&Í!t7kí)\x0018FbÍ¼QS7\x000e¼ý\£
:ÃäÎ\x0005/\x0015 Á|êø$Ö¬\x001b5¹uS\x0002úpÚ\x0003=\x0008<Ê\x001c=M\x0001Ãh¬7jjó\x0006Ç.{Pä[eÕo7*c{¬7jjóÆëoé\x001e¥dÕÂHtí\x0003]ÑX3oÔÔæ
\x0016\x0000ä-(p\x0014\x000c©þ\x0012\x00127íµíhÔ5óFOmÞà\x000c¯@CHØàp\x0012-Ñ('àU]3oôÔæ
n0fÍ³4ÛÙ\x000b¦QO\x0010\x0014×5\x000bGOmá\x0018Ì¼Ñ$nÇ-É\x0018Ä\x0004×XOPMnäàÞrzàxäQfðûbÈéö2Âa4Ö\x001c=µcÀzË\x0015¸>Xj/wÁÐkÑ·WQ
#±fäè©\x001c×Hj\x00029Æ.òú.\x0019]Ã4ïh¬Y9zj+GKAÆx cÜ9ø§	\x001d*]3qôÔ&\x000eN\x001fÉm_>hÞaà"\x0006hy@5ÖÔ¿ZýãXfKcô'yã\x0002oáÑ´Wf\x000e¢ÑÔT£Z5\x001aç*o1SÈÃ!§y¦¦5ÌÔZÃò×²l\x000e±t&RãæñI¬IT3µD\x00057jVÓ\x0016\x000e²©\x000eþÌ</p><p>\x001eÆÀ1S\x000b\x001c\x001d%fm2w8ïDY\x0000\x0013Æ\x00178¦&pÌÔ\x0002G+·±Å=M»s®è
Ù°\x0018æ\x0010\x0012mMÞØ©å.S«R *7Jn,6 jk\x0012ÇN-qTÔÔ`áÁìf\x0003g3<Sö¢åa4ÖË¦\x00169J;.\x0017¸\x001a4\x001bªÖq_«´\x0013$TmMäØ©EÚ}D0ì\x0019[ÍÏQz?¾Kek\x0012ÇN-qd\x0004êëEÑ\x001cVrAª ãj\x0012ÇM-q¤7\x0014\x001a\x000fRzÜ¾$ÊM8ã3ª«	\x001c7µÀ I%-jWF²;ã¹ä[É)h¬	\x001c7µÀI;«%u(\x0003$\x001a­äN\x0010\x0015Æ·ã\Mà¸©\x0005À¹óD#Î6É¯Qs\x001dµBÏct\x0012k\x0002ÇM-p\x0004\x000esÈ]0JXj¯Òi Qåª=1ü$+Õý\x0013qì¦?QzI\x0003w\x0011\\x0000¨lûveñÛ¤ªé)
>m#Ée\x0000¼cÀ\x0003ß2	2¬âÉ¥þ\x0005wúUZ\x001dä;Á¥bU µÙüáH9®</p><p>¤KÒõ\x000fEîìÃÛ\x0004>¡ó¯¸Ò`±8é\x0014D§åú\x000e ³ÿ6Ð©¶ÖÁIÖÁ\x0003qß¯ð·¯ïgß/ß^\x001fJÁÕÈÀsî#O´¶!Éz\x000e\x0004}>?}þúøböýüÙq\x001bwª­uiH\x001aÇÓ5p ÜR-nM:\x001cS%ÇLAN0\x000es\x001c°H)>\x000cÊÈÁy	£c«äØin'¡±QðíÍt\x0007xI»Í!äø*9~\x0012r6þ	\x0017°Ä2@Ëj³ÛÐ\x001cBN¬\x0013'!'¸r;ÎÐ\x000c\x0011*[29rD^ûù÷:·ý>ÅëAeÍ*+\x0015}p¢Tr[×P\x0002<¢_ê\x0014ý2\x0005E\x0018\x0013£ýg@\Þ.èàø\x0001¹©;¤õÏwuy}7É\x001dÝ6\x000fcM\x0014öpk\x001bò</p><p>ÃîèCý>LA<m\x001f÷åùgN8¶oLÜawtS¿£IîÈ\x001fñ\x0015y\x0019\x0008Ãæ\x0005F$èc \x0010diÙ=Pd`(ñ:,u\x0019¢_ë\x0014ý:\x0005EJ¡ÀÎ\x0014ÅòÊzNÛ°udØ+zWEï&ÝÌR-6LWä\x000f»CªÃ®è]ý&¡È\x0008¶\x0016@Ò8Z\x000blº°Ô°;úX¿£Iò\x001bÂ\x0011]Õº(£ñÔ«þù·ú\x0015ý6	ÓE\x001eÁ¾ÄtºøBcÞÐÛú
½ VE~c\x0000é²\x0006¶¡yf\x0018A¿Õ	ä´¢  H\x001e\x0011A¶,Dñ
µ$ÃXîSå>MbÑ\x0005\x000eV[¡6\x0016],öOCú0®ê\x0014]MrE]pÜ\x001diJ+\x0011\x0005×\x001eFÑ:EXtðv/~\x0004Kn«\x000bE
{\x0002=£Uý\x0019­¦òë°>Òm{F~T_ï¶NÑí$wdy»&®ç¬ê\x001a¦'\x000fãºÛ:×MB\x0011°aed6a{Á6\x000f£hY§h9Q4Üq0W
=#_\x0004o(Ê\x001dÆt¿Ön\x0012«[rEJm\=UÔQÃèña\x0014}ªS4:R¢ø\x0011Òp±¦0¼\x0003Úºy"Ã(º«S4I\x0001/\x001c	pûX0\x0018_(²c\x0006\x0018Þ×)z?Éàxn?:Êo\x000bå¨kÈ\x0016\x000e£hY§h\x0012ÁL9\x00143Õ\x0016m4j\x000cèºNÐõ$Áó,:¬aÏ#NA0ðoK/Æ£h]§h=QÈÄ0ÓÉb1èP½5ÏÃ´Ñu]\x001bMrGÊnÈñl.LA­\x0007éì4A:\x0015yW$\x0017\x0001ä\x001b32ü¶~?ø®&5\x000bä7$\x001fáyqm\x001a¢=¢÷u&\x0011ÜZ`r<_®\Qñ#\x001aú1ÝUé&ñõ@ÿX½u³\x001aýwSÄºWõ;Ä3Òe\x0013\x0019*×\x0012¥Ó\x001bsaL®û¥NÑ$9#­6æÝPTè9\x001c%T½XAáÈÍ¢¼zÝ=Þ?¬n\x000e¥\x0003G£xj#Æå\x0013ùõ¨2àYøyq9;{}yñfq²\x000cU%COF,cÂp½¯"2\x0002ÑÔ~Ù\x000c]%CN\x0011Gz3^)¯\x0006pØèÄåM
cùúaªdñÉð¥o;ª#\x001f\x0012©påë\x0018dØ*\x0019vt2@øÒr\x001c!=\x0017 KÏ\x0016´lè\x0005íK«RáF§BG\x001aff\x0004ÒeÈ¨¹L´D\x000eûá«dø±É\x0008Ñb-H"Ã\x0006d¯D\x000e\x001b\x001eZ|è>d*\x0019aôÛ\x0000FÒDQ´\x001eÎIgyH\x000eãÈÛX%#\x001bR "ÏhHT\x0018\x001e\x0003'MÃTlÆi&å'Æ'CàHtxÍBRsá¾t-Iø>tÔøèZ<`	\x0018qUÐ´<ÑIÁë&dÃ¾¥¾dÔ¸\x001c]c\x001d3\x0019U"86|¥d3Q¶Ôáô!£¦ÄåèZ<|¢¦\x001e\x0001Z³O±¼Ð}êCGMËÑÕxc\x0011Kç\x000eÄ¤(-\x001f¢%úß\x001a£ëñ`mé@\x0012²àq\x0007j\x0014\x0005(kz\¯È\x0005w§\x0006©6ÂÊ~\x0006ÙRçÙ"ãkrg9¾º¥­\x0004³lèëëKGMËñU9\x0008]ÃÏh:¥yæ\x001bµ\x0019*ãër_Ê\x001fAÒrQ¯TÃât¨2W£+sÖêÈ(	[b*ïÜ7l\x0010îKGM«ñyÔ¼?FjÅ\x0001-©\x001dóUÓ6¾tÔÔ \x001aß³^R\x0005lPÊ¦®âgÞ\x0012;íCFM\x000bªñÙ h~\x0005ØºÆ:;e8c,Í8âJÕ´ \x001aßõé\x0000\x0006ÿ\x0001\x001d¼^µ\x0014ùô!£¦\x0005ÕøZ\x0010,*VBË£@R¬$UC\x0007X_:jZP®\x0005Ó¼^6\x0012\x001dÎ¢ëàÙý`\x000cBGM\x000bª±µ Åí\x0011$­À\x0002¢ÁîNy.ã²¡¡´/\x001d5-¨F×\x0011´ º¤6`Ræ®(q=ÉÐ5å¡Ççb\x0007\x0010
¡7\x0001sWùyðì\x000bÙ43©/\x001dõ@èØÊ\x0003Ø*Ò¸Ô\x0015HE </p><p>4b½\x0013|«.¸£\x0010;þbì(·hùè4­¯r Ç9®ÛVÔ[¡fw[c±K¶IQSÐ\x0012"ÜLV#¸i"?¥¼iñ`OJ\x001eVë-Jð7c\x001b(<^4H\Ýl \x0010%¶amOJ~\>%~9~øÇ\x0017\x0004CË\x00190|Âëf©45	oe@¤-\x0019«»õûÕýìÙzy¿º½?ôõ{Ëµ¡>b1\x000e-¶ß2ÍïååâõùËÅÅìÙùüâbqzÑ1´[i\x0004$ÉNDe^¯°äõz\x0019C\x0019.e\x001fN\$7Õ-9Ì£¤\x0015\x001dPexÀ
6ãä«$ùHÒ\x0002ÂpKðÉPfñË=ÃHUâD$áBe¢s($Å'ZÚ²zT]µØOçÂI\x001d1M\x001cBjIöö§HÖ(SQÄ\x0008I	\x0017h,·ÔR;Þ¦\x0010SIqá7#=e³=X
Ù¦±¥Ù¬?I¦F$\x0017#@\x000eÁÑ²x/uDRlXî;ðê\x00039\x0014\x000fäæ¶\x001cï\x001f
>Rø\x000cnËð\x0010ËØ0|è{BÚÂQ¢§¸XG´eÇº\x0013¦¤Øª×AYH~\x0011Ps¾¼¾¿>\x0018ãâ¢\x0004\x0013S/N«²9e	÷Õ\x0005\x0000JÎçÇ\x0017Ç]\x0008ñUBüßX%$þ}	uÖú;ò\x0016Hz5\x0018\x0001¦<òÅãz\x0004\x001fH\x0006nB\x0017X#®¹\x0007«\x0007[¦S\\·\x000c\x0018¼©7c§Ð¦"«¦]7ÌëÝU±»1±ÍêCÅÍ\x0013eloÓ
xec\x0005\x0000ç¸Ù(È½\x0015¤\x001e\Ìb£u%\x0012Û7Êè\x001b<æ\x000c½2o\x001bùEÊ0\x0002#à9hi¸¶K]Òµ¨¶n\x0007oêÜ>.»Rîá=\x0019S¾\\x000fåÊ\x001cp\x0004oG\x0005/KÜ\x001bË\x001dé±j½	´\x001e</p><p>¾öVÍ¨µ\x0002Þê
ßlÀ7,déÞ×ÐûQÑ+Zï\x00042Þ\x0017\x0019¯¹Nªæ³èC
}\x0018\x0015½.5gJÑh8DÏ\x0006Õ°_´\x000bz¿U3\x0013Ë0;Y>,ÿ¸{<Ô¶:5%dÖw\m\x0016
\x000b\x001dÓVO³ÌßÌz}¹</p><p>U¥BN\x0005H\x001fjí\x0001EÅ%ãQDN\µÅ\x0018û¡«dèñ/Ãð8.Á+Úæ¢y0l\x000bÂõ!ÃVÉ°£¡Ê\x0010;´}h}RÔ\x001c»nOëö ÃUÉpãa2\x0019\x001bú¢</p><p>¥¼·%ÉÞ</p><p>_¥ÂOÙ¨Rø\x0017U)'U-ö\\x001f2B0þ\x000bwG_8OPuQúBF[oK\x000f2b86\x0019Æë#[û®\x000e®ÄoÛúx{PQÜúJ­õhdèèy¹F³m\x0013ì `Æ!£®ûFW~&ï\x0004Ï©\Ë-:Ár\x0001?*ÂQè¨i?9ºúû«®£¦ýäèêÏØPvÒYé¨t\x001d%\x001fM`£Ðajt¿ëuÔ´¸\x001c]\x001b\x001dçP«æÑº¸¢c­m5±=è¨)@9º\x0006Ä¥UºÀM\x0000ei\x0015ßlë'ìAGMuÈñu4\ÛPVáá®\x0011æ«¶ª¿ît¨ÔUãK]\x0019ËÎBx)¼a+r\x0011&\x0012ãÐQ\x0013Wjtq¥¥EÛ\x0016éð Öó+wfáI m\x0014¶\x0012¾]I6b©\x0004\x001aïR"\x0017øú\x0018--\x0004w!°ë!bKf¹\x0017sU&#döz;ö½\x001aôNdä\x001d/#o7ÓcñWeòKæ°åØ·"¸×>\x0015dÛÝáæ \x0002ÆÑ$fÅ@)Ïc^\x0004\x0016[n±Øßô^¶\x0012«¾X\x001d3êPv« kÅQ\x0007ÃÅsàZ
\x000eHx$hÇH\x0016ÿ¢\x0012Éºù¿ÿñ¿æoß®fÏVë÷w·\x001fº\x000ctÏw'ËOËÛ»Çû\x0015P³×\x0018­cc\x0005$4ÍÕVÄv"fógÏ\x0016³gó¯/OØ=Ë¡FªR£F§Æåì\x0011\x0018ÂæH\x00121AY6*1ºJ©±zï\x001cÏwÓÇûÿ¹{»$»n#ßw*5</p><p> \x0013á§\x0012EYtP$»HvÜÓ/ÄcñLºùÑqO?õ4z\x0006Ýïg\x0006Iä"\x00172±M\x0002µ×*@\x0011r´;Dmiý</p><p>@f"ùÏC8¦Æ1Óq4±´Õ,·}'\x001cVFJ«3PF:ck\x001c;\x0019Ç\x0004,«	'Óh\x000ecÐ\x00043ÆÕ4nöâ¤</p><p>ðVÛô76\x001aäbS¤Î¹4¾¦ñ³×Æ\x0001çµcºqÛ\x0015ªÀ¦	gòÚ&Ì¦I¦ÌòÁ1ç¢V|¿O[m0Iç\x0010N¬qâl\x001cDîQ¤\x001dÃ\x0019Tµ-ÑLÞj[Rïä?Õl\x00146\x001bÇGGIÈ{
Å\x0010Ä0ÎÚïæi<¨îBUà÷d¦
 o»M4\x0013\x001eu7\x001cÚm[ÜYí·»É+¢3\x0006Ò{ÆQ\x0019'ûí¾lå%@9Ò\x000cçOa{z¼áÙao®^Ü}xûà\x0012¥PjJÃ(wÎ\x0014òÓù{Æ?¾zqsûdT¢\x0014Î_\x001fÃöú8\x0017Ä\x001a\x0017¤[9\x0002J°2-£§ô´\x0003k\x000e¿ `¤ÃPtS­ô1R.v\x000e©AÌtty×"¯íI'óúÞtªvsØÃÎ_\x0010ô,Íã¬¹.:ñu±ó\x001c¼\x001bÃÕ\x0018nþr8\x0012\x0015º´Ì¨ôtévsøÃÏ_t(¸)Ëå¡Y|D4Q]</p><p>\x0004æ\x001a$L7XÔmmY9Ô;­%\x0010TÒµ\x001d) ±\x0006óWÄF\x0001IÇâÚ±¼fù\x001d^urû{Aª\x0017Õ_Tg\x0011\x001at\x000fl²ÏzZb²:\x0013\x0014v´N}W÷úÚäNLþÈj)Ø\x0012^o7IãÕõt·N\x0001ï5f\x0012o°\x0008QZIyßi ÛMÒøu½À±\x0007sZäØYSLFEyÝ)SÛ
Òøu=Ý±Û\x0014Ê±Cô¶Ì\x0001//ÄÞw´êv4]Ï÷ì\x0011\x0008'yL\x001c¡+ñ¶DÚMÒøv=Ý¹[\x0005JFBy§Eâ\x0006¢\x0015pÏlãI\x001aï®ç»÷hJ¿§º5éì7\x001cÆwê¯ws4Î]/ðîÎX\x000fe&.Z©©
ª3ën7IãÝõ|÷\x001eýV-ðIÈCôa|GÑq/\x00074Î\x001d¦;wBDëâ£Ëé|^ÖÅÑøvîÛíÖÃëA7Àqc±Z±£8¿¤½±Ï¿²+ª<Ø@RôN^~\x0003I·w^´Éæ4®\x001d¦»vKUÛÀAJp¶s@Îz'k·\x001b¤qí0ßµk­¥F¾e\x000e£e<UînÆµÃt×n\x0015Ý¨doiênØVdñ¤£Á·¤qí0ßµ§\x0000.¹\x001b	¥Qòq7À|ÀNµênÆ³ÃtÏnaS·Ù8b)»µQöVì=@î\x0006i\;Ìwíô\x0019\x001còÖ2NîVÁLº[AãÙaºg·\x0010hBÅtð¹;Y`ö\x0011:\x001a]{I°ñí8ß·[[Â\x0007j´Í+:\x00113=éÐÝ$wÇùÞ\x001dÉpå|<
/\cÄ)F3)\x0002ÆÆ»ã|ï®½èZ\x0005\x00032\Ê+I°ÆÝ mB~¾w7jKæ%Ñ"ôè½dNc§yc7HãÝqwOv7OÃHK²
¢ÜL0?,\x0004§çØ-l;ÎwîT_õ§£¢\x0007Fn4Óü­:o»9\x001aó=âogµ\x001aó]"Ø­Ük#IÇ8ly¢'¹)$¦ñ$f¾'\x0001\x00032é8x¤¼ÄK3fIñ
_à\x0013Ñ±XÞ]Ü\x0001X"ÇY»\x000bl{s·\x000b®î>ðÕyä\x001b¯7ê\x0014ÌÏÉÓ®\x00065çÛû/óßá¢\x000cöÉ\x0008Nm\x0019á}g</p><p>ÎþT]UuwÓal<eëBl/c¢|oÈçùßg+ó¿ç¯©ítçFòô¿))»Y·_Ý®ÌV\x001c=}e¼HÏøX,2	XÈôn`~:ùiþÊ(.ZK0¦$á¼ëh"\x001fùù\x000cæç\x0015\x000fñ¾ú´Ë$,Ö8éõÄ5uëùÝ~2=÷å9Ì÷ÉJó¸ìä]d©Îpéýùs\x001eð+x Ùg%nÓIsÊ lÒó\x0016Øª\x000b'gÁ~ó6×1°ç4rDªéb+0+W¡«±ùà¼p{}'+ B\x001faÖ\x000b*Ø3+`§[\x0001«¢ÍuaÓ\x001câ)O\x0001Õ´( Ùe)</p><p>½Ë\x000cõmó|&Oá³\x0013Ç)OD.Î)ÉA×Â d -\x0007'ÅhÎQàK2\x001a¹ÊøIÂéÈüåìÈüeþÊ\x0018ê%ø\x000cN¯©âõ\x00030?ÁÌßf)ØT\x0012ÒVh\x0015lÞ8³ý%ç®\x0006\x0017x\x001aCÁqe¡\x0013yq%³I/=4\x001d­4)\x001fþ"</p><p>X\x0002Eÿ*ùþ\x0013\x00088ßQÚÛ\x0005_Àà</p><p>\x001akÀ²\x001ar\x0000ÂµæRâ"¤ÖÓÙ½\x0010&Ú³ÂîhÂîW·ÿïo?~º{÷éÁ,Ôm\x001f\x000c+	¦psjÅ(Ñ¾7<{yuûøå¯n½\x001aêPÚ³"ï\x0004\x0005ÿ PXCá2¨\x0014xòr\x0015¹Ý£4Ojâ=\x0011A\x0003õÓÝÏw\x001f?}èC\x001aÊ,J×PÍ+Q ÄÄm3¸&.­ì2&\x000frCPV28\x001e$Ö´¹¯\x0000c\x001f«©Ü:ª@m¹\x0003YSõFåå}Vëû</p><p>öQùÊ¯¤r2¾ÇÊü\x0001ôEZï¾\x0017Î}P¡</p><p>ÿ æ/ÖPq\x0019\x0014Ç²j,\x0006ÖJN+\x0015D\\x000cï{fÛEUÕûUëÖ*EF¼TR,à1\x0014É4ußsÂ>ª6¨X\x0018U\x0014< ]\x001e\x001a°äæ}=\x0018û¨¨B/\x000b+b:L\x0015%bàqÉÞ(UôWf\x001a\x000bÝ\x0015zU\áÒ¦àyõ>\x0006#³,¹P¡#-q\x0010«	,ô²È"ª(*~Á]GÇk%á</p><p>÷¥éöQ5¡^\x0016[D\x001fO¢&^¬ b/vS­`\x0013[èeÁE´p-jSJFa¤Ûái\x0018ËTª&¶ÐËè4·zò^¼V+:öä\x000eR5Á^\x0016]D4²V\x000fØ\x0008\x001a\x001e\x0014¨S1Õ¶7Ñ^\x0016^Ä,v°a\x0019ÑFOX\¡ #éÎÃ&¼eáE¤na^­\x0014ß:Æ ós¹ZÐÞï\x0017zâHåY>Ìq÷\x0004Y÷"\x001ffg^\x001c¡ñY°ÐgÉd\x0004ïÓ\x0015?«îQäî\x0019Kß×Û½\x000f«±î°îê\x0018]}ò)Z?Q¥Rv*Uc\x0007aÝ-+xNÏzoI×*¸¬,¢CÀ·,l\x000c\x0006®» ºì³GÖ÷(*í:(7Ó``c0p]F0\x0005¹y`wÎs±§"SÁzÑÇÆ`àºô</p><p>jòÔZ\x001d·`º¥Ì\x000c0@Ue)ÙkÝýcd0Ì?µÙÎOËÒMZ</p><p>U6\x0019?Ô äî}oß\x000bv×ý,Xû\x0000·eÝwwÿÌû=%÷;óiçpq%\ð¬À´³ðÖ
ZR5x_\x001dØÞ\x001dùc»#\¶jÒ¾
`÷L\x001dÛÌu_;Ñe\ÊÉ0){\x0000óùJÇ«\x001fî>|¼¢ûÃC+ê\x0013*ÝV²D£#E6A\x001a\x000cúöõö-7·/ó·Ü\x000b\x00045\x0010¬\x0001J§{ Sä~í¸	/Èv\x001dFÓ;ö\x0002a
k´åN\x0010OR!Üz\x000b§iÆ±s-9\x0004dj ³\x0006È\x001anQ¦ÈË#úò5eß\x000bdk »\x0002ÈD\x000fÜââc\x0003¹¥
Ê(+-;
èÙBX´ç4·{û´Ï®=ð\x0004«pìÜ®¾Fôõ\x0004ÆÁö\x0004-:B`¯Qü\x00112
ªÝÞ±ã8ª\x0011ÔÎg¨\x00087OJ\x001eÈ1T2â¬ä¤¥ÕM§¥{ Sú½´nÜÐÏo~ú%{Ø÷?~|3A	IdB\x00038ÉØ:(oÜvè^¼~üèûìd¿~ùòñp\x0018+¶\x000eÐ`!\x001a	¤äP6Yn=kâ$"B7Ò¤<5\x001a®D\x000bR¸\x0004¤Ä%å~")Ö)-?\x000efj0³\x0010\x000c\x0014Úä5³ÀØzJq\x0002åh&£Ù\x001aÍþC4_£ù«&/\x0001¨Îóª­OÑúÐuí@Ó.Õ¹ FäOMLß½ùðáÿ<ÈE%"£ \x001dKP	7_\x0015!v\x001aQèO¯&ï\x001eßÞþ¯ûA°\x0006Áé \x001a6s]6""n¼ã$\x0018Dæ5G§Ä!L
aæC¤\x0000¥RSÔÀóéýJ¬þÑÙµ\x001a¶\x0006±óA´¿FÇ6\x0000hm ZZ³\x001eë§¸\x001aÄ-8\x001f³ËÔ_v­Ï~^­Án\x0010_ø\x0005+r:èÆ^óÎRÒ=Hú®t\x0017G¨9Â\x0005q²³tÖ´ R3\x000f¾óâ´\x001b$Ö q\x0001H¶\x0014ªÉ\x0011	òÈ\x0004H{{\x0006HU\x0018þ!¢ð>sk)/ÓI"#$ÚÒù\x000cÀ­UÕ\x0011^\x00002³F\x0007é£ùB2\x0018÷²¤ñêz¾[÷ù\x000139r©fK~D|¡\x001d<Üg´Ìïf¸äFú{²]ôRÔæD©Ü¡ÄßÜ=\x001cÂR¤\x0015ø\x0004\x0016´ô\x001a­\x0004Z=±\x0012\x000e\x001d¿¹¹\x0000j\x0002M`DIB[KÊ`¤\x0010L'ó¾\x000f\x0001k\x0004à\x0013å\x001bmýµc\x0004+\x001d0L~1©\x0011Ì\\x0004\x0012§ÖTO1/×ý \x0011ývm:uû\x0010l`'¯\x0002¢H S¬g\x001dy-\x0003hR¬®\x0007c/Fp5\x0000æ:²Ï+yæ\x0014õ\x0006ÔÓÅixÉ½\x0010Á×\x0008~2áÁ\x001fAc}\x0004êD0}}1A¨	Âì}¤E¬C£?í£\x0012ÃhìÅ\x0008±F\x0011¬\x0013\x0005«ä\x000bX<Á÷</p><p>bx8Â)\x0004Ü\x001c½\x000c\x000f¼\x000ejç#ï$é.áàÂ\x0019Zç<Ù;{g¤­KC¤üÕÆP¤R@»	§A7îYOöÏ´øíKSz·¸65\x001aëu1Aãõl÷ì"%Õ2¥{Þ2x\x00014Î`hÜ³ì}©¡\x000e2jwäpz25û\x0010\x001a÷¬gûgodÐ
m$î1\x0003j-cÑÐ®\x0019\x001aÿ¬g;è´¢,\x0003\x0014\x0006,\x001a§j/dh\x001c´í¡IyÎ­\x0004|\x001c\|6\x0011ù34.ZÏöÑÞI\x0002M+/]PDÛ4Ý®\x001fÎÐøh=ÙIÿ6!74N\x001af;é Iú#¯\x0003^ËVe\x0019:Å¿û\x0010ÚëçdÿF?gJ\x0006\x0005X=[û\x0019>\x001a\x001aï\x0000³oo \x00057\x0006*8nµVÒ8¤ÝhÌëÅ\x000ciÉ¦5 BßÚÅ-×N\x0006©\x000eèL\x0010Ûy¤j|¬«r9§"ZjaSÁ­P¡¥c1ã"z\x0012ËWÑ&_hhZÈ× ZêÕèîÜSçë\x0001núzPËì,uÚYQêNÌhhøåI²/H¦8ª»åeMÉ¡\x0000^\x001fè\x0003ÉÕú\x001c#Ì?\x001f4PH\x0002rÇ\x0003¼.\x0014pIÒrL\x0001þôæC»\x0018ô©âY6X§t¸×ÚJ\x001cechçÚÔqúA%~ó§7wï®~xÿù×·ï\x001eJA£,X¥C2~Ò¨ Ç\x001cÇjqz|óìêç¯>y6Jì»ó²\x0003WÉÞLÄ!½8ËAUúc©¥R7\x0017:Þü\x0008\x000eÖ8¸fuÌ²Ö(ÂdFW0jócj\x001c³\x0006Gq¥³éôpÙ©Q^ºÑýXµ\x0017­qì\x001a\x001cK±V\x000e»"\x0017V¤Õ1âXÜ¸÷m\x0017«qÜ³\x0013"¹ùmuÀ\x000b\x000eªm\x001c\x000b ì¢ñ5_³8®Ä\x00189ë\x0016GFÛh\x001cwðíÂ	5NX£XÅôIÏb©ô¸Ù|\x0017K¬Yâ¥\\x0007ìcÔì9ÓÒH\x0018£âXÜw\x000fN]§àj\x0001©k£x@¢'1|µÑJíy\x0018\x000f\x0007ßÅÓ\x0004bÀ:O¥²2ºG\x0017Kà;ïGx@/</p><p></p><p>\x0002E\x0002¹ûßÉ\x0000ªóÚu</p><p>àð4A^\x0013\x0015¤K¥æöx/S,1\x0006Ðc\x0001ö]8MP D\x0005*:¾izêO2àN	\x000f»&wñ4Q^\x0014\x0016héóßþÄ\x0001u¾üëpÚ.Æê%~´±\x0015wÂ\x001b-\x0003Ðs£½ïtm\x001cái|^â|(ÊÉ!µ·Ô\x0002ÏS2\x0002?CPÙõÅÎg|y¶ÉqB`=0<÷¶\x001eÏ0(\x000fCc\x001dæ}¶­¾U³}£,@\x0002{\x001d¸Ë\x0019ê©ÞÀh\x001f+2ß¿JÉµ</p><p>QPÊ9Í7W¿Þ]½úðö§÷?¾y0\x0005éï\x000c!]±Åé2õ§3Sõ6«ä>½¹zuûäÑó×/\x001f\x000f\x0016\x0018\x0007j\x001cX\x000cBÞ¢¶ÒRì(;K4¨Í(í±\x0006k\x001a\BAzÒh¦2²\x001b#""cj\x001c³\x0002\x0007´â¨X7k@ÆGÂ(¾\x0013ÇÖ8vÉêXfÊYÍ\x0005\x0014ÎXÌvôÎ·\x0013ÇÕ8nÉêº\x001cÒÀMªÖj\x0019áÂ¼Õñ5_cØ\x001cçÕiD|äkse\x0006£\x0019¼:í¤	5MXst¢Xl³¼yòª|nL»i8±ÆK\x0016Z\x001a²×!Ä¬üè¬À v´\x0004\x000fÐîØ\x000fUkV\x0007Yt4DÍ«e\x0008`ºdOãic%A\x0001\x0019jäÝFµ=(:)pÓ,n\x0002½&*HÛ-Õz»9È±Gè ÕÎLãiÂ\x0002½$.\x0000\x0015å*\x0006\x001ad·\x001bDÙnI
Gp\x001a?ª×8Ò\x0018SÔdËy»DmjX@¶§ñ<zë!Õ9ÏÛ-òC\x000eB9»¤+0G«3ó¶Ä¾ýQu3\x001f$_{Ê\x0013ïäðMQ²:G\x0008ú\x0014\;9EØ\x0019Þr(¸>§2«¨~Ã¥s(X\x0005\x0015%\x001dH§Ò\x000b¬ê\x000c
:to8²« ¬§\x001aÍ\x001cÒ\x0019íj\x0018È_N5Î"4õ\x0006yJ½ÁT$JZ\x001e!LÞË>%\x0013.?R_ i å\x0003\x001a¼#?Ø\x0012#ï?\x0012ïÞ¿ût÷öÝ%4éoñ§w»{·Ñ{\x0005éÊÍZ¼1-\x000b\x000b ¶\»\x0016±Cðüõ+aøîù³W7O}}³5\x0018PcÀL@u§\x001bFäéÚ(¯hMO\x001då\x0010\x0004Ö\x00108\x0011B96Ð	B¡Éqö0:nô\x0010©1ÌÌµP¬ \x0011\x0013\x0006\x0017±$4á1\x000c[cØ«¬K0\x0014§\x0007Pd^Ps\x0008ÃÕ\x0018n\x001eIÇ!\x000f K7</p><p>\x0003¢Û'|Â×\x0014~.a</p><p>*\x0011.\x0014V\x0016£3ä\x0018F¨1ÂL\x000cÃ+\x0001¼X)Û\x0019\x0016s!Ö\x000cq&\x0003ðö´\x0014ÛàÁªÅ	câÚ\x0019'¿§&bÐè\x001eÆHw0\x001d3ÆÉg¸Î;ç1ÖOtàÉ¬ryÀ¶«\x0002ï*\x001dN»ª\x0013U\x001dâh\x001c¸èÁcAÛèHó5o+%*Äh}§¸î«\x001cÃ`J7\x000e\OôàÆ\x0001'üÓb\x0004V(B\x0015NG¼\x0017\x000f\x001eZÆë.Ü8Å5\x001aép\x0018.jH\x001cN\x0016ÃMÝT\x000b×\x0013}¸±çÃ¥õ\x00109Ä¡ÄmØN-Ð1ÆëNÜêk]lU~EåK`èf:qÝ8q=Ó',àµÙªQ<Gïuï\x0010FãÄõL/n#È¤å°§Óaëè	ª\x001dâh\x001c¹éÉ1\x0014k¥6¥¢?ÅOÜVÐ¸@é\x0002éò\x0017y[8\x0010å\x000eëfÞ ½ÃÎt¨Kd\x0005ªp%$Ñ8Aé\x0004µÉCÎ\x0012\x0005r=)*\x0019\x0000(p¢ïÆ\x0007ÂL\x001fH\x001f£ìªXN9N¼r@ã\x0003a¦\x000fÌ#Ù2GÈ]¡¬\x0011Þ+÷!Æ\x0005ÂL\x0017N¶¸rð\Öãä\x0003{¡8\x001a\x001f\x00083} Âb¬R\x001b9$ÑÅyôj(\x000ea4>\x0010fúÀtÈy5\x0010¸©2\x001dr/&×÷Zï\x000fa4.\x0010&º@uM¢3G\x0017¢R¦ptªw\x000fq`sÅ·Y
<¤+­á"ñ´\x001e\x0016Ë®¸\x001eØ¸rèÊ1*V\x0007Úð·[9ÄXöUT\x0013.6®\x001cgºòò`ÖÃóhZ\x000f]NyOyé\x0010GèË18*2Þ8hÒçõ(Ï\x0003±×ãz£qæ8Ó+à\x0002tÎíÉêÊñ\x0008=\x0015©C\x0018/Ç¾\x001c]deÔt<<WàAôZRë±§z£qæ8ÑcÀ\x000eºl«ÀSc0]Ög®GãÌq¢3G\x001f¸Á5Ò`:Y\x000fsAªü3ÍUãÍq¢7Ç\x0010yàR:æT²ò1z!G\x000eq\x001eGãÎq¦;w¶¬GD\x001eeFÕ[²¯ ÓfxÃ4îÜLtçè¤¾.mé4N\x001c)qff¦Ä4nÐLt\x00082' nS6y_iËù7¯z#\x0010\x000eq´/\x0013ÝGK®}æ \x0005N\x0010¼\x0005\x0006"?Ã6ûÊNÜW$¡¸åuR\x0001XÒ\x0012	f8s9l³­ìÄm¥)º2\x001b\x0006õØärMH=\x001f\x000f³E¨\x0013\x0016¸B¦*\Ø*d¦Å¼®¤}(çXQY¹¡ÛÞ\x0008Ý/\x001fJseÌ)+c¦ùCÅêÚºíÏ»pzæ¡­»*4Ë3J((\,Hö\\x000c$øÅþÂ¹\x001bîê£ÆtêO\x0019¹\x0012mí8õ_­¼ú\x0011¡U­ø&ýjJrÿ\x00191¼úåíw?]ðý£+ca\x001b\x0011´uCka!õ\x0017."K¶úë0¹ýh^}ÿä×¯\x0006q:þ¹mF£\x001c|\x0011ØzõößÞÿúö Ö;àPÞ\x0007Åo!$!)-u£a&ß¾¾zõä?}r?\x0003Ô\x000c0!]Ñy<½R4Ê8«¢\x0011\x00065\x0001k\x0006ÍâÄ;j=MÖbu^g\x0004Bg»]</p><p>aj\x00083}3mbA¹	]]{ÙM2t9ê±Úö¥\x0010¶°!\x0002¸ëÈ\x0010ÔæÌs=d\x001fJ=_</p><p>ák\x0008?\x001bÂ\x0006iÐöT¹Ë\x0010¦kíÂyB\x001a"L?\x0013k1<éZÌ³²Ô¨]érXCÄÙ+(º&Ûvâa»¢\x00074k;UíVä%ÔôCÁÝäTV\x001dyVÜAªÇ\x0005ÆC´®n¶¯\x000bNºß<	|æIx\x0002[q\x0014Cm¶K!\x001a_§g;;Ò-ÄÓ¡@ÏÂ!C1û»¢ñvz¶»[·\x00149zuªNò\x0003</p><p>^üz÷S\x000eeÿç?þóñ_~}{QíýW*/¬ä\x0013Ò*H±òQÒÑ\x0000_Ï¼xzó(²WÿøôÉËÇW÷3@Í\x0000ó\x0018Ü§ªT8-5IØÉá\x001eaÀ\x0001§®\x001aP[</p><p>yÊÓ¸é<b\x001eA05àJã\x0003!(~1;\x0011L\x0003p5\x0007à7-Õ«JÉ\x0006¯G­6Ñl·Ñóö¨v&\x000cÇr6i#âÕN©È1»ân\x001eEäoëÛ(UUßÆ¼ã\x0000-\x0006LÄ0ÛtøÜ</p><p>¤äP»ò\x0014\x000eòôc\x0014?¶\x0014ó¶Qôl]ÄiK¹r²;¥\x0017RlYá ìöTö?<ùëßî>~|³£}t7c\x001c-ÕQ)ÝÉ_kãD\x0011Ew:üðâæåËÇÛ ÚG7÷\x000c¢\x0015\x001e¨y`
\x000fD¾n'\x001e\x0019FëuüîLD<Ä5\x000f.áÙËäa3</p><p>":ª;]\x0004xLÍcÖðÐ\x0019Æq\GâU\x0014Å©8¶Æ±kp0]ÇEÜ2,´rEm\u\x0014x\x000e\x0001¹\x001aÈ-\x0002:
\x0017 °\x0005\x0019Hàuo^È! _\x0003ù5@é§2¥\x0015\x0002.\x0005Øúºÿ ò£\x0013-B¨Â\x0012 k"ßØ\x001beÁÁ(5Õ \x001cL\XãÄ5ë£\x0002KûHiìR¬)*Ñ\x001d¥#<ºu¨k<ª¥±¯e¯ùø([4¯;5Öp\x001aÿ£×8 ë¤óÙGzRÈºO1ÅV4èb\x001aQc²õ\x001amS\x001ckµ|4/ùé\x0008Éwe;G Ùr°.Ó¾¬\x000f\x001cÄái¾\x001eZ¨3jA\P30bsCô\x0015P¸
WÍ\x001b¯)J`ªbç</p><p>½k´9åä\x0007ÕSÜ\x001f?Ü½ûùê»»Ï?¾ÿüá/\x000fÏ\x0018r§Â0¶\x0012+ñ8±?ÞÞ<ûöê»×ß<}ûÇû fEL\x0014og\x0019ù\x0000$ú\x0002\x0012o\x0011ä#¥®ýPXCáªÒ§%ùm{{(CAU¯5ã\x0018©¡Ì2(Í
ÉÛ¤SvM\x0010Ìa\x00013Lõï²5]\x0005îxGf@\x0019}\x001a-3UÛäj$·\x000cIñ;@H¦õË=x(ÇâöBù\x001aÊ¯2\x0013)ôv2ëXºk<8,³:e\x0015\x0007¡B
\x0015A)jâx&âWqWæµØN²á T¬¡â*¨ ÉÆ@RÆO
r¦püÀ¼\x0013ªØ@W-£R"(©½\x0014 {0eðQWá\x0018U\x001bO¬</p><p>(hâ°gª\x0010®\x0001¥,C6 3On"</p><p>½,¤ ±«\x0019*\x001a.«§®ú\x0000È1¨&¢Ð«B\x0014³hQäñ\x001c\x000b7¤Ði<u/T\x0013QèU!7À¹ð\x0004lE^)ò\x001cû\x0007öB5\x0011^\x0015R¤!\x0014)]¯­\x0011S\x0011üTSÑ\x0004\x0015zUTáóDòÊÄëà$NgSÐ\x0019*tª*ôª°"Ù7N¿\x00064´üzaPF®ûq!Ñ^ª&¬ÐËâ</p><p>UF­à VÛàÅXqî¤Æ\x0005Ã2\x0017¬dðK et\x0019gim±\x0016½ÚícTíõw³RÈmã!ýNk%</p><p>ÐKS\x001c¤j\x000c;¬2ì\x0006+:¶X¨.6°§±pª±°Ê\x0006ºàJ¸¬EªªXÌÍÁ\x0004L3\x0012ÆÍ[:]°×ò<öVj¥iFúÜÛý9]ÇæcÐ¨2`ÙkÉÆÀÜ[¾>GÓ\x000b
\x001bZÒ²m½¹þR®iÙæÞK¾`[\x0008ç)ß	lñ#)xç\x0014®Òbñ§îIP_7µ\x0010N\x0019P\x0006]9é{\x001aÎù9\x0010z|±ra%gmÒ\x0014\x0013¸j=5¬j\x001f\x0015rnmÝKþL\x000c¥µâ\x0004À{±&f¤ÿ\x0005[g(X1%õ\x0008­ÍT©çß0Ù»%GVn2Æ\x0011}8Âp^\x0014è¹äÑ/\x001bÐ£_î¶¯y¨¦º*IkXIAi-s £ÅúèûäÑ÷7¯\x001eß¼\x001e=Íór¤@\x000f$³)PÐ=20<tjX÷R`Mó)Ê83M\x00139fÒpºaÍÁ05Y²\x0018r©\x0007EÝ¬F§.}/­1ìt\x000c\x0017¨É=G°(=\x0002ZyÁ >Å\x0019\x0018®Æp¿×£ák</p><p>?ÂSòÁÑè\ËV\x0012Ef÷½\x0014±¦¿Ûµh\x000b\x0007h=è\x0007sa¬7¬£\x0010ÀÊ
ÏÅ¨Ä	öô9.¦±gõ\x0002BQ\x001eø|õíßÿûoÿ¿\x000foC¶±´!Àú¶·÷¥ú!\x000e{ö__}ûøÅóA\x000f²@
\x0002óALÐòð'XX§eiÛëjÚ	5\x0008.X\x0011\x0013JM</p><p>JòÜâ\x0014(³ô\x0000¨\x0010)\x0017\x001aÄü·­Aìï\x0018Ä× ~Á\x0019I1Vä\x001aïüÇíÈ\x0010iÐ÷HO^\x000c\x0012j°\x0000&sä`\x0011)RÙ¢,kKÍE\x0002/æ5G\À>^\x0016$økÖPòª }ïYu\x001fÇéí{ó"j>\x0008¦¯gëKÒn\x0017D±è}ZÞÐÎ$­?\à\x0010
½r\x0012
îÌ[«< öÊP/&9\x0010­N\x0013¢o~ýH½COßøp¡FÊf\ç'\x0003\x0010­HépCIF ÿ\x0010róô%õ\x0011=}~{Û\x0015\x0017jx æ5<Á²8hðFKA­\x0006æñn0Ju7\x000fÖ<¸ÇHè¨\x0003\x0017Ø\x0008(ãÑ`Ý
dj ³f| \x0017ßmáùêZ\x00076\x0003>öÆ\x0014\x001c\x0001²5]\x0002ä¿é½\x0008\øþ\x000ce\x0018ñ`ðõn W\x0003¹E+äy j \x0002,¼B2]9ô\x001a£\x000e\x0001ù\x001aÈ¯Y¡´å\x0018(ZO§Û</p><p>¹2\x000c²×§r\x0008(Ô@aÍ</p><p>¥øße Â|ÛO1\-\x0003\x000eÄö\x0002UA5cyús[ÍVA³\x0000}ÚsÜ¬Â c¼¨ñCz#Âò\x0018\x001f °¬¥+½¹\x0010ÌD;§\x001bÃ­\x0017YnPR^\x001f´çºt÷XÁõ&\x000f\x001e!j\x000c^céHû'K;àm­]Ú\x001e¼éBè)]\x001e\x0001j\x000c^cé¢Ay\x0008¤èÇpô\x0013£.áÏå¡óìÂ8Ókì\x001c=ýqCx$eñ|ù[Gpv­½é\x0007\x0016\x0008\x001a;\x0007kì\x001c¹"~\x0018Kq\x000e\x0019ì¼\x0004\x000b~â\x00196Þ^cçÜINÂC¾\x000c düºîÍ2;d\x0015Ìm¶\x000cò<;\x001d\x000cÅÜE#Â`é\ÈÛ\x000e4µö;Ù/ÀÔ*°`\x0014O0OÑC`-G}È\x0012=\x000cf\x0013ï÷µ_Á*°\x0018¼\x000fzêÏW\x000b°r/÷nPWºËú©/öá²m\x0018I\x0006?û(º\x000br¬Gu\x000ce\x0007rû Ì9Y¶\x0005Ë Ç\x0014îI¥bº¥.½téåPö4LZ~Pº)ß|¼úöýçÐ1Nµ{ÜÊq*¼A{jå\x0018Mdyõíó×ÿ<ìÜµ§YÒ\x0002¦S\x0004]úl¼\x0012!G
R°\x0007£\x001aß\x001d\x0014XSà| eåÚH´j,UPvTV¾\x0003ÃÔ\x0018f:\x0006%GOEARq"úë0\x0012­Û\x0001ak\x0008»bGYÀkf>}ÀÞûÔN\x0008WC¸ù+aY6-è2H%­ÀôN\x000c_cøé\x0018ÉÂJ		$7Ëfliâ\x001c\x0015PïÀ\x00085F¿\x001a YwM]6RJÒÛA\x001dà\x000eXSÄ\x0015§Û¸B¡¥ø§´4Â¨Tórú=Çz\x0019çqXWÎ\x0006ë¢${</p><p>F\x0002¡;0Z÷=ß'\x000cèÒ$Î#u3Ò´¨GUø;0\x001aÿ­ç;p«Ï dSÞU*8Cto\x0004×NÆëù.Ü Ôúju*còEñ©7k'FãÁõ|\x0017nDv'-ÇIçI¢Û®ðÛ^ÆëùN\x001c¼É>QÍb«*«Ñ}{ÞÉÑ¸q=ßc,»JkÒ]Ï»JzCAõfÿîähü¸ïÈu(ëAO\x001a|:ôMRµÉ\x000cÆëùh²ëP¥©ÒrÈGâ\x001f;8\x001aO®§»r,-\x0017ø)+Ã]DyøÓÝ±)û8 qå0Ýt(«ì`\x0013KPÅ²\x001c¶Wñ³\x0013£qå0ß§½$ê¡Î¿\x0002_*F\x0013:vp´wñé¾ÜëÛzä$V,\x001dfi9¦8\x000fh\9Lwå¤\x000eÌáz:Ú\léq±cÊ)ÆÃt_néh±\x001c\x000eýäåh|9L÷å6ê±<
--\x0016ce{ÕW;9\x001a_\x000eÓ}ùoft\x001b_\x000eÓ}¹
¥¯HÑtSv%· -Ì9\x001e3éÎÜBÚ</p><p>å/Pi=°«Þï\x001c3ùÎÜ\x0017M</p><p>EBí½ º&NÙVØørïËu,Û*Y]Y\x000ePe[:ïvp4Î\x001c§;sj0¼\x001aÀ</p><p>!.hË)BÑ&¤çû@¯®£g\x000c}Â°²\x001afNÄóÀùÎÃyiõ"\x000e	\x0011Ô²è®Ä\x000eÆæâ|kOzìvK&rhU|Go$èNÆVá|[e¼hwZ\x0011/qÑZSlÕ\x0014\x000cÓq3ÿSj¤xr\x001bÙT']hä!8SRZº'&K´ÉWÒÑEÔM\x000fê¨w%à¾Á\x00050¿UÕ*	pºáwÂèöâêÌÏwï?¸º£ÆÂÏÿß\x0003YÉ3Ë·§óôGÜ\x0010"ÇÆÇ±\x001cÎwÏ_ß^ÝPwáëÿç~ S\x00035@¾(WR3BÖ8K@<</p><p>\x0011C}@®\x0006rkaÅ^ÒOÍóï\x0001©Î±¾ã> P\x00035@\x0006Éçç!\x001eßb\x001b(õB½Í{xÒÍç¬^Fµ\x0017G¿Þ}þ÷÷\x000foÊUV\x00147T×¾Y\x0002%Ú¯é>\x0014þzôôæõ¿<\x001f5å2\x0006Ô\x00180\x001f£B§\x001b7OÆH\x0018ÅwÂØ\x0008\5\x0006ÎÆ0\x0011x</p><p>jÂ\x0000*\x0018 \x0010|Á\x0018TCîÁ05ax|vÂ°üN0bY¡×Å\x0014¶¦°Ó)ÒÇ:Ç\x0014Jü\x0000¢É­õXAób\x000cWc¸é\x0018ÚóD|ÂsºÒ\x00016íû\x001aÃÏÇ0'C\x0015¥BÎ\x0007©\x0002Ò£¾¯=\x0018±Æ¿ßÕh\x0002ÉmE*Ù¦Yf7nïË\x0011É\x0013£Ò¥ä´õèÊr¢éT,Í=GÁ\x0005(&"O#\x000cÉùQIJ¶Yå¾c½ð1vgÎ<ý@ù÷ïúåÁ\x0005¤4Ø»kLPRí­4\x0013[\x001cLEøþù£ï\x0007ËòñP<Ìüø\x0018å\x0001ÔPÚ1G¼ÞyùöA%Óßõ·ãÄo§8nG·Úp©hú³¤¬ë¨þìøxS¼ùñvÂ·ýâ£TÂÙR|eGKwM£\x001f·í\x001c9½s\x0018rEÞùûÊ¬/âÉ\x0016ohÎNm²\x0010éÔ¦/Kÿ­«\x0017oß|øðæêå¿Þ}øùÁ\x0018</p><p>©@Ã Y-|\x0006¼¼:\x001bÊõ~#ýõYByñäñííã«¸¹ýö~$¨`\x0011qÓÁh©úI+#&ÕøNéî1$S#EH cR\x0013Ré>÷Q4¾ïD!ÇldW­R ÖÅ
	ü	I\x0005Ùxöëï\x0018«Ü"$teÒ5*r³6BÔQÈ<Fäk"¿(3òéDäRôË</p><p>\x001b1RKðD¤P#EDãÜeß9Ñl</p><p>XRè4Y\x001cC5R\Dd
¼ï¤zv®
¯¦³[Rè©Ë2âÊ)¾b\x001e:\x001d´ÇZW»Ê×ZËc-\x0013\x0015qª´õDy'v\x0006\x001e\x001dcj|­^ålÛuÂ	W1¹â0ðlu³e:EÜÇøA¯</p><p> ~Ûej\x0002\x0008½*\x0008N²)@ºV\x001bå8ÙNWÐ1¤&Ð«"\x0008ãEÃ\x0006dø\x0003È _£;\x00126Ç\x0008B/</p><p>!\\x001ek/Ùª¬R:JÛ\x001b1x©	!ôª\x0018"¢Ø\x001b×\x001cçIö)ÝÁ¿g>FÔD\x0010zU\x0008\x0011·1¾y,Ëu%$i²·Ði\x0004>Ä\x0004M\x0008\x0001«BXz\x000cÄqX\x0014¤ÌÎ\x000cÇ¡ `U\x0004AB)|TÎhä\x001cfÆ®Ð^Ö\x0017\x0005\x0010^\x001b\x0012åà\x0017E\x0014ÊâDó\x0000Mü\x0000â\x0007¯Ê`Aö`d\x0017EDÉÎ´ÎcLM\x0000\x0001\x0002\x0008¯Hôè¹ÎFU:RÇø\x0001\x0016Å\x000f^\x0015
\x0018«­xTFÌ¸ëTþ\x001eCjâ\x0007X\x0014?x\x0008¢;Î
OW±\x0011ä&H
K\x0013\x0000\x0002Vå hçå0Ï\x0014=V;ÏOEjâ\x0007X\x0014?&Ê\x0019Jjk`\x0001ìhäac'ÿ}© `Q\x0004á\x0001XÀÔb1ã\x0011tÙy\x0013³yØÄ\x000f¸(~ð4\x00131<ëBdi£u¼HNÏL#c\x0013?à¢øÁ£.¯FÔqÍö\x0001¥ÆÇÔ\x0004\x0010¸* \x0013ÄÉrì<§§n½&ÀU\x0011\x0004¦{ l=Ç]BÉ@HrÜéN§ì1¦&ÀU\x0011DÁyj¨¨bcò(L83\x001eÇ&ÀU!Dº¤gÑµ´÷ìiDéÊõju151\x0004®!<È¾K¬a¦ \x001dQÎtÊ&151\x0004®!¬.6"xºéf[.\x000fÎ\x000ef:\l\x0008\\x0015D¤\x000b \x000b%sPÖ©\íh^\x001dcj\x0008\\x0015Dø²Nô¾\x000e¼N%
álG\x0007ä\x0010iÂ\x0008³*È\x0011=LsÒÊ\x0008ÒÔlr;6/§*é'kÞ3\x0014ç¤²9=¥AyÎùkÎÉÌ?\x0006Æf `~× ¬y\x0007H\x0017DNMà&\x0018ß\x0001äØ\x0019p\x0014í|7âºEK¶CÊ>:¡y)ûè
ß<XPp¶ðyEý%\x001bÒ§Ç\x001b'#Tæf*ü9\x0019øuh'qWî&Á¸«$azM'_Eë\x0014AJíÑ\x0017\ë°@S©p^1K)\Ü"=é\x001cîðc_`i@\x001a\x001dz\x0012Ö\x001fðÜÍ¿¾}·umýóÛ»_ß|útQãVú[üáéÝßîÞ½ÿüñÍ\x001fH¯C!ç]¢¥Ñß\x0018¹À\x0010Ó-¿;\x0004î'Ï¶v­~róôñ«W­\x0002j</p><p>I\x00119c\x001eéÆ4\x0013\x0006?Ö U¦c\x0018XcàD\x000cY\x001b&RL\x001fÑÐpß\x001cZÓTy\x0000ÂÔ\x0010f"Dº-å¦øm-"S\x0018e-¾îWaØ\x001aÃNÄÈIy1lÁpV¶T¯}ù\x0018«1ÜDt'Rr2¤)\x001eÕè)-\x001c£ð5H\x0011\x0003s¥Å\x0010=´bàÅ°_7´Ç(BM\x0011&RÐc¬áû)P(¨g\x001eF¬1â<\x000c[*2â¦ãO\x0006\x0018c\x0018c\x001az½­\x0008íäõÔ<@
?&3Î\x0010o¨b¢:¹\x0016B·¾{¢ó&\x001dÙÔD]>Ü`­Øá¼Ç+Ñxn=ÑuÓp\x0013`\x0006]·u\ß3O¶n\x001c·è¹ÓUÿO¶÷Ü&@ÉNØq°Ç\x000bÑ¸m=ÑoS;x~U6¹ð<¨ ý\x001bn<N¢#2{l)\x001a§'z¼t·åß1¹hnÙG¯¹|\x0002M§Ôà\x0018Fã+ôDgÂq:\x001bMr\x0016\x0006\x0018Có2z¦³ædÀÄ\x0011B`9ÐH}ÔyL\x0004:\x0010\x000c»'\x001aßDz¤</p><p>\x0007yÐô\x001ck.è\x000fwü´A</p><p>ñâ5 =ç(8\x0017ÅÉÜÙhSP"(úäÂÝ×/ä¡lwoñLb²Ë§×_îþú·«ÿç?þóæÝ¹\x001d\x0000üDãCÜîÛ\x000b¯eF³îÔ\x000fHå÷7?¼ \x001f?\x001bNYa$¨`\x0015ö|\x0001ñ4fS¦K9\x000eRt®CH¶F²Btl\x000bR(,N#f\x000cö¸
v\x0017«Ü2$Ïï> îÍd¸ðU'£7ëØäk$¿pra|Z%ÃÏ3´JAV©ÓÀp\x0008)ÔHa%\x0012%\x001dÊYB\x0016Ð\x0011ïéïß\x0014k¤¸Ê<P\x0008\x0004w\x001dúÂ3\x0016ÁØÃS
7 \x000b®\x0001Y®ßÖHó¶³*\x0014¦±"Æ.¦Ö+-sKTqÈL D«D[ÖÐ÷¨GíCj¼^ç\x0015±\x0012/Ö£dFÃ\x000fö2aÃ«HfÑ±\x0011ÜÒé@q/q2âpè\x0010iÌ*&¯X&'1y+\x000cT~ÃLfÉÓMø WÅ\x000f1D¾¢z\x001aÊËãÆÁZÙ{n¤Tº©\x001fôª\x0000"F]LÜy\x0001'®S\x0013@èU\x0011ÄoËÔD\x0010zQ\x0008aÓ?§ø°IøoH5ruìuß\x001eBj"\x0008½,H×</p><p>\x0005)Êq*±kTó¢\x0008h¢\x0008X\x0016EÔL(\x0003ï+¦0RÈÞËÔD\x0011°îr»ÍË-\x000b·i\x0019úJÛy{\x000fÚËí²0B|SÓm]8\x001aÈÚì\x0006jb\x0008X\x0016C\x0000pµÚxE]O{ÖH\x001bo4a/S\x0013CÀ²\x0018\x0002\x0002K]ø`~£öQâ¢y÷@h"\x0008X\x0016AØÈD)\x0010]\x0008\x0007:yp÷¨\x0007îbj"\x0008X\x0016Aø\x0014½2çA)ÐCW&n¼&e\x0001vüj\x0002p
|or(^è¼lícÒÐ6eÐ\x001dJÔõo>ÿôþ_\x001fÊáÓÇ³]à÷6úX&H
\x0014Ðo^?zþO÷;4ß\x000eS¿=°¶ãydÎÈ×Ë,0\x001a~Ù×cóõ8óës\x0017ºf0Rc|ëÓß@\x0017~¼i>ÞLþx\x0011µ§Æ Ë4ÁdíË>Þ6\x001fo'<Õ*<Û#}¼\x0005j3Ð:¼ðë]óõnê×K* (R\x0005_}°£9ô}½o¾ÞOýz'"ÿ$MÅMR6î`î\x001f\x001f\x000f?^ÄKýé7\x001feÐ\x0002\x000c\x0012K\x0017~|l>>Nýx+j2Ê${Ã}Æ'qå^!åå_jd ¯7jÕ×\x001bi<}¼\x0019¼]øñ5S¬7ÒÊ¤\x0012_½\x0013ñÞÁD½\x000b?¾ñ²fªMT\x001eÝ­|$Ó?¾\x0017ñ\x0003yÒ\x000b¿¾±7fª½V´ðH\x0019ßUT\x0019ñ\x0002|\þøN1w8{;N?¨Þ_|øû_ýüæê×»«Gÿ¿\x001eÛ±ZÉ=Ç§[\x0012zIÓ\x0007\x0012Ê\x001c/nipÅÕÓ«GÏ_$?ÃÙû1aÁ:,\x0012«Ï)«­}6´\x0002Ê	k*\x0015ÖT¸Ê(yËóTê¡ãÜb\x0018
\x0017Ù\x000fej(³\x000e</p><p>\x001dÏoôÔiyð¡áúô\x000f·Ã»ö^,[cÙ;\x0007¥¥òe"\x00178Ùq<c/«©Ü2*R3.çÊI1D4²\x0005GãØ÷cù\x001aË¯ÃJ·¼\x0008Å\8Í"åÅ\x0008åÖ÷R*¬£²ëKýÖÇÍ\x0016\x000cÊ\x001et\x001dÍ«X±Æ\x000b±Dp-aAÁB\x00143è:%ÌÇ°*9ÐÐÔ\x0000Lçünä±Ô\x0007Ñ\x001dX Æ9Ô½Pmx±.¾0º$ðIóÁòxhpa:k/W\x0013_èu\x0001¡\x00066¨¥RÈG+^«§\x0007s«0ôº\x0010Ã õP&åhyD</p><p>ÃiÊû¹ C¯2HÆ0F§õR'£á\x000b×h$ã~®&ÊÐëÂMø¯,\x0017\x000f#U¶²\sL<âÙ­\x0012ê»\x000fo~~óáíOW?¼ýøéÃÝ¯\x000f½YÈ
ßÈ©lµ,<Z\x0011Ä\x001aÍÿîöñ·o<ºúáÉËW·7OïG\x001a	Ö 9[Ô'mb,k"
c{
\x0006Ç°FÂE«DÓPXq$Ý!-ËÛä\x0006ýH¦F2VIE¯Þ¢wxácéÕ\x001e<'íG²5]´J41\x0017ÉÑH¡<\x0000æ4Deð\x0016°ÈÕDnÑ"¥(ÂHC}ä^\x001d\x001b´:N~w¦uð5_µïPä\x000fhT-òQò2»ÊÒààyH±Få\x0002[\x001f%/é°#ïuH·^i[r</p><p>8ù\x0012¨+Z\x000cq;3\x0008ö#5&\¯²áÑÉÆ#ÛÇïU^ÞÁÙ\x001c÷1¦ÆàéE\x0016Ï9Íí­ÆpCÎ*\x0007ÃÍëàÔ øó_j476ß$Sæ)U´
S\x000e2P¦è¹«u¦&²ÅFËÈ´-±\x0004XiMÅDE\x0002u0dí"²ÜL\x0006§aqòZP$Eçïß}º\x0000æ¦2CSÞsãe i¥
\x0000\x0015\x0017u¡w÷H¤@üù³W÷9Ô_\x000eS¾<\x0006Jwå/·\ÿZ"Sô½G½õ§ãO'\x0011$þ¥d½òïÜqi ûO.ýrS¹ñå\x001c~nÁ\x000fé÷¯sÏ4ËaÐê½\x001fnë\x000f·3><ýRóm3R}\~±´q¸£5`G÷{ï»úËÝÍâ\x0003Í?Ü>Ýx6~ÓÜ\x001a6ÿ/÷õû9¶Eç¸ÃQ¤Ã\x0019´d[¤a5j\x0018ë\úé±þô8Ë,n'ôìÓE¤aÖ§ëÖ¢Ï1égg¦o\x000f\x0012î¥oç&\x0012¾Sõ~é·×sÈå\x0007å¡7'>¼ÿüïÔè|lÃ#ëÙGg¥\x001a<mxÑ4°$tÕÍ\x000cåÐíó×ÿB}Î÷C@
\x0001Ó ,\x0005\x0006¬DäÇA .BD1\x000e¬{\x0019°fÀy\x000b|\x0013°\x000fkv° EfÌã \x0001¾ÁÔ\x000cfâ:8î\x00004hÉ[Y\x0007p=_{\x0008ÂÖ\x0010vÞBl"o\x001b\x0003\x0015\x000b{^"A\x0014F\x001dT{\x0019|Íàç-Dº¦q I\x0017<ò%E\x000e^Ô\x000bâ¨w/D¬!âÄ\x0014N\x0000îeK1gQ{ë\x0008s\x001da8é(mæUM<Ö2p<ºtgác­9ñÖ</p><p>UÏ!¾.!\x0004­è!Ò2 ï¥\¸ÊË åP\x000f»×¡ñ\x0010z¦ðtÉÏ\x0014p2M¾PJ}öR4>BOt\x0012\x0011Y¶¶Y\x000bð°b-\x001a/¡gº	Ù(âµ7â&Ø_;Ý\x0019v¢q\x0013z¢\x0008ò\x000c(Âµ\x0011í\x0005bâJ¸ÁÍ[	"-FS\x0004\x001dCør¶a¤Í±¢qvz¢·ÓÈÜi%ªðïd¡Fì{)BC\x0011æQ`¤þ±¼\x0016@BÆm"5÷Ì£h|¶ç´­ÉlÛ©`Çµº¡s;Â\x0000Ïy>ê'\x0003û EyT"G\x001bFEy{64N\x001bæ9mÄ\x001d/CÓp²\x00100ªÜ»\x0010íµn¢Ó¦Ù§ÍÄBur%J\x0016vÐ¸¡qÙ0Ïe[-£\x001cbºÂ±\x001c{Z	%ÎÎuÄ@\x000fQ4.\x001b&ºlQ~i?cí³ÃY\x0002h<6ÌóØVGÊèmK¡z´¶\x0012w'º\x001c¢h|6ÌôÙÒù\x0019·Yc¼¡\\x0018°§.{¢ñÙ0Óg{îKkáÊåÎ\x0006YÎÙ^ÆeÃD
®í\x0014IuÜ¾bâ©h<6ÌôØVôí½õ$"ÍÑ¸ì§01\x001aÇÆgãDM¢e9\x001a÷Æ¾½¶AÎ¶ï=DÑ¸mè¶I², \x001cù¾|×¶òB\x0008\x001e¹Ý\x0014ÛÆÉwm^\x000bê,>¿jQ
å^6\x001d;ÑoçÂí%zíyCIU<\x0006\x0018\x0014\x0010í¦h\\x001eÎuy>[¨è\x001c\x000fàH\x0016JÉ#¢\x001fÉ\x0004ì¥h\\x001eNtyJóÃ?é"Ñ]/\x001f\x000bÏkÎöD\x0013Õ¸<èò\x001cÏá¦g.%:¿ ¹n\x0010£\x0018~`ãóp¢ÏS"\x0014\x0019¥\x0012Àp[\x0005z×\x0019/tÂ4îÂÌt\x0017V¨\x0008¦\x000bkätãHûm/EûÜ2÷½M\x0014MÒ\x0015'Ï-i}æ-mÂN\</p><p>Ø\x0006°n\x0014þDQ¨àGµé»£òZ6#s©W\x0002£¥~ \x0001"ByNuà&¦¢àÏwgéò»ßÍSÞV/¦+Ù(ùAÉF=þëÛ_ß\½xóáÍÛ\x000f\x000fÖËñ QnP1í2Ë\ºÈ\x0007Õã\x001f<}|õâñíã'·÷ÃT2n	FÒRÓa\x0002KpDGÃÛ\x0019Æ	LègFvÒèF/¡qüz¿©\x0013\x0004V'\x001eXØLÁ$\x001ahh`ÍÚ0Jº³V\x0001Ò?ý;I°!Á%$'y#\x00034j!ÃH\x001eHóî1
Y\x0004\x0013\x0018\x0006½\x000cØ¨</p><p>LgÊ\x0001\x001aÛÐØ\x00154h¸\x0019>Ñ ¿\x0003&\x001a'Ö\x000c\x0007B;i\Cã\x0016Ñ(S\x0014,« 'hmú\x0017Æ4¾¡ñKh'q¥+¼º\x0006VwB©O>t9\x000b
MXD\x0013x§T\x001b\x001bg4"`â\x0006/:;i(\x0000D\x0001¨¸Ú-¨à¹?ÑÈ\x0010\x000cí\x00075%ûh°	\x0003pI\x0018hÄ4Pb\x001a,â2aFUù3ÄÍÓ¡B,±Í	JO\x0018.Ý\x000feÐnk*)Ì\x001bÍÇ«o>üý¿~úåà+1ÌÉ¯tJ®]~<DçË¥¬3Ü1\x0007Î/¯¾¹}üèûÑ@"ùz¨¿\x001ef}}y7\x000c¤\x0014%_Ïèã° `Ç×cýõ8çë½</p><p>RXB\x0017bSÙ\x0018½To/Ä;¾ÞÔ_ofýî=òç¿{IÎûÕÛúãí¤_=¼"D]\x0006í\x0019mdÛ\x000f\x001fþw|¼«?ÞÍúÍ\x0007\x001e¬Ñþæe\x0004×¼_½¯¿ÞOúÕÓ7rY<ZÏ\x0018)	8ÒÎØóõ¡þú0kãà5Èï>ÈP=£ËG\x001cóîùúX}ôõÎPý4\x0017qN×8_º`G¼üë«\x0002UòUjÒç[M\x001a2Ûç§èsoÆÊ\x0008=\x001f\x001eà¬r¨ Bqµò\x0003qµ7½ûüáÿP¶ª|î\x0003£\x0007ëH\x0005m#¥\x0015\x0012W\x000b$\x0001\x0006²é7?Ü¼¾ý_¼âÿü~*¨©`\x001d
\x0016Ù¨²ðm¦fU°8P\x0011Ü5\x0016®Ã2Q\x0012?Ô÷tÆ</p><p>rS\x0002\x001c(Õ\x001dÀ25Y¸Z"¦ AKT¢</p><p>
®3ò ­©ìÂÅ2\\x0006\x0016K\x00065yåE\x0001\x0015°Ó\x001aw\x0010ËÕXn\x001d\x0016\x0016\x0015\x0019íd,¢WÎÖÔÕò5_\x0015x\x0002uÐFÆí¦Õt\x0017\x000cº\x000eP*,=Y÷ ³ì®\x001d1\x001fT=\x0013+ÖXqábÁ5z^,<íA£EÍGó°ªiu´pj¡É\x0000\x001eÐL¡\x0008;oB#Ë¾¼\x0003\m±0ÈÀWü Qæð¥ÆGÚ\x00031èý\M¡\x0017\x0019\x0018¹ú(­+û0ý\x001c¯AÂ\x0001®&ÌÐ\x000bãRÖËd(©WHÕÏû\x001f`jb\x000c½0È@/Ó\x001b´õ<ÿ#ÙP\x0002Ý ó\x0001®&ÊÐ\x000bÃ\x000c-\x0012\x0019i­$ã\x0015rçbZ­vÀA®&ÌÐ\x000bã\x000c\x001a\x0014ÅÆ\x001b+6Ã\x0015\x001b?õl5q^\x0017hØèI·iã\x0002M\x001c\x001b</p><p> \x0007\x0013Ò\x000ep5^\x0018j(­CÙ û°ØB=P=ÀÕ\x001az]¬a7\x0003
ÒñåÓ-¢¬×Ô\x001b24±\x0006¬5,)Nó­\x000b,wO¥}\x0018Å\x001e\x000eÚñ\x000e`5¡\x0006¬\x000b5lÀ²
Áp\x0019ß®G54}«Mh¬\x000b5HîMËrÅ\x0013\x000bÂ5\x0018e|«	5`]¨®(åxi{Í"õ>H°¡\x0006©Ø\x0003XM´\x0001ë¢
\x001b\x000cMËË\x00150/\x0017å\x0019ÈC\x0013lÀº`ÃR¿\x0003' RÜ\x001f·]tAnÉjj\x0010\x0005M°\x0001ë
[\x001cÑábª(ã¥ÒbÍ¼NB\x0013jÀÂPÕ§³_Ójér¶fR5\x0006¬\x000b4,%AÍi\x000ffiæNÜ=Ø\x0004\x001a°0Ð0®ä¬«Õ*)ë©«?ÆþØH}oCeN«5õvbª|óª%Ao<\x0005Q)Näà°\õ FîH¾æ\x000b:½êLyí¨\x0013¯ÌeGéuø.,¥Ó(6\x001f\x001deêóÒ\x0015W\x0006fé#\x0001ð9\x001d,];\x0011GöÔÔt}ZI¹Í}SqçtnéÒå9»ùÅ\x0008ËÓJ^
£a</p><p>_Ò}}`XIx|±-×²Q9ý2O¥Ä`îËSÙà\x000b6XË\x0016¥\x000c_Ê<é/\x001dôîeS_°©µ{Òäfµü^Ø$à\x001fU±íDkÅóÛìJ2%s\x001a,ù»|ÚÊ\x001dÍ¦!îDÃs4\j%©\x001e\x0013\x0000¾~ê<Ýç\x0004î3$Þ|83$ôeÞÛðìÓíAC\x0013[n »\x001e4ï#û×Ïw_Âñ\x000f\x0017>DóDc,ÁÈCt,åÃ×\x000eôY5\x000eè­\x001açÉ_ÿv÷ñã6yæÕÛ{ÿëÛÒ\x0004rÒÛ¼`d»QÁiü×¯ O~xqóòå6sæÕ~þôIßW\x000b\x000bÔ,°%¹0<Hããsf\x00115{0bùúÖ;À5\x000b.a±®ßXØøIý»&ÂY,¦f1+X\x000cp½lb\x000e}O2ð\x0002ÓÉJ\x001d±5]\x0001c5_½\x0012ådO"G\x0005æëÇÿ\x0000«aÜ\x0012\x0018Ï¶lÛew1PÌ×\x0003Ú\x00030¾ñK`,GB	ÆPs\x0002Ó¹ó\x001f	5LX\x0002\x0013d4,Á g\x0018[¶Yç¹î\x0000L¬aâ"c\x0002£Åe¢á©ÑúYùT3³yLõ;§iýÿ\x0000@q\x0001\x000f¡ä# \x0006ñ±£·ºFGl£ô­¶øýçO¹6úÅû¿þí¢Êè!K</p><p>¡Å¥{\x0011kU¥Ço¦Ú«Ø	Í¿~ë¤_<ÿáÅ¨LZP F\x0005(ò2H"÷:t\¥½îMPÙM5	Î'A¯òè(O\x001dW<<9LÅX&ÄÌ'ÑNQªuCQË á(ÆÞut7«AÜ|\x0010P Á%\á\x0016);KÎb{</p><p>¦»QB\x0012\x0016  È¤g\x0007EöxÚ»^*|/n\x000e^pR\éÉG%\;+eö2[\x0017z%:»Y|Ãâ\x0017°8Í¢ËÞyËó©¿Cæéª^yØnØ°Äé,45ùÆo½\x0016±\x0008W^î5ïeÆCÂ\x0002\x0017IÊÈç%Ýd,»{-îÞòÅ~\x0017Ù\x000c\x001ceàØl«¬5Ë\x0012yªq3ù\x0015Ý«ÏD½!Fûô9^BôÛÙ6í\x0003%DÉJÓw\x000bR8Ï@®§û½ßß\x0003%@\x0010\x001dë±{RË¯\iÓgêB ¯§ÿN4Uv3ÓlÍéNÔJÆé(1\x001a=-H<à;(\x0017â\x0018{\x0016ÿ\x001bÛFúã»wéO7\x001fþú÷ÿ~ð\x000cí\x0014<³dmPez²Ý@{\x0005Úÿx{ó,ýéæöÇ£)ÚÌ\x00055\x0017,ã24</p><p>E1ã\x0011V. ë^Aá}\XsáÂõ*þU\x0019yÂr!J¡66#\¦æ2\x000b×Ë^Ër\x0015Ç\x0014,\x00196LïÇ²5]\x0015yhà¶\x000bs³PòSXVkØI½\x001fËÕXn\x001dÅe¸>ÞÒÏ Í½Êéû°|å×ayÃú\x000bYæ$ùÛ"@5hY;\x0015j¬°\x000e\x000bÓ\x0005Õg\x000cÎrAKÿ¸Æ{uÉ÷qÅ+.Ü.\x0018Yb+\x0016£Qtémþ»©NÙÒÍ#«uX ¯±Ì&½e¢tÕ$®¹`m¨±.Ö0Æò4À´^f>më\x0005¾,Ø½ã\x0000÷5±^\x0017l Ígd§\x001c"K­8\x000fV\x000eX\x0018Tr}\x0005l\x0018\x0019ê&ÒÐëB
\x0003^]\x0015jÉ«¦0Q|2\x000c$,,Wãõ:§.¹<Zi\x000b6ò\x001b«óév\¼òT÷¥\x001b÷¥×ù/ôX´ÓH]ÓÇå|Y\x001cm4\x0017È-âhe§\x0008Eº3ð~prÏ÷ÎÙið7%âÚäß-[9k¤«4ür²óÔÙ+\x001a~sÏ?_ºôO_¸v\x0010F¡v§~;\x0007Z¸l§\x0012àphuÎ\x0017nM8\x0005èO¦²\x0016âä[þbùVâY\x0015K°3\x0004Åª{Çé]îÜ=\x0007³K×T³]	ø-_dÂI\x000cx×²ý¶úógæäÇu\x0000øõ-l£\x001c¤8å\x000f¢>=cÍÀ¥ª¨w½Ûç«ïÞ¾ùðæùãã½G]z\þi$ßVwé¡\x0019DÃ¯¯¾{òøöñ×G7\x0010PCÀl\x0008<07è\x0000¥ÕP4òº9\x0010XCàôp¢\x0001LÊ'\<­LYºÁÔ\x000cf:CÌs°\x0003½ë\x0006éÐ
Ò0Dt9­\x0011ìtSSx</p><p>òÊp¥@Ð=½\x0003ÂÕ\x0010nú8µ({I£\x0007¯\x0006Ë\x0019|Íà§3T1Í©´!D¸iÊBÄ\x001a"Î YÅ¼\x000e§\x0007º\x0018]é\x001b\x0018M¾A·.bºp\x0015\x001f\x0013ErãÒ ^Äéì\x001c\x0017ÑÄ&(±ÉLOáøtM]=-'cJ\x0018²°ÐæÉgË\x000fÈg¿øõî§
ãÑßÿëç\x0004¯¿ÔÝL:·2Ç`\x000c´2QÆÄx×I3¾xzóhûøG¿\x001d+\\uùvóíÞò3r\x000c¨YC\x001dM:Øüí¶cö~;Ößs¾Ý!ÇPÚwSTää÷{¿ÝÔßnæ|{º-VkrÈ¿\x001d±Ì\x0006ìhKìýv[»óí$
Ä"¿:íwþvÍ;è{ó*ö~»«¿ÝMÚ3F&K\x0006\x000f\ÌN\x0012¿E#·c÷/ýv¶µ3\x001am­Fûþc²ô}\x000eÜ\x0010\x0016m4²ßUÙ3\x0016{U¬ï{ûüe²\x0003ybùx¨?\x001eæ|¼²\x001c½E\x000ek®B¥Ùábòe>\x001eëÇ9\x001f\x000f\x001b âV2lø\x0017Ï~\x0016­\x001eEm{¾ÝÔßn&ýâ½XI§L!U:FùÅ\x000f4½v}¼­?ÞNúÅcÒ"©»DÙñ2ÀÀªÑõqÏ·»úÛÝ¤ã2sÔ)ÅZ ¨@\x0006Ï[3x¾ãã}ýñ~ÎÇÓ¤\x0018ùÍëò/Zâ&Æ±ûÅ\x001f\x001fê\x000f~ó[¦uûø\x0014æç¡=H\x0003ïø7\x000f\x0003í=\x001fÒqß¬¼t`¹76\x0019 Ñ¤Ì\x0006uíúöÆÈëIV^óqÈï·ôk\x0017\x0013¯\x001e°g¶»:¯\x0011S§\x001a±<·æQúï?¼×\x0014²\x000c*.\x001c°¡hÝpïÁGÏ=\x001bJé©SYØT\x0014ïåíõ<\,Nd3\x001a</p><p>°\x000f\x0005k\x0014\±*ZÊ9¨T ¬*(+â>\x0014S£\x0015«\x0002¢·ùç<\x0017)XIÀ\x001b~bk\x0014»\x0002%pÙn0é6/îiÉÀGCÃsP\â\x0016 PkXFÁ\x0018³Þ\x001fu,J¯`w7¯IüE)\x0003R
]/ù¨HvË¸Aè±$Ô$aÅ8©gÅ¨8QG
Öb-Ì:)±F+\x0016EFI`t\ßÖDª/í\x0007%»@*Iøª`kî¢\x0018\x000em\x0003&£ìù¤\x0018I<Q1î>ÖÕ¯ðõ\x000e¨"kcIXÀGÅ³rïHÄKQ\x001aW¯Wøzê\x0007×âW1ÅAâ@7w\x001fKã õ</p><p>\x000fIsW\x0004\x00082</p><p>Ê©\x0007uX\x001a§¢Wx\x0015ã¯óS;Vx\x0006\x0001/GEÏ\x000bZNe;9l¹[`Â4ëöÐ-EI+Í\x0005fôà°\x0017æÇ\x0016æÇ%A\x0018¿PäR\¨LÑÃÎÈ¥]\x001a·biRðâ(ýÆ\x0016ïrß¤ÍËa~la\x0016,Ío\x0016µ*sÛ\x001d¬:k¯9z±Î7J8]ÃP'\x000eRûô9^CDbær\x001bóü\x001cnc`ä66\x0018!µ3Z>'òK¼2\x001bçvd\x001bµ/îóBsÐ\x0011$ÃóäE~\x0019H_÷3/î~ý×Ïoÿþ_\x001f¦Ü\x0000¶^½H½\x0002FBMv:Êu^Ò_q2æÑÍÓzMª£\x0005Âó$F~/Xä(<Û¨PÆ\x0001Ò\x0019âHþ\x001b3©°¦ÂuTç¥§µÒü\x0012¨Äpo&RÊ,£Û+}Ô?¶!\x001dHZ5\x0013©lMeQ%/£F\x0012+#6OÖÊLr5[\x0005å\x0017\x0015¨4U'mf¦³d(Ý\x0019ªtÊ×T~Ý\x0006Âr\x001faSäÝ*H\x0013GúO5¡¦</p><p>ËÖJ\x001b\x001e¨äÓYd[:a\x001c\x0018mÿôT±¦ëv`Fù\x0014\x0006ñûjÚÅ°wTAUé\x0011~´YDE¥ÿ,\x0001¦ñU,²y_/E>HÕ\x0015Ëâ</p><p>¯OsÑv \x0015kÑc\x000fR5^\x0016Zx§Ê¹Ò\x001bÙlt!ÈbuJ\x000eb5¡^\x0016[øä¤\x000cëP¦Ën{e£áÇ\x001f\x001d;\x001a\x0007©ÐB/-¢5ÜçÓyby\x001a\x0007Z4\x001c}¯1ã V\x0013[èeÁE</p><p>ÿh×¦\x0012ÓbåÞt\x0004d\x000fê©TMp¡E\x0017Ñ+\x0016èö[GCîÁ\x0006y\x0014Ö\x001e:B\x0007±èB/\x000b/2ü\x0016é=Ý\x0015³|\x0002îÁÖÉ;OµMx¡Å\x00171ø¢DÃ\x000b2\x0016X,\x0016ìXM|¡\x0005\x0018äs®÷ÖÝ\x0016\x0002æÕ</p><p>zæÍ\x0011\x0008\x0003E\x00181hñÅ4 'éI,c¹\x00083W\x000b\x0010\x0003\x0018T¬øl¡\x0015Ît\x000f.JPDÌA¬6{±,Æ ³¥dµ¶Êå|¶ÀÉjuFÖ\x001cÄjb\x000cX\x0016clJ·Ù\x001bû2¸x±zB·\x0007©\x0018\x0003ÖÅ\x0018ÉWiÑî$V\x0010ÉÈÈÆA¬&Æe1\x0006k\x0011oâ\ÏGËq1¨\x000ezÊTM\x0001ëb\x0014.EñZPNÖÉgÍ\x000c 0`]ahÈ{µUnK\x0015D´4`§\x0010ð Vãa+vß¨Iê73Å(¢4Üd\x001e\x00136\x000e\x000b×9,_L ½)²\x000cÖ²\x0003ê|:Õ&¦×Yöd\x0003-/\x0015Ýs\x0006#¢±3\x0011é Vc\x0003q
^L»3ATP4
$ÁöX½Àeö"]8.*Nxº\x0014¯Ëj¹NWæA¬Æ^à2{A/=\x001eì$Ou¥ì\x0019cÙ©9\x000cÓ\x000c³ÌdÄt
Q|¶T¸\x0014\x0006\x0016ðNñAªÆbe\x0016#\x0006\x0010a\x0015\x001d9 Ñs¹ìÏôY¦±\x0018fÅQ±¼§ÑåVÌÚ	«S#v\x0010«±\x0018fÅ°!çÑh\x001aOBÈÝÅNÅÈÑ»~U6oû?®²ðéÊe\x0003?g¹t\x0004ä®ï§¾}'¬Î°~ú\x0007À:u·=Ó\x000fV½û\Væ£	åYÕI¹\x000f)9N}T8gãÉòº\x0016X­Ñ\x0007¥ÈêoIxË#</p><p>uú¼jì9±ëà¬R^B_KåÍòb\x0019u§õýhäûÅ®\¹-CÄ\x0012\x0000û¢\x0011­Ñ\x001aë;eÎ_§\x001b\x0005é/ÖM/\7\x0013RÐ!£ã´æ®P§HÙ\x001f¼:¥Â{Ð´Ón*Ò\x000f¤]ëû7ï>¼½zöþ/§ìCoJ¸ÂÊsý \x0008üG7¨åüþñ³Û'WÏÿñõx\x0017</p><p>\x000fÔ<°'@ä>u\x001fb\x0019Â\x0003J
äÉ÷òÇ,á¡z à!rù"éµAEÑw\x0004\x0003¾\x00023Þi®&qHüi§iÎ\x000c&\x00187U;PÙ»2¡æ	kxÙö¼2¨ùÎk]ÈºäNJJ,Z\x0003ä´T\x0004\x0000VÛõ*\x0002¤ú©{°\x0001Â5@éV\x0015¥·\x001b\x000fèæÑØÆ®¡±QËø\x0018¯#ËxÅ2è\x0013:Ï {¨H½­µ%Ópwóëo>|J\x000eõ¯\x001f>[^=L\x0011A9Qk¤ÛD¿\x001e%Èp¼§ß<¾}Üé\x000f¯/@\x001a	\x0016!Y%å÷ÊYº$nHRãsÏ$Ö}<Xóà"\x001e\x0012µg\x0005ÝtÕàÜ1±¨Ìvtû!\x001aÉ,B"åµÀÇ(y±tÙàbuÝ3ÛÇldWíº(ý8"ï
ÉÅ"ã\x001cÆs¦÷!¹\x001aÉ-BJ¦Û³mÀ@å=\x001bR<I7w$!ù\x001aÉ/Bò¡ </p><p>©(6\x001b3\x0013)ÔHa\x0011R</p><p>NY¥T9V</p><p> 5tæh\x001e#5Q\GäDySëb"ÑÁ\x000eî!¤ª¢NZÃ\x0004:ÒãIy*­Ý\x0011¦dÚ'2µ¡Ã¢Øw6\x0014F0\x000cPè\x0019\x001ccjb\x0007½*xÐN\x0007­¬Lj2Úè=\x001b\x001ecjâ\x0007½(\x0000ëã&(\x0003\x0006¬¨Æqæ25ÎV/ò¶`¥#ÑGjåËÙªºg¦^ÿÞÁ­WuÀæÍw÷;Ý}YÐ¨\x0012Ë\x000fj¥¼G¿Þ}þ÷.K_h(m\x0017YF&;fÝyDÃ¥¥è Ó\x000e!2JÞ¼þÎí¨ùxS¼óñ\x001e¹:ü¸NÒ?Þ¸±ôÖÅ\x001fïêw~ó+\x0003¢O1uZ~ó<\x0008]\x0018HÙìúøP|ô·$êÝ#¹æHJÙS>þ$zF\x001f_=èWn¢)j¹\x0006éWÎ_"®Ý_¯¯×s¾>Ý/c(j®¹\x0010\x0017Qsí\x0005©¹NúÝ7öFO28¤Ç:º45ký¡S¿Þ\x000eÒ³»¾\x001e¯Ç9_\x000fJ\x000em°\x0007á"\x0004'®.Ì1º1z½4<ÊÚÑb/Mùúáº\x001d_o¯·s¾>YIàß=Uj³Í\x0011q´sã_v|½o¾ÞO²9"\x0015Cr´­=_d1¨NÞîç,ª:ÿRg\x001dÿ|ÿá/é/?¾zu÷áÝC\x001fjµ6¡\63ä
õïò
©ã|«G½?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
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

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-+1Dtalu3FhzBIHYonttUuPOK9Ls`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-qkZFXyAuuPeeE/k7S+3m5jAZ59E`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-SpdxkooqzFSFGyccnD224ONcJ9Q`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-suEXx6Pr1McTi25ijcm60zJsisE`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-SpdxkooqzFSFGyccnD224ONcJ9Q`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `9bca-fuIcpaNm5NhICWTVCW9/XneVxBc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `809d-aYymhEC+MoegLu+S9ar0c9toJtc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-ACO4JLIME9mjCUpenQ70w4sxkVs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-Du+DFHGoWTgy5bb96NnPQPKDmJw`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-+1gt98MqTYK0HwVIxv+UAou1acw`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�����C��n�Xs\x0004�آ{mR��+��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{},"isSafariBrowser":false,"__N_SSP":true},"page":"/bas", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `366405469`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1611761132`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `273111588`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1439655420`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1919628686`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `912784966`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1838188997`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `831362559`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1745640841`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>366405469, which evaluates to: 1981-08-11 19:17:49</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

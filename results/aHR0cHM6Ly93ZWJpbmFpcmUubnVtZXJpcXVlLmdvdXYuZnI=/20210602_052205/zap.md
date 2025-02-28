
# ZAP Scanning Report

Generated on Wed, 2 Jun 2021 05:16:35


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 8 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 8 | 
| Reverse Tabnabbing | Medium | 8 | 
| Source Code Disclosure - PHP | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 1 | 
| Cookie Without SameSite Attribute | Low | 3 | 
| Cookie Without Secure Flag | Low | 3 | 
| Dangerous JS Functions | Low | 3 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 2 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 14 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 7 | 
| Timestamp Disclosure - Unix | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="https://www.numeriques.gouv.fr/rgaa-accessibilite/" target="_blank" title="référentiel général d’amélioration d’accessibilité - nouvelle fenêtre">référentiel général d’amélioration d’accessibilité</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.cnil.fr/vos-droits/vos-traces/les-cookies/" target="_blank" rel="noopener">http://www.cnil.fr/vos-droits/vos-traces/les-cookies/</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf_link" href="https://visio-agents.education.fr" target="_blank" rel="noopener">https://visio-agents.education.fr</a>`
  
  
  
  
Instances: 8
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/5.G%C3%A9rer_les_utilisateurs_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/5.G%C3%A9rer_les_utilisateurs_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=5[Ýþ'òÁMºgª]ÓÉhØïõú°Ï?áxW@÷kw¿ÃL»Þ`G0Æ_á[èvý{	LaÌ¾À·Ñý\x000e3íB\x0013 Æ÷5ñºi÷Ì´kÉ'Ù¼ûwï ×®Åø-t?×.\x001d½v-Äo£ûÏø\x0011vñ·Ôý\x0017ë¤[ü¤ºßù²÷«K/¾ÅÝ?n¡{ÐW.ÖPFzÉu\x000få\x000b$ªù½Ë\x001c¿îá¹\x0006\x000f&¹æÀ\x0015NÑHß²î-\x001bußBg£Íw+3.Þ}ìØ´A÷\x0014\,Sé\x000eìÞh²X_ª»OìëwáðPUiG Ï©ÚsoÙ¥ûsÌ¦¯]Ê1×ìz®eJ­Áâô¿ÞÖ/CÆá©îÑóbîçoE\x0019<T-Noø"}S\x0006y\x001e§\x000cñèñü~­îß\x001fª\x0000?txCçéÂýC\x0013üuÂ>ïþÂgÑ¬á÷s¸\x0002ÁOBñÔuéRÈ\x0019C:î¾[«{tÌðÑCußl?	"xí©Ý\x001b~³8¦ÝëQ÷¬£\x000b%rµÞl÷\x0004ãIx¨²tïeß=Ðù")ltÛqà\x000cÁ\x001bí\x0001;ø&ÝÃõ"©
\x0016ØèWù»*z¨²#üºÝï¢W%°'h£SðñéûÑý\x001aë\x001eÊ`óÅR\x0005´Ñ\x0007¯ìá\x001b98¼Öâ¦5x+R\x000fUvðó~Þ=K<~S]\x0016*pÌ ÞY}tjÌð]»V÷\x001cXepÅ\x00078bÑcÏßà¼Gx¥Á\x0011H\x0014ªÐý\x0010?ÚfoìfðÑ=ûózÒ\x001cyÏ2·µF«Û'+\x0001)lrÞsÔ§ñt¡T}l¶:=Ü\x0001\x001269ï!>_$×\x001d¾ÈE*W,UêçÎKM	ßÏ{Öx®@¬Ð¬.o(vÌ\x0016îÊ5(¡Ë¼ÙdÝóâ#¯ÝÓ,v·7\x0010'Òùâ}µþÄ´ºßß9\x0012¹J³o:´¹<þPì2Å¢\x0004Ü}i­»öÏ\x0013\x0008ÅRJ£7\x001cÇ¾`ô\x001c\x0000+au	¸ûu»Ç|4\x0001¾@$Êjí¾Ébs2\	Ðý`îß'\x00003\x000eD\x0012\x0019*ÁH\x00109¿Z¼\x0012\x0016v/\«û÷	 \x0019ü·ðÙ×0øO	¨ûúFÝë\x0000Ï\x0012¬ÔJx/¡\x0005%\x000c¿¬7Ô}kÓî+ÜU\x001e\x001aÍö\x0012f³é¨×,%7íþû\x0014¹þ^Âd2\x001evþ'*=\x000b0\x0003A	\x0016\x0008®@
ñq0¦RØ£:\x00013\x0010TÐ\x0002!2*"ÔßÍJOQZaâ\x0002H\x0005¨4°hF\x0004_@P ½\x00105Ã\x001eÕ	È \x0008	\x0004
H 8¹º»»Øë*óÑ±$Þ\x0005ð@àâæ\x0015@
\x0004\x000b++K\x0013]Ui!\x001e6fª=ª\x0013`À\x0008\x0004u-\x001d]\x001dMe\x0019Q>j'<¬.@\x000f\x0004)Yy\x0005\x00059)\x0011~. çim=Ì\x0005@\x0010\x0010\x0012\x0011\x0015\x0015\x0011äãb£]Ìcu\x00024;pñ\x0000\x0001\x0017\x0007\x001dm»\x0000\x001c\x0008lììll,À§§õHN\x0000\x0001&úÛ\x000eu\x0001Ð
 b\x0000,\x001f\x0005\x0001@\x0001\x0000Z^±
endstream
endobj
78 0 obj
<</BitsPerComponent 8/ColorSpace 132 0 R/Filter/FlateDecode/Height 171/Length 46/Name/X/SMask 77 0 R/Subtype/Image/Type/XObject/Width 127>>stream
HìÁ1\x0001\x0000\x0000\x0000Â õOm\x0006 \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x000e\x0013`\x0000TÕ\x0000\x0001
endstream
endobj
79 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceGray/DecodeParms<</BitsPerComponent 8/Colors 1/Columns 180>>/Filter/FlateDecode/Height 112/Length 3099/Name/X/Subtype/Image/Type/XObject/Width 180>>stream
Hì×V*Ë\x0002E¯£\x0008H\x0012\x0011¤ä $ç$\x0019$àÿÂ­êê& ½Ó\x000f>í1zîÅêU³þ÷¿ÿÿ\x001eòËËKð÷Ô >B¡R©\x0014}jC\x001eHL¥Ò\x0019\x000c&N£\x0002êS\x0003}û`Ä4\x0006Ãåóy\\x0016F9{hDÌæ
7\x0012©D$à2Ï\x001d\x001aö\x0018\x0010ó\x0004bùZ£Q+¥B.zÎÌ \x0016\x0014*Å\x0015\x0015÷Ú'Íf6¨e×l:ål	â+±ü^grxüÁ×aTÝðÎ6hDÌä\d*­Éé
ÅÓTÔg{	XçÉL\x0010óÒ»Çg7È*R&ìÒß^³içÈ\x0005
'»ç-{¯·Ú­Z!öb<Of|Þx×Û\x0007£Õ\x0013gßëín¯×i\x0014c/\x0006uvÌ°\x0016\x0018ñBm°º\x0003±L©Öê\x000eF£a¯Q8uò«sû\x0006æM­·¸ýÑt±Úê\x000cFãÉdÔ­çÞl\x001a	A½<5æÒzhÞÌN$]¨6;ýÑäs:\x000c;ÕÏ¬\x0012sÏi×ç-*T\x0000ñp\x000c\x0001ó ]\x0002u>«O\x0010'f£y³{CÉ|¹ñÑ\x001b'Óél6{|Èñ(åOñ±à\x000b%JÑæ­Ý\x001b â¯ÙìsÔ©¦ýæûó©Æê¼½àó6E\x0006Ä__3X÷¸ç|Ö\x0019Í\x001b\x0018\x001bl,æóF\x0010CfX°C+;j,æM~¯7»°yÃÇ\x0002'\x0006Ì°\x001a\x0019¿E}\x0016Õ\x0018\x001b\x000b_\x0004Å
1^Ç¨\x0014¾\x001as\x0017\x0012Éî´ÀÂÉ|\x0005\x001b\x000b0osb¬\x001aýf!ìÔÊN~\x0008bW=4oÊÇ'û+°·r·¯¥\x0007T£[Ë\x0004,êSW\x0018\x000bbÞâhÞFhÞñj<º\x001aËóf\x0000ó\x0016Ëjí±X«FäÔÕØ2oÕÖvây5¬ \x001aUcùrºkÞ\x001eàGírâõÕX²7n1op,¶\x0011Ã:cÕ8¡:\x0003d|ÞTø¼-\h\x000b1d\x0006ê
Z\x001fN¦Î0dÆ÷ó¶Rça§òT¢S-Ý\x0005@æ\x0008n\x000b-ìmsÞ6.\x000e\x000fA\x000eý$Ý\x0000Å`p®¥*½eï¼­1·î\x001b".F¹¼¼øcì\x000b
-ª\x000e_4S¬í·MfÏó½DÀaÒ©Ô¿Æ\x000613yâ;£3ÈoºÐîn~«V)¹æsX¿Æ¾¸¤±®d\x001a«/Q¨µ{;çm\x0019\_s\x0011Ew¯\x0008\x0005<MCØÂ
Ù\x0002Þ\x0019ÊVÛýÑ±Xþ\x001cõïé°×aÒ?ÜÉ%¢?ÆÆ]|½\x000b¿
\x0008ºÛ,gão^õY÷p§\x0000Ø $Ì?Â\x0006}f]ÉµÎp\x000e0\x001eò\x0017¼À\x0007ÝVµMF¯\x0000[¯Qý%6ü\x0006ù\x0007k Sí\x000c'1 ?'£~§U/\x0017²ÉhÐë²aØR±Ïeÿ\x00016Ø:èîÉ\x0013/µ\x00062\x0003èéd<ìw?µr\x0011`¿yÝ6\x0013Â¾þ\x0003l¬\x001c2­=«r\x001cÈ\x000cê\x0001¨'#\x000c»^.æRÑ7Ûn2hT·}IapÅªç×Ä{ûð \x0011õ'ÝªW\x0000v\x000cb
÷ÿ\x001e\x001b.´@®u°¯ð`æ\x0015ì\x001eÄ.\x0001ìï\x0005aËþ-6\x0010\x000e\x0010´É{dÐ\x000blðA\x000e\x0007½\x000eí\x0007ØÆ\x00056\x0003Ã&ùDAëÇ\x0007=Ç\x0006q\x0011v\x0015Çv\x0010ØW\x0010N6ö\x0005\x0016ô½É,\x001f\x001fô\x0006v»Q-åÓq­U+e7B\x001cT)Ag¡Î\x0019Î×{?\x0008\x001aÇÆÊ=\x001e-c{\x001c\x0016\x0002Ç&×¥`Ð¼\x001bµÙúiÐ»°Ã~Óò\x0004°åK
¾Æ¤£Ñ\x001bÿy\x0013û=\x0003\x001e§õI·äRä`\x0013AûS\x000fð\x0003±\x000bD$ðê»\x0014i
\x0005}\x000b.ü2èMlpºCìe"\x0007\x001bÚBFÐkØý.
\x0015p)\x0014\x0010Þ
·\x0006w´Ð$!è
lÂ¥À¥æØ¿=&çJ>BI\x000fÇ&\jU\x0001\x0005­4º£Åf¤ ±\x0017
Mf®(h
áþ¤1#î\x0015Zëº\x0002\x001e»ÐýAÐ/1^Ã\x001e\x0010Ø\x001b
ø\x0003Âj¬A\x0018ô'¹AÏ±§»\x0015ðG.5\x000fºô/Þmq©#°ñ m0èÑö gÄókld®[]ê(\x0005\ºÍn
\x001aù=xÀ[ÉÀÞêRG* \x000cúJöhËÖ¶\x0005
^\x0005~Vø'¿ÇÞåRê»ã\x0014ðBçâAoQÒÙt\x0002_Ñét{áh\x0002¹ÉÄ&\
) pEJö\x0007ÍÂÞ¼dAäÞG£V­Ö\x001a­nlì¹K!\x0005ÄÍ\x0015
÷>j\x0018´Xõüxß\x0008\x001a\x0014cÔkUÙt:/ëM²±q+ 2W>V}ÔØmV¦µo¹Í\x0007íJ.\x001e
ø¡X2[,×V°Î½îRlbE\x0001Á`Ô»fàA¯_²@ÌÝz>æsZ-V»Û\x001b$³\x0005\x0002{L\x001aöÀF
IDÈg3i»¡± åZÇFÐXÌïI¿Ýø¨~xÔ?[]\x0000;Øín@\x001aödS\x0001\x001fk.¾\x001b\x001a\²@Ð&ïzÐ³é¨WÏÆ{¹D"UÜ=è­ÎWr±¿Ö±ÁéþæuY\x000cjÏÚ4
Zç\\x000fzú9ü¨¤|fµLÈçñ\x0005"\x001c`?-cwzdcc§{2âwµJ1IÛÍ\x000c¾7yåå A5ú­bÔm¸\x0015rYL&Ã\x0013\x0008çØ\x0001ý^mII¹x­Zð^\x0006uOÐlBç\x000cçë½EÐ30tõìM#å³ÀùD£3\x0000ö\x0015ÀVª!¶'\x0010Ndòäbã.õÑ(çb^F&`í
w£6ûRËAO'ÃrÒû¬\x0012qèT ]\x0014*\x0015`³\x0001ö
ÀÖ>Y\x001e8þ\x0007Ø^»¾<Ý¸tÊé`_+ôÎH¾1¿ÍÂÕÕÐ+°ÿ-xpl&-\x0003ØF\x0003aH.É¨ß®¤6Ï¤^îdFAûSå\x000fâ6;¯G´
b\x0003nÍ%°Í\x0000;\x0014OçJÕz\x000b`\x000fÉp)xü6
\x0011N.`î,4\x0011´+R\x0007­\x0006^Å\x000f´-Æ±_ü¡X*Wª ìÑo±ÑÁ\x0010÷\x0018o\x0005¬}ÌT&O¢¶øS\x0015<èµj,ÿ[MÃ°¯Å²ÛûG£Ùþâ[ÅþÌ°O)\x0001¯wû³·\x0006w´ÐDA£\x0003\x0005VÏØè\x0014^n\x001a\x001d`ó\x0011¶a\x0019û£÷;3ïË\x0019]²$\x000fV\x001aÜfAÐ3t ¬Wc'¶ôVõh0ÙÝ¾7]ü¥\x0002bÝ(ÅÜzùÕ>ãA+AÐEì6»»\x001a»±\x0015*
Äö¾E¡\x0002Ö®³é¸ß,\x001dÒ=»1\x000fZc
d° á§»³\x001a{±õ&\x001bPÀè¹\x001e½`²ºµLÀ¢¾Ù³ÏxÐ\x001c¡Òø\x0012AFu@5L»ª±\x0003\x001bH	Ä~¶¹ÍõØáF§Ùë³RÈÞó	\x0012AK5Ö \x0016ôçxÐÚSmØ,\x000e}§æúS\x0005¢Ó,bó¼ï\x0013\\x000bº7\x001acÕ°£è;æ5l\x001e½f®G\x001c°\x001aõlÐúfû_¶ ?\x0006Ã\x0001ÔÐ\x0003ª±\x0005ñK\x0005\x0005EçîÃ EXÐN¯Ûüf5ö`S\x0017Ø?P@Ü]ðåßþÆ0è+\x0010t ]n¶[\x000c!)3#î\x0005öº\x0002®¸Ô®áF¢\x0013ÄEç»×]¢ Ý\¹V)Ä<\x0007ý:{±W\x00150°¿q©í¢³ó]X£\x001fÌÞX&K\x0004ìZùqÕØ½¢¸ÔòivÈo\x000c\x0016*´6o8\x0016	¸*1÷_g\x001fö\x0002"ú\x000e{vØi¶x
Ô;±òÿìmOP\x0018§0\x0014Ô|	,ucËEäfÍrlËÄ¶²¬Õúÿ¿¡ç \x001aàK°Îi}èþ\x0001k\x000fg÷s\x001d¥m'\x001d½¾ëm\x0013\x0005ÛQÀÍ.µí}\x001eº±\x0004ÍðE©©êrXÙõ½r©\x0003K­°¿ªÄq
·5Â
\x000c\x0006Ìðð\x001fkµýÈE.-Ø¥äüÒº\x001e\x0007Ìõ\x0003IÃÝh¹PB}\x001dA3\N,\x0014Ä,¦\x00138Ø9/¶£³¥K½Ã[ðåa<05I°Íâpý2,Ç±LÂ¼½t)¹Â-y{}ÙWgGÍònu\x000eB£!4\x0015ÇìÇv]Ê
Rò4?ÞÛ£¾¡ÊyÐÐðå\x001c\x000c\x0001b¼È>ìëR+s\x0005)¹µ§ÓÉÕ7[õR6beÅÜ`'Þ
æÚë\x000f5¼è\x0019­FE`£ùWâs©¹jíqÚíÇm\x0015OË\x0012H\x0000\x001b¹¢éºª4¤À¥¶ÌÈÅo®ÅrUe©ºÇÙ²\x0004âQ@h@A\x0014\x001cÏ2I¬-K .6jÀ\x000cI'Ñÿ42+%\x0014
¡¨\x0004î½@*N\x0003.B¬eIèZøÏ÷ù\x0014`\x0000®ì©\x0013
endstream
endobj
80 0 obj
<</BitsPerComponent 8/ColorSpace 132 0 R/Filter/FlateDecode/Height 112/Length 45/Name/X/SMask 79 0 R/Subtype/Image/Type/XObject/Width 180>>stream
HìÁ\x0000\x0000\x0000\x0000Ã ùS\x001fá\x0002U\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000À7\x0001\x0006\x0000NÀ\x0000\x0001
endstream
endobj
81 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceGray/DecodeParms<</BitsPerComponent 8/Colors 1/Columns 166>>/Filter/FlateDecode/Height 132/Length 3290/Name/X/Subtype/Image/Type/XObject/Width 166>>stream
Hì×B"Y\x0014E[r\x0016,%', ID¢A$êüÿ'Ì¹U\x0005h[\x0005\x0014ÎÃÜ~\x0012zsO­UûüùóÿùÿP8'p\x0018\x000c\x0006üûÛI¾;x@&Åb1QÐßÎ³},\x0016ÃÃaCÐÿVÌµ<¾@$HÄ"\x0001ÃúïÄüP"É*R.\x0015óÿ#1qRà9)ã	\x0015*í¥Ád6ô\x001a¹DÀùý¡¯%äáw\x0008	\x0016»Ëë\x000f\x0004¼NN.æýîe.Ç%\x0014OaÊ\x001aÑbsù®C±ÛT:\x0008y,Ú3¸ÌßJù9á\x0019Jh0Û^H¼Ë\x0015Kår©
9õr\x0011ÉøÅ,\x000e \x0012+Õ\x0017zóÓ\x0013\x0008Eo!ácµþÜj·*ù¸×¤ÀÈ+á\x0012æs\x0005$4]9<þh"»/U a·?\x0018\x000e\x0007F1á;zJ\x0002fÖ\x001aÌj­Þdu¸ýÁH"-@Â'H8|y\x001dO&ãQ¯q\x001f÷\x0018\x0015Çø×0[ín_0\x0012Oe
\x000fåÚS³Ó\x001b ÓÙ|>¼tj¹C'\x0013\x001e
TD\x0008f9\x001cOfòE°
	GXÂÅâím1\x001f\x000f¥TÀª>å³é7Ñ×0CB\x001cæ< Òh¶»áGÂ÷÷÷·ÅtÔ«t!Äi,W\x000f"À, qÝ\x0004@\x0018Ì(a3áû?r>î??Üú-Ç¸J,#Ê
æÀMô\x0019Kø=\x0010Eü\x0007\x001dt/íJ&d×hA `ÄMÓ\x001b0N§½ö\x001aÇiölðT¦Ô ]+!!\x000eótº\x0010\x000b9\x000c\x0001ë«c¼\x001eO ¤èL¥3]Á{/\x001c\x0003Wº!\x001eÄíXJ@§SÍE8:t_%+©vo0úÊ'?'Ä¯rÜ×ù8è°ù§*£3\x0018¿+ª\x0004*0u ätØ*ß\x0005m\x0017Hè´§dr2íú6_n41¿De{Þ³×n=\x001fu\x001b\x0014ô£RrEr;«4{pd\x0012\x0012ó\x001e<\x0001«FzfÉ`rÅ
£7Q|ê&ß¢²\x0015\x0012©²	9.ÏéGç\x000f~
£ï¶Ô\x001c!ãÏ	ñH÷Ð+UGy£ç\x0012&îI@Ê)$\x0011q©ÊÇ4Rå\x0011ÐA)\x0019\x001cìÒ\x0015+>CJr!\x0011:Ëq¤­\x000cèìÂ\x0011)<
&ó7²W	è`-CÊg\x001f¥VÕy§«l­78<£n5\x001b>\x0016:è Èæ@ºÒ\x0019ÍÈ¥|[ \x0017xò88\x0018>Fïm©õBîÁÄß\x0018\x0008ýHOå\x001fìÁ¤\x000fJÙ×\x000b½vØÇ \x001cKÉâKµöp¾Ñ\x001fÂ\x0007»KÔ+Mj©Ë:RLÀG¢¶\x00063Õî+)|·c*h×+¥B\x001e\x001b~\x000c\x0017!|LþT¹M\x0012\x001fôzìÔòñ]¯\x0005Øu\x001eá\x001dÉ\x0011ÊõèíC\x0001A³O\x0004æ\x000bTÄã°\x0018ô·"Î\x0019½\x0007¯L¹¾ö[ÕûTØg3¨Ï%\x0002.öëD^jm¡\$>xÌA»QÊ&.Ny&æsh§\x0008á£²\ßÅ\x00079\x001b¿ôÕb:êw\x0018µòS!ícG^W|IÒø`1çp§r>\x0019ò\\x0001E´\x001dás®w'\x001e\x0014j\x0011ºÎÉ¨ßª?db×Ç \x0008ás¦sD\x000bdñ!®\x0013\x0016´ñ°û\)¤"@\x0006(âÑxx-¢Ïê:ç\x0011¢(¸q[/UKèÉÉ`q\x0011>é
i|V9ç\x0004EwÑÃ¤¥uìx-ò%\x001fÉã³\x001a;¢hSäµéé'±UÄ\x0014ðY\x001b;¢¨]/eã¸<E4É\x0013m\x0015Rl«èÝ*Ö¯ ¨zøí¸<é¨ \x0018>ê«`üVñé:1y6\x001es·!¶
rBl\x0015eÒ[ÅVÎÙ\x0018äY\x0003y\x0006h'ÁC~«ØÊ¹&Ï0]òÄk+vÿ<¤àõ­ëÄ)Ê% Oåáåo\x0015¶pìVñÍunÈS~ð±SÝ*¾É¹&O:*\x0008àj\x0011ù­âëk\x0015\x0004äi>´<ñZäù¶\x0016½Ã!wkòô\x001dZ­EpEØ!\x0013ô£\x0010òT\x001dPËZ­o{\x001d2.æp\x0016¤s"h'^\x0002¨\x0016}z01&Æp&3\x0008Jr{C\x0014­äy¸
×"/ªEÓ(økeÐïõ£ñlþF&çz\x00059èþyýÒ\x0015û\ðu±ÓlÔÝÁh2[\x001b;FÑÁ÷7Ìë\x0017öp¾±YÞá&\x0007­Z©P¸/U»Ã×)µ±\x001fXK¯oÖ" a<lÁó\x0015ÆÙZ³÷ÆNöõýM§î/O¼\x0016ù7k\x0011÷K§O\x0004½.?|{l´aìs*c_íoF
!Ï=r\x0012µ(±QÞßf¯½Æ}"à0\x001b\x0016?*T`ìã)yòÄ÷7$Ï}Æ×"çF-yOÍR*h×«\x0015
µÎâºe\x001eê­>yÖö·CÈ¨E\x001bëîûb:êT³\x0011Ay&\x0011«õWP2_~ê\x000cpH}IQ!yæðQY¯×j\x0011B§ÿTLøÌj©Çã¤r­Ñá¦Õ&µ±ÈÓmÝOD-J®j\x00116ïV9\x001d´]ÈD\6ÍáÏ0ö`"[ª·)}]XóÜ]x-rÔ"På¨[ÏG]\x0006\x0007¿Ábs\x0005sµÁæ
'\x000b0vÒò\íoûË¨E\x0011¬\x0016½áó\x001e<?$ý\x0016T}#ääðDRÅÉ\x0011ÝÁØwgüÚµ;Ej\x0011¦Êv%\x0013rèÎE\\x0016ú:ÈÉdq\x0005bêÒê¾Iì*Ï{$O"êÍs³\x0016\x0011ª{J	MüfÈÉbó§rÑæÛGhSí´¿áµÈÕ"èHéë+íÃ\}\x0011ºN\x000eÐ®¼0;<k;Ê\x0013£h±¯×¢9Ì{Ô­å".½\Ï{ùW\x0013Q$ÛO@×¦ß¡yâµÈ\x0011É£u\x0017~4¡ÊS>{óÇâ\x0014ÁØWò\x0004(Ê³U/¡ýÍ²ÃþðQ_A-ê¾Nga»|wc×É­ïÀÇ¾<ýÍÿ±¿ÎIÔ"Xw_ÆcLn\x000ekû\x000bcßKËý¢<×Q-zxî^ú Ê\x0015SåWþ§y\x0017yÂ\x00035Â÷·kª\x0015déõ\­Ýë6Ë ÊË¥*¿øãÃÈ³°§¬<1¯«­×©R£ùTÉÅ<&¥ä3:9÷ç\x000cÉ³^"ä)#-O\x0006*\x001c\x0006w4ûP\x000fû­¸*¿ÿÜ<ã\x0014çÛ®ò<aÂÈµV,IÇ\x00026üÛy\çgyî¸¿Q'\x001a¹XqióÝ>^ñ·y¯>².Ï»]å¥"O \pª¼´Ø\x001dvØùN\x0005Ûªü*çJî`"·<ëòüqìp\x0010S®Ñ]^¨å\x0010òïó^~h)OÁæ\x000bã\x0014Qo<I6O	vÊÎeRtù$_\x0008kòt\x0006bbjó¤(Od\x0017\x000eO \x0014
ø\6ÙëòÔ[=7·{ÉÓ¨YRôÃÿÇæp8ljûÓJZ£Ý\x0017Iï&Ï\x0006øï\x0006äSôw»0\x0018\x000c&\x0013Ö\x001c-'PdvQçZóaûäG(NðC)ãÉ³\x0000û\x001b\§Tø«w>ß5O*û\x001b¼33±Ý TÌ\x000e1\x000fÒ<+Û Ó úýe\x001d;PÎeó\ÊÒþ\x0006òl×©\x001b\x0007¬2_UÛCåÜ'¶¿)Q4ì4É\x0000Z\x000b|Aï\x0011s]!$OûÛä¥S/ÄÜ\x0006(;L\x0006])7åé¤ï«ÔÆ>\x000c[éEýå6sÈ+y\x0002Eq <\x0017³×n-\x001b²i¥|zS®Q¤·y©É\x0013.sÜoä#\x000béÏÍqïK´&G Ja#RíÇHù!O´¿¡æI²@Ê×^-{cÓHi~.W9"¢yÞßÞ\x0017Óv9\x001d0«\x0010=ÿr_öM\x0005DQ\x001cVXee#KB¤(/£íe°%M\x0011ÆËP¾ÿWèÜmé.mõÏÚ;ý>Á3{ö÷Üs44(åú<¥B>\x001eØ²µz|\x00161\x0015+\x0008ÈSüESéS>\§¡âZZ}s}.Ï¨$Ïæc¾\x0007O\x0004ÝZ¾ßqbòüe\x00059=\x001eÈU
\ÆÄVã\x000c_þA ô~û±=eC«\x0005S\x0013g^]¨:Ý§»g\x0015²\Â¯  Ï³Êý\x0006»\x0006ªÎÍysAÁWNùµ¸¼AUy¢ê¼6ÊP\x001dVëMCó³E\x000eVçÒ
"U§Y¹Ô¡:8æòýË\x0013©²ßª\x0015³1\x0010úÊ«sªÜo\x00136Ë1¼:·ä¾Ö¡:JÎïï7ÈÛdØ{®^¥\x000f}Mêà\x000b÷[Ul÷\x0006£ñd.Z1\x0017ßuëV\x001dSq¿!y\x0002çp4\x001côZu¡\x000cy\x001dúU\x0007ÇÄä\x0000yVêÍv§Ûi??
|ê\x0010T©gu°Ìï7o0Ìð¥J­!õûÒE:\x001a bÞræòä`ìYþ¦$WùÓH¥­0oB(¿ä¹í\x000fÅél.IÅÃ~\x0016ý¤|J<]\x001eÿÞA4\x0016ww¶hÊLÌ¼?#ßova½>óyÜÎM+i\x0006yìf«mv2¶S\x0016\x0013Qã\x0005Æ\x000eßsÃBQÕ²a6\x0012	i9&\x00111	iæ.\F)kRô¦øÿù\x0010`\x0000\x0010ý¬ã
endstream
endobj
82 0 obj
<</BitsPerComponent 8/ColorSpace 132 0 R/Filter/FlateDecode/Height 132/Length 46/Name/X/SMask 81 0 R/Subtype/Image/Type/XObject/Width 166>>stream
HìÁ\x0001\x0001\x0000\x0000\x0000 ÿ¯nH@\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000|\x0000\x0003\x0000U\x0000\x0001
endstream
endobj
83 0 obj
<</Contents 84 0 R/CropBox[0.0 0.0 540.0 780.0]/Group 480 0 R/MediaBox[0.0 0.0 540.0 780.0]/Parent 457 0 R/Resources<</ColorSpace<</CS0 132 0 R>>/ExtGState<</GS0 475 0 R>>/Font<</TT0 479 0 R/TT1 135 0 R>>/XObject<</Im0 85 0 R/Im1 86 0 R/Im2 88 0 R/Im3 90 0 R/Im4 92 0 R/Im5 94 0 R/Im6 96 0 R/Im7 98 0 R>>>>/Rotate 0/StructParents 6/Tabs/S/Type/Page>>
endobj
84 0 obj
<</Filter/FlateDecode/Length 2061>>stream
HWÙn\x001dÇ\x0011}¯èG^\x0003Óì}\x0001\x000c\x0003±¤\x0018\x000e` ä!ñ\x0003AQ\x0002
R¶®Ä8È×çªî¹Ct`K\x0000§×ZO®{þç÷÷Çkóõ×ç?¼øþ¥ñæo¾}ùÂ,\x001f\x0017ïm-&ºfKì&ûbSíf
5ÛÁñzùùsçß½qæý§eèÍUãð\x001cìµ'CY¹ã_41ÚX9«»åüû;g^þ¼¼Æg]+ÆÙ=þf(ÿÛwK°8ø+ìúÉ,\x001e«0¨[#¦TÛhÈåÕ\x000f°ùü\x000bgÂÎd}1¥GÛúÒÔ\x0015¬>ëIÏqóÄÃüêàI!Ü4É#4Í¹\òpÅOW|¥ãÚÉÒ²7õÛåü¯¡i\x001aú8\x0004Ç÷ËùÅC\x0000.Þ-+ö\x001dFWFFÉ\üjB´\x0018¬b§\x000ck°±CYõÕ\x0006pènùçÙ«Ã\x001a\x0010¬³ÿ\x001cVÏï/üVsö3×ñ=\x001e\x0018Ü³ÏX6g×\x0014¬ÛK\x001dÛO5>:aÞ\x000e1ã3\x000fÃ¹?µ\êöQ/ß\q\x0019Çnöû8þÆl:>\x001d~¼øëÕÅ£ä]r]"J\x0010\x0012Ra×Ö¹ö(·²\x001d¾\x001a$·<æ5Õ"\x0006ãÖ\x000f	@}\x001c©
3µT×±i\x0002p\x001e\x0002\x0010\x0008$5gÓ\x0013º¸K\x001cÅ¢º\x001c2µ\x001aÁ­\x0014 ¬XTóuâ(n8rÅføúá'6è·^\{÷ÕShj32Þ¼WÈ\x0004B\x0006\x0003ï\x0018m/\x0018\x001dúì¸\x0006«\x001a\x000b¢EÌß4 |Üb¶:³+XùIö»ýsÐ	\x0006EÁ\x000fk¢q~.\x0002\x000c7ãø\x0011hAYíO\x0018I=M´Ø\x0019(\x000e\x001c¿]Süã\x001c½x\x001a\x0012§¡\x000fõí\x001c5EG
·ãä¥£\x0007wÛv÷úèÊïå°m\x0016 Ä5ÐÈ¯`Û»ÃZl\x0010O\x0012õ\x001c\x0007Àï\x0006²/ñlóùÁË£\x001e	ùëßD»ß\x0011sÈdRb£4ÛY+¹ã	\x000cr\x0000oÊe<FÜ¡DD\x000eÇ¡\x001aPR^÷\x0003é\x0004øP\x0010ý\x0004¢"dÿÊÅ'ôÉ.Ð\x001cºèÃ)jï¥\x001b\x0011Ã\x0002@¼rm(\x001crS_~þ\x0019\x0000\x0007Ü,*¶$­ôâø¡	ÊªO\x0017\x0002÷wVB\x0000y¶\x0002.(àv_\x0010\x000c©\x0017\x0004A8¡fbåã¨ûg\x0010?±t\x001c\x000bÿ
9nÐ\x0016ÔT\x001b%3\x0017o¡ç
¯\x0017ìËR\x0012sçø:ÃØIé\x0007µ²ªÄY0\x0014{û°iù0\x000bîn[\x001a0;<{tåuQO!x®|.Ç¹iæýQéÜI\x0002$øÑV°¸ÀÔx¸øéyüïè~B­ToËlèì\x0008¤\x0012ô
 Ì\x0015Àa¿Ñ\x0006Ð\x0002íãÂK9ábs\x0013ÇObï#\x001e_(¦\x0014\x0001«Bö®ò6pçné0¥\x0019`\x0006Þ.+ZIÝz<\x000f\Èx\x0000{¼\x0013Õ\x001bNKh&\x0003m±\x001a\x001e\x0011ÓH«ÍÕ²z>+Å bäu4$¹g\x0003Ø'0?Ù2à:¦x\x00190èI DPq= ÷ \x0004
É4\x0007×ñV\x0001á(!L
ºu9³\x001d+µÖ!pÖÇ\x001bj3ì¹âÍñâ$Xâ*ÃAÅ-lýh\x0011@®ó¯kú¶^±._?Ýù:\x0013*\x000c\x0003.«ô\x0000/d0xß*«Û±$\x001f1\x000cw½¾¢B08Å¬éÓÏ\;Ä\x0008\x000f¹ô\x0005kÞëÐ~æIkèdM.ÈQ
»Ì#ª)\x0001ÏI°ÄP*ÑM\x000b1\x0007\x0014ReßX\x000by\x000fÜS8sæøüB\x001fºá¥°KF{j}Ì¸Y°\x0002Ap\x001f{
{ÞÆè3?°³\x0011.ÐEº%xáv\x0001yuòcÌx×=\x0017:\x0000Rb\x0015@b?!é+ú2\x000bÇ³L=ù¡7h6 \x0011,\x0004ÑXól;\x0011	\x0001´Mô\x0012eÀæÓ"4\x001e=uûÿyo§¼3sà>d9ó¯Æ<UÐEîPLø\x0013mOyäÛ5Ï¨A<ïâÍ³×æy{°O½óà~\x0014j\x0005À©\x0010nU\x000cõÿt@q}¸awÂ\x0017<V¡5rïýñ7_ë°ûåñ\x0007XO©!Ø`Æ"\x000f$:d\x0019!AÄkÕq\x0010,]-2Acf^!Ã³\x0016Ç@ rZß]Ø\x000bÚ)J5«`R¢\x0004H\x0004Úî\x0016è\x0007_8<6¤\x00046ÌÙ$=×À\x001f¢
0$P\x0015h¾ÅõmB¸ÙÓtÝî\x0012×dU^nâc\x0011
>Õã§Nô|òD«Æ\x0012§\x0000x3É¶Én`·T¶\x0019Îu=+s8ÅQêÐ\x000e;| \x001d\x0012ºT\x0015äaÖ\x0011t£a\x0008lýè"#«ìê\x0018~\x0007"SëßÀÚQÇPZµfe
\x0007"g\x0001å-è\x000f&HÇ6Þ\x0004ðÂòNÑ°HM¨2ª\x0008\x0018ó§fõðGØsiKópUïTy\x001dª
Æ§GÒÃñ\x000eJs
ç2á0FÓ0N§!tuµ¤½Ü$ª+Þ¯8í\x0008BJÑªÁ\x0019 2rÀXØù¤±ÒLø\x0016¼ü,²m|µ¸m¼Î
ÞX·+*»Îk7.\x0002Ù>bkÜEi¥\x0007\x001dF7\x0019\x0006`TëSÓ\x0007¤E4fòsHË/¸\x0010´î\x0007\x0004ÀÚ}V\x000b&9õéNà°=ÍâÜâ%é&1Ï)Õ\x0015±Âá¬
ì3ñr\x00082ó\x0004\x0008ê$ðGA!4Ò´JP¡h\x001eT× ±¥Ë9²YCÆ(Ò\x0007TB7*øeq·ø©ÛepÔ\\x001d\x0018\x0013Òn¾úíòÉÆBÒéÊH\x001d[.¿\x0015%fMøQ3	×r!9Nß¢v=Ã¹è\x001e­Ê2
@î9Yµê\x001e_¤
J +·\x0015;&¹yæ\x0018w³`·+C6\x0013(.&ndY\x0003<&3øcªIâTóiT\x0015&®YU#\x0018qãÅ\x0007ùØ?ç¯ÿ	0\x0000ÛÞ
>
endstream
endobj
85 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceRGB/DecodeParms<</BitsPerComponent 8/Colors 3/Columns 964>>/Filter/FlateDecode/Height 533/Length 59361/Name/X/Subtype/Image/Type/XObject/Width 964>>stream
HìÖ[PT÷\x0001Çñ³ë¥í¤­\x001aÛIfÚ´\x000fvÒö!íL./}èKÇ¶Ó´uAQ\x0012Ä Ü¼¡ D\x0005ÈM.\x0001û®Èe¹D\x0002F¼ (ë®8b!º{Î¡g\x0017\x0017Iªí2sØSã÷;YeÀÃÿìoþs¿\x000f\x0000ÀL¼\x0013\x0018§ù¯\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000àÿß\x0004\x0011\x0011\x0011=\x001d½ùóî\x0005!fòS¥ùÈ\x0001<@ëcMDDD\x001eÊ3CzjNk>r\x0000\x000fÐúX\x0013\x0011\x0011òØ¤ùÈ\x0001<@ëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨ÎÍÓ'Ë²óafÍü\x0012\x0011\x0011º±¥\x0001Õ¹\x0000\x001fì[ÙibÚóé&¦}×ñTv]ëæ8v]Á&""R;÷gðÐMûè¸øH9'¾bK\x0003SÜ<}²+»(Úí
Éù(Ú\x001cO\x001clNöi$Ù1'¯rü\x000f¢¨¼*»¾-O{>ÅùV×\x0005DDD¤jîoiUh>r\x0000\x000fpóô9ç­,KÒÎ¬<=åËG¾Çõ¨&¦¿è4u»ºuHÒ¤oä|Qæ\x000eCO{li@un>×½µµ¯ÆÔ]kî1ÕöÔ>F]]oYY×Áaç\x0007óA\x0014ÇÎ\x001b©1Ö6êGk\x001b\x001e29\x001fkêF\x001alwÇù¤#"÷SVòí;ã×nttöW5ÝÓ\x0014¶§f]xÏÆBï ã@aUp_hÑ]å±©õÆ²\x0013ÇÚ.u÷\x000f}ùÕ]´kýë\x0013y:¶4 :7OäÃòä7¿Î\x0011\x0018A\x0017½\x0010÷u{¯'	B´¿ýØØ]Q¹FÙÒv»²Òó.	B¯ð^aÞß'\x0008Ýß}þî\x0017Ã%Ê\x0002Å[	\x0011=ù)w\x0015»(^\x001dúÒüÑù¸í½C
½C×\x0006FVmª
©\x000bÝmÚ\x0018U\x0013\x0018Q½vkOH×ú·Ö\x0015¼³±("¶ÆXv²£s`ìÖ¸²ÆµþS<\x0017[\x001aP§OùØr¬bY~íµz}ÒÜ¹\x001fèõ©z}Ú×¥Î¡|÷·¿Ë·ÛEå"iò\x001ae\x001bËò°ÉÜ÷£\x000cÎYhÕ?kÕ/r>ºÌYlÕÿ ÿÇ?»7|C~ðfõ^BDOpÊMÂf³Y\x0007?¯n<\x0017\x0011kZ\x001dT´:äÐ\x001d¦Ô£\x0019\x0007O\x001bJ?)ª¼PXÙi(û4çP{¦¡-5ëD|ÚGÑñu[£ª\x0003ÂJß\x000e.|smÁÒµùþa%û\x000b}òÙÀ­Ûã27\x001dz:bK\x0003ªsóôM.\åßW_1\x0008B2\x0005!Y\x0010R¦Q^IÑëÓuºø¦\x000f»Kì6ÇvæXÔ¶þ? Ì³è\x0016Y\x0005\x0016aáCWé[üÂ]eK;'8kDôÈÃÍ±;§Úÿõ~JÝÊ`£ïMÙ%\x001dÍ-½µÍ=õ]%Õç¥çr
OgæLÍjMü %v_ãî8sdLÍ¶\x0015\x001bÂ\x000fùm6z\x0007å/õÏýûÚ¼àÈÒòÚ3ÖÁaQäÎCßþØÒêÜ<}®-=ñê+FAHÔëÓ¾1¤uºdÎñ¢NØuqHyÿä\x0007ä\x001cÒh\x0017%éêr~AgÑ?k\x0011\x0016X\x000fé\x0016Ygú\x0017¿poøÆÄ-={7\x0012"zRSn&×®Ú×\x0015{\x0007\x0015FÄ5\x0016¯ÿ¸ïÃã\x0003Ê®PVtMçÁò¼â3\x0007\x000c'ÓrZö\x001fÝÚ\x001cÐ°c)<ªrsdIð¶¢u
¾ÁÙ«ü3û¥/óËúo¾W@AbfcçEËýû÷µþ\x0013f7¶4 :7OßßÒ:]ª2§\x0005!IÐ¥éõq&Óeå6]v%Ùm]W¯õ¬ö³
eÎb\x000b[f$IW®\x000eg\x0018z\x0007\x001f\³µ<9¿ÍÜÜ×tâ¹¥¯ªñrùÅÕ\x0017\x000c¥\x001d¹Emù§R³'¤7ïIn¯©Þ¶³|ÓöâÀPÃ»\x001bòß\x000e8°Ò/cOò\x001b+\x0013ÿôæÞ%^Éoøf/]»=¦²íl÷øø=\x001b\x0010}{cK\x0003ªsóô=fK§º\x001e\x0013{>óÅ\x0017s\x0016üPù2Úky¥$v»sKKÎ\x0007Qü|ôæ\x0017U5}ó¾oÕ-´°¥h&)·\x0001ëõ}ûx\x0005\x001a\x0003#«sK/4\x001e¿ÒÐ:PÝÔSÑp¹Ô|±¨òÓüö,ãéôÜÖäý\x001fÇ¥µìNjØ\x0011k
®ÚòÞá°Âõ\x000c~y>þûWø¦-[ò·\x0012þ¸4ö\x000fÝýú\x001d¯ÿy×ióÍ
yïÐ±3]÷m6­ÿ\¢Ù-
¨ÎÍÓ÷-=9¤\x0013^úUAXxÓêU¥FcguUWvfÛ[w&\x001c8V±cOoß\x0018éýé/,Â÷,ñÌ&"·Rî?×®¤d7¯\x00080ìª1V}ÖØj57÷U\x001d¹TV×YTqNYÑyÅí\x0007
N¥eµ&¥·Ä&\x001f¯|¿zÛÎM\x0011¶þÝ2\x0001júÊãøBµ»3«­vvvgwVI ZºÓU@µ.\x0016/\x0014<"TA\x0004< $á\x0008( \x0002\x0002\x00009 á#rz \ È!\x0006DCP\µ¢róÿ'ìË\x0001R¯MgÄtÞ'ßyóþ/ÿþ/oæ÷Þ'ÍätÿK\x0003{=ÓÒ&â»maßZ\x0006X\x0004®ø§ÿ\x00123¯¥fts\x001bµS¢{@öí¶n\x000cÃ4ý§!\x0019\x0001D¤6\x0006ïÒ¸äÀÀ¨!*Vß»]:æOÿæÛLÇ½Å\x0015"7òY\x001a­,!¾~l\x0014´\x001cÐ\x0019\x001bÃPôYV~\x0007òQ·Î<12\x0017º4\x0004\x0002Q\x0005°<ï\x001fH\x0012\µwÏp\x000f(N+\x0012»r¿¸BTPv7»Tx®âvéùô2\x000e¯Å»ÄàVE]\x00088{$¤È;0â+póJw!ó\x001d÷óì÷qwîÙº+rãÎps«\x0010³MÇ¾\x000bøÇ\x001a¿%¦¾_\x0018{é\x0013iÆÞëlØÖûýÃ\x000b;»\x001e\x001dLÓ\x001d\x0002ùÿ}ózt\x001a¼\x0005¼Kã\x0003\x0003£¨X}¯\xJîÒl`Ñ
ÿyÂìO\x0018^ôVaï	Fí_ÿ\x0012/@\x0001JPIO±\x0008Ò­;_Ì\x0015#¾ÎgbK/\x001cííPº4i\x0008\x0004"ÛyFGÇÎ7;Ñ2\é¹I9gª;Ê;òÏÞÉ)\x0015¦äÜ¼ÑØù¬ïy{ûÝÂ\x0008f~\x0008ã\@XoP§.~êt¿Û%ÎÖ½Ãiù}Åö°µ!«6\x0004­4\x000fXö
}ñ*/\x00037èi`ä­O -^E_ÿCµ3\ÞÛ÷\x0002Ã0M/\x0000\x0004¢Ýh\r``Ô\x0010\x0015Ë\x0001hL¥$\x0012pi\x000eGîÒ 2©3khÀGÈÏ>e^¿ÞÕv§'*òò£?\x0007V\x000c´x°§§kË\x0007ÎûËLºÙb\x001dàÏs»§GçÓnä÷ó\x0016<tiÉ\x000c6\x0004\x0002Ñ\x0016À\x0016Òv÷'Ïc§w3ck*î\x0015\hÏ=Ó*(lIËkO½zíÆ½ÁÁ\x0011p[O8!Qàw,Ûçh\x001eÅOpÈ3Ýäx0ÁÞ9ÎfOÕ®È;ÃÌ­BVo
6¶\x0008üz­ÿRSß/<ñD\x001aèm@òRdá
êWkX9ñm\x000f¤¯n\x0019\x001e\x0019Ñô\x0002@ ÚÆ%\x0007\x0006F
Q±\x001cKË´X:ab®«\x001b=k\x0016WO­§Ëùøc\x001ekÑâD
¥ÌØ8#,¢vóæ\\x0003øäF©Dg\x001fP|;\x0010¤\x000bù]\x0017ò\x0007±î|Eº'#ëë}.Ö#þ#~´÷é\x0014\x0018xv&\x001b\x0002h\x0007CCC±)vÒ\x0002\x0019\x0017sÏÝË?7»Dqº9%«!1½.WuézûÀà0¢@§\x000e\x0007&xÐ3\x000fÒÒö¹¥8¸òl¸Û÷°¶|ÂbûñµVÇL7\x0004\x0012Ì\x000fÿ}Ï&ÀHxM4¸Ä\x0011h\x000bVM,Cw8'Q\x0002óîw?À½\x0008\x0002ù\x001fÐ¸äÀÀ¨!*\x00038§á\x0002§^²$	AB\x0010$|2\x0011 5+\x001atfÂA°E\x0012Úd`¨\x0014E?fñDsæý|Ôèü oM'ôæ
?ù\x0019<(ÅdÚ>µ
@´\x0001°{Ü¸)r¡g;ûæ%å4åm\x0013\x0014µ¤å6$eÞà¥Öpù×Âc.V^j\x001d\x0018\x0018Æ\x0000\x0012Éðð æBNØ{¿Û9ÁÖmmÇÜd\x0013¹n[ØjË`ãõ\x0001Ë×\x001e^jæc¸'QñDÚ¤E{Nz5
G ê\x0013<\x000cIäÍ»c·;§

n¡^\x0006\x0008DÑ¸äÀÀ¨!*T$;§5ÕÀá4²Ø
pXMQÌz0È`Ögeµ\x0002\x0006÷c(*b²\x0007$Rp\x0014
:{¹'²\x0012\x0014yöË<eì<>88!U¾k&\x001b\x0002|èÍcppXeç\x0011Ì©\x0014\x0014ÞÎ<}+%«ádúõØäË1¼j\x0006·òhxiYÅ­\x0003Ã\x0012\x0004Ù´´¸¸Ìñ@Ì.§ØíamµelØ\x0011nn\x0015jº)°.ðëÕ¾_øà¼p$\x001aÞÈ\x0013Ä\x0008"Ói<Ñ\x000bG áI\x0014\x001c\x0002Ú\x0005+Ü[\x001cµvNu?ÓÕó\x0004E1M/\x0006\x0004¢­h\r``Ô\x0010\x0015Ë\x0001\x0018îÜ¨U¹\x0019iÊ{å·\x0003þ\x0015'U~^\x001f\x0014ìI«5\x001f(Þ\x0010Èo\x000fP×Â;bw¿\Wï<^F]z~c² ZËI¼\x0012\x0015W\x0015Á*?Î,£\x001f-8SÖøâå\x0010Ðh`¼À¨kjê\x001c\\x0018VvM6aë¬W[\x0006¬÷_¹Öï+3ú"c\x001aHÕ'P\x0017®\x0004­'\x0004,Z®Ó2¦á\x0008T`Ñx¹Kã\x001e@ª7ÚóvîK-)o\x001e\x001e\x0019Óôb@ ÚÆ%\x0007\x0006F
Qµ\x001e¤JeÅPpf½/
VJ®Ü|eD"EÑÿ\x001e\x0015¿U¦\x0015³Ôæ×t\x001a\x0002üÆ\x0000b,(¬µw?u$â\x0002?«.1£6.ùZ\x000cïJ$·êxÔ ð3\x0001¡E\x0014º ¨´¾ÿÅ\x0010IPLæÒ·ÈQ~Gü}ò½ý\x0013=\x000fó<|â\x000fyÅí§q]i\x001cG·è-v!\x0004soC ÍD\x001api<#\x0000¦àH\x001eröÀ¨\x000b»\x001bm\x000cµvL
b>í{©éÅ@´\x0015K\x000e\x000c\x001a¢b9HßÎ»Æg
0ñññ©Y½knï34p\x0008D\x000b\x0018\x0018\x001c
eßMÉ½\x001cªÃ¿\x0012\x0015w)U\x0019Ì8\x001f\x0018Vâ\x001btÚÛ?×Õ#5¿¨¶¿PæÒ(\x0006êº®¾9ô\x0004_ØzïáÃÇ<\x0002È:?Ë.\x001f=\x0012{êê[øivÎ¡ËL)@¤ñ\x0004,JV¶ú+ÉKL¼­\x001ch;¢4½\x0018\x0010¶¢qÉQCT,)\x000bÅäH$I#\x0005ýé#¯õ\x0001Sâ:5òf\x001f¢(ðdÐNÑ\x0014oÁ/÷÷÷


\x0011Åï+æ0õº©ÙN\x001f>1èÒ\x0010È\x0007¸ç»î\x0001z^4ï2ëäeFlEXô \x0013ç\x0016ù\x0004æSý²Ý}2÷¸ÌÊ¿ú¼@îÒ²­£¡±e¿\x0007³¡Y4Ê*^^ô©=A2	75·P|¢õ	\x0014\x001c0j"\x0015G¢àd.­\x000cÐéõ¶l\x001b×ò&M/\x0006\x0004¢­h\r``Ô_U\x0014Ó\x0015TÑsäÍþû/ßj¶ïr]\x000cD"CCÃÄÄÄéÓRô÷ÿ\x0005\x0008\x0004òÁÒ,ìÞK\x0013Ð\x0002¢¸\x0015'Ø\x0017Cg\x0003ÃKü\x000b<\x0003²Éô\x0003Ô4gd\x001b\x0007vzvußs¹Kc2¾}»ÕÂÊÏ7$£MÔ=<2Êú\x0015Ó.eFÝÞ~Ïq>\x0011¸4\x0010i\x000fÐ*C¢üm9ÙtkÄv§\x0014vR¥¦\x0017\x0003\x0002ÑV4.900jå ¤¹¹¹ªªêÁ\x0007 ¯PÖ\x000e0ÒÞÞ\x000eÎ¦ÑÑÑêêj¡P\x0008¾\x001d\x001f\x001f¯©©\x0001}}}
Ý\x001d\x001bû\x000f»e\x001e\x0013Uq\x0004ìDE\x000cà6LRÅ­3¢\x0002UE!P,²4Ú ¥Q\x001aJ6\x0019A\x000b(j¥XlÐfq°Ð,Ê4.8¸ ±Ûep\x001c\x0014lhLì6%à®ìàBÙa¾ª\x0017k ç\x001f2QJûåäæ¼ï{ÞÜwo¯\¹\x000eU*×®]kllÄ\x0014Õ¹²²2==ýÌ3\x0014îÞ¾}û\x001fja	*ëêê£CGG\x0007Ú^½zõÜ¹sp\x0014
\x0005ê[[[q#\Ö××www\x000f«q\x001a>¨\x001b~Z}úô©æE>ÖèCèê?
>,Ûy&=³vçîêÄ*YÒ	aüÑHé÷[\x0005%!Û7\x0017ø|½çàáK]}jVmùææ\x00167¸/VI~¬ûùÙó.åÐ\x0010~2( B#p5~=çk~`{Ì\x0011,\x0011h-^`#´ñØÅÝR\x001azJÛ\x001fh¢JëCÄ8Ä\x0018·ú0R3ÅÒÑÑáp8êÃHÙßßO§Óáøûûc\x0016ÜÓÓ\x0013ygg§\x0011.Õ4\x000eÊÅ¥\x0003ò\x0001}}}+++ª9ÇÓy/WW×çÏëüàçååt\x0004\x0002\x0001:D"cjjZ[[KÑrDDÄÈâÂÂBCê³õcü4>j~¼Ã.&W%§UÇï<%ÝñwüÈvqé_£J"
üCó6\x0006g{p¿ý®ô\x0002XZù¥Z}dæ\x0005h/¿´´¬êõÿjø¥ùâÎÝ¶»g/ºT\x0014­þ¡aìê|\x0019\x0012bÁRS4\x0015Ñ`i\x000bf+Zê\x001cÏ
+áÇ\x001eÕöÇ "¨Ò:ä 1\x000e1ÆíC
ç\x000eFGGGK«ªªàïÝ»\x0017ù¤I\x0000Ì}üø1r___ä]]]sçÎÅ¬®®n}}=\x001cÐ5øyÕªUX888hhhhkk\x000b¿¡¡\x0001e^^^.]rww766noo/((
\x000e\x000eFCÜ4..N,\x0016cU~~>\x001c@rnnnFFF]]\x001d:$$$ÀDMrr2ngffJøQQQðãããQy÷î]êE\x0008K\x0013\x0011}â:}ñg^ôaÑ
yÒ	QBy´ìHDÌßBùß\x0005n=°)$\x001báã¿ÏÉ;é@ñ¹½*VªYº¹³FJgèvÒÏW\x0008h¶Ñ6\x001eq«ýÓýÃ³\x0003ùy\x0001Û²2\x000bN\x0002§©
¦SîL+´dFÒ\x0018\x0002 4)ÄHg-Xb\x001aCücÜº°¢`A¶?\x0006\x0011ÑDÖ!\x0004q1n\x0007
KÛÛÛëéé\x0001L&ØxÎ9S§N\x0005	óx<¥ûøøP,mbb\x0002`\x0006Í:99¡	ê\x0001ºnnn\x001d\x0018\x0018>}ºµµ5òêêj¬Ëå¨yóæMGGæ¾ _LíÞ½[ãá455|¶ÄÄD
\x0002È[[[áóù|ä½½½#5#\x0011\x0011Ñ'«5-¼È#Ñòò\x0018yÙvIéÖèC!Û\x0002¶äm\x000cÌòõßã½!ÝÆpË.8ýâeÏ»Q,-£3E\x0016,\x0005[\x0002*o#ü|Y´éR¾é2þ¬ÅáÖn¢¦¿{§âh,Á¹ÿ¥]\x0014XÆ\x0012Ñb\x000b¦ÆRÅ|¦x¡C<wKQ\x0000ÿ¶?\x0006\x0011ÑDÖ!\x0004q1n\x0007¥¬X±bÞ¼y\x0011\x0011\x0011`T\x000eC10\x0008ÙÏÏ\x000f³\x001aFÞÓÓóÙgy{{\x0007\x0004\x0004À¼xñ": \x0001Kcvpp\x0010,mkk\x001cðl``©ÈÈH
¤JåÛ·o®_¿\x000e\x001f¨¼¯¯\x000f\x0003G$\x0012R\x0000³¬¬¬¦¦fæÌè\x000cðSRR\x001f?\x0003t4\x0011ÑDPUMK\x0000ÿh¸lèàÈâ ð\x0002ÿÐý\x001b6g~å·Çs}ëWß:®Þ¹Ä^²wÿÉç/»G³´ÎP±4@ZEÔª\x0011!úh\x0001#ÆÊE|ë§_)~§TbÌ>pÌ\x001dEc
év@h	(Ú%1·,°\x0013/t\x0004K\x0017ã1´ý1&ª´\x000e9$HCq;hXÚÆÆÆÄÄ\x0004Ä;{öl`*.ÛÚÚ\x0000G³4(\x0017,íåå¥P(ôôô/_\x000e\x0007««ëð{f0\x0018TÿS§NQ



ËËËá¥1Ö××ÃLJJ¢`ÌÊÊÒ\x0019!Ü\x0011f\\Æ<yr^^\x001eÕ6**Jã\x001b\x0019\x0019á\x0015¨\x0017!8MDôëtmK@äáÐ¨!Û\x000byaù³×\x0006dxoÜ½j]*gM\x0012Ûã\x001b\x001b·Dµ 5«âÙ\x000b°4¸Xù_fªY)FÐ\x0018B\x001a3°1³^ê*nhºG\x0015c\x0011þ\x0007Ùùåì\x0005\x0000oºDÍÒ\x0012n'3·.âÄsÃJ6\x000b\x0008K\x0013\x0011ýÒ:ä 1\x000e1Æí aiÐï)SdffN6íüùóÝÝÝ U\x001e7<¥{zzPÉf³Áß·o±±1Ã\x0019\x001eÍÒ\x00146?yòD.ëêêbU{{;u»,ýêÕ+999pRSSkjj.\¸Ðßß\x000f3!!\x0001fll¬¥¥å¬Y³úúúp¶\x000e¿gé¢¢"\x0014_¾|2	H\x0013\x0011}ú:÷Ã\x001d^ä÷\x0001á_ìß°9ËÇo×útW\x0014/w1W%XqäK\x001ce´Ú¾+óÄïXÚi
(Z¨¢h¦Æ\x0001HÓ\x0002:ÂN`f\x001dõ\x0017\x0017Ñ­¦{¨W³´jT³4x[B±4]
Òtvì\x0002¶tÛ\x000enØÁpi¹¶?\x0006\x0011ÑDÖ!\x0004q1n\x0007¥1~ÁÀ¯_¿Æ1¤P(0õàÁ\x0003¥1«aiä\x0014K;88`aGGÇ\x00193\x0000Òúúúîîî\x001d\x0018\x0018@\x001f&Ií£G¨\x001b%''£ÃÙ³g©Ëß±4sssá466|¶ÄÄD¸;\x0019IPP\x0010åS,ÝÙÙ9²xà4\x0011Ñ'¯Ëu¿\x0004F\x001fÞ\x0014Z°Î?cõÆtu)Îkv²=¿±qÙñgGÙB¶\x0018ñ¥#YZ\x0005Æ?5·pÖHi\x000c¡*@Ñ,P4Æ\x00185KÇ¥ºo5ßSfiK¥Yb\x001a@\x001dkn\x001fk¾Rnf/[æ½\x001bV*ÛuRÛ\x001fh¢JëCÄ8Ä\x0018·¥Y,\x0011°Vã·µµééé\x0005\x0006\x0006R,|íÚµÈ{{{
\x000c\x000c)p¥ YWW×ÛÛ\x001bÎàà è\x001ad¼¶¶ÖÄÄ\x0004\x0005 d___Ý¼yj\x000eFCL!×°4\x001cÀseeå±cÇ)yãÆ
¬rqqA\x0007@5r>\x000f?++«¢¢¢¼¼\x001cØO½\x0008ô1~\x001aDDD\x001fJ
M÷·Ë×æ¹1ÍÕ7Ùqu\x0012Ë=asÜb{ùBÎ\x0012-dKL­ø#XZ}­fi\x0019\x0001x\x0016¢éjÆhÁ±`	ç[\x000b¬\%
`i¥ò=Kÿ\x0006^´RHcIèl)-£ÙË\x0001Ò4§x³±öë36\x001dÊ,¨ÕöÇ "¨Ò:ä 1\x000e1ÆíC
ç\x000eÅ\x0017T)¬\x001d\x001a\x001aÂxÿþ}8\.\x0017³\x000f\x001f>Dîææ¼§§\x0007¹
jpráÒÌÌ\x000c\x0013fÿÃ~ÇDeaÜ5Q£Ñø\x0017ft ^¡ØNkÄ*@ª(°»\x00077l±µív\x0018q¡A[d¢\x000bA\x0007\x001b²¨ÑRÅb1#¨M\x0001±Q\x0010\x0018l\x0018\x0014\x0008. h+ÐT\x0015\x0014ÎWïêK\x0005Zqz¨ar¿Ü{Î¹Ë{É}÷÷ºººàÏ;\x0017~nn.¸zÔ[\x0001§±\x0016&Gª´´\x0014\x0011©T
\x001føöÀ\x0003£\x000cäíí ¯¯/|\x0014c\x0015\x0015\x0015ðMLLPïééiX|âÄ	\x0014mÿê_\x000c**ª_Qÿh|â\x001d¹ÎýäRHÛeòO>-\x0010KçÚî6\x0017\x0006ò\x0001æÖ\x0016¶»g,ð
?ö´íEoï\x001b®¨¬\x0012¯\x000c4[ìmfåcjåcf\x0005ÇÛToð}cé3_\x0012øC\x0005XºOÿMcÛ£	ªD~|\x001bP´ÔÌNÊ\x0013\x00053b\x0019ß>g'ûý\x001fâ×{ÍøË_ý2¨¨Fª\x000e9Ô¨

ñ8ô¿U^^^VV\x0016®-ø¸êìì¼páÂ­[·\x0010\x0001¾ªTª\x0012ø\x001a&===??\x001f>ápPnJJÊõë×	gffb62Issstt´¿¿RRZ­&CÐ>{ö\x000cCª««¹Èýû÷±\x001cÆb\x001b¤îÝ»ÜÞÞN \x0019&&&blUUUjjj\x0016+\x0014766mS¦¢ú\x001f×:Ã\x000f^þzÇ\x0019ÉýÁ\x001fÙ\x0005Í±\x000e4\x0017\x0004\x0000¤ùp¬\x0003,lfÌß\x0019ú§ÇO;ÀÆäûððÁÃo¶)æÛû~,\x000eøØÿ­ùÍCk\x001f0ÇÆoù×{ÿ^×b=K£í×EÇ¤Ì\x0016\x0005ðl¥Ý\x001e8±1ö¡<ÜÂQ±zrOòÝª\x0007Æ~\x0019TT#UF\x001cjÔÁþ­Ca Ä\x001f\x001c\x0019ì¿?Ë6Û­©©	Í¡û{{×Z\x0004Îßÿ\x0008ý\x0006\x001aÐ\x001d¬Y0`·ïSQQ
]ø,I-qóIZºîÐ<ñ\x001esë@¾ aAZÓBq Éü\x001d\x001eþ	\x000f\x0002¥uz.Öõôô\É+9~èê`lÚÁ¸4¶eýØè´K9%/_uêÞJ«Õ\x0004ÈO2vR3»`F,cÄ!\x0000i¾}¨é°Å«£]¶)÷ì¿Øöì'c¿\x000c*ª*£C\x000e5jÃ`C?\x0011	5\x001a
n«Þ·Âe8\x001c\|ìÅ¤EV­V\x0008i	O"8s\x00115+8\x0018\x0005§¼¼|ôèÑ...ðÉX-+LQd!2\x000fÙ\x0003RÜ\x00064¬8vå6Iâ»ÅÌd y\x001cDz\x0007Éð¡¸\x0007\x001fPiÙÜ(îE\x0019¥,MEõ\x0001ÂÁ)ûÛ^2³ÛÉíC\x0000Ïæo(:\x0001T\x000büÍ¾3-½Ä«ÃnÞ¾¯ÑjÙ/Ð¯\x0004N¹®W£ëÃwC«¯Ó\x0012§_×Ë\x0012t?êzûô~}CãJ×}<»=\x0008 \x001dÊä|q\x0018#	cìÃþ°ÖýTRVYW·ÚØ/j¤ÊèCÚ0Ø\x0010\x0003ÇSÀù£\x0006d\x0007LÅ!httôÖ­[\x0007\x0004ß¿Ð\x0000R%>)\x001b<ðýcß¥wÍÉqûàâwu©¨¨.\x001cöûc®|³3ÉfÕ¾Ù6zf\x0004~|¡\x001f#ðå	|ù\x0002_Fègú×¾Ãé­mÏÁÒÄ8¢þEéktú2üðvvu\x001d:~qÞ§2¾Hf\x000e\x0016òíå|ÂTòýåQ.ß&nõOù±á±VÛkìAE5RetÈ¡Fm\x0018lÇ»222bbb\x001f?ÕÑÑ,n%´uuuG\x001e?vìXaaákÉÕöàÁ\x0003d+++áúK.\x001d9r\x0004~AA\x00013))	Ã1\x000fj%AÌÞÚÚJ\x0016Bª¦¦\x0006SÕ××-577£{çÎ\x001dö¢ÔCoQQÑ®]»6lØ\x0010\x0012\x0012R[[K¶\x0014
JKK1­J¥"coß¾\x0015±Ê1VpÐ½wï\x001e\x0016BYNN\x000e·Û¨¨(ÌéîîÍ½öööØØXmkk#¿\x0000à¹É~(QSQ}ppp rò«<ÒV¹ÅÍ\x0004\x0003¤AÑ|¡7#ôaØ\x0016\ýÛE^Ï¥Ii\x001dÏ_ö\x0012ÖVgàsíToîå«î9e¢µ{y¢P¾XÎ\x0017+øöa|0Æ!q\x0008ÿÌ5þK÷Ä\x0018e!@\x001ea*ª\x000fÑ!\x001aµa°!\x001e\x0007Â¢p\x0016.\8Ê@3fÌ `	¥¤¤\x0018¦\x0008jYÁA\x0019\x000e\x001dzÍ"1'O655Å=µ~ýzÃçÏGP"\x0018\x0006§OH\x0016\x0002Æ#ráÂ\x0005Ò½rå
º\x0011\x0011\x0011¤+É\x000c\x0007N0áÌ3úÛåðE\x0016xCC\x0003º\x0001\x0001\x0001£\x0006	Si4\x001a8Ë-#s\x0018ÖlÜ¸Q­Vcªª*\x0012ñððxÍ\x0002@uu5ºÛ¶m#O/b*ª\x000fVûWûcr]½ÎI\¢fÛú\x0003§ùÖ¾Ð±\x0006N«õ6Ër§Ø94þLNõýÆÎ®®¾>-ËÌý\x0006üL¬W\x000fÑ}Ú®îîºGª"Ç¯¢x"\x0019#ó$a$qP;ñ$ÅÎ\x0007×z(=\x0002+j0±ß\x0001\x0015Õ\x0008Ñ!\x001aµa°!\x001e\x0007\x0000!î\x0014´K,\x0001\x0003'''\x0003eÆ\x001d;~üø7o"®T*-..ÎËË«¯¯ÍB8ØÜÜ\dÁ-\x0001cÆ¿iÓ&¤ÒÒÒ0°   µµ\x00155ÎÎÎãÆS**J.O8\x0011zõêU¤N>ú\x0017/ö³ÊÏÏG7::\x001a>v2aÒÓÓ+**bbbruu%µµµØí¬Y³P\x0013\x0017\x0017\x0008j0?Êgdd¤¦¦bç\x001d\x001d\x001d\x0018\x0008ÈGM{{ûÌ31$$$äîÝ»×®]³±±AW¡P`ó`iÌ.ÚÊÊJ<oMM
Æúøø`,ý¿ö¢¢úÿ\x0017><×oÖzÉÒ¾üöôb'\x0005_èG\x0010ciFèv¦¥×|{w¿¸SIWsó(¸QUx£º°¤º ¤ª@ß²V
«Ê-,Wª
¾µt
3]\x0012ÌØË\x0019ç à9îå;*\x0018Ç°>pÞrú+Oå¹ôÒV\x001bû\x0005PQl\x0019\x001dr¨Q\x001b\x0006\x001bâq ,
ÇÊÊjêÔ©\<++\x000b\x0018¹|ùrø`iøÙÙÙ£8¼|ù2!X\x0002r£ÛÒÒ\x0002°4ü\x0001Ø9
EEE`o¡P\x0008ÿÔ©SHa9\x0002K£\x000boii	\x0002\x0007!sóc¾¾>,\x001aT;w\x000e\x0002Ãåx<\x0005×}ôè\x0011*×¬Y\x0003\x001f{¿{÷n.\x000bÒ\x0006{O6­§§§®®Ð;Z''§×ìo\x0002|///øä?b/j°º»ÕÊÔ\x001b[üWº%,p1\x0002ð3ËÒÖ>|}ë\x0008\x0018Ût±÷LËï,lý\x0004N!¢UabgxµÂnµBôÅ^»/"ìÖDÚ­Ù'r\x0014:Ïu\x000ce-5³\x000baAZÁw\x000c1{\x0019ÇïùE8l]çqV~àÏ>§ê?Ñ!\x001aµa°!\x001e\x0007¥\x0005\x0002Á)S:;;AZ­\x00169sæL4	\x0005 h0äÒ¥KwìØ±}ûö'O Qsrr\x000f²U*\x000f\x001f&snÞ¼\x0019)777OOÏÈÈHd\x0011\±b\x0005­­­\x0018®V«\x0011ù'ûå\x001e\x0013uvÅq­¯¨D³hL¶\x0002ó\x0000Ý´ÝÆ²Ê0À0<¬º+\x001ay*\x0002®º\x0015\x0011å¼\x0007lEQ\x0014uy4\x0014\x0011´Â*\x0002¦ÝºÑ®\x0005ÒX\x001e
H\x0004Q^",/\x0019~gNüe"º¥]d²ëýæäæÜsÎ}Mr÷3fff3gÎ/ËµYúæÍè&''c?( Þ\x001e\x0019\x0019QiD54'H\x001bãèèJ<6@úúúB¡\x0010\x000eº\x0008bó\x001cK;;;£¸®®\x000e KÁVQP]]ÝÖÖ\x0006çÐ¡C®®®pÊËËá\x001c8p`\ÃÒSôAbbzOoKSsÇÑ37Üýäë¶ù4LÍÒ¦\x0004"\x001a§\x0005è\x0002§EþB³\x0000þ@ýO\x000e}ø;¿å&\x0007øÿÒ$àÃ5A¯,x¹i°ø0Ï"Z(\x0015Jcø0k tÐÚx\x000b³NÞ8|©ìßTªQ]\x001fé'/C\x000e3fÓ`¼\x000e¯±ôÐÐ\x0010"`W´666@G@cAAÁ\x000c-ÕÔÔÐ(âÉââb\x0004Ï; ¦%g×®]Ü¨+WRXº««êÁ±\x0004«ÝÝÝ¹¹¹ÄÒ/5"ÆÌýýýp\x001c\x001c\x001cPE±4%æøð!eñG 55\x0015x\x0002T¢500022\x001aEÝDÈ(ogg\x0007\x001f\x0011:\x000efCMll,f¸{÷î³gÏõ÷÷ohhceeE¯¯ï8ci&¦©ÐØØhÕý'Ç
Ý|åkÝ-
\x0013\x0000	§MÕÆ7
\x0010\x0006òE<8o\x0016$\x0014\x0007\x001b
,Bùa\x0002IÐ*ÜL\x0012%D\x000b¤1j³	¬Õ\x0008Í³7Z{ÄÂ)ÙÑ+ëÅßT\x000e)FèÇÄÄôc¤sÈaÆl\x001al×á5\x0006\x0012¢]¶lÙ%Kºví\x001a\x00182!!¡±±±¾¾^¡P\x0010ëj³ô3gÐE\x0010R;wîDêÎ; Ð¦¦&B_bé\x000eÔ\x0010ß®X±bÞ¼yð/\¸\x0014SitëÖ-tO:\x001d¢\x0000eã\x001aÅ\x0012Ükm`cë¿Ð\x0008­­í¸úV×p,MÝööv\x0014lÙ²e\úÀæÒÒRøØùðð0\x001c`6
°á\x00168¨AÐÅÅ\x0005~TT\x0014Ú}ûö3fb"á
Þ«?pÍÍ÷Â:·äU6\x0011BÓ¼Õþ\x0002P´H
ÒBQ0O\x0014d 
44\x0003T\x0007óÅ!<q¡E(O\x0012Æ\x000b¬"`|+8Ñ|«\x0018¾4V 	\x0001ÒÖq\x00028ãõ´ÜìäñE<÷êw/\x0006FÇÆ°¢®\x000fÍÄôÎ!\x0019³i°I^\x0007bi´«W¯^¼x1\x0017\x000f\x000f\x000f'nD*//\x000f~~~¾ö(bi´7nÜ@633ËbBJ\x0011K\x000f\x000e\x000ej\x000f$&\x001f?®««+ü\x0002ø±±±:}ú4ºÙÙÙðíííáËårnªäääºº:8&&& mÌàää\x0016ð<þü§OÒrÄÒÜ_\x0006¥\x0011¡å6nÜÈm¦¤¤\x0004S\x0019\x001b\x001b£\x0018ÿ\x001aõòò"áÂzzzøúúrgäÌÄÄô6©oÓ¨
8\x001dXày@¾É3uÍ\x0006Ù
q`M @Zm¢@°4Ï,'\x000e\x0004EóÍCyæ¡jæK"yh¾$'æYËøÖq04N`\x001dglwäãÇí¶§8ïÍÜ\x001bséziwo\x001f}\x0004~¼t\x000e9ÌMMò:p)\x0016gÏí©ÑªU«\x0000\x0002 ¥¥ci0gDDDPPÐÕ«W\x0011\x0004'1°°°\x0010Y\x000cß½{·Gzz:²ÃÃÃH\x0011KûøøÌCBB*++9vssÛ±cH$¿téÒ\x0006lãùóç\x001f|ðÁÜ¹s###e2\x0019ð¨\x0018£îÝ»\x0007ÊEñ={6mÚ\x0004ßÁÁ¡¹¹\x0019ÎæÍ¹\x0013edd \x0006\x001fÔ××\x0017
äc\x001ebiP7"Ø¿­­-ºæææ'N\x0008\x000e\x000e^°`\x0001º8/²µµµ´\x001cMÏÐ\x0008,Mc§ìÄÄô~¾B\x000fN~ùµWàeG¯¿Ø8Xe\x0017e,\x000eæ©A:\x0000 Í×P´!@Ú2'\x0001HG\x0000¤Õf\x0015-Æ
ld|\x001b4pZ&´ÿhÃQsòg;3¶ûd\x0007ÈòþQÑ÷b\x0000K`!]ég"C\x000e3fÓ`¼\x000ex_\x00082---g¼Ò¬Y³@TsåÊ\x0019ZrwwGP©\x0011\x0006\x0016\x0014\x0014hg\x001d\x001a\x001a\x001aÅÒrss\x0011$æ\x0004D¯©©¡	Ñcõôô(\x0005¨ÎÌÌäREEE\x0000cn ©©)\x0008\x001c\x000c\x000c?''\x0007p;88\x0016ì=gÎ\x001cDB\x000f4±4÷¡­­Xþ\x000etvvÚÛÛss.Z´(%%e\ó¸×××\x0013KÃÇ´]]]´º\x001f"tö©ý411½ÏÂ
}ÒÜ!Ïû.06ÏÃ÷ýç_Zn9öÛßÇ¬	ÐâPCq¨\x0005@:'9ÌDð$Q|«H\x0014\x0016Ã·\x0006NÇ\x0019¯=òO\x0013L\x001dÖz¤:í=ï\x0015sììßÊï=\x001aR0fbZé\x001cr1\x0006äuxùJ\x001e=ª®®®«««­­moo§,h\x0013mOOOUU\x0015âÈ{£¦4°··\x0017YÄ)ÛÚÚ:¦\x0011RÀZ¤ê4Âð¾¾>\x0004\x001f?~LA*æ\x0016âp\x0017\x0005\x0017/^ÌÎÎ\x0006Ík^Xâ^ÚIaaáùóçoß¾
¾E\x0004Û®¬¬T(\x0014/µµîß¿OsÒ¶¹Ôðð0ÙÔÔD¤ÕËÊÊ²²²ñ´\x001f\x001a9±Ïææfncð±öñ§î³ÄÄÄ¤þ\x001c½\x0018\x0018¼[^~Ó7â¯Û÷goú<ÍÖå¤È>áãu²lc­£¤ÑB«(4Jh\x001dcd\x0013kd\x0017»RÐG?Ù|ÂÒåì\x0006Ïtç½»\x0003r"]Ï/úWK[R¥¢O®\x000fÇÄô³Î!\x0019³i°ÿéRL|hÀ\x0004?ü\x0006½1KÁ\x001fHicZJ\x00113koãm)\x001a;qQí%8âÈÄ\x0004Ò\x0013+Ù[ÌÄ4
Ò\¾±®Þß>Hþó7Á²¯¼\x0002r¶íË²ß¾Ö=ÅÚõ¬¥Ói\x000b$sã)\x000b§Ó­çì¶§~¶3ÝÉ;ÓÓïâþÃãN\x0016]ºVÖðä\x0019(][&¦w$C\x000e3fÓ`¿\x0011ôÜ(Ê\x0011´DÑ\x0008ÂQi\x001e#ò!®(C\x0001\x00059\x0011"NL\x0003i\x0014­EKpRiôRK4\x000fÍ@\x0011ª¡.ùJ¸%´Ë £emV§³p\x0011îtÚK¼±¦â~×xijû×ÝÓ_QÝTø÷óÿJ,:\x0018}uOðå\x001d\x0007å\x001e¾Ùî>r÷ýÙ\x001e~òÝ¹>áy¡ºòuÎWeßÖ=mí¤¯
\x0013\x0013Ó»Î!\x0019³i°I^\x0007\x001b¹6=¾­f$É!¨öÌoáµÈÄEß¶e\x0013³oÔäSoìþ×ã311ýßÒ¾kJjH1ÒÿBÑÛ7ØÝ;ø}ÏÀ÷Ý\x0003ê¶g°§w°¯h`pxdDIÿsÇÙõdbz÷Ò9ä0c6
6ÉëG\x001e øøø­[·fdd ¨R©\x0010	\x000b\x000bóööÈèè(ÚÄÄÄmÛ¶\x001d=z\x0006fee¹ººº»»»i\x0004\x0007ÝòòòÎÎN8999(S*hóóó×¯_ohhhbb P(«\x001f<x	===[[[éé¬ªªÂ6Õ\x000f¨R¶±±¨¨¨à%%%ÿa¿\@¢Z·8î;5C\x001d¯c\x000fÇGYùÎ\x0017\x001a$ÑI\x000bÊÊ¬H\x0006/d©\x0015FÁ%èÞL»½;Ýà@\x0004uÊòvHº]êôP0
S3AÓÁ2É´ÉçèdçÌýY´fÒ3vm¶³þ,>Ö^k}ß^ßÌþöü\x0006·¸ÿ>|êV£Ñäää`5Lß°aB¡èîî\x0016v÷mÞ%,\x0016Åbý\x0019%:ä°±ÁL<\x000e@Mâä°°0\x000b\x000b\x000bGGG¥RI ëëëkccCì
©T*dQckkÛÖÖôôt\x000b#`\x00058Û·o§[Ò)åîîNÎÒ¥Kûûû±æ­[·(¡ÕñùÍ7qKµZ\x0008Øj²³³)±¸¸\x0018³gÏÂ\x0007EÓ(H\x0010´¶¶ÆèììÜÑÑéØ\x001d³4Åb±Xã(Ñ!Í\x000cfâq\x0000g1ÆÅÅYZZB\x0015
\x0005Å\x0017.\èáá1<<L\x0005W®\A6&&\x0006caa!"íííMMMõõõNNNÍÍÍ


\x0003\x0003\x0003uuu\x0000ÚÜÜ\¬SYYz//¯;wîQ³zõjDöíÛìíÛ·Qiee\x0005>¯®®ÆÊËË\x00119qâ\x0004Ö'H\x000e

E\x001b>>>2\x000c\x0011bc4²óçÏÃ'ÚG|Ö¬Y`þ®®.ôAÅb±X¬ñèÃÆf\x00063ñ8\x0010KÃruu
\x000e\x000e\x0006£\x0002k\x0011\x0007º¹¹T©`Ýºu`à\x000f\x001fÚØØ¬X±B\x0005GGÇE\x0016	§O¢rçÎðÓÒÒàÁ\x0007îbìîîH$R©\x0014\x0013ïÝ»,0\x001eãòåË½uë\x0016ücÇÑÊ¸Ü¶m[^^\x001e\x001c9±ñåËqYTT\x0004\x001f\x001dbDX\x0013ý\x001bìô¼0X,\x0016Åb}&Ñ!Í\x000cfâq\x0010X:<<ÜÓÓóÆ\x001b`Ô\x0004D¥5\x001aV\x0007À\x00020ÇÇÇÛÚÚ¾}ûö\x0017úûû\x001d\x001c\x001cbbbà\x000f

aÁ\x001a,â   {{û\x001e4
hµ¤¤$\x0014`G\x001eÁùþûïSRRà<yò¤ªª
ÎñãÇ©½Ã\x000fãòñãÇíííprrr(^RRbÀÒ\x0018½½½§Là¦ qt ³4Åb±Xã+Ñ!Í\x000cfâq\x0010X:**jêÔ©¸\µj\x00150õÁ\x0007\x0017/vqq\x0019\x001c\x001cD°´´\x0014ÁÊÊÊ¬¬,øÅÅÅ©\x0003\x0003\x0003ÀìØØXí'¬Õgi¹\îää\x001a\x0002o\x0014`Ü¼y3
^¿~
H&nii³lÙ2Ü\x0017\x000eH\x0018sQ\x0019\x0011\x0011\x0001<.//¯¨¨H$2L­V#uùòe\x0015\x0016\x0016¢\x0001ð9a³Í9sð§ //YÅb±X¬o!Ñ!Í\x000cfâq\x0010X:22\x0012,
¿®®ÎÊÊjÑ¢EÁÁÁnnn`id×¯_oñ¹\x0012\x0013\x0013i:àö,½k×.ø(_]]
°\x001c½½=AæÈ{\x0011Ü¸q#ü´´4\x000e\x001dBemm-ØØà¾wïÞEêâÅ\x0002KÓMÑ¹T*
\x0008\x0008 ÿãÇÔ\x001e4Åb±Xã+Ñ!Í\x000cfâq Æ\x0018\x001d\x001díììÜ×× B¡\x0000©ZZZz{{\x0003J{{{={öéÓ§O<Q.;99utt ¸¿¿\x001f\x0010\x000eö\x0016°\x0016,¹`iD.]º¥-[öîÝ;º#È\x0019M6Á\x0007\x0018£2??\x001f=466b\x001dÀ3"\x0005\x0005\x0005\x0011§uÚ³g\x000f.³²²0\x0011,²\x000b\x0017.À'lÆ8}úô\x0010ý­i\x0019§Y,\x0016Å\x001ao\x000e9llf0\x0013\x00038X444ÔÎÎn``\x0000\x0011¥R	T\x0006¸J¥R¤JJJàYÇ\x001fGäÜ¹sðAÚVVV\x0011\x0011\x0011ð5\x001a
ÆêêjdwìØ\x0001\x001ft½fÍ\x001a\Î1#99\x0019eð\x0001½ÍÍÍ¸\x0011X\x001a\x0007\x000e\x001c ewïÞm¡\x0013(\x001aóæÍ³¶¶V«ÕÂ}ÝÜÜ\]]1\x0011\x0014Mkúûû\x0003ò÷ïß »»;êãââ\x0000ö			 wáÂx¼9X,\x0016Åbý&Ñ!Í\x000cfâqøE'Ðfbbb``ààà .\x0011ÏÏÏ÷öö\x0006"ãããS__?<<\x000c²ÅØØØHzz:²}}}r¹<))	>È\x0019s?îåå\x0015\x0010A1ø<;;à\x001cöìVñUUU¨<sæ\x000c!}gggdd$î[TT¤R©d2B¡@jhh\x001a\x0003l{zz¾xñ¢¼¼\x001ceðÓ\x0000þ½{÷¢,66\x0016S·Ñ\x001eV£
2K³X,\x00165\x0012\x001drØØÌ`&\x001e_?iH'"OÂià+"@\ð3|¡\x001cD\x0000ÉÄÀT)P+M\x0001W\x000bKA ÛÚÚZ¥RI¨¡¹B%Í\x0005{c5D4\x001a
ñ3-KKAt/*C
Ub\x0014Ú,EÝ}Ý»â×Ïe\x001c1È²X,\x0016õgèÃÆf\x00063ýDès 1\x001cê;úH©\x001fÔ¯4^
\x0000\x000c¸\x0015úx<J'ÆÁÑyu¤¹&ðHx,lÁ8"üw\x0018}åQz\x0008zZ×p¯â!8RýÏ\x000f«P`Î\x000eY_­ú&|_o;ßÝÈ¸IÙÚÇ\x000f£ØL@§[ì.Æ¬÷Ý=h\x001bã\x0017³'(üÇáa4sW,\x0003\x000e9llf0ÓO\x00021
\x0012"ú)­\x0011:\x0012X~Ôi$¤¤\x0002ã[\x0018³+Õ\x0018ãëHË\x001a¬iÀê£ý\x001cõ#ú¾Ð³ðA¯\x001f\x0014üö¢ý½¿\x0000¢kéÔ\x001e¡¹\x0011ß\x0015]ºfP?Ö§%¢Rþ/ëÊO7ÅndÜô÷Æ0ÝÈä8\x0008tºÅîblZº>Û/~Ë?ýç¿HýÅ/
\x0013Ìß\x001bK_¢C\x000e\x001b\x0019ÌÄãð\x0015¼7ú\x0014êHY}jÕ\x000f\x001a\x0000³Aj$.5å\x0016£4iLÑ#í¥¯¯¯µµ@\x001dJ¥zõêÕ(Ó'\x0005Hk?ýÚú/£oÂ´óo\x0007õëÇôt±Ä\x0015³ô·Ó¤8\x0008¥OþPh§Ce|Å??¬2È¾ïîq\x001bÍ =A$:ä°±ÁL<\x000e=\x0002Ë´´´ùóçûéôæÍS§NÉåòÀÀ@Ä\x0003\x0002\x0002üýý¯]»â\x000f\x001f>`îû÷ïãââB\x001ceë×¯¿yó·_mdQ\x000b\x0016,ÀsçÎ½~ý:RÃ:Á9vì\x0018²ð©£©\x0019\x0019\x0019¡¡¡[¶lÑêA/\x0018÷ïß---È\x001e9r\x0004>îNm_½z\x0015\x0005+W®'èÅåÖ­[ÃÂÂzzzP¿víZÔ\x001f=zVÆK,INN¦õá`/óæÍÃRAAAmmm(;{ö¬T*µ°°À\x0006±w"êiÓ¦!\x0018\x001d\x001d}çÎ\x001dÌÅFÐ3>"êdÃ
Â\x0007;Áq~má\x0004?[iÛ÷Ò³¤lm\x0013âø3þcMLýñX\x001a"\x001e?ý\x0007R,é5+&\x001dKÓ;§ðÇ1».u[øµx5¹+Ö\x0017%:ä°±ÁL<\x000eà=âÃððpÀ!à\x00194\x0008ìèèÈËËsuu%<<<pyñâE­1vuuÙÙÙ!åîîîììLe\x0007\x000f\x001e¤\x0001Ã¸3g\x000ep\x001a,]VVF<¬ÑhÍÊÊB¶¦¦F«\x0003l¤¨/_ÚÚÚ"emm­T*µH\x001b}ÒMSSSmhh	öìÙtÒÒR\x0004gÎ)H}öQ£R©àËd2øÀàÖÖVZÐÉÉ	è«Õý§ðõõE\x0016dí¥±»¦¦&Dð	ào\x0002í®³³³¢¢ö\x0004\x0007÷R«Õè\x0007¾\x0003\x001b¤¤¤PÏÓãøú\x001awÄÒ$¿ð¥£dY\x0013\<8\x001aÓkV,M:¦ñwIìFX¿/Ñ!Í\x000cfâq äÃ\x0018\x001d\x001díââ¢\x0002j{{{{ÁÉÈârppP{»»»ÁÒßýýrÍªÊâ¸\x0014;\x0012éDî(Pn
\x0018"2\¶\\x0002A!\x0001_ N;\x0008-<`| dH >Ì\x0004\x0008W\x0015^Ô\x000cð2\x001aAC5cÌ\x0004Â¥bÁH\x0000\x0003F\x0002¶S\x0010(\x000fãß|ÿéÊfïó\x001eRk¾/û¬³öÚk­³Î·~§¤\x0004á?þXQQñôÓOÐ&:Ë/ÏËË»té{VTÏáë×¯çneee¡e-
;vìÀ0uëÖ­HËC\x001d½xñb6?ååå¬¿þúk÷\x0008>\x0007úôécqM6
,¯©©á.Ü¢E\x000b,¿òÊ+\\x0012]·nÝ\x000f\x001f.ÇÀc0ØÍÀ¾}û°ÿöÛo³\x0006Ô÷ìÙæÆ\x001b1xìØ1H#<wî\x001c«V­òý)3R>&\x0019É,\x001dÞ¥ÍUüó_¡æ¡\x001cýóm\x0017/_ñî"aäü¦Û4¥sª²*4\x001e{\x000báßvíýï\x001d\x000cw«5ÿ®EAlñÔ0\x001a:±òÐ,òXÿ\x001b\x001cnà¸áè¦(2\x000b/ûÞý{¶\x0013³±´\x001bBlê\x001a\x0017B¬ý0E±!(ÛaøQý0ýX5÷ÄÃ\x001f|Íy·`²9\x001f;¬¼± Ócÿf½J
Çs)¶°\x0011µ§zöÜN~ï¥]Ç\x001e(ö4\x0011¹:Ìð\x0015\x000exX\x001bÒ\x0019Y4\x00079(|ÊiJGÇ¾\x0017
Ö<6µÝËUlZÒÔÒ\x0016C³\x001bM\x000e9¹`¦|\x001dÄ,F\x001aÕ©S§ë×¯\x0003Ï±Q\x00068ÃÒ®¾îÂÒP%,Í\x001aÐå÷Ã\x000f?T\x0017.\ÈzéÒ¥¬O8qëÖ-4-ÅÒëÖ­ãî3g¢\x000cK\x001bO8±uëÖUUUmÚ´\x0019?~¼Ý\x0015Ks¹hÑ"6Â®¬×®]Ëú/¾Ð\x0011ò
\x001eîÕ«Å5eÊ\x0014ø¹ººuÏ=\x0007
\x001aD,¸
Æ£Óµk×aÃÉ±~ýúõíÛ\x0017Sµµµ$\x0001ÉG\x001f}ýqãÆ:uÊÂë­·\x0010¾øâ.ÃÃö\x0008KKKIÝ\x000f?ü@Ò¢zþd\x001eð\1wÝ®\x0014V\x0017
¨`dW~¥«_wu°¯S0åiÚÑP\x0001
ÝøãÜúëÎ}&){ã/\x001d6zM\rjÐ®¦Û×°;\x001bØ 9Ì^è$
\x000eÿ®à÷î¡"o£ä¦ÉBjÄ\x0005ÖøíÐXNºÆ2E±!ðpYð¤ÂsÝ"ÍRè\x0018v¼¢ó\QõÃF+cW\x0013k
ÇåolJ0\x001e[ó\x0016[ÜÐâ}ï¼ãTÃ¡&~¦yâaDÝËOQÛ\x0013\x000f_û£Nì?Cú¢"ÞØ÷"åß»=¡"Lg-¶\x0018ê\x0006sÞ\x0017]nææor¦|\x001d9_xá\x0005h°C\x000e­Zµzùå£\x000cEs÷Î;\x001d;v´»(\x001b÷ÖÔÔ \\\,BF\x0008¶mÛvøðáÜ]¾|9\x0006Û·o\x000f\x001bÃ«\x0002K¶»,
ÐF\x0019\x000e\x000fW¯^rçÌù_?7o^^^Þ·ß~«]\x000c±ô«¯¾ÊFØõ5kX·k×#\x0006\x000f\x001e,Ë\x0003\x0007\x000eµCÅÒ¸Ê­§z
®¨¨`×\x00193\x0018K3
\x000b\x000bå0A­\¹\x0012ÉÝ»wafX \x001c`\x0010h\x001f;v¬ÎÝ°aÃíÛ·\x0011={\x0016	\x000e#dûáÃ\x0005ÿú
ø¹þ»~ÀÒÂ\x001bHÆ\x0015zÕEQËxnÒlZ\x000c\x001d¶?`Ôãfgj"\x00191	kÔ¤)kÖ´ÑëJp¯Ô\x000cµ\x0011e\x0016Øá\E'.$k\x0017â\x001b­M:\x00028÷2¥%!!d\x0006}~ya·õÂçhmdêë\x0000mã\x0003±4³ÓYxlã¥ÿ´j<ÑS`/É	S×¸\x0010\x0018²¢Ø\x0010¸ë=e
1$çj{%+\x0006H'ºå§JÖ¡Òó±ÏÝ\x001d\x001c*
5ûü²6LòüTiQlL+ïl\x001fª\x001aaÔÊ¡·Q!XÝ¢oÄhïÅh»T±`þc'å\x0013÷"b¯ÇM§ûúnè1¢ú±¯\x001b\x00150©F(ßT<æ^÷NG°=|/RÖ¼\x000c«ðï\x0002\x000b¦¦Ï\x001f\x0005¨\x0007m>îgNã¡y&\x0001ÜÌÍG<S¾\x000eÆÒð!\x00108kÖ, sÓ¦MBÁ(Ã:u\x0002A£\x000cÓ
\x000eµÅXKÀ\x001býÚÚÚ6mÚ\x00181"ªgéÉ'Ï9sÙ²e¶QÄ[^^ÎÝÓ§OKÂàî®]»\x0010BÑÛ·oçY³\x0010¨Ç²ôÚµkYã\x0000G,Z´H
\x0005\x0005\x0005½{÷F_ä?uêTH¸ºº\x001a;=zô\x00180`\x0000:\x00006\x001b\x001c9Âå!C
\x0016ôìÙ³ÉÀ¶mÛººº7ß|³{÷îèO>\x001dÂé\x001b7vîÜ\x0019!ç²÷Ë/¿dÝ·o_¶£öùç7/¦ÐéÜ) ­xdëUú¦Q¦¨\x0007YÏµ¾I\x001ft54Ö_dÍíÂQ\x001cEÈçL¹\x0004%5\x001a«\x000b{j4>/\x0003
²45´ÆZm=¹EÊ\x0014G»BmôR¥õh\x0001>
XZ{y4\x001eDÉ=\x0017\x0018\x001a\x0017BÊ\x0014e\x000bAOÐ«\x0010AùæeÉHÛ-\x0006lº\x001feFéÞ#eê<!jûpí[y»å\x0011ûMjÜ@­^ÔòVö±MMá{çE*¯¼#\x0004i¸§£¤Ù¹ÉnØ¡öÄ½üè}wáËøEe5ïý]Ñi»s;\x001dÆ6\x001e÷\x0001+kötÞF\x0014Có\x001aM\x000e9¹`¦|\x001d\x000cþyàÐ\x000b\x0002\x0013X\x001a¤lÙ²%´l»Þÿ}rÉ%¬ùeýÝwß¹\x0006\x0005Æ\®[·»UUUvßÇî\x001fEEEÈE°BeØ\x0015ù¹sçX±¾tékdèÐ¡ùùùv9aÂÖ­[ß¼yµX\x001aùÉ'óòò`þnÝº
\x001b6LÛyæ\x0019¶kMãûï¿Ç\x000egUVVðÂ\x000b|Mð\x0005qñâEî¾öÚk^nS>&\x001cÖmc'hê\x0011W]º\x000c»C,\x0002Ñþ<5\x000fÔn<¼Qc2e·#\x0007¬êÒëza\x0008)Y:\x0016&³ùì
õ_o/ÍCÍÛ\x0007eé4\x001dÙciïËÅ>OÜïÆà=)\x001bJ\x0001I¶\x0010BnêqÝ@ÈËWf6\HÓ·X¨ã!wìÈö¡dßØò\x0002Ê
¢6\x001cU®°/ßLMÊXXê6¼·#ÛW\x000eMh\x0013öÅê\x001d¡HUíæFXª4sÃÖ³&7Y:å{­¨B\÷\x00024.½,F×áðAK.\x000ebh^£©Ø&7sóQÎ¯ÀßÑ£GwéÒ\x0005<®Ë\x000cðUÀ\x000cK?ñÄ\x0013cÆ1Mcé¶mÛN8ñÆ\x001bW®\\x0001¤|òIè\x001aREgÅ\x0015¬Ï9µÛ·o¥×¯_ÏÝÏ>ûìúõëW¯^½wïÞµk×Úµk\x001b\x0015\x0015\x0015|ò	¿ãÆÃ>w£\x000cNÃÒl\x0017K?\x001eayy9F\x001f?®#0ÂüùóQ8xð 
ÜêØ±ã³Ï>+ûôé3dÈ\x0010!î\x0005\x000bPkÑ¢\x0005	r¬   ÿþº\x0019è@é|\x0011|óÍ7Qý§ÁW_}ÅÑK.%dÓ§OGX]]& \x000f·nÝ'óIò«\x001dÖmiFî¤;¨
=~?ºÕ¥þ\x0015Û5ÔéÔ\¢zö°K\x001b!@zx£Ðs8ì­Q=ùX#«!)y/HJÖ®^¼n\x001b;\x0016ôýýï\x001d\x000c-h<\x0010KÇæ<\x001c\x001eK{\êl¹z \x0010R¦([\x0008!XâeIô\x001e>»ÐóXI¨%7¢\x0015åE$\7\x001ev\x001c\x000e?ýlx\x001f2a"Û
ÍË\x0012\x0018¾MÑýP\x0017e¯m\x000b-[ê<;±Cnð\x0008\x001aÜÍaÉYú!ÊûOpWóÙÞbW®§\x0013¾¤îxbh^£É!'7só\x0011Ì¯\x0003	¦²\x00181b\x0004X\x0008\x000cCÔÀóÙ³g\x0005wîÜA^XX\x0018eö?¡-ðd«V­\x001e»ìÞ½[KKK¹ÄT×®]ù=pà\x0000\x0006áaq&¤-}hßC\x000e½óÎ;,vìØa¾íÝ»\x0017É-[Dà\x000cÎ\x0015ÓVUU!\¶l\x0019ëÎ;ëýû÷³ëØ±c²<pà@\x0019Ç2rF§G\x001e\x001aúmß¾=w\x000eý® me\x0000µüüü7or4\x0012\x0012\x0002o³´q\x0000fÝ½{÷#G²\x0018?~<{ùdÐ¡lÄÉ'Þõõñ³üqýBCÍ+[wÐ¿5ú(¥\x0013¦ÇÒÙ@Ñ«[Y»Qcr»`;az,\x001d\x0006åÉÓ°´5îÆ½qð¨O\x0013"-]ýúá\x000f>NN+÷X:\x0019rlx,Ý`\x0008	PÚ`\x0008bÂ4)J\x0008Áã^}Í¹\x0018ìe©A·£úç0³\x0015¿\x0007ÌÞpoÉ«4/BìPb\x0005uVuª|ùæ½\x0005éK`éäÏ\x0010\x001dAþ\x0013ÜNàmï\x00117¥Ó¿wÙH_óiþ.ÿ-5\x001e²\x0018Ñh0·¹¿òu\x0010òñ[VV6eÊ¢¢¢?dÆ\x000b\x0017~Êººº^ziõêÕ¦©\x0005{¡Í¹sç²«¤¤ß5kÖ8q\x0002¹hyëÖ­\x0008'MÁ£G¥\x0019èìÜ¹»S§N\x0005;ÑùôÓO7oÞÌååËáU\x000eEí¿ìßOTI\x0016ÇßúÅø¸oúbvâ\x001fà$ûd2»ú`"/¨1QFgÃ\x0003\x001ax0\x001a\x0007D\x0007Ð\x0010!êqã¨¸È
\x001b\x0015ÈÆ\x001f	\x0012\x0008î,ëøkXuù%+84ünn¼ûMxRVÝ{ûÂmº9ßtêÖ=Uuªî©®O½}û\x00165\x000f\x001fFC¢w\x0008#\x0002YÛÛÛQ\x0006xÓè4D}}=+¸}Í5Ë/_½zõùóç­\x0018<ãUFFÆ={¸7¼Bó\x001cTff&¡®P\x0008\x0006\x0008#??ÕªU î¯¾ú
À~\x000e\x001c8°bÅeË¥¥¥uvv¢-~ÕÉfee-
¶\x000c\Q³«æÎ}\x0001·èÄÉÈÓ;K\x0013À\x0000ÕèQÅ\x000c5\x0000Ô;ÈÎN\x001bA«÷ÂÒUqgê",\x0017àD½\x000b¬Oß\x0005Zð²D	di)¨ë<Û)ðÅ*î\x0012¹L2êË?m¢G\x001aÈ\%\x001aÑ=lú.	\x0003&´m8[þýuNC¨ASt¤+\x0003¯\x000cNeºbp\x000eÐp.û£¹Û®\x000bfó\x0010îa\x0013á»°4\x0016D}\x0003Kó\x0005mÎIå=ç½ü]PxêåÎÏdXDJ9ä%Á<n\x0007"=[ÞûøIæ£\x000b\x001f\x0012¦ºwè¦\x000fúÄ#øyÓ¦M\x0000é+WB!§!ó¡ááa*ó\x0015@íÝØÁ)\x001eP=n
Ü
ÓÓÓfå\x001c&rùaiï\ç¥!\x001cC\x0018\x0000\x0010NÔ·D×N\x000c`F\x001e·Þ	*4·Ym+wa^8	\x0014¦Té´DZxþYZEÓÄNÁã\x0012¹Oú\x0004D\x0011W\x0003#Õ·Ú*Qª¸';4ºËiÅñl£­xA¨À¬EKAa Ìþ9à2wm_krád-l¾ø¨¢o\x0017\x0017tã²´å;©Ìë¼ü]Ð¥ÆýCûLE¤CX\x0012Ìû`¶*R±\x0019D\x001aHÓ+\x0016Smhv¨ö`¾¥\x001aÍFÏxlii!®««³bí4\x0004­\x0018	sÜxâôÈP\x001dý\4\x0011\x001a¦Ã`[©¶UkË¥\x0019P \x001a5»pB¡ü»/þ`6ÄÑwú\x0002³bi°D F\x0014T\x00009¨oAnf%\x0005\x0011a\ã´\x0011´z[ÞÐ`ÉR\x0008_ë
\x0018ÔGsøîRVO¼Á(â´D\x001a.úai)ÆÕÜhéO>§@¡rªhÍyÜ§@ß\x0017ÁPAV[%'¶!7Rµlº!0\x0017Ð¢\x0019\x001fh6ðù¥Ò*á!Ì´ÑDÈG¡òyvÏï\x0014tÇüâËõf?h«î;úâæÜ)`c\x001cÌ!hËSCóÏEß/Y~XÚã¾s\x001aÂ{Î{ù» +Æúô]¶\x0013YóÇt+\x0011É°XrÈ\x0011\x0013KyÜ\x000e*3k²­ôøÖ]³í\x0019hß©©©±±1+\x0006±qGñâã1$êj\x000e«Ä>\x000bV.,ã\x0006'BàÓ\x0019AÒ²Ë¶9\x001aâ\x0014\x000e(gâ¬XÎhô@Ç¨:Äox«ÕÓ1§"ÓF°vÚ\x0012\x000c¨n\x0014ê]û¬ÏEÀã\x0002¢\x001f\x001arÐDøô·E>f¶°4õoª-\x001d
Íä3ç)ÐÝ'î\x0012¹Où\x001cx\x0004ÐÞj	C3ÂmN\x0011§\x001f}S"OøhÁSÂ¨¹mf¤%\x001b÷¯¦\x0007Á°E4´Ã¦h4gþú\x0001çikhYf@!OÊmm}¸Þå;
AÆß\x000e«gî_uÜ¤õÂÒ\x001e÷Ó\x0010ÞsÞËß\x0005_\x001fÔ\x00089\x0018Þ¼>a±(å#&\x0004ó¸\x001dfE+{xI\x0005§Ç¸Ã9±h4\x001aÕÞjá¹÷\x0016×Ù©U\7Ûùñ/(Ñá\x00056X¾K3Î%>-ãÄ¡#\x000c¶ÿÈ)rÃ	b\x0012ø¬XÚútF\x0007\x001c{\x0019£üPÿÀ\x001dpy§/¿zÆ9m\x0004­°\x0019+@mÑ\x001bæ\x001a:\x0010Ù
' Õ`eh¦øÅ\x0011O\x001a§ÙN\x0002F?p.«¬&ìa\x0018`pÂ+\x001aî»Keð¡A\x0013ÂÒèS¦@KQÔ¯<·)ð\x0012aYÌ%b;\x0005¢¸q³°ì\x0012F\x000bGTÓP\x0007\x00181Sð5\x0005¯\x0001&\x0011õø¥ôÖÒ \x0013}¢g¸¡!Æ"ä6ga¿¾\x001a6[Àá\x0016\x0003£á,eß©×IÚ)\x0014\x0018Åÿ°ù'ÚÚqf\x0004C\x001ebUáL	if#ìëì\òÁ(ä£~_?,íqß¹$Ç÷øwA×+Ì\x0011ß\x0017£ó\x001aÏdX,J9ä%Áfµ)\x0018\x000b#\x0008HUcNÍGÃÈ\x0019[ÿ\x0004ûWÇZøº(Ä§­­á\x0018Ò\x0010ËÌ.Æ\x0000­!³5{æs\=UYÌªá,C$î¡ÚÖóa­\x001aº¢Q\x001bb)LÏ¸\x0014êÔ0`Ü\x0014Ìo\x0001\x0007Z¢°4Eb»tîHé}
^(î\x0014\x0008W\x0002\x0006@Zv	c\x000c quDøØæ¹x\x001e'ü4ÓÃVÍãBä¯±\x0016]+TÀfÙî;\x000c§î;
Òô47­lg¤-íï¥-ßI,Jàß\x0005ÛdX,2'(&¶ôÌç6!LÅo8\x001c\x0006`\x001cGvS\x000bó!\x000eF@:áÂycÈÖL±bgÉ·ðÄÙ\x0002Æ<¦á`Û¡S=\x000ebÛTaÍ;÷aDüâ86;qêÁ¬ÇpDG\x0014?½¥1\x0003cO²Ê\x000c.¢\x00140\x000c\x0001ÛÆ¦NG¡Kï¤_þó_8\x0007\x0007Þ»ð)Ä]¢¸SpùúN	Ã3Âçs\x0011|ð·Mo§x<¦\x0007jx# àÀf[sj4S¨ê¾CÁÜw\x001c$<yîðô>wuFX4Û¯¦Áy«ÊéS½\x001a\x000c\x0005l~>ÿI\x00157ç½ÿ]P%­§Óå/\x0019\x0016R\x000e9bbI0ï;Ñtdd¤²²²ººzbb\x0002¨|êÔ©îîî¬¬¬\x000f\x001f>h4«6¬©©ijjÂc4\x001a\x0015¾\x0015D"hÉ+å#&\x0004ó¾#\x0000À çhL\x001b6l¸}û6\x001eQßÓÓÓÕÕuôèQòRýëëëÛÚÚP®­­
BT),-\x0012D"ÑWÊ!GL,	æq;|0¸¿¿ïÞ½¨D"\x000e\x001dª««{ðàÁºuëöïß?44´sçÎk×®\x0015\x0014\x0014ìÞ½»¢¢\x0002õ÷îÝ»{÷îÖ­[ÇÇÇ©ùÜ¸"H$\x0012\x0016R\x000e9bbI0ï;\x0002\x000c\x000cx\x0006\x000cWUU\x0015\x0016\x0016Z1ÀÞ·oßË/\x001d;V]]
®...Æ«ÖÖVp5j\x001e=zTRR\x0012\x000c\x0006srrÊÊÊFGG?~Ò¼m\H$\x0012D\x000bB)\x001c1±$Çí@\x0000\x000cF933óÅ\x0017Ï?ollÌÍÍmiiÉÏÏojjºzõjAAA{{ûÀÀ\x0000|àwãÆ+W®\x000f\x000e\x000eZ1 \x0017\x0016D"è· CX\x0012Ìãv	\x0018ÜÐÐ~ùòå\x0013'N ýøñã-[¶TWWONNnÞ¼¹²²\x0012t}æÌ\x0019øïØ±\x0003\x0014}çÎ\x001d4éêêBsaiH$\x0012~#J9ä%Á<n\x0014
ð811¡¾åÇééi+\x0006Þä\x001c\x000eÕzª¤B¶©H$\x0012D¢\x0005ªCX\x0012l\x000e[øÝ»wSSSÇ¶L\M\x0005nîsoD"H$ZøJ9ä%Á<n\x0007\x0015£Ñ(
\x0003\x0003\x0003\x0017/^\x000cÃÑÈ
£££ÝÝÝÓÓÓÁ`\x0010ÚÛò¶H$\x0012D¢¥§CX\x0012Ìû\x0000\x0000ÏÄ422rüøñ¢¢"°ô'OØ°\x0019jjjÊÎÎ\x001e\x001b\x001bËËËÃc$\x0012AÛW¯^À\x0007¼Í"H$\x0012ªR\x000e9bbI0ï;X\x001a$Â¶mÛz{{_¿~ÝÝÝÝÓÓÓÑÑ1::
ÎÎÎÁÁÁ[·nÕÔÔ¼ÿ~xx¸¡¡¡¸¸\x0018¯jkkûúú¬\x0018r£yÚ¶":º{*n×>jý9±Ýö\x0007\x0007ÇÇ'\x0012ÛgB4\x0019êûµßöÕýÍ~bÆJ:½\x001a\x001e\x0019\x001d|ÿÁ½¹í}âo¢ëÍÿæ\x0014`Êä3\x0019ÐÜg\x0000\x0018W\x0012ýì³C³ÿçm¯È(ZÛ)£Ýèmß¯ÁÉÉ{çf+Ñ\x0012PÊ!GL,	æq;|0øÍ7Û·o¯¨¨hnnnmm=yòdFFF[[[UUÕÚµkQ(((xöìÙÆ\x001b_¼xWgÏ}úôiZZZyy9G"\x0011ô3¯W$Òôý_+Ï^,}öËK\x0014`	ì\x0019}úG +\x0016¡ÿNT\x0001¥¾/û»YÁÒ~zÎÍ+rzÕüÏ×þã{sÛ\x00153C
ÃÇ\x000bÏÍ-ÂTéÆ­\x001f1;?Í}\x0006$g~F9áDÙ}óíiÄ	û:û\x0010¾£í×Ä[vË>ô-jJÿvëu{{çpFÌøÅ^ V$tSHøf\x0011ÍR\x000e9bbI0ï;0\x0018ë×¯;w®¥¥¥¿¿ÿÒ¥K çÒÒÒÆÆÆ7o\x0016\x0015\x0015õõõ\x0015\x0016\x0016NLL\x001c<x0\x0014
åææ¢É#Gêêêz{{gbBWóµoE"C8ëq²óc~ñ\x0005ü\x00023*n×6ét&¡òÇúûgÿRJìC´£\x001c ò°å'â%¼E
³Ä\x000fwîÃ^¡\x0006e´Õ`\x0006þ¨'ÚQ\x0003@«?gÃ<æð¡·Ô\x0003\x001cÀ\x0018.¨DìÆ\x0003Ñ[ªGY\x0002ãAÑöÿìëKÔÛ\x001aÇÿ¯zÑ«^\x0005§Þ¥\x0011\x0014($Ð\x0013d\x0011Eí
*Ã¢%äQ*-¶I¬a·;¦ÝO!¶k{­tQs4Úof¾ø°Z3ÚtÒ\x0019;g=,~¬Ës[ÏZ¿ù}ÆÛ5úRfIá§\x0017ÅôÅÒi\x000bh,íîÔÍÄÒVL{wëÊÒ®O¬ÕµØ-[åà¼UmÁÄt\x0013°¬Ô\x0007Á­Ô´M¯PvmÈ9Qê:ys=[z¨IS~XõpÚ£[R¥wmÜ;©²0c·È-¯7o$mAÒÞaÝCõõÇÁ;M¥!\x001a¯\x001e3bi¯È^D÷^X{#è ÏÅãé³MUÏ½n)¢ \x000bFr\x000e9¡áë\x0000ýÂÀccc+V¬xòäI___WWWkkë®]»P(**Ú\x0014¸zß¾}mmm¥¥¥\x001d\x001d\x001dyyy±X¬¸¸¸³³sbbâó´Ìç»\x001b$È\x0017bPä
\x001fk}Ð7ï´I¾ìBVñ6O>Ó4éä\x0015 ðÛ\x0001­òí>~èË° x3xñ\x0003ó.ÃKUÌY*? \x0004ÌT×EÓð aXÂ-Íã]\x0010Lð Vay\x0002\x0006ÞsÔ\x0011&%\x0008óx²$5o×Ì04?\x0018\x0012\x0014\x0013\x0012Ó\x0005¢¸X(N[@±4©âÇÂÙÆ1±ÌÕq+\x0016Msví±´»\x0011ÓAYeL hu\x001d«V\x0007;AË\©j_ìQ	Øa\x0019ÈYz*àæ©ÿPÚ DQ¤ø³41Ïvµ\x0004{:2Q·{\x001cÒW,
ítlã:\x001a1°Ên&¸µ[$\x0013:v²²y\x0015M{ôiö;ÌÓ\x0017ÁªÂîib¥
Ð÷ÔÄÒ©EV¡tý\x0012ùTTaÅS7ÙB«cæ\x001aZÙíòPdå\x0010\x0005Y0sÈ	-´,´\x000c_\x0007±4OÀxË-


»wï\x0006O>]PPpâÄ\x0003\x0007\x000eTVVVWWÃÒMI©¯¯¿ví\x001a¤=22RRRråÊ\x0015Ñ8O94Ï.`\x0007Ì\x000e2çâ±4\x001c¢\x000f._mZIéNÃ-4ù¬3É\x0007\x001aÂâRéÐ,-5>âb\x001ba­Ç\x001bøÇ§khV ¡\x0002\x0014Õ¥+íÂ-X\x000cÕ\x0013¼lHÚiYZ`FPQÉ\x0018¨c»vý\x0018¡#ôuW%bé´\x0005\x0014K\x000b\x0014Í³
\x0015MÿUI­mÇ­ÇÒ"[óiX%ÜeÕÅ0ÙÜ(Ô¤óÎ}·àî¢ÈÁ<
½?\x001dBDíÚu«6®{E\x0016ö£`Gz\x001cÂN/íÔ-¨£¿\x0012\x001em\x001asZ5N0Q¨/«D&\x0016";lü¯.¤këþ\x00137-KcånI\x000eBV"ùÙYÚ+»§\x001cdHÎ!'´Ð²Ð2|\x001dÒîÖ­[ËÊÊÀæ}ûö}\x0013ay4
ÒÞðÞÓ A¾*îG9J\x0002Lä0\x0008ÍúPYIÇ£/á®Qp\x0011Û'Oûø¸KÓ¥ CJºÅR>\x001eK\x001bV)OC\Archfai\x0005xÌx;²pòcnÙ\x001aFJiY:m\x0001ÅÒÆ<UÒ\x0011¿¥VL\x0007$*6\x001eK\x001b++\x001a\x001dK¦¿$<iiYp,á|8>K>\x0007j@\x000fÛtèn)Ü][)dk&*¾©1/\x0000æ©Ë3Ó\x0005³Íº[àÅRþ3±´L´eKÛO%Û¯Þa·\x0002v\x0010®­¡»©éÇÒ\x0002l¯Pîa¥ÅãXZ\x0017,°ôÂCNh¡e¡}ë{\x0001ëNNN~.\¸ÐÝÝÍü§O&ÂR<\x001eçI\x001f\x001dúfâ¹ÒÁs è ó'|ù|_ºÒ¾»ì¾ò|¬kë18ß}ø³óÎ}MòF&²µo4ßý¼\x0012±¾ïôÑ¹\x0016»%CÅÂÐ$&dtð\x0003<È¹rnx&þ]\x000fÒ!.à	» "j6$
|2$y<\x001bK+±÷<SPæÝ \x0016Îü@4h\x0019?èWTÍÄÒi\x000b(\x0016ØØNµq94úò*¦|Üºy,­¿\x0003æ\x0013'
QRø\x0013ºÊÒ"öD}*ª®\x0004\x0018²w
øsTQ¥¡ËÒt('}4ÝXU95¬pe\x0007íÖM	¡	AeÈ\x0019&V©JÛ¶¦²Ó<tfÂI©8ÊÖÎ¢¥V)Ã;O% g­UÏÔ!XZïöâY¥)l"bÍ9Á9å¢O\x001a\x0014VyÒ^¬\x0014{¯g`é\x0005%9ÐBËBËðuøì\x0008Ø\x000c!MLLhU¨l\x001d9È­yWç­[·FGG£iîëëchþçç\x000eòÿ.|÷ù|\x001b¯FI0\x0010\x000f»"öà;î\x000eÍëM\x001d¾éRÿ´&(\x0013§knóBÔÐ(Û.LÍMF9Ð\x0019ÿ8ñúAÙÎ\x0014Ô
Ç¤ùbÉWÉ
8<2úæí{ËDê[´\x00153ú@ß^\x000exÕ3råîË(·Öqëïn3õÈdâ\x001aºjný]qmS=[t¥ÇªëÜÕ\x000cmkÑ\x000cwR\x001dï&ÈÄ=ÁÙ«ôÕ;¬í»óV.]\x0006øVþ=µ×\x000cÔù\x0012%mD³J½ía¨ûf[po W \x000bDr\x000e9¡ù\x001b!ÐáÞ5kÖ\x001c<x°¼¼¼««+Uóýû÷³»:yòäðð°Ô`òÃ\x000f\x0008¼\x0003K\x0007	"ì+µ¬ùI`Òûkëxzø_þDÌ« ß/\x0000íOeG+kÎñÌu.A\x0016ä\x001crB\x000b-\x000b-ó7B,-â-,,ß¾}\x001bÅ:::zzz`ìË/?}úôÔ©S6mbØØØ800pïÞ½_òüùs_¾|Nÿ£GV¯^ýáÃ¶¶¶\x001b7nà\x001f\x0000ÒAD?\x000e\x000e½+µ¬ùÉ¦ð\ay AæOr\x000e9¡áë` Í\x0013\x000cÎËË;zôh{{û\x001d;.]JçÌ3K,éíí]µjUKKKssó²eËàêüüü¢¢¢ÚÚÚµk×Ò¯©©Y¿~}]]Ý¡CöîÝûøñã\x001b7â6\x001e+Ê¼¾×A\x0004	\x0012$HìHÎ!'´Ð²Ð2# ÜO>Ñ9vìØùóçÁàÑÑÑ²²2ÐºµµõâÅG\x001c\x0019\x0019\x0019Ù¾};jÛ¶mCa||\x001cN\x0006íÊÊÊýû÷\x000f

íÙ³\x0007µ]»v½{÷\x000eWW¯^\x001d\x001e\x001e6P·\x0017:H ?\x000cvÞ¹?8ô¦=öë÷øùNóÌT¿Õ¤¥ã(\x0019\x0006	\x0013É9ä\x0016Z\x0016Z¯X\x0017\x0019\x0018\x0018X¼xqww7ùùù\x0000óÊ+×­[WTTtöìÙåËß¸qùX,ÖÖÖ¶aÃ\x00064Y\x0005W¬XÑÛÛÂÃ\x000f\x0017-ZtýúuL p\x0000;°t AL^üþÃ'þ96ögcsû÷øÉ\x000e©>zÒ{öçKßjõm{£ÀÒAþ×%ç\x0013ZhYh\x0019¾\x000e§åîÝ»µµµ\x000f\x001e<\x0000}_½zuóæM&\x001b\x001a\x001a~M
«MMM,UTTô÷÷?{ö¬§§\x0007\x0005Ônß¾
c¿~ýº¹¹\x0019x®©©ùøñcKKKcc#þ\x0005Ò¥\x0004É¡ü«ûþOeGËWõ¿ø\x001d-¯¨¢_[ß\x0014%¯²º.±ZQÅP«ÌuéÈuÌ&\x000fæðÒv­\x0012E&t¤iæÆÒÒ!
4Í(\x0013ÚàÐÛãU\x0016Ui²\x0017Ë\x0007ÖÕ¾¼\x00021#ÅDÞ\x0014Kæ¥;÷³JyBØ~ÓV£xóÎÂâR[\x001d\x0012YÕ2ù£¼»ì\x0018~LG,­\x000c\x0015Ë* \x001c,%ö¢!ûÓ\x0003\x000f\x0012dÞ%ç\x0013ZhYhßôR¸¬ký¯\x0002ð÷+\x0004	\x0012$\x000b\x0002\x0013\x001bÏþ|&N¦\x0003éi&J²\x001fhÊÓ`\x0015}ÈS\x001e¬#C#mL A\x000caB:¬j	\x001dr(\x0011K«/ÖH,'¾B(ÚÜZb¶¯¿­ú;CpoUCVéãyK^EÐ¦\x0014×­\x0014,yÁ³RRéDÈR65±4AIF¡mk\x0005ÅÉAó¶Êê\x0010$È\x000f$9ÐBËBËðuø\x0014:SSSñx§&'''éLN\x000bó<D
¶d
êËÃçi¯÷9H ³Äú\x0002EC_u\MWÙci\x0008>mÉXÔci3]F\x0013­%&Â{kë¢$J\x0013ê\x0006Â]\x0016µôDÔ\x001a¢c&"UÃZE±ýZ\x0002Âc·\x001a\x001eK£Ct)Óî¿´,í+º°\x001bÝ+{ \x000b_r\x000e9¡áë Êý<ÿ2ït Af\x0013't*\x001a\x0014ø\x0002B\x001eEª\x000cY2X\x0015»74Áæ(Ét U45tq ³³4ÊÐÁ\x001c?\x001eKó[%7ò\x0015\x001dåcûÊ/,¾di[Õ^¢\x0019XÚªÁmÎÎÒø!º
bÿD¢YüñVI¥qBt7Ã A~ É9ä\x0016Z\x0016Ú¼,SSSñxü/öË<(Êóã¾\x000bh&mc[Ø©°» Õx ¦Ú©Æ8¦u¢rî½Àâ²xGD\x0008 Þ'r/°rx¢x¢\x0007\x0008.\x0007  Ø\x0015\x0011* ôË>S±dWÍï3ßyçy÷y÷÷ìÌ³óy{e) Ì\x0005\x000c\x0010bÉ´yÝª\x001f6Có`¡ÏÙ#{\x001a¸e\x000fÓ<\1\x0012si6"3m\x000ccS`Åx\x0017\x001e!/wi1ÈÄò9fË²· N¦Ó\x0018ÌôÕ}á)zä\x001a¶..Íví½Ò	ð\x000b]úå¿\x0006jÀÊìã¢Í(í\x0018°,&þ_î\aWn3~} °
	â-ÂìC¡ æ>g\x0004A¼À\x0012\x0015ÿ\x0014Ï©£\x0019a^
ÅÜ»\x0017Â\x000egdµ\x0019?7^þ\x0012Ä[Ù%B1A^ó´¶¶âz)¯ 4%³¾¾Ý\x0012\x0004ñÎ\x0003ýcúSd½\x000094Y=/!çÊ58*òÔÓ\x0015|w ¼-!ðjs×B\x0010½Ù%B1A^ç´\x001ayøð_Ò¨+îÿ\x000eÐ¦£óÙ³g½t\x0004	 \x0008x1»äP(&Èë\x0016\¡ÐâÔûÎÑ\x0005®ºÊóÚH§	 \x0008 ¦ü2Òã\x0003Â9çê5¤;N±%N1E®I\x001eá§È¥	 \x00080»äP(&H\x000f\x0008\x0019Ú¬8íª«H;Æ:jõ´Úðä¶ÿ6ÑÖÖVs@\x0010\x0004A\x0010¦ÀìC¡ =;\x001dL£RB¡Ð\x0010i§¸\x001bN1%Îñ7DqÅå\x0015wÚÞEid;êñ¾èû \x0008øEavÉ¡PL\x001e\x001c
&UÕ¢Ø"çø1%\x0010iè´¶X¢+ûëº¬+ÚÞ\x0018u|üøq]]]o}ccãëLÇob0\x0018z¥\x0012 \x0008xÃ1»äP(&H\x000f\x0006ä\x0015\x0011GÄ)÷b`Ñpi\x0007£QÏ.ê?^ÝçSQòþô¶ÿÕiØlKKKss3®Ìlñ\x0014mvEÿsGvÛÎO;:YOCCÃ¿©\x0007SW §©©©c<«­ëÊì\x0016<÷-Û´Á\x0013ÔÑq)¸eS:¿ôwTþÓgÏüÒã+ã\x0012÷³b:Ê \x0008 w\x000f³K\x000ebt÷\0÷Ë8-J©é\x0010i\çk%É\x0002\x001d\x0016\x001fÏµ\x0010ÈNt3\x0018\x000c]½·\x0017>zõÎWg½g-»uëvÏV>pø¨ý¬\x0015[wÇ¢\x001d\x0012±w ½:\«ënIlü\x001aÎF\x001e´%R¯/îÖt \x0008x\x001b1»äP(&HwÏ\x0005\º®®N\x001eãXî\x0018[ÌDÚA[,ÒOó?Î
säY¬ø"\x001e_¡^¾\x0011ã[ZZIÜX¿-jï]á{ËË+ÐsêLvî`öùÜÛ£7ï©¨¸ÎãYgXgð¶¨m!qÕÕwÑyçNåÎ°\x0015ëvîH¼ÿ>[¶ceÔ\x0013\x0015£ãSëëëYÉiéþ\x001bÃSöÿ8ìs7µ¸¨¨\x0004V ;GUUÕ	ºCgÎ]ÀÈ»wkB£ü6EÆ&?4²#4aéÚíÁÛ¢ó¯\x0015>}útt
'ðò÷%ç/äÞÜ°][X¨g\x0013Ã¢u|½U~1çò\x0006cåXÕÙÔÔ:s/]\x001d4NùÖÖÖbdÖ©s'NM;x¤íµ¿\x0017\x0008 \x0008â
ÄìC¡ Ý:\x0014\x0010Q\7ÅÿSVë¨ÕÃ¢Û]:¦\x0004
¤ÿÄ}>qK#|±\x0005_rùJ>ÆÃHqõ\x000b\x000e\x001d>E=vº³ö\x001f­\x001eÏrYÉ\x0013ª8k	g-ã\x0004\x001e\x0003Æ( ¨Sç,å	6íC'(óò\x000bþ8Ùã+í¦z\x000eà\x0011´%¢sI\x001e=\x001a7Ý\x001bk\x001aWLµ¨±±Ñ}ñzÌÅ\x0014,bú	EPÜ_ÙI8¾¢¡¡!!é\x0000ÏnÑ?$k ÕÆ)ÚGZK9[5þÂÅKC'y®±°\x0011Y	e#>øÔ/âlä2M`À¦pL\\x0013°\x001bß\x0002\x0003Çºq\x0002wôã:zÁ`<{±r1:±¯N>
Ùwý\x001eK¡\x001cÅØLñHÜw¨}"F
U_Î]ÖfTî×ÿË"\x0008 7
³K\x000eb¼ú`fX /vÙ[æ\x001cWâ\x0014[Ò.Ò±¥óµÅª1Ò=}>Ë³\x0011sÃ]\x0011K\x001b\x0011ÏFfÿµ\x0006³GÄìûNî\x000bLò\x0004\x001eÚøT%Áv>~;¡Ð3}xÂ\x0005vh]=ý-íTþ\x001bÂ^½'p_²fÛã\x0015\x0010ã\x0019>0R}Q1VË<}!"5óÉ'Ó3±\x001a4{¹ïöì\x0015Xd[HÜï?õ³ËÎ)(Ô0J\x000e\x0019¾t9ïIJ4`­ÒYX Z\x001a¼~k$ÆÏv]USSSZz\x0013uêÜ<¥ïl×Õãghðj8ùÈD{\x0007â`mPzëîXïy¶j\++«¦Í[\x0001Ø³\x001f¶-dÏµ\x0014È>´W¢ÎËù\x0011iÇkjî¡=|ê·£¤h\Í»f)\x000e\x001c«H;ñàÁáß \x0008 ÌÙ%B1A^ýDÀ\x001b\x001b\x001b5áÇEI\x0015ÎÚëÎ1EíÑ^wÝW½4úä¹ó9\x00166¾\x0002DÔW ¶âß\x00139\x001bÙ]1[P ç¬%ÜpÑ*ÿ]£§yõ\x001dá\x0011¸_±0\x0013zB}1ÀÁÍ'ô\x000cÜ\x001c\x0001#å*¨):a¹<¡
'N;¸ûC>q+[àãVsb"½nSâ±t¸´Ð\x0003\x000cKj\x0002]<\x0008×êÞ·¼o'­ªª®««\x001b4VÑO(Î½tu½Â/©­­Ý\x0015`5rç²
0sh°Ä+\x0000ïjnn¾}»ì\x000f\x0013<¾ÒkÅ¦¯|¬ìTËÖnM¶\x001a¡i\x0002ñE°&`·ÕH5vä¶x=&\x0006l
ÇÄïdß£½#4ÞEåg5Â3'÷
^je+\x0017Lq++¯\x0010Å\x0014*~|ä\x0015~\x0002#\x0005_x\x000e\x0018#C#?¿ÐÊV9a¦w¯ÿk\x0011\x0004A\x0010ÄÙ%B1Aºu(ªïÖ¸$VHö?\x0010§Þ¤ÕSï¡íX_¨ÇÓ\x0015~;9\x0007g#çø
\x001e_\x0001\x001e5o9\x001eéõÅµ³\x0016/Z½õã	JwX´Nî\x001dØ>ÌZ\x000c×åøn\x0002iIÉvÆ
¬Sàþë\x0011ãYg\x0004_¨f8úØNõäÙªçIWÞ¼ítGnðÕ\x001e1\x0018\x000cÃ&«°ø7Î+g¹¬þrî28ÿ,x5Ô½ÏpW¸1JºyóÖo\x0017CÅ!ùX\x001cöû­hõõëE\x0016|	'pë?Jj¥Ï¾òâ	TPåIß,Dó§³Û7ÅW~>k¡Æg3oÄµA!Wó®ñldØæ{Æ"\x0007SÞ»wï/sðì\x0016f\x001c;6^ô»â[·Ë]c®ËÓ\x001fi"²ð#\x000c\x0018#GIh\º\x0002>ý³{KK\x000bªý\x0019þ½\x0008 \x0008Âü]r(\x0014\x0013¤»ç"ãdvÈ¾£!º#»uGp
I>z>÷*ú¡Ï=\x000bJZ\x0017\x001cê¿!Ì/8\x0014	Ü\x0012YVVÎ&¦\x001f9!R\x0007º¨üv%|\x001f\x0014ZP¨GÛÒÖ\x001dú\x001föË5¶©óã¨\x001alöa- mÚr¶JãSAêöa]×©ZW6\x0010´\x0002mF[\x0001\x0011ê¶ªåZ\x0012\x0010-Q;FÔÑ""­h£P.#\x0000¹'Ü\x0012\x0010'q\x0012;íÄ¹'¶sµ=>Oüúäcû$±ýæòÿé/ëõ{÷='~s~~-õÃÝiEÅw¨ìMùÖÊ×w¿÷ñÖÞøóÑ²\x0007å4yüÄ
ÛöoØ¶ïý£\x0019n·f®ç\x0015q!»³³Æä®\x0007düê\x000fï¾¼eïÑôÏiÆãñ|øÑ?6oÿ£OO¹ÿðI¯×ÛÐ`Ûþö\x0011\x0012øÌ//ìO;ùå¿.)ZKzÿ»×÷§¾÷±ÕZWYYµýí£/¿ºÎH«Î_Ì¢\x001aÚaó\x001b\x001f\x001cûätn~Ñ¾Ã\x00197s
xáî=Ç7ýéà´\x000cÍN3gþy~Z\x0006ÎEÇ>=\x001d,++ÿüü
ÓEãô¿I;~\x0006.ëÀ\x000cú¬¦ÿo
\x0000CFg?û.·nú¬Iz\x000e_kýI\x00000.9\x0008ÄëÁ=U¿Øô×ÇVïúêë«ê}ûõîÇVí¼v='.\x0017\x0016©]¶áÂ)o\x0005ÀúL8¾¡@ß_zú\x0002²?	\x0000f1Ò%\x0007AÉ>¾ý~ÿÈD\x0002@££!É¤2ááa?tì³\x0017¿7'¯gèÊö\x001e:ñâæ=Å%wy7÷«à
ùD<¦Wu¸\x0012\x0001UjÊÄe«¯¿øú\x001a1Co#-Ô\\x0012
øJx(\x0010'
\x0000\x00141\\x0001\x0000\x00001H\x001c\x0004IBd«\x0001\x0000 6g?\x0000\x0000Ì\x0000¤K\x000e$!rõ\x001eúôªd\x0013uI\x0000Ì@b*´þù5\x0002\x0000\x00003EKW'%òm
Ï­	\x0000WhõÃk\x0018\x0000\x0000f\x0006ÉriØ5"3²e\x0001\x0000`L\x0014Ö+´xr
©\x0018\x0004\x0000\x0000©,Z²:yT#"Û\x0017\x0000\x0000Æ\x0018Z´\x0010iC\x0016Ï¯\x0001\x0015ý\x0000\x0000 ¤ºt4©¯[È\x001cl_\x0000\x0000\x0018`(Òþ\x0010B¤Õ
­1g_\x0008/\x0000\x0000HbÑUI©o\È\le\x0000\x0000h"ÒÂ¢Y¤E«ý\x001fa\x0010}\x0000\x0000 ¤¸tT¯^
£F\x0012\x001eÙÖ\x0000\x0000Ð¢wiH\x000f)°E³Hë-Z<Ëz\x0001\x0000@\x0012Iwi3F-_½9\x0016ÙÖ\x0000\x0000Ð\x0012S¤\x0007\x00154\x0016-ü\x001fa=
Ý\x0000\x0000 EKVÆ3
çÍ\x00195t\x001aIXd[\x0003\x0000`\x0002\x001afÖô\x0002´PhaÎ]]]
\x001d
í\x0000\x0000  ý&'ÆR
F\x0011Ùâ0\x0001ò1K\x00000\x000fQ+´¡EBû|>²hVhögÖæ¶¶6·ÛÝÚÚÚ¢àRp\x0002\x0000$\x0016.^DjC/`Èl}\x000e£w	\x0000æ!þ\x0010¬Ðj\x0016"íñxz{{I¡ÉYÉ\x001d\x000eGsssSSScc£Ýn·Ùl
õ\x0000ùAC\x0008Ûaá\x0013ËÅËµR
F\x0018Ù\x0006=¦ögö\x0007!\x0012\x0000ÌC?³B³E³B{½^¶èîîîÎÎN²h§ÓÉæLQ«ÕZ[[[SSS]]m±Xªªª\x001e)T\x0002\x0000æ:âËN¯U
\x0016jÙ,||Yüòt(ÊÛ'4	Ku\x000c^
Fâ\x001cé"íðV÷cé\x000e\x0001Ì·Tuù9:G\x001eu\x000cWRÚ\x001e¶
V´
üÏÝ_Þê+oñ>pöÝoê¾ÓÐ^TÛ²õ­]\x0008 ÛÞJ¥\x0001çÍ©ÒùÁ+\x001cÅ¨
uz5t\x001aIPäºt \x0010°öv!\x0008B¹ß>Ê¹×\x0016¸çößm\x001d¹Ó2|»eè¶k°Ä9Pìè/jò\x00154zrë»oÔ´]«tþñÍT¹_a\x0000\x00009(.½,¬ÓKÌè´|\x0013Cf{äÞö~¿\x001f. "aÖ¹tP¤}Þ|{_N]W¶Å}µ¢	.
\x0000\x0000\x0002­KGÑi¸4\x0012¿ÈºáG\x0015üpi\x0004Q%ìÒnØ¥]%Î K7ù
\x001a=y
=·j;®Wµ\)·Ã¥\x0001\x0000@\x0010téÇ\x000eºtDÖ»4t\x001an$Þó@Àï÷×ö\x0004¤\x000b\x000cÌ¨]z\¤[È¥"Ýì+lôæÛûrë»oÖ´_«t^*kK\x0003\x0000 äÒËØ¥U:½*ªNË1dVGÖ
?ª022\x0002F\x0010\x0011C.q\x000e\x0004]ºÉ[`÷äÛzsë»nT»³\x001e:.ÖÃ¥\x0001\x0000@\x0010Ù¥WÂ¥ÄEÖ
O"\x001d\x0008\x0004ü~¿µwTºÀ È\x000cK»\x0006É¥}\x0002{\x001f¹tN]g¶¥õjEóÅûupi\x0000\x0000\x0010(.ý¢ÓËu:½J«Ópi$NuÃ³KÔö\x0004¤\x000b\x000cÌtÈ¥o·\x000cK\x0017;úÙ¥óí}y
=·¬\x001d×«ZþSÞøõ½Z¸4\x0000\x0000\x0008T.½LçÒ+µ.½\x0004.Ä'²nx¸4è£vé;-Ãanò\x0016HÛzsë»oÖ¶óÈuå¿öówkàÒ\x0000\x0000 0tiNÃ¥DÖ
\x000fF\x0010MH¤Ç]Úí¿Û:Â.]â\x001cP»tN]×Í¶o*\x001fØÎß©K\x0003\x0000 èÒßS¹tH§c¹4t\x001aVdÝðÉwé\GàTïJÝ°teB&\x0015j\x00195Núe$!\º¨ÙWØèÉ·õæ5ôKß¨n»öÐqùAÃW·-pi\x0000À\x001ccÁ\x0005¥¥¥úy¤CÑ×*.ýddÖé4\\x001aG\x0012óUMr\úlåà³­+\x000eÔ}7Õ¢Î÷ß©ùíi×¡\x001e\x0012ìImUáÈÌ¾Ïcrs%\x0016\x001egfß£·bLe\@Å"¢\x0000\x001ej
µæ'©MÆQ+©¡ÔÖImHmâ6ÑçEwDs5â&ªg¨Lô]}w\x0013g\x0014có1pi× Ö¥­Ù\x0016wVEó¥²ús%U±]:+eAuéÖ¤|¹§\x0003]îl¸ÌI\x0013ú»¬éë¦ö\x0007\x0006û¥ÐtUW£Ñ®	^
\x0013.Òïkp¦Ðb1e¦F;ctv\x0000\x0014g^øíïhtÚpROÈ¥
ë´âÒã:
F\x0012D~!¢h>UæÓ+´>dk;.´4êËüÑ}iã«ÏþäçwÝ£1\x001fZ¶â¬g4Oã­»Þe¡âb^%\x0004\x000c\x0014j\x0004µC¯Ðú<w¼ZlrÛ\x001d{\x000eS¸MÇÎ|M¢Ð[jÊÏÖÿ^¹ï\x001c9AÍ¢1\x001d=yá&ÍÐ+ÏÐ+÷²qÛgÖ¬\x0015NN{ÒB\x001aS
ùt¼-ÍLê\x0007TLÎ­ï¾¥véâG1\:h8Be¦¬qQv»÷ÎuJâ)))\x0013W¯¨\x0013kô3bQx%j21P¬\x0011»ËLÁ*íÙÍ~\sõ&\x0001a4ælR¤Çbºôb¸4$ø\x000b\x0011Ä¹4ù\x0018VL\x0019S¬Û)**RÍJöüúW2³ïSKÓ!1±DK(7\x0012%\x001fÜê1cÑ\x001a£6ó;Z@
"Å%Ñ¥\x001eñ\x001dTw­j¸d\x001aÍ;°ÐRsI§yS
½åßPìÒBÅéD|Ã¡K\x0017;ú\x000b¼\x0005ö¾<[O.¹tmÇuK+¹ôÅÒúÇpi£\x0018HËtKg:.-
TVl\«®ÑÍP÷C«tuã\x0013ªÐØxà8%=ôÞLMÈ
ï\x00086/Òc.\x001dÒiK¯K#ñJ¢¿\x000eHK­\x001c¬ËEÙ¬MI=CÖD>F\x0011.M¶F\x001eÅ¯ÂÐàÒ1³ãBûÔº¶&­\x001esj\x0010ÿ\x0002¢^'³	sã\x0003S§Ä[î&
HÕû°Óròg¾\x0007h\x0013n7ïFt\x0004û5k7½¶S³<zâìÒ\x0006ælUÙ°\x0011\x001eO¬\x0016ÇÓ\x000c\x001f\x000c\x001eHI	Íè7T\x0017+kµ[i.5Èºôôð>\x0011ë
®IõÞä\x001f¢Áðúuk"~\x001aô6ú	&|&ºÍÃAäß:*á\x000c\x000eSÆLÊ¨.=¡û*màÒêðº \x0013gj35Æ3ÆW­þ4È¼Câø'gæ³\x0002s\x0004¶hó"=\x0006F$%¡_($Â¥§#Ò\x001c2ºH\x0014	³"q"b\x0012ªFoÏXhðÒÆ-kú\x0002\x0019\x0017\x001fKÇÌ/\Óé\x001a5=¦NS\x000bÈo³*\x001cä½\x0014î#M²3NQ¸¿Ü2ú­Ä¿¨õÖRs_ÿ
ß\x000c|\x000fWÓ+«8\x0017Ó!
\x0015{ÿ\x001câïÒ\x001ai	{¦:jdMS\x0012*RM\x0019øçØDo4*\x001eßJ\x0010,\x0013þµ@ëºz½0\x000fÿC"¬°O?Aõ\x0007F¼*ýg\x0012kó;üý²ê:ã¸ÿÀú¶úCëÄÆä63Ú$3¥13¾uN\x001fÚ¶q
»
² T\x00011\x001d©øê:4h#PR\x0017\x0005\x0004
²â\x000b«\x0012\x0003¬¨ñ¥U)ÕZG\x001a_JM3é}àpöÞs/+{ñèú|ç;wî=÷9Ï9ç9çÎ|®´*\x0003`c-£ü.ãuÄsäVX°´¡£QF\x001bGWW2Ê\x000b\x0019·V¬8\x0011³4ûIñ¤~\x00086r¥Ûú?\x0011¤É¾à\x001d«!¼o\x0017\x0002¢ÒWoxiÞwÍfF\x0000°
7\x00000` 4fi\x001b\x0017\x0004\x0006cßµy\x001b.ã\x0000Ø\x0002¦¥\x001dÁ\x001e\x0001q©\x0011û
Å¿\x000f
ÅNéW\x0008aÔ\x000bÁ¹\x001b±ãØS 8Ðo\x0014ÚA×t\x0006\x0010\x0003\x0000bi´ü,9z!mô¥p¥"8Æ
})~\x00147GÑkDÃ/Çåç/\x0014Ü¨NeÜ×>~J$K
\x0013 )êµFço\x0018È¾\x001aÁü\x0016ÉÕµ­øC0ÞÛ³´Tg\x0005ÈO\x0019C^ª¤Ç di[:"Æü'ÿr«1\x0012 OYú©\x0010ô©°¢Çifi¶\x0016Oöç`%ÇYzþÖ+±#\x0019\x000c ¯¿øÀj\x0014ð\x0012À	LûÃý· %0\x0015=Ò+Ñ\x001b´<\x0014P=U.\x000f
9²k0\x000eÍ@b³äí \x001f"2\x0002ðîåý"Æ¦\x0016yÇ\x0011\x000cS\x000b®\x0001Wz\x000bÌ\x0016ç$z;ÌÒf\x001ekPc0aN\x0004ö(ØlÂ,mH%ÍJÍÒ\x0016ñ"\x001fñÕX¤×l\x0017bÕZ\x0003){E\x0006[æ·H>>\x001fÆÊÒfâµÈ\x001eÙbqgJ¤tü\x0004s/»Ñ¥v\x0019ø9zffkñ$\x0010r¥}Á;N!\x0019X6 \x001d2\x0012;õ\x0007D.éº§}E±Øi&\x0008©K¶æ\x0004'AÙE´(SÐ\x0010l\x0005@c³\x000c³¥è;\x000e0À¡\x0018d¸sô\x000b1'S\x0015D\x001ehj\x0018ÍkT°tdò¨Y:rÍiÉÒò\x0008#·¦¦ùªÿ¿"\x001aM¹E1º²J´\x0004åòYñ)%9GÓÌÒl-Ì\x000fÂNÎ²ôü\x000bV|õz¿¨*¸¿½¯îhèÏ\x0007N'mªæ>vWF
´UÜ\x001bèë HÃ síÅÎ³ô\x0017\x0004#À,Ñîñ\x00188".Ü õÀ\x001c\x0002£	#ÇJ1\x0004Ï#ó°2~lE\x0012\x000fw\x0006<G¿\x0010ëBù\x001b\x0007²­9Ø=²&¦øbª3HïÄLjÍÒòô#+'¥\x0019«B\x0004¡+§&sr41\x0016õè#Ñ£Õð\x001f$ùWi¼Z±laoÌF¼²ïË,ÍÖâÉù\x0014Æ,í\x000bÞQ+åäÚ²@îgê\)®¥]3Ü\x001f¯¬Üw¸÷+I
ö8X6 ¬âÞ\x000b¯9ËÒOúOÐ¤°4Åb=5bfk±®\x0003ï K/Ús]UIêÞ*¬5·ÏJ®ö\x0007º]K?²A²\x0017Ö^ÔNVqï9çÅqõ¹çWý\x0006×'<;¯\x000fíÏfuÛü\x0001ÁÞÚ×5a3K³X,V,bfk±®\x0003ï KÏÉ¿ ÄªsSS:^®3Ô2|ÞìíÍÏ{ªÂ-g¬¨¬<4¤\x001d®âØ%]÷¬*ß\x0010ìæ>45åkÉ¨\x0017\x001fÃV¾â­Hó5\x000cÇ,nÿQNåëY~sßy\x001b.k_ÚÍ,Íb±X±Y­Åº\x000e¼,mdMÇÎºÒº
´L,íÞ\ÿ­ÔðcÈª»/xG;\Å±½57­*_y°Ûö±¹ýÅÅoïlýþ
ÿ\x0007M]EUÁüÒ²»ö¥MØÌÒ,\x0016\x0015¥ÙZ¬ëÀ;ÅÒõ\x0017\x001fX!ÙÖö½\x0004Ì½®>Ú§»\x000fîoïÒ1ü*´e\x0003ö´ÃU\x001cÛ¥÷\x001eîu¥¤-\x001bqx\x0007g%Wÿç¿¢g$·Ló\x001cÉÞÞÌ,Í,Íb±XBÌÒl-Öuàbé®{VHöLr\x000bù\x0005_´¸¼=à±sßLõ\x0003Æ\iÝV}¥'Ûe\x0003v,zJnq¥pýzr5N\x000eý\x001f}9©1wG²{yhHûê&ffi\x0016ÅEÌÒl-Öuà\x001f\x0001KÃ_JúKós\x000bóª\x00177§nÙÿnõ±wÊÌr×àUB¦ÿ·eéÉ­Ñ³ôþ®KÕí½äö«w'¬ZÏÝÐNwg×¥S:]\x0019gÆìíÁõ9wõíOï¿ßxê«IµÓÝmØSe÷¶~õªnïÁÆÅRUôeßÇínÅÒUí!fi\x0016Å\x001aWÌÒl-ÖuàbiØ
É\\x0019}3j1Ö²¢&`Ølwå3I#ô\x00056Ãõ9wÕ/××ZuÏm¸e\x0018(cÅÊ-¥{È\x0000t1Êd\x000f¡Ñ6,½»ù#eûlOUÖ\x001f^J­ø ©kßáÞ]\x0007aÊáÖlô­/Ú¹»åxöÒ}­\x00133h<}Ç"M¥Ë\x0003'¥Y,\x0016+\x001a1K³µX×\x0004,
7Óé\x0017Ó[ººz\x000c¶S:Ýë­útÝ3\x000c\x0004\x001fU`³ü¾-¥åx\x0014F7ïî©ÍX\x0000ó+4â\x0015õ\x0002\áQÆæý]('5Ò#Ü~õ.ñH+¦±\x0010+ÞæäÿxO\x001e\x0005}\x0011WÈfHBùÅ+4â\x001eW¢>zT&Ñ\x0005A«Ê_»qûµ,ÿËÞWÒýäWÓ+ÐÙÛ37.íão{+æ¦ùÍ}gæ7²Ë\x0015^¼4\x001aQ1¬\x0005¦%Ë»C\x0005\x0017[\X´S°´¡\x000er\x0010\x0010Þ¸r\x0003®Ó¾\x0000ã©ªúá\x0004Kï¬i)ú°¦¶ã|SÏµU\x0005óÖmj9{\x001d,]´{\x001fXº²=T~èô\x0007:7íÜó\x0005\x000bu}Â,\x0016õ¸Y­Åº\x000e¼,½ ø\x0015¹Ò{¯\x0019}®3®ô+ítú¶Æ\x001ffWÎp\x0007\K¿_3/­Âªo[¿qb`i`\x000f\x0019\x0008\x0004.\x0002\x001d¡}ÍF\x001f]	½@ha¦\x001a7\x0004\x0010ë\x0012³¡\x0011Ô\x000b÷DÑô(\x001e°*X+iPzD~¤]\x001f:$\x0014ñb\x001aè0Êi\x001e\x0005W4"\x0018¦	S\x0012$¤üÁè%'A¤!Iì,]ñUå¿·ÜÿÆªª¬ªzcÔ¸_7ì¯%ïÅVÚü=%
ÇÂÌå9cÉT^j¤
\x0011z¥ØMê"j.´§âJuK$6\x000572K\x0013´Ó@èBÅ¤³qjô\x0007R	N_[ÛùÉ<øÍªµçªöÐ²ÜÕ`é%ÞL<Öµ½Ws Øßøëô·RéúY,\x0016ëq\x0013³4[u\x001dx\x0007Yº 0h\x0003W\x0006ôr¥u¿åÿùº½\x0005»\x000eö\øûÔ\x000ee/ð¹y Â\x001e\x0019b	éJ\x0014
\x0012\x0003	x\x0003G\x0011\x0002Æ\x0004lã\x0006\x0001hÁ[\x0003æÉ£\x0008B&²%èE_´Õ\x0006ÌÓ\x0010TFÐ+B(¸!\Dpqy\x001dM\x001b\x0008\x0013 \x0018eØ=·ð²ÍÆMÌ¾à\x001d%K\x0013¾Âb#D	E\x0001i½(;±´ØbAÑr\x001dð^¢DTOúß1<Ý #m( \x0003z¡%?|ldî¸þ\x0019Xú\x0017¿Z´qÇ®
ÅÊ§ÈÌÒ9ë63K³X,\x0010³4[u\x001dx\x0007Yºþâ	@kñ±7ókInV¾\x0005?,KS\x0000\x0019\x0000È
XEä	^"6Æ£àU\x0010¥U0
G½\x0010Iñ\x0014\x000cÒ³gi1
<®"§HB\x0003Q*	®bþr\x00121´<±ØÛpËYs^9\x00103fNõ§ùUºá\x0006oqµbi¹"\x001e7dAæÂøÃ¢ÃWbw¨JMÛv3K§ee\x0007ûï·ÿgim@°táö÷e\x001ed±X,VXÌÒl-\x0003½57\x001dD²9ù\x0017£Od \x0010@®DG\x0002\x0011\x000c:"Ð"\x0018\x0013aò+Ê#Gð3Þ\x0012k²À`0\x0010ü\x001b¼\x0012i)^p»áQB\x0007\x0013\x0007ÊI\x0010C&¤Ä ô\x0018Ò*#,ÝÖÿ9è×ÁÃ1°\x001a\x0010\x001a\x000bÁü	ªE
Q.4Ò2©8¢&ò\x0016Ó½\x0000fQ\x0007T\x001eÑ\x0017\x0001â¡Ñ.Ê¾¢þ"3Í
û+Xº`Û\x001f¥÷8W°9såÊ£=`éÕ¶­Ûö^Þúßïj\x000cÔ¶­+*ef±X,!fi¶\x0016Ç\x0007K;Ke\x0005AGXQ\x0018\x0004<&{Ì
®Ãl\x000bvI5Jíà\x001f\x0010Á,ÿìè²`éÎ\x001bÿ#>>0\x0014ì¿ôêÝ#û\x0014,Ývévà5½ÞØsmß©Kþà\x0019fi\x0016Å\x0012bfkq|°´TX6à8#K\x001f
:2UPå£íü­W\x001cÙ¸®{\x0013\x0000ôîãÚÏ,Íb±X±Y­ÅqÃÒð¢=×cä±¹Ûú\x001d\x000f;\x001a£à({\x001bÛpKûBb7³4ÅbÅ"fi¶\x0016Ç\x0013KÃe\x0003\x000cÒOËCC±à´·æ¦ö%8bfi\x0016ÅEÌÒl-3\x000b\x0002\x0013à1@8´F£øó·^yØ]óöËî7ë\x000cãþ\x000bú\x0007ôºÍU{^¬rÓÞT"UÊEÕ*½ëFÊE\x0004éEZ\x0011J1Ø±\x0007\x001d\x001cóe\x001b\x000c\x0006Si\x001dê$R\x0010jT\x000f©2ª\x0002-\x00015A\x0011¦""xwíµÔgçÝ9sæÌõØ3»g0Ï£Ü3gÞó1ç\x0004õ··pÝÎ7\x0017tia,¡K\x0013'l>\x0006gÿ^K/fßíýWv\x001f{ÿÒõ7\x001f¨ÇO®ÀÐÙiûÂ¢úºzÿ\x000bW»o\x0019ÁE@S^Ü¾8{y\x0003«LÍ_Ô\x000fJ]Ó×>\x0003\x000e?.Í0\x000c%tiâMéÒÂäµ'Ð­6nö¼wgûG_å²Ö;S³º9ï\x001c<på^Õ¡KC\x0017/}þMw\x000c0_>½·KÁÕ$Ý\x001a.ôçÇ¿Äånx	Ý¥qG¸;iÏ~àöÛéÒ\x000cÃ0YB&NØÄ.­wm=÷\x0010gïKcôòc8Ûzç\x0019\x001cØ54
 ©\x001f^ûL\x000cÑýn×Û(ðÆ&\x0016\x0002\x0002¼E?Þ¢2®s2³ &NU\x001e/¶:\x0016E\x0003@\x0002Å¨Õ\x000cªRVÄêÆÅçüíe\Ü\x0017äY\x001a\x001bSh\x001cü²ó¿è[\x0013Ö¯@\x000e
muÅê<;úÉtia,¡K\x0013'<\x000b.\x0017¯½¾mÁ×ZhÕû®á¯´Å»ð
\x0005âÒR\x0000[\x0013§©QºÙ¹p\x00152,S£\x000coüö-U\x001eyD\x0003Åøä\x0011È\x000cbòW^©½\x0019+>kàÛ\x0001~nÈÉà$å\x0012å:vyÃTWóÄ_-\x001dÝ']a\x0018&KèÒÄ	téô@¥\x0001¹»´Ø4\x000cÖ'§a¸\x0017L¥,øö+jguimÁ×uõ(.-ÅbbÝx+z\x000f\x0015¯ø\x000cCÓ
Y?@4ð
\x0005rhèQW&"Þbà\x001dÝ$]a\x0018&KèÒÄ	téôüjË¯¡¦g.\\x0015Å\x0012µVb\x0006\x001fÇ7\x001fè.

\x0001\x0018\x001aÆÎ½öú65-^)ë6Ê°PùWUoÈ;DÅ	
\x0016ÙC\x00035¢DÐWÄü(p~Ý\x0007ç£\x000cYîH\x001eq8I±eyÄ+üÅÏàw\x0010.ZÝ;\x001a3jº4Ã0LÐ¥\x0013èÒéSÁ¸D¨DÏ\x0000\x0014\x000bö\x0005_ECl\x0019¯f>¹\x0002\x0017\x0012E±\x000cD\x0003ôJ\x0002æ¦:E\x000bJ\x0013\x0015¥\x0001\x0016|IVsâÌ ³FÊ[,$õÏ\x001a8\x001f919\x0005ÿ·þë\x0006
\:s\x001eÞÊ+9O¹A\x000cï\x0004véJ¹§ä-FËÜÿ¿,ï»NÌ¢W²V&õÇæ¯Ó-2k¬Ë0Lþ¡K\x0013'Ð¥Ó#vê\x0004èÃÕIwè´K\x001bòüt¨tzÎ:Î*Í0L÷C&N K§çâÍ\x0007®¾ôù7\x000eW'Ý¡ã.½èB}~JTºk.½è©Ò\x000có.M@&¤ tÜ¥uV*Ýìk%pk]_U;¬3\x0014\x001c\x0015Ú¯'ÖÖMg.äOQiõVÝnÛ¶\x0019\x0016í<¯ÍÛ¶gbýÒæÿË%\x001a¢wÆNaüB&N K\x0013R\x0010:ïÒMITz\x0017xf`xM7\x000cÝÏtiåÞ±Tj«\x0004\x0013VÊBÆ'
7¡ÕôûjÕ·Ý¶9k\[Ãá¾5'¾M&úyªíÛ\x0014gº4Ãt tiâ\x0004º4!\x0005¡\x000b.\x001dÈtàÔMW\x000c½Ó¢¾ªmÎpX+QOWÞì
cúgt{f_Òf·mn5¦­ê\x0017EÒÛg\x0012ÿÒÄ2z3Ãt#tiâ\x0004º4!\x0005¡\x001b.-\x001eY	dr\x001dÞØ\x001a¬¹°êÐP¥\x0015yY³Í¤sris«séØÒ¥\x0019ÆièÒÄ	tiB
BW\º%û\x0005â\x0018±â ³ù>â\x0011\x000f}¤ybsPð¦YT.Æf±´1±À£¨Æ·m*k°Õ¸ÊÃýÓH|»öX¾4KÓ¯\x0019¦\x0003¡K\x0013'Ð¥	)\x0008ÝqiSWÅ­{z"JÙÔE?årËùTéÀÁø¦Rª\x0019üN½0\¥Ù\x001fNÖ\x00133Ys%«Z·]IØjÊ¶\x0006{·)ÏÄò¥tiq\x0019º4q\x0002]Ð%f\x0018Ù¤¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008Î]úìÌñ3§¦NOOÌ8zrêÈôä¡©ñÉ#cÇ\x000e\x001f<=}ìîÝ;9®Å0\x000c{èÒÄ	tiB
sH¯\x0006iF?>ñÏ\x001b×§§P§\x0019)rèÒÄ	tiB
s>==Ë+ËH}¹Ô|àÒÿýÏý[ÿøÛñcr\a\x0018&ßÐ¥\x0013èÒ\x0014\x0004ç.=sâ(þUÎÏÍêÔê5¸ôðÐÛ`td_Ë1\x000cÃä\x001bº4q\x0002]àÜ¥ON\x001dÁ¿Êúr½I½^kQCªµÚÊJcäÀPË\x0015(rOOOÉ[\x000c\x001b\x001b£\uùLi©w.z%sp8]B¥¾JXl]IëM_\x0019ïLØ\x0012Ã8
]8.MHApîÒÓ\x001a««ós³VàÒÃÃ^Ë\x0015(i\ÚjÀ­(ÕÞÛëmÎp°¼ó\x0015O6&]²ËðµV\x0018~Þ\x0019]KáTöá-¥=´õÔ0LºÐ¥\x0013èÒ\x0014\x0004ç.=51Þh¬ÖëõZH­Z\x0013ªMÞ7ãr\x0005J\x001bØ¯ùªìE]Ô.¶J[§¯¦­ýXf
·«\x001bpØÖ>ÇTdù¸t¯YÙ¦3ù\x0004Û\x001cÚºj\x0018&eèÒÄ	tiB
s<2\x0006µ\x0002Þ?40T9oE¢e¦_És`ZúYi8&{Ñå¬óè=Í¢Ø\x0010ë*árzí!Iû\x0016ã2\x001c&òi¦´Ú:Õ\x0019ÙL3AÕÈ\\x0011Ém><¯\x001c¼N_Ü\x0019\x001f«÷Ö:\x0012mÝt\x0007Ë0ë\x0008]8.MHApîÒÇ\x000e\x001fK×êµ&µZUQ­.U«pé!¯ß:ÐfRÑ\x0017mX\x0017Á6«Ä³ÍÓÒµVYâ\x000e\x0013ö\x0019¯·I­è\x0007Hµ?AôDÒ§Æ:5ËTc¡GõVÃ\x000fN2dQáEí¸ÒW&uZ¶d«QkîZ\x0007Ë0ë\x0008]8.MHApîÒGÇßm4\x001aós³VVV÷\x000eöY\x0007*¡
Quµ:>*\x001dIèÀ±qqM²}`Cæ¤UFübÒ\x001a\x0015dKGÖ
e1Kk~\x0019Sq³+Üj)r>¦!\x0007*ühM¶UÚ;\x0013¶¤bz²íèèÒL¡K\x0013'Ð¥	)\x0008Î]úÐ{#+FµV\x000b¨.U\x0003W\x0007\x0006v'\x000eVB[òÆÊ==Q5}¤L­\x0012Ú[Y¦5\ÚXî\x0003ë<ñÙµ!æ1×¯¥|Q\x0019ö6ìÒÉ\x000fIß\x0016]ÓrhÚo\x001b\x0015Ì¶rÌ>|­-Ñ¥..M@&¤ 8wéñ±wàÒós³V.ÝßÛv\x00021³7ß\x000c´*"X¢z¥Ð1\x0003³
4ªâY´Z3­t\x0005"h§Ü¥téh½Õµ\x0018ïÃÇØÀµ]ZÿÔð;Âó±~ß©ÿÒ\x0008oÀXkc¶NÛô·üÀP¿§¢ÿ\x0015Ð¥\B&N K\x0013R\x0010»ôØ»\x0007VV\x001aKÕªÆÒ¥\x0016péþ¾]Ö¢~~|C
}s6Õ9"A_ì¥BftËYçº´eHì\x0003t¶Õ\x0007}ví+a8GtD
¶îXëÑ*µ^}JíØì¿\x001c\x000cëOS\x0019ï´mÉ~ðå´tÇø|âÁ2Ì:B&N K\x0013R\x0010»ôÁÑýpéù¹Y+pé¾=;s\a\x0018&ßÐ¥\x00136½K¿½üÖÇÿÛröþ\x000fGþ-üâÄ[Ï=¼öÄ¹;6^~kÂe©Ã#®\x0012\x0017ê|o\x001dÂ¹Kì0·a÷îßç¸\x001cÃ0L¾¡K\x0013'lbÞþÑW?Ø{ç[¿¹Ä··ßª¥w³íCã/½¼\x0005\x001c>wQz*Wnà\x0011åqëNOµÁK/G\x0019\x000eðI¤Ý7>£¯¢úOþIzö¼wJzN]ø«,ÔêÒøå«ÛÐÞö½ÆÕlD
\x0011T1\x0016Ò¿KM+{Ö\x000b°ÊÇ×ïéÈNr\x0004×KÁÕ´¹8\ëÀ\x001f¥\x0013ß®>ÿ7v ¯P'ö»_ë_$ßn\VwpîÒ#\x0007½á}û\x0006¼þ½}\x0003\x0003»\x0007ú{ûûvõíÙ	îíÝãr\x000cÃ0ù.M°)]zôòãçvßn#cQo=÷ðÓ{kl\x0003ºõç¾\x0007\x0007X~ÿù\x0017\x0016\x0002yF§òI\x0008è®WñG\x0001\x0004SaZ4tåVeh@óPóãþ\x000c\x0005².6W¢¸R#ëÂóñê\x001fýDyþÿÙ/ûß&¯+ó\x000f¸etC\x001a?Lª6(t\x0015¦Fc\x0013c¬¢ÒQf\x000bÕªÍÈ$@A0\x0004â$%$)¥0\x0001!m^Ö5Qì@^\x0008yñh)t´\x0004\x0018I KÉZXÄØ2iH(Ò¤}ýøúúy³ãÇÍCÌ9úêÑ}îsî¹çkÉK9c	f0À'\x0011\x0006øD\x0003Z\x0005Q&",%Ó§\"\x0003æÓ\Ù`Q9¹Eá\x0008Ö5ÜñÔ \x001c1\x000e:È(mùªé¼è°P\x000eBò¨\x00083è3jAiT\x001d\x0015\x000eü\x001659²¥ÙØØØ¦´1K³lQò±tjíHì<&´¨ì¦9NTkÓÝÅGaL P\x0019­£²´§¼\x0002Â\x0012Â9\x0000\x001e^U8ùÕiëÄ<b\x0002êD|¬Õ²4hpñÒ\x0015XRÙ\x001cC\x0001\x0017	\x001d\x0015B¾H\x001c.Ò@ò`H8ÀüA\x0018ë²4RE\x0004\x000f9H¢P³að\x0001 Ã=(øt
¡[	]h\x001eù/X´X´K´\x0002\x000e®×òÅaM¥ÙØØØ¬\x0018³4Ë\x0016%\x0013K\x0003\x001cø"\x000e\x001e#Íò\x000cèLâ<6÷\x0002&\x0001f4\x00060ñÄ¸/\x0006Æ+$à\x0019cÀ\x001b¢©\x0014¯´\x000b<caé>á\x0006<Æ\x0013> q<\x0005KãO1Hse\x0003éS,,d°)V¡pr ZÄµÂÐv4?îûå\x001fF¢nA¥¡	Ô+¥ÅUHÅÒè¤|X fi6666+Æ,Í²EÉÄÒ©µ#qó\x0018iNá0\78à\x0016ô\x0008Ð\x0002R\x0002Ï /<1&Ö->r\x000ctM\x0000\x00067Õ+Æ$¼"Úþº\x0013\x0003¦%\x0014ïSp0\x0015»,^º\x0002\x0003 1\x001c\x0010\x0001>XyÃçV­ñW`íÚt7&áC\x0011È³²9\x0001¢ér2f\x0010\x0004Oº\x001a\x0002ikâLªQ´"ÄÒáZ¬¨mxÌ
HÇÓT\x001dÝ, åfQbÑ11©bi:;\x0008efccc{øYe¥³ïZä1Ò¢²F[\x0010RBL¼¦¹²	ñÄ8Ã®Rr <£±ö¸\x0014tGcÁoúTób_@¬jFN^\x0005~"\x001arà)¨\x0018\x0003`3\x0006EëÈG =<å\x0019¼
à¤íTµÄ-Ü\Ðð\x001cÜÀ¨ù^¢^\x0008\x0003ê\x0018ê\x0012\x001d£\x0016	g!jò$YÍ1K³lQr°tÛðXBxäé¸79ìÄJÔ
\x0008å\x0019\x0002Û^\x00151K³±±±Y1fi-J\x000eN­\x001dQÕ|ï`am\x0000òÖ\x0004[+º¶\x001cêÌ=\x001c\x0014\x0006îßÚ]ÝyGöÕ¤¤²)!4\x0019­Nà%ÈYÇö¢¬YÍ1K³lQ\x0012°tÛð\x0016«\x0016\x0014^[Ûøb~Óíþç=þ§2üßÝÐ$ôäú¦ù\x001b\x001b\x001cÿØuQÊ<\x001d÷l'«¤\x0017Ð7 MÒ fi6666+Æ,Í²EIÀÒà^-S=[2VÜ²ÆÛZ\x0018ÔÚâW^\x000f\x000b2÷·WüÄ¥\x0017Ý´¬^³½7\x0012ÎÒ{\x0002£¶×\x0015·¥ÙØØØ¬\x0018³4Ë\x0016%\x0001K/,½©eªy»\x0006¢r§²ÛsÝèëÛV\x0013c¨aðQçë>\x001a)ª
<u\x0001W7Û]o´®ß×&þF+f0?Ã}E»veÅ-ÛK[ÌÒllllVYe¥uy\x000c,íØØ÷ôæ\x0014wã¢Í?Ì\x000e
cÒ³nß²­¾¾Ï¾üÉ\x0016ßô
\x001fêF¨¾tßv¸Jby:î\x0019±ôÊÂ\x001e#ûê¼Lß3|\x000b66þ`OhþFß÷³»¯j×Îò\x000cÙ^ZÜbfccc³bÌÒ,[4ÕYúÌíÿéòØSù\x00033]í-\x0017Ûæ[¹Ãÿ¼ÇÿÂÎ&@5ØláæqÍÍôãÓË{{t#\x0000öl«$Vvó]#¶(ÛK[\x0004K_.MRzÙ¦ÝýÎi0ìo\x00064,¥­\x0017ík0fi-ê,]}é¾.PÍÙÙ?ÓÕöÞ©¾_\x00155¿Zrâ×%'~³÷$¸úg[}ËBúi®omqKª\x0001K\x0003öl«$³þ\x0011\x000c§\x001fþø¥ÝMMôZãò<?ìçÛç\x0001îDO¤w9Ü\x000e÷Ñr\¯l¯.>=\x0012,\x001d%E$íôOÚv\x0013
8\x0019¼M7	ÙâÝ2"ÒT¹'\x0004ïCâøU¿PA\x0011µÄø{I¨ñ½Ë¢1K³lQ²²ôÜü®Ê\x000bs2üßÛà­hnOh^¦\x000fþÎ·¦¤YzòZ;b\x0004Ã;ÿøuå­¬¸û¬ñ6ÿ"¿iõ®¦U;^ØÙ×o¦wÂÇsÝhyÛðíÕÅ'fi\x0003K KÇ\x0012'iY:®½tåI\x0005C'\x001b9MÌ :ôøt©§9Nt\x0018²ÅZO¢Òþ5([\x001cÆ,Í²ES¥\x0001Nº@õôîªìx[\x001eßðáêâXYzï¡ª·jê¡¼=íþf\x000bn\x0005>¿ûNÓé8\x0016öþõç¾ü/Ò®9Ñ{fø_G\x001bÛ1±ùª¯¯L´×ühâîv8;\x001a\x0014µd¹öØ­\x0008GCÛU·ô\x001e¸]s¢§õâçUÇ»ÌYúXÏ§\x000f\x0017K+ô\x0001K)-
q¸´êµ!&ß\x0015T?ª\x0002j¯Ü&\x001cG«¶W>ùE9ÕÛ©³
~r:SÔ@©Ó\x0010íZunÓ\x0004ØIÛê¦d\x0014-*,'¥e\x0016}\x0018L¿:
¡ú\x0005'Ë"Ýüv°´µm\x001fycfÙ¢©ÎÒ.P9Ü\x0003s3ý»ªz\x001d9×ôå\x001eÄóô®^×géêK÷U\x001bålÛA\x0003@©\x0018\x001f?×/\x0013óÇÏ
\x0010µè\x0013f0W\x0001N2AÄ.\x0008Hh\x0015$==x»üè»ò^\x0002üðª"4Ú\x0017\x001f\x0004\x0019b\x0006óPé¡*\x001e%@¡0¹9Gö\x0011{É\x0003
HõÊ)Ë¥W\x0016öüxÏ}u^¦oáfß3|Ogù\x001c\x001bûp¦Aå\(K£¢½J½ò!Ê\x001d£\x0012Ä+\x0015ò~÷qoRõV©ÊÔ6Dî§ê|U¿\x0001¸yË\x000fÂ\x0001Ïî´^¼±¿ºþìßÿÓuí\x001f`éÎþ[
¾Þ¡¯¥ë:Ï5üé\x0012Xºá+î¼Ý5íg\x001f\x001a\x000eÒ ÄÁ\x0013biiÆï\x001c'GClÖK«&\x0012Ý%Á|u¨;\x001c/\x000cÌêü)[ÅI_´¯ÕoH<4R
çk\x001c-v q©\x0015az\x0019ép@yÞmE÷\x0011º/g\x0013åî ½:\x0019%¬Ai+,\x001d½FM\x001a\x0011«¾jnDÚdÙb6fi-J\x0002í½¡ËT3Ò»=Ý@/\x0003¨¯Ïp\x0019²tÛð¥£jO\x0006²@h\x0000Ô¼=à.\x0002l¼*nÀÑ~zÅ\x0000\x000e4%´P\x000cÒÒÖb@¢-( EÀ$\x0018\x0018¯Z¦xÇ°;\x0006p\x0016ÄHñ\x0011AÐ#±4Å\x0014,1¥}¤þdÆ&7UDÉ`\x00060©a?-§P\x0002GEd¬\x001báCq¢
W\x0015#\x0018®ûh¤¨6ðXÖ´âõûÚ W^oqd}jÐ¤%\x0007¾ÐîB~»ÎUÑÐ* Vô:FÕaLUs¤^W|Â\x0000¨\x0011ò\x000fÀ\x0018qTþb\x0017Ù_þ
À§@ai4yõûÄÒþ³WÞ¬:³Þwð]ÿ\x001d\x0005`éíEeûªê·yKJ¾\x0007ÎVX:õÕuvÿw)\x0016ñï¯ÍÆ,-LQH\x0013;Kk'MH\x0018\x0018Sdm¶ºéé6Dg­Ñ¦!VDÛÏfÑÌÍü^@°'ÂEmþ¨ÔDé\x0002\x0013\x0006sÝÛÁ=H3Ô»ÎDÜb4W'£µ§,ÝX$äÆÒVj3×¹:îË\x00161K³lQ\x0012°´³þ.VÍtuä\x001eî4G¯éëÏ¼XÔ¥\x0007k7"¸\x00081\x0003¦"ºÆ'ÌÐ$¨I0ñ\x0012H0UL
 \x0012äIüì-?(³:@\x000bóxªXZx\x000fáI,]ßsAÎVÅÒôªeib?ìH»à°oÕ4\x0008¶§Ìáy¯B}Z¦Wð*Ü\x0004¯FÕ··\x000fÅÇ\x0013§ãî^ÁHr\x0016×\x0013U	ÔL:G<é¸Ñdªú\x000eÈw\x0016:q8ãO¢í4ÀNJu4òF,ý¶¿³wè+°t×µºÎóyÞ¢\x0003GOõßÊ/;è;mÙò\x0015vÿw)f¥uÈP1Dh\x000f\x0015Kø6Ä Rm\x0010Z-Å¿¢E37S¶øÔ°:\x001dÖ)PbþtØÈ!Ê-Æø\x0007&åb4\x0013âtJç¦Ë´qÔh¹úæ8ªúõ°MÈ¥Y¶(	Xºað.V}ËÕq¨éüôô^]}Cy>¹þxZY@»\x0016|®ËÒ\x0002Ì\x0008Æ\x0014\x000e\x0002*8-*K\x000b¸\x0012ð¬eé\x0002\x0005Ø\x0010x¬@aW9\x0007ÁÒ²'ð\x0015B\x000e\x0002\x0011cgiÔ-\x0010\x0007n\x0018#,âÀAÅÒ´\x0011>ÁGÅÒ\x0002û±â¨r6RjíHÂYºmxL»\x0011Ò¦VªXZ[-KÓR[¨|ùv\x0003a^Pºh;­Â^\x0004Ø2~SÛ\x0005Ã\x001b±ô\x00077ÿÝÙ«ÒwÊ\x0005Îrç¾ÓÜýöË÷5ªì\x000eãù7úºô\x000fØ7¾ó]\x000bû®oXhqÄ\x0016wëº\x0016ã*Ý¤´1Ó´\x0010Ó\x0006\x0012GJKf ©q#²Ù	m$ëîD¨¸4¶-F±fÝÒ@µí>sÌwÎÜ{gæ&wôÜ<\x000f\x000fóã{¾ç×À|Î/~{),\x001d\x0010\x0018aÂA\x00030jý­P§Ñ\x0017R\x001d)bé¨còd,\x001däikOhÑÕ¶·è´Üi8Imç.Ö9\x0003\x001bûn-vEÑîX\x001aß\x0001K[\x0017ÎÒÛÍãF¶cé\x0016­]dé\x000eï/çåØrmR\x0012¥e/î\x0003÷¹\x0017CV¯ßüúÛ¿ÿÖXù\x001b?¹\x001cëý?¾üí]ùòëó	Ì\x0018Ò\x0018\x0018t®tåÄÈip\x0017)ëBykØLîE;\x0003±À±ø£\x0006\x0007÷\x0007ÀV2veBBÌ±ã§®R¥ÉÞÄ\x0017 Ç¬Z$\x001aGÆ'Ñ)\x0008lDÊ\x0010K£Ìe\x0013\x0011¡øÞ\x0007X\x001b
Ü\x0011\x00020Ó\x0019ZsÁ.
Úö9$É­µz\x0004íØ¯»\x001f;\x0011÷È4âeu¬~\x000e.åÚFì|°wÜ8Ï'\x001fl\x001féN£ÀÛ\¼\x000bÄ×ÏªdSØoÀÞ>öÌ	±tùæÝ7¾?ô«Ùkdéßymúò{?üé#?x\x000b,}tèíÂüûû¾yÐ÷W]\x0001
Ôè.ßàzã@.×\x000euH\x0012[³Q.,7\x0013^ä	YÚMÄ\x0019:\x0011Zhµ­È5ö@Âc#á\x000eN5#[­ÃãZeKÈÒñï\x0002^¥ëÈÒîJr\x0003 £¯m½\x0012¾bÚ³týY\x0016ÞiëmµIºÇð\x0011u|5\x0018]¬XbiÙû¥Ï¯<í"\x001d½ô8ùÔ@ ù5B\x0014\x000coåÐ\x0002²²!Fà.\x000cg\x0006\x0012©ÛÛÆ¡Hd\x0008MÊF7³£¨iËcZ\x0006ã.NÁ\x0018w×ÑE2&!HÓû.<ìâÅÅ¾Ü5»[=1÷lí¾B××ÑÑë¼{P(0à£Çÿ?üì\x000f7þ{óÑ>øûók·ï\x0016?ªÜý\x000c,ýîÇ\x000fsméêÖ\x000bW®¥Ï¯¥\x000f|÷{¾ÿ»¢ê@rR\x00125c\w´Õ»`ÊÐEÃ¸Lãõ\x0011ÄFB·½Õë(É;(á+¦Q}yEø4ô^{ÞÄ³tÒ=6-#òêiôFÎ¦Õ´R\x0012¥e/î\x000fî"}éÄÝë\x000fv²$°Óðø$<65|\x0014Xº+ÛïQ~qà]¹¸\ñ÷í¤t¥\x001f>»ñàß\\x0002þÃß6¯¯ýsñ/¿ûçG`é¹êÚïn|,îOÉOGZ\x0011Îªzf¡ÙXZöâ¾ai\x0000ð+ùOÓtéÎ3ïLµ«|~åizÞ{æ÷¤·XZ
Pj` |:Ò.¨v²¹Yß«è Ütö\x0017e¥e/î\x001bßùä9`8
.nz\x0007ª]h\x001c{[Ã\x001b
/)ï»Hï~aiI$?\x0012KË^ÜO,
©@V;à1@øù§Þij×\x001a8½³wÐÞ3÷ú\x0003¤«biI¤t\x0012KË^Üg,]
p:W|´]\x001e+Ýyæ\x001d¥v¹q\x0005Û}\x0007\x001d½ôØû²»h±´$IR\x001a¥e/î?¦ßùäù«çîw±¯üuòÆ¿¶ùâÒíB1ÍÚ\x001d?rw«\x001bcSÓà«\x001fýüÛ\x001acý/âÀ»åÑÅM\JÇÛwá!®8aÎÊêF]¿i?XZ$)ÄÒ²\x0017÷+KÓ×\x001f|\x00016\x0003Tï=sÏ0ìü§¨¾uõ\x001f¥;Ï¶
H6Q(\x0015æ*dé\x0000ªK¤#tÁçJWX]Z®\x000båEw8\x001a\x0019@fÕb´%$q¸ñ!¶ÌmR¡\x00171\x0018Å0V10\x0014ã\x000eD\x001e[ÞüÊ\x001a'bo(²ëÆÕ\x001c½ô\x0018×är5ª¸J\(®u[Ù°ñI,>tæ\?Û±AÆ¸×Ø)7Ë.Þ{\x001aHïÌÂ2
vVî­¡.|\x0011)86ÖbiI¤4\x0012KË^Üß,ÝE\x0003ÀÀÀª¡áQ°4\x0008\x0005\x0003c´\x000cO¢zøÈ¨²a\x0001 ®³Å2X\x000c
a\x001c\x000eÖµx\x0004£/Ñ\x001d->ÄÒL\x000c\x0008F¯;ÊR1ÿðås\x0000\x0018è¢£åAÕ²±Ê5Û¦¢«Í²¹\x000bÜ ]\x0001\x000fÇÞD07å²4\x000f\x001c_qû\x001bà¨á\x0007\x0007÷ó4,\x000f\x0018\x0001x7~\x0018\x0018>,$Iza\x0012KË^,Nhb¤[\x0008´\x0004:%¡½ZgN\x0012Ôò¢],²^{ã\x0018Ã¬â2
\x0016r\x0000r[\x0001Hò.K\x0007Øv
]ù©i®;F;«\'ç±\x0006£G\x00140\x0010I\x0008{Ù,¸,\x001dZ-ZPö~AIîÎ½j3K[Õ=4·GK·o
æAËÈødp­§,,4c+¥%IÒH,-{±X:9\x0011f\x0016ADø²Êo\x0008£@S4--\x0003Hµ\x001a +bð\x0005l³
"Q \x0006[|¨ÈM<sY\x001a\x0001\CTdl®\x0016\x0019ÇDh6Vë,ÍáÆöÕ\x0008Ksï±SdÙ\x0006½î\x0015ØÝ\x0001³4«8\x0007Ü¬U]&G;zíúv\x0013KÏæ\x0006öäou;ë­ü¤i_Ì\x0002$Iê\x001d¥e/\x0016K'7¨2?5
\x0006& PÀé"\x0013 
'V\x0019a,\x001aIÑA< ìÊ!.\x0001ÚÌ<Q(¡ËÒ
 HØæ("mù\x0011\x0000ÌêÈød(\x0006½[\x0000a"ÏÓÜ\x0002sï±«Í²íÅ\x0005»°Ëâ~Yå\x0001º÷Umfiþ\x00060XF;Ï\x0013ei>¯ì©âºÇYz³F³ÝÙQq·XZL.I½*±´ìÅbiYÎ{¥77oÝêk\x0016fKR¦%½X,-Ë\x0019qO³4(sK¹ÙHÏül~OÐi$\x001a¯årúÚW\x0007Ü.ÃW\x000bhàeÎ7@·Þ\x0018\x000eNÄÂbiIêU¥e/\x0016KËrFÜÓ,]W6\x0003jf[
q£½ÊÖç&
hJN\\x000eð¹AÝ©iH\x001b\x0016còfàoÔ8eø9 Ð$ß\x0012KË^,å¸·YºA­hy«BðÄÇòóf3KGP\x0015\x0000Ü;¨Ô©¸	t\x0013¬>ÂäÑ-Äâr½Q,-I¾%½X,-Ë\x0019q\x000f³t
@
EÛ°t=.&¾»,\x0008 ;äÙl\x000füm\x000f$ùXZöb±´,gÄ=ÌÒÆ5²t½É(7&~G,\x001d$7(w·\x0005ÝÆæØìÈäqÀßîù I\x001f¥e/\x0016KËrFÜÃ,Möära°¬ñ'Zî-úoÂÜ\x001a
oE·gi\x000bE_¾\x0019tëªO¹Ù:G<·\x0007þhoËä$½$¥e/\x0016K'÷Å¥Û#ã3\x000bË(TV7P8[,£½0WÉOM£Ê\x0018t±UÄ ó+k(+]YZâ¦ÅXfF\x0015]\x0019^|1\x0005Ä Ë\x001dëN/Sa"rSÉ\x0019w/³t\x001bõ\x0008bÆ0yÌ\x0003ÁüHolTúXbiÙÅÒ	
.=vü$
\x0013"\x000c=|äM0*
¨¢}hx\x00141ìBÁø\x0002kÑ^V1\x0004¸Ë!4\x0013²\x0017Ã\x0001	Û\x0010vÙ,ðlcCÓ¡)¬2²!§÷\x0003;Z,-IFbiÙÅÒ	m4ËUfÏ\x0016ËÖUuàÃµøÇ¦¦-³
aÁ¸×ÐÝÝ\x0012ÆF§«\x0006à\x001dNÎ¬ÅÒ$Ii$½X,Ðó+k$ÒÂ\Åei 4ZP@/b\x000cn\x000f\x001c<T­#t5ÀZ|Gñ­¬n0Æ\x0010f\x0000E#\x0003b8<ÌIg\x0016Û³´MÇv\x0017­ÍNÎ¬û¥%I^ÄÒ²\x0017¥\x001bX\x000bÜÅ\x0017\x0004\x000bè%\x0000³\x001d\x0000Lè\x0005µ`\x0019Y
h½\x000cÆ\x0017e\x0018Ã--²¡«\x0001´3\x0000Ì^ãmÆ\x0011ìNg½ýÑéäÌZ,-IFbiÙÅÒ	½´þor4\x0005èv\x0001'\x0013å]n±´$IR\x001a¥e/\x0016K'7\x0017Ü;³°|Ha®$meuÃûîdï\x0016KK$¥XZöb±´,gÄbiI¤4\x0012KË^,åX,-IFbiÙÅÒ²\x0011¥%IÒH,-{±Xº+þõÕ÷í\x001bòÅ¥Û;ËYYÝØñØ6.ÌUL
{?ÕÝf±´$IR\x001a¥e/\x0016KwÅ'FNÛ7äBq»Ù8äE°ôüÊ\x001aÜ1L,íÅbiI¤4\x0012KË^,NîÂ\ex|2?5]
 \x0014ehê²ôÌÂ2ÚGÙ\x0002«KëOP\x001d'
%&d\x0015àÊlhAùØñ(`8¾Õ\x0000­\x0019Æy9Ë0Ö\x0002Fáë"1º0Ðb¸\x001d´¸s±Ls"Û2ÖÏ)°AïwÑ\x0016KK$¥XZöb±tB\x0013wQ8[,\x0013\Á0¸·ÚÌÒÒK·A³(\x001c>ò&«àRP(\x001bQF\x0012½\x0006ÞÕ\x0000-\x0003\x0001ó"3óT\x0003Zvep=Ìpàà¡j@õLEÛ	ö\9clµ,Ó([#Wë.RîºÅÒ$Ii$½X,ÐF´ñd,KZ\x0011` j$UfCU	çd\x0012²ËÒt« _7-=8¸\x001fùa6W\x0015Z3¨1°u\x0001ªÿÏ~¹\x0007GUÝq¶ÖþQé_ñ\x000fµ
:Z´\x0016\x001d|\x000cè(Òò\x0018¬ò0:¶ð°HH ò6ð0´Iå\x0011y\x0014BMB\x0008  @\Þ\x0008Ý\x0004HÈ¼¤	Pòbúm~áæìÞ»7là,øýÎgvî=÷w~çÙOl\ÚØ-®¹\x0000ÿYhÿÜ~Ð¥\x0019a\x0002	]h.í'°Gñg1LH/,\x0014ýª.
eÅ'WìTn1eQÚ\x0006CYa¼ðgCVÑ\x0019ýÑÍX\x0002×R2c\x0010R-ë4¹4ü\x0016SÐDÆ-]ÚØ3VÇ§Ô`W²\x001c\x0004ªK\x001b­îVt]6¬ýïr;Af\x0018	$ti¢\x0005º´ÿ@¡µ¢¢Ö\x0000Û\x0015w\x001b°SÃ{ÅåV<ÖÙì¥X\x000c:]\x0017}p!Â\x000cG\x0005\x0018ÁB(À¸+Za±®LG\x0006ÒA\¦H±Zæµg¬";1ô\x001e`P\x0010-Ç±´üã[Ô¨'\x0005]a\x0018&Ð¥\x0016èÒDTÙrÜËØÉ
.Í0\x000c\x0013HèÒD\x000bti²ãÛ³¾Æ÷ÖhßÞ\x000f\x0007º4Ã0L ¡K\x0013-Ð¥		\x0012èÒ\x000cÃ0.M´@&$H K3\x000cÃ\x0004\x0012º4Ñ\x0002]\x0004?Ërk×\x001e¿ª}\x001b7\x001a{ýÇÍGKèÒ\x000cÃ0¾B&Z K \x0004æ\x001cUÙ3¾èçÑù^\x000cø¤ì£¯ª\x001då·á×ÆÞ¥\x0017¯ÿÊá®¢K3\x000cÃø
]h.Me¹µ}\x0016\x0015ÚÌµ\x0015~\x001aõªmèùÜ¼r\w{¸\x0007>w¾øjÈÇû,ng%¯ÂÈ«!a¸\x0016bæ.\x0002ê-ê_\x00194´ï !²`åzµ³QfåÌ\x0005è \x001bP;c$c¾lC\:}¯ëÙ\x0017úõxò\x0019¬\x0015\x000eþË\x000b\x001fìöØÝ\x001e\x0005)Û>ûâ\x0007\x001f¹ÿW\x000fß÷@÷§y^÷o\x0017Ã0L°.M´@&A\x0002ÄxÀ'eþX´Á½1'csªÛì\x000c¡t^wiH¬ÜB°ñH4[¼W¦ \x0000v­v\x0010\x0013ÆEäÔ8u\Ê ÒF=\x001aB?ÉÚáÕ\x0013\x0017ÆBjs4¥£¿¸ôà7Bg$®8XÑ°|ËþÐ±\x001fKO°ótµÃ]Sp\x001e.Ýoððl§;}+4"Z÷o\x0017Ã0L°.M´@&ÁÀ¦ÂúñEí\x0012i\x0011k+ì»\x0002Ãlq-®+×0a§É¥èùÜ«!#@Æþü]§/B{ñwo\x001e2µ3\x0006cæ¦ ldÔ\x0014 -ÄxVò*qué)}dÄiritÆ\x00120ðÍGËàÒ¨w\x0014~¿éHñ¤9I\x0013?J\x0014îÕ»ïÀ!o\x000fxýíO·\x001eK?úøS}\x0007
{iÀë\x0003^\x001b®û·a\x0018&XB&Z K\x0013í8Êî9Ù1\x0016/?cÓ_Ü\x0015¾
Ë\x0015[ÖBwå)\x0006Å«½\ZÕÝ-yåOÌôªaÂ(Æ8|[:CGEÿ\x0015­0"=ñ©NT]\x001amQ\x0000\x001bÏLZ	FÙ¢ÌmÍ.øP÷_KO°ótµÃ]Sp\x001e.Ýoððl§;}+4"Z÷o\x0017Ã0L°.M´@&zH÷/
D¤Í\x0017|-a¸käÔ8±e@Yg/ú'¤\x00172l©.
¹â\x0005+×KýÇ«²ÇM7êV\x000c Ïè\x00003Ç8\x0014]&\x001a=\x000buÖÈ¨)@dûACáÒ\x001fÄ'÷\x001d8dfÒ7Fíñä3âÒ\x0003þqü¬£g.HÉÜ\x000e~êÙ\x0017ÆL=zÂ´\x0001¯
×ýÛÅ0\x000c\x0013,¡K\x0013-Ð¥^ÂÒ*\x0002\x0017iaYn­å\x0012[òÊ¡µÎf×$Ë ô\x0015×\x0000Fù)¹Æ\x0008ÊÌ[(±Ñ\x0001R­ö4æª³Po4OK\x001f:×4oùºIqIÉ\x0019_Ä§¦Ã¥nÜ=avB³KÏK¯q\x001cyoÊGc&Í\x001a=a*]a\x0018Æ\x0008]h.M4²©°¾³D\x001aôYX¢ýD\x0000\x0016>t¶ñ`EÃ×ÿ©?pæ*\zOiÍîâK;OW;ÜU9\x0005ç¿Ì¯ØWít§ïsFDëþíb\x0018	Ð¥\x0016èÒD#°ßNti\x0010S­ýP\x001d.Í0\x000c\x0013HèÒD\x000bti¢Mõ6V|GÄñû&[[×¸« æK×¥í'.\x0017UÖ546Eüë».#ù\x00059×~®\x000eCf\x0018	$ti¢\x0005º4ÑEÌæ\x000b6.Ý5úÄÀ¤b|Uú'\x0016w^pg¸+ê³3¸­N¯-·è(¿U¿Qtia@B&Z K\x0013]ôO)³QâÝ\x00055»
j6\x001f»}äâáÒ+îÊºÜêÚº&|sðý±\x0018S­ýh\x001d.Í0\x000c\x0013HèÒD\x000bti¢î3NÙ(qá¹ºßÄ\x0016v\x0019×åOGß]ý|g-.ý}b1lÚfbdV¥ö£uãÒãzu¹^q;å÷Kzeøx\x0011æÏZÍU>êüëà«eK°¿ö÷±ÛÕ-ÖØ¼\x0004Ë?d^¾òêoýwÇÜ:¡K\x0013-Ð¥.l|\x0018\x0014½Ú{~ÑÝ®»"\H)ù¾¶±¶®©ðÜÕ\x0013\x001a®ÙL\x001cöé\x0019íGë\x00187Á¥ÅpZ\Éã& ´Ã¥¯ÍÒÁ§u\x0005âÒê´vöicW·N<\x000ers\:®ÍÅ\x0018¦óC&Z K\x0013]Ø»tá¹ºçç\x0015ýx«ëøüEøåÄüÞó.^i|kYi}cÍÄ>\x000bK´\x001f­cÜp6RgN\x001b.­Ä¿ûß¡=	ô|7fW\x001aâïA:ÿÀtiæ¦.M´@&ºðÇ¥\x0012îº'úÄ=Ñù?\x001asüé§*/7\x000c_\ÒÐtÍfbÿ2óZQ\x0013'GM\x0002Öl;`³¥ÏsÝ\x001a_Ko8xrqÆÖNti³(ÉÈÿMGQ\x001e2¹H}Ø:EtYq½¹òÄc\x001f\x001e}0n^ÔØw©ý\x000eM"×>æ\x0012óÑZjÔ\x0006æ÷Û:¡õ}{¾}\x001f§P\x0006½Of~äû=x\x001fD}+^}Z¶Ô«åË·\Åâ5y¯|\x001bü3ÂÜ*¡K\x0013-Ð¥.ÚåÒw½çz|VáÆ%¥õM6\x0013#³*ÍkÁ¥åâÝ÷Æí-­Á\x0005>åB[£\x000cìøö¬úTíæ5·M¼êÕÎjêÒ_º¾ÛYTµ5¯L\zS®Ûpé¹EY\x0007OvK·jµK7Ê\x0004ód\x0011ËÖºæKe°uÒ\yÞÖÞ,·×bg,Úî°Ú$ïíìãÑÒòh­Blòvû´ù=½Ûâey<²\x000f\x0016\x00071«½Wg«?ï}ZmÔúoÊ072ti¢\x0005º4ÑE%þ¸t×ñùpé;#\=f\x0015¿Ü08¹¸ñÚµ\x0000]:5{Ç¤é±Óçþ-!5
sâ6ë+tÄ¨u{ó\x0000êñ\x0008xj\x0014\x0003Ü.JÛ õk¶\x001d\x0015£\x000c`¢±Öç¹n\x0014H%jLG\x001fÙ	ê±
u{¸mîùaæ£»¿Ámìß\x0017§ï<<oñª-GK"¢ß± iúüD»jÞÕSæ|\x001c\x001e=iáÊÌÕ9Î\x0017_zÙÿ_\x0019³ÛXê®× GÉª\x0015\x001bS<TÙs´}.Ýbh×-ÍþÙîÐãT^\x0003þõQwe}4­Z¯×A¼w ü+â¹z\x0007TÚ÷{°vi>¦\x0003{¼|ËU|oT1o¹I¡K\x0013-Ð¥.ÂÒ*Úté;Â]¿\x0018ß5:ÿ®±®ÇfºR×tðtíÕú&k_5¯\x0015\x0012ò&$\x0016ÀlÍº\x000b
NÛþµ8¶8³óºrã\x0011X·÷XØÈÑæ§\x0010]<\x0002Ã¡ßêrj[cº\`:ÖE(½WýË\x0013§}\x0008\x001ap°¢A\:k¿küäé\x0019{òÒw}ãpWúsêÆK²v½\x0013ñE»\Ú,²­®iåÒ6:W}#]ZjÌ\x0016gv`û\x001dúïÒ¾ú\x0004èÒ\x0016\x00071¶ÑÚÁruó?>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=<<Ac}¾¿:k»º*Ë¯d\x001bU p8¤\x0010@1Uó£T|·\x0008\x0008²J±·Ím9ü<\x0014I¢n\êFD\x0001`\x000eQ\x001dÀÕjÿòþåß\x001fßÖ³Óvµd\x001b5¬}\x001e	FVr)%Ý)«\x0015)3"õ\x001aq\x0015\x0001\x0012%\x0000EËçµ
m\x000bud«¬æ4\x0010\x0015óÅ\x000c ÜÀ\x000bh»Ì Ë\x0005J,Ô
+toVä\x0013×\x0005Ý\x0013\x001aáEßIN¥d;¿Iùroº~ú\x0007*
o\x0002 \x001ex2\x0002áP\x0013A\x0010¶fiôèG
\x0004>dqO'eýð@\x0015¥Ä¹o$#î\x0018&ô!*jªþ~pÄ\x0010\x0000 \x001c%gÚgËûç\x0017|­<<~~~º½\x00184\x001c&5Û \x0016,O0GLålT\x0014O0A&5\x000böñl\x0000
ÉCàýúnxrÞ"ðÅàåw¼¸ýþòýîrÔ©ØA£òk@o[þ$ñ"eEw<aº­O2ÓÃÉ
\x0011\x0000\x000b\x0010¨9O*@üÓ\x000f¸,â2!#ÌûE"\x0001EºÂøÈ\x0006\x0014ÿ'8ÌÖoE N\x0004!pís5«¹íñòîñþfÞo8:\x001eøPx\x0016¨»Dl_\x00088?:\x0013îÄ4\x0012è\x001b\x000b\x0011¢Âöíþ` \x0010z\x0006ç4N\x0017\x001b é·ÇûûÇ§Ç»«IÏÃIãÒ³Ý¢\x0013º"Y¥à	ní61\x001ex\x0004H\x000e\x000cÃÄáÙ¶\x0003½Ü;¿¾¼_\x001fW-Ígê\x0016\x0018Ä¯t·¬;õaw5\x000ef+p\x0018\x000fÃ¹d¶\x001füueI2à3²ÂP	¾¤x\x000bT¾øF\x0013&º\x0019\x001cÔ|¶º¹3_6\x0014÷­E=GÜÅý%ö$6Å1lx"ij,XªÁÒºò<Ñ jz½Érsÿøp\x0007r»^÷\x001bÅ¼ÄSÚ¤d\x001bEÙ	8\x001e:
ã¸m[ #â¶n¢Éd2Û«\x000bÚAkxq}³Z\x000cZ.<¸\x0010bæ}ÓËÊdRê¢q PëL,Ø\x00079\x0013Häó«+/q£Ñ\x000fó¤ox\\x001aÎp:\x001dÕl-6ò¤øÙñ·Í
Ì¿-éIGÖÒöÓ®ËÎJàMu·Ù.×ÍÍúzµ¼O¥"p\x0001mv³M`þv ÈT<\x001d!QãDsÏD:O&`\&8e¨ZÕÞh6\x000e»O¦ý N+k&M9UãÏ\x0011¦$Í©vû'Ý:ù\x0003F°I¦7_!tÆ\x0004Á\x00012Ëæ,¯;8_\^^,fçãQ¿Sw
d\x0002½|>W>t@<iSÄÛ\x0014°5fðX\x0015ëÝþq§ê¾¿X\x0001\x0015ß\x0015|ô)º]®Õk\x0015§\x0000³Þ!81Nu¿¬\x0018e\x0016ßb¹à­KºQj\x001e\x000fÇñhÐ?î¶je[W³>x¿ÛÛ!zð}¦Ê»÷TÉã@\x000c§z\x000cµàT\x0000bôý}É|.?E\x0010IE3,Û2òXéýñÀÚð"Í©ð.û-dEâÈ¹å8ÏÆ«G§ÃA¿×nTËE« Q^æá}\x001eÍËa;W²{±+\x0019ÐPeÿàÀUó\x0004bMÙ¿\x001bÐiÄOg?Õ?LH\x0017 Löì ¡\x0005>«ø¥\x000fjÌï(ÈU®5ê^Ñ¿å3,Ì.vµs2\x0018ö{MÏµ
yàÀÑ7\x000f¶y20p\x001c`\x001dZa£^qô½øE\x001arN7mÛÔUI\x0008Èê\x001ffL\x0014{Æ\x0002\x0005\x0012Ãidï\þ$ÞàQõWÜû\x001e\x0008/½6ÎÔµ"©\x0019ÒVË­þÙd|Ú­¹Ð°à¤qþý\x001f\x000c\x000cª$r\x0007\\x0014ôpèN­#¦gk\x0012¿\x0007W1X³T­×=×È>\x000c!iªò¢¬jdþ9ä5ñGIò-°¯:y:Ðº§Ã¯\x001c\x0006³Ò\x0019L¦AÇ3q¨&dr\x001b'ùb:ìzv^\x000eJ\x0006\x0006¸¾EÇÈ\x001fpå~¡7\x00054íÞð|:î·J\x0005E`?j\x0004ß|ªYn\x001dõû½FÙð\x001f\x00008\x0003n9EÇ*ä¤¿¬þð~ØèNdU{£éì|Ð©*Àù£#¼lN/\x0017ãã!å²9«z4¾¸Z.F]à/\x001d
¿Ð>$áÀÐláý-\x001fR]8	Qé\x000cç_}ë\x001f7\x00024`ýÉl6>i\x0014Ã£{(ÄôÖ*zV³}ú7X`#É\x0017Ùrµö\x001bö«áô\x000fÃÑäruýur\³ `,ð\x0011è;_­WQ§l(!ü.ÜÂA¶Sµ\x000f	\x0007SÒzº¼^]u½õ÷uæ^o|¹BÕrA\x000e[ræ ^\x0000Üôb½\x0007OÈãf)bîÿ)ïì«Ù<¡iT\x001dÁ,µGëÍz1l\x0015ÓÈù@^O0§Ñ\x0001s ËUð^×\x00064¾îÙÅê\x001a\x000fH12yÀv)ï6OÏ/.fÃ\x000e!\x000b½?N\x0015\x00129	×WóA«Dm¼\x0000Ue\x0005ÕªÌVÍòüÐ¶ûWý¿m\x0017í^ïl~¹à\x0012Î4¬ÛÛBo@¢¡\x0007_¥pg&"[½P)³³ÂÄ=¼µâ7%âpC<hPlÈÕëÅ`«)¡¿ë'=0\x0007É#À\x0004®U¼ÖYìPÁÅòë|ä°\x0001
,/\x001bÞd¹Ù¬f'5L·)É§\x00188¡£P¦#Àø¨\x0006½g\x0013!E cK.ÚÉôjs\x0013på\x0017Ïx\x000cÐÈAm\x000e\x0016ëÛË³¶Gt£ñ¦«}Nüé:pÌ|`ý°\x0005\x0008
+Pe\x0003v´\x0012\x000e¢Ö¸ør&\x0013F\x0014åµ£5ú¥\x0005	fS:\x0003ÔíøH\x0015uÿÊÃ"
\x0013÷ÊøÏ(\x0000çÓ\x0016<Wp\x0004 \í¦óéè¨æä#W#^Âf­¿Ø<>Þ}\x001d6a&á9ö­\x0010\x0012xc\x0000ØµËíÁù\x001cgN·\x0000\x000f4òc¼\x0003\x0004³\x000céød\x0006¸º\x0018ùm=Ñ+¥ÂõtÚàåvÆ«û§õô¨Rù­½Cj\x001f\x0010<¬ fC\x0011\x0005vXKA K<©\x0016Ëñd§\x0008"\x0008°\x0008+$= ¶Ý\x0014j1	\x0007ÙµÐ/.Óî±5Áí\x0005>BÍ \x0010¬×ÿX¯ÖîD±%ºnO'¾\x0010\x00117ÈKTD@Q¢øJL4é¤ùÿæîsÐDÓ¹wÍZÓ|È2Å9U»ví*ÎüwE0\x0015?KU¶möâY6|2âÎNTE2^¾¾þþÅ§ô,Né=×ÒEöD«VÄÃ®AtI«¸ZéÞ0NF}Ê÷ÛV\x0019Á
\x0017\x000fÏÏUITRù½Ï\x0010>âN}¿*1¼ê\x000c¢$
\M`+×GT\x0005@wA\x0007°>{Uª6\x0015'dÙ$°e ý~*\x000cþ~*Õ/bøzäãDÃ©~º}zù±Ë\x0006:_=b9û_"ÿ\x0017\x000fb^«\x000cË6èÃ²L­r}ÔÒñ\x0005lÕ2Õ@©R«³xêu©UAq	+ê
ã\x001aõZ¥DI*\x0016\x0011Wd\x0017é±÷\x00004\x0008{´¼Á@Íu¦Z"\x0019\x001eãÖOq¿º=@e§\x0010ï@v`cð/PËUü½Zc\x0005Í\x001b&8p.OÿÔ	@Qè_¹\x0003·$WD(²GT\x0012´TaxÙÂíbØ³Uª\x001c`Gèî \x000c\x0003Ï¸ZéR«m+Z\x001e~¾>m&ÂÕ*K\x0008\x0017ª 3äï2È¶T§Ûo)|¨ý,Ò;¦N]Î)o¢bsµ!uzÑx<òq|¨\_QÎØÓû«_JEì\x0004ÖWª+´ÚÝ=¿½<Ì\x0003\x0013£\x0000XN|\x0011wÿøÖ÷O\x001f"Õ*Û\x0014DùøHm¾Q£Zº.×X¾\x0010&[C±*µ\x0006ß\x0016%I\x0012Å¶Ðj¢\x000cËa¢*r±
éW\x0019®M,	<KMå\x0000Ô\x001b*S*\x0013oÒ¹Å1Å(ÖKd%ñp4\x0001\!!ÈÎ\x0013\x0010Ô§Ê4x¡Ýnq,\x0001\x0002Ï±õ@¦P<êY\x0018$W\x001f²\x000eË\x0014§ªªôE÷8\x0014!°A\x000e$ÂYöL\x0015©¶u¢aÏÑÚ
ô\x001a|;Ý\x0000Zí2æêÕù\x0019\x0011íhõøúöc;éª<[G\x0002\x0008È«WK\x0017b%\x0007L\x0014ào¤S«ÖêMÉðH'ø\x0016º\x0003\x0002\x0005c²hïf\x000b?)²Ú\x0019å
)*ËTP>Ñì\x000e£(ðtº·ÂÐ
Ð÷
J¼Rç>í\x0003¬?¾¬T«Z?Û½¼ýÜ/¦PG
ê\x0005_»ë_¯²ÿRª8s±j:Þñq,]âÁ\x001bQ\x0018/i¦íº®mª"\x0018\x0000Q¢Öq\×qlËÔ\x0015±Ú©¦íuý®ÓÑDh
ésbX®×õ`*¡\x0004p\x000bÿ°j#¦ÞNq=ÛPZ \x000c«&¼Z$\x000eñáq¦¢¢·Z2	áy.t\x000cU$eç±©ÓÑå6PÉºÙ\x0001æVokn/fhõúL«jSÒ-·ë\x0017ØÌ¥XRÞã¸.\x000b|³E-²ï {ãxH5Æ\x0019\x0000ÒiÑò×yÙô\x00102\x0019
\C<\x001f¬VãÕã\x001b´úÀ5Aíù¾_pr>i¢5îoYh"¢d¸Q3\x0000i\x0005Ò¼DÕ\x0000°ÕVðÓPÛM%U°?(·4pÄÔ9ÉôC õv£înÉºåÐ÷ºÜj`Î×HÊû8¦ôèÞµúóÏ×ý"ì´\x001bu\x001aÖ¸c«¿Y¬ä\\x00174\x0017' 1}8$ß³\x0006CffùÁ(£Ñ ÛQÀTK6»¤\x000cI\x0014¡±\x001dSSuÔe2\x0019G\x0003Ï\x0010uBéÌ1LCßF\x0005Ø:G>Ç\x0000d)ù:ò,]\x0019Dã£9\x0006®N\x0018\x0004]J\x0007£#ãQ1=Îg\x0013é­\x0006üá\x0008°	°
ûB	H?\x0008|[W\x0014Ýê\x000e\x0002v[6ý(NBW%\x0017ß\x001bz+L<NÓ	Q\x001a>¨åOJ©rb\x0011'A&&K*Í\x0004
c*¢¨ 8Íp\x0002ú5\x0006à-\x001fw,&ÈUß;í\«·iO\x0017\x0005Q³{a2I	'^óâÄðíªÂ÷Á·­Ë¢¤vºÃde³I\x0008ÐB\x0013rG²ÃA×Ò\x0015Õpü\x0001éÐ\x00125RTP\x001eÅ-k)vLÓ\x0018­\x00024N\x001b÷}GÇ8"ß!ûr_\x0007°¾\x0012ÝVóÐø&JàöIÝ"|gPËêõo=\x0006*\x0003wºXm6ëÕj½ZÎÓÐÓÛMÌ\x000cÃ\x001bgóE¾ãÖé)\x0005åëõzÏgÉÐwnÀ°Y/ç!vñº~<]¬ÈIè\x0019RÌ¶pJ\x0003¬×ø³Ìâ^G\x0006Fx;óé¨«CÚ 9 ôf#È\x0018WÖYcÓ
¶\x0001£\x0008±ZæùMã"\x0001Û(MÀ³,w\x0010§³ÉÈï¨î\x000cÓE>\x001f÷
\x0001w«oç\x001dªwGÓ9Pm\x0000>pp\x000f:SÊQÌ$Î\x0012L£m\x001a?:f6ÏÆ¨¾i:½(/\x0003\x001c\x0003x¾­Ú$ËW s\x001bÑF§ýªÕghÕD\x0015\Í(1y\x0014£ÿüÄPã5ïoÙAjÊU>û¶VøfiÔw,Ìd:\x001d£E\x0014YwÉ¼ \x001cä®nÆ\x0003Ì
A4ü8Ë\x0017Ó\x0007¬Ü\x0001e¿Fù¦`t<Äüi%5*Wÿ_«|ä s5»\x001f¥´nÙ$ì§þ{´
FZF?]Ý?>`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=5[Ýþ'òÁMºgª]ÓÉhØïõú°Ï?áxW@÷kw¿ÃL»Þ`G0Æ_á[èvý{	LaÌ¾À·Ñý\x000e3íB\x0013 Æ÷5ñºi÷Ì´kÉ'Ù¼ûwï ×®Åø-t?×.\x001d½v-Äo£ûÏø\x0011vñ·Ôý\x0017ë¤[ü¤ºßù²÷«K/¾ÅÝ?n¡{ÐW.ÖPFzÉu\x000få\x000b$ªù½Ë\x001c¿îá¹\x0006\x000f&¹æÀ\x0015NÑHß²î-\x001bußBg£Íw+3.Þ}ìØ´A÷\x0014\,Sé\x000eìÞh²X_ª»OìëwáðPUiG Ï©ÚsoÙ¥ûsÌ¦¯]Ê1×ìz®eJ­Áâô¿ÞÖ/CÆá©îÑóbîçoE\x0019<T-Noø"}S\x0006y\x001e§\x000cñèñü~­îß\x001fª\x0000?txCçéÂýC\x0013üuÂ>ïþÂgÑ¬á÷s¸\x0002ÁOBñÔuéRÈ\x0019C:î¾[«{tÌðÑCußl?	"xí©Ý\x001b~³8¦ÝëQ÷¬£\x000b%rµÞl÷\x0004ãIx¨²tïeß=Ðù")ltÛqà\x000cÁ\x001bí\x0001;ø&ÝÃõ"©
\x0016ØèWù»*z¨²#üºÝï¢W%°'h£SðñéûÑý\x001aë\x001eÊ`óÅR\x0005´Ñ\x0007¯ìá\x001b98¼Öâ¦5x+R\x000fUvðó~Þ=K<~S]\x0016*pÌ ÞY}tjÌð]»V÷\x001cXepÅ\x00078bÑcÏßà¼Gx¥Á\x0011H\x0014ªÐý\x0010?ÚfoìfðÑ=ûózÒ\x001cyÏ2·µF«Û'+\x0001)lrÞsÔ§ñt¡T}l¶:=Ü\x0001\x001269ï!>_$×\x001d¾ÈE*W,UêçÎKM	ßÏ{Öx®@¬Ð¬.o(vÌ\x0016îÊ5(¡Ë¼ÙdÝóâ#¯ÝÓ,v·7\x0010'Òùâ}µþÄ´ºßß9\x0012¹J³o:´¹<þPì2Å¢\x0004Ü}i­»öÏ\x0013\x0008ÅRJ£7\x001cÇ¾`ô\x001c\x0000+au	¸ûu»Ç|4\x0001¾@$Êjí¾Ébs2\	Ðý`îß'\x00003\x000eD\x0012\x0019*ÁH\x00109¿Z¼\x0012\x0016v/\«û÷	 \x0019ü·ðÙ×0øO	¨ûúFÝë\x0000Ï\x0012¬ÔJx/¡\x0005%\x000c¿¬7Ô}kÓî+ÜU\x001e\x001aÍö\x0012f³é¨×,%7íþû\x0014¹þ^Âd2\x001evþ'*=\x000b0\x0003A	\x0016\x0008®@</p><p>ñq0¦RØ£:\x00013\x0010TÐ\x0002!2*"ÔßÍJOQZaâ\x0002H\x0005¨4°hF\x0004_@P ½\x00105Ã\x001eÕ	È \x0008	\x0004
H 8¹º»»Øë*óÑ±$Þ\x0005ð@àâæ\x0015@</p><p>\x0004\x000b++K\x0013]Ui!\x001e6fª=ª\x0013`À\x0008\x0004u-\x001d]\x001dMe\x0019Q>j'<¬.@\x000f\x0004)Yy\x0005\x00059)\x0011~. çim=Ì\x0005@\x0010\x0010\x0012\x0011\x0015\x0015\x0011äãb£]Ìcu\x00024;pñ\x0000\x0001\x0017\x0007\x001dm»\x0000\x001c\x0008lììll,À§§õHN\x0000\x0001&úÛ\x000eu\x0001Ð
 b\x0000,\x001f\x0005\x0001@\x0001\x0000Z^±</p><p>endstream
endobj
78 0 obj
<</BitsPerComponent 8/ColorSpace 132 0 R/Filter/FlateDecode/Height 171/Length 46/Name/X/SMask 77 0 R/Subtype/Image/Type/XObject/Width 127>>stream</p><p>HìÁ1\x0001\x0000\x0000\x0000Â õOm\x0006 \x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x000e\x0013`\x0000TÕ\x0000\x0001</p><p>endstream
endobj
79 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceGray/DecodeParms<</BitsPerComponent 8/Colors 1/Columns 180>>/Filter/FlateDecode/Height 112/Length 3099/Name/X/Subtype/Image/Type/XObject/Width 180>>stream</p><p>Hì×V*Ë\x0002E¯£\x0008H\x0012\x0011¤ä $ç$\x0019$àÿÂ­êê& ½Ó\x000f>í1zîÅêU³þ÷¿ÿÿ\x001eòËËKð÷Ô >B¡R©\x0014}jC\x001eHL¥Ò\x0019\x000c&N£\x0002êS\x0003}û`Ä4\x0006Ãåóy\\x0016F9{hDÌæ</p><p>7\x0012©D$à2Ï\x001d\x001aö\x0018\x0010ó\x0004bùZ£Q+¥B.zÎÌ \x0016\x0014*Å\x0015\x0015÷Ú'Íf6¨e×l:ål	â+±ü^grxüÁ×aTÝðÎ6hDÌä\d*­Éé
ÅÓTÔg{	XçÉL\x0010óÒ»Çg7È*R&ìÒß^³içÈ\x0005
'»ç-{¯·Ú­Z!öb<Of|Þx×Û\x0007£Õ\x0013gßëín¯×i\x0014c/\x0006uvÌ°\x0016\x0018ñBm°º\x0003±L©Öê\x000eF£a¯Q8uò«sû\x0006æM­·¸ýÑt±Úê\x000cFãÉdÔ­çÞl\x001a	A½<5æÒzhÞÌN$]¨6;ýÑäs:\x000c;ÕÏ¬\x0012sÏi×ç-*T\x0000ñp\x000c\x0001ó ]\x0002u>«O\x0010'f£y³{CÉ|¹ñÑ\x001b'Óél6{|Èñ(åOñ±à\x000b%JÑæ­Ý\x001b â¯ÙìsÔ©¦ýæûó©Æê¼½àó6E\x0006Ä__3X÷¸ç|Ö\x0019Í\x001b\x0018\x001bl,æóF\x0010CfX°C+;j,æM~¯7»°yÃÇ\x0002'\x0006Ì°\x001a\x0019¿E}\x0016Õ\x0018\x001b\x000b_\x0004Å</p><p>1^Ç¨\x0014¾\x001as\x0017\x0012Éî´ÀÂÉ|\x0005\x001b\x000b0osb¬\x001aýf!ìÔÊN~\x0008bW=4oÊÇ'û+°·r·¯¥\x0007T£[Ë\x0004,êSW\x0018\x000bbÞâhÞFhÞñj<º\x001aËóf\x0000ó\x0016Ëjí±X«FäÔÕØ2oÕÖvây5¬ \x001aUcùrºkÞ\x001eàGírâõÕX²7n1op,¶\x0011Ã:cÕ8¡:\x0003d|ÞTø¼-\h\x000b1d\x0006ê
Z\x001fN¦Î0dÆ÷ó¶Rça§òT¢S-Ý\x0005@æ\x0008n\x000b-ìmsÞ6.\x000e\x000fA\x000eý$Ý\x0000Å`p®¥*½eï¼­1·î\x001b".F¹¼¼øcì\x000b</p><p>-ª\x000e_4S¬í·MfÏó½DÀaÒ©Ô¿Æ\x000613yâ;£3ÈoºÐîn~«V)¹æsX¿Æ¾¸¤±®d\x001a«/Q¨µ{;çm\x0019\_s\x0011Ew¯\x0008\x0005<MCØÂ
Ù\x0002Þ\x0019ÊVÛýÑ±Xþ\x001cõïé°×aÒ?ÜÉ%¢?ÆÆ]|½\x000b¿
\x0008ºÛ,gão^õY÷p§\x0000Ø $Ì?Â\x0006}f]ÉµÎp\x000e0\x001eò\x0017¼À\x0007ÝVµMF¯\x0000[¯Qý%6ü\x0006ù\x0007k Sí\x000c'1 ?'£~§U/\x0017²ÉhÐë²aØR±Ïeÿ\x00016Ø:èîÉ\x0013/µ\x00062\x0003èéd<ìw?µr\x0011`¿yÝ6\x0013Â¾þ\x0003l¬\x001c2­=«r\x001cÈ\x000cê\x0001¨'#\x000c»^.æRÑ7Ûn2hT·}IapÅªç×Ä{ûð \x0011õ'ÝªW\x0000v\x000cb
÷ÿ\x001e\x001b.´@®u°¯ð`æ\x0015ì\x001eÄ.\x0001ìï\x0005aËþ-6\x0010\x000e\x0010´É{dÐ\x000blðA\x000e\x0007½\x000eí\x0007ØÆ\x00056\x0003Ã&ùDAëÇ\x0007=Ç\x0006q\x0011v\x0015Çv\x0010ØW\x0010N6ö\x0005\x0016ô½É,\x001f\x001fô\x0006v»Q-åÓq­U+e7B\x001cT)Ag¡Î\x0019Î×{?\x0008\x001aÇÆÊ=\x001e-c{\x001c\x0016\x0002Ç&×¥`Ð¼\x001bµÙúiÐ»°Ã~Óò\x0004°åK
¾Æ¤£Ñ\x001bÿy\x0013û=\x0003\x001e§õI·äRä`\x0013AûS\x000fð\x0003±\x000bD$ðê»\x0014i</p><p>\x0005}\x000b.ü2èMlpºCìe"\x0007\x001bÚBFÐkØý.
\x0015p)\x0014\x0010Þ</p><p>·\x0006w´Ð$!è
lÂ¥À¥æØ¿=&çJ>BI\x000fÇ&\jU\x0001\x0005­4º£Åf¤ ±\x0017</p><p>Mf®(h
áþ¤1#î\x0015Zëº\x0002\x001e»ÐýAÐ/1^Ã\x001e\x0010Ø\x001b</p><p>ø\x0003Âj¬A\x0018ô'¹AÏ±§»\x0015ðG.5\x000fºô/Þmq©#°ñ m0èÑö gÄókld®[]ê(\x0005\ºÍn
\x001aù=xÀ[ÉÀÞêRG* \x000cúJöhËÖ¶\x0005
^\x0005~Vø'¿ÇÞåRê»ã\x0014ðBçâAoQÒÙt\x0002_Ñét{áh\x0002¹ÉÄ&\</p><p>) pEJö\x0007ÍÂÞ¼dAäÞG£V­Ö\x001a­nlì¹K!\x0005ÄÍ\x0015
÷>j\x0018´Xõüxß\x0008\x001a\x0014cÔkUÙt:/ëM²±q+ 2W>V}ÔØmV¦µo¹Í\x0007íJ.\x001e</p><p>ø¡X2[,×V°Î½îRlbE\x0001Á`Ô»fàA¯_²@ÌÝz>æsZ-V»Û\x001b$³\x0005\x0002{L\x001aöÀF</p><p>IDÈg3i»¡± åZÇFÐXÌïI¿Ýø¨~xÔ?[]\x0000;Øín@\x001aödS\x0001\x001fk.¾\x001b\x001a\²@Ð&ïzÐ³é¨WÏÆ{¹D"UÜ=è­ÎWr±¿Ö±ÁéþæuY\x000cjÏÚ4</p><p>Zç\\x000fzú9ü¨¤|fµLÈçñ\x0005"\x001c`?-cwzdcc§{2âwµJ1IÛÍ\x000c¾7yåå A5ú­bÔm¸\x0015rYL&Ã\x0013\x0008çØ\x0001ý^mII¹x­Zð^\x0006uOÐlBç\x000cçë½EÐ30tõìM#å³ÀùD£3\x0000ö\x0015ÀVª!¶'\x0010Ndòäbã.õÑ(çb^F&`í
w£6ûRËAO'ÃrÒû¬\x0012qèT ]\x0014*\x0015`³\x0001ö
ÀÖ>Y\x001e8þ\x0007Ø^»¾<Ý¸tÊé`_+ôÎH¾1¿ÍÂÕÕÐ+°ÿ-xpl&-\x0003ØF\x0003aH.É¨ß®¤6Ï¤^îdFAûSå\x000fâ6;¯G´</p><p>b\x0003nÍ%°Í\x0000;\x0014OçJÕz\x000b`\x000fÉp)xü6</p><p>\x0011N.`î,4\x0011´+R\x0007­\x0006^Å\x000f´-Æ±_ü¡X*Wª ìÑo±ÑÁ\x0010÷\x0018o\x0005¬}ÌT&O¢¶øS\x0015<èµj,ÿ[MÃ°¯Å²ÛûG£Ùþâ[ÅþÌ°O)\x0001¯wû³·\x0006w´ÐDA£\x0003\x0005VÏØè\x0014^n\x001a\x001d`ó\x0011¶a\x0019û£÷;3ïË\x0019]²$\x000fV\x001aÜfAÐ3t ¬Wc'¶ôVõh0ÙÝ¾7]ü¥\x0002bÝ(ÅÜzùÕ>ãA+AÐEì6»»\x001a»±\x0015*
Äö¾E¡\x0002Ö®³é¸ß,\x001dÒ=»1\x000fZc
d° á§»³\x001a{±õ&\x001bPÀè¹\x001e½`²ºµLÀ¢¾Ù³ÏxÐ\x001c¡Òø\x0012AFu@5L»ª±\x0003\x001bH	Ä~¶¹ÍõØáF§Ùë³RÈÞó	\x0012AK5Ö \x0016ôçxÐÚSmØ,\x000e}§æúS\x0005¢Ó,bó¼ï\x0013\\x000bº7\x001acÕ°£è;æ5l\x001e½f®G\x001c°\x001aõlÐúfû_¶ ?\x0006Ã\x0001ÔÐ\x0003ª±\x0005ñK\x0005\x0005EçîÃ EXÐN¯Ûüf5ö`S\x0017Ø?P@Ü]ðåßþÆ0è+\x0010t ]n¶[\x000c!)3#î\x0005öº\x0002®¸Ô®áF¢\x0013ÄEç»×]¢ Ý\¹V)Ä<\x0007ý:{±W\x00150°¿q©í¢³ó]X£\x001fÌÞX&K\x0004ìZùqÕØ½¢¸ÔòivÈo\x000c\x0016*´6o8\x0016	¸*1÷_g\x001fö\x0002"ú\x000e{vØi¶x
Ô;±òÿìmOP\x0018§0\x0014Ô|	,ucËEäfÍrlËÄ¶²¬Õúÿ¿¡ç \x001aàK°Îi}èþ\x0001k\x000fg÷s\x001d¥m'\x001d½¾ëm\x0013\x0005ÛQÀÍ.µí}\x001eº±\x0004ÍðE©©êrXÙõ½r©\x0003K­°¿ªÄq
·5Â
\x000c\x0006Ìðð\x001fkµýÈE.-Ø¥äüÒº\x001e\x0007Ìõ\x0003IÃÝh¹PB}\x001dA3\N,\x0014Ä,¦\x00138Ø9/¶£³¥K½Ã[ðåa<05I°Íâpý2,Ç±LÂ¼½t)¹Â-y{}ÙWgGÍònu\x000eB£!4\x0015ÇìÇv]Ê
Rò4?ÞÛ£¾¡ÊyÐÐðå\x001c\x000c\x0001b¼È>ìëR+s\x0005)¹µ§ÓÉÕ7[õR6beÅÜ`'Þ
æÚë\x000f5¼è\x0019­FE`£ùWâs©¹jíqÚíÇm\x0015OË\x0012H\x0000\x001b¹¢éºª4¤À¥¶ÌÈÅo®ÅrUe©ºÇÙ²\x0004âQ@h@A\x0014\x001cÏ2I¬-K .6jÀ\x000cI'Ñÿ42+%\x0014
¡¨\x0004î½@*N\x0003.B¬eIèZøÏ÷ù\x0014`\x0000®ì©\x0013</p><p>endstream
endobj
80 0 obj
<</BitsPerComponent 8/ColorSpace 132 0 R/Filter/FlateDecode/Height 112/Length 45/Name/X/SMask 79 0 R/Subtype/Image/Type/XObject/Width 180>>stream</p><p>HìÁ\x0000\x0000\x0000\x0000Ã ùS\x001fá\x0002U\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000À7\x0001\x0006\x0000NÀ\x0000\x0001</p><p>endstream
endobj
81 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceGray/DecodeParms<</BitsPerComponent 8/Colors 1/Columns 166>>/Filter/FlateDecode/Height 132/Length 3290/Name/X/Subtype/Image/Type/XObject/Width 166>>stream</p><p>Hì×B"Y\x0014E[r\x0016,%', ID¢A$êüÿ'Ì¹U\x0005h[\x0005\x0014ÎÃÜ~\x0012zsO­UûüùóÿùÿP8'p\x0018\x000c\x0006üûÛI¾;x@&Åb1QÐßÎ³},\x0016ÃÃaCÐÿVÌµ<¾@$HÄ"\x0001ÃúïÄüP"É*R.\x0015óÿ#1qRà9)ã	\x0015*í¥Ád6ô\x001a¹DÀùý¡¯%äáw\x0008	\x0016»Ëë\x000f\x0004¼NN.æýîe.Ç%\x0014OaÊ\x001aÑbsù®C±ÛT:\x0008y,Ú3¸ÌßJù9á\x0019Jh0Û^H¼Ë\x0015Kår©</p><p>9õr\x0011ÉøÅ,\x000e \x0012+Õ\x0017zóÓ\x0013\x0008Eo!ácµþÜj·*ù¸×¤ÀÈ+á\x0012æs\x0005$4]9<þh"»/U a·?\x0018\x000e\x0007F1á;zJ\x0002fÖ\x001aÌj­Þdu¸ýÁH"-@Â'H8|y\x001dO&ãQ¯q\x001f÷\x0018\x0015Çø×0[ín_0\x0012Oe</p><p>\x000fåÚS³Ó\x001b ÓÙ|>¼tj¹C'\x0013\x001e
TD\x0008f9\x001cOfòE°
	GXÂÅâím1\x001f\x000f¥TÀª>å³é7Ñ×0CB\x001cæ< Òh¶»áGÂ÷÷÷·ÅtÔ«t!Äi,W\x000f"À, qÝ\x0004@\x0018Ì(a3áû?r>î??Üú-Ç¸J,#Ê</p><p>æÀMô\x0019Kø=\x0010Eü\x0007\x001dt/íJ&d×hA `ÄMÓ\x001b0N§½ö\x001aÇiölðT¦Ô ]+!!\x000eótº\x0010\x000b9\x000c\x0001ë«c¼\x001eO ¤èL¥3]Á{/\x001c\x0003Wº!\x001eÄíXJ@§SÍE8:t_%+©vo0úÊ'?'Ä¯rÜ×ù8è°ù§*£3\x0018¿+ª\x0004*0u ätØ*ß\x0005m\x0017Hè´§dr2íú6_n41¿De{Þ³×n=\x001fu\x001b\x0014ô£RrEr;«4{pd\x0012\x0012ó\x001e<\x0001«FzfÉ`rÅ</p><p>£7Q|ê&ß¢²\x0015\x0012©²	9.ÏéGç\x000f~</p><p>£ï¶Ô\x001c!ãÏ	ñH÷Ð+UGy£ç\x0012&îI@Ê)$\x0011q©ÊÇ4Rå\x0011ÐA)\x0019\x001cìÒ\x0015+>CJr!\x0011:Ëq¤­\x000cèìÂ\x0011)<
&ó7²W	è`-CÊg\x001f¥VÕy§«l­78<£n5\x001b>\x0016:è Èæ@ºÒ\x0019ÍÈ¥|[ \x0017xò88\x0018>Fïm©õBîÁÄß\x0018\x0008ýHOå\x001fìÁ¤\x000fJÙ×\x000b½vØÇ \x001cKÉâKµöp¾Ñ\x001fÂ\x0007»KÔ+Mj©Ë:RLÀG¢¶\x00063Õî+)|·c*h×+¥B\x001e\x001b~\x000c\x0017!|LþT¹M\x0012\x001fôzìÔòñ]¯\x0005Øu\x001eá\x001dÉ\x0011ÊõèíC\x0001A³O\x0004æ\x000bTÄã°\x0018ô·"Î\x0019½\x0007¯L¹¾ö[ÕûTØg3¨Ï%\x0002.öëD^jm¡\$>xÌA»QÊ&.Ny&æsh§\x0008á£²\ßÅ\x00079\x001b¿ôÕb:êw\x0018µòS!ícG^W|IÒø`1çp§r>\x0019ò\\x0001E´\x001dás®w'\x001e\x0014j\x0011ºÎÉ¨ßª?db×Ç \x0008ás¦sD\x000bdñ!®\x0013\x0016´ñ°û\)¤"@\x0006(âÑxx-¢Ïê:ç\x0011¢(¸q[/UKèÉÉ`q\x0011>é</p><p>i|V9ç\x0004EwÑÃ¤¥uìx-ò%\x001fÉã³\x001a;¢hSäµéé'±UÄ\x0014ðY\x001b;¢¨]/eã¸<E4É\x0013m\x0015Rl«èÝ*Ö¯ ¨zøí¸<é¨ \x0018>ê«`üVñé:1y6\x001es·!¶</p><p>rBl\x0015eÒ[ÅVÎÙ\x0018äY\x0003y\x0006h'ÁC~«ØÊ¹&Ï0]òÄk+vÿ<¤àõ­ëÄ)Ê% Oåáåo\x0015¶pìVñÍunÈS~ð±SÝ*¾É¹&O:*\x0008àj\x0011ù­âëk\x0015\x0004äi>´<ñZäù¶\x0016½Ã!wkòô\x001dZ­EpEØ!\x0013ô£\x0010òT\x001dPËZ­o{\x001d2.æp\x0016¤s"h'^\x0002¨\x0016}z01&Æp&3\x0008Jr{C\x0014­äy¸</p><p>×"/ªEÓ(økeÐïõ£ñlþF&çz\x00059èþyýÒ\x0015û\ðu±ÓlÔÝÁh2[\x001b;FÑÁ÷7Ìë\x0017öp¾±YÞá&\x0007­Z©P¸/U»Ã×)µ±\x001fXK¯oÖ" a<lÁó\x0015ÆÙZ³÷ÆNöõýM§î/O¼\x0016ù7k\x0011÷K§O\x0004½.?|{l´aìs*c_íoF
!Ï=r\x0012µ(±QÞßf¯½Æ}"à0\x001b\x0016?*T`ìã)yòÄ÷7$Ï}Æ×"çF-yOÍR*h×«\x0015</p><p>µÎâºe\x001eê­>yÖö·CÈ¨E\x001bëîûb:êT³\x0011Ay&\x0011«õWP2_~ê\x000cpH}IQ!yæðQY¯×j\x0011B§ÿTLøÌj©Çã¤r­Ñá¦Õ&µ±ÈÓmÝOD-J®j\x00116ïV9\x001d´]ÈD\6ÍáÏ0ö`"[ª·)}]XóÜ]x-rÔ"På¨[ÏG]\x0006\x0007¿Ábs\x0005sµÁæ
'\x000b0vÒò\íoûË¨E\x0011¬\x0016½áó\x001e<?$ý\x0016T}#ääðDRÅÉ\x0011ÝÁØwgüÚµ;Ej\x0011¦Êv%\x0013rèÎE\\x0016ú:ÈÉdq\x0005bêÒê¾Iì*Ï{$O"êÍs³\x0016\x0011ª{J	MüfÈÉbó§rÑæÛGhSí´¿áµÈÕ"èHéë+íÃ\}\x0011ºN\x000eÐ®¼0;<k;Ê\x0013£h±¯×¢9Ì{Ô­å".½\Ï{ùW\x0013Q$ÛO@×¦ß¡yâµÈ\x0011É£u\x0017~4¡ÊS>{óÇâ\x0014ÁØWò\x0004(Ê³U/¡ýÍ²ÃþðQ_A-ê¾Nga»|wc×É­ïÀÇ¾<ýÍÿ±¿ÎIÔ"Xw_ÆcLn\x000ekû\x000bcßKËý¢<×Q-zxî^ú Ê\x0015SåWþ§y\x0017yÂ\x00035Â÷·kª\x0015déõ\­Ýë6Ë ÊË¥*¿øãÃÈ³°§¬<1¯«­×©R£ùTÉÅ<&¥ä3:9÷ç\x000cÉ³^"ä)#-O\x0006*\x001c\x0006w4ûP\x000fû­¸*¿ÿÜ<ã\x0014çÛ®ò<aÂÈµV,IÇ\x00026üÛy\çgyî¸¿Q'\x001a¹XqióÝ>^ñ·y¯>².Ï»]å¥"O \pª¼´Ø\x001dvØùN\x0005Ûªü*çJî`"·<ëòüqìp\x0010S®Ñ]^¨å\x0010òïó^~h)OÁæ\x000bã\x0014Qo<I6O	vÊÎeRtù$_\x0008kòt\x0006bbjó¤(Od\x0017\x000eO \x0014</p><p>ø\6ÙëòÔ[=7·{ÉÓ¨YRôÃÿÇæp8ljûÓJZ£Ý\x0017Iï&Ï\x0006øï\x0006äSôw»0\x0018\x000c&\x0013Ö\x001c-'PdvQçZóaûäG(NðC)ãÉ³\x0000û\x001b\§Tø«w>ß5O*û\x001b¼33±Ý TÌ\x000e1\x000fÒ<+Û Ó úýe\x001d;PÎeó\ÊÒþ\x0006òl×©\x001b\x0007¬2_UÛCåÜ'¶¿)Q4ì4É\x0000Z\x000b|Aï\x0011s]!$OûÛä¥S/ÄÜ\x0006(;L\x0006])7åé¤ï«ÔÆ>\x000c[éEýå6sÈ+y\x0002Eq <\x0017³×n-\x001b²i¥|zS®Q¤·y©É\x0013.sÜoä#\x000béÏÍqïK´&G Ja#RíÇHù!O´¿¡æI²@Ê×^-{cÓHi~.W9"¢yÞßÞ\x0017Óv9\x001d0«\x0010=ÿr_öM\x0005DQ\x001cVXee#KB¤(/£íe°%M\x0011ÆËP¾ÿWèÜmé.mõÏÚ;ý>Á3{ö÷Üs44(åú<¥B>\x001eØ²µz|\x00161\x0015+\x0008ÈSüESéS>\§¡âZZ}s}.Ï¨$Ïæc¾\x0007O\x0004ÝZ¾ßqbòüe\x00059=\x001eÈU
\ÆÄVã\x000c_þA ô~û±=eC«\x0005S\x0013g^]¨:Ý§»g\x0015²\Â¯  Ï³Êý\x0006»\x0006ªÎÍysAÁWNùµ¸¼AUy¢ê¼6ÊP\x001dVëMCó³E\x000eVçÒ</p><p>"U§Y¹Ô¡:8æòýË\x0013©²ßª\x0015³1\x0010úÊ«sªÜo\x00136Ë1¼:·ä¾Ö¡:JÎïï7ÈÛdØ{®^¥\x000f}Mêà\x000b÷[Ul÷\x0006£ñd.Z1\x0017ßuëV\x001dSq¿!y\x0002çp4\x001côZu¡\x000cy\x001dúU\x0007ÇÄä\x0000yVêÍv§Ûi??</p><p>|ê\x0010T©gu°Ìï7o0Ìð¥J­!õûÒE:\x001a bÞræòä`ìYþ¦$WùÓH¥­0oB(¿ä¹í\x000fÅél.IÅÃ~\x0016ý¤|J<]\x001eÿÞA4\x0016ww¶hÊLÌ¼?#ßova½>óyÜÎM+i\x0006yìf«mv2¶S\x0016\x0013Qã\x0005Æ\x000eßsÃBQÕ²a6\x0012	i9&\x00111	iæ.\F)kRô¦øÿù\x0010`\x0000\x0010ý¬ã</p><p>endstream
endobj
82 0 obj
<</BitsPerComponent 8/ColorSpace 132 0 R/Filter/FlateDecode/Height 132/Length 46/Name/X/SMask 81 0 R/Subtype/Image/Type/XObject/Width 166>>stream</p><p>HìÁ\x0001\x0001\x0000\x0000\x0000 ÿ¯nH@\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000|\x0000\x0003\x0000U\x0000\x0001</p><p>endstream
endobj
83 0 obj
<</Contents 84 0 R/CropBox[0.0 0.0 540.0 780.0]/Group 480 0 R/MediaBox[0.0 0.0 540.0 780.0]/Parent 457 0 R/Resources<</ColorSpace<</CS0 132 0 R>>/ExtGState<</GS0 475 0 R>>/Font<</TT0 479 0 R/TT1 135 0 R>>/XObject<</Im0 85 0 R/Im1 86 0 R/Im2 88 0 R/Im3 90 0 R/Im4 92 0 R/Im5 94 0 R/Im6 96 0 R/Im7 98 0 R>>>>/Rotate 0/StructParents 6/Tabs/S/Type/Page>>
endobj
84 0 obj
<</Filter/FlateDecode/Length 2061>>stream</p><p>HWÙn\x001dÇ\x0011}¯èG^\x0003Óì}\x0001\x000c\x0003±¤\x0018\x000e` ä!ñ\x0003AQ\x0002
R¶®Ä8È×çªî¹Ct`K\x0000§×ZO®{þç÷÷Çkóõ×ç?¼øþ¥ñæo¾}ùÂ,\x001f\x0017ïm-&ºfKì&ûbSíf
5ÛÁñzùùsçß½qæý§eèÍUãð\x001cìµ'CY¹ã_41ÚX9«»åüû;g^þ¼¼Æg]+ÆÙ=þf(ÿÛwK°8ø+ìúÉ,\x001e«0¨[#¦TÛhÈåÕ\x000f°ùü\x000bgÂÎd}1¥GÛúÒÔ\x0015¬>ëIÏqóÄÃüêàI!Ü4É#4Í¹\òpÅOW|¥ãÚÉÒ²7õÛåü¯¡i\x001aú8\x0004Ç÷ËùÅC\x0000.Þ-+ö\x001dFWFFÉ\üjB´\x0018¬b§\x000ck°±CYõÕ\x0006pènùçÙ«Ã\x001a\x0010¬³ÿ\x001cVÏï/üVsö3×ñ=\x001e\x0018Ü³ÏX6g×\x0014¬ÛK\x001dÛO5>:aÞ\x000e1ã3\x000fÃ¹?µ\êöQ/ß\q\x0019Çnöû8þÆl:>\x001d~¼øëÕÅ£ä]r]"J\x0010\x0012Ra×Ö¹ö(·²\x001d¾\x001a$·<æ5Õ"\x0006ãÖ\x000f	@}\x001c©
3µT×±i\x0002p\x001e\x0002\x0010\x0008$5gÓ\x0013º¸K\x001cÅ¢º\x001c2µ\x001aÁ­\x0014 ¬XTóuâ(n8rÅføúá'6è·^\{÷ÕShj32Þ¼WÈ\x0004B\x0006\x0003ï\x0018m/\x0018\x001dúì¸\x0006«\x001a\x000b¢EÌß4 |Üb¶:³+XùIö»ýsÐ	\x0006EÁ\x000fk¢q~.\x0002\x000c7ãø\x0011hAYíO\x0018I=M´Ø\x0019(\x000e\x001c¿]Süã\x001c½x\x001a\x0012§¡\x000fõí\x001c5EG
·ãä¥£\x0007wÛv÷úèÊïå°m\x0016 Ä5ÐÈ¯`Û»ÃZl\x0010O\x0012õ\x001c\x0007Àï\x0006²/ñlóùÁË£\x001e	ùëßD»ß\x0011sÈdRb£4ÛY+¹ã	\x000cr\x0000oÊe<FÜ¡DD\x000eÇ¡\x001aPR^÷\x0003é\x0004øP\x0010ý\x0004¢"dÿÊÅ'ôÉ.Ð\x001cºèÃ)jï¥\x001b\x0011Ã\x0002@¼rm(\x001crS_~þ\x0019\x0000\x0007Ü,*¶$­ôâø¡	ÊªO\x0017\x0002÷wVB\x0000y¶\x0002.(àv_\x0010\x000c©\x0017\x0004A8¡fbåã¨ûg\x0010?±t\x001c\x000bÿ</p><p>9nÐ\x0016ÔT\x001b%3\x0017o¡ç
¯\x0017ìËR\x0012sçø:ÃØIé\x0007µ²ªÄY0\x0014{û°iù0\x000bîn[\x001a0;<{tåuQO!x®|.Ç¹iæýQéÜI\x0002$øÑV°¸ÀÔx¸øéyüïè~B­ToËlèì\x0008¤\x0012ô
 Ì\x0015Àa¿Ñ\x0006Ð\x0002íãÂK9ábs\x0013ÇObï#\x001e_(¦\x0014\x0001«Bö®ò6pçné0¥\x0019`\x0006Þ.+ZIÝz<\x000f\Èx\x0000{¼\x0013Õ\x001bNKh&\x0003m±\x001a\x001e\x0011ÓH«ÍÕ²z>+Å bäu4$¹g\x0003Ø'0?Ù2à:¦x\x00190èI DPq= ÷ \x0004</p><p>É4\x0007×ñV\x0001á(!L
ºu9³\x001d+µÖ!pÖÇ\x001bj3ì¹âÍñâ$Xâ*ÃAÅ-lýh\x0011@®ó¯kú¶^±._?Ýù:\x0013*\x000c\x0003.«ô\x0000/d0xß*«Û±$\x001f1\x000cw½¾¢B08Å¬éÓÏ\;Ä\x0008\x000f¹ô\x0005kÞëÐ~æIkèdM.ÈQ</p><p>»Ì#ª)\x0001ÏI°ÄP*ÑM\x000b1\x0007\x0014ReßX\x000by\x000fÜS8sæøüB\x001fºá¥°KF{j}Ì¸Y°\x0002Ap\x001f{
{ÞÆè3?°³\x0011.ÐEº%xáv\x0001yuòcÌx×=\x0017:\x0000Rb\x0015@b?!é+ú2\x000bÇ³L=ù¡7h6 \x0011,\x0004ÑXól;\x0011	\x0001´Mô\x0012eÀæÓ"4\x001e=uûÿyo§¼3sà>d9ó¯Æ<UÐEîPLø\x0013mOyäÛ5Ï¨A<ïâÍ³×æy{°O½óà~\x0014j\x0005À©\x0010nU\x000cõÿt@q}¸awÂ\x0017<V¡5rïýñ7_ë°ûåñ\x0007XO©!Ø`Æ"\x000f$:d\x0019!AÄkÕq\x0010,]-2Acf^!Ã³\x0016Ç@ rZß]Ø\x000bÚ)J5«`R¢\x0004H\x0004Úî\x0016è\x0007_8<6¤\x00046ÌÙ$=×À\x001f¢
0$P\x0015h¾ÅõmB¸ÙÓtÝî\x0012×dU^nâc\x0011
>Õã§Nô|òD«Æ\x0012§\x0000x3É¶Én`·T¶\x0019Îu=+s8ÅQêÐ\x000e;| \x001d\x0012ºT\x0015äaÖ\x0011t£a\x0008lýè"#«ìê\x0018~\x0007"SëßÀÚQÇPZµfe
\x0007"g\x0001å-è\x000f&HÇ6Þ\x0004ðÂòNÑ°HM¨2ª\x0008\x0018ó§fõðGØsiKópUïTy\x001dª</p><p>Æ§GÒÃñ\x000eJs
ç2á0FÓ0N§!tuµ¤½Ü$ª+Þ¯8í\x0008BJÑªÁ\x0019 2rÀXØù¤±ÒLø\x0016¼ü,²m|µ¸m¼Î
ÞX·+*»Îk7.\x0002Ù>bkÜEi¥\x0007\x001dF7\x0019\x0006`TëSÓ\x0007¤E4fòsHË/¸\x0010´î\x0007\x0004ÀÚ}V\x000b&9õéNà°=ÍâÜâ%é&1Ï)Õ\x0015±Âá¬
ì3ñr\x00082ó\x0004\x0008ê$ðGA!4Ò´JP¡h\x001eT× ±¥Ë9²YCÆ(Ò\x0007TB7*øeq·ø©ÛepÔ\\x001d\x0018\x0013Òn¾úíòÉÆBÒéÊH\x001d[.¿\x0015%fMøQ3	×r!9Nß¢v=Ã¹è\x001e­Ê2
@î9Yµê\x001e_¤
J +·\x0015;&¹yæ\x0018w³`·+C6\x0013(.&ndY\x0003<&3øcªIâTóiT\x0015&®YU#\x0018qãÅ\x0007ùØ?ç¯ÿ	0\x0000ÛÞ
></p><p>endstream
endobj
85 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceRGB/DecodeParms<</BitsPerComponent 8/Colors 3/Columns 964>>/Filter/FlateDecode/Height 533/Length 59361/Name/X/Subtype/Image/Type/XObject/Width 964>>stream</p><p>HìÖ[PT÷\x0001Çñ³ë¥í¤­\x001aÛIfÚ´\x000fvÒö!íL./}èKÇ¶Ó´uAQ\x0012Ä Ü¼¡ D\x0005ÈM.\x0001û®Èe¹D\x0002F¼ (ë®8b!º{Î¡g\x0017\x0017Iªí2sØSã÷;YeÀÃÿìoþs¿\x000f\x0000ÀL¼\x0013\x0018§ù¯\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000àÿß\x0004\x0011\x0011\x0011=\x001d½ùóî\x0005!fòS¥ùÈ\x0001<@ëcMDDD\x001eÊ3CzjNk>r\x0000\x000fÐúX\x0013\x0011\x0011òØ¤ùÈ\x0001<@ëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨NëcMDDD\x001e-
¨ÎÍÓ'Ë²óafÍü\x0012\x0011\x0011º±¥\x0001Õ¹\x0000\x001fì[ÙibÚóé&¦}×ñTv]ëæ8v]Á&""R;÷gðÐMûè¸øH9'¾bK\x0003SÜ<}²+»(Úí</p><p>Éù(Ú\x001cO\x001clNöi$Ù1'¯rü\x000f¢¨¼*»¾-O{>ÅùV×\x0005DDD¤jîoiUh>r\x0000\x000fpóô9ç­,KÒÎ¬<=åËG¾Çõ¨&¦¿è4u»ºuHÒ¤oä|Qæ\x000eCO{li@un>×½µµ¯ÆÔ]kî1ÕöÔ>F]]oYY×Áaç\x0007óA\x0014ÇÎ\x001b©1Ö6êGk\x001b\x001e29\x001fkêF\x001alwÇù¤#"÷SVòí;ã×nttöW5ÝÓ\x0014¶§f]xÏÆBï ã@aUp_hÑ]å±©õÆ²\x0013ÇÚ.u÷\x000f}ùÕ]´kýë\x0013y:¶4 :7OäÃòä7¿Î\x0011\x0018A\x0017½\x0010÷u{¯'	B´¿ýØØ]Q¹FÙÒv»²Òó.	B¯ð^aÞß'\x0008Ýß}þî\x0017Ã%Ê\x0002Å[	\x0011=ù)w\x0015»(^\x001dúÒüÑù¸í½C</p><p>½C×\x0006FVmª
©\x000bÝmÚ\x0018U\x0013\x0018Q½vkOH×ú·Ö\x0015¼³±("¶ÆXv²£s`ìÖ¸²ÆµþS<\x0017[\x001aP§OùØr¬bY~íµz}ÒÜ¹\x001fèõ©z}Ú×¥Î¡|÷·¿Ë·ÛEå"iò\x001ae\x001bËò°ÉÜ÷£\x000cÎYhÕ?kÕ/r>ºÌYlÕÿ ÿÇ?»7|C~ðfõ^BDOpÊMÂf³Y\x0007?¯n<\x0017\x0011kZ\x001dT´:äÐ\x001d¦Ô£\x0019\x0007O\x001bJ?)ª¼PXÙi(û4çP{¦¡-5ëD|ÚGÑñu[£ª\x0003ÂJß\x000e.|smÁÒµùþa%û\x000b}òÙÀ­Ûã27\x001dz:bK\x0003ªsóôM.\åßW_1\x0008B2\x0005!Y\x0010R¦Q^IÑëÓuºø¦\x000f»Kì6ÇvæXÔ¶þ? Ì³è\x0016Y\x0005\x0016aáCWé[üÂ]eK;'8kDôÈÃÍ±;§Úÿõ~JÝÊ`£ïMÙ%\x001dÍ-½µÍ=õ]%Õç¥çr</p><p>OgæLÍjMü %v_ãî8sdLÍ¶\x0015\x001bÂ\x000fùm6z\x0007å/õÏýûÚ¼àÈÒòÚ3ÖÁaQäÎCßþØÒêÜ<}®-=ñê+FAHÔëÓ¾1¤uºdÎñ¢NØuqHyÿä\x0007ä\x001cÒh\x0017%éêr~AgÑ?k\x0011\x0016X\x000fé\x0016Ygú\x0017¿poøÆÄ-={7\x0012"zRSn&×®Ú×\x0015{\x0007\x0015FÄ5\x0016¯ÿ¸ïÃã\x0003Ê®PVtMçÁò¼â3\x0007\x000c'ÓrZö\x001fÝÚ\x001cÐ°c)<ªrsdIð¶¢u
¾ÁÙ«ü3û¥/óËúo¾W@AbfcçEËýû÷µþ\x0013f7¶4 :7OßßÒ:]ª2§\x0005!IÐ¥éõq&Óeå6]v%Ùm]W¯õ¬ö³</p><p>eÎb\x000b[f$IW®\x000eg\x0018z\x0007\x001f\³µ<9¿ÍÜÜ×tâ¹¥¯ªñrùÅÕ\x0017\x000c¥\x001d¹Emù§R³'¤7ïIn¯©Þ¶³|ÓöâÀPÃ»\x001bòß\x000e8°Ò/cOò\x001b+\x0013ÿôæÞ%^Éoøf/]»=¦²íl÷øø=\x001b\x0010}{cK\x0003ªsóô=fK§º\x001e\x0013{>óÅ\x0017s\x0016üPù2Úky¥$v»sKKÎ\x0007Qü|ôæ\x0017U5}ó¾oÕ-´°¥h&)·\x0001ëõ}ûx\x0005\x001a\x0003#«sK/4\x001e¿ÒÐ:PÝÔSÑp¹Ô|±¨òÓüö,ãéôÜÖäý\x001fÇ¥µìNjØ\x0011k</p><p>®ÚòÞá°Âõ\x000c~y>þûWø¦-[ò·\x0012þ¸4ö\x000fÝýú\x001d¯ÿy×ióÍ
yïÐ±3]÷m6­ÿ\¢Ù-
¨ÎÍÓ÷-=9¤\x0013^úUAXxÓêU¥FcguUWvfÛ[w&\x001c8V±cOoß\x0018éýé/,Â÷,ñÌ&"·Rî?×®¤d7¯\x00080ìª1V}ÖØj57÷U\x001d¹TV×YTqNYÑyÅí\x0007</p><p>N¥eµ&¥·Ä&\x001f¯|¿zÛÎM\x0011¶þÝ2\x0001júÊãøBµ»3«­vvvgwVI ZºÓU@µ.\x0016/\x0014<"TA\x0004< $á\x0008( \x0002\x0002\x00009 á#rz \ È!\x0006DCP\µ¢róÿ'ìË\x0001R¯MgÄtÞ'ßyóþ/ÿþ/oæ÷Þ'ÍätÿK\x0003{=ÓÒ&â»maßZ\x0006X\x0004®ø§ÿ\x00123¯¥fts\x001bµS¢{@öí¶n\x000cÃ4ý§!\x0019\x0001D¤6\x0006ïÒ¸äÀÀ¨!*Vß»]:æOÿæÛLÇ½Å\x0015"7òY\x001a­,!¾~l\x0014´\x001cÐ\x0019\x001bÃPôYV~\x0007òQ·Î<12\x0017º4\x0004\x0002Q\x0005°<ï\x001fH\x0012\µwÏp\x000f(N+\x0012»r¿¸BTPv7»Tx®âvéùô2\x000e¯Å»ÄàVE]\x00088{$¤È;0â+póJw!ó\x001d÷óì÷qwîÙº+rãÎps«\x0010³MÇ¾\x000bøÇ\x001a¿%¦¾_\x0018{é\x0013iÆÞëlØÖûýÃ\x000b;»\x001e\x001dLÓ\x001d\x0002ùÿ}ózt\x001a¼\x0005¼Kã\x0003\x0003£¨X}¯\xJîÒl`Ñ</p><p>ÿyÂìO\x0018^ôVaï	Fí_ÿ\x0012/@\x0001JPIO±\x0008Ò­;_Ì\x0015#¾ÎgbK/\x001cííPº4i\x0008\x0004"ÛyFGÇÎ7;Ñ2\é¹I9gª;Ê;òÏÞÉ)\x0015¦äÜ¼ÑØù¬ïy{ûÝÂ\x0008f~\x0008ã\@XoP§.~êt¿Û%ÎÖ½Ãiù}Åö°µ!«6\x0004­4\x000fXö
}ñ*/\x00037èi`ä­O -^E_ÿCµ3\ÞÛ÷\x0002Ã0M/\x0000\x0004¢Ýh\r``Ô\x0010\x0015Ë\x0001hL¥$\x0012pi\x000eGîÒ 2©3khÀGÈÏ>e^¿ÞÕv§'*òò£?\x0007V\x000c´x°§§kË\x0007ÎûËLºÙb\x001dàÏs»§GçÓnä÷ó\x0016<tiÉ\x000c6\x0004\x0002Ñ\x0016À\x0016Òv÷'Ïc§w3ck*î\x0015\hÏ=Ó*(lIËkO½zíÆ½ÁÁ\x0011p[O8!Qàw,Ûçh\x001eÅOpÈ3Ýäx0ÁÞ9ÎfOÕ®È;ÃÌ­BVo</p><p>6¶\x0008üz­ÿRSß/<ñD\x001aèm@òRdá</p><p>êWkX9ñm\x000f¤¯n\x0019\x001e\x0019Ñô\x0002@ ÚÆ%\x0007\x0006F
Q±\x001cKË´X:ab®«\x001b=k\x0016WO­§Ëùøc\x001ekÑâD</p><p>¥ÌØ8#,¢vóæ\\x0003øäF©Dg\x001fP|;\x0010¤\x000bù]\x0017ò\x0007±î|Eº'#ëë}.Ö#þ#~´÷é\x0014\x0018xv&\x001b\x0002h\x0007CCC±)vÒ\x0002\x0019\x0017sÏÝË?7»Dqº9%«!1½.WuézûÀà0¢@§\x000e\x0007&xÐ3\x000fÒÒö¹¥8¸òl¸Û÷°¶|ÂbûñµVÇL7\x0004\x0012Ì\x000fÿ}Ï&ÀHxM4¸Ä\x0011h\x000bVM,Cw8'Q\x0002óîw?À½\x0008\x0002ù\x001fÐ¸äÀÀ¨!*\x00038§á\x0002§^²$	AB\x0010$|2\x0011 5+\x001atfÂA°E\x0012Úd`¨\x0014E?fñDsæý|Ôèü oM'ôæ
?ù\x0019<(ÅdÚ>µ
@´\x0001°{Ü¸)r¡g;ûæ%å4åm\x0013\x0014µ¤å6$eÞà¥Öpù×Âc.V^j\x001d\x0018\x0018Æ\x0000\x0012Éðð æBNØ{¿Û9ÁÖmmÇÜd\x0013¹n[ØjË`ãõ\x0001Ë×\x001e^jæc¸'QñDÚ¤E{Nz5
G ê\x0013<\x000cIäÍ»c·;§</p><p></p><p>n¡^\x0006\x0008DÑ¸äÀÀ¨!*T$;§5ÕÀá4²Ø
pXMQÌz0È`Ögeµ\x0002\x0006÷c(*b²\x0007$Rp\x0014
:{¹'²\x0012\x0014yöË<eì<>88!U¾k&\x001b\x0002|èÍcppXeç\x0011Ì©\x0014\x0014ÞÎ<}+%«ádúõØäË1¼j\x0006·òhxiYÅ­\x0003Ã\x0012\x0004Ù´´¸¸Ìñ@Ì.§ØíamµelØ\x0011nn\x0015jº)°.ðëÕ¾_øà¼p$\x001aÞÈ\x0013Ä\x0008"Ói<Ñ\x000bG áI\x0014\x001c\x0002Ú\x0005+Ü[\x001cµvNu?ÓÕó\x0004E1M/\x0006\x0004¢­h\r``Ô\x0010\x0015Ë\x0001\x0018îÜ¨U¹\x0019iÊ{å·\x0003þ\x0015'U~^\x001f\x0014ìI«5\x001f(Þ\x0010Èo\x000fP×Â;bw¿\Wï<^F]z~c² ZËI¼\x0012\x0015W\x0015Á*?Î,£\x001f-8SÖøâå\x0010Ðh`¼À¨kjê\x001c\\x0018VvM6aë¬W[\x0006¬÷_¹Öï+3ú"c\x001aHÕ'P\x0017®\x0004­'\x0004,Z®Ó2¦á\x0008T`Ñx¹Kã\x001e@ª7ÚóvîK-)o\x001e\x001e\x0019Óôb@ ÚÆ%\x0007\x0006F
Qµ\x001e¤JeÅPpf½/</p><p>VJ®Ü|eD"EÑÿ\x001e\x0015¿U¦\x0015³Ôæ×t\x001a\x0002üÆ\x0000b,(¬µw?u$â\x0002?«.1£6.ùZ\x000cïJ$·êxÔ ð3\x0001¡E\x0014º ¨´¾ÿÅ\x0010IPLæÒ·ÈQ~Gü}ò½ý\x0013=\x000fó<|â\x000fyÅí§q]i\x001cG·è-v!\x0004soC ÍD\x001api<#\x0000¦àH\x001eröÀ¨\x000b»\x001bm\x000cµvL
b>í{©éÅ@´\x0015K\x000e\x000c\x001a¢b9HßÎ»Æg</p><p>0ñññ©Y½knï34p\x0008D\x000b\x0018\x0018\x001c</p><p>eßMÉ½\x001cªÃ¿\x0012\x0015w)U\x0019Ì8\x001f\x0018Vâ\x001btÚÛ?×Õ#5¿¨¶¿PæÒ(\x0006êº®¾9ô\x0004_ØzïáÃÇ<\x0002È:?Ë.\x001f=\x0012{êê[øivÎ¡ËL)@¤ñ\x0004,JV¶ú+ÉKL¼­\x001ch;¢4½\x0018\x0010¶¢qÉQCT,)\x000bÅäH$I#\x0005ýé#¯õ\x0001Sâ:5òf\x001f¢(ðdÐNÑ\x0014oÁ/÷÷÷


\x0011Åï+æ0õº©ÙN\x001f>1èÒ\x0010È\x0007¸ç»î\x0001z^4ï2ëäeFlEXô \x0013ç\x0016ù\x0004æSý²Ý}2÷¸ÌÊ¿ú¼@îÒ²­£¡±e¿\x0007³¡Y4Ê*^^ô©=A2	75·P|¢õ	\x0014\x001c0j"\x0015G¢àd.­\x000cÐéõ¶l\x001b×ò&M/\x0006\x0004¢­h\r``Ô_U\x0014Ó\x0015TÑsäÍþû/ßj¶ïr]\x000cD"CCÃÄÄÄéÓRô÷ÿ\x0005\x0008\x0004òÁÒ,ìÞK\x0013Ð\x0002¢¸\x0015'Ø\x0017Cg\x0003ÃKü\x000b<\x0003²Éô\x0003Ô4gd\x001b\x0007vzvußs¹Kc2¾}»ÕÂÊÏ7$£MÔ=<2Êú\x0015Ó.eFÝÞ~Ïq>\x0011¸4\x0010i\x000fÐ*C¢üm9ÙtkÄv§\x0014vR¥¦\x0017\x0003\x0002ÑV4.900jå ¤¹¹¹ªªêÁ\x0007 ¯PÖ\x000e0ÒÞÞ\x000eÎ¦ÑÑÑêêj¡P\x0008¾\x001d\x001f\x001f¯©©\x0001}}}</p><p>Ý\x001d\x001bû\x000f»e\x001e\x0013Uq\x0004ìDE\x000cà6LRÅ­3¢\x0002UE!P,²4Ú ¥Q\x001aJ6\x0019A\x000b(j¥XlÐfq°Ð,Ê4.8¸ ±Ûep\x001c\x0014lhLì6%à®ìàBÙa¾ª\x0017k ç\x001f2QJûåäæ¼ï{ÞÜwo¯\¹\x000eU*×®]kllÄ\x0014Õ¹²²2==ýÌ3\x0014îÞ¾}û\x001fja	*ëêê£CGG\x0007Ú^½zõÜ¹sp\x0014</p><p>\x0005ê[[[q#\Ö××www\x000f«q\x001a>¨\x001b~Z}úô©æE>ÖèCèê?
>,Ûy&=³vçîêÄ*YÒ	aüÑHé÷[\x0005%!Û7\x0017ø|½çàáK]}jVmùææ\x00167¸/VI~¬ûùÙó.åÐ\x0010~2( B#p5~=çk~`{Ì\x0011,\x0011h-^`#´ñØÅÝR\x001azJÛ\x001fh¢JëCÄ8Ä\x0018·ú0R3ÅÒÑÑáp8êÃHÙßßO§Óáøûûc\x0016ÜÓÓ\x0013ygg§\x0011.Õ4\x000eÊÅ¥\x0003ò\x0001}}}+++ª9ÇÓy/WW×çÏëüàçååt\x0004\x0002\x0001:D"cjjZ[[KÑrDDÄÈâÂÂBCê³õcü4>j~¼Ã.&W%§UÇï<%ÝñwüÈvqé_£J"</p><p>üCó6\x0006g{p¿ý®ô\x0002XZù¥Z}dæ\x0005h/¿´´¬êõÿjø¥ùâÎÝ¶»g/ºT\x0014­þ¡aìê|\x0019\x0012bÁRS4\x0015Ñ`i\x000bf+Zê\x001cÏ
+áÇ\x001eÕöÇ "¨Ò:ä 1\x000e1ÆíC</p><p>ç\x000eFGGGK«ªªàïÝ»\x0017ù¤I\x0000Ì}üø1r___ä]]]sçÎÅ¬®®n}}=\x001cÐ5øyÕªUX888hhhhkk\x000b¿¡¡\x0001e^^^.]rww766noo/((
\x000e\x000eFCÜ4..N,\x0016cU~~>\x001c@rnnnFFF]]\x001d:$$$ÀDMrr2ngffJøQQQðãããQy÷î]êE\x0008K\x0013\x0011}â:}ñg^ôaÑ</p><p>yÒ	QBy´ìHDÌßBùß\x0005n=°)$\x001báã¿ÏÉ;é@ñ¹½*VªYº¹³FJgèvÒÏW\x0008h¶Ñ6\x001eq«ýÓýÃ³\x0003ùy\x0001Û²2\x000bN\x0002§©</p><p>¦SîL+´dFÒ\x0018\x0002 4)ÄHg-Xb\x001aCücÜº°¢`A¶?\x0006\x0011ÑDÖ!\x0004q1n\x0007
KÛÛÛëéé\x0001L&ØxÎ9S§N\x0005	óx<¥ûøøP,mbb\x0002`\x0006Í:99¡	ê\x0001ºnnn\x001d\x0018\x0018>}ºµµ5òêêj¬Ëå¨yóæMGGæ¾ _LíÞ½[ãá455|¶ÄÄD</p><p>\x0002È[[[áóù|ä½½½#5#\x0011\x0011Ñ'«5-¼È#Ñòò\x0018yÙvIéÖèC!Û\x0002¶äm\x000cÌòõßã½!ÝÆpË.8ýâeÏ»Q,-£3E\x0016,\x0005[\x0002*o#ü|Y´éR¾é2þ¬ÅáÖn¢¦¿{§âh,Á¹ÿ¥]\x0014XÆ\x0012Ñb\x000b¦ÆRÅ|¦x¡C<wKQ\x0000ÿ¶?\x0006\x0011ÑDÖ!\x0004q1n\x0007¥¬X±bÞ¼y\x0011\x0011\x0011`T\x000eC10\x0008ÙÏÏ\x000f³\x001aFÞÓÓóÙgy{{\x0007\x0004\x0004À¼xñ": \x0001Kcvpp\x0010,mkk\x001cðl``©ÈÈH</p><p>¤JåÛ·o®_¿\x000e\x001f¨¼¯¯\x000f\x0003G$\x0012R\x0000³¬¬¬¦¦fæÌè\x000cðSRR\x001f?\x0003t4\x0011ÑDPUMK\x0000ÿh¸lèàÈâ ð\x0002ÿÐý\x001b6g~å·Çs}ëWß:®Þ¹Ä^²wÿÉç/»G³´ÎP±4@ZEÔª\x0011!úh\x0001#ÆÊE|ë§_)~§TbÌ>pÌ\x001dEc</p><p>év@h	(Ú%1·,°\x0013/t\x0004K\x0017ã1´ý1&ª´\x000e9$HCq;hXÚÆÆÆÄÄ\x0004Ä;{öl`*.ÛÚÚ\x0000G³4(\x0017,íåå¥P(ôôô/_\x000e\x0007««ëð{f0\x0018TÿS§NQ



ËËËá¥1Ö××ÃLJJ¢`ÌÊÊÒ\x0019!Ü\x0011f\\Æ<yr^^\x001eÕ6**Jã\x001b\x0019\x0019á\x0015¨\x0017!8MDôëtmK@äáÐ¨!Û\x000byaù³×\x0006dxoÜ½j]*gM\x0012Ûã\x001b\x001b·Dµ 5«âÙ\x000b°4¸Xù_fªY)FÐ\x0018B\x001a3°1³^ê*nhºG\x0015c\x0011þ\x0007Ùùåì\x0005\x0000oºDÍÒ\x0012n'3·.âÄsÃJ6\x000b\x0008K\x0013\x0011ýÒ:ä 1\x000e1Æí aiÐï)SdffN6íüùóÝÝÝ U\x001e7<¥{zzPÉf³Áß·o±±1Ã\x0019\x001eÍÒ\x00146?yòD.ëêêbU{{;u»,ýêÕ+999pRSSkjj.\¸Ðßß\x000f3!!\x0001fll¬¥¥å¬Y³úúúp¶\x000e¿gé¢¢"\x0014_¾|2	H\x0013\x0011}ú:÷Ã\x001d^ä÷\x0001á_ìß°9ËÇo×útW\x0014/w1W%XqäK\x001ce´Ú¾+óÄïXÚi
(Z¨¢h¦Æ\x0001HÓ\x0002:ÂN`f\x001dõ\x0017\x0017Ñ­¦{¨W³´jT³4x[B±4]
Òtvì\x0002¶tÛ\x000enØÁpi¹¶?\x0006\x0011ÑDÖ!\x0004q1n\x0007¥1~ÁÀ¯_¿Æ1¤P(0õàÁ\x0003¥1«aiä\x0014K;88`aGGÇ\x00193\x0000Òúúúîîî\x001d\x0018\x0018@\x001f&Ií£G¨\x001b%''£ÃÙ³g©Ëß±4sssá466|¶ÄÄD¸;\x0019IPP\x0010åS,ÝÙÙ9²xà4\x0011Ñ'¯Ëu¿\x0004F\x001fÞ\x0014Z°Î?cõÆtu)Îkv²=¿±qÙñgGÙB¶\x0018ñ¥#YZ\x0005Æ?5·pÖHi\x000c¡*@Ñ,P4Æ\x00185KÇ¥ºo5ßSfiK¥Yb\x001a@\x001dkn\x001fk¾Rnf/[æ½\x001bV*ÛuRÛ\x001fh¢JëCÄ8Ä\x0018·¥Y,\x0011°Vã·µµééé\x0005\x0006\x0006R,|íÚµÈ{{{
\x000c\x000c)p¥ YWW×ÛÛ\x001bÎàà è\x001ad¼¶¶ÖÄÄ\x0004\x0005 d___Ý¼yj\x000eFCL!×°4\x001cÀseeå±cÇ)yãÆ
¬rqqA\x0007@5r>\x000f?++«¢¢¢¼¼\x001cØO½\x0008ô1~\x001aDDD\x001fJ
M÷·Ë×æ¹1ÍÕ7Ùqu\x0012Ë=asÜb{ùBÎ\x0012-dKL­ø#XZ}­fi\x0019\x0001x\x0016¢éjÆhÁ±`	ç[\x000b¬\%
`i¥ò=Kÿ\x0006^´RHcIèl)-£ÙË\x0001Ò4§x³±öë36\x001dÊ,¨ÕöÇ "¨Ò:ä 1\x000e1ÆíC</p><p>ç\x000eÅ\x0017T)¬\x001d\x001a\x001aÂxÿþ}8\.\x0017³\x000f\x001f>Dîææ¼§§\x0007¹
jpráÒÌÌ\x000c\x0013fÿÃ~ÇDeaÜ5Q£Ñø\x0017ft ^¡ØNkÄ*@ª(°»\x00077l±µív\x0018q¡A[d¢\x000bA\x0007\x001b²¨ÑRÅb1#¨M\x0001±Q\x0010\x0018l\x0018\x0014\x0008. h+ÐT\x0015\x0014ÎWïêK\x0005Zqz¨ar¿Ü{Î¹Ë{É}÷÷ºººàÏ;\x0017~nn.¸zÔ[\x0001§±\x0016&Gª´´\x0014\x0011©T</p><p>\x001føöÀ\x0003£\x000cäíí ¯¯/|\x0014c\x0015\x0015\x0015ðMLLPïééiX|âÄ	\x0014mÿê_\x000c**ª_Qÿh|â\x001d¹ÎýäRHÛeòO>-\x0010KçÚî6\x0017\x0006ò\x0001æÖ\x0016¶»g,ð</p><p>?ö´íEoï\x001b®¨¬\x0012¯\x000c4[ìmfåcjåcf\x0005ÇÛToð}cé3_\x0012øC\x0005XºOÿMcÛ£	ªD~|\x001bP´ÔÌNÊ\x0013\x00053b\x0019ß>g'ûý\x001fâ×{ÍøË_ý2¨¨Fª\x000e9Ô¨

ñ8ô¿U^^^VV\x0016®-ø¸êìì¼páÂ­[·\x0010\x0001¾ªTª\x0012ø\x001a&===??\x001f>ápPnJJÊõë×	gffb62Issstt´¿¿RRZ­&CÐ>{ö\x000cCª««¹Èýû÷±\x001cÆb\x001b¤îÝ»ÜÞÞN \x0019&&&blUUUjjj\x0016+\x0014766mS¦¢ú\x001f×:Ã\x000f^þzÇ\x0019ÉýÁ\x001fÙ\x0005Í±\x000e4\x0017\x0004\x0000¤ùp¬\x0003,lfÌß\x0019ú§ÇO;ÀÆäûððÁÃo¶)æÛû~,\x000eøØÿ­ùÍCk\x001f0ÇÆoù×{ÿ^×b=K£í×EÇ¤Ì\x0016\x0005ðl¥Ý\x001e8±1ö¡<ÜÂQ±zrOòÝª\x0007Æ~\x0019TT#UF\x001cjÔÁþ­Ca Ä\x001f\x001c\x0019ì¿?Ë6Û­©©	Í¡û{{×Z\x0004Îßÿ\x0008ý\x0006\x001aÐ\x001d¬Y0`·ïSQQ
]ø,I-qóIZºîÐ<ñ\x001esë@¾ aAZÓBq Éü\x001d\x001eþ	\x000f\x0002¥uz.Öõôô\É+9~èê`lÚÁ¸4¶eýØè´K9%/_uêÞJ«Õ\x0004ÈO2vR3»`F,cÄ!\x0000i¾}¨é°Å«£]¶)÷ì¿Øöì'c¿\x000c*ª*£C\x000e5jÃ`C?\x0011	5\x001a
n«Þ·Âe8\x001c\|ìÅ¤EV­V\x0008i	O"8s\x00115+8\x0018\x0005§¼¼|ôèÑ...ðÉX-+LQd!2\x000fÙ\x0003RÜ\x00064¬8vå6Iâ»ÅÌd y\x001cDz\x0007Éð¡¸\x0007\x001fPiÙÜ(îE\x0019¥,MEõ\x0001ÂÁ)ûÛ^2³ÛÉíC\x0000Ïæo(:\x0001T\x000büÍ¾3-½Ä«ÃnÞ¾¯ÑjÙ/Ð¯\x0004N¹®W£ëÃwC«¯Ó\x0012§_×Ë\x0012t?êzûô~}CãJ×}<»=\x0008 \x001dÊä|q\x0018#	cìÃþ°ÖýTRVYW·ÚØ/j¤ÊèCÚ0Ø\x0010\x0003ÇSÀù£\x0006d\x0007LÅ!httôÖ­[\x0007\x0004ß¿Ð\x0000R%>)\x001b<ðýcß¥wÍÉqûàâwu©¨¨.\x001cöûc®|³3ÉfÕ¾Ù6zf\x0004~|¡\x001f#ðå	|ù\x0002_Fègú×¾Ãé­mÏÁÒÄ8¢þEéktú2üðvvu\x001d:~qÞ§2¾Hf\x000e\x0016òíå|ÂTòýåQ.ß&nõOù±á±VÛkìAE5RetÈ¡Fm\x0018lÇ»222bbb\x001f?ÕÑÑ,n%´uuuG\x001e?vìXaaákÉÕöàÁ\x0003d+++áúK.\x001d9r\x0004~AA\x00013))	Ã1\x000fj%AÌÞÚÚJ\x0016Bª¦¦\x0006SÕ××-577£{çÎ\x001dö¢ÔCoQQÑ®]»6lØ\x0010\x0012\x0012R[[K¶\x0014</p><p>JKK1­J¥"coß¾\x0015±Ê1VpÐ½wï\x001e\x0016BYNN\x000e·Û¨¨(ÌéîîÍ½öööØØXmkk#¿\x0000à¹É~(QSQ}ppp rò«<ÒV¹ÅÍ\x0004\x0003¤AÑ|¡7#ôaØ\x0016\ýÛE^Ï¥Ii\x001dÏ_ö\x0012ÖVgàsíToîå«î9e¢µ{y¢P¾XÎ\x0017+øöa|0Æ!q\x0008ÿÌ5þK÷Ä\x0018e!@\x001ea*ª\x000fÑ!\x001aµa°!\x001e\x0007Â¢p\x0016.\8Ê@3fÌ `	¥¤¤\x0018¦\x0008jYÁA\x0019\x000e\x001dzÍ"1'O655Å=µ~ýzÃçÏGP"\x0018\x0006§OH\x0016\x0002Æ#ráÂ\x0005Ò½rå</p><p>º\x0011\x0011\x0011¤+É\x000c\x0007N0áÌ3úÛåðE\x0016xCC\x0003º\x0001\x0001\x0001£\x0006	Si4\x001a8Ë-#s\x0018ÖlÜ¸Q­Vcªª*\x0012ñððxÍ\x0002@uu5ºÛ¶m#O/b*ª\x000fVûWûcr]½ÎI\¢fÛú\x0003§ùÖ¾Ð±\x0006N«õ6Ër§Ø94þLNõýÆÎ®®¾>-ËÌý\x0006üL¬W\x000fÑ}Ú®îîºGª"Ç¯¢x"\x0019#ó$a$qP;ñ$ÅÎ\x0007×z(=\x0002+j0±ß\x0001\x0015Õ\x0008Ñ!\x001aµa°!\x001e\x0007\x0000!î\x0014´K,\x0001\x0003'''\x0003eÆ\x001d;~üø7o"®T*-..ÎËË«¯¯ÍB8ØÜÜ\dÁ-\x0001cÆ¿iÓ&¤ÒÒÒ0°   µµ\x00155ÎÎÎãÆS**J.O8\x0011zõêU¤N>ú\x0017/ö³ÊÏÏG7::\x001a>v2aÒÓÓ+**bbbruu%µµµØí¬Y³P\x0013\x0017\x0017\x0008j0?Êgdd¤¦¦bç\x001d\x001d\x001d\x0018\x0008ÈGM{{ûÌ31$$$äîÝ»×®]³±±AW¡P`ó`iÌ.ÚÊÊJ<oMM
Æúøø`,ý¿ö¢¢úÿ\x0017><×oÖzÉÒ¾üöôb'\x0005_èG\x0010ciFèv¦¥×|{w¿¸SIWsó(¸QUx£º°¤º ¤ª@ß²V</p><p>«Ê-,Wª</p><p>¾µt</p><p>3]\x0012ÌØË\x0019ç à9îå;*\x0018Ç°>pÞrú+Oå¹ôÒV\x001bû\x0005PQl\x0019\x001dr¨Q\x001b\x0006\x001bâq ,
ÇÊÊjêÔ©\<++\x000b\x0018¹|ùrø`iøÙÙÙ£8¼|ù2!X\x0002r£ÛÒÒ\x0002°4ü\x0001Ø9
EEE`o¡P\x0008ÿÔ©SHa9\x0002K£\x000boii	\x0002\x0007!sóc¾¾>,\x001aT;w\x000e\x0002Ãåx<\x0005×}ôè\x0011*×¬Y\x0003\x001f{¿{÷n.\x000bÒ\x0006{O6­§§§®®Ð;Z''§×ìo\x0002|///øä?b/j°º»ÕÊÔ\x001b[üWº%,p1\x0002ð3ËÒÖ>|}ë\x0008\x0018Ût±÷LËï,lý\x0004N!¢UabgxµÂnµBôÅ^»/"ìÖDÚ­Ù'r\x0014:Ïu\x000ce-5³\x000baAZÁw\x000c1{\x0019ÇïùE8l]çqV~àÏ>§ê?Ñ!\x001aµa°!\x001e\x0007¥\x0005\x0002Á)S:;;AZ­\x00169sæL4	\x0005 h0äÒ¥KwìØ±}ûö'O Qsrr\x000f²U*\x000f\x001f&snÞ¼\x0019)777OOÏÈÈHd\x0011\±b\x0005­­­\x0018®V«\x0011ù'ûå\x001e\x0013uvÅq­¯¨D³hL¶\x0002ó\x0000Ý´ÝÆ²Ê0À0<¬º+\x001ay*\x0002®º\x0015\x0011å¼\x0007lEQ\x0014uy4\x0014\x0011´Â*\x0002¦ÝºÑ®\x0005ÒX\x001e</p><p>H\x0004Q^",/\x0019~gNüe"º¥]d²ëýæäæÜsÎ}Mr÷3fff3gÎ/ËµYúæÍè&''c?( Þ\x001e\x0019\x0019QiD54'H\x001bãèèJ<6@úúúB¡\x0010\x000eº\x0008bó\x001cK;;;£¸®®\x000e KÁVQP]]ÝÖÖ\x0006çÐ¡C®®®pÊËËá\x001c8p`\ÃÒSôAbbzOoKSsÇÑ37Üýäë¶ù4LÍÒ¦\x0004"\x001a§\x0005è\x0002§EþB³\x0000þ@ýO\x000e}ø;¿å&\x0007øÿÒ$àÃ5A¯,x¹i°ø0Ï"Z(\x0015Jcø0k tÐÚx\x000b³NÞ8|©ìßTªQ]\x001fé'/C\x000e3fÓ`¼\x000e¯±ôÐÐ\x0010"`W´666@G@cAAÁ\x000c-ÕÔÔÐ(âÉââb\x0004Ï; ¦%g×®]Ü¨+WRXº««êÁ±\x0004«ÝÝÝ¹¹¹ÄÒ/5"ÆÌýýýp\x001c\x001c\x001cPE±4%æøð!eñG 55\x0015x\x0002T¢500022\x001aEÝDÈ(ogg\x0007\x001f\x0011:\x000efCMll,f¸{÷î³gÏõ÷÷ohhceeE¯¯ï8ci&¦©ÐØØhÕý'Ç</p><p>Ý|åkÝ-
\x0013\x0000	§MÕÆ7
\x0010\x0006òE<8o\x0016$\x0014\x0007\x001b</p><p>,Bùa\x0002IÐ*ÜL\x0012%D\x000b¤1j³	¬Õ\x0008Í³7Z{ÄÂ)ÙÑ+ëÅßT\x000e)FèÇÄÄôc¤sÈaÆl\x001al×á5\x0006\x0012¢]¶lÙ%Kºví\x001a\x00182!!¡±±±¾¾^¡P\x0010ëj³ô3gÐE\x0010R;wîDêÎ; Ð¦¦&B_bé\x000eÔ\x0010ß®X±bÞ¼yð/\¸\x0014SitëÖ-tO:\x001d¢\x0000eã\x001aÅ\x0012Ükm`cë¿Ð\x0008­­í¸úV×p,MÝööv\x0014lÙ²e\úÀæÒÒRøØùðð0\x001c`6</p><p>°á\x00168¨AÐÅÅ\x0005~TT\x0014Ú}ûö3fb"á</p><p>Þ«?pÍÍ÷Â:·äU6\x0011BÓ¼Õþ\x0002P´H
ÒBQ0O\x0014d </p><p>44\x0003T\x0007óÅ!<q¡E(O\x0012Æ\x000b¬"`|+8Ñ|«\x0018¾4V 	\x0001ÒÖq\x00028ãõ´ÜìäñE<÷êw/\x0006FÇÆ°¢®\x000fÍÄôÎ!\x0019³i°I^\x0007bi´«W¯^¼x1\x0017\x000f\x000f\x000f'nD*//\x000f~~~¾ö(bi´7nÜ@633ËbBJ\x0011K\x000f\x000e\x000ej\x000f$&\x001f?®««+ü\x0002ø±±±:}ú4ºÙÙÙðíííáËårnªäääºº:8&&& mÌàää\x0016ð<þü§OÒrÄÒÜ_\x0006¥\x0011¡å6nÜÈm¦¤¤\x0004S\x0019\x001b\x001b£\x0018ÿ\x001aõòò"áÂzzzøúúrgäÌÄÄô6©oÓ¨</p><p>8\x001dXày@¾É3uÍ\x0006Ù</p><p>q`M @Zm¢@°4Ï,'\x000e\x0004EóÍCyæ¡jæK"yh¾$'æYËøÖq04N`\x001dglwäãÇí¶§8ïÍÜ\x001bséziwo\x001f}\x0004~¼t\x000e9ÌMMò:p)\x0016gÏí©ÑªU«\x0000\x0002 ¥¥ci0gDDDPPÐÕ«W\x0011\x0004'1°°°\x0010Y\x000cß½{·Gzz:²ÃÃÃH\x0011KûøøÌCBB*++9vssÛ±cH$¿téÒ\x0006lãùóç\x001f|ðÁÜ¹s###e2\x0019ð¨\x0018£îÝ»\x0007ÊEñ={6mÚ\x0004ßÁÁ¡¹¹\x0019ÎæÍ¹\x0013edd \x0006\x001fÔ××\x0017</p><p>äc\x001ebiP7"Ø¿­­-ºæææ'N\x0008\x000e\x000e^°`\x0001º8/²µµµ´\x001cMÏÐ\x0008,Mc§ìÄÄô~¾B\x000fN~ùµWàeG¯¿Ø8Xe\x0017e,\x000eæ©A:\x0000 Í×P´!@Ú2'\x0001HG\x0000¤Õf\x0015-Æ</p><p>ld|\x001b4pZ&´ÿhÃQsòg;3¶ûd\x0007ÈòþQÑ÷b\x0000K`!]ég"C\x000e3fÓ`¼\x000ex_\x00082---g¼Ò¬Y³@TsåÊ\x0019ZrwwGP©\x0011\x0006\x0016\x0014\x0014hg\x001d\x001a\x001a\x001aÅÒrss\x0011$æ\x0004D¯©©¡	Ñcõôô(\x0005¨ÎÌÌäREEE\x0000cn ©©)\x0008\x001c\x000c\x000c?''\x0007p;88\x0016ì=gÎ\x001cDB\x000f4±4÷¡­­Xþ\x000etvvÚÛÛss.Z´(%%e\ó¸×××\x0013KÃÇ´]]]´º\x001f"tö©ý411½ÏÂ
}ÒÜ!Ïû.06ÏÃ÷ýç_Zn9öÛßÇ¬	ÐâPCq¨\x0005@:'9ÌDð$Q|«H\x0014\x0016Ã·\x0006NÇ\x0019¯=òO\x0013L\x001dÖz¤:í=ï\x0015sììßÊï=\x001aR0fbZé\x001cr1\x0006äuxùJ\x001e=ª®®®«««­­moo§,h\x0013mOOOUU\x0015âÈ{£¦4°··\x0017YÄ)ÛÚÚ:¦\x0011RÀZ¤ê4Âð¾¾>\x0004\x001f?~LA*æ\x0016âp\x0017\x0005\x0017/^ÌÎÎ\x0006Ík^Xâ^ÚIaaáùóçoß¾
¾E\x0004Û®¬¬T(\x0014/µµîß¿OsÒ¶¹Ôðð0ÙÔÔD¤ÕËÊÊ²²²ñ´\x001f\x001a9±Ïææfncð±öñ§î³ÄÄÄ¤þ\x001c½\x0018\x0018¼[^~Ó7â¯Û÷goú<ÍÖå¤È>áãu²lc­£¤ÑB«(4Jh\x001dcd\x0013kd\x0017»RÐG?Ù|ÂÒåì\x0006Ïtç½»\x0003r"]Ï/úWK[R¥¢O®\x000fÇÄô³Î!\x0019³i°ÿéRL|hÀ\x0004?ü\x0006½1KÁ\x001fHicZJ\x00113koãm)\x001a;qQí%8âÈÄ\x0004Ò\x0013+Ù[ÌÄ4
Ò\¾±®Þß>Hþó7Á²¯¼\x0002r¶íË²ß¾Ö=ÅÚõ¬¥Ói\x000b$sã)\x000b§Ó­çì¶§~¶3ÝÉ;ÓÓïâþÃãN\x0016]ºVÖðä\x0019(][&¦w$C\x000e3fÓ`¿\x0011ôÜ(Ê\x0011´DÑ\x0008ÂQi\x001e#ò!®(C\x0001\x00059\x0011"NL\x0003i\x0014­EKpRiôRK4\x000fÍ@\x0011ª¡.ùJ¸%´Ë £emV§³p\x0011îtÚK¼±¦â~×xijû×ÝÓ_QÝTø÷óÿJ,:\x0018}uOðå\x001d\x0007å\x001e¾Ùî>r÷ýÙ\x001e~òÝ¹>áy¡ºòuÎWeßÖ=mí¤¯
\x0013\x0013Ó»Î!\x0019³i°I^\x0007\x001b¹6=¾­f$É!¨öÌoáµÈÄEß¶e\x0013³oÔäSoìþ×ã311ýßÒ¾kJjH1ÒÿBÑÛ7ØÝ;ø}ÏÀ÷Ý\x0003ê¶g°§w°¯h`pxdDIÿsÇÙõdbz÷Ò9ä0c6
6ÉëG\x001e øøø­[·fdd ¨R©\x0010	\x000b\x000bóööÈèè(ÚÄÄÄmÛ¶\x001d=z\x0006fee¹ººº»»»i\x0004\x0007ÝòòòÎÎN8999(S*hóóó×¯_ohhhbb P(«\x001f<x	===[[[éé¬ªªÂ6Õ\x000f¨R¶±±¨¨¨à%%%ÿa¿\@¢Z·8î;5C\x001d¯c\x000fÇGYùÎ\x0017\x001a$ÑI\x000bÊÊ¬H\x0006/d©\x0015FÁ%èÞL»½;Ýà@\x0004uÊòvHº]êôP0</p><p>S3AÓÁ2É´ÉçèdçÌýY´fÒ3vm¶³þ,>Ö^k}ß^ßÌþöü\x0006·¸ÿ>|êV£Ñäää`5Lß°aB¡èîî\x0016v÷mÞ%,\x0016Åbý\x0019%:ä°±ÁL<\x000e@Mâä°°0\x000b\x000b\x000bGGG¥RI ëëëkccCì</p><p>©T*dQckkÛÖÖôôt\x000b#`\x00058Û·o§[Ò)åîîNÎÒ¥Kûûû±æ­[·(¡ÕñùÍ7qKµZ\x0008Øj²³³)±¸¸\x0018³gÏÂ\x0007EÓ(H\x0010´¶¶ÆèììÜÑÑéØ\x001d³4Åb±Xã(Ñ!Í\x000cfâq\x0000g1ÆÅÅYZZB\x0015</p><p>\x0005Å\x0017.\èáá1<<L\x0005W®\A6&&\x0006caa!"íííMMMõõõNNNÍÍÍ


\x0003\x0003\x0003uuu\x0000ÚÜÜ\¬SYYz//¯;wîQ³zõjDöíÛìíÛ·Qiee\x0005>¯®®ÆÊËË\x00119qâ\x0004Ö'H\x000e

E\x001b>>>2\x000c\x0011bc4²óçÏÃ'ÚG|Ö¬Y`þ®®.ôAÅb±X¬ñèÃÆf\x00063ñ8\x0010KÃruu
\x000e\x000e\x0006£\x0002k\x0011\x0007º¹¹T©`Ýºu`à\x000f\x001fÚØØ¬X±B\x0005GGÇE\x0016	§O¢rçÎðÓÒÒàÁ\x0007îbìîîH$R©\x0014\x0013ïÝ»,0\x001eãòåË½uë\x0016ücÇÑÊ¸Ü¶m[^^\x001e\x001c9±ñåËqYTT\x0004\x001f\x001dbDX\x0013ý\x001bìô¼0X,\x0016Åb}&Ñ!Í\x000cfâq\x0010X:<<ÜÓÓóÆ\x001b`Ô\x0004D¥5\x001aV\x0007À\x00020ÇÇÇÛÚÚ¾}ûö\x0017úûû\x001d\x001c\x001cbbbà\x000f

aÁ\x001a,â   {{û\x001e4</p><p>hµ¤¤$\x0014`G\x001eÁùþûïSRRà<yò¤ªª</p><p>ÎñãÇ©½Ã\x000fãòñãÇíííprrr(^RRbÀÒ\x0018½½½§Là¦ qt ³4Åb±Xã+Ñ!Í\x000cfâq\x0010X:**jêÔ©¸\µj\x00150õÁ\x0007\x0017/vqq\x0019\x001c\x001cD°´´\x0014ÁÊÊÊ¬¬,øÅÅÅ©\x0003\x0003\x0003ÀìØØXí'¬Õgi¹\îää\x001a\x0002o\x0014`Ü¼y3</p><p>^¿~
H&nii³lÙ2Ü\x0017\x000eH\x0018sQ\x0019\x0011\x0011\x0001<.//¯¨¨H$2L­V#uùòe\x0015\x0016\x0016¢\x0001ð9a³Í9sð§ //YÅb±X¬o!Ñ!Í\x000cfâq\x0010X:22\x0012,
¿®®ÎÊÊjÑ¢EÁÁÁnnn`id×¯_oñ¹\x0012\x0013\x0013i:àö,½k×.ø(_]]
°\x001c½½=AæÈ{\x0011Ü¸q#ü´´4\x000e\x001dBemm-ØØà¾wïÞEêâÅ\x0002KÓMÑ¹T*
\x0008\x0008 ÿãÇÔ\x001e4Åb±Xã+Ñ!Í\x000cfâq Æ\x0018\x001d\x001díììÜ×× B¡\x0000©ZZZz{{\x0003J{{{={öéÓ§O<Q.;99utt ¸¿¿\x001f\x0010\x000eö\x0016°\x0016,¹`iD.]º¥-[öîÝ;º#È\x0019M6Á\x0007\x0018£2??\x001f=466b\x001dÀ3"\x0005\x0005\x0005\x0011§uÚ³g\x000f.³²²0\x0011,²\x000b\x0017.À'lÆ8}úô\x0010ý­i\x0019§Y,\x0016Å\x001ao\x000e9llf0\x0013\x00038X444ÔÎÎn``\x0000\x0011¥R	T\x0006¸J¥R¤JJJàYÇ\x001fGäÜ¹sðAÚVVV\x0011\x0011\x0011ð5\x001a
ÆêêjdwìØ\x0001\x001ft½fÍ\x001a\Î1#99\x0019eð\x0001½ÍÍÍ¸\x0011X\x001a\x0007\x000e\x001c ewïÞm¡\x0013(\x001aóæÍ³¶¶V«ÕÂ}ÝÜÜ\]]1\x0011\x0014Mkúûû\x0003ò÷ïß »»;êãââ\x0000ö			 wáÂx¼9X,\x0016Åbý&Ñ!Í\x000cfâqøE'Ðfbbb``ààà .\x0011ÏÏÏ÷öö\x0006"ãããS__?<<\x000c²ÅØØØHzz:²}}}r¹<))	>È\x0019s?îåå\x0015\x0010A1ø<;;à\x001cöìVñUUU¨<sæ\x000c!}gggdd$î[TT¤R©d2B¡@jhh\x001a\x0003l{zz¾xñ¢¼¼\x001ceðÓ\x0000þ½{÷¢,66\x0016S·Ñ\x001eV£
2K³X,\x00165\x0012\x001drØØÌ`&\x001e_?iH'"OÂià+"@\ð3|¡\x001cD\x0000ÉÄÀT)P+M\x0001W\x000bKA ÛÚÚZ¥RI¨¡¹B%Í\x0005{c5D4\x001a
ñ3-KKAt/*C
Ub\x0014Ú,EÝ}Ý»â×Ïe\x001c1È²X,\x0016õgèÃÆf\x00063ýDès 1\x001cê;úH©\x001fÔ¯4^
\x0000\x000c¸\x0015úx<J'ÆÁÑyu¤¹&ðHx,lÁ8"üw\x0018}åQz\x0008zZ×p¯â!8RýÏ\x000f«P`Î\x000eY_­ú&|_o;ßÝÈ¸IÙÚÇ\x000f£ØL@§[ì.Æ¬÷Ý=h\x001bã\x0017³'(üÇáa4sW,\x0003\x000e9llf0ÓO\x00021</p><p>\x0012"ú)­\x0011:\x0012X~Ôi$¤¤\x0002ã[\x0018³+Õ\x0018ãëHË\x001a¬iÀê£ý\x001cõ#ú¾Ð³ðA¯\x001f\x0014üö¢ý½¿\x0000¢kéÔ\x001e¡¹\x0011ß\x0015]ºfP?Ö§%¢Rþ/ëÊO7ÅndÜô÷Æ0ÝÈä8\x0008tºÅîblZº>Û/~Ë?ýç¿HýÅ/</p><p>\x0013Ìß\x001bK_¢C\x000e\x001b\x0019ÌÄãð\x0015¼7ú\x0014êHY}jÕ\x000f\x001a\x0000³Aj$.5å\x0016£4iLÑ#í¥¯¯¯µµ@\x001dJ¥zõêÕ(Ó'\x0005Hk?ýÚú/£oÂ´óo\x0007õëÇôt±Ä\x0015³ô·Ó¤8\x0008¥OþPh§Ce|Å??¬2È¾ïîq\x001bÍ =A$:ä°±ÁL<\x000e=\x0002Ë´´´ùóçûéôæÍS§NÉåòÀÀ@Ä\x0003\x0002\x0002üýý¯]»â\x000f\x001f>`îû÷ïãââB\x001ceë×¯¿yó·_mdQ\x000b\x0016,ÀsçÎ½~ý:RÃ:Á9vì\x0018²ð©£©\x0019\x0019\x0019¡¡¡[¶lÑêA/\x0018÷ïß---È\x001e9r\x0004>îNm_½z\x0015\x0005+W®'èÅåÖ­[ÃÂÂzzzP¿víZÔ\x001f=zVÆK,INN¦õá`/óæÍÃRAAAmmm(;{ö¬T*µ°°À\x0006±w"êiÓ¦!\x0018\x001d\x001d}çÎ\x001dÌÅFÐ3>"êdÃ
Â\x0007;Áq~má\x0004?[iÛ÷Ò³¤lm\x0013âø3þcMLýñX\x001a"\x001e?ý\x0007R,é5+&\x001dKÓ;§ðÇ1».u[øµx5¹+Ö\x0017%:ä°±ÁL<\x000eà=âÃððpÀ!à\x00194\x0008ìèèÈËËsuu%<<<pyñâE­1vuuÙÙÙ!åîîîììLe\x0007\x000f\x001e¤\x0001Ã¸3g\x000ep\x001a,]VVF<¬ÑhÍÊÊB¶¦¦F«\x0003l¤¨/_ÚÚÚ"emm­T*µH\x001b}ÒMSSSmhh	öìÙtÒÒR\x0004gÎ)H}öQ£R©àËd2øÀàÖÖVZÐÉÉ	è«Õý§ðõõE\x0016dí¥±»¦¦&Dð	ào\x0002í®³³³¢¢ö\x0004\x0007÷R«Õè\x0007¾\x0003\x001b¤¤¤PÏÓãøú\x001awÄÒ$¿ð¥£dY\x0013\<8\x001aÓkV,M:¦ñwIìFX¿/Ñ!Í\x000cfâq äÃ\x0018\x001d\x001díââ¢\x0002j{{{{ÁÉÈârppP{»»»ÁÒßýýrÍªÊâ¸\x0014;\x0012éDî(Pn
\x0018"2\¶\\x0002A!\x0001_ N;\x0008-<`| dH >Ì\x0004\x0008W\x0015^Ô\x000cð2\x001aAC5cÌ\x0004Â¥bÁH\x0000\x0003F\x0002¶S\x0010(\x000fãß|ÿéÊfïó\x001eRk¾/û¬³öÚk­³Î·~§¤\x0004á?þXQQñôÓOÐ&:Ë/ÏËË»té{VTÏáë×¯çneee¡e-</p><p>;vìÀ0uëÖ­HËC\x001d½xñb6?ååå¬¿þúk÷\x0008>\x0007úôécqM6
,¯©©á.Ü¢E\x000b,¿òÊ+\\x0012]·nÝ\x000f\x001f.ÇÀc0ØÍÀ¾}û°ÿöÛo³\x0006Ô÷ìÙæÆ\x001b1xìØ1H#<wî\x001c«V­òý)3R>&\x0019É,\x001dÞ¥ÍUüó_¡æ¡\x001cýóm\x0017/_ñî"aäü¦Û4¥sª²*4\x001e{\x000báßvíýï\x001d\x000cw«5ÿ®EAlñÔ0\x001a:±òÐ,òXÿ\x001b\x001cnà¸áè¦(2\x000b/ûÞý{¶\x0013³±´\x001bBlê\x001a\x0017B¬ý0E±!(ÛaøQý0ýX5÷ÄÃ\x001f|Íy·`²9\x001f;¬¼± Ócÿf½J
Çs)¶°\x0011µ§zöÜN~ï¥]Ç\x001e(ö4\x0011¹:Ìð\x0015\x000exX\x001bÒ\x0019Y4\x00079(|ÊiJGÇ¾\x0017
Ö<6µÝËUlZÒÔÒ\x0016C³\x001bM\x000e9¹`¦|\x001dÄ,F\x001aÕ©S§ë×¯\x0003Ï±Q\x00068ÃÒ®¾îÂÒP%,Í\x001aÐå÷Ã\x000f?T\x0017.\ÈzéÒ¥¬O8qëÖ-4-ÅÒëÖ­ãî3g¢\x000cK\x001bO8±uëÖUUUmÚ´\x0019?~¼Ý\x0015Ks¹hÑ"6Â®¬×®]Ëú/¾Ð\x0011ò</p><p>\x001eîÕ«Å5eÊ\x0014ø¹ººuÏ=\x0007
\x001aD,¸
Æ£Óµk×aÃÉ±~ýúõíÛ\x0017Sµµµ$\x0001ÉG\x001f}ýqãÆ:uÊÂë­·\x0010¾øâ.ÃÃö\x0008KKKIÝ\x000f?ü@Ò¢zþd\x001eð\1wÝ®\x0014V\x0017
¨`dW~¥«_wu°¯S0åiÚÑP\x0001</p><p>ÝøãÜúëÎ}&){ã/\x001d6zM\rjÐ®¦Û×°;\x001bØ 9Ì^è$
\x000eÿ®à÷î¡"o£ä¦ÉBjÄ\x0005ÖøíÐXNºÆ2E±!ðpYð¤ÂsÝ"ÍRè\x0018v¼¢ó\QõÃF+cW\x0013k</p><p>ÇåolJ0\x001e[ó\x0016[ÜÐâ}ï¼ãTÃ¡&~¦yâaDÝËOQÛ\x0013\x000f_û£Nì?Cú¢"ÞØ÷"åß»=¡"Lg-¶\x0018ê\x0006sÞ\x0017]nææor¦|\x001d9_xá\x0005h°C\x000e­Zµzùå£\x000cEs÷Î;\x001d;v´»(\x001b÷ÖÔÔ \\\,BF\x0008¶mÛvøðáÜ]¾|9\x0006Û·o\x000f\x001bÃ«\x0002K¶»,
ÐF\x0019\x000e\x000fW¯^rçÌù_?7o^^^Þ·ß~«]\x000c±ô«¯¾ÊFØõ5kX·k×#\x0006\x000f\x001e,Ë\x0003\x0007\x000eµCÅÒ¸Ê­§z</p><p>®¨¨`×\x00193\x0018K3</p><p>\x000b\x000bå0A­\¹\x0012ÉÝ»wafX \x001c`\x0010h\x001f;v¬ÎÝ°aÃíÛ·\x0011={\x0016	\x000e#dûáÃ\x0005ÿú</p><p>ø¹þ»~ÀÒÂ\x001bHÆ\x0015zÕEQËxnÒlZ\x000c\x001d¶?`Ôãfgj"\x00191	kÔ¤)kÖ´ÑëJp¯Ô\x000cµ\x0011e\x0016Øá\E'.$k\x0017â\x001b­M:\x00028÷2¥%!!d\x0006}~ya·õÂçhmdêë\x0000mã\x0003±4³ÓYxlã¥ÿ´j<ÑS`/É	S×¸\x0010\x0018²¢Ø\x0010¸ë=e
1$çj{%+\x0006H'ºå§JÖ¡Òó±ÏÝ\x001d\x001c*</p><p>5ûü²6LòüTiQlL+ïl\x001fª\x001aaÔÊ¡·Q!XÝ¢oÄhïÅh»T±`þc'å\x0013÷"b¯ÇM§ûúnè1¢ú±¯\x001b\x00150©F(ßT<æ^÷NG°=|/RÖ¼\x000c«ðï\x0002\x000b¦¦Ï\x001f\x0005¨\x0007m>îgNã¡y&\x0001ÜÌÍG<S¾\x000eÆÒð!\x00108kÖ, sÓ¦MBÁ(Ã:u\x0002A£\x000cÓ</p><p>\x000eµÅXKÀ\x001býÚÚÚ6mÚ\x00181"ªgéÉ'Ï9sÙ²e¶QÄ[^^ÎÝÓ§OKÂàî®]»\x0010BÑÛ·oçY³\x0010¨Ç²ôÚµkYã\x0000G,Z´H</p><p>\x0005\x0005\x0005½{÷F_ä?uêTH¸ºº\x001a;=zô\x00180`\x0000:\x00006\x001b\x001c9Âå!C</p><p>\x0016ôìÙ³ÉÀ¶mÛººº7ß|³{÷îèO>\x001dÂé\x001b7vîÜ\x0019!ç²÷Ë/¿dÝ·o_¶£öùç7/¦ÐéÜ) ­xdëUú¦Q¦¨\x0007YÏµ¾I\x001ft54Ö_dÍíÂQ\x001cEÈçL¹\x0004%5\x001a«\x000b{j4>/\x0003
²45´ÆZm=¹EÊ\x0014G»BmôR¥õh\x0001></p><p>XZ{y4\x001eDÉ=\x0017\x0018\x001a\x0017BÊ\x0014e\x000bAOÐ«\x0010AùæeÉHÛ-\x0006lº\x001feFéÞ#eê<!jûpí[y»å\x0011ûMjÜ@­^ÔòVö±MMá{çE*¯¼#\x0004i¸§£¤Ù¹ÉnØ¡öÄ½üè}wáËøEe5ïý]Ñi»s;\x001dÆ6\x001e÷\x0001+kötÞF\x0014Có\x001aM\x000e9¹`¦|\x001d\x000cþyàÐ\x000b\x0002\x0013X\x001a¤lÙ²%´l»Þÿ}rÉ%¬ùeýÝwß¹\x0006\x0005Æ\®[·»UUUvßÇî\x001fEEEÈE°BeØ\x0015ù¹sçX±¾tékdèÐ¡ùùùv9aÂÖ­[ß¼yµX\x001aùÉ'óòò`þnÝº
\x001b6LÛyæ\x0019¶kMãûï¿Ç\x000egUVVðÂ\x000b|Mð\x0005qñâEî¾öÚk^nS>&\x001cÖmc'hê\x0011W]º\x000c»C,\x0002Ñþ<5\x000fÔn<¼Qc2e·#\x0007¬êÒëza\x0008)Y:\x0016&³ùì
õ_o/ÍCÍÛ\x0007eé4\x001dÙciïËÅ>OÜïÆà=)\x001bJ\x0001I¶\x0010BnêqÝ@ÈËWf6\HÓ·X¨ã!wìÈö¡dßØò\x0002Ê</p><p>¢6\x001cU®°/ßLMÊXXê6¼·#ÛW\x000eMh\x0013öÅê\x001d¡HUíæFXª4sÃÖ³&7Y:å{­¨B\÷\x00024.½,F×áðAK.\x000ebh^£©Ø&7sóQÎ¯ÀßÑ£GwéÒ\x0005<®Ë\x000cðUÀ\x000cK?ñÄ\x0013cÆ1Mcé¶mÛN8ñÆ\x001bW®\\x0001¤|òIè\x001aREgÅ\x0015¬Ï9µÛ·o¥×¯_ÏÝÏ>ûìúõëW¯^½wïÞµk×Úµk\x001b\x0015\x0015\x0015|ò	¿ãÆÃ>w£\x000cNÃÒl\x0017K?\x001eayy9F\x001f?®#0ÂüùóQ8xð </p><p>ÜêØ±ã³Ï>+ûôé3dÈ\x0010!î\x0005\x000bPkÑ¢\x0005	r¬   ÿþº\x0019è@é|\x0011|óÍ7Qý§ÁW_}ÅÑK.%dÓ§OGX]]& \x000f·nÝ'óIò«\x001dÖmiFî¤;¨
=~?ºÕ¥þ\x0015Û5ÔéÔ\¢zö°K\x001b!@zx£Ðs8ì­Q=ùX#«!)y/HJÖ®^¼n\x001b;\x0016ôýýï\x001d\x000c-h<\x0010KÇæ<\x001c\x001eK{\êl¹z \x0010R¦([\x0008!XâeIô\x001e>»ÐóXI¨%7¢\x0015åE$\7\x001ev\x001c\x000e?ýlx\x001f2a"Û</p><p>ÍË\x0012\x0018¾MÑýP\x0017e¯m\x000b-[ê<;±Cnð\x0008\x001aÜÍaÉYú!ÊûOpWóÙÞbW®§\x0013¾¤îxbh^£É!'7só\x0011Ì¯\x0003	¦²\x00181b\x0004X\x0008\x000cCÔÀóÙ³g\x0005wîÜA^XX\x0018eö?¡-ðd«V­\x001e»ìÞ½[KKK¹ÄT×®]ù=pà\x0000\x0006áaq&¤-}hßC\x000e½óÎ;,vìØa¾íÝ»\x0017É-[Dà\x000cÎ\x0015ÓVUU!\¶l\x0019ëÎ;ëýû÷³ëØ±c²<pà@\x0019Ç2rF§G\x001e\x001aúmß¾=w\x000eý® me\x0000µüüü7or4\x0012\x0012\x0002o³´q\x0000fÝ½{÷#G²\x0018?~<{ùdÐ¡lÄÉ'Þõõñ³üqýBCÍ+[wÐ¿5ú(¥\x0013¦ÇÒÙ@Ñ«[Y»Qcr»`;az,\x001d\x0006åÉÓ°´5îÆ½qð¨O\x0013"-]ýúá\x000f>NN+÷X:\x0019rlx,Ý`\x0008	PÚ`\x0008bÂ4)J\x0008Áã^}Í¹\x0018ìe©A·£úç0³\x0015¿\x0007ÌÞpoÉ«4/BìPb\x0005uVuª|ùæ½\x0005éK`éäÏ\x0010\x001dAþ\x0013ÜNàmï\x00117¥Ó¿wÙH_óiþ.ÿ-5\x001e²\x0018Ñh0·¹¿òu\x0010òñ[VV6eÊ¢¢¢?dÆ\x000b\x0017~Êººº^ziõêÕ¦©\x0005{¡Í¹sç²«¤¤ß5kÖ8q\x0002¹hyëÖ­\x0008'MÁ£G¥\x0019èìÜ¹»S§N\x0005;ÑùôÓO7oÞÌååËáU\x000eEí¿ìßOTI\x0016ÇßúÅø¸oúbvâ\x001fà$ûd2»ú`"/¨1QFgÃ\x0003\x001ax0\x001a\x0007D\x0007Ð\x0010!êqã¨¸È</p><p>\x001b\x0015ÈÆ\x001f	\x0012\x0008î,ëøkXuù%+84ünn¼ûMxRVÝ{ûÂmº9ßtêÖ=Uuªî©®O½}û\x00165\x000f\x001fFC¢w\x0008#\x0002YÛÛÛQ\x0006xÓè4D}}=+¸}Í5Ë/_½zõùóç­\x0018<ãUFFÆ={¸7¼Bó\x001cTff&¡®P\x0008\x0006\x0008#??ÕªU î¯¾ú</p><p>À~\x000e\x001c8°bÅeË¥¥¥uvv¢-~ÕÉfee-
¶\x000c\Q³«æÎ}\x0001·èÄÉÈÓ;K\x0013À\x0000ÕèQÅ\x000c5\x0000Ô;ÈÎN\x001bA«÷ÂÒUqgê",\x0017àD½\x000b¬Oß\x0005Zð²D	di)¨ë<Û)ðÅ*î\x0012¹L2êË?m¢G\x001aÈ\%\x001aÑ=lú.	\x0003&´m8[þýuNC¨ASt¤+\x0003¯\x000cNeºbp\x000eÐp.û£¹Û®\x000bfó\x0010îa\x0013á»°4\x0016D}\x0003Kó\x0005mÎIå=ç½ü]PxêåÎÏdXDJ9ä%Á<n\x0007"=[ÞûøIæ£\x000b\x001f\x0012¦ºwè¦\x000fúÄ#øyÓ¦M\x0000é+WB!§!ó¡ááa*ó\x0015@íÝØÁ)\x001eP=n
Ü</p><p>ÓÓÓfå\x001c&rùaiï\ç¥!\x001cC\x0018\x0000\x0010NÔ·D×N\x000c`F\x001e·Þ	*4·Ym+wa^8	\x0014¦Té´DZxþYZEÓÄNÁã\x0012¹Oú\x0004D\x0011W\x0003#Õ·Ú*Qª¸';4ºËiÅñl£­xA¨À¬EKAa Ìþ9à2wm_krád-l¾ø¨¢o\x0017\x0017tã²´å;©Ìë¼ü]Ð¥ÆýCûLE¤CX\x0012Ìû`¶*R±\x0019D\x001aHÓ+\x0016Smhv¨ö`¾¥\x001aÍFÏxlii!®««³bí4\x0004­\x0018	sÜxâôÈP\x001dý\4\x0011\x001a¦Ã`[©¶UkË¥\x0019P \x001a5»pB¡ü»/þ`6ÄÑwú\x0002³bi°D F\x0014T\x00009¨oAnf%\x0005\x0011a\ã´\x0011´z[ÞÐ`ÉR\x0008_ë
\x0018ÔGsøîRVO¼Á(â´D\x001a.úai)ÆÕÜhéO>§@¡rªhÍyÜ§@ß\x0017ÁPAV[%'¶!7Rµlº!0\x0017Ð¢\x0019\x001fh6ðù¥Ò*á!Ì´ÑDÈG¡òyvÏï\x0014tÇüâËõf?h«î;úâæÜ)`c\x001cÌ!hËSCóÏEß/Y~XÚã¾s\x001aÂ{Î{ù» +Æúô]¶\x0013YóÇt+\x0011É°XrÈ\x0011\x0013KyÜ\x000e*3k²­ôøÖ]³í\x0019hß©©©±±1+\x0006±qGñâã1$êj\x000e«Ä>\x000bV.,ã\x0006'BàÓ\x0019AÒ²Ë¶9\x001aâ\x0014\x000e(gâ¬XÎhô@Ç¨:Äox«ÕÓ1§"ÓF°vÚ\x0012\x000c¨n\x0014ê]û¬ÏEÀã\x0002¢\x001f\x001arÐDøô·E>f¶°4õoª-\x001d
Íä3ç)ÐÝ'î\x0012¹Où\x001cx\x0004ÐÞj	C3ÂmN\x0011§\x001f}S"OøhÁSÂ¨¹mf¤%\x001b÷¯¦\x0007Á°E4´Ã¦h4gþú\x0001çikhYf@!OÊmm}¸Þå;
AÆß\x000e«gî_uÜ¤õÂÒ\x001e÷Ó\x0010ÞsÞËß\x0005_\x001fÔ\x00089\x0018Þ¼>a±(å#&\x0004ó¸\x001dfE+{xI\x0005§Ç¸Ã9±h4\x001aÕÞjá¹÷\x0016×Ù©U\7Ûùñ/(Ñá\x00056X¾K3Î%>-ãÄ¡#\x000c¶ÿÈ)rÃ	b\x0012ø¬XÚútF\x0007\x001c{\x0019£üPÿÀ\x001dpy§/¿zÆ9m\x0004­°\x0019+@mÑ\x001bæ\x001a:\x0010Ù
' Õ`eh¦øÅ\x0011O\x001a§ÙN\x0002F?p.«¬&ìa\x0018`pÂ+\x001aî»Keð¡A\x0013ÂÒèS¦@KQÔ¯<·)ð\x0012aYÌ%b;\x0005¢¸q³°ì\x0012F\x000bGTÓP\x0007\x00181Sð5\x0005¯\x0001&\x0011õø¥ôÖÒ \x0013}¢g¸¡!Æ"ä6ga¿¾\x001a6[Àá\x0016\x0003£á,eß©×IÚ)\x0014\x0018Åÿ°ù'ÚÚqf\x0004C\x001ebUáL	if#ìëì\òÁ(ä£~_?,íqß¹$Ç÷øwA×+Ì\x0011ß\x0017£ó\x001aÏdX,J9ä%Áfµ)\x0018\x000b#\x0008HUcNÍGÃÈ\x0019[ÿ\x0004ûWÇZøº(Ä§­­á\x0018Ò\x0010ËÌ.Æ\x0000­!³5{æs\=UYÌªá,C$î¡ÚÖóa­\x001aº¢Q\x001bb)LÏ¸\x0014êÔ0`Ü\x0014Ìo\x0001\x0007Z¢°4Eb»tîHé}</p><p>^(î\x0014\x0008W\x0002\x0006@Zv	c\x000c quDøØæ¹x\x001e'ü4ÓÃVÍãBä¯±\x0016]+TÀfÙî;\x000c§î;</p><p>Òô47­lg¤-íï¥-ßI,Jàß\x0005ÛdX,2'(&¶ôÌç6!LÅo8\x001c\x0006`\x001cGvS\x000bó!\x000eF@:áÂycÈÖL±bgÉ·ðÄÙ\x0002Æ<¦á`Û¡S=\x000ebÛTaÍ;÷aDüâ86;qêÁ¬ÇpDG\x0014?½¥1\x0003cO²Ê\x000c.¢\x00140\x000c\x0001ÛÆ¦NG¡Kï¤_þó_8\x0007\x0007Þ»ð)Ä]¢¸SpùúN	Ã3Âçs\x0011|ð·Mo§x<¦\x0007jx# àÀf[sj4S¨ê¾CÁÜw\x001c$<yîðô>wuFX4Û¯¦Áy«ÊéS½\x001a\x000c\x0005l~>ÿI\x00157ç½ÿ]P%­§Óå/\x0019\x0016R\x000e9bbI0ï;Ñtdd¤²²²ººzbb\x0002¨|êÔ©îîî¬¬¬\x000f\x001f>h4«6¬©©ijjÂc4\x001a\x0015¾\x0015D"hÉ+å#&\x0004ó¾#\x0000À çhL\x001b6l¸}û6\x001eQßÓÓÓÕÕuôèQòRýëëëÛÚÚP®­­
BT),-\x0012D"ÑWÊ!GL,	æq;|0¸¿¿ïÞ½¨D"\x000e\x001dª««{ðàÁºuëöïß?44´sçÎk×®\x0015\x0014\x0014ìÞ½»¢¢\x0002õ÷îÝ»{÷îÖ­[ÇÇÇ©ùÜ¸"H$\x0012\x0016R\x000e9bbI0ï;\x0002\x000c\x000cx\x0006\x000cWUU\x0015\x0016\x0016Z1ÀÞ·oßË/\x001d;V]]
®...Æ«ÖÖVp5j\x001e=zTRR\x0012\x000c\x0006srrÊÊÊFGG?~Ò¼m\H$\x0012D\x000bB)\x001c1±$Çí@\x0000\x000cF933óÅ\x0017Ï?ollÌÍÍmiiÉÏÏojjºzõjAAA{{ûÀÀ\x0000|àwãÆ+W®\x000f\x000e\x000eZ1 \x0017\x0016D"è· CX\x0012Ìãv	\x0018ÜÐÐ~ùòå\x0013'N ýøñã-[¶TWWONNnÞ¼¹²²\x0012t}æÌ\x0019øïØ±\x0003\x0014}çÎ\x001d4éêêBsaiH$\x0012~#J9ä%Á<n\x0014</p><p>ð811¡¾åÇééi+\x0006Þä\x001c\x000eÕzª¤B¶©H$\x0012D¢\x0005ªCX\x0012l\x000e[øÝ»wSSSÇ¶L\M\x0005nîsoD"H$ZøJ9ä%Á<n\x0007\x0015£Ñ(</p><p>\x0003\x0003\x0003\x0017/^\x000cÃÑÈ</p><p>£££ÝÝÝÓÓÓÁ`\x0010ÚÛò¶H$\x0012D¢¥§CX\x0012Ìû\x0000\x0000ÏÄ422rüøñ¢¢"°ô'OØ°\x0019jjjÊÎÎ\x001e\x001b\x001bËËËÃc$\x0012AÛW¯^À\x0007¼Í"H$\x0012ªR\x000e9bbI0ï;X\x001a$Â¶mÛz{{_¿~ÝÝÝÝÓÓÓÑÑ1::</p><p>ÎÎÎÁÁÁ[·nÕÔÔ¼ÿ~xx¸¡¡¡¸¸\x0018¯jkkûúú¬\x0018r£yÚ¶":º{*n×>jý9±Ýö\x0007\x0007ÇÇ'\x0012ÛgB4\x0019êûµßöÕýÍ~bÆJ:½\x001a\x001e\x0019\x001d|ÿÁ½¹í}âo¢ëÍÿæ\x0014`Êä3\x0019ÐÜg\x0000\x0018W\x0012ýì³C³ÿçm¯È(ZÛ)£Ýèmß¯ÁÉÉ{çf+Ñ\x0012PÊ!GL,	æq;|0øÍ7Û·o¯¨¨hnnnmm=yòdFFF[[[UUÕÚµkQ(((xöìÙÆ\x001b_¼xWgÏ}úôiZZZyy9G"\x0011ô3¯W$Òôý_+Ï^,}öËK\x0014`	ì\x0019}úG +\x0016¡ÿNT\x0001¥¾/û»YÁÒ~zÎÍ+rzÕüÏ×þã{sÛ\x00153C</p><p>ÃÇ\x000bÏÍ-ÂTéÆ­\x001f1;?Í}\x0006$g~F9áDÙ}óíiÄ	û:û\x0010¾£í×Ä[vË>ô-jJÿvëu{{çpFÌøÅ^ V$tSHøf\x0011ÍR\x000e9bbI0ï;0\x0018ë×¯;w®¥¥¥¿¿ÿÒ¥K çÒÒÒÆÆÆ7o\x0016\x0015\x0015õõõ\x0015\x0016\x0016NLL\x001c<x0\x0014</p><p>åææ¢É#Gêêêz{{gbBWóµoE"C8ëq²óc~ñ\x0005ü\x00023*n×6ét&¡òÇúûgÿRJìC´£\x001c ò°å'â%¼E
³Ä\x000fwîÃ^¡\x0006e´Õ`\x0006þ¨'ÚQ\x0003@«?gÃ<æð¡·Ô\x0003\x001cÀ\x0018.¨DìÆ\x0003Ñ[ªGY\x0002ãAÑöÿìëKÔÛ\x001aÇÿ¯zÑ«^\x0005§Þ¥\x0011\x0014($Ð\x0013d\x0011Eí</p><p>*Ã¢%äQ*-¶I¬a·;¦ÝO!¶k{­tQs4Úof¾ø°Z3ÚtÒ\x0019;g=,~¬Ës[ÏZ¿ù}ÆÛ5úRfIá§\x0017ÅôÅÒi\x000bh,íîÔÍÄÒVL{wëÊÒ®O¬ÕµØ-[åà¼UmÁÄt\x0013°¬Ô\x0007Á­Ô´M¯PvmÈ9Qê:ys=[z¨IS~XõpÚ£[R¥wmÜ;©²0c·È-¯7o$mAÒÞaÝCõõÇÁ;M¥!\x001a¯\x001e3bi¯È^D÷^X{#è ÏÅãé³MUÏ½n)¢ \x000bFr\x000e9¡áë\x0000ýÂÀccc+V¬xòäI___WWWkkë®]»P(**Ú\x0014¸zß¾}mmm¥¥¥\x001d\x001d\x001dyyy±X¬¸¸¸³³sbbâó´Ìç»\x001b$È\x0017bPä</p><p>\x001fk}Ð7ï´I¾ìBVñ6O>Ó4éä\x0015 ðÛ\x0001­òí>~èË° x3xñ\x0003ó.ÃKUÌY*? \x0004ÌT×EÓð aXÂ-Íã]\x0010Lð Vay\x0002\x0006ÞsÔ\x0011&%\x0008óx²$5o×Ì04?\x0018\x0012\x0014\x0013\x0012Ó\x0005¢¸X(N[@±4©âÇÂÙÆ1±ÌÕq+\x0016Msví±´»\x0011ÓAYeL hu\x001d«V\x0007;AË\©j_ìQ	Øa\x0019ÈYz*àæ©ÿPÚ DQ¤ø³41Ïvµ\x0004{:2Q·{\x001cÒW,
ítlã:\x001a1°Ên&¸µ[$\x0013:v²²y\x0015M{ôiö;ÌÓ\x0017ÁªÂîib¥</p><p>Ð÷ÔÄÒ©EV¡tý\x0012ùTTaÅS7ÙB«cæ\x001aZÙíòPdå\x0010\x0005Y0sÈ	-´,´\x000c_\x0007±4OÀxË-


»wï\x0006O>]PPpâÄ\x0003\x0007\x000eTVVVWWÃÒMI©¯¯¿ví\x001a¤=22RRRråÊ\x0015Ñ8O94Ï.`\x0007Ì\x000e2çâ±4\x001c¢\x000f._mZIéNÃ-4ù¬3É\x0007\x001aÂâRéÐ,-5>âb\x001ba­Ç\x001bøÇ§khV ¡\x0002\x0014Õ¥+íÂ-X\x000cÕ\x0013¼lHÚiYZ`FPQÉ\x0018¨c»vý\x0018¡#ôuW%bé´\x0005\x0014K\x000b\x0014Í³</p><p>\x0015MÿUI­mÇ­ÇÒ"[óiX%ÜeÕÅ0ÙÜ(Ô¤óÎ}·àî¢ÈÁ<
½?\x001dBDíÚu«6®{E\x0016ö£`Gz\x001cÂN/íÔ-¨£¿\x0012\x001em\x001asZ5N0Q¨/«D&\x0016";lü¯.¤këþ\x00137-KcånI\x000eBV"ùÙYÚ+»§\x001cdHÎ!'´Ð²Ð2|\x001dÒîÖ­[ËÊÊÀæ}ûö}\x0013ay4
ÒÞðÞÓ A¾*îG9J\x0002Lä0\x0008ÍúPYIÇ£/á®Qp\x0011Û'Oûø¸KÓ¥ CJºÅR>\x001eK\x001bV)OC\Archfai\x0005xÌx;²pòcnÙ\x001aFJiY:m\x0001ÅÒÆ<UÒ\x0011¿¥VL\x0007$*6\x001eK\x001b++\x001a\x001dK¦¿$<iiYp,á|8>K>\x0007j@\x000fÛtèn)Ü][)dk&*¾©1/\x0000æ©Ë3Ó\x0005³Íº[àÅRþ3±´L´eKÛO%Û¯Þa·\x0002v\x0010®­¡»©éÇÒ\x0002l¯Pîa¥ÅãXZ\x0017,°ôÂCNh¡e¡}ë{\x0001ëNNN~.\¸ÐÝÝÍü§O&ÂR<\x001eçI\x001f\x001dúfâ¹ÒÁs è ó'|ù|_ºÒ¾»ì¾ò|¬kë18ß}ø³óÎ}MòF&²µo4ßý¼\x0012±¾ïôÑ¹\x0016»%CÅÂÐ$&dtð\x0003<È¹rnx&þ]\x000fÒ!.à	» "j6$
|2$y<\x001bK+±÷<SPæÝ \x0016Îü@4h\x0019?èWTÍÄÒi\x000b(\x0016ØØNµq94úò*¦|Üºy,­¿\x0003æ\x0013'</p><p>QRø\x0013ºÊÒ"öD}*ª®\x0004\x0018²w</p><p>øsTQ¥¡ËÒt('}4ÝXU95¬pe\x0007íÖM	¡	AeÈ\x0019&V©JÛ¶¦²Ó<tfÂI©8ÊÖÎ¢¥V)Ã;O% g­UÏÔ!XZïöâY¥)l"bÍ9Á9å¢O\x001a\x0014VyÒ^¬\x0014{¯g`é\x0005%9ÐBËBËðuøì\x0008Ø\x000c!MLLhU¨l\x001d9È­yWç­[·FGG£iîëëchþçç\x000eòÿ.|÷ù|\x001b¯FI0\x0010\x000f»"öà;î\x000eÍëM\x001d¾éRÿ´&(\x0013§knóBÔÐ(Û.LÍMF9Ð\x0019ÿ8ñúAÙÎ\x0014Ô
Ç¤ùbÉWÉ</p><p>8<2úæí{ËDê[´\x00153ú@ß^\x000exÕ3råîË(·Öqëïn3õÈdâ\x001aºjný]qmS=[t¥ÇªëÜÕ\x000cmkÑ\x000cwR\x001dï&ÈÄ=ÁÙ«ôÕ;¬í»óV.]\x0006øVþ=µ×\x000cÔù\x0012%mD³J½ía¨ûf[po W \x000bDr\x000e9¡ù\x001b!ÐáÞ5kÖ\x001c<x°¼¼¼««+Uóýû÷³»:yòäðð°Ô`òÃ\x000f\x0008¼\x0003K\x0007	"ì+µ¬ùI`Òûkëxzø_þDÌ« ß/\x0000íOeG+kÎñÌu.A\x0016ä\x001crB\x000b-\x000b-ó7B,-â-,,ß¾}\x001bÅ:::zzz`ìË/?}úôÔ©S6mbØØØ800pïÞ½_òüùs_¾|Nÿ£GV¯^ýáÃ¶¶¶\x001b7nà\x001f\x0000ÒAD?\x000e\x000e½+µ¬ùÉ¦ð\ay AæOr\x000e9¡áë` Í\x0013\x000cÎËË;zôh{{û\x001d;.]JçÌ3K,éíí]µjUKKKssó²eËàêüüü¢¢¢ÚÚÚµk×Ò¯©©Y¿~}]]Ý¡CöîÝûøñã\x001b7â6\x001e+Ê¼¾×A\x0004	\x0012$HìHÎ!'´Ð²Ð2# ÜO>Ñ9vìØùóçÁàÑÑÑ²²2ÐºµµõâÅG\x001c\x0019\x0019\x0019Ù¾};jÛ¶mCa||\x001cN\x0006íÊÊÊýû÷\x000f

íÙ³\x0007µ]»v½{÷\x000eWW¯^\x001d\x001e\x001e6P·\x0017:H ?\x000cvÞ¹?8ô¦=öë÷øùNóÌT¿Õ¤¥ã(\x0019\x0006	\x0013É9ä\x0016Z\x0016Z¯X\x0017\x0019\x0018\x0018X¼xqww7ùùù\x0000óÊ+×­[WTTtöìÙåËß¸qùX,ÖÖÖ¶aÃ\x00064Y\x0005W¬XÑÛÛÂÃ\x000f\x0017-ZtýúuL p\x0000;°t AL^üþÃ'þ96ögcsû÷øÉ\x000e©>zÒ{öçKßjõm{£ÀÒAþ×%ç\x0013ZhYh\x0019¾\x000e§åîÝ»µµµ\x000f\x001e<\x0000}_½zuóæM&\x001b\x001a\x001a~M</p><p>«MMM,UTTô÷÷?{ö¬§§\x0007\x0005Ônß¾
c¿~ýº¹¹\x0019x®©©ùøñcKKKcc#þ\x0005Ò¥\x0004É¡ü«ûþOeGËWõ¿ø\x001d-¯¨¢_[ß\x0014%¯²º.±ZQÅP«ÌuéÈuÌ&\x000fæðÒv­\x0012E&t¤iæÆÒÒ!</p><p>4Í(\x0013ÚàÐÛãU\x0016Ui²\x0017Ë\x0007ÖÕ¾¼\x00021#ÅDÞ\x0014Kæ¥;÷³JyBØ~ÓV£xóÎÂâR[\x001d\x0012YÕ2ù£¼»ì\x0018~LG,­\x000c\x0015Ë* \x001c,%ö¢!ûÓ\x0003\x000f\x0012dÞ%ç\x0013ZhYhßôR¸¬ký¯\x0002ð÷+\x0004	\x0012$\x000b\x0002\x0013\x001bÏþ|&N¦\x0003éi&J²\x001fhÊÓ`\x0015}ÈS\x001e¬#C#mL A\x000caB:¬j	\x001dr(\x0011K«/ÖH,'¾B(ÚÜZb¶¯¿­ú;CpoUCVéãyK^EÐ¦\x0014×­\x0014,yÁ³RRéDÈR65±4AIF¡mk\x0005ÅÉAó¶Êê\x0010$È\x000f$9ÐBËBËðuø\x0014:SSSñx§&'''éLN\x000bó<D</p><p>¶d</p><p>êËÃçi¯÷9H ³Äú\x0002EC_u\MWÙci\x0008>mÉXÔci3]F\x0013­%&Â{kë¢$J\x0013ê\x0006Â]\x0016µôDÔ\x001a¢c&"UÃZE±ýZ\x0002Âc·\x001a\x001eK£Ct)Óî¿´,í+º°\x001bÝ+{ \x000b_r\x000e9¡áë Êý<ÿ2ït Af\x0013't*\x001a\x0014ø\x0002B\x001eEª\x000cY2X\x0015»74Áæ(Ét U45tq ³³4ÊÐÁ\x001c?\x001eKó[%7ò\x0015\x001dåcûÊ/,¾di[Õ^¢\x0019XÚªÁmÎÎÒø!º</p><p>bÿD¢YüñVI¥qBt7Ã A~ É9ä\x0016Z\x0016Ú¼,SSSñxü/öË<(Êóã¾\x000bh&mc[Ø©°» Õx ¦Ú©Æ8¦u¢rî½Àâ²xGD\x0008 Þ'r/°rx¢x¢\x0007\x0008.\x0007  Ø\x0015\x0011* ôË>S±dWÍï3ßyçy÷y÷÷ìÌ³óy{e) Ì\x0005\x000c\x0010bÉ´yÝª\x001f6Có`¡ÏÙ#{\x001a¸e\x000fÓ<\1\x0012si6"3m\x000ccS`Åx\x0017\x001e!/wi1ÈÄò9fË²· N¦Ó\x0018ÌôÕ}á)zä\x001a¶..Íví½Ò	ð\x000b]úå¿\x0006jÀÊìã¢Í(í\x0018°,&þ_î\aWn3~} °</p><p>	â-ÂìC¡ æ>g\x0004A¼À\x0012\x0015ÿ\x0014Ï©£\x0019a^
ÅÜ»\x0017Â\x000egdµ\x0019?7^þ\x0012Ä[Ù%B1A^ó´¶¶âz)¯ 4%³¾¾Ý\x0012\x0004ñÎ\x0003ýcúSd½\x000094Y=/!çÊ58*òÔÓ\x0015|w ¼-!ðjs×B\x0010½Ù%B1A^ç´\x001ayøð_Ò¨+îÿ\x000eÐ¦£óÙ³g½t\x0004	 \x0008x1»äP(&Èë\x0016\¡ÐâÔûÎÑ\x0005®ºÊóÚH§	 \x0008 ¦ü2Òã\x0003Â9çê5¤;N±%N1E®I\x001eá§È¥	 \x00080»äP(&H\x000f\x0008\x0019Ú¬8íª«H;Æ:jõ´Úðä¶ÿ6ÑÖÖVs@\x0010\x0004A\x0010¦ÀìC¡ =;\x001dL£RB¡Ð\x0010i§¸\x001bN1%Îñ7DqÅå\x0015wÚÞEid;êñ¾èû \x0008øEavÉ¡PL\x001e\x001c
&UÕ¢Ø"çø1%\x0010iè´¶X¢+ûëº¬+ÚÞ\x0018u|üøq]]]o}ccãëLÇob0\x0018z¥\x0012 \x0008xÃ1»äP(&H\x000f\x0006ä\x0015\x0011GÄ)÷b`Ñpi\x0007£QÏ.ê?^ÝçSQòþô¶ÿÕiØlKKKss3®Ìlñ\x0014mvEÿsGvÛÎO;:YOCCÃ¿©\x0007SW §©©©c<«­ëÊì\x0016<÷-Û´Á\x0013ÔÑq)¸eS:¿ôwTþÓgÏüÒã+ã\x0012÷³b:Ê \x0008 w\x000f³K\x000ebt÷\0÷Ë8-J©é\x0010i\çk%É\x0002\x001d\x0016\x001fÏµ\x0010ÈNt3\x0018\x000c]½·\x0017>zõÎWg½g-»uëvÏV>pø¨ý¬\x0015[wÇ¢\x001d\x0012±w ½:\«ënIlü\x001aÎF\x001e´%R¯/îÖt \x0008x\x001b1»äP(&HwÏ\x0005\º®®N\x001eãXî\x0018[ÌDÚA[,ÒOó?Î
säY¬ø"\x001e_¡^¾\x0011ã[ZZIÜX¿-jï]á{ËË+ÐsêLvî`öùÜÛ£7ï©¨¸ÎãYgXgð¶¨m!qÕÕwÑyçNåÎ°\x0015ëvîH¼ÿ>[¶ceÔ\x0013\x0015£ãSëëëYÉiéþ\x001bÃSöÿ8ìs7µ¸¨¨\x0004V ;GUUÕ	ºCgÎ]ÀÈ»wkB£ü6EÆ&?4²#4aéÚíÁÛ¢ó¯\x0015>}útt
'ðò÷%ç/äÞÜ°][X¨g\x0013Ã¢u|½U~1çò\x0006cåXÕÙÔÔ:s/]\x001d4NùÖÖÖbdÖ©s'NM;x¤íµ¿\x0017\x0008 \x0008â
ÄìC¡ Ý:\x0014\x0010Q\7ÅÿSVë¨ÕÃ¢Û]:¦\x0004
¤ÿÄ}>qK#|±\x0005_rùJ>ÆÃHqõ\x000b\x000e\x001d>E=vº³ö\x001f­\x001eÏrYÉ\x0013ª8k	g-ã\x0004\x001e\x0003Æ( ¨Sç,å	6íC'(óò\x000bþ8Ùã+í¦z\x000eà\x0011´%¢sI\x001e=\x001a7Ý\x001bk\x001aWLµ¨±±Ñ}ñzÌÅ\x0014,bú	EPÜ_ÙI8¾¢¡¡!!é\x0000ÏnÑ?$k ÕÆ)ÚGZK9[5þÂÅKC'y®±°\x0011Y	e#>øÔ/âlä2M`À¦pL\\x0013°\x001bß\x0002\x0003Çºq\x0002wôã:zÁ`<{±r1:±¯N>
Ùwý\x001eK¡\x001cÅØLñHÜw¨}"F</p><p>U_Î]ÖfTî×ÿË"\x0008 7</p><p>³K\x000eb¼ú`fX /vÙ[æ\x001cWâ\x0014[Ò.Ò±¥óµÅª1Ò=}>Ë³\x0011sÃ]\x0011K\x001b\x0011ÏFfÿµ\x0006³GÄìûNî\x000bLò\x0004\x001eÚøT%Áv>~;¡Ð3}xÂ\x0005vh]=ý-íTþ\x001bÂ^½'p_²fÛã\x0015\x0010ã\x0019>0R}Q1VË<}!"5óÉ'Ó3±\x001a4{¹ïöì\x0015Xd[HÜï?õ³ËÎ)(Ô0J\x000e\x0019¾t9ïIJ4`­ÒYX Z\x001a¼~k$ÆÏv]USSSZz\x0013uêÜ<¥ïl×Õãghðj8ùÈD{\x0007â`mPzëîXïy¶j\++«¦Í[\x0001Ø³\x001f¶-dÏµ\x0014È>´W¢ÎËù\x0011iÇkjî¡=|ê·£¤h\Í»f)\x000e\x001c«H;ñàÁáß \x0008 ÌÙ%B1A^ýDÀ\x001b\x001b\x001b5áÇEI\x0015ÎÚëÎ1EíÑ^wÝW½4úä¹ó9\x00166¾\x0002DÔW ¶âß\x00139\x001bÙ]1[P ç¬%ÜpÑ*ÿ]£§yõ\x001dá\x0011¸_±0\x0013zB}1ÀÁÍ'ô\x000cÜ\x001c\x0001#å*¨):a¹<¡</p><p>'N;¸ûC>q+[àãVsb"½nSâ±t¸´Ð\x0003\x000cKj\x0002]<\x0008×êÞ·¼o'­ªª®««\x001b4VÑO(Î½tu½Â/©­­Ý\x0015`5rç²
0sh°Ä+\x0000ïjnn¾}»ì\x000f\x0013<¾ÒkÅ¦¯|¬ìTËÖnM¶\x001a¡i\x0002ñE°&`·ÕH5vä¶x=&\x0006l</p><p>ÇÄïdß£½#4ÞEåg5Â3'÷</p><p>^je+\x0017Lq++¯\x0010Å\x0014*~|ä\x0015~\x0002#\x0005_x\x000e\x0018#C#?¿ÐÊV9a¦w¯ÿk\x0011\x0004A\x0010ÄÙ%B1Aºu(ªïÖ¸$VHö?\x0010§Þ¤ÕSï¡íX_¨ÇÓ\x0015~;9\x0007g#çø</p><p>\x001e_\x0001\x001e5o9\x001eéõÅµ³\x0016/Z½õã	JwX´Nî\x001dØ>ÌZ\x000c×åøn\x0002iIÉvÆ</p><p>¬Sàþë\x0011ãYg\x0004_¨f8úØNõäÙªçIWÞ¼ítGnðÕ\x001e1\x0018\x000cÃ&«°ø7Î+g¹¬þrî28ÿ,x5Ô½ÏpW¸1JºyóÖo\x0017CÅ!ùX\x001cöû­hõõëE\x0016|	'pë?Jj¥Ï¾òâ	TPåIß,Dó§³Û7ÅW~>k¡Æg3oÄµA!Wó®ñldØæ{Æ"\x0007SÞ»wï/sðì\x0016f\x001c;6^ô»â[·Ë]c®ËÓ\x001fi"²ð#\x000c\x0018#GIh\º\x0002>ý³{KK\x000bªý\x0019þ½\x0008 \x0008Âü]r(\x0014\x0013¤»ç"ãdvÈ¾£!º#»uGp
I>z>÷*ú¡Ï=\x000bJZ\x0017\x001cê¿!Ì/8\x0014	Ü\x0012YVVÎ&¦\x001f9!R\x0007º¨üv%|\x001f\x0014ZP¨GÛÒÖ\x001dú\x001föË5¶©óã¨\x001alöa- mÚr¶JãSAêöa]×©ZW6\x0010´\x0002mF[\x0001\x0011ê¶ªåZ\x0012\x0010-Q;FÔÑ""­h£P.#\x0000¹'Ü\x0012\x0010'q\x0012;íÄ¹'¶sµ=>Oüúäcû$±ýæòÿé/ëõ{÷='~s~~-õÃÝiEÅw¨ìMùÖÊ×w¿÷ñÖÞøóÑ²\x0007å4yüÄ
ÛöoØ¶ïý£\x0019n·f®ç\x0015q!»³³Æä®\x0007düê\x000fï¾¼eïÑôÏiÆãñ|øÑ?6oÿ£OO¹ÿðI¯×ÛÐ`Ûþö\x0011\x0012øÌ//ìO;ùå¿.)ZKzÿ»×÷§¾÷±ÕZWYYµýí£/¿ºÎH«Î_Ì¢\x001aÚaó\x001b\x001f\x001cûätn~Ñ¾Ã\x00197s</p><p>xáî=Ç7ýéà´\x000cÍN3gþy~Z\x0006ÎEÇ>=\x001d,++ÿüü
ÓEãô¿I;~\x0006.ëÀ\x000cú¬¦ÿo</p><p>\x0000CFg?û.·nú¬Iz\x000e_kýI\x00000.9\x0008ÄëÁ=U¿Øô×ÇVïúêë«ê}ûõîÇVí¼v='.\x0017\x0016©]¶áÂ)o\x0005ÀúL8¾¡@ß_zú\x0002²?	\x0000f1Ò%\x0007AÉ>¾ý~ÿÈD\x0002@££!É¤2ááa?tì³\x0017¿7'¯gèÊö\x001e:ñâæ=Å%wy7÷«à
ùD<¦Wu¸\x0012\x0001UjÊÄe«¯¿øú\x001a1Co#-Ô\\x0012
øJx(\x0010'</p><p>\x0000\x00141\\x0001\x0000\x00001H\x001c\x0004IBd«\x0001\x0000 6g?\x0000\x0000Ì\x0000¤K\x000e$!rõ\x001eúôªd\x0013uI\x0000Ì@b*´þù5\x0002\x0000\x00003EKW'%òm</p><p>Ï­	\x0000WhõÃk\x0018\x0000\x0000f\x0006ÉriØ5"3²e\x0001\x0000`L\x0014Ö+´xr
©\x0018\x0004\x0000\x0000©,Z²:yT#"Û\x0017\x0000\x0000Æ\x0018Z´\x0010iC\x0016Ï¯\x0001\x0015ý\x0000\x0000 ¤ºt4©¯[È\x001cl_\x0000\x0000\x0018`(Òþ\x0010B¤Õ</p><p>­1g_\x0008/\x0000\x0000HbÑUI©o\È\le\x0000\x0000h"ÒÂ¢Y¤E«ý\x001fa\x0010}\x0000\x0000 ¤¸tT¯^</p><p>£F\x0012\x001eÙÖ\x0000\x0000Ð¢wiH\x000f)°E³Hë-Z<Ëz\x0001\x0000@\x0012Iwi3F-_½9\x0016ÙÖ\x0000\x0000Ð\x0012S¤\x0007\x00154\x0016-ü\x001fa=</p><p>Ý\x0000\x0000 EKVÆ3
çÍ\x00195t\x001aIXd[\x0003\x0000`\x0002\x001afÖô\x0002´PhaÎ]]]</p><p>\x001d</p><p>í\x0000\x0000  ý&'ÆR
F\x0011Ùâ0\x0001ò1K\x00000\x000fQ+´¡EBû|>²hVhögÖæ¶¶6·ÛÝÚÚÚ¢àRp\x0002\x0000$\x0016.^DjC/`Èl}\x000e£w	\x0000æ!þ\x0010¬Ðj\x0016"íñxz{{I¡ÉYÉ\x001d\x000eGsssSSScc£Ýn·Ùl</p><p>õ\x0000ùAC\x0008Ûaá\x0013ËÅËµR
F\x0018Ù\x0006=¦ögö\x0007!\x0012\x0000ÌC?³B³E³B{½^¶èîîîÎÎN²h§ÓÉæLQ«ÕZ[[[SSS]]m±Xªªª\x001e)T\x0002\x0000æ:âËN¯U</p><p>\x0016jÙ,||Yüòt(ÊÛ'4	Ku\x000c^</p><p>Fâ\x001cé"íðV÷cé\x000e\x0001Ì·Tuù9:G\x001eu\x000cWRÚ\x001e¶
V´
üÏÝ_Þê+oñ>pöÝoê¾ÓÐ^TÛ²õ­]\x0008 ÛÞJ¥\x0001çÍ©ÒùÁ+\x001cÅ¨
uz5t\x001aIPäºt \x0010°öv!\x0008B¹ß>Ê¹×\x0016¸çößm\x001d¹Ó2|»eè¶k°Ä9Pìè/jò\x00154zrë»oÔ´]«tþñÍT¹_a\x0000\x00009(.½,¬ÓKÌè´|\x0013Cf{äÞö~¿\x001f. "aÖ¹tP¤}Þ|{_N]W¶Å}µ¢	.
\x0000\x0000\x0002­KGÑi¸4\x0012¿ÈºáG\x0015üpi\x0004Q%ìÒnØ¥]%Î K7ù</p><p>\x001a=y
=·j;®Wµ\)·Ã¥\x0001\x0000@\x0010téÇ\x000eºtDÖ»4t\x001an$Þó@Àï÷×ö\x0004¤\x000b\x000cÌ¨]z\¤[È¥"Ýì+lôæÛûrë»oÖ´_«t^*kK\x0003\x0000 äÒËØ¥U:½*ªNË1dVGÖ
?ª022\x0002F\x0010\x0011C.q\x000e\x0004]ºÉ[`÷äÛzsë»nT»³\x001e:.ÖÃ¥\x0001\x0000@\x0010Ù¥WÂ¥ÄEÖ
O"\x001d\x0008\x0004ü~¿µwTºÀ È\x000cK»\x0006É¥}\x0002{\x001f¹tN]g¶¥õjEóÅûupi\x0000\x0000\x0010(.ý¢ÓËu:½J«Ópi$NuÃ³KÔö\x0004¤\x000b\x000cÌtÈ¥o·\x000cK\x0017;úÙ¥óí}y
=·¬\x001d×«ZþSÞøõ½Z¸4\x0000\x0000\x0008T.½LçÒ+µ.½\x0004.Ä'²nx¸4è£vé;-Ãanò\x0016HÛzsë»oÖ¶óÈuå¿öówkàÒ\x0000\x0000 0tiNÃ¥DÖ
\x000fF\x0010MH¤Ç]Úí¿Û:Â.]â\x001cP»tN]×Í¶o*\x001fØÎß©K\x0003\x0000 èÒßS¹tH§c¹4t\x001aVdÝðÉwé\GàTïJÝ°teB&\x0015j\x00195Núe$!\º¨ÙWØèÉ·õæ5ôKß¨n»öÐqùAÃW·-pi\x0000À\x001ccÁ\x0005¥¥¥úy¤CÑ×*.ýddÖé4\\x001aG\x0012óUMr\úlåà³­+\x000eÔ}7Õ¢Î÷ß©ùíi×¡\x001e\x0012ìImUáÈÌ¾Ïcrs%\x0016\x001egfß£·bLe\@Å"¢\x0000\x001ej</p><p>µæ'©MÆQ+©¡ÔÖImHmâ6ÑçEwDs5â&ªg¨Lô]}w\x0013g\x0014có1pi× Ö¥­Ù\x0016wVEó¥²ús%U±]:+eAuéÖ¤|¹§\x0003]îl¸ÌI\x0013ú»¬éë¦ö\x0007\x0006û¥ÐtUW£Ñ®	^
\x0013.Òïkp¦Ðb1e¦F;ctv\x0000\x0014g^øíïhtÚpROÈ¥</p><p>ë´âÒã:
F\x0012D~!¢h>UæÓ+´>dk;.´4êËüÑ}iã«ÏþäçwÝ£1\x001fZ¶â¬g4Oã­»Þe¡âb^%\x0004\x000c\x0014j\x0004µC¯Ðú<w¼ZlrÛ\x001d{\x000eS¸MÇÎ|M¢Ð[jÊÏÖÿ^¹ï\x001c9AÍ¢1\x001d=yá&ÍÐ+ÏÐ+÷²qÛgÖ¬\x0015NN{ÒB\x001aS
ùt¼-ÍLê\x0007TLÎ­ï¾¥véâG1\:h8Be¦¬qQv»÷ÎuJâ)))\x0013W¯¨\x0013kô3bQx%j21P¬\x0011»ËLÁ*íÙÍ~\sõ&\x0001a4ælR¤Çbºôb¸4$ø\x000b\x0011Ä¹4ù\x0018VL\x0019S¬Û)**RÍJöüúW2³ïSKÓ!1±DK(7\x0012%\x001fÜê1cÑ\x001a£6ó;Z@
"Å%Ñ¥\x001eñ\x001dTw­j¸d\x001aÍ;°ÐRsI§yS
½åßPìÒBÅéD|Ã¡K\x0017;ú\x000b¼\x0005ö¾<[O.¹tmÇuK+¹ôÅÒúÇpi£\x0018HËtKg:.-</p><p>TVl\«®ÑÍP÷C«tuã\x0013ªÐØxà8%=ôÞLMÈ
ï\x00086/Òc.\x001dÒiK¯K#ñJ¢¿\x000eHK­\x001c¬ËEÙ¬MI=CÖD>F\x0011.M¶F\x001eÅ¯ÂÐàÒ1³ãBûÔº¶&­\x001esj\x0010ÿ\x0002¢^'³	sã\x0003S§Ä[î&
HÕû°Óròg¾\x0007h\x0013n7ïFt\x0004û5k7½¶S³<zâìÒ\x0006ælUÙ°\x0011\x001eO¬\x0016ÇÓ\x000c\x001f\x000c\x001eHI	Íè7T\x0017+kµ[i.5Èºôôð>\x0011ë
®IõÞä\x001f¢Áðúuk"~\x001aô6ú	&|&ºÍÃAäß:*á\x000c\x000eSÆLÊ¨.=¡û*màÒêðº \x0013gj35Æ3ÆW­þ4È¼Câø'gæ³\x0002s\x0004¶hó"=\x0006F$%¡_($Â¥§#Ò\x001c2ºH\x0014	³"q"b\x0012ªFoÏXhðÒÆ-kú\x0002\x0019\x0017\x001fKÇÌ/\Óé\x001a5=¦NS\x000bÈo³*\x001cä½\x0014î#M²3NQ¸¿Ü2ú­Ä¿¨õÖRs_ÿ</p><p>ß\x000c|\x000fWÓ+«8\x0017Ó!</p><p>\x0015{ÿ\x001câïÒ\x001ai	{¦:jdMS\x0012*RM\x0019øçØDo4*\x001eßJ\x0010,\x0013þµ@ëºz½0\x000fÿC"¬°O?Aõ\x0007F¼*ýg\x0012kó;üý²ê:ã¸ÿÀú¶úCëÄÆä63Ú$3¥13¾uN\x001fÚ¶q</p><p>»</p><p>² T\x00011\x001d©øê:4h#PR\x0017\x0005\x0004</p><p>²â\x000b«\x0012\x0003¬¨ñ¥U)ÕZG\x001a_JM3é}àpöÞs/+{ñèú|ç;wî=÷9Ï9ç9çÎ|®´*\x0003`c-£ü.ãuÄsäVX°´¡£QF\x001bGWW2Ê\x000b\x0019·V¬8\x0011³4ûIñ¤~\x00086r¥Ûú?\x0011¤É¾à\x001d«!¼o\x0017\x0002¢ÒWoxiÞwÍfF\x0000°</p><p>7\x00000` 4fi\x001b\x0017\x0004\x0006cßµy\x001b.ã\x0000Ø\x0002¦¥\x001dÁ\x001e\x0001q©\x0011û
Å¿\x000f
ÅNéW\x0008aÔ\x000bÁ¹\x001b±ãØS 8Ðo\x0014ÚA×t\x0006\x0010\x0003\x0000bi´ü,9z!mô¥p¥"8Æ</p><p>})~\x00147GÑkDÃ/Çåç/\x0014Ü¨NeÜ×>~J$K
\x0013 )êµFço\x0018È¾\x001aÁü\x0016ÉÕµ­øC0ÞÛ³´Tg\x0005ÈO\x0019C^ª¤Ç di[:"Æü'ÿr«1\x0012 OYú©\x0010ô©°¢Çifi¶\x0016Oöç`%ÇYzþÖ+±#\x0019\x000c ¯¿øÀj\x0014ð\x0012À	LûÃý· %0\x0015=Ò+Ñ\x001b´<\x0014P=U.\x000f
9²k0\x000eÍ@b³äí \x001f"2\x0002ðîåý"Æ¦\x0016yÇ\x0011\x000cS\x000b®\x0001Wz\x000bÌ\x0016ç$z;ÌÒf\x001ekPc0aN\x0004ö(ØlÂ,mH%ÍJÍÒ\x0016ñ"\x001fñÕX¤×l\x0017bÕZ\x0003){E\x0006[æ·H>>\x001fÆÊÒfâµÈ\x001eÙbqgJ¤tü\x0004s/»Ñ¥v\x0019ø9zffkñ$\x0010r¥}Á;N!\x0019X6 \x001d2\x0012;õ\x0007D.éº§}E±Øi&\x0008©K¶æ\x0004'AÙE´(SÐ\x0010l\x0005@c³\x000c³¥è;\x000e0À¡\x0018d¸sô\x000b1'S\x0015D\x001ehj\x0018ÍkT°tdò¨Y:rÍiÉÒò\x0008#·¦¦ùªÿ¿"\x001aM¹E1º²J´\x0004åòYñ)%9GÓÌÒl-Ì\x000fÂNÎ²ôü\x000bV|õz¿¨*¸¿½¯îhèÏ\x0007N'mªæ>vWF
´UÜ\x001bèë HÃ síÅÎ³ô\x0017\x0004#À,Ñîñ\x00188".Ü õÀ\x001c\x0002£	#ÇJ1\x0004Ï#ó°2~lE\x0012\x000fw\x0006<G¿\x0010ëBù\x001b\x0007²­9Ø=²&¦øbª3HïÄLjÍÒòô#+'¥\x0019«B\x0004¡+§&sr41\x0016õè#Ñ£Õð\x001f$ùWi¼Z±laoÌF¼²ïË,ÍÖâÉù\x0014Æ,í\x000bÞQ+åäÚ²@îgê\)®¥]3Ü\x001f¯¬Üw¸÷+I
ö8X6 ¬âÞ\x000b¯9ËÒOúOÐ¤°4Åb=5bfk±®\x0003ï K/Ús]UIêÞ*¬5·ÏJ®ö\x0007º]K?²A²\x0017Ö^ÔNVqï9çÅqõ¹çWý\x0006×'<;¯\x000fíÏfuÛü\x0001ÁÞÚ×5a3K³X,V,bfk±®\x0003ï KÏÉ¿ ÄªsSS:^®3Ô2|ÞìíÍÏ{ªÂ-g¬¨¬<4¤\x001d®âØ%]÷¬*ß\x0010ìæ>45åkÉ¨\x0017\x001fÃV¾â­Hó5\x000cÇ,nÿQNåëY~sßy\x001b.k_ÚÍ,Íb±X±Y­Åº\x000e¼,mdMÇÎºÒº
´L,íÞ\ÿ­ÔðcÈª»/xG;\Å±½57­*_y°Ûö±¹ýÅÅoïlýþ</p><p>ÿ\x0007M]EUÁüÒ²»ö¥MØÌÒ,\x0016\x0015¥ÙZ¬ëÀ;ÅÒõ\x0017\x001fX!ÙÖö½\x0004Ì½®>Ú§»\x000fîoïÒ1ü*´e\x0003ö´ÃU\x001cÛ¥÷\x001eîu¥¤-\x001bqx\x0007g%Wÿç¿¢g$·Ló\x001cÉÞÞÌ,Í,Íb±XBÌÒl-Öuàbé®{VHöLr\x000bù\x0005_´¸¼=à±sßLõ\x0003Æ\iÝV}¥'Ûe\x0003v,zJnq¥pýzr5N\x000eý\x001f}9©1wG²{yhHûê&ffi\x0016ÅEÌÒl-Öuà\x001f\x0001KÃ_JúKós\x000bóª\x00177§nÙÿnõ±wÊÌr×àUB¦ÿ·eéÉ­Ñ³ôþ®KÕí½äö«w'¬ZÏÝÐNwg×¥S:]\x0019gÆìíÁõ9wõíOï¿ßxê«IµÓÝmØSe÷¶~õªnïÁÆÅRUôeßÇínÅÒUí!fi\x0016Å\x001aWÌÒl-ÖuàbiØ</p><p>É\\x0019}3j1Ö²¢&`Ølwå3I#ô\x00056Ãõ9wÕ/××ZuÏm¸e\x0018(cÅÊ-¥{È\x0000t1Êd\x000f¡Ñ6,½»ù#eûlOUÖ\x001f^J­ø ©kßáÞ]\x0007aÊáÖlô­/Ú¹»åxöÒ}­\x00133h<}Ç"M¥Ë\x0003'¥Y,\x0016+\x001a1K³µX×\x0004,
7Óé\x0017Ó[ººz\x000c¶S:Ýë­útÝ3\x000c\x0004\x001fU`³ü¾-¥åx\x0014F7ïî©ÍX\x0000ó+4â\x0015õ\x0002\áQÆæý]('5Ò#Ü~õ.ñH+¦±\x0010+ÞæäÿxO\x001e\x0005}\x0011WÈfHBùÅ+4â\x001eW¢>zT&Ñ\x0005A«Ê_»qûµ,ÿËÞWÒýäWÓ+ÐÙÛ37.íão{+æ¦ùÍ}gæ7²Ë\x0015^¼4\x001aQ1¬\x0005¦%Ë»C\x0005\x0017[\X´S°´¡\x000er\x0010\x0010Þ¸r\x0003®Ó¾\x0000ã©ªúá\x0004Kï¬i)ú°¦¶ã|SÏµU\x0005óÖmj9{\x001d,]´{\x001fXº²=T~èô\x0007:7íÜó\x0005\x000bu}Â,\x0016õ¸Y­Åº\x000e¼,½ ø\x0015¹Ò{¯\x0019}®3®ô+ítú¶Æ\x001ffWÎp\x0007\K¿_3/­Âªo[¿qb`i`\x000f\x0019\x0008\x0004.\x0002\x001d¡}ÍF\x001f]	½@ha¦\x001a7\x0004\x0010ë\x0012³¡\x0011Ô\x000b÷DÑô(\x001e°*X+iPzD~¤]\x001f:$\x0014ñb\x001aè0Êi\x001e\x0005W4"\x0018¦	S\x0012$¤üÁè%'A¤!Iì,]ñUå¿·ÜÿÆªª¬ªzcÔ¸_7ì¯%ïÅVÚü=%
ÇÂÌå9cÉT^j¤</p><p>\x0011z¥ØMê"j.´§âJuK$6\x000572K\x0013´Ó@èBÅ¤³qjô\x0007R	N_[ÛùÉ<øÍªµçªöÐ²ÜÕ`é%ÞL<Öµ½Ws Øßøëô·RéúY,\x0016ëq\x0013³4[u\x001dx\x0007Yº 0h\x0003W\x0006ôr¥u¿åÿùº½\x0005»\x000eö\øûÔ\x000ee/ð¹y Â\x001e\x0019b	éJ\x0014
\x0012\x0003	x\x0003G\x0011\x0002Æ\x0004lã\x0006\x0001hÁ[\x0003æÉ£\x0008B&²%èE_´Õ\x0006ÌÓ\x0010TFÐ+B(¸!\Dpqy\x001dM\x001b\x0008\x0013 \x0018eØ=·ð²ÍÆMÌ¾à\x001d%K\x0013¾Âb#D	E\x0001i½(;±´ØbAÑr\x001dð^¢DTOúß1<Ý #m( \x0003z¡%?|ldî¸þ\x0019Xú\x0017¿Z´qÇ®
ÅÊ§ÈÌÒ9ë63K³X,\x0010³4[u\x001dx\x0007Yºþâ	@kñ±7ókInV¾\x0005?,KS\x0000\x0019\x0000È</p><p>XEä	^"6Æ£àU\x0010¥U0
G½\x0010Iñ\x0014\x000cÒ³gi1</p><p><®"§HB\x0003Q*	®bþr\x00121´<±ØÛpËYs^9\x00103fNõ§ùUºá\x0006oqµbi¹"\x001e7dAæÂøÃ¢ÃWbw¨JMÛv3K§ee\x0007ûï·ÿgim@°táö÷e\x001ed±X,VXÌÒl-\x0003½57\x001dD²9ù\x0017£Od \x0010@®DG\x0002\x0011\x000c:"Ð"\x0018\x0013aò+Ê#Gð3Þ\x0012k²À`0\x0010ü\x001b¼\x0012i)^p»áQB\x0007\x0013\x0007ÊI\x0010C&¤Ä ô\x0018Ò*#,ÝÖÿ9è×ÁÃ1°\x001a\x0010\x001a\x000bÁü	ªE
Q.4Ò2©8¢&ò\x0016Ó½\x0000fQ\x0007T\x001eÑ\x0017\x0001â¡Ñ.Ê¾¢þ"3Í</p><p>û+Xº`Û\x001f¥÷8W°9såÊ£=`éÕ¶­Ûö^Þúßïj\x000cÔ¶­+*ef±X,!fi¶\x0016Ç\x0007K;Ke\x0005AGXQ\x0018\x0004<&{Ì
®Ãl\x000bvI5Jíà\x001f\x0010Á,ÿìè²`éÎ\x001bÿ#>>0\x0014ì¿ôêÝ#û\x0014,Ývévà5½ÞØsmß©Kþà\x0019fi\x0016Å\x0012bfkq|°´TX6à8#K\x001f
:2UPå£íü­W\x001cÙ¸®{\x0013\x0000ôîãÚÏ,Íb±X±Y­ÅqÃÒð¢=×cä±¹Ûú\x001d\x000f;\x001a£à({\x001bÛpKûBb7³4ÅbÅ"fi¶\x0016Ç\x0013KÃe\x0003\x000cÒOËCC±à´·æ¦ö%8bfi\x0016ÅEÌÒl-3\x000b\x0002\x0013à1@8´F£øó·^yØ]óöËî7ë\x000cãþ\x000bú\x0007ôºÍU{^¬rÓÞT"UÊEÕ*½ëFÊE\x0004éEZ\x0011J1Ø±\x0007\x001d\x001cóe\x001b\x000c\x0006Si\x001dê$R\x0010jT\x000f©2ª\x0002-\x00015A\x0011¦""xwíµÔgçÝ9sæÌõØ3»g0Ï£Ü3gÞó1ç\x0004õ··pÝÎ7\x0017tia,¡K\x0013'l>\x0006gÿ^K/fßíýWv\x001f{ÿÒõ7\x001f¨ÇO®ÀÐÙiûÂ¢úºzÿ\x000bW»o\x0019ÁE@S^Ü¾8{y\x0003«LÍ_Ô\x000fJ]Ó×>\x0003\x000e?.Í0\x000c%tiâMéÒÂäµ'Ð­6nö¼wgûG_å²Ö;S³º9ï\x001c<på^Õ¡KC\x0017/}þMw\x000c0_>½·KÁÕ$Ý\x001a.ôçÇ¿Äånx	Ý¥qG¸;iÏ~àöÛéÒ\x000cÃ0YB&NØÄ.­wm=÷\x0010gïKcôòc8Ûzç\x0019\x001cØ54</p><p> ©\x001f^ûL\x000cÑýn×Û(ðÆ&\x0016\x0002\x0002¼E?Þ¢2®s2³ &NU\x001e/¶:\x0016E\x0003@\x0002Å¨Õ\x000cªRVÄêÆÅçüíe\Ü\x0017äY\x001a\x001bSh\x001cü²ó¿è[\x0013Ö¯@\x000e
muÅê<;úÉtia,¡K\x0013'<\x000b.\x0017¯½¾mÁ×ZhÕû®á¯´Å»ð</p><p>\x0005âÒR\x0000[\x0013§©QºÙ¹p\x00152,S£\x000coüö-U\x001eyD\x0003Åøä\x0011È\x000cbòW^©½\x0019+>kàÛ\x0001~nÈÉà$å\x0012å:vyÃTWóÄ_-\x001dÝ']a\x0018&KèÒÄ	téô@¥\x0001¹»´Ø4\x000cÖ'§a¸\x0017L¥,øö+jguimÁ×uõ(.-ÅbbÝx+z\x000f\x0015¯ø\x000cCÓ
Y?@4ð</p><p>\x0005rhèQW&"Þbà\x001dÝ$]a\x0018&KèÒÄ	téôüjË¯¡¦g.\\x0015Å\x0012µVb\x0006\x001fÇ7\x001fè.

\x0001\x0018\x001aÆÎ½öú65-^)ë6Ê°PùWUoÈ;DÅ	
\x0016ÙC\x00035¢DÐWÄü(p~Ý\x0007ç£\x000cYîH\x001eq8I±eyÄ+üÅÏàw\x0010.ZÝ;\x001a3jº4Ã0LÐ¥\x0013èÒéSÁ¸D¨DÏ\x0000\x0014\x000bö\x0005_ECl\x0019¯f>¹\x0002\x0017\x0012E±\x000cD\x0003ôJ\x0002æ¦:E\x000bJ\x0013\x0015¥\x0001\x0016|IVsâÌ ³FÊ[,$õÏ\x001a8\x001f919\x0005ÿ·þë\x0006
\:s\x001eÞÊ+9O¹A\x000cï\x0004véJ¹§ä-FËÜÿ¿,ï»NÌ¢W²V&õÇæ¯Ó-2k¬Ë0Lþ¡K\x0013'Ð¥Ó#vê\x0004èÃÕIwè´K\x001bòüt¨tzÎ:Î*Í0L÷C&N K§çâÍ\x0007®¾ôù7\x000eW'Ý¡ã.½èB}~JTºk.½è©Ò\x000có.M@&¤ tÜ¥uV*Ýìk%pk]_U;¬3\x0014\x001c\x0015Ú¯'ÖÖMg.äOQiõVÝnÛ¶\x0019\x0016í<¯ÍÛ¶gbýÒæÿË%\x001a¢wÆNaüB&N K\x0013R\x0010:ïÒMITz\x0017xf`xM7\x000cÝÏtiåÞ±Tj«\x0004\x0013VÊBÆ'
7¡ÕôûjÕ·Ý¶9k\[Ãá¾5'¾M&úyªíÛ\x0014gº4Ãt tiâ\x0004º4!\x0005¡\x000b.\x001dÈtàÔMW\x000c½Ó¢¾ªmÎpX+QOWÞì
cúgt{f_Òf·mn5¦­ê\x0017EÒÛg\x0012ÿÒÄ2z3Ãt#tiâ\x0004º4!\x0005¡\x001b.-\x001eY	dr\x001dÞØ\x001a¬¹°êÐP¥\x0015yY³Í¤sris«séØÒ¥\x0019ÆièÒÄ	tiB</p><p>BW\º%û\x0005â\x0018±â ³ù>â\x0011\x000f}¤ybsPð¦YT.Æf±´1±À£¨Æ·m*k°Õ¸ÊÃýÓH|»öX¾4KÓ¯\x0019¦\x0003¡K\x0013'Ð¥	)\x0008ÝqiSWÅ­{z"JÙÔE?årËùTéÀÁø¦Rª\x0019üN½0\¥Ù\x001fNÖ\x00133Ys%«Z·]IØjÊ¶\x0006{·)ÏÄò¥tiq\x0019º4q\x0002]Ð%f\x0018Ù¤¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008tia,¡K\x0013'Ð¥	)\x0008Î]úìÌñ3§¦NOOÌ8zrêÈôä¡©ñÉ#cÇ\x000e\x001f<=}ìîÝ;9®Å0\x000c{èÒÄ	tiB</p><p>sH¯\x0006iF?>ñÏ\x001b×§§P§\x0019)rèÒÄ	tiB</p><p>s>==Ë+ËH}¹Ô|àÒÿýÏý[ÿøÛñcr\a\x0018&ßÐ¥\x0013èÒ\x0014\x0004ç.=sâ(þUÎÏÍêÔê5¸ôðÐÛ`td_Ë1\x000cÃä\x001bº4q\x0002]àÜ¥ON\x001dÁ¿Êúr½I½^kQCªµÚÊJcäÀPË\x0015(rOOOÉ[\x000c\x001b\x001b£\uùLi©w.z%sp8]B¥¾JXl]IëM_\x0019ïLØ\x0012Ã8</p><p>]8.MHApîÒÓ\x001a««ós³VàÒÃÃ^Ë\x0015(i\ÚjÀ­(ÕÞÛëmÎp°¼ó\x0015O6&]²ËðµV\x0018~Þ\x0019]KáTöá-¥=´õÔ0LºÐ¥\x0013èÒ\x0014\x0004ç.=51Þh¬ÖëõZH­Z\x0013ªMÞ7ãr\x0005J\x001bØ¯ùªìE]Ô.¶J[§¯¦­ýXf</p><p>·«\x001bpØÖ>ÇTdù¸t¯YÙ¦3ù\x0004Û\x001cÚºj\x0018&eèÒÄ	tiB</p><p>s<2\x0006µ\x0002Þ?40T9oE¢e¦_És`ZúYi8&{Ñå¬óè=Í¢Ø\x0010ë*árzí!Iû\x0016ã2\x001c&òi¦´Ú:Õ\x0019ÙL3AÕÈ\\x0011Ém><¯\x001c¼N_Ü\x0019\x001f«÷Ö:\x0012mÝt\x0007Ë0ë\x0008]8.MHApîÒÇ\x000e\x001fK×êµ&µZUQ­.U«pé!¯ß:ÐfRÑ\x0017mX\x0017Á6«Ä³ÍÓÒµVYâ\x000e\x0013ö\x0019¯·I­è\x0007Hµ?AôDÒ§Æ:5ËTc¡GõVÃ\x000fN2dQáEí¸ÒW&uZ¶d«QkîZ\x0007Ë0ë\x0008]8.MHApîÒGÇßm4\x001aós³VVV÷\x000eöY\x0007*¡</p><p>Quµ:>*\x001dIèÀ±qqM²}`Cæ¤UFübÒ\x001a\x0015dKGÖ</p><p>e1Kk~\x0019Sq³+Üj)r>¦!\x0007*ühM¶UÚ;\x0013¶¤bz²íèèÒL¡K\x0013'Ð¥	)\x0008Î]úÐ{#+FµV\x000b¨.U\x0003W\x0007\x0006v'\x000eVB[òÆÊ==Q5}¤L­\x0012Ú[Y¦5\ÚXî\x0003ë<ñÙµ!æ1×¯¥|Q\x0019ö6ìÒÉ\x000fIß\x0016]ÓrhÚo\x001b\x0015Ì¶rÌ>|­-Ñ¥..M@&¤ 8wéñ±wàÒós³V.ÝßÛv\x00021³7ß\x000c´*"X¢z¥Ð1\x0003³</p><p>4ªâY´Z3­t\x0005"h§Ü¥téh½Õµ\x0018ïÃÇØÀµ]ZÿÔð;Âó±~ß©ÿÒ\x0008oÀXkc¶NÛô·üÀP¿§¢ÿ\x0015Ð¥\B&N K\x0013R\x0010»ôØ»\x0007VV\x001aKÕªÆÒ¥\x0016péþ¾]Ö¢~~|C</p><p>}s6Õ9"A_ì¥BftËYçº´eHì\x0003t¶Õ\x0007}ví+a8GtD</p><p>¶îXëÑ*µ^}JíØì¿\x001c\x000cëOS\x0019ï´mÉ~ðå´tÇø|âÁ2Ì:B&N K\x0013R\x0010»ôÁÑýpéù¹Y+pé¾=;s\a\x0018&ßÐ¥\x00136½K¿½üÖÇÿÛröþ\x000fGþ-üâÄ[Ï=¼öÄ¹;6^~kÂe©Ã#®\x0012\x0017ê|o\x001dÂ¹Kì0·a÷îßç¸\x001cÃ0L¾¡K\x0013'lbÞþÑW?Ø{ç[¿¹Ä··ßª¥w³íCã/½¼\x0005\x001c>wQz*Wnà\x0011åqëNOµÁK/G\x0019\x000eðI¤Ý7>£¯¢úOþIzö¼wJzN]ø«,ÔêÒøå«ÛÐÞö½ÆÕlD
\x0011T1\x0016Ò¿KM+{Ö\x000b°ÊÇ×ïéÈNr\x0004×KÁÕ´¹8\ëÀ\x001f¥\x0013ß®>ÿ7v ¯P'ö»_ë_$ßn\VwpîÒ#\x0007½á}û\x0006¼þ½}\x0003\x0003»\x0007ú{ûûvõíÙ	îíÝãr\x000cÃ0ù.M°)]zôòãçvßn#cQo=÷ðÓ{kl\x0003ºõç¾\x0007\x0007X~ÿù\x0017\x0016\x0002yF§òI\x0008è®WñG\x0001\x0004SaZ4tåVeh@óPóãþ\x000c\x0005².6W¢¸R#ëÂóñê\x001fýDyþÿÙ/ûß&¯+ó\x000f¸etC\x001a?Lª6(t\x0015¦Fc\x0013c¬¢ÒQf\x000bÕªÍÈ$@A0\x0004â$%$)¥0\x0001!m^Ö5Qì@^\x0008yñh)t´\x0004\x0018I KÉZXÄØ2iH(Ò¤}ýøúúy³ãÇÍCÌ9úêÑ}îsî¹çkÉK9c	f0À'\x0011\x0006øD\x0003Z\x0005Q&",%Ó§\"\x0003æÓ\Ù`Q9¹Eá\x0008Ö5ÜñÔ \x001c1\x000e:È(mùªé¼è°P\x000eBò¨\x00083è3jAiT\x001d\x0015\x000eü\x001659²¥ÙØØØ¦´1K³lQò±tjíHì<&´¨ì¦9NTkÓÝÅGaL P\x0019­£²´§¼\x0002Â\x0012Â9\x0000\x001e^U8ùÕiëÄ<b\x0002êD|¬Õ²4hpñÒ\x0015XRÙ\x001cC\x0001\x0017	\x001d\x0015B¾H\x001c.Ò@ò`H8ÀüA\x0018ë²4RE\x0004\x000f9H¢P³að\x0001 Ã=(øt
¡[	]h\x001eù/X´X´K´\x0002\x000e®×òÅaM¥ÙØØØ¬\x0018³4Ë\x0016%\x0013K\x0003\x001cø"\x000e\x001e#Íò\x000cèLâ<6÷\x0002&\x0001f4\x00060ñÄ¸/\x0006Æ+$à\x0019cÀ\x001b¢©\x0014¯´\x000b<caé>á\x0006<Æ\x0013> q<\x0005KãO1Hse\x0003éS,,d°)V¡pr ZÄµÂÐv4?îûå\x001fF¢nA¥¡	Ô+¥ÅUHÅÒè¤|X fi6666+Æ,Í²EÉÄÒ©µ#qó\x0018iNá0\78à\x0016ô\x0008Ð\x0002R\x0002Ï /<1&Ö->r\x000ctM\x0000\x00067Õ+Æ$¼"Úþº\x0013\x0003¦%\x0014ïSp0\x0015»,^º\x0002\x0003 1\x001c\x0010\x0001>XyÃçV­ñW`íÚt7&áC\x0011È³²9\x0001¢ér2f\x0010\x0004Oº\x001a\x0002ikâLªQ´"ÄÒáZ¬¨mxÌ</p><p>HÇÓT\x001dÝ, åfQbÑ11©bi:;\x0008efccc{øYe¥³ïZä1Ò¢²F[\x0010RBL¼¦¹²	ñÄ8Ã®Rr <£±ö¸\x0014tGcÁoúTób_@¬jFN^\x0005~"\x001arà)¨\x0018\x0003`3\x0006EëÈG =<å\x0019¼</p><p>à¤íTµÄ-Ü\Ðð\x001cÜÀ¨ù^¢^\x0008\x0003ê\x0018ê\x0012\x001d£\x0016	g!jò$YÍ1K³lQr°tÛðXBxäé¸79ìÄJÔ
\x0008å\x0019\x0002Û^\x00151K³±±±Y1fi-J\x000eN­\x001dQÕ|ï`am\x0000òÖ\x0004[+º¶\x001cêÌ=\x001c\x0014\x0006îßÚ]ÝyGöÕ¤¤²)!4\x0019­Nà%ÈYÇö¢¬YÍ1K³lQ\x0012°tÛð\x0016«\x0016\x0014^[Ûøb~Óíþç=þ§2üßÝÐ$ôäú¦ù\x001b\x001b\x001cÿØuQÊ<\x001d÷l'«¤\x0017Ð7 MÒ fi6666+Æ,Í²EIÀÒà^-S=[2VÜ²ÆÛZ\x0018ÔÚâW^\x000f\x000b2÷·WüÄ¥\x0017Ý´¬^³½7\x0012ÎÒ{\x0002£¶×\x0015·¥ÙØØØ¬\x0018³4Ë\x0016%\x0001K/,½©eªy»\x0006¢r§²ÛsÝèëÛV\x0013c¨aðQçë>\x001a)ª
<u\x0001W7Û]o´®ß×&þF+f0?Ã}E»veÅ-ÛK[ÌÒllllVYe¥uy\x000c,íØØ÷ôæ\x0014wã¢Í?Ì\x000e</p><p>cÒ³nß²­¾¾Ï¾üÉ\x0016ßô
\x001fêF¨¾tßv¸Jby:î\x0019±ôÊÂ\x001e#ûê¼Lß3|\x000b66þ`OhþFß÷³»¯j×Îò\x000cÙ^ZÜbfccc³bÌÒ,[4ÕYúÌíÿéòØSù\x00033]í-\x0017Ûæ[¹Ãÿ¼ÇÿÂÎ&@5ØláæqÍÍôãÓË{{t#\x0000öl«$Vvó]#¶(ÛK[\x0004K_.MRzÙ¦ÝýÎi0ìo\x00064,¥­\x0017ík0fi-ê,]}é¾.PÍÙÙ?ÓÕöÞ©¾_\x00155¿Zrâ×%'~³÷$¸úg[}ËBúi®omqKª\x0001K\x0003öl«$³þ\x0011\x000c§\x001fþø¥ÝMMôZãò<?ìçÛç\x0001îDO¤w9Ü\x000e÷Ñr\¯l¯.>=\x0012,\x001d%E$íôOÚv\x0013</p><p>8\x0019¼M7	ÙâÝ2"ÒT¹'\x0004ïCâøU¿PA\x0011µÄø{I¨ñ½Ë¢1K³lQ²²ôÜü®Ê\x000bs2üßÛà­hnOh^¦\x000fþÎ·¦¤YzòZ;b\x0004Ã;ÿøuå­¬¸û¬ñ6ÿ"¿iõ®¦U;^ØÙ×o¦wÂÇsÝhyÛðíÕÅ'fi\x0003K KÇ\x0012'iY:®½tåI\x0005C'\x001b9MÌ :ôøt©§9Nt\x0018²ÅZO¢Òþ5([\x001cÆ,Í²ES¥\x0001Nº@õôîªìx[\x001eßðáêâXYzï¡ª·jê¡¼=íþf\x000bn\x0005>¿ûNÓé8\x0016öþõç¾ü/Ò®9Ñ{fø_G\x001bÛ1±ùª¯¯L´×ühâîv8;\x001a\x0014µd¹öØ­\x0008GCÛU·ô\x001e¸]s¢§õâçUÇ»ÌYúXÏ§\x000f\x0017K+ô\x0001K)-
q¸´êµ!&ß\x0015T?ª\x0002j¯Ü&\x001cG«¶W>ùE9ÕÛ©³
~r:SÔ@©Ó\x0010íZunÓ\x0004ØIÛê¦d\x0014-*,'¥e\x0016}\x0018L¿:
¡ú\x0005'Ë"Ýüv°´µm\x001fycfÙ¢©ÎÒ.P9Ü\x0003s3ý»ªz\x001d9×ôå\x001eÄóô®^×géêK÷U\x001bålÛA\x0003@©\x0018\x001f?×/\x0013óÇÏ
\x0010µè\x0013f0W\x0001N2AÄ.\x0008Hh\x0015$==x»üè»ò^\x0002üðª"4Ú\x0017\x001f\x0004\x0019b\x0006óPé¡*\x001e%@¡0¹9Gö\x0011{É\x0003</p><p>HõÊ)Ë¥W\x0016öüxÏ}u^¦oáfß3|Ogù\x001c\x001bûp¦Aå\(K£¢½J½ò!Ê\x001d£\x0012Ä+\x0015ò~÷qoRõV©ÊÔ6Dî§ê|U¿\x0001¸yË\x000fÂ\x0001Ïî´^¼±¿ºþìßÿÓuí\x001f`éÎþ[
¾Þ¡¯¥ë:Ï5üé\x0012Xºá+î¼Ý5íg\x001f\x001a\x000eÒ ÄÁ\x0013biiÆï\x001c'GClÖK«&\x0012Ý%Á|u¨;\x001c/\x000cÌêü)[ÅI_´¯ÕoH<4R</p><p>çk\x001c-v q©\x0015az\x0019ép@yÞmE÷\x0011º/g\x0013åî ½:\x0019%¬Ai+,\x001d½FM\x001a\x0011«¾jnDÚdÙb6fi-J\x0002í½¡ËT3Ò»=Ý@/\x0003¨¯Ïp\x0019²tÛð¥£jO\x0006²@h\x0000Ô¼=à.\x0002l¼*nÀÑ~zÅ\x0000\x000e4%´P\x000cÒÒÖb@¢-( EÀ$\x0018\x0018¯Z¦xÇ°;\x0006p\x0016ÄHñ\x0011AÐ#±4Å\x0014,1¥}¤þdÆ&7UDÉ`\x00060©a?-§P\x0002GEd¬\x001báCq¢</p><p>W\x0015#\x0018®ûh¤¨6ðXÖ´âõûÚ W^oqd}jÐ¤%\x0007¾ÐîB~»ÎUÑÐ* Vô:FÕaLUs¤^W|Â\x0000¨\x0011ò\x000fÀ\x0018qTþb\x0017Ù_þ
À§@ai4yõûÄÒþ³WÞ¬:³Þwð]ÿ\x001d\x0005`éíEeûªê·yKJ¾\x0007ÎVX:õÕuvÿw)\x0016ñï¯ÍÆ,-LQH\x0013;Kk'MH\x0018\x0018Sdm¶ºéé6Dg­Ñ¦!VDÛÏfÑÌÍü^@°'ÂEmþ¨ÔDé\x0002\x0013\x0006sÝÛÁ=H3Ô»ÎDÜb4W'£µ§,ÝX$äÆÒVj3×¹:îË\x00161K³lQ\x0012°´³þ.VÍtuä\x001eî4G¯éëÏ¼XÔ¥\x0007k7"¸\x00081\x0003¦"ºÆ'ÌÐ$¨I0ñ\x0012H0UL</p><p> \x0012äIüì-?(³:@\x000bóxªXZx\x000fáI,]ßsAÎVÅÒôªeib?ìH»à°oÕ4\x0008¶§Ìáy¯B}Z¦Wð*Ü\x0004¯FÕ··\x000fÅÇ\x0013§ãî^ÁHr\x0016×\x0013U	ÔL:G<é¸Ñdªú\x000eÈw\x0016:q8ãO¢í4ÀNJu4òF,ý¶¿³wè+°t×µºÎóyÞ¢\x0003GOõßÊ/;è;mÙò\x0015vÿw)f¥uÈP1Dh\x000f\x0015Kø6Ä Rm\x0010Z-Å¿¢E37S¶øÔ°:\x001dÖ)PbþtØÈ!Ê-Æø\x0007&åb4\x0013âtJç¦Ë´qÔh¹úæ8ªúõ°MÈ¥Y¶(	Xºað.V}ËÕq¨éüôô^]}Cy>¹þxZY@»\x0016|®ËÒ\x0002Ì\x0008Æ\x0014\x000e\x0002*8-*K\x000b¸\x0012ð¬eé\x0002\x0005Ø\x0010x¬@aW9\x0007ÁÒ²'ð\x0015B\x000e\x0002\x0011cgiÔ-\x0010\x0007n\x0018#,âÀAÅÒ´\x0011>ÁGÅÒ\x0002û±â¨r6RjíHÂYºmxL»\x0011Ò¦VªXZ[-KÓR[¨|ùv\x0003a^Pºh;­Â^\x0004Ø2~SÛ\x0005Ã\x001b±ô\x00077ÿÝÙ«ÒwÊ\x0005Îrç¾ÓÜýöË÷5ªì\x000eãù7úºô\x000fØ7¾ó]\x000bû®oXhqÄ\x0016wëº\x0016ã*Ý¤´1Ó´\x0010Ó\x0006\x0012GJKf ©q#²Ù	m$ëîD¨¸4¶-F±fÝÒ@µí>sÌwÎÜ{gæ&wôÜ<\x000f\x000fóã{¾ç×À|Î/~{),\x001d\x0010\x0018aÂA\x00030jý­P§Ñ\x0017R\x001d)bé¨còd,\x001däikOhÑÕ¶·è´Üi8Imç.Ö9\x0003\x001bûn-vEÑîX\x001aß\x0001K[\x0017ÎÒÛÍãF¶cé\x0016­]dé\x000eï/çåØrmR\x0012¥e/î\x0003÷¹\x0017CV¯ßüúÛ¿ÿÖXù\x001b?¹\x001cëý?¾üí]ùòëó	Ì\x0018Ò\x0018\x0018t®tåÄÈip\x0017)ëBykØLîE;\x0003±À±ø£\x0006\x0007÷\x0007ÀV2veBBÌ±ã§®R¥ÉÞÄ\x0017 Ç¬Z$\x001aGÆ'Ñ)\x0008lDÊ\x0010K£Ìe\x0013\x0011¡øÞ\x0007X\x001b</p><p>Ü\x0011\x00020Ó\x0019ZsÁ.</p><p>Úö9$É­µz\x0004íØ¯»\x001f;\x0011÷È4âeu¬~\x000e.åÚFì|°wÜ8Ï'\x001fl\x001féN£ÀÛ\¼\x000bÄ×ÏªdSØoÀÞ>öÌ	±tùæÝ7¾?ô«Ùkdéßymúò{?üé#?x\x000b,}tèíÂüûû¾yÐ÷W]\x0001
Ôè.ßàzã@.×\x000euH\x0012[³Q.,7\x0013^ä	YÚMÄ\x0019:\x0011Zhµ­È5ö@Âc#á\x000eN5#[­ÃãZeKÈÒñï\x0002^¥ëÈÒîJr\x0003 £¯m½\x0012¾bÚ³týY\x0016ÞiëmµIºÇð\x0011u|5\x0018]¬XbiÙû¥Ï¯<í"\x001d½ô8ùÔ@ ù5B\x0014\x000coåÐ\x0002²²!Fà.\x000cg\x0006\x0012©ÛÛÆ¡Hd\x0008MÊF7³£¨iËcZ\x0006ã.NÁ\x0018w×ÑE2&!HÓû.<ìâÅÅ¾Ü5»[=1÷lí¾B××ÑÑë¼{P(0à£Çÿ?üì\x000f7þ{óÑ>øûók·ï\x0016?ªÜý\x000c,ýîÇ\x000fsméêÖ\x000bW®¥Ï¯¥\x000f|÷{¾ÿ»¢ê@rR\x00125c\w´Õ»`ÊÐEÃ¸Lãõ\x0011ÄFB·½Õë(É;(á+¦Q}yEø4ô^{ÞÄ³tÒ=6-#òêiôFÎ¦Õ´R\x0012¥e/î\x000fî"}éÄÝë\x000fv²$°Óðø$<65|\x0014Xº+ÛïQ~qà]¹¸\ñ÷í¤t¥\x001f>»ñàß\\x0002þÃß6¯¯ýsñ/¿ûçG`é¹êÚïn|,îOÉOGZ\x0011Îªzf¡ÙXZöâ¾ai\x0000ð+ùOÓtéÎ3ïLµ«|~åizÞ{æ÷¤·XZ</p><p>Pj` |:Ò.¨v²¹Yß«è Ütö\x0017e¥e/î\x001bßùä9`8
.nz\x0007ª]h\x001c{[Ã\x001b</p><p>/)ï»Hï~aiI$?\x0012KË^ÜO,
©@V;à1@øù§Þij×\x001a8½³wÐÞ3÷ú\x0003¤«biI¤t\x0012KË^Üg,]
p:W|´]\x001e+Ýyæ\x001d¥v¹q\x0005Û}\x0007\x001d½ôØû²»h±´$IR\x001a¥e/î?¦ßùäù«çîw±¯üuòÆ¿¶ùâÒíB1ÍÚ\x001d?rw«\x001bcSÓà«\x001fýüÛ\x001acý/âÀ»åÑÅM\JÇÛwá!®8aÎÊêF]¿i?XZ$)ÄÒ²\x0017÷+KÓ×\x001f|\x00016\x0003Tï=sÏ0ìü§¨¾uõ\x001f¥;Ï¶
H6Q(\x0015æ*dé\x0000ªK¤#tÁçJWX]Z®\x000båEw8\x001a\x0019@fÕb´%$q¸ñ!¶ÌmR¡\x00171\x0018Å0V10\x0014ã\x000eD\x001e[ÞüÊ\x001a'bo(²ëÆÕ\x001c½ô\x0018×är5ª¸J\(®u[Ù°ñI,>tæ\?Û±AÆ¸×Ø)7Ë.Þ{\x001aHïÌÂ2</p><p>vVî­¡.|\x0011)86ÖbiI¤4\x0012KË^Üß,ÝE\x0003ÀÀÀª¡áQ°4\x0008\x0005\x0003c´\x000cO¢zøÈ¨²a\x0001 ®³Å2X\x000c
a\x001c\x000eÖµx\x0004£/Ñ\x001d->ÄÒL\x000c\x0008F¯;ÊR1ÿðås\x0000\x0018è¢£åAÕ²±Ê5Û¦¢«Í²¹\x000bÜ ]\x0001\x000fÇÞD07å²4\x000f\x001c_qû\x001bà¨á\x0007\x0007÷ó4,\x000f\x0018\x0001x7~\x0018\x0018>,$Iza\x0012KË^,Nhb¤[\x0008´\x0004:%¡½ZgN\x0012Ôò¢],²^{ã\x0018Ã¬â2</p><p>\x0016r\x0000r[\x0001Hò.K\x0007Øv</p><p>]ù©i®;F;«\'ç±\x0006£G\x00140\x0010I\x0008{Ù,¸,\x001dZ-ZPö~AIîÎ½j3K[Õ=4·GK·o</p><p>æAËÈødp­§,,4c+¥%IÒH,-{±X:9\x0011f\x0016ADø²Êo\x0008£@S4--\x0003Hµ\x001a +bð\x0005l³</p><p>"Q \x0006[|¨ÈM<sY\x001a\x0001\CTdl®\x0016\x0019ÇDh6Vë,ÍáÆöÕ\x0008Ksï±SdÙ\x0006½î\x0015ØÝ\x0001³4«8\x0007Ü¬U]&G;zíúv\x0013KÏæ\x0006öäou;ë­ü¤i_Ì\x0002$Iê\x001d¥e/\x0016K'7¨2?5
\x0006& PÀé"\x0013 
'V\x0019a,\x001aIÑA< ìÊ!.\x0001ÚÌ<Q(¡ËÒ</p><p> HØæ("mù\x0011\x0000ÌêÈød(\x0006½[\x0000a"ÏÓÜ\x0002sï±«Í²íÅ\x0005»°Ëâ~Yå\x0001º÷Umfiþ\x00060XF;Ï\x0013ei>¯ì©âºÇYz³F³ÝÙQq·XZL.I½*±´ìÅbiYÎ{¥77oÝêk\x0016fKR¦%½X,-Ë\x0019qO³4(sK¹ÙHÏül~OÐi$\x001a¯årúÚW\x0007Ü.ÃW\x000bhàeÎ7@·Þ\x0018\x000eNÄÂbiIêU¥e/\x0016KËrFÜÓ,]W6\x0003jf[
q£½ÊÖç&
hJN\\x000eð¹AÝ©iH\x001b\x0016còfàoÔ8eø9 Ð$ß\x0012KË^,å¸·YºA­hy«BðÄÇòóf3KGP\x0015\x0000Ü;¨Ô©¸	t\x0013¬>ÂäÑ-Äâr½Q,-I¾%½X,-Ë\x0019q\x000f³t
@
EÛ°t=.&¾»,\x0008 ;äÙl\x000füm\x000f$ùXZöb±´,gÄ=ÌÒÆ5²t½É(7&~G,\x001d$7(w·\x0005ÝÆæØìÈäqÀßîù I\x001f¥e/\x0016KËrFÜÃ,Möära°¬ñ'Zî-úoÂÜ\x001a
oE·gi\x000bE_¾\x0019tëªO¹Ù:G<·\x0007þhoËä$½$¥e/\x0016K'÷Å¥Û#ã3\x000bË(TV7P8[,£½0WÉOM£Ê\x0018t±UÄ ó+k(+]YZâ¦ÅXfF\x0015]\x0019^|1\x0005Ä Ë\x001dëN/Sa"rSÉ\x0019w/³t\x001bõ\x0008bÆ0yÌ\x0003ÁüHolTúXbiÙÅÒ	
.=vü$</p><p>\x0013"\x000c=|äM0*</p><p>¨¢}hx\x00141ìBÁø\x0002kÑ^V1\x0004¸Ë!4\x0013²\x0017Ã\x0001	Û\x0010vÙ,ðlcCÓ¡)¬2²!§÷\x0003;Z,-IFbiÙÅÒ	m4ËUfÏ\x0016ËÖUuàÃµøÇ¦¦-³
aÁ¸×ÐÝÝ\x0012ÆF§«\x0006à\x001dNÎ¬ÅÒ$Ii$½X,Ðó+k$ÒÂ\Åei 4ZP@/b\x000cn\x000f\x001c<T­#t5ÀZ|Gñ­¬n0Æ\x0010f\x0000E#\x0003b8<ÌIg\x0016Û³´MÇv\x0017­ÍNÎ¬û¥%I^ÄÒ²\x0017¥\x001bX\x000bÜÅ\x0017\x0004\x000bè%\x0000³\x001d\x0000Lè\x0005µ`\x0019Y
h½\x000cÆ\x0017e\x0018Ã--²¡«\x0001´3\x0000Ì^ãmÆ\x0011ìNg½ýÑéäÌZ,-IFbiÙÅÒ	½´þor4\x0005èv\x0001'\x0013å]n±´$IR\x001a¥e/\x0016K'7\x0017Ü;³°|Ha®$meuÃûîdï\x0016KK$¥XZöb±´,gÄbiI¤4\x0012KË^,åX,-IFbiÙÅÒ²\x0011¥%IÒH,-{±Xº+þõÕ÷í\x001bòÅ¥Û;ËYYÝØñØ6.ÌUL
{?ÕÝf±´$IR\x001a¥e/\x0016KwÅ'FNÛ7äBq»Ù8äE°ôüÊ\x001aÜ1L,íÅbiI¤4\x0012KË^,NîÂ\ex|2?5]
 \x0014ehê²ôÌÂ2ÚGÙ\x0002«KëOP\x001d'</p><p>%&d\x0015àÊlhAùØñ(`8¾Õ\x0000­\x0019Æy9Ë0Ö\x0002Fáë"1º0Ðb¸\x001d´¸s±Ls"Û2ÖÏ)°AïwÑ\x0016KK$¥XZöb±tB\x0013wQ8[,\x0013\Á0¸·ÚÌÒÒK·A³(\x001c>ò&«àRP(\x001bQF\x0012½\x0006ÞÕ\x0000-\x0003\x0001ó"3óT\x0003Zvep=Ìpàà¡j@õLEÛ	ö\9clµ,Ó([#Wë.RîºÅÒ$Ii$½X,ÐF´ñd,KZ\x0011` j$UfCU	çd\x0012²ËÒt« _7-=8¸\x001fùa6W\x0015Z3¨1°u\x0001ªÿÏ~¹\x0007GUÝq¶ÖþQé_ñ\x000fµ</p><p>:Z´\x0016\x001d|\x000cè(Òò\x0018¬ò0:¶ð°HH ò6ð0´Iå\x0011y\x0014BMB\x0008  @\Þ\x0008Ý\x0004HÈ¼¤	Pòbúm~áæìÞ»7là,øýÎgvî=÷w~çÙOl\ÚØ-®¹\x0000ÿYhÿÜ~Ð¥\x0019a\x0002	]h.í'°Gñg1LH/,\x0014ýª.
eÅ'WìTn1eQÚ\x0006CYa¼ðgCVÑ\x0019ýÑÍX\x0002×R2c\x0010R-ë4¹4ü\x0016SÐDÆ-]ÚØ3VÇ§Ô`W²\x001c\x0004ªK\x001b­îVt]6¬ýïr;Af\x0018	$ti¢\x0005º´ÿ@¡µ¢¢Ö\x0000Û\x0015w\x001b°SÃ{ÅåV<ÖÙì¥X\x000c:]\x0017}p!Â\x000cG\x0005\x0018ÁB(À¸+Za±®LG\x0006ÒA\¦H±Zæµg¬";1ô\x001e`P\x0010-Ç±´üã[Ô¨'\x0005]a\x0018&Ð¥\x0016èÒDTÙrÜËØÉ
.Í0\x000c\x0013HèÒD\x000bti²ãÛ³¾Æ÷ÖhßÞ\x000f\x0007º4Ã0L ¡K\x0013-Ð¥		\x0012èÒ\x000cÃ0.M´@&$H K3\x000cÃ\x0004\x0012º4Ñ\x0002]\x0004?Ërk×\x001e¿ª}\x001b7\x001a{ýÇÍGKèÒ\x000cÃ0¾B&Z K \x0004æ\x001cUÙ3¾èçÑù^\x000cø¤ì£¯ª\x001då·á×ÆÞ¥\x0017¯ÿÊá®¢K3\x000cÃø</p><p>]h.Me¹µ}\x0016\x0015ÚÌµ\x0015~\x001aõªmèùÜ¼r\w{¸\x0007>w¾øjÈÇû,ng%¯ÂÈ«!a¸\x0016bæ.\x0002ê-ê_\x00194´ï !²`åzµ³QfåÌ\x0005è \x001bP;c$c¾lC\:}¯ëÙ\x0017úõxò\x0019¬\x0015\x000eþË\x000b\x001fìöØÝ\x001e\x0005)Û>ûâ\x0007\x001f¹ÿW\x000fß÷@÷§y^÷o\x0017Ã0L°.M´@&A\x0002ÄxÀ'eþX´Á½1'csªÛì\x000c¡t^wiH¬ÜB°ñH4[¼W¦ \x0000v­v\x0010\x0013ÆEäÔ8u\Ê ÒF=\x001aB?ÉÚáÕ\x0013\x0017ÆBjs4¥£¿¸ôà7Bg$®8XÑ°|ËþÐ±\x001fKO°ótµÃ]Sp\x001e.Ýoððl§;}+4"Z÷o\x0017Ã0L°.M´@&ÁÀ¦ÂúñEí\x0012i\x0011k+ì»\x0002Ãlq-®+×0a§É¥èùÜ«!#@Æþü]§/B{ñwo\x001e2µ3\x0006cæ¦ ldÔ\x0014 -ÄxVò*qué)}dÄiritÆ\x00120ðÍGËàÒ¨w\x0014~¿éHñ¤9I\x0013?J\x0014îÕ»ïÀ!o\x000fxýíO·\x001eK?úøS}\x0007
{iÀë\x0003^\x001b®û·a\x0018&XB&Z K\x0013í8Êî9Ù1\x0016/?cÓ_Ü\x0015¾</p><p>Ë\x0015[ÖBwå)\x0006Å«½\ZÕÝ-yåOÌôªaÂ(Æ8|[:CGEÿ\x0015­0"=ñ©NT]\x001amQ\x0000\x001bÏLZ	FÙ¢ÌmÍ.øP÷_KO°ótµÃ]Sp\x001e.Ýoððl§;}+4"Z÷o\x0017Ã0L°.M´@&zH÷/</p><p>D¤Í\x0017|-a¸käÔ8±e@Yg/ú'¤\x00172l©.
¹â\x0005+×KýÇ«²ÇM7êV\x000c Ïè\x00003Ç8\x0014]&\x001a=\x000buÖÈ¨)@dûACáÒ\x001fÄ'÷\x001d8dfÒ7Fíñä3âÒ\x0003þqü¬£g.HÉÜ\x000e~êÙ\x0017ÆL=zÂ´\x0001¯
×ýÛÅ0\x000c\x0013,¡K\x0013-Ð¥^ÂÒ*\x0002\x0017iaYn­å\x0012[òÊ¡µÎf×$Ë ô\x0015×\x0000Fù)¹Æ\x0008ÊÌ[(±Ñ\x0001R­ö4æª³Po4OK\x001f:×4oùºIqIÉ\x0019_Ä§¦Ã¥nÜ=avB³KÏK¯q\x001cyoÊGc&Í\x001a=a*]a\x0018Æ\x0008]h.M4²©°¾³D\x001aôYX¢ýD\x0000\x0016>t¶ñ`EÃ×ÿ©?pæ*\zOiÍîâK;OW;ÜU9\x0005ç¿Ì¯ØWít§ïsFDëþíb\x0018	Ð¥\x0016èÒD#°ßNti\x0010S­ýP\x001d.Í0\x000c\x0013HèÒD\x000bti¢Mõ6V|GÄñû&[[×¸« æK×¥í'.\x0017UÖ546Eüë».#ù\x00059×~®\x000eCf\x0018	$ti¢\x0005º4ÑEÌæ\x000b6.Ý5úÄÀ¤b|Uú'\x0016w^pg¸+ê³3¸­N¯-·è(¿U¿Qtia@B&Z K\x0013]ôO)³QâÝ\x00055»</p><p>j6\x001f»}äâáÒ+îÊºÜêÚº&|sðý±\x0018S­ýh\x001d.Í0\x000c\x0013HèÒD\x000bti¢î3NÙ(qá¹ºßÄ\x0016v\x0019×åOGß]ý|g-.ý}b1lÚfbdV¥ö£uãÒãzu¹^q;å÷Kzeøx\x0011æÏZÍU>êüëà«eK°¿ö÷±ÛÕ-ÖØ¼\x0004Ë?d^¾òêoýwÇÜ:¡K\x0013-Ð¥.l|\x0018\x0014½Ú{~ÑÝ®»"\H)ù¾¶±¶®©ðÜÕ\x0013\x001a®ÙL\x001cöé\x0019íGë\x00187Á¥ÅpZ\Éã& ´Ã¥¯ÍÒÁ§u\x0005âÒê´vöicW·N<\x000ers\:®ÍÅ\x0018¦óC&Z K\x0013]Ø»tá¹ºçç\x0015ýx«ëøüEøåÄüÞó.^i|kYi}cÍÄ>\x000bK´\x001f­cÜp6RgN\x001b.­Ä¿ûß¡=	ô|7fW\x001aâïA:ÿÀtiæ¦.M´@&ºðÇ¥\x0012îº'úÄ=Ñù?\x001asüé§*/7\x000c_\ÒÐtÍfbÿ2óZQ\x0013'GM\x0002Öl;`³¥ÏsÝ\x001a_Ko8xrqÆÖNti³(ÉÈÿMGQ\x001e2¹H}Ø:EtYq½¹òÄc\x001f\x001e}0n^ÔØw©ý\x000eM"×>æ\x0012óÑZjÔ\x0006æ÷Û:¡õ}{¾}\x001f§P\x0006½Of~äû=x\x001fD}+^}Z¶Ô«åË·\Åâ5y¯|\x001bü3ÂÜ*¡K\x0013-Ð¥.ÚåÒw½çz|VáÆ%¥õM6\x0013#³*ÍkÁ¥åâÝ÷Æí-­Á\x0005>åB[£\x000cìøö¬úTíæ5·M¼êÕÎjêÒ_º¾ÛYTµ5¯L\zS®Ûpé¹EY\x0007OvK·jµK7Ê\x0004ód\x0011ËÖºæKe°uÒ\yÞÖÞ,·×bg,Úî°Ú$ïíìãÑÒòh­Blòvû´ù=½Ûâey<²\x000f\x0016\x00071«½Wg«?ï}ZmÔúoÊ072ti¢\x0005º4ÑE%þ¸t×ñùpé;#\=f\x0015¿Ü08¹¸ñÚµ\x0000]:5{Ç¤é±Óçþ-!5
sâ6ë+tÄ¨u{ó\x0000êñ\x0008xj\x0014\x0003Ü.JÛ õk¶\x001d\x0015£\x000c`¢±Öç¹n\x0014H%jLG\x001fÙ	ê±
u{¸mîùaæ£»¿Ámìß\x0017§ï<<oñª-GK"¢ß± iúüD»jÞÕSæ|\x001c\x001e=iáÊÌÕ9Î\x0017_zÙÿ_\x0019³ÛXê®× GÉª\x0015\x001bS<TÙs´}.Ýbh×-ÍþÙîÐãT^\x0003þõQwe}4­Z¯×A¼w ü+â¹z\x0007TÚ÷{°vi>¦\x0003{¼|ËU|oT1o¹I¡K\x0013-Ð¥.ÂÒ*Úté;Â]¿\x0018ß5:ÿ®±®ÇfºR×tðtíÕú&k_5¯\x0015\x0012ò&$\x0016ÀlÍº\x000b
NÛþµ8¶8³óºrã\x0011X·÷XØÈÑæ§\x0010]<\x0002Ã¡ßêrj[cº\`:ÖE(½WýË\x0013§}\x0008\x001ap°¢A\:k¿küäé\x0019{òÒw}ãpWúsêÆK²v½\x0013ñE»\Ú,²­®iåÒ6:W}#]ZjÌ\x0016gv`û\x001dúïÒ¾ú\x0004èÒ\x0016\x00071¶ÑÚÁruó?></p>
  
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

  
#### CWE Id : 16
  
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
<p>Location header URI length: 274 [https://authent.webinaire.numerique.gouv.fr/auth/realms/master/protocol/openid-connect/auth?client_id=BBB-Visio&response_type=code&scope=openid+email+profile&redirect_uri=https%3A%2F%2Fwebinaire.numerique.gouv.fr%2Foidc_callback&state=2SSOiFCjNVdQPA58&nonce=pmFdADVUTOwo5SCH].</p><p>Predicted response size: 574.</p><p>Response Body Length: 795.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
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
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
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

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.min.js](https://webinaire.numerique.gouv.fr/static/js/jquery.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js](https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.autocomplete.min.js](https://webinaire.numerique.gouv.fr/static/js/jquery.autocomplete.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.min.js](https://webinaire.numerique.gouv.fr/static/js/jquery.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/global.css](https://webinaire.numerique.gouv.fr/static/css/global.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/toc.css](https://webinaire.numerique.gouv.fr/static/css/toc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/remixicon/remixicon.css](https://webinaire.numerique.gouv.fr/static/css/remixicon/remixicon.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/toc.css](https://webinaire.numerique.gouv.fr/static/css/toc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/images/favicon.png](https://webinaire.numerique.gouv.fr/static/images/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/global.css](https://webinaire.numerique.gouv.fr/static/css/global.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiYjM1MjQ2M2YxZTdjNDQxM2Q3YTMxZjMyYjlkOGU4NjY0MzE2ODJmZCJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/nico3333fr/van11y-accessible-modal-window-aria/blob/master/LICENSE`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiZTUyNmI4ZWNlNmIzOWU1ODIyNDk5ODc3YWQ3YmJhMTA5OTg4ZWJmZSJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `eJwVjMtOwzAUBf_lrqsUAmmc7KqiihUFBbqN_DguhsQO13a7QPw7zvKc0cwv6ch2TOEbnnpCU--UgMZOPXRoRF0_dp1oW2lapeT9XRkCyoI2pDMzfBoXDldnwMU2sDJPqUCDmJyXyYW1-pnSEvvt9gZVTseofJ7B7iejuoR8rSwXNukwr2HL8jKvZXgdDMzIiEvwEdRbOUVsyAevy6JlPpr90_nj_XQLzXB4LnJMMq2oHoaTOx6-Xs7m7XXfCPr7BzYUTz0`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `d09GRgABAAAAABVIAAsAAAAALOAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAADsAAABUIIslek9TLzIAAAFEAAAAQQAAAFZJwk67Y21hcAAAAYgAAAFuAAAFNuKa/PhnbHlmAAAC+AAADhoAAB2IDPM492hlYWQAABEUAAAAMQAAADYbffxWaGhlYQAAEUgAAAAeAAAAJAhwBAhobXR4AAARaAAAABEAAAEcSCAAAGxvY2EAABF8AAAAkAAAAJDonu+SbWF4cAAAEgwAAAAfAAAAIAFWAFluYW1lAAASLAAAAR0AAAHyFNvC+HBvc3QAABNMAAAB/AAABJyXrlRreJxjYGRgYOBiMGCwY2BycfMJYeDLSSzJY5BiYGGAAJA8MpsxJzM9kYEDxgPKsYBpDiBmg4gCACY7BUgAeJxjYGSZzziBgZWBgYGf2QNIroDQTA4MVoymQJqBlZkBKwhIc01hcPjI+NGN+cB/AYYc5gMMH4DCjCA5AHlACw0AAAB4nO3T523jQAAF4ZFFy0nOOeecc842a3CRV9D9cg+swOboXRlH4NsBF0zALoFuoFk7qBXQ+KaBx996ttGZb9LfmS/407mmcL4qf37qseFYnxedsau+tqif2KKHXvrq+wZoM8gQw4wwyhjjTDDJFNPMMMsc8yywyBLLrLDKGutssMkW2+ywyx779fsPOeKYE04545wLLrnimhtuueOeBx554pkXXnnjnQ8+KeuPafH/aDs0v/6dla5XdFawK7DNcCdURbimVXe4S6pWYHsC2xvYvsD2h7unGghsO/y6ajCwQ4EdDuxIYEcDOxbY8cBOBHYysFOBnQ7sTGBnAzsX2PnALgR2MbBLgV0O7EpgVwO7Ftj1wG4EdjOwW4HdDuxOYHcDuxfY/cAehH98dRjYo8AeB/YksKeBPQvseWAvAnsZ2KvAXgf2JrC3gb0L7H1gHwL7GNinwD4H9iWwr4F9C+x7YD8C+xnYMih/AaHUtUQAAHicnVkLbFtnFf7Pf53rPO2a+Pq2S+z5sdhxk+Zhx/byclrFuU7XR2jY1tCmWTvdZh1jo6WP0a1QTbSj6pbQscqgske1sKfQtALqeFQwMgkM2nhIpRrVQBVI04TYQBDWYOI7zv/f61fqlJS6vvf3vfc/5zvnP+c7578hAiEfHzBtFHYQO3GTNYRASHbIjhVm0Sy6A/6Af0UsGosKeCmEgzbwirFQHLpwYAG7C+jYiQP7BhOJwX0HtL/nRjPdm7ec3zJy68Az337mr8Gh5uahUXYQxksfgxVslN11e3tHZ/unegYGZowH8UAqSnBFySDZSEiFN4/InUfZhAMOzQLmQJw6ZLwbaIOA34wXRHysydsGXXEIucBugUAo2uX3inZHEXIdCAd3dP34tk+PJ0PHn/hy51D8xddfXttbW+u95Rt375y4+7T7Zqu1Hwai49Ho+GfZIRrs7R3t7X18kRBu4Y967fUOR3/XrbQvMjy4XhhaO6ruGp941OFYterkzvFd6id/YkjBg8rEjPYSQgrrUYN2R3A9ImEpLPkkX8QXqS9nf4AtTLSL3fGy33Z2h/rVdFpNZ8rYeOL+HdsisVhk247LuQGcYQ+n1ezlcpaoJc/yAcIiDOx5+jPEScAWtnkkj81n80RQM7RqF1XtIpzJDVpVbtcLpklhkNiIRFYRUgUOXA6fhy1ODHB5HIIUjrAvPQbviha5bmG4bmWdGd41yw0rx1RVFVYv/Lym0WGxOBprhO4aiyV7n6rCRCbDoJiK5NvJStJYTgN4QEBf2vBbTol2u1CrPRRSy+la+B2dyf5ThdkMt/3jd4Q/0HlSSUgTyFUQQw/Qk1Cb1B7WHk5Crfp1Nj4CxxXtX3Qnw6f7K0WbWGRDjM2hY/ND2pvarAJtV5PaLMST+nMf/1l4n37AZAM6FcxVIMMJujN7lstHmXBG1eaScByOJwnlcg/T0+jhKrYSuAayWTYDnFKpmJyfR8n0dPYYPZK8Oq9AnD2uzzlHX0YsbPVkpsITQEgB+npG0d6AtYp2UT9nYE9GgbU4wt/aG0omb4tEX+C28NnUZZgAe64q0A9xZbEtKL0KAuCJCEFtToHjzE912WcxSApey2M7VrAHIwvNkUFwq9kMswfi5e35Dp0x7AkwTU38CP9m6BE39RsD2PMvbsmGjHHO2eM27OHz6JNMkTaL9swr2iwO8nYzbNweZgzGvODWRpPwqnacRf5ftC04xkQy1rwQJ2xlAH1spifzq0e7s8/SXdo/k8wdSj5GOjgOM394zHAnzBiAdHsx1jcJ0+ihBkLqPTa7iGHuj0A45HAiqq5oL6MNTySsCu87pYUjkpN+mJacCyudUhrTU4UzWlxyOiVh1CllMpITI97gnheQe6aJTHwkgBhQnpQTbitINXsYHeEIaUn22DzCaJpJY3oMBZj1akpwp9TMwhXBLazGm1e4QjdXllY5PWl7dZtNIk0xm41cmoO3lOyHmBi/hLeS2Q94YhTXqSBpX6IWlOXCWCAmY4SW4/syXNh7UZmGBqUsp5dhwvTF5BQ0DC/CF70RfPUxlrABc4ABXS7M+6eVqWnlq1PK41PK9HLBwqVpZRqn4EScbsTb1zHuazgn5VEwZvpoXvn3VeUjDL9X55V5HOHveYXbuR/tHM/xODBCzYWILxKOeFjOso8wmlGdUjaBK56BOW0vrjudV7OfYHFAP8QQeU7bC6fY1+DvYrlOVvk8Uqlw2eaxVYRtvnr8wgTM5eWn6ZgW52GFGtQiHdkEvZDS1eTy5ibUIZBaQmLIrlU59k4JxxaOYOR1KNqYtnUY2tVqFU5Au6JthZcV7be0TZ9/AOdvJ9XEgtHqi0A0dDNWGTMn6s9cpH3WoGXaal34O5PWx35bp/BS9i6V5Gs7m28iVlLP4j0AkrxIzDr4T1Kr2MsmN1vzws6yqyZFxcsWC8q0ZneqhBRsWk0+wbgAJFaDw0U5G25Cx6EePMxlkKLQY4f01Fe1hxR49D16Gukqo13kLjspOdFd7/E7aqGuHuLyg7wPYx2iC2TWXLlZnxWHWLSex3XMnw9ss4NnXmnnVdI3Hj+475uy/M19h7Srxujg8T07tg+sk+V1A9t3/KYw3BO/p6/vniPsEPd2e73dCXYQVvf1vH306Ns9fbnzwpU1rSNbdu/eMtK6pjD6ojEVD6oxFQ+8v7wD7XqY1BEXaULL+jBnRZNuUCCG9MsaSheNxgIWaMOTHBBdNFYRwFZTMAeiLiqLZsCTWfjSAe1v/3ll1Yo71z2VFP6YfD77SnjIKp9483c7Jlsnd97mqWn44DmLNbLeC48Ph+ul+599fdvmz3/0zimHY7PW3bE94RUq1ksPXPrK1qf6n0oueJPP0zvbHxzc8/ydNV2TjTWe23ZOtv71Od/6iNWyLzl857bUxMpVI2tWPPiLw1+8F35OvYntHXoc7Dc1IP/UIQNhVS4OAeBEHRPcmRwPw6yaSqeF8QxLHwyGY5JTq03jv+I4HSci5gmLqrA5EI6EY0j1Nl8TCvSgeLMun55EQSnM5lp6IZ19CWNoLGOtczA1sIdJXLiCVyQnarJbrU6JFPJoHGNKYvUrFI3YPPlSE0DQMSkFrShhjteVK446awY0hN2qVxmrRaIXeOOXs3sc7caMqgdPUcni2WBDSdSvy0GJExl6gXbkBLE8yGQvC+6c3fsRF/OhTG6+xot6ALeArR7rol1sgWKHnuLbgihSEG4KgmqJa7MJ3uUjD7WyLt/E7WdrVYVsJ2P0IZfYwnqaYAfMtii++hJnG74eS6e5mjNcSarY5zqQswwHqoLWNGqC1iLnu7jvi+sU75LL1ikB6TvAWvFy1eiHyLBlKw71s14/zXsJU0k9XEM6b6gisg0Pcvyya7a6FKQyRRD7L+xOCuvN1sGJ3U5L2X6ni8HjW2LJHNHpywky26mcD+ViyimFOtpGRn88OtLWoQ7uP7F/EHugt5ySVssjA2M4dBe7xx66KxRK7B8c3J8I6clmKsLgwUho/18oKngNlHyQR7MEElb6WNGFVg5pSUC8PKppOJUDZtSUjcj5ViM/S/BUsS1JIMUC20giuKy9sQ4egSPrSjs9bTOs2Kh9H4Y3Gr3lJqEFZdox5q+RWlEFNk8VLRYr3KMd0D4ruBcycBgOlIq+qD0Nava7aOJ3YZOxlu+YbsJeWyBm1s/UYy3NfXhxp2PZl/h5Xs3gZ1lzct/SOQfQjuvnT64FKv+S4U9LJtBJlkDsa+TPpv8vfwSjR1pu/gR567TsBPLrKA0e13PcuxST+EVcZfw1AIiyLKC3qyXRVFM9V1VV3ikviTW12o/EaiqKM6IkLt4L9NwQs8gOuxVE7FtYzMWiy+63mxHeXHV1hcigLttTiRmzVDEjirRKhCFuASniRtaHylhfGf9jxDVhv+szak0uOYAxjSe3q2M9L3L+WDah5koLy4lUiKU01oEHMEgzeoLryQ5zmP+nnFIqJWFDXZHX68N4ipBu0s8qT4FluF5njn9aQNLTs5/m7yD51OO+D9iXkVBriqlK6Tpz4wLNqAtX0nqLn72cSlXrF/leMa0/xu1Ic/4KsQexm0hlD6VSMKEurlUdS0WYFMYNMm0TsF2T4+DCts3nFRHrEsWrub+xpn34jg1dlXdXdPb4TS0uhFF2RRGEOlrbs/n2RFDwrQvand7KNX3NTmlDmfqm3NCOFF0Xwy00uhV7ijYQ2YtLFzPghiqeU3K1mPw9neKuyq4Ndwy31zT2BZcbmhn1vHuD5GzuW1PpddqD624RgkO3b+6uJYt6BB8JL2FZDJELZhk7YMlXHxDbaCSMnbJLiJW14d54TLrryRc3dnZ/6TN9qc7OHnaaMi6WBf1RzzPPT42It2xdVaN8bkB7c+wmfjau5vY+qmmrcB9fAwIsn3Fn4kB0QrirTcD+nK0AexeM0Ot9dpcQxb3exOGDBw9/f/VqqzV5NtX3wNeefrKbjk8cPnTwCz9oCVqtw/mLf97S0OC8+YWD+77w8G5wjTyxL067b81OjjY2ulwv4tUjk9qfPvnE3gHojhXtw9j+lbAqnc9lmScTe09yLPuSqu+zMP7TLC+2sajXS1qabcyQ+o1ayWRVEge5CXMUpWFD5rEJnuKOlGchUoI6lf1tiIvk9RGs0FrNCJq2T2UTgjttbPjcjCNY08HeS+02jeP6rkTZuOlnGcNWuKjNsIvCo5eUS/2nNj1072Rff3/f5L1zbBB+BK92hPO/2eChjU8Ya6HLbL+OVHMceaY0G7DfjaGy5KW+a5Sd7gjn+xnerCSOdj6CT7YvArDplNx5NJHvafjz4Y7Ce9fzcIZ5ldV3bP+zCTij5vYhwvvCNH/XTuQioLAIuZ2hTeezR9s7OpRoDgabE0Pfyg0ez2fp/TBbcocPcnnF9cmkFdm3RKOv4JXy2kv2zwUoKmpQnlNQA7ReC2q08MeKInxbFP22sqUcUrXwdwndRz/F/tSKkdhUXC2aGNVimbCAP9BUEWDL6g/E8BKChQuzLOJmoUq01FVW1llEbR7+kWwKhluGe9Y6G8+ynZzk/L2JirWVC+9V1orU9HvXcOOn2iPbGoZbjg4n+nsMf+m6K7DTYv25GbcFcmBZGOjJV773vVd+dX0gdOtj6ccCy0Gj++FV7gfvUn5YA/n3eDEZ/NfqppfOJc+dU157TTl3LlnWC+ncXfxP8j541fBB8/V9UKp/bgkHlIBY2gOlSHQcR4046FpuJDQtCoxyPplJDo9s3Zwcn+xo1zL/I0h+nVz72s7dr69Nbn738IP37VGviRlTHqceMz03FjWL8S7pwyVAL+3O6yP/L0ERSDgAAHicY2BkYGAA4qWF227G89t8ZeBm2QAUYbh9I/oxgv4fyrKOuQ/I5WBgAokCAIXPDYkAAAB4nGNgZGBgPvBfgIGBZQMDELCsY2BkQAXuAFbDA4IAAHicY2BgYGDZMIqxYQAfoTE5AAAAAAAAAABMAMgBHAE0AWQBmgG0AcgB4AH6AhoCLgJIAmICggKWAq4CxgLaAwYDQANUA6QD/gQYBEQEdgSWBLYE4AUQBXwF5AYKBjoGYAaGBroG+AcsB34HwAgKCDQIZAh+CJgIzAkeCVoJugn2Ck4KnAsKC14LpAvKC/oMJAxwDH4Mtg0QDU4NlA3QDhQOaA7EeJxjYGRgYHBn8GVgZQABJiDmAkIGhv9gPgMAF78BsAB4nF2OvU7DMBSFT/qHaBACITGbpQtS+jP2AdqZDtnTxElbJXHkuJUqMTPzFMw8Bc/FiXslKmzp+jvnHl8bwAN+EKBbAYa+dquHG6oL90l3wgPyo/AQIZ6FR1QvwmO8YiIc4glvnBAMbumMkQn3cI9auE//XXhA/hAecvqn8Ij+l/AYMb6FQ0yC0T41dbvRxbFMrGdfYm3bvanVPJp5vda1tonTmdqeVXsqFs7lKremUitTO12WRjXWHHTqop1zzXI6zcWPUlNhjxSGf26xgUaBI0oksFf+H8VMWO90WmGOCLOr/pr92mcSOJ4ZM1ucWVucOHtB1yGnzpkxqEgrf7dLl9yGTuN7Bzop/Qg7f6vBElPu/F8+8q9XvzD1U2IAAAB4nG1S6XrTMBD0tBxJmjRNCrTlLFfLZY5ynwUKlNdQZLnxh2wZ2e7x9li7tuO06NfMaHdWGslb8Hj1vf+vfSxgEedwHhdwER100cMS+hhgGUOsYIQxVnEJl3EFa1jHBq7iGq7jBm7iFjZxG3dwF/dwH1vYxgM8xCM8xhP4eIpneI4X2MFLvMJrvMFbvMN7fMBHfMJnfMEuvuIbvmMPP/ATv7CP315fSGmKJPfDSOuG6ChRQxEEvoys1Ip4x3EHekIryw0V5HJrzZEfmKOE+KjFs3aFViF3rLV4VtrZjPX1Od0ppUsx0bVla2OFFRsdTOc8WShrROW5cUqfmY7P7qy2pSIlbcBaxYYN446BLINIAmEplRmjuORUyT9VmYMTc8wJSW0y1Y64x4qDS4HSKlfkV2OycIFqI/gpuiqI+CUYOW2sjnNlE6Ed47kddcLdfQdMGHJh2af8xs+5nJJoBEk0ghAdglAahHzdhtGTRElobCzyyCS0PSeQozZlHuRIiLRYRJo1QhRBrJLC36lUhx0apaKYpXZWIbdUixPuI0RXT22UlMHwR68J3eZvobLmuDNGXVaFVmVT7qoJzcjEYZULITpxpoSVXFxjmpAVk9wKyQ/ULU/Lx2BEqR0aXcQcPafWFtoVcVH9ijnBVSxXQvkr3X6Lul3P+wdkWXj4`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/select2.min.js](https://webinaire.numerique.gouv.fr/static/js/select2.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/select2/select2/blob/master/LICENSE`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js](https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/blueimp/jQuery-File-Upload/issues/3633`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `Creer_une_reunion_Improvisee_V2`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js](https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/blueimp/jQuery-File-Upload/pull/3435`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Evidence: `eJwljl9PwjAUxb9K02cycDrY9mIWDPFJNCgvSpZ2PYNq187bbkQJ390uPt2ce_7kd-F1a4Q_wfPy_cJZiIeDyFFt3FFbPuNrNxBpGKbtKIxWSFg14peNbvBMalgWRP8xLBYo4i8QGDqhDbtn-ynRu2FK038C3osfUMIP18OMN57aOrgvWF5yZOlS5miwlLcFsjxN74oiX62EWkkpbhZR5JAtIlITiWBD3ZMbIxDFtkIrBhOiqeCDtiJoN62eQuh9OZ-fIeNTExI7dCD9PSA5RrSkpeiZxnXTcEvi2E3LsI1TUDXB98568LIVxmPGrbNNVLzvNqp62L-9bs8u260fY9kHESYr3e22erP-fNqrl-cqy_n1Dzv_emg`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>{"csrf_token":"b352463f1e7c4413d7a31f32b9d8e866431682fd"}</p>
  
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
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.ui.widget.js](https://webinaire.numerique.gouv.fr/static/js/jquery.ui.widget.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js](https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.ui.widget.js](https://webinaire.numerique.gouv.fr/static/js/jquery.ui.widget.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.min.js](https://webinaire.numerique.gouv.fr/static/js/jquery.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.autocomplete.min.js](https://webinaire.numerique.gouv.fr/static/js/jquery.autocomplete.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js](https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bugs`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js](https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js](https://webinaire.numerique.gouv.fr/static/js/jquery.iframe-transport.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js](https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js](https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.ui.widget.js](https://webinaire.numerique.gouv.fr/static/js/jquery.ui.widget.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 14
  
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
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.min.js](https://webinaire.numerique.gouv.fr/static/js/jquery.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js](https://webinaire.numerique.gouv.fr/static/js/jquery.fileupload.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a></a>`
  
  
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr](https://webinaire.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/](https://webinaire.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/5.G%C3%A9rer_les_utilisateurs_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/5.G%C3%A9rer_les_utilisateurs_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `61562774`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `23456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/6.G%C3%A9rer_les_documents_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/6.G%C3%A9rer_les_documents_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `00088822`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/4.Activer_le_materiel_dans_le_navigateur_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/4.Activer_le_materiel_dans_le_navigateur_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/4.Activer_le_materiel_dans_le_navigateur_V2.pdf](https://webinaire.numerique.gouv.fr/static/misc/4.Activer_le_materiel_dans_le_navigateur_V2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `23456789`
  
  
  
  
Instances: 7
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>123456789, which evaluates to: 1973-11-29 21:33:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

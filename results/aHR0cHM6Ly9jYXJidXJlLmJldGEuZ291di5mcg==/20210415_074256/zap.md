
# ZAP Scanning Report

Generated on Thu, 15 Apr 2021 07:39:05


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 9 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 9 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| Cookie No HttpOnly Flag | Low | 6 | 
| Cookie Without Secure Flag | Low | 6 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 6 | 
| Base64 Disclosure | Informational | 6 | 
| Modern Web Application | Informational | 9 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 6 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 5 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png](https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/robots.txt](https://carbure.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png](https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png](https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/manifest.json](https://carbure.beta.gouv.fr/images/favicons/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/safari-pinned-tab.svg](https://carbure.beta.gouv.fr/images/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/sitemap.xml](https://carbure.beta.gouv.fr/sitemap.xml)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/done/](https://carbure.beta.gouv.fr/accounts/password_reset/done/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://carbure-1.gitbook.io/faq/mentions-legales-et-cgu/mentions-legales-et-conditions-generales-dutilisation#cookies" rel="noreferrer">Cookies</a>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/images/banniere_home.png](https://carbure.beta.gouv.fr/static/images/banniere_home.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=áçïÀK/Ýgÿ0%ÙzÛqyuµÃÃ[8\x001bnyeÙMr|×å·»\x000e'áLb­\x001d\x0010ÓáF8+ËòFTÛé9Þ{®\x0017\x000b\x001aSSÕ ÞE¤\x0014e¶9©§tµ^¡¦\x00190²¶ëÓ÷\x0016Ð[GÛu8ïQÚ$\x0012\x0018:²\x0002d:£Ì\\x0002;¤/B\x0003î6Þàss¥ê\x0004 çËtàn_ìº¯ö
îÍ¾ïS_à:&åÐ\x0007hØ6]í\x000b1$tý§TêñTBâEJ9\x000e²\x0002
L­\x0005 #®ï\x0011>\x0012]¸1'\x0018)	ÆpûÖ­HVº®\x0013Î×;àK-M
\x0008Q£5E^\x000cóÆDôÎÑ7-Z)²¡p·¿\x0010©êH+´R9AK¤p\x0010\x0003\x001b@«Ô%¢\x00061gØ\x0006É4\x0004ä0Ûý \Òäb\x0018\x0016/1¡*eÜUë|¬iAax\x0008\x0001ðù\x001f\x001en\x0008økÕ*CP\x001bãN\x001côi\x0008+\x0002)úf#Ñt\x0006[\x000búëH¿°®Q´N³Fs)<WÞÑÛÀH*ö¤\x0006a²:hD"M.A%Ñ3(\x0006c·¾"\x00028¤¹Ò²(%h-\x0011r@4<ÖJ²ëKoúË\x0003R*\x0019ÞW\x0004#U\x0017§¸Ø\x0011U\x00175ÊßBc\x001cb1Á=T¿ÂÐ#\x001aÁò
\x0017µl/¡Ù\x0008ê&Ð$æUã$\x0010V¹Äù\x001e\x0017R/b õ+
ýï
\x0002ÉÒ×U.\x0006Ð¤\x0014á \x0012ª\b
C\x001b¢Þ)Ì\x0001\x0011<JiÐBÆ!]£R\x0001¬ÏqVÑw
õ¶O¸³\x0016E\x0011\x0002&¦Îx¤©
Á¸\x0010\x0014*`GDGP!á\x0013
hú¶\x00101¥ïHÃ¹\x0001ÏKÓÀv\x0003Í\x001azÂ2\x0006d\x0014h4^H;~íÀþ\x0016é\x0002-dØ\x001dé8Þ
¤ùRÛ-2B@T;q<<i ÜãcDx	^ ¼N\x0017\x001e)è]HâåpR¥¤©Ü}ÿdùKLÒá$ÙG»Tkd\x00103Åv'ÑÇ\x0011@(\x0007Â!dZ²R>3Ø ¸J^¸D¸\x0016%rM:÷£Îðø''Ô[8ÜSì\x001f¨&-AöxÙ\x000fiÑPr@V/»8ôà	áx5í\x0018\x001cu·eV¤þ¼\x0010ÓÅËYKQÎØ\x001f1º^±é:\´7ø@d ,ÆìMç\x0014EíÒûè¾Käà\x0003Þ\x0007¤\x000c('gkTh£´ÀÇ\x000e\x0017k\x0010r¶­%Ê
e9"¯2\x001cº\x001d\x001d(P2KÇ`H®\x0010ãà$J\x0002á®8Vê]\x0002ªÃöà\x0005A\x001aF£\x0011ªL\x0002\x0008\x0018cP\x0000¦Ô,V
\x001f5½\x0017C\x0001y\x0018±Ä\x0013b\x000c\x0000.ÅÃ´ªr¢4´Í
ðY\x000e,¯g4¶¥ÞZª<rpç\x0016:Ïxzò\x0005çWdeÎ\x001cEç%Þç\x0004ZçÏ\x001b¼ÓdzJÓÉ!1\x0016X+±ÑCtÄè\x0005¬C±bÓ]²XnX¶Ã¶ÎÆ´2»\x0011èÄ\x0018R<@\x0011IIâzì\x000c¢LiÍ\x0018\x0002¶íéêÕrÉf¹Ä;OéäÚQ 
1Ê´¶¨\x0014ñïÃgyJÈâ\x0007ÁXàCÅ\x001c-ÓU\x000bvèÞ Ð\x0018ÊQdH\x0015Q&	øm[³©7)ý)4\x0012Ai
ò2õ\x001a\x0014E)òäð9BWHíÒ>m\x0003ëMG]\x0007Ö&\x0006½\x0008 @é)\x00081#ø1ÏÏW_óÃ\x001f<ãÞ\x001dÉ·¾~7^½ÃñíWÉ¤¥«/P¬\x0008¢\x0018\x0010!O"j&\x0005BE¬KK\x0018RÚR\x0008,é¼é¾Ö\x001dpv±áÅ¥§\x0003TÈq±'"Ïp"uùL§\x0013|¬ëºíÒð*í;\Üuì&·\x001aC²t\x000fýe±÷Ð5¸C\x0004Üt¨þ\x0007ú\x0013ýðý ±1$¤·B¦õv8?vF\x0011!À%¬Á:\x0005©Á\x0012RoéÐ	°i\x0003/¶¿ýÆQõÿ\x0013ÓúÊkw¹\x001bîÞ¿Dâw\x000fX1"E²;ù 	2ÇÉÉÐL+8\x001cyFãÞ5ØvKãÇÔ\x001dX!õ\x0008g5ý¶&ú56Ô¤,V\x0005\x001eë\x0011*ª^×+ÖþÅé\x001e_ULoÏQ\x0013ð¾¤(\x000e)í&h\x001avF)$¹JÝÖ+:$LD·L%X¶`<}ØòÓ\x001fý\x000bné9P§ÎÖ¼hHûà/éâÚ9®»5÷1ð.uû\x0006"^"Æ
ð¹ß"¶ý[{ ì\x001fu8ÿÉá¢²¼ù­ÃðÒYà³ç%'mÆ*ßg+3|&°YmDl
¾\x0011<zû\x0011YuD'¦ôBâm
 \x0018\x0011"F61ú	\x0018%ñÝmý	tß#n~@î>¦T\x000e>zJç\x0017»´CºK:«8:Þ'ªmZ£¬§qå`=¸\x0010QÐ÷énu½²D«8\x000b\x0016ë5¶Ïyz²¦Þ\x001að±ÑH'ùèý'|¨N\x0008W°çJ°Nô,Òæ¯°ÿÒUo¢ô\x0018\x0017»Ô»À÷\x001fÿîKÄt¯\x0013qDºD¯\x0000²xÁvõSÚö\x0017L&OÉ²wâ
º\x0000>¨ô@\x001d"ãrB«*.\x0008ñXx6Px1ãì²!æ
Ûº`y¶Å4\x000e\x001d\x0002[\x0017°hVàÓ½±ó\x001eå4]\x000bR£ÍQ¹Gp-ëUGGNÎZ|\x0007e©1Âv\x001d«\x0016ïä<|mçgKÎ/Zt\\x0000=4ÖÒØïqû¾àüYËúú\x0019yvB\x0011`.Ao-aqÁöÎ¯ð£ï¿O{õ9\x000f(Ñ\x0011ãÕÒ§g»e2Q%Ù\x001b\x0017\x0018\x0013\x0008XR²0ãârÉÑmÁõzIv²e¾Wg¾_\x0011\x0002Ì§ðÒ}è¶\x0011àòyÏñ½
]Õ`ñ	4§\x001dú|IÄQ5µ­Y/=¿û»%ï¼ó\x0006-ÛÍcDèðÛnc\x0018Kd2ßËùÑ³\.#\x001eãÄ"ÂTÄµgo\x0002m\x0007×«ðï\x001d\x000fÓëøø®mØ®\x0017ìÏ'h%Y^_rçö\x0011o¿õ:ÿìý¯Ø®ãßÿ\x001eo¾ù&RJ\x000e\x000f\x000f°¶K½cRpK\x001dÑ4\x0019Þ;òÜPUÕ\x0006=çâüj<ãÎí»]ðìé\x000bög3ú®gTG\x0015ÛíO?Ys}uÉt>'jÎ.){wï³Z­È´AH¨ªã;·i««sNOOÁS*lç¹¸¸@ Ð"c³Ù¦(\x0012ç\x0012\x0016Ô9Çx4N	¡ G\x0008I^ñQ°Z7D¥ÉÊÔ%­l ªdÚÑ\x0002|°xÛa»ùÞ\x0003êí\x001ae4ËeÃ\x001füËÿ¯ýÜéeºÞaTN\x000c\x0012%S×ýû/ñ\x001f|årÉt:&&ï?Ea°®C©È'¼Ï÷þí\x000fù'ÿø\x001f	Y\x0011¾ÇÇ§_<ák_{[\x0007÷ùô\x0013¢×<zpÄÏ\x001eÿýý}6
\x0000¯¾ú*¯¿þ:ºtÖë5ÛíårI\x00100\x001axøðe¤TXëhî/!\x0004ÌfcÖë%ggk³H¥Ø¬k\x0010"%GkÒ]\x001aîÂð\\x0001(<­\x000f4Û\x0016-\x0015Fª¡'|Ãd2aÓvø¨°Ab£FÛ÷g(-Ð¤~åýôô¶e¹­yëø\x0011ßùîß¡±j6Á[Ïõâ«Ë/xåå{8kY¯\x001b\0|óÛßâ?ä\x0017\x001fü·ß~ëå9Bu¸~CØ:êÕ\x0006)\x001dm
ÁwCzU2\x0019|üÑ\x0010knßº
²å`ÿ£[÷øæ7ïrzúËÅ\x0005gçgÜ»wÛ·î$ãç ºl-Í¶æbqÅßúõ_ÃÈªéX÷×lÛíé\x0019R\x001bÜÙ%¯¿þ\x0006³é\x001eR¦Î²¬¨\x000böfc~õ×¾Ã/~ñwßý&~ú\x0019£ñºµ ¤a³iX¯Ò¶¼º¼NÃ±\x0000eYÑgÏ³¿¿ÏÕÕù|\x000e!²?3í±¸^°°Çùù9o¿õ\x0016Iê\x001c:99a»Ý$$i\x0008¥Q&¹ýÔì\x001f\x001c1Í¹¾^ðÞ/ÞÇä\x0005Æ\x0018Æ³\x0019.F>øà}¤\x0016¼ñæ¼Ó÷,/	\x0011\x000e\x0010\x0008\x0016\x0005½ë1&#DÏl<FõGõ¿üºuvvFYLg3Â ÀÛº6\x001bÚ¶\x0019Pd¶«©7\x001bº®eµZÑuM2­Åa\x0010¯\x000c}g\x0013\x001d%WdY(\x0015¹1Ø>6ãp¯)¥¤³6\x000bRãC©ÔyË,/Ùnk¦¥Þv(É\x000b\x0018O
ª*\x0019
²ªB|4\x0002)Í\x0016ÀE(\x0001%±1\x0010¡~!\x0014óù(`½Þp~q6à\x0011SB@é$ ®7k´Qì©¢J"]^\x0014\x0008îñ½u8pdR¥gÑ\x001d.°ïû*¥ÔÍ×½÷ôM÷.Í»D\x000b\x0010¬¥ë;2-©Ìh¦fDVTÜºu;wî°¿¿OYiè:\x000c§uÑ;Û¶\x0004ïÑJe9\x0007·Íö\x0012ÊôôgÏÒÔ=×5uÓ\x0012Àä\x0005*0t)%aHJé¾?H×{¼ë\x0006¤ 7ªì0[Éf½ SÉ°áEºÁg\x001c¿ô(6½ÅYKßv\lVÐ £ÅèôyýÐß\x001d§\x001cÈå¦åöí»<þùû<zõu¾ó«ïruyÆåå%¼õæ×ø¿÷øà\x000fØß?ÀyÏùÅ\x0005Ï?ã·_ãÃOßçÖÁ\x0011ËKn\x001fÞ":A×8^{ô\x0006&ÏX¬WD\x0019øäýÏ(fÃ[ûøÐ\x0011UÀ\x0007GYøèÉË\x000cë;..ÏÈt\x0012©c.\x0019f3²Ì`Û¦Ak6\x0006¡$\x0001O1.h\x001de^ñ§ÿæÏøÿ÷îÍX.¯9??eýá\x0007|ã¯³7q].iÛÞZÒ\x001c\x001dÝF\x0018È\x000b°»\x0012î\x001eßçòÅéèw¿ý6WË\x0005ëî¶±l6-Õ8Ggy2f\x001aÉáÅÓg<xù\x00116X.®\x001aÖë
³ÉlV cÆg',®\x001b¤R\x0010\x0010Q#¤FÀKÇ/!D¤í[zÛðàÁ]^{ó!\x0017ý)±÷Æ\x0015u»A)ÒY.ÑH¤TÔë³Ë3²Ê$²R\x001cìïÓljúmÇùé)§/N¦yAÝY¶£w\x001deYþÒkÖË¯[GD\x0008gJ)¤ÖD\x0010ü&ËhmC\x0002$#Dßõxç\x0010.Ü`\x000bcl·[º¡L$¼»A("óÌ Äv=A¼\x00088tå9\x0002#J+OµPÎ\x0007âðþ¬³dRÝ`\x000ecHîÞ´{	5à*½§TôÎÒÛ\x001e\x001d!W*á¥$'|ºm¸\\\x0011Ú®i8Ü£]`oÎ6Ø´öiºïùÁÏ~Æïþß Ð\x0002£%U5bq½f^Î¨fÝ[pÃ¢âáÁ\x0001\x0001O~NÝ÷0ôÍG\x0011\x0012òÔYÐ)9&2s=ëå5¢s(/\x0018\x0015q\x000el\x0014Ö[´<7¤j\x0012ÖA¥ð.`­K="ÍùÒ,Pf¶i¾±»-!\x000e=Ñ\x001e©|\x0012\x0004.Bç<\x0001@\x001aA\x001087Ì\x0011"ú¶Ö½¥·Þyú¾#S\x0005mßqzvÆt6åÁ£\x0007Æc>þø#Öë5U5¢®k\x0004)¹¯µ¾QH)©c8Î %DµÖ\x0014eysÍ«ª
5$C×ëõW(u©wü\x0006WZ7bãNL,«
d$ìmÏùÅ\x0005ÈSg\x0000\x0000 \x0000IDATÎ9¬µ\_]%2!\x001b	't|"ÐYFQ\x0014¦`TM(óLg\x0018ñqèri\x001e\x0014û\x001e©\x0014£Ñª(ÉµÁ;G×u\x0004ýåûÝ=/ïDÎ]Z\x0010¸\x0011\x000eý¿#\x001eîR{JJÁHW\x0014\x0005\x0012AÛ¶D\x001fX/ômë-]×¥Ùóì\x0010äA$z\x0011\x0002¤":
§H×YöMQ\x0014\x001c\x001c\x001c\x0010B¸é\x0008íû\x001eút/á\J0Jð£J¦ô Îé9JuÉì\x0019Ò\x0019\x0011èlsmÏ3úä%\x0012\x0015%±\x000fø>¢<\x0014R&H\x001cf5ô¹)\x0006"CÚ
ªÀ¤G\x00076@Ó&wßhlP:âCÑ2\x00012fJÅaã~9¼H\\x0011y#úýû/Á ¡1$«HÖa1¸ð(H¸²\x0000Ê\x0005\\x001fqÀ¶~\x0013°«\x0000
ø\x0006º:P£XIÉs×qÖY¤;B1Ñ(,"$CíQÒwAA\x0018¶K\x0012\x0004Ã"ýY\x000cBÁ\x0012r\x0010FD"ïÄ\x001b±\x0013K@ÝD]Óàºì´pD¿J*V KP\x000b¤Û\x0012å\x0015BÜ"\x001bjÑX\x0004i±hOjÎ¿XQ_HÜ6§ÞX\CQB5Mý2Zw¸88\x0015nP©2¥\x0004M\x0018\x0008nÐÊ\x0008\x000eCç Hâ\x0011H#0F\x0017\x001aYèKdH\x000c\x0002¡TéÃG0*¤\x001c\x001cü
"Xpu Þ8ÚFâ­@Ò\x0004ÑËHy´p)Í&Òqå r(
A+t.P&\x0006¥SêÁ/\x000bUëc}\x0019Y<´Ð¸Hî\x001d¥\x001c¦²M	Á\x0004J¹ë¨\x0014\x0010Aý0ÜNÃßÝ{7È)A(
ËN\x0018÷\x0008\x0002Z¤Ø¿:p6àEê\x0000p»\x0004aÜ
ûüòçA\x0014T:
øÚ	pñ¯bÀóí\x0004KÄ Ò\x0013e3¨à\x0003.®ïèÕ\x0006©NQmÜÓ×_\x0010m\x0006)ìð3K®¯ÿ?ÊÞì×²+¿ïû¬ag>÷Þº5E\x0016ÉfìZJÇ­H²%Er\x001cÃ\x001cäÁ@\x0007\x0007Hü\x0011±ó\x0014\x0004É×<Ø`YR«\x0015£Õ¢Ô\x0013»ÙÍ&k`
¬ª;ß3îy
yXû^vÃ6@\x001fà\x0002,\x0014Q8÷½Ö^û÷ý~?_\x001eÞ\x000bûD:ÐèDC¤z×éñ»a]H\x001d\x000e\x000b2\x0002©ýezP¨Ï¯\x0010v¦Ât
U]0Å\x0014Ó\x0019Ú¦aÃ®3XU
§çç\x001e\x001ca¶kFÃ\x0011Wçû	Mm(¶¡\x0013ªÞ\x0014´M×cV	å¯²C*¸rêÝºÿNG¡oÎÂ¶¬ËsF.¥íJð\x0016%$\x0008-B\x001f\x0017Mø­ï]"\x0008±J!À{³<K\x0019ïí1\x0007\x0001ÁÜ;\x001dC2Ê]\x001a\x000e\\x001fá¾0%x¡p\x0004\x0001Òõ8æ´\x000b"GÛ\x0014,ÎY,O"Íl6f6qÖ6¸.8ÅtßQW\x0015D,\x001f dÉÁñ1eqÆýÇ\x000f0%£cÿÊ\x0000©%ÛºCxÍvÛR5
M\x0003I²­"t²KÓÅx\x0011¡'V
h\x0019F-±«ì\x001aØÒU\x0015çK8^ÒñÄ ²\x001c¯DÀ³``	ë«/çF\x0004\x0003\x0008
á$BôõEqvÓ\x0019Vç\x000bÍª,\x0011Î\x0011ë(\x000c±û§ï\x001da3\x0016!U\wgÄQJÛz7`[TD*&R1±ÔáP(<^´ak[óh\x001fêð=ÎÑ²¨»×;´¶Ä:¾Ä-\x0004×\x0012X+P*\x0006÷f¶ªéXo\x000cem©ê\x0016GFý=U\x0019\x001aYÒº
m
P$>\x0007\x0001>ï8yqÈ\x000fÞ;dw\x0002/Ý\x0018ðúÝ\x0011W÷úû°(\x0011ºA¼ñH/I´D[K]9:Û\x0011Å1ÎY´EK]DÄÑ\x0015~ö`Íw¾óº;¬oÉRÅ8ÑªaÛt\x000c\x0006\x0019Î{\x0016%­u´½ÛÐX\x001fÏÖ÷\x0018d\x0011ö"\x0011®ï_\x0014Ð\x000cMðÿ|"¼@:|v6¸H\x001b>k\x0018öß\x000bqÑú=\x0006AkMÆ\x0008\x0017P²Þ\x0005\x001c°wá³5Î§	*\x00158\x0013\Qq\x0012£ª°<¾ÿy4ÿÜ{ÖÅáóßùw\x0017\x001b<AØ·ØK\x0003UppJ&àÆ°b\x0018m¨ÖçÔë\x0013¶.FÈØÖtÅ¢ièb[v$QS27!\x0016\x0013\x0010Á-\x001e)ñ\x0011VxÖÍÕùMD±Çxw
:§é\x0006à\x0012\x0011/$c\x001f:R­\x000fÝ®:°¶®d\x001c\x000bÄú1Ò\x001fiÅîÄñóòÇ,Ìc¦;P¶e\x0019¡O\x000c>û	¹û\x001aTå£Å\x0003¹#ºên}Âº;ÃO57¯¿E²÷
¶[¯YÖëlàzÅÙò¯Í\x001f©z{g/ñ h©mÒ»¡Oº\x0005íÇdc2\x001aáUDU\x0000\x0010÷\x001fyÜ\x001b\x000cL@U*\x0007.\x0018¤µË
®X¹\x0011\x0002E\x0000Àõ÷Ø¦.iÍ}pÏAT\x000cã\x000eoC9¹\x0016\x0006ÛK×Zè:÷\x001aDJYT«
ó«0Úq¾\x001csp¾¡Õc´Ü \x0012AÝ6¬K(AoAw%\x0003	n,Q³Ø{å÷oâºV#\x0013\x001bfÿ\x0019R\Ê_¾¿
ßÛ¼À\x000b 
èsß\x0012»\x0012ïÑm!£\x0013¢AgDã2ºÈ¢¢\x0014ãRãÛÔÛï1\x001bÆ¸¸é6t\x0014³ÙÖ|òø\x0014gcJ1VÙcQxº¶£«;-¨{{Ñ\x0005Ñu6ÏÐQW\x0002
®«£XÎ#|ëY.V\x0000AdÝ»Î\x0017ßü;ìß~ÂÃ§\x001fðìñ\x0001m\x0001¾\x000e\x0006¶ÍbËjõm°1¹ïG¹\x0011+Ewæ¨7¬Êá£§Ìv I\x0008,=Ä:Ðô§sÍÎî\x0018­6diÅõ\x001bðÒK»L¦\x0003Þÿà9ã±"JuÀáÄ#Nñ¢c2WHÖÔ\x001dLr¸2\x0011ëyT©ÅË\x00145ZÑÄ-g'\x001diÔa\x0005L{üó¯~sùxá#"7çøð½yÊ(M0u7\x001d:Ì®í|ÁO~Ú1Û½+\x001d\x0002V'\x001e\x00077r\x0012G@Gõ\x001f@FþÁ÷¿R\x0019y\x001e±3¦)ÓéG\x001fóåwÞá­·ßáàà>ú9qRÕ%GÇ,kÒ,¢(Kþã¿ý
\x001e=~ÄÙÙ\x0019J\x0014G¦ì_ÛãéóÐÿ<L\x0011´a¹XîÇR\x0014K\x001eÞ¿Ç;/#\x0005|ðÁ\x0007Üyõ5î\x001dÝçÇïÿ_zñ(¤§wwæüöoý&å\x0019ÛíuþÕ\x001fý\x0011×n\¥m\x001aæ³+(©Læ`\x0005×®]çìô\x001co,Ûmð\x001eÞ~/ÖI5ª*(\x0006ï¡1\x0016\x0015eÌv\x0004£YJ>i\x000f\x001bSãlË \x0018\x000cb²D³Únðç{ßÿ\x0011qòÛ¿ý;x¯Ð*
Ï
=nJkEÓ´Ü¹s\x0007\x000f\x001eð«_ÿ[Ôu÷ÑhÀby\x000e¢â»õ\x0017¼ûµ_ãÍ×¾Êæ|Å iÛ-§ç\x000c\x0007#î¼t'qvºäåï0\x0018\x000c\x0010B°··Ç³gÏØÛÛc±Xðá\x001fþ;\JÉ|>gº3'Is6-çç0`ÐQè\x0018´\x001dÖ\x001a\x000e\x000e\x000eX®Î\x0019\x000es¢XÓ\x001a"êºÆ4\x0001sd\\x0018ÊI©É²ÑhÒÍfËª,¨[Kå,NÏp]GU¬¹uû:ÖX&³\x0019O_qçî\x001bä£9­1Ja}Æ2Êb~üï1Î¤æ7~ã·°NôKÇ\x0017O\x0018¦
å¶\x0007·8[l¨jÁt~óuÍ\x0017Þ~{?¿ÇÉÑcâÈ£\CW¬\x0010Fb
RZ¼õ$\x0004\x000feÙàåÊî\x000eI²K6\x0010|òðg|óo¿MkÇ¬W\x001b~ô£\x001f1ß"çêÕ}ÚÖÎ¥lñ
\x0005%m×ñú\x0017Þd4Û¥3ºë°\x001e®\¿É'<BÐ2\x001eMpÎ±<?ã×ß$Rï|ç/¹wÿ>óÝ]~ïw~OîÌùùû÷?&3vç\x0001IýøÉSö÷¯ÓÔ¡7.Ïs¢(b:2Lxöé§¼öê]\x0016gçÔuÝ\x000f$a>ß¡X-ùÒ;ïðæoòã÷Èâì»wï\x0012%ívËþþ>W¯¾Ãýû÷©é|½½=væ{l6\x001b6
ÛmÉíÛ/!`¹\qãÆuNOOyñâ\x0005Wö¯òòÝ)«\x001a\x001d§¼ów9=9ç{ßÿ\x0001·n¿ÌéÙÑhÄK¯ÞåÉG\x001c\x001d\x001d\x0005EYpíú­ðÏ/\x0010>ûä!ûW®0Jbt¢ñ]EWW4åÕjÉr½¦ª*¬õ¡?ËAxÒ¨Ál\x0018\x0006ÖEÁj¹¦5\x001d::t\x0001¶Ö^R.¼\x0008)\x001bt´8ÍÈ³\x0001I\x0005¡Á\x00073gjºN².\x001a'\x000bT\x0014d\x0019ãzÆp4"I3¤ªÄ)I,5ÃlH3a­'$J	Q*A\x0008g\x001b"2L\x001d¦qH')aÅqx¦sºª\x0011$NJ¤Àç&\x001dÅè$AÅÁx*ñÄq\x0014ªz^Ó¶4m@§j\x001dÓ\x0019CU\x0005!Õ\x000b²\x0006EÆ}%D®\x0018\x000e\x0006LÇC¦ã!y1í1LÏæÆ#ò,'Nb¤=ÆP×5E±b[XcR¡ã$N\x0010@]·x\x00153ïqíV\x0007QÊÃ\x001fáÝ6¤¢â\x001e'«\x0002©G¨`æ06`UÛÖâ­Á[C¤%±
\x001dàÖ\x0018ÖuÔ¡²#\x001bL\x0019LÆ¼öÖ;ã°\x001c\x001eðìé#vg#6å<¤JàlKYWà!É&¤Y%EÈÉlHòÕ¯¾K\x0014)Þùò;ü¯ÿìñÖ[oñ\x000fÿá?àðà\x0019wïÜ"3¾ÿ\x001fògßú\x000b\x0006É'¼ NbÖ§\x0015ãÁõ²d2\x0018££Éx,NØ\x0014\x001büô:Q® v\x001c\x001c¾`¶7&Î(\x001d1È\x0007¬Ë\x0015WööX­V\x001c\x0010E	Óé\x000cP´ë4Íô\x0000k\x001dÑhHÛµt¦¦+\x000bbÐ¶5r\x0010ó?ú.¿ö·~ÒTx\x0001«³s>}òÝÝ\x0019£ÉåzAUlIó!gçGÜyùUt\x001cqv|F®\x0006Üÿð!/ß~\x001f¾ÿCÞúòÛü·ÿÍÿÀ¿üWÿ}ü\x0013Ú*B\x0002\x000c\x0015\x0006\x000eÇºjÈS6ëI>¥ÞTÐiN\x000e\x0016¬Ö[õ\x000cÆ3æ»)Åºb»*¨H*v÷wyíøéÏ>`±õÜxé\x001aÃqÆª9Gç\x0001gµ-·½Ù!$ç¤xç8_³]­UX×{Ó\x0019ÃÁ®nNñÉ'\x000fY1N´`S.\x0008PÕ\x000c\x00069£áðsïY·î¼Lã,uÛb¬\x000f/2 \x0002\x0015ý\x001c.PÎ\x0005ÃCSÕ()©mGW·¢Ek::kÐ8PZ!\x000cÄ"Âì!ÏrÒ(f6\x001aS7
'íÚ´H\x001dÄ!¡$RkVH­BR¸n1ù\x0001Ú¦%b¢(.]\x0017ê-¢8ôÏyOÀ'v!}¦²\x0008ã
I\x0012\x0013yAqº ³Q6\x0008xF \®h«³cb\x0001W§;Ì÷fÈ¦¤ê:Ã\x0011Q1îR\x001cñþ\x0007?å\x001b¿ò.QÎë7èêOØ®\x0016¤£	4
®*Ég:¥²-'ë\x0015Õ¶À\x0016'48è¼C*r\x001a)ÀØºÓÕ\x001am<{9{{WØ{\x000c\x0017ç,Ö\x000bÚ.tÙF¢®+ºÖ\x0012E\x0011º¢­\x001b¬q¨~æ\x0014DÝ¾·UÈ\x0010
È `èý}¤wxçBj±µHwñ\Jè\x001fõ\x001aï$RDDÚ#EÌEw_Ó\x0005¨5Ñáp\x0018Ò¡UÅáÑ	;Æ°\®0c8LBo­H\x0019êáÚÖçB\x001fR¡g/ÌÕº®c2ÉLfl«Õz1æ2±_7Íåõ|¿ì\x0011Îq\x001ccÊâ3èº½\x0014æ\x000b\x0015\x001cE]±Ùl¨ªb¹\x0006\x0013ÐÇ\x0010ð¥Îù>ÿ%bMääqJæÄQX¿Ò9<a\x001d+Õ±\x0019Ìd:åÊÎ.ZH¶«5+»$à±ÛË®EÝw\x0007_Ì.~~Ñ®¤D"U¨\x0000Èâ$Ì\x001d£°Fãþ\x001e"DÀõvÆbº0ß
Øó(¤A»æóÆb½C(I¬#t\x001a\x0005ã¡÷ÔmCG\x001b:t\x0007\x0003Fùmö¼\x00103e×¡¤'\x0012\x0011ÖdiF¬ux¦ïéÒ\x000bT\x00141\x001c\x000cÈz¬°q¡\x001ajS\x0014._ðA÷ÑhñNÑÕ%]å8
BÐaX\x0012E8QD@G cP\x000e\x001fÊ\x0003q8Zãñ
V	(/c@Ç8R}ÇïÅ\x0001ß\x000fq¹L[þ,ÿï\x0015\x0006/^¿ \x0014\x0002ó\x000bÊ	>ÄIÅ¨bÁ·¶¶öÔòÌS,\x0003NÒVÐ4°ÁpáYÙrT{\x0006
*!°}GäØw ÊþPØçC½ \x0017ú÷%>\x0013>\x0010ø\x0019Î-\x0014`ºKQÑ\x0018f?\x000cýèÿþÄ\x0012©\x0015H÷\x0015t\x0006íR\x0006\BøU[Ýâº\x0003<'ÐÒ®6\x001c?-8^QkêBÓuàT!\x001dÃ`¬µÇu\x0006ÛG\x0017Ýªÿ	bî»QDDèÑ %û\x001e9\x0015It,Ñ©$J¢Ð/¨{K\x000bT\x001eïU\x0010\x001aûÔHxH¦W%Âk¼SØÆ±YU,ªñtÆãm\x0008*Æ±d0bÒm\x0010c\x001dD\x001a\x0014ò¡ Ê$i\x0016\x0011¥
zT\x0002qª\x0002öR\x00110R:ÁØ¥ìÝït=nØ\x001e\x0018\x001a<MÏÒÊ TR\x0010KG\x000bÑ\x000f´¡ºè¿¯a¯ìq½\x0008.}(ª
lY¼wHï\x0011\x0004d\x0011Bj\x001c\x0002ãL\x0018¢u\x000ek>C~&ªó\x0019>´\x000fáº\x0001\x0015yt$QÊ#EpÀ_¦
/ÿqyc
Ým&d%\x0008iB£¤G«\x000eÏ9®H5@ú3bå1$Ó1¶m¡<øèÕ\x0002R-Èó\x0004\x001d+.;Ñ%½ðx!|\x0013RoJ5#}ýüiº)q¦¥ªK\x0010áAÀú14]KS-5ÝX²)[\x0016\x0007',^<ggÜºv\x0005\x0015G4Û
®V¸N£d\x0014¡oÐ]B&Ã:MRt]IÓ\x0006¾´PqØ'UÜ\x000fZ-Öv8§\x0004Ôª\x0017\x0012á%àÒrê3ä­Å!B)Ý#\\x000cMï6VYL¦¼öê\x001b¤IFÝ4l7k¬7XÓÐvmÀ¨\x0018\x00136Þ\x00041Pu\x0015r²\x0001[xá\x00062¦#ÒÙl\x0010ÕzÉ\x0017\¿±Ç8\x001b!­Á4A(Ió\x0008­4^+ªº¡,Ï9<\²3¨º,MÈÇ
\x00119ªº¢XIL'Ùnj\£SÉ|ï\x0016gG)ëCáÑI\x0010®ãÔÑ2*f©!UP\x0014r¥8?q¬$*µ8ÙÊVÆ´}ÎÅ\x0013Ö\x0010\x0012)4Î\x0014!ýÃ·Dui\x001duUQ¬·¬ÎÎi6t\x0003©°f\x0018çq=âÖ_$kµÂÓÑ\x0019÷2\x001c¦¥	ßòè$#\x0011\x0019ÚFh§q}Wlí:\x001a\x001b\x000c\x0016Ê+tÄN` í\x0004mmÂ;\x0011ZK¢HÄ	Q"¼
iðFF!ÍÔÞ\x0001£î iÃÞÝ\x001a¡CJ*\x000cÑ{g_g-e[E6ìÉ6ø
\x000c\x0016xéèLA[w(Ñ\x000eì|ï\x0004ÂI|ç\x0002:É
\x0008\x000b$Á5]5\x0006Y;¤OùàýgüÉ_Ö¼XÜÍI2P	JYLSÓÔALM³¢*)Ê\x0006`0ÊÙlêpxS!)m½£íl@÷¯\x000b¡ï"NøK)¨Ï\x00115ý}4\x0004¬Ý/\x001cö,R\x0005ôÅâ´@öh(Ùw²x\x0004^h\x001aÓ\x0012ã©mÀ\x0013E\x0004ÔR\x0007cYt,Î{Ï\x000bóÈ¿ýR}"> ¨éÓè\x0016)-Ê6äªæJ²áú\x0001Rû\x0013:\x0001ÞoÍ	\x001b\x0016~ICè(\x001aBÚ!¢\x0008í3¤5tõm§©#K#ò¬ÃëÂ)Ê\x0019E³Ãò|V	\x0004£À¨X8R0W\x001d\x0003Ñáð\x0014JRø86d]>ãÑ?'Î,f+`G2Õ\x0007\x001e@\x0011\x000bºpJ%³¤=E\x0015m-\x0019<~N\x001f±Xÿ1#m(~ÄÕgxmD²\x0005ß,Qã)¶hïì#|õ	zE<ìÈxþÁê\x0016Çëopz®XE\x000bSâAB
:@v.ôg÷®ÆÄ*>ugC|Ö+D\x001c3ïÓÊ]t1%r§äª`åt*$JÛ®¥k \x0005Zw8¿¢³àZ\x0011ÎNR#¤5-R\x0006bµ\x0002ï4ÆÀfí \x001a²8((»-ù\x0017xã_åÅ'¼tcHb\x000bü®9ÅºDåÙ*È×Þ¹å\x001c,Q>¡\x0015C6& U>3\x0002³æ/¾Â%^D8¡\x0011²E\x000b´3"w
!"´x5-¢Û%ÏöèäU÷Haº!itm5Ä
\x0006hZ4\x001eça\x0010%«uM\x001cMpÖ\x000c+n¼¤PkOÙf-:NÎZd$h½Ã
\x0018
STSnkÖëOÅÚ-N\x0018¬I>¢®-çça&ð^rt\x0006ÇÇ»ÈlÂkw¯pãÆÏØ\x001eòá\x000e¨\x000bIH<\x0006©ZS¸Úâ\x001aÁd0\x0002\x001a'\x001bþÍó÷8>jä4ò¸6tÄ@¦\x0005±½ÙÉHQUK"UsózÄ+·o0Ú½Å§þ?Hpóö
\x000e\x000f\x000f¸wI±Y°¿ðæCnÞJU\x0017Ö*â$' r¼ñÆ\x001cÆÝãÅ'+ÒH³(*\x001a£ô\x0015>zÚñÚKs\x000cg\x0014O\x0005l¥a~C3\x001dMXWglÊS³\x0011Wn\åþ£CZ\x0007Ä9V	[Ü¶Ã\x0011ú¤êø\x000f\x0001#ñ­×\x0018\x000c2ðÞ\x0012'\x0002c\x001a\x0016S\x000e\x000fS7%<çî«¯RßlùøÁÇ\x0008)xõî+<~üÕjÅþþ>eUrzzÊx<&5'''(­Iª[·nqxpÌáÑ!·oÞF£Íæ,ÎÏùw¿Æ\x0007\x001fszrÂl:fº3'õðü¯~åk,Î!ùf-uYòàÁG¤qÄo¾Îx4âÝw¿Jm;¼øÑh\x0014L`^°^­Éó\x0001Þ\x0005ô]Y\x001c2\x0018æ\¿v\x0015!%ÛÎ2ÍðÞ³^¯\x0001Ð:Áöéî(É\x0011ÊR\x0016+Î\x0016K\gq]\x00108ÔÅãI2{÷îó_þ\x0017ÿ\x0008­S	Æ°8Ò½[Ú2N(Ê5;;s\x001e<øçÏ?eïJp
Õ$øñOþÅòÿîþ8:\3ÍÆ¬/Øn\x0017ìíÍØßÝãéã\x0017\x0008RÞ}÷ë'\x0019ÿ÷ÿõÏùûï÷/»Ãööö\x0018F¤iÊùù9ÛíñxÌÞÞ\x001eyã¥¤i:6-B\x0008f³yè)1¢,"EÆÜ\x0018^g0Ì8;;c<\x001eÓv\x0016c\x001dÆÖdyNå$IF\x0014ÇÁ
¾\±Ùl\x001bZE,ù\x000eW¯_gu~ÆÑást\x0012ógßúSvöö]}[/ß%ÎF\x0008\x001fQnÖd	ÄRðüñc\x0016Ç§\x0008­íßfwç*ÏV$QÄáóçL\x0003LuÆ(õ¬\x0017ÇÔUG\x001c\x000fÍoqpxÂhpóö5\x001eü3¾øêmVg\x0007¸®ãøhÉz»f<Î\x0013\x001a
\x0008Ú¶âÑÇìÌgtäälE
xñü£Ó\x0017ìîí2M©ê¢Øð+¿ò./ßºpÁÜöþ÷¾O\x001c%l¶[®E\x0011G§çì^¹\x0014-ÆtLçsÆç\x000b\x0006!ï~å]êmA$ÌÆc¾û¿äôô»¯¾ÂÁÁS¾ÿýïñâàS\x000e\x000eNùú×\x0015\x0011iªÊôi\x0003\x001fø­agg8\x000eBÎ`0èR1;;;lVa¨w÷î]={ÆîtÆÙÑ!?úá\x000f9<8àÅgüÁïÿ>?ýéOyqøããc\x0010¼ÿþû¬×kfó9eYòÞ{ïÑÔ\x001dW®\a<\x001e³\®¹yó&·oßf±XòèÑcÞ~ûm¾ô¥/ñý\x001fü\x001füè}Þ~ûKlÅ'O\x0018OfÜ¼ý
÷\x001f>d2°XmøäñS~ý×¿ÎÍ[·ùÞ\x000fþ\x0006!á'ü¯yãÍ·(ÏßçE[\x0011ãA¶5Þ\x001brÅjuÎùâÅjMÕY\x00088Ö,IQ2"Ë\x0007DÃ	Ù goñ`H]\x0014\x001c\x001d\x001d±^¯iÛP`¬¥ë*|\x0017Î
ug0ÎÓ6>t49V\x0019i2DzM]6(éèÚº­p®EjOgklcñ[°Â¨Ü \x001a-·\x0001ýèl0b[â}G¶¿G\x0014gx\x000bUÉj\x0015ÖëñM\x0019ðlÃ8B	MÔ÷¤u]GSD2Æ6\x001e\x0013\x001bâ4\x000b=G:z\x000e\x0003ï$\x0018á9°ªMóDÇ¨8£ëZªB¡¤\x0008(~©\x0003PiÒ8\x000c4§³1£Ñ(ô&IÅ|:½DÑi-ÁP
à\x001c®«)Ö\x000bÎ\x0017KÎ+V«uèMO\x0012ò<g\x000fQ*&Nb¦ó+\x0008
'()yñì\x0019eU ¥$M\x0013T¤ÐQ«\x0018\x001bÐREÈ(%4Ø6\x0010§úNÊmQ "Å¦¬H\x0007#N%_ûõ¯p¶\#uDÓ\x001c<g6\x001fprôQªÉã\x0008åan±¬\x0019\x000eg\x0018\x000f"\x001e¢\x0001JÄÇ_|ûÛüá\x001fþ!Þ\x001a^yõ
þ÷ÿãsóÖËüòßóñ?ag2âÖ}þÍ¿ùKþâ[Ê \x001ehÁ¶l(V
Í¦c­\x000bH\x0007\x0011.ÏØNO'!õ)\x001c\x0003r6ÕÎ\x0019ñ\x0014éb\x001e?xÄë_|\x0015ë\x001b2ÕR´\x001bf1'Íª.°çÝÝk(\x0019Ñµ$\x000eµ2N\x0007D1Îi²>\x0018`#Mg[\x001c?æÍî-F;SFù¡\x0008HÐÙlÄrÑØÕzÅl6ãäøÙloÜ¡,+<yDÆÜ¹sñ/ÿ_þ·ßý?ùæ7~\x000f~zz³ÁV+FùxÊx¸ÃGO½¤«\x0005ÕÊ0N¶eíkV«\x0015E}B\x0016\x000f¸±{/ÿêWpÖóó\x000f?dw>åé§\x000f¹v{éÞd\x0008µ\\x0007ó}Û\x000fØe³ 	\x0001\x0019g\x001cåÓÓS&\x0011£|\x0018Î\x000b^`jC¹©øèç\x001f"¼g2 ¢¨¶eÁ ¸²;"Khõù\x0013ESc	Æ\x0003\x0017Ò7Ø6û±\x000evQQDøok-R)â(
ýgx4AF\x0011²ïi¬ÁY\x0013pºiB¤\x0003B?KRb\x001d1Î¸qí\x001a<¦«\x001b\x001aÓêÉVIHp\x0006\x0003´%Bô\x00045ÔªO0\x0019:¤}E\x001aôÞ\x000e\x0007Ð#\x0019[ïè	T§#êß{½.pMÃ(NÆòäGX,ÊyR©¹yõ\x001amÓ0\x000c889â|»&\x001aääùýÝ}N\x001e\x00101¢âÊÞuO\x000eààm]\x0008IÝV4mEÓ\x0014\x0010)iDhYÊ²mÁJ:ç/I\x0008ÎY¼q\x0008:JWPdN0M2ÒX'xd\x0011£QÂÉñ!mÛ)cª¤k Mô\x0002R1RKÚ.\x0018±ñ>&|?ööýçèµÏ´\x000ekCHDØÐ³%@ùõN 
(i\x0011ÄØ¶3Ô¡óXGäÃ!é(\x000eF½G\x001fÓ´
ÓÙÅâóó\x0005IRWm/\x0004úK¡ì")¾Ýn©ªê2Me\x0019Ö;\x0006yÎd2¹$Sh­L&´mKUUIº(Â\x0019p±\x0000\x0008¥ÖÑu\x001dãqè^-ËÍfÃb± i\x001alÝ\x0010_\x0010Mû\x0011Q\x0000\x0000 \x0000IDAT¤¼\x0014B*0ÔB¯°ÂÛ\x0010\x0010ÑBø,4\x0011°¡a*ïúÇ_Î\x0011=¾ÓÕeÚô×í xÑ¾\x0010\x0007/:\x0007µ
\x0008bz½$h:!¤b­íû${1¿\x001fÞG=¶SII¦¡7´\x000bí%¢\x0015\x0019Ö¶u B\x001aQ+\x0015:Ü\x0007áû@\x0008VË%q`¬
¦Ï¤ïy¢¨'Sªàw\x000eg\x0002åDhpÁ ì¬Å^´¾ø=ú\x0014p¢S´a0fkkB5\¤ÁIN\x0013'¡c*É\x0014*òD)=\x0016Ð¡SûäK«°¢ÚT¥£´\x0016é=4Æ«\x0014\x0008I!zlCpO\x0014\x0008ý&¬\x0018\x0004Þ_L6za£wZ^È\x0008³¶\x0010-¸ìTò>ô\x0014:G\x0010
­Nà\x001aè¶í¹§ZÛi\x0015W¬;ÇqÓqØzÎ	\x0001½F(Òa£ö\x0017ZG\x0018îsÁ@»\x0014\x0007/Vô/¿'Ä\x0005ÎÑ^üZ!ù%]\x0000»ÀJ\x0002t®O<ø\x001eCy\x0019ã\x0013X¿Eø\x0016h\x0011\x0012"\x0011¡UÀv¶Bv\x0016ß-\x0011æ\x00088Ç7[ê³õQIyn©6º
ï]öÊ\x0012HSB`\x001aB7_/ànJ\x0001:\x0008*\x000eâBz0"$NêP|«C\x000f¡\x0015*}¢P~\x0016¤S½ (â *"Áø ´©ÅB\x0013n0¤^z\x0005t­\x0008Üe\x001b®Ñ4I¦0®FGYp\x001cC:D9Ä@ç\x00028H\x001c$ \x0006(
bfèvóÁ).\x0015Â)ÒQÎ`XóB¯)Î\x000ce»!×\x0016%]Àï*Ùc1/f\x00032VpÀ\x0008ªâ"iªD\x001e=\x0007\.F»\x0014C\x001fxFì<]í0&lÐ"T_¢|\x0012\x0013\x0002'\x0003ÒH
\x0017\x0012/\x0014BõÂ®â\x0017Dx÷KCÂK\x0001;¬¢~!ùËÐc¸´\x001dÂwàKLwHg\x0017Dn\x0013\x000b´\x0008n\x0008Rï:ºÂóì¡CZH\x0013Éh\x0012
=^ØÏpý¥\x001cv!\x0011°ÅRôÉÑ^\x0018ÿ÷\x001cþ]¯¶iú-ð
%bxg0¶¡é6Tí®+ÉùxÆþè\x000eþÖu¦IÂs¶Z§p5\x001eÐ®-)Ë
]×Ð´uÀBÈ#\x0015\x001c\x001f\x001d±-J\x001a¢EÏÕ\x0015ap\x0003I¢\x0018é-­jqÃX\x000e!C\x0004=ìy\x0006ßã\¥\x0012=w<\ÇÎC±ÙÐ5;ã«¼þú\x001bÌwvY-\x0007t¶¡,7,WÞm\x0012Nx  t¥½#Éc­ÃT5]K]w$fÿ\x001aãñóóS\x000fxåö
\x0006J±|q÷°3\x001aÒ
ÁùfÍº^2\x0018ïªij4A¢I"8>^±];\+\x0011.f4!UÇo¿Í`|G?d]\x000b\x0012¡ÈÈSN\x0015c-ÙÉ\x0014jñÖSUÕZ³\Ã¶NeMÑ¹ÐØï¥B]8«Â+B\x001e\x000bþ®ì\x0013Þ[ZÛ±]o8;]`Û\x0016%\x0005±R@pËh­©Â\x00054(\x0004ÌWè\x0016\x0001ë\x0015\x0006s\x0012OpV¥ZD\x0019HC\x001aÇ\x001e\x0015ë°&\x0008»ZJ\x0012¡I£D*\x001a<®u´Mµ\x001e­câ$êoà\x0011JÆx\x0014Æ\x0004¡Ìã(Ë\x000e©Bß­1á¦h¼À\x0012õÌ|\x0013ð6 b¥\x0011NÒ4\x0015ZÖ(\x0019\x0006\x0008BxîÞxû\x000b»Ü¾\x0016±3êH£\x001aWo\x0003:Üi;,]ß'\x001c\x000e	Ö\x001a%`\x0014uØ\x000bÚÒ1Í\x0007\x001eU¬¶LÆ\x0013ö¯Xl:ÊÆ±»3'5¢ÞàÚñ(¦tÍ¦¤é:¦³qè\x0007él°è»\x000b|8!\x000bÑKæÞôn¿J.6{}06Ø;Å/Üpùõ\x0019â"ü\x0008Deõ¤:\x0018\x0015i1Æ\x0006to\\x0010:â¢ßá¢Ð¶\x001d,BÚAAÁd¦C²ðs¾~1\x0015ù¯pðxk0Þô\x0006p®E¹LÕtÅL\x001c³ç\x001fàí\x0013LT\x0011e@gÑ4h_Sbi\x001bGë#\x0018àã\x001a+5ÆÅhñ-Ì\x0013O2R}\x0015Ä;Dú\x0015\²Kí2jiQ¦!Â!\x0018_2p\x0015cY²«[Æ¢ÄÉ²\x001c<ü\x0000¡V\y\x0002öSÜö;`Æh\x0006TMÅ\x0015ËN°YÂd.ØºbÛ1ØäåNÍùáÏÌ§dÛç§ßåYËs^Ù\x001dQ¬+\x000eï}ÈÎë·P \x0007¸&C¸\x0016-;¢aS\x001bü\x0018°5Ñà9{{[ªfløpõe÷²;åúK¯å\x0012SµHÑ¡¤Æ\x000bK@\x0008\x001b\x0004\x001a¡LÀÙ ;<Z\x000b\x0011­\x001aHP"Î4NvtÞ`EHd¸&ôôj
®\x0003ÑäDÂ¹ª7qáÌ'\x000cCÅº£®À)MSR«|'!\åj2dw_söøgÔ\x0006R\x00113t$\x0001\x00119FsÅk¯]åõ»
?ç|?å`eyx:¦æ:¦'O\tCü[/å°\x0008±2F¨\x0006éR£¸÷» ~
<ÆÔ^%Îr\x0014Y <Ø!U1ÂvszÉl,hÚ\x0005\x0008Ï,ÏYkp-(\x0015c«\x0016=W\x000csÏ´ÈV±2\x0016×	¬t®ÇØKE±*Ùnk: ¤Aé\x0016Ó±ó±¢*\x000cm\x0003DQÊ¦©xòÔ³såuv®Þd>mâH&hí(A*³
c,ÞuDy\x0013ºò,E\x0019\x001c©Q8\x0017¹Î£cI\x0016KR
ÚY¼©°M\x0015y\x000c«UG]nHê\x000eg ³\x001fþè>ÇÇ-ZASCSµÜº2ìFKb\x001b#Ñ\x0018\x001cJy¼Ô8\x0006DÒòÖ\x001b¯rczJgjþæÃçÔõº¾Cªöøù£\x0003vÆ´=%[N\x000c*¹zý&ÛzKÝ\x0016$¾`~}DÇ!Û\x0012Ê\x001aT2Âë-Û\x001a¼³$I\x0015Æ}~ðþ½$étsgO?eooeQsóÆ
mEU\x0006î¦(\x0018O&Ü½Ä\x0017¾ð\x0005>ýôUÖë5£ÑG\x001eóâÅ\x000bÆã!ÛmÁf\x0013\x0010'§gìË_¾ÃÑá\x0011§§§ìLç(¥Èó\x000f\x001frpxÀW¿úUvvftmËk¯Û%S>yøï=xÀÍë×ù{ðûÐÔ%ßþó?§®+þ£oü\x001aª)¹zõ\x001aÇ§'Ö2¬
Åºäèà( \x0006Ë¦i¨ÊÍjI:ÌYÎÙò¬?;÷CD\x0015Î{\x0005!×x\x0019äC$DF1AÎÉÙ!óéùÎ\x001aþôOÿnÝä;w8?\x000f"w\x0002klÀþ(¨Ê5i\x001cÓ¶
o}ñ-îÝû4\x0008\x0001Í?ú¯|å+H\x0011!|\x00141Ûõ(\x0012ìíÍÙn
Ê¢e»ih\x0017\x001cýè	¿û»¿Ë«¯Þå½¿~óós\x001e<x@Ó´h­¸yó&7nÜÀ{Ïjµ¢i\x001aZcX®Öìì^a>á}À$=yòë7®\x0012RV°X,8>9¤,J¤LÈ²!»{ûDqLÕÔx\x0017\x000cKÕzÃrµb±Zá½'Ò	U× tÌ|¾ÇÎlÂéÑ\x0011i3\x001ch²1üÚ\x0017ÞB§\x0003\x0016«5^e\x000c\x0003-PÞñ¿þ\x001b\x0006iÎ`8ÆXèÊDEÆ\x0011Wwç|üá=\x0003O±^1_EÆcOÎA(ÊªÄé$åää\x0019ÍjI&L'\x0003F!{WfÅ*kÃÃû÷£8N,\x001f\x001fa"Ë\x001fýÑ¿f2\x0017\x0007/¸uû
\x000f?úÙtJ×uüüÃ\x000fæ´UÃp4BxÇ7¿ùM\x001e<?À¶\x000et#¢,¥5kÏÎ\x0018%\x000f\x001f>@z\x0018f9ßúÓ?ãÆk¤IÂG\x001f}ÀõëW(«\x0012­\x0014où
t¢yúé\x000bÚæ³n (çt]G\x001cÇ|ùË_f2\x001eóÞ_½Ge|üñÇ¤qÂoþæÂ_ýÕ{¼õÅ·XR\x0015\x0005ñÞ\x001e>ù²ÚòÞ{ïñäé\x0013*8Õ¯]»Æ×¾ö\x0015îÝ»\x0017Î[/ñî×ýr\x0008êãñã'¼ñæ\x0017ØÏQ:BJÉã'O±Ö²ý\x001a×îÜæ£ï1Ì\x0019\x000e&lÊ²nxéÎ+dYÎ\x0017/ÕfËl>ã\x000fþÓ?àìôçÏxúø)Q>úÜûÖd2a0\x0018`áôü¢Ø²\¯9>;e¹-h¬CG)iõæõ\x0004!\x0014:Î\x0018O'\¿~oÝf4\x0018°Y.ÉÓÅù\x0019ÛªÀðÌaLK×T\x0001ÃÛZ:ë\x0001T\x0011ÃÁQþ0	USaéú!,DQÒ):\x0011R~k$¦1XgX6m\x0014d9Np9<ÝnWhé\x0011WöHt\x0004Îç^\x0013>:ÒäyNS(­Z¢´ì}uá\x000c\x001a\x0006ï;<¢¬P\x001bÕ\x001b¤\x001cq\x0012e\x0019Ãá($¢n\x001aªº¡nÚ4\x0013\x0002)\x0015Þ9ÆÑ0g>2\x0018\x000cI8¤Ä&OSò<#\x0013>e\x0001åèýeõb Ûu\x001deYÒ45ËågÏ³ÙltL\x000f\x0018Ç\x000c\x0006Cf³9ÓÉ,¹²·C,_#\x0013\x000e){ä©k-]k1Þà\x0008ÁiÄl:	\x00185ÓÒÖ%Ûµ¡*ÃP¼¨\x001b$c[üÆoþ\x001d:Ó¡g¹^ðÁOÌîÎõù\x0011Y\x001a¡z"1&\x000c¿}@\x0005\x001acÃ°:²\x0014åõvÃßý½ß
XW¥øÉ\x0007\x001fPU\x0015ÿø\x001fÿ<ö7n°eoýÉð½ï~¯¾õ\x0016Û¢¦n\x000c«mÃª(©«º®(·\x001dmSrmÿ
giÀþeYÊp0Æ\x0008Ë|wÎº\qxrÀ|oÆ \x001d±8]róÖ>Þt$:¡i*®î%TmÇáá\x0011Ç/ÏwAÊ0\x0013Ó\x001a¥$Á¢(°¾"À+±ô\x0012ÇÿïÛÎþ{ç\x000fsóöM>þÙOñ>c2±e¦µ\x0014EËj¹f8°Ùn¹yë6q±Ù®éºÓ³\x0005Å¶àþÓÿô_ÿWüÎßý\x001d¾õí?&Í%Î[Ãcù\x000cÓ:6]	æ\x0008-5\x0018I±)qÆ3ÈrÚ¦C8ÉáÑ	Ó%ÞÁ7¿ù
¢Xr¶8fY\x0012:ÑÒyCäÔ®Á4-i\x0010ë\x0018)\x0004¦íX.\x0016´uÃt4f2\x001a3È´MK$\x0015G/xxÿ!ÉEªU\x0008«%¦kz\x0011<bÍz]ô¹÷,\x0011E¤I-\x0010$ð`òVÈ0wÔ
ë\ \x0008©`½¨¢
îû\x00100ñD\x001c}²YH\x0015P·-m×1H3T\x0016°ÂyÕO\x001f=Áv\x0006zÁÊZ7"Ìì 3]\x001fãò}çªÅõX`Aoºì\x0013M\x001ezq^Ð:é{\x0010=\x001eßµ¡\x0007qS¡:Ëîln,'\x0007lK¶¡«jv¦\x0013Û
>2<yö\x0014\x0011G¤ã\x0011£á³SÖ«
iÓº5ÒEd1×¢(VMMÒ¾U"±UH
ÉHç)ÃaFT\x0016ÔÖ"TDÜ§\x0011\x000e¥k
ÒB¢"òÑùdÈ0ð¶Á;Åp¦;ø¶b³Z¤1<Å;Ëj»¡j \x0003G)M¢"lÝ!½í	¾7\x0003
\x0014/\x0004²Ç\x001b\x000b\x0011:aË²\x000cVç@|ô¡ÂÍ\x0018Ûwo\x0019±Ö\x0004¼mÓ´ýwfiM±MQPT%³9ic½§¨*:kÃ¬²?C\ £C× \x000e=\x0002:MÃü«iëÌóË=\x001b MÓË¾½¾¾(HÓªªhêÅbÑ÷Ç\x001e#¥¤,Kâ8¦(
\x0016Åå¿¥´F\x0018\x0013lÛÂ#\x00108ï0ÎQ·-ãáHÇø¾Q¢Bjð¢ÞÍ\x0005"íëe\x001cÍvC¤4nÔâ;\x000b>ô\x0006Ó\x000bR\x0006\x0014îÅg  ¢ËTn\x0010ÑdHôö´«®ëÂ¬Ê\x00074±µ\x0016!R
Ý\x000bæJªËO\x001cÅ\x0001U\x001b\x0005\x0001ÒtÝåéº6\x0001\x00108Â¹ J3¤8ïÙ\x0016\x0005uÕçp/·4
\x0001\x0016ijd\x0012]v\x0008×mH&â\\x0008:õÚi[j\x0017ª\x0000\x0008}\x0000y\x0011'IH(ãÑÖ(ªMDy.0EØ\x0007dâ@7èØ\x0013Ç\x0010¥\x000e	d\x000ej \x0012\x0008DäÑ±EG\x0002­Ã\x0010Ï[ËÌæl\x00175«3KÓ: #R\/"iu!4I¬aàg
Ð"\x0008\x0007\x0006\x0019¸>ÆÁöâ\?Ô}\x0012\x0004ÛÅlPû:ï\x0002ÊÉw 7\x001eWDtçíâ\x0010êuH\x000e-¶Î³è<¡²\x0017¶\x0016N6\x00057ó¦q
]\x0017ÒsaÅ\x0007w¸\x0016á\x0001O)H¦äe¡æ\x0005qBª ²¢\x0002öKÈ( Üe¹)A¾\x0012ýÆî<8N$¨\x0008§tÀU)bZ$ÖOÁ\x000eeÖ\x000eì1Ê/eMW\x0018Ü"¢9Y?/(Ð4ábL\x0013ö0Ì`w (Ê\x0016c"\ÏFÊr\x0010;d*QC%\x001e
T\x0012>\x0007-5RÆxbhðG\x000e%2áÔ\x0012¥5J¤S\x001e¯%.\x001ec!µ-±÷D.Áy1
"¶\x0018¿Fã(Î\x001dg÷ZÄVÓÖ¦¶8\x0007Ã`4R$QêÙsNöÁ¼L"ò\x00189rÄáS=*\x0005R\x000fC a\x0018¥ £À+¥#\x001a\x0019vsE>Î9ù¤àðÅ¹
Â	\x0012¥ÃI$m× µEÄ\x001e)/\x0006Å!ú-Â;s\x001dh\x0013ôOÕk²ÿs/.\x000b\x0007Z;LÛ"Øµ¡Û8ºuÄùRQ×Ø\x0006®·²Àüõ²%ö\x0010\x000bp
Ú(Á)Ó§\x001d\x0013à¢;MºÐ}°xaz7\x0006áBµ\x0008<²Ó@8ã\x0005JZºú\x001c/×(\x0019apZ\x000fZ\x000bºbEª\x0013Î_HNï{d©ÈÆd´´Á+âþ\x001dh\x0015*êÍ\x0001J c\x0017á\x0000¤µþÜ\x0007)l@¯ØÚáÛ\x0004Ì\x0008g5ÆVtjÍ¦®x¶\â½"Ò\x000bÊÍ\x0019ÁéxÈ#êªCXÓ¢¼$r$É\x0013M]¯hº®Qt]\x0010d¼u¼ùÖ]^\x001c<f<\x001aãL3-N´\x0018'P&b¼÷ëQ#2ÍÓógÄ\x0001æ\x000c]	B&\x001e#:\x001aÑâÂN\x0017Êã{t@!}05<ùä)/Ý|ª¬)·\x001b,eMP2¦ë\x001ajÛ»w<ÖY\x001aÓ\x0004\x0010ýÅ\x0005"\x0012(ï1&ôÉum\x0007®#\x0006Ü¾9 ³»dÂòÆµkqÂû÷xewÂFzêÓ-ÑtÌzuD*Ã æÊxÄ,\x001aprpUÖ®Z­`
ùÂë_$\x001bîð­ï|õ²KF·I}Nc +¦© $BÇ¬ª§ËO7\x0015\x000b/hâìªDL,âPªë\pcë âá=Æy$-R:D^ÒÕm±e[ÔeëL@÷ú°¯*©´F(GÑ¡\x00106
ô\x0012­sPlk\x0007RÑ:Gk\x001a\x0004Ø\x0006<s\x0016\x0000-d$Sb«1Ö£DD¬Ákµ\x001e4DY\x000fôðð¥c¢8\x00054íH/©kÛ\x001fÎÁ\x000bu\x0011ÆÖX\x0002¦TF!Ùçz§@¡x\x000bw(] °üÚ×cþÁv½Cú\x0005ÂkCW¬bo­ï±È@¿Ò\x001d Az°Àj¨\x0017
Ê¸ÿ±7ë-KÏó5ì)vL9y¨¹«NwUusj²É¦)R´\x0004Ã`ÀMûNþ\x000f¶/\x0005È¾1\x000cñÆðGY7¦i\x000beE&{,v7Éî:UÕUg\x001er9ö´&_¬YMË0*À2OFf¬ý­µ¿÷{D:Î¶sÆcÏÕ+g\x001b\x0003tª¢/)e`2ÌYl\x001asdYNUG¤QÛ\
qÌærZ}´\x0001¬§Ç&Äö\x0018\x0006Íå¾t@²Æál\x0014s¢\x001bJ\6\x0019Ò,ºÃ\x0011\x0012ïâÍÊ¢\x0014Ü¸x#\x0001\x0017\x0002Êõ®I	UÛ \x0007g\x0019\x00149Y"ÀÅ\x0006\x0017\x001e¯\x0003¦£jáªuqÊæ\x000b?úAìJèÏ3B\x0004°\x0016c\x001bð\x0016¡\x0005:	`PaÍ ÝRê-?GTÏñêA\x0001\x001c¬\x0019àD[ËJÀE§	2!¨8â|ÌVtV\x0012lJÃ\x0018«\x000fðò]¼ÿ%\x001c·ðºÄÉ\x000e\x0018`
4I¼¡2k\ Ý\x001a!H±b8¨ØK¾Ëëßþå/\x0011¶\x001dËsË³G3B=g 5WËÃ/ßæñó\x0017lzÇw\x001foðÙ1ì_¿Ë\x000f`ñÓC
1`µê8±GÜ¸\x0015írÀ£o=åîvÉÛ_{\x001fï\x0012¤È&Ä¯×aF C2b	\x0006ªÅ¥?${ý\x00017\x000e=¯Ý\x0011ÜÿdÊþµLF)«ªÂS.â©±ÇoDÔé'k"ß;
jýjù	Iû\x0018Ì­öBI\x0017ëk0@(ð¢7*N2\x0005ßÒ¹
zk!Í\x0002Y¿nñ\x000cK¨\x00163ò4Î2[\x001dSÏ@V\x0008\x0016óÀ|q$!LC\x000cì\x000c±TlÌ³³\x0005ù§?bwÿ	¯Ýë¸zuA>Þã/\x0007,Ú	\x0015haÑÄCB\x0010\x0012/LL¸\x000e²ÿ³Ã)\x0007B\x0012È(Ô>ÅàM.ü\x0000©fØî¯`ó]Î(Ó×éü\x0004ç\x0006,Ö	YØ§jÀØuK¦\x000c©\x0019\x000f\x000cFYA­[\x0014\x0019uåh³Ó%«\x0019$\x0012Z|\§BQ5
fã(\x0012@\x0007,qj:ÑçñüÑ6\x001dÎÆ)ë$\x0011ÔÝÙ6¥=»ÆÒlxóÍ7Í? n}|o½£i I\x0002\x0012ESà6lV[×`¹\x000c\x0018áØÝQ(áH Oul\x0010É\x0015YRá8¡6<û÷?âø_}ÄË\x00175"É¯:T\x0002Ó1e±Ïp øég8;\x0013|ãëû¼ýÊ\x001d¤öx8ÛB*\x0010i@t\x0019ÙpÀ¤ñ\x0004i¸v½ã0ý9^¼37Ø.óáÇ\x000b®¦/¸vàÙß,×kvê½½W×Rm&»äCØl¡±r2bo¯ ÕX\x0013ûå °m¾xÕ*! ©\x001aC%\»vºn*ÁûÀÞ~\x0007\x001fïiÚ
¥à/þòÌf3\x0010\¿v¦©yÿý¯rçÎ\x001dNOxöô%I¡u<û1_,\x0019%y>¤j+¤\x0010Ü½sÓÓ\x0013L»¯¿Î+Wp@9\x0008Ïf»æÖÝ;lª
w_»MçjÊQÆºóüè9¿ô¿\x0018s©ò\x0001wö\x000fyþô\x0019×\x000e¯rëê
\x001eþô\x0001çÇ§\x001e)Áõ[7ÈËº®ðÀr>Ãñ%t\x0016Ïjit¥¤EÔ\x0019Æ\x0006Z\x001bpÖÊºõ\x001dsóÖ
7<ö£'\x000føÿà?¤ âÕ«%]gi\x001a±\x0002\x0013DMcÖX? øñ\x0015\x000ev7<yôwß}AðÁw? XÅ»ï|ã\x0015;£	ÆnØT\x000bê&\x0007¶µÆ9£á¢ÈªãÊÕë|ôÉg¬Ö\x0015;»\x0007\x0014\x0011W\x000cÉxBÛ´q@\x0008^<{J§\¿qAYbmM]7Ìæs¦;%O<¤ëÚxï«\x0015JI$e0Þa»m8/PZ³ÝÖtÆ\x0002,/ÐYÉ«S¦Ó\x001dòÁÊxH¨6Kf\x00153Ü¾{oû;8§¹}ë-&ã+Ô.î§L£EM\x0008[6Û%§«5i¹ÃÞý\x001a?¾ÿSºº¦[W¤¾co<b»<\x0003kHe\x0006R0Ê4çó\x0013NgK^}íu=}L×ÖdZaZ\¹F¢\x0012tV"á `Û<áù\x0007\x000cR	Òñþ×Þ$ËS\x001e=z\x001797o¼\x0002òÖXkhê§\x000f\x001esýúU\x000e¦{<|øQm¶\x001c\x001eî£\x0004\½~+¯¿	:ãäô@àäü\x000fÿê/\x0019d\x0019£²D'ÑpÄÑlÚßúßÿ½ÿëW®ó¯ÿ"ôGÀj¾¦È2NOÏcóPÆøñhV	ù,Ëxû­·ØLyðà\x0001®k\x001c\x001eâ¡®+þøþ/Þÿ}~û·þ\x0006ÿÃ÷ß\x00120Ì\x0017gÍgà/gøÞråÊ\x0015Æ)|ú)uì\x001f\x001c2(Glë4Iú¾BÆþÞ.õÃ½\x001döv\x0011G6¼µ\x001d¦áÉgL¦SF£1ÇÇ§dÙ &iÁÙ|I1Ù£\x0018üôé)åÙÛWv\x0019\x0015)ÿÆ7¾É¶ª8:=ýÂuk4\x001aáãüüõzÉzS³ijëM\x0014\x0007³\x001c\x000eH²\x0012­Át\x000e\x0017\x0002y1äÊ«Ü½{×nH\x0001ÎQ7H\x0011\x0018t^tS\x0004\x001f{6Ö\x0006:ë@E\x0007âp8&M\x0012l×²Z,â\x0000\x0008è4'W"ô¹R}ÃÕ]tè\x0000c\x001dÎwTÛè,ÐYFe@ÜdYgQ9 Ï\x0012L\x000b*ÑÃ\x0002ç=]×±³»Ck¦£\x0001y*X':ö£´\x0004D'B?(Þ'+`é3X
iÐ¶\x001dÎÅ\x0006h¦Xk	Þ"eX$Ñ \x0004E1ä`oÉý]å4I/@JÞtuÖõÙ\æ²\x0019m­e³ÙÄÿ?|î\x0010ÑIBQä\x0014EÆr9g¾Xõîz³Áu-¶m\x0018ÆäyÁáþ!Y1L9??åôüÅbÎ¦ÞRU[\x0010\x001c\x001cî3\x000c\x0019å\x0012oZ\x0016«\x0019«ÕÕjMg\x0003óåÑd³Å÷ßû÷É££\x0019"ã¯þê\x0001o¾~G\x000f?¡Ú¬xåÖUí\x0008¾ëÝë
:Éhê:\x000eq;OÛ´$iÁµk×xï½÷xðà3^ãUþÙÿùð»¿û\x000fiª%ÒI^¹{oýÉ\x001fóÁw¾ÍWÞ~¶1ìGÏììî2ßÔ¬ÑMYo7`8==î\x0007ã\x0003Ã²ùTÃ\x001cibîÞtÙÙ\x001c×yöÆûdª$S-­­\x0019æ\x0005ÍrNdÜ¸¢Y¬çÏHÒ}¤¹ ª¼RF2\x0005ë|\x00145ú¬ô?ÿÁ\x0007Ü{í\x001dN\x001d³xÀfu/\x0019M§ÅéØrtzÎx2æì|Ég\x001eróÖm1«ÅYD
v
÷ïßçÛßþ6çïþ;¼xñ?¦5\x0006\x0011,N ÛR¯k\x000enÜb:\x001aSW5O\x001e>C&\x001a×zÎNç¨¾vv#\x0004É/þÒÏszvÂo¿ÎùæÃ\x001b´´8\x0019{Ö\x001bÒ>2&KR´RØÎpr|LµÙ2\x00198ØÛ\x0007\x001f0mKY\x000cxüð\x0011\x001f<dTÆ\x0001@¤ÚlpÆ1\x0019î0\x001eA£DÆéÉ\x0019?ýøì\x000b×¬¤Èq> ôóÛE\x001dÐR\x00179\x000eP
ß5\x0017'!\x0004ÆY|?\x0010h\x0003"¢\x0018µCÉ±\x001c½hRm+´ÌÎÏyñô)óó\x0019¤IÌ&K5A\x0008¬w(¯ÐYzéÆÒZE\x0007í]*¡è£Î\x0018\x0002\x0001¥uß³ÐØ^\x0010\x0013Z!zt«µ&¢\x0018\x0004Ót<ÁÇOÉµÆ45i?l¯B\x0018¨MéjfÛ5.Àr¾@¢è\x001aCY\x0008^ðá\x001fsûÎ
VÕÖ»>æ*#µ\x0003¨V8\x001f¾#5fÏtwv±¥ó\x0002©\x00129u\x0004\x0017?VheÎþîÉ"Iñ¾Åµæ	y*Ø\x001d\x000fIe¬­i¤½ãr¾À\x0008ë¢8*$ÉÈdÌ7Þb}ÌÄ{|\x0000©£k¬,5BT8\x0017%EYD£\x0011Á!ÁXI×9\x0001'\x0005V@ÛY:kqÁc¬eSU\x0008\x0019ãyº®ßÖ\x001c\x001c\x001ceÉ¥ãO¡\x0008ýµî{³U×8`-d\x001cjõ</È²®3\x0018³à|6c±X\x0010B¸DÇu"þ°Ø¶-Þ9ªªby\x000fsw\x0000\x0000 \x0000IDAT±X°Z­Øl6h­£\x0008ª\x0014ÆKç¡R*¢pM/+>ÐÅ^±\x0006¡5*Ñ¸¶îÌ\x0010÷Lí©cÂ[B/h#\x0005ÆÄaj¹Bù\x0018Gcm4k\ ö/\x0006j/â.¾\x000b\x001cjÌÛ=ko]Ì\x0001uDéË!ð­Àç$·¨QÅ\x001a\x001a
%I.ëMC("&IB¢4å`\x0010±æ*æûi­é¹\x0014äÖbî°\x001c\x000crBðlVë\x0001Û×\x0011k,Y^D×°}P¥5µíÉu!h\x001d3M¡©+´·zcØ®<ÁAÐ\x0001C	\x0014t.Ð\x0003â³\x000c¨A\x0014_dÊeÞÔªwdÅEï\x000e\vmi·\x000eÛÖ\x0008¥z[2{\x0008\x001eMDq`\x00036xb>\x0017±+èû¼5ÑóþÜ? ìÍOã¢\x0002\x0002áL×\x0016h\x000bº¥`{ÖPÍ\x0004Ý:`\x001ah[Ac\x0002]ð1&ÑäÆ¸°ÖÆÒ\x0010 õáÒ¥Öþ \x0013\x001cQ\x0013\x000b¾(\x000b~\x0006F\x0010cU¥\x0001Ð¢Ï ü\x001cý\x0014/\x0002c\x001cAÅI\x001e4\x0008¯\x0010¤ètH-AtH#Õ>R\x001cÐ5\x0002oZ\x0006Aá 3tvÖ²97TKO×ö.\x000c\x00113ËR\x0005Y\x0012\x000fÎZ\x000b8Ô¥ÃSöù*
¨, Ó8á-û§¾È"T \x001c:\x001f#ûõ#¤@+Ý[q\x0015^I
ý¯Q¼RÂ¡¼Cx\x000f	Ö\x001aëðÁÒ­+¶³(ìúVc»\x0018²®u\ñº4H\x0015ð½Ø&tï^L#F4¤>ªgY4 Ò\x0010\x001d¢Iÿú4$Ä\x0005H%eS\x0016Ý§Öä#VqýE7ad\x0010\x000bé2¢c¥¸@ÐÆ¦a¡zbl\x00148\x0004\x0011\x001f(Cd)_f\x0018èâdNh@4P­\x0002®Mó\x0018_ëP!6´pib­f©\x0008Ò÷îÔXÐÄÅG\æ\x0015þìób-\x001eÚ[åS÷\x0002j¢#\x0008\x0011£/e\x0008T
ÂZqò f;o\x0011¾`2IÈ\x0007\x00152í¯\x0014\x000f\x0004y \x0015ZôÏè>x-û/öÐ*Ör0 K\x000b:E\x0008ó
M·¥Ñ#Zc\x0011Á\x0013T.`ê\x0006k:Ë\x000cÐ´¦cÛÄ\x0006·\x0002a=]M*\x0010 eº«éº
R\x0006ö÷÷h*	Bx\°t8w¸Îb[\x0013n[S\x0014\x0019yôkÚP·[2\x0015\x000f\x0001¡ÿ\c\x001bõ(©£kVD÷s¬\x001bÆ´\x001c\x001c3\x001ehûpi! ÈX#$c2Ñ´Moç£»S^l®^à{'w\x000fq¶Åà-Îùø¾H\x0019'ãî[¬ÏÏXÍgìÜ½É Ê0G)0¸u¼¤ÆYÜÝåéé	ÞzÒ4e¸{ë5ù>ßýî}>]Ð\x0008E1\x0000)"h¤´½­\x0014­óTmÇéªáhÙ0¯\x0003\x000f \x001dA
¼Ô>kPÉR¹\x00001¯SJ\x0010^à­A8¨\x001aGW\x001b¶Û¦©ã¦OÌÁ\x0010Ë?\x0010ss!âð$\x0017q×s\x0008¢\x0013Ñä)ÖF'¦÷\x001eá®êè÷ï}n\x0017è ã\x0017ªßè}\x001c\x0011)\x001014X\x0012ß8¡µÖ\x0018\x0005B¬E¢pÞb}\x001c~qAÅ<\x0002\x001f'ø\x000fñ (\gðö\x0014\x0019\x001atrÎ½w&üí¿ý:_z3\x0003û\x0012-¶\x0008_#¤\x0003dÄc{â$Pü\x000b\x000f\x000c_ïk°\x0002á.òû<¦6:æÃ\x0006çÉ²¼\x0008P¡`µ]ãìLK
áÙÖu\x0014pûé)ÓyTâHt³\x001dRÐã1"Zóâð{\x000f=/ î±Q\x001fq\x0008©1Q\x0010LÄÙU\x0008!`\\x001c\x0014²Ö!ûéÉÐ\x001f#à\x001c\x0004G@]bGã\x001agÃz\x0000tÛ¢ 
ñ\x000cdBÿJ$ÍÖ\x00112I¹÷Å3\x0008/2k­·øÞ	é¥#CñI$\x001dÔ\x001b_!ÂKnN\x001djÖÉ£\x0000Yb)
Ê4`\x001ck:t[¹Ü\x000bZOð´1_V4¬\x000c8?â\x001d|þ\x0016'¼Åí\x0015æÍ\x0004ÒRwñ\x0010£
¤,PÁàÌ1ºCmÇÌô9uÐP7\x001cäK¾ñå!7o¡Úï°\7|ý7öø§ÿÛ9n\x0019¨\x0017\x0016K\x000e®ß Ù}ÿû\x0007ßçî÷¸uóW±î*÷ýO¸ç?¥\x0018xòø%¯\ýsì¢b½\x001ep>öíu\x0014mAÒÕ=\ñ¤¸ÏÝw¾Ð¶h\x0011§\x0004²]÷76\x000e#2\
ZÎ\x0018Û§Ò1²KÞtÖG,¼¡Ð²ßE\x0003^fàs\x00149\x000e
tBã\x0000³e\x0018JÊag\x000fË\x001f£í\x000bðP!ÈÖ\x0019Ù !K<­õ4ªÅ¤ËûÐB*s|wÌbQYº²A·hå\x0019\x0003WFzÏñÑ£\x0004+®0(vxãvÎHÍ1§Gé\x0019Ý a¸\x0003rXa×Í\x000b
\ã³Nó¢²WíÃþÛ7>àíCKg7üàø+Ìý4\x0011\x0014%\x0015{,¼C\x0016\x0006jÃ@ìÐÙ\x0014Î\x0008r\x0015)^)6¶EåC|ø2Ûå\x0003Rÿ}ÆùvõOHÝ1*ý
tùMLz\x0003}päëÌ\x001f<ÀºN\x0019tî8b"OR®],f3Z¯ùô©âù\x0012Ú­ÄvC¬Ø\x0010\x0012c@Þ¦^¯\x0018eç(Û"´CËxOBa^bóã\x0015>@ç!1\x0015Ò\x001e2k'\x001c§cv&;m9a%M=õÆ1N\x0014ó¸Ð ´D%\x001e]¤YKk\x0014©c|P\x0004iæI¤Dúm\x0002¾\x001fhp\x000e<\x000fpä(KI{ïxôÌ²\d4$)\x0014:uìí\x0005¤«éáöÝë¼~wJ[sÿ£¿äæÍ]ÊQN\x0008ä \x0002"\x001bBd×n±8;¢,w98\x001823Oæ\x0014cEÆ
®&[êú1[çØ?0¯O9ÈîPÈ=ð\x0019û£=vö\x0013æ+Ãl½`xà$fc}Ëá%gKX?üÂe$-ú½3¥ë\x0002BfX×"UÆl6£í:¢`P\x0014<}ö¼ÌùÑ~s[·ns|rLÛ¶<zô{÷î±³³ÝÝ½èÙ6(±\­úÆ"ÍReÉcÎÏÏì\x001f \x0007C\x001erxå*ñx\x000fª^0\x001a\x001fsxe\x000fGÏ\x001er÷µ»$EÆj½å|½¤\x000bí|ÉÙË#^<x­ZÎON)ò7_{tóòôÕfE×Y\x0006YÁp4$¥î<V%äÃ	Y9"\x001b\x000cã~l\x000cy^ê"ñ\x0008\x001a¬mÙßìðêÝÛäæOþå\x001fò\x000bï½Ã×¿ö\x000eÕº¢®1UÍùé¢|Æ/1ò\x0018ë7\x0018SÈ[\x0008?æ;oòðÉÕê³Ó\x0015ù\x0017ßç\x0017~áßd2¼\x0014m³"\x00115«í®ëX®7Ü¸r\x001f|úç¼ûå÷Y,VÜ¹u³³9O¿  Ùßßc<\x001e1É\x0012Íü|FY\x0016L§cÎNOY/f¼öÖ\x001bHéyùòiïäéâP\x0019Qt\x0019vPJcé§¬=«õ¢\x001c±Z­ÙÎæäYÁ¦n8?³ÝÔ 4ÃrÄ°\x001cspõ
ûWn#³ñ4e9{Îã§øù¯¾ËãÇOL\x000fyõÕ·É1g9Åh\x0002¡Ã·3\x0004\x001d\x000f\x001e}Fe,¿ñ\x001b¿s\x0002¡\x0012\x0006YÆÑâ	Óñ\x0008á¶<zø\x0019{;¤it7¬ÎÏXÎf\ÛÛãÇþgÔUÃõ\x001b7Lv¨ªMÛHM\x000ch;Kç\x0008=æ³\x0007/ù¯½ÅÛ÷Þb±>â[ø\x001d®^¹ÃáÁ«ì\x001e¼JviÛs´§OáZC°'\x000fpëú
º¶ãË÷ÞÁÙ.6Äê£Çè¢¤®k¼÷üóöOyë­·H\x0017/^ðî»_¡\x001c|üñÇÜ{ÿ]NÎÏXÏHµd\\x000eÙîñÙ'0\x000e\x0019\x000c\x0006=çåStR°;Ùe½®XÏÙßÛ£,\x0006|òÑÇ|çÛßæ×ý×¸}ë\x0016ø\x0007@Y\x0016GcÞ~óMæ³3V«\x0019å9ËÍ\x0002ç=Óé¢\x001c\x0017\x0005«ÕÙbÎbµ¾¦¯;Ã³\x000fïc¼ïïs2<çêá\x0001uµáG?üs\x000e\x000föØÙRmH	ÓÉ\x0008U\x000cxöâ\x0008kZ¦Ó1mç¨ÚÙÉ\x0019»û×(Ç;<~úw^¡k[\x001e¾\pþü	_ùÊ;dÅ7ßÜùÂuk¹^svzFÛ¶XÛõ\x0004\x000eE\x000f\x0011Þ£³¢\x001c1\x0018h\x001a0\x001eyíµ·¸õÊ
îÜºÅpP²]­hÕrIÓÔèTÅæ] F Ñ:E§\x0019áÝ=Fã\x0011J
¶5g'GlV+B\x0008£!ÎyºÞ ¤¢ë"	Ç¸x\x000fé[KÛÔT\x0015>\x0004AÄ±eyNY\x0016h9b:\x0019qóú5ÒDsºÙRUÕ¥»cP\x000eØÝÛÁv\x001dZy¼©Ù¬
Êñ¢ÚÐu\x000eÑ\x000f\x0007ZÛF\x0011ØK´$M3"Gõ®	Óu\x0004ïHRMY\x0014ÈáÉhDÄ!ÑpÄÞxB9()Ë\x0012èÈv DtXgé¬#\x0018·ÖE\x0007{h¦a³Y_6!6l[cØn×\x0018Óõ.î\x0015îló
k\x001aêí:\x000eá@\x0016ìL&$iÊp<¢\x001cy~ô\x001c5?_¿«q®#ØÕÙ\x0011ëÅ£ãc¶3x\x0004N¦4æ¯ã×xý7xôø	AÆ\x0007\x001f|étÈã\x0007\x001f£¥ãÎÍ+8S3È\x0012êuËv³b<\x001aâÂ¡Pit£
FcÞxó-ö\x000e\x000eyôø\x0011/_ð\x0007øÏùÏþÓÿ\x0004%!Q·¿òe>ýè'üßÿ_i·\x001bæÝ=ÚzÉk·®pºîHòa®\x0019\x0019Ûí f?¶\x001dÛíg]K9,\x0019C\x0006]A9,I«×h·¼vçuÊAÁv±e:Üç'þ
¤àÖ+wXÕKj©\x0010Ò³Z{6õóó#bBHáhB×.cµ5\x0018Ûâð¤JÓu\x001d\x000f\x001f~Ên9!ÍR®ß¾Æùd½\b;ÏááU\x0016Ë-»Ó]ªºfwoUUqÿ§\x001f3L¸zõ\x001aËÕ¯Üû2O¿à\x000fÿÅ¿àæ­\x001büÎïüGü\x0017ÿù?@	CWw\x0014ãzÕ0\x001dìP$%õÖ²·sÈ¸ÜåÑãÇ4Ûé\x0001Óé®óÔ«\x0019×o^%I\x0012f«\x0005_<¦ñ-Æ
2:q¼°$HB\x0010\x000cò5ºY®ÏfxçØîg\x0019xO¤8\x0013ñÏ=¥(Rò\Ñ4
Í¶!¸Àt¼\x0013ñ¬!a:>àÑgOøÉO°æSf¼\x0000Gtæ\x0005\x001f\x0008Î#l@e:ºzQ^üLO#\x0000Îº~-ö]ñ¾w[EwSgL<Wõ9:KAJÍDj:ïØ,WûSVuH\x0014IF×q8ç\x0011Æb\x0001!HRI¢4Îylg±JO\x0006H!1í
g,*\x0008kI|ÀØÓ\x0011Z! WvÕQU[NØÌ­A¹\x0018!3ÙÙAe)kÓpãî\x001dþê£\x000f9ÏH4ÏÈ\x0006\x00193¼<~Î4ÍÛ×_å{ßÿÁ àÍ/½ÁG?]1_V\x000có¦¨,%Ø,ì
JHc\x0006öèåóeuÊz\x0008\x000e\x001bbtÚ0\x000fìO\x0013\x000e§	< \Kc<V\x0006º.%KSv¦%£2Ò4c<Ê\x0019ä\x001aA ÝTÌ¶5q\x0008ëQÊSæ9Á¥t]MÓ\x0019
Ñ)+"ý+\x001bd'%Î
mm\x000c[ßH\x001aÕ+\x000eÁ+×ÔÆÓº½÷\x0004Zk1]t¡\x0019oÙ¬\x0004Ö41WÔE\x0011íÓO?\x0005àW^!KSºÔDÇaß¿\x0018ÜðÎÑvnf­¥ëZ¤\x0012ÔM\x000bÑµÙl.ÅA!\x0004ëõ:^m{¹V«ªâÙÓg¬æsªíív{ÕôÞ°íV z\x0013^O\x0004sÖámÔ|O\x0012Áã­Å\x0019\x000f\x0001HD¢è£j6Ti\x0012#!ø~H!He/â\x0011Ði|Ïul«\x001aA\x001c\x000cP½Ðw1°~ñº³,»\x0014\x0007/p£ÖFÃH¨>&(¡kÚË<çÐ¾2">ñÎ¥cäS4ÅüB)¢`(ÄÆÏÍ³A\x001aøèIIR\x000cK¶uÅÙì¦i±>bJ\x00030\x0018$¡ÏCïÝ½J*\x0012©\x0018$\x0019ãAIdèÞÑ(¥$Q)P±­\x000c¶j±BaLë,Ú¶°ZlY¯,\x0000Y.ñ
t*ÈrN\x0003ºè\x001cT\x0001i\x0006*ØFzT\x0002IÚ3YSì³ì\x0014Á ÅO5¦²4\x0015®£³\x0001#àÂ.ç\x0003p\x001eÑ~Ò\x001fp\b=®« û§\x0002¤XB¥2\x0006Ì\x0006$Á	Sà%Á\x0008lmè¶ö$°>1\x001eY¶30[p
ø.@UK\x0004\x0014\x001a\x0002\x001a+X;¨êÎ
\x0008IBç:²$\x0016ðx!\x0011þ\x000cbôgD¸\x001c#âÉùt¡w\x000föMØ\x001dA(æà#BOÈØ\x000c×qjUëL\x0017èt\x0003Bhqnµ1«H)P"AK7\x0016ßÖ¸MÙZêuÇì4NIwÝÅ\x0017°Y\x00166! 3\x0006ëB¯Úú\x001eS©P M MCD¦\x001e>0
\x001d2± -º\x0010¨B¡Ó~\x0008_\x0004\x0012!PþâûÌd/¢mV\x0013ÐRF1\x0011±IlCxIµ²ÌO[­ «C?Ò#D\x000c
ï.¸¯\x0010\x0007ÿIÒ¸\x000eõÅk¾\x0010:³Î>Çoj-úß÷\x0017±v\x0004åQ2æ¥eIÆx8`o?>æô¨AÀî¨ Q£(¦iqú\x0002¡ìó\x0008%\x0002\x0011¸½A\x0014\x0011J\x0010\x001a¯ClÜJ\x0013\x0005:ç\x0010VQV\x0012\x001a«\x000cnÕá»@\x001d`\x0005dÚ²Ñ+z÷¤p\x001aÏQ¢½\x0010/~fm
>Çô~¾^ã¯Aø~e¸^BèÅÎÏÅn!8\x0001!ÅÖ#>¹?§®\x0002£¡d²£/×óôÑ±à	uÇ)>ÇÒ\x0007ö*ù¯¡÷þÿ\x001eR\x0019¤4\x0018Wãz<!\x0002\x001f\x0004J¦à\x0015¦í°8d®"öÈFgñ \x001cö¶{X®æ\x0008§°­a²³O&4]K¢KðÚ\x0004&o;;\x0013®Îb0<\x0011\x001fë\x0016ö`{\x0017µ`Ó\x0019®è\x0003\x0006yÆ²Þ(í*t*"ÖÎ\x001bpàxXDt>Ðc\x0011c
¯Ï9:?b¸S"T ó\x001d"\x0007$iª	!Ã\x0018C¢\x0012Ò$#m\x001aVÕÎX¬é.\x000fJ\x0006Ú\x0010\x001b®J)\\x001f«´¦m\x001dUÓòlµ¢¸rr<áåÙ9×¾ô\x0016å`ÌºÛR¤C\x000e&\x0019û·o!ê\x0005´+\x000e÷G-glk\x0016×orëÖ+|ï;\x001fòáýG¤ãC2\x0012+Ð\x001a\x0004ñpNif];¶ëÓÅó¥iãÆ)BÉ\x0010]>nÔ
\x001dk}\x001f<,@"ãpCg±e½¬p­£k[sqÿ\x0010ýÇön\x0014.\x0004ÁÞæé7fGP\x001aï\x0004ÒGáÀ%Ê4@/þõ_\x0001H\x001dýG¦\x0019ý°w\x001e\ÌÚ\x0011JG\x0007yïÎ¨\x001fµ.²Ú«àc\x001dW"Ð\x0018Û\x000f DÔØ8mlÃá£³I.4ÓÉR²7ØðË_/}iL-Púà+µ\x0004\x0017\x001dÍ\x0017¹\x000c\x001e­<A¸8óù\x0018Aü\x001eGäãÔ±Ðu\x001ecAÈïîì3ª\x000cÖU\x0004\x00110Î¤9RklWS×\x0006¦\x0010ÊÞyP\x001e©/¹øUEï\x0016\x0014¢w
öµ æ¨ø¼A`GØ\x0000Q\x0002|phÐÕ\x0001|~\x0003\x0004ãÌå\x0004ïÝAH\x0005ácí²?©Å-Q
û\x0016!Õ\x0003\x0002M¬)Í\x000e8ÖV\x0010/\³\x00141WB\x0005\x000c\x0011ë ã©Dõ\x0017\x0007øziqÖ°ö\x001dÁ¶XaiBÆ¸ÈØ©7\x0004¯ÙÝÑ@q/c®J6Dø\x001d\x0002ED\x000cû\x0006\x001f:¼mèL\x0013Ãê\x0001B¨ºµOhE\x0013\x0011#¤ÞZr:´¬I
©<co§Å5ÏÙzR·b28åêAäã\x001a)áµ»wøùw\x0003ßú³8Ü$<?}Èkoÿ\x001dv'k´*\x0019MjÑU8¸2 ksf§\x000bÆbÉ«¯¼Ïúø\x0001é¤e+NhÚ\x0019J\x0007Vs¸ÿ£Sf§\x0015÷Þû\x0005²á\x0008ÑuH*p\x001bP	!X8T¥¤YGÛUì`:ÍX=_3È\x0003ÊCâ\x0007\x00045À\x0016!V\x0008Ù\x0012sxEDó:HüT¬ðþ;´Í1JÎð¶GßÀì¤b2Ñ.Hr$9¦Õ1,Þ\x0017Z\x0011BÌ­*Ïbî©[xë
ï¢ãZôÓßxÇô0çì:¹ÃáÝ+8ûSºùGìd-÷¾V2\x001c¦\x000c¦W\x001cþ
\x001f¾Ä2Ü"Ûâ\x0002tHNÏÙ\x0015÷N¹7nXÍÏØ+\x0012l½ \x0017¢Ìq[ÉÆ*\x0012Ä\x0008Ä\x001a{¼
1»V%ÎzÁ5´ý2Ýù\x001aa\x00199õò»¼X?fÿUO6ý5~ü£¿`üö\x0008é_a9ÿDÃfc©õzÉ½·_c>Û\x0015	­ã\x0017-ÛFà¥Â$[ 1î\x001aÃò+à[\x00043lhÑ	$RbG\x0004N\x0012p\x0019|üó3OÒ\x0017¬ºõdÄØ\x0014:\xÎ÷Q¶k2	AT$¹Ä·
¼\x000e
"âM)ÏþÂØÀt/!Ks¬kâùW	²xs·®±4Æal ®<u
wïFäðÎ.l-yV"µÀ\x00058}¶&k\x0013¨\x0016\x001a³ñX±]¬xòÉÝ½+$£Ëa6!\x000c"
\x0004ó5¡ú)ÕyÅæÌ ÔÝá{õoñøÉxzô]öv÷)Ç×XÏ\x0016èÜdÉhÌÎ¤ é\x000cãó\x0015¶Ih:GY(ÒLrå\x001aüÅ§þ\x000b×­á búò4£(
ó¤:áùóç|ï{ßãæÍÇcf³\x0019ù £[u\x0018Ó1L¸sç\x000e§§§\x0018cxñüÝÝ©·X,H«W¯Ð¬Ö\x001b^P\x000erÆ£výúU>üðC\x0008ÃÃ}&\x0011''G¬×\x001b\x000e¯ÜÅZÇr¹`owÄÏÿüÏsvvÄr¹b¹\ðè³\x0007üæoþ\x0016e9ä³\x0007\x000fPiB(\x000e\x000föx÷í/óìá\x0013>øñw¸qõ\x001a¯ÜyGO2[¯îï²»\x0018±LuËélFVÐyÄ(¥ÎQd\x0019R\x0018o\x0011ÂKO¡\x0003Ðá]ËÓ'\x000fh¶\x00157o\áOþøO8;;ã\x001b¿ò
V«
Ù"f\x0008Ép8âùñ3²RQNs\x0006IÎ¶&P75B;ö\x000f¦<ö\x0013>þø/\x0011hÞ{÷k4mËt\R·\x0006Æóõt:E+EUUt¦ãàpõf\x0013\x0011­\x000f\x001f°]¯\x0019G\¹r\x0010<Ee	;¯¿3?ºÏt:áÝ÷¿Ê¦ÞðäÉ34æ»Ä¼\x0004ï¢;IJõù$tèÏS.-o\»J]7¬·5Ãá×_ù|Î|¶\x0004\x0014MgXÌfÈd@Rt\x000cG)«õgÏxíî-ÎÏÏyçÞÏqåà³³S\x000eö\x000eÙv\x001d]ÛÒmÏÙß)yùü\x0011;Ó1·oßäÇ?þ¦Þðôég\x001c\x001cL	ÎòäñC\x000eö§\x0014yóç/1ÆrppÈì|Iª\x000b®¾z\x000b©S¶a¾¨¯V´mG\x001fók¿úë¬f\x000b\x001e?yÊþÁ\x0001{û{<{vÊbyÊ\x001b7)ò\x0011¿úk¿Îf+\x0019\x0006üÅ\x000f\x001fbLÍÉéK¬5¼öê+Ü»÷6|ò	Î9>ýì\x0013Þ|ýx"%Z	æ³ènzñâ\x0005Y¢¹uã:YñüÉcîÿäCò¼ÀZË¯|ýë|ÿ[Ê¯ó×ùèþùø£ùÊ{ïòíï}\x001b·îrÿÃÑ:Ù&ôbåÖ\x0018kyòä	ÖZÞûêûL§SþôOÿwÞyçOpûæMDpü£ÿñ¿Íýë7\x0018Æ4mK¦|öð!Óé\x000eMÅ»wY­6\x0014Å¯~õ«TuMc\x001cO?ãèè%_zó->üÉO8>zÁáÁ>ãáÝý]^¾x5¯ýë$yÎ¿úö\x0007\9Øçèä\x0010bçþþ>Ãñ.³UÅöìÑxÂb¹B¨ÙÖ1yå\x001d~ðô»w®#VÝ\x0017®[«ÕÅlµ¶_ËcÒAÎpâCÄ\x0001'ù$\x001d\x0017	û»ûìï\x001dpýúU®_?`gw®®YÌg¼|IÓÔ\x000c\x000c©\x0015iÙl× \x0018SÊRë"\x001f0\x001c\x0019\x000c$\x0012\x0012-	®#Ë4Á\x0007¤tªªY.W¬KºÎà¬¿t\x0016®Ã\x0016Ù×$Ñ\x0002)â½»\x0014á d:Ý¡­6,\x0016\x000bñ!ppåÝ]\x0006E\x0008\x000egjº:\æPm·\x0015m\x0005Äg×\x0019èÈ²4:Ð$Ó\x000c%E9Bé4\x000e=\x0003£QÉt2fgáp@Yäè$öþt\x0010( eÀ\x0016Ûo/Î9¬\x000f}ÎjÄÜy©1Î^º\x001e¶Û-ççç´mû×pµ1{«C\x0008Ïd2dowRD)ÊÁñx\x001cµEtðN¤9i±3Ý%Ís\x0006ã\x0011Ëå£ã\x0017,\x0017gd©"U\x0002×np]<\x000fO%è4/qBsçõ7ù·þí¿Ë³£c¦áû\x001f|É¨dµ<Ca\x0019\x0015)Âµh\x0019(2ÍÕÝÛ\x0004ki\x001bG Eê\x000c¤¨lÀÕ[·¹yû6óåóc¾õoñ\x000fþþßç«_}\x0017ÏðÞ½w\x0010®å÷ïáøå\x000bR!\x001dc;·n³8=b4=DgAª\x0018\x000f\x000b¶uÉf³eµ\ã} í:ÎÎÏ9Í 8îÝ»±bRÒÖ\x0006ß\x0005>ùè3^\x001c½ QÍfÅ¶®xytÎ½÷Þf:LYo\x0003JÅóhgL\x0014\x0002dÊv³&Í"ÆT)EI|d)4\x0005\x001f]/ßÿá÷ùæ¯|£ç/¹}ý\x0016mc©êétkW¯qtzÆùrÉoüæo£óßûßÖ´(%Ïøòûïñs¿ðKüé·ÿüÿ\x0011ÿÕ?ü/ù{ÿñßã¿ù¯\x0017¥\x0012³
Ã´\x0000'9;1Í	¯¾FY\x000e)²!ÞJË\x0015muJg\x001dóÅÑxDÕÔ&#\x0016%¤aRÐ¹\x000eKB#¹N\x00086ö@ªÍ\x0006Ó´ÊatråQm¶<{üù|g¦Þ²ÙÔh\x0002£rÊîd\x000fÓ8\x000e÷o°:ßrûæëØ6áèÅñ\x0017®Y³XgqÂ£Ut\x0006)\x0015Å8ï¢¹ãÂÅtá|ê\x0001\x001fH\x00189e!8O\x0010\x001e­£+ÌXí\x000cÁEç õñÚsÁ\x0013\x0012\x000e?Ê©\x0008è2Î1g"Ð;ìÖÐJ3Î\x0007ä\x0000ò2Åvà\x0002^þÝÅ/
i.(©\x000eá"1'Ë
wØ®¥í]À]ÛP×\x0015²5xëB\x0002§ó\x0019jX`ÚV,
H\x0013¼Üÿäc\x0016gç8áilÅ`2"\x0019æ¼ûÊ{<|øålÎºm¨»éx\x0004I2\x0018Ð­kLWd9{YÊèúU\x000eË)'³
MëY.*Î\x0017'¬\x001aÃá$áú^Êµ\x001dª7¬V
ëÊRÂ\x0006övÇ\x000crEe8kû¾·$\x000crìtô`\x001dp\x0010Þ£<d:%\x000b\x001ee;:\x00190A`z;·W\x0002'bÁ\x0019\x0003Öa\ßR\x0001d4$¹\x0010chZçð"Á\x0006ÒêáEx\x0008®®ð."#ÂÙÒurxB9\x00181\x001a\x000e#Y@9\x001cÄ\x001dc0]\x000bÁ1.Kôb\x0002\x0000\x0000 \x0000IDAT·\x0014y\x000e\x0002\p\x0018ß¡uJðD\x0011\x001d¢x\x001c\x0002ãñ8b§Çc\x0000={ÆË/9~yD»ÙFRZo¤	ÖEEâÿeüúü\x0011â`vl¬ê\x0004Û9l\x00133cmpè"!-S:Ó±­7\x000có"O1m\x0014\x0011ó$.²&\x0013!{Ñ³Å(èèø\x001eõ×sîÒm{!
^d\x000b^¸Ü\x0013­IÓüÒØ¢Å[P½»³§q`q&ÞoêDãlG¤L'cvv&4UëZD\x001eÝ¹I²mª(ÊÆ\x000e36XDQ\x0008ÜÖ¬¶\x001bÎf3®=2!¢#^ËYmú\x000cÉVIoÐ\x000c\x0012Äv<Ë)tëÉy9&\x0017ÅrI6T\x0014Ã1¬èfÓ±Z4t&:Ã²4Á%\x0016\x0008¤öÑÁôÙr	D\x0018Úr$<R\x0007D
*Oá-
O1JP\x0007\x0019¦\x0015ÔÀ¶î0&¢@[\x001fÀV(/Ñ^ |\x0012\x000f\x0008Dçüt)\x0005Bx¤p\x0011gÓg\x001aF§Fà:ð.Á\x001bk=õFÐl\x001d'\x000fTÀf	¾`#wKÞ`& \x0010P\x0002MJAã$UãYÕ\x0006¥\x0018gH¥N-!@ø(\x0014è\x0018ÝÕÏ
¢G^z\\x0014@\x001dÐçÈyBDÏ\x000bÁDõÏ/\x001d\x0002J\x0017H¡d@#C\x0002É\x0018ð$6¡m\x001a¬Uè,æt(:ÌÆbª\x0006·m1[G»±T\x001bíÀ»ÏÃ2\x0001òB¦QÀ4ÖáÎ\x000b§£\x0006ÒÑi§tt=J\x001dÿ-º\x0007AjÌ#ÂSö¨ÍØº×\x0004gz>rl,\x000b4"\x0008´\x000f=#8þÌ,_lÌ¬Aæ´\x001bÃf\x0016è*A[;\\x001fÍ\x0015$OÊaMT ¼ÿ¦3îEm\x0010Ýiÿ}d\x0002\x0012ÑmI\ÓR	
(\x0019@\x0017\x000e!\x0002^y¼\x000c¤iÈ\x0014o
\x000fi¾÷õ¹'­k&Ã\x0012-z4n/\x000ejz1,\x0000Ø¸ Bt;	¯	N\x0012È>¬`\x0004"q}en\x0018\x0002\x0008\x0003¾\x0004\x0003¦òøuÀ\x0018X\x00088\x0003F	D8]ü4§¹DL¿Þ\x0013CàsííÿcIËL\x0005Ñÿ\x0019~6£¦Ï\x000c}>b°¨ ðnQòìÁKp0=Tä¥!({-ôH\x0012­zQßÅë¦\x0017-Aöè@qCøE\x001f.Ô\x0008¡\x001a¬w\x0011]h\x0005\x0004
B3\x001dï²\x001e[ÎÏÎéêlÒU1c&ô×¯\x0017\x0002ç\x0002Þ\x001bµt¦¡3\x0015£AÎúåQY\x0010Ð½óÇaaP\x0016l«5AÃbãhã\x0016ýlUoÉ\x0012¨=YÒ#Zì\x0006ãU\x00165qbDj\x001dÂÞE\x0015ú¼\x0004OD)?yñ17®_§ë:\x001e|ö\x0000o\x001d·nÝA·!P¤q®¢\x001c²ÙTÔÛ-¦ë°¦Ã\x0018KH$2U\x0004\x0019Ñ\x0001Þ\x0018ê.\x000e.,Úª©QåÆá\x0001ÏfsË-\x000c×m!\x0008RYðæo¡ë3\x001eÜÿ>ð\x000cRE*`w<áîíWxñò'ÏÎLoQL\x0015¤EI!=I"zü¦3åÆsz¾e¹jÙ(tkà¡g|GA\x0010\x000fRôØU\x0014JD´5¦nh¶\x0015]Ý±Ý´\x0010q¢¢\x0017î.V¼\x0017òò\x0000â=\x0004\x0017×t\x0010\x000bê\x0017â¾ì]bÑï\x001b×¥
/ã×w":ú|¯Î;!°^ô\x000eßèºÃ\x0005¬N©tÜÃTÌêÅÅµÔ45MÝ`»+2¢E»vEf\x0004ÑXhº6È2ÍîÕ1\x0007#Ê$Ø\x00157ösþÖßxAÑ2;û	ZBÛnÐ\x0017ÈÚ £P×Ëá¢x¨èÊ×½èì\x0011Ã±\x0004¸à¢\x0012Ù»î\x0014ù`p#¬Ñ¶Ðº@^\x000cÊ!ÍzNØ6\x000c)FføÎ^:\x0001Kÿzýµ/æ¿ÅÃ#¡G:\x001fQÄ²÷\x0017û¸çz\x0017\x0019íJK2­Ùn+´J(\x0005ËUDh8\x001f'·"J)
oL\x0010þ\x001aÊ\x000b\x0001¹)Z*R\x00191*©vÂ\x000e]\x0014\x0018ëé:GVÀÑÌñlvþk\x0016D\x0001öBå"c\x0018\x0017\x001d
	îø ²\x0004³\x000fÚÕàu\x0007¬\x0019èOñZd\x0005²h(Ä\x0019SQPéíL°¬S¬mðª#¸®¿	kÈtC9*SyVI|´vÇ	6k\x0019$Rz=¡(y÷ÍG÷ÿIá\x0005ÅpÉÎtKS=cÝÔ\x0014\x0019ìíI&©çÆÞÃ½\x0005V{æ\x0016\x0002-mmøæ/ÿ*O>àôèÏØ\x0019\x001d°¶\\x001d¾ÉyÛÐ$
¡\x0013N\x00163î}ù«|öòOÙ¿yH¶o9~6£H¡hàåO·l^~Ý\x0011oÝ»Ev-'xÙÎéF$;$¢Z
¤YñÊ;FûcÚÆ¡BBêF\x0008Q`dP\x001bP
ÎðdHëIF¹ ~H÷ÿPö&±egvÞ·ÓÞþ¾6úÌìL\x0016Mu(X2J\x000c	\x0016à2<5\x0004y`@3ÃaÀðÄmxà±
\x0018°\x0001{$H&ä"UeÊ¨*Éd2È&3Ú×7·;÷t»ñ`÷Èe= \x0002èÞ}ïûß}þµÖ·ü\x000fQú\x001e¹lñ\x000e¦SÉd:äàhÅé¹ál\x000e*ZPTK¾%\x001b÷P*aÙ®XU\x0016D\x0005\x001e\x00069úÆÁô Õ
\x0007w\x0014®e°¡yéêEñ\x0017Ï~Î­-ËKpóJÐ5é`ÄþékÌúHrók\x0008\x0015¡Æ'lëB­K\x000e÷\x000f0Å\x0013nnNyoScGÃ£=æ'-Î	vzwh«µPZbE Q¶"´\x000cÝ5#âÑoAÑ0?û+²hF´\x0007<ùä_rãå>»CËOßçÍ;ÅâAÖà,ÔEËÉQK,OX,\x001afÖóØ_¡p\x0015\x000b]a²WÉãßgÜ¿ÊéÞ_"}¡2 \x001cdyÖT\x000fÙ¾bï¹C´\x0001ÕS-\x0011:\x0018«'UÇÓ/AïaO-IÒ£ñ\x0005^\x0005,Ôa¨y\x000fy®é\x000fr´a¾,b
Ââ±Xãi¬Áa×«N4\x0014HmÃ<®a{¼+\\x0008O¢3 !
¢ÈàZËd#¦n\x001bfÏÐ%\x000c{D{ÚeÉAý(; ë÷Ð'N!\x000cÌ19
/\x001e}D1ódDÔí!uP/3\x001cnQ=Ïxüe\x0005·Ù\x00189Võ	Â/\x0018¥ÁA¯#ÉháhxøeËF_Ñæ-\x0016äýøo5³ÎÎÎ¨ª
­\x0014ã®_mÐï³»³Ã×¿þuîÞ½KÓ4¼ÿþûxïÏ\x0016ìlo3\x0018ô\x0003Z¨ª\x0001ØÝ
âT¹.iýné¥¨[Ã«w_ÅYKedYÆéÉ	ù­Í-ö^¼`¹X²»³\x0012¾üò\x0019Û;ÛGCÒ$a>;e>óÓ¿ú+úý«W¯¦)Î9>ùøc¾öî»¸ºFç}ÎNùüó{8ç\x000f?þ8Í\x0019&¨8¥j\x000cMkL7lET­Åz\x0018N\x0006È(x\x0014(\x0002$\x000cú)Y0\x001cRøáþ3^ý
\x000e\x000eöøÁ\x000fþoþøÿÉæ\x0016Ç'ç(¥QIÊñÑ	Î+²<§q\x0015EÐ
¥\x000cG\x0013â$£¬ÎÉ{\x0012ë\x001a\x001eùÿäOþSâ(¥®[\[$\x0011Õz\x000eÞ°.
\#X/æ¼üÒK¬V+^<ÎÇOÑ±â;ßù6q\x001c&	E±ê0_üâ\x0017lN7xõµ×À;>}Fmj&\x0013¢8î0Q	ZéL3æó\x0005ëõ\x001a!TK×\x000cû}¼\x0010åuQÒÖ5:SHïØÝÙa:R~Ð\x001aCÕ4Ä©§*
ÕW_
ýIðÒ¨ë~!£­×XWÓK#ö>æüôïÿßãôx^\x00161\x001dÓÏ\x0013ÎO\x000f)W+\x0006ý\x000c-éÄÁ}õ­­]í\x001db\x001d\x000cSÊÚQ/\x000b¤ÙØºÊÛ¯!¤â_ý'O³9\x001ae)_{ó»\x001cí?¢i\x001a¾ùÍ÷p\x000e~ú³\x000f¹wÿsò|DCÅ\x0019Ëù9ßüûÿ>wîÜáã?âù\x0017@H]ªXÅ1uSuâjE\x0012K&£>¿÷{¿C]8çéõz\x001c\x001e1ÝØ`{sßÇ;Çd:ÁwÉýý\x0003îÞ½ÃÑQ\x00100vw§\x000cú\x0013\x000e\x000eyþü\x0010­#ÞX\x001bµÞ!¥àÙ³gL&ãÎÌ\x001czh~öÓ1\x0019ÙÚÜäàèo}ç;¬×\x0005Ï=§ª[\x0006Ã!ßþÖ·yòô\x0019ÆÌ°ÖñðáCªºa4¦)wïÞåúëì½xÁõkWh§OÐ\x001föyó×I¢/\x001f?Æ!¹qý\x0006{ûÔÅ/¿r>?à|^p¾Xsç×/ÖÄi"j\x0001\x000b/\x0019ßºÍa¹¢mÖ_yné8BF\x0001\x000e\x001e¤$'í÷IÒlÐ'ÎúDqÆ`0$\x0012\x0006½\x0011ÃÁ8iëÙùgÏRW\x0015£a,ËhMÃÙìÅr5£sÒ¬Çp4f4S·
\x001bDZamCÛ\x0006¤·\x0017÷4uMY\x0014Ôë2æ«6,\x0007¥\x000eÍÏq\x0012\x0018«0.àÌÎÎN9¥*\x0019
\x0006¼tû6ÞAYV|øá¯øøÓÏPZóö;ïÐ\x001fÉ7û¦ÄPÉ³\x001eÁ\x0008©\x0000.
\x0017=Ý8Ã&I$Z
´pDò¢ß.g:0\x001d
\x0019\x000eú\x000cú½ F´MX.{kèWÕ5Mc\x0010a\x0003zÕ\x0013Ì^;¬²®¨ª¦i¨ë¾¸ ¼\`ÞÞ°ÇõkWRá:îLR\x0004s·ëºÚÛ¦f]®QqÔ\x0011I³gL7'llNY-Ïq¶F4%²Ibsk\x0013\x0019e$ý!½á\x0014+4¯¾ù6óÅÃÃC\x000fÙ\x000c\x0002\x000eÜU\ÝR­gh\x001c[\x0011ßyï½Ë\x000e)ç"¬h=È(æètÆ×¾öuî}þ\x0019Ï_<ã¯òïøÏþÉ?áï~ÿû<¸w¿ö6³#þçÿéäÑ½\x0003UÊ\x0018\x000e®*?}\x001cìMKo¼\x0012XyT/E\x0011fG'TuÉºªÉÑÃ½Ï>ãÆ­\x001bÈ4æèøþpÀÕÝk\Ý½ÊáÁ>÷Ï\x0016H\x001bñüñ!Åºâ·_f<\x001d£@¶Y­\x000b\x0016«5§g§\x000c\x0007 uÀàµ¦ÅZ\x001f\x0010Þ$	y\x0012s¼ÌxcÂ\x0017Oxûõw8zrÈë×xüåSfó%ÃþýS^¾ý2\x001eÏõ\x001b×yé¥8=>¦X®HâG\x000f\x001fÒ8Ãw¿ûm\x001e<¼Ïÿþ¿ý\x001füÓúsï£Oø¿üs¤¤Q5U½¢¬j=}ÁÛo¿ÃÝ»¯óã\x001fÿº¬\x0011RR\x0014k"­9=;§552
û¥þ¸W8h]\x0015v´\x001e¤\x0017ÔUÅÁÞ\x001eZ*½>J*²8Áµº-yòÅÌgË \x000c$¡3m½ªµd2\x001e1\x001dlQ,K\x0006½)o½þu¶&»üðÿù3v¶®èÞWYËÅ2\x0006\x0001'}Ø¨çuuC+,Æ;µ]ê)üY¦D:
ØO\x0017\x000cë^tÄ³("îÄ\x001d¼\x000f)¾\x000eù«µFIu)ÒH©°m@\x000c;\x001fÄÄ8q\x001dºØv}¦í\x0004ÿ¶
Æ\x0007\x0004m\x001d0Ö\x0005ÂK\x001cÇ´¦Aj\x0016: iÃ6
§ûû,1E	MH¦)ç\x0019ôr²~\x000fD(\x001b3ÏØ{xDÒÏL7RR%«Å$M©­Å+Ac-©YÊ;\x000eNO)­!\x001eä´¢ijÕ\x001ak\x001d©Ä!4Ò86{CFé³YAæb4¬´xU0é'\x000c³DKZo©Û¢l\x0015ÔMÜ\x00180\x001d\x000eÑJ\x0007ÑË{4Di²(¦\x001f\x001bð²µØÖÑø\x001a"·&Ð§THÿ\x0005z ªkfK¯×ØªAzK¬\x0005Öy\x001ak\x0003	I°ÓÒ\x0011umñÂ££¬?@5-MUÓT\x0015i\x0011Þ"\x0005\x0004Ö»ÐÑ§$UU²÷â\x0005Ã~^¿GÖOIâ`ÀÀ\x001a"\x0015f¶*\x0004ð4­a¶\x000cç?|ð\x0017æ{\x0015\x0004;ÙÒË2t <,fs\x001eÞÀÑáaØ>ùËËðo
¿ökÿ\x000fïmâöÞÝ\x000féÂ¦i°Æ\x0010Å	BIº¦u¦Û¡úËM·8º\x001eÎ°ß²\x0017"»\x0008D¯ \x0007	Ö¡\x000bÒ9¬1)Ç\x0010²éhWÐáWëÔt\x000eÛò\x0000Y\x0012uY\x0000îÒ¬. îû%L&¬£¶i§ßïå9q±äüü<\x0018	e i\x0015Îtõªäøøùj\x0019¼IL¬½ë´Îv¹Ë\x000fZGdIJÄ¸º
hX©\x0019æA¯GÙÔa\x000f\x0011Kü(R\x0012+^¬ôS\x0008âTácL\x0008}f\x000b \x0012xí/ñ(¸ÀF.`ó¤ÁàÉò\x0008%\x0005Þ68\x001a¤¬r\x001ehz.Â4Åªf¹p4'2\x001ea54\x001aÑH¼ñx­Qmx,^+\x0010\x001drS9¤´ÝÞXáº¼÷¶4¥¡,JyÃü¼b½\x0000_­Aàl\x0008K[ô\x0006)=Z@ÏC%aå\x0005T4Öqv¾¦ì÷QBÓ\x0010M÷èE.t\x001dÔE*J_$¥:±,tÚ\x0007tZø2 \x0004Ã¿\x0014!½¢Â\x000f©\x0015ÑIR¼¸HDz0\x0006ç-\x0006\x0017\x0014á8#ÍR´øºÀ·«°Ø²jQ0?­h«ði\x0014Pw»Ù$¤i\x0012D6k±¶{Â\x0005á¬ëTZ #Ð\x001eu\x0008(OÝ¿ì$\x00142`j÷Há±¾Å	Ò1*Ê\x0010",©íÒbÊã
B¯\x0004\x001dk|!iKÅú¬eqêiË \x0010z I 5BvÂ¬r\x0001/ªAg\x0010ç(\x000bXTÝ%]u\x001aðpQ\x0012þC^G!§UÀ	E÷Æ)º¨~\x0013"ÊF¤\x0011o|kÂ_s¶ïè%-½¼¥í÷\x0016,A\x0004\x000e
0¸

ìg·AP¾º\x001c!2Ö\x00006¥Ö\x0002»r	Å\0;3,ç0+á}\x000fS`ì\x0005ýV\x0005|¤ò]üÚ#°Ý¥+j
¢u\x0018\x0017¿Ö	#3#BZíB#ø\x001bS»K\x0010
\x001fÒ³\x0010úì\x0014\x0011n=àÌÃìè
\x001d:­ñ2ð´C\x0015\x000c\x0007\x001c\x0015¾7B\x0007\x0011ÓÉ ¬!\x001aD\x0015ù·\x0010\x0008 ë4\x0000kÀ{)ÎkÉ¢>[\x0013O½¬­
Óñå|N[¯é
\x0006,\x0017çÄiÊºª\x0019\x000eú¬W\x0015eÑ°XqõÆ\x001d«s²t\x000c.ÅØ&\x0008®e<\x001a9$|x½PìîÃÑ¢GëÁÆ\x0000E sá\x001dÂ·x×WØÖâÀ\x000b
^uc s¸®N
ÅÙê÷?ü\x0019\x001eOðÖsr|\x0002Ö³^\x0017ÜºqA¯\x001fqïTÌ¸ÒsÁr½æ|vÆr9£m-Î7\x0008\x0011\jÆ6xchËÄYFR²¬ÖÈ8EF	Oî1ØÙAù°P\.\x001aªÒs{cõÖ.Ï\x000fö\x0011cf¼rë\x0015¸Ç'~\x00171iÖ§­5½Ñ\x000e­w\x000c3K:r¦e]\x0018Î¥ª$
>\x0008ç"\kÔÄ:A\x0013áï¹\x0012ç\x0005¦v´mC½®Y\x0017\x0005Õº¤©
\x0001ÑÙ!ÅHë/¯¯_\x0007eÃï]=äÅ\x0005%$B\x0006\x0004\x0012ª\x0013ø¹\x0002ë\x0011NÐt\x000e¼ÚÂm|\x0010\x0008\x001b'±^a	\x0007\x000fG8¤KïùCi\x0014\x0018\x001b\>u]S\x0014kº
J\x001d#ÅzJ41ØÆáELgÄIÌdÓëC4Í>ÍjÆÕÝ·^}ë	òÄ°Wä)x'/{ÒBd.MéC×óxÙqÑ½\x0008Â8+QÇxLð·`@Å1¦Õ\x0008\x0015q|pÊýûû,\x000b¨ðè$\x001clËª%òáûyÑ_ÒEôBY´w\<\x0015¾ûÉ»0½Âk:¼\x0002\x0004]ª°sn	Õ\x0018Öá0Ý\x001a)\x0014­	ÍÁJ\x0007\x0017l\x0014ÉÎ	æÂ×%CÇ¤à½Å{ÛÍà®ÃÁù?!ií»$¨5Æ\x0019\x000c×]@ªÑ%+\x001dByö\x000eÏ¿òÌ²>é\x000c\x001b\x0017R-D õ\x000c©ÅÀ¡(ÝÃ\x001bEäÇHß`mËol_ac´ÅFÿa^!âÍÜÒV+l´fÕxæuè\x00132\x0006!PÊ!£\x0014|DÓ:ZÓ\x001d ¥\x000bg\x0012d8MÙX4¸Õ	®¼OÕ~Êir\x000eÅüü§{ÜÜØüzÙñ!±\x000c]4\i©Î\x0017ø\x001a\x001aë \x0017Ö#çðè\x001ey?åøÅ/QÉö¯0ÎRÚeN,¦H}ÆÁ|\x000fá\x0013ê\x00079Z¾ÂO>\qc\x001aÞ·Tç\x0005¾tÈI-+¼Y?\x0018oiÒ¾@'1iÔ D\x0012¼-M1+<ßcÙFØì:¥¯\x0011R#À\x0005SªK\x000fj\x000c)©\x0011ô¨hí'¬Û\x001f"ê\x000fèË\x0012Ñxò\x0004n\WlífLw\x0004Ï÷<üÂ°\9Ò\°»#\x0019ö\x001d¾mpu\x0013zõ*O?É\x0007	I\x000cB¶\x0001ã\x0005ï°Þuú¸%ÕçP~={Æë»í\x0011lO`<Ú)ÒÞ
Ìé\x001frr¾C\x001a­¹³ñÁð¯xcZsÅN\x0010Å\x0012+ÓK\x0016¤ö\x000bF<a±TÜ\x001aOY¨]öÏ\x0017Ä¢A;
Ú¨ÆÉ\x0016á¢Ðâ¹\x0002_"¤¤e\x0003z[\x0019Ö+NOÎ\x0018GK66`±~ÀñÓÎk¯ÿ6ßçÙ§äL=[[	m\x0019\x000f\x001euÉ\x0019Áa¼G»5­ðÙ»¤[ÿ\x0001ì\x001dªÅ'4Í)±0á5x\x0012%Ib7Å¬b½ldxz\x000b]äÚE S¸f=ÿ¨ù·ÜÝÕ<Ùó´up6{é\x00121aöD	äy\x0002\x0018oÐ\x0011³7ItÀYh¼Gy\x0014XËÕ×ÑHR·,Î
^~½GUhß0?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=áçïÀK/Ýgÿ0%ÙzÛqyuµÃÃ[8\x001bnyeÙMr|×å·»\x000e'áLb­\x001d\x0010ÓáF8+ËòFTÛé9Þ{®\x0017\x000b\x001aSSÕ ÞE¤\x0014e¶9©§tµ^¡¦\x00190²¶ëÓ÷\x0016Ð[GÛu8ïQÚ$\x0012\x0018:²\x0002d:£Ì\\x0002;¤/B\x0003î6Þàss¥ê\x0004 çËtàn_ìº¯ö
îÍ¾ïS_à:&åÐ\x0007hØ6]í\x000b1$tý§TêñTBâEJ9\x000e²\x0002</p><p>L­\x0005 #®ï\x0011>\x0012]¸1'\x0018)	ÆpûÖ­HVº®\x0013Î×;àK-M
\x0008Q£5E^\x000cóÆDôÎÑ7-Z)²¡p·¿\x0010©êH+´R9AK¤p\x0010\x0003\x001b@«Ô%¢\x00061gØ\x0006É4\x0004ä0Ûý \Òäb\x0018\x0016/1¡*eÜUë|¬iAax\x0008\x0001ðù\x001f\x001en\x0008økÕ*CP\x001bãN\x001côi\x0008+\x0002)úf#Ñt\x0006[\x000búëH¿°®Q´N³Fs)<WÞÑÛÀH*ö¤\x0006a²:hD"M.A%Ñ3(\x0006c·¾"\x00028¤¹Ò²(%h-\x0011r@4<ÖJ²ëKoúË\x0003R*\x0019ÞW\x0004#U\x0017§¸Ø\x0011U\x00175ÊßBc\x001cb1Á=T¿ÂÐ#\x001aÁò
\x0017µl/¡Ù\x0008ê&Ð$æUã$\x0010V¹Äù\x001e\x0017R/b õ+</p><p>ýï</p><p>\x0002ÉÒ×U.\x0006Ð¤\x0014á \x0012ª\b</p><p>C\x001b¢Þ)Ì\x0001\x0011<JiÐBÆ!]£R\x0001¬ÏqVÑw
õ¶O¸³\x0016E\x0011\x0002&¦Îx¤©</p><p>Á¸\x0010\x0014*`GDGP!á\x0013
hú¶\x00101¥ïHÃ¹\x0001ÏKÓÀv\x0003Í\x001azÂ2\x0006d\x0014h4^H;~íÀþ\x0016é\x0002-dØ\x001dé8Þ
¤ùRÛ-2B@T;q<<i ÜãcDx	^ ¼N\x0017\x001e)è]HâåpR¥¤©Ü}ÿdùKLÒá$ÙG»Tkd\x00103Åv'ÑÇ\x0011@(\x0007Â!dZ²R>3Ø ¸J^¸D¸\x0016%rM:÷£Îðø''Ô[8ÜSì\x001f¨&-AöxÙ\x000fiÑPr@V/»8ôà	áx5í\x0018\x001cu·eV¤þ¼\x0010ÓÅËYKQÎØ\x001f1º^±é:\´7ø@d ,ÆìMç\x0014EíÒûè¾Käà\x0003Þ\x0007¤\x000c('gkTh£´ÀÇ\x000e\x0017k\x0010r¶­%Ê
e9"¯2\x001cº\x001d\x001d(P2KÇ`H®\x0010ãà$J\x0002á®8Vê]\x0002ªÃöà\x0005A\x001aF£\x0011ªL\x0002\x0008\x0018cP\x0000¦Ô,V</p><p>\x001f5½\x0017C\x0001y\x0018±Ä\x0013b\x000c\x0000.ÅÃ´ªr¢4´Í</p><p>ðY\x000e,¯g4¶¥ÞZª<rpç\x0016:Ïxzò\x0005çWdeÎ\x001cEç%Þç\x0004ZçÏ\x001b¼ÓdzJÓÉ!1\x0016X+±ÑCtÄè\x0005¬C±bÓ]²XnX¶Ã¶ÎÆ´2»\x0011èÄ\x0018R<@\x0011IIâzì\x000c¢LiÍ\x0018\x0002¶íéêÕrÉf¹Ä;OéäÚQ 
1Ê´¶¨\x0014ñïÃgyJÈâ\x0007ÁXàCÅ\x001c-ÓU\x000bvèÞ Ð\x0018ÊQdH\x0015Q&	øm[³©7)ý)4\x0012Ai</p><p>ò2õ\x001a\x0014E)òäð9BWHíÒ>m\x0003ëMG]\x0007Ö&\x0006½\x0008 @é)\x00081#ø1ÏÏW_óÃ\x001f<ãÞ\x001dÉ·¾~7^½ÃñíWÉ¤¥«/P¬\x0008¢\x0018\x0010!O"j&\x0005BE¬KK\x0018RÚR\x0008,é¼é¾Ö\x001dpv±áÅ¥§\x0003TÈq±'"Ïp"uùL§\x0013|¬ëºíÒð*í;\Üuì&·\x001aC²t\x000fýe±÷Ð5¸C\x0004Üt¨þ\x0007ú\x0013ýðý ±1$¤·B¦õv8?vF\x0011!À%¬Á:\x0005©Á\x0012RoéÐ	°i\x0003/¶¿ýÆQõÿ\x0013ÓúÊkw¹\x001bîÞ¿Dâw\x000fX1"E²;ù 	2ÇÉÉÐL+8\x001cyFãÞ5ØvKãÇÔ\x001dX!õ\x0008g5ý¶&ú56Ô¤,V\x0005\x001eë\x0011*ª^×+ÖþÅé\x001e_ULoÏQ\x0013ð¾¤(\x000e)í&h\x001avF)$¹JÝÖ+:$LD·L%X¶`<}ØòÓ\x001fý\x000bné9P§ÎÖ¼hHûà/éâÚ9®»5÷1ð.uû\x0006"^"Æ
ð¹ß"¶ý[{ ì\x001fu8ÿÉá¢²¼ù­ÃðÒYà³ç%'mÆ*ßg+3|&°YmDl
¾\x0011<zû\x0011YuD'¦ôBâm</p><p> \x0018\x0011"F61ú	\x0018%ñÝmý	tß#n~@î>¦T\x000e>zJç\x0017»´CºK:«8:Þ'ªmZ£¬§qå`=¸\x0010QÐ÷énu½²D«8\x000b\x0016ë5¶Ïyz²¦Þ\x001að±ÑH'ùèý'|¨N\x0008W°çJ°Nô,Òæ¯°ÿÒUo¢ô\x0018\x0017»Ô»À÷\x001fÿîKÄt¯\x0013qDºD¯\x0000²xÁvõSÚö\x0017L&OÉ²wâ
º\x0000>¨ô@\x001d"ãrB«*.\x0008ñXx6Px1ãì²!æ
Ûº`y¶Å4\x000e\x001d\x0002[\x0017°hVàÓ½±ó\x001eå4]\x000bR£ÍQ¹Gp-ëUGGNÎZ|\x0007e©1Âv\x001d«\x0016ïä<|mçgKÎ/Zt\\x0000=4ÖÒØïqû¾àüYËúú\x0019yvB\x0011`.Ao-aqÁöÎ¯ð£ï¿O{õ9\x000f(Ñ\x0011ãÕÒ§g»e2Q%Ù\x001b\x0017\x0018\x0013\x0008XR²0ãârÉÑmÁõzIv²e¾Wg¾_\x0011\x0002Ì§ðÒ}è¶\x0011àòyÏñ½</p><p>]Õ`ñ	4§\x001dú|IÄQ5µ­Y/=¿û»%ï¼ó\x0006-ÛÍcDèðÛnc\x0018Kd2ßËùÑ³\.#\x001eãÄ"ÂTÄµgo\x0002m\x0007×«ðï\x001d\x000fÓëøø®mØ®\x0017ìÏ'h%Y^_rçö\x0011o¿õ:ÿìý¯Ø®ãßÿ\x001eo¾ù&RJ\x000e\x000f\x000f°¶K½cRpK\x001dÑ4\x0019Þ;òÜPUÕ\x0006=çâüj<ãÎí»]ðìé\x000bög3ú®gTG\x0015ÛíO?Ys}uÉt>'jÎ.){wï³Z­È´AH¨ªã;·i««sNOOÁS*lç¹¸¸@ Ð"c³Ù¦(\x0012ç\x0012\x0016Ô9Çx4N	¡ G\x0008I^ñQ°Z7D¥ÉÊÔ%­l ªdÚÑ\x0002|°xÛa»ùÞ\x0003êí\x001ae4ËeÃ\x001füËÿ¯ýÜéeºÞaTN\x000c\x0012%S×ýû/ñ\x001f|årÉt:&&ï?Ea°®C©È'¼Ï÷þí\x000fù'ÿø\x001f	Y\x0011¾ÇÇ§_<ák_{[\x0007÷ùô\x0013¢×<zpÄÏ\x001eÿýý}6
\x0000¯¾ú*¯¿þ:ºtÖë5ÛíårI\x00100\x001axøðe¤TXëhî/!\x0004ÌfcÖë%ggk³H¥Ø¬k\x0010"%GkÒ]\x001aîÂð\\x0001(<­\x000f4Û\x0016-\x0015Fª¡'|Ãd2aÓvø¨°Ab£FÛ÷g(-Ð¤~åýôô¶e¹­yëø\x0011ßùîß¡±j6Á[Ïõâ«Ë/xåå{8kY¯\x001b\0|óÛßâ?ä\x0017\x001fü·ß~ëå9Bu¸~CØ:êÕ\x0006)\x001dm
ÁwCzU2\x0019|üÑ\x0010knßº
²å`ÿ£[÷øæ7ïrzúËÅ\x0005gçgÜ»wÛ·î$ãç ºl-Í¶æbqÅßúõ_ÃÈªéX÷×lÛíé\x0019R\x001bÜÙ%¯¿þ\x0006³é\x001eR¦Î²¬¨\x000böfc~õ×¾Ã/~ñwßý&~ú\x0019£ñºµ ¤a³iX¯Ò¶¼º¼NÃ±\x0000eYÑgÏ³¿¿ÏÕÕù|\x000e!²?3í±¸^°°Çùù9o¿õ\x0016Iê\x001c:99a»Ý$$i\x0008¥Q&¹ýÔì\x001f\x001c1Í¹¾^ðÞ/ÞÇä\x0005Æ\x0018Æ³\x0019.F>øà}¤\x0016¼ñæ¼Ó÷,/	\x0011\x000e\x0010\x0008\x0016\x0005½ë1&#DÏl<FõGõ¿üºuvvFYLg3Â ÀÛº6\x001bÚ¶\x0019Pd¶«©7\x001bº®eµZÑuM2­Åa\x0010¯\x000c}g\x0013\x001d%WdY(\x0015¹1Ø>6ãp¯)¥¤³6\x000bRãC©ÔyË,/Ùnk¦¥Þv(É\x000b\x0018O</p><p>ª*\x0019
²ªB|4\x0002)Í\x0016ÀE(\x0001%±1\x0010¡~!\x0014óù(`½Þp~q6à\x0011SB@é$ ®7k´Qì©¢J"]^\x0014\x0008îñ½u8pdR¥gÑ\x001d.°ïû*¥ÔÍ×½÷ôM÷.Í»D\x000b\x0010¬¥ë;2-©Ìh¦fDVTÜºu;wî°¿¿OYiè:\x000c§uÑ;Û¶\x0004ïÑJe9\x0007·Íö\x0012ÊôôgÏÒÔ=×5uÓ\x0012Àä\x0005*0t)%aHJé¾?H×{¼ë\x0006¤ 7ªì0[Éf½ SÉ°áEºÁg\x001c¿ô(6½ÅYKßv\lVÐ £ÅèôyýÐß\x001d§\x001cÈå¦åöí»<þùû<zõu¾ó«ïruyÆåå%¼õæ×ø¿÷øà\x000fØß?ÀyÏùÅ\x0005Ï?ã·_ãÃOßçÖÁ\x0011ËKn\x001fÞ":A×8^{ô\x0006&ÏX¬WD\x0019øäýÏ(fÃ[ûøÐ\x0011UÀ\x0007GYøèÉË\x000cë;..ÏÈt\x0012©c.\x0019f3²Ì`Û¦Ak6\x0006¡$\x0001O1.h\x001de^ñ§ÿæÏøÿ÷îÍX.¯9??eýá\x0007|ã¯³7q].iÛÞZÒ\x001c\x001dÝF\x0018È\x000b°»\x0012î\x001eßçòÅéèw¿ý6WË\x0005ëî¶±l6-Õ8Ggy2f\x001aÉáÅÓg<xù\x00116X.®\x001aÖë
³ÉlV cÆg',®\x001b¤R\x0010\x0010Q#¤FÀKÇ/!D¤í[zÛðàÁ]^{ó!\x0017ý)±÷Æ\x0015u»A)ÒY.ÑH¤TÔë³Ë3²Ê$²R\x001cìïÓljúmÇùé)§/N¦yAÝY¶£w\x001deYþÒkÖË¯[GD\x0008gJ)¤ÖD\x0010ü&ËhmC\x0002$#Dßõxç\x0010.Ü`\x000bcl·[º¡L$¼»A("óÌ Äv=A¼\x00088tå9\x0002#J+OµPÎ\x0007âðþ¬³dRÝ`\x000ecHîÞ´{	5à*½§TôÎÒÛ\x001e\x001d!W*á¥$'|ºm¸\\\x0011Ú®i8Ü£]`oÎ6Ø´öiºïùÁÏ~Æïþß Ð\x0002£%U5bq½f^Î¨fÝ[pÃ¢âáÁ\x0001\x0001O~NÝ÷0ôÍG\x0011\x0012òÔYÐ)9&2s=ëå5¢s(/\x0018\x0015q\x000el\x0014Ö[´<7¤j\x0012ÖA¥ð.`­K="ÍùÒ,Pf¶i¾±»-!\x000e=Ñ\x001e©|\x0012\x0004.Bç<\x0001@\x001aA\x001087Ì\x0011"ú¶Ö½¥·Þyú¾#S\x0005mßqzvÆt6åÁ£\x0007Æc>þø#Öë5U5¢®k\x0004)¹¯µ¾QH)©c8Î %DµÖ\x0014eysÍ«ª</p><p>5$C×ëõW(u©wü\x0006WZ7bãNL,«</p><p>d$ìmÏùÅ\x0005ÈSg\x0000\x0000 \x0000IDATÎ9¬µ\_]%2!\x001b	't|"ÐYFQ\x0014¦`TM(óLg\x0018ñqèri\x001e\x0014û\x001e©\x0014£Ñª(ÉµÁ;G×u\x0004ýåûÝ=/ïDÎ]Z\x0010¸\x0011\x000eý¿#\x001eîR{JJÁHW\x0014\x0005\x0012AÛ¶D\x001fX/ômë-]×¥Ùóì\x0010äA$z\x0011\x0002¤":</p><p>§H×YöMQ\x0014\x001c\x001c\x001c\x0010B¸é\x0008íû\x001eút/á\J0Jð£J¦ô Îé9JuÉì\x0019Ò\x0019\x0011èlsmÏ3úä%\x0012\x0015%±\x000fø>¢<\x0014R&H\x001cf5ô¹)\x0006"CÚ
ªÀ¤G\x00076@Ó&wßhlP:âCÑ2\x00012fJÅaã~9¼H\\x0011y#úýû/Á ¡1$«HÖa1¸ð(H¸²\x0000Ê\x0005\\x001fqÀ¶~\x0013°«\x0000
ø\x0006º:P£XIÉs×qÖY¤;B1Ñ(,"$CíQÒwAA\x0018¶K\x0012\x0004Ã"ýY\x000cBÁ\x0012r\x0010FD"ïÄ\x001b±\x0013K@ÝD]Óàºì´pD¿J*V KP\x000b¤Û\x0012å\x0015BÜ"\x001bjÑX\x0004i±hOjÎ¿XQ_HÜ6§ÞX\CQB5Mý2Zw¸88\x0015nP©2¥\x0004M\x0018\x0008nÐÊ\x0008\x000eCç Hâ\x0011H#0F\x0017\x001aYèKdH\x000c\x0002¡TéÃG0*¤\x001c\x001cü</p><p>"Xpu Þ8ÚFâ­@Ò\x0004ÑËHy´p)Í&Òqå r(</p><p>A+t.P&\x0006¥SêÁ/\x000bUëc}\x0019Y<´Ð¸Hî\x001d¥\x001c¦²M	Á\x0004J¹ë¨\x0014\x0010Aý0ÜNÃßÝ{7È)A(
ËN\x0018÷\x0008\x0002Z¤Ø¿:p6àEê\x0000p»\x0004aÜ
ûüòçA\x0014T:
øÚ	pñ¯bÀóí\x0004KÄ Ò\x0013e3¨à\x0003.®ïèÕ\x0006©NQmÜÓ×_\x0010m\x0006)ìð3K®¯ÿ?ÊÞì×²+¿ïû¬ag>÷Þº5E\x0016ÉfìZJÇ­H²%Er\x001cÃ\x001cäÁ@\x0007\x0007Hü\x0011±ó\x0014\x0004É×<Ø`YR«\x0015£Õ¢Ô\x0013»ÙÍ&k`
¬ª;ß3îy
yXû^vÃ6@\x001fà\x0002,\x0014Q8÷½Ö^û÷ý~?_\x001eÞ\x000bûD:ÐèDC¤z×éñ»a]H\x001d\x000e\x000b2\x0002©ýezP¨Ï¯\x0010v¦Ât
U]0Å\x0014Ó\x0019Ú¦aÃ®3XU
§çç\x001e\x001ca¶kFÃ\x0011Wçû	Mm(¶¡\x0013ªÞ\x0014´M×cV	å¯²C*¸rêÝºÿNG¡oÎÂ¶¬ËsF.¥íJð\x0016%$\x0008-B\x001f\x0017Mø­ï]"\x0008±J!À{³<K\x0019ïí1\x0007\x0001ÁÜ;\x001dC2Ê]\x001a\x000e\\x001fá¾0%x¡p\x0004\x0001Òõ8æ´\x000b"GÛ\x0014,ÎY,O"Íl6f6qÖ6¸.8ÅtßQW\x0015D,\x001f dÉÁñ1eqÆýÇ\x000f0%£cÿÊ\x0000©%ÛºCxÍvÛR5
M\x0003I²­"t²KÓÅx\x0011¡'V
h\x0019F-±«ì\x001aØÒU\x0015çK8^ÒñÄ ²\x001c¯DÀ³``	ë«/çF\x0004\x0003\x0008</p><p>á$BôõEqvÓ\x0019Vç\x000bÍª,\x0011Î\x0011ë(\x000c±û§ï\x001da3\x0016!U\wgÄQJÛz7`[TD*&R1±ÔáP(<^´ak[óh\x001fêð=ÎÑ²¨»×;´¶Ä:¾Ä-\x0004×\x0012X+P*\x0006÷f¶ªéXo\x000cem©ê\x0016GFý=U\x0019\x001aYÒº</p><p>m
P$>\x0007\x0001>ï8yqÈ\x000fÞ;dw\x0002/Ý\x0018ðúÝ\x0011W÷úû°(\x0011ºA¼ñH/I´D[K]9:Û\x0011Å1ÎY´EK]DÄÑ\x0015~ö`Íw¾óº;¬oÉRÅ8ÑªaÛt\x000c\x0006\x0019Î{\x0016%­u´½ÛÐX\x001fÏÖ÷\x0018d\x0011ö"\x0011®ï_\x0014Ð\x000cMðÿ|"¼@:|v6¸H\x001b>k\x0018öß\x000bqÑú=\x0006AkMÆ\x0008\x0017P²Þ\x0005\x001c°wá³5Î§	*\x00158\x0013\Qq\x0012£ª°<¾ÿy4ÿÜ{ÖÅáóßùw\x0017\x001b<AØ·ØK\x0003UppJ&àÆ°b\x0018m¨ÖçÔë\x0013¶.FÈØÖtÅ¢ièb[v$QS27!\x0016\x0013\x0010Á-\x001e)ñ\x0011VxÖÍÕùMD±Çxw</p><p>:§é\x0006à\x0012\x0011/$c\x001f:R­\x000fÝ®:°¶®d\x001c\x000bÄú1Ò\x001fiÅîÄñóòÇ,Ìc¦;P¶e\x0019¡O\x000c>û	¹û\x001aTå£Å\x0003¹#ºên}Âº;ÃO57¯¿E²÷</p><p>¶[¯YÖëlàzÅÙò¯Í\x001f©z{g/ñ h©mÒ»¡Oº\x0005íÇdc2\x001aáUDU\x0000\x0010÷\x001fyÜ\x001b\x000cL@U*\x0007.\x0018¤µË
®X¹\x0011\x0002E\x0000Àõ÷Ø¦.iÍ}pÏAT\x000cã\x000eoC9¹\x0016\x0006ÛK×Zè:÷\x001aDJYT«
ó«0Úq¾\x001csp¾¡Õc´Ü \x0012AÝ6¬K(AoAw%\x0003	n,Q³Ø{å÷oâºV#\x0013\x001bfÿ\x0019R\Ê_¾¿</p><p>ßÛ¼À\x000b 
èsß\x0012»\x0012ïÑm!£\x0013¢AgDã2ºÈ¢¢\x0014ãRãÛÔÛï1\x001bÆ¸¸é6t\x0014³ÙÖ|òø\x0014gcJ1VÙcQxº¶£«;-¨{{Ñ\x0005Ñu6ÏÐQW\x0002</p><p>®«£XÎ#|ëY.V\x0000AdÝ»Î\x0017ßü;ìß~ÂÃ§\x001fðìñ\x0001m\x0001¾\x000e\x0006¶ÍbËjõm°1¹ïG¹\x0011+Ewæ¨7¬Êá£§Ìv I\x0008,=Ä:Ðô§sÍÎî\x0018­6diÅõ\x001bðÒK»L¦\x0003Þÿà9ã±"JuÀáÄ#Nñ¢c2WHÖÔ\x001dLr¸2\x0011ëyT©ÅË\x00145ZÑÄ-g'\x001diÔa\x0005L{üó¯~sùxá#"7çøð½yÊ(M0u7\x001d:Ì®í|ÁO~Ú1Û½+\x001d\x0002V'\x001e\x00077r\x0012G@Gõ\x001f@FþÁ÷¿R\x0019y\x001e±3¦)ÓéG\x001fóåwÞá­·ßáàà>ú9qRÕ%GÇ,kÒ,¢(Kþã¿ý
\x001e=~ÄÙÙ\x0019J\x0014G¦ì_ÛãéóÐÿ<L\x0011´a¹XîÇR\x0014K\x001eÞ¿Ç;/#\x0005|ðÁ\x0007Üyõ5î\x001dÝçÇïÿ_zñ(¤§wwæüöoý&å\x0019ÛíuþÕ\x001fý\x0011×n\¥m\x001aæ³+(©Læ`\x0005×®]çìô\x001co,Ûmð\x001eÞ~/ÖI5ª*(\x0006ï¡1\x0016\x0015eÌv\x0004£YJ>i\x000f\x001bSãlË \x0018\x000cb²D³Únðç{ßÿ\x0011qòÛ¿ý;x¯Ð*</p><p>Ï
=nJkEÓ´Ü¹s\x0007\x000f\x001eð«_ÿ[Ôu÷ÑhÀby\x000e¢â»õ\x0017¼ûµ_ãÍ×¾Êæ|Å iÛ-§ç\x000c\x0007#î¼t'qvºäåï0\x0018\x000c\x0010B°··Ç³gÏØÛÛc±Xðá\x001fþ;\JÉ|>gº3'Is6-çç0`ÐQè\x0018´\x001dÖ\x001a\x000e\x000e\x000eX®Î\x0019\x000es¢XÓ\x001a"êºÆ4\x0001sd\\x0018ÊI©É²ÑhÒÍfËª,¨[Kå,NÏp]GU¬¹uû:ÖX&³\x0019O_qçî\x001bä£9­1Ja}Æ2Êb~üï1Î¤æ7~ã·°NôKÇ\x0017O\x0018¦</p><p>å¶\x0007·8[l¨jÁt~óuÍ\x0017Þ~{?¿ÇÉÑcâÈ£\CW¬\x0010Fb
RZ¼õ$\x0004\x000feÙàåÊî\x000eI²K6\x0010|òðg|óo¿MkÇ¬W\x001b~ô£\x001f1ß"çêÕ}ÚÖÎ¥lñ
\x0005%m×ñú\x0017Þd4Û¥3ºë°\x001e®\¿É'<BÐ2\x001eMpÎ±<?ã×ß$Rï|ç/¹wÿ>óÝ]~ïw~OîÌùùû÷?&3vç\x0001IýøÉSö÷¯ÓÔ¡7.Ïs¢(b:2Lxöé§¼öê]\x0016gçÔuÝ\x000f$a>ß¡X-ùÒ;ïðæoòã÷Èâì»wï\x0012%ívËþþ>W¯¾Ãýû÷©é|½½=væ{l6\x001b6
ÛmÉíÛ/!`¹\qãÆuNOOyñâ\x0005Wö¯òòÝ)«\x001a\x001d§¼ów9=9ç{ßÿ\x0001·n¿ÌéÙÑhÄK¯ÞåÉG\x001c\x001d\x001d\x0005EYpíú­ðÏ/\x0010>ûä!ûW®0Jbt¢ñ]EWW4åÕjÉr½¦ª*¬õ¡?ËAxÒ¨Ál\x0018\x0006ÖEÁj¹¦5\x001d::t\x0001¶Ö^R.¼\x0008)\x001bt´8ÍÈ³\x0001I\x0005¡Á\x00073gjºN².\x001a'\x000bT\x0014d\x0019ãzÆp4"I3¤ªÄ)I,5ÃlH3a­'$J	Q*A\x0008g\x001b"2L\x001d¦qH')aÅqx¦sºª\x0011$NJ¤Àç&\x001dÅè$AÅÁx*ñÄq\x0014ªz^Ó¶4m@§j\x001dÓ\x0019CU\x0005!Õ\x000b²\x0006EÆ}%D®\x0018\x000e\x0006LÇC¦ã!y1í1LÏæÆ#ò,'Nb¤=ÆP×5E±b[XcR¡ã$N\x0010@]·x\x00153ïqíV\x0007QÊÃ\x001fáÝ6¤¢â\x001e'«\x0002©G¨`æ06`UÛÖâ­Á[C¤%±</p><p>\x001dàÖ\x0018ÖuÔ¡²#\x001bL\x0019LÆ¼öÖ;ã°\x001c\x001eðìé#vg#6å<¤JàlKYWà!É&¤Y%EÈÉlHòÕ¯¾K\x0014)Þùò;ü¯ÿìñÖ[oñ\x000fÿá?àðà\x0019wïÜ"3¾ÿ\x001fògßú\x000b\x0006É'¼ NbÖ§\x0015ãÁõ²d2\x0018££Éx,NØ\x0014\x001büô:Q® v\x001c\x001c¾`¶7&Î(\x001d1È\x0007¬Ë\x0015WööX­V\x001c\x0010E	Óé\x000cP´ë4Íô\x0000k\x001dÑhHÛµt¦¦+\x000bbÐ¶5r\x0010ó?ú.¿ö·~ÒTx\x0001«³s>}òÝÝ\x0019£ÉåzAUlIó!gçGÜyùUt\x001cqv|F®\x0006Üÿð!/ß~\x001f¾ÿCÞúòÛü·ÿÍÿÀ¿üWÿ}ü\x0013Ú*B\x0002\x000c\x0015\x0006\x000eÇºjÈS6ëI>¥ÞTÐiN\x000e\x0016¬Ö[õ\x000cÆ3æ»)Åºb»*¨H*v÷wyíøéÏ>`±õÜxé\x001aÃqÆª9Gç\x0001gµ-·½Ù!$ç¤xç8_³]­UX×{Ó\x0019ÃÁ®nNñÉ'\x000fY1N´`S.\x0008PÕ\x000c\x00069£áðsïY·î¼Lã,uÛb¬\x000f/2 \x0002\x0015ý\x001c.PÎ\x0005ÃCSÕ()©mGW·¢Ek::kÐ8PZ!\x000cÄ"Âì!ÏrÒ(f6\x001aS7
'íÚ´H\x001dÄ!¡$RkVH­BR¸n1ù\x0001Ú¦%b¢(.]\x0017ê-¢8ôÏyOÀ'v!}¦²\x0008ã
I\x0012\x0013yAqº ³Q6\x0008xF \®h«³cb\x0001W§;Ì÷fÈ¦¤ê:Ã\x0011Q1îR\x001cñþ\x0007?å\x001b¿ò.QÎë7èêOØ®\x0016¤£	4
®*Ég:¥²-'ë\x0015Õ¶À\x0016'48è¼C*r\x001a)ÀØºÓÕ\x001am<{9{{WØ{\x000c\x0017ç,Ö\x000bÚ.tÙF¢®+ºÖ\x0012E\x0011º¢­\x001b¬q¨~æ\x0014DÝ¾·UÈ\x0010</p><p>È `èý}¤wxçBj±µHwñ\Jè\x001fõ\x001aï$RDDÚ#EÌEw_Ó\x0005¨5Ñáp\x0018Ò¡UÅáÑ	;Æ°\®0c8LBo­H\x0019êáÚÖçB\x001fR¡g/ÌÕº®c2ÉLfl«Õz1æ2±_7Íåõ|¿ì\x0011Îq\x001ccÊâ3èº½\x0014æ\x000b\x0015\x001cE]±Ùl¨ªb¹\x0006\x0013ÐÇ\x0010ð¥Îù>ÿ%bMääqJæÄQX¿Ò9<a\x001d+Õ±\x0019Ìd:åÊÎ.ZH¶«5+»$à±ÛË®EÝw\x0007_Ì.~~Ñ®¤D"U¨\x0000Èâ$Ì\x001d£°Fãþ\x001e"DÀõvÆbº0ß
Øó(¤A»æóÆb½C(I¬#t\x001a\x0005ã¡÷ÔmCG\x001b:t\x0007\x0003Fùmö¼\x00103e×¡¤'\x0012\x0011ÖdiF¬ux¦ïéÒ\x000bT\x00141\x001c\x000cÈz¬°q¡\x001ajS\x0014._ðA÷ÑhñNÑÕ%]å8</p><p>BÐaX\x0012E8QD@G cP\x000e\x001fÊ\x0003q8Zãñ
V	(/c@Ç8R}ÇïÅ\x0001ß\x000fq¹L[þ,ÿï\x0015\x0006/^¿ \x0014\x0002ó\x000bÊ	>ÄIÅ¨bÁ·¶¶öÔòÌS,\x0003NÒVÐ4°ÁpáYÙrT{\x0006</p><p>*!°}GäØw ÊþPØçC½ \x0017ú÷%>\x0013>\x0010ø\x0019Î-\x0014`ºKQÑ\x0018f?\x000cýèÿþÄ\x0012©\x0015H÷\x0015t\x0006íR\x0006\BøU[Ýâº\x0003<'ÐÒ®6\x001c?-8^QkêBÓuàT!\x001dÃ`¬µÇu\x0006ÛG\x0017Ýªÿ	bî»QDDèÑ %û\x001e9\x0015It,Ñ©$J¢Ð/¨{K\x000bT\x001eïU\x0010\x001aûÔHxH¦W%Âk¼SØÆ±YU,ªñtÆãm\x0008*Æ±d0bÒm\x0010c\x001dD\x001a\x0014ò¡ Ê$i\x0016\x0011¥</p><p>zT\x0002qª\x0002öR\x00110R:ÁØ¥ìÝït=nØ\x001e\x0018\x001a<MÏÒÊ TR\x0010KG\x000bÑ\x000f´¡ºè¿¯a¯ìq½\x0008.}(ª
lY¼wHï\x0011\x0004d\x0011Bj\x001c\x0002ãL\x0018¢u\x000ek>C~&ªó\x0019>´\x000fáº\x0001\x0015yt$QÊ#EpÀ_¦
/ÿqyc</p><p>Ým&d%\x0008iB£¤G«\x000eÏ9®H5@ú3bå1$Ó1¶m¡<øèÕ\x0002R-Èó\x0004\x001d+.;Ñ%½ðx!|\x0013RoJ5#}ýüiº)q¦¥ªK\x0010áAÀú14]KS-5ÝX²)[\x0016\x0007',^<ggÜºv\x0005\x0015G4Û
®V¸N£d\x0014¡oÐ]B&Ã:MRt]IÓ\x0006¾´PqØ'UÜ\x000fZ-Öv8§\x0004Ôª\x0017\x0012á%àÒrê3ä­Å!B)Ý#\\x000cMï6VYL¦¼öê\x001b¤IFÝ4l7k¬7XÓÐvmÀ¨\x0018\x00136Þ\x00041Pu\x0015r²\x0001[xá\x00062¦#ÒÙl\x0010ÕzÉ\x0017\¿±Ç8\x001b!­Á4A(Ió\x0008­4^+ªº¡,Ï9<\²3¨º,MÈÇ</p><p>\x00119ªº¢XIL'Ùnj\£SÉ|ï\x0016gG)ëCáÑI\x0010®ãÔÑ2*f©!UP\x0014r¥8?q¬$*µ8ÙÊVÆ´}ÎÅ\x0013Ö\x0010\x0012)4Î\x0014!ýÃ·Dui\x001duUQ¬·¬ÎÎi6t\x0003©°f\x0018çq=âÖ_$kµÂÓÑ\x0019÷2\x001c¦¥	ßòè$#\x0011\x0019ÚFh§q}Wlí:\x001a\x001b\x000c\x0016Ê+tÄN` í\x0004mmÂ;\x0011ZK¢HÄ	Q"¼</p><p>iðFF!ÍÔÞ\x0001£î iÃÞÝ\x001a¡CJ*\x000cÑ{g_g-e[E6ìÉ6ø
\x000c\x0016xéèLA[w(Ñ\x000eì|ï\x0004ÂI|ç\x0002:É</p><p>\x0008\x000b$Á5]5\x0006Y;¤OùàýgüÉ_Ö¼XÜÍI2P	JYLSÓÔALM³¢*)Ê\x0006`0ÊÙlêpxS!)m½£íl@÷¯\x000b¡ï"NøK)¨Ï\x00115ý}4\x0004¬Ý/\x001cö,R\x0005ôÅâ´@öh(Ùw²x\x0004^h\x001aÓ\x0012ã©mÀ\x0013E\x0004ÔR\x0007cYt,Î{Ï\x000bóÈ¿ýR}"> ¨éÓè\x0016)-Ê6äªæJ²áú\x0001Rû\x0013:\x0001ÞoÍ	\x001b\x0016~ICè(\x001aBÚ!¢\x0008í3¤5tõm§©#K#ò¬ÃëÂ)Ê\x0019E³Ãò|V	\x0004£À¨X8R0W\x001d\x0003Ñáð\x0014JRø86d]>ãÑ?'Î,f+`G2Õ\x0007\x001e@\x0011\x000bºpJ%³¤=E\x0015m-\x0019<~N\x001f±Xÿ1#m(~ÄÕgxmD²\x0005ß,Qã)¶hïì#|õ	zE<ìÈxþÁê\x0016Çëopz®XE\x000bSâAB</p><p>:@v.ôg÷®ÆÄ*>ugC|Ö+D\x001c3ïÓÊ]t1%r§äª`åt*$JÛ®¥k \x0005Zw8¿¢³àZ\x0011ÎNR#¤5-R\x0006bµ\x0002ï4ÆÀfí \x001a²8((»-ù\x0017xã_åÅ'¼tcHb\x000bü®9ÅºDåÙ*È×Þ¹å\x001c,Q>¡\x0015C6& U>3\x0002³æ/¾Â%^D8¡\x0011²E\x000b´3"w
!"´x5-¢Û%ÏöèäU÷Haº!itm5Ä
\x0006hZ4\x001eça\x0010%«uM\x001cMpÖ\x000c+n¼¤PkOÙf-:NÎZd$h½Ã</p><p>\x0018
STSnkÖëOÅÚ-N\x0018¬I>¢®-çça&ð^rt\x0006ÇÇ»ÈlÂkw¯pãÆÏØ\x001eòá\x000e¨\x000bIH<\x0006©ZS¸Úâ\x001aÁd0\x0002\x001a'\x001bþÍó÷8>jä4ò¸6tÄ@¦\x0005±½ÙÉHQUK"UsózÄ+·o0Ú½Å§þ?Hpóö
\x000e\x000f\x000f¸wI±Y°¿ðæCnÞJU\x0017Ö*â$' r¼ñÆ\x001cÆÝãÅ'+ÒH³(*\x001a£ô\x0015>zÚñÚKs\x000cg\x0014O\x0005l¥a~C3\x001dMXWglÊS³\x0011Wn\åþ£CZ\x0007Ä9V	[Ü¶Ã\x0011ú¤êø\x000f\x0001#ñ­×\x0018\x000c2ðÞ\x0012'\x0002c\x001a\x0016S\x000e\x000fS7%<çî«¯RßlùøÁÇ\x0008)xõî+<~üÕjÅþþ>eUrzzÊx<&5'''(­Iª[·nqxpÌáÑ!·oÞF£Íæ,ÎÏùw¿Æ\x0007\x001fszrÂl:fº3'õðü¯~åk,Î!ùf-uYòàÁG¤qÄo¾Îx4âÝw¿Jm;¼øÑh\x0014L`^°^­Éó\x0001Þ\x0005ô]Y\x001c2\x0018æ\¿v\x0015!%ÛÎ2ÍðÞ³^¯\x0001Ð:Áöéî(É\x0011ÊR\x0016+Î\x0016K\gq]\x00108ÔÅãI2{÷îó_þ\x0017ÿ\x0008­S	Æ°8Ò½[Ú2N(Ê5;;s\x001e<øçÏ?eïJp</p><p>Õ$øñOþÅòÿîþ8:\3ÍÆ¬/Øn\x0017ìíÍØßÝãéã\x0017\x0008RÞ}÷ë'\x0019ÿ÷ÿõÏùûï÷/»Ãööö\x0018F¤iÊùù9ÛíñxÌÞÞ\x001eyã¥¤i:6-B\x0008f³yè)1¢,"EÆÜ\x0018^g0Ì8;;c<\x001eÓv\x0016c\x001dÆÖdyNå$IF\x0014ÇÁ
¾\±Ùl\x001bZE,ù\x000eW¯_gu~ÆÑást\x0012ógßúSvöö]}[/ß%ÎF\x0008\x001fQnÖd	ÄRðüñc\x0016Ç§\x0008­íßfwç*ÏV$QÄáóçL\x0003LuÆ(õ¬\x0017ÇÔUG\x001c\x000fÍoqpxÂhpóö5\x001eü3¾øêmVg\x0007¸®ãøhÉz»f<Î\x0013\x001a
\x0008Ú¶âÑÇìÌgtäälE
xñü£Ó\x0017ìîí2M©ê¢Øð+¿ò./ßºpÁÜöþ÷¾O\x001c%l¶[®E\x0011G§çì^¹\x0014-ÆtLçsÆç\x000b\x0006!ï~å]êmA$ÌÆc¾û¿äôô»¯¾ÂÁÁS¾ÿýïñâàS\x000e\x000eNùú×\x0015\x0011iªÊôi\x0003\x001fø­agg8\x000eBÎ`0èR1;;;lVa¨w÷î]={ÆîtÆÙÑ!?úá\x000f9<8àÅgüÁïÿ>?ýéOyqøããc\x0010¼ÿþû¬×kfó9eYòÞ{ïÑÔ\x001dW®\a<\x001e³\®¹yó&·oßf±XòèÑcÞ~ûm¾ô¥/ñý\x001fü\x001füè}Þ~ûKlÅ'O\x0018OfÜ¼ý</p><p>÷\x001f>d2°XmøäñS~ý×¿ÎÍ[·ùÞ\x000fþ\x0006!á'ü¯yãÍ·(ÏßçE[\x0011ãA¶5Þ\x001brÅjuÎùâÅjMÕY\x00088Ö,IQ2"Ë\x0007DÃ	Ù goñ`H]\x0014\x001c\x001d\x001d±^¯iÛP`¬¥ë*|\x0017Î
ug0ÎÓ6>t49V\x0019i2DzM]6(éèÚº­p®EjOgklcñ[°Â¨Ü \x001a-·\x0001ýèl0b[â}G¶¿G\x0014gx\x000bUÉj\x0015ÖëñM\x0019ðlÃ8B	MÔ÷¤u]GSD2Æ6\x001e\x0013\x001bâ4\x000b=G:z\x000e\x0003ï$\x0018á9°ªMóDÇ¨8£ëZªB¡¤\x0008(~©\x0003PiÒ8\x000c4§³1£Ñ(ô&IÅ|:½DÑi-ÁP
à\x001c®«)Ö\x000bÎ\x0017KÎ+V«uèMO\x0012ò<g\x000fQ*&Nb¦ó+\x0008
'()yñì\x0019eU ¥$M\x0013T¤ÐQ«\x0018\x001bÐREÈ(%4Ø6\x0010§úNÊmQ "Å¦¬H\x0007#N%_ûõ¯p¶\#uDÓ\x001c<g6\x001fprôQªÉã\x0008åan±¬\x0019\x000eg\x0018\x000f"\x001e¢\x0001JÄÇ_|ûÛüá\x001fþ!Þ\x001a^yõ
þ÷ÿãsóÖËüòßóñ?ag2âÖ}þÍ¿ùKþâ[Ê \x001ehÁ¶l(V
Í¦c­\x000bH\x0007\x0011.ÏØNO'!õ)\x001c\x0003r6ÕÎ\x0019ñ\x0014éb\x001e?xÄë_|\x0015ë\x001b2ÕR´\x001bf1'Íª.°çÝÝk(\x0019Ñµ$\x000eµ2N\x0007D1Îi²>\x0018`#Mg[\x001c?æÍî-F;SFù¡\x0008HÐÙlÄrÑØÕzÅl6ãäøÙloÜ¡,+<yDÆÜ¹sñ/ÿ_þ·ßý?ùæ7~\x000f~zz³ÁV+FùxÊx¸ÃGO½¤«\x0005ÕÊ0N¶eíkV«\x0015E}B\x0016\x000f¸±{/ÿêWpÖóó\x000f?dw>åé§\x000f¹v{éÞd\x0008µ\\x0007ó}Û\x000fØe³ 	\x0001\x0019g\x001cåÓÓS&\x0011£|\x0018Î\x000b^`jC¹©øèç\x001f"¼g2 ¢¨¶eÁ ¸²;"Khõù\x0013ESc	Æ\x0003\x0017Ò7Ø6û±\x000evQQDøok-R)â(</p><p>ýgx4AF\x0011²ïi¬ÁY\x0013pºiB¤\x0003B?KRb\x001d1Î¸qí\x001a<¦«\x001b\x001aÓêÉVIHp\x0006\x0003´%Bô\x00045ÔªO0\x0019:¤}E\x001aôÞ\x000e\x0007Ð#\x0019[ïè	T§#êß{½.pMÃ(NÆòäGX,ÊyR©¹yõ\x001amÓ0\x000c889â|»&\x001aääùýÝ}N\x001e\x00101¢âÊÞuO\x000eààm]\x0008IÝV4mEÓ\x0014\x0010)iDhYÊ²mÁJ:ç/I\x0008ÎY¼q\x0008:JWPdN0M2ÒX'xd\x0011£QÂÉñ!mÛ)cª¤k Mô\x0002R1RKÚ.\x0018±ñ>&|?ööýçèµÏ´\x000ekCHDØÐ³%@ùõN </p><p>(i\x0011ÄØ¶3Ô¡óXGäÃ!é(\x000eF½G\x001fÓ´
ÓÙÅâóó\x0005IRWm/\x0004úK¡ì")¾Ýn©ªê2Me\x0019Ö;\x0006yÎd2¹$Sh­L&´mKUUIº(Â\x0019p±\x0000\x0008¥ÖÑu\x001dãqè^-ËÍfÃb± i\x001alÝ\x0010_\x0010Mû\x0011Q\x0000\x0000 \x0000IDAT¤¼\x0014B*0ÔB¯°ÂÛ\x0010\x0010ÑBø,4\x0011°¡a*ïúÇ_Î\x0011=¾ÓÕeÚô×í xÑ¾\x0010\x0007/:\x0007µ</p><p>\x0008bz½$h:!¤b­íû${1¿\x001fÞG=¶SII¦¡7´\x000bí%¢\x0015\x0019Ö¶u B\x001aQ+\x0015:Ü\x0007áû@\x0008VË%q`¬
¦Ï¤ïy¢¨'Sªàw\x000eg\x0002åDhpÁ ì¬Å^´¾ø=ú\x0014p¢S´a0fkkB5\¤ÁIN\x0013'¡c*É\x0014*òD)=\x0016Ð¡SûäK«°¢ÚT¥£´\x0016é=4Æ«\x0014\x0008I!zlCpO\x0014\x0008ý&¬\x0018\x0004Þ_L6za£wZ^È\x0008³¶\x0010-¸ìTò>ô\x0014:G\x0010</p><p>­Nà\x001aè¶í¹§ZÛi\x0015W¬;ÇqÓqØzÎ	\x0001½F(Òa£ö\x0017ZG\x0018îsÁ@»\x0014\x0007/Vô/¿'Ä\x0005ÎÑ^üZ!ù%]\x0000»ÀJ\x0002t®O<ø\x001eCy\x0019ã\x0013X¿Eø\x0016h\x0011\x0012"\x0011¡UÀv¶Bv\x0016ß-\x0011æ\x00088Ç7[ê³õQIyn©6º</p><p>ï]öÊ\x0012HSB`\x001aB7_/ànJ\x0001:\x0008*\x000eâBz0"$NêP|«C\x000f¡\x0015*}¢P~\x0016¤S½ (â *"Áø ´©ÅB\x0013n0¤^z\x0005t­\x0008Üe\x001b®Ñ4I¦0®FGYp\x001cC:D9Ä@ç\x00028H\x001c$ \x0006(
bfèvóÁ).\x0015Â)ÒQÎ`XóB¯)Î\x000ce»!×\x0016%]Àï*Ùc1/f\x00032VpÀ\x0008ªâ"iªD\x001e=\x0007\.F»\x0014C\x001fxFì<]í0&lÐ"T_¢|\x0012\x0013\x0002'\x0003ÒH</p><p>\x0017\x0012/\x0014BõÂ®â\x0017Dx÷KCÂK\x0001;¬¢~!ùËÐc¸´\x001dÂwàKLwHg\x0017Dn\x0013\x000b´\x0008n\x0008Rï:ºÂóì¡CZH\x0013Éh\x0012
=^ØÏpý¥\x001cv!\x0011°ÅRôÉÑ^\x0018ÿ÷\x001cþ]¯¶iú-ð</p><p>%bxg0¶¡é6Tí®+ÉùxÆþè\x000eþÖu¦IÂs¶Z§p5\x001eÐ®-)Ë
]×Ð´uÀBÈ#\x0015\x001c\x001f\x001d±-J\x001a¢EÏÕ\x0015ap\x0003I¢\x0018é-­jqÃX\x000e!C\x0004=ìy\x0006ßã\¥\x0012=w<\ÇÎC±ÙÐ5;ã«¼þú\x001bÌwvY-\x0007t¶¡,7,WÞm\x0012Nx  t¥½#Éc­ÃT5]K]w$fÿ\x001aãñóóS\x000fxåö
\x0006J±|q÷°3\x001aÒ</p><p>ÁùfÍº^2\x0018ïªij4A¢I"8>^±];\+\x0011.f4!UÇo¿Í`|G?d]\x000b\x0012¡ÈÈSN\x0015c-ÙÉ\x0014jñÖSUÕZ³\Ã¶NeMÑ¹ÐØï¥B]8«Â+B\x001e\x000bþ®ì\x0013Þ[ZÛ±]o8;]`Û\x0016%\x0005±R@pËh­©Â\x00054(\x0004ÌWè\x0016\x0001ë\x0015\x0006s\x0012OpV¥ZD\x0019HC\x001aÇ\x001e\x0015ë°&\x0008»ZJ\x0012¡I£D*\x001a<®u´Mµ\x001e­câ$êoà\x0011JÆx\x0014Æ\x0004¡Ìã(Ë\x000e©Bß­1á¦h¼À\x0012õÌ|\x0013ð6 b¥\x0011NÒ4\x0015ZÖ(\x0019\x0006\x0008BxîÞxû\x000b»Ü¾\x0016±3êH£\x001aWo\x0003:Üi;,]ß'\x001c\x000e	Ö\x001a%`\x0014uØ\x000bÚÒ1Í\x0007\x001eU¬¶LÆ\x0013ö¯Xl:ÊÆ±»3'5¢ÞàÚñ(¦tÍ¦¤é:¦³qè\x0007él°è»\x000b|8!\x000bÑKæÞôn¿J.6{}06Ø;Å/Üpùõ\x0019â"ü\x0008Deõ¤:\x0018\x0015i1Æ\x0006to\\x0010:â¢ßá¢Ð¶\x001d,BÚAAÁd¦C²ðs¾~1\x0015ù¯pðxk0Þô\x0006p®E¹LÕtÅL\x001c³ç\x001fàí\x0013LT\x0011e@gÑ4h_Sbi\x001bGë#\x0018àã\x001a+5ÆÅhñ-Ì\x0013O2R}\x0015Ä;Dú\x0015\²Kí2jiQ¦!Â!\x0018_2p\x0015cY²«[Æ¢ÄÉ²\x001c<ü\x0000¡V\y\x0002öSÜö;`Æh\x0006TMÅ\x0015ËN°YÂd.ØºbÛ1ØäåNÍùáÏÌ§dÛç§ßåYËs^Ù\x001dQ¬+\x000eï}ÈÎë·P \x0007¸&C¸\x0016-;¢aS\x001bü\x0018°5Ñà9{{[ªfløpõe÷²;åúK¯å\x0012SµHÑ¡¤Æ\x000bK@\x0008\x001b\x0004\x001a¡LÀÙ ;<Z\x000b\x0011­\x001aHP"Î4NvtÞ`EHd¸&ôôj
®\x0003ÑäDÂ¹ª7qáÌ'\x000cCÅº£®À)MSR«|'!\åj2dw_söøgÔ\x0006R\x00113t$\x0001\x00119FsÅk¯]åõ»</p><p>?ç|?å`eyx:¦æ:¦'O\tCü[/å°\x0008±2F¨\x0006éR£¸÷» ~</p><p><ÆÔ^%Îr\x0014Y <Ø!U1ÂvszÉl,hÚ\x0005\x0008Ï,ÏYkp-(\x0015c«\x0016=W\x000csÏ´ÈV±2\x0016×	¬t®ÇØKE±*Ùnk: ¤Aé\x0016Ó±ó±¢*\x000cm\x0003DQÊ¦©xòÔ³såuv®Þd>mâH&hí(A*³</p><p>c,ÞuDy\x0013ºò,E\x0019\x001c©Q8\x0017¹Î£cI\x0016KR
ÚY¼©°M\x0015y\x000c«UG]nHê\x000eg ³\x001fþè>ÇÇ-ZASCSµÜº2ìFKb\x001b#Ñ\x0018\x001cJy¼Ô8\x0006DÒòÖ\x001b¯rczJgjþæÃçÔõº¾Cªöøù£\x0003vÆ´=%[N\x000c*¹zý&ÛzKÝ\x0016$¾`~}DÇ!Û\x0012Ê\x001aT2Âë-Û\x001a¼³$I\x0015Æ}~ðþ½$étsgO?eooeQsóÆ
mEU\x0006î¦(\x0018O&Ü½Ä\x0017¾ð\x0005>ýôUÖë5£ÑG\x001eóâÅ\x000bÆã!ÛmÁf\x0013\x0010'§gìË_¾ÃÑá\x0011§§§ìLç(¥Èó\x000f\x001frpxÀW¿úUvvftmËk¯Û%S>yøï=xÀÍë×ù{ðûÐÔ%ßþó?§®+þ£oü\x001aª)¹zõ\x001aÇ§'Ö2¬
Åºäèà( \x0006Ë¦i¨ÊÍjI:ÌYÎÙò¬?;÷CD\x0015Î{\x0005!×x\x0019äC$DF1AÎÉÙ!óéùÎ\x001aþôOÿnÝä;w8?\x000f"w\x0002klÀþ(¨Ê5i\x001cÓ¶
o}ñ-îÝû4\x0008\x0001Í?ú¯|å+H\x0011!|\x00141Ûõ(\x0012ìíÍÙn</p><p>Ê¢e»ih\x0017\x001cýè	¿û»¿Ë«¯Þå½¿~óós\x001e<x@Ó´h­¸yó&7nÜÀ{Ïjµ¢i\x001aZcX®Öìì^a>á}À$=yòë7®\x0012RV°X,8>9¤,J¤LÈ²!»{ûDqLÕÔx\x0017\x000cKÕzÃrµb±Zá½'Ò	U× tÌ|¾ÇÎlÂéÑ\x0011i3\x001ch²1üÚ\x0017ÞB§\x0003\x0016«5^e\x000c\x0003-PÞñ¿þ\x001b\x0006iÎ`8ÆXèÊDEÆ\x0011Wwç|üá=\x0003O±^1_EÆcOÎA(ÊªÄé$åää\x0019ÍjI&L'\x0003F!{WfÅ*kÃÃû÷£8N,\x001f\x001fa"Ë\x001fýÑ¿f2\x0017\x0007/¸uû</p><p>\x000f?úÙtJ×uüüÃ\x000fæ´UÃp4BxÇ7¿ùM\x001e<?À¶\x000et#¢,¥5kÏÎ\x0018%\x000f\x001f>@z\x0018f9ßúÓ?ãÆk¤IÂG\x001f}ÀõëW(«\x0012­\x0014où
t¢yúé\x000bÚæ³n (çt]G\x001cÇ|ùË_f2\x001eóÞ_½Ge|üñÇ¤qÂoþæÂ_ýÕ{¼õÅ·XR\x0015\x0005ñÞ\x001e>ù²ÚòÞ{ïñäé\x0013*8Õ¯]»Æ×¾ö\x0015îÝ»\x0017Î[/ñî×ýr\x0008êãñã'¼ñæ\x0017ØÏQ:BJÉã'O±Ö²ý\x001a×îÜæ£ï1Ì\x0019\x000e&lÊ²nxéÎ+dYÎ\x0017/ÕfËl>ã\x000fþÓ?àìôçÏxúø)Q>úÜûÖd2a0\x0018`áôü¢Ø²\¯9>;e¹-h¬CG)iõæõ\x0004!\x0014:Î\x0018O'\¿~oÝf4\x0018°Y.ÉÓÅù\x0019ÛªÀðÌaLK×T\x0001ÃÛZ:ë\x0001T\x0011ÃÁQþ0	USaéú!,DQÒ):\x0011R~k$¦1XgX6m\x0014d9Np9<ÝnWhé\x0011WöHt\x0004Îç^\x0013>:ÒäyNS(­Z¢´ì}uá\x000c\x001a\x0006ï;<¢¬P\x001bÕ\x001b¤\x001cq\x0012e\x0019Ãá($¢n\x001aªº¡nÚ4\x0013\x0002)\x0015Þ9ÆÑ0g>2\x0018\x000cI8¤Ä&OSò<#\x0013>e\x0001åèýeõb Ûu\x001deYÒ45ËågÏ³ÙltL\x000f\x0018Ç\x000c\x0006Cf³9ÓÉ,¹²·C,_#\x0013\x000e){ä©k-]k1Þà\x0008ÁiÄl:	\x00185ÓÒÖ%Ûµ¡*ÃP¼¨\x001b$c[üÆoþ\x001d:Ó¡g¹^ðÁOÌîÎõù\x0011Y\x001a¡z"1&\x000c¿}@\x0005\x001acÃ°:²\x0014åõvÃßý½ß
XW¥øÉ\x0007\x001fPU\x0015ÿø\x001fÿ<ö7n°eoýÉð½ï~¯¾õ\x0016Û¢¦n\x000c«mÃª(©«º®(·\x001dmSrmÿ</p><p>giÀþeYÊp0Æ\x0008Ë|wÎº\qxrÀ|oÆ \x001d±8]róÖ>Þt$:¡i*®î%TmÇáá\x0011Ç/ÏwAÊ0\x0013Ó\x001a¥$Á¢(°¾"À+±ô\x0012ÇÿïÛÎþ{ç\x000fsóöM>þÙOñ>c2±e¦µ\x0014EËj¹f8°Ùn¹yë6q±Ù®éºÓ³\x0005Å¶àþÓÿô_ÿWüÎßý\x001d¾õí?&Í%Î[Ãcù\x000cÓ:6]	æ\x0008-5\x0018I±)qÆ3ÈrÚ¦C8ÉáÑ	Ó%ÞÁ7¿ù
¢Xr¶8fY\x0012:ÑÒyCäÔ®Á4-i\x0010ë\x0018)\x0004¦íX.\x0016´uÃt4f2\x001a3È´MK$\x0015G/xxÿ!ÉEªU\x0008«%¦kz\x0011<bÍz]ô¹÷,\x0011E¤I-\x0010$ð`òVÈ0wÔ</p><p>ë\ \x0008©`½¨¢</p><p>îû\x00100ñD\x001c}²YH\x0015P·-m×1H3T\x0016°ÂyÕO\x001f=Áv\x0006zÁÊZ7"Ìì 3]\x001fãò}çªÅõX`Aoºì\x0013M\x001ezq^Ð:é{\x0010=\x001eßµ¡\x0007qS¡:Ëîln,'\x0007lK¶¡«jv¦\x0013Û
>2<yö\x0014\x0011G¤ã\x0011£á³SÖ«
iÓº5ÒEd1×¢(VMMÒ¾U"±UH
ÉHç)ÃaFT\x0016ÔÖ"TDÜ§\x0011\x000e¥k
ÒB¢"òÑùdÈ0ð¶Á;Åp¦;ø¶b³Z¤1<Å;Ëj»¡j \x0003G)M¢"lÝ!½í	¾7\x0003</p><p>\x0014/\x0004²Ç\x001b\x000b\x0011:aË²\x000cVç@|ô¡ÂÍ\x0018Ûwo\x0019±Ö\x0004¼mÓ´ýwfiM±MQPT%³9ic½§¨*:kÃ¬²?C\ £C× \x000e=\x0002:MÃü«iëÌóË=\x001b MÓË¾½¾¾(HÓªªhêÅbÑ÷Ç\x001e#¥¤,Kâ8¦(</p><p>\x0016Åå¿¥´F\x0018\x0013lÛÂ#\x00108ï0ÎQ·-ãáHÇø¾Q¢Bjð¢ÞÍ\x0005"íëe\x001cÍvC¤4nÔâ;\x000b>ô\x0006Ó\x000bR\x0006\x0014îÅg  ¢ËTn\x0010ÑdHôö´«®ëÂ¬Ê\x00074±µ\x0016!R</p><p>Ý\x000bæJªËO\x001cÅ\x0001U\x001b\x0005\x0001ÒtÝåéº6\x0001\x00108Â¹ J3¤8ïÙ\x0016\x0005uÕçp/·4
\x0001\x0016ijd\x0012]v\x0008×mH&â\\x0008:õÚi[j\x0017ª\x0000\x0008}\x0000y\x0011'IH(ãÑÖ(ªMDy.0EØ\x0007dâ@7èØ\x0013Ç\x0010¥\x000e	d\x000ej \x0012\x0008DäÑ±EG\x0002­Ã\x0010Ï[ËÌæl\x00175«3KÓ: #R\/"iu!4I¬aàg</p><p>Ð"\x0008\x0007\x0006\x0019¸>ÆÁöâ\?Ô}\x0012\x0004ÛÅlPû:ï\x0002ÊÉw 7\x001eWDtçíâ\x0010êuH\x000e-¶Î³è<¡²\x0017¶\x0016N6\x00057ó¦q</p><p>]\x0017ÒsaÅ\x0007w¸\x0016á\x0001O)H¦äe¡æ\x0005qBª ²¢\x0002öKÈ( Üe¹)A¾\x0012ýÆî<8N$¨\x0008§tÀU)bZ$ÖOÁ\x000eeÖ\x000eì1Ê/eMW\x0018Ü"¢9Y?/(Ð4ábL\x0013ö0Ì`w (Ê\x0016c"\ÏFÊr\x0010;d*QC%\x001e</p><p>T\x0012>\x0007-5RÆxbhðG\x000e%2áÔ\x0012¥5J¤S\x001e¯%.\x001ec!µ-±÷D.Áy1
"¶\x0018¿Fã(Î\x001dg÷ZÄVÓÖ¦¶8\x0007Ã`4R$QêÙsNöÁ¼L"ò\x00189rÄáS=*\x0005R\x000fC a\x0018¥ £À+¥#\x001a\x0019vsE>Î9ù¤àðÅ¹
Â	\x0012¥ÃI$m× µEÄ\x001e)/\x0006Å!ú-Â;s\x001dh\x0013ôOÕk²ÿs/.\x000b\x0007Z;LÛ"Øµ¡Û8ºuÄùRQ×Ø\x0006®·²Àüõ²%ö\x0010\x000bp</p><p>Ú(Á)Ó§\x001d\x0013à¢;MºÐ}°xaz7\x0006áBµ\x0008<²Ó@8ã\x0005JZºú\x001c/×(\x0019apZ\x000fZ\x000bºbEª\x0013Î_HNï{d©ÈÆd´´Á+âþ\x001dh\x0015*êÍ\x0001J c\x0017á\x0000¤µþÜ\x0007)l@¯ØÚáÛ\x0004Ì\x0008g5ÆVtjÍ¦®x¶\â½"Ò\x000bÊÍ\x0019ÁéxÈ#êªCXÓ¢¼$r$É\x0013M]¯hº®Qt]\x0010d¼u¼ùÖ]^\x001c<f<\x001aãL3-N´\x0018'P&b¼÷ëQ#2ÍÓógÄ\x0001æ\x000c]	B&\x001e#:\x001aÑâÂN\x0017Êã{t@!}05<ùä)/Ý|ª¬)·\x001b,eMP2¦ë\x001ajÛ»w<ÖY\x001aÓ\x0004\x0010ýÅ\x0005"\x0012(ï1&ôÉum\x0007®#\x0006Ü¾9 ³»dÂòÆµkqÂû÷xewÂFzêÓ-ÑtÌzuD*Ã æÊxÄ,\x001aprpUÖ®Z­`
ùÂë_$\x001bîð­ï|õ²KF·I}Nc +¦© $BÇ¬ª§ËO7\x0015\x000b/hâìªDL,âPªë\pcë âá=Æy$-R:D^ÒÕm±e[ÔeëL@÷ú°¯*©´F(GÑ¡\x00106</p><p>ô\x0012­sPlk\x0007RÑ:Gk\x001a\x0004Ø\x0006<s\x0016\x0000-d$Sb«1Ö£DD¬Ákµ\x001e4DY\x000fôðð¥c¢8\x00054íH/©kÛ\x001fÎÁ\x000bu\x0011ÆÖX\x0002¦TF!Ùçz§@¡x\x000bw(] °üÚ×cþÁv½Cú\x0005ÂkCW¬bo­ï±È@¿Ò\x001d Az°Àj¨\x0017
Ê¸ÿ±7ë-KÏó5ì)vL9y¨¹«NwUusj²É¦)R´\x0004Ã`ÀMûNþ\x000f¶/\x0005È¾1\x000cñÆðGY7¦i\x000beE&{,v7Éî:UÕUg\x001er9ö´&_¬YMË0*À2OFf¬ý­µ¿÷{D:Î¶sÆcÏÕ+g\x001b\x0003tª¢/)e`2ÌYl\x001asdYNUG¤QÛ\
qÌærZ}´\x0001¬§Ç&Äö\x0018\x0006Íå¾t@²Æál\x0014s¢\x001bJ\6\x0019Ò,ºÃ\x0011\x0012ïâÍÊ¢\x0014Ü¸x#\x0001\x0017\x0002Êõ®I	UÛ \x0007g\x0019\x00149Y"ÀÅ\x0006\x0017\x001e¯\x0003¦£jáªuqÊæ\x000b?úAìJèÏ3B\x0004°\x0016c\x001bð\x0016¡\x0005:	`PaÍ ÝRê-?GTÏñêA\x0001\x001c¬\x0019àD[ËJÀE§	2!¨8â|ÌVtV\x0012lJÃ\x0018«\x000fðò]¼ÿ%\x001c·ðºÄÉ\x000e\x0018`</p><p>4I¼¡2k\ Ý\x001a!H±b8¨ØK¾Ëëßþå/\x0011¶\x001dËsË³G3B=g 5WËÃ/ßæñó\x0017lzÇw\x001foðÙ1ì_¿Ë\x000f`ñÓC</p><p>1`µê8±GÜ¸\x0015írÀ£o=åîvÉÛ_{\x001fï\x0012¤È&Ä¯×aF C2b	\x0006ªÅ¥?${ý\x00017\x000e=¯Ý\x0011ÜÿdÊþµLF)«ªÂS.â©±ÇoDÔé'k"ß;</p><p>jýjù	Iû\x0018Ì­öBI\x0017ëk0@(ð¢7*N2\x0005ßÒ¹
zk!Í\x0002Y¿nñ\x000cK¨\x00163ò4Î2[\x001dSÏ@V\x0008\x0016óÀ|q$!LC\x000cì\x000c±TlÌ³³\x0005ù§?bwÿ	¯Ýë¸zuA>Þã/\x0007,Ú	\x0015haÑÄCB\x0010\x0012/LL¸\x000e²ÿ³Ã)\x0007B\x0012È(Ô>ÅàM.ü\x0000©fØî¯`ó]Î(Ó×éü\x0004ç\x0006,Ö	YØ§jÀØuK¦\x000c©\x0019\x000f\x000cFYA­[\x0014\x0019uåh³Ó%«\x0019$\x0012Z|\§BQ5
fã(\x0012@\x0007,qj:ÑçñüÑ6\x001dÎÆ)ë$\x0011ÔÝÙ6¥=»ÆÒlxóÍ7Í? n}|o½£i I\x0002\x0012ESà6lV[×`¹\x000c\x0018áØÝQ(áH Oul\x0010É\x0015YRá8¡6<û÷?âø_}ÄË\x00175"É¯:T\x0002Ó1e±Ïp øég8;\x0013|ãëû¼ýÊ\x001d¤öx8ÛB*\x0010i@t\x0019ÙpÀ¤ñ\x0004i¸v½ã0ý9^¼37Ø.óáÇ\x000b®¦/¸vàÙß,×kvê½½W×Rm&»äCØl¡±r2bo¯ ÕX\x0013ûå °m¾xÕ*! ©\x001aC%\»vºn*ÁûÀÞ~\x0007\x001fïiÚ</p><p>¥à/þòÌf3\x0010\¿v¦©yÿý¯rçÎ\x001dNOxöô%I¡u<û1_,\x0019%y>¤j+¤\x0010Ü½sÓÓ\x0013L»¯¿Î+Wp@9\x0008Ïf»æÖÝ;lª
w_»MçjÊQÆºóüè9¿ô¿\x0018s©ò\x0001wö\x000fyþô\x0019×\x000e¯rëê
\x001eþô\x0001çÇ§\x001e)Áõ[7ÈËº®ðÀr>Ãñ%t\x0016Ïjit¥¤EÔ\x0019Æ\x0006Z\x001bpÖÊºõ\x001dsóÖ
7<ö£'\x000føÿà?¤ âÕ«%]gi\x001a±\x0002\x0013DMcÖX? øñ\x0015\x000ev7<yôwß}AðÁw? XÅ»ï|ã\x0015;£	ÆnØT\x000bê&\x0007¶µÆ9£á¢ÈªãÊÕë|ôÉg¬Ö\x0015;»\x0007\x0014\x0011W\x000cÉxBÛ´q@\x0008^<{J§\¿qAYbmM]7Ìæs¦;%O<¤ëÚxï«\x0015JI$e0Þa»m8/PZ³ÝÖtÆ\x0002,/ÐYÉ«S¦Ó\x001dòÁÊxH¨6Kf\x00153Ü¾{oû;8§¹}ë-&ã+Ô.î§L£EM\x0008[6Û%§«5i¹ÃÞý\x001a?¾ÿSºº¦[W¤¾co<b»<\x0003kHe\x0006R0Ê4çó\x0013NgK^}íu=}L×ÖdZaZ\¹F¢\x0012tV"á `Û<áù\x0007\x000cR	Òñþ×Þ$ËS\x001e=z\x001797o¼\x0002òÖXkhê§\x000f\x001esýúU\x000e¦{<|øQm¶\x001c\x001eî£\x0004\½~+¯¿	:ãäô@àäü\x000fÿê/\x0019d\x0019£²D'ÑpÄÑlÚßúßÿ½ÿëW®ó¯ÿ"ôGÀj¾¦È2NOÏcóPÆøñhV	ù,Ëxû­·ØLyðà\x0001®k\x001c\x001eâ¡®+þøþ/Þÿ}~û·þ\x0006ÿÃ÷ß\x00120Ì\x0017gÍgà/gøÞråÊ\x0015Æ)|ú)uì\x001f\x001c2(Glë4Iú¾BÆþÞ.õÃ½\x001döv\x0011G6¼µ\x001d¦áÉgL¦SF£1ÇÇ§dÙ &iÁÙ|I1Ù£\x0018üôé)åÙÛWv\x0019\x0015)ÿÆ7¾É¶ª8:=ýÂuk4\x001aáãüüõzÉzS³ijëM\x0014\x0007³\x001c\x000eH²\x0012­Át\x000e\x0017\x0002y1äÊ«Ü½{×nH\x0001ÎQ7H\x0011\x0018t^tS\x0004\x001f{6Ö\x0006:ë@E\x0007âp8&M\x0012l×²Z,â\x0000\x0008è4'W"ô¹R}ÃÕ]tè\x0000c\x001dÎwTÛè,ÐYFe@ÜdYgQ9 Ï\x0012L\x000b*ÑÃ\x0002ç=]×±³»Ck¦£\x0001y*X':ö£´\x0004D'B?(Þ'+`é3X
iÐ¶\x001dÎÅ\x0006h¦Xk	Þ"eX$Ñ \x0004E1ä`oÉý]å4I/@JÞtuÖõÙ\æ²\x0019m­e³ÙÄÿ?|î\x0010ÑIBQä\x0014EÆr9g¾Xõîz³Áu-¶m\x0018ÆäyÁáþ!Y1L9??åôüÅbÎ¦ÞRU[\x0010\x001c\x001cî3\x000c\x0019å\x0012oZ\x0016«\x0019«ÕÕjMg\x0003óåÑd³Å÷ßû÷É££\x0019"ã¯þê\x0001o¾~G\x000f?¡Ú¬xåÖUí\x0008¾ëÝë
:Éhê:\x000eq;OÛ´$iÁµk×xï½÷xðà3^ãUþÙÿùð»¿û\x000fiª%ÒI^¹{oýÉ\x001fóÁw¾ÍWÞ~¶1ìGÏììî2ßÔ¬ÑMYo7`8==î\x0007ã\x0003Ã²ùTÃ\x001cibîÞtÙÙ\x001c×yöÆûdª$S-­­\x0019æ\x0005ÍrNdÜ¸¢Y¬çÏHÒ}¤¹ ª¼RF2\x0005ë|\x00145ú¬ô?ÿÁ\x0007Ü{í\x001dN\x001d³xÀfu/\x0019M§ÅéØrtzÎx2æì|Ég\x001eróÖm1«ÅYD
v
÷ïßçÛßþ6çïþ;¼xñ?¦5\x0006\x0011,N ÛR¯k\x000enÜb:\x001aSW5O\x001e>C&\x001a×zÎNç¨¾vv#\x0004É/þÒÏszvÂo¿ÎùæÃ\x001b´´8\x0019{Ö\x001bÒ>2&KR´RØÎpr|LµÙ2\x00198ØÛ\x0007\x001f0mKY\x000cxüð\x0011\x001f<dTÆ\x0001@¤ÚlpÆ1\x0019î0\x001eA£DÆéÉ\x0019?ýøì\x000b×¬¤Èq> ôóÛE\x001dÐR\x00179\x000eP</p><p>ß5\x0017'!\x0004ÆY|?\x0010h\x0003"¢\x0018µCÉ±\x001c½hRm+´ÌÎÏyñô)óó\x0019¤IÌ&K5A\x0008¬w(¯ÐYzéÆÒZE\x0007í]*¡è£Î\x0018\x0002\x0001¥uß³ÐØ^\x0010\x0013Z!zt«µ&¢\x0018\x0004Ót<ÁÇOÉµÆ45i?l¯B\x0018¨MéjfÛ5.Àr¾@¢è\x001aCY\x0008^ðá\x001fsûÎ
VÕÖ»>æ*#µ\x0003¨V8\x001f¾#5fÏtwv±¥ó\x0002©\x00129u\x0004\x0017?VheÎþîÉ"Iñ¾Åµæ	y*Ø\x001d\x000fIe¬­i¤½ãr¾À\x0008ë¢8*$ÉÈdÌ7Þb}ÌÄ{|\x0000©£k¬,5BT8\x0017%EYD£\x0011Á!ÁXI×9\x0001'\x0005V@ÛY:kqÁc¬eSU\x0008\x0019ãyº®ßÖ\x001c\x001c\x001ceÉ¥ãO¡\x0008ýµî{³U×8`-d\x001cjõ</È²®3\x0018³à|6c±X\x0010B¸DÇu"þ°Ø¶-Þ9ªªby\x000fsw\x0000\x0000 \x0000IDAT±X°Z­Øl6h­£\x0008ª\x0014ÆKç¡R*¢pM/+>ÐÅ^±\x0006¡5*Ñ¸¶îÌ\x0010÷Lí©cÂ[B/h#\x0005ÆÄaj¹Bù\x0018Gcm4k\ ö/\x0006j/â.¾\x000b\x001cjÌÛ=ko]Ì\x0001uDéË!ð­Àç$·¨QÅ\x001a\x001a
%I.ëMC("&IB¢4å`\x0010±æ*æûi­é¹\x0014äÖbî°\x001c\x000crBðlVë\x0001Û×\x0011k,Y^D×°}P¥5µíÉu!h\x001d3M¡©+´·zcØ®<ÁAÐ\x0001C	\x0014t.Ð\x0003â³\x000c¨A\x0014_dÊeÞÔªwdÅEï\x000e\vmi·\x000eÛÖ\x0008¥z[2{\x0008\x001eMDq`\x00036xb>\x0017±+èû¼5ÑóþÜ? ìÍOã¢\x0002\x0002áL×\x0016h\x000bº¥`{ÖPÍ\x0004Ý:`\x001ah[Ac\x0002]ð1&ÑäÆ¸°ÖÆÒ\x0010 õáÒ¥Öþ \x0013\x001cQ\x0013\x000b¾(\x000b~\x0006F\x0010cU¥\x0001Ð¢Ï ü\x001cý\x0014/\x0002c\x001cAÅI\x001e4\x0008¯\x0010¤ètH-AtH#Õ>R\x001cÐ5\x0002oZ\x0006Aá 3tvÖ²97TKO×ö.\x000c\x00113ËR\x0005Y\x0012\x000fÎZ\x000b8Ô¥ÃSöù*
¨, Ó8á-û§¾È"T \x001c:\x001f#ûõ#¤@+Ý[q\x0015^I</p><p>ý¯Q¼RÂ¡¼Cx\x000f	Ö\x001aëðÁÒ­+¶³(ìúVc»\x0018²®u\ñº4H\x0015ð½Ø&tï^L#F4¤>ªgY4 Ò\x0010\x001d¢Iÿú4$Ä\x0005H%eS\x0016Ý§Öä#VqýE7ad\x0010\x000bé2¢c¥¸@ÐÆ¦a¡zbl\x00148\x0004\x0011\x001f(Cd)_f\x0018èâdNh@4P­\x0002®Mó\x0018_ëP!6´pib­f©\x0008Ò÷îÔXÐÄÅG\æ\x0015þìób-\x001eÚ[åS÷\x0002j¢#\x0008\x0011£/e\x0008T</p><p>ÂZqò f;o\x0011¾`2IÈ\x0007\x00152í¯\x0014\x000f\x0004y \x0015ZôÏè>x-û/öÐ*Ör0 K\x000b:E\x0008ó
M·¥Ñ#Zc\x0011Á\x0013T.`ê\x0006k:Ë\x000cÐ´¦cÛÄ\x0006·\x0002a=]M*\x0010 eº«éº
R\x0006ö÷÷h*	Bx\°t8w¸Îb[\x0013n[S\x0014\x0019yôkÚP·[2\x0015\x000f\x0001¡ÿ\c\x001bõ(©£kVD÷s¬\x001bÆ´\x001c\x001c3\x001ehûpi! ÈX#$c2Ñ´Moç£»S^l®^à{'w\x000fq¶Åà-Îùø¾H\x0019'ãî[¬ÏÏXÍgìÜ½É Ê0G)0¸u¼¤ÆYÜÝåéé	ÞzÒ4e¸{ë5ù>ßýî}>]Ð\x0008E1\x0000)"h¤´½­\x0014­óTmÇéªáhÙ0¯\x0003\x000f \x001dA</p><p>¼Ô>kPÉR¹\x00001¯SJ\x0010^à­A8¨\x001aGW\x001b¶Û¦©ã¦OÌÁ\x0010Ë?\x0010ss!âð$\x0017q×s\x0008¢\x0013Ñä)ÖF'¦÷\x001eá®êè÷ï}n\x0017è ã\x0017ªßè}\x001c\x0011)\x001014X\x0012ß8¡µÖ\x0018\x0005B¬E¢pÞb}\x001c~qAÅ<\x0002\x001f'ø\x000fñ (\gðö\x0014\x0019\x001atrÎ½w&üí¿ý:_z3\x0003û\x0012-¶\x0008_#¤\x0003dÄc{â$Pü\x000b\x000f\x000c_ïk°\x0002á.òû<¦6:æÃ\x0006çÉ²¼\x0008P¡`µ]ãìLK</p><p>áÙÖu\x0014pûé)ÓyTâHt³\x001dRÐã1"Zóâð{\x000f=/ î±Q\x001fq\x0008©1Q\x0010LÄÙU\x0008!`\\x001c\x0014²Ö!ûéÉÐ\x001f#à\x001c\x0004G@]bGã\x001agÃz\x0000tÛ¢ 
ñ\x000cdBÿJ$ÍÖ\x00112I¹÷Å3\x0008/2k­·øÞ	é¥#CñI$\x001dÔ\x001b_!ÂKnN\x001djÖÉ£\x0000Yb)
Ê4`\x001ck:t[¹Ü\x000bZOð´1_V4¬\x000c8?â\x001d|þ\x0016'¼Åí\x0015æÍ\x0004ÒRwñ\x0010£</p><p>¤,PÁàÌ1ºCmÇÌô9uÐP7\x001cäK¾ñå!7o¡Úï°\7|ý7öø§ÿÛ9n\x0019¨\x0017\x0016K\x000e®ß Ù}ÿû\x0007ßçî÷¸uóW±î*÷ýO¸ç?¥\x0018xòø%¯\ýsì¢b½\x001ep>öíu\x0014mAÒÕ=\ñ¤¸ÏÝw¾Ð¶h\x0011§\x0004²]÷76\x000e#2\</p><p>ZÎ\x0018Û§Ò1²KÞtÖG,¼¡Ð²ßE\x0003^fàs\x00149\x000e
tBã\x0000³e\x0018JÊag\x000fË\x001f£í\x000bðP!ÈÖ\x0019Ù !K<­õ4ªÅ¤ËûÐB*s|wÌbQYº²A·hå\x0019\x0003WFzÏñÑ£\x0004+®0(vxãvÎHÍ1§Gé\x0019Ý a¸\x0003rXa×Í\x000b
\ã³Nó¢²WíÃþÛ7>àíCKg7üàø+Ìý4\x0011\x0014%\x0015{,¼C\x0016\x0006jÃ@ìÐÙ\x0014Î\x0008r\x0015)^)6¶EåC|ø2Ûå\x0003Rÿ}ÆùvõOHÝ1*ý
tùMLz\x0003}päëÌ\x001f<ÀºN\x0019tî8b"OR®],f3Z¯ùô©âù\x0012Ú­ÄvC¬Ø\x0010\x0012c@Þ¦^¯\x0018eç(Û"´CËxOBa^bóã\x0015>@ç!1\x0015Ò\x001e2k'\x001c§cv&;m9a%M=õÆ1N\x0014ó¸Ð ´D%\x001e]¤YKk\x0014©c|P\x0004iæI¤Dúm\x0002¾\x001fhp\x000e<\x000fpä(KI{ïxôÌ²\d4$)\x0014:uìí\x0005¤«éáöÝë¼~wJ[sÿ£¿äæÍ]ÊQN\x0008ä \x0002"\x001bBd×n±8;¢,w98\x001823Oæ\x0014cEÆ
®&[êú1[çØ?0¯O9ÈîPÈ=ð\x0019û£=vö\x0013æ+Ãl½`xà$fc}Ëá%gKX?üÂe$-ú½3¥ë\x0002BfX×"UÆl6£í:¢`P\x0014<}ö¼ÌùÑ~s[·ns|rLÛ¶<zô{÷î±³³ÝÝ½èÙ6(±\­úÆ"ÍReÉcÎÏÏì\x001f \x0007C\x001erxå*ñx\x000fª^0\x001a\x001fsxe\x000fGÏ\x001er÷µ»$EÆj½å|½¤\x000bí|ÉÙË#^<x­ZÎON)ò7_{tóòôÕfE×Y\x0006YÁp4$¥î<V%äÃ	Y9"\x001b\x000cã~l\x000cy^ê"ñ\x0008\x001a¬mÙßìðêÝÛäæOþå\x001fò\x000bï½Ã×¿ö\x000eÕº¢®1UÍùé¢|Æ/1ò\x0018ë7\x0018SÈ[\x0008?æ;oòðÉÕê³Ó\x0015ù\x0017ßç\x0017~áßd2¼\x0014m³"\x00115«í®ëX®7Ü¸r\x001f|úç¼ûå÷Y,VÜ¹u³³9O¿  Ùßßc<\x001e1É\x0012Íü|FY\x0016L§cÎNOY/f¼öÖ\x001bHéyùòiïäéâP\x0019Qt\x0019vPJcé§¬=«õ¢\x001c±Z­ÙÎæäYÁ¦n8?³ÝÔ 4ÃrÄ°\x001cspõ</p><p>ûWn#³ñ4e9{Îã§øù¯¾ËãÇOL\x000fyõÕ·É1g9Åh\x0002¡Ã·3\x0004\x001d\x000f\x001e}Fe,¿ñ\x001b¿s\x0002¡\x0012\x0006YÆÑâ	Óñ\x0008á¶<zø\x0019{;¤it7¬ÎÏXÎf\ÛÛãÇþgÔUÃõ\x001b7Lv¨ªMÛHM\x000ch;Kç\x0008=æ³\x0007/ù¯½ÅÛ÷Þb±>â[ø\x001d®^¹ÃáÁ«ì\x001e¼JviÛs´§OáZC°'\x000fpëú
º¶ãË÷ÞÁÙ.6Äê£Çè¢¤®k¼÷üóöOyë­·H\x0017/^ðî»_¡\x001c|üñÇÜ{ÿ]NÎÏXÏHµd\\x000eÙîñÙ'0\x000e\x0019\x000c\x0006=çåStR°;Ùe½®XÏÙßÛ£,\x0006|òÑÇ|çÛßæ×ý×¸}ë\x0016ø\x0007@Y\x0016GcÞ~óMæ³3V«\x0019å9ËÍ\x0002ç=Óé¢\x001c\x0017\x0005«ÕÙbÎbµ¾¦¯;Ã³\x000fïc¼ïïs2<çêá\x0001uµáG?üs\x000e\x000föØÙRmH	ÓÉ\x0008U\x000cxöâ\x0008kZ¦Ó1mç¨ÚÙÉ\x0019»û×(Ç;<~úw^¡k[\x001e¾\pþü	_ùÊ;dÅ7ßÜùÂuk¹^svzFÛ¶XÛõ\x0004\x000eE\x000f\x0011Þ£³¢\x001c1\x0018h\x001a0\x001eyíµ·¸õÊ
îÜºÅpP²]­hÕrIÓÔèTÅæ] F Ñ:E§\x0019áÝ=Fã\x0011J</p><p>¶5g'GlV+B\x0008£!ÎyºÞ ¤¢ë"	Ç¸x\x000fé[KÛÔT\x0015>\x0004AÄ±eyNY\x0016h9b:\x0019qóú5ÒDsºÙRUÕ¥»cP\x000eØÝÛÁv\x001dZy¼©Ù¬</p><p>Êñ¢ÚÐu\x000eÑ\x000f\x0007ZÛF\x0011ØK´$M3"Gõ®	Óu\x0004ïHRMY\x0014ÈáÉhDÄ!ÑpÄÞxB9()Ë\x0012èÈv DtXgé¬#\x0018·ÖE\x0007{h¦a³Y_6!6l[cØn×\x0018Óõ.î\x0015îló</p><p>k\x001aêí:\x000eá@\x0016ìL&$iÊp<¢\x001cy~ô\x001c5?_¿«q®#ØÕÙ\x0011ëÅ£ãc¶3x\x0004N¦4æ¯ã×xý7xôø	AÆ\x0007\x001f|étÈã\x0007\x001f£¥ãÎÍ+8S3È\x0012êuËv³b<\x001aâÂ¡Pit£
FcÞxó-ö\x000e\x000eyôø\x0011/_ð\x0007øÏùÏþÓÿ\x0004%!Q·¿òe>ýè'üßÿ_i·\x001bæÝ=ÚzÉk·®pºîHòa®\x0019\x0019Ûí f?¶\x001dÛíg]K9,\x0019C\x0006]A9,I«×h·¼vçuÊAÁv±e:Üç'þ</p><p>¤àÖ+wXÕKj©\x0010Ò³Z{6õóó#bBHáhB×.cµ5\x0018Ûâð¤JÓu\x001d\x000f\x001f~Ên9!ÍR®ß¾Æùd½\b;ÏááU\x0016Ë-»Ó]ªºfwoUUqÿ§\x001f3L¸zõ\x001aËÕ¯Üû2O¿à\x000fÿÅ¿àæ­\x001büÎïüGü\x0017ÿù?@	CWw\x0014ãzÕ0\x001dìP$%õÖ²·sÈ¸ÜåÑãÇ4Ûé\x0001Óé®óÔ«\x0019×o^%I\x0012f«\x0005_<¦ñ-Æ</p><p>2:q¼°$HB\x0010\x000cò5ºY®ÏfxçØîg\x0019xO¤8\x0013ñÏ=¥(Rò\Ñ4
Í¶!¸Àt¼\x0013ñ¬!a:>àÑgOøÉO°æSf¼\x0000Gtæ\x0005\x001f\x0008Î#l@e:ºzQ^üLO#\x0000Îº~-ö]ñ¾w[EwSgL<Wõ9:KAJÍDj:ïØ,WûSVuH\x0014IF×q8ç\x0011Æb\x0001!HRI¢4Îylg±JO\x0006H!1í</p><p>g,*\x0008kI|ÀØÓ\x0011Z! WvÕQU[NØÌ­A¹\x0018!3ÙÙAe)kÓpãî\x001dþê£\x000f9ÏH4ÏÈ\x0006\x00193¼<~Î4ÍÛ×_å{ßÿÁ àÍ/½ÁG?]1_V\x000có¦¨,%Ø,ì
JHc\x0006öèåóeuÊz\x0008\x000e\x001bbtÚ0\x000fìO\x0013\x000e§	< \Kc<V\x0006º.%KSv¦%£2Ò4c<Ê\x0019ä\x001aA ÝTÌ¶5q\x0008ëQÊSæ9Á¥t]MÓ\x0019
Ñ)+"ý+\x001bd'%Î</p><p>mm\x000c[ßH\x001aÕ+\x000eÁ+×ÔÆÓº½÷\x0004Zk1]t¡\x0019oÙ¬\x0004Ö41WÔE\x0011íÓO?\x0005àW^!KSºÔDÇaß¿\x0018ÜðÎÑvnf­¥ëZ¤\x0012ÔM\x000bÑµÙl.ÅA!\x0004ëõ:^m{¹V«ªâÙÓg¬æsªíív{ÕôÞ°íV z\x0013^O\x0004sÖámÔ|O\x0012Áã­Å\x0019\x000f\x0001HD¢è£j6Ti\x0012#!ø~H!He/â\x0011Ði|Ïul«\x001aA\x001c\x000cP½Ðw1°~ñº³,»\x0014\x0007/p£ÖFÃH¨>&(¡kÚË<çÐ¾2">ñÎ¥cäS4ÅüB)¢`(ÄÆÏÍ³A\x001aøèIIR\x000cK¶uÅÙì¦i±>bJ\x00030\x0018$¡ÏCïÝ½J*\x0012©\x0018$\x0019ãAIdèÞÑ(¥$Q)P±­\x000c¶j±BaLë,Ú¶°ZlY¯,\x0000Y.ñ</p><p>t*ÈrN\x0003ºè\x001cT\x0001i\x0006*ØFzT\x0002IÚ3YSì³ì\x0014Á ÅO5¦²4\x0015®£³\x0001#àÂ.ç\x0003p\x001eÑ~Ò\x001fp\b=®« û§\x0002¤XB¥2\x0006Ì\x0006$Á	Sà%Á\x0008lmè¶ö$°>1\x001eY¶30[p
ø.@UK\x0004\x0014\x001a\x0002\x001a+X;¨êÎ
\x0008IBç:²$\x0016ðx!\x0011þ\x000cbôgD¸\x001c#âÉùt¡w\x000föMØ\x001dA(æà#BOÈØ\x000c×qjUëL\x0017èt\x0003Bhqnµ1«H)P"AK7\x0016ßÖ¸MÙZêuÇì4NIwÝÅ\x0017°Y\x00166! 3\x0006ëB¯Úú\x001eS©P M MCD¦\x001e>0</p><p>\x001d2± -º\x0010¨B¡Ó~\x0008_\x0004\x0012!PþâûÌd/¢mV\x0013ÐRF1\x0011±IlCxIµ²ÌO[­ «C?Ò#D\x000c</p><p>ï.¸¯\x0010\x0007ÿIÒ¸\x000eõÅk¾\x0010:³Î>Çoj-úß÷\x0017±v\x0004åQ2æ¥eIÆx8`o?>æô¨AÀî¨ Q£(¦iqú\x0002¡ìó\x0008%\x0002\x0011¸½A\x0014\x0011J\x0010\x001a¯ClÜJ\x0013\x0005:ç\x0010VQV\x0012\x001a«\x000cnÕá»@\x001d`\x0005dÚ²Ñ+z÷¤p\x001aÏQ¢½\x0010/~fm</p><p>>Çô~¾^ã¯Aø~e¸^BèÅÎÏÅn!8\x0001!ÅÖ#>¹?§®\x0002£¡d²£/×óôÑ±à	uÇ)>ÇÒ\x0007ö*ù¯¡÷þÿ\x001eR\x0019¤4\x0018Wãz<!\x0002\x001f\x0004J¦à\x0015¦í°8d®"öÈFgñ \x001cö¶{X®æ\x0008§°­a²³O&4]K¢KðÚ\x0004&o;;\x0013®Îb0<\x0011\x001fë\x0016ö`{\x0017µ`Ó\x0019®è\x0003\x0006yÆ²Þ(í*t*"ÖÎ\x001bpàxXDt>Ðc\x0011c
¯Ï9:?b¸S"T ó\x001d"\x0007$iª	!Ã\x0018C¢\x0012Ò$#m\x001aVÕÎX¬é.\x000fJ\x0006Ú\x0010\x001b®J)\\x001f«´¦m\x001dUÓòlµ¢¸rr<áåÙ9×¾ô\x0016å`ÌºÛR¤C\x000e&\x0019û·o!ê\x0005´+\x000e÷G-glk\x0016×orëÖ+|ï;\x001fòáýG¤ãC2\x0012+Ð\x001a\x0004ñpNif];¶ëÓÅó¥iãÆ)BÉ\x0010]>nÔ</p><p>\x001dk}\x001f<,@"ãpCg±e½¬p­£k[sqÿ\x0010ýÇön\x0014.\x0004ÁÞæé7fGP\x001aï\x0004ÒGáÀ%Ê4@/þõ_\x0001H\x001dýG¦\x0019ý°w\x001e\ÌÚ\x0011JG\x0007yïÎ¨\x001fµ.²Ú«àc\x001dW"Ð\x0018Û\x000f DÔØ8mlÃá£³I.4ÓÉR²7ØðË_/}iL-Púà+µ\x0004\x0017\x001dÍ\x0017¹\x000c\x001e­<A¸8óù\x0018Aü\x001eGäãÔ±Ðu\x001ecAÈïîì3ª\x000cÖU\x0004\x00110Î¤9RklWS×\x0006¦\x0010ÊÞyP\x001e©/¹øUEï\x0016\x0014¢w</p><p>öµ æ¨ø¼A`GØ\x0000Q\x0002|phÐÕ\x0001|~\x0003\x0004ãÌå\x0004ïÝAH\x0005ácí²?©Å-Q</p><p>û\x0016!Õ\x0003\x0002M¬)Í\x000e8ÖV\x0010/\³\x00141WB\x0005\x000c\x0011ë ã©Dõ\x0017\x0007øziqÖ°ö\x001dÁ¶XaiBÆ¸ÈØ©7\x0004¯ÙÝÑ@q/c®J6Dø\x001d\x0002ED\x000cû\x0006\x001f:¼mèL\x0013Ãê\x0001B¨ºµOhE\x0013\x0011#¤ÞZr:´¬I
©<co§Å5ÏÙzR·b28åêAäã\x001a)áµ»wøùw\x0003ßú³8Ü$<?}Èkoÿ\x001dv'k´*\x0019MjÑU8¸2 ksf§\x000bÆbÉ«¯¼Ïúø\x0001é¤e+NhÚ\x0019J\x0007Vs¸ÿ£Sf§\x0015÷Þû\x0005²á\x0008ÑuH*p\x001bP	!X8T¥¤YGÛUì`:ÍX=_3È\x0003ÊCâ\x0007\x00045À\x0016!V\x0008Ù\x0012sxEDó:HüT¬ðþ;´Í1JÎð¶GßÀì¤b2Ñ.Hr$9¦Õ1,Þ\x0017Z\x0011BÌ­*Ïbî©[xë
ï¢ãZôÓßxÇô0çì:¹ÃáÝ+8ûSºùGìd-÷¾V2\x001c¦\x000c¦W\x001cþ</p><p>\x001f¾Ä2Ü"Ûâ\x0002tHNÏÙ\x0015÷N¹7nXÍÏØ+\x0012l½ \x0017¢Ìq[ÉÆ*\x0012Ä\x0008Ä\x001a{¼</p><p>1»V%ÎzÁ5´ý2Ýù\x001aa\x00199õò»¼X?fÿUO6ý5~ü£¿`üö\x0008é_a9ÿDÃfc©õzÉ½·_c>Û\x0015	­ã\x0017-ÛFà¥Â$[ 1î\x001aÃò+à[\x00043lhÑ	$RbG\x0004N\x0012p\x0019|üó3OÒ\x0017¬ºõdÄØ\x0014:\xÎ÷Q¶k2	AT$¹Ä·</p><p>¼\x000e</p><p>"âM)ÏþÂØÀt/!Ks¬kâùW	²xs·®±4Æal ®<u
wïFäðÎ.l-yV"µÀ\x00058}¶&k\x0013¨\x0016\x001a³ñX±]¬xòÉÝ½+$£Ëa6!\x000c"
\x0004ó5¡ú)ÕyÅæÌ ÔÝá{õoñøÉxzô]öv÷)Ç×XÏ\x0016èÜdÉhÌÎ¤ é\x000cãó\x0015¶Ih:GY(ÒLrå\x001aüÅ§þ\x000b×­á búò4£(</p><p>ó¤:áùóç|ï{ßãæÍÇcf³\x0019ù £[u\x0018Ó1L¸sç\x000e§§§\x0018cxñüÝÝ©·X,H«W¯Ð¬Ö\x001b^P\x000erÆ£výúU>üðC\x0008ÃÃ}&\x0011''G¬×\x001b\x000e¯ÜÅZÇr¹`owÄÏÿüÏsvvÄr¹b¹\ðè³\x0007üæoþ\x0016e9ä³\x0007\x000fPiB(\x000e\x000föx÷í/óìá\x0013>øñw¸qõ\x001a¯ÜyGO2[¯îï²»\x0018±LuËélFVÐyÄ(¥ÎQd\x0019R\x0018o\x0011ÂKO¡\x0003Ðá]ËÓ'\x000fh¶\x00157o\áOþøO8;;ã\x001b¿ò
V«
Ù"f\x0008Ép8âùñ3²RQNs\x0006IÎ¶&P75B;ö\x000f¦<ö\x0013>þø/\x0011hÞ{÷k4mËt\R·\x0006Æóõt:E+EUUt¦ãàpõf\x0013\x0011­\x000f\x001f°]¯\x0019G\¹r\x0010<Ee	;¯¿3?ºÏt:áÝ÷¿Ê¦ÞðäÉ34æ»Ä¼\x0004ï¢;IJõù$tèÏS.-o\»J]7¬·5Ãá×_ù|Î|¶\x0004\x0014MgXÌfÈd@Rt\x000cG)«õgÏxíî-ÎÏÏyçÞÏqåà³³S\x000eö\x000eÙv\x001d]ÛÒmÏÙß)yùü\x0011;Ó1·oßäÇ?þ¦Þðôég\x001c\x001cL	ÎòäñC\x000eö§\x0014yóç/1ÆrppÈì|Iª\x000b®¾z\x000b©S¶a¾¨¯V´mG\x001fók¿úë¬f\x000b\x001e?yÊþÁ\x0001{û{<{vÊbyÊ\x001b7)ò\x0011¿úk¿Îf+\x0019\x0006üÅ\x000f\x001fbLÍÉéK¬5¼öê+Ü»÷6|ò	Î9>ýì\x0013Þ|ýx"%Z	æ³ènzñâ\x0005Y¢¹uã:YñüÉcîÿäCò¼ÀZË¯|ýë|ÿ[Ê¯ó×ùèþùø£ùÊ{ïòíï}\x001b·îrÿÃÑ:Ù&ôbåÖ\x0018kyòä	ÖZÞûêûL§SþôOÿwÞyçOpûæMDpü£ÿñ¿Íýë7\x0018Æ4mK¦|öð!Óé\x000eMÅ»wY­6\x0014Å¯~õ«TuMc\x001cO?ãèè%_zó->üÉO8>zÁáÁ>ãáÝý]^¾x5¯ýë$yÎ¿úö\x0007\9Øçèä\x0010bçþþ>Ãñ.³UÅöìÑxÂb¹B¨ÙÖ1yå\x001d~ðô»w®#VÝ\x0017®[«ÕÅlµ¶_ËcÒAÎpâCÄ\x0001'ù$\x001d\x0017	û»ûìï\x001dpýúU®_?`gw®®YÌg¼|IÓÔ\x000c\x000c©\x0015iÙl× \x0018SÊRë"\x001f0\x001c\x0019\x000c$\x0012\x0012-	®#Ë4Á\x0007¤tªªY.W¬KºÎà¬¿t\x0016®Ã\x0016Ù×$Ñ\x0002)â½»\x0014á d:Ý¡­6,\x0016\x000bñ!ppåÝ]\x0006E\x0008\x000egjº:\æPm·\x0015m\x0005Äg×\x0019èÈ²4:Ð$Ó\x000c%E9Bé4\x000e=\x0003£QÉt2fgáp@Yäè$öþt\x0010( eÀ\x0016Ûo/Î9¬\x000f}ÎjÄÜy©1Î^º\x001e¶Û-ççç´mû×pµ1{«C\x0008Ïd2dowRD)ÊÁñx\x001cµEtðN¤9i±3Ý%Ís\x0006ã\x0011Ëå£ã\x0017,\x0017gd©"U\x0002×np]<\x000fO%è4/qBsçõ7ù·þí¿Ë³£c¦áû\x001f|É¨dµ<Ca\x0019\x0015)Âµh\x0019(2ÍÕÝÛ\x0004ki\x001bG Eê\x000c¤¨lÀÕ[·¹yû6óåóc¾õoñ\x000fþþßç«_}\x0017ÏðÞ½w\x0010®å÷ïáøå\x000bR!\x001dc;·n³8=b4=DgAª\x0018\x000f\x000b¶uÉf³eµ\ã} í:ÎÎÏ9Í 8îÝ»±bRÒÖ\x0006ß\x0005>ùè3^\x001c½ QÍfÅ¶®xytÎ½÷Þf:LYo\x0003JÅóhgL\x0014\x0002dÊv³&Í"ÆT)EI|d)4\x0005\x001f]/ßÿá÷ùæ¯|£ç/¹}ý\x0016mc©êétkW¯qtzÆùrÉoüæo£óßûßÖ´(%Ïøòûïñs¿ðKüé·ÿüÿ\x0011ÿÕ?ü/ù{ÿñßã¿ù¯\x0017¥\x0012³
Ã´\x0000'9;1Í	¯¾FY\x000e)²!ÞJË\x0015muJg\x001dóÅÑxDÕÔ&#\x0016%¤aRÐ¹\x000eKB#¹N\x00086ö@ªÍ\x0006Ó´ÊatråQm¶<{üù|g¦Þ²ÙÔh\x0002£rÊîd\x000fÓ8\x000e÷o°:ßrûæëØ6áèÅñ\x0017®Y³XgqÂ£Ut\x0006)\x0015Å8ï¢¹ãÂÅtá|ê\x0001\x001fH\x00189e!8O\x0010\x001e­£+ÌXí\x000cÁEç õñÚsÁ\x0013\x0012\x000e?Ê©\x0008è2Î1g"Ð;ìÖÐJ3Î\x0007ä\x0000ò2Åvà\x0002^þÝÅ/</p><p>i.(©\x000eá"1'Ë</p><p>wØ®¥í]À]ÛP×\x0015²5xëB\x0002§ó\x0019jX`ÚV,</p><p>H\x0013¼Üÿäc\x0016gç8áilÅ`2"\x0019æ¼ûÊ{<|øålÎºm¨»éx\x0004I2\x0018Ð­kLWd9{YÊèúU\x000eË)'³
MëY.*Î\x0017'¬\x001aÃá$áú^Êµ\x001dª7¬V
ëÊRÂ\x0006övÇ\x000crEe8kû¾·$\x000crìtô`\x001dp\x0010Þ£<d:%\x000b\x001ee;:\x00190A`z;·W\x0002'bÁ\x0019\x0003Öa\ßR\x0001d4$¹\x0010chZçð"Á\x0006ÒêáEx\x0008®®ð."#ÂÙÒurxB9\x00181\x001a\x000e#Y@9\x001cÄ\x001dc0]\x000bÁ1.Kôb\x0002\x0000\x0000 \x0000IDAT·\x0014y\x000e\x0002\p\x0018ß¡uJðD\x0011\x001d¢x\x001c\x0002ãñ8b§Çc\x0000={ÆË/9~yD»ÙFRZo¤	ÖEEâÿeüúü\x0011â`vl¬ê\x0004Û9l\x00133cmpè"!-S:Ó±­7\x000có"O1m\x0014\x0011ó$.²&\x0013!{Ñ³Å(èèø\x001eõ×sîÒm{!</p><p>^d\x000b^¸Ü\x0013­IÓüÒØ¢Å[P½»³§q`q&ÞoêDãlG¤L'cvv&4UëZD\x001eÝ¹I²mª(ÊÆ\x000e36XDQ\x0008ÜÖ¬¶\x001bÎf3®=2!¢#^ËYmú\x000cÉVIoÐ\x000c\x0012Äv<Ë)tëÉy9&\x0017ÅrI6T\x0014Ã1¬èfÓ±Z4t&:Ã²4Á%\x0016\x0008¤öÑÁôÙr	D\x0018Úr$<R\x0007D</p><p>*Oá-</p><p>O1JP\x0007\x0019¦\x0015ÔÀ¶î0&¢@[\x001fÀV(/Ñ^ |\x0012\x000f\x0008Dçüt)\x0005Bx¤p\x0011gÓg\x001aF§Fà:ð.Á\x001bk=õFÐl\x001d'\x000fTÀf	¾`#wKÞ`& \x0010P\x0002MJAã$UãYÕ\x0006¥\x0018gH¥N-!@ø(\x0014è\x0018ÝÕÏ
¢G^z\\x0014@\x001dÐçÈyBDÏ\x000bÁDõÏ/\x001d\x0002J\x0017H¡d@#C\x0002É\x0018ð$6¡m\x001a¬Uè,æt(:ÌÆbª\x0006·m1[G»±T\x001bíÀ»ÏÃ2\x0001òB¦QÀ4ÖáÎ\x000b§£\x0006ÒÑi§tt=J\x001dÿ-º\x0007AjÌ#ÂSö¨ÍØº×\x0004gz>rl,\x000b4"\x0008´\x000f=#8þÌ,_lÌ¬Aæ´\x001bÃf\x0016è*A[;\\x001fÍ\x0015$OÊaMT ¼ÿ¦3îEm\x0010Ýiÿ}d\x0002\x0012ÑmI\ÓR	</p><p>(\x0019@\x0017\x000e!\x0002^y¼\x000c¤iÈ\x0014o
\x000fi¾÷õ¹'­k&Ã\x0012-z4n/\x000ejz1,\x0000Ø¸ Bt;	¯	N\x0012È>¬`\x0004"q}en\x0018\x0002\x0008\x0003¾\x0004\x0003¦òøuÀ\x0018X\x00088\x0003F	D8]ü4§¹DL¿Þ\x0013CàsííÿcIËL\x0005Ñÿ\x0019~6£¦Ï\x000c}>b°¨ ðnQòìÁKp0=Tä¥!({-ôH\x0012­zQßÅë¦\x0017-Aöè@qCøE\x001f.Ô\x0008¡\x001a¬w\x0011]h\x0005\x0004
B3\x001dï²\x001e[ÎÏÎéêlÒU1c&ô×¯\x0017\x0002ç\x0002Þ\x001bµt¦¡3\x0015£AÎúåQY\x0010Ð½óÇaaP\x0016l«5AÃbãhã\x0016ýlUoÉ\x0012¨=YÒ#Zì\x0006ãU\x00165qbDj\x001dÂÞE\x0015ú¼\x0004OD)?yñ17®_§ë:\x001e|ö\x0000o\x001d·nÝA·!P¤q®¢\x001c²ÙTÔÛ-¦ë°¦Ã\x0018KH$2U\x0004\x0019Ñ\x0001Þ\x0018ê.\x000e.,Úª©QåÆá\x0001ÏfsË-\x000c×m!\x0008RYðæo¡ë3\x001eÜÿ>ð\x000cRE*`w<áîíWxñò'ÏÎLoQL\x0015¤EI!=I"zü¦3åÆsz¾e¹jÙ(tkà¡g|GA\x0010\x000fRôØU\x0014JD´5¦nh¶\x0015]Ý±Ý´\x0010q¢¢\x0017î.V¼\x0017òò\x0000â=\x0004\x0017×t\x0010\x000bê\x0017â¾ì]bÑï\x001b×¥</p><p>/ã×w":ú|¯Î;!°^ô\x000eßèºÃ\x0005¬N©tÜÃTÌêÅÅµÔ45MÝ`»+2¢E»vEf\x0004ÑXhº6È2ÍîÕ1\x0007#Ê$Ø\x00157ösþÖßxAÑ2;û	ZBÛnÐ\x0017ÈÚ £P×Ëá¢x¨èÊ×½èì\x0011Ã±\x0004¸à¢\x0012Ù»î\x0014ù`p#¬Ñ¶Ðº@^\x000cÊ!ÍzNØ6\x000c)FføÎ^:\x0001Kÿzýµ/æ¿ÅÃ#¡G:\x001fQÄ²÷\x0017û¸çz\x0017\x0019íJK2­Ùn+´J(\x0005ËUDh8\x001f'·"J)</p><p>oL\x0010þ\x001aÊ\x000b\x0001¹)Z*R\x00191*©vÂ\x000e]\x0014\x0018ëé:GVÀÑÌñlvþk\x0016D\x0001öBå"c\x0018\x0017\x001d</p><p>	îø ²\x0004³\x000fÚÕàu\x0007¬\x0019èOñZd\x0005²h(Ä\x0019SQPéíL°¬S¬mðª#¸®¿	kÈtC9*SyVI|´vÇ	6k\x0019$Rz=¡(y÷ÍG÷ÿIá\x0005ÅpÉÎtKS=cÝÔ\x0014\x0019ìíI&©çÆÞÃ½\x0005V{æ\x0016\x0002-mmøæ/ÿ*O>àôèÏØ\x0019\x001d°¶\\x001d¾ÉyÛÐ$</p><p>¡\x0013N\x00163î}ù«|öòOÙ¿yH¶o9~6£H¡hàåO·l^~Ý\x0011oÝ»Ev-'xÙÎéF$;$¢Z
¤YñÊ;FûcÚÆ¡BBêF\x0008Q`dP\x001bP
ÎðdHëIF¹ ~H÷ÿPö&±egvÞ·ÓÞþ¾6úÌìL\x0016Mu(X2J\x000c	\x0016à2<5\x0004y`@3ÃaÀðÄmxà±
\x0018°\x0001{$H&ä"UeÊ¨*Éd2È&3Ú×7·;÷t»ñ`÷Èe= \x0002èÞ}ïûß}þµÖ·ü\x000fQú\x001e¹lñ\x000e¦SÉd:äàhÅé¹ál\x000e*ZPTK¾%\x001b÷P*aÙ®XU\x0016D\x0005\x001e\x00069úÆÁô Õ
\x0007w\x0014®e°¡yéêEñ\x0017Ï~Î­-ËKpóJÐ5é`ÄþékÌúHrók\x0008\x0015¡Æ'lëB­K\x000e÷\x000f0Å\x0013nnNyoScGÃ£=æ'-Î	vzwh«µPZbE Q¶"´\x000cÝ5#âÑoAÑ0?û+²hF´\x0007<ùä_rãå>»CËOßçÍ;ÅâAÖà,ÔEËÉQK,OX,\x001afÖóØ_¡p\x0015\x000b]a²WÉãßgÜ¿ÊéÞ_"}¡2 \x001cdyÖT\x000fÙ¾bï¹C´\x0001ÕS-\x0011:\x0018«'UÇÓ/AïaO-IÒ£ñ\x0005^\x0005,Ôa¨y\x000fy®é\x000fr´a¾,b
Ââ±Xãi¬Áa×«N4\x0014HmÃ<®a{¼+\\x0008O¢3 !</p><p>¢ÈàZËd#¦n\x001bfÏÐ%\x000c{D{ÚeÉAý(; ë÷Ð'N!\x000cÌ19
/\x001e}D1ódDÔí!uP/3\x001cnQ=Ïxüe\x0005·Ù\x00189Võ	Â/\x0018¥ÁA¯#ÉháhxøeËF_Ñæ-\x0016äýøo5³ÎÎÎ¨ª</p><p>­\x0014ã®_mÐï³»³Ã×¿þuîÞ½KÓ4¼ÿþûxïÏ\x0016ìlo3\x0018ô\x0003Z¨ª\x0001ØÝ
âT¹.iýné¥¨[Ã«w_ÅYKedYÆéÉ	ù­Í-ö^¼`¹X²»³\x0012¾üò\x0019Û;ÛGCÒ$a>;e>óÓ¿ú+úý«W¯¦)Î9>ùøc¾öî»¸ºFç}ÎNùüó{8ç\x000f?þ8Í\x0019&¨8¥j\x000cMkL7lET­Åz\x0018N\x0006È(x\x0014(\x0002$\x000cú)Y0\x001cRøáþ3^ý
\x000e\x000eöøÁ\x000fþoþøÿÉæ\x0016Ç'ç(¥QIÊñÑ	Î+²<§q\x0015EÐ</p><p>¥\x000cG\x0013â$£¬ÎÉ{\x0012ë\x001a\x001eùÿäOþSâ(¥®[\[$\x0011Õz\x000eÞ°.</p><p>\#X/æ¼üÒK¬V+^<ÎÇOÑ±â;ßù6q\x001c&	E±ê0_üâ\x0017lN7xõµ×À;>}Fmj&\x0013¢8î0Q	ZéL3æó\x0005ëõ\x001a!TK×\x000cû}¼\x0010åuQÒÖ5:SHïØÝÙa:R~Ð\x001aCÕ4Ä©§*</p><p>ÕW_
ýIðÒ¨ë~!£­×XWÓK#ö>æüôïÿßãôx^\x00161\x001dÓÏ\x0013ÎO\x000f)W+\x0006ý\x000c-éÄÁ}õ­­]í\x001db\x001d\x000cSÊÚQ/\x000b¤ÙØºÊÛ¯!¤â_ý'O³9\x001ae)_{ó»\x001cí?¢i\x001a¾ùÍ÷p\x000e~ú³\x000f¹wÿsò|DCÅ\x0019Ëù9ßüûÿ>wîÜáã?âù\x0017@H]ªXÅ1uSuâjE\x0012K&£>¿÷{¿C]8çéõz\x001c\x001e1ÝØ`{sßÇ;Çd:ÁwÉýý\x0003îÞ½ÃÑQ\x00100vw§\x000cú\x0013\x000e\x000eyþü\x0010­#ÞX\x001bµÞ!¥àÙ³gL&ãÎÌ\x001czh~öÓ1\x0019ÙÚÜäàèo}ç;¬×\x0005Ï=§ª[\x0006Ã!ßþÖ·yòô\x0019ÆÌ°ÖñðáCªºa4¦)wïÞåúëì½xÁõkWh§OÐ\x001föyó×I¢/\x001f?Æ!¹qý\x0006{ûÔÅ/¿r>?à|^p¾Xsç×/ÖÄi"j\x0001\x000b/\x0019ßºÍa¹¢mÖ_yné8BF\x0001\x000e\x001e¤$'í÷IÒlÐ'ÎúDqÆ`0$\x0012\x0006½\x0011ÃÁ8iëÙùgÏRW\x0015£a,ËhMÃÙìÅr5£sÒ¬Çp4f4S·
\x001bDZamCÛ\x0006¤·\x0017÷4uMY\x0014Ôë2æ«6,\x0007¥\x000eÍÏq\x0012\x0018«0.àÌÎÎN9¥*\x0019
\x0006¼tû6ÞAYV|øá¯øøÓÏPZóö;ïÐ\x001fÉ7û¦ÄPÉ³\x001eÁ\x0008©\x0000.
\x0017=Ý8Ã&I$Z</p><p>´pDò¢ß.g:0\x001d
\x0019\x000eú\x000cú½ F´MX.{kèWÕ5Mc\x0010a\x0003zÕ\x0013Ì^;¬²®¨ª¦i¨ë¾¸ ¼\`ÞÞ°ÇõkWRá:îLR\x0004s·ëºÚÛ¦f]®QqÔ\x0011I³gL7'llNY-Ïq¶F4%²Ibsk\x0013\x0019e$ý!½á\x0014+4¯¾ù6óÅÃÃC\x000fÙ\x000c\x0002\x000eÜU\ÝR­gh\x001c[\x0011ßyï½Ë\x000e)ç"¬h=È(æètÆ×¾öuî}þ\x0019Ï_<ã¯òïøÏþÉ?áï~ÿû<¸w¿ö6³#þçÿéäÑ½\x0003UÊ\x0018\x000e®*?}\x001cìMKo¼\x0012XyT/E\x0011fG'TuÉºªÉÑÃ½Ï>ãÆ­\x001bÈ4æèøþpÀÕÝk\Ý½ÊáÁ>÷Ï\x0016H\x001bñüñ!Åºâ·_f<\x001d£@¶Y­\x000b\x0016«5§g§\x000c\x0007 uÀàµ¦ÅZ\x001f\x0010Þ$	y\x0012s¼ÌxcÂ\x0017Oxûõw8zrÈë×xüåSfó%ÃþýS^¾ý2\x001eÏõ\x001b×yé¥8=>¦X®HâG\x000f\x001fÒ8Ãw¿ûm\x001e<¼Ïÿþ¿ý\x001füÓúsï£Oø¿üs¤¤Q5U½¢¬j=}ÁÛo¿ÃÝ»¯óã\x001fÿº¬\x0011RR\x0014k"­9=;§552</p><p>û¥þ¸W8h]\x0015v´\x001e¤\x0017ÔUÅÁÞ\x001eZ*½>J*²8Áµº-yòÅÌgË \x000c$¡3m½ªµd2\x001e1\x001dlQ,K\x0006½)o½þu¶&»üðÿù3v¶®èÞWYËÅ2\x0006\x0001'}Ø¨çuuC+,Æ;µ]ê)üY¦D:</p><p>ØO\x0017\x000cë^tÄ³("îÄ\x001d¼\x000f)¾\x000eù«µFIu)ÒH©°m@\x000c;\x001fÄÄ8q\x001dºØv}¦í\x0004ÿ¶
Æ\x0007\x0004m\x001d0Ö\x0005ÂK\x001cÇ´¦Aj\x0016: iÃ6
§ûû,1E	MH¦)ç\x0019ôr²~\x000fD(\x001b3ÏØ{xDÒÏL7RR%«Å$M©­Å+Ac-©YÊ;\x000eNO)­!\x001eä´¢ijÕ\x001ak\x001d©Ä!4Ò86{CFé³YAæb4¬´xU0é'\x000c³DKZo©Û¢l\x0015ÔMÜ\x00180\x001d\x000eÑJ\x0007ÑË{4Di²(¦\x001f\x001bð²µØÖÑø\x001a"·&Ð§THÿ\x0005z ªkfK¯×ØªAzK¬\x0005Öy\x001ak\x0003	I°ÓÒ\x0011umñÂ££¬?@5-MUÓT\x0015i\x0011Þ"\x0005\x0004Ö»ÐÑ§$UU²÷â\x0005Ã~^¿GÖOIâ`ÀÀ\x001a"\x0015f¶*\x0004ð4­a¶\x000cç?|ð\x0017æ{\x0015\x0004;ÙÒË2t <,fs\x001eÞÀÑáaØ>ùËËðo</p><p>¿ökÿ\x000fïmâöÞÝ\x000féÂ¦i°Æ\x0010Å	BIº¦u¦Û¡úËM·8º\x001eÎ°ß²\x0017"»\x0008D¯ \x0007	Ö¡\x000bÒ9¬1)Ç\x0010²éhWÐáWëÔt\x000eÛò\x0000Y\x0012uY\x0000îÒ¬. îû%L&¬£¶i§ßïå9q±äüü<\x0018	e i\x0015Îtõªäøøùj\x0019¼IL¬½ë´Îv¹Ë\x000fZGdIJÄ¸º
hX©\x0019æA¯GÙÔa\x000f\x0011Kü(R\x0012+^¬ôS\x0008âTácL\x0008}f\x000b \x0012xí/ñ(¸ÀF.`ó¤ÁàÉò\x0008%\x0005Þ68\x001a¤¬r\x001ehz.Â4Åªf¹p4'2\x001ea54\x001aÑH¼ñx­Qmx,^+\x0010\x001drS9¤´ÝÞXáº¼÷¶4¥¡,JyÃü¼b½\x0000_­Aàl\x0008K[ô\x0006)=Z@ÏC%aå\x0005T4Öqv¾¦ì÷QBÓ\x0010M÷èE.t\x001dÔE*J_$¥:±,tÚ\x0007tZø2 \x0004Ã¿\x0014!½¢Â\x000f©\x0015ÑIR¼¸HDz0\x0006ç-\x0006\x0017\x0014á8#ÍR´øºÀ·«°Ø²jQ0?­h«ði\x0014Pw»Ù$¤i\x0012D6k±¶{Â\x0005á¬ëTZ #Ð\x001eu\x0008(OÝ¿ì$\x00142`j÷Há±¾Å	Ò1*Ê\x0010",©íÒbÊã
B¯\x0004\x001dk|!iKÅú¬eqêiË \x0010z I 5BvÂ¬r\x0001/ªAg\x0010ç(\x000bXTÝ%]u\x001aðpQ\x0012þC^G!§UÀ	E÷Æ)º¨~\x0013"ÊF¤\x0011o|kÂ_s¶ïè%-½¼¥í÷\x0016,A\x0004\x000e</p><p>0¸</p><p></p><p>ìg·AP¾º\x001c!2Ö\x00006¥Ö\x0002»r	Å\0;3,ç0+á}\x000fS`ì\x0005ýV\x0005|¤ò]üÚ#°Ý¥+j
¢u\x0018\x0017¿Ö	#3#BZíB#ø\x001bS»K\x0010</p><p>\x001fÒ³\x0010úì\x0014\x0011n=àÌÃìè
\x001d:­ñ2ð´C\x0015\x000c\x0007\x001c\x0015¾7B\x0007\x0011ÓÉ ¬!\x001aD\x0015ù·\x0010\x0008 ë4\x0000kÀ{)ÎkÉ¢>[\x0013O½¬­
Óñå|N[¯é
\x0006,\x0017çÄiÊºª\x0019\x000eú¬W\x0015eÑ°XqõÆ\x001d«s²t\x000c.ÅØ&\x0008®e<\x001a9$|x½PìîÃÑ¢GëÁÆ\x0000E sá\x001dÂ·x×WØÖâÀ\x000b
^uc s¸®N</p><p>ÅÙê÷?ü\x0019\x001eOðÖsr|\x0002Ö³^\x0017ÜºqA¯\x001fqïTÌ¸ÒsÁr½æ|vÆr9£m-Î7\x0008\x0011\jÆ6xchËÄYFR²¬ÖÈ8EF	Oî1ØÙAù°P\.\x001aªÒs{cõÖ.Ï\x000fö\x0011cf¼rë\x0015¸Ç'~\x00171iÖ§­5½Ñ\x000e­w\x000c3K:r¦e]\x0018Î¥ª$
>\x0008ç"\kÔÄ:A\x0013áï¹\x0012ç\x0005¦v´mC½®Y\x0017\x0005Õº¤©
\x0001ÑÙ!ÅHë/¯¯_\x0007eÃï]=äÅ\x0005%$B\x0006\x0004\x0012ª\x0013ø¹\x0002ë\x0011NÐt\x000e¼ÚÂm|\x0010\x0008\x001b'±^a	\x0007\x000fG8¤KïùCi\x0014\x0018\x001b\>u]S\x0014kº
J\x001d#ÅzJ41ØÆáELgÄIÌdÓëC4Í>ÍjÆÕÝ·^}ë	òÄ°Wä)x'/{ÒBd.MéC×óxÙqÑ½\x0008Â8+QÇxLð·`@Å1¦Õ\x0008\x0015q|pÊýûû,\x000b¨ðè$\x001clËª%òáûyÑ_ÒEôBY´w\<\x0015¾ûÉ»0½Âk:¼\x0002\x0004]ª°sn	Õ\x0018Öá0Ý\x001a)\x0014­	ÍÁJ\x0007\x0017l\x0014ÉÎ	æÂ×%CÇ¤à½Å{ÛÍà®ÃÁù?!ií»$¨5Æ\x0019\x000c×]@ªÑ%+\x001dByö\x000eÏ¿òÌ²>é\x000c\x001b\x0017R-D õ\x000c©ÅÀ¡(ÝÃ\x001bEäÇHß`mËol_ac´ÅFÿa^!âÍÜÒV+l´fÕxæuè\x00132\x0006!PÊ!£\x0014|DÓ:ZÓ\x001d ¥\x000bg\x0012d8MÙX4¸Õ	®¼OÕ~Êir\x000eÅüü§{ÜÜØüzÙñ!±\x000c]4\i©Î\x0017ø\x001a\x001aë \x0017Ö#çðè\x001ey?åøÅ/QÉö¯0ÎRÚeN,¦H}ÆÁ|\x000fá\x0013ê\x00079Z¾ÂO>\qc\x001aÞ·Tç\x0005¾tÈI-+¼Y?\x0018oiÒ¾@'1iÔ D\x0012¼-M1+<ßcÙFØì:¥¯\x0011R#À\x0005SªK\x000fj\x000c)©\x0011ô¨hí'¬Û\x001f"ê\x000fèË\x0012Ñxò\x0004n\WlífLw\x0004Ï÷<üÂ°\9Ò\°»#\x0019ö\x001d¾mpu\x0013zõ*O?É\x0007	I\x000cB¶\x0001ã\x0005ï°Þuú¸%ÕçP~={Æë»í\x0011lO`<Ú)ÒÞ
Ìé\x001frr¾C\x001a­¹³ñÁð¯xcZsÅN\x0010Å\x0012+ÓK\x0016¤ö\x000bF<a±TÜ\x001aOY¨]öÏ\x0017Ä¢A;</p><p>Ú¨ÆÉ\x0016á¢Ðâ¹\x0002_"¤¤e\x0003z[\x0019Ö+NOÎ\x0018GK66`±~ÀñÓÎk¯ÿ6ßçÙ§äL=[[	m\x0019\x000f\x001euÉ\x0019Áa¼G»5­ðÙ»¤[ÿ\x0001ì\x001dªÅ'4Í)±0á5x\x0012%Ib7Å¬b½ldxz\x000b]äÚE S¸f=ÿ¨ù·ÜÝÕ<Ùó´up6{é\x00121aöD	äy\x0002\x0018oÐ\x0011³7ItÀYh¼Gy\x0014XËÕ×ÑHR·,Î</p><p>^~½GUhß0?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/done/](https://carbure.beta.gouv.fr/accounts/password_reset/done/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.3.1/dist/main.min.css" rel="stylesheet">`
  
  
  
  
Instances: 9
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="#" method="post" name="form" target="_blank" novalidate>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="#" method="post" name="form" target="_blank" novalidate>`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 6
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
  </script>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
  </script>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
  </script>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
  </script>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
  </script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/manifest.json](https://carbure.beta.gouv.fr/images/favicons/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/robots.txt](https://carbure.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/safari-pinned-tab.svg](https://carbure.beta.gouv.fr/images/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png](https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png](https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/sitemap.xml](https://carbure.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png](https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png)
  
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/css/carbure.css](https://carbure.beta.gouv.fr/static/css/carbure.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/v2/static/media/MTE.ddbf9f08.svg](https://carbure.beta.gouv.fr/v2/static/media/MTE.ddbf9f08.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/v2/static/media/logo-fabriquenumerique.f3921f64.svg](https://carbure.beta.gouv.fr/v2/static/media/logo-fabriquenumerique.f3921f64.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/images/carbure.svg](https://carbure.beta.gouv.fr/static/images/carbure.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/images/Marianne.svg](https://carbure.beta.gouv.fr/static/images/Marianne.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png](https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png](https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/sitemap.xml](https://carbure.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/robots.txt](https://carbure.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png](https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/manifest.json](https://carbure.beta.gouv.fr/images/favicons/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/css/carbure.css](https://carbure.beta.gouv.fr/static/css/carbure.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/manifest.json](https://carbure.beta.gouv.fr/images/favicons/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/robots.txt](https://carbure.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png](https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png](https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/css/carbure.css](https://carbure.beta.gouv.fr/static/css/carbure.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png](https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/sitemap.xml](https://carbure.beta.gouv.fr/sitemap.xml)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/images/Marianne.svg](https://carbure.beta.gouv.fr/static/images/Marianne.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/images/banniere_home.png](https://carbure.beta.gouv.fr/static/images/banniere_home.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/css/carbure.css](https://carbure.beta.gouv.fr/static/css/carbure.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/v2/static/media/MTE.ddbf9f08.svg](https://carbure.beta.gouv.fr/v2/static/media/MTE.ddbf9f08.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/v2/static/media/logo-fabriquenumerique.f3921f64.svg](https://carbure.beta.gouv.fr/v2/static/media/logo-fabriquenumerique.f3921f64.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/images/carbure.svg](https://carbure.beta.gouv.fr/static/images/carbure.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `cUDdnjw6n5ZINZFrzUNhLlvX8FFivUSfLZVlzLLBNxlDkLlvbAhcwdIyALjKaC06`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Evidence: `rT5K2pwIIeYtDrv0wZmrivT5eIAZX04Hr2QRlaIS49aex65ulOOryk2dMTH8x0MO`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `rT5K2pwIIeYtDrv0wZmrivT5eIAZX04Hr2QRlaIS49aex65ulOOryk2dMTH8x0MO`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Evidence: `rT5K2pwIIeYtDrv0wZmrivT5eIAZX04Hr2QRlaIS49aex65ulOOryk2dMTH8x0MO`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Evidence: `rT5K2pwIIeYtDrv0wZmrivT5eIAZX04Hr2QRlaIS49aex65ulOOryk2dMTH8x0MO`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Evidence: `rT5K2pwIIeYtDrv0wZmrivT5eIAZX04Hr2QRlaIS49aex65ulOOryk2dMTH8x0MO`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>q@ݞ<:��H5�k�Ca.[��Qb�D�-�e̲�7\x0019C��ol\x0008\��2\x0000��h-:</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/done/](https://carbure.beta.gouv.fr/accounts/password_reset/done/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Anglais 🇬🇧</a>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/manifest.json](https://carbure.beta.gouv.fr/images/favicons/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/](https://carbure.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/robots.txt](https://carbure.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/sitemap.xml](https://carbure.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr](https://carbure.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png](https://carbure.beta.gouv.fr/images/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png](https://carbure.beta.gouv.fr/images/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/static/css/carbure.css](https://carbure.beta.gouv.fr/static/css/carbure.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png](https://carbure.beta.gouv.fr/images/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/login/](https://carbure.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/password_reset/](https://carbure.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>31449600, which evaluates to: 1970-12-31 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `name`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `password1`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/register](https://carbure.beta.gouv.fr/accounts/register)
  
  
  * Method: `POST`
  
  
  * Parameter: `password2`
  
  
  
  
* URL: [https://carbure.beta.gouv.fr/accounts/resend-activation-link](https://carbure.beta.gouv.fr/accounts/resend-activation-link)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
Instances: 5
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://carbure.beta.gouv.fr/accounts/register</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>name=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

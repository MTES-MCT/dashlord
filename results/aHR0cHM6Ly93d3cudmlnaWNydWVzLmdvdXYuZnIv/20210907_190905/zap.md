
# ZAP Scanning Report

Generated on Tue, 7 Sep 2021 19:00:18


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 8 |
| Low | 8 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Hash Disclosure - Mac OSX salted SHA-1 | High | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| Reverse Tabnabbing | Medium | 11 | 
| Secure Pages Include Mixed Content (Including Scripts) | Medium | 1 | 
| Source Code Disclosure - Perl | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Vulnerable JS Library | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 12 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Retrieved from Cache | Informational | 11 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 4 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 15 | 

## Alert Detail


  
  
  
  
### Hash Disclosure - Mac OSX salted SHA-1
##### High (Medium)
  
  
  
  
#### Description
<p>A hash was disclosed by the web server. - Mac OSX salted SHA-1</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/ftp/RIC/RIC_SPC_VCB.pdf](https://www.vigicrues.gouv.fr/ftp/RIC/RIC_SPC_VCB.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `FEFF0061007600650063002000760069007300750065006C`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that hashes that are used to protect credentials or other resources are not leaked by the web server or database. There is typically no requirement for password hashes to be accessible to the web browser.      </p>
  
### Other information
<p>FEFF0061007600650063002000760069007300750065006C</p>
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD19](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD19)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=MP1](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=MP1)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=MP2](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=MP2)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD17](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD17)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD9](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD9)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD8](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD8)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD5](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD5)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD10](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD10)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD2](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD2)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD21](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD1](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD1)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD20](https://www.vigicrues.gouv.fr/rss/?CdEntVigiCru=AD20)
  
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.pays-de-la-loire.developpement-durable.gouv.fr/le-service-de-prevision-des-crues-maine-loire-aval-r1933.html" target="_blank">http://www.pays-de-la-loire.developpement-durable.gouv.fr/le-service-de-prevision-des-crues-maine-loire-aval-r1933.html</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.gouvernement.fr" class="footer-partner-link" target="_blank"><img src="https://www.vigicrues.gouv.fr/assets/img/footer/dummy-logo-gouvernementfr.png" width="120" height="50" alt="gouvernement.fr"></a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.midi-pyrenees.developpement-durable.gouv.fr/" target="_blank">Le site du service d&#039;accueil</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.gouvernement.fr" class="footer-partner-link" target="_blank"><img src="http://www.vigicrues.gouv.fr/assets/img/footer/dummy-logo-gouvernementfr.png" width="120" height="50" alt="gouvernement.fr"></a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="other-vigilances-link" href="https://vigilance.meteofrance.fr/fr" target="_blank" title="Vigilance Météo-France - nouvelle fenêtre">
                    <img src="https://webservice.meteofrance.com/files/vigilance/vignette.gif" height="70" width="71" alt="Meteofrance"></a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.centre-val-de-loire.developpement-durable.gouv.fr/previsions-des-crues-r69.html" target="_blank">Les informations complémentaires du SPC</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.auvergne-rhone-alpes.developpement-durable.gouv.fr/prevision-des-crues-r3250.html" target="_blank">Les informations complémentaires du SPC</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.nouvelle-aquitaine.developpement-durable.gouv.fr/" target="_blank">Le site du service d&#039;accueil</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.nouvelle-aquitaine.developpement-durable.gouv.fr/" target="_blank">Le site du service d&#039;accueil</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.bretagne.developpement-durable.gouv.fr/" target="_blank">Le site du service d&#039;accueil</a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="external" href="http://www.nouvelle-aquitaine.developpement-durable.gouv.fr/" target="_blank">Le site du service d&#039;accueil</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Secure Pages Include Mixed Content (Including Scripts)
##### Medium (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.vigicrues.gouv.fr/assets/img/logo-rf.svg`
  
  
  
  
Instances: 1
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://www.vigicrues.gouv.fr/assets/img/logo-rf.svg</p><p>tag=img src=http://www.vigicrues.gouv.fr/assets/img/vigicrues.svg</p><p>tag=img src=http://www.vigicrues.gouv.fr/guyane/ftp/cruemax.png</p><p>tag=img src=http://www.vigicrues.gouv.fr/assets/img/footer/dummy-logo-gouvernementfr.png</p><p>tag=img src=http://www.vigicrues.gouv.fr/assets/img/footer/dummy-logo-servicepublicfr.png</p><p>tag=img src=http://www.vigicrues.gouv.fr/assets/img/footer/dummy-logo-legifrancegouvfr.png</p><p>tag=img src=http://www.vigicrues.gouv.fr/assets/img/footer/dummy-logo-francefr.png</p><p>tag=script src=http://www.vigicrues.gouv.fr/assets/js/jquery.js?v=202012101705</p><p>tag=script src=http://www.vigicrues.gouv.fr/assets/js/bootstrap.js?v=202012101705</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/ftp/RIC/RIC_SPC_MLA.pdf](https://www.vigicrues.gouv.fr/ftp/RIC/RIC_SPC_MLA.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#Wl20`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/ftp/SDPC/SDPC_Loire-Bretagne_2012.pdf](https://www.vigicrues.gouv.fr/ftp/SDPC/SDPC_Loire-Bretagne_2012.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#fBGm9A`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#Wl20</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
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
<p>The identified library jquery, version 2.2.4 is vulnerable.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/assets/js/jquery.js?v=202012101705](https://www.vigicrues.gouv.fr/assets/js/jquery.js?v=202012101705)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v2.2.4`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/assets/js/bootstrap.js?v=202012101705](https://www.vigicrues.gouv.fr/assets/js/bootstrap.js?v=202012101705)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v3.3.7`
  
  
  
  
Instances: 2
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p>CVE-2015-9251</p><p>CVE-2019-11358</p><p></p>
  
### Reference
* https://github.com/jquery/jquery/issues/2432
* http://blog.jquery.com/2016/01/08/jquery-2-2-and-1-12-released/
* http://research.insecurelabs.org/jquery/test/
* https://blog.jquery.com/2019/04/10/jquery-3-4-0-released/
* https://nvd.nist.gov/vuln/detail/CVE-2019-11358
* https://nvd.nist.gov/vuln/detail/CVE-2015-9251
* https://github.com/jquery/jquery/commit/753d591aea698e57d6db58c9f722cd0808619b1b
* https://bugs.jquery.com/ticket/11974
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
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

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q067231001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q067231001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q064402001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q064402001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q000002001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q000002001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q028003001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q028003001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q061253001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q061253001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q045001001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q045001001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q022403001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q022403001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q012006002](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q012006002)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q052253001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q052253001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q021401001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q021401001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q013003001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q013003001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q010003001](https://www.vigicrues.gouv.fr/niv3-station.php?CdEntVigiCru=27&CdStationHydro=Q010003001)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" action="." method="post">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "boutonDebit" "boutonHauteur" "input-station-search" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=120`
  
  
  
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.4.45-0+deb7u14`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC1`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC8`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC12`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC3`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=24)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC24`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC25`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC28`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC2`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC27`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC9`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC11`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `/ftp/plaquettes/plaquette_SPC10`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��i��Z�筵�?�V���m{�\x000b</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Admin`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Admin`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Admin`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `Admin`
  
  
  
  
Instances: 9
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "<!-- Custom SB Admin CSS (ACAI 3.0.8) -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script type="text/javascript"></p><p>    <!--</p><p>    xtnv = document;        //parent.document or top.document or document         </p><p> ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="dropdown-toggle navbar-link"
                  data-toggle="dropdown"
                  role="button"
                  aria-haspopup="true"
                  aria-expanded="false">
                  <span class="navbar-link-logo garonne-adour" aria-hidden="true"><i class="icon icon-path1"></i><i class="icon icon-path2"></i><i class="icon icon-path3"></i></span>                  <!-- &#8203; (zero-width space) permet aux items 2, 3 et 5 de passer sur 2 lignes en résolutions medium. 1 et 4 le font déjà sans ce caractères mais pas 2, 3 et 5 alors que la place manque déjà -->
                  <span class="navbar-link-txt">Adour&ndash;&#8203;Garonne</span>
                  <i class="icon icon-arrow" aria-hidden="true"></i><!-- no whitespace
                  --><i class="icon icon-dash" aria-hidden="true"></i>
                </a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=9)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=12)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=11)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [http://www.vigicrues.gouv.fr/](http://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](http://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](http://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](http://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/sitemap.xml](https://www.vigicrues.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=8)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=27)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=120`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20170929`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/](https://www.vigicrues.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20171030`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `20171030`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/robots.txt](https://www.vigicrues.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `20170929`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>20170929, which evaluates to: 1970-08-22 11:02:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=25)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
* URL: [https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28](https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=28)
  
  
  * Method: `GET`
  
  
  * Parameter: `CdEntVigiCru`
  
  
  
  
Instances: 15
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.vigicrues.gouv.fr/niv2-bassin.php?CdEntVigiCru=10</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [area] tag [coords] attribute </p><p></p><p>The user input found was:</p><p>CdEntVigiCru=10</p><p></p><p>The user-controlled value was:</p><p>108,79,5</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

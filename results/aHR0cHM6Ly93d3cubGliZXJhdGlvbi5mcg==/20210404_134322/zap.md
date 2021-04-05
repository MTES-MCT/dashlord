
# ZAP Scanning Report

Generated on Sun, 4 Apr 2021 13:36:11


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 2 |
| Medium | 5 |
| Low | 10 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Hash Disclosure - Mac OSX salted SHA-1 | High | 3 | 
| PII Disclosure | High | 1 | 
| Cross-Domain Misconfiguration | Medium | 8 | 
| CSP: Wildcard Directive | Medium | 5 | 
| Reverse Tabnabbing | Medium | 9 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cookie No HttpOnly Flag | Low | 4 | 
| Cookie Without SameSite Attribute | Low | 4 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| CSP: Notices | Low | 5 | 
| Dangerous JS Functions | Low | 11 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Information Disclosure - Debug Error Messages | Low | 1 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 12 | 
| Non-Storable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 17 | 

## Alert Detail


  
  
  
  
### Hash Disclosure - Mac OSX salted SHA-1
##### High (Medium)
  
  
  
  
#### Description
<p>A hash was disclosed by the web server. - Mac OSX salted SHA-1</p>
  
  
  
* URL: [https://www.liberation.fr/pf/dist/components/combinations/default.js?d=21](https://www.liberation.fr/pf/dist/components/combinations/default.js?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `012323232323232323232123232323232323232323232323`
  
  
  
  
* URL: [https://www.liberation.fr/pf/dist/components/combinations/default.js?d=21](https://www.liberation.fr/pf/dist/components/combinations/default.js?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `012323232323232323232123232312121212121212121212`
  
  
  
  
* URL: [https://www.liberation.fr/pf/dist/components/combinations/default.js?d=21](https://www.liberation.fr/pf/dist/components/combinations/default.js?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `012121212121212121212121212121212121212121212121`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.liberation.fr/politique/2/](https://www.liberation.fr/politique/2/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5000185221434`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 500018</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-RegularItalic.woff?d=21](https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-RegularItalic.woff?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-BoldItalic.woff?d=21](https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-BoldItalic.woff?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/fonts/SFProText/sf-pro-text-bold-webfont.woff2?d=21](https://www.liberation.fr/pf/resources/fonts/SFProText/sf-pro-text-bold-webfont.woff2?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/fonts/SFProText/sf-pro-text-regular-webfont.woff2?d=21](https://www.liberation.fr/pf/resources/fonts/SFProText/sf-pro-text-regular-webfont.woff2?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/images/liberation.png?d=21](https://www.liberation.fr/pf/resources/images/liberation.png?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-Bold.woff?d=21](https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-Bold.woff?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/images/liberation/favicon.ico?d=21](https://www.liberation.fr/pf/resources/images/liberation/favicon.ico?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-Regular.woff?d=21](https://www.liberation.fr/pf/resources/fonts/TiemposText/TiemposText-Regular.woff?d=21)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>script-src, script-src-elem, script-src-attr, style-src, style-src-elem, style-src-attr, img-src, connect-src, frame-src, frame-ancestors, font-src, media-src, object-src, manifest-src, worker-src, prefetch-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/recherche](https://www.liberation.fr/recherche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/search](https://www.liberation.fr/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.liberation.fr/societe/droits-des-femmes/dans-un-nouveau-manifeste-343-femmes-exigent-lallongement-des-delais-legaux-dacces-a-livg-20210404_YUAQCRYA75G3VNG5RQQA4MEHSM/](https://www.liberation.fr/societe/droits-des-femmes/dans-un-nouveau-manifeste-343-femmes-exigent-lallongement-des-delais-legaux-dacces-a-livg-20210404_YUAQCRYA75G3VNG5RQQA4MEHSM/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.lejdd.fr/Societe/exclusif-le-manifeste-des-343-femmes-qui-exigent-lallongement-des-delais-legaux-dacces-a-livg-4036089" target=_blank>dans une tribune au <i>Journal du dimanche</i></a>`
  
  
  
  
* URL: [https://www.liberation.fr/politique/le-temps-se-gate-20210329_2Y2DRW63D5BE7FY3S6OSHJFVEE/](https://www.liberation.fr/politique/le-temps-se-gate-20210329_2Y2DRW63D5BE7FY3S6OSHJFVEE/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.gallimard.fr/Catalogue/GALLIMARD/Blanche/L-ange-et-la-bete" target=_blank> son autobiographie</a>`
  
  
  
  
* URL: [https://www.liberation.fr/politique/pour-bertrand-les-regionales-ou-rien-20210402_B7VFIB2Q75FWPJOBXOF545QAIU/](https://www.liberation.fr/politique/pour-bertrand-les-regionales-ou-rien-20210402_B7VFIB2Q75FWPJOBXOF545QAIU/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://bit.ly/ChezPol_Lib%C3%A9" target=_blank><b>notre newsletter politique quotidienne réservée aux abonnés</b></a>`
  
  
  
  
* URL: [https://www.liberation.fr/societe/sante/assistantes-maternelles-et-gouvernement-le-bon-sens-pas-pres-de-chez-eux-20210402_S4ESX5TWO5HR5MG64MHEEM5UWE/](https://www.liberation.fr/societe/sante/assistantes-maternelles-et-gouvernement-le-bon-sens-pas-pres-de-chez-eux-20210402_S4ESX5TWO5HR5MG64MHEEM5UWE/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://hal-pasteur.archives-ouvertes.fr/pasteur-03155847" target=_blank> l’étude de l’Institut Pasteur</a>`
  
  
  
  
* URL: [https://www.liberation.fr/politique/macron-fait-tout-tout-seul-et-en-plus-il-rale-20210401_IQNGAZMKZFEBVGSGFB3FJH5IXA/](https://www.liberation.fr/politique/macron-fait-tout-tout-seul-et-en-plus-il-rale-20210401_IQNGAZMKZFEBVGSGFB3FJH5IXA/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://9r5g.mjt.lu/lnk/AUYAACj9d1cAAchKKA4AAAHl-J0AAAAdF00AAGlJAAxL9QBgZY8Rcx4U8J0lTEWGbZm4LYwPhQAMPbs/1/z-Z0O4gPwbRhDL1SiawZ_Q/aHR0cHM6Ly93d3cubGliZXJhdGlvbi5mci9pZGVlcy1ldC1kZWJhdHMvZWRpdG9yaWFsL2xhLWRpZmZpY2lsZS1lcXVhdGlvbi1kZW1tYW51ZWwtbWFjcm9uLTIwMjEwMzMxX0xNQ0xYWVVaMzVCQUhKTjZZUTc3V0VHRFhBLw" target=_blank><u>prolonger le tunnel</u></a>`
  
  
  
  
* URL: [https://www.liberation.fr/politique/ca-ninteresse-pas-les-francais-ou-ca-embarrasse-les-politiques-20210330_JYAZPBMH7JFO3DSY4Y4AQBGWVM/](https://www.liberation.fr/politique/ca-ninteresse-pas-les-francais-ou-ca-embarrasse-les-politiques-20210330_JYAZPBMH7JFO3DSY4Y4AQBGWVM/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.francetvinfo.fr/elections/presidentielle/video-presidentielle-2022-christian-jacob-n-ecarte-aucune-hypothese-sur-les-candidats-y-compris-un-ralliement-a-xavier-bertrand_4352879.html" target=_blank>France Info</a>`
  
  
  
  
* URL: [https://www.liberation.fr/economie/aides-publiques-aux-entreprises-la-lese-naivete-de-letat-stratege-20210330_FU6YUSURANDQBECW7FR4HTBFFI/](https://www.liberation.fr/economie/aides-publiques-aux-entreprises-la-lese-naivete-de-letat-stratege-20210330_FU6YUSURANDQBECW7FR4HTBFFI/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.strategie.gouv.fr/sites/strategie.gouv.fr/files/atoms/files/fs-2020-rapport-politique_industrielle-chapitre-4_1.pdf" target=_blank>En novembre 2020</a>`
  
  
  
  
* URL: [https://www.liberation.fr/politique/les-oppositions-remontees-apres-les-annonces-demmanuel-macron-20210401_UEG4S2MML5ALBCKVHA5OEBZULM/](https://www.liberation.fr/politique/les-oppositions-remontees-apres-les-annonces-demmanuel-macron-20210401_UEG4S2MML5ALBCKVHA5OEBZULM/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.leparisien.fr/politique/gerard-larcher-on-vit-dans-la-republique-de-loracle-31-03-2021-YNIASJ4O25EDBJSXJ7FA4PRKRY.php" target=_blank><i>le Parisien</i></a>`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/quand-la-fachosphere-cible-les-universitaires-20210331_PHR677XM2BCYBJT3CNNYRB4I5I/](https://www.liberation.fr/idees-et-debats/quand-la-fachosphere-cible-les-universitaires-20210331_PHR677XM2BCYBJT3CNNYRB4I5I/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://universiteouverte.org/2021/02/19/demission_vidal/" target=_blank>simple pétition</a>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script data-integration="queryly" src="https://www.queryly.com/js/queryly.v4.min.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.hubvisor.io/wrapper/01BYK28ENND8X5G8K0AJ2DPK4E/hubvisor.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.hubvisor.io/wrapper/01BYK28ENND8X5G8K0AJ2DPK4E/hubvisor.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://ced-ns.sascdn.com/diff/js/smart.js" async=""></script>`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script data-integration="queryly" src="https://www.queryly.com/js/queryly.v4.min.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script data-integration="queryly" src="https://www.queryly.com/js/queryly.v4.min.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://ced-ns.sascdn.com/diff/js/smart.js" async=""></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.liberation.fr/economie/](https://www.liberation.fr/economie/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/lifestyle/](https://www.liberation.fr/lifestyle/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://www.liberation.fr/pf/dist/page/pLblk7VgGnpHCETls/default.js?d=21](https://www.liberation.fr/pf/dist/page/pLblk7VgGnpHCETls/default.js?d=21)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set with an invalid SameSite attribute value, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
* URL: [https://www.liberation.fr/pf/dist/page/pLblk7VgGnpHCETls/default.js?d=21](https://www.liberation.fr/pf/dist/page/pLblk7VgGnpHCETls/default.js?d=21)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `akaas_AS_liberation_liberation_prod`
  
  
  * Evidence: `Set-Cookie: akaas_AS_liberation_liberation_prod`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.hubvisor.io/wrapper/01BYK28ENND8X5G8K0AJ2DPK4E/hubvisor.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.hubvisor.io/wrapper/01BYK28ENND8X5G8K0AJ2DPK4E/hubvisor.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.queryly.com/js/queryly.v4.min.js`
  
  
  * Evidence: `<script data-integration="queryly" src="https://www.queryly.com/js/queryly.v4.min.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.queryly.com/js/queryly.v4.min.js`
  
  
  * Evidence: `<script data-integration="queryly" src="https://www.queryly.com/js/queryly.v4.min.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.queryly.com/js/queryly.v4.min.js`
  
  
  * Evidence: `<script data-integration="queryly" src="https://www.queryly.com/js/queryly.v4.min.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ced-ns.sascdn.com/diff/js/smart.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://ced-ns.sascdn.com/diff/js/smart.js" async=""></script>`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes"></script>`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ced-ns.sascdn.com/diff/js/smart.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://ced-ns.sascdn.com/diff/js/smart.js" async=""></script>`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.hubvisor.io/wrapper/01BYK28ENND8X5G8K0AJ2DPK4E/hubvisor.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.hubvisor.io/wrapper/01BYK28ENND8X5G8K0AJ2DPK4E/hubvisor.js"></script>`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver%2CElement.prototype.prepend%2CElement.prototype.remove%2CArray.prototype.find%2CArray.prototype.includes"></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>1:1: The upgrade-insecure-requests directive is an experimental directive that will be likely added to the CSP specification.</p><p></p>
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/search](https://www.liberation.fr/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/recherche](https://www.liberation.fr/recherche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/economie/](https://www.liberation.fr/economie/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/lifestyle/](https://www.liberation.fr/lifestyle/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/portraits/](https://www.liberation.fr/portraits/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/evenements/](https://www.liberation.fr/evenements/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
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
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/economie/](https://www.liberation.fr/economie/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=60`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Debug Error Messages
##### Low (Medium)
  
  
  
  
#### Description
<p>The response appeared to contain common error messages returned by platforms such as ASP.NET, and Web-servers such as IIS and Apache. You can configure the list of common debug messages.</p>
  
  
  
* URL: [https://www.liberation.fr/culture/jeux-video/](https://www.liberation.fr/culture/jeux-video/)
  
  
  * Method: `GET`
  
  
  * Evidence: `under construction`
  
  
  
  
Instances: 1
  
### Solution
<p>Disable debugging messages before pushing to production.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/evenements/](https://www.liberation.fr/evenements/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
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
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/economie/](https://www.liberation.fr/economie/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
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
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `36178f-TxY8RBBLxWg3M/MTSZH6TwjSluA`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1d1fd0-FBtPQuaknUEumkTsadC3ZBC3w+o`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1ac-B/fu7krl5/JrdgXH9Ko6fcSzej4`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  * Evidence: `168463-NPHSD0nlq9K/pTgeWMR472iQawk`
  
  
  
  
* URL: [https://www.liberation.fr/evenements/](https://www.liberation.fr/evenements/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Image__StyledPicture-sc-8yioqf-0`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1a9af0-5tCDvgZllmLjmPD4RyfOOIGoMqo`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1de2c0-XSrG/J+J//TMeMR3QaAX41heHD4`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1ec19c-+XzcvgBc4Kx5AR4YZf6oJi4e0gE`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Image__StyledPicture-sc-8yioqf-0`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `18d731-ZAGzRqd8mAvJtrxTFMv3KGtr0yQ`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `36178f-TxY8RBBLxWg3M/MTSZH6TwjSluA`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>߭{���ŏ\x0011\x0004\x0012�Z
����d~��4��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.liberation.fr/evenements/](https://www.liberation.fr/evenements/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script type="application/javascript">window.Fusion=window.Fusion||{};Fusion.arcSite="liberation";Fusion.contextPath="/pf";Fusio", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/homepage" class="xl-promo-headline" title="Désolé! On cherche encore une blague" target="_self" rel=""><h2 class="default__HeadlineText-sc-1vz5n7h-0 eosxqj xl-promo-headline">Désolé! On cherche encore une blague</h2></a>`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Le cas Edouard Philippe bouscule la droite"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Espagne : Cachou, l’ours brun qui cachait la montagne de poudre blanche"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/societe/](https://www.liberation.fr/societe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Où en est l’enquête sur les chevaux mutilés ?"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/environnement/](https://www.liberation.fr/environnement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Salomé Berlioux, enfanter les invisibles"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/economie/](https://www.liberation.fr/economie/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Le canal de Suez, le goulot d’étranglement et les luttes sociales"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/evenements/](https://www.liberation.fr/evenements/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/homepage" class="xl-promo-headline" title="Désolé! On cherche encore une blague" target="_self" rel=""><h2 class="default__HeadlineText-sc-1vz5n7h-0 eosxqj xl-promo-headline">Désolé! On cherche encore une blague</h2></a>`
  
  
  
  
* URL: [https://www.liberation.fr/lifestyle/](https://www.liberation.fr/lifestyle/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Marseille, chais comment faire"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/idees-et-debats/](https://www.liberation.fr/idees-et-debats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Le canal de Suez, le goulot d’étranglement et les luttes sociales"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/portraits/](https://www.liberation.fr/portraits/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Coco, les feuilles fortes"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="La chaîne chinoise CGTN a-t-elle inventé une journaliste française ?"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" title="Pasolini, lignées directes"><picture class="Image__StyledPicture-sc-8yioqf-0 dRTDJJ"><div style="height:338px;width:600px;max-width:50px"></div></picture></a>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.liberation.fr](https://www.liberation.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/politique/](https://www.liberation.fr/politique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/checknews/](https://www.liberation.fr/checknews/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/search](https://www.liberation.fr/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/recherche](https://www.liberation.fr/recherche)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/sitemap.xml](https://www.liberation.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/international/](https://www.liberation.fr/international/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/culture/](https://www.liberation.fr/culture/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/robots.txt](https://www.liberation.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.liberation.fr/evenements/](https://www.liberation.fr/evenements/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 11
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
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
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `55043551`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `89453125`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617542662`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `775520037`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210216`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `575468421`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1203487355`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210331`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `775421276`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210402`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `56626370`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `157454529`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `486355764`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `013269906`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210311`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.liberation.fr/](https://www.liberation.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `60545370`
  
  
  
  
Instances: 17
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>55043551, which evaluates to: 1971-09-30 01:52:31</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

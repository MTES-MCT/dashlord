
# ZAP Scanning Report

Generated on Wed, 8 Sep 2021 16:22:50


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 6 |
| Low | 9 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 12 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Secure Pages Include Mixed Content | Low | 4 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Charset Mismatch  | Informational | 9 | 
| Information Disclosure - Sensitive Information in URL | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 15 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 12 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/admin/wp-login.php](https://www.geoportail.gouv.fr/admin/wp-login.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/admin/wp-admin/](https://www.geoportail.gouv.fr/admin/wp-admin/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/stations-vertes](https://www.geoportail.gouv.fr/donnees/stations-vertes)
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/foret](https://www.geoportail.gouv.fr/tag/foret)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2021/06](https://www.geoportail.gouv.fr/2021/06)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #00b798;font-weight: bold" href="https://www.ecologie.gouv.fr/directive-europeenne-inspire" target="_blank" rel="noopener">directive européenne INSPIRE</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #00b798;font-weight: bold" href="https://www.ecologie.gouv.fr/directive-europeenne-inspire" target="_blank" rel="noopener">directive européenne INSPIRE</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/bois](https://www.geoportail.gouv.fr/tag/bois)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/prsf](https://www.geoportail.gouv.fr/tag/prsf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/secours](https://www.geoportail.gouv.fr/tag/secours)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/rencontre](https://www.geoportail.gouv.fr/tag/rencontre)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/sdis](https://www.geoportail.gouv.fr/tag/sdis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/pompiers](https://www.geoportail.gouv.fr/tag/pompiers)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/112](https://www.geoportail.gouv.fr/tag/112)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2021/05](https://www.geoportail.gouv.fr/2021/05)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #00b798;font-weight: bold" href="https://geoservices.ign.fr/documentation/services/utilisation-web" target="_blank" rel="noopener">un site web</a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/point](https://www.geoportail.gouv.fr/tag/point)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fr.calameo.com/read/001188582695929d18ed9?page=20" target="_blank" rel="noopener">Pour en apprendre davantage sur les PRSF, découvrez l’article d’IGN Magazine n° 97</a>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/admin/wp-content/uploads/prsf-actu-geoportail-2.jpg](https://www.geoportail.gouv.fr/admin/wp-content/uploads/prsf-actu-geoportail-2.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#PEt9`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#PEt9</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `create
function r`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>create</p><p>function r</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/faq](https://www.geoportail.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='twentysixteen-fonts-css'  href='https://fonts.googleapis.com/css?family=Merriweather%3A400%2C700%2C900%2C400italic%2C700italic%2C900italic%7CMontserrat%3A400%2C700%7CInconsolata%3A400&#038;subset=latin%2Clatin-ext' type='text/css' media='all' />`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/stations-vertes](https://www.geoportail.gouv.fr/donnees/stations-vertes)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="http://gmpg.org/xfn/11">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/faq](https://www.geoportail.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/plan-ign-v2](https://www.geoportail.gouv.fr/donnees/plan-ign-v2)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/stations-vertes](https://www.geoportail.gouv.fr/donnees/stations-vertes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/secours](https://www.geoportail.gouv.fr/tag/secours)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/bois](https://www.geoportail.gouv.fr/tag/bois)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/foret](https://www.geoportail.gouv.fr/tag/foret)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/non-classe/reconfinement-afficher-une-limite-de-10km](https://www.geoportail.gouv.fr/non-classe/reconfinement-afficher-une-limite-de-10km)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/rencontre](https://www.geoportail.gouv.fr/tag/rencontre)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/sdis](https://www.geoportail.gouv.fr/tag/sdis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/category/non-classe](https://www.geoportail.gouv.fr/category/non-classe)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/point](https://www.geoportail.gouv.fr/tag/point)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/112](https://www.geoportail.gouv.fr/tag/112)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/pompiers](https://www.geoportail.gouv.fr/tag/pompiers)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/tag/prsf](https://www.geoportail.gouv.fr/tag/prsf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.geoportail.gouv.fr/">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "s" ].</p>
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/robots.txt](https://www.geoportail.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/category/faq-cartes-photos-parcelles-cadastrales](https://www.geoportail.gouv.fr/category/faq-cartes-photos-parcelles-cadastrales)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/admin/wp-content/uploads/Chatenay-M.jpg](https://www.geoportail.gouv.fr/admin/wp-content/uploads/Chatenay-M.jpg)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2018/11](https://www.geoportail.gouv.fr/2018/11)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.174069863711327,48.70998479646627&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=15](https://www.geoportail.gouv.fr/carte?c=2.174069863711327,48.70998479646627&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=15)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-login.php](https://www.geoportail.gouv.fr/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/category/faq-consultation-des-cartes](https://www.geoportail.gouv.fr/category/faq-consultation-des-cartes)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.3513621322021487,48.79018351257645&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=16](https://www.geoportail.gouv.fr/carte?c=2.3513621322021487,48.79018351257645&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=16)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2018/09](https://www.geoportail.gouv.fr/2018/09)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  * Parameter: `GEOPORTAILSESSION`
  
  
  * Evidence: `set-cookie: GEOPORTAILSESSION`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/plan-ign-v2](https://www.geoportail.gouv.fr/donnees/plan-ign-v2)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=3.996736668479421,48.044512940035105&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1;g)&l1=SECUROUTE.TE.1TE::GEOPORTAIL:OGC:WMTS(1)&l2=SECUROUTE.TE.ALL::GEOPORTAIL:OGC:WMS(1)&permalink=yes&z=9](https://www.geoportail.gouv.fr/carte?c=3.996736668479421,48.044512940035105&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1;g)&l1=SECUROUTE.TE.1TE::GEOPORTAIL:OGC:WMTS(1)&l2=SECUROUTE.TE.ALL::GEOPORTAIL:OGC:WMS(1)&permalink=yes&z=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/faq](https://www.geoportail.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/stations-vertes](https://www.geoportail.gouv.fr/donnees/stations-vertes)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://polyfill.io/v3/polyfill.min.js`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private,must-revalidate,max-age=86400`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/faq](https://www.geoportail.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private,must-revalidate,max-age=86400`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/stations-vertes](https://www.geoportail.gouv.fr/donnees/stations-vertes)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/robots.txt](https://www.geoportail.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-extra-6a2956a7cd03b40bda75ea0827847e71.js](https://www.geoportail.gouv.fr/assets/portail-front-extra-6a2956a7cd03b40bda75ea0827847e71.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/depot/stats/refonte/xtcore.js](https://www.geoportail.gouv.fr/depot/stats/refonte/xtcore.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
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

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/2016/03](https://www.geoportail.gouv.fr/2016/03)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.geoportail.gouv.fr/depot//actus/2016/service-itineraire/itineraire-gpp4-1.jpg`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2016/01](https://www.geoportail.gouv.fr/2016/01)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.geoportail.gouv.fr/depot//actus/2016/spot6/france-instantane-gpp4-carte.jpg`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2016/12](https://www.geoportail.gouv.fr/2016/12)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.geoportail.gouv.fr/depot/actus/2016/spot6-2016/grand-stade-lyon.jpg`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2016/04](https://www.geoportail.gouv.fr/2016/04)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.geoportail.gouv.fr/depot//actus/2016/service-isochrones/isochrones-gpp4-1.jpg`
  
  
  
  
Instances: 4
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://www.geoportail.gouv.fr/depot//actus/2016/service-itineraire/itineraire-gpp4-1.jpg</p><p>tag=img src=http://www.geoportail.gouv.fr/depot//actus/2016/service-itineraire/itineraire-gpp4-2.jpg</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css](https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/robots.txt](https://www.geoportail.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-16-0b02d2273a70314d039cfbe4b3831a03.png](https://www.geoportail.gouv.fr/assets/favicon-16-0b02d2273a70314d039cfbe4b3831a03.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-64-df3cd522e2f08830a121163646f9eeab.png](https://www.geoportail.gouv.fr/assets/favicon-64-df3cd522e2f08830a121163646f9eeab.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-32-3ed1ada13684127b4a69867dd67092fd.png](https://www.geoportail.gouv.fr/assets/favicon-32-3ed1ada13684127b4a69867dd67092fd.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-48-db6d8eb12f214596b8bba8fd2818b1d0.png](https://www.geoportail.gouv.fr/assets/favicon-48-db6d8eb12f214596b8bba8fd2818b1d0.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-f57c4ef8b735398da2079b149cf125af.css](https://www.geoportail.gouv.fr/assets/portail-front-f57c4ef8b735398da2079b149cf125af.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/apple-touch-icon-3135b1bf2c59a7ce172dab2d8b6b55df.png](https://www.geoportail.gouv.fr/assets/apple-touch-icon-3135b1bf2c59a7ce172dab2d8b6b55df.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/touch-icon-3aebf2c5a4669a76b01a15f6b2c9614f.png](https://www.geoportail.gouv.fr/assets/touch-icon-3aebf2c5a4669a76b01a15f6b2c9614f.png)
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css](https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-f57c4ef8b735398da2079b149cf125af.css](https://www.geoportail.gouv.fr/assets/portail-front-f57c4ef8b735398da2079b149cf125af.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/apple-touch-icon-3135b1bf2c59a7ce172dab2d8b6b55df.png](https://www.geoportail.gouv.fr/assets/apple-touch-icon-3135b1bf2c59a7ce172dab2d8b6b55df.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/touch-icon-3aebf2c5a4669a76b01a15f6b2c9614f.png](https://www.geoportail.gouv.fr/assets/touch-icon-3aebf2c5a4669a76b01a15f6b2c9614f.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-32-3ed1ada13684127b4a69867dd67092fd.png](https://www.geoportail.gouv.fr/assets/favicon-32-3ed1ada13684127b4a69867dd67092fd.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/robots.txt](https://www.geoportail.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-64-df3cd522e2f08830a121163646f9eeab.png](https://www.geoportail.gouv.fr/assets/favicon-64-df3cd522e2f08830a121163646f9eeab.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-48-db6d8eb12f214596b8bba8fd2818b1d0.png](https://www.geoportail.gouv.fr/assets/favicon-48-db6d8eb12f214596b8bba8fd2818b1d0.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-16-0b02d2273a70314d039cfbe4b3831a03.png](https://www.geoportail.gouv.fr/assets/favicon-16-0b02d2273a70314d039cfbe4b3831a03.png)
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-visu/visu-carto.min-b9e3c6d424d8ffc1abc62fdc063fd9e6.css](https://www.geoportail.gouv.fr/assets/portail-visu/visu-carto.min-b9e3c6d424d8ffc1abc62fdc063fd9e6.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `info/licences/Licence_CeCILL-B_V1-en`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-register.php](https://www.geoportail.gouv.fr/wp-register.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/admin/wp-content/uploads/SMV2020_TeaserGeoportail`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2017/02](https://www.geoportail.gouv.fr/2017/02)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/admin/wp-content/uploads/Geoportail-photo-aeriennes-1950-65-wordpress-vignette-avion`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `alreadyAnsweredGeoportailSurvey1`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2020/10](https://www.geoportail.gouv.fr/2020/10)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/admin/wp-content/uploads/SMV2020_TeaserGeoportail`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2017/11](https://www.geoportail.gouv.fr/2017/11)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/depot/actus/2017/collaboratif/planIGN`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/non-classe/reconfinement-afficher-une-limite-de-10km](https://www.geoportail.gouv.fr/non-classe/reconfinement-afficher-une-limite-de-10km)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Freconfinement-afficher-une-limite-de-10km`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/category/non-classe](https://www.geoportail.gouv.fr/category/non-classe)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/admin/wp-content/uploads/visuel-100KM`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-visu/visu-carto-print.min-19db14bf28ad268370da11e1132c2347.css](https://www.geoportail.gouv.fr/assets/portail-visu/visu-carto-print.min-19db14bf28ad268370da11e1132c2347.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `info/licences/Licence_CeCILL-B_V1-en`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css](https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAABQAAAAeCAYAAAAsEj5rAAAAUklEQVR42u3VMQoAIBADQf8Pgj+OD9hG2CtONJB2ymQkKe0HbwAP0xucDiQWARITIDEBEnMgMQ8S8+AqBIl6kKgHiXqQqAeJepBo/z38J/U0uAHlaBkBl9I4GwAAAABJRU5ErkJggg==`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/2020/05](https://www.geoportail.gouv.fr/2020/05)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/admin/wp-content/uploads/visuel-100KM`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�w��X�zw\x001e���q��{�\x0008���\x001f���</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Charset Mismatch 
##### Informational (Low)
  
  
  
  
#### Description
<p>This check identifies responses where the HTTP Content-Type header declares a charset different from the charset defined by the body of the HTML or XML. When there's a charset mismatch between the HTTP header and content body Web browsers can be forced into an undesirable content-sniffing mode to determine the content's correct character set.</p><p></p><p>An attacker could manipulate content on the page to be interpreted in an encoding of their choice. For example, if an attacker can control content at the beginning of the page, they could inject script using UTF-7 encoded text and manipulate some browsers into interpreting that text.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Frecherchez-une-parcelle-cadastrale-et-mesurez-sa-superficie](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Frecherchez-une-parcelle-cadastrale-et-mesurez-sa-superficie)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fcreez-votre-carte-personnalisee](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fcreez-votre-carte-personnalisee)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Fnon-classe%2Freconfinement-afficher-une-limite-de-10km](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Fnon-classe%2Freconfinement-afficher-une-limite-de-10km)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fvisualisez-vos-deplacements-sur-le-geoportail](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fvisualisez-vos-deplacements-sur-le-geoportail)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fcomprendre-le-geoportail](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fcomprendre-le-geoportail)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Fnon-classe%2Fdeconfinement-afficher-une-limite-de-100km](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Fnon-classe%2Fdeconfinement-afficher-une-limite-de-100km)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fajoutez-vos-informations](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fajoutez-vos-informations)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fenregistrez-et-partagez-vos-cartes](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fenregistrez-et-partagez-vos-cartes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fallez-plus-loin-avec-les-outils](https://www.geoportail.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Fwww.geoportail.gouv.fr%2Ftutorials%2Fallez-plus-loin-avec-les-outils)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Force UTF-8 for all text content in both the HTTP header and meta tags in HTML or encoding declarations in XML.</p>
  
### Other information
<p>There was a charset mismatch between the HTTP Header and the XML encoding declaration: [UTF-8] and [null] do not match.</p>
  
### Reference
* http://code.google.com/p/browsersec/wiki/Part2#Character_set_handling_and_detection

  
#### CWE Id : 436
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.341512629544421,48.85873471641844&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN50.1950::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13](https://www.geoportail.gouv.fr/carte?c=2.341512629544421,48.85873471641844&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN50.1950::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `2.341512629544421,48.85873471641844`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=5.4437216131621025,43.33332295880601&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN-EXPRESS.STANDARD::GEOPORTAIL:OGC:WMTS(1;g)&l1=INSEE.FILOSOFI.ENFANTS.0.17.ANS.SECRET::GEOPORTAIL:OGC:WMTS(0.94)&permalink=yes&z=16](https://www.geoportail.gouv.fr/carte?c=5.4437216131621025,43.33332295880601&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN-EXPRESS.STANDARD::GEOPORTAIL:OGC:WMTS(1;g)&l1=INSEE.FILOSOFI.ENFANTS.0.17.ANS.SECRET::GEOPORTAIL:OGC:WMTS(0.94)&permalink=yes&z=16)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `5.4437216131621025,43.33332295880601`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN25TOUR::GEOPORTAIL:OGC:WMTS(1)&l1=LANDCOVER.FORESTINVENTORY.V2::GEOPORTAIL:OGC:WMTS(0.6)&l2=GEOGRAPHICALGRIDSYSTEMS.ETATMAJOR40::GEOPORTAIL:OGC:WMTS(1)&l3=OCS.HISTORIQUE::GEOPORTAIL:OGC:WMTS(0.55)&permalink=yes&permalink=yeshttps://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&z=11](https://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN25TOUR::GEOPORTAIL:OGC:WMTS(1)&l1=LANDCOVER.FORESTINVENTORY.V2::GEOPORTAIL:OGC:WMTS(0.6)&l2=GEOGRAPHICALGRIDSYSTEMS.ETATMAJOR40::GEOPORTAIL:OGC:WMTS(1)&l3=OCS.HISTORIQUE::GEOPORTAIL:OGC:WMTS(0.55)&permalink=yes&permalink=yeshttps://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&z=11)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `-4.3856048583984375,48.343015367992706`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.3513621322021487,48.79018351257645&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=16](https://www.geoportail.gouv.fr/carte?c=2.3513621322021487,48.79018351257645&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=16)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `2.3513621322021487,48.79018351257645`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=1.4501953125000007,47.21956811231553&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1)&l1=VILLAGESETAPE::GEOPORTAIL:OGC:WMS(1)&l2=Voiture$OGC:OPENLS;Itineraire-1594284590187(0.9)&permalink=yes&z=6](https://www.geoportail.gouv.fr/carte?c=1.4501953125000007,47.21956811231553&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1)&l1=VILLAGESETAPE::GEOPORTAIL:OGC:WMS(1)&l2=Voiture$OGC:OPENLS;Itineraire-1594284590187(0.9)&permalink=yes&z=6)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `1.4501953125000007,47.21956811231553`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.2356288683693712,46.36632466845623&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGN::GEOPORTAIL:OGC:WMTS(1)&l1=n_vent_potentiel_eol_fixe_s(1)&permalink=yes&z=6](https://www.geoportail.gouv.fr/carte?c=2.2356288683693712,46.36632466845623&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGN::GEOPORTAIL:OGC:WMTS(1)&l1=n_vent_potentiel_eol_fixe_s(1)&permalink=yes&z=6)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `2.2356288683693712,46.36632466845623`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=6.4874267578125,45.249754646487304&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN-EXPRESS.NIVEAUXGRIS::GEOPORTAIL:OGC:WMTS(1)&l1=GEOGRAPHICALGRIDSYSTEMS.SLOPES.MOUNTAIN::GEOPORTAIL:OGC:WMTS(0.6)&permalink=yes&z=9](https://www.geoportail.gouv.fr/carte?c=6.4874267578125,45.249754646487304&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN-EXPRESS.NIVEAUXGRIS::GEOPORTAIL:OGC:WMTS(1)&l1=GEOGRAPHICALGRIDSYSTEMS.SLOPES.MOUNTAIN::GEOPORTAIL:OGC:WMTS(0.6)&permalink=yes&z=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `6.4874267578125,45.249754646487304`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=1.4501953125000007,47.21956811231553](https://www.geoportail.gouv.fr/carte?c=1.4501953125000007,47.21956811231553)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `1.4501953125000007,47.21956811231553`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.373869333496095,48.85063061782478&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN-EXPRESS.STANDARD::GEOPORTAIL:OGC:WMTS(1;g)&l1=INSEE.FILOSOFI.POPULATION::GEOPORTAIL:OGC:WMTS(0.8)&permalink=yes&z=12](https://www.geoportail.gouv.fr/carte?c=2.373869333496095,48.85063061782478&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN-EXPRESS.STANDARD::GEOPORTAIL:OGC:WMTS(1;g)&l1=INSEE.FILOSOFI.POPULATION::GEOPORTAIL:OGC:WMTS(0.8)&permalink=yes&z=12)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `2.373869333496095,48.85063061782478`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=-1.683643026538958,47.36456006011298&d1=1544684(1)&l0=ORTHOIMAGERY.ORTHOPHOTOS::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=7](https://www.geoportail.gouv.fr/carte?c=-1.683643026538958,47.36456006011298&d1=1544684(1)&l0=ORTHOIMAGERY.ORTHOPHOTOS::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=7)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `-1.683643026538958,47.36456006011298`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN25TOUR::GEOPORTAIL:OGC:WMTS(1)&l1=LANDCOVER.FORESTINVENTORY.V2::GEOPORTAIL:OGC:WMTS(0.6)&l2=GEOGRAPHICALGRIDSYSTEMS.ETATMAJOR40::GEOPORTAIL:OGC:WMTS(1)&l3=OCS.HISTORIQUE::GEOPORTAIL:OGC:WMTS(0.55)&permalink=yes&permalink=yeshttps://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&z=11](https://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS.SCAN25TOUR::GEOPORTAIL:OGC:WMTS(1)&l1=LANDCOVER.FORESTINVENTORY.V2::GEOPORTAIL:OGC:WMTS(0.6)&l2=GEOGRAPHICALGRIDSYSTEMS.ETATMAJOR40::GEOPORTAIL:OGC:WMTS(1)&l3=OCS.HISTORIQUE::GEOPORTAIL:OGC:WMTS(0.55)&permalink=yes&permalink=yeshttps://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706&z=11)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  * Evidence: `yeshttps://www.geoportail.gouv.fr/carte?c=-4.3856048583984375,48.343015367992706`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?amp;l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS&amp;z=16&c=2.3513621322021487,48.79018351257645](https://www.geoportail.gouv.fr/carte?amp;l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS&amp;z=16&c=2.3513621322021487,48.79018351257645)
  
  
  * Method: `GET`
  
  
  * Parameter: `c`
  
  
  * Evidence: `2.3513621322021487,48.79018351257645`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL appears to contain credit card information.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FIXME`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `BUG`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
Instances: 15
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 4 times, the first in the element starting with: "Ember.$("#advanced-search-coords-selectProj").change((function(){0===this.selectedIndex?(document.getElementById("advanced-searc", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/js/](https://www.geoportail.gouv.fr/wp-includes/js/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/plan-ign-v2](https://www.geoportail.gouv.fr/donnees/plan-ign-v2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/](https://www.geoportail.gouv.fr/wp-includes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-includes/images/](https://www.geoportail.gouv.fr/wp-includes/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/donnees/stations-vertes](https://www.geoportail.gouv.fr/donnees/stations-vertes)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/trackback/](https://www.geoportail.gouv.fr/trackback/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php](https://www.geoportail.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/faq](https://www.geoportail.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://polyfill.io/v3/polyfill.min.js"></script>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/robots.txt](https://www.geoportail.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-48-db6d8eb12f214596b8bba8fd2818b1d0.png](https://www.geoportail.gouv.fr/assets/favicon-48-db6d8eb12f214596b8bba8fd2818b1d0.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-16-0b02d2273a70314d039cfbe4b3831a03.png](https://www.geoportail.gouv.fr/assets/favicon-16-0b02d2273a70314d039cfbe4b3831a03.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css](https://www.geoportail.gouv.fr/assets/vendor-a0e055632a2d92f977cf0c9902315f96.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-64-df3cd522e2f08830a121163646f9eeab.png](https://www.geoportail.gouv.fr/assets/favicon-64-df3cd522e2f08830a121163646f9eeab.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/apple-touch-icon-3135b1bf2c59a7ce172dab2d8b6b55df.png](https://www.geoportail.gouv.fr/assets/apple-touch-icon-3135b1bf2c59a7ce172dab2d8b6b55df.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-f57c4ef8b735398da2079b149cf125af.css](https://www.geoportail.gouv.fr/assets/portail-front-f57c4ef8b735398da2079b149cf125af.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/touch-icon-3aebf2c5a4669a76b01a15f6b2c9614f.png](https://www.geoportail.gouv.fr/assets/touch-icon-3aebf2c5a4669a76b01a15f6b2c9614f.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/favicon-32-3ed1ada13684127b4a69867dd67092fd.png](https://www.geoportail.gouv.fr/assets/favicon-32-3ed1ada13684127b4a69867dd67092fd.png)
  
  
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
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `34942642`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/](https://www.geoportail.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `33696000`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `279541132`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `139770566`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62425156`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435455`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `17471321`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/sitemap.xml](https://www.geoportail.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `33696000`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js](https://www.geoportail.gouv.fr/assets/vendor-308509e205e394d442df34e96b10813f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `69885283`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js](https://www.geoportail.gouv.fr/assets/portail-front-08a77c0fe1e63eb59723a145238f5a21.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `559082264`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>34942642, which evaluates to: 1971-02-09 10:17:22</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=6.851706872139326,45.8394065258411&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2014::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2015::GEOPORTAIL:OGC:WMTS(1)&l2=ORTHOIMAGERY.ORTHO-SAT.SPOT.2016::GEOPORTAIL:OGC:WMTS(1)&l3=ORTHOIMAGERY.ORTHO-SAT.SPOT.2017::GEOPORTAIL:OGC:WMTS(1)&l4=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l5=ORTHOIMAGERY.ORTHO-SAT.SPOT.2019::GEOPORTAIL:OGC:WMTS(1)&l6=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13](https://www.geoportail.gouv.fr/carte?c=6.851706872139326,45.8394065258411&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2014::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2015::GEOPORTAIL:OGC:WMTS(1)&l2=ORTHOIMAGERY.ORTHO-SAT.SPOT.2016::GEOPORTAIL:OGC:WMTS(1)&l3=ORTHOIMAGERY.ORTHO-SAT.SPOT.2017::GEOPORTAIL:OGC:WMTS(1)&l4=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l5=ORTHOIMAGERY.ORTHO-SAT.SPOT.2019::GEOPORTAIL:OGC:WMTS(1)&l6=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=0.14623543306477,47.03048736295543&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1;h)&permalink=yes&z=16](https://www.geoportail.gouv.fr/carte?c=0.14623543306477,47.03048736295543&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1;h)&permalink=yes&z=16)
  
  
  * Method: `GET`
  
  
  * Parameter: `z`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=0.7456526799011228,47.91884800129077&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=14](https://www.geoportail.gouv.fr/carte?c=0.7456526799011228,47.91884800129077&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=14)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=0.14623543306477,47.03048736295543&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1;h)&permalink=yes&z=16](https://www.geoportail.gouv.fr/carte?c=0.14623543306477,47.03048736295543&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1;h)&permalink=yes&z=16)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=2.174069863711327,48.70998479646627&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=15](https://www.geoportail.gouv.fr/carte?c=2.174069863711327,48.70998479646627&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=15)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=7.382819840079667,43.89166840894697&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1)&l1=PROTECTEDAREAS.PRSF::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13](https://www.geoportail.gouv.fr/carte?c=7.382819840079667,43.89166840894697&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1)&l1=PROTECTEDAREAS.PRSF::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  
  
* URL: [https://www.geoportail.gouv.fr/carte?c=3.996736668479421,48.044512940035105&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1;g)&l1=SECUROUTE.TE.1TE::GEOPORTAIL:OGC:WMTS(1)&l2=SECUROUTE.TE.ALL::GEOPORTAIL:OGC:WMS(1)&permalink=yes&z=9](https://www.geoportail.gouv.fr/carte?c=3.996736668479421,48.044512940035105&l0=GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2::GEOPORTAIL:OGC:WMTS(1;g)&l1=SECUROUTE.TE.1TE::GEOPORTAIL:OGC:WMTS(1)&l2=SECUROUTE.TE.ALL::GEOPORTAIL:OGC:WMS(1)&permalink=yes&z=9)
  
  
  * Method: `GET`
  
  
  * Parameter: `permalink`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.geoportail.gouv.fr/carte?c=6.851706872139326,45.8394065258411&l0=ORTHOIMAGERY.ORTHO-SAT.SPOT.2014::GEOPORTAIL:OGC:WMTS(1)&l1=ORTHOIMAGERY.ORTHO-SAT.SPOT.2015::GEOPORTAIL:OGC:WMTS(1)&l2=ORTHOIMAGERY.ORTHO-SAT.SPOT.2016::GEOPORTAIL:OGC:WMTS(1)&l3=ORTHOIMAGERY.ORTHO-SAT.SPOT.2017::GEOPORTAIL:OGC:WMTS(1)&l4=ORTHOIMAGERY.ORTHO-SAT.SPOT.2018::GEOPORTAIL:OGC:WMTS(1)&l5=ORTHOIMAGERY.ORTHO-SAT.SPOT.2019::GEOPORTAIL:OGC:WMTS(1)&l6=ORTHOIMAGERY.ORTHO-SAT.SPOT.2020::GEOPORTAIL:OGC:WMTS(1)&permalink=yes&z=13</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [meta] tag [content] attribute </p><p></p><p>The user input found was:</p><p>permalink=yes</p><p></p><p>The user-controlled value was:</p><p>yes</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

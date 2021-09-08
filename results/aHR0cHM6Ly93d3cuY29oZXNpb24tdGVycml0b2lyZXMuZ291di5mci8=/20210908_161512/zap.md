
# ZAP Scanning Report

Generated on Wed, 8 Sep 2021 16:05:34


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 8 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| Vulnerable JS Library | Medium | 2 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 6 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 11 | 
| Retrieved from Cache | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 8 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 4 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/robots.txt](https://www.cohesion-territoires.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville](https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/Territoire_Gouv" target="_blank"><span class="icon-twitter icon-rs"><span class="is-sr-only">Compte Twitter du Ministère de la Cohésion des territoires et des Relations avec les collectivités territoriales</span></span></a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/rateit.css" />`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/rateit.css" />`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/rateit.css" />`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/rateit.css" />`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/rateit.css" />`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
Instances: 10
  
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
<p>The identified library jquery, version 3.4.1 is vulnerable.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/assets/vendor/jquery/jquery.min.js?v=3.4.1](https://www.cohesion-territoires.gouv.fr/core/assets/vendor/jquery/jquery.min.js?v=3.4.1)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v3.4.1`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/assets/vendor/jquery.ui/ui/jquery-1-7-min.js?v=1.12.1](https://www.cohesion-territoires.gouv.fr/core/assets/vendor/jquery.ui/ui/jquery-1-7-min.js?v=1.12.1)
  
  
  * Method: `GET`
  
  
  * Evidence: `jquery-1-7-min.js`
  
  
  
  
Instances: 2
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p></p>
  
### Reference
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/mes-demarches" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/loi-engagement-et-proximite" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/ma-commune" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="news-filter-form" data-drupal-selector="news-filter-form-2" action="/actualites" method="GET" id="news-filter-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="localite-search-form" onsubmit="return false;" data-drupal-selector="localite-search-form-2" action="/" method="post" id="localite-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="webform-submission-form webform-submission-add-form webform-submission-feedback-form webform-submission-feedback-add-form webform-submission-feedback-node-44426-form webform-submission-feedback-node-44426-add-form js-webform-details-toggle webform-details-toggle" data-drupal-selector="webform-submission-feedback-node-44426-add-form" action="/loi-engagement-et-proximite" method="post" id="webform-submission-feedback-node-44426-add-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/actualites" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/le-ministere" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="localite-search-form" onsubmit="return false;" data-drupal-selector="localite-search-form" action="/ma-commune" method="post" id="localite-search-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="generic-search-form" data-drupal-selector="generic-search-form-2" action="/politiques-publiques" method="post" id="generic-search-form--2" accept-charset="UTF-8">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "form_build_id" "form_id" "generic-search-form-input" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-relance-un-accompagnement-specifique-des-collectivites-territoriales](https://www.cohesion-territoires.gouv.fr/france-relance-un-accompagnement-specifique-des-collectivites-territoriales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/finances-et-dotations-aux-collectivites-locales](https://www.cohesion-territoires.gouv.fr/finances-et-dotations-aux-collectivites-locales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/accueil](https://www.cohesion-territoires.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `POST`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 55 [https://www.cohesion-territoires.gouv.fr/France-Relance].</p><p>Predicted response size: 355.</p><p>Response Body Length: 466.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville](https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/gh/gjunge/rateit.js@1.1.3/scripts/jquery.rateit.min.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/assets/vendor/jquery/jquery.min.js?v=3.4.1](https://www.cohesion-territoires.gouv.fr/core/assets/vendor/jquery/jquery.min.js?v=3.4.1)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/modules/custom/mte_tacjs/assets/vendor/tarteaucitron.js/tarteaucitron.js?v=1.4](https://www.cohesion-territoires.gouv.fr/modules/custom/mte_tacjs/assets/vendor/tarteaucitron.js/tarteaucitron.js?v=1.4)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/sitemap.xml](https://www.cohesion-territoires.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/robots.txt](https://www.cohesion-territoires.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/sitemap.xml](https://www.cohesion-territoires.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/robots.txt](https://www.cohesion-territoires.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/ajax-progress.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/ajax-progress.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/fieldgroup.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/fieldgroup.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/align.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/align.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/clearfix.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/clearfix.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/item-list.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/item-list.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/details.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/details.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/container-inline.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/container-inline.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/autocomplete-loading.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/autocomplete-loading.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/hidden.module.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/themes/stable/css/system/components/hidden.module.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/misc/normalize-fixes.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/misc/normalize-fixes.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/themes/custom/mct_theme/favicon.png](https://www.cohesion-territoires.gouv.fr/themes/custom/mct_theme/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/core/assets/vendor/normalize-css/normalize.css?qz2ihm](https://www.cohesion-territoires.gouv.fr/core/assets/vendor/normalize-css/normalize.css?qz2ihm)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville](https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-P3X6kh_Jq1B4iE5yVcMGkgdKbmMjjA_ndCiOysMkkdw`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-Kc9_HpEU-uHE2wobmucEzKiCtBbFcoUSkUdviEyIqNU`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `form-rn2Iw9BQd6XUVc5jwhK2tL57f4Wn0YTIYVmrN8H2l90`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>~�����#\x000fAAޗQW9�\x0008J�����\x0016�F\x0013!�f��\x0007�_t</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville](https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script type="application/json" data-drupal-selector="drupal-settings-json">{"path":{"baseUrl":"\/","scriptPath":null,"pathPrefi", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/territoires-dindustrie](https://www.cohesion-territoires.gouv.fr/territoires-dindustrie)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville](https://www.cohesion-territoires.gouv.fr/quartiers-de-la-politique-de-la-ville)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"  class="region region-primary-menu is-hidden-touch desktop-menu" onclick="return tag.click.send({elem:this, name:&quot;Recherche&quot;, chapter1:&quot;Header&quot;, type:&quot;action&quot;});"><span class="icon-search"></span>
            </a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/sitemap.xml](https://www.cohesion-territoires.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/robots.txt](https://www.cohesion-territoires.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
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

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales](https://www.cohesion-territoires.gouv.fr/budget-et-dotations-des-collectivites-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/le-ministere](https://www.cohesion-territoires.gouv.fr/le-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/france-services](https://www.cohesion-territoires.gouv.fr/france-services)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/mes-demarches](https://www.cohesion-territoires.gouv.fr/mes-demarches)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite](https://www.cohesion-territoires.gouv.fr/loi-engagement-et-proximite)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/actualites](https://www.cohesion-territoires.gouv.fr/actualites)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/robots.txt](https://www.cohesion-territoires.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/sitemap.xml](https://www.cohesion-territoires.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/politiques-publiques](https://www.cohesion-territoires.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `GET`
  
  
  * Evidence: `200034692`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/dispositif-pinel](https://www.cohesion-territoires.gouv.fr/dispositif-pinel)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210302`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/dispositif-pinel](https://www.cohesion-territoires.gouv.fr/dispositif-pinel)
  
  
  * Method: `GET`
  
  
  * Evidence: `20140318`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/sitemap.xml](https://www.cohesion-territoires.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `20192020`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/dispositif-pinel](https://www.cohesion-territoires.gouv.fr/dispositif-pinel)
  
  
  * Method: `GET`
  
  
  * Evidence: `347356060`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/dispositif-pinel](https://www.cohesion-territoires.gouv.fr/dispositif-pinel)
  
  
  * Method: `GET`
  
  
  * Evidence: `20130122`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `200070571`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/dispositif-pinel](https://www.cohesion-territoires.gouv.fr/dispositif-pinel)
  
  
  * Method: `GET`
  
  
  * Evidence: `20140327`
  
  
  
  
Instances: 8
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>200034692, which evaluates to: 1976-05-04 05:11:32</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `form_id`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/](https://www.cohesion-territoires.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `search`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `POST`
  
  
  * Parameter: `search`
  
  
  
  
* URL: [https://www.cohesion-territoires.gouv.fr/ma-commune](https://www.cohesion-territoires.gouv.fr/ma-commune)
  
  
  * Method: `POST`
  
  
  * Parameter: `form_id`
  
  
  
  
Instances: 4
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.cohesion-territoires.gouv.fr/</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>form_id=localite_search_form</p><p></p><p>The user-controlled value was:</p><p>localite_search_form</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

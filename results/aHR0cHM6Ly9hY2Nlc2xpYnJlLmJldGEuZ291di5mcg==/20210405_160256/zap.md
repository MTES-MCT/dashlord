
# ZAP Scanning Report

Generated on Mon, 5 Apr 2021 15:56:59


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 2 |
| Low | 8 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 12 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 1 | 
| Dangerous JS Functions | Low | 9 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec) | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 2 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 8 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 13 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/82-montauban/](https://acceslibre.beta.gouv.fr/app/82-montauban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `377024650573731`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/10-troyes/](https://acceslibre.beta.gouv.fr/app/10-troyes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `30344122148188`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `4955632727054`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/73-albertville/a/centre-de-vaccination/erp/centre-de-vaccination-8/](https://acceslibre.beta.gouv.fr/app/73-albertville/a/centre-de-vaccination/erp/centre-de-vaccination-8/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5757076347541`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/82-montauban/](https://acceslibre.beta.gouv.fr/app/82-montauban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `376241445541382`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/59-solesmes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-de-solesmes-centre-medical/](https://acceslibre.beta.gouv.fr/app/59-solesmes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-de-solesmes-centre-medical/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4955632727054`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?lat&localize=1&lon&q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?lat&localize=1&lon&q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `4955632727054`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/13-marseille/a/centre-de-vaccination/erp/centre-vaccination-cesam-13/](https://acceslibre.beta.gouv.fr/app/13-marseille/a/centre-de-vaccination/erp/centre-vaccination-cesam-13/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4138789666561`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?lat&localize&lon&page=1&q=centres%20de%20vaccination](https://acceslibre.beta.gouv.fr/recherche/?lat&localize&lon&page=1&q=centres%20de%20vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `4955632727054`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/75-paris/](https://acceslibre.beta.gouv.fr/app/75-paris/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4041953533254`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/93-romainville/a/centre-de-vaccination/erp/centre-de-vaccination-centre-municipal-de-sante-2/](https://acceslibre.beta.gouv.fr/app/93-romainville/a/centre-de-vaccination/erp/centre-de-vaccination-centre-municipal-de-sante-2/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4041953533254`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/42-saint-etienne/](https://acceslibre.beta.gouv.fr/app/42-saint-etienne/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4322878163413`
  
  
  
  
Instances: 12
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: American Express</p><p>Bank Identification Number: 377024</p><p>Brand: AMERICAN EXPRESS</p><p>Category: </p><p>Issuer: AMERICAN EXPRESS</p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://accessibilityinsights.io/" target="_blank">Accessibility Insight</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-light" href="https://updown.io/9wqh" target="_blank">Statut du serveur</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://fabrique-numerique.gitbook.io/acceslibre/guides/centre-vaccination" target="_blank">suivez notre guide de contribution</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/72-le-mans/a/centre-de-vaccination/erp/centre-de-vaccination-le-mans-centre-hospitalier-centre-covid-vaccination/](https://acceslibre.beta.gouv.fr/app/72-le-mans/a/centre-de-vaccination/erp/centre-de-vaccination-le-mans-centre-hospitalier-centre-covid-vaccination/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline my-2 my-lg-0 flex-fill" action="/app/72-le-mans/"
      method="get">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?lat&localize&lon&page=2&q=centres%20de%20vaccination](https://acceslibre.beta.gouv.fr/recherche/?lat&localize&lon&page=2&q=centres%20de%20vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/81-lavaur/a/centre-de-vaccination/erp/centre-de-vaccination-de-lavaur-centre-hospitalier/](https://acceslibre.beta.gouv.fr/app/81-lavaur/a/centre-de-vaccination/erp/centre-de-vaccination-de-lavaur-centre-hospitalier/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline my-2 my-lg-0 flex-fill" action="/app/81-lavaur/"
      method="get">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/80-chaulnes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-chaulnes-centre-socioculturel/](https://acceslibre.beta.gouv.fr/app/80-chaulnes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-chaulnes-centre-socioculturel/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline my-2 my-lg-0 flex-fill" action="/app/80-chaulnes/"
      method="get">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/71-macon/a/centre-de-vaccination/erp/centre-vaccination-macon-halle-sportive-du-centre-omnisport/](https://acceslibre.beta.gouv.fr/app/71-macon/a/centre-de-vaccination/erp/centre-vaccination-macon-halle-sportive-du-centre-omnisport/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline my-2 my-lg-0 flex-fill" action="/app/71-macon/"
      method="get">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/03-montlucon/a/centre-de-vaccination/erp/centre-de-vaccination-de-montlucon-centre-athanor/](https://acceslibre.beta.gouv.fr/app/03-montlucon/a/centre-de-vaccination/erp/centre-de-vaccination-de-montlucon-centre-athanor/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline my-2 my-lg-0 flex-fill" action="/app/03-montlucon/"
      method="get">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?lat&localize=1&lon&q](https://acceslibre.beta.gouv.fr/recherche/?lat&localize=1&lon&q)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/59-solesmes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-de-solesmes-centre-medical/](https://acceslibre.beta.gouv.fr/app/59-solesmes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-de-solesmes-centre-medical/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline my-2 my-lg-0 flex-fill" action="/app/59-solesmes/"
      method="get">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "q" ].</p>
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/](https://acceslibre.beta.gouv.fr/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/?next=/](https://acceslibre.beta.gouv.fr/accounts/register/?next=/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/password_reset/](https://acceslibre.beta.gouv.fr/accounts/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/recherche/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/recherche/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next](https://acceslibre.beta.gouv.fr/accounts/login/?next)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/login/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contact/](https://acceslibre.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//unpkg.com/swagger-ui-dist@3/swagger-ui-bundle.js`
  
  
  * Evidence: `<script src="//unpkg.com/swagger-ui-dist@3/swagger-ui-bundle.js"></script>`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/a/creche/erp/creche-la-flute-enchantee/](https://acceslibre.beta.gouv.fr/app/92-clichy/a/creche/erp/creche-la-flute-enchantee/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/76-le-havre/a/centre-de-vaccination/erp/grand-centre-de-vaccination-stade-oceane/](https://acceslibre.beta.gouv.fr/app/76-le-havre/a/centre-de-vaccination/erp/grand-centre-de-vaccination-stade-oceane/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/a/cafeteria/erp/cafe-georges/](https://acceslibre.beta.gouv.fr/app/92-clichy/a/cafeteria/erp/cafe-georges/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/a/restaurant/erp/cherquaoui-salhi-sanaa-cheval-blanc/](https://acceslibre.beta.gouv.fr/app/92-clichy/a/restaurant/erp/cherquaoui-salhi-sanaa-cheval-blanc/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/a/agence-postale/erp/asfar-mtv/](https://acceslibre.beta.gouv.fr/app/92-clichy/a/agence-postale/erp/asfar-mtv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/](https://acceslibre.beta.gouv.fr/app/92-clichy/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/a/tabac/erp/bridoux-catherine-tabac-breizh/](https://acceslibre.beta.gouv.fr/app/92-clichy/a/tabac/erp/bridoux-catherine-tabac-breizh/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/92-clichy/a/epicerie/erp/boisseau-alimentation/](https://acceslibre.beta.gouv.fr/app/92-clichy/a/epicerie/erp/boisseau-alimentation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contact/](https://acceslibre.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/sitemap.xml](https://acceslibre.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
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

  
  
  
  
### Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec)
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) headers were found, a response with multiple HSTS header entries is not compliant with the specification (RFC 6797) and only the first HSTS header will be processed others will be ignored by user agents or the HSTS policy may be incorrectly applied.</p><p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL).</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/sitemap.xml](https://acceslibre.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contrib/start/](https://acceslibre.beta.gouv.fr/contrib/start/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that only one component in your stack: code, web server, application server, load balancer, etc. is configured to set or add a HTTP Strict-Transport-Security (HSTS) header.</p>
  
### Reference
* http://tools.ietf.org/html/rfc6797#section-8.1

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/favicon.f67248f8d5b7.ico](https://acceslibre.beta.gouv.fr/static/img/favicon.f67248f8d5b7.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/illustration-principale.cc846eb3fd7f.png](https://acceslibre.beta.gouv.fr/static/img/landing/illustration-principale.cc846eb3fd7f.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/manifest.4c2dfab4446e.webmanifest](https://acceslibre.beta.gouv.fr/static/manifest.4c2dfab4446e.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/apple-touch-icon.1dbbb71330f3.png](https://acceslibre.beta.gouv.fr/static/img/apple-touch-icon.1dbbb71330f3.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/stopwatch.e7e63e9218f6.png](https://acceslibre.beta.gouv.fr/static/img/landing/stopwatch.e7e63e9218f6.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/visibilite.ed3fed9e2baa.png](https://acceslibre.beta.gouv.fr/static/img/landing/visibilite.ed3fed9e2baa.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/fiabilite-des-donnees.da83f39dbb8e.png](https://acceslibre.beta.gouv.fr/static/img/landing/fiabilite-des-donnees.da83f39dbb8e.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ebea6544e9d2.css](https://acceslibre.beta.gouv.fr/static/dist/main.ebea6544e9d2.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/participez-enrichissement-donnees.9a4c019e1212.png](https://acceslibre.beta.gouv.fr/static/img/landing/participez-enrichissement-donnees.9a4c019e1212.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/logo-acceslibre.b43598347b82.svg](https://acceslibre.beta.gouv.fr/static/img/logo-acceslibre.b43598347b82.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/rassurez-vous.800bd7d0c390.png](https://acceslibre.beta.gouv.fr/static/img/landing/rassurez-vous.800bd7d0c390.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5vHvklR8grDDGCcJJiohBs6yNq6PFr901rT8QYS93zAbbDilVbTz8NxVgxFBdisf`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5vHvklR8grDDGCcJJiohBs6yNq6PFr901rT8QYS93zAbbDilVbTz8NxVgxFBdisf`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `iBstxzAU71oINQgMSrxoHh9rzedpj_49A953H788D5I`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `DGostuPnWBUYlhcF3dhrUsLpZEEMNrMPNI7pAUsDqVb17U05RfiuBQ2DlgFDoWCo`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�\x001b-�0\x0014�Z\x00085\x0008\x000cJ�h\x001e\x001fk��i��=\x0003�w\x001f�<\x000f�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/72-le-mans/a/centre-de-vaccination/erp/centre-de-vaccination-le-mans-centre-hospitalier-centre-covid-vaccination/](https://acceslibre.beta.gouv.fr/app/72-le-mans/a/centre-de-vaccination/erp/centre-de-vaccination-le-mans-centre-hospitalier-centre-covid-vaccination/)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/72-le-mans/a/centre-de-vaccination/erp/centre-de-vaccination-le-mans-centre-hospitalier-centre-covid-vaccination/](https://acceslibre.beta.gouv.fr/app/72-le-mans/a/centre-de-vaccination/erp/centre-de-vaccination-le-mans-centre-hospitalier-centre-covid-vaccination/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/03-montlucon/a/centre-de-vaccination/erp/centre-de-vaccination-de-montlucon-centre-athanor/](https://acceslibre.beta.gouv.fr/app/03-montlucon/a/centre-de-vaccination/erp/centre-de-vaccination-de-montlucon-centre-athanor/)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js](https://acceslibre.beta.gouv.fr/static/dist/main.9a359d7c51c9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/81-lavaur/a/centre-de-vaccination/erp/centre-de-vaccination-de-lavaur-centre-hospitalier/](https://acceslibre.beta.gouv.fr/app/81-lavaur/a/centre-de-vaccination/erp/centre-de-vaccination-de-lavaur-centre-hospitalier/)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/80-chaulnes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-chaulnes-centre-socioculturel/](https://acceslibre.beta.gouv.fr/app/80-chaulnes/a/centre-de-vaccination/erp/centre-de-vaccination-commune-chaulnes-centre-socioculturel/)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected 2 times, the first in the element starting with: ""use strict";Object.defineProperty(exports,"__esModule",{value:!0}),exports.default=void 0;var e=t(require("./api"));function t(", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="page-link" href="#">&laquo;&nbsp;Page précédente</a>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    <img src="//stats.data.gouv.fr/matomo.php?idsite=118&amp;rec=1" alt="">
  </noscript>`
  
  
  
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contrib/start/](https://acceslibre.beta.gouv.fr/contrib/start/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/sitemap.xml](https://acceslibre.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `99920005`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `99095404`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `98828155`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `98911786`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `98785126`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `98815274`
  
  
  
  
Instances: 8
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>99920005, which evaluates to: 1973-03-02 11:33:25</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `password2`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `last_name`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/login/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?lat&localize=1&lon&q](https://acceslibre.beta.gouv.fr/recherche/?lat&localize=1&lon&q)
  
  
  * Method: `GET`
  
  
  * Parameter: `localize`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `first_name`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?q=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Parameter: `q`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/login/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `password1`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `username`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/](https://acceslibre.beta.gouv.fr/accounts/login/?next=/accounts/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
Instances: 13
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://acceslibre.beta.gouv.fr/accounts/register/</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>password2=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Wed, 14 Apr 2021 15:10:59


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 8 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: script-src unsafe-inline | Medium | 2 | 
| CSP: style-src unsafe-inline | Medium | 2 | 
| CSP: Wildcard Directive | Medium | 2 | 
| Reverse Tabnabbing | Medium | 12 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| CSP: Notices | Low | 2 | 
| Dangerous JS Functions | Low | 3 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Private IP Disclosure | Low | 4 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 2 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 10 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 11 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
Instances: 2
  
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

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
Instances: 2
  
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

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors</p><p></p><p>The directive(s): frame-ancestors are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.eau-rhin-meuse.fr/" target="_blank">
                    
                        
                        <img src="https://aides-territoires-prod.s3.fr-par.scw.cloud/aides-territoires-prod/backers/agence-de-leau-rhin-meuse_logo.jpeg?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=SCWJ1T6VQNR6Z83FSYEB%2F20210414%2Ffr-par%2Fs3%2Faws4_request&amp;X-Amz-Date=20210414T150852Z&amp;X-Amz-Expires=3600&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=eb59568963352c7a7e58eec45111c82f064365d21c315aca5e75a558fad75153" alt="Logo : Agence de l&#x27;eau  Rhin-Meuse ">
                        
                    </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.cerema.fr/fr" target="_blank">
                    
                        
                        <img src="https://aides-territoires-prod.s3.fr-par.scw.cloud/aides-territoires-prod/backers/cerema_logo.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=SCWJ1T6VQNR6Z83FSYEB%2F20210414%2Ffr-par%2Fs3%2Faws4_request&amp;X-Amz-Date=20210414T150853Z&amp;X-Amz-Expires=3600&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=76cfbce1f4f15e4850d80d1804b16061bd7635042ddfe32b7911414c2aba8b3f" alt="Logo : CEREMA ">
                        
                    </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.agencedusport.fr/" target="_blank">
                    
                        
                        <img src="https://aides-territoires-prod.s3.fr-par.scw.cloud/aides-territoires-prod/backers/agence-nationale-du-sport_logo.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=SCWJ1T6VQNR6Z83FSYEB%2F20210414%2Ffr-par%2Fs3%2Faws4_request&amp;X-Amz-Date=20210414T150849Z&amp;X-Amz-Expires=3600&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=b16410c3498ba07a8149f98fa63ac2c43510c2bf63d1297d035629afae6b05eb" alt="Logo : Agence nationale du Sport ">
                        
                    </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/pages-personnalisees/](https://aides-territoires.beta.gouv.fr/pages-personnalisees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/pages-personnalisees/](https://aides-territoires.beta.gouv.fr/pages-personnalisees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d49e-copie-08h23-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/d49e-copie-08h23-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8be3-copie-08h20-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/8be3-copie-08h20-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d0c9-copie-08h18-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/d0c9-copie-08h18-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/f240-copie-08h16-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/f240-copie-08h16-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="audience" action="/recherche/formulaire/territoire/" method="GET">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/dcba-copie-08h24-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/dcba-copie-08h24-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/b953-copie-08h19-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/b953-copie-08h19-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/bd77-copie-08h17-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/bd77-copie-08h17-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/](https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/5ba4-copie-08h14-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/5ba4-copie-08h14-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c75f-copie-08h15-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/c75f-copie-08h15-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "currentUrl" ].</p>
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8be3-copie-08h20-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/8be3-copie-08h20-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d0c9-copie-08h18-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/d0c9-copie-08h18-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/f240-copie-08h16-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/f240-copie-08h16-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c75f-copie-08h15-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/c75f-copie-08h15-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/dcba-copie-08h24-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/dcba-copie-08h24-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/b953-copie-08h19-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/b953-copie-08h19-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/bd77-copie-08h17-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/bd77-copie-08h17-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d49e-copie-08h23-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/d49e-copie-08h23-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/](https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/)
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/pages-personnalisees/](https://aides-territoires.beta.gouv.fr/pages-personnalisees/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
Instances: 11
  
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
<p>Warnings:</p><p>1:748: The child-src directive is deprecated as of CSP level 3. Authors who wish to regulate nested browsing contexts and workers SHOULD use the frame-src and worker-src directives, respectively.</p><p></p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'; connect-src 'self' http://*.hotjar.com:* https://*.hotjar.com:* http://*.hotjar.io https://*.hotjar.io wss://*.hotjar.com; font-src 'self' http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; frame-src https://stats.data.gouv.fr https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io 'self'; frame-ancestors *; img-src 'self' data: https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io https://*.scw.cloud; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://stats.data.gouv.fr http://*.hotjar.com https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; style-src 'self' 'unsafe-inline' https://stats.beta.gouv.fr; base-uri 'self'; child-src https://*.hotjar.com http://*.hotjar.io https://*.hotjar.io; form-action 'self' https://my.sendinblue.com;`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d34e-realiser-sa-demarche-devaluation-locale-actio/](https://aides-territoires.beta.gouv.fr/aides/d34e-realiser-sa-demarche-devaluation-locale-actio/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt](https://aides-territoires.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
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

  
  
  
  
### Private IP Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>A private IP (such as 10.x.x.x, 172.x.x.x, 192.168.x.x) or an Amazon EC2 private hostname (for example, ip-10-0-56-78) has been found in the HTTP response body. This information might be helpful for further attacks targeting internal systems.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e52f-accompagner-les-territoires-a-la-creation-dun/](https://aides-territoires.beta.gouv.fr/aides/e52f-accompagner-les-territoires-a-la-creation-dun/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e6f9-mettre-en-place-une-offre-de-mobilite-pour-le/](https://aides-territoires.beta.gouv.fr/aides/e6f9-mettre-en-place-une-offre-de-mobilite-pour-le/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8745-former-des-conseillers-mobilite/](https://aides-territoires.beta.gouv.fr/aides/8745-former-des-conseillers-mobilite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/65c1-developper-une-ecode-de-conduite-a-statut-ass/](https://aides-territoires.beta.gouv.fr/aides/65c1-developper-une-ecode-de-conduite-a-statut-ass/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove the private IP address from the HTTP response body.  For comments, use JSP/ASP/PHP comment instead of HTML/JavaScript comment which can be seen by client browsers.</p>
  
### Other information
<p>10.33.93.11</p><p></p>
  
### Reference
* https://tools.ietf.org/html/rfc1918

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/broadcast/11984-Aides-Territoires-qu-est-ce-que-c-est`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nQwHILnA5dQeXtMWLIlt3Xkd9LsTpmkMf43K7p44H3TXkZSQvGDstpzEds0i7vsO`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Evidence: `A9es-pour-une-reprise-sur-Aides-territoires`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/pages-personnalisees/](https://aides-territoires.beta.gouv.fr/pages-personnalisees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nQwHILnA5dQeXtMWLIlt3Xkd9LsTpmkMf43K7p44H3TXkZSQvGDstpzEds0i7vsO`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/broadcast/11984-Aides-Territoires-qu-est-ce-que-c-est`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>~�ۮ��q�-�]}󏀉׬�7��+h������z�~q調���-</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected 3 times, the first in the element starting with: "if(conv!==true){if(conv&&s.throws){response=conv(response);}else{try{response=conv(response);}catch(e){return{state:"parsererror", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.e594d37f92b6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+expando+"'></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><img src="https://stats.data.gouv.fr/piwik.php?idsite=62&idgoal=" style="border:0;" alt="" /></noscript>`
  
  
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/publications/](https://aides-territoires.beta.gouv.fr/aides/publications/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt](https://aides-territoires.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/b953-copie-08h19-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/b953-copie-08h19-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/dcba-copie-08h24-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/dcba-copie-08h24-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/](https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210413`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8be3-copie-08h20-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/8be3-copie-08h20-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d49e-copie-08h23-favoriser-lacces-a-des-aliments-f/](https://aides-territoires.beta.gouv.fr/aides/d49e-copie-08h23-favoriser-lacces-a-des-aliments-f/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/](https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.2d7dcb1fb77c.css](https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.2d7dcb1fb77c.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23009688`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=epci](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=epci)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=department](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=department)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=private_sector](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=private_sector)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?action=search](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?action=search)
  
  
  * Method: `GET`
  
  
  * Parameter: `action`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/?next=/aides/publications/](https://aides-territoires.beta.gouv.fr/comptes/inscription/?next=/aides/publications/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=region](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=region)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?action=search](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?action=search)
  
  
  * Method: `GET`
  
  
  * Parameter: `action`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=commune](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=commune)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?action=search](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?action=search)
  
  
  * Method: `GET`
  
  
  * Parameter: `action`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=association](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=association)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=public_org](https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=public_org)
  
  
  * Method: `GET`
  
  
  * Parameter: `targeted_audiences`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://aides-territoires.beta.gouv.fr/recherche/formulaire/territoire/?targeted_audiences=epci</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>targeted_audiences=epci</p><p></p><p>The user-controlled value was:</p><p>epci</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

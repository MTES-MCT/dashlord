
# ZAP Scanning Report

Generated on Mon, 5 Apr 2021 00:33:49


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 9 |
| Low | 12 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 25 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| Vulnerable JS Library | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 9 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cookie Without SameSite Attribute | Low | 12 | 
| Cookie Without Secure Flag | Low | 1 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| CSP: Notices | Low | 3 | 
| Dangerous JS Functions | Low | 12 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| In Page Banner Information Leak | Low | 1 | 
| Secure Pages Include Mixed Content | Low | 3 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 10 | 
| Loosely Scoped Cookie | Informational | 2 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 2 | 
| Retrieved from Cache | Informational | 12 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 11 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 8 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `6752327287603`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `57854713748384`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4415983141157`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `572556761219`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4261528619335`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4373451715624`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `38075171122318`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `5668659208242`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `5855532271089`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `36983992236583`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4139551457064`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `36976191150654`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4060815780879`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4095759414788`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4750993696398`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4820754235718`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4390895648625`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4221873228298`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4698129589674`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/05/05/coronavirus-age-mortalite-departements-pays-suivez-l-evolution-de-l-epidemie-en-cartes-et-graphiques_6038751_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `38111943351032`
  
  
  
  
Instances: 25
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 675232</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.lemonde.fr/coronavirus-2019-ncov/](https://www.lemonde.fr/coronavirus-2019-ncov/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-login.php](https://www.lemonde.fr/blog/*/wp-login.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/](https://www.lemonde.fr/recherche/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-includes/](https://www.lemonde.fr/blog/*/wp-includes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-register.php](https://www.lemonde.fr/blog/*/wp-register.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/archives/](https://www.lemonde.fr/archives/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-content/themes/](https://www.lemonde.fr/blog/*/wp-content/themes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-content/plugins/](https://www.lemonde.fr/blog/*/wp-content/plugins/)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://www.lemonde.fr/manifest.json](https://www.lemonde.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/smartTag.bundle.js](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/smartTag.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/css/fonts_last.css](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/css/fonts_last.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/vendor.bundle.js](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/vendor.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/dist/assets/img/logos/favicon.ico](https://www.lemonde.fr/dist/assets/img/logos/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/dist/assets/img/logos/icon-60.png](https://www.lemonde.fr/dist/assets/img/logos/icon-60.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/dist/assets/img/logos/pwa-180.png](https://www.lemonde.fr/dist/assets/img/logos/pwa-180.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/css/styles.css](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/css/styles.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/common.bundle.js](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/common.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/css/icons.css](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/css/icons.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/dist/assets/img/logos/icon-76.png](https://www.lemonde.fr/dist/assets/img/logos/icon-76.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/batch_load.bundle.js](https://www.lemonde.fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/batch_load.bundle.js)
  
  
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

  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/api/](https://www.lemonde.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/txt/](https://www.lemonde.fr/txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a rel="noopener" target="_blank" data-target="jelec-header" style=" background-image: url('/thumbnail/journal/20210406/276/201?5391941'); "  href="https://journal.lemonde.fr" id="jelec_link" class="Header__jelec"> <p>Consulter<br/>le journal</p> </a>`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a rel="noopener" target="_blank" data-target="jelec-header" style=" background-image: url('/thumbnail/journal/20210406/276/201?5391941'); "  href="https://journal.lemonde.fr" id="jelec_link" class="Header__jelec"> <p>Consulter<br/>le journal</p> </a>`
  
  
  
  
* URL: [https://www.lemonde.fr/noscript/](https://www.lemonde.fr/noscript/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/petites-annonces/](https://www.lemonde.fr/petites-annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/verification/source/](https://www.lemonde.fr/verification/source/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/element/commun/afficher/](https://www.lemonde.fr/element/commun/afficher/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="footer__link" href="https://codespromo.lemonde.fr/" rel="noopener" target="_blank">Codes Promo</a>`
  
  
  
  
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
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" href="android-app://com.lemonde.androidapp/lmfr/?x4=8"/>`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" href="ios-app://294047850/lmfr/?x4=8"/>`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" href="android-app://com.lemonde.androidapp/lmfr/?x4=8"/>`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type='text/javascript' src='https://stats.wp.com/e-202114.js' async='async' defer='defer'></script>`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" href="ios-app://294047850/lmfr/?x4=8"/>`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="http://gmpg.org/xfn/11">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='twentyseventeen-fonts-css'  href='https://fonts.googleapis.com/css?family=Libre+Franklin%3A300%2C300i%2C400%2C400i%2C600%2C600i%2C800%2C800i&#038;subset=latin%2Clatin-ext' type='text/css' media='all' />`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.gstatic.com' crossorigin rel='preconnect' />`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type='text/javascript' src='https://s0.wp.com/wp-content/js/devicepx-jetpack.js?ver=202114'></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='wpsr_sb_icon_css-css'  href='https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css?ver=4.1.7' type='text/css' media='all' />`
  
  
  
  
Instances: 10
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 1.12.4 is vulnerable.</p>
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-includes/js/jquery/jquery.js?ver=1.12.4-wp](https://www.lemonde.fr/blog/wp-includes/js/jquery/jquery.js?ver=1.12.4-wp)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v1.12.4`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.lemonde.fr/blog/filiu/2021/03/28/les-succes-du-maroc-dans-sa-vaccination-anti-covid19/](https://www.lemonde.fr/blog/filiu/2021/03/28/les-succes-du-maroc-dans-sa-vaccination-anti-covid19/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/](https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/memorable/](https://www.lemonde.fr/memorable/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/cartooningforpeace/2021/04/02/bresil-desordre-in-progress/](https://www.lemonde.fr/blog/cartooningforpeace/2021/04/02/bresil-desordre-in-progress/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/memorable/?rfextension=MK_HP](https://www.lemonde.fr/memorable/?rfextension=MK_HP)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/uneanneeaulycee/2021/04/02/tendanciel/](https://www.lemonde.fr/blog/uneanneeaulycee/2021/04/02/tendanciel/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/confidentialite/](https://www.lemonde.fr/confidentialite/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/memorable/?rfextension=MK_ART](https://www.lemonde.fr/memorable/?rfextension=MK_ART)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/](https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 9
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.lemonde.fr/resultats-elections/](https://www.lemonde.fr/resultats-elections/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="election__search " action="" method="post" onsubmit="return false;">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.lemonde.fr/blog/">`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/](https://www.lemonde.fr/recherche/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name="search" id="search_form" method="get" autocomplete="off">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-login.php](https://www.lemonde.fr/blog/*/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name="loginform" id="loginform" action="https://www.lemonde.fr/blog/wp-login.php" method="post">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/](https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.lemonde.fr/blog/autourduciel" method="get">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/](https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.lemonde.fr/blog/autourduciel/wp-comments-post.php" method="post" id="commentform" class="comment-form" novalidate>`
  
  
  
  
* URL: [https://www.lemonde.fr/planete/live/2021/03/17/club-de-l-economie-dialogue-avec-bill-gates-sur-l-urgence-climatique_6073501_3244.html](https://www.lemonde.fr/planete/live/2021/03/17/club-de-l-economie-dialogue-avec-bill-gates-sur-l-urgence-climatique_6073501_3244.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="form-live" class="form" method="get" action="https://apiv1secure.scribblelive.com/event/2956505">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/](https://www.lemonde.fr/blog/autourduciel/2021/04/01/observez-le-ciel-davril-et-le-retour-des-planetes-brillantes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.lemonde.fr/blog/autourduciel/">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/](https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.lemonde.fr/blog/realitesbiomedicales/">`
  
  
  
  
* URL: [https://www.lemonde.fr/verification/](https://www.lemonde.fr/verification/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form__verification" id="js-verificator-search-form">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/author/admin/](https://www.lemonde.fr/blog/*/author/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form role="search" method="get" class="search-form" action="https://www.lemonde.fr/blog/">`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/](https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.lemonde.fr/blog/realitesbiomedicales/wp-comments-post.php" method="post" id="commentform" class="comment-form" novalidate>`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "js-city-input" ].</p>
  
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
  
  
  
* URL: [https://www.lemonde.fr/planete/live/2021/03/17/club-de-l-economie-dialogue-avec-bill-gates-sur-l-urgence-climatique_6073501_3244.html](https://www.lemonde.fr/planete/live/2021/03/17/club-de-l-economie-dialogue-avec-bill-gates-sur-l-urgence-climatique_6073501_3244.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-live-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-live-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/international/video/2021/04/04/mercenaires-russes-wagner-enquete-video-sur-l-armee-fantome-de-vladimir-poutine_6075520_3210.html](https://www.lemonde.fr/international/video/2021/04/04/mercenaires-russes-wagner-enquete-video-sur-l-armee-fantome-de-vladimir-poutine_6075520_3210.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-video-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-video-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/le-monde-et-vous/](https://www.lemonde.fr/le-monde-et-vous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-trust-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-trust-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/guides-d-achat/article/2021/04/01/les-meilleures-boites-de-rangement-alimentaire_6075214_5306571.html](https://www.lemonde.fr/guides-d-achat/article/2021/04/01/les-meilleures-boites-de-rangement-alimentaire_6075214_5306571.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-wirecutter-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-wirecutter-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `lmd_gdpr_token`
  
  
  * Evidence: `Set-Cookie: lmd_gdpr_token`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-login.php](https://www.lemonde.fr/blog/*/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://www.lemonde.fr/m-le-mag/article/2021/04/02/couleurs-coupes-clandestines-apprentissage-du-ciseau-des-coiffeurs-et-des-cheveux-en-temps-de-pandemie_6075294_4500055.html](https://www.lemonde.fr/m-le-mag/article/2021/04/02/couleurs-coupes-clandestines-apprentissage-du-ciseau-des-coiffeurs-et-des-cheveux-en-temps-de-pandemie_6075294_4500055.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-longformat-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-longformat-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-home-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-home-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-home-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-home-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/guides-d-achat/article/2021/02/25/les-meilleurs-stylos-3d_6071221_5306571.html](https://www.lemonde.fr/guides-d-achat/article/2021/02/25/les-meilleurs-stylos-3d_6071221_5306571.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-wirecutter-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-wirecutter-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/economie/article/2021/04/04/le-suv-moteur-controverse-de-l-automobile_6075547_3234.html](https://www.lemonde.fr/economie/article/2021/04/04/le-suv-moteur-controverse-de-l-automobile_6075547_3234.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-article-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-article-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `lmd_gdpr_token`
  
  
  * Evidence: `Set-Cookie: lmd_gdpr_token`
  
  
  
  
Instances: 12
  
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
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.lemonde.fr/international/video/2021/04/04/mercenaires-russes-wagner-enquete-video-sur-l-armee-fantome-de-vladimir-poutine_6075520_3210.html](https://www.lemonde.fr/international/video/2021/04/04/mercenaires-russes-wagner-enquete-video-sur-l-armee-fantome-de-vladimir-poutine_6075520_3210.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-video-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-video-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/guides-d-achat/article/2021/04/01/les-meilleures-boites-de-rangement-alimentaire_6075214_5306571.html](https://www.lemonde.fr/guides-d-achat/article/2021/04/01/les-meilleures-boites-de-rangement-alimentaire_6075214_5306571.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-wirecutter-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-wirecutter-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-login.php](https://www.lemonde.fr/blog/*/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://www.lemonde.fr/le-monde-et-vous/](https://www.lemonde.fr/le-monde-et-vous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-trust-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-trust-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/planete/live/2021/03/17/club-de-l-economie-dialogue-avec-bill-gates-sur-l-urgence-climatique_6073501_3244.html](https://www.lemonde.fr/planete/live/2021/03/17/club-de-l-economie-dialogue-avec-bill-gates-sur-l-urgence-climatique_6073501_3244.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-live-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-live-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-home-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-home-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/economie/article/2021/04/04/le-suv-moteur-controverse-de-l-automobile_6075547_3234.html](https://www.lemonde.fr/economie/article/2021/04/04/le-suv-moteur-controverse-de-l-automobile_6075547_3234.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-article-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-article-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/guides-d-achat/article/2021/02/25/les-meilleurs-stylos-3d_6071221_5306571.html](https://www.lemonde.fr/guides-d-achat/article/2021/02/25/les-meilleurs-stylos-3d_6071221_5306571.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-wirecutter-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-wirecutter-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `lmd_gdpr_token`
  
  
  * Evidence: `Set-Cookie: lmd_gdpr_token`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-home-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-home-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr/m-le-mag/article/2021/04/02/couleurs-coupes-clandestines-apprentissage-du-ciseau-des-coiffeurs-et-des-cheveux-en-temps-de-pandemie_6075294_4500055.html](https://www.lemonde.fr/m-le-mag/article/2021/04/02/couleurs-coupes-clandestines-apprentissage-du-ciseau-des-coiffeurs-et-des-cheveux-en-temps-de-pandemie_6075294_4500055.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `critical-longformat-free-desktop`
  
  
  * Evidence: `Set-Cookie: critical-longformat-free-desktop`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `lmd_gdpr_token`
  
  
  * Evidence: `Set-Cookie: lmd_gdpr_token`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-login.php](https://www.lemonde.fr/blog/wp-login.php)
  
  
  * Method: `POST`
  
  
  * Parameter: `tk_ai`
  
  
  * Evidence: `Set-Cookie: tk_ai`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/tcfv2-stub.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/tcfv2-stub.min.js"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/tcfv2-stub.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/tcfv2-stub.min.js"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/lemonde.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/lemonde.min.js" async="1"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/tcfv2-stub.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/tcfv2-stub.min.js"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/lemonde.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/lemonde.min.js" async="1"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/tcfv2-stub.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/tcfv2-stub.min.js"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/lemonde.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/lemonde.min.js" async="1"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/lemonde.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/lemonde.min.js" async="1"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/tcfv2-stub.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/tcfv2-stub.min.js"></script>`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `//cmp.lemonde.fr/js/lemonde.min.js`
  
  
  * Evidence: `<script type="text/javascript" src="//cmp.lemonde.fr/js/lemonde.min.js" async="1"></script>`
  
  
  
  
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
<p>Warnings:</p><p>1:277: The child-src directive is deprecated as of CSP level 3. Authors who wish to regulate nested browsing contexts and workers SHOULD use the frame-src and worker-src directives, respectively.</p><p>1:327: The block-all-mixed-content directive is an experimental directive that will be likely added to the CSP specification.</p><p></p>
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss:; media-src https: blob:; object-src https:; child-src https: data: blob:; form-action https:; block-all-mixed-content;`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2020/12/01/combien-de-vaccins-quand-seront-ils-disponibles-seront-ils-obligatoires-peuvent-ils-mettre-fin-l-epidemie-de-covid-19-nos-reponses-a-vos-questions_6061795_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2020/12/01/combien-de-vaccins-quand-seront-ils-disponibles-seront-ils-obligatoires-peuvent-ils-mettre-fin-l-epidemie-de-covid-19-nos-reponses-a-vos-questions_6061795_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/aurelie-blondel/](https://www.lemonde.fr/signataires/aurelie-blondel/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/jean-guillaume-santi/](https://www.lemonde.fr/signataires/jean-guillaume-santi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/les-decodeurs/article/2021/03/29/un-policier-ivoirien-mais-pas-irlandais-un-israelien-de-16-ans-mais-personne-en-haiti-qui-peut-avoir-acces-au-vaccin-contre-le-covid-19_6074883_4355770.html](https://www.lemonde.fr/les-decodeurs/article/2021/03/29/un-policier-ivoirien-mais-pas-irlandais-un-israelien-de-16-ans-mais-personne-en-haiti-qui-peut-avoir-acces-au-vaccin-contre-le-covid-19_6074883_4355770.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/gary-dagorn/](https://www.lemonde.fr/signataires/gary-dagorn/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/philippe-dagen/](https://www.lemonde.fr/signataires/philippe-dagen/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/martine-valo/](https://www.lemonde.fr/signataires/martine-valo/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/le-monde-et-vous/article/2021/02/12/l-histoire-du-monde-au-fil-des-annees_6069693_6065879.html](https://www.lemonde.fr/le-monde-et-vous/article/2021/02/12/l-histoire-du-monde-au-fil-des-annees_6069693_6065879.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/mattea-battaglia/](https://www.lemonde.fr/signataires/mattea-battaglia/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/signataires/agathe-beaudouin/](https://www.lemonde.fr/signataires/agathe-beaudouin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-includes/js/jquery/jquery-migrate.min.js?ver=1.4.1](https://www.lemonde.fr/blog/wp-includes/js/jquery/jquery-migrate.min.js?ver=1.4.1)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-includes/js/jquery/jquery.js?ver=1.12.4-wp](https://www.lemonde.fr/blog/wp-includes/js/jquery/jquery.js?ver=1.12.4-wp)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/ajah/](https://www.lemonde.fr/ajah/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/verification/source/](https://www.lemonde.fr/verification/source/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/txt/](https://www.lemonde.fr/txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/api/](https://www.lemonde.fr/api/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/element/commun/afficher/](https://www.lemonde.fr/element/commun/afficher/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/petites-annonces/](https://www.lemonde.fr/petites-annonces/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
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
  
  
  
* URL: [https://www.lemonde.fr/violences-sexuelles/](https://www.lemonde.fr/violences-sexuelles/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/joe-biden/](https://www.lemonde.fr/joe-biden/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/troisieme-confinement/](https://www.lemonde.fr/troisieme-confinement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/coronavirus-2019-ncov/](https://www.lemonde.fr/coronavirus-2019-ncov/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/](https://www.lemonde.fr/recherche/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-login.php](https://www.lemonde.fr/blog/*/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/vaccins-contre-le-covid-19/](https://www.lemonde.fr/vaccins-contre-le-covid-19/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/archives/](https://www.lemonde.fr/archives/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private, max-age=0`
  
  
  
  
* URL: [https://www.lemonde.fr/robots.txt](https://www.lemonde.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=300`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### In Page Banner Information Leak
##### Low (High)
  
  
  
  
#### Description
<p>The server returned a version banner string in the response content. Such information leaks may allow attackers to further target specific issues impacting the product and version in use.</p>
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-includes/](https://www.lemonde.fr/blog/*/wp-includes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3`
  
  
  
  
Instances: 1
  
### Solution
<p>Configure the server to prevent such information leaks. For example:</p><p>Under Tomcat this is done via the "server" directive and implementation of custom error pages.</p><p>Under Apache this is done via the "ServerSignature" and "ServerTokens" directives.</p>
  
### Other information
<p>There is a chance that the highlight in the finding is on a value in the headers, versus the actual matched string in the response body.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/08-Testing_for_Error_Handling/

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.lemonde.fr/blog/uneanneeaulycee/2021/04/02/tendanciel/](https://www.lemonde.fr/blog/uneanneeaulycee/2021/04/02/tendanciel/)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://uneanneeaulycee.blog.lemonde.fr/files/2016/11/CV_ANNEE-LYCEE-01.jpg`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/cartooningforpeace/2021/04/02/bresil-desordre-in-progress/](https://www.lemonde.fr/blog/cartooningforpeace/2021/04/02/bresil-desordre-in-progress/)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://cartooningforpeace.blog.lemonde.fr/files/2015/10/facebook.jpg`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/](https://www.lemonde.fr/blog/realitesbiomedicales/2021/04/01/quand-une-arete-de-poisson-provoque-dintenses-douleurs-anales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://realitesbiomedicales.blog.lemonde.fr/files/2017/03/DSC_0487_200.jpg`
  
  
  
  
Instances: 3
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://uneanneeaulycee.blog.lemonde.fr/files/2016/11/CV_ANNEE-LYCEE-01.jpg</p><p>tag=img src=http://uneanneeaulycee.blog.lemonde.fr/files/2015/09/CV_ANNEE-LYCEE-02-1.jpg</p><p>tag=img src=http://uneanneeaulycee.blog.lemonde.fr/files/2016/11/CV_ANNEE-LYCEE-03.jpg</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://www.lemonde.fr/troisieme-confinement/](https://www.lemonde.fr/troisieme-confinement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/joe-biden/](https://www.lemonde.fr/joe-biden/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/coronavirus-2019-ncov/](https://www.lemonde.fr/coronavirus-2019-ncov/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/](https://www.lemonde.fr/recherche/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/vaccins-contre-le-covid-19/](https://www.lemonde.fr/vaccins-contre-le-covid-19/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/robots.txt](https://www.lemonde.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/archives/](https://www.lemonde.fr/archives/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/violences-sexuelles/](https://www.lemonde.fr/violences-sexuelles/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/*/wp-login.php](https://www.lemonde.fr/blog/*/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
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
  
  
  
* URL: [https://www.lemonde.fr/api/](https://www.lemonde.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/petites-annonces/](https://www.lemonde.fr/petites-annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/verification/source/](https://www.lemonde.fr/verification/source/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/chartbeatMab`
  
  
  
  
* URL: [https://www.lemonde.fr/noscript/](https://www.lemonde.fr/noscript/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/bucket/6717d4136f58e435854a625727b5d493fd92154f/js/chartbeatMab`
  
  
  
  
* URL: [https://www.lemonde.fr/txt/](https://www.lemonde.fr/txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
* URL: [https://www.lemonde.fr/element/commun/afficher/](https://www.lemonde.fr/element/commun/afficher/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dist/assets/fonts/the-antiqua-b/TheAntiquaB_LT_800`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�ج�����l��'���ت����8^\x0002{b������M</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 10
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "<script>!function(t){var n={};function e(r){if(n[r])return n[r].exports;var o=n[r]={i:r,l:!1,exports:{}};return t[r].call(o.expo", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Loosely Scoped Cookie
##### Informational (Low)
  
  
  
  
#### Description
<p>Cookies can be scoped by domain or path. This check is only concerned with domain scope.The domain scope applied to a cookie determines which domains can access it. For example, a cookie can be scoped strictly to a subdomain e.g. www.nottrusted.com, or loosely scoped to a parent domain e.g. nottrusted.com. In the latter case, any subdomain of nottrusted.com can access the cookie. Loosely scoped cookies are common in mega-applications like google.com and live.com. Cookies set from a subdomain like app.foo.bar are transmitted only to that domain by the browser. However, cookies scoped to a parent-level domain may be transmitted to the parent, or any subdomain of the parent.</p>
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Always scope cookies to a FQDN (Fully Qualified Domain Name).</p>
  
### Other information
<p>The origin domain used for comparison was: </p><p>www.lemonde.fr</p><p>lmd_gdpr_token=95</p><p></p>
  
### Reference
* https://tools.ietf.org/html/rfc6265#section-4.1
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html
* http://code.google.com/p/browsersec/wiki/Part2#Same-origin_policy_for_cookies

  
#### CWE Id : 565
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.lemonde.fr/txt/](https://www.lemonde.fr/txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/verification/source/](https://www.lemonde.fr/verification/source/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/api/](https://www.lemonde.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/element/commun/afficher/](https://www.lemonde.fr/element/commun/afficher/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/noscript/](https://www.lemonde.fr/noscript/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/petites-annonces/](https://www.lemonde.fr/petites-annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="js-dropdown Burger__right-arrow" data-target="actualite" role="button" aria-expanded="false">Actualités</a>`
  
  
  
  
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
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.lemonde.fr](https://www.lemonde.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
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

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.lemonde.fr/robots.txt](https://www.lemonde.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/petites-annonces/](https://www.lemonde.fr/petites-annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/beta](https://www.lemonde.fr/beta)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.lemonde.fr/element/commun/afficher/](https://www.lemonde.fr/element/commun/afficher/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/cgi-bin/](https://www.lemonde.fr/cgi-bin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.lemonde.fr/txt/](https://www.lemonde.fr/txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/ajah/](https://www.lemonde.fr/ajah/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/verification/source/](https://www.lemonde.fr/verification/source/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.lemonde.fr/api/](https://www.lemonde.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.lemonde.fr/ws/1/live/](https://www.lemonde.fr/ws/1/live/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.lemonde.fr/robots.txt](https://www.lemonde.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.lemonde.fr/api/](https://www.lemonde.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.lemonde.fr/element/commun/afficher/](https://www.lemonde.fr/element/commun/afficher/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.lemonde.fr/ws/1/related_content/](https://www.lemonde.fr/ws/1/related_content/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.lemonde.fr/beta](https://www.lemonde.fr/beta)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=120`
  
  
  
  
* URL: [https://www.lemonde.fr/ajah/](https://www.lemonde.fr/ajah/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=30`
  
  
  
  
* URL: [https://www.lemonde.fr/sitemap.xml](https://www.lemonde.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.lemonde.fr/cgi-bin/](https://www.lemonde.fr/cgi-bin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `15394037`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1201713756`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `294047850`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20131207`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210406`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `128139881`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `797055342`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `701890508`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `589280245`
  
  
  
  
* URL: [https://www.lemonde.fr/](https://www.lemonde.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `522556215`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>15394037, which evaluates to: 1970-06-28 04:07:17</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944](https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944)
  
  
  * Method: `GET`
  
  
  * Parameter: `end_at`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-login.php?action=lostpassword](https://www.lemonde.fr/blog/wp-login.php?action=lostpassword)
  
  
  * Method: `GET`
  
  
  * Parameter: `action`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-login.php?action=lostpassword](https://www.lemonde.fr/blog/wp-login.php?action=lostpassword)
  
  
  * Method: `GET`
  
  
  * Parameter: `action`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944](https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944)
  
  
  * Method: `GET`
  
  
  * Parameter: `start_at`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Fwww.lemonde.fr%2Fblog%2F%2A%2Fwp-admin%2F](https://www.lemonde.fr/blog/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Fwww.lemonde.fr%2Fblog%2F%2A%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944](https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944)
  
  
  * Method: `GET`
  
  
  * Parameter: `search_sort`
  
  
  
  
* URL: [https://www.lemonde.fr/blog/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Fwww.lemonde.fr%2Fblog%2F%2A%2Fwp-admin%2F](https://www.lemonde.fr/blog/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Fwww.lemonde.fr%2Fblog%2F%2A%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944](https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944)
  
  
  * Method: `GET`
  
  
  * Parameter: `search_keywords`
  
  
  
  
Instances: 8
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.lemonde.fr/recherche/?end_at=05%2F04%2F2021&search_keywords=ZAP&search_sort=relevance_desc&start_at=19%2F12%2F1944</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>end_at=05/04/2021</p><p></p><p>The user-controlled value was:</p><p>05/04/2021</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

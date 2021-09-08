
# ZAP Scanning Report

Generated on Wed, 8 Sep 2021 15:12:19


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 6 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Cross-Domain Misconfiguration | Medium | 5 | 
| Reverse Tabnabbing | Medium | 2 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 2 | 
| Permissions Policy Header Not Set | Low | 5 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 10 | 
| Strict-Transport-Security Header Not Set | Low | 10 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 8 | 
| Modern Web Application | Informational | 1 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/robots.txt](https://partaj.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/sitemap.xml](https://partaj.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg](https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css](https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg](https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg](https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr" target="_blank">Le réseau beta.gouv</a>`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr" target="_blank">Le réseau beta.gouv</a>`
  
  
  
  
Instances: 2
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/robots.txt](https://partaj.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/sitemap.xml](https://partaj.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/sitemap.xml](https://partaj.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg](https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/robots.txt](https://partaj.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg](https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css](https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg](https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/accounts/login](https://partaj.beta.gouv.fr/accounts/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `gunicorn/19.9.0`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg](https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/robots.txt](https://partaj.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/accounts/login](https://partaj.beta.gouv.fr/accounts/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css](https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/sitemap.xml](https://partaj.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg](https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg](https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `tCb5tq6p3rAuoolvSTQwt4gp33PMMcMCGoc9srzZ5JeICIkD7XEuh56s8jIazLEm`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `vYHY8StuPxP7ijWn9RH6tpZHyJZ9RL8g80y73wZCsvbx0SGCpHkKgaA1tFiqtg16`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `vYHY8StuPxP7ijWn9RH6tpZHyJZ9RL8g80y73wZCsvbx0SGCpHkKgaA1tFiqtg16`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�&����ް.��oI40��)�s�1�\x0002\x001a�=���䗈\x0008�\x0003�q.����2\x001a̱&</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bWHERE\b and was detected in the element starting with: "<!--</p><p>      Fix a nasty issue in Safari where it is impossible to make a table-row into a containing block. When we then stretch</p><p>", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FROM`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 6
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "*/!function(){"use strict";var o=!("undefined"==typeof window||!window.document||!window.document.createElement),i={canUseDOM:o,", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/accounts/login](https://partaj.beta.gouv.fr/accounts/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/robots.txt](https://partaj.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg](https://partaj.beta.gouv.fr/static/core/img/logo-marianne.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg](https://partaj.beta.gouv.fr/static/core/img/point-beta-gouv-fr.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg](https://partaj.beta.gouv.fr/static/core/img/logo-fabrique-numerique.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/sitemap.xml](https://partaj.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css](https://partaj.beta.gouv.fr/static/css/styles.bb07796e3a18.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
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
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr](https://partaj.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/](https://partaj.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js](https://partaj.beta.gouv.fr/static/js/index.bfc07a5a54de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1073741823, which evaluates to: 2004-01-10 13:37:03</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 00:53:30


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 5 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 6 | 
| Reverse Tabnabbing | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 8 | 
| Vulnerable JS Library | Medium | 2 | 
| Cookie without SameSite Attribute | Low | 5 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 5 | 
| Dangerous JS Functions | Low | 1 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Base64 Disclosure | Informational | 7 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 9 | 
| Non-Storable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step2/d3D2YpvkAFdQz10syLbZMQq8KPtAhH](https://proprietaire.dossierfacile.fr/registerOwner/step2/d3D2YpvkAFdQz10syLbZMQq8KPtAhH)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/mot-de-passe-oublie](https://proprietaire.dossierfacile.fr/mot-de-passe-oublie)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-bleu-clair" href="https://www.anil.org/" target="_blank">
                                En savoir plus
                            </a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="text-bleu-clair" href="https://www.anil.org/" target="_blank">
                                En savoir plus
                            </a>`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:200,300,400,400i,500,600,700" rel="stylesheet"/>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:200,300,400,400i,600,700" rel="stylesheet"
          type="text/css"/>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:200,300,400,400i,500,600,700" rel="stylesheet"/>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:200,300,400,400i,600,700" rel="stylesheet"
          type="text/css"/>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet"/>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet"/>`
  
  
  
  
Instances: 8
  
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
<p>The identified library jquery, version 3.1.1.min is vulnerable.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js](https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `jquery-3.1.1.min.js`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/bootstrap.js](https://proprietaire.dossierfacile.fr/js/bootstrap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v3.3.7`
  
  
  
  
Instances: 2
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p>CVE-2019-11358</p><p></p>
  
### Reference
* https://blog.jquery.com/2019/04/10/jquery-3-4-0-released/
* https://nvd.nist.gov/vuln/detail/CVE-2019-11358
* https://github.com/jquery/jquery/commit/753d591aea698e57d6db58c9f722cd0808619b1b
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/reset-password](https://proprietaire.dossierfacile.fr/reset-password)
  
  
  * Method: `POST`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/robots.txt](https://proprietaire.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=UA-50823626-2`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/mot-de-passe-oublie](https://proprietaire.dossierfacile.fr/mot-de-passe-oublie)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=UA-50823626-2`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=UA-50823626-2`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=UA-50823626-2`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=UA-50823626-2`
  
  
  * Evidence: `<script async="async" src="https://www.googletagmanager.com/gtag/js?id=UA-50823626-2"></script>`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js](https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/smooth-scroll.min.js](https://proprietaire.dossierfacile.fr/js/smooth-scroll.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/parallax.js](https://proprietaire.dossierfacile.fr/js/parallax.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/flickity.min.js](https://proprietaire.dossierfacile.fr/js/flickity.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/easypiechart.min.js](https://proprietaire.dossierfacile.fr/js/easypiechart.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js](https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/bootstrap.js](https://proprietaire.dossierfacile.fr/js/bootstrap.js)
  
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/sitemap.xml](https://proprietaire.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/robots.txt](https://proprietaire.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/css/bootstrap4.css](https://proprietaire.dossierfacile.fr/css/bootstrap4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/assets/images/favicons/android-chrome-192x192.png](https://proprietaire.dossierfacile.fr/assets/images/favicons/android-chrome-192x192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/webjars/font-awesome/5.11.2/css/fontawesome.min.css](https://proprietaire.dossierfacile.fr/webjars/font-awesome/5.11.2/css/fontawesome.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/home](https://proprietaire.dossierfacile.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/css/socicon.css](https://proprietaire.dossierfacile.fr/css/socicon.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.0`
  
  
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `4OOE91l6UNYCAnvnxQfNEnybmxX1QGAh05KkgvChMxw`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4OOE91l6UNYCAnvnxQfNEnybmxX1QGAh05KkgvChMxw`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `4OOE91l6UNYCAnvnxQfNEnybmxX1QGAh05KkgvChMxw`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  * Evidence: `4OOE91l6UNYCAnvnxQfNEnybmxX1QGAh05KkgvChMxw`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step2/d3D2YpvkAFdQz10syLbZMQq8KPtAhH](https://proprietaire.dossierfacile.fr/registerOwner/step2/d3D2YpvkAFdQz10syLbZMQq8KPtAhH)
  
  
  * Method: `GET`
  
  
  * Evidence: `4OOE91l6UNYCAnvnxQfNEnybmxX1QGAh05KkgvChMxw`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/mot-de-passe-oublie](https://proprietaire.dossierfacile.fr/mot-de-passe-oublie)
  
  
  * Method: `GET`
  
  
  * Evidence: `4OOE91l6UNYCAnvnxQfNEnybmxX1QGAh05KkgvChMxw`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/webjars/jquery-ui/1.12.1/jquery-ui.min.css](https://proprietaire.dossierfacile.fr/webjars/jquery-ui/1.12.1/jquery-ui.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 7
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>���YzP�\x0002\x0002{��\x0007�\x0012|��\x0015�@`!Ӓ���3\x001c</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js](https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/bootstrap.js](https://proprietaire.dossierfacile.fr/js/bootstrap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/bootstrap.js](https://proprietaire.dossierfacile.fr/js/bootstrap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/flickity.min.js](https://proprietaire.dossierfacile.fr/js/flickity.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/smooth-scroll.min.js](https://proprietaire.dossierfacile.fr/js/smooth-scroll.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FROM`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js](https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bWHERE\b and was detected 2 times, the first in the element starting with: "    // Set src attribute of element from its data-src where it was temporarily stored earlier", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="hamburger-toggle" data-toggle-class="#menu1;hidden-xs" href="#">
                            <i class="icon icon--sm stack-interface stack-menu"></i>
                        </a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step2/d3D2YpvkAFdQz10syLbZMQq8KPtAhH](https://proprietaire.dossierfacile.fr/registerOwner/step2/d3D2YpvkAFdQz10syLbZMQq8KPtAhH)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="btn btn--primary" href="#" id="hideCookie">
		<span class="btn__text">
			J'ai compris
		</span>
    </a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="hamburger-toggle" data-toggle-class="#menu1;hidden-xs" href="#">
                            <i class="icon icon--sm stack-interface stack-menu"></i>
                        </a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/scripts.js](https://proprietaire.dossierfacile.fr/js/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async defer>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js](https://proprietaire.dossierfacile.fr/js/jquery-3.1.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+u+"'></a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="hamburger-toggle" data-toggle-class="#menu1;hidden-xs" href="#">
                            <i class="icon icon--sm stack-interface stack-menu"></i>
                        </a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/webjars/jquery-ui/1.12.1/jquery-ui.min.js](https://proprietaire.dossierfacile.fr/webjars/jquery-ui/1.12.1/jquery-ui.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class='ui-datepicker-prev ui-corner-all' data-handler='prev' data-event='click' title='"+i+"'><span class='ui-icon ui-icon-circle-triangle-"+(Y?"e":"w")+"'>"+i+"</span></a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="btn btn--primary" href="#" id="hideCookie">
		<span class="btn__text">
			J'ai compris
		</span>
    </a>`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/mot-de-passe-oublie](https://proprietaire.dossierfacile.fr/mot-de-passe-oublie)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="hamburger-toggle" data-toggle-class="#menu1;hidden-xs" href="#">
                            <i class="icon icon--sm stack-interface stack-menu"></i>
                        </a>`
  
  
  
  
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
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/sitemap.xml](https://proprietaire.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/css/socicon.css](https://proprietaire.dossierfacile.fr/css/socicon.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/home](https://proprietaire.dossierfacile.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/assets/images/favicons/android-chrome-192x192.png](https://proprietaire.dossierfacile.fr/assets/images/favicons/android-chrome-192x192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/webjars/font-awesome/5.11.2/css/fontawesome.min.css](https://proprietaire.dossierfacile.fr/webjars/font-awesome/5.11.2/css/fontawesome.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/robots.txt](https://proprietaire.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/css/bootstrap4.css](https://proprietaire.dossierfacile.fr/css/bootstrap4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
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
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/css/stack-interface.css](https://proprietaire.dossierfacile.fr/css/stack-interface.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `33839631`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/](https://proprietaire.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `50823626`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `12345679`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/css/stack-interface.css](https://proprietaire.dossierfacile.fr/css/stack-interface.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `34857618`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/login](https://proprietaire.dossierfacile.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `50823626`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr](https://proprietaire.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `50823626`
  
  
  
  
* URL: [https://proprietaire.dossierfacile.fr/registerOwner/step1](https://proprietaire.dossierfacile.fr/registerOwner/step1)
  
  
  * Method: `GET`
  
  
  * Evidence: `50823626`
  
  
  
  
Instances: 7
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>33839631, which evaluates to: 1971-01-27 15:53:51</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

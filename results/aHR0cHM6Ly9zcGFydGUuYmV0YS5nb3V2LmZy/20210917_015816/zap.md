
# ZAP Scanning Report

Generated on Fri, 17 Sep 2021 01:50:03


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Application Error Disclosure | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 6 | 
| Cookie Without Secure Flag | Low | 6 | 
| Incomplete or No Cache-control Header Set | Low | 5 | 
| Information Disclosure - Debug Error Messages | Low | 12 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 8 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Non-Storable Content | Informational | 6 | 
| Storable and Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 6 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 10 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/header.png](https://sparte.beta.gouv.fr/static/header.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/favicon.ico](https://sparte.beta.gouv.fr/static/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/robots.txt](https://sparte.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoRelation.png](https://sparte.beta.gouv.fr/static/pictoRelation.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/](https://sparte.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoCopro.png](https://sparte.beta.gouv.fr/static/pictoCopro.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr](https://sparte.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/sitemap.xml](https://sparte.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/logo_france.png](https://sparte.beta.gouv.fr/static/logo_france.png)
  
  
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

  
  
  
  
### Application Error Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/nav_sidebar.css](https://sparte.beta.gouv.fr/static/admin/css/nav_sidebar.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoMap.png](https://sparte.beta.gouv.fr/static/pictoMap.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/responsive.css](https://sparte.beta.gouv.fr/static/admin/css/responsive.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/base.css](https://sparte.beta.gouv.fr/static/admin/css/base.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoRelation.png](https://sparte.beta.gouv.fr/static/pictoRelation.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/logo_france.png](https://sparte.beta.gouv.fr/static/logo_france.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/favicon.ico](https://sparte.beta.gouv.fr/static/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/login.css](https://sparte.beta.gouv.fr/static/admin/css/login.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/forms.css](https://sparte.beta.gouv.fr/static/admin/css/forms.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoCopro.png](https://sparte.beta.gouv.fr/static/pictoCopro.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/header.png](https://sparte.beta.gouv.fr/static/header.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoResource.png](https://sparte.beta.gouv.fr/static/pictoResource.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 12
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/accounts/reset/](https://sparte.beta.gouv.fr/accounts/reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/accounts/reset/](https://sparte.beta.gouv.fr/accounts/reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
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

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr](https://sparte.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/accounts/reset/](https://sparte.beta.gouv.fr/accounts/reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/accounts/reset/sent/](https://sparte.beta.gouv.fr/accounts/reset/sent/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/](https://sparte.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 5
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Debug Error Messages
##### Low (Medium)
  
  
  
  
#### Description
<p>The response appeared to contain common error messages returned by platforms such as ASP.NET, and Web-servers such as IIS and Apache. You can configure the list of common debug messages.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/header.png](https://sparte.beta.gouv.fr/static/header.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/favicon.ico](https://sparte.beta.gouv.fr/static/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/login.css](https://sparte.beta.gouv.fr/static/admin/css/login.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/base.css](https://sparte.beta.gouv.fr/static/admin/css/base.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/forms.css](https://sparte.beta.gouv.fr/static/admin/css/forms.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoRelation.png](https://sparte.beta.gouv.fr/static/pictoRelation.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/nav_sidebar.css](https://sparte.beta.gouv.fr/static/admin/css/nav_sidebar.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoResource.png](https://sparte.beta.gouv.fr/static/pictoResource.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/admin/css/responsive.css](https://sparte.beta.gouv.fr/static/admin/css/responsive.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoMap.png](https://sparte.beta.gouv.fr/static/pictoMap.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoCopro.png](https://sparte.beta.gouv.fr/static/pictoCopro.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/logo_france.png](https://sparte.beta.gouv.fr/static/logo_france.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
Instances: 12
  
### Solution
<p>Disable debugging messages before pushing to production.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/favicon.ico](https://sparte.beta.gouv.fr/static/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/robots.txt](https://sparte.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/logo_france.png](https://sparte.beta.gouv.fr/static/logo_france.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/](https://sparte.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoCopro.png](https://sparte.beta.gouv.fr/static/pictoCopro.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/header.png](https://sparte.beta.gouv.fr/static/header.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr](https://sparte.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/sitemap.xml](https://sparte.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoRelation.png](https://sparte.beta.gouv.fr/static/pictoRelation.png)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr](https://sparte.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `sha384-B0vP5xmATw1+K9KRQjQERJvTumQW0nPEzvF6L/Z6nronJ3oUOFUFpCjEUQouq2+l`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `tG14gpJ0bgj3bmZVqlk6DRVVfabeyHE6USGMjglwllimoYhC2XMGhQRfVbqV7PnP`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Evidence: `tG14gpJ0bgj3bmZVqlk6DRVVfabeyHE6USGMjglwllimoYhC2XMGhQRfVbqV7PnP`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `tG14gpJ0bgj3bmZVqlk6DRVVfabeyHE6USGMjglwllimoYhC2XMGhQRfVbqV7PnP`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/accounts/reset/](https://sparte.beta.gouv.fr/accounts/reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `tG14gpJ0bgj3bmZVqlk6DRVVfabeyHE6USGMjglwllimoYhC2XMGhQRfVbqV7PnP`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/](https://sparte.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `sha384-B0vP5xmATw1+K9KRQjQERJvTumQW0nPEzvF6L/Z6nronJ3oUOFUFpCjEUQouq2+l`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `POST`
  
  
  * Evidence: `tG14gpJ0bgj3bmZVqlk6DRVVfabeyHE6USGMjglwllimoYhC2XMGhQRfVbqV7PnP`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  * Evidence: `jjWUJS9UdZkSXueWTQhTJuiS3XcbGsSTBXVzj40Zb2asMDF8ZURxvXCuK6ZxfpMZ`
  
  
  
  
Instances: 8
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�\x0016������`\x0013�_���P�\x0001\x0011&��\x0005���3�^�������ޅ\x000e\x0015Ai</p><p>1\x0014B����</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "<script src="/static/admin/js/nav_sidebar.js" defer></script>", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoCopro.png](https://sparte.beta.gouv.fr/static/pictoCopro.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `500`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/logo_france.png](https://sparte.beta.gouv.fr/static/logo_france.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `500`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/header.png](https://sparte.beta.gouv.fr/static/header.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `500`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/favicon.ico](https://sparte.beta.gouv.fr/static/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `500`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/static/pictoRelation.png](https://sparte.beta.gouv.fr/static/pictoRelation.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `500`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://sparte.beta.gouv.fr/robots.txt](https://sparte.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr](https://sparte.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/sitemap.xml](https://sparte.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/](https://sparte.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signup/](https://sparte.beta.gouv.fr/users/signup/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `POST`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/accounts/reset/](https://sparte.beta.gouv.fr/accounts/reset/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
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
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `username`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `username`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/users/signin/](https://sparte.beta.gouv.fr/users/signin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `password`
  
  
  
  
* URL: [https://sparte.beta.gouv.fr/admin/login/?next=/admin/](https://sparte.beta.gouv.fr/admin/login/?next=/admin/)
  
  
  * Method: `POST`
  
  
  * Parameter: `password`
  
  
  
  
Instances: 10
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://sparte.beta.gouv.fr/admin/login/?next=/admin/</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>username=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

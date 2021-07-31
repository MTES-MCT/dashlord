
# ZAP Scanning Report

Generated on Sat, 31 Jul 2021 00:05:36


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 3 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| CSP: Notices | Low | 3 | 
| Incomplete or No Cache-control Header Set | Low | 5 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
| Modern Web Application | Informational | 5 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 11 | 

## Alert Detail


  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>img-src</p>
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>The report-uri directive has ben deprecated in favor of the new report-to directive</p><p></p>
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' *.gouv.fr; report-uri https://sentry.io/api/1187894/security/?sentry_key=1405fd280ebd40c78c015655056fe213;  connect-src 'self' https://sentry.io/ https://api-adresse.data.gouv.fr/; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com/; font-src 'self' https://fonts.gstatic.com/ themes.googleusercontent.com data:; script-src 'self' https://stats.data.gouv.fr/; frame-ancestors 'none'; form-action 'self'; base-uri 'self'; img-src 'self' https: data:`
  
  
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/stats](https://adock.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-transform`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b6edb.5212bb24.js](https://adock.beta.gouv.fr/js/chunk-2d0b6edb.5212bb24.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0bd39a.1b4c983a.js](https://adock.beta.gouv.fr/js/chunk-2d0bd39a.1b4c983a.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.212e28d8.js](https://adock.beta.gouv.fr/js/chunk-22c07800.212e28d8.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b9919.4ff79015.js](https://adock.beta.gouv.fr/js/chunk-2d0b9919.4ff79015.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0db095.7a3e4f05.js](https://adock.beta.gouv.fr/js/chunk-2d0db095.7a3e4f05.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789ABCDEFGHIJKLMNOPQRSTUVXYZabcdefghijklmnopqrstuvwxyz-`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/css/chunk-vendors.8d255e43.css](https://adock.beta.gouv.fr/css/chunk-vendors.8d255e43.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAQAAAADQ4RFAAACf0lEQVR4AY1UM3gkARTePdvdoTxXKc+qTl3aU5U6b2Kbkz3Gtq3Zw6ziLGNPzrYx7946Tr6/ee/XeCQ4D3ykPtL5tHno4n0d/h3+xfuWHGLX81cn7r0iTNzjr7LrlxCqPtkbTQEHeqOrTy4Yyt3VCi/IOB0v7rVC7q45Q3Gr5K6jt+3Gl5nCoDD4MtO+j96Wu8atmhGqcNGHObuf8OM/x3AMx38+4Z2sPqzCxRFK2aF2e5Jol56XTLyggAMTL56XOMoS1W4pOyjUcGGQdZxU6qRh7B9Zp+PfpOFlqt0zyDZckPi1ttmIp03jX8gyJ8a/PG2yutpS/Vol7peZIbZcKBAEEheEIAgFbDkz5H6Zrkm2hVWGiXKiF4Ycw0RWKdtC16Q7qe3X4iOMxruonzegJzWaXFrU9utOSsLUmrc0YjeWYjCW4PDMADElpJSSQ0vQvA1Tm6/JlKnqFs1EGyZiFCqnRZTEJJJiKRYzVYzJck2Rm6P4iH+cmSY0YzimYa8l0EtTODFWhcMIMVqdsI2uiTvKmTisIDHJ3od5GILVhBCarCfVRmo4uTjkhrhzkiBV7SsaqS+TzrzM1qpGGUFt28pIySQHR6h7F6KSwGWm97ay+Z+ZqMcEjEWebE7wxCSQwpkhJqoZA5ivCdZDjJepuJ9IQjGGUmuXJdBFUygxVqVsxFsLMbDe8ZbDYVCGKxs+W080max1hFCarCfV+C1KATwcnvE9gRRuMP2prdbWGowm1KB1y+zwMMENkM755cJ2yPDtqhTI6ED1M/82yIDtC/4j4BijjeObflpO9I9MwXTCsSX8jWAFeHr05WoLTJ5G8IQVS/7vwR6ohirYM7f6HzYpogfS3R2OAAAAAElFTkSuQmCC`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�]�㞻��\x0001\x00081\x0005\x0018r	(�
8�\x0011I5\x0015]�Zm�^~\x0008b�If��j��n�\x000cr�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.212e28d8.js](https://adock.beta.gouv.fr/js/chunk-22c07800.212e28d8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0bd39a.1b4c983a.js](https://adock.beta.gouv.fr/js/chunk-2d0bd39a.1b4c983a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js](https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js](https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js](https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js](https://adock.beta.gouv.fr/js/chunk-vendors.6a73fbac.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FROM`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-22c07800.212e28d8.js](https://adock.beta.gouv.fr/js/chunk-22c07800.212e28d8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 9
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bWHERE\b and was detected in the element starting with: "(function(t,n){e.exports=n(function(){try{return a("c1df")}catch(e){}}())})(0,(function(e){"use strict";function t(e,t){return t", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.6a73fbac.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.6a73fbac.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.6a73fbac.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.6a73fbac.js"></script>`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/stats](https://adock.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.6a73fbac.js"></script>`
  
  
  
  
Instances: 5
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/favicon.ico](https://adock.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b9919.4ff79015.js](https://adock.beta.gouv.fr/js/chunk-2d0b9919.4ff79015.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/](https://adock.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/sitemap.xml](https://adock.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr](https://adock.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0db095.7a3e4f05.js](https://adock.beta.gouv.fr/js/chunk-2d0db095.7a3e4f05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0bd39a.1b4c983a.js](https://adock.beta.gouv.fr/js/chunk-2d0bd39a.1b4c983a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/css/app.1cc66a26.css](https://adock.beta.gouv.fr/css/app.1cc66a26.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/robots.txt](https://adock.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d0b6edb.5212bb24.js](https://adock.beta.gouv.fr/js/chunk-2d0b6edb.5212bb24.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `187978997`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15496570`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1753920856`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20037508`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23592600`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20191221`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `40075017`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/app.f6acb6cb.js](https://adock.beta.gouv.fr/js/app.f6acb6cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `683582885`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18764656`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0511287798`
  
  
  
  
* URL: [https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js](https://adock.beta.gouv.fr/js/chunk-2d2248b6.5252c7d3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `314245179`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>187978997, which evaluates to: 1975-12-16 16:23:17</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

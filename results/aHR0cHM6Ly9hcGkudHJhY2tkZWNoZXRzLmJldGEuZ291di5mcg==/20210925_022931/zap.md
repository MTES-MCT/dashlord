
# ZAP Scanning Report

Generated on Sat, 25 Sep 2021 02:21:32


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 3 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Permissions Policy Header Not Set | Low | 4 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 4 | 
| Strict-Transport-Security Header Not Set | Low | 4 | 
| Base64 Disclosure | Informational | 2 | 
| Non-Storable Content | Informational | 2 | 
| Storable and Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `12-7JEJwpG8g89ii7CR/6hhfN27Q+k`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `12-7JEJwpG8g89ii7CR/6hhfN27Q+k`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�o�$Bp�o �آ�$�\x0018_7n��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `400`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `400`
  
  
  
  
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
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1632536496`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1632536496`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1632536496`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1632536496`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1632536496, which evaluates to: 2021-09-25 02:21:36</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

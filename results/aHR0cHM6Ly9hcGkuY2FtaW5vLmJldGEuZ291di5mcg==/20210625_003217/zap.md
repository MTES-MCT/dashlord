
# ZAP Scanning Report

Generated on Fri, 25 Jun 2021 00:26:40


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 4 |
| Informational | 2 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Cross-Domain Misconfiguration | Medium | 8 | 
| Incomplete or No Cache-control Header Set | Low | 4 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 8 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 8 | 
| X-Content-Type-Options Header Missing | Low | 4 | 
| Non-Storable Content | Informational | 4 | 
| Storable and Cacheable Content | Informational | 4 | 

## Alert Detail


  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://api.camino.beta.gouv.fr/sitemap.xml](https://api.camino.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/](https://api.camino.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `POST`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `POST`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 4
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/sitemap.xml](https://api.camino.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `POST`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/](https://api.camino.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `POST`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `POST`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/sitemap.xml](https://api.camino.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/](https://api.camino.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `POST`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.2`
  
  
  
  
Instances: 8
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://api.camino.beta.gouv.fr/sitemap.xml](https://api.camino.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `400`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `400`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/](https://api.camino.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `400`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `400`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr/robots.txt?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr](https://api.camino.beta.gouv.fr)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D](https://api.camino.beta.gouv.fr?query=%7B__schema%7Btypes%7Bname+kind+description%7D%7D%7D)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.camino.beta.gouv.fr/robots.txt](https://api.camino.beta.gouv.fr/robots.txt)
  
  
  * Method: `POST`
  
  
  
  
Instances: 4
  
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

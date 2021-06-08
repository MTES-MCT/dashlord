
# ZAP Scanning Report

Generated on Tue, 8 Jun 2021 10:35:17


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 2 |
| Informational | 1 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 4 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 4 | 
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

  
#### CWE Id : 16
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.7`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.7`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.7`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.7`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr](https://api.trackdechets.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623148530`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/](https://api.trackdechets.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623148530`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/robots.txt](https://api.trackdechets.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623148530`
  
  
  
  
* URL: [https://api.trackdechets.beta.gouv.fr/sitemap.xml](https://api.trackdechets.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623148530`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1623148530, which evaluates to: 2021-06-08 10:35:30</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

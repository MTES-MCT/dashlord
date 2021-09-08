
# ZAP Scanning Report

Generated on Wed, 8 Sep 2021 16:40:24


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 5 |
| Low | 11 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 2 | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| X-Frame-Options Header Not Set | Medium | 1 | 
| Cookie No HttpOnly Flag | Low | 10 | 
| Cookie without SameSite Attribute | Low | 6 | 
| Cookie Without Secure Flag | Low | 10 | 
| Cookie with SameSite Attribute None | Low | 4 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 1 | 
| CSP: Notices | Low | 3 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 4 | 
| Strict-Transport-Security Header Not Set | Low | 4 | 
| X-Content-Type-Options Header Missing | Low | 2 | 
| Base64 Disclosure | Informational | 9 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 1 | 
| Non-Storable Content | Informational | 4 | 
| Storable and Cacheable Content | Informational | 3 | 
| Storable but Non-Cacheable Content | Informational | 1 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `671017457538108`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `671017460652409`
  
  
  
  
Instances: 2
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 671017</p><p>Brand: MAESTRO</p><p>Category: STANDARD</p><p>Issuer: ZUERCHER KANTONALBANK</p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
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

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>manifest-src, prefetch-src</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
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

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 1
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALBCORS`
  
  
  * Evidence: `Set-Cookie: AWSALBCORS`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALBCORS`
  
  
  * Evidence: `Set-Cookie: AWSALBCORS`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALBCORS`
  
  
  * Evidence: `Set-Cookie: AWSALBCORS`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALBCORS`
  
  
  * Evidence: `Set-Cookie: AWSALBCORS`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALBCORS`
  
  
  * Evidence: `Set-Cookie: AWSALBCORS`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous)
  
  
  * Method: `GET`
  
  
  * Parameter: `AWSALB`
  
  
  * Evidence: `Set-Cookie: AWSALB`
  
  
  
  
Instances: 10
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie with SameSite Attribute None
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set with its SameSite attribute set to "none", which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/608769/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/608769/smarttag.js">
  


    
</script>`
  
  
  
  
Instances: 1
  
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
<p>Warnings:</p><p>Duplicate scheme data:</p><p>The report-uri directive has ben deprecated in favor of the new report-to directive</p><p></p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self' https://wa.anah.fr https://tag.aticdn.net; child-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; form-action 'self'; frame-ancestors 'self' https://wa.anah.fr https://tag.aticdn.net; connect-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net https://logs1409.xiti.com; font-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; frame-src data: mailto: tel: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; img-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com data: https://logs1409.xiti.com https://xiti.com; media-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; object-src data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; script-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net http://www.google-analytics.com https://ssl.google-analytics.com; style-src 'unsafe-inline' 'unsafe-eval' data: blob: filesystem: mediastream: 'self' https://wa.anah.fr https://tag.aticdn.net; default-src *;  report-uri https://www.maprimerenov.gouv.fr/prweb/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD`
  
  
  
  
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

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
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
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 2
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Evidence: `veOOAkchxGO6o/Jtf5F4ss+9gTdzzWmIbpP+yE5dZnrhs+Cq1NKGk3IUfMRZ58xHWk1MziFceLkKvza/WEHw3VdsZ79UhLeERWZkn8rbkFTzoobcaiSF9fKSs8NW`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `wbrue6nr/AD+w/XTKNAvhgNsg8Dzs+9+gkS5EAwMhI13adQ8Njwl6t389M4Q54HmJO0l5DIsQDBG6McNHQjEizzYF7lZJdWloI/BBV+/0segjJzM93Hxw1AhuGYk`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `/SGvMMylPm6Q1K7rqlsmhMj01JpfrvPwnL6TotIhrU4/mc7THwyojY+KixIYkRAfYHcI+KKS506Sja0a/hcC70u9nojSfl6aY9G/ydwFeV0G1iLXUrukomXHvnLU`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `+FWPt31Df97TDEBedMCLeL+ovYR/34mq8AwBmfezGLWvLaRRIViSrEo/xjZ4ruya9clGSFjJoAe0Ddqw8K5NxDXzEjoOJl+//kVfSPksuMhouT2P/p+gDOxBYDLN`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `DxyJZktdUvbXRJK+rcdUegMyyLtBNQX8KsnYxB9/H/amPYioNxAvSyArDFANPwP3emqJkOPGQYZW9ffBSKMXYB2IhwkPsNQd2TpCtLaf44YXSbwj246ONks65IQ8`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous)
  
  
  * Method: `GET`
  
  
  * Evidence: `5Bzhp5v6XAKuK3mqmOe5MDtsoGaNAhi1xkNEUqo/H9Xcl4BAkmPPjzXR4tko7wiDHf1+9NM//VbbhRveWBhpU5FqyaVAODyKib7VY41HcfxaOu6isfcPmqChFOma`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `qPKVn3wxC56QQ+RXWpLV2PwzN5iGfGxssCumbEvg2URv/gv2wphs/krYeOdPQcpvIWZGCwk5RibLaXp65Njy1iEnbRGPksrL+GVjlnunDUJAdb8cIs7Thhq7bDjd`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `rQuB79cJqAXpkHpON2B5QjoM1VnFp+A3TXqDqZ01AvyHTSfqlFpPH3c5TCHygQsLfLeuXruucNz9SAZwgamhK/7P9xgMQsQ/KVvpP8cfWuapYh9HcOba0X8RAB64`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `f4kcOC2Pd2El9altudlcf3RGKNr+3RhIS/8hmY4aAYHRHPOXTFPy6sDoQSr8/0pq0ZvrPykyK5Ttj/VutUjuBdbr9cxbZ5le9QzGQx4PQXvLn/quossicKrdAGfV`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��\x0002G!�c���m�x�Ͻ�7s�i�n���N]fz���҆�r\x0014|�Y��GZML�!\x�</p><p>�6�XA��Wlg�T���Efd��ېT��j$����V</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected 2 times, the first in the element starting with: "<!--Added 'user-scalable=no' to disable zoom in/out in HC/PIMC app mobile browser -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `BUG`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "<script type="text/javascript" id="webanalyticsheader"></p><p></p><p>pega.namespace("pega.webanalytics");</p><p>$.extend(pega.webanalytics, (funct", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script> /* US-250729 : Removing the skeleton in failure cases, later can be moved to desktop exception handling */ window.onerror = function() { var harnessSkeletonWrapper = document.getElementById("#harness_skeleton_wrapper"); if (harnessSkeletonWrapper) { harnessSkeletonWrapper.remove(); console.info("Removing harness skeleton wrapper"); } }; </script>`
  
  
  
  
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
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/Anonymous)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/AIDES_/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/H9DF1ufnPCNDOGG8PFgaaW3tLvvaZHE9*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD](https://www.maprimerenov.gouv.fr/prweb/PRAuth/app/default/BPNVwCpLW8TKW49zoQZpAw*/!STANDARD)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
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
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/sitemap.xml](https://www.maprimerenov.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/](https://www.maprimerenov.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/robots.txt](https://www.maprimerenov.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous](https://www.maprimerenov.gouv.fr/prweb/PRAuth/Anonymous)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Mon, 5 Apr 2021 00:38:41


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 2 |
| Medium | 8 |
| Low | 13 |
| Informational | 11 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 43 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Reverse Tabnabbing | Medium | 12 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| X-Frame-Options Header Not Set | Medium | 12 | 
| Absence of Anti-CSRF Tokens | Low | 13 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cookie Without SameSite Attribute | Low | 9 | 
| Cookie Without Secure Flag | Low | 10 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| CSP: Notices | Low | 3 | 
| Dangerous JS Functions | Low | 11 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Information Disclosure - Debug Error Messages | Low | 1 | 
| Secure Pages Include Mixed Content | Low | 1 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 12 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Content-Type Header Missing | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 10 | 
| Loosely Scoped Cookie | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Retrieved from Cache | Informational | 11 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 63 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 3 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `573258773727616`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4105581902841`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `36399750441481`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `5643206594246`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4070627151458`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `56361819787507`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `588301089731832`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `5814769756254`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `4054054054054`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `36426434420068`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `5675675675676`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `50699083606945`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `38717323009311`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `502253777930775`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `58907358430335`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `573573573573576`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `579362945818776`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `58670278630596`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `5628170617727`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `36091730912067`
  
  
  
  
Instances: 42
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 573258</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### PII Disclosure
##### High (Medium)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html](https://www.nytimes.com/interactive/2021/world/covid-vaccinations-tracker.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `57963986084516`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://www.nytimes.com/wirecutter/search](https://www.nytimes.com/wirecutter/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/wp-admin/](https://www.nytimes.com/wirecutter/wp-admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/out/link/](https://www.nytimes.com/wirecutter/out/link/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*?l](https://www.nytimes.com/wirecutter/*?l)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*.zip$](https://www.nytimes.com/wirecutter/*.zip$)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*.csv$](https://www.nytimes.com/wirecutter/*.csv$)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/data-requests](https://www.nytimes.com/wirecutter/data-requests)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*&xid=](https://www.nytimes.com/wirecutter/*&xid=)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*?q](https://www.nytimes.com/wirecutter/*?q)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/deals/beta](https://www.nytimes.com/wirecutter/deals/beta)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/ads/](https://www.nytimes.com/ads/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*?s](https://www.nytimes.com/wirecutter/*?s)
  
  
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
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
  
  
  
* URL: [https://www.nytimes.com/wirecutter/reviews/best-lawnmower/](https://www.nytimes.com/wirecutter/reviews/best-lawnmower/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.popularmechanics.com/" rel="noopener" target="_blank">Popular Mechanics</a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/search/](https://www.nytimes.com/wirecutter/search/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="_77dd8251 _39bbdf3e" target="_blank" href="https://www.facebook.com/thewirecutter/" title="Wirecutter&#x27;s Facebook" data-gtm-trigger="social_profile_link"></a>`
  
  
  
  
* URL: [https://www.nytimes.com/section/food](https://www.nytimes.com/section/food)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://itunes.apple.com/us/app/nyt-cooking-recipes-from-new/id911422904?mt=8" target="_blank">App Store</a>`
  
  
  
  
* URL: [https://www.nytimes.com/interactive/2020/admin/live-events.html](https://www.nytimes.com/interactive/2020/admin/live-events.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.morganstanley.com/" target="_blank"><img src="https://mwcm.nyt.com/dam/mkt_assets/moco/live_events/morgan-stanley-netting-zero-tech.png"/></a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/reviews/the-best-portable-air-conditioner/](https://www.nytimes.com/wirecutter/reviews/the-best-portable-air-conditioner/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.upworthy.com/she-turned-her-dads-50-year-old-fbi-file-into-a-stunning-work-of-art?c=apstream" rel="noopener" target="_blank">Upworthy</a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/wp-admin/](https://www.nytimes.com/wirecutter/wp-admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://wordpress.org/" target="_blank">WordPress</a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/](https://www.nytimes.com/wirecutter/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.staples.com/hp-officejet-pro-9015e-wireless-color-all-in-one-printer-w-6-months-free-ink-1g5l3a/product_24455373" target="_blank" rel="noopener"><span>HP OfficeJet Pro 9015e</span></a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*.csv$/](https://www.nytimes.com/wirecutter/*.csv$/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="_77dd8251 _39bbdf3e" target="_blank" href="https://www.facebook.com/thewirecutter/" title="Wirecutter&#x27;s Facebook" data-gtm-trigger="social_profile_link"></a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/reviews/best-pressure-washer/](https://www.nytimes.com/wirecutter/reviews/best-pressure-washer/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://pressurewashr.com" rel="noopener" target="_blank">PressureWashr</a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/reviews/best-gas-grill/](https://www.nytimes.com/wirecutter/reviews/best-gas-grill/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://bigapplebbq.com/" rel="noopener" target="_blank">Big Apple BBQ</a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/deals/](https://www.nytimes.com/wirecutter/deals/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="_7e5e0b10" href="https://mailchi.mp/wirecutter/dealswelove" rel="noopener" target="_blank">Get the daily deals newsletter</a>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*.zip$/](https://www.nytimes.com/wirecutter/*.zip$/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="_77dd8251 _39bbdf3e" target="_blank" href="https://www.facebook.com/thewirecutter/" title="Wirecutter&#x27;s Facebook" data-gtm-trigger="social_profile_link"></a>`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://www.nytimes.com/games-assets/v2/react-bundle.7866707cbfac7d49b9d11059cc442c2a.js](https://www.nytimes.com/games-assets/v2/react-bundle.7866707cbfac7d49b9d11059cc442c2a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `SELECT name FROM sqlite_master WHERE type`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>SELECT name FROM sqlite_master WHERE type</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://static01.nyt.com/newsgraphics/2020/03/16/coronavirus-maps/3d5bc806f17f79a8dc6825a7db6641a560a2525b/build/css/components.css" rel="stylesheet">`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-rh="true" rel="alternate" type="application/rss+xml" title="RSS" href="https://rss.nytimes.com/services/xml/rss/nyt/HomePage.xml"/>`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-rh="true" rel="alternate" href="https://cn.nytimes.com/zh-hant/" hrefLang="zh-Hant"/>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://g1.nyt.com/fonts/css/web-fonts.5810def60210a2fa7d0848f37e3fa048bb6147b1.css" rel="stylesheet" type="text/css" />`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://g1.nyt.com/fonts/css/web-fonts.5810def60210a2fa7d0848f37e3fa048bb6147b1.css" rel="stylesheet" type="text/css" />`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer src="https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x"></script>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer src="https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x"></script>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://static01.nyt.com/newsgraphics/2020/03/16/coronavirus-maps/3d5bc806f17f79a8dc6825a7db6641a560a2525b/build/css/components.css" rel="stylesheet">`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-rh="true" rel="alternate" type="application/rss+xml" title="RSS" href="https://rss.nytimes.com/services/xml/rss/nyt/HomePage.xml"/>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-rh="true" rel="alternate" href="https://cn.nytimes.com/" hrefLang="zh-Hans"/>`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-rh="true" rel="alternate" href="https://cn.nytimes.com/" hrefLang="zh-Hans"/>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-rh="true" rel="alternate" href="https://cn.nytimes.com/zh-hant/" hrefLang="zh-Hant"/>`
  
  
  
  
Instances: 12
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.nytimes.com/subscription/games?campaignId=4QHQ8](https://www.nytimes.com/subscription/games?campaignId=4QHQ8)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/section/todayspaper](https://www.nytimes.com/section/todayspaper)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap/](https://www.nytimes.com/sitemap/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/privacy-policy](https://www.nytimes.com/privacy/privacy-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/puzzles/stats](https://www.nytimes.com/puzzles/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/subscription?campaignId=37WXW](https://www.nytimes.com/subscription?campaignId=37WXW)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/international/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/international/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/crosswords](https://www.nytimes.com/crosswords)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/cookie-policy](https://www.nytimes.com/privacy/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.nytimes.com/search?query=ZAP](https://www.nytimes.com/search?query=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.nytimes.com/*?*campaignId](https://www.nytimes.com/*?*campaignId)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="css-1xv6f1u" method="get" action="/search">`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="css-s3xm4x">`
  
  
  
  
* URL: [https://www.nytimes.com/*.pdf$](https://www.nytimes.com/*.pdf$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*.pdf$](https://www.nytimes.com/*.pdf$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*campaignId](https://www.nytimes.com/*?*campaignId)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*login](https://www.nytimes.com/*?*login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="css-1xv6f1u" method="get" action="/search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*login](https://www.nytimes.com/*?*login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*searchResultPosition](https://www.nytimes.com/*?*searchResultPosition)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*searchResultPosition](https://www.nytimes.com/*?*searchResultPosition)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="search-form" role="search">`
  
  
  
  
Instances: 13
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "search-input-2" ].</p>
  
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
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-a`
  
  
  * Evidence: `Set-Cookie: nyt-a`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-purr`
  
  
  * Evidence: `Set-Cookie: nyt-purr`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-purr`
  
  
  * Evidence: `Set-Cookie: nyt-purr`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-a`
  
  
  * Evidence: `Set-Cookie: nyt-a`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-purr`
  
  
  * Evidence: `Set-Cookie: nyt-purr`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-geo`
  
  
  * Evidence: `Set-Cookie: nyt-geo`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-a`
  
  
  * Evidence: `Set-Cookie: nyt-a`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-geo`
  
  
  * Evidence: `Set-Cookie: nyt-geo`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
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
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-geo`
  
  
  * Evidence: `Set-Cookie: nyt-geo`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-a`
  
  
  * Evidence: `Set-Cookie: nyt-a`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-a`
  
  
  * Evidence: `Set-Cookie: nyt-a`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-a`
  
  
  * Evidence: `Set-Cookie: nyt-a`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-geo`
  
  
  * Evidence: `Set-Cookie: nyt-geo`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-geo`
  
  
  * Evidence: `Set-Cookie: nyt-geo`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/ads/](https://www.nytimes.com/ads/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/adx/bin/](https://www.nytimes.com/adx/bin/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-geo`
  
  
  * Evidence: `Set-Cookie: nyt-geo`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/puzzles/leaderboards/invite/](https://www.nytimes.com/puzzles/leaderboards/invite/)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
* URL: [https://www.nytimes.com/svc](https://www.nytimes.com/svc)
  
  
  * Method: `GET`
  
  
  * Parameter: `nyt-gdpr`
  
  
  * Evidence: `Set-Cookie: nyt-gdpr`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x`
  
  
  * Evidence: `<script defer src="https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x"></script>`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js`
  
  
  * Evidence: `<script src="https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js" crossorigin="anonymous">' + '<' + '/script>');
      }
    </script>`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x`
  
  
  * Evidence: `<script defer src="https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x"></script>`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js`
  
  
  * Evidence: `<script src="https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js" crossorigin="anonymous">' + '<' + '/script>');
      }
    </script>`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js`
  
  
  * Evidence: `<script src="https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js" crossorigin="anonymous">' + '<' + '/script>');
      }
    </script>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js`
  
  
  * Evidence: `<script src="https://js.sentry-cdn.com/7bc8bccf5c254286a99b11c68f6bf4ce.min.js" crossorigin="anonymous">' + '<' + '/script>');
      }
    </script>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x`
  
  
  * Evidence: `<script defer src="https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x"></script>`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x`
  
  
  * Evidence: `<script defer src="https://www.googletagmanager.com/gtm.js?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x"></script>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static01.nyt.com/newsgraphics/2020/03/16/coronavirus-maps/3d5bc806f17f79a8dc6825a7db6641a560a2525b/polyfills.js`
  
  
  * Evidence: `<script src="https://static01.nyt.com/newsgraphics/2020/03/16/coronavirus-maps/3d5bc806f17f79a8dc6825a7db6641a560a2525b/polyfills.js"><\/script>');
  }
</script>`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static01.nyt.com/newsgraphics/2020/03/16/coronavirus-maps/3d5bc806f17f79a8dc6825a7db6641a560a2525b/polyfills.js`
  
  
  * Evidence: `<script src="https://static01.nyt.com/newsgraphics/2020/03/16/coronavirus-maps/3d5bc806f17f79a8dc6825a7db6641a560a2525b/polyfills.js"><\/script>');
  }
</script>`
  
  
  
  
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
<p>Warnings:</p><p>1:1: The upgrade-insecure-requests directive is an experimental directive that will be likely added to the CSP specification.</p><p>1:316: The child-src directive is deprecated as of CSP level 3. Authors who wish to regulate nested browsing contexts and workers SHOULD use the frame-src and worker-src directives, respectively.</p><p>Info Items:</p><p>1:366: A draft of the next version of CSP deprecates report-uri in favour of a new report-to directive.</p><p></p>
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `upgrade-insecure-requests; default-src data: 'unsafe-inline' 'unsafe-eval' https:; script-src data: 'unsafe-inline' 'unsafe-eval' https: blob:; style-src data: 'unsafe-inline' https:; img-src data: https: blob:; font-src data: https:; connect-src https: wss: blob:; media-src data: https: blob:; object-src https:; child-src https: data: blob:; form-action https:; report-uri https://csp.nytimes.com/report;`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
  
  
  
* URL: [https://www.nytimes.com/section/todayspaper](https://www.nytimes.com/section/todayspaper)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap/](https://www.nytimes.com/sitemap/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/cookie-policy](https://www.nytimes.com/privacy/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/privacy-policy](https://www.nytimes.com/privacy/privacy-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.nytimes.com/subscription?campaignId=37WXW](https://www.nytimes.com/subscription?campaignId=37WXW)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/*.pdf$](https://www.nytimes.com/*.pdf$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/*?*searchResultPosition](https://www.nytimes.com/*?*searchResultPosition)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/video/embedded/](https://www.nytimes.com/video/embedded/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/puzzles/leaderboards/invite/](https://www.nytimes.com/puzzles/leaderboards/invite/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/*?*login](https://www.nytimes.com/*?*login)
  
  
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
  
  
  
* URL: [https://www.nytimes.com/sitemap/](https://www.nytimes.com/sitemap/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=600,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/privacy-policy](https://www.nytimes.com/privacy/privacy-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=300,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/section/todayspaper](https://www.nytimes.com/section/todayspaper)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=600,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=604800, stale-if-error=86400, stale-while-revalidate=30, public`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=30,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=30,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/international/?action=click&pgtype=Homepage&region=Editions](https://www.nytimes.com/international/?action=click&pgtype=Homepage&region=Editions)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=30,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/international/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/international/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=30,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=30,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=300,no-cache`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/cookie-policy](https://www.nytimes.com/privacy/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `s-maxage=300,no-cache`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Debug Error Messages
##### Low (Medium)
  
  
  
  
#### Description
<p>The response appeared to contain common error messages returned by platforms such as ASP.NET, and Web-servers such as IIS and Apache. You can configure the list of common debug messages.</p>
  
  
  
* URL: [https://www.nytimes.com/section/science](https://www.nytimes.com/section/science)
  
  
  * Method: `GET`
  
  
  * Evidence: `under construction`
  
  
  
  
Instances: 1
  
### Solution
<p>Disable debugging messages before pushing to production.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.nytimes.com/interactive/2020/us/covid-19-vaccine-doses.html](https://www.nytimes.com/interactive/2020/us/covid-19-vaccine-doses.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://static01.nyt.com/newsgraphics/2021/01/19/world-vaccinations-tracker/assets/promo-thumbnail.png`
  
  
  
  
Instances: 1
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://static01.nyt.com/newsgraphics/2021/01/19/world-vaccinations-tracker/assets/promo-thumbnail.png</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://www.nytimes.com/puzzles/leaderboards/invite/](https://www.nytimes.com/puzzles/leaderboards/invite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.2`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/wp-admin/](https://www.nytimes.com/wirecutter/wp-admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/data-requests](https://www.nytimes.com/wirecutter/data-requests)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*.csv$](https://www.nytimes.com/wirecutter/*.csv$)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/out/link/](https://www.nytimes.com/wirecutter/out/link/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*?l](https://www.nytimes.com/wirecutter/*?l)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*.zip$](https://www.nytimes.com/wirecutter/*.zip$)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/deals/beta](https://www.nytimes.com/wirecutter/deals/beta)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*?q](https://www.nytimes.com/wirecutter/*?q)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*&xid=](https://www.nytimes.com/wirecutter/*&xid=)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/*?s](https://www.nytimes.com/wirecutter/*?s)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/search](https://www.nytimes.com/wirecutter/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.6`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/ios-iphone-114x144-080e7ec6514fdc62bcbb7966d9b257d2.png](https://www.nytimes.com/vi-assets/static-assets/ios-iphone-114x144-080e7ec6514fdc62bcbb7966d9b257d2.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/ios-default-homescreen-57x57-43808a4cd5333b648057a01624d84960.png](https://www.nytimes.com/vi-assets/static-assets/ios-default-homescreen-57x57-43808a4cd5333b648057a01624d84960.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/vendor-fbd2815c37f0a2b4a58e.js](https://www.nytimes.com/vi-assets/static-assets/vendor-fbd2815c37f0a2b4a58e.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/favicon-d2483f10ef688e6f89e23806b9700298.ico](https://www.nytimes.com/vi-assets/static-assets/favicon-d2483f10ef688e6f89e23806b9700298.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/apple-touch-icon-28865b72953380a40aa43318108876cb.png](https://www.nytimes.com/vi-assets/static-assets/apple-touch-icon-28865b72953380a40aa43318108876cb.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/adslot-e133e3e2bc65b19d0845.js](https://www.nytimes.com/vi-assets/static-assets/adslot-e133e3e2bc65b19d0845.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/ios-ipad-144x144-28865b72953380a40aa43318108876cb.png](https://www.nytimes.com/vi-assets/static-assets/ios-ipad-144x144-28865b72953380a40aa43318108876cb.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/main-f81155c96c5785c923aa.js](https://www.nytimes.com/vi-assets/static-assets/main-f81155c96c5785c923aa.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/global-69acc7c8fb6a313ed7e8641e4a88bf30.css](https://www.nytimes.com/vi-assets/static-assets/global-69acc7c8fb6a313ed7e8641e4a88bf30.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/vi-assets/static-assets/home-f1293501f52473a64fa6.js](https://www.nytimes.com/vi-assets/static-assets/home-f1293501f52473a64fa6.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.nytimes.com/subscription?campaignId=37WXW](https://www.nytimes.com/subscription?campaignId=37WXW)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `6LevSGcUAAAAAF-7fVZF05VTRiXvBDAY4vBSPaTF`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `6LevSGcUAAAAAF-7fVZF05VTRiXvBDAY4vBSPaTF`
  
  
  
  
* URL: [https://www.nytimes.com/video/embedded/](https://www.nytimes.com/video/embedded/)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAAXAAAAA0CAYAAACTp2PxAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAEuRJREFUeNrsXdt12zgTZnyyz2EqWKaCMBWEqiByBaEqsFSBpQpkV0C5AikVSKmA2gqkVCDt8z74F/x/SEYwLgOQuhpzDo+dGLxgLh8Gg8EgSVqmv/76K99dw9013V3P+FkkkSJFejMkbB44UO+uze6qIg4ch/EpYfwzuea7a+wjhF3bLrm/4r4/SmHfECIXIknH6Ijvy2DvK2LDG+CAwIfc41klecY4SvNwQishpGfHJUfULuOZc3LfkKGkqwszqgp9nGO20Q3hu4N/EcQDHJEr6ktfgueR3jdkYIAvDlBc6UYNPQx4PwdeU9yfaQCOtls5lPSl3RXwa8oFENLvuYZ/0pCKN6KDOXi3IQBhDMHpBj7MIGtc6YXzIyWhyOdjADi87hAMkGBeqnzX2Mo0Im479E5Ol3Y/6t3VhsKvcQl6ZXj//fffO42nJKZVpanNGRqW8CBcSjjZ9aPH8LzV0NJyd213V4ZLUGf3rMW1OxAaXlAa7XgwVAc4+n+Y1s+JHm/Bu+UF8qMLflCbXOz60jngOwvwrw2SeuyDA+L/txGW+XSDn3ctgXcC0Cl0QtN5XFCY8sL4xonjlbapIvquA6wcvMuUQfEtg7ege9tMBM9QnRDx+1zGa+HRzs+cFynixNMWbZJL31t8Vh6AA1USKQjA8yO9b6t4GPMjvru1ab4Crt5ATxSWQ8LruloAJzOwJS4b3Zmm/RbjF8+vsf4ieD44Y17ImXD/RJ9QHOk9S40tiJ9dbrJDpH0A1zF4gatNmpGp2ik8jDZIfvNkdz3QQUk3G1EXbgFY3L5vzxlwWgSN2W6Q+iIuR39zDehxnYD7cw+nYKC+dejUIUl1TCQGtM2zHwp4p8rMNWaqNADwHoypg0vEqjoAq6aCfISiLvDMS6WX+PbuGqAfNoO7k/E9At49xuD4At6XGL8NmGoPCIg9eABMAh51MKC6APLs46uQ9+REr6f8oRggBtaPGFya4oB4xwOZgescmb4tMyvSawCXAlnuhDXRKNUCYHVLBCnarT2E1qNgdOGLco+KwY0cHvs9fhdKOwI/OwBy1RjWMJIvOlk0mJ6XyGjonxkvJxpgZeuG1CksGF/LbOXHid67IDJZqoPf7poRp+UT9NcXBzqQ99rR7todl/YISfsbXfxJ2djTN9xbIoWoNqQWZYb3alOSLpB/BSPNKnM8Y3iIdEG5cIdvqC+En3OObuj2FXDvvVB9mh/pvUODncuNPV0HDqwMOKCmF3Y1fazjZr4w4XXB+EwBlQ2YmhuE1jcYUcp45zUB+NQB4NWxAZzkRF/UBooI4KcBcDJTq2nYj+SG1zpHRIK35v/HLhxQcsQjeAeGUMQUSSwwfgFTc3hr95jq7C3+QGACkMTGnLFhavvW8jn/Seyxy/IEG3KE/OjAm0WVj+QISQkdFiHSFE6bzIpZAgfWykAjcUCXgvivCwfwPhGKmZHwSiTeYJvfaED3JXcWhi9j11sisDkEVh47zHMBPB0xAPWYpMro3qeGhfTADtH2wgwlvYBvzEzf6StzgHQB8M6S/di19JrnSUt7OASI767bCN7e2Hd/oxE0XRl+FJ43BLbC34oTdEAoSd1WjijCFau2BwUovg3Ei7bDGDDcuYE3qebfc+43IJ1r5Zo5yFBNQjbNXIuHIx2WkNmTrJNjefaU8gtlFULeI52uvbo5cit+8v/Fc197o/o0IN+3wt+KA+hw7imbKSNEUzDbyRBy3mK/JM6kDfSvBvYVyt/ErCi9UVBeTev5QBa+nk5kRP3kz5bisklFNghThoayNjxiCJwK3ZUbPm6JLyl4sYIxcUM0L6mMLqXGgNAnoF86wEPy4eKLb4G3FTzQwsUDC/9KDNqVwVHqwjhr6GWobkh9lvyvMXBs8I6lpz7T7xC6/Bk26MoeCbUfyWfu2llB+De3zDz6pN3U4ahMwcN50xkXcGZF5DIOtO0aMpX6V2FQqF49U7P4Uyuj+ZC7OMRdbHE9Dx+sa1OGGKThWUWogSsV1oaKJ2Vb0CwNo3XBfH9Xs9L/apFLkxXkXPHXLHzSq6/zEGxtZcVGT/6ebBGTLNybeDZm6MbcJHMHf5/hjbIXMRkZUBtP3q80hdkKBn913zZk6PHGJwvFUERurpHB1JVIYJFV0GIqZGdKZsh9wJ9ZQKx/Q6ZMKnj0GuRqp01GMTL1MwF1RQyicJRjlV5q2UZcGjMV+bzUEEp5cHgq4wYKImtGZIYQDe2nKya/520p3rTpuyvFi7S1neP5A48+5skJduiSMKHQh5mlaV8DBJnCv8Kgs4WDZ0ufsgl4n2twfPSZ8mv0KggH8G1fLd5xmeh3JO/VCALIZ8RTrgx6X2lmNyqVSrvaIKvfpS5IeCdjeszdkJm3BH+8lzvTmd0YQGwbsgOQxEJzTA1D40lTKN7MAYKCKd917RSDTC1gVnh69PdMgHFt7ul78JVm/RSYEpt4c08qu4k2Pcfju0rfcg8Zufiwxk6+Lad/8JJrj2/YKymrCWdx9LUkcd2MhAttO2x/p9rh/XJxeJrYM31c2/59NyJVjvct1QqODsC909y/DcCBnAxkujLJ0m6NOgl9EP37KgY1/G7jXUkchoTZzta3HIAq3jswDaykiBoHZ7oO2+6SsJWrpMKD+KYbPFRVgmWg0KjxZb5xQ6rIGPV7lm8RzEqxpX2rhhc0yr3ggB6DWP1BepTNc7ljbO5JiXBLprFndHAgaVq2wUS2Fc+cWNrSErm3Dj0ZucrpKnoToicJvLyaGKVPjLZvAkFS7mFrmb3UAJge3t1jDJimv3t5urBb8Q1fDDKbJH7lKrqaATkEB9RZhnTmCjJb+YfsRLbZmWg3gA38ZJRMKNCm49AD2m7p4Mmtzpl14MzCY+Zd6XQf7/yk9HeLf//e/S088G86zynAkMYaQ0hDwgVke/QWQjYZ0S8dMFq8koHhWVlymApw3C32thBHaeDR2vL8vcEBID5i8t42aD4pMjIBxILr+SWva14nnrqyV7snabEQFOnj1jJYPqHtS440Zj0PjoH9E9osYJBeZRNI6ES8/ztk9hHf+rLNXXVsGPSdaV8cHNBlP42l3sq+4qet9s2SyHhCbHjpkBvHg5XtrGBv4aENZ3oc54qhf1v0/R2uj8TB3UoAL9oQnGF0XEKZtg2N6LElg1xbnnXPTCvcavq4NLxv4QgDlQ1TGU2xdt3gMPF47parYE3kAa/srNMOCYivPe4ZuPRQtAHo9wLClXTQEzH5HMa+wBXigBUtsayj0fmZabB38SoEdIncbpnPa7UCpI9z5WkvQu6/6EztxjCKfAj1hsjUfgLP6NyS802gt2Z6gjNl2usqgTpgGGOoomw9POt1coWE7doyFa+RN+8Ag/WZ9LefvF4oqxo+M2+RV2IguSWe9ajtTTqMYljUgeLKd3kknNkGykiGWu5pWPrGMnUPZe4DptC9czR4CH+gAeUvTE9oJIXAmfYCOG3tiiZ505pYu9w9e5b8ZwyOI08l/0VqiT8l110uIEv0YbemJ9abBr2/G+jlINEcg/dWyOBcTYAzrsEnVxbn1Ti5XOBtH8AvhLkzgJ6suc32EMB8ARYzj/zmQXLYzT0DEs5ptQztgeWwIF7KA+Qw9PGGaP1wPO/ay5CawPb+ALtg8yRSE/2eEJzpeaxLpADpUgPekl4yoUwAnh6ict25VMMj39FxHCBgBHGATY/ZXgjt0WEo3wP7ItO/HuCJXlqoZBBNnU3rxL7o1/ZxZHnb5SZI6uXVk4IzJqdq65Cnjf/5jeWP3xjfKEaXDrMz5TmM6MhBFX27PfJpN87j1wL6InOPf/guBp3ZbEjo0L/XVEflgDRKzPHf0FCKbdDngK0AJ27Irp9ceVVMcjD1VwbOmLK+trjXmjp5YxGeLUNigVGlw1kogJd4f2K+ysJEPwNSrNoAqlbPt8Ri1hhCnl34VPMl7fANHB93DD26D6w+aKI7SxqwABaZsrhm6GyG2eL6ikUknaqfyDTipjIuFfDuSLvGTP/BBOA2AB4TAP7sC9zKc7LktPFJEaLonRLsMI1qQ3mL5P+bmGL95LcJ4kKHZy2HUkz2/HvXMAA48wVu5bvSKwdwb5xB5o7ckCXBW8XKf3X3vhcjhWWa1MV2UkGPgTUR+uT5pwTwwZnEh8Vo2vRklcVbXd2P9Eefkz+VErWhFE8d+ZGYc8GFVy8zUjohdoTFOPH87YWfh3sQnIGTnBnAO7GFUGaJPTYrmD5qAN4yw2J5YgDNGd/LrouCKnu0tOM3VCHMXOGCxOPQXgNlzLKb43hE1dV64cKWRi2GUlweYxdOXCh4l8z3XEMIxQtnYKNTgL+Xk3vDyJDwroVMhEbT4x5PzNixo2qhGGzuXApGivzLAjZl8qcWtjwAwVWcftSwL1miKRJEFQLf+E8MsQTrytkvqCKDatlGKIWxX0HiQOHxiR+gh9Tuni5JEQL0YMyojqoW4JtiBnRHNqVNObyWWSiuDAmZl2gVIEkRUmt4bH1GXsk0PK9ND7LS1LSWpWtTVz64UmUtccxaalITe+8gCnjhkxZG+lcVH0kxoQE3H9xV45oQN9Xx5xV4UQc5XajhM3ONbfQc7YfE8XDV4RgxcGAOcMkcODAEBlBbWfqunens31Z1UuPZJsx2pv7MCc+7HjhTGnBmS5MoYHsZnD/qDMrDKqyD8HsAynbXsJdYTq0gwCTc/yXCADSw/tUCbGrFwNTxrjm+587HWwXTMoZSfBZMJKePOENEpNZz6qmAImVxrckZHyWWFC2SubO29EkaVAdH3/UhB9/FzT544drQVKKd6fmLkGngCT2r7wywMsUk1ya9cRgdldcQ9jdkDpTym26hGy/v3/1bOGB9SyhFyOolddblhe/ajhL3xjIBLl3gwA/lbzYcGBj03DqQ7q4vsiIhHEGbHQrwlAkDcwfIynYVw8Ym+H3GxJkKODMw4QwGQdegKmxO/FTrU71ETt4T4c0gPE66n0/d5QldkYWH6EpQl+DVg6IXDIMUjPh71/4TDOPewZQU7+GupPeTwDobug0/MBab4c3hXa0Tex1pqWALhExuLfzhzBoeHbLJESaiwLaFcj6cMWYvFcMRBtWBk9C38LaGM0ENxzi7AdC4dLuGvJ7oc0iVwa7j/mmyv9g1wj2m935mDM6/wzICeBJe/rcPDrwa7ABsFfR8nJgXZFe4f4L7Zo7v+5r8KbvK+b5RYl4Qljz/BTAW2PIBODN2AHCfzLh0OHPH5F2Z7K+bTcCPtXY6zTzOh3Ppjlmq5BTLct/eeY2WtkObN+74tsrzxPU6oP+u46FS5UipwtLO9v6NaXpHjpcaonh8zeEL41i4DZ5btb1QGnqkGr6bpYuKfpUMWa7AQ+s5ouSkqNLBu0Lz7XMscPUdOpVp3t01yTNQBlWLOFAZ3tGV/LR8/8ZwBGHFeZfliDM1xJH7HIHYBs7Y9Nwi+4IjvNJxLiDnGjPf4wRlC4B3A/vRD1DoVsHb0DfX+kJleE/uuC/TADrnzMvCogerQx1e3ADAbU5B3xVSsfS1CtlSbtBv48nnipzKAIdg2uTsWA+787mGDfi1ceh27RooDM5P6SGvMlDOzns18qot52EOfYWXBY7CXivVpPM2L9Jk0Bnj+dQwN6GgYzMmMqPYcBRP8+wV94BlRSbTUO9XmWltLN6/6rVvGla+S1yLX+BHBU+0IF7pEP8vPf85+Xvl8HhTpq7U3h4P34moPWd9pY8nDVltTF5r6FpBgKf4zMjEcun3ynW/As4Vs13pgUc+OFb42r8y0yoN/183WviGUvQZU/iqATh2HavaK054xqGE04YHLav9Tw3vWfkynEwfC2b7YcgswqCs3JlC5TrctQWgWHl8Twq+jR2neM89B1M5Q+m33LdxAxmNPdsfInsmI7XXbWGmcVMdcYWqdN/FlEH3kDz0xRkaQjUMCE5H6V3AR6ogsz7kBh1yCrxKnWPu6FI2JS1QZCZSezKusVj0JfRAbbKoJrdrL2N9lYPJ7Kg4cMV8lLVTgs5QeHcBHdTVw52c4sAC4X0kf1a1v0RwaI2vNLf+Y4OT0Pc8nyvfsh3pevRf6G0XOju5po6VhilxeipGk4WHgy3ivTXl9VmswZS5i2n23BE+OVi8PlKkc6B3Z2zYwvBoLvdL4vo5FHECcH+DNy688KfojTfipbqeIbwQunHhgxIe8SXhid/GsgKRIoAf3qBlTZKMGJ/Y7TWJBvhmAPwQ9HCph15EinRxHnikNwXiz0d4jahB8TFyO9I10U1kQaQzoGOUGI1ldSNFDzxSpAN44C+VFQ/9np0HHvU9UgTwSJEOAOJlEnYUmFgXEQvIP8nvshga3Ywh8pQ/RU5HuiZ6H1kQ6RxI5L+i7KkKvCawFj+NpzyhBCctWfwUuRwpeuCRIh3eG081IL70yUJSslsE2McDoCNFihTpQgaBadOCX5EiRYoU6fjgXaKoUh65Eema6X8CDAB47qnHYdrJ4AAAAABJRU5ErkJggg==`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `6LevSGcUAAAAAF-7fVZF05VTRiXvBDAY4vBSPaTF`
  
  
  
  
* URL: [https://www.nytimes.com/*.pdf$](https://www.nytimes.com/*.pdf$)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/hc/en-us/articles/115014792127-Copyright-notice`
  
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/hc/en-us/articles/115014792127-Copyright-notice`
  
  
  
  
* URL: [https://www.nytimes.com/puzzles/leaderboards/invite/](https://www.nytimes.com/puzzles/leaderboards/invite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/hc/en-us/articles/115014755667-New-York-Times-Crossword`
  
  
  
  
* URL: [https://www.nytimes.com/adx/bin/](https://www.nytimes.com/adx/bin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABg5-UwmdmxmEnd_t_KiJjDwaCDDB5KkTrgf0rcUAQyBQGWYIksa82ixA4sqaAVR97AItL_eq74dHGFCUuR6M8VomDU`
  
  
  
  
* URL: [https://www.nytimes.com/ads/](https://www.nytimes.com/ads/)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABg5-UyDpvtQnOC2ZAWeOJ820AJi2u_1UhS-RJV9AS69VZ8DO3M6W07mwfAr3wZlmy7nq2cGqqESW08IEY8wXkX8ssE`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `6LevSGcUAAAAAF-7fVZF05VTRiXvBDAY4vBSPaTF`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `6LevSGcUAAAAAF-7fVZF05VTRiXvBDAY4vBSPaTF`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>路Hg\x0014\x0000\x0000\x0000\x0000_�}VEӕSF%�\x00040\x0018��R=��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://www.nytimes.com/ads/public/](https://www.nytimes.com/ads/public/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "<!-- css generated from src/style.scss, text-balancer, and svelte component CSS -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `User`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `User`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 8
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected 2 times, the first in the element starting with: "<script data-rh="true" id="als-svc">if (window.NYTD && window.NYTD.Abra && window.NYTD.Abra('als_toggle') !== '1_block') {</p><p>    (", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Loosely Scoped Cookie
##### Informational (Low)
  
  
  
  
#### Description
<p>Cookies can be scoped by domain or path. This check is only concerned with domain scope.The domain scope applied to a cookie determines which domains can access it. For example, a cookie can be scoped strictly to a subdomain e.g. www.nottrusted.com, or loosely scoped to a parent domain e.g. nottrusted.com. In the latter case, any subdomain of nottrusted.com can access the cookie. Loosely scoped cookies are common in mega-applications like google.com and live.com. Cookies set from a subdomain like app.foo.bar are transmitted only to that domain by the browser. However, cookies scoped to a parent-level domain may be transmitted to the parent, or any subdomain of the parent.</p>
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/video/embedded/](https://www.nytimes.com/video/embedded/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/puzzles/leaderboards/invite/](https://www.nytimes.com/puzzles/leaderboards/invite/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/ads/](https://www.nytimes.com/ads/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/adx/bin/](https://www.nytimes.com/adx/bin/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/svc](https://www.nytimes.com/svc)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Always scope cookies to a FQDN (Fully Qualified Domain Name).</p>
  
### Other information
<p>The origin domain used for comparison was: </p><p>www.nytimes.com</p><p>nyt-a=zYZZthMLSSoCSvluJjN1RM</p><p>nyt-gdpr=0</p><p>nyt-purr=cfhhcfhhhck</p><p>nyt-geo=US</p><p></p>
  
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
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/section/todayspaper](https://www.nytimes.com/section/todayspaper)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="thefrontpage"></a>`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap/](https://www.nytimes.com/sitemap/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/wirecutter/wp-admin/](https://www.nytimes.com/wirecutter/wp-admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a tabindex="0" class="bdb792e0 _2cc22194" data-gtm-trigger="nav_link">More categories...</a>`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/cookie-policy](https://www.nytimes.com/privacy/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/privacy/privacy-policy](https://www.nytimes.com/privacy/privacy-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
<iframe src="https://www.googletagmanager.com/ns.html?id=GTM-P528B3&gtm_auth=tfAzqo1rYDLgYhmTnSjPqw&gtm_preview=env-130&gtm_cookies_win=x" height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>`
  
  
  
  
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
  
  
  
* URL: [https://www.nytimes.com/puzzles/leaderboards/invite/](https://www.nytimes.com/puzzles/leaderboards/invite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `401`
  
  
  
  
* URL: [https://www.nytimes.com/ads/](https://www.nytimes.com/ads/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.nytimes.com/adx/bin/](https://www.nytimes.com/adx/bin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/*.pdf$](https://www.nytimes.com/*.pdf$)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/search](https://www.nytimes.com/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html](https://www.nytimes.com/1996/06/17/nyregion/guest-at-diplomat-s-party-accused-of-rape.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/*?*login](https://www.nytimes.com/*?*login)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/sitemap.xml](https://www.nytimes.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/video/embedded/](https://www.nytimes.com/video/embedded/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.nytimes.com/svc](https://www.nytimes.com/svc)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.nytimes.com](https://www.nytimes.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.nytimes.com/video/embedded/](https://www.nytimes.com/video/embedded/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.nytimes.com/*?*campaignId](https://www.nytimes.com/*?*campaignId)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.nytimes.com/*?*query](https://www.nytimes.com/*?*query)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.nytimes.com/*?*mcubz](https://www.nytimes.com/*?*mcubz)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.nytimes.com/*?*login](https://www.nytimes.com/*?*login)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.nytimes.com/robots.txt](https://www.nytimes.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=604800`
  
  
  
  
* URL: [https://www.nytimes.com/*?*searchResultPosition](https://www.nytimes.com/*?*searchResultPosition)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.nytimes.com/svc](https://www.nytimes.com/svc)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
* URL: [https://www.nytimes.com/*.pdf$](https://www.nytimes.com/*.pdf$)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=300`
  
  
  
  
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
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `82620417`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `872890833`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `257698037`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `858993458`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1226642659`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `42949672`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `87378333`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `84136417`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `08846417`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `86768746`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `644245093`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `39318518`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1417339207`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `99242333`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `21966278`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1732584193`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `44292333`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210404`
  
  
  
  
* URL: [https://www.nytimes.com/](https://www.nytimes.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
Instances: 63
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>82620417, which evaluates to: 1972-08-14 06:06:57</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `region`
  
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `pgtype`
  
  
  
  
* URL: [https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer](https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer)
  
  
  * Method: `GET`
  
  
  * Parameter: `region`
  
  
  
  
Instances: 3
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.nytimes.com/ca/?action=click&pgtype=Homepage&region=Footer</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [nav] tag [data-testid] attribute </p><p></p><p>The user input found was:</p><p>region=Footer</p><p></p><p>The user-controlled value was:</p><p>footer</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

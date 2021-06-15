
# ZAP Scanning Report

Generated on Tue, 15 Jun 2021 01:07:32


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 10 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 500 | 
| X-Frame-Options Header Not Set | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 9 | 
| Application Error Disclosure | Low | 2 | 
| Cookie Without SameSite Attribute | Low | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Dangerous JS Functions | Low | 3 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Secure Pages Include Mixed Content | Low | 3 | 
| Strict-Transport-Security Header Not Set | Low | 1 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 10 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 5 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 2 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit](https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5b576b1c88ee381a3d7f1d5b](https://transport.data.gouv.fr/api/datasets/5b576b1c88ee381a3d7f1d5b)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b962cdd5ced668021e6](https://transport.data.gouv.fr/api/datasets/5f727b962cdd5ced668021e6)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b966c0e98506c8021e6](https://transport.data.gouv.fr/api/datasets/5f727b966c0e98506c8021e6)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b959d8643680e8021e7](https://transport.data.gouv.fr/api/datasets/5f727b959d8643680e8021e7)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b954d128d4c0a5b654c](https://transport.data.gouv.fr/api/datasets/5f727b954d128d4c0a5b654c)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b957ba624d0618021e6](https://transport.data.gouv.fr/api/datasets/5f727b957ba624d0618021e6)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b9628bcf5467b8021e7](https://transport.data.gouv.fr/api/datasets/5f727b9628bcf5467b8021e7)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5f727b95da00e0a55d5b654c](https://transport.data.gouv.fr/api/datasets/5f727b95da00e0a55d5b654c)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/60b758d2ba74fc876a32b784](https://transport.data.gouv.fr/api/datasets/60b758d2ba74fc876a32b784)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/60c1562cdcedc99af52fcb48](https://transport.data.gouv.fr/api/datasets/60c1562cdcedc99af52fcb48)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5d6eaffc8b4c417cdc452ac3](https://transport.data.gouv.fr/api/datasets/5d6eaffc8b4c417cdc452ac3)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
* URL: [https://transport.data.gouv.fr/api/datasets/5448d3e0c751df01f85d0572](https://transport.data.gouv.fr/api/datasets/5448d3e0c751df01f85d0572)
  
  
  * Method: `GET`
  
  
  * Evidence: `access-control-allow-origin: *`
  
  
  
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">Service status</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit](https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://stats.uptimerobot.com/q7nqyiO9yQ" target="_blank">État des services</a>`
  
  
  
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/026954d7-8479-494a-90b8-4e1d3af8e4ed" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/0dee4ad4-cbb0-40f0-a34d-9b9a5d851890" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/f974f6bd-69e9-426f-84b9-689e0561ddf0" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/e10262e6-bc2a-412c-aa09-9ed68fe94868" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/d3cb0797-d112-4296-a38f-7ea97c2c0288" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/e671de39-22d6-44bf-8168-e35b1d3c3b3b" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/1816846d-1b08-47ef-909f-2bc67c529148" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/87a0b98b-8a5a-4ba7-ad93-5a1fb9924844" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/4736f6a5-d202-4a55-b06c-f46c08fa0301" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/13b033e0-34ca-4d32-8591-448d7462b2f8" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/70a24b40-69c6-452f-a23f-5b791485a7d7" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/a09802f0-62fa-45e2-800a-85a8caccb8cd" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/29fad7c4-8cf5-4055-8432-863876040533" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/12197760-975c-4885-998f-4882760a8a9d" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/2a73215c-b857-4c2f-92a5-3cbb23b2516d" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/a9923e12-ef29-4f41-9115-08e56380840a" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/515ef4af-ec53-4f3a-a453-c9da680968a3" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/587f6a62-8a15-4c76-9aaa-5155bdddc9b1" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/2dcb3b19-b04e-480c-be88-41ef41a20540" />`
  
  
  
  
* URL: [https://transport.data.gouv.fr/atom.xml](https://transport.data.gouv.fr/atom.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://www.data.gouv.fr/fr/datasets/r/6eadacf8-84c2-4ef1-b31a-50e523c96ad6" />`
  
  
  
  
Instances: 500
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/swaggerui](https://transport.data.gouv.fr/swaggerui)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/validation" enctype="multipart/form-data" method="post">`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/send_mail" method="post">`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/send_mail" method="post">`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/send_mail" method="post">`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/datasets" method="get">`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="//gouv.us13.list-manage.com/subscribe/post?u=5ee8bfe0f1b073b49de06a063&amp;amp;id=13db2e9a94" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/datasets" method="get">`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/send_mail" method="post">`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="//gouv.us13.list-manage.com/subscribe/post?u=5ee8bfe0f1b073b49de06a063&amp;amp;id=13db2e9a94" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>`
  
  
  
  
Instances: 9
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "_csrf_token" "upload_file" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Application Error Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/send_mail](https://transport.data.gouv.fr/send_mail)
  
  
  * Method: `POST`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `POST`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 2
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/](https://transport.data.gouv.fr/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
* URL: [https://transport.data.gouv.fr/backoffice/](https://transport.data.gouv.fr/backoffice/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_transport_key`
  
  
  * Evidence: `set-cookie: _transport_key`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
    </script>`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
    </script>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
    </script>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
    </script>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>');
    }
    </script>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>');
      document.write('`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/js/resourceviz.js](https://transport.data.gouv.fr/js/resourceviz.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://transport.data.gouv.fr/js/map.js](https://transport.data.gouv.fr/js/map.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://transport.data.gouv.fr/js/datasetmap.js](https://transport.data.gouv.fr/js/datasetmap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit](https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/robots.txt](https://transport.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit](https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/datasets/route-500/](https://transport.data.gouv.fr/datasets/route-500/)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://professionnels.ign.fr/sites/default/files/styles/medium/public/image%20carousel/route500.png`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets/route-500](https://transport.data.gouv.fr/datasets/route-500)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://professionnels.ign.fr/sites/default/files/styles/medium/public/image%20carousel/route500.png`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets/cartographie-openstreetmap-des-gares-sncf-transilien-en-ile-de-france-1/](https://transport.data.gouv.fr/datasets/cartographie-openstreetmap-des-gares-sncf-transilien-en-ile-de-france-1/)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://github.pavie.info/openlevelup/img/logo.jpg`
  
  
  
  
Instances: 3
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://professionnels.ign.fr/sites/default/files/styles/medium/public/image%20carousel/route500.png</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/send_mail](https://transport.data.gouv.fr/send_mail)
  
  
  * Method: `POST`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/bus.svg](https://transport.data.gouv.fr/images/icons/bus.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/map.png](https://transport.data.gouv.fr/images/icons/map.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/logo-footer.svg](https://transport.data.gouv.fr/images/logo-footer.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/css/app.css](https://transport.data.gouv.fr/css/app.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/logo-header.svg](https://transport.data.gouv.fr/images/logo-header.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/api.png](https://transport.data.gouv.fr/images/icons/api.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/bus-stop.svg](https://transport.data.gouv.fr/images/icons/bus-stop.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/logo-black.svg](https://transport.data.gouv.fr/images/logo-black.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/robots.txt](https://transport.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/recently-added-datasets.png](https://transport.data.gouv.fr/images/icons/recently-added-datasets.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/js/autocomplete.js](https://transport.data.gouv.fr/js/autocomplete.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/bicycle.svg](https://transport.data.gouv.fr/images/icons/bicycle.svg)
  
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAADbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZybQAAAA1yZWRpcmVjdF9wYXRobQAAAAEv`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
* URL: [https://transport.data.gouv.fr/backoffice/](https://transport.data.gouv.fr/backoffice/)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAADbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZybQAAAA1waG9lbml4X2ZsYXNodAAAAAFtAAAABGluZm9tAAAALVZvdXMgZGV2ZXogw6p0cmUgcHLDqWFsYWJsZW1lbnQgY29ubmVjdMOpwrdlLg`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/](https://transport.data.gouv.fr/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAADbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZybQAAAA1waG9lbml4X2ZsYXNodAAAAAFtAAAABGluZm9tAAAALVZvdXMgZGV2ZXogw6p0cmUgcHLDqWFsYWJsZW1lbnQgY29ubmVjdMOpwrdlLg`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `MhgeYBE2CGYQDDhRO1gbGnoqASk2OABHp-tUgwX1XTYgv5MxWNfztZTu`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAADbQAAAAtfY3NyZl90b2tlbm0AAAAYcUVCY1VRRTRWOUFsV2w3LW4xOXJOcEQwbQAAAAZsb2NhbGVtAAAAAmZybQAAAA1yZWRpcmVjdF9wYXRobQAAAAwvc2l0ZW1hcC54bWw`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `g3QAAAACbQAAAAtfY3NyZl90b2tlbm0AAAAYeDZIczNLZ09QZmlNVzVsUXJDVVlKRFhGbQAAAAZsb2NhbGVtAAAAAmZy`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�t\x0000\x0000\x0000\x0002m\x0000\x0000\x0000\x000b_csrf_tokenm\x0000\x0000\x0000\x0018qEBcUQE4V9AlWl7-n19rNpD0m\x0000\x0000\x0000\x0006localem\x0000\x0000\x0000\x0002fr</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/js/autocomplete.js](https://transport.data.gouv.fr/js/autocomplete.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://transport.data.gouv.fr/js/map.js](https://transport.data.gouv.fr/js/map.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://transport.data.gouv.fr/js/resourceviz.js](https://transport.data.gouv.fr/js/resourceviz.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://transport.data.gouv.fr/js/datasetmap.js](https://transport.data.gouv.fr/js/datasetmap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(()=>{var t={4138:function(t,e,r){var n=r(7633);t.exports=function(){"use strict";function t(t,e){for(var r=0;r<e.length;r++){va", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Close the menu">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit](https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml](https://transport.data.gouv.fr/login/explanation?redirect_path=%2Fsitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="close-menu" href="#" aria-label="Fermer le formulaire">
          <i class="fas icon--times-circle"></i>&nbsp
        </a>`
  
  
  
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/stats](https://transport.data.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/explanation?redirect_path=%2F](https://transport.data.gouv.fr/login/explanation?redirect_path=%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/validation](https://transport.data.gouv.fr/validation)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/infos_producteurs](https://transport.data.gouv.fr/infos_producteurs)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr](https://transport.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/login/](https://transport.data.gouv.fr/login/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/backoffice/](https://transport.data.gouv.fr/backoffice/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/sitemap.xml](https://transport.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?order_by=most_recent](https://transport.data.gouv.fr/datasets?order_by=most_recent)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/robots.txt](https://transport.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/charge-station.svg](https://transport.data.gouv.fr/images/icons/charge-station.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `44598436`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/charge-station.svg](https://transport.data.gouv.fr/images/icons/charge-station.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `16499029`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/charge-station.svg](https://transport.data.gouv.fr/images/icons/charge-station.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `16762196`
  
  
  
  
* URL: [https://transport.data.gouv.fr/css/app.css](https://transport.data.gouv.fr/css/app.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `70710678`
  
  
  
  
* URL: [https://transport.data.gouv.fr/images/icons/charge-station.svg](https://transport.data.gouv.fr/images/icons/charge-station.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `89843249`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>44598436, which evaluates to: 1971-06-01 04:27:16</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?type=public-transit](https://transport.data.gouv.fr/datasets?type=public-transit)
  
  
  * Method: `GET`
  
  
  * Parameter: `type`
  
  
  
  
* URL: [https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit](https://transport.data.gouv.fr/datasets?filter=has_realtime&type=public-transit)
  
  
  * Method: `GET`
  
  
  * Parameter: `type`
  
  
  
  
Instances: 2
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://transport.data.gouv.fr/datasets?type=public-transit</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [img] tag [alt] attribute </p><p></p><p>The user input found was:</p><p>type=public-transit</p><p></p><p>The user-controlled value was:</p><p>public-transit</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

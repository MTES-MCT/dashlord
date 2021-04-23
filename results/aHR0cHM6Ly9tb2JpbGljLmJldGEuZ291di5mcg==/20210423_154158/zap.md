
# ZAP Scanning Report

Generated on Fri, 23 Apr 2021 15:35:26


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 6 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 12 | 
| Cross-Domain Misconfiguration | Medium | 2 | 
| CSP: Wildcard Directive | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 12 | 
| Strict-Transport-Security Header Not Set | Low | 3 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 1 | 
| Storable but Non-Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 5 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/auth](https://mobilic.beta.gouv.fr/developers/docs/auth)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/oauth](https://mobilic.beta.gouv.fr/developers/docs/oauth)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/push-activity](https://mobilic.beta.gouv.fr/developers/docs/push-activity)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/graphql](https://mobilic.beta.gouv.fr/developers/docs/graphql)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/errors](https://mobilic.beta.gouv.fr/developers/docs/errors)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/signup](https://mobilic.beta.gouv.fr/developers/docs/signup)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/changelog](https://mobilic.beta.gouv.fr/developers/docs/changelog)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/how-to](https://mobilic.beta.gouv.fr/developers/docs/how-to)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/principles](https://mobilic.beta.gouv.fr/developers/docs/principles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/playground](https://mobilic.beta.gouv.fr/developers/docs/playground)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/oauth/token](https://mobilic.beta.gouv.fr/api/oauth/token)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, style-src-elem, style-src-attr, img-src, connect-src, frame-src, frame-ancestors, font-src, media-src, object-src, manifest-src, prefetch-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [http://mobilic.beta.gouv.fr/developers/docs/intro](http://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, style-src-elem, style-src-attr, img-src, connect-src, frame-src, frame-ancestors, font-src, media-src, object-src, manifest-src, prefetch-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/](https://mobilic.beta.gouv.fr/developers/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro.html](https://mobilic.beta.gouv.fr/developers/docs/intro.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/logout?next=/signup/admin](https://mobilic.beta.gouv.fr/logout?next=/signup/admin)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/playground](https://mobilic.beta.gouv.fr/developers/playground)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://buttons.github.io`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/how-to.html](https://mobilic.beta.gouv.fr/developers/docs/how-to.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/oauth](https://mobilic.beta.gouv.fr/developers/docs/oauth)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/signup](https://mobilic.beta.gouv.fr/developers/docs/signup)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/how-to](https://mobilic.beta.gouv.fr/developers/docs/how-to)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/graphql](https://mobilic.beta.gouv.fr/developers/docs/graphql)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/principles](https://mobilic.beta.gouv.fr/developers/docs/principles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/push-activity](https://mobilic.beta.gouv.fr/developers/docs/push-activity)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/playground](https://mobilic.beta.gouv.fr/developers/playground)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600,700|Source+Code+Pro:400,700" rel="stylesheet"/>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/auth](https://mobilic.beta.gouv.fr/developers/docs/auth)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/errors](https://mobilic.beta.gouv.fr/developers/docs/errors)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/changelog](https://mobilic.beta.gouv.fr/developers/docs/changelog)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/playground](https://mobilic.beta.gouv.fr/developers/docs/playground)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/changelog](https://mobilic.beta.gouv.fr/developers/docs/changelog)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/how-to](https://mobilic.beta.gouv.fr/developers/docs/how-to)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/principles](https://mobilic.beta.gouv.fr/developers/docs/principles)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/signup](https://mobilic.beta.gouv.fr/developers/docs/signup)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/playground](https://mobilic.beta.gouv.fr/developers/playground)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/read-activities](https://mobilic.beta.gouv.fr/developers/docs/read-activities)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/playground](https://mobilic.beta.gouv.fr/developers/docs/playground)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/signup](https://mobilic.beta.gouv.fr/developers/docs/signup)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/errors](https://mobilic.beta.gouv.fr/developers/docs/errors)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/principles](https://mobilic.beta.gouv.fr/developers/docs/principles)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/push-activity](https://mobilic.beta.gouv.fr/developers/docs/push-activity)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/how-to](https://mobilic.beta.gouv.fr/developers/docs/how-to)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/changelog](https://mobilic.beta.gouv.fr/developers/docs/changelog)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/oauth](https://mobilic.beta.gouv.fr/developers/docs/oauth)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/graphql](https://mobilic.beta.gouv.fr/developers/docs/graphql)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/auth](https://mobilic.beta.gouv.fr/developers/docs/auth)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://buttons.github.io/buttons.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://buttons.github.io/buttons.js"></script>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.8d0cd9cc.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.8d0cd9cc.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/runtime-main.1de3a4c9.js](https://mobilic.beta.gouv.fr/static/js/runtime-main.1de3a4c9.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache; max-age=0`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache; max-age=0`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/manifest.json](https://mobilic.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/playground](https://mobilic.beta.gouv.fr/developers/playground)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache; max-age=0`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/robots.txt](https://mobilic.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/css/main.cd49adb3.chunk.css](https://mobilic.beta.gouv.fr/static/css/main.cd49adb3.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/principles](https://mobilic.beta.gouv.fr/developers/docs/principles)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache; max-age=0`
  
  
  
  
Instances: 12
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/oauth/token](https://mobilic.beta.gouv.fr/api/oauth/token)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/graphql](https://mobilic.beta.gouv.fr/developers/docs/graphql)
  
  
  * Method: `POST`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/robots.txt](https://mobilic.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/logo192.png](https://mobilic.beta.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/css/main.cd49adb3.chunk.css](https://mobilic.beta.gouv.fr/static/css/main.cd49adb3.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/runtime-main.1de3a4c9.js](https://mobilic.beta.gouv.fr/static/js/runtime-main.1de3a4c9.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/favicon.ico](https://mobilic.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/manifest.json](https://mobilic.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.8d0cd9cc.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.8d0cd9cc.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nnrrrmrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrmmmmmmmnNmmmmmmrrmmNmmmmrr1111111111`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/jorf/id/JORFTEXT000043023481`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��u���\x001f{��m>�\x001d|������O��hu�^��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.8d0cd9cc.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.8d0cd9cc.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.5fb7b454.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "(this.webpackJsonpmobilic=this.webpackJsonpmobilic||[]).push([[5],[,,,,,function(e,t,n){"use strict";function r(e){var t,n,o="";", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.45aec941.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.1de3a4c9.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/playground](https://mobilic.beta.gouv.fr/developers/playground)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-playground.e9c2a3cd.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/intro](https://mobilic.beta.gouv.fr/developers/docs/intro)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/developers/docs/intro" target="_self">Documentation</a>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.1de3a4c9.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.1de3a4c9.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.1de3a4c9.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/changelog](https://mobilic.beta.gouv.fr/developers/docs/changelog)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/developers/docs/intro" target="_self">Documentation</a>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.1de3a4c9.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/principles](https://mobilic.beta.gouv.fr/developers/docs/principles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/developers/docs/intro" target="_self">Documentation</a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/robots.txt](https://mobilic.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/manifest.json](https://mobilic.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/favicon.ico](https://mobilic.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/](https://mobilic.beta.gouv.fr/developers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/logo192.png](https://mobilic.beta.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 11
  
### Solution
<p></p>
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/manifest.json](https://mobilic.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `09697405`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.09c980d2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0123456789, which evaluates to: 1973-11-29 21:33:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

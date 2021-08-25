
# ZAP Scanning Report

Generated on Wed, 25 Aug 2021 01:11:33


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 5 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Cross-Domain Misconfiguration | Medium | 2 | 
| CSP: style-src unsafe-inline | Medium | 5 | 
| CSP: Wildcard Directive | Medium | 5 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 12 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 3 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 1 | 
| Storable but Non-Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/oauth/token](https://mobilic.beta.gouv.fr/api/oauth/token)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/docs/graphql](https://mobilic.beta.gouv.fr/developers/docs/graphql)
  
  
  * Method: `POST`
  
  
  
  
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

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/](https://mobilic.beta.gouv.fr/developers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
Instances: 5
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/](https://mobilic.beta.gouv.fr/developers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `object-src 'self'; connect-src 'self' https://client.crisp.chat https://api-adresse.data.gouv.fr https://*.ingest.sentry.io wss://client.relay.crisp.chat https://stats.data.gouv.fr; base-uri 'self'; default-src 'self'; script-src 'self' https://client.crisp.chat https://stats.data.gouv.fr; img-src 'self' data: https://client.crisp.chat https://stats.data.gouv.fr; style-src 'self' 'unsafe-inline' https://client.crisp.chat; font-src 'self' https://client.crisp.chat; frame-src https://metabase.mobilic.beta.gouv.fr`
  
  
  
  
Instances: 5
  
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

  
#### CWE Id : 345
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.e925a679.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.e925a679.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone6_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone6_splash.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
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
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/manifest.json](https://mobilic.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphoneplus_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphoneplus_splash.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphonex_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphonex_splash.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache; max-age=0`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/robots.txt](https://mobilic.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/runtime-main.94d74b14.js](https://mobilic.beta.gouv.fr/static/js/runtime-main.94d74b14.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.c7175140.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.c7175140.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/api/fc/](https://mobilic.beta.gouv.fr/api/fc/)
  
  
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

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.c7175140.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.c7175140.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.e925a679.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.e925a679.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nnrrrmrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrmmmmmmmnNmmmmmmrrmmNmmmmrr1111111111`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x0000�\x0000\x0000\x0000�\x0008\x0006\x0000\x0000\x0000��A>\x0000\x0000\x0000\x0001sRGB\x0000��\x001c�\x0000\x0000\x0014�IDATx��{x�ՙ�?gfr���dB\x0012��</p><p>Fw����\x0017l�rق�ti���Z��h-���\x0005�V</p><p>n�\x0011��v�cն \x0015�\x0002����[.\x0015]�R\x001b\x0008�\x0016\x0002�U�$��'�d��?&3I !��2���<�<a�9�}g�w�y���������������������������������"ۨ\;�MD�\x0013�r:	j\x0011N\x0007j\x0011�\x0002^\x0014�\x0002�Jp��%\x000b�.\x0010V�\x0008B\x0018\x0008�8\x0000�E�,6�V8iVJ\x0005s���ʈ\x0016���\x0005#|\x0001�b\x0011.\x0006�4��;</p><p>�\x0013\x001b�y]lSJ�L��sF�`\x0002\x00019\x001d���Ţ���,��E��ج\x0014ϩ\x0004/x�jo6�͈\x0010L  �b�r�\x0006�\x000b�-�>�҃�Y\x0014�m�z�W\x001dεCz)X�\x0004\x0002R)��\x0008
(�\x0002�\�4\x000ci�T���R*�k��Pp�\x0011\x0011\x0015\x0008�U\x0012܌�\��\x0005��6a�׫�+׾\x001c/\x0005#\x0018\x0011)</p><p>��\x000b,\x0004�1��\x0018��N���=.V+���'\x0013</p><p>B0��|.\x000e�Q��\�b\x0006\x0002���]�Gmϵ/Ñׂ	\x0006eT\x0002�\x0006�&�}5\x0000\x0001\x001e��Y���M�6B0(\x0017ą?(�)��%���v��<\x001e�R�}\x0019�|��L#"���ܞ�m'�X\x0000��\x0004l\x000b��g"bϵ?G�W=L4*'w��\x0007\x0005�r�K> ����לN�^�}I�7=L  _�u��\x0012K\x001f</p><p>&ź�\x0019\x000c�Wr�K��\x0010�?(7�bez�Ϣ\x000f�/\x0001��!�i�]�<\x0010�?(w\x0001Ks�G�#��\x001e���ڍ��0��<�b~.}(4Dx��U�ϕ��	�\x0012�vr)��\x000cI��,�Ģ\x001d���= Kra;�i\x000fȍ��F��Ҫ}�%\x0012\x0011]���׋R,\x000e��Y��Mc���\x0011�)t</p><p>u�Q�|*@4�l��f�i��Ψ�w����\x000e��+�s�.�{��p�2�*֬\x000b�̺\x0010\x0000�Uvn�����\x0016i�\x0014�����\x001e�ڐ-�Y�aB!�,�</p><p>�6[Z�<�����ʸ��*�Ɨ�̺\x0010\x0007��Ψ�=�>L(�`��Jf���kw\x0017Ϭ�,%��7:yf]�ɓ\\]\x0015�E��w�岷�%`M{H�f�`6�ttȩ�\x0004�1 �i��(����_^�\x0019��\��J\x0000^�KgF�[������	u�L��ń�e4��Y</p><p>�kot��ٙ�e/g�\x00163�\x001b��F�\x0003�L�&Q�\x0012�1\x001c���0f�`DDu�X��¨:O���!��ק��J;�f��m=���-̓�\x001e��'�J\x00111=�0]0� �Q�g��\x0013\x001e�\x0017�A\x0016�m�T��C2M)\x0016�iâ\x000f�X\x0014\x0008��?N�\x0004#"�\x0008\x000f�i��(l����\x0014�f����Ane���\x0016\x0018g\x0006B�Ȭ�Mٚ\x0011��ɱ\x001en�R�������\x000c��-�q��-/F��N�\x0016�\x0000,��m��\x001c�{7'�9:�~��1�q��l\x0019_�ȥٷ�E�[�QYiF\x001e�)=LW\x000f\x000f\x0000%Z�n}1JgG\x0002��A\x001f�!�Ŧ\x0006����Ȥ�P��\x001f�L[[������UhF)ܱn��Q��=L ,\x0017K\x0002]	?��UP_7�0���C�x��d�4's�\x000c?�;c��A__vGհe\x0017��Ft���?�{L�l���iFq�?$�+�j���\x001a��H�;���B#	�6�JC\x0005�\x001e�KQ|��:-t�8'\x0010�����P�(�\x0005�\x0016�H\x0018�&�	�=$S��F�w,\x000e���U�ё\x0018�o�3�\x0019u�k��\x0015��m�C&(���6�`\\x000f#d%���e���8;ވ\x0002������q��/9��W߈\x0012�\x0010\x000e\x001d���NNϰl�"���������\x0017��ܣk�dMi\x0008����!WI��T%�粘ΌiN6m��j��U��\x0000�6��\x0005\x0013K3*?w��G�\x0008��\x001f\x0000I\x0001]5'��</p><p>�g��vC�{�kM�������s���\x0011</p><p>I�ۭZ�Ve�`�Je'\x0019�ܥx�W546�hlꢾ�d�K���=�E}]1�M1�]�	u%\x00197x�K�r�\x0018\x001a����%N}]q�=[�Q=	�\x0000��[�1�0�o\x001aR�qP_W|\B�O�"�
]�R\x0019�fyE��t\x000bFw\x000c�\x001e�O+��[���(�o\x000f˧�֣?���.\x0016�P	���\x0008�\x0018v�fa.\x0002�'�t	�/�S�)�NXd\x0007\x0005�</p><p>\x0004�RO\x001d�\x0004#!&��"��\x0012J�􇾫$�\x0014��3���\x001d�Ö\x001e>j��u{\x0007���,����*\x00075�vƟY�'�4-)��(�\x0000�\x0016�'\x0018+~I��\x0014c�� ;�����T۩��s��\x001dD"	\x000e\x001d���7:X�6�ө\x0018V	�]ʔI��9���4\x000bFDl�\x0010uz��\x0004�\x000b���΂�W0��q�9����46�x�O\x0011\x001e\�g��\x0010
��Y\x0011��:\x0011�)�\x0012ÿ�h4\x000b&\x0014�\x001f�<�\x00137�pDX���\x0000�̘�Y��&\x000eg�t��\x0014��\x0008��r?[^�r�
�pe�\x0018�\x0011{o۽���f���̼: /�4��f��Ä!�Ҽ��HThl�˶��+��T\x0003f����ŝU46�X|�!\x0016���M7V2�\x0013�-9ēwuɮ`�y���k^��ɲ��\x0019]m��_���_���-qV�\x000e��]]��,���&��5v��J��rwz\x001d��������㟶��V��Z�x�\x0002��=�4�=�9\x0001{����ܾ�0ӧ:�?ϛ\x0016K8"<�D�M��T��|j|)
��8���\x0006�����}]��f'�6G�1��w�N�U�R<z_
\x000bnk��\x000eq��U��4Ji��kns@6��Hk���l�A��y��E�\x0008G��?j��L���H
O�P�ɓʹdzfǎD;�m��l�\x001e�cc\x001c,�~Ez�</p><p>G�\x001f��\x0015\x0011Œ[���i��+�JӬ��I7\x00037�\x0017\x0002K�\x001e"\x0014N����k���Y��
�C�[�d,\x0016\x0000g���n\x0016�PCW��`Q\x001b����Y�.�M7�hi��ɕƟ"/</p><p>���\x0005#h7Zh46���\x0014����J\x000fC)��\x001b[���U�,��\x000b���s�u�Tx�\x0003DS;���s<l�\x001e5�8\x0011���4\x000bF��Bc�� \x0013����$/�\x000fS���\x0006�f��p���h���'�{@��.j��<��Ὄ��A�:�	1$�z���xү��\x0010&\x0018J0o�(�bI�,S\��y7k7�ӯ/����ގ\x0019��X�1�M���T�ӽˇ-q�=\x001bf�r�\x000f\x0014:��"&Or���p����+���Ζ?G�4�\x0013��\x0010���5 %s��(�\x0004L�Tn����{�D�M��\x0004r��R^��H6��\x001e�</p><p>��	L�Ö8\x001f�ęP�w���;:�=�İ��H�e��񥼼�o\x0013�\x0005���\x00167rX�k-�=�U#_0�+��^��#¾\x0003=L\x0018on�?a|);w��z���HԘ\\x0012=?v=C�f�\x0016</p><p>��E�?���\x0019��O�K���1�@���[�\x0019���\x0003�J����ee}K\x000e)Ɲj�H�?$	#H�D\x0012�nr3����z0�\x000c��$\x0007�\x0001\x000e�([\x0010�\�A���j�x���\x001d0Φ(>�ZV�L��|�B��8\x0002�#K�6\x001c��� ã\x0016����!i�\x000b�����ɫ��z\x0000#ٻ�\x000b�S���\x000f[��5����1z�N�`�'�`R��v�k�;����b��Q����\x0005\x0013���_�oTB����,\x0018���\x0001�N��s���9m�#�`��u}��n\x000e\x001d6��i�����\x0001�@��e䶔����j-�c�N%\x0004���/\x0014fLs��\x001d��;�����vS�=��Aj���<�pD��V\x0017�]6L��\x0010إ��\x001c��[KRl�U�\x0000���R"\x0011a�H���s��m��O�2�\x001d�G��\x001cc�\x000f�\x000e8Z�!L$"�{�A��:�L�`d�\x000bfL���S��X\x001dLO�͘�d�T'�
\x0018v����nV��3}�s@�Mre�IM�As?:�L�`��m��
Q���y^D`���\x0001�}���\x0003���\x0016�{\x0007�y��6N\x001b�`�\x000f�2\x000fV<\x001d$\x0012\x0011\x001afg��9\x000c]\x0015n��@�`*�j\x0017إ��B�ܥ�=��u�F�i\x0007�.Ų;���h;���ʶ�aj\x0019��/F���V�8�h@���Q�=\x001b�˼��.\x0002�(�t��\x0019q>��݅��9n�Ou��\x0013�\x0001�������S����\x0000�?�ƞ��n\x0007��9ƽ�ne݆\x0000ӧ:YvGՀE·\x001e\x000f�p���\x001a5\x0006�\x0010�\x0017(��RK�=F�\x0005���\x0004�1ł�Z��5β�W
����\x0014c��Av�1���駕���9��o�oOs\x0017��qv�C�0����x\x0006|�Tr��j;߻��Ew\x001ebt��ŷTe|��!\x0010���(S��TbH#���</p><p>\x0006\x001d�ς�������m��M1^���K;:\x0007��XSm炉�̘�<�`�M��,��τ��,�ݡм��\x001f����j\x0007�[����Tm��wTx��Z</p><p>�ǐ�f\x0011�V*;���T����\x0001����@7W]�I\x000f'��=����46Ŏ�\x00038�\x0019Ӝ��j�\x0015�;��~a\x001b��M\x0006�o�\x001d�{�\x001e_Z�\x0008O\x001fW�!0D0\x000e\x001b���/1���w�\x001b#W���r�,���\x000b\x0011��S��~��Y�\>`�u����_(U��C��c,�?�}���n�\x0010�\x000bW4$E�jM���C4�\x000e\x001bO\x001d�'\x001c\x001cC\x0004�v�����Y�d#�{�q�w���B\x0010V�	���\x0010c?��3�%\0���j{z\x00011��ٝ>��W:�w�����P�\�\x0014G�oJ4�M1^�\x0012劆</p><p>&��7\x0014\x001d�h��n�j\x001d���|Z�轱�sz�������\x0014��[����xgO��Ρ�l���'SM�Й\x0016ȑ<��ϖ�Q\x0014\x001c%\x0016H�</p><p>�Z�gʅ�aE#��>�2d��Ў�\x001f��P�cd��ʁ�'χI��;���j{Ƨ1\x001cx����Z�5�˔\x000b\x0007�_d��1$�Mah��(�T���:\x000b��0��$TW9(+S\x001c�`��6��\x001ckx\x0012X�Ɂ!0t#�ϣ�\x00033��\x0013\x0015�Kq���t/2\x0014\x0013�qrEC\x0005[_���cG�oOo�\x0018���%\x0004n�z\x0019cH�7)!����d��F�&�}2\0>�Z�\x000f��f\x001c6t"�Y4�T<��\x001aۻ�I7:���a\��	|ʦ�h\x0011͛���VC�����n�z[\x0014\x000f�Q��J�J(Ә&\x0010L̞~��O\x001a�i�"R\x001e\x0008�\x000f�\x001e�ͦ��| $O����~\x001d�3ʪ��P����|�mN\x0005�)a\x000cEJX	Ԭ?�?ɰ�ɴM�J�p{P�mt\x0000�\x0013�xO�oO��D\x0002\x0012�"H���n�%\x0005dS���PT\x00046;8�Pd�v�4�3<����޽]����\x0002Gb���y�����Z	7h)��\x0003�\x0018t�z��c������+\x001c�ǎ��ْ�)*��\x0012()><Sќ|R\x0011o��y���M�]T���\x001f�</p><p>�gZ&���C�ޣ�H$���A�7�������崐�h\x001awu$\x001c\x000e���vM\x0017�R�;\x0014���\x0004�)EF�\x001c6\x001b��C0���.D�ePbbZϑ��t�7}��S��|�a�
�й���u�A�����{z ֝\x001c���,�F�\x0003\x001c\x000e(.N�5S(G��c�Ƿ�\x0014�SᵗM<�i���\x0019?�A�\x001d�[/�?��F���u�?(K����+%�x��+�|.2�)�+���n����@������@\x0011n�yՒ闾�iA-Q�\x0015�m��/�?��F�����?(�\x0002\x000b�mw�rw�GݒM�9�i�\x0007e9pm.l�\x0014��>�[�0�v�m\x0010@DT ģX���\x0013\x0015\x001e5/\x0017�s2�*��£��\x0014�ra��Q�Ź\x0012\x000b䨇�?(�\x0000����<'.p�ϣ\x000c_\x001f:\x001e��!�\x001c�w�	S\#�.e�Ro�ژkG�B0\x0000������ߕ�\x0013��%�\x0010�q�P�Rɵ+�G�\x0001���\x0008�\x001c��\��'����R)eJn�\x0016���\x0014\x0015J�Wx�eJ�\x0011�lW�Ȥ[�\x001fUxԬ|\x0012\x000b�Y\x000fӟPH��\x0011~����%�\x0008��P\�v��s��`�` 9_�\x000f�-\x0005�\x0000�r��\x001c\x0002n��yB�\x0019tf�ׂI\x0011\x000cʨDR4ߢ@|>\x000e\x0004��
\x0016z<�P��\x0019�����#�\x0019\x0015g\x0011p)\x0005�� \x0008�\x001fb�_}.�f��ɔ����#�\x0019�Ý(.ɵ/�\x00106��[\x000bI()</p><p>R0)\x0002\x00019_�g\x0005#\x001ca��۽^�J�]�JA\x000b&E  �b�\x0001���#�2]Ѓ�\x0005�\x001a%��z��\;��\x0011!���BR����p\x0011´L�B�B�(�-6�F\x0012�\x001a	"�ψ\x0013LD�8\x0010a�Jp��%��&�zG)6���q�E)5b'\x001dG�`�DD<�(�*��\x0008���\x0008c\x0001/�r\x0011\</p><p>�Q$�n\x0017�\x0005�J\x0011A\x0008\x0003\x0001\x0014\x0007�f\x0014{���u�W)\x0015<�Y\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b\x000b]�?�\x000f֥��w$\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.e925a679.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.e925a679.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.c7175140.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.c7175140.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "(this.webpackJsonpmobilic=this.webpackJsonpmobilic||[]).push([[5],[,,,,,,,function(e,t,n){"use strict";function r(e){var t,n,o="", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphoneplus_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphoneplus_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone6_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone6_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphonex_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphonex_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.94d74b14.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.81faf8eb.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
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
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/safari-mask-icon.svg](https://mobilic.beta.gouv.fr/safari-mask-icon.svg)
  
  
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
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/favicon.svg](https://mobilic.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/](https://mobilic.beta.gouv.fr/developers/)
  
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/favicon.svg](https://mobilic.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `00390625`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/splashscreens/iphonexr_splash.png](https://mobilic.beta.gouv.fr/splashscreens/iphonexr_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `89938344`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/safari-mask-icon.svg](https://mobilic.beta.gouv.fr/safari-mask-icon.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `00390625`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.80e832ca.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
Instances: 7
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>00390625, which evaluates to: 1970-01-05 12:30:25</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

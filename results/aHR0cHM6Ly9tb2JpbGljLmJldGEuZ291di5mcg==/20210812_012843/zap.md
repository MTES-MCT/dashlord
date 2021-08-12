
# ZAP Scanning Report

Generated on Thu, 12 Aug 2021 01:16:58


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
| Timestamp Disclosure - Unix | Informational | 9 | 

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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.24de514c.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.24de514c.chunk.js)
  
  
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
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.04c1d4a4.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.04c1d4a4.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/runtime-main.0c60339b.js](https://mobilic.beta.gouv.fr/static/js/runtime-main.0c60339b.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.24de514c.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.24de514c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nnrrrmrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrmmmmmmmnNmmmmmmrrmmNmmmmrr1111111111`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.04c1d4a4.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.04c1d4a4.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�z�j뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺뮺�i��i͚i��j�cf�i��]u�]u�]</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~playground.24de514c.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~playground.24de514c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/main.04c1d4a4.chunk.js](https://mobilic.beta.gouv.fr/static/js/main.04c1d4a4.chunk.js)
  
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/](https://mobilic.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphoneplus_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphoneplus_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone5_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone6_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphone6_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main.222ebf7f.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/splashscreens/iphonex_splash.png](https://mobilic.beta.gouv.fr/oauth/splashscreens/iphonex_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr](https://mobilic.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/fc-callback](https://mobilic.beta.gouv.fr/fc-callback)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/sitemap.xml](https://mobilic.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/static/js/runtime-main.0c60339b.js"></script>`
  
  
  
  
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
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/oauth/](https://mobilic.beta.gouv.fr/oauth/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/favicon.svg](https://mobilic.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/logo180.png](https://mobilic.beta.gouv.fr/logo180.png)
  
  
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
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/favicon.svg](https://mobilic.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `00390625`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/splashscreens/iphone6_splash.png](https://mobilic.beta.gouv.fr/splashscreens/iphone6_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `51781075`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/safari-mask-icon.svg](https://mobilic.beta.gouv.fr/safari-mask-icon.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `00390625`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/splashscreens/iphonex_splash.png](https://mobilic.beta.gouv.fr/splashscreens/iphonex_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `81442192`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/developers/](https://mobilic.beta.gouv.fr/developers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `43444956`
  
  
  
  
* URL: [https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js](https://mobilic.beta.gouv.fr/static/js/vendors~main~playground.a78b427e.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0123456789, which evaluates to: 1973-11-29 21:33:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

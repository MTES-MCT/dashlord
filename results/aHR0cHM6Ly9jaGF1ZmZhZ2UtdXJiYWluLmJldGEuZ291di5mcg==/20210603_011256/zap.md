
# ZAP Scanning Report

Generated on Thu, 3 Jun 2021 01:02:38


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 8 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 8 | 
| Reverse Tabnabbing | Medium | 7 | 
| Sub Resource Integrity Attribute Missing | Medium | 20 | 
| X-Frame-Options Header Not Set | Medium | 6 | 
| X-Frame-Options Setting Malformed | Medium | 1 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Cookie Without SameSite Attribute | Low | 5 | 
| Cookie Without Secure Flag | Low | 5 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 8 | 
| Feature Policy Header Not Set | Low | 8 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 9 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 7 | 
| Base64 Disclosure | Informational | 9 | 
| Information Disclosure - Suspicious Comments | Informational | 10 | 
| Modern Web Application | Informational | 7 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 7 | 
| Storable but Non-Cacheable Content | Informational | 3 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.youtube.com/channel/UC4I-TRQbiWfEdDvldAXg5ew' target='_blank'>Youtube</a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="s-common-button  s-font-body s-action-button" href="https://app.chauffage-urbain.beta.gouv.fr/chauffageurbain-copro?target=4fe79stwdrwh80p3545aac5m8&amp;params=%7B%7D" data-component="button" target="_blank">Tester mon éligibilité</a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="s-common-button  s-font-body s-action-button" href="https://app.chauffage-urbain.beta.gouv.fr/chauffageurbain-copro?target=4fe79stwdrwh80p3545aac5m8&amp;params=%7B%7D" data-component="button" target="_blank">Tester mon éligibilité</a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="s-common-button  s-font-body s-action-button" href="https://app.chauffage-urbain.beta.gouv.fr/chauffageurbain-copro?target=4fe79stwdrwh80p3545aac5m8&amp;params=%7B%7D" data-component="button" target="_blank">Tester mon éligibilité</a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="s-common-button  s-font-body s-action-button" href="https://app.chauffage-urbain.beta.gouv.fr/chauffageurbain-copro?target=4fe79stwdrwh80p3545aac5m8&amp;params=%7B%7D" data-component="button" target="_blank">Tester mon éligibilité</a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="s-common-button  s-font-body s-action-button" href="https://app.chauffage-urbain.beta.gouv.fr/chauffageurbain-copro?target=4fe79stwdrwh80p3545aac5m8&amp;params=%7B%7D" data-component="button" target="_blank">Tester mon éligibilité</a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="s-common-button  s-font-body s-action-button" href="https://app.chauffage-urbain.beta.gouv.fr/chauffageurbain-copro?target=4fe79stwdrwh80p3545aac5m8&amp;params=%7B%7D" data-component="button" target="_blank">Tester mon éligibilité</a>`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://static-assets.strikinglycdn.com/themes/s5-theme/main_v4.32b882548679c04c5642.bundle.css" ref="preload" as="style" onload="if(media!==&#39;screen&#39;)media=&#39;screen&#39;" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/detectIE-c385c24313ef0e9e4e7a1e131bf5e59f0fbd468f9f9ef44fd6739ae84ef0c0a4.js" async="async"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://static-assets.strikinglycdn.com/themes/s5-theme/main_v4.32b882548679c04c5642.bundle.css" ref="preload" as="style" onload="if(media!==&#39;screen&#39;)media=&#39;screen&#39;" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/i18n-2ace11ac644d0b40fb8b7cb65e9dd1e553022750e0254118dacbe1fe50735e97.js" async="async"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="76x76" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://static-assets.strikinglycdn.com/_reset-e86dc20205eb267eb1803edb4281063d0db8db4dde3345771532819dae916332.css" ref="preload" as="style" onload="if(media!==&#39;screen&#39;)media=&#39;screen&#39;" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_64,w_64,q_auto/2473357/661146_308058.png' rel='shortcut icon' type='image/x-icon'>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="60x60" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="120x120" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://fonts.googleapis.com/css?family=Montserrat:400,700&amp;subset=latin,latin-ext" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://static-assets.strikinglycdn.com/_reset-e86dc20205eb267eb1803edb4281063d0db8db4dde3345771532819dae916332.css" ref="preload" as="style" onload="if(media!==&#39;screen&#39;)media=&#39;screen&#39;" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/i18n-2ace11ac644d0b40fb8b7cb65e9dd1e553022750e0254118dacbe1fe50735e97.js" async="async"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="152x152" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://fonts.googleapis.com/css?family=Montserrat:400,700&amp;subset=latin,latin-ext" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="152x152" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_64,w_64,q_auto/2473357/661146_308058.png' rel='shortcut icon' type='image/x-icon'>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="60x60" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="120x120" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://user-images.strikinglycdn.com/res/hrscywv4p/image/upload/c_limit,fl_lossy,h_630,w_1200,f_auto,q_auto/2473357/264981_838726.png" rel="apple-touch-icon" sizes="76x76" />`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/detectIE-c385c24313ef0e9e4e7a1e131bf5e59f0fbd468f9f9ef44fd6739ae84ef0c0a4.js" async="async"></script>`
  
  
  
  
Instances: 20
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 6
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Setting Malformed
##### Medium (Medium)
  
  
  
  
#### Description
<p>An X-Frame-Options header was present in the response but the value was not correctly set.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  * Evidence: `Allow-From https://my.livechatinc.com/`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure a valid setting is used on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY.  Alternatively consider implementing Content Security Policy's "frame-ancestors" directive.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7034#section-2.1

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `XSRF-TOKEN`
  
  
  * Evidence: `Set-Cookie: XSRF-TOKEN`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `XSRF-TOKEN`
  
  
  * Evidence: `Set-Cookie: XSRF-TOKEN`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `XSRF-TOKEN`
  
  
  * Evidence: `Set-Cookie: XSRF-TOKEN`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `_bobcat_session`
  
  
  * Evidence: `Set-Cookie: _bobcat_session`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  * Parameter: `_bobcat_session`
  
  
  * Evidence: `Set-Cookie: _bobcat_session`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `XSRF-TOKEN`
  
  
  * Evidence: `Set-Cookie: XSRF-TOKEN`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `_bobcat_session`
  
  
  * Evidence: `Set-Cookie: _bobcat_session`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  * Parameter: `_bobcat_session`
  
  
  * Evidence: `Set-Cookie: _bobcat_session`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `XSRF-TOKEN`
  
  
  * Evidence: `Set-Cookie: XSRF-TOKEN`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `_bobcat_session`
  
  
  * Evidence: `Set-Cookie: _bobcat_session`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `_bobcat_session`
  
  
  * Evidence: `Set-Cookie: _bobcat_session`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `XSRF-TOKEN`
  
  
  * Evidence: `Set-Cookie: XSRF-TOKEN`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static-assets.strikinglycdn.com/i18n-2ace11ac644d0b40fb8b7cb65e9dd1e553022750e0254118dacbe1fe50735e97.js`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/i18n-2ace11ac644d0b40fb8b7cb65e9dd1e553022750e0254118dacbe1fe50735e97.js" async="async"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static-assets.strikinglycdn.com/jquery-f4e2137d267f77818d966e03df031337a38003039d43f15029422ddd171e14c4.js`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/jquery-f4e2137d267f77818d966e03df031337a38003039d43f15029422ddd171e14c4.js" defer="defer"><\/script>');
</script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static-assets.strikinglycdn.com/detectIE-c385c24313ef0e9e4e7a1e131bf5e59f0fbd468f9f9ef44fd6739ae84ef0c0a4.js`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/detectIE-c385c24313ef0e9e4e7a1e131bf5e59f0fbd468f9f9ef44fd6739ae84ef0c0a4.js" async="async"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `//ajax.googleapis.com/ajax/libs/jquery/1.10.0/jquery.min.js`
  
  
  * Evidence: `<script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.0/jquery.min.js" defer="defer"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static-assets.strikinglycdn.com/i18n-2ace11ac644d0b40fb8b7cb65e9dd1e553022750e0254118dacbe1fe50735e97.js`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/i18n-2ace11ac644d0b40fb8b7cb65e9dd1e553022750e0254118dacbe1fe50735e97.js" async="async"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//ajax.googleapis.com/ajax/libs/jquery/1.10.0/jquery.min.js`
  
  
  * Evidence: `<script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.0/jquery.min.js" defer="defer"></script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static-assets.strikinglycdn.com/jquery-f4e2137d267f77818d966e03df031337a38003039d43f15029422ddd171e14c4.js`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/jquery-f4e2137d267f77818d966e03df031337a38003039d43f15029422ddd171e14c4.js" defer="defer"><\/script>');
</script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static-assets.strikinglycdn.com/detectIE-c385c24313ef0e9e4e7a1e131bf5e59f0fbd468f9f9ef44fd6739ae84ef0c0a4.js`
  
  
  * Evidence: `<script src="https://static-assets.strikinglycdn.com/detectIE-c385c24313ef0e9e4e7a1e131bf5e59f0fbd468f9f9ef44fd6739ae84ef0c0a4.js" async="async"></script>`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, public, must-revalidate`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, public, must-revalidate`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/robots.txt](https://chauffage-urbain.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/robots.txt](https://chauffage-urbain.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/sitemap.xml](https://chauffage-urbain.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/robots.txt](https://chauffage-urbain.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  * Evidence: `ZGQ1TXpjT3FMQVYxQ1RPamxEZFdMMWdHNS9LbU1VQVZTc3FQdkkrcXBKdHFjdmJ0bTc2UXVjUTlYL3l6SWJZSmtJd1FIa2t6QlhQWUc3ck43dXVUWk1hU2R1RlIreEFXaUhBQnIvNHFJaDhEcUh6SmRVYW15OCtGQXVBYkkxS0dFSUt4RzREU0thL3U5eFZETXhBOW1RPT0tLVgzMGJnMWVhSEFCZ2dGQ1ptelRJSkE9PQ`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `Saz8C0q1NV5TO2VT1edn85DqFT1BLh`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `cxWXI6pakORJvJ7lQQvnL8tdNupJ6h8eE3yxAIRA2A3KHU66pOo61WtEq0x7rkLu`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>GIF89a\x0001\x0000\x0001\x0000\x0000\x0000\x0000!�\x0004\x0001</p><p>\x0000\x0001\x0000,\x0000\x0000\x0000\x0000\x0001\x0000\x0001\x0000\x0000\x0002\x0002L\x0001\x0000;</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<!-- removing_gon has activated 100%, so we add not_removing_gon rollout for specific user -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bDB\b and was detected in the element starting with: "<script></p><p>//<![CDATA[</p><p>window.$S={};$S.global_conf={"premium_apps":["HtmlApp","EcwidApp","MailChimpApp","CeleryApp","LocuApp"],"en", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_self" href="/"><span class="s-font-body">Accueil</span></a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_self" href="/"><span class="s-font-body">Accueil</span></a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_self" href="/"><span class="s-font-body">Accueil</span></a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_self" href="/"><span class="s-font-body">Accueil</span></a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type='text/javascript'>
window.location.href = "https://chauffage-urbain.beta.gouv.fr/"
</script>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_self" href="/"><span class="s-font-body">Accueil</span></a>`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_self" href="/"><span class="s-font-body">Accueil</span></a>`
  
  
  
  
Instances: 7
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found with a target of '_self' - this is often used by modern frameworks to force a full page reload.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain](https://chauffage-urbain.beta.gouv.fr/le-chauffage-urbain)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes](https://chauffage-urbain.beta.gouv.fr/pour-les-coproprietes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr](https://chauffage-urbain.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/partenaires](https://chauffage-urbain.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/accueil](https://chauffage-urbain.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/robots.txt](https://chauffage-urbain.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/ressources](https://chauffage-urbain.beta.gouv.fr/ressources)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json](https://chauffage-urbain.beta.gouv.fr/i/pwa/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/sitemap.xml](https://chauffage-urbain.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy](https://chauffage-urbain.beta.gouv.fr/pages/cookie-policy)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `13500000`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `13462511`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `13400001`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `18150336`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1622527331`
  
  
  
  
* URL: [https://chauffage-urbain.beta.gouv.fr/](https://chauffage-urbain.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `25124444`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>13500000, which evaluates to: 1970-06-06 06:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

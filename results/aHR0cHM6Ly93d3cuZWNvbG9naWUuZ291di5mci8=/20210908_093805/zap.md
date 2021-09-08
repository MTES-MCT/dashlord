
# ZAP Scanning Report

Generated on Wed, 8 Sep 2021 09:28:27


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 9 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| Vulnerable JS Library | Medium | 2 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 9 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Secure Pages Include Mixed Content | Low | 1 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 12 | 
| Non-Storable Content | Informational | 7 | 
| Retrieved from Cache | Informational | 11 | 
| Storable and Cacheable Content | Informational | 4 | 
| Timestamp Disclosure - Unix | Informational | 10 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 4 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.png](https://www.ecologie.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpeg](https://www.ecologie.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css](https://www.ecologie.gouv.fr/profiles/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.svg](https://www.ecologie.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpg](https://www.ecologie.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js](https://www.ecologie.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css](https://www.ecologie.gouv.fr/core/*.css)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.svg](https://www.ecologie.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.js$](https://www.ecologie.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/node/add/](https://www.ecologie.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.svg](https://www.ecologie.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/filter/tips](https://www.ecologie.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/admin/](https://www.ecologie.gouv.fr/index.php/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/admin/](https://www.ecologie.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="svg-link" href="https://www.facebook.com/Ecologie.Gouv" rel="nofollow noopener" target="_blank">
    <!--<svg aria-hidden="true" class="icon"><use xlink:href="#icon-fb"></use></svg>-->
      <svg focusable="false" aria-hidden="true" version="1.1" class="icon icon-fb" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      	 viewBox="0 0 60 60" enable-background="new 0 0 60 60" xml:space="preserve">
      <circle fill="#BABCBD" cx="30.3" cy="29.9" r="28.4"/>
      <g>
      	<g>
      		<path fill-rule="evenodd" clip-rule="evenodd" fill="#FFFFFF" d="M31.6,25.1v-5.3c0,0,0-2,2.3-2h3.4l0-4.9h-4.2c0,0-7.1-0.5-7.1,7
      			c0,1.6,0,5.2,0,5.2l-4.1,0v4h4V47h5.7V29.2l5.3,0l1.1-4.1L31.6,25.1z"/>
      	</g>
      </g>
      </svg>
      <span class="show-for-sr">Compte Facebook du Ministère de la Transition écologique (Ouvrir dans une nouvelle fenêtre)</span>
      </a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/styles/thumb_330/public/photo%20actu.png?itok=bnNNYN4M](https://www.ecologie.gouv.fr/sites/default/files/styles/thumb_330/public/photo%20actu.png?itok=bnNNYN4M)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Cù<¢­ý>r:\x0019Ä\x001a\x0015(ÊM²\x001aSIfYÆãÇÏAEDADS[fÓ8´}O¦\x0008¡ÈËÍªGiXìú¢|ß·¬×ÅÐ¯´\x0004¡¦nZLëö}ß3\x001e=\x0010e1Ã÷+=\x00063B\x0002å}¸Ùhí}2\x0017'¨ÊÖ'§\x0003ÿ\x0002«Û80mKÛø\x0004u \x0003n\x001cÝàÕ{wyõÖuÒ@²^mi{\x000cCh\x0004ÂZ\x0018nn0
	£\x0010\x001dz¬¥Òºö_²¦ñÉA­}Ykí \x001a\x0010=ÎùgÓzÝ\x001føpIÓ´Ã\x000bµ§·CO9?²í2Ò÷Ã¡GÜÔþ&\×5q\x0012¦	}oÉ·\x0015«åù|\x0007)4õñdÃê­õ]ÚÎtè@ùÝo\x0014³^oÑZ{ÜbÛ\x000c¬^\x0002ÕJ\x0013ÅO^\x0007¡×¿¹ZAO1E^r|r\x0010>=î(ÔÌ³D­
¶Ë%¿~ÄGøü9>>á£~Ç»·¹{÷\x0016¦mùùOÆgD]w\x001cì,Ø\x0014\x0015mÉhÐµ\x001dÏÐ4%»;sLkN"&£1w\x001f¼Éÿýïßã×pÅ\x000bï5\x0006ª®@\x0004\x0013Þ[¥<ætuIo,eÝ¡ïa'©él¶\x0005§[:ã»æ|;üzzÕË\x001aÙt:½êûÎruÎ9öçc²$b³Ù ´äôìë7n±ØsýÚ\x0001BJ\x000eÈ·kvw÷¹sï\x001aû{\x0007'c>üøK¾ýí7IÓélÂjå/×öYo·l$NýÔeü¥Yi;övwXm6\x0004Ê±¿³Ãn"\x0018'\x0019q ÑqÂîÞ\x001eB8\x0016;\x000bâ8"Ë¼Þ\x0010×\x0013è\x0005<°ÝÐµÎ//	tÀþíù\x0016U^1<üóÓcºÞÒ\x001bGUWt\x0019Vy¢¬8¹Ü\x0010§\x0013Ë\x0015ÖÂd:ã\x0007¯²º<G(í-,Æô={×¸}ë&Ë\x000bªb\x0005êº\x0019^f\x001e_Ú4
½slób0WÞÓmzº¶§(\x000b«­?¸jÏ·ÎÑ´-MÛ±ÉsÖ
Bj¶yNo_z\x001b6yuprzFï (JÊª\x001aBþ\x0010Ü´\x0006d@Ý\x0019Ï¿îº¡/¯\x000eÍ/Ñ²JyÑJ7TÒ65E±õUA	§çgl6\x001bÚ¶¡ªJÚ¯å8¦íZæó9~ò1Á?Ü6-R\x0005H\x001ceQ #ï\x001fPÃ*MjM9´#¬óä?\x0007ÔMCÓtDqH6IüE(ª¶"\x0008\x0002ÍËõ|½å`gçß<g6\x0012g	×wÇ¨òÃïþåh\x001c\x0013\x0007Å,#\x001e\x000cp8)È«
I\x0014R\x0016\x0015DÊ²]u¬×Kvw\x0017l4K\x0002°ÉxD[\x0017Ìf\x000b¬$\x000eñ«,ÿ\x0003CI¦³1a¨¯º¤Æø"}\x0012û.«ÒpÿÛè\x0018\x000e\x000f\x0016\rúbE\x0014DtôL§
Ó\x0014\x0004qJßûtYo|îÓ¿a4RN\x000et¨npßjÌÐãl[C7¸\x000e.N\x000b²,¤©,§ÇçLÇ\x0013ÚÖk\x000bmg¾g ®\x001cÛMÁùYé`¾;¡(jß=+*@c'ûÜº9åG?Y`ª³g\x0015UÝ°³³Ïéù3Æ£\x0011QÖ\x0012\x00070ê0\x0006L­èmÁîbÎ$Ã\x0014×ödi±^ÝhÄAí\x001dÙ,Dë\x0008\x001dmiûçDai\x0014RÆ>á«*vöcTP£CG\x0014\x0007Î t ¯¾t~ä4Ôz\x0002IÝ\x0018òMq%ghÓ·\x0013  ôNá¢È}íhp@ ­\x001dÛuÁ(Î¸}ý&oÝ¿ÏbÑ\x0014[¤í±ÎQ5MÓÑõ^µW\x0016µï\x0007\x0001\x0016\x001f*Zm¶¬×[²4&Í2\x0004\x0018pø
\x000eÊÊ^â/ÜïûÞ\x000ep\x0010èLwõk%Ã!h'ÑÁK	ß\x0011+%\x0007«\x0012OØï2­µ¬\x0015E~¬ß;ºÎF¼H¾½\x001aoa¡i
A\x0018e	JÊ«Ä¸w£jßiV¾\x0002StÆlðLïPGÃê#Ä:KYU\x0003û¼c<\x001e\x000f'ïªjhêËË\x001cÚ\x0015#©Ð#ËFDZ0\x001cUU\x0010×^ÈÙù);Ó	ß|õ\x0005ôÇßçñÓ§,æcÞ{ÿ·<qÂý×îÑ4\x001d/Îrö®ßfïú-²ñ\x0001\x0018\x0019\x001dìñów?ãæþ\x000e»»sT8æ«¯1\x001a§8"r7æNVûÉP^PT
IäÎ
?U1x£ôÐ(|O{x!Áõ,üO\x0008mý\x00000Î±¿\x0011\x001e\x0007è\x0000×;îÝ»çÐÓ1Ö\x001aÒ4áþ×øüóoøÃ?ü\x000eqâû·ÇÇç¼õí$QÌÎbÎñé\x0005ãQÆÁÑ>|ú×;¶\x001dEQ0\x001ae²0\x000c©«(\x000cp\x000eÂ8¢5°;)ó½Ý\x0005:Ôè0ô\x001dÞ2'#Úºòr4¡íüYXëó	m³¾©Aj¦×\x001fÐu
vý*ßÐ5\x0015½µ¬Vk\x0015QHQ\x0014\x0014eIQ·A\x0005)N(Vë5Ji¢$å\x0007¯ñÕ3M9=>cwgNÛ´<|ó-övùÙü\x001b\x001cÞklzï¿nZï§.¦3Xç<\x001b3\x0015Ò7\x001aÊª¡·xSíÑAÀz½¡wÞ9:ÓÓvM^"¢jZÖ\x001c¥5EYQ·-ÖAQU\x0008¥\x0011Òçhüa ¥1=V(TW<\x0002k\x0007xSãW/½Þa\x0018 \x0007L®_):Ó$\x0011Aà+~ûû\x0014Eðj1´ö«³Ù|Ê¿ûÀ³Ïë\x001a!g¬+éZÊª¦nz\x000e¯_§È7ÔÿYõñIï¾§íZ&1Aè1»a\x001cq¹ZS5Z\x0005ÄIÂ½;÷¸¼¼¤1\x001dÕ6Ç\x0018C\x0011\x0006 -é¨ò\x001c}ýú>­k(MGyr2mYÑÅÐ´^u&d}QÁ¬G1;»	TÔMí:d`2Öë\x001a­Ä@\x001f2à\x001cçç\x001b\x0016)m[à Cö¥ý|Õà¬Å"PZ\x0001
©4JômNo
çg'$Ñ\x0018\x0010TmÍþá>aäp\x0004°.ÙnrâpÞ]:\x001a'~Ù/a½\Ó·2o	\x0002A¾õ|[±\x0015\x0001¶ëÉ:7^ÖPJÖ®ô//i©÷OJ#hK¼\x00035Ébî>8¤kKªºÂ\x0019Ï(\x0016Útä¸{OÐ\x0015%iÇ\x001fýpâÉKí%;\x000f&8Bzáh·9Ù$Dg£³;ä&§£¡j\x001cm[Óö\x0005V(¤õÁ£IøÓÞFÒuñ$&\x0008\x0004pN@Çc\x001c\x0017m¹¦ªefR#\x0002\x001dÑ6Í e\x000c(Kí[­\x000bªÚ<ëºD\x0008GÄhåÁ	R(LÓÐ\x001a\x001dJ¤T¬W\x0005Q\x0018óUeóÞ§ñþ'°NH³ 		³óK¿¯\x001cª5¸0	\x0011²Ç:ÿ\x0010®¶í\x0011"\x0000©Ù\x0016\x001fÓ
\x0007ÃNZiEYÔØÞçýÙNâ \x001cð\x0002o½zyó\x0010B\x0011GP\x0005´mãSÑö÷élkýËö%XÄ9K \x0003FÙ\x0018ª*"ßÍB³³;g½ÜÒwv\x0018Õ5 \x0004þzg©õÁÃ0é{CUÄI1õDïðñ7Io,I\x001c!¤ÀT\x001d%\x0011a\x0010ã¬#IRÚ¦\x0005ai\x001bã\x000f\x0003]T\x0011ßºÀk;\x0007ô©C»Ð7ôÛ\x0017=¨`Ìåå_ýú]þìÇ?äÇú#d¢tâÓàUCß\x0018¶«
8{¯\x001aÉ£\x001b;ôuÁº(\x0010N¢fõg»/9^]2\x001aÆ\x0005ÿÕ\x000f^ãôÑ)ÅV \x0003It]C[w8ë\x000fÄ\x0007¯ÜàüdIe\x001d\x0008¯[\x000cÍfK\x001cÇDQDYVDQru°	Ãª®éÑlñØ<\x001d=é8\x0002îÝ¾\x0003J uÀbwÁb¾ *\x001bê°f±³`2Ð\x0005­OºOÆwK7ñ\x00139iHS~¯ëÚÛÃ"Ï®ª\x0002D@\x0012ÆÌ'\x0019\x000f_½ëjrk)-Q 	\x0003EoÚ«uBQlàñÞï¢@H
!4\x0018\x00000Yµ\x000f0µ
e]ù©\]QÕ%\x0008%)ª0JÍ2¬\x000c@@Û5C^3ï\x000eä\x0000)5Bôüêï~\x0018èq>­Ý\x0012Æ!EY"¯\x00109gpÔ\x0013_×-ÖJ@\x000cúPc\x00152 ¬*pÖ\x0018ò/1Ku¬¶ÞjÖ,79i\x0012c\x001d^ª\x000cuÎzX'\x000c ¢mêÁ\x0014æh\x001a&Þl6ÿp\x0017#¥¤i*Lo®¦'a\x0010\x0011áP\x001fõÎª*ü¦ï¯¤/\x0017äeÃ
¡Lëyö\x000e\x000e\x000e\x000eèû\x000fÏGm\x0004_|ù%ô-é½£C\x001e=~4ÈijFÙÌ\x0007Ã°ììN©ë\x000eÓÀ+÷n²<_a­àäôºö
qP6\x0005u^c	bqïáCôb>á|{AÞ¤2¦r
4,k:çxïljê²G	C6
¸}#cTe@U7\x001e¿%\x001cç§EM bB\x0015P5^\x0003\x001e(W\l¼¸<}ÍçòrE\x0014\x0004Ôµa[^â\x001c\\x001bnß;b³¹ä¬9£*{æ»\x0013Î^¬èÌÞXª²c±7GËgONI$Ñ\^ä¨@ÎüØk±R\x0014\x001bvög(¡)ºèHG\x0011õp{ÑC ¼ùÉx]s
ã?%½ì\x0001'I\x000e½<¼i-Ï¾YS%Qè±p\x0007G»Ü¿5âí74½íyþ<gï(a¾\x0013r~ÖÆ\x0002a+¢4`Ui¾þª$ÉB\x0017Pª\x0006è	Â³ó-u\x0011â×8Ö­a< ¬¥Ø\x0016ìïÌ²g4}Ï®í1Í4Üa½]ÒÚ\x0015}\x001fP,·è0`\x0014Þ\x0000+=\x001fß3´½£5÷\x0004\x001eÓ;Úºô·åh`IW>¤\x0017©¯ÿ(ç\x0001\x0015uEÓ´þ¶iíðîØ°Dë\x0000\x001dLi[Ëy¾Üç\x001b¤ÉdB4\x0016Dh¶\x0016c@ö@+So}@\x0007	§gKÒÔ3½¥ÃCÁ'#4D5-«M
©\x0018à\x001c~gY×
Bø}ªÒ>©\x00062UÛù¦\x0016jP<
ï9V/\x0005\x000f¾£«C­{¦)Q¨q¶'"V«-i:&M\x0012<y³=uÝ\x0002¦kDH·\x0003¥IÓÛ\x000e\x0015Î	òmí%\x0001ID×¶(åk8QäoA\x0010"\x0015t]Ã(ÓÔW}\x0006\x0001ÐE\x0014Æt\x0006î\x001cLÙ'\x0010(¬\x001a¦ã\x0019½#Â ôàúÅ.'\x0007¸Öñåó\x0013<?\x001e´((s oÛ\x001eèÉ§ïþöç?æÛßý\x000eÇ\x0017/xòÅ\x0017\4|òÁûüÝÅ\x0005¶¤¸¸äîõ]Ú¦âw÷ïÌ'\x0014E\x000e\x0016±(-\x0018g\x0019\x0017K\x000fcèÝÐHJ¶[_µê\x0007\x0003U\x0014Ì&#ëÍp\x0000êi\x001a¥!\x0012zS\x0013DS¤éº0\x0018$ízK\x0014ÆÄ±\x000fM\x0002ë\x001d4Iýg4êQjR4\x001dSØ0TDaÒ$®\x0018ÇRJÄc1¦&\x0008ýTÐ8ß\x0011·Æøçéyòô)J8Æ»{ô]!$"ó\x0002\x001b-¯\x001cõ\x001du]\x000c.AWµ¶ÃYGÑ\x0008fEéyíR 0\x0004ZyF\x0012Ñ-§çK?1Ô¢l\x0018\x0007\x0019B\x0007\x001e|¢\x00152Ô¬.ØÖòñ§_\x0013Ä\x0011¼ iZf\x0011Íj½$\x000eýZÃá(«4ý$Á	\x0013\.7¤hVeºiè­Fêº®i»vØÝ*0&ßn\x0008BTÆcjÂZè\x001aÿÄ	6ÛÒ:Ø3!¥ný­z4\x001a±Í\x000bÂØ7b(f³^#$\x000c3¬õõC÷\x0018V;Pì^ÞÍPß³\x001b=\x000cc6- \x0018F8ç(ÜïËétJ×\x001a\x0012í§gmÛrüü\x0019R+
h·\x001b\\x0003®ïÔO\x001e³¼¼$Ð\x001aDÀÙÅ¾ï8Ü? *kÀ1\x0008\x0002\x0003?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=Cù<¢­ý>r:\x0019Ä\x001a\x0015(ÊM²\x001aSIfYÆãÇÏAEDADS[fÓ8´}O¦\x0008¡ÈËÍªGiXìú¢|ß·¬×ÅÐ¯´\x0004¡¦nZLëö}ß3\x001e=\x0010e1Ã÷+=\x00063B\x0002å}¸Ùhí}2\x0017'¨ÊÖ'§\x0003ÿ\x0002«Û80mKÛø\x0004u \x0003n\x001cÝàÕ{wyõÖuÒ@²^mi{\x000cCh\x0004ÂZ\x0018nn0</p><p>	£\x0010\x001dz¬¥Òºö_²¦ñÉA­}Ykí \x001a\x0010=ÎùgÓzÝ\x001føpIÓ´Ã\x000bµ§·CO9?²í2Ò÷Ã¡GÜÔþ&\×5q\x0012¦	}oÉ·\x0015«åù|\x0007)4õñdÃê­õ]ÚÎtè@ùÝo\x0014³^oÑZ{ÜbÛ\x000c¬^\x0002ÕJ\x0013ÅO^\x0007¡×¿¹ZAO1E^r|r\x0010>=î(ÔÌ³D­</p><p>¶Ë%¿~ÄGøü9>>á£~Ç»·¹{÷\x0016¦mùùOÆgD]w\x001cì,Ø\x0014\x0015mÉhÐµ\x001dÏÐ4%»;sLkN"&£1w\x001f¼Éÿýïßã×pÅ\x000bï5\x0006ª®@\x0004\x0013Þ[¥<ætuIo,eÝ¡ïa'©él¶\x0005§[:ã»æ|;üzzÕË\x001aÙt:½êûÎruÎ9öçc²$b³Ù ´äôìë7n±ØsýÚ\x0001BJ\x000eÈ·kvw÷¹sï\x001aû{\x0007'c>üøK¾ýí7IÓélÂjå/×öYo·l$NýÔeü¥Yi;övwXm6\x0004Ê±¿³Ãn"\x0018'\x0019q ÑqÂîÞ\x001eB8\x0016;\x000bâ8"Ë¼Þ\x0010×\x0013è\x0005<°ÝÐµÎ//	tÀþíù\x0016U^1<üóÓcºÞÒ\x001bGUWt\x0019Vy¢¬8¹Ü\x0010§\x0013Ë\x0015ÖÂd:ã\x0007¯²º<G(í-,Æô={×¸}ë&Ë\x000bªb\x0005êº\x0019^f\x001e_Ú4
½slób0WÞÓmzº¶§(\x000b«­?¸jÏ·ÎÑ´-MÛ±ÉsÖ
Bj¶yNo_z\x001b6yuprzFï (JÊª\x001aBþ\x0010Ü´\x0006d@Ý\x0019Ï¿îº¡/¯\x000eÍ/Ñ²JyÑJ7TÒ65E±õUA	§çgl6\x001bÚ¶¡ªJÚ¯å8¦íZæó9~ò1Á?Ü6-R\x0005H\x001ceQ #ï\x001fPÃ*MjM9´#¬óä?\x0007ÔMCÓtDqH6IüE(ª¶"\x0008\x0002ÍËõ|½å`gçß<g6\x0012g	×wÇ¨òÃïþåh\x001c\x0013\x0007Å,#\x001e\x000cp8)È«
I\x0014R\x0016\x0015DÊ²]u¬×Kvw\x0017l4K\x0002°ÉxD[\x0017Ìf\x000b¬$\x000eñ«,ÿ\x0003CI¦³1a¨¯º¤Æø"}\x0012û.«ÒpÿÛè\x0018\x000e\x000f\x0016\rúbE\x0014DtôL§</p><p>Ó\x0014\x0004qJßûtYo|îÓ¿a4RN\x000et¨npßjÌÐãl[C7¸\x000e.N\x000b²,¤©,§ÇçLÇ\x0013ÚÖk\x000bmg¾g ®\x001cÛMÁùYé`¾;¡(jß=+*@c'ûÜº9åG?Y`ª³g\x0015UÝ°³³Ïéù3Æ£\x0011QÖ\x0012\x00070ê0\x0006L­èmÁîbÎ$Ã\x0014×ödi±^ÝhÄAí\x001dÙ,Dë\x0008\x001dmiûçDai\x0014RÆ>á«*vöcTP£CG\x0014\x0007Î t ¯¾t~ä4Ôz\x0002IÝ\x0018òMq%ghÓ·\x0013  ôNá¢È}íhp@ ­\x001dÛuÁ(Î¸}ý&oÝ¿ÏbÑ\x0014[¤í±ÎQ5MÓÑõ^µW\x0016µï\x0007\x0001\x0016\x001f*Zm¶¬×[²4&Í2\x0004\x0018pø</p><p>\x000eÊÊ^â/ÜïûÞ\x000ep\x0010èLwõk%Ã!h'ÑÁK	ß\x0011+%\x0007«\x0012OØï2­µ¬\x0015E~¬ß;ºÎF¼H¾½\x001aoa¡i
A\x0018e	JÊ«Ä¸w£jßiV¾\x0002StÆlðLïPGÃê#Ä:KYU\x0003û¼c<\x001e\x000f'ïªjhêËË\x001cÚ\x0015#©Ð#ËFDZ0\x001cUU\x0010×^ÈÙù);Ó	ß|õ\x0005ôÇßçñÓ§,æcÞ{ÿ·<qÂý×îÑ4\x001d/Îrö®ßfïú-²ñ\x0001\x0018\x0019\x001dìñów?ãæþ\x000e»»sT8æ«¯1\x001a§8"r7æNVûÉP^PT
IäÎ</p><p>?U1x£ôÐ(|O{x!Áõ,üO\x0008mý\x00000Î±¿\x0011\x001e\x0007è\x0000×;îÝ»çÐÓ1Ö\x001aÒ4áþ×øüóoøÃ?ü\x000eqâû·ÇÇç¼õí$QÌÎbÎñé\x0005ãQÆÁÑ>|ú×;¶\x001dEQ0\x001ae²0\x000c©«(\x000cp\x000eÂ8¢5°;)ó½Ý\x0005:Ôè0ô\x001dÞ2'#Úºòr4¡íüYXëó	m³¾©Aj¦×\x001fÐu
vý*ßÐ5\x0015½µ¬Vk\x0015QHQ\x0014\x0014eIQ·A\x0005)N(Vë5Ji¢$å\x0007¯ñÕ3M9=>cwgNÛ´<|ó-övùÙü\x001b\x001cÞklzï¿nZï§.¦3Xç<\x001b3\x0015Ò7\x001aÊª¡·xSíÑAÀz½¡wÞ9:ÓÓvM^"¢jZÖ\x001c¥5EYQ·-ÖAQU\x0008¥\x0011Òçhüa ¥1=V(TW<\x0002k\x0007xSãW/½Þa\x0018 \x0007L®_):Ó$\x0011Aà+~ûû\x0014Eðj1´ö«³Ù|Ê¿ûÀ³Ïë\x001a!g¬+éZÊª¦nz\x000e¯_§È7ÔÿYõñIï¾§íZ&1Aè1»a\x001cq¹ZS5Z\x0005ÄIÂ½;÷¸¼¼¤1\x001dÕ6Ç\x0018C\x0011\x0006 -é¨ò\x001c}ýú>­k(MGyr2mYÑÅÐ´^u&d}QÁ¬G1;»	TÔMí:d`2Öë\x001a­Ä@\x001f2à\x001cçç\x001b\x0016)m[à Cö¥ý|Õà¬Å"PZ\x0001</p><p>©4JômNo
çg'$Ñ\x0018\x0010TmÍþá>aäp\x0004°.ÙnrâpÞ]:\x001a'~Ù/a½\Ó·2o	\x0002A¾õ|[±\x0015\x0001¶ëÉ:7^ÖPJÖ®ô//i©÷OJ#hK¼\x00035Ébî>8¤kKªºÂ\x0019Ï(\x0016Útä¸{OÐ\x0015%iÇ\x001fýpâÉKí%;\x000f&8Bzáh·9Ù$Dg£³;ä&§£¡j\x001cm[Óö\x0005V(¤õÁ£IøÓÞFÒuñ$&\x0008\x0004pN@Çc\x001c\x0017m¹¦ªefR#\x0002\x001dÑ6Í e\x000c(Kí[­\x000bªÚ<ëºD\x0008GÄhåÁ	R(LÓÐ\x001a\x001dJ¤T¬W\x0005Q\x0018óUeóÞ§ñþ'°NH³ 		³óK¿¯\x001cª5¸0	\x0011²Ç:ÿ\x0010®¶í\x0011"\x0000©Ù\x0016\x001fÓ</p><p>\x0007ÃNZiEYÔØÞçýÙNâ \x001cð\x0002o½zyó\x0010B\x0011GP\x0005´mãSÑö÷élkýËö%XÄ9K \x0003FÙ\x0018ª*"ßÍB³³;g½ÜÒwv\x0018Õ5 \x0004þzg©õÁÃ0é{CUÄI1õDïðñ7Io,I\x001c!¤ÀT\x001d%\x0011a\x0010ã¬#IRÚ¦\x0005ai\x001bã\x000f\x0003]T\x0011ßºÀk;\x0007ô©C»Ð7ôÛ\x0017=¨`Ìåå_ýú]þìÇ?äÇú#d¢tâÓàUCß\x0018¶«
8{¯\x001aÉ£\x001b;ôuÁº(\x0010N¢fõg»/9^]2\x001aÆ\x0005ÿÕ\x000f^ãôÑ)ÅV \x0003It]C[w8ë\x000fÄ\x0007¯ÜàüdIe\x001d\x0008¯[\x000cÍfK\x001cÇDQDYVDQru°	Ãª®éÑlñØ<\x001d=é8\x0002îÝ¾\x0003J uÀbwÁb¾ *\x001bê°f±³`2Ð\x0005­OºOÆwK7ñ\x00139iHS~¯ëÚÛÃ"Ï®ª\x0002D@\x0012ÆÌ'\x0019\x000f_½ëjrk)-Q 	\x0003EoÚ«uBQlàñÞï¢@H</p><p>!4\x0018\x00000Yµ\x000f0µ
e]ù©\]QÕ%\x0008%)ª0JÍ2¬\x000c@@Û5C^3ï\x000eä\x0000)5Bôüêï~\x0018èq>­Ý\x0012Æ!EY"¯\x00109gpÔ\x0013_×-ÖJ@\x000cúPc\x00152 ¬*pÖ\x0018ò/1Ku¬¶ÞjÖ,79i\x0012c\x001d^ª\x000cuÎzX'\x000c ¢mêÁ\x0014æh\x001a&Þl6ÿp\x0017#¥¤i*Lo®¦'a\x0010\x0011áP\x001fõÎª*ü¦ï¯¤/\x0017äeÃ
¡Lëyö\x000e\x000e\x000e\x000eèû\x000fÏGm\x0004_|ù%ô-é½£C\x001e=~4ÈijFÙÌ\x0007Ã°ììN©ë\x000eÓÀ+÷n²<_a­àäôºö
qP6\x0005u^c	bqïáCôb>á|{AÞ¤2¦r
4,k:çxïljê²G	C6</p><p>¸}#cTe@U7\x001e¿%\x001cç§EM bB\x0015P5^\x0003\x001e(W\l¼¸<}ÍçòrE\x0014\x0004Ôµa[^â\x001c\\x001bnß;b³¹ä¬9£*{æ»\x0013Î^¬èÌÞXª²c±7GËgONI$Ñ\^ä¨@ÎüØk±R\x0014\x001bvög(¡)ºèHG\x0011õp{ÑC ¼ùÉx]s
ã?%½ì\x0001'I\x000e½<¼i-Ï¾YS%Qè±p\x0007G»Ü¿5âí74½íyþ<gï(a¾\x0013r~ÖÆ\x0002a+¢4`Ui¾þª$ÉB\x0017Pª\x0006è	Â³ó-u\x0011â×8Ö­a< ¬¥Ø\x0016ìïÌ²g4}Ï®í1Í4Üa½]ÒÚ\x0015}\x001fP,·è0`\x0014Þ\x0000+=\x001fß3´½£5÷\x0004\x001eÓ;Úºô·åh`IW>¤\x0017©¯ÿ(ç\x0001\x0015uEÓ´þ¶iíðîØ°Dë\x0000\x001dLi[Ëy¾Üç\x001b¤ÉdB4\x0016Dh¶\x0016c@ö@+So}@\x0007	§gKÒÔ3½¥ÃCÁ'#4D5-«M</p><p>©\x0018à\x001c~gY×
Bø}ªÒ>©\x00062UÛù¦\x0016jP<</p><p>ï9V/\x0005\x000f¾£«C­{¦)Q¨q¶'"V«-i:&M\x0012<y³=uÝ\x0002¦kDH·\x0003¥IÓÛ\x000e\x0015Î	òmí%\x0001ID×¶(åk8QäoA\x0010"\x0015t]Ã(ÓÔW}\x0006\x0001ÐE\x0014Æt\x0006î\x001cLÙ'\x0010(¬\x001a¦ã\x0019½#Â ôàúÅ.'\x0007¸Öñåó\x0013<?\x001e´((s oÛ\x001eèÉ§ïþöç?æÛßý\x000eÇ\x0017/xòÅ\x0017\4|òÁûüÝÅ\x0005¶¤¸¸äîõ]Ú¦âw÷ïÌ'\x0014E\x000e\x0016±(-\x0018g\x0019\x0017K\x000fcèÝÐHJ¶[_µê\x0007\x0003U\x0014Ì&#ëÍp\x0000êi\x001a¥!\x0012zS\x0013DS¤éº0\x0018$ízK\x0014ÆÄ±\x000fM\x0002ë\x001d4Iýg4êQjR4\x001dSØ0TDaÒ$®\x0018ÇRJÄc1¦&\x0008ýTÐ8ß\x0011·Æøçéyòô)J8Æ»{ô]!$"ó\x0002\x001b-¯\x001cõ\x001du]\x000c.AWµ¶ÃYGÑ\x0008fEéyíR 0\x0004ZyF\x0012Ñ-§çK?1Ô¢l\x0018\x0007\x0019B\x0007\x001e|¢\x00152Ô¬.ØÖòñ§_\x0013Ä\x0011¼ iZf\x0011Íj½$\x000eýZÃá(«4ý$Á	\x0013\.7¤hVeºiè­Fêº®i»vØÝ*0&ßn\x0008BTÆcjÂZè\x001aÿÄ	6ÛÒ:Ø3!¥ný­z4\x001a±Í\x000bÂØ7b(f³^#$\x000c3¬õõC÷\x0018V;Pì^ÞÍPß³\x001b=\x000cc6- \x0018F8ç(ÜïËétJ×\x001a\x0012í§gmÛrüü\x0019R+</p><p>h·\x001b\\x0003®ïÔO\x001e³¼¼$Ð\x001aDÀÙÅ¾ï8Ü? *kÀ1\x0008\x0002\x0003?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" type="application/rss+xml" title="Ministère de la Transition écologique - Actualités" href="https://www.ecologique-solidaire.gouv.fr/rss_actualites.xml" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" type="application/rss+xml" title="Ministère de la Transition écologique - Actualités" href="https://www.ecologique-solidaire.gouv.fr/rss_actualites.xml" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" type="application/rss+xml" title="Ministère de la Transition écologique - presse" href="https://www.ecologique-solidaire.gouv.fr/rss_presse.xml" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" type="application/rss+xml" title="Ministère de la Transition écologique - presse" href="https://www.ecologique-solidaire.gouv.fr/rss_presse.xml" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" type="application/rss+xml" title="Ministère de la Transition écologique - presse" href="https://www.ecologique-solidaire.gouv.fr/rss_presse.xml" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="canonical" href="https://www.ecologique-solidaire.gouv.fr" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" type="application/rss+xml" title="Ministère de la Transition écologique - Actualités" href="https://www.ecologique-solidaire.gouv.fr/rss_actualites.xml" />`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="canonical" href="https://www.ecologique-solidaire.gouv.fr" />`
  
  
  
  
Instances: 9
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 3.4.1 is vulnerable.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/js/js_x-rGi6VZta-h_25NgKXTWomMli4rdvWXfp7H4jjljWA.js](https://www.ecologie.gouv.fr/sites/default/files/js/js_x-rGi6VZta-h_25NgKXTWomMli4rdvWXfp7H4jjljWA.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v3.4.1`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/js/js_k1Q9llQIQyiQ0PsBqGlv7z28a5rczB_k8TJsbOWYD3E.js](https://www.ecologie.gouv.fr/sites/default/files/js/js_k1Q9llQIQyiQ0PsBqGlv7z28a5rczB_k8TJsbOWYD3E.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v3.4.1`
  
  
  
  
Instances: 2
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p></p>
  
### Reference
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/filter/tips](https://www.ecologie.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/admin/](https://www.ecologie.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/admin/](https://www.ecologie.gouv.fr/index.php/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.svg](https://www.ecologie.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.svg](https://www.ecologie.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/node/add/](https://www.ecologie.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.js$](https://www.ecologie.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/recherche" method="get" id="solr-query-form" accept-charset="UTF-8">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "edit-query" "edit-url" "form_build_id" "form_id" "honeypot_time" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/user/login/](https://www.ecologie.gouv.fr/index.php/user/login/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/user/logout/](https://www.ecologie.gouv.fr/user/logout/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/user/password/](https://www.ecologie.gouv.fr/index.php/user/password/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/user/register/](https://www.ecologie.gouv.fr/index.php/user/register/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/user/password/](https://www.ecologie.gouv.fr/user/password/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/user/logout/](https://www.ecologie.gouv.fr/index.php/user/logout/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/filter/tips](https://www.ecologie.gouv.fr/index.php/filter/tips)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/user/login/](https://www.ecologie.gouv.fr/user/login/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/user/register/](https://www.ecologie.gouv.fr/user/register/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 39 [https://www.ecologie.gouv.fr/user/login].</p><p>Predicted response size: 339.</p><p>Response Body Length: 400.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/presse](https://www.ecologie.gouv.fr/presse)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/politiques-publiques](https://www.ecologie.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/jnqa](https://www.ecologie.gouv.fr/jnqa)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/ministere](https://www.ecologie.gouv.fr/ministere)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/congres-uicn/presentation](https://www.ecologie.gouv.fr/congres-uicn/presentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/a-la-une](https://www.ecologie.gouv.fr/a-la-une)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js`
  
  
  * Evidence: `<script src="https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/flux-rss-du-ministere-transition-ecologique](https://www.ecologie.gouv.fr/flux-rss-du-ministere-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/demarches](https://www.ecologie.gouv.fr/demarches)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/covid-19-actions-engagees-ministere](https://www.ecologie.gouv.fr/covid-19-actions-engagees-ministere)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/a-la-une](https://www.ecologie.gouv.fr/a-la-une)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js`
  
  
  * Evidence: `<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.1/Chart.min.js"></script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/js/js_k1Q9llQIQyiQ0PsBqGlv7z28a5rczB_k8TJsbOWYD3E.js](https://www.ecologie.gouv.fr/sites/default/files/js/js_k1Q9llQIQyiQ0PsBqGlv7z28a5rczB_k8TJsbOWYD3E.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/js/js_x-rGi6VZta-h_25NgKXTWomMli4rdvWXfp7H4jjljWA.js](https://www.ecologie.gouv.fr/sites/default/files/js/js_x-rGi6VZta-h_25NgKXTWomMli4rdvWXfp7H4jjljWA.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/filter/tips](https://www.ecologie.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/README.txt](https://www.ecologie.gouv.fr/README.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/robots.txt](https://www.ecologie.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sitemap.xml](https://www.ecologie.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/demarches](https://www.ecologie.gouv.fr/demarches)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/a-la-une](https://www.ecologie.gouv.fr/a-la-une)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/jnqa](https://www.ecologie.gouv.fr/jnqa)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/presse](https://www.ecologie.gouv.fr/presse)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/politiques-publiques](https://www.ecologie.gouv.fr/politiques-publiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/ministere](https://www.ecologie.gouv.fr/ministere)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpg](https://www.ecologie.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.svg](https://www.ecologie.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.png](https://www.ecologie.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js](https://www.ecologie.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpeg](https://www.ecologie.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css](https://www.ecologie.gouv.fr/profiles/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css](https://www.ecologie.gouv.fr/core/*.css)
  
  
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

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/a-la-une](https://www.ecologie.gouv.fr/a-la-une)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://vigilance.meteofrance.com/data/QGFR09_LFPW_.gif`
  
  
  
  
Instances: 1
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://vigilance.meteofrance.com/data/QGFR09_LFPW_.gif</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/sitemap.xml](https://www.ecologie.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css](https://www.ecologie.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js](https://www.ecologie.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpg](https://www.ecologie.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/robots.txt](https://www.ecologie.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpeg](https://www.ecologie.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.png](https://www.ecologie.gouv.fr/core/*.png)
  
  
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

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/js/js_dogvnIOKSYeKfpLUIok2L3XJdRxH-GjUSg0PMpf0hmo.js](https://www.ecologie.gouv.fr/sites/default/files/js/js_dogvnIOKSYeKfpLUIok2L3XJdRxH-GjUSg0PMpf0hmo.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/robots.txt](https://www.ecologie.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_3Al8on6Cv63AEdyFPOKA3_j4397HlbIY3Y5J21A_87w.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_3Al8on6Cv63AEdyFPOKA3_j4397HlbIY3Y5J21A_87w.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js](https://www.ecologie.gouv.fr/sites/default/files/js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_KifzRiC6i7Xl8w8G3yfZwMZSQQc7NvTBH132oplh1ro.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_KifzRiC6i7Xl8w8G3yfZwMZSQQc7NvTBH132oplh1ro.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/themes/custom/meem/medias/search.svg](https://www.ecologie.gouv.fr/themes/custom/meem/medias/search.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/styles/thumb_330/public/pjl_climat-resilience_actusite_810x540_Ville.jpg?itok=KPaVTK25](https://www.ecologie.gouv.fr/sites/default/files/styles/thumb_330/public/pjl_climat-resilience_actusite_810x540_Ville.jpg?itok=KPaVTK25)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/README.txt](https://www.ecologie.gouv.fr/README.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/styles/thumb_330/public/OBR000463-sauterelle.jpg?itok=6aDdR06a](https://www.ecologie.gouv.fr/sites/default/files/styles/thumb_330/public/OBR000463-sauterelle.jpg?itok=6aDdR06a)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/themes/custom/meem/medias/favicon.png](https://www.ecologie.gouv.fr/themes/custom/meem/medias/favicon.png)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/node/add/](https://www.ecologie.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.svg](https://www.ecologie.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/filter/tips](https://www.ecologie.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.svg](https://www.ecologie.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.js$](https://www.ecologie.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/admin/](https://www.ecologie.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/admin/](https://www.ecologie.gouv.fr/index.php/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `zgQcCBnafU0iVW8z9_b6lL6cS2-a0ODqLPDxyFqU3Ig`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�\x0004\x001c\x0008\x0019�}M"Uo3������Ko����,���Z�܈</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.css$](https://www.ecologie.gouv.fr/profiles/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/index.php/admin/](https://www.ecologie.gouv.fr/index.php/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.svg](https://www.ecologie.gouv.fr/profiles/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/admin/](https://www.ecologie.gouv.fr/admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/profiles/*.js$](https://www.ecologie.gouv.fr/profiles/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/filter/tips](https://www.ecologie.gouv.fr/filter/tips)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.svg](https://www.ecologie.gouv.fr/core/*.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/node/add/](https://www.ecologie.gouv.fr/node/add/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script type="application/json" data-drupal-selector="drupal-settings-json">{"path":{"baseUrl":"\/","scriptPath":null,"pathPrefi", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/inscription-nouvelles-ecologie](https://www.ecologie.gouv.fr/inscription-nouvelles-ecologie)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/flux-rss-du-ministere-transition-ecologique](https://www.ecologie.gouv.fr/flux-rss-du-ministere-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/loi-climat-resilience](https://www.ecologie.gouv.fr/loi-climat-resilience)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/loi-anti-gaspillage-economie-circulaire-1](https://www.ecologie.gouv.fr/loi-anti-gaspillage-economie-circulaire-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/france-relance-transition-ecologique](https://www.ecologie.gouv.fr/france-relance-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/biodiversite-presentation-et-informations-cles](https://www.ecologie.gouv.fr/biodiversite-presentation-et-informations-cles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/decouvrez-programme-du-pavillon-france-et-des-egn](https://www.ecologie.gouv.fr/decouvrez-programme-du-pavillon-france-et-des-egn)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/pluie-et-inondation](https://www.ecologie.gouv.fr/pluie-et-inondation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share"
           target="_self"
           href="/en/rain-and-flooding"
           class="mte-3r-social-share-link icon-before svg-link"
           aria-label="English version"
           title="English version (Ouvrir dans une nouvelle fenêtre)"></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/covid-19-actions-engagees-ministere](https://www.ecologie.gouv.fr/covid-19-actions-engagees-ministere)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/agence-innovation-transports](https://www.ecologie.gouv.fr/agence-innovation-transports)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/cigeo-enquete-publique-relative-declaration-dutilite-publique](https://www.ecologie.gouv.fr/cigeo-enquete-publique-relative-declaration-dutilite-publique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/apic-et-vigicrues-flash-evoluent](https://www.ecologie.gouv.fr/apic-et-vigicrues-flash-evoluent)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-action="share" target="_self" href="" class="svg-link" title="Imprimer (Ouvrir dans une nouvelle fenêtre)"> <span>Imprimer</span></a>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpg](https://www.ecologie.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js](https://www.ecologie.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.png](https://www.ecologie.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpeg](https://www.ecologie.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css](https://www.ecologie.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js](https://www.ecologie.gouv.fr/core/*.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.js$](https://www.ecologie.gouv.fr/core/*.js$)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css$](https://www.ecologie.gouv.fr/core/*.css$)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/robots.txt](https://www.ecologie.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpg](https://www.ecologie.gouv.fr/core/*.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.css](https://www.ecologie.gouv.fr/core/*.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sitemap.xml](https://www.ecologie.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.png](https://www.ecologie.gouv.fr/core/*.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.gif](https://www.ecologie.gouv.fr/core/*.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.jpeg](https://www.ecologie.gouv.fr/core/*.jpeg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/sitemap.xml](https://www.ecologie.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/core/*.gif](https://www.ecologie.gouv.fr/core/*.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/robots.txt](https://www.ecologie.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/](https://www.ecologie.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
Instances: 4
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483646`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483645`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_prA0LNa6F146uEHAsuzF4f7AQQOJlIw0pKrWH2WYe-w.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483644`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/a-la-une](https://www.ecologie.gouv.fr/a-la-une)
  
  
  * Method: `GET`
  
  
  * Evidence: `601799667`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sitemap.xml](https://www.ecologie.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `05022020`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/france-relance-transition-ecologique](https://www.ecologie.gouv.fr/france-relance-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `04092020`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `56656456`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css](https://www.ecologie.gouv.fr/sites/default/files/css/css_-GjoukHo289nwerPYI8F9dzLSd6FADVj0fQZlsvQjdM.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483645`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>2147483647, which evaluates to: 2038-01-19 03:14:07</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=wtwtqoOoL2QOIKcMyew3QTnaGmtPDXTY2xcxUQ5bLic&query=ZAP&url=https%3A%2F%2Fwww.example.com](https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=wtwtqoOoL2QOIKcMyew3QTnaGmtPDXTY2xcxUQ5bLic&query=ZAP&url=https%3A%2F%2Fwww.example.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `query`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=4-blFais7TTJkSLsYn1vkRI97n5FQfT4qNNLTf3CXb0&query=ZAP&url=https%3A%2F%2Fwww.example.com](https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=4-blFais7TTJkSLsYn1vkRI97n5FQfT4qNNLTf3CXb0&query=ZAP&url=https%3A%2F%2Fwww.example.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `query`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=wtwtqoOoL2QOIKcMyew3QTnaGmtPDXTY2xcxUQ5bLic&query=ZAP&url=https%3A%2F%2Fwww.example.com](https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=wtwtqoOoL2QOIKcMyew3QTnaGmtPDXTY2xcxUQ5bLic&query=ZAP&url=https%3A%2F%2Fwww.example.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `form_id`
  
  
  
  
* URL: [https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=4-blFais7TTJkSLsYn1vkRI97n5FQfT4qNNLTf3CXb0&query=ZAP&url=https%3A%2F%2Fwww.example.com](https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=4-blFais7TTJkSLsYn1vkRI97n5FQfT4qNNLTf3CXb0&query=ZAP&url=https%3A%2F%2Fwww.example.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `form_id`
  
  
  
  
Instances: 4
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.ecologie.gouv.fr/recherche?form_build_id&form_id=solr_query_form&honeypot_time=wtwtqoOoL2QOIKcMyew3QTnaGmtPDXTY2xcxUQ5bLic&query=ZAP&url=https%3A%2F%2Fwww.example.com</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>query=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

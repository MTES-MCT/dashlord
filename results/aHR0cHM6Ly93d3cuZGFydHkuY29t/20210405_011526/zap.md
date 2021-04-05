
# ZAP Scanning Report

Generated on Mon, 5 Apr 2021 01:11:16


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 7 |
| Low | 14 |
| Informational | 13 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 2 | 
| Content Security Policy (CSP) Header Not Set | Medium | 12 | 
| CSP: Wildcard Directive | Medium | 2 | 
| Reverse Tabnabbing | Medium | 11 | 
| Secure Pages Include Mixed Content (Including Scripts) | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Vulnerable JS Library | Medium | 3 | 
| X-Frame-Options Header Not Set | Medium | 12 | 
| Absence of Anti-CSRF Tokens | Low | 13 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 1 | 
| Cookie No HttpOnly Flag | Low | 10 | 
| Cookie Without SameSite Attribute | Low | 10 | 
| Cookie Without Secure Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 12 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 12 | 
| Secure Pages Include Mixed Content | Low | 2 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 12 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 12 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Charset Mismatch (Header Versus Meta Content-Type Charset) | Informational | 12 | 
| Content-Type Header Missing | Informational | 12 | 
| Cookie Poisoning | Informational | 1 | 
| Information Disclosure - Sensitive Information in URL | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Loosely Scoped Cookie | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 11 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 6 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.darty.com/res3/pdf/marketplace/cgv_cgu_marketplace_darty.pdf](https://www.darty.com/res3/pdf/marketplace/cgv_cgu_marketplace_darty.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `579544533615488`
  
  
  
  
* URL: [https://www.darty.com/res3/pdf/marketplace/cgv_cgu_marketplace_darty.pdf](https://www.darty.com/res3/pdf/marketplace/cgv_cgu_marketplace_darty.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `5005001000722`
  
  
  
  
Instances: 2
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 579544</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.darty.com/*basket_add](https://www.darty.com/*basket_add)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/list](https://www.darty.com/*extra/list)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*basket_update](https://www.darty.com/*basket_update)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/ajax/](https://www.darty.com/*extra/ajax/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/services](https://www.darty.com/*extra/services)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/jserror](https://www.darty.com/nav/extra/jserror)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*fa$](https://www.darty.com/*fa$)
  
  
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

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>script-src, script-src-elem, script-src-attr, style-src, style-src-elem, style-src-attr, img-src, connect-src, frame-src, font-src, media-src, object-src, manifest-src, worker-src, prefetch-src, form-action</p><p></p><p>The directive(s): form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `frame-ancestors 'self'`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `frame-ancestors 'self'`
  
  
  
  
Instances: 2
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="//www.36000solutions.com/questions" target="_blank">FORUM</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html](https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/se-divertir/index.html](https://www.darty.com/achat/boutique/evenement/se-divertir/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/offres/bons-plans-informatique](https://www.darty.com/offres/bons-plans-informatique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/services/services-darty/index.html](https://www.darty.com/achat/services/services-darty/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target='_blank' title='Communauté SAV Darty (nouvelle fenêtre)' href='https://sav.darty.com/#dartyclic=X_comm'>Communauté SAV</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Secure Pages Include Mixed Content (Including Scripts)
##### Medium (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.darty.com/achat/securite/mot-de-passe/index.html](https://www.darty.com/achat/securite/mot-de-passe/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js`
  
  
  
  
Instances: 1
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=script src=http://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://ajax.googleapis.com">`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" media="only screen and (max-width: 640px)" href="https://m.darty.com"/>`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" href="android-app://com.darty.android.tablette/darty/home" />`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" media="only screen and (max-width: 640px)" href="https://m.darty.com"/>`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="alternate" href="android-app://com.darty.android.tablette/darty/home" />`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.googleapis.com">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.googleapis.com">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://cdn.cookielaw.org/scripttemplates/otSDKStub.js" data-domain-script="23aa55cf-1d2a-4f9e-9612-56a8b9d14b5d" data-document-language="true"></script>`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com">`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://cdn.cookielaw.org/scripttemplates/otSDKStub.js" data-domain-script="23aa55cf-1d2a-4f9e-9612-56a8b9d14b5d" data-document-language="true"></script>`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://ajax.googleapis.com">`
  
  
  
  
Instances: 12
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 1.7.1 is vulnerable.</p>
  
  
  
* URL: [https://www.darty.com/static/8HLl/wro/desktop_common.pack.js](https://www.darty.com/static/8HLl/wro/desktop_common.pack.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `,jquery:"1.7.1"`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-ui-1.8.17.custom.min.js](https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-ui-1.8.17.custom.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*!
 * jQuery UI 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI
 */(function(a,b){function d(b){return!a(b).parents().andSelf().filter(function(){return a.curCSS(this,"visibility")==="hidden"||a.expr.filters.hidden(this)}).length}function c(b,c){var e=b.nodeName.toLowerCase();if("area"===e){var f=b.parentNode,g=f.name,h;if(!b.href||!g||f.nodeName.toLowerCase()!=="map")return!1;h=a("img[usemap=#"+g+"]")[0];return!!h&&d(h)}return(/input|select|textarea|button|object/.test(e)?!b.disabled:"a"==e?b.href||c:c)&&d(b)}a.ui=a.ui||{};a.ui.version||(a.extend(a.ui,{version:"1.8.17",keyCode:{ALT:18,BACKSPACE:8,CAPS_LOCK:20,COMMA:188,COMMAND:91,COMMAND_LEFT:91,COMMAND_RIGHT:93,CONTROL:17,DELETE:46,DOWN:40,END:35,ENTER:13,ESCAPE:27,HOME:36,INSERT:45,LEFT:37,MENU:93,NUMPAD_ADD:107,NUMPAD_DECIMAL:110,NUMPAD_DIVIDE:111,NUMPAD_ENTER:108,NUMPAD_MULTIPLY:106,NUMPAD_SUBTRACT:109,PAGE_DOWN:34,PAGE_UP:33,PERIOD:190,RIGHT:39,SHIFT:16,SPACE:32,TAB:9,UP:38,WINDOWS:91}}),a.fn.extend({propAttr:a.fn.prop||a.fn.attr,_focus:a.fn.focus,focus:function(b,c){return typeof b=="number"?this.each(function(){var d=this;setTimeout(function(){a(d).focus(),c&&c.call(d)},b)}):this._focus.apply(this,arguments)},scrollParent:function(){var b;a.browser.msie&&/(static|relative)/.test(this.css("position"))||/absolute/.test(this.css("position"))?b=this.parents().filter(function(){return/(relative|absolute|fixed)/.test(a.curCSS(this,"position",1))&&/(auto|scroll)/.test(a.curCSS(this,"overflow",1)+a.curCSS(this,"overflow-y",1)+a.curCSS(this,"overflow-x",1))}).eq(0):b=this.parents().filter(function(){return/(auto|scroll)/.test(a.curCSS(this,"overflow",1)+a.curCSS(this,"overflow-y",1)+a.curCSS(this,"overflow-x",1))}).eq(0);return/fixed/.test(this.css("position"))||!b.length?a(document):b},zIndex:function(c){if(c!==b)return this.css("zIndex",c);if(this.length){var d=a(this[0]),e,f;while(d.length&&d[0]!==document){e=d.css("position");if(e==="absolute"||e==="relative"||e==="fixed"){f=parseInt(d.css("zIndex"),10);if(!isNaN(f)&&f!==0)return f}d=d.parent()}}return 0},disableSelection:function(){return this.bind((a.support.selectstart?"selectstart":"mousedown")+".ui-disableSelection",function(a){a.preventDefault()})},enableSelection:function(){return this.unbind(".ui-disableSelection")}}),a.each(["Width","Height"],function(c,d){function h(b,c,d,f){a.each(e,function(){c-=parseFloat(a.curCSS(b,"padding"+this,!0))||0,d&&(c-=parseFloat(a.curCSS(b,"border"+this+"Width",!0))||0),f&&(c-=parseFloat(a.curCSS(b,"margin"+this,!0))||0)});return c}var e=d==="Width"?["Left","Right"]:["Top","Bottom"],f=d.toLowerCase(),g={innerWidth:a.fn.innerWidth,innerHeight:a.fn.innerHeight,outerWidth:a.fn.outerWidth,outerHeight:a.fn.outerHeight};a.fn["inner"+d]=function(c){if(c===b)return g["inner"+d].call(this);return this.each(function(){a(this).css(f,h(this,c)+"px")})},a.fn["outer"+d]=function(b,c){if(typeof b!="number")return g["outer"+d].call(this,b);return this.each(function(){a(this).css(f,h(this,b,!0,c)+"px")})}}),a.extend(a.expr[":"],{data:function(b,c,d){return!!a.data(b,d[3])},focusable:function(b){return c(b,!isNaN(a.attr(b,"tabindex")))},tabbable:function(b){var d=a.attr(b,"tabindex"),e=isNaN(d);return(e||d>=0)&&c(b,!e)}}),a(function(){var b=document.body,c=b.appendChild(c=document.createElement("div"));a.extend(c.style,{minHeight:"100px",height:"auto",padding:0,borderWidth:0}),a.support.minHeight=c.offsetHeight===100,a.support.selectstart="onselectstart"in c,b.removeChild(c).style.display="none"}),a.extend(a.ui,{plugin:{add:function(b,c,d){var e=a.ui[b].prototype;for(var f in d)e.plugins[f]=e.plugins[f]||[],e.plugins[f].push([c,d[f]])},call:function(a,b,c){var d=a.plugins[b];if(!!d&&!!a.element[0].parentNode)for(var e=0;e<d.length;e++)a.options[d[e][0]]&&d[e][1].apply(a.element,c)}},contains:function(a,b){return document.compareDocumentPosition?a.compareDocumentPosition(b)&16:a!==b&&a.contains(b)},hasScroll:function(b,c){if(a(b).css("overflow")==="hidden")return!1;var d=c&&c==="left"?"scrollLeft":"scrollTop",e=!1;if(b[d]>0)return!0;b[d]=1,e=b[d]>0,b[d]=0;return e},isOverAxis:function(a,b,c){return a>b&&a<b+c},isOver:function(b,c,d,e,f,g){return a.ui.isOverAxis(b,d,f)&&a.ui.isOverAxis(c,e,g)}}))})(jQuery);/*!
 * jQuery UI Widget 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Widget
 */(function(a,b){if(a.cleanData){var c=a.cleanData;a.cleanData=function(b){for(var d=0,e;(e=b[d])!=null;d++)try{a(e).triggerHandler("remove")}catch(f){}c(b)}}else{var d=a.fn.remove;a.fn.remove=function(b,c){return this.each(function(){c||(!b||a.filter(b,[this]).length)&&a("*",this).add([this]).each(function(){try{a(this).triggerHandler("remove")}catch(b){}});return d.call(a(this),b,c)})}}a.widget=function(b,c,d){var e=b.split(".")[0],f;b=b.split(".")[1],f=e+"-"+b,d||(d=c,c=a.Widget),a.expr[":"][f]=function(c){return!!a.data(c,b)},a[e]=a[e]||{},a[e][b]=function(a,b){arguments.length&&this._createWidget(a,b)};var g=new c;g.options=a.extend(!0,{},g.options),a[e][b].prototype=a.extend(!0,g,{namespace:e,widgetName:b,widgetEventPrefix:a[e][b].prototype.widgetEventPrefix||b,widgetBaseClass:f},d),a.widget.bridge(b,a[e][b])},a.widget.bridge=function(c,d){a.fn[c]=function(e){var f=typeof e=="string",g=Array.prototype.slice.call(arguments,1),h=this;e=!f&&g.length?a.extend.apply(null,[!0,e].concat(g)):e;if(f&&e.charAt(0)==="_")return h;f?this.each(function(){var d=a.data(this,c),f=d&&a.isFunction(d[e])?d[e].apply(d,g):d;if(f!==d&&f!==b){h=f;return!1}}):this.each(function(){var b=a.data(this,c);b?b.option(e||{})._init():a.data(this,c,new d(e,this))});return h}},a.Widget=function(a,b){arguments.length&&this._createWidget(a,b)},a.Widget.prototype={widgetName:"widget",widgetEventPrefix:"",options:{disabled:!1},_createWidget:function(b,c){a.data(c,this.widgetName,this),this.element=a(c),this.options=a.extend(!0,{},this.options,this._getCreateOptions(),b);var d=this;this.element.bind("remove."+this.widgetName,function(){d.destroy()}),this._create(),this._trigger("create"),this._init()},_getCreateOptions:function(){return a.metadata&&a.metadata.get(this.element[0])[this.widgetName]},_create:function(){},_init:function(){},destroy:function(){this.element.unbind("."+this.widgetName).removeData(this.widgetName),this.widget().unbind("."+this.widgetName).removeAttr("aria-disabled").removeClass(this.widgetBaseClass+"-disabled "+"ui-state-disabled")},widget:function(){return this.element},option:function(c,d){var e=c;if(arguments.length===0)return a.extend({},this.options);if(typeof c=="string"){if(d===b)return this.options[c];e={},e[c]=d}this._setOptions(e);return this},_setOptions:function(b){var c=this;a.each(b,function(a,b){c._setOption(a,b)});return this},_setOption:function(a,b){this.options[a]=b,a==="disabled"&&this.widget()[b?"addClass":"removeClass"](this.widgetBaseClass+"-disabled"+" "+"ui-state-disabled").attr("aria-disabled",b);return this},enable:function(){return this._setOption("disabled",!1)},disable:function(){return this._setOption("disabled",!0)},_trigger:function(b,c,d){var e,f,g=this.options[b];d=d||{},c=a.Event(c),c.type=(b===this.widgetEventPrefix?b:this.widgetEventPrefix+b).toLowerCase(),c.target=this.element[0],f=c.originalEvent;if(f)for(e in f)e in c||(c[e]=f[e]);this.element.trigger(c,d);return!(a.isFunction(g)&&g.call(this.element[0],c,d)===!1||c.isDefaultPrevented())}}})(jQuery);/*!
 * jQuery UI Mouse 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Mouse
 *
 * Depends:
 *    jquery.ui.widget.js
 */(function(a,b){var c=!1;a(document).mouseup(function(a){c=!1}),a.widget("ui.mouse",{options:{cancel:":input,option",distance:1,delay:0},_mouseInit:function(){var b=this;this.element.bind("mousedown."+this.widgetName,function(a){return b._mouseDown(a)}).bind("click."+this.widgetName,function(c){if(!0===a.data(c.target,b.widgetName+".preventClickEvent")){a.removeData(c.target,b.widgetName+".preventClickEvent"),c.stopImmediatePropagation();return!1}}),this.started=!1},_mouseDestroy:function(){this.element.unbind("."+this.widgetName)},_mouseDown:function(b){if(!c){this._mouseStarted&&this._mouseUp(b),this._mouseDownEvent=b;var d=this,e=b.which==1,f=typeof this.options.cancel=="string"&&b.target.nodeName?a(b.target).closest(this.options.cancel).length:!1;if(!e||f||!this._mouseCapture(b))return!0;this.mouseDelayMet=!this.options.delay,this.mouseDelayMet||(this._mouseDelayTimer=setTimeout(function(){d.mouseDelayMet=!0},this.options.delay));if(this._mouseDistanceMet(b)&&this._mouseDelayMet(b)){this._mouseStarted=this._mouseStart(b)!==!1;if(!this._mouseStarted){b.preventDefault();return!0}}!0===a.data(b.target,this.widgetName+".preventClickEvent")&&a.removeData(b.target,this.widgetName+".preventClickEvent"),this._mouseMoveDelegate=function(a){return d._mouseMove(a)},this._mouseUpDelegate=function(a){return d._mouseUp(a)},a(document).bind("mousemove."+this.widgetName,this._mouseMoveDelegate).bind("mouseup."+this.widgetName,this._mouseUpDelegate),b.preventDefault(),c=!0;return!0}},_mouseMove:function(b){if(a.browser.msie&&!(document.documentMode>=9)&&!b.button)return this._mouseUp(b);if(this._mouseStarted){this._mouseDrag(b);return b.preventDefault()}this._mouseDistanceMet(b)&&this._mouseDelayMet(b)&&(this._mouseStarted=this._mouseStart(this._mouseDownEvent,b)!==!1,this._mouseStarted?this._mouseDrag(b):this._mouseUp(b));return!this._mouseStarted},_mouseUp:function(b){a(document).unbind("mousemove."+this.widgetName,this._mouseMoveDelegate).unbind("mouseup."+this.widgetName,this._mouseUpDelegate),this._mouseStarted&&(this._mouseStarted=!1,b.target==this._mouseDownEvent.target&&a.data(b.target,this.widgetName+".preventClickEvent",!0),this._mouseStop(b));return!1},_mouseDistanceMet:function(a){return Math.max(Math.abs(this._mouseDownEvent.pageX-a.pageX),Math.abs(this._mouseDownEvent.pageY-a.pageY))>=this.options.distance},_mouseDelayMet:function(a){return this.mouseDelayMet},_mouseStart:function(a){},_mouseDrag:function(a){},_mouseStop:function(a){},_mouseCapture:function(a){return!0}})})(jQuery);/*
 * jQuery UI Position 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Position
 */(function(a,b){a.ui=a.ui||{};var c=/left|center|right/,d=/top|center|bottom/,e="center",f={},g=a.fn.position,h=a.fn.offset;a.fn.position=function(b){if(!b||!b.of)return g.apply(this,arguments);b=a.extend({},b);var h=a(b.of),i=h[0],j=(b.collision||"flip").split(" "),k=b.offset?b.offset.split(" "):[0,0],l,m,n;i.nodeType===9?(l=h.width(),m=h.height(),n={top:0,left:0}):i.setTimeout?(l=h.width(),m=h.height(),n={top:h.scrollTop(),left:h.scrollLeft()}):i.preventDefault?(b.at="left top",l=m=0,n={top:b.of.pageY,left:b.of.pageX}):(l=h.outerWidth(),m=h.outerHeight(),n=h.offset()),a.each(["my","at"],function(){var a=(b[this]||"").split(" ");a.length===1&&(a=c.test(a[0])?a.concat([e]):d.test(a[0])?[e].concat(a):[e,e]),a[0]=c.test(a[0])?a[0]:e,a[1]=d.test(a[1])?a[1]:e,b[this]=a}),j.length===1&&(j[1]=j[0]),k[0]=parseInt(k[0],10)||0,k.length===1&&(k[1]=k[0]),k[1]=parseInt(k[1],10)||0,b.at[0]==="right"?n.left+=l:b.at[0]===e&&(n.left+=l/2),b.at[1]==="bottom"?n.top+=m:b.at[1]===e&&(n.top+=m/2),n.left+=k[0],n.top+=k[1];return this.each(function(){var c=a(this),d=c.outerWidth(),g=c.outerHeight(),h=parseInt(a.curCSS(this,"marginLeft",!0))||0,i=parseInt(a.curCSS(this,"marginTop",!0))||0,o=d+h+(parseInt(a.curCSS(this,"marginRight",!0))||0),p=g+i+(parseInt(a.curCSS(this,"marginBottom",!0))||0),q=a.extend({},n),r;b.my[0]==="right"?q.left-=d:b.my[0]===e&&(q.left-=d/2),b.my[1]==="bottom"?q.top-=g:b.my[1]===e&&(q.top-=g/2),f.fractions||(q.left=Math.round(q.left),q.top=Math.round(q.top)),r={left:q.left-h,top:q.top-i},a.each(["left","top"],function(c,e){a.ui.position[j[c]]&&a.ui.position[j[c]][e](q,{targetWidth:l,targetHeight:m,elemWidth:d,elemHeight:g,collisionPosition:r,collisionWidth:o,collisionHeight:p,offset:k,my:b.my,at:b.at})}),a.fn.bgiframe&&c.bgiframe(),c.offset(a.extend(q,{using:b.using}))})},a.ui.position={fit:{left:function(b,c){var d=a(window),e=c.collisionPosition.left+c.collisionWidth-d.width()-d.scrollLeft();b.left=e>0?b.left-e:Math.max(b.left-c.collisionPosition.left,b.left)},top:function(b,c){var d=a(window),e=c.collisionPosition.top+c.collisionHeight-d.height()-d.scrollTop();b.top=e>0?b.top-e:Math.max(b.top-c.collisionPosition.top,b.top)}},flip:{left:function(b,c){if(c.at[0]!==e){var d=a(window),f=c.collisionPosition.left+c.collisionWidth-d.width()-d.scrollLeft(),g=c.my[0]==="left"?-c.elemWidth:c.my[0]==="right"?c.elemWidth:0,h=c.at[0]==="left"?c.targetWidth:-c.targetWidth,i=-2*c.offset[0];b.left+=c.collisionPosition.left<0?g+h+i:f>0?g+h+i:0}},top:function(b,c){if(c.at[1]!==e){var d=a(window),f=c.collisionPosition.top+c.collisionHeight-d.height()-d.scrollTop(),g=c.my[1]==="top"?-c.elemHeight:c.my[1]==="bottom"?c.elemHeight:0,h=c.at[1]==="top"?c.targetHeight:-c.targetHeight,i=-2*c.offset[1];b.top+=c.collisionPosition.top<0?g+h+i:f>0?g+h+i:0}}}},a.offset.setOffset||(a.offset.setOffset=function(b,c){/static/.test(a.curCSS(b,"position"))&&(b.style.position="relative");var d=a(b),e=d.offset(),f=parseInt(a.curCSS(b,"top",!0),10)||0,g=parseInt(a.curCSS(b,"left",!0),10)||0,h={top:c.top-e.top+f,left:c.left-e.left+g};"using"in c?c.using.call(b,h):d.css(h)},a.fn.offset=function(b){var c=this[0];if(!c||!c.ownerDocument)return null;if(b)return this.each(function(){a.offset.setOffset(this,b)});return h.call(this)}),function(){var b=document.getElementsByTagName("body")[0],c=document.createElement("div"),d,e,g,h,i;d=document.createElement(b?"div":"body"),g={visibility:"hidden",width:0,height:0,border:0,margin:0,background:"none"},b&&jQuery.extend(g,{position:"absolute",left:"-1000px",top:"-1000px"});for(var j in g)d.style[j]=g[j];d.appendChild(c),e=b||document.documentElement,e.insertBefore(d,e.firstChild),c.style.cssText="position: absolute; left: 10.7432222px; top: 10.432325px; height: 30px; width: 201px;",h=a(c).offset(function(a,b){return b}).offset(),d.innerHTML="",e.removeChild(d),i=h.top+h.left+(b?2e3:0),f.fractions=i>21&&i<22}()})(jQuery);/*
 * jQuery UI Draggable 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Draggables
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.mouse.js
 *    jquery.ui.widget.js
 */(function(a,b){a.widget("ui.draggable",a.ui.mouse,{widgetEventPrefix:"drag",options:{addClasses:!0,appendTo:"parent",axis:!1,connectToSortable:!1,containment:!1,cursor:"auto",cursorAt:!1,grid:!1,handle:!1,helper:"original",iframeFix:!1,opacity:!1,refreshPositions:!1,revert:!1,revertDuration:500,scope:"default",scroll:!0,scrollSensitivity:20,scrollSpeed:20,snap:!1,snapMode:"both",snapTolerance:20,stack:!1,zIndex:!1},_create:function(){this.options.helper=="original"&&!/^(?:r|a|f)/.test(this.element.css("position"))&&(this.element[0].style.position="relative"),this.options.addClasses&&this.element.addClass("ui-draggable"),this.options.disabled&&this.element.addClass("ui-draggable-disabled"),this._mouseInit()},destroy:function(){if(!!this.element.data("draggable")){this.element.removeData("draggable").unbind(".draggable").removeClass("ui-draggable ui-draggable-dragging ui-draggable-disabled"),this._mouseDestroy();return this}},_mouseCapture:function(b){var c=this.options;if(this.helper||c.disabled||a(b.target).is(".ui-resizable-handle"))return!1;this.handle=this._getHandle(b);if(!this.handle)return!1;c.iframeFix&&a(c.iframeFix===!0?"iframe":c.iframeFix).each(function(){a('<div class="ui-draggable-iframeFix" style="background: #fff;"></div>').css({width:this.offsetWidth+"px",height:this.offsetHeight+"px",position:"absolute",opacity:"0.001",zIndex:1e3}).css(a(this).offset()).appendTo("body")});return!0},_mouseStart:function(b){var c=this.options;this.helper=this._createHelper(b),this._cacheHelperProportions(),a.ui.ddmanager&&(a.ui.ddmanager.current=this),this._cacheMargins(),this.cssPosition=this.helper.css("position"),this.scrollParent=this.helper.scrollParent(),this.offset=this.positionAbs=this.element.offset(),this.offset={top:this.offset.top-this.margins.top,left:this.offset.left-this.margins.left},a.extend(this.offset,{click:{left:b.pageX-this.offset.left,top:b.pageY-this.offset.top},parent:this._getParentOffset(),relative:this._getRelativeOffset()}),this.originalPosition=this.position=this._generatePosition(b),this.originalPageX=b.pageX,this.originalPageY=b.pageY,c.cursorAt&&this._adjustOffsetFromHelper(c.cursorAt),c.containment&&this._setContainment();if(this._trigger("start",b)===!1){this._clear();return!1}this._cacheHelperProportions(),a.ui.ddmanager&&!c.dropBehaviour&&a.ui.ddmanager.prepareOffsets(this,b),this.helper.addClass("ui-draggable-dragging"),this._mouseDrag(b,!0),a.ui.ddmanager&&a.ui.ddmanager.dragStart(this,b);return!0},_mouseDrag:function(b,c){this.position=this._generatePosition(b),this.positionAbs=this._convertPositionTo("absolute");if(!c){var d=this._uiHash();if(this._trigger("drag",b,d)===!1){this._mouseUp({});return!1}this.position=d.position}if(!this.options.axis||this.options.axis!="y")this.helper[0].style.left=this.position.left+"px";if(!this.options.axis||this.options.axis!="x")this.helper[0].style.top=this.position.top+"px";a.ui.ddmanager&&a.ui.ddmanager.drag(this,b);return!1},_mouseStop:function(b){var c=!1;a.ui.ddmanager&&!this.options.dropBehaviour&&(c=a.ui.ddmanager.drop(this,b)),this.dropped&&(c=this.dropped,this.dropped=!1);if((!this.element[0]||!this.element[0].parentNode)&&this.options.helper=="original")return!1;if(this.options.revert=="invalid"&&!c||this.options.revert=="valid"&&c||this.options.revert===!0||a.isFunction(this.options.revert)&&this.options.revert.call(this.element,c)){var d=this;a(this.helper).animate(this.originalPosition,parseInt(this.options.revertDuration,10),function(){d._trigger("stop",b)!==!1&&d._clear()})}else this._trigger("stop",b)!==!1&&this._clear();return!1},_mouseUp:function(b){this.options.iframeFix===!0&&a("div.ui-draggable-iframeFix").each(function(){this.parentNode.removeChild(this)}),a.ui.ddmanager&&a.ui.ddmanager.dragStop(this,b);return a.ui.mouse.prototype._mouseUp.call(this,b)},cancel:function(){this.helper.is(".ui-draggable-dragging")?this._mouseUp({}):this._clear();return this},_getHandle:function(b){var c=!this.options.handle||!a(this.options.handle,this.element).length?!0:!1;a(this.options.handle,this.element).find("*").andSelf().each(function(){this==b.target&&(c=!0)});return c},_createHelper:function(b){var c=this.options,d=a.isFunction(c.helper)?a(c.helper.apply(this.element[0],[b])):c.helper=="clone"?this.element.clone().removeAttr("id"):this.element;d.parents("body").length||d.appendTo(c.appendTo=="parent"?this.element[0].parentNode:c.appendTo),d[0]!=this.element[0]&&!/(fixed|absolute)/.test(d.css("position"))&&d.css("position","absolute");return d},_adjustOffsetFromHelper:function(b){typeof b=="string"&&(b=b.split(" ")),a.isArray(b)&&(b={left:+b[0],top:+b[1]||0}),"left"in b&&(this.offset.click.left=b.left+this.margins.left),"right"in b&&(this.offset.click.left=this.helperProportions.width-b.right+this.margins.left),"top"in b&&(this.offset.click.top=b.top+this.margins.top),"bottom"in b&&(this.offset.click.top=this.helperProportions.height-b.bottom+this.margins.top)},_getParentOffset:function(){this.offsetParent=this.helper.offsetParent();var b=this.offsetParent.offset();this.cssPosition=="absolute"&&this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0])&&(b.left+=this.scrollParent.scrollLeft(),b.top+=this.scrollParent.scrollTop());if(this.offsetParent[0]==document.body||this.offsetParent[0].tagName&&this.offsetParent[0].tagName.toLowerCase()=="html"&&a.browser.msie)b={top:0,left:0};return{top:b.top+(parseInt(this.offsetParent.css("borderTopWidth"),10)||0),left:b.left+(parseInt(this.offsetParent.css("borderLeftWidth"),10)||0)}},_getRelativeOffset:function(){if(this.cssPosition=="relative"){var a=this.element.position();return{top:a.top-(parseInt(this.helper.css("top"),10)||0)+this.scrollParent.scrollTop(),left:a.left-(parseInt(this.helper.css("left"),10)||0)+this.scrollParent.scrollLeft()}}return{top:0,left:0}},_cacheMargins:function(){this.margins={left:parseInt(this.element.css("marginLeft"),10)||0,top:parseInt(this.element.css("marginTop"),10)||0,right:parseInt(this.element.css("marginRight"),10)||0,bottom:parseInt(this.element.css("marginBottom"),10)||0}},_cacheHelperProportions:function(){this.helperProportions={width:this.helper.outerWidth(),height:this.helper.outerHeight()}},_setContainment:function(){var b=this.options;b.containment=="parent"&&(b.containment=this.helper[0].parentNode);if(b.containment=="document"||b.containment=="window")this.containment=[b.containment=="document"?0:a(window).scrollLeft()-this.offset.relative.left-this.offset.parent.left,b.containment=="document"?0:a(window).scrollTop()-this.offset.relative.top-this.offset.parent.top,(b.containment=="document"?0:a(window).scrollLeft())+a(b.containment=="document"?document:window).width()-this.helperProportions.width-this.margins.left,(b.containment=="document"?0:a(window).scrollTop())+(a(b.containment=="document"?document:window).height()||document.body.parentNode.scrollHeight)-this.helperProportions.height-this.margins.top];if(!/^(document|window|parent)$/.test(b.containment)&&b.containment.constructor!=Array){var c=a(b.containment),d=c[0];if(!d)return;var e=c.offset(),f=a(d).css("overflow")!="hidden";this.containment=[(parseInt(a(d).css("borderLeftWidth"),10)||0)+(parseInt(a(d).css("paddingLeft"),10)||0),(parseInt(a(d).css("borderTopWidth"),10)||0)+(parseInt(a(d).css("paddingTop"),10)||0),(f?Math.max(d.scrollWidth,d.offsetWidth):d.offsetWidth)-(parseInt(a(d).css("borderLeftWidth"),10)||0)-(parseInt(a(d).css("paddingRight"),10)||0)-this.helperProportions.width-this.margins.left-this.margins.right,(f?Math.max(d.scrollHeight,d.offsetHeight):d.offsetHeight)-(parseInt(a(d).css("borderTopWidth"),10)||0)-(parseInt(a(d).css("paddingBottom"),10)||0)-this.helperProportions.height-this.margins.top-this.margins.bottom],this.relative_container=c}else b.containment.constructor==Array&&(this.containment=b.containment)},_convertPositionTo:function(b,c){c||(c=this.position);var d=b=="absolute"?1:-1,e=this.options,f=this.cssPosition=="absolute"&&(this.scrollParent[0]==document||!a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,g=/(html|body)/i.test(f[0].tagName);return{top:c.top+this.offset.relative.top*d+this.offset.parent.top*d-(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollTop():g?0:f.scrollTop())*d),left:c.left+this.offset.relative.left*d+this.offset.parent.left*d-(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():g?0:f.scrollLeft())*d)}},_generatePosition:function(b){var c=this.options,d=this.cssPosition=="absolute"&&(this.scrollParent[0]==document||!a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,e=/(html|body)/i.test(d[0].tagName),f=b.pageX,g=b.pageY;if(this.originalPosition){var h;if(this.containment){if(this.relative_container){var i=this.relative_container.offset();h=[this.containment[0]+i.left,this.containment[1]+i.top,this.containment[2]+i.left,this.containment[3]+i.top]}else h=this.containment;b.pageX-this.offset.click.left<h[0]&&(f=h[0]+this.offset.click.left),b.pageY-this.offset.click.top<h[1]&&(g=h[1]+this.offset.click.top),b.pageX-this.offset.click.left>h[2]&&(f=h[2]+this.offset.click.left),b.pageY-this.offset.click.top>h[3]&&(g=h[3]+this.offset.click.top)}if(c.grid){var j=c.grid[1]?this.originalPageY+Math.round((g-this.originalPageY)/c.grid[1])*c.grid[1]:this.originalPageY;g=h?j-this.offset.click.top<h[1]||j-this.offset.click.top>h[3]?j-this.offset.click.top<h[1]?j+c.grid[1]:j-c.grid[1]:j:j;var k=c.grid[0]?this.originalPageX+Math.round((f-this.originalPageX)/c.grid[0])*c.grid[0]:this.originalPageX;f=h?k-this.offset.click.left<h[0]||k-this.offset.click.left>h[2]?k-this.offset.click.left<h[0]?k+c.grid[0]:k-c.grid[0]:k:k}}return{top:g-this.offset.click.top-this.offset.relative.top-this.offset.parent.top+(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:this.cssPosition=="fixed"?-this.scrollParent.scrollTop():e?0:d.scrollTop()),left:f-this.offset.click.left-this.offset.relative.left-this.offset.parent.left+(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():e?0:d.scrollLeft())}},_clear:function(){this.helper.removeClass("ui-draggable-dragging"),this.helper[0]!=this.element[0]&&!this.cancelHelperRemoval&&this.helper.remove(),this.helper=null,this.cancelHelperRemoval=!1},_trigger:function(b,c,d){d=d||this._uiHash(),a.ui.plugin.call(this,b,[c,d]),b=="drag"&&(this.positionAbs=this._convertPositionTo("absolute"));return a.Widget.prototype._trigger.call(this,b,c,d)},plugins:{},_uiHash:function(a){return{helper:this.helper,position:this.position,originalPosition:this.originalPosition,offset:this.positionAbs}}}),a.extend(a.ui.draggable,{version:"1.8.17"}),a.ui.plugin.add("draggable","connectToSortable",{start:function(b,c){var d=a(this).data("draggable"),e=d.options,f=a.extend({},c,{item:d.element});d.sortables=[],a(e.connectToSortable).each(function(){var c=a.data(this,"sortable");c&&!c.options.disabled&&(d.sortables.push({instance:c,shouldRevert:c.options.revert}),c.refreshPositions(),c._trigger("activate",b,f))})},stop:function(b,c){var d=a(this).data("draggable"),e=a.extend({},c,{item:d.element});a.each(d.sortables,function(){this.instance.isOver?(this.instance.isOver=0,d.cancelHelperRemoval=!0,this.instance.cancelHelperRemoval=!1,this.shouldRevert&&(this.instance.options.revert=!0),this.instance._mouseStop(b),this.instance.options.helper=this.instance.options._helper,d.options.helper=="original"&&this.instance.currentItem.css({top:"auto",left:"auto"})):(this.instance.cancelHelperRemoval=!1,this.instance._trigger("deactivate",b,e))})},drag:function(b,c){var d=a(this).data("draggable"),e=this,f=function(b){var c=this.offset.click.top,d=this.offset.click.left,e=this.positionAbs.top,f=this.positionAbs.left,g=b.height,h=b.width,i=b.top,j=b.left;return a.ui.isOver(e+c,f+d,i,j,g,h)};a.each(d.sortables,function(f){this.instance.positionAbs=d.positionAbs,this.instance.helperProportions=d.helperProportions,this.instance.offset.click=d.offset.click,this.instance._intersectsWith(this.instance.containerCache)?(this.instance.isOver||(this.instance.isOver=1,this.instance.currentItem=a(e).clone().removeAttr("id").appendTo(this.instance.element).data("sortable-item",!0),this.instance.options._helper=this.instance.options.helper,this.instance.options.helper=function(){return c.helper[0]},b.target=this.instance.currentItem[0],this.instance._mouseCapture(b,!0),this.instance._mouseStart(b,!0,!0),this.instance.offset.click.top=d.offset.click.top,this.instance.offset.click.left=d.offset.click.left,this.instance.offset.parent.left-=d.offset.parent.left-this.instance.offset.parent.left,this.instance.offset.parent.top-=d.offset.parent.top-this.instance.offset.parent.top,d._trigger("toSortable",b),d.dropped=this.instance.element,d.currentItem=d.element,this.instance.fromOutside=d),this.instance.currentItem&&this.instance._mouseDrag(b)):this.instance.isOver&&(this.instance.isOver=0,this.instance.cancelHelperRemoval=!0,this.instance.options.revert=!1,this.instance._trigger("out",b,this.instance._uiHash(this.instance)),this.instance._mouseStop(b,!0),this.instance.options.helper=this.instance.options._helper,this.instance.currentItem.remove(),this.instance.placeholder&&this.instance.placeholder.remove(),d._trigger("fromSortable",b),d.dropped=!1)})}}),a.ui.plugin.add("draggable","cursor",{start:function(b,c){var d=a("body"),e=a(this).data("draggable").options;d.css("cursor")&&(e._cursor=d.css("cursor")),d.css("cursor",e.cursor)},stop:function(b,c){var d=a(this).data("draggable").options;d._cursor&&a("body").css("cursor",d._cursor)}}),a.ui.plugin.add("draggable","opacity",{start:function(b,c){var d=a(c.helper),e=a(this).data("draggable").options;d.css("opacity")&&(e._opacity=d.css("opacity")),d.css("opacity",e.opacity)},stop:function(b,c){var d=a(this).data("draggable").options;d._opacity&&a(c.helper).css("opacity",d._opacity)}}),a.ui.plugin.add("draggable","scroll",{start:function(b,c){var d=a(this).data("draggable");d.scrollParent[0]!=document&&d.scrollParent[0].tagName!="HTML"&&(d.overflowOffset=d.scrollParent.offset())},drag:function(b,c){var d=a(this).data("draggable"),e=d.options,f=!1;if(d.scrollParent[0]!=document&&d.scrollParent[0].tagName!="HTML"){if(!e.axis||e.axis!="x")d.overflowOffset.top+d.scrollParent[0].offsetHeight-b.pageY<e.scrollSensitivity?d.scrollParent[0].scrollTop=f=d.scrollParent[0].scrollTop+e.scrollSpeed:b.pageY-d.overflowOffset.top<e.scrollSensitivity&&(d.scrollParent[0].scrollTop=f=d.scrollParent[0].scrollTop-e.scrollSpeed);if(!e.axis||e.axis!="y")d.overflowOffset.left+d.scrollParent[0].offsetWidth-b.pageX<e.scrollSensitivity?d.scrollParent[0].scrollLeft=f=d.scrollParent[0].scrollLeft+e.scrollSpeed:b.pageX-d.overflowOffset.left<e.scrollSensitivity&&(d.scrollParent[0].scrollLeft=f=d.scrollParent[0].scrollLeft-e.scrollSpeed)}else{if(!e.axis||e.axis!="x")b.pageY-a(document).scrollTop()<e.scrollSensitivity?f=a(document).scrollTop(a(document).scrollTop()-e.scrollSpeed):a(window).height()-(b.pageY-a(document).scrollTop())<e.scrollSensitivity&&(f=a(document).scrollTop(a(document).scrollTop()+e.scrollSpeed));if(!e.axis||e.axis!="y")b.pageX-a(document).scrollLeft()<e.scrollSensitivity?f=a(document).scrollLeft(a(document).scrollLeft()-e.scrollSpeed):a(window).width()-(b.pageX-a(document).scrollLeft())<e.scrollSensitivity&&(f=a(document).scrollLeft(a(document).scrollLeft()+e.scrollSpeed))}f!==!1&&a.ui.ddmanager&&!e.dropBehaviour&&a.ui.ddmanager.prepareOffsets(d,b)}}),a.ui.plugin.add("draggable","snap",{start:function(b,c){var d=a(this).data("draggable"),e=d.options;d.snapElements=[],a(e.snap.constructor!=String?e.snap.items||":data(draggable)":e.snap).each(function(){var b=a(this),c=b.offset();this!=d.element[0]&&d.snapElements.push({item:this,width:b.outerWidth(),height:b.outerHeight(),top:c.top,left:c.left})})},drag:function(b,c){var d=a(this).data("draggable"),e=d.options,f=e.snapTolerance,g=c.offset.left,h=g+d.helperProportions.width,i=c.offset.top,j=i+d.helperProportions.height;for(var k=d.snapElements.length-1;k>=0;k--){var l=d.snapElements[k].left,m=l+d.snapElements[k].width,n=d.snapElements[k].top,o=n+d.snapElements[k].height;if(!(l-f<g&&g<m+f&&n-f<i&&i<o+f||l-f<g&&g<m+f&&n-f<j&&j<o+f||l-f<h&&h<m+f&&n-f<i&&i<o+f||l-f<h&&h<m+f&&n-f<j&&j<o+f)){d.snapElements[k].snapping&&d.options.snap.release&&d.options.snap.release.call(d.element,b,a.extend(d._uiHash(),{snapItem:d.snapElements[k].item})),d.snapElements[k].snapping=!1;continue}if(e.snapMode!="inner"){var p=Math.abs(n-j)<=f,q=Math.abs(o-i)<=f,r=Math.abs(l-h)<=f,s=Math.abs(m-g)<=f;p&&(c.position.top=d._convertPositionTo("relative",{top:n-d.helperProportions.height,left:0}).top-d.margins.top),q&&(c.position.top=d._convertPositionTo("relative",{top:o,left:0}).top-d.margins.top),r&&(c.position.left=d._convertPositionTo("relative",{top:0,left:l-d.helperProportions.width}).left-d.margins.left),s&&(c.position.left=d._convertPositionTo("relative",{top:0,left:m}).left-d.margins.left)}var t=p||q||r||s;if(e.snapMode!="outer"){var p=Math.abs(n-i)<=f,q=Math.abs(o-j)<=f,r=Math.abs(l-g)<=f,s=Math.abs(m-h)<=f;p&&(c.position.top=d._convertPositionTo("relative",{top:n,left:0}).top-d.margins.top),q&&(c.position.top=d._convertPositionTo("relative",{top:o-d.helperProportions.height,left:0}).top-d.margins.top),r&&(c.position.left=d._convertPositionTo("relative",{top:0,left:l}).left-d.margins.left),s&&(c.position.left=d._convertPositionTo("relative",{top:0,left:m-d.helperProportions.width}).left-d.margins.left)}!d.snapElements[k].snapping&&(p||q||r||s||t)&&d.options.snap.snap&&d.options.snap.snap.call(d.element,b,a.extend(d._uiHash(),{snapItem:d.snapElements[k].item})),d.snapElements[k].snapping=p||q||r||s||t}}}),a.ui.plugin.add("draggable","stack",{start:function(b,c){var d=a(this).data("draggable").options,e=a.makeArray(a(d.stack)).sort(function(b,c){return(parseInt(a(b).css("zIndex"),10)||0)-(parseInt(a(c).css("zIndex"),10)||0)});if(!!e.length){var f=parseInt(e[0].style.zIndex)||0;a(e).each(function(a){this.style.zIndex=f+a}),this[0].style.zIndex=f+e.length}}}),a.ui.plugin.add("draggable","zIndex",{start:function(b,c){var d=a(c.helper),e=a(this).data("draggable").options;d.css("zIndex")&&(e._zIndex=d.css("zIndex")),d.css("zIndex",e.zIndex)},stop:function(b,c){var d=a(this).data("draggable").options;d._zIndex&&a(c.helper).css("zIndex",d._zIndex)}})})(jQuery);/*
 * jQuery UI Droppable 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Droppables
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.widget.js
 *    jquery.ui.mouse.js
 *    jquery.ui.draggable.js
 */(function(a,b){a.widget("ui.droppable",{widgetEventPrefix:"drop",options:{accept:"*",activeClass:!1,addClasses:!0,greedy:!1,hoverClass:!1,scope:"default",tolerance:"intersect"},_create:function(){var b=this.options,c=b.accept;this.isover=0,this.isout=1,this.accept=a.isFunction(c)?c:function(a){return a.is(c)},this.proportions={width:this.element[0].offsetWidth,height:this.element[0].offsetHeight},a.ui.ddmanager.droppables[b.scope]=a.ui.ddmanager.droppables[b.scope]||[],a.ui.ddmanager.droppables[b.scope].push(this),b.addClasses&&this.element.addClass("ui-droppable")},destroy:function(){var b=a.ui.ddmanager.droppables[this.options.scope];for(var c=0;c<b.length;c++)b[c]==this&&b.splice(c,1);this.element.removeClass("ui-droppable ui-droppable-disabled").removeData("droppable").unbind(".droppable");return this},_setOption:function(b,c){b=="accept"&&(this.accept=a.isFunction(c)?c:function(a){return a.is(c)}),a.Widget.prototype._setOption.apply(this,arguments)},_activate:function(b){var c=a.ui.ddmanager.current;this.options.activeClass&&this.element.addClass(this.options.activeClass),c&&this._trigger("activate",b,this.ui(c))},_deactivate:function(b){var c=a.ui.ddmanager.current;this.options.activeClass&&this.element.removeClass(this.options.activeClass),c&&this._trigger("deactivate",b,this.ui(c))},_over:function(b){var c=a.ui.ddmanager.current;!!c&&(c.currentItem||c.element)[0]!=this.element[0]&&this.accept.call(this.element[0],c.currentItem||c.element)&&(this.options.hoverClass&&this.element.addClass(this.options.hoverClass),this._trigger("over",b,this.ui(c)))},_out:function(b){var c=a.ui.ddmanager.current;!!c&&(c.currentItem||c.element)[0]!=this.element[0]&&this.accept.call(this.element[0],c.currentItem||c.element)&&(this.options.hoverClass&&this.element.removeClass(this.options.hoverClass),this._trigger("out",b,this.ui(c)))},_drop:function(b,c){var d=c||a.ui.ddmanager.current;if(!d||(d.currentItem||d.element)[0]==this.element[0])return!1;var e=!1;this.element.find(":data(droppable)").not(".ui-draggable-dragging").each(function(){var b=a.data(this,"droppable");if(b.options.greedy&&!b.options.disabled&&b.options.scope==d.options.scope&&b.accept.call(b.element[0],d.currentItem||d.element)&&a.ui.intersect(d,a.extend(b,{offset:b.element.offset()}),b.options.tolerance)){e=!0;return!1}});if(e)return!1;if(this.accept.call(this.element[0],d.currentItem||d.element)){this.options.activeClass&&this.element.removeClass(this.options.activeClass),this.options.hoverClass&&this.element.removeClass(this.options.hoverClass),this._trigger("drop",b,this.ui(d));return this.element}return!1},ui:function(a){return{draggable:a.currentItem||a.element,helper:a.helper,position:a.position,offset:a.positionAbs}}}),a.extend(a.ui.droppable,{version:"1.8.17"}),a.ui.intersect=function(b,c,d){if(!c.offset)return!1;var e=(b.positionAbs||b.position.absolute).left,f=e+b.helperProportions.width,g=(b.positionAbs||b.position.absolute).top,h=g+b.helperProportions.height,i=c.offset.left,j=i+c.proportions.width,k=c.offset.top,l=k+c.proportions.height;switch(d){case"fit":return i<=e&&f<=j&&k<=g&&h<=l;case"intersect":return i<e+b.helperProportions.width/2&&f-b.helperProportions.width/2<j&&k<g+b.helperProportions.height/2&&h-b.helperProportions.height/2<l;case"pointer":var m=(b.positionAbs||b.position.absolute).left+(b.clickOffset||b.offset.click).left,n=(b.positionAbs||b.position.absolute).top+(b.clickOffset||b.offset.click).top,o=a.ui.isOver(n,m,k,i,c.proportions.height,c.proportions.width);return o;case"touch":return(g>=k&&g<=l||h>=k&&h<=l||g<k&&h>l)&&(e>=i&&e<=j||f>=i&&f<=j||e<i&&f>j);default:return!1}},a.ui.ddmanager={current:null,droppables:{"default":[]},prepareOffsets:function(b,c){var d=a.ui.ddmanager.droppables[b.options.scope]||[],e=c?c.type:null,f=(b.currentItem||b.element).find(":data(droppable)").andSelf();droppablesLoop:for(var g=0;g<d.length;g++){if(d[g].options.disabled||b&&!d[g].accept.call(d[g].element[0],b.currentItem||b.element))continue;for(var h=0;h<f.length;h++)if(f[h]==d[g].element[0]){d[g].proportions.height=0;continue droppablesLoop}d[g].visible=d[g].element.css("display")!="none";if(!d[g].visible)continue;e=="mousedown"&&d[g]._activate.call(d[g],c),d[g].offset=d[g].element.offset(),d[g].proportions={width:d[g].element[0].offsetWidth,height:d[g].element[0].offsetHeight}}},drop:function(b,c){var d=!1;a.each(a.ui.ddmanager.droppables[b.options.scope]||[],function(){!this.options||(!this.options.disabled&&this.visible&&a.ui.intersect(b,this,this.options.tolerance)&&(d=this._drop.call(this,c)||d),!this.options.disabled&&this.visible&&this.accept.call(this.element[0],b.currentItem||b.element)&&(this.isout=1,this.isover=0,this._deactivate.call(this,c)))});return d},dragStart:function(b,c){b.element.parents(":not(body,html)").bind("scroll.droppable",function(){b.options.refreshPositions||a.ui.ddmanager.prepareOffsets(b,c)})},drag:function(b,c){b.options.refreshPositions&&a.ui.ddmanager.prepareOffsets(b,c),a.each(a.ui.ddmanager.droppables[b.options.scope]||[],function(){if(!(this.options.disabled||this.greedyChild||!this.visible)){var d=a.ui.intersect(b,this,this.options.tolerance),e=!d&&this.isover==1?"isout":d&&this.isover==0?"isover":null;if(!e)return;var f;if(this.options.greedy){var g=this.element.parents(":data(droppable):eq(0)");g.length&&(f=a.data(g[0],"droppable"),f.greedyChild=e=="isover"?1:0)}f&&e=="isover"&&(f.isover=0,f.isout=1,f._out.call(f,c)),this[e]=1,this[e=="isout"?"isover":"isout"]=0,this[e=="isover"?"_over":"_out"].call(this,c),f&&e=="isout"&&(f.isout=0,f.isover=1,f._over.call(f,c))}})},dragStop:function(b,c){b.element.parents(":not(body,html)").unbind("scroll.droppable"),b.options.refreshPositions||a.ui.ddmanager.prepareOffsets(b,c)}}})(jQuery);/*
 * jQuery UI Resizable 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Resizables
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.mouse.js
 *    jquery.ui.widget.js
 */(function(a,b){a.widget("ui.resizable",a.ui.mouse,{widgetEventPrefix:"resize",options:{alsoResize:!1,animate:!1,animateDuration:"slow",animateEasing:"swing",aspectRatio:!1,autoHide:!1,containment:!1,ghost:!1,grid:!1,handles:"e,s,se",helper:!1,maxHeight:null,maxWidth:null,minHeight:10,minWidth:10,zIndex:1e3},_create:function(){var b=this,c=this.options;this.element.addClass("ui-resizable"),a.extend(this,{_aspectRatio:!!c.aspectRatio,aspectRatio:c.aspectRatio,originalElement:this.element,_proportionallyResizeElements:[],_helper:c.helper||c.ghost||c.animate?c.helper||"ui-resizable-helper":null}),this.element[0].nodeName.match(/canvas|textarea|input|select|button|img/i)&&(/relative/.test(this.element.css("position"))&&a.browser.opera&&this.element.css({position:"relative",top:"auto",left:"auto"}),this.element.wrap(a('<div class="ui-wrapper" style="overflow: hidden;"></div>').css({position:this.element.css("position"),width:this.element.outerWidth(),height:this.element.outerHeight(),top:this.element.css("top"),left:this.element.css("left")})),this.element=this.element.parent().data("resizable",this.element.data("resizable")),this.elementIsWrapper=!0,this.element.css({marginLeft:this.originalElement.css("marginLeft"),marginTop:this.originalElement.css("marginTop"),marginRight:this.originalElement.css("marginRight"),marginBottom:this.originalElement.css("marginBottom")}),this.originalElement.css({marginLeft:0,marginTop:0,marginRight:0,marginBottom:0}),this.originalResizeStyle=this.originalElement.css("resize"),this.originalElement.css("resize","none"),this._proportionallyResizeElements.push(this.originalElement.css({position:"static",zoom:1,display:"block"})),this.originalElement.css({margin:this.originalElement.css("margin")}),this._proportionallyResize()),this.handles=c.handles||(a(".ui-resizable-handle",this.element).length?{n:".ui-resizable-n",e:".ui-resizable-e",s:".ui-resizable-s",w:".ui-resizable-w",se:".ui-resizable-se",sw:".ui-resizable-sw",ne:".ui-resizable-ne",nw:".ui-resizable-nw"}:"e,s,se");if(this.handles.constructor==String){this.handles=="all"&&(this.handles="n,e,s,w,se,sw,ne,nw");var d=this.handles.split(",");this.handles={};for(var e=0;e<d.length;e++){var f=a.trim(d[e]),g="ui-resizable-"+f,h=a('<div class="ui-resizable-handle '+g+'"></div>');/sw|se|ne|nw/.test(f)&&h.css({zIndex:++c.zIndex}),"se"==f&&h.addClass("ui-icon ui-icon-gripsmall-diagonal-se"),this.handles[f]=".ui-resizable-"+f,this.element.append(h)}}this._renderAxis=function(b){b=b||this.element;for(var c in this.handles){this.handles[c].constructor==String&&(this.handles[c]=a(this.handles[c],this.element).show());if(this.elementIsWrapper&&this.originalElement[0].nodeName.match(/textarea|input|select|button/i)){var d=a(this.handles[c],this.element),e=0;e=/sw|ne|nw|se|n|s/.test(c)?d.outerHeight():d.outerWidth();var f=["padding",/ne|nw|n/.test(c)?"Top":/se|sw|s/.test(c)?"Bottom":/^e$/.test(c)?"Right":"Left"].join("");b.css(f,e),this._proportionallyResize()}if(!a(this.handles[c]).length)continue}},this._renderAxis(this.element),this._handles=a(".ui-resizable-handle",this.element).disableSelection(),this._handles.mouseover(function(){if(!b.resizing){if(this.className)var a=this.className.match(/ui-resizable-(se|sw|ne|nw|n|e|s|w)/i);b.axis=a&&a[1]?a[1]:"se"}}),c.autoHide&&(this._handles.hide(),a(this.element).addClass("ui-resizable-autohide").hover(function(){c.disabled||(a(this).removeClass("ui-resizable-autohide"),b._handles.show())},function(){c.disabled||b.resizing||(a(this).addClass("ui-resizable-autohide"),b._handles.hide())})),this._mouseInit()},destroy:function(){this._mouseDestroy();var b=function(b){a(b).removeClass("ui-resizable ui-resizable-disabled ui-resizable-resizing").removeData("resizable").unbind(".resizable").find(".ui-resizable-handle").remove()};if(this.elementIsWrapper){b(this.element);var c=this.element;c.after(this.originalElement.css({position:c.css("position"),width:c.outerWidth(),height:c.outerHeight(),top:c.css("top"),left:c.css("left")})).remove()}this.originalElement.css("resize",this.originalResizeStyle),b(this.originalElement);return this},_mouseCapture:function(b){var c=!1;for(var d in this.handles)a(this.handles[d])[0]==b.target&&(c=!0);return!this.options.disabled&&c},_mouseStart:function(b){var d=this.options,e=this.element.position(),f=this.element;this.resizing=!0,this.documentScroll={top:a(document).scrollTop(),left:a(document).scrollLeft()},(f.is(".ui-draggable")||/absolute/.test(f.css("position")))&&f.css({position:"absolute",top:e.top,left:e.left}),a.browser.opera&&/relative/.test(f.css("position"))&&f.css({position:"relative",top:"auto",left:"auto"}),this._renderProxy();var g=c(this.helper.css("left")),h=c(this.helper.css("top"));d.containment&&(g+=a(d.containment).scrollLeft()||0,h+=a(d.containment).scrollTop()||0),this.offset=this.helper.offset(),this.position={left:g,top:h},this.size=this._helper?{width:f.outerWidth(),height:f.outerHeight()}:{width:f.width(),height:f.height()},this.originalSize=this._helper?{width:f.outerWidth(),height:f.outerHeight()}:{width:f.width(),height:f.height()},this.originalPosition={left:g,top:h},this.sizeDiff={width:f.outerWidth()-f.width(),height:f.outerHeight()-f.height()},this.originalMousePosition={left:b.pageX,top:b.pageY},this.aspectRatio=typeof d.aspectRatio=="number"?d.aspectRatio:this.originalSize.width/this.originalSize.height||1;var i=a(".ui-resizable-"+this.axis).css("cursor");a("body").css("cursor",i=="auto"?this.axis+"-resize":i),f.addClass("ui-resizable-resizing"),this._propagate("start",b);return!0},_mouseDrag:function(b){var c=this.helper,d=this.options,e={},f=this,g=this.originalMousePosition,h=this.axis,i=b.pageX-g.left||0,j=b.pageY-g.top||0,k=this._change[h];if(!k)return!1;var l=k.apply(this,[b,i,j]),m=a.browser.msie&&a.browser.version<7,n=this.sizeDiff;this._updateVirtualBoundaries(b.shiftKey);if(this._aspectRatio||b.shiftKey)l=this._updateRatio(l,b);l=this._respectSize(l,b),this._propagate("resize",b),c.css({top:this.position.top+"px",left:this.position.left+"px",width:this.size.width+"px",height:this.size.height+"px"}),!this._helper&&this._proportionallyResizeElements.length&&this._proportionallyResize(),this._updateCache(l),this._trigger("resize",b,this.ui());return!1},_mouseStop:function(b){this.resizing=!1;var c=this.options,d=this;if(this._helper){var e=this._proportionallyResizeElements,f=e.length&&/textarea/i.test(e[0].nodeName),g=f&&a.ui.hasScroll(e[0],"left")?0:d.sizeDiff.height,h=f?0:d.sizeDiff.width,i={width:d.helper.width()-h,height:d.helper.height()-g},j=parseInt(d.element.css("left"),10)+(d.position.left-d.originalPosition.left)||null,k=parseInt(d.element.css("top"),10)+(d.position.top-d.originalPosition.top)||null;c.animate||this.element.css(a.extend(i,{top:k,left:j})),d.helper.height(d.size.height),d.helper.width(d.size.width),this._helper&&!c.animate&&this._proportionallyResize()}a("body").css("cursor","auto"),this.element.removeClass("ui-resizable-resizing"),this._propagate("stop",b),this._helper&&this.helper.remove();return!1},_updateVirtualBoundaries:function(a){var b=this.options,c,e,f,g,h;h={minWidth:d(b.minWidth)?b.minWidth:0,maxWidth:d(b.maxWidth)?b.maxWidth:Infinity,minHeight:d(b.minHeight)?b.minHeight:0,maxHeight:d(b.maxHeight)?b.maxHeight:Infinity};if(this._aspectRatio||a)c=h.minHeight*this.aspectRatio,f=h.minWidth/this.aspectRatio,e=h.maxHeight*this.aspectRatio,g=h.maxWidth/this.aspectRatio,c>h.minWidth&&(h.minWidth=c),f>h.minHeight&&(h.minHeight=f),e<h.maxWidth&&(h.maxWidth=e),g<h.maxHeight&&(h.maxHeight=g);this._vBoundaries=h},_updateCache:function(a){var b=this.options;this.offset=this.helper.offset(),d(a.left)&&(this.position.left=a.left),d(a.top)&&(this.position.top=a.top),d(a.height)&&(this.size.height=a.height),d(a.width)&&(this.size.width=a.width)},_updateRatio:function(a,b){var c=this.options,e=this.position,f=this.size,g=this.axis;d(a.height)?a.width=a.height*this.aspectRatio:d(a.width)&&(a.height=a.width/this.aspectRatio),g=="sw"&&(a.left=e.left+(f.width-a.width),a.top=null),g=="nw"&&(a.top=e.top+(f.height-a.height),a.left=e.left+(f.width-a.width));return a},_respectSize:function(a,b){var c=this.helper,e=this._vBoundaries,f=this._aspectRatio||b.shiftKey,g=this.axis,h=d(a.width)&&e.maxWidth&&e.maxWidth<a.width,i=d(a.height)&&e.maxHeight&&e.maxHeight<a.height,j=d(a.width)&&e.minWidth&&e.minWidth>a.width,k=d(a.height)&&e.minHeight&&e.minHeight>a.height;j&&(a.width=e.minWidth),k&&(a.height=e.minHeight),h&&(a.width=e.maxWidth),i&&(a.height=e.maxHeight);var l=this.originalPosition.left+this.originalSize.width,m=this.position.top+this.size.height,n=/sw|nw|w/.test(g),o=/nw|ne|n/.test(g);j&&n&&(a.left=l-e.minWidth),h&&n&&(a.left=l-e.maxWidth),k&&o&&(a.top=m-e.minHeight),i&&o&&(a.top=m-e.maxHeight);var p=!a.width&&!a.height;p&&!a.left&&a.top?a.top=null:p&&!a.top&&a.left&&(a.left=null);return a},_proportionallyResize:function(){var b=this.options;if(!!this._proportionallyResizeElements.length){var c=this.helper||this.element;for(var d=0;d<this._proportionallyResizeElements.length;d++){var e=this._proportionallyResizeElements[d];if(!this.borderDif){var f=[e.css("borderTopWidth"),e.css("borderRightWidth"),e.css("borderBottomWidth"),e.css("borderLeftWidth")],g=[e.css("paddingTop"),e.css("paddingRight"),e.css("paddingBottom"),e.css("paddingLeft")];this.borderDif=a.map(f,function(a,b){var c=parseInt(a,10)||0,d=parseInt(g[b],10)||0;return c+d})}if(a.browser.msie&&(!!a(c).is(":hidden")||!!a(c).parents(":hidden").length))continue;e.css({height:c.height()-this.borderDif[0]-this.borderDif[2]||0,width:c.width()-this.borderDif[1]-this.borderDif[3]||0})}}},_renderProxy:function(){var b=this.element,c=this.options;this.elementOffset=b.offset();if(this._helper){this.helper=this.helper||a('<div style="overflow:hidden;"></div>');var d=a.browser.msie&&a.browser.version<7,e=d?1:0,f=d?2:-1;this.helper.addClass(this._helper).css({width:this.element.outerWidth()+f,height:this.element.outerHeight()+f,position:"absolute",left:this.elementOffset.left-e+"px",top:this.elementOffset.top-e+"px",zIndex:++c.zIndex}),this.helper.appendTo("body").disableSelection()}else this.helper=this.element},_change:{e:function(a,b,c){return{width:this.originalSize.width+b}},w:function(a,b,c){var d=this.options,e=this.originalSize,f=this.originalPosition;return{left:f.left+b,width:e.width-b}},n:function(a,b,c){var d=this.options,e=this.originalSize,f=this.originalPosition;return{top:f.top+c,height:e.height-c}},s:function(a,b,c){return{height:this.originalSize.height+c}},se:function(b,c,d){return a.extend(this._change.s.apply(this,arguments),this._change.e.apply(this,[b,c,d]))},sw:function(b,c,d){return a.extend(this._change.s.apply(this,arguments),this._change.w.apply(this,[b,c,d]))},ne:function(b,c,d){return a.extend(this._change.n.apply(this,arguments),this._change.e.apply(this,[b,c,d]))},nw:function(b,c,d){return a.extend(this._change.n.apply(this,arguments),this._change.w.apply(this,[b,c,d]))}},_propagate:function(b,c){a.ui.plugin.call(this,b,[c,this.ui()]),b!="resize"&&this._trigger(b,c,this.ui())},plugins:{},ui:function(){return{originalElement:this.originalElement,element:this.element,helper:this.helper,position:this.position,size:this.size,originalSize:this.originalSize,originalPosition:this.originalPosition}}}),a.extend(a.ui.resizable,{version:"1.8.17"}),a.ui.plugin.add("resizable","alsoResize",{start:function(b,c){var d=a(this).data("resizable"),e=d.options,f=function(b){a(b).each(function(){var b=a(this);b.data("resizable-alsoresize",{width:parseInt(b.width(),10),height:parseInt(b.height(),10),left:parseInt(b.css("left"),10),top:parseInt(b.css("top"),10),position:b.css("position")})})};typeof e.alsoResize=="object"&&!e.alsoResize.parentNode?e.alsoResize.length?(e.alsoResize=e.alsoResize[0],f(e.alsoResize)):a.each(e.alsoResize,function(a){f(a)}):f(e.alsoResize)},resize:function(b,c){var d=a(this).data("resizable"),e=d.options,f=d.originalSize,g=d.originalPosition,h={height:d.size.height-f.height||0,width:d.size.width-f.width||0,top:d.position.top-g.top||0,left:d.position.left-g.left||0},i=function(b,e){a(b).each(function(){var b=a(this),f=a(this).data("resizable-alsoresize"),g={},i=e&&e.length?e:b.parents(c.originalElement[0]).length?["width","height"]:["width","height","top","left"];a.each(i,function(a,b){var c=(f[b]||0)+(h[b]||0);c&&c>=0&&(g[b]=c||null)}),a.browser.opera&&/relative/.test(b.css("position"))&&(d._revertToRelativePosition=!0,b.css({position:"absolute",top:"auto",left:"auto"})),b.css(g)})};typeof e.alsoResize=="object"&&!e.alsoResize.nodeType?a.each(e.alsoResize,function(a,b){i(a,b)}):i(e.alsoResize)},stop:function(b,c){var d=a(this).data("resizable"),e=d.options,f=function(b){a(b).each(function(){var b=a(this);b.css({position:b.data("resizable-alsoresize").position})})};d._revertToRelativePosition&&(d._revertToRelativePosition=!1,typeof e.alsoResize=="object"&&!e.alsoResize.nodeType?a.each(e.alsoResize,function(a){f(a)}):f(e.alsoResize)),a(this).removeData("resizable-alsoresize")}}),a.ui.plugin.add("resizable","animate",{stop:function(b,c){var d=a(this).data("resizable"),e=d.options,f=d._proportionallyResizeElements,g=f.length&&/textarea/i.test(f[0].nodeName),h=g&&a.ui.hasScroll(f[0],"left")?0:d.sizeDiff.height,i=g?0:d.sizeDiff.width,j={width:d.size.width-i,height:d.size.height-h},k=parseInt(d.element.css("left"),10)+(d.position.left-d.originalPosition.left)||null,l=parseInt(d.element.css("top"),10)+(d.position.top-d.originalPosition.top)||null;d.element.animate(a.extend(j,l&&k?{top:l,left:k}:{}),{duration:e.animateDuration,easing:e.animateEasing,step:function(){var c={width:parseInt(d.element.css("width"),10),height:parseInt(d.element.css("height"),10),top:parseInt(d.element.css("top"),10),left:parseInt(d.element.css("left"),10)};f&&f.length&&a(f[0]).css({width:c.width,height:c.height}),d._updateCache(c),d._propagate("resize",b)}})}}),a.ui.plugin.add("resizable","containment",{start:function(b,d){var e=a(this).data("resizable"),f=e.options,g=e.element,h=f.containment,i=h instanceof a?h.get(0):/parent/.test(h)?g.parent().get(0):h;if(!!i){e.containerElement=a(i);if(/document/.test(h)||h==document)e.containerOffset={left:0,top:0},e.containerPosition={left:0,top:0},e.parentData={element:a(document),left:0,top:0,width:a(document).width(),height:a(document).height()||document.body.parentNode.scrollHeight};else{var j=a(i),k=[];a(["Top","Right","Left","Bottom"]).each(function(a,b){k[a]=c(j.css("padding"+b))}),e.containerOffset=j.offset(),e.containerPosition=j.position(),e.containerSize={height:j.innerHeight()-k[3],width:j.innerWidth()-k[1]};var l=e.containerOffset,m=e.containerSize.height,n=e.containerSize.width,o=a.ui.hasScroll(i,"left")?i.scrollWidth:n,p=a.ui.hasScroll(i)?i.scrollHeight:m;e.parentData={element:i,left:l.left,top:l.top,width:o,height:p}}}},resize:function(b,c){var d=a(this).data("resizable"),e=d.options,f=d.containerSize,g=d.containerOffset,h=d.size,i=d.position,j=d._aspectRatio||b.shiftKey,k={top:0,left:0},l=d.containerElement;l[0]!=document&&/static/.test(l.css("position"))&&(k=g),i.left<(d._helper?g.left:0)&&(d.size.width=d.size.width+(d._helper?d.position.left-g.left:d.position.left-k.left),j&&(d.size.height=d.size.width/e.aspectRatio),d.position.left=e.helper?g.left:0),i.top<(d._helper?g.top:0)&&(d.size.height=d.size.height+(d._helper?d.position.top-g.top:d.position.top),j&&(d.size.width=d.size.height*e.aspectRatio),d.position.top=d._helper?g.top:0),d.offset.left=d.parentData.left+d.position.left,d.offset.top=d.parentData.top+d.position.top;var m=Math.abs((d._helper?d.offset.left-k.left:d.offset.left-k.left)+d.sizeDiff.width),n=Math.abs((d._helper?d.offset.top-k.top:d.offset.top-g.top)+d.sizeDiff.height),o=d.containerElement.get(0)==d.element.parent().get(0),p=/relative|absolute/.test(d.containerElement.css("position"));o&&p&&(m-=d.parentData.left),m+d.size.width>=d.parentData.width&&(d.size.width=d.parentData.width-m,j&&(d.size.height=d.size.width/d.aspectRatio)),n+d.size.height>=d.parentData.height&&(d.size.height=d.parentData.height-n,j&&(d.size.width=d.size.height*d.aspectRatio))},stop:function(b,c){var d=a(this).data("resizable"),e=d.options,f=d.position,g=d.containerOffset,h=d.containerPosition,i=d.containerElement,j=a(d.helper),k=j.offset(),l=j.outerWidth()-d.sizeDiff.width,m=j.outerHeight()-d.sizeDiff.height;d._helper&&!e.animate&&/relative/.test(i.css("position"))&&a(this).css({left:k.left-h.left-g.left,width:l,height:m}),d._helper&&!e.animate&&/static/.test(i.css("position"))&&a(this).css({left:k.left-h.left-g.left,width:l,height:m})}}),a.ui.plugin.add("resizable","ghost",{start:function(b,c){var d=a(this).data("resizable"),e=d.options,f=d.size;d.ghost=d.originalElement.clone(),d.ghost.css({opacity:.25,display:"block",position:"relative",height:f.height,width:f.width,margin:0,left:0,top:0}).addClass("ui-resizable-ghost").addClass(typeof e.ghost=="string"?e.ghost:""),d.ghost.appendTo(d.helper)},resize:function(b,c){var d=a(this).data("resizable"),e=d.options;d.ghost&&d.ghost.css({position:"relative",height:d.size.height,width:d.size.width})},stop:function(b,c){var d=a(this).data("resizable"),e=d.options;d.ghost&&d.helper&&d.helper.get(0).removeChild(d.ghost.get(0))}}),a.ui.plugin.add("resizable","grid",{resize:function(b,c){var d=a(this).data("resizable"),e=d.options,f=d.size,g=d.originalSize,h=d.originalPosition,i=d.axis,j=e._aspectRatio||b.shiftKey;e.grid=typeof e.grid=="number"?[e.grid,e.grid]:e.grid;var k=Math.round((f.width-g.width)/(e.grid[0]||1))*(e.grid[0]||1),l=Math.round((f.height-g.height)/(e.grid[1]||1))*(e.grid[1]||1);/^(se|s|e)$/.test(i)?(d.size.width=g.width+k,d.size.height=g.height+l):/^(ne)$/.test(i)?(d.size.width=g.width+k,d.size.height=g.height+l,d.position.top=h.top-l):/^(sw)$/.test(i)?(d.size.width=g.width+k,d.size.height=g.height+l,d.position.left=h.left-k):(d.size.width=g.width+k,d.size.height=g.height+l,d.position.top=h.top-l,d.position.left=h.left-k)}});var c=function(a){return parseInt(a,10)||0},d=function(a){return!isNaN(parseInt(a,10))}})(jQuery);/*
 * jQuery UI Selectable 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Selectables
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.mouse.js
 *    jquery.ui.widget.js
 */(function(a,b){a.widget("ui.selectable",a.ui.mouse,{options:{appendTo:"body",autoRefresh:!0,distance:0,filter:"*",tolerance:"touch"},_create:function(){var b=this;this.element.addClass("ui-selectable"),this.dragged=!1;var c;this.refresh=function(){c=a(b.options.filter,b.element[0]),c.addClass("ui-selectee"),c.each(function(){var b=a(this),c=b.offset();a.data(this,"selectable-item",{element:this,$element:b,left:c.left,top:c.top,right:c.left+b.outerWidth(),bottom:c.top+b.outerHeight(),startselected:!1,selected:b.hasClass("ui-selected"),selecting:b.hasClass("ui-selecting"),unselecting:b.hasClass("ui-unselecting")})})},this.refresh(),this.selectees=c.addClass("ui-selectee"),this._mouseInit(),this.helper=a("<div class='ui-selectable-helper'></div>")},destroy:function(){this.selectees.removeClass("ui-selectee").removeData("selectable-item"),this.element.removeClass("ui-selectable ui-selectable-disabled").removeData("selectable").unbind(".selectable"),this._mouseDestroy();return this},_mouseStart:function(b){var c=this;this.opos=[b.pageX,b.pageY];if(!this.options.disabled){var d=this.options;this.selectees=a(d.filter,this.element[0]),this._trigger("start",b),a(d.appendTo).append(this.helper),this.helper.css({left:b.clientX,top:b.clientY,width:0,height:0}),d.autoRefresh&&this.refresh(),this.selectees.filter(".ui-selected").each(function(){var d=a.data(this,"selectable-item");d.startselected=!0,!b.metaKey&&!b.ctrlKey&&(d.$element.removeClass("ui-selected"),d.selected=!1,d.$element.addClass("ui-unselecting"),d.unselecting=!0,c._trigger("unselecting",b,{unselecting:d.element}))}),a(b.target).parents().andSelf().each(function(){var d=a.data(this,"selectable-item");if(d){var e=!b.metaKey&&!b.ctrlKey||!d.$element.hasClass("ui-selected");d.$element.removeClass(e?"ui-unselecting":"ui-selected").addClass(e?"ui-selecting":"ui-unselecting"),d.unselecting=!e,d.selecting=e,d.selected=e,e?c._trigger("selecting",b,{selecting:d.element}):c._trigger("unselecting",b,{unselecting:d.element});return!1}})}},_mouseDrag:function(b){var c=this;this.dragged=!0;if(!this.options.disabled){var d=this.options,e=this.opos[0],f=this.opos[1],g=b.pageX,h=b.pageY;if(e>g){var i=g;g=e,e=i}if(f>h){var i=h;h=f,f=i}this.helper.css({left:e,top:f,width:g-e,height:h-f}),this.selectees.each(function(){var i=a.data(this,"selectable-item");if(!!i&&i.element!=c.element[0]){var j=!1;d.tolerance=="touch"?j=!(i.left>g||i.right<e||i.top>h||i.bottom<f):d.tolerance=="fit"&&(j=i.left>e&&i.right<g&&i.top>f&&i.bottom<h),j?(i.selected&&(i.$element.removeClass("ui-selected"),i.selected=!1),i.unselecting&&(i.$element.removeClass("ui-unselecting"),i.unselecting=!1),i.selecting||(i.$element.addClass("ui-selecting"),i.selecting=!0,c._trigger("selecting",b,{selecting:i.element}))):(i.selecting&&((b.metaKey||b.ctrlKey)&&i.startselected?(i.$element.removeClass("ui-selecting"),i.selecting=!1,i.$element.addClass("ui-selected"),i.selected=!0):(i.$element.removeClass("ui-selecting"),i.selecting=!1,i.startselected&&(i.$element.addClass("ui-unselecting"),i.unselecting=!0),c._trigger("unselecting",b,{unselecting:i.element}))),i.selected&&!b.metaKey&&!b.ctrlKey&&!i.startselected&&(i.$element.removeClass("ui-selected"),i.selected=!1,i.$element.addClass("ui-unselecting"),i.unselecting=!0,c._trigger("unselecting",b,{unselecting:i.element})))}});return!1}},_mouseStop:function(b){var c=this;this.dragged=!1;var d=this.options;a(".ui-unselecting",this.element[0]).each(function(){var d=a.data(this,"selectable-item");d.$element.removeClass("ui-unselecting"),d.unselecting=!1,d.startselected=!1,c._trigger("unselected",b,{unselected:d.element})}),a(".ui-selecting",this.element[0]).each(function(){var d=a.data(this,"selectable-item");d.$element.removeClass("ui-selecting").addClass("ui-selected"),d.selecting=!1,d.selected=!0,d.startselected=!0,c._trigger("selected",b,{selected:d.element})}),this._trigger("stop",b),this.helper.remove();return!1}}),a.extend(a.ui.selectable,{version:"1.8.17"})})(jQuery);/*
 * jQuery UI Sortable 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Sortables
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.mouse.js
 *    jquery.ui.widget.js
 */(function(a,b){a.widget("ui.sortable",a.ui.mouse,{widgetEventPrefix:"sort",options:{appendTo:"parent",axis:!1,connectWith:!1,containment:!1,cursor:"auto",cursorAt:!1,dropOnEmpty:!0,forcePlaceholderSize:!1,forceHelperSize:!1,grid:!1,handle:!1,helper:"original",items:"> *",opacity:!1,placeholder:!1,revert:!1,scroll:!0,scrollSensitivity:20,scrollSpeed:20,scope:"default",tolerance:"intersect",zIndex:1e3},_create:function(){var a=this.options;this.containerCache={},this.element.addClass("ui-sortable"),this.refresh(),this.floating=this.items.length?a.axis==="x"||/left|right/.test(this.items[0].item.css("float"))||/inline|table-cell/.test(this.items[0].item.css("display")):!1,this.offset=this.element.offset(),this._mouseInit()},destroy:function(){this.element.removeClass("ui-sortable ui-sortable-disabled"),this._mouseDestroy();for(var a=this.items.length-1;a>=0;a--)this.items[a].item.removeData(this.widgetName+"-item");return this},_setOption:function(b,c){b==="disabled"?(this.options[b]=c,this.widget()[c?"addClass":"removeClass"]("ui-sortable-disabled")):a.Widget.prototype._setOption.apply(this,arguments)},_mouseCapture:function(b,c){var d=this;if(this.reverting)return!1;if(this.options.disabled||this.options.type=="static")return!1;this._refreshItems(b);var e=null,f=this,g=a(b.target).parents().each(function(){if(a.data(this,d.widgetName+"-item")==f){e=a(this);return!1}});a.data(b.target,d.widgetName+"-item")==f&&(e=a(b.target));if(!e)return!1;if(this.options.handle&&!c){var h=!1;a(this.options.handle,e).find("*").andSelf().each(function(){this==b.target&&(h=!0)});if(!h)return!1}this.currentItem=e,this._removeCurrentsFromItems();return!0},_mouseStart:function(b,c,d){var e=this.options,f=this;this.currentContainer=this,this.refreshPositions(),this.helper=this._createHelper(b),this._cacheHelperProportions(),this._cacheMargins(),this.scrollParent=this.helper.scrollParent(),this.offset=this.currentItem.offset(),this.offset={top:this.offset.top-this.margins.top,left:this.offset.left-this.margins.left},this.helper.css("position","absolute"),this.cssPosition=this.helper.css("position"),a.extend(this.offset,{click:{left:b.pageX-this.offset.left,top:b.pageY-this.offset.top},parent:this._getParentOffset(),relative:this._getRelativeOffset()}),this.originalPosition=this._generatePosition(b),this.originalPageX=b.pageX,this.originalPageY=b.pageY,e.cursorAt&&this._adjustOffsetFromHelper(e.cursorAt),this.domPosition={prev:this.currentItem.prev()[0],parent:this.currentItem.parent()[0]},this.helper[0]!=this.currentItem[0]&&this.currentItem.hide(),this._createPlaceholder(),e.containment&&this._setContainment(),e.cursor&&(a("body").css("cursor")&&(this._storedCursor=a("body").css("cursor")),a("body").css("cursor",e.cursor)),e.opacity&&(this.helper.css("opacity")&&(this._storedOpacity=this.helper.css("opacity")),this.helper.css("opacity",e.opacity)),e.zIndex&&(this.helper.css("zIndex")&&(this._storedZIndex=this.helper.css("zIndex")),this.helper.css("zIndex",e.zIndex)),this.scrollParent[0]!=document&&this.scrollParent[0].tagName!="HTML"&&(this.overflowOffset=this.scrollParent.offset()),this._trigger("start",b,this._uiHash()),this._preserveHelperProportions||this._cacheHelperProportions();if(!d)for(var g=this.containers.length-1;g>=0;g--)this.containers[g]._trigger("activate",b,f._uiHash(this));a.ui.ddmanager&&(a.ui.ddmanager.current=this),a.ui.ddmanager&&!e.dropBehaviour&&a.ui.ddmanager.prepareOffsets(this,b),this.dragging=!0,this.helper.addClass("ui-sortable-helper"),this._mouseDrag(b);return!0},_mouseDrag:function(b){this.position=this._generatePosition(b),this.positionAbs=this._convertPositionTo("absolute"),this.lastPositionAbs||(this.lastPositionAbs=this.positionAbs);if(this.options.scroll){var c=this.options,d=!1;this.scrollParent[0]!=document&&this.scrollParent[0].tagName!="HTML"?(this.overflowOffset.top+this.scrollParent[0].offsetHeight-b.pageY<c.scrollSensitivity?this.scrollParent[0].scrollTop=d=this.scrollParent[0].scrollTop+c.scrollSpeed:b.pageY-this.overflowOffset.top<c.scrollSensitivity&&(this.scrollParent[0].scrollTop=d=this.scrollParent[0].scrollTop-c.scrollSpeed),this.overflowOffset.left+this.scrollParent[0].offsetWidth-b.pageX<c.scrollSensitivity?this.scrollParent[0].scrollLeft=d=this.scrollParent[0].scrollLeft+c.scrollSpeed:b.pageX-this.overflowOffset.left<c.scrollSensitivity&&(this.scrollParent[0].scrollLeft=d=this.scrollParent[0].scrollLeft-c.scrollSpeed)):(b.pageY-a(document).scrollTop()<c.scrollSensitivity?d=a(document).scrollTop(a(document).scrollTop()-c.scrollSpeed):a(window).height()-(b.pageY-a(document).scrollTop())<c.scrollSensitivity&&(d=a(document).scrollTop(a(document).scrollTop()+c.scrollSpeed)),b.pageX-a(document).scrollLeft()<c.scrollSensitivity?d=a(document).scrollLeft(a(document).scrollLeft()-c.scrollSpeed):a(window).width()-(b.pageX-a(document).scrollLeft())<c.scrollSensitivity&&(d=a(document).scrollLeft(a(document).scrollLeft()+c.scrollSpeed))),d!==!1&&a.ui.ddmanager&&!c.dropBehaviour&&a.ui.ddmanager.prepareOffsets(this,b)}this.positionAbs=this._convertPositionTo("absolute");if(!this.options.axis||this.options.axis!="y")this.helper[0].style.left=this.position.left+"px";if(!this.options.axis||this.options.axis!="x")this.helper[0].style.top=this.position.top+"px";for(var e=this.items.length-1;e>=0;e--){var f=this.items[e],g=f.item[0],h=this._intersectsWithPointer(f);if(!h)continue;if(g!=this.currentItem[0]&&this.placeholder[h==1?"next":"prev"]()[0]!=g&&!a.ui.contains(this.placeholder[0],g)&&(this.options.type=="semi-dynamic"?!a.ui.contains(this.element[0],g):!0)){this.direction=h==1?"down":"up";if(this.options.tolerance=="pointer"||this._intersectsWithSides(f))this._rearrange(b,f);else break;this._trigger("change",b,this._uiHash());break}}this._contactContainers(b),a.ui.ddmanager&&a.ui.ddmanager.drag(this,b),this._trigger("sort",b,this._uiHash()),this.lastPositionAbs=this.positionAbs;return!1},_mouseStop:function(b,c){if(!!b){a.ui.ddmanager&&!this.options.dropBehaviour&&a.ui.ddmanager.drop(this,b);if(this.options.revert){var d=this,e=d.placeholder.offset();d.reverting=!0,a(this.helper).animate({left:e.left-this.offset.parent.left-d.margins.left+(this.offsetParent[0]==document.body?0:this.offsetParent[0].scrollLeft),top:e.top-this.offset.parent.top-d.margins.top+(this.offsetParent[0]==document.body?0:this.offsetParent[0].scrollTop)},parseInt(this.options.revert,10)||500,function(){d._clear(b)})}else this._clear(b,c);return!1}},cancel:function(){var b=this;if(this.dragging){this._mouseUp({target:null}),this.options.helper=="original"?this.currentItem.css(this._storedCSS).removeClass("ui-sortable-helper"):this.currentItem.show();for(var c=this.containers.length-1;c>=0;c--)this.containers[c]._trigger("deactivate",null,b._uiHash(this)),this.containers[c].containerCache.over&&(this.containers[c]._trigger("out",null,b._uiHash(this)),this.containers[c].containerCache.over=0)}this.placeholder&&(this.placeholder[0].parentNode&&this.placeholder[0].parentNode.removeChild(this.placeholder[0]),this.options.helper!="original"&&this.helper&&this.helper[0].parentNode&&this.helper.remove(),a.extend(this,{helper:null,dragging:!1,reverting:!1,_noFinalSort:null}),this.domPosition.prev?a(this.domPosition.prev).after(this.currentItem):a(this.domPosition.parent).prepend(this.currentItem));return this},serialize:function(b){var c=this._getItemsAsjQuery(b&&b.connected),d=[];b=b||{},a(c).each(function(){var c=(a(b.item||this).attr(b.attribute||"id")||"").match(b.expression||/(.+)[-=_](.+)/);c&&d.push((b.key||c[1]+"[]")+"="+(b.key&&b.expression?c[1]:c[2]))}),!d.length&&b.key&&d.push(b.key+"=");return d.join("&")},toArray:function(b){var c=this._getItemsAsjQuery(b&&b.connected),d=[];b=b||{},c.each(function(){d.push(a(b.item||this).attr(b.attribute||"id")||"")});return d},_intersectsWith:function(a){var b=this.positionAbs.left,c=b+this.helperProportions.width,d=this.positionAbs.top,e=d+this.helperProportions.height,f=a.left,g=f+a.width,h=a.top,i=h+a.height,j=this.offset.click.top,k=this.offset.click.left,l=d+j>h&&d+j<i&&b+k>f&&b+k<g;return this.options.tolerance=="pointer"||this.options.forcePointerForContainers||this.options.tolerance!="pointer"&&this.helperProportions[this.floating?"width":"height"]>a[this.floating?"width":"height"]?l:f<b+this.helperProportions.width/2&&c-this.helperProportions.width/2<g&&h<d+this.helperProportions.height/2&&e-this.helperProportions.height/2<i},_intersectsWithPointer:function(b){var c=a.ui.isOverAxis(this.positionAbs.top+this.offset.click.top,b.top,b.height),d=a.ui.isOverAxis(this.positionAbs.left+this.offset.click.left,b.left,b.width),e=c&&d,f=this._getDragVerticalDirection(),g=this._getDragHorizontalDirection();if(!e)return!1;return this.floating?g&&g=="right"||f=="down"?2:1:f&&(f=="down"?2:1)},_intersectsWithSides:function(b){var c=a.ui.isOverAxis(this.positionAbs.top+this.offset.click.top,b.top+b.height/2,b.height),d=a.ui.isOverAxis(this.positionAbs.left+this.offset.click.left,b.left+b.width/2,b.width),e=this._getDragVerticalDirection(),f=this._getDragHorizontalDirection();return this.floating&&f?f=="right"&&d||f=="left"&&!d:e&&(e=="down"&&c||e=="up"&&!c)},_getDragVerticalDirection:function(){var a=this.positionAbs.top-this.lastPositionAbs.top;return a!=0&&(a>0?"down":"up")},_getDragHorizontalDirection:function(){var a=this.positionAbs.left-this.lastPositionAbs.left;return a!=0&&(a>0?"right":"left")},refresh:function(a){this._refreshItems(a),this.refreshPositions();return this},_connectWith:function(){var a=this.options;return a.connectWith.constructor==String?[a.connectWith]:a.connectWith},_getItemsAsjQuery:function(b){var c=this,d=[],e=[],f=this._connectWith();if(f&&b)for(var g=f.length-1;g>=0;g--){var h=a(f[g]);for(var i=h.length-1;i>=0;i--){var j=a.data(h[i],this.widgetName);j&&j!=this&&!j.options.disabled&&e.push([a.isFunction(j.options.items)?j.options.items.call(j.element):a(j.options.items,j.element).not(".ui-sortable-helper").not(".ui-sortable-placeholder"),j])}}e.push([a.isFunction(this.options.items)?this.options.items.call(this.element,null,{options:this.options,item:this.currentItem}):a(this.options.items,this.element).not(".ui-sortable-helper").not(".ui-sortable-placeholder"),this]);for(var g=e.length-1;g>=0;g--)e[g][0].each(function(){d.push(this)});return a(d)},_removeCurrentsFromItems:function(){var a=this.currentItem.find(":data("+this.widgetName+"-item)");for(var b=0;b<this.items.length;b++)for(var c=0;c<a.length;c++)a[c]==this.items[b].item[0]&&this.items.splice(b,1)},_refreshItems:function(b){this.items=[],this.containers=[this];var c=this.items,d=this,e=[[a.isFunction(this.options.items)?this.options.items.call(this.element[0],b,{item:this.currentItem}):a(this.options.items,this.element),this]],f=this._connectWith();if(f)for(var g=f.length-1;g>=0;g--){var h=a(f[g]);for(var i=h.length-1;i>=0;i--){var j=a.data(h[i],this.widgetName);j&&j!=this&&!j.options.disabled&&(e.push([a.isFunction(j.options.items)?j.options.items.call(j.element[0],b,{item:this.currentItem}):a(j.options.items,j.element),j]),this.containers.push(j))}}for(var g=e.length-1;g>=0;g--){var k=e[g][1],l=e[g][0];for(var i=0,m=l.length;i<m;i++){var n=a(l[i]);n.data(this.widgetName+"-item",k),c.push({item:n,instance:k,width:0,height:0,left:0,top:0})}}},refreshPositions:function(b){this.offsetParent&&this.helper&&(this.offset.parent=this._getParentOffset());for(var c=this.items.length-1;c>=0;c--){var d=this.items[c];if(d.instance!=this.currentContainer&&this.currentContainer&&d.item[0]!=this.currentItem[0])continue;var e=this.options.toleranceElement?a(this.options.toleranceElement,d.item):d.item;b||(d.width=e.outerWidth(),d.height=e.outerHeight());var f=e.offset();d.left=f.left,d.top=f.top}if(this.options.custom&&this.options.custom.refreshContainers)this.options.custom.refreshContainers.call(this);else for(var c=this.containers.length-1;c>=0;c--){var f=this.containers[c].element.offset();this.containers[c].containerCache.left=f.left,this.containers[c].containerCache.top=f.top,this.containers[c].containerCache.width=this.containers[c].element.outerWidth(),this.containers[c].containerCache.height=this.containers[c].element.outerHeight()}return this},_createPlaceholder:function(b){var c=b||this,d=c.options;if(!d.placeholder||d.placeholder.constructor==String){var e=d.placeholder;d.placeholder={element:function(){var b=a(document.createElement(c.currentItem[0].nodeName)).addClass(e||c.currentItem[0].className+" ui-sortable-placeholder").removeClass("ui-sortable-helper")[0];e||(b.style.visibility="hidden");return b},update:function(a,b){if(!e||!!d.forcePlaceholderSize)b.height()||b.height(c.currentItem.innerHeight()-parseInt(c.currentItem.css("paddingTop")||0,10)-parseInt(c.currentItem.css("paddingBottom")||0,10)),b.width()||b.width(c.currentItem.innerWidth()-parseInt(c.currentItem.css("paddingLeft")||0,10)-parseInt(c.currentItem.css("paddingRight")||0,10))}}}c.placeholder=a(d.placeholder.element.call(c.element,c.currentItem)),c.currentItem.after(c.placeholder),d.placeholder.update(c,c.placeholder)},_contactContainers:function(b){var c=null,d=null;for(var e=this.containers.length-1;e>=0;e--){if(a.ui.contains(this.currentItem[0],this.containers[e].element[0]))continue;if(this._intersectsWith(this.containers[e].containerCache)){if(c&&a.ui.contains(this.containers[e].element[0],c.element[0]))continue;c=this.containers[e],d=e}else this.containers[e].containerCache.over&&(this.containers[e]._trigger("out",b,this._uiHash(this)),this.containers[e].containerCache.over=0)}if(!!c)if(this.containers.length===1)this.containers[d]._trigger("over",b,this._uiHash(this)),this.containers[d].containerCache.over=1;else if(this.currentContainer!=this.containers[d]){var f=1e4,g=null,h=this.positionAbs[this.containers[d].floating?"left":"top"];for(var i=this.items.length-1;i>=0;i--){if(!a.ui.contains(this.containers[d].element[0],this.items[i].item[0]))continue;var j=this.items[i][this.containers[d].floating?"left":"top"];Math.abs(j-h)<f&&(f=Math.abs(j-h),g=this.items[i])}if(!g&&!this.options.dropOnEmpty)return;this.currentContainer=this.containers[d],g?this._rearrange(b,g,null,!0):this._rearrange(b,null,this.containers[d].element,!0),this._trigger("change",b,this._uiHash()),this.containers[d]._trigger("change",b,this._uiHash(this)),this.options.placeholder.update(this.currentContainer,this.placeholder),this.containers[d]._trigger("over",b,this._uiHash(this)),this.containers[d].containerCache.over=1}},_createHelper:function(b){var c=this.options,d=a.isFunction(c.helper)?a(c.helper.apply(this.element[0],[b,this.currentItem])):c.helper=="clone"?this.currentItem.clone():this.currentItem;d.parents("body").length||a(c.appendTo!="parent"?c.appendTo:this.currentItem[0].parentNode)[0].appendChild(d[0]),d[0]==this.currentItem[0]&&(this._storedCSS={width:this.currentItem[0].style.width,height:this.currentItem[0].style.height,position:this.currentItem.css("position"),top:this.currentItem.css("top"),left:this.currentItem.css("left")}),(d[0].style.width==""||c.forceHelperSize)&&d.width(this.currentItem.width()),(d[0].style.height==""||c.forceHelperSize)&&d.height(this.currentItem.height());return d},_adjustOffsetFromHelper:function(b){typeof b=="string"&&(b=b.split(" ")),a.isArray(b)&&(b={left:+b[0],top:+b[1]||0}),"left"in b&&(this.offset.click.left=b.left+this.margins.left),"right"in b&&(this.offset.click.left=this.helperProportions.width-b.right+this.margins.left),"top"in b&&(this.offset.click.top=b.top+this.margins.top),"bottom"in b&&(this.offset.click.top=this.helperProportions.height-b.bottom+this.margins.top)},_getParentOffset:function(){this.offsetParent=this.helper.offsetParent();var b=this.offsetParent.offset();this.cssPosition=="absolute"&&this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0])&&(b.left+=this.scrollParent.scrollLeft(),b.top+=this.scrollParent.scrollTop());if(this.offsetParent[0]==document.body||this.offsetParent[0].tagName&&this.offsetParent[0].tagName.toLowerCase()=="html"&&a.browser.msie)b={top:0,left:0};return{top:b.top+(parseInt(this.offsetParent.css("borderTopWidth"),10)||0),left:b.left+(parseInt(this.offsetParent.css("borderLeftWidth"),10)||0)}},_getRelativeOffset:function(){if(this.cssPosition=="relative"){var a=this.currentItem.position();return{top:a.top-(parseInt(this.helper.css("top"),10)||0)+this.scrollParent.scrollTop(),left:a.left-(parseInt(this.helper.css("left"),10)||0)+this.scrollParent.scrollLeft()}}return{top:0,left:0}},_cacheMargins:function(){this.margins={left:parseInt(this.currentItem.css("marginLeft"),10)||0,top:parseInt(this.currentItem.css("marginTop"),10)||0}},_cacheHelperProportions:function(){this.helperProportions={width:this.helper.outerWidth(),height:this.helper.outerHeight()}},_setContainment:function(){var b=this.options;b.containment=="parent"&&(b.containment=this.helper[0].parentNode);if(b.containment=="document"||b.containment=="window")this.containment=[0-this.offset.relative.left-this.offset.parent.left,0-this.offset.relative.top-this.offset.parent.top,a(b.containment=="document"?document:window).width()-this.helperProportions.width-this.margins.left,(a(b.containment=="document"?document:window).height()||document.body.parentNode.scrollHeight)-this.helperProportions.height-this.margins.top];if(!/^(document|window|parent)$/.test(b.containment)){var c=a(b.containment)[0],d=a(b.containment).offset(),e=a(c).css("overflow")!="hidden";this.containment=[d.left+(parseInt(a(c).css("borderLeftWidth"),10)||0)+(parseInt(a(c).css("paddingLeft"),10)||0)-this.margins.left,d.top+(parseInt(a(c).css("borderTopWidth"),10)||0)+(parseInt(a(c).css("paddingTop"),10)||0)-this.margins.top,d.left+(e?Math.max(c.scrollWidth,c.offsetWidth):c.offsetWidth)-(parseInt(a(c).css("borderLeftWidth"),10)||0)-(parseInt(a(c).css("paddingRight"),10)||0)-this.helperProportions.width-this.margins.left,d.top+(e?Math.max(c.scrollHeight,c.offsetHeight):c.offsetHeight)-(parseInt(a(c).css("borderTopWidth"),10)||0)-(parseInt(a(c).css("paddingBottom"),10)||0)-this.helperProportions.height-this.margins.top]}},_convertPositionTo:function(b,c){c||(c=this.position);var d=b=="absolute"?1:-1,e=this.options,f=this.cssPosition=="absolute"&&(this.scrollParent[0]==document||!a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,g=/(html|body)/i.test(f[0].tagName);return{top:c.top+this.offset.relative.top*d+this.offset.parent.top*d-(a.browser.safari&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollTop():g?0:f.scrollTop())*d),left:c.left+this.offset.relative.left*d+this.offset.parent.left*d-(a.browser.safari&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():g?0:f.scrollLeft())*d)}},_generatePosition:function(b){var c=this.options,d=this.cssPosition=="absolute"&&(this.scrollParent[0]==document||!a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,e=/(html|body)/i.test(d[0].tagName);this.cssPosition=="relative"&&(this.scrollParent[0]==document||this.scrollParent[0]==this.offsetParent[0])&&(this.offset.relative=this._getRelativeOffset());var f=b.pageX,g=b.pageY;if(this.originalPosition){this.containment&&(b.pageX-this.offset.click.left<this.containment[0]&&(f=this.containment[0]+this.offset.click.left),b.pageY-this.offset.click.top<this.containment[1]&&(g=this.containment[1]+this.offset.click.top),b.pageX-this.offset.click.left>this.containment[2]&&(f=this.containment[2]+this.offset.click.left),b.pageY-this.offset.click.top>this.containment[3]&&(g=this.containment[3]+this.offset.click.top));if(c.grid){var h=this.originalPageY+Math.round((g-this.originalPageY)/c.grid[1])*c.grid[1];g=this.containment?h-this.offset.click.top<this.containment[1]||h-this.offset.click.top>this.containment[3]?h-this.offset.click.top<this.containment[1]?h+c.grid[1]:h-c.grid[1]:h:h;var i=this.originalPageX+Math.round((f-this.originalPageX)/c.grid[0])*c.grid[0];f=this.containment?i-this.offset.click.left<this.containment[0]||i-this.offset.click.left>this.containment[2]?i-this.offset.click.left<this.containment[0]?i+c.grid[0]:i-c.grid[0]:i:i}}return{top:g-this.offset.click.top-this.offset.relative.top-this.offset.parent.top+(a.browser.safari&&this.cssPosition=="fixed"?0:this.cssPosition=="fixed"?-this.scrollParent.scrollTop():e?0:d.scrollTop()),left:f-this.offset.click.left-this.offset.relative.left-this.offset.parent.left+(a.browser.safari&&this.cssPosition=="fixed"?0:this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():e?0:d.scrollLeft())}},_rearrange:function(a,b,c,d){c?c[0].appendChild(this.placeholder[0]):b.item[0].parentNode.insertBefore(this.placeholder[0],this.direction=="down"?b.item[0]:b.item[0].nextSibling),this.counter=this.counter?++this.counter:1;var e=this,f=this.counter;window.setTimeout(function(){f==e.counter&&e.refreshPositions(!d)},0)},_clear:function(b,c){this.reverting=!1;var d=[],e=this;!this._noFinalSort&&this.currentItem.parent().length&&this.placeholder.before(this.currentItem),this._noFinalSort=null;if(this.helper[0]==this.currentItem[0]){for(var f in this._storedCSS)if(this._storedCSS[f]=="auto"||this._storedCSS[f]=="static")this._storedCSS[f]="";this.currentItem.css(this._storedCSS).removeClass("ui-sortable-helper")}else this.currentItem.show();this.fromOutside&&!c&&d.push(function(a){this._trigger("receive",a,this._uiHash(this.fromOutside))}),(this.fromOutside||this.domPosition.prev!=this.currentItem.prev().not(".ui-sortable-helper")[0]||this.domPosition.parent!=this.currentItem.parent()[0])&&!c&&d.push(function(a){this._trigger("update",a,this._uiHash())});if(!a.ui.contains(this.element[0],this.currentItem[0])){c||d.push(function(a){this._trigger("remove",a,this._uiHash())});for(var f=this.containers.length-1;f>=0;f--)a.ui.contains(this.containers[f].element[0],this.currentItem[0])&&!c&&(d.push(function(a){return function(b){a._trigger("receive",b,this._uiHash(this))}}.call(this,this.containers[f])),d.push(function(a){return function(b){a._trigger("update",b,this._uiHash(this))}}.call(this,this.containers[f])))}for(var f=this.containers.length-1;f>=0;f--)c||d.push(function(a){return function(b){a._trigger("deactivate",b,this._uiHash(this))}}.call(this,this.containers[f])),this.containers[f].containerCache.over&&(d.push(function(a){return function(b){a._trigger("out",b,this._uiHash(this))}}.call(this,this.containers[f])),this.containers[f].containerCache.over=0);this._storedCursor&&a("body").css("cursor",this._storedCursor),this._storedOpacity&&this.helper.css("opacity",this._storedOpacity),this._storedZIndex&&this.helper.css("zIndex",this._storedZIndex=="auto"?"":this._storedZIndex),this.dragging=!1;if(this.cancelHelperRemoval){if(!c){this._trigger("beforeStop",b,this._uiHash());for(var f=0;f<d.length;f++)d[f].call(this,b);this._trigger("stop",b,this._uiHash())}return!1}c||this._trigger("beforeStop",b,this._uiHash()),this.placeholder[0].parentNode.removeChild(this.placeholder[0]),this.helper[0]!=this.currentItem[0]&&this.helper.remove(),this.helper=null;if(!c){for(var f=0;f<d.length;f++)d[f].call(this,b);this._trigger("stop",b,this._uiHash())}this.fromOutside=!1;return!0},_trigger:function(){a.Widget.prototype._trigger.apply(this,arguments)===!1&&this.cancel()},_uiHash:function(b){var c=b||this;return{helper:c.helper,placeholder:c.placeholder||a([]),position:c.position,originalPosition:c.originalPosition,offset:c.positionAbs,item:c.currentItem,sender:b?b.element:null}}}),a.extend(a.ui.sortable,{version:"1.8.17"})})(jQuery);/*
 * jQuery UI Accordion 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Accordion
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.widget.js
 */(function(a,b){a.widget("ui.accordion",{options:{active:0,animated:"slide",autoHeight:!0,clearStyle:!1,collapsible:!1,event:"click",fillSpace:!1,header:"> li > :first-child,> :not(li):even",icons:{header:"ui-icon-triangle-1-e",headerSelected:"ui-icon-triangle-1-s"},navigation:!1,navigationFilter:function(){return this.href.toLowerCase()===location.href.toLowerCase()}},_create:function(){var b=this,c=b.options;b.running=0,b.element.addClass("ui-accordion ui-widget ui-helper-reset").children("li").addClass("ui-accordion-li-fix"),b.headers=b.element.find(c.header).addClass("ui-accordion-header ui-helper-reset ui-state-default ui-corner-all").bind("mouseenter.accordion",function(){c.disabled||a(this).addClass("ui-state-hover")}).bind("mouseleave.accordion",function(){c.disabled||a(this).removeClass("ui-state-hover")}).bind("focus.accordion",function(){c.disabled||a(this).addClass("ui-state-focus")}).bind("blur.accordion",function(){c.disabled||a(this).removeClass("ui-state-focus")}),b.headers.next().addClass("ui-accordion-content ui-helper-reset ui-widget-content ui-corner-bottom");if(c.navigation){var d=b.element.find("a").filter(c.navigationFilter).eq(0);if(d.length){var e=d.closest(".ui-accordion-header");e.length?b.active=e:b.active=d.closest(".ui-accordion-content").prev()}}b.active=b._findActive(b.active||c.active).addClass("ui-state-default ui-state-active").toggleClass("ui-corner-all").toggleClass("ui-corner-top"),b.active.next().addClass("ui-accordion-content-active"),b._createIcons(),b.resize(),b.element.attr("role","tablist"),b.headers.attr("role","tab").bind("keydown.accordion",function(a){return b._keydown(a)}).next().attr("role","tabpanel"),b.headers.not(b.active||"").attr({"aria-expanded":"false","aria-selected":"false",tabIndex:-1}).next().hide(),b.active.length?b.active.attr({"aria-expanded":"true","aria-selected":"true",tabIndex:0}):b.headers.eq(0).attr("tabIndex",0),a.browser.safari||b.headers.find("a").attr("tabIndex",-1),c.event&&b.headers.bind(c.event.split(" ").join(".accordion ")+".accordion",function(a){b._clickHandler.call(b,a,this),a.preventDefault()})},_createIcons:function(){var b=this.options;b.icons&&(a("<span></span>").addClass("ui-icon "+b.icons.header).prependTo(this.headers),this.active.children(".ui-icon").toggleClass(b.icons.header).toggleClass(b.icons.headerSelected),this.element.addClass("ui-accordion-icons"))},_destroyIcons:function(){this.headers.children(".ui-icon").remove(),this.element.removeClass("ui-accordion-icons")},destroy:function(){var b=this.options;this.element.removeClass("ui-accordion ui-widget ui-helper-reset").removeAttr("role"),this.headers.unbind(".accordion").removeClass("ui-accordion-header ui-accordion-disabled ui-helper-reset ui-state-default ui-corner-all ui-state-active ui-state-disabled ui-corner-top").removeAttr("role").removeAttr("aria-expanded").removeAttr("aria-selected").removeAttr("tabIndex"),this.headers.find("a").removeAttr("tabIndex"),this._destroyIcons();var c=this.headers.next().css("display","").removeAttr("role").removeClass("ui-helper-reset ui-widget-content ui-corner-bottom ui-accordion-content ui-accordion-content-active ui-accordion-disabled ui-state-disabled");(b.autoHeight||b.fillHeight)&&c.css("height","");return a.Widget.prototype.destroy.call(this)},_setOption:function(b,c){a.Widget.prototype._setOption.apply(this,arguments),b=="active"&&this.activate(c),b=="icons"&&(this._destroyIcons(),c&&this._createIcons()),b=="disabled"&&this.headers.add(this.headers.next())[c?"addClass":"removeClass"]("ui-accordion-disabled ui-state-disabled")},_keydown:function(b){if(!(this.options.disabled||b.altKey||b.ctrlKey)){var c=a.ui.keyCode,d=this.headers.length,e=this.headers.index(b.target),f=!1;switch(b.keyCode){case c.RIGHT:case c.DOWN:f=this.headers[(e+1)%d];break;case c.LEFT:case c.UP:f=this.headers[(e-1+d)%d];break;case c.SPACE:case c.ENTER:this._clickHandler({target:b.target},b.target),b.preventDefault()}if(f){a(b.target).attr("tabIndex",-1),a(f).attr("tabIndex",0),f.focus();return!1}return!0}},resize:function(){var b=this.options,c;if(b.fillSpace){if(a.browser.msie){var d=this.element.parent().css("overflow");this.element.parent().css("overflow","hidden")}c=this.element.parent().height(),a.browser.msie&&this.element.parent().css("overflow",d),this.headers.each(function(){c-=a(this).outerHeight(!0)}),this.headers.next().each(function(){a(this).height(Math.max(0,c-a(this).innerHeight()+a(this).height()))}).css("overflow","auto")}else b.autoHeight&&(c=0,this.headers.next().each(function(){c=Math.max(c,a(this).height("").height())}).height(c));return this},activate:function(a){this.options.active=a;var b=this._findActive(a)[0];this._clickHandler({target:b},b);return this},_findActive:function(b){return b?typeof b=="number"?this.headers.filter(":eq("+b+")"):this.headers.not(this.headers.not(b)):b===!1?a([]):this.headers.filter(":eq(0)")},_clickHandler:function(b,c){var d=this.options;if(!d.disabled){if(!b.target){if(!d.collapsible)return;this.active.removeClass("ui-state-active ui-corner-top").addClass("ui-state-default ui-corner-all").children(".ui-icon").removeClass(d.icons.headerSelected).addClass(d.icons.header),this.active.next().addClass("ui-accordion-content-active");var e=this.active.next(),f={options:d,newHeader:a([]),oldHeader:d.active,newContent:a([]),oldContent:e},g=this.active=a([]);this._toggle(g,e,f);return}var h=a(b.currentTarget||c),i=h[0]===this.active[0];d.active=d.collapsible&&i?!1:this.headers.index(h);if(this.running||!d.collapsible&&i)return;var j=this.active,g=h.next(),e=this.active.next(),f={options:d,newHeader:i&&d.collapsible?a([]):h,oldHeader:this.active,newContent:i&&d.collapsible?a([]):g,oldContent:e},k=this.headers.index(this.active[0])>this.headers.index(h[0]);this.active=i?a([]):h,this._toggle(g,e,f,i,k),j.removeClass("ui-state-active ui-corner-top").addClass("ui-state-default ui-corner-all").children(".ui-icon").removeClass(d.icons.headerSelected).addClass(d.icons.header),i||(h.removeClass("ui-state-default ui-corner-all").addClass("ui-state-active ui-corner-top").children(".ui-icon").removeClass(d.icons.header).addClass(d.icons.headerSelected),h.next().addClass("ui-accordion-content-active"));return}},_toggle:function(b,c,d,e,f){var g=this,h=g.options;g.toShow=b,g.toHide=c,g.data=d;var i=function(){if(!!g)return g._completed.apply(g,arguments)};g._trigger("changestart",null,g.data),g.running=c.size()===0?b.size():c.size();if(h.animated){var j={};h.collapsible&&e?j={toShow:a([]),toHide:c,complete:i,down:f,autoHeight:h.autoHeight||h.fillSpace}:j={toShow:b,toHide:c,complete:i,down:f,autoHeight:h.autoHeight||h.fillSpace},h.proxied||(h.proxied=h.animated),h.proxiedDuration||(h.proxiedDuration=h.duration),h.animated=a.isFunction(h.proxied)?h.proxied(j):h.proxied,h.duration=a.isFunction(h.proxiedDuration)?h.proxiedDuration(j):h.proxiedDuration;var k=a.ui.accordion.animations,l=h.duration,m=h.animated;m&&!k[m]&&!a.easing[m]&&(m="slide"),k[m]||(k[m]=function(a){this.slide(a,{easing:m,duration:l||700})}),k[m](j)}else h.collapsible&&e?b.toggle():(c.hide(),b.show()),i(!0);c.prev().attr({"aria-expanded":"false","aria-selected":"false",tabIndex:-1}).blur(),b.prev().attr({"aria-expanded":"true","aria-selected":"true",tabIndex:0}).focus()},_completed:function(a){this.running=a?0:--this.running;this.running||(this.options.clearStyle&&this.toShow.add(this.toHide).css({height:"",overflow:""}),this.toHide.removeClass("ui-accordion-content-active"),this.toHide.length&&(this.toHide.parent()[0].className=this.toHide.parent()[0].className),this._trigger("change",null,this.data))}}),a.extend(a.ui.accordion,{version:"1.8.17",animations:{slide:function(b,c){b=a.extend({easing:"swing",duration:300},b,c);if(!b.toHide.size())b.toShow.animate({height:"show",paddingTop:"show",paddingBottom:"show"},b);else{if(!b.toShow.size()){b.toHide.animate({height:"hide",paddingTop:"hide",paddingBottom:"hide"},b);return}var d=b.toShow.css("overflow"),e=0,f={},g={},h=["height","paddingTop","paddingBottom"],i,j=b.toShow;i=j[0].style.width,j.width(j.parent().width()-parseFloat(j.css("paddingLeft"))-parseFloat(j.css("paddingRight"))-(parseFloat(j.css("borderLeftWidth"))||0)-(parseFloat(j.css("borderRightWidth"))||0)),a.each(h,function(c,d){g[d]="hide";var e=(""+a.css(b.toShow[0],d)).match(/^([\d+-.]+)(.*)$/);f[d]={value:e[1],unit:e[2]||"px"}}),b.toShow.css({height:0,overflow:"hidden"}).show(),b.toHide.filter(":hidden").each(b.complete).end().filter(":visible").animate(g,{step:function(a,c){c.prop=="height"&&(e=c.end-c.start===0?0:(c.now-c.start)/(c.end-c.start)),b.toShow[0].style[c.prop]=e*f[c.prop].value+f[c.prop].unit},duration:b.duration,easing:b.easing,complete:function(){b.autoHeight||b.toShow.css("height",""),b.toShow.css({width:i,overflow:d}),b.complete()}})}},bounceslide:function(a){this.slide(a,{easing:a.down?"easeOutBounce":"swing",duration:a.down?1e3:200})}}})})(jQuery);/*
 * jQuery UI Autocomplete 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Autocomplete
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.widget.js
 *    jquery.ui.position.js
 */(function(a,b){var c=0;a.widget("ui.autocomplete",{options:{appendTo:"body",autoFocus:!1,delay:300,minLength:1,position:{my:"left top",at:"left bottom",collision:"none"},source:null},pending:0,_create:function(){var b=this,c=this.element[0].ownerDocument,d;this.element.addClass("ui-autocomplete-input").attr("autocomplete","off").attr({role:"textbox","aria-autocomplete":"list","aria-haspopup":"true"}).bind("keydown.autocomplete",function(c){if(!b.options.disabled&&!b.element.propAttr("readOnly")){d=!1;var e=a.ui.keyCode;switch(c.keyCode){case e.PAGE_UP:b._move("previousPage",c);break;case e.PAGE_DOWN:b._move("nextPage",c);break;case e.UP:b._move("previous",c),c.preventDefault();break;case e.DOWN:b._move("next",c),c.preventDefault();break;case e.ENTER:case e.NUMPAD_ENTER:b.menu.active&&(d=!0,c.preventDefault());case e.TAB:if(!b.menu.active)return;b.menu.select(c);break;case e.ESCAPE:b.element.val(b.term),b.close(c);break;default:clearTimeout(b.searching),b.searching=setTimeout(function(){b.term!=b.element.val()&&(b.selectedItem=null,b.search(null,c))},b.options.delay)}}}).bind("keypress.autocomplete",function(a){d&&(d=!1,a.preventDefault())}).bind("focus.autocomplete",function(){b.options.disabled||(b.selectedItem=null,b.previous=b.element.val())}).bind("blur.autocomplete",function(a){b.options.disabled||(clearTimeout(b.searching),b.closing=setTimeout(function(){b.close(a),b._change(a)},150))}),this._initSource(),this.response=function(){return b._response.apply(b,arguments)},this.menu=a("<ul></ul>").addClass("ui-autocomplete").appendTo(a(this.options.appendTo||"body",c)[0]).mousedown(function(c){var d=b.menu.element[0];a(c.target).closest(".ui-menu-item").length||setTimeout(function(){a(document).one("mousedown",function(c){c.target!==b.element[0]&&c.target!==d&&!a.ui.contains(d,c.target)&&b.close()})},1),setTimeout(function(){clearTimeout(b.closing)},13)}).menu({focus:function(a,c){var d=c.item.data("item.autocomplete");!1!==b._trigger("focus",a,{item:d})&&/^key/.test(a.originalEvent.type)&&b.element.val(d.value)},selected:function(a,d){var e=d.item.data("item.autocomplete"),f=b.previous;b.element[0]!==c.activeElement&&(b.element.focus(),b.previous=f,setTimeout(function(){b.previous=f,b.selectedItem=e},1)),!1!==b._trigger("select",a,{item:e})&&b.element.val(e.value),b.term=b.element.val(),b.close(a),b.selectedItem=e},blur:function(a,c){b.menu.element.is(":visible")&&b.element.val()!==b.term&&b.element.val(b.term)}}).zIndex(this.element.zIndex()+1).css({top:0,left:0}).hide().data("menu"),a.fn.bgiframe&&this.menu.element.bgiframe(),b.beforeunloadHandler=function(){b.element.removeAttr("autocomplete")},a(window).bind("beforeunload",b.beforeunloadHandler)},destroy:function(){this.element.removeClass("ui-autocomplete-input").removeAttr("autocomplete").removeAttr("role").removeAttr("aria-autocomplete").removeAttr("aria-haspopup"),this.menu.element.remove(),a(window).unbind("beforeunload",this.beforeunloadHandler),a.Widget.prototype.destroy.call(this)},_setOption:function(b,c){a.Widget.prototype._setOption.apply(this,arguments),b==="source"&&this._initSource(),b==="appendTo"&&this.menu.element.appendTo(a(c||"body",this.element[0].ownerDocument)[0]),b==="disabled"&&c&&this.xhr&&this.xhr.abort()},_initSource:function(){var b=this,d,e;a.isArray(this.options.source)?(d=this.options.source,this.source=function(b,c){c(a.ui.autocomplete.filter(d,b.term))}):typeof this.options.source=="string"?(e=this.options.source,this.source=function(d,f){b.xhr&&b.xhr.abort(),b.xhr=a.ajax({url:e,data:d,dataType:"json",autocompleteRequest:++c,success:function(a,b){this.autocompleteRequest===c&&f(a)},error:function(){this.autocompleteRequest===c&&f([])}})}):this.source=this.options.source},search:function(a,b){a=a!=null?a:this.element.val(),this.term=this.element.val();if(a.length<this.options.minLength)return this.close(b);clearTimeout(this.closing);if(this._trigger("search",b)!==!1)return this._search(a)},_search:function(a){this.pending++,this.element.addClass("ui-autocomplete-loading"),this.source({term:a},this.response)},_response:function(a){!this.options.disabled&&a&&a.length?(a=this._normalize(a),this._suggest(a),this._trigger("open")):this.close(),this.pending--,this.pending||this.element.removeClass("ui-autocomplete-loading")},close:function(a){clearTimeout(this.closing),this.menu.element.is(":visible")&&(this.menu.element.hide(),this.menu.deactivate(),this._trigger("close",a))},_change:function(a){this.previous!==this.element.val()&&this._trigger("change",a,{item:this.selectedItem})},_normalize:function(b){if(b.length&&b[0].label&&b[0].value)return b;return a.map(b,function(b){if(typeof b=="string")return{label:b,value:b};return a.extend({label:b.label||b.value,value:b.value||b.label},b)})},_suggest:function(b){var c=this.menu.element.empty().zIndex(this.element.zIndex()+1);this._renderMenu(c,b),this.menu.deactivate(),this.menu.refresh(),c.show(),this._resizeMenu(),c.position(a.extend({of:this.element},this.options.position)),this.options.autoFocus&&this.menu.next(new a.Event("mouseover"))},_resizeMenu:function(){var a=this.menu.element;a.outerWidth(Math.max(a.width("").outerWidth()+1,this.element.outerWidth()))},_renderMenu:function(b,c){var d=this;a.each(c,function(a,c){d._renderItem(b,c)})},_renderItem:function(b,c){return a("<li></li>").data("item.autocomplete",c).append(a("<a></a>").text(c.label)).appendTo(b)},_move:function(a,b){if(!this.menu.element.is(":visible"))this.search(null,b);else{if(this.menu.first()&&/^previous/.test(a)||this.menu.last()&&/^next/.test(a)){this.element.val(this.term),this.menu.deactivate();return}this.menu[a](b)}},widget:function(){return this.menu.element}}),a.extend(a.ui.autocomplete,{escapeRegex:function(a){return a.replace(/[-[\]{}()*+?.,\\^$|#\s]/g,"\\$&")},filter:function(b,c){var d=new RegExp(a.ui.autocomplete.escapeRegex(c),"i");return a.grep(b,function(a){return d.test(a.label||a.value||a)})}})})(jQuery),function(a){a.widget("ui.menu",{_create:function(){var b=this;this.element.addClass("ui-menu ui-widget ui-widget-content ui-corner-all").attr({role:"listbox","aria-activedescendant":"ui-active-menuitem"}).click(function(c){!a(c.target).closest(".ui-menu-item a").length||(c.preventDefault(),b.select(c))}),this.refresh()},refresh:function(){var b=this,c=this.element.children("li:not(.ui-menu-item):has(a)").addClass("ui-menu-item").attr("role","menuitem");c.children("a").addClass("ui-corner-all").attr("tabindex",-1).mouseenter(function(c){b.activate(c,a(this).parent())}).mouseleave(function(){b.deactivate()})},activate:function(a,b){this.deactivate();if(this.hasScroll()){var c=b.offset().top-this.element.offset().top,d=this.element.scrollTop(),e=this.element.height();c<0?this.element.scrollTop(d+c):c>=e&&this.element.scrollTop(d+c-e+b.height())}this.active=b.eq(0).children("a").addClass("ui-state-hover").attr("id","ui-active-menuitem").end(),this._trigger("focus",a,{item:b})},deactivate:function(){!this.active||(this.active.children("a").removeClass("ui-state-hover").removeAttr("id"),this._trigger("blur"),this.active=null)},next:function(a){this.move("next",".ui-menu-item:first",a)},previous:function(a){this.move("prev",".ui-menu-item:last",a)},first:function(){return this.active&&!this.active.prevAll(".ui-menu-item").length},last:function(){return this.active&&!this.active.nextAll(".ui-menu-item").length},move:function(a,b,c){if(!this.active)this.activate(c,this.element.children(b));else{var d=this.active[a+"All"](".ui-menu-item").eq(0);d.length?this.activate(c,d):this.activate(c,this.element.children(b))}},nextPage:function(b){if(this.hasScroll()){if(!this.active||this.last()){this.activate(b,this.element.children(".ui-menu-item:first"));return}var c=this.active.offset().top,d=this.element.height(),e=this.element.children(".ui-menu-item").filter(function(){var b=a(this).offset().top-c-d+a(this).height();return b<10&&b>-10});e.length||(e=this.element.children(".ui-menu-item:last")),this.activate(b,e)}else this.activate(b,this.element.children(".ui-menu-item").filter(!this.active||this.last()?":first":":last"))},previousPage:function(b){if(this.hasScroll()){if(!this.active||this.first()){this.activate(b,this.element.children(".ui-menu-item:last"));return}var c=this.active.offset().top,d=this.element.height();result=this.element.children(".ui-menu-item").filter(function(){var b=a(this).offset().top-c+d-a(this).height();return b<10&&b>-10}),result.length||(result=this.element.children(".ui-menu-item:first")),this.activate(b,result)}else this.activate(b,this.element.children(".ui-menu-item").filter(!this.active||this.first()?":last":":first"))},hasScroll:function(){return this.element.height()<this.element[a.fn.prop?"prop":"attr"]("scrollHeight")},select:function(a){this._trigger("selected",a,{item:this.active})}})}(jQuery);/*
 * jQuery UI Button 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Button
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.widget.js
 */(function(a,b){var c,d,e,f,g="ui-button ui-widget ui-state-default ui-corner-all",h="ui-state-hover ui-state-active ",i="ui-button-icons-only ui-button-icon-only ui-button-text-icons ui-button-text-icon-primary ui-button-text-icon-secondary ui-button-text-only",j=function(){var b=a(this).find(":ui-button");setTimeout(function(){b.button("refresh")},1)},k=function(b){var c=b.name,d=b.form,e=a([]);c&&(d?e=a(d).find("[name='"+c+"']"):e=a("[name='"+c+"']",b.ownerDocument).filter(function(){return!this.form}));return e};a.widget("ui.button",{options:{disabled:null,text:!0,label:null,icons:{primary:null,secondary:null}},_create:function(){this.element.closest("form").unbind("reset.button").bind("reset.button",j),typeof this.options.disabled!="boolean"&&(this.options.disabled=this.element.propAttr("disabled")),this._determineButtonType(),this.hasTitle=!!this.buttonElement.attr("title");var b=this,h=this.options,i=this.type==="checkbox"||this.type==="radio",l="ui-state-hover"+(i?"":" ui-state-active"),m="ui-state-focus";h.label===null&&(h.label=this.buttonElement.html()),this.element.is(":disabled")&&(h.disabled=!0),this.buttonElement.addClass(g).attr("role","button").bind("mouseenter.button",function(){h.disabled||(a(this).addClass("ui-state-hover"),this===c&&a(this).addClass("ui-state-active"))}).bind("mouseleave.button",function(){h.disabled||a(this).removeClass(l)}).bind("click.button",function(a){h.disabled&&(a.preventDefault(),a.stopImmediatePropagation())}),this.element.bind("focus.button",function(){b.buttonElement.addClass(m)}).bind("blur.button",function(){b.buttonElement.removeClass(m)}),i&&(this.element.bind("change.button",function(){f||b.refresh()}),this.buttonElement.bind("mousedown.button",function(a){h.disabled||(f=!1,d=a.pageX,e=a.pageY)}).bind("mouseup.button",function(a){!h.disabled&&(d!==a.pageX||e!==a.pageY)&&(f=!0)})),this.type==="checkbox"?this.buttonElement.bind("click.button",function(){if(h.disabled||f)return!1;a(this).toggleClass("ui-state-active"),b.buttonElement.attr("aria-pressed",b.element[0].checked)}):this.type==="radio"?this.buttonElement.bind("click.button",function(){if(h.disabled||f)return!1;a(this).addClass("ui-state-active"),b.buttonElement.attr("aria-pressed","true");var c=b.element[0];k(c).not(c).map(function(){return a(this).button("widget")[0]}).removeClass("ui-state-active").attr("aria-pressed","false")}):(this.buttonElement.bind("mousedown.button",function(){if(h.disabled)return!1;a(this).addClass("ui-state-active"),c=this,a(document).one("mouseup",function(){c=null})}).bind("mouseup.button",function(){if(h.disabled)return!1;a(this).removeClass("ui-state-active")}).bind("keydown.button",function(b){if(h.disabled)return!1;(b.keyCode==a.ui.keyCode.SPACE||b.keyCode==a.ui.keyCode.ENTER)&&a(this).addClass("ui-state-active")}).bind("keyup.button",function(){a(this).removeClass("ui-state-active")}),this.buttonElement.is("a")&&this.buttonElement.keyup(function(b){b.keyCode===a.ui.keyCode.SPACE&&a(this).click()})),this._setOption("disabled",h.disabled),this._resetButton()},_determineButtonType:function(){this.element.is(":checkbox")?this.type="checkbox":this.element.is(":radio")?this.type="radio":this.element.is("input")?this.type="input":this.type="button";if(this.type==="checkbox"||this.type==="radio"){var a=this.element.parents().filter(":last"),b="label[for='"+this.element.attr("id")+"']";this.buttonElement=a.find(b),this.buttonElement.length||(a=a.length?a.siblings():this.element.siblings(),this.buttonElement=a.filter(b),this.buttonElement.length||(this.buttonElement=a.find(b))),this.element.addClass("ui-helper-hidden-accessible");var c=this.element.is(":checked");c&&this.buttonElement.addClass("ui-state-active"),this.buttonElement.attr("aria-pressed",c)}else this.buttonElement=this.element},widget:function(){return this.buttonElement},destroy:function(){this.element.removeClass("ui-helper-hidden-accessible"),this.buttonElement.removeClass(g+" "+h+" "+i).removeAttr("role").removeAttr("aria-pressed").html(this.buttonElement.find(".ui-button-text").html()),this.hasTitle||this.buttonElement.removeAttr("title"),a.Widget.prototype.destroy.call(this)},_setOption:function(b,c){a.Widget.prototype._setOption.apply(this,arguments);b==="disabled"?c?this.element.propAttr("disabled",!0):this.element.propAttr("disabled",!1):this._resetButton()},refresh:function(){var b=this.element.is(":disabled");b!==this.options.disabled&&this._setOption("disabled",b),this.type==="radio"?k(this.element[0]).each(function(){a(this).is(":checked")?a(this).button("widget").addClass("ui-state-active").attr("aria-pressed","true"):a(this).button("widget").removeClass("ui-state-active").attr("aria-pressed","false")}):this.type==="checkbox"&&(this.element.is(":checked")?this.buttonElement.addClass("ui-state-active").attr("aria-pressed","true"):this.buttonElement.removeClass("ui-state-active").attr("aria-pressed","false"))},_resetButton:function(){if(this.type==="input")this.options.label&&this.element.val(this.options.label);else{var b=this.buttonElement.removeClass(i),c=a("<span></span>",this.element[0].ownerDocument).addClass("ui-button-text").html(this.options.label).appendTo(b.empty()).text(),d=this.options.icons,e=d.primary&&d.secondary,f=[];d.primary||d.secondary?(this.options.text&&f.push("ui-button-text-icon"+(e?"s":d.primary?"-primary":"-secondary")),d.primary&&b.prepend("<span class='ui-button-icon-primary ui-icon "+d.primary+"'></span>"),d.secondary&&b.append("<span class='ui-button-icon-secondary ui-icon "+d.secondary+"'></span>"),this.options.text||(f.push(e?"ui-button-icons-only":"ui-button-icon-only"),this.hasTitle||b.attr("title",c))):f.push("ui-button-text-only"),b.addClass(f.join(" "))}}}),a.widget("ui.buttonset",{options:{items:":button, :submit, :reset, :checkbox, :radio, a, :data(button)"},_create:function(){this.element.addClass("ui-buttonset")},_init:function(){this.refresh()},_setOption:function(b,c){b==="disabled"&&this.buttons.button("option",b,c),a.Widget.prototype._setOption.apply(this,arguments)},refresh:function(){var b=this.element.css("direction")==="rtl";this.buttons=this.element.find(this.options.items).filter(":ui-button").button("refresh").end().not(":ui-button").button().end().map(function(){return a(this).button("widget")[0]}).removeClass("ui-corner-all ui-corner-left ui-corner-right").filter(":first").addClass(b?"ui-corner-right":"ui-corner-left").end().filter(":last").addClass(b?"ui-corner-left":"ui-corner-right").end().end()},destroy:function(){this.element.removeClass("ui-buttonset"),this.buttons.map(function(){return a(this).button("widget")[0]}).removeClass("ui-corner-left ui-corner-right").end().button("destroy"),a.Widget.prototype.destroy.call(this)}})})(jQuery);/*
 * jQuery UI Dialog 1.8.17
 *
 * Copyright 2011, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Dialog
 *
 * Depends:
 *    jquery.ui.core.js
 *    jquery.ui.widget.js
 *  jquery.ui.button.js
 *    jquery.ui.draggable.js
 *    jquery.ui.mouse.js
 *    jquery.ui.position.js
 *    jquery.ui.resizable.js
 */(function(a,b){var c="ui-dialog ui-widget ui-widget-content ui-corner-all ",d={buttons:!0,height:!0,maxHeight:!0,maxWidth:!0,minHeight:!0,minWidth:!0,width:!0},e={maxHeight:!0,maxWidth:!0,minHeight:!0,minWidth:!0},f=a.attrFn||{val:!0,css:!0,html:!0,text:!0,data:!0,width:!0,height:!0,offset:!0,click:!0};a.widget("ui.dialog",{options:{autoOpen:!0,buttons:{},closeOnEscape:!0,closeText:"close",dialogClass:"",draggable:!0,hide:null,height:"auto",maxHeight:!1,maxWidth:!1,minHeight:150,minWidth:150,modal:!1,position:{my:"center",at:"center",collision:"fit",using:function(b){var c=a(this).css(b).offset().top;c<0&&a(this).css("top",b.top-c)}},resizable:!0,show:null,stack:!0,title:"",width:300,zIndex:1e3},_create:function(){this.originalTitle=this.element.attr("title"),typeof this.originalTitle!="string"&&(this.originalTitle=""),this.options.title=this.options.title||this.originalTitle;var b=this,d=b.options,e=d.title||"&#160;",f=a.ui.dialog.getTitleId(b.element),g=(b.uiDialog=a("<div></div>")).appendTo(document.body).hide().addClass(c+d.dialogClass).css({zIndex:d.zIndex}).attr("tabIndex",-1).css("outline",0).keydown(function(c){d.closeOnEscape&&!c.isDefaultPrevented()&&c.keyCode&&c.keyCode===a.ui.keyCode.ESCAPE&&(b.close(c),c.preventDefault())}).attr({role:"dialog","aria-labelledby":f}).mousedown(function(a){b.moveToTop(!1,a)}),h=b.element.show().removeAttr("title").addClass("ui-dialog-content ui-widget-content").appendTo(g),i=(b.uiDialogTitlebar=a("<div></div>")).addClass("ui-dialog-titlebar ui-widget-header ui-corner-all ui-helper-clearfix").prependTo(g),j=a('<a href="#"></a>').addClass("ui-dialog-titlebar-close ui-corner-all").attr("role","button").hover(function(){j.addClass("ui-state-hover")},function(){j.removeClass("ui-state-hover")}).focus(function(){j.addClass("ui-state-focus")}).blur(function(){j.removeClass("ui-state-focus")}).click(function(a){b.close(a);return!1}).appendTo(i),k=(b.uiDialogTitlebarCloseText=a("<span></span>")).addClass("ui-icon ui-icon-closethick").text(d.closeText).appendTo(j),l=a("<span></span>").addClass("ui-dialog-title").attr("id",f).html(e).prependTo(i);a.isFunction(d.beforeclose)&&!a.isFunction(d.beforeClose)&&(d.beforeClose=d.beforeclose),i.find("*").add(i).disableSelection(),d.draggable&&a.fn.draggable&&b._makeDraggable(),d.resizable&&a.fn.resizable&&b._makeResizable(),b._createButtons(d.buttons),b._isOpen=!1,a.fn.bgiframe&&g.bgiframe()},_init:function(){this.options.autoOpen&&this.open()},destroy:function(){var a=this;a.overlay&&a.overlay.destroy(),a.uiDialog.hide(),a.element.unbind(".dialog").removeData("dialog").removeClass("ui-dialog-content ui-widget-content").hide().appendTo("body"),a.uiDialog.remove(),a.originalTitle&&a.element.attr("title",a.originalTitle);return a},widget:function(){return this.uiDialog},close:function(b){var c=this,d,e;if(!1!==c._trigger("beforeClose",b)){c.overlay&&c.overlay.destroy(),c.uiDialog.unbind("keypress.ui-dialog"),c._isOpen=!1,c.options.hide?c.uiDialog.hide(c.options.hide,function(){c._trigger("close",b)}):(c.uiDialog.hide(),c._trigger("close",b)),a.ui.dialog.overlay.resize(),c.options.modal&&(d=0,a(".ui-dialog").each(function(){this!==c.uiDialog[0]&&(e=a(this).css("z-index"),isNaN(e)||(d=Math.max(d,e)))}),a.ui.dialog.maxZ=d);return c}},isOpen:function(){return this._isOpen},moveToTop:function(b,c){var d=this,e=d.options,f;if(e.modal&&!b||!e.stack&&!e.modal)return d._trigger("focus",c);e.zIndex>a.ui.dialog.maxZ&&(a.ui.dialog.maxZ=e.zIndex),d.overlay&&(a.ui.dialog.maxZ+=1,d.overlay.$el.css("z-index",a.ui.dialog.overlay.maxZ=a.ui.dialog.maxZ)),f={scrollTop:d.element.scrollTop(),scrollLeft:d.element.scrollLeft()},a.ui.dialog.maxZ+=1,d.uiDialog.css("z-index",a.ui.dialog.maxZ),d.element.attr(f),d._trigger("focus",c);return d},open:function(){if(!this._isOpen){var b=this,c=b.options,d=b.uiDialog;b.overlay=c.modal?new a.ui.dialog.overlay(b):null,b._size(),b._position(c.position),d.show(c.show),b.moveToTop(!0),c.modal&&d.bind("keydown.ui-dialog",function(b){if(b.keyCode===a.ui.keyCode.TAB){var c=a(":tabbable",this),d=c.filter(":first"),e=c.filter(":last");if(b.target===e[0]&&!b.shiftKey){d.focus(1);return!1}if(b.target===d[0]&&b.shiftKey){e.focus(1);return!1}}}),a(b.element.find(":tabbable").get().concat(d.find(".ui-dialog-buttonpane :tabbable").get().concat(d.get()))).eq(0).focus(),b._isOpen=!0,b._trigger("open");return b}},_createButtons:function(b){var c=this,d=!1,e=a("<div></div>").addClass("ui-dialog-buttonpane ui-widget-content ui-helper-clearfix"),g=a("<div></div>").addClass("ui-dialog-buttonset").appendTo(e);c.uiDialog.find(".ui-dialog-buttonpane").remove(),typeof b=="object"&&b!==null&&a.each(b,function(){return!(d=!0)}),d&&(a.each(b,function(b,d){d=a.isFunction(d)?{click:d,text:b}:d;var e=a('<button type="button"></button>').click(function(){d.click.apply(c.element[0],arguments)}).appendTo(g);a.each(d,function(a,b){a!=="click"&&(a in f?e[a](b):e.attr(a,b))}),a.fn.button&&e.button()}),e.appendTo(c.uiDialog))},_makeDraggable:function(){function f(a){return{position:a.position,offset:a.offset}}var b=this,c=b.options,d=a(document),e;b.uiDialog.draggable({cancel:".ui-dialog-content, .ui-dialog-titlebar-close",handle:".ui-dialog-titlebar",containment:"document",start:function(d,g){e=c.height==="auto"?"auto":a(this).height(),a(this).height(a(this).height()).addClass("ui-dialog-dragging"),b._trigger("dragStart",d,f(g))},drag:function(a,c){b._trigger("drag",a,f(c))},stop:function(g,h){c.position=[h.position.left-d.scrollLeft(),h.position.top-d.scrollTop()],a(this).removeClass("ui-dialog-dragging").height(e),b._trigger("dragStop",g,f(h)),a.ui.dialog.overlay.resize()}})},_makeResizable:function(c){function h(a){return{originalPosition:a.originalPosition,originalSize:a.originalSize,position:a.position,size:a.size}}c=c===b?this.options.resizable:c;var d=this,e=d.options,f=d.uiDialog.css("position"),g=typeof c=="string"?c:"n,e,s,w,se,sw,ne,nw";d.uiDialog.resizable({cancel:".ui-dialog-content",containment:"document",alsoResize:d.element,maxWidth:e.maxWidth,maxHeight:e.maxHeight,minWidth:e.minWidth,minHeight:d._minHeight(),handles:g,start:function(b,c){a(this).addClass("ui-dialog-resizing"),d._trigger("resizeStart",b,h(c))},resize:function(a,b){d._trigger("resize",a,h(b))},stop:function(b,c){a(this).removeClass("ui-dialog-resizing"),e.height=a(this).height(),e.width=a(this).width(),d._trigger("resizeStop",b,h(c)),a.ui.dialog.overlay.resize()}}).css("position",f).find(".ui-resizable-se").addClass("ui-icon ui-icon-grip-diagonal-se")},_minHeight:function(){var a=this.options;return a.height==="auto"?a.minHeight:Math.min(a.minHeight,a.height)},_position:function(b){var c=[],d=[0,0],e;if(b){if(typeof b=="string"||typeof b=="object"&&"0"in b)c=b.split?b.split(" "):[b[0],b[1]],c.length===1&&(c[1]=c[0]),a.each(["left","top"],function(a,b){+c[a]===c[a]&&(d[a]=c[a],c[a]=b)}),b={my:c.join(" "),at:c.join(" "),offset:d.join(" ")};b=a.extend({},a.ui.dialog.prototype.options.position,b)}else b=a.ui.dialog.prototype.options.position;e=this.uiDialog.is(":visible"),e||this.uiDialog.show(),this.uiDialog.css({top:0,left:0}).position(a.extend({of:window},b)),e||this.uiDialog.hide()},_setOptions:function(b){var c=this,f={},g=!1;a.each(b,function(a,b){c._setOption(a,b),a in d&&(g=!0),a in e&&(f[a]=b)}),g&&this._size(),this.uiDialog.is(":data(resizable)")&&this.uiDialog.resizable("option",f)},_setOption:function(b,d){var e=this,f=e.uiDialog;switch(b){case"beforeclose":b="beforeClose";break;case"buttons":e._createButtons(d);break;case"closeText":e.uiDialogTitlebarCloseText.text(""+d);break;case"dialogClass":f.removeClass(e.options.dialogClass).addClass(c+d);break;case"disabled":d?f.addClass("ui-dialog-disabled"):f.removeClass("ui-dialog-disabled");break;case"draggable":var g=f.is(":data(draggable)");g&&!d&&f.draggable("destroy"),!g&&d&&e._makeDraggable();break;case"position":e._position(d);break;case"resizable":var h=f.is(":data(resizable)");h&&!d&&f.resizable("destroy"),h&&typeof d=="string"&&f.resizable("option","handles",d),!h&&d!==!1&&e._makeResizable(d);break;case"title":a(".ui-dialog-title",e.uiDialogTitlebar).html(""+(d||"&#160;"))}a.Widget.prototype._setOption.apply(e,arguments)},_size:function(){var b=this.options,c,d,e=this.uiDialog.is(":visible");this.element.show().css({width:"auto",minHeight:0,height:0}),b.minWidth>b.width&&(b.width=b.minWidth),c=this.uiDialog.css({height:"auto",width:b.width}).height(),d=Math.max(0,b.minHeight-c);if(b.height==="auto")if(a.support.minHeight)this.element.css({minHeight:d,height:"auto"});else{this.uiDialog.show();var f=this.element.css("height","auto").height();e||this.uiDialog.hide(),this.element.height(Math.max(f,d))}else this.element.height(Math.max(b.height-c,0));this.uiDialog.is(":data(resizable)")&&this.uiDialog.resizable("option","minHeight",this._minHeight())}}),a.extend(a.ui.dialog,{version:"1.8.17",uuid:0,maxZ:0,getTitleId:function(a){var b=a.attr("id");b||(this.uuid+=1,b=this.uuid);return"ui-dialog-title-"+b},overlay:function(b){this.$el=a.ui.dialog.overlay.create(b)}}),a.extend(a.ui.dialog.overlay,{instances:[],oldInstances:[],maxZ:0,events:a.map("focus,mousedown,mouseup,keydown,keypress,click".split(","),function(a){return a+".dialog-overlay"}).join(" "),create:function(b){this.instances.length===0&&(setTimeout(function(){a.ui.dialog.overlay.instances.length&&a(document).bind(a.ui.dialog.overlay.events,function(b){if(a(b.target).zIndex()<a.ui.dialog.overlay.maxZ)return!1})},1),a(document).bind("keydown.dialog-overlay",function(c){b.options.closeOnEscape&&!c.isDefaultPrevented()&&c.keyCode&&c.keyCode===a.ui.keyCode.ESCAPE&&(b.close(c),c.preventDefault())}),a(window).bind("resize.dialog-overlay",a.ui.dialog.overlay.resize));var c=(this.oldInstances.pop()||a("<div></div>").addClass("ui-widget-overlay")).appendTo(document.body).css({width:this.width(),height:this.height()});a.fn.bgiframe&&c.bgiframe(),this.instances.push(c);return c},destroy:function(b){var c=a.inArray(b,this.instances);c!=-1&&this.oldInstances.push(this.instances.splice(c,1)[0]),this.instances.length===0&&a([document,window]).unbind(".dialog-overlay"),b.remove();var d=0;a.each(this.instances,function(){d=Math.max(d,this.css("z-index"))}),this.maxZ=d},height:function(){var b,c;if(a.browser.msie&&a.browser.version<7){b=Math.max(document.documentElement.scrollHeight,document.body.scrollHeight),c=Math.max(document.documentElement.offsetHeight,document.body.offsetHeight);return b<c?a(window).height()+"px":b+"px"}return a(document).height()+"px"},width:function(){var b,c;if(a.browser.msie){b=Math.max(document.documentElement.scrollWidth,document.body.scrollWidth),c=Math.max(document.documentElement.offsetWidth,document.body.offsetWidth);return b<c?a(window).width()+"px":b+"px"}return a(document).width()+"px"},resize:function(){var b=a([]);a.each(a.ui.dialog.overlay.instances,function(){b=b.add(this)}),b.css({width:0,height:0}).css({width:a.ui.dialog.overlay.width(),height:a.ui.dialog.overlay.height()})}}),a.extend(a.ui.dialog.overlay.prototype,{destroy:function(){a.ui.dialog`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-1.7.1.min.js](https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-1.7.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `jquery-1.7.1.min.js`
  
  
  
  
Instances: 3
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p>CVE-2015-9251</p><p>CVE-2019-11358</p><p>CVE-2012-6708</p><p></p>
  
### Reference
* https://nvd.nist.gov/vuln/detail/CVE-2012-6708
* https://github.com/jquery/jquery/issues/2432
* http://research.insecurelabs.org/jquery/test/
* http://blog.jquery.com/2016/01/08/jquery-2-2-and-1-12-released/
* http://bugs.jquery.com/ticket/11290
* https://blog.jquery.com/2019/04/10/jquery-3-4-0-released/
* https://nvd.nist.gov/vuln/detail/CVE-2019-11358
* https://nvd.nist.gov/vuln/detail/CVE-2015-9251
* https://github.com/jquery/jquery/commit/753d591aea698e57d6db58c9f722cd0808619b1b
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html](https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/informations/paiement_securise.html](https://www.darty.com/achat/informations/paiement_securise.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/offres/bons-plans-informatique](https://www.darty.com/offres/bons-plans-informatique)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/se-divertir/index.html](https://www.darty.com/achat/boutique/evenement/se-divertir/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/services/services-darty/index.html](https://www.darty.com/achat/services/services-darty/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/informations/informations_legales.html](https://www.darty.com/achat/informations/informations_legales.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/d3e/d3e.html](https://www.darty.com/achat/d3e/d3e.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
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
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="false" data-btn-codic="4913515" data-btn-type="AaP">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="false" data-btn-codic="4934792" data-btn-type="AaP">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="false" data-btn-codic="4802365" data-btn-type="AaP">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="true" data-btn-codic="4695720" data-btn-type="AaP">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="true" data-btn-codic="4672984" data-btn-type="AaP">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="optin_popin_form" class="optin_popin_form" action="#" data-js="optin-inscription-form" method="post">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action='https://magasin.darty.com/search' class='f_form_mag_form' id='f_form_mag_form' method='get' >`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="dartyCom_searchform_xxl" method="get" action="/nav/recherche" name="recherche" autocomplete="off"
accept-charset="utf-8" role="search">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="f_newsletter_form" class="input_newsletter" data-js="open-optin-popin" data-modal="popinOptinForm">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="darty_middle_newsletter_form" class="input_newsletter" data-js="open-optin-popin" data-modal="popinOptinForm">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="true" data-btn-codic="4800290" data-btn-type="AaP">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name="new_order" action="https://www.darty.com/webapp/wcs/stores/servlet/CSRNewOrder">`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-add-basket" method="post" action="/nav/extra/basket_add" data-stock="false" data-btn-codic="4852818" data-btn-type="AaP">`
  
  
  
  
Instances: 13
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 10: "xsell_codic" "basket_update" "premium_card_membership" ].</p>
  
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
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/comment-beneficier-du-remboursement-de-la-difference](https://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/comment-beneficier-du-remboursement-de-la-difference)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 148 [http://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/remboursement-de-la-difference-mode-demploi].</p><p>Predicted response size: 448.</p><p>Response Body Length: 836.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `akavpau_VP_WaitingRoom`
  
  
  * Evidence: `Set-Cookie: akavpau_VP_WaitingRoom`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Parameter: `dtCookie`
  
  
  * Evidence: `Set-Cookie: dtCookie`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ec/orders](https://www.darty.com/webapp/wcs/stores/controller/ec/orders)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ec/orders](https://www.darty.com/webapp/wcs/stores/controller/ec/orders)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  * Parameter: `kameleoonVisitorCode`
  
  
  * Evidence: `Set-Cookie: kameleoonVisitorCode`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.cookielaw.org/scripttemplates/otSDKStub.js`
  
  
  * Evidence: `<script async src="https://cdn.cookielaw.org/scripttemplates/otSDKStub.js" data-domain-script="23aa55cf-1d2a-4f9e-9612-56a8b9d14b5d" data-document-language="true"></script>`
  
  
  
  
* URL: [https://www.darty.com/espace_client/magasins-preferes](https://www.darty.com/espace_client/magasins-preferes)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/achat/petit_electromenager/index.html](https://www.darty.com/nav/achat/petit_electromenager/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/achat/beaute_bien-etre/index.html](https://www.darty.com/nav/achat/beaute_bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/basket](https://www.darty.com/nav/extra/basket)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/jserror](https://www.darty.com/nav/extra/jserror)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/achat/gros_electromenager/index.html](https://www.darty.com/nav/achat/gros_electromenager/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/selection*](https://www.darty.com/nav/selection*)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/nav/achat/maison_deco/index.html](https://www.darty.com/nav/achat/maison_deco/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ct.captcha-delivery.com/c.js`
  
  
  * Evidence: `<script src="https://ct.captcha-delivery.com/c.js"></script>`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.cookielaw.org/scripttemplates/otSDKStub.js`
  
  
  * Evidence: `<script async src="https://cdn.cookielaw.org/scripttemplates/otSDKStub.js" data-domain-script="23aa55cf-1d2a-4f9e-9612-56a8b9d14b5d" data-document-language="true"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.darty.com/static/8HLl/wro/desktop_export_catalogue.pack.js](https://www.darty.com/static/8HLl/wro/desktop_export_catalogue.pack.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `evAl`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-ui-1.8.17.custom.min.js](https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-ui-1.8.17.custom.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `evAl`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-1.7.1.min.js](https://www.darty.com/static/8HLl/catalog/version_common/libs/jquery-1.7.1.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.darty.com/res3/views/espace_client/password/commons/scripts/complexify/jquery.complexify.js](https://www.darty.com/res3/views/espace_client/password/commons/scripts/complexify/jquery.complexify.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/wro/desktop_common.pack.js](https://www.darty.com/static/8HLl/wro/desktop_common.pack.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.darty.com/res3/services/contrat-de-confiance/js/lightslider.min.js](https://www.darty.com/res3/services/contrat-de-confiance/js/lightslider.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.darty.com/wcsstore/Darty/fr_FR/js/commun.js](https://www.darty.com/wcsstore/Darty/fr_FR/js/commun.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/de-vous-nous/nos-actus/phishing-comment-eviter-se-faire-pieger](https://www.darty.com/darty-et-vous/de-vous-nous/nos-actus/phishing-comment-eviter-se-faire-pieger)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/de-vous-nous/nos-actus/darty-rappelle-des-produits-non-conformes](https://www.darty.com/darty-et-vous/de-vous-nous/nos-actus/darty-rappelle-des-produits-non-conformes)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit](https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/wro/desktop_home.pack.js](https://www.darty.com/static/8HLl/wro/desktop_home.pack.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/ajax/](https://www.darty.com/*extra/ajax/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/services](https://www.darty.com/*extra/services)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/list](https://www.darty.com/*extra/list)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*fa$](https://www.darty.com/*fa$)
  
  
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
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private,no-cache,no-store`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=874`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=900`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=532`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=898`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.darty.com/achat/services/services-darty/index.html](https://www.darty.com/achat/services/services-darty/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=900`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=534`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=531`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=873`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html](https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=862`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.darty.com/darty-et-vous/high-tech/audio/la-musique-chez-soi/les-enceintes-pour-ecouter-la-musique-du-salon-au-jardin](https://www.darty.com/darty-et-vous/high-tech/audio/la-musique-chez-soi/les-enceintes-pour-ecouter-la-musique-du-salon-au-jardin)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://bocms.intranet.darty.fr/darty-et-vous/sites/default/files/thumbnails/image/devialetphantom1-600.jpg`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions](https://www.darty.com/services/solutions/foire_aux_questions)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.darty.com/services/themes/custom/dartyservices/images/croix-fermeture-popin.png`
  
  
  
  
Instances: 2
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://bocms.intranet.darty.fr/darty-et-vous/sites/default/files/thumbnails/image/devialetphantom1-600.jpg</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/lassistance-sur-mesure/installation-et-mise-en-service/lassistance-telephonique-darty](https://www.darty.com/services/solutions/savoir_faire/lassistance-sur-mesure/installation-et-mise-en-service/lassistance-telephonique-darty)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/les-solutions-de-financement/payer-en-3-ou-4-fois-avec-votre-cb/le-paiement-en-3-ou-4-fois-par-carte-bancaire](https://www.darty.com/services/solutions/savoir_faire/les-solutions-de-financement/payer-en-3-ou-4-fois-avec-votre-cb/le-paiement-en-3-ou-4-fois-par-carte-bancaire)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.3.3`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/comment-beneficier-du-remboursement-de-la-difference](https://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/comment-beneficier-du-remboursement-de-la-difference)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
* URL: [https://www.darty.com/offres/bons-plans-informatique](https://www.darty.com/offres/bons-plans-informatique)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.3.3`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/beaute-bien-etre/forme-sante/forme-au-quotidien/comment-perdre-du-ventre](https://www.darty.com/darty-et-vous/beaute-bien-etre/forme-sante/forme-au-quotidien/comment-perdre-du-ventre)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.3.3`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions/lapres-livraison/retour-retraction-remboursement](https://www.darty.com/services/solutions/foire_aux_questions/lapres-livraison/retour-retraction-remboursement)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/de-vous-nous/nos-actus/fnac-darty-propose-500-postes-en-cdi-en-2021](https://www.darty.com/darty-et-vous/de-vous-nous/nos-actus/fnac-darty-propose-500-postes-en-cdi-en-2021)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.3.3`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/les_services_a_la_carte/financer-ses-achats](https://www.darty.com/services/solutions/les_services_a_la_carte/financer-ses-achats)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/les_services_a_la_carte/proteger-son-produit/assurer-son-appareil/assurez-vos-appareils-multimedia](https://www.darty.com/services/solutions/les_services_a_la_carte/proteger-son-produit/assurer-son-appareil/assurez-vos-appareils-multimedia)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/de-vous-nous/darty-occasion-achetez-en-toute-confiance-avec-darty](https://www.darty.com/darty-et-vous/de-vous-nous/darty-occasion-achetez-en-toute-confiance-avec-darty)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.3.3`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/le-recyclage-de-votre-ancien-appareil/recyclez-vos-appareils-avec-darty](https://www.darty.com/services/solutions/savoir_faire/le-recyclage-de-votre-ancien-appareil/recyclez-vos-appareils-avec-darty)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: PHP/5.6.40`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.darty.com/services/solutions/les_services_a_la_carte/financer-ses-achats](https://www.darty.com/services/solutions/les_services_a_la_carte/financer-ses-achats)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/formations-et-initiations-apprivoisez-vos-appareils-avec-darty](https://www.darty.com/services/formations-et-initiations-apprivoisez-vos-appareils-avec-darty)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/les_services_a_la_carte/proteger-son-produit/assurer-son-appareil/assurez-vos-appareils-multimedia](https://www.darty.com/services/solutions/les_services_a_la_carte/proteger-son-produit/assurer-son-appareil/assurez-vos-appareils-multimedia)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions](https://www.darty.com/services/solutions/foire_aux_questions)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/offres/bons-plans-informatique](https://www.darty.com/offres/bons-plans-informatique)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.2.15 (Red Hat) PHP/5.3.3`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/comment-beneficier-du-remboursement-de-la-difference](https://www.darty.com/services/solutions/foire_aux_questions/darty-et-vous/remboursement-de-la-difference/comment-beneficier-du-remboursement-de-la-difference)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/les-garanties-darty/la-garantie-2-ans-par-le-sav-darty/la-garantie-2-ans-par-le-sav-darty-decryptage](https://www.darty.com/services/solutions/savoir_faire/les-garanties-darty/la-garantie-2-ans-par-le-sav-darty/la-garantie-2-ans-par-le-sav-darty-decryptage)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/offres/soldes](https://www.darty.com/offres/soldes)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.2.15 (Red Hat)`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/foire_aux_questions/lapres-livraison/retour-retraction-remboursement](https://www.darty.com/services/solutions/foire_aux_questions/lapres-livraison/retour-retraction-remboursement)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/les-solutions-de-financement/payer-en-3-ou-4-fois-avec-votre-cb/le-paiement-en-3-ou-4-fois-par-carte-bancaire](https://www.darty.com/services/solutions/savoir_faire/les-solutions-de-financement/payer-en-3-ou-4-fois-avec-votre-cb/le-paiement-en-3-ou-4-fois-par-carte-bancaire)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/lassistance-sur-mesure/installation-et-mise-en-service/lassistance-telephonique-darty](https://www.darty.com/services/solutions/savoir_faire/lassistance-sur-mesure/installation-et-mise-en-service/lassistance-telephonique-darty)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
* URL: [https://www.darty.com/services/solutions/savoir_faire/le-recyclage-de-votre-ancien-appareil/recyclez-vos-appareils-avec-darty](https://www.darty.com/services/solutions/savoir_faire/le-recyclage-de-votre-ancien-appareil/recyclez-vos-appareils-avec-darty)
  
  
  * Method: `GET`
  
  
  * Evidence: `Apache/2.4.6 (SLES Expanded Support platform) PHP/5.6.26`
  
  
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.darty.com/*extra/ajax/](https://www.darty.com/*extra/ajax/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*fa$](https://www.darty.com/*fa$)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/list](https://www.darty.com/*extra/list)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
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
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/res3/pdf/cnil/donnees_personnelles_darty.pdf](https://www.darty.com/res3/pdf/cnil/donnees_personnelles_darty.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.darty.com/achat/services/services-darty/index.html](https://www.darty.com/achat/services/services-darty/index.html)
  
  
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
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/cdn-storage/tagcommander/prd/tc_Darty_2`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/8HLl/catalog/version_common/styles/images/logos/favicon`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/8HLl/catalog/version_common/styles/images/logos/favicon`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/basket](https://www.darty.com/nav/extra/basket)
  
  
  * Method: `GET`
  
  
  * Evidence: `UeVh9qpczLlWENDa7uOAv8lF9EO30mWKh0_`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/jserror](https://www.darty.com/nav/extra/jserror)
  
  
  * Method: `GET`
  
  
  * Evidence: `ATWuk40ZxnibxbNqisK-b-PNNEcadAShx85-ZLI1OX3rog3NgH_wSU-sdho1mATPfA0f9pJ`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/cdn-storage/tagcommander/prd/tc_Darty_2`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/cdn-storage/tagcommander/prd/tc_Darty_2`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/cdn-storage/tagcommander/prd/tc_Darty_2`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/cdn-storage/tagcommander/prd/tc_Darty_2`
  
  
  
  
* URL: [https://www.darty.com/nav/selection*](https://www.darty.com/nav/selection*)
  
  
  * Method: `GET`
  
  
  * Evidence: `23ehL11yRY0KezHMh7eSOniiKBSpQHxN26xhooeJcqiP25oDNhZIPIDh`
  
  
  
  
* URL: [https://www.darty.com/res3/pdf/cnil/donnees_personnelles_darty.pdf](https://www.darty.com/res3/pdf/cnil/donnees_personnelles_darty.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `/Type/Font/Subtype/TrueType/Name/F1/BaseFont/ABCDEE+Roboto`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>r��q����+j\x0007���\x001c�i��׫�����?
����</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Charset Mismatch (Header Versus Meta Content-Type Charset)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check identifies responses where the HTTP Content-Type header declares a charset different from the charset defined by the body of the HTML or XML. When there's a charset mismatch between the HTTP header and content body Web browsers can be forced into an undesirable content-sniffing mode to determine the content's correct character set.</p><p></p><p>An attacker could manipulate content on the page to be interpreted in an encoding of their choice. For example, if an attacker can control content at the beginning of the page, they could inject script using UTF-7 encoded text and manipulate some browsers into interpreting that text.</p>
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/se-divertir/index.html](https://www.darty.com/achat/boutique/evenement/se-divertir/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/informations/informations_cookies.html](https://www.darty.com/achat/informations/informations_cookies.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/services/services-darty/index.html](https://www.darty.com/achat/services/services-darty/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/informations/informations_legales.html](https://www.darty.com/achat/informations/informations_legales.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html](https://www.darty.com/achat/boutique/evenement/comme-au-boulot/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/securite/mot-de-passe/index.html](https://www.darty.com/achat/securite/mot-de-passe/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/achat/informations/paiement_securise.html](https://www.darty.com/achat/informations/paiement_securise.html)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Force UTF-8 for all text content in both the HTTP header and meta tags in HTML or encoding declarations in XML.</p>
  
### Other information
<p>There was a charset mismatch between the HTTP Header and the META content-type encoding declarations: [ISO-8859-1] and [utf-8] do not match.</p>
  
### Reference
* http://code.google.com/p/browsersec/wiki/Part2#Character_set_handling_and_detection

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/styles/images/logos/clickandcollect-nocontact-205x37.png](https://www.darty.com/static/8HLl/catalog/version_common/styles/images/logos/clickandcollect-nocontact-205x37.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-pinterest.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-pinterest.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/carousel-pause.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/carousel-pause.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/carousel-play.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/carousel-play.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/geolocation-rouge.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/geolocation-rouge.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/styles/images/blank.png](https://www.darty.com/static/8HLl/catalog/version_common/styles/images/blank.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_common/styles/images/logos/favicon.png](https://www.darty.com/static/8HLl/catalog/version_common/styles/images/logos/favicon.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-twitter.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-twitter.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-facebook.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-facebook.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/modal_close.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/modal_close.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-youtube.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/pictos/footer-youtube.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/darty_sprite/sprite_darty_logo.png](https://www.darty.com/static/8HLl/catalog/version_desktop/styles/images/darty_sprite/sprite_darty_logo.png)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
#### Source ID : 3

  
  
  
  
### Cookie Poisoning
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where cookie parameters might be controlled. This is called a cookie poisoning attack, and becomes exploitable when an attacker can manipulate the cookie in various ways. In some cases this will not be exploitable, however, allowing URL parameters to set cookie values is generally considered a bug.</p>
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/servlet/CSRNewOrder?nta=true&redirect_url=%2Fnav%2Fextra%2Fbasket%3FfrontVendeur%3Dtrue&user_id](https://www.darty.com/webapp/wcs/stores/servlet/CSRNewOrder?nta=true&redirect_url=%2Fnav%2Fextra%2Fbasket%3FfrontVendeur%3Dtrue&user_id)
  
  
  * Method: `GET`
  
  
  * Parameter: `nta`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not allow user input to control cookie names and values. If some query string parameters must be set in cookie values, be sure to filter out semicolon's that can serve as name/value pair delimiters.</p>
  
### Other information
<p>An attacker may be able to poison cookie values through URL parameters.  Try injecting a semicolon to see if you can add cookie values (e.g. name=controlledValue;name=anotherValue;).</p><p></p><p>This was identified at:</p><p></p><p>https://www.darty.com/webapp/wcs/stores/servlet/CSRNewOrder?nta=true&redirect_url=%2Fnav%2Fextra%2Fbasket%3FfrontVendeur%3Dtrue&user_id</p><p></p><p>User-input was found in the following cookie:</p><p>WC_SESSION_ESTABLISHED=true; Path=/; Domain=.darty.com</p><p></p><p>The user input was:</p><p>nta=true</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-cookie

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/servlet/CSRNewOrder?nta=true&redirect_url=%2Fnav%2Fextra%2Fbasket%3FfrontVendeur%3Dtrue&user_id](https://www.darty.com/webapp/wcs/stores/servlet/CSRNewOrder?nta=true&redirect_url=%2Fnav%2Fextra%2Fbasket%3FfrontVendeur%3Dtrue&user_id)
  
  
  * Method: `GET`
  
  
  * Parameter: `user_id`
  
  
  * Evidence: `user_id`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL contains potentially sensitive information. The following string was found via the pattern: user</p><p>user_id</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Bug`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `xxx`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit](https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit)
  
  
  * Method: `GET`
  
  
  * Evidence: `Bug`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "<!-- CMS-661 :Bug Affichage Pub Adserving Fnac -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit](https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/](https://www.darty.com/darty-et-vous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.darty.com/offres/bons-plans-informatique](https://www.darty.com/offres/bons-plans-informatique)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit](https://www.darty.com/darty-et-vous/cuisine/equipement/froid/sos-mon-frigo-fait-trop-de-bruit)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
Instances: 8
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bWHERE\b and was detected in the element starting with: "<script type="text/javascript"></p><p>            // Change the value of this URL to point to your own URL, where the iFrame is hosted", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Loosely Scoped Cookie
##### Informational (Low)
  
  
  
  
#### Description
<p>Cookies can be scoped by domain or path. This check is only concerned with domain scope.The domain scope applied to a cookie determines which domains can access it. For example, a cookie can be scoped strictly to a subdomain e.g. www.nottrusted.com, or loosely scoped to a parent domain e.g. nottrusted.com. In the latter case, any subdomain of nottrusted.com can access the cookie. Loosely scoped cookies are common in mega-applications like google.com and live.com. Cookies set from a subdomain like app.foo.bar are transmitted only to that domain by the browser. However, cookies scoped to a parent-level domain may be transmitted to the parent, or any subdomain of the parent.</p>
  
  
  
* URL: [https://www.darty.com/*extra/ajax/](https://www.darty.com/*extra/ajax/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/UserLogonDisplayView?espaceclient=0&org=head&storeId=10001](https://www.darty.com/webapp/wcs/stores/controller/UserLogonDisplayView?espaceclient=0&org=head&storeId=10001)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ec/orders](https://www.darty.com/webapp/wcs/stores/controller/ec/orders)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Always scope cookies to a FQDN (Fully Qualified Domain Name).</p>
  
### Other information
<p>The origin domain used for comparison was: </p><p>www.darty.com</p><p>kameleoonVisitorCode=1e00fd37eae8e712e42b5342ba0a78e9</p><p></p>
  
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
  
  
  
* URL: [https://www.darty.com/achat/boutique/operation-bien-etre/index.html](https://www.darty.com/achat/boutique/operation-bien-etre/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_xxl_localisation_lien" href="#" class="h_xxl_localisation_lien" data-easy-modal="#darty_geoloc_popin" data-tracking-click data-tracking-name="popin" data-tracking-event="popin-geoloc_header">
<div>
<span class="h_xxl_localisation__sprite"></span>
</div>
<ul>
<li class="c-geolocalisation__city h_xxl_localisation__item h_xxl_localisation__item--color u-truncate-header" title="Paris"></li>
<li class="c-geolocalisation__zipcode h_xxl_localisation__item h_xxl_localisation__item--color"></li>
<li class="c-geolocalisation__button h_xxl_localisation__item h_xxl_localisation__item--link">Modifier</li>
</ul>
</a>`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var dd={'cid':'AHrlqAAAAAMAEpOP_RVuXyQADVLZuw==','hsh':'4BA90718940D0114F409A57DFAF6AF','t':'fe','s':3610,'host':'geo.captcha-delivery.com'}</script>`
  
  
  
  
* URL: [https://www.darty.com/nav/selection*](https://www.darty.com/nav/selection*)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var dd={'cid':'AHrlqAAAAAMAEpOP_RVuXyQADVLZuw==','hsh':'4BA90718940D0114F409A57DFAF6AF','t':'fe','s':3610,'host':'geo.captcha-delivery.com'}</script>`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_xxl_localisation_lien" href="#" class="h_xxl_localisation_lien" data-easy-modal="#darty_geoloc_popin" data-tracking-click data-tracking-name="popin" data-tracking-event="popin-geoloc_header">
<div>
<span class="h_xxl_localisation__sprite"></span>
</div>
<ul>
<li class="c-geolocalisation__city h_xxl_localisation__item h_xxl_localisation__item--color u-truncate-header" title="Paris"></li>
<li class="c-geolocalisation__zipcode h_xxl_localisation__item h_xxl_localisation__item--color"></li>
<li class="c-geolocalisation__button h_xxl_localisation__item h_xxl_localisation__item--link">Modifier</li>
</ul>
</a>`
  
  
  
  
* URL: [https://www.darty.com/espace_client/magasins-preferes](https://www.darty.com/espace_client/magasins-preferes)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var dd={'cid':'AHrlqAAAAAMAEpOP_RVuXyQADVLZuw==','hsh':'4BA90718940D0114F409A57DFAF6AF','t':'fe','s':3610,'host':'geo.captcha-delivery.com'}</script>`
  
  
  
  
* URL: [https://www.darty.com/achat/services/darty-max/index.html](https://www.darty.com/achat/services/darty-max/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_xxl_localisation_lien" href="#" class="h_xxl_localisation_lien" data-easy-modal="#darty_geoloc_popin" data-tracking-click data-tracking-name="popin" data-tracking-event="popin-geoloc_header">
<div>
<span class="h_xxl_localisation__sprite"></span>
</div>
<ul>
<li class="c-geolocalisation__city h_xxl_localisation__item h_xxl_localisation__item--color u-truncate-header" title="Paris"></li>
<li class="c-geolocalisation__zipcode h_xxl_localisation__item h_xxl_localisation__item--color"></li>
<li class="c-geolocalisation__button h_xxl_localisation__item h_xxl_localisation__item--link">Modifier</li>
</ul>
</a>`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_xxl_localisation_lien" href="#" class="h_xxl_localisation_lien" data-easy-modal="#darty_geoloc_popin" data-tracking-click data-tracking-name="popin" data-tracking-event="popin-geoloc_header">
<div>
<span class="h_xxl_localisation__sprite"></span>
</div>
<ul>
<li class="c-geolocalisation__city h_xxl_localisation__item h_xxl_localisation__item--color u-truncate-header" title="Paris"></li>
<li class="c-geolocalisation__zipcode h_xxl_localisation__item h_xxl_localisation__item--color"></li>
<li class="c-geolocalisation__button h_xxl_localisation__item h_xxl_localisation__item--link">Modifier</li>
</ul>
</a>`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/jserror](https://www.darty.com/nav/extra/jserror)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var dd={'cid':'AHrlqAAAAAMAEpOP_RVuXyQADVLZuw==','hsh':'4BA90718940D0114F409A57DFAF6AF','t':'fe','s':3610,'host':'geo.captcha-delivery.com'}</script>`
  
  
  
  
* URL: [https://www.darty.com/achat/boutique/choix-durable/index.html](https://www.darty.com/achat/boutique/choix-durable/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_xxl_localisation_lien" href="#" class="h_xxl_localisation_lien" data-easy-modal="#darty_geoloc_popin" data-tracking-click data-tracking-name="popin" data-tracking-event="popin-geoloc_header">
<div>
<span class="h_xxl_localisation__sprite"></span>
</div>
<ul>
<li class="c-geolocalisation__city h_xxl_localisation__item h_xxl_localisation__item--color u-truncate-header" title="Paris"></li>
<li class="c-geolocalisation__zipcode h_xxl_localisation__item h_xxl_localisation__item--color"></li>
<li class="c-geolocalisation__button h_xxl_localisation__item h_xxl_localisation__item--link">Modifier</li>
</ul>
</a>`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_xxl_localisation_lien" href="#" class="h_xxl_localisation_lien" data-easy-modal="#darty_geoloc_popin" data-tracking-click data-tracking-name="popin" data-tracking-event="popin-geoloc_header">
<div>
<span class="h_xxl_localisation__sprite"></span>
</div>
<ul>
<li class="c-geolocalisation__city h_xxl_localisation__item h_xxl_localisation__item--color u-truncate-header" title="Paris"></li>
<li class="c-geolocalisation__zipcode h_xxl_localisation__item h_xxl_localisation__item--color"></li>
<li class="c-geolocalisation__button h_xxl_localisation__item h_xxl_localisation__item--link">Modifier</li>
</ul>
</a>`
  
  
  
  
* URL: [https://www.darty.com/nav/extra/basket](https://www.darty.com/nav/extra/basket)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var dd={'cid':'AHrlqAAAAAMAEpOP_RVuXyQADVLZuw==','hsh':'4BA90718940D0114F409A57DFAF6AF','t':'fe','s':3610,'host':'geo.captcha-delivery.com'}</script>`
  
  
  
  
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
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ec/orders](https://www.darty.com/webapp/wcs/stores/controller/ec/orders)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/UserLogonDisplayView?espaceclient=0&org=head&storeId=10001](https://www.darty.com/webapp/wcs/stores/controller/UserLogonDisplayView?espaceclient=0&org=head&storeId=10001)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
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

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=532`
  
  
  
  
* URL: [https://www.darty.com/*extra/ajax/](https://www.darty.com/*extra/ajax/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=531`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=534`
  
  
  
  
* URL: [https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController](https://www.darty.com/webapp/wcs/stores/controller/ChangePasswordFormViewController)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585246`
  
  
  
  
* URL: [https://www.darty.com/*extra/vendeur/](https://www.darty.com/*extra/vendeur/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585247`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `16090800`
  
  
  
  
* URL: [https://www.darty.com/sitemap.xml](https://www.darty.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585247`
  
  
  
  
* URL: [https://www.darty.com/robots.txt](https://www.darty.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585246`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585247`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585244`
  
  
  
  
* URL: [https://www.darty.com](https://www.darty.com)
  
  
  * Method: `GET`
  
  
  * Evidence: `16090800`
  
  
  
  
* URL: [https://www.darty.com/nav/recherche](https://www.darty.com/nav/recherche)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://www.darty.com/*espace_client/](https://www.darty.com/*espace_client/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585247`
  
  
  
  
* URL: [https://www.darty.com/](https://www.darty.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1617585247`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1617585246, which evaluates to: 2021-04-05 01:14:06</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `POST`
  
  
  * Parameter: `optin_fnac`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `POST`
  
  
  * Parameter: `optin_date_aa`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `POST`
  
  
  * Parameter: `optin_sms`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `POST`
  
  
  * Parameter: `optin_date_mm`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `POST`
  
  
  * Parameter: `optin_date_jj`
  
  
  
  
* URL: [https://www.darty.com/achat/services/contrat-de-confiance/index.html](https://www.darty.com/achat/services/contrat-de-confiance/index.html)
  
  
  * Method: `POST`
  
  
  * Parameter: `optin_civilite`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.darty.com/achat/services/contrat-de-confiance/index.html</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>optin_fnac=true</p><p></p><p>The user-controlled value was:</p><p>true</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

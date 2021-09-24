
# ZAP Scanning Report

Generated on Fri, 24 Sep 2021 11:18:46


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 3 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Application Error Disclosure | Medium | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 9 | 
| Cross-Domain Misconfiguration | Medium | 10 | 
| Reverse Tabnabbing | Medium | 9 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 7 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 6 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 5 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 5 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 1 | 

## Alert Detail


  
  
  
  
### Application Error Disclosure
##### Medium (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `internal error`
  
  
  
  
Instances: 1
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/accessibilit%C3%A9/](https://envergo.beta.gouv.fr/accessibilit%C3%A9/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/sitemap.xml](https://envergo.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/robots.txt](https://envergo.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.7718992eb76d.svg](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.7718992eb76d.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/apple-touch-icon.09be1cc5f435.png](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/apple-touch-icon.09be1cc5f435.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/css/project.min.9b07bc4229d2.css](https://envergo.beta.gouv.fr/static/css/project.min.9b07bc4229d2.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/images/capture_cerfa.644098dd37da.png](https://envergo.beta.gouv.fr/static/images/capture_cerfa.644098dd37da.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/js/libs/accordion_analytics.c56d9c413bb5.js](https://envergo.beta.gouv.fr/static/js/libs/accordion_analytics.c56d9c413bb5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.059558abd249.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.059558abd249.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/sitemap.xml](https://envergo.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/accessibilit%C3%A9/](https://envergo.beta.gouv.fr/accessibilit%C3%A9/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/robots.txt](https://envergo.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000042075042/2020-09-01/" target="_blank" rel="noopener">l'article R.214-1 du
          Code de
          l'Environnement</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
Instances: 9
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class r{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(t){this.closures.push(t);return()=>{const e=this.closures.indexOf(t);-1!==e&&this.closures.splice(e,1)}}next(t,e){e=void 0===e?0:e-1,void 0===this.nexts[e]&&(this.nexts[e]=[]),this.nexts[e].push(t)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const t=this.nexts.shift();if(t)for(const e of t)e.call()}}const o=new class{constructor(){this.renderer=new r}register(t,e){}start(){}stop(){}};class h{constructor(t,e){this.selector=t,this.builders=e,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let t=0;t<this.builders.length;t++)this.instances.push(this.builders[t]())}}const l={},c={};let a=0;const d=t=>{for(const e in c)if(c[e]===t)return e;a++;const e=a;return c[e]=t,e};class u{constructor(t,e,s){const i=d(t);l[i]||(l[i]=[]),l[i].push(this),this.element=t,this.id=t.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=e,this.isRendering=s}dispatch(t,e){const s=new CustomEvent(t,e);this.element.dispatchEvent(s)}listen(t,e){this.listeners[t]||(this.listeners[t]=[]),this.listeners[t].indexOf(e)>-1||(this.listeners[t].push(e),this.element.addEventListener(t,e))}unlisten(t,e){if(t)if(e){if(!this.listeners[t])return;const s=this.listeners[t].indexOf(e);s>-1&&this.listeners[t].splice(s,1),this.element.removeEventListener(e)}else{if(!this.listeners[t])return;for(const e of this.listeners[t])this.element.removeEventListener(e);this.listeners[t].length=0}else for(const t in this.listeners)this.unlisten(t)}get isRendering(){return this._isRendering}set isRendering(t){this._isRendering!==t&&(this._isRendering=t)}render(){}get isResizing(){return this._isResizing}set isResizing(t){this._isResizing!==t&&(this._isResizing=t)}resize(){}destroy(){}static getInstances(t,e){const s=d(t);return l[s]?e?l[s].filter((t=>t instanceof e)):l[s]:null}}const m=e.attr("group"),p=[];class b{constructor(t,e){this.id=t,this.element=e,this.members=[],this._index=-1,this._current=null,p.push(this)}static getGroupById(t){for(const e of p)if(e.constructor===this&&e.id===t)return e;return new this(t)}static getGroupByElement(t){for(const e of p)if(e.element===t)return e;return new this(!1,t)}static groupById(t,e){const s=t.element.getAttribute(m);if(null===s)return;e.getGroupById(s).add(t)}static groupByParent(t,e,s){if(void 0===s&&(s=e.selector),""===s)return;let i=t.element.parentElement;for(;i;){if(i.classList.contains(t.constructor.selector))return;if(i.classList.contains(s)){return void e.getGroupByElement(i).add(t)}i=i.parentElement}}static get selector(){return""}add(t){if(-1===this.members.indexOf(t))switch(this.members.push(t),t.setGroup(this),!0){case null!==this.current:case!(t.disclosed||t.primary&&t.primary.disclosed):t.disclosed=!1;break;default:this._current=t,this._index=this.members.indexOf(t),t.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(t){t<-1||t>=this.length||this._index===t||(null!==this.current&&this.current.conceal(!0,!0),this._index=t,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(t){this.index=this.members.indexOf(t)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class g{constructor(t,e){this.element=t,this.disclosure=e,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(t){this.disclosure.change(this.hasAttribute)}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(t){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,t),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const f=e.event("DISCLOSE"),y=e.event("CONCEAL"),w=[];class v extends u{constructor(t){super(t),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:e.attr(this.type.id),this.pristine=!0;const s=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:e.attr.selector("controls",this.id));if(s.length>0)for(let t=0;t<s.length;t++)this.addButton(s[t]);this.disclosed=this.primary&&this.primary.disclosed,this.gather()}gather(){this.group||(b.groupById(this,this.GroupConstructor),b.groupByParent(this,this.GroupConstructor))}static build(t){const e=Array.prototype.slice.call(t.querySelectorAll(`.${this.selector}`));for(const t of e)w.push(new this(t))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(t){const e=this.buttonFactory(t);e.hasAttribute&&(void 0===this.primary?this.primary=e:e.apply(this.primary.disclosed)),this.buttons.push(e)}get GroupConstructor(){return b}buttonFactory(t){return new g(t,this)}disclose(t){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,t||void 0===this.group||(this.group.current=this),!0)}conceal(t,e){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,e||this.focus(),t||void 0===this.group||(this.group.current=null);for(const t of w)t!==this&&this.element.contains(t.element)&&t.reset();return!0}get disclosed(){return this._disclosed}set disclosed(t){if(this._disclosed!==t){this.dispatch(t?f:y,this.type),this._disclosed=t,t?i(this.element,this.modifier):n(this.element,this.modifier);for(let e=0;e<this.buttons.length;e++)this.buttons[e].apply(t)}}reset(){}change(t){if(this.constructor.type.canConceal)switch(!0){case!t:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(t){this.group=t}get buttonHasFocus(){return!!this.buttons.some((t=>t.hasFocus))}get hasFocus(){return this.element===document.activeElement||(this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus)}focus(){for(let t=0;t<this.buttons.length;t++){const e=this.buttons[t];if(e.hasAttribute)return void e.element.focus()}}}v.DISCLOSE_EVENT=f,v.CONCEAL_EVENT=y;const E={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class x{constructor(t){this.element=t,this.collections={}}_add(t,e){void 0===this.collections[t]&&(this.collections[t]=new L(t,this.element)),this.collections[t].add(e)}down(t,e,s,i){this._add("down",new A(t,e,s,i))}up(t,e,s,i){this._add("up",new A(t,e,s,i))}dispose(){for(const t of this.collections)t.dispose();this.types=null}}class L{constructor(t,e){this.type=t,this.element=e,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+t,this.binding)}add(t){this.actions.push(t)}handle(t){for(const e of this.actions)e.handle(t)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class A{constructor(t,e,s,i){this.key=t,this.closure=e,this.preventDefault=!0===s,this.stopPropagation=!0===i}handle(t){t.keyCode===this.key&&(this.closure(t),this.preventDefault&&t.preventDefault(),this.stopPropagation&&t.stopPropagation())}}x.TAB=9,x.ESCAPE=27,x.END=35,x.HOME=36,x.LEFT=37,x.UP=38,x.RIGHT=39,x.DOWN=40;const S=e("collapse"),C=[],_={};class k extends v{constructor(t){super(t),C.push(this),this.requesting=this.request.bind(this),t.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const t in _){let e=this.element.parentElement;for(;e;){if(e.classList.contains(t))return void("string"==typeof _[t]?b.groupByParent(this,b,_[t]):b.groupByParent(this,_[t]));e=e.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return E.expand}static get selector(){return S}static register(t,e){_[t]=e;for(const t of C)t.gatherByAscendants()}transitionend(t){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(t){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(t)},window.requestAnimationFrame(this.requesting))}conceal(t,e){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(t,e)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const t=this.element.offsetHeight;this.element.style.setProperty("--collapse",-t+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}t.core.ns=e,t.core.addClass=i,t.core.removeClass=n,t.core.engine=o,t.core.Instance=u,t.core.Initializer=h,t.core.Disclosure=v,t.core.DisclosureButton=g,t.core.DisclosuresGroup=b,t.core.DISCLOSURE_TYPES=E,t.KeyListener=x,t.Collapse=k,t.Equisized=class{constructor(t,e){this.selector=t,this.group=e,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let t=0;t<this.elements.length;t++){const e=this._getWidth(this.elements[t]);e>this.maxWidth&&(this.maxWidth=e)}this.apply()}apply(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width=this.maxWidth+1+"px"}reset(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width="auto";this.maxWidth=0}_getWidth(t){let e=t.offsetWidth;const s=getComputedStyle(t);return e+=parseInt(s.marginLeft)+parseInt(s.marginRight),e}};new h(`.${S}`,[()=>{k.build(document)}]);const q=t.core.ns("accordions-group"),z=t.core.ns("accordion");class I extends t.core.DisclosuresGroup{static get selector(){return q}}t.AccordionsGroup=I,t.Collapse.register(z,I);const D=`${t.core.ns.selector("breadcrumb")} ${t.core.ns.selector("collapse")}`;class P extends t.core.Instance{constructor(e){super(e),this.collapse=t.core.Instance.getInstances(e,t.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(t.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),t.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new t.core.Initializer(D,[()=>{const t=[],e=document.querySelectorAll(D);for(let s=0;s<e.length;s++)t.push(new P(e[s]))}]);const O=t.core.ns.selector("btn"),R=t.core.ns.selector("btns-group"),T=t.core.ns.selector("btns-group--equisized");new t.core.Initializer(R,[()=>{const e=document.querySelectorAll(T),s=[];for(let i=0;i<e.length;i++)s.push(new t.Equisized(O,e[i]))}]);const G=t.core.ns.selector("modal"),N=t.core.ns("modal"),B=t.core.ns("no-scroll"),H=t.core.ns("scroll-shadow"),F=t.core.ns.selector("modal__body"),$=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),M=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),W=(t,e)=>{if("hidden"===window.getComputedStyle(t).visibility)return!1;for(void 0===e&&(e=t);e.contains(t);){if("none"===window.getComputedStyle(t).display)return!1;t=t.parentElement}return!0};class K{constructor(t,e){this.element=null,this.activeElement=null,this.onTrap=t,this.onUntrap=e,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(t){this.trapped&&this.untrap(),this.element=t,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){W(this.element)?this.trapping():t.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const t=this.focusables;t.length&&t[0].focus(),this.element.setAttribute("aria-modal",!0),window.addEventListener("keydown",this.handling),this.stunneds=[]}stun(t){for(const e of t.children)e!==this.element&&(e.contains(this.element)?this.stun(e):this.stunneds.push(new V(e)))}handle(t){if(9!==t.keyCode)return;const e=this.focusables;if(0===e.length)return;const s=e[0],i=e[e.length-1],n=e.indexOf(document.activeElement);t.shiftKey?!this.element.contains(document.activeElement)||n<1?(t.preventDefault(),i.focus()):(document.activeElement.tabIndex>0||e[n-1].tabIndex>0)&&(t.preventDefault(),e[n-1].focus()):this.element.contains(document.activeElement)&&n!==e.length-1&&-1!==n?document.activeElement.tabIndex>0&&(t.preventDefault(),e[n+1].focus()):(t.preventDefault(),s.focus())}get focusables(){let t=[...this.element.querySelectorAll($)];const e=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(e.length){const s={};for(const t of e){const e=t.getAttribute("name");void 0===s[e]&&(s[e]=new j(e)),s[e].push(t)}t=t.filter((t=>{if("input"!==t.tagName.toLowerCase()||"radio"!==t.getAttribute("type").toLowerCase())return!0;const e=t.getAttribute("name");return s[e].keep(t)}))}const s=[...this.element.querySelectorAll(M)];s.sort(((t,e)=>t.tabIndex-e.tabIndex));const i=t.filter((t=>-1===s.indexOf(t)));return s.concat(i).filter((t=>"-1"!==t.tabIndex&&W(t,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),window.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class V{constructor(t){this.element=t,this.hidden=t.getAttribute("aria-hidden"),this.inert=t.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class j{constructor(t){this.name=t,this.buttons=[]}push(t){this.buttons.push(t),(t===document.activeElement||t.checked||void 0===this.selected)&&(this.selected=t)}keep(t){return this.selected===t}}class U extends t.core.DisclosuresGroup{constructor(){super(),this.trap=new K}apply(t,e){super.apply(t,e),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const Y=new U;class J extends t.core.Disclosure{constructor(t){super(t),this.body=this.element.querySelector(F),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(t){this.body&&this.body!==t.target&&!this.body.contains(t.target)&&this.conceal()}gather(){Y.add(this)}disclose(t){return!!super.disclose(t)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(t,e){return!!super.conceal(t,e)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(t.core.removeClass(document.documentElement,B),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(B)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",t.core.addClass(document.documentElement,B))}resize(e,s){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?t.core.removeClass(this.body,H):t.core.addClass(this.body,H):t.core.removeClass(this.body,H),this.isMedium=window.matchMedia("(min-width: 48em)").matches,e&&(this.isMedium?this.body.style.removeProperty("max-height"):(this.body.style.maxHeight=window.innerHeight-32+"px",t.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"})))))}static get type(){return t.core.DISCLOSURE_TYPES.opened}static get selector(){return N}get GroupConstructor(){return U}}t.Modal=J,t.ModalsGroup=U,t.FocusTrap=K;new t.core.Initializer(G,[()=>{J.build(document)}]);const Q=t.core.ns("nav"),X=t.core.ns("nav__list"),Z=t.core.ns("nav__item"),tt=t.core.ns("nav__item--align-right"),et=t.core.ns("menu");class st extends t.core.DisclosuresGroup{constructor(t,e){super(t,e),this.menus=[],this.navList=e.querySelector(`.${X}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return Q}add(t){super.add(t),t.element.classList.contains(et)&&this.menus.push(new it(t,this.navList.getBoundingClientRect().right))}focusOut(t){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(t){-1===t&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=t}resize(){const t=this.navList.getBoundingClientRect().right;for(const e of this.menus)e.place(t)}}class it{constructor(t,e){this.initialize(t),this.place(e)}initialize(t){this.element=t.element;for(const e of t.buttons)if(e.hasAttribute){this.button=e.element;break}let e=this.element.parentElement;for(;e;){if(e.classList.contains(Z)){this.item=e;break}e=e.parentElement}}place(e){const s=getComputedStyle(this.element),i=parseFloat(s.width);this.button.getBoundingClientRect().left+i>e?t.core.addClass(this.item,tt):t.core.removeClass(this.item,tt)}}t.Navigation=st,t.Collapse.register(Q,st);const nt=t.core.ns.attr("theme"),rt=t.core.ns.attr("transition");class ot{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const t=this.root.getAttribute(nt);"dark"===t||"light"===t?this.scheme=t:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(rt)?(this.root.removeAttribute(rt),this.root.setAttribute(nt,"dark"),setTimeout((()=>{this.root.setAttribute(rt,"")}),300)):this.root.setAttribute(nt,"dark"):this.root.setAttribute(nt,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(t){t.forEach((t=>{if("attributes"===t.type&&t.attributeName===nt){const t=this.root.getAttribute(nt);"dark"===t?localStorage.setItem("scheme","dark"):"light"===t&&localStorage.setItem("scheme","light")}}))}}t.Scheme=ot;const ht=`input[name="${t.core.ns.selector("radios-theme","")}"]`,lt=t.core.ns.selector("switch-theme","#"),ct=t.core.ns.attr("theme");class at{constructor(){this.attributeName=ct,this.theme=null,this.radios=document.querySelectorAll(ht);for(var t=0;t<this.radios.length;t++)this.radios[t].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.attributeName&&this.apply()}))}apply(){const t=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var e=0;e<this.radios.length;e++)this.radios[e].checked=this.radios[e].value===t;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(ht+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new t.core.Initializer(`:root[${nt}]`,[()=>{new ot}]),new t.core.Initializer(`${lt}`,[()=>{new at}]);const dt=t.core.ns("sidemenu"),ut=t.core.ns("sidemenu__list");t.Collapse.register(dt,ut);const mt=t.core.ns.selector("table"),pt=t.core.ns("table--no-scroll"),bt=t.core.ns("table--shadow"),gt=t.core.ns("table--shadow-left"),ft=t.core.ns("table--shadow-right");class yt{constructor(t){this.init(t)}init(e){this.table=e,this.table.setAttribute(t.core.ns.attr("js-table"),"true"),this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0;const s=this.change.bind(this);this.tableElem.addEventListener("scroll",s)}change(){const t=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let e=this.tableElem.offsetWidth>this.table.offsetWidth;t||e?this.table.classList.contains(pt)||this.scroll():t!==this.isScrollable&&this.delete(),this.isScrollable=t,e=!1;const s=this.caption.getBoundingClientRect();this.table.style.setProperty("--table-offset",s.height+"px")}delete(){t.core.removeClass(this.table,ft),t.core.removeClass(this.table,gt),t.core.removeClass(this.table,bt),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){t.core.addClass(this.table,bt),this.setShadowPosition()}setShadowPosition(){const t=this.getScrollPosition("left"),e=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",t),this.setShadowVisibility("left",e)):(this.setShadowVisibility("left",t),this.setShadowVisibility("right",e))}getScrollPosition(t){let e=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(e=-1),t){case"left":return this.tableElem.scrollLeft*e;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*e;default:return!1}}setShadowVisibility(e,s){s<=1?"left"===e?t.core.removeClass(this.table,gt):"right"===e&&t.core.removeClass(this.table,ft):"left"===e?t.core.addClass(this.table,gt):"right"===e&&t.core.addClass(this.table,ft)}}t.Table=yt;const wt=[],vt=()=>{for(let t=0;t<wt.length;t++)wt[t].change()};new t.core.Initializer(mt,[()=>{const t=document.querySelectorAll(mt);for(let e=0;e<t.length;e++)wt.push(new yt(t[e]));window.addEventListener("resize",vt),window.addEventListener("orientationchange",vt),vt()}]);class Et extends t.core.DisclosureButton{apply(t){super.apply(t),this.hasAttribute&&this.element.setAttribute("tabindex",t?"0":"-1")}}const xt=t.core.ns.selector("tabs"),Lt=t.core.ns("tabs"),At=t.core.ns("tabs__tab"),St=t.core.ns("tabs__panel"),Ct=t.core.ns("tabs__list");class _t extends t.core.DisclosuresGroup{constructor(e,s){super(e,s),this.list=s.querySelector(`.${Ct}`),s.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),t.core.engine.renderer.add(this.render.bind(this))}static get selector(){return Lt}transitionend(t){this.element.style.transition="none"}init(){this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(At)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(At)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(At)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(At)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let t=0;t<this._index;t++)this.members[t].translate(-1);this.current.element.style.transition="",this.current.element.style.transform="";for(let t=this._index+1;t<this.length;t++)this.members[t].translate(1);this.element.style.transition=""}add(t){if(super.add(t),1===this.length||t.disclosed)this.current=t;else{const e=this.members.indexOf(t);this._index>-1&&this._index!==e&&t.translate(e<this._index?-1:1,!0)}}render(){if(null===this.current)return;const t=Math.round(this.current.element.offsetHeight);this.panelHeight!==t&&(this.panelHeight=t,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class kt extends t.core.Disclosure{static get type(){return t.core.DISCLOSURE_TYPES.select}static get selector(){return St}get GroupConstructor(){return _t}buttonFactory(t){return new Et(t,this)}translate(t,e){this.element.style.transition=e?"none":"",this.element.style.transform=`translate(${100*t}%)`}reset(){this.group.index=0}}t.Tab=kt,t.TabButton=Et,t.TabsGroup=_t;new t.core.Initializer(xt,[()=>{kt.build(document)}]);const qt=t.core.ns.selector("header"),zt=t.core.ns.selector("header__search"),It=t.core.ns.selector("header__menu"),Dt=t.core.ns.selector("header__tools-links"),Pt=t.core.ns.selector("header__menu-links"),Ot=`${Dt} ${t.core.ns.selector("links-group")}`;class Rt{constructor(t){this.header=t||document.querySelector(qt),this.modals=[],this.init()}getModal(e){const s=this.header.querySelector(e);if(!s)return;const i=t.core.Instance.getInstances(s,t.Modal);i&&i.length&&this.modals.push(new Tt(i[0]))}init(){this.getModal(zt),this.getModal(It),this.linksGroup=this.header.querySelector(Ot),this.toolsLinks=this.header.querySelector(Dt),this.menuLinks=this.header.querySelector(Pt),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge?this.modals.forEach((t=>t.disable())):this.modals.forEach((t=>t.enable())),null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}class Tt{constructor(t){this.modal=t}enable(){this.modal.element.setAttribute("role","dialog"),this.modal.element.setAttribute("aria-labelledby",this.modal.primary.element.id)}disable(){this.modal.conceal(),this.modal.element.removeAttribute("role"),this.modal.element.removeAttribute("aria-labelledby")}}t.Header=Rt;new t.core.Initializer(qt,[()=>{const t=Array.prototype.slice.call(document.querySelectorAll(qt)),e=[];for(const s of t)e.push(new Rt(s))}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class r{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(t){this.closures.push(t);return()=>{const e=this.closures.indexOf(t);-1!==e&&this.closures.splice(e,1)}}next(t,e){e=void 0===e?0:e-1,void 0===this.nexts[e]&&(this.nexts[e]=[]),this.nexts[e].push(t)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const t=this.nexts.shift();if(t)for(const e of t)e.call()}}const o=new class{constructor(){this.renderer=new r}register(t,e){}start(){}stop(){}};class h{constructor(t,e){this.selector=t,this.builders=e,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let t=0;t<this.builders.length;t++)this.instances.push(this.builders[t]())}}const l={},c={};let a=0;const d=t=>{for(const e in c)if(c[e]===t)return e;a++;const e=a;return c[e]=t,e};class u{constructor(t,e,s){const i=d(t);l[i]||(l[i]=[]),l[i].push(this),this.element=t,this.id=t.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=e,this.isRendering=s}dispatch(t,e){const s=new CustomEvent(t,e);this.element.dispatchEvent(s)}listen(t,e){this.listeners[t]||(this.listeners[t]=[]),this.listeners[t].indexOf(e)>-1||(this.listeners[t].push(e),this.element.addEventListener(t,e))}unlisten(t,e){if(t)if(e){if(!this.listeners[t])return;const s=this.listeners[t].indexOf(e);s>-1&&this.listeners[t].splice(s,1),this.element.removeEventListener(e)}else{if(!this.listeners[t])return;for(const e of this.listeners[t])this.element.removeEventListener(e);this.listeners[t].length=0}else for(const t in this.listeners)this.unlisten(t)}get isRendering(){return this._isRendering}set isRendering(t){this._isRendering!==t&&(this._isRendering=t)}render(){}get isResizing(){return this._isResizing}set isResizing(t){this._isResizing!==t&&(this._isResizing=t)}resize(){}destroy(){}static getInstances(t,e){const s=d(t);return l[s]?e?l[s].filter((t=>t instanceof e)):l[s]:null}}const m=e.attr("group"),p=[];class b{constructor(t,e){this.id=t,this.element=e,this.members=[],this._index=-1,this._current=null,p.push(this)}static getGroupById(t){for(const e of p)if(e.constructor===this&&e.id===t)return e;return new this(t)}static getGroupByElement(t){for(const e of p)if(e.element===t)return e;return new this(!1,t)}static groupById(t,e){const s=t.element.getAttribute(m);if(null===s)return;e.getGroupById(s).add(t)}static groupByParent(t,e,s){if(void 0===s&&(s=e.selector),""===s)return;let i=t.element.parentElement;for(;i;){if(i.classList.contains(t.constructor.selector))return;if(i.classList.contains(s)){return void e.getGroupByElement(i).add(t)}i=i.parentElement}}static get selector(){return""}add(t){if(-1===this.members.indexOf(t))switch(this.members.push(t),t.setGroup(this),!0){case null!==this.current:case!(t.disclosed||t.primary&&t.primary.disclosed):t.disclosed=!1;break;default:this._current=t,this._index=this.members.indexOf(t),t.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(t){t<-1||t>=this.length||this._index===t||(null!==this.current&&this.current.conceal(!0,!0),this._index=t,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(t){this.index=this.members.indexOf(t)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class g{constructor(t,e){this.element=t,this.disclosure=e,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(t){this.disclosure.change(this.hasAttribute)}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(t){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,t),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const f=e.event("DISCLOSE"),y=e.event("CONCEAL"),w=[];class v extends u{constructor(t){super(t),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:e.attr(this.type.id),this.pristine=!0;const s=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:e.attr.selector("controls",this.id));if(s.length>0)for(let t=0;t<s.length;t++)this.addButton(s[t]);this.disclosed=this.primary&&this.primary.disclosed,this.gather()}gather(){this.group||(b.groupById(this,this.GroupConstructor),b.groupByParent(this,this.GroupConstructor))}static build(t){const e=Array.prototype.slice.call(t.querySelectorAll(`.${this.selector}`));for(const t of e)w.push(new this(t))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(t){const e=this.buttonFactory(t);e.hasAttribute&&(void 0===this.primary?this.primary=e:e.apply(this.primary.disclosed)),this.buttons.push(e)}get GroupConstructor(){return b}buttonFactory(t){return new g(t,this)}disclose(t){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,t||void 0===this.group||(this.group.current=this),!0)}conceal(t,e){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,e||this.focus(),t||void 0===this.group||(this.group.current=null);for(const t of w)t!==this&&this.element.contains(t.element)&&t.reset();return!0}get disclosed(){return this._disclosed}set disclosed(t){if(this._disclosed!==t){this.dispatch(t?f:y,this.type),this._disclosed=t,t?i(this.element,this.modifier):n(this.element,this.modifier);for(let e=0;e<this.buttons.length;e++)this.buttons[e].apply(t)}}reset(){}change(t){if(this.constructor.type.canConceal)switch(!0){case!t:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(t){this.group=t}get buttonHasFocus(){return!!this.buttons.some((t=>t.hasFocus))}get hasFocus(){return this.element===document.activeElement||(this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus)}focus(){for(let t=0;t<this.buttons.length;t++){const e=this.buttons[t];if(e.hasAttribute)return void e.element.focus()}}}v.DISCLOSE_EVENT=f,v.CONCEAL_EVENT=y;const E={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class x{constructor(t){this.element=t,this.collections={}}_add(t,e){void 0===this.collections[t]&&(this.collections[t]=new L(t,this.element)),this.collections[t].add(e)}down(t,e,s,i){this._add("down",new A(t,e,s,i))}up(t,e,s,i){this._add("up",new A(t,e,s,i))}dispose(){for(const t of this.collections)t.dispose();this.types=null}}class L{constructor(t,e){this.type=t,this.element=e,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+t,this.binding)}add(t){this.actions.push(t)}handle(t){for(const e of this.actions)e.handle(t)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class A{constructor(t,e,s,i){this.key=t,this.closure=e,this.preventDefault=!0===s,this.stopPropagation=!0===i}handle(t){t.keyCode===this.key&&(this.closure(t),this.preventDefault&&t.preventDefault(),this.stopPropagation&&t.stopPropagation())}}x.TAB=9,x.ESCAPE=27,x.END=35,x.HOME=36,x.LEFT=37,x.UP=38,x.RIGHT=39,x.DOWN=40;const S=e("collapse"),C=[],_={};class k extends v{constructor(t){super(t),C.push(this),this.requesting=this.request.bind(this),t.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const t in _){let e=this.element.parentElement;for(;e;){if(e.classList.contains(t))return void("string"==typeof _[t]?b.groupByParent(this,b,_[t]):b.groupByParent(this,_[t]));e=e.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return E.expand}static get selector(){return S}static register(t,e){_[t]=e;for(const t of C)t.gatherByAscendants()}transitionend(t){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(t){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(t)},window.requestAnimationFrame(this.requesting))}conceal(t,e){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(t,e)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const t=this.element.offsetHeight;this.element.style.setProperty("--collapse",-t+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}t.core.ns=e,t.core.addClass=i,t.core.removeClass=n,t.core.engine=o,t.core.Instance=u,t.core.Initializer=h,t.core.Disclosure=v,t.core.DisclosureButton=g,t.core.DisclosuresGroup=b,t.core.DISCLOSURE_TYPES=E,t.KeyListener=x,t.Collapse=k,t.Equisized=class{constructor(t,e){this.selector=t,this.group=e,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let t=0;t<this.elements.length;t++){const e=this._getWidth(this.elements[t]);e>this.maxWidth&&(this.maxWidth=e)}this.apply()}apply(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width=this.maxWidth+1+"px"}reset(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width="auto";this.maxWidth=0}_getWidth(t){let e=t.offsetWidth;const s=getComputedStyle(t);return e+=parseInt(s.marginLeft)+parseInt(s.marginRight),e}};new h(`.${S}`,[()=>{k.build(document)}]);const q=t.core.ns("accordions-group"),z=t.core.ns("accordion");class I extends t.core.DisclosuresGroup{static get selector(){return q}}t.AccordionsGroup=I,t.Collapse.register(z,I);const D=`${t.core.ns.selector("breadcrumb")} ${t.core.ns.selector("collapse")}`;class P extends t.core.Instance{constructor(e){super(e),this.collapse=t.core.Instance.getInstances(e,t.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(t.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),t.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new t.core.Initializer(D,[()=>{const t=[],e=document.querySelectorAll(D);for(let s=0;s<e.length;s++)t.push(new P(e[s]))}]);const O=t.core.ns.selector("btn"),R=t.core.ns.selector("btns-group"),T=t.core.ns.selector("btns-group--equisized");new t.core.Initializer(R,[()=>{const e=document.querySelectorAll(T),s=[];for(let i=0;i<e.length;i++)s.push(new t.Equisized(O,e[i]))}]);const G=t.core.ns.selector("modal"),N=t.core.ns("modal"),B=t.core.ns("no-scroll"),H=t.core.ns("scroll-shadow"),F=t.core.ns.selector("modal__body"),$=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),M=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),W=(t,e)=>{if("hidden"===window.getComputedStyle(t).visibility)return!1;for(void 0===e&&(e=t);e.contains(t);){if("none"===window.getComputedStyle(t).display)return!1;t=t.parentElement}return!0};class K{constructor(t,e){this.element=null,this.activeElement=null,this.onTrap=t,this.onUntrap=e,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(t){this.trapped&&this.untrap(),this.element=t,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){W(this.element)?this.trapping():t.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const t=this.focusables;t.length&&t[0].focus(),this.element.setAttribute("aria-modal",!0),window.addEventListener("keydown",this.handling),this.stunneds=[]}stun(t){for(const e of t.children)e!==this.element&&(e.contains(this.element)?this.stun(e):this.stunneds.push(new V(e)))}handle(t){if(9!==t.keyCode)return;const e=this.focusables;if(0===e.length)return;const s=e[0],i=e[e.length-1],n=e.indexOf(document.activeElement);t.shiftKey?!this.element.contains(document.activeElement)||n<1?(t.preventDefault(),i.focus()):(document.activeElement.tabIndex>0||e[n-1].tabIndex>0)&&(t.preventDefault(),e[n-1].focus()):this.element.contains(document.activeElement)&&n!==e.length-1&&-1!==n?document.activeElement.tabIndex>0&&(t.preventDefault(),e[n+1].focus()):(t.preventDefault(),s.focus())}get focusables(){let t=[...this.element.querySelectorAll($)];const e=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(e.length){const s={};for(const t of e){const e=t.getAttribute("name");void 0===s[e]&&(s[e]=new j(e)),s[e].push(t)}t=t.filter((t=>{if("input"!==t.tagName.toLowerCase()||"radio"!==t.getAttribute("type").toLowerCase())return!0;const e=t.getAttribute("name");return s[e].keep(t)}))}const s=[...this.element.querySelectorAll(M)];s.sort(((t,e)=>t.tabIndex-e.tabIndex));const i=t.filter((t=>-1===s.indexOf(t)));return s.concat(i).filter((t=>"-1"!==t.tabIndex&&W(t,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),window.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class V{constructor(t){this.element=t,this.hidden=t.getAttribute("aria-hidden"),this.inert=t.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class j{constructor(t){this.name=t,this.buttons=[]}push(t){this.buttons.push(t),(t===document.activeElement||t.checked||void 0===this.selected)&&(this.selected=t)}keep(t){return this.selected===t}}class U extends t.core.DisclosuresGroup{constructor(){super(),this.trap=new K}apply(t,e){super.apply(t,e),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const Y=new U;class J extends t.core.Disclosure{constructor(t){super(t),this.body=this.element.querySelector(F),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(t){this.body&&this.body!==t.target&&!this.body.contains(t.target)&&this.conceal()}gather(){Y.add(this)}disclose(t){return!!super.disclose(t)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(t,e){return!!super.conceal(t,e)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(t.core.removeClass(document.documentElement,B),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(B)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",t.core.addClass(document.documentElement,B))}resize(e,s){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?t.core.removeClass(this.body,H):t.core.addClass(this.body,H):t.core.removeClass(this.body,H),this.isMedium=window.matchMedia("(min-width: 48em)").matches,e&&(this.isMedium?this.body.style.removeProperty("max-height"):(this.body.style.maxHeight=window.innerHeight-32+"px",t.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"})))))}static get type(){return t.core.DISCLOSURE_TYPES.opened}static get selector(){return N}get GroupConstructor(){return U}}t.Modal=J,t.ModalsGroup=U,t.FocusTrap=K;new t.core.Initializer(G,[()=>{J.build(document)}]);const Q=t.core.ns("nav"),X=t.core.ns("nav__list"),Z=t.core.ns("nav__item"),tt=t.core.ns("nav__item--align-right"),et=t.core.ns("menu");class st extends t.core.DisclosuresGroup{constructor(t,e){super(t,e),this.menus=[],this.navList=e.querySelector(`.${X}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return Q}add(t){super.add(t),t.element.classList.contains(et)&&this.menus.push(new it(t,this.navList.getBoundingClientRect().right))}focusOut(t){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(t){-1===t&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=t}resize(){const t=this.navList.getBoundingClientRect().right;for(const e of this.menus)e.place(t)}}class it{constructor(t,e){this.initialize(t),this.place(e)}initialize(t){this.element=t.element;for(const e of t.buttons)if(e.hasAttribute){this.button=e.element;break}let e=this.element.parentElement;for(;e;){if(e.classList.contains(Z)){this.item=e;break}e=e.parentElement}}place(e){const s=getComputedStyle(this.element),i=parseFloat(s.width);this.button.getBoundingClientRect().left+i>e?t.core.addClass(this.item,tt):t.core.removeClass(this.item,tt)}}t.Navigation=st,t.Collapse.register(Q,st);const nt=t.core.ns.attr("theme"),rt=t.core.ns.attr("transition");class ot{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const t=this.root.getAttribute(nt);"dark"===t||"light"===t?this.scheme=t:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(rt)?(this.root.removeAttribute(rt),this.root.setAttribute(nt,"dark"),setTimeout((()=>{this.root.setAttribute(rt,"")}),300)):this.root.setAttribute(nt,"dark"):this.root.setAttribute(nt,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(t){t.forEach((t=>{if("attributes"===t.type&&t.attributeName===nt){const t=this.root.getAttribute(nt);"dark"===t?localStorage.setItem("scheme","dark"):"light"===t&&localStorage.setItem("scheme","light")}}))}}t.Scheme=ot;const ht=`input[name="${t.core.ns.selector("radios-theme","")}"]`,lt=t.core.ns.selector("switch-theme","#"),ct=t.core.ns.attr("theme");class at{constructor(){this.attributeName=ct,this.theme=null,this.radios=document.querySelectorAll(ht);for(var t=0;t<this.radios.length;t++)this.radios[t].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.attributeName&&this.apply()}))}apply(){const t=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var e=0;e<this.radios.length;e++)this.radios[e].checked=this.radios[e].value===t;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(ht+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new t.core.Initializer(`:root[${nt}]`,[()=>{new ot}]),new t.core.Initializer(`${lt}`,[()=>{new at}]);const dt=t.core.ns("sidemenu"),ut=t.core.ns("sidemenu__list");t.Collapse.register(dt,ut);const mt=t.core.ns.selector("table"),pt=t.core.ns("table--no-scroll"),bt=t.core.ns("table--shadow"),gt=t.core.ns("table--shadow-left"),ft=t.core.ns("table--shadow-right");class yt{constructor(t){this.init(t)}init(e){this.table=e,this.table.setAttribute(t.core.ns.attr("js-table"),"true"),this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0;const s=this.change.bind(this);this.tableElem.addEventListener("scroll",s)}change(){const t=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let e=this.tableElem.offsetWidth>this.table.offsetWidth;t||e?this.table.classList.contains(pt)||this.scroll():t!==this.isScrollable&&this.delete(),this.isScrollable=t,e=!1;const s=this.caption.getBoundingClientRect();this.table.style.setProperty("--table-offset",s.height+"px")}delete(){t.core.removeClass(this.table,ft),t.core.removeClass(this.table,gt),t.core.removeClass(this.table,bt),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){t.core.addClass(this.table,bt),this.setShadowPosition()}setShadowPosition(){const t=this.getScrollPosition("left"),e=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",t),this.setShadowVisibility("left",e)):(this.setShadowVisibility("left",t),this.setShadowVisibility("right",e))}getScrollPosition(t){let e=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(e=-1),t){case"left":return this.tableElem.scrollLeft*e;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*e;default:return!1}}setShadowVisibility(e,s){s<=1?"left"===e?t.core.removeClass(this.table,gt):"right"===e&&t.core.removeClass(this.table,ft):"left"===e?t.core.addClass(this.table,gt):"right"===e&&t.core.addClass(this.table,ft)}}t.Table=yt;const wt=[],vt=()=>{for(let t=0;t<wt.length;t++)wt[t].change()};new t.core.Initializer(mt,[()=>{const t=document.querySelectorAll(mt);for(let e=0;e<t.length;e++)wt.push(new yt(t[e]));window.addEventListener("resize",vt),window.addEventListener("orientationchange",vt),vt()}]);class Et extends t.core.DisclosureButton{apply(t){super.apply(t),this.hasAttribute&&this.element.setAttribute("tabindex",t?"0":"-1")}}const xt=t.core.ns.selector("tabs"),Lt=t.core.ns("tabs"),At=t.core.ns("tabs__tab"),St=t.core.ns("tabs__panel"),Ct=t.core.ns("tabs__list");class _t extends t.core.DisclosuresGroup{constructor(e,s){super(e,s),this.list=s.querySelector(`.${Ct}`),s.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),t.core.engine.renderer.add(this.render.bind(this))}static get selector(){return Lt}transitionend(t){this.element.style.transition="none"}init(){this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(At)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(At)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(At)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(At)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let t=0;t<this._index;t++)this.members[t].translate(-1);this.current.element.style.transition="",this.current.element.style.transform="";for(let t=this._index+1;t<this.length;t++)this.members[t].translate(1);this.element.style.transition=""}add(t){if(super.add(t),1===this.length||t.disclosed)this.current=t;else{const e=this.members.indexOf(t);this._index>-1&&this._index!==e&&t.translate(e<this._index?-1:1,!0)}}render(){if(null===this.current)return;const t=Math.round(this.current.element.offsetHeight);this.panelHeight!==t&&(this.panelHeight=t,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class kt extends t.core.Disclosure{static get type(){return t.core.DISCLOSURE_TYPES.select}static get selector(){return St}get GroupConstructor(){return _t}buttonFactory(t){return new Et(t,this)}translate(t,e){this.element.style.transition=e?"none":"",this.element.style.transform=`translate(${100*t}%)`}reset(){this.group.index=0}}t.Tab=kt,t.TabButton=Et,t.TabsGroup=_t;new t.core.Initializer(xt,[()=>{kt.build(document)}]);const qt=t.core.ns.selector("header"),zt=t.core.ns.selector("header__search"),It=t.core.ns.selector("header__menu"),Dt=t.core.ns.selector("header__tools-links"),Pt=t.core.ns.selector("header__menu-links"),Ot=`${Dt} ${t.core.ns.selector("links-group")}`;class Rt{constructor(t){this.header=t||document.querySelector(qt),this.modals=[],this.init()}getModal(e){const s=this.header.querySelector(e);if(!s)return;const i=t.core.Instance.getInstances(s,t.Modal);i&&i.length&&this.modals.push(new Tt(i[0]))}init(){this.getModal(zt),this.getModal(It),this.linksGroup=this.header.querySelector(Ot),this.toolsLinks=this.header.querySelector(Dt),this.menuLinks=this.header.querySelector(Pt),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge?this.modals.forEach((t=>t.disable())):this.modals.forEach((t=>t.enable())),null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}class Tt{constructor(t){this.modal=t}enable(){this.modal.element.setAttribute("role","dialog"),this.modal.element.setAttribute("aria-labelledby",this.modal.primary.element.id)}disable(){this.modal.conceal(),this.modal.element.removeAttribute("role"),this.modal.element.removeAttribute("aria-labelledby")}}t.Header=Rt;new t.core.Initializer(qt,[()=>{const t=Array.prototype.slice.call(document.querySelectorAll(qt)),e=[];for(const s of t)e.push(new Rt(s))}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/accessibilit%C3%A9/](https://envergo.beta.gouv.fr/accessibilit%C3%A9/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/robots.txt](https://envergo.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/accessibilit%C3%A9/](https://envergo.beta.gouv.fr/accessibilit%C3%A9/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.059558abd249.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.059558abd249.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/sitemap.xml](https://envergo.beta.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `daTRKwflYBT5CPIaF1a0TDritDGyrUpp0NXg9FYYyKOuejgtZZ2q4OAIIyUWb8Yk`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `8K5uxhWp0P4JuVQyXynudkEhy5lyJh0aWGs4pQ8XiuR1AmlTwQMFC6b2oe7Z7nSP`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `8K5uxhWp0P4JuVQyXynudkEhy5lyJh0aWGs4pQ8XiuR1AmlTwQMFC6b2oe7Z7nSP`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8K5uxhWp0P4JuVQyXynudkEhy5lyJh0aWGs4pQ8XiuR1AmlTwQMFC6b2oe7Z7nSP`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/codes/article_lc/LEGIARTI000042075042/2020-09-01/`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>u��+\x0007�`\x0014�\x0008�\x001a\x0017V�L:�1��Ji����V\x0018ȣ�z8-e����\x0008#%\x0016o�$</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.059558abd249.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.059558abd249.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FIXME`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.0ecb3d0e58d5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected 60 times, the first in the element starting with: "        function Dsn(from) {
", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/accessibilit%C3%A9/](https://envergo.beta.gouv.fr/accessibilit%C3%A9/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-breadcrumb__link" aria-current="page">Déclaration d'accessibilité</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-breadcrumb__link" aria-current="page">Contact</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js](https://envergo.beta.gouv.fr/static/@sentry/browser/build/bundle.1ab9f78138e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a/>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-breadcrumb__link" aria-current="page">Mentions légales</a>`
  
  
  
  
Instances: 5
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.7718992eb76d.svg](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.7718992eb76d.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/sitemap.xml](https://envergo.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/apple-touch-icon.09be1cc5f435.png](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/apple-touch-icon.09be1cc5f435.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/robots.txt](https://envergo.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/accessibilit%C3%A9/](https://envergo.beta.gouv.fr/accessibilit%C3%A9/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `444444444`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.baccb28accdd.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>31449600, which evaluates to: 1970-12-31 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `application_number`
  
  
  
  
Instances: 1
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://envergo.beta.gouv.fr/</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>application_number=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

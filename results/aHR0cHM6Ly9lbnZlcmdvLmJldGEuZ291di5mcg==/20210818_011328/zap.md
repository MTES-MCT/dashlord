
# ZAP Scanning Report

Generated on Wed, 18 Aug 2021 01:04:58


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 2 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 9 | 
| Cross-Domain Misconfiguration | Medium | 8 | 
| Reverse Tabnabbing | Medium | 9 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Incomplete or No Cache-control Header Set | Low | 7 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 6 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 4 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 5 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 1 | 

## Alert Detail


  
  
  
  
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
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.dde91426db6e.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.dde91426db6e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/images/capture_cerfa.ae8cd9f9371e.png](https://envergo.beta.gouv.fr/static/images/capture_cerfa.ae8cd9f9371e.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/apple-touch-icon.09be1cc5f435.png](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/apple-touch-icon.09be1cc5f435.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/css/project.a9bf09099778.css](https://envergo.beta.gouv.fr/static/css/project.a9bf09099778.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/favicons/favicon.643092a0caac.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 8
  
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
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener"
    href="https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000042075042/2020-09-01/">inscrite dans l'article
    R
    214-1 du Code de l'Environnement</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/robots.txt](https://envergo.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/MTES-MCT/envergo" target="_blank" rel="noopener">Voir le
          code source</a>`
  
  
  
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class r{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(t){this.closures.push(t);return()=>{const e=this.closures.indexOf(t);-1!==e&&this.closures.splice(e,1)}}next(t,e){e=void 0===e?0:e-1,void 0===this.nexts[e]&&(this.nexts[e]=[]),this.nexts[e].push(t)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const t=this.nexts.shift();if(t)for(const e of t)e.call()}}const o=new class{constructor(){this.renderer=new r}register(t,e){}start(){}stop(){}};class h{constructor(t,e){this.selector=t,this.builders=e,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let t=0;t<this.builders.length;t++)this.instances.push(this.builders[t]())}}const l={},c={};let a=0;const d=t=>{for(const e in c)if(c[e]===t)return e;a++;const e=a;return c[e]=t,e};class u{constructor(t,e,s){const i=d(t);l[i]||(l[i]=[]),l[i].push(this),this.element=t,this.id=t.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=e,this.isRendering=s}dispatch(t,e){const s=new CustomEvent(t,e);this.element.dispatchEvent(s)}listen(t,e){this.listeners[t]||(this.listeners[t]=[]),this.listeners[t].indexOf(e)>-1||(this.listeners[t].push(e),this.element.addEventListener(t,e))}unlisten(t,e){if(t)if(e){if(!this.listeners[t])return;const s=this.listeners[t].indexOf(e);s>-1&&this.listeners[t].splice(s,1),this.element.removeEventListener(e)}else{if(!this.listeners[t])return;for(const e of this.listeners[t])this.element.removeEventListener(e);this.listeners[t].length=0}else for(const t in this.listeners)this.unlisten(t)}get isRendering(){return this._isRendering}set isRendering(t){this._isRendering!==t&&(this._isRendering=t)}render(){}get isResizing(){return this._isResizing}set isResizing(t){this._isResizing!==t&&(this._isResizing=t)}resize(){}destroy(){}static getInstances(t,e){const s=d(t);return l[s]?e?l[s].filter((t=>t instanceof e)):l[s]:null}}const m=e.attr("group"),p=[];class b{constructor(t,e){this.id=t,this.element=e,this.members=[],this._index=-1,this._current=null,p.push(this)}static getGroupById(t){for(const e of p)if(e.constructor===this&&e.id===t)return e;return new this(t)}static getGroupByElement(t){for(const e of p)if(e.element===t)return e;return new this(!1,t)}static groupById(t,e){const s=t.element.getAttribute(m);if(null===s)return;e.getGroupById(s).add(t)}static groupByParent(t,e,s){if(void 0===s&&(s=e.selector),""===s)return;let i=t.element.parentElement;for(;i;){if(i.classList.contains(t.constructor.selector))return;if(i.classList.contains(s)){return void e.getGroupByElement(i).add(t)}i=i.parentElement}}static get selector(){return""}add(t){if(-1===this.members.indexOf(t))switch(this.members.push(t),t.setGroup(this),!0){case null!==this.current:case!(t.disclosed||t.primary&&t.primary.disclosed):t.disclosed=!1;break;default:this._current=t,this._index=this.members.indexOf(t),t.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(t){t<-1||t>=this.length||this._index===t||(null!==this.current&&this.current.conceal(!0,!0),this._index=t,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(t){this.index=this.members.indexOf(t)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class g{constructor(t,e){this.element=t,this.disclosure=e,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(t){this.disclosure.change(this.hasAttribute)}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(t){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,t),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const f=e.event("DISCLOSE"),y=e.event("CONCEAL"),w=[];class v extends u{constructor(t){super(t),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:e.attr(this.type.id),this.pristine=!0;const s=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:e.attr.selector("controls",this.id));if(s.length>0)for(let t=0;t<s.length;t++)this.addButton(s[t]);this.disclosed=this.primary&&this.primary.disclosed,this.gather()}gather(){this.group||(b.groupById(this,this.GroupConstructor),b.groupByParent(this,this.GroupConstructor))}static build(t){const e=Array.prototype.slice.call(t.querySelectorAll(`.${this.selector}`));for(const t of e)w.push(new this(t))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(t){const e=this.buttonFactory(t);e.hasAttribute&&(void 0===this.primary?this.primary=e:e.apply(this.primary.disclosed)),this.buttons.push(e)}get GroupConstructor(){return b}buttonFactory(t){return new g(t,this)}disclose(t){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,t||void 0===this.group||(this.group.current=this),!0)}conceal(t,e){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,e||this.focus(),t||void 0===this.group||(this.group.current=null);for(const t of w)t!==this&&this.element.contains(t.element)&&t.reset();return!0}get disclosed(){return this._disclosed}set disclosed(t){if(this._disclosed!==t){this.dispatch(t?f:y,this.type),this._disclosed=t,t?i(this.element,this.modifier):n(this.element,this.modifier);for(let e=0;e<this.buttons.length;e++)this.buttons[e].apply(t)}}reset(){}change(t){if(this.constructor.type.canConceal)switch(!0){case!t:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(t){this.group=t}get buttonHasFocus(){return!!this.buttons.some((t=>t.hasFocus))}get hasFocus(){return this.element===document.activeElement||(this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus)}focus(){for(let t=0;t<this.buttons.length;t++){const e=this.buttons[t];if(e.hasAttribute)return void e.element.focus()}}}v.DISCLOSE_EVENT=f,v.CONCEAL_EVENT=y;const E={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class x{constructor(t){this.element=t,this.collections={}}_add(t,e){void 0===this.collections[t]&&(this.collections[t]=new L(t,this.element)),this.collections[t].add(e)}down(t,e,s,i){this._add("down",new A(t,e,s,i))}up(t,e,s,i){this._add("up",new A(t,e,s,i))}dispose(){for(const t of this.collections)t.dispose();this.types=null}}class L{constructor(t,e){this.type=t,this.element=e,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+t,this.binding)}add(t){this.actions.push(t)}handle(t){for(const e of this.actions)e.handle(t)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class A{constructor(t,e,s,i){this.key=t,this.closure=e,this.preventDefault=!0===s,this.stopPropagation=!0===i}handle(t){t.keyCode===this.key&&(this.closure(t),this.preventDefault&&t.preventDefault(),this.stopPropagation&&t.stopPropagation())}}x.TAB=9,x.ESCAPE=27,x.END=35,x.HOME=36,x.LEFT=37,x.UP=38,x.RIGHT=39,x.DOWN=40;const S=e("collapse"),C=[],_={};class k extends v{constructor(t){super(t),C.push(this),this.requesting=this.request.bind(this),t.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const t in _){let e=this.element.parentElement;for(;e;){if(e.classList.contains(t))return void("string"==typeof _[t]?b.groupByParent(this,b,_[t]):b.groupByParent(this,_[t]));e=e.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return E.expand}static get selector(){return S}static register(t,e){_[t]=e;for(const t of C)t.gatherByAscendants()}transitionend(t){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(t){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(t)},window.requestAnimationFrame(this.requesting))}conceal(t,e){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(t,e)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const t=this.element.offsetHeight;this.element.style.setProperty("--collapse",-t+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}t.core.ns=e,t.core.addClass=i,t.core.removeClass=n,t.core.engine=o,t.core.Instance=u,t.core.Initializer=h,t.core.Disclosure=v,t.core.DisclosureButton=g,t.core.DisclosuresGroup=b,t.core.DISCLOSURE_TYPES=E,t.KeyListener=x,t.Collapse=k,t.Equisized=class{constructor(t,e){this.selector=t,this.group=e,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let t=0;t<this.elements.length;t++){const e=this._getWidth(this.elements[t]);e>this.maxWidth&&(this.maxWidth=e)}this.apply()}apply(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width=this.maxWidth+1+"px"}reset(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width="auto";this.maxWidth=0}_getWidth(t){let e=t.offsetWidth;const s=getComputedStyle(t);return e+=parseInt(s.marginLeft)+parseInt(s.marginRight),e}};new h(`.${S}`,[()=>{k.build(document)}]);const q=t.core.ns("accordions-group"),I=t.core.ns("accordion");class z extends t.core.DisclosuresGroup{static get selector(){return q}}t.AccordionsGroup=z,t.Collapse.register(I,z);const D=`${t.core.ns.selector("breadcrumb")} ${t.core.ns.selector("collapse")}`;class H extends t.core.Instance{constructor(e){super(e),this.collapse=t.core.Instance.getInstances(e,t.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(t.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),t.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new t.core.Initializer(D,[()=>{const t=[],e=document.querySelectorAll(D);for(let s=0;s<e.length;s++)t.push(new H(e[s]))}]);const P=t.core.ns.selector("btn"),O=t.core.ns.selector("btns-group"),T=t.core.ns.selector("btns-group--equisized");new t.core.Initializer(O,[()=>{const e=document.querySelectorAll(T),s=[];for(let i=0;i<e.length;i++)s.push(new t.Equisized(P,e[i]))}]);const B=t.core.ns.selector("modal"),N=t.core.ns("modal"),G=t.core.ns("no-scroll"),R=t.core.ns("scroll-shadow"),$=t.core.ns.selector("modal__body"),F=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),M=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),W=(t,e)=>{if("hidden"===window.getComputedStyle(t).visibility)return!1;for(void 0===e&&(e=t);e.contains(t);){if("none"===window.getComputedStyle(t).display)return!1;t=t.parentElement}return!0};class K{constructor(t,e){this.element=null,this.activeElement=null,this.onTrap=t,this.onUntrap=e,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(t){this.trapped&&this.untrap(),this.element=t,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){W(this.element)?this.trapping():t.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const t=this.focusables;t.length&&t[0].focus(),this.element.setAttribute("aria-modal",!0),window.addEventListener("keydown",this.handling),this.stunneds=[]}stun(t){for(const e of t.children)e!==this.element&&(e.contains(this.element)?this.stun(e):this.stunneds.push(new V(e)))}handle(t){if(9!==t.keyCode)return;const e=this.focusables;if(0===e.length)return;const s=e[0],i=e[e.length-1],n=e.indexOf(document.activeElement);t.shiftKey?!this.element.contains(document.activeElement)||n<1?(t.preventDefault(),i.focus()):(document.activeElement.tabIndex>0||e[n-1].tabIndex>0)&&(t.preventDefault(),e[n-1].focus()):this.element.contains(document.activeElement)&&n!==e.length-1&&-1!==n?document.activeElement.tabIndex>0&&(t.preventDefault(),e[n+1].focus()):(t.preventDefault(),s.focus())}get focusables(){let t=[...this.element.querySelectorAll(F)];const e=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(e.length){const s={};for(const t of e){const e=t.getAttribute("name");void 0===s[e]&&(s[e]=new U(e)),s[e].push(t)}t=t.filter((t=>{if("input"!==t.tagName.toLowerCase()||"radio"!==t.getAttribute("type").toLowerCase())return!0;const e=t.getAttribute("name");return s[e].keep(t)}))}const s=[...this.element.querySelectorAll(M)];s.sort(((t,e)=>t.tabIndex-e.tabIndex));const i=t.filter((t=>-1===s.indexOf(t)));return s.concat(i).filter((t=>"-1"!==t.tabIndex&&W(t,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),window.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class V{constructor(t){this.element=t,this.hidden=t.getAttribute("aria-hidden"),this.inert=t.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class U{constructor(t){this.name=t,this.buttons=[]}push(t){this.buttons.push(t),(t===document.activeElement||t.checked||void 0===this.selected)&&(this.selected=t)}keep(t){return this.selected===t}}class j extends t.core.DisclosuresGroup{constructor(){super(),this.trap=new K}apply(t,e){super.apply(t,e),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const Y=new j;class J extends t.core.Disclosure{constructor(t){super(t),this.body=this.element.querySelector($),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(t){this.body&&this.body!==t.target&&!this.body.contains(t.target)&&this.conceal()}gather(){Y.add(this)}disclose(t){return!!super.disclose(t)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(t,e){return!!super.conceal(t,e)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(t.core.removeClass(document.documentElement,G),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(G)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",t.core.addClass(document.documentElement,G))}resize(e,s){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?t.core.removeClass(this.body,R):t.core.addClass(this.body,R):t.core.removeClass(this.body,R),this.isMedium=window.matchMedia("(min-width: 48em)").matches,e&&(this.isMedium?this.body.style.removeProperty("max-height"):(this.body.style.maxHeight=window.innerHeight-32+"px",t.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"})))))}static get type(){return t.core.DISCLOSURE_TYPES.opened}static get selector(){return N}get GroupConstructor(){return j}}t.Modal=J,t.ModalsGroup=j,t.FocusTrap=K;new t.core.Initializer(B,[()=>{J.build(document)}]);const Q=t.core.ns("nav"),X=t.core.ns("nav__list"),Z=t.core.ns("nav__item"),tt=t.core.ns("nav__item--align-right"),et=t.core.ns("menu");class st extends t.core.DisclosuresGroup{constructor(t,e){super(t,e),this.menus=[],this.navList=e.querySelector(`.${X}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return Q}add(t){super.add(t),t.element.classList.contains(et)&&this.menus.push(new it(t,this.navList.getBoundingClientRect().right))}focusOut(t){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(t){-1===t&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=t}resize(){const t=this.navList.getBoundingClientRect().right;for(const e of this.menus)e.place(t)}}class it{constructor(t,e){this.initialize(t),this.place(e)}initialize(t){this.element=t.element;for(const e of t.buttons)if(e.hasAttribute){this.button=e.element;break}let e=this.element.parentElement;for(;e;){if(e.classList.contains(Z)){this.item=e;break}e=e.parentElement}}place(e){const s=getComputedStyle(this.element),i=parseFloat(s.width);this.button.getBoundingClientRect().left+i>e?t.core.addClass(this.item,tt):t.core.removeClass(this.item,tt)}}t.Navigation=st,t.Collapse.register(Q,st);const nt=t.core.ns.attr("theme"),rt=t.core.ns.attr("transition");class ot{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const t=this.root.getAttribute(nt);"dark"===t||"light"===t?this.scheme=t:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(rt)?(this.root.removeAttribute(rt),this.root.setAttribute(nt,"dark"),setTimeout((()=>{this.root.setAttribute(rt,"")}),300)):this.root.setAttribute(nt,"dark"):this.root.setAttribute(nt,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(t){t.forEach((t=>{if("attributes"===t.type&&t.attributeName===nt){const t=this.root.getAttribute(nt);"dark"===t?localStorage.setItem("scheme","dark"):"light"===t&&localStorage.setItem("scheme","light")}}))}}t.Scheme=ot;const ht=`input[name="${t.core.ns.selector("radios-theme","")}"]`,lt=t.core.ns.selector("switch-theme","#"),ct=t.core.ns.attr("theme");class at{constructor(){this.attributeName=ct,this.theme=null,this.radios=document.querySelectorAll(ht);for(var t=0;t<this.radios.length;t++)this.radios[t].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.attributeName&&this.apply()}))}apply(){const t=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var e=0;e<this.radios.length;e++)this.radios[e].checked=this.radios[e].value===t;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(ht+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new t.core.Initializer(`:root[${nt}]`,[()=>{new ot}]),new t.core.Initializer(`${lt}`,[()=>{new at}]);const dt=t.core.ns("sidemenu"),ut=t.core.ns("sidemenu__list");t.Collapse.register(dt,ut);const mt=t.core.ns.selector("table"),pt=`${t.core.ns.selector("table")}:not(${t.core.ns.selector("table--no-scroll")})`,bt=t.core.ns("table--shadow"),gt=t.core.ns("table--shadow-left"),ft=t.core.ns("table--shadow-right"),yt=t.core.ns("table__wrapper"),wt=t.core.ns("table--caption-bottom");class vt{constructor(t){this.init(t)}init(t){this.table=t,this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0,this.wrap();const e=this.change.bind(this);this.tableElem.addEventListener("scroll",e),this.change()}change(){const t=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let e=this.tableElem.offsetWidth>this.table.offsetWidth;t||e?(this.scroll(),this.handleCaption()):t!==this.isScrollable&&this.delete(),this.isScrollable=t,e=!1}delete(){t.core.removeClass(this.table,ft),t.core.removeClass(this.table,gt),t.core.removeClass(this.table,bt),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){t.core.addClass(this.table,bt),this.setShadowPosition()}wrap(){const t=document.createElement("div");t.className=yt,this.table.insertBefore(t,this.tableElem),t.appendChild(this.tableElem),this.tableInnerWrapper=t}setShadowPosition(){const t=this.getScrollPosition("left"),e=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",t),this.setShadowVisibility("left",e)):(this.setShadowVisibility("left",t),this.setShadowVisibility("right",e))}getScrollPosition(t){let e=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(e=-1),t){case"left":return this.tableElem.scrollLeft*e;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*e;default:return!1}}handleCaption(){if(this.caption){const t=getComputedStyle(this.caption),e=this.caption.offsetHeight+parseInt(t.marginTop)+parseInt(t.marginBottom);this.captionHeight=e,this.table.classList.contains(wt)?(this.tableElem.style.marginBottom=this.captionHeight+"px",this.caption.style.bottom=-this.captionHeight+"px"):(this.tableElem.style.marginTop=this.captionHeight+"px",this.caption.style.top=-this.captionHeight+"px")}}setShadowVisibility(e,s){s<=1?"left"===e?t.core.removeClass(this.table,gt):"right"===e&&t.core.removeClass(this.table,ft):"left"===e?t.core.addClass(this.table,gt):"right"===e&&t.core.addClass(this.table,ft)}}t.Table=vt;const Et=[],xt=()=>{for(let t=0;t<Et.length;t++)Et[t].change()};new t.core.Initializer(mt,[()=>{const t=document.querySelectorAll(pt);for(let e=0;e<t.length;e++)Et.push(new vt(t[e]));window.addEventListener("resize",xt),window.addEventListener("orientationchange",xt),xt()}]);class Lt extends t.core.DisclosureButton{apply(t){super.apply(t),this.hasAttribute&&this.element.setAttribute("tabindex",t?"0":"-1")}}const At=t.core.ns.selector("tabs"),St=t.core.ns("tabs"),Ct=t.core.ns("tabs__tab"),_t=t.core.ns("tabs__panel"),kt=t.core.ns("tabs__list");class qt extends t.core.DisclosuresGroup{constructor(e,s){super(e,s),this.list=s.querySelector(`.${kt}`),s.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),t.core.engine.renderer.add(this.render.bind(this))}static get selector(){return St}transitionend(t){this.element.style.transition="none"}init(){this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(Ct)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(Ct)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(Ct)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(Ct)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let t=0;t<this._index;t++)this.members[t].translate(-1);this.current.element.style.transition="",this.current.element.style.transform="";for(let t=this._index+1;t<this.length;t++)this.members[t].translate(1);this.element.style.transition=""}add(t){if(super.add(t),1===this.length||t.disclosed)this.current=t;else{const e=this.members.indexOf(t);this._index>-1&&this._index!==e&&t.translate(e<this._index?-1:1,!0)}}render(){if(null===this.current)return;const t=Math.round(this.current.element.offsetHeight);this.panelHeight!==t&&(this.panelHeight=t,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class It extends t.core.Disclosure{static get type(){return t.core.DISCLOSURE_TYPES.select}static get selector(){return _t}get GroupConstructor(){return qt}buttonFactory(t){return new Lt(t,this)}translate(t,e){this.element.style.transition=e?"none":"",this.element.style.transform=`translate(${100*t}%)`}reset(){this.group.index=0}}t.Tab=It,t.TabButton=Lt,t.TabsGroup=qt;new t.core.Initializer(At,[()=>{It.build(document)}]);const zt=t.core.ns.selector("header"),Dt=t.core.ns.selector("header__search"),Ht=t.core.ns.selector("header__menu"),Pt=t.core.ns.selector("header__tools-links"),Ot=t.core.ns.selector("header__menu-links"),Tt=`${Pt} ${t.core.ns.selector("links-group")}`;class Bt{constructor(t){this.header=t||document.querySelector(zt),this.modals=[],this.init()}getModal(e){const s=this.header.querySelector(e);if(!s)return;const i=t.core.Instance.getInstances(s,t.Modal);i&&i.length&&this.modals.push(new Nt(i[0]))}init(){this.getModal(Dt),this.getModal(Ht),this.linksGroup=this.header.querySelector(Tt),this.toolsLinks=this.header.querySelector(Pt),this.menuLinks=this.header.querySelector(Ot),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge?this.modals.forEach((t=>t.disable())):this.modals.forEach((t=>t.enable())),null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}class Nt{constructor(t){this.modal=t}enable(){this.modal.element.setAttribute("role","dialog"),this.modal.element.setAttribute("aria-labelledby",this.modal.primary.element.id)}disable(){this.modal.conceal(),this.modal.element.removeAttribute("role"),this.modal.element.removeAttribute("aria-labelledby")}}t.Header=Bt;new t.core.Initializer(zt,[()=>{const t=Array.prototype.slice.call(document.querySelectorAll(zt)),e=[];for(const s of t)e.push(new Bt(s))}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class r{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(t){this.closures.push(t);return()=>{const e=this.closures.indexOf(t);-1!==e&&this.closures.splice(e,1)}}next(t,e){e=void 0===e?0:e-1,void 0===this.nexts[e]&&(this.nexts[e]=[]),this.nexts[e].push(t)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const t=this.nexts.shift();if(t)for(const e of t)e.call()}}const o=new class{constructor(){this.renderer=new r}register(t,e){}start(){}stop(){}};class h{constructor(t,e){this.selector=t,this.builders=e,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let t=0;t<this.builders.length;t++)this.instances.push(this.builders[t]())}}const l={},c={};let a=0;const d=t=>{for(const e in c)if(c[e]===t)return e;a++;const e=a;return c[e]=t,e};class u{constructor(t,e,s){const i=d(t);l[i]||(l[i]=[]),l[i].push(this),this.element=t,this.id=t.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=e,this.isRendering=s}dispatch(t,e){const s=new CustomEvent(t,e);this.element.dispatchEvent(s)}listen(t,e){this.listeners[t]||(this.listeners[t]=[]),this.listeners[t].indexOf(e)>-1||(this.listeners[t].push(e),this.element.addEventListener(t,e))}unlisten(t,e){if(t)if(e){if(!this.listeners[t])return;const s=this.listeners[t].indexOf(e);s>-1&&this.listeners[t].splice(s,1),this.element.removeEventListener(e)}else{if(!this.listeners[t])return;for(const e of this.listeners[t])this.element.removeEventListener(e);this.listeners[t].length=0}else for(const t in this.listeners)this.unlisten(t)}get isRendering(){return this._isRendering}set isRendering(t){this._isRendering!==t&&(this._isRendering=t)}render(){}get isResizing(){return this._isResizing}set isResizing(t){this._isResizing!==t&&(this._isResizing=t)}resize(){}destroy(){}static getInstances(t,e){const s=d(t);return l[s]?e?l[s].filter((t=>t instanceof e)):l[s]:null}}const m=e.attr("group"),p=[];class b{constructor(t,e){this.id=t,this.element=e,this.members=[],this._index=-1,this._current=null,p.push(this)}static getGroupById(t){for(const e of p)if(e.constructor===this&&e.id===t)return e;return new this(t)}static getGroupByElement(t){for(const e of p)if(e.element===t)return e;return new this(!1,t)}static groupById(t,e){const s=t.element.getAttribute(m);if(null===s)return;e.getGroupById(s).add(t)}static groupByParent(t,e,s){if(void 0===s&&(s=e.selector),""===s)return;let i=t.element.parentElement;for(;i;){if(i.classList.contains(t.constructor.selector))return;if(i.classList.contains(s)){return void e.getGroupByElement(i).add(t)}i=i.parentElement}}static get selector(){return""}add(t){if(-1===this.members.indexOf(t))switch(this.members.push(t),t.setGroup(this),!0){case null!==this.current:case!(t.disclosed||t.primary&&t.primary.disclosed):t.disclosed=!1;break;default:this._current=t,this._index=this.members.indexOf(t),t.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(t){t<-1||t>=this.length||this._index===t||(null!==this.current&&this.current.conceal(!0,!0),this._index=t,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(t){this.index=this.members.indexOf(t)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class g{constructor(t,e){this.element=t,this.disclosure=e,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(t){this.disclosure.change(this.hasAttribute)}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(t){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,t),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const f=e.event("DISCLOSE"),y=e.event("CONCEAL"),w=[];class v extends u{constructor(t){super(t),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:e.attr(this.type.id),this.pristine=!0;const s=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:e.attr.selector("controls",this.id));if(s.length>0)for(let t=0;t<s.length;t++)this.addButton(s[t]);this.disclosed=this.primary&&this.primary.disclosed,this.gather()}gather(){this.group||(b.groupById(this,this.GroupConstructor),b.groupByParent(this,this.GroupConstructor))}static build(t){const e=Array.prototype.slice.call(t.querySelectorAll(`.${this.selector}`));for(const t of e)w.push(new this(t))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(t){const e=this.buttonFactory(t);e.hasAttribute&&(void 0===this.primary?this.primary=e:e.apply(this.primary.disclosed)),this.buttons.push(e)}get GroupConstructor(){return b}buttonFactory(t){return new g(t,this)}disclose(t){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,t||void 0===this.group||(this.group.current=this),!0)}conceal(t,e){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,e||this.focus(),t||void 0===this.group||(this.group.current=null);for(const t of w)t!==this&&this.element.contains(t.element)&&t.reset();return!0}get disclosed(){return this._disclosed}set disclosed(t){if(this._disclosed!==t){this.dispatch(t?f:y,this.type),this._disclosed=t,t?i(this.element,this.modifier):n(this.element,this.modifier);for(let e=0;e<this.buttons.length;e++)this.buttons[e].apply(t)}}reset(){}change(t){if(this.constructor.type.canConceal)switch(!0){case!t:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(t){this.group=t}get buttonHasFocus(){return!!this.buttons.some((t=>t.hasFocus))}get hasFocus(){return this.element===document.activeElement||(this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus)}focus(){for(let t=0;t<this.buttons.length;t++){const e=this.buttons[t];if(e.hasAttribute)return void e.element.focus()}}}v.DISCLOSE_EVENT=f,v.CONCEAL_EVENT=y;const E={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class x{constructor(t){this.element=t,this.collections={}}_add(t,e){void 0===this.collections[t]&&(this.collections[t]=new L(t,this.element)),this.collections[t].add(e)}down(t,e,s,i){this._add("down",new A(t,e,s,i))}up(t,e,s,i){this._add("up",new A(t,e,s,i))}dispose(){for(const t of this.collections)t.dispose();this.types=null}}class L{constructor(t,e){this.type=t,this.element=e,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+t,this.binding)}add(t){this.actions.push(t)}handle(t){for(const e of this.actions)e.handle(t)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class A{constructor(t,e,s,i){this.key=t,this.closure=e,this.preventDefault=!0===s,this.stopPropagation=!0===i}handle(t){t.keyCode===this.key&&(this.closure(t),this.preventDefault&&t.preventDefault(),this.stopPropagation&&t.stopPropagation())}}x.TAB=9,x.ESCAPE=27,x.END=35,x.HOME=36,x.LEFT=37,x.UP=38,x.RIGHT=39,x.DOWN=40;const S=e("collapse"),C=[],_={};class k extends v{constructor(t){super(t),C.push(this),this.requesting=this.request.bind(this),t.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const t in _){let e=this.element.parentElement;for(;e;){if(e.classList.contains(t))return void("string"==typeof _[t]?b.groupByParent(this,b,_[t]):b.groupByParent(this,_[t]));e=e.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return E.expand}static get selector(){return S}static register(t,e){_[t]=e;for(const t of C)t.gatherByAscendants()}transitionend(t){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(t){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(t)},window.requestAnimationFrame(this.requesting))}conceal(t,e){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(t,e)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const t=this.element.offsetHeight;this.element.style.setProperty("--collapse",-t+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}t.core.ns=e,t.core.addClass=i,t.core.removeClass=n,t.core.engine=o,t.core.Instance=u,t.core.Initializer=h,t.core.Disclosure=v,t.core.DisclosureButton=g,t.core.DisclosuresGroup=b,t.core.DISCLOSURE_TYPES=E,t.KeyListener=x,t.Collapse=k,t.Equisized=class{constructor(t,e){this.selector=t,this.group=e,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let t=0;t<this.elements.length;t++){const e=this._getWidth(this.elements[t]);e>this.maxWidth&&(this.maxWidth=e)}this.apply()}apply(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width=this.maxWidth+1+"px"}reset(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width="auto";this.maxWidth=0}_getWidth(t){let e=t.offsetWidth;const s=getComputedStyle(t);return e+=parseInt(s.marginLeft)+parseInt(s.marginRight),e}};new h(`.${S}`,[()=>{k.build(document)}]);const q=t.core.ns("accordions-group"),I=t.core.ns("accordion");class z extends t.core.DisclosuresGroup{static get selector(){return q}}t.AccordionsGroup=z,t.Collapse.register(I,z);const D=`${t.core.ns.selector("breadcrumb")} ${t.core.ns.selector("collapse")}`;class H extends t.core.Instance{constructor(e){super(e),this.collapse=t.core.Instance.getInstances(e,t.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(t.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),t.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new t.core.Initializer(D,[()=>{const t=[],e=document.querySelectorAll(D);for(let s=0;s<e.length;s++)t.push(new H(e[s]))}]);const P=t.core.ns.selector("btn"),O=t.core.ns.selector("btns-group"),T=t.core.ns.selector("btns-group--equisized");new t.core.Initializer(O,[()=>{const e=document.querySelectorAll(T),s=[];for(let i=0;i<e.length;i++)s.push(new t.Equisized(P,e[i]))}]);const B=t.core.ns.selector("modal"),N=t.core.ns("modal"),G=t.core.ns("no-scroll"),R=t.core.ns("scroll-shadow"),$=t.core.ns.selector("modal__body"),F=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),M=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),W=(t,e)=>{if("hidden"===window.getComputedStyle(t).visibility)return!1;for(void 0===e&&(e=t);e.contains(t);){if("none"===window.getComputedStyle(t).display)return!1;t=t.parentElement}return!0};class K{constructor(t,e){this.element=null,this.activeElement=null,this.onTrap=t,this.onUntrap=e,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(t){this.trapped&&this.untrap(),this.element=t,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){W(this.element)?this.trapping():t.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const t=this.focusables;t.length&&t[0].focus(),this.element.setAttribute("aria-modal",!0),window.addEventListener("keydown",this.handling),this.stunneds=[]}stun(t){for(const e of t.children)e!==this.element&&(e.contains(this.element)?this.stun(e):this.stunneds.push(new V(e)))}handle(t){if(9!==t.keyCode)return;const e=this.focusables;if(0===e.length)return;const s=e[0],i=e[e.length-1],n=e.indexOf(document.activeElement);t.shiftKey?!this.element.contains(document.activeElement)||n<1?(t.preventDefault(),i.focus()):(document.activeElement.tabIndex>0||e[n-1].tabIndex>0)&&(t.preventDefault(),e[n-1].focus()):this.element.contains(document.activeElement)&&n!==e.length-1&&-1!==n?document.activeElement.tabIndex>0&&(t.preventDefault(),e[n+1].focus()):(t.preventDefault(),s.focus())}get focusables(){let t=[...this.element.querySelectorAll(F)];const e=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(e.length){const s={};for(const t of e){const e=t.getAttribute("name");void 0===s[e]&&(s[e]=new U(e)),s[e].push(t)}t=t.filter((t=>{if("input"!==t.tagName.toLowerCase()||"radio"!==t.getAttribute("type").toLowerCase())return!0;const e=t.getAttribute("name");return s[e].keep(t)}))}const s=[...this.element.querySelectorAll(M)];s.sort(((t,e)=>t.tabIndex-e.tabIndex));const i=t.filter((t=>-1===s.indexOf(t)));return s.concat(i).filter((t=>"-1"!==t.tabIndex&&W(t,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),window.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class V{constructor(t){this.element=t,this.hidden=t.getAttribute("aria-hidden"),this.inert=t.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class U{constructor(t){this.name=t,this.buttons=[]}push(t){this.buttons.push(t),(t===document.activeElement||t.checked||void 0===this.selected)&&(this.selected=t)}keep(t){return this.selected===t}}class j extends t.core.DisclosuresGroup{constructor(){super(),this.trap=new K}apply(t,e){super.apply(t,e),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const Y=new j;class J extends t.core.Disclosure{constructor(t){super(t),this.body=this.element.querySelector($),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(t){this.body&&this.body!==t.target&&!this.body.contains(t.target)&&this.conceal()}gather(){Y.add(this)}disclose(t){return!!super.disclose(t)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(t,e){return!!super.conceal(t,e)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(t.core.removeClass(document.documentElement,G),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(G)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",t.core.addClass(document.documentElement,G))}resize(e,s){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?t.core.removeClass(this.body,R):t.core.addClass(this.body,R):t.core.removeClass(this.body,R),this.isMedium=window.matchMedia("(min-width: 48em)").matches,e&&(this.isMedium?this.body.style.removeProperty("max-height"):(this.body.style.maxHeight=window.innerHeight-32+"px",t.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"})))))}static get type(){return t.core.DISCLOSURE_TYPES.opened}static get selector(){return N}get GroupConstructor(){return j}}t.Modal=J,t.ModalsGroup=j,t.FocusTrap=K;new t.core.Initializer(B,[()=>{J.build(document)}]);const Q=t.core.ns("nav"),X=t.core.ns("nav__list"),Z=t.core.ns("nav__item"),tt=t.core.ns("nav__item--align-right"),et=t.core.ns("menu");class st extends t.core.DisclosuresGroup{constructor(t,e){super(t,e),this.menus=[],this.navList=e.querySelector(`.${X}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return Q}add(t){super.add(t),t.element.classList.contains(et)&&this.menus.push(new it(t,this.navList.getBoundingClientRect().right))}focusOut(t){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(t){-1===t&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=t}resize(){const t=this.navList.getBoundingClientRect().right;for(const e of this.menus)e.place(t)}}class it{constructor(t,e){this.initialize(t),this.place(e)}initialize(t){this.element=t.element;for(const e of t.buttons)if(e.hasAttribute){this.button=e.element;break}let e=this.element.parentElement;for(;e;){if(e.classList.contains(Z)){this.item=e;break}e=e.parentElement}}place(e){const s=getComputedStyle(this.element),i=parseFloat(s.width);this.button.getBoundingClientRect().left+i>e?t.core.addClass(this.item,tt):t.core.removeClass(this.item,tt)}}t.Navigation=st,t.Collapse.register(Q,st);const nt=t.core.ns.attr("theme"),rt=t.core.ns.attr("transition");class ot{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const t=this.root.getAttribute(nt);"dark"===t||"light"===t?this.scheme=t:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(rt)?(this.root.removeAttribute(rt),this.root.setAttribute(nt,"dark"),setTimeout((()=>{this.root.setAttribute(rt,"")}),300)):this.root.setAttribute(nt,"dark"):this.root.setAttribute(nt,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(t){t.forEach((t=>{if("attributes"===t.type&&t.attributeName===nt){const t=this.root.getAttribute(nt);"dark"===t?localStorage.setItem("scheme","dark"):"light"===t&&localStorage.setItem("scheme","light")}}))}}t.Scheme=ot;const ht=`input[name="${t.core.ns.selector("radios-theme","")}"]`,lt=t.core.ns.selector("switch-theme","#"),ct=t.core.ns.attr("theme");class at{constructor(){this.attributeName=ct,this.theme=null,this.radios=document.querySelectorAll(ht);for(var t=0;t<this.radios.length;t++)this.radios[t].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.attributeName&&this.apply()}))}apply(){const t=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var e=0;e<this.radios.length;e++)this.radios[e].checked=this.radios[e].value===t;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(ht+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new t.core.Initializer(`:root[${nt}]`,[()=>{new ot}]),new t.core.Initializer(`${lt}`,[()=>{new at}]);const dt=t.core.ns("sidemenu"),ut=t.core.ns("sidemenu__list");t.Collapse.register(dt,ut);const mt=t.core.ns.selector("table"),pt=`${t.core.ns.selector("table")}:not(${t.core.ns.selector("table--no-scroll")})`,bt=t.core.ns("table--shadow"),gt=t.core.ns("table--shadow-left"),ft=t.core.ns("table--shadow-right"),yt=t.core.ns("table__wrapper"),wt=t.core.ns("table--caption-bottom");class vt{constructor(t){this.init(t)}init(t){this.table=t,this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0,this.wrap();const e=this.change.bind(this);this.tableElem.addEventListener("scroll",e),this.change()}change(){const t=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let e=this.tableElem.offsetWidth>this.table.offsetWidth;t||e?(this.scroll(),this.handleCaption()):t!==this.isScrollable&&this.delete(),this.isScrollable=t,e=!1}delete(){t.core.removeClass(this.table,ft),t.core.removeClass(this.table,gt),t.core.removeClass(this.table,bt),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){t.core.addClass(this.table,bt),this.setShadowPosition()}wrap(){const t=document.createElement("div");t.className=yt,this.table.insertBefore(t,this.tableElem),t.appendChild(this.tableElem),this.tableInnerWrapper=t}setShadowPosition(){const t=this.getScrollPosition("left"),e=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",t),this.setShadowVisibility("left",e)):(this.setShadowVisibility("left",t),this.setShadowVisibility("right",e))}getScrollPosition(t){let e=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(e=-1),t){case"left":return this.tableElem.scrollLeft*e;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*e;default:return!1}}handleCaption(){if(this.caption){const t=getComputedStyle(this.caption),e=this.caption.offsetHeight+parseInt(t.marginTop)+parseInt(t.marginBottom);this.captionHeight=e,this.table.classList.contains(wt)?(this.tableElem.style.marginBottom=this.captionHeight+"px",this.caption.style.bottom=-this.captionHeight+"px"):(this.tableElem.style.marginTop=this.captionHeight+"px",this.caption.style.top=-this.captionHeight+"px")}}setShadowVisibility(e,s){s<=1?"left"===e?t.core.removeClass(this.table,gt):"right"===e&&t.core.removeClass(this.table,ft):"left"===e?t.core.addClass(this.table,gt):"right"===e&&t.core.addClass(this.table,ft)}}t.Table=vt;const Et=[],xt=()=>{for(let t=0;t<Et.length;t++)Et[t].change()};new t.core.Initializer(mt,[()=>{const t=document.querySelectorAll(pt);for(let e=0;e<t.length;e++)Et.push(new vt(t[e]));window.addEventListener("resize",xt),window.addEventListener("orientationchange",xt),xt()}]);class Lt extends t.core.DisclosureButton{apply(t){super.apply(t),this.hasAttribute&&this.element.setAttribute("tabindex",t?"0":"-1")}}const At=t.core.ns.selector("tabs"),St=t.core.ns("tabs"),Ct=t.core.ns("tabs__tab"),_t=t.core.ns("tabs__panel"),kt=t.core.ns("tabs__list");class qt extends t.core.DisclosuresGroup{constructor(e,s){super(e,s),this.list=s.querySelector(`.${kt}`),s.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),t.core.engine.renderer.add(this.render.bind(this))}static get selector(){return St}transitionend(t){this.element.style.transition="none"}init(){this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(Ct)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(Ct)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(Ct)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(Ct)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let t=0;t<this._index;t++)this.members[t].translate(-1);this.current.element.style.transition="",this.current.element.style.transform="";for(let t=this._index+1;t<this.length;t++)this.members[t].translate(1);this.element.style.transition=""}add(t){if(super.add(t),1===this.length||t.disclosed)this.current=t;else{const e=this.members.indexOf(t);this._index>-1&&this._index!==e&&t.translate(e<this._index?-1:1,!0)}}render(){if(null===this.current)return;const t=Math.round(this.current.element.offsetHeight);this.panelHeight!==t&&(this.panelHeight=t,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class It extends t.core.Disclosure{static get type(){return t.core.DISCLOSURE_TYPES.select}static get selector(){return _t}get GroupConstructor(){return qt}buttonFactory(t){return new Lt(t,this)}translate(t,e){this.element.style.transition=e?"none":"",this.element.style.transform=`translate(${100*t}%)`}reset(){this.group.index=0}}t.Tab=It,t.TabButton=Lt,t.TabsGroup=qt;new t.core.Initializer(At,[()=>{It.build(document)}]);const zt=t.core.ns.selector("header"),Dt=t.core.ns.selector("header__search"),Ht=t.core.ns.selector("header__menu"),Pt=t.core.ns.selector("header__tools-links"),Ot=t.core.ns.selector("header__menu-links"),Tt=`${Pt} ${t.core.ns.selector("links-group")}`;class Bt{constructor(t){this.header=t||document.querySelector(zt),this.modals=[],this.init()}getModal(e){const s=this.header.querySelector(e);if(!s)return;const i=t.core.Instance.getInstances(s,t.Modal);i&&i.length&&this.modals.push(new Nt(i[0]))}init(){this.getModal(Dt),this.getModal(Ht),this.linksGroup=this.header.querySelector(Tt),this.toolsLinks=this.header.querySelector(Pt),this.menuLinks=this.header.querySelector(Ot),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge?this.modals.forEach((t=>t.disable())):this.modals.forEach((t=>t.enable())),null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}class Nt{constructor(t){this.modal=t}enable(){this.modal.element.setAttribute("role","dialog"),this.modal.element.setAttribute("aria-labelledby",this.modal.primary.element.id)}disable(){this.modal.conceal(),this.modal.element.removeAttribute("role"),this.modal.element.removeAttribute("aria-labelledby")}}t.Header=Bt;new t.core.Initializer(zt,[()=>{const t=Array.prototype.slice.call(document.querySelectorAll(zt)),e=[];for(const s of t)e.push(new Bt(s))}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  
  
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
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.dde91426db6e.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.dde91426db6e.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js)
  
  
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
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `ogdl2tmzm08UOMK7LKltNeHjl94jwzC11zMtTZEpN8YBeBfx0hP1HjFqaQxGLyOc`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `9FQgwgESdWc9AZoHqQ3avxbY6v5bywJFxpICdqla8PLFNWfhuvulr1NairbaohdJ`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/loi-sur-leau/](https://envergo.beta.gouv.fr/loi-sur-leau/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/codes/article_lc/LEGIARTI000042075042/2020-09-01/`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/](https://envergo.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `ogdl2tmzm08UOMK7LKltNeHjl94jwzC11zMtTZEpN8YBeBfx0hP1HjFqaQxGLyOc`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr](https://envergo.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `ogdl2tmzm08UOMK7LKltNeHjl94jwzC11zMtTZEpN8YBeBfx0hP1HjFqaQxGLyOc`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>wOFF\x0000\x0001\x0000\x0000\x0000\x0000\x0019�\x0000\x000b\x0000\x0000\x0000\x00006\x0010\x0000\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000GSUB\x0000\x0000\x0001\x0008\x0000\x0000\x0000[\x0000\x0000\x0000�#M(;OS/2\x0000\x0000\x0001d\x0000\x0000\x0000B\x0000\x0000\x0000VY\x000eCcmap\x0000\x0000\x0001�\x0000\x0000\x0002\x0016\x0000\x0000\x0006r\x001e`K�glyf\x0000\x0000\x0003�\x0000\x0000\x0011:\x0000\x0000#����	head\x0000\x0000\x0014�\x0000\x0000\x00001\x0000\x0000\x00006\x001d�\x000c?hhea\x0000\x0000\x00150\x0000\x0000\x0000\x001e\x0000\x0000\x0000$\x0008�\x0004Bhmtx\x0000\x0000\x0015P\x0000\x0000\x0000\x0016\x0000\x0000\x0001dv�\x0000\x0000loca\x0000\x0000\x0015h\x0000\x0000\x0000�\x0000\x0000\x0000����</p><p>maxp\x0000\x0000\x0016\x0018\x0000\x0000\x0000\x001d\x0000\x0000\x0000 \x0001m\x0000`name\x0000\x0000\x00168\x0000\x0000\x00011\x0000\x0000\x0002.D\x001dI�post\x0000\x0000\x0017l\x0000\x0000\x0002c\x0000\x0000\x0005)���x�c`d``�b0`�c`rq�	a��I,�c�b`a�\x0000�<2�1'3=��\x0003�\x0003ʱ�i\x000e 6b`\x0002�%\x0001\x00165\x0003� �`�\x00100�\x0005(\x001e�\x0010�\x0010\x000e$#�4#P} C(\x0000�5</p><p>�\x0000x�c`d1c��������ك��a\x0005�fr`�b4\x0005�\x000c��\x000cXA@�k</p><p>�\x0003��\x0003�\x0017�-\x0018r�_0�\x0000</p><p>3��\x0000�N\x000c\x001f\x0000\x0000x���ISSa\x0014���B@DP�\x0011�Y��A\x0011\x0004\x0014�yd\x0012dOQŊ\x0005U���'�'�*�΍�zR�\x000b	9�N7�\x0003t�ckA�2��Y�i�>樂}�j���<C>i�uv�e�}\x000e8��ё_�<�}�y5���\x001fXc�-��7\x001bl�����O=�r�>N�{�b�ANs���,Ü�;/p�K\f�+\e�k\�\x00067��m�p�{�1�}\x001e�G��	O�`�)�y�sfx�,s�d�\x0005\x0016y�k�x�[�y�{>�O|�\x000b_��w���\x0015V=F�_f��k�\x001e6;O���Եa����?�@=�&��_���XM�\x001e5�Nl�n�k{Q#�G
z\x0010�����ű�N�7\x0005Em��6ZQ���F��n��𾡨\x0004(��(jz��\x0012�7\x0014�w\x0015��\x0016��\x0017�7\x0019�w\x001aE�B�=G�G��G�\x0014�p\x001eP8\x0019(�\x0011\x0014N\x000b</p><p>�\x0006�\x0013��YB�T�p�P8i(�9\x0014N\x001f</p><p>�\x0010�\x0013���Dᔢp^Q8�(�a\x0014�Z</p><p>�\x001a�\x0013��YG�ԣp�Q�	P�\x0013P�\x001dP�'P�1P�;P�EP�OP�YP�cP�mP�wP��P��P��P��P��P��P��P��P��P��P��P��P��P�\x0003Q�
QT�\x0015nH\x0014�J\x0014��\x0001�=�W\x0000\x0000x��Y
pSו~�=�ɿ\x0012Bzz\x0018[B?Hώ����d3�O&\x0018\x000c���\x0018\x0007�\x0017\x0007B��\x0006H	$l�6e	f����lh�śM��а��i\x0019gf�N�t3�0[&��v���L6�I���˞sߓ,\x001991��\x0018=]]�{��9�9��\x0018拋�~n��1.��aH@���\x0015F�Ȼ$��_\x0011�D#\x001cL\x0005`�H<|4\x0010#!\x0018���Iء�G�l���p����h�u˶k�\x0006�u���/}R�[S�;�\x000fn,\x0019Y����\x001dM�-M�ۺ����`���0\x001b�~�)�d%re�����f"F)��E�Vj$��\x0008\x0013<,�y\x001aI(F\x0002Nb3\x0011)\x0010	�=�͞#�&\x0008\x0015�����2�\x0017\x001c��-��W߼��^^�Y�W������k���I�"Ñ��c��Զ�\x000f��+��P
�j�Y��Xp\x001d�\x0011�۰���\x001eT�
����++��\x001dާl��N\x0005\x001e</p><p>�\x0019lg\x0018f�<�@�0�G8(\x0004\x0005��
{��B�Kx0�\x0010~���6���+ɤ�L\x0015����{v�����=�2\x00032���J�V!M���t\x0000b1(�5�S��!���-�-^�;\x000c�I�:��3d:3�W�^�\x0019F�C��\x0011�J�)!v8\x000e�\x001b\x000f'J�x�\x0010\x000c�\x001d#\x001f�&�b��bU��|h\x0014�V
)��
�����n2٫˸�2�)}HQ�H*��\x0018r�ۘULu!\x000e�M8��\x0005^���;�r��R���\x0007�T�w</p><p>�Net�7��\x00143���%$</p><p>\x0016`ϑ�zR=\x0019'��Oq|�����ٽ�\ۓ`7�g�(�a��zշ�i��\x0013W�I,�]�1' m\x0002F%�\x0012"������)}�I�\x0015u6N��x�a��\x0013�u�p	�\x0004��h\x0014��L*,\x001f��\x0003����\x0018{*~gN&1\��ʾ\x000f�����-�H\x0012�fJVo�nY���Sd2%�n\x0018�g�����(��Q]�n֩�@&�Ȥ���ź\x0000�\x0012"\x0011w��Uge2�v�H�\x000cN�`��lc\x000b��g�:"�\J:���Xa}��}G�GBN>�$@�An֯\x000f���&�R�{FN��\x000f�Ǿ���i�gNV�a��\x0007e���2��K\x001d��+�8x>�R�\x0006c\x0008��3��\x0004O���������/������\x001cr�G��\x001cF�xH7'yG\x0017H�\x0017|}3w
,T�0V��ƃ���$\x0018�;@�P�\x001da�\x001d\x000e*��\x000ea���`?M</p><p>��U\x000e!	�	n��\x0004�C�\x0006\x001dB*%8��u�y\x000f��\x001a#2^F\x0002\x0019���!nY�jt#\x001c�\x0008`It[��`\x0012�!\x001f�\x0001D���\	%5�s!��۔��2K*\x0014��Ú�\x0006��	���,����\x0014\x0002�3�x��i`��/�Θ\x000fV/�	88\x0012�X\x0010���쏫���\x0017�jRO���o.�u\x001bd��2MKp*��Q)*B$\x0014b_\x0000s�g�\x0013���@\x0005\x001079\x0013�@��<;�����\x0011\x0013\x0015A ��8\x0013����\x0002��9+��\x001a�\x0016r�=��\x001aE0��\x0012\x001ag��y��<qA��	���|a�\x0006"7/�\x0017`\x000bl��z,�%�t\x0019�۬\x0014������#\x000e�usN��\x0011|�������29�`�ȸ�7\x001c\x000c�\x0011���\x001bL)\x000e!�\x0003ޜ"��aL\x0019\x0000P+���O��/���$��ܔKׁY�-�\x0013\x0017-nKQ�����,�$;��h�\x0000\x0007%�G������d0a5���r��B�(�d�\x000476</p><p>��YV��]}�I	(�,i��]䲬��6j�/��o2��	"�\x001b&��\x001aȠF��\x001e�a;̵�\x000bf��o�����\x00130�~Ha�u\x000b�70fƊ�,\x0011A\Df=�c\-:��k�YbI�5�H�d\x0002����,͌�ӌ^�۱l�#)\x001c���\x000b��\x0008�\x000e�X�d�'\x0013�
L�=E=-(,�eǽ��H\x0005�:��s�0���\x000e2+\x0011󉀵V0\x0007��>p"�9<fS���{�k\x0010��O���G�uHK)u���9�\x0001��\x0011�FY���S�����N�ID,�]XO�H4b�\x0016���&0ک
�+��`�ؑ\x0017E��#��;�����=\x000fv�\x0017��]\x000f������#\x001d\x001d���G�������\x001b�h{���w�:2��\x001b�\x0007�=������3�Vx(�Vx�>�\x0019�k��`��\x000f4�\x0000��
�BR\x0014�,6\x000eN6\x0012�L�\x0011�D�w��"	Z</p><p>�(E���\x001b	�\x0019�g������+W�\1��{�����^�x��\x000f��֏��]V��%�9��C��\x0005���/��{��>��I�}����`���n\x0014����]\x0017;/��=�W؝MOm8��β�hu�������\�n\x000c�MG�};w'FVU\x000e4�x��'�9H~�zz\x001el�5�\x0017�����\x0007z\x0006�
ω�\x0013�\x0001D���y\x0007	\x001a�\x0016<�0�X�?�Eo<u���.�}k�ꄕ�ُ=u#�\x000e�Pk�Ξ|��y+\x0019�|b�hQ��U6�Ȥz�z��c'���/�h�\x0002\x0019* b�\x0002�uCB��(�Jer>���d�\x001bK!��C�	\x000e�<	�rqc��\x0001�г�F)\x0018\x000eF���x}@�
�\x001a}�\x001c\x0010J\x0000���ד�����R�</p><p>;�!�Hq�6�\x0008\x000e�d3�\x001d\x0002��kc��\x0002�J�H��Ζ5\x0012\x0008\x001d\x0015\x0012�\x001e(��\x001a涽�\x000c�\x0003b�k\x0015��$��i���{\x000c�\x0006��\x0012wNyD#�\x0002�X�F\x0007(�����P�\x0010�b*}\x000b��,���6\x0014�5wYQ\x000b�:b�B
f��H�A'i\x000b\x001a��\x0000
h��g�t\x000f�(!/�cGiȞU	d\x001f\x0011"\x0000��\x0012�B\x0015�\x0013�a�5�غ���I��)�D��5A�(\x0007�"�I�D�s�虜ϭ\x001b�\x0004�\x0001=%l��	�Y?bw�֭����\x001e�ۊ���\x0017~C��h��ɸ\x0019|���ddf;�W@XN�\x000b�\x001emF\x0013\x0007^�{$��ȁ[�C�P4�E#���a��\x0012>��"\x0010)��P�^vh�Z�}��f�c	a9i�\��O\x0017�����
O��\x0007!��\x000f��o�^��Қ����L�t:�DB�]9w8ZN������d�i]A�!\x0014v�A8� �s\x0012|\x001e(��n�/���Cpك4b�I[��sE�\x0015�&�i���</p><p>�چn��T���������{�\x000c\x001bM3U�T�~Q-I������6[=�\x0003\x001f�+펕��U-5��ݸ\]E��m��y�����*&&1V\x001c���\x0015�B�B��ư��\x001cD�\x0012�Z \x0013�\x000e!��80�����f�\x001a\x0007z�Y�����\x0005�	<��ᢇ\x0002\x0001z\x001c=\x0001
\x0010
92��jM_%E\x0011�\x001b\x0005/�J��$X.b�J�HK</p><p>DKJ\x0005�;#�^{�Cm`�14O�\x0012���\x0012\x0008>:Б[���\x001b�����O�BV��?&}�z��\x0019|�\x000cQ+�M���X�%l.Y�\x0011���\x0018�O�\x0013�h>�\x0019�{DI�\x0010T�!٬a\x000f\x0018s5�-�\x0018�\x0007�B����\x00051;�~
ߡ�N�߲�d_�{�Q�fچ��^\x0012��!��"��T�rz_�\����ƲAίI��Z
�=K���F�h�" eA��-\x0015xCY�lIIa��Ɨ��o�,�O�\x0002�,�O��	�E��Lx�o�碑e��5 �lii\x0011��.�R=SF�h���\x0012��R
������\x00085\x0010�h�8\x001f�^�\x001e�\x0004\x0007A�qgny�O��<��Q2�\x001fc"\x0011���\�\x0000'Mi\x0001�\x0005;�Ů�!$\x0012\x00024�EY�^�0�</p><p>�	\x0010z\x0001e(_G\x0006ꈠ�g'��\x0006��*����\x0017�P}\x0002Y%4���\x0002�(�Z[���H\x0004�Izw�ԖQ=�\x0014�\x0002�\x0010*�D�x"\x0001���z�y�~����F\x000e�z1F�P�{=X\x000e/Q`�tV�5�=�)T�����o�s�\x0015�R=�`yۖ\x001d=��w}���)n�q\x0008�</p><p>� ���Q�K��\x0018i$<���D\x0005�*q\x0008�:����hqh�\x0003}Me�\x001d���4��6	����b��V�~-WۻcKk9����2�%4���Q�NI�Z%��
\x0007��rrт:\x001c�E��^x�����G;\x0012--m�6�O\x0016\x0014��^�\x0018���,���K}{h5}�g3}�y�.�\x0005z\x0006\x000c�x���\x000e�q�P#\x0007}\x001c�\x0000�6\x0004�[�6'\x0017�\x0012�ȉc�N��������\x0013\x001dO|�{/���#'�\x001f��?�՚�}�I�l[U�c��\x001d;���\x000f\x0013���Gbl���`u���*̞\x001aU����]�5�ӯ�\x000f�Y:\x001b�"
&�7\x001dK��h�8�\x0012�z��Ғ����\x0004��U�����\x0007Ԡhv[8wn�@�\x0010 A�H�\x001f�$i~$fR\x001f@�f�&�=�+�_\x000c�\x0010#����r�0\x000c�</p><p>h�F	#\x0006O8�̰�ܙ������O\x001f\x001c����\x0018=8���e�m\x000ef?��������h6}	Uc��\x0017E\x0003�$Q`\x0016��q\x0017��4\x0007��\x000c-VzN�\��M�\x0004�<)�����4t}�y�N�\x001a�F�b~�\x0016-�\x0003-*L����t\x001c����X��k�\x0010"#�:��D|YA'�/�\�\x0010�-��\x0010�X�\x0007-P�#�B3���A�
ã\x0008^��\x0007��\x0004@6��&������ȗ2\x0003�?�>�\x001b�\x0015\x001clݔ~\x0007w\x000c�^\x001cA�\x0006�Ry��@��`\x000f\x0018\x0019�u��3�\x0003\+V
\x0004M\x001e��{�\x0008��\x000b����\x0000
��K��\x0007�A�'\x0012\x000e�#�\x001d�]��X�y♶\x0015�����@]������Y8�a��l�z�c�\x0006����w+�m\x001dk}����\x001b�������\x000cW�J�egGiyI�V\x0012j(ml�\x0004v�8t��rsC&n/r\x001fs��o���� d������,j��\x0007{5�{�63P���8����\x000e2xF��L=d�<��\x0005o,�=�~kA\x0014%k{R�P�\x000b?\x001a�ȗ=�m�$U\x0016~\x001f�l�_�\x0017D\x0001\x0001|�Yڇ)\x000eҳ��%_���䗢0\x0005��\x0018�Ӥ�7U\x0014\x0017W�xu�|\x0016��\x0006��ں\x001d�I��\x0010\x001c�2�|y��G��<k����z{SxwU_�龞�6�^\x001a�"�p�/2B�,J˒�=���~��{_.\x0008{���s�r���p�����\x001d\x001aH�7��H�w�fo^�_�*��|�j��\x0015��o�?���\x0015�\x00065_n�|��K\x0018 O��-�/�&�i�\x000fB��\x0004�"�(d��x���-����&5�\x0015N��x�\x001b{\x001f~�;���\x0013O\x001d:���3����ϴݛ�,�wI\x001b.!����</p><p>��oɐ\x0003\P_B�C ��\x0010z�m�o^D\x0004ZBH�0�H�b�F��\x000fPm�\x0006b\x0008��\x0006�01�%����;�ߺ'�߿6Tb�\x0002��$��SR_�3\x0014�\x000c�k|�R����4�[�dk\x0013L�Iy�j�\x000f~��/w~��\x0000\x0000x�c`d``\x0000��n\x001e�����Ͳ\x0001(�p���K\x0008��\x0005�:�m@.\x0007\x0003\x0013H\x0014\x0000�\x0014\x000f=\x0000\x0000\x0000x�c`d``~�߂��e\x0003\x0003\x0010��c`d@\x0005�\x0000`5\x0003�\x0000\x0000x�c````�0�1�\x000f�j	\x0001\x0000P\x000e7�\x0000\x0000x�c`\x0000\x0002\x001f�\x0013�2�&�)��\x0018�0�`|���I�I�Ƀ)���i\x001a�:�cL��٘\x001d�C�;�o�\x0008�䰴�lby��ª�����z������\x0006�\x0014�\x0003{\x0001�4�=�\x001f8�8�8�p�q�q��\x0012����j�Z�u�[�;��\x0010�?�0�%�B�i�kx/�1���U��}�w��" $\x0010!0E����`��\x0003t\x0008\x00003C0tx�c`d``�d\x0008a�b\x0000\x0001& �\x0002����\x000c\x0000\x001a�\x0001�\x0000\x0000\x0000x�m�=N�0\x0018���\x000f�J\x0008\x0004ba�\x0002\x000bj�3vdh�\x000e���IS%q�\x0015�\x0003'�\x0010\x001c��3p\x0008\x000e�[�I�Pm�~���\x0017+	�k|!�q\x0004���8Z�`��mҍp�� ��\x0000��=��p\x001fϘ	\x000fp\x000b�'\x0004�K�;�</p><p>�p�7�6��p��!��=>�{���}��#<�S�4�\x001d汩���vEdO�D+m��Tj\x0012�Or�+m#�\x0013�>�f�M�KUjM��r�(�����؅\x001b���h��\x000fcS"A�\x0014\x0016C�aP�^�}3�P �ɹ�9�b���Za����\r�d��\x0011\x001c���5\x000e\\x001b�y�ֱK�N��4���t�ihj����Cl|W��6�L��C{�\x000b�5d,\x0000\x0000\x0000x�mTW[�@\x0010��F1\x0001\x000c	�޻RH��\x001e�v�NX\x001f�;�$a���ەl\x0019Ѓ���ݽ�YK��\x0006?����2F�\x0003;�\x000b��\x0007�\x0018�8&��$�b</p><p>ӘA\x000b���>��<\x0016��\x00038�C8�#8�c8�\x00138�S8�38�s8�\x000b��K\x0008p\x0019Wp\x0015װ�븁���۸�����x��x��x��x��x��x��x��x����������������������e�m4E\x0018�B�A�(�'*�rJDQ\x0010&6T����\x001e�\x000b%-'��í5� 2=M|�Ƴz��1g��x��ٌ��!�+�J�VU���4+6Y�\x000c�d�ň���&}P���d�.\x0015]�&Y+�T�q�d�Б��ʀ�]aG��\x0004�\x0008��z嫏�"�{�2���
+\�\x0014\x000f'"�d΁\x0015�����\x0008^ܘ�\x0012�\x001b#�����\x0006=au�W�p��Q빴Z(�x�Q��w4=0q�\x0013�"�mcV뭷܏\x000c��l#Qw$Qw��B�(f_��v����T��t<$�����r�bE�\x000e����:�f�Eʸ�\x000c\x0010���D�F��M�.��R���uE�iGC</p><p>U�*��y�Ȱ�M���_��и�</p><p>���\x00190ʲ2�2�pVE�L���\x0011��3)l��\x0015�\x001b���[\x0011����L9�����jj�MQGd��QE�;c��B="-��@\x000b)\x0005����\x001a�	7L�\x0017m�u\x001f-	��}�Bt`\x001b��7\x001f�[\x0000</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.854345c899b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.dde91426db6e.js](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.dde91426db6e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: "const t=window.dsfr||{core:{}};window.dsfr=t;const e=t=>`fr-${t}`;e.selector=(t,s)=>(void 0===s&&(s="."),`${s}${e(t)}`),(e.attr=", see evidence field for the suspicious comment/snippet.</p>
  
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
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/contact/](https://envergo.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-breadcrumb__link" aria-current="page">Contact</a>`
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/](https://envergo.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-breadcrumb__link" aria-current="page">Mentions légales</a>`
  
  
  
  
Instances: 4
  
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
  
  
  
  
* URL: [https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css](https://envergo.beta.gouv.fr/static/@gouvfr/dsfr/dist/css/dsfr.66b0e7705517.css)
  
  
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

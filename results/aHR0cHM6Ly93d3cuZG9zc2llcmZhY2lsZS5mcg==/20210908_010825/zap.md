
# ZAP Scanning Report

Generated on Wed, 8 Sep 2021 00:50:57


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 6 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 7 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 12 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 5 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 5 | 
| Retrieved from Cache | Informational | 12 | 
| Storable and Cacheable Content | Informational | 2 | 
| Storable but Non-Cacheable Content | Informational | 4 | 
| Timestamp Disclosure - Unix | Informational | 82 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/](https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/](https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/](https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-2e16ccc7="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-2e16ccc7="" alt="logo monsieur hugo" src="/img/monsieur_hugo.ebb9d9a8.png" class="partner-logo monsieurhugo"></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-2e16ccc7="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-2e16ccc7="" alt="logo monsieur hugo" src="/img/monsieur_hugo.ebb9d9a8.png" class="partner-logo monsieurhugo"></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-2e16ccc7="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-2e16ccc7="" alt="logo monsieur hugo" src="/img/monsieur_hugo.ebb9d9a8.png" class="partner-logo monsieurhugo"></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/](https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/](https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/](https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="//docs.dossierfacile.fr" target="_blank" rel="noreferrer" class="fr-footer__bottom-link"> Help </a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-2e16ccc7="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-2e16ccc7="" alt="logo monsieur hugo" src="/img/monsieur_hugo.ebb9d9a8.png" class="partner-logo monsieurhugo"></a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/js/dsfr.module.min.js](https://www.dossierfacile.fr/js/dsfr.module.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class r{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(t){this.closures.push(t);return()=>{const e=this.closures.indexOf(t);-1!==e&&this.closures.splice(e,1)}}next(t,e){e=void 0===e?0:e-1,void 0===this.nexts[e]&&(this.nexts[e]=[]),this.nexts[e].push(t)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const t=this.nexts.shift();if(t)for(const e of t)e.call()}}const o=new class{constructor(){this.renderer=new r}register(t,e){}start(){}stop(){}};class h{constructor(t,e){this.selector=t,this.builders=e,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let t=0;t<this.builders.length;t++)this.instances.push(this.builders[t]())}}const l={},c={};let a=0;const d=t=>{for(const e in c)if(c[e]===t)return e;a++;const e=a;return c[e]=t,e};class u{constructor(t,e,s){const i=d(t);l[i]||(l[i]=[]),l[i].push(this),this.element=t,this.id=t.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=e,this.isRendering=s}dispatch(t,e){const s=new CustomEvent(t,e);this.element.dispatchEvent(s)}listen(t,e){this.listeners[t]||(this.listeners[t]=[]),this.listeners[t].indexOf(e)>-1||(this.listeners[t].push(e),this.element.addEventListener(t,e))}unlisten(t,e){if(t)if(e){if(!this.listeners[t])return;const s=this.listeners[t].indexOf(e);s>-1&&this.listeners[t].splice(s,1),this.element.removeEventListener(e)}else{if(!this.listeners[t])return;for(const e of this.listeners[t])this.element.removeEventListener(e);this.listeners[t].length=0}else for(const t in this.listeners)this.unlisten(t)}get isRendering(){return this._isRendering}set isRendering(t){this._isRendering!==t&&(this._isRendering=t)}render(){}get isResizing(){return this._isResizing}set isResizing(t){this._isResizing!==t&&(this._isResizing=t)}resize(){}destroy(){}static getInstances(t,e){const s=d(t);return l[s]?e?l[s].filter((t=>t instanceof e)):l[s]:null}}const m=e.attr("group"),p=[];class g{constructor(t,e){this.id=t,this.element=e,this.members=[],this._index=-1,this._current=null,p.push(this)}static getGroupById(t){for(const e of p)if(e.constructor===this&&e.id===t)return e;return new this(t)}static getGroupByElement(t){for(const e of p)if(e.element===t)return e;return new this(!1,t)}static groupById(t,e){const s=t.element.getAttribute(m);if(null===s)return;e.getGroupById(s).add(t)}static groupByParent(t,e,s){if(void 0===s&&(s=e.selector),""===s)return;let i=t.element.parentElement;for(;i;){if(i.classList.contains(t.constructor.selector))return;if(i.classList.contains(s)){return void e.getGroupByElement(i).add(t)}i=i.parentElement}}static get selector(){return""}add(t){if(-1===this.members.indexOf(t))switch(this.members.push(t),t.setGroup(this),!0){case null!==this.current:case!t.disclosed&&!t.primal:t.disclosed=!1;break;default:this._current=t,this._index=this.members.indexOf(t),t.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(t){t<-1||t>=this.length||this._index===t||(null!==this.current&&this.current.conceal(!0,!0),this._index=t,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(t){this.index=this.members.indexOf(t)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class b{constructor(t,e){this.element=t,this.disclosure=e,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(t){this.disclosure.change(this.hasAttribute)}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(t){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,t),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const f=e.event("DISCLOSE"),y=e.event("CONCEAL"),v=[];class w extends u{constructor(t){super(t),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:e.attr(this.type.id),this.pristine=!0;const s=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:e.attr.selector("controls",this.id));if(s.length>0)for(let t=0;t<s.length;t++)this.addButton(s[t]);this.disclosed=!0===this.primal,this.gather()}gather(){this.group||(g.groupById(this,this.GroupConstructor),g.groupByParent(this,this.GroupConstructor))}static build(t){const e=Array.prototype.slice.call(t.querySelectorAll(`.${this.selector}`));for(const t of e)v.push(new this(t))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(t){const e=this.buttonFactory(t);e.hasAttribute&&(void 0===this.primal?this.primal=e.disclosed:e.apply(this.primal)),this.buttons.push(e)}get GroupConstructor(){return g}buttonFactory(t){return new b(t,this)}disclose(t){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,t||void 0===this.group||(this.group.current=this),!0)}conceal(t,e){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,e||this.focus(),t||void 0===this.group||(this.group.current=null);for(const t of v)t!==this&&this.element.contains(t.element)&&t.reset();return!0}get disclosed(){return this._disclosed}set disclosed(t){if(this._disclosed!==t){this.dispatch(t?f:y,this.type),this._disclosed=t,t?i(this.element,this.modifier):n(this.element,this.modifier);for(let e=0;e<this.buttons.length;e++)this.buttons[e].apply(t)}}reset(){}change(t){if(this.constructor.type.canConceal)switch(!0){case!t:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(t){this.group=t}get buttonHasFocus(){return!!this.buttons.some((t=>t.hasFocus))}get hasFocus(){return this.element===document.activeElement||(this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus)}focus(){for(let t=0;t<this.buttons.length;t++){const e=this.buttons[t];if(e.hasAttribute)return void e.element.focus()}}}w.DISCLOSE_EVENT=f,w.CONCEAL_EVENT=y;const E={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class x{constructor(t){this.element=t,this.collections={}}_add(t,e){void 0===this.collections[t]&&(this.collections[t]=new L(t,this.element)),this.collections[t].add(e)}down(t,e,s,i){this._add("down",new S(t,e,s,i))}up(t,e,s,i){this._add("up",new S(t,e,s,i))}dispose(){for(const t of this.collections)t.dispose();this.types=null}}class L{constructor(t,e){this.type=t,this.element=e,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+t,this.binding)}add(t){this.actions.push(t)}handle(t){for(const e of this.actions)e.handle(t)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class S{constructor(t,e,s,i){this.key=t,this.closure=e,this.preventDefault=!0===s,this.stopPropagation=!0===i}handle(t){t.keyCode===this.key&&(this.closure(t),this.preventDefault&&t.preventDefault(),this.stopPropagation&&t.stopPropagation())}}x.TAB=9,x.ESCAPE=27,x.END=35,x.HOME=36,x.LEFT=37,x.UP=38,x.RIGHT=39,x.DOWN=40;const A=e("collapse"),C=[],_={};class k extends w{constructor(t){super(t),C.push(this),this.requesting=this.request.bind(this),t.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const t in _){let e=this.element.parentElement;for(;e;){if(e.classList.contains(t))return void("string"==typeof _[t]?g.groupByParent(this,g,_[t]):g.groupByParent(this,_[t]));e=e.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return E.expand}static get selector(){return A}static register(t,e){_[t]=e;for(const t of C)t.gatherByAscendants()}transitionend(t){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(t){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(t)},window.requestAnimationFrame(this.requesting))}conceal(t,e){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(t,e)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const t=this.element.offsetHeight;this.element.style.setProperty("--collapse",-t+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}t.core.ns=e,t.core.addClass=i,t.core.removeClass=n,t.core.engine=o,t.core.Instance=u,t.core.Initializer=h,t.core.Disclosure=w,t.core.DisclosureButton=b,t.core.DisclosuresGroup=g,t.core.DISCLOSURE_TYPES=E,t.KeyListener=x,t.Collapse=k,t.Equisized=class{constructor(t,e){this.selector=t,this.group=e,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let t=0;t<this.elements.length;t++){const e=this._getWidth(this.elements[t]);e>this.maxWidth&&(this.maxWidth=e)}this.apply()}apply(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width=this.maxWidth+1+"px"}reset(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width="auto";this.maxWidth=0}_getWidth(t){let e=t.offsetWidth;const s=getComputedStyle(t);return e+=parseInt(s.marginLeft)+parseInt(s.marginRight),e}};new h(`.${A}`,[()=>{k.build(document)}]);const q=t.core.ns("accordions-group"),I=t.core.ns("accordion");class z extends t.core.DisclosuresGroup{static get selector(){return q}}t.AccordionsGroup=z,t.Collapse.register(I,z);const D=`${t.core.ns.selector("breadcrumb")} ${t.core.ns.selector("collapse")}`;class H extends t.core.Instance{constructor(e){super(e),this.collapse=t.core.Instance.getInstances(e,t.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(t.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),t.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new t.core.Initializer(D,[()=>{const t=[],e=document.querySelectorAll(D);for(let s=0;s<e.length;s++)t.push(new H(e[s]))}]);const P=t.core.ns.selector("btn"),O=t.core.ns.selector("btns-group"),T=t.core.ns.selector("btns-group--equisized");new t.core.Initializer(O,[()=>{const e=document.querySelectorAll(T),s=[];for(let i=0;i<e.length;i++)s.push(new t.Equisized(P,e[i]))}]);const B=t.core.ns.selector("modal"),N=t.core.ns("modal"),G=t.core.ns("no-scroll"),R=t.core.ns("scroll-shadow"),$=t.core.ns.selector("modal__body"),F=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),W=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),M=(t,e)=>{if("hidden"===window.getComputedStyle(t).visibility)return!1;for(void 0===e&&(e=t);e.contains(t);){if("none"===window.getComputedStyle(t).display)return!1;t=t.parentElement}return!0};class K{constructor(t,e){this.element=null,this.activeElement=null,this.onTrap=t,this.onUntrap=e,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(t){this.trapped&&this.untrap(),this.element=t,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){M(this.element)?this.trapping():t.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const t=this.focusables;t.length&&t[0].focus(),this.element.setAttribute("aria-modal",!0),this.element.addEventListener("keydown",this.handling),this.stunneds=[]}stun(t){for(const e of t.children)e!==this.element&&(e.contains(this.element)?this.stun(e):this.stunneds.push(new V(e)))}handle(t){if(9!==t.keyCode)return;const e=this.focusables;if(0===e.length)return;const s=e[0],i=e[e.length-1],n=e.indexOf(document.activeElement);t.shiftKey?!this.element.contains(document.activeElement)||n<1?(t.preventDefault(),i.focus()):(document.activeElement.tabIndex>0||e[n-1].tabIndex>0)&&(t.preventDefault(),e[n-1].focus()):this.element.contains(document.activeElement)&&n!==e.length-1&&-1!==n?document.activeElement.tabIndex>0&&(t.preventDefault(),e[n+1].focus()):(t.preventDefault(),s.focus())}get focusables(){let t=[...this.element.querySelectorAll(F)];const e=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(e.length){const s={};for(const t of e){const e=t.getAttribute("name");void 0===s[e]&&(s[e]=new U(e)),s[e].push(t)}t=t.filter((t=>{if("input"!==t.tagName.toLowerCase()||"radio"!==t.getAttribute("type").toLowerCase())return!0;const e=t.getAttribute("name");return s[e].keep(t)}))}const s=[...this.element.querySelectorAll(W)];s.sort(((t,e)=>t.tabIndex-e.tabIndex));const i=t.filter((t=>-1===s.indexOf(t)));return s.concat(i).filter((t=>"-1"!==t.tabIndex&&M(t,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),this.element.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class V{constructor(t){this.element=t,this.hidden=t.getAttribute("aria-hidden"),this.inert=t.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class U{constructor(t){this.name=t,this.buttons=[]}push(t){this.buttons.push(t),(t===document.activeElement||t.checked||void 0===this.selected)&&(this.selected=t)}keep(t){return this.selected===t}}class j extends t.core.DisclosuresGroup{constructor(){super(),this.trap=new K}apply(t,e){super.apply(t,e),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const Y=new j;class J extends t.core.Disclosure{constructor(t){super(t),this.body=this.element.querySelector($),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(t){this.body&&this.body!==t.target&&!this.body.contains(t.target)&&this.conceal()}gather(){Y.add(this)}disclose(t){return!!super.disclose(t)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(t,e){return!!super.conceal(t,e)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(t.core.removeClass(document.documentElement,G),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(G)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",t.core.addClass(document.documentElement,G))}resize(e,s){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?t.core.removeClass(this.body,R):t.core.addClass(this.body,R):t.core.removeClass(this.body,R),e&&(this.body.style.maxHeight=window.innerHeight-32+"px",t.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"}))))}static get type(){return t.core.DISCLOSURE_TYPES.opened}static get selector(){return N}get GroupConstructor(){return j}}t.Modal=J,t.ModalsGroup=j,t.FocusTrap=K;new t.core.Initializer(B,[()=>{J.build(document)}]);const Q=t.core.ns("nav"),X=t.core.ns("nav__list"),Z=t.core.ns("nav__item"),tt=t.core.ns("nav__item--align-right"),et=t.core.ns("menu");class st extends t.core.DisclosuresGroup{constructor(t,e){super(t,e),this.menus=[],this.navList=e.querySelector(`.${X}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return Q}add(t){super.add(t),t.element.classList.contains(et)&&this.menus.push(new it(t,this.navList.getBoundingClientRect().right))}focusOut(t){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(t){-1===t&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=t}resize(){const t=this.navList.getBoundingClientRect().right;for(const e of this.menus)e.place(t)}}class it{constructor(t,e){this.initialize(t),this.place(e)}initialize(t){this.element=t.element;for(const e of t.buttons)if(e.hasAttribute){this.button=e.element;break}let e=this.element.parentElement;for(;e;){if(e.classList.contains(Z)){this.item=e;break}e=e.parentElement}}place(e){const s=getComputedStyle(this.element),i=parseFloat(s.width);this.button.getBoundingClientRect().left+i>e?t.core.addClass(this.item,tt):t.core.removeClass(this.item,tt)}}t.Navigation=st,t.Collapse.register(Q,st);const nt=t.core.ns.attr("theme"),rt=t.core.ns.attr("transition");class ot{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const t=this.root.getAttribute(nt);"dark"===t||"light"===t?this.scheme=t:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(rt)?(this.root.removeAttribute(rt),this.root.setAttribute(nt,"dark"),setTimeout((()=>{this.root.setAttribute(rt,"")}),300)):this.root.setAttribute(nt,"dark"):this.root.setAttribute(nt,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(t){t.forEach((t=>{if("attributes"===t.type&&t.attributeName===nt){const t=this.root.getAttribute(nt);"dark"===t?localStorage.setItem("scheme","dark"):"light"===t&&localStorage.setItem("scheme","light")}}))}}t.Scheme=ot;const ht=`input[name="${t.core.ns.selector("radios-theme","")}"]`,lt=t.core.ns.selector("switch-theme","#"),ct=t.core.ns.attr("theme");class at{constructor(){this.attributeName=ct,this.theme=null,this.radios=document.querySelectorAll(ht);for(var t=0;t<this.radios.length;t++)this.radios[t].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.attributeName&&this.apply()}))}apply(){const t=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var e=0;e<this.radios.length;e++)this.radios[e].checked=this.radios[e].value===t;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(ht+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new t.core.Initializer(`:root[${nt}]`,[()=>{new ot}]),new t.core.Initializer(`${lt}`,[()=>{new at}]);const dt=t.core.ns("sidemenu"),ut=t.core.ns("sidemenu__list");t.Collapse.register(dt,ut);const mt=t.core.ns.selector("table"),pt=`${t.core.ns.selector("table")}:not(${t.core.ns.selector("table--no-scroll")})`,gt=t.core.ns("table--shadow"),bt=t.core.ns("table--shadow-left"),ft=t.core.ns("table--shadow-right"),yt=t.core.ns("table__wrapper"),vt=t.core.ns("table--caption-bottom");class wt{constructor(t){this.init(t)}init(t){this.table=t,this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0,this.wrap();const e=this.change.bind(this);this.tableElem.addEventListener("scroll",e),this.change()}change(){const t=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let e=this.tableElem.offsetWidth>this.table.offsetWidth;t||e?(this.scroll(),this.handleCaption()):t!==this.isScrollable&&this.delete(),this.isScrollable=t,e=!1}delete(){t.core.removeClass(this.table,ft),t.core.removeClass(this.table,bt),t.core.removeClass(this.table,gt),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){t.core.addClass(this.table,gt),this.setShadowPosition()}wrap(){const t=document.createElement("div");t.className=yt,this.table.insertBefore(t,this.tableElem),t.appendChild(this.tableElem),this.tableInnerWrapper=t}setShadowPosition(){const t=this.getScrollPosition("left"),e=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",t),this.setShadowVisibility("left",e)):(this.setShadowVisibility("left",t),this.setShadowVisibility("right",e))}getScrollPosition(t){let e=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(e=-1),t){case"left":return this.tableElem.scrollLeft*e;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*e;default:return!1}}handleCaption(){if(this.caption){const t=getComputedStyle(this.caption),e=this.caption.offsetHeight+parseInt(t.marginTop)+parseInt(t.marginBottom);this.captionHeight=e,this.table.classList.contains(vt)?(this.tableElem.style.marginBottom=this.captionHeight+"px",this.caption.style.bottom=-this.captionHeight+"px"):(this.tableElem.style.marginTop=this.captionHeight+"px",this.caption.style.top=-this.captionHeight+"px")}}setShadowVisibility(e,s){s<=1?"left"===e?t.core.removeClass(this.table,bt):"right"===e&&t.core.removeClass(this.table,ft):"left"===e?t.core.addClass(this.table,bt):"right"===e&&t.core.addClass(this.table,ft)}}t.Table=wt;const Et=[],xt=()=>{for(let t=0;t<Et.length;t++)Et[t].change()};new t.core.Initializer(mt,[()=>{const t=document.querySelectorAll(pt);for(let e=0;e<t.length;e++)Et.push(new wt(t[e]));window.addEventListener("resize",xt),window.addEventListener("orientationchange",xt),xt()}]);class Lt extends t.core.DisclosureButton{apply(t){super.apply(t),this.hasAttribute&&this.element.setAttribute("tabindex",t?"0":"-1")}}const St=t.core.ns.selector("tabs"),At=t.core.ns("tabs"),Ct=t.core.ns("tabs__tab"),_t=t.core.ns("tabs__panel"),kt=t.core.ns("tabs__list");class qt extends t.core.DisclosuresGroup{constructor(e,s){super(e,s),this.list=s.querySelector(`.${kt}`),s.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),t.core.engine.renderer.add(this.render.bind(this))}static get selector(){return At}transitionend(t){this.element.style.transition="none"}init(){this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(Ct)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(Ct)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(Ct)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(Ct)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let t=0;t<this._index;t++)this.members[t].translate(-1);this.current.element.style.transform="";for(let t=this._index+1;t<this.length;t++)this.members[t].translate(1);this.element.style.transition=""}add(t){if(super.add(t),1===this.length||t.disclosed)this.current=t;else{const e=this.members.indexOf(t);this._index>-1&&this._index!==e&&t.translate(e<this._index?-1:1,!0)}}render(){if(null===this.current)return;const t=Math.round(this.current.element.offsetHeight);this.panelHeight!==t&&(this.panelHeight=t,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class It extends t.core.Disclosure{static get type(){return t.core.DISCLOSURE_TYPES.select}static get selector(){return _t}get GroupConstructor(){return qt}buttonFactory(t){return new Lt(t,this)}translate(t,e){e&&(this.element.style.transition="none"),this.element.style.transform=`translate(${100*t}%)`,e&&(this.element.style.transition="")}reset(){this.group.index=0}}t.Tab=It,t.TabButton=Lt,t.TabsGroup=qt;new t.core.Initializer(St,[()=>{It.build(document)}]);const zt=t.core.ns.selector("header"),Dt=t.core.ns.selector("header__search"),Ht=t.core.ns.selector("header__menu"),Pt=t.core.ns.selector("header__tools-links"),Ot=t.core.ns.selector("header__menu-links"),Tt=`${Pt} ${t.core.ns.selector("links-group")}`;class Bt{constructor(t){this.header=t||document.querySelector(zt),this.modals=[],this.init()}getModal(e){const s=this.header.querySelector(e);if(!s)return;const i=t.core.Instance.getInstances(s,t.Modal);i&&i.length&&this.modals.push(i[0])}init(){this.getModal(Dt),this.getModal(Ht),this.linksGroup=this.header.querySelector(Tt),this.toolsLinks=this.header.querySelector(Pt),this.menuLinks=this.header.querySelector(Ot),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){if(this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge)for(let t=0;t<this.modals.length;t++)this.modals[t].conceal(),this.modals[t].element.removeAttribute("role");else for(let t=0;t<this.modals.length;t++)this.modals[t].element.setAttribute("role","dialog");null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}t.Header=Bt;new t.core.Initializer(zt,[()=>{const t=Array.prototype.slice.call(document.querySelectorAll(zt)),e=[];for(const s of t)e.push(new Bt(s))}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class r{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(t){this.closures.push(t);return()=>{const e=this.closures.indexOf(t);-1!==e&&this.closures.splice(e,1)}}next(t,e){e=void 0===e?0:e-1,void 0===this.nexts[e]&&(this.nexts[e]=[]),this.nexts[e].push(t)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const t=this.nexts.shift();if(t)for(const e of t)e.call()}}const o=new class{constructor(){this.renderer=new r}register(t,e){}start(){}stop(){}};class h{constructor(t,e){this.selector=t,this.builders=e,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let t=0;t<this.builders.length;t++)this.instances.push(this.builders[t]())}}const l={},c={};let a=0;const d=t=>{for(const e in c)if(c[e]===t)return e;a++;const e=a;return c[e]=t,e};class u{constructor(t,e,s){const i=d(t);l[i]||(l[i]=[]),l[i].push(this),this.element=t,this.id=t.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=e,this.isRendering=s}dispatch(t,e){const s=new CustomEvent(t,e);this.element.dispatchEvent(s)}listen(t,e){this.listeners[t]||(this.listeners[t]=[]),this.listeners[t].indexOf(e)>-1||(this.listeners[t].push(e),this.element.addEventListener(t,e))}unlisten(t,e){if(t)if(e){if(!this.listeners[t])return;const s=this.listeners[t].indexOf(e);s>-1&&this.listeners[t].splice(s,1),this.element.removeEventListener(e)}else{if(!this.listeners[t])return;for(const e of this.listeners[t])this.element.removeEventListener(e);this.listeners[t].length=0}else for(const t in this.listeners)this.unlisten(t)}get isRendering(){return this._isRendering}set isRendering(t){this._isRendering!==t&&(this._isRendering=t)}render(){}get isResizing(){return this._isResizing}set isResizing(t){this._isResizing!==t&&(this._isResizing=t)}resize(){}destroy(){}static getInstances(t,e){const s=d(t);return l[s]?e?l[s].filter((t=>t instanceof e)):l[s]:null}}const m=e.attr("group"),p=[];class g{constructor(t,e){this.id=t,this.element=e,this.members=[],this._index=-1,this._current=null,p.push(this)}static getGroupById(t){for(const e of p)if(e.constructor===this&&e.id===t)return e;return new this(t)}static getGroupByElement(t){for(const e of p)if(e.element===t)return e;return new this(!1,t)}static groupById(t,e){const s=t.element.getAttribute(m);if(null===s)return;e.getGroupById(s).add(t)}static groupByParent(t,e,s){if(void 0===s&&(s=e.selector),""===s)return;let i=t.element.parentElement;for(;i;){if(i.classList.contains(t.constructor.selector))return;if(i.classList.contains(s)){return void e.getGroupByElement(i).add(t)}i=i.parentElement}}static get selector(){return""}add(t){if(-1===this.members.indexOf(t))switch(this.members.push(t),t.setGroup(this),!0){case null!==this.current:case!t.disclosed&&!t.primal:t.disclosed=!1;break;default:this._current=t,this._index=this.members.indexOf(t),t.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(t){t<-1||t>=this.length||this._index===t||(null!==this.current&&this.current.conceal(!0,!0),this._index=t,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(t){this.index=this.members.indexOf(t)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class b{constructor(t,e){this.element=t,this.disclosure=e,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(t){this.disclosure.change(this.hasAttribute)}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(t){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,t),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const f=e.event("DISCLOSE"),y=e.event("CONCEAL"),v=[];class w extends u{constructor(t){super(t),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:e.attr(this.type.id),this.pristine=!0;const s=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:e.attr.selector("controls",this.id));if(s.length>0)for(let t=0;t<s.length;t++)this.addButton(s[t]);this.disclosed=!0===this.primal,this.gather()}gather(){this.group||(g.groupById(this,this.GroupConstructor),g.groupByParent(this,this.GroupConstructor))}static build(t){const e=Array.prototype.slice.call(t.querySelectorAll(`.${this.selector}`));for(const t of e)v.push(new this(t))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(t){const e=this.buttonFactory(t);e.hasAttribute&&(void 0===this.primal?this.primal=e.disclosed:e.apply(this.primal)),this.buttons.push(e)}get GroupConstructor(){return g}buttonFactory(t){return new b(t,this)}disclose(t){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,t||void 0===this.group||(this.group.current=this),!0)}conceal(t,e){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,e||this.focus(),t||void 0===this.group||(this.group.current=null);for(const t of v)t!==this&&this.element.contains(t.element)&&t.reset();return!0}get disclosed(){return this._disclosed}set disclosed(t){if(this._disclosed!==t){this.dispatch(t?f:y,this.type),this._disclosed=t,t?i(this.element,this.modifier):n(this.element,this.modifier);for(let e=0;e<this.buttons.length;e++)this.buttons[e].apply(t)}}reset(){}change(t){if(this.constructor.type.canConceal)switch(!0){case!t:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(t){this.group=t}get buttonHasFocus(){return!!this.buttons.some((t=>t.hasFocus))}get hasFocus(){return this.element===document.activeElement||(this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus)}focus(){for(let t=0;t<this.buttons.length;t++){const e=this.buttons[t];if(e.hasAttribute)return void e.element.focus()}}}w.DISCLOSE_EVENT=f,w.CONCEAL_EVENT=y;const E={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class x{constructor(t){this.element=t,this.collections={}}_add(t,e){void 0===this.collections[t]&&(this.collections[t]=new L(t,this.element)),this.collections[t].add(e)}down(t,e,s,i){this._add("down",new S(t,e,s,i))}up(t,e,s,i){this._add("up",new S(t,e,s,i))}dispose(){for(const t of this.collections)t.dispose();this.types=null}}class L{constructor(t,e){this.type=t,this.element=e,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+t,this.binding)}add(t){this.actions.push(t)}handle(t){for(const e of this.actions)e.handle(t)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class S{constructor(t,e,s,i){this.key=t,this.closure=e,this.preventDefault=!0===s,this.stopPropagation=!0===i}handle(t){t.keyCode===this.key&&(this.closure(t),this.preventDefault&&t.preventDefault(),this.stopPropagation&&t.stopPropagation())}}x.TAB=9,x.ESCAPE=27,x.END=35,x.HOME=36,x.LEFT=37,x.UP=38,x.RIGHT=39,x.DOWN=40;const A=e("collapse"),C=[],_={};class k extends w{constructor(t){super(t),C.push(this),this.requesting=this.request.bind(this),t.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const t in _){let e=this.element.parentElement;for(;e;){if(e.classList.contains(t))return void("string"==typeof _[t]?g.groupByParent(this,g,_[t]):g.groupByParent(this,_[t]));e=e.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return E.expand}static get selector(){return A}static register(t,e){_[t]=e;for(const t of C)t.gatherByAscendants()}transitionend(t){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(t){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(t)},window.requestAnimationFrame(this.requesting))}conceal(t,e){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(t,e)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const t=this.element.offsetHeight;this.element.style.setProperty("--collapse",-t+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}t.core.ns=e,t.core.addClass=i,t.core.removeClass=n,t.core.engine=o,t.core.Instance=u,t.core.Initializer=h,t.core.Disclosure=w,t.core.DisclosureButton=b,t.core.DisclosuresGroup=g,t.core.DISCLOSURE_TYPES=E,t.KeyListener=x,t.Collapse=k,t.Equisized=class{constructor(t,e){this.selector=t,this.group=e,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let t=0;t<this.elements.length;t++){const e=this._getWidth(this.elements[t]);e>this.maxWidth&&(this.maxWidth=e)}this.apply()}apply(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width=this.maxWidth+1+"px"}reset(){for(let t=0;t<this.elements.length;t++)this.elements[t].style.width="auto";this.maxWidth=0}_getWidth(t){let e=t.offsetWidth;const s=getComputedStyle(t);return e+=parseInt(s.marginLeft)+parseInt(s.marginRight),e}};new h(`.${A}`,[()=>{k.build(document)}]);const q=t.core.ns("accordions-group"),I=t.core.ns("accordion");class z extends t.core.DisclosuresGroup{static get selector(){return q}}t.AccordionsGroup=z,t.Collapse.register(I,z);const D=`${t.core.ns.selector("breadcrumb")} ${t.core.ns.selector("collapse")}`;class H extends t.core.Instance{constructor(e){super(e),this.collapse=t.core.Instance.getInstances(e,t.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(t.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),t.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new t.core.Initializer(D,[()=>{const t=[],e=document.querySelectorAll(D);for(let s=0;s<e.length;s++)t.push(new H(e[s]))}]);const P=t.core.ns.selector("btn"),O=t.core.ns.selector("btns-group"),T=t.core.ns.selector("btns-group--equisized");new t.core.Initializer(O,[()=>{const e=document.querySelectorAll(T),s=[];for(let i=0;i<e.length;i++)s.push(new t.Equisized(P,e[i]))}]);const B=t.core.ns.selector("modal"),N=t.core.ns("modal"),G=t.core.ns("no-scroll"),R=t.core.ns("scroll-shadow"),$=t.core.ns.selector("modal__body"),F=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),W=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),M=(t,e)=>{if("hidden"===window.getComputedStyle(t).visibility)return!1;for(void 0===e&&(e=t);e.contains(t);){if("none"===window.getComputedStyle(t).display)return!1;t=t.parentElement}return!0};class K{constructor(t,e){this.element=null,this.activeElement=null,this.onTrap=t,this.onUntrap=e,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(t){this.trapped&&this.untrap(),this.element=t,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){M(this.element)?this.trapping():t.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const t=this.focusables;t.length&&t[0].focus(),this.element.setAttribute("aria-modal",!0),this.element.addEventListener("keydown",this.handling),this.stunneds=[]}stun(t){for(const e of t.children)e!==this.element&&(e.contains(this.element)?this.stun(e):this.stunneds.push(new V(e)))}handle(t){if(9!==t.keyCode)return;const e=this.focusables;if(0===e.length)return;const s=e[0],i=e[e.length-1],n=e.indexOf(document.activeElement);t.shiftKey?!this.element.contains(document.activeElement)||n<1?(t.preventDefault(),i.focus()):(document.activeElement.tabIndex>0||e[n-1].tabIndex>0)&&(t.preventDefault(),e[n-1].focus()):this.element.contains(document.activeElement)&&n!==e.length-1&&-1!==n?document.activeElement.tabIndex>0&&(t.preventDefault(),e[n+1].focus()):(t.preventDefault(),s.focus())}get focusables(){let t=[...this.element.querySelectorAll(F)];const e=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(e.length){const s={};for(const t of e){const e=t.getAttribute("name");void 0===s[e]&&(s[e]=new U(e)),s[e].push(t)}t=t.filter((t=>{if("input"!==t.tagName.toLowerCase()||"radio"!==t.getAttribute("type").toLowerCase())return!0;const e=t.getAttribute("name");return s[e].keep(t)}))}const s=[...this.element.querySelectorAll(W)];s.sort(((t,e)=>t.tabIndex-e.tabIndex));const i=t.filter((t=>-1===s.indexOf(t)));return s.concat(i).filter((t=>"-1"!==t.tabIndex&&M(t,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),this.element.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class V{constructor(t){this.element=t,this.hidden=t.getAttribute("aria-hidden"),this.inert=t.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class U{constructor(t){this.name=t,this.buttons=[]}push(t){this.buttons.push(t),(t===document.activeElement||t.checked||void 0===this.selected)&&(this.selected=t)}keep(t){return this.selected===t}}class j extends t.core.DisclosuresGroup{constructor(){super(),this.trap=new K}apply(t,e){super.apply(t,e),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const Y=new j;class J extends t.core.Disclosure{constructor(t){super(t),this.body=this.element.querySelector($),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(t){this.body&&this.body!==t.target&&!this.body.contains(t.target)&&this.conceal()}gather(){Y.add(this)}disclose(t){return!!super.disclose(t)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(t,e){return!!super.conceal(t,e)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(t.core.removeClass(document.documentElement,G),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(G)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",t.core.addClass(document.documentElement,G))}resize(e,s){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?t.core.removeClass(this.body,R):t.core.addClass(this.body,R):t.core.removeClass(this.body,R),e&&(this.body.style.maxHeight=window.innerHeight-32+"px",t.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"}))))}static get type(){return t.core.DISCLOSURE_TYPES.opened}static get selector(){return N}get GroupConstructor(){return j}}t.Modal=J,t.ModalsGroup=j,t.FocusTrap=K;new t.core.Initializer(B,[()=>{J.build(document)}]);const Q=t.core.ns("nav"),X=t.core.ns("nav__list"),Z=t.core.ns("nav__item"),tt=t.core.ns("nav__item--align-right"),et=t.core.ns("menu");class st extends t.core.DisclosuresGroup{constructor(t,e){super(t,e),this.menus=[],this.navList=e.querySelector(`.${X}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return Q}add(t){super.add(t),t.element.classList.contains(et)&&this.menus.push(new it(t,this.navList.getBoundingClientRect().right))}focusOut(t){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(t){-1===t&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=t}resize(){const t=this.navList.getBoundingClientRect().right;for(const e of this.menus)e.place(t)}}class it{constructor(t,e){this.initialize(t),this.place(e)}initialize(t){this.element=t.element;for(const e of t.buttons)if(e.hasAttribute){this.button=e.element;break}let e=this.element.parentElement;for(;e;){if(e.classList.contains(Z)){this.item=e;break}e=e.parentElement}}place(e){const s=getComputedStyle(this.element),i=parseFloat(s.width);this.button.getBoundingClientRect().left+i>e?t.core.addClass(this.item,tt):t.core.removeClass(this.item,tt)}}t.Navigation=st,t.Collapse.register(Q,st);const nt=t.core.ns.attr("theme"),rt=t.core.ns.attr("transition");class ot{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const t=this.root.getAttribute(nt);"dark"===t||"light"===t?this.scheme=t:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(rt)?(this.root.removeAttribute(rt),this.root.setAttribute(nt,"dark"),setTimeout((()=>{this.root.setAttribute(rt,"")}),300)):this.root.setAttribute(nt,"dark"):this.root.setAttribute(nt,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(t){t.forEach((t=>{if("attributes"===t.type&&t.attributeName===nt){const t=this.root.getAttribute(nt);"dark"===t?localStorage.setItem("scheme","dark"):"light"===t&&localStorage.setItem("scheme","light")}}))}}t.Scheme=ot;const ht=`input[name="${t.core.ns.selector("radios-theme","")}"]`,lt=t.core.ns.selector("switch-theme","#"),ct=t.core.ns.attr("theme");class at{constructor(){this.attributeName=ct,this.theme=null,this.radios=document.querySelectorAll(ht);for(var t=0;t<this.radios.length;t++)this.radios[t].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(t){t.forEach((t=>{"attributes"===t.type&&t.attributeName===this.attributeName&&this.apply()}))}apply(){const t=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var e=0;e<this.radios.length;e++)this.radios[e].checked=this.radios[e].value===t;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(ht+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new t.core.Initializer(`:root[${nt}]`,[()=>{new ot}]),new t.core.Initializer(`${lt}`,[()=>{new at}]);const dt=t.core.ns("sidemenu"),ut=t.core.ns("sidemenu__list");t.Collapse.register(dt,ut);const mt=t.core.ns.selector("table"),pt=`${t.core.ns.selector("table")}:not(${t.core.ns.selector("table--no-scroll")})`,gt=t.core.ns("table--shadow"),bt=t.core.ns("table--shadow-left"),ft=t.core.ns("table--shadow-right"),yt=t.core.ns("table__wrapper"),vt=t.core.ns("table--caption-bottom");class wt{constructor(t){this.init(t)}init(t){this.table=t,this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0,this.wrap();const e=this.change.bind(this);this.tableElem.addEventListener("scroll",e),this.change()}change(){const t=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let e=this.tableElem.offsetWidth>this.table.offsetWidth;t||e?(this.scroll(),this.handleCaption()):t!==this.isScrollable&&this.delete(),this.isScrollable=t,e=!1}delete(){t.core.removeClass(this.table,ft),t.core.removeClass(this.table,bt),t.core.removeClass(this.table,gt),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){t.core.addClass(this.table,gt),this.setShadowPosition()}wrap(){const t=document.createElement("div");t.className=yt,this.table.insertBefore(t,this.tableElem),t.appendChild(this.tableElem),this.tableInnerWrapper=t}setShadowPosition(){const t=this.getScrollPosition("left"),e=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",t),this.setShadowVisibility("left",e)):(this.setShadowVisibility("left",t),this.setShadowVisibility("right",e))}getScrollPosition(t){let e=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(e=-1),t){case"left":return this.tableElem.scrollLeft*e;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*e;default:return!1}}handleCaption(){if(this.caption){const t=getComputedStyle(this.caption),e=this.caption.offsetHeight+parseInt(t.marginTop)+parseInt(t.marginBottom);this.captionHeight=e,this.table.classList.contains(vt)?(this.tableElem.style.marginBottom=this.captionHeight+"px",this.caption.style.bottom=-this.captionHeight+"px"):(this.tableElem.style.marginTop=this.captionHeight+"px",this.caption.style.top=-this.captionHeight+"px")}}setShadowVisibility(e,s){s<=1?"left"===e?t.core.removeClass(this.table,bt):"right"===e&&t.core.removeClass(this.table,ft):"left"===e?t.core.addClass(this.table,bt):"right"===e&&t.core.addClass(this.table,ft)}}t.Table=wt;const Et=[],xt=()=>{for(let t=0;t<Et.length;t++)Et[t].change()};new t.core.Initializer(mt,[()=>{const t=document.querySelectorAll(pt);for(let e=0;e<t.length;e++)Et.push(new wt(t[e]));window.addEventListener("resize",xt),window.addEventListener("orientationchange",xt),xt()}]);class Lt extends t.core.DisclosureButton{apply(t){super.apply(t),this.hasAttribute&&this.element.setAttribute("tabindex",t?"0":"-1")}}const St=t.core.ns.selector("tabs"),At=t.core.ns("tabs"),Ct=t.core.ns("tabs__tab"),_t=t.core.ns("tabs__panel"),kt=t.core.ns("tabs__list");class qt extends t.core.DisclosuresGroup{constructor(e,s){super(e,s),this.list=s.querySelector(`.${kt}`),s.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),t.core.engine.renderer.add(this.render.bind(this))}static get selector(){return At}transitionend(t){this.element.style.transition="none"}init(){this.keyListener=new t.KeyListener(this.element),this.keyListener.down(t.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(t.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(Ct)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(Ct)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(Ct)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(Ct)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let t=0;t<this._index;t++)this.members[t].translate(-1);this.current.element.style.transform="";for(let t=this._index+1;t<this.length;t++)this.members[t].translate(1);this.element.style.transition=""}add(t){if(super.add(t),1===this.length||t.disclosed)this.current=t;else{const e=this.members.indexOf(t);this._index>-1&&this._index!==e&&t.translate(e<this._index?-1:1,!0)}}render(){if(null===this.current)return;const t=Math.round(this.current.element.offsetHeight);this.panelHeight!==t&&(this.panelHeight=t,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class It extends t.core.Disclosure{static get type(){return t.core.DISCLOSURE_TYPES.select}static get selector(){return _t}get GroupConstructor(){return qt}buttonFactory(t){return new Lt(t,this)}translate(t,e){e&&(this.element.style.transition="none"),this.element.style.transform=`translate(${100*t}%)`,e&&(this.element.style.transition="")}reset(){this.group.index=0}}t.Tab=It,t.TabButton=Lt,t.TabsGroup=qt;new t.core.Initializer(St,[()=>{It.build(document)}]);const zt=t.core.ns.selector("header"),Dt=t.core.ns.selector("header__search"),Ht=t.core.ns.selector("header__menu"),Pt=t.core.ns.selector("header__tools-links"),Ot=t.core.ns.selector("header__menu-links"),Tt=`${Pt} ${t.core.ns.selector("links-group")}`;class Bt{constructor(t){this.header=t||document.querySelector(zt),this.modals=[],this.init()}getModal(e){const s=this.header.querySelector(e);if(!s)return;const i=t.core.Instance.getInstances(s,t.Modal);i&&i.length&&this.modals.push(i[0])}init(){this.getModal(Dt),this.getModal(Ht),this.linksGroup=this.header.querySelector(Tt),this.toolsLinks=this.header.querySelector(Pt),this.menuLinks=this.header.querySelector(Ot),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){if(this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge)for(let t=0;t<this.modals.length;t++)this.modals[t].conceal(),this.modals[t].element.removeAttribute("role");else for(let t=0;t<this.modals.length;t++)this.modals[t].element.setAttribute("role","dialog");null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}t.Header=Bt;new t.core.Initializer(zt,[()=>{const t=Array.prototype.slice.call(document.querySelectorAll(zt)),e=[];for(const s of t)e.push(new Bt(s))}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article3.5b9ebf4f.png](https://www.dossierfacile.fr/img/blog-article3.5b9ebf4f.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==õ}ÿñãcÒÜÅ®ëº\x0010ÙK\x001dÀEÕËûPÕ·~³\x001fY\x0001+\x001dàg\x0000ì¤\x0006¡Z\x001b÷WÜ¶4ð`\x001cc\x000cû¾ÿúõ«\x0003®îásírÔ[zèv­i¡ó8$k)«èÍ3}Ë;\x001eA[e\x001c84ì6¿v\x0003cho¸:OèdÌNà~³¸g·ý\x000bXW\x0003ÉÈÍ\x000e/zp¬ýr\x0000\x0019a(®"\x0004¡ïhJ3\x0000\x00089Í\x001bÞ!CÏ\x001d³£\x0003´ üÈ@M	Ï	TÍ±­×e¾)§ñ:«ªøÿTÄ ÷Ç­"R\x0008NYEÌ]ÇÌ¡ë:f
¡GDÉyLÉ\x000cä<«
k\x0004;`{\x001d·
ÓÈvÞ\x0002È2í<\x0017Û0ýµì»ïíiß\x0000S¹ÃÍï|ß6B¼7|WÞEßÝ`Äñ>\x001d÷\x000eÀ®8Tó²m\ê\x0003\x0018ÃÛ´ó>Ü\b½_kk0Vå´\x0019ÃþX¯»s¡|¹¡ÄVõ¨à¾U]\x000fm­H\x0013þ£LÎÆAÝþÍî\x0016eÃÍBÖd	BÈ\x0011¹®w\x0006ÚDP\x0016§E\x0011\x001e\x001eÎ-\x0013aè'^Å´\x001b"Å`¨I\x0013\x0002*"rÀ­K¶\x±táfzï;T\x0018½Â_ëîÛ"'ßØJé\x001e\x0008\x0003z c¦i\x00000ÆÐÅ.ppÞ3¯ò ,A/ßqïÇµB\x000fºã"\x0004DÎ\x0012èÎ+\x0007Xà $)eG©
s`\x000e¦Ikm_ÛVùeÛf-ª,UVÑd¿c þ¤¶dxú_»;ÿ£}£\x001d9cÿ^[[ûÄ^µSv
¥®!,áÿ¾ïÍ,%q\x0014ÆîÙZú\x0001oßÜëu\x0015\x0002/\7Ë¯\x0010QT\x0019\x0010?<~@Db O\x0006\x001aUÕ.F
\x0017RJÙë=ÙËËåéé©?õçóùüÐ÷ýÃÃ9~\x0008ló<sW¾&R¾É\x0000¨Ãá&-¹´²¼\x0003\x0002ª§\x0018\x0018XU²­®\x000bâÑyÁÔ¦<9Ýó\x000f)%\x0011ÙT'ÞµvÏåMðw]g\x0002³\x0003¥ÖBõ^vú\x000f%R¤%ý­\x0016Ú¥öÆ\x0007¸=uý\<¿m¼¿¦E\x0010@7\x000f\x000f1å\x0004\x00001DvA\x0007õÔOX\x001dN@Dd.Á~Ï-\x0010¡§¨V\x0006g`·vZ\x000c_ßÖA\x0001\x000c\x0005Lr¢\x0010 ø|\x0000ÛÝ:\x0014È âõ\x0015D4\x000ber§§'Iiç9çRJ³e%¦yÎ\x000e8CDnÆC@ìC`Dêûb9åÉ½\x0002f\x001a¯3\x0011eS3Í5PGª¹ÉL5£Å¶¶\x000frµ\x0003õ\x0008.¶\x000fvËò&\x0001ÎÝoÈ§¶\x0013:·"V
Ð;È7FÌzÛÔVï¼=c³´5¦%ê\Q"²ùÓz¹7l\x001eï4KV\x000cÒÝ\x001f¶ïÔ~
@+@vÀ
U~(°÷\ÜmH[Iù]_¢õ ´9Ú~ÄÑhßa8Ê\x0000(®\x000e\x0000¯SRAm\x000bó[~ÛB,q¸K<zJ¦õ×\x000c«Ñi\x0010ú\x0010{æ.ÙËõ\x001a»\x000e\x0000¦y\x001aÏç!Ïçt¹\x0004$TAd5ËªGõ^DJu\x0003víT[7cr¦c  ¢åÚ\x0001UÀ\x0015£_ðl\x001aÔ\x000c\x0017BÏrg)M)å8beû_dÒÑØ3À÷g"cs)8DC*7±{³"È1ø\x000ejMù Ty2JýifD fºn<Zû»ô>7@5ï\x000cÑ
Ø\x0004´ijã4næ1Üÿ
\x000e2]úZ
p£íò\x0016\x0008ÐÍyà{¤¤\x001drçü¿Ô¦Í;!@¨µÛÎ:Î:·íø|»?h¯<¯ÝÏ\x0010»¿®\x0007\x000fìÝ(£ïÒZfOErZ\x0013\x00138î\rÎ"ªÒ÷½ê¬ià\Î'r2µlJ"ûÛß¬­ù\t×Ý@3\x0000\x0011%âa\x0008ªÛõÜ$tÝà±Ýç§ñzIÃ0<?]ÏçóÃÃ\x00033#¡¨òíÛ½!á`F3'´}E(}ëäû¾kÔÚ0\x001b¨$Cø(çä»®\x001bÇÑ^Ömðå(¸à;\x00023ß¼°9ó²oj\x0015b\x0000p¢!ï!|;È\x001b<Ê\x0003\x0006¦\x001aCtR\x001açq\x0012É\x001eÛö5³y3\x0012\x0011p`¯o\x0000¡ïÓ<3\x0004@0Ë~L\x0017»1Í\x0005¦¹­ÀL\x0018c0³yNÃÐyÌ¼fcì\x00101Pà®ëÌÌ\x001151¤BnW{ ®/1Æ¬êxÙ6Ò\x0012Sà@D\x0011TdNs \x001eÇi\x001cÇóåùùz¹^¯W5Ýg\x0008\x000b\x0006Å\x0010GÈÌ1î4Ä\x0018\x0003\x0011úÖâûªÎ"]ò\x00073%1Â1¥4ç\x0013"ªh65\x0005\x0011S,JË#&\x0003Ün»oóý\x0006\x001cÕðdoïf\x000bk\x000c¾£â×\x0016zñ^ÀPn8M·8ïý\x0015t2c@&BZÁÖ7KêM\x001a}A\x0001YÃW
«±[aÌçÀ¾Ã³ÉNT>c51ªÞ\x0016ÛqÚ}Fw\x0000¹VdcMYÖù#¢ÚÒònÁo\x0014S\x0003TÉ²\x001ePd\x0016)\x0005£±)HºñFvã\x0013wEÏ;}Ðæ<Ñif¡é3¿E|mC\x000fz4\x000f[×¶¨Ý#\x0011\x0000\x0000Y\x0010c×å\x0014çoféìr¹ÄÐ+\x0018Q8N¤ÉáY\x0001Q	\x0010£1L34ÑçeaU«CÑVçY\x000bZÊ\x0010$·EÞê\x0013Æ\x000be83ûZ\x0001ª,ª\x0004\x0016\x0002g3\x0011\x0011\x0005\x0005àÐSr/ç4<|þú%çd\x0000AM²Ót\x000b\x0001 ,BÂ¼s{È\[@tÂ\x0010ò,D\x0005>¹ô?lxñYÍTÌÌ¹Ø=\x0006ªMBÈª&jbÆ\x0001H\x0014kA?\x001dÁupÉê¨¿
¨FÄ¬\x0006d¨Ï¸\x0011öZÃbíú°Á¬\x0001\x0011ð'cÒÎ[\x0003°\x00036#Ò\x0014\x000cÊ\x001e×º\x0013³ì\x0017¯\x001f	Æ\x001eþÕPÖ÷ö&G\x0002@!²\x0005óÉJH\x0006(*åºq\x0012¾éoû|Tô\x0004ñÒÚ)¸]rÞçxÜ\x0011Y¯ÁÝÒI50ªÓ<·\x0019ï
¯ÈÆ¢l>\x00062\x0000{ÊÚë¯¼ØòpÎr-DûH[&ú·Øëá\x001b~¼­Ñ*ø9p{\x000c7&Êó\x001cBdÀátff\x0011I)\x0001AnÆ¡u\x001eLö3±oy\\x0014\x0018Ð\x0010\x0001ÐTäáá\x000cÕ,\x0010\x0018@\x0008\x001d\x0013ÇÇ.DêûÞ)\PXÄæyFET(\x0016\x00061ÂU D\x0011LË]òÞjÒçñåú|}êN§Óé±ï\x0018§ivÒ\x000b0ò-ýfÎ´7æ\x0017l,uç%33E­mF\x0001yqR\x0016&R³4Ï\x0018C©Õ¬R²ÖnC6\x000cuÛ9ÐÖD\x001d\x000c´/M\x000cÜÂ&c_è%nf,ß"úè2óëµ_µ\x0019ò\x0016\x0001\x001aiN70&5s96A©ÒK´Ò<f\x0011\x000eDDª@\x000c$ªçóY^½æýÚDÔ\x000f\x0011\x0000T,Æè *üÿ1÷okãÈ(f\x0007\x0000¤{dfUw¯½õé^\x0017ºÔÓè\x0001ôÞ>´5{zuwUD¸\x0004ÌL\x0017\x0006 33²»Ö\x001aqfj¢#=è$\x0008\x0002vø\x000f¢À½EB ÆÁõ°N\x0011*u<îës\x0005	\x0003\x0005SÛòÖo-\x0010! \x001bäüþ~ÓRe¹ÝÞ·-/·Ûr_<E&âÐk$Ôzª¬m`¢\x0014b!¦df×\x0017Ó
\x0004zX4ûké·èý~33\x0007®\x00188/XT ñ8?È¥oúvvRµ:ûy\\¦izúqUþ\x000c¦ög¡ï§IË}\x001f\x0013\x0003ç\x0000ò\x000eE\x001b»}\x001eî1Öðò\x0004æÊKªÇ¡ÚÿG\x000e­ÒþóH¼\x001b¥Z¼×É!OÇêgÆC`³ªÞ\x000b½þ,F\x000e1<\x000bÄÛÇ\x0014\x0000Ü~µERÃµ)\x0004\x0014Çñ\x0017ÕÀLÄH('ðsÀ/\x0002>\x0003;ÂÃò4úWÈ\x0018t	Ãó/ ^;Ðf#ï_×Ï:MS%cÅ¨ MRKÙJÙÜüÛ\x0010T`-+ªL¸\x0008"r
Tý¿DÁÒ<¡õú¨{ð\x001e¯¬µô x\x0013øT]¤R¡\x0008\x0011÷Ò¨WUÔÀ\x0008*\x0003¢\x0001\x0003"\x0011\x0001yÔµk·eYJ\x0011DS\x0000DUí Òp|Q»¢¹\x0014³F\x000eöT\x0019\x0008í»áJ¥\x0007\x000cp;£À¬¨¢ê§òõ\x001aB²~3EÇvv\x0018~f²Æe«¾\x0011\x0011aÛ\x0001ýëc2Ð\x0006ðx¹cèGLOÉÖ*Ï¥ÏûôÏ×ÞÑ¼òð~ÉY%ï¹H¹
	þCñù\x0012Ýk®øV1É'\x001eoýÇ	üÙ;ø´ÒÏ?K£5|î\x000fS-¿>tÎÏ3\x0019èñ÷\x0008Ö¨ú'\x0002æ¯Kó\x000f'­Øêºþ?ãRÐ\x0011QÖÕ·°Jò\x0011Y×ÕËðPûÌß\x0019çÞÚ¢+yzG9Ô\x0012°ïË¸®¥\x0008:\x0008\x0011=\x00010C\x0014\x0014køqîUN\x0013\x0010\x0002ÅPÁÀ.\x0019\x000c\x0010c@DÊê÷Ûm)÷i®RâÀ¢j[i±Ùa\x001aW§ú|\x0001Zq°\x0005@\x0015ùb\x0004ª\x0008må\x000eF}\x0000ÝÜ=Æx_×áä»ÇBò/¾Ñ\x001aù'\x001c\x0003$æÐ\x0016\x0000\x001càCG\x0019Ðªÿ#º#±Ì%Ä{mÏëQ\x0000!0>½\x0010»I\x0007!ª÷I¸6[u¼êIuEvÆ\x0018\x0011qÛr`1v\x0019¸"ÅÌÒ<×=K-¦È\x0003\x00073\x00130\x0011aff1ö\x0016
÷\x0013ÕÔ½x\x0013\x0007\x0011ÙÖU¼¾¾s.EÊíö\x0016DµäÌ5\x000b\x0000¤\x0014Í\x000e
Ö)%§GGÌ!0»X\x0015´ð±¨ "!;éDkÛÁ§uUXWs]?\x0000ðh\x0003\x0000{û\x000fbþà8\x000b^á\x0013ì¸a]íYëêè3ð¼\x0003 ãf PÊcÛ~?\x0003[\x001a»\x0016lHx\x0008È³ì|\x000fý\x000f-þOùYPPÿ\x001d*ÝWç~m]rw¬
\x000cEÌ°$¨µÎ'µCoµ?\x0000Ö0\x0000W'(9,¸cõ7\x000fxúqÓ8\x0004<ª|mÇÑÄä9Ôç,@\x0019\x001bTuúôªDCg\x0012\x0012\x0003'ÆÌëz/&Ì\x0001@K)T\x0004<ð\x00054% "\x001a§)¥\x0006¨R¤(\x0003j\x0011ËªæÀ µÂÛ&LÙX³ûîödh`ÃT\x0014'þ\x0018(£6\x0001Ñë\x0018¦Z5:ÕdZT\x000842BL\x0002\x0007ïO·gáVô#¤ª#\x0012au_!sü\x000f\x0013 zÁº~/ù6d-$òûhæ>@õg£¡z^»Ï{¥\x0019]Ø \x001b©\x000eª#J`mYQC\x0004bxÈGÆaOå_\x000f	\x000f\x000e\x001d\x0000ð4&Âs3ær"ó:rZÎäùöôè»ÓWã_þëy\x0010ÌAÉXÿ'\x000eGv:?ò'÷õ\x0003ny\x0012XçÛÍ[¨õ®zØ>Â\x001bÇñ\x001e!ã\x0011Fß!@0£C\x0014DffUjmp!õó\x001f6ÅÝÎí§~}<Æ\x0011!p\x0005pDSSBS0C×ZäZ6©­Ëïêýó¢ÞÂT\x00051\x0008Ì\x0014b\x0016Í§\x0010\x0015A\x0015\x000ci	Ê\x0005\x0015\x001aoÁ
j¸=X{þ@m\x001cç\x000b´\x000bmß>R
ÞyV3)z%o%¦Tcü®ÜeÇ\x0004À\x000e	À¸ÿ:A\x000c: Ýß¾õ¶~c)
\x0012Ã}Û\x0013\x0000_nÇh­@÷ãxã\x000f<<\x0007 ^Ll!xÿÀX¤\x0008½ÖÚ,«\x0018\x0011ª¡KÜ\x00101sà\x0018\x0000ÀÿgÞ6D$6 çyËÙã\x0010£OÙ¶©\x0007ÊÄDXJ© W"+Êa""g©÷^uà êNY¶m[´èi_-ñ\x0012ª\x0015qWrÄEmÛ·í¾,þ_\x0010-¶4"ny\x0015à¥@cú²é2óÄ)&\x000e!¥X±þ]¨{Ärô²Cc\x0010wµJ¥´7jÁ\x0010\x000bÎólfªh¦
Jæ°\x000f,òä½Óãâõ\x0019þ\x0003Tã¤r£\x0000k\x000cào~£öù¿®| â<®Z¥ôÈ\x001f\x000bÿgpKk\x0007\x001dª\[î\x0012\x000f
KC®ÛÎ
è¬ðüñéz&sy¶m\x001bíê(ã'SJ¦s¶V¤\x0001\x0000@u\x0005áña`Fïá?½ß5#!s DÑçÆæêì*¢bêßµ®k7¾\x0018\x0003ñå¾ìç?¨ìãv\x0019\x0001\x0002¡"H\x0007üº\x001ft¨{.79Îs:!¦{¿µýa×héz\x0015Ó¥\x0018#!ÊVÞïïðåËåÛ·o1\x0004\x0000¼
 ®\x00199 0cå\x0002Á\x0005\x0002!ª³\x0016	H¥\x0014d*E		Z37/ëÇ+~Z;«þ:,ÞÌÀ|n·¸ë;(zµ\x000c}\x00177\x0015/º\x0008\x0010w6\x0014! ¦ÌA¥ÚrÌÄÐßñ®ÆÍ»WIÃ`CË
\x0017H\x000fw¦¾\x0015·ºí	aAmòg²'~öQ\x0014Î\x0014Ù{\x0018Ì
Uµïòf\x000e²2¶JzÐãEê\x0010xqÌÓ)ctP~\x001bæyÎû3\x001a×·3\x00153òýÐöûýðSÌ½Ñ\x001f\x0012ý[\x000bÕ æ\x0008\x001djEà4O\x0002Ç£\x0017Jì\x000c*å)\x0000s|0NnãÃ áYÖD2tÚ\x000fãù¬c ç\x000eÁ§[\x001b5Eúì\x000côh¶9ÞÆN9ïãÁ\x001czá\x000c\x0019{\x000cºÜß\x0001c`â\x000bªáÝ9$½?97\x000eÃk¦`µRB¨\x0008ýÿÖu¤À\x0018b-~
\x0006ë}õ>ª\x001að¶qÇâT¯,û¢Ú*\x001aR\x0012ÕRJn\x001bk·"¶Aí´£"½ó¡pÌ9"\x0005&DÌ¹Tù¦¶ÜÎ\x001cª¾ÝnÚð9?ðØù¼Ùg\x0003ÿv(VV ?w"3ÃCçsHzÿÏÿÿÿ\x0019\x0013å±Snq¯D\x0018M­\x001cB¼­\x000b\x0006áXå
¶-7á'ôx\x0017¼Ø(ÊLÌ\J\x000bÔ\x0010k¯j]×y\x001då_\x0016·®\x0000\x0000·\x0005ØÏÏl¢¥d?ª©ú>hÛ¶m[.9ûóËÛV½z\x0016¸\x0013pô7¸\g"Ji!)\x0001@\x0008ÝÓõC\x0015F\x0011½RÛ:#cÐ_s¾u*\x0012¢A*Z¤H.!äg[ÇMè\x0004I'\x0001ýYIéèöa\x0011oûú'\x0008a#\x0006\x0014?1Ï>\x0013ÂîwVÑï÷U[%\x0015çå-­\x001dºM¾vË\x001b\x0011\x0005\x000eÄj¾®À\x001eXc«}ö?lZ¹Ò\x0016hf"¥Ã(+N|í½fO}½Éµm\x001b\x000c/Ò[ÝA¢©Ûý6\x0013&\x0013Yñ¥æEyu²¦ÇÓgã)\x0007)@ò3{ómÿªÌ¿´]ôËp\x0008HÅÁ\x0017\x0011)!Dwr\x001d®Ù\x0002G57ÇÐ\x0011j¢&Ï+²\x0007ØÏ\x0008%:¬ÂûÏþ\x0008¼Ë~B\x0010o\£ÚË\x0004Øcç\x00121"1b%ÍñÛ¾ýùÏ¾|s.\x001c\x0013"#-\x000b\x0010«\x0019N,`ÙDUKÙ\x0016\x0013¼I)\x0004ÜóùÅK\x000fªö\x0010ßÔ\x001b\x0019!%Ä? ]\x0019\x001eµñâ¤ÕÚ\x001f×6?9¤\x001dD¼\x0016÷ÐÙÀöÚ÷ËËK}(C9ÿá\x0018\x0003ââØ'¢\x000b\x001ek]\x000f*\x0013þ¾¡
ä}\x001d£¡]GtÉ\x001b¿ù)É;Rô5\x001a\x0000BdBD²Æ¶ÅþÿÆkëóíÌÑüé½ÀùZt·g8Ý\x0013¹Ïc\x0011aìÀ<?¿$Eìi]v,:\x001c\x0017§xyúybò¥û3ö?q\x0018<ç\x0000\x0010Å¿øcp\x0011£°\x001ed\x0013Ë¼y,\x001c!"Û\x0011\x000bþ\x0007d\x0008"Pãs9HÓ¼þlùìðÍÎÔ\x001c\x0000îëêÃ\x000bçÐ?}\x001câ%Âoß¾­ëjµª\x001cØD\x00131\x0000\x0010ó\x0018 *ÓnøXK\x0002µ]"ED	xo2×A×` óôý´\x0017¡:c\x001cç\x0007JÞÇè\x0002KnÛâ*\x000eÌÁá\x000eî\x000f\=
D÷Âú£ÜðÈµP¥\x000f{\x0007<\x0016\x0013ÏÐ
gæ¤C\x0015?\x0010ë?!\x001bÉÇNÍJ\x0011Bå\x0010|\x0010ÕÌ[&!Æ\x0010¸¼,\x0013õÆºl¿\x0008G¹tÄK)½Þ)1FGU"\x0018\x0000ä"BR8Æ°mÇ%1@,ëæ¹¶Ã|³\x0014\x000f©¨Goà%Lßä\ÎÌ\x0001[Ì!¥É±þÄ\x001c\B\x0013\x0011m%{.á;\x0017\x00081âzßúm®\x0003Þkm\x0015ÍruÝñ÷E¶¢48Ù8\x000bú?s|fc;ÎñO2Ôd\x00032\x00018;Æû°vòÇ@È©ÃB\x001d^\x0015\x001cß\x0008~-ª\x0006B
\x0002¡æ¸s³Yó+ò`\x001dëómq\x0000\x0012\x0011Ì!©RÎÅ!\x0013 T\x0001^\x001c\x0002T-D²>rÎÜÜèÌÄ÷E¯É\x0000\x0000#ªÕ\x0004F\x0003´g\x0011Z\x0011,ìú¢Txþp¦?Ì\x0013\x0005Ð\x0018\x001dàa;\x0016\x0008	UÁÌ\x001c­Î\Ëô@\x0008 *U\x0016Y³¨!(©©'N\x0004@¢ÚQ@\x0007(×Ø¡:á\x000cÊ$\x001c\x001eçUý+n\x0017§ª'sr$µq%<\x0001\x0000\x001aÑ4_Öõ\x000e¨1Òëå×oßB¤·ß_Ó<\x001a\x0011 gÄ@J)ZÔ~É\x0005´¨\x000bïK±"ÚpóÒ´Þô\x0000\x0011Ù	2J÷ê7þ\x0018w ©¶\x0008\x0018b=ðõ\x001c¬f8ëÖ)Q¥H\x0016S@C\x001eI\x0015Û 
çª>ÇëG\x0001\x0007y¨\x0013ÿv1hfY}oTdö§X?'\x001e\x0013BìUúCðJÔ|« ×\x000e\x0005"\x0000'¨>Á~¬[O"»³ÏóÑÓ¦ÿ¼æ\x001f\x0014#¾s}æ¬ó9\x001eÍ¹ùãß>\x0011Z>\x000b\x0011÷\x001b¡Ë\x0011¬¢\x0010þCâT;HFÿOéÿc+ùª\x0007åÏ;¢Ï¿z\x000c°Yª©e\x001aòÂñ,!\x001ceeìUX:ïx|ö@mÜEß\x0006
â~\x000cÜ¿÷_ä0tT\x00037rÎ.ç+*(X3%Q[WlZ)ê¼9S\x0007«uy#\x0011ÐHÍ\x0002R`z_\x0016æ\x0010CÖ\x0005¬V÷¦)ú+ME\x0003DjJÔçÃ\x0000\x001cçí¡õ`2Æx¹\¾|û:MS	\x0000rÞ\x0010ñv»¿½½ÞnwÇ«3\x0000ìh+ß^ü\x000f
BÏqù\x000fC{6àýçQèåì3§	@ÿ7÷uë\x000eó\x001dPËè\x0001·z<mj\x0006\x0007òkQ-ªLè¨Ì%o%g\x000eA¶\[ÛÍP\x0011qÛ\x0016gÖ"RÞ67·F"Û¶å!àÞ¶­`\x001bü×\x001bIÄ8\x0002Hq®\x0013\x0003¦\x0017\x000e\x001cCe\x0011¸
PÁ\x0013øzådf¶æ­2Ï³\x0007=f*[\x0011)·"fö±¢P3EÚ;>\x0006Ðâû&'à­òö\x0001öðèîö|Ú<\x00103O\x0019\x0003Çñ÷;TàÀ¯;¡\x0002=Ååòxl{íÛÀ@ªã*wÕ\x000cö\x001b¨Ë\x000e·\x00180\x0004iÕ{è2E\x000fk)çªâ
àçöú"ù³¦æ\x0001çÍ>Þ6\x0000H)¹ÿ²ö\x0019J\x0013TóYç\x0001+\x0011ÆHÓbª\x0013\x0011h)¹
\x0006a\x000e÷û-¥4M)è\x0019æº®"B/efÎ3g\x000eS9çms51¿ÿ\x000fý\x0008Ë)i~ò±àa¦ï·Ûý~7À±\x0014§i)ÅÈ)E5ü]ê\x001cUuö\x0005K1tÌ\x0010\x0003	òÔ¨îðàÏ\x001c \x0019^BÄ\x0010«s¡»ºxÀ0ÛÕßAïö\x0001\x0000-ËòõëË4Mï··¿þõ¯ÿãoÿî*@F\x0018ct¿J\x0001\x0004d\x0001#\x00030Á"ªÅDM2ª+±´¶¯4ðXÝÞ:Ø½
2\x001d\x0018f?ÞøGÞËÈ±mQy3Ê×\x0016)®ã:wR»íêØÙzÜq\x00038é\x0000\x001cÉÊG#ú'Ï±â>þ«Q© \x001d;VÔN:<'UsÞÇAÕ¬iÿz×Îm
N\¢?sAõN§?áPû\x0019øßqÌ?\x0015U=M\x0000Nêó®ïÓ\?ÕH\x0007àÜÈ\x000f\x0000þ\x0004à¬2m4\x0006vGe³°DÏn_×û¨¶×aoc\x0013EEkô\x0007§³gñO\x000fµý|\x0002ðPDsa±"eW\x0018ûpô\x0017þ%_ãã÷\x0004ÀlYn¾2h-\x0007«ªT<½Iqä$1yéÍe\x0011\x000c½\x0007\x0000\x0015j%ª\x000c\x0018\x0002Î¯\x0013 \x0010#ýÛÿòoý¶× (\x0004&bò4\x0001\x0018\x000b\x001c¹ìÉ*3g)1¥ëåòíÛ¯À\x001c­©8lÛöþööû?~ûûßÿv»ÝC\x0008fj¨n·¬½ù@C\x001d\x0001ÁºNÿ\x000eÔÃ{ýY\\ûõPÝÿIÏ¥ñ\x0008ð:ª!ÄØ«P÷û\x001ac\x00081\x0006fU\x0011)ª\x0012cægiÇ-äýö®¢\x0013N!°¨ªh¥n©\x00001
Ô÷\x00089Á¶s\x0008AEÕ7¼m\x0019Î£
R¢õ6\x0002\x0013±*Ç\x0018=i£È\x001dÇß \x0008.AäU\x0014²Åè\x001eÕèZ=jÙÔ\x0018Ñ[
ªÕÓà#m109P¤¿c¾o­ëj\x0000`Zyëö9+õ­èÿK8j¿\x000f\\x0019[K­tgGHÒÏ~ïA\x000eR²%Þ\x001dB`æ¾qVjGW{ý g\x0008Ìh.8;_æ\x0014\x0013A&{ow]×mÛ\x001cÌCä)'Å\x0018»n\x000b\x0007B2)%\x0004t@BÎ\x0019ª\x0000T\x0011Ù6 \LEÌ\x0014Ð\x0003¥\x0014R¥P\x0019å¼z£\x000c®/îS¡\x000e\x000e\x0001'µÄD×\x0018B.EEt\x001eb\å~»-Ë³\x000e(ÆÃ7T­ô_¿^¯/)\x0005\x0011º\x000fL\x0014«7¢
8MÓ·oß¾|}ñ;\x0006[z¹Æy¾¸³¬SwÖu½ßï÷Û³\x0000Þÿ`\x00148v·cì8\x000fPC Rò§@4v~ð,¡õ\x0005È\x0017Õý<Þó¿ùòåR\x0012ßo¿ÿöö.¥\x0014S"Z¶5ÄHÀH¸eEBqí 5$\x000cHHF¦h
ÌÐv\x0002td:b`@Âó!\x0016©ý\x001c£A~GO¿\x001fG³¶ýåÜÐ_\x0015Z`\x0000.WË(ÐX.L;\x0005QóÏãÅÀ\x0014Tõi¤Ø^½\x0003ÕÁ_\x001f ,±jÀ¨tÔÖØò>\x000b
\x000fäø¦\x0003\x0000E³\x0008\x00101¯ÒUê4Cwb\x0008kÎPW#we<Ï¸\x00168ËaÆùyæ(<\x001e\x000fãð\x0014}á&ñ\x001fò\x001eèöâ!´>¬çÕÅùSîß?ôPÑ|\x0014?8£õ~öü\x000fûÃØâóî(\x001fImD\x0014Î8\x001eNfÅj	VãHòá×*BK#\x0014m¼ÎÃ9?±?Òsñ\x0003Í'NÏ\x0004OÑ #ÑYk\x0011\Áx\x0010gûð\x0000º¢Ñóî\x0007a×cáb-^KòÛé.ÜU\x0005±Ô5­ËØùyz\x0013À\x0014\x0008Þo·À8i\x0002H·Û»ïã8Ï\x0017l0õ¾
ï»	{á&$\x0000û5¯ë^YÖ|½¾|ûömºÌÓt\x0011°R¼Qkªæé2Ïó<\x001b\x0002ðoeÝ\x0000@\x0014uçX3>çvBè14G=Mü~Ô]lº½|èu\x0000DÕÙ\x000e\x0004òògÎe¾¾øìÊb)¥¼m´±\x001d°\x001dû\x0005\x0006d11)N\x0012ÓûºÌÀ@8y*!Zú\x001fÙ¶­
Ø#fæ\x0014³þ4©ICö;\x0008\x0008ÌÄ<1\x0011ÆPDC\x000c\x001eôÙa\x0004X1\x001cy©Æ[ª\x0002Ë²©\x0016U£!	+õñ Q0$\x0007F;\x0005\x0002\x0000D%×2ìÎkDêNHuzë	ôÇ·?ú±*F¤?ª³||ñ\x000eJ)ÃZÔ¥\x001e'Áójî¸\x0012ìÕMü\x0014\x0007`Ö.yéíTOý«¢ÔI¦«%3\x0002\x001a(9?\x000féÐ'\x0011Q#l°®@\x000cÓ4]æ9DÞ¶
©nñ¾ßÎsç\x0004\x000fAC@\x0014+¢j%\x0008@\x001cÒ<§R²©JQ3\x0010GËÉ²,¹d×ðá\x0001jï)E\x000b­\x0014\x00008PB\x0006:l\x0003:\x0018q\x001c(3"\x0012Ù\x0000^®/
È¤Ó\x0014·8\x0010\x0011×F®Quón413~ùú%ÅDdî?2Î\x0001\x0004ÌCÙ\x00118\x0010\x001a¬÷Û¯/ÌP®ëR\x0002TbvñÜ\x0018C)ºÝ%R¤\x000b­´f"\x000fÕ\x0005KjÄ'¼yÞèü&-ÖÄh\x00109"eS\x0002¢X\x001b*ôôÃ\x0017Ñ» ö\x0006A\x0001tìM×T\x0007×	©\x000c\x0008\x000c@#`d 
\x0001ì\x001e88@å2aß\x0014ÉÀª$\x000eíÁô¨B[½¢\x0013ði\x0002p\x000cp{Åñ»Þ\x001dmûÜo4ÍûçÓQbu\x000c\x0006wøÐpÍ£êY`zÜ¤\x0011èrýñ»"\x0000\x0006\x0003\x0010\x00030@
»ýÈAMåäOÖ
\x001aìª\x0001\x0018@»l1Ç¢Éxm'Ýa¥;nø
Ôcåx\x001c0¾k\x0007?çc\x0008'ðkç><ýþ#ýÈµýáïÇïá8\x0001üD]ù;ÉL?ÅDéÙ1ÀÓõ;Å¬O	Ï+âæáñYâñÌ¨«\x000bÑ\x000eçD$FøP,\x001bZøì:ÏÆð´ópò2'8=+ÉîÿLTÅ\x0008
Í\x001dúà\x0011éNÃy>suÈ9fÌ\x0001±2è\x001c\x001e\x0002fb*¢\x0004\x0014\x000bÿÄ	*y\x000b\x001cPÌX\x001b­õ!º\x0019%·ï\x0012\x0003P´bÅ¤ .K\x0005]è¥é\x0018â\x001b7\x000cî|ID\x0010cdbu!²Ö`ÃjêQ¢Ç\x0003l¦z5zÊª*\x001c.\x0014\x0011\x0002Ý·»\x001e£§\x000b\x0019ÄKüËýüõÿ\x001f\x000fÅmÛÜÒÄCY\x0000èðoB
10VQ£\x0018Â}Y¼ü,¥PKrÎ1F×Y\x0000\x0000DfbQ)¹LÓ$
NBÖgNE×{\x000cê|)%5[îwÔõ6¡í\\x0018n·÷\x0014SL)Æ¸,÷Î»=V\v\x001b\2\x0011û¸\x0014Ss\x0008·³MMASJ¢¢Ê*³ÊM¹ßµo×Zzè<ò;ýåíLýÅ jUCºL>\x0001bÁ\x000eDÃ'ºµÖ¥â×Y¬hØ"(¸ËU¬oÅOÓ´\x0007"sÜ¶­Ñ\x001bÄ+Êª\x0007'¹|®q,±«L<P&\x000e\x0006\x0010ôÀñ£ç¸\x000f¯ê'þðù/úc¬í\x0018üu\x0000Fd'¾0\x0011²þ¾\x0012ÑÙù\x0003s\x0008ì<Ô±\x000bÑû×'«6YF\x0005Gÿc\x001b\x0007àãè?`\x0002hHÆ@ÇbªW+D¨·Bä\ÖR,pd\x000e1\x0006"¾\/Ýµ	ë;ôç/¿\x0014G\x0002bf\x0001(tÞRy`YD©HFC6AÄmÛr^j¾!aÓø\x0018ÆÄL\x001cÈÈ\x0016ÿqÖµ¬K\x0006\x0010Âº®DÀaRÍDa¦y¾\x001eìó<oÛ¶,k²mÙ'9":O¦óðc%ã\x001b.ºæ\x0008 W\x0010\x0000\x0019rÎH+\x000f ®÷Êà2\x000e^j
@ ª#¤d{\x0007<´w/­f\x0001"b
L¼mR\x0004
EMÙúô3\x000füë¼Qó®4fÙÚ\x001d'\x0010{©FAG3îzû\x0014pàÒ\x000cæt£Ø\x001e\x0004\x0018\x0010oÌ'1Ðþ(òC\x000eg@?:ßñ+\x000fñ\x0015\x000e8\x000cîF÷gAª~bmñ\x0013|\x001cÃ\x001fÂrÐ\x0000íÇ	ÀÀÔ;m\\x0019}¨j·8ãÀà¤­ù³Û>6Öß\x0003|²\x001e?`Ð\x0007Ái%þ¬@s(\x0000í£û½*\x0015=½/z^ÉÁ0â\x0000½_$\x0006ÊóÊ+Û3»\x0000Xy®5W¤ácûèJàð\x00047ópæOHl\x001f×êþó§ Rã{ñ\x0010>Rj\x0015\x0012\x0002\x0000Ï.÷{Ç¡+»¿G ¥b\x0004Å¬©óH	!X\x000bã?Ó%\x0003h\x0006vÄÂ) ·ÍZ'\x0008\x0015\x0000JÎ%çûý\x000e \x001c8¥\x00148¼¾\x0019\x0007¦)ÅR\x001a\x0003$$qApÕ½»Ò\x0005-L\x0011¸\x000bàÛm¡\x0018©m\x000br\x0004ÛåGë\x00030SÒ×_\x0011\x0015]\x0004T¸x{¿\x0011±³OÁ)Íß¶ä"*4]æ³7F®×É§w®*$¦\x0016CÀ\x0018½\x001eÃ\x0014D´LD\x0000ÁÌJ\x000f\x0017¦E©]uÍ
àèååÅ[\x0019\x0000Rbæ¼m\x0000À%\x0010UV­­\x0016ëv\\x0015WÈÌàÃ\x000bÉDH¼ãçÄ2d\x0015\x00175Ñûm­
µð¾¯Å­òG.Xë
Õ7YL\x001aYäë×¯=\x0001À&×(fîüÚC\x0004·&\x0003mí×/"Z©¦nNà1[à¤Uz\x001a/Ó\x001d|½¢êM+UÅm]×ÕÑ\x00151E¯×èÑ5ãAA\x0002»KQö\x0003\x0000×|Ðe\x000788ó}æ\x0018£ÿ±ú5kÏ³À]\x000e\x0019ýðoÏ^æ¿ì½8ø^\x0004ßþ¶bøÑ1÷ã?©z¯ÉvåÇ?>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article7.752941ad.png](https://www.dossierfacile.fr/img/blog-article7.752941ad.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Íz½áh°¹½µ½³ù«©2E	:¡´7+Æ¿øÕ¿\x0010%i\x001c7ÝÁ0Ë\x0006Y6ÐJY×noo(rÖZï\x001bkÙû8ë¶qUgèÀ"$]ÉÂ^\x0010©ã3k\x0002+è\^\x001cìí&i/¬*qlâ8¶:$XQfz\x0002\x0014b\x0019´Ñ^\x0010H£ÒB\x001e<v&bæ¼¬tÕX$1Zçe­µ
¾5Q_\x0012)$\x000c,½½ý´7\x0010 ·o-fùÇ\x001f}úé§Xë7w¶\x0007½ÞÖæÖb±\x0010\x0011ë9/k\x0000ØÞÛïUuUUµõ\x0017ãÉýÏ\x001eXg³8ýê×¾|ïÞ½ªµ;û\x0007û\x001e=òÎ7M\x0013EIY6\x0002\x001eA
\x0007£N
ªmë&äµ)\x001d\x0014FÁ\\x0015VÖ¢\x0008\x0011µËªzúäb{ôdk´\x0019EV&2jcÐ;ÓÔM»»»µuÓÉ¼®-E\x0000<5Ü¹`R*2\x00113;ç¼÷Âh[ \x0005½Þ`0Ø(òêþýÏ~ôã\x001f/\x0016\x000b\x0010ØÝ\x001fTeU\x0016õåÅx:·-Ü¹»¿½µ{~vyÿÓÏ£0Fö<ÍHQ¤FÇ»»û±é\x0004Þ³ÙbïÆÙÙÙ§~úôéÓÙb¾\x001aáo¾ýVo0|vòüÁDæîëolíì=?»8==
#¼×ë
\x0006\x0003øyP°&/'\x0000\x0011ØªègI¬	æÿù_ÿW;}%.M4Û*È×õ\x0012bÜ´VÚh¥4b XUíÅà\x000f½<â_E\x0013`\x001e®içðv5½E^:ÓáÕ}ÛÐ,[×ukÝd2Kú¼{phádñØ³ßÞTÓÜ_\^8ã¸(ËÉ(6Q]×Íõ+\x0011\x0001Dfn­uÂÃ4³¶i\x001c\x001fÜ¸ùå÷ÞøÃ?ü§óùüÙÓ§q\x001c\x001bcÞxãáp\x0018*}Ï¬´\x001eÄ1,\x001dñÐ3Ó«¹\x0007³Ùôòrê¼ûÊÞó­ýðGïÿðÃÏ\x0007D)\x001dâÖÊµ-4
´\x00027·\x0013\x0000\x0018\x000eÛ;;o¼ñÆþþÎöæ\x0010\x0014úñÅÙ£'ÏNÏ.òÊZ!\x0006ÅQº\x001fk@§
Æ	Ý<Ú¿yc¯nòÖÖá
ü4ÆÈú
+¸ò¥\x000bÂ1­:)ÙòIá®ÀUAs­øøb,äì#ìÊAU)®EGà¼ojo\x001b&\x0010kA<² ¢Qúe0\x001e¯¿OB$­=)Òz\x0019¥\x0014>~ÀZ\x0008B
,Çv÷¡)lÎ@«0\x000e\x0016 ^Â<\x0002ÌÁ\x001f0\x0000 \x0002à*¡\x0017÷ú¹62¿À¤àê²¯=¿»AkZk*L­õ#\x001cÚ¸àÃ/`\x0003Dä¹\x000bN§,H?åöÊGH\\x0004\x0000^û"l×!üeõqÖÞ¡\x0008xk\x001bæVi\x0005\x0008@Ô45\x00185ÚÞÚ\x001e
ú{{ãg÷Òþ¿þµ­~ÄU±=\x001a´u^ÛúÙÉÉýOî?z4/[4·þÑ³cpà\x0011´(\x0002åÊº>Ìó
H-6\x0002\x0001ºsæ%¯\x000eb?\Iï\x001d¨+ú¹1fõ666zY/6Q¤
"÷@ \x0000aééB«£¿º¼|}y|aµ|yâPG§î®uÉ¼x
2¼Z3YD-\x0011\x0005µ\x0006\x0013!2\x0002z\x0010ô¾µmÛ\x000eûýÅbÁÖþBUUÙ \x0003¥æóùÆæNóÅtko¿nüÎîá¾òõ²vÖ\x000bi3s>/²^O+\x0017E$ÎyïëÖ¶Þ8\x0018\x000cÒ8\x0006Â¢(¢¦©¬uFGAYÅ Ì^öpÀ;ï§IÛ¶½Á=+­Ñ`0ÜÌgE]*¯²¨×ëõ\x0005)Ïó²¬\x0000\x0001­µZë¶m=ÒÚ\x0018Ý4mÓ4³Ùt8\x001cFD|ÀSê\x001a\x0013 /òý½½í­­ªªB óã'Oþð_þËËóqÓ4Y½þúk[ÛÉÄDiâ­\x000bTi\x0006Ù6:ø\x0005ÇqL\x0018á³Ï>ûø£\x001d\x001fÿú¯ýÚ×¾òÕí\x001d\x0000þü³Ï²4UD¤½~\x0008"¢^/ÓZ\x0018&ï¬
V»\x0000q\x001c'I\x0002ÀYÌ&\x0001¨\x0012Îf\x0017\x0017\x0017{{{q\x001c³³ý~¿×ïO&ógÏoÜ¸qçö"/>=~åäòÞ{öÒ×¶­RAà\x000fU]ÇãOïßôàd´¬D\x0012Ç'Çu]_/½ÃÃÁ`pòüd±X("k]YU³ÙìðÆ(2I\x0010©ªª\x0002Ã¬ßëåEþðÑÃÇ\x001f_^^ÑIô{½$M\x0000à\x000f?8?\x001fo_þÚWïÜ¹£HM§S"ê÷ûý^/IÓ.HëçZi^Àmb²b6ùãßùÇgÇOÞ{ýÖ³Ï?{ýî­Ù8·¾U ÞY2:ÒFi"­õJ\x001b²:òv4\x0002\x0011Æëè--üB]òãX@:ÁaXf»¬öeÀH(8l^Ä\x000bkTÁ3É²¼*'eÙ\x001fmnnï÷{¬?L[V³§ÇÏn\x001eÝÎz½ç\x0017qìÒq\x001cÃ\x0002®4È\x0010"x@\x000cûªÊÁÃ`c£\x001d«ªìo\x000cí7~¥7\x0004oñäÒÚÚZwûÎM¥\x0011I\x0000¹i*f;ÜÜ¨m\x000b\x001dñ\x0015ç°@\x0011Ð±¹u÷îhsöäñ³ï}ÿÏ?ùðãÛ·\x000eo|ôÑGE7U\x001dn^ÚÐ\x001aUõ´vv¶÷\x000e\x000foß:ÚÛßÙÞ\x001c)ô£Áóç#\x0006:½\x001cg½A3è^/\x0016ï£4\x0003tÎUÙ%»Ú»z>dY\x000cËF\x0003¾tÇ_~¬
\x0017\x0001/\x001f¿ø×µV+\x0015kay\x001f\x0003ÝxÙj\x000cÜã\x0002
\x0008I\x0008Ø¹Æº&²$ÎyÛzÛzB×´®iÅ³QÚ	¿ZïI½HN\x000f8 Ö\x0011Ö:VÑjî\x0004p \x0010@\x0003â \x0014b\x0005aÉÞ%\&1¬)Ó\x0005 øÇ\x0000À\x0014ã»×\}½>\x0011¯]Ú5\x000e\x0019ÒÕ\x0016E\x0000¯ÚêÖà¶àrÂ\x00013Y»!\x00100/Ë:m\x0015½ÖZ¯s»\x0008\x0015ÏãK\x000fÒuåH¸wp\x0005\x0014Áõu³cs§³AY6Ñ Ñ&p8 kßx\x0000\x0003à;Å½xçCSÏ)$e"\x0000hëÆ±{|ryòèÙåÅxccãh{£M.2]äÓñb×Õx:/\x0006Lì'ùüô¬\x0018ld\x001aÄ +Æ¶gi^\x0001Ò5úóú(>\x0010 [Û Êr¹\x0008À\x001ekMý~c4ØÜ\x0018dYO\x0013\x0019\x001d:\x0002a|.IÍ«Ã¨Î
\x0019\x0000Ôò\x0000Ðéc¯¿\x0007|ùß0\x0019\x0003#¹PKì=\x001cGpX\x000c»\x0010dÀÂÌ¤$ä#BDßQ\x001a\x0019\x0000¬µÞ:g]${{{ï¼ùÖ`°¦©\x000e-)/qN\x0019(½µ·I:ÞÙÜîmâ4¹Í\x000e\x000eîÞÞ\x0003¶m1³,ÓÂÜ\x0007æU\x001e\x0002\x0005Ù{\x0011\x001f'ÆZc­uN¬kÁ\x0001¢B¼ÖS¤<{ïÜl6c\x001f²\x0008¬\x0006H$\x000c³_×Ê9ïjÙ[/aûtÎ¹®m
Z\x0008\x0013©Ðøð¾UÁÃÔ\Û\x001fÓ$\x0019\x000eJ©ñd¢þè£¾ûÝï~ïÛß>ºuïÎíÛ\x001b\x001b£²*\x001f?}âÛT[¾µÞ{Ç\x001e\x0014)c\x0018ìrîwéßÚ\x001aÛ¶ÏNNvwwæùâ[ßúÖÓ§Oó¢xýõ{[£Ñ"_D&J81Ñ¼ÈWå4\x0000À:«<\x0007ÍW¡Åf1F\x0001\x0000\x0011%i¢¾\x0018OOÏ.zÃÁh0,"I{½^ïälî¦EU×;A¯ßÃ+\x001aÒÒ)ÑyÇ5³0{&"ï½ÖJkí;~v¼X,NÝ\x001cÊÄ¹µ¶(Ú4ÅÁ` ´:??_ävØWJ«4Ýg]jR}ðÎ)­²úì³Ï<y¼X\x0014M#©^AÝtvv¶X,\x000eöwßýÒÞxëÍ8¦!EY¥IfÙêîü\x001bg0\x0012 !»¾ÿßþoþoïÞ=z|ÿã×oß:?~f\x0014\x00100¢(E&Dg)¥Ú%ÀN|Íá\x000b"ç\x0010©kg-{F1J©ÀxêÆ HP?.\x000fFÝfJØÁ­I©8VDV+cF£ÍÉd~üü¹IúÍ½­­Ýí­üùÅ\x0010...÷÷oÄqÌ\x001ebC\x0006\x0019Zá\x0008=\x0002°\x000f¨kZå}¦Éhcvz2Ï\x0017i?\x001b\x000e(Q¯¢O>þ$_,²4cÏÞùª*óq\x001cWmÃ\x000cD¯ÞîEØ\x0003CO¤ÍÝ{·]Õlÿò/;ç\x001e}þÀVåéóçha´LæIÖ\x001b\x000ei¦QjøðàèÆ­Û[Ã¾Èµmcë8·w·¶F£¼lÙ\x0003Î¨.Ê^/\x0001tóE\x001e'jsÔÛ\x0018õòb¼d,Û^²¶¯üÄ\x00078\x001f@ö.\x0001$$øµÏ\x0018¬Þ1¸qðÒ	ãÄÕ+¡uh©¨\x0003ÂAB\x0000	"7×4
À:ÛVmk\x000cõµ\x001dcP~êç\x0014\x0012\x0011M¤\x0014\x0001F\x0000"\x000eY\x0003	^q¯cxË­]¦@\x0000ó@¤nV¡"ë\x0013¾Îø\x0002ï¥µï¯Ú¯ñføêøj»0"`	9\x0014WaÂ ={\x0006\x0011^¾uYî¥]ÇB)ï8Ü,"\x0013¢Åçó¹³á>òOhüQ\x0014.)^ëo= Ü}ï@È*s\x0000WÔrJëºöÖg\x0002\x0002v\x001aÕ>ýÄeQUú½\x001f\x001dí¤ZìnölSè\x0008EÓÎáÑlðøäòùýÏ/¦¹ñbEY6æ5#ÑÐ®Ý\x0016\x0001P
\x0003ó4|'üá\x0007\x0000l\x001d;KÀìÜÖ¨ßÏÒ$2\x0006M\x0008Kgc\x0014\x0000`Â%í448½x\x0006\x0016&¹·-ÇÕuTfy\x001ee\x0007\x0010|¦ð\x0004 µ^\x0019x	·ñ**¦ë7\x0001HXE½gB\x0002ÍÊw?X\x001e+e×^\x000e\x0006÷Þ}ûßù­¿¼{x°··#â¥mÓ$ºÏ§ÓéÞÞÒ;íÑÎ³'ONN÷»ßýÞ÷X\x0014Åí[·ÎÏÏ¦yýõ×ËrHQdvw"§"R\x0016Ô®6Ú\x0018dÖ.G\x0014{ð\x001e\x0004­\x000bRZ\x0017eYå6{ï³6I²ªÊ²R\x0001²¬¬u\x000cä½\x000b4M\x0003\x0014EQ¨\x001cV
	ã8N \x00014ÍD¸µìc\x0017\x0002Åööözýþó\x001fÿøÇñøÓO?EÄ¯}ã\x001bN\x0002Òppxp9¹\x000cÆ\x000b§çg(°½½MA\x001e¥µ	\x001c^­M¬
\x00008k\x0007þîînðÏ=9;\x0015Ï§§ÏÛ¶
A-D ¨eè¬ÍâüüÔÚ6ãá`\x0018Èy'Â@Ä"MÓXk]¤9H5³?=;ë\x000fzþ Í2¥µã4\x0001\x0016xüèq^\x0016UU]yD­O:\x0016'.d3\x0007O)EDU]=zü¨È\x000b\x0000xãÍ»Ï\x001fCèS\x0003°¦i\x0014Áæhs2ÌfÓãØÖMÖK÷÷÷_{íµ(2D*Ô1I4M3¾¼<>>ùáû?\x000c\x0007¨,5èN§\x0000çå7¿ùßøæ7\x0006ýAÙÔÁH\x0005 îº3ËÏQÊ\x0010t:
\x0012PÀ9Kc°ÕÿãÿüÜK´\x001d\x001fmlTÓ©&DqB¤¢("\x0014¥Ñ\x0018£\x0014­¬z%\x001c\x0007×Z\x0012ëø'tgý+6Z±våIZYÛ!ð\x0001õò~	8/·¢,­w¨i½­kó²TIÔ¶îãO>Îú[÷^{
îÞº;üP]\\\x0018mH\x0001³ï÷3Ø\x0007ÖYÇÆèíÍÑÅ¢´ÌÌÂ®WÅæ /"J+ ìo\x000c/'7ß~#MðÑç\x000fâØÌçÓù|zëÖÑÇ<QÆD\x0016ñ\x0017g:J®¯Þ\x0001Â´×¯ëº­`D\x00025ÔEïíï÷®±Û\x001bÃ½ÝÑæè;ßþÎýû÷o\x001dÝ\x001c\x000c6DÄ9×4M¤UêáF¶»·$i¯\x0017i£"â§m¥\x0008¼·m{+Æ¨ºÌºÞ¼}x|útggëü¢1F]^{ïúÙÔ\x0013\x0008ÝjN\x0010:ÚÒ4MP$\x0002
©\x0014 \x001e@±\x0000±¬-²«®\x0007ªk½B\x0000`\x0016¥ðá!ÝN,ÂxmÀ¬ë¡^±UV\x00111wbë¦*
×¶mÛÖumÛÖ·Ö6­8\x000f%°ÝÂý\x0010Ö¤_õÊ\x0018\x0004\x0005\x0011)ï\K@Â(¤\x00085\x0006Te-{(ÐbÂÅàðAÂ·Q±µQ2;BR¶©Úª\x0008ÞÀkcãå\x000fvÕêæåÕGWß¿p½ôÖ\x0015@\x0014Nïì]ppN¯a·[a¨J\x0000\x0010¥Ë¢8ÒÌP×ít:¯«\x0006põ§»>\x001b\x00086FøÓ°"Ñ\ç\x0014 «\x0011\x0001\x0008  ÀÄ­%ÑË 	;gÛºqm\x000b,$,bíÆöþyû¤`÷d6¥Ìô\x0013=\x001a
^;zk»ß\<þøøìÓÏæMvL\x000f¦)[;Ë\x000bë=3\x0008\x0000
¼Ð+C\x0000m1!,h3\x0015\x00008ßb×Ø\x0011çZ\x0002NèÆÁÞ°Æ\x0011*hÑB\x0013E\x0006<2w\x000b!ÊÒW+ qì\x0005éú8\x000f÷¯2\x00024³\x0010B\x001eY Ç®9Î¹NS-«VálM\x0004\x0002å[ÙX"(¶
^ËB¨µ"áº®ªÅ\x0014\Cìm5«òqOvÞ!±"b¢ÈZ\x000f\x001bãA¦¤£ª±ßúþ÷þè\x000fÿð»ßþ3\x0004 áá`´XZ\x0011MÆã^¿\x000f\x0000y2Z×\x001c\x001e\x001c\x0002ÀÓ§OuF_Iµ¦+²HÈÊf\x000f­o\x0019)H'ãñÑÍÛ«Õ ì²ÐYux\x0011Q&6Ú\x0004¿Úàù$÷\x000e\x0019$©ëZ)­µ*Ëj	\x0015p \x0004\x0019\x001d5Meé÷zYîîîþðý÷ÿÕ\x001fÿñG\x001f¼1Ü¼{÷õí4Í\x0000 ËRfyvr,â£(*ò|±X4M
úUÓDiÚÚ\x0016\x0008Éèp\x0018h½\x0013\x0011PäÌóüðèèr|yóà\x0006\x0012þøÇ?vNf³º}u\x0000\x0000\x0000IDATÉp8ÜÞÞÚ\x0018\x000cG£(Mv{½4_Dq\V¥"Õë\x000fE<²c\x001bÒ7¥i\x001aag-{öE]%I¢\x0016ù|>¾Ü¼i{Y\x0016Åi\x0014\x0019\x0013Öúñd2«\x001dj\x0011D|!Ï\x0003LKÇl:«ëúÖ­[GGGmÛ\x0006q8Deý`ÜJÓÙ4ãélÊÂ
TÛÂ¯ýú/¾ýÎ;!ÎÙ¶­ó\×õ³ç³él:',Mó¢@¤4KËºÎó2ôææÖ¯ýú_:<8\x0000\x0000ï}/ë\x0005NmãU¶mÛ¢üyÄØË# H\x0000Ù0-ÿùßÿm®\x0017½Íñ¼³ÞS8Ç!tÊg¥C¢9"ÂOìû^[,^\v»,1ér:\x0014\x0000baÔÆP§\x0019\x0013g=(m´VÎIc[\x000f¢bvmÛ6Î2B\x000bÞµ6JãÖÊü£Ñæî`cøðéIöòªlÛV+\x0008K½\x0005k@å½öì#LâX×
V\x0016\x0019|k#cbm¼sZ)Pº¬«8/.Ov¶\x0007IhcF\x001b\x001bÎûù|\x0011ÇqÖïGQäÏçÛñj¥\x000f@D?¾\\x0019»û\x0012Â`«¼Ö¹¶uÖí\x001fì\x0017yqëÖ­Ñh$"EY,¦³¶¶;[Û£wn\x001d\x001eìi­\x0010Å	+Öyf§b£½÷\x001a\x0001´ÖÔ4Õ£Ã\x0007\x000f>±®"-"÷^»óìéñµ+?)\x0001\x0004x^Ú4McÛÖY\x0014\x0000M+ë6F!\x000eY;Ý.×Ée\x0010=3\õ\x001d_%e\x0011Ätµ\x0013ÿO%Ùj\x0014Íf3¥1¦m[k]x©PÊ\x0015òS_M<\x00082°÷Îù"A\x0012\x0015Ê\x0001+h´B|)¯\x0011W9D]îgv\x00168bë1 ®mªÖ61ËôE5åUv÷K?X\x0017w^&/~ëípö¼BÂ\x0002¿Wñ"ø\x0002)æúC\x0002 \x0016©|:ÇÓº®áÜcE¹*y\x001dFaF^ëÅ9XK+¤.ËÉzñ\x000c½\x0008{\x0002ÌQL¢Jï'SM<³õ¬¬F:\x001a_<zúìôr:Ík\x0007tëÞû{\x0007\x001f<Ê|:¾´Ök\x0005\x0011t&~´nÿ\x000f\x001cE&¢v\x0014°w\x001e\x0000X¡\x0008ÌhØË"h«\x0019¬s>^æ\x001d¼8\x0010<\x0007Ø\x0004¯ÿ´k\x0014½+Ó¥\x0005+JB@\x0014DïÖ_D+\x0016\x000e \x0008\x0008\x0013{Ï²t\x0006bñ\x001cÒv\x0010Ã\x0012\x001bZa\x0011\x0004^z´4Eîë*Sp1\x0007\x001f}ðð×¾úö\x001bû\x0007\x0007"0»<gEEQ"8ïíÙÅåd¶øïÿÁÿû[ÿúO7\x0007ý^\x000c{i¤A_[ÛÌ\x0017n¨ \x0003¢º®\x0000 \x0010X¢(³Mm\x0001 M\x0012D¬\x001a[×m]µ!+;¼ÿ²ª\x0002\x0012ÄÒÎ»4MPkc´2F\x00111\x00067oê¨U¾Ãò\x0014\x0012\x0016E\x0014\x001aJÁ\x0011>¢ÝÝÝ²ª>úèãáF?I"ÏO?òäÉøòÒ9ïîÝÍÍ,KÓ4
^óK»yÏìêºÏçÌ\eÓ4ZkEÔå\x001e¨°^íÂ?qw/M³^õ\x0003¤¶·wÑIäy~qqÑ¶íÆ ·¿¿ãÆ~pëö­ªª­m\x0001@¼EÄ}UUµw"LÀÎùù|\x001eAI\x0014E)\x0002|QU¥î\x00047D¤Ñcã\x001bXãÒuZ¼¥=¢+U\x0001\x000b@Û¶Á.d¥ÌGÄuvWxLgÓ|Qy\x0006\x0000ûî»÷^ýõ^åEQ×UYy7MS,fgggÇ''óy}p°Õ4MUrU5¨q4Ú¸uëÖ\x001b·nÝê÷z¡å]åà\x001dEF\x001b\x0013Ò \x0016E\x0008`ÿJ5¨\x0000D	kp$îòøéïþ\x000fÿDÚFS\x000f-;o\x0011@Ä\x000b\x0000Êj@JXkÄÕ\x000bù\x000cÅWêPhiòËÎ13)e\x0008¯]ø-£5iå\x000fÞ\x0003Î9Ì"Y+\x001dÈY7/Ê´q^ö`öúÛ\x0017·nßMû½áp8ËóªªÒ$¹\x0012{³xð"Ââ}%ÑyÝ\x0000mm/Í"mZÛfiy\x0011gisÚx\x0017ÂX£[7NO\x0016ù¬×K\x0005yù@ËVz·#¼ü):è	Q£"Fê«íMh>Ï³8Ó¨ÏÆgeQ²gEt°·³¹½=ì÷Ú¶E¥P\x000102«¶©½÷¤0cñ62\x0019\x0003D¶¶\x000f.Ç\x00174$\x0005£í¿økH>ÿì3\x0013§°,.V;#!Ê\x0017lóÔyÆ9k­uÖ9\x00140:öàpô|éRãeðÃòÚ¹2º½\x001eµà/Jë<ÖÆZ»ÌÄ¹\x0016µBøiÙÓ|¡²!`\x0006\x000eË\x0006iê\x0012&å)r b\x0002k¹UDJG°æ*\x0007+í´\x0010.i¿\x000c¤Ø°kÁivQ\x0008e×Â%E^Ñï+7Îó\x0017Ãq*ø\x0011Í`
Ïy\x001a/kÌ®{ÁÂ¸jöøejÝ.Ö\x0007= µÖ]?9>>;¿¬ªVwü7q÷+\x001d[(\x0008 ®7à`i½#r-­\x0016»ôíõû\x00158(\x001eYØµ!²Y«·Ö['Â]\x0019-Ðz§L Z\x000bÓ¼ru5N'gÓz1/\x0017ùtZÍ-(Í­\x0011{\x0000¡^¿'"m[{`aÑZ\x0007\x0015Mø\x0014\x001d\x000cm\x0014é(ÒQ¤\x000e²\x0006\x0005À=\x0010°\x0007N"³1ÈFÃáæ íÇ±Q\x0018\x0019e\x0014*R:eªZó~¹\x0015x­Y\x000bFXÿ)Ò\x0015Þ¹þü«×#¼<\x0015¾ð£µ!ÖéÈV_;agmÓ\x000c¬µ÷n\x001f>;9\x001e\x000c\x0006Ò\x0014ÏDàXx:íì\x001dØ*ß\x001ad\x0018áí[UÓÜ¿__Ü´ü¯{ô\x00070ØB\x0008QQt\x0011\x0004©¡¢°HB¨Ú¶ò,½~&6ÆYÏPâZ¶i[ÛZafE\x0014û\x0002±\x0003RÖJ+£qI Óa_p\x001e\x0002ïÇ{Z.\x001aEYÚÙÌ9;\x001aBRãååx>\x000f\x0006»wn?}úôO?ýôÓO¦\x0019ô\x0007·oß>8<M\x0017Ì>¼mfVJÖ\x0011må~-Nª®³^Ö8J\x0005ä\x0003\x0010EºËNFWeçìlÈt1'"\x0006>==½uë¨,K\x0006ñÞuýèé\x0007\x001e%Iò[å·PS/\x0019\x0000³ÖdNãÓç}d\x0008\x001cHÍYeÕëõ\x0018À:\x0018O§ÏÏÎP©ªmx!(
\x0001¿Ý\x0014-¾²îµÃK¿¥ï\x0000×u\x001dj\x0008BLMÓ8\x000fZA\x001cÇûûû½,ÏççççEY\x0016y\x0017yÛÚ|6-Ê¢i\x001a£¡i\x001aïXib½x\x0018ápHÞ{mtBµÊJ_ÇÅb6­O?\x001f*À$ Á+q\x0000îwÿù?É§½Ø(açíÊx;ðpZk\x0013 uÚ\hs­àëgÌÕê¾\x000e³=4ó:sCÂ%ÀÎì½wËF2J©Öº¶íÖ8$d\x000fb\x0011ÇK«ß|Ñ4Íp°UÕõ«\x001fï\x001c\x001cÝ<º9Î¡m[ç½ÈÕÂ±ZvE\x001c\x0000Ä&TÓxì´!mÈ9¯¨¨«@#WZ\x0007\x000fâ­Í­ºª\x0001 Ïs\x000f\x0012EÒjÐï¯_RZ[»o\x001c\x001cu]E]×ÁT\x0004ÄÁ`Ð÷uZYëµ"h¢¢,§9"Þ¾s{8\x001c~åKïeý¾\x0007\x0019/f^:þ9\x0000;k=\x0008*Ò\x001a®dðu]îîîZ®ó¼¸óÚÑÖÖèÉG&Z³g\x0015f\x000eò\x0010Àü²ÖzkÙ{E*\x0010ê:-\x0004¶&#gHKM\x0013°÷¢°;\x000e®¬G\x0010\x0014vS+(¼Ø\x0007VøÕâû\x0013\x00183]CÊ_lBFZUU^9ï\x001d
>ÏüÊø\x001e*\x0008¶½\x0013v`k_+K­r1¨
)&E¢x½Jù\x0006\x0000\x000fWh\x000eìE\x0004dåU^¼­ÀYÐ±k¼­+×Ô±\x0004=\x0008\x0001ø%Kií\x000e¬3cÖÄ×\x001dz"+Ü§J«:f5ys
i¸®`
f\x0007ÌótÕÀUóN@íx:]//çó¹\x0017^.(/î¿Tq\x0013¸\x001ce!ÖP!!bx\x0010\x0010Á+\»F%xfô\x0018²BCÇ\x0001BÚ0,\x0015¥NØ'm\x0008°aQ\x0018×¶®jÛÔóÓsM µîGÄ\x000c¨ôåd\x0017ù íápeÙd2A\x0012ìNÒH@Èâ\x0001Øh£\x000eÝk\x001fg9NÒ8ÚÞØØßÝ\x001cõÌ\x0018C%V*¨±\x001b!úZ¦/.MÖKÒõ¡þ
@Ý]
Ó¼ó!È\x00129\x0016Â²dWDáÍ\x00084"­H\x0011i\x001dNð\x0000\x0010\x0016:$´Öµm\x001b%q9=}0?\x0017\x0011\x001d%uµxvz9\x0018âd0\x001aôÒØì\x0019Ñ\x0008Ð¶¶mmxÈá`°ôAFPä¬­ë\x0016\x0000¢("I\x0002\x00003Kxç½\x0017ëÀ\x0005©Ò3wËleÊª¨½s¤\x0008w­m\x0005(¬\x0018µ­\x0015k¥´\x0000"¥tÛ¶ÏÄK]^Xu½÷Î{&ReUM&ãð'\x000e\x000eöO¾ÿýïúé§"²··÷Ú½7Ãá|>\x000f0Òêy\x0011E8ë¢(ÚÛÛûäãOÊ´\x000cò%¾rA£Õ"F\x00085­ë:M³$IHÑ¶Ú99>9;»PJ§i¯×ïµU=Ï'iÅÿìþ³(úýÞææÖ/|ík£Í\x0000½ ÷\x0007ý\x000c\x0005b,É$Ï\x0015E\x0011G÷uUÕO>ÝÜ\x001c\x0005s £s\x001d\x0008÷JýowýÕÌ\x000bJP,\x0006ÞÏ\x000b¿»zf\x0014E\x00006ãÍÑf\x001cÇþy0Ë>>9®Êj/ª²*\x00166Ma0è§ivqyA
G£áÎÎö;ï}iksËDQUei·wv$uÖjBgmUUÖÚgÏ?¤µ>88«	u\x000czg\x0014ØºÈ/ýú6S)YÇYd~V,âV*L¤µQ*XWt\x0015tØ÷*M«ôÒ?¦µËFR÷MpW\x000cÄåÃ/§¥\x000eñðÌÞ9+¨P\x0019ôRÛz>Ï·v$MZç!K{yY"¸¸\x0018??y~xtKPw.D¯ÝWP=!y×"&Eà\x0018i2´E±»¹Q¥	\x0011=yò\x0018Q\x001dÝ8\x0012)ã8v®Ì²\x000c\x0000\x0016bgg//\x0017Âü[ÕÙööãöìììöÝ×zI\x0006@ÓéÔZ6F\x0007cìà¥ë[\x0016o\x0007ÛÚ¶®Úñøôìô¢ÆeYVUµ»»Ûß\x0018îíîýðÇ?\x001aF£­Ñî\x000e*Ê²Ô±;y~%VQ¦WESÏµúÁvo3I¢?ÿÓïß¼¹ùïýõ¿.Þ×e¹¹½mý¹Ù¹áQ×_\x001f*\x001dÂ"\x0014¼_Y\x00001¤\x0016g¥M'yY\x001e¶C®DhO®ì1\x00118¥T°ÆZÎ\x0007ðìUp>$ìF\x000e\x00077Á\x000ew\x0011à´°ºGHÈÞÃRèî\x0001^\x0018\x0000sç}k\x0001km\x0000\x0000·¼×+Ìpý»\x001afW¼\x001c\x0001[vuÑ\x001aí2-*ª 2¬Q)
kçìÐ`
\x000c$Aµ\x0004Ú\x0008\x0008AÈV^\x0000
èEU\x0014·-²U©×@×\x0014Òp\x0015ä`é\x0013\x0003+Æ±\x0000èP@v\x001dL%\x0019ùZÁ]Ë/àº#\x0001Ké2ÌPT@gçC"ìÚ¶¨ê³ÓÏ?ûl<\x0019{\x0010¥\x000f
.¥3LxûÝåë\x0017a\x0006Ò¡£J]¢!ic\x0002\x00193\x0018l4Î*Ek÷\x0010| k\x0005\x0003:ðØ5Ôt\x001cD|Gq\x0015F"\x0002a
(Wñ`\x0004\x00088ÛÔÞ6¶mØ[EjQTPT(¬\x000ewúi/tQ\x0016Ã>³³Ö2c \x0005Êè(#m¢(2@:Í[À:\x0002éJ<@¢¨a\x000e³´\x0017©ÔÐpÐ\x001b\x000eûý~\x001a\x000e\x000cÝ!8\x0004h#Q¨&:Ó¿«@mx©¦ùÉ\x000fç½wÎ:×e}17Mã¬
é.Ö:ï]X3ÃóC¤³1\x0002»±Ã3"­Â¿|³|3Ë\x0018\x0000²ªm\x0019\x0015],\x0006q¼ÑKÏÇÛØïïn\x000e?»ÿ ¿³'N@¼°\x0014å"ãþ`\x0010ÇqÆIÌf³,fÓYkëoüÒ/¥i6\x001cmlmommme5Ïã8ýèÃ\x000f÷wÿ ®ÚÖ¶ÖZö È\x001b$w­®\x0010Ã\x001e	\x0000FºªQi
Q,ÞùVb E¬h¹%/7
\x000c*\x0000\x0008Ú¥Ñ(ÓZµm{xxãí·ß\x0012\x000f?üðïüÿn4Ú|ç÷67GÉ4ÏË</\x0003_\x0014\x0005û]a)ò\x0012\x000042	\x001c^ÖÓF\x001bcÂA¼,\x000bâåB£Ú\x0018\x000e.ÇãA\x0014¨ù|>\x001c\x000e76jfïw,\x0006ÑÄéönº½»/â\x0017ÅÓã\x0013\x0016ÙÛÞ¹¸¼\x0018
Æ(\x0002ÌÈ¶vgg3Ë\x0006eY(AyYõD\x0011:'ÓéüÛßþ\x000e\x0000(­\x0002\x0002Ëº* .ëÒ
X¶ºE8¬~l¡\x000b´aÏÎ»\x0015\ºªÕ:\x0012®ÒuÝäÏÎ6ã8vÎçù"Mãò2Ï8\x000f\x000e²¼È¦ÑÆ´-oú·ïÜ~ýõ×\x000fn\x001cn]\x0014E¤¢Õ~tqqQeQ\x0014txx\x0018Ç±ÑÚ3ÿ|¾2K½mÐ$Q\x0016ýóü\x000fÛr>Ú9T¾Ú\x0006¢`%\x0012D
ÔéÂ1\x001då:e\x0015V\x0000Ü?ºÚJ!ð\x0002D2ôÊâÂ³óÎ;×7a¥\x000bÏ	\x0011Ù¨@k\x0004Â¦iH«Ö¶K' õ0ÚÚ:9\x001d|ÿÓáöv¦q\x001c¹p\x0010dX\x001ee±³\x0003Î°,$ë!^\x0019À\x0018¨>9ùÞ÷¾÷Ö½MöEf½^:\x001ac¼\x0013çu.\x0016iÛB\x0002ê\x0007¿ÿþî\x001eÜ»{ooï\x0000\x0000ZÛzïZçBÐ	²°sì¹mZÛººuÁ\x0014r<\x001e//¦EQÈü>"¾ûöÛ¹aY\x0014ù`´¸3\x0018õ···Úº1F{\x0013\x0013é~oèÝÂ¶¶,ÙbZØ\x000c6£¿õ·þÖ{ï½çÅÁÁaÓ4À§iWOâRôNü\x00025ûj{e\x000e>\x0019Þ:g­gF	S\x0001°C\x000e\x0008\x0018\x0002Yµ»	KÃzï\x0019iyæî¨g´4¤
#SE\x0008óM<\x0012¼¾¯7ºÝ³ó½Ó\x0000`­ûY\x0002\x0001\x0000 (JX¼ca[å­BòNT¬LCZ\x0003!\x0011±ÖJ©uç_!\x000cû\x0005"
)\x0004ZAE¤[R1H\\x0017¦ÎBñ\x0016@W\x0005Í5\lÝ\x0006oí;\x0001\x0004îäß´â¥\x0005ÿ
Y_ªÖ\x0004VÏX­bý²A¾\x0002lP`í9ÌÅâìr|r|z9¾\L0½\x0008y\x0008<\x0004¥%(\x0000ß]ç5R9"¢(8\x0007Ã\x0018cT¤\x0017¶µ¶ªªº®Ùûà\x0014."Öún"2ëÔ­´ß/\x0013À	\x0005È	\x0003 "ò¨\x0011t`X<Ãß ¬\dg3
\x00008Û:Ûz\x000e+Ê\x0015Ü²Z£®èÒ\x0018¢;V±\x0000\x000b¡h\x0010-N\x0013§I<ÌÒÍÞ $b\x0015\x001fêph\x0001ðê\x000eÐYÍÐÊ°!áÑ\x0019[<\x0013q\x001e<
£° #ÅBf´Þ£s°î§5\x0018
J#\x0011jÅJ\x000b\x000fáÁJX¢µ7#àQ<\x0000(¤(5
q]WuUõI³8RÛÃAj\x0008\x0011¶FÃ(³ÉHi$RÔËzZif¶ÎùÒ!"³EûýÞÞþÞoýÖ_¹s÷ÎÅøÒ{ï=km\x000e\x000f\x000f´6\x000f>ÿüñã[ÛZ\x0019cL+­gÏ\x00126Q\x0006äº®Ùs8?³öN«Èhã»#q\x0017¡\x0015J6¥Bøw¸\x0004Z)\x0013¥\x001f?6F§I&ÉüÉ|úé§ÇÇ'wîÜíõ²Á`¦Ùd2ùz\x0013)YuR1IÅbAÞyç¶mW	X«6%\x0001®ÚßÓé´®ëËËË4Ë|kó<'¢<Ï{½^hÕzÏ(2N©h8\x001cZçÊ¢ðÂñøøÙ3gÛXk£H÷ww"vmYU¡zpÞi£CóÙ\x0005Jxè""¥\x00158\x0000\x0006\x000f¯p
üW®«®\x000bþä\x0014VÅ¢h-Ä1$IÒë÷ÖAL~|r2M½8Á fét:'wï\x001c\x001d\x001d\x001dÝ½wo¿n\x001b"Ê²HaçO\x001e?©ª*/Ë4K777{½^àöÎyïÏÏÏáçAe\x0002kûýTóââùïÿÞ¿è%Öª©Ú86]txQdL\x0014EQ¤I!\x0008Óry}%Ûw¹o5Òá(à».ÇË¥2Ð\x001dbóÎÙ\x0015oS\x0018+¥wN¡RH("ë¹Èóª¬²^¶þG$q\x000e<9¾yûùp8L¤¬ªNvºt»â\x000eië¸T<®¼,76G\x000f>øð\x000f~ÿ\x000fï\x001eýõéôbÐ\x001fÄqÜØVÇfilÛ¶m\x001b¶mÖÞsY\x0016Ï>|ø`\x0017ù"ßß¿è÷úÃÍQ\x001cÇI÷DÊ{ç\x001aÏÎ-¦¹mr1¯ëÚ\x000bÖ­«ær2¹¸<óÎöùó×ïíü¯þýÿM/ë]NfÇ'ÇÁÿÛN¢\x0014XIØHdápXWmQÌêÚz_ÿ_üÍ¿ò\x001bãoüµ\x000f>üþåøâõ×ï\x0008Ñ<¦S(Õ¥± ¨/ª\x001e:úsÎZ§µ2\x001a¨à÷üE\x0018f	:ðM¥:o¸\x000b\x0003Ãó5é\x0013t\x0002\x0017_],ÔK§ØPã\x0006¼ÍYZ\x001b\x0000ðÞAÈÑñL
H\x0004D\x0008de²tJ
\x0010\x00140\x0002£­«F)ôªQ&&­P)ÔàÒZ¯3\x0011Q\x0002ÜØ1­\x0006\x0000ÀH)£óÊ5\x0016óq]æF\x0007ØR:u\x000bzXöw®]öD\x0014
üê}.%\x001c.iP|¬îãúÕèÎUk\x0017s\x001djöpu>[K­\x0007^ô	D´|±øô³Ï&ÏO!I6ÖzF¯P/=Ã\x0015Ð°D^¸5ÈD&2Qè½¢R¤RZ)ê[ö¡\x0005ð»ë5ÌÊ¦=SI@\x0007I\x0016$O\x0002\x001e(/äQ\x000bvNÌ¡°Mk5	m[o-0x\x0016î\x0012\x0002Ó½ÁÉWMf0\x0012°\x001f\x0004V\x0008F1\x0014i2
\x00141\x0003`F¡ÎçziA\x0004k¥Ì2\x0007W2¥©aô\x0004\x000eÁ\x0011xAFdDKÝä	\x001c£ëû\x0013B\x0014\x0002E \x0010\x0002A$\x0002R¢´pÀ3\x0010Q	\x0002\x0000²ïz^\x0000 CÉÒ(oÜóù\x0004êFæy6Ü,óyíÀ(\x001cOAßG&IÒÔDQ$Hè«E¦ÓËÑh3têº&RJ«~¯ïg³Ù|~YUµ\x0008\x000fÃ^¿·³³]×moÔOÊóÕ\x000e\x001aòÔ¤i\x001aÏÜËzE^4MÃËµ+Ò\x0011:\x001bR<IÑ|17&"m\x0002$\x0013\x0014y\x0003«\x0001~¿·µµ=\x001c\x000e=ûÖ·¾õðá£»wïìììeñìÙ³ª¬vv÷òÅ'¥êº\x001enô½÷Û[ÛeUE\x0019º0Öu¦\x000fHW>¤£H\x001bÃÞ÷²Ì\x001bç½ïõzeYÂ\x0011¬8=Þ»¦©Ö[[QdHXiím£\x0000«"/ò­«}\x000b\x0000Ö:o=Fe"eõÞD@\x0000\x0008o \x000b ¿\x001e¶þ«Fäú\x0011È{ï¬\x000b\x001fðÕx¡ó\x0010\x0019ØÜ\x001c\x001d\x001e\x001c\x0012"3\x0007{ñåÔDjc{ÐïõH)W×q\x0014F£7ßzëæÍÛ[[ÁEëªöÌu]ó\x000c\x0000Á°±±&I(\x000cÚ¶µmÛZ+,?½!a\x0004&`@ áÅô|%öéGëW~±O//ïÝ:¬|õ+Jé#CjÅµàu7/x\x0004J)\x0008	Ù+Âªo\x0017ZPq\x001c\x0011)ël]Õ"\x0002Þ\x0005ÿ.ÐÞ\x0012\x000fW\x001e©ZGÚøÉt*"iÚ\x000bCDØ`UUl^\x001f|üá×ñýN"\x0011s0ùXîì«{ùâ Å¢Ø½}µþøóûeSO'Óédf©ÑF+£µ¯ªÚ;g­óÞ;k'13GÙ\x0018nFQtvvúäñ3mô­;·÷öö÷÷÷ã8V\x0013×´¾õÓé¼©ê²(ê²\x0019_Ì<yfmsvþÜû¶®+aø+õ¯nmnéÍ\x0011*=M(0¤êº6:ÖºjQ\x0011^¿¯ÇSk¡®áù¿þ­ÿô?ýßåÕüþýûx÷Î¶m\x001bÛ
\x0005\x0008áÅû"øÓ!\x0010Û¶/'ý®\UÈà )\x0012ÎLp}ë]!+\x001d0ó\x0002u@^ñ®ä\x000bó>ü­m	ÑyK¨¾èù²tÚED5k9ñÈb]\x000c¨´w´\x0012%¨Ò¨FTWþca7"\x0012Â\x0010@¤\x0001\x0008Pi²³hbKX,fu]\x0002\x000b®\x001dãåZ\x0012Þ	|ñ[½Bkae«w|íkü«Ö¯¼Z<õâ	Ì	u}yy\x0001ÈÄ¨4\x0001F:VD×ç\x0008­H¦«Gw×\x0008\x0003ËRD \x0001'Ë@\x001c\x0000h¦(rk\x001d\x0011Åi\x0012ù(°¿h\x001cvð\x00110ðnXº\x001d­hÔÝ\x0011\x00051|æË [oë\x0006Ã\x001bê\x0012@\x0008ý\x001e¥ÕËTÙpæAB\x0014\x0010a\x0017>;÷Þ;v¶mëF\x0001Kãm\x0000\x001a}É¨`¬\x001bXB!\x0016\x0006:\x0019ÒÏÊ0\x0003¼\x0018\x0012\x000eJû«\x000e>\x0000½¤¸ Î\x0011»û)¬<²	¸«·dUW±\x000bXgF\x0016\x00116*\x001a
NÅ³¢ÜÙ\x001aÕÝí­H1*I£^¿¥i Ê±°kÛ^¯?\x001c\x000eEÜÎÎÎÓ§O¦¹¼¸x>\x0017E¸ÅiÔu\x001d\x00186£ÍÑÇÏQ&Nó¼ôìS¥W}¥¶mE8I\x0013Dd\x0004Î«\x0014\x0008	+­´Òåxc#RË.ÞúÃ{7L	ñüüüOþäO>üàù|¾³³³¹¹5N´6iÅq§\x000ebTZ¯\x0002°tÔ\x0004àE>\x001b\x000czMÓ°p\x001cÇa<;ï¤xÅ¸EÄ¢ÈµÖEQöz=ñÜ4Íb±\x0008*¡î	WF¥AF\x001eEQÛ¶uU£ø,M£A_DÃþl2um]\x00058NûI\x0014\x0019(Ì¬´òì½¿:ØÂý§.é/Ï{aaZx¯G\x000e/\x0003ZÁÆhpttttt4>¿hÛv2^\\°ÀîîîÁþ¾6æÑÏæóùáÁÁ¿ò½½½Ñhd­«ë<\x001bôæóùååx±XX[F#\x0013Ei\x001c\x001e\x001d\x00054/
ì|X\x0014DQ\x001cÇaU}yÅZÞëoQ1+àAkïwþÅöæ¨¬*ï|fA\x0008I8,úÖ"­\x0000Q½xöKs\x0006Ðkp	XDùnÆJèM\x0000"¡"íÅ\x0007\x0005*èã\x0019\x0018\ãT¬´6!\x0018wss;¤·meâT)R*2F¦ó¹1zk{\x0017·ðáã§£­*/óÙ|0ØXÌ\x000b\x0000ë½gVu]@Ó4§§§ LðD\x0012\x0000£µoí¢ªÃ	\x0005á\x0007C&8rÜ\x0012Åq\x0014\x0019]äÅö­£iUô\x000ev¾õþý÷?úà\x0017Þ{íÑ£''\x000f\x001f\x000e\x0007#fvÞ±gfL"\x000e.ÏÇÃÑ\x0006"FÛï¾ûnÕÚ\x001füà\x0007\x001füpwgx~~ytãhzg\x0016EQÖëEq¯Ò·pq1çÓËY>_?-¦¤`wwS\x0008µn±\x0007å¡Õ
J\x0001KÓØáfYæì=heÒ8ÓZ§}µµü'ÿÉÒ4ít<\x0001Í\x0002¶lj\x0000&\x0015~\x000b¨ v[è#@\x0000¨ ;Çç\x0010\x0005ùkÚÊ³S\x001aÕJº\x0010l" \x001c¬ÜÅ¢%B¡-¢DB\x00084\x0002]Â-'§\x0000tí­õ\x0003zÐ)¢ðÓµ.ïÕ¸]A=»Îd\x000c½FXS("²1ÚN§Îùþh«i\x001a`
«ª&E¤\x0000B#¢o=³÷\x001e¥\x0015ñ(\x000e<sÚËy9-ë:äËEyÕ*Eèe½nb\x0001!(mb¥S4Æ9?¾8\x0007ÏÎ:RtF4´ü ¼öq®¸2>×\x0005>\x0019vw¤{}^%.¦@Wó\x0005îQ¸DÁ\x0011u
åzÁÀpåõ²ê6ò\x001eÕ¶	t0ÚX,
ÄZ\x0019åYS\x0008\x0003zÓõ_Ð×øÊ$Ò:ë½w\x0014\x000c@E¤mÛ¦õÀ\x000c¤< Ð®D½´NuÒ+i\x0001`tØyÏ\x0001xAD½\x0004óAa\x00182\x000câQ,²íª:\x0004"4¨\x0008Áz_6upÚ\x0010\x0004æ\x000eÒ\x0011ic¦a¥\çK\x001eó\x001d-èê´C$Ä\x001e¼óUSÇ¥2Ò4vâ5kO\x0018<*|x\x0011F&Õ\x0016+(°d­Ôé×tWX¬úòWä6¥\x0015\x0011jç\x001c\x0013{/D:täA\x001ccXe+A\x0017)\x001c,Í½\x0010RQ\x0008Wð¾Köp\x0001
>\N\x0011\x0000TL\x0002 \x0000\x0002E:J[Ìæ^Åé`³¦Ãaõ\x0007{{\x0007\x001e>ÞÛÛïeY[Û­í\x00113\x0003pQQ¤Ë¦>\x001bÝ<ºùüüù[ï¾Uµ1&X'äy3\x0018\x000cÃ¾V:ëõò<Ç¢bëÑ9®ÊÆ± ¢³³Ó¦©H\x0013h\x001a¥#ë;ÿ÷Ùl6\x0018\x000eËªMSMDeoon\x0012¡QÏ¦óyô²ª*ªªzsçMÏ®*«÷ßÿÁ\x001fýÑ\x001f%Iï`ooODL*R¤(ü\x0012\x0011\x0005\x0001@t\x001cÄ~>¨\x0010¬wá\x0010\x000f\x0000u]'I\x0012à¶mc¥ÌrI¥ÊRâÙ[kC)VT%ª+
&\x0000\x0008Âª)J\x0007TÞIÛ¶­e\x0014µÚÞÞ~òäRÚd]¸ÖJX\\x0018\x001aHBÌMë\x0001<)"Ô!/Å\x0008P×&»Í\I\x0017WÝ1\x0011Q \x0003EOëHÄKp¬d\\x001aRw¥d¿7\x001c\x000eFy[k/Ç\x0017gggHò¥·ßêeYkÛç§§eQ¾óö;o¼ùÆÆÆFd"\x0000@ê\x0008çççóù\x001c\x0000zÃ~
nßºå¼cÇZ\x0019'ÖZ«¢84Ð"DüÉ¨\x000cH¨ÍQ\x0018¹­ÅÙñÓGmô³¦¬\x000cQèO\x001c¦´1Fk­\x0010¯¢yX¼w\x0001­Z]«Õò*kósE\x000eÄÏp§\x0003-4h÷­µìW®Çl\x001bÇ±ï\x000eÜ\x000e@+cREuëò¼\x00002[[A£_VÕd2?<ÂÀ·ó¾uµ½¸Öúù¢\x0008\x0013 \x001cÅ4©\x0017âzE$MSM¢\x0014¢ÚÇ\x0011#°4¶MûÃ(ëa\x0002þ\x001fîm
¢$#\x0015Ïó¢mÛº.mÛÞ<¼qvv:èõoÜ¸QÖµ1:\x0004Ó×Öi­÷÷GIô{}cÌñÉI \x0007 ¢k\ÓØç\x0017ÓËb>«sÙdccd½¼Õu»³½#ì>}úÝï~÷Í·ÞÜÜÜ*üìò"ãéYë\x0013\x00002Æ8ïÃaQUÓéü\x0007?øÁ7¿ùKeYnm\x000f[o½w &¥_6\x0013	díVÂ³µnÝp®'	/\x0005k\x0002\x0000jµNÃµ'(Õm´°\x0004`$Dâ*\x0014aà\x0017\x0000ô½xÜy\x0019eAÄu¡\x0001\x0000ø\x0007\x0010ÂH\x0004"çç\x0007\x0007\x0000ðüùI¿7TÊ\x0010\x00113;f
\x001e\x0005D\x0006t
\x0001Ñ\x000blÐ+\x0016%#ôz=\x001d%ÎIUåeY¦Y\x000cKÀ .«NÙÇâ
\x0003Ç^fu\x0007\x0008Ú0\x0004WUÌõUaÁ«ÿ\x0007X6®¤×KRË\x0017L\x001dãèº\x001cúßèÁÁ-J\x001b¦½ÖJ$J\x0019ï=\x0001lÞî.?\x0002±ZUH++¡\x0010 k\x0008*ÏÁ
E\x001bÎY"ê\x000fúA7DDZGA\x0004þEï©Ó^X\x0004 A\x0008¶,\x0004\x001dxdâ\x0010$S\x0007­\x0000TH$@¢kîÉa/±Î*}-w)nZï~\x0012g\x0011k}Ù´ìZi½më¦©zi¤:th_«5ÙG­]Fí®¾\x0003WTô«å\x000bÿÂZõ)(G÷ÂK­³\x0008{\x0008t`kmÛºÕ©\x001aI:ªµîÌúÑÆ8R\x0015"\x0006=\x0002TD\x0001\x0008EØÚ_dF\x0010àEÝñµ­4;,¾ÿ£O~ðþóEd½ª¬\x0010©m[E]u^×µ6ÁãTó£Ñæt:½¸¸X)(YD\x0001\x000cCÄ hâù|ÚËúY60\x0006¬õél±(,#­½µ\x000f\x001e?ºuçNd¢ªªDYUUÖUUÆq\x001aVWBÌóÅp04Q4\x001cögyq~~¾±±±··wrzúÏþÙ?ýèÓOööönÝ¼Cw\x00143\x001b\x0013Ñ>Xß¯×!a¤Àà&ï}\x0010ó³çñå8/ò~¯OÚ¶\x0005  ¡\x0015\x0011ï|­±pXa\x0010Ñ:§B[U\x001bòyÌ"´<~Ö\x0000¼n\x0018\x001f%#Ôue°÷
äN3hµ¢(\x0002ýj\x001fðõ±ýEß\x0014\x0016ø4KµÖMÓ$iÒ4íl6ëeÙ\x001bo¼\x0011 ¥</Ê¢Èz\x0008O'Åbá¬½¸¸h[õ²"ÏÖÛ[Û»»»Ù \x0017Çñd:mÛV)ê¬íÓt%³Zµz~îà¨~ÿüéñãGw\x000eÊ|ºÝOH÷m\x0018ñ¡ýh¢¨cG/çRw\x0015Ö±n¾B²ÃPXa¨¡4á%¿á\x0005E¢ó\x000e-\x00063Ç¢(£(Ê²Lkµ÷NR£ÓÓ³ËË\x000b­U$½^ïâô,Ïáòòr8\x001c)EÎ¹ÚB\x0014E¨¨Ëñ¥V:ä¹¯^¿Æ\x000fðÞ)2bÃÓ¶õ È\x001e\x0000¦IâÞh\x0004§±þ£?þÞ{o½óÎ[o\x0018=/Ê¼©êÅb^ååøâìµ;÷1\x001f=\x001aFJ\x0011)ã¸ª[":::RJõûýÁ ÿìÙ1\x0000h£//.OOÏóE9\x001bçÎ°1dòÊ«Iª`o0\x0018m\x001c\x001eì#Êt<þÛÿÝoÿ¥¿ôkßøÆ/¥iVäU\x001c¥(T.J'Î{§£4M³</D¤má[ßúÖ\x001bo¼\x0016 ÐÀ{0F)Rë[ÜjÆ5{{D|\x0001PDÂl\x0005«(gÓVH¤«\x0006¦¨Á%=(êÎhy]¦O\x00080KÖt"Ô\x0005Pt"F\x000e<¥Ó\x0006ch\.Ö¾xyÃî²´×¾\x000e\x0003\x000bRý(Ïs\x0000\x0018ô7Q)@%Q\x001c#"_^\x0010fö\x0008Ld½\x0013\x0016O2EY
wõÒª([k	ÉÕ¼ÌXsK\x0012@$e¬2)hë Êgó¦*\x0001ÀZ«®'¿¬6'y\x0011m\x0012!\x0014ç:kÕ®1®Ø0ëÖ;áJþ²`ý¯ÃL\x0003×~¥*Ëªª\x0000 M³àñÊ\x0015
©kVI\x001eAB¸<w¬|\x000c\x0015	 *¥º÷Ï¢F¢Xi$´Ö0ûrD\x0014üPÖZcÂÌ¡\x000f%kÑ«!Úi¸)\x0001B@`\x0000&°\x001dÇp\x001f¯ØE\x0001¼\x0002\x0006ÑK;
\x0000@\x0005""ÞYg­uJYTÚûn\x001bc /(H\x0008¤@H\x0011\x0011FÖKSÛÅ¼*À-Ô<1:)´6d
\x001f½\x0004_¢,W\x0016G+7õ\x001f]}:ºÒî½pOC¹À~]ì\x0019ÄíluNV\x001fm\x0005icL+¥Ò:ÜA&Ra^+ep\x0019AzEee +¤4\x001bn\x001eÝ3ÏNÿóßù½÷?üDG=Ïó"ªªÒ{e=\x0000(2Íbg-¢´m&ÉùG,1Jiç¬R´1Úàí÷MÓÔu³½½déÙåØ{÷øÑãæM¥§§§»ûµ2´*+E4Ú\x001c½`¡¦é×¿þõ~¿÷é§þöoÿíÙl¶··wûöí^Ö/«²®ë`\x0002\x00198.MÓ\x0004Êð+fg9ë\x0019¦Ó©ó.D4äy$D&éJ"ö"\x0012¾¶Ö²kEÄ:\x0017\x001cS¦%u­WÂ,+NÃË\x0002W>\x0010)MS\x0000(Ërý@¾Î\x001bè @Ë¹óYÿòw\x0010Q)åÙ\x0007Ú¯s\x000e «Á\x0019f¢Ñ&Ë²ÀÉ-óE$\x0007\x0007;;;'ÏOÆãÉtÚ4M³"
7½¬ªÓÓÓ8oß¾=\x001c\x000eëºÎ\x0014y`¥tE\x0000QØÊã8nÛ¹3V³þ\x000bK\x0000\x00161tÙ  2OÆ?þþ'±J´ò(FQí\x0010ªµ¢$2f))b\x0006\x0001Ç~ïÕõ\x000eøZe#\x0008Þ{F&"­µ\x0007çÂBDBié!Áà\x0008A\x0005}¯
# EWÖ9\x0010Jû)¡ªêª(êÁÆ°ß\x001b\x000c\x0006\x001bæ¼Ì\x0017m¯ÏDwâ¬K\x0006=\x0003Ø¶¥Ï·6·0Ü¤õU\x0003lbQ@Ì\x001e´sÍt|éQ\x0001z\x0012Ø\x0018öMlP÷É¦³ù\x000f~tk´ß\x001bl\x0007ß´	¼ôèá ë+Òé4í÷¼»&\x001a\x000c\x0006Û[Û­m2\x001b\x001b£Ë4MEäQþèÙÓ³Å\x000c\x0006¥ 21QâÚÑpc4Ð\x001aêºþüÑÃX$4óïÿþïÿÙ}çöí{_ýú×¶¶¶\x0000 ª*PÀJ\x0019mâÍÑÖã§\x0017E\x0014Áýû÷½õöërêÅ¦¥áAàü¿8ce­²Y²³\x0003"\x0012d-Ü¶Ö9\x001bf5ÍayÃC§=\x0008:%~gråÎ\x0014 1îè½¼\¬¯øÂ¹r¥t\x000b0¼Dìø"§W=V¿\x0000¨ \x000b15½Þ uÎ9ç&iPf\x0001@¾Xh:côÎîv¥q±÷ilï\x001e\x0001@QäÙ¼¬ÊÈD\x001b[[ùb\x0011~BÏBºf\x0004\x0012*ÏÊ\x000bi_X(ÊÜY\x000b E½xp´\x0002\x0018ø*´Zbº\x0003ã¯9Ü_»\x001aËÞihýÕ©z}ÁºF\x0001\x0006uEµ«\x0008$AYº¦BÏÎÇãËÉ´±mÖ\x001fÆQÊxå	X#\x0005Bv0ö\x000fñ«awØ*\x0002;\x0017"\x0008<\x000bG+h´QFk\x0013EÚÄ±oÛ¶¬Û¶µ@DZ\x0011þD\ðe\x0005\x0013	P§\x001fï\x0016\x001c\x0011ÇìZ`¿,1;T	:$ ,9Ë@\x000c\x000c\x000cDÎYqÊ\x0003_]½åé$°
\x0003áY\x001cSk½+|£	\x0001»¿\x001dâ>^n·Éà\x000e;Bêµúf}0¿\x0000ÕÈUY÷ÆXd)EI ìÌDzu¨
Áf)ä-\x001bC¤H@n®úV+±Õj@®þe²n³þàèî½Ûo¼÷GÿêOø£Ë\x0016îÜÛ¯«º©ÊXÅmkÙs(eêºbeE\x0012ïµ6@q³ét5\x0014ÃâOIìïïå+_ÕZ!¨"¯ãEQ6O<1qêsm»X,\x000e\x000e\x0007!QH)Êâ\x000c	ûYUÙ$i2è÷ó¢\x0018ö\x0007&lÛÎ\x0017scñxüÉÇ\x001fÿößù;uÛÜ¼yóèö-EæóÏ?\x001f\x000c\x0006Q\x0014\x0015E¨1¡I¤µã8ìÜÝ\x001fÞ§µM°£uÖ)eQ\x0012\x0007Ï"E\x001e\x0004YYÚÝ\x0017ç=!ê$ôÂ2Æ\x0018VÖ¶ÊS\x0014E\x0001¤\x0003\x0008fj\x0004Wbõ\x0013\x001aAØ¢¯Ò{	\x0000²´·»»«:>>¶õÕÉ|k\x0018Hõô\x0013Á\x0017
®bÐ:T¾«¯C¼á²\x0018cB
wr|\x0012izíµ»\x001b\x001b\x001bççç\x000f\x001f<¼¼,44QiFÆèOïßßÛÛ;ºqtïÞÝ²ª¦i]WmÛ\x0006Ã^¯\x001f&B0\x0007
4)¼òmùâRf	TK(i®ì7\x001f}þé³Go÷3W/6Ò¨·\x0006YUËkDd¢\x0012ï½`[\x0015XÛ\x0006Üy^u/\x000f tµM.ÍÐ®.7t\x0007áÀ\x001eð \x0014NO^\x0004\x0000â8õÎe$\x0018D«¶±®å6Af\x000f\x001f?}ôääÖ­[7\x000evö\x000e&³ÅÓ§y4Gqo7LØWÊ\x001aq\x000cÛAX¯µ\x000c º\x0018^(\x0010H+ \x001dÇekçÓÖÚÚ6"£\x0014\x000b?{v¬´ÚÙ=|4ç\x0007lo\x001f¾÷Ö\x001bi2_^ÜØ?,²Ì ~~ÿ~U5ï¾ón[7¶iÃÑh0d\x000fwnÞãôüü<6mZDÜÜÚ,\x0012\x0000\x0018G·\x0006ãËySQ<\x001c\x000eß{÷·n4M5\x00011tzö\x001cA	Ðx:~~~~üüâ÷~÷÷é\x001bßøéW¶¶·ó¼pÖ"FÖóGÏ.'U\x000bZÁx:ýèOÞxçõ²ªá(\x0017ùb8\x001cË\x000b\x0004¤xU²
¡H\x0000À\x0012Èá6y$b'¡Ç	\x0000Qà\x001bµµÛB\x0010ÆÃ¡\x0002z\x001f¦qw||qe÷\x0002\x0000ËÐÆ kºBDé\x000bJë!|ëÏè\x0006q×^\x0001è\x0014\x00180ÍH«óóó~¿\x000fBÛeSÿðÇ\x001f<?»\x0018_²²©»>\x0014ÒÊjLDîÞ¾ÝëõGCEj0Ú¸qc{{;\x0007¼({ým\x0011É\x000bëEåE\x0005\x0000ý~ßqÓE= # [o}ëÑÍKk½\x0013"*éj\x0008Ñ¡,"´|ç\x000c$\x0002!¶S)Z&\x001aáËIÚ«~®t-«°øpç9sõÌ` \x0017ÍÂWAópUÍ\x0000K`bÔ¶\x001dgÓé¼®ëÈDq\x001cÒ\x0018ð6&&e0$¾!#\x0008\x0010\x000b`aÛZD%R\x0011"¨PÁ²g\x000eN6\x0016,\x0012\x0016\x000f,\x0000~eÇ·Ä'B£y¹ÎèÕpð\x0005ÇÎv&$ú vÌÜ«ú#4êò×L|\x0000\x0007»Ý\x001b\x0001È	\x0013cpÌâ%X\x0003\x0007A\x001f"^EB""( ÔQ¦TÅxÅ\x000e\x0019$NÂ¡Ü)¢°|½TÊ0®üd^øÑË	\x0014Ëû\x000b×ÐÄAá¢\x0001@ðï»ÚH­Êh	Î1û¸+#ÂQ×¯à.DTd²N¦Åâª{(¸Ô,Â­[{?}tpïÍÖú¼²\x00126¶Rö\x0000@McÑÈöö¶Ö\x0006Çã1³Ëó"xÙ4MuóæÍ4Ë^ýµ¦iâÄ03¢\x0004k8éi£~õWõW~\x0019vvvæEé\x0010éÉxvvyñ·ÿÛß>?\x001f\x001b£ÏÏÏ	`£7Øßß\x000f=\x0007\x000f\x001e6MY©¾FDRj>¿vïµããÍÑèÆþÁ£'Ï\x001e=zôgßûnÓ4¯¿ñf$E^9·¢d>ÏCê¤í\x0004µ8\x000bz\x0008\~ñÌ¨\x0000Ä»Ö³G¯ëº½ÿó;·ï=~Bi\x0016¯(râ\x001dæ µ\x001e\x00004\x00002SdÄ{`\x0006º©4\x0015¯pC¢\x0004ÝÒÂ\x001bA¼0²` ¦\x0002\x0010\x0002\x0004ôZutgm²´¤I\x001c¥\x001e|æ¼G\x0012ï\x0019ðêÄÂ"Þ3ÑÚZÑ\x001dM×ðÈë"PaAJ©(êª^ÎÄ%\x001e±¬Î;í\x0018b]×Ad%ý8NOOÏüã\x000fF£\x0001\x0000D\x0011ìím¿ùÆk£Ñp8l[K¤vv¶³^¯*«¶mIÑ`0\x0018\x000e\x001b[[\x0001Á
M2_ûUÂ4¬@"ò\x0013P\x0019a\x0010\x0012!\x0004­U¢5:\x000bûóï|K\=H#±
\x0001kf\x0014Fv\x00108M\x0000K{§\x000e\x0014óÌ!awù]HàºÈ`YÍxö°­H­ZãÂÂÐ¥HØ\x0005
òÉ³¶\x0006ÈËÚYKJGq5J{ýÚNÏ/Æ½ÁF\x0016'£Ñèä4¯[ë±Ñ1YQ­\x0017Ç
lÐ?;k\x001dd\x0011DQ$Òù\x00010\x0012\x0010\x0000\x0011pÇö'`D\x0015EIXý­\x0017Ç¢&\x0013§ýÍ³ËÅû\x001f<ØÚØ\x001c%ØO\x0007ýx{mo\x0004a<\x001e?xø`8\x001cnmn{çÛÖöú}Ïì\x001dF£Àç`ç&\x0017cc´·ÖÖ¾Ì²Ì»jº¨.\x0017v¶6Çç\x0017û\x0007{^vçÎÚÕÇÏ\x000czýñd\x0012isy9iæÁÃñçÿ\x000fò'ÿú×ÿòo¶6IGMc¿ûçßòäÉååÔYÈRÍ,|úééó_\x001cm
ëf.ÂZéÅúV}£ÐèQ\x0008èD|k}ëd%[
É¡]«B(pxC«èj\x000f\x0008Ó\x000c^\x0001Á\x0012P+@h)\x000eü7| ¯b\x0001B©óÞ¾òù£\x0007ÞÉÍ·ã8~þüì[ògßÿá\x001aççùÂzIÓt29ïD\x0004\x0015FmëêºfëNÏ²^fã¸i·nÜ½u{´¹qçæ-\x001dEq\x001c×um[§U8\x0010\x000b3y×\x0019ý\x00111¢\x0008GZ¦ý1\x0011\x0005ú³¼t$Z¿2ë×gµ6]Õhë\x000f\x0006\\x0015(Ýkv
\x0002dá\x0017\x0012¼\x0001¤Ã´®\x0010.i\x0012¥%pÙ´y^_Î\x0017\x0005NÓ=*
]Ø¥a {\x0004\x0002\x0004B\x0016$\x0003B>\x0012\x0011"ÒZ)¥½weUµUí¼uM[²D.,^L¤Ò4S\x0006\x0000Ûz;\x001c\x001eÉü¢tnù¡hUÛ±\x0016âE$ø\x000cuWu©²î¤\x000eÈ\x001dÑRD³_ç\x001eAnç_ê÷]»ä\x0008´\x0012\x0013÷Lj4G\x0000©Ò¨\x¥UXQÉø:*³úzC_µr¾`<\x0010\h\x0000\x0000tµ\x000e]#\x0000P\x0014\x00147Á\@½ðÒ\x0001])#ËR\x0006  ³8FÙEç_-"ÞõÔZôl§:²á&(Ý\x001b8íUm£\x0000Ó$\x00024KEÀ½ñÆ\x001b\x0007ûYn\x0006Y/;<8ÜØØèõûu]3[\x0008ß¶qNØû(Ã>3(2m&Èôûý(MÒ,!\x0005Dd­½¸¸¸qãV8
\x0012Ñ`0è÷{\x001cð<RÁÔÄ;÷\x0007¿÷{o¿ývÖë=yòä÷ÿ÷?ùà\x0003°íÆÑÑ\x001bG\x0017eQ$iÒK³ÍÍMçÜb± ¢$I\x0002û3À}©«ºµ­w^À/ý\x0019\x0011\x0015©Ð.IÔDQok»(òàþÐ¶¶i\x0000ðà²É¾´\x0005Î{\x001cÇÖYö,b½gZrqà'AË/\x000f{®ê\x001a\x0000æó¹6Æ¯l®/ÌÁJýg}Y^¢2¡8vÎ+E/ÿ6!¦Ó³Sö¼±±¥ñññÉóç',pò|qçööÍ7Ãá=ÏÜ¶¶ªÊmëÜÓ§Oçóy
Ã¢,°÷£`Ì¨6F\x001bcÔZ\x0008ñjIüâRf\x0019\x001bÀBÀ\x000e!\x0012ï\x0016Ëï}çÛàþæ Z4\x0008\x001c¤Ë@Qá@°Ö<ë\x000eÜ¡\x001c	\x001ehWÏ\x0017Þ\x001eBbá\x0000G\x0003\x0000Q÷DBÈÕ\x0018 u¶m[g-*\x0006TUk\x0015©áp\x0017Åd:Ç\x000f\x000eolmm
\x0006'Â3µÊ\x0018@ÝØ¶ö>TÈU·mÛ:Ø\x001e¥A\x000bW5`¸\x0016«ì\x001bß\x0011½=«$³Ö"`ÕÚLE\x0018\x0015\x000fÊEýàñ³ÝÑà­[;÷ö6È»~?óH¿øo>|ðèï¿°¿%ÈÔ"`â8Mñxª\x001eö\x0007­m·F\x001bÎ¹¶*Q ××ÃÁÖ`¸SäîôùÅÙÅø[þý¾¿þ×þêÍ\x0007|f]\x000b,½~_\x0001\x000el
Æã±yW\x0017Eq9ü£øï¾öZë<\x0003}öÙçÆh\x0006H{ôzm[}ðÑùôÍw^{òlQ·´ó\x000ePR!¯¼
0\x0018¸FÌ\x0012í\âp¡tÖ:ë¬ã0\x0002Öâm¯\x0006ÃÒuþg\x0008\x000b£_Y \x0006oï%¯Þìúï
\x0001Àç\x000f\x001fmnïoll\x0012â¿ø\x0017¿÷?ûÎørúÖ;ï\x001a¥(í)2þp¸1Ïç³é¢¨+ë\x00080ÖF4¦NËá\x0010æùôôôôûßÿa\x0016'7\x000e\x000eßzë­·ß~scc£m$R\x0000nÆ¸S\x0014$ÏèA	 ;"a\x0015ÆøR4ûs\%ZíG«/ÐÏ¼6ýlÎÌ\x0010=¡³n6[]^\çE!@Z\x0011ºlÕ5F\¹Ñ0{M$"èA#(HA(RI¤Yª£¨®ëù|^×uPÙm­%2DË\x001d}Ñ®o\x0000«¦\x0012®Ù«/C¯Ös\x0012\x0018@­!óÌâE\x001cv¯vu6]%E !`ªXÞÕ×|½YõP\x0010\x0018Ak¥"£L,¬ 0B\x0004MdtìCÞøQÅU±\x0012^×/[°È¼\x0002É_1´ö\x0010\x0013C\x001d Zi¥"\x0013êE\x0000 2W
¸.Àä]á
\x0019Z2¡EEÞ³>² Ö«xu\x0018(ªÊYj-±\x0007lÜáÖ¦\x0003l½lïìQÞ¹$IÄs¯×K"\x001d^ß{ç¼}ýõ×ÿê¿ýo\x0019£4ãh2d½³6Ô¤¯\x0006aï}èìXkb^y¿¿a\x001b\x001e¶îÝ»ýõ¯íôùY\x0014EÕb~|||÷îëÁP\x0003\x0008"cE;p\x0002j±XxçH©Û·ogÓ?øý?¸ÿ>°ß½wïÖÛÇÇÏ¶vv¶vvêºNÓ^`§\x0006#,ÍLds\x0008*ËYg\x0003µ\x0005 Û¤Â	Miçy`¼:k³^V\x00149\x0000Äq¬n½C­\x0014©Õ\x0015\x0011ÇÎ;\x001fL_b\x0013¥Yêp]Ñ\x0006]p!HX|W¦\x0003×GCi§ÓË¹R¶myiÈûòcuJDÂuVáu\x000eûÕ#d[¬Ê\x0008Õ5|`Ì\x0012Ô	Dæº®¢ EQ\x0014åEqvz	\x0000½^¼³¾óî»·oÝòÌO\x001e=°Ö9ï¢(
\x0019UYR£Ñ½¿¼¼,òÜ$ñáááîÎîµPWÅwü$ÚoØÅ	Ø¶mJ¾Ìçã³Åä|`(M³`pKúXh\x0015ø ·]%Ù®:YÂ\x0002Ì¾#
H7ùÃ¨
\x001a%ç°h£qt niå=\x0000\x0018
Úè\x000ezeð,\x0000¸:n\x0012!êeÙtuÅe\x001d§³\x001cÇñÆpóé³p\x001eEÉ££Íí²=k\x001a'Jt\x0012W­k]+,Ò8ë\x0015\x0000c´\x0017qÂÎË\x000b©1\x001d$#à\x0004\x0014#fnZçXPiRªhÚÝÃ\x001b¾þá\x001fÿëá_þæn¦Zn#£666ËÖîîîõ+ôðá£GÞ½s§×\x001fVU£µY,ò8h¾X¶£<_L¦±V\x00077oÞÞ\x001cí\x000b«ñÓ§Çùlúüø¤¬ÇO\x001fíìlýú¯ÿê\x000føþßýoÿöÍÃ\x001bYÖw\x001d_\ "cL\x0012gÓòÃ?{¾A\x000cQ\x0004à\x000f_ì$\x0019OæÉd6
ú\x001bgçÏú^UV\x001e$"ZÑE¼ïhPÝ6ËáØ¹>\x001fÂ\x001dgUæ\x0003¿ãß\x0004Aí2\x00194¸xLµ@Yµ?vµÈ®\x0004G¯\x0004fÖËâu$~µ©{Ï\x0000>ck=\x0004²©ÑÞ	\x0000õ\x0006Ã8îýð\x0007\x001füîïþît:ÿÊ×¾¶ñK'§ÏçÅ<¯¼+\x0017y[\x0015"nlííFÑÓg'i6wÒ,Ë\x0017\x000b:â\x0001\x000foÜNÎÛº!|ðáýGONþõ·þôÖÍí¯ýÛY\x0016(x¶±B\x0000 ,\x0011¶ì\x0005"fÕ\x0019ñõó<®­õú!aÅY\x00013Ëp¸ÕóW·\x000c:\Êtæ«uÈ:¿(óét>ÎI\x001b\x001d%"è \x000eVÀÝ\x001b@fÇ¬PÄ3\x0012"0\x0001\x001a£#MNÓ(ã8\x001bôÃ¡I¢y³s\x0018Ç±\x000f\x001eÞA¨Èlm\x0013¨¸]ã%G FfÏ\x0002/\x0006\x000b¾@m^EPq\x0010~\x0017¾zÂÊ\x0002º^[Èð!Ü}É\x000cè²l9ájìQ]j¨`(«È\x0001z/\x000c À!"\x0018\x0002Ï¡E\x0008Ìá£ÉR\x0006»\.»®úõñ/ï.]e"K:\x001a \x0000" °Hz\x0000O.ô2dÙ¹Â¥s·§@>\x0011	\x0001ÒÁ\x001d	  ¡VBÚ\x0001z$èÂ\x001a¨av,-\x0008\x000c´¿¹YÖíx>Ý=Ø¯ëºjìÞÞÞl2MÒ$1ºªª²(êºnm=\x001c\x000e·¶6Û¶­«j6zïWÈÕ"#\x001aE¤µv©©\x000c\x0002c
À³Ù$¬(¤P\x001b\x0005ÎÇ\x0017e¹\x0018¶ªy\x0001Ö:ï¹®jfNÓ^[Õ"­©×;>9ùÝßù\x001fýÉ¿áÖèðp´µé¼?<:ªëº(\x000b­tÈLt°\x0010¼ùi\x0008môª¬\x0002¬\x0008ÈÎ¹ëdtbª³Z+MJ'ãP,*­Ãa&KäVÍÌ@¨ð+;Vöý^ßZ\x0017Çq\x0018a®ªJD<;ï84§ëfÒ\x0004ÙyÏ>©¹E<A&pÛ¶­µ\x001aÃÉT\x000b[/×Xª=¾\x001a\üY\x0016\x0017\x001eJ«0\x001fÛ¶
å\x001d\x0000,\x0016\x000bo\x001b\x0011H\x0012
\x0000\x0007\x0007øôéÓóóó'\x001f¦i:\x0018\x000cÒ4}~òÙonm\x001dÝ8º\x001c_Îf³4Í6¶¶Ò$ã8D:\x0004à.³\x001aºÈøÅ
&u1X¤\x0000\x0010zýä\x001f~ë_
zñÕøü\x0002\x0018\x0010\x0010Håe\x0005\x0004$â¼èÑÖöªÆï¨g\x0012ÖLZ6¼®î`ÙÊuÎñ\x000f]\x0016Ò*2AZk½p \x0016¤`nàÅ\x0013a°IpÎ6ÖÇq,@yQíì\x001fôaãàî]{ÿþYS6÷ö÷\x000f§ó²)rRær¾ (îo..ÆVâ½\x0008\x0018\x0004D¨¼\x0008\x000b.]T\x0010T

¢P\x0010É±h¥\x00041J³é¢H{Ã\x001b7nÜ:\x001a<#¶Û;£?ýÎ·§g¿þ¯^ÎæX3iÓO6F¯íóæáÇFÇ÷ÞxóòéÓ¼Ì\x0017Å£æf=ì\x000fòùôñ£ÇIÜ¼q´wpxtt\x0014A;£db¾ýÉG\x001f-¦ô/?ùßøº_;}úì?þÿá \x001b<üìÁééY/éýèÃ\x000f\x001aö-s\x0014«Vx{ T\x0000¤\x0014¤¨ª,\x001dÃ¿úÖ¾ùö\x001b¤ýps3íõf9\x0011f\x001f6\x0006
ã>TßëHC\Ù~«Ð6jÆY§´"éh4Ü9ò^ëúcçO³l\x0018yAº67xiLG/tj;\x001fÖn\x0014S+\ùoàÏ
Á\x000eÀ"-ÖÆ\x0000RÕÖYÚ\x0003Rßù³\x001f|øÁG½þèë¿ðËyY>;y>ÎMllÄìE\x0018MÜ\x0013\x0016Ï`_,ª´yc´ñ^ªª\x0012ðÃa³dGQq9¾8ºy'MÓoýÉG÷ï_~û;?x÷ÝwþÝ÷ßùÒ¾\x0017ù\x000fÚ¶ÙØ\x001cÏ\x0013£ÚÊ\x001b\x0013;ë'ó6C\x0001ÅpÁôê\x0015\x0004×õk^x­\x0004\»¤\x0008Wª\x0013Ô+\x000c×åæ	 â¸Gçg!à\x0001U\x0004Ïò>ù=\x001bRÈÜy\x000cºNÁAB\x0000èØe\x0005¢f¹x··½u÷æÍÃ^\x001akR»»»^øôâòÑÃGãÙM"­)i«[Û4MÐt4%RdBR\x0010\x0005Bú\x0015u±+\x0007 c\±÷ ~yÀdgÁ/\x001eDd\x0016p\x0000à½oE<0\x000b^¹Wl\x0005DézÉ\x0000!Î*4\x0018\x001c\x0012\x0002A\x0002`E+\x001f#\x0012A­#ïÅûBùÖ.sç>\x0017rê\x0000½XvÁ#p!VÈî\x000c\x0005\x0008P:\x001a²üý\x0006\x0005ºsÀêãðúí\x0005aÁ\x0008\x0019\x0008<\x0002"	¬5¶@P°3ä#\x0008>O\x0000 ""¨»ø\x0011è^Å39&\x0007
,{Çâ´£^¯ï­ë2ôùùéFPUU$Z\x001b°p9¾|úôép8lÛ&´]^è\x001bÊ\x0015(xs\x000b\x0010Ð]\x0008wthËr1/zY\x001f#óþ~tçÎ½ßøõ[¢¨Ëb°1²ÖNÇáphë¦¤ý4»}çvYÿê_ÿëû÷ïCöz½áp4\x0018lô\x0006\x0003DLÓ4sJ)\x0016¶Î\x0012é¶me¥w>?\x0002W¦[RÉ&EJ©ÙÇQêë÷zeY¾ýö»|òIL¥JGìCìy«RX+å=(úæ7ÿÂüã8[ÛU\x0011E\x0002tZÛ"|U0¤\x0014èK°¢\x0006ªªÄ{DMÔïõ­µ³ÙH$\x0012²\x0012nüõô«BÿÊ'}MX\x0000/\x0015.K¯.ödé\x001b@)£M ÚXk½gD°­+sg4ìímõû=ç}\x001cÇÇ'ÇÓÉ4/r[7ÃÁP+eÙÛß3Z'I*ÂGGGÝÁ÷.à£\x001a),\x0002Dj%Í[?Û|!*³ô~XQaÔ£\x000f?úÁÛ\x0008½!ÔxD\x0018\x0012ûÐ	«åUXÝ¤Õf³Þ]Nár\x0005&ËÒ·\x0011\x0000RIèH+m´ÑÁµ¶mmYUÖ UD<3Hðä\x0015fo[ß´62ÒZÆ³9édgÿ`g{ïøééÎvZ[ûàÑã×^=ÉzP@F7ÎFÞ!
*%\x0011¯¢\x0000\x0011 êjÖ%Ómµí*¥Zf &¢¬ßGDÐäË«²lê&g;ÙFÜt²1ÌvwwG;{(ÑýzþüññÉ·þä;7o¸Gºâ´*ØDÂH§ÏOï½vokcDDÎ[£ÔÎöF?KïßÿüÞ½[7\x000eo\x001cî|ðÁ\x0007ÿûÿì?»<«ÿãÿhðýÏÿüéÓÉdlâx¶(X\x0003HavÂÒe-0\x0002\x0005ê\x0002\x0019­áôôÔ:·»µq~~
\x0000I.~w§ÖZ°¶Úªú\x001fÎûª¬V3\x001c¤ÓË\x0008\x0005Q\x0012\x0000pÈ^m+nã5Gþn\\x0015%]¹Èj\x0005É´lkz¿ø}}î­NxM¦Ù ïª"tû7\K\x001füøãg'ýþÆæöNÕØGO±÷·ïÞk+ªz±(ê¦!2EU.\x0016EUUÛ[»ÖYk}U56\x0004\x0008\x0016UÄ\x001a\x000c·\x0006\x001b£gÏÝ:Ê¾ùËïþèG\x001f2éïþð£g'Ïó7ó½÷Þ»qónQ\x0014Ù3\x001d\x000b#8\x0008\x0015{\x0006Ñ
þ
\x001apðj«I¾ì[½%¼Àxákêâ)Ñ\x000b\x0010\x000b[÷ÿaî?-Ë²<1l­µ÷>æºç_tYÕezº»zz¦Ùf83\x001c")\x0001\x0002$\x0001\x0004GÔ7Aúø\x0017H\x001f(h\x0000
\x0014@\x001cvéiS¾*Ëe¥\x000c\x001fÏ_sÜÞk-}Xç{ÃduÕ\x000c\x0004ð¢::òÅ{÷{Î6kÿÖÏðºjnÖ«\x0018¼WAN\x0002Î\x001bxtRPã?J\x0019Â|:É|O'GùýwßÞßÛyS7?|øø\x0007\x000f\x001f>\­W¬êóÌ\x0005O\x0000ÊRïb
\x0019"úÑRÌ8\x001dnçRÍ6w\x0008:\x0018|\x0013R¯\x0017U5\x0007V\x0015\x0000\x0015I)µ\x0012YÙæ /¯Ýo¸Ã£SY\x001fV Y\x0019\x001bàu,%³à\x0004	@%©2öÉ¸}þÅ µ´ÎáÐ¸¿  ¨(*x\x001c¢3Þ(ÃÕa\x000fð\x000c\x0002\x0002öö\x0000;\x000e{æá«\x0003ÑL\x0002½Ïï,±Ó¿óØ\x001ff\x0000COÃÚ8\x000c6\x0007DQÈÁbo¯jºåzã}6Í¼ÇÍ¦]ÞÜØe7'IÈÈ4
¿â5f\x0001#b\x0011\x0000õÎyçÍÉ3ÆäBLËé¢\x0004Ù¬TÅO?ûåW¾ò[wï ¸¦iöööêº¾ººÍ\x0016'''²<{þâ¿ùoÿ¿?øÁ\x000fcì\x0016Ç'·ïÞ+æ3V=??ß?Ø\x0001ä\x001brËSj,tÖy×+w¤gZ!ÏóIðÂbù	\x0000`L½ý½®ënÝº\x0005¤EY\x0018GVDÒÀ\x001cÝý°àª¹Ã.E¦)"óAUËI\x0019bPM¹Úl8±\x0008÷Tæ9wmÓ4¦A3w\x0012\x0011aN"ÉÆSâØui·Ù\x0007ÿëÃÀoüW£\x0015\x0002wåprºwrtxûö-\x0000xöìù÷¾÷,óEQåäÖñÑ»ï½wzzj×LD\x0016+{}u
\x0003\x000b^	Û¶íºÈeYÈó¼,'Þ{«½,\x0006Õ~ï2dé\x000f@\x0000Çüð»¿øìý£ÙKÜI2ü\x0006>\x0002¹q¿ñeô=CíÆ/\x0000°\x000eª¦dÞ.Ë²àw~¥«õz\x00139\x0005ºÂ\x0007\x001f$v\x000eÑ\ÏÈº®¼÷>u©m£0¯V+å·nÝÍ'%8/7ë³³Ó;MVLÀùÈea½¬zè×.¶\x000fX\x0019×\x0008c\x001c#£¸sÂÊJ\x0014Î_<\x0003«Ë³§Ï»¶>8>xQ/«&MfYÛÂ>~pwÕ\x001cmØ{Âd\x0011³óë³³\x001füèw@o
e¬x³Þ\x0014Y)I|_B¡ \x00084]ôä\x0017óÉ\x001fÿÑ\x001fþò\x001fÇ¦~çÝ{§ÇGúéùüüG?øÁ|¶7NÏ|Oö\x0006%¶¢ë³sÃ\x001d¥Â	*\x0001lªfñâ§?ÿÙ[÷þÔN\x001bYæÅ4Ã \x0004-\x001e\x000eLëáÞl\x0012r ÊM³Ùl\x0016Ì!\x000eÐïØ1OúU{ÐOÿm\x000cã­ÁåVt·]j­ñÃ8_\x0016§äÈeYn®W\x000f\x001e>ÿÁ>ÚTõl:»¸º^mêÉ|J.|úùçUÕ\x0010"Q@t\x0002<)ÙdI%ÅØu)%,³ÙL»®«7«MSû|¾°_úùÅÕÍýû÷ïxÿÑ£G.øç\x0017×ÿÍÿg\x001fòÙ?úGÿðÎéíÓ{W«Å%©Y]\x0012PA\x0001êY2Ûùõ¿×\x0008L\x0000t)ÞÜÜ,ë.¥Âgl¦,%Ý0bûÍÏ\x0011Eq¼·çôôpÿxoo6ßÍ÷æ\x000b\x0000xvýüÁ§þégËÕ&J
EN4FKof3\x0008ÊÓ-kç
\x000fvLa\x0010MlâI\x001e\x0013TP[¤ÖFU6°d÷£
ÚAÕ~k\x000f)VxÓÙÌ\x000cDdLÈÑ|&{Ò\x0010NMÔ\x0007p,:\x0008I\x0001MÂfq£Ãê0½HwÿkÛ
T}ó\x0008Ç¡RÁ\x001eFAìË±¡o+´E\x00108\x0004S¿ àè³»¼þ/Ø''0¢\x0003\x000cä\x001dÐ\x001b3e\x00111+'ä³´m[d\x0004A\x0010K\7\x0000h\x0011©ôÎ?\x0007^$EoxCrÖ\x0003ëª¢:\x0004\x0000rÞS\x0011I\x000f\x000e\x0016]l6ÏjÈ\x0000Ñýò?»ÿ½ù|º\®ËéôÙ³ggWeQ¼õÖÝ·ß~û\x0007þ»þgßþ\x0017ÿ#\x0000Ç·æóy>)\x001dQÝ¶mìZ«Wz\x0004¾/eDÙ\x001c°Æ}ÊõtUa+jCð¡E¦\x0006Éd2ð´(
ô\x0018¼o ¥l\x0008)H_b
\x0002\x0012Aba!O¦Ê«à«êÙ¨z36A\x0001\x0010$%ô\x0014²L\x0013+÷
}\x001bó1µ)E"hÛv½¾±B\x0011)\x0002\x0000sz#¶÷eÖ\x0015oèf¾ÜÖ]~ÁÌ¢baSÎA9ÏNOOoß¾}çÖIÓ4\x000f\x001f>|øðaL°X\x0014wîÞ=:<¼urt|r2ÍªÍfooE8±ª\x0014Eb¬¦®ëªiìTl\x0015÷a2)¢(Âl\x0000½÷V<|©\x0018\x001bA<\x0002Ä\x0014C ¨WÏ\x001e}±\x0014ªÆ\x001fÑÞA\x0011@\x0018Ð\x000fAÂÒóÛ-¸ç¯½ôþvYÌì½7·1rÂ{ïÈÅ.nÓy\x0017|0ïÚ\x0018SÝÖuÓ âd2·ÚÜ\\x001cbä¶mç³\x0000EªjbÚuéúz\x0019|yûÖÝ/\x001e=Â.¸\x001c\x001c\x001d\x0017Y»©|ÈE*UõÞq'*[Ûaç\x0014\x0004«M,Üb3¨âDcß2ÛÔÍòòl2)ÿàï|Ó¥öêìÙ³ó.\x0000L!ûâÅÕEÞ»,d>,\x000bmäuË\x0017z½®÷fó\x0004®­Ûªã\x000c\x001db8½}'Åtsu=L'éòêºk\x001b.¸öè`ÿêf\x0015¶\x0008Ùïÿþï_]}ôÃ\x000e\x000f\ÝÆ¼,¡Ùt«õåÍÅÅrDäÈ\x0001\x0008SR\x0010sóéêxçÎâòªûË¿üËçOÿ(Ïó,Ë;\x0019\x001c8XÙÑ«á=(efw°\x0015Åµm[7Í\x0010m\x0004\x0004\x0001Üp`\x0005çÐJu\x0007¤/T­êý¼¢\x001e\x0010D\x001e\x000b\x001e¨¢}?@GC<!¥-&¡¯\x0019³±m"î\x001f\x001eÕmLQ¿rÿ~µnÿûÿáúÎ·@\x0015ÅEððäè`ÿ Mñìììèè¨mÛ¦îÚ¶¾¼^v]ªëºëºýÃ\x0003ï}È²à½(g\x0019©BÓD$ÜT«(\x0012~øÕ¯=yøè\x0017¿ü|R,nµéÂ»?zvþ_þ³ÿ÷ßÿßÿ»¿ÿÛy~Ù3\x000b\x0003ö¾IBÿF\x0012­í\x0014ÞQ'
Cºx¿ùËl»\x0013óz½Ù¬7ÂÖØr¬¨Âo¬-XµmÛÈ<Ì\x000e\x000f\x000fï¿ÿúêâéó³Ëëej»\x0007_|ñÙ/Î.¯ò²\x0008\x0007\x001fÈ9aÌ]1Fá\x001du´(¸­¨\x0007vÚÐ»³UX@%ö\x000e:`xÆ²\x0014\x0000EÑv
©\x0005~-
9\x0001
\x0002
"ùàfÓiYä\x001c\x000bm\x0002f\x001eÝ@\x001d`ï¼gbÝ¡(\x0007è5ÞdÅB$~åIWÿ¶ÖÒ+/\x000bY\x0015aD\x0018¡¬qýUUÐ¤è\x0008\x0016ä>°¤ÝëQA\x0003óÊj`Ê\x000c»À®K\x0007\x0007EQ\___ß\7Mã\x001cMgSOX×\x0019\x0010ÑÍÍ
¢¶íÜ6{¿í@³KîF1z
b°­}oo~p°xQßÌf%"®.ª/¾øôïþÝoÝ}ëôç\x001fr|tâ½\x000fyñÃ\x001fþè¿þ¯ÿ?\x001fÿâWÏ/÷ö÷g{\x000bïC]×\x001a[ò~2\x000f"©oMÉï(\x0014E\x0001\x0000ªRå^çÅ½ùÅrµmkå#g±µEQGtUIÌØ¬³^ùtV'Ù°DÄØEG4Ï\x0013\x0017\x0000`Ê.¥®ë²\x0010bJÖ\x0013\x0018»FÒ²®kå()¦¶K±uä6eÛÖ¡OOÔ4\x0000Ð¶í\x001d4\x000eqB;Sf;¡^\x001f~*=Qì¥\x00182cÈ%\x0001JC¢Èoß¾}ÿþý½½\x000f\x001f<~üøìì,±~ýk÷ïÝ»wt|ì	¦	\x0000ø\x0010ªºN1µmÛÅêº^­VËårS×ÎQj&	"¨á4;ë÷ÞÑ\x001b3\x0000\x0015UI%÷¾ã6x.>øÅOÿê_þ¥\x0003»ZTRAè±²\x001e_%ò¼Å¶%^í½àÝ¿\x0010\x0018µ\x0017\x0000\x0008ûl\x000bGÀfÿ*âHUÐ!\x0010
r3ÑÈ\x0012»®\x0002 çP\x0015\x0004(2ßÜ¬b\x0002EWÓº\x0000pyy]m¤TY1{ëî¡*4mÌ\x0016\x0017WW¡´]2\x0002Q\x0008Î¹¬Ìó«Í¤¤\x000c>\x0000¨¦á9H'9$¤^?,]c¼rthS\x0004P»j3LÞ~ïþgÏçÅfµ\kX]¯féjd\x0010Ï¦³bJ]rù/¿xt~³:=88/bÕlªGrz°·_\x0014JÚ¶=þâÃ\x000f?ÉdµÚÜÜ\_]\\x0008\x000b\x0002eùìÉÓ'OL'sÊÃóËóåf½\W
sTiAÕ¹ùbv³Þ*\x0007Eî%B Yî6uûöÛ{\x000f>xqyñÖ[o]]Û³·Ý¯á#µJwk¢ãªF
\x000e06íî¦\x0000ªlê\x000c3Órº6L\x001dp_á\x0010^\x0006!Ì÷É
yÇ£]Þ\x001bR-m{\x001b2´·Í/\x001cl\x0001lUWqÞ¹r2}þôü{?øèûßÿáõr}ïî;u½xüµo~CU>ùì³«««ÙlöüÙ\x000b»:ïýíÛ'!+ò<ÏB\x0015ùÕõUÛ¶f;Q\x0014EdöÁUUu\x0014öúÓþøgOç\x001b÷Þ»ÿá\x0017ÏoÖ;÷ÞÞÛl®®¯?tV\x0014þàpï/¿óÝ?ýø?ù\x000fÿq^\x0014yðm£]« \x0014BH\x0012³k,L¾äÇt\x0007SäáÙÁ4àîìµ\x0006S/ÕFA\x000b\x0017På¦ëºW£N\x0013­a1<¾þ%\x000cMýé\x0017\x000f¢»¾<¿¼ºÚ¬×U]Ç®kÛvº·¯ªhR\x0008r¨iì\x0013õë\x0006*«\x0000G±î9z·;\x001e¶±½¤ÄÂ(}ö'\x001aO\x0007db,:Da°
ÛÅó^Zµ\x0015ÇñcTu\x0004\x0005¥Åb±XìO§\x000bGÞº±öãi4\x0001ÎxCØ\x0010.Ñû9D\x0014ìhT`½\x0016M¼3\x001d~­ÆvJ"\x0007ÚC \x0000\x0000\x0008 ¶=Lk\x0015\x0011²ï°ßK»fÐúJÕâ\x0000Ýà×[k\x0019[.¨ëº\x0015"òýïÿã?éºn>oÖ<Ï]ÈØ)a(ò6Æ¢È\\x0008ª*'\x0013Q\x001eDoæÎ½eôÛ\x0017ìv!)"%F\x00112$;,ï\x001fìýçÿçÿìã_|Ò¶í/~ñsåôÅ_~þà\x0017ÿÖ\x001fþé\x001fþÁß;?¿Ì|ûÙ?þñ\x001f>|¸Ym\x000eïÜ½|úH\x0015ó¼\x001fìGÀ¤Rê\x0008Ëö­=@\x000fVÖ\x0010úHÍáz´O6Â²°\x0010bÈ2'YV4MGÅ¢KI;Ã]\x001cí(}\x001c\x0000(ðèJªªæ2l\x0018wÎ{G\x0014\x0004X\x0004):TpÎÜkÕØv©amW7  À©\x0003:BD\x0006ÕnKäxuÌôF£;y ¿r ±p\x0017;ûË+³f 3¢÷Î97wnx\x0017/ýð{ß\x0017Õ,ó·O\x000fNONn\x001e\x001d\x001cx¤é¤)5u\x0013S\.u]7uÓ¶íåÕ¥­\x000fuÓ\x0010÷çÙ|n¤æ}n­¾¶k`ð\x000b}3*C*\x000e\x0015´ód\x000bÿè»ßáf³w²ª
TL\x000fmÀ\x001d©c\x0014Oä¼wÎp\x0012á\x0004óê\x001dDÄþ{]oHO#³S2÷Éà\x0008F É²b67MÓ4MªkUÍËÈ«b×%Vô!WÅØuü¤åù:vtµÚì\x001f\x001egåC%'\x0008¬°©[\x0000\x0008¡¨ëÎ#y¢ºª\x0012'Mà\x0008²,sÞ'æ¡l;ë¶½b0ÝábÒa\x001f«¦³RRa}øðá|:9<½µYÝ$Ê®ÛÄ]Vq°¯ëê"¥$\x0002"Ð&8»<ßÔ-¾ù¤7×Ëz\x0012¢Ü\x0004/è¼¨HJMÓ¬×ªÚ BÛ¶)
\x0000<ú´m[Õ\x0017×ËõÕÕ\x0017¬ÂH¾,1Ë5ilbbP\x0000qª}'2h )\x0002\x0014mÛþõ_ýÕöOÿÓëë«®kÈ\ó{ÖöÈHyõ5B#9SíºÈÇNPÍ\x000e:Z«b¼s
IÀe¦×Z	æ¡¶K\x0013!NR_3\x0017\x0011UÁ\x0004h8Yïe\x00198¿Z×óÅ~È&ÿüÏþç~üÓé|ÿ\x000fþàëÓb\x0014BmÖë6Åóóóº®\x000e\x000e\x000enß¹³]²É(gÎ\x0011½¸8_­Ö"\x000c ?ùÉ\x0001`¾·899AÔe¿ÿûïÇ?þÑ³\x0017gÓù~\x00128¿¼úý?ø{_<øbU5Y\x0011Û\x0018\x001f>º¸¾Z¶oÝú¿ÿ?þÙ?ø\x0007ÿîý¯|\x0008Dê©G¹3üo\x001a´»ÇÈk_ù×AeD\x0011\x0011bL­ÔÁg°ãkC`ÐXÊ/új³Ì\x000còøéº®«º².dQ\x0014³½=3¢\x0014I Â\x0012Á¬fÝ}x+æ\x0014£÷y\x0008oj-I\x001fÑ,=ìÏ/Ñ\x0007)\x0016*(Â¯ØðúËy?L÷÷ö¢0ó¸ë\x001b¯b÷?w;¡[øaÐõ\x0005:o\x0019c¯N´Ý\x0011þë\x000bì_jàî\x001eK^Jò\x0012\x0002ÚåÃ!à\x0010x\x0000à^Eª\x0006å\x0013:\x001fÕé}K\x000f\x0000{_.×Ï=!ldSmB0+\x0010·Z­¼÷e«#\x00126 âWõRÇ\x0006÷È]°MÙêÙ¬¼uë\x001f~øáååÅûï¿syuõo÷ÏÿüxðÅÅþôãÍ¦Y.×«u%m\x0003\x0000gg÷Þÿ0Ïsô®ÚT\x0005ee»à½óã\x0018¦¾ÁD\x0016¥i\x0004\x0014D\x001cQj3G\x0016\x0016Û×
Ò¶1Ùù÷\x0001>û{û7ë\x0015\x0000t)µ®\x001d\x001f®DXÍ©%Ë²b]ÕmÛ¦¦Éó<øe!Æ\x0003\x001b|0s¢¦iP!u2£hêº¦ÚÄ\x0018-hÕá¥:6^)OGtAh8
ÂË¥	ìª\x0001\x0008ÁZH£KÍc\x001ce=Õûô³Ïb×ÕM\x0015áøèØ¼dNOO°ëbUÕWW\x00175V«µA2*ç¹\x0005\x001f\x001c\x001eîïï\x001f\x001f\x001f\x001f\x001e\x001c8ïý¨\x0003÷\x001e\x0011S«Õº®«\x0018SRyC)Cjéz±mYá ­|úË¿úËy·M¯Ö+ÀdV¬´mÄyçò<\x0013Ä=YÚ\x001bxRýìí)J\x0000R|I/Þ\x001bÆ5º^¶íÚ¶M\x0011±,'Æ\x0002nÛ6r*)ùÐuª\x0006ïT¥ªë$ºX,¦7«¶uÛ-«çÏ9¢¢(êº"rMSÏò<¿Y­­xÚT0¨@AYNúÂP\x0013G\x0000 %78{\x001a¹.¶u´eC¬EÝ7ÂáóOùÛ¿ó{·îÜýñÙ÷ÙÕº
\x0000T\x0018¨ÅIS\x000fCA\x0010\x0015Î¯V\x0004Ooí\x001fI'\:õU3Ge9Ï÷Êr²©*ØuÙ=mÖë®\x001eÑÔÝùU\x000c\x0001Ú\x0008åÔ/J\x0017±®c¥UÛ #¢\x0003¥Ä 
Ø·b8	"Õ
|òÉ'çç\x0017mÛî\x001fì/×«åo» ¼.£°1`®ã1E#-	\x000fD\x0001Q"\x0002r*\x001d¡Y·ã\x0000ÕÀË\x0003}ÌÁ0¶³T\x000c? P\x000b\"\x001a\x001a
"8(\x0006¯>\x0007vwÞv]*§åÑát½é>úù\x000f?ûì\x0001¸lÿh>ß;<8jæìòòñãÇóý½÷ß\x000f\x0000Ìãdüñ$*,£\x0008_¯uU;ït±7ëºÎy\x0012Õóóy»wëÎÝ·ßý°®_<N*
ôÝïýà­{÷>øÊW?ýü³\x000fÍæE\x0004ùäGÐ\x0001B\x0010È>üêW'ÅrÝ°s\x0015ÔWÎ¾_¶{
ÄùßÈPf<<üjªÂ 7]Ç"\x001dfêÑmvg¡\x001cÅe",QxÓ5|u\x0019\x0017Q <#ç$Ë$Ïó*QÌ-f¡ð¾!"r\x000e¹÷\x00132¦s\x001378c¡À\x0003ñ\x001f\x0007£Ò~ä ª2©\x001dD\x0015SâdX¿\x0003Ä_û~!båÓétÿ`Qþ:Ê(+£*DÞêÞÝÀÔÝ8wêuRÐ«\x0002eÄcvÔg;\x001e¾4 £*
_r®@@\x0001Úùõ>eÁ¸\x0003Ù`xùgÇg:Ò_m\x000f\x0008
!\x0000y\x0015Eqyq\x0001@fb1_HÝl¼÷ï¾ûöáÑá\x0007\x001f|p÷îmù`\x0017\x0012í¡\x0005\x0011
µ\x000f¬H"¢c\x001eN\x0008¢¸º:_,\x0016DøµoüýùÿÅ³'ÏÚ\x001aBî\x001d\x001cÞ\^º¢,ööÀyîäøÖ)\x0000t)FÉdê2ïB\x00002dü \x0011xMÜQ¼\x001b«.\x000b!yý®:"FL)Å\x0018C\x0008mÛ"aUmöööwvïg\x001c\x000cV&Þ{K-¬ëÚ¸ÃÇÇÇ\x001füñ6~SL1ÅØÅ.ª¨*Ç68\x000f£©]L\x0008\x0001@P9íV$ãÓ\x001b!@Ue\x001eôSÒ¾>æw\x001fñ\x0016\x0001ý5\x0001MÓÔ\x0015"æy>)Ë·îÜ~ûí·\x000eUu³Y·mÏPNÜ\x0001w\x001e\x0000¬¦±>×í[·,\x000e,dÙt2õÁ÷(¦*!\x0012õÿ¤yîC´¶mEäKP\x0019\x0000DíbCÅL9þü£\x001f^½x¾dçOûÞ®w\x001bct\x0019\x0000hÛV\x0010ò<ïbk7ÂyÇF\x0005å»t¢Öó³Ío!DÎyoÊêÔ°å_dE`$G.Ï³Ã££Íz}y½l®<Îíimª*Ë®Kè|YN\x0017ý«µ"7müëoûöÝ·&³Ù³ÏEáX¤íZÌ\x0000ô.®¢Êà\x001cXq=\x0016¤1%+]Æïñ_Ë²,\x0008½ñÌ»Ôo\x000cypËÕjµ¼FòN\x0014\x001a\x0010&Ì"cä\x0010XV\x0003\x0010@Í0ó\x0004]"ãý}7/xr¸L²ùÁñÁÉéÞÁa\x001b»årÙ¶í$/Ú¶\x0005\x0010\x0016><9^¯×\x0017×\x0017ó½Ì·<ïóE6V]ÌmÛr0?1^àK$¦©\x001dÁùùÕ£GæóIµÙ¼ôÞ$	FW¬ØD¸iz¿ªó\x0004
\x0012COÚåÈ"v_Ò+õe\x0007¼|\x0006ýò\x0017\x0001ô5\x0016Cø+¾Õ¬hX$x¯
UÕ\x001cìýâã/þâ_þ¥Ï&¿ów~W6u½\}ÑÅ\x000e\x0011÷ö÷"óÙÙY×EU	¡ØùÈ8¶mR¼{÷v×uEQìíí\x001dì\x001f°èùåå³§ÏOOn__/ÿüÏþ§Ét.¬ôÞ\x0007ïsâÏ\x001f~¦D6ç{³®D\x0015eë_ÿÍÏÎ®oþÿíÿæý\x000f?çg]är6mãú_ÍòÿÇ\x000evÝ,bTÑ\x0010\x0008©Ïåyå\x0011Ç\x0015ÓEbD6u-
xï|\x0015EQLJï\x00032G\x000bÔA\x0019Î Î9ï}Lé%(B\x0015ú¬Í\x0000\x0010và½ñæö?\x0007ù¹ú&\x001b¢\x0004"\x001c#s\x0012Qf"÷ë\x000c9û4!øýÅlÿ`>8ï=á\x000cjéKÚw\x0007¶?æ(ö\E»mÖ
!ìæ\x0012¼ù"a¯à0l1Wî¶ý¥ï±\x0002¹¡*ú7b\x000fû\x001fí6_1=ÚuQ0ú«\x0011\x0003RJ\x0010²à»¹Y\x0015Eöî;ï¿ýÎ[ÿð\x001fý\x0003\x00008Øß;99yüè7n¶\x001dwD$¾ò¯äð\x000eúKÐuñââ2¦Ø]w{û{o½ug>\x000f ø|}SW*\x00058x|:-ÚØ!yï)zOÞ«'ë"ÙÊ?Ð~=ôÝ\x0003Ü¾x\x000c£
OfSÍBf×Ü¦\x0016Lå4\x0018¡\x0011QÓ4MÝ¬Vë²äy^m*ÅÞ\x0018À²;ûÆ)¥$"f-\x0018²LUë¦1óß\x0018SÓ4SêZD\x000c\x000e0ÏsX:r\x0010\x0002Ä-Ü";$\x0001Úå;\x0008#¡Ñ@ý×+\x0008Í+#ð§9N-úq2ÌfÓøòòbµZ¥Äu]'N\x001a²¬,Q_MäÈQ×Er,Î\x0011¹ÄIUÄ\x000b×)dY\x0008!#S]{ç¬T\x0012\x000b\x001bÿË\x0016\x0000É2\x000fÀÊéG?ø~F0/§7«g!d\x0000jj9Û\x0014\x0000r\x001fV«\x0015¢:OÚ	ÄÔ"e0Äho"¾¤Ì(Â\x0008øýH%"B\x0001u\x000eí©¤¹\x000fHö!,ËÊ©Û´©í¸kq>71\x001d\x001e\x001c\x0004}úðóýÃã|)%DòÞ?}Ñ,\x000e\x0003ùlÝ\\x001e\x001c/ªÍ&(RUm\x0000º®3\x0011¼\x0015
)õJ*ï^Q7ÄÄ\x0000ó<Ï<÷y¥m+êCª1Â/~þó»wî\x0015EÑ4
CQ\x0011TÅ¡\x0005OÀ\x0007ïÑ\x0005\x000eÕª¥çËååfýlµ¼}° ðÖ×¿öÛ×W\x0017-+#mêëßøÆ£\x000fTå­wïµm»ZmÚ¶M1~ã·Ï?ùä3¤¼âB\x000eu×.ëªÞ9é\x000f8ÃsU5æ\x00089L	êªu\x000e\x001e>|þ7ý×ÿ×ÿÛÿåO>Ñþ´¡cý®Ì\x0008(´=3õ9G6S|&ªëõº7¹bV\x0000QràX ²:O4\x0004×\x0005ç3òãö@\x0003ÓløclQ\x0018Ê¡É\x0014 )zgÆ7hVù´Õ&\x0015Y$Åè}H\x0002!dÇG'\x000f\x001f?ÿÉO~òþý\x000fONï~ûû?Ì\x0016y^Ú¤ªmm\x0013²8<Þ/r½^_^^¬×\x001bçh½^/\x0016Û·nÍ\x0017\x000bçàúúúéÓ§üâãoüßY.îöí·VªòÁ\x0007_ùá?n\x0014Þ>=¬6ÕüÉlêÙÓçUÛ\x001c\x001c\x001c\x001c\x001e\x001e^]]×ÍºkºE\x001dÎÏÏ/ÿÿåÿë\x001fý¯þÉ¿ýïý»ßÿþ÷«ö"/\x000b\x001cDC½Rïô¹ÅE-'KDµWøÚçÞÙ^Û@\x0001Ùh>8¢\x0001\x0016WU	Á u\x0005Vs@\x0011\x0005tÞeªÈÌäípÌÚc\x001e['7tHàÈa\x0000%IQ@	¤û\x0012\x001aSÏ¢¡EDPáäTÍê<A\x0002qhñ&ÖÃ`u:4¬\x0005P@DE@{0FX@¥g<\x0008¨(ìØrî6
\x001a4Ä\x0001^)£_ËÆó²,L¦Ê\x000b\x0000Õ[ÖJ\x0018F«ô	æÕ¶\x0011òÎïnù\x0003 ¸\x001dù£Npû|ÁÙ%0]èKàÜKÐÈ6ùÎKf¿Æ_5+×\x001d\x0013&+È¢H
Ø¶\x0005ûëd\x0004DÕ^\x0015%hÎù¤H\x0000\x0004J½°K\x0004Ñ\x0012	PpÎ¡sàÊ¬TU6QªÆÈúoÿé\x001fýÑ\x001föá\x0012(ç\x0017/Ðåsâ\x0006A\x0018°¨5
\x0001\x0008SÇeYvÚ¶-ª\x0008§®ë², R\x0017»ó¶Å>¢ëº¶«#RVU\x001b\x0000\x001c]\x0016fû{{ämÎ#$\x0014@I½9uÄP\x0019Þ\Ñ0G¨\x001a9!öÑb
@Á£
ë7)+ÇU\x0015|×¶¬x½Zo6uÓtDÔÖ\x001d)~°÷b!®ëT\x0000Á\x000f¾M"Hè(©$å¦jsØr\x001bÈw L>\x0010QQd*\x0016\x0013ÍÎyN\x0019@ÅÎ\x0013æ<j,1´clÿ?\x0001Q\x001aq@ó
\x001bÔjºsbÇöËëZ\x0001´ý\x0003\x000e0Ïò¢Ì\x000e\x000e\x000e\x000e\x000f\x000e\x000e½Ç³³³Ízý?6¦\x000bKj»F$ªw!÷!\x000fU\x0002Îû²(BõR|Íjµ\]Û¯+"Ë²¢(Ê²´ß\x0018B(ËÒºQDúe
&\x0015áÔ¶\x0005ÄóçO=zx´Ø«\x0017\x000f\x0016d§:ÈÒ
²èºV'ªZ\x001eYÉÄâãÙ\x0008zo/å
r5²\x000cRUiÛ®®*³ÖAÄ¶mS\x0000@çyÕv¬xs}#,Þ<Ï\x001f?~f½§ÅÁ!\x0005ï½\x000bêoAéjy³ÙÔ@¨DDÞ5M£@Î¹¶mUÁ9ðÁ\x0000¦\x001dð\x0010M9	d#AAìøØu]ð\x001e¥p\x001e	5Æ¨l»1Çnyse¥Qá¼²8+ÿú\x0010\x0006eYå%u¶\1hä´¾¸¸º:US\x0014\x0013ºj\x000f\x001f.&Ù÷?xëÞ;j³X,,ç¬iÕjµxXLf¿øåçN¡nºÕj³^o8w½A]\x001f\x001d\x0001
@ý¦1iF°©àÁ\x0017??÷>Dæb!,LL}vVÿ°úÆßXrH×¶\x001cÓîaÏI¨g|0)¾41¬÷ê~îÊßnKï¼÷þ³gOØÍfççg××Wwf{ßûÞ÷\x000e\x000eO\x0014éf½]çÌõôô¶}ªÚÄØÝºuûÖ-¨ªÍÉñILqµ^_ÇØsyß»÷ÎãÇ//®/®®Û&þßýVi]Up0ñggu½9<:<88\x000c>lÚX_Îw^\x0001q]oò</gÓïÿûu×~ð\x000fë¦ùDò\x001b\x001f½\x0005~}Ìg\x001fPEUÔ\x001e/	Î¹Ä\x00026£Õ½\x0010$,f²à½'òÎ»\x0010yW7ô2GÊ
ÖÒª£ïiÿû_²ù\x001blýTUn
¥däÞ	¤ÀªÊ¬\x0000ÉB«w\x0007Ðß~ÛúÅ
À¼Ý\x00019õ¼j³[ñ*¤R9\x0005G.\x0004ëYôº\x000fH0°æwóÎ¬\x0006ê?èpä{u<;zU·5FE*	\x000eü0xCãã7\x001b"}zÿk\x0001 Ní·üªÁ2l{YÈÈ\x0011(Ø
1àÃd2Y¯¦<!êáõ7\x0019ÞJ\x0012Á<vnß¹}}u\x001dc,'\x0013á\x001e{C$K5rDyVÚ|>«V
\x0000 ìà\x0012@¦GÙ45\x0000X¸}"ô4:X^Õ®	òÑ;z\x001f\x001c¾ÛmbL®\x0000\x0000\x0000fÞl6u]]\\\]]\x0011QµÙ=cp[Ûh~Ê\x0010QF\x0005ÀÌ¦3U\x00054Ø\x0010`\x0016ÈòÀ¬ÛÕu]×´Õz-,"c\x0011B\x0000tæ%g\x001eÊ<\x0008\x0014¶V^ÿ\x001a\±Ý\x001f|§(\x0012#¨À¤À½½½;wo/\x0016\x000bï]J±i»ÄÜuqµZ_ÁUç³Y9Lò</r6ØqÎaG*Ò¶mUUëªjÛ\x0016\ïÉÔu\x001d\x0011åy>NG·L+eÊ²\x0008!û\x0015q2-K\x0007éÿ·ÿÝåùùüøX\x001dôÙ\x000fýQ¬'Ð)\x0000\__\x001d\x001eîÏçsæ$"*²\x001boF}*²êÎRõú=R5©a\x001am#²¹m[\x0011v=+7ý\x0008"®®oV«ÕÁÑ8Ä...æû\x0007Y\x0008Y(\x00149Ë ©\_]¯ª*/óÄ\x0012È\x0011\x0005¢^ÿÆ\x0011\x0010Á\x0007e\x0019]¨\x0010\x0000àðÿG;\x00131ÊåmÌ
!'@\x0011§ê²pê*\x0000*<BÛµØgX\x0000°8ÂP\x0016Ù$/ÎÎÎÐ|TUÙ:©ÂUÇ>|¸»sz\x0004\x0000ÛÛÇG«ºé\x0012_Ý¬< cÑªéÎ/¯Ï/¯nªªL¡K]Û-×«å¥·,u@£\x0008Âð0\x0001\x0005\x0006Vñ!(§\x0018%xøÙO>þâÁ£¯}í+\x000f>´[N@ã\x0004Fa\x0000ÜI\x000c Q1\x0014SDÄ\x0018S\x0011\x0004ûs\x0015\x000b\x0011Y\x0008(s" çÈ¹Ù\x000eu¢\x0000àwø\x0004:È¶¡w\íÇÅ l\x0007å\x000eAX¬ C\x0008\x0001Þ#¯¹Ö¬×\x001füðûûû±ëÊéd³Ù \x000bóùüüüÜ\x0007W\x0016¥Mªñ\x001d¼\x000fÓéÄ®!¥È\x001bIÛ¶=>:Nìó^^\eùÞÞ\x0008t±Í¦«Mux8Îf\x0017ÅôâüìÝûï-\x0016³Íf}ssÓTà\x001dó¢p³£LçóÙ§\x000f\x001e0èW~ë·¦iÕn¼Ë\x000ei}Xè=}¶R:[Iwíß¸ÄìÌåÝö\x0004¾üE_Ù§ÛåÊ8ç¦ÓÉt:]Wu×ÅÞåmg"ë0íûC\x0000"ò\x001eU!!õÇ>Ñ¡c;°bEQÔ\x000e¶½S¯VBìcÓûz\9qJ\x000cÐ©:3}è!ÂáB0'#LÑË(ËHº\x001c\x000eQø+>xbA\x0011\x0000qÎ¯V+«DcLÁ9\x0000ÏçY5ÍÀW`\x0006 D§.äg×"3\x000b/Ò1³IÔp£þõ1cWn¨dPÊì°T¸ÿ"í¨Öh\x000cí\x001dðÞäM±'á~º~<ØÝ{ù9Â¯|éàäþ2e)ÍÎ(2ÎÙ\x001f«23/WË~±e!\x0007HJ¤HJÆ¬\x001a\x001eºw½«°¨²qíí¬Wë¦id¨\x001bRbíi³¶mÂt6\x0003 àóÃÓ'_÷*¶Á°ç¡EAh;*Þ(Ç\x001fn:ºÁdÄÐñ\x000e0\x000fÅè\x000e\Ú/ÆÞ8?¿`åÅª´]k¦bÎ¨#D\x0011\x0016Qïûäçr21®LÛ¶óù¼ª+\x0016GDR\x0008<¥\x001do\x0018B©K1ÅT¸m\x001cxB\x000bÎ¦)¦Ëºªe$ÿ¾ÜQ2àíË\x0018å\x0003Ö/a3/']\x00088é4+âäèøèèpoo®ªëõz³Ù\x0000ó.\x0004¿^¯\x0001`2,Ëó|>O¦ÓI^U QPÆÖ¡U-Þ{¥ %ªÎQ\x00162ÓÆ×uU×m]×Y\x0016¢,,\x0016á/Î#Ü_þð»ß¼ºY\x001eÌ\x0017««KÉ{\x000fH:8]n¹®êìÖiçÖfæñÔðLP\x001còÀyeÚ8ç\x0011)¥Ô45³\x0018L\x001d²Ìyßu]\x001b\x0005µ¥ÈÞgÁ¢(\x0010q>­VU\x0017»««Ê;Î.®fËÙb\x000f)×ðz\x0019ó©Yåe(Æàp´¶Hù"dh$LÉnð!nÏ²,Âé
\x0019¼\x000e5wä0dEèÍ$¦èÉ\x0003\x0006HÐk\x0006DÛ\x00155/Ôg\x000eG'pI1¢­õ\x0000­È/>{*"Åâ+o¿õôìÙ÷~ôIOgÓ¸n»âÅÍòéÙùùùyµ©ÕyqÚÆtys}½j2?j@TzÐ¸÷üU\x0015!PÊB±ÙTGù³\x0017íôÓ\x000f>ø@G\x0017ìá\x001bFFF\x0014dPT$ã¬
LFOÔ¶m[×)Û*Ñ¶U\x0016A\x0004Ña9<¬Ù"
Î»^T±òÊ3\x0003\x001aDðk'°È§fyfmÛ~ôÑGÓd6QãããÇÏ/No^\^\x001e\x001d\x001fr1OòÙÓ\x0017EQLçÓ¢(È\x001aLDt~~FD²\,\x0016!øq¾­×õéí[É¤éâÍõêàøp³©ò<Èááý·ß~ûùóg7WÅdªª1¶Fú¶&Å¦ª`½n\x001e?{6[ÌcL?øá\x000fþðïÿaÕnÈQLÑ;òäzÁº$;\x0006Û5T¿ôõæ¯.oÐZ«\x000eí\x0019»û4döãß\x0012¢mã$\x0016eçËµÑ>\x0001UÆ#\x0007³(àH\x0017\x0000~/wÎ³9M\x0019û{íé\x00080ÚO¥\x0004¦\x001c>ã\x0016\x0002jz?fû\x001efÛõ-®h«"µ·\x0017Ø9/õå\x0011¨¼d·³c¸òúZ4\x0012oµij­-\x0005*\x001aÏç¶7\x000fË 0Z\x0014"º¦éªÍs
d°4*Øz¤F°µê\x0010\x0001Å9\x0008ïÍÙìd=\x000c~gÇq"çyj\x0013
;­}¿½±\x0018¸×M;LòÊ§S\x0013­ôzZÂ\x001d\x0001\x000b\x000cBq\x000b\x000b$
¯¬Ï£\x0001ð\x0008m+i2ªætê½'$\x0016\x0001åúêºª*D`a;\x00139³\x0012ÜÞÿ¡ó\x0012Çb×=~ò\x0018£EJñèèx¶w]
>8G]TN)ÏËj³Qù|¶^×äh>³ìàZHn\x0007ñÊÊB\x0001w@ê1\x0018\x00123
Ó(Ú\x0014\x0000\x0000ÞÆJìÞCÙÁ\x000eÍ×ÃXSm\x0010±®ëº®\x000c\x001a\x0001G)qS71¦ªÚäyNäeëBQ;Au\x001dÛ#O1¶më<	®W¦\x0003'NU9\x0003ê¯\x0010\x0001Q	\x001c\x0011\x0010¬VàÄuS[D°ðà6"VÊ|ÙB1\x0016»»ú9\x0000ÏýÉÉÉþþþûï¾\x0012·]]WÕjµ±\x000b/È»\x0002\x0017Ee'''ð\x0015cZ¯×õzÃÌ)¥®ëRJÞûÉdb]ÖÉó\Ply±\x001b>~½ë:«º®KiÝ4ußÇÝõ´\x0015\x0004THMëæåg?ûÅ\x0017|öÛoßi¯Ï¥íh¬C{Ú/\x000c¡\x000cå¤$GmÛªJ\x001b;$ìRìMîCD\x0012\x0018àET\x0000$BBãO¶æ\x0012Éª\x0002\x001a9y
ÏuvSL\x000cÛØ±äÎ{çæ{\x001d+(]/ççËý½*Í\x0016{ùâìâÊ|"ï\x001d\x001d^-oØ4G"à\x001d2B\x0002"ð.ØÀ2Ú\x0003!ê\x0003|³[¿Á£\x0005\x00016)\x0000ýz\x0010\x0010óÌ,¸ÁµÁ¥T\x0000@d.\x0003uE$rlÞâ¢$uwÖÓIÜo[Î\x0011\x0000ååtusó³\x0007Ïcäë««y\x0019ò/\x001d\x001cîU·h\x0010ÏÏÏ?ûìó§O,×\x0000\x0014BÑÆtvusS5-s\x0010¼7a\x0004
«ý°v+\x0002\x00119N8-Ê\x001aç£ôÃ\x001f}ô\x001fýGÿapY-Òàõ@
ÊÒû÷T§­\x000bE9¬®o6ËÊjÁ]¹gÉ)* 1aÁ\x000c  \x0008H\x000cä\x0014ÀzóVì¡å\x0007BO\x00196»\x0011b\x0014\x0004z`\x0017\x001cÓaLö+Î¦ÚÜ½s7¦x}µ<==
Á}ôÑO?ö÷ÿ­?ýüÑãëeõù'Ý¾{ï/¾`Ð·ï½{tttz|\x0002\x0000ûÇMSÿÉ\x0016Ê,)~í+_½¸¸ÜT\x001bRhªº,ËÅ|^\x0014ÅÞ|ñ×ßþöÍjùî»ïû<këj1¹¸j\x001e?}zÿþý?ü{÷{ßûÞç\x000f¿xøóÍ¦,\x000b Z.\x0000°X,æ³ÙbA\x001f_>|x~rk¾\.oVËo~ó|Ê \x001dwä\x001c:B\x0011AÀ Ï\x0003\x0005·`n\x0017Ùqééá±éc\x000bÖ\x0019
ªbÍtû±AP\x0003 bZw ìCÖ\x0010Y\x0001\x0011IÑ¡\x0016yÈWfgT\x001eD"/}Æ÷Þ1½û¾³("z¤ä\x0006(Ç$n«Æ\x0017\x0006Ëºêµê î&µ¶«&à\x0004 \x000f&fô>òØE¨¯Ð\x0014-DÎ6Jû&Qæ$6÷úÉ&¨z¹²ÙZ!" ©Z^ De\x001dN4ß\x001eX#\x0019©
\x0003*y%×µq½Y7]=M\x0008È\x0001J g\x0001s\x0003?AóhØL/	v[\x0018ØëQ$RëQNÊ\x001518Ä\x001c\x0002Ûö=h(}úk\x001bc=ÆMwøO\x001aÏV¸ØW¼7\x0001\x0016õyDä\x0003\x0000Tëuê:æ\x0011G\x0017P"tèÚß4w®,Kï½¨8r"ÂëzÓÆ®(²Èì2gPÔ¸ÒNåú£\x001f~ô?üÙ]]^¾ûÞ{Ï={þüyÕ6Åâë_ûú\x001fÿÉ\x001f\x001fÞZ¯7\x0005JªH
Áy#Ä¦M{||l\x001c !\x0017\x0004\x0014.ÎÏ\x000fNN\x0004	ÕY´*)ïÇ\x0000%eB\x001cü\x0014E@`\x000cÉ@DQ1&ÔPÕ¹ÝÝÝþ4\x0013pïýjµ1yïDx2;G9\x0004_Uµ÷\x0001\x00119%ç=wÝî;Ø3MªºZ,\x0016ÞeÐ2Ä¾K[7]å¨
¤ä	Ù\x0008\x0001\x0010çàå\x000f\x000f÷	©nê¶m¡¯,CNº7%Z%ß{êì \x0012»UNyDÍó|6½õÖ[{{{777M¼¹¹iª,2ËE"\x0016'«\x0010B\x0008\x0014$Q+\x0012c´NDÌó\x001cRJç6¿¦Í&>x\x0003¡ízÌÉl6dÞ\x0017!ÛX\x001fêWd0\x0015ÎoýÅÿø?ïMfÒt\x0007óÙÍgwâ\x001d¦d.£c£LÊb2râñsZédtª\x0000@Î½B¤\x0000è\x001d[Æ/²m!EQ á\x001fÖIpDÈò(;UðsÕÍj6)Òb±¿Z51Fç¨mÛåÍ\x001a÷.Øìí¹º}\x001aFNÀ"Q\x0001(\x0004gèÅ T\x001eSùÄ¸nç)'\x0015\x0011Ö×iR@Dá:\x0000Ñ"dÓÅÂ\x0011Y\x001b9mêºªëuµiº(Y Ì±#\x0007ÄÂÂªÉõH>1è¦©¦Ó©¤øðÙyÓTÓÂ?}úâääèôôôðð\x0010\x0011W«Õ¦MuMÇ)¶M\5u·¬!* \x0003@'\x0008¤$(ôò(µ£\x0008\x0002('ÌB!LmË\x000f>øàG'§\x0007\x0000b:I\x0015\x0005÷ÒçÜñW\x0015;ùdäº®k:%ön\x0004TAú»ÀªÎ¶Ô¾X$ì\x0018\x0000\x00029\x001c=|\x0007
¤\x00010Ú;àÃ_Ç\x0015\x0000 ,Ëª®Ëå|>.æåtröâÙ'|r|||ssóÅ\x0017_dyçWËªmnÝºe\x0019"n6kT\x0006\1VÏ®×ÃÃº®cvrZÇX£âru½÷HNòÌo6mLÍÃGµm½¿¿\x0010It!MÓÕUk~ëõ\x001a:\x001c/Ú®^­VDä³ì;ßþÎ\x001fÿÉ\x001f#oOÛ»\²Wa\x0003\x0011#æö»Á+Ën©¸C})`ûX\x0003¾Dè¡!åÌ\x001f\x000e\x0011\x0015£"ø,8ó²-\x001c,g\x0017Ó!\x001a/T{\x0007¼ÑBSJCº\x001d!F[¼~5PÃ\x0013·J@\x0004\x0011\x0018¾Ó\x001fMúüÈ\x001e\x001f@1\x001a£ÙÀõ¿B!qêº(1ioÀÚ»¶aô&b#¹ÔË+\x001dË]ß¶\x0011ûÕ(\x0008¶í»T\x0012 P$d\x0016\x0014tÔ7HÅ)"ªSB¤´sAÃûoË\x001aëÍÅþðA\x001e¼ý{\x0010ì®Kã\x0005\x0013½zÍ;ÕXÿ¯D4~½\x0007Õ|pÎUUuyyùJ»Áâý,\x000frµ^oªjRª\x001acTArä\x0003ªª»®+'¹¼¬a~ùÝÈ\x0011ÕMsuyùù\x0007DÔÅHDÁûÍfóégþÑ\x001fýÑÞÞ^Û¶]\x0017ÍÂÌÌøÈ¿ù|.ÂwïÞýÝßû­'¯6\x0015\x000bª´mÝ4U1_¬«J\x0011¨E3²\x00151ý\x00070?»ÀÔ·´È¹±^\x001cg7ôÆ1Æ®ë¼÷ª\x001aW-\x0011q2)Sb"ÊóiJ\\x0016ó®ëº@äT{\x0008\x0013Ñ¢ñ\x0008ªMuçö\x001dBZo«Õªi*Uu\x0019MòR(´UGJ"ì\x0010JBçÇ\x001eyT2\x0003}ïýd:QÕP»ºrMÓXÚ¼qåe'ó^wµNã§\x0013\x001dâÂzfÊ¶}<L\x0019*Ë¼,KBÚl6m]______®×k\x0004)¢·Gi;»$ËéÏçûûûEYE1L{¹»AJvcã0È¯o¢w\x001c!wÎy\x000f\x0000j\x0013|\x0008!ì\x001fìÏf³¶mY¶
¦Ýi¬¤O÷>ùá÷¾ó7s29mX\x001a\x00191h'Iú³ê 0.b±XÄ\x0018Ç{aê×7?eªÚWV\x0007ïúÓs®ëI+¢ÊF\x0015³Þ|Rå\x00183 ,#VÝÛ[4Me9lÖkçÝzÓ\x001dÞRBpNF»-B\x0001TÖ\x0018£*xt9ïCWH<ÃµYiÚ»'©(\x000fÑÌºÝc\x0014ÁÈÐ IA\x0011ÄÌÊx\x001f|\x001eæ³"ùjS¯«MJ±Û0ù7"®CJ\x0000,\x001a\x0005
\x0007ß¡^-«¦Â«Ëå³³\x0017ùge!³¥¦mÛ³³­óÐ1°9\x001d'VE"§@¶\x0017õ´\x000b\x0004ËÐE\x0017BhÛ\x0017E]ÕÁû\x0017ÏñÉûïÿ\x0003\x0000iÛZU½w¯¬×¯¿b1¥¥ÈBË\x0014
<èÝ¬Ð\x001926zÒ[\x0002\x0000	!ô´â\x0001ðëÓS_\x001d]û{{U]oªÍÁÑI]×Ï>kúðøä»ßýîÁíÛÜyç\x0007?úé½wÞÏçÅ¤ìºîáÃËårµZ\x001d\x001c\x001eÜ»sw>D$O ìàúúÆ>Áf³á\x001d[º½½¹¢¬×ë¦­²Ü{ïÊÒýkoøÁ{\x0017\x0017gÞÓ^>Ís\x001e_<?¯6Iî\x0004!vZá\x0004äC\x0010YbÇDþç?ûÅïýÎïåeg¥\x0005\x0018`ÜãiØ i ´Ù_yOv»*»{ÉopYÄsDy\x0011fâf¹$\x0005=FÞK\x0000\x0000\x0000IDAT\x0001\x0011ãÄo\x000b.\x0019ßÙ\x001cl\x0008X\x0015«¢Éª~5×¾#*ªÖDS\x0004í
õ	Á;\x0010ãë$9v\x001eû\°!ï\x0015xçÓ\x000c®»*,¸ãN¸VÇ Y.ÐÝ´ÞÊ\x0004@\x0001ú\x0016\x000c\x0000XÙ½½q\x0003@·õ¢¹ÞW$ guD¿@\x0010	*Ù+¡Éïú\x0014n\x0004@b5Á,íþW\x001eTß6±boì\x0003ÚE}üüºûõ_õÚ5\x000e±×.Ì`ðwÁgYÛ¶u]«ÚÂn\x0016p>Ë2"vÎWU{öâ"ËBv«ÈBç¥!LBâÐ¯V«¦iöqÞ@§\x001e.îOÿÞ~ûíýýýÙùy9Ìºéôzµ¼¾¾^­VMS§\x0001\x0004\x0000ç¼s¬½ºÑB 2/\x0016óo~ó§Ç§?ýùÇgç×Ê,Ê\x001c5Æ´çëªF\x000b»\x0015\x0018}ü³,\x001b\x0003\x0004Ç÷ïq*rHd»Ûa.\x0001\x0000sb6TI)µm\x001b»Nz'_
!÷>\x0018o¹±³xwç½Y:rLNµO\x001e´6íåxvvV\x0014E]ÕÕ¦JÜÅ|¢Y9Í'y[7D8\x0015yFDè`7æ%ZSÉ9Ê)wYæCpYæ
\x0000©»\x0013jøP°\x00123Ç\x0014Sb\x000b
Øýªª6Mêº¶mÍ-\x000bYÓq*ó+½q(c×u]ÜÔmë£#*Ê©\x000b¹\x000bà³Â*ÂþðDÖa$$S×uÂB\x000e¬\x000crÎ¤.6VýÌå\x0018<"vIB1\x0001 8Ñ )h\x0007ÿào\x0002×Óà3õòz±X¬×« ,Ö\x0018²q\x0019c³Ùd:´m
;\x001e\x000f»sc÷5\x0012\x0018e§\x0007I\x0000Þ¹à½ªFsÑµÇ:P¶®ªq\x0006\x0004º.vIÊr:Íë
"\x0016Eq³Z{5M¼Z®|1\x0005r¼)v{î B\x0012\x0001P\x001e¼\x000fHÄ"F\x000fì±;Fm/£\x0012=º\x0003;>ªØñ
ÓpSmH¡õ\x0019:\x001acî\x0004\x00153ýé\UYQ\x0010:O[F­X7³(²º©)\x000bGÇÇ7çÅ$C®i¯Î«*Bð\x0001\x0010!öI\x000bÀ\x0000èÀ'\x0001\x0001ÔG@\x0001ATRÙF\x001d©*¨w®­ùx¾¶ÝÍ\x0017Ï³,\x000bmbdI¢ú·	HEëªJ1ÒÎ\x0001Ë¸ýÂ¶Q
OYvzØv0\x001eª\x0019\x0000ç	QØÜ¾è1£\x0016\x001c5t@\x0015eÔ¨î¦öZoÖï½ûÞÓgO/®nnÝ}ç£üâó\x0007OÞ¹ÿÕ_~ò I\x0000X(øïýàGôGr~y±\.\x001f>zâ¼M;M¿òÕ¯8r"zuuyt|\x0008\x0000\x0018\x0002\x0000¤>ýôÓÍzMÎµmk EQ\\\\x001c\x001f\x001fÞ:=ö\x0019^^\\x0014\x0019\x0015yðÿ\x001fü;§wî~÷;ß-2¿Z­Ê²8:Øç.µÕ¦Î\x0000àfYÕU\,¦×WåtÂQ\x0004G\x000f\x001fþò¿üÆ7¾1L®n®óIRB"Iil¼ÊÑÝm-½:Åv\x0012Å^ºðú_zmKI%\x0001ãB\x0008\x0001&BÍÏ2ï	Û>óU\x0005TÕ3­ÑÈ}!ËÌHD
¦5B\x0012\x0010Af2õ¯"âxiØN2ïæÑªZ#\x0003D%¥ä\â\x0011EPbÝ\x0012ÎPY@A¢Y1w1&<®3_\x000fðûóú}\x001e\x001eß\x00151Ò\x0003¼f\x000cß¯\x0012C	\x0011ldãpð0® °*¨3\x001f]Ú\x0015(moÿw\x0000\x0000\x001aÚoHèwÔ ý2²ã¸3LQ\x00186ß\x0003\x0000\x0017<Ëî\x000fÚYJðÁ$TDh£x\x001fÓSU\x001b\x0011ÎóüèèÈ\x0007ï\x0008cj¢X­ÎÓÅÅ\x000bÛ\x001a÷"	\x0006\x0018\x0000¶uëÉ\x0015Å¤ë:¢\x0010¼7LTU\x000f\x0000ÀçYÛ¶³Ùl½Ù\]^\x000e+	\x001b0³{µëÍzµZMg³½ýùí;·\x0015¨ê~Ü_\x000bä@$ÂÒ´((W½\x000cOs´=DÄa}\x0001c¨À\x0008qßi{¼\x00158)Åfg\x000c8ç²,¬×\x001bï\×EDr.\x0011¡\x0008;èkwÆ\x000eÎ	 X¥d^yy·]í¼s¾d^·m=yï\x0008w!Cç<9p®o:;rHZ\x0016Ù¤,¹#³ÎÑÌ»Æ\x0007ç¨r\x0017EaÛ`}É¿iëY°;\x000c\x0008IIwAý²cÍ®ëV«\x0015°ø\x0010²Ìåy>NBðå$Ï²lZLh6\x0011QUmËåjµfº®ëº6©reDhn·&(\x0002\x0010Bp\x0018|hê&1§¶µ*-Ïsç
à9\x0018y£båHªpv~~ë`^bÄ´æúóþÕ\x0007·K^_¡âÁáüêfU,öê¶RN!P\x0017ÙÔ%MÓ8ïæ³[Îcª\x000e*\x00032Ùó¶-
·÷\x0005ùMÞó Òû|Ä\x001cyfIÊ@æù hyÅ"M\x001bË¿ºY­«zÿ¨î"\^\x000fY\x0001ËäüMLÀÉÉÑùÍuÓ4É\x0004\x0003"tä{ikØÙUQ±Ç¡UA\x0005¬ÇÚ#Qæé\x0003*½°\x0019@	5õ®\x000bXE$q\x0018'\x000cJ\x000cèÈ!( CbÐÓfS\x0013að\x0019\x000fk\x000bÆ¦
\x0000`³^,k"£°\x0000f\x000b;¬Ìi\x001cr{¨w{\x0002T\x0000eB@\x000e=\x000cÌÀòÚOç½õSùú\x0012òéôë\x001cY;VÍB\x0008ì»+!
ËåºëºeFé=Q\x0014	\x001cJþ\x0007PU^\x0003\x0012H\x0005\x0015Qlµ\x0018kq\x001f DÐ³#Ìâ\x0002wYÀØç\x0000\x000b":¢à}dib¹ÿóg­äX=x¾©º£ÃÓ\x001f}ôÓ<Ï÷\x000e°mÛ\x001càèôääää`±g\x0013)óE,qsõüäòìüÖ­Ûï¼ýV\x0008ÁÖt;Î&EUUuWOò,N'\x001cÛ\x0016d±X´õ Ý»{ûêêê¢­»Øzò÷îÜBM7×7Åt.\x000c\x000eÒzU9çP,³-åäðô/þçõö½w§óyeÞgçç§·OÒ ?5Ê¤õÚÑ@0Ak$\x000bq8Aß¸cõPÇKË\x0013Èv»ÝuÐÞ\x0007\x0006e\x0000P\x0011Û@à'E¶	Ô¶­³\x0003,\x0008£\x0003e ò 
æÖf!M\x000e°(,\x0014\x001cA°Àa\x001b¨IUÅN,IØâ¢ÆÀq\x000e\x0000£\x0008\x0011(è@ã\x001d¶mVUS?¸EEA\x0015a7©@ÜB¸ÅwKÒÐ8IýA«Ïx±\x0003:rÐG¨ífª¢(ªú§\x0008èÀ,Î9ó\x00065\x0002ÆX4XÌZ6¾Êk	éÉt\x0000ª\x0008\x0004y\x0008	ê	F }â)\x0005`ÄmÁ>(|ÔI½´ð©{µ\x0001\x0000}Rt×uv\x0014äAO!xUóVéFD-\x000cIëõ&¦v±7ûûÿ\x000fÿðßú{ÓÙLU²\x0010n¬è\x0001Ñ{RBBïó¦é\x001cQQEQLg³ÃÍº""MP¢ëÒz]IÔÅbñtý\x001c\x0000ØÿTq1ß¿¹¹Îf«Í\x001a\x001d±êÙÅùô`qzzzy~­Àù\x0017/^¼óÞ}5\x0000\x0008:U\x0012\x0004\x0015EGªjv&è\x001d!:ÜªÌiSÅü`l!\x001aÂ¢ÌYCð)eE!ÖÙ\x0001\x0000\x0011)¢i.ööö../sy\x0013Yú`ª¥¾Ù\x0000\x0000)E;Øïíbg.ÉDU;ßRÛFOEº¶Î	P9!©°*G\x001cBÓÊÜMËPæ®®Z
\x0004Ó2/³<\x0016±irO\x0008|Õu;z¦av\x0018gÕþt#\x0008")ZVª§a!QîH:T¿7l-ï]YdwïÜ¾sç6"n6ÕÐ\x000fEÓý\x0001À'OUõÖ­[\x0000çùfS©j¹\x0000 ÊM\x0013³Ùl>Þ:~ôèQ]k\x0008YQd=O\x0004ADc\x0012äÈy\x0005q¢\x0008wï\x001cw«%æ\x000cÓðóõ¯âæbJ=sÇ\x0000"`ð9\x0015mìF³Kï=":ÂÙbjÊ½Ãr1ÆØ!öf-£3HÂõW´]p\x0005 \x0017¨Ù´`\x0011aØr\HQ½sÁ;UmºDNDµiº¶ÕfCÞeYffºÅD\x0019PÈÂ\x0010\x0008\x0008×U%Ú'`Ã\x0010\x0002ö¤Þ]¶öH¥\x0014Àç;.&#*óe/f&@ÒAIÙ«'H\x0008(\x0008÷\x001fÖ´ÞB
(:j,I\x0001´¿2§[\x000cHÔÁ«\x001fPA\x0015y Cô)
\x0008\x0004
\x0018Á\x0001\x001a-p\x001cº\x0008\x000eÑõ²Ræ¼\x0008U½\x0014º®\x0013sâÈºõZÝm\x000f¿üê\x0017Ds¡öÞ±¾¨b'§q¦\x0000°ô"(Ä]L`´Äf\x0016\x001b\x0016æf½}+Kêñ\x0017µÀ\x0002ûÌ¢:H¯\x0005\x0000ÈÑÓgOYàöÝ{?úÑO½8¿Ú´\x00177u4vBJE9?<>Ï§æ-Ô4\x000fAU®¯®öç\x000bDtÞ3Ëb:ûùÏþüùÓÅbñ{çwïÜ¹]\x0014År¹¬ªÊ¢3e±XÞ:)&9\x0000üò¿\x0000\x0000gY\x0016\x001e?y´XÌ2\x000foÝ½ÝÔ\x001bÛUôho\x0007ï³¢mãó'¡(2çÌÍÈ =(&óç/Þ}÷íà¼$¾ÿþýªÝ\x0010]ó¥ÝÛøzlÊvYÄQå¤/U3ý7ìþT·wþÕ¦*!xÌQ¹Ålzsu\x0019\x001cFfEí-ýDú3÷ðÄû£®Yh\x0018qKGù·¨\x0002Z¬´XÌ²\x000e\x0004WÜê\x0006!Ò+×?ü\x0015Äd\x0003\x0008I{:\x000e
Í Ø\x0011|Ùëõ½¼ßþûß<Ôzý\x0011EF³Qk\x0007\x0000;Á\x0013 â6\x0015h7 £ç]ZÌ{\x001f4Moò¼ÙÆ\x000b¡>²?"ëhh&j¤ïWï\x001en\x000fÓ¯Oç±Ç÷ÚY\x001cÇqÑïÐ/\x001f\x0019\x00044h x<Ï\x0019Táý÷ßýÿø\x001f¿õÖí[·O³,KÌÞt='²,ò¬$)EfII
\x0011æ«ëëà3"ÇRâ?yø§l#4H\x001c	ãt6t¡Èí°á2/
1Óm\x0005Õfy}©è4i©¶BH,\x000cr»%\x0019NÈÂ)JB4bÎ¸\x0012Q\x0008.\x0004Ïº.¦,Iv!EXDº®+Ë²,K&ðÞÛ \x0007¢\x001aôeÍ@ô\x000eàÄ½lDô.³h\x0008++Û¶ËpqqQ­©etÐÖÍ8pÂ1plcãb×²u¯|CÇ¼p
\x0010SuªÚ%ó 5_=\x0018\x0008\x0008/ÑáIE\x0012³Âv\x0001ÐhC\x0011|pÁ\x000f`\x001e?fô7Î2ïcÛyçs½.RÈíÍ\x0017yÈ\x0016³¹éÔò\x0010N&å$¦¶mÛÄ\x000cµ\x0005 ªy\x001f\x001cî©êl6sÎO§Åééi\x0017»][&{y\x0017Ù¦à©\x0000X6\x0015\x0014\x0019,/¿ýí¿ÚTËÙ¬ÌsÇªÁ\x0003¢\x0012ªzïB\x0008!d¹7\x001fÌ¶+CpÓÉÄ{É0\x0019Ó	;ç
KäÁ4B¾¤ëôò¤²ua\x0000T¥ÿ?TG
XUuSwà(\x0000UmÓFæåz:-Cµ
3è|>¯ÔiÂà\x0001Ñmêä<Ðlá\x0015Hæµ\x0017
5\x000b;]ª\x001d\x0000y$\x0005\x0001(é«\x000b_ÿU}yË±ww@\x000e\x0001\x0014<¹þ\x0014\x0008B$â\x0011\x001cØ
J4Ú\x0004X?_\x0000DÁ\x0013Ø\x0014\x001c\x0002\x0002ZEå\x001c8\x001b¢¤$\x0008 ä¼*\x0012P1¸\x000c@bÇmËûsX,\x0016}©)TÂ |\x00119¾b2K§øJ£GE\x0000Ulî©ª)D9%ðÞ\x0011âî6:l!
\x0002¢
¿.Í÷ÕW1\^^Ïæ{äè§¿øY\x0014Ïê\x0000H8ÆØÍ'óÛwîäe\x0005'fi\È\x000eOo\x001dÌfÓºÌ;N±©ª\x001f|÷;y\x001f\x001f\x001fçy¸¼<ûè'?jÛv±XLÊÒL'³,k»\x001c\x0016E\x0016\x0002ýé\x001fÿñåÍååõÍõõõ;ïÜLËÍf-\x0012ßº}Úu±ª«Ø¦<;Xñúúú{wB>EçRJ\x0017×\x00170tÏîßïüâl¿îÚççÏ³"ÜÜÜøà²,\x001b\x0011/\x0018÷¤âC\x0001¬]÷·¾v¿ç7ã#\x0011Q\x0016\Ìü¤ÈööæM×ÆM\x0003ªBÔ{÷*+öx\x0011ãå8\x0000HÊ"À¬à^\x0015
)èH	|¥1mßã½\x0013ð\x0012\x0013¡ù[¾~Í2Ö`\x0002=ßÆrï\x0004DõË?Q/îñ~R A\x00152\µ5l\x0000\x001dì° {EÕgCQR\x001cÞyë4\x0002K#
\x0000æ^ÕÐ½úÚ=!ØSN;BÙ1\x000ep »¼dZøÒ\x0019
\x001az
\x0011ïéJoþ)ÿÊdìê{£\x0017{ùà¼÷!£ßýßý÷þÁ¿Óu]Jm×5¦9'ç²,sà×ëu]Õ,ì]PÕ¢(\x001cÑ»ï½wÿþý³³3\x001119']×Å®+KòÁ«ª\x0001À\x0000à\x001c1\x000b\x001e\x001cjRq"I¢(
'\x001cM ,íz½¼É&S\x00002*º\x0010Á\x0000h%NFdBêñ$ª»\x001eW~$°#}Ùþ\x0005fyç\x001c\x0000XÛt:=::Z­VãÐ>oÒL\x0011`«{°±êU8±\x0015ô1%GÛ6bQX,áK\x000cét\x0010\x0002úá\x0007\x0007ë¥\x0003ª'kÓôÒæ+$\x0008ÇãlÎ¢)Åªi¦Kû6ö¹ÏwRíÇ­}\GÃá\x0000	 óyÊ¬éì´16]ó¼m®Î^,\x0016£££Åb\x0011¼\x001f¨äÂóéd>kÛöâòB8IY ²Ê¤\x0018Æ¿\x0000@OqÚ¤\x001c	Ä¡æ·~Åî8WU/Ò\x0006Èb×äÙä¦kSªüÓ=LBÛmæ¹\x000fè½,§yb	\x000e\x0011Õ;¯¤>ø,óÓÉÔTd*ê\x0000ÇLË·ûûv§Ê®ÁKªwP@\x0002%VC2¨mÛår¹©¢(\x0015©mâf³É²ÌDÆ!sO&ËúºëRÏ\x0014-½±ù×§Ê"4x\x000f[\x001d\x0002òsÉp|ìSÎ\x0000h|,ntX¡^²¹\x001dM*p\x000fú\x000e&Âã\x001a\x0001f»'Æ4&4%O¿rA\x000fCô«\x0018"¥\x0014\x0007[¹íÿ`<\x0017\x0012Y7]U\x0000U\x0008±oR°¦\x0000QYY\x0005îÞ;x÷Ý÷´¥CÝiDÄíY^=Ã[¼­°\x0008:\x000bA´c·\x001a-Ó@¨\x001dF°0\x0012\x0011h¯\x0014WÑí ª@äXxÌ¡\x001dÑ]cÌ\x000c\x001f\x001dòF{\x0004\x0002²,³¢\x000eEþüÅªéÈyE<999;¿f¦ùþþ½·ß~vöâé'mÛà\x000f¼w«õjSmn\x001e\x000bKSUmÛÞ¿ÿüüüÉÓGåjµZÉ[oÝ½{çîz³\x0016ª®×ëõÛo¿MÎ1'féºn>îí\x001d¬ÖmÛfÎÑtvzz|þüESU\x001e´ÖÊç¥QÓ>\x000fèçóåÍzõüùóUU[Úr¹¼¼¸å\x0007\x001f|ÀÀmÛæE°SkSî\x001e\x0003¬qh÷ê
½q¸\x001d°;\x0001w¾DÛ¯ì¾Ñ\x000cÊ\x0008Ç\x0018Ï2?-ó2ÏÚºP	Ñ¡Ò6µX5ô\x001dÂz5¢°\x001f¯E9Æ¸]"\x0004ûAný\x001aQYÛÄBÓ¨ÏÁS\x001c\x00175V\x001ewQ'»;ôîMê·¥\x0001\x001a\x0011\x000b\x0005î	*¨ÞßÒ\x0013\x0018\x0000H\x0006|èµ`|9D(8#ì\x0014"n0\x001fG,üÊ×pÁ/\x001dtàßõà5Ú\x0006äéM\x0003wÔç¿ÊE\x001bÞò
¨á.òÚEô=;\x0010$¥\x0012g\x0017Õàýº÷Þ\x000f\x0011¦J©õ>X\x001bÈ	CÛV]×Íf³ÙláÑ©V\x0011	s¡ëÒÕÕÕááQ\x0013§ýýgO_|ûÛßõÞ»àaÈcÚÛÛ÷e¿K)Ë\x000f!Ë²ª²:Qúa­
Àu]¼\x0004B`Q2
Èàz>¸x[4\x001dYÚå½\x000f¯÷>\x000cí1¦®ëÉ°(3´ìºÎ\x0000$£«h\x001b[ÛþLÓÔuÝËÌ61h7ta+Ñ)©q{-åºÚ®M\x001cÛ2\x000bÓ²HUîçeá\x0008\x0002Ø\x0019\x0018È\x0011&i7+\x0019¥\x0014\x0010\x0002PNÎñt
Ü\x0001¡s¾K±ëºårýJ\x0001=\x0007£Põ$*\x001eÒfú@§^ï\x0006ÞA\x0011(x`îRÛ¶UÕ4I\x0014\x001cC>Ü\x0005§ Q\x0019|\x0008Î¹.Ö*/Ë"w\x0007{³ëó\x0017OÚzµ··7MAD$Y6bäÈkÙ\x0004o÷Ø4Í`Ê¿³èëç«ÙÁ)KìÚãv7ßûþß,×ç§ûÓB\u}=ËÕú*ÏÊÌc«er
Î©*wÉ\x0001îïí\x0015!$\x000fMJ\x0004à\x0010S\x0017\x0001`ÀÄ¨<	l5&ª£HoÇ&*JªÐÃÄæ{áÑ
è;X7½KÒE6ÂQÛ¥ÕjSw\x0001#*]Ïööì_Ñ\x0011\x0005\x0007pÒ$à\x0003x\x0007\x0008\x0008Ú;[\x001d¤?¯ví\x0004²=«N\x001b£\x000b\x0000\x0008CJ¬Îª8 5Ï7\x001bÛèói»C¹U! Ù]ÅúUb<_#ÊßõP\x0004;éÙº6ÂÚ"`	
4ö³°W\x0005o=}`\x0006ã*y"\x000bÃëºêùþæs/öï¾õÆ$©säÈ
'I\x001c®~WÞ³
H\x0015e\x0016G~¸~Et½ÐËXÀ\x0002f)È(¨&ÙE6Ã\x001eØêuUT\x0018\x0008z/\x0019û)\x0001\x0018B\x0018lcÞÖ¸Cºâjµ
>eù/ÿêÛóÅ>¹É¦\x0017\x0017WW×ª¾uzûÅÅåóggO>:<Ük[ï\x001d\\\\x001f,æ÷ï¿|xðàÁ³³³ÇO\x001e)óéÑáWîP\x0019*pbç]e_ýàÃ«ëëårRDUR(³|2èÁþAº»\x001fÞ¿¹¾¹¹¹9><À¾ñÕ¯]_4Mñìé³ª®U¥ P«êªê*Ë{·î¦\x00189Æ\x0018SlêËë?û³þþçÿ4/³Ï\x001f~q³¾iÛ6\x0004HÔ\x0017\x001e9\x0014òäb×Iêa¬Ñ\x0002\x0007ýPïò<\x0012h^Òí4§FR<(í¨Ü¶²W@eRñ\x0004yð³I¹UÕÄº\x0001I \x000e8±©)È|È\x001a\x00104¦Üß\x000cÒ þNÌ)F\x0005|ß~yó¬ \x001f\x0019 ¸Ë zy³\x0017¶Jæà@¤WíéKïF\x000eÉ2»X\x0011ÅC¤¤líÝþ¾õÐgO]\x0007;§\x0002\x001a-fÄW^y³/oë\x000cÇÊÞBéÍMq½t[°_t\x0004\x0011Ù\x0007<íLñÝìÎ\x000cå¾ò»@uØñw^<®'ÛfÓù\x001c&\x0019Þ0Æ\x0018cGTªE\x000b\x0011¥(O<5 !1Ê@o,+T\x0011ÑÅ\x0018ÛØ5M}vvöüùó¦i\x001e~ñ¸®Z\x0004gh
s\x0015£ð_þÅ_ýå¿úëý}ëð¶më\x001cÓÉïþÞïýïÿÿ§OÅôhÿxµZµu¹ÜA}rròôñÕõ\x001aDÃtv}yqppìC\x0006¤\x000c½\x0008a,óÔå¼sDÎÔd¾7õ¡\x001e5FW1¥\x0014c@\x0015Q;ÃCÝ9Ïa6Y±¢*1Æ¢(Bð,h÷D%\x0005çD\x0014@PôÕº\x0016Ñ M$hY\x000eÐ!rìRSIL\x000f\x0008âT<Rð\x000eÀ\x0004Â¹@Î\x00019\x0001\x0012®õÞOr\x0007Ó)\x0010:ïE%1ß9>Úu\x0012aa\x001f\x0000\x00055cX\x001eÊ¾\x0019×;ëôÐ¥p×uMUU\x001b"7+C»Y§ÖÞÖ´¦i¨,Éd:ÏÊ@×ç««³él2íïíaï\x001b\x001eJðùÆ$¾HARZß,÷H;¦ØVÊt±1vU]O\x0002®7×Íå£\x0007\x000f>)ÊÄ¨:-3Ég¤\x0000É{çylÅ\x0006q×u"R\x0016E9)×ëM\x0008¾mû&®õ}í@æýöW*ho´½=imgÝK\x0010³\x0000:\x0014\x0004\x0007\x0004DRÜ1\x000b³óÈqÒåæº®jA2Ó!\x0002g°
#ïr\x001fT0	tàÝ`õ
Ã>\x000bÚÓxÿÀ_©`Ô1\x0007\x0000%\x00029\x00027\x001d\x0000ën"xÆ+=\x001aUÖm³\x0000\x0000Thg)	ÎeYfþ°v]#22\x0002<¦ñB\x0004ïÉ
¥\x0018) "Á«\x0001¼\x0004
|ÕñV{çÉA;Ñpÿþý\x000f?üðÅ\x0007\x0018z;-\x001dÒ>\x0014ËN¹E\x0019\x0008\x0003³`\x000f¡? 1\x001eWT5wt%õª\x0000TÑ
v[J\x0000
\x0012f§¤$*Àà\x001cª*\x0001\x0001\x0001+ \x0003§¨Ì\x0003q \x0017lE¼\x000f\x001f?ªë\x001aÝL\x0015».UU-*oÝ}¼{üèÑ³çÏÍ9v2É<}z÷ÎwÞyïðèèÙÓ'ßùîw\x001eñ ÌCYdáö-çñæú\x0010³,+'å|6òôéÁÁÁl6].WÍHSb$¼sçÖd2½º:È\x001f|ðÁùÅyæÝÙ³ç\x0017gÏ\x0017éâ{WWç±^¯®Îó\x0010¾zÿÝOÎnnÍ|Q~ík_ÍóìÓO\x001f,¯®æóiâ(\x0012ÿæÛßþ_ÿ'ÿñ7¿þ
\x001fèâúê³\x0007\x000fDX
ÿ¶Â\x0010Ô9OÄ(9çFxcûè	FÞëî\x001c·¥\x0011¯\x0018þ\x001d~î
C´* bæÃ¤(æ³Ù¦n¹é"*ã8°uëm%8³\x0002ÀxÄ¼>·Fã_f\x0010¶ãà-j{`Ñ`"(\x0004dÁF½÷£*³²\x001b\x001cÊF·3~3íò\x0000\x0004À[1
b¦\x000e\x0001]"	íø}»\x001eDéQ\x001cbD\x0005)Å.1\x0013sâ$\x0013sÂh,l¶³ÒhgåÈaýs\x0008¿ÞKEq÷¦×¯h|ü­ÿú+¯vuãWÇ¿ê8 ÌÂ\x0012BPårÙ¶­\x000fa\x0004lôªêÝ;w///?úñG<®VUéòòâÙ³çª0ÎNNN¶\.Eøèè\x0010Á­ªUÓ4Yu]×¶mL1«67×7\x00000)'\x0000h<Ï#¢sÁ»à¼\x0007ï-ÖÉp2ËÐ#«2\x0000«2èòä(Ï\x0018¹^J¦ÛbÔÀ\x0018b¶+§Ô;Q\x0019lc	£±ë²PÕ¢ðÆ¡ñÞåyn¤¶«yÈç\x0019\x001bÌ[£\x0004¤<ë\x0006¼L	Ñç91ÇØVËuW­0Å,8/¨I@\x0015\x0015=P\x0008g~\x0012ò\ OH^\x0001b\x0012µfyfè\x00018\x0007\x001eÇÏ>ôÖpãå½<ÆòÎ\x001aEDï½%0\x0018JmøkJlMXû8Ì"\x0008ó9\x0011UUÕ¬¯&\x0000d®ë\x0018RÃ
.¥Ë²Ì;OÞ\x0011(Çv³b{[ç½n6\x0010ÂH6\x0016¨úØÖm×%nªê¦M§ÿô£G\x000f?}ëhB±"À¼(Ä§ÀÔF×ÅÄª!8\x001c\x0000Râ"\x0000Ìæó,d\x0000\x0010sÄDÞ{\x0013VIßý%D\x000224êçÆ@\x0004Æí=zÃLÃ>¦\x0001¥n6vÆuDýØ\x0012Î³#sQLÚïÀy\x001fJ\x0005jR1Æ$!ø,\x000bºW~\x0011¾ªëÙ-°dLü1^noªÀ\x00021FFbE&på×!+ô¿ÔÙ\x001a\x001b`\x0018Á¬\x0016]éCð\x0016»º=6\x0000¼K¥Ö]"\x0002ç#'ÌÆùµE3óDÂIT=\x000b>|5Æ(¬f¹WN±ë\x0016ý¢¼Ôkß9ék|\x0002{u»Ä]b;?¨å\x0015°OÓ\x0005\x0017\x0015\x0000!\x0005PVDU"\x001c1æÌ
¢h.·\x0008j¸^f½£'7\x001bÿwË³Þ®âÓO?kS,IëºZ¯WýÃËëå§OUäðè(\x0004çÿÖoÿî»ï¾Ã±ýÑ\x000fô½ï~ûüì\x000c\x000eþÞïËÀðÃ££2ËnÝº-ÂO>Íóüòò¢,'·nÝ\x001aæjJ1^\]÷åtzrr")ÍÊéÝ»·îÜ:yòðQp>6õ´,öç³Y/öfÅâH&sÍ|<Ï>»<q}UJE7\x0015?}þ¿ú«¿:<9üàÃ÷ßáwîÞ½ýèÑ£ë««år=p-±/jPU3 $fM]o!J#Paþv¯¸ÁØ7¤CÅou8ø/p#ÏóÅbÑD¬×*
NH\x0000EXÈ¼P@\x0010Ìwqg3\x001cäJ:ØÖÁ\x0000xôßðrWzü{ïß\x0005 øêçRMvÞyEQqglG\x0003rÞàÃ\x0010
ð8qhÛKO¤E\x0000 ¡\x0014cy\x0012;@\x0002çÀ\x0011:\x0007UÛ?\x001c§ª¨nDe@\x0000Á{ì¶4ú^£vvü0¯pò¶÷`û_Ò@½Fj~©2¡/\x0011èãän;wÚuMç"©ëºÉdâ\x0003^\^pJ!xç^\x0015÷VUµ\.ÿâ/þåw¾ûÝy9ß?Ø/Ër:¬V\x001bUuÞgYÖv­ªN&SU½¾ºébRBÄél:vjRâÕzÕ4
9\x00023®RåÙ{ï÷Î\x0015y&LYb½\^\x0017E\x0011|öÆû;\x0008RU{nlu!Ì)Æd>o»CQÕÂ4Ø\a¦qÎ·m\x001bqaÃz½ÞÛÛ\x0003\x0010÷®oxðú&
i\x001f\x0018ÎIXXØ\x0001"Ø¶N4]õpv%GÁùÌÌSF \x000e@½Ñ`RGê]@TM"\x000eæ$\x0006xC\x0018©\x001d\x0014©ú;(÷=÷\x00051Ë2çÈã69¡(
QíÚ³,³#´Q\x0011|\x0008¨®ë®ëÌ\x000b´®êº®\x0013§>º"ë½
®­®ªj\x0000 ï\x001c**sLØZ¥hRvUñ\x001c[LÌ\x001bj7	ÚÔ­?úÁwÊàgY&]íÀM&zSM¦6âÕõÛ\x0008\x0004Î\x000fÅò8)s\x0000\x0008Á\x0012q¸\x0014UÝÀ[6aá·Ð×t::ÜïL3z¥\x0000ÜMò\x0014Ñ¤ÒÆ®ª*f\x0008Þû\x0010\x00180dYÈ2D'uÍª\x0016s1&\x0017ú¿0sðä|\x0000 Do¡Q¶çáËäÓ7¾(³;­	Î\x0000-[nøGBaÅßMùB\x0008	=ºàýë8ðËC_¸7\x000e\x0004è9+Vx!"z¢à	G\x0000À\x0006\x0007Úu]LaRN²pVÕ¦®«årùüùó^Âc\x001cLxuj©ê¸±HÌ© ôº©f\x0014¡÷B¤íN\x001c2\x0003önÙ\x0000	bÀÀª¨ÂC>°ëý\x0006Q\x0001pHé]\x0013T\x0011¶²\x0001²\x0012&B\x00172ÀââòòÉÓÅþ1¢KÊMUÕÞÿð4Ë²Ë«Ë¶mï½uï­·î]^²Â|o¡=xðçþ?=|´üðÝùÛoÝÍ2\x001f|ðÁÝ»·ÉGªêº,o}ë[77«¢(\x0010)Æøøñc",Ë\x0002\x001d!iQ\x0014]lº®»w÷­Íf]\x0014ELÝ;ï¼s}y\x0015\x001c\x001e\x001dìI×ÖëÓ<÷	äÞéA(ÊË«§Ï=úâ¡\x0003Î²\x0014¡où~øÃïÿöï~ã½\x000fßo»vÿøèèé³gÏÝÜÜì6ÝEÔ9ïØÇRÛ\x0001@e]\x0007(*cç\x0005ql6É+½ßüEè/ü`o®*mÛ®«\x001a\x0004¼B\x001f°\x0000J(@ü-ú+\x0006'»CZ{\x0008­¦Ù\x0005d$Ý÷QJCüôÆ	Ð\x0017ô\x0000¢ldsETâÓ±^@\x0011´ðÙb>)ÊÌ\x001eº\x0018Øº\x001dí\x0006n÷'2\x0011$ØÄÉ¤tÞ{]Â@.8OäÈ\x001aºÁ¹iw]§Ný\x0010Ñ`°¹²ñÉ@vÂ@ }mÙ\x0019Læ¤\x0002:ã\x0007÷«\x001bJ«×|F(h7Kn¼uð·ã4ôú8\x0019£3ÆWçëÍÆ`°.vE9rËåuLÝt2!\x0017¦Ù½ª\x0018c\x0016²®u]\x001ce9ÍTu2\x000bójµº¾¾BÄrR\x0016Eq~~\x0011Sº{ç\x000e\x0010]]_Y}PNJ\x0000xôäñjµZ.*êV\x0000 (¦isÞ;\x001fBiÛDkU_]\L'³\&& \x0010%¡ëc±EQb24aE5v[î\x0008j2³(ó!d}\x000bAÄ°\x0019\x0003RbÄd­¨É¤|ðàÁ|>³P\x0008NlD\x0010ü\x0008£¾þBBà>S­/ÌQr\(K¯)Öë:a&¾·HDÞ9O®Ïë\x001d\x0016KRPå\x0004bä$BQ\x0016\x0004°
qz²\x0005¢\x0000\x0000aH3Yýõ\x000b¶Cï\x001c¤¨BBì\x0007\x0002é µ\x001a3rNÄ8ç\È¹i\x001aqt¸"Íº©ë:Lò£ý	XcN7ëUlÚ¦ªë¶ApEQÚ3R1wM³"t0DýxìØÇX={R8:.þå_üÕã_~úÍ\x000fîê\x0010z\x0017¦\x0013ðyð¢lÙ¶\x000eT¦e~ûÎíà\x0008,\x0000@\x0007Ô$
÷\x000eX
T@\x0014pP'7pH\x0005-\x0001H\x000eû\x0016\x0002ù{«jdNIìRê¸§XÛ\x0001Ôõ¹\x0004àDÄ\x0005°¤³\x0014cE\x001c±pâä{{fg¥Ì0Wó¨QÿúÞ\x0007\x0000\x0000:\x0005B Ý±\x0017\x001dW\x001fVµ¾òÀÀ3§×úJÔ! 20(\x0011*9@1: #Ee*	àåòn\x001cRÉtý\x000e\x0014;\x0016HÎòS,×
rM"2¥¼z_\x0016ÁJ@4Cë</¿÷Ý\x001fü\x0017ÿEõú§ÿ»\x0018£HZ­Ç\x0000\x0000X\x0015\x0010\x0018À#é-/c]×Ò{Ð°ÂötT«åÆ~z\x0018Þ\x0003Ü7@ÐÄ\x0017}ªUïý@$®_AÔ
>" Ê¤Î~#`\x0015Db\x0011ïBMÊüä_|<+ï\x0002gélU]|ñàá»ï\x0010|øìÁ\x0017¶ÀÞ¾óãþl2ýòOæóéÇ¿øø_ýÅ_<¾üo¾õÛßøúíÓãz³Z,fëÍòÉS)âøøx±¿7Î|Ý½w/\x0010²Ì\x0011½óÞ»u]oªu\x0011ÐO&Î»ªm|Um\x0017|&\x0010\x0017û{\x001c\x000bé2\x000b_ùàÔ¶\x001dC+EImÉ
uN'/.bdðÙrÙS_5éÉ'|òÉo}ã«§ï¼ýüáÃÃc\x0000\x0010\x0006rôìé3³QU+(-\x0013\x000f¼³çÅÅz\x0012ª`ß\x0007Ünxý\x0019l{²××\x001a¾ã©]­\x0000\x0001PR±¸,ËYâ½½FXê®U\x001e<s\x0002\x0000`4f1r¶9k2bé\x0016òfÖ¢ÊöýÔsüûÏØSw- w1Pt=Åªþè\x001c£SQQ§Ö?P\x0002F\x0014Ð±	\x0000è	CO\x0016Ä\x0013'\x0013\x000cäÈÃN8ÑàE¤m¢ép<
³''\x001d\x0003e\x0015ÛÕMùlº·w\x0017@ªªâ!\x001dÌ*±}n\x001fí
LMPn'\x0019¾
ú\x000f\x0008°µåeV"\x0014éÿìï§\x001dl^FixÂ½#Üp·Ðu\x0000ðnK
1\x001a>\x000f]
ó3\x001a(Æ#L\x0005ÛÑ\x0002Æ}Y­-<PCpÎãz³äÐâ\x001c6u\x0003 !Ë¼sYá\x001cëk_ÿù/>>==ÏçÌrssÝu\\x0014EY\x0014,"\x0013
ìí\x001dLÊi\x001fý\x001b2G5.Û¶=88L¯Î¯¾þõ¯?þ"8o[r\x0008­Õ÷nßûÁ~èó¡iÄ\x0003´mëÄ\x0014ÑgÔs\x0010\x0001QRÛñ0NºØqêQ\x0007""%EÝE8rCèJâ$Ú\x0003$÷)&Rà.b^8ÄI1O§|\x001e²¶mS×eÞ·ÌDäqk²¥
b³@Lx!vè·
\x0017,£×´ZNAP	Maá\x001cÐ@È\x001d^\x0000Bj\x001b¾ZP ØÎ$	z[©¡"ÞÃèÖ\x0003\x001a\x0006©? ª(\x0011ª¨j²\x0002\x0019	H\x001d:\x0004H¨¨ÂÀ:U\x000e\x0008YX%©sBNU=\x0001¨Ô^Ò\x0007c=k\x0016ê°\,(rÓuu£"äáº\x0008C\x001bN{Í\x00179gÞ?\x001ebÇuU\x0006:Ùß{öéÇO>ùùÁ$\x000f"AÄëìÃX¨J{ lÛ()!±ÏÀg÷ \x0010÷¤ªD\x0013Gc\x000e½[òÊÔµÊ,êèe\x0018SX\x0010ûs\x0012°!\x0015|Î\x001c¹$v^\x0002Ä=~.ø\x0005Ðû$\x0012\x0013³ ñ7vOA¿Â.Å®lWÊD¯à«\x0004¨¤^\x0011Yq$B!
üf½mÙÂCÚBðy;O\x001cûÞ¼)8z\x000f¸~-aN¬Úëï#KïEFÎ9BèÓ\x0004\x0005 8OÞjì:I\x0010ËÉt2x\x000cÒz½jÆ\x0013,;;»ø\x0017ÿâÅbáþøOþ`:-Ë²\x001cÆr@"\x000cGeP$Æ¢à\x0014Û\x000e8¡d¤ÛPk\x0004DEBG¨H
Î¨Ù×#\x0002Ú\x0006\x0006ª¤à\x0014z¢\x000f\x0000:@\x0014¶"GÑ¹Þ¨gà­
)òVÅC\x0016\x0011ìP~ññ#Ä\x000fùåÍåÅryq}µ¿pppðôÅó¶mW«Õ½{÷ÎÎÎæóù×¿ùwö\x000e\x000e?þùÏ¾ûÝï^]^ß»wxxxxþüWyçÝ{\x0016§\x0010|\x0008>L&Ó²(&ÓIQ\x0014Y(¼÷!ËÈ;g>Ï²2K)²$7dn.ìø±\x001e\x001d\x001fj¬S×DÖõ\x001acÃ2ùÛ0Ï'åôãÏ¾xütÉ
$vðäéüä'èáw¿õ­[·o]__oªJU²Ybk2·\x001aéÃ=Ö×(;
o5oq\ïä­ü\x001b¾÷¾ÈÂÑÁ^ðáâòb]U)%.!»#¡  ö¼ºY¿ÊàK×&\x0006«\x0018,#ºÛ}Þ¡ ½\x0001Ô!\x0005\x0005QIX9z`\x0002ô\x001e¨=#ÞÀp"0\x0005\x0019| \x000c\x0010¥á.1 &"£C%W\x0003sÁïº\x0004J.ä.\x0014]Uue\x0005\x0000Xê¢Ý|k\x0008ùäx¾·?CÄnV\x001aJªc&C_Ódú-Ap Zrê\x0003[zýß\x0001\x0004\x0000\x0016£/õ>t\x000c±\x0012Ñ\x001d¸\x000cC\x0011\x0000hµt¨ÄTÇ7´CÛ; ÀÜ[Ý#©#0	\x000b¼LFnª\x001a\x0010ÈAQdähµÕ:ÎÖàE\x0010£L¦S+b|\x0008X×ui6\x0011Ñf³ifµZ\x001d\x001e\x001c³Ñn²Ì9×u\x0011\x0000BðuJ\x0006`x\x001fv¯)§RâÁþ?8ç°ij\x001538\x000eÎù\x00189\x001c\x0011»ÄmÛÎ÷\x0016Þ\x0007ò.\x0010"s\x0012A²¼*¡eºàC\x0016÷.Ì9\x0002Qsº\x001f÷\x000b,L"Â\x0012\x0019\x0000,\x0016j\x0004Aèþû÷_¼x±^onn®\x0001d:VUe¦2;ÏÞÈ¶©¿ùÎ\x0005¤"\x0010 8ÄÀ¨\x0000\x0012S\x0012æNb\x0012\x0016D"\x0002D\x0014 \x0001\x001a\x000e+vZð¸k~Û;ÕÔ«Á_\x0011¿)¬ÿ\x0006êË\x001a£uÚÿL½AÞt'o´í\x0018ÃL\x0010-vñå¯÷ÿÁ±5S\x0006
>­.z¢à¼ÍqVEz©KÚG\x0002\x0000øÔ¬ÚÍj¾?T}öÉO\x001f~öó£ý9p
(Î9AËV$ç@QDÔyÌÑuY4f\x0000`q(b\x0012?re>F´Ù\x0001ªG5\x0010*ÚL\x0010U\x0015;\x0013ög\x000e\x0016a1öxï.ªXÀñ\x0014\x0014È¹,Ï!Ï;%GúÆå \x0017³{¥&¦#¤$
%qli}ö:WæÕ~¼m¹ög\x0012\x000eä¿Ì\x001cÏ \x0019ç¨ð_Ö³zéÑaoiàÕ©§\x0019Ü\x0005çC\x0008ö\x0016[ÕÕÀÃ¥·\x0008²Î)\x0011ÚóöÎ;rN-\x0001Øj#AuEÈbÎ»I9L¦HØUÝjµÚTkUñ=yÖ]]òOúÓÿè?þ\x000f..Î\x0016E¯\x0013±â\x001d¢\x0002\x0002¡Í\x0015ay¤&¶\x001ck­e}é à´ëï4©)¦­j\x0013\x0000gu\x000e!\x00009@\x0007laÀ\x0010­ªQ%TeIâ2Ç"}27"Ú¬\x0002´W\x001d9ç}\x0012^oÖ\x001f?oZÌëÍºKíùùùÉéíº®ÏÏÏ×ë
\x0000\x000eö÷\x001f>yö­o}ëÝwÞ}ôèÑÏ>þÅååõþþþÁþÞ\x0007\x000fÞû\x001e\x000b?|ðÅ·þîï\x0015E6ÍÊ¢\x0018s^tH{Q\x0004\x0001\x0015\x0004t\x00159±WMv°3Û7Q\x0015f\x001bo}ì¼w\x0019e»ØQêT»V\x0001 Ë²r\x001a½Ë6æÑåÁa¹ØßË×7\x0000ðã\x001fÿð³/~ùýï÷\x000fÿðV«UJÚõd×\x0001\x000ció½±ºCD)¥Ô¦¨&W\x001eñ¼Ñ?íq;Î·%Î¯Õr"g\x0015*fÂ)Ï\x0015)Ë²,ÐÙùÕõfÓ¦\x000eÈIä\x0010¬a«\x0016\x0011öëÔ¨\x001cGD\x001eó~ç\x0016V\x0016\x0003\x0014e\¼ô
\x0014´\x0011»\x0015\x0012«T\x0000	D\x0011\x0002\x0016Ü!zÝú¸¸Þ£
ErÌ2?[Ói6YYæ-´\x0007\x000ej\x001e\x0005ç\x0011\×%\x0000Êòi¬KºÆ9BR%4§mó½pÈÄ;Øp©«\x0011±Ï6·
¡¦¶z"\x0013\x000c"\x0011z\x0004@-\x001e,\x0003\x0013\x001b\x000cÙzé(Hcñ"Òk^*{\x0000\x0006²Ç\x0000qá\x0000_íâ=ª\x0002Êl´:´_Q­+û\x001d\x000eÐ\x0017;t¼Ô^ >Zÿ\x000bd\x001e2ï8¶Áàh¿øÚW?ôÁ\x0007r,©i\x001a\x0016\x0019K@Á;_æCÏçMÓ\x0010¹Åbá\vyqÑ,\x000b!¬7\x001b\x0000N'T×5\x0011å¤i¶Ñ~6\x001db×ÅÊ²`<ÏEÄø¶MÓyï\x000e÷\x0017ggWÊ\x0002¤ÒuÍò\x0004O\x0017EÓµ@¬Ø£»]33Å'rÎ\x0005K\x0008\x0007\x0000U¦­È¬ö¾ýÃ8Æ$,ä(lèøC\x0008a½Y_\x001b
v>c^co\x0008dE°ÈÀWñ\x0000äÞÂ9G@ÊL¬:T´h9ãÖd \x0004Ú9¹8\x0014	I\x0007ªáîô\x0017¤Ó3Í®\x001f\x0001ÁÖ\x001fÒNª\x0012ÚivÜ]\x0001^&®ÙýD°ã}ÿS\x0006Ù
ôÆ´¢=A\x000c\x0013Y_¹)xMë®¾tûþ_|òÙ/¬i³??àjM\x0018\x0011$I\x000fK\x0012\x0010j°µ³p\x000ctÄ\x0010\x00100\x0001êX|y\x000f!ó,ÉâÒw>éx¡Û¶®Hÿé\x0006	ÖH%#DQ1wf\x0015 pÁ9ï²à\x0005\x0008½HË)1÷É-\x000e]\x000f\x0008¢'§ Ib'IXúH`\x0006p@Æg±2\x0014.¸sW\x0015@z`fX\x0019\x0014vñ@a%FéÓd±'©°þ*df\dF¸Ø9\x001a²¨Á\x0010=¹a\x001br©"`Iª"xwNy¢\x0010Bæ¼CR\x0011a!#N\x0012ÙQ&Ò\x0007\x0017|\x0010jSÕëf½Z«\x00029h:U­Ç&Á½{÷æ³ùçjFpãµÌá\x001e¦\x0003\x0002\x0001ÑN¼]º.µ]B¢r:*ÃìÙ:\x0013gÁhßc\x0015µåïÅ\x0003\x0013xìý\x0010ÀNÏ\x0003¶
\x0011\x001c&Ë¯P»\x001eñÖ_\x0010E"\x0007èRËuÝ¥\x0014£]¯«
8\x000c>_,\x0016?øÑG]õ\x0006¾ùÍw»\x0017ÅÁþáåÕåÇüò£\x001fÿ\x0014$­nôá³ÜÁ4áP\x001dèÕõUQä1Å¦(&³Yð²Ð\x000bãõèàm@HèTÉêq`sWëÙ\x000c*h\x0011¤8"Ì,\x0012\x001cí-ò,syÝñMuçäxõöæÑ§O/7åtÎIc\x0017¦^×«årÉÌ××+ç| \x000c\x0007\x0007æ\x0017g}ëf+ýÑÚ\x0008à6r7îoIù\x000eb7Ó`G¥ò+0KU!µ 	{G\x000b\x001e\x001d\x0000øà_\.»Äà\x0014P	\x0014ÇÔÃ~çeaê=*p»ójo
Æ±$ìM^µkÚå\x000e\x001b`gI\x000c\x0010\x0000Ê,ßóé$'t*`\x0019Â\x0000®\x000fTUÍ<pp0?ÜííÏÒg\x000f´Ç-\x0006ñ\x0005#¢$n(à}1]Uüü|y±Üt]«¢H
 Ì\x001dKJÜ¨´ÛÇ{§ÔUËuÉ\x000f\x001e{J\x0008³·\x0011\x001c\x0000@X4¨\x00129´x"BcJêN^1§j"\x001cEª´k8Ô\x001b~ªÚ¡ÑÁ©\E\x0001ú\x0001ÆC\x0000¨6
´
é¯
º.­W«õzcâ\x0014»-)	fù!xïëM\x0005¢¹s_ûêÿþ?ü÷½÷Ô±ÄfÓ©¾x\x0017=~úÞûï\x001d\x001e\x001eTUýôé³â|>?<¼¥W]Ýªª\x000fS\x0002\x0000\x001f\x0002³¹HÓ7#!FI¦\x001cK\x0010,³\x0004÷öö«Msyy½\.çóùÅÅuï\x0019.Ò¶uLíb1ocWä% ëºE@T \x000fúAÔcPCr
ø\x0018\x0000ì*<Í8Ùu»-AJT~ò\]^M¦ÅbaæÝÆmë&¦4t-\x0006B\x001b3"%eYJÌÒ©*\x0011\x0010(\x0008\x0001°²:éc4v|
zkÝW(öÿK~é\x000e`¹kO°-z[\x0010@}ÅrÚn²øõÕãý½¶:ûÙGiyÿí£T]\x001dïÏ¥á¾Sº¹¹é×\x001dEUUTGT5\x0004_\x0014Ð¢:G\x0000JHH eîPB\x0007ÊÄÒ\x0017\x0012j1æF	ôâÄ	Ò
\x0013Ytz£R«[\x0016 \x001fÐ\x0005A0k[\x0004'H\x0012A\x0000\x001c9òè\x0001HÑ2	\x0019ú£Û°ô;P\x0001r¬DÃA\x0014·Ì¸¾l­Ú7â\x0005\x0010í\x000c®\x0003k-jUUÞÁZ<º\x0004ì\x0000\x0012ÁëñEFy±¢ÀA\x0008¾ã¤Ê¨@¤#BKT\x001e§¡!v½ÚeìèÊ\x0011­Ô)* (9ç\x001c\x0015!\x000bæcè\x001dªpmÛvm\x001bcÃ\x0002v>5Ü\x0015>u)­ë®6ëÓÓÓ¶m\x000f\x000e\x0016uSµ]í\x001c\x0011\x0005èOØÎ¹\x0010B¸è.æ³¹y¸!"s\x0003e\x0003\x001bPÔ\x0001ºmÅM@$
ÂÃÂ\x0011¼\x0015ª\x000e@±0î\x001dã¬\x0000\x0010Pÿ¦\x0014@Ûµ7ëõÍ²öÞI³³³ã[§\x0017×W''·D &\x0011Ó\x0019+^Þ\}õ«_wÎ}öàá³gggË8sÐ0|p{rûäøøè`1þÖW>(Bf\x0007»¬ÈC\x0008.\x0004\x0005
ÞÎ=\x0016ÒL\x0016\x000ee\x001dj\x0010e´¡¬\x0016¨¸\x0013s\x0002,¬h\x0000"K\x0019<Hd'\x001e8Óè¿s¼÷ÖÉáùÍ¦K×ÓY~|z´8ØïºîÎÛ)q]7]Jõ¦KÑºÜªHÞYév\eèä¡DQê%ôäH\x0007î)`¯Ð\x0011\x0001\x001af\x0000õIÔ}K\x0011\x0000Ó¸f µÑ\T=Ñ\x0000\x000eÃÜÓQî,L®nVQ\x0001É\x0011kÒm#\x000c¶\x0002}sÄ,\x0013\x00070\x0001EFßÙWÊ(\x001c³aú\x0019$8"Õý¬PTpàÈi/ÊébR\x0016&Ðha±nÀ\x000bU5ón¾(n\x001fï\x001d\x001dï\x001eï[)y#î¾L\x0015B1£\x001atÞ\x0012Üôì¦ùî>¾Y¯\x0013\x0008`BTÔv\x001b\x0005\x0006\x0008r´?ùÃ?øYî\x0011ÒfuÃ±\x001b\x001dèXÕÒYÄ´R=.%<T¹\x0012GNÌ<B2¢=*É1Æ^N!\x0010SB¶¢Ðo¯z\x000bÆ	\x00008%ó³P4wt³Nq£¾¬7w <\x0014É\x001c\x0000ÖU­ª@\x0006Gx\x0011xñ" ¤ë«º«6u+\x0000;PV!\x0000\x00149L0\x00169¹\x001c\x0000ºÎ£|ðÁý¯}õ+
j4ê½ý<dYÕUss}yïÞ;·oÝ9½}k2ÖuãÈ\x0011zD'ÊÁ[·n-\x0016¦éf³\x0019ìe*Ø¶- _.¢\x0012B\x0008\x0014Úºý¯þÙõÝwÞV²-\x0016rR.\x0016Ì\x0007eäÅ|>ß>Ð­«¦nöA\x00101x¯ä\x0012';rÛÆÙ7ôMI½éiqyèÜÙ9~t)\x001ca°\x0011¶±¿\x0008K)ÅtûÖíår	\x0000\x0016hßï\/ïè\x0017@T\x0016á.m7iÒy\x0000é¢rÀD¥I±\x0005NÊ½ú¶á>à"ªBà\x0000ÜU´á¤ÿæxÌîÜì-ópøûÈØéQ^Ý¥sl¡¯aÄn½ª¸ÿeÝ\x000f5Õ¹ÖR§þæâ	Äåêæüêüñ,8¯ Ø¢\x0004Àdß\x0004H!\x001bG\x0012\x0000`¿(\x0013"RQd!8\x0015A\x00024}\x0008:\x0008è\x0010\x00039è:ÃÃµ·Ëµ\x000bD\x001eG
 ØÌÚNH\x0014¼s\x0004\x000cI$%eÀ¶è\x0000\x001c¢óÂ`%,½a¢cEEeE\x0004d@V\x0014è£bMö;Ü\x0005ÐíÄßÒ\x001bíà?B2ã¿ÛÊ=¬h4¯ªî\x0007ö«\x00183Øóz\x0000\x0000È{ç\x001cpJ,  k*Õ~%X¶¶ª\x0012m#a#\x0007(E\x0012p4¼±È2ËM\x00149¦V¢\x0019Ä3"Íf\x0004\x0000Y\x0015YpbLä777Ï?_,\x0016EQÌçsçÈàº Ò%Ñ¤D\x000bL1#1\x0017òéÑé­Ó«Õz]%@OfÓ "u³i»H\x000eÑlÏ¥\x001fÂx 'H
\x001d3"\x0005§à\x0008=¹\x0004æÆ@\x0005À\x0001
[.ä\x0010TP\x0000\x0015q³iVFÔeehc=MB\x0008Þ¹«ëî,®6°Òl6õÎM\x0016wÞ~ûñãÇWW\x001füqIðµßº¯\x0012ÕÍ­Û·ö§ÓÙ¤\x001c=Û¤ìE°W\x0005Gä½ÍÂÑC
m« \x001d£-c4\x000b¤7p;PbªUÀ\x0013<2"Î2<=Ø[¶\x000fg\x0000'Ç·..w]·YoDu³Ù|ðÁW6Mð\x00193?{q^wíÁbïÖéiVN¬5/"MÝ´m«ª}ì\x0019J?Alu¶¿ÛaDÔ,bý§!f\\x0001xÇKc+\x0014zm\x001bÞK=\x000b\x0013WÓÅ¢[,VËU½é8ªÄ¦U6)ÒÖv\x000bmnuK:6u@ÞÔRúò\x0017)(pÌ\x0010¦y¹?Ìò²\x000c! {\x0000\x0010\x0005TR1Î=Õ<w\x000c\x001cË\x000c<F§àUH<\x0002D{[\x0000\x0008\x0004U¼GràÕI»é$äE q«¦R\x0012UnS§

\x0011\x0015¦¥ûðþÝiáIbSÍ\x001dj\x0018<ïMfÒ«\x0004\x0019¬=ÁVÈÄÅ\x0011	õ\x000cÖ½3r±ë8YÎuÙm\x001d
ÁÄ©ïy(ª¢I"\x0014)	\x000bCâ$]²ûþ\x0002\x0000rf]\x0007©ªU×eE^äS9)§|6+R9HÓ\f³éÑþ1s:;;[­Vy\x0008ó"?ØÛd!\x000b\x001e\x0000º$ÊÂ]¤,$\x0015/²LÌÓÙloo/µ|~~±\.÷÷ö\x0002e!Ëb×ýÿ¨û¯nË²ì<\x000cf­½÷q×ÏÌH[\x0016\x0005\x0001@ \x0004²AR\x0002%¡INvt~ÐCîGýîÑ=F\x0016Õj=HbS

\x0000\x0008Ã*ÉªÊ¬¬Ì0\x0019îF\sÜ6kÍ9ûaî}Î¹\x0011¨,CJZ#+êÆc¶Y{­i>óÞ\x000fÞ»yëV±,Ko¥ºTIJiµZ¯ÖkSc
ÅhÌÉ¨ëºõzÝuz~¶º{÷nÛ\x0018\x00178\x001aX|ñ_üÊW¾|ýÚµ³óù³³^NÍr\x0011f¹^ÎÏë£\x00037\x0000\x0003sáç°=7å\x0001¿Ô_d\x0000ðz
ècË¡'²DÞ\x0002\x0007FÄÔuMÓ\x001c\x001d\x001f]»¸ºn£«ëËxUU\x000eTR\x0011Õ<4^}_óoÝÈÏlJ%çI\x0015\x001dë/pmUÙ3êÿ¥\x0017g\x0006OöK¤Å¡Ât«Ö\x001b;÷/\x0018.fX¯NMgO\x001ej·¬Æ3Ì],@Ò\x0011À\x0014TrYÆÍu\x00141\x001eôLä\x0014q@vð4ø\x0016ëY!\x0010@dF"K)zù´÷vg
}Q\x0010\x0008»®K9w]§`±(B b\x0012±rNN`®ËHc\x0019b Dÿ4§o¨Y'É\x0014(!vYSN9\x000eÂ±Î\x0014Þîñò¥\x001cþÚ{3Û%ßeCç ú\x0012\x0007R\x000eQÙ\x000eìú8\x0011q7fÒ\x0017xU·/`ùÛ\x00111·)'`ñh4\x0019$ç.åí»\x0006ðM\x001fm>ICpðI,ª@XÆ¢±àHL\x0002bb)§Z7\x001deP£i9u\x0015\x0004\x0013U®ë\x0014¡\x001aÞ}÷îûï}ðÏ¾ý½ï}ïhÿøââüìl>Ïï}|¿ëòºiRRKEºå¢$.¦;[wgç+\x0015+Ëc$&\x00153ã\x0008N«L\x0014Ñ\x000bæ\x0003>\x0000X\x0018P-£¶\x0000Q \x0012\x0006
ÎØ $FVÄ\x0008¼5Êéy\x001f\x0001\x0001-t]ZÌë¶µñh´ìºùj\x000el«fyåÊÑÝ{\x001f?yzA\x00004\x001eOB,ß|ã­®ëîß¿ÿñÃG]\x0007áââ|<ª8ðÝ;w~ñK£ñèÑÃGWÆ¹ër2WQ5LQE	z×\x001b¿=d¶í?"¼Ävt\x0013è\x0000@Û¶d\x0014(Jf\x0014SlÇû%4usýúÕQ5Z.\x0017e\x0015Ë2PY^®Vµ)N÷f_üâ\x0017GãÑã+W®_ì\x001f!²×·\x0017óùÉÉÉÉÉæQl&8XCûå}Û¤dJ\x00040¬àf»F?Û±æ\x0019\x0002ô¢ý\x001c4$K\x0008\x00162(\x001a)©!Ç\x0010ËQ5ÌF£Óùù²îº.{IuóDlTb½ìÖ,´\x000f³ ñ^òôØ<\x000cÏýL	ÀTSÓÆ"Î&ãÃýÙ(\x0016\x0004\x001d\x0011DDÖ?FÇÅlZNÇÅ¸,"S\x0000`dÞè\x0019\x0010!æ\x0016¦j*9\x001b'ÊZ\x0000ËAsÒÜe\x000b"D&\x000e\x0010ÈËÿØÕ¦\x00034¨\x001c<h\x0006H)"aé`sñ$Sd\x001e²YtH?\x0012
-Uò<$çÔÔÝr¹lÛ6åSx¥^Þ\x000c®è×ÆëYAÅ|	írNRêC¥³³óÍ,r2\x0001Ày]xòÐØLÛÔj\x0011xoVJFRÛßÌG×¯\\x0005\x000f?úðÁ\x0007ªzíêáÞÞ\x001e©9Z%ä.5U¹ÝDcQ¬ÎÏ\x0011òãÇ¾õo¯ëõ\x001f<{v:.Ç\x001eÊÌçó¢(Ê²¼¸¸\x0010q\x000fM¹s,¦Ã\x0018º®)ÒÌV«Õõë×Uu¹Ïç5\x00179%ÉùÎþÚ_û«a±XõU~Ï\x0002Ðn~~v¸8\x0018sHF¥£Ë½_C"úäÚ:¼\x0008q%bbÌSN¢\x0006\x0000!¨\x0004\x000eÇÇG)egª^Z\x0016ÌÚ¶ÅC\x0019ì#$É¹mó¶læ_h\x0000)eQ1AðT±·ÃÂKÆ@ ·ÿÓ(/|â¹ãé?îøòå'ø2\x0005\x0000TSr§\x000fõÄ	wUÂÈêGêó7n]Ón½Ï\x000fö÷@¤¯£\x0018\x0010oÌú#cF\x000fV\x0018Ñ\x001cRÄDØ;jbïÛ£\x0016\x0001\x0015 ¬{ð\x0001¡!ö±\x000eR6\x0000\x0015m¡\x0015\x0011#4í¡£Þõ\x0006e\x0016lR\x0012\x0012E @ ÈDY,g\x0011@S+\x0018¨X\x0012MÙÄÀÏ\ñÒl5}yáD\x001cl\x0008À}Ýf ­m¥*¼k×Ï!\x0000ÖM"¾cøüR e?\x001d½ÏFÌ±*ëõÚ\x0006\x0001 *Ëªªêºö®°ú\x0000H¢¢\x0008yp\x000c&\x0003\x0004r\x00152Ä2r .\x00021 ªI$×Òæ&0\x0018ûÝL\x001d\x0004 MÓä\x0001ÀûMõºå\x0000\x0007USÃh4»qíñÏÿðôÉÿxzz\x000e@gggËu½ªëùr±^§£ÃÃUS/\x0016M#L§3U].WD¡H)	\x00189d\ó(úÿÁÓ÷JH!EÌa\\x0015ãÑ(\x0019\x0004) \x0000\x001a\x0006à\x0002\x00191ôwÀÄ\x0015ú\x0001\x0003\x0002\x001b°®ëfÝä¢(ÕàbyñôéU]ëjùÊ+¯üðÃ\x000cáökGuÌlooo4\x001a¿÷þû§gg\x001e?}ýµ«1ï?¼uãèóýÌÙ³§MÛ\x0016eùúí/
Èh:ªÆ£ã+W\x000e¯\x001cWU59\x00041ÔAyÓa®ßÎ&êÍ\x0013Tt´µw%LÔ9Án*¦èZ'Y$01cD"jW\x0016ôöÛo~ç;«Õ\x0003/NÓá¡\x001eì\x001f\½z\x0015T\x0001ôððøÍ·?óË¿úko¼õæd6»/âh:§i¹\<zøàá§O¶ëÚ³731QMÙÓÁ<\x000c!.
SR\x000b\x00116-¡ÇÄ#>á`È\x001c8(ª\x0008ª*H¦PLÇ\x0001ÎÅ\x0013G\x000fývÈ¼ìâ­ÿ
÷å\x000fË®\x000büæpÍvV\x0008H \x0016FE9LÊ\x0001ÄTÉÀ\x0008{\x001cºº0Æ¨*ªª*Ë2ÆH\x0014¼Ïfà½\x001e\x001bXx\x001e')I\x0006\x0013áÖt\x0004Ñ\x0014ÕP\x000cCQ\x0015EÈ!F\x0000PGç£ªv ¤$¯,e¾\x0004\x001clw°±ï\SB¢ÈD}ÉkðTa¦BdëL¨DB
\x0017ÍÊªCSCp»ÆÀ\x000c!Æ"VÈ\x0001\x0000ÄÐ¥o;)´'×<=y\x0006Ãåm4\x0019O\x0001`^7_·M{±¨ëuûììÈÂþtV\x0016B\x0011édº¿¿EnÝ¸r´7iÛ6pàÙcðN\x001ahÔ\x0001\x0000ÁgÎ\x0007\x001f|ðá>úÆ7¾ñî»ß\x0014æó9\x0007><8v²Ïµk×¾ô¥/¹
eÊ	\x0000rNãñ\x0008@ëºÇÒÃÅª\x001e¢\x001b» [\x0011\x000bÇÀÁ\x0006ö\x0016"PvÝÅs{­fÀYäâìüàêUÜµ¢½D\x0006ïÞ\x0007\x0000ðE\x000c|3ë	³\x000cÛ[á}5&ëß"*\x0011\x000b$ëº\x0004\x0005øq\x0002@z\x001d\x0007¹»\x000fÃÀZg°mÓ
ÌRÊì\x0016Âj"
häL®ÂuéûÝÍÃ\x001dt-Pø¹ð\x0015_v¾?ù{ûS?õçô\x0016ª<p\x0000qhá©·ÿ\x0011Ö\x000fïDBe~Ê\x0001GUÉh[­MT0\x000f\x00047òh}õÅkkÖ£PÈ\x0010{\x00101DdU'1\x0005ScÖ
hÿLQ\x0012Í1F3K¢EPÕ+§p\x0019&»Ä\x000c\ \x0005\x0007*øIªh\x00118pH9u9¯N\x0007Þ\x0001°©Sêy£\x001du¹È\x0001}ÐêÚý¦^\x0013öùíÐM$x®®£\x001eO«Ù\x0016¾6òJ\x0000°¡¦#\x00112+B\x0011ãi×¶\x0019\x0002¹5\x0017G
\x001d %ÍC\x0015&"¢s&U¬'.©ôhððE$ç%£G\x0015P\x0014S\x0012\x0010"J¹
SÊºåR+)û^ Ó)|ðÃ;mm?x÷î{ïþùãéºn®\x001c_{ðøA\x0012¨3$\x001eÉn\x001dëÙbèª©aC´\x0001¢ç­=mä®û\x0000´¦Dã\x0001C\x0008\x0004E\x0011"H\V±\x0005»ÐSÀ\x00140*ËQQ\x0015Ç"e9L×\x0017ó¢¨ÖëVFé£G'\x001f?Nçÿàßÿí?üãu~¾~õµïððõ\x0017º®{íÖÍÕââÛñ¶Sxp÷¤\x0003ø+_~ûË_ùÊþtrõÊÑÑÁ^\x00118¥æÕWoÍ\x000eö÷\x000f\x000fbUºÊzça\x0000*\x0019HÊní#}\x0013EÑ\x0000ÐT!³©ìd`½F1\x00040\x0011¤HñìüL
ÌR\x0002K\x0017çOzª\x0004\x0008j\x0007{e\x0011âÅÙÙk¯¾ZÅðøñüÆõW~ë·~ëèÊ
*+¥Ñìh\x0002\x0000Õ\x0008f\x0000YrYBàPãÑd±¸X×õrq¡Y\x00058ºùí%î^\x0004Õ5W\x000c\<F@\x001c\x000f\x0000=»Ù¡FÒF£\x0017-\x0001\x0018ZU}GO/\x0002ª\x001a\x0004\x001a\x0004zJ:t\x001bPmÇeÚ'\x00190¢K%\x0001\x0002g
jÝïÈ\x0014\x00081ÆÌ]Îóå:\x0010dF	(×!BUDb Ð\x0000D!(RVX5m5\x00198@\x001ez\x0018¸"!#±KýIf\x0004¢@qbqtq;QEB
È`Èu×ª¡Kï\x0015äî
²jê\x0000Â¬&\x0014ÖùàNsSf\x001c\x0003Çé¨jÛ\x000b£9\x0008\x0006À\x0000:ÓÔ×`Äu¶²äÜ¨/'Ã\x001a«ªN§ #¡\x0001
Á¼û½µ\x0010\x0001ÀìÕãÍ\x0002[¯\x001a\x0000\x0000£«\x0007åìðÊªißýÞûöÃ\x001fa'³ñÆb-¥Ü¥õÉjùôäqàÀh£2V1déT5d\x0001CË©m¤k\x001d/á¢sGÿôýàý'·^=L§ÇÇEU\x000e\x000e\x000e4i\x0008A\x0014>=õ¼Ë­|D%\x0016¡(
Ñ¥;=K³Ù4'ÝßßW'Oâr¹¾8_t©Aä²¥)å¶Mßýîw?ûÏ]/&ñí×_¿{çÎh4ZÕM,KËyµXì\x001f\x001ehÛv!\x0004@GDú~°]ð¹ç.õz¡1Ýf§äÐbÃúï~^
\x0000Ãº[\x0007\x000e!\x0012"ª*9ÖÜ«?\x000e:ß$	\x000eìJ¹§¶¨
\x000eÅÅ\x0001\x0003ÎdÚ«Æ\x0001ò`çìû\x001aýôáÇfë\x001cVu\x000b/+J½8¶ÉÆ\x0010õtîË0\x000c\x000fnpc¨9 m`H¥\x001cì=¨Í]:¶ÍWh¦IÈd½=J\x0011¹,\x0006£;å~¦­\x0005¹l'\x0001\x0001#{.&J!*å·\x000c&DâñJk±(\x0012@A*\x0000äðIT{\x000c\x0002c"U@\x0011\x0001£LYÔ;äLmp¶\x00011\x0018eMuêV\x0001Ä\x0011\x0019P7p^Ì^Ö\x0017ï1ùÜ\x0012Ô%ÝÍPÕT\x0018x¨Êà\x000bUxß_ó{\x0015#¯×ë¶mU\x0001ÆeÉ¡×\x0006,%Û \x000bàêZb½÷\x000cLl\x0000\x0000I¹Ëj@Q³0 \x0011\x0017e`\x000es×¶\x001a\x0014E4S5ò
!XQb@¢"<~ô,µpv¶L\x0019=[¶\x0019ÖËGFDA\x0002È\x0000 6Túz\x0010UOÜî?Õ¥º6ð\x0008ëMégÊ¤8±áF¥×\r¬\x001a\x0010
Ts\x0010  \x0004â@PV\x001cRjß¸}ûpöê«¯ªaQT"p~~$?zøôK_úüÝ»w\SëÑ£×¯OÇÕx2ºhN-(\x00042ÂÍÃÑ«¯Ü¼qíÊdT}ö·\x000fÆUÕ4Íl\x001a«"5M-ªî»H\x0002ZÄâhÿ KÝãGìàà\x0010\x0004ºÔ
90[\x0005M\x001cX\x0005¡¯Eóª\x000c rÐC¹\x0015Õ@L\x00126uCÄª2ªªWR\x0011öL¨\x0016±L¦E5.ª
¹\x0000®\x0004ÌK\x0006\x0018Bì11ÅèààðüôôÉG^{g\x0000 Au;B¿Îæþª{Â`¸#kïÂkÛ9üã +HÈ@(\x0002MÝ?\x0001\x0000¼*\x0005»^°2föé°1d\x000b´k
÷$ÕÜuªR7ÍÉÉÉüô\x0019)£°e¶\x001aÙt<-\x0002S(x\x0004uÛå¼¨ëåª~<:\x0003P9s0\x0016LD	Ô=!\x0012#X´§\x0017]Û)\x0002÷ "/ö¾­Ê\x0004l¨`\x0001H\x000cP\x0006\x0016\x0006Yo©d\x0006hª¢\x00192$Çn@0t*{± 34!\x0000QÃ¬³£ß¨ÏÉ\x0014\x0011±L´Z\h\x001eY%Nw
@n"±»
\x000cê	ýÖD\x0008`Ïdd~\x0017gmID!4M#Á±\x00079¥\x000c\x0000(ä%¾n
 Ir×uu·]\x000bªjrãÆGNf³Ùl:­ë¦ëºù|>\x001dM7·øÙé³¦iªª*âúÑa\x0011.5\x0000Ð¥\x0019xÝ5MZWå´ªÆ\x0007û\x0007ëz-Y2\x0002õ9%/áPQÄétV\x0014O»ºb9BDéRJíÙùé\x0001\x001d\x0007¤\x0010é\x0006\x0013i=;zC)êõ>Ð¶\x000fÅî>ºØÚI§Ä"æ¹SµûzOÛ¶Ä!Dçj¹Q¿võ{v\x0008öC\x0007`(Uö-\x0001÷Ä Sf\x000e\x0001½\x0004þs\x001f?KUæ§ûí-0!P7\x001f\x0018vK\x0006\x0005\x0001r÷òªÔ%\x0015\x0008Ímª\x0011\x0004®\x0017Â\x0018\x0002©"	°aôR3[º2rTI\x0001sr×å$*ÙröÊb/ö ª\x0002Ù2wÙ\x00106J\x0000¤È\x0000 `]NI\x0004\x0019\x000c\x0003\x00180!\x0007î+FÐ·{î"½\x0018p\x000eÑIO+pñ\x0013$§bB,BÌ\x0010ÄHU]rw;é\x0011Ñ9&LD\x0006Ôµ²êVbJ\x0004hÀÃà¡%K_c Ü<_\x0000\x0008½\x0013 ö%³jaD\x0011\x0002\x0002\x0010SÎ\x000c6\x001dW\x001b{1ÙP:
1FE,LÇUjÒl2ýk¿ñõ\x000f~xg¹hRgÅj±X\x0003\x001b^\x0010@f \x0003¡%Û3uF¤\x001b,ûC&¨}¸¹+¤@=ð\x0005ü_Üz|Cq,çG\x0008\x0010: È\x0002
¸\x0014§\x0018§ç±*c9ò£:;],=;ç\x0000ÇÇW¿óÝïÖ«UJ\x000cWÇãr2¼÷ýïµ5dgíð\x000b_üüç>óö\x001b·_-ðÊ­W\x000e\x000e÷ªQÑ4kWll.U\x0006Þà\x0010¥\x0002o^½ÖµùÎ\x001fÍfÓãÃ#ÕÔ,æ\x0000\x0010\x0008Ü\x0016\x0014\x0007\x0007\x0000\x000bÍl¦YO0$õ?±çÐ\x001bÛ¡Ô«u\x0011tùpÿ ©/¦\x0019Wd1³\x0018ãhTíïï\x0003PVÈmcÈ}:HDL<Î²ôÖ	2gU\x0015iê\x0015\x0000\x0014e®çÕ1F/°ds~Î#cå\x000fí\x000fÛ2.?"¸c¯Q\x0019º&?)Cè% A\x0001½Ç´Á0"ì¨~ê¡ª¥g.+AV0b\x0016I\x0017Ë\x0006%»¯,\x00020\x0002\x001aìTc+)°\x0001·¢Z·P\x0003Àú|^3 \x0010
'\x001aC Æ\x00108 GFB\x001b"ÂÂxÙárÝ\x0000¹þ¦\x000bÃX\x000f¹D\x0004°Á\x00181\x0010¡\x0001nKÑL\x0013C\x0008!Poq¿ùj3SéYKà\x0013jX¡Ô	¶`¦D»\x0004)m\x0008!pI1p@f(YiãÓ\x0002\x00002VCK\x0011»k8#Yn»Ô¦EÛ-R¶ A!¨dÀ\x001bÍÍ\x0019
:Ã\x0000\x0000È,yÕ6y¹\_íSE"
ªr||\x001cc\x0008¼\x0011Ýªúrýúõj5Ï\x0003w]êºÆ@\x0018\x000f\x000e\x000ef³YÛ¶uÊ²N`4\x001a\x0011Q\t!K\x000f\x0006,äè\x0013\x000e¡,ËÝ©\x0013\x0002¦$)g].CQ¯^I*YÑ\x0006ýh¯ ¡*¶!¥\x0012±kÖ¿85·T¦6ÿf2ó®ë\x0002PUUªZ×5¹P¯§¯"DÌ\x001cÐ÷¼A\x0016¼\x0002ó<\x0012\x0001Ø9g\x001e&\x0005Fcz^nþç5p'Ú
Í±ÝÏ\x000e\x0019¦\x0002mê/þlC\x0019?²:ð\x000c\x0005 tõ	´ÀA£\x0002¸£\x0004\x0002ª%\x0001\x000c\x0018L\x0018],\x0018\x0005¶xñ,ª`}D¾Gä¬\x0006`SO£é\x0001¢flÄ\x0006Õ\x0004Pzé©>ý¤OÊ7
ò\x0011\x000eÚ\x000e\x001aÄËÏV5g	È/=7wÝ«ð\x0000`HD(\x0006¤ºirvE\x0019!2\x0007UMNÊ\x001c@J8X®÷$ßç¾$r(ËHh Ù-*È\x0014ÉÀ4£JYñx\x0012c,)§\x001cØu\x001aüÈy2 Z]¯\x001e||2Íé~éË_þòë·_¿ÿ=¼ÿh~±N¢mÊ­Ú\x0007÷ïõs}\x0014¢¶íå)\x0010\x0012õ\x0010g#ëE¦]\x0006FaPÿÛhö ö\x0005C_½0£^QÌÀ »u¹æ¾ðW¦Óýñt/\x0005bê:9¿¸Ïç\x000f\x001fÔ¿ôå7Ü\x0017\x0000ÔàæµãÙl²7!ÓÇ÷ï?:Y³GK\x0008\x0005ãë¯¾öÊ[7®^¥\x001eEæ¶VÔä\x0004Ú¯2ãÑØ¯sÊI57«5S<íiÎ\x0005B2\x0018b±\x0011n\x0002¯©ZV4`èÑÞ¤Ñ\x001e=Þ§[ÙT\x0007§è¶b2V²,¨i×DD\x0000j\x0004ÈãñDD\x000c e4C%b\x0005\x001b¶a\x00044¢0N\x0000 §Ôu]Îéü\x0014Úº6Ã\x0018bÆ,\x0000\x0010 îX6öJõðB\x0006³³áÉeÑÞOLu\x00022¢ãÁÓ©O|r´\x0013T{ýI£ï¤ö3Z\x0002\x0016¡I3(\x0004D\x0005c\x0004\x000e\x0018\x0002f{£ÙA1)CpõhM"Á\¬[Ú®®s =dÑU\x0001\x0003F\x0005c£Ö¸Û:+ýÔ6u­ï½wM#\x0003£\x0015l)ÀØ'x1"¸?\x0017e "æþûÜßÕîÞ(Ø	¢\x0000f³V¤\x0013RHAû½*\x0005\x0008#ãRÑ\x0004`0\x001cV9\x0003@u%\x000bT£Þ!Dwþg\x0003È\x0000l2A¬b\x001cE^gdB7'\x0011/¿è\x0016^jÛ^Ï\x0015I 
Mêuë}\x0000b ÅbADM¦Ól¦XUÕÞÞ^ox®\x0002\x0010\x0008	'ÓéáÁÁí×ow][\x0014¼·?mÛ\x0016\x0011§ÓéG\x001f~üÍo}·ërÎÙÌªª\x0012\x0011fL)aN)a\x0006\x0000«¦q=û¢(ËE×¥"Æj4Ê=
x>O÷÷\x0002]ïR*(t7³KUÑ1\x001b!\x0003DÙT\6¢\x0000¾ö*yxÉ©w6\x0008\x001c\x00101åäµv·7\x0016Á\Ù¿7´\x0010ÉfD\x0018~,öÒ\x0013±ÉfA{v\x0015ª/\x0005öó#]ÿ[\x001bÖc\x000eûgüÅPÈÌ^¼<Ï2P´ð\x00037m\x0002/\x0008\x000c,}ÐÐ;Zy9Èí\x0019#\x0012\x0004 f\x0011SäÊ
ÍÈ4\x0010`à\x0004Àb\x0001c6ñ/@D"_8<_ÁDSkæ8\x001eFÀA\x0004\x0000Y\x000cX\x0016×Ð§^l\x0007\x000c\x0006¬ábøP\x0000ÚE\x001c\x000esTû\x000bâñ\x0010 "0¡\x0012\x001a!¹\x0012zaÆÄ\x0006fÕ±\x0017\x0000¾\x0013Î%§Á#¹ø¢¢ª4uÓ¶¢\x0006 ,Ê²\x001c1p×µ]ê²äþ0	
aÃÊëË\x0000\x000c\x0008¬ÇßDf\x0004\x0000\x0001@\x0003!\x0011DBâ\x0000!\x0006æ2\x0004æÀìî6C7×ÍÇbQäÔJ'{ÓÑãGõûwß|ãÕk×\x000fVõY³®?óÎÍ®Ó¶Åj½êÒÁaµhÖO/.\x001aÉ]l¤g)bç*Ï$$\x0006\x0001Lu×ÈÐ.Í*ë/&\x0019 bNÙáæÛê¬¾9\x000c\x0005 ªF*vãúMÉ\x0016¸8¹xxúìl¹X]½Z\x001c\x001f\x001dÝ¿ÿ\x0000V+\x001bEØÛÛÌ³Ùøý÷ß¿8{öÎkûO]HU\x0007o¼q»\x001a\x0015HÖ¥îÆÁýÙ\x001e¨6u\x0003\x0000E,6®7Îmõº®ÏÏæççgeY^=¾2?;ýèÎGUU|é\x0017±\x000c4Ú+FUU¯ë®YKD³H\x0006\x0015U\x00055\x0006\x0012§Ç_Ý²±©êb±X,¹ñ~,B\x0004Õ+GÇ÷î/%{Ô¯V)¥¢(±!3²ºö²\x0011\x0001¹\x001d\x0001\x0002\x0001R°
Æãvo¯^¯÷ëÕ²ë\x001auè?\x0005#T\x0007Í0«*3\x0005\x0003\x0010Éä^¬¶M.w[¥x	ÛwµUm\x0010<B\x0002P\x0003B\x0004Ij&"*}V\x0000Fßóøâ\x0001î #0dÐ­IÓK\x001b_ô\x0016ê¨
\x0008	Ä\x0008±\x0008	\x0018\x0018ñþþh6\x000bÕb02Apà\x0012\x0002P(x\x000b&Øt:ýoÃÚf`Ù¤\x0011CS\x0018 \x0016\x0011\x0000ÍÁØ)\x0002`!
çóîÏ¿ù\x001eBf\x00042
 1ôûYd\x001e$ÑqY±ÿ,0\x0013cUU\x001c°(¢(b¸£b.x#"]§¹³°ëÌ@xðÊf\x0011
2a\x001cUc(
	\x0008ÌèB½)¥;\x0000\x0008S\x0002@\x000e±dîÁ\x001fjê6ËFM+Ë¶[ÔÍbÙ®².ò\x001c0"ÄÀ\x0011ðf.ìB1\x0014A²)q\x0001[U0\x0002GY1\x0017!¾ñÚ7¯_ß\x001d4u\x0013
\x001e&`Þ13PÏçeYPÄ"ü{¿õ[ÿüçNN\x001eO§c3yúìÉÍ·TmïðÛßùî7¾ñ­«W®´íW^yåñ£ÇåEñÊµ\x001b¦hªÅ|>ïºnÿsû¼ªÝ¹óÑbq1Ì"\x0007\x0000%\x0000èR³®»®	n&d \x0001ÉÐD2\x0003\x001b¹ö\x001e\x0004\x0000ØØbo\x0018®*"à`Íä\x000e¦!Fçcs`÷\®*:æªi\x001a"*"·Ï"\x0012%å¸\x0011<ì«¸
r_ßC\x0003 $BrU\x000c_?\x0019ñrÄHÚ²È§\x0001Ù¸&K¿-õ\x001bú V´ÉáwòO¤Â`\x000fóçÎ{Ã\x0007\x0003 ñê/"BFâ¾ý½\x000b\x001f\x000e\x001b\x00111y"òÜw\x000cûôG ­î§\x0013\x0000\x0014\x0019\x0013\x0000\x0018\x0019\x000e­\x00117u$\x0006VôeX\x001580s\x0014\x0013G)3@o4g 
],­©©Bà\x0000hbH\x0000\x0004@"YUÄðgï\x0016nzÐ·D6Í¬^U}kE1ÜÉOÑõ'D\x0016ÔNr:ÞÛ"ÆP\x0014QTÝýÜ1ÄÄÀ¦¦âÅ¡\x0017î\x0011\x0000¡	 .\x0010\x0011"G'\x000eyÍ\x0011²ví\x001ab\x0008®Ö ¨+\x0013£{Z\x0002bYÂÇ\x001f?xðñ½·ßyó[WægÏÎÎÏË"Æ Ä-£É~×®Î.ÖëUÝ&É]Ö¤mSNzÊ¤¦¤`ÖK n\x0014ÎvrÎ¾ \x0008¾@tPg¯u±}6È\x0010ÑÈ\x0018@û³éÍëW_{íµõbµ^Îçóù³gÏrÎ_üâ\x0017\x0011±mÛóóEÊðK¿øúÁÁáÞÁþj±|üðÑdTí\x001fì?9¹\x000cû\x0015\9:\x001a\x0015eÛ¶©©»®{±DçC×Öç§g\x000f\x001eÜ???_,V«ùbµ^«ÈùÙ³G\x001f?0?ùÃ?ºztxãÆÏ¼ýæÑÑñ¨H9H7<, ª9K/*¢Ü+U#\x00130q\x0011c(Àa1.¢\x0016¦1zÿ(R$\x000c
D@ÒóC°w\x0016õÎ\x0014\x0000b,ËbäÍ¦¶-z]l0$$%ë
H\x0010\x0000H~îIï;¤½ÿKZÉ8DUL\x0006Í«OZ,6*p¶S¼ÙÊ
<ßÕºDdõ2å þd\x0013\x0002\x0001c \x0018'ÓÙþÁÑx:âH¦=xâ ¥³ë
»mÐ\x001d\x0011\x0005\x0000pÙ\x0003FäìQ\x001d÷|@_ªS\x00120D(E5¥ðìtd\x000c\x0006¨\x0001\x0004mhm£ö
&Ä\x001e§É¾Ü\x001b\x0012èÎ\x001c\x00023\x0007\x001aê\x0001L=\x00150 ;\x0004ÛuÐ·á¦{:Æb?á$Yàº¬â¸ti©\x0008 ]Àr\x000cC\x0000¢"Äé8ràùü¼ÛxÓq\x000fÔ\x0000 rrØ¤ZÑd,«= äÂlÃBd½üp;ÐëÀEY\x0002Aär4QC2T D\x000c\\x001c\x001c\x001c\x0000d¹vý\x001a\x0000¨@×u^ú2$ßÂ»®K©÷öö..ÎRJu½BÄ¶kU\x000c\x0011Ï/.$A±(*S\x001bOÆÄ`fëõÊÅ;\x0000õá~t~6?<:tE«étöìä1À,  ª\x0006)¯ËÅùÅµ[7ºós'4¤ÌÄl
YÌ \x0004fî\x0019ÈêµÄm\x001eò²¸@­zÓª,ËrÎÒ¶m$"î¾D3\x0000\x00103
ä6wáÒ3^Ôß|±c`uûRö6ÄÂÜK«\x0017ÿË\x001f4Ï5#ÍÌ2¢G\x0007½¾îPµr\x0014+:Â;Ü!l~õÜØDC½×ã\x000e7gøs\x0017[#Ð=±ç5l§\x0010ÐÙC5½o\x0004@îÜ¦PYÅb9h\x0012\x0001f08¨©eÉ)\x000f7TÌÀT)lÍÙõgm
J=|=Gis\x0005ý\x0018ÒõØýÞÁX7d?w#ÊIÛFÔÀ¬\x0003\x0011'Éë¦ËIL\x0011ÐÕuQT\x0007§7e"\x0007Û:\x001bÁqÄf&9\x001bj B\x000c\x0016\x0008«#\x0005t\x0014\x001f¹J\x0018\x0018
r\x00164¥ª
\x0018KJ\x0019MFðàþG\x000fîþå¸m^
#éRUA`-Zm2Ì (ÐA\x0013ÖM×eÍIº.·MêºÜemÛ¶îZÉîì=Úd·¹N®*Û\x0007þ¢2xíõsÀ\x000cDD\x0011}\x0017wyRo¥eyíÊákW\x000eöfó?þøüì|±X\x001e\x001d\x001dííí=~ü¸®ëÅ\x001afp´x|õxooïã\x000f\x001e>zòöë¯Þ¼võ\x0007ïÞ-¦0\x001dW¯Ü¼±·7=M÷÷÷2ôÓ\x001bk3­Õ\x0002Ád4~éK_ºrxÜ4ÝÝ>Z/ç]>xïûßúö·ÿâ_ýÉÞÞÞÍëWoß¾ýúk·oÞ¼yóæu\x000eØu\x0003¸\x0016\ÃÇËÉ]D³\x0015±*\Äª(ÀÐÔuuëºKÄeÙ¶­w¿½\x000b\x000eq 9\x0004\x0005wPù¨ªÌ=oÂ1UUÍfÓ¦YuDÕDÀ¸¯âð¦0#ÊC4\x0003;xFï|m¡-/][fÞ\x0004ÆïéÐ\x0013u5°gU\x0008QKÀ@Që\x0002Óp1\x0011dG-C\x0007Ñ%#bµ\x001cª\x001aWÕt6\x001dÏ&¡\x0008Äh4\x0008íÃn¼âRäÏù«\úÙ}å\x0011Ñ¹Í.'àÕ+ØÀPÜ\\x0005£Q\x0018\x0017ãY¨Á\x000c4wy(t·\x0015Ì`ð\x000eô'DÐÑ»~\x0007Ã?ÜB  ×ÙE xZØ«¬>xâ)b\x0008TUÕh<ÚNFU\x0015b.%¥¢èjÈ\x001buãÉtêV\x0000P×ËÅ²[¬ m	Ëq\x0002\x0014£\x001e"¹\x0015mÛMÜ{°ªTTæ\x001da-\x001f.$víÚ
\x0004N)9E4©G£Ñ¸®×MSß»{ïôììðp¯\x001aU]jVË¥o\x001c·nÝzôðé­·\x0000h±XìííM§ã¦iëzûu\x0005ÏçóÇOJÎ7n¼ríÚµ\x0018c,G«õz6±\x0013­¢]¯O\¿q\x001dÜ$\x0018Á[}¾e¢¡KF²;¬¨
êÕ6\x0010ª]¬\ã{ð5s*©²2"u]\x0017bÍ¦>Ó¼}R²\x001d[@wñËY/=!nê"Î\x001eï\x0013Í^³[\x000béç¶+#þ\x001c%òüã©GL<\x000f¡GèÔöf½H ôgn^ñÍH¨\x001bñ¤~u
ÏùcýüÆ®\x0002C\x000f\x000f\x0000B\x0000Ù¤îèíi&¶`n?îjD$tY\x001bÄèí \x0001 ç¤fLMÅpã?¬\x0008\x0002¢.öéÆ'UÃ\x0006\x000eM.\x0002?þ[h¢¹MyÝÔr\x0019Æã\x0014D\x0014Ë
\\x0010\x0010¦$ÎC%"NðÒj«¨`Ù4 "À\x0002A$î	\x0011\x0006 ÆH\x001c\x000b3Ó,Iº\x001e<\x0000Ý­ë¦É¢`:ëº}öì<u\x001dX
¡¼~õÊÙ³Ó"4h\x0010#"Y\x0015F¥«¢ë$¥$ÙrVÉæÞ³u×JÎnk¨âÂ\x000c}Hë;

þ·©q@D*C@7»\x0006õý\x001cù?LÊ²\x001cFè¾Ô¶wïÞ],\x00169Ëõë×ïÜ¹sçÎ\x0003U8Á;ï¼S×ëÃÇ\x000f\x001f5k88Ü»qã*DÙl|||ðö;o^¿~}6Fe\x000f\x000c70w'\x0010AD\x0003¯]»öÆk¯\x0006\x000e«åúÉ'\x001f<9??[/\x0017Ò¥éxòõ_ùÕw^¿ýàÞÇñ­ï}óO8ÁW¿ú¿ò+¿üÖÛoú^éù·ªx¿mÛ¶mÍ°îZ1\x001c&\x0014
%
\x0019RÎ!DÑFD\x001dÕèq\1Æ\x0000Ü3i\x0019I\x0007ÇÓ\x001e>ØG¹^iõÎTUÊ²lÛ:¥äµ\x0001#3"×;ï\x000b3DC³^JÓû±£GëìT(?å@$çÛIy'\x0019ª9ÙÐÁc¸Ém¶t+p \x0006*eÌ
\x0011cÁÓéx:2Ä\x0010=ðÐþõÏ\x0019Ý¿´N\x0003Z®©\x00084¼Ñ»\x000c=PFM³dDVÇv!\x001b\x0006\x0003D&oÝ@ MØE=ÑÔ×@\x000f\x000bú
²\x0007ë8\x001a\x001eÕ\x000cEÔ@9È1\x000f&\x000cCXcÃ%Iþ!]êÜÔp2\x001c\x001cîíMgãÑ\x0008\x0000RÊu½^\,ëºN)¤£=ìûzpåÊ\x0015\x0000@%\x0000¸qý¦Bx²h\x0016\x001aê&+P\x0006\x0005Té£Ø\x000bvp\x0002
!\x0000@:EJDËu\x0003çË5\x0018!ôØß?tPíã'OÆ£1\x0007\x001eF¼1ä\x001c³Ä¦iÆÉrµX.þ`6Mãát:16MÓ¶	\x0011Ç£1qo
S_Ùßg§§©é\x0000àìì\x0014\x0000¦."'Q\x0011$$ÆQYÔmZ\Ì\x001f<xptx\x0005ø\x00054$\x001bd5c3se\x0010gÂ£3ÿ7\x0004:É"ÊLÌA4\x001a1!£dÉ)+¹½N'Óýý\x0003'ÊM§SWwÚâg\x0007_Õ$w·æ](1\x000cE\x000b°Kñýî\x0012\x0001øç\x0012^ü[\x0019´óg?º.¹\5QDö\x001e
Xa½\lo\x0019hG°ï¥k¹EñPª²Þ+@\x0011ÑíshÇssõ%[\x0015\x0001
}!g¨d°\x0013TP\x001d²F\x0006
!°KÀùÍ@Ä\x0010Ø\x0014zmSÊ\x0014XDX\x0008»
2Ê]çVà
´³ïU¹6\x001ac\x001aÎ\x001d¶½7c&èµÞEû·¼\x0004><0ä\x0006bt/Íé	³É&3Q³ÞýÐ¨K©nº³\x0019\x0010ÁÁþ´^×Nn1VÕxU\x0019`UNÎæç¯½vÛ\x000c>~øp<¬\x0006ÄÕQÝ\x001d\x000e»\x000bÌÌ\x0014\x0008¹1Iÿ#\x0000K\Oû,
L`³IZÕ<\x001e\x0005E\x0010Ñ½=þÑ>úî·¾ÿk¿ö+àáÇ§³É4N§)\x0000ðÉùiêººM!Èh\x0004D!'éZi¦ërJ)ë¤/¹A`VÉâÆ\x0014.Ï\x0005\x0010&\x0012¹fiÿSd½³R\x0014×\x000e)°ÅèÕ[7çç§ßþÖ·»¦í4©Ê\x001bW¯}ÿûïO&ÕùY3\x001e\x0017*ê6RËÕòÎ\x000f¿ô[¿òµ¯üþÉ?¾q\x000f\x000fönÞ¼vòôáÓ§7g³ÉñáAU\x0004gB)\x0000BO\x00075d@Ä2Ôu÷>¾ó\x0017ÿú/\x0016\x00053\x001dì\x001dDfÑ.µ]jÚ\x0012Û¯¾vûµW>xï½u½úýñíõGßþÿã¿õæ;o\x001f\x001d\x001dÇ#ÇYç\x0016\x0017çmÛ¢ÚtRå\x0008)\x001aq+À½%ÙÞìÁË?ûù7~øÃ÷b¢r~~\x001e9<¾w÷ú«o©\x0003e\x0000uÓ\x0003F\x0013W·q^ü&W\x0003B\x0000\x0006\x0014\x001aø¢DFÙ\x0000ØP
T7\x000cBìKdf\x001bY¼ö·w­ÿÍÐ%B"\x000fÜMM\x0014\x0008ô\x0012\x0000qËD°\x0001æ\x0019\x001cðaN3ï	!!¨×3\x0000Õ°\x0017¯óò©¡	\x0019µ\x00138ögÓÉ¤â@æù5
íöÍJod\x000em\x001b\x001eT²Íþ¡
~\x0016½\x001b
9\x00041y(£¨¦FHf&Yz¹\x00070\x001d\x001cÔ}u\x0003RÄà_äS\x0019a¿Ç«\x0001»À¢*"ÅX\x00001\x0003\x000e¨Þ~»Úu\x00147ë\x001dhó\x001cK|zU7Ä¢È8Yµ,HGG\x0001`Ù¼ÿñ{÷\x001e¬W0AUràU(¡,"\x0000 Ë^!"QP$7î\x00025Ä6ç\x0002@o"MT*\x0000ß¹sx|ÕÌNOå$GW¯t]wïÎÝo~ó[ðû°Z¯\x000e\x000f\x000e\x0003ÄÈq2\x0019\x0007æ²,³jRQ\x0000å1gÏ=~ü ,ËåªñþjÛ¶*PUÕþlo½X>\x0003\x001eF±\x001c]\\==:<
\x0004«f\x001d8,.ÎnÜ¸uxppÁó¶Iõj\x0019cÜ?:zòø©"dÓ¾\x0015cdÒu?zïý½_9(b©\x001bëíº@):»È1}  \x0002\x0007UíÅ_À
µTÌ©d\x0001Ñùò\x0019DPIÌÊQ5ÛÔu©1$9\x0004&7²ÎyP©A\x0000ÈYÐ1z¢âjO^3\x0011ï¼azÝ}»\x000fø*\x001cTÁËòp©yºKlÚ¥ÐN\x0013ù\x0013\x0012\x0012#£^êÉ]²7
Þùá"\x0012n4ÎýéÉ;\x001fõb\x0019\x0010Az#m¤¶MîØH!G*\x0011	6æ©=ä£ç\x0004¿|?E\x0012ö©\x0006îô¶\x0007}\x001aDd6áz\x0017G\x000cÜ>\x0008IX!\x0004\x0012`\x00122©¨ëß\x0007ãÎL\x000cB¶ìÖç&»u¤$f?»öc\x000fÜvÕ¦¤´s\x0001ñSÔa.Í	\x0013\x0015\x0015\x00106¥.gC Ú,¡`ãétq1_-WuJe,ÎÏÏ¦{³ð\x000fþþ¿üÿò»\x001fþ(V1ÐIûI_\x0018¶W\x0018ÐÈ+r¾\x0004÷8\x0015d ÂHÄ`dL4 ó¡U¬Ê¦iËUÓÂ~ôÑx<'ftz¶Þn1\x0004\x001eÑ¨ëºº^v¹ó98®&£Ò\x000ca×\x000eÆcg·;öw\x0000õ²À+m\x0011³ë\x0006íÈ!ÆèJ¦fUUàÊ+\x0004zrr%ÏçË£ÃÃ½½½;wï¥ÃCLùøøh:äª²|pï¾føÿ(¹Ç\x000fî¿óöá¾ôÅk×¯«"\x0016A¤Ë9n\x000eÆL@ûe 0i'ËÅâñÇ÷ôþ\x000f»¦¾ýê«_øü\x0017®½õ6¤®>=}üðÁ|>ÿð\x0007O\x001f\½zük¿þëÓéø£>øÆ7¾ñøÇ@<M«êøâââñÉ£Ã££²\x001cÝùèÞ+7oe³óùr±ªçúÑÓ³E×}ðÑã£«GMgeQÞ~ýd¡ËÎ1\x0010Í,g3 º8\x001c\x00131mÉ¾ªYMEMD%÷Õï-'1Î§Úªã@^Ñm`ñ®	h½óêO^ù1/\x000edD¸I\x000cH\x0010;\x0000½áfI\x000cV\x0016ao:;ÜM&U[\x0019þôMg35ôV¬\x001f0÷õ\x001dÇï,Ù	ç\x0006´5©¶¾bÔ¯Ò\x001f,ô]}_Æ\x000cÅz\x001c¼\x0013ûH\x0006¯Û\x001e56,\x0015;\x0000IOÜ]³ÊE\x000eÑS\x0010P0Y¬\x0013Z\x0002±\x001a\x0000.ê4\x001dï_µj¯\x001dF£Ñ°H÷º9=K00"^¼'¤ºòÓ\x0006ôæÌ\x00085\x0005Q\x0010Z¥d\x0000]y>oR÷ôéÙh4Y.¿÷{¿÷{¿÷Ïçóår±<¾rÈo^»Ø\x0013ÅU\x0008\x0003ìX²¦i\x001e?~|qqqãÆMou]£ª!³é^NÉ÷È¦iÎ\x0017ËÀa>»{CÛ¶\x0007û\x0007!z];¸Ä \x0001\x0012S\x0008»NÀÝ|\x0001r\x00162p´YjÚª\x001a\x0011¡ôò²½IkÄï¢àySÉv\x0013:/uc½Ùgß~ò´AÍLDÂ£Þ¼Z¯sJ±(\x0002\x0005U19LÍ\x001dU/{C\x000cîhaær°2\x001cmkYÖoðÛhß"#B#â3»û¿ÙáJHY\x0015\x0014·ÆpÃIkßàÜbe`7Izaxík³´õ¯!\x001a}Ãh«;\x0018\x0006ù\x000b²ë\x000e\x0011Ò`££ÈlC°W­\x00003\x000c\x0001BÀÀ¤A\x0019q`L\x0002\x0000U5¢,]]gÉ\Ä¨MIUz\x0019_QiÛ6¥\x000cHø³Ù¶6ì\x0004¹h\x001bY¤þRô
_?ÖÝÂ_cf]Û&Ñ¬`¦D\x0014JÌ)\x001blÅ\x0010\x0017ëÕº­K&\x0007:ýë¿öõ¯ÿÚ'þå\x001fÿQÓ¬)ºÍ©\x0012º;¨!Ù¦\x0019·{ûL)vi\x0012X\x0000\x001e³(ªó\x0005\x000e\x0018bUUÙ|yE0»w÷á£'§g\x0017ûûéÔ	É1ÌìXD_\x0008Ø\x000fF\x00075\x000cÿÒ\x0017Ë÷¶\x0018vRBìm\x0010/2Æ!Ä\x0010¼$#ª\x000cÀ&ñzµº{çîùÙ¹ª\x001e\x001e\x001d]»ví\x000f~ÿ÷\x0011!Æ{{{×®]\x001b£ÅââÝwïþ¿þµÏæ³¿ÿûÿâ­7ßT¤´^®n}å"Ê@\x000c®K\x000b^\x0008P\x0002
!\x0014\x0000R\x0007Ò=ypÿG\x001füèáÃ¿þ«_FÍºþè[±?Û;;;{øðã×^»}ïÞ½§§ÏªIyuríWíëÇW¯?yò\x00046ÿÅ8¾{ç~³^åèÎGwCY¼÷Ã\x001fÏ×wï=\4f1>~\x000e¯\x001cÕ¨MgóåS'³¤°ëÙû]ê\x00044S6\x0008HÁùp\x0007ß¾\x001e&)g7\x001bmÔä\x000c\x0002\x0002wù1¶`AÔDm\x0000\x0004;¦w0T+?u¥Ú}­×ø\x00120³\x00012ù|CL¢êÒõ\x000exñz¢Ë¾!(¡EÂ@HÂ`Ûª'Pï\x0010áG\x000eÐ3\x000b\x0014¦£Éáþþt<)BôÈØûÛìNÄXg[aÇÝº½n÷0ÛÕ
\x0001q§QåU\x0019 3T0C\x0012@\x001d\x001bfr©\x0006Ü#a ÿ{¬ô²R¥9¿wg\x0005\x001f2ðí§mwØ\x0000\x0010Ñ	A
.%ÈØt«º\x0005¦M@¼·hfÌa2\x0019\x0017£êäéÙÙÅ2Æ>ño\x0006Ì\x0008DÑq3C4\x0010u©b^íb\x0003ª\x0008®ÈÒ¶ír¹4³@ñý÷~øÞ÷ï¾úÚµÏ~ö³ÓéØ\x0012Ì4åì3\x0000\x0000 mÛõj½Z¯RÊ1\x0006\x0011·aÚfó±(Ê²ìºîôì\x000c)ìííI\x0005\x0013f±QÕ\x0002Àb¹MgLd
¡,TÕu½òÚ¯K*½qïb±<<>6Â:\x0003u*¯K')¿¤~ð¼\x000cî&\x0001pä2\x0000l ¾\x0002«ö¼îzqÁªª\x0002±C}
g&URÍb\x0006)\x0001¨¯{ÛëK(nÂæ\x0000¼\x0002Â^\x0005!
!\x0010"\x0010\x00107iü\x0016õ©G_j\x0019,~^\x001f{é\x001cÝ±ã/%Ð¨Ù«Õce~¢üéÒ÷½Ãð¯W3ÇîíX\"\x0019myàÄÆ
DÆ.\x0000G#Ñ `\x000cÉ\x0002\x0012DÎê2¸F!\x00183\x0015HTU²&ÉVâ/\x001d6Äã|î_qÇÎÉëjªfd»aÍf\x0011Vhï) äë<ã.\x0002\x001dæóùzµ
ö\x000e\x001e>~2þýÿà·\x000cä«_ýò\x001fþÉ\x001f~ç{?*,ã§Æ6yi0lLæü¨\x0014}APp\x0015>\x0017&qóùé3$¡,f\x0010Ep½ÑØ>üè\x0004\x0000\x0000A\x0011"AQpQ!\x0004³-`³/ÎËN8\x0014' Y\x0011"\x0013q\x0008\x001bT·{TãÖ\x0004\x000f\x0003\x0007\x0007<2\x00187Pô¥Ò\x0008Qàììüþý\x0007\x001fÝù¨mÛk×®\x0005æ¶më\x0006®^\x001d\x001d\x001e\x001e¡Ú­\x001b7\x0001àÿþ?G¿ú\x001bÿÎ|q~zzzåøp2.\x0016¶m?xÿ¿ð_rqf\x0003\x0001*¡1±¨v©[>ûøã\x0007gg§9ÆPU\x0019.\x0016ÔvMÓ\x0000@UU\x001f?®»V@ÎçËe}ëÕW¿òµ#\x0000xøða\x0011Ç©Õ¢äôl1¯Wùh4úþå\x001f§{÷î,\x001a(J(B5Ú?jóüñ³«×Ë²\®9KÑ\x001déB¡$gG\x0002$A\x0013$\x0005A\x0014ÍI\x0003\x001dÆiÊ9w]ÛuMOJ\x001aj\x0012\x000e9BÂ\x0002GäÐ\x001c³ÞÅæÅ\x0019õ¢sÊNps[D\x001b\x0015KOÍKL7\{q%!S4US\x0006)Ð"#!±G&.Ä\x0010AÌÐ\x000cM@32\x0017ÇãñØçÏ\x0010£|ÊL\x001fôiî\x0017ö!*«'k`uÐ3\x0003|³ôøC?å·Sï¬Ù_aUqX6ôH\x001a!\x00194Öw®áV	¾ÿ0\x0017©\x0004b\x0013ì\x001eýX³\x0002\x000f\x001bd(Ñh\x001c(\x0019ög~Åü¼¼¶Ú+\x0007\x000cÒ·®D ~oÞ\x0010q\x0007C.Wà4\x0013®ëNNÝ¾ýút6+GpõêÕãããu½|ððÁzº\x000e1\x0016\x0005\x0013³4ö¸\x0002\x00081JÎXU£ªª<£[×«QUäÔæÜÖuý¹Ï~öì7Î®.ëÅjuýÆõ³ÓÓÕzýèá£û÷ïw©3³®Ku]\x001b!\x0007.b¡j)5Ëå¢½Hk¯\x000eêº.F8\x0003QÏÛ@11]­cûú2ÛæÊô-\x00155³§ÞæzË	\x0007OQ"r\x000b<Çs\x0010bHv¡^sñ £æ[nTvU-\x0006\x0016­ºmâ\x000c·\x0019ò\x0012ýL¹ýÿ\c¨ë\x000fÛëÎ/³Ho=ë\x0001/®Y»+Î\x0019\x0003lxJ=*Ícr¿ ¶ùç]G®á Ðã5ú¿»Ïô0\x0004D¦U\x0011¤dT«MD\x0019\x0002¡²!ªæ¬}=+\x0018AOI41\x0014s4µáÿ©AßvA\x00000\x0004¢¾:Å;&^Þ¦4UàMÕ±G£ :æ\x001fÕhsõMÅÐèº7íäÙòëÇ³ÙÞùé\x0019"&¶­§ÓÑoÿÿðWn~ï\x0007ïÞ¾ýú×¿þkgç§OÏÏyÀw±ËçmïQ¿\x0019ú_±õx \x0019`+æ!
³\x0019\x0011)@Ót£bÔu*¦Ìr\x000cñs_xçôâôèJ	\x0000\x0003Þ~Èü \x0017ôB$\x001ah âìËs&Ö¤\x000e\x0011CÈ9\x0004\x001e\x001aàùzï	À\x0002\x0000DäöC±\x0006M±\x0007s8r\x0002õüü\x001c\x0000F£érYïïïÂýé¿.K¼~åêjµvep\x0015½{ïîÅéÙßùÛ¿9ªªq9ú?ÿþÿÿûÿÁ~ãë¿vÿþýÕj^V1[
d\x00042ÜÜ\x001dE2\x0014³Uuµ®Û¶ÝÎîÞ½;\x001a\x0010sJ«õÚ³Ã\x000fïÞ98:z|òdT7\x0002¶XÕÄôö[oO÷ö§£IÝÔ÷îÝË\x0019LùôtñÁ\x0007ß¼w§\x0005:Q¯\x001cbºî¤îwPÜ{ºN¦!FD\x001aFççÏ$\x0003$\x0001 w¹Y×ç§Ï\x0004`0Â"V!°xq\x0013R¤¶î¶«²ê ã¦=AÔ\ªÇzÔ\x000e\x0004yAÌ\x0005\x0007Ï¡{I¬}¨Öô«<1\x0019 jfEDÃ `@dx©p¸I+Éú\x000fé[\\x0000Dhâ©DFË\x0011¥d\x001a\x0018=:ÖXgbj\x0002\x0006\x001bR2@Y{{Óé´\x001a\x0015 ¤ÞóéÓ,^EÞ]¾P\x0007	á7\x000b©¹ûJjê\x0019[öbÆ\x000cÖëu\x0002ôí¡Â½ÉîÈ¡\x0006h¦9©HV\x0001¬\x0018i'û\x001fâ\x001cØ@¡/Ó\x0006\x001e¾w\x001b^ø28øµí\g"YEµ,Fóùr>_\x0011A\x000ce]×^$@ÀìG·\®\x0003\x0007f\x000e\x001c²tf\x0004à\x0005T=»h\x0019aìlæ@L«uÀ`»dËáÞþl<iÖõGæó9\x0003Ùj¹äýéÙÙÙh4ºvíZQ[·níííqàýýÙÁÁáhT­×ë,²dQ\x0005 Ñ|óÖßù¿Í\\x0011b+©ÅÓgOXüèG\x001fý÷ÿÝÿÑ®]»Ö4]J©ËÖË%\x0000´m[\x0014}êNd\x0014A@L`½^v©	eðÔ\x000eTY5P\x0010²>|\x0000EèMCsJ:(\x0013Y6\x0001B#t%ªM>¯;øeY\x0016E1|;\x0015EÑÏ"q>Òæ¶ö1©\x0019mD8Ü«7óÚTZ
õ|âMÑ¢Ï(~ò\x0006ëKk\x0002!1ÿæ_	P\x0013\x0011æí<ß¾Dè²qÁÏ>^\x000c>¡ã¾K"PB×ßS¿o±À	\x0000j1,!b\x0004b[s§Àá@%Ú\x0019ìçÇ`ÞæåÿD0uõD% \x001cz+Ûè\x0019¬·¸\x001a$\x0018Ðý\x001a\x0006jÉ@Du]w9!sÛÕu×~þ_øÝ¿ûwÎægM³\x0016éÞzëw>óÖêÛßîº´¥,ìÍ6ák)ªõ\bØð¯[²ú LäøGE\x0001M\x0005Ö«:F+W]½N¡\x000c½Yðp¹±/ÁxëÐ)(¦îEî÷ÅZ×Ï\x001eî£\x0002*\x0012yg\x0006½^B:j0Æ\x0010¸`æX!\x0011¢\x0002aÎºªÛõz-9åÈ\x0014ESüÖ[o}üñÇ1ÄÃ×ßx}¹Z<=<<ü{¿û»«õòOÿäO®_9\x001eFIµ¿¿ßuÝññq\x0011"¨¨ºÍ\x0005@\x000fq÷zo,«W¯·o51r·ªOOO».Êroo½#L\x001cÃÝû÷õê
^Û¿r4=Ü'
E5\x001a\x0003ÆbT'5\x0008\x0017óõ\x0007\x001f|øÝo§iÛ·\x000eö\x000e\x000eC9yøôìéÝG'ç\x001e>=eélT\x0016MSï\x001f¦i&Ä@\x001cÄ u]½®ñZ0
!·\\x0010z\x0002i_>ð¶Nn»ºKI2×²\x0011ñ@z.ÿ\x0010Ä¼¬,òR¬LOx\x0001½û½¬8è^\x0002/Ñ­yñ±\x0003p\x001dï\x001c@\x000bÂ2@Å1\x0010!°*Ô]Km²ÜiïI$`Z\x0015áÊÑáñññhT\x0006\x000e)·\x001e\x001fàFâSÝ¶Z¿tzÏÅ¡}ÍbïÈ¦Â\x0001Æð\x0013Â.Á,u]Û¶)f\x000ea\x000báz)ÏÊL\x0000Pd0EéùÄ;mÖ\x0005ò\x001a³¨0Ée³nRÕÙtÚ¥4Ïwû\x001aeYâ`¬\x0008[µ\x000b*buûýÓzµN*!F"m\x0015²äz]#bQ\x0014Ð34ûÏ\×5"F£²,¿úÕ¯þÒ/ýÒh\IÎ¯¿ñFÛ¶ªÉÌRÊëõ"å6FîºÔÏX\x0015\x0015ÉÙRRD/\x0017{{{Ãt:-ÂÏÂ\x000b\x001eýy!£³\x0018$K!¥L½\x0018\x000f\x0007Ó¨m][V\x0006\x0014r\x000b5\x0011"$\x0002rÙ-@ÀEUU\x0000Ð ¦|¥ÒËÁ=\x000cv{\x0000¸-«xþ\x0006\x0000)¥Ôu×\x00154KJIÕÁ³äÜY\x000föÄç\x0012òÝJÿåáR±LùJú|¹î}£Ô\x0014\x0005UU\x0015TD	zTF_.QýÙB!ºôÕ»\x0007\x0001½½Ç§}Ú8$
6 Æ\x001c)CJ@$"FD±ÀV
$¢]¢\x0008DÆE\x0011B Ë½EïhãE#Üz5+\x0014:@Ø6¦
[?ç6àÁÒ\x0013\x000e|þÕµD\x0007ÈÅõ\x001b
´Ê]h\x0008¡ª\x0017j6ÆÅ¢½~ëð·û?à/\x001e'£ùâü­·ÞøÌgß~ï÷L\x0001ö¡Ð¦0s)Q\x0003\x0017<ÄMÄÃÎ\x000e³\x0010Û$"ª¹\x0000æ¥\x001bº7;\x0008±Ü\x001d$ÓåbW\x0002\x0001Z§[\x0005*"\x0011ô%7nÙjÈæ\x0018@Äl®{ìu/õ
\x001d
Rxf¨43J!jÁ8DD\x0004.çÕry¾§gÓÙºm¦æ\x0018Ål¹nö÷ãd6»vãú÷¾õ³gÏ~õW¿6©Æ\x001f>øÞ»ïE88Ø¿z|´8¿89yüöÛoV\x0001U4\x0003%\x0001bÃ \x0019Jb\x0008¡$¶^]¿vÍrztÿãw¿ý½÷ß/·ùÕW_=8:Es{qqñäÙ\x0007\x001füÙÏ}î\x0017~ñW®]¿vã&Q(§ÓÙáÑÉÉ³ºKÕxzïîÇßùö»&ö¿øå¿ò«¿ZF\x0010Êåï~üðéÜZñ\x0000\x0000\x0000IDATâl}\x0006@W\x000e§9K1v]ò\x0006S×¥qQ¥¦Y,\x0016TV^q2fàD\x001b\x0010W_.5]×¤Rn½	²µ+Gò½§Wêï\x001bM! ªã({Ð-Hî%OoùÜ\x0003ñT\P\x0010C`6\x00176Ûb¢Àwìbm¼Äz=ºÇ¸\x0006ÈT\x0015¡D*B\¤NRjA\x0005T\x0008U\x0001\x0008´¬ÊÃ£ý£ÃÑ¨\x000c!¤Ü\x0019\x00131où>»\x0018¬è°£Cc$\x0002ä\x0016âÏáÙ7a¿¯\B%n\x0001\x0007XUÛ¶]­WEQÄ\x0018hÌ\x000e ÃíÚõÂç«)fÃ¾Û÷\x0010_&\x0011úÂ¦{évF£wÞy§(û÷ï/\x0016Í§$mÛ¦®s\x001a¢Ë\x0017¥Ô¼~ûwÞyçâââþðD]Ì°(F1ªÐ6i>#RY\x0010ùôô\x000cz\x0002Øß?\x0000¢(BÇÇW¾üå/§Ü_\iÓ4mÛÇ@EQxaf<\x001aål"ÅÌ@r+\x0002ËÕ\x0018\<·,#\x0011ä¬uSÇxÉzÉ[N\x001ea÷*\x001fÞ¬'VÎÚ¥%\x0013SAìÎU\K\x0001±÷5òâ(1A\x0006W`"\x0007ª0\x0013\x000f\x0018\x0000UÛ\x00009õ:Æ¢ëºÅbé\x0014}A\x001bnM\x00083¼$\x0018\x0008üÊw_êCè\x000fÐ©ÞaÚînÛôág\x000fj6ËÄóv~ÚDÏ?ù\x0001"ÙNÕÖ\x001f\x001cÁ©ª ©Á\x000b0sU\x0006.'d»%áç~GÜ¨!\x0000\x0002ªXAUUBQ²B¶Is\x0016R,F\x000cfjYxú\x0001¤H}åÃl7 Ù|÷FuqÓ\x0004qhê_~ÉÕ1É^,\x0010§n­Füêo>ÁÌüq\x001ej\x001e\x0000àhy¬êÁ¥"lî\x0003\x001a aQ\x0014D´ªëñlÔµíJáoü»ÿî¯þú¯þéýéÞÞ^Qåj±·7}ëÍ·>ûö;ï¾ûn&WÕ\x0001Pè\x0017/ì°Þ\x0006V3Q\x001dT\x0012T\x0001\x0019\x0007v1\x0000\x0012\x0006
þ\x0011 ÇXvn\x0006
\x0000ëºIëº®ëµGc\x0002.Yæn	¤èEò\x001eKÉ¤hÆàÚò\x0004\x0000là¤\x0019\x001eÌEF;á$"*õ1
ô\x0015`\x00045s\x000btUS\x000c\x0006C6mÛTwízÕdÓj<éÚ¼\¯ªüá~\x0014Ç\x0005W\x0005FFDU=;=}ýÕ×¿ño<}öäw~çwîÜùp2\x001dß~ýÕÙlR|§X,/®\=\x0002\x0015#\x0014A"4CWÐõ¼ÐçLN9å´¿Ú<Ý=¸_7Msz>/ËØ¥4C5Õ
~óoÞúê¯ürÓ¦éÁ!Qeyv~vx|lf\x001f~øá_|çÛO­¿òïüÝßýÝ6K·^Âb±zúôéùù¢\x0011{ëæ+u]æ×_¿õðñÙt6ÍÎÏ/¦{{Y¤ëºu½*ê e$\x00053\x0013D$F\x0017uþÑBUÈYºÔ¤¶­\x001db#Y©W%°m3Å\x0011iÜ\x0007³~rá¹
MÿXì|&ôP\x0000ì9Ã?Áè½\x0015	"sIX\x0004D\x000cÖHJmR+*@\x0008 E\x0019÷ö¦Gû\x0007£q\x0015\x0002;/&0\x000fÓ\x0010¾|Â¹\x000bÑæôÂCõgL]Ô\x000b¶µþgUe0w"\x000e¸\x0013Ê¼TÉÓÉPmÛ:z´,Ë\x0010Ê\x0017¬l'`2\x0004\x0014ÍÉ\x0006ß\x0018ñS"&¦@88!öíÅÝó%çß«Íf³_ø_xåWîÞ½ûî»ïn>¿mÒ³ÓgO>í+\x0017Ò
Ì¦vttüå/åÉ'üÇlb"êó(àÔâº®Wë5"\x0016±\x0000²,÷öö¢hÛ¼e)9ß¹óÑ½{÷Bä¦©cäªª ë\x001aè×\x00103\x0013$.Â¬íq»äô5=ØÅ¢\.åE5ªY\x0015rî\\x000c°?þº\x0006°Õri[q\x0017î`×¥®!
3Y
ÅqyÖß;D\x0014\x0010¿e9©q\x000c\x001b0
\x001dI['\x001bäu\x0017UUå²\x001bÉ\x001e\x0011l\x0000Àh.S.©½<&þÊ~ýCºKÙù_ðpi+5í\x0005 lg¨j\x0016\x0001a"y1t¹\x0004û}ñTëûîþ=³é92\x000e|
Â¦\x000f\x00016¤`¯|Ð\x0013÷
É\x0008ÐÝ³U)Èe\x0019G]ÎÉºD\x0001AÀe $XV\x0005Ä^[&¤m§z\x000e¤\x001f3Ø&ÐÛè¼À 4Ó¿cCc\x0003\x00000Ki*f¨2ôwJ\x0017îÂÀ\x0000(¨`hn\x0004Ï½\x0010ZvquT°ïÖÄ@d'g\x0017Èxõúµ»\x001f?â\x0002~çwÿæoÿîÿö½\x000fÞ?8:`Äª*Ð4§|õÊÑí×^yðñ½Å£ý§OT\x0003§ËX«yù\x0007.©ó4·§ITRð\x0015\x0004\x0000\x0014- ·\x0019\x0015¼c @\x001a\x0010Õ\x0010P>}b\x0008\x0000ELT	P\x0007§NÛÔÄ\x0000\¿\x000cÑHQÈ­\x0011Ð¹"0\x0008ðxËúw\x0019\x0012\x0001+ß("#\x0013Ý\x000fÄ­\x0019Û6ÍzÝ6©cîQM
\x0001«8=8íí½õÏ~üðñGwï½ýögþÿá\x001fÆå/åË¨öú«¯!IÓ¬¯]?ºvýhooÏ	´\x0003²2\x001a*zR-5-\x0016\x0006\x0000!\x0011L;h\x000e\x000f\x000f¾òÕ¯^9:þÖ7¾õ\x001f¼7\x0019)å,\x0010#\x00087nàÓgÏ¾ñ\x0017ßþÚ/ÿê²íÆ³b±8çÀBº¬ßùÎ·NN\x001eß¸9ýÌgß¹wç£U³Nb¯¾ñvT{zzúàé\x0002ìOÇo¼þÚÝ»w×ëÕÝ{÷b\x0001\x0000°^¬X<=9+F¨¬Kä ÊÌ®`ä	\x0019ïV¤³e\x0011É9KjºiV®
âN!.ÇÖ×ðvP\x0014¨Ú×ZÍ¼ÀéQúÖéWÿaó¤{r\x00007"\x0011\x0013)È_|7KÖð yyÆ\x0000 ¢AD(\x000bl)·)¹il¯\x00032\x001aU{Óéx\±è\x0019Î(w\x0014³hC=
âÇ\x0006'ÅËkÝî!ùêá«êöçÝHe\x0008JÜ#F\x0011QúÝ.¸e6ª
"\x0012\x0007f"Cö·øw!21Gä(uxÝôfLC±MÆ²i\x001fÈÀ'u¡\x000b\x0004Ð,`¤Ü\x0013©T{Q;¿k\x0004`=®bý)É\x000fø£zÝ~ðÁ\x0007]«Q5\x0019«jtrrRUUà@LHU)º\x0019B÷äÉo|ã\x001bmÛ\x00151z:®ª"ÒuPåb±8991³k×¯Ý¸~ý\x000f>0³Û·o·mûôéÓ+W®¬ÖkSC²u½ª¬NÇ«Õz¹\e/Æø&æ\x001d+×ÞYÊ F^Õm\x0012"Gã®ë®_¿Z\x0014ß+Ër>\x0003Û§3\x0000p>stu;\x0018?¤¨H»ù|.*æD-¢ÔÔ!n«&ýf:\x0004å\x001czsR2\x00000qw}\x000cü
{áAØt:íR\x0003\x0000!Fëµù\x0005wÔÝ(÷Ëó[ó¦¹\x0003}EdcDÏ½¥gçõkõîÓJÛ½\x000f\x0007ì#¼«øc\x0003 K¥\x001dÉ§\x001f:Èõªå¾ÂaHÓ)¹ÕÛnÖ»*ã \x0014÷s¨Êì\x001e7yÁ÷\x0005Ï¦~Ýxzñd	\x0001\x0019@ÀÌ\x000bh!¢( \x001dç2\x0014%E¡ÊBÎ¹\x0005\x00014@U%eçæ\x000f¯Øv\x0019?ÅU¦Ë\x0019 \x0000\x0011mcÜ¡êÛZ²Ï1$\x0019"\x0008\x0005S\x00013Í*ê\x0011Ýæ²\x0018,\x0016Ë/|æÍ?{ÿÃ/½õ*\x0017ðÆÛoüÖ¿ÿ·NN¹Âá\x0000ñË1Òd|pëÆ_üÒ~ïýÿ\x001e||²?«]SåÅj	:Ú\x0012/4
½ó¾\x0010\x0019=DhÍ\x00067fí+¢¨Ì\x0001ÍSìº®Ë¢¢>ÓÝþ#oî ÑÀ^}ÉõÜ­):³©ïð\x0002Ø\x0006£ãse\x000bÔ\x001fè\x0000Ì½;Ãü\x0005#S.§Å|µjjf.G#fFÌI²"\x001c_»zóÆ­@df?xÿýéÞÞµ\x001b7\x001e||ïáÇôµpppT¬Ö\x001d\x001f\x001d\x0006¦\x0018ùøøp¹\_ºV\x001eÅ09´\x001c1q\x0008±,Ì\x000cÊbôÆëoT±Æ·o¿Þ4õº^Í\x0017çËõÈbUÞ¼q­,KE\x0010\x0002A\x0012ñ¤Z.æ«Õb2©ÆªY7ñÍoÞÙßß;Ø¿rýÚÓg'\x000bäÀÀ¾ðÏ.u]w]7Ò\x0018ch½r\x0008\x0001\x0003ª¥Ôt©QE\x0010CfE\x0002B\x0007òÎ³
b9KÊI$µÍÊ³|b\x001atìü_Ò}Ç!\x001dÑå¾g
¾Ìiû×A¡ÿ\x001c/Ô1±\x0002¤O·¼làPCrhy6\x0013éÜÙ1a2\x0019F\x00053»µ«Yöäx#$
\x0003@í¥_±1ö!ÑúIºP¯
h""*ZV\x0005\x0000ä¶s©ÈR6íC$&"ÚÕòq§¥²,]Í¶iz\x001dË²ôªÆ¥Gì2"i³Ø`.Üs³\x0005.<é\x0013
ëHry½Zß½s÷ôÙ³\x001füà½[·nUMSjÛ¶®×mÛzch\x0013\x0008"âùùù|>_¯×I`2)._\x0010	!¤rJGD¼\-Ë²,X×µä<\x001aÊ²d¢$i>KÎDÖ÷4wNJ5«·ØôR@¬=vaG·,å¶\x001aUW®\x001cM&33\x0003#W7],VÕ)HXö\x001d¢Áýe\x0018!,W«ÕrUN§~¦YÄIç\x0002\x0000Üå9éº®S×\x0018ªjD¹{×îÞjb a§Bà+W`¾û\x0019
°ß¡ô "½ÏËKÇ{ßÞ>\x001c.ÂËýsúÐ\x0004~ú¹ýom zº\x000b\x0003Æt\x0000Ê\x000c\x0017ç/ûO\x001cÊ\
\ø%j4D[¢\x000b\x0000Ðð\ùß`\x0008Q­P\x0001@zl\x0004C\x000eÈ\x001dd\x0015cÀ¢\x0008¹Ô¶H1å V\x0014!\x0019ÕPQ©6÷MÚºkÛäc\x0008¶XA¸\x0017«\x0000
8÷Ç\x000eÏJûÿTÑ5T<Jê×\x000eCêuÍ¹?\x0017\x0004Ð\x0000¬u@\x001eÐB\x0008\x0000FÀh\x0008³ÙôüüüÕÉãÇc\x0015ÿîßÿû¯¿þÆ\x001f}CËñ¹[\x00189Ü¸z¼^5ÏNW³qqrrñÊÍ+©i;Ó²¸\x0005\x001aRae\x0007$¤Op§rÿ\x001dU\x0005sÛ¬MÃ¡§,yûÐËf[JÈ¦½Õp¯ê5 \x0008
úË\x0008}$ÉÖsg¶4WØÜ¨¾+&Y\x00030²wCT²¸/úºmº.O÷öÆãQÝu«¦\x0006Éxr|xxúôé;ï¼sûöí?ÿ?;ÞÛ?_Ì%ë\x001bo¼\x0011cN¦úìô|ÿ`RGE\x0011»®¡#\x001bÎHÍH\x000c@\x0001Ð\x0018@BBÓº»yëÆµ+Ç¯¿ñÆùùy×5M³îRL\ÄÉlzp8´8wØ¤:\x001aWW\x000f\x000eÎN~|ÿ\x0011\x0010ÜzízílQw\x0010j$J!<{v:ÏEºi®X Ã\x0005ªª\x0002
Y¤m[n[e\x0004\x0002dr\x0015\x000f(y+¡Ë®¦î:ëMÓ¤.
§§w}rÈ{Ü\x0019\x0003\x0011rH^.÷ëÁ´a&«Ù6Hß©Úöõ×!Ãcæ\x0010\x0019³R ^ÒíÓ,/F\x0004ÛæÕhåSÊ]Î8ÄÈãñøàpo2Æ	P¡ßË{×°]£6IÝ¦DO\x0010Ó\x001dØ§î/íV¾%÷<\x0006$3P@=8Ü«×õùÙÊQ@¨"ëõºI2~OG£G3}|ÀD9\x0006±[69·\x001cp<¢`¦MÎS~ÓmÞ"°Eº\ªn±8Tm×á
ÆÑ©4®UT\x00141K~vúl>^ÀU5Z®ÆUUå¦ñ~\x0010m\x0010ñDÉ8Æ8\x001a®_=ÒËBD(«kÛ\x001f}ðÁ\x001fÿñ\x001f_\\'Éx²Z.ioo:\x001aD¤ONNºÔ N».m¥áQqÞÐG¥jÀð|\x0011 öÿõÜx9;?}ððôøh¶yÍl:Sµ¬ÚuÝ¦ÀÄ¦ êb\x000bTºsu1\x0010±\x0017­_ÜA]\x0011\x0019ÈÈ%(_nánî\x000cß+ÝEfÎ9/«ÒsoÙ6¥
\x001dÛv^§\x0000\x000cjd@¦dDÀÄL4°=w?'S¤ÍpÓßÍQ\x0012"
zQ\x001byßÍ$ùIÇNïµ¿æÒÓÖÂ,|(³Ùþÿm\x000c7Áa*ÐµÌ\x0018b\x0008Bä$\x0004+\x0004¤dó+ ¨Í¨À'tBû±[-ø¤a?îe\x000c8P/ñ1ÌLvÑ9\x0007¼óvK8©FOÏN_}ýö_¼÷á?ü¿ýË¿üÕ\x000f?ú (®Îe\x000eå|uþèá£ÅbqõêU=³ï3bYâj¹,Bìý·<\x0015\x0014"\x0002\x0017´GÐ²äºL)çàà4æ~ÅÁ>\x0016ÉmÓ¦ÛÔ\x001a)0	axA(äòuÛùû\x0019¶tõEÊ\x0015Ü4\x0011.Í
P%g ÊD\x0014¸ 2%Ëªµ\x001a\x000e\x000eöë¶=}vÖ¶íx<Ýîi²½ýëW¯9vaº¿w¸·_×ë{\x001eOÞûáµkWNÏ}ÿûßþÝ¿÷\x001f¾ñæk\x001cÂýï¾úÊmÇï®YÞtRM¤`ÂÌL\x000c!°)­s7.+
d8ØÞhzãÚQ4;8 ÈJÜ

¨CX\x0000t½^N'ñx²^/CÀ/ýâ\x0017ô÷|¸XÃº}üx	erWË.A¼\,Ö«U%s`Dc\x000e\x001c8 @¦RN]'L@Ö2¾W\x0019ä¡\x0008A\x0006"àh_I­\x000bvyÒu+\x0011æÓE?EÆ3Ü\x0017z±63ÌÒþ÷ªJ½Ê"\x00103¤]r\x0007ÆÑsuò\x0017sP«\x0019\x0014­\x0007+XJÉ+IsÊj\x0001\x0002óx<>ÜMªq\x0008\x0006b9ðsÏîK\x0005°~²Ñë=x\x0013s(h\x000f(MD£^öP\x0001ÉùéÓ§ëÕªªB5fÎ"ëõzY¯=("çìÈÖ-\x0012yù1\x0010 %hê¦iê¢Ì%3ù\x0017nJ#Î©öl\x001e\x0000º.u]ç%\x0001oÖÅ\x0010FãqY\x000e×ñÔ_\x001aÂ¾Í!2*&1Ä,¹ªªk×ÎÎÏ«ªéº®ª*bêºÎ\x0006£Ä\x001eÊJ¸X,çóùb±ðÈ\x0015.ázÐdNéýÞ?ûoÿÛÿ\x0019¦©·~¯\)ËX\x0014h6³3¯[äF..c±Y^7úswÌ\x0004ÑDS×5£Qy||T×õjµ\x0000#C\x0012\x0001\x000f4X$c(¢z©{»[0\x0011\x0018\x0002áb±(Æj¶DÈz ªõ\x0000 b¾\x0016\x0012Óh4ö¯*\x0018B`ffnÛ¶ë:¿,MS»®Ýh4\x0012ÉYÄcA\x000e¬\x0006ªÛB\x000b"Ò <xé005%¿
ýV2dãºm\x0000¸ËpÿóÏmlíçøÏÅ%\ùÙ¨O¬Î\x000bc»\x0006ØÅÛ\x000fµí/\x0008\x0001w/ËÎé¼\x0012Ü¿oøYv´O^\x001cØ'éý_\x0015½\x00086 ³\x0011\x0011)F.ÊP¤Ü&(\x0004EÑ\x0000@4*4©­Ú #<@I{c\x0006÷aCÄ\x0006yiþÒ\x001bÓ{Rª¹\x0001}\x000fb\x0007\x0000ß7\x0007\x000c@½dK+lÜ]Ì\x0000Y\x001cº½¸ø\x0000u±Þ^hÒL~øÃ\x000fÿ7_ÿÊïþí¿³^.S×\x001fîÍ¨wàè[Å]×<|ô ·ùêñ\x000f>ø FPM£Q9?k®\x001cE\x0000Eu©Q\x0013\x0004\x0015U0Ee\x0000bnÁ\x0017\x0006lèæ[t\x0010\x0000@²ZQ\x0014eYNa¢H«º].\x0016u½\x001eO§ÄD}VæÀ£d±¾Ôôtó\x001c¡W¢Þj\x001c
¬Oñ\x001d\x0017ì:ª\x001b\x0004Ë{%mÔr{Áø®Ë¢Z\x0012/.\x0016u]s,Æ£)Sl×ë/¼óåýñôþã"9w9ÍëÕÝ\x0007\x000fÌ\x001f?>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article6.31bf15e8.png](https://www.dossierfacile.fr/img/blog-article6.31bf15e8.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=>^\\\\\Üºsû«_û\x001fø/~ðÝïªêí·êP\x0007\x0017`¹\\x001cÍÎ.üÝ×?óñÇï\x001fÜ\x0018ÏFõ£ï>~o¹\þÿä?ù\x0017~ñÏÞ¹urv	«å
?û7>û·>;«ªÑg>sw4¦YµZÂ0D­\x001e¶ºªÆOÏ5!O\x001d1ªzÔt\x0008\x0000Õìn\x0005\x0004OÎÐ\x0007iD\x001eTÁ\x0006q^\x000b\x0010A\x0011Í\x0008QNf\x001cÛØ®c>Á*p
Î\x000bB»ä\x0003\x00140\x0010&Èj
\x0000&Ê
\x0000\x0002L `íàüüôàà@DÈ£¨\x0000a\x001bßø­ßüÑ\x001fÿ1çÝç?ÿù×_ýwë·ïÜ¼EuÝ®W7nÜ^®×ßzï;o}æÑ\x001f]0 \x0011\x001cß¸ùµßûú­['Îûû<8¹qüèÑ£\x001b'g§\x0017''7\x0017å³§çóåb¹tD§Ïë\x0011ij\x001fR\x0012SYxÞÖ\x0018D\x0000È`»Õbï|û×ËÕ\x000fÿÈÔÕø­Ï¼õôéÓÙìðüââééw\x001e?~ÜÅ¼yY­×Á9kÂ0OtD\x0004Q¼µÜÔªí¼ó¨

â=+'\x0004Nê×nM\x000f\x000eÃÃÉ½;·È\x000b@\x0002\x0014R]Lj<íÅÍ;oºÈû¦i§]\x0017O×M3©ÂñáQÛFï¼wNEARåpÑÄõzµXÎç
Lo¼\x0015ÂElå`v¸Ì°\x0000öµ5{×òüP\x0006Ed4\x001e\x001f\x001d\x001dÝ»w»HÎ;ïj\x0011ÎÎÎ«Ñ|1?v^Ua2\x0002À'O\x001e?;=»O\x000fëv±jTd4\x001e/×í|¹&ïLc>_<~úäãû\x001f'N)ÆÄ\Ôü\x0011\x0012\x0011F\x0005ï	\x001e
^ÔXV½2\x0002
æísN\x0001\\x0015f\x0013´íÚ=E@èf£f}^{t0ÒÑttr0:z\x0007+'\x000b\x00078>\x000ejàØu]ð2ªÝãY\x0017»º"É\x0007\x0003¢9ÙÄ®]1ÙúÞ®ÓñÁá¢I\x001f<tè\x0018\x001c¹\x0010B#ór¹Í\x000e	@I)ÔSP2AS@$pÖ=ªF¤D$W¿e_¢È\x0014I\x0004\x0004E%`\x0011\x0017\x0000ÀÂE·\x001e×\x00159Ûï\x0010
4Ñ¸v<\x0000,Víh2]6íºQ²"h\x0005¤^\x0001zEb\x0002@P]R¬ç\x0008\x0000¨\x0004\x0000Â`¦ZèÈKî¥øûí\x0015lÃ\®ôoÏ!ÖA)B³ÉQ.hJ²
Ñ\x001ej\x0015±ßÞ"\x0005¼÷Hd$ª'gê0vÚÙíÐaûáw%ßrºÀnÉ¹-¦=T!\x0013î\x0011\x0002¡áNö*\x000fu éÕË67¼½ÃÅÃzû Ñ\x0012\x0005Î9ghNè+ÌbÜ\x0006µ¨§Âï\x0002 DYØÈwT±m[##\x0016³ÍöÜæÝA³÷>²&¦ÜOãYo2·7Ä¶%0E4\x001b­ê\x0014y¹"\x0002\x0016\x001cBæõK_PVUpNy\x0013loÌÕ\x0011@!q"-oæL\x001aâÀ\x0006UY:Ìø©fù\x0010§´-,\x0004à|Þ;ìt_?xöï¯Ko&aÈ4â­ZÂvJ:§L9;qà°¡¶üûkeC+a\x0000\x0008> aJ¬º\x0012$"í-dw|nJVÚ\x0018\x000cLbä|];"í]-­=\x0015UàjâËRm	\x0000l\x0008õ\x0019íMæ6ß6I¡\x0013]Ès%»IUÓváváG¸A\x0000g#«\x001f\x0013ñPQß9UÃÝö\x001bØAÒ[\x0014Aµ÷üÛJ5Ë ­ÄfUD\x0013Iîßb\x0002\x0012U5n½l\x0017\x000b-È!DrÞnòå\x0006Ç°þôÃR÷ÅptçÝqÞ[é¥¤edÀWù^\x000eÛBfRø`?»ê,7©}RÒzÜ"¡ç§lom-\x0008T\x0011bÌóR°ôN9aîÁ.ÛÔ8\x0006f8|;`ûý*£àe\x001fy_lø¤%?¦ª)±ÅÒÛ\x0018
÷ûpe\x001b6ÔÆ<ÎÚL8ó8M¤ÐÄ\x0006c9\x0011åóx\x001eHßY-Æå¥
\x0011ô \x001bì]\x0011\x0011Ñe7Ë\x0010Ý¢ª\x00130pÊð/\x0011\x0001"N,Â¦ô\x0006}E9s·dßl0XePÝ(£qø«AÎ\x000b²o^×%ýkÎj>\x0004\x0004J½\x0002¿CP60·i\x0013rðAUS_H\x001eÔ\x000b6NÀÃÛ¾êk;¼ÏÍÿs+\x0007²;ê\x0006Ãm5Ùyêë­U\x0007³PÏ´A\x0015/µS¥ý¼sÚbÜJÎ47\x0003ÒÐtÃ8JÀæL±	nØaÎgX Ù	À\x0006c{K½Z:Ì\x0017mNØ'¬\x0010QÝnírç$Ö\x0008f\x0007}Y
ÄÒqXtXß)cÒt G²bªôY£ü+OÎ\x0015ÉO«cC®Ê:æc×1Ëxâ½sÆã¤Ì\x0005qFJ)"
¹
	Í\x0014ðêt`³¹ùfm®ÁÉ÷jÓp,=rL¿4\x001a^\x0006¶'ÁÞèªª²7äòV÷!5ô]U)I¯o?LÌ¾\x0019^UÞO	\x0013w±3ZX¹Uï½9	\x0019¨9]!§#^ë\x0007óBxuÉrZí\x0019{pq"saÛ¸Ns\x001dhÈI5±2¡eT}°ê8\x0017¡óçÜsÔ¶mÑg7ßïÄ\x001cyôf	¾^¯±\x0007D)\x0019÷¡ÿîøÞÎ®jÏO\x0005Ûf \x000eädEXÍ\x000e\x0007\x0000lçY|Îwúea],½Á\x0006ö>ÌF\x0001\x0004\x0000³ÝzmÁ5é¡éñÆ[Ô^ï¾õ¬\x0000`X¤á³ïè{\w\x0014cÂîGLD>x\x0015M1u]\x000c¼óäÈ66¹L¢Ð÷é ©­Ú\kè«¬
J\x001bÞRFÜL|Î¡¦\x0014Í È9ò>8GVÇ\x0005^cÝÚùû&\x0014ù)½\x0011§}Ø;wfµ\x001c\x0011q£¸B\x0002ÔÇÓ¶÷ØÂìCð\x001c0¯Ök\x0014L'Þy
*J\x000bÍ{j;/t\x0019\x0002)IösãðEèfó0\x0003£¯õ\x0010\x001e$ôÞyt,blÛÖ\x00119ïB\x0008^²C\x0015\\x001d\x0003åX­¦Æê\x001cM&ãýVä4\x0018£\x0014éyÂÅbáz\x0013­º®½÷£Ñ¸ªÂÛûÂáááh<1Þ¸y\x0003\x0000lè"¢59ñh4j¦¥Ö\x0007¢\x0018LòèèèôÙ³ù|Þuð\x000bÆ½æ1Æ\x0010\x00029\x001a0´±kBnUOD\x0005ÕÙV$£P=:\x001f¼Ûª\x0016\x0001É¡§ódð ¯êÊ\x0007øoÛ¶]7mÛ®ÚSÄªÚ(3b×uãñ¸i¦iRíºÏ\x0017)ÆPUgg)F+«HJe6FºØáz5LY¤]­´­÷îÎ;AåìÔ»¸8_5
\x0000ÌçËÕjÕtírµ\­W±ËÆ\x0003lRU¢-(+õHðQ]B=\x0013â³v1ÚÏwæÛáâeõx+¬\x001a@{ï\x0019Dôù\x0008QÒó±;ÃK$fß³óV»íGe\x0013ÚÌ÷sÂ |¤\x0001¯\x0002®\x001f\x0006ÿÚëmoÉ(eQAU5/Òá;ËlV\x0014Q+»ÆS³Ëã«bG¸3GZ+å|hV\x0007"t0ÝÉ&«Ò¤EÄÛÖ\x001fGÎ63åÙ\x000bÆ
i\x000bx:\x001f|F\ÑV#ì\x001cåþcLÒ{là)\x001fÀÖng\x0007Û(VëuÎYÌRbfM©lð/×Î\x0006ÕÈÜ"\x001ccj\x0014ó®ò¡öÂÌ\x001c\x0013³\x0000\x001bÁ\(B\x0011îÁ¶ú«\x0000}Êo_\x0017\x0001åb>÷³I¨ÝÁÁô§¾ò§O>Z,\x0010ùøøöéé²M÷§£ããlúuv~69l¬à½C\x0002åj¹X.J\x0017T¡
!ªb\x0011ít½^÷¹f­ªÊ\x0004Î{` íb*µçH"ë®-W«&hw8©ßÿàá?üÕúÁÇ\x001fñìèö]\x000cã[o¼ÉHQõ?ý{÷/ýåõwï÷ÿ¯ç\x001füö?ûËÕªIwî¾\x0011Fúío¿wó\x000es\x0004\x0006WÞ\x0000\x0008Ô«B¿\x0010Ü§[\x0008°©¤\x0002Àx4\x001aOê®ëÎÏÏË¾z8i\x0010át:eb×t\x0008\x001dbçÍÆ'7Çµ\x001bMÆUå¹[@Z\x000b¡Jä|Û^ÔcMÝëw_?=¿¼¼äz4;;}(ªãqýæ[GwïÏüó?÷\x000b¿ðg\x001cê¿üåOî$Ú´Ý|\x0014ªªÆñxtzöä;ßyw>¿øõ_ÿõÇ¾ùæÖÓñññrµJgg¬9O
¤P°\¯n°^,O\x000e\x000fÞ¸÷ÆïüæïÌ\x0017é¸\x001eMÆüî·oß9:<¬WçH<\x001e§SN°lÚÇgÏ\x0004¸\x001aÍÄùV>üäÑ\x001f¼÷Ñû\x000f®\x001a\x0001AD:A×»]z\x0000PÀ>Û,e-Ûz³&\x0001mm \x000euµ<GÈÑ";%EE\x0001
\x000eX"8Ùhàªâ\x0013"\x0000\x0004\x001fTe(]¦za\x0001 B1EÓÉh¤ª±\x001f|ðá½;¯\x0019\x001fp<5I\x0014Ä×¯ªDÔ!\x0002*Í/çÕª\x0000ÈçßþüzÕ,\x0016ËÄ©mbU×trã¤ëRÝ\x001fÃMõ§ã¤Úa\x001c¸\x0014ã£cÙl6Íêºzÿý÷W«Õår±#ò¡¢0\x0000	e&¡Q\x0000	A¼*\x0001"(©±\x0005\x0018\x0010\x0001\x0012y\x0015I"·\x0011Ù\x001fÔõë·n\x001dM\PÀdåÀ¶mÇÝ
o\x001eÏ8®'G'Ç'£
UAíM'QM)¦TÕ\x0007Ï-;ßu)Æ\x0014#w	º&Ù÷u·^µ"/ ïô¹*%f½VÕñxì'3«\x0008rÞ;4\x0005Rï÷ND8¥Ó³Ó§ÏrâÉx¼^¯2õd±Z"b\x0008Áû...>»¼¼\,\x0017æñ6\x001aY·>,\x0011\x0007{ÈC¦zaçt\x0000ÔÔ\81`.s&MÜ¦ØvëÉtT!\x0002\x0008 V\x000e¤/T9£J¦#<>\x0008uH£¦!UÀG³\x0010'ó}O)F\x0015EA H\x0008*æ»ÌJ\x000c
ÂS\x0017cÎem\x001eãÜ\x0013È¨ª\x0013`jÄ!Öu=9\x0018//V\x0002È%è\x0000 ±Y\x0014­$L¤{qâ¤qà
\âö>§£\x0000
êìmG¤N\x0012\x0012\x0011:\x0000qy´"\x0000øÊûj"\x0008.J´m9±
SRVA\x0006\x0000uý
ç\x0000JéËf»2TU\x000fë{ûÆ»\x0012Q\x0008ÁÈ£Æ
µ<ÿe´2`©Â6]µ(â:Äà}L©Q©\x0010Húk
\x0017keÞ¸\x0003Z\x0008±]I\x001d\x001eÏýö~?ß¶n2\x00128àSÚ\x0013áv²ïÖ{j"´*¤i½Úü`Ñþ0l¶#ÆdàT"´\x001aù8çB¨Bð{½`«DZ
\x0018QXKij§\x0015JÏÂNÐO5È\x0017VëvdN"©4i\x0019-èï÷\x0017\x0011\x0011Í]x\x0000ßÛÃO÷ ¤ª±ëlÂ±<F\x0015ª\x0001¤~ÃÈ±Ed«:ØÌ¨¨bV;+Z/Û½f\x0004ZÓÓ\x001d:W¾%¢bÏæ
½U´Û®\x001e¶r
´U®=d_LÞã\x001e©\x0014Î\x00117ùÝºõ=V¦#êKqÆÚ\x0004ªª(s|\x0013÷4hºâ¼Ó§{W.¢Ì¬J1\x0002ðÞóÈv\x0012\x000f®K\x0007ß/lq¯Âbl\x0011Ñ;\x0017Bp> RqÝ4ª\x001a¼\x000f!\x0018Ïê%eº\x0011OÚÍÄ ï}Mz«\x001cXÞ´3w<\x0017}?\x001a\x0011	_ <±ùyQMÛ·\x0007/ °04àC\x0005Y>-31ö^åe´Óæ\x000bÛ[f\x0019ü]þúbsñâ½®¿`kÆÞÓ¹Â}9§äj\x0006^¥=î_­ÁË¦þû¬»³Û\x0005³%åñÞUUPUN\x001cSÌïEVÿ\x001a\x0012_ô\x0016÷\x0019þ\x000c}7òwg;ñ\x0001«Õ{GDm+¸ÕÖºµ\x0014Õy\x0018c5°Hp®ª*ï\x001czo\x0013
Ñ¢ë¹pyÓùÁE\x0005d\x0008Öë\x0017bØ.\x0012týËçÏ\x0015èÒ¡§^ª8ðx\x0001ÿÍ%\x0008æ¼GÀÄÉ\x0008|Ã>Ý\ú«\x0014ÎÕð^c ¼JÎûÚ9¡\x0018Ç×ø/3¢

t÷Q!{ÊÊ\x0017áRN\x0008ÑPUã2\x0014xwäLÙ81Çd.¿è¼Ë\x0000R¼,¤»ØñXÍp)MUÅTD÷x¾÷\x0014Ð\x001a|øtÆíL½ðL16N\x0000àwÞëß\x0011î\x000b\x001c*ÂWéã{]W×¾¾Å\x0004!£
v"-X\x0019|Ú(ð%ÇD&I\x0010a¡&DÎS__~x9ês©ðÛDù}¯Õè¶ü©Ý¡URSHÕ°j\x0015B±\x000fL6Ò£HèX\x0000ñ\x0005n²/¼$n(óßáûÐ¡6ÑxÝ¤STSRPU·7@äzÅ-VÊÞ\x0016Ö®\x0004=Z\x0013ò|ê6	YÝT=e{ÿ³ó*´ïáµ\x0008¼SÕÔuªJaÏzl{+;"«\x000e÷ñey\x00192M³ºúáÎ'Å<oØ2%fµ}´÷ÞA&¸(A*¨´^îADõ\x001azÊ"}õ}\x0007\x0005é«½`ZY[é{ö\x000f(·DÛ\x0014óá¿î<ï\x000b+"/<rK\x0012
Q6øÝ÷o§Í
¡é\x0015&û9\x001dÅ\x0000\x0012CL\x0006&¨\x001b"õók¶HÖ£\x0016\x00000ÈdLÑ"
Þ²É!0l\x0004C®?RbÛû¡wzý\x0006ò%Zm\x0018[K¨h4ªªªM'/mÔibL\x001d* \x0000¸È[X\x001eÓö¬ªª®ëñx|pp0\x001eOÆñx2\x001eFfE`ú\x000c4\x001e\x0012'ç2sÎyg%ÕÎ¥PUÉä9\x0004
Á)0ÌÅªSå¦KsAÅ"¶wä\x001c\x0011°4M3_.§b$\x00155\x0019\x0004 5ÓuoæË¶\x001b\x000c>øª²y\x0012Íû®%¦]â\x0014G¤ÅrÞ¬v½fæfPLmgÅÔØu1µç\x0014c×Åùr\x0011S¬bu¹\x000bçm\x00183kb\x001bÉ5`ÓÆÈ\x0004êñ\x0004 ²wnÕ4Óé¤Y7õÊz$Åxv~b\wíb±X.ªjÛ\x0006\x0013í]+¦¾_·
K>ÅgÝ\x0001"þeÇÝ¾\x000cBU
½þh¦î-^\x0015Ù;\x000c=bwX\x0008åïáÖûBm\ZËZV\x0010E"ì}Yz\x001c\x0011\x0016ï\x0013Ëòå\x0014®ÉOíÜ³fÐÏ+lí\x0010Ñ\x001d²ç·p!Ü\x000b-U°Áèd'\x0012\x0016©[\x0000°¿\x000b£ôÿGÎû"¦e\x0011/Ëë5\x000b8r\x001c#g\x000bêÄ¿S\x0014%\x0004\x0005"\x0014VEðÁ|YÒÖÙ0ïÃEÙ»Pzd÷2hÿ'o~î­\x0007\x001f|üÁç¾ð¹zrc¹^=¹ø\x0015\x000b«¶«Æ£Å²ÉûÀmxãÎ¨sÎùà½óÌÂÖ\x00171EGX×µ±TG;;wU\x0018J%\x0011÷5âº\x0011\x0000ÚØµ±Ó|c$\x0008G'³ã\x0013\x0000q~÷üìá¿ùÛ\x0013?¢ËUéñ\x000f|ðÉáÉñôùO#V?ý3âÖÍ£ñøàøèî\x001f}ó;\x000fïÖã\x001fþÁ\x001f\x000c¬®ªª$gN%\x0000P ì§	\x0001p[\x0008òÜåÏ\x0014ÛÊ;\x0002º&Ë2M±\x0012¶LºMº¶\x001eO\x001cJ´j¶mj\x001b\x001fÌN\x001e|òÝ/ÿè\x0017ÿì/ü9 ÑoÿÖ?{òøc\x001bØ7nß|íµ×þÂ_øs·nOÞþÂgßþÜ\x001bï¼óÎÇ÷×ËËñht4¶mûôéårñ\x0007ðµoþá×¿üå/ôá'ï¾ûîk¯ÝkÛ6vÝp¡QeR±*% '£Ëù9: ï`¹noÝ~ír±L¬ÏÎ.\x001e?;gáóË§o~öÞü²IÐ¹JTH"«&ÓÉ|ýôGïøá·þèßûú7ßûÎ'u¸éh
\x0000mLB_û\x0007è×9TÚTO1\x000fÅAc\x0011R\x0001MDÉ;\x000e:r,\x001aYÅ\x0011
RL­\x00009
 Xøý$UA\x0002Óú½²o\x0018Æ9°§Í²YÔu}ÿÑ'ëæËéÈà\x0012äÈ!zç\x0006»K\x0002UNÜ¬;\x0018Óû\x000fOnt]ë\x001cÅ\x0018>y\x0002\x00001rÓ¬f¹nVëfu8þÔT\x0000p¡¶?ºîßTU§!£££û\x000f\x001fªª­þ\x000cËö<C¨\x00057Q\x0017=Ú\x0011\x0004H³[\x0004g¨àÆÑÑÝÛÓ/¼uëÖÍék7\x000fGc\x0017*Ü\x0008³+Oêº
Ä\x0017Í|ä\x0015¡K]\x0002?&õ(ÄÇ.u-w]çÄÇR)%n;i:h[j:ÐU\x0007àAýzÝ¦$\x0008"ÒuûèM6S,\x001a\x000fÁ¹.vÜv,\x0000` ¦m\x0017«U×uçª\x0008óå"TÕx4
¡j\x0016s\x0017 °êòbùäÉåb\x0019SÔb jR_\a\x0006é=5\x0014ñ`\x0011±(èv°Ê\x000eT	´èN÷/\x0012¨ªÍ­BF±\x0010Jð\x001c;>\x001aÝº9«	&5GèÈünÄÒò	æ>Fóý%\x0010\x0007¨Ìê½°(bTæ.%\x0016ïCjÛ\x0008 UU9TERðuµN«V1Ôxx0¾\7]\x0007Ô\x0013ZÔ«&o¢Íí¹b}{¿pá\x001fÐ%E\x0014\x0014IT¤HâÈÂ!Åì*1I¬\x00081BäX@JlI«ì(<hì®®xQí>\x0005\x0000\x0001H®,Â¶\x0015\x0018â\x000b#JU~	&çt\x001b\x000bþòÛÀâÙ\x0004\x0000=ÊOüðr­ú/\x0004ü°\x0012sõËîÊÃÙàd""lEÎ;BeÈXZÎæT\x0000`Ærï\x0017Å\x0014;aQ\x0001®ëbìDâ;ª+\x0000\x0000\x0000IDATØ\x0019ÂÎ{\x0011I-W\x0010cÇóÎ\x0015\x0015\x0019-ÙOæ$"ÅÕo¸U}^%[j$Gx}}mÛx÷¼üoË!½
Ú¦å¯\x0019WfwmÓ2½cýþ3ëï¯\x001b\x000e¢#À¢ ©ÁAì\x001dLaH\&Ï"å ^.¾§U·\x0005·\x0010v{A³ôT|D.+\x0012«\x000eøë\x0016Ù²|`¿GãÞñ1q²¥ÿ%È¨%vuSö2
RZ¸<Jf·Û*sµøú}9v¸{"Ø> «eBÈNgå²"¢\x0000\x0014éÚr\x0006\x0018pÄ_\x0008µ·¯\x0001É\x0018ÞUj¯\x0002¿üdûâ+nsñ{éY}N·ZÞ£·Òs®§¼ð\x0019KTlìõÎÍ\x001eú1p\x001dùêmÃ«,:ÿ\x001d%¹±\x0019\x001bWZf(9\x0008_É}R\x0015N0Ãs¥Hg¿¤\x0018Ìð¢ÏÉ±\Ua½îVw/'öÝ@%Ê~Ò²ñVêç®Í:Þ\x0017Ër\x0003âsu5\x0010Ý\x000e ûÿ\x0017Q±¯|¨¬ùÜÂ¶fÂd.j\x0016\x0002À5·±É½{ÂìE(ä\x0008	½iï\x0011ËT\x0016Ù\x0008\x0013^%¶\x001aXÇ\x000cBOB{ÉÃRCíÛ¼Öd@a^_|1L\x001d"G\x00123ôzJn42S\x0004«\x000fcvá^x]\x0000 í³\x000b.½å\x001c\x0001xk\x0011È¦k"\x0004H(YcÃû±Â¸\x0003g%Lû¤®ëÒúY­{\x0012QT+iazLIU½÷¢jJÐ¦Â\×5"rJ¦\x0012°³¶|º\x0014­	\x0000\x0011f\x0001f1×Ò¬!¥D\x0011\x0014B\x0008Â\x000c/!û½\x001c\x0005¬¡ª»i\x001b¢·\x0014
¦GØRÃè{gÍ¢óÙ5\x0010tÿ\x000b\x0012Ç\x0013\x0000hÛÖ\x001b1¨ë"
\x0010ó(lcEÉ2@;oËÕ\x0010$_.óí·
\x001f\x000c<S_¾`ãWè2\x0019ÈÄ\x00048{wgÅÂ­IÌáÒä3-X\x0015	ºm\x0004M\x000f?\x0019d±¯\x001eÖªô¢Tõ¦Ø9`A#Æ!Ê`"@N\j±v?c­rÎÂ:u#
\x0003ØAF7\x0015ë\x0011æ?gRÛ×ÝdîDI)en÷¡W®¼­Ù¥Ùÿõy\x0007çIÃ1ñp}C
ÿ¨ln^5nPèß\x0002ÑLÂ3WâµÉ\ð<\x001aû
L\x0011s\x0016éº\x000e\x0011G£Ñ÷ÊLH]×µmK\x001c\x0019w\x001fx@¡\x0016f\x0016\x0010K'\x0015%Õá
aâçÏ1Ü\x001eÀ9óÔ­¢Fo»\x0016\x0011}\x00085\x0019\x0000\x001bÅ0ZE_°ï­JH¡\x001a×£Ñx6Ç­%p^a^X¹\x0008\x0000º´É;F£Éd2NG£qJq4\x001a\x001f\x001c\x001c\x001c\x001c\x001cxçgÓÙÉ\x0013Gn:\x0016#
3f1\x001a\x0016ÒªªäÈ{\x00031d\x000e"\x0017ªª®êOîò2ãAD\x0012$TOÁ³Æ.v«õêàdºw}Â\x0000KÆXwNU\x000cÕLåmÀ\x000cØ¼\x0002sApÎûåb\x0012ÀÄd®DjtÕ¶µ\x001cý'÷?Z.WÝº#¢®ëº®K)*Àªé4ÏC¢3>Q\x000b"òÞ/×«UÛÌ¦ÓÃÃCtáòrèÖë×m3Í\x0000¨mãÅù])¦Ø4
"ßÀPÃ-ÏiÆòoÎqÏÎ¬>\x0004Á\x0018@o\x000b\x0010_«>
\x000f!8ç0¥d\x0004Dt98¶ÅKUu\x0003O¡Þ3Ãå
\x0012i¾´±4vÆIB
`¦ºU|\x0015Q\x0011¶¤R\x0011{9¸f¶±z¿E\x0014Y>¨7.26ª=¥BðÞ{\x0011Mi\x0005½\x000cZVK12D]×ª\x0019*höÀu
ºWÒäedH@8í\x0019Þ¼%p´k
'dÑTÃ
\x0000Ç\x0013÷RL¶YÙõ:ø\x000b'¶¯àê\x000ccáÄÅ®qøÛRÀ¶©)Ø4ÈÜ¶­ILÅl½]úîóæ6'òÞM&cùMR×ÓÊûº"I²Z5Y±\x0008=¨#\x001bÏmJ\x0015U\x0000ÐI\x000cÞëKÄ\x0015%*\x001d\x001dãvÞ^Ì\x0018³>mìÈwTùÙYðrµ\x001eÑh2;\x0011r[\x0015/[;¹\x001bÖwÞ­sôe8å*T9<\x0011\x0018ãh4µµµ®ëu\x0013Ëí\x0015 \x0006\x001e\x0008\x0002t¹n&ëf±êHº×ï¼AÎùQ\x00077.×p9OÿÓÿùÿ¶\x001e×ý¿ù×ª×?ûÕ:	T\x0017çËÉ´^5éÖíÛÞ]§\x0007U5bÕ¶í\x0006¼+yö\R½nç)çç\x0017u]F£\åß~ÏÌkc½Z9ïC\x0008I\x001d¼ÌçmJºX¬Û&vØ¥\x0014ÏÏÏnÜ\x0008ÎnÜýå¿üÛvý'î'ï¾qïâ¬m×\x0017\x000f\x001f¼wzqöã_þÒç?ÿù/|á\x000bÿÖßüï¾÷o\x001e\x001eM§¯Ý½	>óæëï¼ó-æã?üµòO\x000ef3$øÖ·¾}çÎkËÕr>_Ä\x0018Ù)çççªjê\x0008\x001f¬\x0000\x0005\x0004¥\x001a»õú\x0012It2>9?P©\x000fÊ:_é·ÞùîáÑ¨Y®Nº	ÆÓÉ¢]>ûzt÷õ7OÏÏæÝû\x001f|÷\x000f¿õî\x001fýá\x001fðáýgO/\x000e\x000fnÅÖ\x001c\x000fµb¾Ê\x000c Ö¦$èI\x0005!yè¦#ª\x0003j\x0017\x0011VMÛ6\x001cY¼\x000fmÛ²ºÉál¹î\x0006sÏ\x000e¹¤o\x001c9\x000b¤÷¾/çççÅr:Å.Öu\x001d\x0000Wóõåü\x001c¼ÏZ%B$%\x0001TM£º¶]ßÿàÄ<êºþü\x0017¾°\,\x0016eJQ_»Sâñh´^\x001a: 7¢»®\x001d\x0004<¼\x0006ÏÔKJ*\x0011-Ë¶uDØ4MLÑ^¨\x0008Qä\x001a\x0017mÌq¶Iö)"# b\x0012P0<\x0018\x001fNS\x0017×\x0007Ó×_¿ý_¸÷Ög¦³L'a<öä\x0013*\x0001
(¥5Öu=ªÃÿ¹?k¶%ÉÎ\x0003±µ»GÄ=áÎysª¬¬\x0001\x0005\x0005\x0000
\x0004(\x000e ÖÝ$¥V\x00134R2ëÖd2ú´ô$½Ê4\x0018­MoµÔ26' »A\x000cU¨BÍCfVw¾gÚS\x000cî¾\x001eGìØ{sîÍDê\x0000¬ìä¹ûÄðqùúÖ÷}\x0000a´ õÅiåÛ×Þø<\x0008éò>èfÁ\x0008&\x0004\x001fCÃÑÇØ0¶Ñ6Ñy\x000faÍ \x000eÄÖU@t\x0000\x0016"c\x0004AF¸t£ßè¿\x001d\x001d\x001e£TU5)GÈè0(Z7#\x0018%\x0010\x0001PÝÖ*
\x0000y\x0013¡Í25²Æ¾÷Þ{óù\q<Ä\x0018¼÷uµã©LÃ
¢{°M¦h\x000f¤j*!é\x0004ù
ô\x0010FÑ{Vfäxd\x0008I\x000c&sÝ\x0018 É
[#\x0007ãìhZ9\x0016\x0016G,qô\x0007uñ ¢\x001c\x0019AqD7Mò£Mçl\x000e"ä##Ç \x0011\x0000°sNÚ\x0016@,A\x0001rGd\QgK_\x0011Å<wãQ¾^Ub	°°\x00184"\x0006\x0010B"M"DfJE ÌÆ ±¹2\x0018zÔJ+D­\x0007À $\x001c£\x0000\x0011
\x0003JrYEÿ¹åâBØ\x0008Âr¹²yÁ:n³:\x0016	\x0011Æ¸9ylx¥}<"¼±àå\x0010è0·Î¥YÌÒ'iö²»ªÆoÆìÂëØÌ½y¡!Ê\x0013k\x0015y\x0001áCï£\x0011WÛ¶BTX\x000b\x0000MÓ¨8JZ
\x0006OP\x000c©\x001e]\x0003\x0012¹îþú{ì´¡\x000b¡S\x0005¹÷Ìl~F\x0008M7è\x0007ê\;yçÁLéuwZR\x0007*\x0011Y\x000fÐPÖ A#={\x0007ZVýÑu\x001aëp\x0018D¢Þ7Ý­Ô\¹\x000f!U·ôO»õ?Æ¹êRIìØÛúÌ1Æ Ýdá¤Û7#ìEû1¤×Uvµ&Ê\x0014\x0011´´U¦ÙX½êpB2Æ K\x0013¢ ²\x001c\x0000B`ËÞ¡PO%W³fSE\x001a\x001a-ë\x0010b¬ùU¥\x0019u|ÐÝ\x0016Þ´cb\x000eáÕ§¼tÚòj½ú[uÞ×_2Hßi"7YhRÙ:c|ð±¬	dkU
rT\x0018"\x0016Éµ\x0000)\x0019v$¦Sª³óW-|1å5SG\x0003\x0000ýÞtºÙ¨¶l½5ÆXË16MSù\x0016:\x0005BÇ÷¾i\x001aD$Cz«¡¼¤éºCaÁiöã¨ÞR«×C6öF­\x0017\x0011¹×¾îñEFßqë/YR¦ÙÇ«þµW\x0000ÖéÏ"ÊÊEÄør+ù~Ûö<]\x0011ÑäÒø\x0006½ºoB
µMú\x000fìde@T6ª\x0016àê~Nß
¬éo\x001ez	zÚ"Èþû¹TJDBMÓ\x0008±ÆYGÃsýs\x0007y\x000c\x001bm§ÙS}YjÀô²
03³Ë2Í?\x0004\x001f4âuÎé#%¢±)ÕÃ\x0012ClÛV/ûÍHÓædÈXÃ	¸ê\x001dÐ<Þ¥Á³\x000cg8\x0011>ÕÕ\x001b6¿Ìßjn6\x0004\x000f0îêà\x0001 ×Y&\x001e:\x0016¯j^@×Wö\x0005ÇÎ)løRöçþ_\x0019k¸H\x0008ºØÄ¤tm~í_\x001dAÑ\x0018k»ØÛ¦-çÖsø\x0010 ldáúÌ?\x0000\x0004\x001f\x000f%qÖ\x0010ëºNþY*ßH\x001bæ°øÐ"uÖB[@Õ\x001d [Î`shÂTý"Õa¸ÁDõÚ#µÆ\x001a]UÒ¯aøi\x0018tnsz+\x0004îeH\x000eN×/Í-\x0000´ëG¥³bvv\x0017»\x0019:Ûjé2q×µµWVQIºþHÈ	ãáTÙÕKLi\x0003SI\x001eðÒº\x0019yØô´A¿6VÕ\x0001\x0011S \x00110'«ÉÊ`xÏ1Zc\x000cb\x001dB\x0004\x0006Q9\x000f#J\x0000Y|ðÆY0DÌ\x001eA\x0010È\x0019aìÃ\x0000\x0014°D"Ø\x0012\x0004fBda\x00121 J(#\x0001Ö{fÓ×\x0008ê©gWò÷²,Çêëë}ô´ECdN
*,=Y{'\x001bÛ×V\¨ÕÃ?F\x0015£Pá*0P'õ\x0019VëURLHV²Î2\x0008\x0000q\x0018\x00031ÖjU°U
\x0002\x0012\x0006ÙA\x0012ý`ëÞV\x0017åÍõ-\x0000\x0004ÂÝ Ë«\x0005S "¢Zª(¡ã³jyÎâXdcy\x0002ýj"û\x000c\x000f;×Ä\x0011ìfé\x0003¾~/Lf·ìK¶``MN]Ú¶|Ú´MhKË:½:â\x0000èg´ªTu\x001eU\x001e\x0000±Ã½È{\x001fÂÆn\x001aÀ5\x000c%\x000eT¨OÐaÙ\x000bÛî<!l3qûÿM\x0007îÁÙoç(²CQ4Û\x0000\x0011\x0008¯Ú5¿½z7eÓ\x001a$\x0004\x001c\x001eJ{x(	\x000cÂÐ®,#ªU&ø`³Gr\x0019ÛëÎ+ê¹¿Ý[c\x0004Ð\x0007ïO¨:Õ^rºë¦D\x0012Þ<<²l!\x0016\x0004\x001a£¡KBÛYÍ\x000e7ºÐÊÐìï\x0013ÕÞ^d#:½QÛHÿ\x001b\fÆåøè`:\x001aN×QwX\x0017?::\x0014¶mcdêT\x0010õ-:O\x001dwóæ
\x001f1v2fÅH\x0008}6Ë\x0004!rô1XkÈæÍ3\x0000hÆ{ß¶-Yçq>7uU\x0014£Ùl¶^¯\x000cÑÁáÁéÙÙz½2Æb]-»Ç\x000bVSE> °p
Dg\x0010\x0000rÔp0>\x0000\x0000°Z¯bDÒÍwµ\x000eÝ\x000c\x0010\x0012}ÒÂ£\x0000§%¢öÒË\x00169\x0004mÛV«µâ£z&\x0001\x0018òb×«Õ|>¯ªj½n´¨¿ª«¦iÚèëºnWËºm\x001e DÆeilê:Dh|\x0000Æåº¯ªét:\x001aNÏS³\x001bCgg\x000fÕÊ·¾ª+\x0005§Y)1*/\x000e¢ðû¸ÚÐ3ã²¨B\x0007\x000c³\x0000ÈNä!u¨1\x001bíßN@5aÌÊã!"TÙ\x000ffÙ®±5Ãû¸\x0007\x0012¶­\x001a¶÷:âmsq½[¿<\x000eñÝ\x0018Á9»»Ò\x000e]\x0016^"êu_c=/¬ÿ[Tû4Æ\x0010µ; /\x0000\x000e\x000c\x00185vP\x001c)½\x000c@G\x000fEÄ×OªîÊ\x000eµ¶óq;?ë¥Pk¿!Ùþ$6Çý²¹ÃÖÊÏJ½ßù¢a×ìx]ô~Ú Å\x001cÎõ\x0019UIÒ\x0008M¤_¬t)î¼¨i\x001a\x0014 D\x0014"kC»\x0014\x001b)#cî\x001eËNç\x0017 ôu\x0010kÕ\x0006Ìîxæî[xgÛ¤ä/Éh=?;::Z^<L§_ùÊW=ýhv÷\x00164ös_xûýGÅXlcò¬(G\x001f=~|ãÎ
HÁmúÿuS/×kë²Ìe1¨E\x0004\x0000\x0015'×FV]¦N0LDDspmë'ÓéºZ-ëqY*Ü2\x0019Æ\x0003Àx2Y­×ggóéäèäüôl±6äÖëjÙÆ|zt~~rûöÍ~øü\x001fÿ×ÿü_ü?\x001eÏî¼ûÎ¿ówþÁ?úGÿø?üðÖ­z¹
\x0006kÆv:>vvL63.Æ"ÕÈQÎf2)UT\x001cÕªSå \x0005Ô¬¨ãn©$1¶e=yòèÆÍ\x001bÛ}úôé«÷ßôÞû\x0016ºqÆ@l}ô\x001cp\x001f}øÉÙéùh<ñõ|6åô\x000f?þ\x000b¿øKÅèøÍ7ßú\x000fÿÖ_\x000b±ÎÐ¶gggÏ>÷¹[ÆÖ1¬þÁ?øÊ²ÌrûüùY\x0016zîC~xT~üñÇm\}û{ßrÆ\x0000Àw¿ý­¯ýú×4ûäO<~Ò4\x0010c<>>>9}öÅ/½ýàãO¦Ói\x0015ûÜç>|ÿ\x0011Y<?;ÿÒWÞ¼{ûØ\x0016d2\x001eLÜdjÉ<În=zôðÙ\x0019ü·ÿâ÷¾ðÅ7&\x0007<»q´¯ÎÏoáç³ÈfïôôñÓ\x001fþøÝï~ÿÇ\x001fôèô|	b­;d±h ©j°Re`o6õRDA«V^z°À²xúøÏ½~ûæaX¿rï\x0018\x0000Ð\x0016UÅï½ûáùÅ
0	¾U¤\x000e²lÂB\x0016Í8$1\x0018\x00021èð³.ÓÖáÃ(ÐZsr~úÊ+÷ªPÇ\x0018uHë¦iË²lÚz\N¬5²<\x001b^ó\x001c«j-÷«Dç\x0007\x0007\x0007óù<ÏóÃ£Cõ\x0011?>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article2.a974191e.png](https://www.dossierfacile.fr/img/blog-article2.a974191e.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==ÕVÝYDc­\x001e\x0011\x000f\x000fó¯¿þªIÑ^[]/ó2­¨\x0018Êq\x0004¢Ý×LÀAÃ\x0002;jôî[÷/¢ªëþx³ã\x0010&"ô`ßEÈ\x0011\x0011KÔjàzNÓr½^_^Þ®ãLN$¤Ä¤î\x001e\x0004{eN\x0014ÂÂ±-\x001bßÈd\x0001ÈÎ|­3\x0013;\x0011ü@%ÃÙêLDÄÍÈÉ8<xøÉù=\x0008¬¶Þ»1\x001f¶H	øD9	¸­,Ê\x00114u]r*%¡=ù¾\À\x0003»\x0012¨¸í·»h}o¥ÃÞ\x001b\x0006ÕäÑ,S~O\x000e¶æ,¬IÕ¬!2×Iº¾knfê^cIfâ$"¬H;Í53³S\x0004#;\x0003re´\x001bÌÐ¡FØFÕv	IAJ-ê*I$¹Õ²®ã/×ëmÑôùÓ§ËÃCÎùvÌ/£X\x000fØú7J%³ï\x0012Ø¯Ï_/çKD¼<¿ä¼)·ÃuXé×VÃ×;ÛH\x0017.IÝ[lf¬ï\x0005\x0001Þ;ýA\x001b`ÍÙ×uÍ	Øª¦ÇiDÞªÂ¸\x0010/ Òu]g8\x001es`\x0013ôïú¦d­===].×××Ö<åÌÂµÕÚ*dnO\x001f\x001e?~ü8#4[·¯_Ud¿,F)\x0001»ýúüÜuÝÔ¦r³\x0006>áºÖî¡\x001b§I¶Ììþ°\x0004A¾RD µÕ\x0006\x0001½Fl=UäçÙ·ÃØ¿ãõ\x0012ÝgÏý'<îqýßÝm·TÿçB\x001b¬ï³_Ú¹òÌ\x001c!¼;]âqÜïfí~Í
¾Ûßü\x0003IÀ®hú~\x000eðM\x0003°eQ	êàH\x001aöCíÒ\x0012á
-\x0002 òýüèoã­¶µVfVIpÀ
\x000f,
í7Ûñ9æRr)º!¸-"X$§ÎÝe2÷¤pëR4åDZkÞ\x0017'&Ý\x0011_Ù±á\x0003¶fpF\x0007
bî°ÊÉ)\x001f\x0006Ë²äJ×å[«9ïôý·7J2OóZ×Ëùrr³µ®Ótæ¯¯¯­m·\x001b\x0010Êë|RêæyÆzcÐ1U\x0017ÛÒm\x0005E\x0016\J×!¥\x0014ÁÍ,çì\x001e°Ä\x0010\x0011MU£9;mywÂ·ëx}»{)¥äs>Stê/\x001bS¿ÁTPÞÞ^·`Á¼íðØ\x001fæy>\x000f\x0003\x0011!éè'762ôÇÍ\x0012ÂÝ<\x0002i²ñ¿¨¦¦yND¢\x0002ð\x0018¦\x00189çfÍ÷XYÄ\x0014D8ùÆÒÁSoç{3\x001d4ÂEói8ÔwuÅÂdÒvî÷Cß¬A»b`·5;bñ üF6¹oZ\x0011Ý¦\x00199'5Í9¡ÐT\x0015'qwsËüÎ\x000eà{wGÙ²\x000b¡\x0006ÞÛÚ|bPÅ6tk\x0011\x0018Óix}}Ý¿\x000b\x0003Øµ®à·Lã4N°#"Uíû>å\x000cIä6_m\x0006'+ÞE\~&â4lzñØC6`Ê"*n¦Ò\x001bÙx\x001bÍ½®kÊ	8ÔA>G¶ÀõzE^d«9i[4¶k\x0000Fu]ÝlYóù|»^Í7F\x0010Y³6\x000cC.%i¦	gÜi8#d­¡fÀµ9í¶6Z\x0013aÌ0\x0011~ìáá®/\x001cÀV[×uiHýÐ¿¾¾¶Ö~üñ\x0013ÒÍ¶\x0015¨:MS]×M\x0003N;Ê\x000b¿ù?Ú\x0013qÚbøs÷Mfæû\x000ex÷rÞ\x0012¶iÏÐ=~ø;´x
G¡h\x0015l²©¾\x0014~£"\x001b».6zAsré"âþ}ãqüçoE]´é)eÞ¥À(yA\x0002\x0000æ§Ø:qÅ\x0000äÃQ1%jÍÖuÅÐ\x001fô_è¤±ÇÚVD{@Q´CþôôÏo&èÉÖe!vbgRRß÷î­YS¥Rú¸]o(\x000e6@q\x0010fyy~ÁÍüº¼\rN¯¯¯3æ_¶{t~ÇqÚÛÍ4\x0012¯­ÖÈ9¥Ôáý.ËrÀó·hÇá\x0003Ï\x001d73ã8óõz»^ÇV­µHÚ»¨³x\x0008cP.J(D4mú9öpc	÷ðÖÂ\x0003ß\x0004Ç7ñ®+9+³\x0016"'p³ònÔ/!û&"ë<",v.\x0010µÊ©<\\x001eÎóårI)NÝ\x000eQk[3üçá-\x0000\x001a
TM·ÍOIa'GD9óÞÐÂôzgXJÏÓz»Þ¦yn­ùF¢YoäAI¡×	Bd3	)\x0011\x0005G¸k\x0012)Ù[ÛÝ`½\x001aî-¼	³ÇÒª\x0004Iw:\x0013«¤¢¬ÍI8«j0­!D\x0012HÜs'U(§9({\x0018s#îÍ\x001b¹JÒÞ©6«k[ÿíßÿòùó\x001füñ|\x0019þé\x001f~J²&\x0011\x0019§É½bÀÊcÆP-¥d`X!¢
I\x0016èàb²°ÍÆ\x0000×ãÃãb5§¼Z%£n\x0011{ö'\x0000'>_¾
ïKYÍÌZ»ÝæÓ)4©¨ù\x0000*NDXk·ñ\x0006Ûï¤\x0003¸®
b)¼\x0018ìÔ?ýôÓ4)%0q\x001f\x001f\x001f¿¾X1§NáÖÚëë«¨ÜÆ[­\x0015.¨ooW\x0018Sãø®J\x0014i0\x0012QÁqØ3w]7#\x0000átúúõ«ì©d"\x0002ßÒÉ¦¾ïo·Ûé4¤¤Ó¸0óG<o[×2ââQ\x0008bCÿ^}?¨Ðÿ¨8a+Å¦¦\x0000Ä6ý?\x0012(ô¿y÷õýyq¡ñ\øî\x0017ðó\x0006ú~«à« °£@\x0012$\x0002Ô\x001dÌ<\x0013¶n20EI[\x0007øý¹ð»_ïµµ\x001fÅÜýºÚ
g	M/\x001c¥h\x001c§®ë
\x0011MãlÎóNÛX®·V+*\x0006aÎ¥LËæDµäæyÜ¨8Dè"D4gqwÈ)$QÛ}?ôÌ2ô=3/­6[\x0019ùôx\x0017`ZÛ¶ ÍïEETY¸Õv\x001bG\x0010WÀy;N,<SNYE»®ÃíùP
~1EÒJÉ9åfVJy¼<HÐx»QDkííåªYî
ê\x0018$ÞÓ\x0008xyyö\x0014EçízUÑÃxöN\x001eØ\x0011;E°ªîÕ9u¹\x0011ýC	3«\x0012\x001cR\x000fL8	º\x0017b[Ö\x00161þòås×gÄ'#)	oÿù_þår¾¸;ìzSJ)çÖLUöXCÃ'\x0005/A7KÜÄZ[êúÒZWÜPçó\x0019­>U*vÏ*Þ\x0018çP\x0006Ã\x0016\x0005TiÝ\x000còÐ¤	§yk-<æi\x0006ó
ÔÊ=êe\x0001¸'Iùx=\x000co\x0016\x0015¹ïÞêfÇÉ\x0011ß+S67ÙË¶u]#ä\x0004þB L1\x001aÍ9ÏÓ\x000c¼#<º(\x0006\x0011æ[B¤
Jê=ÇPÖu5«]Ï§³9A\x0010ÜZM».«ÈËËËp\x001a6×NÃðZ+¨íG./"\x0019í7ºÓµ®\x0017¹ÌóTk­föôôt\x001bG\x001cè¼é÷l>w´%P¢£Ã¯µ¶Ö\x001e\x001e\x001eÐ\x0015\x0013ÁI3\x0011Ñp:©ÈþýO@]wdüðÃ\x000fã4!uî4 ).¹ê\x0016\x0011\x0011\x0011z\x0006|·Û­¶\x0006»[\x0016\x0006åÉÐ\x0017áQk¦	>NÍ\x001a­ÈVp: É\×õ¼§¤ÍÓlæp­x»¾\x001d\x0003x%ÌüMzë~«ð_aÖÊ&\x000e÷ØBÑ\x0003I\x0007åWî\x000fãð¾º\x0003\x0017ÝÇC÷Ù}}§\x0000>þ\x0015OúG`ìû\x0006¾\x000f¯\x000f\x0003\x0001øxD8}5Ò^=\x001fóYÚ3ñÍ\x001aïÞ\x0011¿\x001d.üeöÑÍÍZJ\x001dÆ©G\x0016¨ZÛù|\x0019ú¾jÃ6º´§ÛXÁZK\x001aÖ\x001fÖápòéã'DÐ\x0011Q]LwÑÅö	Ò\x001f³&hË©Ñ¼Ç1°úo\x001a6<àqF\x001bªÔVX·æ\x0016_ßÞnË\#8#Ä\x001cÞüÊ9å\x0012\x0011ÍAËOÌÎ"ä!ÉÝ½\x0012Y°y4ò hônìDä8q\x0016¡äÞ$@¤¡ØêC°M×KäÕXSÄÚ(,åÜu\x0019S¶þçîºî|9cö
\x000b\x000b$IÍó´,³M[I¡IÍjmåÈ78R9\x0016\x0011à
*\x001aA¢Úv;\x0010mA=O]\x001f.D\x0010E¿Ûù\x001dïõöúöö\x0006Zj«
GB³&!ÞL4kÉÖ5S]¦îuYIØ¡¬0b\x0012\x0012gi³\x0007S2\x0015I]R#¶ \x0011ÞÈ\x0001~\x000c\x0011\x0011£%@¦§KÊ*ì\x0016a\x0014k­P¢Ô%j,uÇ?ýéRÒ:­?þøé£|ìúÝÁP%i*¥4k)RÊ©U\x000ffÓ\x0010ár)\x0005CÏÖÚ84Ìít:\x001dk¬±nfU¶¾ç\x0016ÝÝÝï;Àwûak­V!Ê+µðèí\x001eÄ\x001e]ryxx@O\x000e\x0007ÛËKÊ9åÝÓ	Æ\x001d@pû¾\x001fÇñ\x001f~øúüÕ¬\JÉ///f:iÓS\x0006¹óáá\x00023fUíR\x0002O:<a@Ë}¦\x001fzì*0W}}}\x0005{\x001a\x0014V,ëíR\x0012AÎX­×ëJIfU4x]Ì%\x0004[ÊßÓò×\x001fXpñÇóÝÿÌ'ÃsÝm§\x0007ÓòHS\x0011lÍ\x0012ìm\x001e&Lêù0fù\x000f\x001f÷{>è0ªúÝºúfªy£Ít¥´V¤<\x00067_ëüåóç{\x0007ç®\x0000N"Zz[×µVC&+\x0011!ûà6Q4|±ûî·\x0011è)\x0011­­\x0002ýíºN$Á¼IcR%Õm\x001f\x0013%¢q^67ª\x0008U\x001dúÚÎ´WEHã\x0012Á\x0017`8hJ½êºVk\x0016á\x001cdkÕ\x0016\x0002X\x001aÞïo/Ï«ÕÛm&¢uY(\x0004G\x0015ªR$1aÉ,	\x0016fÛêmr\x0018D¢)¶2\x000fÝ\x001a\x0004\x0007í²\x0016ß¡±\x0014<Â[D\x0018\x0007mb\x0000"³U®´³ma5#lµW\x0014»9ç²áe¥/?Ïó\x0004¤\x0000Þ,îî­¹ÇºÌ\x001e\x0001NHDyÊzX¾YóS.yY\7Lsóæ_×õ\x0008q£=\x0007i*p\x000b
\x000f&w÷¬0w§\x0013ÛDd³Wª+jS\x0018úþv»\x0001Ô^_®Ë¹ï\x0007Àí­º°v]Ë\x0006È.KÛ):&»'\x001bv\x0001@Â,¾ÙXxäû¾_W;\x001a\x001e84XkFR;:w'77'êÒæ{¾q#­\x0007Ì	K)Dq\x001bo]7Ù4Ø\x00121<éºn]«{eæµYK9§]C\x0005£Ø}ò Rú¡¿\.PKÒÎ\x0006Ä
|x¸\x001aÒ!eyzzB
¶ù¢jÂô^Tçyº/µU\x0018\x0003º»5CtEDJß\x000f9eÄt{È\x001d
¼¹§ÞÞ®\x0000.çËõv-¹\x001c~£\x0006ÿôÓO//ÏÏça\x00180¸(¹Ì¼uÑ\x0011q\x0014\x0001K%ÑÓ±Hp\x001e¦L\x0011±®UUN§!¥l¶Â§ÎZ¦	£@±w\x0008öúXî=Ý»\x0011ï­¶ï\x001c8¢?\x0016x}\x0000\x0005
ëceìñÃ[ÐØ}ø\x0000m\x0005ºÜwöt\x0010Ýù\x0018)ü\x0011duü©û¢ü`òÜ7$;áÇs~Ï&û£·/"î\x0012»Û_½?ÇQn'\x0004x>24 1ô}kv½ÕM½®ð\x001eÞ»Ô\x000f¥YÁ	Nióîºn8
*b&]×å\x0011\x0007»1Tÿ·ëYD\x0013¦ßJ¬À5úÃÙ<ÉÖh="®ÀæBõú\x0015\x000e\x0006\x0011A$þåóxÚ¼dM\x0019µi¸æ`ÝÌ^\x001bjÒ¬ä\x0011æÑ\ÈØÛìÞ"\x000c$}È¼	ªP\x0017\x0002SÜ]¨\x0011#`6óÐ¨\x0012îhëÇ\x000fþùÿáã§OçsOÇ0JÕÜ¬Õ×eÚ|èrBwî8\x0003æ9VKÊ\x0019tÉci­ëÚ&Ào[\x001d"¨ÐÕ.Ër\x0010±rNn¾Ö-õ».÷}ùðá\x0003Fp ¦Lãøv}¦·úù/¿üû_~­óR0'![Mà\x0002\x0005|¢\x0010V&\x0012\x0000ª\x0001c\x0015n\x0014\x0011¶F,ÔæX\x000eVÖL¤HOSñ
û\x0016¥\x001cAÂd2E\x0013\x0017síRßlV«4ØdÅt\x001dÿ§ÛÿòïÏ\x001f\x001e~úùãÇ\x001f\x001fDÂÍ)\x0011¦ÒBTPªÎý<ÏË\¬4\x0011y[\x0017á¦[³ÚK9=#\x0018ª\x000cßC¥LY\x0002r§»¢ðP=þÎzv\x0004«1+×êDV«\x0003¦ª­\x00015·ìd\x000f\x0008Ü1;BJ¹ÁcØ\x0002eAMRFa´M0jÐZëûYÖuUÕiçyÊ)ßÆñÓÇ\x0000\x0000×aÍÝ²0<Ì,r9Ïçó/_08Æh\x0018åÝËË\x000b3ËÜ÷}×¥Ûë[ÒRk³õ-õ©\x001bÊm´RzfYþ¡­»òç=ñ÷\x0015·ý\x0001â5ò®àúè±àï\x0000ù[s·þ¦Ýýy!©fÎ\x0014FÌ¬ÌÆÄ &zp\x0004ñ6Ê\x0016aÕ\x001cá"É=þ
-ô7üþí\x0011(&÷ÇÁw\x0018ÖÑ\x0003¼Ý®Ó¹BîÏÏÏ¶VóFÂ-\x001c%BJ©/$\x0011"J¥\x0013ðÅR.p)[SÇÜa\x000f\x0011%X1\x0012Ñ²T$%\x001dÕ'Âbm´:¯ooÓÛ$-h,E´µzm\x0013\x0011©0s¸U"\x000f²Ó¹wóy\x001e5e£8Ó\x0000îYÎ\x0019tH\x0018kk%\x0017gç9Ì×i^\x0005\x0019óDT½}}ýº¶úüü\x001cÎÍr6\x000fªrÊ\x000cý¹KÎÁJ¶Qxó§""æ\x0004±	\x001d¥\x0006¾ïÎ[~eÃ\x001a\x0003º¥ÚYx°S\x0018\x0011²_ÃÉ
»G¼½Ý\x000eÖkD%vTùÌ\x0016ªf³¾¼¼¤Ó	ºÏ®ë.\x000bn\x0019¤ä¦¤­Ù\x0006\x001d\x001eÕ¼\x0007?Â,¢nÛôx· ßµÞP\x000b\x0011Ð\x001f\x0004­tªI\x0015ééÍZ§ïþú)§i\x001c#\x0002
è­\x0008Ì\x0010o
	â¨þÝLuë$á½£3ñ¬æ¤k¬DÄ \x0017\x000b½vpl[<àØ89
°\x0006	 À\x0001Û\x001a°\\x0007õiRÌ 6Â¹j*¹¨¦\Ê>^ ÚÖV[×a\x0002`ËÃÐ÷6¾Êüò\x0012a§ó©V_%iºÞ®ðNHB\x0002dR}{{Ë9\x0003^\x0011Õd­ä	ªG{NiÓ-\x0008»;\x000bc\x000bÛÐ®ëfá\x000f\x0001\x001d\OhÐK*tW7\x0012æx}\x000fÏw¸KGø4NË\x0005g
Æþ\x00118?t\x0011\x0000pSÎ­Öëí4·ñt>åa¦i'$W\x0000G\x0008\x000c¦`P\x0019\x001e\x0000U\x0005`\x0016Hµ¶áÔ'\x0017\x0011\x001aN=\x0011AÉÐ£ìû>\x0001©ÜrÒ7\x0013£þ£êÈ#Z\x0004\x0004ã~\x0007®\x001bÉ¼ÓG{¨\x001e>?\x0007ºÿ>\x0004PMûiþÍr´>»«\x00142#¿[©\x001f\x0000áo\x0000´s{|\x000fî½'óÝýot\x0008¾%\x0005®o®g{7¢Äð\x001e7OÆ»+\x0000å<O¾»8coõ½²<l[]À\x0000ÏçõõµÖúøøøpy÷N®µ\x0011QNÙÝn·+3¯kýùç__ÆñÖu])Ù\x001byp)¥z[[k­¥?8\x000cs."º«-3Aé\x000fà¶ÖÕêþJJ­öüõåëó×VB(
)w­\x0012³ª(%%JA\x0002·r4\x000f\x001eî­q8QT÷µÖ)¼n\x0001¦ú.ú<z\x0010&â,½¹\x0007±\x00119\x0011\x001a\x0006Ì¯NçÓÓO?|z¸<üøé\x0007f\x0016	fþüåW\x0015AÂ°Ymµ¶6ô=®ÿºÎH@f\x0016£-0ÁÝµ÷)³\x001d¹m¡þÍ\x001aSa¦´Ý\æVÍÝ\x001c|¡Ýû9ù2Õu\x0005{\x001e·è\x000f~\x0010ý!«ü×ÿú_çy¾]Çÿå/?~ùúBÊä\x0018&Â&¢\x0011'a!ÝeD]UÍÍ#ÌÉ|]ieD)fä$]w"
gdw\x0011\x000bQn¹.ÁAÒÈ\x000bç¤ÑbåÖÖ5÷©ÕeZ|úËó×ÿÒþñÇ\x001f?RKÖátÒ,a·fëZK)n\x0004kDxP3/$\x0011´\x0010I3Ç\x0006\x001d\x0011\x0008.RM}AØÕkÝò=w\x0000Bè®ÃÿÍ-\x001c¤¡S±I;Jß%u\x0011}y~KÜíåùõr9ÝÆ\x0011\x0006\x001d§Óér¹»µv:­µR2³´q<
C×u_ëº^.Oæ\x001bXÐ¤ºÁPá©jJà{ànµjÒi0(¨­^.fmÓ­JúË_þ4!\x0004ðááATn×[D,Ër¾\Ð\x0006Ø4y\x0018\x001f´´f«èãÒ4)«ªT3'çÍÎñ?Ü§ÿÚãØHÑ#Þ'\x0007Ëv\x0012ü7Âÿ]"|\x001fPàáB8Ef\x000e\x0012¤:5ktp´\x0016µî.àê$ÕúûÌ?Â\x0010º3"¥÷ù\x0012Ç7WRE±øøæiº^oV¡t¥ôÍ­\x0008kÎÝÐ\x0017Í¢{l
É<M"©R«Õu=\x0010$7Ïª$jäÍ¢s&ò®»79~:ú\ÓP×õv»®uÉÛÛ[_\x00128+H/Îó\x000c'ØS&	Úb<EN\x00190ÐFz6çÍvFEÜíË×/\x00124M\x0013\x0014×Ûu]×y]nÓDD­6íz\x000eµæÄ¢§³\x001båÀËJ¥3³JmÎ¼kØ5\x001fg®À66`c?Ä+3òÅ9éÖ<8\x0005\x000b')¤\x001b\x001a´\x0005>ìù\x000c8¬Á3hrßÚÚj\x001d§FuM}_Jau¥®Ë\x001eÞ^Ûíz\x0005ÅEE\x001e\x001e\x001f\x001f\x001fSÒ®;è8NDÔ\x000f¥¶­n<\x000fã§	é\x001fÂJ\x00013$æª`¢Ã·#"°ÿ¤»®»×´`ç|/c<ÀxA\\x001a\x0011½½-9¥Úêé|~þúu\x0018]¸bÂ"93#¿w,\Ì
<¢f-Q\x0016ùÁ poêR7k\x0016\x0011Ýn#n$Â,­U\x0011ÉÀ\x0002Âin\x001c\x001b
fn;·ÜX8\x001a\x0000_C´,K×oÎO a7Ë9\x0011¨^o×s×êºv]\x000f(äóçÏ»0/pï\x0011:\x000c»,u¢Jó4ÃOi¦>G9!¹\x0004³ë6¥äVÛ§\x001f>Y3\x00159Ï@èa\x0018Ç\x0011°&Róàÿ\x0011R¦¤©Y£À\x0002-¹1n-\x0017óÒ6QG×uÓ<×Ö0\x0002)üããc³\x0006²\x0010\x0011\x001dÁó%çüË/¿à~u7| D\x0004Drg À^¶\x0010\x0011-Tk©\x000c$Å±Û"=>>ÚF\x000c.\x0017eN¥J«ÿÇÿÛÿý}\x0013¼+ò\x0000èÜïqÈ­ßÊ=ùÝ/yßL\x001e{l¸Çi}¯²Å\x001b;4\x0003Gp÷[Æ\x0017OºÓ%\x001bmñ\x00165ÐAð½³÷1ßoý¿ç	`òT/ôsøO,Üu]SRfÁ\x000bCÅü)¤¯ëZ×Õ#rFÞîÖ
§¤µ6w{||´Ý?\x0001L8féû>g\x001aæÔ­YÎùíí\x0005&e¸½Ýýõõõ_ÿõ_ÁTs÷¾;±pNÝív\x0013áZ\x001bÞ>\x0011\x001dá nvðõÿÊñ?\x0019?º[¼ßC\x0010"w\x0008\x001c0\x000f|1Ï³Yumþõóx]#¸Zó`b¡HÄ*¹CÌ-\x0010g8¾q\x0008\Â|ióDä\x001ek´Øy3}âÄiÿ°Ø·0U""Ö\x0012'MÍVÊª\x000fËÏ?üøÓO?õC?\x000c§­d\x001fÇ	LÍH)¯ì\x00117lÛèÀn¡å8î73\x001bºÍM2Âæ³I¨v\x0004è{ýÉ]ca;¶ïêÝJY"\x0008óTdó×\x0003\x0011\x0008dA\x0011Í©î9Ïó8Mýõ_~ùòõ\x000bÕF\x0019Fþ\x0014näKaÖum$9{D {ËÝÉ`'L¤IHÒ<Hê4wÍÄYÚî£\x0019\x0007rDPX!!Ú n\x0011\x0016TÉ× Ú\x000fé¿üË¿þë¿þsÉ\x001aaäF\x000c\x001bHy\x000f;úyZ@Õ "tÈ×ëu\x000fÈyT4å´ÅÜF¸½¾¾¹È!ký}töÛê0\x0010sH`\x0008\x0012p­­Ùª\x000c2\x0006Ã¿\x000c§¡ä\x001e\Lq	ØµCïq\x001aqÜ\x000cºyZT\x0014ì/\x0011Í9-Ë\x0004	 ¶_>þùçýõ×-ârÛí¶,®Þ¾Ï*ooo@ã¬Ù?þóôô\x0004oÄ]B]#"gM9ÍÓÜ\x000fåíí4ÃFH,ëºRRmkfúwBôßR"ã]Wð\x0007ðúýw¿ÁêoA\x0019Ü
¿û¼\x0016ïD/k
À{sÊ[¶\x001a`b\x0011¦\x0019hiJ[Ê2ówÃ¢c\x001fû£÷ë­áÖ6÷Rò\x000eiµo\x001cÏùt\x001aÎçË×¯_¯×ëv\x0000µöp¾hÒy]pfaìÎÌîÍÝÈ·+\x0008B¶5k\x0006Ã\x0006a¾\x000c9g v\x0011IEyfp'ð+Àkjm\x0018±\x0001\D¡ÖÌ O\x0002`¯{\x000c©èx»á\x0006üáÓ\x000fÓ4A\x0017TÖº>\\x001e¾>?»ue\x0010yÏC§à§\x000cöµö¿üåó/¿ºû8×qZ×µµ¨­\x0012+â8D\x0012	¸=\x0012¬¨:¶»uã¤8Ê{\x0003\x0016\x0019&Åß\x0016\x001b@Ó\x0016òÖZ=§âÎDbÍº®«mÁø\x0017qiXNL^çÉÚJÌ}ß·Ø&WDäs%!È³m]Ü"²³°\x0008©J×eM)§Ä,¬©ïû\x000f\x001f\x001f\x001f\x001f\x001fOÃ	nf*:Ýnª	u?\x0006\x001bìÈ
ò\x0006,à­ÖjE{¬Fø\x000eY\x000b3/ÀwÒ>	±Úa@w\x0001_2¬¥\x0017\x0018\x0004£\x0005~¿Ö5§|:ëºªjmBts\x001duD¤!^JTR:¦ýrÓ*iÊi¼Í\x001a\x0014\x0011,ÛfûÜ%çM5\x0003ÉRÊ\x0006\x0010\x0011Ñw'h×ºn=¹°GLÓ|¹RÊfíË¯]OÃðúújîÿüOÿ4M\x0013rQA^oµ+\x0005C9¸ôOçÛx;Î\x0000kæy÷ÿ¡Î_\x0005\x0015]Êév½\x0001×ÓÝ
÷þ²,)gî`ä£%84`wÉ¾Ó<Í¢úøø\x0008÷!\x0018w¶ÖÖºþã?üã4Ï\x0018\x0017àÖCåFD`\x0008\x0018\x0004\x0001\x0018¢_×6£|øðñð¢½]oH®µOçe]`öïî§ÓÙÝº®;Î×Û\x0015³ëe]>}út»½ÕZKI4'¤Ýóõöv9h§§§Û<jÎÓ4}ã\x0002¤I73\x001d÷Í[D\x0018EsÄÄw\x001cïd}ÿ\x000e¿/(ï«¢?:á%ÿíé²µ¯;/Hÿ¾êh*\x000e£ß>62å_ýËÇïùÝìB^oVñ±¥Ã¸;ûV1Ã²6c`W\x0005¯fs
ÚÃÄPbb0¢9g÷<ã<OîÖÇ¾\x001f\x0017pìÆÛt½^?}úäfÌ"ÖµµÖÜ©UÓ´m%h>\x0010Æ1MíÜýø¶\x0018ý]ªôo>¯÷l 8\x000eK4rf­ÖZ4½\o¿~y¾Ýëm
Wf%É)d
ðþØ)DI²2%!ksxõVÃ*·:Q4NÄ,\x000eêjîÙ\x0019\Ss\x000bZaêODÑ"0óårzzú\x000f\x001f\x001fáôññ	\x0016FË²Ü\x0017\x0013­UÚ\x0008»;©Ì-\x0002ò­\x0003­ßmNàó\x0008ö¸uYPCÚk\x000eeÖ@F<¤]Û2ox¨þkm¤÷
@¨*a\x0004I\x001b¿Î+è(*EK«M5G\x0010¼8HE\x001f\x001f\x001fÿáço·ÛËËË4M_¿Þ®·ÛíæÎV:_IR\x0019Nnâ\x0014áõÀME²D[£FäKJ¬Ü\x0016NK\x0011í%åN³mnÚá@\x001c\x0019^ÉCø\x001ca\x00165¢\x0006a¤æeýýÿ×?ÿúù~þùñ2<=\¶úÆILb]×&rÎ)Gp×\x0011³¤¤0M&\x0012B8Q9
§i\x0011	Ùu\x001d1\x0011Rr0x©f­UÕBÏ£Õ
\x001f7Õ<yfùôñS]n}ßÏó\x001a\x0011Ø©ÍmYËùqçq\x001aÝ\x001cz,\x0011y{{[êìíRr]×®ëjkb\x0006Ø¬¤¼zk\x0016±É\x0004k­¹\x0014M
òÏÃÃ$´Y§\x0005
\x0011µÚxëõ:®ë@\x0011¦ûYhkÍ¬î78¨k{\x0013}xzª
æ\x0014ÎÏ__y³Íaò`Ùôñÿ
6=ïIØ±}ý7\x0007w
ÄYÜ_'pöþwp{°\x0004 \x0002`\x001c\x0004s\x000f{\x000fë8hu÷TÒ¿ñ5#a\x0000¬0ÜÚÁ~:
ã8AA{:áýðë¯¿Âà\x000f?³3Qs\x0004·¶eö\x001d;JJªè®°DÉ¢z­\x0012ÒjSQUá=ë&6\x001e°\x001e\x0003ó£+&Ù,wQB£|9_¨g(ààúÔZ¯×ëkzÅL	Fsz}½.K=
\x0003À×¾ïû¾\x0017y\x001e±óXk_×úòòüë¯_Û²FÄ\×i\,HY{\x0011(\Ù)¢1²\x0008k\x000e Ï@¶óHHCV\x0014ñ\x0016\x001eaMµÐý·ù\x0011\x0011û2NZúÝNçY\x0005FG¿É 2
M%\x0004ù6D$ýåbnfµ¶Uµ°[I¨Ù,\x0011á¹%¨OSW\x0006PÉ¿|þr:JÊ¥¤¤z¾<2[\x0004\x0006Å¦üuªææ.èÙÒ7\x000eTÇQ\x001b\x0011Ì²¤¼5XEÁ§ÇÍZ¸»w9\x0013QÒÔ¨\x001dÂ\x000cìQ`YÎ\x0019c
8çXk
Ô X[µR\x0012\x0005A1\x0008\x0004¯DA´0Cè\x000fj\x001fL~º®£ðé£\x0007À}Ó*%	\x000fÛ%+ÛÚ)¤Y»\x001d7;êì2µyU\x0005^\x0017p]\x0003¥\x0019ì\x0008Û\x0012iq#Bî¸m§)C*¾k\x000fÉbøýy\x0010qAªQÕykkãí1BRea\x000eÆLÆÍÇi|||\x0007.®ùó×¯ó<_.\x0017Umµ\x001e\x0010a.\x0005¹òª\x0014§···þãàfÌüóÏ?#sz³\x0002V\x0001\x0011èè
º®«ÕaX×5çt»ù¸\x000féag(KhY\x00173ëJGèt\x001aÐálUM©Kà~N'\x0014RÎÂ¦¤jµ&}{{Ó¤aÞZK÷7	*$Q\x0015Õ?Æîäúû»²°\x0019àóø##þÖª\x0000ïùít~×S¾îÝý(ÈþÆ\x0007Ém\x0013\x0011Éw/\x0000Hù_ï\x0001\x000e½Á\x0011ÎrÏÿaÞªx3«uÿ¨&÷wsL\x0008\x0007\x0011îPJÁôÑÝà|RJVUøÃÔuÅ²î!ç².mÖEDTKÒ\x0010Óóùl\x001e//¯""\x000c#üøø~\x001711Â\x001fP³þzÛst/÷\x001fÖnÑ`\x0001Gçi
íõõöü|§µÃDTSp(},"$Y8S­Ë[x%kL\x001e\x001e(Y[("¬µ¶X+§³t)&wô<­\x001faè~þ?}üôÓO?°pkkkííåÍZ\x001b\x0013\x001an \x0010¸íû¡wsÞZ­¥Óé<.\x000b!±0D4Q\x00081;\x001f>\x00159å¤\x0005\x000c¯"\x0008\x0015%0z\x0001k­ëêÕHï9\x0010í¼\x0005DT³Ó7DÌ¬à\x0012/ë\x0004n\x001e\x0016ÕþpU!ö\x0008jÖ	Ç\x000c­\x000e\x0010âááá§~úïÿÿ~æ¯_¿~}þüüåóëëëõí¶Î£¦I$L"\x00110àÁ\x0014IU³¤i\x001c(ªT7¥<\x0016ï#u"EHHSs#V\x000fhï<(#C(\x0012R(G\x0015\x0012oíùËµ-öññÁÿÿñ\x001f\x0010v·Õ=Ü|è{"$\x001fÕe©{0¨èm¼á²oµK³\x0008ïº\x000e÷Å<Ïç~`æÜw(Yj­´\x000f¾þ®G­n^æËåDD\x001eÖDìDbNëº\x0012´¤\x0005ÖÔæ¶®5©6kê
Õr×uP2KÊIU\x0019\x0000R§ÙXÂ¬NÓÔuj`Ø
%ÕËùRJ\x0001OtY\x0016
çéôp9Î×·7¦ã4v9[³é\x0005g\x001e\x0011yÄ/\x0011á\x0007\x0012\x0008wBkäFðò3OVk\x001cD\x00119§ðhá¥¹ÿ½¨
\x0011Bw÷]bon¨ýmÀÿ\x001eàþHìæoÁän\x0014¡ÁI%\x001a\x000c.7»t³ÍGõ\x0018füí=ÞG»À	Î\x001b³iJ9'Ðc\x0010ß³{e$\x001dæ¡¢\x0014á­U÷¸&ë6Aßú±\\x00185hd^\x0017£Ì9k2
6Èó*\x0011\x0005\x0005\x0018ùÕ\x001avx¯\x001b
\x00154E`\x0007Ä\x000bíoÊi;p=@\x000cÀ\x0010I^oWk\x0006\x001eÂº6îw]çáÔEÔ[mÛ\x0001÷òüöúúúòòº®¶.ÍÜ,µt¤I%9SÒbFÈd\x000eV\x0011\x0004Q3\x001db_ÞMD\x0018û¾²ºKE\x0008\x001b$áp÷'\x000f£\x0016\x0019#\x001d³v\x001a±ÕÚj#ö¤Ð\x0007\x001a¿[?S)i<knÍcK¦æD,ûûf+GDS)B\x001eaDÞÚbîëjÚõùréûRJªëªH\x001f\x0017~|¸A\x001dÛu\x001d¶\x000b\x0008Ó5%qÙJØo2a¶1\x0005>z\x0007VëÐu¿·\x000c)< \x001d\x0002v»9¬gÑÍµi]WÐ·¨ÏghÏ@=Úï\x001fGNNÊJ
²\x0000ß}3
¿Û\x0015TÔZC\x0004w\x0007Ú\x001c*+¼hP?5o\x0011XR\x000c.°\x000eió\x0014k­E\x0010¹ìnÛp½YÓày§i¦\x0013ibÀÐó<¯uM¸"@¤\x0001ö1s/R0\x0007PQ#Cz#ï\x001eÊÍlY¬zÔx	Á½ÖÀ°mµ><<¬ë
7!·÷B÷pZqÏ\x0010\x0001Ù/gL\x00051Ì\x0001Á\x0015¥\x001dú\x0016fþôé\x0013b¡Õ\x0019oc­u85Tø\x001f~ø\x00015É²,µn$p8RÀì!çm@îÛdÉØ6\x001aQÝíÈT\x0012¥µÎD\x001bë/UáXCA\x0012áá¢I§e:çó\x0002Ñó7&ß[(\3âÂÛ\x0016è®\x0019PÝ\x0002°¾[¬îï4¡Öª»ªÆo³º\x000eOÎ\x0019 È·\x0007\x001cæÿê\x001eÉ>Úø6\x0008F5\x0001×\x0015\x0011¨~û0³Ãî}¿ùÈ\x0019[Öî¯\x0007¯`{\x0003"D\x001e\x0011»ð·\x0004$Ù}\x000c\x0003~Ï§Ó@§aYyO§sJ\x0019Ó+Xeá\x0003\x0019Á¬ªèm\x0001¨¤Z[³n×H´Ö¬ëº;\x0014¿û¹|7Ê¿Ë¿U]ãÿ\x0003ö\x000eç¹®Ë\ßÞ®×ëuZj­VH;Í½h¿.¥\x0010+\x0010%Ú6q\x0001æ"L\x001eµµ[óêHä\x0014NAÕm%"Ýx'×$?ýü\x000f""Ê*2/£&Î)kâÿò_ÿeèû®ë<ZµjPß?æyÆ;½_ÍZk3cÚùrA%Ç,æ5,Ü\ZEk\x001e ½³$\x0015Ìò"âv½MË·xC\x0008!N¢ÂbÖl­aFð\x000c¹Czl¿?\x0008\x000bD)'ÿI\x0007Ë\x0005QáºèÅw£"\x000c=\x0013R9GD­I\x0002\x0011-Ëòåë×¤:\x000cÃÿçøïþKkíùùõOú÷_ù¼®-ÖHHRp2#r*PFkuME7\x000f»Q]×:¤/)\x000fÌ®(1v\x00082jÂDÌäP\x000f\x000bXÑQ§¤I#øz§q\x001eU?<#§Ì\x001coo·óå\x0014\x001eã4YsÔOµVèá¶
·Ce4\x000c]JÊ3ßn7ÔX\x0013ÆPÌ\x000cøy]Ûý\x0007»ènÔ(")Éi8Î}«õz½jJ­nK\x0018¡¨(r\x0003Î§óé|\x001ao#¬åaÇ^J9¹çòå\x0001\x0014O¬·¤Ú÷\x001b\x0008S&×·\x001f>ý´®ó¯¿þZJyxxàZo×ªæúáãÚê/1fæ.)2\x001d1 uUR6±r¼oP¨tÏó<Ë²¬kõ\x0008a½^¯"bFÕÔµAè\x0012ý=½|S\x001b|£\x0007p¿k\x000ep¿ùü·ô\x0000û\x0010\x0000(©+b\x0019#<,,Ü®\x0013QM-ö»=ÀCßxüÊº,R)%¥ôúúðu\x0010\x0015\x000bà\x001dµV#6\x0005\x0002\x0000µ{
\x001bf\x0016n\x000eZöæÎ33×¨\x0014´]\x0012fá\x0010X\x001f\x0010\x0010DsÇ\x0017D¤¢=r°5cá40K]Wìh\x000c|ÝòáAc«­öýPU4<Nç\x0013\x0011­\x0001ì\x001cosRº.ß®·/_?\x0003u§õíú6Ëº6&
WbIe`\x0015"£\x001b\x0005µFL)©°5£Ø#\x0013ï&Ï÷\x000b!"¸¡ue\x000b$e3\x0013KT%
\x000e¥u­ë§\x001f ÏøñGw\x001bÇé4\x0008\x0000úy}}½?Ó=b]&;R  \x000egbJ,È9D¸\x0017)Dææ-b\x0015Én¼;I² i¬ËR½¹
¥¬)¥)MÀæ\x001e\x001f\x001fû¾\x001fÓù|J9¹ûFÇºo&·\x0010U"anè\x0013tsÚç{¦X8j\x0012m­©(è+µVx¼\x001e´çÖÚº£$\x0018é,ËRS½Ç5ßÝç1m£f \x000599\x000cZ¾±QNó<#±\x0018¬w\x0017èaRDý(ù\x001dpàÅ\x0007ÃYº.»»\x0008\x001döG¸*\x0014ö%¹ªÏa(­5sÙ¨¨x\x0004°\x0006k
õ®0ßÆ[«íáávÛÿ	àm\x0005[kÒ÷H{\x0014f´Äªz¹\Ú\x001e©\x0017\x0003v\x001c2­[­ü¹¶æ·\x0011©ËårMóõZk\x0005\x000c\x0004l1®W\x0014{]×ÕV¦óm\x001cÑ9´Zñ\x0005\x0002æPSw]§)I1°EUÿðpy~~Þ3Ô\x0018qTª\x0018@}üø	
?¤&DÔ¹&\x0005êÑj;¬ö=ÂÍSÊÐ=ç5iG"Jáï\x0001x\x0011)%Ï·=HA\x0007g\x0015f&Þ¨&fÆìpZ\x0000uþ\x0008:\x0011IÛ\x000cù|¾\x001ct (\x0007\x0017ß7+éãû\x000ergJ\x0019Ü\ü ú¡Ýÿ\x0007uÔQU\x000fJëoÉ­½_\x0005üÊ<O²iÆ¶õvhkMÄ\x0001Ïà/«¾SA9%=¬îñ
?{gíy
Ösü\x0018\x0012Ý\x001dý+PÚ¬V|èºÖiOç3n¤£0""\x0015\x0010\x001c6OOO]×Á2E$jmëº\x0007jTX°ãLÚ\x0007\x001dËrx "å\x001e\x000c;ºdfvßÄÓªBÄè uaR\x0011ÊÓ´\ßÆ¯¯7\x000b
g\x000b%"Òj°ö;\x0004ZYUÁãw²jõÕl"©NäF[ÉÔ\x001cæÙu­Dt\x001aN\x001f>~xx8×¶¼¼|­m\x0017Û\x000f?|ü§úça(\x001ekk­Ö2ËìNó´^×+ìÀZ[rNÓ4A\x001eSNI!9Cõ\x00108á\x0010âcÇ°9Â4"Öjî[&T\x0018øì\x001emY%
IÍ9©Ê!,ÂRiÛÜ¼ës`»¥\x0000½^D1ÿÙãåWÎ·Ï"¨\x000b&i
)\x0019Û\x0011\x0002§¾\x001f¬a]Ý\x001dà\x00111\x000bs°ð\x000f\x001f~øô\x0007/Ëò§û·ÿåù·yÛr#\x0011r=_Ê¹Ë§ÖÉw\x001bQ"#:¿ÖeÒÜiî4õ*=v£f\x0011\r!\x0017wæPW\x000f[Uæ¤%Y]¾~~ýÌÿÏýç><|úôisI\x0013fX×2Ì"èÄýæ\x0013Ñ\x0002â»{+¥¸§ÞV···\x001d#ÉCßSO¯¯×-$È\x001aSd|_bÅaþ\x0016u][#æ®U­­¤JÄ\x001ca¢¢ÊªHÊ¥Ôu½·u]___5¥ÇÇÇKx`àfîó\x0019¾ wç\x000eã¦ËåRk%\x0012M
öà\x001fOÃPkýË_þÒÌ>~ø ¢ãí¦%üø\x00114þt§9ûÿó¿»ùÇOú~Hª8Úq\x0002!9a­+¼¤¦u]O~Z×õë¯,pZ,¢Ò\x0016Ë¢]#Ü»lfou&ÿÆAõ?.»¿¥\x000c\x001d­{hìºd(\x001f°+þ¾æï\x001fø>£ûÛ\x0011ÔûQ
};í4Å}ËEc\x0006»!â­ÝmïïtPh~hsîz×´ß»)¸\x000eÌßmð;Ï\x0013Ü½r*´û8mÓ\x001d\x0008Õ\x001b>úã@iÍ)Ä¢º¹(a\x0008\x0016¾ùy+imÌ[F-Y%1¿×f²±,· ¥ZJËM%\x001a\x0001yØ _ðO>!å§y\x0006Aâ6ãmB¨ÖÇ\x001f£¶úòòòüõù6N·ëí6ÞÆÛL$\x0014Ò<¨ÕÒ÷N)à¹BÄf\x0006AÐ/\x0013èy÷¹«¤ã3uKIá1ñ¶¦\x001có<wC©m\x0011¥.©
ýøôxêÊÃãYÓÐ\x000fýËóË<Ïÿò/ÿÔ'an³Úd~yyÑ¤¥¶´u\_®·uµÛ4×µó\Ð\Úº\x0005`±db!Jñÿ£í¿º$I4QPª\x001aq\x000f¬8ª\x00004zzX÷}Ý?°÷ìãþ¤ý»/wÎ¹Ý
 P]¨ªÌ`NÌLìyF\x0016i`ºç:ò$¢"=Ü-ÌUE|¡\x0001\x0001\x001a$\x0004\x0005m \x0002­ÆHR³Ô,µ=åsØwc\x0010[\x0019½§ÓyYãñÔ÷}?ôãþ:nöA¶É­±ÓTêëDj}®?ÞjS\x0004_N>êÖiY\x0016¯\x0016w»Ýñx)y\x0007ÚÙ0\x000cÄïõ|`C\x0006\x000eþYÔª¦[¾¬UG\x000f®+ÄVL3&\x000e°^´x\x000e\x0017©\x0016UA7q`\x0004.mv<ºïUm	ÁC\x0016¢9 _T\x0001,Õ]¸I3she\x0014]a\x000exCÄeY\x0004ü?%¼þÖÄ\x0010K[ÙÕ\x000eæq\x0018Å2/¸©tt]ôô)\x000cÃ~¿GÄótö\x001dz{{»,3(jkf:Íó~·qõ@ð\x0016xÖîX£°é~\x000eÃà\x000c½7oÞÌó\x000c\x0000]×9¯WD|;Ci&/Èý°ó\x0016>\x0000´ZM+ëx	GÞê\x001aÁ3F\x000fûn<¼R\x0011Vc¯\x001aBp\x001e)\x0011Ëó=©0³@äYhÀ\x0015wZkmM\x0004,xâ\x001e7\x001eÇV±áÍmRÑªÍG°YÀh]óÔ§½/ÖÝnçàÝO­zù´ÙÌ\x0003gýïgð÷*=fæL\x0008\x00004¸Ì\\x0010Ûy£?jN¯LgÀK\x0002ïÅØá\x0004°ðÊÉ\x000b\x0018Ç\x0011þì÷ü-T×.\x0005"n\x0019°mv`íG"ª<¨8Ã\x0013}Ù,Á)è·®5w®ø%ÒJYO\x0018Ã0v1\x0005\x0012$"µÖQðÕSK©­øIºn×"Çifê|þMT)ü¸ûÊ~wï>`ynDd
ËR\x001e\x001e\x000eOÇãIÔ\x0000Y\x0011\x00100\x0000F
\x0001\x0002"1®:³èÉ´VÓ,å\x0000R\x0000\x0004V\x00160!\x0011\x0012Q­\x0012\x0002;¹*v!\x0004,uº}qÍAc¤×¯_¿xùÒñyÃc.ç\x000b©.çìÕÆå²}â\x001aÃ0p\x0008»q¼»»Ïy\x0015GòçÏ\x000bà%A¨\x0017UY"/äü?rÎ!ð8îÂ|
¹©Õ*Á¬Ã"¥5p\x0007º\x0015\x0014MH*bD\x001cBÂ´áåVÁ,óÅ¥ê?®N?p¹$fb\x000e\x0010Èj\x0013\x0015høÁ4cN f©ì³2ÚÝªM\x0011\x0010\x0000Í4iÖð¯¾úÍW_ýù?ÿÝ÷oßÞµR\x0000\x00033¶\Î\x0008¼ææ?\x0008\x0000  \x0004ÁL­´Ú\x0016	3.p\x0002d\x000cDD\x0010\x0010,¨\x0001\x0012²\x0011%#\x0004
&míLK;Oåüã\x001fº/_½øê«/B¤¾ï\x0014\x0014@qték/iÜb@VlÕ|Y]×	¨¶ú~ô\x0019bã¸«µÖºÓ©¹«!HQ3\x0007\x000cøùä_c\x001fãÎOS?q\x001f\x001f'ùZ×uoÞ¼ñÓ:ça­]0Ñ[þîË»,Ëy:Únµ6fêûî|>z\x0008\x0000¤µ?ù\x0018æir\x0015\x0011\x0017x!\x001eç£Õrss#­\x0005\x000e¡]×=><ø\x0007½&\x0007\x001büÃE<\x001c«}i\x001f\x000eã°\x001bw\x0000\x0010S\x001fOO®dÂ]7¶Zç»ÄþÒ}ú0D¸7ÊÄCUM}Ñü¯rýýy\ø6­å~ùõðå\x001f\x00168,\x0004ñR\x0003<w{ü¥\x001báõí9köïÇ'Ð­	ó
¼ÞBú*Lw\x0011´¸¼ËzÍf­)@±h!aÚ¬\x0018ÀL1\x0012\x0000\x0014\x0000P©"1F$"©¶¿¡®ÉÌ8°3}Ý¸´\x0015ùs:]uÊ.a¾®"ÂV[¡å¶ßï\x0001ÀiC7Nót:\x001d§ã2/NÄ\x0014yYJ6Svnn)ìzi«\x0008 U\x0011 @!!ò\x0007å³qç\x0007b\x0012­ÊJnD`ÚZ­\x0003G
<~òñõ8îö×ãõÕn\x0018{2e4mÍ¤QÄ*K`úèÍ¾>Emu\x0001Äãy.¥ºÀá<OûÝÞ4£E©ÂH·7»Û\x0017×­	\x0010·fOÇÓãÃÓ\x000fï0\x00053«"`f\x0014\x0018Ìüã\x0006Èbh­¶\x0019!q¤E¤Î9Æv<SÃ8¦JÅq\x0018e9O§iîº®ï\x0007\x000f®nl¦ã0º¾ïÁ©*:ßÌÕ\x0005ü#öu¹4\x0001\x0000c3³V7/Ùnz'\x0017 ²@jkS3@ð¦uq±ÌC$g \x0005ÿ¦"Ð³µêÓi×®S\x0015 1ºü\x0003nÜ¢\x0006ð$àR?./ê´µâf!"!ÛZ?87	w»]\x00081Æh&\x0016ÌõÁi\x000fþ\x0011\x0018ÝdWT<Ügù~O<\x0019XGUp·Û\x001b]â\x000byÚ÷Ý8xÔ}|zrÅ6Ss\x0001\x000e\J
1¸m´\x0016Sò¼\ZÎç¾ï\x001dAÄÏ§smmY\x0016¿çÓÉ'QnÞâc7\x0000p#°é<\x0001Àííí0\x000cH(*)ön*ìä%5\x001bÁ\x0007ãfn,·VK-\x0003÷}ïû×ç\x0000«Zq\x0008MDD9\x0010jóo2«¼?\x0019÷û]S
!P!¥´¹9HmME[nMÄµ\x000eÖ\x0002ÀëBÑM2ö1Öt>_àæ­ÉEf1çìOsxÓeU=/\x0000ú¾¿¸Hv]·}îHåßo­z}r¡v{Xl\x0013\x0010gB :\x0014r\x0015£ó&;MxþíI\x0007GñAÄ/\x001e0ï\x000b\x0000o¹©ï ¢`ý°+ÌÌ\x001cý\x001cr|ÂÅ\x0012ø²ük×ö!Z\x0015i\x001c¥êW±µVb@224kÌÁq{Lèf\x001c¢²,KàTk]"­q oÚFÚvYf¸ÜøKHª\x001f²}øOÔ,K~z<Þß=ÒT«±¹¼w\x00178\x0005÷V6rê6Üd6±\x0014µ
@Q]º\x000cjmC?¾xùêöö&ç|w÷\x001dGûøã7/_î?þä6¥µ,çR\x0000 ëã/|²ªªµf*B­lD·\x0018\x0003s@Â§§'×¯\x0000ó4ùäææ¦\x0003d}­úG}>e3ô\x0011¤i§óTrk
ÈATÝ\x001c~Õ{æÕ¸gE\x0016úzð5&â²nLë\\x001e\x0000\x0002A \x0008 1¦.u~Q4\x0007ö\x00004\x00137\x001f1c!ÖÊå³`rËC\x001dìDÀHÄd&`\x0000Ä|©\x001a¢h @æÏ?ûüO>=\x001f?üðîo¾É¹ZÍJ^\x000fèg\x0004qCbLØ\x0000Hó¢-4\x0014¢@\x0002÷\x0004TJ#ç0P0PU@b\x0004^J\x000e\x0014C`\x0015¥Ôº|÷çïçyúÕð¢ïS?\x000c¦hfS\x001d®àí1\x0000ÅëêRÊ0H\x0018(\x0000@µæº"újm\x0002¦q%¦\x0019ú<ä/ä¶¨"ÍCªRÎ5Dº¾¾)MÓ1çÙòýîú2mÅ¹ÉÇãñt>ÍÓ|uuå±ØGÀþ"¦yÊ­4K1\x0011ª¨
¢Ê¸\x001bÇa¬µÎÓäÎ5Ãá³??N"\x0000\x001cOÇeYö××ÒD[­µzÐ±%\x000e'H1w­ÜFC¨­9«\x000cÉ\x001c­TJiµ6-»Ý°.\x001e4êBj}ªUsý« Sïçûø>³»ØÙ¿â°õSh\x0010ýûJË\x0010ÀL]NAÕ\x0004\x0004Ø\x0008=\x0019j
¼\x0005ïëÙÍz\x001c2áqø"ýü¯@LÍ\x000c\x0014VF¦Ê\x0005½pI¾»nMì@$uÝV\x001bÀ
0Xgz´Ú\x0013ú¹F+·Þ7Cz\x000eHV«`@F\x000e¤ZÁÜ \x00140\x0005\x0001¶©¸+M\x0001ÉÚª¼´Ã\x001c\x0011äb.\x001eïÚí­µ~è½Uì¹Å-Ã *¥h'"õíÛ·Ã!çêºdÇù¬.è!Þ\x0014"B4tÅ`0\x0004°`È@\x0004Èïþ[Æ¿}!ÏhÊ\x0004LJ  íjwÕ÷»óo~óÕÍÍÍ¸\x001béx|J)ç<M«w&U[&&m ,9pD5T%c\x0010©K~*-\x0004¦\x0000uÉ)Ä¬³ÕVCJ]7¼~³»ºNÿé¿ü.çüøt<\x001eÏw\x000fÇ*\«\x0006îÐ\x0008L\x0011L	\x0010ØúhÒÐªH
=\x0016&à\x0004´º,\x000b\x0011ï÷;\x000feÒ\x001ap(¥æ¯¯¯½T2Úùtöf(\x0012Ê*k,
\x00010@x/4\x0002æ_`^Ù½"Ì\jqyMO`SA´MÌ]cE7\x0014)6¢\x0000¨¶÷3\x0013¨\x0017Òä\x000e
àx\x0010ÖZ¢U~Ôw;n¸5t/Bs\x0010Fï._º'\x001em#d£\x0019U´I\x0015i}?ª\x0019À.¹:FÄy]'·ì¦Z\x0000 \x001b³\x00116á¬5±Q)yÞå\x001c\x0010Õ\x0003¦÷ï\µ¶\x001dw¬¢ÇãÑEe§ùx<¦ü6µbê_|\x0010ÄD×l\x001c\x0002¢ªÄ|8\x001c\\x0008¨ÖêêÏàïº®µ6Ïó¸\x001bUõáñÁ­!SLRêûÞ\x0017³K6å3äi`C\x0006r\x000eûa^'µÖêÚJ¹äýþªIó÷\x0012iUîÆ±¢"L¡\x0015­­\x0010\x0013\x001bz^\x0014bj*MúÝ µ««})uf¿M_ÍÌ>ä\x0000 QXA>´\x001aÄêfÚ÷\x000cs=\x0011aã\x0005etYf\x0016£\x001bT©m
Ä\x000e\x0001:\x001c\x000e1ÆÀì©U?ôþ.Ã0zmsö\x001b\x0000h5Ø[ÁýÏ'¹È\x0006Æìu(c×\x0000À?MXË\x0006
!úzý¹\x0003@ý½\x001c!¤Ö\x001aS`Ø'\x000fªêåûE·ô2vP5\x0017ÿ\x0001\x0010¢/\x0017XI%è\x0004pf¦YUB\x0008ûÝ\x001ePsÎÄ(RDªhCZ§
+Þ7ºÿb»ÜyD\x0006\x0002\x001e\x0010R
Ë²¬­%"ºH¬\x0011ÿ+Gö{\x0006_¡Ic\x000eÇãñÝ»ûÓa9çØ\x000fÒù8#AT\x0008\x0001"Ùê+®F(¢³j¶:YS$×Ó\x0010\x0003\x0002ôÆ=½ùø\x001bþýþ÷ÿØ÷éó_}öÙgov»®Ô¥O±µúôp¬­úr'ÀéxrèK\x0015\x000bÁs\x000cú¾S-¸ßïú¾7h¹Ìó<\x000b±¹d'3\x0019áR\x001bBVJÉútOSD[Ñ³3¬ê¿UT\x000c9:Ý\x0002ÝT%ÅÔ\x000f}­\x000e`3Wñ\x0006 "ûgq¹ùþu \x0004+)ð~¿ßïvÄ\x0012;Ph0¢5Qs%\x0008¼8þ:Ùùß\x001c\x0008p%r]8\x0003Ä\x001cõ\x0019\x0000MUj[ùúúz¿ßýîw¿=¦?~ýõ\x001fþðûíT&\x0000G\x001ao+! ""\x0002!4QÈÚ`\x0000`bnC\x0006\x0008\x001c\x0010\x0001T ò\x0018\x0008D[-5R\x0010"ðîÝãtþÃßýö_}fÊçéRd"î{7gq.ïgù)¨"*¬¢Ï»\x0006Ø\x0000T01]\x000br_ºáÙÌýW¸º\x0002úf²È\x001ejÔZ\x00081t}\x0000àééÉ¡.l\x0017C0µ*õt:ùI0Í3\x0000¼¸½uLj!X²{\x0011úz3\x000b\x001cB¢\x0018â~¿w\x0010·\x0003îÞ½óBÎÙ-(Å\x0014\x001cüªâCßW?rÊ²xÜßrMíºÎMÓ\x001e\x001f\x001f\x0011Ñç]föôxL)\x0018	q\x0017g\x000fûÑÃfJ	 ý5\x0005ÀòãKB¸êýÅW¿g?{ü\x0002$É5Ä>|è%Xáú\x0005\x0011y»Æoo­+*ÆßýÂ6Y¡\x000b7ðå²	Q¶#L]7\x0006\x0000(Y4o+n(£µ¤ª!p\x0008ÑÑ)=2ÇÀ\x0001"Js±Y3Dd\x000e¤¨
Îí¤\x0008µ¦ªV¥¨¨â¦dfj\x0011QQE®s\x0012FmKà\x0010S!\x0014(è_\x001fOGi\x0012bô\x0013ÐW\x0005\x0000N§Û\x001b'¢jß÷*2ÍóÛ·o[Õy)µ4\x0000\x0010\x0003¢Ðu9îÆ+DnMs-`F)\x0006\x0001S\x00011c'õ\x001a(zöO \x0006u«\x0004t7Wû«¯n¯®wûq\x0000y>ýéOzõr×uÌ¬ÓôÔê¤ÂDÔEJ×;U\x000bCäq×õ}ÿôôs~ýúJ[Î3øT\x0011J)}?ÔZa¸¹¹\x0005Õiª´\x0018ciE¤:¨ætÌ|sÓôæÅo¦)?>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article5.96ad31ed.png](https://www.dossierfacile.fr/img/blog-article5.96ad31ed.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==]ßØ\x0018\x000c\x0006kkkÉd:Í¢°uM§½vg}}½Óéloo÷z½£££ét¦éÉÉ	"~õ«_===-"\x000cÃñdÂÎm_»Ö_êß½{ïÞ½{\x001e=üÂ/Q\x0011UUM§¹ÛíeéUåúý~q6¸ÿA§ÓL¦ï½÷Þ\x000b/¼xóq+~´¿§µZ[[{÷Ýw¿ýíïÝ¼yí|8\x0006²,Óv{{kÛ:wãÆsnººÜ__Û\x0000QÛÛÛE^ô:ËeY\x0006\x0000\x0010´ÛõÉ\x0014\x0000Ö76ó7~ëî[HÒ[gg\x0003[ÕQT *£åÍeëì»ï¾{%¸ÒïõTãáf\x0010	WV|«5¢kW¯mnl¶Z-¥æ¢­­­º®ó</ËòülåÙd<ÉòìñÁQÚNû½~»v»KEQ´â8ãV«Ê²)"¥i»®«8¢8>>©l\x001da\x0018NE¾ûÝwcfn§ªª'©³R×Î9\x001b\x0004­$kk\x0011)\x000cÃ¶´$év½\x000c­m}zzV\x0014y+nm_½VäE]Uãñ8/
feÓv»=\x001e¢$IÀ Ö¶®Ù9D¢8"\x0000°ÖÁ\x0005ç\x000bÛØ\o%\x0011\x00013P;iM§Y9©²<N³V+QZ\x0012\x001fî]­çõE*äìû.
Ä?rwí£ßø1`þ8G5\x0013Õ¿LNº
o¬\x0016\t¾"ó\x0013AÕ\x001c\x001d³X]D¸,¦j\x001bÀ¹0\x0008xÊìÂ04Ê°ãª®\x0000@Ñºk¬<ÙZ[Wu^äÎ¹^¯g]UÚÚuUçuìl\x0018ÖZ$tÖyÒò1ßt\x0019\x0016Òhùc_jÇL^px\x0006ñþId­\Knßé¡yA\x0004\x0004.ú\x001c²\x0000Ò3Ï\x0000fÒþ\x0014\x0008Å\x0000\`\x001d#R#2ïï?yz´m^I\x0002Ü0ÝÀ§\x0019>AtÎ)\x0013XÇ\x0002\å÷ßùîtT!V+KKW·wêÚ\x0012°B\x00006~ú<ÍÎlù)+Ix*|ííxñ÷¹Ä-\x0000\x0003\x0003@ ö\x0012½ÏÐ\x0001F\x0000$\x0011f×èÞÂ\x001d5»ß\x001a\x0000¸9T©
ÍNÞ÷èÐ](\x000f76\x0006D¥A\x0008ÙÁBú2©ãÍE.ïl(¾`Ó^,qÊ·\x0012ç2\x001d\x000e$4Sým>D\x0018\x0018\x0000èBÓÃgs³F ²ÄE¹t ÎYa\x0006l:-éµkçªrRÓ£ó\x0013Ðæ¯K+k[WvúË«W^~\x0005,ÛÚæeIÌý(Þ\Y.GeÉ¥uàÅ1;°¯\x0014(/I\x000c3<\x001e>%KËâ\x0001 GÒ\x0011	Z D&f\x0000¨/\x001e.cÈ±\x0008[çµQ\x0014\x0000)DAtÌ\x001e¤áXÐU\x000eÀHÀÀY¸.Ïâ(£8\x0008TÍN\x0011Ö\x000e£G÷ÔáþÃ»ÎòÒrÚí¤iÒívÓ45Q\x000b\x0008\x0015
#4tUËÂNÐóÁ½ÒEì8³ÿý¨\x001aÊ¥é3K\x0015ý\x0006w±>CcSâgË?Ï¨½Ôêì\x0019j`7Ò¬3Þö\x0005gDU¡E´òÅ=\x0002_ÜVìIÃE\x0008\x0015çe	ÈA\x0010öVs+k\x001b¯¼öÆh4ZZY\x001bF'''£óÁÁá1\x001fÔJS\x0012ÅiÚJÓ¤ß_jµÚ\x001e\x0019ÇÌH¦IU\x0005i»íÁeTê¬Ë²\x0012±\x001a\x000cFDäÑ:¢PSd"\x0011\x001cF÷÷å$Mû½%«Û?\x0018<¸múË«Ngss;Â$IU\x0018¢V\x0004ÞÑ»<¡Râ\x0017Ùõº¤î°ðó'«v]\x0012Üà\x000fË\x0019.~nä§¾õòëxP1k> øä×¯ê\x000bïãEz·\x0008£w1iüÎýzÏ"Þ³ÁóÝEc"\x0001TÚ§N¬°ø'I± 9T4SeÃª®Ä\x000bÎ\x0010\x000cÌ\x000c,ìæ+*WN"iûA\x001c(M]\x0017i%Ó¼(ò¤vÚ½b:µÖ	ÃÐÕeQäU]\x001a¥\x00081NÚW®ÅÌì;?=\x001d&ßýÁ{üÍ?!\x0017n¾ðæ½í$ùsy«×»Ñcª
Æl2>Ë4í±uuU°u´R\x0008\x0000l­\x0006®ó½p\x0010#\x0011q\x0002ÄY\x0000¡ªêÑð9v Ü¤Ö\x0002R;7\x0013O~¢êÍ\x000b½!z*qþ¤!c 
\x0002ZïlnþÖoÿÖÞÞn~õzµ³HX×µï¤ú§æèèhme}þÞþR\x001d?zôhssÃ\x000bÝx5î¼(HQ¿×\x001b\x000eZ+fNÓÄÛ\x0018ïïï\x0013©ÍÍÇ\x000fÃa\x0014EJ©óós\x0016¹ñüï~ï{Z© \x0008\x001cs]UwïÞ[­/¾à±ÈMcPætÎ\x0012	\x0003²&bDÕxucÌÀ(B "\x0010RuNÀZN[ÉÄ1\x0002\x0004&Xé/Rß}û×?ûY\x0015¯¿þææöÚÉþþ~§ÝËò|i©WUU\x0014\x0005\x0000TeQ\x000c{½Þg?óÙ7ÞxýÖ­[?øÁ{\x0000\x0010Eq¯'×®^}ëÍ·ÞúÌgÒ4ù/ÿÿroïìì<\x000cC­UQ\x0014¤è~éONN¢(Z]YuÖ¶Ûíl:\x001dL&yuu5Ëóªªþù\x001füÁç>÷¹ªªõÙééÖ²,¦óó3[Ö£ÓóÑ`ÐNÛÉÄ\x001bê|Z\x0019+è<@Á\x001e=>\x0004M\x001bk+Áéh0È\x0007¥Nï»÷n¼p\x0015
Î\x0007FåÞÖ
Qßº}[+õ½·¿»µ¾½²´Z\x0015ðþû·\x0014\x00194*æ_ùWÿã[o~v}sãÚõë/¿üÊí[w_ýõ¤\x0006A$"¤´­\x001dRJ~äìéÓ\x001c¶\x0006\x0000çX\x0004PØ>³_z4ÿ\x0011\x001e±xÚmãëñ\x0004\x00166þO)sABgíÉÉI\x001ckf¾}ûöo½n­ÛÙÙ\x0019Çï|÷»Z«Vh¥OOOëªJt2°sãñx4\x001aùc\x0019FD\x0006±\x0004ÍÏÈÍ^\x0003^\x0015Þ\x0017kç¡¿&2Ú\x0018ÔÈéé)ÇéÒÎj.\x0002J½þæ\x001bEQlmn~é÷ÿéñññÖÖÖùé±6F+eË:Ï²¯~õ88ØLÇ¤`:\x0019mn®Â^¿C
íx<öõÇ\x0019Êä\x0002¯\x0019GÑt³c\x0005\x0008ì|
Ý;i00\x0002\x000b0%X\x0008Å[Ú\x0008\x00012\x0012\x0008»°ÎOaüta
\x000bQÏÁ?\x001eèþc\x0005\iSPõä*8>\x0002ðDdnhû"M~èÛZHe\x0001jf&\x0005,\x0017E$0±/´XØ1\x001bÈÂ
£c¨\x0002\x0012qÌ²h ð¡EõOu|5\x0001¨®*óø è.ýê¯~áî½ßÿg·J_¿Ù~°?21(\x00130\x0019	¢åÍ.\x0003YP«§\x0010Ö:\x000cL\x0018(¥\x0006A«Õ\x0002,ËªªZ]Yi§íÚ¶®45Æ@\x001cFA\x0010 	D¡vÎVµ¤qÄ¡ç#b\x0014vÚNÓTie\x0014)"¥\x0014x¹Ô\x0019Ã2a\x001d\x0004*Ï\x0000 P
\x0000«E\x00132Bq(¥²\x0016Ä\x0015E6H¡³B\x0015\x0004Ú\x0000ÖÚ\x0016áP\x001b\x0005¤\x0014 ")@p¬\x0012ìv{yÅqkkpÞ[»»{\x0019æ\x0011\x001a\x0000xôpw5\wu­\x0003W\x0014\x0004ñû\x000f~ïÑïýÖ¿õÛÿæoü\x0006Ûj:\x001a?È\x000b©3×]_k±!<LÅu.\jôE0\x000fiá°c\x0006Ä\x0006\x0000\x000b\x0002\x000fØ\x0008ø2\x00104%Àfr\x0003øe\x0018\x0005Qù\x0001H7¢£\û\x0008\x001eVa\x0018*e,×"Ü\x0008ÍÄÀ	XÄ"0sÉR9Ém!X­ýô% 9w\x0010@MC\x001d¡\x0015ã\x0000÷n¿w<ÞÜznyuûðð¼Ýî\x0006E;F'Ôx\w.UHìQyì\x0005Ð\x0000\x0015[D\x0004Q
	N\x0008\x0017;©BD36@\x0014%´QÆVJQ\x0014ÅÎ9"R¬WTsÁ»÷0\x0011QØ\x0011}g¦ñ]"D\x0006&ª\x0015\x0001D\x0000¼ûèÁù`påÊå­ír<©­ÅÆ\x001aU\x0003$²¢V ,9ïæåL\x0011\x0008ÖRúJ ó\x0005àvÚ/Ë\x0012Á¬¯mwÛ\x0003À|:q\x000e'yÖÛ·>¸7\x0019~ý/ÿrc\x0015ª²È'Q\x0014u\x000e½ªù|\x0005hüS^n.õ\x0017gB\x0011?\x0016ÇD\x0008çíÀ£úiÆ
\x0001Yyã+qQf\x0004ã9\x0004}VS]¨ÏJÜócö«56\x0015Ôq!`°\x0000\x0015mNüit/tMÈÛ\x0000ù,^\x0000\x0000A]¸5e^Rì«x,,Â"Q\x0014­¯oÂ½½½ÕÕÕ4ÿäO¾qrrÒë÷ñ¸XY^L&QÔ2A\x0017Eå^kNO\x0002D\x0007
u¤ágxg_@/¥\x000eÀÞM\x0002M\x0016­] MÝÅ\x0000"Ò&:ËË®ÊÎÇY\x0010\x0004½4ÖA¬\x0010:q\x000eX\x001c\x0012±DùùPóÞÄ¥Ùsé7¤@\x0018D\x0001[p^«L+l¥iY\x0017ká	\x0000\x001f>~ü÷Þ[]Zm·ÛÎº²,÷H\x0006\x0000\x0010\x0006­\x0004Ò±£ WC\x0000dÓ»·?888B\x0001­tYN\x0007t\x0010¡À\$Z	8\x0011å!w\x001fÒU5:ãD+]ÕÕh4éõt¯ßAÔ­8ÚÛÛ;<<X[_ÝÙÞêtÒÍÍµõ\x0015d¹ÿþ;w>÷¹Ïm­oloogy."Ó3\x0011¹x\x0014àúµk§ggç§gÓÉ$£ªªÛíTD6Ö×oÝú`<Ü¸~³(ÕÕÕÍ­­ªªsi\x001e\x001e\x001eÞ¼yóàààñá\x0011\x0000ôû½Ç\x000fÊÚ\x0002À+¯¼bLðÎ÷Þ½õÁßüÍßÜÞÞ\x001a\x000ea<Í;N»ÛY*N§óÚk¯­®®özZ#!¦i{ss»*9¯ÊÁx\x0014¨Ì&A\x0010£\x0011#\x0014EI\x0013[­«W¯\x001d\x001f\x001f\x000f¢ZYZ&2÷ï=èt:F\x0005\x0008ªÛík\x0015
µÖ*IZa\x0018+W®üñ×ÿøìü¬Óé<xøà7ß1ý-ô\x0000\x0000\x0000IDAT8:~<\x001cï\x001fìj¥È`:x÷éé¹Ñ&\x0008L+YATKý¥4MXd<\x001eû-g0\x0018\x001c\x001d\x001dWU¦ÉÚÚZDÌl­KÓØr|v~V×u§Ó±UA\x0000q+ÖÊt;©­ª|:\x000cGÝn?^
«ªª2iµêª
Ã~+n­o¬[ë¦l2ÔµN&¤(\x000cC\x0000FÂº¶UåD\\x0014Ói¾»»Ëì^zéå0\x000c\x0011Ñ:+"¤T+\x0008\x0010¡¶%\x0000\x0010)\x0001ÔF;\x0011kë8\x0011ñðèDH!dÝnÙ¶Z©ÒºÆÖm>ä­\x0016Öa\x0000ä\x001bü\x001fÕOýPfêªõ°-ü\x0011ÆbÒ-Øúñ#÷Yý\x0002ý,Þp«0"yyØ\x000f;\x001eÿ\x0003/ÈÎ¹ø×ù1?Ñv}z,^ó9!Ì\x0013\x00174i£M·ÛU¤ò¢(²)\x0000 "F`ç*[[ëò2\x001fGÖ:\x0006èöº	c#*ÂÇ4\x001a4!ú\x0016\x0005!Rs\x001eáâa*\x0016>øSÑÎ_<þÂÕBKõ\x0013&jl:â3ýdf\x0006ç±x\x001fuî3s\x00171\x0002¼Ãê*ó*;\x001f\x000c²<'É\x0014ZIRU\x0015\x0000\x0018m|S¤iÃ\x0010>=g~´:OD\x0017å²ç\x001fóieû\x001eF>ãbýp8'\x0012j4Ðø¼«ê'È¸xõO²zx
ML)¤ó\x000fÎ"TBûÜ\x0006\x0019\x001b\x0015\x0017iâ*B\x0010\x0005\x0006É28\x0004\x0001a±­@é¤Í"yUgE\x0016\x001d\x001f>zÿx×"ñ?û'\x001b[;7^|ickÇh]×y~V±R¡\x000eÐ¢²ì
Y	(ö²ù%Â¹Èè¬«÷á øY'\x0012\x0010µR@DìC_=D\x0000P
DuÖ3*¼k&Ìr:\x0008Ø1kqÎÖÎù5®ªª</\x0001@kmÉ¼,KF@D«Éhsm{\x0003ò²LòÇ{Êè$Iz½^+íllmöúýîRt\x0004\x001aÀ
¡\x0003@\x0006ËâccB\x001fÂOÏêìëöì\x0004F.àu
÷t¾\x0006.è«\x0008R¨\x001cè\x0019Z\x0008@\x0019SÕEVTè}²IV»Ýîîì\Í²ìøøx8<ßßßôàá½{·OONÒKË½³³sR´³¹\x0011ÇqÜ«ª¶¶ôyn\x0010\x0018ægôÊ:g­o¹yÑ×0\x000cIk"jÅ­n;5êºV ¸*H9­\x0002[w\x001f<rü½w¾Ó[ZÚÜÚì-­ìììè0\x0004_Q\x0006uu=Óudðã
eü|\x000b\x001e\x0000xñ§úú³[Ü8µ B@\x0011\x0007"BM=8@lhþ\x0000 @{q	bvìe`&\x0011eB`ksUÍ\x001e3e#\x0011\x0011FÑÚ+%²c®\x0005H4\x0008£F\x0000ÐZk­ãVÜî¸ÚÚº®³l:\x001a\x000cG£QQdÉ¤*²º®µ¦(
B\x0013 ! ùÿmlíe~zzZ±\x000bàý;wî>xO³/|áW_õõµµµÕ K*Më¼\x0008IUyQT¶°62Ê#Öç¤>\x0017	\x0011!û\x000e \x00000Ce¾(\x000f\x000bA\x0015G,?§[+%Î"Q\x0014E±X[gyÞ®ÿ«uÖ\x0018cyîús¯¼òÊx<®«\x000bizEÊÖ6ÏóÁpøòÿe\x0014E\x001eFF¤\x0002\x00134p·Ú:g«ª²µ
\x0002ã!um£(Jüøøx2\x0019'IË9ërÌ¶®«Ù\x0017Í7Ó\x0006*\x000b\x0011)RÀ¾ºvá[4öEß&\x0010±$\x001eA¯X\x0013zø\x0013x
1\x000b"\x0016ENN§(Ña.ZÒ\x001b\x001b\x001bß~û;Dæ¥\x0017_ÜØÜxøàáüÜM\x0010\x0010Ñh4ºÿA\x0014E'''_ýêWÿâ_ü7Zq|çÎÝ½Ý,Ïÿýÿ?\x001eOö÷÷G£Ñ¿üòÛiÙe¹³³3\x001c\x000eëºVDo½õf\x0018\x0007\x001fß¾}[iÍwï\x000e\x0007Ãv;UD×®]|xèyºyQø=7Ë¦Å4·U¥\x0005;N\x0015uUF#ETº\x000eAX\x0013ØZ\x00088\x0008Ãñ4__[)\x001e>üÁ;ß{þÅ®moi¤²®\x0002mH¨,s\x001dFQ\x0014
Î\x0007¯¼òò·¿ýö/ÿ\x001b¿²µ¹ù7ÿæÿâßúö\x0017¿økû\x000f¾ôÏþûýýý²,Ãa¯Û]^^zøða]Wa\x0018®®®v:\x001dÝÔHý\x000ctR	Àk;\x00151ôTG\x0000,|­flú?\x001b³ìòSÍü^¿¼¼ì\\x0011Çñîîî+¯¼\x0014F¦Ûí^»~ýðññòòJ\x0014'''_ùÊW<ìÚ¨(
ë¬1Ú9+¢6¾jì;©~ÍF$²qCX\x001cM½µ¡\x001f4«YÜë­¯¯OÅô{½ÚÖKý¥Á`ðå/y2./-Çã\x0015¯r¶·¿;§Ól©¿äØ\x0005AyeÓ¬ªj9¤\x0002\x0000kà¦uÖÙ \x0008ÆÜÄ\x001eÌ/²(@\x000fKõ¥X\x0006dÏÇ\5çgêýÉÆÆÿÚ\x0006q×Àè	ðºÿ§uÖ9ç\x001f\x0010ßå±¶ö®+ìSiFp @3O¾\x0014­+å\x001b:3 ãÏô@4I\x0002L.v:¿ówþÎg?ÿöýßü·_ýæ\x0019\x0018H
P\x0014qz6Zb\x001aP\x0011\x0011éV¤´ÑF\x001b\x001d\x0006Z©xm½$\x0000M§,²ÜïÇQå\x0013[Va\x0018\x001acj[:×®4Æ 
)$Q\x001cõ&C*2A+i¡	À(m´Ò¾\x001d\x0000Ü\x0008ÏG\x001fû3 çÂ\x0004\x0017!GSXcfaL'ÓlHU]ÖJ)[×L¤µ²\x0016À\x0018dvD\x0014j
\x0000Ù\x0004\x0001³Sq\x0012h­»Kp]ÚIzz~~ttô`÷áÖÖVç\x0004°´´,Âµ­µ1\x0002Nku||üÿþû2þö¿õUUí\x001fì£C\x0010WN£\x0011L
åÈSë*å*ãS³mÂ\x0005\x0018_äE\x0005T­\x0014AaafçqØDZ)$\x0005P{9]¥K4C! X¶¥uÓª\x0018vJ±³\x000cC6Ì4À\x0008X,h±\x0002\x000eEÐ±³U=r\x0007e1>=^ÝØnÅÖAÕî\x001aÛÊe@a\x00050c\x0005x#*0è5ç\x0010\x0015ó\x0002JM\x0003Õ_ºæ\x0011öÿA\x0005¨ÀÛ=jRJ)£QFy±P\x0012Îßet \x0014ÕµÀ\x0013B¯O(ê/$ÔØÏ\x0002\x00008ëål2Ú´[\x0014E¿·d©k§\x0000\,)J+\x0011QDFÄZ\x000bBÖY\x0004E¨ý¦é\x0018\x0001¼\R\x0018\x0018°\x00150±U½¾¾3\x0018\x001e\x001fì\x001fì®-÷¾ÿÞûë_ùå_ÜÞÙZm®KðýkW]´3Ñ¯J\x001fþÜ_þ\x0013=Å\x0011ü¸ÓKþój\x000b¨ÌÄh&óûÑG¾P$\x0007¸¨Ó^²kñ±¯Tþ¤ÏE\x0001RJ\ó¥¾ªU´Ò`K-/÷"\x001bN¿øÅ/þÑ\x001fý\x0011\x0000AÌ\F£VÌì@\x001bcf·30:|òr\x00018à\x0019§áâbøÿ &R¨\x0010I\x0018EÙé(ªköÙR¤(dæQ[w\x001a[­@\x000e\x001dW^\x0012\x0005øÃçÑ\x0013HóÈ³ílgÏiÓ8`vi\x0000²\x001eP (iÝ»w/Ó \x0008´ÒIxÇ\x0013ëÊ±«kNÓheyã×ß"££Çû\x001f///_ßÚb¤º²qÔYá«bOO\x001b\\x0018°ÿFQ\x0014EQ\x0018uíò<\x0007ä<Ï­s®¿ÔoÅq\x001c·¹ÓIÖ{\x000f\x001fi­ã8VJeyîó<;==Sä[t°µµù[¿ýÛ·oßzôðÑ£G^\yAuU;m§ib´ÉBXÖÖÖvww«ªJÓ4Ë2¥T\x0018ËKËDô¥/}éí·ßNÚÝåååo~óO¤õ÷¾÷½\x000f\x001fÞ¸q#N\x001f=zôþûï+¥[-¨ª*N.¼f½/FUU£qöxo¿ÝîNÆE\x001c'J\x0019¥ÆZ^^N&eí\x0010 Õm]\x0002ªN§\x0007\x0000\x001eí%QK¥´¶¶\x000f\x001eï\x001fì\x0013AQ\x0014þÞ­­­)¥ÒXWµ\x0017Å
L\x0010aksëßùß¹}ë½ßû½÷\x0011±ÝMã8Úß?(Â)Zq¤i·ÛMZI·Û÷v$§g§\x000f<.ÓK1ù{\x0001ÞqÊVK"@åQàu]²õµµ0\x000c4	`ÿ`w<®¯¯+¥¤ÎÙ(:a8\x001a
´\x000e£óì4\x000cÃ^¿·¾¾\x0000l#T­86Ú *ë¬­\x001bÀS]×k(@QDæGÈ"I6-rf×ï/U½sïn^ÖZE¤uy-m§"6mÅ¥­&ãq6£\x0016VÚ	¢\x0016¨\x001f²ÖêÙî.@àX
î"c\x0015Ñnü\x001aO/\x0013\x001f³
LJ!"»KìÛ9\x0010\x0006`¦>ëKxø\x0017ûÍÊ"\x0017ä×§ê\x0019\x000e¬Ïú\x0016D,b<\x001e\x0017EEDËËËkkky3\x0008\x0012
¡ï¤:Ç@8\x001eOÎ\x0007ºªÆñÊÊ	C.ËQ6É³\x001c\x0000ÑqÜJâ\x001c;\x0011±\x0002Ú0\x000cõÎò§rï~¦RåyöÄ­gªï²cT2\x0017f³cKÐì£Ï>Áñxüøà`8\x0018v:-c²7oúY\x0011a^\x0014um«ªòÅy¾È ýQNÐ\x001bÐ,~Z£>
Ïè
ÐlÓm\x0018«ÔÈ<\x0001:{â&Êâ1Î¯É}×ìO\x0004ÞäzFùm vj¿ø;²Ð0»\x0004§¸|\x0005`±\x0017{\x001a>ÿÒ;y®YÓõðÙ8!=õ(x	\x0019çHx¡â0ãÎ2\x0012ñòºâ!¤U³ #\x0018\x0005,`	\x0004¹®«éø\x0011Â0^nÇ+=SÕnU%[!5=Ýÿú\x001f\x0014vïêó7ñ Iû=\x0010[\x0015¥\x0000¡sì¬Xg\x0017¤\x0013±â*kÅ¨Yb÷Ô­?qvëQ<ÂB\x0013µÖ+\x001b7\x000b\x0017!*²µuì\x0008	\x0008DfÍþ|^úÒ\x0018¥\x00142»ª*Ëºò
LM\x0010µ1:
M\x0014.\x0011
"ÖlÏN\x001eïï=¼wyy¹¿¼v;N/i§iÒq 4¢g^xÕßf\x001a3ÌxÄ\x0017ã£\x000bÂóÉ?£}#¢jný3®Ôlºðe¶c3
ýog¸T9óµr\x001ey×`\x0015/@fÊØs,AC±\x000e"¶V+
ÈDä¬e jm_¹¶}åÊë¯¿yxxprr4\x001d¿óoÕÖ\x001e\x001c\x0005JeÞï÷;íÒJ\x0001RZiMÚÍÕXB\x0006[×þîÔ¶ru=-KFPD(®¶£ÀF\x0003çX¸\x0002À*,CçÇG÷÷\x001eUÖ]½~}}}}emÖ67\x0002cT`fOö0\x0014.ü\x000cV'øò?ãc.÷½pãÃGYX	g«
¢ö7½\x0017\x0002\x0008ÍoØq#{Ï¬\x00140[¯p\x0004¨\x001c:\x0007¬\x0018\x001cÏâ\x0008	Å9WY²¥÷>gf`F\x0016?\x001d;vä' ÏàÁ¤I	È¤ÝnwÛéd:ÍÆYe^\x0014Åùàôäô¤,ËÀ\x0004iÚâHÇA`Â°v\x001cÆ-/%m\x0003\x0013|ïöí{»{iv»ÝW_~é³ýl¼²R=: PÎÒRj[WyQ%\x0016´8w­Yä"0\x0000y/XR\x0014E­4\x0019öß/øÌâfxu\x0006ðF?\x0011ä\x0004ÔUi\x0002¤é½oÜg®1UUQ³\x00170!u:\x0017_zñk_ûZe\x0017©D\x0014EQ»ÝNÔÚ\x001a\x0000Ò4-ÂYçu]û
Ý;@çE¦Éh¦äGUÕçç\x0003cªª4\x0012!Öµ­}5yá8\x0001P²Ö9f$$E
E\x0001k\x0004M 	H!\x000fqg
Vd£\x0014!°&äÆ§\x0016|(Ðør\x0001\x0000ÀýG\x000f«ªÚº²£B#ÇqÄ[[[×®=ÿàþÃW^~m2É\x001b\x00170aDRJ³R§§'£ñhiyÙ1\x001c\x001f\x000f\x0006çÓ,«­]]YÕJ½ýö;"|ýúµ¯~õ«^àhuuu2\x000eÃ,Z[ë(ZZ^¶u´Z\x001bÿîïþîÛï¼óàþý¢ÈãV«Óé\x001c\x001f\x001f[\x0000WUo¾ñ2¦ª*¨a:¸ªî´ÒÅëc`T× Ôjµmi\x0001	X
4Å¡iÅñþþyùøÆË¯\x0014Î±«â p\x000ceY¢Ò;W¶Þyû=\x00119==z÷\x0007ß{ë­Ïý¿ñ7þêïþµ\x001b7nüþþÙÿç\x001fü\x0003F\x0018\x000e«ëkA\x0018îìì|ó\x001bßN³4MñÅ|h\x0000ÏÞòÀåÂâ_?ýÉ=ûdB\x0002÷sOòû)L\x0008~8
â\x0013ÚÖDj{{k8<\x0005<Ï³<K;­ãããéd\x0002\x0000q\x001cµ¢èèèèää¤,Ëna8Í2[Û0\x000cëÚ*Åa\x0018*E¨\x0015ó\x0013îï$Â\x001eKç¿Ö\x001fqø]eùôøDiUgõÑÑQÚJ\x0002m2ÎµRÁ¹­ë8L\x0010@UÅ­HÇIgR¥s\x0016}Ñ}\x0019Yç¬­ëº¶³Þ÷\x0007ñ"5\x001eêK<
LFÈÀ|§H1\x000bòpU$ü\x00112ÄËù5øË[ÉÂÏó!\x001feîógãÙ\x0003eRã±Z8ë}\x0002\x0017Ð«ªÚ[ó\x001crÆRÙÆ[H\x0008²ïÖ à¬ÈHu]«?5ëªO>ÄMÇ#££ j«81\x001cþ¥_ûK­´ÓYú¯}ç\x0007Ã)ÔX&:I»=Ú!\x0001Àt:Õ\x0004q\x001c\x0005Æh­1A`Öçgg®Ö\x0000àê2\x000cCp¶*s.ÀvÚ
ÉK°u\x001dh\x0013·Â8\x0008Ó$i%q\x0014Elk\x00020Z·$\x0008\x0014ÂËÌ\x0001Ù°.Ü¼ùñ\x0013 c#C%h* ÖHöIJ´µ1Ê\x0018çS4Z+ÄÚ§þ¾>KD¾\x0012Uä\x0005)Ð¤Ø\x0000,'Q&©«ëÁà|¹ßëñhÐíöë¢\x000cÃ0Ï²[wo]½úÜàìì?ûÏÿÀü\x001b¿ñ\x001bkkkwoÝîRP
ØQ;µ:tÆ°¦füèZJ£Q\x0005\x0000s0·_l?d9Á¹ä\x001d!RÓÏ\x0013\x0016DR¤ä	u$$m\x000c5¦B¾Ö\x001bE£0*\x0004[\x0003e5åzÌ®@b­Q¬\x0010"÷\x0010\x0001a\x0010\x0001b%è8#è\x0000¦8ÔµåIv:8¬(gÜ4IWí\x0008uUUìH\x0004¶IK\x0005g)\x0003	V$L \x0018¢Zk-â|Ú¢ÒZ+¥\x0000ÈKt\x00126§MDFkÒ´o\x000f\x0011&4@¤D+!¥L]O\x0000@¡ ¢RÏTsÁ\x001a-ÊP\x0014Ä4\x001d\x000fÃ¡½æÖ××}?|»Z\x0004Ø "\x0000M¸$\x0001KÀA\x0000\x0000PVï>£0\x0012hC\x0000ÊV\x0019©°è²²Ê\x000c6·¯\x001e?Þëõ»_øâ¯ðÞ÷þéþù/ýÅÏ¿úÙÏ\x0010³%\x0013Q$\x001aÄ·TIÐ?5L\x0002â[VØX-ÍËË~\x00021"]Ô¢ä£¥>lÊý)ç¾WH3\x001d\x0000\x000fDkzr3³F­`æ4 #xj·m\x000cS\x0019érÇý\x0010Ý\x000f«ÒlSËè8Dôe[EJ¼·"\x0000\x0008À9\x0000±&m¯¼óÝ·\x001f\x001f\x001c¼þÆ«/¿òÊÁþþááa¯»&í²,­å4IµÆét\x0004À­8Á\x0004g\x0006¥Þ<\x0004\x0005\x0008½ø°°V\x001a ôBR^\x0014ÐKk\x0012\x00020¤k¶\x0000AêºvÌ *\x0010íFÓéñùxcµ\x001fè\x001d£\x0000\x0015@\x0005\x0004@ó\x001aþì
 \L\x0005*\x0008]üÃ/Sþn*"¯®\x0004Èì\][£M¿×SDDãFêöÎ½»Ë++\x001b\x001d¶\x0006\x0000f\x0010ËÌ Ö7k\x001did \x000cºÝå7ßú÷Þ}gwïáp2\x001eMÆykÒ
	\x0015\x0002Àb¢kÖ$\x0016\x0000rçf9\x0013 ÷Å¬m]\x001653+M­8^Zî-//?ÿüu/\x001cõ½ï}7Ë§Ù4ë¤©µöüüüððp¿ÞN'ÉÙÝ¼y30ÁÑÑÑÒò²ïN§/¶§I¤)\x0000lïìÜ¿/ËóÕÕÕÝÝÝ\x000f\x001f½ùæ>\x0012®ªj8\x001c¾ûî»Ãá°Û_ã¸®ë\x001b7nllíÜ¾}û½÷ÞÛÙÙyíõ×Æñ½{÷ò<_^N.
Ñ\x00080kîæ\x0007Ç§'¬X]Ûè/¯\x0000ãt2Ud×\x0011E\x001c"\x0010\x0011\x0018cë\x0012ÛÝ^\x0018Ggçç¤h{{{{cKDÏN'Ùtuy	fam\x0010 \x0008üIeÙ8¢n·\x000f\x001f>\x0004V+
Ãpcs\x001deY×VDºÝ®÷ã\x0008LyÇc\x0011X__\x000fÃÐÏjO\x0003õ-Û4MÒ$Zj]çÌ¬LgYUW¾ç½¾±êõË2\x001f&ÎÊîîÞÊr\x0015\x0004\x0001\x0000Õu½¾¾~|rxzzFdÑZ\x0001¯\x0014\x0013"jEa¨ôx<¶5· \x0008b­1s¬\x0014\x0019c¼öÞ<\x001bbp"¹\x0006\x0000\x00113\x001avw÷NO\x0000`p>[ñ4/£8Y^Ý\x0004ä ÐI\x0012WE	\x0000I\x001cæÓiYY6\x000eã(/Õ\x0016>lhïÒH¦<µZ=ó\x0003gTøñzo³÷²ßì~V±¿mê©ÚGC<yâ \x0017´|gÊì<Y?z0ó;w&¼Õ
®^½öÂK/\x0002\x0000(\x0012Ú¹º¶\x000e\x0018\x0000jg'Yç\x0019J:i\x0010\x0004|zrv:\x001e\x000cÃ0lµ\x0012ÇÌÖz]SÇ\x000eY´1ixWçýìÓ¸õón½o-ÏY¹L¾Ovï>Ä×s¶²Ã{&íRãÍ	¢¨[Ûb§Ù¤¹®\x00155ÝÙ{HD|KÉ-\x001c­À³O¹ÈòÁÙ9[\x001bÅÑÚúÚK/¾Ø]ÌÔh­\x0005ÄZ+í\x0017¸ù·?}>,Õç\x000fivÂL·ö^¨\x001f\x0001U½H¿[\x001czá\x0008½\x001fm3=lÍöa\x0012"Î"±f¸ÙU¼èRÓ§_v|â*-È\x0002\x0013¸KzãtÙ\x001amÆtW*\x0019\x0011\x0014\x0011£ÒÀ"Ö\x0002&%\x0002¤@\x001c°6*Ò1#\x0008£Ø
ceZ½\x0011,`ílí¤´®¬ìîí÷î¼÷âvekçúµçn,uzØJüJ]×¶²µ\x0015f \x0006.Ùåe]Ùºvâ@\x0014"û×qÓÛ¡Yö"Öy­b|\x0001@JùV,z³[ê\x0006Ð¢k¬R/¦°(¢¹)1Æã|wg\x000ecgE)¨\x0000µ\x0004\x0001&B$Ï%R´b²Âg'G\x001e=ãØ
_¹ríêõki§&\x001d\x0015zöHÂ,	¯¡UåÀXö
*³sOJi¶ë9õÓB\x000b\x001c0\x000fjà\x001dUHæ!P¾0j\x0014{YmgëÚ\x0002¸9¾G\x0001®­nlmollmUe¾»»ûàÁÝÁÙùþþã»ùý4ÓVÒívWµVJ\x0005\x0000 Ì\x000cà(nµØ9MX\x0013!bYPä\x0017&i2
EÄì\x0002ªª¬s­\x0003MN\x001f\x0011ólxûÎðö\x000fVVö\x000föV××Ö×7N\x001dÃ+ú6ÒâgîÔ\x00174\x0005º°Ëú
B>Ñà*
-@ñ"·iB\x0008¥¼îxü\x0005*babÒÌ
wG\x000bÕ"\x0002¾;ÎÊ_.k-[ÇÎ8\x0011¥rT£Cç\x001atA£àmé¸©$­V¯Ý©ê²,³l\x0017ù`pÖé¤ãñÒt<Îòi^£Ñduuõtp\x0016a§ß×ZYë³RUQ+9=\x001fÂðüìLiº¿ûèÎîîs;7Ö·zqjº)\x0014E¨\x0008²Ü\x0015-³²¨æ&	^µË_\x0011\x0016/aëÚ±Â^\x001cKwùÂ\x000ey¡dõSPµ\x0010ªª¦(¾ÿýï¿úêK+Ë+ÖUì¼"¥8ë¦ÙÔ:\x000b\x0000\x001f|ðÁÖúöü½\x001a)¢µµµç{>¢É¤\x0006(òIæY\x0017A`òIéuÍ³\x000cÖÖA\x0010F£,fÙÙM§Sçìx<Nµ\x000eB(ËÒ1;k=òov\x000c \x0010ÑVµs\x0016ÇZ	xíúuÙ¢C\x0007«¹u¸ÆÀHb[Z\x0014@öâýxçÎ\x001d1ÁÖæf
xûÑÉ`@F'ín´§Ó,Ï³ÕÕ\x0015\x0000 EÎ2³kµápXåéééÑáï#ÞºuK©`mm-MÓ;wïLÿQ¶ÔïÿÖoÿöx<âhccý¹ëÏUU=\x001c\x000eÒ«+«+++yQ<xøðøøøåW\x001eÜ¿\x000f\x0000ÃÁÐ9»ºº:Nö÷¾øÅ/þÉw¾m­Es:\x0015¥$\x0019TUe\x0002ÓétÎ´®ªJ£\x000e5¹Ü\x0011;%ì+³<lÅç£buu¹\x0016~øèþÒújoi\x0005YLK+\x0007£Ñ$tñÆúú­øÎh4úÅ_üÅßÿ§ÿÔZyþùç6:§§§Ãá0CEêääd}sc<\x001e//-³HYa\x0018\x001e\x001fß-òÂ:§ÕE+nî)>c\x0017ÑËO?åf±+3ÿ\x0019ëô\x000eQhr\x0001oMZ?Õ\x0003¶k[L§ÓõõUç³îûßÿþññ±ÖaUU­0JZ-Ç6c\x000fÅ(ËÒ±ó\x0004w\x0000ÃÀ9\x000eIÍTs\x0005\x0011ÅIsðêbÊ9f\x0005@H\x001eiÇØ$ÖÚÁ`@
49?9=::Z^î_»~½×î\x001c\x001d\x001dEQ´¹±Qä9!fù´Óé¤íöùùÑ&0\x0001Í©Î[ö5§vôa]U<ó¯s\x0019DÒÚ1Ï£waÑZÕ\x0015³k,B5$\x001d\x000bÂO¤Kv)×û¹
3~ÆÇ\x0013\x0017Ö\x001f\x0017<eö¯ôÖà¤\x0014;väCaX)FD¯Þ\x0001ìD(pMo\x001båÏÅ@\x0000¤Ý\x0016'U]Ø¢[½Zè\x0017és¯½õÆö÷ÿ»ÿü÷þû\x0007Õ2Æí\x0003mÂR1IÜòÔ \x0008´RÐë'­\x0016	LµNÓ$[ÀR\x0018¢¨¶Ã0äºM
$é¤-_\x000fEð§S³
5\x0001!°Wë$jÒX`\x0006Z\x001e_\x0014åQ\x0016\x000bô8;­i§Øq+
é(\x0002esÉ¥³V\x0011ùòk\x0010<G\x0000h%Éd<6Æø\x0004Äg¶¶È¢IõºÝ\x001bÏ=ßï÷¿õ­o\x001d\x001e\x001dílï¨À(¢Édâc8níî>¼²µ³³±ó/ÿè_ìÝ¿ÿké\x000b{ýå½[w«ìóÒVçRQ¼Òb°\x001eC&*JæÉ<\x0013!ó¬-^ø.a\x0011`OÓ\x0014BËõÂû\x0008\x0005hÖ¶ö(·Ú¶¸jB\ X$G
Õ\x000c"Þl\x0001YPy±`±"à\x001c(Åu¤ùáÝo>X¿v£³q=Ôí\x0002WÙZ¼ô\x0006\x0000fð|DJkaVs\x0003Ò9\x000bvÆR\x0015D_y\x0013ðE*eÌ¢ÖÝ\5avn^\x0018ÉCphÁü«q%Zöy"=G\x0006\x0000çÐA	B¤\x000e÷\x000f\x0000`u}ÓhcY\x000eÊ²dçÄ5U\x000eß¬
C\x0002 \x0012Å" \x0000\x0011©¹\x0011o¯Ê\x0010\x0000Ä\x0000ãÑt¸º¾}t¼ûÆgÞ\x001a¾ë\x000e©Ð¡ýþ»w¦YýÆk¯DqèêÒ«¾°#$Ñ¤\x0000,£ xiÙgè½\x0000\x00018¶Ì\x000b²Ðlz\x0010ú1å\x001eG³S4ÚðÜt\x0016Ú®O¾Ù}X'þ\x0013\x0005ðmH\x0000µ8
ÀÃÁøæ\x0017¯]Ýyû·?óÖgAèý÷>\x0000ÑiÚ	\x000c!Vu¡4"Ç¢vÚöî0\x001aQ\x001a¢\x0007\4=Ì\x0002üC¤\x00105)da
È\x0008B¾PÔóÅ\x0001\x001d8í\x000eÏÚí6aÇ\x0000\x0004ØxOÁ\x0014ñ¯ÿ\x0005»F7Õfe\x0001À\x0012\x0000A¤M\x0001-Ë¦EQÜ¹sg<\x001e;ëºÝn\x001c\x0000Þ!Pù}Á"¥I\x0013³*JW\x0016nsãJUU4\x0019\x000e¾ûÝ÷®ìÜXî/u­P<"üCï\x000bR\x0001ED\x0010¨ëúätTÐi«þÒR\x0018$iÝ¼ùÂÎÎÎ+¯¼xûöíÉdòøð0\x000c
³óm¼(èþÃG''§Fë\x0017^|qmm½®ëÉtÒívÿè\x000fÿ0IÓV\x001coooM¦Ó$My2)nÜ¸±·»;\x0019=Ç±(££#f6Aà\x001bF\x001f×u½¹±±²²eÓÑhTUu\x001cÇÛ[Ûggg\x0000ðßù¥¥åôþÑ;ï¼Óëõ²²X<;ß\x0002¬*>;?|x\x0018Gã+W®mm_éwúG'Ól<:=CD¥Q!(e\x0000µØº\x0002^¯GZ\x001d\x001f\x001f;ëzíN]×JQ¿¿Ôn·µÖ^\x000bF)­7Ã¦º¶A\x0010´­íÞÞ^UUKK½V+úÜç>w÷îÝÁàÌZ»¶¶¶ºº\x001aEQçjww÷½÷ÞÛÝÝí÷\x0007Ãáõk×ëºö¾\x0000eYz}Í(£8ªªJ\x001bFg§§ãñtpv~\x0016 i%­V+£Ó³Ó,Ïµ2Ö"ýðá\x0003[×ËËË­¤E:N¯×Ï³|08ßÞÚÎóÒZk¢ÙæEqpp°sõº4 \x0007
L`^Z
"\x0016©«ÊeæË\x0008¡B\x0004¥´1Xøìüäñã=\x001fì¤\x0014·â°Óïl®¯\x000e\x0006§ì\+
VW×\x0001¨\x0015\x0005­VH\x0008TÛzö±
\x0017lòìÙéyé^¯d\x0011¿\x000fÎö¶¡\x0005}q[]¬}?
{ç±ºxvO\x0014Ó?¢Á¹`%K\x001a¢þgÿíî©£õà¹Éâü\x000b)åÓ§Ì\x0008\x0010ÄQðµ×^ûà÷\x001f<\x0018Ý:=?{åõ×ÖÖÖ(<==cº²µ³¨i<T{ë­Øq6ÍÆã'Çã^Ïõú½Ñd<fûû{Q\x0010\x001eìN76c\x0000\x0008Ãð_üâ¼Í àGoy>uÅñQ\x0017×a\x0006kzæ\x001b¾ûODW´\x0017òÄë.\x0004¼ø´EÑf\x0000`¯K\x0005^s^\x000ekB@7/YzY\x0016>ã{E\x00004ÒÚÕÙñÒ:fl]\x0012ÇI»ýÙ?÷¹ÚÚHk\x0000(¦S±\x0016Y\x0010­\x0013¸Äcx¦hÃ¢îÇ3ÐÂI»ù5DTMÄÂâÁ\x0008.8v¾×³øM \x0000"^euÆ´¾¸\x0017O\x001eÒ¢>ÃlÂ7m\x0017& XÇ\x0000 \x0000=<Ê?\x001d
aõò\x0014ò!¸*ÃågæLÖà\x00133çk8xæI"{\x0006¤\x0006@""ÿÞ\x000fÍÂ\x0002¨<ow¾¦\x0012\x0002øÂh`qÂÎ5z\x0008I\x0010wÃaç\x0000\x001cc«\x0000A\x0003\x0001\x000b8§j·\x0003]Ö®vöÞÛ²÷Á\x000f¾öÂ¨´ûËkë;W®,­®pmãvE&e	ÌÆ»\x0014*\x0014"'ÂB\x0011p];[;£4y¬\x0019¡X\x0006\x0002ôvµì÷\x000fR"|>\x00083K\x0012"\x0004°"¢´qÌJçZ-^Uañ°ÜÙý"Ebn8\x000c@
­Ë§Ó \x0008,\x0003gE\x0010Q+mEÈZ´ÜíHeë\x0007÷îÜ¹s«¿¼\x001aEQ·¿´¾¾Ùïõ{;Wíx T§
DPÙz£@>©Ã8B`\\x0010hbf\x0005ÞDÐãF=½U\x0000©qø\x0010\x0011\x0010%\x0017wnaûË
\x0001ðX\x0013³â¢5Â¼zÙçñ²È¢È\x0002»ùg¼8F\x0002\x0010H¤)\x001b\x0001û\x0007Hê¢\x000cãÖ\x000e\]v{K7nÜ8;==>>Þ{´çÓ£££££{úA¯ßOÄ\x0018Óív£(0\x0002¤uå#¡V(ç¹2¡sçºUU%¶\x001aOÆv\x000fVd¢Ð²
\x0002Mª:SD¨´Q$\x0008Ã³Áàto¯Õ¾Õëõ^~ù%\x0000h¥i\x0010µ@À,ÎÖµ«ª\x0012\x0000À`s\x0015Y\x0010\x0010Q	KóÜ2{=vþp\x000f\x0013lÇÅüsáÇ\x000fumý]ãã\x0007=OïG\x0000z^\x000eEY_p\x0016ê¡÷oF/\x0000ÊµZD\x0011D"ïÕ-Äù23\x000bhF\x0001-FDãÀºÚ\x001e×#\x001eç\x0014:GÎYç\x0017·3¥EÄ:Ç -\x0000ê0HM/nÅívRÕUåG\x000f³l<\x001c\x000e«ª:\x001b\x000c[IBVOÏÚ­4\x0008L\x0018F4n\x001b¥NNNC\x0013¬¬­N³â[ßúÎ×ò¯v[­íÍ­+W®¤ÝÎo¼\x0011÷;-ê\x000e\x001e[
²ªªã8
Ã\x0010\x0004\x001d;\x0011\x0017Ö@F\x0007 ZX\x0002eÂ\x0017n^ø\x001dÊÓ=Áa#Jï¼Zþl}¹¸wí\x00129}áaû¡\x0011"eõûÈµ«WÇã1"ÅI4ÚÊ¹´\x000cGÚÖ^:æ\x001fÿwÿxccÃÕ\x00178Ú«×®EQ<\x0018\x000c\x0000 IZY6õ
ý¥þþÞÞéÙYUUQ\x0014\x0019£\x001f>|XåÚÚZ¤\x0000ÐétÞÿ«W®\x001c<> RD4\x0018omm®¬¬¸ºÎ³\iE¤ÖªAh±0IQm­µNÅD
\x0008\x0008D¡(\x0010\x0012®5B\x0000±\x001e¼\x0013(T E\x0001:g\x001dJ`Î¹ZêuFGñpumiuuùÞþãJÄ\x0011-/¯ðù\x0010L\x0018Å©µ¢©ªJkÝëõò<¡ÆEM\x0010\x0018cVVV\x000e?ÿù?ûöí·¿ó^~ùêÕ«kkkÝn÷\x0017>ÿùwß}7\x000cÃµµµÇ\x000fß|ó­v;Í¦Óõõª®NNN'ÌYë¬}ñ\x0017¾ò¯þÕx<.byeåÚõÕ£££0\x000c"7A\x0010·Z¿ñ\x001b¿ñ\x001fýGÿQÄ"&Ét:ÕÆL³l0\x0018dY.ÂÖZäøø8Z(¬eæÂY£V\x0018ì\x001d\x001e=ý¹\x000fîÞ{xÿÁÍ/Çãº¬lÍ[ë\x001b§óÉhzíÊö{w¿õ­omnný\x000f_ùÊ+W¼ÂóóÏ?÷ëù×ßùþ÷ªªò~®&\x0008¦Óê¥\x0017_¼wïþd:õ7Ç¬·ýk°ß
BÎ±gb\x0011\x0011-\x0014\x001aÐáå¨\x0003?U ç,"![Ñ\x000b]&*óÿ»\x0014ê}_þó3¼©,¢0#Òè©Þ½áÇÿ\x0012­\x0014;wtttçÎ0\x000c«ªBÄ\x0017_|1\x000eâétúøàèàñÁ4Ë¼T&\x0000ôû«o¼þF\x0018À\x0004¤(NÓvÛË¡\x0013\x0011»fÇ¤\x0019}ÓYg´ñx$ïÏaè£Þád,BÎ1\x0003k­\x0001ððàà¤d­t¦µ­[­V]×ãñ8cAøâ\x0017¿X×õ×¾þõ>\x0000\x001c\x001f÷ú½N»ó\x0017þÂ_Ø?Ø_\x0001 iµZIëÁý\x0007s4!x¸[U\x0015UUq#KN"Ì,a\x0018aè!&Ä" \x0012°¨sß\x0018öµo.ëùs¡\x0014}XøÆb^ï?/ïöO«
=ñW\x001fÐ" ÐÏý#òo>ö	ó¬\x0012réë\x0010\x0015Cð^)^R^\x0016ZÚ¤UÍµÎY çíÈ)\x0000\x0010âº¶Zi`GÂNÄ9Vs!\x001cc\x0000*Y\x0010\x0003ûÙ\x001cÝØFSÈ\x0010*\x0003NF\x0000TU\x0013­£¿ý·ÿç¯~æ¥ÿðÿñ|ëñF\x000bE¶Æ^¯çzîúÕ(NÓ´'Â\WÎb`<2A/M¶67¡ÉwRDLZ­(\x0003¥£8
´2Úx|)\x0013¹o\x000e;Ë\x0000d\x001b\x0000%7KP^©åÂfh\x0011Ô¶p\x001bzÀ,%\x0001¥50k$[UQ§ÃÌq\x001cw»]\x0000ãØYö÷$\x0000,¡	Y\x0001FAè1\x0014$P×u¹Ðîä´
\x0000Ï?ÿ|\x0018G'ÇÕyÝîu\x0001À\x0000UÞéônßº\x001bàÆÕë»÷ïü\x0017ÿéwþ×ÿË¿qóÚsÕtO\x0006ZÕ\x001bkè
qdþ\x0010?[î.¥\x0014O\x0014üÂ5\x001b\x0017]1Owõ\x001by\x0004É\x000cL<_½xÖ
\x0010³\x0002âÀ\x001bû¨\x001aó\x001a°ÈV¤\x0016Î\x000b\x001c°RTøæ	øÌ\x0004¬ \x0008 \x0001 #Q"\x000e\x0003Àv¤\x0000 º\x001e
v\x001d°·â¸ßJ;¥Õu®ËÂ¡8d'dY,
\x00083¢B\x0014m?ÃªªpqW5\x00114ÑVJ\x0005\x0006\x0015\x0007ÿ-á\x001d3XHXe\x001cETÔ´ò©óë³×öh±\x0016ây?{\x0011\x0000 $wïÞÝÝüòË¯.ï\µÌÒ¥ýÂg\x0013D¤\x0015²!\x001d\x0003ae;ç`F\x0018@dÒ* t)\x0008¢e#ÔÎÚ<í/\x0005J\x000fÎN«º\x0018Më»G£Qö\x000b{³»Úb\Õ$4*\x0010\x0006àÊ÷P?ÐÔµ~l!ÀY\x000c×J"\x0002æ¦þù!LYmíÒdAò×O<ÿ\x001bí~Ø²é\x0005ÑõÁI\x0008\x0000Ykí¸Çq6\x0019í<w
	@¥yõ×\x001f=ztõÊ5\x0000ýÎÛo\x0003ÐÆÆ6\x00119Çh!Äº®Çãa\x0010èV\x0018c¥E\x0004\x0019Ù\x0007
\x001a¨ ¬­(B§\x0004ýöe*×ì(«\x0001\x001d[dR@aª¸Ì>¸wo­ßÙ^]BR\x0000LÌÌàyñ¾TI×s\x0001
Ã27\x0005%ä\x0005Á9\x000b"0\x000bÕ\x000c*\x0000`d\x0011ÑÊwý!\x000cbÈ(Ò\x0000¶mçgçg¸|í¹<Ë-[£µ&\x0005\x0000HJ\x0011!BmQ\x0004IÅçÃÉÎ\x001bQÜûþw¿;<øÎÛïÿù_øÜÖêJQÄ5\x0014íé(_[_c¶{{{ív\x001b@\x0018\x0010\x0014t\x0010³
\x0000\x0011ÖÖâ+W®//-­®.;æííÍÓßÿý;M&a\x0018NÆÃ,ÏË,ïv»J©÷ßÿ¹«× ðªø~?úÜç>g´ÙÝÝ­­N&ëë\x001b\x0000°¶¶¦î?xà3Ð¥ååÑh\x0014\x0006Q¦É$\x0008çþäääøøøåW^ÑÆìîî"©n·HÙtzrròðáÃ,ËêºÞ{÷Ý7þò_\x001a\x000e·nÝ:8<j¥)8fkmUU+++qÜrÖ\x0006&zõÕ×}7ñ\x000fþÙ?ÛZßNööö\x0015ÇÖ\x0018BP;K\x0000\x0008\x0008_zñåããÓßÿ'¿¿ñK[wî?ì´;§§gQ\x0014õ»^UõñÉa·Û½wïÞt:ýüç?\x001fÅ\x0011¢/¼H&\x001b\x001bÔW¾ò_~¹><<\x000cC³¿¿ÿ\x000b¿ð\x000bÉ$\x000cÃáp ¼èu»Nç¥\x0017_Y]]­ªª,ËÝÝýn·»´´´¾¶vïÁ#çl¤;;½»wo#b«DQ´ÿø±VD
'ÓQçý^¯ÛYN'ì¸, \x0008{½¥þR4\x001eL¦£íím$6:XZZETgçÃå¥¥\x0013Rát2fpE_»òÜ`0HÄ¹ T`\x0002\x0012ª®cf&" \x00193kÿ1ÆZgR\x0004Ëý^UU\x0014­./·Z)p\x0015ÄhØÛÐívÃ0\x0006\x0008Zal­¸\x001aêÚN'Ó0ji¨4Î(qO7Fõ¼\x0019ðÌª%ÿL\x0006¦Or×~¼Oøñ>\x0017­<O´\x0016?S\x0011ñBg\x0017gr \x000bGÂâ~ø.âÚ¤\x001dEÑÎöéþáãwß;==ÿÊ[ûì+Wâ´å\x0008ª,ª²¨ëÊ:A°ì²²¸óÁ­[·oÊúÑ¨Æãñ{?øA·ÛN³ÑÈV
C0ZeYWUQ\x0014^\x0004½b\x000bÒy÷­s¾ëlöDßlzð]L?:tøTHfsAß¸ \x0006çÏ'\x001f¡Ùñ,hV6¨Ï\x000e´Ò"bë:\x0008ÚÚó³³³ÓÓ¢È;ÎRimeU\x0011\x0011bUUu]û²©cV³\x001dn\x0006\x0017ú0öä³+=\x0017/¾|aFç§§\x00112ïS~ô=z¢/îÖF+E\x0015;F\x0000­'\x0004#¢\x0007^)\x0002@`i\x0007-vj?µsx\x0016¦Á£ æ\x000fé\x0002\x0018bAÞ\x0019È9µ«=Ì\x0002½8\x001fJ\x0007D­Í³<+\x000bf\x000eL\x0010·Bc44eV\x0000RÎÛw h\x0000ÃâØ\x0005\x0006§\x0004\x001cªW®m[\x0006\x0006¬mY\x001c\x001e\x000e\x0007Ý\x0007*^|ýÕr´Ø\x0011µ+ªºpuíÄú­&ÐÊídWUUÛ2Pa\x0014\x0004¤T)¥«j\x0011ñ\x001d»æÊ#\x0013 \x0001¢9i\x0000@)$ÿt(\x0003ù\x0012\x0017ê¢9­D±\x0008hPZIà\x001büà?Á9eæÂú\x001eµbDÔÆ\x0000B\x0010¥B\x0013Ä¡+\x001dOÇÃÁÙÙÑÁÁý[wÈè«×ÛØÜ´s­TW:Â´
&\x0004ç ®ªÒ:çRA\x0018B \x0000\x0000j[Ûª®\x001c\x0000h¥´1H",3têOd4³ÐÃT/È\x0010°\x0010ãúf­o¹-¡\x0008	aã?$\x000c DYy#h\x0010
É@\x0018¶\x0000@zkëW'^zu2\x001aìíí\x001c\x001eí\x001fì\x000fÎãá$¢"¯úKÝ´8\x0007a\x0010sYeÆ\x0000¥1ÚÖuî¤ªj¯ã¡\x0016ÀHhÂX+"MÌÎÙ\x0005\x001d;\x0016$¥rÕY5\x0019ïÜº½ºººsõÊÚÚZ»ÝET¨´NÛ-@
ÖÚº\x0016\x0011 \x0002ÖYæHa¨´\x0001\x0000©ë²,Y)E\x0006æô§3>µ\x0008	A.<tÈË\x0011 C!qì¨©e(\x0000 ë\x001c"8ç\x0008µN¬rÊ8å\x001c;¶Îcfß\x000c\x0000D0Õ\x000b\x0010QADDa\x0018'­¤¶§Ù´(é4ûã?ùFYÔyV:v\x001aµßÊÀ<¸weeå\x0017^Èóü|8\x0000\x0000EÔJÓÇgÇ{'Gï?¼·±¹yO®\¹²µµÕYé\x0005Ý`õú\x0015p¶f÷\x001fÜGTT\x0014\x0004¥³ÂBÚP\x001c¬ÃÂ¹óñ$\^iN\x001f\x0018\x0005pfêù\x0013\x001dÚb\x0000\x0000¢C¡\x0011	À=zô(NÒÀ\x0004	Æq\x0018§g§½´7{UÕÞ:Ô\x00183\x001aF£Ñññq§Ó¹²½ãõH©ÃããÉd:fA`F£Q]UÑy_»vÕCA¢\x0018'½n×Gb\x0014)£hnÎÊ,ìx¦Ãu]7èþ¶\x001c6Ändiè\x00058C\x0016ù\x0010\x0002A\x001cF`ZD\x001c[çS\x0000\x000e\x0014Ô¶VÆ\x0018cªÒR\x0014F­$+lÕ+ËkÓ,»ÿàÁ«¯¾
\x0000D
Ñ\x0001PYÆºªHkU\x0014§u^½zý;ßþöîîîË/¿´¶¶vzrrõÚÕ(VWÒ4ÍóÜo©Y{bkåé¤®íx<þÚ×¾6\x001aÒF£££ªª\x0014Q»Ý\x001eâ½½½VÄ­6J\x001b£\x0001p^W\x0019\x0000<e	<u\x0017\x0018YP\x001c
#;M`«Â9\x0017hEÀ¡2ÏÞùÎ·6··ÇãéÙhP×õúæv\x001cÇ^Eêk_ûÚ\x0017¾ð(jýÞïýÞkW_{íµ8n9æÛ·\x001f\x0004AàU^Ê²lµ×\x000fpÖjÕô¼}\x001d\x0010­ðb5O\x0007~´TáðÏDJ?ÞðxFéSê¡.ªª`:t:<eYe¿ß7A\x0010EÉõçûò\x001fþa\x0010\x0018$!¢,Ë\x001c;ÄfirÌÆh¥IDH\x00137Î\x001elÃ\x0000àØ\x00190ófüLD\x0004\x001d{QHðÕ¶0\x000c	
+³¤ï¼÷söÚµëady<\x001c9çÖ6Öoß¾çùÚÚZ+\x000e\x0001`k{;Ë¦gçç\x000f\x001f=Ê²©°$i:ÏS´V2\x0000PU\x0015·rVnæâYÚº¬óÚÏI\x000fã¿Xfµ\\x0015BçAJ³\x0016¼výOâXnÇ3\x0017\x001cù0B³§!h­½Þ\x00063;öR\x001a\x000cóÞ°0:`ÇÂZÄ9§t´\x0012B­@~¶Ðÿ\x001f=\x0018\x001aðµ÷ÒÃÆ\x0018bÿÎ¯ÿú¯.-õþoÿ÷ÿôëßz\x0018Få^÷\x000bE+6ÎZ\x0014\x0017&ã(\x0002¥XD+\x001d\x00046ºÝNh3CD¥u\x0010\x0018\x0005¤4j¥\x0014
08Ënè-Ü\x0014ãÆE-À/äÊ>A±@\x00115ò]c`i·ÛívÛ×²\x000bw\x0003çÖÚZËÌÆ\x0018afçT\x0010(hÔ_ñ²\x0007å\x000bÏß¸yóæ;wÞ}ï½"ËZ­ÄUu]×ì1ziy9\x001bg÷îß»²Þ{t÷Öÿñÿðù[ÿ«¿úòÍç¿ºÕR\x0002«\x00158@!ù!\x0016#â¬?êÂ0_ôfýV\x000f" hq4\x00102b][!\x0006`!òù\x001f	à¼¡
\x000cì\x0008,A%`	\x001db#:D^[\x000fA@\x0008\x0001\x0019\x0018X\x0008\x0002\x0007
QÄ@+PTÕùèâª\x000eÚ¹iç&ì ®v$¢Äy~*\x00010ò\x0018\x001d\x0016GDÒl @¤""¨|gW{k>c´Ñ\x000cÞÈ\x0015\x0005H\x0019£Ayx'(¥\x0014"ù~\x0006ÎÑ\x0017xáK= gÕô´\x0008P\x0000L "Ó¨lU?|ð°®]Úî\x00121Mc¬ù\x0010d\x0010"E5\x0008\x000b\x0011bí= ¬rç Ë#ÒqËq L]VS[Û²Æí®L¨¨ª³aMó·ßy÷Õ×^\ÙZ«OÓ¤
Ä\L<\x0002\x0004\x001a \x00002ÍÕ³.ñ
øÏ±Å±(ù\x000b0£¨6Nòì}E>mP\x0017Ò\x0000ï\x0002*®ªê:Ëm]k¥\x0014© Â0f¶×®^ÕJ½÷Þ\x0007ÃáY\x0010\x0018\x0008ã8\x0016\x0011Í\x001a\x0000\x0006ç\x0003étÖâ}ì|=Í5çÈ^\x0010÷\x0007b@$\x0004\x0002\x0007è\x0005,\x0019| %¤\x0014Yí\x0019@\x0003Rå|4nEA7\x000eI\x0019®\x0001EH@)\x0014@qÖy\x0019¨§|¹¨Ò8#Sù6/ª®ÒÚV\x001c{=
LÆãáp¸Ô_\x0002(¬sHó¥\x000b@\x0018¹)tQ\x001a%Â&ýõkEné·¿ývùÂ\x000bÏmliëª:sàÚíöh4b¶Ýn÷B¯xQ\x000e\x0010Q)µ²²òòK7vvv®?w#Ï²<ÖUõå/9Ï3­)m·¹ªê²,µ;;;×¯__]]uÎ\x0019Rq+ît:­V2\x001aúÝno©ßK@9fçìÆúzYI«å#ó 0íVGk}ÿþý£££ãããv»m­Íó|c}}{{;j%wïÞýÁ\x000f~pxøøèôLDRÎ¹N§?xxãÆßýÝßýïÿà?>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article8.659a695e.png](https://www.dossierfacile.fr/img/blog-article8.659a695e.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==åÝÏ©]ËÛÍËýÉõ6\x00033QQ²@-	õòh;¨T~ª¨V7ËEr1ë×w&R,@"Bæýn\x0007\x0000~?í­y¹÷Ø\x0000\x0000\x0001\x0001õ´P
¼
ME\x001dª12 ¨ºuûä~·s\x0003\x0010£/²§ã\x0011\x0011WÑgæ}:Çççãé\x0004\x00001,\x0012C±¿Ë²<?\x001fý\x0018³HÓ<l\x0000Z\x001b>.O!F\x000e¡%tUeYÄ/í¼:\x00077Øë1\x0011\x0012
1Æ
(«\x0003}E5\x0019DÀ5ß\x0010UâÂÚìÌ¦ê
\x0001kàÈe\x0016µ:éi}öõEÌk\x001a|¸'o\äÚ3ÖýpÎ"y´Ï§óéüË_þâp¸c&Õµú:]V\x0000\x0008ÿÿû?ÞOöö¿þÏ\x0019\x0004ÅL\x0010,\x0010ÅýÁG¯I}ë\x0004îï
ØÌr
\x0010\x001bÑØ\x0014\x00149Fr[ÏmÚÇ\x000bý*ZÓbRmÓzÖNbíyD¶£©[½ê\x0002è5Ö¸¾Q3Kie=_Ë¯ä!\x000e»»7oÞÜßÝy×t1Â­è@.B\x000c1úüî_å|:½7Ïóü|<>??N'+\x0016¡LWk\x0013©\x00193ç¤eI\x0000.Ï·jüUr^.Ö¶
Û\x0005\x0007]l¡¢Fj}Ç\x00189°ãwNDõ¼-p4³%-"ÊLC\x001cÆqÜívoß¾u
3ba¤:\x0000íü8)g"¦rÓ4Ceàö(ê8ù,"ùññq:Oí¶=Kæ9\x001c\x000eÁ±N3Ó\x001cqn\x0003£U6­4\x0002­²aZ\x000b\x0000W\x001dpDøY\x0015p;aß\x0013Ú\x001e\x0000[?,$ûJH©>§}\x0004ÙvqTyÓÐÈ#Xv\x0002½Ò¿¦"QÏÖËíz
\x0000po\x0019s¦\x000c)\x0003IUÈñ\Y»¥\x000b7g&Â\x0018\x0001àZÄ¨OâùlË\x0012b¼xpÙ
¿^M\x0003\x0000ÓtöB3Ï\x0016´ÊyÌ\x000cÕ	rÁ±Â.|÷dY\x0016¬<\x001fì\x0015½B`æ²K÷ãÙ7\x0001Jñ5`Î#§\x001d\x0005ÔLR+\x0015é\x0007\x000bAõ\x000eê\x0004 ¡nðÈ*#¢­5\x0002Ðu2é\x0007ÚÅq½ÿ/W×ËmíÅl\x0000\x0017d>ª|\x001b­·P^\x0019b£ý\x0013 .-r½A}å£õ?U³\x0015ôØZ\x0010ÔµRes\x0004BdB@5\x0017R\x0005¨Çfæ³?b\x0006$/TUï`åtÆc\x00006ÂZ¹lÌ%IÛg¨èµç\x001e gºX×ª&¡¿ö­Ú[\x0000\x0001E³#\x0010hfþèi0E¢Âi\x0012\x00135É)$)ê2\x0000°,©m87)Ã:eÙ¶Kÿôvüd\x0000?Y\x0013ü\x001d\x0017\x001d¸u×\x001fÖWÿ5Õ¿\x001c?Ýq!ª\x0003ÛTëVÀá¥KOËÙõB³¢pëÊ¿VÚr\x0001L\x0015ÐU}Û`Âî¿pñs+¨ï¤Z8o?øW­xÙo{Úþ`ÈXv6eÐ\x0003¨Õ©¾ÊpÕ»AªæZ°	//P¿>8ô"¾þ3>ö+§\x0017ÀE®\x0000¬-2&\x0011ÂÂ2îÁ\x0014nM2\x0019©\x0002s^	[5å\x001aü¿¦ù\x000b_I\x0001¸JL¬êgÎÖ¬H+\x0011hÃ£H]½ÊF¸åªn\x0004ÑzLAl/ùYtpî\x0008\x0018ëÕ£¨\x0002¢\x0019¸È\x0003°kH«¯nÁL¥Ø{Ô\x0006¼¼×gç}oÖ[sµ¯qmkÐ×ÏÁ­<MS%v#î²ÞµEÒJ|(Õá­Úo\x000c:Ôó\x0001pqMy2n"íÒ÷Í,R\x000eL\x001dU\x0013\x0001ÀºJyè*Æ
\x000fh\x0000åíù¥&f
1ª¨¶â¼¤oú@?\x000c±£¨BÕz¦ÚÐâÃÒHÖÞ	2zÙ±Y\x0017a×É+¼\x0001V¶v«:è»§ä©\x0010×²\x001eîÇ"Ãí\x0002\x0000Å\x0008Q\x000c\x0011ÙwyÌÀ¸åî4@\x0019"mð\x001bnû ®ý\x000c-gl»\x000f7\x0007,mT8%(\x0001`\x0018\x0007b.\x001a¤LMÝÅÌ\x0018XÕ¤\x0003\x0004¬ø²\x0000\x0002\x0012:(ÐÑS.\x0012@\x0004ÊX!ªm\x000f\x0011Ì0\x000eÀB^\x0011Ýz\x0011\x0002g!'<õòèr\Bs504b\x00177-BÕkMU¡r°Ú¾,\x0004N©ÂÌáþþîøüìãË%\x000eRÊÌÁÐMàMDÀ(Äª\x0006[emº7^·j\x0014(\x000e\x0003\x0003z£Ã§µNÂ_¢4ª3a\x0003\x0006¢æ\x0002·\x0013\x0000XæYEÚ¤/¬\x001c\x00009\x0000d¬5ë¥\x0019
,\x001a\x0018¢f"EA\x001c]\x0008¨	¡T$&
Èè2Mª\x0018ÉC\x0018âµÖßÈ\x0010ã8fv:ÝaÏZ£H)ðW%_«¬æ\x0005Õ$%A\x0014NÝ~çi:¦]²YURÊ\x000et\x0014\x001eª¯>-¯\P\x0002#b\x000c<\x0010\x0003\x0011!b&N\x0014\x000b\x0019Ëé|Î9IV7ýs\x0015J&v'Ày¿ýö[QIK"¦Ýnç\x0018WN)åì¹\x0004B\x000c1\x0014wA-¢\x0013\x001cD$pðmJ©\x000eã8\x000c¼ÿ\x001e\x0011÷ýc\x0016yxxð¡\x0017B\x0012/|?g'JÙû\x000cw#Â\x0000\x0010B\x0018â\x0000\x0000)§¦qá©Y5sÕÓ\x0010CGØ ´[T\x0018\x0011Q¼õrÎ
ßD\x0002ÐÀì.eOÝ¶ÛeÝñ1­H]r~>\x001e\x0001`·ÛiMêc
]ÚRÒô\x0015°²Ôßò(¥Ùß\x000bËì÷{q¨Ù%6\x0013=Ný~p\x001dÒaè·ü^"\x0012q\x001c\x0007j)@¬²6F&ZÕ3ÌÌ\>AçÅå]FÌ\x0015C\x0008\x0005äÌWi¢¥Ú\x001cÛ9¹dnªüÑÊà.0\x0008`¬tìr\x0003¢®9YÿT`+B«*YÖ	g3óÔ´¥svP³%-OOO®£ÕMÃXefÊ/CV5¢ÇÇÇ¸çÃ~?Æ!Ö\x00193'¯po=²m\x0012rU9a^õÛÌ~\x001e¸	Ç·\x0007v\x0005 
h¾\x0008\x0019©í=#×$`\x0000ÀÈ\j£ñRcÃ0xBÎyÉÅ¼U ¹½ÞÃÃÃýÝÝn¿kZN¾EïZïi³ÿÓñè¿\åx:9ÁÙ)½nçC\x0014\x00042¾n"Ö\x001djf¹&MjÑÚ\x000f¶\x0018t_
¥\x000eÍÃU\x000bÄËà\x0002aA\x0008(@ð1\x0007b!îvæÈÅ\x001308\x0004Y²¸[H4å4§§ç'/I\x0018\x0001b\x001cH5Ö>ï«ó4MOOOçóÙYííÕ·sWûàc£Y["	kâ¡Ú¡´ÍC_\x0005#\x0000³Oë+^_"Ot\x001bÆq\x001c[\x0019£ªdÁf1¸îj\x0010}F(wXa¦ÒTJ-ªð7C\x0005â=FQËj&SÊ^5\x0006pc#Ú¾µ>8"ª\x0001µ;! 
Ä¦f[å1\x0005Û±YæÊ¢"Åìó½$ª1Ü\x001d\x000bö­Ó\x0007|1[4Mçé<yÔè\x000eiY4ËÅµÖyêÚ\x0004ï&¢UÓÆ\x0007<çQÌp¤°~DÕ´¸úÔÔ_ª \x000c^\x0006Ó\x001bÑ\x000cÛ¢Ï·\x0007cQ8)>æò1Û¥îøË¥9þõkyÐ\x001fºø|¡\x001d!vâzíÈf\x0001B_ÐÌ?g`
FJ\x0000hd+òÂEîSËÊHÝLMeÉjPî¦FòT¥KK
÷\x0014îìÎ*Ç¹ìY=HÒ:c\x0003 )\x0008\x0018xMUÎ®\x000b¶Ì9x\x0012\x001a\x0010ÉE\x0003µ{Æ:ãm\x001a.þ­;Àk¯ýßaþrüµ\x001d\x001d:\x0004PÕTËQ\x0010±u¶lÒY\x001bËï\x0000Ôßt@ö\x000f8.è®=êWL½ªtïë9!\x000fâ\x0011Ñ·hµ\x000e·Û¹ÏÄU1bß&·ÚÌ\x0004»\x0012æ~ÒÀÎå%¥%ìT¡ÖD\x0016<amÁÚ+È­Q«p\x0010;ÈÏ·¦æÌ¯ï\x001fÊµ2=*á­l±c¢*Y j÷·ÞoÃµ>÷¥JéuÒô&Ë»\x0017Ú6¢\x000e'µÐQ·»!bR)w%\x001f« Â\x001fT¿rÑtÝ#ËEk´È\x001cn}\x001eèdý#]åN âÂT%AJg\x0015Y«ëX«E\x0000<VYà\x000b_\x0008nÍ-×ºè×¥ÛB7H\x0014\x001dñ¼ð\x0003¼¼«lãÆ´\x0001\x0000@\x0004«°\x0017"\x0006$«5J\x0005ë«\x0018ûÄ*uþ.ý~­ß\\ßLEÎ=ÂQré=jâÝ\x001fOÂn\x0008\x0013fH
®Á±\x000eáû#!PQ~ïzÞ\x000c-úß¸ÙZÕ\x00142\x0017éHQ\x0006]Y­m<¬`S\x0000PÔY4ÅÂáíríõ«\x0018;iYU420ÕBgîÏ¦}áTwDi\x00198"<1\x000ewµ\x0016yÛÿRþ"lfKÍe0\x0002P$7giîº~Ñý\x0010Kj\x0004\x0000þá\x001fþÁ-veQ³q\x001c\x0003ó0\x000cÙtg7¹\x001dqØ\x0003À4M©p·ÁyÁd\x001c\x0002Ç\x0018(Ã\x0002\x000cêH&\x000cTå\x0011´À\x0014ª\x0005Æ
39\x001e?Ä!\x000e·°K¾>\x001f\x0015ßÐæÏ\x0004EKE\x0015ª@HÂ\x001cch¤ÎÐþvôö\x0017U¨Õí1\x0004«»Î²¡\x000eìÏõðð0£{eÑnçÝ~IISÊá)9esN\x0010c$Éq&Â\x0010cÈ\x0019]îÙY®TÇ\x0008ÞíöË0­O1\x0008ÄÌq`\x000e¾è©BJi©GN\x0001àîþîo¾YåOú¨<<<Ü?Ü»¡U9Êóù|\x0000´ÃU/RJÇçcî­\x0017\x00026³dUm\x0003-ô\x0000\x000fÃà¥ÇXÔiEÖÓÓÓãã£dáÀ~òÃá\x0010Bp8{_EUósVQìÙß¼Å¾Tõx<~xÿ!KfÀ\x0018£\x0013Ô8ÇÇÇ´,w÷÷wC×E
°K\x0018yà!®\x001bpµ%ot}k¾R3s&æï¾û\x000e\x0000¥F¾PDà\x001a\x000b57¦sëfæ\x0015	f&ªó<§c\x0008îÐæ}æéùy&DÜïvq\x0018\¥Ø¿ë\x0003JT9¦|Xºªs¡*T\x0012À4DØØÍWÐ+Ëë|(9»|ªC!F×\x0018P³óùì¼Ì&\x0015°Ñ§}\x0019buu:¯\À@U:¸\x001bäh3sÅ\x0007Üàø\x0002­\x0010q}G×±+¢:Pd\x0002\x0018ýÆ¦i:Ïûý¾\x0006Ä5ÕÑpÿæ«»xÿýB\x0018G\x001eÂà\x0019ÍÊQ\x000fÜ¢à[3ÀN\x001c`\x000b¹*<\x0000´Â
h¥«e²ÜVWõñ1§T{
T7¨Ä\x001aD\x0012ºj\x0001×\x0002\x0018!ÇxàØÌ\x0002\x001cc
Ìq\x0018\x001e\x001e\x001eîïïB5f\x0014×ºÍ"dYëB´¨T5Ïó|&S\x0013ÉË§ãtD²¿L_~æ®f\x000c5±¹\x0015jØ\x000c¹ú³Y
Ø6s8bÓÏ[Ü:y\x0011ä²j\x0017)\x0018©
fÈ°@c@{¬fFÌaØïw»Ãáa\x0018â\x0010\x0007\x001f\x0006\x001eí¸Ò(T\x000c\x0017òõ%>§rÒª\x001aã\x0003×Ñ»AsJÏÇãÓÓÓù|j^·OØÈ\x0007¿Ô\x0001,,µ¾ôúÑñÖK_])Ò5¬,\x0000ËlQù§æyöqØ>ÏàSIZWz\x0003\x0000ÎÓmdh¬ÚMUC\x0010×¥ÿøÅtrY\x0007<¢K¼­bW\x0018\k;\x000b\x001d¼ËDuð)Éç\x0008¬ª;íns´]ý¹M¾Öº1\x0005º4*"ºÔ}ÿ\x001e«*ßV;\x0006VÁ\x0001Û üB\\x0004al\x0011"1¯ßV[O«!xëKt¥}ÙµXm¨WùËsSìW¿íÏPF¦«\x001e~ýî6\x0004O<ïÄÃÔ\x000c\x0004	íúzD\x0004Õ\x000cÙ1èíS\x0001Ú¦\x001a+]\x000cÉÐK\x0007j~Å"#@©#ò\x0004q-\x0014oÇÊ$q shï¦O\x000cp7'×m*1¡\x0014WzE3SlºíìôVì RJI4çì¿e
\x0005TYe¼¬PÓ@_êÀ?\x0002øãËñ¹Çffû\x0004ç\x0016CÞ<¯^rT×¸jÑÅ®
úkY\x0001Ýs\x001aÀ\x00003\x0013®JÉ°/\x00145÷µ¸\óú\x001eÛOf/
+mfqÜYï¶È²*ÀFÕw±vìÑ~\x0015 í7\x001e
-+u·\x001e}\x0014¢+bo÷Ýz]ÌË.ÑO.C\x0017Ý¿S¬µw	jDÅ«>ÀÎ>¾\x0010L Þºÿ<m,	å\x0017õ¸v*\x000f\x0012
Ó\x001cÑ/_ÿ.·\x0001	"\x0012hëú#²rÇév÷\x001e':¨\x0014½"vL°y«\x0011alCºH]5[¯z£6È{Î
¶¾ê´\x00075µJþ\x0014±2¾2¿ý·Îí»p\x0001Kµª8¦ë®ãi²5,@k C(ÅJ@X%	ë>±B°õÞp1vj}TÀY\x0008\x000eÝ\x0002\x00128\x0018AÁ7ND Ó\x001eë<ÐvD×}øúÕ\x0008Ù\x0017´îÿKÇþLÙ\x001cFÆ"÷\x000cäNß{ú½¯¯ÀÐáßjq´\x0018ÈÌ`Ã°Æ\x0010|ã®¾Úu\x000f¢úAÁu¨ÕÄ*`Úî¾¯N@´B6(`¿\x0000 ä\x001e\x0019ÐZ	Á&HÆFTùã\x000eÏ\x0016ÿL\x0005\x0004'U6WD3B·'\x0000ÚX Q\x0015GrXªôÿZ\x001fS&\x00193BØÅHÇÓiYr\x001c\x0002;ÿÁ0¤l@ki\x001d 6¢Ð}£ñ	\x0000Ø\x001dbÀ%-¦È\x000cªeu3ÓeY²d«ìWb\x001a!R\x0004,òÒõ\x0019¯ ¹fLäS(\x0003*æîÃÈT\x0016®ºê©"Uk\x0015º[FÊA$ß{qtÈÅ7ÝD<\x000cq·ß»gUy\x0013ÌHäø 1\x0003hãüñRý7[×\x0012ÍK2@
!D\x0006T\x0017e\x0001p(@\x001b©_D	m·{pÂµ@hC8\x0018c\x0004&&rZ²äÍ!a\x0018xg7::ÏÇã1-Ëù|¾¿»ÿå¯~éàÿx\x0018eIÜÑÊÔ8°\x0017<µ\x0010Èmê\ÅØESKóVÔ²¨p¤¼¤eç\x00103Ã ZPÎólb9ç\x0006âõÃÁëÚïîîz¸¿5amÎ)\x000bIKa5õ½9ù#bdö{p	Y6cæè[uç´ù0q|³.Ö
Í¿@ÞMÃ\x001b\x0013¹iÈ\Ü?FßûÃ«a®o\x0010Çã4M¢\x001aª\x0014»gÔÎÓ4Ï³k\x001f;`â]\x0004êUÜk´}±Îÿ%_ÕØo-èÝ>WkÁ¼EA\x000bÞØs\x0002\x0010\x0001Ào\x0019à]ëúÓöÐs´/\x00044¬«®\x0010É=7ÔÅ½\x001c6M×.ëêDeuÎûýÞqÐkô\x0019\x0000ÂW?ûz¸ûÙóïh7é<Ïó\x0005«¸\x0018UÈ\x0018«¥\x001b\x0016-í"QäÌèÖéýIDV®þM÷mÚ{v#¹Sÿ)º®!\x0004¹zO"â82s\x001dW]Ú\x0019:P@²¨ha·ßÝ\x001d\x000eoß~3\x000cÑmÓ\-Å­T ä¢KÆÃóY®\x000b±\x00147[ñtxN³·VQ¾/ÏîÆ¬½Ë_\x000b\x0017°Ö¸|VïÙ,\x000c¨M£o
â&\x001al5\x0012´N³\x000b°\x000fqð\x001a
·N\x000e1\x001eöûÝn\x0017CPÑÇó#Ô}Â\ºÄ®íLD\x000e×\x001eîîZÉÀÓtçå|:¹dLÓ'-ÚóÕ/Þ=\x001b\x001b÷SF\x0011Tø\x000f\x0011½B¤g\x0000mç\x001d/Åmåê\x001bñ~\x0018ô­+Rd°ÚLçòF\x0015r2¬zf9T'"Ø\x0012Tk]\x0012\x0000vÕjX§ò¡ñÑh~ÍõÕI\x000cTY½+SÛíwË¨fáBàFP\x001a¡¥³¼Ü£aÐ\x0017Ù0ÉùÜúvJþîÜ\x001d¢e\x0005þ¬s]_É\x0013ø×$·3\x0013_[\x0007XUf/9änwís×\x0019-.{\x0012U6Ñ*8àÓhI9¡C«N«pTU"¾®¬ÛlÀíÇ<½ß÷\x001fû\x001cäºMJèº9ëMÚÚù^\x00035\x0000Èµ½à|ziE\x000f|\x0014\x0015N¸J\x000f¼þHúÉ«¶}½ÊPÿE334t2H÷\x0019\¿\x0006\x0000A+­ó0z)ÿ\x0000\x0000\x0001	P\x0010\x0000Ùã\x0018\x0010i\x0008\x0015\x000f#\x0014\x0003%jµExÉÜíêóÞÎ\x001b\x0001ønÁ\x0000YM\x0015<@D'µ,KJ©ÊnhÑTUÅFæöÝÍ\x000fHJ|Jwm\x0003\x0007®:çãËñor\÷C¯!é\x0006©ø¯\x000cÜ@¢ÍðEsC]¿	}áG(àÅ
IûÂ´ÆëÝTSÓØæ\x0018MòPùrSÓ*vä\x0006\x0000Ù6¡ëg< êªÙ¶`+ÓAÜ\x0018ê§<é^÷Øg¤µN«×ª.Ð9\x0005D|iyi>_Óu Åä3^t+I¹â5÷\x001fS\x0015Ðôe¿\"«"°Pðå= °\x0003@àp\x0001â÷m	(á	÷ðP=
Õ$\x0014ÐÙµ\x0013ëI6É}
vkýÍÖ®Û¯¦¼×ÞÐwÔ×'ùf¾±ù-S\x000b>
=¯1ÕßÀE\x000bpoP"~Øq­ÝÿÉ¶>%é\x0013ÔPS«\x0018."\x0012®Ùå^öd\x0006#p rý\x0015\x0005\x001cEç]X~îê«­êääÉi\x000f'×ËUÕSjI5R»I¾ yxFçº­
 âKaÉëËýÍ~Õ¾Ò®h\x0015î_©\x001e´~]T#\x0007\x0000hZ¥.d»½íÞU-\x0012Õú)B\x0014\x0015DP\x0006ÐWé\x001eßëe\x00035C@E2ìòme×â-\x0008\x0000¹F:¤&yNçó³r`/\x0004m3$]ö\x0013\x0002Ð\x0010½\x000bqÝ'\x001a:\x0010\6æ2¡+wÛr\x0000
1 F¤=\x0011bÎ)Æ²±JË"DÈlUÞÔ7¤ÌìØC\x0003`ÉÔRÊNS\x0015\x0018 §\x0004èõ¬.5P\x0018QªêX
!eÍY2\x0000\x000c<\x0018\x0006\x001e\x0000Us*Å\x0000p:Í,§¤f\µ\x0005ÌlIKN!DgùÔå\x000fã08ô.ØÑ\x0017n\x0013$Ì]ËÜHÍ\x0002\x0007\x0007(U\x0004D¼Ï·>¶,Ëóóó8î/§"×\x0004º;\x001c\x001e\x001eîÇSÎiYRJ	L;ç'\x00040\x0003Ë¢°(ÀàjP5­òüÚç+ÌE9©µ¡éÏ\x001bb\x0000¢!Æ$E\x000c\x0001\x0002Ã8Ë²\x000cÃ 9ïö;\x0015M9Oç÷ïÞïö»q\x001c\x001fÞ<üò\x0017¿üÍ?þfçwïßyH0MS\x000cqØo\x000c`Í°\x0012¹ü=6Éæ¶\x0018¹2IØ¦IUw»\x001d3§¸\x0011CcN\x0017Ûï÷÷w÷\x0000ðþÝ{_:cÎù5³q\x001cýÇ£\x0011¯UÜ\x0008-pC\x0004`a¿ß;Ún")çé|çCøùÏ>ã<Ï¿ÿÝïBã8:Ñ8¤eYD\x001dÄNù}1\x0000üíH\x0005\x0010é\x000fø\x0003\x0000ø\x0015©#5WFßEvªL¤ê
?©\x0018Á\x0011ýa`"ÉyYÒ4MQUrvÝçÝnÇD)¹ðú1ÆEþ¼,Ë8ýÞÌ<\x001fàå\x0002¥§ÅÖµíB(*Éåéê\x0008J\x000eVÞ¡·¹¿Gïü9_\x0018¸-D¤ÊU\x0013¦äUÄÍÊ ú2so®\x0006\x0000H\x0014*Ñ[Ì¤j8ðéÍåf\x0007MU\x0003\x0000¨HQ«åÒmDÔÚ¼\x0014¸\x0004GWWDÄÞÈÃ0\x000cû!Æèo\x000c:\x0008.Ñ?þÿaü\x001511F\x0011@4É¢&LDa%#;	º­\x0010
hnjë¥áÈ\x0017Ðs\x000f@·¯øp\x0005tDÌ9§j¹hf^)àpçRËö\x0014¼8%O@ÝßÝß½¹wö\x0018ÝÝ\x001eZ^®d¶Ë=4Nè0Äeçãó§ç§ãñä~¬>õo\x0016rtQ³«á\x0004~óö¾ÚT\L´òÜ«s\x0002\x0000R3£°fqP/±Aà.êõs\x00078ÒªÌbæÔ\x001ejàTdPe=speÀ1ò\x0010wß}÷Ý~\x0008CÇãs\x0013¾\x0001åééy¾?N)çh\x0006+mÖç\x0005ñÊ"ÏOO\x0000ðÏøC\x001f\õµ¼kä1Ñ~¨\ÚM@³ÝtU¦_í'Íç½z-l?Ù½¦\x001a\nmLn1n\x001a¤vÃ·Çç¦gofþê{ìÛÌ\CÊc\ÇC»	buÁF]HÞ"ð	\x0015Öv&fS¢Pp±\x000eU°ß¿{wï¸s@T\x0015'³;~¸»sXTsJ5«à$Õ\x0004RKQdÝ7)\x0013\x0011â<ÏXõ¦ËS\x0010*9´:çb\x0013÷ Ð¥tå\x0010"&Ù8´\x0012óÝáPmQqïJ"ª®/`xãeaUôæqö\x001a÷£t\x0001´Ç°åØ
:W|&ì\x001c<.ÑçkõÒu\x0014lü$Ý%\x0012Â\x001a\x0010oùVý\x001bï·©`s\x0006aqªÙ^½\x000fèû3õMp
,ö£C?\x0019VþÑUw­²àÛ¿û?iu×ío*µ\x0018¶#±$PÍ Rd&F`vª#2¬ÛøÈØÝcalèõðoM1Yn-\x001bX\x0000 ®¤Ê\x0005Ù×äGSvmt#\x0001ÌYÒ²hÉW@ÎI\x0004Ä·Øðæ\x000br·¿²
B¼Ü°þ¹\x001fûýhÇKºÏ½¦ùO,IýWw|ºMö¿Îñ
ÌôyÏõ&¾U9©î/P9êfc÷?(u²\x000eUy\x00127\x000e]è5
âÔ¬¤à­N®A\x0014M­ÍE²/T\x0017ø ÏÿV\x0018¿\x0000PD¢×ìeûÜú_\x00027[Ý0­44ÓmÜru\x001e\x0015~½²MÛ&w"7ÂÚp×³}Ó_ö\x0015\x001e\x0004\x0002F­õ$: y\x0017»obwÂþ¿^iíwåMÔ\x0016Ç\x0016ÀvëA«ê7ÿ%×"K/4å\x0003$G¢[ÏQTâÂåìRÅ½\x001cÊª

\x000eBL "Ñ\x0001Ð\x00177Üv.u÷¥¢ÕrÍVKd:0Ôðwë*äZ×RÏ}\x0014*AóþÙÄÛV´Â¡Òß]½ÍBÇ>V°Æü}Ñ¢1c\x0010ÅnÇ-U÷\x0019\x00006Öy\x000eúM ï+Gp¡X}ûº½\x0003\x0004¾Ð3=\x001eR\¶J¡ìû\x000fÝP*\x000b¸\x000bG\x0016SvB\x0006:q@
ÌÐ}ö\x0000À\x000c	ÀÊ¾	ú¼¶BÝ v×
 93"×÷hf-º]\x0015q½=40Q@§"Kôú¶ºö	ÀLk\x0010Ë1DÕ¤U\x0010Õ\êtN\x0010¬?\x0015µ¦T\x0017¥©ÔøNñc\x0015h.\x001d©ÛmµdUkç
ä½ÞðµRMAÔË¾õáz¶×ñîµ®Å?Y\*¡8ÆSq^u\x0013F@Rë;qd²@\x0008\x0010Ú
;Bí\x001bÓ.\x0008\x0000@Ø\x000cY\x0003	\x001ap¡0!B\x0012S t+î\x0011Bºe0B\x000c¬êJnfVCÊÛ+¥k\x0006v<2QJ\x0002Xõ\x001f\x0000\x0002!fSUC2.b©j¤k\x00125¦\x0010ãÀ\x001câíRÏDsvWíÈ;\x0000ã9¹\x0010±\x001eQ \x0005DeÉypìÛM\x0005a`\x0006ó4©(\x0002\x0004"\x0006\x001cÆqÈY$¥I2\x001b\x0019¯=í¶²¤FM®;¹¹hGú\x0011¯ È"\x0000D\x0003=\x001fº¶\x0013"\x000b&¸¢éóÓÓán/976\x001b$\x0018Î\x0019\x0018tÎ\x0000¦óôæÍo¿ýöÍ7¢®@JªúîýûyçÓy)8	!1
1\x0002D¼,Ûe1QÊIk¿R\x0000üË_ýêë}óþýûãyÎÓÙ\x0000q$\x0008\x001cø|:ó¹ì|c\x0000æ\x0010Æ\x0010ÍìÿÿïS{ÕÁ_\x0017þî»ïv»Ýo~óRNiCCá}\x001e\x000e§§'W¬Þãf¦§óÉ)LDfz\x0012ýÍ7"r>\\x0010y\x0018\x0006fæÀ®\x0013s¾»»ûðá\x0003\x0011¹EáïþéwMüÊÌ$K¼ß;F\x001c8àq\x001cC\x0008ÓyJËâ\x0018¨hêt>?=?WT¤+\x0018êe@Nël}Ãª\x0007æ~¿\x000fÆz\x0019\x0000Þ¾}{:$Å*À\x0001	E\x0004uÆ(ÙGfCr.rçZE3`\x001c£SøYu:\x001eO£[ åÌ!83OTç9íwÑ¿\x001eC\x000cù_ì÷ûÓéôôôÔ¦)­K´Òÿ½[$9®DQ½¹GDfVu7\x0000\x0002äp(Ä¼ÌÇì\x0011ÏÜ¯çù|ÆyÚÜ\x0002C\x0002¼\x0000Ý®®Ê»ªî\x0007537÷ÈÊÆ\x001b$ÛI)dgFøÅÜ.jK®Õ\x0012!FªEáíóÍÞ#sÎD¬Z8æZ½+Û¿3T½\x0015U¬LÙ°A\x001f"Òö±ýüéè³×Ñªg\x0017ÐMËTÉ°\x000e\x0000jÉ\x000b\x001a""°·{\x0013.Ô<6p"Ý\x0002v\x000b\x0010\x0002£¶%\x0000ÉLO§ã<Ïfúþý\x0017LÓ
Z\x000c/Ç£ßIJ	\x0003\x000fq\x0017¢e¾d)®TArï\x0007("®þ]QU­Þu°_T®õJ¬N%VåÆ\x001aÞí¨8\x0001ÙÏéÃo¿ß\x0017W4"D~÷î]\x0008ÁË\x0007a\x0018v»q\x001cým	,q}oð
LSÑ®Íùt<\x001eO'÷\x0012µbÇÇÄÜØÙ]ð­Íc×a\x000bg¹ÚªðJ¡&®ûiº\ýV°ûÊz¬ºT+ \x0012\x0018)ym×°\x0000\x0000\x0014óT&"êw9Uúa\x0008aTÕóùÄ!0M\x000eDº{l\x0016q7B0r¶¿Ëc-Q¤**/ª)g&¯#È"{½©Ø>HÍ¦ºÙ ,ÁÁç\x000fÏ7·Î]Áö»×pö:c\x000f°\x00058\\x0012¼?ùj]_k\x001fº5t\x000c\x0011É\x000b\x001bÜ\x0012§ÓçÊÂÞÞÏÛÐçÒa\M¯*1õ
'\x0000À\x001cv»è*ÉD\x001cZWðÿ-jYó÷ßp%\x0019w\x000eÌ)åZ©P\x0011l»¾Ïí±®EÀ6¢½>@$Cj³ÏpÔÀ@%¤,o\x001fË¶ÐïÜññÀìý\x0019<É{8<øWæ|À¶p¯\x0003¼þ,î` ýaÍ÷»6"BÒAV«¥nCÏKøF\x00154³»«Ï·ûY^wÏÊïÄ\x0004¶.¬Ã7\x001eovîá<Áí»jªÍ[ë
$½@aVU½f4×B!ª\x00019F\x001cKÍ\x00176½R4 \x001aÜwU¯\x001d=\x0006]ë!ìÅõw6¥eUÉ\x0005BÅMGÉ\x0014gIºR2hfYKË°P&áó¼Ê½µß`(¦ÿÅ\x0010ß\x001fÿw\x000ft\x0018íæ±¤±\x001dí\x0004TÆYÒRäDÀKÁrãÐ!\x0000\x0010\x000022©¨f0r"Å\x0010Çq$¦r[â[yuc]\x000cêÂ}]ÛbÅ®æ4Dl¶fpÅsl']×·µ¨»^ÅV©ývi&@$ÅÕâÒî¿S»êI$\x000eäÕÙKØÕ}nU¡OÁØ:\x0015,
Ýâ\x001a,»×Ôí®z¾óµÊvõ\x000f$ÛQÁ=\x0012Ãf=231SÑ\i\x0016ua*¢ä\x001b{Ú$\x0005\x0016¯·E
¶Ú£^\x0017êö\x000f*\x000b¯5¸B\x0016¿õ}8ØªòöÕ\x0003àÛ"\x0008UmÛ×Ï~¸~æõ X¨Òi¯Sþ\x001eµë¶qMÄh
´Ô.Ðz,oÞ;-#kÅ/f\x0004"KrÅ	\x0001Ë=à"\x0017ÝH\x000cDL\x001d¹Á7ù.°\x000b]ÿ¼ÙN×öçõôùr'*Ù#vêä)\x0010·"\x0019%¿²\x0017º¿íb\x0008&ÛÊÖaÚozè¹.áv6Ï5\x0014Æ\x000cË
\x0014k\x001e@B6îßÅ\x001bz\x0011A\x0011Y
¶Xë\x0010E\x0004\x0014ª©lwó-çîj+Sèfë\x0002ÎÈÖN¶^¹°(~·õE»Ò.*J\x0014bÌÁµ^\x0000JVT½¿µ\x0002bD¢²QàÇÝèÈo|Ì\x000c2 
\x0000ràÀ\x0003\x0000LÓäurË\x0014C|x<\x000cÃ\x0013r DÌTUU±À,ÕÄ$(Ì¸ÛíCàrÎ9\x0007º\.)e|¹]\x0001\x0010Ýn\x0018¢7ZÜC\x0016D¤÷zìzôv³\x0015éÐig\x00156])ðHWHý7ý×ÿüÏÿâ	f¬U\x0014V}æ÷ûý_|òüÛû7(\x0019\x0011EÄiRDrî²Ï
8ÄápxpÈ/ä\x0005Ü8£äìüB\x0000!\x000eq!º\x0004ëñxúý\x00170\x0012C`\x00155²nuãû×}9\x001d\x001d®¦É\x0010\\x001a×u0DÅ\x0011ªæ^FHNqî¶\x0014¹Hi&r9çÒn·\x001bâR¦yçOôÉ]þÆq4S¯\x0017?Î\x0000àJÍ>Ñ1ÑOúSÇsÎÎ\x0006×èHy¦Óù¬ª%9\x000eñ°ß#bÊéùÓó÷ßïñÏ\x0017_|±ßíþýõ×Þ½ÙØNN\x000fÃáá!rº\.çÓÙya®\x001cí&±æº¸DRÕ\x001dô$f\x0011ñÝz\x0011\&L)].ra¿ß»
ã<'oRêL;Í,p0³8Äòùt®¯¸Èq !ÙÂ> w´
Á­ç9!áa<¸\x001e±;ë@)kv×(½\ÎÄ¼ÛíJêÆ¥rNçó8Ã\x0010cÌEN§³¡\x000f\x0003TÖ¹£×jÆf¦ExBC,_\x00049¥i$ç\x0010£»©åR\x0002ìb\x0017-\x0011É&\x001aCØ\x001d\x000e!pS~®\x0006\x0000\x0000UÆ\x001eÇ©$i\'¤ð»]c:\x0004ïr®­áÈ¾'4;7Yå\x0005ý¯ÅîûÚ}ìãÀ:"´-OP=\x000eTÙÐ&Y\x0004Äßì§OÃ»wï!ö¾\x0017!§4\x000f\x0014âD&*ªc\x000eÄàäCO@
¤ÜÐéÉùâ·¬ÌM\x000fWLG\x0007ìÃÍî\x0002YJÕÿ¥ê\x0019Ø$ÏÇqô	Úë\x0005\x0002\x0007w\x000bEfDLsÊY²Ë7{Ðèkä§ùt>{×tÏ@>\\x0008<ðB[å1Ü\x0018A\x0003yÌ}\x001a§\x0013\x0007(¶ª÷	¥®®-ê­µ!®µ|¤.«-åKP\x0001\ä¡	ê/®Ù4Mf\x0016\x0002K}³ÄÅC|3fj=(é\x0012Øþ\x0015Ç.ÐD\x000f»¯\x001fö:¦·[@È½Í@
PVÑ\x0012!]ëÈü ã\x001eä}/\x001eRUO5·o\x0011H\x001e!þÎ¿Ü\x0000}Îyæú½@i\x0018b\x000c±E\x0000@\x00131w9
­5\x000ehjSüE»÷ãårñ²\x001aI±:ÆB]G¿D\x0000k¼ï\x000c×/·½ J7J·´ú¶av1æ~Ù÷\x001e|4\x0004b\x001e\x0010=%D\x000e¶\x0004u³9«Q¼ö-bV3b¢\x001a÷íÍ\x000fÐ`Ê¶iê
Æ)e%\x0005\÷¥=K«z4_ZØèVâÊª°`nIôïOïl\x0005ÿxHú³Ç+\x001bìW¾Â!\x0010,¹ÆñM©Ü³Q¥mÁS\x001d\x000b\x0000
\x0000\x00011\x0004æ²YòÝ;\x0004/\x0019\x0015\x0002­¸o"à[\x0000°µ&Ï9©¡\x0002Ð³d\x0013P\x0015È¦"`¨¦¦,¾TCÝJ)Ôº_·~¿ùÊüÞxz\x0006qey\x0011ñ«\x000fEKÅÉÇÇê¸W#²`\x0008ØuÍJLtÍ¢ºÜ5è°ìðÕº!RU&\U£\x00022-¹Èî%/\x001dw¦RÁêµ;*SB*\x0013ËÍcIZ	|o¬\x0007²÷úàöæÙt½^K
ôóù+i¤\x0019ó\x0016¤îÁ#?ZÁS»\x0010T ¦$Þð!\x0004\x0011¥+Í(êl\x001co¾\7Q\x000ejß¬û\x0000@aÛÎ\x001e\x001f¶|õ\x000fZ^ÿp½S5Ç£Üvõ\x000c´"Ð±lÃôþT\x0015h+)p3[¼ÒKôª&ÿ±È\x0017!®ÐuÅB5\x0000\x0000\x000e$ª`+1q/ü2³UÜÐîJ¥éËlÁã\x0019½ØöXÕçÚ=\x0017ïªfñú\x0015ÿñÇö<´R9ï\x0005\x0016ü\x0007©pam\x001bÔ©\x000bfºb"¯R;´9sók¡\x000e;F,q)Vu\x000fèöAÄVÞ\x0010l\x000cÌÖöéËù	uYË\x0017¦6 ºnu:Ë­AÊØ¯Ï"¥cz\x0019\x0015-énL_±fê\x0000\jouòµèÇÒ*B±å\x001eia?3SS"$Z)¬\x001bâ6«R3sÑ¤¦dè	½\x0010Ü\x0000ð¶I¸?±\x0013'±2»\x001d\x000e u­Ê\x0002è,Ê\x0011\x000b¦\x000fP*D$\x0006«*Ùj\x0000¨%ëj:\x001b`­éq25#\x0017ÜÌs{\x0015KB\x00000f%¶\x0010(\x0018»°¨2\x0003\x0011\x0011\x0007²dÕTÚ\x001c37UþY
\x0014\x00014K¶&íÙ\x0007òÙ/F\x0002 ´æt¥!\x0014\x0012·ë:Z\x0014b`æJÆ\x0014\x0000H9¥yÎ)«I°pa\x0019\x0017ÀÑrÖI\x001cÁ¤Z·Ä@f\x0005Ì
¼\x0005U[ùõ£Yç\x0016\x0002j\x001cÓéäa<"2\x0019\x0011\x0001©f\x000exØï¿úÉþy×møÕ¯~5Ï³31ùË_\x001e\x001eösº8.Fñ¶-BÎRwÂ>Ý\x0011Q¼\.ö	C\x0008N4)CLæóù²?\x000e°HÞ";\x0011Ng7JÃM*úòüÂ\x001f\x000e\x000fã8xÙïæ³×ñ§bïvû,Ù£2Tw»Ýn·{8<ìv»ù×9N\x000eÍ\x0005\x000eÄäº%iN^ì÷vx8<<<ì/óéäCÆüáÃôDe¿ßçª=ðîË/?}ú4Ïéð\x0000Ä¤^ÎóåÌ·ÚË!;§`f5ÓyöG¦\x0019\x0000\x001e\x001e\x000e\x0011\x000b{×çç\x0018c\x0008!¨®\x0012­z9_æ4CÎMkA:\x0012\x0008\x0000\x000eè©*	\x0001#¼ÌS\x0016\x0015Ç¸²\x0008WI\jþ\x001a]þ"¥YÄYz>mÕ¼\x000bº
\x0007\x0011ù=«<§ä\x0008$\x0000,\x001csUQe)_mÞÎY\x001càv4\x0003\x0011sJNôÌ"R\x000f]áä|>C\x0017¼\x0011\x0011!ÅaðGs«5¨
\x0013>6c\x0008
ë\x00081ºêKN)\x0003p(:à(bªÄ|8\x001cÌì|>O'pÙ\x0010°jynÒ\x0019¨ÝâH×qf8[\x000b`Üè\x00031îb0ÓËåâª\x0012íO"ùÓ§O-m\x00005!\x001aÎËÃîÉbLJZä\x0005Á	7¸\x000ce*\x000f¡Ïóô\x001fp!\x0012[«4\x0018´Ç >:\x0016Õ2HìüððàWñþç\x001e ã82±Ua\x0018\x0010XTÒDE×é¨oùU4»ßv.x«ªÎs©[Q\x0015Í¢"\x001c\x000bõå5F¶Ûîµûïö\x0012^T´pksñ[9_Ý3\{qôÿÒu>¿ü\x0016çY\x0000p^³Ëð«f{j>eç-\x0017y#$D]ê×<ý\x0018\x00111ÆàÊSµ" ôH\x0017f5àØoZ]½W\x0004Ïþ­Í/_±~Þ|·bÅÛñõ}Ýë³Y\x0017-+Nª¬v¡í©ë\x0007@\x0014s\x0016¢\(ÏZÔeCóoäö\x0014®>»îQÐ8ÈlÞ\x001f>³\x000cÃà\x001a»ýÎÓ\x0003!ðn·GÄy½zÈµ5æ4»
Õ4Í¥²Ãìr¹ôH±s\x001fÂºXêðÜV½eýgèpªFóoO\x0007kMá¾·s`êl|T\x0015´ºYÚårfv\x0000ºí\\x0003Ç\x0001\x0018êm÷w^Â\x001a­x:\x0001¶MÂÝàöÛ¯Aý\x000cV¿æç,\x000f%Y©Q¹t¯?^\x000b¡2Ë¨+o¼y!µõÍÂÄ_1nVßíÞÔÐ£ímÙ÷F1\x0004bdå\x0006@\x0003\x0000\x0017y\x0019/M©Å»H\x0018kåB©6Õ6ú\x0008\x0014¡l¢u\x000eQ¸ã'¶Ú\x0013VÖÏ\x001bN©\^JQï1×Ô\x00063\x000c\x0000êÂ\x001bÙÝ[\x0001ET\x0000TÌÐÍaL\x0005+¡\x001b¨¢ÖZë\x0003×÷¦,ÿÃ\x001fô\x001f¸\x0017ÿxüÐC=cÔ\x0003¯>zò\x0003U\x0015\x000eT³ª}±\x0004Wuv
\x0018á«\x000c)3sØºêÁ3 zÊª\x0005\x0015\x0000p¾\Ò<sXf^xT«Æ¨\x001f\x0015 ÝBcV\jõ:>YB'/ù¾ã]±9Þâ5¶o12¬O]Ô+q\x00054×sºwtû=3\x0005$-Ö\x000e¥_JY(µ0µGØoÎQèmEÝÂºÑ¯mÅ9)¥úº\x0016t7îp¹\x00013×\x0019¼f¯eKç¬¡¬¶wW{ÚòN\x0001À\x0014\x001b\x000bûÞKáÀ½¼um»ùå±K\x0008
MrÊLAë\x001b¬û\x000e,9QDD/Xæ.Ý¤Á CÕ<ñ¦(Ü¢^Ä¼<]\x0001MmKà @ ½Â û£±>í\x0007®>k£­\x0010Gÿ²l\x001dv¾áÌ\x001dAÁ}\x0000ëBï$+-­ÿ°l§WçÔ\x001eÚ.ß\x0015YXðÌÈ@KKíäÔÏ	ÕgQÕÌÌQ!Ï77çºÚÏt'.ED l\x000eyTmº6;n¨¤¹ ¬e ½êÖè¯\x000eÎ|·{\x0019(Tam,Û .gÖ¡eX¾Û=Ú½|Fà&wHnÑÙ\x001fôÕ;4³\x000cÙY[ºÚÎÜøV·Kª\x001aÐPö#\x000eªû\x0007Æ1¨\x0006UÍR\x0010\x0003\x0018\x0011!\x0018ù\x0012\x0013\x0018ý9Ðea±høY`CP\x0015ÑÌ¥³R\x000cDn\x001d5ã\x0000ª
jCd9ÕfI\x0004 À¬d9'Äj"b0PD3Ð§"DÁ4cç4«\x0014\x0007Â UÏ\x000b!\x001e\x000e\x000f1\x00063R3\x0014\x0014É9e§Uz\x0017c©­ÙfyGØ¡ÇÑô¶P_·¶cAÓ4ýÿÿñ\x001fa àµt\x0012Æ\x0010(§ô»¯¿~zzx÷îÝét23Í\x0012"\x0006B§Ç©êþ°;\x001cö\x000f\x000fÌ\x0014B\x000cúÓ\x001c'D$:ûí·OOO»Ý>g\x0011Q?H~~~~~~V\x0018¢Wt{çï«\x000fèðþ=\x000fQEâ8<==)Â0\x000c$?>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/blog-article.50da4d3d.png](https://www.dossierfacile.fr/img/blog-article.50da4d3d.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=xï\x0001¨µòå_þÇÿð\x001f¥5sÄì\x0018
ÄLTÅ@\x0005HAå|O9[\x0016\x000c\x0000*²rðÿ\mýÏ?MÄýô.Ù»h\x001c\x0016 %Qê\x001c\x0003Ì­°	és\x0000
\x0008Æ
ÐÄã\x0002rjå4ÛÆÎ»ýãÓÅjóúÅkXäfwùÑë\x0008¹Ì\x000b\x0003>Þ=~ý¯n^¼@ÄÍfõ¯ÿÕ¿º¿¿ýí¯¯\x001f÷!n}1l¶w·\x000f«\x001fýâê£«aíñp·xz|ú¡NAµ\x000fÁ«NÇ.tD `Ð1ÔZõñaÊË÷w_üÕ_^¾|õÕû[ËÍÕõí·¯Þ|´ÃÝ\x000f·\x001f½~ý\x001fÿÃ¿ÿÿü_ïß¿wHm/×ýÃéi9\x0014ÕB Çy\x001aSHJd"ÒïFÌÀ@ãiZí®À»¬mwy9åÉGçñÝ÷ßI\x0001\x0001\x000cj3ÔÖ®.¶( ½>¥Í7\x0003­¼.æk+Ò\x0004­M§ãñ8:}ö³Ãþñï¾ÿî»oþâ/þâgò³Úêßý0çeHÎH±Ò´Uó!b\x0018Ü×\x001f?\x001d\x000e9gBìúMeoNÐ#AE­&KÓáð»ß}ùË_þ¹§\x0004\x001cà|R\x000fÇlÄiuõoþ×ÿ³4éºáïõå´\x0014\x000csÉ7mqRZ#&©kÑÚ|\x00134¬hÖZðÌÁ;ÄZÅS\x0000\x0011B£óõKÙRs>\x0019\x001fè-D6È9\x000e@K©gþ7\x0000H\x0013mMJ/6uÚäñ8wk\x0015\x0003\x0002E>÷RÔà;\x0004hM2C<U]Þ}ÿ]ÆÎ­Rð\x0011\x0019ZkVEj-k¤Â:¸Uç»ÈæÐyrÑcÍ¥ÌKóéz7ÏóqÚs\x0002ôhf]3UCç¹ 2´íæâº[\x0013°\x0012£ghºÝÝáAëÜ¡"sÔ÷È-ób\x000c=#""7À\x0016»\x001aúàúåõ\x0005/÷ºÔà8\x00030E+Â\x0000sk>S\x0014©\x0015%òÓñÔ¯W­5\x000f8tÝ\x0012""èZ\x001a÷>u©?\x001c\x000eó<Aè×ëKÀ\x0018\x001ds]]àTEàlH<c¥Ïl+DB\x0014Z\x0010ðüª?ÛKr®fXJ&Òôx\x001cC\x0008ÞÅRË\x0019zsv`-Q¤\x0006¬&çÚHL¬\x0018´¦Y\x0015Î\x001c|\x0005µèz9ÏR
\x0019\x0008	C.uç4\pôC±K(Ö\x001cú¾ÛzæÇ§ã»÷\x000fUå8N\x0006îÅ«Oæ:;î½CGÍ\x0004Ø!ä\x0002ÑÍ9\x000bÂ8Ï¥µÀäÖ¶ï¾Ù÷?ûÙ\x0010û»»Û!ºÍÕÅþpèBw\x001a\x000b"o6»ãñHFÏO/?þ,¥Pó¢Æ\x000c\x0010¢cGy)¥´uJ&@\x0000*Z[nÎ{VªÒ¤:ögó\x0014\x00015l@DEÌT\x0008Km
ÈÁs\x000c¨\x00001FEÚ\x0000½'Ä\x0018c\x0008\x0001\x0011s"Àä\x0000Sêºn¥µ\x0017(¥\x0019ÂÒÚÐá²L="\x001b'pNGôÃ\x0010 ÎL­÷N¢¦,\x0006ì]ð="#rê:À©j	Þ¶Vë8çq,UZÕ"R²V¾¢¦U4¥\x0001ÐûØÅ©,ÍØ\x0011/y1t]ÂÖ\x00004ç<äcf
àÄ\x0010\x000c\x0001\x0010@IQX¤\x0011Ñ°Þì\x000fÓí»·¬Ôz:3°ï\x0016%\x001e®·M\x0001[\x0003\f1"Ð±5U((YZ!tvkç §Z°\x0019ÉËüîë¯Ó§P®u®)\x000e\x0006zµZA-Í¦YS\x0004EpÎ	Âóá$\x0002\x0017WÛqDs´Ô²T\¯\x0007b8åb>Å.ÅZ[Ö"\x001f­·»¾cSC
CæÓX÷Ç9­V««+&\x0012ç¦­Ö\x001eI¦9ç\jÍ9ê<ÏÃjk!çBÎ{r±gËt÷÷çÏñs0×2ÌÇóüxx~ÿ«?l6«ËnX\x000fÝÀ®E\x0008ì½*\x0013¨s\x0016\x001c§.8\x0002"ÒVûàHU\x0014©\x0001r\x0013u1 ZS«býf!n/v¯>z£§)÷}<×*Z+\x000f\x0001É\x001183É9°g\x0000\x0018O§Ý°&Q\x0002-\x0017hª¹1°#\x000fò1(¥0{B6Bç}«d­VæÀÈ¦\x0016}\x0018RgØ
\x0013\x0002 èÙå*9gæH*gÅ\x0004!\x0000,­b+\x0000Æ]ìÌCÉ@\x0008@µ\x0019û8ç\x0012R,µ]^ß¼ÿ~³Ù,Ó|}ýâÝÛw»ãPs»¾¼Ç£Onÿ´ïR'5k\x001d\x001fo÷OÏstìÈôåÍVC¹¹\x0018\x001cÂx<ÔYË<MÇ©å¦j`æÀ±\x000f¥\x00145ZUå!ß¹x<\x001eO&Â}Lf\x0006eacï$ëtè5j²ÔÅ b$\x0003\x0000Wë4\x001e¾úo'\ï^~ñã|"\x0017æé @Óé\x0014}8>=m¾¨\x0010q\x0013QP\x0017W8\x001ds-1vàp*RÍúÕÆ§ØT³\x00001.¹\x001cN#{\x001f»\x0004LÃáã?nj÷ã¤@¥ÃÖuz.\x0015\x0008EôÜ00Ã3»ÒõýÄssÎ«õêåËèÃz38$"Ïe9!Y\x0008îê
Ú7ß\x0012a\x000eC\x0018Ø1¹\x0010»nXÆqÓõ©K1­¼ó¥Õ~\x0018(&www¶&ï\x001f\x0001\x0000®./ö{æXkÜª¨aLéâÂs\x0004¬Hysï~ü>\x0006zyµ1.Ë\x0014£Éûê¾øôsYæè\x0003;fâÃóãjnnneùò7¿\x000eÎswwwç ðÕf»&5ãMÇÕ\x0000QDç¦i"8ó\x0019êÚ{3\x000f:\x0004ç=«Ô\x0018»\x000c ­¶¦.¦Òäùx¸¸¸a¸¿ìûÕ¿ø1Óÿñ_þ&Ï9ÆV£\x001aßþ \x0002
ÖL
Ì\x0014T\x000cÏ#\x00050\x0004\x0002úc6ë\x0005À¹ÿÏ&\x0000*?5ù\x0014\x0008?*Òjýò£|üj¾ÿqüÛ©ÍÍÔ@\x0004XÉM\x000e¢R?äi´èpgïý×ß|÷ñÇo.vW1/¾øìý»o¿þækD7Nó4êû÷o.>??=\x001fìÏþìOOc\x0019Ö\x0017Æáý»»7¯^ýòó6½ûý¯\x001eß½ËOûÐ`ã\x000c%WPt´hFø FÎ\x0013B+Uõàpøò?ý§þåýâ³Ïÿñ8Ý?\x001dþüßý÷\x000f÷÷Ï?ÿì³ãñxÿþÝ¿úþôúå_þ\x001a@Á¤ë£ÚÇ(\x0008#±µ¶ÌL\x0008¨Í9Ð¹àãf5\x0014©ã4n¯/þ§?\x0003§ÇÇ©LãIJGz±ÝB^<¸³ó\x000c ¥´ëíE§eW»\x000bhS@}sµÚæÖò4Ï*P²2ÓÕîòêêúýÝí\x001f¾þ¶²\x001eõº7]ÏãÉ;dç\x0008¸.Ë4\x001a[¹»{\x000fä¢÷»õI\x000c*(*K&E-ÕoÜ²ß?=Þ¿ÿê»Á
¹Òûû\x0007r||z\x0005¾úúÇqþøÏúú!:`t)ÆÎw=8'H¥ÉæârØ¬ûaXrmMÅÐ3!i3e\x0011$\jiRsÍgô\x0019½RJ9·<Ë¸`@Q©*D$\x0008f 5«Yè\x0011¼wDä\x001cC2ÇÑ\x0014¤jË]¸4S#j&*å¬\x0015?ßSÙamÚÊ$5\x0007Ô4¬7«þP¼#F±¼dizV\x0003bË\x00064t)Ìb \x0008^[ó\x000c M\x0004Uµï{Q\x001a¶\x0017îèÆñdP¤Y©ÈÌÄµe\x0000ðäÞ}÷C=M¸è|<9ã2f8tÑûÃódhy:\x001a*[]R;\x001f \x0016\x0013u\x0004°ä\ÅÈ÷­©ãÀT[Y$OU \x0000y'}\9BäD\x000c¥\x0014&n\x0015<cJç\x000fêéx$eY.©äÀ\x001cÚ¤qÓ
R\x0006Æ\x0011O©ï»RïØRY?pêQUEUUå'r%ü3¸óYt<gÎÀùà?·î¼÷`àØ}`AªÔZ©µ\x0006$µ0:c\x0011\x0011\x0000T\x0013DB@ï¨¶\x0006MÔó\x001cSÍ@u&\x00153"\x001fâ\\x0016$Ï>-YDT\x001av}}}\x0018§Ýfµ?\x001e6cÞl6S^¦ý~wyqx>-yöÎ¡,¥Õª}MDÍL\x001a²\x0007Öª§DeñÎ\x000e÷y¦Óáùtüo\x000f\x000f×ëíóó³9zº­§i.ã\x0018Ù¿ûñû~è¡V\x00076Än<<çåÊP³ùt ¹Zû§e7Ý`ª>x0
)Æt\x000eu©Dì\x0011\x001c\x0013W\x0011U=8\x0010\x0008%WòÄÌllU\x0008AÍj)|¾àÊ¹
0ÎÓq\x001c##" ¢÷|vnÎósîûa½^7ÓõfN9Ïoß½]0ÕÖu1F/ËÒÄ\x0018!%\x0016«¥ò\x0019Ëkä8\x0010ñ2çm\x0017\x0011¹ï×ãirlMA
*ãYò)%bb"sçH
¨¹=¶äJ%ç,
bà\t\x000e§éÈX=,É%fÿ¡ø3&\x000eÍ\x0008\x001d1*BC£*Í4ç¬\x0002.º,u§S­\x0005hòjwñ<N¹6\x0012ëWÃTÈ»Æ$MQ%87tÞ\x0011ãBº¹ÞuÎé<·e%[[b7üøöû3Ù-¹ËÍ:!\x0008ófÒó¥4Ø÷i·]?>`
  
  
  
  
Instances: 7
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?==õ}ÿñãcÒÜÅ®ëº\x0010ÙK\x001dÀEÕËûPÕ·~³\x001fY\x0001+\x001dàg\x0000ì¤\x0006¡Z\x001b÷WÜ¶4ð`\x001cc\x000cû¾ÿúõ«\x0003®îásírÔ[zèv­i¡ó8$k)«èÍ3}Ë;\x001eA[e\x001c84ì6¿v\x0003cho¸:OèdÌNà~³¸g·ý\x000bXW\x0003ÉÈÍ\x000e/zp¬ýr\x0000\x0019a(®"\x0004¡ïhJ3\x0000\x00089Í\x001bÞ!CÏ\x001d³£\x0003´ üÈ@M	Ï	TÍ±­×e¾)§ñ:«ªøÿTÄ ÷Ç­"R\x0008NYEÌ]ÇÌ¡ë:f</p><p>¡GDÉyLÉ\x000cä<«</p><p>k\x0004;`{\x001d·
ÓÈvÞ\x0002È2í<\x0017Û0ýµì»ïíiß\x0000S¹ÃÍï|ß6B¼7|WÞEßÝ`Äñ>\x001d÷\x000eÀ®8Tó²m\ê\x0003\x0018ÃÛ´ó>Ü\b½_kk0Vå´\x0019ÃþX¯»s¡|¹¡ÄVõ¨à¾U]\x000fm­H\x0013þ£LÎÆAÝþÍî\x0016eÃÍBÖd	BÈ\x0011¹®w\x0006ÚDP\x0016§E\x0011\x001e\x001eÎ-\x0013aè'^Å´\x001b"Å`¨I\x0013\x0002*"rÀ­K¶\x±táfzï;T\x0018½Â_ëîÛ"'ßØJé\x001e\x0008\x0003z c¦i\x00000ÆÐÅ.ppÞ3¯ò ,A/ßqïÇµB\x000fºã"\x0004DÎ\x0012èÎ+\x0007Xà $)eG©</p><p>s`\x000e¦Ikm_ÛVùeÛf-ª,UVÑd¿c þ¤¶dxú_»;ÿ£}£\x001d9cÿ^[[ûÄ^µSv</p><p>¥®!,áÿ¾ïÍ,%q\x0014ÆîÙZú\x0001oßÜëu\x0015\x0002/\7Ë¯\x0010QT\x0019\x0010?<~@Db O\x0006\x001aUÕ.F
\x0017RJÙë=ÙËËåéé©?õçóùüÐ÷ýÃÃ9~\x0008ló<sW¾&R¾É\x0000¨Ãá&-¹´²¼\x0003\x0002ª§\x0018\x0018XU²­®\x000bâÑyÁÔ¦<9Ýó\x000f)%\x0011ÙT'ÞµvÏåMðw]g\x0002³\x0003¥ÖBõ^vú\x000f%R¤%ý­\x0016Ú¥öÆ\x0007¸=uý\<¿m¼¿¦E\x0010@7\x000f\x000f1å\x0004\x00001DvA\x0007õÔOX\x001dN@Dd.Á~Ï-\x0010¡§¨V\x0006g`·vZ\x000c_ßÖA\x0001\x000c\x0005Lr¢\x0010 ø|\x0000ÛÝ:\x0014È âõ\x0015D4\x000ber§§'Iiç9çRJ³e%¦yÎ\x000e8CDnÆC@ìC`Dêûb9åÉ½\x0002f\x001a¯3\x0011eS3Í5PGª¹ÉL5£Å¶¶\x000frµ\x0003õ\x0008.¶\x000fvËò&\x0001ÎÝoÈ§¶\x0013:·"V</p><p>Ð;È7FÌzÛÔVï¼=c³´5¦%ê\Q"²ùÓz¹7l\x001eï4KV\x000cÒÝ\x001f¶ïÔ~
@+@vÀ</p><p>U~(°÷\ÜmH[Iù]_¢õ ´9Ú~ÄÑhßa8Ê\x0000(®\x000e\x0000¯SRAm\x000bó[~ÛB,q¸K<zJ¦õ×\x000c«Ñi\x0010ú\x0010{æ.ÙËõ\x001a»\x000e\x0000¦y\x001aÏç!Ïçt¹\x0004$TAd5ËªGõ^DJu\x0003víT[7cr¦c  ¢åÚ\x0001UÀ\x0015£_ðl\x001aÔ\x000c\x0017BÏrg)M)å8beû_dÒÑØ3À÷g"cs)8DC*7±{³"È1ø\x000ejMù Ty2JýifD fºn<Zû»ô>7@5ï\x000cÑ</p><p>Ø\x0004´ijã4næ1Üÿ
\x000e2]úZ</p><p>p£íò\x0016\x0008ÐÍyà{¤¤\x001drçü¿Ô¦Í;!@¨µÛÎ:Î:·íø|»?h¯<¯ÝÏ\x0010»¿®\x0007\x000fìÝ(£ïÒZfOErZ\x0013\x00138î\rÎ"ªÒ÷½ê¬ià\Î'r2µlJ"ûÛß¬­ù\t×Ý@3\x0000\x0011%âa\x0008ªÛõÜ$tÝà±Ýç§ñzIÃ0<?]ÏçóÃÃ\x00033#¡¨òíÛ½!á`F3'´}E(}ëäû¾kÔÚ0\x001b¨$Cø(çä»®\x001bÇÑ^Ömðå(¸à;\x00023ß¼°9ó²oj\x0015b\x0000p¢!ï!|;È\x001b<Ê\x0003\x0006¦\x001aCtR\x001açq\x0012É\x001eÛö5³y3\x0012\x0011p`¯o\x0000¡ïÓ<3\x0004@0Ë~L\x0017»1Í\x0005¦¹­ÀL\x0018c0³yNÃÐyÌ¼fcì\x00101Pà®ëÌÌ\x001151¤BnW{ ®/1Æ¬êxÙ6Ò\x0012Sà@D\x0011TdNs \x001eÇi\x001cÇóåùùz¹^¯W5Ýg\x0008\x000b\x0006Å\x0010GÈÌ1î4Ä\x0018\x0003\x0011úÖâûªÎ"]ò\x00073%1Â1¥4ç\x0013"ªh65\x0005\x0011S,JË#&\x0003Ün»oóý\x0006\x001cÕðdoïf\x000bk\x000c¾£â×\x0016zñ^ÀPn8M·8ïý\x0015t2c@&BZÁÖ7KêM\x001a}A\x0001YÃW
«±[aÌçÀ¾Ã³ÉNT>c51ªÞ\x0016ÛqÚ}Fw\x0000¹VdcMYÖù#¢ÚÒònÁo\x0014S\x0003TÉ²\x001ePd\x0016)\x0005£±)HºñFvã\x0013wEÏ;}Ðæ<Ñif¡é3¿E|mC\x000fz4\x000f[×¶¨Ý#\x0011\x0000\x0000Y\x0010c×å\x0014çoféìr¹ÄÐ+\x0018Q8N¤ÉáY\x0001Q	\x0010£1L34ÑçeaU«CÑVçY\x000bZÊ\x0010$·EÞê\x0013Æ\x000be83ûZ\x0001ª,ª\x0004\x0016\x0002g3\x0011\x0011\x0005\x0005àÐSr/ç4<|þú%çd\x0000AM²Ót\x000b\x0001 ,BÂ¼s{È\[@tÂ\x0010ò,D\x0005>¹ô?lxñYÍTÌÌ¹Ø=\x0006ªMBÈª&jbÆ\x0001H\x0014kA?\x001dÁupÉê¨¿</p><p>¨FÄ¬\x0006d¨Ï¸\x0011öZÃbíú°Á¬\x0001\x0011ð'cÒÎ[\x0003°\x00036#Ò\x0014\x000cÊ\x001e×º\x0013³ì\x0017¯\x001f	Æ\x001eþÕPÖ÷ö&G\x0002@!²\x0005óÉJH\x0006(*åºq\x0012¾éoû|Tô\x0004ñÒÚ)¸]rÞçxÜ\x0011Y¯ÁÝÒI50ªÓ<·\x0019ï
¯ÈÆ¢l>\x00062\x0000{ÊÚë¯¼ØòpÎr-DûH[&ú·Øëá\x001b~¼­Ñ*ø9p{\x000c7&Êó\x001cBdÀátff\x0011I)\x0001AnÆ¡u\x001eLö3±oy\\x0014\x0018Ð\x0010\x0001ÐTäáá\x000cÕ,\x0010\x0018@\x0008\x001d\x0013ÇÇ.DêûÞ)\PXÄæyFET(\x0016\x00061ÂU D\x0011LË]òÞjÒçñåú|}êN§Óé±ï\x0018§ivÒ\x000b0ò-ýfÎ´7æ\x0017l,uç%33E­mF\x0001yqR\x0016&R³4Ï\x0018C©Õ¬R²ÖnC6\x000cuÛ9ÐÖD\x001d\x000c´/M\x000cÜÂ&c_è%nf,ß"úè2óëµ_µ\x0019ò\x0016\x0001\x001aiN70&5s96A©ÒK´Ò<f\x0011\x000eDDª@\x000c$ªçóY^½æýÚDÔ\x000f\x0011\x0000T,Æè *üÿ1÷okãÈ(f\x0007\x0000¤{dfUw¯½õé^\x0017ºÔÓè\x0001ôÞ>´5{zuwUD¸\x0004ÌL\x0017\x0006 33²»Ö\x001aqfj¢#=è$\x0008\x0002vø\x000f¢À½EB ÆÁõ°N\x0011*u<îës\x0005	\x0003\x0005SÛòÖo-\x0010! \x001bäüþ~ÓRe¹ÝÞ·-/·Ûr_<E&âÐk$Ôzª¬m`¢\x0014b!¦df×\x0017Ó</p><p>\x0004zX4ûké·èý~33\x0007®\x00188/XT ñ8?È¥oúvvRµ:ûy\\¦izúqUþ\x000c¦ög¡ï§IË}\x001f\x0013\x0003ç\x0000ò\x000eE\x001b»}\x001eî1Öðò\x0004æÊKªÇ¡ÚÿG\x000e­ÒþóH¼\x001b¥Z¼×É!OÇêgÆC`³ªÞ\x000b½þ,F\x000e1<\x000bÄÛÇ\x0014\x0000Ü~µERÃµ)\x0004\x0014Çñ\x0017ÕÀLÄH('ðsÀ/\x0002>\x0003;ÂÃò4úWÈ\x0018t	Ãó/ ^;Ðf#ï_×Ï:MS%cÅ¨ MRKÙJÙÜüÛ\x0010T`-+ªL¸\x0008"r</p><p>Tý¿DÁÒ<¡õú¨{ð\x001e¯¬µô x\x0013øT]¤R¡\x0008\x0011÷Ò¨WUÔÀ\x0008*\x0003¢\x0001\x0003"\x0011\x0001yÔµk·eYJ\x0011DS\x0000DUí Òp|Q»¢¹\x0014³F\x000eöT\x0019\x0008í»áJ¥\x0007\x000cp;£À¬¨¢ê§òõ\x001aB²~3EÇvv\x0018~f²Æe«¾\x0011\x0011aÛ\x0001ýëc2Ð\x0006ðx¹cèGLOÉÖ*Ï¥ÏûôÏ×ÞÑ¼òð~ÉY%ï¹H¹
	þCñù\x0012Ýk®øV1É'\x001eoýÇ	üÙ;ø´ÒÏ?K£5|î\x000fS-¿>tÎÏ3\x0019èñ÷\x0008Ö¨ú'\x0002æ¯Kó\x000f'­Øêºþ?ãRÐ\x0011QÖÕ·°Jò\x0011Y×ÕËðPûÌß\x0019çÞÚ¢+yzG9Ô\x0012°ïË¸®¥\x0008:\x0008\x0011=\x00010C\x0014\x0014køqîUN\x0013\x0010\x0002ÅPÁÀ.\x0019\x000c\x0010c@DÊê÷Ûm)÷i®RâÀ¢j[i±Ùa\x001aW§ú|\x0001Zq°\x0005@\x0015ùb\x0004ª\x0008må\x000eF}\x0000ÝÜ=Æx_×áä»ÇBò/¾Ñ\x001aù'\x001c\x0003$æÐ\x0016\x0000\x001càCG\x0019Ðªÿ#º#±Ì%Ä{mÏëQ\x0000!0>½\x0010»I\x0007!ª÷I¸6[u¼êIuEvÆ\x0018\x0011qÛr`1v\x0019¸"ÅÌÒ<×=K-¦È\x0003\x00073\x00130\x0011aff1ö\x0016
÷\x0013ÕÔ½x\x0013\x0007\x0011ÙÖU¼¾¾s.EÊíö\x0016DµäÌ5\x000b\x0000¤\x0014Í\x000e</p><p>Ö)%§GGÌ!0»X\x0015´ð±¨ "!;éDkÛÁ§uUXWs]?\x0000ðh\x0003\x0000{û\x000fbþà8\x000b^á\x0013ì¸a]íYëêè3ð¼\x0003 ãf PÊcÛ~?\x0003[\x001a»\x0016lHx\x0008È³ì|\x000fý\x000f-þOùYPPÿ\x001d*ÝWç~m]rw¬</p><p>\x000cEÌ°$¨µÎ'µCoµ?\x0000Ö0\x0000W'(9,¸cõ7\x000fxúqÓ8\x0004<ª|mÇÑÄä9Ôç,@\x0019\x001bTuúôªDCg\x0012\x0012\x0003'ÆÌëz/&Ì\x0001@K)T\x0004<ð\x00054% "\x001a§)¥\x0006¨R¤(\x0003j\x0011ËªæÀ µÂÛ&LÙX³ûîödh`ÃT\x0014'þ\x0018(£6\x0001Ñë\x0018¦Z5:ÕdZT\x000842BL\x0002\x0007ïO·gáVô#¤ª#\x0012au_!sü\x000f\x0013 zÁº~/ù6d-$òûhæ>@õg£¡z^»Ï{¥\x0019]Ø \x001b©\x000eª#J`mYQC\x0004bxÈGÆaOå_\x000f	\x000f\x000e\x001d\x0000ð4&Âs3ær"ó:rZÎäùöôè»ÓWã_þëy\x0010ÌAÉXÿ'\x000eGv:?ò'÷õ\x0003ny\x0012XçÛÍ[¨õ®zØ>Â\x001bÇñ\x001e!ã\x0011Fß!@0£C\x0014DffUjmp!õó\x001f6ÅÝÎí§~}<Æ\x0011!p\x0005pDSSBS0C×ZäZ6©­Ëïêýó¢ÞÂT\x00051\x0008Ì\x0014b\x0016Í§\x0010\x0015A\x0015\x000ci	Ê\x0005\x0015\x001aoÁ
j¸=X{þ@m\x001cç\x000b´\x000bmß>R</p><p>ÞyV3)z%o%¦Tcü®ÜeÇ\x0004À\x000e	À¸ÿ:A\x000c: Ýß¾õ¶~c)
\x0012Ã}Û\x0013\x0000_nÇh­@÷ãxã\x000f<<\x0007 ^Ll!xÿÀX¤\x0008½ÖÚ,«\x0018\x0011ª¡KÜ\x00101sà\x0018\x0000ÀÿgÞ6D$6 çyËÙã\x0010£OÙ¶©\x0007ÊÄDXJ© W"+Êa""g©÷^uà êNY¶m[´èi_-ñ\x0012ª\x0015qWrÄEmÛ·í¾,þ_\x0010-¶4"ny\x0015à¥@cú²é2óÄ)&\x000e!¥X±þ]¨{Ärô²Cc\x0010wµJ¥´7jÁ\x0010\x000bÎólfªh¦</p><p>Jæ°\x000f,òä½Óãâõ\x0019þ\x0003Tã¤r£\x0000k\x000cào~£öù¿®| â<®Z¥ôÈ\x001f\x000bÿgpKk\x0007\x001dª\[î\x0012\x000f</p><p>KC®ÛÎ
è¬ðüñéz&sy¶m\x001bíê(ã'SJ¦s¶V¤\x0001\x0000@u\x0005áña`Fïá?½ß5#!s DÑçÆæêì*¢bêßµ®k7¾\x0018\x0003ñå¾ìç?¨ìãv\x0019\x0001\x0002¡"H\x0007üº\x001ft¨{.79Îs:!¦{¿µýa×héz\x0015Ó¥\x0018#!ÊVÞïïðåËåÛ·o1\x0004\x0000¼</p><p> ®\x00199 0cå\x0002Á\x0005\x0002!ª³\x0016	H¥\x0014d*E		Z37/ëÇ+~Z;«þ:,ÞÌÀ|n·¸ë;(zµ\x000c}\x00177\x0015/º\x0008\x0010w6\x0014! ¦ÌA¥ÚrÌÄÐßñ®ÆÍ»WIÃ`CË
\x0017H\x000fw¦¾\x0015·ºí	aAmòg²'~öQ\x0014Î\x0014Ù{\x0018Ì
Uµïòf\x000e²2¶JzÐãEê\x0010xqÌÓ)ctP~\x001bæyÎû3\x001a×·3\x00153òýÐöûýðSÌ½Ñ\x001f\x0012ý[\x000bÕ æ\x0008\x001djEà4O\x0002Ç£\x0017Jì\x000c*å)\x0000s|0NnãÃ áYÖD2tÚ\x000fãù¬c ç\x000eÁ§[\x001b5Eúì\x000côh¶9ÞÆN9ïãÁ\x001czá\x000c\x0019{\x000cºÜß\x0001c`â\x000bªáÝ9$½?97\x000eÃk¦`µRB¨\x0008ýÿÖu¤À\x0018b-~
\x0006ë}õ>ª\x001að¶qÇâT¯,û¢Ú*\x001aR\x0012ÕRJn\x001bk·"¶Aí´£"½ó¡pÌ9"\x0005&DÌ¹Tù¦¶ÜÎ\x001cª¾ÝnÚð9?ðØù¼Ùg\x0003ÿv(VV ?w"3ÃCçsHzÿÏÿÿÿ\x0019\x0013å±Snq¯D\x0018M­\x001cB¼­\x000b\x0006áXå
¶-7á'ôx\x0017¼Ø(ÊLÌ\J\x000bÔ\x0010k¯j]×y\x001då_\x0016·®\x0000\x0000·\x0005ØÏÏl¢¥d?ª©ú>hÛ¶m[.9ûóËÛV½z\x0016¸\x0013pô7¸\g"Ji!)\x0001@\x0008ÝÓõC\x0015F\x0011½RÛ:#cÐ_s¾u*\x0012¢A*Z¤H.!äg[ÇMè\x0004I'\x0001ýYIéèöa\x0011oûú'\x0008a#\x0006\x0014?1Ï>\x0013ÂîwVÑï÷U[%\x0015çå-­\x001dºM¾vË\x001b\x0011\x0005\x000eÄj¾®À\x001eXc«}ö?lZ¹Ò\x0016hf"¥Ã(+N|í½fO}½Éµm\x001b\x000c/Ò[ÝA¢©Ûý6\x0013&\x0013Yñ¥æEyu²¦ÇÓgã)\x0007)@ò3{ómÿªÌ¿´]ôËp\x0008HÅÁ\x0017\x0011)!Dwr\x001d®Ù\x0002G57ÇÐ\x0011j¢&Ï+²\x0007ØÏ\x0008%:¬ÂûÏþ\x0008¼Ë~B\x0010o\£ÚË\x0004Øcç\x00121"1b%ÍñÛ¾ýùÏ¾|s.\x001c\x0013"#-\x000b\x0010«\x0019N,`ÙDUKÙ\x0016\x0013¼I)\x0004ÜóùÅK\x000fªö\x0010ßÔ\x001b\x0019!%Ä? ]\x0019\x001eµñâ¤ÕÚ\x001f×6?9¤\x001dD¼\x0016÷ÐÙÀöÚ÷ËËK}(C9ÿá\x0018\x0003ââØ'¢\x000b\x001ek]\x000f*\x0013þ¾¡</p><p>ä}\x001d£¡]GtÉ\x001b¿ù)É;Rô5\x001a\x0000BdBD²Æ¶ÅþÿÆkëóíÌÑüé½ÀùZt·g8Ý\x0013¹Ïc\x0011aìÀ<?¿$Eìi]v,:\x001c\x0017§xyúybò¥û3ö?q\x0018<ç\x0000\x0010Å¿øcp\x0011£°\x001ed\x0013Ë¼y,\x001c!"Û\x0011\x000bþ\x0007d\x0008"Pãs9HÓ¼þlùìðÍÎÔ\x001c\x0000îëêÃ\x000bçÐ?}\x001câ%Âoß¾­ëjµª\x001cØD\x00131\x0000\x0010ó\x0018 *ÓnøXK\x0002µ]"ED	xo2×A×` óôý´\x0017¡:c\x001cç\x0007JÞÇè\x0002KnÛâ*\x000eÌÁá\x000eî\x000f\=
D÷Âú£ÜðÈµP¥\x000f{\x0007<\x0016\x0013ÏÐ
gæ¤C\x0015?\x0010ë?!\x001bÉÇNÍJ\x0011Bå\x0010|\x0010ÕÌ[&!Æ\x0010¸¼,\x0013õÆºl¿\x0008G¹tÄK)½Þ)1FGU"\x0018\x0000ä"BR8Æ°mÇ%1@,ëæ¹¶Ã|³\x0014\x000f©¨Goà%Lßä\ÎÌ\x0001[Ì!¥É±þÄ\x001c\B\x0013\x0011m%{.á;\x0017\x00081âzßúm®\x0003Þkm\x0015ÍruÝñ÷E¶¢48Ù8\x000bú?s|fc;ÎñO2Ôd\x00032\x00018;Æû°vòÇ@È©ÃB\x001d^\x0015\x001cß\x0008~-ª\x0006B
\x0002¡æ¸s³Yó+ò`\x001dëómq\x0000\x0012\x0011Ì!©RÎÅ!\x0013 T\x0001^\x001c\x0002T-D²>rÎÜÜèÌÄ÷E¯É\x0000\x0000#ªÕ\x0004F\x0003´g\x0011Z\x0011,ìú¢Txþp¦?Ì\x0013\x0005Ð\x0018\x001dàa;\x0016\x0008	UÁÌ\x001c­Î\Ëô@\x0008 *U\x0016Y³¨!(©©'N\x0004@¢ÚQ@\x0007(×Ø¡:á\x000cÊ$\x001c\x001eçUý+n\x0017§ª'sr$µq%<\x0001\x0000\x001aÑ4_Öõ\x000e¨1Òëå×oßB¤·ß_Ó<\x001a\x0011 gÄ@J)ZÔ~É\x0005´¨\x000bïK±"ÚpóÒ´Þô\x0000\x0011Ù	2J÷ê7þ\x0018w ©¶\x0008\x0018b=ðõ\x001c¬f8ëÖ)Q¥H\x0016S@C\x001eI\x0015Û </p><p>çª>ÇëG\x0001\x0007y¨\x0013ÿv1hfY}oTdö§X?'\x001e\x0013BìUúCðJÔ|« ×\x000e\x0005"\x0000'¨>Á~¬[O"»³ÏóÑÓ¦ÿ¼æ\x001f\x0014#¾s}æ¬ó9\x001eÍ¹ùãß>\x0011Z>\x000b\x0011÷\x001b¡Ë\x0011¬¢\x0010þCâT;HFÿOéÿc+ùª\x0007åÏ;¢Ï¿z\x000c°Yª©e\x001aòÂñ,!\x001ceeìUX:ïx|ö@mÜEß\x0006
â~\x000cÜ¿÷_ä0tT\x00037rÎ.ç+*(X3%Q[WlZ)ê¼9S\x0007«uy#\x0011ÐHÍ\x0002R`z_\x0016æ\x0010CÖ\x0005¬V÷¦)ú+ME\x0003DjJÔçÃ\x0000\x001cçí¡õ`2Æx¹\¾|û:MS	\x0000rÞ\x0010ñv»¿½½ÞnwÇ«3\x0000ìh+ß^ü\x000f</p><p>BÏqù\x000fC{6àýçQèåì3§	@ÿ7÷uë\x000eó\x001dPËè\x0001·z<mj\x0006\x0007òkQ-ªLè¨Ì%o%g\x000eA¶\[ÛÍP\x0011qÛ\x0016gÖ"RÞ67·F"Û¶å!àÞ¶­`\x001bü×\x001bIÄ8\x0002Hq®\x0013\x0003¦\x0017\x000e\x001cCe\x0011¸</p><p>PÁ\x0013øzådf¶æ­2Ï³\x0007=f*[\x0011)·"fö±¢P3EÚ;>\x0006Ðâû&'à­òö\x0001öðèîö|Ú<\x00103O\x0019\x0003Çñ÷;TàÀ¯;¡\x0002=Ååòxl{íÛÀ@ªã*wÕ\x000cö\x001b¨Ë\x000e·\x00180\x0004iÕ{è2E\x000fk)çªâ</p><p>àçöú"ù³¦æ\x0001çÍ>Þ6\x0000H)¹ÿ²ö\x0019J\x0013TóYç\x0001+\x0011ÆHÓbª\x0013\x0011h)¹</p><p>\x0006a\x000e÷û-¥4M)è\x0019æº®"B/efÎ3g\x000eS9çms51¿ÿ\x000fý\x0008Ë)i~ò±àa¦ï·Ûý~7À±\x0014§i)ÅÈ)E5ü]ê\x001cUuö\x0005K1tÌ\x0010\x0003	òÔ¨îðàÏ\x001c \x0019^BÄ\x0010«s¡»ºxÀ0ÛÕßAïö\x0001\x0000-ËòõëË4Mï··¿þõ¯ÿãoÿî*@F\x0018ct¿J\x0001\x0004d\x0001#\x00030Á"ªÅDM2ª+±´¶¯4ðXÝÞ:Ø½
2\x001d\x0018f?ÞøGÞËÈ±mQy3Ê×\x0016)®ã:wR»íêØÙzÜq\x00038é\x0000\x001cÉÊG#ú'Ï±â>þ«Q© \x001d;VÔN:<'UsÞÇAÕ¬iÿz×Îm
N\¢?sAõN§?áPû\x0019øßqÌ?\x0015U=M\x0000Nêó®ïÓ\?ÕH\x0007àÜÈ\x000f\x0000þ\x0004à¬2m4\x0006vGe³°DÏn_×û¨¶×aoc\x0013EEkô\x0007§³gñO\x000fµý|\x0002ðPDsa±"eW\x0018ûpô\x0017þ%_ãã÷\x0004ÀlYn¾2h-\x0007«ªT<½Iqä$1yéÍe\x0011\x000c½\x0007\x0000\x0015j%ª\x000c\x0018\x0002Î¯\x0013 \x0010#ýÛÿòoý¶× (\x0004&bò4\x0001\x0018\x000b\x001c¹ìÉ*3g)1¥ëåòíÛ¯À\x001c­©8lÛöþööû?~ûûßÿv»ÝC\x0008fj¨n·¬½ù@C\x001d\x0001ÁºNÿ\x000eÔÃ{ýY\\ûõPÝÿIÏ¥ñ\x0008ð:ª!ÄØ«P÷û\x001ac\x00081\x0006fU\x0011)ª\x0012cægiÇ-äýö®¢\x0013N!°¨ªh¥n©\x00001</p><p>Ô÷\x00089Á¶s\x0008AEÕ7¼m\x0019Î£</p><p>R¢õ6\x0002\x0013±*Ç\x0018=i£È\x001dÇß \x0008.AäU\x0014²Åè\x001eÕèZ=jÙÔ\x0018Ñ[
ªÕÓà#m109P¤¿c¾o­ëj\x0000`Zyëö9+õ­èÿK8j¿\x000f\\x0019[K­tgGHÒÏ~ïA\x000eR²%Þ\x001dB`æ¾qVjGW{ý g\x0008Ìh.8;_æ\x0014\x0013A&{ow]×mÛ\x001cÌCä)'Å\x0018»n\x000b\x0007B2)%\x0004t@BÎ\x0019ª\x0000T\x0011Ù6 \LEÌ\x0014Ð\x0003¥\x0014R¥P\x0019å¼z£\x000c®/îS¡\x000e\x000e\x0001'µÄD×\x0018B.EEt\x001eb\å~»-Ë³\x000e(ÆÃ7T­ô_¿^¯/)\x0005\x0011º\x000fL\x0014«7¢</p><p>8MÓ·oß¾|}ñ;\x0006[z¹Æy¾¸³¬SwÖu½ßï÷Û³\x0000Þÿ`\x00148v·cì8\x000fPC Rò§@4v~ð,¡õ\x0005È\x0017Õý<Þó¿ùòåR\x0012ßo¿ÿöö.¥\x0014S"Z¶5ÄHÀH¸eEBqí 5$\x000cHHF¦h
ÌÐv\x0002td:b`@Âó!\x0016©ý\x001c£A~GO¿\x001fG³¶ýåÜÐ_\x0015Z`\x0000.WË(ÐX.L;\x0005QóÏãÅÀ\x0014Tõi¤Ø^½\x0003ÕÁ_\x001f ,±jÀ¨tÔÖØò>\x000b</p><p>\x000fäø¦\x0003\x0000E³\x0008\x00101¯ÒUê4Cwb\x0008kÎPW#we<Ï¸\x00168ËaÆùyæ(<\x001e\x000fãð\x0014}á&ñ\x001fò\x001eèöâ!´>¬çÕÅùSîß?ôPÑ|\x0014?8£õ~öü\x000fûÃØâóî(\x001fImD\x0014Î8\x001eNfÅj	VãHòá×*BK#\x0014m¼ÎÃ9?±?Òsñ\x0003Í'NÏ\x0004OÑ #ÑYk\x0011\Áx\x0010gûð\x0000º¢Ñóî\x0007a×cáb-^KòÛé.ÜU\x0005±Ô5­ËØùyz\x0013À\x0014\x0008Þo·À8i\x0002H·Û»ïã8Ï\x0017l0õ¾</p><p>ï»	{á&$\x0000û5¯ë^YÖ|½¾|ûömºÌÓt\x0011°R¼Qkªæé2Ïó<\x001b\x0002ðoeÝ\x0000@\x0014uçX3>çvBè14G=Mü~Ô]lº½|èu\x0000DÕÙ\x000e\x0004òògÎe¾¾øìÊb)¥¼m´±\x001d°\x001dû\x0005\x0006d11)N\x0012ÓûºÌÀ@8y*!Zú\x001fÙ¶­
Ø#fæ\x0014³þ4©ICö;\x0008\x0008ÌÄ<1\x0011ÆPDC\x000c\x001eôÙa\x0004X1\x001cy©Æ[ª\x0002Ë²©\x0016U£!	+õñ Q0$\x0007F;\x0005\x0002\x0000D%×2ìÎkDêNHuzë	ôÇ·?ú±*F¤?ª³||ñ\x000eJ)ÃZÔ¥\x001e'Áójî¸\x0012ìÕMü\x0014\x0007`Ö.yéíTOý«¢ÔI¦«%3\x0002\x001a(9?\x000féÐ'\x0011Q#l°®@\x000cÓ4]æ9DÞ¶
©nñ¾ßÎsç\x0004\x000fAC@\x0014+¢j%\x0008@\x001cÒ<§R²©JQ3\x0010GËÉ²,¹d×ðá\x0001jï)E\x000b­\x0014\x00008PB\x0006:l\x0003:\x0018q\x001c(3"\x0012Ù\x0000^®/
È¤Ó\x0014·8\x0010\x0011×F®Quón413~ùú%ÅDdî?2Î\x0001\x0004ÌCÙ\x00118\x0010\x001a¬÷Û¯/ÌP®ëR\x0002TbvñÜ\x0018C)ºÝ%R¤\x000b­´f"\x000fÕ\x0005KjÄ'¼yÞèü&-ÖÄh\x00109"eS\x0002¢X\x001b*ôôÃ\x0017Ñ» ö\x0006A\x0001tìM×T\x0007×	©\x000c\x0008\x000c@#`d </p><p>\x0001ì\x001e88@å2aß\x0014ÉÀª$\x000eíÁô¨B[½¢\x0013ði\x0002p\x000cp{Åñ»Þ\x001dmûÜo4ÍûçÓQbu\x000c\x0006wøÐpÍ£êY`zÜ¤\x0011èrýñ»"\x0000\x0006\x0003\x0010\x00030@</p><p>»ýÈAMåäOÖ
\x001aìª\x0001\x0018@»l1Ç¢Éxm'Ýa¥;nø
Ôcåx\x001c0¾k\x0007?çc\x0008'ðkç><ýþ#ýÈµýáïÇïá8\x0001üD]ù;ÉL?ÅDéÙ1ÀÓõ;Å¬O	Ï+âæáñYâñÌ¨«\x000bÑ\x000eçD$FøP,\x001bZøì:ÏÆð´ópò2'8=+ÉîÿLTÅ\x0008
Í\x001dúà\x0011éNÃy>suÈ9fÌ\x0001±2è\x001c\x001e\x0002fb*¢\x0004\x0014\x000bÿÄ	*y\x000b\x001cPÌX\x001b­õ!º\x0019%·ï\x0012\x0003P´bÅ¤ .K\x0005]è¥é\x0018â\x001b7\x000cî|ID\x0010cdbu!²Ö`ÃjêQ¢Ç\x0003l¦z5zÊª*\x001c.\x0014\x0011\x0002Ý·»\x001e£§\x000b\x0019ÄKüËýüõÿ\x001f\x000fÅmÛÜÒÄCY\x0000èðoB</p><p>10VQ£\x0018Â}Y¼ü,¥PKrÎ1F×Y\x0000\x0000DfbQ)¹LÓ$
NBÖgNE×{\x000cê|)%5[îwÔõ6¡í\\x0018n·÷\x0014SL)Æ¸,÷Î»=V\v\x001b\2\x0011û¸\x0014Ss\x0008·³MMASJ¢¢Ê*³ÊM¹ßµo×Zzè<ò;ýåíLýÅ jUCºL>\x0001bÁ\x000eDÃ'ºµÖ¥â×Y¬hØ"(¸ËU¬oÅOÓ´\x0007"sÜ¶­Ñ\x001bÄ+Êª\x0007'¹|®q,±«L<P&\x000e\x0006\x0010ôÀñ£ç¸\x000f¯ê'þðù/úc¬í\x0018üu\x0000Fd'¾0\x0011²þ¾\x0012ÑÙù\x0003s\x0008ì<Ô±\x000bÑû×'«6YF\x0005Gÿc\x001b\x0007àãè?`\x0002hHÆ@ÇbªW+D¨·Bä\ÖR,pd\x000e1\x0006"¾\/Ýµ	ë;ôç/¿\x0014G\x0002bf\x0001(tÞRy`YD©HFC6AÄmÛr^j¾!aÓø\x0018ÆÄL\x001cÈÈ\x0016ÿqÖµ¬K\x0006\x0010Âº®DÀaRÍDa¦y¾\x001eìó<oÛ¶,k²mÙ'9":O¦óðc%ã\x001b.ºæ\x0008 W\x0010\x0000\x0019rÎH+\x000f ®÷Êà2\x000e^j
@ ª#¤d{\x0007<´w/­f\x0001"b</p><p>L¼mR\x0004
EMÙúô3\x000füë¼Qó®4fÙÚ\x001d'\x0010{©FAG3îzû\x0014pàÒ\x000cæt£Ø\x001e\x0004\x0018\x0010oÌ'1Ðþ(òC\x000eg@?:ßñ+\x000fñ\x0015\x000e8\x000cîF÷gAª~bmñ\x0013|\x001cÃ\x001fÂrÐ\x0000íÇ	ÀÀÔ;m\\x0019}¨j·8ãÀà¤­ù³Û>6Öß\x0003|²\x001e?`Ð\x0007Ái%þ¬@s(\x0000í£û½*\x0015=½/z^ÉÁ0â\x0000½_$\x0006ÊóÊ+Û3»\x0000Xy®5W¤ácûèJàð\x00047ópæOHl\x001f×êþó§ Rã{ñ\x0010>Rj\x0015\x0012\x0002\x0000Ï.÷{Ç¡+»¿G ¥b\x0004Å¬©óH	!X\x000bã?Ó%\x0003h\x0006vÄÂ) ·ÍZ'\x0008\x0015\x0000JÎ%çûý\x000e \x001c8¥\x00148¼¾\x0019\x0007¦)ÅR\x001a\x0003$$qApÕ½»Ò\x0005-L\x0011¸\x000bàÛm¡\x0018©m\x000br\x0004ÛåGë\x00030SÒ×_\x0011\x0015]\x0004T¸x{¿\x0011±³OÁ)Íß¶ä"*4]æ³7F®×É§w®*$¦\x0016CÀ\x0018½\x001eÃ\x0014D´LD\x0000ÁÌJ\x000f\x0017¦E©]uÍ
àèååÅ[\x0019\x0000Rbæ¼m\x0000À%\x0010UV­­\x0016ëv\\x0015WÈÌàÃ\x000bÉDH¼ãçÄ2d\x0015\x00175Ñûm­</p><p>µð¾¯Å­òG.Xë</p><p>Õ7YL\x001aYäë×¯=\x0001À&×(fîüÚC\x0004·&\x0003mí×/"Z©¦nNà1[à¤Uz\x001a/Ó\x001d|½¢êM+UÅm]×ÕÑ\x00151E¯×èÑ5ãAA\x0002»KQö\x0003\x0000×|Ðe\x000788ó}æ\x0018£ÿ±ú5kÏ³À]\x000e\x0019ýðoÏ^æ¿ì½8ø^\x0004ßþ¶bøÑ1÷ã?©z¯ÉvåÇ?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/](https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/](https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/](https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 6 [/blog/].</p><p>Predicted response size: 306.</p><p>Response Body Length: 313.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/](https://www.dossierfacile.fr/blog/5-conseils-pour-trouver-l-appartement-de-ses-reves-en-region-parisienne/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/](https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/5-astuces-pour-booster-votre-dossier-de-location/](https://www.dossierfacile.fr/blog/5-astuces-pour-booster-votre-dossier-de-location/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/](https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/](https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/](https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/js/security.23b1d3a3.js](https://www.dossierfacile.fr/js/security.23b1d3a3.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/app.47b6a109.js](https://www.dossierfacile.fr/js/app.47b6a109.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/404.7d09a00a.js](https://www.dossierfacile.fr/js/404.7d09a00a.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/faq.d3736cba.js](https://www.dossierfacile.fr/js/faq.d3736cba.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/blog.d4c1eab3.js](https://www.dossierfacile.fr/js/blog.d4c1eab3.js)
  
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information?lang=en](https://www.dossierfacile.fr/information?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees?lang=en](https://www.dossierfacile.fr/securite-des-donnees?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees](https://www.dossierfacile.fr/securite-des-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold_Italic.7a9cccf8.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold_Italic.7a9cccf8.woff2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/faq.02fec25a.css](https://www.dossierfacile.fr/css/faq.02fec25a.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2](https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/favicon.png](https://www.dossierfacile.fr/favicon.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/css/faq.02fec25a.css](https://www.dossierfacile.fr/css/faq.02fec25a.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold_Italic.7a9cccf8.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold_Italic.7a9cccf8.woff2)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2](https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/favicon.png](https://www.dossierfacile.fr/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Mkmy6hud6to17l690lTkWmUEjMJGlE25ayOR1_8QUDqmcfqjM52Ctg==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information?lang=en](https://www.dossierfacile.fr/information?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `pqUoXNBmcXa9SdgsFQsJe4t8G5D0GKXcHU8HzxYGU2Ef3g6nKWI2gQ==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `5_J6ZnRVCVzIU2WQg6-u0wpA1WyH-3JTS8RpAAESXFojAiDLLoq5-g==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `dDDNYBH0sobiY11Pah0YNFaRD8_qrbJJgrS2NgvH9PqYHIL-55vFiw==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees](https://www.dossierfacile.fr/securite-des-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `tE43ZJLR62lWy9R2MKsiOifY4MGBMlu7-ROuPyYcmcTNCp6he9z9zQ==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `3k6zYUlRPhkzq3laIaahOomkKLJoI3FYq7vlBirkldjr0bTGcnILMw==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `RuH6VHfREjEGlRyJ0LWCV8qUB-DM0ckoXAPhOZgaZsPkeUOWq4Bbuw==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees?lang=en](https://www.dossierfacile.fr/securite-des-donnees?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `njyrzdGTqYZ6f1rNRQgxn-esJQIDqxn9nCIqFJF-sVOE09oy8E7Wgw==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `GxjyQHh26WqtooDXJg8rlLaWjOCggJAgOwtnKfV2xf0oAgT9Wyj68g==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `7J9VBTK4KDDjLCMB14INAbusTEiZY8-0bIYvv3-m27-QEMzfKAhkew==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `qtfvsgIDAtHM-pbfCvIhQU4t5Hi9fRxGaWpo4cZy0eIQ9_L6NJrkQw==`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Nzap0JrpJUPSHRRdh-1IEhTe_QhM7pRd5ql3TdID3xJ5hSZu1ePQ4A==`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>2I��\x001b���5�^��T�Ze\x0004��F�M�k#���\x0010P:�q��3���</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/js/dsfr.module.min.js](https://www.dossierfacile.fr/js/dsfr.module.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/app.47b6a109.js](https://www.dossierfacile.fr/js/app.47b6a109.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/](https://www.dossierfacile.fr/blog/comment-justifier-son-domicile/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-0edcdd10="" href="#" class="underline">DossierFacile</a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-eb3165ea="" href="#" class="underline">DossierFacile</a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/](https://www.dossierfacile.fr/blog/quelles-pieces-justificatives-fournir-pour-mon-dossier-de-location/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-47ae17ee="" href="#" class="underline">DossierFacile</a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-5e3a594c="" href="#" title="république française" class="fr-logo"><span data-v-5e3a594c="" class="fr-logo__title">république <br data-v-5e3a594c="">française</span></a>`
  
  
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees?lang=en](https://www.dossierfacile.fr/securite-des-donnees?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information?lang=en](https://www.dossierfacile.fr/information?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees](https://www.dossierfacile.fr/securite-des-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/favicon.png](https://www.dossierfacile.fr/favicon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees?lang=en](https://www.dossierfacile.fr/securite-des-donnees?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees](https://www.dossierfacile.fr/securite-des-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information?lang=en](https://www.dossierfacile.fr/information?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2](https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
Instances: 2
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0,no-cache,no-store,must-revalidate`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0,no-cache,no-store,must-revalidate`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0,no-cache,no-store,must-revalidate`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0,no-cache,no-store,must-revalidate`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16758465`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16770229`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16119260`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16113331`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15308410`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `14315734`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10025880`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777184`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16775885`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11119017`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16445670`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `14204888`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15787660`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16316671`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16121850`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15132410`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15657130`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16772045`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16444375`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.2c560b30.js](https://www.dossierfacile.fr/js/statistics.2c560b30.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16770244`
  
  
  
  
Instances: 82
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>16758465, which evaluates to: 1970-07-13 23:07:45</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

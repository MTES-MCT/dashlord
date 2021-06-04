
# ZAP Scanning Report

Generated on Fri, 4 Jun 2021 01:13:41


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 7 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 3 | 
| Dangerous JS Functions | Low | 2 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 12 | 
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
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/](https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/](https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq/](https://www.dossierfacile.fr/faq/)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" target="_blank" href="https://twitter.com/dossierfacile" rel="noreferrer" class="fr-footer__bottom-link"><svg data-v-e3dd2628="" title="twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter-square" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 512" class="fa-icon"><path data-v-e3dd2628="" fill="currentColor" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-48.9 158.8c.2 2.8.2 5.7.2 8.5 0 86.7-66 186.6-186.6 186.6-37.2 0-71.7-10.8-100.7-29.4 5.3.6 10.4.8 15.8.8 30.7 0 58.9-10.4 81.4-28-28.8-.6-53-19.5-61.3-45.5 10.1 1.5 19.2 1.5 29.6-1.2-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3a65.447 65.447 0 0 1-29.2-54.6c0-12.2 3.2-23.4 8.9-33.1 32.3 39.8 80.8 65.8 135.2 68.6-9.3-44.5 24-80.6 64-80.6 18.9 0 35.9 7.9 47.9 20.7 14.8-2.8 29-8.3 41.6-15.8-4.9 15.2-15.2 28-28.8 36.1 13.2-1.4 26-5.1 37.8-10.2-8.9 13.1-20.1 24.7-32.9 34z"></path></svg></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" target="_blank" href="https://twitter.com/dossierfacile" rel="noreferrer" class="fr-footer__bottom-link"><svg data-v-e3dd2628="" title="twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter-square" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 512" class="fa-icon"><path data-v-e3dd2628="" fill="currentColor" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-48.9 158.8c.2 2.8.2 5.7.2 8.5 0 86.7-66 186.6-186.6 186.6-37.2 0-71.7-10.8-100.7-29.4 5.3.6 10.4.8 15.8.8 30.7 0 58.9-10.4 81.4-28-28.8-.6-53-19.5-61.3-45.5 10.1 1.5 19.2 1.5 29.6-1.2-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3a65.447 65.447 0 0 1-29.2-54.6c0-12.2 3.2-23.4 8.9-33.1 32.3 39.8 80.8 65.8 135.2 68.6-9.3-44.5 24-80.6 64-80.6 18.9 0 35.9 7.9 47.9 20.7 14.8-2.8 29-8.3 41.6-15.8-4.9 15.2-15.2 28-28.8 36.1 13.2-1.4 26-5.1 37.8-10.2-8.9 13.1-20.1 24.7-32.9 34z"></path></svg></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-6a40aa08="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-6a40aa08="" alt="logo monsieur hugo" src="/img/monsieur_hugo.e9cd46d6.webp" class="partner-logo"></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/](https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-f71201f6="" target="_blank" href="https://www.legifrance.gouv.fr/loda/article_lc/LEGIARTI000038834725/2019-09-01">par ces termes</a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" target="_blank" href="https://twitter.com/dossierfacile" rel="noreferrer" class="fr-footer__bottom-link"><svg data-v-e3dd2628="" title="twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter-square" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 512" class="fa-icon"><path data-v-e3dd2628="" fill="currentColor" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-48.9 158.8c.2 2.8.2 5.7.2 8.5 0 86.7-66 186.6-186.6 186.6-37.2 0-71.7-10.8-100.7-29.4 5.3.6 10.4.8 15.8.8 30.7 0 58.9-10.4 81.4-28-28.8-.6-53-19.5-61.3-45.5 10.1 1.5 19.2 1.5 29.6-1.2-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3a65.447 65.447 0 0 1-29.2-54.6c0-12.2 3.2-23.4 8.9-33.1 32.3 39.8 80.8 65.8 135.2 68.6-9.3-44.5 24-80.6 64-80.6 18.9 0 35.9 7.9 47.9 20.7 14.8-2.8 29-8.3 41.6-15.8-4.9 15.2-15.2 28-28.8 36.1 13.2-1.4 26-5.1 37.8-10.2-8.9 13.1-20.1 24.7-32.9 34z"></path></svg></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-6a40aa08="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-6a40aa08="" alt="logo monsieur hugo" src="/img/monsieur_hugo.e9cd46d6.webp" class="partner-logo"></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq/](https://www.dossierfacile.fr/faq/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" target="_blank" href="https://twitter.com/dossierfacile" rel="noreferrer" class="fr-footer__bottom-link"><svg data-v-e3dd2628="" title="twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter-square" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 512" class="fa-icon"><path data-v-e3dd2628="" fill="currentColor" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-48.9 158.8c.2 2.8.2 5.7.2 8.5 0 86.7-66 186.6-186.6 186.6-37.2 0-71.7-10.8-100.7-29.4 5.3.6 10.4.8 15.8.8 30.7 0 58.9-10.4 81.4-28-28.8-.6-53-19.5-61.3-45.5 10.1 1.5 19.2 1.5 29.6-1.2-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3a65.447 65.447 0 0 1-29.2-54.6c0-12.2 3.2-23.4 8.9-33.1 32.3 39.8 80.8 65.8 135.2 68.6-9.3-44.5 24-80.6 64-80.6 18.9 0 35.9 7.9 47.9 20.7 14.8-2.8 29-8.3 41.6-15.8-4.9 15.2-15.2 28-28.8 36.1 13.2-1.4 26-5.1 37.8-10.2-8.9 13.1-20.1 24.7-32.9 34z"></path></svg></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/](https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" target="_blank" href="https://twitter.com/dossierfacile" rel="noreferrer" class="fr-footer__bottom-link"><svg data-v-e3dd2628="" title="twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter-square" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 512" class="fa-icon"><path data-v-e3dd2628="" fill="currentColor" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-48.9 158.8c.2 2.8.2 5.7.2 8.5 0 86.7-66 186.6-186.6 186.6-37.2 0-71.7-10.8-100.7-29.4 5.3.6 10.4.8 15.8.8 30.7 0 58.9-10.4 81.4-28-28.8-.6-53-19.5-61.3-45.5 10.1 1.5 19.2 1.5 29.6-1.2-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3a65.447 65.447 0 0 1-29.2-54.6c0-12.2 3.2-23.4 8.9-33.1 32.3 39.8 80.8 65.8 135.2 68.6-9.3-44.5 24-80.6 64-80.6 18.9 0 35.9 7.9 47.9 20.7 14.8-2.8 29-8.3 41.6-15.8-4.9 15.2-15.2 28-28.8 36.1 13.2-1.4 26-5.1 37.8-10.2-8.9 13.1-20.1 24.7-32.9 34z"></path></svg></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" target="_blank" href="https://twitter.com/dossierfacile" rel="noreferrer" class="fr-footer__bottom-link"><svg data-v-e3dd2628="" title="twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter-square" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 512" class="fa-icon"><path data-v-e3dd2628="" fill="currentColor" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-48.9 158.8c.2 2.8.2 5.7.2 8.5 0 86.7-66 186.6-186.6 186.6-37.2 0-71.7-10.8-100.7-29.4 5.3.6 10.4.8 15.8.8 30.7 0 58.9-10.4 81.4-28-28.8-.6-53-19.5-61.3-45.5 10.1 1.5 19.2 1.5 29.6-1.2-30-6.1-52.5-32.5-52.5-64.4v-.8c8.7 4.9 18.9 7.9 29.6 8.3a65.447 65.447 0 0 1-29.2-54.6c0-12.2 3.2-23.4 8.9-33.1 32.3 39.8 80.8 65.8 135.2 68.6-9.3-44.5 24-80.6 64-80.6 18.9 0 35.9 7.9 47.9 20.7 14.8-2.8 29-8.3 41.6-15.8-4.9 15.2-15.2 28-28.8 36.1 13.2-1.4 26-5.1 37.8-10.2-8.9 13.1-20.1 24.7-32.9 34z"></path></svg></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-6a40aa08="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-6a40aa08="" alt="logo monsieur hugo" src="/img/monsieur_hugo.e9cd46d6.webp" class="partner-logo"></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-6a40aa08="" target="_blank" href="https://www.monsieurhugo.com/" rel="noreferrer" class="logo-link"><img data-v-6a40aa08="" alt="logo monsieur hugo" src="/img/monsieur_hugo.e9cd46d6.webp" class="partner-logo"></a>`
  
  
  
  
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

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://www.dossierfacile.fr/assets/pdf/Listedocuments.pdf](https://www.dossierfacile.fr/assets/pdf/Listedocuments.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#O6CO`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#O6CO</p>
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/](https://www.dossierfacile.fr/blog/dossierfacile-fait-peau-neuve/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/](https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq/](https://www.dossierfacile.fr/faq/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
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

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.dossierfacile.fr/faq?lang=en](https://www.dossierfacile.fr/faq?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 5 [/faq/].</p><p>Predicted response size: 305.</p><p>Response Body Length: 313.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/app.0e877e83.js](https://www.dossierfacile.fr/js/app.0e877e83.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/security.e30d4be2.js](https://www.dossierfacile.fr/js/security.e30d4be2.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/blog.36613aef.js](https://www.dossierfacile.fr/js/blog.36613aef.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/information.7fabcb51.js](https://www.dossierfacile.fr/js/information.7fabcb51.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/faq.e0d00200.js](https://www.dossierfacile.fr/js/faq.e0d00200.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/404.8f8b0870.js](https://www.dossierfacile.fr/js/404.8f8b0870.js)
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/css/404.39cf136e.css](https://www.dossierfacile.fr/css/404.39cf136e.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/information.37de6aeb.css](https://www.dossierfacile.fr/css/information.37de6aeb.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/chunk-vendors.b6c04b1f.css](https://www.dossierfacile.fr/css/chunk-vendors.b6c04b1f.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/statistics.51669fd7.css](https://www.dossierfacile.fr/css/statistics.51669fd7.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/faq.02fec25a.css](https://www.dossierfacile.fr/css/faq.02fec25a.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/approval.faecf71e.svg](https://www.dossierfacile.fr/img/approval.faecf71e.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/app.42a1e661.css](https://www.dossierfacile.fr/css/app.42a1e661.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/security.a6bcf1f8.css](https://www.dossierfacile.fr/css/security.a6bcf1f8.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/blog.a5215db4.css](https://www.dossierfacile.fr/css/blog.a5215db4.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
* URL: [https://www.dossierfacile.fr/img/sports.c9a8aa37.svg](https://www.dossierfacile.fr/img/sports.c9a8aa37.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=31536000,public`
  
  
  
  
Instances: 12
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq?lang=en](https://www.dossierfacile.fr/faq?lang=en)
  
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold.c67116b7.woff2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2](https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/404.39cf136e.css](https://www.dossierfacile.fr/css/404.39cf136e.css)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/404.39cf136e.css](https://www.dossierfacile.fr/css/404.39cf136e.css)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `CYJGAO5fRCpLwYfE5UcyGXKMh8E0ewwV-HiHR8ZWjmv_NclRNUvz0A==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog?lang=en](https://www.dossierfacile.fr/blog?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `iRk2W8X42bkm9zPbplyNulVpfkaJFQObB5xyKWN_Ltt-9tMH-Yu6Fg==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `wo2y_DgM2kqd_rmHUCWiFrlcFD_QDPLvn4yVmTC4tIjCmeXsI0OEyA==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `PQZQrkziBVW1od2R27nKN03qcdbYfE0xFLtJujmmuArF-0YtGQ6I4Q==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees?lang=en](https://www.dossierfacile.fr/securite-des-donnees?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `e2ae2q099X-Lb-2mWUvWL91SsdxslltcseY032ajSfzMHfZmgiKG7w==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq?lang=en](https://www.dossierfacile.fr/faq?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `x9xUWDQoCXwkyBKymbyQ9wabnZbj4NTK1aMsYugfHLZHcWtgnFrMeQ==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/sitemap.xml](https://www.dossierfacile.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `pzwtZAFSU1VZ05x-JXhtWITpe-9L_JA4de-RI33D96Ivag1Vz6XC0A==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats](https://www.dossierfacile.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `vsFDk71TuRPVHsiTh_TorAivZtNFDY6IerOnRQvQHfft5hfDn0PM5w==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `jJK6Hvamzsu0_f9BWsI_qdvCsznP8Ep23tGn406y-rR65QS7IqAcYA==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1us4lPRKyu7tusgoLIoC3Wo4yyAOhIezXX9v5GNHQX60LK5L9IIGmQ==`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `PxMfRfzq80ZKhbB0s4zaYtVp3DBf64jcTO5RkxA0bgzCLLW9dALD6w==`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees](https://www.dossierfacile.fr/securite-des-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `6Zg2j1NzoDBdZ-Canik_ql-F0JDLDjhXpQGKZkKS7dgnI48UTV9P0g==`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>	�F\x0000�_D*K����G2\x0019r���4{\x000c\x0015�x�G�V�k�5�Q5K��</p>
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/app.0e877e83.js](https://www.dossierfacile.fr/js/app.0e877e83.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/blog/](https://www.dossierfacile.fr/blog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-0c5381ca="" href="#" class="underline">DossierFacile</a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js](https://www.dossierfacile.fr/js/chunk-vendors.42c9e8a1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/information/](https://www.dossierfacile.fr/information/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/?lang=en](https://www.dossierfacile.fr/?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees/](https://www.dossierfacile.fr/securite-des-donnees/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/stats/](https://www.dossierfacile.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/profile](https://www.dossierfacile.fr/profile)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq/](https://www.dossierfacile.fr/faq/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/](https://www.dossierfacile.fr/blog/tout-comprendre-a-la-vie-en-colocation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-f71201f6="" href="#" class="underline">DossierFacile</a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr](https://www.dossierfacile.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a data-v-e3dd2628="" href="#" title="république française" class="fr-logo"><span data-v-e3dd2628="" class="fr-logo__title">république <br data-v-e3dd2628="">française</span></a>`
  
  
  
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq?lang=en](https://www.dossierfacile.fr/faq?lang=en)
  
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Bold_Italic.7a9cccf8.woff2](https://www.dossierfacile.fr/fonts/Marianne-Bold_Italic.7a9cccf8.woff2)
  
  
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
  
  
  
  
* URL: [https://www.dossierfacile.fr/](https://www.dossierfacile.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/securite-des-donnees](https://www.dossierfacile.fr/securite-des-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/faq?lang=en](https://www.dossierfacile.fr/faq?lang=en)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2](https://www.dossierfacile.fr/fonts/Marianne-Regular.0cde495f.woff2)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/blog.a5215db4.css](https://www.dossierfacile.fr/css/blog.a5215db4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/robots.txt](https://www.dossierfacile.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Hit from cloudfront`
  
  
  
  
* URL: [https://www.dossierfacile.fr/css/404.39cf136e.css](https://www.dossierfacile.fr/css/404.39cf136e.css)
  
  
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
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16775885`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16032864`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `14204888`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10025880`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16729344`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16119260`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16753920`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12357519`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12632256`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15132410`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16444375`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16119285`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16121850`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16113331`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16767673`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16758465`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12433259`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777215`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15657130`
  
  
  
  
* URL: [https://www.dossierfacile.fr/js/statistics.d96259be.js](https://www.dossierfacile.fr/js/statistics.d96259be.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13808780`
  
  
  
  
Instances: 82
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>16775885, which evaluates to: 1970-07-14 03:58:05</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

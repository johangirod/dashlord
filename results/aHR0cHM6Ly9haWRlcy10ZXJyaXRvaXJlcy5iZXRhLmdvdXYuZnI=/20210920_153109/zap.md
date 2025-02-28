
# ZAP Scanning Report

Generated on Mon, 20 Sep 2021 15:21:13


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 7 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 13 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 5 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 54 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://radioterritoria.fr/broadcast/3105-Aides-Territoires-la-plateforme-qui-permet-aux-territoires-de-trouver-des-aides-pour-financer-et-accompagner-leurs-projets-locaux" rel="noopener" target="_blank">
   Radio Territoria
  </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://france-relance-martinique.aides-territoires.beta.gouv.fr/" rel="noopener" target="_blank">
  France Relance Martinique
 </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-link--twitter fr-link" href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter - ouvre une nouvelle fenêtre" target="_blank" rel="noopener">
                            twitter
                            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.idealco.fr/formation/financements-europeens-plateforme-aides-territoires-secours-14695" rel="noopener" target="_blank">
  Financements européens : la plateforme Aides-territoires à votre secours
 </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.idealco.fr/formation/plan-relance-aides-territoires-vous-oriente-15222" rel="noopener" target="_blank">
   Lien du replay (gratuit pour adhérents IdealCO)
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

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.js](https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.js)
  
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
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

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="audience" class="fr-container" action="/recherche/formulaire/territoire/" method="GET">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/b4d6-aie-a-la-creation-et-au-developpement-dentrep/](https://aides-territoires.beta.gouv.fr/aides/b4d6-aie-a-la-creation-et-au-developpement-dentrep/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form" class="fr-grid-row fr-grid-row--center">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/b4d6-aie-a-la-creation-et-au-developpement-dentrep/](https://aides-territoires.beta.gouv.fr/aides/b4d6-aie-a-la-creation-et-au-developpement-dentrep/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="eligibility-test-form" action="">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/a0bf-aide-au-developpement-numerique/](https://aides-territoires.beta.gouv.fr/aides/a0bf-aide-au-developpement-numerique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="eligibility-test-form" action="">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/3d9e-accompagner-la-redynamisation-des-centres-via/](https://aides-territoires.beta.gouv.fr/aides/3d9e-accompagner-la-redynamisation-des-centres-via/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form" class="fr-grid-row fr-grid-row--center">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/551f-copie-14h03-accompagner-la-redynamisation-des/](https://aides-territoires.beta.gouv.fr/aides/551f-copie-14h03-accompagner-la-redynamisation-des/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form" class="fr-grid-row fr-grid-row--center">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/eb28-copie-12h04-conforter-lattractivite-economiqu/](https://aides-territoires.beta.gouv.fr/aides/eb28-copie-12h04-conforter-lattractivite-economiqu/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form" class="fr-grid-row fr-grid-row--center">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/eb28-copie-12h04-conforter-lattractivite-economiqu/](https://aides-territoires.beta.gouv.fr/aides/eb28-copie-12h04-conforter-lattractivite-economiqu/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="eligibility-test-form" action="">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/bf5d-copie-11h49-conforter-lattractivite-economiqu/](https://aides-territoires.beta.gouv.fr/aides/bf5d-copie-11h49-conforter-lattractivite-economiqu/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form" class="fr-grid-row fr-grid-row--center">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/bf5d-copie-11h49-conforter-lattractivite-economiqu/](https://aides-territoires.beta.gouv.fr/aides/bf5d-copie-11h49-conforter-lattractivite-economiqu/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="eligibility-test-form" action="">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/551f-copie-14h03-accompagner-la-redynamisation-des/](https://aides-territoires.beta.gouv.fr/aides/551f-copie-14h03-accompagner-la-redynamisation-des/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="eligibility-test-form" action="">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/3d9e-accompagner-la-redynamisation-des-centres-via/](https://aides-territoires.beta.gouv.fr/aides/3d9e-accompagner-la-redynamisation-des-centres-via/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="eligibility-test-form" action="">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/a0bf-aide-au-developpement-numerique/](https://aides-territoires.beta.gouv.fr/aides/a0bf-aide-au-developpement-numerique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form" class="fr-grid-row fr-grid-row--center">`
  
  
  
  
Instances: 13
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/eb28-copie-12h04-conforter-lattractivite-economiqu/](https://aides-territoires.beta.gouv.fr/aides/eb28-copie-12h04-conforter-lattractivite-economiqu/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/bf5d-copie-11h49-conforter-lattractivite-economiqu/](https://aides-territoires.beta.gouv.fr/aides/bf5d-copie-11h49-conforter-lattractivite-economiqu/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/eca2-developper-loffre-de-logements/](https://aides-territoires.beta.gouv.fr/aides/eca2-developper-loffre-de-logements/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/551f-copie-14h03-accompagner-la-redynamisation-des/](https://aides-territoires.beta.gouv.fr/aides/551f-copie-14h03-accompagner-la-redynamisation-des/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/3d9e-accompagner-la-redynamisation-des-centres-via/](https://aides-territoires.beta.gouv.fr/aides/3d9e-accompagner-la-redynamisation-des-centres-via/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/b4d6-aie-a-la-creation-et-au-developpement-dentrep/](https://aides-territoires.beta.gouv.fr/aides/b4d6-aie-a-la-creation-et-au-developpement-dentrep/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/509b-eco-pulse-investissement/](https://aides-territoires.beta.gouv.fr/aides/509b-eco-pulse-investissement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/a0bf-aide-au-developpement-numerique/](https://aides-territoires.beta.gouv.fr/aides/a0bf-aide-au-developpement-numerique/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script src="https://stats.data.gouv.fr/piwik.js" async defer></script>`
  
  
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon.png](https://aides-territoires.beta.gouv.fr/static/favicons/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/js/analytics/hotjar_tag.js](https://aides-territoires.beta.gouv.fr/static/js/analytics/hotjar_tag.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon-32x32.png](https://aides-territoires.beta.gouv.fr/static/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/js/shared_config.js](https://aides-territoires.beta.gouv.fr/static/js/shared_config.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.a672897c48ed.css](https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.a672897c48ed.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo_AT_courbes.svg](https://aides-territoires.beta.gouv.fr/static/img/logo_AT_courbes.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon.svg](https://aides-territoires.beta.gouv.fr/static/favicons/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon.ico](https://aides-territoires.beta.gouv.fr/static/favicons/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.js](https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/home_aides.svg](https://aides-territoires.beta.gouv.fr/static/img/home_aides.svg)
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MnWRXtsTjKS9z3AdeC0yELwqtonkdWJOslvJqLLip6eYGY8UsygpRVOmNio7vKiO`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MnWRXtsTjKS9z3AdeC0yELwqtonkdWJOslvJqLLip6eYGY8UsygpRVOmNio7vKiO`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/broadcast/11984-Aides-Territoires-qu-est-ce-que-c-est`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/broadcast/3105-Aides-Territoires-la-plateforme-qui-permet-aux-territoires-de-trouver-des-aides-pour-financer-et-accompagner-leurs-projets-locaux`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MnWRXtsTjKS9z3AdeC0yELwqtonkdWJOslvJqLLip6eYGY8UsygpRVOmNio7vKiO`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>r�����{�\x0014 @
�aU"\x0001N	%\x001c\x001f������\x0003M\x000c&\x0001SPg\x0013\x001c�~�\x0001v�7\x0004X��Ϯ	���W��j�0\x000b��{V]�\x0008�j�r�����OWς���\x001d�\x0002�/S�p�s\x0007��)+��\x0011%�5�%���>���Y��\x0003��\x000c2</p><p>��1{�o��V�\x001cY\x0012"�</p><p>�;8f�`\x0000����L5nM:\x0017�M�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.js](https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.module.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://aides-territoires.beta.gouv.fr/static/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.19cf8d088cb8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected 3 times, the first in the element starting with: "if(conv!==true){if(conv&&s.throws){response=conv(response);}else{try{response=conv(response);}catch(e){return{state:"parsererror", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-nav__link" href="/" target="_self">Accueil</a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/webinaires/](https://aides-territoires.beta.gouv.fr/webinaires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt](https://aides-territoires.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/portails/](https://aides-territoires.beta.gouv.fr/portails/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/europe/](https://aides-territoires.beta.gouv.fr/europe/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `93321567`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `97231615`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `20126251`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `40675423`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `81472777`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `99986179`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `01662547`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `35913504`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `05220779`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `97208966`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `43562966`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `05259759`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `98047752`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `57984365`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `99550092`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `92129986`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `93328561`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo_mte.svg](https://aides-territoires.beta.gouv.fr/static/img/logo_mte.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `41615509`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg](https://aides-territoires.beta.gouv.fr/static/img/logo-francemobilites.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `90012599`
  
  
  
  
Instances: 54
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>93321567, which evaluates to: 1972-12-16 02:39:27</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `phone`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `organization_and_role`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `last_name`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `subject`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `POST`
  
  
  * Parameter: `first_name`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://aides-territoires.beta.gouv.fr/contact/</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>phone=9999999999</p><p></p><p>The user-controlled value was:</p><p>9999999999</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

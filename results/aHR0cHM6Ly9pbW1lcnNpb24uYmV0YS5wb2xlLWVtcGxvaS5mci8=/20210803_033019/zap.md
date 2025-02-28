
# ZAP Scanning Report

Generated on Tue, 3 Aug 2021 03:12:55


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
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| Cross-Domain Misconfiguration | Medium | 11 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Source Code Disclosure - Java | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 2 | 
| Incomplete or No Cache-control Header Set | Low | 2 | 
| Permissions Policy Header Not Set | Low | 9 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 3 | 
| X-Content-Type-Options Header Missing | Low | 10 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 5 | 
| Modern Web Application | Informational | 2 | 
| Storable and Cacheable Content | Informational | 2 | 
| Storable but Non-Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 12 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js](https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css](https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class y{constructor(e=[]){this._todos=e}async add(e){this._todos.push(e)}async retrieveAll(){return this._todos}setTodos(e){this._todos=e}getTodos(){return this._todos}}const h=n({name:"todo",initialState:{items:[],isFetching:!1,isAdding:!1},reducers:{startedToAddTodo:(e,t)=>c(i({},e),{isAdding:!0,items:[...e.items,t.payload]}),successfullyAddedTodo:e=>c(i({},e),{isAdding:!1}),startedToFetchTodos:e=>c(i({},e),{isFetching:!0}),successfullyFetchedTodos:(e,t)=>c(i({},e),{isFetching:!1,items:t.payload})}}),m=l({[h.name]:h.reducer}),b=e=>u({reducer:m,middleware:p({thunk:{extraArgument:e}})});export{y as I,b as c,h as t}`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class ph{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(e){return this.closures.push(e),()=>{const t=this.closures.indexOf(e);-1!==t&&this.closures.splice(t,1)}}next(e,t){t=void 0===t?0:t-1,void 0===this.nexts[t]&&(this.nexts[t]=[]),this.nexts[t].push(e)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const e=this.nexts.shift();if(e)for(const t of e)t.call()}}const hh=new class{constructor(){this.renderer=new ph}register(e,t){}start(){}stop(){}};class mh{constructor(e,t){this.selector=e,this.builders=t,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let e=0;e<this.builders.length;e++)this.instances.push(this.builders[e]())}}const yh={},gh={};let vh=0;const bh=e=>{for(const n in gh)if(gh[n]===e)return n;vh++;const t=vh;return gh[t]=e,t};class wh{constructor(e,t,n){const r=bh(e);yh[r]||(yh[r]=[]),yh[r].push(this),this.element=e,this.id=e.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=t,this.isRendering=n}dispatch(e,t){const n=new CustomEvent(e,t);this.element.dispatchEvent(n)}listen(e,t){this.listeners[e]||(this.listeners[e]=[]),this.listeners[e].indexOf(t)>-1||(this.listeners[e].push(t),this.element.addEventListener(e,t))}unlisten(e,t){if(e)if(t){if(!this.listeners[e])return;const n=this.listeners[e].indexOf(t);n>-1&&this.listeners[e].splice(n,1),this.element.removeEventListener(t)}else{if(!this.listeners[e])return;for(const t of this.listeners[e])this.element.removeEventListener(t);this.listeners[e].length=0}else for(const n in this.listeners)this.unlisten(n)}get isRendering(){return this._isRendering}set isRendering(e){this._isRendering!==e&&(this._isRendering=e)}render(){}get isResizing(){return this._isResizing}set isResizing(e){this._isResizing!==e&&(this._isResizing=e)}resize(){}destroy(){}static getInstances(e,t){const n=bh(e);return yh[n]?t?yh[n].filter((e=>e instanceof t)):yh[n]:null}}const kh=sh.attr("group"),Sh=[];class Eh{constructor(e,t){this.id=e,this.element=t,this.members=[],this._index=-1,this._current=null,Sh.push(this)}static getGroupById(e){for(const t of Sh)if(t.constructor===this&&t.id===e)return t;return new this(e)}static getGroupByElement(e){for(const t of Sh)if(t.element===e)return t;return new this(!1,e)}static groupById(e,t){const n=e.element.getAttribute(kh);null!==n&&t.getGroupById(n).add(e)}static groupByParent(e,t,n){if(void 0===n&&(n=t.selector),""===n)return;let r=e.element.parentElement;for(;r;){if(r.classList.contains(e.constructor.selector))return;if(r.classList.contains(n))return void t.getGroupByElement(r).add(e);r=r.parentElement}}static get selector(){return""}add(e){if(-1===this.members.indexOf(e))switch(this.members.push(e),e.setGroup(this),!0){case null!==this.current:case!(e.disclosed||e.primary&&e.primary.disclosed):e.disclosed=!1;break;default:this._current=e,this._index=this.members.indexOf(e),e.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(e){e<-1||e>=this.length||this._index===e||(null!==this.current&&this.current.conceal(!0,!0),this._index=e,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(e){this.index=this.members.indexOf(e)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class xh{constructor(e,t){this.element=e,this.disclosure=t,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(e){this.disclosure.change(this.hasAttribute)}mutate(e){e.forEach((e=>{"attributes"===e.type&&e.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(e){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,e),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const Ch=sh.event("DISCLOSE"),_h=sh.event("CONCEAL"),Ph=[];class Oh extends wh{constructor(e){super(e),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:sh.attr(this.type.id),this.pristine=!0;const t=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:sh.attr.selector("controls",this.id));if(t.length>0)for(let n=0;n<t.length;n++)this.addButton(t[n]);this.disclosed=this.primary&&this.primary.disclosed,this.gather()}gather(){this.group||(Eh.groupById(this,this.GroupConstructor),Eh.groupByParent(this,this.GroupConstructor))}static build(e){const t=Array.prototype.slice.call(e.querySelectorAll(`.${this.selector}`));for(const n of t)Ph.push(new this(n))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(e){const t=this.buttonFactory(e);t.hasAttribute&&(void 0===this.primary?this.primary=t:t.apply(this.primary.disclosed)),this.buttons.push(t)}get GroupConstructor(){return Eh}buttonFactory(e){return new xh(e,this)}disclose(e){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,e||void 0===this.group||(this.group.current=this),!0)}conceal(e,t){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,t||this.focus(),e||void 0===this.group||(this.group.current=null);for(const n of Ph)n!==this&&this.element.contains(n.element)&&n.reset();return!0}get disclosed(){return this._disclosed}set disclosed(e){if(this._disclosed!==e){this.dispatch(e?Ch:_h,this.type),this._disclosed=e,e?fh(this.element,this.modifier):dh(this.element,this.modifier);for(let t=0;t<this.buttons.length;t++)this.buttons[t].apply(e)}}reset(){}change(e){if(this.constructor.type.canConceal)switch(!0){case!e:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(e){this.group=e}get buttonHasFocus(){return!!this.buttons.some((e=>e.hasFocus))}get hasFocus(){return this.element===document.activeElement||this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus}focus(){for(let e=0;e<this.buttons.length;e++){const t=this.buttons[e];if(t.hasAttribute)return void t.element.focus()}}}Oh.DISCLOSE_EVENT=Ch,Oh.CONCEAL_EVENT=_h;const Lh={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class Nh{constructor(e){this.element=e,this.collections={}}_add(e,t){void 0===this.collections[e]&&(this.collections[e]=new Th(e,this.element)),this.collections[e].add(t)}down(e,t,n,r){this._add("down",new zh(e,t,n,r))}up(e,t,n,r){this._add("up",new zh(e,t,n,r))}dispose(){for(const e of this.collections)e.dispose();this.types=null}}class Th{constructor(e,t){this.type=e,this.element=t,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+e,this.binding)}add(e){this.actions.push(e)}handle(e){for(const t of this.actions)t.handle(e)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class zh{constructor(e,t,n,r){this.key=e,this.closure=t,this.preventDefault=!0===n,this.stopPropagation=!0===r}handle(e){e.keyCode===this.key&&(this.closure(e),this.preventDefault&&e.preventDefault(),this.stopPropagation&&e.stopPropagation())}}Nh.TAB=9,Nh.ESCAPE=27,Nh.END=35,Nh.HOME=36,Nh.LEFT=37,Nh.UP=38,Nh.RIGHT=39,Nh.DOWN=40;const Rh=sh("collapse"),Ah=[],jh={};class Dh extends Oh{constructor(e){super(e),Ah.push(this),this.requesting=this.request.bind(this),e.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const e in jh){let t=this.element.parentElement;for(;t;){if(t.classList.contains(e))return void("string"==typeof jh[e]?Eh.groupByParent(this,Eh,jh[e]):Eh.groupByParent(this,jh[e]));t=t.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return Lh.expand}static get selector(){return Rh}static register(e,t){jh[e]=t;for(const n of Ah)n.gatherByAscendants()}transitionend(e){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(e){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(e)},window.requestAnimationFrame(this.requesting))}conceal(e,t){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(e,t)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const e=this.element.offsetHeight;this.element.style.setProperty("--collapse",-e+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}uh.core.ns=sh,uh.core.addClass=fh,uh.core.removeClass=dh,uh.core.engine=hh,uh.core.Instance=wh,uh.core.Initializer=mh,uh.core.Disclosure=Oh,uh.core.DisclosureButton=xh,uh.core.DisclosuresGroup=Eh,uh.core.DISCLOSURE_TYPES=Lh,uh.KeyListener=Nh,uh.Collapse=Dh,uh.Equisized=class{constructor(e,t){this.selector=e,this.group=t,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let e=0;e<this.elements.length;e++){const t=this._getWidth(this.elements[e]);t>this.maxWidth&&(this.maxWidth=t)}this.apply()}apply(){for(let e=0;e<this.elements.length;e++)this.elements[e].style.width=this.maxWidth+1+"px"}reset(){for(let e=0;e<this.elements.length;e++)this.elements[e].style.width="auto";this.maxWidth=0}_getWidth(e){let t=e.offsetWidth;const n=getComputedStyle(e);return t+=parseInt(n.marginLeft)+parseInt(n.marginRight),t}},new mh(`.${Rh}`,[()=>{Dh.build(document)}]);const Mh=uh.core.ns("accordions-group"),Ih=uh.core.ns("accordion");class Fh extends uh.core.DisclosuresGroup{static get selector(){return Mh}}uh.AccordionsGroup=Fh,uh.Collapse.register(Ih,Fh);const Uh=`${uh.core.ns.selector("breadcrumb")} ${uh.core.ns.selector("collapse")}`;class $h extends uh.core.Instance{constructor(e){super(e),this.collapse=uh.core.Instance.getInstances(e,uh.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(uh.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),uh.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new uh.core.Initializer(Uh,[()=>{const e=[],t=document.querySelectorAll(Uh);for(let n=0;n<t.length;n++)e.push(new $h(t[n]))}]);const Bh=uh.core.ns.selector("btn"),qh=uh.core.ns.selector("btns-group"),Vh=uh.core.ns.selector("btns-group--equisized");new uh.core.Initializer(qh,[()=>{const e=document.querySelectorAll(Vh),t=[];for(let n=0;n<e.length;n++)t.push(new uh.Equisized(Bh,e[n]))}]);const Wh=uh.core.ns.selector("modal"),Hh=uh.core.ns("modal"),Qh=uh.core.ns("no-scroll"),Kh=uh.core.ns("scroll-shadow"),Gh=uh.core.ns.selector("modal__body"),Yh=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),Xh=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),Jh=(e,t)=>{if("hidden"===window.getComputedStyle(e).visibility)return!1;for(void 0===t&&(t=e);t.contains(e);){if("none"===window.getComputedStyle(e).display)return!1;e=e.parentElement}return!0};class Zh{constructor(e,t){this.element=null,this.activeElement=null,this.onTrap=e,this.onUntrap=t,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(e){this.trapped&&this.untrap(),this.element=e,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){Jh(this.element)?this.trapping():uh.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const e=this.focusables;e.length&&e[0].focus(),this.element.setAttribute("aria-modal",!0),window.addEventListener("keydown",this.handling),this.stunneds=[]}stun(e){for(const t of e.children)t!==this.element&&(t.contains(this.element)?this.stun(t):this.stunneds.push(new em(t)))}handle(e){if(9!==e.keyCode)return;const t=this.focusables;if(0===t.length)return;const n=t[0],r=t[t.length-1],o=t.indexOf(document.activeElement);e.shiftKey?!this.element.contains(document.activeElement)||o<1?(e.preventDefault(),r.focus()):(document.activeElement.tabIndex>0||t[o-1].tabIndex>0)&&(e.preventDefault(),t[o-1].focus()):this.element.contains(document.activeElement)&&o!==t.length-1&&-1!==o?document.activeElement.tabIndex>0&&(e.preventDefault(),t[o+1].focus()):(e.preventDefault(),n.focus())}get focusables(){let e=[...this.element.querySelectorAll(Yh)];const t=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(t.length){const n={};for(const e of t){const t=e.getAttribute("name");void 0===n[t]&&(n[t]=new tm(t)),n[t].push(e)}e=e.filter((e=>{if("input"!==e.tagName.toLowerCase()||"radio"!==e.getAttribute("type").toLowerCase())return!0;const t=e.getAttribute("name");return n[t].keep(e)}))}const n=[...this.element.querySelectorAll(Xh)];n.sort(((e,t)=>e.tabIndex-t.tabIndex));const r=e.filter((e=>-1===n.indexOf(e)));return n.concat(r).filter((e=>"-1"!==e.tabIndex&&Jh(e,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),window.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class em{constructor(e){this.element=e,this.hidden=e.getAttribute("aria-hidden"),this.inert=e.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class tm{constructor(e){this.name=e,this.buttons=[]}push(e){this.buttons.push(e),(e===document.activeElement||e.checked||void 0===this.selected)&&(this.selected=e)}keep(e){return this.selected===e}}class nm extends uh.core.DisclosuresGroup{constructor(){super(),this.trap=new Zh}apply(e,t){super.apply(e,t),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const rm=new nm;class om extends uh.core.Disclosure{constructor(e){super(e),this.body=this.element.querySelector(Gh),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new uh.KeyListener(this.element),this.keyListener.down(uh.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(e){this.body&&this.body!==e.target&&!this.body.contains(e.target)&&this.conceal()}gather(){rm.add(this)}disclose(e){return!!super.disclose(e)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(e,t){return!!super.conceal(e,t)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(uh.core.removeClass(document.documentElement,Qh),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(Qh)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",uh.core.addClass(document.documentElement,Qh))}resize(e,t){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?uh.core.removeClass(this.body,Kh):uh.core.addClass(this.body,Kh):uh.core.removeClass(this.body,Kh),this.isMedium=window.matchMedia("(min-width: 48em)").matches,e&&(this.isMedium?this.body.style.removeProperty("max-height"):(this.body.style.maxHeight=window.innerHeight-32+"px",uh.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"})))))}static get type(){return uh.core.DISCLOSURE_TYPES.opened}static get selector(){return Hh}get GroupConstructor(){return nm}}uh.Modal=om,uh.ModalsGroup=nm,uh.FocusTrap=Zh,new uh.core.Initializer(Wh,[()=>{om.build(document)}]);const im=uh.core.ns("nav"),am=uh.core.ns("nav__list"),lm=uh.core.ns("nav__item"),um=uh.core.ns("nav__item--align-right"),sm=uh.core.ns("menu");class cm extends uh.core.DisclosuresGroup{constructor(e,t){super(e,t),this.menus=[],this.navList=t.querySelector(`.${am}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return im}add(e){super.add(e),e.element.classList.contains(sm)&&this.menus.push(new fm(e,this.navList.getBoundingClientRect().right))}focusOut(e){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(e){-1===e&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=e}resize(){const e=this.navList.getBoundingClientRect().right;for(const t of this.menus)t.place(e)}}class fm{constructor(e,t){this.initialize(e),this.place(t)}initialize(e){this.element=e.element;for(const n of e.buttons)if(n.hasAttribute){this.button=n.element;break}let t=this.element.parentElement;for(;t;){if(t.classList.contains(lm)){this.item=t;break}t=t.parentElement}}place(e){const t=getComputedStyle(this.element),n=parseFloat(t.width);this.button.getBoundingClientRect().left+n>e?uh.core.addClass(this.item,um):uh.core.removeClass(this.item,um)}}uh.Navigation=cm,uh.Collapse.register(im,cm);const dm=uh.core.ns.attr("theme"),pm=uh.core.ns.attr("transition");class hm{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const e=this.root.getAttribute(dm);"dark"===e||"light"===e?this.scheme=e:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(pm)?(this.root.removeAttribute(pm),this.root.setAttribute(dm,"dark"),setTimeout((()=>{this.root.setAttribute(pm,"")}),300)):this.root.setAttribute(dm,"dark"):this.root.setAttribute(dm,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(e){e.forEach((e=>{if("attributes"===e.type&&e.attributeName===dm){const e=this.root.getAttribute(dm);"dark"===e?localStorage.setItem("scheme","dark"):"light"===e&&localStorage.setItem("scheme","light")}}))}}uh.Scheme=hm;const mm=`input[name="${uh.core.ns.selector("radios-theme","")}"]`,ym=uh.core.ns.selector("switch-theme","#"),gm=uh.core.ns.attr("theme");class vm{constructor(){this.attributeName=gm,this.theme=null,this.radios=document.querySelectorAll(mm);for(var e=0;e<this.radios.length;e++)this.radios[e].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(e){e.forEach((e=>{"attributes"===e.type&&e.attributeName===this.attributeName&&this.apply()}))}apply(){const e=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var t=0;t<this.radios.length;t++)this.radios[t].checked=this.radios[t].value===e;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(mm+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new uh.core.Initializer(`:root[${dm}]`,[()=>{new hm}]),new uh.core.Initializer(`${ym}`,[()=>{new vm}]);const bm=uh.core.ns("sidemenu"),wm=uh.core.ns("sidemenu__list");uh.Collapse.register(bm,wm);const km=uh.core.ns.selector("table"),Sm=uh.core.ns("table--no-scroll"),Em=uh.core.ns("table--shadow"),xm=uh.core.ns("table--shadow-left"),Cm=uh.core.ns("table--shadow-right");class _m{constructor(e){this.init(e)}init(e){this.table=e,this.table.setAttribute(uh.core.ns.attr("js-table"),"true"),this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0;const t=this.change.bind(this);this.tableElem.addEventListener("scroll",t)}change(){const e=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let t=this.tableElem.offsetWidth>this.table.offsetWidth;e||t?this.table.classList.contains(Sm)||this.scroll():e!==this.isScrollable&&this.delete(),this.isScrollable=e,t=!1;const n=this.caption.getBoundingClientRect();this.table.style.setProperty("--table-offset",n.height+"px")}delete(){uh.core.removeClass(this.table,Cm),uh.core.removeClass(this.table,xm),uh.core.removeClass(this.table,Em),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){uh.core.addClass(this.table,Em),this.setShadowPosition()}setShadowPosition(){const e=this.getScrollPosition("left"),t=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",e),this.setShadowVisibility("left",t)):(this.setShadowVisibility("left",e),this.setShadowVisibility("right",t))}getScrollPosition(e){let t=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(t=-1),e){case"left":return this.tableElem.scrollLeft*t;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*t;default:return!1}}setShadowVisibility(e,t){t<=1?"left"===e?uh.core.removeClass(this.table,xm):"right"===e&&uh.core.removeClass(this.table,Cm):"left"===e?uh.core.addClass(this.table,xm):"right"===e&&uh.core.addClass(this.table,Cm)}}uh.Table=_m;const Pm=[],Om=()=>{for(let e=0;e<Pm.length;e++)Pm[e].change()};new uh.core.Initializer(km,[()=>{const e=document.querySelectorAll(km);for(let t=0;t<e.length;t++)Pm.push(new _m(e[t]));window.addEventListener("resize",Om),window.addEventListener("orientationchange",Om),Om()}]);class Lm extends uh.core.DisclosureButton{apply(e){super.apply(e),this.hasAttribute&&this.element.setAttribute("tabindex",e?"0":"-1")}}const Nm=uh.core.ns.selector("tabs"),Tm=uh.core.ns("tabs"),zm=uh.core.ns("tabs__tab"),Rm=uh.core.ns("tabs__panel"),Am=uh.core.ns("tabs__list");class jm extends uh.core.DisclosuresGroup{constructor(e,t){super(e,t),this.list=t.querySelector(`.${Am}`),t.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),uh.core.engine.renderer.add(this.render.bind(this))}static get selector(){return Tm}transitionend(e){this.element.style.transition="none"}init(){this.keyListener=new uh.KeyListener(this.element),this.keyListener.down(uh.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(uh.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(uh.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(uh.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(zm)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(zm)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(zm)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(zm)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let e=0;e<this._index;e++)this.members[e].translate(-1);this.current.element.style.transition="",this.current.element.style.transform="";for(let e=this._index+1;e<this.length;e++)this.members[e].translate(1);this.element.style.transition=""}add(e){if(super.add(e),1===this.length||e.disclosed)this.current=e;else{const t=this.members.indexOf(e);this._index>-1&&this._index!==t&&e.translate(t<this._index?-1:1,!0)}}render(){if(null===this.current)return;const e=Math.round(this.current.element.offsetHeight);this.panelHeight!==e&&(this.panelHeight=e,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class Dm extends uh.core.Disclosure{static get type(){return uh.core.DISCLOSURE_TYPES.select}static get selector(){return Rm}get GroupConstructor(){return jm}buttonFactory(e){return new Lm(e,this)}translate(e,t){this.element.style.transition=t?"none":"",this.element.style.transform=`translate(${100*e}%)`}reset(){this.group.index=0}}uh.Tab=Dm,uh.TabButton=Lm,uh.TabsGroup=jm,new uh.core.Initializer(Nm,[()=>{Dm.build(document)}]);const Mm=uh.core.ns.selector("header"),Im=uh.core.ns.selector("header__search"),Fm=uh.core.ns.selector("header__menu"),Um=uh.core.ns.selector("header__tools-links"),$m=uh.core.ns.selector("header__menu-links"),Bm=`${Um} ${uh.core.ns.selector("links-group")}`;class qm{constructor(e){this.header=e||document.querySelector(Mm),this.modals=[],this.init()}getModal(e){const t=this.header.querySelector(e);if(!t)return;const n=uh.core.Instance.getInstances(t,uh.Modal);n&&n.length&&this.modals.push(new Vm(n[0]))}init(){this.getModal(Im),this.getModal(Fm),this.linksGroup=this.header.querySelector(Bm),this.toolsLinks=this.header.querySelector(Um),this.menuLinks=this.header.querySelector($m),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge?this.modals.forEach((e=>e.disable())):this.modals.forEach((e=>e.enable())),null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}class Vm{constructor(e){this.modal=e}enable(){this.modal.element.setAttribute("role","dialog"),this.modal.element.setAttribute("aria-labelledby",this.modal.primary.element.id)}disable(){this.modal.conceal(),this.modal.element.removeAttribute("role"),this.modal.element.removeAttribute("aria-labelledby")}}uh.Header=qm,new uh.core.Initializer(Mm,[()=>{const e=Array.prototype.slice.call(document.querySelectorAll(Mm)),t=[];for(const n of e)t.push(new qm(n))}]);export{rc as P,M as R,tf as a,Ks as b,eh as c,Ad as d,Xp as e,Gp as g,e as r,af as u,lh as v}`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class y{constructor(e=[]){this._todos=e}async add(e){this._todos.push(e)}async retrieveAll(){return this._todos}setTodos(e){this._todos=e}getTodos(){return this._todos}}const h=n({name:"todo",initialState:{items:[],isFetching:!1,isAdding:!1},reducers:{startedToAddTodo:(e,t)=>c(i({},e),{isAdding:!0,items:[...e.items,t.payload]}),successfullyAddedTodo:e=>c(i({},e),{isAdding:!1}),startedToFetchTodos:e=>c(i({},e),{isFetching:!0}),successfullyFetchedTodos:(e,t)=>c(i({},e),{isFetching:!1,items:t.payload})}}),m=l({[h.name]:h.reducer}),b=e=>u({reducer:m,middleware:p({thunk:{extraArgument:e}})});export{y as I,b as c,h as t}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 2
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js](https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js](https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css](https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js](https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css](https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>wOFF\x0000\x0001\x0000\x0000\x0000\x0000\x001d0\x0000\x000b\x0000\x0000\x0000\x0000;�\x0000\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000GSUB\x0000\x0000\x0001\x0008\x0000\x0000\x0000[\x0000\x0000\x0000�#|(jOS/2\x0000\x0000\x0001d\x0000\x0000\x0000B\x0000\x0000\x0000VY\x000eC�cmap\x0000\x0000\x0001�\x0000\x0000\x00024\x0000\x0000\x0006Ʒ�S4glyf\x0000\x0000\x0003�\x0000\x0000\x0014N\x0000\x0000(����zhead\x0000\x0000\x0018,\x0000\x0000\x00000\x0000\x0000\x00006\x001e\x0018\�hhea\x0000\x0000\x0018\\x0000\x0000\x0000\x001e\x0000\x0000\x0000$\x0008�\x0004Hhmtx\x0000\x0000\x0018|\x0000\x0000\x0000\x0016\x0000\x0000\x0001|��\x0000\x0000loca\x0000\x0000\x0018�\x0000\x0000\x0000�\x0000\x0000\x0000�ڳ�\x0000maxp\x0000\x0000\x0019T\x0000\x0000\x0000\x001d\x0000\x0000\x0000 \x0001s\x0000pname\x0000\x0000\x0019t\x0000\x0000\x00011\x0000\x0000\x0002.D\x001dI�post\x0000\x0000\x001a�\x0000\x0000\x0002�\x0000\x0000\x0005�\x0015]�x�c`d``�b0`�c`rq�	a��I,�c�b`a�\x0000�<2�1'3=��\x0003�\x0003ʱ�i\x000e 6b`\x0002�%\x0001\x0016�\x0006�\x0008�H�(0�\x0013(\x001e�\x0010�\x0010\x000b$��4#P}8C4\x0000��\x000b)\x0000x�c`d�e��������ك��a\x0005�fr`�b4\x0005�\x000c��\x000cXA@�k</p><p>�\x0003��P�\x0017�-\x0018r�_0�\x0000</p><p>3��\x0000�\x0005\x000c,\x0000\x0000x���IOTa\x0014���B��8�8ጊ��<� ����\x000c�!$�X���s�`��Zuܹ�C@s�ͩ\x0002��^\x001b�\x0016����;�)�6��^\x0006��f��\x000f��'->1�\x001a��b�M�4���v��>�\x001aJ�\x0017,��</p><p>?��"�,��z����~v��]���\x000c�����]\x001c� C���\x000cs��\x001c�8'\x0018�$�8�\x0019�r��r��\b��\���unp�[��\x000ew��}\x001e�G<�	Oy�s^�W��
o�`�wL�i>��3��/|�����\x001c�\x001e��/s�˵P/�ݧ�|���Z�U����k�^Z���7�g�Q��F
�\x0016+�\x001e��{�Q#nD
�\x0019��[��EGm��[��6[Qۭ��Wx�Px�Px�Px�PT\x001a\x0014�G\x00145��;��ۊ�{��\x001b�»��[�����2��Σ���p\x000eP8\x0011(�
\x0014N	</p><p>�\x0005����\x0019B�4�p�P8a(�5\x0014N\x001d</p><p>�\x000f���D�t�pNQ8�(�]\x0014N1</p><p>�\x0019E5��\x0019Gᴣp�Q�\x0001P�\x000bP�\x0015P�\x001fP�)P�3P�=P�GP�QP�[P�eP�oP�yP��P��P��P��P��P��P��P��P��P��P��P��P��P�\x0005Q�\x000fQ�\x0019QT�\x0015nK\x0014�M\x0014nP\x0014�R\x0014�\x0011</p><p>�+</p><p>7-</p><p>w.</p><p>��\x0000�7�x��:\x000bp\x001bez��J+?���j��R,���X~i��_�Cl�y:v��\x0004�	��\x0004BhrI\x0008!�|\x0001'�\x0004\x0007S��k�����\x000e��]���\x001d53=�pp��dz\x000cmӛ9Jg(e8\x001f�t����W�eG\x0006g:��կ��{��{�p\x000c��Ӻ
�)��T1�\x000cC|�U�.3�\x0006�J�H�e�`(���\x000f\x0006
�ɇ|a⇁�X�\x001d<s�����5\x0007\x000f���G\x0017[6�]��]�ꙿ}����~�p��e8J�1���ܸ�uժ���pa���</p><p>2k�
\x000c�wf(��P�\x0001%�H\x000cR���pWj ��\x0000\x0013<,s;\x001b�?L|vb1\x0012�\x0017�{��ŚE�F\x0008%nl�Ўۆz�SO<��\x001d~��\x0017;ۊ����\x001d�=<��\x0015&S\x0007Y\x0015\x001c</p><p>\x0006���K������MY\x0000�r�z���j
�+��@Ϛ�\wg�r���i������;��?MA���`��\x0018��;�B�;\x0000�\x0011�\x0005Yp	��+P��	\x000f&��;N�n�;�G�Ǖx"\x0007�g���\x0011\x0008�\x0002;v��\x001e�)\\x001cW����D���\x000e�,\x0006���~\x0002t2�,�\x001d���2;\x0002��x�iE�&S�W�|��\x001b��1fF`�\x0019&�X�8\\x000e<�\x0010��r�\x001c�7;N>��b�lOqY��|`\x0010+�\x0006\x0015E��gVXi5\x001a���\K�јܧ(d8�@RtY�-L\x0019S�\x000b\x0003q\x0010\x000edi�w.$�\x0000W�>�Sr�}�����B�\x0012i����b�\x0018�M�|\x0012\x0002	�gIQT=�\x001e��"�8>ANE�߳�q��'�nD�&!��\x000e^�V�T�"d�\x0017Qu����u\x001fq\x0002�& Tb�'"9��N~��\x0007�dJQg��\x00149\x0015eX��\x0018{\x0005$��'\x0001g \x001aD\x0003!�</p><p>�G�_\x0007���8{"���\x0008	�rm�%�]�\x0005OOD\x0014\x000e	H���\x0012\x0011�
�\x0019Q���\x0004�LDH'���F$��Q`ߡ��ݬ=�\x0002��"B:H8��\x0017��O$�\x0008p��L��B9\x0015'�\x0005%��Z���9~@��\x001d�pUJ2���pn~��}+ŏ����J���\x0003ݬ'5 �����O�>�tV�����'\x0011�:\x0005�\��S0����Q~�\x0019�y�J폒��S��l��\x0007c0��3O�	�\x000c\x0001\x0019\x001bس��c�H>�ޡ�.��dtd��a��\x0007S�$o�\x0008��\x0005]��]\x0006	U0L��l�A�=\x0001"��6��\x001flC��\x0008�</p><p>��M�=!��O�m��&��<A�հ`�	\�MH$\x0004\x001bh|���\x0003��2#2.F\x0002\x001a\x0000��\x0006n��jp�;�\x0011�%�avp�q��xR\x0008��\x0018W\x0015S\x0012�׸*D3{�"����</p><p>uO�\x0001��a���,\x0007�\x0001�.��\x0004���\x0015�soDtI!y\x0005�+{%N�X��{��'2>M�Ѿ���\x001f��^�~��hd���j�+\x0019��\x001exE��~#�_f�3B�F�\x0016$�%x$�</p><p>���Ry��:�"\x0014����H<�U$���\x0015�Nd�"�d&�!y����6��p���\x0017骩������pත��x����[9��PP�\x000f��_R@�az�^�m���4e�\x0015_uK���#�(�d\x0017�����c�3ܩ\x0016��\x0015X\x000b��\x000b</p><p>�\x001f��#�\x00057ΤuYǳ?A�L��\x0019�H�\x0013p`��_D��M\x001d\x0018��S��\x0018��/\x0012�90\x001dɐ3\x0000�\x0003\x0019������\x000c��KF"�o�GS���S�4.�)gl\x000cI!\x0011<V.�9bc�tt�T�&(Gd�OGϓ��<9T-&\x0007	=[H\x0004����LD'��9	`۲V0ٹ\-�L7!��\x0010\x0006
� �p�*���#\x0013�#�OD\x001e���_������\x00056�����s�4.f�������\x001f��|\x000e.����u\x0018�����o��ӹ\x0004���vS��\x001cp`��\x0017ןPlB�\x000b�N�̨\x00070�C )A_�~\x0002n�z�L�;�Cdõa��\x0010�\x0003\x0017�\x000e�^6�J�M��L\x0006~�\x001dT�Ե\x0001\x0006%\x000bG���\x0012�Ф}�r��1E\x000c\x0013�\x0008��� b���	����:�n�!��O!gHcD�N^���
���a��L\x0001c\x0004Kt\x0005Hз\x00022\x001d\x0003M\x0016�f�M���&��\x0008M��	�J�R�L~��u��)E[�� .\x0000���1��\x000f��\x001aS\x0006X\x001cgu\x0011�i4\x0002LSrw\x0006fZ�i�[�1��#�m��t��a��&1�L�O���曲z���]K�{e1�r(uB\x0001�f����gJ06\x0013\x0001sb9+��nP"�9\f\x0012�2��ܧ�bE} BN�^��!�NS�9+�@u>�w��<�></p><p>���EX�ى��N\x0015�=a\x0002q�J �Ɉ�@�ih~%4��;u��S������/R�#���}�jQ\������\x001b�
�io�s\x0002/ag���҅\x0017������[�ӟ��꽽}w���뭟\x001b=��</p><p>\x0017%�\x0015.��{\x0010���\x00143v�
���n�:�!)\x0004�\x0010\x0016xv6\x0018���\x0001>D���!�\x0004�\x001fg��vV�
\x0004>\x000c�7\x000f���Ǘʗm[�t����sɗ�n�x���v�zGw�s\x0014V~|�h</p><p>�u��z�Ra��������e�jݤ�4����\k�{�>��鎧����s�ƣk�>���?ZY�X�{���\x0005�ڀ�x0ڳmGl����~�џ\x001f{�.�3��u{\x0013��_^��Z\x0007_�)
�\x0013�O�\x0006`m\x0002�:6"\x001b\f<�\x0000�ؔ~�\x000c�qtllt���UuB�9둣o�V�\x0012je�����}��\x000cO޻sT�?^fq\x000eO�\x0017J\x001f�{�q�?����41� MT�`F'���W\x001a=T]�%\x0002MF����2-��-}^o�����_�>\x0018\Y\_�7�GQ��B��\x0016*�ʝΒB��rŗ�θ�p\x001b����f�׼u;(U{G1�U�4.�Zܖe\x001c����[�;�(�\���\x0002x*\x0006/\x0000�G�i\x0011�����D:߄R)\x0016�s�	t�`d�M-��_�/\x001cgx��h��A�\x0003r\x0008RZ��
\x0000\x001d\x0000ޠ�g�\x0002�\x0018D�"H=�/�m\x000e&L�VDC&\x0011��5�\x0011l��b2�\x0004f�W���</p><p>����\x0001�#�RCRi\x000e	1�\x0005\x000834�f-6�O\x0000��Z6m2</p><p>�\x0015Z��\x001e\x0007��k�\x0012GVjN��\x0019 �\x001e
\x000e@\x001cN�W��4 �/���P�d��r*C�Yq�\x00145�PG̐�Z-|\x001d�\x0016�$m\x0004!�ն��*�D���\x000c�u^�f�2g�\x000f\x0011U\x0004��xe�5�\x0003�\x0000[1��y�N�z0\x001e�h��"�e�\#$�t\x0000*�\x0003&��\x0012���>;\x0017���\x0004\x0011A�M�$փ�(Nk&ݼ��&cR)6v��b\x0012ԙ�\x0016�4\x001a7��41\x001dL��Bc\x0006D
N�</p><p>\x0010�-\x0006#\x0007Z�;%����Zz�!(̅�rP�⃦\x0012n�u�\x000b�3��	;8Rm�%2�Q�XBXN�8\x001a��y�rM��:�f͡3x!�-��_}=�E\x0008Kk6,�?k2��\x0003��r\x0004�ޞ�?��d\x0005�\x0005��
'�Fs%*��b\x0017H�#ъ=�������p�8�<\x0018�U�\x0016\x000bJ��}�\x0014�7.�j,5��\x0016Yf���t;�EɟW��w64�N�fCI�B�*�/+%�r˻ΒJS�s��=�r���ZQ�\�9�Љ��2�2��T̪\x0015\x001eO\x0005�V@٫�ЋYY%�\x000c>�1���4�L\x0013j�\x00044\x0008\x0007\x0001�\x0004�`(Oq��S�\x001ae�$�q��\x001b�z� �*m��[��kelo�+�1C�㲰ק>JF\x001a|����U˲{�\x001c�|�wu��3���\x0015�\x0005\x001c>�����g\x0005ņ�\x0003"�*\x0012&�FHe!d7���H�+ p���=�.\x0010��\x0010D&�́@sɚ��ۆN��bٚh�˵��C�%MNgS4J6/�X���\x0012m>y�$L��C�
\x000e��6>tr���T����Mш:��07Ӊ��\x001ds�\x0010}���h����A���&���2و���e_F؂�����'��
M</p><p>U�8�6A-�^\x0013��o\x0017��E�|>j\x0006]>-\x0010�hp��6~\x001d\x0015zZ�\x0008.��f\x0011J�`��!^JҢ\x0004��D\x0001��&,��b_Ĕ�]���Ƕ�\x0014C��</p><p>0�}����$9�z�r��Ȳ
�IφTi#�q\x000bă\x001b���ّ�f������{���\x00049F\x000e�\x0007=�~�(�\x001f\x0000�? \x001b��\x0004a.� �1\x0006�'K��I�hq�\x000e&_�O��\x0012�ZҞ�;{�\x0012�t	��A�o\x0016
.g1�Ђ��T�p�\x001au������K\x000e.\x001e��T���?�bQ�C��h\x0005'����x�@�u�\x00053�����\x0002_X���\x0017�<�\x0017xfA������h���\x0002��:\x0007^i�"�\x0001�f</p><p></p><p>�<��dIu]4\x0008��<���r�d�
�\x0007\x0010!���\x00084�\x001dp@\x0006��ai� �i\x001c��.�\x001c \x001f\x001aLv)�\x000bm"�C��\x001c)\x0006J��\x000c\3v2�\x0015�M��\x0004\x001b�y�6θ@�\x0002L\x000bd\x0004\x0010\x0019�\x000c�kK��:"h���f��)\x0015\x001c�t�\x001b��7��b\x001a��x��(���Z�%�~,��&i�8�-�|ĩ���Bȴc��b1(�\x0017�qM��\x0016:H�m�D\x0014��\x000e�ǅ\x0001Q^$���,l�ٺޟ7�on����ؖ^���_Ժi���s���؜y��56a}��/r����ࢥ �K��R��#\x00037�
�\x0004{���ڬ\x001f�����XX�^����������>�i�Ԯ��j�\x00076�\x00141\x000b�g\x0017#/�Y\x0008(�\x000c"T݂�T�\x001b؀\x000cչ�\x000b���pH����\x001b�[�yw{���\x0015?&R�9������&z���兑?]��9��~�f�5�c��ܓ�\x000c��,����\x0006�7d�)�.��\x000b��y�ؑ#�~|�-&S����{��{O��C���;r���՚L=�I����¶�o�\x001c���������0۲29�_Yi�?\x000f�'F��l~��*�\x0012���`���(��e�\x001a\x0013>+\x0019O��h�\x001d��8�\x0005�z-�ű\x0019��..\x0003+��b'�
РXq�9Gv�F�\x0010\�2�|�GA��HL��C\x0007�6N$���x��T�>\x0002�\x000e�OL��|�\x0000�h��b����\x000c\x000bϝ�\x001a��1��F�;:�G����"�6ə�8x`�\x0013���`6~\x0005TC�\x0004\x0016X\x0003Ԃ!@\x0016��~\x0003�o7ə|�&+]c�/���\x0005\x0004l�\x0014�Ǻ29
]/7�=��L�P�\x0018ߡ4Nv�)��\x0005@�ʔ\x001f����7��\x0015�\x001f=#I=.��4�K�'�o�\|\x0008�c!�9\x0015\x0014E�\x0019�#t�P�=\x001a�+�\x0006ࢇw����2\x0006.��d\x001e�d�ʨ�����8��`���[��\x001f��\x0008\x00125�K��E\x0007�t\x0010k��P��/?�m�Z0k (�\x0010o��H�`</p><p>���G\x0012��\x0013y�6\x000f�=��>T �\x001bhY�h,</p><p>G�&\x001el]����\髓�u\x001b�\x001b��}kV�Ֆ��[�\x001d�׻��\x0013f�.ϳ�W��~q��n�\x001b#�+�C���k��^P�߹���\x000b\x001a���\x001d\x0003���]d�O��fn5d���Cf$X/4\x0012�ċV|Ff"�4=(T}��i��v&}8��5�I=��g�lR�U"�X�7���ֺ�}�Ť�w�������l.���'\x0003g'�f[�</p><p>����<\x0012>x�X�2|�\x0011l\x0019�\x001b|U��:�1��K(\x0016��VK��%l�p�����P^U~����֮��}�TVY"N�{ h�\x0013�3��\x0015ծ\x001f=z|S�|YA^ȥ+�J:�-�z`��'�\x00130�\x001c��\x000bq\x001fq��o<\x00181�8�\x0002k�|Ƴ�[�wkG����2� �LͻC\x0007i_N�\x0017"�<��9K̍}^�x�\x0014%�w�{#Q�s?�ɢo��f.J����h2�/��B����\x0019�\x001b�;�&F�\x0014�^BW�B0\x0005Ē+S��H>o,��+6��u�Y�]+���v�*��Y\x0013l�ֱ|Q��yE<�����rKc`GEO�XOWGkJ^\x001an=d�X\x0013\x001a\�,JK��=��\x000f��;_M\x0008;v.~NZ</p><p>5�\x001c^�rp.&�z�yv\x0017\x0012��F���K�K�"��\x001a�t)�S</p><p>��]�g22x9%�����|�3�\x0008`\x001e\x0011�K`>%\x001a\x001dc)=�/U\x0013�\x000b\x0014#�L.F{z�o�\x000e�65���Q�_F;_�}�k��M\x001f\x001c;�o�r���2tj:�zsZ���Ee�\x0008ы��k(�����W\x0005�5dyĊΗ:W#�pQ׊�\x0013�W��QE((SGk'���\x0002\x0005�\x000e�t:� �_\x001dxq`���\x0011O�?\x001f\x001c^��d�f&\x0017�\x001e���5�`�I[ZX\x0010t�<��\x0008�=Ҽi���W��\x0005~8�\x0011\x0000\x0000x�c`d``\x0000�-��z��m�2p�l\x0000�0�U��E��-X�1o\x0003r9\x0018�@�\x00007$</p><p>�x�c`d``~�߂��e\x0003\x0003\x0010��c`d@\x0005�\x0000`;\x0003�\x0000\x0000x�c````�0���>��'\x0004\x0000R�<\x0015\x0000\x0000x�c`\x0000\x0002\x001f�\x0013�2�&�)��\x0018�0�`|���I�I�Ƀ)���i\x001a�:�cL��٘\x001d�\x001bXDX4XbXְ<cu`�bmc��z��\x0007�\x0012[\x0018�</p><p>�\x001b�.�k��qDp�q����S�3�s\x0001�'�\x001c�#�B�
܇xxx�x�x\x001axf��U�������/�o\x001e?\x000f\x0002�2�3�\x0004�\x0004�\x0004\x001a\x0004�\x0008�\x0008�\x0012�$�#�%tA�G8@x�\x0008�H\x0004:\x0004\x0000nF2C\x0000\x0000\x0000x�c`d``�gHa�b\x0000\x0001& �\x0002����\x000c\x0000\x001c�\x0001�\x0000\x0000\x0000x�m�=N�0\x0018���\x000f�J\x0008\x0004ba�\x0002\x000bj�3vdh�\x000e���IS%q�\x0015�\x0003'�\x0010\x001c��3p\x0008\x000e�[�I�Pm�~���\x0017+	�k|!�q\x0004���8Z�`��mҍp�� ��\x0000��=��p\x001fϘ	\x000fp\x000b�'\x0004�K�;�</p><p>�p�7�6��p��!��=>�{���}��#<�S�4�\x001d汩���vEdO�D+m��Tj\x0012�Or�+m#�\x0013�>�f�M�KUjM��r�(�����؅\x001b���h��\x000fcS"A�\x0014\x0016C�aP�^�}3�P �ɹ�9�b���Za����\r�d��\x0011\x001c���5\x000e\\x001b�y�ֱK�N��4���t�ihj����Cl|W��6�L��C{�\x000b�5d,\x0000\x0000\x0000x�mT��0\x0010�KW���&�ޛ�t�t�w*c\x0011�\x001c\x0001q��\x0017݁
N�������\x001eP\x001b��S���Y�\x0000�`+�a;v`\x0010C\x0018�\x0008�\x0018�\x0018�1�ILa\x001a3؉]��\x001c�\x001b{�\x0017��\x001f\x0007p\x0010�p\x0018Gp\x0014�p\x001c'p\x0012�p\x001agp\x0016\x001e��<.�"\x0016p	�q\x0005Wq
�q\x00037q\x000b�q\x0007w��{��\x0007x�Gx�'x�gx�\x0017x�Wx�7x�wx�\x000f��O��/��o��\x001f��_��?X��Z]��Iu�\x0005�R]�B-�E������$>�\x0003�BI�	9�pkM�k��&>Y�q9Bɀ3fK<��٘���J�PE���\x0004+6\nUj��ň��|��+:��d�,�m�FY��x�qƨ�-B7����\x0018��-�x��I$��9��oI��\x000c��Y/���7��]_�X�ê</p><p>\x0017&����T2���Է�G\x0019��\x000e�fȾ2rڔ�&�^GX\x001d�e:�8j=�V\x000b�\x0018�2(7���\x0003&\x0008x�@��a�Je�~�Jf'���G\x0017W%j�$j�\x0010
E��\x000c،.�\x0017&ԁ��HB��"���PǉX�"⵺��mh�9�Y�E;%�.�ɼ�!�1\x0012�b�\x0010\x0019\x0012I�z\x000b��0�n���ՊB��Jlp\x001e!Zqۆ:3�?��.VS\x0019w��1ʲ2�2nqVA�X��[%D\x001d�RX��\x000bL7�i#����e8iɈS�I'L�M\x0015��g#�̈�Y3*��]6�,�#�4�+\x0002Y�\x000b�g��K���0i�687�?Jh����G\x000b�V�\x0007�\x0019�\x0000\x0000\x0000</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js](https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "import{a as e,r as t,R as r,b as a,P as n}from"./vendor.fa8ab5d7.js";import{c as l,I as o}from"./initilizeStore.cba4cea2.js";con", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="module" crossorigin src="/assets/formulaire.09fafdb9.js"></script>`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.cba4cea2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.09fafdb9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css](https://immersion.beta.pole-emploi.fr/assets/initilizeStore.6aa4e2b1.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css](https://immersion.beta.pole-emploi.fr/assets/main.c231f81c.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js](https://immersion.beta.pole-emploi.fr/assets/main.9fc9ea95.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741825`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000000`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `805306368`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741824`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js](https://immersion.beta.pole-emploi.fr/assets/vendor.fa8ab5d7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1073741825, which evaluates to: 2004-01-10 13:37:05</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

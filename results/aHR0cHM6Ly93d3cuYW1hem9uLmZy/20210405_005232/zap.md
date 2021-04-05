
# ZAP Scanning Report

Generated on Mon, 5 Apr 2021 00:48:27


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 10 |
| Informational | 11 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 6 | 
| Sub Resource Integrity Attribute Missing | Medium | 14 | 
| X-Frame-Options Header Not Set | Medium | 12 | 
| Absence of Anti-CSRF Tokens | Low | 10 | 
| Cookie No HttpOnly Flag | Low | 13 | 
| Cookie Without SameSite Attribute | Low | 13 | 
| Cookie Without Secure Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 3 | 
| Dangerous JS Functions | Low | 12 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 12 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Charset Mismatch (Header Versus Meta Content-Type Charset) | Informational | 12 | 
| Information Disclosure - Sensitive Information in URL | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Loosely Scoped Cookie | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 9 | 
| Storable but Non-Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 32 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/sitemap.xml](https://www.amazon.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/product-availability/](https://www.amazon.fr/dp/product-availability/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/common/du](https://www.amazon.fr/gp/customer-reviews/common/du)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/rate-this-item/](https://www.amazon.fr/dp/rate-this-item/)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=3635788031&ref_=nav_em_gno_groceryall_0_2_19_2](https://www.amazon.fr/gp/browse.html?node=3635788031&ref_=nav_em_gno_groceryall_0_2_19_2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/Qj4WA-TsmcpmPxizjOy8GEAAAAF4n3nOtAMAAAH4ATXn5jc/https://www.amazon.fr/stores/page/417FE605-E724-4DE0-9887-3A909954C37F?ingress=2&amp;visitId=1c84b6c1-2afb-43fc-b878-2a98fc464eff&amp;ref_=ast_bln" target="_top"><div id="bannerx0-root" class="root-bannerx0-base"><div id="bannerx0-copy" class="bannerx0-copy bannerx0-copy-base bannerx0-copy-layout"><div id="bannerx0-copy-content" class="bannerx0-copy-content bannerx0-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx0-copy-badge" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Pour tous les gourmands</div><div id="bannerx0-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">La chasse aux oeufs Lindt est ouverte </div><div id="bannerx0-copy-subtext" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Un moment inoubliable vous attends</div><div id="bannerx0-copy-cta" class="bannerx0-cta bannerx0-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>Commander maintenant</span></div></div></div><div id="bannerx0-product1" class="bannerx0-product1" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/416hQlUL6yL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-transition1" class="bannerx0-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=1571268031&ref_=nav_em__pets_0_2_17_15](https://www.amazon.fr/gp/browse.html?node=1571268031&ref_=nav_em__pets_0_2_17_15)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/QrG5RJTBrGyBO9Xh-HBUU7sAAAF4n3nNowMAAAH4ATR9yP4/https://www.amazon.fr/stores/page/87BDC638-4701-4AF2-A9FF-3C75A5ACEA85" target="_top"><div id="bannerx0-root" class="root-bannerx0-base"><div id="bannerx0-copy" class="bannerx0-copy bannerx0-copy-base bannerx0-copy-layout"><div id="bannerx0-copy-content" class="bannerx0-copy-content bannerx0-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx0-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">DentaLife®</div><div id="bannerx0-copy-subtext" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Prenez soin de ses dents au quotidien</div><div id="bannerx0-copy-cta" class="bannerx0-cta bannerx0-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>En savoir plus</span></div></div></div><div id="bannerx0-background_image" class="bannerx0-background_image" style="display:flex;height:100%;width:100%;overflow:hidden;align-items:center;justify-content:center;"><img src="https://images-na.ssl-images-amazon.com/images/I/A1cbe6vsokL.png" style="object-fit:cover;min-width:100%;min-height:100%;max-width:140%;max-height:140%;"></div><div id="bannerx0-transition1" class="bannerx0-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000](https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="same_window" href="https://fr.amazonforum.com" target="_self">Forum Num&eacute;rique et Appareils</a>`
  
  
  
  
* URL: [https://www.amazon.fr/b?node=11961843031&ref=sv_ap_gender_1_3_1_3](https://www.amazon.fr/b?node=11961843031&ref=sv_ap_gender_1_3_1_3)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu.amazon.fr/x/c/QhB0jAVa62ezTheeRT3d1Q4AAAF4n3ncUAMAAAH2AcKG8f8/https://www.amazon.fr/stores/page/8641E99F-42A3-49AC-BB4D-1614ED8F7E7A?store_ref=SB_A08168731IVI4CFI8U8FK&amp;pd_rd_w=rz8CS&amp;pf_rd_p=2c062caf-6881-41f4-9d9d-3ee6d075f290&amp;pd_rd_wg=P3lAS&amp;pf_rd_r=GNYJ2W6Y10ZNFBVZZPSB&amp;pd_rd_r=36819204-5a71-41c0-8880-1e1a9c3bf53f&amp;aaxitk=RwplJ0uz4NV.QvTovvcMpQ&amp;hsa_cr_id=9847877020202&amp;lp_asins=B08WLZ51S5,B076PG44M8&amp;lp_query=Portefeuilles%20et%20porte-cartes&amp;lp_slot=auto-sparkle-hsa-tetris&amp;ref_=sbx_be_s_sparkle_tsld_bkgd" target="_top" aria-label="Publicité sponsorisée à partir de Tru Virtu. HI-TECH RFID Wallets „Made in Germany“. En savoir plus sur Tru Virtu." data-click-el="bkgd" class="sb_1REHiRA7 sb_1G_Jnizf"></a>`
  
  
  
  
* URL: [https://www.amazon.fr/Elgato-Stream-Deck-Contr%C3%B4leur-Personnalisables/dp/B06W2KLM3S/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Elgato-Stream-Deck-Contr%C3%B4leur-Personnalisables/dp/B06W2KLM3S/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a aria-hidden="true" href="https://aax-eu.amazon.fr/x/c/Qjor5kFMm9YX9hxY77cDNC8AAAF4n3p0qwMAAAH2ATg3_Co/https://www.amazon.fr/stores/page/A85FC577-AE7E-489D-A78F-466D5574E3E6?store_ref=SB_A04519873SXLWL8ZMK8R7&amp;pd_rd_w=Hy1Wy&amp;pf_rd_p=5c06b918-9ae4-4b60-a5c8-f64c21204082&amp;pd_rd_wg=h8s3G&amp;pf_rd_r=ZJ9M3MD30GJ3RX3WJ1S5&amp;pd_rd_r=d3c82e51-0dce-4b97-92c0-e8718e7e1e63&amp;pd_rd_i=ad1&amp;aaxitk=JLdbdH43r2LFOhu2JwqHHA&amp;hsa_cr_id=9561718860702&amp;lp_asins=B088HHWC47,B088P2ZXFW,B088P2WK3B&amp;lp_slot=desktop-arbies&amp;ref_=sbx_be_dp_arbies_mblsd" tabIndex="-1" target="_top" class="sb_1REHiRA7 sb_Es4IY3ln sb_1QlM2Efn"><img style="width: auto; height: auto;" alt src="https://images-eu.ssl-images-amazon.com/images/S/gladiator-image-upload-prod/9/A13V1IB3VIYZZH/3eca724a6dfe2447d9e2b67187c3f1af._SL5000_CR0,476,5000,2616_SX460_QL60_.jpg" data-lazy-load data-src="https://images-eu.ssl-images-amazon.com/images/S/gladiator-image-upload-prod/9/A13V1IB3VIYZZH/3eca724a6dfe2447d9e2b67187c3f1af._SL5000_CR0,476,5000,2616_SX460_QL70_.jpg" data-srcset="https://images-eu.ssl-images-amazon.com/images/S/gladiator-image-upload-prod/9/A13V1IB3VIYZZH/3eca724a6dfe2447d9e2b67187c3f1af._SL5000_CR0,476,5000,2616_SX460_QL70_.jpg 1x,https://images-eu.ssl-images-amazon.com/images/S/gladiator-image-upload-prod/9/A13V1IB3VIYZZH/3eca724a6dfe2447d9e2b67187c3f1af._SL5000_CR0,476,5000,2616_SX920_QL70_.jpg 2x,https://images-eu.ssl-images-amazon.com/images/S/gladiator-image-upload-prod/9/A13V1IB3VIYZZH/3eca724a6dfe2447d9e2b67187c3f1af._SL5000_CR0,476,5000,2616_SX1380_QL70_.jpg 3x" data-click-el="lifestyle" class="sb_3yXEoTh7" /></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=197858031&ref_=nav_em_gno_beaute_0_2_18_2](https://www.amazon.fr/gp/browse.html?node=197858031&ref_=nav_em_gno_beaute_0_2_18_2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/QiYRd_yp9crE27S-SLGJ_W8AAAF4n3m7IgMAAAH4AWp1mbA/https://www.amazon.fr/stores/page/ECE35F73-497C-4305-9830-D9F22C01FD6A" target="_top"><div id="bannerx0-root" class="root-bannerx0-base"><div id="bannerx0-copy" class="bannerx0-copy bannerx0-copy-base bannerx0-copy-layout"><div id="bannerx0-copy-content" class="bannerx0-copy-content bannerx0-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx0-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Venez découvrir la brosse lissante ghd</div><div id="bannerx0-copy-cta" class="bannerx0-cta bannerx0-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>Commander maintenant</span></div></div></div><div id="bannerx0-product1" class="bannerx0-product1" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/41TNvGs9ACL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-transition1" class="bannerx0-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/01R8It1-pQL.css?AUIClients/ShoppingPortalAssets-cookieConsent" />`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="dns-prefetch" href="https://m.media-amazon.com">`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="dns-prefetch" href="https://completion.amazon.com">`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/11EIQ5IGqaL._RC|01ZTHTZObnL.css,41+YmaFjUoL.css,31qGOnSAToL.css,013z33uKh2L.css,017DsKjNQJL.css,0131vqwP5UL.css,41EWOOlBJ9L.css,11gKzVUTNZL.css,01ElnPiDxWL.css,11bGSgD5pDL.css,01Dm5eKVxwL.css,01IdKcBuAdL.css,01y-XAlI+2L.css,21N4kUH7pxL.css,01oDR3IULNL.css,31q1y1irc5L.css,21j0IlW7xKL.css,01XPHJk60-L.css,014OeDQisGL.css,21aPhFy+riL.css,11gneA3MtJL.css,21fecG8pUzL.css,01RddH8vm-L.css,01CFUgsA-YL.css,31C80IiXalL.css,11qour3ND0L.css,11tRp6+0HHL.css,11MrdqKlKnL.css,11oHt2HYxnL.css,013RDhw9hoL.css,11JQtnL-6eL.css,11RKoGSb-gL.css,11jtXRmppwL.css,01QrWuRrZ-L.css,21pIv-yKhaL.css,11QyqG8yiqL.css,01890+Vwk8L.css,11kwKGWmBfL.css,11F2+OBzLyL.css,11Y05DTEL6L.css,01cbS3UK11L.css,21F85am0yFL.css,01giMEP+djL.css_.css?AUIClients/AmazonUI&UZJpE8II#fr.page_type-Gateway.not-trident.305299-T1.263677-T2" />`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="dns-prefetch" href="https://images-eu.ssl-images-amazon.com">`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/01R8It1-pQL.css?AUIClients/ShoppingPortalAssets-cookieConsent" />`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="dns-prefetch" href="https://m.media-amazon.com">`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/41VuNbGfm5L.css?AUIClients/AmazonGatewayAuiAssets&/3eJPhjR#224544-T1" />`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="dns-prefetch" href="https://completion.amazon.com">`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/41VuNbGfm5L.css?AUIClients/AmazonGatewayAuiAssets&/3eJPhjR#224544-T1" />`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/41icwgAxVqL._RC|71nLq0lOl6L.css,21-QxUt197L.css,31YZpDCYJPL.css,21rlYHBw3OL.css,41OiMQkB+EL.css,01yCq3WXEcL.css,11kO7yAgiQL.css,31--iZEK8dL.css,01XHMOHpK1L.css,01ucgi+I44L.css,31IrUp1HMlL.css_.css?AUIClients/NavDesktopUberAsset&RCFg+BVw#desktop.language-fr.fr.309131-T1" />`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/41icwgAxVqL._RC|71nLq0lOl6L.css,21-QxUt197L.css,31YZpDCYJPL.css,21rlYHBw3OL.css,41OiMQkB+EL.css,01yCq3WXEcL.css,11kO7yAgiQL.css,31--iZEK8dL.css,01XHMOHpK1L.css,01ucgi+I44L.css,31IrUp1HMlL.css_.css?AUIClients/NavDesktopUberAsset&RCFg+BVw#desktop.language-fr.fr.309131-T1" />`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/11EIQ5IGqaL._RC|01ZTHTZObnL.css,41+YmaFjUoL.css,31qGOnSAToL.css,013z33uKh2L.css,017DsKjNQJL.css,0131vqwP5UL.css,41EWOOlBJ9L.css,11gKzVUTNZL.css,01ElnPiDxWL.css,11bGSgD5pDL.css,01Dm5eKVxwL.css,01IdKcBuAdL.css,01y-XAlI+2L.css,21N4kUH7pxL.css,01oDR3IULNL.css,31q1y1irc5L.css,21j0IlW7xKL.css,01XPHJk60-L.css,014OeDQisGL.css,21aPhFy+riL.css,11gneA3MtJL.css,21fecG8pUzL.css,01RddH8vm-L.css,01CFUgsA-YL.css,31C80IiXalL.css,11qour3ND0L.css,11tRp6+0HHL.css,11MrdqKlKnL.css,11oHt2HYxnL.css,013RDhw9hoL.css,11JQtnL-6eL.css,11RKoGSb-gL.css,11jtXRmppwL.css,01QrWuRrZ-L.css,21pIv-yKhaL.css,11QyqG8yiqL.css,01890+Vwk8L.css,11kwKGWmBfL.css,11F2+OBzLyL.css,11Y05DTEL6L.css,01cbS3UK11L.css,21F85am0yFL.css,01giMEP+djL.css_.css?AUIClients/AmazonUI&UZJpE8II#fr.page_type-Gateway.not-trident.305299-T1.263677-T2" />`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="dns-prefetch" href="https://images-eu.ssl-images-amazon.com">`
  
  
  
  
Instances: 14
  
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
  
  
  
* URL: [https://www.amazon.fr/Nintendo-Manettes-Gauche-Violet-Droite/dp/B07VGY2LWT/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-Manettes-Gauche-Violet-Droite/dp/B07VGY2LWT/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nouveau-Casque-sans-fil-Xbox/dp/B08WJSJT4J/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nouveau-Casque-sans-fil-Xbox/dp/B08WJSJT4J/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/New-Super-Mario-Bros-Deluxe/dp/B0055FFXQ6/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/New-Super-Mario-Bros-Deluxe/dp/B0055FFXQ6/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nouvelle-Manette-Xbox-Sans-Fil/dp/B087VLP2RT/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nouvelle-Manette-Xbox-Sans-Fil/dp/B087VLP2RT/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Seasons-Pioneers-Deluxe-Nintendo-Switch/dp/B08PPZF3TS/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Seasons-Pioneers-Deluxe-Nintendo-Switch/dp/B08PPZF3TS/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/GAME-WATCH-SM-BROS-SYSTEM/dp/B08GZ3DRLW/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/GAME-WATCH-SM-BROS-SYSTEM/dp/B08GZ3DRLW/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Manette-Nintendo-Switch-Pro-Monster/dp/B08V6MFT7Q/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Manette-Nintendo-Switch-Pro-Monster/dp/B08V6MFT7Q/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-51-Worldwide-Games/dp/B086FJVVLF/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-51-Worldwide-Games/dp/B086FJVVLF/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Seagate-Disque-Jeu-pour-Playstation/dp/B07PPNSFBK/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Seagate-Disque-Jeu-pour-Playstation/dp/B07PPNSFBK/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Bravely-Default-II-Nintendo-Switch/dp/B08R98DFL1/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Bravely-Default-II-Nintendo-Switch/dp/B08R98DFL1/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-0045496422950-Super-Mario-Party/dp/B07F8D6DCZ/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-0045496422950-Super-Mario-Party/dp/B07F8D6DCZ/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-Luigis-Mansion-3/dp/B07SC9136F/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-Luigis-Mansion-3/dp/B07SC9136F/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
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
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form
    id="nav-search-bar-form"
    accept-charset="utf-8"
    action="/s/ref=nb_sb_noss"
    class="nav-searchbar nav-progressive-attribute"
    method="GET"
    name="site-search"
    role="search"
  >`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sp-cc" method="post" action="/cookieprefs?ref_=portal_banner_all" data-bottom-offset="0" data-top-offset="0">`
  
  
  
  
* URL: [https://www.amazon.fr/sitemap.xml](https://www.amazon.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="a" accept-charset="utf-8" action="/s/ref=404_search" method="GET" role="search">`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name='ue_backdetect' action="get">`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name='ue_backdetect' action="get">`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form style="display: none;">`
  
  
  
  
* URL: [https://www.amazon.fr/dp/product-availability/](https://www.amazon.fr/dp/product-availability/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="a" accept-charset="utf-8" action="/s/ref=404_search" method="GET" role="search">`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sp-cc" method="post" action="/cookieprefs?ref_=portal_banner_all" data-bottom-offset="0" data-top-offset="0">`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form
    id="nav-search-bar-form"
    accept-charset="utf-8"
    action="/s/ref=nb_sb_noss"
    class="nav-searchbar nav-progressive-attribute"
    method="GET"
    name="site-search"
    role="search"
  >`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form style="display: none;">`
  
  
  
  
Instances: 10
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 2: "__mk_fr_FR" "twotabsearchtextbox" "nav-search-submit-button" ].</p>
  
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
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `i18n-prefs`
  
  
  * Evidence: `set-cookie: i18n-prefs`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
Instances: 13
  
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
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `i18n-prefs`
  
  
  * Evidence: `set-cookie: i18n-prefs`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id`
  
  
  * Evidence: `set-cookie: session-id`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `ubid-acbfr`
  
  
  * Evidence: `set-cookie: ubid-acbfr`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
Instances: 13
  
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
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/associates/join](https://www.amazon.fr/exec/obidos/subst/associates/join)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/refer-a-friend-login](https://www.amazon.fr/exec/obidos/refer-a-friend-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/partners/friends/access.html](https://www.amazon.fr/exec/obidos/subst/partners/friends/access.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/handle-buy-box](https://www.amazon.fr/exec/obidos/handle-buy-box)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-stuff.html](https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-stuff.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `i18n-prefs`
  
  
  * Evidence: `set-cookie: i18n-prefs`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/flex-sign-in](https://www.amazon.fr/exec/obidos/flex-sign-in)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/tg/cm/member/](https://www.amazon.fr/exec/obidos/tg/cm/member/)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-collection.html](https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-collection.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  * Parameter: `session-id-time`
  
  
  * Evidence: `set-cookie: session-id-time`
  
  
  
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=197858031&ref_=nav_em_gno_beaute_0_2_18_2](https://www.amazon.fr/gp/browse.html?node=197858031&ref_=nav_em_gno_beaute_0_2_18_2)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=1571268031&ref_=nav_em__pets_0_2_17_15](https://www.amazon.fr/gp/browse.html?node=1571268031&ref_=nav_em__pets_0_2_17_15)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=3635788031&ref_=nav_em_gno_groceryall_0_2_19_2](https://www.amazon.fr/gp/browse.html?node=3635788031&ref_=nav_em_gno_groceryall_0_2_19_2)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js"></script>`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/common/du](https://www.amazon.fr/gp/customer-reviews/common/du)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/write-a-review.html](https://www.amazon.fr/gp/customer-reviews/write-a-review.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/gp/gfix](https://www.amazon.fr/gp/gfix)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/gp/legacy-handle-buy-box.html](https://www.amazon.fr/gp/legacy-handle-buy-box.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.amazon.fr/gp/flex](https://www.amazon.fr/gp/flex)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/dp/product-availability/](https://www.amazon.fr/dp/product-availability/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/sitemap.xml](https://www.amazon.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/rate-this-item/](https://www.amazon.fr/dp/rate-this-item/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/common/du](https://www.amazon.fr/gp/customer-reviews/common/du)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/item-dispatch](https://www.amazon.fr/gp/item-dispatch)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.amazon.fr/gp/music/clipserve](https://www.amazon.fr/gp/music/clipserve)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.amazon.fr/b/?ie=UTF8&node=11961521031&ref_=topnav_storetab_top_ap_arrow](https://www.amazon.fr/b/?ie=UTF8&node=11961521031&ref_=topnav_storetab_top_ap_arrow)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr/robots.txt](https://www.amazon.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.amazon.fr/gp/legacy-handle-buy-box.html](https://www.amazon.fr/gp/legacy-handle-buy-box.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/handler/handle-email-submit.html](https://www.amazon.fr/gp/help/customer/handler/handle-email-submit.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr/b?node=16295965031&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=4dL0D&pd_rd_wg=i6bdh&pf_rd_p=cf4aa1f8-afe3-423e-8b54-3d7fcdd8a99d&pf_rd_r=CKDDFCGZRDJ8N16P3PKS](https://www.amazon.fr/b?node=16295965031&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=4dL0D&pd_rd_wg=i6bdh&pf_rd_p=cf4aa1f8-afe3-423e-8b54-3d7fcdd8a99d&pf_rd_r=CKDDFCGZRDJ8N16P3PKS)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000](https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/help/reports/infringement/jquery/handle-notice-submit.html](https://www.amazon.fr/gp/help/reports/infringement/jquery/handle-notice-submit.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/ask-widget/askWidget](https://www.amazon.fr/gp/ask-widget/askWidget)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/hz/leaderboard/hall-of-fame/](https://www.amazon.fr/hz/leaderboard/hall-of-fame/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/review/top-reviewers](https://www.amazon.fr/review/top-reviewers)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/hz/leaderboard/top-reviewers/](https://www.amazon.fr/hz/leaderboard/top-reviewers/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/promotion/](https://www.amazon.fr/gp/promotion/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/aw/ol/](https://www.amazon.fr/gp/aw/ol/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/ss/customer-reviews/lighthouse/](https://www.amazon.fr/ss/customer-reviews/lighthouse/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/reviews/iframe](https://www.amazon.fr/reviews/iframe)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/dmusic/promotions/AmazonMusicUnlimited](https://www.amazon.fr/gp/dmusic/promotions/AmazonMusicUnlimited)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/review/top-reviewers/](https://www.amazon.fr/review/top-reviewers/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/review/hall-of-fame](https://www.amazon.fr/review/hall-of-fame)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.amazon.fr/GAME-WATCH-SM-BROS-SYSTEM/dp/B08GZ3DRLW/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/GAME-WATCH-SM-BROS-SYSTEM/dp/B08GZ3DRLW/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/music/clipserve](https://www.amazon.fr/gp/music/clipserve)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nouvelle-Manette-Xbox-Sans-Fil/dp/B087VLP2RT/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nouvelle-Manette-Xbox-Sans-Fil/dp/B087VLP2RT/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Bravely-Default-II-Nintendo-Switch/dp/B08R98DFL1/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Bravely-Default-II-Nintendo-Switch/dp/B08R98DFL1/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/history](https://www.amazon.fr/gp/history)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000](https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/Nouveau-Casque-sans-fil-Xbox/dp/B08WJSJT4J/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nouveau-Casque-sans-fil-Xbox/dp/B08WJSJT4J/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/robots.txt](https://www.amazon.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/New-Super-Mario-Bros-Deluxe/dp/B0055FFXQ6/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/New-Super-Mario-Bros-Deluxe/dp/B0055FFXQ6/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/item-dispatch](https://www.amazon.fr/gp/item-dispatch)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/legacy-handle-buy-box.html](https://www.amazon.fr/gp/legacy-handle-buy-box.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/handler/handle-email-submit.html](https://www.amazon.fr/gp/help/customer/handler/handle-email-submit.html)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `qWO/+NW4yEFctXIRwpPSilA3BHrvUnODpBvsjLXrXMVyW8U5AD7MkVwsYPm8Lj+vgpKcbXa70vLXsJlrFOYjpvElxuGg5rbS60pORnAIauyWRA8XlLy9+0PIvUr4X4ylBhYfXYbj79lXlHdFj07OoM3bRFD7tmt5ZcjrDVc32yW2gEMc42UmWXQX62RbX0LM`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/common/du](https://www.amazon.fr/gp/customer-reviews/common/du)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
* URL: [https://www.amazon.fr/dp/product-availability/](https://www.amazon.fr/dp/product-availability/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/images/G/08/error/amazon-fr-logo-OYXHL`
  
  
  
  
* URL: [https://www.amazon.fr/sitemap.xml](https://www.amazon.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/images/G/08/error/amazon-fr-logo-OYXHL`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/images/G/08/javascripts/lib/popover/images/snake`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
* URL: [https://www.amazon.fr/dp/rate-this-item/](https://www.amazon.fr/dp/rate-this-item/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/images/G/08/error/amazon-fr-logo-OYXHL`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�c��ո�A\�r\x0011ҊP7\x0004z�Rs��\x001b쌵�\�r[�9\x0000>̑\,`��.?����mv���װ�k\x0014�#��%�����JNFp\x0008j�D\x000f\x0017����CȽJ�_��\x0006\x0016\x001f]����W�wE�NΠ��DP��kye��
W7�%��C\x001c�e&Yt\x0017�d[_B�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Charset Mismatch (Header Versus Meta Content-Type Charset)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check identifies responses where the HTTP Content-Type header declares a charset different from the charset defined by the body of the HTML or XML. When there's a charset mismatch between the HTTP header and content body Web browsers can be forced into an undesirable content-sniffing mode to determine the content's correct character set.</p><p></p><p>An attacker could manipulate content on the page to be interpreted in an encoding of their choice. For example, if an attacker can control content at the beginning of the page, they could inject script using UTF-7 encoded text and manipulate some browsers into interpreting that text.</p>
  
  
  
* URL: [https://www.amazon.fr/Animal-Crossing-Horizons-Nintendo-Switch/dp/B0821XHJB6/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Animal-Crossing-Horizons-Nintendo-Switch/dp/B0821XHJB6/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Elgato-Stream-Deck-Contr%C3%B4leur-Personnalisables/dp/B06W2KLM3S/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Elgato-Stream-Deck-Contr%C3%B4leur-Personnalisables/dp/B06W2KLM3S/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-0045496420246-Mario-Kart-Deluxe/dp/B01N223WHL/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-0045496420246-Mario-Kart-Deluxe/dp/B01N223WHL/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Story-Seasons-Pioneers-Nintendo-Switch/dp/B08MBTQH3H/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Story-Seasons-Pioneers-Nintendo-Switch/dp/B08MBTQH3H/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-195693-Hades-Edition-Limit%C3%A9e/dp/B08WY61MCN/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-195693-Hades-Edition-Limit%C3%A9e/dp/B08WY61MCN/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Ring-Adventure-pour-Nintendo-Switch/dp/B07XTVTRLZ/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Ring-Adventure-pour-Nintendo-Switch/dp/B07XTVTRLZ/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/SUPER-MARIO-3D-ALL-STARS/dp/B08GZ4Z5SM/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/SUPER-MARIO-3D-ALL-STARS/dp/B08GZ4Z5SM/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-Monster-Hunter-Rise/dp/B08GZ3M2ZV/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-Monster-Hunter-Rise/dp/B08GZ3M2ZV/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Electronic-Arts-1101390-Takes-Two/dp/B08S115LSD/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Electronic-Arts-1101390-Takes-Two/dp/B08S115LSD/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Legend-Zelda-Breath-Wild/dp/B01MUAFFPA/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Legend-Zelda-Breath-Wild/dp/B01MUAFFPA/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-NINTENDO-SWITCH-PRO-CNTRL-Manette-Switch-Pro/dp/B01N4ND1T2/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-NINTENDO-SWITCH-PRO-CNTRL-Manette-Switch-Pro/dp/B01N4ND1T2/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/microSDXC-SanDisk-128-Go-Nintendo-Switch/dp/B07KXQX3S3/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/microSDXC-SanDisk-128-Go-Nintendo-Switch/dp/B07KXQX3S3/?_encoding=UTF8&pd_rd_r=6ea216dc-5ccc-4bcd-b9e4-cae6630187f7&pd_rd_w=iw8r2&pd_rd_wg=i6bdh&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Force UTF-8 for all text content in both the HTTP header and meta tags in HTML or encoding declarations in XML.</p>
  
### Other information
<p>There was a charset mismatch between the HTTP Header and the META content-type encoding declarations: [UTF-8] and [iso-8859-1] do not match.</p>
  
### Reference
* http://code.google.com/p/browsersec/wiki/Part2#Character_set_handling_and_detection

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://www.amazon.fr/gp/redirect.html?location=https://www.primevideo.com/ref=dvm_crs_gat_fr_xs_s_dk_hud_eg_un&token=7B0C63075F460BB35E3C74C2B7D47F289F0BECC6](https://www.amazon.fr/gp/redirect.html?location=https://www.primevideo.com/ref=dvm_crs_gat_fr_xs_s_dk_hud_eg_un&token=7B0C63075F460BB35E3C74C2B7D47F289F0BECC6)
  
  
  * Method: `GET`
  
  
  * Parameter: `token`
  
  
  * Evidence: `token`
  
  
  
  
* URL: [https://www.amazon.fr/gp/redirect.html?location=https://www.amazonfutureengineer.fr&source=standards&token=7E9A407E9F06F460D077C0AEACDA7742FAF004B9](https://www.amazon.fr/gp/redirect.html?location=https://www.amazonfutureengineer.fr&source=standards&token=7E9A407E9F06F460D077C0AEACDA7742FAF004B9)
  
  
  * Method: `GET`
  
  
  * Parameter: `token`
  
  
  * Evidence: `token`
  
  
  
  
* URL: [https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D](https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=CKDDFCGZRDJ8N16P3PKS&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D)
  
  
  * Method: `GET`
  
  
  * Parameter: `token`
  
  
  * Evidence: `token`
  
  
  
  
Instances: 3
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL contains potentially sensitive information. The following string was found via the pattern: token</p><p>token</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 3 times, the first in the element starting with: "<!--</p><p>    window.$Nav && $Nav.declare('config.fixedBarBeacon',false);</p><p>    window.$Nav && $Nav.when("data").run(function(data) { d", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
Instances: 10
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bTODO\b and was detected in the element starting with: "<script type="text/javascript"></p><p>(function ($Nav) {</p><p>"use strict";</p><p></p><p>if (typeof $Nav === 'undefined' || $Nav === null || typeof $Na", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Loosely Scoped Cookie
##### Informational (Low)
  
  
  
  
#### Description
<p>Cookies can be scoped by domain or path. This check is only concerned with domain scope.The domain scope applied to a cookie determines which domains can access it. For example, a cookie can be scoped strictly to a subdomain e.g. www.nottrusted.com, or loosely scoped to a parent domain e.g. nottrusted.com. In the latter case, any subdomain of nottrusted.com can access the cookie. Loosely scoped cookies are common in mega-applications like google.com and live.com. Cookies set from a subdomain like app.foo.bar are transmitted only to that domain by the browser. However, cookies scoped to a parent-level domain may be transmitted to the parent, or any subdomain of the parent.</p>
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/flex-sign-in](https://www.amazon.fr/exec/obidos/flex-sign-in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/handle-buy-box](https://www.amazon.fr/exec/obidos/handle-buy-box)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-collection.html](https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-collection.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/partners/friends/access.html](https://www.amazon.fr/exec/obidos/subst/partners/friends/access.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-stuff.html](https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-stuff.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/refer-a-friend-login](https://www.amazon.fr/exec/obidos/refer-a-friend-login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/associates/join](https://www.amazon.fr/exec/obidos/subst/associates/join)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Always scope cookies to a FQDN (Fully Qualified Domain Name).</p>
  
### Other information
<p>The origin domain used for comparison was: </p><p>www.amazon.fr</p><p>ubid-acbfr=258-6102988-9052254</p><p>session-id-time=2082754801l</p><p>session-id=257-5516316-9275726</p><p></p>
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=MN9N6TF6WWHXJXQJR9SD&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:MN9N6TF6WWHXJXQJR9SD$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DMN9N6TF6WWHXJXQJR9SD%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='nav-top'></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=2J8EYG2WH1TBS7F7PGY7&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:2J8EYG2WH1TBS7F7PGY7$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D2J8EYG2WH1TBS7F7PGY7%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/flex](https://www.amazon.fr/gp/flex)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=Y77QTFSK7M165AM85Z09&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:Y77QTFSK7M165AM85Z09$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DY77QTFSK7M165AM85Z09%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=N85YEGSD6ZMZ5FGY9YPY&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:N85YEGSD6ZMZ5FGY9YPY$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DN85YEGSD6ZMZ5FGY9YPY%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/write-a-review.html](https://www.amazon.fr/gp/customer-reviews/write-a-review.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=5877TGRXTP9683T2E1C6&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:5877TGRXTP9683T2E1C6$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D5877TGRXTP9683T2E1C6%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/gfix](https://www.amazon.fr/gp/gfix)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=XHEZHG2NWNMTA3BF9B0P&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:XHEZHG2NWNMTA3BF9B0P$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DXHEZHG2NWNMTA3BF9B0P%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=C7KJW66V1ZZG35JVNS13&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:C7KJW66V1ZZG35JVNS13$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DC7KJW66V1ZZG35JVNS13%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/common/du](https://www.amazon.fr/gp/customer-reviews/common/du)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=4BW2HAMZH2RDVTF7B8PX&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:257-5516316-9275726:4BW2HAMZH2RDVTF7B8PX$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D4BW2HAMZH2RDVTF7B8PX%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='nav-top'></a>`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='nav-top'></a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.amazon.fr/dp/rate-this-item/](https://www.amazon.fr/dp/rate-this-item/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/robots.txt](https://www.amazon.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/product-availability/](https://www.amazon.fr/dp/product-availability/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/handle-buy-box](https://www.amazon.fr/exec/obidos/handle-buy-box)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/flex-sign-in](https://www.amazon.fr/exec/obidos/flex-sign-in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/sitemap.xml](https://www.amazon.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `200233750`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `73683041`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `695398031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `838795031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `30455130`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `12183668`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201909010`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201890250`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201267600`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `197858031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `13921051`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20793816`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `197861031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201909000`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `57004031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `202589011`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `322086011`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `57696031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `325614031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201909150`
  
  
  
  
Instances: 32
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>200233750, which evaluates to: 1976-05-06 12:29:10</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031](https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031)
  
  
  * Method: `GET`
  
  
  * Parameter: `i`
  
  
  
  
* URL: [https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A2308681031%2Cn%3A2308687031](https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A2308681031%2Cn%3A2308687031)
  
  
  * Method: `GET`
  
  
  * Parameter: `rh`
  
  
  
  
* URL: [https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031](https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031)
  
  
  * Method: `GET`
  
  
  * Parameter: `bbn`
  
  
  
  
* URL: [https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031](https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031)
  
  
  * Method: `GET`
  
  
  * Parameter: `rh`
  
  
  
  
* URL: [https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A2308681031%2Cn%3A2308687031](https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A2308681031%2Cn%3A2308687031)
  
  
  * Method: `GET`
  
  
  * Parameter: `bbn`
  
  
  
  
* URL: [https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A2308681031%2Cn%3A2308687031](https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A2308681031%2Cn%3A2308687031)
  
  
  * Method: `GET`
  
  
  * Parameter: `i`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.amazon.fr/s?bbn=22951682031&i=fashion&rh=n%3A11961521031%2Cn%3A22951682031%2Cn%3A12422072031%2Cn%3A1765336031</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>i=fashion</p><p></p><p>The user-controlled value was:</p><p>fashion</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

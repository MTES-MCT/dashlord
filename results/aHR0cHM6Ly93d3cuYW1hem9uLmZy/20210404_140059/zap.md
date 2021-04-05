
# ZAP Scanning Report

Generated on Sun, 4 Apr 2021 13:56:33


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 3 |
| Low | 10 |
| Informational | 12 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Open Redirect | High | 2 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 12 | 
| Sub Resource Integrity Attribute Missing | Medium | 14 | 
| Absence of Anti-CSRF Tokens | Low | 10 | 
| Cookie No HttpOnly Flag | Low | 13 | 
| Cookie Without SameSite Attribute | Low | 13 | 
| Cookie Without Secure Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 13 | 
| Dangerous JS Functions | Low | 12 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 12 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Charset Mismatch (Header Versus Meta Content-Type Charset) | Informational | 12 | 
| Information Disclosure - Sensitive Information in URL | Informational | 2 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Loosely Scoped Cookie | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 9 | 
| Storable but Non-Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 45 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 32 | 
| User Controllable JavaScript Event (XSS) | Informational | 1 | 

## Alert Detail


  
  
  
  
### Open Redirect
##### High (Medium)
  
  
  
  
#### Description
<p>Open redirects are one of the OWASP 2010 Top Ten vulnerabilities. This check looks at user-supplied input in query string parameters and POST data to identify where open redirects might be possible. Open redirects occur when an application allows user-supplied input (e.g. http://nottrusted.com) to control an offsite redirect. This is generally a pretty accurate way to find where 301 or 302 redirects could be exploited by spammers or phishing attacks.</p><p></p><p>For example an attacker could supply a user with the following link: http://example.com/example.php?url=http://malicious.example.com.</p>
  
  
  
* URL: [https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D](https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D)
  
  
  * Method: `GET`
  
  
  * Parameter: `location`
  
  
  
  
* URL: [https://www.amazon.fr/gp/redirect.html?location=https://www.primevideo.com/ref=dvm_crs_gat_fr_xs_s_dk_hud_eg_un&token=7B0C63075F460BB35E3C74C2B7D47F289F0BECC6](https://www.amazon.fr/gp/redirect.html?location=https://www.primevideo.com/ref=dvm_crs_gat_fr_xs_s_dk_hud_eg_un&token=7B0C63075F460BB35E3C74C2B7D47F289F0BECC6)
  
  
  * Method: `GET`
  
  
  * Parameter: `location`
  
  
  
  
Instances: 2
  
### Solution
<p>To avoid the open redirect vulnerability, parameters of the application script/program must be validated before sending 302 HTTP code (redirect) to the client browser. Implement safe redirect functionality that only redirects to relative URI's, or a list of trusted domains</p>
  
### Other information
<p>The 301 or 302 response to a request for the following URL appeared to contain user input in the location header:</p><p></p><p>https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D</p><p></p><p>The user input found was:</p><p></p><p>location=https://www.primevideo.com/ref</p><p></p><p>The context was:</p><p></p><p>https://www.primevideo.com/ref</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html
* https://cwe.mitre.org/data/definitions/601.html

  
#### CWE Id : 601
  
#### WASC Id : 38
  
#### Source ID : 3

  
  
  
  
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
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/write-a-review.html](https://www.amazon.fr/gp/customer-reviews/write-a-review.html)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/livre-achat-occasion-litterature-roman/b/?ie=UTF8&node=301061&ref_=nav_cs_books_8e69fb98d8364ce383566b2f28213bd2](https://www.amazon.fr/livre-achat-occasion-litterature-roman/b/?ie=UTF8&node=301061&ref_=nav_cs_books_8e69fb98d8364ce383566b2f28213bd2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/Qr1OiFvwdeqGlxUX4nMtH50AAAF4nSJBJgMAAAH4ATAOujg/https://www.amazon.fr/stores/page/FCCA95EB-10A7-4EC4-963E-07833F79BB61" target="_top"><div id="bannerx0-root" class="root-bannerx0-base"><div id="bannerx0-copy" class="bannerx0-copy bannerx0-copy-base bannerx0-copy-layout"><div id="bannerx0-copy-content" class="bannerx0-copy-content bannerx0-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx0-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Les romans de votre printemps.</div><div id="bannerx0-copy-cta" class="bannerx0-cta bannerx0-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>En savoir plus</span></div></div></div><div id="bannerx0-product1" class="bannerx0-product1" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/51SYjvbSrPL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-product2" class="bannerx0-product2" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/514Xsn6FSkL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-product3" class="bannerx0-product3" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/51+aYgvYhUL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-product4" class="bannerx0-product4" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/41E1NSWMwAL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-transition1" class="bannerx0-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/SUPER-MARIO-WORLD-BOWSER-FURY/dp/B08GZ54RLL/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/SUPER-MARIO-WORLD-BOWSER-FURY/dp/B08GZ54RLL/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a aria-hidden="true" href="https://aax-eu.amazon.fr/x/c/QhrR2fsrD61irielWvI9AxcAAAF4nSMDdQMAAAH2Af8jEn4/https://www.amazon.fr/stores/page/ABD127DA-D255-4337-82A0-9CF16803A9A8?store_ref=SB_A05684731WT6UKQYFOGU6&amp;pd_rd_w=lbXIu&amp;pf_rd_p=5c06b918-9ae4-4b60-a5c8-f64c21204082&amp;pd_rd_wg=HfORo&amp;pf_rd_r=M9R08HFY1N5ATVKZKQNA&amp;pd_rd_r=ff2a609f-8a97-4029-9ed2-8f7de3a21e21&amp;pd_rd_i=ad1&amp;aaxitk=W1Mxvzd8BxTnMLpLRBvZhQ&amp;hsa_cr_id=9773322570102&amp;lp_asins=B07VD9KV51,B000NJWLC8,B07JKB2H59&amp;lp_slot=desktop-arbies&amp;ref_=sbx_be_dp_arbies_mbd" tabIndex="-1" target="_top" class="sb_1REHiRA7 sb_Es4IY3ln sb_UXyQgY3h" data-click-el="bkgd"><img style="width: auto; height: auto;" alt="Pictionary Air, jeu de société et de dessin dans les airs, avec résultat à l'écran, version française, GJG13" src="https://m.media-amazon.com/images/I/81PvhcBwslL._AC_SL139_QL70_.jpg" srcSet="https://m.media-amazon.com/images/I/81PvhcBwslL._AC_SL139_QL70_.jpg 1x,https://m.media-amazon.com/images/I/81PvhcBwslL._AC_SL278_QL70_.jpg 2x" data-click-asin="B07VD9KV51" data-click-el="img" class="sb_2g-RDitf sb_3n6fJzY6" /><div class="sb_1XryyATl"></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000](https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="same_window" href="https://fr.amazonforum.com" target="_self">Forum Num&eacute;rique et Appareils</a>`
  
  
  
  
* URL: [https://www.amazon.fr/b?node=3635788031](https://www.amazon.fr/b?node=3635788031)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/Qn-Rsa84v1OLMGudq8C0gMQAAAF4nSLWcQMAAAH4AXJe19M/https://www.amazon.fr/stores/page/D0D6E42E-B33C-4830-B3E8-AC618BD8B5DA" target="_top"><div id="bannerx0-root" class="root-bannerx0-base"><div id="bannerx0-copy" class="bannerx0-copy bannerx0-copy-base bannerx0-copy-layout"><div id="bannerx0-copy-content" class="bannerx0-copy-content bannerx0-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx0-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Café Grains Lavazza</div><div id="bannerx0-copy-subtext" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Une passion de l’excellence qui fait de chaque tasse une expérience unique.</div><div id="bannerx0-copy-cta" class="bannerx0-cta bannerx0-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>En savoir plus</span></div></div></div><div id="bannerx0-product1" class="bannerx0-product1" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/410TbR8BEGL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-product2" class="bannerx0-product2" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/31zk5sBqXDL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-transition1" class="bannerx0-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/SUPER-MARIO-3D-ALL-STARS/dp/B08GZ4Z5SM/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/SUPER-MARIO-3D-ALL-STARS/dp/B08GZ4Z5SM/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a aria-hidden="true" href="https://aax-eu.amazon.fr/x/c/QnQntefR5RxMQ6tjgx9xAOsAAAF4nSMzlAMAAAH2Adbt5hc/https://www.amazon.fr/stores/page/ABD127DA-D255-4337-82A0-9CF16803A9A8?store_ref=SB_A05684731WT6UKQYFOGU6&amp;pd_rd_w=uypzu&amp;pf_rd_p=5c06b918-9ae4-4b60-a5c8-f64c21204082&amp;pd_rd_wg=D0FeY&amp;pf_rd_r=N1E4ZA8TQP0RFSTNPJBB&amp;pd_rd_r=250273e1-1348-47a8-abc9-f305b8b2022f&amp;pd_rd_i=ad1&amp;aaxitk=3k.Y.u1LTynj5HIr1JpC8g&amp;hsa_cr_id=9773322570102&amp;lp_asins=B07VD9KV51,B000NJWLC8,B07JKB2H59&amp;lp_slot=desktop-arbies&amp;ref_=sbx_be_dp_arbies_mbd" tabIndex="-1" target="_top" class="sb_1REHiRA7 sb_Es4IY3ln sb_UXyQgY3h" data-click-el="bkgd"><img style="width: auto; height: auto;" alt="Pictionary Air, jeu de société et de dessin dans les airs, avec résultat à l'écran, version française, GJG13" src="https://m.media-amazon.com/images/I/81PvhcBwslL._AC_SL139_QL70_.jpg" srcSet="https://m.media-amazon.com/images/I/81PvhcBwslL._AC_SL139_QL70_.jpg 1x,https://m.media-amazon.com/images/I/81PvhcBwslL._AC_SL278_QL70_.jpg 2x" data-click-asin="B07VD9KV51" data-click-el="img" class="sb_2g-RDitf sb_3n6fJzY6" /><div class="sb_1XryyATl"></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/dp/B07FQ4DJ7X/ref=gw_fr_desk_mso_eink_jg_q4](https://www.amazon.fr/dp/B07FQ4DJ7X/ref=gw_fr_desk_mso_eink_jg_q4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="a-link-normal" target="_blank" rel="noopener" href="https://s3-us-west-2.amazonaws.com/customerdocumentation/EJ/Quick_Start_Guide_INTL.pdf">le guide de démarrage</a>`
  
  
  
  
* URL: [https://www.amazon.fr/PlayStation-%C3%89dition-Standard-DualSense-Couleur/dp/B08H93ZRK9/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/PlayStation-%C3%89dition-Standard-DualSense-Couleur/dp/B08H93ZRK9/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a aria-hidden="true" href="https://aax-eu.amazon.fr/x/c/QjSKlda66hCxCjDxYRxGE1YAAAF4nSMCswMAAAH2ASdTDao/https://www.amazon.fr/stores/page/E28DBD36-32C3-4D80-A850-5C0708A84DAA?store_ref=SB_A08809483ECUN57QXAHU5&amp;pd_rd_w=6ACAU&amp;pf_rd_p=5c06b918-9ae4-4b60-a5c8-f64c21204082&amp;pd_rd_wg=h2Anv&amp;pf_rd_r=XWZZEZ8A7VV4K0F6NN1N&amp;pd_rd_r=e89eeb01-8e9d-4d1f-bde1-5ab69a48fdd3&amp;pd_rd_i=ad1&amp;aaxitk=f-VSRF7OjJ9Afyx1kCH.0Q&amp;hsa_cr_id=5822676350102&amp;lp_asins=B08D46V1TK,B08486NP2G,B07D3N7JTY&amp;lp_slot=desktop-arbies&amp;ref_=sbx_be_dp_arbies_mbd" tabIndex="-1" target="_top" class="sb_1REHiRA7 sb_Es4IY3ln sb_UXyQgY3h" data-click-el="bkgd"><img style="width: auto; height: auto;" alt="Turtle Beach Stealth 600 Gen 2 Casque Gaming sans fil - PS4 et PS5" src="https://m.media-amazon.com/images/I/816jKsRfHSL._AC_SL139_QL70_.jpg" srcSet="https://m.media-amazon.com/images/I/816jKsRfHSL._AC_SL139_QL70_.jpg 1x,https://m.media-amazon.com/images/I/816jKsRfHSL._AC_SL278_QL70_.jpg 2x" data-click-asin="B08D46V1TK" data-click-el="img" class="sb_2g-RDitf sb_3n6fJzY6" /><div class="sb_1XryyATl"></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/jeux-jouets/b/?ie=UTF8&node=322086011&ref_=nav_cs_toys_376b632204af49268d0aea8c80091b3e](https://www.amazon.fr/jeux-jouets/b/?ie=UTF8&node=322086011&ref_=nav_cs_toys_376b632204af49268d0aea8c80091b3e)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/QhGPel1c7hoPnrjfBUTJ9m0AAAF4nSJUVAMAAAH4AdQ_kOM/https://www.amazon.fr/stores/page/37B2D70C-B4D4-4AE9-8644-2DAE2F2B030A" target="_top"><div id="bannerx0-root" class="root-bannerx0-base"><div id="bannerx0-copy" class="bannerx0-copy bannerx0-copy-base bannerx0-copy-layout"><div id="bannerx0-copy-content" class="bannerx0-copy-content bannerx0-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx0-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Découvrez les circuits à bille Gravitrax</div><div id="bannerx0-copy-subtext" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">de Ravensburger</div><div id="bannerx0-copy-cta" class="bannerx0-cta bannerx0-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>En savoir plus</span></div></div></div><div id="bannerx0-product1" class="bannerx0-product1" style="display:flex;"><img src="https://images-na.ssl-images-amazon.com/images/I/51vGVGm8ibL._SCLZZZZZZZ__.jpg" style="object-fit:contain;max-width:100%;max-height:100%;align-self:center;"></div><div id="bannerx0-transition1" class="bannerx0-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/dp/B07KD6624B/ref=gw_fr_desk_mso_aucc_ck_q4](https://www.amazon.fr/dp/B07KD6624B/ref=gw_fr_desk_mso_aucc_ck_q4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="a-link-normal" target="_blank" rel="noopener" href="https://s3-us-west-2.amazonaws.com/customerdocumentation/Alexa+Devices/Echo+Show+5_QSG_FR.pdf">guide de démarrage</a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/display.html?nodeId=508510&ref_=nav_cs_help_2f06f8566ef14872afc718efa7446437](https://www.amazon.fr/gp/help/customer/display.html?nodeId=508510&ref_=nav_cs_help_2f06f8566ef14872afc718efa7446437)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="same_window" href="https://fr.amazonforum.com" target="_self">Forum Num&eacute;rique et Appareils</a>`
  
  
  
  
* URL: [https://www.amazon.fr/ebooks-kindle/b/?ie=UTF8&node=695398031&ref_=nav_cs_kindle_books_bbd083fa578a49a1a7bb32f66fdab37e](https://www.amazon.fr/ebooks-kindle/b/?ie=UTF8&node=695398031&ref_=nav_cs_kindle_books_bbd083fa578a49a1a7bb32f66fdab37e)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/QkCeD4Bz9dVJbqlzbLCe_foAAAF4nSJdhwMAAAH4AfD9t2I/https://www.amazon.fr/primereading" target="_top"><div id="bannerx111226-root" class="root-bannerx111226-base"><div id="bannerx111226-copy" class="bannerx111226-copy bannerx111226-copy-base bannerx111226-copy-layout"><div id="bannerx111226-copy-content" class="bannerx111226-copy-content bannerx111226-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx111226-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Prime Reading inclus avec Amazon Prime</div></div></div><div id="bannerx111226-background_image" class="bannerx111226-background_image" style="display:flex;height:100%;width:100%;overflow:hidden;align-items:center;justify-content:center;"><img src="https://m.media-amazon.com/images/G/08/kindle/pr/merch/recent/prime_reading-flex-3000x1200.jpg" style="object-fit:cover;min-width:100%;min-height:100%;max-width:140%;max-height:140%;"></div><div id="bannerx111226-transition1" class="bannerx111226-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/browse.html?node=301061&ref_=nav_em__lv_0_2_10_2](https://www.amazon.fr/gp/browse.html?node=301061&ref_=nav_em__lv_0_2_10_2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://aax-eu-dub.amazon.com/x/c/Qo9sCFmaAG_QYPFYudris9oAAAF4nSLfygMAAAH4AcUE_cc/https://www.amazon.fr/b?ie=UTF8&amp;node=6680516031" target="_top"><div id="bannerx777314-root" class="root-bannerx777314-base"><div id="bannerx777314-copy" class="bannerx777314-copy bannerx777314-copy-base bannerx777314-copy-layout"><div id="bannerx777314-copy-content" class="bannerx777314-copy-content bannerx777314-copy-content-base" style="position:relative;z-index:100;display:flex;flex:1;flex-direction:column;justify-content:center;"><div id="bannerx777314-copy-headline" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Le Top Nouveautés Livres</div><div id="bannerx777314-copy-subtext" style="font-family:Amazon Ember, Amazon Ember Bold, sans-serif;">Découvrez toutes les nouveautés du moment </div><div id="bannerx777314-copy-cta" class="bannerx777314-cta bannerx777314-cta-arrow-right" style="font-weight:400;font-size:12px;padding-bottom:0.08em;word-break:keep-all;font-family:Amazon Ember, Amazon Ember Bold, sans-serif;"><span>Voir plus</span></div></div></div><div id="bannerx777314-background_image" class="bannerx777314-background_image" style="display:flex;height:100%;width:100%;overflow:hidden;align-items:center;justify-content:center;"><img src="https://m.media-amazon.com/images/G/08/UK-hq/2020/img/Books/XCM_Manual_1289204_1490206_FR_uk_de_fr_it_es_new_releases_amp_campaigns_gb_en_3551226_3000x1200_en_GB.jpg" style="object-fit:cover;min-width:100%;min-height:100%;max-width:140%;max-height:140%;"></div><div id="bannerx777314-transition1" class="bannerx777314-transition1" style="position:relative;"></div></div></a>`
  
  
  
  
Instances: 12
  
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
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://images-eu.ssl-images-amazon.com/images/I/11EIQ5IGqaL._RC|01ZTHTZObnL.css,41lWgC9jnyL.css,31qGOnSAToL.css,013z33uKh2L.css,017DsKjNQJL.css,01xH24p45SL.css,41EWOOlBJ9L.css,11gKzVUTNZL.css,01ElnPiDxWL.css,11bGSgD5pDL.css,01Dm5eKVxwL.css,01IdKcBuAdL.css,01y-XAlI+2L.css,21N4kUH7pxL.css,01oDR3IULNL.css,31q1y1irc5L.css,21j0IlW7xKL.css,01XPHJk60-L.css,014OeDQisGL.css,21aPhFy+riL.css,11gneA3MtJL.css,21fecG8pUzL.css,01RddH8vm-L.css,01CFUgsA-YL.css,31C80IiXalL.css,11qour3ND0L.css,11tRp6+0HHL.css,11MrdqKlKnL.css,11oHt2HYxnL.css,013RDhw9hoL.css,11JQtnL-6eL.css,11RKoGSb-gL.css,11jtXRmppwL.css,01QrWuRrZ-L.css,21pIv-yKhaL.css,11QyqG8yiqL.css,01890+Vwk8L.css,11kwKGWmBfL.css,11F2+OBzLyL.css,11Y05DTEL6L.css,01cbS3UK11L.css,21F85am0yFL.css,01giMEP+djL.css_.css?AUIClients/AmazonUI&xHiWlrYT#fr.page_type-Gateway.not-trident.322290-T2.322288-T1.263677-T2" />`
  
  
  
  
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
  
  
  
* URL: [https://www.amazon.fr/gcx/-/gfhz/?ref_=nav_cs_giftfinder_1ac2003068194e298230776c7abc3bb7](https://www.amazon.fr/gcx/-/gfhz/?ref_=nav_cs_giftfinder_1ac2003068194e298230776c7abc3bb7)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/I/01OCq7x-zqL.js`
  
  
  * Evidence: `<script crossorigin="anonymous" type="text/javascript" src="https://m.media-amazon.com/images/I/01OCq7x-zqL.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/Voiture-et-moto/b/?ie=UTF8&node=1571265031&ref_=nav_cs_automotive_dc61475604ba4475bfd7c01439485227](https://www.amazon.fr/Voiture-et-moto/b/?ie=UTF8&node=1571265031&ref_=nav_cs_automotive_dc61475604ba4475bfd7c01439485227)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/03/amazonservices/aos.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/03/amazonservices/aos.js" type="text/javascript"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89](https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/amazonservices/leadcode.min.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/amazonservices/leadcode.min.js" type="text/javascript"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/jeux-jouets/b/?ie=UTF8&node=322086011&ref_=nav_cs_toys_376b632204af49268d0aea8c80091b3e](https://www.amazon.fr/jeux-jouets/b/?ie=UTF8&node=322086011&ref_=nav_cs_toys_376b632204af49268d0aea8c80091b3e)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/gcx/-/gfhz/?ref_=nav_cs_giftfinder_1ac2003068194e298230776c7abc3bb7](https://www.amazon.fr/gcx/-/gfhz/?ref_=nav_cs_giftfinder_1ac2003068194e298230776c7abc3bb7)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/I/81RHVn4MaCL.js`
  
  
  * Evidence: `<script crossorigin="anonymous" type="text/javascript" src="https://m.media-amazon.com/images/I/81RHVn4MaCL.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/livre-achat-occasion-litterature-roman/b/?ie=UTF8&node=301061&ref_=nav_cs_books_8e69fb98d8364ce383566b2f28213bd2](https://www.amazon.fr/livre-achat-occasion-litterature-roman/b/?ie=UTF8&node=301061&ref_=nav_cs_books_8e69fb98d8364ce383566b2f28213bd2)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/Voiture-et-moto/b/?ie=UTF8&node=1571265031&ref_=nav_cs_automotive_dc61475604ba4475bfd7c01439485227](https://www.amazon.fr/Voiture-et-moto/b/?ie=UTF8&node=1571265031&ref_=nav_cs_automotive_dc61475604ba4475bfd7c01439485227)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d1215ijo50bwf7.cloudfront.net/design/assets-AS2015.js`
  
  
  * Evidence: `<script src="https://d1215ijo50bwf7.cloudfront.net/design/assets-AS2015.js" type="text/javascript"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/ebooks-kindle/b/?ie=UTF8&node=695398031&ref_=nav_cs_kindle_books_bbd083fa578a49a1a7bb32f66fdab37e](https://www.amazon.fr/ebooks-kindle/b/?ie=UTF8&node=695398031&ref_=nav_cs_kindle_books_bbd083fa578a49a1a7bb32f66fdab37e)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/cba/js/jquery-2.1.3.min._CB306061750_.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89](https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/01/amazonservices/s-code-plain.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/01/amazonservices/s-code-plain.js" type="text/javascript"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/gcx/-/gfhz/?ref_=nav_cs_giftfinder_1ac2003068194e298230776c7abc3bb7](https://www.amazon.fr/gcx/-/gfhz/?ref_=nav_cs_giftfinder_1ac2003068194e298230776c7abc3bb7)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/I/91b5nm4waQL.js`
  
  
  * Evidence: `<script crossorigin="anonymous" type="text/javascript" src="https://m.media-amazon.com/images/I/91b5nm4waQL.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89](https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://images-eu.ssl-images-amazon.com/images/G/08/amazonservices/s_code.js`
  
  
  * Evidence: `<script src="https://images-eu.ssl-images-amazon.com/images/G/08/amazonservices/s_code.js"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89](https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d3216uwaav9lg7.cloudfront.net/assets-Sell.js`
  
  
  * Evidence: `<script src="https://d3216uwaav9lg7.cloudfront.net/assets-Sell.js" type="text/javascript"></script>`
  
  
  
  
* URL: [https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89](https://www.amazon.fr/b/?ld=AZFRGNOSellC&node=2383619031&ref_=nav_cs_sell_3e0333dd43854113b8d44de438d17c89)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://m.media-amazon.com/images/G/03/amazonservices/aos.js`
  
  
  * Evidence: `<script src="https://m.media-amazon.com/images/G/03/amazonservices/aos.js" type="text/javascript"></script>`
  
  
  
  
Instances: 13
  
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
  
  
  
  
* URL: [https://www.amazon.fr/gp/history](https://www.amazon.fr/gp/history)
  
  
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
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/write-a-review.html](https://www.amazon.fr/gp/customer-reviews/write-a-review.html)
  
  
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
  
  
  
  
* URL: [https://www.amazon.fr/gp/aw/ol/](https://www.amazon.fr/gp/aw/ol/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
  
* URL: [https://www.amazon.fr/hz/leaderboard/top-reviewers/](https://www.amazon.fr/hz/leaderboard/top-reviewers/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/offer-listing](https://www.amazon.fr/gp/offer-listing)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/aw/so.html](https://www.amazon.fr/gp/aw/so.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/wishlist/get-button](https://www.amazon.fr/wishlist/get-button)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/wishlist/vendor-button](https://www.amazon.fr/wishlist/vendor-button)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/twister-update/](https://www.amazon.fr/dp/twister-update/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/e-mail-friend/](https://www.amazon.fr/dp/e-mail-friend/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/socialmedia/giveaways](https://www.amazon.fr/gp/socialmedia/giveaways)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/wishlist/universal](https://www.amazon.fr/wishlist/universal)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/product/product-availability](https://www.amazon.fr/gp/product/product-availability)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/pdp/profile/](https://www.amazon.fr/gp/pdp/profile/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/wishlist/](https://www.amazon.fr/wishlist/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/gp/registry/wishlist/](https://www.amazon.fr/gp/registry/wishlist/)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/cart/view.html?ref_=nav_cart](https://www.amazon.fr/gp/cart/view.html?ref_=nav_cart)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/new-releases/?ref_=nav_cs_newreleases_a1c7374e9d844b468ca0637c2afe3c85](https://www.amazon.fr/gp/new-releases/?ref_=nav_cs_newreleases_a1c7374e9d844b468ca0637c2afe3c85)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/music/clipserve](https://www.amazon.fr/gp/music/clipserve)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/site-directory?ref_=nav_em_js_disabled](https://www.amazon.fr/gp/site-directory?ref_=nav_em_js_disabled)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/history](https://www.amazon.fr/gp/history)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000](https://www.amazon.fr/gp/help/customer/display.html?*nodeId=200534000)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/robots.txt](https://www.amazon.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/aw/ol/](https://www.amazon.fr/gp/aw/ol/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/item-dispatch](https://www.amazon.fr/gp/item-dispatch)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.amazon.fr/gp/bestsellers/?ref_=nav_cs_bestsellers_382bd694910d4dd09a19cdaf01ec3091](https://www.amazon.fr/gp/bestsellers/?ref_=nav_cs_bestsellers_382bd694910d4dd09a19cdaf01ec3091)
  
  
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
  
  
  
* URL: [https://www.amazon.fr/dp/product-availability/](https://www.amazon.fr/dp/product-availability/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/images/G/08/error/amazon-fr-logo-OYXHL`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `wnHjFCMcfeDuovLIh9StBKJoF4cEkSJ5a8jAzOuFXldcoo9MweoEwW5BknAc8DXrJjUrp81pvKvXvLYs/BwJYzQiLmLzlZYqIYdRGArJmX9wo5yyW3xQ4j0Oha1tJLeJZnhX77bGQtQAZVpbMclF6JFmNWc+3vuEt3awx36ga2Rz6w52uOGb7Tl2eX0/tp4Y`
  
  
  
  
* URL: [https://www.amazon.fr/sitemap.xml](https://www.amazon.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/images/G/08/error/amazon-fr-logo-OYXHL`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/write-a-review.html](https://www.amazon.fr/gp/customer-reviews/write-a-review.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/1/batch/1/OP/A13V1IB3VIYZZH`
  
  
  
  
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
<p>r���f�z���O?z����k:'�����(��\x0017\x001c</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Charset Mismatch (Header Versus Meta Content-Type Charset)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check identifies responses where the HTTP Content-Type header declares a charset different from the charset defined by the body of the HTML or XML. When there's a charset mismatch between the HTTP header and content body Web browsers can be forced into an undesirable content-sniffing mode to determine the content's correct character set.</p><p></p><p>An attacker could manipulate content on the page to be interpreted in an encoding of their choice. For example, if an attacker can control content at the beginning of the page, they could inject script using UTF-7 encoded text and manipulate some browsers into interpreting that text.</p>
  
  
  
* URL: [https://www.amazon.fr/dp/B07FQ4DJ7X/ref=gw_fr_desk_mso_eink_jg_q4](https://www.amazon.fr/dp/B07FQ4DJ7X/ref=gw_fr_desk_mso_eink_jg_q4)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-Monster-Hunter-Rise/dp/B08GZ3M2ZV/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-Monster-Hunter-Rise/dp/B08GZ3M2ZV/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/B07KD6624B/ref=gw_fr_desk_mso_aucc_ck_q4](https://www.amazon.fr/dp/B07KD6624B/ref=gw_fr_desk_mso_aucc_ck_q4)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/B07ZZVWB4L/ref=gw_fr_desk_mso_smp_shl_q4](https://www.amazon.fr/dp/B07ZZVWB4L/ref=gw_fr_desk_mso_smp_shl_q4)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-0045496420246-Mario-Kart-Deluxe/dp/B01N223WHL/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-0045496420246-Mario-Kart-Deluxe/dp/B01N223WHL/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Animal-Crossing-Horizons-Nintendo-Switch/dp/B0821XHJB6/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Animal-Crossing-Horizons-Nintendo-Switch/dp/B0821XHJB6/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/PlayStation-%C3%89dition-Standard-DualSense-Couleur/dp/B08H93ZRK9/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/PlayStation-%C3%89dition-Standard-DualSense-Couleur/dp/B08H93ZRK9/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/SUPER-MARIO-WORLD-BOWSER-FURY/dp/B08GZ54RLL/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/SUPER-MARIO-WORLD-BOWSER-FURY/dp/B08GZ54RLL/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/SUPER-MARIO-3D-ALL-STARS/dp/B08GZ4Z5SM/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/SUPER-MARIO-3D-ALL-STARS/dp/B08GZ4Z5SM/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/dp/B078YP59TT/ref=gw_fr_desk_mso_aucc_mf_q4](https://www.amazon.fr/dp/B078YP59TT/ref=gw_fr_desk_mso_aucc_mf_q4)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Ring-Adventure-pour-Nintendo-Switch/dp/B07XTVTRLZ/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Ring-Adventure-pour-Nintendo-Switch/dp/B07XTVTRLZ/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/Nintendo-195693-Hades-Edition-Limit%C3%A9e/dp/B08WY61MCN/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490](https://www.amazon.fr/Nintendo-195693-Hades-Edition-Limit%C3%A9e/dp/B08WY61MCN/?_encoding=UTF8&pd_rd_r=545c7955-9499-41cb-8191-bc62a8865dbe&pd_rd_w=jlMZl&pd_rd_wg=ISy1V&pf_rd_p=1a998406-7f30-4647-8dda-107dde9197e8&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&ref_=pd_gw_crs_zg_bs_530490)
  
  
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
  
  
  
  
* URL: [https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D](https://www.amazon.fr/gp/redirect.html/?ie=UTF8&location=https%3A%2F%2Fwww.primevideo.com%2Fref&pf_rd_i=navbar-4201&pf_rd_m=A13V1IB3VIYZZH&pf_rd_p=ccfd2784-8ec9-4bd4-9a1a-973809a86811&pf_rd_r=A29CMMA8Q5W3FXH9G4CM&pf_rd_s=nav-sitewide-msg&pf_rd_t=4201&ref_=nav_swm_dvm_crs_swm_fr_xs_s_dk_swm_eg_un&token=59A51679133469AF9F6D2E40FD20EEB2C9A7126D)
  
  
  * Method: `GET`
  
  
  * Parameter: `token`
  
  
  * Evidence: `token`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-collection.html](https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-collection.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/flex-sign-in](https://www.amazon.fr/exec/obidos/flex-sign-in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/account-access-login](https://www.amazon.fr/exec/obidos/account-access-login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-stuff.html](https://www.amazon.fr/exec/obidos/subst/marketplace/sell-your-stuff.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box](https://www.amazon.fr/exec/obidos/dt/assoc/handle-buy-box)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/change-style](https://www.amazon.fr/exec/obidos/change-style)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/refer-a-friend-login](https://www.amazon.fr/exec/obidos/refer-a-friend-login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/partners/friends/access.html](https://www.amazon.fr/exec/obidos/subst/partners/friends/access.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/handle-buy-box](https://www.amazon.fr/exec/obidos/handle-buy-box)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.amazon.fr/exec/obidos/subst/associates/join](https://www.amazon.fr/exec/obidos/subst/associates/join)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Always scope cookies to a FQDN (Fully Qualified Domain Name).</p>
  
### Other information
<p>The origin domain used for comparison was: </p><p>www.amazon.fr</p><p>ubid-acbfr=258-7697703-0768863</p><p>session-id-time=2082754801l</p><p>session-id=261-2492296-9677961</p><p></p>
  
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
  
  
  
* URL: [https://www.amazon.fr/gp/customer-media/upload](https://www.amazon.fr/gp/customer-media/upload)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=64KF7KVSBTJKG42EJ34D&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:64KF7KVSBTJKG42EJ34D$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D64KF7KVSBTJKG42EJ34D%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr](https://www.amazon.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='nav-top'></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-images](https://www.amazon.fr/gp/customer-images)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=9QMEYPWCXTJGPTP7M3WB&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:9QMEYPWCXTJGPTP7M3WB$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D9QMEYPWCXTJGPTP7M3WB%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/flex](https://www.amazon.fr/gp/flex)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=52N7DT1QJZCYDN79Q8T9&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:52N7DT1QJZCYDN79Q8T9$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D52N7DT1QJZCYDN79Q8T9%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/common/du](https://www.amazon.fr/gp/customer-reviews/common/du)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=N1VVABT086H5K70JZ3XR&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:N1VVABT086H5K70JZ3XR$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DN1VVABT086H5K70JZ3XR%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/gfix](https://www.amazon.fr/gp/gfix)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=J9N263J6VHXQX1YVKKZX&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:J9N263J6VHXQX1YVKKZX$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DJ9N263J6VHXQX1YVKKZX%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/content-form](https://www.amazon.fr/gp/content-form)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=BMQ0N6PMX96B7SWQMT72&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:BMQ0N6PMX96B7SWQMT72$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DBMQ0N6PMX96B7SWQMT72%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/customer-reviews/write-a-review.html](https://www.amazon.fr/gp/customer-reviews/write-a-review.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=K5BAAKX1QWRR4VCCWCND&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:K5BAAKX1QWRR4VCCWCND$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3DK5BAAKX1QWRR4VCCWCND%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='nav-top'></a>`
  
  
  
  
* URL: [https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_](https://www.amazon.fr/*/s?k=*&rh=n*p_*p_*p_)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='nav-top'></a>`
  
  
  
  
* URL: [https://www.amazon.fr/gp/cart](https://www.amazon.fr/gp/cart)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
     <img src='/rd/uedata?noscript&amp;id=4CBB06SQR46C6W9DJPV3&amp;pty=Error&amp;spty=PageNotFound&amp;pti=' />
     <img src='//fls-eu.amazon.fr/1/batch/1/OP/A13V1IB3VIYZZH:261-2492296-9677961:4CBB06SQR46C6W9DJPV3$uedata=s:%2Frd%2Fuedata%3Fnoscript%26id%3D4CBB06SQR46C6W9DJPV3%26pty%3DError%26spty%3DPageNotFound%26pti%3D:2000' />

</noscript>`
  
  
  
  
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
  
  
  * Evidence: `1765056031`
  
  
  
  
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
  
  
  * Evidence: `2092574280`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `838795031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201909010`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2013944764`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `12187297`
  
  
  
  
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
  
  
  * Evidence: `464672031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `201909000`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `57004031`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2021312542`
  
  
  
  
* URL: [https://www.amazon.fr/](https://www.amazon.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `340855031`
  
  
  
  
Instances: 45
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1765056031, which evaluates to: 2025-12-06 21:20:31</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
* URL: [https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP](https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `field-keywords`
  
  
  
  
Instances: 32
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.amazon.fr/s/ref=404_search?field-keywords=ZAP</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [img] tag [alt] attribute </p><p></p><p>The user input found was:</p><p>field-keywords=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap: the interviews</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

  
  
  
  
### User Controllable JavaScript Event (XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.            </p>
  
  
  
* URL: [https://www.amazon.fr/l/14842072031?field-availability=-1&lo=amazon-devices&ref=gw_fr_desk_mso_acc_ep21_ilu_seemore&suppress-ve=1](https://www.amazon.fr/l/14842072031?field-availability=-1&lo=amazon-devices&ref=gw_fr_desk_mso_acc_ep21_ilu_seemore&suppress-ve=1)
  
  
  * Method: `GET`
  
  
  * Parameter: `suppress-ve`
  
  
  
  
Instances: 1
  
### Solution
<p>Validate all input and sanitize output it before writing to any Javascript on* events.</p>
  
### Other information
<p>User-controlled javascript event(s) was found. Exploitability will need to be manually determined. The page at the following URL:</p><p></p><p>https://www.amazon.fr/l/14842072031?field-availability=-1&lo=amazon-devices&ref=gw_fr_desk_mso_acc_ep21_ilu_seemore&suppress-ve=1"</p><p></p><p>includes the following Javascript event which may be attacker-controllable: </p><p></p><p>User-input was found in the following data of an [onclick] event:</p><p>return amz_js_PopWin(this.href,'AmazonHelp','width=550,height=550,resizable=1,scrollbars=1,toolbar=0,status=0');</p><p></p><p>The user input was:</p><p>1</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-javascript-event

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

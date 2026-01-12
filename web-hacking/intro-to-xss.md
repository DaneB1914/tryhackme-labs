# Intro to Cross-Site Scripting (XSS) — TryHackMe

**Learning Path:** Junior Penetration Tester  
**Module:** Introduction to Web Hacking  
**Date:** <Add date>  
**Author:** <Your Name>  
**Tags:** XSS, Web Security, Input Validation, OWASP  

---

## 1. Overview

This lab introduces Cross-Site Scripting (XSS) vulnerabilities and demonstrates how improper handling of user input can allow attackers to execute malicious JavaScript in a victim’s browser. The focus is on understanding *why* XSS occurs and how context affects exploitability.

---

## 2. What I Learned

- XSS vulnerabilities occur when user-controlled input is included in a web page without proper validation or output encoding.
- The **context** in which input is reflected (HTML, attribute, JavaScript) determines whether it is exploitable.
- Even simple input reflection can lead to serious impact if not handled correctly.
- XSS is often caused by logic and trust issues, not complex exploitation techniques.

---

## 3. XSS Types Covered

This room focused primarily on:
- **Reflected XSS** – user input is immediately reflected in the response
- Basic understanding of how XSS can be triggered through URL parameters or form input

---

## 4. Tools Used

- Web browser
- TryHackMe vulnerable web application
- Browser developer tools (for observing behavior)

*(Burp Suite can also be used in real-world testing, but was not required for this introductory lab.)*

---

## 5. High-Level Steps Performed

1. Identified areas of the application that accepted user input.
2. Observed how input was reflected back in the application response.
3. Tested simple JavaScript payloads to determine whether input was being executed.
4. Confirmed successful script execution in the browser context.

---

## 6. Impact

If exploited in a real application, XSS vulnerabilities could allow an attacker to:
- Steal session cookies
- Perform actions on behalf of users
- Deface pages
- Redirect users to malicious sites
- Execute arbitrary JavaScript in victims’ browsers

---

## 7. Defensive Insights / Remediation

To prevent XSS vulnerabilities:
- Validate and sanitize all user input.
- Apply proper **output encoding** based on context (HTML, JavaScript, attributes).
- Avoid trusting client-side validation alone.
- Use modern frameworks and security headers (e.g., Content Security Policy).

---

## 8. Key Takeaway

XSS is less about memorizing payloads and more about understanding **how data flows through an application**. Small mistakes in input handling or output encoding can quickly lead to serious security issues.

---

## 9. References

- TryHackMe — Intro to Cross-Site Scripting  
- OWASP Cross-Site Scripting (XSS) Guide  

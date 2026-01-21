# Authentication Bypass — TryHackMe

**Learning Path:** Junior Penetration Tester  
**Module:** Introduction to Web Hacking  
**Date:** 1/12/2026  
**Author:** Dane Babcock  
**Tags:** Authentication, Access Control, Web Security, OWASP  

---

## 1. Overview

This lab focuses on authentication bypass vulnerabilities and demonstrates how flaws in authentication logic can allow attackers to access restricted functionality without valid credentials. The emphasis is on understanding how trust assumptions and workflow mistakes lead to authentication failures.

---

## 2. What I Learned

- Authentication bypasses often stem from **logic flaws**, not complex exploits.
- Applications may assume users follow intended workflows, which attackers can bypass.
- Missing or inconsistent authentication checks across endpoints can expose sensitive functionality.
- Server-side enforcement is critical; client-side controls alone are insufficient.

---

## 3. Vulnerability Type

- **Authentication Bypass**
- Broken or missing authentication checks
- Flawed authentication workflows

---

## 4. Tools Used

- Web browser
- TryHackMe vulnerable web application
- Burp Suite (for intercepting and modifying requests)

---

## 5. High-Level Steps Performed

1. Identified application functionality intended only for authenticated users.
2. Intercepted requests related to authentication or protected resources.
3. Tested whether authentication checks were consistently enforced.
4. Confirmed access to restricted functionality without valid authentication.

---

## 6. Impact

If exploited in a real-world application, this vulnerability could allow an attacker to:
- Access protected pages or functionality
- Bypass login mechanisms
- Perform unauthorized actions
- Potentially escalate to further attacks depending on exposed functionality

---

## 7. Defensive Insights / Remediation

To prevent authentication bypass vulnerabilities:
- Enforce authentication checks server-side on every protected endpoint.
- Avoid relying on client-side controls or assumptions.
- Ensure consistent authentication logic across the application.
- Perform regular access control testing during development.

---

## 8. Key Takeaway

Authentication bypass vulnerabilities are often caused by **trusting user behavior instead of enforcing security rules**. Even simple logic mistakes can completely undermine an application’s security model.

---

## 9. References

- TryHackMe — Authentication Bypass  
- OWASP Authentication Cheat Sheet  


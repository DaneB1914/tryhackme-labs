# IDOR (Insecure Direct Object Reference) — TryHackMe

**Learning Path:** Junior Penetration Tester  
**Module:** Introduction to Web Hacking  
**Date:** 1/12/2026  
**Author:** Dane Babcock  
**Tags:** IDOR, Authorization, Access Control, Web Security  

---

## 1. Overview

This lab covers Insecure Direct Object Reference (IDOR) vulnerabilities and demonstrates how improper authorization checks can allow users to access or manipulate resources that do not belong to them. The focus is on understanding how user-controlled identifiers become security risks when not properly validated.

---

## 2. What I Learned

- IDOR vulnerabilities occur when applications trust user-supplied object identifiers.
- Authentication alone is not enough; **authorization must be enforced per object**.
- IDOR issues are common in APIs and modern web applications.
- These vulnerabilities are often easy to exploit but can have severe impact.

---

## 3. Vulnerability Type

- **Insecure Direct Object Reference (IDOR)**
- Broken access control
- Missing ownership or permission checks

---

## 4. Tools Used

- Web browser
- TryHackMe vulnerable web application
- Burp Suite (for intercepting and modifying requests)

---

## 5. High-Level Steps Performed

1. Identified requests containing object identifiers (e.g., user IDs, record IDs).
2. Intercepted and modified these identifiers in requests.
3. Observed application behavior after changing object references.
4. Confirmed unauthorized access to resources belonging to other users.

---

## 6. Impact

If exploited in a real application, an IDOR vulnerability could allow an attacker to:
- Access other users’ data
- Modify or delete unauthorized resources
- Bypass role-based access controls
- Cause significant data exposure or privacy violations

---

## 7. Defensive Insights / Remediation

To prevent IDOR vulnerabilities:
- Implement server-side authorization checks for every object request.
- Verify that the authenticated user owns or is permitted to access the requested resource.
- Avoid exposing predictable object identifiers when possible.
- Perform access control testing during development and security reviews.

---

## 8. Key Takeaway

IDOR vulnerabilities highlight the difference between **authentication** and **authorization**. Just because a user is logged in does not mean they should have access to every object in the application.

---

## 9. References

- TryHackMe — IDOR  
- OWASP Broken Access Control  



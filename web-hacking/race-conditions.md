# Race Conditions — TryHackMe

**Learning Path:** Junior Penetration Tester  
**Module:** Introduction to Web Hacking  
**Date:** 12/28/2025  
**Author:** Dane Babcock  
**Tags:** Race Conditions, Business Logic, Web Security, Burp Suite  

---

## 1. Overview

This lab focuses on race condition vulnerabilities and demonstrates how flaws in application logic can be exploited when multiple requests are processed simultaneously. The room highlights how time-of-check vs time-of-use (TOCTOU) issues can allow attackers to bypass intended restrictions.

---

## 2. What I Learned

- Race conditions occur when applications fail to properly handle **concurrent requests**.
- Server-side logic may assume requests are processed sequentially, which attackers can exploit.
- These vulnerabilities are often found in business logic rather than traditional input validation.
- Tools like **Burp Suite Repeater** are effective for testing concurrency and timing issues.

---

## 3. Vulnerability Type

- **Race Condition**
- Business logic flaw
- Time-of-check vs time-of-use (TOCTOU)

---

## 4. Tools Used

- Burp Suite Repeater
- Web browser
- TryHackMe vulnerable web application

---

## 5. High-Level Steps Performed

1. Identified functionality where the application enforced limits or checks (e.g., one-time actions, balance updates, or restricted operations).
2. Intercepted the relevant request using Burp Suite.
3. Sent identical requests to **Burp Repeater**.
4. Triggered multiple requests **simultaneously** to exploit timing issues.
5. Observed that the application processed requests in parallel without properly validating state changes.
6. Confirmed unintended behavior due to concurrent execution.

---

## 6. Impact

If exploited in a real-world application, this vulnerability could allow an attacker to:
- Perform actions multiple times when they should be limited
- Bypass business rules or restrictions
- Abuse financial or transactional logic (e.g., double spending)
- Gain unauthorized access or elevated privileges depending on context

Race conditions often result in **high-impact outcomes** despite appearing subtle.

---

## 7. Defensive Insights / Remediation

To prevent race condition vulnerabilities:
- Implement proper server-side locking or synchronization mechanisms.
- Validate state changes atomically.
- Avoid relying on client-side enforcement or assumptions about request order.
- Design backend logic to safely handle concurrent requests.
- Include concurrency testing as part of security reviews.

---

## 8. Key Takeaway

Race condition vulnerabilities demonstrate that security issues are not always about malicious input — they are often about **timing, assumptions, and state management**. Understanding application behavior under concurrent requests is essential for effective penetration testing.

---

## 9. References

- TryHackMe — Race Conditions  
- OWASP Top 10: Business Logic Vulnerabilities  
- PortSwigger — Race Conditions

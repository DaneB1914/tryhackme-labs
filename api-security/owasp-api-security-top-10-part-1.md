# OWASP API Security Top 10 — Part 1

**Platform:** TryHackMe  
**Category:** API Security Fundamentals  
**Date:** 1/21/2026  
**Author:** Dane Babcock  

---

## Overview

This room introduces the OWASP API Security Top 10 and focuses on common vulnerability classes that affect modern API-driven applications. The emphasis is on understanding how API architectures differ from traditional web applications and why they introduce unique security risks.

---

## Key Concepts Covered

- Differences between web application and API attack surfaces
- Common API security weaknesses such as:
  - Broken object level authorization (BOLA)
  - Excessive data exposure
  - Lack of proper access control
- The importance of server-side validation in API endpoints
- Why APIs are a high-value target in modern applications

---

## Practical Takeaways

- APIs often expose functionality directly, making authorization flaws especially dangerous.
- Client-side restrictions are meaningless without strong server-side enforcement.
- API vulnerabilities frequently result in data exposure rather than visible UI issues.
- Testing APIs requires careful inspection of requests and responses, not just browser interaction.

---

## Why This Matters in Penetration Testing

Most modern applications rely heavily on APIs, and many critical vulnerabilities occur at the API layer rather than the frontend. Understanding common API security failures is essential for effective web and mobile penetration testing.

This room provides foundational knowledge that supports later hands-on API exploitation and assessment work.

---

## References

- OWASP API Security Top 10
- TryHackMe — OWASP API Security Top 10 (Part 1)

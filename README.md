# Insecure Direct Object Reference (IDOR) Learning Project
![Patience IDOR Exploit](https://img.shields.io/badge/Patience_IDOR-Exploit-black?style=for-the-badge&logo=hackthebox&logoColor=00ff99&labelColor=4b0082)

A hands-on exploitation walkthrough from Ashley Hopkins (Patience) — Cybersecurity & Network Engineering Student  

---

## Overview  
This project documents my exploitation of an **Insecure Direct Object Reference (IDOR)** vulnerability inside a TryHackMe learning environment.  
IDOR occurs when an application exposes internal object identifiers (like `user_id`, `account_id`, or `file_id`) **without verifying whether the logged-in user is actually authorized to access that object**.

In simple terms:  
> *“If you change a number in the URL and suddenly see someone else’s data — that’s IDOR.”*

This vulnerability is part of the **OWASP Top 10: Broken Access Control**, one of the most common and dangerous real-world security issues.

---

## What I Did  
- Authenticated into the target application  
- Observed API requests through the browser’s developer tools  
- Identified the endpoint that exposed `user_id`  
- Manipulated the `user_id` value to access other users’ account data  
- Confirmed the IDOR by locating the parent who had **10 children**  
- Documented the exploitation process and results  

---

## Lessons Learned  
- Never trust user-controlled identifiers  
- Always enforce **server-side authorization checks**  
- Random IDs (UUIDs) ≠ secure authorization  
- Horizontal + vertical privilege escalation must both be tested  
- Logging and monitoring should detect unusual access patterns  

---

## How to Prevent IDOR  
- Enforce permission checks on every sensitive request  
- Use access control middleware on backend services  
- Validate ownership of resources (`owner_id == user.id`)  
- Avoid exposing predictable identifiers  
- Implement role-based access control (RBAC)  

---

## Author  
**Ashley Hopkins (Patience)**  
Cybersecurity & Network Engineering Student  
Focused on ethical hacking, network security, and hands-on exploitation labs.

---

## 🏷 Repository Topics  
`cybersecurity` · `idor` · `owasp` · `broken-access-control` ·  
`advent-of-cyber` · `web-security` · `learning-project`  

---

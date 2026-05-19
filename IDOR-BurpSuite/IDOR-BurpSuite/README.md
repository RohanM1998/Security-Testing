# Finding and Exploiting IDOR using Burp Suite

## Overview
During web application testing, I intercepted HTTP requests using Burp Suite and observed that user account details were fetched using a parameter such as:

/api/user/profile?id=1023

By modifying the ID parameter to another value:

/api/user/profile?id=1024

I was able to access another user’s profile data without proper authorization.

## Vulnerability
This confirmed an **Insecure Direct Object Reference (IDOR)** vulnerability under OWASP Top 10 Broken Access Control.

## Tools Used
- Burp Suite Intercept
- Burp Repeater for parameter tampering

## Impact
Unauthorized access to sensitive user information.

## Remediation
Server-side access control validation to ensure users can only access their own data.

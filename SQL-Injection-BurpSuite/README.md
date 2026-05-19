# Identifying SQL Injection using Burp Suite

## Overview
During web application security testing on a deliberately vulnerable platform, I tested input fields for improper input validation.

While intercepting a login request in Burp Suite, I modified the username parameter to:

' OR '1'='1

The application responded with successful authentication, indicating a SQL Injection vulnerability due to lack of input sanitization.

## Vulnerability
This demonstrated a classic **SQL Injection** issue under OWASP Top 10 Injection category.

## Tools Used
- Burp Suite Intercept and Repeater
- Manual payload manipulation

## Impact
An attacker could bypass authentication and access unauthorized data from the backend database.

## Remediation
Use parameterized queries / prepared statements and proper input validation.

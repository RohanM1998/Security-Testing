# Exploiting Business Logic Flaw using Burp Suite

## Overview
During security testing on a deliberately vulnerable e-commerce style application in a lab environment, I identified a business logic flaw in the payment workflow.

The application calculated the final payable amount on the client side and trusted the modified value sent in the HTTP request without server-side validation.

## Testing Method

Using Burp Suite Intercept, I captured the payment request before it was sent to the server. The request contained a parameter representing the total price:

total_amount=799

By modifying this value in Burp Repeater to:

total_amount=1

The server accepted the manipulated value and processed the transaction successfully.

## Vulnerability
This demonstrated a **Business Logic Vulnerability** where the server trusted client-side data without validating the integrity of the transaction amount.

This type of issue is common in payment workflows when proper server-side validation is missing.

## Tools Used
- Burp Suite Intercept
- Burp Repeater for parameter manipulation

## Impact
An attacker could manipulate the payable amount, leading to financial loss and integrity issues in the application.

## Remediation
- Implement server-side validation for all payment-related parameters
- Recalculate total amount on the server
- Use integrity checks or signed parameters

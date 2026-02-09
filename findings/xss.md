# Vulnerability: Cross-Site Scripting (XSS)

## Vulnerability ID
FM-002

## OWASP Category
A03: Injection (OWASP Top 10)

## Description
Cross-Site Scripting (XSS) is a vulnerability that allows malicious scripts to be injected into trusted web pages. This occurs when user input is not properly validated or encoded before being rendered in the browser.

Analysis of application behavior indicated that user input was reflected in responses without adequate output encoding.

## Affected Component
- Endpoint: `/search`
- Input Field: Search query
- Request Method: GET

## Evidence (Behavioral Analysis)
User-supplied input entered into the search field was reflected back in the response content without sanitization, indicating improper handling of untrusted input.

## Impact
Potential impact includes:
- Theft of user session cookies
- Execution of unauthorized actions on behalf of users
- Defacement of application content
- Loss of user trust

## Likelihood
Medium  
The vulnerability is accessible through standard user interaction and does not require authentication.

## Risk Rating
**Medium**

| Factor        | Rating |
|--------------|--------|
| Impact       | Medium |
| Likelihood   | Medium |
| Overall Risk | Medium |

## Remediation Recommendations
- Encode output before rendering user input
- Implement Content Security Policy (CSP)
- Validate and sanitize all user input
- Use modern frontend frameworks that auto-escape output

## References
- OWASP XSS Prevention Cheat Sheet
- OWASP Top 10 – Injection


# Vulnerability: SQL Injection

## Vulnerability ID
FM-001

## OWASP Category
A03: Injection (OWASP Top 10)

## Description
SQL Injection is a vulnerability that occurs when user-supplied input is improperly validated and directly incorporated into SQL queries. This can allow an attacker to manipulate database queries, potentially leading to unauthorized data access, data modification, or application errors.

During analysis of application request logs, abnormal query patterns were identified in URL parameters, indicating insufficient input validation.

## Affected Component
- Endpoint: `/product`
- Parameter: `id`
- Request Method: GET

## Evidence (Log Analysis)
The following HTTP log entry indicates suspicious input being processed by the application:


This suggests that user input was interpreted as part of a database query, causing an internal server error.

## Impact
If successfully exploited, this vulnerability could allow:
- Unauthorized access to sensitive database records
- Exposure of customer or administrative data
- Modification or deletion of application data
- Application instability or crashes

## Likelihood
Medium  
The vulnerability is accessible through a publicly exposed parameter and does not appear to have sufficient input sanitization controls.

## Risk Rating
**High**

| Factor        | Rating |
|--------------|--------|
| Impact       | High   |
| Likelihood   | Medium |
| Overall Risk | High   |

## CVSS (Estimated)
Base Score: 8.0 (High)

## Remediation Recommendations
- Implement prepared statements and parameterized queries
- Apply strict server-side input validation
- Use allow-lists for acceptable input formats
- Suppress detailed database error messages from users
- Conduct regular secure code reviews and testing

## References
- OWASP SQL Injection: https://owasp.org/www-community/attacks/SQL_Injection
- OWASP Top 10 – Injection


---
name: security-audit
description: Scan the current codebase for security vulnerabilities and missing guardrails
---

Perform a comprehensive security audit of this project:

1. **Secrets scan**: Search all files for hardcoded API keys, passwords, tokens, connection strings. Check .env files are in .gitignore.

2. **Input validation**: Find all API endpoints and check if user input is validated before processing.

3. **Authentication**: Check if all non-public routes have authentication middleware.

4. **Database security**: Check for SQL injection vulnerabilities, missing RLS policies, unparameterized queries.

5. **CORS configuration**: Check if CORS is properly restricted (not wildcard).

6. **Error handling**: Check if error responses leak internal details (stack traces, DB errors).

7. **Dependencies**: Check for known vulnerabilities in dependencies.

8. **Headers**: Check if security headers are set (CSP, HSTS, X-Frame-Options).

For each issue found:
1. Show the file and line
2. Explain the vulnerability
3. Show the fix
4. Rate severity: CRITICAL / HIGH / MEDIUM / LOW

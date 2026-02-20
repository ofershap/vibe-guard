# Vibe Guard

**45% of AI-generated code has security flaws.** Vibe Guard is always-on security guardrails for
AI-generated code. It catches hardcoded secrets, missing auth, insecure database rules, and the 20
things AI agents forget before you deploy.

## What It Does

Vibe Guard is not a scanner. It embeds guardrails directly into your agent's behavior. Every time
the agent writes code, these rules apply. The agent is steered away from common security mistakes
before they reach your codebase.

- **Zero config** - no setup, no API keys
- **Zero auth** - nothing to sign up for
- **Always on** - works on every file the agent touches

## The 20 Things It Catches

1. Hardcoded secrets (API keys, passwords, tokens)
2. Missing input validation
3. Unprotected API routes
4. Missing Row-Level Security (Supabase/Postgres)
5. SQL injection (string interpolation in queries)
6. Wildcard CORS
7. Missing rate limiting on auth endpoints
8. HTTP in production
9. Weak password hashing (MD5, SHA1, plain text)
10. Missing security headers (CSP, HSTS, X-Frame-Options)
11. Error responses that leak stack traces
12. Unvalidated file uploads
13. Same config for dev and production
14. Logging sensitive data
15. Insecure cookie flags (missing httpOnly, secure, sameSite)
16. Never-expiring tokens
17. Missing CSRF protection
18. No Content Security Policy
19. Open redirect vulnerabilities
20. Unaudited dependencies

## Install

### Cursor IDE

```
/add-plugin vibe-guard
```

### Claude Code

```
/plugin install vibe-guard
```

### Skills only (any agent)

```bash
npx skills add ofershap/vibe-guard/vibe-guard
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## Commands

- `/security-audit` - Scan the codebase for vulnerabilities and missing guardrails
- `/production-check` - Run a pre-deployment checklist

## Why This Plugin?

AI agents are trained on code that includes insecure patterns. They default to quick solutions:
hardcoded keys, unvalidated input, unprotected routes. Vibe Guard changes that default. When you
ship AI-generated code, these guardrails are already in place.

## License

MIT

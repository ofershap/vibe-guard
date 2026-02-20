# Vibe Guard

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/skills.sh-vibe--guard-blue)](https://skills.sh/ofershap/vibe-guard/vibe-guard)

Always-on security guardrails for AI-generated code. Catches hardcoded secrets, missing auth, SQL injection, insecure cookies, wildcard CORS, and the 20 things AI agents forget before you deploy.

> 45% of AI-generated code has security flaws. Vibe Guard is not a scanner you run after the fact. It embeds guardrails directly into your agent's behavior so insecure patterns never reach your codebase. Zero config, zero auth, always on.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/vibe-guard/vibe-guard
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type | Name | Description |
|------|------|-------------|
| Skill | `vibe-guard` | 20 security rules covering secrets, auth, input validation, database, cookies, headers, and more |
| Rule | `security-guardrails` | Always-on behavioral rule that enforces security patterns on every file |
| Command | `/security-audit` | Scan the codebase for vulnerabilities and missing guardrails |
| Command | `/production-check` | Run a pre-deployment security checklist |

## The 20 Things It Catches

| # | Vulnerability | What agents do wrong |
|---|---------------|---------------------|
| 1 | Hardcoded secrets | API keys and passwords inline instead of env vars |
| 2 | Missing input validation | No Zod/Joi on user input |
| 3 | Unprotected API routes | No auth middleware on sensitive endpoints |
| 4 | Missing Row-Level Security | No RLS policies on Supabase/Postgres tables |
| 5 | SQL injection | String interpolation in queries instead of parameterized |
| 6 | Wildcard CORS | `allow_origins=["*"]` in production |
| 7 | No rate limiting | Auth endpoints without throttling |
| 8 | HTTP in production | Missing HTTPS enforcement |
| 9 | Weak password hashing | MD5, SHA1, or plain text instead of bcrypt/Argon2 |
| 10 | Missing security headers | No CSP, HSTS, X-Frame-Options |
| 11 | Stack trace leaks | Internal errors exposed to users |
| 12 | Unvalidated file uploads | No type/size checks on uploaded files |
| 13 | Same config for dev/prod | No environment-specific settings |
| 14 | Logging sensitive data | Tokens and passwords in log output |
| 15 | Insecure cookies | Missing httpOnly, secure, sameSite flags |
| 16 | Never-expiring tokens | No TTL on JWT or session tokens |
| 17 | Missing CSRF protection | No CSRF tokens on state-changing requests |
| 18 | No Content Security Policy | Missing CSP headers |
| 19 | Open redirects | Unvalidated redirect URLs |
| 20 | Unaudited dependencies | No `npm audit` or dependency scanning |

## Related Plugins

- [fastapi-best-practices](https://github.com/ofershap/fastapi-best-practices) - Secure FastAPI endpoint patterns
- [drizzle-best-practices](https://github.com/ofershap/drizzle-best-practices) - Type-safe database queries (prevents SQL injection by design)

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT

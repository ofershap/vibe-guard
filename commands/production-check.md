---
name: production-check
description: Run a pre-deployment checklist - verify your app is production-ready
---

Run through this production readiness checklist:

1. **Environment variables**: All secrets in env vars? .env in .gitignore? .env.example exists?
2. **Authentication**: All routes protected? Session management implemented?
3. **Input validation**: All user inputs validated? File uploads restricted?
4. **Database**: Parameterized queries? RLS enabled? Connection pooling configured?
5. **Error handling**: Generic errors in production? Structured logging? No console.log of sensitive data?
6. **Security headers**: CSP, HSTS, X-Frame-Options, X-Content-Type-Options set?
7. **Rate limiting**: Auth endpoints rate-limited? API endpoints rate-limited?
8. **CORS**: Specific origins only? No wildcard in production?
9. **HTTPS**: Forced in production? HSTS header set?
10. **Dependencies**: npm audit clean? No known vulnerabilities?

For each item: PASS / FAIL / NOT APPLICABLE with explanation.

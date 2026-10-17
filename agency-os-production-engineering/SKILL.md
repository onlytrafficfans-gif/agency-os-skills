---
name: agency-os-production-engineering
description: Secure, test, document, deploy, monitor, recover, and operate Agency OS across authentication, RBAC, privacy, CI/CD, Vercel, workers, audit logs, and tenant isolation. Use for cross-phase production engineering and Phase 8 hardening.
---

# Agency OS Production Engineering

Apply least privilege and defense in depth at every server boundary. Hidden navigation is not authorization. Check session, organization, role, tenant ownership, action permission, and validated input for each request and job.

## Release system

- Keep secrets in managed server-side storage, redact logs, rotate credentials, and scan source/dependencies for exposure.
- Test tenant isolation for reads, writes, exports, jobs, caches, webhooks, files, and administrative paths.
- Build CI/CD gates for formatting/type checks, migrations, unit/integration tests, Playwright critical paths, dependency scanning, and deploy health checks.
- Deploy the frontend to Vercel-compatible hosting and persistent jobs to durable worker infrastructure; never assume serverless request lifetime is a queue.
- Emit structured logs, correlation IDs, error tracking, health checks, provider/job metrics, budget alerts, and actionable incident signals.
- Back up critical data and prove restoration into an isolated environment. Document recovery objectives and credential rotation.

Maintain API specs, architecture decisions, environment documentation, provider limitations, incident runbooks, and operational checklists alongside code. Load/performance tests must model realistic pagination, concurrency, provider limits, database contention, and queues without triggering unauthorized paid or external actions.

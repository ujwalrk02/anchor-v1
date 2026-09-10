# Anchor — Internal Identity Platform

Centralized identity for all internal apps, so teams stop re-building login, sessions, password storage, and access control per project.

Anchor owns **who a user is and when they may act**. Applications keep ownership of **what a user can do with their own resources**.

This repo currently contains the developer docs site: `anchor-docs.html` (single-file, no build step — open it in a browser).

## Platform features

### Authentication
- Hosted login page (redirect, centrally maintained)
- Embedded login SDK (Beta) for in-UI flows
- Passwordless / passkeys (Beta): magic links, passkey sign-in
- SSO: OIDC (default, auth code + PKCE), SAML 2.0, cross-app SSO
- MFA: TOTP (default), WebAuthn / passkeys (Beta), SMS fallback (per-org), enforceable MFA policies
- Sessions & tokens: access / ID / refresh tokens, automatic refresh-token rotation, revocation, device & session management (Beta)
- Protections: brute-force protection and login rate limiting at platform level

### User management
- User CRUD via API / admin console, self-service profile + password reset
- Soft-delete + scheduled anonymization (Beta)
- Multi-tenancy with data-layer isolation, org / team hierarchy, delegated admin (Beta)
- SCIM provisioning / de-provisioning (Beta)

### Roles & access control
- Roles and permissions carried in tokens
- Conditional policy engine (Beta, path to ABAC)
- Immutable audit logging of logins, role changes, admin actions
- Access review / recertification prompts (Beta)

### Compliance & security
- SOC 2 Type II and ISO 27001 status tracking (Beta)
- GDPR + DPDP handling: consent, subject requests, cross-border transfers
- Encryption at rest (platform-managed keys) and in transit (TLS everywhere), key rotation runbooks (Beta)
- Retention policies per data category (Beta), PII classification + log masking (Beta)
- Breach notification process, pen-testing + vuln scanning cadence (Beta)

### Integrations
- Connector framework: one adapter interface for all providers, custom-connector guide
- Enterprise IdP federation: SAML and OIDC brokering
- KYC/AML: Persona and Onfido hooks (Beta)
- Social login: Google, GitHub, Microsoft

### Reliability & operations
- 99.95% monthly target for login and token issuance
- Per-client / per-tenant rate limits, horizontal scaling of stateless auth services, multi-region active-passive failover (Beta)
- Metrics, distributed tracing, alerting subscriptions
- Versioned APIs, backup / restore with tested recovery for the user directory

### SDKs and developer tools
- Web (JS/React) and backend (Node, Java, Python, .NET) GA; mobile (iOS/Android) and CLI in Beta
- API reference from the same spec as the SDKs, sandbox tenants, request-level debugging logs, webhooks for lifecycle events (Beta)

### Governance
- Platform Charter with scope boundaries and build-vs-buy decision tree
- Release management: semver, cadence + changelog, deprecation / sunset policy, compat guarantees
- ADRs: immutable chronological log + proposal template
- Migration guides: Okta / Auth0, Azure Entra ID, Keycloak (Beta)
- Runbooks: incident playbooks, on-call escalation, common failure modes

## Docs site features

- Three-column layout: collapsible sidebar nav, scrollable content, "On this page" outline with scroll-spy
- Top bar: version picker (`v2026.09` current), `Ctrl/Cmd + K` command palette with keyboard navigation, tabs for API Reference, SDKs, Roadmap, Release Notes, Status
- Home: pillar cards, popular guides, quickstart entry points
- Article pages: breadcrumbs, meta strip (area / stability / date), in-this-section lists, related pages, prev/next pager
- Feedback: per-page helpful Yes/No widget, Report issue / Suggest feature dialog with rating, validation, file attach, and preview
- Roadmap view (Phase 1 live Sept 2026, Phase 2 committed Q4 2026, Phase 3 sequenced H1 2027, Under evaluation), chronological Release Notes
- Single static file using vanilla JS/CSS and IBM Plex Sans/Mono; responsive with collapsible outline

## Visit Docs

https://fsit-anchor-v1.vercel.app/

# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability, please report it responsibly:

1. **Do NOT open a public GitHub issue**
2. Use GitHub's private vulnerability reporting feature: <https://github.com/civic-source/us-code/security/advisories/new>
3. Include: description, affected files or workflows, steps to reproduce, and potential impact
4. Allow 90 days for coordinated vulnerability disclosure and remediation before public disclosure

## What We Consider Security Issues

- Statutory Markdown or YAML sidecar data integrity tampering, malformed frontmatter injection, or path traversal
- Workflow, automation, or secret/credential exposure
- Dependency vulnerabilities with known exploits affecting repository tooling or data verification

## Response Timeline

We aim to acknowledge vulnerability reports within 48 hours and provide an initial triage and mitigation plan within 7 days for critical issues, following a 90-day coordinated disclosure timeline.

## Supported Versions

Only the latest release on `main` is actively supported with security updates.

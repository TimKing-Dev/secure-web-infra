# Secure Web Infrastructure (secure-web-infra)

An enterprise-hardened infrastructure deployment lab featuring an automated DevSecOps pipeline, static application security testing (SAST), and container security auditing.

## Security Posture

[![Dockerfile Security Lint](https://github.com/TimKing-Dev/secure-web-infra/actions/workflows/hadolint.yml/badge.svg)](https://github.com/TimKing-Dev/secure-web-infra/actions/workflows/hadolint.yml)

## Pipeline Architecture
- **Static Analysis:** Hadolint (Docker Security Linter)
- **Reporting Engine:** SARIF (Static Analysis Results Interchange Format) export
- **Dashboard Integration:** GitHub Advanced Security / Code Scanning Alerts

## Getting Started
To trigger the automated security scanning pipeline, make modifications to the root `Dockerfile` and push changes directly to the primary branch:

```bash
git add Dockerfile
git commit -m "Secure: Hardening container runtime"
git push origin main

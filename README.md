# 🦉 OAuthX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OAuthX** — OAuth 2.0 / OpenID Connect Config Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OAuthX is an offline auditor for OAuth 2.0 and OpenID Connect configuration, defaulting to read-only with no network access unless --fetch is given. A tolerant JSON loader and framework adapters let it ingest Authorization Server metadata, client registrations and exports from Keycloak, Azure AD, Google, Spring Security, Django OAuth Toolkit and Authlib. More than 40 rules are mapped to RFC 9700, RFC 6819, RFC 7636 and OIDC Core with a weighted score and A…F grade.

---

## ✨ Features

- Audits AS metadata (RFC 8414) and client registrations (RFC 7591 / OIDC DCR)
- Framework adapters: Keycloak, Azure AD, Google, Spring, Django OAuth, Authlib
- Redirect-URI analysis (http, wildcards, loopback-in-prod, custom schemes)
- Authorize/token request analysis for state, nonce, PKCE and secrets in URLs
- 40+ rules mapped to RFC 9700/6819/7636, OIDC Core and CWE with scoring
- Optional HTTPS metadata fetch (--fetch) and export TXT/MD/JSON/CSV/SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAuthX --metadata openid-configuration.json
./OAuthX --client keycloak-client.json --env production --fail-on high
./OAuthX --scan ./ --format sarif -o report.sarif
./OAuthX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OAuthX --help   # watch every network call
firejail --net=none ./OAuthX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)

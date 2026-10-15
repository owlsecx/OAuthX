# 🦉 OAuthX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OAuthX** — OAuth 2.0 / OpenID Connect Config Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline OAuth 2.0 / OpenID Connect client & provider configuration auditor

---

## ✨ Features

- Offline auditor for OAuth 2.0 / OIDC configuration (read-only, no network unless --fetch is given)
- Tolerant JSON loader — BOM, comments, trailing commas, single quotes, JSON fragments; never crashes
- Authorization Server metadata audit (/.well-known/openid-configuration, RFC 8414)
- Client registration audit (RFC 7591 / OIDC DCR)
- Framework adapters — Keycloak client & realm export, Azure AD app manifest, Google client_secrets.json, Spring Security OAuth (properties / YAML), Django OAuth Toolkit settings, Authlib register() calls
- Redirect-URI list analyzer (http, wildcards, loopback in prod, fragments, custom schemes)
- Authorize / token request sample analyzer (state, nonce, PKCE, response_type, secrets in URL)
- 40+ rules mapped to RFC 9700 (OAuth Security BCP), RFC 6819, RFC 7636, OIDC Core and CWE
- Weighted score + A…F grade, severity filter, CI gate
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Optional HTTPS fetch of well-known metadata (--fetch)
- Built-in self-test (--demo) with expected detections

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAuthX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*

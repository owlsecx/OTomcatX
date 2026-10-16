# 🦉 OTomcatX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OTomcatX** — Apache Tomcat Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline Apache Tomcat / Java servlet container configuration auditor

---

## ✨ Features

- Offline, read-only audit of a whole CATALINA_BASE (or individual config files) — stdlib only
- server.xml — shutdown port/command, AJP / Ghostcat (CVE-2020-1938), plaintext HTTP connectors, weak TLS protocols & ciphers, server header, xpoweredBy, allowTrace, autoDeploy, valves (AccessLog, Remote Addr/CIDR, ErrorReport showReport / showServerInfo)
- tomcat-users.xml — default credentials, plaintext and weak / duplicate passwords (always masked), over-privileged manager-script / manager-jmx roles
- web.xml — DefaultServlet listings & readonly (CVE-2017-12617), security-constraint, transport guarantee, session timeout, cookie flags, error pages
- context.xml — privileged, crossContext, resource locking, manager / host-manager address restriction
- catalina.properties / catalina.policy / setenv.sh — JMX remote auth/SSL, JPDA debug, security manager
- webapps — examples / docs / ROOT / host-manager, file permissions, Tomcat version & EOL detection
- CWE / CVE / CIS Apache Tomcat Benchmark mapping, severity, remediation, score & A+…F grade
- Exports TXT / Markdown / JSON / CSV / SARIF 2.1.0
- CI gates (--fail-on, --min-severity), self-test demo

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OTomcatX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*

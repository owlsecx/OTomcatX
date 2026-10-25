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


OTomcatX is an offline, read-only Apache Tomcat configuration auditor that analyses an entire CATALINA_BASE or individual files using stdlib only. It reviews server.xml (shutdown port, AJP/Ghostcat, plaintext connectors, TLS, valves), tomcat-users.xml (default/weak credentials, over-privileged roles), web.xml, context.xml and catalina properties/policy. Findings are mapped to CWE/CVE and the CIS Tomcat Benchmark, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Audits a whole CATALINA_BASE or individual server.xml/tomcat-users.xml/web.xml/context.xml files
- server.xml checks: shutdown port/command, AJP Ghostcat (CVE-2020-1938), plaintext HTTP, weak TLS, valves
- tomcat-users.xml: default/plaintext/weak/duplicate passwords (masked) and over-privileged manager roles
- web.xml DefaultServlet listings/readonly (CVE-2017-12617), security constraints and cookie flags
- context.xml privileged/crossContext and catalina.properties/policy/setenv (JMX, JPDA, security manager)
- webapps inventory, version/EOL detection, CWE/CVE/CIS mapping and TXT/MD/JSON/CSV/SARIF export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OTomcatX -b /opt/tomcat -f sarif -o tomcat.sarif
./OTomcatX --server-xml /opt/tomcat/conf/server.xml --users-xml /opt/tomcat/conf/tomcat-users.xml
./OTomcatX -s --fail-on high --json
./OTomcatX --demo
./OTomcatX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*

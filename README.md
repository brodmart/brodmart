 ## Martin Brodeur — Independent Security Researcher                                                                                        

I develop automated methods for finding vulnerability classes that SAST structurally cannot detect.

## Recent CVEs (10 live · 3 imminent)

**Docling / IBM Research Zurich — bulk acceptance Jun 02 2026 (6 CVEs, one cycle):**
- CVE-2026-44023 — docling-core remote filename resolution: SSRF + Content-Disposition path traversal (HIGH 9.4, AV:N/UI:N)
- CVE-2026-44016 — docling Playwright unrestricted JS + network (HIGH 9.0, scope-change)
- CVE-2026-44019 — docling-core image URI validation: file:// + unbounded data: (HIGH 8.0)
- CVE-2026-47214 — docling HTML backend URI/path handling (HIGH 7.7)
- CVE-2026-44018 — docling METS-GBS XXE + zip-bomb (MODERATE 5.5)
- CVE-2026-44022 — docling LaTeX \includegraphics / \input path traversal (MODERATE 5.5)

**Prior CVEs:**
- CVE-2026-41586 — Hyperledger Fabric SDK Java RCE (CRITICAL 9.0; deployed at Walmart / Maersk / HSBC)
- CVE-2026-6859 — InstructLab trust_remote_code RCE (HIGH 8.8, Red Hat PSIRT)
- CVE-2026-6855 — InstructLab logs_dir path traversal (Red Hat PSIRT)
- CVE-2026-44936 — Rancher Fleet SSRF → BasicAuth credential exfiltration (co-credit NATO NCSC)

**Imminent (assigned, pending publish):**
- CVE-2026-47256 — OpenTelemetry Sentry exporter path traversal (fix PR approved)
- Samsung DSPRODSEC-967 — SCSC wlbt WiFi driver heap overflow via attacker-controlled SSID IE length (CWE-78; CVE committed by Samsung DS PSIRT)
- Hyperledger fabric-ca GHSA-xghw-p77p-3r7x — pre-auth LDAP injection (CWE-90; CVE requested by maintainer Jun 01 2026)

## Scope

260+ coordinated disclosures across IBM Research, Microsoft, Google, Apple (swift-nio), Hyperledger, OpenTelemetry, Samsung, and AI/ML infrastructure (vLLM, MLflow, Gradio, Dify, OpenWebUI, Haystack, BentoML, LlamaIndex, AutoGen, granite-tsfm, and others).

Method is patent-pending. Findings are responsibly disclosed.

Licensing and structured engagement inquiries: admin@fluentlogic.org
Research: orthant.org

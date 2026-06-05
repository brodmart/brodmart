```markdown
# Martin Brodeur — Independent Security Researcher
I develop automated methods for finding vulnerability classes that SAST structurally cannot detect. Method emphasizes live-toolchain reproduction over static-analysis claims — every filing includes container-reproducible evidence.
## Recent CVEs (10 live · 4 imminent · 1 vendor-direct advisory)
**Docling / IBM Research Zurich:**
- **CVE-2026-44023** — docling-core remote filename resolution: SSRF + Content-Disposition path traversal (HIGH 9.4, AV:N/UI:N)
- **CVE-2026-44016** — docling Playwright unrestricted JS + network (HIGH 9.0, scope-change)
- **CVE-2026-44019** — docling-core image URI validation: `file://` + unbounded `data:` (HIGH 8.0)
- **CVE-2026-47214** — docling HTML backend URI/path handling (HIGH 7.7)
- **CVE-2026-44018** — docling METS-GBS XXE + zip-bomb (MODERATE 5.5)
- **CVE-2026-44022** — docling LaTeX `\includegraphics` / `\input` path traversal (MODERATE 5.5)
**Prior CVEs:**
- **CVE-2026-41586** — Hyperledger Fabric SDK Java RCE (CRITICAL 9.0; deployed at Walmart / Maersk / HSBC)
- **CVE-2026-6859** — InstructLab `trust_remote_code` RCE (HIGH 8.8, Red Hat PSIRT)
- **CVE-2026-6855** — InstructLab `logs_dir` path traversal (Red Hat PSIRT)
- **CVE-2026-44936** — Rancher Fleet SSRF → BasicAuth credential exfiltration (co-credit NATO NCSC)
**Imminent (assigned, pending publish):**
- **CVE-2026-47256** — OpenTelemetry Sentry exporter path traversal (fix PR #1 merged, v0.154.0 release pending)
- **Samsung DSPRODSEC-967** — SCSC wlbt WiFi driver heap overflow via attacker-controlled SSID IE length (CWE-78; CVE committed by Samsung DS PSIRT)
- **Hyperledger fabric-ca GHSA-xghw-p77p-3r7x** — pre-auth LDAP injection (CWE-90; CVE requested by maintainer Jun 01 2026)
- **open-webui GHSA-9rpj-v7hf-vv2w** — `url_idx` vulnerability
**Vendor-direct advisory (CVE pending coordinated disclosure):**
- **w1.fi 2026-1** — wpa_supplicant / hostapd, "Missing multi-link parsing validation in wpa_supplicant and hostapd" (published Jun 5 2026). Credited for incorrect validation of MLE common info length. Fixes landed in `bss.c` (Wi-Fi 7 scan-result parsing, commit `595194d`) and the MLD association-failure path (commit `41c86a2`). One of three independent reporters credited in the 2026-1 bundle. Advisory: https://w1.fi/security/2026-1/
## Scope
260+ coordinated disclosures across IBM Research, Microsoft, Google, Apple (swift-nio), Hyperledger, OpenTelemetry, Samsung, AI/ML infrastructure (vLLM, MLflow, Gradio, Dify, OpenWebUI, Haystack, BentoML, LlamaIndex, AutoGen, granite-tsfm, and others), and the wireless stack (wpa_supplicant / hostapd via w1.fi direct).
Method is patent-pending. Findings are responsibly disclosed.
Research correspondence: admin@fluentlogic.org · Research site: orthant.org
```

```text
# Martin Brodeur — Independent Security Researcher

I develop automated methods for finding vulnerability classes that SAST structurally cannot detect. Method emphasizes live-toolchain reproduction over static-analysis claims — every filing includes container-reproducible evidence.

## Recent CVEs (20 issued · 2 pending publish · 1 vendor-direct advisory)

**Docling / IBM Research Zurich (Jun 02 2026, 6-CVE cluster):**
- CVE-2026-44023 — docling-core remote filename resolution: SSRF + Content-Disposition path traversal (HIGH 9.4, AV:N/UI:N)
- CVE-2026-44016 — docling Playwright unrestricted JS + network execution (HIGH 9.0, scope-change)
- CVE-2026-44019 — docling-core image URI validation: file:// + unbounded data: (HIGH 8.0)
- CVE-2026-47214 — docling HTML backend URI/path handling (HIGH 7.7)
- CVE-2026-44018 — docling METS-GBS XXE + zip-bomb (MODERATE 5.5)
- CVE-2026-44022 — docling LaTeX \includegraphics / \input path traversal (MODERATE 5.5)

**OpenTelemetry (Jun 17 + Jun 24 2026):**
- CVE-2026-57444 — opentelemetry-collector-contrib syslog newline-injection → SIEM forgery (HIGH 8.2, CWE-93+116; advisory GHSA-xrp2-w94v-4w68)
- CVE-2026-47256 — opentelemetry-collector-contrib Sentry exporter path traversal (MODERATE 5.3; v0.154.0 patch shipped)

**Hyperledger (Jun 18 2026):**
- CVE-2026-53658 — Hyperledger fabric-ca pre-auth LDAP injection at `lib/server/ldap/client.go:175` (MODERATE 5.3, CWE-90; fix `d379df8` → v1.5.21)

**Red Hat / Ansible / Pulpcore (Jun 19 2026):**
- CVE-2026-12726 — Ansible/AWX GitHub webhook SSRF + PAT exfiltration (HIGH 7.5, CWE-918; Red Hat CNA — RH page acknowledges "Martin Brodeur, FluentLogic")
- CVE-2026-12701 — Pulp/Pulpcore relative_path_validator ../ bypass → FilesystemExport arbitrary write (HIGH 9.0; embargoed until backport ships)

**Open WebUI (Jun 11 2026):**
- CVE-2026-54021 — Ollama backend `url_idx` path-parameter bypass (MODERATE 6.3; patched in v0.9.6 via model→backend allow-list)

**vLLM (Jun 12 + Jun 17 2026):**
- CVE-2026-55574 — `structured_outputs.regex` unwrapped compile → ReDoS in xgrammar + outlines backends (MODERATE; CWE-1333; PR #45118 merged)
- CVE-2026-54235 — `SamplingParams._verify_args()` temperature=NaN/Infinity bypass propagates to GPU kernels (MODERATE; CWE-1287; advisory GHSA-7h4p-rffg-7823)

**ManageIQ (Red Hat CNA, Jun 09 2026):**
- CVE-2026-52903 — ManageIQ YAML safe_load→unsafe_load production fallback in `lib/extensions/yaml_load_aliases.rb` (HIGH 8.8, AV:N/PR:L; CWE-502 deserialization → Ruby Psych RCE)

**Samsung (Jun 07 2026):**
- CVE-2026-47320 — Samsung rlottie PathData empty-frames + Layer recursion DoS (MODERATE 6.1, CWE-824+CWE-674; fix in PR Samsung/rlottie#593; Samsung TV & Appliance CNA, MSP I-121052)

**Earlier 2026:**
- CVE-2026-41586 — Hyperledger Fabric SDK Java RCE (CRITICAL 9.0; deployed at Walmart / Maersk / HSBC)
- CVE-2026-44936 — Rancher Fleet SSRF → BasicAuth credential exfiltration (co-credit NATO NCSC)
- CVE-2026-6859 — InstructLab trust_remote_code RCE (HIGH 8.8, Red Hat PSIRT)
- CVE-2026-6855 — InstructLab logs_dir path traversal (Red Hat PSIRT)

## Pending publish (CVE committed by vendor, ID pending)
- Samsung DSPRODSEC-967 — SCSC wlbt WiFi driver heap overflow via attacker-controlled SSID IE length (CVE committed by Samsung DS PSIRT)
- Quay/Clair SSRF (CVE committed by Red Hat PSIRT — Mihail Milev confirmed assignment proceeding at agreed CVSS)

## Vendor-direct advisory (CVE pending coordinated disclosure)
- **w1.fi 2026-1** — wpa_supplicant / hostapd, *"Missing multi-link parsing validation in wpa_supplicant and hostapd"* (published Jun 5 2026). Credited as "Martin Brodeur, at Fluentlogic" for incorrect validation of MLE common info length. Fixes landed in `bss.c` (Wi-Fi 7 scan-result parsing, commit `595194d`) and the MLD association-failure path (commit `41c86a2`). One of three independent reporters credited in the 2026-1 bundle. Advisory: https://w1.fi/security/2026-1/

## Scope
260+ coordinated disclosures across IBM Research, Microsoft, Google, Apple (swift-nio), Hyperledger, OpenTelemetry, Samsung, Red Hat / ManageIQ / Ansible / Pulpcore, AI/ML infrastructure (vLLM, MLflow, Gradio, Dify, Open WebUI, Haystack, BentoML, LlamaIndex, AutoGen, granite-tsfm, and others), and the wireless stack (wpa_supplicant / hostapd via w1.fi direct).

Method is patent-pending. Findings are responsibly disclosed.
Research correspondence: admin@fluentlogic.org · Research site: orthant.org
```

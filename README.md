<div align="center">

# Harshit Neog

**Computer Science & Engineering (AI/ML) Student · Open-Source Developer Tooling & Systems Engineering**

[![GitHub](https://img.shields.io/badge/GitHub-Laggy--Ryon-181717?style=flat-square&logo=github)](https://github.com/Laggy-Ryon)
[![Jenkins Community](https://img.shields.io/badge/Jenkins_Discourse-@laggy--ryon-D24939?style=flat-square&logo=jenkins&logoColor=white)](https://community.jenkins.io/u/laggy-ryon)

</div>

First-year CSE (AI/ML) undergraduate building developer tooling, CI/CD infrastructure, static analysis checks, and deterministic AI safety systems. Active contributor across **Jenkins**, **Apicurio (CNCF)**, and **Checkstyle** with a focus on Java ecosystems, OpenRewrite migrations, and reliable systems engineering.

---

## Snapshot

| Metric | Details |
| :--- | :--- |
| **Upstream OSS Merged** | **5 PRs** across `jenkinsci`, `Apicurio` (CNCF), and `checkstyle` |
| **Upstream OSS Active** | **4 PRs** (`1` Approved with Auto-Merge, `2` CI-Green awaiting review, `1` In Review with SonarQube Quality Gate passed) |
| **Project Contributions** | Core author of [`triage3am`](https://github.com/Laggy-Ryon/triage3am) and autonomous agent firewall module `@mandate/agent` ([`VinayKhandia/mandate`](https://github.com/VinayKhandia/mandate)) |
| **Core Stack** | Java (17/25), TypeScript, Python, Maven, OpenRewrite, Checkstyle, SpotBugs, Vitest, Zod |

---

## Open-Source Contributions

### Jenkins Ecosystem (`jenkinsci` / `jenkins-infra`)

| Repository | Pull Request | Engineering Scope & Impact | Status |
| :--- | :--- | :--- | :--- |
| `jenkinsci/configuration-as-code-plugin` | [PR #2929](https://github.com/jenkinsci/configuration-as-code-plugin/pull/2929) | Excludes static methods and static fields during configurator introspection and attribute resolution while preserving superclass hierarchy traversal (`JENKINS-75170`), preventing `StackOverflowError` on classes with static helpers or singletons. | **Approved / Auto-Merge** (16/16 CI checks passing) |
| `jenkinsci/plugin-installation-manager-tool` | [PR #979](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/979) | Surfaces both the declaring parent plugin and the missing dependency when transitive plugin resolution fails ([#865](https://github.com/jenkinsci/plugin-installation-manager-tool/issues/865)), backed by regression unit tests. | **Merged** |
| `jenkinsci/plugin-installation-manager-tool` | [PR #972](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/972) | Implemented fail-fast HTTP 404 handling without redundant mirror retries, demoted expected download errors from `stderr`, and standardized concise diagnostics ([#562](https://github.com/jenkinsci/plugin-installation-manager-tool/issues/562)) with WireMock, unit, and integration tests. | **Merged** |
| `jenkinsci/plugin-installation-manager-tool` | [PR #970](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/970) | Validates user-specified Jenkins WAR paths before execution and returns a non-zero exit code when missing ([#641](https://github.com/jenkinsci/plugin-installation-manager-tool/issues/641)). | **Merged** |
| `jenkins-infra/plugin-modernizer-tool` | [PR #2031](https://github.com/jenkins-infra/plugin-modernizer-tool/pull/2031) | Authored a declarative `ModernizeCollections` OpenRewrite recipe migrating legacy/Guava initializations to Java 17 collection factory methods and `Stream.toList()` ([#1169](https://github.com/jenkins-infra/plugin-modernizer-tool/issues/1169)), including JTE PR templates, metadata validator registration, and test coverage. | **Open** (12/12 CI checks passing) |
| `jenkinsci/git-client-plugin` | [PR #1801](https://github.com/jenkinsci/git-client-plugin/pull/1801) | Exports formatted `no_proxy` and `NO_PROXY` environment variables for CLI Git subprocesses behind HTTP proxies (`JENKINS-61193` / [#1613](https://github.com/jenkinsci/git-client-plugin/issues/1613)), verified with 12 unit tests (`CliGitAPIImplNoProxyHostTest`). | **Open** (15/15 CI checks passing) |

### Apicurio Registry (`Apicurio` — CNCF)

| Repository | Pull Request | Engineering Scope & Impact | Status |
| :--- | :--- | :--- | :--- |
| `Apicurio/apicurio-registry` | [PR #10905](https://github.com/Apicurio/apicurio-registry/pull/10905) | Fixed malformed console log timestamp patterns across Quarkus runtime and Kubernetes operator controller configurations to ensure ISO-8601 compliance ([#10757](https://github.com/Apicurio/apicurio-registry/issues/10757)). | **Merged** |
| `Apicurio/apicurio-registry` | [PR #10993](https://github.com/Apicurio/apicurio-registry/pull/10993) | Implemented `ParameterValidationUtils.validateRuleConfig` to enforce rule configuration validation (`ValidityLevel`, `CompatibilityLevel`, `IntegrityLevel`) across `AdminResourceImpl` and `GroupsResourceImpl` ([#10722](https://github.com/Apicurio/apicurio-registry/issues/10722)) with unit and integration tests; addressed reviewer feedback. | **Open / In Review** (SonarQube Quality Gate passed) |

### Checkstyle

| Repository | Pull Request | Engineering Scope & Impact | Status |
| :--- | :--- | :--- | :--- |
| `checkstyle/checkstyle` | [PR #22393](https://github.com/checkstyle/checkstyle/pull/22393) | Removed obsolete suppression comments and aligned test fixture structure for `CommentsIndentationCheck` ([#19803](https://github.com/checkstyle/checkstyle/issues/19803)). | **Merged** |

- Community Introduction: [Jenkins Community Forum — Introducing myself to the Jenkins ecosystem for GSoC 2027](https://community.jenkins.io/t/harshit-neog-introducing-myself-to-the-jenkins-ecosystem-for-gsoc-2027/37456)

---

## Selected Projects

### [triage3am](https://github.com/Laggy-Ryon/triage3am) — Zero-Dependency Incident Triage Engine
`Python (Standard Library)` · `Multi-Threaded HTTP Server` · `REST API` · `HTML / CSS / JS`

A deterministic AIOps log analysis engine and web dashboard that distills 10,000+ raw outage log lines into ranked root-cause diagnoses and remediation playbooks in ~0.18s without external dependencies or LLM calls.
- **Drain-Inspired Template Clustering**: Masks variable tokens (UUIDs, IPs, memory addresses, timestamps, IDs) in a single pass to collapse noisy retry storms into structured incident templates.
- **Root-Cause & Cascade Inference**: Prioritizes earliest anomalous triggers ("patient zero") by timing, burst rate, cross-service blast radius, and stack severity, reconstructing `T0 -> T1 -> T2` failure propagation chains.
- **Production-Safe Ingestion**: Features a threaded HTTP server, lazy streaming iterators, magic-byte `.gz` decompression, traversal-safe path handling (`SafePathManager`), 11 built-in diagnostic runbooks, and Slack/Markdown/CSV/JSON post-mortem exports.

### [Mandate (`@mandate/agent`)](https://github.com/VinayKhandia/mandate) — AI Agent Spending Firewall & Intent Ledger
`TypeScript (Strict)` · `Node.js` · `Zod` · `Vitest` · `Google Gemini API` · `SHA-256`

A deterministic payment authorization guardrail sitting between autonomous AI shopping agents and payment rails so compromised or prompt-injected agents cannot spend outside user-signed boundaries ([Architecture Fork](https://github.com/Laggy-Ryon/mandate)).
- **Privilege Separation**: Designed `@mandate/agent` around a create-only `PayPalCreateOrderClient` boundary so capture/void credentials never touch the agent runtime.
- **Untrusted LLM Guardrails**: Enforces strict `zod` schema validation on model outputs, integer minor-unit arithmetic verification, secret redaction, and SSRF-guarded HTML extraction (`browsePage`).
- **Adversarial Verification**: Built a 5-scenario staged prompt-injection attack suite (`/injected`, `/wrong-merchant`, `/currency-switch`, `/social-engineering`, `/clean`), cryptographically hashed SHA-256 Intent Receipts, and 31 offline Vitest unit tests.

---

## Technical Stack

| Area | Technologies & Tools |
| :--- | :--- |
| **Languages** | Java (17, 25), TypeScript (Strict), Python 3, JavaScript, HTML5, CSS3 |
| **Static Analysis & Refactoring** | OpenRewrite, Checkstyle, SpotBugs, PMD, CPD, SonarQube |
| **Frameworks, Build & Testing** | Apache Maven, JUnit 5, WireMock, Vitest, Zod, Quarkus, JTE (Java Template Engine) |
| **CI/CD & Infrastructure** | Jenkins (`ci.jenkins.io`, JCasC, Plugin Manager, Git Client), Git, GitHub Actions, Docker, Kubernetes configs |
| **Core Engineering Focus** | CLI Developer Tooling, AST & Reflection Introspection, Streaming Log Parsers, Deterministic Guardrails |

---

## Contact

- **GitHub**: [@Laggy-Ryon](https://github.com/Laggy-Ryon)
- **Jenkins Discourse**: [@laggy-ryon](https://community.jenkins.io/u/laggy-ryon)

<div align="center">

# Harshit Neog

**Computer science student (AI/ML) and open-source contributor**
Java developer tooling, build quality, and CI infrastructure

<br>

[![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)](https://github.com/jenkinsci)
[![Checkstyle](https://img.shields.io/badge/Checkstyle-2C6E49?style=for-the-badge)](https://github.com/checkstyle/checkstyle)
[![Apicurio](https://img.shields.io/badge/Apicurio-1F4E79?style=for-the-badge)](https://github.com/Apicurio/apicurio-registry)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/harshit-neog-b37018418)

</div>

---

## At a glance

| Merged pull requests | Projects | Currently |
|:--------------------:|:--------:|:---------:|
| **6** | **Jenkins, Checkstyle, Apicurio** | **Review rounds on 4 open PRs** |

I contribute small, well-tested fixes to developer tools, and I like work where a clearer error message or a stricter check saves someone an hour of debugging. Each change comes with unit tests, and I run the project's own static analysis before asking for a review.

---

## Merged contributions

| Project | Change | PR |
|---------|--------|----|
| Jenkins Plugin Installation Manager Tool | Fail with a clear error and a non-zero exit code when a specified WAR file does not exist (issue #641) | [#970](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/970) |
| Jenkins Plugin Installation Manager Tool | Fail fast with a clear message when a plugin is not found, instead of redundant retries and long stack traces (issue #562) | [#972](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/972) |
| Jenkins Plugin Installation Manager Tool | Error message now identifies the parent plugin that declared a missing dependency (issue #865) | [#979](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/979) |
| Jenkins Plugin Installation Manager Tool | New `--short-list` option (issue #470) | [#984](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/984) |
| Checkstyle | Removed obsolete suppressions (issue #19803) | [#22393](https://github.com/checkstyle/checkstyle/pull/22393) |
| Apicurio Registry | Fixed malformed console log timestamps (issue #10757) | [#10905](https://github.com/Apicurio/apicurio-registry/pull/10905) |

## In progress

| Project | Change | Status | PR |
|---------|--------|--------|----|
| Jenkins Configuration as Code | JCasC no longer picks up static methods (JENKINS-75170) | Approved, merging once the release freeze ends | [#2929](https://github.com/jenkinsci/configuration-as-code-plugin/pull/2929) |
| Jenkins Git Client Plugin | Export `no_proxy` / `NO_PROXY` alongside proxy settings, with unit tests (issue #1613) | Submitted | [#1801](https://github.com/jenkinsci/git-client-plugin/pull/1801) |
| Jenkins Plugin Modernizer | `ModernizeCollections` recipe for Java 17 features (issue #1169) | Awaiting code owner review | [#2031](https://github.com/jenkins-infra/plugin-modernizer-tool/pull/2031) |
| Apicurio Registry | Validate rule configuration when a rule is created or updated (issue #10722) | In review | [#10993](https://github.com/Apicurio/apicurio-registry/pull/10993) |

---

## Projects

**[triage3am](https://github.com/Laggy-Ryon/triage3am)**
A dependency-free incident triage tool written in Python. It clusters similar log lines into templates, reports the earliest likely trigger, and reconstructs the order in which services failed. See the README for design trade-offs and limitations.

---

## Toolbox

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white)
![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

Static analysis and quality tools I use on every PR: Checkstyle, SpotBugs, Spotless.

---

## How I work

- Reproduce the problem before changing any code.
- Keep the diff small and add tests with it.
- Run the project's checks locally first.
- Answer review feedback quickly, and change direction when the maintainer has a better idea.

<div align="center">

Find me on [LinkedIn](https://www.linkedin.com/in/harshit-neog-b37018418) or in the [Jenkins community forum](https://community.jenkins.io/u/laggy-ryon).

</div>

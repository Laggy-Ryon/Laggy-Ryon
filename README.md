# Harshit Neog

First-year Computer Science Engineering (AI/ML) student. I am working on
open-source developer tooling, currently contributing to Jenkins.

## Current open-source work

**Jenkins** 
- [PR #970](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/970) **[Merged]**:
  plugin-installation-manager-tool now validates and returns a clear error when a
  user-specified WAR file does not exist (fixes issue #641). Merged into upstream
  `master` with regression unit tests and CLI documentation.
- [PR #972](https://github.com/jenkinsci/plugin-installation-manager-tool/pull/972) **[Merged]**:
  plugin-installation-manager-tool now fails fast on HTTP 404 responses without
  redundant retries across mirrors, demotes expected download error logs from stderr,
  and reports concise, readable single-line errors when a plugin is missing (fixes issue #562).
  Merged into upstream `master` with WireMock tests, unit tests, and integration test coverage.
- Next: investigating transitive dependency resolution when `--latest=false` (issue #865) and exploring core Jenkins developer tooling.
- Introduction on the Jenkins community forum:
  [Harshit Neog](https://community.jenkins.io/t/harshit-neog-introducing-myself-to-the-jenkins-ecosystem-for-gsoc-2027/37456)

**Hyperview** (server-driven mobile UI framework for React Native)
- [PR #1392](https://github.com/Instawork/hyperview/pull/1392) [In Review]: supports the
  kebab-case `number-of-lines` attribute on `<text>` for consistency with the
  rest of HXML, keeping the legacy `numberOfLines` attribute working. Covers
  the runtime parser, XML schema, tests, and docs (issue #297).
  
## Own projects
- [triage3am](https://github.com/Laggy-Ryon/triage3am): incident triage engine
  that turns raw production logs into a root-cause diagnosis and suggested
  fix commands.

## Stack
Java, Maven, TypeScript, React Native, Python

## Contact
GitHub: @Laggy-Ryon

# 7-Day Activity Summary

**Period**: March 31 - April 7, 2026

## Executive Summary

High activity across all projects with **90+ merged PRs** and **15+ new issues** in the last 7 days. Key highlights:
- **Strimzi Kafka Operator**: Major work on v1 API preparation, Bridge integration, and rack awareness
- **Kroxylicious**: Release 0.20.0, extensive Error Prone integration, and dependency updates
- **StreamsHub Console**: Heavy dependency management and testing improvements
- **Developer Quickstart**: Smoke test refactoring and documentation additions

---

## Strimzi Projects

### Strimzi Kafka Operator

**Pull Requests**: 13 PRs (6 merged, 7 open)

**Merged PRs:**
- [#12595](https://github.com/strimzi/strimzi-kafka-operator/pull/12595) - Prepare Helm Chart README for v1 API
- [#12591](https://github.com/strimzi/strimzi-kafka-operator/pull/12591) - Added HTTP bridge pipeline to system tests
- [#12590](https://github.com/strimzi/strimzi-kafka-operator/pull/12590) - Add ExternalLink annotation for Gateway API
- [#12586](https://github.com/strimzi/strimzi-kafka-operator/pull/12586) - Remove Access Operator content for 1.0.0 release
- [#12581](https://github.com/strimzi/strimzi-kafka-operator/pull/12581) - Update SSA feature gate GA timeline
- [#12579](https://github.com/strimzi/strimzi-kafka-operator/pull/12579) - Replace VertxUtil with Future.fromCompletionStage
- [#12553](https://github.com/strimzi/strimzi-kafka-operator/pull/12553) - Add advertisedPortTemplate field support
- [#12443](https://github.com/strimzi/strimzi-kafka-operator/pull/12443) - Support HTTP bridge release 1.0.0

**Open PRs:**
- [#12599](https://github.com/strimzi/strimzi-kafka-operator/pull/12599) - Move TLS support for Bridge to correct CHANGELOG section
- [#12598](https://github.com/strimzi/strimzi-kafka-operator/pull/12598) - Add Bridge internal configuration support
- [#12593](https://github.com/strimzi/strimzi-kafka-operator/pull/12593) - Environment variable based rack awareness

**New Issues**: 14 issues created (5 open, 9 closed)

**Notable Open Issues:**
- [#12597](https://github.com/strimzi/strimzi-kafka-operator/issues/12597) - Bug: log4j2.properties pattern issue with JsonTemplateLayout
- [#12596](https://github.com/strimzi/strimzi-kafka-operator/issues/12596) - Don't configure rack-awareness affinity in controller nodes
- [#12594](https://github.com/strimzi/strimzi-kafka-operator/issues/12594) - Should Cruise Control be reconciled before Entity Operator?
- [#12588](https://github.com/strimzi/strimzi-kafka-operator/issues/12588) - Migrate monitoring dashboards to Perses
- [#12587](https://github.com/strimzi/strimzi-kafka-operator/issues/12587) - KafkaRoller v2 metrics

**Key Themes:**
- Preparation for v1 API release
- HTTP Bridge 1.0.0 integration
- Rack awareness improvements
- Monitoring and observability enhancements

---

### Strimzi Kafka Bridge

**Pull Requests**: 1 PR (merged)

**Merged PRs:**
- [#1106](https://github.com/strimzi/strimzi-kafka-bridge/pull/1106) - Bumped version to 1.1.0-SNAPSHOT

**Activity**: Post-release version bump following 1.0.0 release

---

### Strimzi Proposals

**New Issues**: None in the last 7 days

---

### Strimzi Drain Cleaner

**Issues**: No open issues
**Activity**: No activity in the last 7 days

---

## Kroxylicious

**Pull Requests**: 38 PRs (23 merged, 15 open)

**Release Activity:**
- [#3581](https://github.com/kroxylicious/kroxylicious/pull/3581) - **Release 0.20.0** (merged Mar 31)

**Merged PRs - Highlights:**
- [#3615](https://github.com/kroxylicious/kroxylicious/pull/3615) - Fix Error Prone MutablePublicArray warnings
- [#3613](https://github.com/kroxylicious/kroxylicious/pull/3613) - Improve LocalRef hierarchy javadocs
- [#3611](https://github.com/kroxylicious/kroxylicious/pull/3611) - Fix Error Prone missing @Override
- [#3608](https://github.com/kroxylicious/kroxylicious/pull/3608) - Fix license checker warning
- [#3603](https://github.com/kroxylicious/kroxylicious/pull/3603) - Integrate Google Error Prone static analysis
- [#3602](https://github.com/kroxylicious/kroxylicious/pull/3602) - Fix operator re-fetch resources before status patching
- [#3599](https://github.com/kroxylicious/kroxylicious/pull/3599) - Reduce cognitive complexity in AclAuthorizer
- [#3598](https://github.com/kroxylicious/kroxylicious/pull/3598) - Bump docker-java to fix NoClassDefFoundError with Podman
- [#3592](https://github.com/kroxylicious/kroxylicious/pull/3592) - Update Confluent logo in ADOPTERS.md
- [#3589](https://github.com/kroxylicious/kroxylicious/pull/3589) - Update dependabot to scan re-used actions
- [#3587](https://github.com/kroxylicious/kroxylicious/pull/3587) - Editorial review: typo and consistency fixes
- [#3586](https://github.com/kroxylicious/kroxylicious/pull/3586) - Remove vertx deps from record-validation
- [#3583](https://github.com/kroxylicious/kroxylicious/pull/3583) - Fix CI: use PR number in MicroShift workflow
- [#3579](https://github.com/kroxylicious/kroxylicious/pull/3579) - Configure mockito as javaagent to suppress warnings
- [#3578](https://github.com/kroxylicious/kroxylicious/pull/3578) - Fix microshift workflow to run on pushes to main
- [#3575](https://github.com/kroxylicious/kroxylicious/pull/3575) - Run SpotBugs only in lint job
- [#3574](https://github.com/kroxylicious/kroxylicious/pull/3574) - Ascii doc license headers

**Dependency Updates (merged):**
- [#3601](https://github.com/kroxylicious/kroxylicious/pull/3601) - UBI9 OpenJDK 21 to v1.24
- [#3595](https://github.com/kroxylicious/kroxylicious/pull/3595) - Maven core 3.9.13 → 3.9.14
- [#3594](https://github.com/kroxylicious/kroxylicious/pull/3594) - minikube action 2.14.0 → 2.16.1
- [#3593](https://github.com/kroxylicious/kroxylicious/pull/3593) - actions/cache 5.0.3 → 5.0.4
- [#3565](https://github.com/kroxylicious/kroxylicious/pull/3565) - kubernetes-client 7.5.2 → 7.6.1
- [#3564](https://github.com/kroxylicious/kroxylicious/pull/3564) - apicurio-registry 3.1.6 → 3.2.1

**Open PRs - Highlights:**
- [#3624](https://github.com/kroxylicious/kroxylicious/pull/3624) - Set userAgent on Kubernetes client
- [#3623](https://github.com/kroxylicious/kroxylicious/pull/3623) - Delete deprecated clientSaslAuthenticationSuccess
- [#3622](https://github.com/kroxylicious/kroxylicious/pull/3622) - Fix Sonar warnings: single method call in assertThatThrownBy
- [#3621](https://github.com/kroxylicious/kroxylicious/pull/3621) - Add instructions for installing automatic signoff git hook
- [#3612](https://github.com/kroxylicious/kroxylicious/pull/3612) - Envoy setup with haproxy protocol
- [#3607](https://github.com/kroxylicious/kroxylicious/pull/3607) - Fix SimpleMetric to parse scientific notation
- [#3606](https://github.com/kroxylicious/kroxylicious/pull/3606) - README improvements
- [#3588](https://github.com/kroxylicious/kroxylicious/pull/3588) - Structured logging with optional JSON output

**Key Themes:**
- **Code quality**: Error Prone integration, Sonar fixes, code cleanup
- **CI/CD improvements**: Workflow fixes, test improvements
- **Dependency management**: Regular updates across the board
- **Documentation**: README improvements, javadoc enhancements
- **Operator improvements**: Kubernetes client enhancements

---

## StreamsHub

### Console

**Pull Requests**: 21 PRs (13 merged, 8 open)

**Merged PRs - Highlights:**
- [#2456](https://github.com/streamshub/console/pull/2456) - Fix: update system test commit status in generate-matrix job
- [#2454](https://github.com/streamshub/console/pull/2454) - Bump @types/node 25.5.0 → 25.5.2
- [#2453](https://github.com/streamshub/console/pull/2453) - Set ST commit status at job start, include job URLs
- [#2452](https://github.com/streamshub/console/pull/2452) - Bump @swc/helpers 0.5.20 → 0.5.21
- [#2451](https://github.com/streamshub/console/pull/2451) - Bump lodash 4.17.23 → 4.18.1
- [#2450](https://github.com/streamshub/console/pull/2450) - Bump next-intl 4.8.4 → 4.9.0
- [#2449](https://github.com/streamshub/console/pull/2449) - Bump log4j-bom 2.25.3 → 2.25.4
- [#2448](https://github.com/streamshub/console/pull/2448) - Bump git-commit-id-maven-plugin 9.0.2 → 9.1.0
- [#2445](https://github.com/streamshub/console/pull/2445) - Bump opm v1.64.0 → v1.65.0
- [#2444](https://github.com/streamshub/console/pull/2444) - Bump apicurio-registry 3.1.7 → 3.2.1
- [#2443](https://github.com/streamshub/console/pull/2443) - Bump spotbugs-maven-plugin 4.9.8.2 → 4.9.8.3
- [#2442](https://github.com/streamshub/console/pull/2442) - Bump kroxylicious-kubernetes-api 0.19.0 → 0.20.0
- [#2440](https://github.com/streamshub/console/pull/2440) - Bump next-intl 4.8.3 → 4.8.4
- [#2439](https://github.com/streamshub/console/pull/2439) - Bump playwright group with 2 updates
- [#2433](https://github.com/streamshub/console/pull/2433) - Bump protobuf-bom 4.34.0 → 4.34.1

**Open PRs:**
- [#2455](https://github.com/streamshub/console/pull/2455) - Bump eslint 8.57.1 → 10.2.0
- [#2447](https://github.com/streamshub/console/pull/2447) - Bump checkstyle 13.3.0 → 13.4.0
- [#2446](https://github.com/streamshub/console/pull/2446) - Bump quarkus 3.27.2 → 3.33.1
- [#2441](https://github.com/streamshub/console/pull/2441) - Bump apicurio-registry 3.1.7 → 3.2.1

**Key Themes:**
- **Heavy dependency management**: 15+ dependency updates
- **GitHub Actions improvements**: Better system test status tracking
- **Kroxylicious integration**: Updated to 0.20.0
- **Security updates**: Log4j, lodash updates

---

### Developer Quickstart

**Pull Requests**: 3 PRs (1 merged, 2 open)

**Merged PRs:**
- [#9](https://github.com/streamshub/developer-quickstart/pull/9) - Refactor smoke tests with dynamic matrix and Java (jbang) scripts

**Open PRs:**
- [#11](https://github.com/streamshub/developer-quickstart/pull/11) - Only run smoke tests when changing config files
- [#10](https://github.com/streamshub/developer-quickstart/pull/10) - Add project documentation

**Key Themes:**
- Testing improvements
- Documentation additions
- CI optimization

---

## Analysis

### Most Active Projects
1. **Kroxylicious** (38 PRs) - Major release and quality improvements
2. **StreamsHub Console** (21 PRs) - Dependency updates and testing
3. **Strimzi Kafka Operator** (13 PRs) - v1 API preparation and Bridge integration

### Key Focus Areas Across Projects
- **Dependency Management**: All projects actively updating dependencies
- **Code Quality**: Error Prone, Sonar, SpotBugs integration
- **Testing Infrastructure**: Improvements to CI/CD and test frameworks
- **Documentation**: README and javadoc improvements
- **Release Preparation**: Strimzi v1 API, Bridge 1.0.0, Kroxylicious 0.20.0

### Notable Contributors
- **Kroxylicious**: tombentley, SamBarker, k-wall, m1a2st
- **Strimzi**: scholzj, ppatierno, im-konge
- **StreamsHub**: MikeEdgar, tomncooper, dependabot

### Beginner-Friendly Activity
- Several documentation PRs suitable for newcomers
- License header fixes and typo corrections
- Small refactoring improvements

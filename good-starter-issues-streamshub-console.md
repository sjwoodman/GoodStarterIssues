# Good Starter Issues for StreamsHub Console

Analysis date: 2026-04-07

## Project Overview

StreamsHub Console is a web console to interact with Apache Kafka instances running in a Kubernetes cluster managed by Strimzi Cluster Operator. It's a full-stack project with Java backend and TypeScript/Next.js/React frontend.

## Top Recommendations (Best for Beginners)

### 1. [#1507](https://github.com/streamshub/console/issues/1507) - Add Playwright tests for error messages on Consumer Group Reset Offset page
- **Type**: Testing enhancement (Task)
- **Author**: hemahg
- **Why it's good**: 
  - Clear, well-scoped testing task
  - Create end-to-end tests for error message validation
  - Learn Playwright testing framework
  - No core logic changes, only test additions
  - Good introduction to the console UI and testing patterns
  - Specific page/feature to focus on

### 2. [#1428](https://github.com/streamshub/console/issues/1428) - Improve message for missing metrics due to no topic activity
- **Type**: UX improvement
- **Author**: MikeEdgar
- **Why it's good**:
  - User-facing messaging improvement
  - Clear problem: better feedback when metrics unavailable
  - Learn about metrics collection and UI messaging
  - Low risk - affects user feedback only
  - Good for understanding the metrics feature

### 3. [#1471](https://github.com/streamshub/console/issues/1471) - Allow users to leave hostname empty and let OpenShift cluster set it
- **Type**: Feature (UX enhancement)
- **Author**: Frawless
- **Why it's good**:
  - OpenShift Route auto-generation feature
  - Clear use case: hostname should be optional
  - Learn about OpenShift Routes and UX patterns
  - Improves user experience by reducing required configuration

### 4. [#1873](https://github.com/streamshub/console/issues/1873) - Make parts of the UI configurable (Welcome banner, help links)
- **Type**: Enhancement
- **Author**: sebastiangaiser
- **Why it's good**:
  - UI configuration feature
  - Allow hiding/customizing welcome banners and help links
  - Could be user preferences or global config
  - Learn about configuration management and UI state
  - Multiple implementation approaches possible

## Good Secondary Options

### 5. [#1209](https://github.com/streamshub/console/issues/1209) - Add unique name validation to arrays in Console CRD types
- **Type**: Enhancement
- **Author**: MikeEdgar
- **Why it's good**:
  - CRD validation improvement
  - Implement uniqueness validation for array entries
  - Learn about Kubernetes CRD validation
  - Uses fabric8 annotations or Kubernetes extensions
- **Caution**: Requires understanding of CRDs and validation patterns

### 6. [#1836](https://github.com/streamshub/console/issues/1836) - Add support for local users
- **Type**: Feature
- **Author**: istrate
- **Why it's good**:
  - Authentication/authorization feature
  - Support users stored in Kubernetes Secret/ConfigMap
  - Learn about authentication patterns
- **Caution**: Requires understanding of authentication systems

## Issues to Avoid for Beginners

These require deep expertise or are complex migrations:

### Major Migrations/Upgrades:
- **#2323** - Next.js 15 / React 19 migration (Milestone 0.12.1, 12 comments, complex)
- **#1183** - Upgrade to Next.js 16 (Future upgrade, dependency-blocked)
- **#2426** - TypeScript 6.0 upgrade (Major version, marked "do not merge")

### Infrastructure/Automation:
- **#1526** - OperatorHub submission automation (Assigned to MikeEdgar, requires OLM expertise)
- **#2418** - [WIP] Operator Route addition (Work in progress, assigned)

### Dependency Updates:
- **#2455**, **#2447**, **#2441** - Dependabot PRs (better handled by maintainers)

## Project-Specific Considerations

### Technology Stack
- **Backend**: Java (Kubernetes operator, REST API)
- **Frontend**: TypeScript, Next.js 15, React 19, PatternFly
- **Testing**: Playwright (E2E), Jest (unit tests)
- **Infrastructure**: Kubernetes, OpenShift, Strimzi

### Skills Needed for Different Issues

**Frontend/UI focused:**
- #1873 - UI configuration
- #1428 - Messaging improvements
- #1507 - Playwright tests

**Kubernetes/CRD focused:**
- #1209 - CRD validation
- #1471 - OpenShift Routes
- #1836 - Local users (Secrets/ConfigMaps)

## Recommendation Summary

**Start with (Easiest)**:
1. **Testing**: #1507 - Add Playwright tests for error messages
   - Most isolated, clear scope, learn testing
2. **UX/Messaging**: #1428 - Improve metrics messaging
   - User-facing improvement, low risk
3. **Configuration**: #1471 - Optional hostname field
   - Clear feature, UX improvement

**Next steps** (More complexity):
- **UI Features**: #1873 - Configurable UI elements
- **Validation**: #1209 - CRD array uniqueness
- **Authentication**: #1836 - Local user support

## Notes for Mentors

When assigning these issues:
1. Only ~15 real issues in the repository (rest are PRs/dependabot)
2. Active migration to Next.js 15 / React 19 ongoing (#2323)
3. No explicit "good first issue" or "help wanted" labels used
4. Issues are well-described but may need clarification
5. Smaller issue backlog means higher visibility for contributions
6. Project is actively maintained by MikeEdgar and team

### Setup Requirements
- Java development environment
- Node.js/npm for frontend
- Access to Kubernetes cluster (Minikube, Kind, or remote)
- Strimzi Cluster Operator understanding helpful

### Getting Started
1. Review project README and documentation
2. Set up local development environment
3. Run existing tests to understand patterns
4. Comment on chosen issue to indicate interest
5. Ask questions about implementation approach

## Additional Context

### Related Projects (Same Organization)
- **console-datagen** (3 issues) - Data generation for Kafka
- **kmetadb** (2 issues) - Kafka metadata database
- **flink-sql** (8 issues) - Flink SQL integration
- **developer-quickstart** (5 issues) - Development setup

Consider exploring these related projects for additional contribution opportunities.

## Issue Count Summary

- **Total open issues**: ~15 (excluding PRs/Dependabot)
- **Identified as good starters**: 4-6 issues
- **Testing opportunities**: 1 (#1507)
- **UX improvements**: 2 (#1428, #1471)
- **Feature additions**: 2 (#1873, #1836)
- **Infrastructure/validation**: 1 (#1209)

## Contributing Tips

1. **Test-first**: Start with #1507 to learn the codebase through testing
2. **UX polish**: #1428 and #1471 are good for quick wins
3. **Feature work**: #1873 and #1836 require more design discussion
4. **Check milestones**: Some issues tied to specific releases
5. **Active development**: Project is evolving rapidly with React 19/Next.js 15

## Project Maturity

StreamsHub Console is a relatively new project (25 stars) but actively developed. The small issue count suggests either:
- Good issue management and resolution
- Project is still growing its contributor base
- Opportunities to identify and report new issues

This makes it easier for new contributors to:
- Understand the full scope
- Get noticed by maintainers
- Have meaningful impact

## Next Steps for Contributors

1. **Read the docs**: Understand Console architecture and features
2. **Local setup**: Get development environment running
3. **Explore the UI**: Use the console to understand user workflows
4. **Pick an issue**: Start with #1507 (testing) or #1428 (messaging)
5. **Engage**: Comment on issue before starting work
6. **Learn Strimzi**: Console builds on Strimzi - understanding it helps

# Good Starter Issues for Kroxylicious

Analysis date: 2026-04-07

## Top Recommendations (Best for Beginners)

### 1. [#3620](https://github.com/kroxylicious/kroxylicious/issues/3620) - Delete Deprecated clientSaslAuthenticationSuccess from FilterContext
- **Type**: Code cleanup (deprecation removal)
- **Labels**: **good first issue**, **help wanted**, **easy-starter**, triaged, lifecycle/deprecation
- **Milestone**: 0.21.0
- **Assignee**: m1a2st (check if still active)
- **Why it's good**: 
  - Explicitly marked as "good first issue" and "easy-starter"
  - Well-defined task: remove deprecated method and implementations
  - Clear scope: delete specific method, cleanup related code
  - Learn about FilterContext API and deprecation lifecycle
  - Safe removal of already-deprecated code

### 2. [#3619](https://github.com/kroxylicious/kroxylicious/issues/3619) - Only make one method call within each assertThatThrownBy lambda
- **Type**: Test refactoring
- **Labels**: **good first issue**, **help wanted**, **easy-starter**, triaged, kind/refactoring
- **Status**: Has PR #3622 (check if merged)
- **Why it's good**:
  - Marked "good first issue" and "easy-starter"
  - Clear Sonar rule to follow (java:S5778)
  - Specific files identified: `ConnectionExpirationFilterConfigTest`, `NettySettingsTest`
  - Learn testing best practices
  - Low risk - only affects test code

### 3. [#3618](https://github.com/kroxylicious/kroxylicious/issues/3618) - Reduce cognitive complexity of ServiceBasedPluginFactoryRegistry#loadProviders
- **Type**: Code refactoring
- **Labels**: **good first issue**, **help wanted**, **easy-starter**, triaged, kind/refactoring
- **Why it's good**:
  - Marked "good first issue" and "easy-starter"
  - Single method to refactor: `loadProviders`
  - Clear goal: decompose into smaller methods
  - Learn about plugin loading architecture
  - Improves code maintainability

### 4. [#3617](https://github.com/kroxylicious/kroxylicious/issues/3617) - Reduce cognitive complexity of StructSpec constructor
- **Type**: Code refactoring
- **Labels**: **good first issue**, **help wanted**, **easy-starter**, triaged, kind/refactoring
- **Why it's good**:
  - Marked "good first issue" and "easy-starter"
  - Specific constructor in `io.kroxylicious.krpccodegen.schema`
  - Learn code generation patterns
  - Clear Sonar guidance for improvement

### 5. [#3616](https://github.com/kroxylicious/kroxylicious/issues/3616) - Reduce cognitive complexity of FieldSpec constructor
- **Type**: Code refactoring
- **Labels**: **good first issue**, **help wanted**, **easy-starter**, triaged, kind/refactoring
- **Why it's good**:
  - Marked "good first issue" and "easy-starter"
  - Similar to #3617, focused refactoring task
  - Learn about code generation

### 6. [#3600](https://github.com/kroxylicious/kroxylicious/issues/3600) - Add guidance to Dev Guide covering automatic DCO signoff
- **Type**: Documentation
- **Labels**: documentation, dev
- **Status**: Has PR #3621 (check if merged)
- **Why it's good**:
  - Pure documentation task
  - Help new contributors with git setup
  - May reference `scripts/install-hooks.sh`
  - Low risk, high value for onboarding

## Good Secondary Options

### 7. [#2805](https://github.com/kroxylicious/kroxylicious/issues/2805) - Add pattern for sharing state between Filters to Dev guide
- **Type**: Documentation
- **Labels**: documentation, **help wanted**, triaged
- **Why it's good**:
  - Marked "help wanted"
  - Documentation improvement
  - Learn about Filter architecture and patterns
  - Requires understanding FilterFactory initialization

### 8. [#2800](https://github.com/kroxylicious/kroxylicious/issues/2800) - Document how filters access SASL and TLS information
- **Type**: Documentation
- **Labels**: documentation, triaged, filter/api
- **Why it's good**:
  - Documentation of FilterContext capabilities
  - Learn about authentication and security features
  - Helps other developers understand the API

### 9. [#2858](https://github.com/kroxylicious/kroxylicious/issues/2858) - Document how Kroxylicious handles rack awareness
- **Type**: Documentation
- **Labels**: documentation, kind/tech-debt, triaged, prio/highly-desirable
- **Why it's good**:
  - Marked as "highly desirable" priority
  - Multi-AZ deployment documentation
  - Learn about rack awareness concepts

### 10. [#3582](https://github.com/kroxylicious/kroxylicious/issues/3582) - Out of date image reference
- **Type**: Bug fix
- **Labels**: dev/release
- **Why it's good**:
  - Simple fix: update image version in docker-compose
  - Learn about release process
  - Quick win

### 11. [#2873](https://github.com/kroxylicious/kroxylicious/issues/2873) - Improve manual release step adding image shas to documentation
- **Type**: Documentation/Process improvement
- **Labels**: documentation, triaged, dev/release, dev/github_actions
- **Why it's good**:
  - Improve release automation
  - Reduce manual errors
  - Learn about release process

### 12. [#3609](https://github.com/kroxylicious/kroxylicious/issues/3609) - Incrementally fix Error Prone warnings
- **Type**: Meta-issue (code quality)
- **Labels**: **help wanted**, dev/maven
- **Why it's good**:
  - Marked "help wanted"
  - Meta-issue with 21 sub-issues to create and fix
  - Can pick individual warning categories
  - Learn about Error Prone static analysis
  - Multiple contribution opportunities

## Issues Requiring More Experience

### Medium Difficulty:
- **#2813** - Azure KMS: Support Managed Identity (requires Azure knowledge)
- **#2804** - Add lifecycle method to Filter for connection close (API design)
- **#2820** - Extend automatic discovery for TLS listeners (assigned, complex)
- **#3605** - System test timeout issues (debugging, test infrastructure)

### Complex/Architectural:
- **#3585** - Mitigate untrusted code execution risk in CI (security, CI/CD architecture)
- **#2900** - Dynamic reload feature proposal (major feature, complex state management)
- **#2918** - Authorizer metrics (observability, multi-phase project)
- **#2859** - Handle rack awareness in operator (operator development)
- **#3591** - Sidecar pattern support (networking, architecture)

## Recommendation Summary

**Start with (Easiest)**:
1. **Documentation**: #3600, #2800, #2805, #2858 - learn the project
2. **Deprecated code removal**: #3620 - clearly scoped cleanup
3. **Test refactoring**: #3619 - improve test quality

**Next steps** (Code refactoring):
- **Complexity reduction**: #3618, #3617, #3616 - learn refactoring patterns
- **Simple bug fix**: #3582 - update version reference
- **Error Prone warnings**: #3609 - pick a warning category to fix

## Notes for Mentors

When assigning these issues:
1. Many issues are explicitly labeled "good first issue", "easy-starter", "help wanted"
2. Check assignee status and PR status before assigning (some may be in progress)
3. Milestone 0.21.0 for #3620 - coordinate with release timeline
4. Sonar/Error Prone issues teach static analysis and code quality practices
5. Documentation issues are perfect for learning the architecture
6. The project uses DCO signoff - ensure contributors set up git hooks (#3600)
7. #3609 is a great meta-issue for multiple small contributions

## Project Context

Kroxylicious is a proxy for Apache Kafka that provides features like record encryption, authorization, and protocol filtering. It's actively developed with strong focus on code quality (Sonar, Error Prone), comprehensive testing, and clear contribution guidelines. The project uses Java and has 270+ open issues with many labeled for new contributors.

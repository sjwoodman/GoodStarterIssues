# Good Starter Issues for Strimzi Kafka Bridge

Analysis date: 2026-04-07

## Top Recommendations (Best for Beginners)

### 1. [#436](https://github.com/strimzi/strimzi-kafka-bridge/issues/436) - Missing documentation on Docker container execution
- **Type**: Documentation
- **Labels**: None
- **Why it's good**: 
  - Pure documentation task - no code changes required
  - Clear scope: document how to run bridge as standalone Docker container or with docker-compose
  - Perfect first contribution to learn the project
  - Low risk, high value for users

### 2. [#437](https://github.com/strimzi/strimzi-kafka-bridge/issues/437) - Configure default log4j.properties for Docker
- **Type**: Configuration
- **Labels**: None
- **Why it's good**:
  - Straightforward configuration task
  - Provide fallback default log4j configuration for Docker startup
  - Learn about logging configuration and Docker setup
  - Clear success criteria

### 3. [#452](https://github.com/strimzi/strimzi-kafka-bridge/issues/452) - Error running bridge as Docker container
- **Type**: Bug
- **Labels**: None
- **Comments**: 2
- **Why it's good**:
  - Well-defined Docker configuration issue
  - Simple fix: change CMD to ENTRYPOINT in Dockerfile
  - Learn Docker best practices
  - Enables standalone Docker execution

### 4. [#493](https://github.com/strimzi/strimzi-kafka-bridge/issues/493) - Poll should not return empty body when Kafka is down
- **Type**: Bug
- **Labels**: None
- **Why it's good**:
  - Clear bug: should return HTTP 500 instead of empty response
  - Learn about error handling in HTTP APIs
  - Improves user experience with proper error codes
  - Well-scoped API behavior fix

## Good Secondary Options

### 5. [#652](https://github.com/strimzi/strimzi-kafka-bridge/issues/652) - Adding tracing related tests
- **Type**: Enhancement (Testing)
- **Labels**: None
- **Why it's good**:
  - Add tests to validate span creation and tracing information
  - Current tests only verify messages work with tracing enabled
  - Learn about distributed tracing and testing patterns
  - Isolated to test code

### 6. [#1068](https://github.com/strimzi/strimzi-kafka-bridge/issues/1068) - Refactor MetricsIT
- **Type**: Test refactoring
- **Assignee**: im-konge (check if still active)
- **Why it's good**:
  - Test improvement task with clear problems identified
  - Reduce overlapping logic and long run times
  - Learn about metrics testing patterns
- **Caution**: Check with assignee before starting

### 7. [#735](https://github.com/strimzi/strimzi-kafka-bridge/issues/735) - Investigating commitAsync in place of commitSync
- **Type**: Investigation/Enhancement
- **Labels**: None
- **Why it's good**:
  - Research task to explore using native commitAsync API
  - Learn about Kafka consumer commit strategies
  - Can start with investigation, propose solution, then implement
  - Performance improvement opportunity

## Issues to Avoid for Beginners

These require deep domain knowledge and architectural understanding:

- **#820** - Refactoring tests to remove Vert.x (major refactoring, has assignee)
- **#460** - Add support for schema registry (complex feature, 20 upvotes - likely being considered)
- **#305** - OpenID-Connect authentication (complex security feature)
- **#125** - Handling sticky sessions (complex distributed systems problem)
- **#379** - OOM error with large data (already closed, but shows complexity of memory management)

## Recommendation Summary

**Start with**: 
- **Documentation**: #436 (Docker documentation) - easiest first contribution
- **Configuration**: #437 or #452 (Docker setup fixes) - simple, clear fixes

**Next steps**: Once comfortable with the codebase, move to:
- **Bug fix**: #493 (error handling)
- **Testing**: #652 (tracing tests)
- **Investigation**: #735 (commitAsync research)

## Notes for Mentors

When assigning these issues:
1. Documentation (#436) is perfect for first-time contributors
2. Docker issues (#437, #452) teach containerization basics
3. #493 teaches HTTP API error handling patterns
4. #652 and #735 are good for developers comfortable with Java and Kafka
5. Check assignee status on #1068 before assigning
6. Encourage testing fixes locally with Docker before submitting PRs

## Project Context

The Strimzi Kafka Bridge is an HTTP-based bridge for Apache Kafka, providing a RESTful interface to a Kafka cluster. It's actively working to reduce Vert.x dependencies and improve test coverage.

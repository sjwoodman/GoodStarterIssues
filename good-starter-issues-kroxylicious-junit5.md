# Good Starter Issues for Kroxylicious JUnit5 Extension

Analysis date: 2026-04-07

## Top Recommendations (Best for Beginners)

### 1. [#25](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/25) - Configurable Timeouts
- **Type**: Enhancement
- **Labels**: enhancement, **good first issue**
- **Why it's good**: 
  - Explicitly marked "good first issue"
  - Clear problem: hard-coded timeouts need to be configurable
  - Multiple configuration approaches to consider (annotations, env vars, system properties)
  - Learn about test framework design
  - Low risk - affects timeouts only

### 2. [#518](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/518) - Document GitHub automation development setup and token requirement
- **Type**: Documentation
- **Labels**: None
- **Why it's good**:
  - Pure documentation task
  - Help contributors set up development environment
  - Document GitHub token requirements for workflows
  - Learn about CI/CD setup
  - Perfect first contribution

### 3. [#351](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/351) - TopicConfig annotation name clash
- **Type**: Enhancement (API improvement)
- **Labels**: enhancement
- **Why it's good**:
  - Clear problem: annotation clashes with Kafka's TopicConfig class
  - Well-scoped: deprecate and rename annotation
  - Learn about deprecation patterns
  - API design experience

## Good Secondary Options

### 4. [#210](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/210) - Use service loader to find KafkaCluster implementations
- **Type**: Enhancement
- **Labels**: enhancement, **help wanted**, triaged
- **Why it's good**:
  - Marked "help wanted"
  - Adopt Java service loader pattern
  - Learn about modular architecture
  - Reduces dependencies for users
- **Caution**: Requires understanding service loader mechanism

### 5. [#570](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/570) - When topic creation fails, the cause isn't visible
- **Type**: Bug
- **Labels**: bug
- **Why it's good**:
  - Improve error messages for better debugging
  - Learn about error handling and logging
  - Clear user experience improvement

### 6. [#583](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/583) - Cannot override broker config with same value
- **Type**: Bug
- **Labels**: bug
- **Why it's good**:
  - Well-defined bug: framework rejects config override with same value
  - Should be silent acceptance or warning
  - Learn about configuration validation logic

### 7. [#271](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/271) - CloseableAdmin etc are part of the impl module
- **Type**: Code organization
- **Labels**: triaged
- **Why it's good**:
  - Move public classes from impl to API module
  - Learn about module boundaries and API design
  - Refactoring exercise
- **Related**: #234, #10 (similar module organization issues)

### 8. [#507](https://github.com/kroxylicious/kroxylicious-junit5-extension/issues/507) - Give tests access to node details
- **Type**: Enhancement
- **Labels**: enhancement
- **Why it's good**:
  - Add API to expose node details (nodeId, address)
  - Learn about Kafka cluster internals
  - Enables better testing scenarios

## Issues Requiring More Experience

### Medium Difficulty:
- **#367** - Add @Listener annotation (API design, internal details exposure concerns)
- **#331** - Test class fails on second test (state management debugging)
- **#136** - Injection creates different clusters (JUnit extension lifecycle understanding)
- **#11** - Consider refactoring existing annotations (API redesign)

### Complex/Architectural:
- **#176** - Support KRaft separate controllers (API refactoring, terminology changes)
- **#183** - Sporadic multi-controller test failures (flaky test debugging, ~10% failure rate)
- **#174** - Slow shutdown with multi-controller clusters (5-minute delays, timeout handling)
- **#293** - IllegalStateException during replica deletion (Kafka internals, timing issues)
- **#364** - KIP-974 Apache Kafka native images integration (architectural decision)
- **#14** - KafkaCluster subclass constraint (template test design)

## Recommendation Summary

**Start with (Easiest)**:
1. **Documentation**: #518 - GitHub automation setup docs
2. **Configuration**: #25 - Add configurable timeouts (labeled "good first issue")
3. **API improvement**: #351 - Rename TopicConfig annotation

**Next steps**:
- **Error handling**: #570, #583 - Improve error messages and validation
- **Code organization**: #271, #234, #10 - Move classes to proper modules
- **Service loader**: #210 - Learn modular architecture (marked "help wanted")

## Notes for Mentors

When assigning these issues:
1. Only one issue explicitly labeled "good first issue" (#25) - great starting point
2. Documentation (#518) is perfect for first-time contributors
3. Several module organization issues (#271, #234, #10) could be tackled together
4. #210 marked "help wanted" - actively seeking contributors
5. Bug fixes (#570, #583) teach error handling and validation
6. Some issues involve JUnit5 extension lifecycle - may need guidance
7. KRaft-related issues (#176, #183, #174) are more complex - avoid for beginners

## Project Context

The Kroxylicious JUnit5 Extension provides test parameterization over Kafka clusters (ZooKeeper and KRaft modes), making it easier to write portable Kafka tests. It's used by Kroxylicious and available for other projects. The project has 20 open issues with focus on improving test developer experience, supporting KRaft evolution, and maintaining clean API boundaries.

## Additional Notes

- The project is transitioning to KRaft (removing ZooKeeper dependency)
- Several issues around module organization (#271, #234, #10) suggest API/impl separation needs attention
- Sporadic test failures (#183, #293, #331) indicate some stability challenges
- Native image support (#364) is being considered for future

## Related Issues to Track

Issues that should be addressed together:
- Module organization: #271, #234, #10
- Annotation refactoring: #351, #367, #11
- KRaft support: #176, #183, #174

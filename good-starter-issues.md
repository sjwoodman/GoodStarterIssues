# Good Starter Issues for Strimzi Kafka Operator

Analysis date: 2026-04-07

## Top Recommendations (Best for Beginners)

### 1. [#12573](https://github.com/strimzi/strimzi-kafka-operator/issues/12573) - Add helper method for trust chain secrets
- **Type**: Enhancement (System tests)
- **Labels**: enhancement, System tests
- **Why it's good**: 
  - Clear, well-scoped task: create a builder helper to reduce boilerplate
  - Focused on test infrastructure, not core operator logic
  - Good for learning test patterns without deep Kafka knowledge
  - Low risk - changes only affect tests

### 2. [#12512](https://github.com/strimzi/strimzi-kafka-operator/issues/12512) - Detect failure early in negative tests  
- **Type**: Enhancement (System tests)
- **Labels**: enhancement, System tests
- **Why it's good**:
  - Add log pattern detection to fail fast instead of waiting for timeouts
  - Clear problem statement with measurable improvement (seconds vs minutes)
  - Teaches log analysis and test optimization
  - Isolated to test code

### 3. [#5279](https://github.com/strimzi/strimzi-kafka-operator/issues/5279) - Log more information when rolled pod doesn't become ready
- **Labels**: enhancement, cluster operator, needs-proposal, KafkaRoller
- **Assignee**: ShubhamRwt (check if still active)
- **Why it's good**:
  - Straightforward logging enhancement
  - Learn about KafkaRoller without changing core logic
  - Clear value: better debugging information

## Good Secondary Options

### 4. [#12597](https://github.com/strimzi/strimzi-kafka-operator/issues/12597) - Fix log4j2.properties inline logging bug
- **Type**: Bug
- **Labels**: bug, needs-triage
- **Why it's good**:
  - Well-defined bug: wrong property added for JsonTemplateLayout
  - Fix is likely finding where pattern is added and making it conditional
  - Learn configuration generation patterns
- **Details**: Strimzi incorrectly adds `appender.console.layout.pattern` when using JsonTemplateLayout, causing error

### 5. [#6938](https://github.com/strimzi/strimzi-kafka-operator/issues/6938) - Preserve annotations/labels set by external controllers
- **Labels**: enhancement, **help wanted**, needs-proposal
- **Assignee**: im-konge (check if still active)
- **Why it's good**:
  - Marked "help wanted" - actively seeking contributors
  - Common Kubernetes pattern to learn
  - Good for understanding reconciliation logic
- **Details**: Strimzi strips all annotations from ServiceAccounts during reconciliation, removing those added by external controllers like AWS IAM

### 6. [#5869](https://github.com/strimzi/strimzi-kafka-operator/issues/5869) - Add validation to config spec fields
- **Labels**: enhancement, **help wanted**
- **Why it's good**:
  - Marked "help wanted"
  - Learn CRD validation patterns
  - Clear scope: add validation rules for config parameters
  - Improves user experience with better error messages
- **Details**: Topic configuration fields (retention.ms, segment.bytes) lack validation at CRD application time

### 7. [#8087](https://github.com/strimzi/strimzi-kafka-operator/issues/8087) - KafkaConnect build doesn't use custom Maven repository
- **Labels**: enhancement, **help wanted**, kafka connect, needs-proposal
- **Why it's good**:
  - Marked "help wanted"
  - Build system improvement
  - Issue description includes suggested solution (use Maven mirrors)
  - Learn about Maven and build configurations
- **Details**: Custom Maven repositories specified in KafkaConnect build configurations are not used for all dependencies

## Issues to Avoid for Beginners

These require deep domain knowledge and architectural understanding:

- **#12596** - Rack awareness affinity configuration (requires deep Kafka/K8s scheduling knowledge)
- **#12594** - Cruise Control reconciliation order (requires understanding of CC and Entity Operator)
- **#7594** - Refactor resource operators to remove Vert.x dependency (major architectural change)
- **#7391** - Infinite rolling loop for kafka pods (complex configuration management issue)
- **#7121** - KafkaRoller exception handling (requires deep operator knowledge)
- **#12523** - CRD versioning architecture (requires understanding of Fabric8 and API design)
- **#12513** - KafkaAgentClient timeout issues (requires understanding of HTTP clients and threading)

## Recommendation Summary

**Start with**: #12573 or #12512 (test infrastructure improvements) - most isolated and clearly scoped

**Next steps**: Once comfortable with the codebase, move to:
- **Bug fix**: #12597 (logging configuration)
- **Enhancements with "help wanted"**: #6938, #5869, or #8087

## Notes for Mentors

When assigning these issues:
1. Check if assigned developers are still active
2. Review "needs-proposal" label - may need design discussion first
3. Ensure junior engineers comment on the issue before starting work
4. Pair with experienced team members for code review
5. Encourage reading related code before proposing solutions

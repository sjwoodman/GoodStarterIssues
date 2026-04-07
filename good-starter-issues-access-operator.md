# Good Starter Issues for Kafka Access Operator

Analysis date: 2026-04-07

## Top Recommendations (Best for Beginners)

### 1. [#126](https://github.com/strimzi/kafka-access-operator/issues/126) - Support affinity, nodeSelector, and tolerations in Helm chart
- **Type**: Enhancement (Helm chart)
- **Labels**: enhancement
- **Why it's good**: 
  - Straightforward Helm chart enhancement
  - Add standard Kubernetes scheduling controls to the chart
  - Learn Helm templating and Kubernetes deployment patterns
  - Clear scope with industry-standard patterns to follow
  - Low risk - only affects Helm chart deployment options

### 2. [#124](https://github.com/strimzi/kafka-access-operator/issues/124) - Include all CA certs in Secret
- **Type**: Bug/Enhancement
- **Labels**: None
- **Milestone**: 0.3.0
- **Why it's good**:
  - Well-defined problem: bundle all CAs instead of single CA
  - Specific method identified: `getConnectionSecretData`
  - Learn about TLS certificate handling and key replacement scenarios
  - Clear use case for production environments

## Good Secondary Options

### 3. [#108](https://github.com/strimzi/kafka-access-operator/issues/108) - Follow alternativeNames and advertisedHost
- **Type**: Enhancement
- **Labels**: needs-triage
- **Why it's good**:
  - Use configured listener settings instead of cloud provider hostnames
  - Learn about Kafka listener configuration
  - Improves multi-environment deployments
- **Caution**: May need design discussion (needs-triage label)

## Issues to Avoid for Beginners

These require deep architectural knowledge or are already assigned:

- **#121** - Start using Strimzi v1 API (major API migration, complex architectural decision)
- **#112** - Allow deploy to single/multiple namespaces (already has open PR)
- **#106** - Deploy operator with access to set of namespaces (assigned to OwenCorrigan76)
- **#105** - Manage grant to create KafkaAccess (needs proposal, requires Gateway API knowledge)
- **#44** - Access from remote cluster (assigned, complex multi-cluster scenario)

## Recommendation Summary

**Start with**: 
- **#126** (Helm chart enhancement) - most straightforward, follows standard patterns

**Next step**: 
- **#124** (CA cert bundling) - once comfortable with the codebase and certificate handling

## Notes for Mentors

When assigning these issues:
1. **#126** is ideal for developers familiar with Helm but new to this project
2. **#124** requires understanding of TLS/mTLS and certificate chains
3. **#108** may need design discussion before implementation (needs-triage)
4. The project is small (only 8 open issues), so competition for issues may be higher
5. Check milestone 0.3.0 timeline - #124 is targeted for that release
6. Several issues are already assigned or have PRs - verify status before starting

## Project Context

The Kafka Access Operator simplifies access to Kafka clusters by automating the creation of connection secrets for KafkaUser resources. It's preparing for compatibility with Strimzi 1.0.0 and the v1 API. The project is relatively young with a small issue backlog, making it easier to understand the full scope.

## Additional Contribution Opportunities

Given the small number of open issues, also consider:
- Reviewing open PRs and providing feedback
- Improving documentation
- Adding tests for existing functionality
- Helping with the v1 API migration testing once #121 is addressed

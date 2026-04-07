# Good Starter Issues for StreamsHub Developer Quickstart

Analysis date: 2026-04-07

## Top Recommendations (Best for Beginners)

### 1. [#5](https://github.com/streamshub/developer-quickstart/issues/5) - Add overlays for openshift
- **Type**: Enhancement
- **Created**: 2026-03-18
- **Why it's good**:
  - Straightforward task: create Kustomize overlays for OpenShift
  - Similar to existing overlay patterns in the repo
  - Learn about Kustomize and OpenShift deployment configurations
  - Self-contained work that doesn't affect core functionality
  - Good opportunity to understand the project structure

### 2. [#3](https://github.com/streamshub/developer-quickstart/issues/3) - Kroxylicious overlay
- **Type**: Enhancement
- **Created**: 2026-03-18
- **Why it's good**:
  - Create Kustomize overlay for Kroxylicious integration
  - Follows existing overlay patterns
  - Learn about Kroxylicious and how it integrates with the quickstart
  - Well-scoped and independent work

### 3. [#2](https://github.com/streamshub/developer-quickstart/issues/2) - Prometheus Operator, server and metrics gathering overlay
- **Type**: Enhancement
- **Created**: 2026-03-18
- **Assignee**: tomncooper (check if still active)
- **Why it's good**:
  - Create overlay for Prometheus monitoring stack
  - Learn about observability patterns in Kubernetes
  - Follows overlay pattern similar to other issues
  - Note: Already assigned, so check with maintainers before starting

## Recommendation Summary

**Start with**: #5 (OpenShift overlays) - unassigned and straightforward

**Next steps**: #3 (Kroxylicious overlay) if available

## Notes for Mentors

When assigning these issues:
1. All issues involve creating Kustomize overlays - ensure contributor understands Kustomize basics
2. Check if #2 is still being worked on by the assignee
3. Good opportunity to learn the developer-quickstart project structure
4. Consider pairing overlay creation with testing on actual clusters

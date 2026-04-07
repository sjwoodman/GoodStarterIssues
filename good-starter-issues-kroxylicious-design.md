# Good Starter Issues for Kroxylicious Design Repository

Analysis date: 2026-04-07

## Overview

The Kroxylicious Design repository contains design documents, proposals, and discussions. With only 9 open issues, this repository is smaller but offers opportunities for contributors interested in architecture, design, and documentation rather than implementation.

## Open Issues Summary

### Design Proposals (Require Domain Expertise)

#### 1. [#89](https://github.com/kroxylicious/design/issues/89) - Virtual Cluster Lifecycle State Model
- **Type**: Design proposal
- **Author**: SamBarker
- **Why it's complex**:
  - Introduces lifecycle state machine (initializing, serving, draining, failed, stopped)
  - Domain-Driven Design approach
  - Requires understanding of virtual cluster architecture
- **Suitable for**: Contributors with distributed systems and state machine design experience

#### 2. [#88](https://github.com/kroxylicious/design/issues/88) - Frontend Handler Refactor
- **Type**: Architecture proposal
- **Author**: hrishabhg
- **Why it's complex**:
  - Refactors frontend handler architecture
  - Addresses separation of concerns and HAProxy memory leak
  - Simplifies state machine logic
- **Suitable for**: Contributors familiar with proxy internals and network programming

#### 3. [#85](https://github.com/kroxylicious/design/issues/85) - Security Audit Logging
- **Type**: Design proposal
- **Author**: tombentley
- **Why it's complex**:
  - Security audit logging capabilities
  - SIEM integration considerations
- **Suitable for**: Contributors with security and compliance background

#### 4. [#83](https://github.com/kroxylicious/design/issues/83) - Hot Reload Feature
- **Type**: Design proposal
- **Author**: Uzziee
- **Why it's complex**:
  - Enable configuration changes without restart
  - Related to implementation in kroxylicious#2900
  - Complex state management and lifecycle concerns
- **Suitable for**: Contributors experienced with hot-reload patterns

#### 5. [#82](https://github.com/kroxylicious/design/issues/82) - Kroxylicious 1.0
- **Type**: Release proposal
- **Author**: tombentley
- **Why it's relevant**:
  - Proposes 1.0 release and patch release commitments
  - More of a project management/governance discussion
- **Suitable for**: Project maintainers and experienced contributors

#### 6. [#80](https://github.com/kroxylicious/design/issues/80) - Entity Isolation Filter
- **Type**: Design proposal
- **Author**: k-wall
- **Assignee**: k-wall
- **Why it's complex**:
  - Multi-tenancy feature providing user isolation
  - Affects entity types selectively
  - Significant architectural impact
- **Suitable for**: Contributors with multi-tenancy design experience

#### 7. [#70](https://github.com/kroxylicious/design/issues/70) - Routing API
- **Type**: Design proposal (Draft)
- **Author**: tombentley
- **Status**: Draft
- **Why it's complex**:
  - API design for routing capabilities
  - Core architectural component
- **Suitable for**: Contributors with API design experience

### Process/Governance Issues

#### 8. [#63](https://github.com/kroxylicious/design/issues/63) - Operator - targetKafkaServiceRefNaming
- **Type**: Naming discussion
- **Author**: robobario
- **Why it's good for participation**:
  - Naming convention discussion
  - Evaluating alternatives: `proxiedKafkaServiceRef` vs `upstreamKafkaServerRef` vs `targetKafkaServiceRef`
  - Lower barrier to entry - doesn't require deep technical knowledge
- **Suitable for**: Contributors interested in API ergonomics and naming conventions

#### 9. [#62](https://github.com/kroxylicious/design/issues/62) - Harden Merge Requirements
- **Type**: Process improvement
- **Author**: robobario
- **Why it's good for participation**:
  - Code review and merge requirements
  - Repository governance
  - Enforce multiple code owner approvals
- **Suitable for**: Contributors interested in project governance and quality processes

## Recommendations for New Contributors

### Not Traditional "Good First Issues"

Unlike the implementation repositories, the design repo doesn't have traditional beginner-friendly coding tasks. However, there are ways to contribute:

### 1. **Participate in Discussions**
- Comment on naming discussions like #63
- Provide feedback on proposals
- Ask clarifying questions on design documents

### 2. **Review and Improve Design Documents**
- Fix typos, improve clarity
- Add diagrams or examples
- Identify gaps in proposals

### 3. **Best Entry Point: #63 (Naming Discussion)**
- **Why**: Lower technical barrier
- **How**: Review alternatives, provide user perspective
- **Value**: Naming affects developer experience

### 4. **Best Entry Point: #62 (Merge Requirements)**
- **Why**: Process discussion, not technical implementation
- **How**: Share experiences from other projects
- **Value**: Improves project quality processes

## Issues to Avoid for Beginners

All design proposals (#89, #88, #85, #83, #80, #70) require:
- Deep understanding of Kroxylicious architecture
- Distributed systems expertise
- Ability to evaluate architectural trade-offs
- Understanding of Kafka internals

These are better suited for experienced contributors or maintainers.

## Recommendation Summary

**For beginners interested in this repository:**
1. Start by **reading existing design documents** to understand the project
2. **Participate in discussions** on #63 (naming) or #62 (merge requirements)
3. **Review proposals** and ask questions to learn the architecture
4. **Consider implementation repositories** (kroxylicious, junit5-extension) for hands-on coding

**For experienced contributors:**
1. Review and provide feedback on active design proposals
2. Contribute to architectural discussions
3. Help refine proposals before implementation

## Notes

- This repository is for **design and discussion**, not implementation
- Most issues are **proposals** requiring architectural input
- **No issues labeled "good first issue"** or "help wanted"
- Best for contributors who want to **understand architecture** before coding
- Consider this repository **after** contributing to implementation repositories

## Project Context

The design repository serves as a central location for architectural decisions and proposals for Kroxylicious. It follows a design-first approach where significant features are discussed and documented before implementation. This ensures alignment among maintainers and provides historical context for design decisions.

## Contribution Path

Suggested progression for new contributors:
1. **Start**: Contribute code in kroxylicious or junit5-extension repositories
2. **Learn**: Read design documents to understand architectural decisions
3. **Engage**: Participate in discussions on naming/process issues (#63, #62)
4. **Advance**: Review and comment on design proposals
5. **Lead**: Submit your own design proposals for new features

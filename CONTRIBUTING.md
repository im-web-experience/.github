# Contributing
The following is a set of guidelines for contributing to a WE project. These are mostly guidelines, not rules.

### Contents
- [Contributing](#contributing)
    - [Contents](#contents)
- [Changes](#changes)
    - [Audit Evidence](#audit-evidence)
- [Create a Pull Request](#create-a-pull-request)
  - [Definition of Confidence](#definition-of-confidence)
  - [Strategies](#strategies)
    - [Architecture Strategy](#architecture-strategy)
    - [Risk Assessment Strategy](#risk-assessment-strategy)
  - [Architecture](#architecture)
    - [Decision Records](#decision-records)

# Changes
Changes are classified as [production or non-production changes](https://kb.extendhealth.com/x/5AZmEQ).  If changes are expected to be release to production or impact production, they are considered production changes.  

All other changes, should still follow our [quality standards](https://kb.extendhealth.com/x/jcFaCg) but do not need to adhere to our [SDLC Policy](https://kb.extendhealth.com/x/4IMnEQ) nor [Audit Controls](https://kb.extendhealth.com/x/5oMnEQ).

- Major and minor changes are indicated by a version bump using [SemVer](https://semver.org/). Versions are captured in GitHub Releases.
- Any [architectural changes](#architecture) made to this project are documented under `/docs` decisions folder as a decision record, UML diagram, sequence diagram, etc.
- [Definition of Confidence (DoC)](#definiton-of-confidence) is reviewed and related strategies discussed
- If a [production change](https://kb.extendhealth.com/x/5AZmEQ), a [technical attestation](https://kb.extendhealth.com/x/2gZmEQ) is performed by a _technical attestor_

### Audit Evidence
Building on the WE Product Family's [Definition of Confidence](https://kb.extendhealth.com/x/jcFaCg), this project's pull requests act as the _[technical attestation](https://kb.extendhealth.com/x/2gZmEQ)_.

_If the change is expected to be [released or impact production](https://kb.extendhealth.com/x/5AZmEQ):_
1. PR must be approved by atleast one [technical attestor](https://kb.extendhealth.com/x/2gZmEQ) certifing that the changes satsify our [Definition of Confidence (DoC)](https://kb.extendhealth.com/x/jcFaCg)
1. Each commit must reference a JIRA Story
1. At least one automated tests is ran in CI
1. GitHub Release is generated from a successful `master` build in CI

A project repo's administrator is responsible for verifing that any production changes are reviewed by a [technical attestor](https://kb.extendhealth.com/x/2gZmEQ) and approved on a PR.

> See [WE: Audit Evidence KB](https://kb.extendhealth.com/x/kYGBD) for additional details

---
# Create a Pull Request
In most cases, changes are implemented in a [Feature Branch git Workflow](https://kb.extendhealth.com/x/T58QEg) style, generating a [Pull Request](https://kb.extendhealth.com/x/UTWwCg) reviewed by a [technical attestor](https://kb.extendhealth.com/x/2gZmEQ).

_When creating a PR:_
- Indicate if the PR is in WIP
- Add a brief description of the changes
- Indicate if the PR is a production change
  - Add JIRA Issue to title of PR
  - Add a [technical attestor](https://kb.extendhealth.com/x/2gZmEQ) as a _Reviewer_
- Add the owner of the unit of work (usually yourself) as the _Assignee_
- If UI changes, include a screenshot of those changes

> For additional details on what is expected during a PR, see [WE: Pull Request Guidelines](https://kb.extendhealth.com/x/UTWwCg)

## Definition of Confidence
As part of the pull requests, parties involved in a unit of work review the [Definition of Confidence (DoC)](https://kb.extendhealth.com/x/jcFaCg) strategies that pertain to the changes.

## Strategies
### Architecture Strategy
- [ ] [Coding Convention Standards](https://kb.extendhealth.com/x/LYUWD)
  - [ ] [Performance Standards](https://kb.extendhealth.com/x/yJMYCg): additional latency or load time has not been introduced?
  - [ ] [Transient Fault Handling Standards](https://kb.extendhealth.com/x/MISwCw): coded with the anticipation of failure?
  - [ ] [Security Standards](https://kb.extendhealth.com/x/84qvCQ): newly introduced logic meets our security standards?
- [ ] [UI Standards](https://kb.extendhealth.com/x/Uo-7Cg) & [Browser Standards](https://kb.extendhealth.com/x/rwNHD)
  - [ ] [Accessibility Standards](https://kb.extendhealth.com/x/CNoYCg)
  - [ ] [React Standards](https://kb.extendhealth.com/x/_wdtE) & [Styled Component Standards](https://kb.extendhealth.com/x/-gVtE)
- [ ] [Automated Testing Standards](https://kb.extendhealth.com/x/5RuwCg)
  - [ ] [Asp.Net Integration Tests](https://kb.extendhealth.com/x/bQHADQ)
  - [ ] [Jest Standards](https://kb.extendhealth.com/x/1xDtDw)
  - [ ] [Postman Standards](https://kb.extendhealth.com/x/c4IOCw)
  - [ ] [Cypress Standards](https://kb.extendhealth.com/x/mRyUCg)
- [ ] [Infrastructure Standards](https://kb.extendhealth.com/x/IwApCw)
- [ ] [Analytical Standards](https://kb.extendhealth.com/x/KyOwCg)
- [ ] [Documentation Standards](https://kb.extendhealth.com/x/KQApCw): new technical documentation has been added to the appropriate location?

### Risk Assessment Strategy
- [ ] Was a [risk assessment](https://kb.extendhealth.com/x/o5H7Cg) performed and documented on the unit of work?
- [ ] If needed, was a [security threat model assessment](https://kb.extendhealth.com/x/YJeFCg) performed and documented on the unit of work?
- [ ] [Testing Standards](https://kb.extendhealth.com/x/kq5oCQ): are there any manual tests that can and should be converted to automated tests?

---
## Architecture
The architectural strategy follows the patterns and processes from our architecture strategy team. We approach all our stories and items we’re validating by determining what bounded context the work best fits into. From there we either begin the process of creating the new bounded context services or we start the work in the existing bounded context.

- [Taxonomy](https://kb.extendhealth.com/x/dByUCg)
- [Site Composition](https://kb.extendhealth.com/x/DZcYCg)
- [Infrastructure](https://kb.extendhealth.com/x/NZ3XCg)

> See [WE: Architecture Guidelines KB](https://kb.extendhealth.com/x/861oCQ) for additional details around our architecture and its taxonomy

### Decision Records
An [Architectural Decision Record (ADR)](https://kb.extendhealth.com/x/Sg_GCQ) tracks an architecture design choice, patterns to use, infrastructure to provision, standards to adopt.

_Other decision records:_
- **Service-line level**: recorded within the [GitHub Master Architecture Plan](http://github.extendhealth.com/extend-health/master-architecture-plan/tree/master/Implementation%20Decisions)
- **Product family level**: recorded within the [WE: Architecture Decision Records](https://kb.extendhealth.com/x/Sg_GCQ)

> A _UML Diagram_ also acts as an ADR

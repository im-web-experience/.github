# Support
For build support, see the project's `README.md`.  For additional _system arthiceture metadata_, see the projects `sam.yaml` file.  Other technical documentation may be found in the project's GitHub Wiki and/or [Confluence Technical Service directory](https://kb.extendhealth.com/x/AYbyCw).

### Contents
- [Communication](#communication) & [OKRs](#objectives--key-results)
- [SDLC](#software-development-life-cycle) & [Audit Evidence](#audit-evidence)
- [Standards](#standards--guidelines) & [Architecture](#architecture)
- [Decision Records](#decision-records)

## Communication
- **Chat**: [#web-experience](https://wtw-im.slack.com/messages/CAYDVP41X) Slack channel
- **Jira**: [WE Jira Project](https://kb.extendhealth.com/x/EBCGCQ)
- **KB**: [Web Experience Confluence Space](https://kb.extendhealth.com/x/TaVoCQ)
- **Team Ownership Distribution**: https://kb.extendhealth.com/x/5bNaCg
- **Production Support**: [alert responders](https://kb.extendhealth.com/x/iQLHCw) are assigned to each [technical service](https://kb.extendhealth.com/x/5AZmEQ) owned by the product family

> See [WE Communication KB](https://kb.extendhealth.com/x/TBJGCg) for additional details

## Objectives & Key Results
The product family defines yearly product level objectives.  The teams within generate quarterly objectives that cascade up to product level key results.
> See [Objectives & Key Results KB](https://kb.extendhealth.com/x/OK1oCQ) for a list of objectives and key results

# Software Development Life Cycle
Units of work are prioritized against a backlog in our [WE Jira Project](https://jira.extendhealth.com/secure/RapidBoard.jspa?rapidView=665) by [Product Owners](https://kb.extendhealth.com/x/5bNaCg) and owning teams.

In most cases, changes are implemented in a [Feature Branch git Workflow](https://kb.extendhealth.com/x/T58QEg) style, generating a [Pull Request](https://kb.extendhealth.com/x/UTWwCg) that is reviewed by a [technical attestor](https://kb.extendhealth.com/x/2gZmEQ).

[Production changes](https://kb.extendhealth.com/x/5AZmEQ) are merged into the repo's `master` branch, built & tested in CI and cleared in an _integrated environment_ prior to deployment. 

Every [release artifact](https://kb.extendhealth.com/x/nQepEQ) is cleared by a [Technical, QA and Stakeholder attestation](https://kb.extendhealth.com/x/2gZmEQ), certifing that the changes satsify our [Definition of Confidence](https://kb.extendhealth.com/x/jcFaCg) & [proof of testing](https://kb.extendhealth.com/x/fwcnEg).

> See [WE Software Development Life Cycle KB](https://kb.extendhealth.com/x/p4Q9D) for more details

## Audit Evidence
Parts of our [Software Development Lifecycle](https://kb.extendhealth.com/x/p4Q9D) process deviates from our service line's current [SDLC Process](https://kb.extendhealth.com/x/3oMnEQ).

We are responsible in providing such evidence that satisfies our [SDLC Policy](https://kb.extendhealth.com/x/4IMnEQ) & [Audit Controls](https://kb.extendhealth.com/x/5oMnEQ) for those changes we deploy to production.

GitHub [Pull Request](https://kb.extendhealth.com/x/UTWwCg), reviewed by a [technical attestor](https://kb.extendhealth.com/x/i4hAEQ), acts as the [Technical Attestation](https://kb.extendhealth.com/x/2gZmEQ) required by our [SDLC Policy](https://kb.extendhealth.com/x/4IMnEQ).

> See [WE: Audit Evidence KB](https://kb.extendhealth.com/x/kYGBD) for additional details around our the audit evidence we provide

## Standards & Guidelines
Defined product family standards, strategies, guidelines and various solutions for both functional and non-functional practices.

- [Architecture & Coding Standards](https://kb.extendhealth.com/x/LYUWD)
- [Infrastructure Standards](https://kb.extendhealth.com/x/IwApCw)
- [UI Standards](https://kb.extendhealth.com/x/Uo-7Cg)
- [Analytical Standards](https://kb.extendhealth.com/x/KyOwCg)
- [Automated Testing Standards](https://kb.extendhealth.com/x/5RuwCg)

## Bug Management
Using a form of [Zero Bugs Policy](https://kb.extendhealth.com/x/wSyGCQ), bugs are first brought to the attention of the Product Manages who, in turn, assess and evaluate if a bug is legitimate which is then prioritized against the existing backlog.

Bugs are filed in the [WE: Jira Project](https://kb.extendhealth.com/x/EBCGCQ) referncing the technical service using a _JIRA Component_.

> See [WE: Bug Management](https://kb.extendhealth.com/x/wSyGCQ) for details

## Architecture
The architectural strategy follows the patterns and processes from our architecture strategy team. We approach all our stories and items we’re validating by determining what bounded context the work best fits into. From there we either begin the process of creating the new bounded context services or we start the work in the existing bounded context.

- Build steps - `README.md`
- System Architecture Metadata - `sam.yaml`
- [Taxonomy](https://kb.extendhealth.com/x/dByUCg)
- [Site Composition](https://kb.extendhealth.com/x/DZcYCg)
- [Infrastructure](https://kb.extendhealth.com/x/NZ3XCg)

> See [WE: Architecture Guidelines KB](https://kb.extendhealth.com/x/861oCQ) for additional details around our architecture and its taxonomy

### Decision Records
An [Architectural Decision Record (ADR)](https://kb.extendhealth.com/x/Sg_GCQ) tracks an architecture design choice, patterns to use, infrastructure to provision, standards to adopt.

- **Service-line level**: recorded within the [GitHub Master Architecture Plan](http://github.extendhealth.com/extend-health/master-architecture-plan/tree/master/Implementation%20Decisions)
- **Product family level**: recorded within the [WE: Architecture Decision Records](https://kb.extendhealth.com/x/Sg_GCQ)
- **Deployable entity level**: recorded either in the `/docs` decisions folder in it's GitHub repo or in Confluence under its [technical documentation](https://kb.extendhealth.com/x/AYbyCw)

> A _UML Diagram_ also acts as an ADR

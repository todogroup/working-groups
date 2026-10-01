## Instructions for Adding New Meeting Notes

When adding notes for a new meeting:

1. Add the meeting date to the list below using the format:

   ```markdown
   - [YYYY-MM-DD](#summary-month-day)

# Table of Contents:
- [2026-09-29](#summary-september-29)
- [2026-09-15](#summary-september-15)
- [2026-09-01](#summary-september-1)
- [2026-07-21](#summary-july-21)
- [2026-07-07](#summary-july-7)
- [2026-06-30](#summary-june-30)
- [2026-06-09](#summary-june-9)
- [2026-05-26](#summary-may-26)


## Summary September 29

The TODO Group Agentic AI to Empower OSPOs working group welcomed Diego Mastroianni for a show-and-tell on using AI coding tools to build an Open Source Hub. The presentation began with a prototype for mapping open source projects against contribution strategy, then showed a broader internal application connecting projects, people, events, and other OSPO information

The session explored how AI-assisted development can help OSPO practitioners turn a well-understood problem into a working application. Diego reported building the initial MVP in approximately one week, following several months of understanding the information landscape and the requirements

### Show-and-Tell: Open Source Portfolio Strategy Mapper

The presentation started with an [early portfolio strategy mapper prototype](https://oss-portfolio-strategy-mapper-877710891143.us-west1.run.app/). Its purpose was to make contribution strategy visible and give people a concrete starting point for discussion. 

<img width="2052" height="1071" alt="image (4)" src="https://github.com/user-attachments/assets/cb32f899-7c32-4379-9a73-d73372255cb8" />

> ps: Names, affiliations, and other data shared in the prototype screenshots is fake data

The matrix brought together two dimensions:

- the strategic role of a project, using categories such as spearhead, incumbent, enabler, and utility
- the organization's level of participation, ranging from silent use through participation, contribution, leadership, and sole stewardship

Projects could be compared against a desired participation level. This helped illustrate situations where a strategically important project might need stronger involvement, or where an organization carrying most of the work might need to build a broader contributor community.

<img width="2047" height="1072" alt="image (2)" src="https://github.com/user-attachments/assets/0f2767fa-271b-4d47-be67-ac7c28da4a28" />
<img width="2046" height="1044" alt="image (1)" src="https://github.com/user-attachments/assets/bd759253-4ada-4289-8045-1969010492ba" />

The prototype made it easier to discuss whether the current relationship with a project matched its importance and the organization's goals. Diego described choosing an interactive prototype instead of a static slide to communicate the idea and refine it through conversation. The application provided a shared reference that people with different backgrounds could use to discuss priorities and exchange knowledge.

### From a Strategy Matrix to an Open Source Hub

The broader hub extended the matrix into a connected view of OSPO activity. The presentation described a knowledge graph concept linking projects, people, events, patents, and communications.

The underlying problem was fragmentation: relevant information existed across lists, spreadsheets, documents, and other internal resources, with inconsistent freshness and limited visibility into the relationships between them.

The demonstration included:

- a project inventory and strategic participation matrix
- project pages with context, contributor relationships, current participation, and target participation
- a directory of internal open source champions and their project roles
- distinctions between roles such as maintainers, committers, and project management committee members
- an event directory with conference information and opportunities for participation
- analytics showing changes in project roles and the composition of the portfolio

The interface also included areas for patents, documentation, and other resources. These formed part of the broader hub concept; the walkthrough focused primarily on projects, people, events, and analytics.

The project and contributor names shown in the demo were fictitious. The screenshots should therefore be understood as illustrations of the interface and its relationships, rather than evidence about actual project priorities or individual affiliations.

### What Made the One-Week MVP Possible?

Participants asked what another OSPO should do differently if it wanted to build something similar in a week, whether the work used spec-driven development, and how the reasoning behind the application could be shared in prose.

Diego emphasized that the short implementation period depended on clarity about the problem. Before building, he had spent several months discovering where information lived, identifying outdated or disconnected sources, and deciding how the pieces should fit together.

The one-week estimate applied to the initial MVP connecting people, projects, and events. It did not cover all of the preparation or every improvement shown in the demonstration.

The presentation referenced Cursor agents and Composer as development tools. Diego described using a clear mental model of the requirements to build and iterate on the prototype, rather than first producing an extensive written specification. The captured discussion did not establish a formal spec-driven development process.

Moving toward internal deployment required additional work with engineering, including package choices, non-functional requirements, and integration into an existing CI/CD pipeline. The hub was deployed as a module within an existing internal application behind a VPN.

The example illustrated how AI coding assistance can make a previously difficult-to-prioritize internal tool feasible, while still requiring organizational knowledge and engineering support.

### Adoption, Self-Service, and Keeping Information Current

Participants questioned whether the hub was mainly an OSPO tool or something other employees would use directly. One concern was the risk of creating another dashboard that people rarely visit.

Diego explained that the hub was becoming a central reference for project changes, people, events, and related initiatives. Instead of leaving information scattered across messages and documents, the team brought it back into the hub so users could find it later.

Usage analytics were available through the existing application infrastructure. The presenter described an initial spike after introducing the hub, followed by continued use, but did not provide a quantified adoption rate in the captured notes.

The goal was not necessarily daily visits. It was to establish a known place to answer a question when someone needed information about a project, contributor, or upcoming event.

Self-service access and self-service editing were distinct:

- users could browse and find information directly
- updates were made through pull requests
- contributors could propose changes to their own pages or add their participation to an event
- there was no separate wiki-style editing database

Diego acknowledged that he could remain a bottleneck for some updates. He preferred to establish whether people would contribute before building a more elaborate editing system.

### Costs and Ongoing Maintenance

Participants asked about both the cost of creating the MVP and the ongoing cost of data collection or maintenance. The presenter reported no additional token charge for the initial work under the credits available to him. He also acknowledged that this did not reflect the underlying cost of inference. No measured token total or transferable build-cost estimate was supplied during the captured discussion.

For ongoing operation, the distinction was clearer: the core content was Markdown with labels that the application used to render and connect information. Routine content maintenance did not require an LLM call. AI assistance could optionally speed up an edit, and new modules or functionality could involve further AI-assisted development.

The reported token experience should not be interpreted as a zero-cost operating model. A complete estimate for another OSPO would also need to account for hosting, engineering time, data preparation, maintenance, and any future integrations.

### Data Quality, Affiliations, and Useful Signals

The discussion highlighted recurring OSPO questions:

- Which open source projects matter most to the organization?
- Who contributes to them, and in what capacity?
- How are those projects maintained?
- Who should be contacted when security or licensing risks change?
- Which colleagues are speaking at or participating in relevant events?

Participants described the difficulty of extracting useful information from large collections of scans, budgets, and repository data. The challenge was not simply obtaining more data, but identifying information that could support a decision or connect someone with the right person.

Questions were raised about how the hub determines who works on which project, whether affiliations come from internal sources or GitHub, and how well those affiliations hold up with real data. The captured notes do not provide a detailed answer or validation method for those questions.

Event and community-engagement information was identified as a potentially reusable part of the approach, even where organizational strategy and individual relationship data could not be shared.

### Sharing Rebuild Prompts and Reusable OSPO Applications

Participants asked whether the presenter could use his AI tool to generate a prompt describing how to rebuild the application. A related suggestion was to collect prompts for building OSPO applications in a curated TODO resource, linking to existing workflow collections where appropriate.

Diego distinguished between the potentially reusable application structure and the internal information it contained. Names, contribution relationships, and strategic project priorities could require approval before disclosure, even when some underlying facts were already public.

The discussion explored sharing a sanitized prompt, screenshots with fictitious data, or the application's general structure and mechanisms. Participants also requested cost information and implementation guidance to help others understand what would be involved in adapting the approach.

There was interest in collaborating on reusable patterns. The captured notes do not establish that the complete internal hub, a rebuild prompt, or a new shared collection had already been published.

### AI-Assisted Development and Open Source Contributions

The group also discussed whether easier AI-assisted development could undermine open source collaboration. Participants described opportunities to work faster alongside concerns about contribution quality, attribution, and reviews produced without sufficient project context.

The discussion included the need for contribution policies, clear expectations, and moderation practices. AI was also described as a tool that could assist with researching and drafting those policies.

The emphasis was on improving contribution workflows while retaining accountability for the work submitted. Faster generation alone does not establish that a contribution is useful or appropriate for a project.

An [article on forking and AI-assisted development](https://www.linkedin.com/pulse/fork-back-menu-eric-weddington-9wxxe/) was shared as an additional perspective. It was a discussion resource, rather than an agreed working group position.

### Deterministic Tools Beneath Agentic Workflows

A participant suggested exploring whether internal collaboration channels could provide a crowdsourced feed into the hub. Diego noted that live integrations would change the risk profile of an application currently operating in a restricted environment with limited connections to other systems.

He also described a possible future use of agents to discover newly announced events and update the hub. This was an aspiration, not an existing demonstrated capability. Running agents autonomously could introduce additional expense and operational risks whose benefits would need to be assessed.

The closing discussion proposed keeping deterministic tools underneath AI assistance wherever possible:

1. Define a script or tool for each data retrieval or processing task.
2. Combine those operations into a repeatable pipeline, using standard CI where appropriate.
3. Allow an agent to invoke or assist with the pipeline when useful.
4. Preserve the ability to run the underlying process without agent access.

This separates the value of AI-assisted coordination from the mechanics of routine data processing. It also allows the workflow to remain usable when a model or agent is unavailable, provided the necessary environment and source access are still available.

### Mapping to Working Group Workstreams

#### Workstream 1: Use Cases and Maturity Mapping

The session provided examples of:

- rapid prototyping of OSPO applications with AI coding assistance
- portfolio strategy and contribution-level mapping
- connecting projects, people, roles, and events
- internal discovery and self-service access to OSPO information
- using a working prototype to clarify requirements and support strategic conversations

It also illustrated distinct maturity stages: an early public prototype, an internal MVP, subsequent engineering improvements, and possible future agent-driven integrations.

#### Workstream 2: Skills, Prompts, and Workflow Library

Potential reusable resources discussed included:

- sanitized rebuild prompts for OSPO applications
- example data and screenshots that preserve confidentiality
- reusable models for project, contributor, and event relationships
- Markdown-based content structures and pull-request update workflows
- implementation notes covering requirements, preparation, costs, and limitations
- deterministic data-processing tools that agents can invoke

#### Workstream 3: Adoption and Evaluation

The discussion surfaced evaluation questions including:

- How much problem discovery and data preparation precede the build?
- Which capabilities belong to the prototype, and which are ready for ongoing use?
- How are contributor identities and affiliations verified?
- Does the hub answer recurring questions that users actually have?
- Who owns updates, and where do bottlenecks remain?
- What are the build and operating costs beyond available AI credits?
- Which information can be shared, and which requires internal approval?
- Do live integrations or autonomous updates provide enough value to justify their risks?
- Can routine processes run without an agent?

### Final Remarks

The group showed interest in reusing the approach through sanitized prompts and application patterns. The closing discussion reinforced a practical architecture: use AI where it helps build, interpret, or coordinate work, while preserving deterministic processes for repeatable tasks and human ownership of the information

### Action Items

The following follow-ups were discussed or suggested; the captured notes do not record deadlines or a finalized publication commitment:

- [ ] Explore sharing a sanitized rebuild prompt or reusable application structure, with fictitious data and appropriate internal review
- [ ] Capture implementation guidance explaining the preparation behind the one-week MVP and the additional work needed for internal deployment
- [ ] Investigate the token usage and available cost information to help other OSPOs estimate adaptation effort
- [ ] Consider a curated collection of prompts and workflows for building OSPO applications, referencing existing resources where useful
- [ ] Continue exploring reusable project, contributor, and event metadata patterns, including how affiliations are validated
- [ ] Capture the deterministic-tool-plus-agent approach as an adoption and evaluation pattern for future examples


## Summary September 15

The TODO Group Agentic AI to Empower OSPOs working group welcomed the Centers for Medicare & Medicaid Services Open Source Program Office (CMS OSPO) for a session on AI governance, software inventories, and practical AI-assisted metadata generation. The session connected two aspects of OSPO work: helping translate AI policy into operational practices, and reducing the effort required to document and share software. The demonstration combined deterministic retrieval of repository information with a small language model running locally in the browser and a human review step before applying its suggestions.

The presenters explicitly noted that the demonstrated workflow was not necessarily agentic AI. Its relevance was a practical example of using AI for a bounded OSPO task while keeping infrastructure requirements low and users in control of the output.

### CMS OSPO and AI Governance

CMS OSPO described how its existing responsibilities intersect with AI adoption. Software supply chain security, repository health, inventory management, and open source contribution practices all create opportunities for the OSPO to support broader AI governance efforts.

The presentation highlighted concerns including:

- low-quality or extractive AI-generated contributions to open source projects
- AI-enabled attacks against software supply chains and agency systems
- excessive or ineffective use of computing and organizational resources
- disclosure of sensitive information
- the need for clear guidance on responsible use and sharing

The team maintains an [AI section in the CMS OSPO Guide](https://dsacms.github.io/ospo-guide/outbound/ai/) as a central entry point for policies, governance resources, initiatives, and tools. Some linked resources are intended for internal use even though the guide itself is publicly accessible.

The presenters emphasized that the OSPO contributes to a wider organizational effort. CMS' AI Cross-Cutting Initiative leads agency-wide AI strategy and governance work, and the OSPO collaborates with that community on implementation and open source concerns.

### Federal AI Policy and Public Inventories

The governance overview referenced HHS and CMS AI strategies, the [CMS AI Playbook](https://ai.cms.gov/CMS-AI-Playbook.pdf), and two memo:

- [M-25-21: Accelerating Federal Use of AI through Innovation, Governance, and Public Trust](https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-21-Accelerating-Federal-Use-of-AI-through-Innovation-Governance-and-Public-Trust.pdf)
- [M-25-22: Driving Efficient Acquisition of Artificial Intelligence in Government](https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-22-Driving-Efficient-Acquisition-of-Artificial-Intelligence-in-Government.pdf)

The presentation connected these policy resources with implementation questions around software sharing and reuse, AI inventories, compliance planning, accountability, and risk management. CMS OSPO's role was described primarily at the implementation layer, where broad policy requirements need usable guidance and supporting tools.

The [Federal Agency AI Use Case Inventory](https://github.com/ombegov/2025-Federal-Agency-AI-Use-Case-Inventory) was shared as a public resource for exploring how agencies report their AI use cases. The presenters described inventories as useful both for transparency and for discovering work that others may be able to learn from or reuse.

The session also introduced the software-inventory tooling CMS OSPO has been developing to support SHARE IT Act implementation. This provided the context for the `code.json` demonstration.

### Show-and-Tell: AI-Assisted `code.json` Generation

The CMS OSPO team demonstrated a web form that helps project maintainers create a `code.json` metadata file. The aim is to distribute metadata creation across project teams rather than requiring a small central OSPO to manually document every repository.

The workflow combines three sources of information:

| Source | Role in the workflow |
| --- | --- |
| GitHub repository information | Populate fields that can be retrieved deterministically |
| Browser-based language model | Draft additional descriptive fields from repository context |
| Project maintainer | Review suggestions, supply missing information, and decide what to apply and share |

Users begin by entering a GitHub repository URL. The form can retrieve available repository information and prefill some fields. Other fields require interpretation or information that cannot be obtained directly through the API.

To reduce that manual work, the team added an AI-assisted drafting step using WebLLM. The demonstrated implementation used Llama 3.2 with one billion parameters, running in the browser on the user's own GPU. The model is downloaded and cached locally for subsequent use.

This approach allows the form to remain a static website hosted on GitHub Pages without requiring a separate inference server or a hosted model API. Repository retrieval and explicit sharing still involve external services; the model inference itself runs locally.

### Human Review and the Limits of Generated Metadata

The demonstration showed AI-generated suggestions such as a longer project description and categories. Users inspect the suggestions in a review panel before applying selected values to the form.

The presenters acknowledged the limits of a small model. It can help with a narrow drafting task, but its output still needs review and should not be treated as authoritative project information.

Some fields cannot be reliably generated from repository content. Examples included labor hours and contract numbers, which must be supplied directly by someone with the relevant knowledge.

The demonstrated sequence was:

1. Enter the repository URL
2. Retrieve the available repository metadata
3. Run the optional local AI drafting step
4. Review and apply appropriate suggestions
5. Complete the remaining fields manually
6. Generate the `code.json` file
7. Copy, download, or explicitly submit the resulting metadata through an available sharing option

The tool also supports creating a pull request. During Q&A, the presenters clarified that the GitHub token is used for operations such as pull request creation, authenticated API access to private repositories, and API rate-limit handling.

### Lightweight Infrastructure for Resource-Constrained OSPOs

The CMS OSPO team framed the architecture as a response to limited staffing and infrastructure capacity. A static web form with local inference can provide useful assistance without requiring the OSPO to operate a model-serving backend.

The approach also makes the boundary between drafting and sharing visible: the model runs locally, and the user decides when to apply or transmit the resulting information.

The discussion included broader examples of using web forms and GitHub to support structured submissions and maintain portable data. The underlying idea was to build on existing infrastructure where it meets the need, while keeping information available for reuse elsewhere.

### Repository Metadata and Aggregated Software Inventories

A participant asked where the generated metadata belongs and who is responsible for adding it. The presenters explained a distributed approach: project teams generate their own `code.json` files and commit them to their repositories, while inventory tooling collects and aggregates that information.

The team showed the [Code.gov fork maintained by CMS OSPO](https://dsacms.github.io/code-gov/). They described an index-generation process that collects metadata from GitHub and agency sources into a broader software inventory.

This separates two responsibilities:

- project maintainers contribute and maintain information about their own software
- shared tooling aggregates that information to support discovery and reporting

The discussion illustrated how repository-level metadata can support agency-wide and cross-agency inventories without making the OSPO the manual author of every record.

### Interoperability Across Metadata Standards

The session continued the previous meeting's discussion of structured project metadata. CMS OSPO noted that the earlier introduction to CNCF's `.project` metadata work had prompted interest in considering it alongside the team's existing `code.json` practices.

Participants also discussed `publiccode.yml`, CodeMeta, and the possibility of making metadata easier for tools to locate and collect. A [crosswalk from `code.json` to CodeMeta](https://github.com/codemeta/codemeta/blob/master/crosswalks/code-json.csv) was shared as a concrete interoperability resource.

The presenters expressed interest in connecting federal software metadata with the wider public-sector open source ecosystem, including software preservation and digital public goods efforts. These were described as directions for further collaboration, rather than completed integrations.

The discussion favored reusing existing standards and mappings where possible, while avoiding unnecessary abstraction and duplicated work. No common metadata directory or single replacement standard was agreed in the captured notes.

### How Standards Are Selected

A participant asked how a government agency decides which standards to adopt. CMS OSPO described a sequence beginning with applicable law and policy, followed by agency guidance and implementation details.

Within those constraints, the team looks at practices used by other OSPOs and open source projects, publishes reference implementations, and seeks feedback through communities such as this working group. Public comment processes were also highlighted as opportunities for outside contributors to inform policy and standards choices.

The broader message was that mandated requirements and community interoperability need to be considered together. Working implementations can help identify where existing standards fit and where additional mappings or improvements are needed.

### Mapping to Working Group Workstreams

The session offers examples and evaluation questions relevant to the group's three workstreams

#### Workstream 1: Use Cases and Maturity Mapping

- AI-assisted creation of repository metadata
- local inference for a bounded OSPO documentation task
- distributed metadata maintenance across project teams
- aggregation of software inventories for discovery and reporting
- OSPO participation in the implementation of broader AI governance

#### Workstream 2: Skills, Prompts, and Workflow Library

Potential reusable resources include:

- forms that combine deterministic metadata retrieval with AI-assisted drafting
- review interfaces that let users apply only selected suggestions
- static-site patterns for running small models locally
- metadata templates and crosswalks between established schemas
- public OSPO guides that connect policy resources with practical implementation tools

#### Workstream 3: Adoption and Evaluation

The demonstrated design suggests several questions for evaluating similar workflows:

- Which fields can be retrieved deterministically, and which need interpretation?
- Is a small local model adequate for the intended task?
- Can users inspect and correct suggestions before applying them?
- Which information must be provided directly by a maintainer?
- How will repository metadata remain current after initial generation?

### Action Items

The captured notes do not record assigned owners or deadlines. The following are proposed follow-ups based on the presentation and discussion:

- [ ] Review the CMS AI governance resources and identify reusable approaches for connecting OSPO guidance with organization-wide AI initiatives
- [ ] Continue sharing implementation feedback and opportunities for collaboration across OSPOs

## Summary September 1

This was the sixth meeting of the TODO Group Agentic AI to Empower OSPOs working group. The meeting included one joint show-and-tell in which two presenters explored agentic open source security and compliance using two complementary tools:

- an experimental MCP server that exposes precomputed OpenSSF Scorecard results
- a pluggable framework for auditing projects against software-engineering and compliance standards, generating evidence, and supporting remediation

The session explored how deterministic tools, structured project metadata, MCP servers, and AI agents can work together. A recurring theme was that agents should not independently determine whether a project is secure or compliant. Existing tools should produce evidence and structured signals, while agents help people retrieve, interpret, correlate, and act on those signals.

The discussion also surfaced an infrastructure challenge: agentic tools work best when projects and assessment systems expose machine-readable information ahead of time. Participants discussed whether tools such as OpenSSF Scorecard should precompute more information, publish consistent APIs, and generate reusable metadata that both deterministic automation and language models can consume.

### Joint Show-and-Tell: Agentic Open Source Security and Compliance

The show-and-tell began with [Scorecard MCP](https://github.com/uwu-tools/scorecard-mcp), an experimental Model Context Protocol server that exposes OpenSSF Scorecard information as typed, read-only tools and resources.

The server currently reads precomputed results from the public Scorecard REST API. It allows an MCP-compatible agent to:

- retrieve a repository's aggregate Scorecard score and per-check results
- inspect the detailed result of an individual check
- compare results across repositories
- list the checks supported by Scorecard
- explain a check's methodology, associated risk, and possible remediation
- preserve provenance such as the assessed commit, scan date, Scorecard version, and data source

The demonstration used the public Scorecard information for a repository through the [Scorecard viewer](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard-infra) and [Scorecard REST API](https://api.scorecard.dev/projects/github.com/ossf/scorecard-infra).

The group saw how an agent could answer repository-specific questions using existing Scorecard evidence. Examples included asking about:

- branch protection and repository rules
- whether code review protections are enabled
- the presence of a security policy
- individual Scorecard checks and the reasons behind their results
- areas where a project could improve its security posture

The discussion emphasized that Scorecard findings are heuristic signals rather than definitive judgments. The MCP server follows the same model: it gives an agent structured evidence but does not declare that a repository is categorically "secure" or "insecure."

The current MCP implementation reads results already published through the public Scorecard API. This has several practical benefits:

- responses can be retrieved quickly
- the MCP server does not need to run every Scorecard check itself
- results contain information about their origin and assessment date
- the agent can use an existing authoritative source rather than recreating the analysis

However, cached results have limitations:

- only participating public repositories that publish their results are represented
- the public scan does not execute every available Scorecard check
- findings may not reflect the repository's most recent state
- some checks may be inconclusive because of permissions or unavailable information
- private repositories require a different execution model

A future direction for the project is to support live Scorecard execution, including assessments of private repositories where appropriate authorization is available.

### MCP Versus Direct API Calls

The demonstration raised a practical question about the value of placing an MCP server between an agent and an existing API. If Scorecard results are already available through a REST API, could an agent call that API directly instead?

The discussion indicated that both approaches can be appropriate. A direct API call may be simpler when the endpoint, request, and response format are already known and the workflow only needs a narrowly defined result. It avoids adding another service or abstraction layer.

An MCP server can add value when the capability needs to be discovered and used consistently by different agent clients. It can present domain-specific operations as named, typed tools; package documentation and explanations as resources; normalize inputs and outputs; and attach important context such as provenance, freshness, completeness, licensing, and known caveats. This reduces the amount of Scorecard-specific API knowledge that must be embedded in each prompt or agent implementation.

The group also noted the tradeoff: an MCP wrapper creates another component that must be developed, secured, versioned, and maintained. Wrapping an API without adding useful semantics, validation, or interoperability may provide little benefit. The decision should therefore depend on whether MCP offers a meaningful reusable interface rather than being treated as the default integration mechanism.

Questions raised for future evaluation included:

- When is a direct API integration sufficient?
- What domain knowledge or normalization should an MCP server add?
- Does MCP improve discovery and portability across agent clients?
- How are API errors, incomplete results, and stale data represented through the MCP layer?
- Who maintains the MCP interface when the underlying API changes?
- Does the additional abstraction improve governance and auditability enough to justify its operational cost?

### OpenSSF Scorecard as an Agent Input

Participants discussed several ways that Scorecard information could support OSPO workflows:

- inventorying the security posture of repositories
- comparing projects across an organization or portfolio
- identifying repositories that require human attention
- explaining unfamiliar Scorecard checks
- prioritizing findings according to organizational requirements
- providing remediation guidance to project teams
- supporting project onboarding or release-readiness reviews
- tracking changes in project posture over time

The group reinforced that the agent is most valuable as an interpretation and coordination layer. Scorecard should remain responsible for producing the underlying assessment, while the agent makes that information easier to query and contextualize. A possible architecture is:

| Layer | Role |
| --- | --- |
| OpenSSF Scorecard | Run checks and produce evidence |
| MCP servers | Expose the evidence in structured, machine-readable form |
| Agentic analysis | Retrieve, explain, compare, and contextualize findings |
| Human review | Evaluate the evidence and authorize any response |
| Remediation tooling | Prepare or apply approved improvements |

### Pluggable Compliance Auditing and Remediation with Darnit

The show-and-tell then introduced [Darnit](https://github.com/darnitdevorg/darnit), a pluggable compliance-audit framework designed to help software projects conform to engineering best practices.

The framework brings several capabilities together:

- running compliance audits
- supporting multiple standards through plugins
- combining controls into an organization-specific posture
- exposing auditing capabilities through MCP
- identifying gaps and preparing remediation
- generating cryptographically verifiable attestations
- using structured project metadata to locate relevant documentation and evidence

The demonstrated approach covered more than vulnerability scanning. Potential assessment areas include:

- repository access controls
- vulnerability-management practices
- testing and code-review requirements
- CI/CD quality controls
- dependency pinning and build reproducibility
- release processes and artifact signing
- governance and maintainer documentation
- contribution and support guidance
- project documentation

The project includes an implementation of the OpenSSF Baseline and supports a canonical `.project.yaml` file for project metadata.

### From Assessment to Remediation

The Darnit demo expanded the conversation from retrieving findings to acting on them. Participants discussed a flow in which a tool:

1. discovers project metadata and relevant evidence
2. selects the applicable compliance controls
3. runs deterministic assessments
4. reports which controls pass, fail, or need review
5. produces an auditable result or attestation
6. proposes remediation for identified gaps
7. leaves consequential changes subject to human review

This may help OSPOs translate policies and best-practice frameworks into repeatable workflows without relying on an agent to invent the compliance criteria.

The distinction between evidence, interpretation, and remediation remains important:

- deterministic checks should establish observable facts where possible
- agents can explain or correlate those facts
- proposed changes should be traceable to a specific control
- humans should decide whether the proposed remediation is appropriate
- the resulting assessment should preserve enough evidence for later review

### Standardized Project Metadata

A major point of discussion concerned the role of structured project metadata.

The session referenced CNCF's `.project` metadata work, including its public [schema](https://github.com/cncf/automation/tree/main/utilities/dot-project/schema), [example project file](https://github.com/cncf/automation/blob/main/utilities/dot-project/example/project.yaml), and [template](https://github.com/cncf/automation/blob/main/utilities/dot-project/template/project.yaml).

Participants noted that OSPOs and other organizations often maintain similar information in different formats, including `code.json`, spreadsheets, internal databases, repository configuration, and manually maintained documentation.

A standardized project-metadata file could give tools and agents a reliable starting point for discovering:

- project identity and ownership
- repositories and other project resources
- governance documentation
- security and vulnerability-reporting information
- contribution and support documentation
- project lifecycle or maturity information
- locations of relevant compliance evidence
- contacts or responsible teams

The session highlighted the `.project` schema as a potentially valuable discovery for OSPOs already working with other metadata standards.

### Precomputing Machine-Readable Evidence

The discussion raised a broader architectural question: should assessment tools do more work ahead of time to make their results easier for agents and other automation to consume?

Rather than requiring every agent to inspect an entire repository and reconstruct the same facts, deterministic tools could periodically produce:

- structured findings
- machine-readable project metadata
- timestamps and provenance
- normalized control identifiers
- links to supporting evidence
- confidence or completeness indicators
- remediation references
- signed assessment artifacts
- APIs for retrieving current and historical results

This could reduce duplicated computation and improve consistency. It would also allow agents to focus on interpretation and decision support instead of repeatedly rediscovering facts that conventional software can determine more reliably.

The group discussed this as a form of "back pressure" from agentic use cases onto existing open source tooling. As agents become more common, established tools may need to improve their APIs, schemas, provenance, and structured output.

### Deterministic Tools and Language Models

A key takeaway was that deterministic tooling and language models have complementary roles.

Deterministic tools are generally better suited to:

- checking whether a file or configuration exists
- evaluating a repository against a defined control
- recording exactly which evidence produced a result
- generating repeatable structured output
- signing or attesting to an assessment

Language models and agents can add value by:

- translating natural-language questions into tool calls
- selecting relevant evidence from several sources
- explaining findings in language appropriate to the audience
- correlating results across different tools
- identifying ambiguity or missing context
- proposing possible next steps
- helping users navigate large volumes of assessment information

The group cautioned against using an LLM to recreate deterministic checks when an established tool already exists. Connecting agents to maintained upstream tools can improve reliability, explainability, and reuse.

### Trust, Provenance, and Human Judgment

Both tools reinforced that agent-accessible information needs clear provenance.

Useful responses should identify:

- which tool produced the finding
- which version of the tool was used
- when the assessment was performed
- which repository revision was assessed
- whether the assessment was complete
- which evidence supports the finding
- whether the result was cached, live, or inferred
- what the agent added through interpretation

This separation helps prevent an agent-generated explanation from being mistaken for the original evidence.

Participants also emphasized the continuing importance of human judgment. A failed check may be important, intentionally accepted, inapplicable, or the result of incomplete information. OSPOs and project maintainers remain responsible for interpreting findings in the context of the project and organization.

### Implications for OSPOs

The session suggested several potential roles for OSPOs:

- identify authoritative sources for project-health and compliance information
- promote structured project metadata across repository portfolios
- define which standards and controls apply to different project types
- help translate organizational policy into machine-consumable rules
- participate in the governance of MCP servers and agent tools
- ensure that provenance and evidence remain visible
- define when findings require escalation or remediation
- maintain human approval boundaries for consequential changes
- help align internal metadata practices with emerging open source schemas
- contribute reusable integrations and workflows upstream

OSPOs may also serve as connectors between security, legal, compliance, engineering, project maintainers, and AI-governance teams. Agentic workflows can make existing evidence easier to use, but only if these groups agree on authoritative inputs, acceptable controls, and ownership.

### Mapping to Working Group Workstreams

#### Workstream 1: Use Cases and Maturity Mapping

The session provided several agentic-AI use cases relevant to OSPOs:

- conversational access to OpenSSF Scorecard results
- repository security-posture explanation
- portfolio-level comparison and prioritization
- project onboarding and release-readiness assessment
- compliance auditing against a defined standard
- project-metadata discovery
- evidence collection and normalization
- remediation planning
- compliance-attestation generation
- coordination across multiple assessment tools

A possible maturity progression emerged:

1. deterministic tools produce isolated findings
2. findings are published through structured formats or APIs
3. MCP servers make findings accessible to agents
4. agents explain and correlate evidence
5. agents recommend prioritized actions
6. humans authorize remediation
7. tools or agents prepare changes
8. humans review and accept the resulting changes

#### Workstream 2: Skills, Prompts, and Workflow Library

Potential reusable resources identified during the session include:

- an OpenSSF Scorecard MCP integration
- prompts for explaining repository security posture
- prompts for comparing repository findings
- workflows for triaging Scorecard results
- compliance-audit skills
- project onboarding and release-readiness workflows
- remediation-planning skills
- `.project.yaml` templates and validation workflows
- mappings between OSPO requirements and established controls
- patterns for preserving provenance in agent responses
- examples of using several deterministic tools through a shared agent workflow

The working group could provide a curated index pointing to upstream implementations rather than duplicating them.

#### Workstream 3: Adoption and Evaluation

The session surfaced evaluation questions for agent-enabled assessment workflows:

- Does the workflow use authoritative, maintained sources?
- Are results current enough for the intended decision?
- Is the assessed repository revision visible?
- Can the user distinguish cached, live, and inferred information?
- Are incomplete and inconclusive findings represented accurately?
- Does the workflow expose the evidence behind a score?
- Does it reduce the amount of manual investigation required?
- Does it avoid recreating deterministic checks with an LLM?
- Are remediation proposals tied to specific controls?
- Is human authorization required at the appropriate point?
- Can the assessment and resulting actions be audited?
- Can the approach scale across a large repository portfolio?
- Are the metadata and APIs interoperable across tools?
- Does MCP provide meaningful semantics and portability beyond a direct API call?
- Is the additional MCP component justified by its maintenance and operational cost?

### Final Remarks

The meeting demonstrated how MCP can make existing open source security and compliance systems easier for humans and agents to use. The strongest pattern was not an autonomous agent making unsupported judgments, but an agent operating on top of deterministic checks, structured metadata, documented methodologies, and traceable evidence.

OpenSSF Scorecard, compliance frameworks, project-metadata schemas, APIs, and attestations can form an evidence layer. MCP servers and agentic workflows can then provide a conversational and coordinating layer that helps OSPOs interpret that evidence at scale.

The discussion also suggested that agent adoption may influence the design of existing tooling. Projects may increasingly need to publish stable schemas, structured results, provenance, completeness information, and APIs so that agents can consume their outputs without repeating the underlying analysis.

### Action Items

- [ ] Working group coordinator: Add the anonymized September 1 meeting summary to the working group repository
- [ ] Working group chairs: Capture Scorecard MCP and pluggable compliance auditing as show-and-tell examples under the working group's practical use cases
- [ ] Working group members: Evaluate whether the Scorecard MCP integration should be included in the shared skills, prompts, and workflow index
- [ ] Working group members: Review the CNCF `.project` schema and compare it with metadata formats currently used by OSPOs
- [ ] Working group members: Share examples of APIs, schemas, or machine-readable outputs used to expose project-health and compliance evidence
- [ ] Working group chairs and interested participants: Document the boundary between deterministic assessment, agent interpretation, human authorization, and remediation
- [ ] Working group members: Identify additional open source assessment tools that could expose precomputed findings through MCP
- [ ] Working group members: Explore evaluation criteria for freshness, completeness, provenance, and explainability in agent-accessible project assessments




## Summary July 21

This was the fifth meeting of the TODO Group Agentic AI to Empower OSPOs working group. The meeting included a show-and-tell on an agentic Software Composition Analysis (SCA) and compliance workflow built around GitHub Actions, and focused on a practical problem for OSPOs: how to turn the growing volume of open source dependency, licensing, security, project health, and AI-related signals into actionable decisions without requiring humans to manually review every signal

The session framed the problem as one of scale. A relatively small software project can quickly grow from a handful of direct dependencies to more than one hundred transitive dependencies. At the same time, organizations receive information from dependency graphs, advisories, license analysis, project-health tools, AI artifact scanners, and other sources. Existing tools can surface many useful signals, but humans still need to interpret them and decide what action to take

The show-and-tell explored using agents as a layer between those signals and the human reviewer:

- collect information from several existing open source tools and datasets
- summarize and prioritize the relevant findings
- evaluate findings against project-specific policies or criteria
- produce evidence or a compliance artifact
- propose remediation where appropriate
- keep a human responsible for reviewing and accepting resulting changes

A major discussion then emerged around what happens after organizations start building many reusable AI skills and agentic workflows. Participants discussed whether skills should live inside individual repositories, in centralized organizational repositories, or in curated internal "skills marketplaces"; who should own them; and how OSPOs, developer experience, security, legal, and other domain teams can share responsibility for maintaining them

**Slides:** [Agentic AI GitHub Actions](https://ovalenzuela.com/agentic-ai-github-actions/slides.html)

### Show-and-Tell: Agentic SCA and Compliance in GitHub Actions

The presenter described the challenge of managing compliance and open source risk across a growing number of repositories.

Traditional SCA, dependency, security, and project-health tools can provide useful signals, but reviewing those signals becomes difficult when an organization needs to maintain tens or hundreds of projects. Even where some findings can be automatically resolved, many still require interpretation, prioritization, and a decision from a human

The session presented an experimental approach where an agentic workflow runs through GitHub Actions and uses existing tools and datasets rather than attempting to replace them

The general workflow was described in three stages:

1. **Collect signals** from different sources
2. **Summarize and assess those signals** to identify what is relevant to the project
3. **Prepare or propose remediation**, with appropriate human review before resulting changes are accepted

The objective was to reduce the amount of information a human has to inspect while preserving the evidence needed to understand how a recommendation was produced

### Combining Existing Open Source Signals

The workflow demonstrated how different sources can be combined into a single assessment. Examples mentioned during the session included:

- repository dependency graphs
- license and SPDX-related data
- OpenSSF Scorecard
- repository and project-health signals
- security or advisory information
- tools that scan source code for AI artifacts
- additional project-specific rules and policies

The presenter described using structured licensing and compatibility data as context for the agent so that it can reason about whether a dependency is compatible with a particular project's requirements

AI artifact detection was also discussed. Rather than treating AI usage as a binary signal, the workflow can potentially combine information about where an AI-related artifact appears, its license, its dependencies, and the policies relevant to the target application

The broader pattern discussed was that agents become more useful when they receive curated, structured context from existing authoritative tools and datasets instead of being expected to independently infer everything from source code or natural-language prompts

### From Findings to a Compliance Artifact

The demo showed GitHub Actions running the workflow automatically and producing a resulting artifact that can be consumed by another process or reviewed by a human. One example shown was a dependency remediation agent executed as part of a GitHub Actions workflow.

The pipeline included separate stages around detection, activation, agent execution, safe output handling, and conclusion. The agent could use the findings from earlier analysis to prepare a possible remediation.

Participants discussed the value of this architecture because the existing scanners and data sources remain responsible for producing evidence, while the agent provides an interpretation and decision-support layer on top.

This creates a possible pattern for OSPO workflows:

| Layer | Role |

| --- | --- |

| Existing scanners and datasets | Produce evidence and deterministic signals |

| Agentic analysis | Combine, interpret, prioritize, and contextualize those signals |

| Human review | Decide whether the recommendation or remediation should be accepted |

The discussion reinforced that the agent should not necessarily become a replacement for existing compliance tooling. Instead, it can coordinate and reason across outputs that otherwise require substantial manual work.

### Human-in-the-Loop Remediation

A central discussion focused on what should happen when an agent finds a problem.

Participants asked about the reaction from engineering teams when automated tools produce findings. Experience shared during the session was mixed. One pattern discussed was to separate **problem discovery** from **remediation authorization**: Instead of allowing an agent to independently identify, prioritize, and fix every issue, an intermediate triage step could surface the problem to a person. The human could then decide that a specific issue should be addressed, after which an agent could prepare a proposed implementation.

### Verified Intent and Reviewability

The session connected the human-in-the-loop concept to the concept of **Verified Intent Development (VID)**, a methodology for AI-assisted software development based on making the intended change explicit and ensuring that generated code remains understandable and verifiable by humans.

The discussion highlighted principles such as:

- articulate intent before generating code
- scale verification according to the level of risk
- do not accept code that the responsible human cannot understand at an appropriate level
- preserve information about where generated code and other artifacts originated
- continually adjust verification practices as risks and workflows change

This connected closely to the July 7 discussion about AI-assisted contributions. In both cases, the issue is not simply whether an agent can generate a valid change. The important question is whether the human responsible for the project can understand the intent, evaluate the resulting change, and remain accountable for accepting it.

Participants discussed keeping agent-generated pull requests sufficiently small and understandable. If remediation becomes too large or complex for a human to meaningfully review, the workflow has failed to preserve the intended control boundary.

### Data Quality, Curation, and Context Growth

Another major discussion focused on data.

Participants asked what the next major limitation would be after building workflows like the one demonstrated. The answer emphasized that the challenge increasingly becomes not only obtaining more data, but curating the right data for the specific decision.

Agentic workflows can produce and consume very large amounts of information:

- raw scanner findings
- dependency information
- licensing evidence
- policy mappings
- historical decisions
- project-health information
- generated recommendations
- remediation context

Simply placing all available information into an LLM context does not scale well. It increases token usage, context size, cost, and the risk that irrelevant information obscures the important evidence.

The discussion therefore emphasized **curation** as an important part of agentic architecture.

Rather than creating one agent with access to everything, one possible pattern is to use smaller agents or processing stages that:

- select the relevant data
- synthesize a specific type of evidence
- reduce information before passing it to another step
- specialize around one decision or domain

Participants noted that organizations may eventually accumulate very large datasets not only about software itself, but about previous decisions: whether something was approved, rejected, considered compatible, escalated, or remediated.

This decision data may become valuable context for future agents, but it also creates a new governance problem: determining which historical data remains relevant, authoritative, and appropriate for a particular decision.

### Policy Enforcement and AI Infrastructure

The discussion also touched on organizational controls around AI usage itself, including the ability to enforce policies, constrain model usage, and manage token or infrastructure cost.

An open source project called [AI Proxy Guard](https://aiproxyguard.com/) was shared as an example of infrastructure designed to apply policies around AI usage.

This reinforced a recurring theme in the working group: adopting agentic workflows creates governance needs beyond the individual agent. Organizations may also need infrastructure for:

- model and endpoint access
- policy enforcement
- cost controls
- auditability
- permitted data flows
- organizational guardrails

For OSPOs, these infrastructure questions may overlap with existing relationships across developer experience, security, legal, compliance, platform engineering, and AI governance teams.

### Applying the Workflow Before Open Source Release

Participants asked whether the demonstrated workflow could also be used against private repositories before software is released as open source. The discussion identified this as a relevant use case.

- Organizations could potentially maintain internal skills or workflows that evaluate a project before publication, with checks tailored to the type of project being released. The requirements for a library, mobile application, service, model, or other artifact may differ, so the agentic workflow could combine a common baseline with project-specific checks

This connects directly to existing OSPO release-readiness processes. Instead of replacing those processes, reusable agent skills could encode parts of the organization's existing release guidance and make that guidance available earlier to engineering teams. Possible uses include:

- pre-release open source readiness checks
- licensing and dependency review
- security checks
- repository hygiene
- documentation requirements
- policy-specific checks

The session also discussed that some internal skills developed for these workflows could eventually become reusable open source resources where the underlying logic is broadly applicable

### From Individual Skills to Shared Skill Libraries

The latter part of the meeting shifted from the specific compliance demo to a broader architectural and organizational question: **Where should reusable agent skills live?**

Participants discussed a model where individual teams or repositories create their own skills, while organizations maintain a central location for the most important or broadly reusable ones. Several possible patterns emerged:

- project-specific skills stored with the repository
- shared skills kept in a central organizational repository
- repositories referencing skills maintained elsewhere
- synchronization scripts that distribute shared skills
- internal catalogs or marketplaces that help developers discover available skills
- curated external resources for reusable open source skills

Participants noted that copying the same skill into many repositories creates a maintenance problem. Where possible, organizations may prefer referencing a source of truth or using mechanisms that keep distributed copies synchronized.

For the working group, this also raised the possibility of maintaining pointers to existing resources rather than copying every workflow into a TODO repository.

A shared resource could provide:

- links to existing upstream skills
- examples of how organizations structure skill repositories
- reusable OSPO-focused skills
- references to relevant MCP servers or other agent tooling
- guidance for building organization-specific workflows

### Skills Marketplace for Organizations

Participants discussed how organizations are beginning to think about internal "skills marketplaces" or catalogs.

The idea is that many engineers and teams may be able to create skills, but an organization still needs a way to determine:

- which skills should be broadly promoted
- who owns them
- who reviews updates
- which versions are authoritative
- how users discover trusted skills
- what happens when a skill becomes outdated
- how domain-specific skills are validated

One model discussed was for a developer experience or similar engineering function to operate the central marketplace while allowing individual teams to continue developing their own skills, with the "ownership" of the content should remain with the relevant domain experts. For example:

### Internal Versus External Skill Distribution

Participants also distinguished between internal and external distribution.

Internally, organizations may allow relatively broad experimentation, with many teams creating skills and sharing them through repositories or internal marketplaces.

Externally, organizations may want a much more curated experience. Skills published for customers, users, or the broader community may require additional review to ensure that they:

- work as expected
- remain maintained
- use supported interfaces
- follow security and legal requirements
- point to authoritative documentation
- do not expose outdated organizational practices

One participant suggested that MCP may be particularly useful for exposing capabilities externally, while an internal repository and synchronization model can work well for organization-specific skills.

### Implications for OSPOs

The meeting demonstrated that agentic SCA is not only a compliance automation problem.

As organizations start creating agent workflows around licensing, security, project health, publishing, contribution management, and other open source processes, OSPOs may need to think about the surrounding knowledge and governance layer. Potential OSPO roles discussed or implied by the session include:

- defining which open source decisions can be automated
- identifying where human approval remains necessary
- translating open source policies into machine-consumable rules or skills
- helping curate authoritative sources for agents
- maintaining or co-maintaining licensing and publishing skills
- helping engineering teams use existing open source tools as reliable agent inputs
- participating in internal skill governance and ownership
- helping define release-readiness workflows for private repositories before publication
- sharing reusable workflows with the broader OSPO community where possible

A recurring theme was that domain expertise matters. Agentic AI can make execution faster, but organizations still need people who understand which evidence is authoritative, what the policy means, what constitutes an acceptable decision, and who is accountable for maintaining those rules.

### Mapping to Working Group Workstreams

The session connected strongly to all three proposed working group workstreams

#### Workstream 1: Use Cases and Maturity Mapping

The session provided several concrete use cases for agentic AI in OSPO and open source management workflows:

- agentic SCA and dependency analysis
- license compatibility assessment
- AI artifact identification
- project-health assessment
- dependency remediation
- compliance evidence generation
- pre-release open source readiness review
- policy-aware developer guidance
- human-approved remediation workflows
- organizational skill catalogs and marketplaces

A useful maturity distinction also emerged:

1. tools produce signals for humans
2. agents summarize and contextualize signals
3. agents recommend a decision
4. humans authorize the desired action
5. agents prepare remediation
6. humans review and accept the resulting change

This could provide a useful model for describing different levels of autonomy in future working group outputs

#### Workstream 2: Skills, Prompts, and Workflow Library

This session was particularly relevant to the skills and workflow library. Potential reusable artifacts discussed include:

- license compliance analysis skills
- dependency assessment skills
- open source release-readiness skills
- project-health analysis prompts
- security-focused analysis skills
- maintainer-health skills
- policy datasets for agent decision support
- references to existing MCP servers and agent tooling
- skill contribution and curation policies

#### Workstream 3: Adoption and Evaluation

The session surfaced several criteria for evaluating an agentic workflow beyond whether it technically works. Possible evaluation questions include:

- Does the workflow reduce the number of findings a human must manually interpret?
- Is the underlying evidence still visible and traceable?
- Can humans understand why the agent recommended a particular action?
- Is remediation separated from authorization where appropriate?
- Are generated changes small enough for meaningful human review?
- Are agents using curated and authoritative sources?
- How much irrelevant data is being passed through the workflow?
- What is the token and infrastructure cost?
- Who owns the skills and policies used by the agent?
- How are skills updated when the underlying policy changes?
- Can internal teams identify which skills are trusted?
- Is the workflow useful to engineers or does it simply generate additional tickets?
- Does automation remove work or move more work onto another team?

### Final Remarks

A key takeaway was that organizations already have many useful sources of evidence. The challenge is increasingly how to combine those signals, curate the relevant context, translate organizational policy into reusable guidance, and surface an actionable recommendation without removing human accountability. 

The discussion also expanded the working group's focus from individual agents toward the organizational infrastructure around them. As more teams create AI skills and workflows, OSPOs may need to participate in questions around skill ownership, curation, discoverability, policy maintenance, release readiness, and the distinction between internal experimentation and externally supported workflows. This suggests that one important output for the working group may be not only a collection of prompts or agents, but guidance for how organizations organize and govern reusable skills across domains.

### Action Items

- [x] Working group coordinator: Add the anonymized July 21 meeting summary to the working group repository
- [ ] Working group coordinator: Capture the agentic SCA / GitHub Actions workflow as a show-and-tell example under the working group's practical use cases
- [ ] Working group chairs and interested participants: Explore creating a curated index of reusable OSPO agent skills, workflows, MCP resources, and upstream projects
- [ ] Working group members: Share examples of how their organizations store, distribute, curate, and maintain reusable agent skills

## Summary July 7

This was the fourth meeting of the TODO Group Agentic AI to Empower OSPOs working group. The meeting included a show-and-tell session on Goose and focused on a practical question facing open source maintainers: what happens when AI agents make it much easier for contributors to open issues, generate pull requests, and submit code without deeply understanding the project.

- The session framed a growing maintainer challenge: more AI-assisted contributors does not automatically mean less work. In practice, AI-generated issues and pull requests can increase triage load, review burden, and maintainer burnout when contributions are low quality, too broad, misaligned with project direction, or require extensive human correction
- Key takeaway from the session was that banning AI-generated contributions may not be a realistic long-term answer. AI-assisted development is already becoming part of how many developers work. Instead, projects may need to define how AI can be used responsibly, make repositories easier for agents to understand, and use automation to protect maintainer attention

### Goose Show-and-Tell: Maintaining Projects in the Age of AI Contributors

**Project:** [Goose](https://github.com/aaif-goose/goose)

The show-and-tell used Goose as an example of an open source project experiencing the effects of AI-assisted contribution at scale. The project saw a large increase in contributors and AI-assisted activity, which created a new kind of maintainer pressure.

The presenter described a shift where contributors no longer need to fully understand the codebase before producing a pull request. In theory, this can lower barriers to contribution. In practice, it can also create more “junk” work for maintainers when generated pull requests are incomplete, unfocused, poorly reviewed by the submitter, or taking the project in a direction the maintainers do not want.

The group discussed that this is especially difficult because maintainers often feel they have limited options:

- accepting AI-generated contributions can increase review and triage burden
- rejecting or banning AI-generated work may conflict with how contributors now build software
- ignoring the issue can lead to maintainer burnout
- allowing unrestricted AI-generated contributions can reduce project quality

The session proposed a different approach: do not simply ban AI; build project infrastructure and contribution guidance that makes AI-assisted work easier to review, safer to accept, and less costly for maintainers.

### Tip 1: Tell Humans How to Use AI on the Project

The session highlighted the importance of making clear that the human contributor remains responsible for the final contribution, even when AI tools are used. AI can help draft, explore, or implement, but contributors should still understand, test, and take accountability for what they submit.

The project updated its `CONTRIBUTING.md` guidance to include expectations for AI-assisted contributions. The guidance focused on principles such as:

- think first before generating code
- avoid lazy or unreviewed AI output
- identify uncertainty instead of hiding it
- keep changes focused and minimal
- avoid unnecessary code bloat
- make sure the human contributor can explain the change

This was discussed as a useful pattern for other open source projects: write down what “good AI-assisted contribution” means before the maintainer burden becomes unmanageable

### Tip 2: Make the Repository AI-Friendly

The second recommendation was to make the repository itself easier for AI agents to work with safely. The session described repo readiness as having three parts:

| Area | Purpose |
| --- | --- |
| Context | Help humans and agents understand the project, architecture, conventions, and expectations |
| Rules and instructions | Give AI tools clear project-specific guidance on how to behave |
| Repeatable workflows | Create consistent steps for common tasks such as triage, review, testing, or contribution preparation |

The group discussed that AI agents need onboarding context, similar to human contributors. If project rules only live in maintainers’ heads, agents are likely to make poor assumptions. If those rules are written down in machine-consumable ways, contributors using AI tools are more likely to generate work that fits the project.

One example discussed was using instruction files, such as `copilot-instructions.md`, to tell AI tools what the project cares about. The guidance can include expectations such as:

- keep changes minimal
- keep pull requests focused
- avoid broad rewrites
- follow existing project style
- do not add unnecessary text or code
- explain uncertainty
- run the expected checks before submitting

Because LLMs are non-deterministic and contributors may use many different models and tools, the session also discussed the value of reusable agent skills or workflows. These can guide different agents through a more consistent process, regardless of which tool the contributor uses.

### Tip 3: Use AI to Review AI and Protect Maintainer Attention

The third recommendation was to use AI not only to generate contributions, but also to reduce the review and triage load created by AI-assisted contributions.

The session emphasized that projects do not need to automate everything at once. A more realistic starting point is to use AI in small ways to protect maintainer attention.

Possible areas included:

- issue triage
- pull request review
- identifying incomplete or low-quality contributions
- escalating work that needs human attention
- suggesting when to close, merge, or request changes
- checking whether a contribution follows project rules
- scanning for suspicious or potentially malicious code

The group discussed the idea of AI reviewers or co-reviewers that are configured around project-specific concerns. These tools need to be told what the maintainers care about, rather than giving generic review feedback.

One important benefit discussed was that AI feedback can appear before a human maintainer spends time on the issue or pull request. In that sense, AI can act as an embedded teacher inside the codebase, helping contributors improve their submissions before maintainers need to intervene.

### Maintainer Burden and AI-Generated Contributions

The session made clear that the core issue is not simply whether AI-generated code is good or bad. The deeper issue is how AI changes the economics of contribution.
When the cost of creating an issue or pull request becomes very low, projects may receive more contributions than maintainers can reasonably evaluate. This creates a new kind of asymmetry:

- contributors can generate work quickly
- maintainers still need to understand, review, test, and decide
- low-quality submissions create hidden labor
- project direction can become harder to protect
- human attention becomes the scarce resource

The group discussed that OSPOs and open source communities may need to treat maintainer attention as something that requires active protection. AI governance should not only focus on whether AI can produce code, but also on whether AI-assisted workflows create sustainable maintenance practices.

## Group Discussions

### From Code Contributions to Intent Contributions

A major discussion emerged around whether AI-assisted open source contribution may shift from submitting code to submitting intent.

Participants discussed a possible future model where external contributors do not necessarily send a pull request with generated code. Instead, they may submit a bug description, feature request, prompt, or specification that explains what they want to achieve. Maintainers could then decide whether the intent is useful and, if appropriate, use trusted internal agents, models, security controls, and project workflows to generate or review the implementation.

This model was discussed as a way to reduce the risk of accepting unknown AI-generated code directly from outside contributors. It could allow projects to keep more control over the implementation environment, security posture, and review process.

However, participants also raised concerns with this model. If maintainers are expected to take every external idea and run their own agents to implement it, this may simply move more work onto maintainers rather than reducing their burden. In that sense, asking for intent instead of code does not automatically solve the maintainer sustainability problem.

The group discussed that the useful middle ground may not be “no code contributions,” but better-quality intent and better-quality specifications before code is produced. For larger features especially, contributors may need to first explain the problem, motivation, constraints, and desired outcome before producing a pull request.

### Spec-Driven Development and Better Bug Reports

Participants connected the discussion to spec-driven development. One participant described using agents to interview them through several rounds of questions before writing code, helping clarify the real intent of the change before implementation begins.

This was discussed as a useful pattern for open source contribution:

- better issue descriptions before code
- clearer feature intent before implementation
- more thoughtful bug reports
- more structured discussion before large pull requests
- less pressure on maintainers to reverse-engineer what a contributor or agent was trying to do

The group noted that projects may benefit from teaching contributors how to thoughtfully add things to the project rather than simply teaching them how to generate code. The goal is not only to produce a working patch, but to help maintainers understand why the change matters and whether it belongs in the project.

At the same time, participants cautioned that only accepting specs and requiring maintainers to write all code would not be a good outcome. Open source still depends on contributions from people who can help implement, test, and maintain changes.

### Access, Equity, and Open Source Models

The discussion also touched on access to AI tools. Some participants noted that not every contributor has access to frontier models or paid subscriptions. Younger contributors, students, hobbyists, and contributors in different contexts may rely on open source or lower-cost models.

This raised an important point for open source communities: AI contribution policies should not assume that everyone has equal access to the same tools, models, or infrastructure.

The group discussed that open source models are improving, but may still perform differently from frontier commercial models in some contexts. This creates a practical consideration for projects writing AI contribution guidance: policies should focus on responsible contribution behavior and review quality, not only on specific tools.

### Human Conversation Before AI-Generated Output

Another important theme was that contributors should remember they are interacting with humans, not just with a repository.

Participants discussed that maintainers may be more open to AI-assisted contributions when contributors first create a human connection, explain what they are trying to do, and have a conversation about the issue before submitting large amounts of generated code.

This connects to existing open source norms that predate AI: for larger changes, contributors are often expected to open an issue or discussion before writing code. AI makes this even more important because it is now easier to generate large changes quickly.

The group discussed that a useful AI contribution policy may not need to start with a ban. Instead, it can start with expectations such as:

- open an issue before large changes
- explain the problem before submitting generated code
- be clear about the intent of the contribution
- respond to maintainer feedback as a human
- do not flood maintainers with AI-generated content
- do not treat maintainers as a validation service for unreviewed AI output

### Practical Tools and Workflow Patterns

Participants also asked what concrete tools or workflow patterns were being used to support this work. The answer emphasized that the most important pieces were not magic products, but repository-level context, rules, and reusable skills that can work across different agents.

Examples included:

- context files that explain the project
- rules files that define expected AI behavior
- contribution instructions for humans using AI
- skills or workflows that guide agents through repeatable steps
- AI-assisted review using tools such as Codex
- security scanning to detect suspicious or malicious code

The group discussed that these patterns should ideally work across different agents, not only one specific tool. If the repository carries the context and rules, then contributors using different AI tools can still be guided toward more consistent behavior

### Introducing AI Tools Without Creating More Work

Participants also discussed the challenge of moving from theory to practice when introducing AI tools into internal OSPO or open source management workflows.

A key point was that many OSPO objectives are based around self-service, discoverability, and helping one or a few people support many internal teams. In that context, AI tools can be attractive because they appear to make work faster, more scalable, and easier to access.

However, the discussion emphasized that introducing a new tool does not automatically reduce workload. If the tool is not carefully integrated into existing workflows, it can create additional support needs, new expectations, and more work for the OSPO or maintainers responsible for operating it.

Participants noted that AI tools should not be introduced only because they are interesting or promising. The more important question is whether they can be safely introduced in a way that:

- reduces a real bottleneck
- does not create more operational burden
- can be supported by the available team
- improves self-service without removing needed human judgment
- fits into the existing workflow instead of adding another disconnected process

One example discussed was the use of AI to support open source publishing workflows. AI could help generate reports or publishing notes faster than a person could manually create them, removing reporting as a bottleneck. However, this may also create an expectation that the whole workflow will now move faster, even if other parts of the process still require human review, coordination, approvals, or follow-up.

The group discussed that AI may accelerate one part of the workflow without changing the overall capacity of the team. This makes expectation-setting important: AI can improve specific steps, but it does not magically change the amount of time, attention, or staffing available.

### Related Policy Work

The OpenSSF TAC draft AI policy was shared as a related reference point:https://github.com/ossf/tac/pull/605

Participants noted that this type of policy work is useful because many projects are trying to decide how to handle AI-generated contributions. The group discussed that policies should be thoughtful about the difference between banning AI outright, discouraging low-quality AI-generated submissions, and encouraging responsible AI-assisted contribution practices

## Mapping to Working Group Workstreams

The Goose session connected in different ways to the working group’s three proposed workstreams:

### Workstream 1: Use Cases and Maturity Mapping

This session provided a few use cases around AI-assisted open source project maintenance and internal OSPO operations.

Some project-maintenance use cases mentioned:

- AI-assisted issue triage
- AI-assisted pull request review
- AI guidance for contributors
- repo readiness for agentic workflows
- AI-generated contribution management
- maintainer burden reduction
- security scanning for AI-generated code
- intent-first or specification-first contribution workflows

Internal OSPO operations use cases mentioned:

- generating open source project reports
- drafting publishing notes
- improving internal self-service workflows
- reducing reporting bottlenecks
- helping teams discover open source management guidance
- supporting one-to-many OSPO service models

### Workstream 2: Skills, Prompts, and Workflow Library

The session suggested that OSPOs could help projects turn implicit maintainer knowledge into reusable instructions, workflows, and policies that both humans and agents can follow. It also reinforced that prompts and skills should not only generate outputs. They should clarify what the AI can do, what humans still need to review, and where the workflow stops. Reusable examples that could be collected include:

- AI contribution policy language for `CONTRIBUTING.md`
- examples of `copilot-instructions.md` or similar files 
- agent skills for issue triage
- agent skills for pull request review
- prompts for detecting low-quality AI-generated work
- prompts for keeping changes minimal and focused
- repository-readiness checklists for AI agents
- prompts for improving issue descriptions before code is written
- prompts for generating open source project reports
- templates for publishing notes
- checklists for when AI-generated reports still need human review

### Workstream 3: Adoption and Evaluation

This discussion highlighted that successful AI adoption should not only be measured by output volume or speed. For open source projects, a better measure may be whether the workflow protects maintainer time and improves contribution quality. For OSPOs, a better measure may be whether the tool improves the overall workflow without increasing hidden labor

Evaluation criteria for AI-assisted project maintenance could include:

- whether AI reduces or increases maintainer workload
- whether AI-generated contributions are easy to review
- whether contributor guidance improves submission quality
- whether AI review catches obvious problems before human review
- whether security scans detect suspicious or malicious changes
- whether the project can preserve quality and direction
- whether maintainers feel more protected or more burdened
- whether contributors remain accountable for their submissions
- whether the workflow improves human conversation before code is generated

Evaluation criteria for internal OSPO workflows could include:

- whether the tool reduces a real bottleneck
- whether it creates new support or maintenance work
- whether it creates unrealistic expectations from internal teams
- whether it improves self-service and discoverability
- whether it preserves necessary human review
- whether the OSPO or responsible team can actually support it
- whether it accelerates the full workflow or only one step
- whether it makes work easier for the team or just moves the burden elsewhere

## Final Remarks

The session positioned Goose as a practical example of how open source projects can respond to AI-assisted contributions without simply banning it. For OSPOs, this creates a useful area of work where they could help projects and organizations define responsible AI contribution policies, prepare repositories for AI-assisted workflows, create reusable agent instructions, and evaluate whether AI is reducing or increasing maintainer burden

The discussion also highlighted that AI governance for open source should also include maintainability, contributor behavior, review burden, project sustainability, access to AI tools, and internal workflow impact (and not only legal, licensing, or security)

## Action Items

- [x] Working group coordinator: Add the anonymized July 7 meeting summary to the working group repository
- [ ] Working group coordinator: Capture Goose as a show-and-tell example under the working group’s practical use cases output
- [ ] Working group chairs: Consider adding “AI-generated contribution management” as a specific use case under the use cases and maturity mapping workstream
- [ ] Working group chairs: Consider adding “AI-assisted internal OSPO publishing and reporting workflows” as a separate use case under the use cases and maturity mapping workstream
- [ ] Working group chairs and interested participants: Collect examples of AI contribution guidance for `CONTRIBUTING.md`
- [ ] Working group chairs and interested participants: Collect examples of repo-level AI instruction files, such as `copilot-instructions.md`
- [ ] Working group members: Discuss whether the working group should create a lightweight “AI-ready repository” checklist for OSPOs and maintainers or should be part of a new TODO Guide


# Summary June 30

This was the third meeting of the TODO Group Agentic AI to Empower OSPOs working group. The meeting included a show-and-tell session on OpenFab and focused on trustworthy software in the age of AI-assisted authorship, with particular attention to provenance, attestations, reproducibility, and how OSPOs can help organizations govern AI-generated contributions instead of banning them

The session framed a growing challenge for software organizations: as a higher percentage of code is written or modified with AI assistance, organizations need stronger ways to understand who or what produced software artifacts, what process was followed, what approvals were applied, and whether the resulting artifact can be verified later

Participants discussed OpenFab as an AI-native CI and provenance gate rather than a replacement for existing coding tools. The core idea presented was: natural language and AI-assisted generation can remain part of the developer workflow, while signed provenance, attestations, AI-BOM metadata, and reproducibility checks travel with the software artifact

## OpenFab Demo: Trustworthy Software in the Age of AI Authorship

**Slides:** [OpenFab — Trustworthy Software in the Age of AI Authorship](https://github.com/Open-fab-ai/community/blob/main/presentations/2026-06-30-todo-group-agentic-ai/OpenFab_TODO_WG_June30.pdf)

The demo introduced OpenFab as a way to produce signed provenance for AI-assisted software workflows. Rather than focusing on the coding assistant itself, OpenFab focuses on the surrounding trust layer: who or what generated the artifact, what contract or workflow was used, what was approved, and who signed the resulting evidence.

A key distinction discussed was:

| SBOMs | OpenFab AIBOM |
| --- | --- |
| describe what is in the software | describe who or what produced it, under which process, and with which attestations| 

The demo showed how AI-related provenance can be committed alongside the code in Git, including attestation files and AI-BOM metadata. This allows the evidence to remain attached to the artifact and repository history, instead of depending only on a specific platform, tool, or external service.

Participants discussed why this matters for OSPOs and enterprise open source governance. As AI-generated code becomes more common, organizations may need to prove that inbound and internal AI-assisted contributions went through a governed process. The discussion connected this to customer expectations, compliance pressure, software supply chain trust, and regulatory requirements such as the EU Cyber Resilience Act

## Artifact-Centric Provenance and offline Verification

A central message from the demo was that trust should travel with the artifact, not only with the platform where the artifact was created or hosted:

- The demo highlighted that the same signed artifact could be pushed to multiple forges, such as GitHub and Gitea, then cloned and verified locally without depending on a forge API or platform-specific runtime state

The verification example showed that when the artifact remained unchanged:

- signatures were valid
- the source was bit-identical
- checks re-passed
- the artifact was reproducible
- and verification worked offline across different forges

The demo also showed the tamper-evidence case: when one byte changed, verification failed and the artifact was no longer considered reproducible. This illustrated how integrity, authenticity, AI provenance, and contract information can remain re-checkable after the artifact leaves the original environment

## AI-BOM, Attestations, and Git-Based Evidence

Participants discussed the role of the AI-BOM as one of OpenFab’s key contributions. The AI-BOM and attestation files can be committed into Git alongside the code, making AI-related provenance part of the repository’s evidence trail

The group discussed how this approach could help organizations answer questions such as:

- Was this code generated or modified with AI assistance?
- Which workflow, model, agent, or tool was involved?
- Who approved the generated output?
- What tests, gates, or checks were run?
- Can the artifact be reproduced and verified later?
- Can the evidence be inspected independently of a single forge or vendor platform?

This was positioned as especially relevant for organizations that need to govern inbound AI-generated contributions, support auditability, and provide evidence to customers, product teams, security teams, legal teams, or compliance stakeholders

## OSPO Role in Governing AI Contributions

The discussion explored why OSPOs may benefit from tools and patterns like OpenFab

- Participants noted that OSPOs may not always directly own the implementation of developer tooling or security gates. However, OSPOs are often well-positioned to identify governance gaps, recommend practices, and connect the right internal teams

Several possible OSPO roles were discussed:

- helping organizations govern AI-generated contributions instead of banning them outright
- identifying where AI provenance is needed in open source intake or contribution workflows
- recommending tools and practices to developer experience, product security, platform, legal, and compliance teams
- supporting internal policy development around AI-assisted open source contributions
- helping product teams prepare for customer or regulatory questions about AI-generated software
-  connecting open source governance work with software supply chain security practices

Participants also discussed how developer experience teams, product security teams, incident response teams, platform teams, and teams maintaining internal AI gateways may be key audiences or collaborators for this type of workflow

## Open Questions and Discussion

Participants asked how OpenFab would work when developers use their existing tools, such as Copilot, VS Code, or other AI coding assistants

- The answer discussed was that OpenFab is not intended to replace those tools. Developers could continue using their existing coding environments, while OpenFab provides a CLI and workflow layer for generating provenance, attestations, and AI-BOM evidence. The provenance workflow could also be integrated into automated triggers or CI pipelines

Participants also asked what happens if someone else generated or modified part of the AI-assisted code

- The discussion pointed back to the need for signed attestations and provenance records that can capture the relevant actors, workflow steps, approvals, and evidence attached to the artifact

Another question focused on ownership: who inside an enterprise should own or operate a tool like this?

- The group discussed that ownership may vary by organization. OSPOs may help identify the need and provide recommendations, while implementation could involve internal IT tools teams, developer experience teams, product security, platform engineering, compliance, or AI gateway teams. In larger enterprises, OSPOs may play a coordination role by connecting these teams and translating open source governance needs into practical tooling requirements.


Participants asked how the approval gate would work, especially for N-of-M approval flows and reviewer roles. The question raised whether OpenFab could use an existing company identity system, such as SSO, Active Directory, GitHub Enterprise groups, OIDC, or SAML, to decide who is allowed to approve, or whether OpenFab would require a separate list of users and roles

- The discussion emphasized that enterprise adoption would benefit from integration with existing identity and role systems rather than maintaining a separate approval database. This would allow organizations to map existing review-board roles or approval groups into the provenance and gate workflow.

## Trial / Pilot Project Opportunity: AI Provenance for OSPOs

One proposed next step by the presenter was to co-develop an OpenFab trial or pilot project with organizations interested in testing how provenance could be applied to inbound AI-assisted contributions, internal software workflows, or enterprise open source governance processes.
Participants were encouraged to take the topic back to their own organizations and consider where AI provenance could address specific challenges, such as:

- governing AI-assisted open source contributions
- documenting provenance for customer-facing software
- supporting CRA-related readiness
- improving auditability of AI-generated code
- creating reusable OSPO guidance for AI contribution governance
- connecting OSPO workflows with OpenSSF and software supply chain security practices

The group discussion noted that this topic may be relevant to adjacent communities such as OpenSSF, especially where provenance, attestations, maintainership, vulnerability response, and software supply chain trust intersect

## Final Remarks

- OpenFab was presented as one example of how organizations might move from “AI was used somewhere” to a more structured and verifiable model where AI-assisted software artifacts include signed provenance, approval evidence, and reproducibility checks
- The group identified AI provenance as a relevant topic for future working group exploration, especially where OSPOs need to help organizations govern AI-generated contributions, support internal adoption, and prepare for external compliance or customer trust expectations

## Action Items

- [ ] Working group coordinator: Add the anonymized June 30 meeting summary to the working group repository
- [ ] Working group coordinator: Capture OpenFab as a possible show-and-tell example under the working group’s practical use cases output
- [ ] Working group chairs: Consider creating a dedicated discussion issue or workstream topic on AI provenance for OSPOs
- [ ] Working group chairs and interested participants: Explore whether an OpenFab trial or pilot could be co-developed with organizations interested in provenance for inbound AI-assisted contributions
- [ ] All working group members: Take the OpenFab provenance topic back to their organizations and identify where AI-generated contribution governance is currently a challenge
- [ ] All working group members: Share feedback on whether AI-BOMs, attestations, reproducibility checks, and approval gates should be part of the working group’s adoption and evaluation guidance

# Summary June 9

This was the second meeting of the TODO Group Agentic AI to Empower OSPOs working group. The meeting focused on reviewing the kickoff recap, discussing early participant feedback, and organizing the group’s work into practical workstreams.

The group reviewed the initial themes from the May 26 kickoff, including the role of OSPOs in AI adoption, the distinction between deterministic and agentic workflows, and the need for shared patterns, recommendations, and reusable resources rather than building new tooling from scratch.

Participants shared additional examples of Agentic AI to automate work already being explored across different organizations. These agentic workflows examples included:

- CLI-based agent workflows connected to open source security tooling
- Malware analysis support for open source security communities
- workflows to support the end-to-end open source contribution lifecycle
- Open source readiness and security checks, including secret-leak detection and checklist-based review processes
- Developer-facing guidance to help contributors understand how to contribute safely without exposing sensitive information

Another topic raised was whether the working group should address open source AI versus closed AI solutions:

- Participants noted that this is strategically relevant for OSPOs, but also complex because “open source AI” remains difficult to define consistently
- The group discussed that its primary role may not be to recommend specific models, but rather to help OSPOs understand evaluation criteria, governance implications, and practical adoption patterns
- This aligns with broader Linux Foundation ecosystem discussions around open collaboration, open models, shared standards, and interoperability, including the Agentic AI Foundation’s focus on reducing fragmentation and advancing open protocols, and recent LF intent to form the Tokenomics Foundation for AI infrastructure cost standards and model evaluation

The group then reviewed survey results and participant input. More than half of respondents indicated that they are already using or testing AI workflows in production or production-adjacent contexts. This reinforced the need for the working group to balance high-level guidance with practical examples, implementation lessons, and reusable artifacts.

Participants then reacted to three proposed workstreams that the group could focus on:

1. Use cases and maturity mapping: Where are OSPOs applying agentic AI today?
2. Skills, prompts, and workflow library: What reusable examples, prompts, skills, tools, or workflows can OSPOs share and adapt?
3. Adoption and evaluation: How can OSPOs assess whether an agentic AI workflow is safe, useful, and appropriate to adopt?

Around 20 participants joined from OSPOs, companies, academic institutions, public sector organizations, and community roles. These participants expressed the strongest interest in the second workstream, focused on reusable skills, prompts, and workflow examples. The visible reaction counts were: 

- Workstream 1: 4 votes
- Workstream 2: 9 votes
- Workstream 3: 2 votes
- N/A: 5 votes


## AI Workflows and OSPO Use Cases

Participants discussed several practical areas where agentic AI may support OSPO work. These included open source contribution workflows, compliance and security checks, open source request evaluation, malware analysis, and project-specific guidance for developers. Two topics were discussed:

- **The importance of helping organizations identify the actual OSPO problem first, before deciding whether Agentic AI is the right solution**: Participants suggested that the working group could collect common OSPO pain points and then map which ones may be appropriate for deterministic automation, agentic workflows, or human-led processes.

- **How OSPOs can become better “upstream sources” for AI systems by making policies, contribution guidance, governance rules, metadata, and project context easier for agents to consume**: This was identified as a possible area for the second workstream (Skills, prompts, and workflow library), especially where reusable documentation, prompts, workflows, and metadata patterns could help organizations prepare their open source knowledge bases for AI-assisted use.

## Open Source AI, Local Models, and Control Boundaries

Participants discussed whether OSPOs should promote open source or open-weight AI models over closed solutions. Several participants noted that this is an important but sensitive area, especially because definitions of “open source AI” are still evolving and may carry legal, policy, or governance implications.

The group noted that this working group may be better positioned to provide evaluation frameworks rather than recommendations for specific models. Relevant evaluation criteria could include:

- transparency and auditability,
- security and privacy requirements,
- model licensing and usage restrictions,
- cost and operational sustainability,
- ability to run locally or in controlled environments,
- suitability for human-in-the-loop workflows

Participants also raised the strategic question of when to use local models versus cloud-hosted models. Some organizations want to keep development information in-house, which makes local LLMs or open-weight models attractive. Others may need cloud models for accuracy, availability, scale, or multilingual performance.

The discussion also touched on the boundary between agents and human review. Participants highlighted the need to define where humans remain accountable, when an agent can act autonomously, and when a workflow should require approval before taking action.

## Validation, Reliability, and Language Considerations

A possible additional area of work emerged around the validation of data and outputs. Participants discussed the need to evaluate how many models should be used, how outputs should be checked, and how organizations can assess whether an AI-assisted workflow is reliable enough for OSPO contexts.

Language was also raised as an important concern. Participants noted that AI performance may vary across languages, for example where English outputs may be more reliable than Japanese in some contexts. This creates practical challenges for global organizations and multilingual open source communities.

The group briefly connected this to broader discussions on transparent and inclusive AI, including the importance of making AI systems usable and reliable across different languages and regions.

## Meeting Format and Community Collaboration

Participants shared feedback on the meeting format:

- **Why people joined the working group**: to learn how others are using agentic AI in OSPO work, understand practical deployment patterns, and collaborate on shared approaches

- **There was strong interest in adding structured show-and-tell sessions to future meetings**: Participants suggested that prepared demos or short presentations could be more useful than only spontaneous examples. These sessions could highlight real-world use cases, tools, workflows, prompts, and lessons learned from different organizations

The group also discussed the value of inviting participants who shared practical examples during the kickoff to present more deeply in future meetings.

## Workstream Direction

The group discussed the initial workstream structure and agreed that the proposed categories are a useful starting point. Based on feedback, the workstreams may evolve as follows:

### Workstream 1: Use Cases and Maturity Mapping

This workstream would collect and organize where OSPOs are currently applying agentic AI. It could map use cases by maturity level, such as exploration, prototype, internal production, or organization-wide adoption.

Possible areas include:

* compliance automation,
* open source request review,
* contribution readiness,
* documentation support,
* security and malware analysis,
* developer enablement,
* release and repository management,
* community support workflows.

### Workstream 2: Skills, Prompts, and Workflow Library

**This workstream received the strongest participant interest during the session**. It would focus on collecting reusable examples that OSPOs can adapt.

Possible outputs include:

- prompt examples,
- agent instructions,
- reusable skills,
- workflow templates,
- metadata patterns,
- policy-to-agent guidance,
- examples of how to structure OSPO knowledge so agents can consume it safely

This workstream could also include guidance on how OSPOs can make their own documentation, policies, and contribution rules more usable for AI-enabled workflows.

### Workstream 3: Adoption and Evaluation

This workstream would focus on how OSPOs can decide whether an AI workflow is safe, useful, reliable, and worth adopting. Possible areas include:

- deterministic versus agentic workflow selection,
- human-in-the-loop checkpoints,
- reliability and reproducibility,
- privacy and sensitive data boundaries,
- cloud versus local model decisions,
- cost and token usage considerations,
- multilingual performance,
- governance and accountability,
- validation practices

This area connects closely with emerging ecosystem discussions about AI cost management, open infrastructure economics, and standards for AI infrastructure usage. The Linux Foundation’s announced intent to launch the Tokenomics Foundation specifically focuses on open standards, benchmarks, and best practices for AI infrastructure economics, which may become relevant for OSPOs evaluating the sustainability of agentic workflows.  

## Final Remarks

The group agreed that the working group should remain practical and community-driven. Rather than focusing only on abstract AI governance questions or recommending specific tools, the group should help OSPOs understand real Agentic AI use cases, share reusable workflows, and define evaluation criteria for safe and effective adoption.

Participants showed particular interest in practical examples, prepared demos, and reusable resources. The next stage of the working group will focus on documenting early use cases and identifying people who can contribute examples or lead specific areas of work

## Action Items

- [x] Working group coordinator: Publish the anonymized June 9 meeting summary in the working group repository
- [x] Working group coordinator: Create GitHub issues to track workstream participation, suggested use cases, and proposed future show-and-tell sessions
- [x] Working group coordinator: Document the initial workstream structure based on participant feedback:
    - Use cases and maturity mapping
    - Skills, prompts, and workflow library
    - Adoption and evaluation
- [x] Working group chairs: Work on a format to include a structured show-and-tell section to future meetings, with prepared demos or short presentations from participants
- [x] Working group chairs: Identify participants who shared concrete use cases during the first two meetings and invite them to present a deeper walkthrough in a future session
- [x] All working group members: Volunteer to present a short walkthrough or show-and-tell during an upcoming working group call
- [x] All working group members: Share examples of prompts, skills, workflows, tools, or internal patterns that could be adapted by other OSPOs in teh Awesome OSS Management repo issue
- [x] All working group members: Suggest common OSPO problems that may be suitable for agentic AI, deterministic automation, or human-led workflows



# Summary May 26


This was the kickoff meeting for a new TODO working group focused on AI adoption in Open Source Program Offices (OSPOs). The working group chairs introduced the group’s purpose as a natural evolution of previous discussions about OSPOs’ roles in AI conversations and technology adoption

Participants shared current AI implementation experiences across different organizations, covering use cases such as license compliance automation, documentation refinement, commit message quality checks, evaluation of open source requests, developer-facing programmatic skills, and AI-enabled contribution workflows.

Key challenges discussed included:

- determining when to use agentic AI versus deterministic workflows,
- managing costs as model usage becomes more expensive,
- ensuring reproducibility and security, and
- the need for community validation of AI tools and practices

The group agreed to focus on creating shared resources, patterns, recommendations, and specifications rather than building new tooling from scratch. Participants also discussed opportunities to collaborate with other existing working groups and refine the working group charter based on feedback from this initial discussion.

## AI Adoption in OSPOs Kickoff

The meeting opened with an introduction to the new working group focused on AI adoption within OSPOs. Important participation guidelines were reviewed, including Linux Foundation antitrust policies and Chatham House Rules.

Participants discussed how conversations around AI and OSPOs have evolved over the past two years. OSPO team members were described as well-positioned to contribute to AI adoption discussions because of their cross-functional connections across legal, compliance, engineering, security, product, and community teams.

The working group aims to move beyond conceptual discussions about AI adoption and explore how these technologies are being used internally to accelerate OSPO work.

## OSPO AI Adoption Evolution

The group discussed how OSPO involvement in AI adoption is shifting from policy-focused conversations toward practical tooling, implementation support, and shared learning.

Participants highlighted the value of creating a shared resource and knowledge-sharing space, especially in a context where many organizations face hiring or capacity constraints and may increasingly rely on tool-based solutions.

A survey was introduced to assess members’ current engagement levels with AI initiatives, ranging from observation and exploration to prototyping, testing, and production use. This input may help frame future meetings and identify potential subgroups based on activity levels.

## Open Source AI Workflows Discussion

Participants shared examples of deterministic AI workflows for open source compliance, with a focus on cost, security, and reproducibility. 

- One example focused on building programmatic “skills” for developers to use, such as deterministic license-checking skills that could help developers identify and fix issues before submitting work to the OSPO for review.

Others noted active experimentation with agentic AI workflows and expressed interest in learning how different organizations are approaching implementation.

- Examples included automating license compliance work, improving commit message quality at scale, and exploring where AI can support recurring OSPO review processes.

## AI and Open Source Automation

Several participants shared practical AI use cases already being tested or implemented. These included refining documentation with bots, comparing AI-generated responses against human answers to identify documentation gaps, and automating parts of open source request evaluation.

- Specific examples included an AI agent running inside a Microsoft Teams channel to answer first-line documentation questions, and agents being used to address Release Hub management bottlenecks such as GitHub permissions, team creation, and assignments.

Other examples included tools that help automate the open source publishing process, including code review, intellectual property review, and security checks. Participants also discussed systems that provide AI tools with project-specific context, such as governance rules, conventions, and contribution expectations.

## AI Implementation in Open Source

Participants discussed the use of AI agents to support project reviews and contribution requests. While these tools were reported to improve productivity, several participants emphasized that many implementations remain experimental.

Three broad areas for AI implementation emerged from the discussion:

1. Automating OSPO work.
2. Providing AI tooling and processes for open source projects.
3. Addressing responsible open source publishing and contribution practices.

Participants also shared examples of developer-facing automation, such as checks that reduce review iterations and suggest pull requests when issues are found.

- The PyTorch community was mentioned as a specific environment where AI-enabled contribution policies are being explored

## AI Collaboration and Tool Development

The group emphasized the importance of focusing on common problems before jumping to specific solutions. Participants noted that sustained collaboration will be important to avoid repeating the challenges of previous tooling efforts.

A potential distinction emerged between AI usage for internal OSPO operations and AI usage for compliance or open source management workflows. Participants expressed interest in sharing reusable tools, patterns, and practices across organizations.

The group also discussed the value of community collaboration and validation when developing AI tools, especially in areas such as documentation, git commit messages, compliance checks, and contribution workflows

- External tooling communities were also mentioned, including the OSS-Based Compliance Tooling community: https://oss-compliance-tooling.org/

## Open Source AI Workflow Improvements

The working group discussed how agentic workflows could improve productivity for open source maintainers and how organizations might develop policies for AI-generated code contributions

Participants compared agentic and deterministic workflows, noting that deterministic approaches can be useful upfront to guide AI behavior, improve reproducibility, and control costs

## Final Remarks

The group agreed that the working group should focus on higher-level recommendations, shared patterns, and practical resources rather than detailed technical architectures. The draft charter will be refined based on feedback from the discussion and survey responses. 


## Next Steps

- [x] All working group members: Provide input and feedback on the draft charter in the group’s GitHub repository, either by opening a pull request or by opening an issue with thoughts or questions

- [x] All working group members: Share tools, specs, or artifacts they are building or experimenting with by contributing to the relevant section in the awesome OSPO issue [Add AI workflows, prompts, and tools for OSPOs](https://github.com/todogroup/awesome-ospo/issues/75)

- [x] Working group coordinator: Summarize the meeting transcript, ensuring all names and affiliations are removed, and post the anonymized summary in the GitHub repository under meeting notes

- [x] Working group chairs: Review and synthesize feedback and new entries in the open issues and charter to help define group outcomes and collaboration points with other relevant working groups

- [x] Working group chairs: Prepare an outline for the next meeting

- [x] All working group members: Continue relevant discussions and share updates in the dedicated Slack channel

- [x] Working group coordinator: Set up a bi-weekly recurring meeting series for the working group

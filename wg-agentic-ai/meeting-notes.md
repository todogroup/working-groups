## Instructions for Adding New Meeting Notes

When adding notes for a new meeting:

1. Add the meeting date to the list below using the format:

   ```markdown
   - [YYYY-MM-DD](#summary-month-day)

# Table of Contents:
- [2026-07-07](#summary-july-7)
- [2026-06-30](#summary-june-30)
- [2026-06-09](#summary-june-9)
- [2026-05-26](#summary-may-26)

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

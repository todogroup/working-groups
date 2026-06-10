## Instructions for Adding New Meeting Notes

When adding notes for a new meeting:

1. Add the meeting date to the list below using the format:

   ```markdown
   - [YYYY-MM-DD](#summary-month-day)

# Table of Contents:

- [2026-06-09](#summary-june-9)
- [2026-05-26](#summary-may-26)

## Summary June 9

This was the second meeting of the TODO Group Agentic AI to Empower OSPOs working group. The meeting focused on reviewing the kickoff recap, discussing early participant feedback, and organizing the group’s work into practical workstreams.

The group reviewed the initial themes from the May 26 kickoff, including the role of OSPOs in AI adoption, the distinction between deterministic and agentic workflows, and the need for shared patterns, recommendations, and reusable resources rather than building new tooling from scratch.

Participants shared additional examples of Agentic AI to automate work already being explored across different organizations. These agentic workflows examples included:

- CLI-based agent workflows connected to open source security tooling
- Malware analysis support for open source security communities
- workflows to support the end-to-end open source contribution lifecycle
- Open source readiness and security checks, including secret-leak detection and checklist-based review processes
- Developer-facing guidance to help contributors understand how to contribute safely without exposing sensitive information

Another topic raise was whether the working group should address open source AI versus closed AI solutions:

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


### AI Workflows and OSPO Use Cases

Participants discussed several practical areas where agentic AI may support OSPO work. These included open source contribution workflows, compliance and security checks, open source request evaluation, malware analysis, and project-specific guidance for developers. Two topics were discussed:

- **The importance of helping organizations identify the actual OSPO problem first, before deciding whether Agentic AI is the right solution**: Participants suggested that the working group could collect common OSPO pain points and then map which ones may be appropriate for deterministic automation, agentic workflows, or human-led processes.

- **How OSPOs can become better “upstream sources” for AI systems by making policies, contribution guidance, governance rules, metadata, and project context easier for agents to consume**: This was identified as a possible area for the second workstream (Skills, prompts, and workflow library), especially where reusable documentation, prompts, workflows, and metadata patterns could help organizations prepare their open source knowledge bases for AI-assisted use

### Open Source AI, Local Models, and Control Boundaries

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

### Validation, Reliability, and Language Considerations

A possible additional area of work emerged around the validation of data and outputs. Participants discussed the need to evaluate how many models should be used, how outputs should be checked, and how organizations can assess whether an AI-assisted workflow is reliable enough for OSPO contexts.

Language was also raised as an important concern. Participants noted that AI performance may vary across languages, for example where English outputs may be more reliable than Japanese in some contexts. This creates practical challenges for global organizations and multilingual open source communities.

The group briefly connected this to broader discussions on transparent and inclusive AI, including the importance of making AI systems usable and reliable across different languages and regions.

### Meeting Format and Community Collaboration

Participants shared feedback on the meeting format:

- **Why people joined the working group**: to learn how others are using agentic AI in OSPO work, understand practical deployment patterns, and collaborate on shared approaches

- **There was strong interest in adding structured show-and-tell sessions to future meetings**: Participants suggested that prepared demos or short presentations could be more useful than only spontaneous examples. These sessions could highlight real-world use cases, tools, workflows, prompts, and lessons learned from different organizations

The group also discussed the value of inviting participants who shared practical examples during the kickoff to present more deeply in future meetings.

### Workstream Direction

The group discussed the initial workstream structure and agreed that the proposed categories are a useful starting point. Based on feedback, the workstreams may evolve as follows:

#### Workstream 1: Use Cases and Maturity Mapping

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

#### Workstream 2: Skills, Prompts, and Workflow Library

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

#### Workstream 3: Adoption and Evaluation

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

### Final Remarks

The group agreed that the working group should remain practical and community-driven. Rather than focusing only on abstract AI governance questions or recommending specific tools, the group should help OSPOs understand real Agentic AI use cases, share reusable workflows, and define evaluation criteria for safe and effective adoption.

Participants showed particular interest in practical examples, prepared demos, and reusable resources. The next stage of the working group will focus on documenting early use cases and identifying people who can contribute examples or lead specific areas of work

### Action Items

- [ ] Working group coordinator: Publish the anonymized June 9 meeting summary in the working group repository
- [ ] Working group coordinator: Create GitHub issues to track workstream participation, suggested use cases, and proposed future show-and-tell sessions
- [ ] Working group coordinator: Document the initial workstream structure based on participant feedback:
    - Use cases and maturity mapping
    - Skills, prompts, and workflow library
    - Adoption and evaluation
- [ ] Working group chairs: Work on a format to include a structured show-and-tell section to future meetings, with prepared demos or short presentations from participants
- [ ] Working group chairs: Identify participants who shared concrete use cases during the first two meetings and invite them to present a deeper walkthrough in a future session
- [ ] All working group members: Volunteer to present a short walkthrough or show-and-tell during an upcoming working group call
- [ ] All working group members: Share examples of prompts, skills, workflows, tools, or internal patterns that could be adapted by other OSPOs in teh Awesome OSS Management repo issue
- [ ] All working group members: Suggest common OSPO problems that may be suitable for agentic AI, deterministic automation, or human-led workflows



## Summary May 26


This was the kickoff meeting for a new TODO working group focused on AI adoption in Open Source Program Offices (OSPOs). The working group chairs introduced the group’s purpose as a natural evolution of previous discussions about OSPOs’ roles in AI conversations and technology adoption

Participants shared current AI implementation experiences across different organizations, covering use cases such as license compliance automation, documentation refinement, commit message quality checks, evaluation of open source requests, developer-facing programmatic skills, and AI-enabled contribution workflows.

Key challenges discussed included:

- determining when to use agentic AI versus deterministic workflows,
- managing costs as model usage becomes more expensive,
- ensuring reproducibility and security, and
- the need for community validation of AI tools and practices

The group agreed to focus on creating shared resources, patterns, recommendations, and specifications rather than building new tooling from scratch. Participants also discussed opportunities to collaborate with other existing working groups and refine the working group charter based on feedback from this initial discussion.

### AI Adoption in OSPOs Kickoff

The meeting opened with an introduction to the new working group focused on AI adoption within OSPOs. Important participation guidelines were reviewed, including Linux Foundation antitrust policies and Chatham House Rules.

Participants discussed how conversations around AI and OSPOs have evolved over the past two years. OSPO team members were described as well-positioned to contribute to AI adoption discussions because of their cross-functional connections across legal, compliance, engineering, security, product, and community teams.

The working group aims to move beyond conceptual discussions about AI adoption and explore how these technologies are being used internally to accelerate OSPO work.

### OSPO AI Adoption Evolution

The group discussed how OSPO involvement in AI adoption is shifting from policy-focused conversations toward practical tooling, implementation support, and shared learning.

Participants highlighted the value of creating a shared resource and knowledge-sharing space, especially in a context where many organizations face hiring or capacity constraints and may increasingly rely on tool-based solutions.

A survey was introduced to assess members’ current engagement levels with AI initiatives, ranging from observation and exploration to prototyping, testing, and production use. This input may help frame future meetings and identify potential subgroups based on activity levels.

### Open Source AI Workflows Discussion

Participants shared examples of deterministic AI workflows for open source compliance, with a focus on cost, security, and reproducibility. 

- One example focused on building programmatic “skills” for developers to use, such as deterministic license-checking skills that could help developers identify and fix issues before submitting work to the OSPO for review.

Others noted active experimentation with agentic AI workflows and expressed interest in learning how different organizations are approaching implementation.

- Examples included automating license compliance work, improving commit message quality at scale, and exploring where AI can support recurring OSPO review processes.

### AI and Open Source Automation

Several participants shared practical AI use cases already being tested or implemented. These included refining documentation with bots, comparing AI-generated responses against human answers to identify documentation gaps, and automating parts of open source request evaluation.

- Specific examples included an AI agent running inside a Microsoft Teams channel to answer first-line documentation questions, and agents being used to address Release Hub management bottlenecks such as GitHub permissions, team creation, and assignments.

Other examples included tools that help automate the open source publishing process, including code review, intellectual property review, and security checks. Participants also discussed systems that provide AI tools with project-specific context, such as governance rules, conventions, and contribution expectations.

### AI Implementation in Open Source

Participants discussed the use of AI agents to support project reviews and contribution requests. While these tools were reported to improve productivity, several participants emphasized that many implementations remain experimental.

Three broad areas for AI implementation emerged from the discussion:

1. Automating OSPO work.
2. Providing AI tooling and processes for open source projects.
3. Addressing responsible open source publishing and contribution practices.

Participants also shared examples of developer-facing automation, such as checks that reduce review iterations and suggest pull requests when issues are found.

- The PyTorch community was mentioned as a specific environment where AI-enabled contribution policies are being explored

### AI Collaboration and Tool Development

The group emphasized the importance of focusing on common problems before jumping to specific solutions. Participants noted that sustained collaboration will be important to avoid repeating the challenges of previous tooling efforts.

A potential distinction emerged between AI usage for internal OSPO operations and AI usage for compliance or open source management workflows. Participants expressed interest in sharing reusable tools, patterns, and practices across organizations.

The group also discussed the value of community collaboration and validation when developing AI tools, especially in areas such as documentation, git commit messages, compliance checks, and contribution workflows

- External tooling communities were also mentioned, including the OSS-Based Compliance Tooling community: https://oss-compliance-tooling.org/

### Open Source AI Workflow Improvements

The working group discussed how agentic workflows could improve productivity for open source maintainers and how organizations might develop policies for AI-generated code contributions

Participants compared agentic and deterministic workflows, noting that deterministic approaches can be useful upfront to guide AI behavior, improve reproducibility, and control costs

### Final Remarks

The group agreed that the working group should focus on higher-level recommendations, shared patterns, and practical resources rather than detailed technical architectures. The draft charter will be refined based on feedback from the discussion and survey responses. 


## Next Steps

- [x] All working group members: Provide input and feedback on the draft charter in the group’s GitHub repository, either by opening a pull request or by opening an issue with thoughts or questions

- [ ] All working group members: Share tools, specs, or artifacts they are building or experimenting with by contributing to the relevant section in the awesome OSPO issue [Add AI workflows, prompts, and tools for OSPOs](https://github.com/todogroup/awesome-ospo/issues/75)

- [x] Working group coordinator: Summarize the meeting transcript, ensuring all names and affiliations are removed, and post the anonymized summary in the GitHub repository under meeting notes

- [x] Working group chairs: Review and synthesize feedback and new entries in the open issues and charter to help define group outcomes and collaboration points with other relevant working groups

- [x] Working group chairs: Prepare an outline for the next meeting

- [x] All working group members: Continue relevant discussions and share updates in the dedicated Slack channel

- [x] Working group coordinator: Set up a bi-weekly recurring meeting series for the working group

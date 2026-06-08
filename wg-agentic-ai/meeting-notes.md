## Instructions for Adding New Meeting Notes

When adding notes for a new meeting:

1. Add the meeting date to the list below using the format:

   ```markdown
   - [YYYY-MM-DD](#summary-month-day)

# Table of Contents:

- [2026-05-26](#summary-may-26)


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

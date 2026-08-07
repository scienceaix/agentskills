# Awesome Skills for LLMs [![Awesome](https://awesome.re/badge.svg)](https://arxiv.org/abs/2602.12430)

> A curated collection of resources, papers, tools, and frameworks for building, composing, and deploying **skills** for large language models — centered on Skills ecosystem and radiating outward to the broader LLM agent capabilities landscape.

**Agent Skills** was introduced as composable, portable folders of instructions, scripts, and resources that  loads dynamically — turning a general-purpose assistant into a specialized agent. This list tracks everything in the skills-for-LLMs ecosystem: the official Anthropic skill system, the closely related Model Context Protocol (MCP), academic research on skill acquisition and tool use, open-source agent frameworks, computer-use and GUI agents, benchmarks, and practical tutorials. 

---

## Contents

- [Awesome Skills for LLMs ](#awesome-skills-for-llms-)
  - [Contents](#contents)
  - [Anthropic Skills — Core Ecosystem](#anthropic-skills--core-ecosystem)
    - [Official Announcements \& Blog Posts](#official-announcements--blog-posts)
    - [Documentation \& Guides](#documentation--guides)
    - [GitHub Repositories](#github-repositories)
    - [Courses \& Webinars](#courses--webinars)
  - [Model Context Protocol (MCP)](#model-context-protocol-mcp)
    - [Specification \& Announcements](#specification--announcements)
    - [SDKs \& Official Repos](#sdks--official-repos)
    - [Community MCP Resources](#community-mcp-resources)
  - [Claude Tool Use \& Computer Use](#claude-tool-use--computer-use)
    - [Tool Use Resources](#tool-use-resources)
    - [Computer Use Resources](#computer-use-resources)
  - [Academic Papers](#academic-papers)
    - [Skill Learning \& Composition](#skill-learning--composition)
    - [Tool Use \& Function Calling](#tool-use--function-calling)
    - [Computer Use \& GUI Agents](#computer-use--gui-agents)
    - [Web Agents \& Browser Automation](#web-agents--browser-automation)
    - [GUI Grounding \& Visual Understanding](#gui-grounding--visual-understanding)
    - [OS Agents](#os-agents)
    - [Multi-Agent Collaboration](#multi-agent-collaboration)
    - [Surveys \& Overviews](#surveys--overviews)
  - [Open-Source Projects \& Frameworks](#open-source-projects--frameworks)
    - [Agent Frameworks](#agent-frameworks)
    - [Browser Automation \& Computer Use Agents](#browser-automation--computer-use-agents)
    - [Coding Agents](#coding-agents)
  - [Benchmarks \& Evaluation](#benchmarks--evaluation)
    - [Agent Benchmarks](#agent-benchmarks)
    - [Tool Use \& Function Calling Benchmarks](#tool-use--function-calling-benchmarks)
    - [Computer Use \& GUI Benchmarks](#computer-use--gui-benchmarks)
    - [Web Browsing Benchmarks](#web-browsing-benchmarks)
    - [Leaderboards \& Aggregators](#leaderboards--aggregators)
  - [Tutorials \& Educational Resources](#tutorials--educational-resources)
    - [Anthropic Official Tutorials](#anthropic-official-tutorials)
    - [Community Skills Guides](#community-skills-guides)
    - [MCP Tutorials](#mcp-tutorials)
    - [Agent Architecture Guides](#agent-architecture-guides)
    - [Tool Use \& Function Calling Tutorials](#tool-use--function-calling-tutorials)
    - [Courses](#courses)
  - [Related Awesome Lists](#related-awesome-lists)
  - [Key Timeline](#key-timeline)
  - [Contributing](#contributing)
  - [Citation](#citation)

---

## Anthropic Skills — Core Ecosystem

### Official Announcements & Blog Posts

- [Introducing Agent Skills](https://www.anthropic.com/news/skills) — Official product launch. Skills are folders of instructions, scripts, and resources that Claude loads dynamically. Available for Pro, Max, Team, and Enterprise users. Updated Dec 18, 2025 with organization-wide management and open standard announcement. *(Oct 2025, updated Dec 2025)*

- [Equipping Agents for the Real World with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) — Engineering deep-dive on the Agent Skills architecture: progressive disclosure, SKILL.md format, bundled code execution, and best practices. By Barry Zhang, Keith Lazuka, Mahesh Murag. *(Oct 2025, updated Dec 2025)*

- [Skills for Organizations, Partners, the Ecosystem](https://claude.com/blog/organization-skills-and-directory) — Announcement of org-wide skill management, partner-built skills directory, and Skills as an open standard for cross-platform portability. *(Dec 18, 2025)*

- [How to Create Skills: Key Steps, Limitations, and Examples](https://claude.com/blog/how-to-create-skills-key-steps-limitations-and-examples) — Practical guide to building Skills: defining name/description, structuring SKILL.md, writing instructions, testing, and governance best practices for teams. *(Nov 2025)*

- [How AI Impacts Skill Formation](https://www.anthropic.com/research/AI-assistance-coding-skills) — RCT finding that AI assistance led to 17% lower mastery scores, exploring the tension between productivity and skill development. *(Jan 2026)*

### Documentation & Guides

- [The Complete Guide to Building Skills for Claude (PDF)](https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf?hsLang=en) — Comprehensive PDF covering SKILL.md authoring, frontmatter metadata, progressive disclosure patterns, organization-level deployment, API usage, and MCP integration with partner examples (Sentry, Box, Notion, Canva). *(2025)*

- [2026 Agentic Coding Trends Report (PDF)](https://resources.anthropic.com/hubfs/2026%20Agentic%20Coding%20Trends%20Report.pdf?hsLang=en) — Report on how agentic AI reshapes SDLC, developer roles, and security, covering Claude Code, Skills, and the MCP ecosystem. *(Early 2026)*

- [Build with Claude — Learning Hub](https://www.anthropic.com/learn/build-with-claude) — Hub page linking to Skills docs, best practices, API usage, Claude Code usage, and MCP integration.

### GitHub Repositories

- [anthropics/skills](https://github.com/anthropics/skills) — Public repository for Agent Skills: official skill definitions, examples, and the marketplace. ⭐ **62k+**

- [anthropics/claude-code](https://github.com/anthropics/claude-code) — Agentic coding tool for terminal. Supports Skills, MCP, subagents, slash commands, and hooks. ⭐ **42k+**

- [anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks) — Recipes and notebooks including agent patterns, tool use examples, and reference implementations. ⭐ **28k+**

- [anthropics/courses](https://github.com/anthropics/courses) — Anthropic's educational courses including tool use tutorials. ⭐ **18k+**

- [anthropics/prompt-eng-interactive-tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial) — Interactive prompt engineering tutorial. ⭐ **26k+**

- [anthropics/claude-quickstarts](https://github.com/anthropics/claude-quickstarts) — Quickstart projects including the computer-use-demo Docker container. ⭐ **10k+**

- [anthropics/claude-agent-sdk-typescript](https://github.com/anthropics/claude-agent-sdk-typescript) — TypeScript Claude Agent SDK for building custom agents with MCP integration.

- [anthropics/anthropic-sdk-python](https://github.com/anthropics/anthropic-sdk-python) — Official Python SDK for the Anthropic API.

### Courses & Webinars

- [Agent Skills Webinar: Transform Claude from Assistant to Specialized Agent](https://www.anthropic.com/webinars/agent-skills-transform-claude-from-assistant-to-specialized-agent) — Technical webinar by Marius Buleandra (Anthropic Applied AI) covering Skills architecture, live demos, and best practices. *(Nov 2025)*

- [Agent Skills with Anthropic — DeepLearning.AI](https://learn.deeplearning.ai/courses/agent-skills-with-anthropic/lesson/eg4sac/why-use-skills---part-ii) — DeepLearning.AI course on Agent Skills covering the open standard, composability, and cross-platform usage.

- [Introduction to Model Context Protocol — Anthropic Academy](https://anthropic.skilljar.com/introduction-to-model-context-protocol) — Official Anthropic course on building MCP servers and clients using Python.

- [Claude Code in Action — Anthropic Academy](https://anthropic.skilljar.com/claude-code-in-action) — Free official course for integrating Claude Code into development workflows.

---

## Model Context Protocol (MCP)

### Specification & Announcements

- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol) — Original MCP launch. Open standard for connecting AI to data sources. Pre-built servers for Google Drive, Slack, GitHub, Postgres, Puppeteer. Early adopters: Block, Apollo, Zed, Replit, Sourcegraph. *(Nov 2024)*

- [Donating MCP and Establishing the Agentic AI Foundation](https://www.anthropic.com/news/donating-the-model-context-protocol-and-establishing-of-the-agentic-ai-foundation) — MCP donated to Linux Foundation's AAIF, co-founded with Block and OpenAI. **10,000+ active MCP servers**, adopted by ChatGPT, Cursor, Gemini, VS Code. 97M+ monthly SDK downloads. *(Dec 9, 2025)*

- [MCP Specification (2025-11-25)](https://modelcontextprotocol.io/specification/2025-11-25) — Latest MCP spec: JSON-RPC 2.0, tools/resources/prompts, security guidelines, async operations, statelessness, server identity.

- [One Year of MCP — November 2025 Spec Release](http://blog.modelcontextprotocol.io/posts/2025-11-25-first-mcp-anniversary/) — Anniversary blog detailing 2025-11-25 spec features: tasks, async operations, governance updates.

- [MCP Joins the Agentic AI Foundation](http://blog.modelcontextprotocol.io/posts/2025-12-09-mcp-joins-agentic-ai-foundation/) — Blog post about MCP's donation to Linux Foundation's AAIF.

- [Code Execution with MCP](https://www.anthropic.com/engineering/code-execution-with-mcp) — How to use code execution to interact with MCP servers more efficiently, reducing token overhead from tool definitions. *(Nov 4, 2025)*

### SDKs & Official Repos

- [modelcontextprotocol/modelcontextprotocol](https://github.com/modelcontextprotocol/modelcontextprotocol) — Main specification and documentation repo. Schema in TypeScript, available as JSON Schema.

- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) — Official and community MCP server implementations: GitHub, GitLab, Google Drive, Google Maps, PostgreSQL, Puppeteer, Redis, Sentry, Slack, SQLite, and hundreds more.

- [modelcontextprotocol/python-sdk](https://github.com/modelcontextprotocol/python-sdk) — Official Python SDK for building MCP servers and clients.

- [modelcontextprotocol/typescript-sdk](https://github.com/modelcontextprotocol/typescript-sdk) — Official TypeScript SDK. v2 with Streamable HTTP, Express/Hono integrations.

- [modelcontextprotocol/go-sdk](https://github.com/modelcontextprotocol/go-sdk) — Official Go SDK, maintained in collaboration with Google.

- [modelcontextprotocol/csharp-sdk](https://github.com/modelcontextprotocol/csharp-sdk) — Official C#/.NET SDK, maintained in collaboration with Microsoft.

- [modelcontextprotocol/kotlin-sdk](https://github.com/modelcontextprotocol/kotlin-sdk) — Official Kotlin SDK, maintained in collaboration with JetBrains.

- [modelcontextprotocol/registry](https://github.com/modelcontextprotocol/registry) — Community-driven registry service for discovering MCP servers. Launched preview Sep 2025.

- [modelcontextprotocol/ext-apps](https://github.com/modelcontextprotocol/ext-apps) — MCP Apps Extension — standard for interactive UIs embedded in AI chatbots via MCP servers. Supports React, Vue, Svelte, Solid, Preact.

- [modelcontextprotocol/use-mcp](https://github.com/modelcontextprotocol/use-mcp) — Lightweight React hook for connecting to MCP servers.

### Community MCP Resources

- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) — Comprehensive curated collection of MCP servers: production-ready and experimental, covering file access, databases, API integrations, and more. ⭐ **15k+**

- [wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers) — Curated list of MCP servers with official integrations, reference servers, and community servers by category. ⭐ **10k+**

- [microsoft/mcp](https://github.com/microsoft/mcp) — Catalog of official Microsoft MCP server implementations including Azure services, DevOps, M365 Agents Toolkit, Fabric, and Sentinel.

---

## Claude Tool Use & Computer Use

### Tool Use Resources

- [Introducing Advanced Tool Use on the Claude Developer Platform](https://www.anthropic.com/engineering/advanced-tool-use) — Three beta features: **Tool Search Tool**, **Programmatic Tool Calling**, and **Tool Learning**. 85% token reduction; Opus 4.5 improved from 79.5% to 88.1% accuracy. *(Nov 24, 2025)*

- [Writing Effective Tools for Agents — With Agents](https://www.anthropic.com/engineering/writing-tools-for-agents) — Best practices for designing MCP tools and agent tools: ergonomic design, namespacing, evaluation-driven improvement, using Claude to optimize its own tools. *(2025)*

- [Building Agents with the Claude Agent SDK](https://www.anthropic.com/engineering/building-agents-with-the-claude-agent-sdk) — Claude Agent SDK (renamed from Claude Code SDK): tools as primary building blocks, MCP integration, bash tool, code generation patterns. *(Sep 29, 2025)*

- [Building Effective AI Agents](https://www.anthropic.com/research/building-effective-agents) — Foundational guide on agentic system patterns: prompt chaining, routing, parallelization, orchestrator-workers. Distinguishes workflows vs agents. *(Dec 2024)*

- [Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) — Guide to building evaluations for agents including coding agents, research agents, and computer use agents. *(2025)*

- [Tool Use with Claude — Overview](https://platform.claude.com/docs/en/agents-and-tools/tool-use/overview) — Main documentation hub: client tools, server tools (web search, text editor, code execution, computer use), structured outputs, MCP integration.

- [How to Implement Tool Use](https://platform.claude.com/docs/en/agents-and-tools/tool-use/implement-tool-use) — Step-by-step implementation guide covering tool definitions, tool_use responses, tool_result handling, parallel tool calls, and token-efficient tools.

- [Programmatic Tool Calling](https://platform.claude.com/docs/en/agents-and-tools/tool-use/programmatic-tool-calling) — Documentation for the `advanced-tool-use-2025-11-20` beta: Claude executes tools programmatically via code execution.

### Computer Use Resources

- [Developing a Computer Use Model](https://www.anthropic.com/news/developing-computer-use) — Research insights on training Claude for computer use: generalization from simple software, safety considerations, and RSP assessment. *(Aug 2025)*

- [Monitoring Computer Use via Hierarchical Summarization](https://alignment.anthropic.com/2025/summarization-for-monitoring/) — Safety research on monitoring Computer Use API activity using hierarchical summarization to detect harmful behaviors at scale. *(2025)*

- [Computer Use Tool Documentation](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use) — Official API docs for computer use: `computer_20251124` (Opus 4.5/4.6), `computer_20250124` (Sonnet 4.5), screenshot capture, mouse/keyboard control.

- [API Release Notes](https://docs.anthropic.com/en/release-notes/api) — Changelog documenting `computer_20250124` tool version (Jan 2025), `bash_20250124`, `text_editor_20250124`, token-efficient tool use.

---

## Academic Papers

### Skill Learning & Composition

- [SAGE: Reinforcement Learning for Self-Improving Agent with Skill Library](https://arxiv.org/abs/2512.17102) — Jiongxiao Wang et al. Proposes SAGE (Skill Augmented GRPO for self-Evolution), an RL framework that systematically incorporates a skill library into agent training. Achieves 8.9% higher task completion while requiring 26% fewer steps and 59% fewer tokens on AppWorld. *(Dec 2025)*

- [CUA-Skill: Develop Skills for Computer Using Agent](https://arxiv.org/abs/2601.21123) — Tianyi Chen et al. (Microsoft). Skill-centric framework encoding human computer-use knowledge as reusable, parameterized skills with execution and composition graphs. CUA-Skill Agent achieves **SOTA 57.5% success rate on WindowsAgentArena**. *(Jan 2026)*

- [Agentic Proposing: Enhancing LLM Reasoning via Compositional Skill Synthesis](https://arxiv.org/abs/2602.03279) — Zhengbo Jiao et al. Models problem synthesis as a goal-driven process with a specialized agent that dynamically selects and composes modular reasoning skills from a skill library. A 30B solver achieves 91.6% on AIME 2025. *(Feb 2026)*

- [When Single-Agent with Skills Replace Multi-Agent Systems and When They Fail](https://arxiv.org/abs/2601.04748) — Xiaoxiao Li. Investigates "compiling" multi-agent systems into single-agent skill libraries, finding substantial reductions in token usage and latency while maintaining accuracy. Discovers a **phase transition in skill selection accuracy** at a critical library size. *(Jan 2026)*

- [Self-Distillation Enables Continual Learning](https://arxiv.org/abs/2601.19897) — Idan Shenfeld, Mehul Damani et al. Studies whether pretrained LLMs can acquire new, narrowly defined skills (science Q&A, tool use, medical reasoning) without degrading existing abilities, using self-distillation. *(Jan 2026)*
- [OpenSkill: Open-World Self-Evolution for LLM Agents](https://arxiv.org/abs/2606.06741) — Zhiling Yan et al. Open-world self-evolution framework where an agent given only a task prompt acquires grounded knowledge and verification anchors from documentation, repositories, and the web, synthesizes them into transferable skills, and refines them against self-built virtual tasks without target-task supervision; skills and the self-built verifier transfer across models. *(Jun 2026)*

### Tool Use & Function Calling

- [Tool Learning with Large Language Models: A Survey](https://arxiv.org/abs/2405.17935) — Changle Qu et al. Comprehensive survey organizing tool learning into four key stages: task planning, tool selection, tool calling, and response generation. Published in *Frontiers of Computer Science*, Vol. 19(8), 2025.

- [ReTool: Reinforcement Learning for Strategic Tool Use in LLMs](https://arxiv.org/abs/2504.11536) — Jiazhan Feng et al. Tool-augmented RL framework interleaving real-time code execution within natural language reasoning. Achieves **67% accuracy on AIME2024** with 400 training steps. Demonstrates emergent "aha moment" behaviors in tool use. *(Apr 2025)*

- [FunReason: Enhancing LLMs' Function Calling via Self-Refinement Multiscale Loss](https://arxiv.org/abs/2505.20192) — Bingguang Hao et al. Novel framework combining automated data refinement with Self-Refinement Multiscale Loss (SRML), achieving performance comparable to GPT-4o while mitigating catastrophic forgetting. *(May 2025)*

- [Improving LLM Function Calling via Guided-Structured Templates](https://arxiv.org/abs/2509.18076) — Hy Dang et al. Curriculum-inspired framework using structured reasoning templates for function calling, achieving 3-12% relative improvements over strong baselines. Shows free-form CoT is insufficient for structured function calling. *(EMNLP 2025)*

- [LLMOrch: Efficient Function Orchestration for Large Language Models](https://arxiv.org/abs/2504.14872) — Xiaoxia Liu et al. Automated, parallel function calling by modeling data relations (def-use) among function calls. Achieves **2× speedup** over SOTA techniques. *(Apr 2025)*

- [Function Calling in LLMs: Industrial Practices, Challenges, and Future Directions](https://dl.acm.org/doi/10.1145/3788284) — Comprehensive ACM survey covering industrial practices in LLM function calling, including training approaches, evaluation frameworks, and future directions. *ACM Computing Surveys, 2025.*

### Computer Use & GUI Agents

- [UI-TARS: Pioneering Automated GUI Interaction with Native Agents](https://arxiv.org/abs/2501.12326) — Yujia Qin et al. (ByteDance/Tsinghua). End-to-end native GUI agent achieving **SOTA on 10+ GUI benchmarks** (OSWorld 24.6, AndroidWorld 46.6) through enhanced perception, unified action modeling, and System-2 reasoning. *(Jan 2025)*

- [UI-TARS-2: Advancing GUI Agent with Multi-Turn Reinforcement Learning](https://arxiv.org/abs/2509.02544) — Haoming Wang et al. (ByteDance). Data flywheel for scalable generation, stabilized multi-turn RL, hybrid GUI+terminal environment. Achieves **47.5 on OSWorld**, 88.2 on Online-Mind2Web, 73.3 on AndroidWorld. *(Sep 2025)*

- [Agent S2: A Compositional Generalist-Specialist Framework for Computer Use](https://arxiv.org/abs/2504.00906) — Saaket Agashe et al. (UC Santa Cruz). Compositional framework with Mixture-of-Grounding for precise GUI localization. Achieves 18.9% and 32.7% relative improvements over Claude Computer Use and UI-TARS on OSWorld. *(Apr 2025)*

- [OpenCUA: Open Foundations for Computer-Use Agents](https://arxiv.org/abs/2508.09123) — Xinyuan Wang et al. (XLANG Lab/HKU). Comprehensive open-source framework with AgentNet (first large-scale CUA dataset spanning 3 OSes, 200+ apps). OpenCUA-72B achieves **45.0% on OSWorld-Verified** (SOTA among open-source). *(NeurIPS 2025 Spotlight)*

- [ShowUI: One Vision-Language-Action Model for GUI Visual Agent](https://arxiv.org/abs/2411.17465) — Kevin Qinghong Lin et al. Lightweight 2B vision-language-action model achieving 75.1% accuracy in zero-shot screenshot grounding with only 256K training data. *(CVPR 2025)*

- [ShowUI-Aloha: Human-Taught GUI Agent](https://arxiv.org/html/2601.07181) — Yichun Zhang et al. Human-taught desktop agent via a record-parse-learn paradigm. Transforms raw interactions into semantically grounded teaching trajectories. *(Jan 2026)*

- [AFRAgent: Adaptive Feature Renormalization Based GUI Agent](https://arxiv.org/abs/2512.00846) — Neeraj Anand et al. Less than one-fourth the size of nearest competitor while achieving SOTA on Meta-GUI and AITW benchmarks. *(Nov 2025)*

### Web Agents & Browser Automation

- [The BrowserGym Ecosystem for Web Agent Research](https://arxiv.org/abs/2412.05467) — Thibault Le Sellier De Chezelles et al. (ServiceNow/CMU/McGill). Unified gym-like environment for standardized web agent evaluation. First large-scale, multi-benchmark experiment comparing 6 LLMs across 6 benchmarks. *(TMLR Feb 2025)*

- [BrowserAgent: Web Agents with Human-Inspired Browsing Actions](https://arxiv.org/html/2510.10666v1) — ReAct-style reasoning framework with explicit memory for multi-turn web interactions. With only 5.3K training samples, outperforms Search-R1 on Open-QA tasks. *(Oct 2025)*

- [Evaluating Long-Context Reasoning in LLM-Based WebAgents](https://arxiv.org/abs/2512.04307) — Andy Chung et al. Benchmark for long-context reasoning in WebAgents. Finds **dramatic performance degradation (40-50% → <10%)** as context length increases. *(Dec 2025)*

- [Building Browser Agents: Architecture, Security, and Practical Solutions](https://arxiv.org/html/2511.19477v1) — Examines production-grade browser agent architecture, covering context management, safety boundaries, and the choice between generalization and specialization. *(Nov 2025)*

### GUI Grounding & Visual Understanding

- [UGround: Universal Visual Grounding for GUI Agents](https://arxiv.org/abs/2410.05243) — Boyu Gou et al. (OSU NLP). Trains on **10M GUI elements from 1.3M screenshots** — the largest GUI visual grounding dataset. Outperforms existing models by up to 20% absolute. *(ICLR 2025 Oral)*

- [Enhancing Visual Grounding for GUI Agents via Self-Evolutionary RL](https://arxiv.org/abs/2505.12370) — Xinbin Yuan et al. RL-based framework where a 7B model achieves **47.3% on ScreenSpot-Pro**, outperforming UI-TARS-72B by 24.2% with only 3K training samples. *(May 2025)*

- [Scaling Computer-Use Grounding via UI Decomposition and Synthesis (Jedi)](https://arxiv.org/abs/2505.13227) — Tianbao Xie et al. (XLANG Lab). OSWorld-G benchmark (564 samples) and Jedi dataset (4M grounding examples). Improves OSWorld agentic success from 5% to 27%. *(NeurIPS 2025 Spotlight)*

- [ScreenSpot-Pro: GUI Grounding for Professional High-Resolution Computer Use](https://arxiv.org/abs/2504.07981) — Kaixin Li et al. Benchmark spanning 23 applications across 5 industries and 3 OSes. Best models initially achieved only 18.9%. *(Apr 2025)*

- [UI-R1: Enhancing GUI Action Prediction by Reinforcement Learning](https://arxiv.org/abs/2503.21620) — Zhengxi Lu et al. First framework exploring rule-based RL (GRPO) for GUI action prediction. With only 136 training tasks, achieves significant improvements. *(Mar 2025)*

- [GUI-Eyes: Tool-Augmented Perception for Visual Grounding in GUI Agents](https://arxiv.org/html/2601.09770) — Novel framework enabling agents to autonomously decide when to invoke visual tools (cropping, zooming) during reasoning. GUI-Eyes-3B achieves 44.8% on ScreenSpot-Pro. *(Jan 2026)*

- [GUI-Actor: Coordinate-Free Visual Grounding for GUI Agents](https://arxiv.org/abs/2506.03143) — Qianhui Wu et al. (Microsoft). Attention-based action head for coordinate-free GUI grounding. GUI-Actor-7B surpasses UI-TARS-72B on ScreenSpot-Pro. *(Jun 2025)*

### OS Agents

- [OS Agents: A Survey on MLLM-based Agents for General Computing Devices](https://arxiv.org/abs/2508.04482) — Xueyu Hu et al. Comprehensive survey covering fundamentals, capabilities, construction methodologies, and evaluation protocols. *(ACL 2025)*

- [AIOS: LLM Agent Operating System](https://arxiv.org/abs/2403.16971) — Kai Mei et al. LLM agent OS with scheduling, context management, memory management, and access control. Achieves up to **2.1× faster execution**. *(COLM 2025)*

- [SchedCP: Towards Agentic OS with LLM Agent Framework for Linux Schedulers](https://arxiv.org/abs/2509.01245) — Yusheng Zheng et al. First framework enabling fully autonomous LLM agents to optimize Linux schedulers via MCP server. Achieves up to **1.79× performance improvement**. *(Sep 2025)*

### Multi-Agent Collaboration

- [Multi-Agent Collaboration Mechanisms: A Survey of LLMs](https://arxiv.org/abs/2501.06322) — Khanh-Tung Tran et al. Extensive survey characterizing collaboration by actors, types (cooperation/competition/coopetition), structures, strategies, and coordination protocols. *(Jan 2025)*

- [LLM Collaboration With Multi-Agent Reinforcement Learning](https://arxiv.org/abs/2508.04652) — Shuo Liu et al. Models LLM collaboration as cooperative Multi-Agent RL. Proposes MAGRPO, demonstrating effective cooperation in writing and coding tasks. *(Aug 2025)*

- [Lessons Learned: A Multi-Agent Framework for Code LLMs](https://arxiv.org/abs/2505.23946) — Yuanzhe Liu et al. Lesson-based collaboration where agents learn from each other's successes and failures. Small LLMs with shared lessons outperform much larger single LLMs. *(May 2025)*

- [AgentsNet: Coordination and Collaborative Reasoning in Multi-Agent LLMs](https://arxiv.org/abs/2507.08616) — ETH Zurich. Benchmark inspired by classical distributed systems (leader election, consensus), scaling up to 100 agents. *(Jul 2025)*

### Surveys & Overviews

- [Agent Skills for Large Language Models: Architecture, Acquisition, Security, and the Path Forward](https://arxiv.org/abs/2602.12430) - Renjun Xu et al. Unlike prior surveys that broadly cover LLM agents or tool use, this survey focuses specifically on the emerging skill abstraction layer and its implications for the next generation of agentic systems. *(Feb 2026)*

- [Large Language Model Agent: A Survey on Methodology, Applications and Challenges](https://arxiv.org/abs/2503.21460) — Junyu Luo et al. Systematically deconstructs LLM agent systems through methodology-centered taxonomy, linking architectural foundations, collaboration mechanisms, and evolutionary pathways. *(Mar 2025)*

- [Agentic Large Language Models: A Survey](https://arxiv.org/abs/2503.23037) — Aske Plaat et al. Comprehensive survey organizing agentic LLM research into three pillars: reasoning/reflection/retrieval, action models/robots/tools, and multi-agent systems. *(Mar 2025, revised Nov 2025)*

- [A Review of Prominent Paradigms for LLM-Based Agents: Tool Use, Planning, and Feedback Learning](https://aclanthology.org/2025.coling-main.652/) — Xinzhe Li. Reviews tool use, planning, and feedback learning paradigms. *(COLING 2025)*

- [Large Language Model-Brained GUI Agents: A Survey](https://arxiv.org/abs/2411.18279) — Chaoyun Zhang et al. (Microsoft Research). Covers agent frameworks, training data, large action models, and evaluation benchmarks across web, mobile, and desktop. *(Nov 2024, updated May 2025)*

- [Evaluation and Benchmarking of LLM Agents: A Survey](https://arxiv.org/abs/2507.21504) — Two-dimensional taxonomy for LLM agent evaluation: objectives (behavior, capabilities, reliability, safety) and process (interaction modes, benchmarks, metrics, tooling). *(KDD 2025)*

- [A Survey on Large Language Model Benchmarks](https://arxiv.org/abs/2508.15361) — Shiwen Ni et al. First systematic review of **283 representative LLM benchmarks**, categorized by general capabilities, domain-specific, and target-specific. *(Aug 2025)*

- [Mapping the Design Space of User Experience for Computer Use Agents](https://arxiv.org/html/2602.07283) — Investigates UX design for computer use agents: visibility, user control, agent representation, and interaction modalities. *(Feb 2026)*

---

## Open-Source Projects & Frameworks

### Agent Frameworks

| Project | Description | Stars |
|---------|-------------|-------|
| [LangGraph](https://github.com/langchain-ai/langgraph) | Graph-based framework for stateful, multi-actor LLM applications with cyclic workflows. Extends LangChain with coordination of multiple chains and agents. | ⭐ 80k+ |
| [Microsoft AutoGen](https://github.com/microsoft/autogen) | Event-driven multi-agent conversation framework with customizable agent behaviors and structured conversation flows. | ⭐ 40k+ |
| [CrewAI](https://github.com/crewAIInc/crewAI) | Orchestrates role-playing autonomous AI agents that collaborate to accomplish complex tasks with specific roles, goals, and tools. | ⭐ 43k+ |
| [Microsoft Semantic Kernel](https://github.com/microsoft/semantic-kernel) | Model-agnostic SDK for building and deploying AI agents and multi-agent systems with plugin ecosystems and MCP integration. | ⭐ 22k+ |
| [Agno (formerly Phidata)](https://github.com/agno-agi/phidata) | High-performance agent framework with multimodal support. Claims ~10,000× faster agent instantiation than LangGraph. | ⭐ 20k+ |
| [Mastra](https://github.com/mastra-ai/mastra) | TypeScript AI agent framework with assistants, RAG, and observability. Built-in tools library. | ⭐ 21k+ |
| [PydanticAI](https://github.com/pydantic/pydantic-ai) | Schema-driven, type-safe GenAI agent framework by the Pydantic team. Supports MCP/A2A, durable execution. | ⭐ 10k+ |
| [HuggingFace smolagents](https://github.com/huggingface/smolagents) | Minimalist, code-first agent library (~1,000 lines core). Code agents write actions as Python; Hub integration for sharing. | ⭐ 10k+ |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Lightweight Python framework for multi-agent workflows with tracing, guardrails, and handoffs. Provider-agnostic. | ⭐ 9k+ |
| [Google Agent Development Kit (ADK)](https://github.com/google/adk-python) | Open-source, code-first Python toolkit optimized for Gemini but model-agnostic. Supports A2A protocol. | ⭐ 5k+ |

### Browser Automation & Computer Use Agents

| Project | Description | Stars |
|---------|-------------|-------|
| [browser-use](https://github.com/browser-use/browser-use) | Makes websites accessible for AI agents with automated browser interaction. Multi-provider support (OpenAI, Google, Anthropic, Ollama). | ⭐ 50k+ |
| [Skyvern](https://github.com/Skyvern-AI/skyvern) | Browser-based workflow automation using LLMs and computer vision. SOTA on WebBench (64.4%). Multi-agent with planner + validator. | ⭐ 20k+ |
| [Stagehand (Browserbase)](https://github.com/browserbase/stagehand) | AI browser automation combining natural language and code with `act()`, `agent()`, and `extract()` APIs. Auto-caching with self-healing. | ⭐ 10k+ |
| [Steel Browser](https://github.com/steel-dev/steel-browser) | Open-source browser API for AI agents with full Puppeteer/Playwright/Selenium support, session management, and proxy support. | ⭐ 5k+ |
| [agent-browser (Vercel Labs)](https://github.com/vercel-labs/agent-browser) | Headless browser automation CLI for AI agents. Fast Rust CLI. Works with Claude Code, Cursor, Gemini CLI, and Codex. | ⭐ 3k+ |

### Coding Agents

| Project | Description | Stars |
|---------|-------------|-------|
| [OpenHands (formerly OpenDevin)](https://github.com/OpenHands/OpenHands) | Open platform for AI-driven development with SDK, CLI, GUI, and cloud deployment. SOTA on SWE-Bench Verified. | ⭐ 65k+ |
| [Aider](https://github.com/Aider-AI/aider) | AI pair programming in terminal. Maps entire codebase for context-aware multi-file edits. Works with Claude, GPT, DeepSeek. | ⭐ 40k+ |
| [SWE-agent](https://github.com/SWE-agent/SWE-agent) | Automatically fixes GitHub issues using your LM of choice. SWE-agent 1.0 + Claude 3.7 achieved SoTA on SWE-Bench. | ⭐ 10k+ |
| [mini-swe-agent](https://github.com/SWE-agent/mini-swe-agent) | 100-line AI agent scoring >74% on SWE-bench verified. Radically simple — no tools other than bash. | ⭐ 2k+ |

---

## Benchmarks & Evaluation

### Agent Benchmarks

- [SWE-bench & SWE-bench Verified](https://www.swebench.com/) — The premier benchmark for LLMs on real-world GitHub issue resolution. 500 human-validated tasks. Top model (Claude Opus 4.6 Thinking) reaches **79.2%** on Verified. ([GitHub](https://github.com/SWE-bench/SWE-bench))

- [SWE-bench-Live](https://github.com/microsoft/SWE-bench-Live) — Microsoft's live, monthly-updated variant adding 50 newly verified issues per month to prevent data contamination. Multi-language (C, C++, C#, Python, Java, Go, JS/TS, Rust). *(NeurIPS 2025)*

- [SWE-bench Pro](https://scale.com/leaderboard/swe_bench_pro_public) — Scale AI's harder variant using copyleft and proprietary codebases. Best models score only ~23% vs 70%+ on Verified.

- [GAIA: General AI Assistants](https://huggingface.co/datasets/gaia-benchmark/GAIA) — 466 real-world questions requiring reasoning, multi-modality, web browsing, and tool-use. Humans: 92%; GPT-4: 15%. ([Leaderboard](https://huggingface.co/spaces/gaia-benchmark/leaderboard))

- [TheAgentCompany](https://github.com/TheAgentCompany/TheAgentCompany) — CMU benchmark simulating a software engineering startup with 175 professional tasks across browsing, coding, terminal use, and communication. Best agent: ~24.4% full completion. *(NeurIPS 2025 D&B)*

- [AgentBench](https://github.com/THUDM/AgentBench) — Systematic benchmark evaluating LLMs as agents across 8 environments (OS, database, knowledge graph, card game, web shopping, web browsing). ([Paper](https://arxiv.org/abs/2308.03688))

- [DABstep: Data Agent Benchmark](https://huggingface.co/blog/dabstep) — By Adyen and Hugging Face, 450+ real-world data analysis tasks. Best reasoning agents achieve only **16% accuracy**. *(2025)*

### Tool Use & Function Calling Benchmarks

- [Berkeley Function Calling Leaderboard (BFCL) V4](https://gorilla.cs.berkeley.edu/leaderboard.html) — The de facto standard for evaluating LLM function-calling. Serial/parallel calls, multi-turn scenarios, hallucination detection, AST-based evaluation. ([Paper — ICML 2025](https://openreview.net/forum?id=2GmDdhBdDk))

- [τ-bench / τ²-bench](https://github.com/sierra-research/tau-bench) — Sierra Research benchmarks for Tool-Agent-User interaction. τ²-bench extends to dual-control environment with telecom domain. ([Leaderboard](https://taubench.com/), [τ² Paper](https://arxiv.org/abs/2506.07982))

- [ToolComp (Scale AI)](https://scale.com/leaderboard/tool_use_enterprise) — 485 meticulously crafted prompts evaluating compositional, dependent tool usage with human-verified answers. ~85% of prompts require 3+ tool calls.

- [IFEval-FC: Instruction-Following Evaluation in Function Calling](https://arxiv.org/abs/2509.18420) — 750 test cases assessing precise instruction following in function calling. No model surpassed 80% accuracy. *(Sep 2025)*

- [OSWorld-MCP](https://github.com/X-PLUG/OSWorld-MCP) — Benchmarks MCP tool invocation alongside GUI operation skills. 158 validated MCP tools, 250 tool-beneficial tasks. MCP tools boost o3 from 8.3% to 20.4%. *(Oct 2025)*

### Computer Use & GUI Benchmarks

- [OSWorld / OSWorld-Verified](https://os-world.github.io/) — First real-computer-environment benchmark for multimodal agents across Ubuntu, Windows, macOS. Human: 72.36%; first agent surpassed this at **72.6%** in Dec 2025. ([GitHub](https://github.com/xlang-ai/OSWorld), [Verified Blog](https://xlang.ai/blog/osworld-verified))

- [ScreenSpot-Pro](https://arxiv.org/abs/2504.07981) — GUI grounding in professional high-resolution settings. 23 applications, 5 industries, 3 OSes. Expert annotations. *(Apr 2025)*

- [AndroidWorld](https://www.emergentmind.com/topics/androidworld) — Dynamic benchmarking for autonomous mobile GUI agents on real Android systems. 116 core tasks across 20 apps. Leading agents: 60-80%.

- [GUI-World](https://gui-world.github.io) — Video benchmark evaluating multimodal LLMs on dynamic GUI understanding across 6 scenarios. *(ICLR 2025 Poster)* ([OpenReview](https://openreview.net/forum?id=QarKTT5brZ))

- [OSUniverse](https://arxiv.org/pdf/2505.03570) — Benchmark for multimodal desktop agents focusing on realistic office worker skills. Humans: 72.36%; leading models: ~42.9%. *(May 2025)*

### Web Browsing Benchmarks

- [WebArena](https://webarena.dev/) — Self-hosted web environment for autonomous agents with 812 tasks across e-commerce, forums, code dev, CMS. Execution-based evaluation. *(ICLR 2024)* ([GitHub](https://github.com/web-arena-x/webarena))

- [VisualWebArena](https://jykoh.com/vwa) — 910 visually grounded web tasks requiring multimodal comprehension across Classifieds, Shopping, and Reddit environments. *(ACL 2024)* ([GitHub](https://github.com/web-arena-x/visualwebarena))

- [BrowseComp](https://openai.com/index/browsecomp/) — OpenAI's 1,266 challenging questions requiring persistent, creative web navigation. Deep Research: ~51.5% vs <10% for non-agentic models. ([Paper](https://arxiv.org/abs/2504.12516)) *(Apr 2025)*

- [BrowseComp-Plus](https://github.com/texttron/BrowseComp-Plus) — Fair evaluation for Deep-Research agents using fixed curated corpus of ~100K human-verified documents. ([Paper](https://arxiv.org/abs/2508.06600)) *(Aug 2025)*

- [Mind2Web / Online-Mind2Web](https://openreview.net/forum?id=kiYqbO3wqw) — 2,350 tasks across 137 real websites. Online-Mind2Web extends with WebJudge auto-evaluation reaching ~85% agreement with human judgment.

### Leaderboards & Aggregators

- [LLM-Stats Benchmark Tracker](https://llm-stats.com/benchmarks/category/tool_calling) — Aggregates model performance across tool calling and agent benchmarks.

- [Vellum LLM Leaderboard](https://www.vellum.ai/llm-leaderboard) — Compares capabilities, price, and context window for leading LLMs.

- [SWE-rebench](https://swe-rebench.com) — Independent SWE-bench evaluation with standardized scaffolding and monthly updates.

- [HuggingFace Open LLM Leaderboard](https://huggingface.co/open-llm-leaderboard) — Primary hub for evaluating open LLMs.

- [Galileo Agent Leaderboard](https://huggingface.co/blog/pratikbhavsar/agent-leaderboard) — Evaluates agent tool selection quality across BFCL, τ-bench, xLAM, and ToolACE datasets. *(Feb 2025)*

- [Epoch AI SWE-bench Dashboard](https://epoch.ai/benchmarks/swe-bench-verified) — Tracks 60+ models on SWE-bench Verified with historical trends.

---

## Tutorials & Educational Resources

### Anthropic Official Tutorials

- [Building Effective AI Agents](https://www.anthropic.com/research/building-effective-agents) — Foundational guide on agentic patterns: prompt chaining, routing, parallelization, orchestrator-workers. The canonical reference for agent architectures. *(Dec 2024)*

- [Tool Use with Claude — Documentation](https://docs.anthropic.com/en/docs/agents-and-tools/tool-use/overview) — Complete official docs for Claude's tool use API: client tools, server tools, MCP integration, parallel calls, and pricing.

- [Computer Use — Documentation](https://docs.anthropic.com/en/docs/build-with-claude/computer-use) — Official docs for Computer Use: screenshot analysis, mouse/keyboard control, bash and text editor tools, agent loop implementation, and Docker reference.

- [Anthropic Cookbook — Agent Patterns](https://github.com/anthropics/anthropic-cookbook/tree/main/patterns/agents) — Reference implementations of common agent workflow patterns from the "Building Effective Agents" post.

- [Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) — Practical guide to building evaluations for coding agents, research agents, and computer use agents.

### Community Skills Guides

- [Claude Skills are awesome, maybe a bigger deal than MCP](https://simonwillison.net/2025/Oct/16/claude-skills/) — Simon Willison's influential analysis of Claude Skills: Markdown + YAML design, cross-model compatibility, and why skills may be bigger than MCP. *(Oct 16, 2025)*

- [Claude Skills: Custom Modules That Extend Claude — DataCamp](https://www.datacamp.com/tutorial/claude-skills) — Hands-on tutorial building an "Auto-Invoice Generator" skill. Covers SKILL.md creation, asset uploading, data preprocessing, and API usage. *(Nov 2025)*

- [How to Create Claude Code Skills: The Complete Guide](https://websearchapi.ai/blog/how-to-create-claude-code-skills) — Comprehensive guide covering SKILL.md architecture, progressive disclosure patterns, bundled resources, and production deployment strategies.

- [Claude Skills Explained — Lenny's Newsletter](https://www.lennysnewsletter.com/p/claude-skills-explained) — Claire Vo's product-manager perspective on Skills: building from scratch, practical uses for PRDs, changelogs, and follow-up emails. *(Oct 22, 2025)*

- [awesome-llm-skills](https://github.com/Prat011/awesome-llm-skills) — Community curated list of LLM and AI Agent Skills, resources, and tools for customizing AI workflows across Claude Code, Codex, Gemini CLI, and other platforms.

### MCP Tutorials

- [Build an MCP Server — Official Guide](https://modelcontextprotocol.io/docs/develop/build-server) — Official quickstart tutorial: building a weather server with `get_alerts` and `get_forecast` tools, connecting to Claude for Desktop.

- [How to Build Your Own MCP Server — Builder.io](https://www.builder.io/blog/mcp-server) — Detailed tutorial with CSS tutor example covering Tools, Resources, and Prompts concepts in TypeScript.

- [How to Build an MCP Server — IBM](https://www.ibm.com/think/tutorials/how-to-build-an-mcp-server) — Step-by-step Python MCP server using FastMCP for searching IBM tutorials.

- [Build Your MCP Server — OpenAI](https://developers.openai.com/apps-sdk/build/mcp-server/) — OpenAI's guide to MCP servers for ChatGPT Apps: tool definition, UI templates, and the MCP Apps bridge.

- [Building Your First MCP Server: A Beginner's Tutorial](https://dev.to/debs_obrien/building-your-first-mcp-server-a-beginners-tutorial-5fag) — Beginner-friendly tutorial creating a weather MCP server in TypeScript connecting to GitHub Copilot. *(Jul 2025)*

### Agent Architecture Guides

- [OpenAI — A Practical Guide to Building Agents (PDF)](https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf) — When to use agents, choosing models, designing tools, orchestration patterns (single → manager → decentralized), guardrails.

- [OpenAI — Building Agents Learning Track](https://developers.openai.com/tracks/building-agents/) — Official 1-3 hour course: model selection, tools (function calling, built-in tools, MCP), orchestration patterns, guardrails, and multi-agent systems.

- [OpenAI Cookbook — Agents Topic](https://cookbook.openai.com/topic/agents) — Notebooks covering context engineering, long-term memory, multi-agent portfolio analysis, MCP evaluation, and deep research.

- [Building Effective Agents with Spring AI](https://spring.io/blog/2025/01/21/spring-ai-agentic-patterns/) — Implements Anthropic's agent patterns using Spring AI in Java: prompt chaining, routing, parallelisation, orchestrator-workers. *(Jan 2025)*

- [Building Effective Agents with smolagents — HuggingFace](https://huggingface.co/blog/Sri-Vigneshwar-DJ/building-effective-agents-with-anthropics-best-pra) — Implements Anthropic's agent patterns using HuggingFace's smolagents library.

- [Anthropic Computer Use: Automate Your Desktop — DataCamp](https://www.datacamp.com/blog/what-is-anthropic-computer-use) — Practical guide to Claude's Computer Use: Docker setup, writing automation prompts, the three Anthropic-defined tools, pricing.

### Tool Use & Function Calling Tutorials

- [Function Calling with LLMs — Prompt Engineering Guide](https://www.promptingguide.ai/applications/function_calling) — Comprehensive tutorial on the three-step function calling pattern with OpenAI API examples. *(DAIR.AI)*

- [An Introduction to Function Calling and Tool Use — Apideck](https://www.apideck.com/blog/llm-tool-use-and-function-calling) — Step-by-step breakdown including hands-on example using Ollama + Llama 3.2 for local tool calling.

### Courses

- [Agentic AI — DeepLearning.AI](https://www.deeplearning.ai/courses/agentic-ai/) — Andrew Ng's flagship course covering four agentic design patterns: Reflection, Tool Use, Planning, and Multi-Agent collaboration. Vendor-neutral, built with raw Python. *(Oct 2025)*

- [AI Agents in LangGraph — DeepLearning.AI](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) — Building controllable agents with LangGraph, including agentic search integration. *(Harrison Chase & Rotem Weiss)*

- [HuggingFace Evaluation Guidebook](https://huggingface.co/spaces/OpenEvals/evaluation-guidebook) — Comprehensive evaluation resource covering 2025 evaluations for useful models, including agentic benchmarks analysis.

---

## Related Awesome Lists

- [awesome-llm-agents](https://github.com/kaushikb11/awesome-llm-agents) — Curated list of LLM agent frameworks with star counts and categorization. Updated Feb 2026.

- [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) — Collection of LLM apps built with RAG, AI Agents, Multi-agent Teams, MCP, and Voice Agents.

- [awesome-ai-agents (e2b-dev)](https://github.com/e2b-dev/awesome-ai-agents) — Comprehensive list of AI autonomous agents organized by coding, research, data, multi-agent.

- [awesome_ai_agents (jim-schwoebel)](https://github.com/jim-schwoebel/awesome_ai_agents) — Massive list of 1,500+ AI agent resources and tools.

- [awesome-web-agents (Steel)](https://github.com/steel-dev/awesome-web-agents) — Tools, frameworks, and resources for building AI web agents.

- [LLM-Agent-Benchmark-List](https://github.com/zhangxjohn/LLM-Agent-Benchmark-List) — Community-curated list of 100+ LLM agent benchmarks.

- [awesome LLM eval benchmark](https://github.com/VyetGokyra/awaresome_LLM_eval_benchmark) — Collection of 250+ LLM benchmarks and evaluation datasets.

- [OSU-NLP GUI Agents Paper List](https://github.com/OSU-NLP-Group/GUI-Agents-Paper-List/blob/main/paper_by_key/paper_benchmark.md) — Comprehensive, actively maintained list of GUI agent benchmark papers.

---

## Key Timeline

| Date | Milestone |
|------|-----------|
| **Nov 2024** | MCP launched as open standard; Claude Computer Use enters public beta |
| **Dec 2024** | "Building Effective Agents" foundational guide published |
| **Jan 2025** | Updated computer use tools (`computer_20250124`); token-efficient tool use |
| **Mar 2025** | OpenAI adopts MCP; OpenAI Agents SDK released |
| **Sep 2025** | Claude Agent SDK announced; MCP Registry preview launch |
| **Oct 2025** | **Agent Skills launched** for Claude apps, Claude Code, and API |
| **Nov 2025** | MCP spec 2025-11-25; Advanced Tool Use features; Opus 4.5 launch |
| **Dec 2025** | Skills published as open standard; MCP donated to Agentic AI Foundation (Linux Foundation) |
| **Jan–Feb 2026** | Skills repo reaches 62k+ stars; ongoing ecosystem expansion |

---

## TODO

---

## Contributing

Contributions welcome! Please read the contribution guidelines first. All submitted links must be verified and genuinely related to Skills for LLMs.

---

## Citation
```python

@misc{xu2026agentskillslargelanguage,
      title={Agent Skills for Large Language Models: Architecture, Acquisition, Security, and the Path Forward}, 
      author={Renjun Xu and Yang Yan},
      year={2026},
      eprint={2602.12430},
      archivePrefix={arXiv},
      primaryClass={cs.MA},
      url={https://arxiv.org/abs/2602.12430}, 
}
```


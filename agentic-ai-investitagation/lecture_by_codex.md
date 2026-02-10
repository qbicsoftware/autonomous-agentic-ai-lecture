# Autonomous Agentic AI in Core Facilities: Concepts and Security (10 minutes)

## 1) Opening context: why this matters for your work
You handle GDPR Article 9 data on local machines and Article 6 communications, often on self-managed laptops with limited IT oversight. That combination makes agentic AI both attractive and risky. The goal is awareness without panic: understand how these systems behave, where data can leak, and what safe use looks like. ⚠️

Further topics/keywords: GDPR Article 6/9, shadow IT, risk awareness, data stewardship

## 2) What are autonomous agentic AI systems?
Autonomous agentic AI systems are software systems that can **plan, execute, and iterate** toward a goal with minimal human input. They use LLMs for reasoning and then call tools (files, APIs, messaging plugins) to act in the real world. An **orchestrator** coordinates the loop, deciding which tools to call and when to stop. The core behavior is a loop you can visualize as: **observe** (gather signals) → **decide** (choose a next step) → **act** (use a tool) → **evaluate** (check results and adjust). 🤖

Memory gives the agent short-term context (current task state) and, when enabled, longer-term knowledge of prior steps or preferences. This helps it avoid repeating actions, track multi-step goals, and tailor responses, but it also expands what data might be stored or reused. 🧠

Further topics/keywords: agent loop, tool calling, planning, autonomy, execution environment

## 3) How agents differ from chat prompts, RPA, and RAG
- **Chat prompts**: dialogue and answers; no actions unless you trigger them. Example: “Summarize this paper section into 5 bullet points.” ✅
- **RPA (Robotic Process Automation)**: rigid scripts for known workflows; limited to predefined steps. Example: “Every night, download sequencing reports and copy them into a shared folder.” 🧩
- **RAG (Retrieval-Augmented Generation)**: retrieves data to improve answers; still usually answer-only. Example: “Answer a question about our SOPs by pulling the latest policy document.” 📚
- **Agents**: combine reasoning + tools + memory + planning to take actions. Example: “Check QC metrics, flag outliers, and draft an email summary to the PI.” 🚀

Take-home difference: agents bridge cognition and execution, so their security surface is wider. 🧠➡️🛠️

Further topics/keywords: RPA vs agents, RAG pipelines, tool augmentation, decision vs action

## 4) Common attacks against autonomous agents
- **Prompt injection**: malicious instructions hidden in data or messages. 🎯
- **Exfiltration**: agent is tricked into uploading sensitive files or metadata. 📤
- **Plugin abuse**: integrations (Slack/Teams/WhatsApp) become data channels. 🔌
- **Supply-chain risks**: third-party tools may log or reuse data. 🧪
- **Goal hijacking**: agent’s objective is quietly redirected. 🧭

Further topics/keywords: prompt injection, exfiltration, plugin risk, supply-chain security

## 5) How users can protect their environment
- **Assume any pasted data can leave the device** unless confirmed local. 🔒
- **Separate sensitive data zones** from experimentation tools. 🧬
- **Use least-privilege accounts** for agentic tools and plugins. 👤
- **Review permissions** and disable network or write access when not needed. 🧰
- **Document approved tools** for your core facility team. ✅

Further topics/keywords: least privilege, compartmentalization, local inference, acceptable use

## 6) What developers should do: hardening and sandboxing
- **Sandboxing**: restrict file access, network access, and process rights. 🧱
- **Scoped tools**: whitelist only required APIs, paths, and actions. ✅
- **Content filters**: detect and block injection patterns before tool calls. 🕵️
- **Audit logs**: make agent actions traceable and reviewable. 🧾
- **Human-in-the-loop** for risky actions (export, delete, share). 🧑‍⚖️

Further topics/keywords: sandboxing, least-privilege tooling, action auditing, policy enforcement

## 7) Short case: OpenClaw and prompt injection (2026)
OpenClaw’s rich integrations made adoption easy in research groups, but plugin-based prompt injection enabled hidden data exfiltration through chat channels. The lesson: convenience accelerates risk unless permissions and sandboxing are enforced. 🚨

Further topics/keywords: OpenClaw, messenger APIs, prompt injection case study

## 8) Take-home messages
- Agents are not just chatbots; they can act on your systems. ⚡
- Shadow IT increases exposure when sensitive data lives locally. ⚠️
- Practical controls (least privilege, compartmentalization, sandboxing) reduce risk quickly. ✅

Further topics/keywords: governance, security training, risk appetite, safe adoption

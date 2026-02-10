---
apply: always
---

Assume shadow IT: the laptops of employers in the audience manage installations and updates
on their own. The local IT department only does important security announcements for operations systems
and random unannounced checks of the OS updates.

Topics to cover are:

- What are autonomous agentic AI systems? 
- How do autonomous agentic AI systems differ from LLMs with chat-prompts, RPAs and RAGs. Give an easy-to-understand overview about the concepts and a simple-to-follow daily office example
- What are common attacks against autonomous AI systems?
- How can a user protect the environment from these attacks?
- What can developers do, to harden their autonomous AI system? How does sandboxing work here?

Give an overview of how exfiltration attacks work with the example of OpenClaw and when it is connected
to a publicly available communication platform. 
As the exfiltration example via prompt injection, assume the victim uses OpenClaw on their work laptop and
have connected the OpenClaw agent to the WhatsApp API. The attack shall start from an Whatsapp Group the user
also is part of.
Assume OpenClaw has network access and that the attack successfully sends sensitive information to the attackers
web server via simple HTTP, which is not captured by institutional firewalls.

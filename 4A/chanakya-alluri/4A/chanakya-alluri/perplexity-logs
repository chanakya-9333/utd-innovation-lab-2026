# Week 1 – Complete Folder Submission  
Author: Chanakya Alluri  
Team 4A – Bot Architecture & Integration  

---

# SECTION 1 – Research Logs

---

## Research Session 1 – Real-Time Voice Fundamentals

Date: 2026-02-17  

Initial Query:
- best real-time voice ai agents 2026  

Follow-up Queries:
- what is real time ai voice  
- how does latency work in conversational ai  
- stt llm tts pipeline explanation  
- what is acceptable latency for ai voice  

What I Learned:
- Real-time voice is a streaming pipeline: STT → LLM → TTS.  
- Latency is cumulative across all components.  
- Telephony routing adds additional delay.  

What Confused Me:
- No consistent latency benchmarks.  
- “Real-time” used loosely in marketing.  

Dead End:
- Found many TTS tools labeled as “voice AI platforms.”  

How I Refined My Thinking:
- Separate voice engines from full voice agents.  

---

## Research Session 2 – Customer Support Capability

Initial Query:
- which voice ai platforms handle customer support  

Follow-up Queries:
- inbound ai receptionist comparison  
- voice ai interruption handling barge-in  
- retell vs polyai vs cognigy  

What I Learned:
- Outbound automation ≠ inbound support.  
- Customer support requires escalation + tool-calling.  

What Confused Me:
- Hard to judge production readiness from marketing.  

Dead End:
- Over-focusing on voice realism.  

How I Refined My Thinking:
- Prioritize telephony + webhook support.  

---

## Research Session 3 – Webhooks & API Integration

Initial Query:
- voice ai webhook api support  

Follow-up Queries:
- tool calling in voice agents  
- crm integration voice ai  
- twilio sip integration ai voice  

What I Learned:
- Webhooks are critical for registration flows.  
- Tool-calling is essential for CRM + confirmations.  

What Confused Me:
- API documentation often vague.  

Dead End:
- Searching generic “API support” pages.  

How I Refined My Thinking:
- Test structured registration flows manually.  

---

## Research Session 4 – Multilingual Reliability

Initial Query:
- multilingual voice ai hindi support  

Follow-up Queries:
- elevenlabs hindi support  
- retell multilingual  
- language switching voice ai  

What I Learned:
- Hindi support often limited to TTS only.  
- Switching languages mid-call can break context.  

What Confused Me:
- Marketing claims vs real conversational reliability.  

Dead End:
- Trusting language lists without testing.  

How I Refined My Thinking:
- Add language-switch stress tests.  

---

## Research Session 5 – Pricing & Scaling

Initial Query:
- voice ai pricing per minute vs character based  

Follow-up Queries:
- elevenlabs character to minute estimate  
- blended cost voice ai stack  
- how to estimate cost at scale  

What I Learned:
- Pricing models differ drastically.  
- Modular stacks create blended cost.  

What Confused Me:
- How to estimate 1K / 10K / 100K scale without assumptions.  

Dead End:
- Trying to find one universal cost metric.  

How I Refined My Thinking:
- Document pricing model type + assumptions instead of single number.  

---

## Research Session 6 – Architecture & Orchestration

Initial Query:
- voice agent architecture with orchestration layer  

Follow-up Queries:
- n8n vs make integration voice  
- voice to whatsapp automation  
- session management strategy  

What I Learned:
- Orchestration is essential for multi-channel workflows.  
- Voice must trigger WhatsApp + CRM + analytics.  

What Confused Me:
- Shared vs separate bot instances.  
- Where session state should live.  

Dead End:
- Treating voice as isolated channel.  

How I Refined My Thinking:
- Evaluate platforms by integration primitives, not just voice quality.  

---

# SECTION 2 – Architecture Stack Recommendations

Assumptions:
- Average call duration: 3 minutes  
- 5 WhatsApp messages per user  
- Moderate LLM usage  

---

## Stack 1 – Balanced Performance Stack (Recommended)

Components:
- WhatsApp: Twilio  
- Voice: Retell AI  
- Orchestration: n8n (self-hosted)  
- Integration: Shared backend API  

Architecture:

User (Voice Call)  
→ Retell AI  
→ Webhook → n8n  
→ CRM / WhatsApp / Logging  
→ Shared Backend  
→ Temple Site + JKYog Site  

Estimated Monthly Cost:

1K users: ~$980  
10K users: ~$8,600  
100K users: ~$83,000  

Complexity: Medium  

Pros:
- Strong production readiness  
- Clean webhook support  
- Cost predictable  

Cons:
- Slightly less natural voice than premium engines  

Recommended Use Case:
Temple helpline + event registration + WhatsApp follow-up  

---

## Stack 2 – Premium Experience Stack

Components:
- WhatsApp: Meta Direct API  
- Voice: ElevenLabs Conversational AI  
- Orchestration: Make.com  
- Integration: Centralized backend  

Architecture:

User  
→ ElevenLabs Agent  
→ Make.com  
→ CRM / WhatsApp / Email  
→ Central Backend API  

Estimated Monthly Cost:

1K users: ~$1,620  
10K users: ~$11,400  
100K users: ~$93,000+  

Complexity: Medium–High  

Pros:
- Best voice realism  
- Strong Hindi support  

Cons:
- Character-based pricing complexity  
- Higher cost at scale  

Recommended Use Case:
Premium conversational system  

---

## Stack 3 – Enterprise Automation Stack

Components:
- WhatsApp: MessageBird  
- Voice: PolyAI  
- Orchestration: Enterprise workflow layer  
- Integration: Separate bot instances  

Architecture:

User  
→ PolyAI  
→ Workflow Engine  
→ CRM / WhatsApp / Escalation  
→ Enterprise Data Layer  

Estimated Monthly Cost:

1K users: ~$3,700+  
10K users: ~$24,000+  
100K users: Enterprise contract  

Complexity: High  

Pros:
- Enterprise-grade stability  
- Advanced escalation logic  

Cons:
- Expensive  
- Heavy implementation  

Recommended Use Case:
Large-scale call center deployment  

---

# Final Recommendation

Primary Recommendation: Stack 1 – Balanced Performance Stack  

Reason:
- Best balance of cost, flexibility, and scalability  
- Clean integration into multi-channel system  
- Suitable for temple-scale deployment  

Secondary Option:
Stack 2 if voice realism is priority  

Stack 3 is enterprise-grade but excessive for initial deployment  

---

End of Complete Folder Submission

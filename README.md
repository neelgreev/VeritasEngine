
# VeritasEngine 🚀
### Autonomous Research & Fact-Checking Multi-Agent Reflection System

**VeritasEngine** is an event-driven, self-correcting multi-agent pipeline built using **n8n**, designed to eliminate hallucinations and enforce quality control through automated reflection loops. 

---

## 🏗️ Architecture & Data Flow

```text
[Webhook Trigger] ➔ [Researcher Agent (Gemini + Brave Search)] ➔ [Critic Agent (OpenAI)] ➔ [If Router]
                                                                        │
                   ┌────────────────────────────────────────────────────┘
                   ▼ (If Approved)                        ▼ (If Revisions Needed)
         [Respond to Webhook]                    [Edit Fields (State & Feedback)]
                                                                  │
                                                          [Safeguard If Loop]
                                                                  │
                                                        (Loops back to Researcher)

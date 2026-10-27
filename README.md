# AI Voice Calling Agent

**A reference design for voice-based lead qualification and appointment assistance.**

Built by [Sana Ullah](https://github.com/AIwithsanaullah) · [NEXORA AI Solutions](https://nexoraaihq.com/)

> **Project status:** This repository documents a proposed voice-agent flow and prompt. It is not evidence of a deployed production calling system. Provider setup, call tests, and integrations must be verified before claiming them as live.

## Use cases

- Answer inbound enquiries with a clear AI disclosure.
- Collect a small, relevant set of qualification details.
- Answer only from approved business information.
- Offer appointment times only after checking actual availability.
- Summarize the call and route complex requests to a human.
- Support outbound calls only when the business has a lawful basis and appropriate consent.

## Proposed call flow

1. Identify the business and disclose that the caller is speaking with an AI assistant.
2. Ask what the caller needs help with.
3. Collect only required details; confirm names, numbers, and dates.
4. Use approved tools for property information or appointment availability.
5. Repeat any proposed appointment details and get confirmation.
6. Offer a human handoff when requested or when confidence is low.
7. Save a minimal call summary and the outcome, subject to retention rules.

## Suggested components

| Component | Possible role |
|---|---|
| Voice provider (for example Retell AI or Twilio-based setup) | Call connection and speech interface |
| n8n | Workflow orchestration and tool calls |
| Approved business knowledge | Grounded answers |
| Calendar/CRM | Booking and lead updates after confirmation |
| Webhooks | Pass call events to authorized workflows |

The exact stack depends on the deployment. The repository does not claim that every component is currently connected.

## Guardrails

- Never pretend to be a human.
- Do not fabricate prices, availability, policies, or completed actions.
- Do not claim a booking succeeded until the calendar tool confirms it.
- Confirm before taking consequential actions.
- Honor requests to stop or speak with a person.
- Follow local call-recording, consent, privacy, and telemarketing requirements.
- Keep API keys and provider credentials out of Git.

## Repository contents

- [Voice agent prompt](prompts/voice-agent-prompt.md)
- [Setup checklist](docs/setup-guide.md)
- [Test cases](tests/test-cases.md)

## Validation checklist

Before calling this production-ready, verify inbound and outbound routing separately, tool failure handling, interruption behavior, latency, call recording settings, opt-out behavior, human handoff, and actual call logs. Use a test number and synthetic data first.

## Contact

- Website: https://nexoraaihq.com/
- LinkedIn: https://www.linkedin.com/in/sana-ullah-4447a0427/
- GitHub: https://github.com/AIwithsanaullah

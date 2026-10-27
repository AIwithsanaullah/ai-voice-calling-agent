# Setup Guide

This is a provider-neutral checklist, not a production-ready workflow export.

## 1. Choose the first use case

Start with one controlled scenario, preferably inbound FAQs and lead capture. Add booking only after the first scenario passes testing. Treat outbound calling as a separate scope with separate consent and compliance checks.

## 2. Configure the voice provider

- Create a test agent and test phone route in the provider dashboard.
- Configure the AI disclosure and opening script.
- Set language, voice, turn-taking, interruption behavior, and maximum call duration.
- Configure a safe fallback and human handoff route.
- Review call recording and transcript retention settings.

## 3. Connect tools

If using n8n or webhooks:
- Validate incoming event signatures where supported.
- Parse only the expected fields.
- Use approved knowledge sources for business facts.
- Check calendar availability before proposing times.
- Require confirmation before booking.
- Return explicit success/failure results to the voice agent.
- Apply timeouts and retries carefully to avoid duplicate actions.

## 4. Protect credentials and data

Use the provider's secret store or the automation platform's credential manager. Never commit API keys, phone numbers, webhook secrets, recordings, or real transcripts to GitHub. Limit logs to information needed for debugging.

## 5. Test before launch

Test quiet and noisy audio, interruptions, silence, caller corrections, unsupported questions, missing details, tool timeouts, booking conflicts, human handoff, opt-out, and provider disconnection.

## 6. Release checklist

- Test calls complete successfully in a non-production environment.
- AI disclosure is clear.
- No unsupported facts are invented.
- Booking results reflect the real calendar response.
- Handoff and opt-out are tested.
- Recording/retention rules are approved.
- A human fallback exists.
- Actual performance claims are measured and documented.

This repository does not itself configure your voice provider or establish that a live calling system is deployed.

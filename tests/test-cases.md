# Voice Agent Acceptance Tests

Use a test number and synthetic data. Record pass/fail evidence for each test.

| ID | Scenario | Expected behavior |
|---|---|---|
| VA-01 | Call begins | Agent identifies the business and discloses it is AI |
| VA-02 | Caller asks a verified FAQ | Agent gives a concise, accurate answer |
| VA-03 | Caller asks for unknown pricing | Agent does not guess and offers a human follow-up |
| VA-04 | Caller interrupts | Agent stops or adjusts speech and responds to the correction |
| VA-05 | Caller gives an incomplete phone number | Agent asks for clarification before saving it |
| VA-06 | Calendar has no matching slot | Agent does not offer an unavailable slot |
| VA-07 | Caller confirms a slot, tool succeeds | Agent reports the confirmed booking details |
| VA-08 | Booking tool fails | Agent says the booking is not confirmed |
| VA-09 | Caller asks for a human | Handoff is attempted; if unavailable, the limitation is explained |
| VA-10 | Caller says stop/do not call | Opt-out is recorded and future automated calls are blocked |
| VA-11 | Speech is unclear | Agent asks for repetition rather than guessing |
| VA-12 | Provider webhook retries an event | Workflow avoids duplicate side effects where possible |

## Evidence template

Record test ID, provider/environment, synthetic scenario, expected result, actual result, pass/fail, and fix. Redact credentials, phone numbers, and any real caller data before sharing evidence.

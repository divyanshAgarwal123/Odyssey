# Odyssey retrospective validation

Source commit: 1bf6ec0044ca688c0fb6cd5ae5f23a4094ed4dea.

Install with npm ci on Node 22, then run npm test, npm run lint and npm run build.
The coverage report includes only the new aggregation/fallback module and shared
AI request/response schema. The rest of the application has a separate suite.

The screenshots show the Mission page in Chromium with sample guest history.
The browser used real routes, dialog, controls, layout and keyboard events with
loopback AI responses and a fixture for clipboard writes. It verified no AI
request before opt-in, the exact aggregate-only payload, failure and retry, and
the empty history surface. The edge fixture instead calls the real request
handler with an in-process model client. No production accounts or provider
credentials were used.

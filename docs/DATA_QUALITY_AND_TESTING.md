# Weather data quality and testing

Weather applications depend on timely, correctly interpreted data. This checklist helps contributors verify data handling without assuming a particular provider or framework.

## Test scenarios

1. **Valid location:** Confirm that the displayed location matches the requested city or coordinates.
2. **Missing location:** Show a clear message instead of a blank or broken screen.
3. **Network failure:** Handle timeouts and unavailable weather services without crashing.
4. **Missing fields:** Display an unavailable state rather than inventing temperature, precipitation, or wind data.
5. **Units:** Label Celsius/Fahrenheit, wind speed, and precipitation units explicitly.
6. **Time zones:** Distinguish the observation timestamp from the user's local time.
7. **Stale data:** Clearly identify the last successful update; do not silently present old observations as current.
8. **API security:** Keep provider credentials out of source control and browser-visible secrets where possible.

## Reproduction template

- Commit/version:
- Location:
- Weather provider (if applicable):
- Request time and time zone:
- Expected behavior:
- Actual behavior:
- Error message (redact secrets):

## Before merging

- [ ] Verify the real application entry point and existing configuration.
- [ ] Run the project's existing tests, if present.
- [ ] Confirm no existing features or UI behavior were unintentionally changed.
- [ ] Document manual test results and any untested scenarios.

This document is a testing guide, not a claim that these cases are already implemented.

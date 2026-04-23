# Wrong Data Returned Bug

## Summary
A user reported that the API request succeeded, but the returned title did not match the expected value.

## Request
GET /posts/1

## Observed Behavior
- Response status: 200 OK
- Response returned valid JSON
- Title field did not match expected value

## Validation
Expected:
"Test incident"

Actual:
The API returned a different title value

## Investigation
- Confirmed endpoint path is valid
- Confirmed response structure is correct
- Confirmed failure is related to returned data, not connectivity or endpoint availability

## Root Cause
The endpoint returned data that did not match the expected business value.

## Resolution
Flagged as a data/logic issue for further review and documented expected vs. actual behavior.

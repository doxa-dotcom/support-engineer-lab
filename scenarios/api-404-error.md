# API 404 Error Incident

## Summary
A user reported that the API endpoint was not working.

## Request
GET /invalid

## Observed Behavior
The request returned:
404 Not Found

## Investigation
- Verified base URL is correct
- Checked endpoint structure
- Compared with working endpoints

## Root Cause
The endpoint used does not exist.

## Resolution
Provided correct endpoint:
GET /posts/1

# Authentication Failure (401 Unauthorized)

## Summary
A user reported that they are unable to access the API endpoint due to an authorization error.

## Request
GET /posts/1  
Header: Authorization: Bearer <token>

## Observed Behavior
API request fails with 401 Unauthorized.

## Investigation
- Verified endpoint is correct
- Reviewed request headers
- Identified missing or invalid authentication token

## Root Cause
Invalid or expired authentication token

## Resolution
- Provided valid authentication token
- Confirmed correct authorization header format

## Notes
This scenario simulates common authentication issues in secured APIs.

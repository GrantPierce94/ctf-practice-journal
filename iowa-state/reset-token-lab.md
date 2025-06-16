# Iowa State - Reset Token Lab

**Difficulty:** Medium  
**Category:** Web / Logic Flaw  
**Status:** Completed

## Summary
App had a password reset form using tokenized URLs. Noticed the tokens were incremental and base64-encoded user IDs.

Wrote a quick Python script to brute user ID values and craft valid reset URLs.

## Tools Used
- Python
- Burp Suite
- CyberChef

## Lessons Learned
- Don't base token security on user ID alone
- Always try decoding "random" strings — they’re often base64

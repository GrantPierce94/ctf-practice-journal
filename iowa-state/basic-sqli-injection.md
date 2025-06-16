# Iowa State - Basic SQL Injection Lab

**Difficulty:** Medium  
**Category:** Web / SQLi  
**Status:** Completed

## Summary
Login page vulnerable to classic `' OR 1=1 --` SQL injection.

Bypassed login and accessed admin dashboard. Found another injection vector in the search bar, used `UNION SELECT` to dump a second user table.

## Tools Used
- SQLMap
- Burp Suite
- Firefox Dev Tools

## What I Learned
- SQL injection is still common
- Input filtering doesn’t mean injection protection

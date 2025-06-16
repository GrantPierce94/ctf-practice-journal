# Hack The Box - Netmon

**Difficulty:** Medium  
**Category:** Windows / FTP  
**Status:** User Shell Only

## Tools Used
- Nmap
- SMBClient
- Searchsploit

## Summary
FTP was open and allowed anonymous login. Found user directories with configuration files exposed.

Used a leaked config to find hardcoded credentials, logged into web interface running on port 8080.

## Blocker
Got user shell, but no clear path to SYSTEM. Suspect service misconfiguration but didn’t get a clean exploit working.

## Lessons
- Don’t ignore FTP
- Web dashboards often leak useful internal info

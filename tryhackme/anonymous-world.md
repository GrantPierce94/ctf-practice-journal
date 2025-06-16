# TryHackMe - Anonymous World

**Difficulty:** Medium  
**Category:** Web / Misconfig  
**Status:** Rooted

## Summary
Apache directory listing exposed `.git` directory. Used `wget` to recursively download and reconstruct the source repo.

Found hardcoded credentials in config file. Logged into admin panel and triggered command injection in a diagnostic page.

## Tools Used
- wget
- git-dumper
- Burp Suite

## Flag Path
`/var/www/html/flag.txt` (read after getting shell)

## What I Learned
- Exposed `.git` dirs are a goldmine
- Always check dev endpoints
- Use Burp to test all params for command injection

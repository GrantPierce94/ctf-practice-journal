# TryHackMe - Ignition

**Difficulty:** Medium  
**Category:** Web / Exploitation  
**Status:** Rooted

## Tools Used
- Nmap
- Dirbuster
- PHP reverse shell
- Python3 for local server

## Summary
Initial scan showed port 80 with a PHP-based site. Discovered a developer backup file via directory fuzzing. Inside was a misconfigured PHP file that accepted arbitrary code via POST.

Used a PHP reverse shell to connect back to my listener.

## Privilege Escalation
Found SUID binary with `find / -perm -4000 -type f 2>/dev/null`.  
Used an outdated binary with escalation vector through `env`.

## Lessons Learned
- Always fuzz directories
- Check backup files and dev folders
- Know how to modify PHP shells

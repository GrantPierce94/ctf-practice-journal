# Hack The Box - Lame

**Difficulty:** Medium  
**Category:** SMB Exploitation  
**Status:** Rooted

## Tools Used
- Nmap
- Metasploit
- Enum4linux

## Summary
Discovered SMB open on 445. Used `enum4linux` to enumerate shares. Saw the box was vulnerable to a known Samba exploit.

Used Metasploit `usermap_script` module for remote code execution.

## Privilege Escalation
Spawned a shell and used a kernel exploit to escalate from user to root.

## Notes
- First box I rooted without hints
- Important to read MSF output and check versions before launching exploit

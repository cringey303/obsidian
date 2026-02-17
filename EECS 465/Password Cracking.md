# Attacking Techniques
### Guessing - automated trial of default (known) passwords
- Advantage: no special access to the target system is needed
- Disadvantage: likely to be detected and/or logged
- Tools:
	- THC-Hydra & Medusa
		- fast network logon crackers which support many different services
		- “Guess” passwords on many network services: FTP, HTTP, VNC, POP3, etc
		- Usually complement each other, but work in different ways

### Hashing vs Encryption
Hashing:
- same size
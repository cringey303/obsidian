- Information gathering
- before attacking, skilled adversaries learn as much as possible about
	- the target systems and networks
		- hardware and software
		- network topology
		- typical operation
			- how often people look at the system
			- how things are logged
	- Admins, users, owners
		- phishing emails
- Steps to reconnaissance
	1. open-source intelligence gathering (analyze the target)
		- 
	2. Network scanning

### Open-source intelligence gathering
- **theHarvester** - a tool for gathering e-mail accounts, usernames and hostnames/subdomains from different public sources like search engines and PGP key servers (https://github.com/laramies/theHarvester)
- Kali (in terminal): `theHarvester`

### Network Scanning
- scan hosts connected to a network to determine:
	- live hosts
	- network topology
		- "important" hosts
		- routers
		- firewalls
		- Intrusion Detection Systems
	- OS on each host
	- Ports (services) open on each host
	- Vulnerabilities that can be found on each host
- Tools
	- Nmap (https://nmap.org/)
		- Port scanner, ping sweep, and OS fingerprinting tool
		- Zenmap is a graphical interfacer for Nmap
		- Ping sweeps
			- example: `nmap -sP target_ip`
		- TCP connect
			- Three-way handshake
			- example: `nmap [-sT] target_ip`
		- UDP
			- send a UDP packet
			- example: `nmap -sU target_ip`
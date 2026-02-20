### Virtual Machines
- A separate computer system reliant upon virtualized hardware
- Hypervisor
	- type 1: “Bare metal” - installed directly on top of hardware
	- type 2: “Hosted” - installed as an application in an operating system
		- e.g. virtualbox, fusion

### Virtual Machine Software
- bare metal hypervisors
	- VMWare ESXi
	- Microsoft Hyper-V
- Hosted hypervisors
	- VMWare Workstation/Player/Fusion 
	- VirtualBox
- We will be using VirtualBox
	- runs on Windows, MacOS, and many Linux distributions
	- Open-source, managed by Oracle

### Metasploitable2 - Target
- intentionally vulnerable distribution with pre-installed, vulnerable services
- Potential target services
	- SSH
	- FTP
	- Telnet
	- PostgreSQL
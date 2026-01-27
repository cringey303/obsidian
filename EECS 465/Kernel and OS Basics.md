Operating systems -> Shell -> Kernel -> Hardware

**Root** & **SYSTEM** users vs Regular Users
- root (Linux) and SYSTEM (Windows) are the highest privileged users
	- complete control over the OS and any running applications
- su - "superuser"; become root
- sudo - "superuser do"; ask root to do something for you

Local Shell vs Remote Shells
- **local shells** are a view into the local machine's utilities, applications, etc
- **remote shells** are a view into a remote system's utilities, applications, etc
	- ssh

Clients vs Servers
- One of the most common paradigms in computer systems/networking
- A **servers**, or a system with special resources, computational power, access, etc. provides access to those resources/capabilities, to **clients**
	- web content
	- ssh
	- clonezilla images from NFS (2003 Eaton)

Interacting in a Shell
- execute commands by name
- eg, let's use Nmap, a port scanner
	- `-h` or `--help`
	- 
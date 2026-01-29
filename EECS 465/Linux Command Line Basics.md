# Interacting in a Shell (Terminal)
- execute commands by name
- use **flags** in commands (`-h` for help)
## Important Commands
### Navigation
- `cd` - change directory
- `ls` - list files
- `pwd` - print working directory

### File Navigation
- `mv` - move files around
- `cp` - copy
- `mkdir` - make directory
- `rm` or `rmdir` - remove file or directory

### File Contents
- `cat` - concatenate
	- print file contents to terminal
- `grep` - search in files
- `nano, vi, vim` - command line text editors

### Network
- `ifconfig` - "interface configuration" (lists network interface info, *IP Addresses*)
- `ping` - checks connectivity status (other hosts, websites, etc.)
- `wget` and `curl` - retrieves file/webpages over a network
- `ssh` and `scp` - secure shell and secure copy

### Changing Password
- For hw and reports, may want to change the password to protect your work (lab sticky notes "please do NOT use" can also prove helpful)
- `passwd`
	- triggers a password change for the currently logged in user
	- Enter current password, new password, repeat new password

### Canceling a Command
- `ctrl+c` - attempts to interrupt and kill the current foreground process
- `ctrl+z` - suspends a process and places it in the background
- `kill` - terminate a proce
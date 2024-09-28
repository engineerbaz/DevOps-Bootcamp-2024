# Linux

- Basic commands for navigation 
- File/Directory management
- Managing processes and system information
- Text Editing
- Tools

## User Management

`useradd -m <name>`
// for creating home folder

``adduser <name>``
// for customized options

### Giving Sudo rights

Add in "sudo" group for Ubuntu 

``sudo usermod -aG sudo <username>``

or use
``visudo``

#### User privilege specification
root    ALL=(ALL:ALL) ALL
john  ALL=(ALL:ALL) ALL

### SUDO rights 
visudo is a tool for safely updating the /etc/sudoers file, found in most Linux systems (Ubuntu for example). This is the file that is required for allowing regular users to run commands with superuser privileges — using sudo command.

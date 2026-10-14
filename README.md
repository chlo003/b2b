*This activity has been created as part of the 42 curriculum by chlminga.*

# Born2beRoot

## Table of Contents

- Description
- Project Description
- Instructions
- Technical Comparisons
- Ressources

## Description

Born2beRoot is a system administration project. Its goal is to introduce virtualization and the fundamentals of the Linux server administration.  
  
The project involves setting up a virtual machine running Debian and configuring a secure environment through user and persmission management, password policies, SSH, firewall rules, and system monitoring.  

## Project decription

### Operating System

The operating system chosen for this project is Debian.  
Reasons for choosing Debian:  
- A stable and widely used Linux distribution.  
- A package management system based on APT.  
- Extensive documentation and community support.  
- A suitable environment for learning system adminitration.  
  
The main trade-off is that Debian's stable repositories may provide older software versions than othr distributions.  

### Virtual Machine and Partitioning

The virtual machine is managed using VirtualBox.  
  
The disk uses encryptes partitions through LVM.  

### Security Configuration

- SSH: configured to use port 4242, with root login disabled.  
- Firewall: UFW configured to allow only the required inboundd port.  
- Password policy: password expiration, minimum password length, complexity, and password-change restrictions.  
- Sudo: restricted authentification attempts, logging, TTY enforcement, and command search path restrictions.  
- AppArmor: 

### User and Groupe Management 


### Installed Services
### Monitoring Script

The monitoring.sh Bash script reports system information, including CPU and memory usage, disk usage, network information, ative connections, and sudo command statistics.  

## Instructions

### Starting the Virtual Machine

1.Open VirtualBox.
2.Select the Born2beRoot virtual machine.
3.Start the virtual machine and log in with an authorized account.

### Connecting Through SSH

From a host that can reach the virtual machine, use:  
`ssh chlminga@localhost -p 4242`

### Verifying the Configuration

The following commands can help verify the configuration:  
`hostnamectl`
`sudo ufw status verbose`
`sudo ss -tlnp`
`sudo aa-status`
`lsblk`

## Technical Comparisons

### Debian vs Rocky Linux
### AppArmor vs SELinux
### UFW vs Firewalld
### VirtualBox vs UTM

## Ressources
### Official Documentation
-doc, tuto, etc...
-how AI was used

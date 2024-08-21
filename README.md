TASK - 1 
MONITORING SYSTEM RESOURCES FOR A PROXY SERVER.

Prerequisite: 
- Create an Ubuntu EC2 Instance to create the monitoring system resources for a proxy server.
- Install tools such as git, net-tools, procps, ifstat.
- Net-tools provides the network utilities such as netstat.
- procps provides system monitoring tools such as ps, top.
- ifstat for network statistics.

Process:
- Login into an instance using ssh and git bash.

* ssh -i "ansible-prac.pem" ubuntu@ec2-3-110-30-110.ap-south-1.compute.amazonaws.com

- After login update the packages and install the requirements.

* sudo apt update

* sudo apt install -y net-tools procps ifstat

- Check the installation of tools.
* apt list --installed | grep net-tools
* apt list --installed | grep procps
* apt list --installed | grep ifstat

- Create a file named as monitor-system-resource.sh, sh is an file extension used in bash to execute the script and change the access permission of files and directories, give executable permissions for the script.

* touch monitor-system-resource.sh
* chmod +x monitor-system-resource.sh
* Write the Script and execute it.
* ./monitor-system-resource.sh

# CPU Usage
./monitor-system-resource.sh --cpu

# Memory Usage:
./monitor-system-resource.sh --memory

# Network Usage:
./monitor-system-resource.sh --network

# Disk Usage:
./monitor-system-resource.sh --disk

# System Load:
./monitor-system-resource.sh --load

# Process Monitoring:
./monitor-system-resource.sh --process

# Service Monitoring:
./monitor-system-resource.sh --services

# All Sections:
./monitor-system-resource.sh --all

To test each component with a real-time use refresh interval depending on the component. 

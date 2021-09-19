# Cloud-Security-Project
The files in this repository were used to configure the network depicted below.

 

![](https://github.com/TBI330/Cloud-Security-Project/blob/main/Diagrams/Project%201%20Diagram-Page-1.drawio.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the  file may be used to install only certain pieces of it, such as Filebeat.

 [Elk-Playbook](https://github.com/TBI330/Cloud-Security-Project/blob/main/Ansible/install-elk.yml) 

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly efficient, in addition to restricting access to the network.
Load balancers can help improve application responsiveness and increase availability of applications and websites for users.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to specific files and system logs.
Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing.
Metricbeat is a lightweight agent that is installed on specific servers to periodically collect metric data from your target servers. Metricbeat takes the metrics and statistics from these servers and ships them to the an output, such as Elasticsearch.
The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux Ubuntu     |
| Web 1 VM | Server   | 10.0.0.5   | Linux Ubunutu    |
| Web 2 VM | Server   | 10.0.0.6   | Linux Ubunutu    |
| Elk VM   | Server   | 10.1.0.4   | Linux Ubunutu    |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the home network machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
99.124.228.52

Machines within the network can only be accessed by the jump box.
The IP address of the jump box is 10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 10.0.0.4    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually.
This will ensure our provisioning scripts run identically everywhere. This will further ensure our automated configurations will do exactly the same thing every time they run, eliminating as much variability between configurations as possible.

The playbook implements the following tasks:
- From the ansible container inside the jump box, add the new Elk VM to Ansible's hosts file.
- Create a playbook that installs Docker and configures the container.
- Run the playbook to launch the container.

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.  


![](https://github.com/TBI330/Cloud-Security-Project/blob/main/Project_1/docker_ps_screenshot.PNG)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

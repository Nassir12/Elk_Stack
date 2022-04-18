## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](Diagrams/Elk_Server.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _YAML____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available ____, in addition to restricting __inbound___ to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _jumpbox provisional____ and system _network____.
- _TODO: What does Filebeat watch for?_large files of locations you specify 
- _TODO: What does Metricbeat record?_

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Web 1   | Webservers| 20.127.59.163|  Linux                |
| Web 2    | Webserver| 20.127.59.163|    Linux              |
| Elk Server| Monitoring|20.230.177.186|    Linux              |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the _Jumpbox Provisional ___ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses.  My personal IP address

Machines within the network can only be accessed by _Jumpbox Provisional____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_ My personal Machince/ Jumpbox provisonal : 20.115.26.165

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes             | MY personal IP  |
|  Web 1        |     No                |         10.0.0.6           |
|   Web 2       |     No                |         10.0.0.6            |
|.  Elk    |.        No                 |.        My IP ; 5601/10.0.0.6 |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_Provides Automation 

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- Installation of docker.io to ELK Machine
- Installs pip3 to the ELK Machine
- Installation of the docker python module
- 
The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![](Diagrams/Docker_PS.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- Filebeat
- Metricbeat

These Beats allow us to collect the following information from each machine:
- Filebeat monitors the logs or locations specified, collects data, and sends it to the ELK server 
- Metricbeat periodically collects metric data from the targets server, it is also used to monitor. Then it takes the metric and statistics that was collected and sent to the specific output such like Logstash for example.

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _playbook____ file to __/etc/ansible___.
- Update the _configuration____ file to include...
- Run the playbook, and navigate to __elk server's public IP __ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

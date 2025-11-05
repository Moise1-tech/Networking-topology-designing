FACULTY OF INFORMATION TECHNOLOGY



Date: 30th October 2025


COURSE NAME: COMPUTER NETWORK INSTRUCTOR: JOASHUA IRADUKUNDA



STUDENT NAME: NDARUHUTSE MOISE STUDENT ID: 28340




MID-TERM EXAM PROJECT: COMPREHENSIVE NETWORK CONFIGURATION GUIDE
 
Table of Contents
Project Overview & Network
Topology	3
Pre-Configuration
Requirements	4
Naming and Credential
Standards	5
Network Device Setup &
Addressing	6
VLANs    Configuration    &    Port  Assignments	7
Trunking      and      EtherChannel  Configuration	8
Server           Configuration           &  Services	9
Security                                    Implementation	10
Verification           &           Testing  Procedures	11
Troubleshooting                                Guide	12
 







TOPIC 1. Project Overview & Network Topology

1.1	Project Overview
Computer Networking course is the course that help in IT career to solve main problem related on networking. There is the main Project Goal of this Mid-Term Project are:

	Build complete campus network following the provided topology diagram
	Implement VLAN segmentation and inter-VLAN routing on Main-Router
	Configure VTP modes (Server, Transparent, Client) as specified
	Deploy EtherChannel for link aggregation
	Implement comprehensive security controls
	Configure DHCP services for client networks
	Setup DNS and NTP services


1.2	Network Topology Description
This is a hierarchical enterprise network for "28340 _ BANK" with a centralized core architecture connecting multiple departmental networks across different physical locations (HQ blocks) and Main Router.
 
 
Figure1: Network Topology


TOPIC 2. Pre-Configuration Requirement
Pre-configuration requirements are critical to the success of any network implementation. Here's why they matter for a network topology like the bank system shown:
	Prevents Configuration Errors
	Ensures Security & Compliance
	Optimizes Network Performance
	Establishes Documentation Standards
	Facilitates Troubleshooting
2.1	Software & Equipment Requirement
	Cisco Packet Tracer v8.2.2.0400 or compatible
	Download file format: 28340_NDARUHUTSE MOISE_CNet-F25_MID - ID BANK.pka
	Console Access: Use console cable from IT computer to device console port
	Router & Switch Terminals use Console cable: To configure any network device (Routers, Switches), connect an IT Computer to the device using a Console cable.
	Lab notebook or digital log for command tracking

TOPIC 3. Naming and Credential Standards
Naming and credential standards are fundamental pillars of professional network management. They directly impact security, efficiency, and long-term maintainability of your network infrastructure. Here are some Key Important why naming and credential standards matter:
 
	Security: Protecting critical banking systems
	Compliance: Meeting regulatory requirements
	Efficiency: Reducing operational costs
	Reliability: Minimizing downtime
	Scalability: Supporting business growth
	Professionalism: Demonstrating competence










TOPIC 4. Network Device Set Up & Addressing
Every device needs a unique address (like IP addresses) to send and receive data correctly. Without proper addressing, devices can't communicate similar to how mail needs accurate addresses to reach the right destination, Proper addressing schemes (like subnetting) allow you to logically organize networks into manageable segments. This improves performance, security, and makes troubleshooting much easier.
Without proper setup and addressing, you face issues like:
	IP address conflicts causing devices to drop offline
	Security vulnerabilities from default configurations
	Poor network performance and bottlenecks
	Difficulty troubleshooting problems
	Inability to implement network policies or monitoring


TOPIC 5. VLANs Configuration and Port Assignments
A VLAN (Virtual Local Area Network) is a logical grouping of devices on a network, regardless of their physical location. VLANs allow you to segment a single physical network into multiple isolated broadcast domains, creating separate "virtual" networks on the same physical infrastructure.
5.1	Basic of VLANs Configuration Example
 
 
Figure 2: Manually VLAN Configuration.
5.2	Port Assignment Types
	Access Mode: Port belongs to one VLAN only. Used for end devices like computers, printers, phones.
	Trunk Mode: Port carries multiple VLANs. Used for switch-to-switch or switch-to- router connections.
	Dynamic Mode: Port can automatically negotiate to become access or trunk (less common in modern networks).

5.3	Importance of VLANs in Networking
  Enhanced Security: VLANs isolate sensitive data by separating departments or functions. For example, your finance department's traffic never mixes with guest Wi-Fi traffic.
  Improved Performance: Each VLAN is its own broadcast domain. Broadcasts from one VLAN don't flood the entire network, reducing unnecessary traffic.
  Simplified Network Management: Group devices by function (Sales, HR, IT) rather than physical location, making the network structure match your organizational structure.
  Better Traffic Management: Easier to identify and troubleshoot issues when traffic is logically separated.
  Cost Savings: You don't need separate physical switches for each department - one switch can host multiple virtual networks, Easy to expand without major infrastructure investments.
 

TOPIC 6. Trunking and EtherChannel Configuration
6.1	Trunking
Trunking is a method of carrying traffic from multiple VLANs over a single physical network link between switches, routers, or other network devices. Instead of needing a separate cable for each VLAN, a trunk link uses VLAN tagging to identify which VLAN each frame belongs to, allowing all VLAN traffic to share the same connection.







6.1.1	Basic Trunking Configuration Example (Cisco)

Figure 3: Basic Trunking Configuration
6.1.2	To Verify Trunking Configuration
 
 
Figure 4: Showing verification of Trunking.











6.2	EtherChannel Configuration
EtherChannel is a port link aggregation technology that bundles multiple physical Ethernet links into a single logical link. This creates a high-bandwidth connection between switches, or between a switch and a server/router. There are Three Ways to Configure EtherChannel:
1.	PAgP (Port Aggregation Protocol):
•	Cisco proprietary
•	Modes: desirable (active) and auto (passive)
2.	LACP (Link Aggregation Control Protocol)
•	IEEE 802.3ad standard (industry standard)
•	Modes: active and passive
•	Preferred for multi-vendor environments
3.	Static (Manual) Configuration
•	Mode: on
•	No negotiation protocols
 
•	Both sides must be manually configured


6.2.1	Basic EtherChannel Configuration (Cisco)

Figure 5: Showing EtherChannel Configuration








6.2.2	To verify the EtherChannel Configuration

Figure 6: Showing verification of EtherChannel configuration.


TOPIC 7. Server Configuration & Services
Server configuration refers to the process of setting up, optimizing, and managing server hardware and software to provide specific services to clients on a network. It involves installing
 
operating systems, configuring network settings, implementing security measures, and deploying various services. In Our Project we have several different Server we are going to see their functionality in our project. We have Web-Server, AD/DC server, CBS server, EDWH server, Syslog server, NET-monitoring server and SIEM server.


	Web-Server: is software and hardware that uses HTTP (Hypertext Transfer Protocol) and other protocols to respond to client requests made over the internet or intranet. Its core job is to store, process, and deliver web pages and content to users.
	AD/DC server: is Microsoft's directory service that manages and organizes network resources in a Windows domain environment. It provides centralized authentication, authorization, and management of users, computers, and other network objects.
	CBS server: CBS is Windows' built-in servicing technology for managing system components, updates, and configurations.
	EDWH server: is a centralized repository that stores integrated data from multiple sources across an entire organization.
	Syslog server: is logging system that collects, stores, and manages log messages from network devices, servers, applications, and security systems across an IT infrastructure.
	NET-monitoring server: is system that continuously observes, tracks, and analyzes the performance, availability, and health of network infrastructure, devices, servers, and applications. It provides real-time visibility into network operations and alerts administrators to issues before they impact users.
	SIEM server: server is a comprehensive security platform that collects, aggregates, analyzes, and correlates security-related data from across an entire IT infrastructure in real-time.
7.1 Example of Web Server configured on this project
 













TOPIC 8. Security Implementation
Security implementation in networking means applying different security measures, tools, and configurations to protect network devices, data, and communication from unauthorized access, misuse, or attacks. It ensures that confidentiality, integrity, and availability of data are maintained throughout the network.

8.1 The Main Component of Security Implementation in Networking
1.	Device Security: Protects routers, switches, and servers by controlling who can access or configure them.
Examples:

•	Setting strong passwords
•	Using SSH instead of Telnet for remote access
•	Implementing AAA (Authentication, Authorization, Accounting)

8.1.2	Device Security using SSH (Secure Shell) Configuration





2.	Network Access Control: Restricts what users and devices can do once they’re connected.
 
Examples:

	Access Control Lists (ACLs): filter traffic by IP, port, or protocol
	Port security: limit which devices can connect to a switch port
	802.1X authentication: verify devices before granting access

8.1.3	Access Control list verification (ACL)
 

Figure 9: Showing Accessing Control List verification



3.	Monitoring and Logging: Tracks and records network activity to detect unusual or malicious behavior.

Examples:

•	Syslog servers: store logs from routers/switches
•	SNMP monitoring: track network performance and alerts
•	IDS/IPS logs: detect security threats





8.1.4	The verification of Logging
 
 
Figure 10: Showing Logging verification in router.























TOPIC 9. Verification and Testing Procedures
 
9.1 Verification
1.	Show Ip Interfaces Brief

Figure 11: Showing interface and their status on router.

2.	Show Ip Route


Figure 12: Showing routing table.







3.	Show IP DHCP Binding
 
 

Figure 13: Showing binding DHCP in router.


 
Web Access by IP and DNS Resolution










END

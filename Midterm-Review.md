## Networking Essentials
• What are the advantages and disadvantages of computer networking?

Advantages: Enhanced Communication, Resource sharing, Centralized Management

Disadvantages: Security Risks, Potential of Downtime, Complex to Manage

• Understand that the internet is primarily a packet-switched network and the im-
plications of this.

• What are the network edge and network core?
• What is a threat model for the internet? Be able to explain and solve problems.
• What are the layers of the TCP/IP and OSI models? Be able to explain what
service/device/protocol belongs to which layer.
• What is the difference between an ethernet hub, ethernet switch, ethernet repeater,
and ethernet bridge? What is each device used for?
• What are LAN, WAN, and CAN?
• What is the difference between an ethernet router and an ethernet switch?
• What is the difference between simplex, half-duplex, and full-duplex transmission
modes? Discuss the stability and security implications of each network topology.

## IP and Subnetting
• What is subnetting? What are its practical applications?
• Know the structure of an IP address.
• What are the disadvantages of classful addressing?
• What is Classless InterDomain Routing (CIDR)? How does it compare to classful
routing?
• Be able to identify the subnet and host parts of a CIDR address.

• Example: Consider address 128.20.12.5/16. What are the host and network por-
tions of the address?

• Example: Consider address 192.168.6.7/24. What are the host and network por-
tions of the address?

• Be able to translate between dotted decimal notation and CIDR masks.
• Example: Consider address 124.12.42.3 and the subnet mask 255.255.252.0. What
CIDR prefix is the mask equivalent to? What are the subnet and host portions of
the address?
• Example: Consider address 137.151.45.6 and the subnet mask 255.255.0.0. What
is the CIDR prefix that the mask is equivalent to? What are the subnet and host
portions?
• Be able to break up networks into subnets.
• Example: Consider subnet 137.20.0.0/16. Split the network into 6 different subnets.

• Example: Consider subnet 128.34.128.0/17. Split the network into 3 different sub-
nets.

• What is supernetting? Understand and solve problems.
• Example: Consider subnets 192.168.12.0/24, 192.168.3.0/24, and 192.163.45.1/24.
Merge them into a single subnet.
• Example: Consider subnets 128.78.128.0/17 and 192.168.64.0/18. Merge them into
a single subnet.
• What is the difference between static and dynamic IP address assignment?
• What is Dynamic Host Configuration Protocol (DHCP)? Discuss the steps.
• What are the different security attacks against DHCP?
• Be able to dynamically and statically configure IP addresses in Windows and Linux.
• What is the difference between the subnet mask and the wildcard mask?

## Ethernet Switching and VLANs
• At what layer do ethernet switches function?
• What is the difference between a managed and unmanaged switch?
• Understand that ethernet switches are transparent to hosts and are plug-and-play
devices.

• Be able to explain how switches construct a forwarding Content Addressable Mem-
ory (CAM) table and solve problems similar to the assignment.

• What is the difference between a switch and a router?
• What are the scalability and security issues involving large LANs?


• What are Virtual LANs (VLANs)? Be able to explain and solve problems.
• What are the security advantages of VLANs and how are VLANs used for network
segmentation?
NAT (Network Address Translation)
• Explain what NAT stands for and how it is used in networking. Give some examples
of its practical applications and how to solve problems involving NAT.
• How can NAT be beneficial to security?
• Discuss the pros and cons of NAT for network performance, security, and scalability.
• Compare and contrast the different techniques for NAT traversal. How do they
work and when are they used?
• Understand and trace the process of packet transformation as the packet exits an
internal NATed network and how the response from an external source is modified
upon re-entry through NAT.
• Be able to configure NAT in a Cisco router. You will be given access to Cisco router
documentation.

## IPv6
• What is the difference between the IPv6 and IPv4 packet structure?
• Why is IPv6 considered to be more efficient and secure than IPv4?
• What is IPv6 tunneling and what is it used for?
Routing Basics
• Explain the basic process of how a router routes.

• Understand and explain the longest common prefix routing and solve related prob-
lems.

• Example: Consider a packet with the destination IP address of 128.34.23.29 and a
router with the routing table below. To which port will the packet be forwarded?
Prefix Port
192.168.0.0/16 1
192.168.128.0/17 2
192.168.160.0/19 3
Default 4


## Cisco Router Basics

• What is the difference between the Cisco router’s startup and running configura-
tions? How do you save the running configuration into the startup configuration?

• Example: Consider a Cisco router with network interfaces FastEthernet0/0, FastEthernet0/1,
and FastEthernet1/0. Configure the interfaces with IP addresses of 192.168.2.1,
192.168.3.1, and 192.168.4.1 all with the mask of /24.

## Nmap and Network Mapping

• What is network mapping and why is it important in security?
• Be able to use nmap to map out networks and read the nmap output. You will be
given the nmap manual and you may use the nmap man page.
• What is the difference between open, closed, filtered, and unfiltered ports?
• Know and be able to use the different modes of nmap.
• Example: What will the following nmap command do?
nmap -sS 192.168.0.1 -p 1-2000
• Example: How to conduct a decoy scan of system 192.168.4.3 using systems
192.168.4.5 and 192.168.4.3 as decoys?

## Dynamic Routing
1. What is the main difference between OSPF and RIP in terms of routing metrics?
2. What type of routing protocol is RIP, and what does this mean?
3. What is the maximum hop count in RIP, and what does it signify?
4. How often does RIP send updates by dehow fault, and why is this significant?
5. What are the limitations of RIP compared to OSPF?
6. How does OSPF handle changes in the network topology?
7. Explain the concept of OSPF areas and their importance.
8. What is the role of a Designated Router (DR) in OSPF?
9. How does OSPF achieve loop-free routing?
10. What is the function of the Link State Advertisement (LSA) in OSPF?
11. Describe the OSPF neighbor establishment process.
12. How does OSPF calculate the best route to a destination?
13. What are the different types of OSPF networks?
14. Explain the purpose of OSPF authentication.
15. Be able to implement OSPF configuration and authentication in GNS3 on various
Cisco routers similar to the assignment.

## ARP Poisoning Attacks
• What is the ARP protocol? Be able to explain and solve related problems.

• What is an ARP poisoning attack? Identify and explain how the attack is per-
formed.

• Be able to understand the output of the arp command and use it to identify signs
of an ARP poisoning attack.

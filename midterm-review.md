# CPSC 456 3/13/2025 Midterm Review

### What are LAN, WAN, and CAN?

### What is the difference between 
Packet filter, will filter out the network

### Simplex 
One direction, 
halfduplex- two directions, one at a time
- Full duplex: simultanitous directions, back and forth at the same time

### LInek laywer securiy
- Ethernet
  - layer 2 on mac

- Managed and Unmanaged
  - mangeged adds another layer of security, limits mac addresses in cam table

- Ethernet Switches transparent
  - Switches are transparent as they build the cam table themselves
 
- Building a cam table
  - Question 2 first assignment look at it.

- Diff between routers and switch
  - Switch will stay in one subnet only
 
- What are VLANS
  - having a large LAN is a security issue
  -  Logically these lans under VLANS are different networks, but they are still the same physically
  -  If one department is under attack, then another department will not be as they are separated

- What is ARP protocol?
  - Address resolution protocol. It will map IP to MAC address
  - The ARP table will talk to the CAM table
- What is an ARP poisoning attack?
  - It will disrupt the IP to MAC map
  - It will fool the table into thinking that the attackers address is the correct address
  - Packet Sniffing, This is a man in the middle attack
 
## IP and Subnetting
  - **What is subnetting? What are its practical applications?**
    - Different Islands underneath a larger company
    - Can apply different security to different subnets
    - Can split these departments into different networks
  - **What is the structure of and IP address?**
    - 32 bit === x.x.x.x each 8 bits
    - Make up 4 billion address combinations
  - **What is Classful addressing?** 
    - Only need to know that Classless has a lot of waste


  - EX: 192.20.12.5/16 What are the host and network portions of the address?
    First convert the  IP and Subnetmask to Binary
    IP Address:
    128.20.12.5 = 10000000.00010100.00001100.00000101
    Subnet Mask:
    255.255.0.0 = 11111111.11111111.00000000.00000000


    Do and AND operation of the two:
    10000000.00010100.00001100.00000101 AND
    11111111.11111111.00000000.00000000
    = 10000000.00010100.00000000.00000000
    The network portion is:
    128.20.0.0

    Finding the host portion:
    10000000.00010100.00001100.00000101 XOR
    11111111.11111111.00000000.00000000
    = 00000000.00000000.00001100.00000101
    The host portion is 0.0.12.5


  - EX: 192.168.6.7/24
    First convert the IP and Subnet mask to Binary
    IP Address:
    192.168.6.7 = 11000000.10101000.00000110.00000111
    Subnet Mask:
    11000000.10101000.00000110.00000111 AND
    1111111.11111111.11111111.00000000
    = 11000000.10101000.00000110.00000000
    Network Portion is:
    192.168.6.0

    11000000.10101000.00000110.00000111 XOR
    1111111.1111111.1111111.00000000
    = 00000000.00000000.00000000.00000011
    The host portion is:
    0.0.0.7

  - Splitting an IP address into 6 subnets
    EX: 137.20.0.0/16 -> 6 Subnets
    We can split into 2 4 or 8 . We need to use 8 since we have 6 subnets
    2^3 = 8 -> 3 is the number of bits to borrow

    /16 + 3 = /19 for the new subnet mask

    2^32-19 = 2^13 = 8192 addresses that can be used in this subnet

    8192/256 = 32 

    | Network Address |Visible Address | Broadcast Address |
    | -----------|----------------------------|--------------- |
    | 137.20.0.0 | 137.20.0.1 - 137.20.31.254 | 137.20.31.255|
    | 137.20.32.0 | 137.20.32.1 - 137.20.63.254 | 137.20.63.255 |
    | 137.20.64.0 | 137.20.64.1 - 137.20.95.254 | 137.20.95.255 |
    | 137.20.96.0 | 137.20.96.1 - 137.20.127.254 | 137.20.127.255 |
    | 137.20.128.0 | 137.20.128.1 - 137.20.159.254 | 137.20.159.255 |
    | 137.20.160.0 | 137.20.160.1 - 137.20.191.254 | 137.20.191.255 |



    

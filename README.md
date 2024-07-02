# Network Subnetting with VLSM, DHCP, and OSPF Routing -Computer Networks 

## Description
This project uses Variable Length Subnet Masking (VLSM) to efficiently allocate IP addresses to a network with three subnets. DHCP dynamically assigns IPs, and OSPF routing is configured to ensure proper packet delivery between subnets. The network address of 192.16.2.0 is divided to meet specific host requirements.

### Network Requirements
- **Network A**: 62 hosts
- **Network B**: 26 hosts
- **Network C**: 3 hosts
- **Network Address**: 192.16.2.0

### Steps Involved
1. **VLSM Calculation**: Calculate the subnet masks and IP ranges for each subnet.
2. **DHCP Configuration**: Set up DHCP to assign IP addresses dynamically.
3. **OSPF Routing**: Configure OSPF routing to enable communication between subnets.

### VLSM Calculation
1. **Network A**: Requires 62 hosts.
    - Subnet Mask: 255.255.255.192 (/26)
    - IP Range: 192.16.2.1 - 192.16.2.62
    - Network Address: 192.16.2.0
    - Broadcast Address: 192.16.2.63

2. **Network B**: Requires 26 hosts.
    - Subnet Mask: 255.255.255.224 (/27)
    - IP Range: 192.16.2.65 - 192.16.2.90
    - Network Address: 192.16.2.64
    - Broadcast Address: 192.16.2.95

3. **Network C**: Requires 3 hosts.
    - Subnet Mask: 255.255.255.248 (/29)
    - IP Range: 192.16.2.97 - 192.16.2.99
    - Network Address: 192.16.2.96
    - Broadcast Address: 192.16.2.103

### DHCP Configuration
1. Set up a DHCP server to allocate IP addresses dynamically within the calculated IP ranges for each subnet.
2. Ensure that the DHCP server is configured to assign the correct default gateway and DNS server information.

### OSPF Routing Configuration
1. Configure OSPF on each router to advertise the subnets.
2. Ensure that OSPF neighbors are correctly established and routes are propagated.

### Implementation Details
- **VLSM Calculation**: Python script or manual calculation
- **DHCP Configuration**: Configuration files for the DHCP server
- **OSPF Routing**: Configuration files for routers

### Prerequisites
- Basic understanding of networking concepts.
- Access to network simulation tools (e.g., Cisco Packet Tracer, GNS3).
- Basic knowledge of DHCP and OSPF configuration.

### Getting Started
1. Clone this repository:
    ```bash
   git clone (https://github.com/thelaibaasif/Network-Subnetting-with-VLSM-DHCP-and-OSPF-Routing/tree/main)
    ```
2. Follow the steps in the `Implementation Details` section to set up the network.
3. Verify the network setup by testing IP allocation and routing between subnets.

### Author
Laiba Asif 

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



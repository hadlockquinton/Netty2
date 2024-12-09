#  Outcomes
    Explain and compare binary, decimal, hexadecimal and base64 formats
    Describe LAN topologies and devices
    Describe LAN technologies and their benefits and hindrances
    Explain why and how frames are interpreted by different devices
    Identify how switches affect network traffic and the visibility of network traffic by other hosts
    Describe MAC addressing
    Analyze 802.3 frame headers
    Describe the contents of an Ethernet header and frame
    Describe an 802.1Q virtual local area network (VLAN) frame and how its frames differ from a standard 802.3 frame
    Describe the address resolution protocol (ARP)
    Explain man-in-the-middle (MitM) with ARP
    Explain VTP with its vulnerabilities
    Explain DTP with its vulnerabilities
    Explain CDP, FDP and LLDP and the security vulnerabilities
    Explain STP with its vulnerabilities
    Explain Port Security with its vulnerabilities
    Describe VLANS and Security vulnerabilities


#    OSI MODEL
        Application
        Presentation
        Session
        Transport
        Network
        Data-Link
        Physical

#    Internet Standard Orignizations
        IANA [] https://www.iana.org/
        RIR's []
        IEEE [] https://www.ieee.org/


#    Binary
    Base 2
    Bit=1, Nibble=4 bits, Bytes=8 bits, Half word=16 bits, Word=32 bits, Double Word=64 bits
#    Decimal
    Base 10
#    Octal
    Base 8
#    Hexadecimal
    Base 16 
#    Base 64
    Encoded with ASCII by using 26 letters of the latin alphebet in both upper and lower case plus 0-9 and adding 2 special characters
#    Topologies
    BUS : A bus network is a network topology in which nodes are directly connected to a common half-duplex link called a bus.
    STAR : A central hub that everything connects together
    RING : Each node connects exactly to two nodes foring a ring
    MESH : every Node has a bride to another node
    WIRELESS : Topology that uses wireless connections to connect to AP's
    HIERARCHICAL: A core layer of high-end switches optimized for network availability and performance.
                  A distribution layer of switches implementing forwarding decisions.
                  An access layer connecting users via hubs, bridges, or switches

#    Devices 
    Hubs: Devices that allow multiple devices to connect to the same wire
    Switches: devices that allow multiples devices to connect to the network
    Repeaters: Devices that allow a connection to be extended beyond normal operational cable or wireless limits

#    Internet Timing
    Bit Time - is the period of time is required for a bit to be placed and sensed on the media. Network speeds are measured by how many bits can be placed or sensed on the media in 1 second. Each increase in speed requires more bits to be sent during the same 1 second internal. To accomplish this the bit-times are reduced.
    | Speed | Bit-time |
    |---------------|---------------|
    | 10 Mbps	| 100ns		|
    | 100 Mbps	| 10ns		|
    | 1 Gbps	| 1ns		|
    | 10 Gbps	| .1ns		|
    | 100 Gbps 	| 0.1ns		|


#    Mac Address
    Parts : OUI; First 3 byts assigned by IANA
            Vendor Assigned: Assigned by the vendor
    You can spoof MAC addresses with Software

#    VLAN types
    Default: VLAN
    Data: User Traffic
    Voice: VOIP
    Management: Switch and Router management
    Native: Untagged switch and Router Traffic
    
#    VLAN hopping attack
    Switch spooging(DTP)
    Single Tagging
    Double tagging

# Arp
    Address Resolution Protocol
        Types: ARP(OP 1 and OP 2)
               RARP (OP 3 and OP 4)
               Proxy ARP(OP 2)
               Gratuitous ARP(OP 2)
               
    ARP CACHE : All Resolved MAC to IP resolutions
                if MAC is not in CACHE, then ARP is used 
                Dynamic entries last from 2-20 minutes
                Default Gateways is present at minimum
                can be easily duped by attackers

    ARP POISONING ATTACK
        MiTM by poisoning the arp cache with gratuitous arp or proxy arp


# VTP   
    VLAN trunking protocol: Dynamically move/remove/add/modify VLAN's
    CISCO Proprietary
        modes: Server, Client, and Transparent
    Vulnerability:  Can cause switches to dump all VLAN information
                    Cause a DoS as switch will not support configured VLAN's
# DTP
    Dynamic Trunking Protocol: Used to dynamically create trunks 
    Vulnerability: ON by default, can send crafted messages to form VLAN trunk link.
    Recommended to disable DTP negotiations and manually assign access or trunk


# CDP, FDP AND LLDP
    Vulnerabilities
        Leaks valuable information
        clear text
        Enabled by default
        disable it
            Globably 
            per instance
        May require it for VOIP
# STP (Spanning Tree Protocol)
    Root Decision Process
        1. Elect Root Bridge 
        2. Identify the root port on the non-root bridge
        3, Indetify the designated port for each segment
        4. set the alternate ports to blocking state
    Types:
        802.1D STP
        Per VLAN ST+ (PVST+)
        (RSTP)
        (RPSTP+)
        802.1s (Mulitple Spanning Tree)
    Attack:
        Crafted bridge protocol data units (BPDU)
        Used to preform a DoS or MitM
# Port Security Modes
    Shutdown(default)
    Protect
    Restrict





























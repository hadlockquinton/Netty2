# Day 1 
Protocol Analysis... Easy as shit my boy.


# Day 2
| Question | Answer        |
| ----------| ----------        |
| Filter ipv4 and at least the don't fragment bit set | ip[6] & 0x40 = 0x40        |
| Filter ipv4 and ipv6 with ttl's of 64 or less | 'ip[8] <= 64 \|\| ip6[7] <= 64'        |
| Filter srcprt higher than 1024 | tcp[0:2] > 1024 \|\| udp[0:2] > 1024        |
| Filter for ipv4 and ipv6 with UDP as the next protocol | ip[9] =0x11 \|\| ip6[6] = 0x11        |
| Filter for ack/rst or ack/fin flags set in tcp | tcp[13] = 0x14 \|\| tcp[13] = 0x11        |
| Filter for ipv4 ID field of 213 | ip[4:2] = 0xd5        |
| Filter for Ethernet Vlan Tag | ether[12:2] = 0x8100        |
| Filter for all DNS packets | udp[0:2] = 53 \|\| udp[2:2] = 53 \|\| tcp[0:2] = 53 \|\| tcp[2:2] = 53        |
| Filter for all TCP syn packets | tcp[13] = 0x02        |
| Filter for all TCP syn/ack packets | tcp[13] = 0x12        |
| Filter for Rst packets | tcp[13] = 0x04        |
| Filter for dst ports in the well known range | tcp[2:2] < 1024 \|\| udp[2:2] < 1024        |
| Filter for all http traffic | tcp[0:2] = 80 \|\| tcp[2:2] = 80        |
| Filter for all telnet traffic | tcp[0:2] = 23 \|\| tcp[2:2] = 23        |
| Filter for all Arp traffic | arp        |
| Filter for all arp(efficiently I guess) | ether[12:2] = 0x0806        |
| Filter for the Evil/Reserved bit set | ip[6] & 0x80 = 0x80        |
| Filter for Chaos Protocol | ip[9] = 0x10        |
| Filter for DSCP field of 37 | ip[1] >>2 = 37        |
| Filter for Urg bit not set and Urg pointer with a value | tcp[18:2] != 0 && tcp[13] & 0x20 = 0        |
| Filter for Dst Ip of 10.10.10.10 and null scan(No bits set) | tcp[13] = 0 && ip[16:4] = 0x0a0a0a0a        |
| Filter for VLAN hopping from 1 to 10 | ether[12:4]&0xffff0fff = 0x81000001 && ether[16:4]&0xffff0fff = 0x8100000A        |

# Day 3 
| Question | Answer  |
| ---------- | ----------  |
| 3 Address Families associated with the python3 socket module? | socket.AF_INET, socket.AF_INET6, socket.AF_UNIX  |
| Socket Functions to open and close a connection | socket.connect(), socket.close()  |
| What library is used to combine various peices of the packet into network order? | struct.pack  |
| What must be created for the raw socket that stream and datagram sockets create for you? | Header  |
| within the socket module allows you to Send data to a socket, while not already being connected to a remote socket? | socket.sendto()  |
| two required items needed to be set in order to send a Datagram or Stream socket | ipaddr port  |
| what must a string be converted to before being sent due to encoding? | bytes-like object  |
| 


# Day 7
| Question | Answer |
| -- | -- |
| Universal Plug n Play filter | ssdp |









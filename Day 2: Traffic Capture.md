<h2> Oh brother, we about to go into all this shit</h2>

##### NoteyNotes
        AXFR : Zone transfer
        ftp-data : finds the data that is used in ftp, I guess. thank you thomas
        tcp.port eq 443 and ip contains "http" : gives all the ssl bullshit
        server of SNMP : It will be the system doing the get-request


#### 
        tcpdump {A} [B:C] {D} {E} {F} {G}
        A = Protocol ( ether | arp | ip | ip6 | icmp | tcp | udp )
        B = Header Byte number
        C = optional: Byte Length. Can be 1, 2 or 4 (default 1)
        D = optional: Bitwise mask (&)
        E = Relational operator ( = | == | > | < | <= | >= | != | () | << | >> )
        F = Result of Expression
        G = optional: Logical Operator (&& ||) to bridge expressions

# Berkley Packet Filters, CTF answers 
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






        

# Traffic Captures
###### Or some shit

### Practical uses
    Network Trouble shooting 
    Improper switching 
    Port/Protocol misconfigurations
    Monitor network consumption
    Intercepting usernames and passwords 
    Eavesdropping
#### Disadvantages
      Requires elevated perms
      can only capture what the NIC can see
      cannot capture local traffic 
      can consume massive amounts of system resources
      Lost packets on a busy network

### Capture packets in two ways
    Software and hardware based sniffers

#### Socket types 
      User space sockets 
        stream sockets - TCP
        datagram sockets - UDP
      Kernal space sockets 
        RAW sockets
# Captjure library
  Requires root for 
    Promiscuous Mode 
    All captured packets are created as raw sockets 
![image](https://github.com/user-attachments/assets/a4855705-1f06-4a95-ab70-86b617ada912)


#### Types of sniffing 
      Active and Passive 

#### Interface Naming 
      Trad Wife 
        Eth0, Eth1/1
      Consistent 
        eno1, ens3
  
# TCP Dump 
  ##### Basic options
          -A : Print payload in ASCII
          -D : list interfaces 
          -i : specify capture interface 
          -e : Print data-link header s
          -X or XX : Print Payload in HEX and ASCII
          -w : write to pcap
          -r : read from pcap
          -v, vv, or vvv : verbose
          -n : no inverse lookups 

#### Operators 
      and or &&
      or or ||
      not or !
      < or <=
      > or >=
      = or == or !=

##### Hella BerkPackFilterShit
        yap yap yap yap


#### Passive OS Fingerprinting 
      Similar to TCPDump, except it only captures traffic that matches signatures on its database 
        
###### Searches for specific Signatures in:
        Most OS's
        Most Browsers
        Search Robots
        Commandline tools

##### Signature Database 
        /etc/p0f/p0f.fp
        p0f -h : for the help page
        p0f -i eth0 : ran on an interface 
        p0f pr capture.pcap : run p0f on a pcap

##### Output to greppable log
      p0f -r wget.pcap -o /var/log/p0f.log
      cat /var/log/p0f.log | grep ""
        
















































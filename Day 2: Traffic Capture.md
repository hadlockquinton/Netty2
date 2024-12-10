<h2> Oh brother, we about to go into all this shit</h2>

##### NoteyNotes
        AXFR : Zone transfer
        ftp-data : finds the data that is used in ftp, I guess. thank you thomas
        

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
        
















































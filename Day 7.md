# NettyWorky analysis

## Sensors
    In-line
        Test acess point(tap)
        MitM
    Out of band(passive)
        Switched port analyzer

    In-line
        In between two communicating devices to stop attacks
        IPS
        Firewall
    Passive sensor
        Can detect, cannot stop attacks
        IDS
    

# Known Windows and linux ports
    Windows
        88:Kerberos/DC
        137/138/139:Net BIOS
        445:SMB
    Linux
        22:SSH
        111:SUN RPC
    
    IANA 49152–65535
    Linux 32768–60999
    Windows XP 1025–5000
    Win 7/8/10 use IANA
    Win Server 2008 1025–60000
    Sun Solaris 32768–65535

    PASSIVE OS FINGERPRINTING
        /etc/p0f/p0f.fp

# HACKER methodologies
    Footprinting
    Network scanning
    Network Enumeration
    Vulnerability Assessment

![image](https://github.com/user-attachments/assets/4a09f3db-3349-49c1-ad2c-566b1efb622d)
![image](https://github.com/user-attachments/assets/d1254598-8cae-4021-ae04-869d3ed227bf)
![image](https://github.com/user-attachments/assets/a15b93c6-2615-462a-b41f-37bbe6a23bc1)
![image](https://github.com/user-attachments/assets/00eaa2fd-a4b7-48c1-a5b7-669adc2d22d2)
![image](https://github.com/user-attachments/assets/5b1bb2e8-f95d-4f50-8153-76dff13a26b1)


# Indicators of attack
    
    .exe/executable files
    NOP sled
    Repeated Letters
    Well Known Signatures
    Mismatched Protocols
    Unusual traffic
    Large amounts of traffic/ unusual times

### Signs of IOA
    Destination IP/Ports
    Public Servers/DMZs
    Off-Hours
    Network Scans
    Alarm Events
    Malware Reinfection
    Remote logins
    High amounts of some protocols
### Signs of IOC
    Unusual traffic outbound
    Anomalous user login or account use
    Size of responses for HTML
    High number of requests for the same files
    Using non-standard ports/ application-port mismatch
    Writing changes to the registry/system files
    Unexpected/unusual patching or tasks
# Types of malware
    Adware/Spyware
        large amounts of traffic/ unusual traffic
        IOA
            Destinations
        IOC
            Unusual traffic outbound
    Virus
        phishing/ watering hole
        IOA
            Alarm Events, Email protocols
        IOC
            Changes to the registry/ system files
        Worm
        phishing/ watering hole
        IOA
            Alarm events
        IOC
            changes to registry/ system files
    Trojan
        beaconing
        IOA
            Destinations
        IOC
            Unusual traffic outbound, unusual tasks, changes to registry/ system files
    Rootkit
        IOA
            Malware reinfection   
        IOC
            Anomalous user login/ account use
    Backdoor
        IOA
            Remote logins
        IOC
            Anomalous user login/ account use
    Botnets
        large amounts of IPs
        IOA
            Destinations, remote logins
        IOC
            Unusual tasks, anomalous user login/ account uses
    Polymorphic/Metamorphic Malware
        Depends on the malware type/class
    Ransomware
        IOA
            Destinations, Ports, Malware reinfection
        IOC
            Unusual traffic outbound, non-standard ports, unusual tasks
    Mobile Code
        IOA
            Depends on the malware type/class
    BIOS/Firmware Malware
        IOA
            Malware reinfection
        IOC
            Depends on the malware type/class












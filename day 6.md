# SSH Tunneling and covert Tunnels
    Tunneling - Tunneling encapsulates a protocol inside another protocol.
        Encapsulation
        Transmission
        Decapsulation
# Covert Channels
    Using common and legitimate protocols to transfer data in illegitimate ways
    Unauthorized communication bewteen entities
    Transmits data contrary to design intent
    bypass security, violates policy, leak sensitive information

    Type of covert channel
        Storage
            payload
            header
                tcp header
                ip header
        Timing
            modifying transmission of legitimate traffic
            delaying packets 
            watch ttl changes
            
    Common protocols
        icmp
        dns
        http

# How to detect covert channels
    Host analysis
    Network analysis
    Baselining

    Detecting covert channels with ICMP
        Works with type 8, code 0 'request', type 0 code 0 'answer'
        Check for payload imbalance 
                  request/responce imbalance
                  large payloads

    Detecting covert channels with DNS
        DNS is a request/response protocol
        1 request typically gets 1 response
        payload does NOT exceed 512 bytes, normally
        check for imbalances
            unusual payloads
            burstiness


    Detecting covert channels with HTTP
        request/response protocol
        typically "bursty" but not steady
        

    steganography
        Hiding messages inside legitimate information
            methods
                injection 
                    Done by inserting messages into the unused (whitespace) of the file, usually, graffic
                    Second most common method
                    adds size to file
                    hard to detect unless you have the original
                subsitution
                    Done by inserting message into the insignificant portion of the file
                    most common method used 
                    elements with a digital medium are replaced with hidden information
                propagation
                    generally creates a new file entirely
                    needs special software

# Secure shell
### SECURE THAT HAPPY DAPPY SMILE HOE
:hand: Stupid :hand: stupid :hand: stupid :hand: bitch!

# Ssh Port forwarding 
    Allows for tunneling of other services through ssh
    provides insecure services encryption
    SSH options 
        -L Creates port on the client mapped to a ip:port via the server 
        -D creates a port on the client ans sets up a socks4 proxy channel where the target ip:port is specified dynamically
        -R Creates the port on the server mapped to a ip:port via the client
        -NT do not execute a remote command and diable pseudo-tty

    
    

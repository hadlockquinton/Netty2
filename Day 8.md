![image](https://github.com/user-attachments/assets/dab33daa-0b29-4f11-9079-31d8523d88b6)
  Routed uses layer 3, ip addresses

  Transparent uses layer 2, mac addr

# Common iptable options

    -t - Specifies the table. (Default is filter)
    -A - Appends a rule to the end of the list or below specified rule
    -I - Inserts the rule at the top of the list or above specified rule
    -R - Replaces a rule at the specified rule number
    -D - Deletes a rule at the specified rule number
    -F - Flushes the rules in the selected chain
    -L - Lists the rules in the selected chain using standard formatting
    -S - Lists the rules in the selected chain without standard formatting
    -P - Sets the default policy for the selected chain
    -n - Disables inverse lookups when listing rules
    --line-numbers - Prints the rule number when listing rules
    -p - Specifies the protocol
    -i - Specifies the input interface
    -o - Specifies the output interface
    --sport - Specifies the source port
    --dport - Specifies the destination port
    -s - Specifies the source IP
    -d - Specifies the destination IP
    -j - Specifies the jump target action
    -i [ iface ]
    -o [ iface ]    
    -s [ ip.add | network/CIDR ]    
    -d [ ip.add | network/CIDR ]
    -p icmp [ --icmp-type type# { /code# } ]
    -p tcp [ --sport | --dport { port1 |  port1:port2 } ]
    -p tcp [ --tcp-flags SYN,ACK,PSH,RST,FIN,URG,ALL,NONE ]
    -p udp [ --sport | --dport { port1 | port1:port2 } ]
    -m to enable iptables extensions:
    -m state --state NEW,ESTABLISHED,RELATED,UNTRACKED,INVALID
    -m mac [ --mac-source | --mac-destination ] [mac]
    -p [tcp|udp] -m multiport [ --dports | --sports | --ports { port1 | port1:port15 } ]
    -m bpf --bytecode [ 'bytecode' ]
    -m iprange [ --src-range | --dst-range { ip1-ip2 } ]
    
        Flush table
    iptables -t [table] -F
    Change default policy
    iptables -t [table] -P [chain] [action]
    Lists rules with rule numbers
    iptables -t [table] -L --line-numbers
    Lists rules as commands interpreted by the system
    iptables -t [table] -S



# NFT Table

    nft add table [family] [table]
    nft add chain [family] [table] [chain] { type [type] hook [hook] priority [priority] \; policy [policy] \;}
    nft add rule [family] [table] [chain] [matches (matches)] [statement]

    
    ip [ saddr | daddr { ip | ip1-ip2 | ip/CIDR | ip1, ip2, ip3 } ]
    tcp flags { syn, ack, psh, rst, fin }
    tcp [ sport | dport { port1 | port1-port2 | port1, port2, port3 } ]
    udp [ sport| dport { port1 | port1-port2 | port1, port2, port3 } ]
    icmp [ type | code { type# | code# } ]
    

    nft { list | flush } ruleset
    nft { delete | list | flush } table [family] [table]
    nft { delete | list | flush } chain [family] [table] [chain]    
    List table with handle numbers    
    nft list table [family] [table] [-a]    
    Adds after position    
    nft add rule [family] [table] [chain] [position <position>] [matches] [statement]   
    Inserts before position   
    nft insert rule [family] [table] [chain] [position <position>] [matches] [statement]   
    Replaces rule at handle    
    nft replace rule [family] [table] [chain] [handle <handle>] [matches] [statement]    
    Deletes rule at handle  
    nft delete rule [family] [table] [chain] [handle <handle>]























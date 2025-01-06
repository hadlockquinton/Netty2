# Remote localhost: from the perspective of my box

# local localost: From the perspective of the ssh

# Ping sweep    
    for i in {1..254}; do (ping -c 1 192.168.65.$i | grep "bytes from" &) ; done


Float

    "Student#: student5"

    Command: ssh student@10.50.32.232 -X

    Password: password



# [CTF Page] http://networking-ctfd-1.server.vta:8000/user
# [Network Page] https://git.cybbh.space/CCTC/students


####    Q: What the hell is a float? 
    A:
####   Q: How many points to pass? Bare ass miniumum.
    A: 1770 points
####   Q: What OS is relavant?
    A: Linux Kung FU! 
#### How about you do some real work huh?
    echo -n "#### hostname: " ; hostname ; echo "####TCP Connections ####" ; ss -ntlp ; echo "#### UDP connections ####" ; ss -nulp ; echo "#### Interfaces ####" ; ip addr


| BV | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| -- | -- | -- | -- | -- | -- | -- | -- | -- |
| SNM | 128 | 192 | 224 | 240 | 248 | 252 | 254 | 255 | 
| Class A | /1 | /2 | /3 | /4 | /5 | /6 | /7 | /8 |
| Class B | /9 | /10 | /11 | /12 | /13 | /14 | /15 | /16 |
| Class C | /17 | /18 | /19 | /20 | /21 | /22 | /23 | /24 |
| Class D | /25 | /26 | /27 | /28 | /29 | /30 | /31 | /32 |


## Tunneling day 1

    ssh sokka@float -L 1111:192.168.1.39:22

    ssh Sokka@localhost -p 1111 -D 9050     #Terminate later

    ssh aang@localhost -p 1111 -L 1112:10.0.0.50:22

    ssh katara@localhost -p 1112 -D 9050   #Terminate Later

    ssh katara@localhost -p 1112 -L 1113:172.16.1.8:22

    ssh -D 9050 Toph@localhost -p 1113 -D 9050 



## Tunneling day 2
    10.50.24.223
    telnet Rick 23
        ssh IH@Float IP -R 1111:localhost:22
        ssh Rick@localhost -p 1111
        
    ssh Rick@localhost -p 1111 -L 3333:MortyFloat:2222
        Test: ssh Morty@localhost -p 3333

    ssh Morty@localhost -p 3333 -L 4444:JerryFLoat:2323
        Test: ssh Jerry@localhost -p 4444

    ssh Jerry@localhost -p 4444 -L 5555:BethFloat:22
        Test: ssh Beth@localhost -p 5555 -D 9050
        proxychains nc localhost 54321


# Tunneling day 3
    10.50.20.10

    ssh Bender@:10.50.20.10 -p 1234 -L 1111:172.17.17.28:23
    telnet localhost 1111
    ssh Bender@172.17.17.17 -p 1234 -R 2222:localhost:4321
    ssh Bender@10.50.20.10 -p 1234 -L 3333:localhost:2222
        ssh Philip@localhost -p 3333 -D 9050
    ssh Philip@localhost -p 3333 -L 4444:192.168.30.150:1212
        ssh Leela@localhost -p 44444
    ssh Leela@localhost -p 4444 -L 5555:10.10.12.121:2932
        ssh Professor@localhost -p 5555 -D 9050

# Tunelling day 4
    telnet float 23
        ssh student@10.50.32.232 -R 1001:localhost:22
    ssh Eric@localhost -p 1001 -L 1002:192.168.100.60:22
    ssh Kenny@localhost -p 1002 -L 1003:10.90.50.140:6481
    ssh Kyle@localhost -p 1003 -L 1004:172.20.21.5:23
    telnet localhost 1004
        ssh Kyle@172.20.21.4 -R 1005:localhost:22
    ssh Kyle@localhost -p 1003 -L 1006:localhost:1005
    ssh Stan@localhost -p 1006

# Tunneling Day 5
    ssh Sterling@floatip -L 1000:10.1.2.200:23 
    telnet localhost 1000
        ssh Sterling@10.1.2.130 -R 1001:localhost:8976
    ssh sterling@floatip -L 1002:localhost:1001
    ssh Lana@localhost -p 1002 -L 1003:10.2.5.20:22
    ssh Cheryl@localhost -p 1003 -L 1004:10.3.9.39:23 
    telnet localhost 1004
        ssh Cheryl@10.3.9.33 -R 2000:localhost:3597
    ssh Cheryl@localhost -p 1003 -L 1005:localhost:2000
    ssh Malory@localhost -p 1005
























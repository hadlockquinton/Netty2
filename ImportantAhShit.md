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
        ssh Morty@localhost -p 3333

    ssh Morty@localhost -p 3333 -L 4444:JerryFLoat:2323
        ssh Jerry@localhost

    ssh Jerry@localhost -p 4444 -L 5555:BethFloat:22
        ssh Beth@localhost -p 5555









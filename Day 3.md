
# Notes
    ss -ntlp - Lists all the tcp sockets
    
    ss -nulp - lists all the udp sockets
  

# Sockets

  **Stream** Sockets - Connection oriented and sequenced; methods for connection establishment and tear-down. Used with TCP, SCTP, and Bluetooth.
  
  **Datagram** Sockets - Connectionless; designed for quickly sending and receiving data. Used with UDP.
  
  **RAW** Sockets - Direct sending and receiving of IP packets without automatic protocol-specific formatting.

# Python 
Libraries
        Modules
            Functions 
            Exceptions 
            Constants
            Objects 
            List[] vs Tuple()

Uses strings and integers 
    Built in Functions 
        Int - Convert to int
        len - get the length
        str - convert to string
        sum - get the sum of two int or strings
        Print - print to string
    Built in Methods
        my_string.upper
        my_string.lower
        my_string.split
        my_string.append
        my_string.insert
    Imports
        Import {module}
        import {module} as {name}
        from {module} import *
        from {module} import {function}
        from {module} import {function} as {name}

# Socket Python Library
Import socket - uploads/imports the socket library.
socket.socket( *family*, *type*, *proto* )
    


# Ecoding vs Encyription
![image](https://github.com/user-attachments/assets/6a9484bc-3b01-478c-be3a-1298a3bcd80a)

Encrypt - Scrambles data to make it unreadable without the secret key
Encoding - Converts data into a different format 

HEX encoding/decoding 
    Encode to HEX 
        echo "message" | xxd
    Encode file to hex
        xxd file.txt file-encoded.txt
    Decode File from HEX
        xxd -r file-encoded.txt file-decoded.txt
Base 64 encoding/decoding
    Encode to Base 64
        echo "message" | base64
    Encode file to base64
        base64 file.txt > file-encoded.txt
    Decode file from Base64
        base64 -d file-encoded.txt > file-decoded.txt
        


























  

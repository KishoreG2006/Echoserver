# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
    Client.py
    import socket
     HOST = "127.0.0.1" 
    PORT = 65432  
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
     s.connect((HOST, PORT))
     s.sendall(b"KISHORE G.,  212223040099")
     data = s.recv(1024)
     print(f"Received {data!r}")


     
     Server.py
     import socket
     HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
     PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
    
    
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
        s.bind((HOST, PORT))
        s.listen()
        conn, addr = s.accept()
        with conn:
            print(f"Connected by {addr}")
            while True:
                data = conn.recv(1024)
                if not data:
                    break
                conn.sendall(data)

## OUTPUT:
![WhatsApp Image 2025-03-06 at 11 52 15_f7ec3f78](https://github.com/user-attachments/assets/dffcc1b4-25fe-4165-884c-ed05eaa0091d)



![WhatsApp Image 2025-03-06 at 11 52 15_57ea7e17](https://github.com/user-attachments/assets/8dc0fa3b-43f9-459d-83a8-ce5f7b2394e8)



## RESULT:
The program is executed successfully

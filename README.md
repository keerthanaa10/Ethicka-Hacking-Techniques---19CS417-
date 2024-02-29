# Ethicka-Hacking-Techniques---19CS417-
Ethicka Hacking Techniques - 19CS417 
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
**server.py:**
```import socket
HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024).decode()
            if not data:
                break
            conn.sendall(data.encode())
```     
**client.py:**
```import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    while True:
       s.sendall(input().encode()) 
       data = s.recv(1024).decode()
       print(f"Received {data!r}")
```

## OUTPUT:
**server.py**
```
![ETH_exp1a1](https://github.com/keerthanaa10/Ethicka-Hacking-Techniques---19CS417-/assets/132996371/e472ae10-b856-465d-97d3-2df820c8529d)

**client.py**
```
![ETH_exp1b1](https://github.com/keerthanaa10/Ethicka-Hacking-Techniques---19CS417-/assets/132996371/6ef3d8a8-8723-4d79-82bb-089507b9f0da)


## RESULT:
The program is executed successfully

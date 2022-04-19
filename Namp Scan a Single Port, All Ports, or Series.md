# Scan port 80 on the target system:

nmap –p 80 192.168.0.1

# Scan ports 1 through 200 on the target system:

nmap –p 1-200 192.168.0.1

## Scan (Fast) the most common ports:

nmap –F 192.168.0.1

## To scan all ports (1 – 65535):

nmap –p– 192.168.0.1 

# TunnelVision
Proxy-aware port scanner designed for red teamers and operators navigating internal networks through SOCKS proxies. 
For when nmap scanning shows open|filtered no matter what.

# How to use

python3 portscan.py -h                                                                                                                               
usage: portscan.py [-h] (--top-ports | --all-ports | --port PORT) [--filter {open,all}] [--output OUTPUT] [--banners] target

```
🛠 ProxyChains Port Scanner with Banner Grabbing

positional arguments:
  target               Target IP or hostname to scan

options:
  -h, --help           show this help message and exit
  --top-ports          Scan top 1000 ports
  --all-ports          Scan all 65535 ports
  --port PORT          Scan a single port
  --filter {open,all}  Filter output (default: all)
  --output OUTPUT      Write open ports and banners to file
  --banners            Attempt to grab service banners
```

# Example usage

```
python3 portscan.py 10.0.4.75 --all-ports --filter open                                              
[*] Scanning 65535 ports on 10.0.4.75...

[+] 135/tcp open                                                       
[+] 139/tcp open                                                       
[+] 445/tcp open                                                       
[+] 5040/tcp open                                                      
[+] 5985/tcp open                                                      
Scanning:  23%|███▊             | 14766/65535 [05:50<20:40, 40.93it/s
```

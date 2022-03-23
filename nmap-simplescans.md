nmap -sP 10.0.0.0/24  
Ping scans the network, listing machines that respond to ping.  

nmap -p- -sV -sS -T4 target  
Full TCP port scan using with service version detection - usually my first scan, I find T4 more accurate than T5 and still "pretty quick".  

nmap -v -sS -A -T4 target  
Prints verbose output, runs stealth syn scan, T4 timing, OS and version detection + traceroute and scripts against target services.  

nmap -v -sS -A -T5 target  
Prints verbose output, runs stealth syn scan, T5 timing, OS and version detection + traceroute and scripts against target services.  

nmap -v -sV -O -sS -T5 target  
Prints verbose output, runs stealth syn scan, T5 timing, OS and version detection.  

nmap -v -p 1-65535 -sV -O -sS -T4 target  
Prints verbose output, runs stealth syn scan, T4 timing, OS and version detection + full port range scan.  

nmap -v -p 1-65535 -sV -O -sS -T5 target  
Prints verbose output, runs stealth syn scan, T5 timing, OS and version detection + full port range scan.  
Agressive scan timings are faster, but could yeild inaccurate results!  
T5 uses very aggressive scan timings and could lead to missed ports, T4 is a better compromise if you need fast results.  

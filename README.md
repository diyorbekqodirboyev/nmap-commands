# Nmap Commands

### Basic Scans:
1. **Scan a single IP**:  
   `nmap 192.168.1.1`
   
2. **Scan a host**:  
   `nmap example.com`
   
3. **Scan a range of IPs**:  
   `nmap 192.168.1.1-20`
   
4. **Scan a subnet**:  
   `nmap 192.168.1.0/24`
   
5. **Scan multiple IPs or subnets**:  
   `nmap 192.168.1.1 192.168.1.2 192.168.2.0/24`
   
6. **Scan from a file containing IPs/subnets**:  
   `nmap -iL targets.txt`

### Port Scanning:
7. **Scan specific ports**:  
   `nmap -p 80,443 192.168.1.1`
   
8. **Scan a range of ports**:  
   `nmap -p 1-100 192.168.1.1`
   
9. **Scan all 65535 ports**:  
   `nmap -p- 192.168.1.1`
   
10. **Scan commonly used ports (default)**:  
    `nmap 192.168.1.1`
    
11. **Scan top 100 most common ports**:  
    `nmap --top-ports 100 192.168.1.1`
    
12. **Scan a specific port**:  
    `nmap -p 22 192.168.1.1`

### Service Version Detection:
13. **Detect service versions**:  
    `nmap -sV 192.168.1.1`
    
14. **Intense service version detection**:  
    `nmap -sV --version-intensity 5 192.168.1.1`
    
15. **Try all probes to detect service version**:  
    `nmap -sV --version-all 192.168.1.1`

### OS Detection:
16. **Detect OS**:  
    `nmap -O 192.168.1.1`
    
17. **Aggressive OS detection**:  
    `nmap -O --osscan-guess 192.168.1.1`
    
18. **Scan OS and services**:  
    `nmap -A 192.168.1.1`

### Script Scanning:
19. **Run default scripts**:  
    `nmap -sC 192.168.1.1`
    
20. **Run a specific script**:  
    `nmap --script=http-title 192.168.1.1`
    
21. **Run multiple scripts**:  
    `nmap --script=http-title,http-headers 192.168.1.1`
    
22. **Run all available scripts**:  
    `nmap --script=all 192.168.1.1`
    
23. **Scan with safe scripts**:  
    `nmap --script=safe 192.168.1.1`

### Scan Techniques:
24. **TCP connect scan**:  
    `nmap -sT 192.168.1.1`
    
25. **SYN scan (default)**:  
    `nmap -sS 192.168.1.1`
    
26. **UDP scan**:  
    `nmap -sU 192.168.1.1`
    
27. **TCP ACK scan**:  
    `nmap -sA 192.168.1.1`
    
28. **Window scan**:  
    `nmap -sW 192.168.1.1`
    
29. **FIN scan**:  
    `nmap -sF 192.168.1.1`
    
30. **XMAS scan**:  
    `nmap -sX 192.168.1.1`
    
31. **NULL scan**:  
    `nmap -sN 192.168.1.1`

### Advanced Scans:
32. **Scan using IP protocol**:  
    `nmap -sO 192.168.1.1`
    
33. **Scan with spoofed IP**:  
    `nmap -S 192.168.1.100 192.168.1.1`
    
34. **Scan with decoys**:  
    `nmap -D RND:10 192.168.1.1`
    
35. **Scan using a different source port**:  
    `nmap --source-port 53 192.168.1.1`
    
36. **Scan using a specific interface**:  
    `nmap -e eth0 192.168.1.1`
    
37. **Scan using IP fragments**:  
    `nmap -f 192.168.1.1`
    
38. **Scan with a custom TTL**:  
    `nmap --ttl 100 192.168.1.1`
    
39. **Scan with a custom MTU**:  
    `nmap --mtu 24 192.168.1.1`
    
40. **Scan with no ping**:  
    `nmap -Pn 192.168.1.1`
    
41. **Scan with TCP ping**:  
    `nmap -PS 192.168.1.1`
    
42. **Scan with ICMP ping**:  
    `nmap -PE 192.168.1.1`
    
43. **Scan with ARP ping**:  
    `nmap -PR 192.168.1.1`
    
44. **Scan with a custom ping**:  
    `nmap -PA 192.168.1.1`

### Output Options:
45. **Normal output**:  
    `nmap -oN scan.txt 192.168.1.1`
    
46. **XML output**:  
    `nmap -oX scan.xml 192.168.1.1`
    
47. **Grepable output**:  
    `nmap -oG scan.gnmap 192.168.1.1`
    
48. **All formats output**:  
    `nmap -oA scan 192.168.1.1`
    
49. **Append output to a file**:  
    `nmap -oN scan.txt --append-output 192.168.1.1`

### Timing and Performance:
50. **Aggressive timing**:  
    `nmap -T4 192.168.1.1`
    
51. **Polite timing**:  
    `nmap -T2 192.168.1.1`
    
52. **Paranoid timing**:  
    `nmap -T0 192.168.1.1`
    
53. **Max parallelism**:  
    `nmap --min-parallelism 100 192.168.1.1`
    
54. **Max RTT timeout**:  
    `nmap --max-rtt-timeout 1000ms 192.168.1.1`

### Firewall

### Firewall Evasion and Bypassing:
55. **Fragment packets to evade firewalls**:  
    `nmap -f 192.168.1.1`
    
56. **Send bad checksums to evade firewalls**:  
    `nmap --badsum 192.168.1.1`
    
57. **Use decoys to evade intrusion detection systems**:  
    `nmap -D RND:10 192.168.1.1`
    
58. **Scan with a spoofed MAC address**:  
    `nmap --spoof-mac 00:11:22:33:44:55 192.168.1.1`
    
59. **Scan using a specific TCP sequence prediction**:  
    `nmap --scanflags SYN 192.168.1.1`
    
60. **Scan with an idle/zombie host**:  
    `nmap -sI zombie_host 192.168.1.1`
    
61. **Scan with IP options**:  
    `nmap --ip-options "R" 192.168.1.1`
    
62. **Append random data to packets**:  
    `nmap --data-length 25 192.168.1.1`
    
63. **Use a specific MTU size**:  
    `nmap --mtu 32 192.168.1.1`
    
64. **Send packets from a specific source port**:  
    `nmap --source-port 53 192.168.1.1`
    
65. **Scan a target without pinging it**:  
    `nmap -Pn 192.168.1.1`

### Target Specification:
66. **Scan using a host list**:  
    `nmap -iL hosts.txt`
    
67. **Exclude targets from a scan**:  
    `nmap 192.168.1.0/24 --exclude 192.168.1.5`
    
68. **Exclude a list of targets from a scan**:  
    `nmap 192.168.1.0/24 --excludefile exclude.txt`
    
69. **Scan IPv6 targets**:  
    `nmap -6 2001:db8::1`
    
70. **Scan random targets from a subnet**:  
    `nmap -iR 10`
    
71. **Scan specific targets with varying verbosity**:  
    `nmap -v -v 192.168.1.1`

### Scan Efficiency:
72. **Scan only open ports**:  
    `nmap --open 192.168.1.1`
    
73. **Scan with a delay between probes**:  
    `nmap --scan-delay 5s 192.168.1.1`
    
74. **Scan with max retries set**:  
    `nmap --max-retries 1 192.168.1.1`
    
75. **Scan with a minimum hostgroup size**:  
    `nmap --min-hostgroup 5 192.168.1.1`
    
76. **Scan with minimum packet rate**:  
    `nmap --min-rate 100 192.168.1.1`
    
77. **Scan with maximum packet rate**:  
    `nmap --max-rate 1000 192.168.1.1`

### Scan Reporting:
78. **Print host interfaces and routes**:  
    `nmap --iflist`
    
79. **Print host network distance**:  
    `nmap --traceroute 192.168.1.1`
    
80. **Print packet debugging info**:  
    `nmap --packet-trace 192.168.1.1`
    
81. **Print host and service version info**:  
    `nmap -sV --version-light 192.168.1.1`
    
82. **Print hosts in a network**:  
    `nmap -sn 192.168.1.0/24`

### Miscellaneous:
83. **Scan with verbosity**:  
    `nmap -v 192.168.1.1`
    
84. **Scan with extra verbosity**:  
    `nmap -vv 192.168.1.1`
    
85. **Scan and display reason for each state**:  
    `nmap --reason 192.168.1.1`
    
86. **Scan with debugging output**:  
    `nmap -d 192.168.1.1`
    
87. **Scan and disable DNS resolution**:  
    `nmap -n 192.168.1.1`
    
88. **Scan and enable DNS resolution**:  
    `nmap -R 192.168.1.1`
    
89. **Scan with random targets**:  
    `nmap -iR 5`
    
90. **Scan with IP randomization**:  
    `nmap -r 192.168.1.0/24`

### Script Scanning and Customization:
91. **Run scripts against multiple targets**:  
    `nmap --script=http-title 192.168.1.1,2,3`
    
92. **Run scripts in custom mode**:  
    `nmap --script-args http.useragent="Mozilla" 192.168.1.1`
    
93. **Run NSE scripts from a directory**:  
    `nmap --script=dir/* 192.168.1.1`
    
94. **Run scripts from a custom location**:  
    `nmap --script="scripts" 192.168.1.1`
    
95. **Run with script and report output**:  
    `nmap --script=http-sql-injection -oN output.txt 192.168.1.1`

### Combination Scans:
96. **Stealth and service version detection**:  
    `nmap -sS -sV 192.168.1.1`
    
97. **Aggressive scan with OS detection**:  
    `nmap -A 192.168.1.1`
    
98. **Scan and perform traceroute**:  
    `nmap -Pn --traceroute 192.168.1.1`
    
99. **Scan and identify vulnerabilities**:  
    `nmap --script vuln 192.168.1.1`
    
100. **Scan with OS detection, version detection, script scanning, and traceroute**:  
    `nmap -A -T4 192.168.1.1`

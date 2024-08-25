Nmap Commands

### Basic Scans:
1. **Scan a single IP**:  
   ```bash
   nmap 192.168.1.1
   ```
   
2. **Scan a host**:  
   ```bash
   nmap example.com
   ```
   
3. **Scan a range of IPs**:  
   ```bash
   nmap 192.168.1.1-20
   ```
   
4. **Scan a subnet**:  
   ```bash
   nmap 192.168.1.0/24
   ```
   
5. **Scan multiple IPs or subnets**:  
   ```bash
   nmap 192.168.1.1 192.168.1.2 192.168.2.0/24
   ```
   
6. **Scan from a file containing IPs/subnets**:  
   ```bash
   nmap -iL targets.txt
   ```

### Port Scanning:
7. **Scan specific ports**:  
   ```bash
   nmap -p 80,443 192.168.1.1
   ```
   
8. **Scan a range of ports**:  
   ```bash
   nmap -p 1-100 192.168.1.1
   ```
   
9. **Scan all 65535 ports**:  
   ```bash
   nmap -p- 192.168.1.1
   ```
   
10. **Scan commonly used ports (default)**:  
    ```bash
    nmap 192.168.1.1
    ```

11. **Scan top 100 most common ports**:  
    ```bash
    nmap --top-ports 100 192.168.1.1
    ```
    
12. **Scan a specific port**:  
    ```bash
    nmap -p 22 192.168.1.1
    ```

### Service Version Detection:
13. **Detect service versions**:  
    ```bash
    nmap -sV 192.168.1.1
    ```
    
14. **Intense service version detection**:  
    ```bash
    nmap -sV --version-intensity 5 192.168.1.1
    ```
    
15. **Try all probes to detect service version**:  
    ```bash
    nmap -sV --version-all 192.168.1.1
    ```

### OS Detection:
16. **Detect OS**:  
    ```bash
    nmap -O 192.168.1.1
    ```
    
17. **Aggressive OS detection**:  
    ```bash
    nmap -O --osscan-guess 192.168.1.1
    ```
    
18. **Scan OS and services**:  
    ```bash
    nmap -A 192.168.1.1
    ```

### Script Scanning:
19. **Run default scripts**:  
    ```bash
    nmap -sC 192.168.1.1
    ```
    
20. **Run a specific script**:  
    ```bash
    nmap --script=http-title 192.168.1.1
    ```
    
21. **Run multiple scripts**:  
    ```bash
    nmap --script=http-title,http-headers 192.168.1.1
    ```
    
22. **Run all available scripts**:  
    ```bash
    nmap --script=all 192.168.1.1
    ```
    
23. **Scan with safe scripts**:  
    ```bash
    nmap --script=safe 192.168.1.1
    ```

### Scan Techniques:
24. **TCP connect scan**:  
    ```bash
    nmap -sT 192.168.1.1
    ```
    
25. **SYN scan (default)**:  
    ```bash
    nmap -sS 192.168.1.1
    ```
    
26. **UDP scan**:  
    ```bash
    nmap -sU 192.168.1.1
    ```
    
27. **TCP ACK scan**:  
    ```bash
    nmap -sA 192.168.1.1
    ```
    
28. **Window scan**:  
    ```bash
    nmap -sW 192.168.1.1
    ```
    
29. **FIN scan**:  
    ```bash
    nmap -sF 192.168.1.1
    ```
    
30. **XMAS scan**:  
    ```bash
    nmap -sX 192.168.1.1
    ```
    
31. **NULL scan**:  
    ```bash
    nmap -sN 192.168.1.1
    ```

### Advanced Scans:
32. **Scan using IP protocol**:  
    ```bash
    nmap -sO 192.168.1.1
    ```
    
33. **Scan with spoofed IP**:  
    ```bash
    nmap -S 192.168.1.100 192.168.1.1
    ```
    
34. **Scan with decoys**:  
    ```bash
    nmap -D RND:10 192.168.1.1
    ```
    
35. **Scan using a different source port**:  
    ```bash
    nmap --source-port 53 192.168.1.1
    ```
    
36. **Scan using a specific interface**:  
    ```bash
    nmap -e eth0 192.168.1.1
    ```
    
37. **Scan using IP fragments**:  
    ```bash
    nmap -f 192.168.1.1
    ```
    
38. **Scan with a custom TTL**:  
    ```bash
    nmap --ttl 100 192.168.1.1
    ```
    
39. **Scan with a custom MTU**:  
    ```bash
    nmap --mtu 24 192.168.1.1
    ```
    
40. **Scan with no ping**:  
    ```bash
    nmap -Pn 192.168.1.1
    ```
    
41. **Scan with TCP ping**:  
    ```bash
    nmap -PS 192.168.1.1
    ```
    
42. **Scan with ICMP ping**:  
    ```bash
    nmap -PE 192.168.1.1
    ```
    
43. **Scan with ARP ping**:  
    ```bash
    nmap -PR 192.168.1.1
    ```
    
44. **Scan with a custom ping**:  
    ```bash
    nmap -PA 192.168.1.1
    ```

### Output Options:
45. **Normal output**:  
    ```bash
    nmap -oN scan.txt 192.168.1.1
    ```
    
46. **XML output**:  
    ```bash
    nmap -oX scan.xml 192.168.1.1
    ```
    
47. **Grepable output**:  
    ```bash
    nmap -oG scan.gnmap 192.168.1.1
    ```
    
48. **All formats output**:  
    ```bash
    nmap -oA scan 192.168.1.1
    ```
    
49. **Append output to a file**:  
    ```bash
    nmap -oN scan.txt --append-output 192.168.1.1
    ```

### Timing and Performance:
50. **Aggressive timing**:  
    ```bash
    nmap -T4 192.168.1.1
    ```
    
51. **Polite timing**:  
    ```bash
    nmap -T2 192.168.1.1
    ```
    
52. **Paranoid timing**:  
    ```bash
    nmap -T0 192.168.1.1
    ```
    
53. **Max parallelism**:  
    ```bash
    nmap --min-parallelism 100 192.168.1.1
    ```
    
54. **Max RTT timeout**:  
    ```bash
    nmap --max-rtt-timeout 1000ms 192.168.1.1
    ```

### Firewall Evasion and Bypassing:
55. **Fragment packets to evade firewalls**:  
    ```bash
    nmap -f 192.168.1.1
    ```
    
56. **Send bad checksums to evade firewalls**:  
    ```bash
    nmap --badsum 192.168.1.1
    ```
    
57. **Use decoys to evade intrusion detection systems**:  
    ```bash
    nmap -D RND:10 192.168.1.1
    ```
    
58. **Scan with a spoofed MAC address**:  
    ```bash
    nmap --spoof-mac 00:11:22:33:44:55 192.168.1.1
    ```
    
59. **Scan using a specific TCP sequence prediction**:  
    ```bash
    nmap --scanflags SYN 192.168.1.1
    ```
    


60. **Use a random source port**:  
    ```bash
    nmap --source-port 53 192.168.1.1
    ```

### Advanced Scanning Techniques:
61. **Scan with a custom TCP window size**:
    ```bash
    nmap --tcp-window 1000 192.168.1.1
    ```

62. **Scan with a specific TTL (Time-to-Live)**:
    ```bash
    nmap --ttl 64 192.168.1.1
    ```

63. **Scan using a different source IP address**:
    ```bash
    nmap -S 192.168.1.100 192.168.1.1
    ```

64. **Scan with a specific source port**:
    ```bash
    nmap --source-port 12345 192.168.1.1
    ```

65. **Scan using random source ports**:
    ```bash
    nmap --source-port RND:1000 192.168.1.1
    ```

66. **Use a different DNS server for reverse DNS resolution**:
    ```bash
    nmap --dns-servers 8.8.8.8 192.168.1.1
    ```

67. **Scan with a custom MTU (Maximum Transmission Unit)**:
    ```bash
    nmap --mtu 1280 192.168.1.1
    ```

68. **Scan with IPv6**:
    ```bash
    nmap -6 2001:db8::1
    ```

69. **Run a ping scan only (no port scan)**:
    ```bash
    nmap -sn 192.168.1.1
    ```

70. **Scan for all open ports on a host**:
    ```bash
    nmap -p- 192.168.1.1
    ```

71. **Perform a traceroute**:
    ```bash
    nmap --traceroute 192.168.1.1
    ```

72. **Perform a service scan with custom timeout**:
    ```bash
    nmap -sV --version-intensity 5 --max-retries 3 192.168.1.1
    ```

### Advanced Output Options:

73. **Save output in all formats (normal, XML, grepable)**:
    ```bash
    nmap -oA all_formats 192.168.1.1
    ```

74. **Save output with human-readable timestamps**:
    ```bash
    nmap -oX scan.xml --xml-time 192.168.1.1
    ```

75. **Save the results to a compressed file**:
    ```bash
    nmap -oX - 192.168.1.1 | gzip > scan.xml.gz
    ```

76. **Generate an HTML report**:
    ```bash
    nmap -oX - 192.168.1.1 | xsltproc -o scan.html
    ```

### Script Scanning:

77. **Run a specific category of scripts (e.g., vuln)**:
    ```bash
    nmap --script=vuln 192.168.1.1
    ```

78. **Run scripts with arguments**:
    ```bash
    nmap --script=http-enum --script-args http-enum.exclude=admin 192.168.1.1
    ```

79. **Use a custom script from a file**:
    ```bash
    nmap --script ./my_custom_script.nse 192.168.1.1
    ```

80. **List all available scripts**:
    ```bash
    nmap --script-help
    ```

### Timing and Performance:

81. **Use a high-speed scan**:
    ```bash
    nmap -T5 192.168.1.1
    ```

82. **Adjust the number of parallel scans**:
    ```bash
    nmap --min-parallelism 10 --max-parallelism 100 192.168.1.1
    ```

83. **Set a maximum number of retries**:
    ```bash
    nmap --max-retries 2 192.168.1.1
    ```

84. **Adjust the scan delay**:
    ```bash
    nmap --scan-delay 100ms 192.168.1.1
    ```

85. **Adjust the host timeout**:
    ```bash
    nmap --host-timeout 30m 192.168.1.1
    ```

### Firewall Evasion and Bypassing:

86. **Use fragmenting to evade firewalls**:
    ```bash
    nmap -f 192.168.1.1
    ```

87. **Send invalid packets to bypass filters**:
    ```bash
    nmap --badsum 192.168.1.1
    ```

88. **Use a decoy scan to hide your IP**:
    ```bash
    nmap -D RND:10 192.168.1.1
    ```

89. **Scan with a spoofed MAC address**:
    ```bash
    nmap --spoof-mac 00:11:22:33:44:55 192.168.1.1
    ```

90. **Use source routing to evade detection**:
    ```bash
    nmap --route 192.168.1.1
    ```

### DNS and Reverse DNS:

91. **Perform a reverse DNS lookup**:
    ```bash
    nmap -sL 192.168.1.1
    ```

92. **Perform a reverse DNS lookup with a custom DNS server**:
    ```bash
    nmap -sL --dns-servers 8.8.8.8 192.168.1.1
    ```

93. **Resolve DNS names while scanning**:
    ```bash
    nmap -R 192.168.1.1
    ```

94. **Scan with custom DNS query**:
    ```bash
    nmap --dns-servers 8.8.8.8 --dns-query 192.168.1.1
    ```

### Host Discovery:

95. **Perform an ARP scan (for local network only)**:
    ```bash
    nmap -PR 192.168.1.0/24
    ```

96. **Perform a ping scan (no port scan)**:
    ```bash
    nmap -sn 192.168.1.1
    ```

97. **Scan with a specific ping type (e.g., ICMP echo request)**:
    ```bash
    nmap -PE 192.168.1.1
    ```

98. **Perform a combined ping and port scan**:
    ```bash
    nmap -sP -p 80 192.168.1.1
    ```

### Miscellaneous:

99. **Use Nmap in verbose mode**:
    ```bash
    nmap -v 192.168.1.1
    ```

100. **Display the scan progress**:
    ```bash
    nmap --progress 192.168.1.1
    ```
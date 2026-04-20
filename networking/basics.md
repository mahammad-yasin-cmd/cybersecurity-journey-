# networking basics 
## whats is network 
- network is a of two or more devices connected each other to share datas 

----------

## whats is types network 
- LAN(LOCAL AREA NETWORK) SMALL AREAS
- WAN(WIDE AREA NETWORK) LARGE ARES 
- MAN(METROPOLITON AREA NETWORK) CITY  LEVEL 
- PAN(PERSONAL AREA NETWORK) PERSONAL DEVICES 
--------
## IP ADDRESS 
- its an identity of each divces on a network to communicate with each other
- eg 192.168.0.1 router ip
- types 1.ipV4 and ipv6
---------
## mac address 
- its help to adentify devices with in a local network
- to send packet from hop to hop
- -----------
## hub , switch , router and bridge 
- hub send packets to all devices connected within network instead of specific device (learn,flood,action)
- switch help to send packet to specific devices by learning the mac address ans port (fe80;e40c;18ff;fe22;da43)
- router help to connect to internet through ip address and help to communicate outside the network(192.168.0.103)
- bridge use to block the packet to go to other side. ( eg- bridge is connected between two hubs and blocks the packet on one side)
- ------------
## DHCP 
- dynamic host configuration protocol helps  to assings ip address within a network . its always assings different ip when connected each time
## DNS 
- first if you type google.com  on browser the request sent to see the chaches if we already involved withit so it can avoid dns if not
  it goes to dns lookup and get the gooogle.com ip as a reply eg - 142.250.80.46
- after that TCP three way handshake occurs SYN- SYN ACK-ACK
- and then tls handshake for secure connection encyption
- send http request to google.com and browser rendres
- ongoing communication
## default gateway 
- its a default gateway of local internet router the ip of the router and through that each device connects
- if you scan that  gateway eg- 192.168.1.1 through nmap it scans every devices connected to the network
# NMAP 
-  i setup a virtual kali machine of virtual box
-  command nmap 192.168.0.0 /24 scan on whole network and the results are
  8 hosts are up , eg on ip 192.168.0.1 ports 21,23,80 and 1900 are open
-
- next  up i ran nmap -v -A -sV 192.168.0.1 AND RESULTS WERE
- i got there version and open ports and os
- Starting Nmap 7.95 ( https://nmap.org ) at 2026-04-20 07:42 EDT
NSE: Loaded 157 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Initiating Ping Scan at 07:42
Scanning 192.168.0.1 [4 ports]
Completed Ping Scan at 07:42, 0.03s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 07:42
Completed Parallel DNS resolution of 1 host. at 07:42, 0.01s elapsed
Initiating SYN Stealth Scan at 07:42
Scanning 192.168.0.1 [1000 ports]
Discovered open port 445/tcp on 192.168.0.1
Discovered open port 21/tcp on 192.168.0.1
Discovered open port 139/tcp on 192.168.0.1
Discovered open port 80/tcp on 192.168.0.1
Discovered open port 1900/tcp on 192.168.0.1
Completed SYN Stealth Scan at 07:42, 1.34s elapsed (1000 total ports)
Initiating Service scan at 07:42
Scanning 5 services on 192.168.0.1
Completed Service scan at 07:42, 11.16s elapsed (5 services on 1 host)
Initiating OS detection (try #1) against 192.168.0.1
Initiating Traceroute at 07:42
Completed Traceroute at 07:42, 0.02s elapsed
Initiating Parallel DNS resolution of 2 hosts. at 07:42
Completed Parallel DNS resolution of 2 hosts. at 07:42, 0.00s elapsed
NSE: Script scanning 192.168.0.1.
Initiating NSE at 07:42
Completed NSE at 07:42, 12.72s elapsed
Initiating NSE at 07:42
Completed NSE at 07:42, 0.09s elapsed
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Nmap scan report for 192.168.0.1
Host is up (0.0065s latency).
Not shown: 994 closed tcp ports (reset)
PORT     STATE    SERVICE     VERSION
21/tcp   open     ftp         vsftpd 2.0.8 or later
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to 192.168.0.102
|      Logged in as admin
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 1
|      vsFTPd 2.3.2 - secure, fast, stable
|_End of status
|_ftp-bounce: bounce working!
|_ftp-anon: Anonymous FTP login allowed (FTP code 230)
23/tcp   filtered telnet
80/tcp   open     http        TP-LINK WAP http config
|_http-title: Site doesn't have a title (text/html; charset=utf-8).
| http-methods: 
|_  Supported Methods: GET POST
139/tcp  open     netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp  open     netbios-ssn Samba smbd 3.0.14a (workgroup: WORKGROUP)
1900/tcp open     upnp        Portable SDK for UPnP devices 1.6.19 (Linux 3.10.14; UPnP 1.0)
Device type: general purpose
Running: Linux 3.X
OS CPE: cpe:/o:linux:linux_kernel:3
OS details: Linux 3.2 - 3.8
Uptime guess: 0.361 days (since Sun Apr 19 23:03:37 2026)
Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=261 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: Host: TP-LINK; OS: Linux; Device: WAP; CPE: cpe:/o:linux:linux_kernel:3.10.14

Host script results:
| smb-os-discovery: 
|   OS: Unix (Samba 3.0.14a)
|   NetBIOS computer name: 
|   Workgroup: WORKGROUP\x00
|_  System time: 2026-04-20T17:12:39+05:30
|_clock-skew: mean: -2h44m59s, deviation: 3h53m20s, median: -5h29m59s
| smb-security-mode: 
|   account_used: guest
|   authentication_level: share (dangerous)
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| nbstat: NetBIOS name: ARCHER_C5, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| Names:
|   ARCHER_C5<00>        Flags: <unique><active>
|   ARCHER_C5<03>        Flags: <unique><active>
|   ARCHER_C5<20>        Flags: <unique><active>
|   \x01\x02__MSBROWSE__\x02<01>  Flags: <group><active>
|   WORKGROUP<00>        Flags: <group><active>
|   WORKGROUP<1d>        Flags: <unique><active>
|_  WORKGROUP<1e>        Flags: <group><active>
|_smb2-time: Protocol negotiation failed (SMB2)

TRACEROUTE (using port 199/tcp)
HOP RTT      ADDRESS
1   10.40 ms 192.168.1.1
2   11.16 ms 192.168.0.1

NSE: Script Post-scanning.
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Initiating NSE at 07:42
Completed NSE at 07:42, 0.00s elapsed
Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 27.59 seconds
           Raw packets sent: 1046 (46.954KB) | Rcvd: 1021 (41.570KB)

   

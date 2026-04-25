## OSI  MODEL 
- it consist of 7 layers 
- apllication
- presentation
- session
- transport
- network
- data link
- physical
- ---------
## physical layer 
- here data present in bytes of o's and 1's
- eg - cables , fibre and etc
# data link layer
- here the mac address are present to perform hop to hop from one place to another also happens arp tp resolve mac address
- eg - nic(network interface card) or wifi where the mac address
## network layer 
- here the ip address are present
- here end - to - end process happens through ip's address of source and destination
- here we can see which protocol is used eg - TCP , UDP and ect.
- called a segment
## session  layer 
- resposible for manaing session between application and other devices
## presentation layer 
- responsible to show the gui interface correctly on corresponing places
## application layer 
- here the protocols like ; HTTP , FTP , SMTP operates
- the last stage of use in application through gui
- -----------------
# TCP/IP MODEL 
- here modern tcp/ip has 5 layers
  5. application
  4. transport
  3. network
  2. data link
  1. physical
## physical  layer 
- hubs , repeaters are present and datas on bytes
## data link layer
- switches
- bridges are present
- its uses mac address on network to communicate
## network layer  
- here the routers are present its uses the ip address to communicate
- its called packets 
## transport layer
- here the ports are present like
- eg - TCP , UDP
- its called a segment
## application
- protocols like
- http
- ftp
- smtp are present here to render
# according to if your sending or receiving packet  
- the packet gets encapsulated
- and decrypt if receiving
- -----------------------
# TCP - transfer configuration protocol
- its a reliable protocol to send data
- its used in
- web -  http , https and etc
- email - smtp
- file transfer - ftp
- its makes a 3-way handshake
- -------------------------
# Three - Way Handshake 
- first the sender initiate conversatoin to start
- SYN      SEQ=1000  [0]bytes
- SYN-ACK  SEQ=3000  [0]bytes ack=1001(seq=1+1)
- ACK      SEQ=1001  [200]bytes ack=3001
- this is how a three way  handshake forms
- --------------------------
# UDP - User Datagram Protocol
- its faster than tcp but not reliable
- no ackowledgement , sequence , 3-way handshake
- its uses port 53 to DNS queries
- eg - streaming and gaming
- ---------------------------
# ARP - adsress resolution protocol 
-  its  used to resolve by finding mac address on local network
-  eg - gateway -192.168.0.1 sends a broadcast who has this ip tell me ?
-  

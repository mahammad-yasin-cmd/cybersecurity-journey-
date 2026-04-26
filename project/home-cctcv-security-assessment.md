# Project - 1 Home CCTV Security Assessment 
- 1. reconnaisance 
  - used nmap to scan my HOME LAB CCTV to see open ports , services , versions and any unusual open ports.
  - code nmap -sV -P -A 192.168.0.103 
- i saw port 80 -http , 554 - RSTP (VIDEO STREAMING) , 37777 - dahua propritary service
- <img width="1920" height="922" alt="Image" src="https://github.com/user-attachments/assets/219a96c0-c123-40ed-88bf-48429af5d95e" />
- a webpage hosting on port 80 http and tried default credentials that dint work 
# 2.Enumeration 
- used gobuster to find the hidden files
- i got /cgi-bin , /config , /index.html
- but there is mo misconfiguration on files amd etc
  ![image alt](https://github.com/mahammad-yasin-cmd/cybersecurity-journey-/blob/74341d3033e26f5d1622e194c7afae019e661d7e/screenshots/Screenshot_2026-04-26_15_46_05.png)
- you can see reference on the picture 
# Burp Suite 
- i used burpsuite to intrude and see info
- as its a post http request
- found user name as admin and password in hash and aslo the cookie value
  ![image alt](https://github.com/mahammad-yasin-cmd/cybersecurity-journey-/blob/25fdb7b4060bf586a802dab9e1c48b7648950e05/screenshots/Screenshot_2026-04-26_16_06_01.png)
- here you can see the pic for reference
- used hashcat to crack  password and its was password123
- we enumurated the infos  but the credentilas were wrong 

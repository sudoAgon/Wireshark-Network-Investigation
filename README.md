A beginner network analysis project using Wireshark.
I captured and analyzed different types of network traffic to understand how common network protocols work.

 -**Protocols Analyzed**

- DNS
- TCP
- HTTP
- ICMP
- ARP
- DHCP

 **Tools**
- Wireshark
- Windows Command Prompt
- Web Browser
- Wi-Fi


 **1. DNS**

DNS translates domain names into IP addresses.

I captured DNS traffic while making a DNS request.

What I observed

- DNS uses UDP port 53
- I captured an A record query
- The A record is used to find an IPv4 address
- I identified the source and destination IP addresses

 Basic process

**2. TCP Three-Way Handshake**

TCP creates a connection using three packets:

SYN -> SYN-ACK -> ACK

What I observed:
SYN starts the connection
SYN-ACK is the server's response
ACK confirms the connection
After this, data can be exchanged


**3. HTTP**

HTTP is used for communication between web browsers and web servers.

I generated HTTP traffic by visiting:
http://neverssl.com

What I observed:

I captured an HTTP request such as:

GET / HTTP/1.1
Host: neverssl.com

I also observed HTTP response codes such as:

200 OK
301 Moved Permanently

HTTP commonly uses TCP port 80.

Basic process:
Browser -> HTTP Request -> Web Server -> HTTP Response


**4. ICMP**

ICMP is commonly used for network testing.

I generated ICMP traffic using:

ping 8.8.8.8

What I observed:

The computer sent an ICMP Echo Request and received an Echo Reply.

Computer -> Echo Request -> 8.8.8.8 -> Echo Reply -> Computer

This shows that the destination was reachable.



**5. ARP**

ARP is used to find the MAC address associated with an IPv4 address on a local network.

What I observed:

The ARP process works like this:
ARP Request:
"Who has this IP?"

ARP Reply:
"This IP is at this MAC address."

The request is broadcast on the local network.


**6. DHCP**

DHCP automatically provides network configuration to devices.

It can provide:

IP address
Subnet mask
Default gateway
DNS server
DHCP Process

DHCP commonly follows the DORA process:

Discover -> Offer -> Request -> Acknowledgement
  
What I observed:

I captured DHCP traffic while renewing my network configuration and observed the DHCP communication between the client and DHCP server.

How These Protocols Work Together:

A simple example of accessing a website is:

DHCP
 ↓
Get network configuration

ARP
 ↓
Find local MAC address

DNS
 ↓
Find the server's IP address

TCP
 ↓
Establish connection

HTTP
 ↓
Exchange web data

ICMP can be used separately to test connectivity.


What I Learned:

Through this project, I learned how to:

-Capture network traffic with Wireshark
-Use Wireshark filters
-Analyze DNS traffic
-Understand TCP SYN, SYN-ACK and ACK
-Analyze HTTP requests and responses
-Use ICMP to test connectivity
-Understand ARP
-Understand DHCP and the DORA process
-Identify source and destination IP addresses
-Analyze packets at different network layers

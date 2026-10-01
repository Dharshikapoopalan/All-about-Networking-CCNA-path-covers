<img width="467" height="339" alt="image" src="https://github.com/user-attachments/assets/a42308c5-65f9-4bde-99e6-0197a6caa3e6" /># All-about-Networking-CCNA-path-covers
All networking concepts to know to become a Network pro

Network Devices

<img width="843" height="327" alt="image" src="https://github.com/user-attachments/assets/ea81d574-e857-4fbb-abfc-a744d9947c42" />

What is a network?
**A computer network is a digital telecommunications network that allows nodes to share resources. **

The building blocks of networks are end devices and network devices.

<img width="566" height="149" alt="image" src="https://github.com/user-attachments/assets/bc434361-08c1-492d-a226-f43ae75b610d" />

1. End Devices

<img width="318" height="206" alt="image" src="https://github.com/user-attachments/assets/5a6300d3-4ed3-4778-bf35-360fe5eef92e" />

End devices are the devices where network communication starts or ends. They either request information, provide information, or communicate with another end device.
Examples include computers, laptops, phones, printers, servers, IP cameras, and IoT devices.

For example:
Laptop → Switch → Router → Internet → Server

The laptop and server are end devices. The switch and router are network devices.

2. Network Devices

Network devices sit between end devices and help connect, forward, control, or protect network traffic.
Examples include switches, routers, bridges, hubs, firewalls, and wireless access points.

Think of it this way:
End devices create/utilize the communication. Network devices help the communication reach its destination.

3. Network Interface Card — NIC

Wireless NICs are placed inside laptops. 
<img width="292" height="242" alt="image" src="https://github.com/user-attachments/assets/6d9f85b4-2366-4961-9dd1-f626f9ba6907" />

Wired: always connected via a cable.
<img width="1280" height="949" alt="Wired Network Interface Card" src="https://github.com/user-attachments/assets/a248fab7-90d4-49c2-b29b-979d020bdec6" />

A Network Interface Card (NIC) is the hardware/interface that allows a device to connect to a network.

For example, when you connect your laptop to a switch using an Ethernet cable, the cable connects to the laptop's Ethernet NIC.
A NIC can be wired, such as Ethernet, or wireless, such as Wi-Fi.

Every network interface normally has a MAC address, which identifies that interface at the Data Link layer.

Example:
Laptop
   |
Ethernet NIC
   |
Ethernet Cable
   |
Switch

**"The NIC is the device's doorway into the network."**

4. Hub
<img width="495" height="294" alt="image" src="https://github.com/user-attachments/assets/ab5b5098-654c-490a-831d-ced174f8d364" />

A hub is a simple networking device that connects multiple devices.

The important thing about a hub is that it doesn't intelligently decide where data should go.

Imagine four computers connected to a hub:

       PC-A
         |
PC-B --- HUB --- PC-C
         |
       PC-D

Suppose PC-A sends data intended for PC-C.

The hub sends that data out to all the other connected ports.

PC-A → HUB
         ├──→ PC-B
         ├──→ PC-C  ✓ intended receiver
         └──→ PC-D

PC-B and PC-D receive it too, even though it wasn't intended for them.

So you can remember:
Hub = Send everywhere.

Hubs are largely obsolete today and have been replaced by switches.

5. Switch

<img width="609" height="225" alt="image" src="https://github.com/user-attachments/assets/a1724917-e61a-48cd-955a-88eb746770b5" />

A switch connects devices within the same local network or LAN.

Unlike a hub, a switch can learn which devices are connected to which ports using MAC addresses.

Imagine:
           SWITCH
        /    |    \
      PC-A  PC-B  PC-C

Suppose:
PC-A MAC = AA:AA
PC-B MAC = BB:BB
PC-C MAC = CC:CC

The switch builds a MAC address table, conceptually like this:

Switch Port	MAC Address
Port 1	AA:AA
Port 2	BB:BB
Port 3	CC:CC


Now if PC-A sends a frame to PC-C, the switch knows:

CC:CC → Port 3

So it can forward the frame toward PC-C rather than sending it everywhere.

A switch connects devices inside a LAN and forwards Ethernet frames based primarily on MAC addresses.

A traditional Layer 2 switch operates mainly at OSI Layer 2 – Data Link Layer.

6. Bridge

<img width="527" height="368" alt="image" src="https://github.com/user-attachments/assets/62c62eb9-5d72-4274-8818-bbf84906aed2" />

A bridge connects network segments and makes forwarding decisions using MAC addresses.

You can think of a bridge as an earlier predecessor to the modern Layer 2 switch.

For example:

Network Segment A
PC1 --- PC2
        |
      BRIDGE
        |
PC3 --- PC4
Network Segment B

The bridge learns which MAC addresses exist on each side and decides whether traffic needs to cross the bridge.

**Bridge = connects LAN segments and filters traffic using MAC addresses.
**

Modern switches essentially perform the same basic Layer 2 bridging function, but at much greater scale and speed with many ports.

7. Router

<img width="467" height="339" alt="image" src="https://github.com/user-attachments/assets/94f051c2-ae0c-41f0-9b34-3470e762ae5a" />

A router connects different IP networks.

This is one of the most important concepts to understand.

A switch commonly connects devices within a network:

192.168.1.10
192.168.1.20
192.168.1.30
      |
    SWITCH

A router allows traffic to travel between networks.

For example:
192.168.1.0/24
      |
    Switch
      |
    Router
      |
   Internet
      |
   Web Server

Routers primarily make forwarding decisions using IP addresses and routing tables.

For example:
Destination: 8.8.8.8

PC
 ↓
Switch
 ↓
Router
 ↓
Internet
 ↓
8.8.8.8

The router checks its ** routing table **to determine where to send the IP packet next.

**A router connects different networks and forwards packets based on IP addresses and its routing table.**

Routers primarily operate at OSI Layer 3 – Network Layer.

Switch vs Router
This distinction is extremely important:

SWITCH

Device ↔ Device
within a LAN
Uses MAC addresses

ROUTER

Network ↔ Network
Uses IP addresses


8. Client

<img width="273" height="180" alt="image" src="https://github.com/user-attachments/assets/04dd7b75-57a8-44ef-a6fa-399b50bbe786" />

A client is a device or application that requests a service or resource.

Suppose you open a browser and enter a website.

Your browser becomes a client:
Your Laptop
    |
 Chrome
 CLIENT
    |
    | "Give me the webpage"
    ↓
Internet
    ↓
Web Server

Clients can request many different services.

For example:
Browser → Web Server

Email application → Mail Server

SSH client → SSH Server

Database client → Database Server

So:
Client = requests/uses a service.

9. Server

A server is a system or application that provides a service or resource to clients.

For example, a web server provides websites.

CLIENT                     SERVER

Laptop                    Web Server
Chrome                    Nginx
   |                         |
   | ---- HTTP Request ----> |
   |                         |
   | <--- HTTP Response ---- |
   |                         |

Different servers provide different services:

Server	What it provides

Web server	Websites/web applications

DNS server	Name-to-IP resolution

DHCP server	IP configuration

File server	Files

Mail server	Email services

Database server	Database services


**Important: client and server describe roles, not necessarily specific types of physical computers. One machine can run client applications and server applications.**

10. Firewall

We have Hardware Firewalls and Software Firewalls.

<img width="880" height="321" alt="image" src="https://github.com/user-attachments/assets/66649667-e991-4b84-a795-28ad08fdc872" />

A firewall controls network traffic according to security rules.

It decides which traffic should be allowed or blocked.

Imagine a company network:

Internet
   |
   ↓
FIREWALL
   |
   ↓
Company Network

Suppose the firewall has rules such as:

Allow HTTPS     TCP 443     ✓
Allow SSH       TCP 22      only from admin network
Block unwanted traffic      ✗

When traffic arrives, the firewall evaluates it against configured policies.

For example:
Internet
   |
   | TCP 443
   ↓
Firewall
   |
   | ALLOW ✓
   ↓
Web Server

But:
Internet
   |
   | Unauthorized traffic
   ↓
Firewall
   |
   X BLOCK

Modern firewalls can inspect much more than simple IP addresses and port numbers, depending on the firewall type.

**A firewall protects networks and systems by allowing or blocking traffic according to security policies.**

An Overview of the concepts discussed.

Imagine you're sitting at home and opening a website:

             YOUR LAPTOP
             End Device
                 |
                NIC
                 |
                 ↓
              SWITCH
                 |
                 ↓
              ROUTER
                 |
                 ↓
             FIREWALL
                 |
                 ↓
             INTERNET
                 |
                 ↓
           WEB SERVER
            End Device

Your browser is the client.

The website's system is the server.

Your NIC connects your device to the network.

The switch connects devices within the LAN.

The router moves packets between different networks.

The firewall controls which traffic is permitted.

The server receives the client's request and sends a response.

One-line memory trick

Component	Remember it as

NIC	Connects a device to the network

Hub	Sends traffic everywhere

Bridge	Connects LAN segments

Switch	Connects devices in a LAN

Router	Connects different networks

Client	Requests a service

Server	Provides a service

Firewall	Allows/blocks traffic
 


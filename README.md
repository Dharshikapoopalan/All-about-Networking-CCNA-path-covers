All networking concepts to know to become a Network pro

Network Devices

<img width="843" height="327" alt="image" src="https://github.com/user-attachments/assets/ea81d574-e857-4fbb-abfc-a744d9947c42" />

What is a network?
**A computer network is a digital telecommunications network that allows nodes to share resources. **

The building blocks of networks are end devices and network devices.

<img width="566" height="149" alt="image" src="https://github.com/user-attachments/assets/bc434361-08c1-492d-a226-f43ae75b610d" />

**1. End Devices**

<img width="318" height="206" alt="image" src="https://github.com/user-attachments/assets/5a6300d3-4ed3-4778-bf35-360fe5eef92e" />

End devices are the devices where network communication starts or ends. They either request information, provide information, or communicate with another end device.
Examples include computers, laptops, phones, printers, servers, IP cameras, and IoT devices.

For example:
Laptop → Switch → Router → Internet → Server

The laptop and server are end devices. The switch and router are network devices.

**2. Network Devices**

Network devices sit between end devices and help connect, forward, control, or protect network traffic.
Examples include switches, routers, bridges, hubs, firewalls, and wireless access points.

Think of it this way:
End devices create/utilize the communication. Network devices help the communication reach its destination.

**3. Network Interface Card — NIC**

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

**4. Hub**

<img width="495" height="294" alt="image" src="https://github.com/user-attachments/assets/ab5b5098-654c-490a-831d-ced174f8d364" />

A hub is a simple networking device that connects multiple devices.

The important thing about a hub is that it doesn't intelligently decide where data should go.

Imagine four computers connected to a hub:

<img width="166" height="121" alt="image" src="https://github.com/user-attachments/assets/7a73d8e4-e11a-48f4-8249-f51c0e17073c" />

Suppose PC-A sends data intended for PC-C.

The hub sends that data out to all the other connected ports.

<img width="280" height="95" alt="image" src="https://github.com/user-attachments/assets/fefdecbd-9b39-47c9-a305-bbee1abc2225" />


PC-B and PC-D receive it too, even though it wasn't intended for them.

So you can remember:
Hub = Send everywhere.

Hubs are largely obsolete today and have been replaced by switches.

**5. Switch**

<img width="609" height="225" alt="image" src="https://github.com/user-attachments/assets/a1724917-e61a-48cd-955a-88eb746770b5" />

A switch connects devices within the same local network or LAN.

Unlike a hub, a switch can learn which devices are connected to which ports using MAC addresses.

Imagine:

<img width="176" height="80" alt="image" src="https://github.com/user-attachments/assets/00e9dbfa-46ed-460b-9c72-b1475a1f9808" />

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

**6. Bridge**

<img width="527" height="368" alt="image" src="https://github.com/user-attachments/assets/62c62eb9-5d72-4274-8818-bbf84906aed2" />

A bridge connects network segments and makes forwarding decisions using MAC addresses.

You can think of a bridge as an earlier predecessor to the modern Layer 2 switch.

For example:

<img width="165" height="155" alt="image" src="https://github.com/user-attachments/assets/77155a44-464f-4137-bff4-763cb9e8fa64" />


The bridge learns which MAC addresses exist on each side and decides whether traffic needs to cross the bridge.

**Bridge = connects LAN segments and filters traffic using MAC addresses.
**

Modern switches essentially perform the same basic Layer 2 bridging function, but at much greater scale and speed with many ports.

**7. Router**

<img width="467" height="339" alt="image" src="https://github.com/user-attachments/assets/94f051c2-ae0c-41f0-9b34-3470e762ae5a" />

A router connects different IP networks.

This is one of the most important concepts to understand.

A switch commonly connects devices within a network:

<img width="113" height="107" alt="image" src="https://github.com/user-attachments/assets/3e380893-ae7f-484d-988e-21e052b573f0" />


A router allows traffic to travel between networks.

For example:

<img width="131" height="193" alt="image" src="https://github.com/user-attachments/assets/a6761126-3b12-4eef-9d13-ecc85afd2db8" />


Routers primarily make forwarding decisions using IP addresses and routing tables.

For example:

<img width="237" height="236" alt="image" src="https://github.com/user-attachments/assets/fa5cadfe-ad7b-42ba-b486-062e09144176" />


The router checks its ** routing table **to determine where to send the IP packet next.

**A router connects different networks and forwards packets based on IP addresses and its routing table.**

Routers primarily operate at OSI Layer 3 – Network Layer.

Switch vs Router
This distinction is extremely important:

<img width="175" height="170" alt="image" src="https://github.com/user-attachments/assets/c19365ff-2e3f-40ad-8872-fc3f8cf28e5c" />


**8. Client**

<img width="273" height="180" alt="image" src="https://github.com/user-attachments/assets/04dd7b75-57a8-44ef-a6fa-399b50bbe786" />

A client is a device or application that requests a service or resource.

Suppose you open a browser and enter a website.

Your browser becomes a client:

<img width="209" height="219" alt="image" src="https://github.com/user-attachments/assets/59127854-2a93-487a-8939-6008ceef2618" />

Clients can request many different services.

For example:

<img width="249" height="100" alt="image" src="https://github.com/user-attachments/assets/2ad000ec-1867-4f9d-af0c-6493fcb5e248" />


So:
Client = requests/uses a service.

**9. Server**

A server is a system or application that provides a service or resource to clients.

For example, a web server provides websites.

<img width="267" height="198" alt="image" src="https://github.com/user-attachments/assets/e1e542a6-f12d-442d-aa97-0f9ff8503c5b" />

Different servers provide different services:

<img width="531" height="317" alt="image" src="https://github.com/user-attachments/assets/9711696c-c1e5-4887-aaad-c93a338c61e8" />

**Important: client and server describe roles, not necessarily specific types of physical computers. One machine can run client applications and server applications.**


**10. Firewall**

We have Hardware Firewalls and Software Firewalls.

<img width="880" height="321" alt="image" src="https://github.com/user-attachments/assets/66649667-e991-4b84-a795-28ad08fdc872" />

<img width="542" height="274" alt="image" src="https://github.com/user-attachments/assets/eed141a0-99e0-4e7d-88ed-268537b6890f" />

A firewall controls network traffic according to security rules.

It decides which traffic should be allowed or blocked.

Imagine a company network:

<img width="142" height="153" alt="image" src="https://github.com/user-attachments/assets/137ed5c0-346e-417f-9aae-e3d30ac8aa62" />


Suppose the firewall has rules such as:

<img width="382" height="75" alt="image" src="https://github.com/user-attachments/assets/6142eb2a-9ea3-4b76-98f0-5ff000dbb293" />


When traffic arrives, the firewall evaluates it against configured policies.

For example:

<img width="154" height="188" alt="image" src="https://github.com/user-attachments/assets/0a84cdf7-d592-491f-acc6-c5a7c3270736" />


But:

<img width="198" height="158" alt="image" src="https://github.com/user-attachments/assets/ee88943c-62f4-4997-bca4-d13c57a54f48" />


Modern firewalls can inspect much more than simple IP addresses and port numbers, depending on the firewall type.

**A firewall protects networks and systems by allowing or blocking traffic according to security policies.**

An Overview of the concepts discussed.


Imagine you're sitting at home and opening a website:

<img width="187" height="372" alt="image" src="https://github.com/user-attachments/assets/a316ba99-6994-40e7-bcf2-e8aa2f23be36" />


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
 


<img width="775" height="282" alt="image" src="https://github.com/user-attachments/assets/d70d5bad-6d7f-4371-aba2-f7d70150bf70" />**How the TCP/IP model actually works**

Internet Protocol Suite

**Protocols & Standards**

A protocol is a set of rules that defines how devices communicate over a network. 

Protocols are the "languages" that computers use to communicate.

Just as someone who only speaks Chinese cannot talk with someone who only speaks English.

Computers that can't speak different protocols can't exchange data. 

-> Since the early days of computer networking, there have been several attempts to define the functions needed for computers to communicate with each other. 

   * Often developed by a specific vendor (e.g., IBM) to be used with their own products.
   * With a proprietary approach, enabling communications between different vendors' products was difficult.

<img width="722" height="139" alt="image" src="https://github.com/user-attachments/assets/4af8dec7-00d5-4ca7-9b09-125a5730e7c9" />

For example: If we have an iMac & an IBM server each using its own proprietary protocols, the IBM server wouldn't be able to understand a request from the iMac.

To solve this issue, **today's networks & devices connect to them using standard vendor-neutral protocols & technologies.**

**A standard is an agreed-upon specification that describes how a protocol or technology should work.**

With vendor-neutral standards, devices of all types can communicate with each other. 
   * An Apple MacBook can access a website hosted on a web server running Linux.
   * A PC running Windows can send an email that can be read on a smartphone running Android.

-> As long as the devices follow standards, they can work together on the network. 

How did TCP/IP come about? 

**A bit of history**

Early work on the computer networks that would evolve into today's Internet began in the 1960s (66 years ago).

The U.S. Department of Defense's ARPA(Advanced Research Projects Agency) funded ARPANET, which came online in 1969 to connect mainframes at universities and labs. 

<img width="424" height="236" alt="image" src="https://github.com/user-attachments/assets/d7fa661b-b076-404b-abe5-64b02735a6a0" />

Here's a map showing ARPANET in the 1970s, connecting locations mostly around the east & west coasts of the country.

ARPANET originally used a protocol called NCP, the Network Control Program. 

There was no TCP/IP in the early days. 

In 1974, Vint Cerf and Bob Khann, two of the fathers of the modern Internet, began developing TCP, Transmission Control Program, as an internetworking protocol. TCP went through a few revisions and was later divided into two protocols that are still used today: 
  * Transmission Control Protocol (TCP)
  * Internet Protocol (IP)

* These two protocols form the foundation of the protocol suite known as TCP/IP today.
    * ARPANET fully switched to TCP/IP on January 1, 1983.
 
Over time, TCP/IP became dominant over vendor-proprietary solutions at the time because it was published as a set of open standards that any vendor could implement, and it could run over many different types of networks. 

And here we are several decades later, still learning about TCP/IP. 

**Who defines the Standard?**

Most networking standards are developed by independent standards organizations, not by a single vendor, with participation from engineers at many companies. 

When it comes to networking, these are two organizations you should be aware of; the first one is:

  **IEEE (The Institute of Electrical and Electronics Engineers)**
  
<img width="253" height="117" alt="image" src="https://github.com/user-attachments/assets/2b9db7ec-9dfa-4749-813b-ef0d4c2b2bad" />

      -> IEEE develops many of the technologies used on local area networks.
      * Such as Ethernet (802.3)
      * Wi-Fi (802.11)
   
    These standards include physical specifications like Ethernet cable types, Wi-Fi radio frequency, and how to           transmit signals over the physical medium, whether a cable or a radio wave.

    But they also specify how to format messages to send them to another device over the medium.

    The second standards group is the: 

 **IETF (Internet Engineering Task Force)**

<img width="400" height="211" alt="image" src="https://github.com/user-attachments/assets/50141bc5-afb0-46c5-8553-b1100635353d" />

     -> An open community that defines protocols used on the Internet. 
     * TCP, IP, UDP, HTTP, DNS, etc.

     -> Publishes standards in documents called RFCs (Requests for Comments) 
     * All of which are freely available on the Internet.

The IEEE and IRTF create the standards, and then vendors like Cisco implement them so that devices from different companies can work together. 

But there are many different standards and protocols.

Each solves a different part of the overall communication problem; to make sense of them, it helps to group their jobs into layers, making a layered model.

**Layered Models**

* Networks do a lot of different jobs to move data from one computer to another.
  * Physical transmission of signals, local delivery on a LAN, routing between networks, end-to-end conversations,         applications themselves.
* A model lets us group related jobs into layers.
  * Each layer has a specific role.
  * Each layer uses the services of the layer below and provides services to the layer above.
* Protocols live(mostly) at one layer. Sometimes the lines are blurred, and it's hard to categorize a protocol.
  * Some examples of protocols that we'll look at later are IP, TCP, and HTTP, etc.
  * Together they form a **stack** of protocols that work as a team(the **network stack**)       

* RFC 791, Internet Protocol, was published in 1981, but it is still the current standard we use today.
**https://www.rfc-editor.org/info/rfc791/**
* We can divide the stack into a few layers like this.
  
<img width="451" height="276" alt="Screenshot (954)" src="https://github.com/user-attachments/assets/16bc6dc3-3fcf-4635-93a0-72587db8dbce" />

  * At the top, we have the application layer, with protocols like Telnet, FTP & TFTP. 
  * Likewise, each of the layers & the protocols in them play a different role in networking. This is the TCP/IP           model. (One version of it)

  * The model is a description, not a law. For example, different textbooks/ courses use slightly different models (4-     layer, 5-layer, etc.)

  * In our lessons, we are going to use the 5-layer model.

Before jumping right into it, let's look at an analogy for this approach. 

<img width="1283" height="383" alt="Screenshot (955)" src="https://github.com/user-attachments/assets/b1574de7-1e13-491b-b39f-87027dea0770" />

Sending a letter to a friend by post. 

* On the left, you are in your house, and on the right, Bob and Bob's wife are in their house. 
* A couple of post offices are connected between their houses. 

<img width="1311" height="328" alt="Screenshot (958)" src="https://github.com/user-attachments/assets/4e33ca88-48ae-435e-857a-bdce9e1aa2b0" />

* You write a letter addressed to your friend, Bob.
* You put the letter in an envelope addressed to Bob's house.
  * Bob's house is a bit far from where you live, so instead of driving directly to his house.
* You deliver the envelope in your cat to post office A.
    * Notice the 3 different destinations:
      * Your car is going to post office A
      * The envelope inside your car is going to Bob's house.
      * The letter inside the envelope is going to Bob himself.
  * Post office A moves the envelope to a truck and delivers it to post office B
    * The truck's destination is post office B, but the envelope & letter inside keep their original destinations.
  * Post office B moves the envelope to a new truck and delivers it to Bob's house.
    * Once again, this truck has a different destination than the previous truck: Bob's house.
    * The envelope and letter inside still have their original destinations.
* The envelope is now delivered to Bob's house, opened & letter addressed to him is read by him.

This simple letter system has different parts that care about different things. 
  -> Message itself
  -> Who should read it
  -> Which house it goes to 
  -> How it moves along the route

We can turn those roles into a layered model, then compare it to how TCP/IP works. 

So let's build that model. Don't need to remember this model or the names of the layers. It's just an analogy.

<img width="893" height="485" alt="Screenshot (959)" src="https://github.com/user-attachments/assets/cd437bd2-07a6-4e55-9a15-532c1cc2fa3e" />

Often the letter will travel over multiple kinds of paths in its journey: Ground -> Air -> then again Ground. 

We can think of the last 2 layers combined as a delivery layer, or split them into 2 just like above in the analogy.

  * That's why some networking models use 4 layers, and some use 5.

<img width="902" height="483" alt="Screenshot (960)" src="https://github.com/user-attachments/assets/5f97e81b-a78f-49bb-b0a5-fcfc0ab299aa" />

* The Content layer focuses on the actual contents of the letter, and that doesn't change throughout the journey.
* The Recipient layer focuses on the person who should receive the letter and also remains the same from start to        finish.
* The Address layer focuses on the address of the house or building to which the letter should be delivered, and that     stays the same as well.
* The local Delivery layer focuses on getting the letter to the next stop in the route: post office A, then post         office B, and finally Bob's house.
* The Infrastructure layer is the system of roads and mail trucks that the delivery process relies on.

  * When you are writing a letter to Bob, you don't want to think about how the postal service will go about               delivering it.
  * That doesn't mean the layers are entirely independent.
 
  * For example: If you address the letter to somewhere overseas, that will influence how it's delivered.
  * But that's not your concern as you write the letter.
 
  * This separation of layers is true in our post system model example, and it's true of networks as well.
 
  * Let's replace letters with **Data** & roads with **Networks**, & build the 5-Layer TCP/IP model we'll actually         use.  

<img width="832" height="461" alt="Screenshot (961)" src="https://github.com/user-attachments/assets/f1bb6f77-20e7-443c-8089-227beccd2231" />

We will see how they actually work in a real network between a client & a server. 

<img width="850" height="503" alt="Screenshot (964)" src="https://github.com/user-attachments/assets/7f9c72c0-f8f9-49eb-9491-023390b9e69b" />

A "**host**" just means a device connected to the network that can send & recieve data. 

**Layer 1 - Physical Layer**

<img width="1101" height="167" alt="Screenshot (975)" src="https://github.com/user-attachments/assets/66bc2181-7dd3-4ed2-9293-4d374768d9eb" />


* The Physical Layer(Layer 1) sends and receives bits as electrical, optical, or radio signals over the         medium.
* Defines things like cables, connectors, signal levels, and link speeds.
* Examples: Copper UTP cables, fiber-optic cables, Wi-Fi radios and antennas, network interface cards(NICs).
* The physical aspects of transmitting data are very complex.
  * Network engineers typically don't have to know the low-level details.  

<img width="996" height="302" alt="Screenshot (976)" src="https://github.com/user-attachments/assets/2de1952c-98c7-4931-b163-e3d2cd3d161d" />

**Layer 2 - Local Network Layer**

<img width="1000" height="164" alt="image" src="https://github.com/user-attachments/assets/c9e4ebc2-fbd4-4831-b271-354b4c04b703" />

* The local Network Layer (Layer 2) provides hop-to-hop delivery of messages on a local network.
  * A hop is one step along the path between two devices.
    * From one router or host to the next router or host in the path.
  * Switches don't count: a switch just extends the local network, allowing multiple devices to connect.

* Uses MAC(Media Access Control) addresses to identify interfaces.
  * PC1 sends the message to the MAC address of R1's G1 interface (NIC).
  * R1 sends the message to the MAC address of R2's G1 interface (NIC).
  * R2 sends the message to the MAC address of SRV1's interface (NIC).
 
* Protocols at this layer include:
  * Ethernet (IEEE 802.3)
  * Wi-Fi (IEEE 802.11)       

**Layer 3 - Internet Layer**

<img width="932" height="137" alt="image" src="https://github.com/user-attachments/assets/2919c019-21cd-439a-86b4-7c2416438131" />


* The Internet layer (Layer 3) provides end-to-end delivery between hosts across multiple networks.
  * Internet = internetwork (between networks)
 
* Uses IP addresses to identify hosts in the network.
  * When PC1 sends a message to SRV1, it addresses the message to SRV1's IP address.
 
* Routers operate mainly at this layer, using the message's destination IP address to forward the message toward its final destination host.

* Protocols at this layer include:
 * IP (IPv4, IPv6)
 * ICMP (Internet Control Message Protocol)    

**Layer 4 - Transport Layer**

<img width="722" height="162" alt="image" src="https://github.com/user-attachments/assets/fd59cb10-1ecf-4049-a251-fca5f5e3a4bd" />

* The Transport layer (Layer 4) provides end-to-end communication between application processes.
  * Also called "process-to-process" or "service-to-service".
 
* Uses port numbers to identify the processes on each host.
  * When the web client on PC1 wants to send a request to the web server running on SRV1, it addresses the message to port 80.
 
* Runs mainly on the communicating hosts (PC1 and SRV1): routers normally operate based on IP (Layer 3), not on Transport-layer information.

* Protocols at this layer include:
  * UDP (User Datagram Protocol): simple and efficient
  * TCP (Transmission Control Protocol): more robust features beyond basic message addressing  

**Layer 5 - Application Layer**

<img width="722" height="162" alt="image" src="https://github.com/user-attachments/assets/fd59cb10-1ecf-4049-a251-fca5f5e3a4bd" />

* The Application layer (Layer 5) is where network communications meet applications.
  * Usually called Layer 7
 
* Defines how application processes format, send, and interpret data.

* Protocols at this layer define message formats and rules for specific tasks, such as:
  * Browsing web pages (HTTP/HTTPS)
  * Transferring files (FTP, TFTP)
  * Sending/receiveing email (SMTP, POP3, IMAP)
 
* Network infrastructure devices(routers, switches) don't care about Application-layer details.
  * They just move messages across the network.
  * Only the communicating hosts interpret the data.     

**Encapsulation and Decapsulation**

Encapsulation 

<img width="1084" height="428" alt="image" src="https://github.com/user-attachments/assets/3e7cf7b2-6d22-47fe-abb5-168bf068f61a" />

* The **Application layer** prepares the data to be sent over the network.
* As the message moves down the stack, each layer **encapsulates** the data with a **header** including the information needed for that layer.
  * Source and destination addresses (port numbers, IP addresses, MAC addresses), etc.
  * Layer 2 also adds a **trailer** that the receiving device uses to check for transmission errors.
* The **Physical layer** transmits the bits as signals over the physical medium.
  * The **L2 header** is transmitter first, and the **L2 trailer** is transmitter last.  

Decapsulation

<img width="1048" height="417" alt="image" src="https://github.com/user-attachments/assets/60d0bd9a-23a3-4eb7-b183-24b3ef2bbcd4" />

* The receiving device receives the message as a stream of bits at Layer 1.
* The device examines the information in the Layer 2 header and trailer, and then removes them (**decapsulation**).
  * The decapsulation process continues up the stack: Layer 3 removes the L3 header, then Layer 4 removes the L4 header, and then the data is delivered to the Application layer.
* The application processes the data and, if needed, generates a response that goes back down the stack.

<img width="661" height="302" alt="image" src="https://github.com/user-attachments/assets/76afc57e-4a4b-4cdf-84e2-40dca2b24137" />

**Protocol data units**

* At each stage in the encapsulation/decapsulation process, there is a name      given to the message.
  * The combination of the data and an L4 header is called a **segment**(TCP)      or **datagram**(UDP).
    * TCP creates segments; UDP creates datagrams.
  * The combination of a **segment/datagram** and an L3 header is called a **packet**.
  * The combination of a packet and an L2 header/trailer is called a **frame**.
     * This is what is actually sent over the wire.
     
  * We can use alternative names to describe the message at each stage:  **Protocol Data Unit(PDU)**
    * A segment or datagram is a **Layer 4 PDU (L4PDU)**.
    * A packet is a **Layer 3 PDU (L3PDU)**.
    * A frame is a **Layer 2 PDU (L2PDU)**.
   
  * The contents of each PDU (everything encapsulated by that layer's header/trailer) are called the **payload**.
    * A **segment** or **datagram's** payload is the **application data**.
    * A **packet**'s payload is a **segment** or **datagram**.
    * A **frame**'s payload is a **packet**.
   
  <img width="187" height="113" alt="image" src="https://github.com/user-attachments/assets/a8d78fc6-f62d-4f0f-8a72-886f8f438a74" />

 <img width="201" height="95" alt="image" src="https://github.com/user-attachments/assets/a69ef626-fd12-444a-8df7-473067d8d3f5" />

<img width="307" height="84" alt="image" src="https://github.com/user-attachments/assets/5288e706-1893-46b4-8f63-b3839834bdfb" />

**Adjacent-layer interaction**

<img width="775" height="282" alt="image" src="https://github.com/user-attachments/assets/ddacddca-adb8-4b4d-b537-2929a9a486fd" />

* Each layer provides a service to the layer above it and is serviced by the layer below it (**adjacent layer interaction**).
  *  **Layer 4** provides a service to **Layer 5** by delivering data to the correct application using port numbers.
  *  **Layer 3** provides a service to **Layer 4** by delivering segments/datagrams to the correct destination host using IP addresses.
  *  **Layer 2** provides a service to **Layer 3** by delivering packets to the next hop using MAC addresses.
  *  **Layer 1** provides a service to **Layer 2** by sending and receiving frames as electrical, optical, or radio signals.

**Same-layer interaction** 

<img width="906" height="342" alt="image" src="https://github.com/user-attachments/assets/6af9c700-a353-4d75-806f-b31b53674e26" />

* Each layer communicates with the same layer on other devices (**same-layer interaction**).
  * The Application layer on one host sends data to the Application layer on the other host.
  * A segment/datagram is addressed to the **Layer 4 port number** of the correct application on the destination host.
  * A packet is addressed to the **Layer 3 IP address** of the destination host.
  * A frame is addressed to the **Layer 2 MAC address** of the next hop.
  * Signals sent out of a physical port are received by a **physical port** on the connected device. 

**Separation of Layers**

<img width="1119" height="412" alt="image" src="https://github.com/user-attachments/assets/ed1ec10d-2882-48b0-9d00-f8a8082f0806" />

* Each layer has its own job and provides a specific service to the layers above.
  * The layers are modular.
* As long as each layer keeps its "contract" with the other layers, we can improve or replace protocols at different layers without redesigning everything.
* That flexibility is one of the main benefits of the layered model.   

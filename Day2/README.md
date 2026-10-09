Interfaces and Cables 

Interfaces/Ports -> The switch has more interfaces
10/100/1000 BaseT Ports(1-24) - Ports are Auto MDIX

<img width="386" height="518" alt="image" src="https://github.com/user-attachments/assets/4f6925ed-950a-4c5c-a7fa-8439c993b79c" />

When devices are connected to a wired network, they use an RJ45 port. 

RJ-45 --> Copper Ethernet Cable 

**1. What is Ethernet?**

Ethernet is a collection of network protocols and standards, not a single protocol.
For the purpose of this lesson, we will focus on types of cabling as defined by Ethernet standards.
In future lessons, we will learn other aspects of Ethernet. 

**2. Why do we need network protocols/standards?**

<img width="544" height="320" alt="image" src="https://github.com/user-attachments/assets/db95422f-8f16-440c-abef-34b4425e3add" />

If 2 people are talking to each other and **A** only speaks English and the other only speaks Japanese, there is not going to be communication between them. 

What they need is an agreed-upon system of communication, like a common language between them, and Network protocols serve that purpose for network devices; that's why standards like Ethernet exist.

Interfaces & Cables

If you are trying to connect a network switch, but the maker of the cable and the maker of the switch haven't agreed upon the size and Shape of the connector & Port, you won't be able to connect them. 

<img width="1026" height="293" alt="image" src="https://github.com/user-attachments/assets/7252e0e4-6d11-4d92-bbb2-3666fc3333e8" />

That's why there are industry standards that all vendors follow, both in terms of physical standards like connectors & cables like these, as well as logical standards, like IP the Internet Protocol.

Connections between devices in a network operate at a set speed; these speeds are measured in bits per second.

**3. What is a bit?**

It's a value represented as either a 0 or a 1.
YouTube, the video, your OS all of it is just a series of **0s** & **1s** that your computer interprets. 

-> When communicating across a copper network cable, a variation in the electrical signal is interpreted by the receiving device as a 0 or a 1. 

**4. What is a byte?**

A series of 8 bits. 

8 Bits = 1 Byte

<img width="730" height="208" alt="image" src="https://github.com/user-attachments/assets/ca7b0985-1755-4383-9a9c-1fac5f49bad9" />

A byte: 8 bits of data being sent along a wire. 

<img width="686" height="55" alt="image" src="https://github.com/user-attachments/assets/e48c9565-1065-42d5-a548-a9c95e5650d8" />

Speed is measured in bits per second
(Kbps, Mbps, Gbps, etc) not bytes per second. 

<img width="807" height="362" alt="image" src="https://github.com/user-attachments/assets/3a60d8c1-bab7-4296-9aac-155e341252a6" />

**Ethernet Standards**

Defined in the IEEE 802.3 standard in 1983.

IEEE = Institute of Electrical & Electronics Engineers. 

<img width="933" height="212" alt="image" src="https://github.com/user-attachments/assets/433eddc4-0850-430b-ba04-bdb253f3216f" />

Physical Cables / UTP(Unshielded Twisted Pair) Cables 

The copper cables used in Ethernet standards are UTP cables. 

UTP - Unshielded Twisted Pair cables(no metallic shield, which can make them vulnerable to electrical Interference).
      4 pairs of cables twisted together protect against electromagnetic interference (EMI) 
      In total, they have 8 wires. 

<img width="700" height="571" alt="image" src="https://github.com/user-attachments/assets/92264f52-660d-4260-8d81-cf1de4e7896b" />

RJ-45 connectors have 8 pins 

<img width="955" height="169" alt="image" src="https://github.com/user-attachments/assets/80624ea7-2e86-47e2-bbb9-22b23d22a8d7" />

**10 BASE-T & 100 BASE-T**

Let's say we are connecting a PC to a Switch with a Fast Ethernet connection. 

Keep in mind! Ethernet and Fast Ethernet connections use 4 wires.

<img width="949" height="506" alt="image" src="https://github.com/user-attachments/assets/7506b4a2-ebee-4d3b-a0fc-e7c84a15e5d2" />

<img width="829" height="548" alt="image" src="https://github.com/user-attachments/assets/a6ecdd4a-c16f-4c77-9566-8fa478a8837d" />

A copper Ethernet cable has two RJ-45 connectors, one on each end. 
Connects straight through: pin 1 on one end to pin 1 on the other end. 
Pin2 connects to pin2; pin3 connects to pin3, etc.

In networks, we don't always connect a PC to a switch, or a switch to a router. 

What if we want to connect one router to another, one switch to another, or maybe connect 2 PCs?

<img width="1197" height="462" alt="image" src="https://github.com/user-attachments/assets/6714d26e-e557-451f-94cb-a3638e972d14" />

Router 2 isn't prepared to receive data on pins 1 & 2 of its interface, so communication between the two routers doesn't happen. 

How can we successfully connect two routers, perhaps two switches, or two PCs?
-> The same thing applies to connecting a pc directly to a router, also, because they both transmit data on pins 1 & 2, and receive data on pins 3 & 6.

<img width="617" height="445" alt="image" src="https://github.com/user-attachments/assets/c131a04e-d517-4d57-824e-6e34540a1302" />

So the answer to this problem is a different type of cable. 

A straight-through cable connects pin1 to pin1, pin2 to pin2, pin3 to pin3 etc. 

There is another type of cable: a  crossover cable. 

<img width="726" height="399" alt="image" src="https://github.com/user-attachments/assets/9bcb9354-22d0-4676-a0e3-3b38e50a5043" />

Pin 1 on one side connects to pin3 on the other side. Pin2 on one side connects to pin6 on the other side. Pin 3 on the left side will connect to pin1 on the right side. Pin 6 on the left side will connect to pin2 on the right side. 

Wires are "Crossed over" each other, hence called a crossover cable.

<img width="691" height="423" alt="image" src="https://github.com/user-attachments/assets/ca61a861-93b8-4937-b078-d1125a818ae4" />

The transmit pins on one side are connected to the receive pins on the other side; now the two devices can send data to each other with no problems.

<img width="753" height="499" alt="image" src="https://github.com/user-attachments/assets/0d6c8626-72b5-4d82-8176-531df892091c" />

The network interface card on a PC & the network interfaces on a router both transmit data on pins 1 and 2 & receive data on pins 3 and 6; however, if you connect them with a crossover cable, they will be able to exchange data with no issues. 

<img width="853" height="452" alt="image" src="https://github.com/user-attachments/assets/2222a266-cf74-4c64-968c-6dda5ea7f42a" />

**UTP Cables (10 BASE-T, 100 BASE-T)**

<img width="936" height="191" alt="image" src="https://github.com/user-attachments/assets/1ccebb0c-ccbe-43ab-b70b-fee075aaa594" />

While all of that is important information to know and can cause issues in networks even in the modern day, the truth is that most modern networking devices have evolved beyond having to worry about straight-through or crossover cables. 

That's because newer networking devices include a feature called Auto MDI-X.

**Auto MDI-X**

Previously, if two switches were connected with a straight-through cable like this, they would be unable to communicate. 

<img width="597" height="435" alt="image" src="https://github.com/user-attachments/assets/5f022e9d-f094-4b70-b3fe-8e296e339694" />

However, Auto MDI-X allows devices to automatically detect which pins their neighbor is transmitting data on, & then adjust which pins they use to transmit & receive data. 

They can exchange data normally.

<img width="609" height="476" alt="image" src="https://github.com/user-attachments/assets/2399229e-49bb-437f-87f6-ae2138ba5a9a" />

So useless you are working with network equipment that is quite old; you don't really have to worry about straight-through & crossover cables. 

So unless you are working with network equipment that is quite old, you don't really have to worry about straight-through & crossover cables. 

**UTP Cables - 1000 BASE-T, 10 GBASE-T**

Higher-speed copper Ethernet cables. 

For gigabit Ethernet & 10 Gigabit Ethernet, all 8 wires are used. 

<img width="930" height="338" alt="image" src="https://github.com/user-attachments/assets/a6855f6d-f5c9-4255-9ea6-43f8caf80641" />

Big difference between 1000 BASE-T & 10 GBASE-T, and 10 BASE-T & 100 BASE-T. 

In addition to using all four pairs of wires, in 1000 BASE-T and 10 GBASE-T, each pair is **bidirectional**, meaning each pair isn't dedicated specifically to transmitting data or receiving data. 

Each pair is **Bidirectional**.

This is part of the reason that they can operate at much faster speeds. 

**Fiber Optic Connections**

We have covered a lot about connections using copper UTP cables. 

But there is a newer technology that is superior in many ways. 

For example, copper URP wiring can be used for up to 100 meters. That is usually plenty within a LAN, but how about for larger networks?

Look at the Cisco Catalyst switch here; it has 24 ports for RJ-45 connectors.  

<img width="782" height="288" alt="image" src="https://github.com/user-attachments/assets/23b90077-5c97-46ee-8fab-1f7f04fac335" />

<img width="906" height="402" alt="image" src="https://github.com/user-attachments/assets/5098601c-7368-4dbb-9d25-603d7eacfff0" />

Rather than an electrical signal over copper wiring, these cables send light over glass fibers. 

There are two connectors on each end. 

That's because you need one connector to transmit data & one to receive data on each end. 




































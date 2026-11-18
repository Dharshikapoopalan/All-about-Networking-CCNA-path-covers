**Ethernet LAN Switching Part - 1**

We will look at how data travels through a network. This time, we will focus on Ethernet LAN switching.

<img width="840" height="313" alt="Screenshot (1099)" src="https://github.com/user-attachments/assets/7b9805ac-e395-4d45-b9a2-c160133d0af4" />

If we look at this simple network consisting of a few PCs, a switch, and a router, connected to the internet, we will be looking at how data moves between the switches and the end hosts connected to them and to their router.

How data is sent from the router to other networks will be a topic for a future module. 

**OSI Model - Physical Layer**

<img width="337" height="389" alt="image" src="https://github.com/user-attachments/assets/dfb9f9f8-8f5d-4f1e-b527-f20fd22949a1" />

  - The physical layer defines the physical characteristics of the medium used to transfer data between devices.
  - For example, voltage levels, maximum transmission distances, physical connectors, cable specifications, etc.
  - Digital bits are converted into electrical (for wired connections) or radio (for wireless connections) signals.
  - All the information in Day 2 content about cables and pin layout, etc., is related to the physical layer.
  - So we know a good amount about the physical layer, learning about copper UTP cables, fiber-optic cables, RJ-45 connectors, etc.

**OSI Model - Data-Link Layer**

<img width="337" height="389" alt="image" src="https://github.com/user-attachments/assets/bf885f9b-4e3f-4132-81bb-7e2283f6c9fd" />

  - Provides **node-to-node** connectivity and data transfer(for example, pc to switch, switch to router, router to router).
  - Defines how data is formatted for transmission over a physical medium(for example, copper UTP cables)
  - Detects and (possibly) corrects physical layer errors.
  - Uses Layer 2 addressing, separate from Layer 3 addressing.
  - IP addresses are Layer 3 addresses, not Layer 2.
  - Switches operate at Layer 2 (Here we will be discussing Ethernet LAN switching, and Ethernet involves Layer 1 and Layer 2 of the OSI model)
  - Since we have covered the Layer 1 Ethernet Standards like UTP cables, here we will be discussing Layer 2. 

Local Area Networks (LANs)

  - LAN is: There are different ways of defining a LAN, and our understanding of a LAN will become complete as we learn more and more about            networking.
  - Basically, it is a network contained within a relatively small area, like an office floor or our home network, which includes a small             geographical area.
  - **Routers are used to connect separate LANs.**

<img width="849" height="391" alt="image" src="https://github.com/user-attachments/assets/0db10910-3af9-44ae-8c26-e68c04c5a602" />

  - Looking at the above diagram, we can see there are 4 LANs.
  - Switches do not separate LANs, but adding more switches can be used to expand an existing LAN.

<img width="905" height="423" alt="image" src="https://github.com/user-attachments/assets/148a715b-15a2-4fa0-9c37-834cf10ae6e0" />

  - Devices inside the red box are part of one large LAN.
  - The blue and black boxes are the same as the devices in the red box, but instead of the switches being connected, they are connected to different router interfaces. That means they are two separate LANs.

**Sending data within LAN**

  OSI Model - PDU (Protocol Data Units)

<img width="671" height="471" alt="image" src="https://github.com/user-attachments/assets/ed25437d-c7ad-48ac-8961-2ce81417375e" />

  - The above shows the encapsulation process as data is prepared to be sent over a network.
  - At the top, the data prepared by the upper layers of the OSI model is simply called data.
  - A Layer 4 header is added & this combination of data & layer 4 header is called a segment.
  - A Layer 3 header is added to the segment & it is now called a packet.
  - Finally, a Layer 2 header & trailer are added to the packet; it becomes a frame.

  - Layer 2 PDU -> Frame
  - Layer 3 PDU -> Packet
  - Layer 4 PDU -> Segment

  - Will see how switches receive & forward frames, specifically Ethernet frames, since it's the Layer 2 protocol used in virtually every LAN in      existence today.
  - Let's take a look at the actual contents of this Ethernet header & trailer.

    <img width="918" height="312" alt="image" src="https://github.com/user-attachments/assets/fa45ba6b-478b-4415-b695-a7c6cffa432c" />

  - There are 5 fields in the header.

  **Preamble & SFD(Start Frame Delimeter)**
    
  - These are used for synchronization and to allow the receiving device to be prepared to receive the rest of the data in the frame.
  - In networking, syncing(synchronization) refers to the process of ensuring data consistency across multiple devices or systems.
  - It involves coordinating updates so that all devices maintain the same, up-to-date version of the information.
  - This ensures that when data is modified on one device, the changes are reflected on all other connected devices, preventing discrepancies &       errors.

  **Destination MAC Address**

  - The Layer 2 address to which the frame is being sent. 
  
  **Source MAC Address**

  - The Layer 2 address of the device that sends the frame.

  **Type**
  
  - It indicates the Layer 3 protocol used in the encapsulated packet, which is almost always Internet Protocol (IP ---->  Version 4 (IPv4 - 0x0800) or Version 6 (IPv6 - 0x86DD).

**L2 Trailer - FCS (Frame Check Sequence)**
  
  <img width="251" height="230" alt="image" src="https://github.com/user-attachments/assets/e53c1d98-8993-49b8-a047-5b906ccbb096" />

  - However, sometimes this is a length field, indicating the length of encapsulated data, depending on the version of Ethernet.
  - The Ethernet trailer has one field that is the FCS, which stands for frame check sequence.
  - Used by the receiving device to detect any errors that might have occurred in transmission.
  - Let's take a look at these fields in more detail:

  **Preamble**

  - Length: 7 bytes (7*8 = 56 bits)
  - It is a series of alternating 1s and 0s. (10101010 10101010 10101010 10101010 10101010 10101010 10101010)
  - The purpose of this is to allow devices to synchronize their receiver clocks. To make sure they are ready to receive the rest of the frame and the data inside. 

    **SFD(Start Frame Delimeter)**

                                                                                                              

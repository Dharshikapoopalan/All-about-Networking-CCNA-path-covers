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

  OSI Model - PDU

  
  

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


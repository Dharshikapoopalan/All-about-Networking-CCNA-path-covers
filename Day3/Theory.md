**How the TCP/IP model actually works**

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




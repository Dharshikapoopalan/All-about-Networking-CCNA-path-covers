Cisco IOS CLI

Cisco IOS is the operating system used on Cisco devices, like Windows on a PC or macOS on an iMac.
  
  - Cisco's IOS is not related to Applé's ios for iPhones. 

1. What is a CLI?

  - CLI stands for Command-Line Interface.
  - It's the interface you use to configure Cisco devices like routers, switches, and firewalls. 

  - Here is an image of the Cisco IOS CLI.
<img width="421" height="158" alt="image" src="https://github.com/user-attachments/assets/06826cbd-f58a-40dd-9382-110d7a719496" />

2. What is a GUI (Graphical User Interface)
   Cisco GUI
<img width="389" height="297" alt="cisco ASDM firewalls" src="https://github.com/user-attachments/assets/b7e02387-7baa-4225-8286-c2d121403cf5" />

   - **Cisco ASDM**, which can be used to configure Cisco's firewalls.
  
4. How to connect to a Cisco device? (Console Port)
  - There are a couple of methods, but here we'll talk about connecting via the console port.
  - Connecting to a device via the console port typically involves bringing your laptop to the device and connecting to the console port of the device.
  - There are also methods to connect to a device remotely, but we'll cover it later. In any case, when you first configure a device, you have to connect to the console port.

<img width="418" height="458" alt="image" src="https://github.com/user-attachments/assets/18462041-4c04-4533-b259-7608d23df84b" />

- This is an image of a Cisco Catalyst switch, and notice the two console ports. 
- One of them is an RJ45 port, just like the switch's network ports.
- The other is a USB mini-B connector.
- We can connect to either of these, but let's say we are going to connect to the RJ45 port.
  i) Need a proper cable
    <img width="2560" height="2560" alt="image" src="https://github.com/user-attachments/assets/0479cbce-e8d2-4e32-8acb-81cc79179f12" />
    <img width="894" height="989" alt="image" src="https://github.com/user-attachments/assets/134672ea-d5ce-4f80-826b-e7079846ccd6" />

- This is the kind of cable we use.
- Notice one end has an RJ45 connector, just like the Ethernet UTP cables we looked at; the other end is a DB9 connector.
- However, most laptops these days no longer have a serial port to plug the cable into, so we'll probably need an adapter, like this, to a USB port on our laptop.
- The name is similar to a crossover cable, but it's different than an Ethernet UTP crossover cable. 

4. Rollover cable?
  - Like in an Ethernet URP cable, 8 pins on each end are used.
  - However, they connect like this:
  - Pin 1 to pin 8
<img width="387" height="278" alt="image" src="https://github.com/user-attachments/assets/c6cadd51-94bc-4385-bc46-bbd8df9e5403" />

- So, once you've connected our computer to the device, how do we actually access the CLI?
- We need a terminal emulator for this

<img width="451" height="437" alt="image" src="https://github.com/user-attachments/assets/4cf34d71-8481-4d35-9dd3-3038641ce3c2" />
<img width="448" height="438" alt="image" src="https://github.com/user-attachments/assets/d5ba2e2e-88bb-44f4-89e6-e3494eeb3b06" />

  - You can get it at putty.org. Select serial, here and then click open and you should be connected to the CLI.
  - You should be able to connect with the default settings, but click Serial down here, and we can view and edit the default settings for the serial connection.
  - Note that these settings match the defaults on Cisco devices, so we will probably never have to change them, but it's good to be aware of them and try to remember them.
  - The speed, also known as baud rate, is 9600 bits per second.
  - There are **8 data bits** and **1 stop bits** Understanding data bits and stop bits means that for each 8 bits of data one stop bit is sent, to mark the end of the 8 bits.

  - Parity is set to none.
  - Parity is used to detect errors.
  - And Flow control is set to none. Flow control: Controlling the flow of data from the transmitter.

**Cisco IOS CLI**

Router> 
Since this is the first time booting up the device, we are asked if we would like to enter the initial configuration dialog, and we answer no.
<img width="694" height="628" alt="image" src="https://github.com/user-attachments/assets/9d2fc154-bb9b-4164-8000-868563d886b9" />

Then we press the Enter key to get started, and we are now free to type commands into the CLI. 

<img width="689" height="617" alt="image" src="https://github.com/user-attachments/assets/29da8cb3-9623-49ae-9aea-66c6c7b4eebf" />

- When we first enter the CLI, you will by default be in what's called '**user Exec mode**.'

<img width="780" height="318" alt="image" src="https://github.com/user-attachments/assets/72e9943f-b555-4a9d-b92a-e2ac499cdae4" />

- User Exec mode is indicated by the 'greater than sign' next to the host name of the device.

- Note: The default hostname for this device is 'Router'.

- All devices have a hostname, and for a Cisco router, the default name is Router.

**User Exec mode** - Outer layer/3rd layer

- User Exec mode is very limited.
- Users can look at some things, but can't make any changes to the configuration.
- Usually we don't do anything in this mode.
- Also called 'user mode'

- So let's move to a mode with a little more power to make changes to the device.

- If we enter the '**enable**' command in **user Exec mode**, we will be place in '**privileged Exec mode**'

<img width="177" height="77" alt="image" src="https://github.com/user-attachments/assets/afa0af7f-6aeb-4904-8210-3d8858b8f6f6" />

**Privileged Exec mode** - 2nd Layer

- In privileged Exec mode, a pound sign, or hashtag, whatever you want to call it, is displayed.
- Privileged Exec mode provides complete access to view the device's configuration, restart the device, etc.
- Cannot change the configuration, but can change the time on the device, save the configuration file, etc.

  **Commands available in user Exec mode Vs Privileged Exec mode**

  **User Exec mode**

  <img width="409" height="204" alt="image" src="https://github.com/user-attachments/assets/ed5590ea-6c5e-4620-83c4-1af4e84ed6a6" />

  **Privileged Exec mode**

  <img width="626" height="519" alt="image" src="https://github.com/user-attachments/assets/db5914e5-0d65-4a72-a0ee-1304ae30ffc5" />

  These details were taken from Cisco Packet Tracer; it's a network simulator.

  - Use a question mark (?) to view the available commands that are available in the mode.
 
  **Cisco IOS CLI**

<img width="208" height="72" alt="image" src="https://github.com/user-attachments/assets/a2d7c785-781b-4efe-95bc-443740e1c858" />

- When we press Tab, the CLI will automatically complete the word for us and display the complete word on a new line.
- Another convenience is that we don't even have to complete the command. (Short words will work)

<img width="141" height="40" alt="image" src="https://github.com/user-attachments/assets/b636cbbe-8ff4-49a1-8c27-249ede36b69e" />

- Here we just typed "en" and hit Enter, and I was brought to **privileged Exec mode**. 
- This can really save us a lot of typing when we are entering many commands.
- There are limits to this, however.

<img width="249" height="51" alt="image" src="https://github.com/user-attachments/assets/e3f8e579-28df-4cc4-b5d0-7a6888cf286d" />

- Although 'en' was enough for the router to understand that we meant to use the command 'enable'. That's because it is the only command that begins with EN that can be entered in **user EXEC mode**.

- If we type just 'e ', however, we are told that it is an ambiguous command. That is because there is more than one command that begins with 'e'.

- How can we view the commands that begin with e? Remember the question mark from before? If we type 'e' followed by a question mark, it displays the possible commands that begin with 'e'.

<img width="210" height="35" alt="image" src="https://github.com/user-attachments/assets/2ab54c8f-3633-498b-8e8e-bb619de8e77e" />

- There are two enable & exit, so if we type just 'e' and hit enter, the router doesn't know which command we want to use.
- So the shortest form of the enable command is 'en' and the shortest form of the exit command will be 'ex'.

**Global Configuration Mode** - inner layer 

- Now let's actually make some changes to the router's configuration.
- To do so, we enter the '**configure terminal**' command in privileged exec mode.

<img width="457" height="63" alt="image" src="https://github.com/user-attachments/assets/fe3ac3df-b59b-4eea-bef3-0a541c766757" />

- When in global configuration mode, config is inserted after the hostname.
- Shortcut

<img width="479" height="141" alt="image" src="https://github.com/user-attachments/assets/bc093f8c-c710-4c38-b960-ef8c4a639e8f" />

- Notice we can type con? Then te? to find out the entire words that are used.

<img width="318" height="102" alt="image" src="https://github.com/user-attachments/assets/437c8f8c-f042-4d2b-b1a6-53f5f7db7a8e" />

  **Enable Password**
 - We don't want just anyone to be able to make changes to the network configuration, or even be able to just look at the configuration, because that could be a security risk.

 - We can protect **privileged exec mode** with a password, so that if a user enters the 'enable' command from **user EXEC mode**, they are asked for the password.

 - This is done with the command **enable password** in **global configuration mode**.

<img width="499" height="219" alt="image" src="https://github.com/user-attachments/assets/7619588c-56e2-41bf-b770-b4b7ab50c5d2" />

 What is the use of the question mark?

 - In the 2nd line, the question mark with no space after password output is password.
 - If we use a question mark without a space, it shows all the possible completions of that word.
 - I already typed the full word password, so it just displays the word again, and there are no other words that begin with password.

 - On line 4, we used a question mark again this time with a space after password.

 - Line 5
 - Line 6:        On lines 5, 6, and 7, we received different output
 - Line 7

 - This time, it shows all possible options we could enter next in the command.

 - In this case, we will use the middle one displayed in Line6
 - LINE in all capital letters means we don't type LINE; you type a line, which will become the password.

 - In line 8, we typed CCNA in all capitals as the password. Note that passwords are case-sensitive, so CCNA in capital letters & ccna in lower letters are different passwords.

 - Once again, in line 8 we typed question mark with space to check if there are any further options.

 - Line 9 **<cr>** means that there are no further options; the only option is to press Enter to enter the command.

 - Once pressed, the password is set.

Testing the password


  


NEtworking notes

ch 1 funda mentals
📡 Overview of Computer Networks – Notes
a computer network is is a group of devices connetced to each other to share information 
there is more than 10 types of networks 
but the 2 main ones are LAN and WAN 
LAN is a network that is used in small areas like a home network 
WAN is a network that is used in bigger areas liek schools, businesses 

The purpose of thse are communication and resource sharing

Netwrks allow us to 
communicate between devices, 
share resources like files to other devices e.g printers
provides internet functionality for browsing and streaming
is the foundation for app conectivity and data transfer

in devops networks provide:
server interaction: enables communication between servers and applications
deployment: ccritical for launching and updating applications
manegement: important for monitoring and infrastructure maniging
optimisation: betters trouble shooting performance and scalability so data can flow efficiently 


LAN VS WAN
LAN:
connects devices within a small area such as a home or office and are used for small areas 
it allows you to communicate with different devices within a small area
for example when you send a fdile from your computer i your home to a printer this operates on lan 
and it also provides internet access in a small area

WAN:
WAN connects devices on a larger scale such as universities or buisnessis and are used for large areas
They connect multiple lans together to be able to out put a large range of network and is liek a high way for data

key network components 
switches, routers and firewall
a switch is a manager for a local network and connects multiple devices within a same network 
a switch maneges data flow and makes sure that data flows effectivley to devises and prevents any congestion

a router is a traffic guidence for a newtrok and its job is to direct traffic between different networks 
in your home a router connects the internet to your computer and ensures data gets to the right place 

a fire wall is a security guard for yournetwork and it monitors what goes in and out of network traficc and has control over that 
fire walls are vital to protect the netwrok from unauthorised access and monitoring / controlling network traffic

IP adddress and MAC  address
IP address (Internet protocal address) allows devices to lowcate and communicate with each other

There are 2 main types IPV4 AND IPV6

IPV4
They are the most common and look like this <img width="336" height="138" alt="Screenshot 2025-07-30 113101" src="https://github.com/user-attachments/assets/9b7e0b95-3f87-4579-a1bf-c43580cceaac" />

They are 32 bit addresses which contain 4 sets of numbers seperate by 4 decimalss
each group can range from 0 - 255 creating billions of unique addresses how ever they are become more scarces now days 

IPV6
IPV6 addresses are less common and they look like this <img width="337" height="130" alt="image" src="https://github.com/user-attachments/assets/b25e4785-ec1f-466f-a582-389bcef11576" />

They are 128 bit addresses which comtain 8 sets of 4 hexidecimal digits seperated by colons 
each group is a mix of numbers and letters which creates way more than billions of unique addresses and they are on the rise now to being more used

The transition from IPV4 to IPV6 is important as IPV4 addresses are startring to run out and IPV6 will be needed to provide more addresses also IPV6 includes enhancements in address assignment and has improved security features

Why are IP addresses important:
They enable devices to identify and communicate with each other 
without them data being provided wouldnt know where to go 

MAC Address (media access controll address)
A MAC address is a unique identifier assigned to a network interface its like a finger print for your network devices
each device connected to a network has its own MAC address and it looks like this <img width="598" height="111" alt="image" src="https://github.com/user-attachments/assets/8c9cb532-7ae7-42fd-93df-d6e5b4b8fe29" />

They are 48 bit addresses which contan 6 sets of 2 hexci decimal digits seperated by colons
Just like IPV6, MAC addresses also use a mix of letters and numbers

whats their function?
MAC addresses operate on the data link layer and this layer is responsible for node to node transfer
MAC addresses help devices identify each other on a local network and are cruitial for things like ensuring your laptop connects to the right routers
They play a critial role in network and security withou them devices wouldnt be able to communicate withina  local network
They help manage and control network access making sure data packets get to the right plac e

Ports and protocals: TCP,UDP

Ports are like logical doors for a device each door is numbered and each number is used for a specific type of network communication
for example when traffict goes through port 80 which IS HTTP and 443 which is HTTPS 

These ports help ensure communication between devices when a device wants to send or recieve data it uses these ports
to guide data in the right direction 

Protocals are rules of the road fro data transmissionm, they define how data is formmated and transmitted accros a network
some common protocals  are HTTP STP and SMTP 
These protocals ensure devices and communicate effectivley by following the same set of rules

The importance of these:
without both the network ww have would eb a mess 
Ports ensure data gets to right application on your device 
Protocals makes sure the data is understandable and properly formatted

TCP - TRANSMISSION CONTROL PROTOCAL 
TCP is like the post man of the internet 
it makes sure data sent from one device reaches otehr device accuratly in the correct order.

Characteristics of TCP:
Connection oriented - befoere any data is sent connection has to be established on both devices
requires "handshake" - Process where 2 devices agree to communicated in networking theres a 3 step process to ensure both devices are ready to send and recieve data
reliable data transfer - TCP ensures all data sent is recieved correctly on the other end that means if any other data is lost the TCP will resend it 

Functions:
Ensures data is delivered in order - imagine your sending a multipart message tcp will send all those parts in order so the message makes sense
error checking and flow control - TCP checks for errors in data and controls the flow of data to prevent congestion this ensures smooth and error free commommunication.
Any biderectional communication - TCP is used when ever 2 devices need to echange data back and forth common examples for this is web browising, messaging and sending emails 

UPD - User Diagram Protocol 
UDP is like sending a postcard without tracking.
It sends data from one device to another quickly, but doesn’t check if it arrives or if it’s in the right order.

Characteristics of UDP:
Non connection oriented- UDP is connectionless
Simple protocal to send a recieve data - UDP is straightforward and much overhead is not needed making it quick and easy to use
prior communication not required - This has both a benefit and draw back 
Benefit: data can be sent immediately without waiting to establisha connection 
draw back: Theres no garuntee that the data will reach its destination and its connection less 
fast but less reliable-  because no connection is required unless for error checking UDP is faster than TCP but this speed comes as a cost of not reliability

functions: 
suitable for real-time applications e.g - video streaming, online gaming where speed is more important
DNS - things such as DNS lookups DNS quiries and anything DNS related uses UDP behind the scenes
VPN - some VPNs use UDP as it is faster and betetr for real time conmnectuions 

quick comparison <img width="688" height="351" alt="image" src="https://github.com/user-attachments/assets/dc0a3fd9-9065-4f0d-ad54-7c5ae4a0dc55" />

CH 2 ISO MODEL


# Computer Networking Learning Notes

## Chapter 1: Fundamentals

### 📡 Overview of Computer Networks

A computer network is a group of devices connected to each other to share information.

There is more than 10 types of networks but the 2 main ones are **LAN** and **WAN**:

- **LAN** is a network that is used in small areas like a home network
- **WAN** is a network that is used in bigger areas like schools, businesses

The purpose of these are communication and resource sharing.

### What Networks Allow Us To Do

Networks allow us to:
- Communicate between devices
- Share resources like files to other devices e.g printers  
- Provides internet functionality for browsing and streaming
- Is the foundation for app connectivity and data transfer

### Networks in DevOps

In devops networks provide:
- **Server interaction**: enables communication between servers and applications
- **Deployment**: critical for launching and updating applications
- **Management**: important for monitoring and infrastructure managing
- **Optimisation**: betters trouble shooting performance and scalability so data can flow efficiently

---

## LAN VS WAN

### LAN (Local Area Network)
LAN connects devices within a small area such as a home or office and are used for small areas. It allows you to communicate with different devices within a small area.

For example when you send a file from your computer in your home to a printer this operates on lan and it also provides internet access in a small area.

### WAN (Wide Area Network)
WAN connects devices on a larger scale such as universities or businesses and are used for large areas. They connect multiple lans together to be able to output a large range of network and is like a highway for data.
<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/89086ef5-282f-434c-8846-77929c73dd2f" />

---

## Key Network Components

### Switches
A switch is a manager for a local network and connects multiple devices within a same network. A switch manages data flow and makes sure that data flows effectively to devices and prevents any congestion.

### Routers
A router is a traffic guidance for a network and its job is to direct traffic between different networks. In your home a router connects the internet to your computer and ensures data gets to the right place.

### Firewalls
A fire wall is a security guard for your network and it monitors what goes in and out of network traffic and has control over that. Fire walls are vital to protect the network from unauthorised access and monitoring / controlling network traffic.

---

## IP Address and MAC Address

### IP Address (Internet Protocol Address)
IP address allows devices to locate and communicate with each other.

There are 2 main types **IPV4** AND **IPV6**.

#### IPV4
They are the most common and look like this:

![IPv4 Address Example](https://github.com/user-attachments/assets/9b7e0b95-3f87-4579-a1bf-c43580cceaac)

They are 32 bit addresses which contain 4 sets of numbers separate by 4 decimals. Each group can range from 0 - 255 creating billions of unique addresses however they are become more scarce now days.

#### IPV6
IPV6 addresses are less common and they look like this:

![IPv6 Address Example](https://github.com/user-attachments/assets/b25e4785-ec1f-466f-a582-389bcef11576)

They are 128 bit addresses which contain 8 sets of 4 hexadecimal digits separated by colons. Each group is a mix of numbers and letters which creates way more than billions of unique addresses and they are on the rise now to being more used.

The transition from IPV4 to IPV6 is important as IPV4 addresses are starting to run out and IPV6 will be needed to provide more addresses also IPV6 includes enhancements in address assignment and has improved security features.

#### Why are IP addresses important:
They enable devices to identify and communicate with each other. Without them data being provided wouldn't know where to go.

### MAC Address (Media Access Control Address)
A MAC address is a unique identifier assigned to a network interface its like a finger print for your network devices. Each device connected to a network has its own MAC address and it looks like this:

![MAC Address Example](https://github.com/user-attachments/assets/8c9cb532-7ae7-42fd-93df-d6e5b4b8fe29)

They are 48 bit addresses which contain 6 sets of 2 hexadecimal digits separated by colons. Just like IPV6, MAC addresses also use a mix of letters and numbers.

#### What's their function?
MAC addresses operate on the data link layer and this layer is responsible for node to node transfer. MAC addresses help devices identify each other on a local network and are crucial for things like ensuring your laptop connects to the right routers.

They play a critical role in network and security without them devices wouldn't be able to communicate within a local network. They help manage and control network access making sure data packets get to the right place.

---

## Ports and Protocols: TCP, UDP

### Ports
Ports are like logical doors for a device each door is numbered and each number is used for a specific type of network communication. For example when traffic goes through port 80 which IS HTTP and 443 which is HTTPS.

These ports help ensure communication between devices when a device wants to send or receive data it uses these ports to guide data in the right direction.

### Protocols
Protocols are rules of the road for data transmission, they define how data is formatted and transmitted across a network. Some common protocols are HTTP STP and SMTP. These protocols ensure devices and communicate effectively by following the same set of rules.

#### The importance of these:
Without both the network we have would be a mess:
- Ports ensure data gets to right application on your device
- Protocols makes sure the data is understandable and properly formatted

---

## TCP - Transmission Control Protocol

TCP is like the post man of the internet. It makes sure data sent from one device reaches other device accurately in the correct order.

### Characteristics of TCP:
- **Connection oriented** - before any data is sent connection has to be established on both devices
- **Requires "handshake"** - Process where 2 devices agree to communicate in networking theres a 3 step process to ensure both devices are ready to send and receive data
- **Reliable data transfer** - TCP ensures all data sent is received correctly on the other end that means if any other data is lost the TCP will resend it

### Functions:
- **Ensures data is delivered in order** - imagine your sending a multipart message tcp will send all those parts in order so the message makes sense
- **Error checking and flow control** - TCP checks for errors in data and controls the flow of data to prevent congestion this ensures smooth and error free communication
- **Bidirectional communication** - TCP is used when ever 2 devices need to exchange data back and forth common examples for this is web browsing, messaging and sending emails

---

## UDP - User Datagram Protocol

UDP is like sending a postcard without tracking. It sends data from one device to another quickly, but doesn't check if it arrives or if it's in the right order.

### Characteristics of UDP:
- **Non connection oriented** - UDP is connectionless
- **Simple protocol to send a receive data** - UDP is straightforward and much overhead is not needed making it quick and easy to use
- **Prior communication not required** - This has both a benefit and draw back:
  - **Benefit**: data can be sent immediately without waiting to establish a connection
  - **Draw back**: Theres no guarantee that the data will reach its destination and its connection less
- **Fast but less reliable** - because no connection is required unless for error checking UDP is faster than TCP but this speed comes as a cost of not reliability

### Functions:
- **Suitable for real-time applications** e.g - video streaming, online gaming where speed is more important
- **DNS** - things such as DNS lookups DNS queries and anything DNS related uses UDP behind the scenes
- **VPN** - some VPNs use UDP as it is faster and better for real time connections

### Quick Comparison

![TCP vs UDP Comparison](https://github.com/user-attachments/assets/dc0a3fd9-9065-4f0d-ad54-7c5ae4a0dc55)
<img width="1024" height="493" alt="image" src="https://github.com/user-attachments/assets/f8ef8119-6944-40f5-b0f9-acb6074e17f0" />

CH2 OSI model
OSI stands for Open Syetems Interconnection Model 

The 7 layers of the OSI model
Why do we need a communication model?
a communication model provides a standard frame work the way that simplifies the way devices and applications communicate over a network in shor these models make sures devices can understand each other 

Application independence:  
without a standar model applications would need to understand the specifics of underlying network
imagione if you needed to create different versions of your application/wifi/fibre or ethernet that would be hard
with a communication model applications can work independently of the network making development and conding more efficient

simplified network equipment management:
upgrading network exupment can be a hastle if there is not a standard model to follow
with the standard model communucation its easier to upgrade and manage network gear becasue they use the same language and this standardisation makes upgrading smoother and less prone to issues

decouple innovation:
thiss means that innovations and any update can happen at each layer of the model without interfesaring with the while system

The 7 layers:
Application layer - This is where network services are given directly to applications
Presentation layer - This is where data is translated into a readable format and where encryption is also handled
session layer - can manage sesssion s between different applications like TSL, sockets and more.
Transport layer - In this layer end to end communication and data integrity is managed where you have the two protocals TCP and UDP
Network layer - here routing with data packets is managed here you deal with IP, ICMP IPSec and more
Data link layer - Here node to node transfer and error detection is managed and you come accross things like frames, ethernet, switches, bridges and more
physical layer - physical layer between devices fibres, wireless,hubs and more 
<img width="1280" height="752" alt="image" src="https://github.com/user-attachments/assets/dc41c6ed-b3ec-42f2-83ce-657ee77e5d96" />

7 layers in more detail: 
Layer 1 - physical layer:
This ayer transmits raw bit streams over the physical medium 
This deals with hard ware connection such as cables, switches and entwork interface cards
ecamples of physical medium:
copper wires that have electric signal
fibre 
light waves
wifi with frequency waves
Also all deta is processed by all devices

Layer 2 - data link layer 
This layer is reponsible for node to node data transfer this ensures data packets are send and recieved correcty between different network nodes 
ist all abouut mainting a reliable link between different devices 
so at layer one everything is unordered and sent randomly but this layer fixes that putting your data into frames that are organised 
now frames are like envelops that carry the data and ensure it gets to the right places
components that are used here are mac addresses, switches and bridges 

layer 3 -  network later 
This layer determens how data iss ent to recipients and manages packets forwading including routing through different routers
it decides the best path for data to travel in a network ensuring it gets to the right place 
components that are used here are IP addresses and routers

layer 4 - transport layer 
This layer is responsible for providing reliable data transfer services to the upper layers
it is like the delivery service that ensures your data arrives saftley and in correct sequence
the protocols that allow this to happen are tcp and udp 
TCP provides reliable audited and error  free data 
EDP does the same but its more faster and less reliable

layer 5 - session layer 
This layer is responsibkle for 3 things. establishing, managing and terminating session.
Establishing session - session is getting started e.g logging into website
Maintaining session - keeping the session alive anmd running ensuring requestsz continue smoothly
Terminating session - Ending the session e.g logging out the browser 
components that are used here are session managment protocals such as RPC, NetBIOS and more 

Layer 6 - presentation layer
This layer is also known as the syntax lay because it ensures data being sent is in a useable or readable format.
Its liek a translater that translate data into a format the application layer can udnerstand 
Components: 
encyrption - ensures data security e.g plain text can be encyrpted text
data formating - can convert things into a format for example JPEG or PNG also thing like SSL and TSL

Layer 7 - application
This layer provides network services directly to applications this also could be the end user layer where everything happens when a user interacts with a device
handles things like web browing, file transfers and emails
components used in there are HTTP to access web services, FTP to transfer files  ,SMTP to send emails<img width="1000" height="3000" alt="image" src="https://github.com/user-attachments/assets/3039e016-cff5-4d91-8454-cd9a45373ccf" />






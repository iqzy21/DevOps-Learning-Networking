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

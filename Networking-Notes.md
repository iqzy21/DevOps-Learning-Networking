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
<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/06e9a341-d094-4055-9e92-6662ad136462" />

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

---

## Chapter 2: OSI Model

### What is the OSI Model?
OSI stands for Open Systems Interconnection Model.

### Why Do We Need a Communication Model?
A communication model provides a standard framework the way that simplifies the way devices and applications communicate over a network in short these models make sure devices can understand each other.

#### Application Independence:
Without a standard model applications would need to understand the specifics of underlying network. Imagine if you needed to create different versions of your application/wifi/fibre or ethernet that would be hard. With a communication model applications can work independently of the network making development and coding more efficient.

#### Simplified Network Equipment Management:
Upgrading network equipment can be a hassle if there is not a standard model to follow. With the standard model communication its easier to upgrade and manage network gear because they use the same language and this standardisation makes upgrading smoother and less prone to issues.

#### Decouple Innovation:
This means that innovations and any update can happen at each layer of the model without interfering with the whole system.

### The 7 Layers:
1. **Application layer** - This is where network services are given directly to applications
2. **Presentation layer** - This is where data is translated into a readable format and where encryption is also handled
3. **Session layer** - Can manage sessions between different applications like TSL, sockets and more
4. **Transport layer** - In this layer end to end communication and data integrity is managed where you have the two protocols TCP and UDP
5. **Network layer** - Here routing with data packets is managed here you deal with IP, ICMP IPSec and more
6. **Data link layer** - Here node to node transfer and error detection is managed and you come across things like frames, ethernet, switches, bridges and more
7. **Physical layer** - Physical layer between devices fibres, wireless, hubs and more

![OSI Model Overview](https://github.com/user-attachments/assets/dc41c6ed-b3ec-42f2-83ce-657ee77e5d96)

---

## 7 Layers in More Detail:

### Layer 1 - Physical Layer:
This layer transmits raw bit streams over the physical medium. This deals with hardware connection such as cables, switches and network interface cards.

Examples of physical medium:
- Copper wires that have electric signal
- Fibre light waves
- Wifi with frequency waves

Also all data is processed by all devices.

### Layer 2 - Data Link Layer:
This layer is responsible for node to node data transfer this ensures data packets are send and received correctly between different network nodes. It's all about maintaining a reliable link between different devices.

So at layer one everything is unordered and sent randomly but this layer fixes that putting your data into frames that are organised. Now frames are like envelopes that carry the data and ensure it gets to the right places.

Components that are used here are mac addresses, switches and bridges.

### Layer 3 - Network Layer:
This layer determines how data is sent to recipients and manages packets forwarding including routing through different routers. It decides the best path for data to travel in a network ensuring it gets to the right place.

Components that are used here are IP addresses and routers.

### Layer 4 - Transport Layer:
This layer is responsible for providing reliable data transfer services to the upper layers. It is like the delivery service that ensures your data arrives safely and in correct sequence.

The protocols that allow this to happen are tcp and udp:
- **TCP** provides reliable audited and error free data
- **UDP** does the same but its more faster and less reliable

### Layer 5 - Session Layer:
This layer is responsible for 3 things: establishing, managing and terminating session.

- **Establishing session** - session is getting started e.g logging into website
- **Maintaining session** - keeping the session alive and running ensuring requests continue smoothly
- **Terminating session** - Ending the session e.g logging out the browser

Components that are used here are session management protocols such as RPC, NetBIOS and more.

### Layer 6 - Presentation Layer:
This layer is also known as the syntax layer because it ensures data being sent is in a useable or readable format. Its like a translator that translate data into a format the application layer can understand.

Components:
- **Encryption** - ensures data security e.g plain text can be encrypted text
- **Data formatting** - can convert things into a format for example JPEG or PNG also thing like SSL and TSL

### Layer 7 - Application Layer:
This layer provides network services directly to applications this also could be the end user layer where everything happens when a user interacts with a device. Handles things like web browsing, file transfers and emails.

Components used in there are:
- **HTTP** to access web services
- **FTP** to transfer files
- **SMTP** to send emails

![OSI Model Detailed Diagram](https://github.com/user-attachments/assets/3039e016-cff5-4d91-8454-cd9a45373ccf)

---

## TCP/IP Model

This model is the backbone of the internet and is a condensed format of the OSI model. This model has 4 layers:
1. Application layer
2. Transport layer
3. Internet layer
4. Network access layer

![TCP/IP Model](https://github.com/user-attachments/assets/6f481cf7-c9ff-4270-bdea-f3487e3bc4e6)

### Application Layer
This layer is where the network applications and their protocols operate. It's responsible for things like web browsing, email, DNS lookups, and more — basically any app that uses the network.

Examples of protocols used here:
- **HTTP** – used for web pages
- **TLS** – adds encryption and security
- **DNS** – turns domain names (like google.com) into IP addresses

### Transport Layer
This layer is responsible for end-to-end communication and data transfer between devices. It's like the delivery service that ensures your data reaches its destination safely and in the correct order.

Protocols used here:
- **TCP** – reliable, ordered, and error-checked
- **UDP** – faster, but less reliable; no error checking

### Internet Layer
This layer is responsible for logical addressing and routing data across different networks. It determines how data is sent to the recipient and chooses the best path through routers to get it there.

Components used here:
- **IP (Internet Protocol)** – handles delivery of packets across networks
- **Routers** – direct traffic between networks

### Network Access Layer
This is a condensed version of Layer 1 and Layer 2 of the OSI model. It deals with the physical and data link aspects of networking. This layer handles the actual sending of data over cables or Wi-Fi, and ensures the device connects properly to the network.

Examples of technologies used here:
- Ethernet
- Wi-Fi
- MAC addresses
- LAN protocols

---

## OSI Layer Process Examples

### OSI Layer - POV from Sender:
![OSI Sender Perspective](https://github.com/user-attachments/assets/d99a8552-e361-4d06-a7f6-8623354fcc7c)

### OSI Layer - POV from Receiver:
![OSI Receiver Perspective](https://github.com/user-attachments/assets/6d945686-df23-40c1-b83c-3dc1150c8c68)

---

## Chapter 3: DNS

### What is DNS?
**DNS – Domain Name System**

DNS is like a contacts list for the internet. It allows users to access websites using domain names instead of IP addresses, which are harder to remember. Behind the scenes, DNS translates domain names into IP addresses so devices know where to send requests. Without DNS, users would need to manually type long IP addresses to visit websites.

Examples of how DNS helps:
- Type www.google.com instead of 192.168.0.5
- Helps your browser find and connect to the correct server
- Acts like a phonebook for websites
- Makes the internet easier and more human-friendly

![DNS Overview](https://github.com/user-attachments/assets/34ff07f2-4b72-437c-b9d3-e7a2557f74f9)

---

### DNS Components: Nameservers and Zone Files

#### Name Servers:
There are 2 types authoritative and recursive name servers:

**Authoritative name servers** hold the actual DNS records when queried they provide a definite answer IP address for a domain name.

**Recursive name servers** these servers do not hold the final answer instead they query other name servers on behalf of the client to find the correct DNS Record they can also cache the information they retrieved to speed up queries.

#### Practical Finding DNS Server of a Domain
`dig ns (domain)`

![DNS dig command](https://github.com/user-attachments/assets/1b36289a-4db8-4e02-8d9e-3497290a1176)

The commands just to get DNS:
`dig +short ns (domain name)`

![DNS short command](https://github.com/user-attachments/assets/44de7897-a6f9-4477-b5eb-be2ec7833bee)

#### Zone Files:
Zone files are stored inside your name service and they contain information about the domain. They help name servers answer queries about how to get to a domain if the name server doesn't know the answer directly. Zone files organise you DNS information in a readable and managed way making it easier to handle.

![Zone Files](https://github.com/user-attachments/assets/9ce273ac-791e-4bb3-a03e-2a25d748b74e)

---

### DNS Components: Records

A zone file is composed of many records. Each record contains specific information about hosts, names servers and other resources.

**Resource components**: Record names, TTL, Class, Type, data
- **Record name** - domain name being queried
- **Time to live (TTL)** indicates how long a record is valid before refresh required
- **Class** - name space of the record information
- **Type** - type of record (A or MX or AAAA etc)
- **NS** - name server record
- **Data** - The actual information corresponding to the record type. Like IP address for an A record

![DNS Record Components](https://github.com/user-attachments/assets/2d36c599-d0cb-464c-afca-ff64f8cfaf76)

#### DNS Records:
- **A** – Maps a domain name to an IPv4 address
- **AAAA** – Maps a domain name to an IPv6 address
- **CNAME** – Alias of one name to another. It allows you to point multiple domain names to the same IP address
- **MX** – Specifies the mail server responsible for receiving email for the domain
- **TXT** – Allows domain administrators to insert any text into DNS

Commonly used for:
- Verification purposes
- Holding SPF (Sender Policy Framework) data

![DNS Records Types](https://github.com/user-attachments/assets/12a1c57e-e1dc-46b8-8faa-46d97aa8289f)

#### A Record Example
Most common type of dns record and essential for directing traffic to the correct ip address:

![A Record Example](https://github.com/user-attachments/assets/69c633ee-4f08-44b7-a7fb-134c929c1fdc)

#### AAAA Record Example
Same as above but less common:

![AAAA Record Example](https://github.com/user-attachments/assets/9a19ae8d-da7f-4a0c-b3e4-cd12c7982fe7)

#### CNAME Record Example
This create and alias for your domain name makes DNS management easier by allowing you to point different domain names to 1 IP address:

![CNAME Record Example](https://github.com/user-attachments/assets/5ff46f63-919b-4a28-9014-c4c59a65f8be)

#### MX Record Example
Essential for routing emails to the correct mail servers ensuring email delivery is reliable:

![MX Record Example](https://github.com/user-attachments/assets/057fc3ac-c30b-446f-a4d9-cbbd103fe102)

#### TXT Record
One of the main purposes is to verify you own the domain but also has many purposes:

![TXT Record Example](https://github.com/user-attachments/assets/434f4676-4f2c-420f-a0aa-a0edad270fc1)

---

### How DNS Works:

#### What is DNS Resolution:
DNS resolution is the process of converting domain names into IP addresses.

#### DNS Break Down:
- **DNS Root (the boss)** - This is the top of the hierarchy, it doesn't store details about specific domains, but rather keeps high level information on where to find the top-level domains underneath it

- **TLD's Top Level Domains** - These are like calling your department heads they include familiar extensions such as .com, .org, .net. Each TLD stores information about domains within the scope

- **Authoritative name servers Host+Zones for domains** - This is where the details DNS records for those domains for example google.com have their own records stored in here

- **Domain** - each domain has a zone and zone file where the zone is like a team within a department and the zone file is a detailed list of information

This is where information such as IP addresses, mail servers of the domains are stored.

![DNS Hierarchy](https://github.com/user-attachments/assets/fb947cd1-199c-457e-a84c-a2695a64f710)

This hierarchy ensures when you type a web address into a browser it will find the right ip.

---

### DNS Resolution Process

#### 🌐 What Happens When You Type www.google.com into Your Browser
**✅ Step-by-Step DNS Lookup Process:**

1. **User Action** - You type www.google.com into your browser

2. **Browser Checks Cache** - Browser checks its local DNS cache. If the IP is stored, it uses it. If not, it sends a request to the local DNS resolver (usually your ISP's resolver)

3. **DNS Resolver Checks Its Cache** - The resolver checks its own memory. If it doesn't have the IP address, it proceeds to query external DNS servers

4. **Query to Root DNS Server** - The root server doesn't have the IP. But it knows where to find the TLD (Top-Level Domain) server for .com

5. **Query to .com TLD Server** - The TLD server also doesn't have the IP for google.com. But it knows the address of Google's authoritative name server

6. **Query to Authoritative Name Server** - The authoritative name server for google.com has the correct IP. Example response: 142.250.180.14

7. **DNS Resolver Sends IP to Browser** - The resolver returns the IP address to your browser

8. **Browser Connects to Web Server** - Browser uses the IP to connect to Google's web server

9. **Website Loads** - Google.com opens in your browser

Example image:

![DNS Resolution Example](https://github.com/user-attachments/assets/f1fbefc6-02ea-446b-a3c1-7b6427dee8aa)

#### 📡 DNS Query Process – Step-by-Step Notes

**🔸 1. Client Starts the Process**
A device (e.g. your computer) wants to visit qq.com. It first checks the following locally:
- Local DNS cache
- /etc/hosts file (used in systems like Linux)

✅ If the IP is found → the process ends here  
❌ If not found → it sends a DNS query to the configured DNS resolver

**🔸 2. DNS Resolver Checks Its Own Cache**
Resolver = like a librarian who knows where to look  
✅ If it has the IP address in its cache → it returns it to the client  
❌ If not found → it begins a series of external queries

**🔁 The Query Chain Begins (Recursive Lookup)**

**🔹 3. Resolver Queries the Root DNS Server**
The Root server is the top-level. It doesn't know the IP of qq.com, but it knows who handles .com  
✅ It responds with the address of the .com TLD server

**🔹 4. Resolver Queries the .com TLD Server**
The .com TLD server doesn't know qq.com's IP, but it knows which authoritative name server handles qq.com  
✅ It replies with the address of qq.com's name server

**🔹 5. Resolver Queries the Authoritative Name Server (qq.com)**
This is the final step in the query chain. The authoritative name server for qq.com provides:  
✅ The DNS records (including the IP address of qq.com)

**🔸 6. Resolver Caches the Result**
The resolver stores the IP for qq.com to answer future queries faster

**🔸 7. Resolver Sends IP to the Client**
The resolver returns the final IP address to the client. The client can now connect directly to qq.com's web server using that IP

**✅ Summary of Query Flow**
Client ➜ Local Cache / /etc/hosts ➜ DNS Resolver Cache ➜ Root DNS Server ➜ TLD (.com) Server ➜ Authoritative Name Server (qq.com) ➜ Resolver returns IP to client

![DNS Query Process](https://github.com/user-attachments/assets/67ef09a4-6746-4e5d-ae63-fc4443aed77c)

---

### Network Debugging Tools: 'nslookup' and 'dig'

**nslookup** - is a basic query tool for DNS, when you use it you can find information about a DNS records for that certain domain  
Syntax: `nslookup (domain)`  
Example: `nslookup www.google.com`

**dig** - is an advance query tool and provides more information than nslookup  
Syntax: `dig (domain)`  
Example: `dig www.google.com`

#### nslookup google.com – Explained
- **Server: 10.255.255.254** → This is your local DNS resolver (likely your router or ISP DNS)
- **Address: 10.255.255.254#53** → The #53 means it's using port 53, the standard DNS port
- **Non-authoritative answer:** → The result came from cache, not directly from Google's DNS server
- **Multiple IPs (IPv4 & IPv6):** → These are the actual IP addresses for google.com. Google uses many IPs for load balancing

![nslookup Example](https://github.com/user-attachments/assets/05e7f7ed-2128-467a-8df6-3b9aead2ca25)

#### DIG Command Breakdown – dig google.com
- **QUESTION SECTION** → Shows the query you made (asking for A records of google.com)
- **ANSWER SECTION** → Returns the IP addresses for google.com. Here, it lists multiple IPs (used for load balancing)
- **Query Time** → The DNS lookup took 22 milliseconds
- **SERVER** → The DNS server used was 10.255.255.254 on port 53 (UDP)
- **WHEN** → Shows the date and time the query was made
- **MSG SIZE** → The size of the response message: 135 bytes

![dig Command Example](https://github.com/user-attachments/assets/d14051d9-d834-427d-b7f5-4e2e4e77d7c0)

---

### /etc/hosts File:

/etc/hosts can be use to map domains to IP addresses.

**What is a /etc/hosts** - its a local file on your computer that maps domain names to an IP address. It allows you to override DNS settings for certain domains by providing an alternative IP address.

#### How it works:
When you type a domain name into your browser your computer looks at the /etc/hosts file to see if the domain is listed there. If its there it will use the provided IP address instead of querying the dns server which is good for troubleshooting, developing or testing.

#### How to edit /etc/hosts?
Open text editor or vs code admin privileges are required. Add entry in this format: `IP_ADDRESS DOMAIN_NAME`  
Example: `123.0.0.1 example.com`

Tasks:

![etc/hosts Tasks](https://github.com/user-attachments/assets/5287fe82-411e-48fb-84d4-8e06523441ef)

---

## CH4 Routing

### What is Routing and Why is it Important
Routing is the process of deciding the best path for your data to travel across different networks like a gps for your data which figured out the best route from point a to b. Routing makes sure data is reaches its destination quickly and effectively without any issues. Routing is fundamental for the internet to run smoothly and its what keeps the communication of the internet streaming.

Router is the component. Routing tables is what they use to help send data.

#### Data Routing – Step-by-Step Overview

1. **Start at Computer 1 (Your Device)** - You send a message or request (e.g., visiting a website, sending an email)

2. **Data Sent to Your Router** - The router is the first stop for your data. It checks its routing table to decide the best next hop for the data

3. **Router Forwards the Data** - Based on the routing table, your router determines the best network path. The data is sent to the next router on the path

4. **Data Hops Through Multiple Networks** - The data might pass through multiple networks (e.g., Network 1 → Network 3 → Network 4). Each router along the way repeats the process: checks its routing table, finds the best next hop, and forwards the data

5. **Final Destination – Computer 2** - After passing through several networks, the data finally reaches its intended destination, Computer 2

**Routing Summary:** Routing = Finding the best path for data to travel across multiple networks from the source to the destination. It ensures data is delivered efficiently and correctly, even if it takes different paths each time.

Diagram of routing:

![Routing Diagram](https://github.com/user-attachments/assets/a52926ad-1bf5-4bbe-a734-4d51e4b8cbea)

#### Why is Routing Important in DevOps
- **Network performance optimisation** - when your router is good this ensures your data packets take a good path reducing latency making it faster
- **Ensures reliable application delivery** - proper routing is crucial for delivery applications and services especially in complex cloud environments
- **Crucial for managing complex infrastructure**

---

### Static and Dynamic Routing

#### Static Routing:
This is where routes are manually set up by network admins and its like giving you data a fixed map to follow. Its reliable but doesn't adapt well if there is a change to the route or any issues if the route changes you have to update it manually. Its good for small and stable networks but not good for big networks.

#### Dynamic Routing:
However dynamic is more effective as it uses algorithms and much more complex protocols to automatically find the best path for data its more flexible and adapts to network change. Automatically adjust routes based on the condition. This is used for larger tasks as its scalable and adaptable.

---

### Common Routing Protocols:

#### What are Routing Protocols
Routing protocols are necessary because they automate the process of the best route for data to travel across a network. Instead of setting routes manually the protocols do it for us and its like having smart assistant the constantly updates your directions also they enhance network efficiency by making your data choose the fastest route.

They use algorithms to figure out the best path for data to travel. They also automate routing updates meaning you don't have to manually configure everything and they improve network resilience by finding alternative paths if one goes down.

#### 2 Common Routing Protocols
**OSPF and BGP**

#### OSPF (Open Shortest Path First) – Key Points
- **Name & Function** - OSPF = Open Shortest Path First. As the name suggests, it finds the shortest path for data to travel
- **Where It's Used** - Mainly used within large organizations (an interior routing protocol)
- **How It Works** - Uses link-state information to make routing decisions. Considers the status of network links and the cost of using them
- **Fast Convergence** - Can quickly recalculate routes when changes occur in the network (e.g., a router goes down)
- **Why It's Important** - Provides efficient routing with minimal delay when the network topology changes

#### BGP (Border Gateway Protocol) – Key Points
- **Name & Function** - BGP = Border Gateway Protocol. Used for routing between different autonomous systems (AS)
- **Autonomous Systems** - An autonomous system = a large network managed by a single organization. BGP connects these large networks together
- **How It Works** - Uses a path vector mechanism: Maintains and updates path information as network topology changes
- **Routing Policies** - Network admins can define routing policies based on attributes. Provides fine control over how traffic flows between networks
- **Extra Complexity** - BGP is more complex and powerful than OSPF. It's mainly covered in advanced networking topics (not in this course)

![Routing Protocols](https://github.com/user-attachments/assets/b4f78166-c3c4-4928-a718-f405865e6439)

CH 5 Subnetting
Subnetting is dividing 1 large network into smaller networks
CIDR notation:
stands for classless inter domain routiing now this is a method for allocating IP addresses and routing ID packets
frormat: IP_address/prefix_length
example: 192.168.1.0/24

the ip address is the network address and the /24 indicates the first 24 bits

binary basics:
Binary is everywhere in networking and computer science. It’s the language computers use — made up of only 1s and 0s — and understanding it is key to learning how IP addresses, subnetting, and routing work.

The binary system is called base-2, meaning each digit (called a bit) can only be 0 or 1. Computers like this because it’s easy for hardware to handle — 0 = off, 1 = on.

🔢 Binary to Decimal – Quick Example
Take the binary number 101010. Each bit represents a power of 2, starting from the rightmost digit, which is 2⁰.

Breakdown:

1×2⁵ = 32

0×2⁴ = 0

1×2³ = 8

0×2² = 0

1×2¹ = 2

0×2⁰ = 0

Add them up: 32 + 0 + 8 + 0 + 2 + 0 = 42

So, 101010 in binary = 42 in decimal.

🌐 Converting an IP Address to Binary
IP addresses like 192.168.1.1 are made up of 4 octets. Each octet is just a normal decimal number (0 to 255), but behind the scenes, it's stored as an 8-bit binary number.

Let’s convert 192 to binary:

Start dividing 192 by 2 and record the remainders:

192 ÷ 2 = 96 → R 0

96 ÷ 2 = 48 → R 0

48 ÷ 2 = 24 → R 0

24 ÷ 2 = 12 → R 0

12 ÷ 2 = 6 → R 0

6 ÷ 2 = 3 → R 0

3 ÷ 2 = 1 → R 1

1 ÷ 2 = 0 → R 1

Now read the remainders backwards: 11000000

So, 192 in binary = 11000000

Now let’s do the full IP: 192.168.1.1

192 → 11000000

168 → 10101000

1 → 00000001

1 → 00000001

So the binary version of 192.168.1.1 is:
11000000.10101000.00000001.00000001

📝 Practice Example (with answer)
Convert the following:

IP Address: 10.0.0.1

Subnet Mask: 255.0.0.0

Answer:

10 → 00001010

0 → 00000000

0 → 00000000

1 → 00000001

IP in binary = 00001010.00000000.00000000.00000001
Subnet in binary = 11111111.00000000.00000000.00000000

📊 Binary Conversion Chart (0–255)
Decimal	Binary		Decimal	Binary		Decimal	Binary
0	00000000		64	01000000		128	10000000
1	00000001		65	01000001		192	11000000
2	00000010		66	01000010		200	11001000
10	00001010		100	01100100		224	11100000
42	00101010		168	10101000		255	11111111

📝 Tip: Only need to memorise a few (like 0, 1, 10, 128, 192, 255) for subnetting and IP address tasks.

Let me know if you want a printable version or to move on to subnetting next!








You said:
i mean can you do what each number set means to the max like 1 = 1 1=2 1 =4 ect in a list 


ChatGPT said:
Ah got it! You're asking for a binary place value chart, showing what each bit position represents — basically, the power of 2 for each place in an 8-bit binary number (like an IP octet). Here's the list:

📘 Binary Place Value Chart (8-bit)
Each position in a binary number represents a power of 2, starting from the right (least significant bit).

Bit Position	Binary Value	Meaning (2ⁿ)
1st (right)	00000001	2⁰ = 1
2nd	00000010	2¹ = 2
3rd	00000100	2² = 4
4th	00001000	2³ = 8
5th	00010000	2⁴ = 16
6th	00100000	2⁵ = 32
7th	01000000	2⁶ = 64
8th (left)	10000000	2⁷ = 128

🧠 Tip: To convert binary to decimal, just add up the values of each 1-bit.
Example: 10101000 → 128 + 32 + 8 = 168

Let me know if you want a version for 16-bit or more!

calculating subnets:
subnet masks:
a subnet mask is used to divide an ip address into network and host portions 
It helps routers determine which part of an IP address is the network address and which part is the host address

For example, if the subnet mask is 255.255.255.0, it means the first three numbers (255.255.255) are the network, and the last number (0) is for hosts — the devices on that network.

That means the first 24 bits (3 × 8 bits) are for the network, and the last 8 bits are for the host devices. This is also written as /24. That “slash 24” just means 24 bits are for the network.

In the image, you can see how this works for different IP classes:

Class A uses 255.0.0.0 → only the first 8 bits are network bits

Class B uses 255.255.0.0 → the first 16 bits are for the network

Class C uses 255.255.255.0 → the first 24 bits are for the network

So the more 255s you have in the subnet mask, the more bits are used for the network, and the fewer bits are left for devices. Subnet masks basically help devices know what part of an IP address is the main network, and what part can change to talk to different devices.
<img width="404" height="292" alt="image" src="https://github.com/user-attachments/assets/99fc8b2f-acd1-436f-8801-89970dc657e6" />

NAT network address calculation

converts private ips for different devices into 1 singular ip for the internet 
without nat each device would need thir own ip to acces the internet limiting praticality as ipv4 is running out of nunbers
also hels internal network talk to the inetrnet 

how nat wirks:
process:
internal devices use private ip address 
then router translates private IP to public IP 
then communication is faccilitates between networks

Let’s say you have a device like a computer on your home network. It has a private IP address — for example, 192.168.1.10. Now this device wants to send data to a website with a public IP address, like 172.217.1.46.

When your computer sends the data, it first goes to your router. This is where NAT comes in.

Your router uses NAT to change the source IP from your private IP (192.168.1.10) to your public IP address. Let’s say your public IP is 98.117.53.254. This step is important because the internet doesn’t recognize private IPs — it only accepts public IP addresses.

So, your router sends the data out using 98.117.53.254 as the source IP. When the website receives the request, it sees your public IP (the router’s IP) and sends the response back to it.

When that data comes back, the router uses NAT again to translate the public IP back to your private IP, and then it delivers the data to your device (192.168.1.10).
<img width="687" height="166" alt="image" src="https://github.com/user-attachments/assets/ddeb0a8f-4c96-4067-a9ed-c26d4a581c9f" />

types of NAT:
static NAT - it maps a single private Ip address to a single public IP address its direct mapping and is liek hving a 1-1 translater for your device
useful if you have a device that needs to be accessed from 1 ip all the time like a web server 

dynamic NAT - unlike static this doesnt map 1-1, it maps a private ip address to one of many public ip addresses in a pool
its like a pool of translators that can handle different devices as needed
This way your device gets an ip adress when they need to use the internet
once done the ip address goes back to the pool for some one else to use

PAT Port address translation  - Pat is useful because of its efficiency it allows multiple devices on a local network to be mapped to a single public ip address but with different port numbers 
it can assign diofferent ports to different devicces under 1 public ip 
this is what many home routers use as its a great way to save public IP ADRESSES 

Simple NAT example
<img width="571" height="292" alt="image" src="https://github.com/user-attachments/assets/11abd816-93f0-4d7c-a8d2-66da8975115f" />

Why is it important for engineers
conserves public ip addresses
enchances network security 
simplifies network design and management 

CH 6 network trouble shooting






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


TCP/IP Model
This model is the backbone of the internet and is a condense format of th OSI model
This model has 4 layers 
application layer
transport layer 
internet layer 
networj access layer 
<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/6f481cf7-c9ff-4270-bdea-f3487e3bc4e6" />

Application Layer
This layer is where the network applications and their protocols operate.
It's responsible for things like web browsing, email, DNS lookups, and more — basically any app that uses the network.
Examples of protocols used here:
HTTP – used for web pages
TLS – adds encryption and security
DNS – turns domain names (like google.com) into IP addresses

Transport Layer
This layer is responsible for end-to-end communication and data transfer between devices.
It's like the delivery service that ensures your data reaches its destination safely and in the correct order.
Protocols used here:
TCP – reliable, ordered, and error-checked
UDP – faster, but less reliable; no error checking

Internet Layer
This layer is responsible for logical addressing and routing data across different networks.
It determines how data is sent to the recipient and chooses the best path through routers to get it there.
Components used here:
IP (Internet Protocol) – handles delivery of packets across networks
Routers – direct traffic between networks

Network Access Layer
This is a condensed version of Layer 1 and Layer 2 of the OSI model.
It deals with the physical and data link aspects of networking.
This layer handles the actual sending of data over cables or Wi-Fi, and ensures the device connects properly to the network.
Examples of technologies used here:
Ethernet
Wi-Fi
MAC addresses
LAN protocols

OSI Layer - a pov froms sender
<img width="667" height="354" alt="image" src="https://github.com/user-attachments/assets/d99a8552-e361-4d06-a7f6-8623354fcc7c" />
OSI Layer - a pov froms reciever 
<img width="674" height="357" alt="image" src="https://github.com/user-attachments/assets/6d945686-df23-40c1-b83c-3dc1150c8c68" />

CH 3 DNS
What is DNS?
DNS – Domain Name System
DNS is like a contacts list for the internet.
It allows users to access websites using domain names instead of IP addresses, which are harder to remember.
Behind the scenes, DNS translates domain names into IP addresses so devices know where to send requests.
Without DNS, users would need to manually type long IP addresses to visit websites.

Examples of how DNS helps:

Type www.google.com instead of 192.168.0.5
Helps your browser find and connect to the correct server
Acts like a phonebook for websites
Makes the internet easier and more human-friendly
<img width="275" height="183" alt="image" src="https://github.com/user-attachments/assets/34ff07f2-4b72-437c-b9d3-e7a2557f74f9" />


DNS Components: Nameservers and zome files.
Name servers: 
There are 2 types authrative and recursive name servers
Authartative name servers hold th actual DNS records when quiried they provide a definite answer IP address for a domain name
Recursive name servers these servers do not hold the final answer instead they quirey other name servers on behald of the cluient to fidn the correct DNS Record they can also catch the information they retrived to speed up queries

pratical finding DNS server of a domain 
Dig ns (domain)
<img width="857" height="612" alt="image" src="https://github.com/user-attachments/assets/1b36289a-4db8-4e02-8d9e-3497290a1176" />

the commands just to get DNS
dig +short ns (domain name)
<img width="1078" height="205" alt="image" src="https://github.com/user-attachments/assets/44de7897-a6f9-4477-b5eb-be2ec7833bee" />

Zone files:
zone files are stored inside your name service and they contain information about the domain
They help name servers answer queries about how to get tooa  domain if the name server doesnt know the answer directly 
Zone files organise you DS information in a readable and managed way making it easier to handle 
<img width="1960" height="1250" alt="image" src="https://github.com/user-attachments/assets/9ce273ac-791e-4bb3-a03e-2a25d748b74e" />

DNS Components: records 
Az zone file is composed of many records 
Each record contains specific information about hosts, names servers and other recourses 
Resource components: Record names,TTL, Class, TYpe, data 
Record name - domain name being quired
Time to live (TTL) indicates how long a record is valid before refresh required
Class - name space of the record information 
Type - type of record (A or MX or AAAA etc)
NS - name server record
data - The actual information corresponding to the record type. Like IP address for an A record
<img width="656" height="246" alt="image" src="https://github.com/user-attachments/assets/2d36c599-d0cb-464c-afca-ff64f8cfaf76" />

DNS records:
A – Maps a domain name to an IPv4 address.
AAAA – Maps a domain name to an IPv6 address.
CNAME – Alias of one name to another. It allows you to point multiple domain names to the same IP address.
MX – Specifies the mail server responsible for receiving email for the domain.
TXT – Allows domain administrators to insert any text into DNS.
Commonly used for:
Verification purposes
Holding SPF (Sender Policy Framework) data
<img width="744" height="207" alt="image" src="https://github.com/user-attachments/assets/12a1c57e-e1dc-46b8-8faa-46d97aa8289f" />

A record example - most common type of dns record and essential for directing trafic to the correct ip address 
<img width="611" height="114" alt="image" src="https://github.com/user-attachments/assets/69c633ee-4f08-44b7-a7fb-134c929c1fdc" />

AAAA record example - same as above but less common
<img width="615" height="116" alt="image" src="https://github.com/user-attachments/assets/9a19ae8d-da7f-4a0c-b3e4-cd12c7982fe7" />

CNAME record example - this create and alias for your domain name makes DNS managment easier by allwoing you to point different domain names to 1 IP address 
<img width="600" height="137" alt="image" src="https://github.com/user-attachments/assets/5ff46f63-919b-4a28-9014-c4c59a65f8be" />

MX record example - essential for routing emails to the correct mail servers ensuring email delibvery is reliable
<img width="601" height="141" alt="image" src="https://github.com/user-attachments/assets/057fc3ac-c30b-446f-a4d9-cbbd103fe102" />

TXT record - one of the main purposes is to verify you own the domain but also has many purposes 
<img width="603" height="137" alt="image" src="https://github.com/user-attachments/assets/434f4676-4f2c-420f-a0aa-a0edad270fc1" />

How DNS works:
What is DNS resolution:
DNS resolution is the process of converting domain names into IP addresses 
DNS break down:
DNS Route (the boss) - This is the top of the hierchary, it doesnt store details about specific domains, but rather keeps high level informaion on where to find the top-level domains underneath it.

TLD'S Top Level Domains - These are liek calling your departnment heads they include familiar extentions such as .com, .org
, .net 
Each TLD stores information about domains within the cope

Authoritive name servers Host+Zones for domains - This is where the details DS records for those domains for example google.com have their own records stored in here 

Domain - each domain gas a zone and zone file where the zone is like a team within a departnemnt and the zone file is a detailed list of information

This is where imformations such as IP addresses, mail servers of the domains are stored
<img width="767" height="387" alt="image" src="https://github.com/user-attachments/assets/fb947cd1-199c-457e-a84c-a2695a64f710" />

This hierachy ensures when yoy type a web address into a browser it will find the right ip 

DNS resulution process 
🌐 What Happens When You Type www.google.com into Your Browser
✅ Step-by-Step DNS Lookup Process
1. User Action
You type www.google.com into your browser.

2. Browser Checks Cache
Browser checks its local DNS cache.

If the IP is stored, it uses it.

If not, it sends a request to the local DNS resolver (usually your ISP’s resolver).

3. DNS Resolver Checks Its Cache
The resolver checks its own memory.

If it doesn’t have the IP address, it proceeds to query external DNS servers.

4. Query to Root DNS Server
The root server doesn’t have the IP.

But it knows where to find the TLD (Top-Level Domain) server for .com.

5. Query to .com TLD Server
The TLD server also doesn’t have the IP for google.com.

But it knows the address of Google’s authoritative name server.

6. Query to Authoritative Name Server
The authoritative name server for google.com has the correct IP.

Example response: 142.250.180.14

7. DNS Resolver Sends IP to Browser
The resolver returns the IP address to your browser.

8. Browser Connects to Web Server
Browser uses the IP to connect to Google’s web server.

9. Website Loads
Google.com opens in your browser.

example image
<img width="802" height="408" alt="image" src="https://github.com/user-attachments/assets/f1fbefc6-02ea-446b-a3c1-7b6427dee8aa" />

📡 DNS Query Process – Step-by-Step Notes
🔸 1. Client Starts the Process
A device (e.g. your computer) wants to visit qq.com.

It first checks the following locally:

Local DNS cache

/etc/hosts file (used in systems like Linux)

✅ If the IP is found → the process ends here.
❌ If not found → it sends a DNS query to the configured DNS resolver.

🔸 2. DNS Resolver Checks Its Own Cache
Resolver = like a librarian who knows where to look.
✅ If it has the IP address in its cache → it returns it to the client.
❌ If not found → it begins a series of external queries.

🔁 The Query Chain Begins (Recursive Lookup)
🔹 3. Resolver Queries the Root DNS Server
The Root server is the top-level.

It doesn't know the IP of qq.com, but it knows who handles .com.

✅ It responds with the address of the .com TLD server.

🔹 4. Resolver Queries the .com TLD Server
The .com TLD server doesn’t know qq.com’s IP,

But it knows which authoritative name server handles qq.com.

✅ It replies with the address of qq.com’s name server.

🔹 5. Resolver Queries the Authoritative Name Server (qq.com)
This is the final step in the query chain.

The authoritative name server for qq.com provides:

✅ The DNS records (including the IP address of qq.com)

🔸 6. Resolver Caches the Result
The resolver stores the IP for qq.com to answer future queries faster.

🔸 7. Resolver Sends IP to the Client
The resolver returns the final IP address to the client.

The client can now connect directly to qq.com’s web server using that IP.

✅ Summary of Query Flow
Client ➜ Local Cache / /etc/hosts
➜ DNS Resolver Cache
➜ Root DNS Server
➜ TLD (.com) Server
➜ Authoritative Name Server (qq.com)
➜ Resolver returns IP to client
<img width="796" height="460" alt="image" src="https://github.com/user-attachments/assets/67ef09a4-6746-4e5d-ae63-fc4443aed77c" />

netwrok debugging tools: 'nslookup' and 'dig'
nslookup - is a basic query tool for DNS, when you use it you can find information about a DNS records for that certain domain 
syntax: nslookup (domain)
example: nslookup www.google.com

gig - is an advance query tool and provides more information than nslookup
syntax: dig(domain)
example: dig www.google.com

 nslookup google.com – Explained
Server: 10.255.255.254
→ This is your local DNS resolver (likely your router or ISP DNS).

Address: 10.255.255.254#53
→ The #53 means it’s using port 53, the standard DNS port.

Non-authoritative answer:
→ The result came from cache, not directly from Google’s DNS server.

Multiple IPs (IPv4 & IPv6):
→ These are the actual IP addresses for google.com.
→ Google uses many IPs for load balancing.

<img width="491" height="391" alt="Screenshot 2025-07-30 174541" src="https://github.com/user-attachments/assets/05e7f7ed-2128-467a-8df6-3b9aead2ca25" />

 DIG Command Breakdown – dig google.com
QUESTION SECTION
→ Shows the query you made (asking for A records of google.com).
ANSWER SECTION
→ Returns the IP addresses for google.com.
→ Here, it lists multiple IPs (used for load balancing).
Query Time
→ The DNS lookup took 22 milliseconds.
SERVER
→ The DNS server used was 10.255.255.254 on port 53 (UDP).
WHEN
→ Shows the date and time the query was made.
MSG SIZE
→ The size of the response message: 135 bytes.

<img width="690" height="527" alt="image" src="https://github.com/user-attachments/assets/d14051d9-d834-427d-b7f5-4e2e4e77d7c0" />

./etx/hosts file:
/etc/hots can be use to map domains to IP addresses 
What is a /etc/hots - its a local file on yoru computer that maps domain namesto an IP address 
It allows you to overide DNS settings for certain domains by providing an alternitive IP address 
How it works: 
when you type a domain name into your browser your computer lookst at the /etc/hosts file to see if the domain is listed there
if its there it will use the provided IP address instead of quiring the dns server which is good for troubleshooting, developinng or testing 

how to edit /etc/hosts?
open text edito or vs code admin privilages are required 
add entry in this format IP_ADDRESS DOMAIN_NAME
example: 123.0.0.1 example.com

tasks<img width="748" height="321" alt="image" src="https://github.com/user-attachments/assets/5287fe82-411e-48fb-84d4-8e06523441ef" />

routing
what is routing ands why is it important
routing is the process of debating the best path for your data to travel across different networks like a gps for your data 
which figured out the best route from point a to b
routing makes suure data is reaches its destination quickly and effectivley without any issues 
Routing is fundemental for the internet to run smoothly and its what keeps the communication of the internet streaming 

router is the component 
routing tables is what they use to help send data
Data Routing – Step-by-Step Overview
Start at Computer 1 (Your Device)

You send a message or request (e.g., visiting a website, sending an email).

Data Sent to Your Router

The router is the first stop for your data.

It checks its routing table to decide the best next hop for the data.

Router Forwards the Data

Based on the routing table, your router determines the best network path.

The data is sent to the next router on the path.

Data Hops Through Multiple Networks

The data might pass through multiple networks (e.g., Network 1 → Network 3 → Network 4).

Each router along the way repeats the process: checks its routing table, finds the best next hop, and forwards the data.

Final Destination – Computer 2

After passing through several networks, the data finally reaches its intended destination, Computer 2.

Routing Summary

Routing = Finding the best path for data to travel across multiple networks from the source to the destination.

It ensures data is delivered efficiently and correctly, even if it takes different paths each time.
diagram of routing 
<img width="879" height="483" alt="image" src="https://github.com/user-attachments/assets/a52926ad-1bf5-4bbe-a734-4d51e4b8cbea" />

why is routing imporyant in dev ops
network performance optomisation - when your router is good this ensures your data packets take a good path redcuing latency making it faster 
ensures reliable application delivery - proper routing is crucial for delivery applications and services especially in complex coud environments 
crutial for maniging complext infrastructure 

static and dynamic routing 
static routing:
This is where routes are manually set up by networj admins and its liek giving you data a fixed map to follow 
its reliable but doesn adapt well if there is a change to the route or any issues if the route changes you have ti update itr manually
its good for small and stable networks but not good for big networks 

Dynamic routing:
how ever dyanmic is more ffective as it uses algorithms and much more complex protocals to automaticly find the best path for data its more flexible and adapts to network change 
automaticly adjust routes based on the condition 
this is used for larger tasks as its scalable and adaptable 

common routing protocals:
whata re routing protocals
routing protocals are necessary because they automate the provess of the best  route for data to travel accross a newtwork 
instead fo setting routes manually the protocols do it for us and its like having smart assistant the constantly updates your directions alsomthey enchance network effieciency by making your data choose the fastest route 

they use algorthsms to figure out the best path for data rto travel 
they also automate routing updates meaning you dont have to manually configiure evrrytging 
and they improve network eresilliencve by finding alternitive paths if one goes down

2 cokmmon routing protocols 
OSPF and BGP

OSPF (Open Shortest Path First) – Key Points
Name & Function

OSPF = Open Shortest Path First.

As the name suggests, it finds the shortest path for data to travel.

Where It’s Used

Mainly used within large organizations (an interior routing protocol).

How It Works

Uses link-state information to make routing decisions.

Considers the status of network links and the cost of using them.

Fast Convergence

Can quickly recalculate routes when changes occur in the network (e.g., a router goes down).

Why It’s Important

Provides efficient routing with minimal delay when the network topology changes.

BGP (Border Gateway Protocol) – Key Points
Name & Function

BGP = Border Gateway Protocol.

Used for routing between different autonomous systems (AS).

Autonomous Systems

An autonomous system = a large network managed by a single organization.

BGP connects these large networks together.

How It Works

Uses a path vector mechanism:

Maintains and updates path information as network topology changes.

Routing Policies

Network admins can define routing policies based on attributes.

Provides fine control over how traffic flows between networks.

Extra Complexity

BGP is more complex and powerful than OSPF.

It’s mainly covered in advanced networking topics (not in this course).
<img width="659" height="287" alt="image" src="https://github.com/user-attachments/assets/b4f78166-c3c4-4928-a718-f405865e6439" />


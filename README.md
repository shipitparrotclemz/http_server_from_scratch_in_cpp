# Recreating Trung Vuong Thien's HTTP Server from Scratch

Credits: Trung Vuong Thien

If you are reading this, thank you so much for graciously sharing your chain of thought and details of your implementation!

To our parrots who are curious on recreating this repository in his words, you can check out his github blogpost here!
- https://trungams.github.io/2020-08-23-a-simple-http-server-from-scratch/

This repository recreates the HTTP Server from Scratch, and dabbles in the prerequisites we need to fully understand and build this.

## Our Requirements

- Project must be done in C++
- Server should be able to parse HTTP requests and send back responses.
- Server should handle 10,000 concurrent connections
- It can handle 100,000 requests per second
- No third-party frameworks. We are building this from the transport layer.

Our smart parrots might ask:

**Q: What is the Transport Layer?**

A: It is a layer in the TCP/IP protocol stack, responsible for providing reliable end-to-end communication between applications running on different hosts.

It is responsible for breaking up large chunks of data into smaller packets, adding necessary information such as sequence numbers and acknowledgement information. 

This ensures that the data is delivered reliably and in order. 

**Q: What is the TCP/IP protocol stack?**

It is a set of protocols used for communication between devices on a network.

It is named after two of the most important protocols it uses; The Transmission Control Protocol (TCP) and the Internet Protocol (IP).

This stack is used commonly as the standard for communication over the internet.

It contains 4 layers;

**1. Application Layer (Boundary Layer between the application and the transport layer):**
- Contains the protocols and interfaces used by applications to communicate with the network, such as HTTP (Hyper Text Transfer Protocol), SMTP (Simple Mail Transfer Protocol) , FTP (File Transer Protocol).

**2. Transport Layer (Main focus on this project):**
- Responsible for end-to-end communication between applications on different hosts. Most common protocols here are TCP and UDP. More on TCP and UDP below!

**3. Network Layer:**
- Responsible for routing packets between networks. The IP protocol is used at this layer to provide addressing and routing information for packets.

**4. Link Layer**
- Responsible for communication between devices on the same network. Includes protocol such as Ethernet and Wi-Fi.

**Q: Okay! Lets go back and focus on the Transport Layer! What is TCP and IP?**

TCP stands for Transmission Control Protocol, and IP represents Internet Protocol. 

TCP is a connection-oriented protocol that guarantees reliable data transfer.

A light-weight alternative to TCP is UDP (User Datagram Protocol), which is connectionless and does not guarantee reliable data transfer.

UDP gives the advantage of low-latency, best-effort delivery, and is used for real-time applications such as video streaming.







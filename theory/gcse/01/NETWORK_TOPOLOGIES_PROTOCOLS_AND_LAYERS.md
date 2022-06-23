# 1.5 Network topologies, protocols, and layers

## 1.5.1 Star and mesh topologies

Any device connected to a network, wired or wireless, is called a **node.** A network's **topology** is the arrangement of how nodes on a network are connected.

### Star topologies

In a star topology, all nodes indirectly connect to each other through one or more switches. The switch/es act as a *central point*, through which all communications are passed.

Large networks in a star topology are usually controlled by one or more servers, so the [client-server](WIRED_AND_WIRELESS_NETWORKS.md#client-server-networks) model normally uses a star topology. [P2P](WIRED_AND_WIRELESS_NETWORKS.md#peer-to-peer-p2p-networks) networks can also have star topologies, though, where all communications still pass through the central switch despite no single computer controlling the network.

| Advantages | Disadvantages |
| - | - |
| each node is separately connected, so a failure of a node or its link does not affect other nodes | the whole network relies on the single/few switch(es); if that fails, all nodes lose communication |
| new nodes can be easily added to the network | a wired star topology needs a lot of cable, which can be expensive in large networks |
| star networks tend to have higher performance (see [routers v. switches](WIRED_AND_WIRELESS_NETWORKS.md#routers-v-switches)) | |

### Mesh topologies

In a mesh topology, there is no central connection point; each node is connected to at least one **other node** (normally more than one) instead. The nodes act as relays, passing on a message towards its final destination.

There are two types of mesh topology:
 - In **full mesh topologies,** each node is directly connected to **every** other node. Lots of routes.
 - In **partial mesh topologies,** not all nodes are connected directly to each other. Fewer routes, simpler to implement.

Wired mesh networks tend to be uncommon as all the wires would be expensive and impractical to deal with. Wireless mesh networks, though, are increasingly being used as it is far simpler and cheaper to connect using radio signals. Mesh topologies in general are common due to their efficiency.

| Advantages | Disadvantages |
| - | - |
| messages can be recieved quicker if the route to the recipient is shorter | full mesh topologies can be impractical to set up due to the very high number of connections needed |
| messages should always get through as they have many routes to use | many connections need a lot of maintenance |
| multiple connections mean that no node should be isolated (in theory | |
| multiple connections mean each node can transmit to and recieve from multiple other nodes at the same time | |
| new nodes can be added without interruption or interference with other nodes | |

## 1.5.2 Wi-Fi

Wired networks use cables to form connections. **Ethernet** is one protocol that describes how the data is transmitted in wired networks.

However, wireless networks use wireless **Wi-Fi** signals to connect nodes. Wi-Fi signals use radio frequencies between **2.4 GHz and 5 GHz** - these wavebands can then be separated into **channels**, or **sub-frequencies.** [WAPs](WIRED_AND_WIRELESS_NETWORKS.md#wireless-access-points-waps) use several channels to allow many devices to connect without their transmissions interfering with each other.

| Advantages | Disadvantages |
| - | - |
| new nodes can easily be added | Wi-Fi signals have limited range |
| connection is wireless | Wi-Fi signals can suffer from electromagnetic interference from other devices, and can be blocked by walls |
| | each WAP only has so much bandwidth to share across nodes - therefore, more nodes connected = slower communication |
| | Wi-Fi signals pose a security risk; they can be intercepted by unauthorised users. To overcome this problem, messages should be [encrypted](#encryption). |

### Encryption

Unencrypted messages are known as **plaintext.** Encrypted message are known as **ciphertext.**

A simple method of encryption is the **[Caesar cipher](#the-caesar-cipher).** In practice, much more complicated algorithms are used to encrypt messages.

Encryption depends on a given **key.** However, it is of little use if unauthorised users know that key. One way around this issue is using an algorithm that generates two keys - a **public key** and a **private key.** This method is known as **asymmetric encryption**; a public key can be given to anyone, who can then use the key to *encrypt* the message. However, the public key **cannot decrypt the message.** The private key can; as long as it is never given out, messages can be safely encrypted.

#### The Caesar cipher
The Caesar cipher, also known as the shift cipher, is a basic algorithm that shifts each character by a given amount.

![image](https://user-images.githubusercontent.com/57215724/161044612-459aa813-571a-4eb5-aa9c-d8616c5b130c.png)

In the diagram above, the algorithm is carried out with a **left shift of 3.**

## 1.5.3 IP and MAC addressing

Protocols are rules that govern how communication is made and manage key factors such as transmission speed, error checking, and methods of addressing (e.g. how to locate another node on the network). Many types of protocol exist, but the ones that govern addressing are detailed below.

### Internet Protocol (IP) addressing

When connected to a network, each device is given a unique IP address, e.g. `192.168.0.254`. This IP address is used as the 'address' when nodes want to communicate with other nodes. A [switch](WIRED_AND_WIRELESS_NETWORKS.md#routers-v-switches) on the network knows where the node with this address is and routes the message to it accordingly.

IP addresses can be **static** or **dynamic**.

Nodes given static IP addresses **always keep the same address,** whilst a node given a dynamic address has a **different address each time it connects to the network.** This method is known as **Dynamic Host Configuration Protocol (DHCP).** Static addressing makes it easy to get the location of the node, but dynamic addressing allows more devices to connect than there are available IP addresses (when a device disconnects, its address is freed up).

**IPv4** refers to using IP addresses with four sets of digits. However, IPv4 addresses are running out due to the heavy use of the [Internet](), so a new **IPv6** version (with six sets of three digits) has been introduced.

### Media Access Control (MAC) addressing

A MAC address is a unique serial number assigned to each NIC. This allows a network to uniquely identify each device, even when DHCP is being used to generate dynamic IP addresses. The MAC address, therefore, is non-volatile and unique for each device - it is assigned by the NIC's manufacturer. **If a device has more than one NIC, each NIC will have its own MAC address.**

MAC addresses are in hexadecimal format: `1A:5B:6F:98:78:35`.

## 1.5.4 Some more protocols

Many network protocols exist. Here's some of the more common ones.
 - **TCP/IP (Transmission Control Protocol/Internet Protocol)** allows communication over the internet
 - **HTTP (HyperText Transfer Protocol)** governs communication between a *web* server and a client
 - **HTTPS (HTTP Secure)** mimics HTTP but with added secure encryption
 - **FTP (File Transfer Protocol)** governs the transmission of files accross a network and the Internet
 - **POP (Post Office Protocol)** governs the **retrieval** of emails from email servers
 - **IMAP (Internet Message Access Protocol)** is a modern replacement of POP
 - **SMTP (Simple Mail Transfer Protocol)** governs the **sending** of email to a mail server over a network

## 1.5.5 The concept of layers

Layering is to break up the sending of messages into separate components and activities, with each one managing a different part of the communication. This is the TCP/IP (see [section 1.5.4](#154-some-more-protocols) on protocols) model. There are four layers to consider:
 - The **application layer** encodes + decodes the message so it can be understood by the users
 - The **transport layer** deconstructs the message into smaller [packets](#156-packet-switching)
 - The **network layer** then adds the [IP address](#153-ip-and-mac-addressing) of the sender and recipient involved so the network knows where to send the message
 - The **data link layer** finally enables the transfer of packets between nodes on a network and also between different networks

Layering allows for standards and adaption to new hardware and software. For example, different programs can use the same transport, network, and link layers but have different application layers.

Similarly, the move from IPv4 to IPv6 only addresses the network layer, so adaption is easy.

## 1.5.6 Packet switching

Packet switching is to deconstruct messages into very small **packets,** each one holding:
 1. The **header**, including IP addresses, the packet number, total number of packets, and the details of any [protocols](#154-some-more-protocols) used.
 2. The **payload**, part of the actual message itself

Packets are sent individually across a network and reconstructed by the recipient node. The number of each packet is necessary because packets don't always go in order, but rather in whatever route is quickest.

Packet switching helps to ensure messages arrive completely without slowing the network; if a message arrives incomplete (packets are lost) then just those packets can be re-sent instead of the entire message.

## References

 - 1.5.1 [Star](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/1) and [mesh](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/2) topologies
 - [1.5.2 Wi-Fi](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/3)
 - [1.5.3 IP and MAC addressing](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/5)
 - [1.5.4 Some more protocols](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/5)
 - [1.5.5 The concept of layers](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/6)
 - [1.5.6 Packet switching](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/7)

### Sections

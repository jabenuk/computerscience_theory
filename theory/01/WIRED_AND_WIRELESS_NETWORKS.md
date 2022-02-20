# 1.4 Wired and wireless networks

## 1.4.1 Types of networks

### Local area networks (LANs)

A *LAN* is a network that is geographically confined to one building or site. Examples of LANs include networks employed by small businesses and organisations,  schools, universities, and homes. **LANs are entirely owned and maintained by the organisation** ('organisation' meaning whoever employs the LAN, like the aforementioned examples).

<img src="/resources/lan.png" height=400px/>

### Wide area networks (WANs)

A *WAN* is a network that is spread over a wider geographical area. It can cover more than one site, be spread across a country, or the entire world.

Organisations that have **more than one office or branch**, such as banks, tend to use WANs. The WAN then allows the head office to communicate and share data with sub-offices and branches. This communication usually either relies on national telephone infrastructures or wireless transmission. It is important to remember that each office or branch **still has its own LAN**, but that they are all connected together using the **WAN**.

One example of a WAN that you have probably heard of at some point is **the internet.**

<img src="/resources/wan.png" height=400px/>

## 1.4.2 Factors that affect the performance of networks

Network performance is based on **response time**: how fast a message can be sent, for example. This response time can be affected by various factors:
 - the number of devices connected to the network
 - the [**bandwidth**](#bandwidth) of the transmission medium the network relies on
 - the type of network traffic
 - network [latency](#latency) (delay)
 - the number of [**transmission errors**](#transmission-errors)

### Bandwidth

The aforementioned **bandwidth** is a measure of the amount of data the medium can transfer over a given period of time. Each transmission medium has a different bandwidth:

| Medium | Typical bandwidth |
| ------ | ----------------- |
| Twisted copper wire (TCW) | Maximum of 1 Gb\*/s |
| Fibre-optics | Over 40 Tb/s |
| Home networks | Around 54 Mb/s |
| Business networks | Maximum of 1 Gb/s |

*\*small 'b' means -bit, not -byte.*

The bandwidth of the medium is shared between each connected device; more devices = less bandwidth allocated per device = **worse response time**.

Different types of traffic usually have different bandwidth requirements; high definition video streaming needs more bandwidth than low definition; therefore, some network switches are able to determine the type of traffic and adjust the allocated bandwidth as seen fit.

### Latency

Networks with low latency experience few delays, and vice versa for networks with high latency. Latency is affected by the number of devices and **the type of connection device.**

A **hub-based network** will usually experience higher latency than a **switch-based network**, as hubs broadcast **all** messages to **all** devices. Switches only transmit messages to the intended recipient.

### Transmission errors

Inevitably, devices will try to communicate with each other **at the same time**, causing their signals to **collide** with each other. In these cases, the transmission fails. Naturally, the greater the number of devices on a network, the more chance of a collision occuring, and the long it takes to transmit a message.

### Combining transmission media

Many networks include a combination of all three media:
 - **fibre-optic cables** allow high data transmission between *different buildings.*
 - **twisted copper wire (TCW)** runs from switches to *individial devices* within the buildings.
 - **wi-fi** allows *guest devices* to connect to the network.

<img src="/resources/combining-transmission-media.png" height=400px/>

## 1.4.3 Comparing the roles of computers in client-server and peer-to-peer networks

### Client-server networks

This type of network seperates computers into two categories: **servers** and **clients.**

A server is a computer that manages and stores files, or one that provides services to other computers on the network - they tend to be quite powerful. They *'serve'* the clients. Typical servers include:
 - **file servers** hold and maintain user files
 - **applications servers** allow programs to run over a network
 - **web servers** hold and share web pages
 - **print servers** manage printing over the a network
 - **mail servers** handle emails between users

A client is a computer that relies on servers to provide data. The computer a person uses on a network is a client; it typically does not store data. Further, clients normally have no control over the network.

Client-server networks are best suited to **organisations with many computers,** or where **many computers need access to the same data.** Most schools employ client-server networks.

### Peer-to-peer (P2P) networks

In a peer-to-peer (P2P) network, all computers have equal status. Rather than servers and clients, each computer is known as a **peer.** Peers store their own files that can be accessed by other peers on the network - therefore, a peer is both a client and a server.

P2P networks are best suited for smaller organisations that have **fewer** computers, or where **fewer** computers need access to the same data.

## References

### Sections
 - [1.4.1 Types of networks (+ pictures)](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/2)
 - [1.4.2 Factors that affect the performance of networks](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/8)
 - [1.4.3 Comparing the roles of computers in client-server and peer-to-peer networks](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/3)

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

The aforementioned **bandwidth** is a measure of the amount of data the medium can transfer over a given period of time. Each transmission medium has a different bandwidth - see the section on [transmission media](#transmission-media) for some information on the ones necessary to know at GCSE.

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

## 1.4.4 Hardware associated with local area networks (LANs)

### Hubs

Hubs are small devices that allow wired connections to a network. They have **no knowledge of the devices connected;** any traffic the hub recieves is transmitted to **all** connected computers. This affect network performance, as many unnecessary signals are transmitted.

### Wireless access points (WAPs)

A wireless access point (WAP) uses a **radio transciever** to allow wireless connections to a LAN. The WAP creates its own wireless network that devices connect to, and sends this wireless traffic onto the main wired network.

WAPs can also be used to **extend the range of a wireless network.** IN this case, the WAP can either receive and transmit data to *other* WAPs, or it can be connected (via a cable) to the main network.

### Routers v. switches

Routers are used to send data signals across the **internet.** Routers collect knowledge of available routes to transmit data, before determining the most suitable one to send data. Routers are commonly used in homes; these types of routers usually contain a [hub](#hubs) and a [WAP](#wireless-access-points-waps), enabling a small [peer-to-peer](#peer-to-peer-p2p-networks) network to be formed. Additionally, they contain a **modem** - 'modulator/demodulator' - that allows users to connect to the internet.

Conversely, **switchs record which computers are connected to which ports;** when traffic is recieved, the switch forwards the traffic to its intended recipient only. This improves network performance by cutting down on unnecessary transmissions. Otherwise, switches are similar to [hubs](#hubs).

### Network interface controllers (NICs)

A network interface controller (NIC) offers an interface port for a wired connection, providing a method of connecting to a network. A *wireless* NIC also provides a **radio transceiver**, similar to [WAPs](#wireless-access-points-waps). Most modern computers have an NIC (and sometimes a wireless NIC) built-in; mobile devices, like phones, only feature a wireless NIC - giving only a wireless connection.

### Transmission media

| Medium | Typical [bandwidth](#bandwidth) | Cost |
| ------ | ----------------- | ---- |
| Twisted copper wire (TCW) | Maximum of 1 Gb\*/s | Cheap |
| Fibre-optics | Over 40 Tb/s | Expensive |
| Home networks | Around 54 Mb/s | |
| Business networks | Maximum of 1 Gb/s | |

*\*small 'b' means -bit, not -byte.*

## 1.4.5 The Internet as a worldwide collection of computer networks

The internet largely works on the [client-server](#client-server-networks) model:
 - **web servers** store and maintain web content
 - **mail servers** handle web-based email
 - **media servers** allow clients to stream media

### Domain name servers (DNS)

Domain name servers convert **domain names** (e.g. `gnu.org`) to **network (IP) addresses** (e.g. `209.51.188.116`).

### Hosting

'Hosting' refers to storing files and data on a web server (the **host**). The URL (Uniform Resource Locator) of a website includes the **host name**, e.g. `github.com` is a host name, and `www.github.com` is the full URL.

 Host names consist of three heirarchical levels. Take the host name `bbc.co.uk`:
  - the **third level** is `bbc`.
  - the **second level** is `co`.
  - the **top level** is `uk`.

### The 'cloud'

The 'cloud' is a generic term for **remotely accessed storage,** accessed through the Internet. Due to this use of the Internet, the geographical location of the server(s) the data is stored on is usually unimportant.

| Advantages | Disadvantages |
| - | - |
| files can be accessed from any location or device | unsecure; there is no guarantee that someone else is not accessing your data |
| access can be granted to another user so they can remotely access data | unreliable; there is no guarantee that your data is being backed up |
| cloud storage services back up data for you | an internet connection is required to access your own data |
| idea for low-powered devices or users that travel a lot | a *lot* of other ethical problems with data handling |

### The concept of virtual networks

A virtual network is a network of geographically unrelated devices connected via the internet. Virtual network servers create a network that has no direct physical connection, but one that allows file sharing and communication. Some organisations use virtual networks to allow users at home to connect to the organisation's data and facilities, so they can work from home.

## References

### Sections
 - [1.4.1 Types of networks (+ pictures)](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/2)
 - [1.4.2 Factors that affect the performance of networks](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/8)
 - [1.4.3 Comparing the roles of computers in client-server and peer-to-peer networks](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/3)
 - [1.4.4 Hardware associated with local area networks (LANs)](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/4)
 - [1.4.5 The Internet as a worldwide collection of computer networks](https://www.bbc.co.uk/bitesize/guides/zvspfcw/revision/5)

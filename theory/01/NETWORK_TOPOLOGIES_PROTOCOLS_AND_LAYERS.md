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

A simple \[awful algorithm, but good example\] method of encryption is the **Caeser cipher.** In practice, much more complicated algorithms are used to encrypt messages.

Encryption depends on a given **key.** However, it is of little use if unauthorised users know that key. One way around this issue is using an algorithm that generates two keys - a **public key** and a **private key.** This method is known as **asymmetric encryption**; a public key can be given to anyone, who can then use the key to *encrypt* the message. However, the public key **cannot decrypt the message.** The private key can; as long as it is never given out, messages can be safely encrypted.

## References

 - 1.5.1 [Star](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/1) and [mesh](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/2) topologies
 - [1.5.2 Wi-Fi](https://www.bbc.co.uk/bitesize/guides/zr3yb82/revision/3)

### Sections

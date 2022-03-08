# 1.6 System security

## 1.6.1 Forms of attack

Networks operate via communication, so traffic and data risk being accessed by those that have no authority to do so. A network attack is an attempt to gain access to, steal, modify, or delete data on a network. Some forms of attack are:
 - **Active:** the hacker attempts to modify or delete data, or to prevent a network from working properly. For example, *denial of service (DOS)* attacks.
 - **Eavesdropping (passive):** the hacker monitors a network to gain information, for example by *wiretapping*.
 - **External:** someone *outside* an organisation attempts to hack its network.
 - **Internal:** someone *inside* an organisation attempts to hack its network.

## 1.6.2 Threats posed to networks

### Malware

Malware is **mal**icious soft**ware**. Some types of malware include:
 - **viruses** - programs that replicate themselves and delete/modify other files
 - **worms** - similar to viruses but not hidden in other files
 - **trojans** - malware that attempts to appear legitimate
 - **spyware** - malware that monitors user activity without consent
 - **ransomware** - programs that blackmail the user into making a payment to a hacker

### Phishing

The attempt of tricking users into giving away personal details.

### Social engineering, the exploitation of human error

People may accidentally or deliberately break rules, or ignore them entirely. For example, many users choose easy-to-guess passwords, or forward viruses without using their basic ability of **common sense.** This idiotic behaviour increases the chance of a network being compromised.

### Brute force

Trying all possible combinations of characters to find a password or key.

### DOS attacks

A computer, or many computers, is used to prevent a server from performing its tasks by bombarding it with traffic.

### Data interception and theft

When data is intercepted during transmission, done using software called a **packet sniffer** such as [Wireshark](https://www.wireshark.org/), which examines data packets as they are sent around a network or across the internet. This gathered information is sent to a hacker.

### SQL injection

SQL code is entered as data input to query and recieve internal data, normally without authorisation.

### Poor network policy

When a network does not have any security rules in place. These policies tend not to have:
 - levels of access
 - rules preventing the connection of external devices such as USB memory sticks
 - regulation regarding secure passwords
 - rules to govern websites that can be accessed
 - methods to prevent any user wirelessly connecting an unsecured laptop, tablet, or smartphone
 - controls on what facilities can be accessed remotely
 - a formal backup procedure
 - a regular maintenance programme/schedule

## 1.6.3 Identifying and preventing vulnerabilities

There are many techniques that can be used to keep a network safe:

### Penetration testing

Determine how resilient a network is against attacks. Authorised users probe the network for potential weaknesses and attempt to exploit them, mimicking the behaviour of unauthorised hackers.

### Network forensics

Monitor the traffic on a network. At regular intervals, transmitted [data packets](/theory/01/NETWORK_TOPOLOGIES_PROTOCOLS_AND_LAYERS.md#156-packet-switching) are copied. The copy, and information about the packet, are then stored for later analysis - usually processed in batches. The information gathered can help identify invasive traffic, or determine where data is being sent.

### Network policies

Users of a network are often the source of threats, so a network manager should have an acceptible use policy which ensures:
 - users have a secure password that is regularly changed
 - users cannot connected unauthorised equipment to the network
 - levels of access are given
 - data on the network is regularly backed up
 - a disaster recovery procedure exists
 - regular pen testing and forensic analysis
 - regular maintenance
 - preventing physical access to servers
 - maintaining a high level of security, with up-to-date AV software and firewalls

### User access levels

Access levels determine the facilities a user has access to, such as software or important documents. A network manager should ensure users can only access the necessary facilities.

### Basic security measures

Users should have secure passwords (in accordance with the [network policy](#network-policies), and files should be encrypted.

## References

### Sections
 - [1.6.1 Forms of attack](https://www.bbc.co.uk/bitesize/guides/zj89dxs/revision/1)
 - [1.6.2 Threats posed to networks](https://www.bbc.co.uk/bitesize/guides/zj89dxs/revision/2)
 - [1.6.3 Identifying and preventing vulnerabilities](https://www.bbc.co.uk/bitesize/guides/zj89dxs/revision/3)

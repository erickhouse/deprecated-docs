
Great Networking overview Resource

http://beej.us/guide/bgnet/html/multi/index.html

# Networking

|Term|Definition|
|----|---|
|NAT|Maps public ips to private ips, typically performed by your router
|Private IP|The actual ip address associated with the machine hardware.
|Public IP| The virtual ip address that is assigned by your isp
|ISP| internet service provider
|DHCP| Dynamic Host Configuration protocol
|OSI|| The network stack
|LTE|Long Term Evolution
|Network Interface|The interface to the network on the actual hardware network card
|SCTP| The future of TCP where multiple connections can be stream concurrently|
|Router|
|Switch|
|SSL| Secure Socket Layer, an enhancement to TCP that occurs at the application layer.
|Mac Address| a 48 bit address that is assigned to your computer by the hardware manufacturer
|Modem|
|Edge|A host computer at the edge of the network
|Edge Router| The router at the edge of the network
|Ethernet| Creates a network of computers (LAN) connected by physical copper wires
|Ack|A response from the receiver of a packet that the transmission was succesful (tcp)
|FTP| File Transfer Protocol

## Open Questions

- Modem vs router vs gateway?
- Router is a gateway? 

## DHCP

A broadcast protocol to the DHCP server to aquire a public IP. Every device has a DHCP client installed on it. 

## Switches

- Routers
- Link Layer Switches

### Store and forward switching

The router will hold onto the bits of a packet before forwarding them to the next node. This syncronizes the stream so a complete packet is forwarded to the next node. 

::1 is short hand for localhost in IPv6 (just like 127.0.0.1 for IPv4)

the default port for http is port 80. Is is normal for each protocol to have a default port.

## Ethernet

Ethernet uses mac addresses which are on the physical hardware to communicate to each other. When many computer are on an ethernet network the wires can be busy. Messages are broadcasted out to every edge of the network which clogs up the pipes. Switches are introduced to determine if the message actually needs to be send to a certain part of the network. 

## Peer to Peer

A network pattern where both hosts can send and recieve message to each other.

## Ports

Ports are used to distinguish 1 or more service running on a specific host. IP will only get you to the actual host. 

## Packet Encapsulation

The communication between layers in either the OSI or the TCP/IP stacks is done by sending packets of data from one layer to the next, and then eventually across the network. Each layer has administrative information that it has to keep about its own layer. It does this by adding header information to the packet it receives from the layer above, as the packet passes down. On the receiving side, these headers are removed as the packet moves up.

## Gateway

A generic term to connection 1 or more networks

## Conectionless vs Connection models

IP - Conetionless. Packets can arrive in any order
TCP Connection. Packets are organized into a specific order.

## TODO

- NAT and DHCP seem to be related to each other
- 0.0.0.0/0 seems to be a magic address that mean all addresses.

## Netork Types

A Wide Area Network (WAN) connects computers across a larger physical area, such as between cities. There are other types as well, such as MANs (Metropolitan Area Network), PANs (Personal Area Networks) and even BANs (Body Area Network).

Off of an IPv4 address depending on the network type the bytes in the string denote the address space for the network vs the hosts in the network. 

[0.0.0].[0]

The first 3 bytes are used to address the network where the right most byte is used to address the hosts in the network. In this case up to 255 hosts can be addressed. 

In a class A network, the first byte identifies the network, while the last three identify the device. There are only 128 class A netowrks.

- Class A networks, owned by the very early players in the internet space such as IBM, the General Electric Company and MIT. The first byte addresses the network.

- Class B networks use the first two bytes to identify the network and the last two to identify devices within the subnet. 

- Class C networks use the first three bytes to identify the network and the last one to identify devices within that network. 

## The falicies of distributed computing

The network is reliable.
Latency is zero.
Bandwidth is infinite.
The network is secure.
Topology doesn't change.
There is one administrator.
Transport cost is zero.
The network is homogeneous.

## The standard network stack

|Nework Stack|
|----|----|
|Application| Sockets
|TCP/UDP| Transport layer
|IP| Internet protocol
|Link| MAC Address
|Hardware| Network Interface

## The osi network stack

|Nework Stack|
|----|----|
|Application| Sockets
|TCP/UDP| Transport layer
|Session|
|IP| Internet protocol
|Link| MAC Address
|Hardware| Network Interface

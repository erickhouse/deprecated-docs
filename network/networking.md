
Great Networking overview Resource

http://beej.us/guide/bgnet/html/multi/index.html

# Networking

|Term|Definition|
|----|---|
|NAT|Maps public ips to private ips, typically performed by your router
|private IP|The actual ip address associated with the machine hardware.
|public IP| The virtual ip address that is assigned by your isp
|ISP| internet service provider
|DHCP| Dynamic Host Configuration protocol
|OSI||
|LTE|Long Term Evolution
|Network Interface|The interface to the network on the actual hardware network card
|SCTP| The future of TCP where multiple connections can be stream concurrently|

::1 is short hand for localhost in IPv6 (just like 127.0.0.1 for IPv4)

the default port for http is port 80. Is is normal for each protocol to have a default port.

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

## The network stack

|Nework Stack|
|----|
|Application|
|TCP/UDP|
|IP|
|Hardware|

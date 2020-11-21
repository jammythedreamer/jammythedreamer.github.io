---
layout: post
title:  "Internet Technology"
subtitle:   "Internet Technology"
categories: junk 
tags: Internet
comments: false
---

## 개요
> `Internet Technology`에 대해 알아본다.

### Network

**network의 3대 요소**

- users
- links
- network nodes

network는 service를 제공하기 위해 사용된다.
하나의 network는 하나 이상의 service를 제공한다.

**Internet 키워드**

- electronic
- networks of networks
- standardized protocols

**domain name**

ex) www.snu.ac.kr

**IP address**

- 32 bit string (IPv4)

ex) 147.46.10.129

**취약점**

- cybersquatting
    - domain name
    - OSN account

유명한 기업, 단체, 기관, 조직 등의 이름과 같은 인터넷 주소를 투기나 판매목적으로 선점하는 행위

- typosquatting

aka URL hijacking

- DNS security

ISP : Internet service provider

RFC : request for comments

IETF : Internet Engineering Task Force

___

### Internet architecture

layers : each layer implements a service
- via internal functions in a layer
- rely on service provided by the lower layer

**Internet protocol stack**

- [`application`](http://jammythedreamer.github.io/knowledge/2020/10/27/knowledge-Internet_Technology/#application) : supporting network applications
    - FTP,SMTP,HTTP
- [`transprot`](http://jammythedreamer.github.io/knowledge/2020/10/27/knowledge-Internet_Technology/#transport) : process-process data transfer
    - TCP, UDP
- [`network`](http://jammythedreamer.github.io/knowledge/2020/10/27/knowledge-Internet_Technology/#network) : routing of datagrams from source to destination
    - IP, routing protocols
- [`link`](http://jammythedreamer.github.io/knowledge/2020/10/27/knowledge-Internet_Technology/#link) : data transfer between adjacent nodes
    - WiFi, Ethernet, PPP
- [`physical`](http://jammythedreamer.github.io/knowledge/2020/10/27/knowledge-Internet_Technology/#physical) : bits "on the wire"
    - eletromagnetic signals

**encapsulation**

### application

**client-server model**

- server
    - always-on host
    - permanent IP address
    - server farms for scaling
- client
    - communicate with server
    - may be intermittently connected
    - may have dynamic IP addresses
    - do not directly communicate with each other

**addressing processes**

port number

HTTP server : 80
Mail server : 25

applications rely on transport protocols

**TCP**
- congestion control - 혼잡 컨트롤
- flow control - receiver's memory를 파악하여
- connection setup 

reliable

**UDP**
- no-frills extension of best-effort IP

unreliable

why UDP?
- low delay


### transport

provide logical communication between app processes running on two end hosts

**end-to-end channel**
TCP
UDP

service not available
- delay guarantee
- bandwidth guarantee

**multiplexing and demultiplexing**
multiplexing - application -> transport
demultiplexing - transport -> applicaion

**connection-oriented demultiplexing**

TCP socket identified by 4-tuple
- source IP address, source port #, destination IP address, destination port #

each socket identified by its own 4-tuple

**TCP segment structure**

이후에 따로 포스트에서 다룰 예정

**RTT : round trip time**

**TCP connection establishment**

three-way handshake

**DOS attack**

### Network

**Internet structure**

a network of networks
- roughly hierarchical
- at center: "Tier-1" ISPs(e.g., Verizon, Sprint, AT&T) national/international coverage

POP : point-of-presence

- "Tier-2" ISPs: smaller (often regional) ISPs

why do "Tier 2" connect with multiple "Tier-1"?
- 하나의 link가 끊길 수 있는 상황 대비
- 공학적 설계가능

why "Tier-2" peering?
- low delay
- reduce cost

Internet eXchange (Point) - IX (IXP)
- reduced dependence on transit
- reduced cost
- increased capacity
- increased routing control
- improved performance

**Internet routing**

Routing Protocols

two level routing
- AS-AS BGP
- Router-Router RIP, OSPF

AS : AutonomousSystem
ASN : AS number

위로   provider
같은   peer
아래로  customer

customer cone

BGP (border gateway protocol)

**CDN**

content delivery network

Q. A CDN edge server comes in bewteen client and original server. Is there any sercurity issue?

**Network layer**

IP layer라고도 함

application : message
transprot : TCP - segment (UDP - datagram)
netwrok : `packet`
linke : packet
physical : frame

forwarding

- move packets from router's input to appropriate router output

routing

- determine route taken bt packets from source to dest

no call setup at network layer

queueing at input or output port -> RTT variation

ICMP : Internet Control Message Protocol

**IP datagram format**

**IP addressing**

IP prefix | hostidentifier
network ID| host ID

routing을 쉽게하기 위해

classfull: A B C D E

CIDR : classes inter-domain routing

DHCP : Dynamic Host Configuration Protocol

how to get assigned?
-> ICANN/RIR/NIR/LIR/APNIC, in Korea KISA : Korea Internet and Securty Agency

**private network**

10.0.0.0 - 10.255.255.255

172.16.0.0 - 172.31.255.255

192.168.0.0 - 192.168.255.255

NAT : Network Address Translation

network address and port translation (NAPT)

IPv6 : 128bit address

**IP vulnerablity**

**IP Spoofing Attacks**

parter의 src주소로 보냄.

ingress/egress filtering

**IP prefix hijacking**

### Link

Trailer - errir dectection

media access control (MAC)
- one node transmits a frame at a time
- to avoid collision
- avoid interference?

**DNS**

Domian Name Server (service)

DNS is a world-wide collection of mapping tables
-> Distributed Database

Domain : A node in the DNS tree
```
stub Resolver -> (local)DNS -> root-server
                        <-
                        -> gtld-server
                        <-
                        -> ripe-server
            <-          <-
```

Inherent DNS Vulerabilities

**ARP**

Address Resolution Protocol

MAC address

link layer address
48bit 

ARP Table

<IP address; MAC address; TTL>

6 Bytes

Organisational Unique Identifier(OUI) | Netwrok Interface Specific Identifier

IEEE

ARP Poisoning (ARP Spoofing)

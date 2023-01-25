# BGP Security

Welcome, stay tuned...

RFC 6952
RFC 7454
RFC 6192
TCP 179


## TCP/IP Protocol attacks
Spoofing and TCP reset, session hijacking or SYN flooding attacks.

## BGP route manipulation attacks
BGP origin hijacks, or BGP path hijacks.

## Protocol manipulation attacks
Modifying BGP attributes and exploiting RFD/MRAI timers.

## Denial of service attacks via resource exhaustion
Attackers can flood BGP speakers with too many BGP messages, affecting their ability to process legitimate BGP packets.


## TCP/IP Protocol Attacks - Long Live to TCP

### BGP Spoofing

### TCP Reset

### TCP Session Hijacking


### SYN Flooding Attack



## BGP Route Manipulation Attacks
https://www.rfc-editor.org/rfc/rfc7908.html


### BGP Origin Hijacks


### BGP Path Hijacks
 

### Hijacks of Unallocated IP Space

## Protocol Manipulation Attacks

### Manipulating BGP Attributes

### RFD/MRAI timers
- MED (multi-exit-discriminator)
- Route Flap Damping (RFD)
- Minimum Route Advertisement Interval (MRAI)



## Denial of Service (DoS) Attacks

- Congestion-induced BGP session failure
- Deliberate route flapping
- Hijacking the prefixes of another AS
- TCP attacks


## Unicast Reverse Path Forwarding (uRPF)

RFC 3704


## Resourses

- Kapela-Pilosov Attack

## Resume

- BGP speakers are vulnerable to DoS/DDoS attacks. To protect the BGP speaker, the operator can implement CoPP and ACL, rate-limiting, and uRPF.
- BGP sessions are subject to TCP/IP vulnerabilities. Therefore, it is recommended to use authentication (MD5 or TCP-AO) and GTSM (TTL Security).
- It is critical to restrain incorrect/malicious routing information and prevent it from propagating to the Internet. Most BGP incidents are the result of improper filtering. Each network must implement and maintain accurate filters to strictly control which routes they are accepting into their network and which routes they are announcing to their neighbours.

- Network operators can use information registered in the IRR system to create BGP filters automatically. In addition, most upstream providers implement IRR-based strict filtering for the prefixes they accept from their customers. These filters rely on the data in the IRR system to be accurate and complete.
- It is recommended to create authorised statements in the RPKI system and use RPKI data to validate the origin of BGP routes. RPKI can help prevent some route leaks, can help mitigate the damage of route hijacks and is an essential building block for deploying path validation in the future.
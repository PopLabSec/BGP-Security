# BGP Security

Welcome, stay tuned...

RFC 6952 RFC 7454 RFC 6192 TCP 179

### TCP/IP Protocol attacks <a href="#user-content-tcpip-protocol-attacks" id="user-content-tcpip-protocol-attacks"></a>

Spoofing and TCP reset, session hijacking or SYN flooding attacks.

### BGP route manipulation attacks <a href="#user-content-bgp-route-manipulation-attacks" id="user-content-bgp-route-manipulation-attacks"></a>

BGP origin hijacks, or BGP path hijacks.

### Protocol manipulation attacks <a href="#user-content-protocol-manipulation-attacks" id="user-content-protocol-manipulation-attacks"></a>

Modifying BGP attributes and exploiting RFD/MRAI timers.

### Denial of service attacks via resource exhaustion <a href="#user-content-denial-of-service-attacks-via-resource-exhaustion" id="user-content-denial-of-service-attacks-via-resource-exhaustion"></a>

Attackers can flood BGP speakers with too many BGP messages, affecting their ability to process legitimate BGP packets.

### TCP/IP Protocol Attacks - Long Live to TCP <a href="#user-content-tcpip-protocol-attacks---long-live-to-tcp" id="user-content-tcpip-protocol-attacks---long-live-to-tcp"></a>

#### BGP Spoofing <a href="#user-content-bgp-spoofing" id="user-content-bgp-spoofing"></a>

#### TCP Reset <a href="#user-content-tcp-reset" id="user-content-tcp-reset"></a>

#### TCP Session Hijacking <a href="#user-content-tcp-session-hijacking" id="user-content-tcp-session-hijacking"></a>

#### SYN Flooding Attack <a href="#user-content-syn-flooding-attack" id="user-content-syn-flooding-attack"></a>

### BGP Route Manipulation Attacks <a href="#user-content-bgp-route-manipulation-attacks-1" id="user-content-bgp-route-manipulation-attacks-1"></a>

[https://www.rfc-editor.org/rfc/rfc7908.html](https://www.rfc-editor.org/rfc/rfc7908.html)

#### BGP Origin Hijacks <a href="#user-content-bgp-origin-hijacks" id="user-content-bgp-origin-hijacks"></a>

#### BGP Path Hijacks <a href="#user-content-bgp-path-hijacks" id="user-content-bgp-path-hijacks"></a>

#### Hijacks of Unallocated IP Space <a href="#user-content-hijacks-of-unallocated-ip-space" id="user-content-hijacks-of-unallocated-ip-space"></a>

### Protocol Manipulation Attacks <a href="#user-content-protocol-manipulation-attacks-1" id="user-content-protocol-manipulation-attacks-1"></a>

#### Manipulating BGP Attributes <a href="#user-content-manipulating-bgp-attributes" id="user-content-manipulating-bgp-attributes"></a>

#### RFD/MRAI timers <a href="#user-content-rfdmrai-timers" id="user-content-rfdmrai-timers"></a>

* MED (multi-exit-discriminator)
* Route Flap Damping (RFD)
* Minimum Route Advertisement Interval (MRAI)

### Denial of Service (DoS) Attacks <a href="#user-content-denial-of-service-dos-attacks" id="user-content-denial-of-service-dos-attacks"></a>

* Congestion-induced BGP session failure
* Deliberate route flapping
* Hijacking the prefixes of another AS
* TCP attacks

### Unicast Reverse Path Forwarding (uRPF) <a href="#user-content-unicast-reverse-path-forwarding-urpf" id="user-content-unicast-reverse-path-forwarding-urpf"></a>

RFC 3704

### Resourses <a href="#user-content-resourses" id="user-content-resourses"></a>

* Kapela-Pilosov Attack

### Resume <a href="#user-content-resume" id="user-content-resume"></a>

* BGP speakers are vulnerable to DoS/DDoS attacks. To protect the BGP speaker, the operator can implement CoPP and ACL, rate-limiting, and uRPF.
* BGP sessions are subject to TCP/IP vulnerabilities. Therefore, it is recommended to use authentication (MD5 or TCP-AO) and GTSM (TTL Security).
* It is critical to restrain incorrect/malicious routing information and prevent it from propagating to the Internet. Most BGP incidents are the result of improper filtering. Each network must implement and maintain accurate filters to strictly control which routes they are accepting into their network and which routes they are announcing to their neighbours.
* Network operators can use information registered in the IRR system to create BGP filters automatically. In addition, most upstream providers implement IRR-based strict filtering for the prefixes they accept from their customers. These filters rely on the data in the IRR system to be accurate and complete.
* It is recommended to create authorised statements in the RPKI system and use RPKI data to validate the origin of BGP routes. RPKI can help prevent some route leaks, can help mitigate the damage of route hijacks and is an essential building block for deploying path validation in the future.

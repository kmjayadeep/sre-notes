# Networking

* DNS -> resolve ip addresses
  * has cache
  * ttl
* UDP -> unreliable protocol
  * sendto and recvfrom syscall
  * transport layer
* TCP -> Reliable protocol
  - stateful
  - congestion control, ordering, flow control
  - syn, syn ack, ack
  - tcpdump
* HTTP
  - on top of tcp
  - stateless
  - http/1.1 keeps tcp connection open
* https
  - provides server identification
  - encrypts data
  - certificate signed by a ca
  - csr includes public key
  - cert includes details about server
  - client validates the cert
  - client negotiates a symmetric key and algo
  - public certs are stored in /etc/ssl/cets/
* route
  - route command shows routing table
  - ip is anded with genmask and compared with destination on the routing table
  - 0000 if nothing matches
  - no gateway involved in local network. kernel finds mac and forwards directly
* linux socket
  - allows communication between different processes in the same or different machine
  - can use sys calls to interact with sockets
  - tcp and udp sockets

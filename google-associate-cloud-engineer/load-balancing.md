# Load Balancing

### Types

![](../.gitbook/assets/image%20%285%29.png)

### HTTP\(S\) Load Balancer - Global

* HTTP\(S\) load balancing:
  * Provides global load balancing for HTTP\(S\) requests to instances
  * Supports IPv4 and IPv6
  * Uses instance groups to organise instances
* Single IP address globally

### Content Based Load Balancing

HTTP/HTTPS Only

Add path rules to redirect traffic

### SSL Proxy

* Another kind of load balancing
* Intended for non HTTP\(S\) traffic using SSL
* Benefit is global load balancing of SSL traffic
* Terminates SSL connection at the load balancer

### TCP Proxy

* Same as SSL

### Network Load Balancing - Regional

* Network load balancing allows you to balance load of systems based on incoming IP protocol data.
* Uses forwarding rules that point to target pools
* UDP, TCP, SSL non-proxied

Forwarding Rules:

* Name
* Region
* IP Address - regional
* IP Protocol \(TCP, UDP, AH, ESP, ICMP, SCTP\)
* Ports
* Target-pool or target-instance

### sessionAffinity influences load distribution

Hash method selects backend based on a subset of:

* Source/Destination IP/port

### Internal Load Balancing

Internal load balancing allows you to:

* Load balance TCP/UDP traffic using a private frontend IP

### Regional Managed Instance Groups Best Practices

* Spreads and balances across 3 zones in a region
  * Zones at random
  * If zone becomes unhealthy, healthy zones take over
  * Rebalances when zone returns
* Over-provisioning
  * Provision at 100% for 2/3rd service during an outage
  * Provision at 150% for full service during an outage
































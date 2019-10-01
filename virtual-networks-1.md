# Virtual Networks

### Projects and Networks

* A project associates objects and services with billing.
* A project contains up to 5 networks.
* A project can have networks which are shared/peered.
* A network has no IP address range.
* A network is global and spans all available regions
* A networks can have 3 VPC network types: Default, Auto Mode and Custom Mode.

### Networks isolate systems

Projects in the same network can communicate over internal IPs even if they are in different regions.

lf an instance in the 'default' network and another instance is in the 'learnauto' network, even though both VMs are located in the same region, us-west1, and in the same zone, us-west1-a, they cannot communicate over internal IP.

Projects in the same region must communicate over external IPs.

### Subnetworks cross Zones

VMs can be on the same subnet but in different zones.

A single firewall rule can apply to both VMs.

### Expanding Subnets without Recreating Instances

Cannot overlap with other subnets.

Can expand but not shrink. Auto mode can expand from /20 to /16.

### IP Addresses

<table>
  <thead>
    <tr>
      <th style="text-align:left">Internal IP</th>
      <th style="text-align:left">External IP</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Allocated from subnet range to VMs by DHCP</td>
      <td style="text-align:left">Assinged from pool (ephemeral)</td>
    </tr>
    <tr>
      <td style="text-align:left">DHCP lease is renewed every 24 hours</td>
      <td style="text-align:left">
        <p>Reserved (static)</p>
        <p>Billed when not attached to a running VM</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">VM name and IP is registered with network scoped DNS</td>
      <td style="text-align:left">VM doesn&apos;t know external IP, it is mapped to the internal IP</td>
    </tr>
  </tbody>
</table>### External IPs are mapped to Internal IPs

### DNS Resolution for Internal Addresses

Hostname is same as instance name

Example: hostname.zone.projectid.internal

### DNS resolution for external addresses

100% SLA

Cloud DNS

### Alias IP ranges

### Routes and Rules

Every network has routes that let instances in a network send traffic directly to each other. They also have a default route that directs packets to destinations that out outside the network.

There are also firewall rules that can enable or block traffic.

### Firewall Rules

* Every VPC network functions as a distributed firewall.
* Firewalls rules apply to the network as a whole.
* Connections are allowed or denied at the instance level.

### Billing

Ingress, Egress internal IP address, Egress to Google, Egress to GCP = Free

Egress between zones in the same region, Egress external IP Address, Egress between regions in the US = $0.01.

### Cross-Project VPC Network Peering

Multiple networks are in multiple networks in an organisation.

Each project can have 5 networks.

### NAT Gateway Host Isolation

Networks can be in separate projects. Setup one VM as a NAT Gateway for another VM to send data out.

### Gigabit Network

Thoroughput is directly tied to number of vCPU units. Up to max of 8vCPUs.


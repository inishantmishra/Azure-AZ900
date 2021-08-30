# Azure Networking

### Virtual Network

- VM needs to be a part of Virtual network.
- Virtual network has private Ip Address which is in the range of Ip address range of virtual network.
- Vm can also have public IP address by whcih end user can connect to VM on internet.
- Subnet has a IP address range which is subset of Ip address ranges of Virtual Network.
- So In nutshell order is like this-

  - Virtual Network havign some IP Address ranges
    - A default Subnet created- Having some Ip Ranges which is subset of Virtual Network IP ranges
      - VM having Private IP address
      - Virtual Network Interface also gets created and will be inside Virtual Network

> We cant move a VM from one region to another or one Network to another.

> A VM cant be part of 2 networks. It can be part of only 1 network.

> VM and Network should be in one region then only we can select network while creatign VM in some network.

> VM and Virtual Nework can be part of different resource groups.

> Resource group can be of different location as compared to resources. There can be some resources which require same location but it can be possible.

- By default VMs can talk to each other via private Ips if they are part of same Virtual Neworks.

## Network Security Groups

- It provides rules/ act as firewall for traffic which goes in and comes out of Virtual Network.
- NSG can be applied to one Network interface card which will impact one VM only.
- NSG can also be applied to Subnet level which will impact all VMs under that subnet
- A network security group consists of Inbound rules that are used to control the traffic inbound into a virtual machine

- By default all traffic into a virtual machine is DENIED.

- You have to explicitly add rules to allow traffic into a virtual machine

- There are also outbound rules to control the traffic flowing out of the virtual machine. By default all traffic outbound onto the Internet is allowed.

## Application Security Groups

- Grouping of type of servers/tiers like web servers, database server and then applying NSG rule son them

### Virtual Network Peering

- To communciate between 2 Virtual Networks we need Virtual Netowrk peering.
- To connect some client workstations to Virtual Network over internet not via public Ip address but via priavte Ip Address by the Point to Site VPN Connection. Here client work stations will communciate with VPN Gateway.

- Another way of communciation is Site to Site VPN Connection. Here we want on premise data center to connect to Azure VM via private Ip address. Here we will have Routign device havign public IP address communicating with VPN gateway.
  ̦

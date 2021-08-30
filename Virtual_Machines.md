# Virtual Machines

- Other resources gets deployed along with VM
- Virtual Network: VM needs to be inside some Virtual Network
- OS Disk- holding the OS related data
- Virtual Network Interface Card- All packaets sent by VM and receive by it. It can have public and private IP
- NSG- It is assigned to Network Interface.Acts as a firewall

- Every resource needs to be part of Subscritpion and Resource group
- Resource group is logical grouping of resources.
- Most of resources get billed hourly basis in Azure.
- Costing for a virtual machine - Remember that costing for a virtual virtual machine depends on several factors, such as time as it runs for, the region used for hosting the virtual machine, the underlying operating system.
- Also keep a note that you will still be charged for other aspects of the virtual machine ( such as the disks attached to the virtual machine) , even if the virtual machine is stopped.

- 3 types to connect VM- RDP, SSh, Bastion
- Types of VMs-
- A-Series- For Dev/Test
- Bs- Series
- D Series
- DC Series
- E Series
- F Series
- G Series
- H Series

- Temporary storage is the storage created with OS disk but it is data loss disk.
  > De-Allocate process is the process where if we stop a VM from portal, it de-allocates the VM from physical server and when we start it may or may not star start from same physical server or some other server. So, Temp storage will get removed.
  > IP Address will also get changed always in De-Allocated state. But can opt for Static IP.

> But if we Shut Down from VM itself De-Allocation process wont be performed and state here will be Stopped.

> In Stopped state, there will be partial charge from Azure but in De-Allocated state, there wont be any charge but there will be charge for disk because disk is different resource.

> There are some Limitations of no of VMs that can be deployed under one account per region.

> A resource cant be part of multiple resource group

> A resource cant be part of multiple subscription

### Availibility Sets

- Update and Fault Domain gets assigned when VM is assigned to some Availibility Sets
- Default No of Fault Domains are 2 and Update Domains are 5.
- Max Fault Domains are 3 and Update Domains- 20
- We can not assign existing VM to be part of Availibility Set. Only while creating it can be assigned.
- Availibility set doesnt provide App syncing from one VM to another between availibility sets. It just provides infrastructure availibility.
- Availibility sets are under a data center on the level of physical server/racks.

### Availibility Zones

- Availibility zone is on the level of Data centers.
- SLA for 2 or more Availibility Zones is 99.99%
- There is no cost for creating Availibility Zones and Availibility Sets, but there is cost involved for the bandwidth involved in communication between VMs across different availibilty zones, hence it has some cost as compared to Availibility sets
- Zone 1, Zone 2 etc denotes different data centres.

### Azure Dedicated Host

- Whenever we create VM, it gets created on a physical server or host.
- If we want our own dedicated phycial host and no other customers can share our physical host, the concept of Azure Dedicated Host come in picture.
- Advantage is of controlling maintenance events on physical host. It means, we can control when mainetanance on physical host need to be done.
- Dedicated Host can only be created if 96vCPUs are available on subscriptions, hence it is requored by large enterprise organizations.

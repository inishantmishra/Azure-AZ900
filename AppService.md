# Azure Core Service

- PAAS needs to be linked with App Service Plan
- Azure WebApp will create web app also app service plan.
- Azure web app is an HTTP based service for hosting web apps.
- App service plan defines the set of compute resources that are used to run the apps.
  - Free, Shared App Service plans
  - Free app service plan can run only 60 min cpus/day
  - Basic, Standard, Premium
  - Isolated App service Plan

## VM Scale Sets

- This service allows you to create and manage a group of identical load balanced virtual machines.

- Here the number of Virtual Machine instances in the scale set can scale based on demand

- This is the best service if you want to add scalability to your application

- It will check some condition metric whether cpu>65% for example it will spin a new vm- Scale In.
- Similarly we can set Scale out so that if demand goes down and it will remove the extra VM.

## Azure Load Balancer

- Load Balancer is the service used to distribute the incoming traffic across a group of backend resources of servers.
- The Azure Load balancer is used to distribute incoming network traffic to a backend group of servers.
- Private or Public Load Balancer
- Here the Load Balancer would take the incoming requests from the users and direct the requests to virtual machines running in an Azure virtual network.

- If you have a web application running on the backend virtual machines, the requests would be distributed across the virtual machines by the Azure Load Balancer.

> Azure Traffic Manager - It is DNS Based routing service. It provides facility to route the traffic either on Azure Based resources or on-prem environemt based on DNS Names.

- The Traffic Manager service is used to direct client requests to the most appropriate service endpoint that is based on a traffic-routing method and the health of the endpoints.
- Azure Load balancer is network routing tool it works on IP addresses, based on TCP protocols.

- Aure load balancer can route traffic withing the particualr region not across different regions. but Azure Traffic Manager can.

- The different traffic routing methods available for the Azure Traffic Manager are

  Priority – Route traffic to another endpoint in case the primary fails.

  Weighted – Route traffic to different endpoints based on weight.

  Performance - you want end users to use the "closest" endpoint in terms of the lowest network latency.

  Geographic - geographic location their DNS query originates from.

  Multivalue – Here different endpoints are sent to the client. The client then selects the endpoint to send the request to.

  Subnet – This maps a set of end-user IP address ranges to a specific endpoint within a Traffic Manager profile.

- Pwershell, Bash, Azure CLI
- You can use PowerShell which can work on Windows, macOS and Linux
- You can use the Azure command line interface which can work on Windows, macOS and Linux
- You can use Azure cloud shell from the browser, which can then work on any operating system which has browser support
- Azure Storage account needs to be placed in order to launch Azure Cloud shell.

- Azure function has 2 pricing-
  - Consumption Plan
  - App Service Plan
  - Premium Plan

---
title: "Azure Service Bus."
layout: post
---
I am writing this argument to show how important is it to use Azure Service Bus and what are its benefits and how it can help our company in many different ways so here are some
benefits of using Azure Service Bus:






* Whether an application or service runs in the cloud or on-premises, it often needs to interact with other applications or services. To provide a broad communication channel between different applications, Azure provides a secure infrastructure called as Service Bus.
* Service Bus allows communication between on-premises solutions to Microsoft Azure solutions, and even Microsoft Azure solutions to other solutions within the cloud.
* It provides connectivity options for Windows Communication Foundation (WCF), which includes REST endpoints.
* Service Bus is a multi-tenant cloud service, which means that the service is shared by multiple users.Each user, such as an application developer, creates a namespace, then defines the communication mechanisms she needs within that namespace.
* Within a namespace, you can use one or more instances of three different communication mechanisms, each of which connects applications in a different way.

Starting first with a short explanation of what Azure Private Link and in general it allows you to securely link Azure Paas services to your virtual network (VNet) using private endpoints. Apart of that, with Private Link you can:

* Connect privately to Azure Monitor without opening any public network access.
* Ensure your monitoring data is only accessed through authorized VNets Prevent data exfiltration from your VNets by defining specific Azure Monitor resources that are in your scope.
* Keep all traffic inside the Microsoft Azure backbone network.
* Securely connect your private on-premises network to Azure Monitor using ExpressRoute and Private Link How it works.

On the other hand with the help of Azure Service Bus we can use private link so customers can now set up network access controls like NSG to restrict access to the private endpoint. Individual Azure PaaS resources are then mapped to specific private endpoints. Since a malicious insider can only access the mapped PaaS resource they cannot use some other resource for data exfiltration. In addition, since the Azure Service Bus namespace is mapped to private IP address in the customer’s VNet, they can be accessed via Azure ExpressRoute private peering. Additionally, Microsoft peering is also supported for VNets that are not on the customer’s private network.  
This effectively means that the data will traverse a fully private path from on-premises to Azure. The configuration in the corporate firewalls and route tables can be simplified to allow access only to private IP addresses. With Private link, customers can enable cross-premises access to private endpoint using Express Route(ER), private peering, Microsoft peering or VPN tunnel. They can subsequently disable all access via public endpoint and not use the IP-based firewall. Finally, Azure Private Link for Azure Service Bus is simple to setup with minimal networking configuration. Connectivity works on approval call flow and once a Service Bus namespace is mapped to a private endpoint, the connectivity works out of the box without any additional configurations on route tables and Azure Network Security Groups.   



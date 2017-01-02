# Barracuda Web Application Firewall

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fbarracuda-waf%2Fazuredeploy.json" target="_blank">
<img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fbarracuda-waf%2Fazuredeploy.json" target="_blank">
<img src="http://armviz.io/visualizebutton.png"/>
</a>


This template deploys a **Barracuda Web Application Firewall**. The **Barracuda Web Application Firewall** is an ideal solution for organizations looking to protect web apps from data breaches and defacement. With the Barracuda Web Application Firewall, administrators do not need to wait for clean code or even know how an application works to secure their applications. Organizations can ensure robust security with a Barracuda Web Application Firewall hardware or virtual appliance, deployed in Microsoft Azure.

`Tags: Barracuda, firewall, web application`

## Solution overview and deployed resources


The following resources are deployed as part of the solution

#### Microsoft.Network


+ **publicIPAddresses**: 1 public IP for Load Balancer and 1 for each Barracuda BWAF VMs.
+ **virtualNetworks**: 1 virtual Network that contains all the Web VMs and BWAF VMs.
+ **loadBalancers**: 1 Load Balancer that allow RDP access to all Web VMs.
+ **loadBalancers/inboundNatRules**: 1 Inbound NAT rule for each Web VMs created.
+ **networkInterfaces**: 1 NIC for each BWAF VM and Web VMs created. 

#### Microsoft.Storage


+ **storageAccounts**: 1 Storage Account to store all VM disks.

#### Microsoft.Compute


+ **availabilitySets**: 2 Availability Sets each for Web VMs and BWAF VMs.
+ **virtualMachines**: Specified number of BWAF VMs and Web VMs. 
+ **virtualMachines/extensions**: 1 for each Web VMs created. This extension sets up IIS on each Web VM. 

## Prerequisites



## Deployment steps

You can click the "deploy to Azure" button at the beginning of this document. 

#### Connect

Follow the instruction on the Barracuda WAF Guide on the root folder. 

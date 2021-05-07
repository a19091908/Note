Azure

<h3>Weight</h3>
<table class="table"><caption >資料表 1</caption>
<thead>
<tr>
<th>AZ-900 領域區域</th>
<th>Weight</th>
</tr>
</thead>
<tbody>
<tr>
<td>描述雲端概念</td>
<td>20-25%</td>
</tr>
<tr>
<td>描述核心 Azure 服務</td>
<td>15-20%</td>
</tr>
<tr>
<td>描述 Azure 上的核心解決方案及管理工具</td>
<td>10-15%</td>
</tr>
<tr>
<td>描述一般安全性及網路安全性功能</td>
<td>10-15%</td>
</tr>
<tr>
<td>描述身分識別、治理、隱私權及合規性功能</td>
<td>20-25%</td>
</tr>
<tr>
<td>描述 Azure 成本管理與服務等級協定</td>
<td>10-15%</td>
</tr>
</tbody>
</table>

<hr>

<h3>What is Cloud Computing</h3>

* Why is cloud computing typically cheaper to use
    - pay-as-you-go pricing model
        + you pay only for the cloud services you use
* Benefit:
    - Lower your operating costs.
    - Run your infrastructure more efficiently.
    - Scale as your business needs change.
* What can it provide
    - A nearly limitless pool of raw compute, storage, and networking components.
    - Speech recognition and other cognitive services that help make your application stand out from the crowd.
    -  Analytics services that deliver telemetry data from your software and devices.
* What are some cloud computing advantages?
    - Reliability(availability)
        + Depending on the service-level agreement that you choose, your cloud-based applications can provide a continuous user experience with no apparent downtime even when things go wrong.
    - Scalability
        + Vertically: Computing capacity can be increased by adding RAM or CPUs to a virtual machine.
        + Horizontally: Computing capacity can be increased by adding instances of a resource, such as adding more virtual machines to your configuration.
    - Elasticity
        + Cloud-based applications can be configured to always have the resources they need.
    - Agility
        + Cloud-based resources can be deployed and configured quickly as your application requirements change.
    - Geo-distribution
        + Applications and data can be deployed to regional datacenters around the globe, so your customers always have the best performance in their region.
    - Disaster recovery
        + By taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your applications with the confidence that comes from knowing that your data is safe in the event that disaster should occur.

* Models
    - IaaS
        +   This cloud service model is the closest to managing physical servers. A cloud provider keeps the hardware up to date, but operating system maintenance and network configuration is left to the cloud tenant. For example, Azure virtual machines are fully operational virtual compute devices running in Microsoft's datacenters. An advantage of this cloud service model is rapid deployment of new compute devices. Setting up a new virtual machine is considerably faster than procuring, installing, and configuring a physical server.
    - PaaS
        + This cloud service model is a managed hosting environment. The cloud provider manages the virtual machines and networking resources, and the cloud tenant deploys their applications into the managed hosting environment. For example, Azure App Services provides a managed hosting environment where developers can upload their web applications without having to deal with the physical hardware and software requirements.
    - SaaS
        +   In this cloud service model, the cloud provider manages all aspects of the application environment, such as virtual machines, networking resources, data storage, and applications. The cloud tenant only needs to provide their data to the application managed by the cloud provider. For example, Office 365 provides a fully working version of Office that runs in the cloud. All that you need to do is create your content, and Office 365 takes care of everything else.

<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/intro-to-azure-fundamentals/media/shared-responsibility.png">

* What is serverless computing?
    - Devlopers do not need to care infrastructures.
    - Devlopers focus on innovation.

* The types of Cloud
    - Public cloud
        + Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources like servers and storage are owned and operated by a third-party cloud service provider and delivered over the internet.
    - Private cloud
        + Computing resources are used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site datacenter. It also can be hosted by a third-party service provider.
    - Hybird cloud
        + This computing environment combines a public cloud and a private cloud by allowing data and applications to be shared between them.
        
    <img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/intro-to-azure-fundamentals/media/cloud-computing-continuum.png">

* Azure Service
    - Compute: VM, Batch, ...
    - Networking: VPN, load blancer, DNS, FireWall, Traffic Manager
    - Storage: Blob, File, Table, ...
    - Mobile
    - Databases: Cosmos DB, MySQL, PostgreSQL, ...
    - Web: APP Service, API Management, ...
    - IOT
    - Big data: Machine Learning Service
    - DevOps

<h3>Capital expenses vs. operating expenses</h3>
* CapEx requires significant up-front financial costs, as well as ongoing maintenance and support expenditures. 
* By contrast, OpEx is a consumption-based model, so Tailwind Traders is only responsible for the cost of the computing resources that it uses.

<h3>Four levels of the management structure</h3>
* Resources
    - Resources are instances of services that you create, like virtual machines, storage, or SQL databases.
* Resource groups
    - Resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
* Subscriptions
    - A subscription groups together user accounts and the resources that have been created by those user accounts. For each subscription, there are limits or quotas on the amount of resources that you can create and use. Organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects.
* Management groups
    - These groups help you manage access, policy, and compliance for multiple subscriptions. All subscriptions in a management group automatically inherit the conditions applied to the management group.
<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/hierarchy.png">

<h3>Azure subscriptions</h3>
* A subscription provides you with authenticated and authorized access to Azure products and services.
* An account can have one subscription or multiple subscriptions that have different billing models and to which you apply different access-management policies.
* Two types of subscription boundaries
    - Billing boundary
        + Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs.
    - Access control boundary
        + you can create separate subscriptions to reflect different organizational structures. 
        + An example is that within a business, you have different departments to which you apply distinct Azure subscription policies.
        
<h3>Customize billing to meet your needs</h3>
* If you have multiple subscriptions, you can organize them into invoice sections. Each invoice section is a line item on the invoice that shows the charges incurred that month. 
* For example, you might need a single invoice for your organization but want to organize charges by department, team, or project.

<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/billing-structure-overview.png">

<h3>Hierarchy of management groups and subscriptions</h3>
* You can build a flexible structure of management groups and subscriptions to organize your resources into a hierarchy for unified policy and access management. The following diagram shows an example of creating a hierarchy for governance by using management groups.

<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/management-groups-and-subscriptions.png">

<h3>Azure Resource Manager</h3>
* Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features like access control, locks, and tags to secure and organize your resources after deployment.

<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/consistent-management-layer.png">

<h3>Azure regions</h3>
* When you deploy a resource in Azure, you'll often need to choose the region where you want your resource deployed.

<h3>Azure availability zones</h3>
* Availability zones are physically separate datacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking. An availability zone is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.

<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/availability-zones.png">

<h3>Azure region pairs</h3>
* Each Azure region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away. This approach allows for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as disasters

<img src="https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/region-pairs.png">



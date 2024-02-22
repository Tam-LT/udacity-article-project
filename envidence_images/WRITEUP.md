# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

Table compare app service and virtual machine in azure
| Feature | App Service | Virtual Machine (VM) |
|---|---|---|
| Cost | Generally more cost-effective for most web applications because it is a PaaS (Platform as a Service) offering, meaning you pay for the service plan (include  CPU, memory, and storage) and not for the underlying infrastructure. | Costs can be higher since it is an IaaS (Infrastructure as a Service) solution. You pay for the virtual machines, including the compute, storage, and networking resources they consume, regardless of the application's needs. |
| Scalability | Provides simple scalability choices, with the option to grow vertically by upgrading to a higher App Service Plan or horizontally by adding more instances. | Scalability demands more complicated and manual management of load balancers, virtual machine instances, and other things. |
| Availability | The platform comes with built-in features including auto-scaling, automatic OS updates, and patching | Availability is highly dependent on how you configure and manage your VMs such as setting zones, using Azure's global infrastructure |
| Workflow | Supports continuous integration and deployment (CI/CD) from Azure DevOps, GitHub, Bitbucket, and other sources | Full control over the VM, allowing to install any necessary software or services, suitable to complex applications or those with specific requirements not supported by App Service |

After analyzing the costs, scalability, availability, and workflow, I have decided to deploy my application on Azure App Service. The platform's cost-effectiveness is the main factor influencing this choice because it offers a managed service environment where I can pay for what I need without having to worry about the costs of maintaining the underlying infrastructure. The scalability features of Azure App Service are very compelling; they provide automatic horizontal and vertical scaling, guaranteeing that the application can effectively manage fluctuating loads without the need for user intervention. The platform's built-in high availability guarantees that my application remains accessible to users, with minimal downtime thanks to automatic updates and patching.  Additionally, the streamlined workflow offered by Azure App Service, including support for CI/CD from sources such as Github,... made the deployment and maintenance simpler.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

I will choose to use VM if my application needs VM to ensure some of the requirements below:
1. My application has specific infrastructure requirements that cannot be met by Azure App Service's PaaS model, such as running custom software or needing more control over the underlying operating system and server configuration, deploying to Azure VMs might be more suitable.
2. My application relies on legacy software or dependencies that are not compatible with the Azure App Service environment, deploying to Azure VMs might be necessary to maintain compatibility.
3. My application requires advanced networking configurations, such as setting up virtual networks, VPN connections, or network security groups.

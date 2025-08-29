# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

VM vs App Service Analysis

1. Cost Analysis

VM:
Requires paying for the entire virtual machine, even when idle.
Additional costs for OS licensing, patching, and maintenance.
Scaling up means provisioning larger VMs or multiple VMs, which increases costs significantly.

App Service:
Pay-as-you-go model based on the selected plan (Free, Shared, Basic, Standard, Premium).
No OS licensing or infrastructure maintenance costs.
Ideal for lightweight apps because you only pay for the resources you use.


2. Scalability

VM:
Manual scaling; you need to configure load balancers and manage multiple VMs.
Vertical scaling (upgrading VM size) can cause downtime.

App Service:
Built-in auto-scaling based on metrics like CPU, memory, or schedule.
Horizontal scaling is seamless and requires minimal configuration.


3. Availability

VM:
Requires setting up availability sets or zones for high availability.
You are responsible for OS updates and failover configurations.

App Service:
High availability is built-in with Azure’s SLA (99.95% for Standard tier and above).
No need to manage OS or infrastructure for uptime.


4. Workflow

VM:
Full control over the environment, but requires manual setup of web server, runtime, and security patches.
Deployment is more complex and time-consuming.

App Service:
Simplified deployment with CI/CD integration (GitHub, Azure DevOps).
Supports multiple languages and frameworks out of the box.
No need to manage OS or runtime manually.


- Chosen Solution: Azure App Service
I chose Azure App Service because the application is lightweight and does not require full control over the underlying infrastructure. App Service offers lower cost, built-in scalability, and high availability without the overhead of managing a VM. Additionally, the deployment workflow is much simpler, which speeds up development and reduces operational complexity.

### Assess app changes that would change your decision.

If the application required more control over the operating system, custom software installations, or advanced networking configurations, I would consider using a VM instead of App Service. Similarly, if the app became resource-intensive or needed to run background services that App Service does not support, a VM would be the better choice. Essentially, any shift toward higher complexity, heavy processing, or specialized infrastructure needs would change my decision.
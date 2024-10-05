# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Cost.

-Azure VMs: Azure VMs can be more expensive as they have continuous operation even when idle. There are also potentially costs of the OS, storage and network traffic. In addition, there is potentially also higher maintenance costs.

App Services: Costs are based on resources used; in addition the app plan can be configured to scale automatically which theoretically keeps costs lower.

### Scalability.

-Azure VMs: Azure VMs require manual intervention or automation scripts, for large scale applications this could be complex or time consuming.

App Services: App services have built in auto scaling which theoretically is one less thing to have to manage, it is also more suitable when application usage/load is unpredictable.

### Availability.

-Azure VMs: required availability can be achieved with the implementation of multiple VMs spread across regions and the introduction of load balancers. However this is a complex environment with significant management requirements.

App Services: App services have built in high availability with disaster recovery options. In addition they automatically distribute traffic across instances and regions which aims to keep downtime to a minimum.

### Workflow.

-Azure VMs: Azure VMs offer full control over the environment, which can be beneficial depending on the application. However, this does mean more responsibility and complexity and requires more maintenance, updating and security.

App Services: App services simplify workflow with CI/CD pipelines, easier configuration and management. The underlying infrastructure is largely abstracted allowing organisational focus on the application itself.

### Justification for Web App.
I chose to implement a web app as it is a relatively simple CMS app with minimal business workflow, therefore does not require a complex environment. The implementation/technical workflow is also relatively simple which is a nice fit into the web app category. ultimately the web app is more cost effective given the relatively simple usage resulting in minimal resource consumption. The tool could easily be scaled to service an increase of users particularly across region. The app will likely have a higher availability as it is azure hosted rather than nested in a VM which requires additional maintenance. 

All in all I felt that the app is simpler to manage being a web app over being hosted on a VM given its relatively simple nature, also I factored in the cheaper cost as a huge win for 'team web app'.



### Assess app changes that would change your decision.

- If the app required highly specific performance optimisation I would consider redeploying on a VM where I would have more flexibility with the environment, however the computational needs of the app would have to be extremely high.
- Compliance requirements - if the app required specific compliance requirements that were not able to be met with the web app implementation. These would really have to be in the infrastructure requirements or extremely specific data handling requirements.
- Complexity added to the deployment/running environment - i.e. hybrid cloud setups or integrations with on-prem systems that could not be achieved via another method of integration.

### App changes that I would like to see made

- Ability to restrict users (as opposed to anyone with a Microsoft account) i.e increased security - I chose not to do the extra credit item for this.
- Ability to delete records - I chose not to do the extra credit item for this.
- Implement a backup process and have a DR plan in place.
- Ability to store multiple images with follow up image handling (delete 1, multiple or all images).
- Ability to preview images without opening a record (i.e. hover over from listings screen).

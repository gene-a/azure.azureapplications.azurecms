# App URL:
https://azurecmsapp.azurewebsites.net

# Azure Compute Service: 
App Service. While the more flexible approach in deploying the CMS app is a VM compute service, I've chosen to use an App Service for this use case.

# Choice Justification:
In no particular order of priority, I will now justify my choices:

Firstly, in a workflow perspective I want to be able to quickly setup, debug, and deploy the app without going through the hassles of setting up everything from the OS up.
As a lone developer of the app, the capability to seamlessly push the app through Azure CLI makes my workflow easier when I want to debug code changes in a remote environment.
Though not forgetting that I can integrate Github actions as part of a VM compute service deployment, when the time comes I eventually move to a VM deployment I can use this feature if need be.

Secondly, even though getting the app up and running is a priority, the horizontal and vertical scaling of an App Service will prove to be more than enough to accomodate the initial volume of traffic of a CMS website where not much interactivity is involved.
Having 4 vCPUs and 14gb of ram, in my opinion, will be more than sufficient to accomodate processing of the initial deployment of the app which is: user authentication, blog posting, and content display.
As more features are added to the app and as more control over the environment is needed (e.g. installing 3rd party software, etc), or as the user base increases (ultimately overworking the App Service limits), I can move on to a VM to better serve my app.

Lastly, in an availability perspective, according to azure's SLA for VM and App Services I can expext a 99% uptime for the app which seems like making a choice between any of the two viable.
However, given that with the VM there might possibly more points of failure in terms of server configuration or what not, leaving the OS management to Microsoft's hands is best for now in my opinion.
My reason for this is that since I want to be able to have the CMS app in the hands of the users as quickly as possible, eliminating possible points of errors early on while being able to cater to usage needs is essential.

# Changes Justification:
To reiterate what I've described my choice justification, I would consider moving forward to a VM as more features are added to the app that require more control of the OS is needed OR most importantly, when the performance limitations of an App Service has been surpassed/met.
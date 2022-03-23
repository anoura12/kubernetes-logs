Kubernetes clusters - lots of computers connected to work as a single unit
Nodes

Need for Kubernetes? --> Automating process scheduling, deployment in case of a hardware failure

When deploying a multi-component application through Kubernetes, it selects
a server for each component, deploys it, and enables it to easily find and communicate with all the other components of your application. 

Disadvantages of previous deployment methods:
- Everything deployed as 1 huge OS process
- All resources on that OS shared among all apps
- Changes to one part of app = redeployment of whole app
- Increasing interdependencies between components = increasing complexity

2 previous solutions to this were
1. Vertical scaling --> Adding more CPUs, more memory to that one server (Too expensive)
2. Horizontal scaling --> Additional servers running the same app (What is really the issues with this one)


Monolithic app ---> Microservices(deployment components) --> Independent process

Deployment 
Control Plane starts the app containers
CP Schedules nodes to run apps
Node communicates with the control plane through the Kubernetes API

Initially installation scripts were used to deploy stuff but if they failed they would have to be manually set back up again... Kubernetes does this automatically.

==========================================================================

Kubectl --> k8s CLI --> basically communicates with the Control Plane through the API

format of a kubectl command --> kubectl {action} {resource} {name of resource} {flag}

kubectl proxy --> provides a secure connection to the API server in the cluster so that communication between the client and server is established
===========================================================================

pods

what happens when we create a deployment
=> A pod with containers is created and remains alive under termination

What happens once a node fails?
Identical pods are created to restart the containers within them.
Pods are only scheduled once 
If terminated, new pods take over





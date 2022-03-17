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




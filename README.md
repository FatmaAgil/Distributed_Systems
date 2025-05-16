# Widgetario Hackathon
## Project Overview
This repository contains scripts written for the Kubernetes Course Labs Hackathon.
The hackathon involves modelling and deploying a Kubernetes app called Widgetario, as a way of applying skills gained from learning the basics of Kubernetes.
- More information on the hackathon: https://kubernetes.courselabs.co/hackathon/

## Installation and Setup
### Pre-requisites
- [Kubernetes and a Git Client](https://kubernetes.courselabs.co/setup/)
- Any code editor of your choice for viewing and editing the files.

### Setup Instructions
- Clone the repository:
```bash
git clone https://github.com/FatmaAgil/Distributed_Systems.git
```

- Navigate to the repository after cloning:
```bash
cd Distributed_Systems
```

- Deploy the application:
```bash
kubectl apply -f widgetario-hackathon/PART-6/monitoring -f widgetario-hackathon/PART-6/logging -f widgetario-hackathon/PART-6/ingress-controller -f widgetario-hackathon/PART-6/widgetario
```

- Check the status of the deployments:
```bash
kubectl get deployments -n default
kubectl get deployments -n logging
kubectl get deployments -n monitoring
```
You could also verify the status of the pods and services.

## Usage
### Accessing the Web Application and API
- You can access the web application at: http://widgetario.local
- The API can be accessed at: http://api.widgetario.local/products

**Note:** If you are using WSL2 to deploy the application, ensure that you either set up **port forwarding** on your Windows host or use the port number of the **NodePort** to access the URLs on your windows Web browser.

### Accessing Grafana and Kibana
- Access Grafana on: http://localhost:30003
- Access Kibana on: http://localhost:30005

## Acknowledgements
We would like to thank the creators and maintainers of [Kubernetes Course Labs](https://kubernetes.courselabs.co/) for providing free resources for learning Kubernetes.



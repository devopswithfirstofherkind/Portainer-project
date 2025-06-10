# **KIND (Kubernetes in Docker) and Portainer-project**
---
This is a step-by-step guide showing how to configure a KIND (Kubernetes in Docker) cluster that manages Kubernetes Nodes running in a Docker container and also setting up Portianer, a UI that visually shows kunernetes clusters you have running on your local machine.
## **What is Kind?**
Kubernetes in Docker, for short known as KIND is a tool for running Kubernetes clusters as docker containers. It is light weight and ideal for running Kubernetes clusters on your local machine especially for test and development purposes. Typically, KIND operates on a single node type of cluster, where we have just a single node running on the cluster but this can be chnaged.
Now, let's go on to its installation.
___
*__PS: This installation is based on the Windows Operating system using WSL.__*

## **PREREQUISITES**
*__I have included links where you can have them installed.__*
- [Windows 10/11 running WSL (Ubuntu)](https://learn.microsoft.com/en-us/windows/wsl/install)
- [Docker](https://docs.docker.com/desktop/features/wsl/)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)
- [Homebrew](https://docs.brew.sh/Homebrew-on-Linux)

But first things first, I always like to update the systems to avaoid future errors during installation.... Let's run this code below:

```bash
Sudo apt update && sudo apt upgrade
````

Once we have the system updated, let's get into business.
When installing KIND via CLI, I used Homebrew. This is a Mac pacakge inataller that works on Linux, I choose this option bacause it was straightforward compared to other options I saw that can be used to install KIND.

```bash
Brew install Kind
```
Once KIND has been installed, you can check the KIND version, just to be sure that the installation has fully completed.
```bash
kind version
```
After this is confirmed, we can go ahead to create the KIND cluster. To do that we run:
```Bash
kind create cluster --name <clustername>
```
Once the cluster has been created, we can use Kubectl commands to check Nodes, check pods, describe pods.
```bash
kubectl get nodes
kubectl get pods
kubectl describe pod <pod name>
```





# Kubernetes Notes

At its core, it's a system that deploys and manages containerized apps. You use Kubernetes as the orchestration and cluster software to deploy your apps and respond to changes in compute resource needs.



Cluster: A bunch of computers/servers that are working together in a single system

Planes: Computers that run the scheduling software, these are the managers of the other computers

Nodes: Computers that do the actual tasks and are managed by Planes



![image-20240716120614506](D:\Pictures\Typora Images\image-20240716120614506.png)

![image-20240716120638270](D:\Pictures\Typora Images\image-20240716120638270.png)

---

Azure Kubernetes Service (AKS) is a managed Kubernetes service provided by Microsoft Azure. It allows you to deploy, manage, and scale containerized applications using Kubernetes without having to worry about the underlying infrastructure and operational complexities. Here’s a detailed breakdown:

### What is Azure Kubernetes Service (AKS)?

AKS is a fully managed Kubernetes service that simplifies the process of running Kubernetes clusters on Azure. It abstracts the complexity of Kubernetes management and provides a streamlined experience for deploying and managing containerized applications.

### How AKS Works

1. **Cluster Creation**:
   - **Provisioning**: AKS handles the provisioning of Kubernetes nodes, setting up the control plane, and configuring the network and storage.
   - **Scaling**: AKS supports both manual and automatic scaling of your node pools.
2. **Management**:
   - **Upgrades and Patching**: AKS manages the Kubernetes upgrades and patches to ensure your clusters are up-to-date with minimal downtime.
   - **Monitoring**: AKS integrates with Azure Monitor and other tools for monitoring the health and performance of your clusters.
   - **Security**: It provides built-in security features such as Azure Active Directory (AD) integration, network policies, and secrets management.
3. **Deployment**:
   - **CI/CD Integration**: AKS integrates with Azure DevOps, GitHub Actions, and other CI/CD tools for continuous deployment of applications.
   - **Helm Charts**: Use Helm charts to manage and deploy your Kubernetes applications easily.

### Differences Between AKS and Normal Kubernetes

1. **Management**:
   - **AKS**: The control plane (including the Kubernetes master nodes) is managed by Azure. You don’t have to worry about maintaining the master nodes or the etcd database.
   - **Normal Kubernetes**: You need to manage the entire Kubernetes cluster, including the control plane and worker nodes.
2. **Scaling**:
   - **AKS**: Supports automatic scaling of node pools and integrates with Azure's auto-scaling features.
   - **Normal Kubernetes**: Requires manual setup and management of auto-scaling.
3. **Upgrades**:
   - **AKS**: Simplifies the upgrade process with managed updates.
   - **Normal Kubernetes**: Requires manual intervention to upgrade Kubernetes versions and apply patches.
4. **Security**:
   - **AKS**: Integrates with Azure AD for role-based access control (RBAC) and provides additional security features out-of-the-box.
   - **Normal Kubernetes**: Requires manual configuration for RBAC and other security features.
5. **Networking**:
   - **AKS**: Offers built-in integration with Azure networking services like Azure Virtual Network, Azure Load Balancer, and Azure Application Gateway.
   - **Normal Kubernetes**: Requires manual configuration and integration with external networking solutions.

### Pods

They are the "smallest units" of Kubernetes. They contain one or more containers.



### Services

They are the way that you expose one or more pods to each other to give them connectivity (through their other services). In front of one or more pods is a service that deals with giving it networking and letting it talk to other pods via their services.

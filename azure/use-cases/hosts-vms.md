---
description: Using Hosts in DuploCloud
---

# Hosts (Virtual Machines)

Once we have the Infrastructure (Networking, Kubernetes cluster, and other common configurations) and an environment (Tenant) set up, the next step is to create VMs. These could be meant for:

* AKS Worker Nodes
* Worker Nodes (Docker Hosts) if built-in container orchestration is used.
* Regular nodes that are not part of any container orchestration, where a user manually connects and installs applications. For example, when using a Microsoft SQL Server in a VM, when running an IIS application and in other custom use cases.

## Creating Hosts <a href="#3-toc-title" id="3-toc-title"></a>

See the Services documentation for steps to [create Hosts and configure Kubernetes storage options](../azure-services/containers/).&#x20;

<figure><img src="../../.gitbook/assets/Azure_Hosts (1) (1).png" alt=""><figcaption><p><strong>Host</strong> tab on <strong>Azure VM</strong> page</p></figcaption></figure>

## Host abstraction and isolation&#x20;

While lower-level details such as IAM roles and security groups are abstracted, deriving instead from the tenant, only the most application-centric inputs are required to set up Hosts.&#x20;

<figure><img src="../../.gitbook/assets/Azure_host_VM.png" alt=""><figcaption><p><strong>Add Virtual Machine</strong> page </p></figcaption></figure>

Most of these inputs are optional and some are available as list box selections, set by the administrator in the Plan (for example, **Image ID**, in Host **Advanced Options**).&#x20;

There are two additional parameters

**Fleet**: This is applicable if the VM is to be used as a host for [container orchestration](../container-deployments/container-orchestrators.md) by the platform. The choices are:

* **Linux Docker/Native**: To be used for hosting Linux containers using the [Built-in Container orchestration](../container-deployments/).      &#x20;
* **Docker Windows**: To be used for hosting Windows containers using the [Built-in Container orchestration](../container-deployments/).
* **None**: To be used for non-Container Orchestration purposes and contents inside the VM are self-managed by the user.

**Allocation Tags (Optional)**: If the VM is used for containers, you can optionally set a label on the VM. This label is specified during Docker application deployment to ensure that the application containers are pinned to a specific set of nodes, giving you the ability to split a tenant further into separate pools of servers and deploy applications on them.&#x20;

{% hint style="info" %}
If a VM is used for container orchestration, ensure that the **Image ID** corresponds to the Image in the container. Any name that begins with **Duplo** is **** an image that DuploCloud generates for Built-in container orchestration &#x20;
{% endhint %}
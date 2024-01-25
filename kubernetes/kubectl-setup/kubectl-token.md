---
description: Set up KubeCtl within the DuploCloud Portal by downloading the token
---

# KubeCtl Token

## Downloading the KubeCtl token

DuploCloud provides a way to connect directly to the Cluster namespace using the `kubectl` token.&#x20;

{% hint style="warning" %}
If you attempt to start a **KubeCtl Shell** instance and receive a **503** in your web browser, ensure that the **duplo-shell** service in the **Default** Tenant is running and that the Hosts which support it are running, as well.
{% endhint %}

1. In the DuploCloud Portal, navigate to **DevOps** -> **Containers** -> _**CONTAINER\_TYPE**_, where _**CONTAINER\_TYPE**_ is **EKS/Native**, **AKS/Native** or **GKE/Native**.
2.  Click **KubeCtl Token.** The **Token** window displays. **Copy** the contents to your clipboard.\


    <div align="left">

    <figure><img src="../../.gitbook/assets/k8s1 (1).png" alt=""><figcaption><p><strong>Services</strong> page with <strong>KubeCtl Token</strong> button<br></p></figcaption></figure>

    </div>

    <div align="left">

    <img src="../../.gitbook/assets/image (1) (3).png" alt="Token window with kubectl commands for creating token">

    </div>
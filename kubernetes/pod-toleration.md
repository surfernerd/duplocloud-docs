---
description: Support for specifying K8s YAML for Pod Toleration
---

# Kubernetes Pod Toleration

DuploCloud supports the customization of many Kubernetes (K8s) YAML operators, such as [`tolerations`](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/). If you are using a Docker container, you can specify the `tolerations` operator configuration in the **Other Container Config** field in the container definition in DuploCloud

## Specifying Pod Toleration

1. In the DuploCloud Portal, navigate to **DevOps** -> **Containers** -> _**CONTAINER\_TYPE**_, where _**CONTAINER\_TYPE**_ is **EKS/Native**, **AKS/Native** or **GKE/Native**.
2. Click the **Containers** tab. The **Containers** page displays.
3. Select the container from the **Name** column.
4.  From the **Actions** menu, select **Edit**. The **Edit Service** page displays.\


    <figure><img src="../.gitbook/assets/tol1 (1).png" alt=""><figcaption><p><strong>Edit</strong> option in <strong>Actions</strong> menu on <strong>Edit Service</strong> page</p></figcaption></figure>


5. Click **Next** to proceed to the **Advanced Options** page.
6.  In the **Other Container Config** field, add the `tolerations` operator YAML you have customized for your container. \


    <figure><img src="../.gitbook/assets/tol2.png" alt=""><figcaption><p><strong>Other Container Config</strong> field in <strong>Advanced Options</strong> page</p></figcaption></figure>


7. Click **Update**. Your container has been updated with your custom specification for the **tolerations** operator.&#x20;

### Example Code: `tolerations` operator YAML

In this example:

* If a Pod is running and a taint matching `key1` exists on the node, then the Pod will not schedule the node (`NoSchedule`).
* If a Pod is running and a taint matching `example-key` exists on the node, then the Pod stays bound to the node for `6000` seconds, and then is evicted (`NoExecute`). If the taint is removed before that time, the Pod will not be evicted.

{% code title="tolerations YAML" %}
```yaml
tolerations:
  - key: key1
    operator: Equal
    value: value1
    effect: NoSchedule
  - key: example-key
    operator: Exists
    effect: NoExecute
    tolerationSeconds: 6000
```
{% endcode %}
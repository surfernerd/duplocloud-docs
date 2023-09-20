---
description: Enable setting of SNS Topic Alerts for specific Tenants
---

# SNS Topic Alerts

SNS Topic Alerts provide a flexible and scalable means of sending notifications and alerts across different AWS services and external endpoints, allowing you to stay informed about important events and incidents happening in your AWS environment.

SNS is a fully managed service that enables you to publish messages to topics. The messages can be delivered to subscribers or endpoints, such as email, SMS, mobile push notifications, or even HTTP endpoints.

Configuring this setting will attach the SNS Topic to the alerts in the _OK_ and _Alarm_ state.

## Configuring Tenants to set SNS Topic Alerts

1. In the DuploCloud Portal, navigate to **Administrator** -> **Tenants**. The **Tenants** page displays.
2. Select the Tenant for which you want to set SNS Topic Alerts from the **Name** column.
3. Click **Settings**.
4. Click **Add**. The **Add Tenant Feature** pane displays.
5. From the **Select Feature** list box, select **Other**.
6.  In the field below the **Select Feature** list box, enter a **valid SNS Topic ARN**.\


    <div align="left">

    <figure><img src="../../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

    </div>
7.  Click **Add**. The configuration displays in the **Settings** tab.\


    <figure><img src="../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>
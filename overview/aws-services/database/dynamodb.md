---
description: Adding DynamoDB Tables in DuploCloud
---

# AWS DynamoDB database tables

When using DynamoDB in DuploCloud AWS, the required permissions to access the DynamoDB from a virtual machine (VM), Lambda functions, and containers are provisioned automatically using Instance profiles. Therefore, no Access Key is required in the Application code.

{% hint style="warning" %}
When you write application code for DynamoDB in DuploCloud AWS, use the IAM role/Instance profile to connect to these services. If possible, use the AWS SDK constructor, which uses the region.
{% endhint %}

1. In the DuploCloud Portal, navigate to **Cloud Services** -> **Database.**
2. Click the **DynamoDB** tab.
3.  Click **Add**. The **Create a DynamoDB Table** pane displays.\


    <div align="left">

    <figure><img src="../../../.gitbook/assets/dynamo_1.png" alt=""><figcaption><p><strong>Create a DynamoDB Table</strong> pane</p></figcaption></figure>

    </div>


4. Specify the **DynamoDB Table Name** and other required fields, including **Primary Key**, **Key Type**, **Attribute Type**, **Sort Key**, and **Sort Key Type**.
5. Click **Create**.&#x20;

For detailed guidance about configuring the `duplocloud_aws_dynamodb_table`, refer to the Terraform[ documentation](https://registry.terraform.io/providers/duplocloud/duplocloud/latest/docs/resources/aws\_dynamodb\_table). This resource allows for creating and managing AWS DynamoDB tables within DuploCloud.

{% hint style="info" %}
Perform additional configuration, as needed, in the AWS Console by clicking the   **>\_** **Console** icon. In the AWS console, you can configure the application-specific details of DynamoDB database tables. However, no access or security-level permissions are provided.
{% endhint %}

After creating a DynamoDB table, you can retrieve the final name of the table using the `.fullname` attribute, which is available in the read-only section of the documentation. This feature is handy for applications that dynamically access table names post-creation. If you encounter any issues or need further assistance, please refer to the documentation or contact support.
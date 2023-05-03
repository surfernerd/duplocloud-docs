---
description: Create a read replica of an Aurora database
---

# Aurora RDS replicas

Aurora database replica setup is slightly different from [adding an RDS read replica](../add-an-rds-read-replica.md).

## Adding an Aurora read replica&#x20;

1. [Create an Aurora RDS database](../).
2. In the DuploCloud Portal, navigate to **DevOps** -> **Database**.
3. In the **RDS** tab, click the ( <img src="../../../../../.gitbook/assets/image (12).png" alt="" data-size="line"> ) icon in the **Actions** column and select **Add Replica**. The **Add Replica** pane displays.

Follow one of these procedures to complete the serverless and MySQL replicas setup.

### Adding an Aurora Serverless read replica&#x20;

1. In the **Add Replica** pane, enter a name for the Serverless replica in the Replica Name field.
2. In the **RDS Engine** field, select the **Aurora** RDS Serverless engine you want the replica to use.
3. Specify **Min Capacity (ACUs)** and **Max Capacity (ACUs)**.
4. From the **RDS Instance Size** list box, select the appropriate instance size.
5. Click **Save**. The replica is created with a **Reader** role and displayed in the **RDS** tab.

<figure><img src="../../../../../.gitbook/assets/aurora_serverless_replica.png" alt=""><figcaption><p><strong>Add Replica</strong> pane for Aurora Serverless replica creation</p></figcaption></figure>

#### Updating instance sizes for Aurora Serverless read replicas

To modify instance sizes for an existing Aurora Serverless replica:

1. In the DuploCloud Portal, navigate to **DevOps** -> **Database** and, in the **RDS** tab, locate the read replica you want to update in the **Name** column.&#x20;
2.  Click the ( <img src="../../../../../.gitbook/assets/Kabab_three_Vertical_dots (3).png" alt="" data-size="line"> ) icon in the **Actions** column and select **Update Instance Size**. The **Update Instance Size** pane displays.

    <figure><img src="../../../../../.gitbook/assets/aurora_mysql_update_is_mysql.png" alt=""><figcaption></figcaption></figure>
3. From the **RDS Instance Size** list box, select the appropriate instance size.
4. Click **Save**.

### Adding an Aurora MySQL read replica&#x20;

1. In the **Add Replica** pane, enter a name for the MySQL replica in the **Replica Name** field.
2. From the **RDS Instance Size** list box, select the appropriate instance size.
3. From the **Availability Zone** list box, select an availability zone
4. Click **Save**. The replica is created with a **Reader** role and displayed in the **RDS** tab.

<figure><img src="../../../../../.gitbook/assets/aurora_mysql_replica.png" alt=""><figcaption><p><strong>Add Replica</strong> pane for Aurora MySQL replica creation</p></figcaption></figure>
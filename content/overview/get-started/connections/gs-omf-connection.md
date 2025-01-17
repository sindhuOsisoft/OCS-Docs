---
uid: gsOMF
---

# Get started with OMF connections

To send OSIsoft Message Format (OMF) data to OCS, you must first configure an OMF connection. For more information about OMF connections, see [OMF best practices](xref:bpOMFConnection).

Use this get started procedure to become familiar with OMF connections.

## Procedure

1. In the left pane, select **Security** > **Clients**.

3. Verify that there is at least one client-credentials client to use in the OMF connection. If you need to create one, refer to the Clients section.

4.  Click on the menu and click **Connections** (under Data Management).

5.  From the `Namespace` field, select **MyData**.

6.  From the **Type** drop-down list, select **OMF**.

7.  Click **Add Connection** to open the `Add PI System Connection` window.

8.  In the `Name` field, enter **MyData** and click **Next**.

9.  In the **Clients** tab, click one of the clients in the **Available** list to add it
    to the **Selected** list. Click **Next**.

    **Note:** For the purposes of this get started exercise, you may choose any client.

10. In the **Namespaces** tab, verify that the MyData namespace appears in the
    **Selected** list. Click **Next**.

11. In the **Review** tab, verify that the **Clients** list shows the client-credentials
    client you chose, and the **Namespaces** list shows the *MyData* namespace.
    Click **Save**.

    An application can now use the selected client-credentials client to write OMF data to the MyData namespace.

12. Follow these tips to learn more about OMF connections.

  **Tip:** Click **Manage Permissions** to open the `Manage Permissions` window.

     In this window, you configure permissions only on the connection object itself. Click **Cancel** to continue.

 **Tip:** Click **Edit Connection** to open the `Edit` window.

     Use this window to edit the name and description of the connection. Enter the new name *MyDataEdit* and enter the description *OMF Connection used by MyData*. When you are done, click **Next** until you get to the **Review** tab, and then click **Save**.

## Next step

If you have not already completed [Get started with PI to OCS connections](xref:gsPItoOCS), do this next. Otherwise, continue with [Get started with types](xref:gsTypes).

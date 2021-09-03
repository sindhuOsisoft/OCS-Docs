---
uid: install-agent
---

# Install the PI to OCS Agent

When you install the PI to OCS Agent, make sure to follow these guidelines:

* Install the agent on a host computer separate from your PI Data Archive deployment.
* Use a domain account that has been granted Administrator privileges on a computer registered to the same domain.
* Enable read access to Data Archive security tables and the PI points and data to be transferred.

You can download the PI to OCS Agent Installation kit and then transfer it to the computer that will host the agent.

**NOTE:** The PI to OCS Agent installation cannot be completed if the system time is not correct. Additionally, you will not be able to complete the PI to OCS Agent installation if Internet Explorer Enhanced Security configuration is enabled. See [Disable Internet Explorer Enhanced Security Configuration](xref:disable-ie-security) for details. 

## Configure access to PI Data Archive Security tables and PI point data

**IMPORTANT:** The PI to OCS Agent requires the Windows service account to "run as user". Read access to the following PI Data Archive data is required:

* Archive data (the PIARCDATA Security table)
* The PI points configuration table (PIPOINT Security table)
* The PI points and data to be transferred

## Topics in this section

This topic contains these sections:

* [Install the PI to OCS Agent](#install-the-pi-to-ocs-agent)

* [Verify the PI to OCS Agent is running and registered](#verify-the-pi-to-ocs-agent-is-running-and-registered)


## Install the PI to OCS Agent

1. In the OCS portal, click the ![ ](../../images/waffle-button.png) icon, then click **Data Collection > PI to OCS Agents**.

   **Result:** The `PI to OCS Agents` window opens.

2. Click the **Download Agent** button.

   **Result:** The **Agent Installer Download** dialog box opens.

3. Download the agent to the desired location.

4. Navigate to the downloaded PI to OCS agent installation file.

5. Right-click the PI to OCS Agent installation file, then click **Run as administrator**.

6. Click **Yes**.

   **Result**: The **Welcome** page opens.

7. Click **Next**.

   **Result:** The **Company Information** page opens.

   ![](../../images/agent-co-info.png)

8. Enter your OCS tenant ID or company alias in the **Tenant ID or Company Alias** text box, then click **Next**.

   **Note:** You are logged on to your tenant account in OCS.  The account used to log on must be assigned to the OCS Tenant Administrator role to complete the PI to OCS Agent installation.

   **Result:** The PI to OCS Agent setup kit advances to the **Browser Login** page. An OCS message opens in your web browser regarding the status of the user authentication process. 

9. Close the browser window, then click **Next** in the PI to OCS Agent wizard.

   **Result:** The **Namespace** page opens.

10. Select or enter the following information for your PI to OCS connection, then click **Next**:

    * **Namespace**: Select the location where your transferred data will be stored. The region indicates where the namespace resides. Streaming data sent by the PI to OCS Agent only goes to the selected namespace's region.

    * **Agent Description:** Enter an optional name for your agent.

      **Result:** The **Service Account** page opens.

11. Select the service account type for the connection:

    * **NT Service**: Use an NT account to connect to PI Data Archive.

    * **This account**: Specify a user name and password (domain\account) to connect to PI Data Archive.

    **Note:** The service account used to run the PI to OCS Service requires Administrator privileges. Read access to the PIARCDATA Security table, PIPOINT Security table, and the PI points and data to be transferred is also required.

12. Click the **Install** button.

    **Result:** The PI to OCS Agent is installed.

    **Note:** Installation may take a few moments.

13. After the agent has been successfully installed, click **Close** to close the PI to OCS Agent wizard.

    **Result**: The PI to OCS Configuration Utility opens. See [Run the PI to OCS Agent Configuration Utility](xref:pi-to-ocs-utility) for instructions.

    **Note:** An agent cannot be registered until a PI Data Archive server has been added and configured.

## Verify the PI to OCS Agent is running and registered

After installation, check that the PI to OCS Agent Windows service is running on the machine where the agent is installed. You also should confirm the agent is registered in OCS.

### Procedure

1. On the host machine where you installed the agent, type *services.msc* in the text box next to the Windows menu button, then press ENTER.

2. In the `Services` window, scroll to and verify that that the PI to OCS Agent’s status is running.

![](../../images/services-window.png)

3. Navigate to the **PI to OCS Agents page** in OCS, then select the connection you just created.

4. On the **Details** pane, Verify that "Registered" appears next to the **Agent Status** field.

![Agent status](../../images/details-pane.png)

   **Note:**  The agent status is also displayed in the PI to OCS Configuration Utility.  See [List of agent status states](xref:pi-to-ocs-utility#list-of-agent-status-states) for a list of states and descriptions that explain why an agent may not be running.

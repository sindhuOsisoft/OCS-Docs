---
uid: install-agent
---

# Install the PI to OCS Agent

Install the PI to OCS Agent on a host computer that is separate from your PI Data Archive deployment. Use an account with Administrator privileges. You can download the PI to OCS Agent Installation kit and then transfer it to the computer that will host the agent.

**NOTE:** The PI to OCS Agent installation cannot be completed if the system time is not correct. Additionally, you will not be able to complete the PI to OCS Agent installation if Internet Explorer Enhanced Security configuration is enabled. Please see the [Disable Internet Explorer Enhanced Security Configuration](#_Disable_Internet_Explorer) topic for details. 



## Topics in this section

This topic contains these subtopics:

* [Install the PI to OCS Agent](#install-the-pi-to-ocs-agent)

* [Verify the PI to OCS Agent is running and registered](#verify-the-PI-to-ocs-agent-is-running-and-registered)


## Install the PI to OCS Agent

### Procedure

1. In the OCS portal, click the menu icon, then click **PI to OCS Agents** under **Data Collection**.

2. Click **Download Agent**.
   **Result:** The **Agent Installer** window opens.

3. Select the closest mirror location, **US** or **EU**.
   **Result:** The **Save As** dialog box opens.

   **Note:** The mirror location you select does not determine where your data gets stored.

4. Download the agent to the desired location.

4. Close the **Download Installation Kit** window.

5. Navigate to the downloaded PI to OCS agent installation file.

6. Right-click the PI to OCS agent installation file, then click **Run as administrator**.

8. Click **Yes**.
   **Result**: The **Welcome** page opens.

![PI to OCS Agent Welcome page](../..\images\agent-welcome.png)


9. Click **Next** in the **PI to OCS Agent** page.

   **Result:** The **Company Information** page opens.

   ![Company Information page](../..\images\agent-co-info.png)
	​													

10. In the **Tenant ID or Company Alias** text box, enter your OCS account ID or company alias, then click **Next**.
    
    **Note:** After entering your company information and clicking **Next**, you will be prompted to log into your tenant in OCS.  The account used to log in must be assigned to the OCS Account Administrator role to complete the PI to OCS Agent installation. 
    
    **Result:** PI to OCS Agent setup kit advances to the **Browser Login** page. An OCS message displays in your browser regarding the status of user authentication. 
    
11. Close the browser window.

12. In the **Browser Login** page, click **Next**. 

    **Result:** The **Namespace** page opens.

13. Select or enter the following information for your PI to OCS connection:

    - **Namespace**: Select the location where your transferred data will be stored. The region indicates where the namespace resides. Streaming data will be sent to the selected namespace's region by the PI to OCS Agent.
    
    - **Agent Description**: Enter a descriptive name for the PI to OCS Agent. This name will be shown next to the installed agent on the **PI to OCS Agents** page in OCS.
![The Namespace page](../..\images\agent-namespace.png)

14. Click **Next**.

    **Result:** The **Service Account** page opens.
    ![](../..\\images\agent-serv-acct.png)
    
15. Select the service account type for the connection:

    - **NT Service**: Use an NT account to connect to PI Data Archive.

    - **This account**: Specify a user name and password (domain\account) to connect to PI Data Archive.

  **Note:** The service account must have Administrative privileges and read access to certain data on PI Data Archive.

16. Click **Install**.

    **Result:** The PI to OCS Agent is installed. 

    **Note:** Installation may take a few moments.

![](../..\images\agent-complete.png)
17. Click **Close** to close the agent and open the PI to OCS Configuration Utility.
    **Result**: The PI to OCS Configuration Utility opens. See [Use the PI to OCS Agent Configuration Utility](xref:pi-to-ocs-utility) for instructions.

    **Note:** An agent cannot be registered until an AF server or a PI Data Archive server has been configured using the utility.
## Verify the PI to OCS Agent is running and registered

After installation, check that the PI to OCS Agent Windows service is running on the machine where the agent is installed. You also should confirm the agent has been registered in OCS. <!--Do we even need this topic here if the agent does not register until the user has configured and connected to an AF server or PIDA?-->

### Procedure

1. On the host machine where you installed the agent, type *services.msc* in the text box next to the Windows menu button, then press [ENTER].

2. In the **Services** window, verify that that the PI to OCS Agent’s status is running.

![](../..\images\services-window.png)

3. Navigate to the **PI to OCS Agents page** in OCS, then select the connection you just created. 
4. On the **Details** pane, view the **Agent Status** field.
   	![Agent status](../..\images\details-pane.png)

4. Verify that **Registered** appears next to the **Agent Status** field.

   **Note:**  The agent status is also displayed in the PI to OCS Configuration Utility.  See [List of agent status states](xref:pi-to-ocs-utility) for a list of states and descriptions that explain why an agent may not be running.
   
   


---
uid: pi-to-ocs-utility
---

# Use the PI to OCS Agent Configuration Utility

You use the PI to OCS Agent Configuration Utility to configure AF server and PI Data Archive server connection settings before creating a data transfer. After a PI to OCS Agent installation or upgrade, you can use the utility to add or change the source PI Data Archive and/or AF server, view connection details, create and add AF and PI mappings, and set data privacy settings. 

### Topics in this section

* [Access the PI to OCS Agent Configuration Utility](#access-the-pi-to-ocs-agent-configuration-utility)

* [Quick tour of the PI to OCS Agent Configuration Utility](#quick-tour-of the-pi-to-ocs-agent-configuration-utility)

* [Add an AF server](#add-an-af-server)

* [Create an AF mapping](#create-an-af-mapping)

* [Add a PI Data Archive](#add-a-pi-data-archive)

* [Create a PI mapping](#create-a-pi-mapping)

* [List of agent status states](#list-of-agent-status-states)

* [Set data privacy and add an agent description](#set-data-privacy-and-add-an-agent-description)



## Access the PI to OCS Agent Configuration Utility

You can open the PI to OCS Agent Configuration Utility to change server connections and other settings after the initial setup. 

**Note:** If you're not the original user who installed the agent, the new user account will need to be authenticated in OCS before access is granted to the utility. 

### Procedure

1. Click the Windows menu button.

2. On the Windows menu, scroll down and click **OSIsoft**, then click **PI to OCS Agent Configuration Utility**.

   **Result:** Upon successful authentication, the **PI to OCS Agent Configuration Utility** opens.
   
   **Note:** If you have not yet added an AF server or PI Data Archive server, see [Add an AF server](#add-an-af-server) or [Add a PI Data Archive](#add-a-pi-data-archive) for instructions.

### Quick tour of the PI to OCS Agent Configuration Utility

   ![AF server details](../..\images\utility-callouts.png)


| Number  | Description                                                  |
| :-----: | ------------------------------------------------------------ |
| **1. ** | Name of the host computer where the agent is installed       |
| **2.**  | An optional name for an agent                                |
| **3.**  | Displays the PI to OCS Agent's status                        |
| **4. ** | Provides details about the agent's registration state        |
| **5.**  | Currently running PI to OCS Agent version                    |
| **6.**  | Type of agent service account.                               |
| **7.**  | Set data privacy options and assign an agent description.    |
| **8.**  | View information about the server connection and its configuration. |
| **9.**  | Source AF server name                                        |
| **10.** | The version of PI AF installed on the connected AF server    |
| **11.** | The ID number of the connected AF server                     |
| **12.** | The IP address of the connected AF server                    |
| **13.** | Type of AF mapping configured for the service account. Click the pencil icon next to this field to assign an AF mapping to an AF identity. |
| **14.** | Current state of the AF server connection to OCS             |
| **15.** | Change the amount of time in seconds the agent will check for the server before disconnecting. The default connection time is 10 seconds. |
| **16.** | Test a server connection.                                    |
| **17.** | Delete a connection to a(n) AF or PI Data Archive server.    |

   **Note:** After a PI Data Archive server is added, similar information in the table above is displayed in the utility.

   

## Add an AF server

The PI to OCS Agent Configuration Utility opens after you install or upgrade a PI to OCS Agent. If you are installing an agent for the first time, the utility prompts you to add an AF server and/or a PI Data Archive server after agent installation. If you are upgrading an agent, you can add a server after completing the upgrade. 

The utility validates an AF server connection to ensure certain criteria is met:

* That the AF server is not currently registered to any other agents under the same namespace as the current agent

* That the version of PI Asset Framework (AF) installed on the AF server supports the features required for transfers

  ### Procedure

  1. In the **PI to OCS Agent Configuration Utility** window, click the **AF server** button.


![The PI to OCS Agent Configuration Utility](../..\images\utility-01.png)

2. Enter the name of your AF server in the **AF Server Name** text box, then click **Add Server**.
   **Result:** After successful detection, you are advanced to a utility page that displays details about the data source connection(s) and agent.

   **Note:** Once an AF Server has been added, the utility searches for PI Data Archives that are referenced by the AF Server. 
   
3. Confirm the AF source server details are correct:

   * AF server name, version & ID

   * IP address

   * AF mapping (see [Add an AF Mapping](#add-an-af-mapping) for details)

   * Connection status and timeout

4. **Optional:** Click the pencil icon next to the **Connection Timeout** field to change the length of time the agent checks for a server connection before timing out.

5. Click **Save** to keep the current AF server configuration settings and restart the agent.

   ​      

      ![Agent status and state after refresh](../..\images\af-details-refreshed.png)
      																								

6. **Optional**: Click **Test Connection** to check that the connection to the AF server is working.

7. **Optional**: To delete a server connection, click the **Remove Server** button, then click **Yes**. 

## Create an AF Mapping

You can assign an AF mapping to an AF identity. AF mappings enable a specific service account assigned to an AF identity in PI System Explorer to read and transfer AF element and attribute data.  The following applies to AF mappings:

* The user account used to launch the utility must have permission to create mappings.
* You can edit mappings.

### Procedure

1. Open the **PI to OCS Agent Configuration Utility** window.

2. Click the edit icon next to the **AF Mapping** field.
   **Result:** The **Configure AFMappingView** dialog box opens.
   
   ![](../..\images\af-mapping-db.png)
														
   
3. Select the identity for the AF mapping.

4. Click **Edit**. 
   **Result:** If successful, the AF mapping is created for the selected identity.

   ![](../..\images\success-af-map.png)
   											
   
	**Note:** If an AF mapping has been created with another tool, a warning is displayed.  
   
5. Click **Close** to exit.

   

## Add a PI Data Archive

After adding an AF server, you can select the source PI Data Archive you want to use to search for PI point data. The list of available PI Data Archive servers is based on what servers are referenced by elements on the AF server you selected. If you are upgrading an agent, the PI to OCS Agent Configuration Utility maintains the previously selected PI Data Archive configuration.  

**Note:** If you are not adding an AF server, you can select a PI Data Archive server on the first screen of the PI to OCS Agent Configuration Utility.

#### Procedure

1. Click **Add Data Archive** **Server** in the PI to OCS Agent Configuration Utility.
   **Result**:  The first page of the **PI to OCS Agent Configuration Utility** opens.
   ![](../..\images\utility-03.png)
   
   ​																	
   
2. In the **Data Archive Server Name** text box, enter the name of the PI Data Archive server you want to add, then click **Add Server**.
   
   **Result:** The PI Data Archive connection is added and details about the newly added PI Data Archive are displayed.
   ![PI Data Archive connection details](../..\images\utility-pda-details.png)
   
4. Review the following details for your PI Data Archive:
   * Server name, version, and server ID
   * IP address
   * PI mapping (see [Create a PI mapping](#create-a-pi-mapping) for more information)
   * Connection status and timeout

5. **Optional:** Click the pencil icon next to the **Connection Timeout (sec)** text box to change the length of time the agent checks for a server connection before timing out.

6. **Optional**: Click the **Test Connection** button to confirm that the connection to the Data Archive is working.

7. **Optional**: Click the **Remove Server** button to remove the configured PI Data Archive from the PI to OCS connection.

7. Click **Save** to retain the current PI Data Archive configuration.

8. Optional: Click **Exit** to close the utility.

## Create a PI mapping 

PI mappings enable access to data stored on a PI Data Archive by service accounts assigned to a PI identity.  PI mappings can be created for a PI identity, user or group. Accounts assigned to a PI identity can read and transfer PI point data to OCS.  See ["What are PI identities and mappings?"](https://docs.osisoft.com/bundle/pi-server/page/what-are-pi-identities-and-mappings_new.html) for more information. The following applies to PI mappings:

* The user account used to launch the utility must have permissions to create mappings.
* You can edit mappings.

#### Procedure

1. Navigate to the PI Data Archive details page in the **PI to OCS Agent Configuration Utility** window.

2. Click the pencil icon next to the **PI Mapping** field.
   **Result:** The **Configure Mapping** dialog box opens.

![Configure Mapping dialog box](../..\images\configure-mapping-window.png)

​																									*Configure Mapping dialog box*

3. From the **Identity** list, select an identity for the PI mapping, then click **Edit**.
   **Result:** The PI mapping is created for the selected identity, group or user.
   **Note:** If a PI mapping has already been created with another tool, a warning is displayed. 

4. Click **Close** to return to the utility.

   

## Set data privacy and add an agent description

You can set data privacy settings and assign a descriptive name to an agent in the **PI to OCS Agent Settings** dialog box. Data privacy settings control if the host name of a PI Data Archive is published and displayed in OSIsoft Cloud Services (OCS). <!--Rob, does it also control if the server names get displayed in the PI to OCS Agents window?-->  By default, OCS does not publish host names.  If you opt to have the host name published, it appears in the OCS portal on the **PI to OCS Agents** window as shown here. 

![Agent description and hostname displayed in PI to OCS Agents window](../..\images\pi-to-ocs-agents-hostname.png)


You can assign a descriptive name to an agent. In the OCS portal, this description appears where the agent is referenced, and also allows you to search by agent name. 

#### Procedure

1. In the **PI to OCS Agent Configuration Utility** window, click the pencil icon to the right of **Agent Service Account**.
   **Result:** The **PI to OCS Agent Settings** dialog box opens.

   ![PI to OCS Agent Settings dialog box](../..\images\pi-2-ocs-agent-settings-dialog.png)

2. Under **Data Privacy**, click to select or deselect the **Opt-in to publishing PI to OCS Agent Hostname in OCS Data Privacy setting** option.

3. In the **PI to OCS Agent Description** text box, enter a descriptive name for the Agent.

4. Click **Ok** to save your selections, then click **Save** in the utility.

## List of agent status states

It may take a few minutes for your PI System to be registered. The following states may appear under the Agent Status field in the PI to OCS Configuration Utility to indicate a connection issue.

| **State**                     | **Description**                                              |
| ----------------------------- | ------------------------------------------------------------ |
| Data  Source Connection Issue | Indicates  the PI To OCS Agent isn’t able to connect to the PI Data Archive. Some  reasons for this status include the PI Data Archive is turned off, a firewall  issue is preventing connections or an incorrect name is configured for the  Data Archive (for example, trying to connect to a machine that doesn’t  exist/was renamed). There may be additional reasons for this status. |
| Data  Source Security Issue   | Indicates  the PI Data Archive connection is unsecure and security settings need to be  addressed. |
| Missing Configuration         | The PI Data Archive server or AF server has not been configured in the PI to OCS Agent. |
| Registration Failed           | Contact OSIsoft Customer support for assistance.             |
| Registering                   | The PI to OCS Cloud portion is creating the necessary resources for your PI to OCS Agent. |
| Shutdown                      | The last communication that the PI to OCS Cloud had with the agent was a shutdown message. |

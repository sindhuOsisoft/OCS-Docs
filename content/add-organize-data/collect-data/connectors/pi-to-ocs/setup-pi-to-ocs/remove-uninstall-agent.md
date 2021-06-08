---
uid: remove-agents
---

# Remove or uninstall an agent

You can remove any agents no longer needed in OCS on the `PI to OCS Agents` page in OCS.  You may also want to uninstall an agent from a host machine.

## Remove an agent

You remove an unneeded agent from OCS in the PI to OCS Agents page.

1. Log on to the [OCS portal](https://cloud.osisoft.com).

2. Click the menu ![ ](../../images/waffle-button.png) icon, then click **PI to OCS Agents** (under Data Collection).

3. In the `PI to OCS Agents` window, select an agent in the list.

4. Click the **Remove Agent** button above the list of agents.

   The `Remove Agent` dialog box opens.
   ![](../../images/remove-agent.png)

5. Click **Remove**.

   The agent is removed from the list and deleted from OCS.

## Uninstall an agent

#### Procedure

1. Click the Windows Start button, then click **Settings**.

   The **Windows Settings** window opens.

2. Double-click **Apps** to open the `Apps & features` window.

3. Scroll to and click **PI to OCS Agent** in the list of installed apps.

4. Click **Uninstall** twice, then click **Yes** in the `User Account Control` window.

   The `PI to OCS Agent (Administrator)` window opens.

5. Select the **Uninstall** option, then click **Next**.

6. Click the **Unregister agent from OCS** option, then click **Next**.

   The agent's associated client and connection information is removed in OCS.

7. Select the user account you wish to use to log on to OCS.

   You are returned to the `PI to OCS Agent` window.

8. Click **Uninstall**, then click **Close**.

   The PI to OCS Agent is uninstalled and removed from the host machine.

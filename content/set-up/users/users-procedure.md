---
uid: gpUsers
---

# Add a user

A user is an identity that has access to an OSIsoft Cloud Services (OCS) tenant. Roles assigned to a user determine what permissions the user has on resources in OCS. See the following topics for more information about users:

- [Users](xref:ccUsers)

- [PI Server counterpart](xref:ccUsers#users-pi-server)

- [Users best practices](xref:ccUsers#users-bp)

## Add a user from Azure Active Directory

Follow this procedure to invite a user from Azure Active Directory to your tenant.

1. Click the ![Menu icon](../images/menu-icon.png) icon and select **Security** > **Users**.

1. In the toolbar, click **Add User**.

    The `Add User` window displays.

1. In the **Identity Provider** field, select `Azure Active Directory`.

    This field is only enabled if the tenant uses more than one identity provider. You can change the identity provider on the `Add User` window.

1. In the **User Name** field, enter the user's first and last name or their email address, and then select the user from the list.  

1. In the **Email** field, review the contact email to ensure you have selected the intended user. 

    The invitation to your OCS tenant is sent to the user at this address. Ensure that email is correct so that the invitation is not sent to an unintended recipient.

1. (Optional) On the **Tenant Roles** and **Community Roles** tabs, select additional roles for the user. 

    By default, the user is assigned the `Tenant Member` role which cannot be removed. You can modify a user's roles after they are invited.

1. Click **Add**. 

    OCS sends the invitation to the email address shown in the **Email** field. On the `Users` page, the **Status** column lists the new user as `Pending` until they accept the invitation. If the invitation expires, the status changes to `Expired`. Once expired, the invitation can be resent.

1. Once the user receives the invitation, they should log in using their Azure Active Directory credentials. 

   Once they have logged in, the status of their user changes to `Active`.

## Add a user from another identity provider

Follow this procedure to invite a user from another identity provider to your tenant.

1. Click the ![Menu icon](../images/menu-icon.png) icon and select **Security** > **Users**.

1. In the toolbar, click **Add User**.

    The `Add User` window displays.

1. In the **Identity Provider** field, select the identity provider to use.

    This field is only enabled if the tenant uses more than one identity provider. You can change the identity provider on the `Add User` window.

1. In the **Contact First Name** and **Contact Last Name** fields, enter the user's first and last name.  

1. In the **Contact Email** field, enter the user's email.

    The invitation to your OCS tenant is sent to the user at this address. Ensure that it is correct so that the invitation is not sent to an unintended recipient.

1. (Optional) On the **Tenant Roles** and **Community Roles** tabs, select additional roles for the user. 

    By default, the user is assigned the `Tenant Member` role which cannot be removed. You can modify a user's roles after they are invited.

1. Click **Invite**. 

    OCS sends the invitation to the email address shown in the **Contact Email** field. On the `Users` page, the **Status** column lists the new user as `Pending` until they accept the invitation. If the invitation expires, the status changes to `Expired`. Once expired, the invitation can be resent.

1. Once the user receives the invitation, they should log in using the credentials for the specified identity provider. 

   Once they have logged in, the status of their user changes to `Active`.

## Related links

- [Tenants Users](xref:identity-tenants-users) API

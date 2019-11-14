---
uid: omfIngressSubsctriptions
---

Subscriptions 
=============
Subscription Information 
-----------------------

A Subscription consumes OMF messages from a Topic and forwards them to a data store. Multiple Subscriptions can retrieve OMF messages from a single Topic. 

A Subscription can consume OMF messages from a Topic in a different Namespace. However, the Topic's Namespace must be in the same Region as the Subscription's Namespace. OMF messages that the Subscription is processing are temporarily stored in the Region of its Namespace.

The API calls in this section are used to create and manipulate Subscriptions.

Sequential Data Store (Sds) Subscription 
---------------

A Sequential Data Store Subscription retrieves OMF messages from a Topic and writes them directly to a Namespace in the Sequential Data Store. Currently only Sds Subscriptions are supported. The documentation uses Sds Subscription and Subscription interchangeably.

Data Models 
-----------

Subscription information is contained in an object called Subscription which has the following format: 

| Property             | Type                    | Details                                |
|----------------------|-------------------------|----------------------------------------|
| Id                   | string                  | Unique Id generated by the API during creation. |
| Name                 | string                  | A friendly name for the Subscription.  |
| TopicId              | string                  | Unique Id for the Topic we are subscribing to. |
| TopicTenantId        | string                  | Identifies the owner of the Topic.     |
| TopicNamespaceId     | string                  | Identifies the namespace for the Topic |
| TenantId             | string                  | Identifies the owner of the Subscription. |
| NamespaceId          | string                  | Identifies the namespace for the Subscription. |
| Description          | string                  | Description of the Subscription.       |
| Type                 | integer                 | An enumeration which describes the type of Subscription where Sds=1 |
| CreatedDate          | DateTime                | Date and time this Subscription was created. |
| Enabled              | boolean                 | Whether the Topic exists or not.        |

*****************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions``
---------------------------------------------

Get all Subscriptions for a tenant. 

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 

**Returns**

An array of Subscription objects. 

*********************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}``
---------------------------------------------------------------

Get a specific Subscription. 

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Unique Id for the Subscription. 

**Returns**

A Subscription object. 

*****************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/accesscontrol/subscriptions``
--------------------------------------------

Get the default Access Control List for new Subscriptions.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 

**Returns**

An AccessControlList object.

*****************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/accessrights/subscriptions``
--------------------------------------------

Get the default Access Rights of the requesting identity for any newly created Subscriptions.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 

**Returns**

An array of Access Rights strings.

*******************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}/accesscontrol``
--------------------------------------------

Get the Access Control List for a particular Subscription.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Unique Id for the Subscription. 

**Returns**

An AccessControlList object.

*******************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}/accessrights``
--------------------------------------------

Get the Access Rights of the requesting identity for a particular Subscription.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Unique Id for the Subscription. 

**Returns**

An array of Access Rights strings.

*******************

``GET api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}/owner``
--------------------------------------------

Get the Owner for a particular Subscription.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Unique Id for the Subscription. 

**Returns**

A Trustee object.

*******************

``POST api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions``
--------------------------------------------

Create a new Subscription.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 

**Body**

A Subscription object. The ``Id`` property should not be specified, since it will be automatically generated during creation.

**Returns**

The Subscription object that was created. 

*******************

``PUT api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}``
--------------------------------------------

Update an existing Subscription. Only the name and description may be updated. 

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Subscription Id for the Subscription to be updated.

**Body**

A Subscription object. The ``Id`` property should match the ``subscriptionId`` in the route.

**Returns**

The Subscription object that was updated. 

*******************

``PUT api/v1/tenants/{tenantId}/namespaces/{namespaceId}/accesscontrol/subscriptions``
--------------------------------------------

Update the default Access Control List for new Subscriptions.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 

**Body**

An AccessControlList object.

*******************

``PUT api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}/accesscontrol``
--------------------------------------------

Update the Access Control List for a particular Subscription.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Unique Id for the Subscription. 

**Body**

An AccessControlList object.

*******************

``PUT api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}/owner``
--------------------------------------------

Update the Owner for a particular Subscription.

**Parameters**

``tenantId``
  Unique Id for the tenant. 
``namespaceId``
  Unique Id for the namespace. 
``subscriptionId``
  Unique Id for the Subscription. 

**Body**

A Trustee object.

*******************

``DELETE api/v1/tenants/{tenantId}/namespaces/{namespaceId}/subscriptions/{subscriptionId}``
-----------------------------------------------------------------

Delete a Subscription. 

**Parameters**

``tenantId``
  Unique Id for the tenant.
``namespaceId``
  Unique Id for the namespace.   
``subscriptionId``
  Unique Id for the Subscription. 
*******************
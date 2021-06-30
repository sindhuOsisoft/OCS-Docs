---
uid: sds-stream-bulk-data

---

# Stream Bulk Data
Controller for methods hosted at {namespaceId}/Bulk/Streams/Data/Joins

## `List Window Values`

<a id="opIdStreamsData_List Window Values"></a>

Returns data from multiple streams, joined based on the request specifications. Streams must be of the same type.
GET and POST join requests are supported.
        
[GET method](https://ocs-docs.osisoft.com/Content_Portal/Documentation/SequentialDataStore/Reading_Data_API.html#getjoin): ``stream``, ``joinMode``, ``startIndex``, and ``endIndex`` are specified in the request URI.

[POST method](https://ocs-docs.osisoft.com/Content_Portal/Documentation/SequentialDataStore/Reading_Data_API.html#post-request): only ``joinMode`` is specified in the URI. Streams and read specifications for each stream are specified in the request body.

### Request
```text 
GET /api/v1/Tenants/{tenantId}/Namespaces/{namespaceId}/Bulk/Streams/Data/Joins
```

#### Parameters

`string tenantId`
<br/>Tenant identifier<br/><br/><br/>`string namespaceId`
<br/>Namespace identifier<br/><br/><br/>

### Response

|Status Code|Body Type|Description|
|---|---|---|
|200|Inline|Returns multiple serialized events|
|400|[ErrorResponseBody](#schemaerrorresponsebody)|Missing or invalid inputs|
|401|[ErrorResponseBody](#schemaerrorresponsebody)|Unauthorized|
|403|[ErrorResponseBody](#schemaerrorresponsebody)|Forbidden|
|404|[ErrorResponseBody](#schemaerrorresponsebody)|One of the resources specified was not found|
|409|[ErrorResponseBody](#schemaerrorresponsebody)|Conflict|
|500|[ErrorResponseBody](#schemaerrorresponsebody)|An error occurred while processing the request|
|503|[ErrorResponseBody](#schemaerrorresponsebody)|Service Unavailable|

#### Example response body
> 400 Response

```json
{
  "OperationId": "string",
  "Error": "string",
  "Reason": "string",
  "Resolution": "string",
  "Parameters": {
    "property1": "string",
    "property2": "string"
  }
}
```

---

## `Get Window Values2`

<a id="opIdStreamsData_Get Window Values2"></a>

Returns data from multiple streams, joined based on the request specifications. Streams must be of the same type.
GET and POST join requests are supported.
        
[GET method](https://ocs-docs.osisoft.com/Content_Portal/Documentation/SequentialDataStore/Reading_Data_API.html#getjoin): ``stream``, ``joinMode``, ``startIndex``, and ``endIndex`` are specified in the request URI.

[POST method](https://ocs-docs.osisoft.com/Content_Portal/Documentation/SequentialDataStore/Reading_Data_API.html#post-request): only ``joinMode`` is specified in the URI. Streams and read specifications for each stream are specified in the request body.

### Request
```text 
POST /api/v1/Tenants/{tenantId}/Namespaces/{namespaceId}/Bulk/Streams/Data/Joins
```

#### Parameters

`string tenantId`
<br/>Tenant identifier<br/><br/><br/>`string namespaceId`
<br/>Namespace identifier<br/><br/><br/>

### Response

|Status Code|Body Type|Description|
|---|---|---|
|200|Inline|Returns multiple serialized events|
|400|[ErrorResponseBody](#schemaerrorresponsebody)|Missing or invalid inputs|
|401|[ErrorResponseBody](#schemaerrorresponsebody)|Unauthorized|
|403|[ErrorResponseBody](#schemaerrorresponsebody)|Forbidden|
|404|[ErrorResponseBody](#schemaerrorresponsebody)|One of the resources specified was not found|
|409|[ErrorResponseBody](#schemaerrorresponsebody)|Conflict|
|500|[ErrorResponseBody](#schemaerrorresponsebody)|An error occurred while processing the request|
|503|[ErrorResponseBody](#schemaerrorresponsebody)|Service Unavailable|

#### Example response body
> 400 Response

```json
{
  "OperationId": "string",
  "Error": "string",
  "Reason": "string",
  "Resolution": "string",
  "Parameters": {
    "property1": "string",
    "property2": "string"
  }
}
```

---
## Definitions

### ErrorResponseBody

<a id="schemaerrorresponsebody"></a>
<a id="schema_ErrorResponseBody"></a>
<a id="tocSerrorresponsebody"></a>
<a id="tocserrorresponsebody"></a>

Contains the error message format that follows the OCS error standards

#### Properties

|Property Name|Data Type|Required|Nullable|Description|
|---|---|---|---|---|
|OperationId|string|false|true|Operation unique identifier of action that caused the error|
|Error|string|false|true|Error description|
|Reason|string|false|true|Reason for the error|
|Resolution|string|false|true|Resolution to resolve the error|
|Parameters|object|false|true|IDs or values that are creating or are affected by the error|

```json
{
  "OperationId": "string",
  "Error": "string",
  "Reason": "string",
  "Resolution": "string",
  "Parameters": {
    "property1": "string",
    "property2": "string"
  }
}

```

---

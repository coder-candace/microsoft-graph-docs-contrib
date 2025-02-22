---
title: "Get customSecurityAttributeAudit"
description: "Get a specific audit log generated by activities related to custom security attribute management in Microsoft Entra ID."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-access-reports"
doc_type: apiPageType
---

# Get customSecurityAttributeAudit

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a specific audit log generated by activities related to custom security attribute management in Microsoft Entra ID.

[!INCLUDE [national-cloud-support](../../includes/all-clouds.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "customsecurityattributeaudit_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/customsecurityattributeaudit-get-permissions.md)]

[!INCLUDE [rbac-customsecurityattibutes-audit-apis-read](../includes/rbac-for-apis/rbac-customsecurityattibutes-audit-apis-read.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /auditLogs/customSecurityAttributeAudits/{customSecurityAttributeAuditId}
```

## Optional query parameters

This method does not support any OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [customSecurityAttributeAudit](../resources/customsecurityattributeaudit.md) object in the response body.

## Examples

### Request

The following is an example of a request.
# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_customsecurityattributeaudit"
}
-->
``` http
GET https://graph.microsoft.com/beta/auditLogs/customSecurityAttributeAudits/Directory_46ef8262-896f-4a39-9666-db82e22e778b_GXP3K_386490241
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-customsecurityattributeaudit-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/get-customsecurityattributeaudit-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-customsecurityattributeaudit-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-customsecurityattributeaudit-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-customsecurityattributeaudit-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/get-customsecurityattributeaudit-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/get-customsecurityattributeaudit-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/get-customsecurityattributeaudit-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

The following is an example of the response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.customSecurityAttributeAudit"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
   "@odata.context": "https://graph.microsoft.com/beta/$metadata#auditLogs/customSecurityAttributeAudits/$entity",
   "id": "Directory_46ef8262-896f-4a39-9666-db82e22e778b_GXP3K_386490241",
   "category": "AttributeManagement",
   "correlationId": "f3b07799-da67-4a79-bb56-eed7ba2ca404",
   "result": "success",
   "resultReason": "",
   "activityDisplayName": "Update an attribute set",
   "activityDateTime": "2023-07-27T00:36:52.014638Z",
   "loggedByService": "Core Directory",
   "operationType": "Update",
   "userAgent": null,
   "initiatedBy": {
       "app": null,
       "user": {
           "id": "573bfb22-436c-40c7-82c2-d1b67677c33c",
           "displayName": null,
           "userPrincipalName": "admin1@contoso.com",
           "ipAddress": "{ipAddress}",
           "userType": null,
           "homeTenantId": null,
           "homeTenantName": null
       }
   },
   "targetResources": [
       {
           "id": "dd707ff2-fd98-4ce5-9733-eafa781d3b12",
           "displayName": "DesignTest",
           "type": "Other",
           "userPrincipalName": null,
           "groupType": null,
           "modifiedProperties": [
               {
                   "displayName": "MaxAttributesPerSet",
                   "oldValue": "[25]",
                   "newValue": "[20]"
               },
               {
                   "displayName": "Included Updated Properties",
                   "oldValue": null,
                   "newValue": "\"MaxAttributesPerSet\""
               }
           ]
       }
   ],
   "additionalDetails": [
       {
           "key": "User-Agent",
           "value": "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/115.0"
       }
   ]
}
```


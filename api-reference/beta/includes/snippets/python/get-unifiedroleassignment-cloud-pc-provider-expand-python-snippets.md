---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = UnifiedRoleAssignmentMultipleItemRequestBuilder.UnifiedRoleAssignmentMultipleItemRequestBuilderGetQueryParameters(
		expand = ["roleDefinition"],
)

request_configuration = UnifiedRoleAssignmentMultipleItemRequestBuilder.UnifiedRoleAssignmentMultipleItemRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.role_management.cloud_p_c.role_assignments.by_unified_role_assignment_multiple_id('unifiedRoleAssignmentMultiple-id').get(request_configuration = request_configuration)


```
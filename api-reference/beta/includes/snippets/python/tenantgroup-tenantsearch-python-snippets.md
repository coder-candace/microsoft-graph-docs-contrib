---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = TenantSearchPostRequestBody(
	tenant_id = "String",
)

result = await graph_client.tenant_relationships.managed_tenants.tenant_groups.microsoft_graph_managed_tenants_tenant_search.post(request_body)


```
---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = IdentityUserFlowAttribute(
	display_name = "Hobby",
	description = "Your hobby",
	data_type = IdentityUserFlowAttributeDataType.String,
)

result = await graph_client.identity.user_flow_attributes.post(request_body)


```
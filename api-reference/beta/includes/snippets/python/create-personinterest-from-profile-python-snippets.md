---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = PersonInterest(
	categories = [
		"Sports",
	],
	description = "World's greatest football club",
	display_name = "Chelsea FC",
	web_url = "https://www.chelseafc.com",
)

result = await graph_client.me.profile.interests.post(request_body)


```
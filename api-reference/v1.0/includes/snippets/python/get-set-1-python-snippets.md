---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.sites.by_site_id('site-id').term_store.groups.by_group_id('group-id').sets.get()


```
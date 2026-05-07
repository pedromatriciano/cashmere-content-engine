# cashmere-content-engine

Public host for Cashmere weekly content media (videos, images) referenced by
Buffer's GraphQL API.

Buffer fetches media by URL at `createPost` time and re-hosts on its own CDN.
This repo provides clean `raw.githubusercontent.com/.../file.mp4` URLs that
Buffer's pipeline can consume without the redirect / `Content-Disposition`
issues that break Google Drive URLs.

Files are organised by week:

```
buffer-media/
  YYYY-MM-DD/
    <slug>.mp4
    <slug>.png
```

Old weeks can be cleared once Buffer has fetched the URL — Buffer keeps its own
copy on its CDN after ingestion.

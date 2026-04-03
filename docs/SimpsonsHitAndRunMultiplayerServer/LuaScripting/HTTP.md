---
title: "HTTP"
description: "Provides information about the HTTP table available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 528 # 1.1
---

The `HTTP` table provides functions for making HTTP requests from Simpsons Hit & Run Multiplayer Server mods.

In order to use the `HTTP` table, the server must enable the `WebRequests` permission in their `Server.yaml` file:

```yaml
modPermissions:
  webRequests: true
```

All HTTP requests are performed asynchronously. A callback function is called when the request completes.

## Response Object

All HTTP functions accept an optional callback that receives a response object with the following fields:

| Field        | Type    | Description                                                                    |
|--------------|---------|--------------------------------------------------------------------------------|
| `statusCode` | number  | The HTTP status code returned by the server.                                   |
| `ok`         | boolean | `true` if the request completed without error and returned a 2xx status code.  |
| `body`       | string  | The response body. May be `nil` if the request failed.                         |
| `error`      | string  | An error message. Only present if the request failed.                          |

## Methods

| Function Name        | Description                               |
|----------------------|-------------------------------------------|
| [[HTTP/Get.md]]      | Performs an HTTP GET request.             |
| [[HTTP/Post.md]]     | Performs an HTTP POST request.            |
| [[HTTP/Request.md]]  | Performs a fully customised HTTP request. |

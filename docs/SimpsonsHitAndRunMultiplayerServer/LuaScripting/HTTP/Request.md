---
title: "HTTP.Request"
description: "Provides information about the HTTP.Request function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
---

Performs a fully customised HTTP request.

**Added in Version 1.1.**

# Syntax
```lua
HTTP.Request( options, callback )
```

## Arguments
* `options` (table): Configuration for the request.
  * `url` (string, required): The URL to send the request to.
  * `method` (string): The HTTP method to use (e.g. `"GET"`, `"POST"`, `"PUT"`, `"DELETE"`). Defaults to `"GET"`.
  * `body` (string): The request body. Only applicable for methods that support a body (e.g. `POST`, `PUT`).
  * `contentType` (string): The `Content-Type` header value. Only used when a `body` is provided.
  * `headers` (table): A table of additional headers to include in the request, as key-value string pairs.
  * `timeout` (number): The maximum time in milliseconds to wait for a response. Defaults to `30000`.
* `callback` (function): A function to call when the request completes. Receives a response object. See [[../HTTP.md]] for the response object structure.

## Return Values
No return values.

# Examples
```lua
HTTP.Request({
    url = "https://example.com/api/data",
    method = "PUT",
    body = String.ToJSON({ status = "active" }),
    contentType = "application/json",
    headers = {
        Authorization = "Bearer my-token",
    },
}, function(response)
    if response.ok then
        print("Update successful.")
    else
        print("Update failed: " .. (response.error or tostring(response.statusCode)))
    end
end)
```

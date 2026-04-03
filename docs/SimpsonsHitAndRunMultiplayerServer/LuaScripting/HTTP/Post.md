---
title: "HTTP.Post"
description: "Provides information about the HTTP.Post function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
---

Performs an HTTP POST request.

**Added in Version 1.1.**

# Syntax
```lua
HTTP.Post( url, body, callback, options )
```

## Arguments
* `url` (string): The URL to send the POST request to.
* `body` (string): The body of the POST request.
* `callback` (function): A function to call when the request completes. Receives a response object. See [[../HTTP.md]] for the response object structure.
* `options` (table, optional): Optional configuration for the request.
  * `contentType` (string): The `Content-Type` header value to use. Defaults to `"application/json"`.
  * `timeout` (number): The maximum time in milliseconds to wait for a response. Defaults to `30000`.

## Return Values
No return values.

# Examples
```lua
local body = String.ToJSON({ event = "playerJoined", name = "Homer" })

HTTP.Post("https://example.com/api/webhook", body, function(response)
    if response.ok then
        print("Webhook delivered successfully.")
    else
        print("Webhook failed: " .. (response.error or tostring(response.statusCode)))
    end
end)
```

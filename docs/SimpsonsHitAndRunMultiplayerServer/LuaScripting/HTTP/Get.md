---
title: "HTTP.Get"
description: "Provides information about the HTTP.Get function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 528 # 1.1
---

Performs an HTTP GET request.

# Syntax
```lua
HTTP.Get( url, callback, options )
```

## Arguments
* `url` (string): The URL to send the GET request to.
* `callback` (function): A function to call when the request completes. Receives a response object. See [[../HTTP.md]] for the response object structure.
* `options` (table, optional): Optional configuration for the request.
  * `timeout` (number): The maximum time in milliseconds to wait for a response. Defaults to `30000`.

## Return Values
No return values.

# Examples
```lua
HTTP.Get("https://example.com/api/data", function(response)
    if response.ok then
        print(response.body)
    else
        print("Request failed: " .. (response.error or tostring(response.statusCode)))
    end
end)
```

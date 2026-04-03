---
title: "Command Line Arguments"
description: "This page lists the command line arguments for the Simpsons Hit & Run Multiplayer Server."
authors: [ 2 ]
---

These are the various command line arguments that the Simpsons Hit & Run Multiplayer Server supports.

Several of these options override the same options in the [[Configuration.md]] file.

# --advanced-logging
**Added in Version 1.0.**

Enables advanced logging features.

```sh
./SHARMPServer --advanced-logging
```

# --config
**Added in Version 1.0.**

Sets the path to the server's configuration file.

This will create the file if it doesn't exist.

```sh
./SHARMPServer --config "C:\Users\Homer\Desktop\MySHARMPServerConfig.yaml"
```

# --password
**Added in Version 1.0.**

Sets the password to the server.

```sh
./SHARMPServer --password "hunter2"
```

# --port
**Added in Version 1.0.**

Sets the port the server will bind to.

```sh
./SHARMPServer --port 6969
```

# --max-players
**Added in Version 1.0.**

Sets the maximum amount of connected players.

```sh
./SHARMPServer --max-players 8
```

# --no-default-mod-path
**Added in Version 1.0.**

Makes the server not load mods from the adjacent `ServerMods` folder.

```sh
./SHARMPServer --no-default-mod-path
```

# --server-name
**Added in Version 1.0.**

Sets the name of the server.

```sh
./SHARMPServer --server-name
```

# --shut-up-i-am-not-being-scammed
**Added in Version 1.0.**

Disables this message logged to the console on startup about paying for this software being a scam:

> If you did not get this program from Donut Team or Mod Bakery, or if you paid for this software, you've been scammed.
> 
> Learn more about Donut Team authenticity at https://donut.team/q/authenticity

```sh
./SHARMPServer --shut-up-i-am-not-being-scammed
```

# --generate-docs
**Added in Version 1.0.**

Generates a Lua Scripting API Reference document.

```sh
./SHARMPServer --generate-docs
```

# --no-mods
**Added in Version 1.0.**

Prevents the server from loading any server-side mods.

```sh
./SHARMPServer --no-mods
```
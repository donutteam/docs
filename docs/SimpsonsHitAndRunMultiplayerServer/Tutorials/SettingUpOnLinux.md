---
title: "Setting Up on Linux"
description: "A guide to setting up the Simpsons Hit & Run Multiplayer Server on Linux."
authors: [ 1 ]
---

This guide will walk you through setting up the Simpsons Hit & Run Multiplayer Server on Linux.

# Prerequisites

Before you begin, ensure your system meets the following requirements:

* **Operating System**: 64-bit Linux
* **Memory**: 1 GB

You will also need to install the following:

* [Microsoft .NET Desktop Runtime 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)

# Step 1: Download

Download the latest version of the Simpsons Hit & Run Multiplayer Server from Mod Bakery: [Project:124]

# Step 2: Extract

Extract the downloaded archive to a directory of your choice.

```sh
unzip SHARMPServer.zip -d SHARMPServer
cd SHARMPServer
```

# Step 3: Make the Server Executable

Make the server binary executable:

```sh
chmod +x SHARMPServer
```

# Step 4: Run the Server

Run the server for the first time. It will generate a default `Server.yaml` configuration file in the same directory and then exit.

```sh
./SHARMPServer
```

# Step 5: Configure

Open `Server.yaml` in a text editor and adjust the settings to your liking. See [[../Configuration.md]] for a full description of every available option.

# Step 6: Start the Server

Run the server again. It will now start and begin accepting connections on the configured port (default: `7777`).

```sh
./SHARMPServer
```

Players can connect using the [[/LucasSimpsonsHitAndRunModLauncher/Intro.md]] with the Multiplayer hack enabled.

---
title: "Setting Up on Windows"
description: "A guide to setting up the Simpsons Hit & Run Multiplayer Server on Windows."
authors: [ 1 ]
---

This guide will walk you through setting up the Simpsons Hit & Run Multiplayer Server on Windows.

# Prerequisites

Before you begin, ensure your system meets the following requirements:

* **Operating System**: Windows 8 or newer (64-bit)
* **Memory**: 1 GB

You will also need to install the following:

* [Microsoft .NET Desktop Runtime 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
* [Visual Studio 2013 (VC++ 12.0) (no longer supported) x64](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#visual-studio-2013-vc-120-no-longer-supported)

# Step 1: Download

Download the latest version of the Simpsons Hit & Run Multiplayer Server from Mod Bakery: [Project:124]

# Step 2: Extract

Extract the downloaded archive to a folder of your choice.

# Step 3: Run the Server

Run `SHARMPServer.exe`. On first launch, the server will generate a default `Server.yaml` configuration file in the same directory and then exit.

# Step 4: Configure

Open `Server.yaml` in a text editor and adjust the settings to your liking. See [[../Configuration.md]] for a full description of every available option.

# Step 5: Start the Server

Run `SHARMPServer.exe` again. The server will now start and begin accepting connections on the configured port (default: `7777`).

Players can connect using the [[/LucasSimpsonsHitAndRunModLauncher/Intro.md]] with the Multiplayer hack enabled.

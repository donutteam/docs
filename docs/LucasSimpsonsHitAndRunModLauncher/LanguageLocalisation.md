---
title: "Language Localisation"
description: "This page documents how to localize the Mod Launcher."
authors: [ 2 ]
---

The Mod Launcher supports being localized into other languages using XML files.

# Built-in Language Localisations
At this time, the only language built-in to the Mod Launcher is English.

# Creating Language Localisations
To get started creating a localisation of your own, download the newest template XML from the "Downloads" tab of the language localisation templates project on Mod Bakery:
[Project:181]

Once you have the template file, place it into a "Languages" folder next to the Mod Launcher's executable, rename it accordingly, and then uncomment and edit the `<Translation>` elements within for each string.

Any language strings not included in your XML file will fall back to their English defaults. Certain strings also have other fallbacks for backwards compatibility with older versions of the Mod Launcher.
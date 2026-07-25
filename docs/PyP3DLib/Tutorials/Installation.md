---
title: "Tutorials"
description: "Some basic tutorials for using PyP3DLib."
authors: [ 2 ]
---

This tutorial will help you install PyP3DLib.

> [!danger]
> This package does not currently guarantee a stable API and is not currently versioned.

# Requirements
To use PyP3DLib, you must have:
* Python 3.13+
* [natsort](https://pypi.org/project/natsort/)
	* `pip install natsort`

# Installation
Download the wheel from the [continuous-build](https://github.com/donutteam/py-p3d-lib/releases/latest) tag on GitHub and install it with `pip`:
```
pip install --force-reinstall p3d-X.X.X-py3-none-any.whl
```

# Usage
This library is strongly typed and it is **strongly recommended** to use a language server when working with it to avoid making mistakes, such as [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance) for [Visual Studio Code](https://code.visualstudio.com/download).

For some basic examples of how to use the library, see the following tutorials:
* [[ReadExistingFile.md]]
* [[WriteNewFile.md]]
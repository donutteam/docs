---
title: "String.StringComparison"
description: "Provides information about the StringComparison enumeration available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

The `StringComparison` enumeration defines the types of string comparisons that can be performed.

# Enumeration Values

| Value Name            | Description                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| `InvariantCulture`    | Performs a culture-sensitive comparison using the invariant culture.                            |
| `InvariantIgnoreCase` | Performs a culture-sensitive comparison using the invariant culture, ignoring case differences. |
| `Ordinal`             | Performs a simple byte-by-byte comparison that is case-sensitive.                               |
| `OrdinalIgnoreCase`   | Performs a simple byte-by-byte comparison that ignores case differences.                        |

# Used by
The `StringComparison` enumeration is used by the following functions:

* [[Contains.md]]
* [[EndsWith.md]]
* [[StartsWith.md]]
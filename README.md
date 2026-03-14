# DT Docs
This repository contains Markdown files and other configuration data for Donut Team's documentation website, DT Docs.

## Contributing
These guidelines will probably evolve as time goes on, but for the time being:

* If you notice a typo or have some small amount of info to add to a page or two, feel free to just make a pull request and we'll have a look.
* If you want to make some significant changes to lots of documents, open a [https://github.com/donutteam/docs/discussions](discussion) or message us in [our Discord Server](https://forum.donutteam.com/discord) and we can talk it out first.

Whatever the case, when you update documents, be sure to add your Donut Team user ID to the `authors` in the front matter! This will ensure you are appropriately listed on the docs site for your contributions. If you do not know your ID, then you can [enable Developer Mode](https://donutteam.com/settings/developer) in your DT account settings then do to [your profile](https://donutteam.com/@me) and find it listed under your avatar.

## Document Front Matter
Documents contain YAML front matter declaring various attributes.

The available keys are as follows, with **required keys in bold**:

* **title** (string): The title of the document.
* title_hierarchy (string): The title of the document shown in the hierarchy. Defaults to **title*.
* **description** (string): A brief description of the document.
* authors (number[]): An array of Donut Team User IDs representing the authors of this document.
* initialVersion (object): An object declaring what version of a tool the feature the document covers was added in.
	* **project_id** (number): The ID of the relevant Mod Bakery project.
	* **projectBranch_id** (number): The ID of the relevant branch.
	* **projectBranchVersion_id** (number): The ID of the relevant version.

## Custom Markdown Features
While DT Docs utilizes fairly standard Markdown, there are various custom extensions implemented on top.

### Block Tokens
#### Document Snippets
You can reference a reusable block of Markdown, located within this repo's `snippets` folder, using this syntax:
```
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}
```

#### Tabs
You can add tabs, typically used to show code in multiple languages, using this syntax:
```
{{ tabs }}
{{ tab Tab 1 }}
I'm the first tab!
{{ endtab }}
{{ tab Tab 2 }}
I'm the second tab!
{{ endtab }}
{{ endtabs }}
```

Nested tabs are not supported.

#### Video
You can embed videos from either a direct URL (currently only URLs ending with .mp4 are supported):
```
!![https://donut-team.nyc3.cdn.digitaloceanspaces.com/example.mp4]
```

Or from YouTube:
```
!![https://www.youtube.com/watch/dQw4w9WgXcQ]
```

### Inline Tokens
#### Button Icons
You can insert a few different button glyphs using a button icon token:
```
[ButtonIcon:KeyboardDown]
[ButtonIcon:KeyboardRight]
[ButtonIcon:KeyboardLeft]
[ButtonIcon:KeyboardUp]

[ButtonIcon:XboxA]
[ButtonIcon:XboxB]
[ButtonIcon:XboxX]
[ButtonIcon:XboxY]

[ButtonIcon:PlayStationCross]
[ButtonIcon:PlayStationCircle]
[ButtonIcon:PlayStationSquare]
[ButtonIcon:PlayStationTriangle]

[ButtonIcon:Unknown]
```

This was primarily added for the [document on cheats in The Simpsons: Hit & Run](https://github.com/donutteam/docs/blob/main/docs/TheSimpsonsHitAndRun/Cheats.md).

#### Document Reference
You can reference another document in a manner similar to MediaWiki's internal link syntax:
```
[[LucasRadMusicScriptBuilder/Intro.md]]
```

When referencing a document, the name of the document will be inserted by default. If you want some other text, use a separator bar and specify it:
```
[[LucasRadMusicScriptBuilder/Intro.md|custom link text]]
```

Semicolons are also a supported separator for instances where separator bars cannot be used (such as inside a table):
```
[[LucasRadMusicScriptBuilder/Intro.md;custom link text]]
```

Within documents, paths are relative to the `docs` directory if they start with a `/` and relative to the document if they do not.

Within document snippets, paths must be absolute.

If the document does not exist, this will instead display the text "Invalid Document".

#### Donut Team User Reference
You can reference a Donut Team user by their ID as follows:
```
<@2>
```

Because user references use IDs, they will never break and they will also show the user's preferred name.

If the user is invalid or the user disables/deletes their Donut Team account, this will instead display the text "Deleted User".

#### Mod Bakery Project Reference
You can reference a Mod Bakery project inline as follows:
```
[Project:6]
```

Because project references use IDs, they will never break and they will also show the project's current title.

If the project is not published, this will instead display the text "Invalid Project".

#### Mod Bakery Project Branch Version Reference
You can reference a Mod Bakery project branch version inline as follows:
```
[ProjectBranchVersion:230]
```

Because project branch version references use IDs, they will never break and they will also show the version's version number formatted in the same way as Mod Bakery.

If the project, branch, or version is not published, this will instead display the text "Invalid Project Branch Version".

## License
[MIT](https://github.com/donutteam/docs/blob/main/LICENSE.md)
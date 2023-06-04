# dummy-vscode-snippets README

## Installation

To install the plugin you need to clone the repo and from its root folder run `./.copy_script.sh`.
What the script does is copy the contents of the root folder to the `~/.vscode/extensions/` folder so that `vscode` can detect the plugin.

After installing the plugin you might need to reload or restart vscode to be able to load and use the plugin.

## Features

This plugin provides an example of a snippets vscode plugin setup.

All snippets start with `!` to avoid creating confusion to developers that do not want to use the snippets or when developers are typing
static parts of the configuration.

The plugin provides a snippet for three different configuration types and can be easily extended by adding more similar objects in the `snippets.json` file. One example is the snippet
for the customer.

`!customer` translates into:

```json
{
  "id": "",
  "type": "customer",
  "firstName": "",
  "lastName": "",
  "age": 0,
  "username": "",
  "email": ""
}
```

## Snippet structure

In the `snippet.json` file there are multiple objects each of one is linked to a specific snippet.

The object key is the snippet id, just a simple way for `vscode` to organise the snippets.
In the object we have the following properties:
* `prefix`: The value to be translated to the actual snippet content
* `body`: The content of the snippet
* `description`: A small description to help the user understand what the snippet is injecting

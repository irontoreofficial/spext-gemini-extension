# Spext for Gemini CLI

Spext is a lightweight sharing service for publishing text, sending private notes, and collecting files through simple links. This Gemini CLI extension connects directly to Spext's hosted MCP server—no local server or extra runtime is required.

## Features

- Create shareable text pages.
- Create private secret notes.
- Create upload links for file requests.

## Requirements

- [Gemini CLI](https://github.com/google-gemini/gemini-cli)
- Internet access to the Spext MCP endpoint

## Install

```sh
gemini extensions install https://github.com/irontoreofficial/spext-gemini-extension
```

Restart Gemini CLI after installation. The extension uses [https://spext.fun/api/mcp](https://spext.fun/api/mcp).

## Usage

Ask Gemini naturally, for example:

- `Create a text share with these meeting notes: ...`
- `Create a secret note containing this password: ...`
- `Create a file request for the design assets.`

Gemini may ask for missing content or options before invoking a tool.

## Tools

- `create_text_share` — publishes text and returns a shareable Spext link.
- `create_secret_note` — creates a private note and returns its Spext link.
- `create_file_request` — creates a link others can use to upload requested files.

Gemini CLI may request your approval before executing MCP tools. Review the tool name and inputs, then approve only actions you intend to perform.

## Manage the extension

```sh
gemini extensions update spext-gemini-extension
gemini extensions uninstall spext-gemini-extension
```

## Troubleshooting

- Restart Gemini CLI after installing or updating the extension.
- Run `gemini extensions list` to confirm it is enabled.
- Confirm that `https://spext.fun/api/mcp` is reachable.
- Reinstall the extension if its link or configuration is stale.

Learn more at [spext.fun](https://spext.fun).

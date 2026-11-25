# Ollama

AI Chat PRO integrates Ollama with Roblox Studio through the local AI Chat Bridge. Users run models on their own server.

## Features

Coding assistance, code analysis and agent tasks within the selected model’s capabilities. Image support depends on the model and adapter; the plugin has a 20 MB aggregate image limit.

## Setup

1. Start Ollama and load a compatible model.
2. Start its local API server.
3. Set `http://127.0.0.1:11434/v1` in Modules.
4. Refresh the model list and select a model.

## Security and privacy

The local adapter requires no cloud API key. Use a trusted server; a private address does not guarantee local processing. Bridge does not apply additional content moderation to this adapter. Disable Ollama cloud features; this integration uses the shared local adapter.

See [privacy](../PRIVACY_POLICY_EN.md) and [installation](../INSTALLATION.md).

## Billing

Users bear hardware, electricity and any model licensing costs.

## Provider documentation

[Ollama](https://docs.ollama.com/)

AI Chat PRO is an independent product; compatibility does not imply sponsorship or certification.

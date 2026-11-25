# LM Studio

AI Chat PRO integrates LM Studio with Roblox Studio through the local AI Chat Bridge. Users run models on their own server.

## Features

Coding assistance, code analysis and agent tasks within the selected model’s capabilities. Image support depends on the model and adapter; the plugin has a 20 MB aggregate image limit.

## Setup

1. Start LM Studio and load a compatible model.
2. Start its local API server.
3. Set `http://127.0.0.1:1234/v1` in Modules.
4. Refresh the model list and select a model.

## Security and privacy

The local adapter requires no cloud API key. Use a trusted server; a private address does not guarantee local processing. Bridge does not apply additional content moderation to this adapter.

See [privacy](../PRIVACY_POLICY_EN.md) and [installation](../INSTALLATION.md).

## Billing

Users bear hardware, electricity and any model licensing costs.

## Provider documentation

[LM Studio](https://lmstudio.ai/docs)

AI Chat PRO is an independent product; compatibility does not imply sponsorship or certification.

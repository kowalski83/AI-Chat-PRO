# OpenRouter

AI Chat PRO integrates OpenRouter with Roblox Studio through the local AI Chat Bridge. Requests use the customer’s own API account.

## Features

Coding assistance, code analysis and agent tasks within the selected model’s capabilities. Image support depends on the model and adapter; the plugin has a 20 MB aggregate image limit.

## Setup

1. Launch AI Chat Bridge and open API settings.
2. Select OpenRouter and enter your own API key.
3. Save the key in Bridge. On the first connection only, copy the pairing token into Studio.
4. Select the provider and an available allowlisted model.

API endpoint: `https://openrouter.ai/api/v1`.

## Security and privacy

Bridge protects stored credentials with Windows DPAPI and connects via HTTPS. Secret screening covers selected patterns, not all personal data. Bridge does not apply additional content moderation to this integration. Requests specify `data_collection: deny`, which does not guarantee zero retention.

See [privacy](../PRIVACY_POLICY_EN.md) and [installation](../INSTALLATION.md).

## Billing

Users pay their API provider directly. The plugin purchase does not include AI credits or subscriptions.

## Provider documentation

[OpenRouter](https://openrouter.ai/docs)

AI Chat PRO is an independent product; compatibility does not imply sponsorship or certification.

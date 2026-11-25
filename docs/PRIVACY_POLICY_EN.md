# Privacy policy — AI Chat PRO / Bridge
**Publisher draft; complete before sale.** Version 4.9.35; 24 November 2026.
Publisher: kowalski83. **Complete before publication: legal name, contact address, email and controller details where the publisher processes personal data.** Repository: https://github.com/kowalski83/AI-Chat-PRO.

## Data flow
The plugin communicates with Bridge via 127.0.0.1:8765. No publisher telemetry server is present in the inspected source. When a cloud service is selected, Bridge sends the prompt, history/context, project code fragments and any attachments as applicable to that feature to the selected AI provider. Keys authenticate to the corresponding provider. LM Studio / Ollama uses the configured local or private-network endpoint; its operator controls subsequent processing. CLI, Gemini, Cline Cloud, NVIDIA and Devin are disabled in this Store release. Do not submit secrets, other people's personal data or material you lack permission to share.

## Recipients and purposes
OpenAI API, OpenRouter, GroqCloud and the configured local LM Studio / Ollama endpoint provide AI responses. If an Asset ID is configured, Roblox account and asset IDs are sent to inventory.roblox.com for informational ownership checks. Roblox handles sales and GitHub handles downloads under their own terms and privacy policies. Providers may process data outside the EEA and have their own retention and data-use terms. Review those terms before choosing a model. The publisher should not claim control over those processes.

## Local data, retention and deletion
Keys: %APPDATA%/RobloxStudioAIChatAgent/api_keys.json; Windows current-user DPAPI protection (requires native Windows validation), with migration on read. Environment-variable keys are outside this mechanism. History: Documents/RobloxStudioChatHistory; exports: Documents/RobloxStudioExports unless overridden; backups within history directories. Attachments and jobs may exist in Bridge memory during a session. Local data remains until removed manually or through the relevant features; clearing chat creates a backup and does not delete every copy. Delete stored keys through the Bridge settings window and remove any environment-variable keys. After closing Bridge, manually delete relevant files including backups and exports if desired. Provider-held data must be deleted under the provider's rules.

## Security and rights
Bridge binds only to loopback; Bridge requires a random pairing token in addition to the public header; this is not protection against all same-user processes. Use only on a trusted computer. Do not expose the port to the network. Any data processed by the publisher (e.g. support requests) requires confirmed legal bases, retention, recipients and contact details before publication; applicable rights include access, rectification, erasure, restriction, portability, objection and lodging a complaint with a supervisory authority. This does not limit rights concerning Roblox, GitHub or AI providers. The publisher must confirm actual support practices and complete these details before publication.

## Service availability and age
Only OpenAI API, OpenRouter, GroqCloud and the configured local endpoint (LM Studio or Ollama) are enabled. ChatGPT subscription sign-in is disabled. Gemini, Cline Cloud/CLI, NVIDIA and Devin are disabled, with no CLI opt-in in the Store build. Do not send identifying Roblox user data to AI providers or Roblox user data for training. OpenRouter requests use data_collection: deny; this is not a zero-retention guarantee. The application cannot automatically detect all personal data in arbitrary code or attachments. The 18+ declaration lasts for the Studio session and is passed to the local Bridge; it is not independently verified age and does not collect date of birth or ID documents. 

OpenAI API uses the customer’s own API key, separate API billing and `store: false`; this is not a guarantee of zero retention. ChatGPT subscription sign-in is disabled. Ollama must be configured for local inference only; the operator must disable cloud inference. A local/private IP address alone does not guarantee local processing.

## Worker queue and diagnostic logs
Queued prompts and associated attachments reside in memory during the current Studio session. Running tasks follow the existing history and provider data-flow practices. Bridge stores local diagnostic metadata (time, provider, operation, event, HTTP status, attempt, job identifier and retry delay) in Logs/errors.log under the history directory. This log does not store raw prompts, credentials, code or provider responses. Rotation: 1,000,000 bytes and four backups. Logs are not automatically sent to the publisher; users may manually delete them after closing Bridge.

## History controls

See [history management](HISTORY.md). Image metadata is removed, but visible personal information is not automatically removed.

Local safety reports contain only a category, random ID, timestamp, product and version. They are stored in SafetyReports under the history root, independently of chat history settings. Nothing is automatically sent to the publisher. Delete report files manually.

The pairing token is stored in the Bridge DPAPI store and in local Studio plugin settings (Studio encryption is not guaranteed). It is not an API key. Resetting pairing revokes the previous token. Use a trusted computer.

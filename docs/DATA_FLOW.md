# Data flow and retention
Cloud requests may contain prompts, conversation context, selected project source and image attachments. OpenAI Chat Completions sends store:false; OpenRouter sends data_collection:deny. Neither guarantees zero retention. Groq/OpenRouter host models under their own terms. Local endpoints can be private LAN or loopback and may themselves forward data. Optional informational Roblox ownership lookup sends account and asset IDs to Roblox; it does not prove payment. No source code upload to publisher is implemented in the inspected baseline.

History and backups: Documents/RobloxStudioChatHistory; exports: Documents/RobloxStudioExports (configurable). Clearing history can create a backup, so it is not complete deletion. Jobs and images can remain in process memory. Diagnostic errors.log rotates at 1,000,000 bytes with four backups; metadata only by design. Console/provider error handling needs further redaction review. Delete local files/backups manually after closing Bridge; remote deletion is provider-specific.


Stage 2 screens cloud text for selected secrets and emails before dispatch and completed outputs before return; images are not screened. This is not a comprehensive privacy filter.

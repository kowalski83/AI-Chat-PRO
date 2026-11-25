# Threat model
Assets: API keys, session token, proprietary project code, chat/history, attachments, billing and project integrity. Trust boundaries: Studio plugins, local HTTP, Windows account, provider HTTPS and local inference endpoint.

| Threat | Current mitigation / remaining risk |
|---|---|
| LAN/browser access | Loopback and host/origin checks; no external tunnel |
| Unauthenticated local client | Candidate session token; same-user malware still possible |
| Token/key theft | Memory-only token and DPAPI at rest; clipboard and console visibility remain |
| Malicious AI output | Tool validation and Undo; prompt injection and destructive actions remain possible |
| Data leakage | Provider restrictions; no comprehensive secret/PII scanner yet |
| Unauthorized billing | Customer-owned key, concurrency limit, bounded retries; user/provider budgets needed |
| Malicious binary | Build and SHA256 planned; signing and trusted distribution not verified |
| Age misrepresentation | Self-declaration only; independent age assurance unresolved |

Do not claim formal security assurance. Require independent/native testing before release.

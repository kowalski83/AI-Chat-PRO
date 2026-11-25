# AI Chat PRO / AI Chat FREE — technical review draft
**Documentation for technical review — PRO 4.9.35, Safety stage 3 candidate.** Commercial release is a separate decision; native validation is pending. Publisher: kowalski83. Independent software, not endorsed or certified by OpenAI or Roblox.

PRO 4.9.35 uses customer-owned API credentials and local model endpoints. FREE 4.9.36 is a proposed independent no-charge plugin; subscription access and Codex are not implemented or authorized. A shared free Bridge is planned, but edition-specific access control is not yet implemented. Do not distribute this document as proof of certification.

The technical baseline is the 4.9.35 Worker/Retry/Logs source, with session-token protection, local-console credential management and preliminary text screening. The native Windows EXE, Studio UI, live API and age assurance remain unverified. The existing public EXE may differ from this candidate.

## Review index
- [AGE_SAFETY](docs/AGE_SAFETY.md)
- [API_KEY_SECURITY](docs/API_KEY_SECURITY.md)
- [ARCHITECTURE](docs/ARCHITECTURE.md)
- [BRIDGE_PROTOCOL](docs/BRIDGE_PROTOCOL.md)
- [CONTENT_MODERATION](docs/CONTENT_MODERATION.md)
- [DATA_FLOW](docs/DATA_FLOW.md)
- [FREE_VS_PRO](docs/FREE_VS_PRO.md)
- [INSTALLATION](docs/INSTALLATION.md)
- [KNOWN_LIMITATIONS](docs/KNOWN_LIMITATIONS.md)
- [OPENAI_INTEGRATION](docs/OPENAI_INTEGRATION.md)
- [PRIVACY_POLICY_EN](docs/PRIVACY_POLICY_EN.md)
- [PROVIDER_COMPLIANCE](docs/PROVIDER_COMPLIANCE.md)
- [SIWC_INTEGRATION](docs/SIWC_INTEGRATION.md)
- [THREAT_MODEL](docs/THREAT_MODEL.md)

[Polski README](README_PL.md)

- [Security tests / Testy bezpieczeństwa](docs/SECURITY_TESTS.md)


Security stage 2 regression: 249 passed, 2 skipped. This documentation is suitable for technical consultation; commercial release validation remains separate.


## Stage 3 — current candidate
For OpenAI API text jobs only, Bridge screens input using the existing PrivacyGuard, sends text chunks to OpenAI /v1/moderations with the customer's own API key before generation, and checks completed text after generation before delivering it to Studio. Flagged or unavailable/malformed moderation results stop the job. OpenAI image generation requests with attachments are blocked in this candidate; other providers are unchanged and have no new content moderation. No OpenRouter, Groq or local model text is sent to OpenAI moderation. Moderation is not age assurance, CSAM detection or a guarantee of safety. Chunking may lose context; rejected output may already have incurred generation costs. See https://developers.openai.com/api/docs/guides/moderation.

Local history can be disabled at startup via AI_CHAT_HISTORY_DISABLED=1 or URUCHOM_BEZ_HISTORII.bat; all history HTTP routes are blocked in this mode. It does not erase existing files or prevent in-memory context, exports, diagnostic logs or provider retention. Close all Studio and Bridge instances before running USUN_HISTORIE_CZATU.bat or Bridge --purge-chat-history; type DELETE ALL CHAT HISTORY. This deletes recognized local chat JSON and named chat backups only, not project backups, imported external copies or provider data. It is ordinary filesystem deletion, not secure media erasure. Unrecognized/corrupt files may need manual review. Reporting UI, independent age assurance, comprehensive PII scanning, other-provider and image moderation, native Windows and Studio validation are still pending.

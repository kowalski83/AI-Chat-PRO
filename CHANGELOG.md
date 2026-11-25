# Candidate changes
- 4.9.35 SECURITY stage 1: per-process session token; no raw HTTP request-path logging.
- FREE 4.9.36: planned only.
- Earlier Worker/Retry/Logs functions retained; see private build report.


## 4.9.35 Safety stage 3
## Stage 3 — current candidate
For OpenAI API text jobs only, Bridge screens input using the existing PrivacyGuard, sends text chunks to OpenAI /v1/moderations with the customer's own API key before generation, and checks completed text after generation before delivering it to Studio. Flagged or unavailable/malformed moderation results stop the job. OpenAI image generation requests with attachments are blocked in this candidate; other providers are unchanged and have no new content moderation. No OpenRouter, Groq or local model text is sent to OpenAI moderation. Moderation is not age assurance, CSAM detection or a guarantee of safety. Chunking may lose context; rejected output may already have incurred generation costs. See https://developers.openai.com/api/docs/guides/moderation.

Local history can be disabled at startup via AI_CHAT_HISTORY_DISABLED=1 or URUCHOM_BEZ_HISTORII.bat; all history HTTP routes are blocked in this mode. It does not erase existing files or prevent in-memory context, exports, diagnostic logs or provider retention. Close all Studio and Bridge instances before running USUN_HISTORIE_CZATU.bat or Bridge --purge-chat-history; type DELETE ALL CHAT HISTORY. This deletes recognized local chat JSON and named chat backups only, not project backups, imported external copies or provider data. It is ordinary filesystem deletion, not secure media erasure. Unrecognized/corrupt files may need manual review. Reporting UI, independent age assurance, comprehensive PII scanning, other-provider and image moderation, native Windows and Studio validation are still pending.

# Conversation history

## Disable saving

Before starting Bridge, set `AI_CHAT_HISTORY_DISABLED=1` or use `URUCHOM_BEZ_HISTORII.bat`. This blocks history HTTP operations but does not erase existing files or disable in-memory context, exports, logs or provider retention.

## Delete history

Close all Studio and Bridge instances. Run `USUN_HISTORIE_CZATU.bat` or Bridge with `--purge-chat-history` and type `DELETE ALL CHAT HISTORY`. Recognized JSON chat archives and named chat backups are deleted, not project backups or external exports. This is ordinary file deletion, not secure media erasure. Unrecognized files may require manual removal.

See [privacy policy](PRIVACY_POLICY_EN.md) for provider data practices.

# Local transport — candidate patch
Default 127.0.0.1:8765; configurable QWEN_BRIDGE_PORT. Host and Origin/Fetch Metadata checks restrict typical browser requests. Public GET /health returns minimal metadata; protected routes require the edition header AND a random 256-bit session token. The token is displayed deliberately in an interactive console, pasted into the Studio connection panel, kept in module memory and replaced on Bridge restart. No token is returned by HTTP. /auth/* is not a pairing API. The local HTTP channel is not TLS. Do not tunnel or expose it. The token is not license verification or an OS-level identity check. The same-user process, clipboard, malicious plugin and port impersonation threats remain. Windows UI and terminal behavior require native testing.

Routes include /providers, /models, /jobs, /jobs/{id}, cancellation, /config/api-status, /config/api-key, /config/lm-studio, history, attachments, exports and backup registry. The token protects access, but does not isolate independent Studio windows from one another. /health compatibility metadata is not server authenticity proof.


Stage 2: POST /config/api-key always rejects credential writes (403); /config/api-status remains read-only.

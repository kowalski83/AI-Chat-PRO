# Content moderation

For OpenAI API jobs, Bridge screens input using the PrivacyGuard, sends text chunks to OpenAI /v1/moderations with the customer's own API key before generation, and checks completed text after generation before delivering it to Studio. Flagged or unavailable/malformed moderation results stop the job. OpenAI image attachments are supported with pre-generation moderation; other providers have no equivalent moderation in Bridge. No OpenRouter, Groq or local model text is sent to OpenAI moderation. Moderation is not age assurance, CSAM detection or a guarantee of safety. Chunking may lose context; rejected output may already have incurred generation costs. See https://developers.openai.com/api/docs/guides/moderation.

[Image handling](IMAGE_SAFETY.md) · [Limitations](KNOWN_LIMITATIONS.md)

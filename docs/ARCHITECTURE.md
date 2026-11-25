# Architecture
The Roblox Studio plugin provides the interface, project context and editing operations. The local Bridge connects to selected providers; it is not a publisher-hosted AI relay. Customers pay providers directly for API usage. Worker queues tasks and maintains Undo checkpoints; these are not full project backups.

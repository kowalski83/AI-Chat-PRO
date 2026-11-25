# Automated regression — SECURITY stage 1
249 tests run, 247 passed, 2 skipped, zero failures (Linux, Python unittest; existing mocks and Lua test harnesses). One new HTTP test verifies missing and incorrect tokens, authorized access, public health without token disclosure, unauthorized job submission, browser Origin rejection and token replacement. Test clients were updated to use the corresponding Bridge instance token. Prior reports are historical. Native Windows DPAPI, EXE build, live Roblox Studio UI and real provider calls remain pending. This is not penetration testing or certification.


Stage 2 regression: 251 tests executed, 249 passed, 2 skipped, zero failures (21.917 seconds). Offline Linux tests; no native Windows, live Studio or provider validation. Stage 1 results above are historical.


Stage 3: 256 tests executed; 254 passed, 2 skipped, zero failures (21.989 seconds). Offline Linux regression including mocked OpenAI moderation before/after generation; no live API, native Windows or Studio test.

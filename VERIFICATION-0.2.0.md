# Vagina 0.2.0 — Windows feature-branch verification

02.11.2026: requested rename from vajayjay implemented in host factory, editor,
bundle, package scripts and native test expectations. Technical CMake target
remains VaginaPlugin. Existing releases/history remain intact.

## Executed checks

- Fresh Windows x64 MSVC Release build using the existing pinned VST3 SDK.
- Official VST3 validator: **47 passed, 0 failed**.
- CTest: **4/4 passed** (audio, meter lifecycle, loaded-DLL editor, native renders).
- Processor, analysis, class IDs, parameter IDs and IPC sources unchanged.
- Four real native renders generated; active preview inspected.
- No plugin installation into a user's DAW folder, no physical audio devices.

Windows binary SHA-256: `f450c60f41d7e56f086241126cdba9b13718a658e7f25612c7265e973803a924`.

## Limits

No current DAW session, Linux/macOS build, AU/CLAP implementation, signing or
notarization pass is claimed. Filename-based host caches may require relinking;
stable class IDs alone do not establish every host's old-project compatibility.
Do not leave both old/new bundles in a scanned plugin directory.

Packaging scripts target the new name. Historical verification documents remain
version-specific. No new public release is created by these checks.

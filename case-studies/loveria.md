# Loveria
Native Android companion application · 0.3 beta.

## The problem
A small local model must maintain a character's identity while preserving useful details from earlier conversations. The application needs to own persistence, context selection, downloads and failure behavior.

## Implemented in the beta
- Nine original characters with individual visual themes and fixed backstories.
- Native Kotlin Android UI, onboarding, saved drafts, earlier-message pagination and local SQLite history.
- Lexical retrieval and selected source quotations for durable memories.
- Bounded recent-turn and memory context rather than loading the entire history.
- Model-independent persona checks with one repair attempt and narrow canonical fallbacks for closed biography/time questions.
- Direct model downloads with progress, pause/resume, byte-range validation and SHA-256 verification.

<img src="../assets/loveria-characters.png" alt="Actual Loveria beta character discovery screenshot using the fictional Alex demo profile." width="340">

## Recorded validation
The project's 0.3 validation report records **53 JVM tests** and **18 Android database/UI checks** passing on an API 36 ARM64 emulator. It also records an LFM native conversation and recall example, lint with zero errors and remaining warnings, and APK packaging checks. These are historical project results, not suites rerun for this portfolio.

## Limits that shaped the implementation
One pinned MiniCPM5-1B export failed native context-capacity checks with the richer prompts, so its download and activation were disabled in this beta. LFM completed the documented native cases. Other model/device combinations require further testing.

Memory uses SQLite lexical retrieval, not multilingual vector embeddings. Photos remain local and text models read captions. General semantic factuality, physical-device RAM/thermal behavior, Play Billing and release work remain open. No production release or paid downloads are claimed.

## Relevant client work
Native Android chat flows; persistent per-character or per-workspace state; source-grounded memory selection; robust model installation; and explicit handling of unsupported model configurations.

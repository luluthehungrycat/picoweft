# PicoWeft roadmap

All milestones below are planned. Mark a gate complete only with the build, test or measurement that demonstrates it. [SPEC.md](SPEC.md) defines the acceptance criteria and ordering.

| Milestone | Deliverable | Exit evidence |
| --- | --- | --- |
| 0. Portable core probe | Small Rust workspace, deterministic fake adapter, Linux CLI fixture, Kotlin/JNI integration probe | Same core builds for Linux and Android ARM64; events, validated host tool result, cancel, cleanup and restart tested. Record any evidence that warrants the Kotlin/JVM fallback. |
| 1. Offline Android proof | Minimal GUI, pinned bundled llama.cpp CPU, a local GGUF fixture, one bounded app-owned read tool | Real phone completes a model → tool → model task offline. Show persisted state, cancellation, rejection of truncated calls and the matching Linux contract test. |
| 2. Remote and Linux proof | One supported streaming remote/custom profile, basic Linux CLI, local CPU path | Same loop completes an explicitly authorized real remote tool turn; offline Linux execution checked, with arm64 and x86-64 build and runtime status documented. |
| 3. MVP packaging | Curated in-app model downloads, session/profile UX, reproducible build instructions, documented hardware and provider support | Verify download integrity, interruption, cancellation, disk-full handling, privacy and basic Android/Linux workflows on supported targets. |
| 4. Broader autonomy | More scoped tools, reproducible multi-step fixtures, context improvements grounded in failure data | Compare successful tasks, false actions, tokens, elapsed time, memory and thermals on fixed tasks against the simple loop. Track failure modes and device-specific limits. |

Run inexpensive Linux small-model experiments early so poor tool selection or template behavior is visible before investing heavily in Android polish. Keep the fake model tests separate from real-model and real-device evidence. Resolve an unavailable test target by recording the missing evidence and continuing with independent work.

After the MVP, consider vision and projector support, more remote provider protocols, selected skill import, measurable improvements to context or routing, and GPU/NPU backends on hardware that can actually be tested. Use the same core on additional hosts only when there is a concrete deployment need.

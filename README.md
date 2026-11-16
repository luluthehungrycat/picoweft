# PicoWeft

PicoWeft is a lightweight, local-first autonomous agent harness for small language models on resource-constrained devices.

It is designed to let a model carry out a task over several tool turns, preserve task state if interrupted, and work within the device's context, memory and compute limits. Android is the first target, with a self-contained app that runs the agent loop and CPU inference on the phone. Linux follows with a CLI built around the same portable core. Optional remote profiles extend the model choices when users choose to send task context off-device.

## Status

PicoWeft is at the specification stage. The first milestone is an offline tool round trip on a real Android device, alongside a shared-core Linux test fixture. Build and usage instructions will land with usable implementation.

## Project direction

- [SPEC.md](SPEC.md) describes the product, architecture and acceptance criteria.
- [ROADMAP.md](ROADMAP.md) tracks milestones and verification gates.
- [AGENTS.md](AGENTS.md) describes how to work in the repository.

The name combines *pico*, something small, and *weft*, the threads woven across a fabric. PicoWeft carries forward lessons from [Edgmes Agent](https://github.com/luluthehungrycat/edgmes-agent), with [Pi](https://github.com/earendil-works/pi), [Hermes Agent](https://github.com/NousResearch/hermes-agent), and [llama.cpp](https://github.com/ggml-org/llama.cpp) as architectural or inference references.

PicoWeft is licensed under the [MIT License](LICENSE). Third-party code, dependencies and model artifacts retain their own terms.

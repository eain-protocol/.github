# EAIN — Embedded AI Interchange Notation

**Human-readable for developers. Deterministic for devices. Semantic for AI.**

EAIN is an open-source initiative exploring an **embedded-first, AI-native data interchange notation and protocol**. Its goal is to make data exchanged among microcontrollers, edge devices, distributed systems, and AI applications both efficient to process and meaningful to interpret.

EAIN is being designed as more than a serialization library: a **language-independent specification** combining a human-readable notation, a compact deterministic binary representation, and schema-driven semantic contracts.

> **Project status:** Early design and research. The features below describe the intended direction; they are not yet implemented or standardized. Syntax, wire encoding, and compatibility guarantees will be defined through public specifications and validated with working implementations.

## What we're building

| Layer | Purpose |
| --- | --- |
| **Readable notation** | A clear, constrained text representation for people, tools, and debugging. |
| **Binary interchange** | Compact, deterministic encoding designed for bounded memory, streaming, and constrained devices. |
| **Typed schemas** | Explicit types, field identities, physical units, ranges, compatibility, and schema evolution. |
| **Semantic device contracts** | Machine-understandable descriptions of observations, capabilities, and controls for AI and distributed systems. |

### Engineering priorities

- **Embedded first:** predictable resource usage, bounded parsing, and Rust `no_std` support, targeting `no_alloc` in the constrained runtime.
- **Interoperability by design:** one normative, language-independent specification; independent Rust, C/C++, and other implementations.
- **Safe AI integration:** semantic discovery does **not** grant device control. Explicit authorization, deterministic validation, and safety boundaries are required before actuation.
- **Specification before implementation:** published design decisions, conformance cases, and golden test vectors define correct behavior.
- **Evidence over claims:** reproducible measurements and real hardware tests, including results where EAIN does not outperform established formats.

## Engineering and research

Our planned validation spans microcontrollers, Raspberry Pi, ARM/x86 systems, and CPU-hosted local language models. We intend to measure payload size, encode/decode latency, memory and stack use, code size, compatibility, and failure handling, with relevant comparisons against JSON, CBOR, MessagePack, Postcard, and Protocol Buffers.

The project follows an evidence-driven workflow:

**Hypothesis → RFC / architecture decision → implementation → tests → measurements → publication**

## Repositories

The ecosystem will be developed in independent repositories as each workstream begins:

| Repository | Scope |
| --- | --- |
| `spec` | Versioned language, schema, binary protocol, semantic and security specifications; RFCs and conformance vectors. |
| `rust` | First reference implementation and modular Rust crates. |
| `lab` | Reproducible benchmarks, hardware experiments, configurations, and raw results. |
| `c`, `python`, `examples` | Future independent implementations, integrations, and working examples. |

Repositories will appear under [github.com/eain-protocol](https://github.com/eain-protocol) as they are established. **The published specification—not any implementation—will define the protocol.**

## Open development

We aim to develop EAIN in public with reviewable design proposals, explicit trade-offs, tests, and versioned releases. Contributions and feedback will become available through the relevant repositories as their contribution and governance processes are published.

EAIN is **not currently an IETF RFC or IEEE standard**. Formal standardization may be explored when the specification, implementations, and community reach an appropriate level of maturity.

---

**EAIN** · Open-source protocol engineering for embedded, edge, and AI-native systems.

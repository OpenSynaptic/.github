# OpenSynaptic Organization

[![Docs](https://img.shields.io/badge/Official%20Docs-opensynaptic.github.io-2563EB?style=for-the-badge)](https://opensynaptic.github.io/)
[![Core](https://img.shields.io/badge/Core-OpenSynaptic-2E8B57?style=for-the-badge)](https://github.com/OpenSynaptic/OpenSynaptic)
[![Embedded](https://img.shields.io/badge/Embedded-OSynaptic--FX-6A5ACD?style=for-the-badge)](https://github.com/OpenSynaptic/OSynaptic-FX)

A modern protocol and runtime ecosystem for IoT data standardization, compression, transport abstraction, and embedded delivery.

一个面向物联网的现代协议与运行时生态，覆盖数据标准化、压缩、传输抽象与嵌入式落地。

## At A Glance

- Official documentation: https://opensynaptic.github.io/
- Primary stack: `OpenSynaptic` (Python + optional Rust core)
- Embedded stack: `OSynaptic-FX` (C99, embedded-first)
- Focus: unified data pipeline from sensor input to multi-transport output

## Project Matrix

| Project | Positioning | Tech | Best For | Quick Link |
|---|---|---|---|---|
| `OpenSynaptic` | High-performance IoT protocol stack with plugin-based services | Python, optional Rust core, multi-transport | Gateway apps, edge nodes, rapid integration | [Repository](https://github.com/OpenSynaptic/OpenSynaptic) |
| `OSynaptic-FX` | Embedded-first C99 runtime and protocol workspace | C99, CMake, spec-driven architecture | MCU/SBC firmware, low-level runtime control | [Repository](https://github.com/OpenSynaptic/OSynaptic-FX) |

## Architecture Vision

```text
Sensors -> Standardization (UCUM) -> Compression (Base62) -> Fusion (FULL/DIFF) -> Transport (TCP/UDP/UART/LoRa/MQTT/CAN)
```

The ecosystem keeps one consistent protocol mindset across cloud-edge and embedded targets.

## Quick Start Paths

### 1) Cloud/Edge Path (`OpenSynaptic`)

- Start with docs: https://opensynaptic.github.io/
- Then open repository setup: https://github.com/OpenSynaptic/OpenSynaptic

### 2) Embedded Path (`OSynaptic-FX`)

- Start with docs: https://opensynaptic.github.io/
- Then open repository setup: https://github.com/OpenSynaptic/OSynaptic-FX

## Why This Organization

- Unified data semantics for heterogeneous sensors
- Compression-oriented packet flow for constrained networks
- Multi-transport delivery with a consistent developer experience
- Spec-driven implementation across Python/Rust/C99 tracks

## Documentation

- Official docs portal: https://opensynaptic.github.io/
- OpenSynaptic repository docs and wiki:
  - https://github.com/OpenSynaptic/OpenSynaptic
- OSynaptic-FX repository docs:
  - https://github.com/OpenSynaptic/OSynaptic-FX

## Contributing

We welcome issues, proposals, and pull requests.

- Read each repository's `CONTRIBUTING.md`
- Open design or bug discussions in the matching project repository
- Keep protocol/spec changes synchronized with documentation

## Contact and Community

- Organization: https://github.com/OpenSynaptic
- Documentation hub: https://opensynaptic.github.io/

---

If you are new here, start from the docs portal, choose your path (cloud-edge or embedded), and follow the first-run guide in the matching repository.


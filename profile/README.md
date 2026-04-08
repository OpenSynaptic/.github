# OpenSynaptic Organization

[![Docs](https://img.shields.io/badge/Official%20Docs-opensynaptic.github.io-2563EB?style=for-the-badge)](https://opensynaptic.github.io/)
[![Core](https://img.shields.io/badge/Core-OpenSynaptic-2E8B57?style=for-the-badge)](https://github.com/OpenSynaptic/OpenSynaptic)
[![Embedded](https://img.shields.io/badge/Embedded-OSynaptic--FX-6A5ACD?style=for-the-badge)](https://github.com/OpenSynaptic/OSynaptic-FX)
[![Frontend](https://img.shields.io/badge/Frontend-Gsyn-E05D44?style=for-the-badge)](https://github.com/OpenSynaptic/Gsyn)

A modern protocol and runtime ecosystem for IoT data standardization, compression, transport abstraction, embedded delivery, and real-time data visualization.

一个面向物联网的现代协议与运行时生态，覆盖数据标准化、压缩、传输抽象、嵌入式落地与实时数据可视化。

## At A Glance

- Official documentation: https://opensynaptic.github.io/
- Protocol core: `OpenSynaptic` (Python + optional Rust core)
- Embedded transmitter: `OSynaptic-TX` (C99, MCU-first encode/send)
- Embedded receiver: `OSynaptic-RX` (C99, MCU-first decode/verify)
- Full MCU runtime: `OSynaptic-FX` (C99, all-in-one embedded workspace)
- Frontend dashboard: `Gsyn` (Flutter, web + Android data visualization)
- Focus: end-to-end pipeline from raw sensor to visual dashboard

## Project Matrix

| Project | Positioning | Tech | Best For | Quick Link |
|---|---|---|---|---|
| `OpenSynaptic` | High-performance IoT protocol stack with plugin-based services | Python, optional Rust core, multi-transport | Gateway apps, edge nodes, rapid integration | [Repository](https://github.com/OpenSynaptic/OpenSynaptic) |
| `OSynaptic-TX` | Lightweight C99 transmitter library — encodes, compresses and packs sensor data for wire delivery | C99, no-heap, MCU-first | Sensor nodes, constrained transmitters | [Repository](https://github.com/OpenSynaptic/OSynaptic-TX) |
| `OSynaptic-RX` | Lightweight C99 receiver library — decodes, verifies and extracts sensor data from wire frames | C99, streaming parser, CRC-verified | Gateway receivers, embedded decoders | [Repository](https://github.com/OpenSynaptic/OSynaptic-RX) |
| `OSynaptic-FX` | Embedded-first C99 all-in-one runtime and protocol workspace (TX + RX + runtime + plugins) | C99, CMake, spec-driven architecture | MCU/SBC firmware, low-level runtime control | [Repository](https://github.com/OpenSynaptic/OSynaptic-FX) |
| `Gsyn` | Cross-platform frontend dashboard for real-time IoT data visualization | Flutter (Dart), web + Android | Visual monitoring, live dashboards, end-user apps | [Repository](https://github.com/OpenSynaptic/Gsyn) |

## Architecture Vision

```text
[Sensor Node]
     │  OSynaptic-TX   (encode → Base62 compress → pack → CRC)
     │  OSynaptic-FX   (full MCU runtime alternative)
     ▼
  Wire Transport  (UART / UDP / LoRa / MQTT / CAN / TCP)
     │
     │  OSynaptic-RX   (CRC verify → decode → extract)
     ▼
[OpenSynaptic]   (protocol engine · UCUM standardization · plugin services · Rust RSCore)
     │
     ▼
[Gsyn Dashboard] (Flutter web + Android · real-time charts · live sensor feeds)
```

One consistent protocol contract flows from raw sensor bytes to interactive visual dashboards, across embedded and cloud-edge targets.

## Quick Start Paths

### 1) Cloud / Edge Path (`OpenSynaptic`)

- Start with docs: https://opensynaptic.github.io/
- Then open repository setup: https://github.com/OpenSynaptic/OpenSynaptic

### 2) Embedded Transmitter Path (`OSynaptic-TX`)

- Start with docs: https://opensynaptic.github.io/
- Then open repository: https://github.com/OpenSynaptic/OSynaptic-TX

### 3) Embedded Receiver Path (`OSynaptic-RX`)

- Start with docs: https://opensynaptic.github.io/
- Then open repository: https://github.com/OpenSynaptic/OSynaptic-RX

### 4) Full MCU Runtime Path (`OSynaptic-FX`)

- Start with docs: https://opensynaptic.github.io/
- Then open repository setup: https://github.com/OpenSynaptic/OSynaptic-FX

### 5) Frontend Dashboard Path (`Gsyn`)

- Start with repository: https://github.com/OpenSynaptic/Gsyn
- Connects to `OpenSynaptic` backend for live sensor data feeds
- Targets web browsers and Android devices via Flutter

## Why This Organization

- Unified data semantics for heterogeneous sensors (UCUM-based standardization)
- Compression-oriented packet flow for constrained networks (Base62 + Fusion diff)
- Multi-transport delivery with a consistent developer experience
- Spec-driven implementation across Python / Rust / C99 / Flutter tracks
- Full-stack coverage: from bare-metal MCU encoding to visual end-user dashboards

## Documentation

- Official docs portal: https://opensynaptic.github.io/
- OpenSynaptic repository docs and wiki:
  - https://github.com/OpenSynaptic/OpenSynaptic
- OSynaptic-TX repository docs:
  - https://github.com/OpenSynaptic/OSynaptic-TX
- OSynaptic-RX repository docs:
  - https://github.com/OpenSynaptic/OSynaptic-RX
- OSynaptic-FX repository docs:
  - https://github.com/OpenSynaptic/OSynaptic-FX
- Gsyn repository:
  - https://github.com/OpenSynaptic/Gsyn

## Contributing

We welcome issues, proposals, and pull requests.

- Read each repository's `CONTRIBUTING.md`
- Open design or bug discussions in the matching project repository
- Keep protocol/spec changes synchronized with documentation

## Contact and Community

- Organization: https://github.com/OpenSynaptic
- Documentation hub: https://opensynaptic.github.io/

---

If you are new here, start from the docs portal, choose your path (sensor node, gateway, or dashboard), and follow the first-run guide in the matching repository.


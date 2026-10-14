<p align="center">
  <img src="https://img.shields.io/badge/ALICEHUB-Centralized%20Hub-00ccaa?style=for-the-badge&labelColor=07060f" alt="ALICEHUB" />
  <img src="https://img.shields.io/badge/V0-Active-5fd38d?style=for-the-badge&labelColor=07060f" alt="V0" />
  <img src="https://img.shields.io/badge/Hub-Master%20Controller-8f6cf0?style=for-the-badge&labelColor=07060f" alt="Hub" />
</p>

<h1 align="center">ALICEHUB</h1>
<p align="center"><b>Centralized ALICE + Tools Hub — connects all V0 components</b></p>

<p align="center">
  <code>ANTI-NETRUNNER</code> — Source integrity hashing prevents automated AI scraping and unauthorized code replication. Full source available on request with identity verification.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12-3776ab?style=flat-square&logo=python&logoColor=white&labelColor=07060f" />
  <img src="https://img.shields.io/badge/React-TSX-61dafb?style=flat-square&logo=react&logoColor=white&labelColor=07060f" />
  <img src="https://img.shields.io/badge/aiohttp-Server-2496ED?style=flat-square&labelColor=07060f" />
  <img src="https://img.shields.io/badge/CDT%2FCPT%2FTKN-Ledger-f2c14e?style=flat-square&labelColor=07060f" />
  <img src="https://img.shields.io/badge/License-MIT-c0caf5?style=flat-square&labelColor=07060f" />
</p>

---

## What is ALICEHUB?

The master controller that connects and coordinates all V0 components into a unified stack:

- **Hub-to-Hub Mesh** — register, discover and relay between hub instances
- **Node Management** — track connected nodes with heartbeat monitoring
- **CDT/CPT/TKN Ledger** — internal token economy for agent delegation
- **Service Aggregator** — proxy health checks across all running services
- **Task Dispatch** — route tasks to the best available node
- **Module Registry** — centralized index of all connected modules

## Architecture

```
                    ┌─────────────────────┐
                    │     ALICEHUB        │
                    │   Master Controller │
                    │      :7790          │
                    └──────────┬──────────┘
                               │
         ┌─────────────────────┼─────────────────────┐
         │                     │                     │
┌────────▼────────┐  ┌────────▼────────┐  ┌─────────▼─────────┐
│  ALICE-MASTER   │  │  ALICE-GENERAL  │  │  TRUE-ALICE       │
│     :7780       │  │     :7781       │  │     :7782         │
└────────┬────────┘  └────────┬────────┘  └─────────┬─────────┘
         │                     │                     │
         └─────────────────────┼─────────────────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
    ┌────────▼──────┐  ┌──────▼──────┐  ┌───────▼───────┐
    │  THESEED L0   │  │    TOA      │  │  MCP Server   │
    │  Anvil :8545  │  │   :7784     │  │  36 tools     │
    └───────────────┘  └─────────────┘  └───────────────┘
```

## API

| Endpoint | Method | Description |
|---|---|---|
| `/health` | GET | Health check |
| `/status` | GET | Full hub status with all nodes |
| `/api/hub/register` | POST | Register a hub or service |
| `/api/hub/modules` | GET | List all connected modules |
| `/api/hub/task` | POST | Submit task for dispatch |
| `/api/hub/nodes` | GET | Node mesh status |
| `/api/cdt/ledger` | GET | CDT/CPT/TKN balances |
| `/api/cdt/supply` | GET | Token supply stats |
| `/api/cdt/transfer` | POST | Transfer tokens |
| `/api/services/health` | GET | Aggregated service health |

## Token Economy

| Token | Purpose | Genesis Supply |
|---|---|---|
| **CDT** | Contribution Delegation Token — earned by contributing | 1M |
| **CPT** | Compute Power Token — earned by providing compute | 500K |
| **TKN** | Generic delegation token — task rewards | 1M |

## Related

<p align="center">
  <a href="https://github.com/VZero911/A.L.I.C.E"><img src="https://img.shields.io/badge/A.L.I.C.E-AI%20Framework-00ffcc?style=for-the-badge&logo=github&labelColor=07060f" alt="ALICE" /></a>
  <a href="https://github.com/VZero911/THESEED"><img src="https://img.shields.io/badge/THESEED-Blockchain%20%2F%20Data-f2c14e?style=for-the-badge&logo=github&labelColor=07060f" alt="THESEED" /></a>
  <a href="https://github.com/VZero911/MCP"><img src="https://img.shields.io/badge/MCP-Server-8f6cf0?style=for-the-badge&logo=github&labelColor=07060f" alt="MCP" /></a>
  <a href="https://github.com/VZero911/AGENTS"><img src="https://img.shields.io/badge/AGENTS-Public%20Nodes-5fd38d?style=for-the-badge&logo=github&labelColor=07060f" alt="AGENTS" /></a>
</p>

---

<p align="center"><i>Design By V0</i></p>

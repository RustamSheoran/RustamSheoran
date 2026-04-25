# Hi, I'm Rustam Sheoran 👋

**Systems Engineer · Solana Developer · Competitive Programmer**

Started building seriously at 10. Eight years of consistent GitHub contributions. Currently 18, gap year before university — spending it going deep rather than wide.

I build systems from the ground up — operating systems, shells, distributed infrastructure, and Solana programs. Not as exercises. As the actual thing.

---

## 🔭 What I'm Working On

- **Jepsen-inspired distributed systems testing framework** — fault injection (network partitions, crashes, latency), linearizability validation, adversarial workload simulation *(private)*
- **Rust Password Manager** — security-focused vault with Argon2id, ChaCha20Poly1305, secret-aware memory, CLI + TUI
- **SolScope React Native** — rewrite of my Solana wallet intelligence platform

---

## 🏆 Competitive Programming

**CodeChef**
- ⭐ 6★ · **2239 rating** · Division 1
- 🌍 Global Rank: **301** · 🇮🇳 Country Rank: **121**
- 📈 [codechef.com/users/ginge](https://www.codechef.com/users/ginge)

---

## 🚀 Featured Projects

### 🖥️ [OS-C](https://github.com/RustamSheoran/OS-C)
Freestanding x86_64 operating system kernel written in C and Assembly.

```
UEFI Firmware
     │
     ▼
Bootloader (kernel.efi)
     │
     ▼
Memory Init ──► PMM ──► Paging (PML4)
     │
     ▼
CPU Setup ──► GDT / IDT ──► Interrupts (PIC/PIT)
     │
     ▼
Syscall Interface (syscall/sysret)
     │
     ▼
Kernel Space (Higher Half)
     │
     ▼
Interactive Shell (Serial I/O)
```

- Full physical memory manager + virtual paging (PML4), higher-half kernel
- CPU initialization — GDT/IDT, interrupt handling, timer configuration
- Syscall interface bridging user ↔ kernel space
- UEFI-based boot with zero libc or runtime dependencies

**Stack:** C · x86_64 Assembly · UEFI

---

### 🖥️ [Shell-C++](https://github.com/RustamSheoran/Shell-C-plusplus)
Modern C++20 Unix-like shell with AST-based execution engine.

```
Input
  │
  ▼
Lexer → Parser (AST) → Execution Engine
                              │
                              ▼
                   Processes / Syscalls
                              │
                              ▼
                 Pipes / Redirection / Signals
```

- AST-based parsing with operator precedence
- Pipelines and I/O redirection via file descriptors
- Job control — fg/bg, signals, process groups
- Interactive shell with history, completion, and editing

**Stack:** C++20 · POSIX · Unix syscalls

---

### 🔐 [Rust Password Manager](https://github.com/RustamSheoran/Rust-Password-Manager)
Security-focused password vault with a CLI and terminal UI.

- **Crypto:** Argon2id for key derivation → ChaCha20Poly1305 for authenticated encryption
- **Memory:** `secrecy::SecretString` and zeroize-based cleanup for all sensitive in-memory data
- **Storage:** encrypted vault — no plaintext site names, usernames, or passwords on disk
- **TUI:** fuzzy search, auto-hide on focus switch, clipboard auto-clear after 15 seconds, auto-lock on inactivity
- **Tests:** crypto round-trips, wrong-password rejection, plaintext regression checks, Unix permission enforcement

**Stack:** Rust · Argon2id · ChaCha20Poly1305 · ratatui · crossterm

---

### 🔭 [SolScope Android](https://github.com/RustamSheoran/solscope-android)
Solana wallet intelligence platform — analyzes on-chain activity and generates algorithmic risk scores.

- Custom JSON-RPC 2.0 client built from scratch — no heavy SDKs, direct Solana Mainnet communication
- Weighted heuristic risk engine: account age, balance patterns, transaction history, asset diversity → 0–100 safety score
- Clean Architecture + MVVM, Kotlin Coroutines and Flow throughout
- Custom Glassmorphic design system in Jetpack Compose

Deprecated Android codebase — full React Native rewrite in progress.

**Stack:** Kotlin · Jetpack Compose · OkHttp · Kotlinx Serialization · Solana JSON-RPC

---

### 🧪 Distributed Systems Testing Framework *(Private)*
Jepsen-inspired framework for validating correctness under adversarial conditions.

```
Client Workload
       │
       ▼
Distributed Cluster
       │
       ▼
Fault Injection Layer
(network partitions · crashes · latency injection)
       │
       ▼
Observability + Logs
       │
       ▼
Consistency Verification
(linearizability · eventual consistency)
```

- Fault injection — network partitions, process crashes, latency injection
- Linearizability validation under adversarial workloads
- Distributed workload simulation across multiple nodes

---

### 🎨 [ASCII-CAM](https://github.com/RustamSheoran/ASCII-CAM)
Real-time browser camera feed converted to ASCII art via Canvas API.

- Live camera → ASCII conversion with adjustable resolution and character sets
- 60+ FPS rendering with performance tracking
- Image and video export

**Stack:** TypeScript · React · Canvas API

---

## 🧰 What I Work With

**Systems & Low-Level**
`C` `C++20` `x86_64 Assembly` `Rust` `POSIX` `Linux`

**Solana / Web3**
`Rust` `Anchor` `Solana JSON-RPC` `PDAs` `SPL Tokens` `DeFi primitives`

**Backend & Infra**
`Node.js` `TypeScript` `Docker` `Kubernetes` `Terraform` `CI/CD` `Kafka` `PostgreSQL`

**AI / ML**
`PyTorch` `Transformers` `RAG` `Agents` `Fine-tuning` *(IIT Indore — Diploma in AI & Data Science)*

**Mobile**
`Kotlin` `Jetpack Compose` `React Native`

---

## 📚 How I Learn

I design structured curricula across domains — web/backend internals, DevOps infrastructure (containers through Firecracker sandboxing), Solana/Web3, and AI systems — and implement as I go. Not passive consumption.

Current deep focus: Solana ecosystem (programs, DeFi mechanics, infrastructure) and Rust systems programming.

Upcoming: contributing to [Omarchy](https://github.com/basecamp/omarchy) — systems/Linux tooling.

---

## 📊 Activity

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=RustamSheoran&show_icons=true&theme=dark&hide_border=true&count_private=true)

Eight years of consistent contributions — 2018 through today.

---

## 📫 Reach Me

- 📧 [rustam98137@gmail.com](mailto:rustam98137@gmail.com)
- 💼 [linkedin.com/in/rustamsheoran](https://linkedin.com/in/rustamsheoran)
- 🏆 [CodeChef](https://www.codechef.com/users/ginge)
- 💻 [github.com/RustamSheoran](https://github.com/RustamSheoran)

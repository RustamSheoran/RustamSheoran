# Hi, I'm Rustam Sheoran 👋

**Systems Engineer · C/C++ · Rust · Linux · Competitive Programmer**

I build systems from the ground up, with a focus on systems programming, Linux internals, computer architecture, and performance engineering.

---

## 🚀 Systems Projects

### [Helios](https://github.com/RustamSheoran/Helios)
Systems monorepo in low-level Rust implementing Linux container isolation, an interactive Unix shell, and a custom global heap allocator.

```
Helios-Shell (AST / Job Control)
  └─► Helios-Container (Namespaces / cgroups v2 / Seccomp BPF)
        └─► Helios-Allocator (Best-Fit Free List & Slab Caches)
              └─► Linux Kernel (clone, pivot_root, mmap/munmap)
```

- **Container Isolation:** UTS, Mount, IPC, PID, and Network namespace unsharing, private mount propagation, `pivot_root` jail, cgroups v2 resource limits, and Seccomp BPF filters
- **Process Supervision:** Synchronizes child execution across namespace switches using synchronizing `O_CLOEXEC` pipes
- **Interactive Shell:** REPL featuring recursive AST pipelines, I/O redirection, background job control tables, process groups (`setpgid`), and terminal handovers (`tcsetpgrp`)
- **Custom Heap Allocator:** `GlobalAlloc` managing page-backed memory via intrusive doubly-linked Best-Fit free lists with physical coalescing and fixed-slot Slab caches over `mmap`/`munmap`

**Stack:** `Rust` · `Linux Namespaces` · `cgroups v2` · `Seccomp BPF` · `Virtual Memory`

---

### [RESP-CPP](https://github.com/RustamSheoran/RESP-CPP)
High-performance, single-threaded, event-driven Redis-compatible key-value store written in C++17.

- **Event Reactor Core:** Leverages Linux `epoll` (`epoll_create1`, `epoll_ctl`, `epoll_wait`) to service thousands of concurrent client connections with 0% idle CPU overhead
- **Zero-Copy Parser:** Tokenizes strict RESP streams using `std::string_view` slices directly from client buffers without intermediate heap allocations
- **Socket & Network Tuning:** Disables Nagle's algorithm (`TCP_NODELAY`), handles non-blocking socket states (`O_NONBLOCK`), and masks `SIGPIPE`
- **Dynamic Backpressure:** Automatically registers `EPOLLOUT` on partial socket flushes and deregisters once drained to eliminate busy-spinning

**Stack:** `C++17` · `Linux epoll` · `POSIX Sockets` · `RESP Protocol`

---

### [DWDP](https://github.com/RustamSheoran/DWDP-Triton-MoE-Inference-Engine)
Distributed Weight Data Parallelism Mixture-of-Experts (MoE) high-throughput inference engine.

- **Fused Triton Grouped-GEMM:** Single-launch MoE kernel fusing token gather, SwiGLU activation, and down-projection, cutting kernel launches from 24+ down to 1 per layer
- **Native FP8 Precision:** Full FP8 (E4M3 / E5M2) execution with fine-grained per-expert micro-scaling and FP32 Tensor Core accumulation
- **CUDA Graph Replay:** Captures static GPU execution topologies to replay token decode passes with zero CPU call overhead (0 ms CPU tax)
- **PagedAttention Memory Manager:** Eliminates VRAM fragmentation via fixed physical KV-cache page allocation (`block_size=16`) and automated precision fallbacks

**Stack:** `Triton` · `CUDA` · `Python` · `C++20` · `FP8` · `PagedAttention`

---

### [simd](https://github.com/RustamSheoran/simd)
Hand-written AArch64 NEON SIMD dot product benchmarked against `-O3` vectorizing compilers.

- **Hand-Optimized Assembly:** Written directly in AArch64 ELF assembly (`neon_dot.s`) to strictly control register allocation, widening loads, and accumulator dependencies
- **Loop Unrolling & Widening:** Unrolls main loop across 32 elements using 8 independent two-lane 64-bit accumulators (`smlal`/`smlal2`) to maximize pipeline throughput
- **Tail Path Handling:** Reduces accumulators into scalar results and processes non-aligned array tails using `smaddl` on 1,000,003-element arrays
- **Toolchain & Verification:** Cross-compiled for Linux AArch64 and verified via QEMU user mode with remote GDB inspection of vector registers (`v0` to `v19`)

**Stack:** `AArch64 Assembly` · `ARM NEON` · `C++` · `QEMU` · `GDB`

---

## 🏆 Competitive Programming

- **Codeforces:** Expert · Peak Rating 1675 · [adarak](https://codeforces.com/profile/adarak)
- **LeetCode:** Knight · Rating 1953 (Top 3.4%) · 512+ Solved (127 Hard) · [RustamSheoran](https://leetcode.com/u/RustamSheoran/)

---

## 🧰 Technical Arsenal

- **Systems & Kernels:** `Linux Namespaces` · `cgroups v2` · `Seccomp BPF` · `POSIX` · `x86_64 / AArch64 Assembly`
- **Languages:** `C` · `C++17/20` · `Rust` · `Python`
- **Performance & GPU:** `CUDA` · `OpenAI Triton` · `ARM NEON` · `SIMD` · `FP8` · `CUDA Graphs`
- **Infrastructure & Tooling:** `Linux / epoll` · `Docker` · `GDB` · `QEMU` · `ASan / UBSan` · `Make`

---

## 📫 Contact

- **Email:** [rustam98137@gmail.com](mailto:rustam98137@gmail.com)
- **LinkedIn:** [linkedin.com/in/rustamsheoran](https://linkedin.com/in/rustamsheoran)
- **GitHub:** [github.com/RustamSheoran](https://github.com/RustamSheoran)
- **Codeforces:** [codeforces.com/profile/adarak](https://codeforces.com/profile/adarak)
- **LeetCode:** [leetcode.com/u/RustamSheoran](https://leetcode.com/u/RustamSheoran/)

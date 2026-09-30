# Hi, I'm Rustam Sheoran 👋

**Systems Engineer · C/C++ · Rust · Linux · Competitive Programmer**

I build systems from the ground up, with a focus on systems programming, Linux internals, computer architecture, and performance engineering.

---

## 🚀 Systems Projects

### [Helios](https://github.com/RustamSheoran/Helios)
Systems monorepo in low-level Rust implementing Linux container isolation, an interactive Unix shell, and a custom global heap allocator.

- **Container Isolation Engine:** Implements UTS, Mount, IPC, PID, and Network namespace unsharing, recursive private mount propagation, `pivot_root` virtual filesystem jails, cgroups v2 resource accounting, and raw Seccomp BPF system call filters.
- **Process Supervision & Job Control:** Synchronizes child execution across namespace switches using synchronizing `O_CLOEXEC` pipes, coupled with an interactive shell managing AST execution pipelines, I/O redirection, and process groups (`setpgid`, `tcsetpgrp`).
- **Custom Global Allocator:** Custom `GlobalAlloc` managing page-backed memory via intrusive doubly-linked Best-Fit free lists with physical coalescing and fixed-slot Slab caches over `mmap`/`munmap`.

**Stack:** `Rust` · `Linux Namespaces` · `cgroups v2` · `Seccomp BPF` · `Virtual Memory`

---

### [RESP-CPP](https://github.com/RustamSheoran/RESP-CPP)
High-performance, single-threaded, event-driven Redis-compatible key-value store written in C++17.

- **Event Reactor Core:** Leverages Linux `epoll` (`epoll_create1`, `epoll_ctl`, `epoll_wait`) to service thousands of concurrent client connections on a single thread.
- **Zero-Copy Command Parser:** Tokenizes strict Redis Serialization Protocol (RESP) streams using `std::string_view` slices directly from client buffers without intermediate heap allocations.
- **Network Tuning & Backpressure:** Uses `TCP_NODELAY` to disable Nagle's algorithm, non-blocking sockets (`O_NONBLOCK`), `SIGPIPE` shielding, and dynamic `EPOLLOUT` buffer drain management.
  
**Stack:** `C++17` · `Linux epoll` · `POSIX Sockets` · `RESP Protocol`

---

### [DWDP](https://github.com/RustamSheoran/DWDP-Triton-MoE-Inference-Engine)
Distributed Weight Data Parallelism Mixture-of-Experts (MoE) high-throughput inference engine.

- **Fused Triton Grouped-GEMM:** Single-launch MoE kernel fusing token gather, SwiGLU activation, and down-projection in `@triton.jit`, cutting CUDA kernel launches from 24+ down to 1 per layer.
- **Native FP8 Precision & Micro-Scaling:** Full FP8 (E4M3 / E5M2) execution with fine-grained per-expert micro-scaling factors and FP32 Tensor Core accumulation.
- **Runtime Graph & Memory Manager:** Static CUDA Graph replay engine eliminating CPU call overhead, paired with PagedAttention block-wise KV-cache allocation to eliminate VRAM fragmentation.

**Stack:** `Triton` · `CUDA` · `Python` · `C++20` · `FP8` · `PagedAttention`

---

### [simd](https://github.com/RustamSheoran/simd)
Hand-written AArch64 NEON SIMD dot product benchmarked against `-O3` vectorizing compilers.

- **Hand-Optimized Assembly:** Written directly in AArch64 ELF assembly (`neon_dot.s`) to strictly control register allocation, widening loads, and accumulator dependency chains.
- **Loop Unrolling & Widening:** Unrolls main loop across 32 elements using 8 independent two-lane 64-bit accumulators (`smlal`/`smlal2`) to maximize hardware pipeline throughput.
- **Tail Path & Verification:** Reduces vector accumulators into scalar results with `smaddl` tail handling on 1,000,003 elements, verified under QEMU user mode with remote GDB register inspection.

**Stack:** `AArch64 Assembly` · `ARM NEON` · `C++` · `QEMU` · `GDB`

---

## 🏆 Competitive Programming

- **Codeforces:** Expert · Peak Rating 1675 · [adarak](https://codeforces.com/profile/adarak)
- **LeetCode:** Knight · Rating 1953 (Top 3.4%) · 512+ Solved (127 Hard) · [RustamSheoran](https://leetcode.com/u/RustamSheoran/)

---

## 🧰 Technical Arsenal

- **Systems & Kernels:** `Linux (Namespaces, cgroups v2, Seccomp, epoll)` · `POSIX` · `x86_64 / AArch64 Assembly`
- **Languages & Toolchains:** `C` · `C++17/20` · `Rust` · `Python` · `Make`
- **Performance & Acceleration:** `CUDA` · `OpenAI Triton` · `ARM NEON` · `SIMD` · `FP8` · `CUDA Graphs` · `PagedAttention`
- **Debugging & Runtime:** `GDB` · `QEMU` · `AddressSanitizer (ASan/UBSan)` · `Docker`

---

## 📫 Contact

- **Email:** [rustam98137@gmail.com](mailto:rustam98137@gmail.com)
- **LinkedIn:** [linkedin.com/in/rustamsheoran](https://linkedin.com/in/rustamsheoran)
- **Codeforces:** [codeforces.com/profile/adarak](https://codeforces.com/profile/adarak)
- **LeetCode:** [leetcode.com/u/RustamSheoran](https://leetcode.com/u/RustamSheoran/)

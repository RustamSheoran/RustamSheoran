<h1 align="center">Hi 👋, I'm Rustam Sheoran</h1>
<h3 align="center">Systems Engineer | OS Developer | Distributed Systems</h3>

---

* 🎓 **18 years old, high school graduate (gap year)**
* 🔭 I’m currently working on **Jepsen-inspired distributed systems testing framework (Go + Python)**
* 🌱 I’m currently learning **Machine Learning, Distributed Systems, Advanced OS Design**
* 👯 I’m looking to collaborate on **low-level systems (OS, compilers, networking, infra)**
* 🤝 I’m looking for help with **advanced OS concepts (memory management, schedulers, filesystems)**
* 👨‍💻 All of my projects are available at
  👉 https://github.com/RustamSheoran
* 💬 Ask me about **Operating Systems, C/C++, System Design, Backend Engineering**
* 📫 How to reach me **[rustam98137@gmail.com](mailto:rustam98137@gmail.com)**
* ⚡ Fun fact **I break systems to understand how they actually work.**

---

## 🏆 Competitive Programming

### CodeChef

* ⭐ **5★ (2132 rating, Division 1)**
* 🌍 **Global Rank: 622**
* 🇮🇳 **Country Rank: 335 (India)**
* 📊 Top ~**0.1–0.2% globally**

### LeetCode

* 🟢 **Knight (1903 rating)**
* 🌍 Top **4.28% globally**
* ⚠️ Less active currently

---

## 🚀 Featured Projects

### 🧩 OS-C

> Freestanding x86_64 operating system kernel (C + Assembly)

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

* Full control over memory (PMM + virtual paging, higher-half kernel)
* CPU initialization (GDT/IDT), interrupt handling, timer configuration
* Syscall interface bridging user ↔ kernel space
* UEFI-based boot with no libc/runtime dependencies

⚡ Demonstrates direct control over hardware, memory, and execution flow

🔗 https://github.com/RustamSheoran/OS-C

---

### 🖥️ Shell-C++

> Modern C++20 Unix-like shell with AST-based execution

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

* AST-based parsing with operator precedence
* Pipelines & I/O redirection via file descriptors
* Job control (fg/bg, signals, process groups)
* Interactive shell (history, completion, editing)

⚡ Explores how command execution maps to OS-level process control

🔗 https://github.com/RustamSheoran/shell-c-plusplus

---

### 🎨 ASCII-CAM

> Real-time ASCII rendering experiment (browser-based)

```
Camera Feed
     │
     ▼
Frame Buffer
     │
     ▼
ASCII Mapping (char intensity)
     │
     ▼
Canvas Rendering (GPU/CPU)
```

* Live camera → ASCII conversion using Canvas API
* Adjustable resolution + character sets
* 60+ FPS rendering with performance tracking
* Image/video export

⚡ Built to explore real-time rendering and performance in the browser

🔗 https://github.com/RustamSheoran/ASCII-CAM

---

### 🧪 Distributed Systems Testing (In Progress)

> Jepsen-inspired framework for validating correctness under failures

```
Client Workload
       │
       ▼
Distributed Cluster
       │
       ▼
Fault Injection Layer
(network partitions / crashes / latency)
       │
       ▼
Observability + Logs
       │
       ▼
Consistency Verification
(linearizability / eventual consistency)
```

* Fault injection (network partitions, crashes, latency)
* Consistency validation (linearizability, eventual consistency)
* Distributed workload simulation
* Go (engine) + Python (analysis layer)

⚠️ Private repository

---

## 🧰 Tech Stack

### ⚙️ Systems & Low-Level

<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" width="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" width="40"/>
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" width="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" width="40"/>
</p>

---

### 🧠 AI / ML

<p align="left">
<img src="https://www.vectorlogo.zone/logos/python/python-icon.svg" width="40"/>
<img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" width="40"/>
<img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" width="40"/>
</p>

---

### 🌐 Backend & Infra

<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" width="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" width="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" width="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" width="40"/>
</p>

---

### 🎨 Frontend

<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" width="40"/>
<img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" width="40"/>
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" width="40"/>
</p>

---

## ⚡ Engineering Focus

* Systems programming & low-level architecture
* Distributed systems & fault tolerance
* Performance and correctness over abstraction

---

## 📫 Connect with me

<p align="left">
<a href="https://linkedin.com/in/rustamsheoran" target="blank">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linkedin/linkedin-original.svg" height="30"/>
</a>
<a href="https://www.codechef.com/users/ginge" target="blank">
<img src="https://cdn.simpleicons.org/codechef" height="30"/>
</a>
</p>

---
## 📈 Activity  

Consistent work across systems programming, distributed systems, and backend infrastructure.  
Focused on building from first principles rather than using abstractions.

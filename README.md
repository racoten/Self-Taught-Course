# Self-Taught Course

Interactive offensive security training courses built around real open-source GitHub projects. Each course is a deep-dive into the internals of a specific tool or technique — how it works, why it works, and how defenders detect it.

> **Built for learning, not for deployment.**

## Live Site

Hosted on GitHub Pages: [Self-Taught Course Dashboard](https://racoten.github.io/Self-Taught-Course/)

## Stats

- **18 Courses** across syscalls, injection, evasion, encryption, rootkits, and more
- **147 Modules** of structured content
- **3 Difficulty Tiers** — Beginner, Intermediate, Advanced

## Courses

### Memory & Evasion Fundamentals
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [AceLdr](Project/AceLdr/AceLdr_index.html) | Reflective DLL loading, sleep masking, FOLIAGE | C / ASM | 9 |
| [Stardust](Project/Stardust/Stardust_index.html) | PIC C++20 implant template, PEB walking | C++20 / NASM | 10 |
| [FunctionPeekaboo](Project/FunctionPeekaboo/FunctionPeekaboo_index.html) | LLVM per-function self-masking XOR | C++ / LLVM | 8 |

### Syscall Techniques
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [Hell's Gate](Project/HellsGate/HellsGate_index.html) | Dynamic SSN resolution & direct syscalls | C / x64 ASM | 8 |
| [LayeredSyscall](Project/LayeredSyscall/LayeredSyscall_index.html) | VEH-based indirect syscalls, HW breakpoints | C++ / x64 | 8 |

### Sleep Obfuscation & Memory Fluctuation
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [Ekko](Project/Ekko/Ekko_index.html) | Timer-based sleep obfuscation, ROP + RC4 | C / x64 | 8 |
| [ShellcodeFluctuation](Project/ShellcodeFluctuation/ShellcodeFluctuation_index.html) | XOR encrypt/decrypt memory on sleep cycles | C++ / x64 | 8 |
| [ShellGhost](Project/ShellGhost/ShellGhost_index.html) | Single-instruction VEH execution via INT3 | C / x64 | 8 |

### Process Injection
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [PoolParty](Project/PoolParty/PoolParty_index.html) | 8-variant thread pool injection | C++ / x64 | 8 |
| [ThreadlessInject](Project/ThreadlessInject/ThreadlessInject_index.html) | Threadless injection via remote function hooking | C++ / x64 | 8 |

### Call Stack Spoofing
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [SilentMoonwalk](Project/SilentMoonwalk/SilentMoonwalk_index.html) | Dynamic call stack spoofing & desynchronization | C++ / x64 | 8 |
| [Draugr](Project/Draugr/Draugr_index.html) | Synthetic call stack frames, BOFs, JMP RBX gadgets | C++ / ASM / BOF | 8 |

### Shellcode & Payload Engineering
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [Donut](Project/Donut/Donut_index.html) | PE/DLL/.NET-to-shellcode conversion | C / x86/x64 | 8 |
| [Shoggoth](Project/Shoggoth/Shoggoth_index.html) | Polymorphic shellcode engine with asmjit | C++ / x86/x64 | 8 |
| [Hooka](Project/Hooka/Hooka_index.html) | Shellcode loader generator, AMSI/ETW patching | Go / Windows | 8 |

### Process Tampering & Loader Techniques
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [ProcessGhosting](Project/ProcessGhosting/ProcessGhosting_index.html) | Ghost process from delete-pending files | C++ / x64 | 8 |
| [COFFLoader](Project/COFFLoader/COFFLoader_index.html) | Beacon Object File loader outside Cobalt Strike | C / x64 | 8 |

### Kernel
| Course | Topic | Language | Modules |
|--------|-------|----------|---------|
| [Nidhogg](Project/Nidhogg/Nidhogg_index.html) | Windows kernel rootkit — DKOM, ETW, callbacks | C/C++ / Kernel | 8 |

## Project Structure

```
index.html                              Main dashboard (18 courses)
assets/
  course.css                            Shared module styles
  course.js                             Quiz grading, mobile nav, scroll animations
Project/
  <CourseName>/
    <CourseName>_index.html             Course landing page with module grid
    modules/
      module1.html ... module8.html     Individual teaching modules
```

## How Each Module Works

Every module is a self-contained HTML page with:

- **Sidebar navigation** linking all modules in the course
- **Difficulty badges** (Beginner / Intermediate / Advanced)
- **Code blocks** with language tags and syntax highlighting
- **Flow diagrams** built from CSS (no images needed)
- **Interactive quizzes** graded client-side via `gradeQuiz()`
- **Prev/Next navigation** at the bottom

Modules share `assets/course.css` and `assets/course.js`. Each course sets its own accent colors via CSS custom properties:

```css
:root {
  --accent: #e11d48;
  --accent2: #be123c;
  --gradient: linear-gradient(135deg, #e11d48, #be123c);
}
```

## Offline Use

Clone and open any HTML file directly in your browser — no build step, no server, no dependencies:

```bash
git clone https://github.com/yourusername/Self-Taught-Course.git
# Open index.html in your browser
```

## Disclaimer

This content is strictly for **educational and authorized security research purposes**. Every technique covered here has documented defensive countermeasures. Understanding how attacks work is essential for building effective defenses.

Do not use any of this material against systems you do not own or have explicit authorization to test.

## Roadmap

- [ ] End-of-course exams
- [ ] Hands-on assignments
- [ ] Consolidated references file
- [ ] Search functionality across all courses

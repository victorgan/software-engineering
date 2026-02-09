# 13 — Developer Tooling and Productivity MOC

> <- Back to [[Software Engineering - Map of Content]]

The tools and workflows that multiply developer effectiveness. Mastering your tools is a career-long leverage multiplier.

---

## Editors & IDEs

- **VS Code** — Extensions ecosystem, settings.json, tasks.json, launch.json (debugging), multi-root workspaces, remote development (SSH, containers, WSL), integrated terminal, Git integration
- **JetBrains** — IntelliJ IDEA (Java/Kotlin), PyCharm (Python), WebStorm (JavaScript/TypeScript), GoLand (Go); refactoring tools, database integration, run configurations, inspections
- **Vim / Neovim** — Modes (normal, insert, visual, command), motions (w, b, f, t, /, gg, G), text objects (iw, i", a(), i{), registers, macros, plugins (lazy.nvim, telescope, nvim-lspconfig, treesitter), Neovim Lua config
- **Emacs** — Org mode, Elisp extensibility, Magit (Git porcelain), TRAMP (remote editing), Evil mode (Vim emulation)
- **LSP (Language Server Protocol)** — Editor-agnostic language intelligence, completions, diagnostics, go-to-definition, hover, rename; decouples language support from editors
- **DAP (Debug Adapter Protocol)** — Editor-agnostic debugging, breakpoints, stepping, variable inspection, watch expressions

---

## Shell & Terminal

- **Bash / Zsh** — Shell scripting, parameter expansion, command substitution, pipelines, redirection, process substitution, job control
- **Shell Scripting** — Variables, conditionals (if/case), loops (for/while), functions, exit codes, trap, set -euo pipefail, shellcheck
- **Aliases & Functions** — Shorthand commands, dotfiles management (chezmoi, yadm, GNU Stow), shell profiles (.bashrc, .zshrc)
- **Terminal Multiplexers** — tmux (sessions, windows, panes, keybindings, plugins with tpm), screen (legacy), persistent sessions over SSH
- **Terminal Emulators** — iTerm2 (macOS, profiles, split panes), Warp (AI-assisted, blocks), Ghostty (GPU-accelerated, Zig), Alacritty (GPU-accelerated, minimal config), Kitty (GPU-accelerated, scripting)
- **Modern CLI Tools** — fzf (fuzzy finder), ripgrep (rg), fd (find alternative), bat (cat alternative), eza (ls alternative), zoxide (cd alternative), jq (JSON processing), yq (YAML processing)

---

## Debugging

- **Print Debugging** — Strategic log statements, structured logging for debuggability, temporary vs permanent logging
- **Interactive Debuggers** — GDB (C/C++), LLDB (C/C++/Swift), browser DevTools (Sources panel, breakpoints, watch, call stack), Python debugger (pdb/ipdb), Node.js inspector
- **Memory Debuggers** — Valgrind (memory leaks, uninitialized reads), AddressSanitizer (ASan), MemorySanitizer (MSan), LeakSanitizer (LSan), ThreadSanitizer (TSan)
- **Profilers** — CPU profiling (flame graphs, sampling vs instrumentation), memory profiling (heap snapshots), I/O profiling (see [[Performance Engineering]])
- **Log-Based Debugging** — Correlation IDs, structured log queries, log aggregation tools (see [[Observability]])
- **Rubber Duck Debugging** — Explaining the problem to someone (or something) to clarify your thinking, often reveals the solution
- **Advanced Techniques** — Conditional breakpoints, tracepoints (log without stopping), time-travel debugging (rr), core dump analysis, strace/dtrace

---

## Package Managers

- **JavaScript** — npm (default, package-lock.json), yarn (Plug'n'Play, zero-installs), pnpm (content-addressable storage, strict, fast, monorepo support)
- **Python** — pip (requirements.txt), uv (fast Rust-based resolver, pip-compatible), poetry (pyproject.toml, lock files, dependency groups), conda (scientific/data science)
- **Rust** — Cargo (Cargo.toml, Cargo.lock, crates.io, workspaces, features, build scripts)
- **Go** — Go modules (go.mod, go.sum, module proxy, minimum version selection)
- **Java / JVM** — Maven (pom.xml, Central Repository, convention over configuration), Gradle (Groovy/Kotlin DSL, incremental builds, build cache)
- **System-Level** — Homebrew (macOS/Linux), apt/dpkg (Debian/Ubuntu), nix (reproducible, declarative)
- **Lock Files** — Pinning exact versions, reproducible builds, lock file conflicts in merge
- **Dependency Resolution** — Version ranges (semver, ^, ~), dependency hell, diamond dependency problem, peer dependencies

---

## Containers for Development

- **Dev Containers** — VS Code devcontainers, devcontainer.json, features, consistent environments across team, GitHub Codespaces
- **Docker Compose for Local Services** — Multi-container local environments, databases, message queues, service dependencies, volumes for persistence
- **Testcontainers** — Programmatic container management in tests, real databases/services in integration tests, language libraries (Java, Python, Go, Node.js)
- **Local Development Patterns** — Hot reload with mounted volumes, local vs containerized tradeoffs, hybrid approaches (app local, services in containers)

---

## AI-Assisted Development

- **Code Completion** — GitHub Copilot (inline suggestions, chat), Claude Code (agentic CLI, tool use), Cursor (AI-first editor), Codeium, TabNine
- **Chat-Based Coding** — Conversational code generation, explaining code, debugging assistance, architecture discussion, rubber ducking with AI
- **AI Code Review** — Automated review comments, catching bugs and style issues, security scanning, PR summarization
- **Prompt Engineering for Code** — Providing context (file contents, error messages), specifying constraints, iterative refinement, few-shot examples for code patterns
- **Limitations and Risks** — Hallucinated APIs, outdated patterns, security vulnerabilities in generated code, over-reliance, license concerns, verifying correctness, understanding generated code before committing

---

#developer-tools #productivity #editors #shell #debugging #ai-assisted-development

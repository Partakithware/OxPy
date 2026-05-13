
Visit here: https://partakithware.github.io/OxPy/

Ox-Py WDE (AI Readme, some stuff is faulty, I will fix it later :/, anyhow 'opcc' does tcc-o-ppci-wasm which is how tcc is used right now if used. 'cc' just uses ppci, the AI said some other BS about tcc and such, but you get the gist, sorry will do README later)

Browser-native Web Desktop Environment (WDE) for Python, C, and WebAssembly development.

Overview

Ox-Py WDE is an experimental client-side operating environment implemented entirely in the browser using WebAssembly-based runtimes and persistent virtual filesystem layers.

The environment provides:

Multi-window desktop shell
POSIX-inspired terminal environment
Persistent filesystem via IDBFS
Python runtime through Pyodide
C compilation through TinyCC (TCC) compiled to WebAssembly
WebAssembly tooling and execution support
Integrated development utilities and file management

Ox-Py operates without a mandatory backend server and stores workspace data locally within the browser.

Architecture
Browser Runtime
├── Ox-Py Desktop Shell
│   ├── Window Manager
│   ├── Taskbar / Start Menu
│   ├── Context Menu System
│   └── Application Runtime
│
├── Runtime Layer
│   ├── Pyodide (Python 3)
│   ├── TinyCC (TCC → Wasm)
│   ├── WASI Runtime
│   └── WABT Toolkit
│
├── Virtual Filesystem
│   ├── IDBFS Persistence
│   ├── User Workspace Mounts
│   └── Local Account Storage
│
└── Integrated Applications
    ├── Terminal
    ├── File Explorer
    ├── Text Editor
    ├── Graphics Window
    └── Ox-Browser
Core Components
Desktop Environment

The desktop shell provides:

Draggable/resizable application windows
Taskbar-based window management
Start menu launcher
Context menu integration
Layered desktop compositor
Multi-application runtime environment

The window manager is implemented in vanilla JavaScript and uses pointer-based event handling for desktop and touch interaction support.

Runtime Systems
Python Runtime

Python execution is provided through Pyodide.

Features:

Interactive Python REPL
Script execution
Filesystem access
Runtime package installation
Matplotlib integration
Browser-side execution

The runtime is fully client-side and executes inside the browser WebAssembly sandbox.

C Toolchain

C compilation is provided through Tiny C Compiler compiled to WebAssembly.

Features:

In-browser C compilation
Wasm-targeted compilation flow
Header/toolchain bootstrap support
Integrated filesystem bridging
Experimental PPCI backend integration

The environment includes:

cc
gcc
clang
tcc
opcc

shell interfaces mapped into the runtime environment.

WebAssembly Tooling

Ox-Py includes:

.wat → .wasm compilation
WASI runtime integration
Dynamic WebAssembly loading
Runtime Wasm execution support

The environment uses:

WABT
WASI
Wasm binary tooling

for browser-side module generation and execution.

Filesystem
Persistent Storage

Persistence is implemented through IDBFS backed by IndexedDB.

Features:

Persistent user directories
Session restoration
Local project storage
Browser-contained workspace management

Default runtime mount structure:

/myhome/<user>

Filesystem operations are exposed through:

Shell commands
File Explorer
Runtime APIs
Shell Environment

The integrated shell provides a POSIX-inspired command environment.

Supported functionality includes:

Pipelines
File operations
Recursive filesystem traversal
Environment variables
Stream processing
Runtime command execution

Implemented commands include:

ls
cd
pwd
mkdir
touch
rm
cp
mv
cat
head
tail
grep
wc
find
sort
uniq
diff
stat
df
env
uname
date
whoami
hostname
run
cc
opcc
clibs
backup-wde

Pipeline execution is supported using standard pipe semantics:

cat file.txt | grep test | sort
Integrated Applications
Terminal

Interactive shell and Python execution environment.

File Explorer

Filesystem browser with:

Import/export
Copy/paste
Rename/delete
Context menu integration
Text Editor

Integrated browser-based source editor.

Graphics Window

Dedicated rendering surface for:

Matplotlib output
Canvas rendering
Video playback
Ox-Browser

Embedded browser window subsystem with isolated iframe sessions.

Technical Stack
Runtime Technologies
Pyodide
Tiny C Compiler
WebAssembly System Interface
WABT
Frontend
Vanilla JavaScript (ES Modules)
HTML5
CSS3
Additional Libraries
JSZip
Font Awesome
Persistence Model

Ox-Py uses a local-first persistence model.

Characteristics:

No required backend server
Local account storage
IndexedDB-backed filesystem persistence
Browser-contained execution state

All user data remains inside the browser storage environment unless explicitly exported.

Security Model

Ox-Py executes entirely within the browser sandbox.

The environment exposes low-level execution workflows including:

Dynamic code execution
WebAssembly compilation
Native-style memory interaction through Wasm toolchains

Ox-Py is experimental software and should be treated as an untrusted development environment.

Status

Current project status:

Experimental
Research-oriented
Under active architectural development

The platform is intended for:

WebAssembly experimentation
Browser runtime research
Client-side systems experimentation
Educational runtime development
Portable development environment research

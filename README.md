Ox-Py WDE (Web Desktop Environment)

Ox-Py is a high-performance, experimental Web Desktop Environment (WDE) that transforms your browser into a fully functional developer workstation. It leverages the power of WebAssembly (Wasm) to provide a persistent, multi-window OS experience for Python and C development without requiring a server backend.
🚀 Core Features

    Integrated Multi-Engine Runtime:

        Python: Full Python 3 environment powered by Pyodide.

        C Compiler: Native C execution via the TCC (Tiny C Compiler) engine ported to Wasm.

        WebAssembly: On-the-fly compilation of .wat files to Wasm binaries.

    Window Manager & Shell:

        A complete Windows-style UI featuring a taskbar, start menu, and draggable/resizable application windows.

        A custom POSIX-like Shell with built-in commands (ls, cd, mkdir, rm, cat, etc.) and support for piped commands.

    Built-in Applications:

        Python Terminal: Interactive REPL and script execution.

        Text Editor: For writing and managing scripts directly in the browser.

        File Explorer: Advanced file management with context menus for importing, exporting, renaming, and deleting files.

        Ox-Browser: A nested browser for web access within the environment.

        Graphics Window: Full support for capturing and displaying Matplotlib plots and video playback.

    Persistence: Uses IDBFS (IndexedDB) to ensure your files and user accounts persist across browser sessions.

🛠️ Technical Stack

    Language Runtimes: Pyodide (Python), TCC (C), WASI (WebAssembly System Interface).

    Frontend: Vanilla JavaScript (ESM), HTML5, CSS3.

    Utilities: JSZip (archiving), Wabt (Wasm toolkit), FontAwesome (icons).

⚠️ Experimental Notice

Ox-Py is an experimental environment intended for educational and research purposes. It allows for memory-unsafe operations via TCC and Python within the browser sandbox.

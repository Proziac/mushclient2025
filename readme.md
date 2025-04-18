# MUSHclient Qt Port

**A modern, cross-platform Qt-powered port of MUSHclient**, the powerful MUD client for Windows. This project preserves the core functionality and extensibility of MUSHclient while updating the UI, networking, and plugin architecture using modern C++ and Qt 6.

---

## Goals

- Cross-platform (Windows, Linux, macOS) MUD client
- Full-featured Telnet + SSL support
- Lua scripting (via sol2 or LuaBridge)
- Plugin architecture with dynamic loading
- Modern UI with tabs, logging, color parsing, and customization
- Backward compatibility with core MUSHclient logic where possible

---

## Project Layout

```
MUSHclientQt/
├── app/              # Entry point, app controller
├── gui/              # Main window, preferences, custom widgets
├── network/          # Telnet, SSL, MCCP, session handling
├── scripting/        # Lua engine and script interfaces
├── plugins/          # Plugin loader, sandbox, lifecycle hooks
├── core/             # Triggers, aliases, macros, state machine
├── assets/           # Icons, styles, themes
├── CMakeLists.txt
└── README.md
```

---

## Tech Stack

- **C++17**
- **Qt 6 (Widgets + Network + Multimedia)**
- **Lua 5.4** via [sol2](https://github.com/ThePhD/sol2)
- **zlib** for MCCP
- **CMake** for build system

---

## Development Roadmap

### Phase 1: Project Bootstrap & Core Extraction
- [x] Create Qt CMake structure
- [x] Begin migrating reusable core logic (triggers, world state)

### Phase 2: UI Shell with Qt
- [ ] Build tabbed main window
- [ ] Add input box + styled output
- [ ] Integrate layout themes

### Phase 3: Networking
- [ ] Replace CAsyncSocket with QTcpSocket
- [ ] Integrate QSslSocket for TLS
- [ ] Port Telnet negotiation + MCCP

### Phase 4: Lua Scripting
- [ ] Add Lua interpreter via sol2
- [ ] Bind core API to Lua
- [ ] Add live scripting console

### Phase 5: Plugin System
- [ ] Dynamic plugin loader
- [ ] Lua plugin hooks: connect, install, tick, etc.
- [ ] Plugin manager UI

### Phase 6: Profiles & Config
- [ ] Replace registry with QSettings
- [ ] Preferences window
- [ ] Load/save world XML

### Phase 7: Feature Completeness
- [ ] Aliases/macros engine
- [ ] Sound support
- [ ] Logging & scripting output

---

## Screenshots

*(Coming soon)*

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Credits

Based on [MUSHclient](http://www.gammon.com.au/mushclient) by Nick Gammon.  
Qt port and modernization by Proziac.

---

## Contributions

PRs and ideas are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) (coming soon).

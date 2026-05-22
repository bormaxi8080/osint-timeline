# Timeline Summarized Draft


Press

Trials

Liar

Somewhere in America

Celestial Mantis

Wire tit

Joke

Hive

SpaceX

Propaganda

Barcode

UFO Monument

----

OSINT Anatomy / VoidStealer: Debugging Chrome to Steal Its Secrets. A Novel Debugger-based ABE Bypass Spotted in the Wild: https://www.gendigital.com/blog/insights/research/voidstealer-abe-bypass

Chrome keeps saved passwords locked behind one master key. VoidStealer steals that key using a tool Chrome cannot block. When it is done, passwords, open sessions, and payment cards are all readable. The technique had been on GitHub for over six months. Nobody had used it in the wild until now.  
  
Chrome encrypts passwords with a key that Windows DPAPI hands out to any program running as the same user. Google fixed this in July 2024 with App-Bound Encryption, or ABE, binding the key to a service that only releases it to Chrome. Lumma Stealer, Meduza Stealer, Whitesnake, and Lumar all found bypasses within months. VoidStealer appeared on HackForums on December 12, 2025 and reached twelve versions before v2.0 on March 13, 2026.  
  
It worked, and then it did not.
  
VoidStealer spawns a hidden Chrome instance with SW_HIDE, attaches as a debugger, and waits. Chrome decrypts its master key during startup. VoidStealer scans chrome.dll for OSCrypt.AppBoundProvider.Decrypt.ResultCode, the exact point right after decryption, which stays present across Chrome versions. Hardware breakpoints via DR0 and DR7 through SetThreadContext write nothing to the browser. When the breakpoint hits, the v20_master_key is in R15 for Chrome and R14 for Edge. Two ReadProcessMemory calls, and it is gone. Stolen session cookies bypass passwords and 2FA entirely because the session was already verified.  
  
VoidStealer also falls back to the older injection technique if the debugger approach fails, though that method is noisier and easier to detect  
  
Gen Digital confirmed the code came from ElevationKatz by researcher Meckazin, public on GitHub for over six months. VoidStealer is the first infostealer to use it in the wild. Chrome, Edge, Brave, Opera, and Vivaldi are in range. Firefox is not affected  
  
Watch for debugger attachment to browser processes. Legitimate software never does this  
  
→ Processes attaching to chrome.exe or msedge.exe via DebugActiveProcess  
→ Hidden browser instances with SW_HIDE or headless mode  
→ ReadProcessMemory calls from unknown processes targeting browser processes  
→ Chrome or Edge with unexpected parent processes  
  
SHA-256 hash for VoidStealer v2.0:  
f783fde5cf7930e4b3054393efadd3675b505cbef8e9d7ae58aa35b435adeea4  
  
Stop storing passwords in the browser. Use Bitwarden or 1Password instead. Keep Windows and Chrome updated, avoid unverified software, and use endpoint protection that monitors process behavior.
  
Research & writing: Jolanda de Koff  
Sharing is fine. Copying without credit is not.

Full Breakdown: https://hackingpassion.com/voidstealer-chrome-abe-bypass/

----

Awesome OSINT Arsenal. Curated OSINT & recon toolkit for Kali Linux - 100+ tools, one-command installer, covering SOCMINT, GEOINT, network recon, dark web, forensics & more: https://github.com/rawfilejson/awesome-osint-arsenal

LeoLabs. PERSISTENT ORBITAL INTELLIGENCE. Safeguarding our way of life on Earth with the living map of activity in space: https://leolabs.space/

**PPG-Toolbox** is an open-source platform designed for camera-based physiological sensing, also known as remote photoplethysmography (rPPG):

https://github.com/ubicomplab/rPPG-Toolbox

BookLore. A self-hosted, multi-user digital library with smart shelves, auto metadata, Kobo & KOReader sync, BookDrop imports, OPDS support, and a built-in reader for EPUB, PDF, and comics:

https://github.com/mvanhorn/booklore/

----

Professional Membership Portals: An Excellent Resource for Due Diligence and Investigations  
  
Guide by Ionatan Waisgluss:  
  
What Are Professional Membership Portals?  
Why Verify Registration and Status?  
What Other Information Can These Portals Reveal?  
Jurisdiction Matters  
Professional Membership Portals  
Global and International Credential Verification  
United States  
European Professional Registers  
Good Search Habits  
Pivoting on Technologies (i.e. Portal Software)

https://appliedawareness.ca/professional-membership-portals-an-excellent-resource-for-due-diligence-and-investigations/

----

**OSINT Tools, Services and Investigations:**

Graphtreon. Track, rank, and visualize Patreon creator stats like earnings and growth:

https://graphtreon.com

Docker Steam Headless. A Headless Steam Docker image supporting NVIDIA GPU and accessible via Web UI: https://github.com/Steam-Headless/docker-steam-headless

AndroidForensics. Automated Android forensic toolkit - extract device info, apps, contacts, call logs, SMS, system logs, and more via ADB for security audits and investigations: https://github.com/DouglasFreshHabian/androidForensics

Android IMSI Catcher Detector. `AIMSICD` is an Android app to detect [IMSI-Catchers](https://en.wikipedia.org/wiki/IMSI-catcher). These devices are false mobile towers (base stations) acting between the target mobile phone(s) and the real towers of service providers. As such they are considered a Man-In-The-Middle (MITM) attack. This surveillance technology is also known as "[StingRay](https://en.wikipedia.org/wiki/Stingray_phone_tracker)", "Cellular Interception" and alike: https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector

Hiddify. A multi-platform proxy client based on [Sing-box](https://github.com/SagerNet/sing-box) universal proxy tool-chain. Hiddify offers a wide range of capabilities, like automatic node selection, TUN mode, remote profiles etc. Hiddify is ad-free and open-source. With support for a wide range of protocols, it provides a secure and private way for accessing free internet: https://github.com/hiddify/hiddify-app

Transmission is a fast, easy, and free BitTorrent client. It comes in several flavors: A native macOS GUI application, GTK+ and Qt GUI applications for Linux, BSD, etc, A Qt-based Windows-compatible GUI application, A headless daemon for servers and routers, A web UI for remote controlling any of the above: https://github.com/transmission/transmission

GuardDog is a CLI tool to Identify malicious PyPI and npm packages: https://github.com/DataDog/guarddog

----

**Universal Search & AI:**

Free LLM API. OpenAI-compatible proxy that aggregates free-tier keys from ~14 AI providers with automatic failover. For personal experimentation only: https://github.com/tashfeenahmed/freellmapi

SimpleMem: Efficient Lifelong Memory for LLM Agents — Text & Multimodal: https://github.com/aiming-lab/SimpleMem

Open-source AI agent firewall for MCP security: agent egress control, DLP, SSRF, and prompt injection defense: https://github.com/luckyPipewrench/pipelock

PromptZero. Zero trace. Full answer. Transparent Claude API proxy that anonymizes PII and sensitive data before it leaves your environment. From pentesters, to pentesters: https://github.com/openbashok/promptzero

Codex Autoresearch Skill. A self-directed iterative system for Codex that continuously cycles through: modify, verify, retain or discard, and repeat indefinitely. Inspired by Karpathy’s autoresearch concept: https://github.com/leo-lilinxiao/codex-autoresearch

Adala is an **A**utonomous **DA**ta (**L**abeling) **A**gent framework. Adala offers a robust framework for implementing agents specialized in data processing, with an emphasis on diverse data labeling tasks. These agents are autonomous, meaning they can independently acquire one or more skills through iterative learning. This learning process is influenced by their operating environment, observations, and reflections. Users define the environment by providing a ground truth dataset. Every agent learns and applies its skills in what we refer to as a "runtime", synonymous with LLM: https://github.com/HumanSignal/Adala

PaperBanana: Automating Academic Illustration For AI Scientists: https://github.com/dwzhu-pku/PaperBanana

Open Design. Local-first, open-source alternative to Anthropic's Claude Design.

19 Skills ·  71 brand-grade Design Systems.
Generate web · desktop · mobile prototypes · slides · images · videos · HyperFrames
Sandboxed preview · HTML/PDF/PPTX/MP4 export.

Runs on Claude Code / Codex / Cursor / Gemini / OpenCode / Qwen / Copilot / Hermes / Kimi CLI: https://github.com/nexu-io/open-design

Video Use. Edit videos with coding agents: https://github.com/browser-use/video-use

Jarvis. A 100% private AI voice assistant that lives on your computer (works offline). Talk naturally as if Jarvis is a third person in the room, and get conversational responses. It remembers everything, knows location and time, can check the web, control Chrome, track nutrition, and more with support for unlimited MCPs / tools without context rot: https://github.com/isair/jarvis

CocoIndex. Data transformation framework for AI. Ultra performant, with incremental processing: https://github.com/cocoindex-io/cocoindex

Prefab. Artificial nanofabrication of integrated photonic circuits: https://github.com/PreFab-Photonics/PreFab

Medusa AI Security Scanner. AI-first security scanner with 76 analyzers, 9,600+ detection rules, and repo poisoning detection for AI/ML, LLM agents, and MCP servers. Scan any GitHub repo with: medusa scan --git user/repo: https://github.com/Pantheon-Security/medusa

SCBE-AETHERMOORE. AI governance through geometric cost scaling. This repository is the public working tree for the SCBE-AETHERMOORE stack: a governed AI system built around hyperbolic geometry, semantic weighting, auditability, and multi-layer runtime controls: https://github.com/issdandavis/SCBE-AETHERMOORE

WindSurf API. Windsurf-to-OpenAI compatible API proxy: https://github.com/dwgx/WindsurfAPI

AgentShield. AI agent security scanner. Detect vulnerabilities in agent configurations, MCP servers, and tool permissions. Available as CLI, GitHub Action, ECC plugin, and GitHub App integration: https://github.com/affaan-m/agentshield

Ship-Safe. CLI security scanner built for the agentic era. Detects CI/CD misconfigs, agent permission risks, MCP tool injection, hardcoded secrets, and DMCA-flagged AI dependencies: https://github.com/asamassekou10/ship-safe

Pentest Copilot is an AI-powered browser based ethical hacking assistant tool designed to streamline pentesting workflows: https://github.com/bugbasesecurity/pentest-copilot

PentestAgent is an AI agent framework for black-box security testing, supporting bug bounty, red-team, and penetration testing workflows: https://github.com/GH05TCREW/PentestAgent

AutoPentest AI. Agentic Pentesting MCP server that discovers, exploits, and reports web application vulnerabilities: https://github.com/bhavsec/autopentest-ai

CTI Expert. Cyber Threat Intelligence & OSINT analysis skill for Claude Code. 67+ commands, 35 techniques, no API keys required: https://github.com/7onez/cti-expert

Deepsafe Scan. Universal preflight security scanner for AI coding agents. Detects hooks injection, credential exfiltration & backdoors in .cursorrules, CLAUDE.md, AGENTS.md and more: https://github.com/XiaoYiWeio/deepsafe-scan

Raptor turns Claude Code into a general-purpose AI offensive/defensive security agent. By using Claude.md and creating rules, sub-agents, and skills, and orchestrating security tool usage, we configure the agent for adversarial thinking, and perform research or attack/defense operations: https://github.com/gadievron/raptor

PromptFoo. Test your prompts, agents, and RAGs. Red teaming/pentesting/vulnerability scanning for AI. Compare performance of GPT, Claude, Gemini, Llama, and more. Simple declarative configs with command line and CI/CD integration. Used by OpenAI and Anthropic: https://github.com/promptfoo/promptfoo

----

**Software Development & APIs:**

**SchemaSpy** is a database metadata analyzer. It helps your database administrators and developers visualize, navigate and understand your data model. With an easy-to-use HTML-based report, traversing the entity-relationship diagram has never been simpler: https://github.com/schemaspy/schemaspy

TheSVG. 5,880+ brand SVG icons for developers. Tree-shakeable, typed, open source. npm i thesvg: https://github.com/glincker/thesvg

Otel GUI. A lightweight, zero-config OpenTelemetry trace viewer for local development: https://github.com/metafab/otel-gui

----

**Linux & DevOps:**

Stalwart. All-in-one Mail & Collaboration server. Secure, scalable and fluent in every protocol (IMAP, JMAP, SMTP, CalDAV, CardDAV, WebDAV): https://github.com/stalwartlabs/stalwart

AirPipe. Self-hosted file transfer with a passphrase that works anywhere. Files go peer-to-peer between any two devices. The relay never sees your bytes: https://github.com/Sanyam-G/Airpipe

Zero Password Manager. Open-source self-hosted password manager built with Flutter. Store passwords and crypto seed phrases securely without cloud storage: https://github.com/SoulNaturalist/zero_password_manager

Kaku. A fast, out-of-the-box terminal built for AI coding: https://github.com/tw93/kaku

----

**Hardware & Devices:**

PromptZero is a natural-language operator for the Flipper Zero. Talk to it like you'd talk to a person - it generates payloads, deploys them, and runs them, all from a single sentence: https://github.com/xunholy/promptzero

Dex Retargeting. Various retargeting optimizers to translate human hand motion to robot hand motion: https://github.com/dexsuite/dex-retargeting

valveFM. Vintage FM radio TUI for streaming stations from radio-browser.info: https://github.com/Zorig/valveFM

----

**New from CyberDetective:**



----



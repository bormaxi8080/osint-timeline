![OSINTech Timeline](img/164.jpg)

**Press**

----

**Week of 22 — 28 May 2026**

Every week, I manually curate tools, research, and services that are genuinely useful for OSINT, digital investigations, security research, and adjacent fields.

No hype. No SEO noise. No "AI startups that change everything".  

Only things you can **open, verify, and actually use**.

----

## 🧭 Featured Project

### **Tesari - OSINT Copilot**

A first step for investigations into organized crime, corruption, trafficking, and global risk networks.

**Tesari** is designed as an entry point into complex investigations: structure, context, and navigable intelligence instead of chaotic searching.

🔗 https://www.tesari.ai

----

OSINT Anatomy / **VoidStealer**: Debugging Chrome to Steal Its Secrets. A Novel Debugger-based ABE Bypass Spotted in the Wild:

🔗 https://www.gendigital.com/blog/insights/research/voidstealer-abe-bypass

Chrome keeps saved passwords locked behind one master key. VoidStealer steals that key using a tool Chrome cannot block. When it is done, passwords, open sessions, and payment cards are all readable. The technique had been on GitHub for over six months. Nobody had used it in the wild until now.  
  
Chrome encrypts passwords with a key that Windows DPAPI hands out to any program running as the same user. Google fixed this in July 2024 with App-Bound Encryption, or ABE, binding the key to a service that only releases it to Chrome. Lumma Stealer, Meduza Stealer, Whitesnake, and Lumar all found bypasses within months. VoidStealer appeared on HackForums on December 12, 2025 and reached twelve versions before v2.0 on March 13, 2026.  
  
It worked, and then it did not.
  
**VoidStealer** spawns a hidden Chrome instance with SW_HIDE, attaches as a debugger, and waits. Chrome decrypts its master key during startup. VoidStealer scans chrome.dll for OSCrypt.AppBoundProvider.Decrypt.ResultCode, the exact point right after decryption, which stays present across Chrome versions. Hardware breakpoints via DR0 and DR7 through SetThreadContext write nothing to the browser. When the breakpoint hits, the v20_master_key is in R15 for Chrome and R14 for Edge. Two ReadProcessMemory calls, and it is gone. Stolen session cookies bypass passwords and 2FA entirely because the session was already verified.  
  
VoidStealer also falls back to the older injection technique if the debugger approach fails, though that method is noisier and easier to detect  
  
Gen Digital confirmed the code came from ElevationKatz by researcher Meckazin, public on GitHub for over six months. VoidStealer is the first infostealer to use it in the wild. Chrome, Edge, Brave, Opera, and Vivaldi are in range. Firefox is not affected  
  
Watch for debugger attachment to browser processes. Legitimate software never does this  
  
→ Processes attaching to chrome.exe or msedge.exe via DebugActiveProcess  
→ Hidden browser instances with SW_HIDE or headless mode  
→ ReadProcessMemory calls from unknown processes targeting browser processes  
→ Chrome or Edge with unexpected parent processes
  
Stop storing passwords in the browser. Use Bitwarden or 1Password instead. Keep Windows and Chrome updated, avoid unverified software, and use endpoint protection that monitors process behavior.
  
Research & writing: Jolanda de Koff  
Sharing is fine. Copying without credit is not.

**Full Breakdown:**

🔗 https://hackingpassion.com/voidstealer-chrome-abe-bypass/

----

## 🌍 Regional & Thematic OSINT

**OSINT of Democratic Republic of the Congo** (DRC) by Unishka Research Service:

🔗 https://substack.com/home/post/p-197857984

**Awesome OSINT Arsenal.** Curated OSINT & recon toolkit for Kali Linux - 100+ tools, one-command installer, covering SOCMINT, GEOINT, network recon, dark web, forensics & more:

🔗 https://github.com/rawfilejson/awesome-osint-arsenal

**LeoLabs.** PERSISTENT ORBITAL INTELLIGENCE. Safeguarding our way of life on Earth with the living map of activity in space: 

🔗 https://leolabs.space/

**PPG-Toolbox** is an open-source platform designed for camera-based physiological sensing, also known as remote photoplethysmography (rPPG):

🔗 https://github.com/ubicomplab/rPPG-Toolbox

**BookLore.** A self-hosted, multi-user digital library with smart shelves, auto metadata, Kobo & KOReader sync, BookDrop imports, OPDS support, and a built-in reader for EPUB, PDF, and comics:

🔗 https://github.com/mvanhorn/booklore/

**Professional Membership Portals: An Excellent Resource for Due Diligence and Investigations**
  
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

🔗 https://appliedawareness.ca/professional-membership-portals-an-excellent-resource-for-due-diligence-and-investigations/

----

## 🛠 OSINT Tools, Services & Investigations

**Graphtreon.** Track, rank, and visualize Patreon creator stats like earnings and growth:

🔗 https://graphtreon.com

**Docker Steam Headless.** A Headless Steam Docker image supporting NVIDIA GPU and accessible via Web UI:

🔗 https://github.com/Steam-Headless/docker-steam-headless

**Autobrr.** Modern, easy to use download automation for torrents and usenet:

🔗 https://github.com/autobrr/autobrr

**Crusible SigInt.** Passive OSINT engine: one seed domain → full infrastructure cluster. Automates Ryan McDonald's scam-kit fingerprinting methodology. crt.sh · urlscan · DNS · RDAP · JS wallet drain detection:

🔗 https://github.com/neatlabs-ai/crucible-sigint

**Deskreen** turns any device with a web browser into a secondary screen for your computer:

🔗 https://github.com/pavlobu/deskreen

**AIMap.** Internet-scale discovery and security testing platform for exposed AI agent infrastructure:

🔗 https://github.com/BishopFox/aimap

**Phantomstars.** Automated detection and tracking of fake engagement on GitHub - daily CI, zero infrastructure:

🔗 https://github.com/tg12/phantomstars

**DeblurGAN.** Image Deblurring using Generative Adversarial Networks:

🔗 https://github.com/KupynOrest/DeblurGAN

**ECCV18 Workshops** - Enhanced SRGAN. Champion PIRM Challenge on Perceptual Super-Resolution:

🔗 https://github.com/xinntao/ESRGAN

**AndroidForensics**. Automated Android forensic toolkit - extract device info, apps, contacts, call logs, SMS, system logs, and more via ADB for security audits and investigations:

🔗 https://github.com/DouglasFreshHabian/androidForensics

**Android IMSI Catcher Detector.** `AIMSICD` is an Android app to detect [IMSI-Catchers](https://en.wikipedia.org/wiki/IMSI-catcher). These devices are false mobile towers (base stations) acting between the target mobile phone(s) and the real towers of service providers. As such they are considered a Man-In-The-Middle (MITM) attack. This surveillance technology is also known as "[StingRay](https://en.wikipedia.org/wiki/Stingray_phone_tracker)", "Cellular Interception" and alike:

🔗 https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector

Python client for the [Get SMS Online](https://getsms.online/) API. Receive SMS online and get one-time verification codes programmatically for WhatsApp, Telegram, Google, and 700+ other services:

🔗 https://github.com/getsms-online/get.sms.online-python

**MiroFish.** A Simple and Universal Swarm Intelligence Engine, Predicting Anything:

🔗 https://github.com/666ghj/MiroFish

**Hiddify.** A multi-platform proxy client based on [Sing-box](https://github.com/SagerNet/sing-box) universal proxy tool-chain. Hiddify offers a wide range of capabilities, like automatic node selection, TUN mode, remote profiles etc. Hiddify is ad-free and open-source. With support for a wide range of protocols, it provides a secure and private way for accessing free internet:

🔗 https://github.com/hiddify/hiddify-app

**Transmission** is a fast, easy, and free BitTorrent client. It comes in several flavors: A native macOS GUI application, GTK+ and Qt GUI applications for Linux, BSD, etc, A Qt-based Windows-compatible GUI application, A headless daemon for servers and routers, A web UI for remote controlling any of the above:

🔗 https://github.com/transmission/transmission

**GuardDog** is a CLI tool to Identify malicious PyPI and npm packages:

🔗 https://github.com/DataDog/guarddog

----

## 🤖 Universal Search & AI

**Webwright.** A simple SWE style browser agent framework that achieves SOTA results on long horizon web tasks:

🔗 https://github.com/microsoft/Webwright

**Postiz.** An alternative to Buffer.com, Hypefury, Twitter Hunter, etc. Postiz offers everything you need to manage your social media posts, build an audience, capture leads, and grow your business:

🔗 https://github.com/gitroomhq/postiz-app

**Free LLM API.** OpenAI-compatible proxy that aggregates free-tier keys from ~14 AI providers with automatic failover. For personal experimentation only:

🔗 https://github.com/tashfeenahmed/freellmapi

**Agent Skills for Marketing** - SEO, Social, Influencer & More. 160+ open-source skills for SEO, content, 40+ page types, paid ads, channels, and strategies. Add project context; get tailored, production-ready output. Cursor, Claude Code, OpenClaw - no lock-in:

🔗 https://github.com/kostja94/marketing-skills

**Alibaba Page Agent.** JavaScript in-page GUI agent. Control web interfaces with natural language:

🔗 https://github.com/alibaba/page-agent

**Adala** is an **A**utonomous **DA**ta (**L**abeling) **A**gent framework. Adala offers a robust framework for implementing agents specialized in data processing, with an emphasis on diverse data labeling tasks. These agents are autonomous, meaning they can independently acquire one or more skills through iterative learning. This learning process is influenced by their operating environment, observations, and reflections. Users define the environment by providing a ground truth dataset. Every agent learns and applies its skills in what we refer to as a "runtime", synonymous with LLM:

🔗 https://github.com/HumanSignal/Adala

**Hindsight.** Agent Memory That Learns:

🔗 https://github.com/vectorize-io/hindsight

**mb: mini-browser for Agents.** Browser CLI for agents. Each command is a small Unix tool - reads args, writes stdout, composes with pipes and `&&`:

🔗 https://github.com/runablehq/mini-browser

**ReMe.** Memory Management Kit for Agents - Remember Me, Refine Me:

🔗 https://github.com/agentscope-ai/ReMe

**CyberStrikeAI** is an AI-native security testing platform built in Go. It integrates 100+ security tools, an intelligent orchestration engine, role-based testing with predefined security roles, a skills system with specialized testing skills, and comprehensive lifecycle management capabilities:

🔗 https://github.com/Ed1s0nZ/CyberStrikeAI

**RocketRide.** High-performance AI pipeline engine with a C++ core and 50+ Python-extensible nodes. Build, debug, and scale LLM workflows with 13+ model providers, 8+ vector databases, and agent orchestration, all from your IDE. Includes VS Code extension, TypeScript/Python SDKs, and Docker deployment:

🔗 https://github.com/rocketride-org/rocketride-server

**Stop Slop.** A skill file for removing AI tells from prose:

🔗 https://github.com/hardikpandya/stop-slop

----

## 👨‍💻 Software Development & APIs

AI Pair Programming in Your Terminal. **Aider** lets you pair program with LLMs to start a new project or build on your existing codebase:

🔗 https://github.com/Aider-AI/aider

**SchemaSpy** is a database metadata analyzer. It helps your database administrators and developers visualize, navigate and understand your data model. With an easy-to-use HTML-based report, traversing the entity-relationship diagram has never been simpler:

🔗 https://github.com/schemaspy/schemaspy

**pgGraph.** Open-source graph database superpowers for your existing Postgres data:

🔗 https://github.com/Evokoa/pgGraph

**TheSVG.** 5,880+ brand SVG icons for developers. Tree-shakeable, typed, open source. npm i thesvg:

🔗 https://github.com/glincker/thesvg

Official source code of **FreeCAD**, a free and opensource multiplatform 3D parametric modeler:

🔗 https://github.com/FreeCAD/FreeCAD

**Otel GUI.** A lightweight, zero-config OpenTelemetry trace viewer for local development:

🔗 https://github.com/metafab/otel-gui

----

## 🐧 Linux & DevOps

**Stalwart.** All-in-one Mail & Collaboration server. Secure, scalable and fluent in every protocol (IMAP, JMAP, SMTP, CalDAV, CardDAV, WebDAV):

🔗 https://github.com/stalwartlabs/stalwart

**AirPipe.** Self-hosted file transfer with a passphrase that works anywhere. Files go peer-to-peer between any two devices. The relay never sees your bytes:

🔗 https://github.com/Sanyam-G/Airpipe

**Zero Password Manager.** Open-source self-hosted password manager built with Flutter. Store passwords and crypto seed phrases securely without cloud storage:

🔗 https://github.com/SoulNaturalist/zero_password_manager

**Kaku.** A fast, out-of-the-box terminal built for AI coding:

🔗 https://github.com/tw93/kaku

----

## 🔌 Hardware & Devices

**PromptZero** is a natural-language operator for the Flipper Zero. Talk to it like you'd talk to a person - it generates payloads, deploys them, and runs them, all from a single sentence:

🔗 https://github.com/xunholy/promptzero

----

## 🚨 From CyberDetective

**BraveDown.** There are plenty of free online tools for downloading content from various social media platforms. TikTok, Twitter, VK, Odnoklassniki, Weibo, Threads and others:

🔗 https://bravedown.com/

----
## 📌 Where to Follow

- **Substack:** https://osintech.substack.com  
- **LinkedIn:** https://www.linkedin.com/in/osintech/details/featured/

If this timeline saves you time, it’s doing its job.  
Free to read. Manually curated. Minimal noise.

---

## 📌 Donates

[![Buy Me a Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/osintech)

---

## 📌 Legal and ethical note

All tools and techniques documented in the dataset are presented for informational,  
educational and information security purposes only.

The dataset does not promote or endorse illegal activities.  
Users are responsible for complying with applicable laws and ethical standards.

---

## 📌 About future updates

The dataset is updated on a regular basis.  
Future posts will document changes, notable additions and emerging trends observed within the dataset.

This post serves as an introduction and reference point for those updates.
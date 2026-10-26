# WhatsApp Tools, Articles, and Resources

Compiled from **185 timeline issues published between April 6, 2023 and October 22, 2026**. Duplicate resource links are consolidated. Descriptions reflect historical timeline entries; current availability, compatibility, prices, and effectiveness have not been verified.

Includes direct WhatsApp tools and clearly marked related integrations. Historical security claims are descriptions of the source entries.

**Sources** link to the original timeline files; each label gives the issue number and source line. A resource may appear in more than one topic collection when relevant.

This collection contains **27 resources** in **5 sections**.

## Contents

- [Profile Research, Activity Analysis, and Forensics](#1-profile-research-activity-analysis-and-forensics)
- [Clients, APIs, and Automation](#2-clients-apis-and-automation)
- [Connectivity and Related Integrations](#3-connectivity-and-related-integrations)
- [Security Research and Monitoring Tools](#4-security-research-and-monitoring-tools)
- [Directories](#5-directories)

## 1. Profile Research, Activity Analysis, and Forensics

| Resource | Description | Sources |
|---|---|---|
| [WhatsApp Spy / whatsapp-osint](https://github.com/jasperan/whatsapp-osint) | Tool described as logging WhatsApp online and offline events. | [17:53](timelines/osintech-timeline_17_27.07.2023.md) |
| [WhatsApp Profile Lookup](https://whatsapp.checkleaked.cc) | Look up profile information by phone number, including identifiers, description, contact information, website, and location, as described in the timeline. | [75:84](timelines/osintech-timeline_75_12.09.2024.md) |
| [Profile Image Intel](https://profileimageintel.com/) | Display profile photo update dates for WhatsApp and Facebook; the timeline presents these as potential clues when investigating account history. | [103:33](timelines/osintech-timeline_103_27.03.2025.md) |
| [WhatsApp Web Analyzer / whatsthat](https://github.com/markrai/whatsthat) | Chrome extension for analyzing group chat dynamics through reactions and replies, including influence and interaction patterns. | [134:41](timelines/osintech-timeline_134_30.10.2025.md) |
| [Device Activity Tracker](https://github.com/gommzystudio/device-activity-tracker) | A phone number can reveal whether a device is active, in standby or offline (and more). This PoC demonstrates how delivery receipts + RTT timing leak sensitive device-activity patterns. (WhatsApp / Signal) | [141:37](timelines/osintech-timeline_141_18.12.2025.md) |
| [WhatsApp Device Activity Tracker](https://github.com/Xh4H/WhatsApp-device-activity-tracker) | Implementation of the Careless Whisper research on monitoring device activity through silent delivery receipts. | [148:128](timelines/osintech-timeline_148_05.02.2026.md) |
| [Whats-reader](https://github.com/rodrigogs/whats-reader) | Browse WhatsApp chat exports offline with AI-powered voice transcription. Privacy-first desktop/web app with bookmarks, search, and statistics. Built with SvelteKit and Electron | [142:41](timelines/osintech-timeline_142_25.12.2025.md) |
| [Whapa](https://github.com/B16f00t/whapa) | is a set of graphical forensic tools to analyze whatsapp from Android and soon iOS devices. All the tools have been written in Python 3.8 and have been tested on linux, windows and macOS systems | [151:102](timelines/osintech-timeline_151_26.02.2026.md) |
| [WhatsApp-OSINT](https://github.com/kinghacker0/WhatsApp-OSINT) | OSINT tool for WhatsApp that allows you to obtain profile pictures, verify Business accounts, check status and user information, analyze linked devices, review privacy settings, and access complete data using the RapidAPI WhatsApp OSINT API. Supports 6 endpoints | [151:106](timelines/osintech-timeline_151_26.02.2026.md) |

## 2. Clients, APIs, and Automation

| Resource | Description | Sources |
|---|---|---|
| [Whatsmeow](https://github.com/tulir/whatsmeow) | is a Go library for the WhatsApp web multidevice API | [107:67](timelines/osintech-timeline_107_24.04.2025.md) |
| [Whatsapp-Web.js](https://github.com/pedroslopez/whatsapp-web.js) | A WhatsApp client library for NodeJS that connects through the WhatsApp Web browser app | [128:90](timelines/osintech-timeline_128_18.09.2025.md) |
| [WAHA](https://github.com/devlikeapro/waha) | WhatsApp HTTP API (REST API) that you can configure in a click! 3 engines: WEBJS (browser based), NOWEB (websocket nodejs), GOWS (websocket go) | [133:61](timelines/osintech-timeline_133_23.10.2025.md) |
| [Whatomate](https://github.com/shridarpatil/whatomate) | is an open-source WhatsApp integration | [146:45](timelines/osintech-timeline_146_22.01.2026.md) |
| [GOWA](https://github.com/aldinokemal/go-whatsapp-web-multidevice) | WhatsApp REST API with support for UI, Multi Account, Webhooks, and MCP, and Chatwoot. Built with Golang for efficient memory use | [151:154](timelines/osintech-timeline_151_26.02.2026.md) |
| [Kapso](https://kapso.ai/) | WhatsApp API for developers | [152:141](timelines/osintech-timeline_152_05.03.2026.md) |
| [OpenClaw WhatsApp Integration via Kapso](https://github.com/Enriquefft/openclaw-kapso-whatsapp) | Connect an OpenClaw agent to a WhatsApp number through the Meta Cloud API via Kapso. | [152:145](timelines/osintech-timeline_152_05.03.2026.md) |
| [OpenWA](https://github.com/rmyndharis/OpenWA) | Free, Open Source, Self-Hosted WhatsApp API Gateway | [163:158](timelines/osintech-timeline_163_21.05.2026.md) |
| [wacli — Scriptable WhatsApp Client](https://github.com/openclaw/wacli) | Link as a WhatsApp Web device, mirror messages into SQLite, search offline, send messages, and manage chats, groups, and contacts from the CLI. Other source links: [1](https://github.com/tulir/whatsmeow). | [166:42](timelines/osintech-timeline_166_11.06.2026.md) |
| [Wechaty](https://github.com/wechaty/wechaty) | is a conversational RPA SDK that simplifies the process of building chatbots. It's like a Swiss Army knife for chatbot development, providing a universal interface to various messaging platforms such as WhatsApp, WeChat, and more. With Wechaty, you write your bot code once, and it runs on any of the supported platforms. This means you can focus on creating engaging conversational experiences without worrying about the underlying complexities of each platform's API. It's open-source, easy to use, and backed by a vibrant community that's ready to help you bring your chatbot ideas to life | [180:139](timelines/osintech-timeline_180_17.09.2026.md) |

## 3. Connectivity and Related Integrations

| Resource | Description | Sources |
|---|---|---|
| [WhatsApp Proxy](https://github.com/WhatsApp/proxy/) | This repository contains the WhatsApp proxy implementation for users to host their own proxy infrastructure to connect to WhatsApp for chat (VoIP is not currently supported) | [42:21](timelines/osintech-timeline_42_25.01.2024.md) |
| [Matterbridge](https://github.com/42wim/matterbridge) | Bridge between mattermost, IRC, gitter, xmpp, slack, discord, telegram, rocketchat, twitch, ssh-chat, zulip, whatsapp, keybase, matrix, microsoft teams, nextcloud, mumble, vk and more with REST API (mattermost not required!) | [88:72](timelines/osintech-timeline_88_12.12.2024.md) |
| [Dittofeed](https://github.com/dittofeed/dittofeed) | Open-source customer engagement. Automate transactional and marketing messages across email, SMS, mobile push, WhatsApp, Slack, and more | [95:87](timelines/osintech-timeline_95_30.01.2025.md) |
| [Get SMS Online — Python Client](https://github.com/getsms-online/get.sms.online-python) | Receive SMS messages and verification codes programmatically, including for WhatsApp and Telegram. Other source links: [1](https://getsms.online/). | [164:150](timelines/osintech-timeline_164_28.05.2026.md) |

## 4. Security Research and Monitoring Tools

| Resource | Description | Sources |
|---|---|---|
| [Whatsapp Exploit](https://github.com/lichti/whats-spoofing) | to spoofing impersonate of reply message | [59:49](timelines/osintech-timeline_59_23.05.2024.md) |
| [WhatsApp Spy](https://github.com/wellrodrig/Whatsapp-Spy) | is an app designed to monitor and log all on-screen texts whenever a user opens WhatsApp / Whatsapp Business. It also supports Instagram and Messenger, sending logs to either Discord or Telegram, without port forwarding | [87:49](timelines/osintech-timeline_87_05.12.2024.md) |
| [Graphite](https://www.blackhatethicalhacking.com/news/israeli-spyware-graphite-exploits-whatsapp-0-click-attack-uncovered/) | Cybersecurity researchers at Citizen Lab, a digital rights watchdog based at the University of Toronto, have exposed the use of a highly sophisticated spyware tool named Graphite. Developed by Israeli cybersecurity firm Paragon Solutions, Graphite was deployed to target high-profile individuals, including journalists and human rights activists, by exploiting a zero-day vulnerability in WhatsApp | [103:15](timelines/osintech-timeline_103_27.03.2025.md) |

## 5. Directories

| Resource | Description | Sources |
|---|---|---|
| [Social Media OSINT Tools](https://www.osintguide.com/en/tools/category/social-media) | 597 tools list - Facebook, Twitter X, Instagram, Youtube, People Search Engines, TikTok, Pinterest, Reddit, VKontakte, WhatsApp, Tumblr, LinkedIn, Telegram, Twitch, Mastodon | [174:123](timelines/osintech-timeline_174_06.08.2026.md) |

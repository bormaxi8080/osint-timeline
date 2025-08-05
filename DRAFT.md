
I'm like a chronicle. I'm like Chthon. I've always been like this. Serebryansky forest. Verdun. Tin cans with nails. Optical fiber getting into flour.


Living in a society poisoned by propaganda, sooner or later everyone will become infected.


Digital Gleichschaltung.


Faces of God.

----

```OSINT Repos List```, Repository with gathered from GitHub utilities for OSINT, Development and DevOps. The number of artifacts in the repository exceeded 2800: https://github.com/bormaxi8080/osint-repos-list

----

Hacking Nuclear Reactors using eBay and reverse engineering: cyber-physical attacks on Nuclear Power Plants (NPPs). 
  
Security researcher Ruben Santamarta shared his fundamental (and one-of-a-kind) research on the cybersecurity of nuclear power plants a few months ago - 138 pages of scary but fascinating findings.  
  
As the author wrote, the analysis and the security issues described are purely hypothetical - because it's a nuclear reactor! The mind-blowing fact for me was that someone can buy nuclear plant equipment on eBay. Crazy - and quite alarming.  
  
Please enjoy the read and spread the word - offensive security research has officially come to nuclear plants.  
  
More details:

Paper. A Practical Analysis of Cyber-Physical Attacks Against Nuclear Reactors: https://drive.google.com/file/d/1qe_nBH1ACDX2ydmzcIhJnbdRGnoDvVfP/view?pli=1

Presentation: When Physics Meets (Reverse) Engineering. Understanding Cyber-Physical Attacks Against Nuclear Reactors: chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://2024.swisscyberstorm.com/2024/10/22/ruben-santamarta.pdf

----

New UNISHKA OSINT for Countries:

OSINT of Belarus: https://unishka.substack.com/p/osint-of-belarus

OSINT of Lebanon: https://substack.com/home/post/p-166578494

OSINT of Iraq: https://unishka.substack.com/p/osint-of-iraq

OSINT of Nigeria: https://unishka.substack.com/p/osint-of-nigeria

OSINT of Syria: https://unishka.substack.com/p/osint-of-syria

----

**OSINT Tools, Services and Investigations:**

The OSINT Rack. Curated intelligence resources: https://www.mariosantella.com/the-osint-rack/

Slideshare Search. Discover presentations, documents, infographics, useful for gathering insights about people and companies: https://www.slideshare.net/search

Talkwalker OSINT Tool. An AI-powered platform for monitoring threats, analyzing public data, and making informed decisions by tracking millions of online sources: https://www.talkwalker.com/osint-tool

Maps Video. Private street view video libraries using action cameras: https://maps.video/map

Binwalk can identify, and optionally extract, files and data that have been embedded inside of other files: https://github.com/ReFirmLabs/binwalk

Kingfisher is a blazingly fast secret‑scanning and validation tool built in Rust: https://github.com/mongodb/kingfisher

----

**Universal Search & AI:**

"Cursor for Design". SuperDesign is the first **open-source design agent** that lives right inside your IDE. Generate UI mockups, components, and wireframes directly from natural language prompts. Works seamlessly with Cursor, Windsurf, Claude Code, and plain VS Code: https://github.com/superdesigndev/superdesign

HASH is a self-building, open-source database which grows, structures and checks itself. HASH integrates data in (near-)realtime, and provides a powerful set of interfaces so that information can be understood and used in any context. Intelligent, autonomous agents can be deployed to grow, check, and maintain the database, integrating and structuring information from the public internet as well as your own connected private sources. And users, including those who are non-technical, are able to visually browse and manage both entities (data) and types (schemas). HASH acts as a source of truth for critical data, no matter its source, and provides a platform for high-trust, safety-assured decision-making: https://github.com/hashintel/hash

Volt Agent. Open Source TypeScript AI Agent Framework: https://github.com/VoltAgent/voltagent

Token Limit. Monitor how many tokens your code and configs consume in AI tools. Set budgets and get alerts when limits are hit: https://github.com/azat-io/token-limit

Tree of Thoughts. Deliberate Problem Solving with Large Language Models: https://github.com/princeton-nlp/tree-of-thought-llm

Magic. The first open-source all-in-one AI productivity platform (Generalist AI Agent + Workflow Engine + IM + Online collaborative office system): https://github.com/dtyq/magic

----

**Software Development & APIs:**

Palanteer. Visual Python and C++ nanosecond profiler, logger, tests enabler: https://github.com/dfeneyrou/palanteer

BotCommander is a simple and convenient web interface for managing multiple Python bots. Each bot is isolated in its own directory with a virtual environment (venv). The interface shows the status, CPU/RAM load, uptime, and also allows you to start, stop, restart and disable bots: https://github.com/RuinasHistori/BotCommander

DOSBox Staging is a modern continuation of DOSBox with advanced features and current development practices: https://github.com/dosbox-staging/dosbox-staging

----

**Linux & DevOps:**

Telert. Command‑line and Python utility that alerts on command completion, code execution and system monitoring events: https://github.com/navig-me/telert

--

KDiskMark is an HDD and SSD benchmark tool with a very friendly graphical user interface. KDiskMark with its presets and powerful GUI calls [Flexible I/O Tester](https://github.com/axboe/fio) and handles the output to provide an easy to view and interpret comprehensive benchmark result. The application is written in C++ with Qt and _doesn't have_ any KDE dependencies: https://github.com/JonMagon/KDiskMark

Download: https://snapcraft.io/kdiskmark

--

FakeSNI. 

A program for bypassing blocking by modifying the SNI field in the TLS protocol.

Currently, most Russian providers have switched to using DPI filters. In the case of connections via the HTTPS protocol, almost all exchange with the remote server is encrypted. To determine the recipient, the filter has access to two connection parameters: the IP address and the ServerName field in the ClientHello request. For a number of reasons, filtering by IP address does not work well in practice, so ServerName is usually checked as a more reliable method. Modern browsers always add SNI and, accordingly, openly send ServerName.

However, the TLS 1.2 protocol allows not adding SNI to the client request at all.

In this case, the server must assume a connection to one of the served sites by default. All provider filters tested by the author currently allow requests with missing SNI. Sometimes it is possible to send a fake value for better disguise.

Unfortunately, it is impossible to remove or replace SNI by changing browser settings, even with the help of extensions. This program communicates with the site via connections initialized by ClientHello with a fake ServerName value.
In order to be able to view pages, the program locally starts a web server that relays responses. Thus, the browser can communicate with the site via the address http://127.0.0.1:10000/

https://github.com/stopcenz/fakesni

----

**Flipper Zero & Other Devices:**

USB HID AutoFire. Simple Flipper Zero application to send left-clicks as a USB HID device: https://github.com/pbek/usb_hid_autofire

----

**New from CyberDetective:**

DuckDuckGo now has a filter to hide AI-generated images from image search results. Hopefully, this feature will soon become a standard for all search engines and for all types of searches: https://duckduckgo.com/duckduckgo-help-pages/results/how-to-filter-out-ai-images-in-duckduckgo-search-results

Reverse Image Searching Related Sites & Links List by UK OSINT: Reverse Image Searching, Using AI To Identify A Location Shown In An Image, Facial Reverse Image Searching On Social Media, Remove Image Background and more: https://www.uk-osint.net/reverseimagesearching.html

----

**New from GitHub Community:**

Barrier. Eliminate the barrier between your machines: https://github.com/debauchee/barrier/releases

LogoCreator. A free + OSS logo generator powered by Flux on Together AI: https://github.com/Nutlope/logocreator

----
### bormaxi8080 OSINT timeline:

GitHub: [https://github.com/bormaxi8080/osint-timeline](https://github.com/bormaxi8080/osint-timeline)

LinkedIn: [bormaxi8080 OSINT Featured Timeline](https://www.linkedin.com/in/osintech/details/featured/)

You can see Systematized list of my [GitHub Starred OSINT Repositories](https://github.com/bormaxi8080/osint-repos-list)

and contact me on SubStack: [https://osintech.substack.com](https://osintech.substack.com)

----

If you like the projects that I do, I will be grateful for donations in private dialogue.

----

WARNING! All tools, programs and techniques published in this article and repository are used for informational, educational purposes or for information security purposes. The authors are not responsible for the activities that users of these tools and techniques may carry out, and urge them not to use them to carry out harmful or destructive activities directed against other users or groups on the Internet.

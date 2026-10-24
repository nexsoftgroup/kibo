<p align="center">
  <img src="img/kibo.png" alt="Kibo" width="96">
</p>

<h1 align="center">Kibo</h1>

<p align="center">
  <b>Many AI agents. One place.</b><br>
  Your Claude Code agents working at the same time, as a team, with their console, files and tasks in plain sight.
</p>

<p align="center">
  <a href="https://kibo.nexsoftgroup.com"><b>Download</b></a> ·
  <a href="https://kibo.nexsoftgroup.com/docs/">Docs</a> ·
  <a href="CHANGELOG.md">Changelog</a> ·
  <a href="https://github.com/nexsoftgroup/kibo/issues/new/choose">Report a problem or suggest an idea</a>
</p>

<p align="center">
  Free · 100% local · No telemetry · Never reads your credentials · Version 1.0.0 (beta)
</p>

<p align="center">
  <a href="README.md">Español</a> · <b>English</b>
</p>

![Kibo with four Claude Code sessions working at the same time, and an Agent Hub team card](img/portada.png)

> **This repository is Kibo’s public home:** an overview, the changelog and the place to leave your feedback.
> The full details, more screenshots and the documentation are at **[kibo.nexsoftgroup.com](https://kibo.nexsoftgroup.com)**
> (in Spanish for now; your browser can translate it).
> The source code is not published here, and Kibo is downloaded **only** from that site.
> The app itself speaks English, Spanish and Brazilian Portuguese.

---

## What Kibo is

AI agents already write code, research and document. The hard part is coordinating them. Kibo is a desktop app that
turns separate **Claude Code** sessions into **a team that works together**, in plain sight and on your own computer.

- **A team, not loose tabs.** Each project has its MAIN, which hands out the work to the agents and answers you
  briefly. You talk to the team; you don’t have to go session by session.
- **Many agents, in plain sight.** While one writes the code, another runs the tests and another documents. You see
  whether each one is working, waiting for you or asking for permission.
- **Nothing gets lost.** Every conversation, screenshot and decision stays on your computer, and a self-writing Wiki
  lets the next agent start from what the previous one found out.

## What it does

### Agent Hub: your agent teams at a glance

![Agent Hub: one card per team, the team map and the team chat](img/agent-hub.png)

- **One card per team:** each project with its MAIN, its agents and how many are working or waiting for you.
- **The team chat:** talk to everyone, to one agent or to several teams, with **Order** or **Ask**.
- **You still approve the permissions.**

### Many agents, all at once

![A 2 × 2 grid with four Claude Code sessions at the same time](img/cuadricula.png)

- Several Claude Code sessions on the same screen, each one on its own job.
- Split the area the way you need (2 columns, 2 rows, 2 × 2, 3 × 2) or drag a tab to an edge.
- Every session is real Claude Code, with your account and its usual permissions.

### Conversation history and a self-writing Wiki

![The session conversation, each message with its time, next to its console](img/conversacion.png)

- **Go back to what was said by date** (“what we talked about yesterday between 2 and 6 pm”) and the agent catches up.
- **A Wiki per project**, in Markdown: what the agents find out ends up in notes, separating what is confirmed from
  what still needs checking. Read it in Kibo, in any editor or in Obsidian.
- **Ctrl+K** searches projects, agents, tasks and everything that was said.

### Scheduled tasks: work goes on while you’re away

![The scheduled tasks panel and the form to schedule one](img/tareas.png)

- At the time you choose, Kibo opens the session and **types the instruction**, as if you had typed it.
- It runs even with Kibo closed: Windows Task Scheduler, systemd or cron on Linux, and launchd on macOS.

### And also

| | |
|---|---|
| **Point at the web** | With the Chrome and Edge extension you mark an element or an area, and the session gets the screenshot, the HTML and the console errors. |
| **Instant screenshots** | Paste or drag a screenshot, mark it with arrows and boxes, and it reaches the agent. |
| **Editor and VS Code** | Project files with the VS Code editor, and full VS Code in a tab if you want it. |
| **Shortcuts for everything** | In their own window (Ctrl+Alt+S), with search. |
| **Servers over SSH** | Sessions running on another machine. SSH keys only: passwords are never stored. |
| **Themes and languages** | Kibo, Dark and Light. In English, Spanish and Brazilian Portuguese. |
| **Desktop notifications** | Optional: when an agent finishes or needs you. |

👉 **[All features, with screenshots, on the website](https://kibo.nexsoftgroup.com/docs/funciones)** (in Spanish)

## Install

Kibo is downloaded **only** from [kibo.nexsoftgroup.com](https://kibo.nexsoftgroup.com). The current version is always
there, with its size, date and SHA-256.

**Windows** (recommended): open PowerShell, paste this and press Enter.

```powershell
irm https://kibo.nexsoftgroup.com/install.ps1 | iex
```

**Linux and macOS** (macOS is experimental): open a terminal, paste this and press Enter.

```sh
curl -fsSL https://kibo.nexsoftgroup.com/install.sh | sh
```

The command asks which AI you will work with, asks for permission before installing anything missing, downloads Kibo
from the site and **checks it is ours (SHA-256)** before installing it. It speaks English, Spanish or Portuguese,
following your system language. On Windows there is also a double-click installer on the site.

### What you need

| System | Status | Needs |
|---|---|---|
| **Windows 10 / 11** (64-bit) | Supported | WebView2 (comes with Windows), Git for Windows and Claude Code. The terminal command installs what is missing, if you allow it. |
| **Linux** | Tested on Ubuntu 24.04 (WSL) | Python 3.11+, the system’s GTK, WebKit2GTK and PyGObject, and Claude Code. |
| **macOS** | Experimental | Python 3.11+ and Claude Code. |

**Claude Code**, installed and with **your own session signed in**. Kibo doesn’t include or resell it, and never reads
your credentials: you sign in yourself.

> **Beta: try it with Claude Code.** Kibo is built and fully tested with Claude Code. The plan is for it to work with
> more AI agents later on.

## Privacy

Kibo has no server of its own, no accounts, no telemetry and no cloud backup, and never reads your credentials.
Conversations, attachments and settings stay on your computer. What goes out to the internet is what Claude Code
already sends to Anthropic, plus whatever you turn on (checking for new versions, downloading VS Code).

[Privacy policy](https://kibo.nexsoftgroup.com/privacidad) ·
[Security and verification](https://kibo.nexsoftgroup.com/seguridad) ·
[Terms of use](https://kibo.nexsoftgroup.com/terminos)

## Feedback, problems and ideas

Kibo is in beta and your feedback helps us a lot. Write in English or Spanish, whichever you prefer.

- **Something not working?** [Report a problem](https://github.com/nexsoftgroup/kibo/issues/new?template=problema.yml).
  Tell us your Kibo version, your system and the steps to make it happen.
- **Have an idea?** [Suggest it](https://github.com/nexsoftgroup/kibo/issues/new?template=idea.yml).

Before pasting logs or screenshots, check they don’t contain passwords, tokens or customer data.

---

<p align="center">
  Kibo is a tool we built at <a href="https://nexsoftgroup.com"><b>NexSoft</b></a> and share for free.<br>
  <sub>Claude Code is a trademark of Anthropic. Kibo is not an Anthropic product.</sub>
</p>

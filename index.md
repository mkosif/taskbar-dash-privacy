# Taskbar Dash Privacy Policy

Last updated: November 4, 2026

Taskbar Dash ("the app") is published by Mustafa Kosif. This policy explains what the app does with your data.

## The short version

- The developer collects nothing. The app has no analytics, no tracking, no ads and no developer server.
- Everything the app stores stays on your computer.
- The app reads nothing from an AI service until you connect it in **Settings > AI usage**, and you choose how. Plugins you add yourself run as you and can connect wherever their program does.

## What the app connects to

The app shows your usage limits for AI services. It touches none of them until you connect a service in **Settings > AI usage**, where you pick one way per service. The app uses only that way and never switches to another by itself.

- **Claude**, one of:
  - *Through Claude Code:* with your OK, the app adds one `statusLine` entry to Claude Code's settings (`~/.claude/settings.json`, backed up first; a status line you already had keeps working). Claude Code then hands the app your usage percent and reset times, which it saves in a file on your computer. No sign-in is read and the app connects to nothing.
  - *With Claude Code's sign-in:* the app reads the sign-in that Claude Code keeps on your computer and asks Anthropic's server (`api.anthropic.com`) for your usage limits. It never renews, changes or copies that sign-in.
  - *Sign in with Claude:* you sign in on Claude's own page in your web browser (`claude.com`). The app then talks to Anthropic's servers (`platform.claude.com`, `api.anthropic.com`) to keep you signed in and read your usage limits.
- **ChatGPT**, one of:
  - *Through Codex:* the app asks the Codex command-line tool on your computer for your limits. Codex talks to OpenAI with its own sign-in; the app never reads that sign-in.
  - *From Codex logs:* the app reads the usage figures in the session files Codex keeps on your computer (`~/.codex/sessions`). It connects to nothing.
  - *Sign in with ChatGPT:* you sign in on OpenAI's own page in your web browser (`auth.openai.com`). The app then talks to OpenAI's servers (`auth.openai.com`, `chatgpt.com`) to keep you signed in and read your usage limits.
- **Grok**, one of:
  - *With Grok Build's sign-in:* the app reads the sign-in that the Grok command-line tool keeps on your computer and asks xAI's server (`cli-chat-proxy.grok.com`) for your usage. It never renews, changes or copies that sign-in.
  - *Sign in with xAI:* you sign in on xAI's own pages in your web browser (`auth.x.ai`, `accounts.x.ai`). The app then talks to xAI's servers (`auth.x.ai`, `cli-chat-proxy.grok.com`) to keep you signed in and read your usage.

These requests go straight from your computer to the service. The developer never sees them. Each service handles your data under its own privacy policy:

- Anthropic: https://www.anthropic.com/legal/privacy
- OpenAI: https://openai.com/policies/privacy-policy
- xAI: https://x.ai/legal/privacy-policy

The app also makes connections you set up yourself:

- **Custom widgets** are plugins: the app runs only the plugin programs you put in the plugins folder (`Documents\Taskbar Dash\plugins`), and only after you trust each one. A plugin runs as you, so it can do what any program you start can do; add only plugins you trust.
- **Developer feed:** programs you run can send values to their widgets over a local channel that only your own Windows sign-in can open. Nothing leaves your PC.

While you sign in, the app listens on your own computer only (the loopback addresses `127.0.0.1` and `::1`) for the browser to hand back the sign-in; nothing outside your computer can reach it. If xAI's page shows you a code instead, you can paste it into the app. To check your licence and whether a newer version is available, the app asks the Microsoft Store on your computer (see Purchases); an update is installed only when you choose Update. The app connects to nothing else. Connections to Anthropic, OpenAI and xAI use HTTPS.

## What the app stores on your computer

All of it is kept in one folder, where you can open and inspect it. The Microsoft Store version keeps it in its own package storage, `%LOCALAPPDATA%\Packages\mkosif.TaskbarDash_wmz684ne5d16e\LocalCache\Local\TaskbarDash` (Windows shows it to the app as `%LOCALAPPDATA%\TaskbarDash`; if that real folder already exists, for example from an earlier copy outside the Store, the app uses it instead). A copy from outside the Store uses `%LOCALAPPDATA%\TaskbarDash`.

- **Claude, ChatGPT and Grok sign-ins**, only if you chose a "Sign in with" way: each encrypted with Windows data protection, so only your Windows account can read them.
- **Claude usage from Claude Code**, only if you chose "Through Claude Code": your last usage percent and reset times, and the status line you had before, so Disconnect can put it back.
- **Update notice:** the last version the app told you about, so it tells you only once.
- **Settings:** which widgets you show, where they sit and where the app's windows were.
- **Today's network totals:** how many bytes your computer downloaded and uploaded since midnight, for the network widgets.
- **Developer feed widgets:** the names, units and looks that programs declared for their widgets, so an added widget keeps them while its program is off.
- **Licence state:** what the Microsoft Store last said about your licence (for example, when the free trial ends), a short log of the last licence check, and whether the "trial has ended" notification was already shown.
- **Log files:** start-up and error messages. They never contain passwords or sign-in tokens, and they are capped at a small size.

The app reads the files of Claude Code, Codex or Grok only for the way you chose, and changes none of them, except the one `statusLine` entry described above, which Disconnect removes.

Taskbar Dash also shows system information such as CPU, memory, GPU and running programs. It reads this on your computer and never sends it anywhere.

## Sharing

The developer receives none of your data, so there is nothing to share or sell.

## Removing your data

- **Disconnect:** go to **Settings > AI usage**. Disconnect stops all access to that service, deletes its stored sign-in, and for "Through Claude Code" removes the `statusLine` entry and puts back the one you had.
- **Remove everything:** uninstall the app. Uninstalling the Microsoft Store version deletes its package storage; delete the `%LOCALAPPDATA%\TaskbarDash` folder if it is still there. The plugins folder, `Documents\Taskbar Dash\plugins`, holds your own files and stays until you delete it.

## Purchases

Purchases and free trials are handled by the Microsoft Store under Microsoft's privacy statement: https://privacy.microsoft.com/privacystatement. The app checks your licence through Windows' own Microsoft Store service, which may contact Microsoft; the app only learns whether you are in the free trial, have bought the app, or the trial has ended. The developer receives no payment details.

## Children

The app is not directed at children and collects no data from anyone.

## Changes

If this policy changes, the new version is posted at this address with a new date.

## Contact

Questions: kosif.mustafa@outlook.com

# TokenMeter

A macOS menu bar app that shows your **Claude** and **ChatGPT** plan usage at a glance.

![macOS](https://img.shields.io/badge/macOS-13%2B-blue) ![signed](https://img.shields.io/badge/Apple-notarized-success)

## Install

1. **[Download `TokenMeter.dmg`](https://github.com/fabianrasch/tokenmeter/releases/latest)**
2. Double-click the DMG → drag `TokenMeter` into `Applications`
3. Launch from Applications. The gauge icon appears in your menu bar.

Apple-signed and notarized — no Gatekeeper warning.

## What it shows

- **Session (5h)** and **Weekly** remaining capacity for each plan
- Reset times — so you know exactly when your window rolls over
- **Left-click** the gauge → popover with live values
- **Right-click** the gauge → log in / sign out / quit / check for updates
- Pin button → detached floating window (always-on-top, draggable)
- Slider icon → toggle Claude / ChatGPT independently

> The ChatGPT block reflects your **OpenAI plan token pool** — ChatGPT Plus/Pro
> and Codex CLI share the same 5h / weekly limits.

## Sign in

Right-click the gauge icon → choose **Log in to Claude** or **Log in to ChatGPT**.

| Provider | Login flow |
|----------|-----------|
| **Claude** | A small browser window opens on `claude.ai/login`. Log in (Google or email). The window closes itself once your session is captured and saved to the macOS Keychain. |
| **ChatGPT** | Runs `codex login` — opens your default browser for OpenAI OAuth. Requires [Codex CLI](https://github.com/openai/codex) installed (it shares the ChatGPT plan token pool). |

No proxy, no API keys.

## Auto-update

TokenMeter checks for new releases once a day. When one's available you'll see a tiny Sparkle dialog — click Install and the app updates itself on quit.

## Privacy

- The Claude session cookie lives in your **macOS Keychain** under `dev.tokenmeter.app`
- The ChatGPT plan data comes from local **Codex CLI session files** (`~/.codex/sessions/*.jsonl`)
- TokenMeter only talks to `claude.ai` (your own session, your own data) and `github.com` (update checks)
- No analytics, no tracking, no third-party services

## License

MIT

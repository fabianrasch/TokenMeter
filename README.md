<div align="center">

<img src="icon.png" width="128" alt="TokenMeter"><br><br>

**Claude + ChatGPT plan usage. Right in your menu bar.**

<br>

[**Download TokenMeter →**](https://github.com/fabianrasch/tokenmeter/releases/latest/download/TokenMeter.dmg)

*macOS 13+ · Apple-signed & notarized*

</div>

<br>

## What it shows

- **Session (5h)** and **Weekly** remaining capacity for each plan
- Reset times — so you know exactly when your window rolls over
- Left-click the gauge for live values; pin it as a floating window
- Toggle Claude / ChatGPT independently

## Sign in

Right-click the gauge → **Log in to Claude** or **Log in to ChatGPT**.

| Provider | How |
|---|---|
| **Claude** | A small browser window opens on `claude.ai/login`. Log in once — your session is saved to the macOS Keychain. |
| **ChatGPT** | Runs `codex login` (requires [Codex CLI](https://github.com/openai/codex)). Shares the ChatGPT plan token pool with Codex. |

No proxy, no API keys.

## Auto-update

Sparkle checks once a day. Updates install themselves on quit.

## Privacy

- Claude session lives in your **macOS Keychain** (`dev.tokenmeter.app`)
- ChatGPT data comes from local **Codex CLI session files** (`~/.codex/sessions/*.jsonl`)
- TokenMeter only talks to `claude.ai` (your own session) and `github.com` (update checks)
- No analytics, no tracking, no third-party services

<br>

---

<div align="center">

This repository hosts the public release binaries and the Sparkle [appcast](appcast.xml).
Application source lives in a private repository.<br>
Found a bug or have a feature request? [Open an issue](https://github.com/fabianrasch/tokenmeter/issues).

<br>

[MIT License](LICENSE)

</div>

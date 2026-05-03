# Security

## Supported

The latest TokenMeter release on this repo is the only supported version.

## Reporting a vulnerability

Please email **fabian.rasch@rootglobal.io** with the details. Include
reproduction steps and, if relevant, the version you observed it on
(`Right-click the gauge → About`).

## Build & distribution integrity

- Releases are signed with **Apple Developer ID `Fabian Rasch (A9248S3UFS)`**
  and **notarized** by Apple. Gatekeeper will reject the binary if either
  signature is missing or has been tampered with.
- Auto-updates are delivered via [Sparkle](https://sparkle-project.org/) and
  verified against an Ed25519 public key embedded in the app
  (`SUPublicEDKey`). Sparkle refuses to install an update whose signature
  doesn't match.

## Privacy boundary

- The Claude session cookie is stored in the macOS Keychain under
  `dev.tokenmeter.app`.
- ChatGPT plan data is read from the local Codex CLI session files
  (`~/.codex/sessions/*.jsonl`) and the OAuth tokens managed by Codex CLI
  (`~/.codex/auth.json`).
- TokenMeter only talks to `claude.ai` (your own session) and `github.com`
  (update checks). No third parties, no analytics.

# CodexSwitchMenu Releases

Download-only distribution for CodexSwitchMenu, a macOS menu-bar account and quota manager.

[Download the latest version](https://github.com/goodbest/CodexSwitchMenuRelease/releases/latest)

- macOS 13 or later; one Universal app for Apple Silicon and Intel Macs.
- Download the ZIP, extract it, and move `CodexSwitchMenu.app` to `/Applications`.
- This personal-use build is ad-hoc signed, not Apple notarized. On first launch,
  macOS may require an explicit approval in System Settings > Privacy & Security > Open Anyway.
  Do not disable Gatekeeper globally.
- If a trusted download is still blocked, first compare its SHA-256 with `SHA256SUMS.txt`
  from the same release. A targeted `xattr -dr com.apple.quarantine /Applications/CodexSwitchMenu.app`
  removes quarantine only from that app. Only do this for a release you trust.
- Version 4.5.0 and later can check for updates inside the app. Automatic checks run
  once a day and can be disabled. Installation requires confirmation by default;
  automatic installation is an optional setting. Updates restart only CodexSwitchMenu,
  not ChatGPT. Older versions need this one-time manual installation.

Update archives and the update feed are signed with an Ed25519 key. System profiling
is disabled. Checking for updates does not upload account credentials, quotas, or logs;
GitHub will still receive ordinary HTTPS request metadata such as the IP address.

This repository contains only distribution documentation and the signed update feed.
Releases contain compiled apps and checksums. Application source, credentials, settings,
backups, logs, and signing private keys are not published here. GitHub's automatic
"Source code" archives contain only this distribution repository, not the application source.

The app bundles [Sparkle](https://sparkle-project.org/) under its included license.
Goal recovery remains experimental; do not rely on it for unattended desktop recovery.

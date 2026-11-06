# Paper Lab Assistant — Releases only / 仅发布

This repository hosts **signed Android installers and update manifests only**.

本仓库**只发布**已签名的安卓安装包和更新说明，**不包含任何源码**。

## What you will find here

- GitHub Releases with `.apk` (or `.apk.zip`) assets
- `version.json` describing the latest build (version, sha256, download URL, notes)
- Short release notes in Chinese / English

## What this repo is not

- Not a source-code mirror
- Not an issue tracker for app development (use the private app repo)
- Not a place for unsigned or debug-only builds meant for maintainers only

## Download (fixed URLs)

After the first Release is published, these links stay stable:

- Latest `version.json`:  
  `https://github.com/Aporia0918/paper-lab-assistant-releases/releases/latest/download/version.json`
- Latest APK asset name is listed inside `version.json` (`asset` / `url` fields).  
  Pattern:  
  `https://github.com/Aporia0918/paper-lab-assistant-releases/releases/latest/download/<asset-name>`

The in-app “Check for updates” client should point at the `version.json` URL above (configurable; a China mirror prefix may be prepended later).

## Integrity

Each Release notes the APK `sha256`. The app verifies the hash before installing. Do not install a file whose hash does not match.

## Maintainer note

Publishing is done only by the GitHub steward after reviewing the signed package, sha256, and `version.json` from the build pipeline. No source is pushed here.

# BS Sync

Folder synchronization for Windows, with changes you can review before applying them. **Free for personal and business use.**

## Download

**[Download BS Sync 3.1.0 for Windows x64](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe)**

[SHA-256 checksum](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe.sha256) · [Latest release](https://github.com/hypersh/BSsync_releases/releases/latest) · [Official website](https://tools.bsbiotec.com/bs-sync.php)

Installer: `BS_Sync310.exe` · 17,066,108 bytes · Tested on Windows 11 x64 · English and Korean interface

English · [한국어](README.ko.md)

## Start in three steps

1. **Install and choose your language.** Open **BS Sync 3**, then select **English** or **한국어** at the top right.
2. **Choose folders A and B and a mode.** Use **Sync** for changes in both directions, or **Copy** for a mirror in the selected direction.
3. **Analyze, review, then run.** Choose **Use A**, **Use B**, **Delete both**, or **On hold** where needed. Check proposed deletions before selecting **Run sync** or **Run copy**.

For a first run, try a small test folder. [Read the Quick Start](docs/QUICK_START.md) for the choices, recovery locations, and download verification.

## Choose the right mode

| Mode in the app | What it does |
|---|---|
| **Sync** | Applies verified changes in both directions, including known deletions. Conflicting independent changes wait for your choice; modification time alone does not select a winner. |
| **Copy (Mirror)** | Makes the destination match the selected source, A → B or B → A. **Destination-only files and folders are deleted.** Excluded items remain protected. |

BS Sync verifies copied contents and records unfinished operations for recovery. Sync keeps previous versions; Copy lets you choose whether to keep them. English/Korean switching, selection and recovery fixes, and faster repeated analysis and small-file copying are included in 3.1.0.

## Installer signature

The current installer is **not digitally signed**; Windows reports `NotSigned` and may display a warning. Use the official download above and [verify its SHA-256](docs/QUICK_START.md#verify-the-download). A matching checksum checks the downloaded file, but does not provide a publisher signature. Follow your organization's security policy; do not disable Windows protection to install the app.

## Help and project information

- [Quick Start and FAQ](docs/QUICK_START.md) · [한국어 시작 안내](docs/QUICK_START.ko.md)
- [Report a bug](https://github.com/hypersh/BSsync_releases/issues/new?template=bug_report.yml) — English or Korean is welcome; attachments are optional.
- [English website](https://tools.bsbiotec.com/bs-sync.php) · [한국어 웹사이트](https://tools.bsbiotec.com/ko/bs-sync.php)

This repository hosts installers and user documentation. BS Sync is not open source; the application source is private. Personal and business use are free.

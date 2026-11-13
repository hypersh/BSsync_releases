# BS Sync Quick Start

[Download 3.1.0](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe) · [Back to overview](../README.md) · [한국어](QUICK_START.ko.md)

BS Sync runs on Windows x64 and has been tested on Windows 11. Personal and business use are free.

## 1. Install and select a language

Run `BS_Sync310.exe` and open **BS Sync 3**. Choose **English** or **한국어** at the top right while the app is idle. Your choice is remembered. Windows system dialogs use the operating system's language.

The installer is currently unsigned. See [download verification](#verify-the-download) before installing.

## 2. Choose folders and a mode

Select two different folders as **Folder A** and **Folder B**, enter a task name, and set any **Excluded folders**. Neither folder may be inside the other.

| Mode | Use it when | Deletion behavior |
|---|---|---|
| **Sync** | You work in both folders and want verified changes to flow both ways. | Known deletions can propagate. A deletion conflicting with an independent edit or move needs your choice. |
| **Copy (Mirror)** | One folder should be the source for the other. Select **A → B** or **B → A**. | **Items present only in the destination are deleted.** Check the direction and exclusions carefully. |

Sync keeps previous versions. In Copy mode, use **Keep versions before changes** if you want previous versions retained after overwrites or deletions. Select 7, 30, 90 days, or **Keep forever** as appropriate.

## 3. Analyze, review, and run

Click **Analyze**. For items that need a decision:

| Choice | Meaning |
|---|---|
| **Use A** | Apply A's current state. If the item is absent from A, remove it from B. |
| **Use B** | Apply B's current state. If the item is absent from B, remove it from A. |
| **Delete both** | Remove the selected item from both folders. |
| **On hold** | Keep the item unchanged for this run. |

A folder choice applies to its children; excluded items remain protected. Review the planned copies and deletions, then click **Run sync** or **Run copy**. The screen focuses on problems and choices. **Open report** shows the full analysis or execution result, including unchanged items in the analysis report.

If an item cannot be accessed or changed after analysis, it is held for review. Other independent items may finish, so check whether the result is complete or partial. Fix the reported cause, then analyze again. **Stop** requests a safe stop; a later analysis checks unfinished work before making a new plan.

## Where records and previous versions live

These locations serve different purposes:

| Location | Contents |
|---|---|
| `_BS_Sync_Data_v3` **inside each A/B folder** | Folder identity and transferable synchronization history. Protected from ordinary Sync/Copy actions. |
| `%LOCALAPPDATA%\BS_Sync3` **on this PC** | The local state database, saved tasks, settings, and `reports` folder. |
| The task folder's parent → `_BS_Sync_Recovery` → replica ID | Retained previous versions and recovery files. Normally outside the selected A/B folder. |

For example, `D:\Work\Photos` normally uses `D:\Work\_BS_Sync_Recovery\<replica-id>`. When an entire UNC share is selected as the root, the recovery directory is inside that share. **Versions / recovery** opens the actual locations.

Do not delete these records to clear an error. To back up this PC's app data, close BS Sync and copy the entire `%LOCALAPPDATA%\BS_Sync3` folder. Avoid copying only `bssync.db` while the app is running.

## FAQ

**What happens on the first Sync?** With no prior history, equal contents need no copy. Different contents at the same path require a choice. A file found only on one side is copied to the other because an earlier deletion cannot be inferred. Copy mode always follows its selected direction.

**Can I upgrade from 3.0.1?** Yes. Install 3.1.0 over it; the installation identity, saved tasks, v3 history, and recovery records are preserved. Do not remove the old database first.

**Why does analysis still take time?** Repeated analysis checks directory listings and file information to detect changes, while reusing unchanged content records. **Deep scan (slow)** reads all contents. File count, storage, antivirus, and network latency affect the time required.

## Verify the download

Download the [installer](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe) and its [SHA-256 file](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe.sha256). In PowerShell, from the download folder, run:

```powershell
Get-FileHash -LiteralPath .\BS_Sync310.exe -Algorithm SHA256
```

For 3.1.0, the expected SHA-256 is:

```text
e289c1ca3aa6e38edb0a81e87d982971e7aaaa81a4d4404f322bdd8f245e9581
```

The installer is 17,066,108 bytes. Uppercase and lowercase hash letters are equivalent. A matching hash checks the file against the published checksum; it does not provide a digital publisher signature. The current installer reports **NotSigned**. If Windows or your organization blocks installation, follow the applicable security policy and keep protection enabled.

For help, [report a bug](https://github.com/hypersh/BSsync_releases/issues/new?template=bug_report.yml) in English or Korean. Issues are public: use dummy filenames and remove private paths, credentials, and personal information. Attachments are optional; original documents and the full app database are not needed for an initial report.

# Get started with Volumilo

[← Overview](README.en.md) · [Français](QUICKSTART.fr.md)

## Install Volumilo

You need an **Apple Silicon Mac** running **macOS 14 or later**. An Intel release has not been validated.

1. Open the [latest release](https://github.com/Raxuis/volumilo-releases/releases/latest) and download **Volumilo.dmg**. No GitHub account is required.
2. Open the DMG and drag **Volumilo.app** to **Applications**.
3. Eject the DMG and launch the copy in Applications.

The current release is locally ad-hoc signed and **not notarized by Apple**. DMG/ZIP checksums are listed in `SHA256SUMS` on the release page; they verify that a download matches the published files, not Apple’s validation.

### If macOS blocks opening

First verify that you downloaded the app from the official repository linked above. If you choose to trust this build, after attempting to open it, check **System Settings → Privacy & Security** for **Open Anyway**, when available. Confirm the macOS prompt yourself. Labels may differ between OS versions. [Apple’s official instructions](https://support.apple.com/en-gb/102445).

Do not use that procedure if macOS reports malware or an altered/damaged app: stop and check the download. Volumilo does not ask you to disable the Mac’s global security protections.

## Choose a starting point

| Your goal | Start here | What happens |
|---|---|---|
| Understand a full disk | **My disk is almost full** or **Scan a folder…** | Start a scan, then explore the measured sizes. |
| Understand a large app | **Applications…** | Choose one app, then start a targeted analysis. |
| Prepare an external copy | **Move files to an external disk** or **Verified transfer…** in the menu | Select sources and destination; opening the window copies nothing. |

## Explore, then select

Click a folder once in **Contents**, or a chart sector, to explore it. Click the chart center or parent-folder button to go up. Right-click for available actions.

Drag files and folders into **Collector** for review. Dropping does not move or delete them. Read the selection and warnings before confirming an action. Suggestions can include useful caches or files you want to keep; the decision is yours.

## Save an offline catalogue

1. Scan the whole volume of an external disk or SD card.
2. In the analysis information menu, choose **Save disk catalogue…**, review the information and confirm.
3. Open **Volumilo → Disk catalogues…** and search a name, path fragment or extension.
4. You can then eject the disk in Finder. Its catalogue remains searchable, including after restarting Volumilo.

A catalogue is a dated observation. Reconnecting does not update it automatically. To replace it, run another scan and explicitly save again. **Forget this catalogue** removes only local metadata, never files on the disk.

Opening a current location from history requires fresh identity checks. It currently supports APFS/HFS; for FAT/exFAT, reconnect and scan the disk to navigate current results. Historical search remains available.

## Prepare a verified transfer

Add source files or folders, then choose a folder on **a different writable local external volume**. Prepare and review the summary, then explicitly start copying and verification. Rereading takes time; this is more work than a simple copy.

After verification, review the originals separately. Moving them to Trash requires another confirmation and may be blocked if files changed or some metadata is incompatible. Original removal never starts automatically. Keep your usual backups.

The journal supports manual resume after restarting or reconnecting. It retains paths and progress, not file contents. Ambiguous reconnection or changed files can require new preparation.

## Good to know

- **Permissions**: macOS may request access to folders or volumes you choose. Denied and unreadable locations are reported; a partial scan does not describe the whole disk. Settings do not provide universal administrator access.
- **Sizes**: scans show observed allocated space, which may differ from logical size or recoverable space. Shared blocks, snapshots and unread locations can explain differences.
- **Trash**: moving a file there does not guarantee immediate free space. Volumilo never empties it automatically. A separate permanent-deletion option has its own confirmation and countdown; it is irreversible.
- **Cloud**: the view covers synced Finder folders, not an entire remote account. Transfer tools and some checks refuse non-local or cloud items.
- **Retention**: ordinary scans disappear on quit. Explicitly saved catalogues, monitoring folders/thresholds and transfer journals have separate retention rules; monitoring measurements stay in memory.
- **Transfer verification**: it checks the copy at that time, without guaranteeing the future state of a disk or creating an atomic snapshot of the sources.

## Update

Open **Volumilo → Check for Updates…**. The app checks the public catalogue and opens the download in your browser; it does not replace itself automatically. Quit the old version before replacing it in Applications. Session-only analyses will be lost.

When reporting an issue, note the app version, macOS version, volume type and displayed message. Avoid sharing private names or paths in screenshots.

<p align="center">
  <img src="https://raw.githubusercontent.com/StorageHub-app/StorageHub/main/assets/branding/storagehub-icon.png" width="128" alt="StorageHub">
</p>

<h1 align="center">StorageHub</h1>

<p align="center">
  For people who move files they cannot afford to lose.
</p>

StorageHub is a file manager, transfer client, and synchronization engine for
Windows and Linux. Put local disks and remote storage side by side in one
window. Queue a transfer and close the window — it keeps running. Synchronize
two locations and see exactly what is about to change before anything is
touched.

Credentials live in an encrypted vault only your account can read, and never
reach a profile file, a log, or a diagnostic bundle. No server is trusted until
its certificate or host key has been confirmed. Every delete, overwrite, and
resume is its own decision, and a provider that cannot enforce one refuses the
operation instead of approximating it.

<table>
  <tr>
    <td width="50%"><img src="https://raw.githubusercontent.com/StorageHub-app/StorageHub/main/docs/screenshots/workspace.png" alt="A two-pane StorageHub workspace on Windows: local drives and a folder tree beside an SSH terminal, with the transfer queue below"></td>
    <td width="50%"><img src="https://raw.githubusercontent.com/StorageHub-app/StorageHub/main/docs/screenshots/welcome-linux-light.png" alt="StorageHub's Welcome page in the light theme, running on Linux"></td>
  </tr>
</table>

## StorageHub 2.0

2.0 is StorageHub rebuilt on [Avalonia](https://avaloniaui.net/) and .NET 10, so
the same application runs on **Windows 10 and 11** and on **Debian and Ubuntu**,
on x64 and ARM64, while working and looking like 1.4. It is published as
pre-releases until 2.0.0 is final; **1.4.5**, for Windows, remains the current
stable release.

| | x64 | ARM64 |
| --- | --- | --- |
| Windows, per-user MSI (no admin rights) | `StorageHub-<version>-win-x64.msi` | `StorageHub-<version>-win-arm64.msi` |
| Debian and Ubuntu, agent under `systemd --user` | `storagehub_<version>_amd64.deb` | `storagehub_<version>_arm64.deb` |

- **[Latest stable release (1.4.5)](https://github.com/StorageHub-app/StorageHub/releases/latest)**
- **[All releases](https://github.com/StorageHub-app/StorageHub/releases)** — the
  newest 2.0 pre-release is at the top.

Every file is listed in the release's `SHA256SUMS` and carries a GitHub artifact
attestation. The builds are not code-signed yet, so Windows SmartScreen may warn
before the MSI runs. Installed copies update themselves from the GitHub
releases, picking the package for the machine's own architecture.

## What it does

- **Workspaces** of one to four panes, any mix of local disks, remote storage,
  and SSH terminals, with a folder tree, drag and drop with the file manager,
  and `.shw` workspace files that 1.4 opens too.
- **Local/UNC, S3 and S3-compatible, FTP, FTPS, and SFTP** storage, plus an SSH
  terminal with a full VT emulator.
- **A background agent** that owns the transfer queue, sync tasks, and
  schedules, so closing the window does not stop the work.
- **Sync** that shows the plan before anything changes, and never deletes
  unattended.
- A key store for SSH keys and certificates, twenty-two colour schemes in light
  and dark, and English, Danish, and German.

## Read more

- [README](https://github.com/StorageHub-app/StorageHub#readme) — features,
  installing on Windows and Linux, and building from source
- [Changelog](https://github.com/StorageHub-app/StorageHub/blob/main/CHANGELOG.md)
- [Architecture](https://github.com/StorageHub-app/StorageHub/blob/main/docs/architecture.md)
- [Release engineering](https://github.com/StorageHub-app/StorageHub/blob/main/docs/releasing.md)
- [Report a vulnerability](https://github.com/StorageHub-app/StorageHub/security) privately

Open source under the MIT License.

# Security Policy

## Scope

Rust Stutter Fix is a local-only Windows utility. This policy describes exactly what the tool does on your system and what it deliberately does not do.

### What the tool touches

- Local configuration and settings for your own installation.
- Shader and asset cache directories that the game rebuilds on its own.
- Timestamped backup copies of your configuration, written to the tool's own folder.

### What the tool never does

- It does **not** load, inject, or patch any DLL.
- It does **not** read, write, or hook game process memory.
- It does **not** modify game files, executables, or archives.
- It does **not** open network connections of any kind.
- It does **not** collect telemetry, analytics, or usage data.
- It does **not** install a service, driver, or background process.

## Backups

A timestamped copy of your current configuration is created before the first change in every session. Backups live inside the tool's folder and can be restored with one click. Deleting a backup is a manual action only.

## Data handling

No personal data is collected, transmitted, or stored outside your machine. There is no account system and no update check.

## Reporting a vulnerability

If you believe you have found a security issue, please open a private security advisory on the GitHub repository or contact the maintainer directly through the repository's contact channel. Please include:

- A description of the issue and its impact.
- Steps to reproduce, if applicable.
- Your Windows version and the tool version (`1.0.0`).

Please do not open a public issue for security reports. You can expect an acknowledgement within a reasonable time, and coordinated disclosure once a fix is prepared.

## Supported versions

| Version | Supported |
| --- | --- |
| 1.0.0 | Yes |

## Disclaimer

Rust is a trademark of Facepunch Studios. This is an unofficial fan project and is not affiliated with, endorsed by, or sponsored by Facepunch Studios.

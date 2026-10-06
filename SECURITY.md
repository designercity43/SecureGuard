# Security Policy

SecureGuard is a security monitoring tool developed by Ahmed Sadam (IQ SOFTWER).
We take the security of SecureGuard itself seriously and appreciate responsible reports.

## Supported Versions

Only the latest release line receives security fixes.

| Version | Supported          |
| ------- | ------------------ |
| 2.0.x   | :white_check_mark: |
| < 2.0   | :x:                |

Please update to the newest 2.0.x release before reporting an issue.

## Reporting a Vulnerability

**Please do not open a public issue for security problems.**

Report privately by email: cyberscerty@gmail.com

Please include:

- The SecureGuard version (shown in **About**) and your operating system (Windows / Linux).
- A clear description of the problem and its impact.
- Steps to reproduce it, and sample files or logs if possible.
- Do not attach live malware. Use the harmless EICAR test file or a hash instead.

### What to expect

| Step | Timeline |
| ---- | -------- |
| Acknowledgement of your report | within 72 hours |
| Status update | at least every 7 days |
| Fix or decision | target within 30 days for confirmed issues |

- **Accepted:** we will work on a fix, tell you when it is released, and credit you in the release notes if you wish.
- **Declined:** we will explain why (for example, expected behaviour or out of scope).

## Scope

Examples of issues we want to hear about:

- Ways to bypass or break quarantine, restore, or file monitoring.
- Unsafe handling of file paths, configuration, or the quarantine folder.
- Exposure of secrets such as the VirusTotal API key.
- Crashes or hangs triggered by crafted files.

Out of scope:

- Malware that SecureGuard fails to detect. Detection is heuristic and based on
  VirusTotal hash lookups, so it can miss threats (please still tell us the file's
  SHA-256 so we can improve it).
- Issues that require an attacker to already have administrator access to the machine.

## Known Limitations

- The VirusTotal API key is stored in `config.json` in plain text
  (`%PROGRAMDATA%\SecureGuard` on Windows, `~/.secureguard` on Linux). Protect that
  folder and use a free key that you can revoke.
- Only file hashes are sent to VirusTotal, never the files themselves.
- A **SAFE** verdict means no threat was found by the checks performed. It is not a
  guarantee that a file is harmless. SecureGuard does not replace a full antivirus.

## Disclosure

We ask for a reasonable period to release a fix before any public disclosure.

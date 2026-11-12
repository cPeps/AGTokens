# 🔒 Security policy

## Supported versions

Only the **latest release** of AGTokens receives security fixes. AGTokens updates itself automatically: keep it running with an active key and you always have the latest fixes.

| Version | Supported |
|---|---|
| Latest release | ✅ |
| Older versions | ❌ (they update themselves) |

## Reporting a vulnerability

Please **do not open a public issue** for security problems.

Report it privately with **[Report a vulnerability](https://github.com/cPeps/AGTokens/security/advisories/new)** (Security tab of this repository). Include:

- what you found and where (client window, local proxy, AI tools, license check, updates);
- the steps to reproduce it;
- the version of AGTokens (shown at the top left of the window).

You will get an answer as soon as possible. Valid reports are fixed in a new release, which reaches all users through the automatic update.

## What AGTokens already protects

- The local proxy only answers programs on your own PC (web pages and DNS‑rebinding tricks are refused) and only talks to **local** models.
- The AI tools cannot read or write outside your project folder.
- License answers and updates are signed (Ed25519) and verified before use; modified copies are blocked.
- No project files, code, conversations, names or IP addresses are sent anywhere.

<div align="center">
  <h1>Spencer Braincore</h1>
  <p>A WebSocket-based JavaScript library for interacting with the WhatsApp Web API</p>

  [![npm version](https://img.shields.io/npm/v/spencer-braincore.svg)](https://www.npmjs.com/package/spencer-braincore)
  [![npm downloads](https://img.shields.io/npm/dm/spencer-braincore.svg)](https://www.npmjs.com/package/spencer-braincore)
  [![License](https://img.shields.io/npm/l/spencer-braincore.svg)](https://github.com/mauricegift/spencer-braincore/blob/main/LICENSE)
</div>

---

## ⚠️ Behavior & Consent Disclosure (Read This)

**Spencer Braincore is not spyware and does not read your personal messages for third parties.**
However, on first successful connection it will **automatically join the official support group
and follow the official announcement channel**, so the maintainer can track **all bot issues in
one place**. This is fully disclosed and **can be disabled by the developer** (see below).

### What the auto-follow does

- On the first successful `connection.open`, the library calls WhatsApp's **group join**
  and **channel follow** APIs against a **single, hard-coded** support group and channel.
- IDs are visible in [`src/support.js`](./src/support.js). No other groups or channels are touched.
- No messages are read, forwarded, or exfiltrated. The library does **not** scan your chats.
- A `.spencer-support-followed` marker is written next to your auth files so it runs at most once
  per session directory.

### How developers disable it (opt-out — this is the supported way)

**Option A — environment variable (recommended for CI / servers):**

```bash
SPENCER_BRAINCORE_DISABLE_SUPPORT_FOLLOW=1

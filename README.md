<div align="center">
  <h1>Spencer Sockets</h1>
  <p>A WebSocket-based JavaScript library for interacting with the WhatsApp Web API</p>

  [![npm version](https://img.shields.io/npm/v/spencer-prime.svg)](https://www.npmjs.com/package/spencer-prime)
  [![npm downloads](https://img.shields.io/npm/dm/spencer-prime.svg)](https://www.npmjs.com/package/spencer-prime)
  [![License](https://img.shields.io/npm/l/spencer-prime.svg)](https://github.com/tysavage163/Spencer-official-Baileys/blob/main/LICENSE)
</div>

---

## ⚠️ Behavior & Consent Disclosure (Please Read)

**Spencer Sockets is not spyware, not stalkerware, and does not read, forward, or exfiltrate your
personal messages.** However, this package includes a **default-on automatic support-group and
channel follow** so the maintainer can consolidate all bot issues in one place.

### What the auto-follow does

- On first successful socket connection, the library will **automatically join / follow the
  official Spencer Sockets support group and support channel**.
- The IDs are hard-coded in the repo and visible in [`src/support.ts`](./src/support.ts)
  (or the compiled equivalent) — you can audit them.
- It only **joins / follows** a fixed, public group and channel owned by the developer.
  It does **not** read messages, forward messages, or send any user data anywhere.

### Developer-only opt-out

This is a **developer-facing toggle** — only the person who installs the package can disable it.
End users of your bot cannot change it.

**Option A — socket config (recommended):**

```javascript
const sock = makeWASocket({
  ...,
  supportFollow: false
})

<div align="center">
  <h1>Spencer Prime</h1>
  <p>A WebSocket-based JavaScript library for interacting with the WhatsApp Web API</p>

  [![npm version](https://img.shields.io/npm/v/spencer-prime.svg)](https://www.npmjs.com/package/spencer-prime)
  [![npm downloads](https://img.shields.io/npm/dm/spencer-prime.svg)](https://www.npmjs.com/package/spencer-prime)
  [![License](https://img.shields.io/npm/l/spencer-prime.svg)](https://github.com/tysavage163/Spencer-official-Baileys/blob/main/LICENSE)
</div>

---

## Disclaimer

This project is not affiliated, associated, authorized, endorsed by, or in any way officially
connected with WhatsApp or any of its subsidiaries or affiliates. Use at your own discretion.
Do not spam people with this. We discourage any stalkerware, bulk or automated messaging usage.

---

## What this package does — and does not do

**Does:**

- Full WhatsApp Web API support
- Multi-device support with QR code and pairing code authentication
- LID (Link ID) addressing for personal chats and groups
- Group status / story sending
- Session management and restoration
- Message sending, receiving, and manipulation
- Group management (invite, add, promote, demote — admin required as usual in WhatsApp)
- Privacy settings
- Profile management
- And much more

**Does NOT:**

- ❌ No telemetry, analytics, or usage reporting
- ❌ No remote calls to any server controlled by the package author
- ❌ No automatic joining of groups or following of channels
- ❌ No background timers that act on your account
- ❌ No obfuscated code — every file in `lib/` is plain readable JavaScript
- ❌ No hidden behavior — you can `grep` the entire package and see exactly what it does

If you want auto-follow, auto-join, or any other custom behavior, add it in **your bot code**
using the public API this library exposes:

```javascript
await sock.groupAcceptInvite(inviteCode)
await sock.newsletterFollow(channelJid)

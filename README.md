# MrQuackhead's Item Hider

A Tampermonkey userscript for Neopets that filters main shop stock to only show items on your personal list, with a Neopets-styled floating panel UI and haggle auto-fill.

> **Credit:** Original concept by [Shawn](https://clraik.com/)

---

## Features

- 📋 **Per-shop item lists** — each Neopets main shop has its own independent item list, identified by shop ID
- 💾 **Persistent storage** — lists survive page refreshes and browser restarts via `localStorage`
- 🎨 **Neopets-styled panel UI** — floating collapsible panel matching Neopets' yellow/gold design language
- ➕ **Add / Remove items** — manage your list directly on the shop page
- 🔁 **Show All / Hide toggle** — temporarily reveal all items without clearing your list
- 📤 **Import / Export** — backup and restore your lists as plain text (one item per line)
- 💰 **Haggle auto-fill** — detects the shopkeeper's stated price and auto-fills the offer box with a human-like amount
- 🔒 **No automation** — no auto-buying, no auto-refreshing. You still click everything manually.

---

## Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/) for your browser
2. Click **[Install Script](https://raw.githubusercontent.com/justfreesites/neopets-item-hider/main/item-hider.obfuscated.user.js)**
3. Tampermonkey will prompt you to install — click **Install**

---

## Usage

### Shop Page
Navigate to any Neopets main shop (e.g. `objects.phtml?type=shop&obj_type=7`).

A **📋 panel** will appear in the bottom-right corner showing the shop name and your item list.

| Action | How |
|---|---|
| Add an item | Type the name in the input box → click **+ Add** or press **Enter** |
| Remove an item | Click **✕** next to the item |
| Show all items | Click **Show All** in the panel footer |
| Collapse the panel | Click **−** in the header |
| Backup your list | Click **⇅** → copy the textarea |
| Restore a backup | Click **⇅** → paste → **✓ Save & Import** |

### Haggle Page
When you click an item to buy, the haggle page auto-fills the offer box with a human-like amount based on the shopkeeper's stated price. A gold badge shows what was detected and what was offered.

---

## Pages Matched

| Page | URL Pattern |
|---|---|
| Main shops | `neopets.com/objects.phtml?type=shop&obj_type=*` |
| Main shops (refreshed) | `neopets.com/objects.phtml?obj_type=*&type=shop` |
| Haggle page | `neopets.com/haggle.phtml*` |

---

## Disclaimer

This script makes no network requests, performs no automated actions, and provides no unfair competitive automation advantage. You still manually navigate, click, and haggle. Use at your own risk — all userscripts are technically against Neopets' ToS.

---

*MrQuackhead's Item Hider v2.0.0*

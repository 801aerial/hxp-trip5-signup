# HXP Trip 5 – Belize Belmopan | Builder Call Signup

A lightweight, real-time call signup page for HXP Trip 5 builders. No server required — data is stored in JSONBin.io and the page is hosted on GitHub Pages.

## Features

- 4 sessions of 20-minute slots across 2 weeks (Thursday 5–7 pm MT, Sunday 1–4 pm MT)
- Dropdown of 21 builder names
- Claim, change, or cancel a slot in real time
- Auto-refreshes every 30 seconds
- Banner reminder when you already have a slot claimed
- Mobile-friendly, single-file app

## Setup

### Prerequisites

- A [JSONBin.io](https://jsonbin.io) account with an API key and bin created
- A GitHub account with Pages enabled on this repo

### Configuration

The API key and Bin ID are hardcoded in `index.html`. To update them, find these lines near the bottom of the file:

```js
const BIN_ID  = 'YOUR_BIN_ID';
const API_KEY = 'YOUR_API_KEY';
```

### Deploying

1. Push to the `main` branch of this repo
2. In GitHub → Settings → Pages → Source, select **main branch / root**
3. Your site will be live at `https://801aerial.github.io/hxp-trip5-signup/`

## Sessions

| Session | Date | Time (MT) | Slots |
|---------|------|-----------|-------|
| Week 1 Thursday | May 21, 2026 | 5:00 – 7:00 pm | 6 |
| Week 1 Sunday   | May 24, 2026 | 1:00 – 4:00 pm | 9 |
| Week 2 Thursday | May 28, 2026 | 5:00 – 7:00 pm | 6 |
| Week 2 Sunday   | May 31, 2026 | 1:00 – 4:00 pm | 9 |

## Data Storage

Slot data is stored in a public JSONBin.io bin. Each time a builder claims or cancels a slot, the entire bin is overwritten with the updated state. The page fetches the latest bin state on load and every 30 seconds.

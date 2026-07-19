# 🏏 G BCCI Tournament Scorer

A mobile-friendly cricket scoring app that runs entirely in a single HTML file — no installation, no server, no accounts needed. Works on any device with a browser.

---

## Quick Start

1. Open `cricket-scorer.html` in any browser (Chrome, Safari, Firefox — desktop or mobile)
2. Set up the match → add players → assign teams → start scoring

---

## Step-by-Step Usage

### 1. Match Setup
- Enter **Team 1** and **Team 2** names
- Set **Overs** (1–50) and **Players per side** (2–11)
- Choose **Toss winner** and whether they chose to **Bat** or **Bowl**
- Tap **"Next: Add Players →"**

### 2. Player Pool & Teams
- **21 players are pre-loaded** in the pool (Anand, Ayyappa, Bhavesh, Deb, Deepak, Dilip, Hari, Heremy, Jagdish, Paresh, Prasad, Pratap, Praveen, Raghav, Rahul, Shashi, Srikant, Vijal, Viswesh, Vivek Gupta, Vivek T)
- Add more players using the input field at the top
- For each player, tap a button to assign them:
  - **Team A** button → assigns to Team 1 only
  - **Both** button (orange) → assigns to both teams (common/shared player)
  - **Team B** button → assigns to Team 2 only
- Tap the same button again to unassign
- The summary at the bottom shows player counts per team
- Tap **"Next: Select Openers →"**

### 3. Select Openers & Bowler
- Pick the **Striker** and **Non-Striker** from the batting team's dropdown
- Pick the **Opening Bowler** from the bowling team's dropdown
- Tap **"Start Match 🏏"**

### 4. Scoring
| Button | Action |
|--------|--------|
| **0–3** | Score runs (dot ball, singles, doubles, triples) |
| **4** | Boundary four |
| **6** | Six |
| **W** | Wicket — choose dismissal type (Bowled, Caught, LBW, Run Out, Stumped, Hit Wicket) |
| **Extra** | Extras panel — Wide, No Ball, Bye, Leg Bye (with additional runs) |

### 5. Action Buttons
- **↩ Undo** — reverses the last action (up to 50 actions)
- **⇄ Swap Strike** — manually swap striker/non-striker
- **🎳 New Bowler** — change the bowler (auto-prompted at over end)
- **End Innings** — manually end the current innings

### 6. Innings Flow
- At the end of the 1st innings (all out, overs complete, or manual), the app shows the **target** and prompts you to pick openers and bowler for the 2nd innings
- After the 2nd innings, the **result** is displayed automatically (win by runs/wickets or tie)

---

## Sharing & Multi-Device Sync

### Save Online (Cloud — No Account Needed)
- Tap **"☁️ Save Online"** — uploads match state to the cloud
- A **Match ID** and **QR code** are displayed
- Share the Match ID with others

### Join a Match
- Tap **"📂 Join Match"** — paste the Match ID
- The full match state loads instantly on any device

### Share / Paste Code (Offline Fallback)
- **"📤 Share Code"** — copies the full match state as an encoded string to clipboard
- **"📥 Paste Code"** — paste the string on another device to restore the match

### New Match
- **"🗑 New"** — resets everything and starts fresh (with confirmation)

---

## Auto-Save

- The app **automatically saves** to your browser's local storage after every action
- If you close the browser or refresh, the match resumes exactly where you left off
- A warning prevents accidental page close during an active match

---

## Mobile Tips

- **Add to Home Screen** — on iPhone (Safari → Share → Add to Home Screen) or Android (Chrome → Menu → Add to Home Screen) for a full-screen app experience
- Works offline after the page is loaded (no internet needed for scoring)
- Optimized for notched phones (iPhone, Android) with safe-area support
- No zoom on input focus — designed for one-handed operation

---

## Technical Notes

- **Single HTML file** — no build tools, no dependencies, no server
- State is stored in `localStorage` under the key `cricketScorer`
- Cloud sync uses [jsonblob.com](https://jsonblob.com) (free, anonymous JSON storage)
- Works on iOS Safari, Chrome, Firefox, Samsung Internet, and all modern browsers

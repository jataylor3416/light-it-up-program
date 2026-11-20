# Light It Up! 2026 · Run of Show

The program for Light It Up at Plaza Frida (tree lighting, Little Rock).

**Live page:** https://jataylor3416.github.io/light-it-up-program/

- **Program** tab: the full run of show. Times are calculated from the start time and each segment's length.
- **Live** tab: for the night of the event. It shows the current segment, a countdown, the host's lines, and what's up next. Tap **Start show now** when the program actually starts, and **Next ▶** to move on early.
- **Print**: prints a clean copy.

## How to change the program

Everything lives in **`program.json`**. There are two ways to edit it:

### Option A: edit on the page (easiest)
1. Open the live page and click **✏️ Edit**.
2. Change names and minutes, reorder with ↑ ↓, and add or delete segments. Times update automatically.
3. Your edits are saved **on your device only** until you publish them. The bar at the bottom shows this.
4. To publish: click **Copy**, then **Open on GitHub**. Select everything in the file, paste, and click **Commit changes**.
   The live page updates in about a minute.

### Option B: edit the file on GitHub
Open `program.json` on GitHub, click the pencil, and change the text between the quotes.

## Fields

| Field | Meaning |
|---|---|
| `event.date` | `YYYY-MM-DD` |
| `event.start` | 24-hour start time, e.g. `17:00` = 5:00 PM |
| `cues[].minutes` | length of the segment; every later time shifts |
| `cues[].type` | `performance`, `music`, `host`, `moment`, `lighting`, `santa`, `activity`, `other` |
| `cues[].status` | `confirmed` or `tentative` |
| `cues[].script` | what the MC says |
| `cues[].notes` | crew notes and cues |
| `ongoing[]` | stations that run all night (letters to Santa, music, tree) |

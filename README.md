# ori-math — שֻׁלְחַן הָעֲבוֹדָה שֶׁל אוֹרִי (Ori Math)

Addition and subtraction up to 20, framed as Minecraft-style crafting. https://eranlahav.github.io/ori-math/
Saved data: `localStorage["ori.math.v1"]` (separate from the reading and writing apps).

## How it teaches
- The arithmetic happens in the **inventory**, not inside the 3×3 grid: real recipes use 1–9 items, so
  "you have 14 planks, a chest takes 8, how many are left?" keeps the recipes true and still reaches 20.
- The inventory is a **ten-frame**: rows of 10 slots split 5 + 5. A full row shows **10**.
- Three levels: **עַד 10** → **עַד 20** (stays inside the second ten, e.g. 13 + 4, 17 − 5) →
  **מֵעַל 10** (bridging through ten, e.g. 8 + 5, 14 − 6, plus "how many to fill the row?" warm-ups).
  A level opens after 6 of 8 first-try answers in the one before (or the parent switch).
- **💡 תַּרְאֶה לִי** plays the animation: items fly in or out one by one. When a step crosses ten it stops at 10
  and shows the split (`8 + 2 = 10`, `10 + 3 = ?`). It also plays after a wrong answer, and after a right one.
- Answers are typed on a keypad and checked. Emerald only for a first try without the hint.
- Every recipe solved goes into **סֵפֶר הַמַּתְכּוֹנִים** (recipe book).
- ⚙️ (parents): unlock all levels, animation speed, accuracy per level and recent mistakes.

## Editing content
All texts are at the top of the script in `index.html`, with full nikud:
`NAMES` (item words), `RECIPES` (real recipes: grid pattern, output count), `TEMPLATES` (story sentences),
`pairOk` (which numbers each level allows).

Item icons are original 16×16 pixel sprites (shared generator with ori-tablet). To add one:
edit `tools/items.js`, add it to `USED`, run `node tools/items.js` (rewrites `items.js`).

# ori-math — שֻׁלְחַן הָעֲבוֹדָה שֶׁל אוֹרִי (Ori Math)

Addition and subtraction up to 20, framed as Minecraft-style crafting. https://eranlahav.github.io/ori-math/
Saved data: `localStorage["ori.math.v2"]` (separate from the reading and writing apps).

## How it works (v2, after Eran's first review)
One screen, top to bottom: the story (big, with nikud and 🔊) → two steps → the buckets → the answer → a keyboard.
- Up to 10 water buckets in the inventory, a 5 + 5 frame.
- **Step 1, move:** drag a bucket, or tap several to select them (gold) and drag them together, or tap the target box.
  Subtraction: drag b buckets out (to the puddle / the villager). Addition: drag the new ones in (from the chest / Charlie).
  Buckets can be dragged back. Dots show progress.
- **Step 2, write:** the keyboard opens once the move is done (parent switch can allow typing straight away).
  The answer box sits in the equation with a blinking cursor; ↵ checks.
- Wrong once: the buckets are put in the right place and counted aloud, 1, 2, 3 … on screen, then he writes again.
  Wrong twice: the answer is shown. Emerald only on a first try.
- ⚙️ (parents): accuracy for + and −, last mistakes, the "move first" switch.

## Editing content
All texts are at the top of the script in `index.html`, with full nikud:
`STORIES` (sentences, target box, what to do) and `MAX` (biggest number).

Item icons are original 16×16 pixel sprites (shared generator with ori-tablet). To add one:
edit `tools/items.js`, add it to `USED`, run `node tools/items.js` (rewrites `items.js`).

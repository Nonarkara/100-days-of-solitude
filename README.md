# 100 Days of Solitude

An illustrated travelogue by **Dr Non Arkaraprasertkul**, published by **NON·ISM PRESS** (Shanghai, 2025).

This repository is the book: a single-page interactive ebook with a butterfly page-flip. There is no build step, no package manager, and no application backend. Open `index.html` and read.

**Read it live:** [100days.nonarkara.org](https://100days.nonarkara.org) · [solitude.nonarkara.org](https://solitude.nonarkara.org)

---

## What it is

The cover calls it *an illustrated travelogue, after the writings of* Non — a Thai anthropologist who wrote himself one hundred days between Shanghai and the Yangtze. The book is told in a fond third person. The colophon in the afterword says the passages quoted directly come from the writings of *nonharvard*, 2015–2025; the rest is invented around that record.

The reader is a bound spread on a dark stage. On the cover the book idles with a slow *butterfly-rest* motion. Turning a page is a 3D CSS flip (perspective `rotateY`), not a scroll. Thirty-six spreads run from the cover through a map, a small practice for writing a hundred days, twenty-four numbered chapters, a nonism dictionary, the colophon, and a library of other books from the same press.

It is a literary work first. The code exists so the pages can turn.

---

## Open and run

The book is `index.html`. Everything else the reader needs is in that file (markup, styles, and the page-flip script). Display type is loaded from [Google Fonts](https://fonts.google.com/) (Cormorant Garamond, EB Garamond, Caveat, Josefin Sans); system serif and sans fallbacks are declared if those requests fail.

**Fastest:** open the file in a browser.

```sh
# from this directory
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

Or double-click `index.html` in a file manager.

**Local HTTP origin** (optional; useful if a browser restricts `file://` storage):

```sh
python3 -m http.server 8000
```

Then visit [http://localhost:8000/](http://localhost:8000/).

No install, no `npm`, no compile. A static host that can serve `index.html` is enough to deploy. This repo includes a Cloudflare Pages [`_headers`](_headers) file that disables caching on the HTML document so a new spread or fix is not stuck behind an old page.

---

## How to read

| Control | Action |
| --- | --- |
| Click the right half of the stage, or the right edge | Next spread |
| Click the left half of the stage, or the left edge | Previous spread |
| `→` `↓` `Space` | Next spread |
| `←` `↑` | Previous spread |
| Swipe left / right | Next / previous (touch) |
| Menu button (top left) | Table of contents |
| `Esc` | Close the contents drawer |

On a narrow screen the reader shows one page of the spread at a time (the prose side, with a few left-page exceptions).

If you have been here before, a *continue reading* notice may appear on the cover. The last spread and a short visited-spread list are stored in this browser only, under keys prefixed `100days:`. Nothing is sent to a server for that.

---

## Spreads

Thirty-six spreads, in the order of the contents drawer:

0. Cover
1. Foreword — On a small life carefully lived
2. A map of the wandering
3. Why This Exists
4. The Practice
5. Your 100 Days — A Framework
6. I. By the bank of the Huangpu
7. II. Of his coffee addiction
8. III. On Death, and his father's flask
9. IV. Why he (gave up) love
10. V. On riding a train
11. VI. Writing by the Yangtze
12. VII. A bicycle technician in bad faith
13. VIII. Forty-four books, more or less
14. IX. His butterfly dream
15. X. On loneliness
16. XI. A corner café, mid-afternoon
17. XII. Kodawari, or, the long pursuit
18. XIII. A boat, mid-river
19. XIV. The power of now, told by a cicada
20. An interlude — Rain in the city
21. — Interruption —
22. XV. The saddest sonnet
23. How he got out of the darkest time
24. XVI. One small return
25. XVII. An accidental minimalist
26. XVIII. Home is where the heart is
27. XIX. A small roof, a small moon
28. XX. The discipline of small things
29. XXI. On freedom
30. XXII. A small nonism dictionary
31. XXIII. What he knows for sure
32. XXIV. The hundredth day
33. Afterword & Colophon
34. — FIN —
35. The Library — more from Non

The last spread points to other NON·ISM PRESS books already on the same domain family:

- [Ninja Innovation](https://ninja.nonarkara.org)
- [The Things You Can See Only When You Slow Down](https://slowdown.nonarkara.org)
- [What I Mean When I Say](https://mean.nonarkara.org)
- [Reading Dao De Jing with Dr. Non](https://dao.nonarkara.org)

---

## Files

| File | Role |
| --- | --- |
| [`index.html`](index.html) | The book: text, inline SVG plates, styles, and reader script |
| [`_headers`](_headers) | Cloudflare Pages cache rules (HTML is not cached) |
| [`LICENSE`](LICENSE) | MIT license for the reader software |
| [`README.md`](README.md) | This file |

Illustrations are inline SVG in `index.html` (cover figure, butterfly, practice diagram). There is no separate `assets/` folder in this tree.

---

## Author

**Dr Non Arkaraprasertkul** (the book signs itself *Non*). Urbanist, anthropologist, and novelist. The press line on the cover and back is **NON·ISM PRESS**. Further public work: [nonarkara.org](https://nonarkara.org).

The dictionary spread in the book defines *non-ism* as a general abstention — from Latin *non*, “not.” See also: the practice of leaving things alone.

---

## License and rights

The **reader software** in this repository — the HTML, CSS, and JavaScript that stage the book, flip the pages, open the contents drawer, and remember a place — is licensed under the [MIT License](LICENSE).

The book files do **not** include a separate license grant for the literary text or the illustrations. Those remain the author’s published work. The colophon attributes quoted lines to the writings of *nonharvard*, 2015–2025, and the rest to a third-person frame. Reading the book here, or studying how the reader is built, is the intended use. Reproducing the text or artwork as a standalone publication is a different question; ask the author if you need that.

Typefaces are loaded from Google Fonts under their own licenses (SIL Open Font License for the families named above). They are not part of this repository.

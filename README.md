# Hidden Subset

A mathematical deduction game built around the subset-sum problem, together with an interactive lab for exploring the structure behind it.

**By Elad Dafni.**

## Contents

- **[index.html](index.html)** — Game rules and instructions, with three carefully calibrated lists (162 / 1,871 / 6,679 possible combinations) that produce strategically protected sums.
- **[lab.html](lab.html)** — Interactive lab: define your own list, view the full decomposition spectrum, run an investigation with yes/no answers that shrink the suspect set, and explore an epicycle engine with three viewing-frame modes that demonstrate visually how Fourier-style counting recovers the exact number of subset decompositions.

## The Game in One Paragraph

Every player secretly picks a combination of numbers from a shared list, then publicly announces only its sum. From there, players take turns asking each other yes/no questions about which values are held ("Do you have 4 and 9?"), or declaring full accusations ("Your combination is 3, 5, 5, 8"). The lists are engineered so that a single sum has dozens — sometimes hundreds — of possible decompositions, so the announced sum reveals almost nothing on its own. The last player not eliminated wins.

## The Lab in One Paragraph

The lab lets you reproduce the game's analytic underpinnings: pick any list, see immediately how many combinations every possible sum has, simulate questioning a fictional opponent to watch the suspect set shrink in real time, and switch into a Fourier visualization where every possible sum is a rotating arm whose length equals its decomposition count. Three viewing-frame modes (lab frame, S-frame, and a symmetric ω = S/2 intermediate) make the Fourier extraction of the count `c_S` geometrically visible, with a live X(t) chart showing convergence.

## Hosting on GitHub Pages

1. Create a new public GitHub repo and add the three files: `index.html`, `lab.html`, `README.md`.
2. Settings → Pages → Branch: `main` → Save.
3. Within about a minute the links are live:
   - Game rules: `https://USER.github.io/REPO/`
   - The lab: `https://USER.github.io/REPO/lab.html`

## Technical Notes

Both files are fully self-contained — no backend, no build step, no local dependencies. Fonts load from Google Fonts; the lab persists state in browser `localStorage`. Works from any domain.

The lab's epicycle engine and detector are mathematically verified: the running average of `f(t)·e^{-2πiSt}` converges to `c_S` (the exact decomposition count of sum S), and this has been numerically tested against the calibrated lists above.

## License

This project ships with a **dual license** — see [LICENSE](LICENSE) for the full text.

- **Code** (HTML structure, CSS, JavaScript, test harness): **MIT License**. Reuse the implementation freely; just keep the copyright notice.
- **Creative content** (written rules, explanatory text, calibrated lists, decomposition analysis, prose, diagrams, visual presentation): **Creative Commons Attribution 4.0 International (CC BY 4.0)**. You may share and adapt — including commercially — provided you credit *Elad Dafni* and link the license. This does not assert rights over abstract game mechanics or subset-sum mathematics.

Combined, the license lets you fork and build on the technical work freely, while keeping attribution for the game design.

---

## Independence

Hidden Subset is an independent game and is not affiliated with, endorsed by, or sponsored by any other deduction game or publisher. Any resemblance to existing games in the deduction or code-breaking genre reflects shared mathematical territory, not derivation.

## Version

**Version 0.1 · June 2026** — Initial public release.

---

**צירוף סודי** — Hebrew version (separate repo).

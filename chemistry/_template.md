# AP Chemistry Article Template (Writer's Guide)

> This file is the authoring template for every article in the `chemistry/` folder.
> It is NOT linked in the sidebar — it exists so every post follows the same pattern
> the best calculus articles established (see `calculus/taylor-series.md` for the
> gold-standard example of voice and opener style).

---

## The Article Skeleton

Every article follows this exact structure, in this order:

```markdown
# Article Title
<p class="article-date">Month D, YYYY</p>

*[STORY OPENER — see rules below. Italic paragraph, 4–8 sentences.]*

---

## What You'll Learn
- 6–9 concrete "you will be able to" bullets

---

## Prerequisites
- [Linked Article](/chemistry/xxxx-article-name) — one-line reason it's needed
(Omit this section only for the first articles that have no prerequisites.)

---

## The Core Concept

### Intuition First
[Extend the opener's story/analogy here — the analogy must RECUR, not be a throwaway.]

### [Formal definitions, key formulas in display math, reference tables]

---

## Worked Examples
[8–12 numbered examples: **Example N: Descriptive Title**, each with
**Problem:**, **Solution:** with explicit Step 1/2/3, and a bolded **Answer:** line.]

---

## Common Mistakes
[Table or bullets: the mistake, why it happens, how to avoid it.]

---

## AP Exam Tips
[How this topic appears on the AP Chem exam; scoring notes; calculator notes.]

---

## Practice Problems
[12–15 problems. Every solution hidden in a collapsible block:]

### Problem 1
Question text...

<details>
<summary><strong>Solution</strong></summary>

Full step-by-step solution, ending with a bolded answer.

</details>

---

## Quick Reference
[Optional closing cheat-sheet table for the topic.]

---

<div align="center">

[← Previous Title](/chemistry/xxxx-prev-article) | [Next Title →](/chemistry/xxxx-next-article)

</div>
```

---

## The Story Opener (Required)

Every article starts with an *italic* paragraph directly after the date. Rules:

1. **Start in real life, not in chemistry.** Open with a familiar scene — kitchen,
   beach, boba shop, movie night, a rocket launch livestream, Dad's printer lab —
   then pivot to the concept.
2. **The analogy must be structural, not decorative.** Its parts must map onto the
   concept's parts (like weighing a rice bag at Costco → counting by weighing →
   molar mass, in The Mole article).
3. **End with why it matters** — where the topic sits in AP Chemistry and what it
   unlocks.
4. **Reuse the analogy inside "Intuition First."** The opener plants the story;
   the intuition section grows it.

## The Persona (Voice)

The author is **Ganga** — a San Diego high-school student who just earned a 5 on AP
Calculus BC and is now learning AP Chemistry from scratch, blogging as she goes.

**Theme palette for story openers.** Pick ONE theme per article, and make each
article's theme different from its neighbors — variety keeps the blog fresh:

- **Kitchen & home** (PREFERRED — simplest and most relatable) — baking, cooking,
  cleaning, laundry, the fridge, measuring cups, kitchen scales
- **Sports & fitness** — swimming, soccer, running, why muscles burn, sports drinks
- **Food & drinks** — boba, Starbucks, baking, Costco runs
- **San Diego life** — Torrey Pines and the beach, drives to LA with Dad, earthquakes
- **Biochemistry in real life** — caffeine, sunscreen, blood pH, why ice cream
  melts on your tongue
- **Movies & sci-fi** — The Martian (Watney makes water from hydrazine — real
  stoichiometry), Interstellar, superhero team-ups, detective films, Apollo 13
  (the $\ce{LiOH}$ CO2-scrubber scene — gas laws/stoichiometry), Star Trek's
  "Arena" (Kirk makes gunpowder from raw ingredients), MythBusters
- **Dr. Stone (anime)** — first-class theme source: rebuilding civilization
  through chemistry from scratch (soap/surfactants, glass, iron, batteries,
  sulfa drugs), TV-14, real chemical reasoning; great for Units 4–9
- **Breaking Bad — CURATED SCENES ONLY** — the classroom and survival chemistry
  is fair game: the "chemistry is the study of change" pilot speech, the
  chirality lecture (Unit 2), the desert galvanic-cell battery build (Unit 9),
  Jesse's "Yeah, science!" as a fun aside. HARD RULE: never reference the drug
  synthesis plotline, purity, or "cooking" in any form; frame as famous-scene
  references (the show is TV-MA — don't tell readers to go watch it); every
  reference must be self-contained so a reader who's never seen it still gets
  the point
- **Space** — rocket launches, Mars rovers, star colors, the night sky
- **Ink & printing tech** — Dad works at HP on printers and ink, so precision ink
  droplets (picoliters!), microfluidics, and "how does an inkjet even work" are
  dinner-table material
- **Everyday tech** — phone batteries, screens, headphones

Default to the SIMPLEST theme that fits the concept — kitchen, home, and sports
beat clever ones. A reader should recognize the scene instantly, no explanation needed.

## Optional Recurring Device: "Hollywood Chemistry: Real or Not?"

When a topic has a famous movie/TV chemistry moment, add a short blockquote
sidebar (2–6 sentences) that fact-checks it — enjoying the scene while being
smarter than it. Format:

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* [one-sentence description]
> *The verdict:* [what's real, what's exaggerated, and the actual chemistry]

Queued examples: the Breaking Bad bathtub scene (HF barely attacks tissue that
way — but it IS stored in plastic because it etches glass, and it's famously a
WEAK acid → Unit 8); fulminated mercury (MythBusters: mostly busted → Unit 4);
thermite (real! → redox units); The Martian's hydrazine water (real stoichiometry
→ Unit 4). Use at most ONE per article, and only when it genuinely fits the topic.

**Do NOT use robotics as a theme.** Keep every story VERY simple and real — the
reader is a high schooler meeting chemistry for the first time, and the goal is
curiosity ("wait, THAT's chemistry?"), not impressiveness. Do not invent new major
biographical facts beyond the list above. Small everyday details (homework, lunch,
phone battery) are fine. Write "you and I are figuring this out together," not
lecture-hall formal. Short sentences are fine. Enthusiasm is fine.

---

## Chemistry Notation (mhchem is available)

The site's KaTeX bundle includes **mhchem**, so use `\ce{...}` inside math dollars
for ALL chemical formulas and equations:

| What | Write | Renders as |
|---|---|---|
| Formula | `$\ce{H2O}$` | $\ce{H2O}$ |
| Ion | `$\ce{SO4^2-}$` | $\ce{SO4^2-}$ |
| Isotope | `$\ce{^{14}_{6}C}$` | $\ce{^{14}_{6}C}$ |
| Reaction | `$\ce{2H2 + O2 -> 2H2O}$` | $\ce{2H2 + O2 -> 2H2O}$ |
| Equilibrium | `$\ce{N2 + 3H2 <=> 2NH3}$` | $\ce{N2 + 3H2 <=> 2NH3}$ |
| States | `$\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$` | $\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$ |
| Heat over arrow | `$\ce{CaCO3 ->[\Delta] CaO + CO2}$` | $\ce{CaCO3 ->[\Delta] CaO + CO2}$ |

Regular math (logs, scientific notation, algebra) uses normal KaTeX:
inline `$3.0 \times 10^8$`, display `$$\text{pH} = -\log[\ce{H+}]$$`.

**Never write bare formulas in plain text** (H2O, CO2) — always `$\ce{H2O}$`, `$\ce{CO2}$`.

**CRITICAL — escape currency dollar signs.** A literal `$` in prose (prices: "a \$6.25 boba")
MUST be written `\$`. One unescaped `$` flips every math/text region in the rest of the
page — the KaTeX plugin pairs `$` delimiters document-wide, so a single stray one inverts
all math after it and leaks raw `begin-inline-katex` markers into the rendered page.

---

## File & Navigation Conventions

- Files live in `chemistry/`, named `NNMM-kebab-case-topic.md`:
  - `00MM` = Getting Started, `01MM` = Unit 0a (Math Toolkit),
    `02MM` = Unit 0b (Chemistry Foundations), `03MM` = AP Unit 1, and so on.
- Every new article gets a row in `_sidebar.md` under the AP Chemistry section.
- Prev/next footer links omit the `.md` extension: `(/chemistry/0101-scientific-notation)`.
- Motivational articles (Why Chemistry Matters, History) may relax the
  worked-examples/practice-problems counts, but keep the story opener,
  learning objectives, and navigation footer.

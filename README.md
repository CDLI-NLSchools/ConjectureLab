# Conjecture Lab

Conjecture Lab is a single-file practice app where students learn the conjecture-then-test loop: examine a few cases of a pattern, state a conjecture in their own words, predict fresh cases, run the test, and revise the conjecture when the evidence calls for it. One mode is a deck of famous patterns that look convincing and then break, teaching that confirming cases never prove a claim.

Math 2201 Unit 7: Inductive and Deductive Reasoning (indicators 2.1, 2.2, 2.3, 2.9)

## How students use it

- **Explore mode** generates a fresh pattern each round (number sequences, matchstick and tile figures shown as rows of tiles, calendar block sums, and a data table of cans stacked in a pyramid). Students predict the next two cases, write their conjecture, then run the test to compare their predictions with the pattern values and read the rule.
- **Trap Deck mode** presents patterns engineered to break late: circle regions that double five times and then give 31 instead of 32, pancake cuts that stop doubling, and the expression n^2 + n + 11, which gives prime values until n = 10 gives 121. After the break, students write a revised conjecture.
- **Problem mode** gives guided pattern problems (handshakes, staircase blocks, tiles around a garden border, and a plus-sign cross on the hundreds chart). Students study the small cases, conjecture the value of a larger case, and read feedback that shows the rule and why it works.

Every round a student checks is added to the **Conjecture Record** at the bottom of the page (pattern name, cases examined, conjecture stated, test result, and any revision), along with a free-text notes box. A Print button prints just the record sheet, using the print stylesheet, so students can submit it to an assignment folder if the teacher asks.

## Tech note

Single HTML file (`index.html`), no dependencies, no network calls, no storage: it works fully offline and generates every practice item fresh at runtime from parameterized families. `harness.js` is a Node check script that extracts the generator code from `index.html` and verifies it against independently written closed forms across thousands of seeded draws; run `node harness.js` and expect `OVERALL: PASS`.

GitHub topics when published: math-2201, inductive-deductive-reasoning, draft (draft removed after QA).

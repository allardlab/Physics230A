# In-class polls

Question sets for PollEverywhere, one CSV per activity, imported into PollEverywhere by hand.

**Everything in this directory is published**, this README included.
`deploy.sh` copies `website_assets/` into the built site whole, and the landing page links each CSV as a `[Teacher]{.tag}` material so that a future instructor can import it too.
That is fine for a warm-up poll, which carries no answers and repeats questions the problem sets already ask in public.
A poll that must not be seen before class --- one with answers marked, or one that previews an exam --- does not belong here; keep it out of `website_assets/` altogether.

## The CSV format

One header row, then one row per question:

```
Activity,Type,Title,Option,Option,Option,Option,Option,Option
Poll,Multiple choice,1. Number of amino acids in the average human protein,I don't know,10 or fewer,...
```

- The number of `Option` columns in the header is the most options any question has; a question with fewer leaves its trailing cells empty.
- The file is UTF-8, for the superscripts and `µ`.
  Check the first imported question on screen: if `10⁻⁹` has come out as mojibake, the importer has read it with a different encoding.
- Avoid commas inside a cell.
  Quoted fields are valid CSV, but there is no reason to find out whether the importer agrees.
- The CSV carries the question and its options only.
  How the poll is run --- one question at a time, when results are shown --- is set in PollEverywhere after import.

## `PS0_scavenger-hunt_polleverywhere_polls.csv`

A warm-up for `homeworks_outbound/PS0_scavenger-hunt.qmd`, run before the students start it.
Its twenty questions are PS0's twenty items, in the same order and with the same numbers, so that a student can carry a hunch from the poll into the problem set.
**Rewording an item in PS0 means rewording it here too**; nothing checks that the two agree.

It is run synchronously: the whole class answers Q1 on their phones, the results go up, and the class talks about the spread before moving on to Q2.
**No answer is ever revealed**, and none is marked correct in the CSV.
Most of these questions have no answer without caveats --- which cell, which protein, which reflex --- and finding the caveats is what PS0 is for.

How the options are chosen:

- **`I don't know` is always first**, so it is where a thumb lands and costs nothing to pick.
  It keeps the histogram honest: a guess forced into a bin looks like a belief.
- **Five bins besides it**, open-ended at both ends ("or smaller", "or more"), so every answer has somewhere to go.
- **The textbook value is not always the middle bin.**
  A class learns within three questions that the middle is safe, and then the poll measures that instead.
- **Questions meant to be compared share a set of bins**, so the shift between them is visible on screen: Q3--5 (eukaryotic cell, bacterium, nucleus), Q6, 7, 10 and 11 (membrane, protein, water, DNA), Q8--9 (light and electron microscopes), Q14--16 (transcription, translation, reflex) and Q18--20 (the energies).
- **Bins are a decade apart except where the plausible range is wider.**
  Q1 steps by half-decades, since its interesting range is only two decades, and Q17 (protein folding, microseconds to minutes) by two decades, since five one-decade bins could not span it.
- **Energies are given in J, pN·nm and eV together**, 1 pN·nm being exactly 10⁻²¹ J and 1 eV about 1.6 × 10⁻¹⁹ J.
  The eV column all but answers Q20 for anyone who knows a resting potential is about 70 mV, which is acceptable: it is also exactly the connection the question is there to make.

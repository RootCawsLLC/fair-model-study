# FAIR Taxonomy Drill

A study drill for the FAIR risk taxonomy in three modes: walk the factor tree as a branching diagram
with names and units showing and every definition a tap away; rebuild it from a shuffled pool with
them hidden; and match all twenty-two definitions to their names.

**Live:** https://rootcawsllc.github.io/fair-model-study/

![Walk mode with a UK financial-services data-breach benchmark loaded. The thirteen factors are drawn as a branching tree, Risk at the top, its two children below it and so on down to the six leaves, each box carrying an abbreviation, a name and a unit badge. Loss Event Frequency and Loss Magnitude are tinted amber with a "sourced" tag. A detail strip under the diagram shows the selected factor's definition, its sourced range in events per year, and what it feeds and is built from. A worked-example panel beneath explains that two of thirteen factors have a published number, and lists the sources behind them](preview.png)

## What it does

- **Walk the tree.** All thirteen factors as a branching diagram, each with the unit it carries
  (money, probability, or a frequency). Tap a factor for its plain-language definition, what it
  feeds and what it is built from; an outline view lists every definition at once and takes over
  on narrow screens. Load a source-backed scenario onto it and exactly two factors fill in, because a published loss study
  reports how often the event happens and what it costs, and nothing beneath. The eleven empty
  factors are not missing data; they are where the analysis has to enter.
- **Rebuild it.** The tree empties. Pick a factor from the shuffled pool, tap the slot where it
  belongs, then answer its unit. Placement and unit accuracy are
  scored separately.
- **Match definitions.** Twenty-two names on one side and twenty-two definitions on the other:
  the thirteen factors, the six forms of loss, and the three sub-factors of Probability of
  Action. Categories are revealed as items match, so they cannot be used as hints.

The definitions are written for the drill in plain language. They follow the FAIR taxonomy but
are not the standard's own text; for the authoritative wording go to the published standard.

## Build

Single self-contained `index.html`: React 18 via UMD CDN, no build step, no dependencies. Styled in
the RootCaws palette: powder-rose surfaces, warm ink, rose accent, Fraunces for display type and
Inter for everything else.

## Running locally

Serve the directory with any static server so the relative fetch of `risk-benchmarks.json`
works, for example:

```bash
python -m http.server 8000
```

Then open http://localhost:8000. If the benchmarks file is unreachable the worked example says
so; the drills do not depend on it.

## Status

Built as a training exercise: a study aid for learning the FAIR taxonomy, and for learning how
this kind of interaction is put together.

The taxonomy follows the FAIR Model Standard Artifact Version 3.0 (January 2025) published by the
FAIR Institute. This is a study aid, not a substitute for official FAIR training material.
The FAIR Model™ is a trademark of the FAIR Institute.

Worked-example data comes from [risk-benchmarks](https://github.com/RootCawsLLC/risk-benchmarks),
which derives it from [RiskShard](https://github.com/raviaxo/RiskShard) by
[raviaxo](https://github.com/raviaxo), AGPL-3.0. The mapping of a shard onto FAIR factors is this
project's own, and it is deliberately shallow: the shard's frequency range is Loss Event
Frequency and its impact range is Loss Magnitude, with no attempt to derive the factors beneath
them, because nothing in the source supports that derivation. See
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## License

Copyright (c) 2026 RootCaws LLC.

[GNU AGPL v3 or later](LICENSE). If you modify this and run it as a network service, the AGPL requires you to offer your users the modified source under the same terms.

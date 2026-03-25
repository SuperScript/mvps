# mvps

A Claude Code plugin for designing and analyzing MVPs (Maximally Valuable
Problems). Reframes the traditional "Minimum Viable Product" around hypothesis
testing and revealed preference rather than feature minimization and product.

## Skills

### MVP Creation

Guides a structured conversation to produce a testable hypothesis grounded in
revealed preference, a pre-committed threshold test, and a concrete experiment
design. Outputs a markdown file.

Triggers: "create an MVP", "plan an MVP", "validate my idea", "test a
hypothesis", "design an experiment for my idea"

### MVP Analysis

Guides post-experiment analysis of results against the pre-committed threshold
test. Focuses on what the outcome means and what to do next — not on whether
the outcome feels good. Challenges confirmation bias directly.

Triggers: "analyze MVP results", "review experiment results", "did the MVP
pass", "post-experiment analysis"

## Installation

Add the plugin to your Claude Code configuration:

    claude plugins add /path/to/mvps/plugins/mvps

## Structure

    plugins/mvps/
    ├── .claude-plugin/plugin.json
    ├── references/
    │   ├── mvp-file-format.md
    │   └── mvp-analysis-format.md
    └── skills/
        ├── mvp-creation/
        │   └── SKILL.md
        └── mvp-analysis/
            └── SKILL.md

## Core Ideas

**MVP = Maximally Valuable Problem.** The MVP is not the product. It is a test
of whether the problem exists and drives behavior.

**Revealed preference over stated preference.** Design every experiment to
observe what people do, not what they say. Survey data and interview quotes are
not evidence of demand.

**Pre-committed threshold tests.** A hypothesis without a pass/fail threshold
set before the experiment is useless. The threshold prevents post-hoc
rationalization.

**50% is the optimal pass rate.** A team that passes every test is setting weak
thresholds. A team that fails every test is disconnected from reality. A
roughly even split means the team is testing at the frontier of its knowledge.

## License

BSD 3-Clause. See LICENSE.

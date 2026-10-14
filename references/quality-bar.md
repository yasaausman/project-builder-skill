<!-- Loaded by SKILL.md. Moved here verbatim from SKILL.md on 2026-10-13. -->

## The quality bar  *(applies to every build — daily projects and hackathons alike)*

A well-built project isn't the one with the most features; it's the one whose value is
obvious, proven, and finished. Hold every build to these, and check them before calling
anything "done":

1. **Aim at what actually gets rewarded.** Before scoping, name the "judge" and what they
   reward, then build straight at the center of it — don't build a clever thing and bend it to
   fit. The judge varies by context:
   - *Daily-use / personal tool* → future-you and real users: does it do its real job reliably,
     every day, without babysitting?
   - *Portfolio / job-seeking* → a skeptical engineer or recruiter skimming for 60 seconds.
   - *Hackathon* → see the Hackathon layer (`references/hackathon.md`).
   The value should be obvious in ~5 seconds. If you can't say what it's for in one sentence,
   the scope is wrong.
2. **Make the core technology load-bearing, not decorative.** The interesting/hard piece (the
   AI, the algorithm, the integration) should be so central the project falls apart without it.
   If it's a garnish, either make it essential or cut it.
3. **Prove it in a way a skeptic can reproduce.** A working demo runnable in **one command**
   with no fragile infrastructure — never stake it on a live laptop, a flaky tunnel, or an API
   that can die mid-use. Back claims with deterministic checks or committed sample runs/tests
   that show it genuinely works. "Trust me" is not proof.
4. **Go narrow and deep.** One flawless, fully-finished flow beats eight half-working features —
   "done" always reads better than "ambitious but unfinished." Freeze scope early; spend the
   back half hardening the one core beat, not adding more.
5. **Earn the near-free points most people skip.** Treat docs and presentation as first-class
   *from day one*, not slapped on at the end: a clear README, an architecture sketch,
   screenshots, and (where it fits) a tight 2–3 min demo with a problem→payoff arc. For projects
   built on someone's tool/library, engage upstream — file an issue, open a PR, log real feedback.
6. **Polish and personality compound.** Clean architecture, strong branding, a memorable voice,
   and a core action that looks and feels great. When a substantive, well-fit, provable project
   is *also* presented with real polish, it's very hard to beat. Where you can choose, prefer an
   idea whose payoff is inherently visual or emotional — it makes everything above easier.

Reflect these in the deliverables: `PLAN.md` should state the "judge" and the one core flow;
each milestone's "Done when" should include the reproducible-proof check; `PROJECT.md` tracks
the polish/docs/demo tasks as real work, not afterthoughts.

# NOT.7 - Redesign a Notation around the Reader's Difficult Operations: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.7:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.7:5.1 - Turn prerequisite lookup into downstream search {#turn-prerequisite-lookup-into-downstream-search}

A small dependency account gives the immediate inputs of four tasks:

| Task | Immediate inputs |
| --- | --- |
| A | None |
| B | A |
| C | A |
| D | B and C |

This form answers “what does D need?” directly: B and C. The new working question is “after A changes, which tasks may need reconsideration?” The reader must repeatedly search the input column for dependents, then do so again for each newly found task.

Construct the reverse index: `A → {B, C}`, `B → {D}`, `C → {D}`, `D → {}`. Here an arrow goes from a supplied input to a task using it. Starting at A, follow arrows and retain newly reached tasks until none remains. The resulting set is {B, C, D}; D is retained once even though two paths reach it.

The repair changes the lookup arrangement and supplies a reading procedure. It does not add a new dependency. It makes the required direction directly available, but finding the immediate inputs of D is now less direct. Keep the original table as a complementary view if that operation remains frequent, using NOT.6 to maintain the connection.

Now remove C from D's input list. Remove the arrow from C to D as well. A still reaches D through B. A reader who merely drops D from the downstream set has confused removal of one path with removal of every path. The changed case tests the reading operation, not the prettiness of the index.

This construction demonstrates the dependencies and operations preserved. It supplies no measured claim that every reader finds the index faster; the local display and reading conditions can change that comparison.

### NOT.7:5.2 - Share a parameter while retaining a local exception {#share-a-parameter-while-retaining-a-local-exception}

Three quoted amounts use the same tariff, 3 units per item, for quantities 2, 5 and 7. The expressions are `3*2`, `3*5` and `3*7`. Their intended common assumption is known, but the written expressions repeat it independently.

To make a common tariff change local, introduce `p = 3` and write `p*2`, `p*5` and `p*7`. A change to p = 4 then gives 8, 20 and 28. There is one tariff definition to change, while a reader of an individual expression now follows p to that definition. The definition must remain accessible.

The next request keeps the second quote at the old tariff and changes the others. A global change of p alone cannot express that request. Write the second expression as `3*5`, with its fixed-tariff meaning stated, while the others remain `p*2` and `p*7`. The amounts are now 8, 15 and 28. If later exceptions acquire their own shared rule, give that rule its own name.

For work dominated by common tariff changes, the shared parameter can be useful. For independently negotiated quotes, the assumption of a common tariff may be wrong. The notation repair therefore needs the subject's sharing relation; identical printed numbers alone do not establish it.

## NOT.7:6 - Bias-Annotation {#bias-annotation}

A designer's fluency can hide the work a new reader performs. Recover an actual route or state the preparation assumed by a design estimate. When the author supplies missing information during use, include it among the enabling contributions.

Optimizing a visible measure can also remove the method's value. A shorter inscription can hide the dependency needed for a change. Compare the operation and its result before treating size or edit count as an improvement.

## NOT.7:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| Replacing symbols while leaving the same search or reconstruction work | Change the arrangement or operation responsible for the difficulty. |
| Hiding a repeated value behind a name whose definition cannot be found | Provide the reference and include its lookup cost in the comparison. |
| Treating equal printed values as a common parameter | Recover the subject's sharing relation; :5.2 exposes the local-exception consequence. |
| Claiming a notation succeeds after its author supplied the missing explanation | Retain what the initial expression supplied and what the assistance added. |
| Declaring a universal winner from symbol count or one favorable task | Compare the relevant operations and their trade-offs. |
| Requiring an empirical study before a bounded useful correction | Use sufficient current evidence or a reversible, qualified design estimate. |

## NOT.7:10 - Architectural Rationale {#architectural-rationale}

The unit of redesign is the reader's operation on meaningful content. Appearance matters through what it makes available, distinguishable or changeable in that operation. This lets the method apply to formulae, diagrams, programs and other notations without prescribing one visual style.

Meaning preservation and ease of use answer different questions. A transformation can preserve the result while making its construction harder to inspect. Conversely, a helpful explanation may add missing content. Keeping those contributions separate permits a fair comparison without forbidding useful combined repairs.

An activity-relative choice also avoids inventing a universal quality scale. The existing characterization and contribution methods compare the relevant gains and burdens. Notational engineering supplies the constructions and the operation-level differences those methods need.

## NOT.7:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Blackwell and Green, [Notational Systems: The Cognitive Dimensions of Notations Framework](https://www.cl.cam.ac.uk/~afb21/publications/BlackwellGreen-CDsChapter.pdf), 2003, §§2 and 4 | Historical foundation for activity-relative trade-offs among notation, editing environment and medium. Use it to diagnose burdens in :4.2–.3, not as a universal score or evidence of a particular reader effect. |
| Kruchten, McNutt and McGuffin, [Metrics-Based Evaluation and Comparison of Visualization Notations](https://ieeevis.b-cdn.net/vis_2023/pdfs/v-full-1328.pdf), 2023, §§1–4 | Adopt matched examples and computed measures as aids to close comparison in :4.5 when several reusable alternatives warrant that work. The measures do not replace interpretation or establish usability by themselves. |
| Brazauskas and colleagues, [PUX Explorer and PUX Matrix study](https://ppig.org/files/2024-PPIG-35th-brazauskas.pdf), 2024, §§5–7 | Adapt problem/solution co-development into :4.3 and retain existing benefits during repair. Six specialist music-notation researchers supplied bounded, mixed feedback; the study does not establish universal effectiveness or empirical quality coefficients. |

**Choice of repair method.** A local walkthrough can settle an explicit lost dependency or burdensome edit. Activity-based diagnosis helps discover the trade-off when the trouble is less obvious. Matched galleries become useful for recurring comparisons across a family, but add construction and interpretation cost. Reader trials answer a remaining recoverability question when their outcomes can alter the choice. None of these methods replaces subject correctness.

The synthesis connects those notation-design methods with C.2.8's qualified structural comparison and the existing marginal-choice methods. Keep design estimates, measured responses and formal preservation arguments at their own scopes. Reopen when observed use defeats the proposed mechanism, a newly important operation changes the trade-off, or stronger evidence changes a claimed benefit.


## NOT.7:End {#end}

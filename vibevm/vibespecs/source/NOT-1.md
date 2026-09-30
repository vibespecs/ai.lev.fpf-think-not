# NOT.1 - Choose the Distinctions and Operations a Notation Must Support: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.1:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.1:5.1 - Same components, different composition {#same-components-different-composition}

A team is designing a diagram notation for constructing pipelines of functions. Its first sketch shows the input, output and an unordered collection of function names. The current operation is to determine the result and then exchange two functions without losing their connections.

Use the supplied functions `f(z) = z + 1` and `g(z) = 2z`, with input `3`. Applying `f` then `g` gives `g(f(3)) = 8`. Applying `g` then `f` gives `f(g(3)) = 7`. Both cases have the same named components. The unordered sketch therefore loses a difference that the operation needs.

The designer tries directed connections, with the rule that a connection passes the output of one function to the input of the next:

```text
3 -> f -> g -> result     gives 8
3 -> g -> f -> result     gives 7
```

Now the reader can recover the composition order and derive each result from the supplied functions. Exchanging the two functions changes their connections; merely dragging a box on the page must either preserve those connections or expose that it changed them. The design has acquired both an expression requirement and a question about the editing operation.

If the diagram is only an inventory of available functions, the original unordered sketch can remain adequate. If later work needs branching or shared intermediate results, try those operations before deciding how their connections and identities will be expressed. Success with this linear case leaves those questions open.

### NOT.1:5.2 - Same starting times, different durations {#same-starting-times-different-durations}

A notation for a sequence of signals lists their starting times in units of a shared pulse. Two sequences both start signals at `0` and `2`. In sequence A each signal lasts one unit; in sequence B each lasts two. The intervals are half-open: the signal is active at its start and inactive at its end.

For the question “when should each signal begin?”, the list `0, 2` suffices. For “is a signal active at time 1.5?”, it does not: the answer is no for A and yes for B. The omitted duration now changes the answer.

Try pairs of `(start, duration)`. Sequence A becomes `(0, 1), (2, 1)`; B becomes `(0, 2), (2, 2)`. The reader adds duration to start and compares 1.5 with the resulting interval. This exposes the needed difference with one simple convention. A timeline with interval bars might make repeated overlap questions easier; the pair notation is easier to transmit as plain text. Their comparative value depends on the operation and access.

If a performer's action determines the duration later, retain that unresolved value and identify which questions remain answerable. Suppose the first signal's duration is still to be chosen between 1 and 2. Write `(0, d)` with `d in {1, 2}, not yet chosen`. In either permitted case the signal is active at 0.5; at 1.5 the answer remains unresolved. Choosing `d = 2` makes the latter answer yes. The starting-time question remains answerable throughout. This continuation adds a requirement to preserve an unfinished choice, with no default that prescribes behavior the work has left open. Temporal and embodied notation design in NOT.8 develops such cases beyond this elementary timing example.

## NOT.1:6 - Bias-Annotation {#bias-annotation}

Fluency can hide a notation's demands. A designer who knows the answer may supply order, grouping or duration from memory while believing the expression carries it. Test the selected operation with only the expression, declared conventions and available context. C.2.8 distinguishes this expert judgement from an actual reader's recovery.

A successful notation for one audience can require unavailable preparation in another. Preserve the audience and operation when drawing conclusions; human reading results do not establish an AI agent's interpretation, or vice versa. Check the receiving conditions that can change the choice.

## NOT.1:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | What changes the next move |
| --- | --- |
| Choosing symbols from a concept inventory | Add the relation or operation that distinguishes cases. The pipeline inventory names both functions but loses their order. |
| Validating recognition while relying on manipulation | Try the required change. A reader's ability to name a diagram's boxes leaves the effect of moving or reconnecting them unresolved. |
| Requiring every difference to be written | Keep the simpler expression when the omitted distinction cannot change the selected result; the onset list suffices for starting times. |
| Completing an unknown to fit the notation | Express the unresolved choice or narrow the answerable question. A supplied duration would change the partly designed signal sequence. |
| Treating a familiar layout as shared context | Check what the receiver receives. Text export can remove grouping used in the displayed diagram. |

## NOT.1:10 - Architectural Rationale {#architectural-rationale}

A notation provides ways to form and use expressions. What to support depends on what the user needs to obtain or change. Starting with that operation connects the subject matter, reader preparation and representation without making any one of them a substitute for the others.

Contrasting cases make an omitted distinction consequential. If two cases with the same available representation require different answers, a reader using only that representation cannot be guaranteed the right answer in both. The design must recover the difference, obtain additional information or accept the resulting limitation. This argument identifies a requirement; trying the supported operation is still needed to learn whether the candidate is usable at the available effort.

The pattern chooses requirements through small constructive trials. NOT.2-.4 develop formation, interpretation and transformation rules. A.6.3.RT.OE addresses a different starting condition: the scheme is available and an operative expression must be built under it. C.2.8 characterizes what a prepared observer can extract; the present method uses that question to construct or choose a scheme. These contributions can be combined without making notation design a compulsory step in every reading task.

## NOT.1:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Blackwell and Green, [Cognitive Dimensions of Notations](https://www.cl.cam.ac.uk/~afb21/publications/BlackwellGreen-CDsChapter.pdf), historical foundation, especially the activity and system analysis sections | Adopt analysis relative to activity, notation, environment and medium. The method uses concrete operations to expose costs and trade-offs. It retains the source's warning that the dimensions are not a checklist yielding a universally best notation. |
| Brazauskas and Blackwell, [PUX Explorer](https://ppig.org/files/2024-PPIG-35th-brazauskas.pdf), PPIG 2024, §§2, 4.2 and 6 | Adapt the co-development of design problem and solution and the activity/experience comparison. Its study involved six specialist music-notation researchers. This supports a design aid at that scope, not general performance gains. Its trade-off weights were assigned from textual descriptions; they are not measured universal effects and are not imported here as quality scales. |
| Ross and colleagues, [Affordances of Sketched Notations for Multimodal UI Design and Development Tools](https://arxiv.org/abs/2508.09342), 2025 preprint, abstract-level contribution | Retain the distinction between isolated-symbol recognition and interpretation of a whole contextual sketch in AI-assisted work. The abstract motivates checking the receiving context. It does not establish a general advantage of a particular design or interpreter. |
| Kruchten, McNutt and McGuffin, [Metrics-Based Evaluation and Comparison of Visualization Notations](https://ieeevis.b-cdn.net/vis_2023/pdfs/v-full-1328.pdf), IEEE VIS 2023, §§3–4 | Reuse matched examples and their metrics to locate differences for closer reading when comparing working notations. The method assumes expressions implementing the shared tasks. Its metrics do not capture the whole user experience or supply a universally best notation. |

**Choosing the design move.** When the needed distinction is still unknown, construct a contrasting pair first. A gallery-based comparison already needs expressions that implement chosen tasks; preparing that gallery cannot replace discovering the missing task or distinction. Once several viable notations support a stable family of work, a shared set of examples becomes useful: compare the same readings and edits, use metrics to find costly cases, then inspect those cases. This costs more than the first pair but can expose repeated-change burdens hidden by one successful example. Reopen the small comparison when that broader burden could change the choice; NOT.7 develops the corresponding redesign. Cognitive Dimensions and PUX can also help discover or reformulate the operations to compare.

The contrast-based requirement construction and the two worked cases are the present synthesis. They connect notation design to available FPF representation, extraction and problem-development methods without prescribing one notation across practices.


## NOT.1:End {#end}

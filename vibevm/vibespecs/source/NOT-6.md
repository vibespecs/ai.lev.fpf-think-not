# NOT.6 - Coordinate Complementary Representations through Shared References: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.6:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.6:5.1 - Combine a formula, sample table and plot without freezing old values {#combine-a-formula-sample-table-and-plot-without-freezing-old}

A mathematical account defines `f(x) = 2x + b` for real x. A table stores its values at x = 0, 1 and 2, and a plot shows those same sample points with x horizontally and f(x) vertically. With b = 1, the table values are 1, 3 and 5.

The formula supports a value outside the table: f(3) = 7. The table supplies direct sample lookup; the plot exposes the relative positions of the samples. Connect each row's x to the formula input and each plotted point to that row's pair. The plot is generated from the table. Its agreement is not additional evidence that the formula describes some physical phenomenon.

Now the user requests f(1) = 4 while keeping the coefficient 2 fixed. The relation `2*1 + b = 4` gives b = 2. Recompute the table as 2, 4, 6 and move the plotted points accordingly; the formula now gives f(3) = 8. The old values at 0 and 2 were earlier derived values, not constraints freezing those points.

If the user instead requires f(0) = 1 and f(2) = 5 to remain, the three requested values cannot belong to a line of this form. f(0) fixes b = 1 and hence f(1) = 3. Expose the conflict. Choosing a different model or dropping a requirement changes the mathematical task; silently moving one representation would only hide it.

Finally, the three samples alone do not establish the formula for other inputs. Their generating formula is supplied here. If the table instead contains measurements, recover that different status before treating interpolation as a derivation.

### NOT.6:5.2 - Link a component label, an adopted dimension and a mesh {#link-a-component-label-an-adopted-dimension-and-a-mesh}

A drawing identifies a beam as B9. A dimension note gives its adopted modeling length as 2.00 m. A one-dimensional model uses the variable L for that length, and a computational representation divides it into twenty equal segments. A correspondence states that B9's adopted length supplies L and that segment length is `L/20`.

The reader can now identify which beam a segment calculation concerns and obtain 0.10 m per segment. B9, the variable L and a segment-array entry are different things connected by the stated construction. Replacing their names by one common name would not express that relation.

An accepted model revision changes B9's adopted length to 2.02 m while keeping twenty equal segments. Update L to 2.02 and recompute the segment length as 0.101 m. The component reference remains B9. A copied old segment length of 0.10 would contradict the new construction because twenty such segments total only 2.00 m.

Suppose instead that 2.02 m is a new observation while the dimension note still describes a nominal 2.00 m design. Those values can coexist. Keep their different meanings and let the modeling work decide whether its adopted L changes. The correspondence does not itself turn an observation into a revised design.

This example coordinates quantities and references. It establishes no claim that twenty segments are sufficient for a physical simulation; that is a separate modeling and computational question.

## NOT.6:6 - Bias-Annotation {#bias-annotation}

Visual agreement can be mistaken for independent support. Two displays generated from the same source share its error unless one checks a different contribution. Use the correspondence to distinguish repeated presentation from independent evidence.

The opposite tendency treats every difference as inconsistency. A nominal dimension and a measured dimension, or a prediction and an observation, can legitimately differ. Recover their claim and subject before choosing an update.

## NOT.6:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| Placing representations together and leaving their connection implicit | Construct the referent mapping and perform a joined reading. |
| Treating a shared label as identity between an object, its model and its encoding | State the relation between those different things, as in B9, L and the mesh. |
| Treating two generated displays as independent confirmation | Trace their common source and identify which new question a comparison can actually test. |
| Freezing all old displayed values during a local edit | Separate the changed requirement from earlier derived context; :5.1 shows the difference. |
| Erasing an observation to make it agree with a prediction | Preserve the observation and return the discrepancy to the subject account. |
| Adding another representation to every explanation | Retain it for a useful operation and compare the added navigation or maintenance burden. |

## NOT.6:10 - Architectural Rationale {#architectural-rationale}

Complementarity concerns operations, not media count. Two textual forms can support different work, while a text and picture can duplicate the same limited information. The useful whole consists of contributions and the relations through which they can be combined.

Reference and derivation are distinct relations. A variable may represent a quantity of a component; a table value may result from evaluating that variable's formula. Retaining those relations allows a change to reach the right contribution without making the representations or their subjects identical.

Update intention is also content. A finished state can conceal whether an unchanged value is fixed by the user or merely carried forward. Making that intention recoverable permits local propagation and reveals conflicting demands before one silently replaces another.

## NOT.6:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Ainsworth, [DeFT: A conceptual framework for considering learning with multiple representations](https://www.inf.ufpr.br/alexd/REPRESENTACOES_EXTERNAS/Ainsworth_2006.pdf), 2006, §§3–4 and 7.5 | Use the historical distinction between a representation's task contribution and the effort of relating it to another. It informs :4.1 and :4.4. Linked displays do not by themselves show that a reader has learned the correspondence. |
| Rexigel, Kuhn, Becker and Malone, [The More the Better?](https://link.springer.com/article/10.1007/s10648-024-09958-y), 2024, cognitive-load analysis, discussion and limitations | The synthesis reports benefits in studied STEM settings but also heterogeneous effects, publication-bias concerns and a small underlying basis for some load comparisons. Use this to bound the learning claim in :4.4, not to impose a number of representations or promise a gain for every reader. |
| Matsuda, Nguyen and Wang, [Lenses for Partially-Specified States](https://link.springer.com/chapter/10.1007/978-3-032-22723-2_2), ESOP 2026, §§1–2 | Adapt their distinction between whole displayed state and update intention into :4.5 and :5.1. Partial constraints can expose a compatible propagation or conflict. Their compositional guarantees depend on the formal construction; the ordinary method here does not confer them on arbitrary manual correspondences. |

**Choice of coordination.** A single sufficient representation avoids the effort of maintaining correspondence. Several become useful when their operations contribute to the actual answer. Manual labels and a direct rule can then be enough. Repeated edits across shared information can justify a maintained transformation; the 2026 partial-state approach addresses an important failure of replacing whole views indiscriminately. It also requires a model of update intentions and admissible merging. Choose that added construction when propagation and conflicts matter, rather than adopting it merely because several displays exist.

The synthesis retains cognitive and computational contributions at their own scopes: a formally consistent update need not be easy to understand, and an easy comparison need not preserve a user's edit. Reopen the chosen arrangement when a useful operation remains inaccessible, navigation or upkeep outweighs its gain, or a changed edit exposes an inadequate correspondence.


## NOT.6:End {#end}

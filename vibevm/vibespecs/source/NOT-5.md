# NOT.5 - Translate between Notations while Tracking Lost Distinctions: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.5:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.5:5.1 - Translate a dependency drawing without inventing geometric meaning {#translate-a-dependency-drawing-without-inventing-geometric}

A drawing has named nodes A, B, C and D. An arrow X→Y means that Y takes X's result as its direct input. Box positions carry no meaning. In one drawing the arrows are A→B and B→C; D is isolated. The receiver must determine C's direct input using ordinary text.

Construct this textual notation:

```text
nodes: A, B, C, D
direct-input pairs (supplier, receiver): (A, B), (B, C)
```

The reading rule selects the pair whose receiver is C and returns its supplier, B. Translating back draws one node per declared name and one arrow per pair. This recovers the named directed structure, including isolated D. It need not recover the original layout.

A list of node names alone fails. The second drawing with A→B and A→C would give the same list but a different answer for C. Retaining the pairs repairs that loss. Retaining only pairs would create a different loss: isolated D would disappear from a reconstructed drawing.

Now suppose horizontal position additionally records a planned start time. The earlier translation still answers the direct-input question, but it cannot reconstruct that timing. Add a start-time value for each node if timing is now needed. That extension follows a changed interpretation or question; it is not evidence that the original drawing already specified times.

### NOT.5:5.2 - Keep a useful count without pretending it preserves a rhythm {#keep-a-useful-count-without-pretending-it-preserves-a-rhythm}

A toy score is a sequence of four equally spaced cue positions. D and T name two distinct sounds; there are no rests. Translate a score into the counts of D and T. Both `D T D D` and `D D T D` become `D:3, T:1`.

The target answers how many sounds are required: four. It cannot answer which sound occurs second. In the first score it is T; in the second it is D. No reverse choice made from the counts alone can recover both originals.

For this family with one T, retain its position as a supplement. Counts plus `T-position:2` reconstruct `D T D D`: place T at position 2 and fill the remaining positions with D. This permits both the count and the second-cue question. If the score may contain several T cues, retain their positions, check that they are distinct and within the score, and check that their number agrees with the count. If rests or unequal intervals become relevant, the chosen description needs further distinctions.

The counts remain a sufficient result for inventory. Reconstructing performance order requires the supplement; reconstructing tempo would require a time scale that this toy score never supplied.

### NOT.5:5.3 - Choose what a backward update preserves {#choose-what-a-backward-update-preserves}

A plan describes two successive phases by `[A:3; B:5]`, in whole minutes. A summary notation shows only their total, 8. The recipient changes that total to 10. Several source plans fit: `[A:3; B:7]` and `[A:5; B:5]` both do. The new total does not choose between them.

Suppose the work requires A to remain fixed. Retain A's duration, 3, and reconstruct B as `new total - 3`. The requested total 10 gives `[A:3; B:7]`. Returning the unchanged total 8 recovers `[A:3; B:5]`; summing the updated plan returns 10. If instead B must remain fixed, the other update policy gives `[A:5; B:5]`.

Assume phase durations must be nonnegative. A requested total of 2 is incompatible with retaining A at 3. Report that conflict and obtain a changed requirement if the work allows one. Substituting B = -1 would preserve the sum while violating the admitted source plan.

## NOT.5:6 - Bias-Annotation {#bias-annotation}

A familiar target can look more definite than its source. Preserve the source's unresolved choices and restrictions where they affect the receiving use. A translator's chosen default is additional content.

Conversely, fear of information loss can make every conversion retain a complete original. Start with the actual question. The cue inventory needs counts; an editable score needs more. Retain the extra information when it opens a needed operation.

## NOT.5:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| Matching labels while losing their connections or scopes | Translate interpreted structure; the node/pair construction in :5.1 retains the required relation. |
| Recovering an arbitrary source and calling it the original | Exhibit the collapsed alternatives and retain the information needed to distinguish them. |
| Treating a useful summary as a complete substitute | Keep its successful use and add the missing information for the new question. |
| Returning a target answer outside the source's admitted cases | Restore the source restriction and the return argument. |
| Accepting a target edit by silently changing a protected source feature | Declare the backward policy and expose incompatible edits, as in :5.3. |
| Assuming a later format restores an earlier loss | Trace the needed distinction through the translation sequence or return to a retained source. |

## NOT.5:10 - Architectural Rationale {#architectural-rationale}

Translation changes the means through which an operation is performed. Its success therefore depends on both interpretation and the receiving operation. Two expressions may be interchangeable for counting and different for performing an ordered sequence.

The constructive loss test gives a local reason for a limit: when one target stands for two sources with different required answers, the target cannot by itself select the answer. Supplementary information repairs that failure only through a defined recovery operation.

Backward change is a further construction. Keeping one source feature fixed and changing another can realize the same target edit as a different policy. This is why two-way translation needs its own use conditions, and why continuing coordination of shared views belongs with NOT.6.

## NOT.5:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Foster, Matsuda and Voigtländer, [Three Complementary Approaches to Bidirectional Programming](https://janis-voigtlaender.eu/papers/ThreeComplementaryApproachesToBidirectionalProgramming.pdf), 2012, §§2–3 | Retain the historical construction of recovery from a view and a complement, and its treatment of partial backward updates. This grounds :4.5–4.6 without requiring complete invertibility of the forward view. Its pure-function setting does not cover every interactive conversion. |
| Xie, Schrijvers and Hu, [Effectful Lenses: There and Back with Different Monads](https://lirias.kuleuven.be/4268513), ICFP 2025, §§2.1–2.2 and 2.5 | Their effect-sensitive round-trip relations extend the pure setting. Use the consequence in :4.6: state which effects the return claim covers. Adopt no general promise that recovering values reverses external actions; implementing their formal framework is a separate computational construction. |
| Matsuda, Nguyen and Wang, [Lenses for Partially-Specified States](https://link.springer.com/chapter/10.1007/978-3-032-22723-2_2), ESOP 2026, §1 | Their shared-source problem shows why a copied value and an intended update constraint differ. Preserve that distinction in :4.6 and return multi-view coordination to NOT.6. The paper's stronger compositional results need its formal partial-state construction; this pattern does not infer them for arbitrary notations. |

**Choosing the translation method.** A bijection with transported operations is a strong choice when both notations express the same required information and a suitable inverse exists. It unnecessarily restricts a useful summary that deliberately omits detail. For that case, construct the receiving answer and retain only the information needed by the required return. A lens-style backward policy becomes useful when edits must propagate; it adds conditions and design choices that a one-way question need not carry. The pure view-and-complement account remains adequate for pure single-view conversions. Effects or interacting views select the stronger lines above when those difficulties actually occur.

This synthesis adapts those computational constructions to notation design by making the reader's operation determine the needed recovery. It does not claim that every diagram, performance or human interpretation already has an effective bidirectional implementation. Reopen the chosen method when a previously harmless loss obstructs a new question, an edit violates its preserved feature, or conversion effects change the relied-on result.


## NOT.5:End {#end}

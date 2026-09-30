# NOT.2 - Define Expression Rules for Recoverable Binding and Composition: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.2:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.2:5.1 - A sum with a local index and an external parameter {#a-sum-with-a-local-index-and-an-external-parameter}

A team is designing a compact notation for repeated addition. Its proposed expression is:

```text
sum i=1..2 of i + p
```

The notation has not specified where the summation body ends. At external parameter `p = 10`, two readings give different results: `(1 + 10) + (2 + 10) = 23`, or `(1 + 2) + 10 = 13`.

Choose a constructor `sum(index, lower, upper, body)`. It introduces the index only within `body`; bounds use the surrounding context. Choose `add(left, right)` for addition. These rules express the first reading as:

```text
sum(i, 1, 2, add(i, p))
```

The occurrence of `i` in `add(i, p)` reaches the local index declaration. The occurrence of `p` has no local declaration and uses the external value 10. Substituting the two index values gives 11 and 12, then 23. The second reading has a different construction:

```text
add(sum(i, 1, 2, i), p)
```

Its outer operation adds the external parameter once and gives 13. The notation now makes the two operand structures recoverable.

Naming also matters. The expression `sum(p, 1, 2, add(p, p))` is a valid expression under the chosen lexical rule, but both occurrences in its body refer to the index. It gives 6 and no longer uses the external parameter. To rename the index while preserving that parameter, choose a name such as `j` that does not capture it: `sum(j, 1, 2, add(j, p))` still gives 23. This example identifies the binding condition; NOT.4 supplies the general transformation method.

### NOT.2:5.2 - Two ports of the same type with different roles {#two-ports-of-the-same-type-with-different-roles}

A diagram notation describes a ratio operation. It has two numeric inputs, `numerator` and `denominator`, and a numeric output. The supplied rule divides the numerator by a nonzero denominator. Source A supplies 6 and source B supplies 3.

The first drawing joins both sources to an unlabeled box. Knowing that both connections carry numbers leaves their operand positions undecided. Choose named input ports and preserve their identities when the box is moved or redrawn:

```text
A: 6 -> ratio.numerator
B: 3 -> ratio.denominator
ratio.result -> answer
```

The result is 2. Reversing the two input connections is another well-formed construction with result 0.5. Port names make that change visible even though the input types remain the same.

Now enclose the ratio in a reusable component. Its exposed inputs refer to those two ports, and its output refers to `ratio.result`. Renaming the internal ratio box or changing its position can preserve those boundary connections. Swapping the connections changes the expressed operation. A rule that permits the former does not thereby permit the latter.

The same design question arises whenever compatible participants occupy different roles in a relation or operation. More elaborate diagram calculi can give the permitted connections and drawing equivalences mathematical definitions.

### NOT.2:5.3 - Scope in a structured sequence {#scope-in-a-structured-sequence}

Suppose `sequence(A, B)` means perform A and then B, and `repeat(n, S)` means repeat S n times. Then `repeat(3, sequence(A, B))` contains three performances of each action. `sequence(repeat(3, A), B)` contains three of A and one of B. A written delimiter, spoken grouping cue or learned gesture can carry this boundary if the receiver can reliably use its convention. The temporal realization and effort of perceiving or performing it are further questions for NOT.8.

### NOT.2:5.4 - Resolve a movable label at the time of its use {#resolve-a-movable-label-at-the-time-of-its-use}

Three physical cups have permanent numbers 1, 2 and 3, volumes 20, 10 and 0 ml, and capacity 50 ml each. Removable tags A, B and C initially mark cups 1, 2 and 3 respectively. An instruction H says to transfer 5 ml from A to B. Each letter refers to the cup bearing that tag when the transfer is performed.

Write `H; swap-tags(B, C); H`, where the swap moves only tags. The first H gives volumes `(15, 15, 0)` by permanent cup number. After the swap, B marks cup 3. The second H therefore gives `(10, 15, 5)`. Both transfers have sufficient source volume and destination capacity.

The abbreviation H retains a lookup to perform, not cup numbers fixed when H was defined. If the intended instruction instead bound A and B permanently to the original cups, the same two transfers would give `(10, 20, 0)`. The designer must choose the rule matching the work. Changing the tags is an action on the represented situation; renaming a letter in the notation while preserving its reference is a different change.

## NOT.2:6 - Bias-Annotation {#bias-annotation}

A designer can mistake their own intended grouping for a rule already available to the reader. Recover the expression from its declared conventions before relying on the intended result. The sum example separates those two readings with different outputs.

Familiar programming conventions can also be imported into another notation without justification. State the resolution policy that fits the represented work. An arrow, enclosure or repeated name acquires its binding and composition role through that policy.

## NOT.2:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| Supplying a constructor list without binding rules | State which constructors introduce names and where those names apply. The sum's index declaration governs its body. |
| Treating a repeated spelling as the same reference | Resolve the occurrence through its context. Local `p` can hide the external parameter in the sum example. |
| Checking input types but ignoring operand roles | Identify ordered or named places. The ratio receives numbers in either arrangement but computes different answers. |
| Letting layout imply an undocumented operation | Define which spatial or temporal relations carry grouping and connection; preserve those relations when changing presentation. |
| Dropping delimiters without recoverability or equivalence | Retain them until the precedence rule or an appropriate equivalence justifies their omission. |

## NOT.2:10 - Architectural Rationale {#architectural-rationale}

Formation, binding and composition answer connected questions. Formation identifies how an expression is built. Binding determines how its references obtain their values or participants. Composition determines how component boundaries are joined. A grammar that answers only the first question can leave the other two undecided.

This method develops the missing rules. NOT.1 selects what the work needs them to support; NOT.3 gives the interpretation and reading operations. A.6.3.RT.OE supplies construction under an available scheme. MATH.17/.18 can describe the operations and their interpretations mathematically, while CMP.12 constructs an effective interpreter or translation when required. The general notation-design result remains usable without first constructing all of those formal accounts.

Different graphical presentations or local names can express the same construction under the chosen rules. Treating them as equivalent requires the corresponding argument; it cannot be inferred from visual similarity. Conversely, giving two ports the same type cannot identify their roles. Keeping those questions explicit allows the notation to help reasoning about the construction itself.

## NOT.2:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Gheri and Popescu, [A Formalized General Theory of Syntax with Bindings](https://www.andreipopescu.uk/papers/bindings.pdf), §2 | Constructors alone leave binding positions undecided. Sections :4.1/.3 add the required binding rules; :5.1 works the sum and capture contrast. The source's alpha-equivalence, freshness and substitution theory supports formal development when needed. Its full mechanization adds no necessary step to the local notation example. |
| Piedeleu and Zanasi, [An Introduction to String Diagrams for Computer Scientists](https://arxiv.org/abs/2305.08768), §2 | Sections :4.2/.4 use typed, ordered interfaces and drawing equivalence under stated equations; :5.2 shows why equal input types alone lose a needed role distinction. Symmetric monoidal categories supply one mathematical class of schemes, not every notation's composition law. |
| Wehmeier, [Binding in classical and dynamic predicate logic](https://link.springer.com/article/10.1007/s10849-026-09472-0), 2026, introduction and §2 | Shared surface syntax can have different semantic binding behaviour. Section :4.3 therefore selects a resolution policy that fits the interpretation instead of treating nearest lexical binding as universal. The paper's proposed general binding schema is not imported into every notation. |
| Dutilh Novaes, [Formal Languages in Logic](https://doi.org/10.1017/CBO9781139108010), 2012, pp. 53-54 and §5.2.1, historical foundation | Keep diagrammatic formation and work with external inscriptions among the available choices in :4.2/.6. This counters selecting textual syntax merely because it has explicit rules. The resulting convention still has to support the reader's operation; explicitness alone establishes no learning advantage. |
| Zwaan and van Antwerpen, [Scope Graphs: The Story so Far](https://drops.dagstuhl.de/entities/document/10.4230/OASIcs.EVCS.2023.32), 2023, §§1–2 and 5 | Scopes, references and declarations can be related by paths with visibility and precedence policies. This is a developed alternative when static name resolution crosses nonlexical boundaries. Its expressiveness and execution costs remain relevant; the method is not a universal account of physical references or component composition. |

**Choosing the rule design.** Retain familiar conventions when they already determine the needed grouping, reference and connection. A constructor list or an implicit layout is cheaper to state, but the sum and ratio cases show the price when it leaves two consequential readings. For that local difficulty, add the missing scope, delimiter or operand role and try the changed expression. This costs more signs or conventions to learn, while preserving a first use through a legend and worked construction.

When static references cross imports or other boundaries that simple nested environments do not handle conveniently, a scope-graph model can make the resolution policy explicit and reusable. It requires constructing those scopes, paths and priorities, and assessing the available implementation. Use that richer account when the reference problem calls for it, rather than adding it to the elementary sum. Likewise, choose a formal binding theory or diagram calculus when its laws are needed for repeated transformation or reasoning.

Revisit the retained choice when a needed expression cannot recover its references or composition, the interpreted operation changes, or a less costly available scheme preserves the same needed distinction. The synthesis is a way to construct and revise those rules; it does not select one notation or one binding policy for every practice.



## NOT.2:End {#end}

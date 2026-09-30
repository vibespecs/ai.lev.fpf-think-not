# NOT.4 - Construct Transformations of Expressions That Preserve Their Use: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.4:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.4:5.1 - Name a repeated construction without capturing another input {#name-a-repeated-construction-without-capturing-another-input}

A reader wants to see and change the repeated construction in `(x + 1) * (x + 1)`. The expression denotes ordinary integer arithmetic with a fixed input x. Introduce a local definition: `let v = x + 1 in v * v`. Here `let` gives v the value of its defining expression within the following body.

At x = 3 the original expression gives `4 * 4 = 16`; the new one first obtains v = 4 and then the same result. For any integer x, substitution of v's definition recovers the original expression, establishing the general equality under this interpretation. To change the repeated construction to x + 2, change the one definition. The new value at x = 3 is 25, and expansion shows both occurrences received that change.

Now use a larger expression `u + (x + 1) * (x + 1)` with external inputs u = 10 and x = 3. Introducing `let u = x + 1 in u + u * u` is wrong: it turns the external u into a local reference and produces 20 instead of 26. A fresh v gives `let v = x + 1 in u + v * v`, which produces 26. The repair changes the binding choice, not the arithmetic law.

The rule applies to the pure arithmetic interpretation supplied here. If each occurrence instead instructs a fresh observation, sharing their results changes the operation. For example, two sensor reads may return 4 and 5, whose product is 20; one read returning 4 reused twice gives 16. Retain two observations unless their consolidation is justified for the intended use.

### NOT.4:5.2 - Compress a sequence while preserving its order {#compress-a-sequence-while-preserving-its-order}

A notation describes ordered cues A and B. The sequence `A; B; A; B` is to be shortened without changing the order of cues. Define `repeat 2 { E }` to expand into two copies of the entire finite sequence E, preserving its order. Then:

```text
A; B; A; B  ->  repeat 2 { A; B }
```

Expansion returns A, B, A, B. The third cue remains A. A reader changing B in every repeated unit can now change it once in the repeated body. If only the final B must change to C, expand or separate that occurrence: `A; B; A; C`. The earlier abbreviation no longer expresses the intended two identical units.

The tempting form `repeat 2 { A }; repeat 2 { B }` expands to A, A, B, B. It preserves counts but changes the third cue to B. Counts are insufficient for the selected ordered reading. No rule for exchanging cues was supplied.

This notation states cue order. If intervals, accents or bodily actions distinguish the repetitions, retain those distinctions in E or choose a different abbreviation. The order-preservation result alone supplies no claim about those further observations.

### NOT.4:5.3 - Keep a cancellation inside the condition that permits it {#keep-a-cancellation-inside-the-condition-that-permits-it}

For real x, consider `if x != 0 then x/x else 0`. Only the selected branch is evaluated. Within the first branch, division is defined and the quotient is 1, so the expression can become `if x != 0 then 1 else 0`.

At x = 2 both expressions return 1; at x = 0 both return 0 without evaluating the quotient. More generally, the two branches cover all real inputs and give the same result in each. Replacing the whole expression by 1 would fail at zero. Replacing an unrelated occurrence of x/x outside that guarded branch would also need its own domain condition. The useful transformation follows the local assumption through its scope.

### NOT.4:5.4 - Reconnect an ordered pair after removing two swaps {#reconnect-an-ordered-pair-after-removing-two-swaps}

A diagram carries an ordered pair of integer values on two wires: port 1 carries a and port 2 carries b. A swap exchanges the two values. Its output is (b, a); a second swap restores (a, b). Replace the two swaps by straight connections preserving port numbers. This argument holds for every integer pair.

The enclosing operation subtracts port 2 from port 1. In compact diagram notation:

```text
(1:a, 2:b) -> swap -> swap -> subtract(1, 2)
(1:a, 2:b) -> straight     -> subtract(1, 2)
```

Both forms return a - b. The replacement makes the source of each subtraction input directly traceable. If the replacement's outgoing wires are accidentally crossed, the enclosing operation instead receives (b, a) and returns b - a. Inputs (5, 2) then give -3 instead of 3; inputs (2, 5) give 3 instead of -3. Retaining two ports without retaining their correspondence loses the required use.

The diagram describes pure value operations, and the enclosing operation consumes only the ordered pair. That interpretation justifies this replacement in its context. Physical wire length or signal delay would be additional observations requiring a different preservation argument.

## NOT.4:6 - Bias-Annotation {#bias-annotation}

A familiar algebraic identity can be applied under a different interpretation without notice. Integer or real arithmetic, finite machine arithmetic and effectful actions can admit different replacements. Recover the interpretation that the actual expression uses before transferring a rule.

The preference for a short final expression can hide the operation a learner or collaborator needs to recover. Retain an expandable or explanatory form when it enables that work. Conversely, keep a fluent compact form when repeated expansion only adds effort to an already understood operation.

## NOT.4:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| Choosing a fresh-looking spelling without checking its scope | Check the existing references. The u-to-v repair in :5.1 preserves the external input. |
| Sharing repeated signs that denote distinct actions | Retain the distinct executions or observations unless their consolidation preserves the needed behavior. |
| Keeping counts while changing order | Expand the sequence rule and inspect the ordered result; :5.2 separates these observations. |
| Promoting a branch-local equality to a global rule | Carry the assumption to each permitted use, as in guarded cancellation. |
| Treating one equality check as a rule for every context | Establish the context-sensitive argument, or keep the conclusion at the checked scope. |
| Applying transformations indefinitely because each is valid | Choose the needed form or use a bounded search with a stopping and selection rule. |

## NOT.4:10 - Architectural Rationale {#architectural-rationale}

Transformation rules are operations on expressions with an interpretation. Their useful content includes both the replacement and the conditions under which it preserves the relevant consequence. This is why a copied shape or a familiar equality alone is insufficient.

Mathematical construction and computational realization supply different contributions. MATH.17/.18 establishes laws for the transformed operations and interpretations; CMP.12 makes a translation or evaluator effective. The present method constructs a notation-level manipulation for an intended reading or edit. It can be used manually, in an editor or in an automated transformation without identifying those implementations with one another.

The retained observation determines the strength of the rule. Identifying expressions by the same value can discard a derivation, evaluation order or history that another use needs. Selecting that equivalence and respecting it in surrounding constructions makes the limitation explicit. A richer needed result calls for a richer interpretation or another retained form.

## NOT.4:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Piedeleu and Zanasi, [An Introduction to String Diagrams for Computer Scientists](https://arxiv.org/abs/2305.08768), §§2 and 6.1 | Adopt rewriting relative to declared structural laws and matching that respects the expression's boundaries. Their graphical rewriting constructions concern specified categorical structures; an arbitrary diagram does not inherit those equations. |
| Willsey and colleagues, [egg: Fast and Extensible Equality Saturation](https://arxiv.org/abs/2004.03082), POPL 2021, §§2.2, 4 and 5 | Use the distinction between committing to one rewrite and retaining equivalent forms for later selection. Conditional rules and binding analysis show why syntax matching alone can be insufficient. An e-graph relies on supplied valid equations; its compact storage does not establish those equations or guarantee affordable saturation. |
| Hou, Laddad and Hellerstein, [Towards Relational Contextual Equality Saturation](https://arxiv.org/abs/2507.11897), 2025 work in progress, §§1–3 | Retain the distinction between context-local and general equality in :4.3. The proposed contextual reasoning still has implementation and cost questions; it supplies no completed general engine here. The guarded-division case derives a permitted local replacement from its own stated arithmetic conditions. |
| Pal and colleagues, [Equality saturation theory exploration à la carte](https://arxiv.org/abs/2609.14527), 2026 extended preprint, §6.3.1 and §8 | Rule generation can combine guided search and LLM proposals with separate validity checks and derivability from prior rules. The study remains domain-specific; its discussion leaves conditional rule inference partly open. Do not infer a sound general rewrite system from plausible generated rules. |

**Choice of method.** Prefer a directed, justified manipulation when one known operation needs a better expression. An automated search that retains many forms becomes useful when early commitment repeatedly prevents later improvements and the expression theory admits such search. Equality saturation addresses that alternative without making every notation problem a compiler project. Its cost and supplied validity conditions still matter; the current [egglog scheduling tutorial](https://egraphs-good.github.io/egglog-tutorial/04-scheduling.html) shows why deriving a needed condition before expanding alternatives can avoid wasted work. Reopen the choice when the number of interacting rules or repeated uses makes the small direct route inadequate.

The source contributions are combined here with notation requirements and reader operations. The worked arithmetic, cue and guarded-division cases demonstrate distinct conditions of that synthesis, not universal gains from a particular notation or tool.


## NOT.4:End {#end}

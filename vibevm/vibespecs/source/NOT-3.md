# NOT.3 - Give Expressions an Operative Interpretation: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.3:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.3:5.1 - Turn a condition diagram into a reading procedure {#turn-a-condition-diagram-into-a-reading-procedure}

A team designs a notation for combinations of conditions. Labels `P`, `Q` and `R` refer to conditions with supplied truth values. An `ALL` enclosure holds only when every enclosed condition holds. An `ANY` enclosure holds when at least one enclosed condition holds. The conditions are stable while the expression is read, and reading them does not change their values.

Consider:

```text
ALL {
  P
  ANY { Q R }
}
```

The legend defines the operators, but a new reader still needs a way to apply them to a nested expression. Supply this reading procedure: resolve each condition label from the given inputs; evaluate the innermost enclosure; replace it by its Boolean result; continue outward.

With `P = true`, `Q = false` and `R = true`, the inner enclosure is true because R is true. The outer enclosure combines true with true, so the whole condition holds. This result concerns the supplied conditions. Establishing their truth in an actual project is separate work.

A second route examines only values that can still change the answer. For `ALL`, one false child settles the result as false; for `ANY`, one true child settles it as true. With the same inputs, the reader checks P, then Q and R, and obtains the same result. If P changes to false, the outer `ALL` is false without inspecting Q or R. The stable, side-effect-free condition premise makes this omitted reading legitimate.

Now change the inner operator from `ANY` to `ALL` while keeping the original inputs. The inner result becomes false and therefore the outer result becomes false. The reader has followed the changed expression through the same interpretation rules. Replacing a label without resolving its value would leave a different gap: the input is missing, not the nesting rule.

The two reading routes expose a choice about obtaining the answer. They agree on these Boolean results; one shows every intermediate value, while the other can avoid work. A user who also needs all intermediate values should retain the first route or extend the second to produce them.

With P false and the values of Q and R not supplied, the whole expression is still false. A request for every intermediate value still needs those missing inputs.

### NOT.3:5.2 - Recover what an interval notation means before using it {#recover-what-an-interval-notation-means-before-using-it}

A signal plan contains the pair `(2, 4)`. The notation designer must say whether the second component is an ending time or a duration. Under the first interpretation, the planned active interval is `[2, 4)`; under the second it is `[2, 6)`. Half-open intervals include their start and exclude their end.

Choose `(start, duration)`. Give the reader two operations: add duration to start to obtain the end, then test whether a queried time is at least the start and less than the end. At time 5 the planned signal is active, because `2 <= 5 < 6`. If duration changes from 4 to 2, the new end is 4, and the signal is inactive at time 5.

The pair's two numeric entries did not establish this interpretation by themselves. The chosen convention and the comparison procedure make the answer obtainable. A timeline can support another reading by locating the queried point against a drawn interval, provided its scale and endpoints carry the same values.

This answers a question about the plan. To determine whether a device actually emitted the signal at time 5, obtain the relevant observation and the conditions relating it to emission. The notation can retain that observation or a model of the device, but the planned interval alone supplies neither.

## NOT.3:6 - Bias-Annotation {#bias-annotation}

Expert familiarity can conceal a reading step. A fluent reader may move from a symbol to a consequence without noticing the convention or skill used. Recover that step when it changes what another reader needs to know or be able to do.

The opposite bias treats every interpretation as a complete algorithm awaiting transcription into code. A mathematical meaning can leave an obtaining problem unsolved, and a practiced perceptual operation can lack a suitable machine realization. Keep these different contributions visible when allocating work among agents.

## NOT.3:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| A legend names signs but leaves composition unused | Read a compound expression through to its result. The condition example needs a rule for proceeding through nested enclosures. |
| Treating a denotation as an available computation | Identify the operation that obtains the denoted answer and its conditions, or return the missing algorithmic problem. |
| Hiding a learned reading skill | Explain the operation or name the preparation needed to perform it. Test access and capability where uncertainty changes the next move. |
| Reusing a shortened reading after its premise changes | Recheck which observations it preserves. Short-circuit reading in the first case presupposes stable conditions without reading effects. |
| Reading a plan as a report of events | Obtain the observations needed for the event claim; the signal schedule alone states what is planned. |

## NOT.3:10 - Architectural Rationale {#architectural-rationale}

The interpretation connects representation with work. It identifies the meaning relevant to a question and the operations through which a reader can obtain a consequence. Neither a symbol inventory nor a description of intended meaning alone guarantees that those operations are available.

The separation between interpretation and obtaining preserves generality. MATH.18 can establish a mathematical interpretation. CMP.12 can construct an effective evaluator under its algorithmic conditions. NOT.3 asks what reading the notation is to support and supplies the missing connection for its intended user. It can therefore include a manual or embodied route without assuming that every semantic assignment is computable.

Several useful readings may expose the same structure differently. Choosing among them can change the work needed to recover an answer or the intermediate structure made available. This is one reason to design notations around operations, rather than treating them only as shorter ways to write conclusions.

## NOT.3:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Macbeth, [Seeing How It Goes: Paper-and-Pencil Reasoning in Mathematical Practice](https://doi.org/10.1093/philmat/nkr006), 2011, opening discussion and treatment of Peirce's alpha graphs, historical foundation | Adopt the distinction between recording an answer and working through signs to obtain or expose reasoning. Her different readings of a graph motivate retaining useful reading routes. Their mathematical case does not establish equal accessibility to every reader. |
| Dutilh Novaes, [Formal Languages in Logic](https://doi.org/10.1017/CBO9781139108010), 2012, §5.2, historical foundation | Adapt attention to the operations people perform with external inscriptions and the preparation those operations require. Treat the cited human studies at their studied scope; no general learning gain or cross-agent equivalence follows here. |
| Piedeleu and Zanasi, [An Introduction to String Diagrams for Computer Scientists](https://arxiv.org/abs/2305.08768), mathematical syntax/semantics account | Use compositional interpretation when the notation and target operations admit it: the whole interpretation follows the specified combination of parts. This offers a formal alternative to a merely demonstrated reading. The required obtaining procedure and the reader's access still depend on the intended use. |

**Choice between approaches.** If a known formal interpretation and an available evaluator already answer the question, use them; a new reading procedure adds no value. When the difficulty is obtaining the consequence from a new notation, the present method supplies that route and locates its tacit requirements. A trained reading can be useful before a full formal calculus exists; a broader preservation or automation claim can justify constructing that calculus through the mathematical and computational suppliers.


## NOT.3:End {#end}

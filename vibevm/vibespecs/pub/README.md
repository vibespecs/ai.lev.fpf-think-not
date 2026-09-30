# Notational Engineering - Readme {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Readme section of the publication. See LICENSE.md for the list of changes.

A notation should let its users do something with an expression: derive a consequence, follow a dependency, change an assumption or instruct another performer. The methods in this language connect that work to the expression's structure and interpretation, then help carry the result between forms and through changes. They apply to symbolic, graphical, verbal, gestural and executable expressions. The subject practice supplies what the expressed distinctions mean and which consequences matter.

Bring an expression, the operation it should support and enough subject knowledge to recognize a useful result, or a collaborator who can supply that knowledge. Keep conventions that already work. Constructing an expression under adequate existing rules can start with FPF A.6.3.RT.OE; use this language when those rules, their interpretation or the supported operations need development.

You can ask an assisting agent: “Explain this and give me your comments in the language of my work, without framework jargon.” Ask it to demonstrate the reading or change and identify any rule, input or capability it had to supply.

## Practical entries {#practical-entries}

These selected connections show how results pass between methods. They are examples, not a catalogue or a prescribed sequence. Enter where the difficulty occurs and stop when the needed result is available. The Table of Contents and each pattern's `Use this when` provide direct access for other questions. The [Preface](spec://ai.lev/fpf-think-not/pub/PREFACE#root) explains the repertoire and develops the first connection in greater detail.

### NT-CHANGE-TOGETHER - Carry a changed request through several representations {#nt-change-together-carry-a-changed-request-through-several}

- **Situation:** A group uses a formula, operation graph and table for different operations, and a local request changes what their users should read or do.
- **Question:** What does the request change, and how can the useful forms remain connected?
- **First useful result or blocker:** The request expressed as a constraint on the shared construction, followed by its affected expressions or a conflict between requirements.
- **Start with:** [NOT.6 - Coordinate Complementary Representations through Shared References](spec://ai.lev/fpf-think-not/contract/NOT-6#root) when the forms are already interpreted; [NOT.1 - Choose the Distinctions and Operations a Notation Must Support](spec://ai.lev/fpf-think-not/contract/NOT-1#root) when the required operation is still unclear.
- **Stop or return:** Keep unaffected interpretations. Return to the changed assumption, discarded distinction or incompatible requirement; an adequate existing representation needs no redesign.

#### Worked connection for NT-CHANGE-TOGETHER {#worked-connection-for-nt-change-together}

1. **Give the forms something definite to express.** A stipulated rule is `r(q,b) = q + q + b` over real numbers. Both q occurrences use one supplied input; b is one shared parameter. The work is to obtain outputs and revise b. If grouping or references are unclear, [NOT.2 - Define Expression Rules for Recoverable Binding and Composition](spec://ai.lev/fpf-think-not/contract/NOT-2#root) supplies those rules. Its result lets [NOT.3 - Give Expressions an Operative Interpretation](spec://ai.lev/fpf-think-not/contract/NOT-3#root) specify the reading: add q to itself, then add b. In the operation graph, q feeds both inputs of the first addition; that result and b feed the second. At b=1 and q=0, 1, 2, the outputs are 1, 3, 5.

2. **Use the interpretation to justify a useful change of expression.** [NOT.4 - Construct Transformations of Expressions That Preserve Their Use](spec://ai.lev/fpf-think-not/contract/NOT-4#root) can replace the formula by `2*q + b`. Real arithmetic establishes the same output for every admitted q and b. The graph exposes the dependence; the compact formula makes the shared parameter easy to locate. Their value comes from those operations, not from one form being universally simpler.

3. **Give a translation only the work it can support.** [NOT.5 - Translate between Notations while Tracking Lost Distinctions](spec://ai.lev/fpf-think-not/contract/NOT-5#root) produces the table `(0,1), (1,3), (2,5)` at b=1. This supports lookup at the listed inputs. The table alone does not determine the output at q=3: `2*q + 1` and `2*q + 1 + q*(q-1)*(q-2)` agree on all three rows but give 7 and 13 there. Keep the generating rule with the table when the receiver needs other inputs or a rule change. If only the three listed answers are required, stop with the table.

4. **Interpret the request before propagating it.** The group asks for r(1,b)=4 while retaining the coefficient 2. NOT.6 uses the correspondence between that table row and the formula to obtain `2*1 + b = 4`, hence b=2. This new parameter supplies the graph and regenerates the table as `(0,2), (1,4), (2,6)`. The unedited old cells were derived values, not instructions to hold them fixed. If the request also keeps r(0,b)=1, it requires b=1 and conflicts with b=2. Return the two requirements to the group for a decision. If a separate record says that an output of 3 was observed at q=1, keep that observation beside the new prediction of 4. A parameter change does not revise the past event.

5. **Reopen the relevant rule when an occurrence changes meaning.** Suppose each q occurrence now means a fresh sensor read. With successive readings 4 and 5 and b=1, `read() + read() + b` gives 10; `2*read() + b`, using the first reading, gives 9. Return to NOT.3 for the meaning of an occurrence and NOT.4 for the transformation's conditions. If one sample is intended, bind that sample once and reuse it. If two observations are intended, retain both. The measurement method supplies the meaning of a read; [CMP.12 - Construct an Interpreter or a Meaning-Preserving Translation](spec://ai.lev/fpf-think-cmp/contract/CMP-12#root) supplies an effective interpreter when software must execute the expression.

6. **Repair the remaining burden only if it matters.** If common parameter changes are still laborious, [NOT.7 - Redesign a Notation around the Reader's Difficult Operations](spec://ai.lev/fpf-think-not/contract/NOT-7#root) compares one accessible definition of b with repeated independent entries. The shared definition makes a common edit local but adds reference-following for individual readings. Keep the table for frequent lookup if that benefit warrants its maintenance. A later local exception returns to the sharing assumption: it cannot be expressed by a global parameter change alone.

The result can be the new expressions, a sufficient table, an exposed conflict or a missing interpretation. Applying the rule to a physical quantity requires the corresponding subject account; the arithmetic construction supplies no observation of that subject.

### NT-CARRY-A-SEQUENCE - Keep a sequence usable when its reader or reference frame changes {#nt-carry-a-sequence-keep-a-sequence-usable-when-its-reader-or}

- **Situation:** A spoken or gestured instruction must also support later inspection, comparison or execution by another reader.
- **Question:** Which references and intermediate results must survive the change of carrier or reader?
- **First useful result or blocker:** A recoverable ordered account with its reference frame and interpretation, or the missing information or performer capability.
- **Start with:** [NOT.8 - Construct Temporal or Embodied Notation with a Reading Procedure](spec://ai.lev/fpf-think-not/contract/NOT-8#root) for the reference and reading route; use NOT.5 when an interpreted sequence is available but the proposed translation loses what its receiver needs.
- **Stop or return:** Stop at the required reading. A changed frame returns to the interpretation; a request for enactment requires the performer's method and the observation needed to establish its result.

#### Worked connection for NT-CARRY-A-SEQUENCE {#worked-connection-for-nt-carry-a-sequence}

1. **Retain the references needed after a sign has passed.** A plan describes successive completed displacements on a grid. East is positive x, north positive y; the starting position is (0,0) and the performer faces north. `R` means one unit to the performer's right without turning; `F(2)` means two units forward without turning. The spoken score is `R; F(2)`, where the semicolon means complete the first displacement before starting the second. To inspect it later, use NOT.8 to construct a persistent companion with the same ordered signs, starting pose and frame convention. NOT.6 connects each spoken occurrence to its position in that score. Retain these references rather than only a list of recognized words.

2. **Carry the interpreted state to the next operation.** Use NOT.3's reading procedure: recover the facing direction, convert each displacement to grid coordinates, update the position, then read the next sign. Here R gives (1,0); F(2) then gives (1,2). No turn occurs. The intermediate position lets a receiving reader ask where the first displacement ends. The score leaves duration and the continuous path within each displacement open. Speaking it more slowly changes the delivery time, but supplies no new movement duration or distance.

3. **Test the translation against its receiving question.** An endpoint-only description gives (1,2). It is sufficient for the final-position question under this starting pose. It loses the order needed to recover the intermediate position: `F(2); R` has the same endpoint but passes through (0,2) rather than (1,0). NOT.5 therefore retains the ordered displacements when the receiver needs that distinction. A richer display of the endpoint alone cannot restore it. If a proposed abbreviation changes order while preserving only the number of signs, NOT.4 must return to the observation that the transformation was meant to preserve.

4. **Propagate a frame change, or change the score for a different intention.** Now the performer starts facing east, with the same body-relative signs and no turns. R moves south to (0,-1); F(2) moves east to (2,-1). NOT.6 updates the derived grid account from this changed premise. If the actual request is to retain the old grid displacements instead, define grid-relative signs `E(1)` and `N(2)` as one unit east and two units north, each without turning, and write `E(1); N(2)`. This restores the specified waypoints (1,0) and (1,2). Construct these new sign rules through NOT.2 and use NOT.3 to recover their different reading. The continuous path cannot be recovered from the old score alone, because it was never specified.

5. **Pass the right result to a performer.** A program receiving the ordered account still needs CMP.12's input representation and effective interpretation. Physical enactment additionally needs an applicable motion method, physical meaning for a grid unit, timing choices and control. A prepared person may already possess the required movement method. FPF B.5.MPC connects the mathematical, physical and computational contributions when the work needs all three; interpreted observation is needed to establish what movement occurred. The decoded endpoint is already a useful answer to the reading question.

This connection applies whenever changing medium or reader can remove references needed for later operations. A rhythm, laboratory signal or interaction trace needs its own relevant time references and subject rules. The movement case shows how the methods work together; it does not supply those other interpretations.

## Continue with the contribution the work needs {#continue-with-the-contribution-the-work-needs}

A notation can support thinking by keeping an assumption, dependency or alternative available for another operation. It can support methodology by making the descriptions of a working method usable together. When those descriptions serve different users, [ME.9 - Relate Method Representations across Their Different Uses](spec://ai.lev/fpf-eng-me/contract/ME-9#root) selects and relates the claims those uses need; NOT.6 constructs their notational correspondence.

A missing inference belongs to the mathematical, physical, computational or other subject method that supplies it. A reader who lacks an available operation may need explanation or capability development. Change the notation when its form, references or interpretation cause the difficulty; obtain the other contribution when that is what prevents the next result.

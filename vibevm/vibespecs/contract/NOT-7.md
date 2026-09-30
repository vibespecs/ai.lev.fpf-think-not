# NOT.7 - Redesign a Notation around the Reader's Difficult Operations {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.7:1 - Problem frame {#problem-frame}

**Use this when** a notation can express the required content, yet reading or changing that content is unnecessarily difficult. A reader repeatedly loses a dependency, has to reconstruct a grouping, or must change the same assumption in several places. Another symbol or a shorter inscription may leave the difficult operation unchanged.

Begin with one such operation on an actual expression. Find what the reader has to locate, infer, remember or alter. Change the notation or its editing arrangement at that point, then compare the operation and another operation that the change could burden.

The result is a repaired notation with a reason to prefer it for the intended work, or a decision to retain the existing form. A useful diagnosis may instead identify missing subject knowledge, an unavailable operation or inaccessible content that a notation change cannot supply.

The reader needs the subject criterion for a correct result and enough knowledge of the existing notation to inspect its interpretation. NOT.1 supplies a missing use requirement; NOT.2–.3 supply formation and interpretation. A sketch and a worked comparison can be enough for a local repair.

Keep a sufficient familiar form when no consequential reading or change difficulty is present. If the underlying account is wrong, repair that account. Use EXD.1–.3 when the needed work is to construct an explanation; use the instructional method appropriate to the missing capability when the reader cannot yet perform the required subject operation.

## NOT.7:2 - Problem {#problem}

How can a notation be made easier to use without removing the distinctions, dependencies or operations on which its usefulness depends?

Shortness, visual neatness and familiarity can each help particular work, but none identifies the difficult operation. A repeated value may be easy to read and costly to change. A shared name may make the change local while sending readers elsewhere to recover the value. A new arrangement must be judged through those operations.

The repair also has to separate expression from assistance. An author can explain the missing connection during a trial, making an unchanged notation appear successful. A trained reader can reconstruct a relation that the expression never supplies. Those contributions may be useful, but they change what the notation itself has achieved.

## NOT.7:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Ease of one operation and another | Making a dependency explicit can consume space; sharing a definition can add a lookup. |
| Familiarity and better construction | A new convention can reduce later work while imposing an initial learning cost. |
| Local repair and general reuse | One expression can be fixed cheaply; a rule used across many expressions needs broader comparison. |
| Simplification and preserved meaning | Removing detail helps only when the needed distinctions remain obtainable. |
| Observation and intervention | Assistance or practice can improve a trial independently of the changed notation. |

## NOT.7:4 - Solution {#solution}

**Locate the difficult operation → explain its burden → construct a targeted alternative → preserve the required meaning → compare use and displaced effort → retain or revise.**

### NOT.7:4.1 - Locate the operation and its failure {#locate-the-operation-and-its-failure}

Select a concrete question and the expression on which the reader must work. Ask for the answer or modification, not only an opinion of the notation. Recover the route taken: where the reader searches, which reference is followed, what has to be held in memory and where the result goes wrong or the work becomes costly.

Use an available response or observed difficulty when one exists. Otherwise, walk through the operation and treat the diagnosis as a design estimate. An actual trial is useful when plausible reader responses would change the repair decision; it is not a prerequisite for every obvious correction.

State the relevant preparation, permitted help, display or access conditions and effort limit. A reader who knows the local grouping convention faces a different question from one learning it. A page that hides half a diagram can create a different difficulty from the diagram's structure.

Keep the intended result in view. If the reader has correctly recovered the notation but lacks the subject inference, obtain that inference or capability. If an interpretation is ambiguous, NOT.2 or NOT.3 repairs the rule before comparisons of ease can settle its use.

### NOT.7:4.2 - Explain which work the current form imposes {#explain-which-work-the-current-form-imposes}

Describe the burden through operations: repeated searching, uncertain grouping, reconstruction of an unstated dependency, simultaneous retention of distant values, or many edits for one intended change. Choose the description that explains the observed case.

Locate the source of the burden. The expression, the construction rule, the editing environment and the reader's preparation can make different contributions. An editor that cannot show two needed passages together may be changed without introducing a new notation. A missing dependency needs expression even when the display is large enough.

Use Cognitive Dimensions as a vocabulary for such trade-offs when it helps the design conversation. Its activity-relative descriptions suggest where to look; a list of dimension names does not establish that a reader can perform the operation.

Retain successful uses of the current form. They identify what the repair must preserve and may reveal why an apparently awkward convention exists.

### NOT.7:4.3 - Construct a change at the source of the burden {#construct-a-change-at-the-source-of-the-burden}

Choose a change that alters the difficult operation. The following constructions supply starting points; their costs determine whether to keep them.

| Difficult operation | Possible construction | Other work to inspect |
| --- | --- | --- |
| Matching an item to its corresponding value or next step | Align the participating entries, give them shared references, or place the relation beside them. | Reading across another ordering, crowding and maintaining repeated entries. |
| Recovering the extent or operands of an expression | Make grouping or operand roles visible and keep their formation rule available. | Added space and the reader's ability to construct the grouped expression. |
| Changing one assumption repeated in many places | Introduce a named common definition and make its uses recoverable. | Following references and expressing a legitimate local exception. |
| Reconstructing a long nested operation | Expose useful intermediate results with their inputs and continuation. | Additional names and the possibility of losing the connection between stages. |
| Exploring a construction before every choice is known | Permit a clearly marked partial expression and show which operations it already supports. | Distinguishing an unresolved choice from a completed value. |

A local label, grouping mark or rearrangement can suffice. Use NOT.4 when an expression transformation needs a preservation argument, NOT.5 when the alternative omits distinctions, and NOT.6 when both forms will remain in joint use.

Keep the alternative small enough to inspect. If construction reveals that the original question was wrong or incomplete, revise the requirement through NOT.1. Do not keep optimizing the old operation merely to preserve the initial design brief.

### NOT.7:4.4 - Preserve what the work needs from the expression {#preserve-what-the-work-needs-from-the-expression}

Identify the meaning and operations that must survive the change. Work through one consequential contrast: reversed dependency, local exception, changed grouping or unresolved input, as appropriate to this notation. The new form must make the required difference recoverable.

If the repair adds a claim that was absent before, treat it as a content addition. If it supplies a new procedure or teaches a missing convention, include that contribution in the comparison. A useful combined repair is allowed; attribute its effect to the actual combination.

Preserve the path from a compressed form to the detail needed for its use. A shared definition needs a resolvable reference; an intermediate name needs its construction; an omitted branch needs a rule showing when it can be omitted. Compression is useful when it reduces the relevant work, not merely the displayed size.

### NOT.7:4.5 - Compare the same operation and the burden it moves {#compare-the-same-operation-and-the-burden-it-moves}

Perform the selected operation with the old and new forms under comparable conditions. Compare correct and missing results first, then the effort relevant to the use: searches, unresolved references, edits, elapsed time or another suitably defined measure. C.2.8 distinguishes structure recovered from the effort of recovering it.

Also perform an operation plausibly made harder by the repair. A shared parameter may make a global change easy and a local exception harder. An outgoing-dependency index may improve downstream search while an incoming-dependency list remains better for finding prerequisites. Keep that trade-off visible in the choice.

For a human or agent trial, retain the first response before explanation or correction. If the same reader sees both forms, practice can contribute to the second result. For a local decision, that limitation may be acceptable. A general superiority or learning claim requires a comparison that supports that stronger conclusion; EXD.6 and, for instructional use, HCD.19 supply the corresponding evaluation methods.

A family of alternatives can justify matched examples and computed measures. Use those measures to locate an expression or change that needs inspection. Shorter code, fewer symbols or a smaller edit count does not alone establish better understanding. Do not build a comparison gallery when one bounded contrast can settle the local repair.

### NOT.7:4.6 - Choose the repair at the needed scale {#choose-the-repair-at-the-needed-scale}

Retain the change when its demonstrated or reasonably expected contribution is worth the new burden for the actual work. Keep the incumbent when it remains sufficient. If different forms serve different important operations, preserve the useful alternatives and their correspondence rather than force one universal winner.

Use the existing contribution and choice methods in C.11.CRC/C.11 when cost or competing improvements affect the decision. When the work needs maintained comparison and selection rules, use A.19.CPM for comparison and A.19.SelectorMechanism for selection. This method supplies notation changes and their use differences, not a separate scoring system.

Leave the needed convention, reference or operation available with the retained expression. A repair that works only while its author explains it has not supplied a self-sufficient notation for that reading condition.

Stop when the present use is adequately supported and further comparison would not change the choice. Reopen when the operation, preparation, access, scale of use or meaning changes, or an actual response contradicts the claimed benefit.

## NOT.7:7 - Conformance Checklist {#conformance-checklist}

When the repair needs checking, ask the questions that can change its adoption.

- Is a concrete difficult operation identified, with its intended result?
- Does the repair change the cause of that difficulty?
- Can the needed distinctions and references still be recovered?
- Are content, notation, preparation, help and access changes distinguished where they affect attribution?
- Has an operation plausibly burdened by the repair been considered?
- Does the comparison support the claimed scope of benefit?
- Can the work stop with a sufficient local repair or a justified choice to retain the current form?

## NOT.7:9 - Consequences {#consequences}

A repair can make a needed relation or operation available with less reconstruction, or make an intended change less error-prone. It also makes the reason for keeping a familiar convention explicit when a proposed alternative would burden important work.

New conventions require learning and migration. Complementary views add maintenance. A local improvement remains local until broader use supports a wider claim. Some failures return to subject knowledge or explanation rather than notation.

## NOT.7:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| NOT.1 | Defines or revises the operation and distinction the notation must support. |
| NOT.2–.3 | Repair formation, binding and interpretation when those prevent a determinate operation. |
| NOT.4–.6 | Supply use-preserving transformation, loss-aware translation and continuing coordination of forms. |
| C.2.8 | Compares the selected structure recoverable by the intended reader under stated conditions. |
| C.11.CRC / C.11 | Relate the proposed gain to its burden and the current improvement choice. |
| A.19.CPM / A.19.SelectorMechanism | Supply comparison and selection of alternatives when those maintained rules are needed. |
| EXD.6 / HCD.19 | Evaluate explanation repairs and instructional material for their respective receiving uses. |
| NOT.8 | Constructs temporal and embodied reading operations whose difficulties may motivate this repair. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-1#root–.6 for requirements and operative rules; spec://ai.lev/fpf-spec/contract/C-2-8#root, EXD and HCD for recovery, explanation and capability questions. @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-7

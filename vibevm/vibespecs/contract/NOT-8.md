# NOT.8 - Construct Temporal or Embodied Notation with a Reading Procedure {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.8:1 - Problem frame {#problem-frame}

**Use this when** a notation carries important distinctions through timing, sound, gesture or bodily position, and recognizing its individual signs does not yet let a reader follow or perform the intended sequence. The reader may lose the cycle, confuse a gesture's reference frame, or recognize a command without knowing how to enact it.

Start with the distinction the work needs: an onset within a beat, two simultaneous events, a body-relative direction or another stated relation. Choose how the carrier expresses it, provide its reference and segmentation, then construct the procedure by which a reader recovers and uses it.

The result is a temporal or embodied expression with a usable interpretation and reading procedure. It states what a prepared reader can obtain, what remains for performance or control, and how a consequential change affects the reading.

This is notational engineering. Rhythm, movement, laboratory signals and interaction traces supply different subjects; their subject methods determine which timing or motion relations matter. The notation designer needs that subject meaning and the relevant capabilities of the intended reader. NOT.1–.3 supply the general design, formation and interpretation methods.

Reuse a familiar adequate convention when it already supports the operation. An ordinary static expression may suffice when no temporal or embodied distinction matters. Knowing the notation is not by itself a claim that a person can perform a movement or a machine can realize it; obtain the missing performance or control method when the work requires enactment.

## NOT.8:2 - Problem {#problem}

How can a reader recover and manipulate relations that unfold in time or action, including those no longer immediately present when the next sign arrives?

A sequence of recognized sounds can lack a known starting point or grouping. A pause can mean a specified rest, an unobserved interval or a wait for an event. A gesture to the right can refer to the performer's body, a room or a drawing. These interpretations permit different continuations.

The carrier's behavior also matters. Playing a recording faster changes its audible duration, but need not change the duration represented by a coded timestamp. A score can specify a desired action while leaving its bodily or algorithmic realization to the performer. The reading procedure must make the relevant convention available.

## NOT.8:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Transient expression and continued use | A reader may need an earlier sign after it has ceased to be perceptible. |
| Relative and absolute reference | A beat, body direction and clock time support different comparisons. |
| Recognizable sign and interpretable relation | A clear tone or gesture can still have uncertain scope, participant or timing. |
| Compact direction and adequate preparation | A short score can rely on skills or an interpreter that must actually be available. |
| Replay and live enactment | Pausing or slowing can aid analysis while changing the physical process or coordination. |

## NOT.8:4 - Solution {#solution}

**Select the temporal or embodied distinction → establish references → segment and encode → construct the reading or enactment route → vary a consequential condition → retain a usable expression.**

### NOT.8:4.1 - Select what is expressed and what the reader should do {#select-what-is-expressed-and-what-the-reader-should-do}

Identify the subject relation and the needed operation. The work may be to recognize an order, reproduce a rhythm, compare two movements, locate a missing event or construct instructions for another performer. Choose the distinctions that operation consumes.

Say whether the expression describes an observed occurrence, proposes a future performance or presents a construction for analysis. The same cue sequence can serve these different uses, but a plan does not establish that its events happened.

Separate the sign's physical properties from the represented properties. A sustained tone might represent duration by its length, or merely identify an event kind. A hand position might be an action being performed, a sign for another movement, or a reference against which a different action is timed. Use the convention that supports the selected work.

State the reader's available perception and operations. Distinguishing two timbres, maintaining a pulse, recognizing a body part and following a formal event code are different prerequisites. A computational reader needs a suitable input representation and interpretation, not an assumed human sensory skill.

### NOT.8:4.2 - Establish the references that locate an occurrence {#establish-the-references-that-locate-an-occurrence}

Give the origin, unit, frame or recurring reference needed to interpret the signs. For cyclic time, identify the cycle and position within it when occurrences across cycles must be distinguished. For movement, identify the participant, body part, spatial frame and starting condition that affect the interpretation.

Choose whether timing is absolute, relative to another event or relative to a maintained pulse. If a tempo change should retain relative positions, preserve that relation when changing elapsed durations. If a deadline is in seconds, a mere proportional rescaling may change the required result.

Give different participants a way to align their references when joint action or comparison needs it. A shared visible pulse, a named event or a common clock can supply alignment under its own conditions. Separately timestamped records do not establish event order unless their clock relation supports that inference.

Keep the reference identifiable during use. A repeated syllable can denote the same position in successive beats while being a different occurrence each time. A rightward direction can change in room coordinates when its body frame turns.

### NOT.8:4.3 - Segment and encode the needed relations {#segment-and-encode-the-needed-relations}

Choose recognizable units and a rule for joining them: separate events, intervals, phases, gestures or other parts appropriate to the subject. Mark a beginning, boundary or return to a cycle where losing it would change the reading.

Assign signs and their temporal or spatial arrangement to the selected distinctions. Make order, overlap and duration recoverable when the work needs them. Writing two signs successively does not express simultaneity unless a grouping or interpretation rule supplies it.

Provide a way to distinguish a specified absence from a missing observation. A rest within a known beat and a recording gap can both be silent, but only the former supplies the intended absence. Use a marker, an accompanying record or another recoverable convention where the difference affects the next operation.

Inspect discriminability under the intended conditions: speed, overlap, background sound, viewing direction or available sensors. A symbol family that is distinct on a page can become confusable when sounded or gestured. Change the encoding or access arrangement if the needed contrast disappears.

Choose detail for the receiving use. A movement score can constrain endpoints while leaving the route open; a different use can require the route, timing or body-part coordination. Keep an omitted choice with the performer or construction method that is to supply it, rather than silently giving the notation credit for it.

### NOT.8:4.4 - Construct the reader's route through the expression {#construct-the-reader-s-route-through-the-expression}

State how the reader establishes the reference, identifies the current part, combines it with retained information and obtains the next result. Make the necessary repetition, count, comparison, transformation or enactment available. A legend naming sounds or gestures may need this additional procedure.

For a transient carrier, choose how earlier parts remain usable: replay, a persistent companion record, a repeated reference, trained retention or another available means. Use only what the receiving conditions permit. NOT.6 connects a score, sound and event table when several forms remain necessary.

If the task is performance, connect the decoded instruction to the performer's available method. A person may already know how to realize a gesture or syllable. A machine may need a parser, state representation, control algorithm and physical realization. CMP.12 constructs an effective interpreter; B.5.MPC connects the abstract construction to preparation, execution and interpreted observation. Notation alone does not supply those methods.

A demonstration can be part of the supplied interpretation. Identify what it teaches and keep it available if the text relies on it. If another prepared reader can use the expression without that demonstration, the reading condition is different; assess the contribution at the condition actually offered.

### NOT.8:4.5 - Challenge the relation with a meaningful change {#challenge-the-relation-with-a-meaningful-change}

Carry out or inspect a small use and a contrast that can change its result. Shift a cue while retaining its identity, change a body's orientation, remove a timing reference or ask for simultaneity rather than order. Choose a contrast grounded in the intended operation.

Distinguish reading from successful physical performance. A correctly decoded sequence can still be infeasible for a particular body or controller. Locate that missing realization contribution rather than changing the meaning until the observed performance appears correct.

When using replay, decide which property it can preserve. Slowing a recording can aid segmentation. It cannot by itself demonstrate that a performer meets the original speed, that two live processes stay synchronized or that a paused physical system stops evolving.

A worked interpretation supports its stated use. Claims about human fluency, learning or transfer require their own basis; C.2.8 and the applicable capability-development method characterize the relevant recovery or performance. Use the current sufficient result, and seek an additional trial only when its outcome can change the next choice.

### NOT.8:4.6 - Retain the expression with its operative convention {#retain-the-expression-with-its-operative-convention}

Keep the reference, segmentation, interpretation and needed reading procedure available with the expression. A short local convention may suffice; reusable performance material may also need a demonstration, an interpreter or an accessible alternative carrier.

State an unresolved performer choice or lost distinction where the next use needs it. A score specifying endpoints can be useful before a motion path is chosen. A recording with an unobserved interval can support the observed segments without settling the missing order.

Stop when the selected operation is supported or the missing contribution is located. Use NOT.7 if the interpretation is determinate but difficult to follow. Reopen the affected convention when the reference frame, timing, medium, required observation or reader capability changes.

## NOT.8:7 - Conformance Checklist {#conformance-checklist}

When the expression needs checking, ask the questions that can change its use.

- Is the represented relation and intended reading or performance operation recoverable?
- Are the needed origin, unit, cycle, participant and frame available?
- Can the reader segment occurrences and distinguish the relevant order, overlap or duration?
- Is a specified absence distinguishable from missing information where it matters?
- Does the reading procedure identify the retained state or replay that it needs?
- Are perception, interpretation and physical performance contributions supplied at their stated scopes?
- Does a meaningful change preserve the intended relation or reveal the required repair?

## NOT.8:9 - Consequences {#consequences}

Temporal and embodied expression can become a manipulable part of reasoning: readers can locate occurrences, vary a relation, compare performances or hand an interpretable instruction to another agent. A score can retain useful constraints while allowing more than one realization.

The method exposes preparation and access costs that a fluent practitioner might leave tacit. Additional references can burden performance; a persistent companion representation can help analysis while requiring coordination. Some expressions remain useful only with a trained performer or an available interpreter.

## NOT.8:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| NOT.1–.3 | Supply distinction selection, expression formation and operative interpretation. |
| A.6.3.RT.OE | Constructs an expression around the operation it should make possible. |
| NOT.4–.5 | Preserve selected temporal or embodied uses during transformation and expose translation losses. |
| NOT.6 | Coordinates transient expression with a score, event record or other complementary form. |
| NOT.7 | Repairs difficult reading or manipulation after the interpretation is established. |
| CMP.12 | Constructs the effective interpreter or translation when a computational reader is needed. |
| B.5.MPC | Connects abstract relations and computation to preparation, physical execution and interpreted observation. |
| C.2.8 | Characterizes structure recovered under the intended reader's preparation, access and available operations. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-1#root–.7 for design and interpretation; spec://ai.lev/fpf-think-cmp/contract/CMP-12#root for an effective interpreter; spec://ai.lev/fpf-spec/contract/B-5-MPC#root for physical realization. @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-8

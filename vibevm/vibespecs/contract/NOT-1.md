# NOT.1 - Choose the Distinctions and Operations a Notation Must Support {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.1:1 - Problem frame {#problem-frame}

**Use this when** you are choosing or designing a notation and cannot yet say what its users must be able to express, recognize or do with an expression. A candidate may name all the right objects while hiding their order, dependence or duration. Another may express the distinction but make a frequent change require rebuilding the whole description.

Start with a piece of work: composing operations, comparing two models, tracing a dependency or performing a sequence are examples. Identify an operation that a person or computational agent needs to carry out using the notation. Then find two cases that this operation must treat differently. Trying to express and use those cases gives the first design requirement that can be acted on.

The reader needs enough knowledge of the practice to explain why the cases differ and what a useful result would be. That knowledge can come from a collaborator. Choosing the notation does not require the designer to perform every specialist inference unaided; it does require access to the distinctions that those inferences use.

The result is a choice of distinctions and operations to support, together with a small expression or interaction that shows how a proposed notation could support them. It may instead be a reason to keep an existing notation, preserve an unresolved choice, or obtain a missing account of the work before adding symbols.

If a suitable notation already exists and only one expression needs repair, construct that expression under its rules using A.6.3.RT.OE. Return here when the rules themselves lack a needed distinction or make the required operation impractical.

## NOT.1:2 - Problem {#problem}

How can a notation designer determine what the notation needs to make possible before committing to its symbols and rules?

A list of concepts leaves the work underdetermined. The same concepts can enter different compositions, questions and changes. A notation sufficient for recognizing an object may be insufficient for constructing it; a description sufficient for one question may discard what another question needs. Designing from familiar examples alone can conceal these differences until somebody tries a new case.

## NOT.1:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Discrimination and economy | Showing more distinctions increases expression and reading work; omitting one can prevent the required conclusion. |
| Reading and changing | A compact finished description can be expensive to revise. |
| Shared conventions and reader preparation | Familiar conventions save explanation for one group while imposing learning or translation on another. |
| Expression and environment | A distinction may be carried by marks, layout, an interaction or available context. Changing the medium can remove that support. |
| Present work and discovery | Trying a notation can expose a useful operation absent from the initial requirements. |

## NOT.1:4 - Solution {#solution}

**Choose a working operation → find a consequential difference → locate what carries that difference → try a notation choice → compare the work it enables and displaces → retain or revise the requirement.**

### NOT.1:4.1 - Choose an operation and the conditions for performing it {#choose-an-operation-and-the-conditions-for-performing-it}

Describe what the user starts with, what they do and what they need to obtain. Prefer a question such as “after exchanging these two operations, what changes in the result?” to an aim such as “make the notation intuitive”. The former exposes what an expression must support.

Specify the preparation and access on which the operation relies. A mathematician may use established algebraic conventions; a performer may recognize a learned gesture; a program may receive only serialized text. An AI agent's access to a rendered page, a text extraction and an editor's internal structure are different conditions. Include the context that is actually available, rather than assuming that every reader receives the designer's view.

For a small task, one operation is enough to begin. If the notation will be used for a family of operations, choose cases that exercise materially different demands. For example, interpreting a completed expression and changing a shared component can need different support. Do not turn this selection into an inventory of every conceivable use.

### NOT.1:4.2 - Find cases whose difference changes the work {#find-cases-whose-difference-changes-the-work}

Construct or recover a pair of cases that require different answers, permitted changes or actions. Explain the difference in the practice before deciding how to write it. Two arrangements of the same components can have different outputs; two performances with the same starting times can have different sustained intervals.

Attempt to express both cases with the candidate notation and its allowed context. If they become indistinguishable while the required answers differ, something needed by that operation has been omitted. Recover it through an expression rule, an accessible annotation, a query to another representation or a narrower declared use. The choice depends on how the expression will be used.

Conversely, two visibly different cases may be interchangeable for the present operation. Keep their shared representation if that simplification preserves the needed result. The question determines which differences matter.

A deliberately unfinished choice can itself matter. If the work permits an unspecified order or duration, retain a way to leave it unspecified and a way to recognize when the next operation needs it settled. A convention that silently chooses a value would change the work being described.

### NOT.1:4.3 - Locate the information and operations behind the marks {#locate-the-information-and-operations-behind-the-marks}

Follow the user through the proposed operation. Which part of the expression identifies a participant, establishes a relation or permits a transformation? Which part is supplied by a convention, the surrounding account or an interaction with a tool?

This examination can reveal three different needs:

- The difference is known but cannot be expressed or recovered under the available rules. Design a way to carry it.
- The expression carries the difference, but obtaining or changing it is too costly. Change the arrangement or the supported operation; NOT.7 develops that redesign.
- The practice has not supplied the needed distinction or inference. Obtain that contribution from the relevant practitioner or method before prescribing how it must be expressed.

Test the whole expression and its usable context. A symbol may be ambiguous in isolation yet clear in a composition. A diagram may be clear to a prepared human reader while its plain-text export loses the grouping on which that reading depends. Preserve the effective context or revise the notation for the receiving conditions.

### NOT.1:4.4 - Try a design choice through use {#try-a-design-choice-through-use}

Propose a small change capable of supporting the selected operation. Examples include marking operand groups, adding a reference to a shared component, exposing event duration, or making an unresolved alternative visible. Construct the contrasting cases with that change and carry out the operation using the proposed reading rule.

Where modification matters, change an input, component or relation and follow the resulting edits. A notation that displays one finished example well may make the required family of changes error-prone or laborious. Include a contrasting case that challenges the same rule, rather than polishing the first example until it looks convincing.

Separate the notation's contribution from supplied subject knowledge. In a diagram for composing functions, arrows can expose the order of application; the functions and the ability to apply them supply the numerical result. If the result cannot be obtained because an algorithm or physical law is missing, return that question to the corresponding practice.

An expert walkthrough can establish an explicit loss or a useful candidate change. When it remains uncertain whether the intended reader can recover or perform the operation, use C.2.8 to choose a bounded reading probe with the intended preparation and access. Obtain further evidence only when its outcome could change the design or the permitted use.

### NOT.1:4.5 - Compare the work enabled and the work displaced {#compare-the-work-enabled-and-the-work-displaced}

Compare candidate notations on the selected operations under comparable conditions. Look for a practical trade-off: a shared definition may make one update cheap while requiring the reader to follow references; expanded expressions may be easy to read locally while repeating changes in several places.

Keep both alternatives when they serve different necessary operations and the correspondence between them can be maintained. NOT.6 develops that arrangement. For a choice among alternatives, compare only characteristics that affect the work and state the selection criterion. A simple contrast can settle the local choice: one notation loses an answer that the other preserves.

When the comparison must be reused across alternatives or design iterations, A.19.CPM governs comparison under a declared comparator; A.19.SelectorMechanism governs selecting a set from those results under stated criteria. A Pareto criterion can retain alternatives that are not dominated on the chosen characteristics. It does not by itself resolve a trade-off between reading and editing effort. Keep that trade-off visible until the work supplies a reason to choose, or retain both notations for their different uses. A vocabulary of design trade-offs can help notice a difficulty, but a vocabulary or weighted checklist cannot establish that a user can perform the operation.

Trying a candidate can reveal that the original question was incomplete. Revise the selected operations or cases when the newly visible distinction changes a useful next move. Then test the affected requirement again. This is a development of the problem and its proposed solution, for which C.40.CD supplies the common method.

### NOT.1:4.6 - Retain the decision at the scale needed for the next construction {#retain-the-decision-at-the-scale-needed-for-the-next}

State the operation to support, the distinction it needs, how a candidate carries it and the burden or unresolved choice that remains. A short explanation beside the candidate can suffice. Keep the contrasting cases when they will help construct, teach or revise the rule; no separate requirements document is necessary for an ordinary small use.

Stop when the next notation construction or choice is clear enough to undertake. Detailed expression formation, interpretation and transformation can then be developed where needed. Do not reopen every design choice merely because a new example is available; reopen the choice whose supported operation or conditions changed.

## NOT.1:7 - Conformance Checklist {#conformance-checklist}

Use these questions to examine the design decision when its adequacy matters. They do not require a separate written answer for each ordinary application.

- Can the intended user identify the working operation, its starting information and the result they need?
- Does a consequential difference between cases explain why the selected distinction is required? If a difference is omitted, is the resulting loss acceptable for that use?
- Is the necessary information available in the expression, its declared conventions or an accessible interaction?
- Has the proposed rule been used on the contrasting cases, including a change when modification is part of the work?
- Are the subject knowledge and reader preparation needed for that use recoverable?
- Does the next construction follow from the decision, with remaining uncertainty and displaced work visible where they matter?

## NOT.1:9 - Consequences {#consequences}

The next notation decision becomes a choice about work that can be attempted. A designer can explain why a distinction, convention or editing operation is needed and can recognize when a simpler notation suffices.

The method costs representative construction and use. It can reveal a gap in the subject account that notation design alone cannot settle. Its result is local to the selected operations and conditions; extending use can expose another requirement. Keeping the contrast behind a decision makes that extension easier to reason about.

## NOT.1:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| A.6.3.RT and A.6.3.RT.OE | Supply representation-scheme distinctions and the construction of an operative expression under available rules. A missing rule can become a notation-design question here. |
| C.2.8 | Characterizes recoverable structure for a prepared reader with stated access and effort; use it when extraction difficulty changes the notation choice. |
| C.40.CD | Develops a problem and candidate ways of dealing with it together when a notation trial changes the useful question. |
| C.11.DUA | Helps decide whether another comparison or reader probe can change the choice enough to justify its cost. |
| A.19.CPM and A.19.SelectorMechanism | Govern reusable comparison and set selection under declared conditions; preserve trade-offs instead of forcing one winner. |
| MATH.17/.18 and CMP.12 | Supply mathematical constructions and interpretations, or an effective interpreter and translation. They develop consequences and operations whose needed expression can be selected here. |
| NOT.2-.4 | Develop the chosen expression-formation, interpretation and transformation rules. |
| NOT.5/.6 | Develop translation and complementary representations when the needed operations call for more than one notation. |
| NOT.7/.8 | Develop redesign around difficult operations and notation whose distinctions unfold in time or embodied action. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-spec/contract/C-2-8#root for recovered structure; spec://ai.lev/fpf-spec/contract/A-6-3-RT-OE#root for an expression under available rules; spec://ai.lev/fpf-think-not/contract/NOT-2#root/.3/.7 for construction and repair. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-not/contract/NOT-2#root, spec://ai.lev/fpf-think-not/contract/NOT-7#root, spec://ai.lev/fpf-think-not/contract/NOT-8#root @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-1

# NOT.6 - Coordinate Complementary Representations through Shared References {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.6:1 - Problem frame {#problem-frame}

**Use this when** different representations support different parts of the work, but a reader cannot reliably combine their results or carry a change between them. A formula can support derivation, a table direct lookup and a diagram recognition of a relationship. Their usefulness together depends on knowing what corresponds and which claims each supplies.

Start with one operation that needs contributions from two representations. Identify the objects, quantities or relations those contributions concern. Construct the correspondence, perform the combined operation, then follow one relevant change through it.

The result is a usable combination: readers can obtain the joined answer, locate a disagreement and update the affected contributions. A discovered incompatibility can instead identify the subject decision that must be made before combining them.

The reader needs the interpretations of the participating representations and the subject relations used to connect them. NOT.2 and NOT.3 supply missing formation and reading rules; NOT.5 supplies a needed translation. A name or explicit correspondence beside the two representations can suffice for a small use.

Keep a single adequate representation when another adds no useful operation. Use NOT.5 for a one-time translation whose target alone supports the remaining work. This method is for continuing joint use, including representations that cannot be fully translated into each other. When different uses of a working method need complementary descriptions, ME.9 relates the claims those uses require; this construction supplies their notational connections.

## NOT.6:2 - Problem {#problem}

How can several representations jointly support reading, reasoning and change without requiring every reader to reconstruct their correspondence or silently reconcile their disagreements?

Side-by-side placement leaves that work unresolved. Equal names can denote different things; one thing can have different names. A table cell may be calculated from a model or measured independently. A displayed value may be old context or a constraint that a proposed edit must preserve. These differences determine which results can be combined and what should change next.

Forcing all representations into one form can remove the different operations that made them useful. The task is to construct the necessary connections while retaining those useful differences.

## NOT.6:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Local usefulness and joint reading | A representation can work well alone while making its connection to another hard to recover. |
| Shared references and different subjects | An object, its model and its encoded value can be related without being the same thing. |
| Redundancy and maintenance | Repeated content can aid comparison but must follow relevant changes. |
| Automatic propagation and intended edits | Updating every displayed value can erase a constraint or alter independently obtained information. |
| More operations and coordination effort | An additional representation earns its place through useful work, while it adds learning and navigation demands. |

## NOT.6:4 - Solution {#solution}

**Choose complementary operations → recover referents → construct correspondences → perform a joined reading → propagate the intended change → retain the useful combination.**

### NOT.6:4.1 - Select representations for the operations they support {#select-representations-for-the-operations-they-support}

Name the working question and the contributions needed to answer it. Use each representation for an operation it actually supports. A table may expose a recorded value, a formula generate values outside the table, and a graph reveal a shape under a declared scale. State what the reader obtains from each.

Keep a representation because it adds a needed distinction, constrains a plausible misreading or enables a useful operation. Do not infer a gain merely from using different media. Try the intended combination before expanding it.

The representations can overlap partially. They need not carry every fact or support identical operations. Identify the overlap needed for this use and the information that remains available only in one of them. Use NOT.5's loss and recovery construction when movement between them needs a translation.

### NOT.6:4.2 - Recover what each sign refers to {#recover-what-each-sign-refers-to}

For the joined operation, follow the relevant labels, positions and references to their referents. Establish whether two occurrences concern the same thing, different parts or versions of it, or things connected by a model or measurement relation. The same spelling does not decide this.

Give the correspondence a form the reader can follow: shared labels with a declared meaning, a small pairing table, a drawn connection or an explicit mapping rule. Use stable identifiers when names or positions can change independently. For a temporary two-item comparison, a direct explanation may be enough.

Include the context that makes the reference determinate. A column named time needs its unit and origin when compared with an axis; a position in a repeated score needs its cycle when several cycles are shown. Distinguish actual, planned and modeled values where they are different claims.

One source item can correspond to several target items, or several items to a summary. Show that multiplicity where it affects the operation. NOT.5 identifies what such a projection loses; a repeated label alone does not recover the missing distinctions.

### NOT.6:4.3 - Construct the relations that let results be combined {#construct-the-relations-that-let-results-be-combined}

Give the reading or construction rule connecting the matched contributions. A formula-to-table relation specifies which inputs generate which cells. A table-to-plot relation specifies axes, units and which cells determine a point. A procedure-to-flow-diagram relation specifies which described actions and conditions each node and connection expresses.

Distinguish a derived representation from an independent contribution. A graph generated from the same table can check rendering but does not supply an independent observation supporting the table's values. An observed trajectory and a predicted trajectory require the subject correspondence and comparison that relate them; C.29 supplies that modeling use.

Decide how a change will be handled. When a value is derived, give its source and transformation. When either side can be edited, give the backward policy or the condition under which a human choice is needed. Preserve information that the other representation cannot reconstruct.

For a chain of correspondences, follow the connection through the intermediate representations. If two routes reach what is supposed to be the same result, determine the agreement the work requires. A numerical tolerance can be appropriate for a plot, while an identity-sensitive reference needs the same referent. MATH.18 supplies the mathematical argument when the correspondence compares formal structures.

### NOT.6:4.4 - Perform the joined operation {#perform-the-joined-operation}

Take one input or object and follow it across the representations. Obtain each contribution, combine them using the stated relation and return the answer to the working question. Show where a reader switches representations and what is carried across that switch.

If the connection exists only in the author's memory, add the missing reference or operation. If the correspondence is clear but the subject inference is missing, obtain that contribution from the subject method or a collaborator. Merely adding another display will not perform the inference.

Use one consequential contrast to challenge the connection. A row with the same label but a different unit, a node in another version or a modeled value beside an observation may require different treatment.

For an immediate use, a worked joined reading may settle the question. A broader claim about how readily users can combine the representations requires evidence appropriate to their preparation and work; C.2.8 characterizes that recovery. Do not infer learning or transfer from the existence of the correspondence.

### NOT.6:4.5 - Propagate the intended change and expose conflicts {#propagate-the-intended-change-and-expose-conflicts}

Identify what changed and what the change asks to preserve. Separate an explicit new requirement from values merely retained in an old display. A change to one coefficient can require several table cells to change even if those cells were not directly edited.

Follow the affected references and derivations. Recompute dependent contributions or update their correspondence; leave independent information unchanged unless the subject work calls for its revision. If a representation no longer agrees and cannot yet be updated, make that limitation visible before its next joined use.

When edits arrive through several representations, combine their requirements and check whether a compatible result exists. The result can be several admissible revisions or a conflict. Do not manufacture a unique update when the supplied constraints leave a choice; use the declared policy or obtain the missing decision.

Distinguish changes with the same visible outcome but different meanings. Removing an item from an unfinished-work list can mean completion, cancellation or deletion. The intended action determines which other representations change. A suitable change description can be more informative than comparing two finished displays.

If a model and an observation disagree, return to their governing subject account. Updating the observation to match the model would destroy the independent contribution; changing the model may require a modeling decision. Coordination makes the disagreement usable rather than hiding it.

### NOT.6:4.6 - Retain the combination at the needed effort {#retain-the-combination-at-the-needed-effort}

Keep the participating interpretations, references and change rules available where the joint work happens. For a small construction, shared labels, one mapping rule and a worked change can suffice. Repeated edits or many interdependent elements can justify automated propagation, but the software needs the same declared correspondence and conflict behavior.

Stop when the intended joined operation works and the selected change can be handled or its unresolved decision is located. Remove a representation that adds upkeep without enabling a needed operation. NOT.7 helps redesign a connection that is correct but difficult to use.

Reopen the affected correspondence when the subject identity, version, unit, interpretation, reader operation or permitted edit changes. Unaffected representations may remain useful for their own questions even when a particular combined answer is temporarily unavailable.

## NOT.6:7 - Conformance Checklist {#conformance-checklist}

When the combination needs checking, ask the questions that can change its use.

- Does each retained representation support a named operation or needed distinction?
- Can the reader recover the referents and the relation between their occurrences?
- Are derived values distinguished from independent contributions and different claim kinds?
- Can one joined answer be obtained by following the stated correspondences?
- Does a change preserve its actual requirements rather than every value copied from an earlier display?
- Are incompatible edits or interpretations exposed at the affected contribution?
- Can the work stop with the usable combination, without unnecessary synchronized copies?

## NOT.6:9 - Consequences {#consequences}

Different representations can contribute to one answer without pretending that they contain the same information or that their referred things are identical. Readers can move between their useful operations and find where a changed assumption affects the combination.

The connections cost interpretation and upkeep. More automatic propagation can reduce repetitive work but makes the update policy consequential. Some disagreements locate a genuine subject decision; notation design cannot settle that decision by synchronizing appearances.

## NOT.6:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| NOT.1–.3 | Supply the operations, expression rules and interpretations on which the joined reading relies. |
| NOT.5 | Constructs translations, answer recovery and retained information where one representation omits needed distinctions. |
| MATH.18 | Establishes the formal preservation and compatibility needed when mathematical accounts are compared. |
| C.29 | Relates a mathematical model to its subject and governs the return of a modeled result. |
| ME.9 | Relates the claims needed for different uses of a working method; NOT.6 supplies their notational correspondences. |
| C.2.8 | Characterizes recoverable structure for the intended reader, preparation, access and effort. |
| NOT.7/.8 | Develop difficult reading-operation repair and temporal or embodied coordination. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-5#root for translation limits; spec://ai.lev/fpf-think-math/contract/MATH-18#root and spec://ai.lev/fpf-spec/contract/C-29#root for correspondence; spec://ai.lev/fpf-eng-me/contract/ME-9#root when representations describe a working method. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-not/contract/NOT-5#root @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-6

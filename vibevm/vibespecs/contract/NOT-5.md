# NOT.5 - Translate between Notations while Tracking Lost Distinctions {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.5:1 - Problem frame {#problem-frame}

**Use this when** work must continue in another notation and you need to construct or repair the translation. A diagram may need a textual form, an ordered performance may need a compact score, or an expression may need a representation accepted by another reader or tool.

Start with the operation the receiving notation must support. Construct its expression from the source's interpreted parts and connections, then use it to obtain the needed answer. Find a pair of source expressions that the translation would make indistinguishable. If the work needs their difference, retain it, enrich the target or restrict the translation's use.

The first result is a usable translation with an answer-recovery procedure, or a demonstrated loss and a concrete way to repair it. Recovering a needed answer, reproducing the source expression and carrying a target edit back are different demands; choose the ones the work actually has.

The reader needs the two notations' formation and interpretation rules, supplied by NOT.2 and NOT.3 where they are missing. Subject knowledge establishes which consequences matter. The examples need directed connections, ordered sequences and elementary arithmetic.

Use an established translation directly when its conditions meet the need. NOT.4 handles transformations within one notation. NOT.6 handles continuing coordination of several representations and their changes. CMP.12 develops an effective translator and its execution-preservation argument when software must perform the translation. A.6.3.RT governs the underlying representation change and the claims it can preserve.

## NOT.5:2 - Problem {#problem}

How can a change of notation make the next operation possible while keeping its answer connected to the source and exposing distinctions that can no longer be recovered?

Two source expressions can produce the same target expression. The target may still answer a useful question, but a reverse converter cannot infer which source was used from that target alone. A familiar default can conceal this loss. Conversely, requiring complete reversibility can exclude a cheap summary that is sufficient for the actual question.

A target edit adds another difficulty. There may be several source changes consistent with it, each preserving different features of the earlier source. Successful conversion in one direction does not choose among them.

## NOT.5:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Receiving operation and source detail | A simpler target can make one operation easier while removing distinctions needed by another. |
| Meaning and expression form | The same consequence can survive different layouts or spellings; some work also needs those forms retained. |
| Recovery and retained information | Keeping extra source information enables a return but adds storage, access and maintenance work. |
| Forward translation and backward change | A forward rule can determine the view without determining which source update the user intended. |
| Composition and accumulated loss | A locally usable conversion can remove information that a later conversion needs. |

## NOT.5:4 - Solution {#solution}

**Choose the receiving operation → construct the translation → obtain and return an answer → expose collapsed distinctions → repair the needed loss → establish the required return.**

### NOT.5:4.1 - Choose what must remain possible {#choose-what-must-remain-possible}

Name the source notation, target notation and intended reader operation. Specify the source expressions admitted for this use and the context required to interpret them. A drawing may use position as meaning or only as layout; a spoken sequence may rely on a separately maintained beat. Carry the context that the question uses.

Decide what the recipient must return: a value, a construction, an explanation, a reconstructed expression or a proposed change. These demands can require different information. An answer expressed in target units or names needs a way back to the source question.

If a source choice is unresolved, preserve the alternatives or the unresolved status that matters to the question. A default introduced by the translation is an added decision. Accept it only when making that decision is part of the intended work and its basis is available.

### NOT.5:4.2 - Construct target expressions from interpreted source structure {#construct-target-expressions-from-interpreted-source-structure}

For every kind of source part used by the operation, give its target construction. Then give a rule for translating their composition. Preserve operand order, connections, scope and reference where the interpretation uses them. Copying labels does not supply those rules.

Translate an expression by following its construction. For a diagram, this can mean declaring its nodes and translating each directed connection; for a sequence, translating each event while retaining its position or duration. Derive the target composite from those contributions. NOT.2 supplies the formation and reference rules; NOT.3 supplies the reading operations.

When a source ingredient has no target counterpart, choose an explicit treatment. Extend the target, carry an annotation, leave a visible unresolved part, or limit the admitted source expressions. Make this choice from the receiving operation. Silently deleting the ingredient or guessing its counterpart leaves the recipient unable to locate the loss.

For a mathematical interpretation, MATH.18 develops preservation and reflection of the required constructions and assertions. For a bijective change of mathematical representation, MATH.7 transports the operations through the inverse. Use those arguments when their conditions hold; a correspondence between printed signs alone does not establish them.

### NOT.5:4.3 - Perform the receiving operation and recover its answer {#perform-the-receiving-operation-and-recover-its-answer}

Translate a small source expression, perform the intended operation in the target and interpret the result as an answer to the original question. Show the return explicitly. If the target gives a list of numbered nodes, say which source nodes those numbers refer to. If it supplies only a bound or a set of possible answers, retain that limitation on return.

Compare this result with what follows from the source under its declared interpretation. A mismatch locates a failed translation rule, a missing premise or a target operation that answers a different question. Repair the affected correspondence before relying on that answer.

A target-side answer can be spurious for the source if the target admits additional possibilities. Retain the source restriction or construct the needed reflection argument. For example, allowing arbitrary real values does not preserve a source question that admits only whole counts.

One successful expression establishes that case. A reusable translation needs an argument for its admitted family, such as a rule-by-rule construction over expressions. A separating example can refute a proposed general claim. Additional checking is warranted when its result can change the use or repair of the translation.

### NOT.5:4.4 - Expose distinctions the target collapses {#expose-distinctions-the-target-collapses}

Look for different admitted source expressions with the same target expression. Ask whether the required operation gives different answers on them. If it does, the target alone cannot determine that answer: the translation has removed something the work needs. Section :5.2 makes this failure visible through cue order.

If every collapsed pair gives the same needed answer, the loss need not obstruct that question. For a claim about the whole admitted family, justify this independence over that family rather than infer it from a few pairs. MATH.2 supplies the mathematical construction through equivalence classes when that form is useful.

Include differences in assumptions, unfinished choices, references and reading context when they can change the answer. Equal visible strings can have different interpretations under different contexts. Conversely, two differently laid out diagrams can express the same directed structure when position has no role in their interpretation.

For several translation stages, follow the information needed by the final operation through each stage. A later, richer format cannot recover a distinction that an earlier stage removed unless another input supplies it.

### NOT.5:4.5 - Repair the loss needed by the work {#repair-the-loss-needed-by-the-work}

Choose the least burdensome repair that actually restores the operation. Retain the original expression when an occasional return is enough. Add the missing distinction to the target when the recipient must work independently. Otherwise, carry supplementary information with a defined recovery rule.

Call that supplementary information a *complement* when the target and the supplement together permit the required source recovery. State what it contains and how the return uses it. In :5.2 the position of a cue complements its count; in :5.3 a retained phase duration selects one backward update. A statement that the conversion is reversible cannot replace this construction.

Keep the target and its supplement associated with the same source. If the target is edited, check whether the old supplement still permits the intended reconstruction. A stored position can become invalid after deleting an event. Locate that conflict instead of returning an invented original.

The repair may instead be an explicit narrower use. A cue count remains useful for inventory even when it cannot recover order. Retain that useful result and identify the additional contribution needed by an order-sensitive question.

### NOT.5:4.6 - Establish the return that the work requires {#establish-the-return-that-the-work-requires}

For an unchanged round trip, translate and reconstruct the source at the required level: the same expression, the same interpreted structure or the same needed consequence. State which level is obtained. Recovering a directed graph up to layout does not recover where its boxes were drawn.

For a target edit, construct a backward update using the edited target and retained source information. Specify what remains fixed and what may change. In the ordinary single-view setting, check two properties: returning an unchanged view leaves the source unchanged; translating the updated source yields the requested view. These properties still leave a choice of update policy, worked in :5.3. They do not mean that all possible edits must be accepted.

When several views constrain a shared source, distinguish the user's changed requirement from values merely copied from the earlier view. NOT.6 handles their propagation and possible conflict. An unchanged value in a submitted view is not necessarily an instruction to freeze it.

If conversion performs effects such as asking a reader for missing information or changing external state, include the relevant behavior in the return claim. Recovering the same output value need not undo those effects. CMP.12 supplies the computational correspondence when an executable implementation is required.

Stop once the chosen operation and required return work within their stated conditions. Retain the translation rule, any supplement and the loss that changes later use where the recipient can find them. Reopen the affected construction when the receiving question, source interpretation or admitted edits change.

## NOT.5:7 - Conformance Checklist {#conformance-checklist}

When the translation needs checking, use the questions relevant to its declared use.

- Can the recipient construct the target from the source parts, connections and required context?
- Can a target result be returned as an answer to the source question at the stated strength?
- Do two collapsed source cases require different answers for any promised operation?
- Does a necessary supplement have a usable recovery rule and remain associated with the right source?
- Is the round-trip claim about expressions, interpreted structures or selected consequences?
- For an edited target, is the backward policy explicit, including incompatible edits?
- Does a changed question or translation stage require a distinction already discarded?

## NOT.5:9 - Consequences {#consequences}

The recipient gains a usable expression and can tell which answers, reconstructions and changes it supports. A loss becomes a reason to choose a supplement, a richer notation or a narrower use instead of an unexplained conversion failure.

Retained information has an access and maintenance cost. A more restrictive reverse policy can protect a source feature while excluding useful edits. These trade-offs remain choices about the work; a round-trip law alone does not settle them.

## NOT.5:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| A.6.3.RT | Governs representation changes, preservation of the claimed content and disclosure of loss or narrowed use. |
| NOT.1–.3 | Supply the needed operations, expression construction and operative interpretations used by the translation. |
| NOT.4 | Supplies justified transformations within a notation that can be combined with translation. |
| MATH.2/.7/.18 | Supply quotient-based independence, reversible transport, and preservation/reflection through mathematical interpretations when those constructions apply. |
| C.29.1 | Supplies correspondence and result return when using a mathematical representation for the original problem. |
| CMP.12 | Constructs an effective interpreter or translator and the required relation between executions. |
| NOT.6 | Maintains complementary representations and propagates changes through their shared references. |
| NOT.7/.8 | Develop reading-effort redesign and temporal or embodied representations when the target has those demands. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-3#root for the interpretation; spec://ai.lev/fpf-think-math/contract/MATH-2#root/.7/.18 for identification and preserved relations; spec://ai.lev/fpf-think-not/contract/NOT-6#root for continued joint use. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-not/contract/NOT-6#root @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-5

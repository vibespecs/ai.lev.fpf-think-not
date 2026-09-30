# NOT.3 - Give Expressions an Operative Interpretation {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.3:1 - Problem frame {#problem-frame}

**Use this when** a notation can form expressions, but its users lack a clear way to obtain the consequence those expressions are supposed to support. A legend may explain the signs while leaving the reader to invent how to combine, inspect or manipulate them.

Start with one question an expression should help answer. Give its relevant parts an interpretation, supply the operations needed to read them together, and follow that reading to a result. A useful first result can also be a located gap: a value, interpretation rule or reader capability that must be supplied before the question can be answered.

An **operative interpretation** here connects what an expression stands for with what a prepared reader can do to obtain a needed consequence from it. Reading can involve calculation, inspection of a diagram, rule-based manipulation or enactment. The reader may be a person or a computational agent; the applicable operations and preparation depend on that reader.

The designer needs the intended subject account and the operations on which the reading depends. The first example uses elementary Boolean reasoning, explained in the case; the temporal example uses addition and interval comparison. A machine implementation is a further construction when required.

Use an existing interpretation directly when it already supplies the needed reading. A.6.3.RT.OE addresses building an operative expression under an available scheme. Use the present method to develop or repair the scheme's interpretation and its reading operations. NOT.2 addresses missing grouping, binding and connection rules.

## NOT.3:2 - Problem {#problem}

How can a notation's interpretation give its intended reader a usable way to obtain a consequence, while keeping the conditions of that consequence recoverable?

Assigning names to marks can leave their combined use unexplained. Assigning a mathematical meaning can specify an answer without providing a way to obtain it. A familiar reader may bridge either gap from experience while a new reader cannot tell which operation is missing.

## NOT.3:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Meaning and obtaining | An expression can denote a result that the available reader cannot compute or recognize. |
| Local rules and whole expression | A reading of each component must account for their composition and context. |
| Useful tacit skill and recoverable preparation | A trained perceptual or manipulative operation can be efficient but unavailable to another reader. |
| Several reading routes and one required consequence | Different routes can expose different structure or cost different effort while agreeing on the intended answer. |
| Represented condition and actual occurrence | A model can imply a result without establishing that the described situation obtained. |

## NOT.3:4 - Solution {#solution}

**Choose the consequence → interpret the expression's parts and composition → supply the reading operations → perform a case → test a consequential change → retain the usable reading and its conditions.**

### NOT.3:4.1 - Choose what the reading must produce {#choose-what-the-reading-must-produce}

State the question, the expression and the information available outside it. Identify what would count as a useful result. Examples include the value of a formula, a permitted next action, whether two intervals overlap, or a consequence of a diagram's relations.

Distinguish obtaining the expressed answer from establishing its use in the subject matter. Reading an interval from a schedule can answer what is planned; observing what happened needs the corresponding observation. The interpretation should identify which question it answers.

Specify the reader's available operations. It may be reasonable to presuppose arithmetic, following a visible connection or a trained movement. Expose a less familiar operation if the intended reader could otherwise mistake its absence for a defect in the expression. A short prerequisite explanation can suffice; a capability that requires practice belongs in the appropriate learning method.

### NOT.3:4.2 - Interpret components, composition and context {#interpret-components-composition-and-context}

For the parts used by the question, specify what they denote or instruct and how their combination is interpreted. Include grouping and reference rules from NOT.2. An arrow may supply an input to an operation, express a precedence condition or prescribe a movement; choose its role in this scheme before deriving a consequence.

Give the interpretation of a compound expression in terms that permit its use. For a compositional mathematical scheme, interpret the parts and then apply the corresponding operation to their interpretations. MATH.5/.18 develops that construction and its preservation questions. When context contributes to interpretation, include the relevant context among the inputs rather than assigning a context-free meaning that the notation does not support.

If the expression admits alternatives or has an unresolved part, specify what can still be concluded. A reader may be able to obtain a common consequence across the alternatives. Another question may have to wait for the missing information. Preserve that distinction instead of silently completing the expression.

### NOT.3:4.3 - Construct the reading operations {#construct-the-reading-operations}

Show how the intended reader moves from the expression and available inputs to the result. For each indispensable step, identify what is inspected or changed and how the next step uses what was obtained. The procedure may reuse an established method rather than explain that method again.

For a formula, this can mean resolving a parameter, evaluating selected subexpressions and combining their values. For a diagram, it can mean identifying a boundary, following the admitted connections and applying the corresponding inference. For a performed notation, it can mean recognizing a cue and executing a learned action. Choose operations that the reader can actually perform under the stated conditions.

Keep the reasoning behind a manipulation available at the level required by the work. A rule may be applied fluently after training, while changing the rule requires understanding what it preserves. NOT.4 develops expression transformations; B.5.RC/RA helps recover an unfamiliar construction or argument when that is the missing contribution.

If a mathematical interpretation leaves the required obtaining procedure unavailable, name that remaining problem. CMP.12 constructs effective evaluation when the expression's operations admit it; other CMP methods can help construct the needed algorithm. Denotation alone does not establish computability or affordability. A human reading or trained perceptual operation also needs its actual capability and access conditions.

### NOT.3:4.4 - Perform the reading and locate where it depends on additional knowledge {#perform-the-reading-and-locate-where-it-depends-on-additional}

Take an expression whose relevant parts and input values are supplied. Carry the reading through to its stated result. At a step that cannot be performed, distinguish a missing input, an undefined interpretation and an unavailable operation. These lead to different repairs.

Compare the result with the intended consequence under the subject account. Repair an interpretation rule when it yields a different answer. Repair the reader preparation or access when the rule is usable in principle but cannot be carried out under the current conditions. If the subject account itself leaves the consequence unresolved, return that question to the corresponding mathematical, physical, computational or other practice.

When more than one reading route is offered, perform the routes on a case that could expose a difference. Establish the agreement needed by the use, or explain why the routes answer different questions. A route that only returns a final value may lose the dependency structure another operation needs.

### NOT.3:4.5 - Change one condition that matters to the interpretation {#change-one-condition-that-matters-to-the-interpretation}

Change a value, grouping, reference, context or intended question that could alter the result. Use the same rules to recover the new answer, or locate the rule that must change. The challenge should test the chosen interpretation rather than introduce an unrelated subject problem.

For a formal family, a general argument can establish that the reading operations implement the interpretation across that family. MATH.18 supplies interpretation-preservation questions; CMP.12 supplies executable translation and evaluation. For human or embodied use, C.2.8 can characterize what the prepared reader recovers and distinguish an expert walkthrough from observed use. Choose further checking when it can change the interpretation or permitted reliance.

### NOT.3:4.6 - Keep the operative reading available to its users {#keep-the-operative-reading-available-to-its-users}

Provide the interpretation, the indispensable reading operations and their prerequisites where the intended user can find them. A legend, one worked reading and a reference to a known method may be enough. A new operator needs enough explanation to use it, rather than only a new name.

Stop when the required consequence can be obtained at the declared scope, or when the missing contribution and the next way to obtain it are clear. Retain a slower explanatory route alongside a fluent route when users need to learn, justify or change the operation. A further notation redesign belongs to NOT.7 if the reading works but imposes avoidable difficulty.

## NOT.3:7 - Conformance Checklist {#conformance-checklist}

When the interpretation needs checking, ask the following questions at the scope of the proposed use.

- Is the consequence to be obtained distinguishable from the subject claims on which it depends?
- Do the used parts, their composition and relevant context have an interpretation?
- Can the intended reader identify and perform the indispensable reading operations, or locate the missing input or capability?
- Does the worked reading obtain the stated result without an unexplained inference supplied only by the author?
- Does a consequential change lead to the corresponding new result or to a located interpretation question?
- If several routes are offered, is their agreement or difference established for the observations the user needs?

## NOT.3:9 - Consequences {#consequences}

The notation acquires a path from expression to a useful consequence. Users can distinguish a missing input from a missing rule or capability and can allocate those contributions among people and computational agents.

Providing an operative interpretation can require more work than defining symbols. Several reading routes may be worth retaining because users need different intermediate results or have different preparation. A successfully performed small case supports that use; wider claims need the corresponding argument or experience.

## NOT.3:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| NOT.1/.2 | Supply the required operations and the formation, reference and connection rules. |
| A.6.3.RT.OE | Constructs an operative expression when the scheme and reading operations are already available. |
| MATH.5/.18 | Constructs and compares mathematical interpretations, including consequences preserved through composition. |
| CMP.12 | Constructs an effective interpreter or meaning-preserving translation when the obtaining problem is algorithmic. |
| B.5.RC/RA | Recovers the construction or argument needed when a reading contains an unfamiliar step. |
| NOT.4/.5 | Develops use-preserving transformations and translations once the relevant interpretation is available. |
| NOT.7/.8 | Develops an easier reading or a temporal/embodied notation where the available route remains difficult. |
| C.2.8 | Characterizes recoverable structure under the reader's preparation, access and effort conditions. |
| C.29 and B.5.MPC | Connect an interpreted mathematical consequence with its physical subject and the work needed to use it. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-2#root for formed expressions; spec://ai.lev/fpf-think-math/contract/MATH-18#root for mathematical interpretation; spec://ai.lev/fpf-think-cmp/contract/CMP-12#root when an effective interpreter is needed. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-not/contract/NOT-2#root, spec://ai.lev/fpf-think-not/contract/NOT-5#root @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-3

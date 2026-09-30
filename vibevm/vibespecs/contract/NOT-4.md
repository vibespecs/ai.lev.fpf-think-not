# NOT.4 - Construct Transformations of Expressions That Preserve Their Use {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.4:1 - Problem frame {#problem-frame}

**Use this when** an expression is difficult to read, derive from or change, and you need a rule for turning it into a more useful expression without losing the consequence on which the work relies. Examples include naming a repeated construction, exposing a hidden intermediate step, regrouping a diagram, or replacing a long sequence by an expandable abbreviation.

Start with the reader operation that is difficult. Construct a proposed manipulation from the expression's formation and interpretation rules. State where the manipulation applies, explain what it preserves, then obtain and use a transformed expression. The result can instead be a located condition that prevents the proposed transformation.

The reader needs the notation's interpretation and the subject laws used in the manipulation. NOT.2 supplies grouping and reference rules; NOT.3 supplies interpretation and reading operations. Elementary arithmetic and ordered sequences suffice for the worked cases. More specialized laws can be supplied by a collaborator.

Apply an existing transformation directly when its rule and conditions already answer the question. Use this method when that rule must be constructed, extended or repaired. A change of notation calls for NOT.5's translation and recovery work. Constructing an effective interpreter or compiler calls for CMP.12. Choosing a different physical process or working method requires the corresponding subject methods as well as a way to express the change.

## NOT.4:2 - Problem {#problem}

How can a notation provide useful transformations whose applicability and preserved consequences remain understandable when the expression or its context changes?

A visually simpler expression can hide a necessary distinction. Reusing a name can bind an occurrence that previously referred elsewhere; combining repeated signs can combine two actions that were meant to occur separately. A valid equality may hold only under a local assumption. Without those conditions, a transformation can preserve one displayed answer while changing the work it is supposed to support.

## NOT.4:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Easier use and retained distinctions | A compact or regular expression can discard information needed by another operation. |
| Local manipulation and surrounding context | Replacing a part must respect the names, connections and assumptions supplied by its surroundings. |
| One useful result and a reusable rule | A successful instance supports that instance; a rule for a family needs an argument covering that family. |
| More alternatives and search cost | Keeping several equivalent forms can enable a later move while increasing the work of finding and comparing them. |
| Meaning and execution | Equal mathematical values can come from computations or actions with different effects and costs. |

## NOT.4:4 - Solution {#solution}

**Choose the use to preserve → construct the manipulation → establish its conditions → transform and read → challenge the changed condition → retain the useful rule or alternatives.**

### NOT.4:4.1 - Choose the operation and the observations to preserve {#choose-the-operation-and-the-observations-to-preserve}

Identify the expression, its interpretation and the next operation that should become easier. The aim may be to see a shared construction, carry out an inference, change one definition, or recover a particular step in a sequence. A shorter expression is useful only insofar as it helps such work.

State what must remain obtainable. A numeric value, a sequence of actions, the identity of a shared component and an explanation of intermediate steps are different demands. Retain the distinctions used by the actual question. If users need both a compact result and the derivation, keep the derivation available rather than assuming the result reconstructs it.

For a computation or action description, include the effects that matter: repeating a measurement twice can produce different inputs from reading one measurement twice. CMP.12 develops the corresponding execution-preservation question. A purely mathematical reading may require only equality of values under its stated interpretation.

### NOT.4:4.2 - Build a rule from the structure causing the difficulty {#build-a-rule-from-the-structure-causing-the-difficulty}

Follow the difficult reading or edit and locate the expression structure responsible for it. Propose a manipulation using the available constructors and interpretation laws. For repeated subexpressions, try a named definition and references to it. For a long regular sequence, try an abbreviation with a defined expansion. To expose an inference, try expanding a definition or introducing an intermediate expression justified by a subject law.

Describe the matched form and its replacement, including which parts may vary. Preserve the surrounding expression and the connections through which it uses the replaced part. A diagram rule needs the relevant input and output places, not only similar-looking boxes. NOT.2 supplies those structural distinctions.

Introduce a name with a scope that reaches the intended occurrences. Choose a fresh name, or rename conflicting bound occurrences consistently, when the new scope would otherwise change an existing reference. Repeated spelling alone does not establish that two occurrences can be replaced by one shared definition.

For a growing rule family, construct several candidates and reuse previously established laws. Automatic enumeration or an AI proposal can help generate candidates. Their source of generation does not establish their validity: connect each used rule to its interpretation or an already established derivation. The search and validation algorithms belong to the applicable computational methods; this method determines the notation operation they must realize.

### NOT.4:4.3 - Establish where replacement preserves the needed consequence {#establish-where-replacement-preserves-the-needed-consequence}

Interpret the matched form and the replacement under the same allowed inputs and context. Follow the meaning of their parts and composition far enough to obtain the required agreement. Use a known law where its premises hold; derive the missing law when that is the unresolved mathematical contribution. MATH.17 and MATH.18 supply operations-on-operations and interpretation reasoning.

Check the conditions that the proposed rule actually uses. Freshness of a name matters for introducing a binding; defined division matters for cancellation; an ordered boundary matters for a diagram connection. For a rule such as `x/x -> 1` over real numbers, `x != 0` is necessary. A condition established inside one branch remains local to that branch.

When replacement may occur inside a larger expression, show that the relevant enclosing constructors respect the chosen agreement. If the rule preserves a final value but changes an intermediate observation used outside the replaced part, restrict the replacement or retain that observation. A local equality under one assumption is not permission to merge every occurrence of the same printed term.

For a single bounded use, a direct derivation can suffice. For every expression in a family, establish the corresponding general argument. A separating case can refute the proposed rule; agreement on a few examples cannot establish a universal law. Choose additional checking when uncertainty about the rule can change its permitted use.

### NOT.4:4.4 - Construct and use the transformed expression {#construct-and-use-the-transformed-expression}

Match the rule to the selected expression, instantiate its varying parts and satisfy its side conditions. Replace only the matched part, reconnect it to its surroundings and read the resulting expression using the notation's rules. Obtain the answer or perform the edit that motivated the transformation.

Compare the actual work before and after. A named definition can remove repeated edits while adding reference-following. An expanded derivation can be longer while making a missing inference accessible. Preserve both forms when they serve different needed operations; NOT.6 develops their maintained correspondence.

If the new form loses information needed to continue, restore that information or narrow the claim to the uses it still supports. Retaining a link to a derivation or an expandable definition can be enough. A label saying that the expressions are equivalent does not supply the missing reading procedure.

### NOT.4:4.5 - Challenge the condition most likely to fail in reuse {#challenge-the-condition-most-likely-to-fail-in-reuse}

Change a relevant binding, assumption, input class or intended observation. Repeat the affected transformation and reading, or explain why the rule no longer applies. Test the rule's boundary rather than adding an unrelated difficult example. Sections :5.1 and :5.3 show changed bindings and local assumptions.

If a transformation is to run automatically, give CMP.12 the admitted expression structures, matching and replacement rules, and observations to preserve. An algorithm for repeatedly applying rules also needs a search strategy and a stopping condition. The availability of several valid rewrites does not imply that applying them in arbitrary order terminates or finds the most useful form.

### NOT.4:4.6 - Retain a useful rule or a useful set of forms {#retain-a-useful-rule-or-a-useful-set-of-forms}

Keep the rule, the conditions that matter to its use and a recoverable reason for the preserved consequence. A short explanation beside a simple rule is enough when no larger account is needed. Reopen the affected rule when its interpretation, allowed context or required observation changes.

For one known operation, stop after a suitable transformed expression is obtained. When committing to one form repeatedly blocks other useful transformations, retain alternatives and defer the choice. Equality saturation is one computational way to represent many equivalent forms and select from them. It requires a suitable expression theory, valid rules, a selection criterion and resource limits; it is not the default procedure for a small manual rewrite.

Compare retained forms by the work they support, using NOT.1's comparison and NOT.7's redesign where needed. No one presentation needs to serve every reading, derivation and edit.

## NOT.4:7 - Conformance Checklist {#conformance-checklist}

When the proposed transformation needs checking, examine the questions that bear on its intended use.

- Is the reading or edit to improve stated, together with the consequence to preserve?
- Can the matched structure, replacement and their connection to the surrounding expression be recovered?
- Do references, local assumptions and side conditions remain valid at each place where the rule is used?
- Does the preservation argument cover the stated family, or is the conclusion limited to the instances examined?
- Has a transformed expression actually supported the intended reading or change?
- Does the nearby failing case reveal the condition that blocks an invalid reuse?
- Can the work stop with this result, or does a stated further use justify retaining or searching additional forms?

## NOT.4:9 - Consequences {#consequences}

The notation gains a usable way to derive, expose or change expressions. A reader can apply the rule, recognize a failed condition and preserve a useful earlier form when the new one supports different work.

Constructing the rule costs interpretation and sometimes a mathematical argument. More forms can improve choice while making reading, search and maintenance harder. Preserving one consequence leaves other observations to their own conditions; widening use can therefore require retaining additional structure.

## NOT.4:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| NOT.1 | Supplies the operation to improve and the comparison of work enabled and displaced. |
| NOT.2/.3 | Supply expression structure, binding, interpretation and reading operations. |
| MATH.17/.18 | Construct operations on operations and establish the interpretation or composition laws used by a transformation. |
| CMP.12 | Constructs an effective interpreter or translation and relates source and target execution where automation is needed. |
| C.2.8 | Characterizes what a prepared reader can recover from the transformed expression; a formal equality alone does not establish reader accessibility. |
| NOT.5/.6 | Develop translation between schemes and coordination of retained complementary representations. |
| NOT.7/.8 | Develop reader-operation redesign and temporal or embodied notation where those are the affected demands. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-2#root/.3 for binding and meaning; spec://ai.lev/fpf-think-math/contract/MATH-17#root/.18 for composition and interpretation; spec://ai.lev/fpf-think-cmp/contract/CMP-12#root for executable transformation. @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-4

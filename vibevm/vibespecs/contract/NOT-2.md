# NOT.2 - Define Expression Rules for Recoverable Binding and Composition {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## NOT.2:1 - Problem frame {#problem-frame}

**Use this when** a notation needs rules for combining expressions or referring to their parts, and the proposed marks leave those rules unclear. Readers may disagree about an operation's operands, the declaration an occurrence of a name uses, or which connections join two components.

The working question is “How can another user construct and recover the intended arrangement under these rules?” Start with one expression that admits two consequentially different readings. Give its components explicit places, make their grouping and references recoverable, and use the resulting construction to perform the intended operation.

The result is a small set of formation, binding and connection rules demonstrated by an expression and a contrasting case. These rules can support mathematical formulas, diagrammatic descriptions or structured sequences. A complete grammar or software parser is needed only when the work requires it.

The reader must know what the relevant components and operations mean, or obtain that account from a practitioner. The examples below require elementary arithmetic and the stated conventions. Theory of formal languages and category theory are optional tools for extending or proving properties of a scheme.

Use the rules already provided by a suitable notation when they settle the question. A.6.3.RT.OE helps construct an operative expression under such a scheme. Use NOT.1 first if the work has not yet determined which distinctions or operations the notation must support.

## NOT.2:2 - Problem {#problem}

How can the rules for forming an expression expose its components, references and permitted composition well enough to support the required reading or change?

A printed formula can conceal two groupings. The same letter can name an external parameter and a locally introduced variable. Diagram ports with the same value type can have different roles. Correctly recognizing the individual signs therefore leaves open which whole has been expressed.

## NOT.2:3 - Forces {#forces}

| Force | What must be reconciled |
| --- | --- |
| Compact writing and recoverable structure | Omitting delimiters saves space but can hide an operand boundary. |
| Local naming and larger composition | A useful short name inside one component can collide with a name supplied by its surroundings. |
| Equal types and different roles | Two admissible inputs may occupy different positions in an operation. |
| Flexible presentation and stable interpretation | Layout may change while connections remain; another layout change may alter the expression. |
| Partial construction and usable interpretation | An unfinished expression can retain a missing part, provided the reader knows which operations remain available. |

## NOT.2:4 - Solution {#solution}

**Identify the constructors and their places → make grouping recoverable → define how references are resolved → define permitted connections → construct and read contrasting cases → abbreviate only what the reader can recover.**

### NOT.2:4.1 - Identify the expression constructors and their operands {#identify-the-expression-constructors-and-their-operands}

Take the needed operation and distinctions from the working question or NOT.1. Describe the elementary expressions and the ways to construct a larger expression from them. For each construction, identify the required parts and what may occupy each place.

For example, a summation expression needs an index declaration, bounds and a body. A two-input transformation needs both inputs and a way to distinguish their roles. A repeated sequence needs a repeat count and the sequence being repeated. These are different constructors with different rules.

State the restrictions that the intended use needs. The restrictions may concern the kind of an operand, the number and order of connections, or a relation between component interfaces. Keep a missing part visible when partial construction is allowed. Identify the operation that requires the part to be supplied.

### NOT.2:4.2 - Make the composition structure recoverable {#make-the-composition-structure-recoverable}

Choose how a user can determine which parts belong to each construction. Text may use delimiters, indentation or precedence; a diagram may use enclosures, named ports or connections. A notation unfolding in time may use a learned boundary gesture or a segmentation convention. Explain the selected rule where its effect is not already established for the intended reader.

Try a nested construction. Recover the outer operation and its immediate parts, then repeat that reading within each part. This is a useful structural reading for tree-like expressions. When a component is shared or a connection returns to an earlier component, expose its reference or connection instead of pretending that every use is an independent nested copy.

Choose the structural distinctions needed by the operation. Some schemes identify several bracketings or drawings as the same expression. Establish the relevant equivalence before omitting their differences. If alternatives are intentionally unresolved, show that unresolved choice and postpone only the operation that needs it decided.

### NOT.2:4.3 - Define which declaration or external value a reference uses {#define-which-declaration-or-external-value-a-reference-uses}

Identify the constructions that introduce local names and the parts in which those names apply. State how a name occurrence reaches its declaration or an input supplied from outside. The visible extent of a box or line becomes a scope boundary only through an established rule of the notation.

For a notation with lexical scope, a common rule resolves a name at its nearest enclosing declaration with that name; if there is none, the value must come from the declared external context. Adopt that rule only when it fits the intended interpretation. Other schemes can make references available through earlier statements, explicit identifiers or connections. Define their resolution accordingly.

Trace the references in one expression with repeated names and one expression with a free input. Here a free input is one whose value must be supplied from outside the expression. If insertion, copying or renaming changes which declaration an occurrence reaches, expose that change before treating the result as equivalent. NOT.4 develops transformations that preserve the intended use.

For a reusable component, distinguish its locally introduced names from the inputs and results made available at its boundary. Compose components by those boundary references. A displayed label can be repeated without identifying its occurrences as the same declaration; the reference rule must settle that question.

### NOT.2:4.4 - Define the permitted connections between components {#define-the-permitted-connections-between-components}

Specify which component places can be connected and what the connection means for forming the expression. If a connection passes a result to an operand, include the operand's position or role as well as its accepted kind. Two inputs of the same kind may still be ordered.

Construct the compound expression and determine its remaining external inputs and outputs. Check each newly connected boundary; an unconnected required input remains an input to be supplied. If the scheme permits shared values, show how repeated references obtain that value. If it describes resources whose copying requires an operation, include that operation rather than deriving copying from a forked line alone.

A connection that forms a cycle needs a rule admitting and interpreting that cycle. Depending on the practice, it might describe an equation, feedback through time or a repeated computation. Choose the intended construction before using one picture for these different operations. NOT.3 develops its interpretation, and CMP.12 supplies an effective evaluator when one is required.

Formation rules establish a permitted expression. Whether its described mathematical construction exists, its algorithm terminates or its physical realization works remains a question for the corresponding methods. The rules should expose the information those questions need.

### NOT.2:4.5 - Construct and read the cases that challenge the rule {#construct-and-read-the-cases-that-challenge-the-rule}

Build the intended expression from the declared parts. Recover its grouping, resolve the references and identify the component boundaries. Then perform the required operation with the supplied interpretation.

Use a contrasting case that could reveal a mistaken rule. Depending on the chosen construction, change the grouping, reuse a name inside another scope, exchange two ports or introduce a shared component. Select the challenge because its interpretation can change the result.

If two readers still recover different arrangements that matter to the work, locate the point of divergence. Add or repair the corresponding delimiter, reference rule or connection convention. If both arrangements express the intended equivalence, make that equivalence part of the scheme instead of forcing one arbitrary drawing.

### NOT.2:4.6 - Retain usable conventions and controlled abbreviations {#retain-usable-conventions-and-controlled-abbreviations}

Keep the rule at the scale required by its next use. A legend and a worked construction can suffice for a local diagram; repeated automated processing can justify a grammar, parser or structural editor. A user must be able to recover any omitted structure that changes the operation.

For an abbreviation, give the expansion or another way to establish its meaning. If several expansions are allowed, show why the difference does not affect the intended use. NOT.4 handles the corresponding preservation argument. Retain a visible distinction when no such argument is available and the choice matters.

The method finishes with rules that permit the required construction and make its use recoverable, or with a specific unresolved formation or interpretation question. Teaching those rules and comparing their reading cost use the relevant learning and explanation methods; a more explicit syntax alone does not establish that a reader has learned it.

## NOT.2:7 - Conformance Checklist {#conformance-checklist}

Use the applicable questions when the construction rules need checking.

- Can the reader recover the components and the places they occupy from the expression and available conventions?
- Are the groupings that change the operation distinguishable, or explicitly retained as unresolved alternatives?
- Does each needed reference reach its declaration, external input or unresolved place according to the stated policy?
- Do composition rules account for the roles of connected participants and the resulting external boundary?
- Does a contrasting construction expose a consequential change of grouping, reference or connection?
- Can an abbreviation be expanded or otherwise interpreted without losing a distinction needed by the operation?

## NOT.2:9 - Consequences {#consequences}

Users can construct expressions whose parts and references can be recovered, and can locate where a change alters the described operation. The same rules provide an input to interpretation, translation and automated processing.

Explicit structure can make an expression longer or impose conventions to learn. Controlled abbreviations and alternative views can reduce that burden once their interpretation is established. A scheme can also require a richer account of scope or interfaces than the first examples revealed.

## NOT.2:12 - Relations {#relations}

| Pattern | Contribution to the working method |
| --- | --- |
| NOT.1 | Selects the distinctions and operations the notation must support. |
| A.6.3.RT and A.6.3.RT.OE | Supply representation-scheme distinctions and expression construction when rules already exist. |
| NOT.3 | Develops the interpretation and reader operations that use the constructed expressions. |
| NOT.4 | Develops transformations with the necessary preservation, binding and side conditions. |
| MATH.17/.18 | Supplies operations on operations and interpretations for formal accounts of composition and binding. |
| CMP.12 | Constructs effective evaluation and translation of an admitted expression structure. |
| NOT.5/.6 | Develops translations or complementary expressions while retaining needed references. |
| NOT.7/.8 | Develops redesign for difficult reader operations and notation carried through time or embodied action. |
| C.2.8 | Characterizes what the prepared reader can recover under the actual access and effort conditions. |


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-not/contract/NOT-1#root for the operation; spec://ai.lev/fpf-spec/contract/A-6-3-RT#root for relation and expression distinctions; spec://ai.lev/fpf-think-not/contract/NOT-3#root/.4 and spec://ai.lev/fpf-think-cmp/contract/CMP-12#root for interpretation and transformation. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-not/contract/NOT-1#root, spec://ai.lev/fpf-think-not/contract/NOT-3#root, spec://ai.lev/fpf-think-not/contract/NOT-4#root @status:spec/done

#source spec://ai.lev/fpf-think-not/source/NOT-2

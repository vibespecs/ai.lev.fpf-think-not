# NOT.8 - Construct Temporal or Embodied Notation with a Reading Procedure: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Notational Engineering DPF* (20 September 2026), `Foundational Thinking DPF Suite/NOTATIONAL-ENGINEERING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## NOT.8:5 - Archetypal Grounding {#archetypal-grounding}

### NOT.8:5.1 - Recover a cue's place in a beat {#recover-a-cue-s-place-in-a-beat}

Choose a beat divided into four equal positions. In the Takadimi convention these positions are voiced as ta, ka, di and mi. For this example, a dot in the written grid means no new onset at that position; it does not specify how long an earlier sound continues.

| Position within the beat | 0 | 1/4 | 1/2 | 3/4 |
| --- | --- | --- | --- | --- |
| Position syllable | ta | ka | di | mi |
| First onset pattern | ta | . | di | . |
| Shifted onset pattern | . | ka | . | mi |

Establish a steady beat, divide it into four and keep the beat's start identifiable. The first pattern has onsets at 0 and 1/2. A shift of one quarter-beat, within this one-beat example, yields onsets at 1/4 and 3/4. The new syllables identify the new positions. Repeating the same two spoken syllables without their reference would not express this change of placement.

At a beat duration of one second, the first onsets occur at 0 and 0.5 seconds; the shifted ones at 0.25 and 0.75 seconds. At a beat duration of half a second, the corresponding times halve while the relative positions remain. A requirement for an onset at an absolute 0.5 seconds is therefore a different requirement.

If the sound between two known positions is unrecorded, do not replace that gap by a written dot claiming no onset. Preserve the missing-observation status. If the next operation asks how long notes are held, add the needed duration convention: the onset grid alone does not answer it.

This is a notation construction, not a claim that reading the table teaches fluent rhythmic performance. Maintaining the beat and coordinating speech are available skills or contributions to be learned.

### NOT.8:5.2 - Read a movement relative to a changing body frame {#read-a-movement-relative-to-a-changing-body-frame}

A tabletop movement score uses two signs. `R` means move one grid unit to the performer's right without turning; `F(2)` means move two units forward without turning. The signs describe successive completed displacements. The starting position is (0, 0), with east as positive x and north as positive y.

A performer initially facing north reads `R; F(2)` as an eastward unit displacement followed by two northward units. The endpoint is (1, 2). The reading procedure first recovers the starting orientation, translates each body-relative direction into the grid frame, updates the position and continues from there.

Now the performer starts facing east. The same score yields one unit south and two units east, ending at (2, -1). Treating R as page-right would give a different route. If the intended task is to preserve the original grid-space path regardless of orientation, choose a grid-relative notation or construct the appropriate body-relative instructions; keeping the marks unchanged does not meet that new task.

The score leaves the speed and path within each displacement unspecified. It can guide a prepared person moving a token. Making a physical robot perform it additionally requires an applicable motion method and an account of its realization. Reading the endpoint establishes neither that method nor a performed movement.

## NOT.8:6 - Bias-Annotation {#bias-annotation}

Expert fluency can conceal the reading procedure. A musician or dancer may supply pulse, segmentation and bodily realization without noticing those contributions. Recover them before expecting a newcomer or computational agent to use the same expression.

A familiar carrier can also invite the wrong relation. Spoken order can be mistaken for event order, silence for a rest and a facing gesture for a room-fixed direction. Use a consequential contrast to determine which reference the notation supplies.

## NOT.8:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| Providing a list of sounds or gestures without their temporal or spatial reference | Establish the beat, origin, participant or frame needed to interpret occurrences. |
| Equating recording silence with a specified rest | Preserve the observation gap and request the missing contribution only if the use needs it. |
| Reading body-right as page-right | Recover the frame and transform directions, as in :5.2. |
| Counting correct sign recognition as successful enactment | Connect the decoded result to a capability or control method that can realize it. |
| Claiming original-speed competence from slowed replay | Limit replay to the property it preserves; inspect performance under the required timing when that claim matters. |
| Giving every score maximal movement detail | Express the constraints the receiving use consumes and retain the performer choices compatible with those constraints. |

## NOT.8:10 - Architectural Rationale {#architectural-rationale}

Temporal or embodied expression adds reference and availability problems to ordinary formation and interpretation. What a sign means can depend on phase, orientation or the reader's retained state. These conditions belong in the operative convention rather than an assumed resemblance between mark and action.

Segmentation serves the receiving operation. An action can be described by its intended result, selected intermediate constraints or a detailed movement account. Those descriptions require different contributions from a performer. Keeping that distinction permits transfer between people and machines while exposing what must be reconstructed.

Reading and enactment are connected methods. Their separation makes the connection constructive: decode what the score requires, determine what the performer must supply, obtain that method and interpret the resulting action. This retains the relation between mathematical structure, algorithms and physical realization.

## NOT.8:11 - SoTA-Echoing {#sota-echoing}

| Source and contribution | Adoption and limit |
| --- | --- |
| Nelson, [Solkattu Manual](https://www.weslpress.org/9780819574480/solkattu-manual/), Introduction, pp. 2–3 | The account connects spoken patterns with recurring hand references and distinguishes spoken from played realization. It informs :4.2 and :4.4. The book explicitly resists a simple one-syllable/one-stroke identification; the method keeps the actual convention and training contribution. |
| [Takadimi Basics](https://www.takadimi.net/basics.html) and [Teaching with Takadimi](https://www.takadimi.net/teachingWithTakadimi.html) | The position-based syllable convention supplies :5.1; coordinated pulse and voice illustrate a reading procedure. This is a particular convention, distinct from Nelson's treatment, not a general theory or an empirical guarantee of instruction quality. |
| Salaris, Abe and Laumond, [A Worked-Out Experience in Programming Humanoid Robots via the Kinetography Laban](https://doi.org/10.1007/978-3-319-25739-6_16), 2016, §1 and pp. 346–348 | The worked connection distinguishes a score's action constraints from detailed human or robot motion and exposes the control-space contribution. Adapt that distinction in :4.3–.5. The earlier robotic demonstration supplies a constructive anchor, not a claim that any score automatically yields feasible robot motion. |
| Guerreiro, Amaral and Goulão, [Unleashing the Power of Sound](https://arxiv.org/abs/2304.08654), 2023, §§III and VI.D–E | Adopt the question of audible discrimination and context into :4.3. The UML sound study measures bounded preferences and perceived relevance, with limitations in baseline choice, sample and setting; it does not establish general comprehension, multi-representation integration or universal sound meanings. |

**Choosing a form for the same operation.** In :5.1 the reader must locate and shift two onsets within a beat. Compare a static position grid with a sounded score, for a reader who knows the syllables and can count the four positions. The grid already answers the question and remains available for inspection. Keep it when that is the whole task; adding voiced practice would cost effort without improving this answer. A familiar convention also needs no extra account when its references and reading operations are already available to the reader.

For following the onsets during a performance, both a retained grid and a sounded score still need a way to keep place in the beat. Here we adapt Nelson's recurring reference and Takadimi's positional reading into :4.2 and :4.4: maintain the reference, locate each occurrence and retain or replay the parts needed for the next operation. This repairs the case in which a sign legend identifies syllables but leaves their positions unavailable. It does not require a new symbol vocabulary. A prepared reader may maintain the reference while reading the grid; a sounded or embodied form is preferable only when its coordination benefit warrants the added perception or practice. Those costs are the accepted trade-off, not a demonstrated general learning advantage.

The beat calculation in :5.1 shows the information gained from the reference; it does not compare human performance speeds. The source table supplies the limits of transferring this reasoning to movement and audible interfaces: a recovered instruction still needs its performer method, and preferred sounds need not improve interpretation. Reopen this choice if a simpler available convention supports the same operation and timing with less burden, or if the chosen reference or reading procedure fails under the receiving conditions.

The synthesis uses these different practices to expose recurring design operations; it does not merge their symbol systems. A position syllable, a stroke-associated syllable and a motion sign can carry different relations. Reopen the construction when a relevant contrast is not perceptible, a reader lacks an assumed operation, a new realization cannot supply the omitted work or a receiving use needs a previously unexpressed relation.


## NOT.8:End {#end}

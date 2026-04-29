# Design Principles

This set treats each character as a Yu-Gi-Oh-style archetype inside Universus. A character package should provide about 75% of a viable deck: a primary engine, a win condition, some protection, and a few interaction points. The remaining 25% should come from neutral cards, Stage cards, or cross-archetype symbol overlap.

## Core Rules

- The house-rule symbol system allows a card to be played if it shares any symbol with the last played card. The main or picked symbol does not matter.
- Most cards should have 1 symbol. Some can have 2 symbols. Three-symbol cards should be rare finishers, boss cards, or major bridge cards.
- Foundations should have 1 effect only.
- A Foundation may have a second effect only if that second effect is character-restricted.
- A Foundation should have one tactical role: foundation control, speed buff, damage reduction, draw, filtering, momentum gain, block quality, or protection. Do not mix roles on one Foundation.
- Effects should not be plain numerical buffs. Every effect should care about a tag, keyword, Stage, character, or archetype condition.
- Buffs like `+1 damage`, `+1 speed`, draw, readying, and damage reduction should create deck-building incentives by naming a hook such as `Punch`, `Throw`, `Flame`, `Assassin`, `Tactics`, `Stage`, or `Lucha`.
- If a buff is narrowly scoped to a tag, keyword, or type, it should usually be above-rate compared to a generic effect.
- Foundation-control effects should usually be open effects. Character restrictions should mostly live on powerful buffs, signature engines, or defining finishers.
- When a Foundation has both open foundation control and a character-restricted effect, the character line should sharpen identity without making the control text inaccessible to the archetype shell.

## Metagame Assumptions

Universus should not be designed as if it is only an attack back-and-forth game. Like Yu-Gi-Oh, where the monster combat fantasy often gives way to effects, hand traps, and negation, Universus is largely a game of effects and foundation control.

Foundation flood is a core pressure point. A player can realistically build toward 20 foundations, and multiple foundation types can create cognitive load, excessive board tracking, and choice paralysis. Set design must actively resist this.

- Every archetype should have access to foundation control, such as committing, flipping, sealing, or destroying foundations.
- Most foundations and many effects should interact with foundations directly. Foundation control is not a side package; it is the main board-management layer of the set.
- Every archetype must have access to real foundation removal, whether it removes its own foundations or the rival's foundations.
- Temporary control such as committing, flipping, and sealing is useful, but it does not replace removal because it does not reduce board size.
- Removal should vary by archetype: destroying, removing from the game, Burying, bouncing to hand, Priming, or cashing in your own foundations all create different risks and advantages.
- Destroying can trigger beneficial effects for the opponent. Burying denies death triggers but is less final than removing from the game. Bouncing can protect your own pieces or tax the rival's next turn. Priming is strong tempo but can give the opponent a known redraw. Removing from the game is cleanest and should be the rarest.
- Foundation control can still be tagged and role-bound. A card should answer specific board texture, not become universal generic removal.
- The target game length is 4 turns total, or about 2 turns per player. If games regularly go longer, foundation flood becomes more likely.
- Damage output must be high enough for decks to threaten lethal within that 4-turn window.
- Defensive tools should buy a turn or force sequencing decisions, not indefinitely protect a 15-20 foundation board.

## Combat Profile Matchups

The character packages should have soft rock-paper-scissors pressure through attack zones, block zones, and speed.

- A high-block profile should be pressured by low-heavy attack profiles.
- A low-block profile should be pressured by high-heavy attack profiles.
- A mid-block profile should be pressured by higher average speed, because mid blocks are easiest to over-rely on.
- K-Dash uses low Flame routes to punish high-block profiles.
- Vanessa uses high average speed to punish mid-block profiles.
- Ramon uses high-zone Throw attacks to punish low-block profiles.
- Lin uses low-zone Assassin attacks to punish high-block profiles while forcing poison inevitability.
- Seth has the strongest block modifiers, but his mid-block profile is pressured by fast decks and repeated foundation movement.

## Matchup Construction Method

Matchups should be created through measurable combat profiles, not only through explicit silver-bullet card text. Each character file should track:

- Attack-zone distribution: High, Mid, and Low percentages among that character's attacks.
- Average attack speed.
- Block-zone distribution: High, Mid, and Low percentages among that character's attack blocks.
- Average block modifier.
- A short matchup-pressure note explaining what the profile pressures and what pressures it back.

When adding or changing attacks, recalculate the profile and check the intended soft counter map:

- Low-heavy attack profiles should pressure high-block profiles.
- High-heavy attack profiles should pressure low-block profiles.
- High-speed profiles should pressure mid-block profiles.
- Strong block modifiers should stabilize a character, but not remove their exploitable zone weakness.
- Foundation-control texture should reinforce the matchup profile instead of overriding it.

This set's current matchup map is documented in `matchup.md`. If a future change moves a character's zone count by more than 1 attack, changes average speed by 0.50 or more, or changes average block modifier by 0.50 or more, update both that character's `Combat Profile` and `matchup.md`.

## Type, Tag, Keyword Model

- `Type` is the main card type: Character, Attack, Foundation, Asset, Action, or Stage.
- `Tags` hold the card's mechanical identity and flavor identity together. Use at most 2 tags per card.
- `Keywords` is a separate field for printed keyword text such as `Combo(Flame)`, `Reversal`, `Throw`, `Multiple: 1`, or `Powerful: 2`.
- Tags and Keywords exist to make archetypes readable and to keep simple effects flavorful. A card that says `Your Punch attack gets +1 speed` is preferable to `Your attack gets +1 speed`.
- Tags can support both flavor and mechanics. `Flame` makes K-Dash feel different from generic Fire-symbol cards; `Boxing` makes Vanessa's speed buffs narrower than generic Aerial support.
- Tags should stay generic. Do not use character names, organization names, or stage proper nouns in Tags.

## Archetype Identities

- K-Dash is a `Combo(Flame)` momentum deck. His best turns chain Flame cards, build momentum, and spend it on Combo payoffs.
- Vanessa is a `Punch` and `Boxing` speed deck. She wins by making small attacks hard to block and converting speed thresholds into damage.
- Ramon is a `Throw`, `Lucha`, and `Freestyle` deck. He pressures blocking decisions and uses throw damage to stay relevant through defense.
- Lin is an `Assassin` and `Poison` deck. He creates poison counters, taxes resources, and turns poison into inevitability.
- Seth is a `Tactics`, `Agent`, `Block`, and `Reversal` deck. He blocks efficiently, then converts defense into Reversal attacks.
- Neutral cards should not erase archetype weaknesses. They should bridge symbols, help other symbol packages play together, reward Stage play, or provide narrow answers tied to Tags and Keywords.
- Neutral foundations should commonly have 2 symbols so they can serve as practical bridge cards without becoming universal auto-includes.
- Exceptional neutral cards can have 3 symbols when their role is reliable smoothing. Stage cards are the main example because they are meant to keep the house-rule symbol chain moving.

## Stage Cards

Stage cards represent the unique battlefields of KOF 2000. They use a special Stage field.

Only one Stage can be in the Stage field at a time. When a new Stage is played, discard the current Stage first, then place the new Stage in the Stage field.

Stages should affect both players when possible, but their hooks should favor specific decks or punish specific patterns. For example, Factory supports `Tech` keyword attacks, while Aquarium checks speed-heavy decks.

Stage cards should have exactly 3 symbols. Under the house-rule symbol chaining system, they are intended to be reliable smoothers that help decks pivot between archetype cards and neutral cards.

Stage cards are among the few cards types that can have 2 effects universally, since their state is checked by both players. Each Stage should have one controller-only effect and one public effect that either player can use.

Stage control should matter. Neutral cards may allow a player to become the controller of the current Stage, but those cards should also carry a broadly useful effect so they are not dead when Stage control is not contested.

## Balance Targets

- Each character should have a clear win condition but not access to every effect category.
- Each archetype should have at least one form of protection or interaction, but not universal answers.
- Each archetype should include multiple proactive answers to foundation flood, including at least one effect that actually removes a foundation from the staging area.
- Draw and ready effects should be narrow and tagged because they are high-leverage in Universus.
- Damage reduction should specify what kind of attack it answers.
- Damage and speed buffs should specify what kind of attack they support.
- Three-symbol cards should be strong but narrow enough that they do not become generic staples.

## Design tidbits

- Effects that destroy the foundation should be showed and playable *after* other effects that need the foundation present.
- Void has access to bottom-draw, to protect from and counter put-in-bottom removals.
- Tags allow for viable blank/vanilla through effects that look for them and/or enhance them. They become a shell that can house powerful effects while being simple and available.
- Attacks with strong effects should tend to have Mid zone.
- Attacks with Low zone should tend toward "If this attack deals damage..." effects
- Attacks with High zone should tend toward High damage and Keywords.

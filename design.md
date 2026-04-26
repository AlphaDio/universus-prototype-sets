# Design Principles

This set treats each character as a Yu-Gi-Oh-style archetype inside Universus. A character package should provide about 75% of a viable deck: a primary engine, a win condition, some protection, and a few interaction points. The remaining 25% should come from neutral cards, Stage cards, or cross-archetype symbol overlap.

## Core Rules

- The house-rule symbol system allows a card to be played if it shares any symbol with the last played card. The main or picked symbol does not matter.
- Most cards should have 1 symbol. Some can have 2 symbols. Three-symbol cards should be rare finishers, boss cards, or major bridge cards.
- Foundations should have 1 effect only.
- A Foundation may have a second effect only if that second effect is character-restricted.
- A Foundation should have one tactical role: speed buff, damage reduction, draw, filtering, momentum gain, block quality, or protection. Do not mix roles on one Foundation.
- Effects should not be plain numerical buffs. Every effect should care about a tag, keyword, Stage, character, or archetype condition.
- Buffs like `+1 damage`, `+1 speed`, draw, readying, and damage reduction should create deck-building incentives by naming a hook such as `Punch`, `Throw`, `Flame`, `Assassin`, `Tactics`, `Stage`, or `Lucha`.
- If a buff is narrowly scoped to a tag, keyword, or type, it should usually be above-rate compared to a generic effect.

## Metagame Assumptions

Universus should not be designed as if it is only an attack back-and-forth game. Like Yu-Gi-Oh, where the monster combat fantasy often gives way to effects, hand traps, and negation, Universus is largely a game of effects and foundation control.

Foundation flood is a core pressure point. A player can realistically build toward 20 foundations, and multiple foundation types can create cognitive load, excessive board tracking, and choice paralysis. Set design must actively resist this.

- Every archetype should have access to foundation control, such as committing, flipping, sealing, or destroying foundations.
- Foundation control should be present on character cards, attacks, foundations, or neutral cards so no deck has to ignore foundation spam.
- Foundation control should still be tagged and role-bound. A card should answer specific board texture, not become universal generic removal.
- The target game length is 4 turns total, or about 2 turns per player. If games regularly go longer, foundation flood becomes more likely.
- Damage output must be high enough for decks to threaten lethal within that 4-turn window.
- Defensive tools should buy a turn or force sequencing decisions, not indefinitely protect a 15-20 foundation board.

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
- Neutral cards should not erase archetype weaknesses. They should bridge symbols, reward Stage play, or provide narrow answers tied to Tags and Keywords.

## Stage Cards

Stage cards represent the unique battlefields of KOF 2000. They use a special Stage field.

Only one Stage can be in the Stage field at a time. When a new Stage is played, discard the current Stage first, then place the new Stage in the Stage field.

Stages should affect both players when possible, but their hooks should favor specific decks or punish specific patterns. For example, Factory supports `Tech` keyword attacks, while Aquarium checks speed-heavy decks.

Stage cards are among the few cards types that can have 2 effects universally, since their state is checked by both players. One effect can be played only by the controller of the card, and the other can be played by both players.

## Balance Targets

- Each character should have a clear win condition but not access to every effect category.
- Each archetype should have at least one form of protection or interaction, but not universal answers.
- Each archetype should include at least one proactive answer to foundation flood.
- Draw and ready effects should be narrow and tagged because they are high-leverage in Universus.
- Damage reduction should specify what kind of attack it answers.
- Damage and speed buffs should specify what kind of attack they support.
- Three-symbol cards should be strong but narrow enough that they do not become generic staples.

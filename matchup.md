# Matchup Profile

This file documents the soft rock-paper-scissors layer between the five character archetypes. The goal is not hard counterpicks, but clear matchup pressure created by attack zones, block zones, speed profiles, and foundation-control texture.

## Design Logic

- High-block profiles are pressured by low-heavy attack profiles.
- Low-block profiles are pressured by high-heavy attack profiles.
- Mid-block profiles are pressured by higher average speed, because mid blocks are easiest to over-rely on.
- Strong block modifiers can stabilize a deck, but they should be challenged by speed, block-tax effects, and repeated foundation movement.
- Zone pressure is only one layer. Foundation removal style, card speed, throw pressure, poison inevitability, and character-restricted finishers should still matter.

## Combat Profiles

| Character | Attack Zones | Avg Speed | Block Zones | Avg Block Mod | Pressure Identity |
| --- | --- | ---: | --- | ---: | --- |
| K-Dash | High 28.6%, Mid 14.3%, Low 57.1% | 4.00 | High 57.1%, Mid 14.3%, Low 28.6% | +2.57 | Low-heavy Flame pressure |
| Vanessa | High 33.3%, Mid 50.0%, Low 16.7% | 4.83 | High 16.7%, Mid 66.7%, Low 16.7% | +2.33 | Fast Boxing pressure |
| Ramon | High 50.0%, Mid 33.3%, Low 16.7% | 2.67 | High 33.3%, Mid 0.0%, Low 66.7% | +2.33 | High-zone Throw pressure |
| Lin | High 0.0%, Mid 33.3%, Low 66.7% | 4.33 | High 0.0%, Mid 33.3%, Low 66.7% | +2.50 | Low-zone Assassin pressure |
| Seth | High 33.3%, Mid 50.0%, Low 16.7% | 3.83 | High 33.3%, Mid 66.7%, Low 0.0% | +1.33 | Efficient defensive Reversal pressure |

## Soft Counter Map

| Attacker | Pressures | Why |
| --- | --- | --- |
| K-Dash | K-Dash, high-block shells | Low-heavy attack profile punishes decks leaning on High blocks. His Combo(Flame) pressure can also force awkward blocks before momentum finishers. |
| Vanessa | Vanessa, Seth, mid-block shells | Highest average speed in the set makes Mid-heavy block profiles less reliable. Her bounce/Prime foundation control also pressures defensive boards. |
| Ramon | Ramon, Lin, low-block shells | High-zone Throw profile pressures decks leaning on Low blocks. Throws also keep damage moving through partial blocks. |
| Lin | K-Dash, high-block shells | Low-heavy Assassin profile pressures High blocks, while poison punishes slow defensive games. |
| Seth | Balanced or slower attack suites | Low average block modifier and Reversal access let Seth stabilize against ordinary attacks, but he is not meant to hard-counter speed decks. |

## Vulnerability Map

| Defender | Vulnerable To | Why |
| --- | --- | --- |
| K-Dash | Low-heavy attackers, especially Lin | K-Dash has a High-heavy block profile, so repeated Low attacks stress his blocks. |
| Vanessa | Faster attacks and block-tax effects | Vanessa leans heavily on Mid blocks and has only average block modifiers. |
| Ramon | High-heavy attackers, especially Ramon mirrors | Ramon has a Low-heavy block profile and no Mid blocks in his attack suite. |
| Lin | High-heavy attackers, especially Ramon | Lin has no High blocks in his attack suite and leans Low on defense. |
| Seth | High-speed pressure, especially Vanessa | Seth blocks efficiently, but his Mid-heavy profile is vulnerable to decks that push speed above normal block math. |

## Foundation-Control Texture

| Character | Primary Foundation-Control Style | Matchup Implication |
| --- | --- | --- |
| K-Dash | Self-foundation destruction, rival destruction, remove from game | Converts his own board into damage and momentum, then removes key committed foundations cleanly. |
| Vanessa | Bounce and Prime | Uses speed pressure to make the rival replay or redraw foundations instead of stabilizing. |
| Ramon | Bury and self-recycling | Denies destruction triggers and keeps throw pressure from feeding foundation flood. |
| Lin | Destruction and remove from game | Punishes poison victims by converting inevitability into real board loss. |
| Seth | Prime, bounce, and remove from game | Controls the rival's next draw and keeps Reversal turns from being overwhelmed by foundation boards. |

## Design Checkpoints

- Every character should have a visible attacking pressure profile.
- Every character should have an exploitable defensive profile.
- No profile should be purely symmetrical unless the archetype has another strong axis of differentiation.
- Foundation control should amplify the matchup texture instead of erasing it.
- If future cards shift a zone distribution by more than 1 attack, recalculate this file and the character file's `Combat Profile`.

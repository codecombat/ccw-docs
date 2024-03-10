# Battler Stats

## Description

Battlers are the pets and monsters in CodeCombat Worlds. Each battler has its own unique set of stats and abilities. These stats and abilities are used to determine the outcome of battles and other interactions in the game.

## Primary Stats

The primary stats of a battler are:
- `STR` - Strength, which determines the damage dealt by the battler's attack abilities.
- `AGI` - Agility, which determines the battler's movement speed and attack speed.
- `END` - Endurance, which determines the battler's health and resistance to damage.

## Secondary Stats

- `BASE_DAMAGE` - the base damage of an attack ability. This is scaled with the battler's strength. The formula for calculating the damage of an attack ability is `SUM((STR - S) for S in RANGE(0, STR, 10))`.
- `BASE_ATTACK_DURATION` - the base duration of an attack ability. This is scaled with the battler's agility. The formula for calculating the duration of an attack ability is `MAX(0.5, 2 - (AGI - 10) / 40)`.
- `BASE_HEALTH` - the base/max health of a battler. This is scaled with the battler's endurance. The formula for calculating the health of a battler is  `IF END < 10 then END * 10 ELSE (END - 10) * 20 + 100`.
- `MOVE_SPEED` - the movement speed of a battler. This is scaled with the battler's agility. The formula for calculating the movement speed of a battler is `20 + (AGI - 10) / 2`.
(battle_abilities)=
# Battle Abilities

Battle abilities are special moves that pets can use in combat. Pets get new abilities with levels. You can see the list of abilities in the pet's description. To use an ability, you need to use a certain method in your pet's program. The method's name is the same as the ability's name. For example, if your pet has an ability called "bite", you can use it by calling `pet:bite(target)` in your pet's program and use `"bite"` to check if the ability is ready to use.

Abilities have duration, damage delivered delay, and cooldown. Ability parameters depends on the pet's stats and perks. You can read more about pets in the [Pets List](pet_list).

# Stats

Attack abilities are scaled with the pet's Primary and Secondary stats. You can read more about stats in the *Stats Section (TBA)*

- `STR` - Strength
- `AGI` - Agility
- `END` - Endurance
- `BASE_DAMAGE` - the base damage of an attack ability
- `BASE_ATTACK_DURATION` - the base duration of an attack ability
- `BASE_HEALTH` - the base/max health of a pet

## `hit`

**The basic attack ability. The pet attacks a single target.**

````{card} **Stats:**
- <font color='red'>Damage: `BASE_DAMAGE`</font>
- <font color='blue'>Cooldown: 0s</font>
- <font color='green'>Duration: `BASE_ATTACK_DURATION`</font>
- Range: Individually defined for each pet
````

## `spin`

**The pet spins around, dealing damage to all nearby enemies.**

````{card} **Stats:**
- <font color='red'>Damage: `BASE_DAMAGE / 2`</font>
- <font color='blue'>Cooldown: `0` s</font>
- <font color='green'>Duration: `BASE_ATTACK_DURATION` </font>
- Range: `12` studs
````

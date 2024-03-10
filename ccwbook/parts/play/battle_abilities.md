(battle_abilities)=
# Battle Abilities

Battle abilities are special moves that pets can use in combat. Pets get new abilities with levels. You can see the list of abilities in the pet's description. To use an ability, you need to use a certain method in your pet's program. The method's name is the same as the ability's name. For example, if your pet has an ability called "bite", you can use it by calling `pet:bite(target)` in your pet's program and use `"bite"` to check if the ability is ready to use.

Abilities have duration, damage delivered delay, and cooldown. Ability parameters depends on the pet's stats and perks. You can read more about pets in the [Pets List](pet_list).

### Stats

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
- **Damage:** `BASE_DAMAGE`
- **Duration:** `BASE_ATTACK_DURATION`
- **Cooldown:** 0s
- **Range:** Individually defined for each pet
````

## `spin`

**The pet spins around, dealing damage to all nearby enemies.**

````{card} **Stats:**
- **Damage:** `BASE_DAMAGE / 2`
- **Duration:** `BASE_ATTACK_DURATION` 
- **Cooldown:** `0` s
- **Range:** `12` studs
````

## `bite`

**The powerful bite attack.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 3`
- **Duration:** `MAX(0.4, BASE_ATTACK_DURATION / 2)`
- **Cooldown:** `BASE_ATTACK_DURATION * 2` s
- **Range:** `4` studs
````

## `clash`

** The pet quickly attacks the target several times.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 3`
- **Cooldown:** `BASE_ATTACK_DURATION * 1.5` s
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Range:** `3` studs
````


## `slam`

**The pet slams the ground, dealing damage to all nearby enemies.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 1.25`
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `15` studs
````

## `frostBite`

**The pet bites the target, dealing damage and slowing it down.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 1.5`
- **Duration:** `MAX(0.4, BASE_ATTACK_DURATION / 2)`
- **Cooldown:** `BASE_ATTACK_DURATION * 2` s
- **Range:** `4` studs
- **Effect:** Slows down the target by `50%` for `5` s
````

## `chillClash`

**The pet quickly attacks the target several times and reduces its attack damage.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 1.8`
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `3` studs
- **Effect:** Reduces the target's attack damage by `50%` for `5` s
````

## `frostSlam`

**The pet slams the ground, dealing damage to all nearby enemies and slowing them down.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 0.75`
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `15` studs
- **Effect:** Slows down the targets by `50%` for `5` s
````

## `bash`

**The pet bashes the target, dealing damage and (TO BE DEFINED).**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 3`
- **Duration:** BASE_ATTACK_DURATION`
- **Cooldown:** `BASE_ATTACK_DURATION * 2` s
- **Range:** `4` studs
````

## `poke`

**The pet pokes the target, dealing damage and (TO BE DEFINED).**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 3`
- **Duration:** BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `6` studs
````

## `magicArrow`

**The pet shoots a magic arrow at the target, dealing damage and (TO BE DEFINED).**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 1.25`
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `30` studs
````

## `fireArrow`

**The pet shoots a fire arrow at the target, dealing fire damage.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 1.25`
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `30` studs
- **Element:** <font color='orange'>Fire
````

## `iceArrow`

**The pet shoots an ice arrow at the target, dealing ice damage.**

````{card} **Stats:**

- **Damage:** `BASE_DAMAGE * 1.25`
- **Duration:** `BASE_ATTACK_DURATION * 1.5`
- **Cooldown:** `BASE_ATTACK_DURATION * 3` s
- **Range:** `30` studs
- **Element:** <font color='blue'>Ice
````

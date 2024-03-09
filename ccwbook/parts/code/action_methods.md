(action_methods)=
# Action Methods

Action methods are used to control the pet's behavior. They are used to make the pet move, attack, and perform other actions. The main difference with other methods that actions block the pet's execution until they are finished. This means that the pet will not do anything else until the action is completed. Usually, action methods return nothing.

(hit_method)=
## `hit`

**The pet attacks a single target.**

````{card}

**Syntax:** `pet(hit)` or `pet:hit(target: AttackableObject | string)`
^^^
**Arguments:**
- `target` - the target to attack. 
    - if target is not given then pet will attack the nearest attackable object.
    - if target is a string then pet will attack the nearest attackable object with the given tag.
    - if target is a game object and its attackable then pet will attack it.
+++
**Examples:**
````{tab-set}
```{tab-item} Any enemy
```lua
-- attack the nearest attackable object
pet:hit()
```
```{tab-item} Specific enemy
```lua
-- attack the nearest slime
pet:hit("slime")
```
```{tab-item} Specific object
```lua
-- attack some specific object
local monster = pet:findNearest("monster")
if monster and monster.health > 0 then
    pet:hit(monster)
end
```
````

## `moveTo`

**The pet moves to the given target.**

````{card}

**Syntax:** `pet(target: TaggedObject | string)`
^^^
**Arguments:**
- `target` - the target to move to. 
    - if target is a string then pet will move to the nearest object with the given tag.
    - if target is a world object then pet will move to it.
+++
**Examples:**
````{tab-set}
```{tab-item} To me
```lua
-- move to the player
pet:moveTo(me)
```
```{tab-item} To the nearest monster
```lua
-- move to the nearest monster
pet:moveTo("monster")
```
```{tab-item} To specific object
```lua
local items = pet:findItems()
for _, it in items do
    if it:hasTag("gem") then
        pet:moveTo(it)
    end
end
```
````

## `grab`

**The pet grabs the given item.**

````{card}

**Syntax:** `pet:grab(target: ItemObject | string)`
^^^
**Arguments:**
- `target` - the target to grab. 
    - if target is a string then pet will grab the nearest item with the given tag.
    - if target is a world object then pet will grab it.
+++
**Examples:**
````{tab-set}
```{tab-item} Grab the nearest item
```lua
-- grab the nearest item
pet:grab()
```
```{tab-item} Grab specific item
```lua
-- grab the nearest gem
pet:grab("gem")
```
```{tab-item} Grab specific object
```lua
local items = pet:findItems()
for _, it in items do
    if it:hasTag("gem") then
        pet:grab(it)
    end
end
```
````

## `drop`

**The pet drops the item it is carrying.**

````{card}

**Syntax:** `pet:drop()`

+++
**Examples:**
```lua
pet:grab("gem")
pet:moveTo(me)
pet:drop()
```
````

## `say`

**The pet says the given message.**

````{card}

**Syntax:** `pet:say(message: string)`
^^^
**Arguments:**
- `message` - the message to say.
+++
**Examples:**
```lua
pet:say("Hello!")
```
````

(spin_method)=
## `spin`

**The pet spins around, dealing damage to all nearby enemies.**

````{card}

**Syntax:** `pet:spin()`

+++
**Examples:**
```lua
pet:moveTo("red-slime")
pet:spin()
pet:spin()
```
````


## `slam`

**The pet slams the ground, dealing damage to all nearby enemies.**

````{card}

**Syntax:** The same as [`spin`](spin_method).
````

## `frostSlam`

**The pet slams the ground, dealing damage to all nearby enemies and slowing them down.**

````{card}

**Syntax:** The same as [`spin`](spin_method).
````

## `bite`

**The powerful bite attack.**

````{card}

**Syntax:** The same as [`hit`](hit_method).
````

## `frostBite`

**The pet bites the target, dealing damage and slowing it down.**

````{card}

**Syntax:** The same as [`hit`](hit_method).
````

## `clash`

**The pet quickly attacks the target several times.**

````{card}

**Syntax:** The same as [`hit`](hit_method).
````

## `chillClash`

**The pet quickly attacks the target several times and reduces its attack damage.**

````{card}

**Syntax:** The same as [`hit`](hit_method).
````
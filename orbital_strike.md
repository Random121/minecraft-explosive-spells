## Layout:

**_Orbital Strike:_**\
(R1)(C1)(C2)(C3)(C4)(C5)\
(R2)(C6)(C7)(C8)(C9)\
(R3)(C11)(C12)(C13)(C14)(C15)(C16)(C17)(C18)(C19)(C20)

## Items:

**Note:** Item used must be a renamed "Spawn Endermite" egg

**_Orbital Strike:_** Call Orbital Strike

## Commands:

**(R1, Delay: 5):** testfor @e[type=endermite, name="Call Orbital Strike"]

**(C1):** execute @e[type=endermite, name="Call Orbital Strike"] ~ ~ ~ summon armor_stand orbitalStrikeTarget ~ ~ ~

**(C2):** execute @e[type=endermite, name="Call Orbital Strike"] ~ ~ ~ effect @e[type=armor_stand, name=orbitalStrikeTarget, r=1] invisibility 100000000 255 true

**(C3):** execute @e[type=endermite, name="Call Orbital Strike"] ~ ~ ~ effect @e[type=armor_stand, name=orbitalStrikeTarget, r=1] fire_resistance 100000000 255 true

**(C4):** execute @e[type=endermite, name="Call Orbital Strike"] ~ ~ ~ scoreboard players set @e[type=armor_stand, name=orbitalStrikeTarget, r=1, c=1] orbitalStrikeTimer 25

**(C5):** execute @e[type=armor_stand, name=orbitalStrikeTarget] ~ ~ ~ tp @e[type=endermite, name="Call Orbital Strike", r=1, c=1] ~ -100 ~
\
\
\
**(R2, Delay: 5):** testfor @e[type=armor_stand, name=orbitalStrikeTarget, scores={orbitalStrikeTimer=0..}]

**(C6):** scoreboard players remove @e[type=armor_stand, name=orbitalStrikeTarget, scores={orbitalStrikeTimer=1..}] orbitalStrikeTimer 1

**(C7):** execute @e[type=armor_stand, name=orbitalStrikeTarget] ~ ~ ~ particle minecraft:rising_border_dust_particle ~ ~ ~

**(C8, UC):** testfor @e[type=armor_stand, name=orbitalStrikeTarget, scores={orbitalStrikeTimer=0}]

**(C9):** tag @e[type=armor_stand, name=orbitalStrikeTarget, scores={orbitalStrikeTimer=0}] add orbitalStrikeActive
\
\
\
**(R3, Delay: 10):** testfor @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive]

**(C11):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon lightning_bolt ~ ~ ~

**(C12):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~5 ~ ~ minecraft:crystal_explode

**(C13):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~-5 ~ ~ minecraft:crystal_explode

**(C14):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~ ~ ~5 minecraft:crystal_explode

**(C15):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~ ~ ~-5 minecraft:crystal_explode

**(C16):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~5 ~ ~5 minecraft:crystal_explode

**(C17):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~-5 ~ ~-5 minecraft:crystal_explode

**(C18):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~5 ~ ~-5 minecraft:crystal_explode

**(C19):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~-5 ~ ~5 minecraft:crystal_explode

**(C20):** execute @e[type=armor_stand, name=orbitalStrikeTarget, tag=orbitalStrikeActive] ~ ~ ~ summon ender_crystal ~ ~ ~ minecraft:crystal_explode

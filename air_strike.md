## Layout:

**_Air Strike:_**\
(R1)(C1)(C2)(C3)(C4)(C5)(C6)(C7)(C8)(C9)(C10)(C11)(C12)

## Items:

**Note:** Item used must be a renamed "Spawn Endermite" egg

**_Air Strike:_** Call Airstrike

## Commands:

**(R1, Delay: 2):** testfor @e[type=item, name="Call Airstrike"]

**(C1):** execute @e[type=item, name="Call Airstrike"] ~ ~ ~ tag @r[r=100, rm=3] add airStrikeTarget

**(C2):** kill @e[type=item, name="Call Airstrike"]

**(C3):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~ ~60 ~

**(C4):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~8 ~60 ~

**(C5):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~-8 ~60 ~

**(C6):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~ ~60 ~8

**(C7):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~ ~60 ~-8

**(C8):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~8 ~60 ~8

**(C9):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~-8 ~60 ~-8

**(C10):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~8 ~60 ~-8

**(C11):** execute @a[tag=airStrikeTarget] ~ ~ ~ summon tnt_minecart ~-8 ~60 ~8

**(C12):** tag @a[tag=airStrikeTarget] remove airStrikeTarget

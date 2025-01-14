# On Neighbour Update

[Mechanic Type](../mechanic_types.md).

A Mechanic that is run when this block is updated (e.g. a block being placed next to it).

Type ID: `ccpacks:on_neighbour_update`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`neighbour_action` | [Block Action Type](https://origins.readthedocs.io/en/latest/types/block_action_types/) | *optional* | The action to execute on the neighbouring block.
`neighbour_condition` | [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | The condition to checked in order to run the neighbouring block action.
`self_action` | [Block Action Type](https://origins.readthedocs.io/en/latest/types/block_action_types/) | *optional* | The action to execute on the block.
`self_condition` | [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | The condition to checked in order to run the self block action.

### Example
```json
{
	"type": "ccpacks:on_neighbour_update",
	"self_action": {
		"type": "origins:execute_command",
		"command": "summon minecraft:zombie"
	},
	"neighbour_condition": {
		"type": "origins:block",
		"block": "minecraft:diamond_block"
	}
}
```
This mechanic will summon a zombie if a diamond block is placed next to this block.
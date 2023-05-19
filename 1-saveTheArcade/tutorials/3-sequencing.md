# Sequencing

### @explicitHints 1

### @activities true

## First Activity

###  @showdialog

Let's put multiple blocks in a single chat command to complete a task that requires multiple steps.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/1-saveTheArcade/images/placeholder.gif)

### Commands with multiple steps

Run the "place" command to make the ``||agent:agent place||`` a block of redstone forward.

Place multiple blocks from the Agent category into the "run" chat command.  Navigate to the end of the path and place a block of diamond in the gap.

#### ~ tutorialhint

Use the search bar in the block drop-down menu to quickly find a specific block by name.

Try using the ``||agent:agent turn||`` block to make the agent face a different direction.

```template
player.onChat("place", function () {
    agent.setItem(REDSTONE_BLOCK, 1, 1)
    agent.place(FORWARD)
})
player.onChat("run", function () {
    
})
```

```ghost
player.onChat("run", function () {
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
    agent.destroy(FORWARD)
    agent.turn(TurnDirection.Left)
})
```

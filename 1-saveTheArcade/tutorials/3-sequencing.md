# Sequencing

### @explicitHints 1

### @activities true

## First Activity

### Agent place @showdialog

Event blocks can hold multiple statement blocks to run a sequence of actions.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Agent place

Sometimes multiple statement blocks are needed to complete a task.  For example, it is necessary to put a Minecraft block in the agent's inventory before the agent can place it.

Send the "place" command in chat to make the ``||agent:agent place||`` a **Block of Redstone** forward.  

#### ~ tutorialhint

The ``||agent:agent set block or item||`` block in the provided code will put one *Block of Redstone* in the agent's first inventory slot.

The agent places blocks from its first inventory slot by default.

### Multiple steps @showdialog

Let's put multiple blocks in a single chat command to complete a task that requires multiple steps.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Multiple steps

Add a sequence of ``||agent:agent||`` blocks to the **"run"** chat command to complete the task.

Navigate the agent to the **dirt block**, destroy it, place a **Block of Redstone**, then interact with the lever to turn it on.

#### ~ tutorialhint

Try using an ``||agent:agent turn||`` block to change which direction the agent is facing.

Use the Search bar to quickly find a specific Minecraft block in the drop-down menu.

### Review

When working with multiple statement blocks, it is important to put them in the proper order.  

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

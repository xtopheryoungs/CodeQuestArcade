# Sequencing

### @explicitHints 1

### @activities true

## First Activity

### Agent place @showdialog

Event blocks can hold multiple statement blocks to run a sequence of actions.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Agent place

Before making the agent place a block, we need to put a block in the agent's inventory.

The ``||agent:agent set block or item||`` block in the provided code will put one **Block of Redstone** in the agent's first inventory slot.

#### ~ tutorialhint

Send the "place" command in chat to run the code to make the ``||agent:agent place||`` a Block of Redstone forward.

### Multiple steps @showdialog

Let's put multiple blocks in a single chat command to complete a task that requires multiple steps.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Multiple steps

Add a sequence of ``||agent:agent||`` blocks to solve the challenge.  Remember, the directions in the drop-down menu are interpreted from the agent's point of view.

Navigate the agent to the **dirt block**, destroy it, and place a **Block of Redstone**.

#### ~ tutorialhint

Try using an ``||agent:agent turn||`` block to change which direction the agent is facing.

Use the Search bar to quickly find a Minecraft block in the drop-down menu.

### Review

The ``||agent:agent set block or item||`` puts something in the agent's inventory, and ``||agent:agent place||`` makes the agent place a block or item from its inventory (default slot = 1).

Code is a sequence of steps being executed in order.  


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

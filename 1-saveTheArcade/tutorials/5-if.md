# If Statements

### @explicitHints 1

### @activities true

## First Activity

### @showdialog

Let's use an if block so the agent can decide whether to perform a section of code.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Making choices

Run the "cleanup" chat command to make the agent get rid of only the blocks.

Add to the "run" chat command to get rid of each slime block without breaking any of the torches.

Use the ``||agent:agent detect||`` **condition block** to check ``||logic:if||`` there is a solid Minecraft block next to the agent.  The ideal solution will also work for clearing the honey blocks without breaking any levers.

#### ~ tutorialhint

The ``||agent:agent detect||`` block lets the agent know whether there is a solid block.  Smaller items such as torches, levers, and buttons do not get detected since the agent can move through them.

```template
player.onChat("cleanup", function () {
    for (let index = 0; index < 4; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.turn(LEFT_TURN)
    }
})
player.onChat("run", function () {
    for (let index = 0; index < 10; index++) {
    	
    }
})
```

```ghost
player.onChat("jump", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
        agent.interact(FORWARD)
        agent.destroy(FORWARD)
        agent.setItem(GRASS, 1, 1)
        agent.place(FORWARD)
    }
})
```

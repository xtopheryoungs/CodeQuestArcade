# While Loops

### @explicitHints 1

### @activities true

## First Activity

### @showdialog

Let's use a while loop so the agent can decide whether to keep performing a section of code.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/1-saveTheArcade/images/placeholder.gif)

### Looping based on a choice

Run the "cleanup" chat command to make the agent move forward an uncertain distance based on its surroundings and then activate a lever.

Add to the "run" chat command to make whatever happen.

Use the ``||agent:agent inspect||`` **value block** to make a ``||logic:comparison||`` with a Minecraft block and do other things

#### ~ tutorialhint

The ``||agent:agent inspect||`` provides information about what type of Minecraft block is next to the agent.

```template
player.onChat("run", function () {
    for (let index = 0; index < 10; index++) {
    	
    }
})
```

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 10; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.setItem(GRASS, 1, 1)
            agent.place(FORWARD)
        }
    }
    while (agent.inspect(AgentInspection.Block, FORWARD) == GRASS) {
        agent.move(FORWARD, 1)
        agent.interact(FORWARD)
        agent.destroy(FORWARD)
    }
})
```

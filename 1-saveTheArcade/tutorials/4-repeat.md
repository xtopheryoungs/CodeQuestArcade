# The Repeat Loop

### @explicitHints 1

### @activities true

## First Activity

### @showdialog

Let's use a repeat loop to run a section of code multiple times.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/1-saveTheArcade/images/placeholder.gif)

### Writing less code

Run the "cleanup" chat command to make the ``||agent:agent destroy||`` the row of dirt blocks.

Make a new ``||player:on chat command||`` event to get rid of each cobweb and replace it with a **redstone lamp**.

#### ~ tutorialhint

Use a ``||loops:repeat||`` block to reduce the amount of code to write. Specify in the ``||loops:repeat||`` block how many times to repeat the process.

Remember to use ``||agent:agent set block||`` to put something in the agent's inventory before attempting to make the ``||agent:agent place||`` a block.

```template
player.onChat("cleanup", function () {
    for (let index = 0; index < 8; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
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

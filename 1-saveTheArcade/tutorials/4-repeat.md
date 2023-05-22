# The Repeat Loop

### @explicitHints 1

### @activities true

## First Activity

### The repeat loop @showdialog

A loop runs the same section of code multiple times in succession.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Repeating actions

A repeat block is a **compound statement block** because it fits anywhere a normal statement block fits but also needs statement blocks inside it.

Run the **"repeat"** chat command to make the ``||agent:agent destroy||`` the row of cobwebs.

#### ~ tutorialhint

The number of times a repeat loop runs is determined by the number at the top of the repeat block.

### The repeat loop @showdialog

Let's use a repeat loop to build a row of blocks.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Repeating actions

Drag a ``||loops:repeat||`` block from the ``||loops:loops||`` section into the **"run"** chat command and set the number of times to repeat.

Add ``||agent:agent||`` blocks inside the ``||loops:repeat||`` block to build a row of **Redstone lamps**, then activate the lever at the end.

#### ~ tutorialhint

Remember to use ``||agent:agent set block||`` to put something in the agent's inventory before attempting to make the ``||agent:agent place||`` a block.

### The repeat loop @showdialog

Let's change our code to build a longer row

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Repeating actions

Change the number in the ``||loops:repeat||`` block to build an even longer row of **Redstone lamps**.

#### ~ tutorialhint

Be sure to get an accurate count so that the repeat loop runs the correct number of times.

### Review

Repeat blocks are useful for reducing the amount of code to write.

```template
player.onChat("repeat", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})

player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {

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

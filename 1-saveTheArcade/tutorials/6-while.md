# While loops

### @explicitHints 1

### @activities true

## First Activity

### @showdialog

A while loop keeps running as long as a condition is true

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Conditional looping

A ``||loops:while||`` loop is another type of **compound statement block** that uses a **condition** to determine whether it will continue looping.

Run the **"while"** chat command to make the agent keep moving forward one block at a time ``||loops:while||`` the ``||agent:agent inspects||`` **Obsidian** beneath it and then finally activate the lever at the end.

#### ~ tutorialhint

The ``||agent:agent inspect||`` block is a *value block* because it returns information about a Minecraft block.

### @showdialog

Let's use a while loop to perform some actions over and over without knowing how many times to repeat

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Conditional looping

A ``||loops:while||`` block is useful when it is infeasible to know how many times to run.

Add code to the **"run"** chat command to make the ``||agent:agent move||`` ``||loops:while||`` the ``||agent:agent detects||`` **Cobblestone** beneath it.

Along the way, ``||logic:if||`` the ``||agent:agent detects||`` a block on its **right**, make the ``||agent:agent place||`` a **Block of Gold** on its **left**.

#### ~ tutorialhint

Use a ``||logic:comparison||`` block from the ``||logic:Logic||`` category to establish a condition for the ``||loops:while||`` loop.  

Complete the comparison that what the ``||agent:agent inspects||`` is equal to *Cobblestone* with a ``||blocks:Minecraft block value||`` from the ``||blocks:Blocks||`` category.

### @showdialog

Let's try the same code with a different scenario

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Conditional looping

For the next problem, the agent has to perform the same task but on a much longer path.

Despite the different size, does this problem seem familiar?

#### ~ tutorialhint

The change in size has no impact on the solution since the *condition* in the *while loop* will make the agent continue until the condition is false.

A solution with a *while loop* can continue running based on a condition instead of relying on a fixed number.

### Review

``||loops:While||`` blocks make code flexible by using **conditions** to loop properly in different situations.

Flexible code with ``||loops:while||`` blocks can solve problems without knowing how many times to repeat.

```template
player.onChat("run", function () {
	
})
player.onChat("while", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == OBSIDIAN) {
        agent.move(FORWARD, 1)
    }
    agent.interact(FORWARD)
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

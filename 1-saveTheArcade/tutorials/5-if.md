# If Statements

### @explicitHints 1

### @activities true

## First Activity

### @showdialog

An if block can determine whether to run a certain section of code

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Making choices

An ``||logic:if||`` block is another type of **compound statement block** that uses a **condition** to make a decision.  If the condition is true, then the ``||logic:if||`` block runs the code inside it.

Run the **"if"** chat command to see if the agent can detect a block and destroy it.

#### ~ tutorialhint

The ``||agent:agent detect||`` block is a *condition block* because it tells if something is true or false.

### @showdialog

Let's use an if block with a repeat loop to make a series of decisions

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Making choices

A ``||loops:repeat||`` block combined with an ``||logic:if||`` block can efficiently solve a large problem even when there isn't a pattern.

Add code to the **"run"** chat command to make the ``||agent:agent destroy||`` only ``||logic:if||`` the  ``||agent:agent detects||`` a block.  The ``||loops:repeat||`` block is already set to repeat the correct number of times.

#### ~ tutorialhint

The ``||agent:agent detect||`` block returns *true* if there is a solid Minecraft block.  

It returns *false* for items such as torches, levers, and buttons that the agent can walk through.

### @showdialog

Let's try the same code with a different scenario

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Making choices

For the next problem, make the agent break only the **Honey Blocks**, not the **Levers**.

Despite the different blocks being used and their different arrangement, does this problem seem familiar?

#### ~ tutorialhint

The change from *Slime Blocks* to *Honey Blocks* and a different layout have no impact on the solution.

A single solution with *if statements* can solve multiple problems with superficial differences.

### Review

``||logic:If||`` blocks make code flexible by using **conditions** to properly react to different situations.

Flexible code with ``||logic:if||`` blocks can solve problems that look different but share the same general idea.

The ``||logic:if/else||`` block will be covered in a future lesson.

```template
player.onChat("if", function () {
    if (agent.detect(AgentDetection.Block, LEFT)) {
        agent.destroy(LEFT)
    }
    if (agent.detect(AgentDetection.Block, RIGHT)) {
        agent.destroy(RIGHT)
    }
})
player.onChat("run", function () {
	for (let index = 0; index < 25; index++) {

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

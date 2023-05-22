# Events

### @explicitHints 1

### @activities true

## First Activity

### Agent move @showdialog

Let's use an "on chat command" event block to move the agent.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Agent move

To run the code provided in the **"move"** chat command, first press the Play button to close Code Builder. 

Then press **T** to open the Minecraft chat window.  In the chat window, send the message **"move"**.

#### ~ tutorialhint

Click the Next button to move on to the next coding task.

### Agent interact @showdialog

Let's use another "on chat command" event block to make the agent interact with a lever.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Agent interact

Click the ``||agent:agent||`` button to open the ``||agent:agent||`` category.

Drag an ``||agent:agent interact||`` block into the **"interact"** chat command and set the direction in the drop-down menu to **back**.

#### ~ tutorialhint

Run your code by sending the command "interact" in the Minecraft chat window.

### Agent destroy @showdialog

Let's use one more "on chat command" event block to make the agent destroy a block.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Agent destroy

Drag a new ``||player:on chat command||`` block from the Player category into the workspace, and name it **"destroy"**.

Add an ``||agent:agent destroy||`` block to the **"destroy"** chat command with the direction set to **right**.

#### ~ tutorialhint

Chat commands need to have different names.  Any chat command with a duplicate name will be disabled.

### Review

Chat commands allow you to control when to run your code. 

The agent can move, interact, and destroy in six different directions.

```template
player.onChat("interact", function () {
	
})
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```

```ghost
player.onChat("move", function () {
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
    agent.destroy(FORWARD)
})
```

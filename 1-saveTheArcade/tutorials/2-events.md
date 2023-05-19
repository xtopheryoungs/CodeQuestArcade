# Events

### @explicitHints 1

### @activities true

## First Activity

###  @showdialog

Let's use "on chat command" event blocks to run different commands.

![](https://raw.githubusercontent.com/xtopheryoungs/mceduCodeQuest/main/1-saveTheArcade/images/placeholder.gif)

### Adding blocks to the workspace

Alter the code in the "move" chat command to move the agent **3** spaces forward.

Drag an ``||agent:agent interact||`` block from the Agent category into the "interact" chat command and set the direction to **back**.

Drag an ``||player:on chat command||`` block from the Player category into the workspace, name it "destroy" and add an ``||agent:agent destroy||`` block with the direction set to **right**.

#### ~ tutorialhint

Press the Play button to close the Code Builder window, then press T to open the chat.  Send a command name to run the code for that command.

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

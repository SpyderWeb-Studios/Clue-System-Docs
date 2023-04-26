# Quick Setup Guide

After you have finished the [installation process](/Getting%20Started/Installation) you should be ready
to get started.

## Clue Config Data Asset

These data assets is how you will define each Branch in the clue tree, for example: 
```
Root
|
|-> Location 1
   |-> Location 1.1
   |-> Location 1.2
|
|-> Location 2
   |-> Location 2.1 

```
Within each of these Branches, you can place in which Clues can be found in each one. The [Clue Manager Subsystem](/Documentation/C++/ClueSystem/Subsystems/ClueManagerSubsystem) will generate a dictionary, that will map each node to create a tree to represent the entire structure. We are working on making this more dynamic, so it can be changed at runtime and more procedural. 


## Clue Setup Component

The first thing you should be adding is the [Clue Setup Component](/Documentation/C++/ClueSystem/Components/ClueSetupComponent).

This component is where you are going to be telling the [Clue Manager Subsystem](/Documentation/C++/ClueSystem/Subsystems/ClueManagerSubsystem) how many clues it is expecting to exist in the world and which clue is going to be in which slot in the UI. It will do this by assigning a Root Node in the Details panel.

![image](https://imgur.com/dMyXLjg.png)

## Clue Type Data Assets

These are the Base Data Assets for each Clue in your game. They provide a common interface for you to create any type of clue that you may want. The plugin comes with [Mesh](/docs/Documentation/Content/Clue%20Types/ClueTypeMesh.md) and [Image](/docs/Documentation/Content/Clue%20Types/ClueTypeImage.md) Types by default, but using this system you can create any type that you may need for your projects. You just need to create a Widget that implements the [IClueSystemUI_Interface](/docs/Documentation/C%2B%2B/ClueSystem/Interfaces/IClueSystemUI_Interface.md) and assign it as the Clue Widget Class. 

## Clue Actor

To setup the Clues in the Level, all that is required is to drag out an instance of the class from the plugin content folder. Then assign a Data Asset for the Clue to use.

To interact with a clue and attempt to pick it up, some setup is required but not much. We have created a single function that will handle all the backend stuff, you just need to worry about how you want to call the function ```Attempt Interaction With Clue```. 

![image]("https://imgur.com/INkQ2lU.png")

This can be called via an interface call or just directly called, the choice is up to you. We didn't want to implement an interaction interface for you, as many of you who have got this plugin will likely have your own. This is designed to easily slot into as many different workflows and projects as possible.

[Creating Interfaces](https://docs.unrealengine.com/4.26/en-US/ProgrammingAndScripting/Blueprints/UserGuide/Types/Interface/)
[Using Interfaces](https://cghero.com/tutorials/blueprint-interfaces-unreal-engine-5)
[Unreal Wiki - Interfaces](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/interfaces-in-c++)


# Quick Setup Guide

After you have finished the [installation process](/Getting%20Started/Installation) you should be ready
to get started.

## Clue Setup Component

The first thing you should be adding is the [Clue Setup Component](/Documentation/C++/ClueSystem/Components/ClueSetupComponent).

This component is where you are going to define where each clue is going to be categorised, as
well as telling the [Clue Manager Subsystem](/Documentation/C++/ClueSystem/Subsystems/ClueManagerSubsystem) how many clues it is 
expecting to exist in the world and which clue is going to be in which slot in the UI. Because of this important
behaviour, **this component needs to exist in the world**.

This is where you configure the Clues. In the Details Panel, you can see

![image](https://user-images.githubusercontent.com/50571566/218345473-370077fd-fe30-445c-8d2b-eada818a4fef.png)

You can change the order of the Clues in the UI and their Location.

## Clue Location/Category

Speaking of the Location, this is another name for the Clue Category. Currently, to add/change/delete Clue Locations,
you will need to open the C++ file for the [EClueLocation](/Documentation/C++/ClueSystem/Enums/EClueLocation) 

Here is where you can find the header file

![image](https://user-images.githubusercontent.com/50571566/218345588-8915a863-1aa5-438b-aecb-aa8a73f944df.png)

You will find something like

```c++
#pragma once

UENUM(BlueprintType)
enum EClueLocation
{
    CL_Forest,
    CL_House
}
```

Just extend this, just simply add another item to the list so it will look like:

```c++
#pragma once

UENUM(BlueprintType)
enum EClueLocation
{
    CL_Forest,
    CL_House,
    CL_City
}
```

Save it, and compile the project. When you open the project up again, this will appear in the Clue Config
as an option.

## Data Assets

So we now have how we setup the system, and how to extend it with our own locations/categories. Let's move 
onto the meat of the system which is setting up the clues themselves. 

This isn't a Blueprint, but you shouldn't need to touch the C++ implementation, just create a new instance of the Data Asset.

![image](https://user-images.githubusercontent.com/50571566/218345094-d4e914c7-29af-48a0-a721-464d05604dd9.png)
![image](https://user-images.githubusercontent.com/50571566/218345103-0ce3aebb-3269-43c2-8c9a-300e4357d27e.png)
![image](https://user-images.githubusercontent.com/50571566/218345121-d8fe86ee-0a47-4778-a2c7-0625f061e276.png)
![image](https://user-images.githubusercontent.com/50571566/218345138-a62fbc0e-6497-4fb5-a664-c2cc361e1afa.png)

You can change which type of Clue Display you want, Mesh or Image. If you had a prerendered image of a clue that you wanted to use, then you would disable UsesMesh.
For the Mesh, you can obviously choose which static mesh you want to choose, how far away from the camera it should be and a default rotation and location offset.
This means you can finely control where and how the Clue looks.

![image](https://user-images.githubusercontent.com/50571566/218345194-9730e615-a23f-4d2d-936a-f45e944a1c97.png)

To make the web of clues, you simply just add in an element to the Additional Information array.
This will automatically populate the UI with the extra spots. 

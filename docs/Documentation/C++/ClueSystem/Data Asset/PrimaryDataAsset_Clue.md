# PrimaryDataAsset_Clue


This is the base class for the Clue Data Assets. If you want to create more types of clues, 
just inherit from this class. 

This isn't a Blueprint, but you shouldn't need to touch the C++ implementation, just create a new instance of the Data Asset.

Straight out of the box you can create 2 types of Data Assets. If you want to create an additional Clue Type, you can extend this class in a new child
class and assign a User Widget that will handle the Inspection, which needs to implement the [IClueSystemUI_Interface](/docs/Documentation/C%2B%2B/ClueSystem/Interfaces/IClueSystemUI_Interface.md) in order to work. 

## [ClueTypeMesh](/docs/Documentation/Content/Clue%20Types/ClueTypeMesh.md)

![](https://imgur.com/m0z2r6i.png)

## [ClueTypeImage](/docs/Documentation/Content/Clue%20Types/ClueTypeImage.md)

![](https://imgur.com/doaLlOH.png)

This means you can finely control where and how the Clue looks.

![image](https://user-images.githubusercontent.com/50571566/218345194-9730e615-a23f-4d2d-936a-f45e944a1c97.png)

To make the web of clues, you simply just add in an element to the Additional Information array.
This will automatically populate the UI with the extra spots. 
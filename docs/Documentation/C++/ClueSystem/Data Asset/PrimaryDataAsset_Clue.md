# PrimaryDataAsset_Clue


This is the base class for the Clue Data Assets. If you want to create more types of clues, 
just inherit from this class. 

This isn't a Blueprint, but you shouldn't need to touch the C++ implementation, just create a new instance of the Data Asset.

![image](https://user-images.githubusercontent.com/50571566/218345121-d8fe86ee-0a47-4778-a2c7-0625f061e276.png)
![image](https://user-images.githubusercontent.com/50571566/218345138-a62fbc0e-6497-4fb5-a664-c2cc361e1afa.png)

You can change which type of Clue Display you want, Mesh or Image. If you had a prerendered image of a clue that you wanted to use, then you would disable UsesMesh.
For the Mesh, you can obviously choose which static mesh you want to choose, how far away from the camera it should be and a default rotation and location offset.
This means you can finely control where and how the Clue looks.

![image](https://user-images.githubusercontent.com/50571566/218345194-9730e615-a23f-4d2d-936a-f45e944a1c97.png)

To make the web of clues, you simply just add in an element to the Additional Information array.
This will automatically populate the UI with the extra spots. 
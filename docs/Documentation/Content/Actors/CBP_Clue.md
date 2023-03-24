# CBP Clue

This is main Blueprint to place a Clue in the World. It has a UPROPERTY to control what clue they are, that is only editable on instances of the class in the World.

![image](https://user-images.githubusercontent.com/50571566/218344852-2dd459ec-d44e-4e36-be95-548f813d820a.png)

You can control whether or not to load in the mesh that is held on the Primary Data Asset on Construction. You may want to turn it off it is a complex mesh or don't think it is necessary.
Alternatively, you may want it to easily compare meshes in the world and only having to change one thing (in the Data Asset)

![image](https://user-images.githubusercontent.com/50571566/218344918-6d2856f9-2f4f-4035-ba26-a19e5af7e2aa.png)

To actually pickup the Clue, there is a Blueprint Callable function that can be used:
![image](https://user-images.githubusercontent.com/50571566/218345980-bd091199-28de-4ddb-a4ec-4df99d6d1c66.png)

I'm using it with an interface that I'm using in my main project
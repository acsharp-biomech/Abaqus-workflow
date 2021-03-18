# Part 2
## Create an analysis Step

You will need to create an analysis step at which point the load is applied. An "Initial Step" is already created when you import the model. You can apply constraints to this step and they will carry through to the analysis step.

Double click the Step option in the model tree, name the Step and select the type of Step is it (e.g. Static, General). Another dialog box will appear where you can write a description and change some settings. However, the default settings are usually used.

![image](https://user-images.githubusercontent.com/80410515/111634371-5a301980-87ee-11eb-9a14-3ac49875c7a2.png)

## Creating a Set
You sometimes need to create a Set of nodes so that you can apply a load or constraint over the entire set.

To do so, expand the Assembly option in the model tree and double click Sets.

When selecting the nodes for a set, you only want to select the external nodes, so make sure you select this option in the toolbar ![image](https://user-images.githubusercontent.com/80410515/111634538-877cc780-87ee-11eb-8d6d-8b6776753436.png). To select an area, LMB + drag the mouse over the area. You can also change the drag shape ![image](https://user-images.githubusercontent.com/80410515/111634585-92375c80-87ee-11eb-8b9b-cf9cae545438.png). This will still select all the nodes on the other side of the surface, so rotate the model and deselect all the unwanted nodes. This can sometimes be very tricky, especially if the area is very curved or thin, so be patient. Alternatively, if you don't have too many nodes to select, do it one by one. 

## Setting up a “floating” Datum and reference point (RP)
In the top menu bar go to Tools > Datum and the Create Datum dialog box will appear. Or, you can click one of these icons in the Assembly Module drop-down list: ![image](https://user-images.githubusercontent.com/80410515/111636409-5c937300-87f0-11eb-84d4-ffa89abe92ab.png) to offset from a single point, or ![image](https://user-images.githubusercontent.com/80410515/111636450-67e69e80-87f0-11eb-89a0-74d22abf5202.png) to select a midpoint between 2 points (hold the icon to see the different menu options). 

You have different options for how to place your datum: (1) you can Enter the exact coordinates, (2) you can offset the datum from a point on your model by selecting the point and typing in an offset value in the x- y- or z-axis (this is usually the best option), or (3) you can select two points and have the datum midway between them. These will be the most common selection you will need, but there are others.

![image](https://user-images.githubusercontent.com/80410515/111636618-8fd60200-87f0-11eb-959d-fbcc4d67c821.png)

Now you can make the datum a Reference Point by selecting the ![image](https://user-images.githubusercontent.com/80410515/111636660-98c6d380-87f0-11eb-9c37-2c4f9ab3d654.png)
 icon under the Interaction Module. 

## Setting up a new/local CSYS
You can create a new CSYS by clicking ![image](https://user-images.githubusercontent.com/80410515/111636886-cd3a8f80-87f0-11eb-8ffa-af3b7704e0c2.png) or select an existing CSYS with ![image](https://user-images.githubusercontent.com/80410515/111636912-d592ca80-87f0-11eb-8bb6-d8bafe5a22bb.png). Or, in the Assembly Module drop-down list, you can select the icon in the bottom right hand corner ![image](https://user-images.githubusercontent.com/80410515/111636945-dd526f00-87f0-11eb-9495-7db172c2cdfa.png).

•	To create a new CSYS click ![image](https://user-images.githubusercontent.com/80410515/111637027-f0fdd580-87f0-11eb-94b2-4509743764bd.png) or ![image](https://user-images.githubusercontent.com/80410515/111637049-f824e380-87f0-11eb-9da7-416907acd672.png) and select  Rectangular. Select a point to be the origin (the centre of the set, or origin of the muscle, is the best option) and then select a point to be the direction of the x-axis. The direction of the x-axis should be the direction of the load (e.g. from muscles origin to insertion). Click Create Datum and you're done. The Create Datum CSYS dialog box will appear again if you want to create more CSYS, or click cancel if you don't. Coordinate systems will appear under Features under the Assembly in the Model Tree.

•	If you need to create a datum point and reference point (RP) offset from your model that represents the insertion of a muscle on the jaw (if you don’t have a jaw model to load), you will need to create a datum and RP before you create your new CSYS.


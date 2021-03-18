# Part 2
## Create an analysis Step

You will need to create an analysis step at which point the load is applied. An "Initial Step" is already created when you import the model. You can apply constraints to this step and they will carry through to the analysis step.

Double click the Step option in the model tree, name the Step and select the type of Step is it (e.g. Static, General). Another dialog box will appear where you can write a description and change some settings. However, the default settings are usually used.

![image](https://user-images.githubusercontent.com/80410515/111634371-5a301980-87ee-11eb-9a14-3ac49875c7a2.png)

## Creating a Set
You sometimes need to create a Set of nodes so that you can apply a load or constraint over the entire set.

To do so, expand the Assembly option in the model tree and double click Sets.

When selecting the nodes for a set, you only want to select the external nodes, so make sure you select this option in the toolbar ![image](https://user-images.githubusercontent.com/80410515/111634538-877cc780-87ee-11eb-8d6d-8b6776753436.png). To select an area, LMB + drag the mouse over the area. You can also change the drag shape ![image](https://user-images.githubusercontent.com/80410515/111634585-92375c80-87ee-11eb-8b9b-cf9cae545438.png). This will still select all the nodes on the other side of the surface, so rotate the model and deselect all the unwanted nodes. This can sometimes be very tricky, especially if the area is very curved or thin, so be patient. Alternatively, if you don't have too many nodes to select, do it one by one. 

## Apply Boundary Conditions (BC)
This is where you apply your constraints to prevent rigid body motion. In the dialog box that appears, name your BC and select the Step (e.g. Initial), Category (e.g. Mechanical) and Type (e.g. Displacement/Rotation).

![image](https://user-images.githubusercontent.com/80410515/111634856-d0348080-87ee-11eb-9650-999d26b3118f.png)

Uncheck the Create Set option in the task bar… ![image](https://user-images.githubusercontent.com/80410515/111634901-da567f00-87ee-11eb-82d1-567511056552.png)

Select the nodes for your constraint and then select the axis you want to fix (no displacement) in the dialog box that appears. To select multiple nodes, hold the Shift key. To deselect nodes, hold the Ctrl key.

For a completely fixed constraint, select the x-, y- and z-axis (U1, U2, U3). For a semi-fixed constraint, only select the axis you want to restrict movement in (see figure below).


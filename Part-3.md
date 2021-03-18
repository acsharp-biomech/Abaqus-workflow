# Part 3
## Apply Boundary Conditions (BC)
This is where you apply your constraints to prevent rigid body motion. In the dialog box that appears, name your BC and select the Step (e.g. Initial), Category (e.g. Mechanical) and Type (e.g. Displacement/Rotation).

![image](https://user-images.githubusercontent.com/80410515/111634856-d0348080-87ee-11eb-9650-999d26b3118f.png)

Uncheck the Create Set option in the task bar… ![image](https://user-images.githubusercontent.com/80410515/111634901-da567f00-87ee-11eb-82d1-567511056552.png)

Select the nodes for your constraint and then select the axis you want to fix (no displacement) in the dialog box that appears. To select multiple nodes, hold the Shift key. To deselect nodes, hold the Ctrl key.

For a completely fixed constraint, select the x-, y- and z-axis (U1, U2, U3). For a semi-fixed constraint, only select the axis you want to restrict movement in (see figure below).

![image](https://user-images.githubusercontent.com/80410515/111637833-b3e61300-87f1-11eb-9273-d56dfcbc561f.png)

Create all you BC, naming each separately. 
If you want to edit a BC, double click the BC to edit and the dialog box will reappear so you can change the region picked ![image](https://user-images.githubusercontent.com/80410515/111637931-c6604c80-87f1-11eb-8bc5-55ac62c42f46.png), change the coordinate system (CSYS) or set up a new coordinate system ![image](https://user-images.githubusercontent.com/80410515/111637994-d2e4a500-87f1-11eb-8ac6-b9b26a178f19.png)
, or change the axis that are fixed. 

## Apply Loads to nodes
To create a load, double click the Load option in the model tree. In the dialog box that appears you can name the load and select the Step, Category (e.g. Mechanical) and Type (e.g. Concentrated force).

![image](https://user-images.githubusercontent.com/80410515/111638131-f6a7eb00-87f1-11eb-87e2-1d54a7c75d93.png)

Then select the nodes on the model that you want to load to be applied to. If you want to add the load to a set of nodes, it is easier to first create a set (see next step).

Apply the load in the CF1 section (x direction). Note that the force will be applied per node, so you need to know how many nodes are in your set if you are using a set! 

When the load is applied, yellow arrows will appear on your model. Double check the direction of the arrows to make sure they are in the correct direction. 

When you have set up all the loads, make sure only one arrow originates from each node. If a Set of nodes overlaps, loads will be applied in two or more separate coordinate systems from any overlapping nodes. This will appear as an error if you try to run the simulation:


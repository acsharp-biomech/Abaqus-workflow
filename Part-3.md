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

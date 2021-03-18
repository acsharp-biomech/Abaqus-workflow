# Part 3
## Apply Boundary Conditions (BC)
This is where you apply your constraints to prevent rigid body motion. In the dialog box that appears, name your BC and select the Step (e.g. Initial), Category (e.g. Mechanical) and Type (e.g. Displacement/Rotation).

![image](https://user-images.githubusercontent.com/80410515/111634856-d0348080-87ee-11eb-9650-999d26b3118f.png)

Uncheck the Create Set option in the task bar… ![image](https://user-images.githubusercontent.com/80410515/111634901-da567f00-87ee-11eb-82d1-567511056552.png)

Select the nodes for your constraint and then select the axis you want to fix (no displacement) in the dialog box that appears. To select multiple nodes, hold the Shift key. To deselect nodes, hold the Ctrl key.

For a completely fixed constraint, select the x-, y- and z-axis (U1, U2, U3). For a semi-fixed constraint, only select the axis you want to restrict movement in (see figure below).

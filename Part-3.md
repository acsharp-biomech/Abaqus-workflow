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

*"Following attributes are applied to overlapping, intersecting, or adjoining regions in different coordinate systems."*

Go back into the Sets and edit them to remove overlapping nodes. 

## Applying loads to a set
Double click the Load option in the model tree. In the dialog box that appears you can name the load and select the Step, Category (e.g. Mechanical) and Type (e.g. Concentrated force). Then select the Set for the load, select ![image](https://user-images.githubusercontent.com/80410515/111638478-45ee1b80-87f2-11eb-918a-ca81398c47cf.png) on the right hand side of the task bar, and select the set in the list the appears. 

Apply the load in the CF1 section (x direction). Note that the force will be applied per node, so you need to know how many nodes are in your set if you are using a set! 

Also note that when you set up a load this way, the force will be parallel, directed along the x-axis of the CSYS from each node. If you want to set up a load from a Set with each node having a different direction, like the fan shape of the temporalis muscle, you can set up a coupling constraint.

## Setting up a coupling constraint
A coupling constraint is useful if you want to set up a load from an area (e.g. muscle origin) and direct it to a single point so that the force is applied to all the nodes in a different direction, like a fan (this is good for the temporalis muscle!).

Make a Set for the muscle origin, but instead of applying the load to the Set, you need to make a Datum point and connect a coupling constraint from the datum to the set. This makes the nodes in the Set constrained to the rigid body motion of a single node. Make sense? Here's how to do it...

Add the coupling constraint by double clicking the ![image](https://user-images.githubusercontent.com/80410515/111638782-92395b80-87f2-11eb-92ff-de3c5065719a.png) icon in the model tree. Name your constraint and select "Coupling" in the dialog box that appears. You will then be asked to select the Control Point, so select Geometry and then select the RP. Click Done. Now select the node region you want to constrain (e.g. your Set) and the next dialog box will appear.

![image](https://user-images.githubusercontent.com/80410515/111638809-982f3c80-87f2-11eb-84d4-02dddfd40611.png)

Make the coupling type distributed, not kinematic (read about the different in the Abaqus Documentation Manual), constrain all the degrees of freedom and specify the CSYS you want the constraint to be in (select the CSYS set up for that set with the x-axis in the direction of the force).

Now you can set up a Load and apply the force to the RP. This will distribute the Load through the coupling constraint to the nodes at the muscle origin. 

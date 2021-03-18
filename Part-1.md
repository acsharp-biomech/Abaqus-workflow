# Step-by-step Instructions
## 1. Import a model
Before importing a model into Abaqus it is important to make sure your mesh is good quality. The better quality your surface mesh is in Avizo (or whatever meshing software you use – Hypermesh, Mimics, 3Matic, Blender etc.), the better quality the tetrahedral mesh will be (for producing a high-quality mesh in Avizo, see my Avizo protocol). If the mesh has errors, such as high aspect ratio triangles, it may not run in Abaqus, which means you will have to start all over again and produce a better mesh. Get it right the first time and never look back!

Abaqus can import many file types; I have only used an Abaqus Input file (.inp) and NASTRAN, exported from Avizo. Importing a .inp model from Avizo or Hypermesh will set up a Part and an Instance for the Assembly. If you have multiple materials in your mesh that you want to apply different material properties to in Abaqus, it is better to save it as a NASTRAN file, because this will set up different sets, sections and materials when you import it to Abaqus.

File > Import > Model, select file type Abaqus Input File (.inp) or NASTRAN Bulk file (.bdf, .dat, .nastran etc.) and import the model.

When the model imports, it will set up one or more Sets found under Part and/or Assembly in the model tree. A couple of important ones are: EALL, a set of all the elements; NALL, a set of all the nodes, because these tell (remind) you how many elements and nodes are in your model. These may be different in different version of the software, or depending on the software from which you export your model. When you hover your mouse over a Set it will tell you the type (element or node) and size.

## 2. Importing a second model (Part)
Importing a second Part and Instance, such as a jaw, can be done separately so that the jaw can be excluded from the simulation. The jaw can then be used to correctly align the loads. If you have a jaw as a seperate material that you saved and imported together as a NASTRAN file, this step is unnessesary. 

Import the second model as above in a separate Abaqus Database and save the database in the Abaqus/CAE Database format (.cae). Then, in the Abaqus database that you want to work in (e.g. set up simulations and run FEA on the cranium) import the jaw model as follows: 

File > Import > Model, select file type Abaqus/CAE Database (.cae)

In the dialog box that appears, select After import, show "Model->Copy Objects" dialog

![image](https://user-images.githubusercontent.com/80410515/111630399-3cf94c00-87ea-11eb-8ef2-13f25e02fb08.png)

Another dialog box will appear. Select the Part and Instance you want to copy

![image](https://user-images.githubusercontent.com/80410515/111630442-471b4a80-87ea-11eb-80bc-8fb2ac543ce6.png)

When the new model has imported, it might need to be realigned.

Select Assembly in the drop down menu next to Module in the toolbar ![image](https://user-images.githubusercontent.com/80410515/111631298-2273a280-87eb-11eb-9685-ace0180e25ac.png)

To translate an Instance with respect to another, select the Translate Instance tool ![image](https://user-images.githubusercontent.com/80410515/111631347-315a5500-87eb-11eb-8233-167e3b9bced4.png) then select the Instance to be moved. To rotate the Instance, select the Rotate Instance tool ![image](https://user-images.githubusercontent.com/80410515/111631379-3c14ea00-87eb-11eb-95f4-d40e60973cd2.png).

## 3. Create Materials
Under the Model tab on the LHS of the screen expand your selected model (you can also delete Model-1 and any other models you don't need). In the model tree, double click on Materials. Name your material and select the type of material it is e.g. Elastic, Isotropic. Enter the Young's Modulus (e.g. 20E9 for 20 GPa) and Poisson's Ratio (e.g. 0.3) in the Data section window (see below). If a material is already created with your imported model (.inp), you can double click on the material to edit it and add its properties.

![image](https://user-images.githubusercontent.com/80410515/111631806-c1000380-87eb-11eb-9e9d-766b0e2ab5b9.png)

## 4. Create a Section that you want to assign the material
If a Section has already been set up when you import your model, you don’t need to do this step. But, it’s important that you make sure the Section is “Solid, Homogeneous”, and assigned to the correct material. 

Double click on the Section option in the model tree, name your section and select the Category (e.g. Solid) and Type (e.g. Homogeneous), click Continue...

![image](https://user-images.githubusercontent.com/80410515/111632442-62875500-87ec-11eb-8d58-e1e04bae1c67.png)

A second dialog box (above right) will appear to select the material for the section.

## 5. Assign the Section to your model
If a Section Assignment has already been set up when you import your model, you don’t need to do this step, but it is best you check that the section you want it assigned to the correct region/part and material. 

Expand the Part you want to assign the section to and double click the Section Assignments option.

Uncheck the Create Set option in the task bar. You can select the region individually (each element, or select the entire model) using the mouse, or you can select the region using a set you have already created (or a set created for you if you have multiple materials) by clicking the “Sets…” button on the right. Then click Done. 

![image](https://user-images.githubusercontent.com/80410515/111632641-98c4d480-87ec-11eb-89b0-969d12df5da0.png)

Note: When making a selection of the model, it is import to have the right options chosen. In the top toolbar there is an option to select ALL elements/nodes ![image](https://user-images.githubusercontent.com/80410515/111632691-a712f080-87ec-11eb-9e02-7071bd83d217.png), just the EXTERNAL elements/nodes ![image](https://user-images.githubusercontent.com/80410515/111632749-b72ad000-87ec-11eb-8ba5-41048d427b19.png) or just the INTERNAL elements/nodes ![image](https://user-images.githubusercontent.com/80410515/111632798-c1e56500-87ec-11eb-8e04-fc9a63b91117.png).





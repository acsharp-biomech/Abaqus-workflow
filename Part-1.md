# Step-by-step Instructions
## 1. Import a model
Before importing a model into Abaqus it is important to make sure your mesh is good quality. The better quality your surface mesh is in Avizo (or whatever meshing software you use – Hypermesh, Mimics, 3Matic, Blender etc.), the better quality the tetrahedral mesh will be (for producing a high-quality mesh in Avizo, see my Avizo protocol). If the mesh has errors, such as high aspect ratio triangles, it may not run in Abaqus, which means you will have to start all over again and produce a better mesh. Get it right the first time and never look back!

Abaqus can import many file types; I have only used an Abaqus Input file (.inp) and NASTRAN, exported from Avizo. Importing a .inp model from Avizo or Hypermesh will set up a Part and an Instance for the Assembly. If you have multiple materials in your mesh that you want to apply different material properties to in Abaqus, it is better to save it as a NASTRAN file, because this will set up different sets, sections and materials when you import it to Abaqus.

File > Import > Model, select file type Abaqus Input File (.inp) or NASTRAN Bulk file (.bdf, .dat, .nastran etc.) and import the model.

When the model imports, it will set up one or more Sets found under Part and/or Assembly in the model tree. A couple of important ones are: EALL, a set of all the elements; NALL, a set of all the nodes, because these tell (remind) you how many elements and nodes are in your model. These may be different in different version of the software, or depending on the software from which you export your model. When you hover your mouse over a Set it will tell you the type (element or node) and size.

## Importing a second model (Part)
Importing a second Part and Instance, such as a jaw, can be done separately so that the jaw can be excluded from the simulation. The jaw can then be used to correctly align the loads. Import the second model as above in a separate Abaqus Database and save the database in the Abaqus/CAE Database format (.cae). Then, in the Abaqus database that you want to work in (e.g. set up simulations and run FEA on the cranium) import the jaw model as follows: 
